# Building a base and reading its dependencies

[Guide index](README.md) | [All structures](04-BUILDINGS.md) | [All units](02-UNITS.md)

<!-- ILLUSTRATIONS:START -->
![A working base contains services with distinct dependencies, not interchangeable buildings.](images/yuri-allied-start.png)

*A working base contains services with distinct dependencies, not interchangeable buildings. Historical local Android-emulator campaign-start capture; not a completed campaign.*
<!-- ILLUSTRATIONS:END -->

The workflows below explain the dependency pattern. They are not a mandatory competitive build order. Country restrictions, game mode, campaign overrides, captured technology, money and placement still determine what is actually legal.

## 1. Allied development

1. Begin with an Allied Construction Yard, or deploy the supplied Allied MCV on a clear legal foundation.
2. Add power so the base can support its consuming services.
3. Establish resource delivery through an Ore Refinery and Chrono Miner.
4. Add Barracks for eligible infantry and War Factory for eligible vehicle records.
5. Add Air Force Command infrastructure for the aircraft/radar/technology paths it supplies. The American variant has its own record.
6. Add the advanced prerequisites required by the desired unit or structure, such as Battle Lab or Robot Control Center.
7. Use a suitable shoreline for naval production, and preserve valid factory exits and aircraft docking space.
8. Add specialized defenses, information services, income modifiers and superweapons as the rules and battle require.

An Allied Battle Lab unlocks advanced choices; it does not itself eject tanks. The War Factory still performs production. A Robot Control Center supplies a control dependency that continues to matter after the Robot Tank has already been built.

## 2. Soviet development

1. Start from the Soviet Construction Yard or deploy its MCV.
2. Provide Tesla Reactor power and conventional resource processing.
3. Use War Miners to drive ore to the refinery.
4. Add Barracks and War Factory for the appropriate production queues.
5. Add Radar and advanced research prerequisites as needed.
6. Place the Naval Yard on a legal shore when naval production is useful.
7. Develop high-output power and advanced industry/special weapons where available.
8. Keep the support network alive while attacking; a large army does not replace income or factory access.

**Version distinction:** RA2's Soviet psychic technology is not simply retained unchanged in Yuri's Revenge. The expansion moves the Yuri-related roster/services and adds other Soviet options. Compare the two columns on the Psychic Sensor/Radar, Yuri infantry and Cloning Vats cards.

## 3. Yuri development

1. Start with Yuri's Construction Yard or deploy the Yuri MCV.
2. Use Bio Reactors for power; eligible occupants can increase their contribution.
3. Establish Slave Miner processing near a useful deposit.
4. Use its deployed form and managed slaves for the local collection cycle.
5. Add Yuri Barracks and War Factory for the eligible infantry and vehicle records.
6. Add Psychic Radar and Battle Lab prerequisites for the desired technology paths.
7. Use the Naval Yard for Boomers and the corresponding transport options.
8. Add specialized control, recycling, cloning and superweapon facilities according to the battle's needs and explicit restrictions.

The Grinder recycles owned units. Cloning Vats duplicate eligible newly produced infantry. The Bio Reactor uses occupants to support power. These are three different services; a captured soldier can be useful in different ways depending on where you send it.

## 4. Captured technology and neutral facilities

1. Identify whether the structure permits Engineer capture.
2. Reach it with a surviving compatible Engineer.
3. Transfer ownership through the supported entry operation.
4. Update the services or technology now available to the new owner.
5. Check remaining prerequisites, country restrictions, build limits and production facilities before expecting a new item in the sidebar.

An Oil Derrick provides income. An Airport grants a drop ability. A Machine Shop provides a vehicle-healing benefit. A Secret Lab grants its supported technology choice. None is a generic replacement for every missing prerequisite.

## 5. Turning a request into a finished building

