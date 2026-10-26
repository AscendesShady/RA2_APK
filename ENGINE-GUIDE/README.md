# Red Alert 2 and Yuri's Revenge: a non-code engine guide

Read the game as a collection of decisions: what happens first, what is checked, what changes, and what happens next. This guide connects the original binaries, game rules, campaign maps, supplied manuals, and the local Android implementation.

It covers **157 distinct registered mobile types**, **408 distinct registered structure types**, **38 story missions**, both Boot Camp missions, and one additional legacy/alternate map. Detailed mission references translate **4,274 triggers**, **4,787 event records**, and **13,724 ordered actions**. Separate references explain **341 game-specific weapon/effect paths** and **266 global AI team templates**. See [Sources and limits](SOURCES.md) for exactly what these counts mean.

## Start here

1. [How the engine works](01-ENGINE-WORKFLOW.md) - startup, live objects, commands, movement, targeting, production, missions, saves and rendering.
2. [Every mobile piece](02-UNITS.md) - step-by-step unit behavior and separate RA2/Yuri properties, including hidden, civilian and managed attacker records.
3. [Combat and economy](03-COMBAT-ECONOMY.md) - weapons, armor, special effects, resources, money, power, repairs and superweapons.
4. [Every establishment and structure](04-BUILDINGS.md) - construction, factories, defenses, technology, income, repair, landmarks, scenery and mission-only additions.
5. [All campaigns, step by step](05-CAMPAIGNS.md) - the intended progression of each mission, with links to its complete logic ledger.
6. [Computer-army workflow](06-AI-WORKFLOW.md) - houses, task forces, recruitment, teams, scripts, staging, reinforcements and alliances.
7. [Android workflow](07-ANDROID-WORKFLOW.md) - native libraries, host services, touch/pen/mouse adaptation, save names and returning to the chooser.
8. [Reading while playing](08-STUDY-EXERCISES.md) - small observation exercises that connect the explanations to your own games.
9. [Building a base and reading prerequisites](09-BASE-BUILDING.md) - faction workflows, production dependencies and a plain-language glossary for the reference cards.

Read chapters 1, 3, 5 and 6 first for the overall engine. Treat the large unit, structure, weapon and mission pages as a reference library, rather than trying to memorize them in order. All links are relative so the folder remains readable after downloading it.

## Questions you can follow through the book

| Question | Reading path |
|---|---|
| Why does the same IFV behave differently? | [IFV](02-UNITS.md#fv), then its passenger's IFV mode and linked weapon |
| Why does my Chrono Miner drive outward but return differently? | [Chrono Miner](02-UNITS.md#cmin), then [economy](03-COMBAT-ECONOMY.md) |
| How does the Slave Miner become a building? | [Mobile miner](02-UNITS.md#smin), [deployed miner](04-BUILDINGS.md#yarefn) |
| Why does a Robot Tank stop when power fails? | [Robot Tank](02-UNITS.md#robo), [control center](04-BUILDINGS.md#garobo) |
| Why did the mission not end after I destroyed the main base? | Its [campaign workflow](05-CAMPAIGNS.md), then terminal gates and incoming trigger links |
| Why does a landmark matter even without a special weapon? | Its structure card, then attached tags in the mission ledger |
| Where did an enemy wave come from without a factory? | [Create Team versus Reinforcement](06-AI-WORKFLOW.md), then the mission's team plan |
| How does my finger become an original mouse command? | [Android input conversion](07-ANDROID-WORKFLOW.md) |

## How to read the evidence

- **Data-confirmed** means the value, definition or relationship is present in the extracted local data.
- **Binary-supported** means the explanation also has identified local binary/lifted-procedure evidence.
- **Manual-described** means the supplied manual describes that player-visible behavior.
- **Conceptual reconstruction** means a readable decision sequence, without claiming every original instruction has been recovered.
- **Unverified in play** means the prediction/branch was not demonstrated by a recorded playthrough.

The narrative workflows combine these sources, and their limits are stated where they matter. The detailed ledgers are static translations of declared logic. A declared trigger may be disabled, difficulty-specific, unused, or dependent on an event that never occurs on a particular route. A unit being registered is not proof it can be bought in a normal battle.

**No complete campaign playthrough was performed to write this book.** Existing emulator QA establishes particular startup, input and save/reload cases. Exact pathfinder internals, every hardcoded default, all target-score formulas and every mission branch remain outside the verified claims. The guide keeps those gaps visible instead of filling them with invented algorithms.

## Reference shelves

- [Weapon, projectile and warhead paths](reference/WEAPONS.md)
- [Global AI rosters and ordered plans](reference/AI-TEAMS.md)
- Every mission's trigger ledger, team-plan companion and override companion, linked from [Campaigns](05-CAMPAIGNS.md)
- [Sources, fingerprints, coverage and limitations](SOURCES.md)

The reading folder contains prose and factual reference tables. You do not need a compiler, reverse-engineering tool or programming knowledge to use it. Technical IDs in parentheses are stable cross-references that distinguish objects sharing the same display name.
