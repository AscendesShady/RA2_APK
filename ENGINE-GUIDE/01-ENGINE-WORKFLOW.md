# How the engine works, one decision at a time

[Reading order and evidence labels](README.md) | [Units](02-UNITS.md) | [Buildings](04-BUILDINGS.md) | [Missions](05-CAMPAIGNS.md)

This chapter explains the original RA2 and Yuri engine in ordinary language. A unit is a soldier, vehicle, ship, aircraft, or other mobile object. A structure is a building, defense, landmark, or map prop. A house is an owner: a player, enemy army, civilian group, or scripted faction. An algorithm is simply a repeatable sequence of decisions.

## 1. The four things that cooperate

| Layer | What it contributes | Example |
|---|---|---|
| Original executable | General procedures and special behavior | How a vehicle moves, how an Engineer enters a building, how a trigger fires |
| Rules and art data | Settings and references | Tank health, weapon selection, prerequisites, model and animation |
| Scenario map | A particular battle's starting state and instructions | Which base exists, where Tanya starts, which bridge matters |
| Android host | Phone/tablet services and input adaptation | Two-finger right click, file access, video playback, presenting the frame |

**Confirmed from local files:** the delivered app has separate recompiled RA2 and Yuri libraries. It preserves the original games' procedures while replacing required operating-system services. It is therefore essential to select the correct rules and campaign, rather than treating Yuri as a collection of extra units added to the RA2 rules. See [sources](SOURCES.md).

## 2. What happens after you choose a game

1. The launcher identifies RA2 or Yuri's Revenge.
2. The host prepares that game's writable working directory and the required packaged assets.
3. The corresponding native library initializes the original program's memory and operating-system connections.
4. The game locates its archives. An archive is a container holding named resources; it is not itself the game simulation.
5. Rules describe available object types. Art records describe their appearance. String tables supply readable names and messages.
6. A campaign choice identifies a starting map. The campaign progression table identifies later stages.
7. The map supplies terrain, houses, starting objects, waypoints, tags, variables, teams, and local rule changes.
8. The engine creates live objects from those definitions and begins the scenario.

**Important finding:** some maps contain old-looking next-scenario fields that disagree with the campaign progression table. The mission catalogue follows the progression table and mission descriptions, rather than assuming every old field is an active campaign route.

## 3. A definition is different from a live object

A Rhino's definition is a recipe shared by all Rhinos in that ruleset. A particular Rhino on the battlefield has its own owner, current health, position, facing, order, target, and experience.

1. Read the shared Rhino recipe.
2. Create a new battlefield instance.
3. Give that instance its owner, starting position and starting condition.
4. Change the instance as it moves, fires or takes damage.
5. Leave other Rhinos alone unless the relevant rule affects them too.

This explains why two identical-looking tanks can have different health or rank. It also explains why a campaign can change all Rhinos in that scenario without changing the global skirmish recipe. A map's explicit overrides take precedence for the properties it replaces; unspecified properties still come from the effective rules.

## 4. One simulation step

**Conceptual reconstruction:** the following is a useful dependency order for learning. It is not a claim that every original function executes in exactly this order during every frame.

1. Collect pending commands and relevant events.
2. Decide which live objects can act: alive, present, enabled, and in a state that permits the action.
3. Advance movement and orders. Check whether a destination, target, transport or building is still valid.
4. Advance weapons, projectiles, special effects and recovery timers.
5. Apply damage, ownership changes, construction progress, money and power changes as their procedures require.
6. Notify mission logic about events such as entry, discovery, destruction or a changed flag.
7. Evaluate eligible mission conditions and execute their actions.
8. Update the visible battlefield, sidebar, sound and movies from the resulting state.
9. Repeat until paused, a mission outcome occurs, or the game exits.

Simulation time and display time are different. A smooth-looking display does not prove a different movement or weapon rule. Frame counts in data must not automatically be read as seconds on the wall clock. Pausing and changing game speed affect the relationship.

## 5. What a click means

1. Convert the physical input into the game's mouse coordinates and button state.
2. Determine what is under the cursor: interface control, terrain cell, unit, building, or empty space.
3. Consider the current selection and any modifier keys.
4. Ask what action those objects support. An Engineer may enter and capture; a tank may attack; a miner may harvest.
5. Show an appropriate cursor when the interface has enough information.
6. Queue or apply the selected order through the game's normal command path.
7. The object's later updates carry out the order; the click itself does not teleport it to completion.

Right click is contextual too. A short right click cancels/deselects in the normal interface. Holding right and moving pans the view. Panning changes the camera, not the position of the army. [Android adaptation](07-ANDROID-WORKFLOW.md) explains how touch and pen reach these same actions.

## 6. Movement: request, route, progress, reconsider

1. Establish a destination, or choose a position from which to interact with a target.
2. Check the object's movement type and the terrain it can use.
3. Consider cells, occupied spaces, bridges, ramps and other obstructions relevant to that movement type.
4. Find a usable route under those constraints.
5. Let the object's movement controller advance along it, turning and accelerating as applicable.
6. If something blocks the next part, wait, adjust, or request another route as the relevant procedure decides.
7. Stop or transition to another order when close enough, when the target disappears, or when a replacement command arrives.

**Boundary:** the exact search algorithm, tie-breaking rules and every movement exception have not been proved here. Calling the original pathfinder a particular textbook algorithm without tracing its routines would overstate the evidence. The extracted data does confirm different movement controllers and permitted zones. A submarine, hover transport, aircraft and ordinary tank do not share identical movement constraints.