1. Check whether the building is available to the current owner.
2. Check its prerequisites and limits.
3. Enter it into the correct construction category/queue.
4. Fund progress under the current power and production conditions.
5. When ready, find a legal footprint near permitted base-adjacency sources.
6. Reject blocked cells, unsuitable terrain or other placement violations.
7. Place/activate the structure and recalculate affected services.

Unit production ends differently: the factory needs a usable exit or delivery path. A ready tank is not a building-placement cursor. A naval unit needs an appropriate water exit. An aircraft may require a usable docking allocation.

## 6. Prerequisite groups in plain language

| Reference on a card | Meaning |
|---|---|
| POWER | A structure from the effective rules' power prerequisite group |
| FACTORY | A qualifying vehicle-production structure |
| BARRACKS | A qualifying infantry-production structure |
| RADAR | A structure in the effective radar prerequisite group |
| TECH | A qualifying advanced research structure |
| PROC | A qualifying resource-processing prerequisite, with supported alternatives such as the Slave Miner in Yuri |
| A named structure ID | That specific type is required by this record |
| Several comma-separated prerequisites | The record declares several requirements; group alternatives are resolved by their group definitions |

The global rules explicitly define the common groups. Capturing one faction's building does not automatically satisfy a different named structure requirement. A mission can add/replace the relevant properties, which is why its override companion matters.

## 7. Country-name aliases in the reference data

| Data name | Player-facing identity |
|---|---|
| Americans | America |
| Alliance | Korea |
| French | France |
| Germans | Germany |
| British | Great Britain |
| Russians | Russia |
| Confederation | Cuba |
| Africans | Libya |
| Arabs | Iraq |
| YuriCountry | Yuri's faction |
| Player, BadGuy and other map-created types | Scenario-specific owners/types; read that map's house list and trigger owner references |

A trigger's numeric owner selector is not automatically the same index as the list of placed house instances. The ledger reconstructs the country/type list from the baseline list followed by newly introduced map types and shows the matching placed owner where available. The inspected Yuri owner-resolver compares the requested type index with each house's country/type index. Special/unresolved selectors remain labeled instead of assigned to a guessed player.

## 8. Reading the object cards

| Card term | Meaning and limit |
|---|---|
| Price | Base cost setting; modifiers and mission rules can change the practical amount |
| Starting health capacity | Full-health setting before applicable modifiers; not a placed object's current health |
| Technology level | Availability threshold; -1 ordinarily disables normal construction for that type |
| Required structures/groups | Eligibility conditions, not an optimized build order |
| Permitted country list | One part of eligibility; it does not override every other restriction |
| Required/excluded countries | Additional owner restrictions |
| Build limit | A configured count restriction; unusual negative/special values require their own interpretation |
| Signed power | Positive output or negative requirement; no explicit field is reported as unspecified |
| Movement rating | Engine setting, not real-world velocity |
| Movement zone | Terrain/passability category used with the movement controller |
| Passenger capacity and size | Different checks: a transport may have slots but reject a unit too large to enter |
| IFV mode | A passenger's choice of the IFV configuration, not a general weapon number for every vehicle |
| Veteran/elite improvements | Explicit improvement lists; only applicable improvements should be assumed |
| Primary/secondary/elite weapon links | Paths into the weapon system; actual selection depends on target and object state |
| Spyable/capturable/unsellable | Independent interaction permissions |
| Missing field | The property was not explicitly recovered in that section; the engine may have a default or special case |

## 9. Read a base failure backwards

Suppose no new tank appears after you paid for it.

1. Check whether the queue is still progressing or completed.
2. Check current money and the power-dependent production conditions.
3. Check whether the correct factory still exists and belongs to you.
4. Check whether the factory's exit is blocked.
5. Check whether the unit requires a special production/arrival manager.
6. Check mission overrides and scripts that may remove, transfer or interrupt the result.

Suppose the tank exists but does nothing. Now inspect its order, target eligibility, movement restrictions, powered-unit service and any script/input issues. These are different branches of the engine workflow and need different explanations.
