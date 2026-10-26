# Combat, money, power, and special effects

[Guide index](README.md) | [Weapon reference](reference/WEAPONS.md) | [Buildings](04-BUILDINGS.md)

**Evidence:** numeric examples below use the extracted effective rules. The per-object cards distinguish RA2 and Yuri and the mission pages list local overrides. Workflows are readable reconstructions of the rules, manuals and identified engine responsibilities; they are not a line-by-line description of every original routine.

## 1. Follow a shot through four records

1. The attacker chooses an available weapon.
2. The weapon specifies a base effect, firing interval, range and a projectile reference.
3. The projectile specifies how the effect travels and which target domains it can reach.
4. The warhead specifies how the effect interacts with armor and whether special handling is required.
5. The target contributes armor, health, position, ownership and any special protection.
6. The engine resolves the encounter, updates state, and emits animations/sound/events.

The same shell appearance can accompany different damage rules. Conversely, two different-looking attacks can share a warhead. Weapon names are references, not enough information by themselves to predict an outcome.

## 2. Ordinary damage, explained carefully

A useful starting estimate is: base damage multiplied by the warhead's effectiveness against the target's armor. After that, the real engine can apply veterancy, distance/spread, difficulty, special protection and rounding. This is a learning approximation, not a complete universal damage formula.

The armor-effectiveness list has eleven positions: unarmored infantry; flak-armored infantry; plate-armored infantry; light vehicle; medium vehicle; heavy vehicle; wood structure; steel structure; concrete structure; special category 1; special category 2. These category names are game classifications, not a physical materials model.

1. Find the target's armor class on its card.
2. Find that class's position in the warhead's effectiveness list.
3. Check whether the percentage is zero or strongly reduced.
4. Check whether the weapon/projectile is even allowed to engage that target.
5. Only then compare health, base damage and reload interval.

Zero effectiveness and inability to target are distinct. An attack can also do negligible damage while a different secondary weapon is appropriate. A rapid anti-infantry gun is not automatically a good anti-tank weapon because its animation is busy.

## 3. Range and reload are independent

1. A target enters weapon range.
2. The attacker turns or positions itself as needed.
3. It waits for its reload and ammunition rules.
4. It releases one shot or a burst.
5. The effect may take more time to reach the target.
6. The next legal firing opportunity is checked again.

The displayed speed stat is not kilometers per hour. The firing interval field is not seconds. A weapon with a burst is not equivalent to multiplying every displayed number together and calling that exact damage per second. Travel time, misses, target changes and special effects matter.

## 4. Armor, health and experience

1. Health determines how much damage the live object can still sustain.
2. Armor determines which effectiveness multiplier ordinary attacks use.
3. Training eligibility determines whether the object gains rank.
4. Experience and the configured thresholds determine promotion.
5. Veteran/elite ability lists determine which improvements apply.
6. An elite weapon reference can replace an ordinary weapon, changing the attack itself.

Do not assume every elite object receives every possible bonus. The cards retain each explicit ability list. An object's cost, its score value, and the experience contribution associated with destroying it are related data concepts, but are not interchangeable labels.

## 5. The three resource-gathering workflows

### War Miner

1. Locate accessible ore/gems.
2. Drive to the resource and collect into its storage.
3. Return to an eligible refinery when required.
4. Wait for/dock at the unloading point.
5. Convert the delivered resource into the owner's economy and go out again.
6. Use its gun for supported combat situations; that does not make it invulnerable or exempt from needing a refinery.

### Chrono Miner

1. Drive outward to reachable resource cells.
2. Gather into its smaller cargo capacity under its rules.
3. Use its chrono return procedure toward an eligible refinery.
4. Complete unloading and resume the outward journey.
5. If the destination cannot be used, the engine must handle that condition; teleport capability does not guarantee a legal refinery always exists.

### Slave Miner

1. Move the mobile miner to a usable deposit.
2. Deploy into its linked building form.
3. Its manager supplies slave workers, which travel out, collect and return ore.
4. Process deliveries locally rather than routing a conventional ore truck back to a remote refinery.
5. Replace lost workers according to the configured regeneration delay.
6. Undeploy into the mobile form to relocate when appropriate.

The mobile and deployed forms are separate type records connected by deployment references. They are not two independent income sources simply because both appear in the catalogue.

## 6. Resource cells and income modifiers

1. A map places resource-bearing cells and controls relevant growth settings.
2. The resource type contributes its configured value and amount.
3. A harvester or worker removes resource while collecting.
4. Delivery converts cargo into usable economic value.
5. Applicable purifier or other modifiers adjust the result.
6. Credits are spent on production, repairs and other supported actions.

Yuri's effective global purifier bonus is 0.25. That is a configured bonus factor, not proof that every map grants it or every resource-related event receives it. A mission can replace rules, provide scripted cash or use a different production setup.

For an Oil Derrick, the effective Yuri record explicitly gives 1,000 startup credits, 20 recurring credits and a recurring delay of 100 simulation frames. Do not read that as 20 credits every 100 seconds. Ownership, capture handling and scenario overrides still matter.

## 7. Power is an owner-wide service

1. Sum the active output of the owner's generating structures under their current conditions.
2. Sum the requirements of the owner's consuming structures.
3. Compare supply with demand.
4. Apply power-dependent effects: relevant defenses, radar, production conditions, special weapons and powered units.
5. Recalculate when construction, damage, ownership or other state changes require it.