An apparent pathfinding error can therefore have several causes: an impassable cell, an occupied exit, an illegal shoreline crossing, a vanished bridge, an attack position the unit cannot reach, or an order overridden by a script. Check these before assuming the route search failed.

## 7. Targeting and attacking

1. Obtain a target from a player order, a team script, or automatic acquisition.
2. Check whether it is a valid enemy or a permitted forced target.
3. Choose an eligible weapon for the target and the attacker's current state.
4. Check target category, relevant immunities, range, ammunition, reload and facing requirements.
5. Move into a usable attack position if necessary and possible.
6. Fire when ready. A shot may create a projectile, beam, temporal effect, capture attempt, spawned attacker, or another special action.
7. Resolve the effect using that weapon's associated logic and data.
8. Keep attacking, reacquire, or return to the next order as the target and attacker change.

A field named damage does not always mean ordinary health subtraction. Repair weapons, mind-control weapons and special effects reuse parts of the weapon system. See [combat](03-COMBAT-ECONOMY.md) and the linked weapon references on each unit card.

## 8. Building and the technology tree

1. Start with the owning house and its permitted faction/country.
2. Check technology level, prerequisites, special restrictions and build limit.
3. Find a suitable production facility or construction queue.
4. Spend credits as production advances; insufficient money can interrupt progress.
5. Apply the relevant production conditions, including power and scenario settings.
6. For a completed building, wait for a legal placement. For a completed mobile unit, find a valid exit or delivery mechanism.
7. Create/activate the object, update power and technology availability, and give it its initial order or rally destination.

Prerequisites are not a recommended build order. They are eligibility conditions. Owning a building, having enough power, having money, and having an unblocked factory exit are separate questions. A structure can unlock technology without directly producing that unit.

## 9. Mission logic is a network of conditions

1. A mission defines named triggers.
2. A trigger belongs to an owner and can be enabled or disabled for a particular difficulty.
3. Events describe what it waits for: elapsed time, a destroyed object, an entered area, an active flag, and so on.
4. A tag associates certain triggers with placed objects or map cells.
5. When the required events have occurred, the trigger runs its action list in order.
6. Actions can show an objective, create a reinforcement, set a flag, enable another trigger, change ownership, or end the battle.
7. Persistence determines whether the attached logic can fire again or is consumed.

**Binary-supported detail:** the Yuri trigger action runner checks that the trigger is enabled and not destroyed, then walks its action list and calls the action executor for each item. A failure return from one action does not by itself make this a transactional sequence that rolls back earlier actions. The guide's mission ledgers therefore retain action order. They do not present the order of trigger records as a chronological story.

Multiple events can remember that different things happened at different times. They are not necessarily a demand that all visible events happen in the same instant. Enabling a trigger can reset its elapsed-time counters. This is why crossing an invisible boundary can start a new timer or attack wave.

## 10. Victory is an explicit outcome

1. Read the current objective, including newly displayed objectives.
2. Identify the object, owner, region or flag that represents completion.
3. Satisfy the appropriate mission event, rather than assuming the entire enemy army must always be destroyed.
4. Let any enabling triggers, remaining conditions, delays or scripted sequences complete.
5. The mission invokes its win/lose outcome action and then the score/progression flow.

Destroying a building and capturing it are different events. A scripted capture objective can fail if the building is destroyed. Conversely, destroying an objective may be sufficient even if enemy units remain. Each mission page shows its recorded terminal triggers and the steps feeding them.

## 11. Saving and loading

1. Pause into the game's options and request Save Game.
2. Initialize the original save dialog and its mission description.
3. In this Android build, append the device-local date and time to that description automatically.
4. Let the original save routine serialize the game's current state into its save format.
5. Acknowledge the original save confirmation through the Android bridge.
6. On load, restore the original game's saved objects and relationships, then continue its simulation.

This is different from saving a screenshot or merely remembering the mission number. A useful save must retain the battle's changing state. The existing QA confirms save/restart/load cases for RA2 and Yuri; it does not establish every possible mission or long-session save condition.

## 12. How the picture is produced

1. Determine which terrain and objects are visible in the current view.
2. Select the appropriate art, facing, animation, house color and lighting.
3. Draw terrain and objects with the engine's ordering/depth procedures.
4. For voxel models, use their model parts and transforms to produce an image; cached results can avoid repeating work.
5. Combine objects, shadows, effects, selection markers and the interface into the game surface.
6. The host scales/presents that surface on the Android display.

Infantry and many buildings use image sequences; many vehicles and aircraft use voxel models with part transforms. A three-dimensional-looking vehicle does not mean the entire engine is a modern free-camera 3D world. The local voxel research documents the separate model, cache, shadow and battlefield-copy stages. Enhancements described for the desktop presenter must not automatically be assumed enabled in the delivered Android APK.

## 13. A practical way to study any surprising event

1. Identify the live object and its type card.
2. Select RA2 or Yuri's rules. Compare any version difference on the card.
3. Check that mission's overrides and starting placement.
4. Follow the object's current order and special behavior.
5. Inspect its weapon and the target's armor/immunities.
6. Inspect attached tags, local flags and relevant mission triggers.
7. Separate simulation changes from camera, audio, movie and input effects.
8. Record what you actually observe in a saved test. Treat unobserved possibilities as explanations to test.

For a worked path through an actual scenario, start with [Lone Guardian](missions/ra2/all01t.md). For changing states within one unit, start with the [IFV, Chrono Miner and Slave Miner](02-UNITS.md).
