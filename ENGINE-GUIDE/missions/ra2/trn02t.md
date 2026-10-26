# Boot Camp - Day 2

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for trn02t.map.](../../images/map-trn02t.svg)

*Initial placement schematic for trn02t.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** trn02t.map. **Effective extracted member:** MAPS01.MIX/trn02t.map. **Trigger definitions:** 45.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](trn02t-teams.md) | [All mission overrides](trn02t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | TEMPERATE |
| Map size | 0,0,40,41 |
| Visible local rectangle | 2,4,36,31 |
| Placed vehicles | 1 |
| Placed infantry | 10 |
| Placed structures | 18 |
| Placed aircraft | 0 |
| Team templates | 9 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 50 | Player |
| 1 | RedTeam House | 100 | RedTeam |
| 2 | Civilian House | 0 | Neutral |
| 3 | Other1 House | 20 | Other1 |
| 4 | Other2 House | 20 | Other2 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | 1stRedTeamWon,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [PlayerLose (09E02EA0)](#trigger-09e02ea0) | Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House). | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [PlayerWin (09E02BF0)](#trigger-09e02bf0) | Destroyed,  Buildings,  All: owner selector 14 (country/type REDTEAM; placed owner RedTeam House). | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-0907b430"></a>

### 1. 1Speech - 0907B430

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0907B1E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [1Text (09078F40)](#trigger-09078f40).
2. Play voice notification Mis_T2_DrillSearg01.
3. Enable and reset applicable timers for [1!MCVFlash (094C6984)](#trigger-094c6984).
4. Enable and reset applicable timers for [1EnableArrowMoveOut (07F8CD3C)](#trigger-07f8cd3c).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1790, Events line 1837, Actions line 1884.

<a id="trigger-09078f40"></a>

### 2. 1Text - 09078F40

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1Speech (0907B430)](#trigger-0907b430).

Attached scope: tag definitions 09078CB0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Move your Mobile Construction Vehicle to open ground” (MISSION:TRN02a).
2. Create radar-event marker type 1 at waypoint 14 (cell 42, 28).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1791, Events line 1838, Actions line 1885.

<a id="trigger-094c6984"></a>

### 3. 1!MCVFlash - 094C6984

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1Speech (0907B430)](#trigger-0907b430).

Attached scope: tag definitions 094C6234 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 13 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash team [Player_MCV (0BEB05FC)](trn02t-teams.md#team-0beb05fc) with duration setting 120.
2. Display message “Objective 1: Move your Mobile Construction Vehicle to open ground” (MISSION:TRN02a).
3. Create radar-event marker type 1 at waypoint 14 (cell 42, 28).
4. Reveal terrain around waypoint 14 (cell 42, 28).
5. Reveal terrain around waypoint 4 (cell 46, 27).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1792, Events line 1839, Actions line 1886.

<a id="trigger-07f8cd3c"></a>

### 4. 1EnableArrowMoveOut - 07F8CD3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1Speech (0907B430)](#trigger-0907b430).

Attached scope: tag definitions 07F8CB3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 22 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Arrow - MoveOut (07F8B04C)](#trigger-07f8b04c).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1793, Events line 1840, Actions line 1887.

<a id="trigger-07f8b04c"></a>

### 5. Arrow - MoveOut - 07F8B04C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1EnableArrowMoveOut (07F8CD3C)](#trigger-07f8cd3c).

Attached scope: tag definitions 07F8CF4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 477; location/duration field P.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1794, Events line 1841, Actions line 1888.

<a id="trigger-09078860"></a>

### 6. 1Complete(OpenGround) - 09078860

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 2 tagged map cells: (40, 26), (41, 26); tag 09078730, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Vertical Line: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [1Text (09078F40)](#trigger-09078f40).
2. Enable and reset applicable timers for [2Speech (0907AF40)](#trigger-0907af40).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1795, Events line 1842, Actions line 1889.

<a id="trigger-0907af40"></a>

### 7. 2Speech - 0907AF40

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1Complete(OpenGround) (09078860)](#trigger-09078860).

Attached scope: tag definitions 0907ADD0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Deploy your Mobile Construction Vehicle into a Construction Yard” (MISSION:TRN02b).
2. Enable and reset applicable timers for [2Text (0907ACF0)](#trigger-0907acf0).
3. Play voice notification Mis_T2_DrillSearg02.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1796, Events line 1843, Actions line 1890.

<a id="trigger-0907acf0"></a>

### 8. 2Text - 0907ACF0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [2Speech (0907AF40)](#trigger-0907af40).

Attached scope: tag definitions 0907AB20 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Deploy your Mobile Construction Vehicle into a Construction Yard” (MISSION:TRN02b).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1797, Events line 1844, Actions line 1891.

<a id="trigger-0907a900"></a>

### 9. 2Complete(ConYard) - 0907A900

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0907A7D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Destroy current instances of [2Text (0907ACF0)](#trigger-0907acf0).
2. Enable and reset applicable timers for [3Speech (07DCAB60)](#trigger-07dcab60).
3. Destroy current instances of [1Complete(OpenGround) (09078860)](#trigger-09078860).
4. Destroy current instances of [1Text (09078F40)](#trigger-09078f40).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1798, Events line 1845, Actions line 1892.

<a id="trigger-07dcab60"></a>

### 10. 3Speech - 07DCAB60

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [2Complete(ConYard) (0907A900)](#trigger-0907a900).

Attached scope: tag definitions 07DCAA90 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Build a Power Plant” (MISSION:TRN02c).
2. Enable and reset applicable timers for [3Text (07DCA9B0)](#trigger-07dca9b0).
3. Play voice notification Mis_T2_DrillSearg03.
4. Flash cameo/type 0; additional configured duration/location argument 150.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1799, Events line 1846, Actions line 1893.

<a id="trigger-07dca9b0"></a>

### 11. 3Text - 07DCA9B0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [3Speech (07DCAB60)](#trigger-07dcab60).

Attached scope: tag definitions 07DCA840 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Build a Power Plant” (MISSION:TRN02c).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1800, Events line 1847, Actions line 1894.

<a id="trigger-07dca4b0"></a>

### 12. 3Complete(Power) - 07DCA4B0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07DCA3E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 0 (global list position: Power Plant (GAPOWR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Disable [3Text (07DCA9B0)](#trigger-07dca9b0).
2. Enable and reset applicable timers for [4Speech (07DCDF40)](#trigger-07dcdf40).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1801, Events line 1848, Actions line 1895.

<a id="trigger-07dcdf40"></a>

### 13. 4Speech - 07DCDF40

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [3Complete(Power) (07DCA4B0)](#trigger-07dca4b0).

Attached scope: tag definitions 07DCDE70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 4: Build an Ore Refinery” (MISSION:TRN02d).
2. Enable and reset applicable timers for [4Text (07DCDC50)](#trigger-07dcdc50).
3. Play voice notification Mis_T2_DrillSearg04.
4. Flash cameo/type 1; additional configured duration/location argument 150.
5. Switch the sidebar to tab 0.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1802, Events line 1849, Actions line 1896.

<a id="trigger-07dcdc50"></a>

### 14. 4Text - 07DCDC50

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [4Speech (07DCDF40)](#trigger-07dcdf40).

Attached scope: tag definitions 07DCDB20 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 4: Build an Ore Refinery” (MISSION:TRN02d).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1803, Events line 1850, Actions line 1897.

<a id="trigger-03f6a0a0"></a>

### 15. 4Complete(Refinery) - 03F6A0A0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03F68190 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 1 (global list position: Allied Ore Refinery (GAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Disable [4Text (07DCDC50)](#trigger-07dcdc50).
2. Enable and reset applicable timers for [4Complete2(Miner Hint) (0B30B27C)](#trigger-0b30b27c).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1804, Events line 1851, Actions line 1898.

<a id="trigger-0b30b27c"></a>

### 16. 4Complete2(Miner Hint) - 0B30B27C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [4Complete(Refinery) (03F6A0A0)](#trigger-03f6a0a0).

Attached scope: tag definitions 0B30B19C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_T2_DrillSearg12.
2. Enable and reset applicable timers for [5Speech (08FA9940)](#trigger-08fa9940).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1805, Events line 1852, Actions line 1899.

<a id="trigger-08fa9940"></a>

### 17. 5Speech - 08FA9940

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [4Complete2(Miner Hint) (0B30B27C)](#trigger-0b30b27c).

Attached scope: tag definitions 08FA9810 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 11 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 5: Build a Barracks” (MISSION:TRN02f).
2. Enable and reset applicable timers for [5Text (08FAED70)](#trigger-08faed70).
3. Play voice notification Mis_T2_DrillSearg05.
4. Flash cameo/type 3; additional configured duration/location argument 150.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1806, Events line 1853, Actions line 1900.

<a id="trigger-08faed70"></a>

### 18. 5Text - 08FAED70

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [5Speech (08FA9940)](#trigger-08fa9940).

Attached scope: tag definitions 08FAEAE0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 5: Build a Barracks” (MISSION:TRN02f).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1807, Events line 1854, Actions line 1901.

<a id="trigger-08faea00"></a>

### 19. 6Text - 08FAEA00

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [6Speech (08FA95F0)](#trigger-08fa95f0).

Attached scope: tag definitions 08FAE830 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 6: Build a squad of GIs” (MISSION:TRN02g).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1808, Events line 1855, Actions line 1902.

<a id="trigger-08fae4a0"></a>

### 20. 7Text - 08FAE4A0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [DestroyRedBase (09E06A00)](#trigger-09e06a00).

Attached scope: tag definitions 08FA9EB0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 7: Destroy Red Team's base” (MISSION:TRN02i).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1809, Events line 1856, Actions line 1903.

<a id="trigger-08fa95f0"></a>

### 21. 6Speech - 08FA95F0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [5Complete(Barracks) (08FADE60)](#trigger-08fade60).

Attached scope: tag definitions 08FA83D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 6: Build a squad of GIs” (MISSION:TRN02g).
2. Enable and reset applicable timers for [6Text (08FAEA00)](#trigger-08faea00).
3. Play voice notification Mis_T2_DrillSearg06.
4. Switch the sidebar to tab 2.
5. Flash cameo/type 364; additional configured duration/location argument 150.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1810, Events line 1857, Actions line 1904.

<a id="trigger-08fade60"></a>

### 22. 5Complete(Barracks) - 08FADE60

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08FA9D40 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 3 (global list position: Allied Barracks (GAPILE)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Destroy current instances of [5Speech (08FA9940)](#trigger-08fa9940).
2. Enable and reset applicable timers for [6Speech (08FA95F0)](#trigger-08fa95f0).
3. Disable [5Text (08FAED70)](#trigger-08faed70).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1811, Events line 1858, Actions line 1905.

<a id="trigger-07d47630"></a>

### 23. 6Complete(GIBuilt) - 07D47630

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07D47440 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Infantry Type: type index 0 (global list position: GI (E1)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Disable [6Text (08FAEA00)](#trigger-08faea00).
2. Enable and reset applicable timers for [RedTeamA-Create (098925C0)](#trigger-098925c0).
3. Enable and reset applicable timers for [RedTeamA-Won (0909F130)](#trigger-0909f130).
4. Display message “Deploy your GIs near the entrance to your base for a better defense” (MISSION:TRN02_Hint1).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1812, Events line 1859, Actions line 1906.

<a id="trigger-098925c0"></a>

### 24. RedTeamA-Create - 098925C0

Owner reference: RedTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [6Complete(GIBuilt) (07D47630)](#trigger-07d47630).

Attached scope: tag definitions 098924F0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 75 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [RedAttackTeamA (09AB3C8C)](trn02t-teams.md#team-09ab3c8c).
2. Display message “WARNING: Red Team invasion imminent” (MISSION:TRN02h).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
4. Production Begins: owner selector 14 (country/type REDTEAM; placed owner RedTeam House).
5. Play voice notification Mis_T2_DrillSearg07.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1813, Events line 1860, Actions line 1907.

<a id="trigger-0909f130"></a>

### 25. RedTeamA-Won - 0909F130

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [6Complete(GIBuilt) (07D47630)](#trigger-07d47630).

Attached scope: tag definitions 090B34D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (1stRedTeamWon) is set.

**Then perform these actions in order:**

1. Create/recruit team [RedTeamRegroup (07FB10F4)](trn02t-teams.md#team-07fb10f4).
2. Enable and reset applicable timers for [RedTeamB-Create (098A0B80)](#trigger-098a0b80).
3. Play voice notification Mis_T2_DrillSearg10.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1814, Events line 1861, Actions line 1908.

<a id="trigger-098a0b80"></a>

### 26. RedTeamB-Create - 098A0B80

Owner reference: RedTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [RedTeamA-Won (0909F130)](#trigger-0909f130).

Attached scope: tag definitions 098A0700 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [RedAttackTeamB (0973C33C)](trn02t-teams.md#team-0973c33c).
2. Display message “WARNING: The stench of Red Team is in the air” (MISSION:TRN02hAlt).
3. Play voice notification Mis_T2_DrillSearg19.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1815, Events line 1862, Actions line 1909.

<a id="trigger-091050b0"></a>

### 27. RedTeamA-Destroyed - 091050B0

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09104210 (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [DestroyRedBase (09E06A00)](#trigger-09e06a00).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1816, Events line 1863, Actions line 1910.

<a id="trigger-09e06a00"></a>

### 28. DestroyRedBase - 09E06A00

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [RedTeamA-Destroyed (091050B0)](#trigger-091050b0); enable from [RedTeamB-Destroyed (09E06560)](#trigger-09e06560).

Attached scope: tag definitions 09E06930 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 7: Destroy Red Team's base” (MISSION:TRN02i).
2. Play voice notification Mis_T2_DrillSearg09.
3. Enable and reset applicable timers for [Ping Map (096D1994)](#trigger-096d1994).
4. Enable and reset applicable timers for [7Text (08FAE4A0)](#trigger-08fae4a0).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1817, Events line 1864, Actions line 1911.

<a id="trigger-096d1994"></a>

### 29. Ping Map - 096D1994

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [DestroyRedBase (09E06A00)](#trigger-09e06a00).

Attached scope: tag definitions 096D2734 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 17 (cell 44, 56).
2. Enable and reset applicable timers for [Arrow - GoToRedBase (0B09C8CC)](#trigger-0b09c8cc).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1818, Events line 1865, Actions line 1912.

<a id="trigger-0b09c8cc"></a>

### 30. Arrow - GoToRedBase - 0B09C8CC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Ping Map (096D1994)](#trigger-096d1994).

Attached scope: tag definitions 0B09C6CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 473; location/duration field Q.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1819, Events line 1866, Actions line 1913.

<a id="trigger-098a71f0"></a>

### 31. EnteredPotty - 098A71F0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [EvictPottyBoy (094D2984)](#trigger-094d2984).
2. Play voice notification Mis_T2_DrillSearg17.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1820, Events line 1867, Actions line 1914.

<a id="trigger-094d2984"></a>

### 32. EvictPottyBoy - 094D2984

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [EnteredPotty (098A71F0)](#trigger-098a71f0).

Incoming activation links: enable from [EnteredPotty (098A71F0)](#trigger-098a71f0).

Attached scope: Outhouse (CAFRMB), owner Civilian House, cell (44, 14), tag 098A2460, persistence mode 2.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Evict occupants from the attached building.
2. Disable [EvictPottyBoy (094D2984)](#trigger-094d2984).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1821, Events line 1868, Actions line 1915.

<a id="trigger-07ef1c00"></a>

### 33. DiscoverBarn - 07EF1C00

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Farm Silo (CAFARM02), owner Civilian House, cell (61, 34), tag 07EFE840, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.
2. Build Infantry Type: type index 0 (global list position: GI (E1)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 2 (cell 58, 34).
2. Play voice notification Mis_T2_DrillSearg21.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1822, Events line 1869, Actions line 1916.

<a id="trigger-09e06560"></a>

### 34. RedTeamB-Destroyed - 09E06560

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09E06490 (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [DestroyRedBase (09E06A00)](#trigger-09e06a00).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1823, Events line 1870, Actions line 1917.

<a id="trigger-09e02ea0"></a>

### 35. PlayerLose - 09E02EA0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CreateMCVTeam (0975F6C4)](#trigger-0975f6c4).

Attached scope: tag definitions 09E02CD0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1824, Events line 1871, Actions line 1918.

<a id="trigger-09e02bf0"></a>

### 36. PlayerWin - 09E02BF0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09E02A20 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 14 (country/type REDTEAM; placed owner RedTeam House).

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.
2. Play voice notification Mis_T2_DrillSearg11.
3. Disable [7Text (08FAE4A0)](#trigger-08fae4a0).
4. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1825, Events line 1872, Actions line 1919.

<a id="trigger-0975f6c4"></a>

### 37. CreateMCVTeam - 0975F6C4

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0975D424 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Player_MCV (0BEB05FC)](trn02t-teams.md#team-0beb05fc).
2. Enable and reset applicable timers for [PlayerLose (09E02EA0)](#trigger-09e02ea0).
3. Reveal terrain around waypoint 98 (cell 21, 38).
4. Reveal terrain around waypoint 3 (cell 17, 39).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1826, Events line 1873, Actions line 1920.

<a id="trigger-07ba8b6c"></a>

### 38. RedAttackBarn - 07BA8B6C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Farm (CAFARM01), owner Civilian House, cell (59, 35), tag 07BA8A8C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [BarnHaters (088CE6EC)](trn02t-teams.md#team-088ce6ec).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1827, Events line 1874, Actions line 1921.

<a id="trigger-07ba892c"></a>

### 39. BarnHatersDestroyed - 07BA892C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07BA884C (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play voice notification Mis_T2_DrillSearg23.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1828, Events line 1875, Actions line 1922.

<a id="trigger-07d66e1c"></a>

### 40. HintCrate - 07D66E1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 13 tagged map cells: (44, 36), (45, 36), (46, 36), (42, 37), (44, 37), (45, 37), (46, 37), (48, 37), (43, 38), (44, 38), (45, 38), (46, 38), (47, 38); tag 07D66D3C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Play voice notification Mis_T2_DrillSearg20.

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1829, Events line 1876, Actions line 1923.

<a id="trigger-09f9c49c"></a>

### 41. AmbientSounds/Crate - 09F9C49C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09F9C34C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_River at waypoint 5 (cell 19, 49).
2. Play sound _Amb_River at waypoint 6 (cell 32, 49).
3. Play sound _Amb_River at waypoint 7 (cell 38, 42).
4. Play sound _Amb_River at waypoint 8 (cell 52, 44).
5. Play sound _Amb_BirdsTemperate2 at waypoint 10 (cell 32, 38).
6. Play sound _Amb_BirdsPark at waypoint 9 (cell 27, 59).
7. Play sound _Amb_BirdsPark at waypoint 11 (cell 39, 23).
8. Play sound _Amb_BirdsTemperate1 at waypoint 12 (cell 66, 33).
9. Play sound _Amb_UrbanMurmur2 at waypoint 90 (cell 5, 38).
10. Create crate type 0 at waypoint 80 (cell 45, 39).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1830, Events line 1877, Actions line 1924.

<a id="trigger-0868b9ac"></a>

### 42. RedTeamRepairBridge - 0868B9AC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0868B46C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [EngineerBridge (0868EEFC)](trn02t-teams.md#team-0868eefc) at waypoint 17 (cell 44, 56).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1831, Events line 1878, Actions line 1925.

<a id="trigger-0bbdb55c"></a>

### 43. Disable MoveOutArrow - 0BBDB55C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 2 tagged map cells: (29, 30), (30, 30); tag 0BBDB1BC, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Vertical Line: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [Arrow - MoveOut (07F8B04C)](#trigger-07f8b04c).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1832, Events line 1879, Actions line 1926.

<a id="trigger-0b09c52c"></a>

### 44. Disable RedBaseArrow - 0B09C52C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 16 tagged map cells: (51, 44), (52, 44), (53, 44), (54, 44), (55, 44), (56, 44), (57, 44), (58, 44), (51, 45), (52, 45), (53, 45), (54, 45), (55, 45), (56, 45), (57, 45), (58, 45); tag 0B09C32C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [Arrow - GoToRedBase (0B09C8CC)](#trigger-0b09c8cc).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1833, Events line 1880, Actions line 1927.

<a id="trigger-0d9e7f3c"></a>

### 45. RevealRedBase - 0D9E7F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Construction Yard (GACNST), owner RedTeam House, cell (38, 55), tag 0D9E4BAC, persistence mode 0; Allied Ore Refinery (GAREFN), owner RedTeam House, cell (38, 64), tag 0D9E4BAC, persistence mode 0; Allied Barracks (GAPILE), owner RedTeam House, cell (47, 57), tag 0D9E4BAC, persistence mode 0; Power Plant (GAPOWR), owner RedTeam House, cell (50, 55), tag 0D9E4BAC, persistence mode 0; Power Plant (GAPOWR), owner RedTeam House, cell (32, 64), tag 0D9E4BAC, persistence mode 0; Power Plant (GAPOWR), owner RedTeam House, cell (35, 64), tag 0D9E4BAC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 19 (cell 46, 56).
2. Reveal terrain around waypoint 54 (cell 42, 58).
3. Reveal terrain around waypoint 20 (cell 42, 62).
4. Reveal terrain around waypoint 21 (cell 37, 64).

Source locator: MAPS01.MIX/trn02t.map; Triggers line 1834, Events line 1881, Actions line 1928.

[All team rosters and ordered plans](trn02t-teams.md) | [All mission overrides](trn02t-overrides.md)
