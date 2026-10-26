# How the computer army and mission scripts cooperate

[Guide index](README.md) | [Every mission](05-CAMPAIGNS.md) | [Global team reference](reference/AI-TEAMS.md)

The opponent is not one all-knowing decision procedure. House-level production, team recruitment, task-force composition, ordered scripts, target acquisition and scenario triggers cooperate. The exact target-ranking internals have not all been traced; the responsibilities and the extracted data below are still useful for understanding the workflow.

## 1. The vocabulary

| Term | Meaning |
|---|---|
| House | The owner of objects and a pool of money, power and production capabilities |
| Task force | A required roster, such as several tanks plus infantry |
| Team type | A template connecting owner, roster, script, recruitment and behavior flags |
| Team | A live instance trying to fill or execute that template |
| Script | An ordered list of actions, such as move, unload, attack, wait and repeat |
| AI trigger | A conditional/weighted opportunity to select a team template |
| Scenario trigger | A map's event/action rule, often controlling story sequences or waves |
| Waypoint | A named/numbered location used by scripts and scenario actions |

## 2. Ordinary team production

1. The house must be allowed to produce and have suitable facilities/resources under its rules.
2. Eligible AI decisions consider team templates and their conditions.
3. A selected team asks for its task-force roster.
4. Recruit existing eligible objects or produce missing objects according to the team and house rules.
5. Wait for readiness as required by the template/script.
6. Execute the script one action at a time.
7. Handle destruction, replacement, team limits and completion through the associated procedures.

The global AI reference lists the extracted templates and their rosters. Mission pages list their local templates. A definition's presence does not establish that the team actually spawns on every difficulty, or at all: it must be selected or invoked.

## 3. Create Team and Reinforcement mean different things

1. A Create Team action instantiates the team logic and attempts to obtain its members through the applicable recruitment/production path.
2. A Reinforcement action supplies new objects through the reinforcement mechanism.
3. A reinforcement-at-waypoint action also identifies the arrival location.
4. A chrono reinforcement uses a different arrival presentation/placement path.
5. The resulting team then follows its script unless other state changes intervene.

This difference explains why one scripted wave can arrive without the visible factory you expected, while another waits for units. It does not prove that all AI objects are free or that no economic rules ever apply.

## 4. Following a script

1. Start at its current script instruction.
2. Perform that instruction or wait until its completion requirement is satisfied.
3. Move to the next instruction.
4. A branch/repeat instruction changes which instruction is next.
5. A change-script instruction replaces the current plan; a change-team instruction changes the owning team relationship.
6. A destroy/disband instruction may remove objects or remove team organization depending on the actual action.

Script line numbers are reference positions, not seconds. A move can wait for progress, while a sound instruction can complete almost immediately. The script's apparent final action may never be reached if an earlier condition cannot be satisfied.

## 5. Why a force gathers before attacking

1. Assemble the roster.
2. Move to a staging waypoint or a gather position near a base.
3. Wait for transport loading or other readiness where required.
4. Approach the target or move to a specified enemy-building category.
5. Begin attack/attack-move/hunt under the relevant targeting behavior.
6. Repeat, change plan or dissolve as the script specifies.

Gathering is not necessarily indecision. Likewise, a unit left guarding after its transport unloads may have been intentionally removed from the continuing team. The unload action's continuation setting decides whether the transport, passengers, both or neither continue following that team script.

## 6. Campaign wave control

1. The map begins with only some triggers enabled.
2. A timer, discovered unit, entered cell or changed flag makes a trigger eligible.
3. Its actions can create a wave and enable its next timer/trigger.
4. Tags can report that a particular building or team-related object has been destroyed.
5. Further actions can disable earlier attacks, change ownership or open the next objective.
6. Difficulty flags can include/exclude parts of this network.

Two missions using the same tank can therefore feel very different. The tank recipe is only one input. Placement, wave timing, team size, script, player economy and mission overrides are separate inputs.

## 7. Ownership and alliances

1. Each live object belongs to a house.
2. House relationships determine allies/enemies for supported targeting decisions.
3. A mission can change those relationships.
4. It can transfer attached objects, all objects of a particular owner, or a scripted portion of a base through the relevant action.
5. Production, radar/power, target selection and objectives respond to the changed state.

An enemy suddenly becoming friendly can be a story action rather than a weapon hit. The exact trigger is shown in the mission ledger.

## 8. Difficulty without guessing

1. Read the scenario trigger's Easy/Normal/Hard eligibility flags.
2. Read explicit difficulty sections in the effective rules and any local replacement.
3. Inspect team availability, roster, delays and production settings.
4. Distinguish changed rules from a player taking a different route and activating more triggers.
5. Compare actual runs before claiming an exact difficulty effect that the data alone cannot settle.

The generated mission pages show the raw eligibility flags translated into their named difficulty slots. They do not assume all three are enabled. Rules also contain difficulty-indexed arrays; their ordering is specific to the consuming feature and must not be inferred from the label order on a different record.

## 9. How to read the detailed ledgers

1. Open the mission from [Campaigns](05-CAMPAIGNS.md).
2. Read its story/objective explanation first.
3. Read terminal gates to see which trigger can declare a winner or loser.
4. Follow incoming enabling, forcing and local-flag dependencies.
5. Inspect attached structures/units/cells to understand what the event applies to.
6. Follow any team link to its roster and ordered script.
7. Check the override table before using a global unit statistic.

The ledger preserves file order only for browsing. Triggers are a graph of possible transitions, not a mandatory sequence that every playthrough takes. Disabled, orphaned and alternative records are still documented; their existence alone is not proof of runtime reachability.