The cards report signed power: positive generates, negative consumes. A missing value is reported as unspecified, not silently changed to zero. A Bio Reactor also depends on its occupants. A Robot Tank depends on its control infrastructure. A Floating Disc can impose a different kind of shutdown through its drain effect.

## 8. Repairs and selling

1. A building repair request checks whether ordinary repair is permitted.
2. While repairing, spend credits and restore health through the repair procedure.
3. Stop at full health, on cancellation, or when the state no longer permits repair.
4. An Engineer entering a suitable damaged friendly building uses an entry-based repair path instead.
5. A service depot or repair IFV uses its supported vehicle-repair path.
6. Selling, where allowed, removes the owned structure and applies refund/survivor rules rather than applying ordinary weapon damage.

A structure can be capturable but unsellable. A mobile unit can self-heal but not be trainable. These are independent switches, which is why the catalogue reports explicit values rather than inferring all behavior from the object's appearance.

## 9. Capture, disguise and mind control are different workflows

### Engineer capture

1. Select a building that the current Engineer can enter.
2. Check eligibility and ownership.
3. Reach the entry point.
4. Apply capture or the appropriate friendly-repair operation.
5. Notify the mission about the interaction and update the new owner's services.

### Spy infiltration

1. Adopt a supported enemy infantry disguise.
2. Move through the battlefield while avoiding units that expose or kill the spy.
3. Enter a spyable enemy structure.
4. Apply the structure-specific infiltration result: power disruption, economic theft, radar reset or a technology/training benefit as supported.
5. Notify any mission-specific spy event.

### Ordinary mind control

1. Check the target's eligibility and immunity.
2. Establish a control relationship if the attack succeeds and the controller has the relevant capacity.
3. Let the controlled object act for the controlling side.
4. Maintain or release that relationship according to the controlling mechanism.
5. Handle controller destruction, release and exceptional effects through that mechanism's rules.

Do not describe the Psychic Dominator as an ordinary Yuri Clone with a larger radius. Its persistent capture effect is a separate special weapon behavior. Do not describe a mission's mass ownership-change action as proof that every unit was individually hit by a mind-control weapon.

## 10. Special combat mechanisms

| Mechanism | Readable sequence | Why ordinary damage estimates fail |
|---|---|---|
| Chrono erasure | Attach temporal effect; hold target in the temporal interaction; accumulate removal progress; finish or release if interrupted | Health subtraction is not the whole mechanism |
| Terror Drone parasite | Reach a valid victim; enter its parasite relationship; apply internal damage; handle victim destruction/removal | The visible drone can disappear inside the victim |
| Giant Squid | Reach a valid naval victim; attach and damage; handle release/interruption | The victim's movement and attachment state matter |
| Mind control | Validate susceptibility; acquire relationship; maintain capacity and ownership effect | The weapon's damage field can serve special logic |
| Gattling | Fire and accumulate stage progress; choose stage weapons; lose stage progress when firing ceases | Damage output depends on sustained engagement |
| Magnetron | Choose vehicle-lift or structure-damage interaction; move the affected vehicle according to magnetic logic; release/place it | Lifting and displacement can be the main outcome |
| Carrier/Dreadnought/V3 | Manage spawned attack objects; launch; resolve their independent travel/attack; reload or replace | The launcher may not deliver the impact directly |
| Radiation/poison | Create a damaging site/effect; test eligible nearby objects over its lifetime; decay/remove | The consequence lasts beyond the initial attack |
| C4/Ivan bomb | Reach/place the attached effect; wait for applicable fuse or immediate demolition; detonate or disarm if supported | Detonation is separate from the original targeting click |
| Transport open-topped fire | Carry infantry; allow eligible passenger weapons to fire through the host's rules | Passengers contribute weapons while the host provides movement |

## 11. Superweapons, one cycle at a time

1. Own the granting structure or receive a scripted grant.
2. Check the weapon's power/availability conditions.
3. Advance its charging state.
4. When ready, accept a legal target or the relevant AI/script request.
5. Execute that weapon's dedicated effect.
6. Reset/recharge, or consume a one-use grant.

Nuclear attack resolves launch/flight/impact and aftermath. Weather Control produces a timed storm. Iron Curtain applies temporary protection to eligible targets. Chronosphere separates a selected group/area from its destination and applies placement consequences. Genetic Mutator transforms eligible infantry through mutation rules. Force Shield protects an area of structures while imposing its configured drawback. These are distinct procedures sharing a charge-and-target interface.

Campaign triggers can set charge, change the next recharge duration, select preferred targets or invoke effects at a waypoint. A campaign countdown can therefore differ from the usual skirmish building's recharge cycle. Read the mission's timer actions before assuming a universal interval.

## 12. Worked reading exercise

Suppose a tank seems unable to damage a hovering opponent.

1. Look up both type cards and select the right game version.
2. Determine whether the target is treated as airborne at that moment.
3. Follow the attacker's normal and secondary weapon links.
4. Check their projectile target domains.
5. Check warhead effectiveness and the target's immunity fields.
6. Check range, current orders and any local mission override.
7. Only after those checks investigate an input or runtime fault.

This procedure distinguishes a designed limitation, a scenario-specific rule and a possible implementation defect without requiring you to read source code.
