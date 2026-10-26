# Boot Camp - Day 1

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for trn01t.map.](../../images/map-trn01t.svg)

*Initial placement schematic for trn01t.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** trn01t.map. **Effective extracted member:** MAPS01.MIX/trn01t.map. **Trigger definitions:** 72.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](trn01t-teams.md) | [All mission overrides](trn01t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | TEMPERATE |
| Map size | 0,0,56,69 |
| Visible local rectangle | 3,19,50,44 |
| Placed vehicles | 2 |
| Placed infantry | 6 |
| Placed structures | 34 |
| Placed aircraft | 0 |
| Team templates | 12 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 0 | Player |
| 1 | BadGuy1 House | 100 | BadGuy1 |
| 2 | BadGuy2 House | 0 | BadGuy2 |
| 3 | BadGuy3 House | 0 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 20 | Other1 |
| 6 | Other2 House | 0 | Other2 |
| 7 | Other3 House | 0 | Other3 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Engineer Landed,0 |
| 1 | Helicopter Leaves,0 |
| 2 | Annoyed,0 |
| 3 | Annoyed_Again,0 |
| 4 | Near Target,0 |
| 5 | Far Target,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Mission Complete (07B729DC)](#trigger-07b729dc) | 45 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [Friendly Fire (07CAA20C)](#trigger-07caa20c) | Destroyed by any house. See attached-object/cell scope below. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [Friendly Destroyed (07C4FB34)](#trigger-07c4fb34) | Destroyed by anything. See attached-object/cell scope below. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-07ad555c"></a>

### 1. Smoke From Tank - 07AD555C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tank Sighted (07B499AC)](#trigger-07b499ac).

Attached scope: tag definitions 07AC2BFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Particle Anim at; main setting 2.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2153, Events line 2227, Actions line 2301.

<a id="trigger-07cffd8c"></a>

### 2. Tank Dead No Smoke - 07CFFD8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Derelict Tank (CAMSC13), owner BadGuy1 House, cell (55, 26), tag 07CFF60C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove Particle Anim at; main setting 0.
2. Enable and reset applicable timers for [Drill Sarge 9 (07B72F3C)](#trigger-07b72f3c).
3. Disable [Objective 6b Reminder (07AE7BAC)](#trigger-07ae7bac).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2154, Events line 2228, Actions line 2302.

<a id="trigger-07b72f3c"></a>

### 3. Drill Sarge 9 - 07B72F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tank Dead No Smoke (07CFFD8C)](#trigger-07cffd8c).

Attached scope: tag definitions 07B72ACC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 6 Complete” (MISSION:TRN01j).
2. Enable and reset applicable timers for [Mission Complete (07B729DC)](#trigger-07b729dc).
3. Display message “Day One Training Complete” (MISSION:TRN01k).
4. Play voice notification Mis_T1_DrillSearg09.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2155, Events line 2229, Actions line 2303.

<a id="trigger-07ae7bac"></a>

### 4. Objective 6b Reminder - 07AE7BAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tank Sighted (07B499AC)](#trigger-07b499ac).

Attached scope: tag definitions 07AE78FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 6: Destroy the derelict tank” (MISSION:TRN01i).
2. Create radar-event marker type 1 at waypoint 0 (cell 55, 26).
3. Play Anim At; main setting 479; location/duration field I.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2156, Events line 2230, Actions line 2304.

<a id="trigger-07b729dc"></a>

### 5. Mission Complete - 07B729DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 9 (07B72F3C)](#trigger-07b72f3c).

Attached scope: tag definitions 07B7272C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2157, Events line 2231, Actions line 2305.

<a id="trigger-0922e85c"></a>

### 6. Objective 6a Reminder - 0922E85C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 7 (07B7941C)](#trigger-07b7941c).

Attached scope: tag definitions 0922E77C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 6: Continue up the path and destroy the derelict tank” (MISSION:TRN01h).
2. Create radar-event marker type 0 at waypoint 0 (cell 55, 26).
3. Play Anim At; main setting 476; location/duration field L.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2158, Events line 2232, Actions line 2306.

<a id="trigger-07517cfc"></a>

### 7. Extend Local Map Size - 07517CFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Both Targets Destroyed (08DE3C4C)](#trigger-08de3c4c).

Attached scope: tag definitions 0751773C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Resize Player View; main setting 0; parameter 1: 3, parameter 2: 4, parameter 3: 50, parameter 4: 59.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2159, Events line 2233, Actions line 2307.

<a id="trigger-0751023c"></a>

### 8. Broken Bridge Sighted - 0751023C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 37 tagged map cells: (69, 64), (70, 64), (69, 65), (70, 65), (70, 66), (71, 66), (83, 66), (84, 66), (85, 66), (86, 66), (71, 67), (72, 67), (82, 67), (83, 67), (84, 67), (85, 67), (86, 67), (72, 68), (73, 68), (74, 68), (75, 68), (76, 68), (77, 68), (78, 68), (79, 68), (80, 68), (81, 68), (82, 68), (73, 69), (74, 69), (75, 69), (76, 69), (77, 69), (78, 69), (79, 69), (80, 69), (81, 69); tag 075100AC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector -1 (unresolved or special selector).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 2 (cell 77, 66).
2. Reveal terrain around waypoint 3 (cell 77, 58).
3. Reveal terrain around waypoint 4 (cell 77, 49).
4. Play sound HealCrate.
5. Enable and reset applicable timers for [Engineer en-route (08FD02AC)](#trigger-08fd02ac).
6. Enable and reset applicable timers for [Drill Sarge 4 (07B79E4C)](#trigger-07b79e4c).
7. Enable and reset applicable timers for [Text_Objective 3 (07BADA9C)](#trigger-07bada9c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2160, Events line 2234, Actions line 2308.

<a id="trigger-08fd02ac"></a>

### 9. Engineer en-route - 08FD02AC

Owner reference: Other1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Broken Bridge Sighted (0751023C)](#trigger-0751023c).

Attached scope: tag definitions 08FD2E9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Engineer by Blackhawk (0D521B7C)](trn01t-teams.md#team-0d521b7c) at waypoint 5 (cell 112, 74).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2161, Events line 2235, Actions line 2309.

<a id="trigger-07b79e4c"></a>

### 10. Drill Sarge 4 - 07B79E4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Broken Bridge Sighted (0751023C)](#trigger-0751023c).

Attached scope: tag definitions 07B79A0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2 Complete” (MISSION:Objective2).
2. Disable [Objective 2 Reminder (0922D40C)](#trigger-0922d40c).
3. Enable and reset applicable timers for [Objective 3 Reminder (0922D15C)](#trigger-0922d15c).
4. Play voice notification Mis_T1_DrillSearg04.
5. Disable [Drill Sarge 3 Text (09CA94AC)](#trigger-09ca94ac).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2162, Events line 2236, Actions line 2310.

<a id="trigger-07bada9c"></a>

### 11. Text_Objective 3 - 07BADA9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Broken Bridge Sighted (0751023C)](#trigger-0751023c).

Attached scope: tag definitions 07BAD5BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Select the ENGINEER and move him into the REPAIR HUT” (MISSION:TRN01c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2163, Events line 2237, Actions line 2311.

<a id="trigger-0922d40c"></a>

### 12. Objective 2 Reminder - 0922D40C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 3 (043B011C)](#trigger-043b011c).

Attached scope: tag definitions 0922D24C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Select all GIs and head right to the bridge” (MISSION:TRN01b).
2. Create radar-event marker type 1 at waypoint 3 (cell 77, 58).
3. Play Anim At; main setting 472; location/duration field AU.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2164, Events line 2238, Actions line 2312.

<a id="trigger-0922d15c"></a>

### 13. Objective 3 Reminder - 0922D15C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 4 (07B79E4C)](#trigger-07b79e4c).

Attached scope: tag definitions 0922EDCC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Select the ENGINEER and move him into the REPAIR HUT” (MISSION:TRN01c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2165, Events line 2239, Actions line 2313.

<a id="trigger-09ca94ac"></a>

### 14. Drill Sarge 3 Text - 09CA94AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 3 (043B011C)](#trigger-043b011c).

Attached scope: tag definitions 09CA93CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 38 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Select all GIs and head right to the bridge” (MISSION:TRN01b).
2. Create radar-event marker type 1 at waypoint 3 (cell 77, 58).
3. Enable and reset applicable timers for [Point to Bridge (0B45896C)](#trigger-0b45896c).
4. Enable and reset applicable timers for [Point to Bridge Stop (0B4585CC)](#trigger-0b4585cc).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2166, Events line 2240, Actions line 2314.

<a id="trigger-0b45896c"></a>

### 15. Point to Bridge - 0B45896C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 3 Text (09CA94AC)](#trigger-09ca94ac).

Attached scope: tag definitions 0B45876C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 472; location/duration field AU.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2167, Events line 2241, Actions line 2315.

<a id="trigger-0b4585cc"></a>

### 16. Point to Bridge Stop - 0B4585CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 3 Text (09CA94AC)](#trigger-09ca94ac).

Attached scope: tag definitions 084D617C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Point to Bridge (0B45896C)](#trigger-0b45896c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2168, Events line 2242, Actions line 2316.

<a id="trigger-075109ec"></a>

### 17. 075109EC - 075109EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

No event entries. Reachability requires separate runtime interpretation.

**Then perform these actions in order:**

No action entries.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2169, Events line 2243, Actions line 2317.

<a id="trigger-0751768c"></a>

### 18. Drill Sarge 1 - 0751768C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0751748C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create 1GI Team (07516AFC)](#trigger-07516afc).
2. Particle Anim at; main setting 2.
3. Enable and reset applicable timers for [Objective 1 Reminder (0922D5DC)](#trigger-0922d5dc).
4. Play voice notification Mis_T1_DrillSearg01.
5. Enable and reset applicable timers for [Reveal Base Gate (09C9503C)](#trigger-09c9503c).
6. Enable and reset applicable timers for [Drill Sarge 2 (08FABE0C)](#trigger-08fabe0c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2170, Events line 2244, Actions line 2318.

<a id="trigger-07516afc"></a>

### 19. Create 1GI Team - 07516AFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 1 (0751768C)](#trigger-0751768c).

Attached scope: tag definitions 07516A1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 28 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [1 GI (0D7FE2AC)](trn01t-teams.md#team-0d7fe2ac).
2. Enable and reset applicable timers for [Arrow Out of Base (086E1C1C)](#trigger-086e1c1c).
3. Destroy current instances of [Quick Create 1 GI Team (0A71229C)](#trigger-0a71229c).
4. Enable and reset applicable timers for [Point at GI (0847214C)](#trigger-0847214c).
5. Enable and reset applicable timers for [Point at GI Stop (0848304C)](#trigger-0848304c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2171, Events line 2245, Actions line 2319.

<a id="trigger-0922d5dc"></a>

### 20. Objective 1 Reminder - 0922D5DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 1 (0751768C)](#trigger-0751768c).

Attached scope: tag definitions 0922D4FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 220 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Move GI down out of the base” (MISSION:TRN01a).
2. Create radar-event marker type 1 at waypoint 6 (cell 71, 95).
3. Play Anim At; main setting 474; location/duration field W.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2172, Events line 2246, Actions line 2320.

<a id="trigger-09c9503c"></a>

### 21. Reveal Base Gate - 09C9503C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 1 (0751768C)](#trigger-0751768c).

Attached scope: tag definitions 09C9704C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 22 (cell 60, 91).
2. Display message “Objective 1: Move GI down out of the base” (MISSION:TRN01a).
3. Create radar-event marker type 1 at waypoint 6 (cell 71, 95).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2173, Events line 2247, Actions line 2321.

<a id="trigger-08fabe0c"></a>

### 22. Drill Sarge 2 - 08FABE0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 1 (0751768C)](#trigger-0751768c).

Attached scope: tag definitions 08FAB6DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 85 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 6 (cell 71, 95).
2. Play voice notification Mis_T1_DrillSearg02.
3. Display message “Objective 1: Move GI down out of the base” (MISSION:TRN01a).
4. Play Anim At; main setting 474; location/duration field W.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2174, Events line 2248, Actions line 2322.

<a id="trigger-086e1c1c"></a>

### 23. Arrow Out of Base - 086E1C1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create 1GI Team (07516AFC)](#trigger-07516afc); enable from [Quick Create 1 GI Team (0A71229C)](#trigger-0a71229c).

Attached scope: tag definitions 086E1A1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Point Out of Base (0B45D33C)](#trigger-0b45d33c).
2. Enable and reset applicable timers for [Point Out of Base Stop (0847B03C)](#trigger-0847b03c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2175, Events line 2249, Actions line 2323.

<a id="trigger-0a71229c"></a>

### 24. Quick Create 1 GI Team - 0A71229C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: GI (E1), owner Player House, cell (57, 89), tag 0A71735C, persistence mode 0.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [1 GI (0D7FE2AC)](trn01t-teams.md#team-0d7fe2ac).
2. Enable and reset applicable timers for [Arrow Out of Base (086E1C1C)](#trigger-086e1c1c).
3. Destroy current instances of [Create 1GI Team (07516AFC)](#trigger-07516afc).
4. Enable and reset applicable timers for [Point at GI (0847214C)](#trigger-0847214c).
5. Enable and reset applicable timers for [Point at GI Stop (0848304C)](#trigger-0848304c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2176, Events line 2250, Actions line 2324.

<a id="trigger-0847214c"></a>

### 25. Point at GI - 0847214C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create 1GI Team (07516AFC)](#trigger-07516afc); enable from [Quick Create 1 GI Team (0A71229C)](#trigger-0a71229c).

Attached scope: tag definitions 0847F04C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 479; location/duration field AV.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2177, Events line 2251, Actions line 2325.

<a id="trigger-0848304c"></a>

### 26. Point at GI Stop - 0848304C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create 1GI Team (07516AFC)](#trigger-07516afc); enable from [Quick Create 1 GI Team (0A71229C)](#trigger-0a71229c).

Attached scope: tag definitions 084D625C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Point at GI (0847214C)](#trigger-0847214c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2178, Events line 2252, Actions line 2326.

<a id="trigger-0b45d33c"></a>

### 27. Point Out of Base - 0B45D33C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Arrow Out of Base (086E1C1C)](#trigger-086e1c1c).

Attached scope: tag definitions 0B458D2C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 474; location/duration field W.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2179, Events line 2253, Actions line 2327.

<a id="trigger-0847b03c"></a>

### 28. Point Out of Base Stop - 0847B03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Arrow Out of Base (086E1C1C)](#trigger-086e1c1c).

Attached scope: tag definitions 084D633C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Point Out of Base (0B45D33C)](#trigger-0b45d33c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2180, Events line 2254, Actions line 2328.

<a id="trigger-043b011c"></a>

### 29. Drill Sarge 3 - 043B011C

Owner reference: Other2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Army Tents (CAARMY04), owner Civie1 House, cell (71, 92), tag 043BD15C, persistence mode 0; Army Tents (CAARMY01), owner Civie1 House, cell (69, 96), tag 043BD15C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “Objective 1 Complete” (MISSION:Objective1).
2. Create/recruit team [4 GIs (0B197B7C)](trn01t-teams.md#team-0b197b7c).
3. Reveal terrain around waypoint 6 (cell 71, 95).
4. Play sound HealCrate.
5. Make ally: owner selector 13 (country/type PLAYER; placed owner Player House).
6. Disable [Objective 1 Reminder (0922D5DC)](#trigger-0922d5dc).
7. Enable and reset applicable timers for [Objective 2 Reminder (0922D40C)](#trigger-0922d40c).
8. Play voice notification Mis_T1_DrillSearg03.
9. Disable [Drill Sarge 2 (08FABE0C)](#trigger-08fabe0c).
10. Enable and reset applicable timers for [Drill Sarge 3 Text (09CA94AC)](#trigger-09ca94ac).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2181, Events line 2255, Actions line 2329.

<a id="trigger-08de3c4c"></a>

### 30. Both Targets Destroyed - 08DE3C4C

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DE336C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (Far Target) is set.
2. local flag 4 (Near Target) is set.

Flag writers in this mission: set local flag 5 (Far Target) at [Far Target Destroyed (0893EE4C)](#trigger-0893ee4c); set local flag 4 (Near Target) at [Near Target Destroyed (07B7879C)](#trigger-07b7879c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Extend Local Map Size (07517CFC)](#trigger-07517cfc).
2. Play sound HealCrate.
3. Enable and reset applicable timers for [Drill Sarge 7 (07B7941C)](#trigger-07b7941c).
4. Reveal terrain around waypoint 9 (cell 67, 34).
5. Reveal terrain around waypoint 10 (cell 68, 35).
6. Reveal terrain around waypoint 11 (cell 65, 32).
7. Play Anim At; main setting 476; location/duration field L.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2182, Events line 2256, Actions line 2330.

<a id="trigger-07b7941c"></a>

### 31. Drill Sarge 7 - 07B7941C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Both Targets Destroyed (08DE3C4C)](#trigger-08de3c4c).

Attached scope: tag definitions 07B7921C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 4 Complete” (MISSION:TRN01e).
2. Disable [Objective 4 Reminder (0922EBFC)](#trigger-0922ebfc).
3. Disable [Objective 5 Reminder (0922EA2C)](#trigger-0922ea2c).
4. Enable and reset applicable timers for [Objective 6a Reminder (0922E85C)](#trigger-0922e85c).
5. Play voice notification Mis_T1_DrillSearg07.
6. Enable and reset applicable timers for [Drill Sarge 7 Text (090C6E1C)](#trigger-090c6e1c).
7. Disable [Drill Sarge 6 Text (0AB5C41C)](#trigger-0ab5c41c).
8. Supply reinforcement team [Veteran GI (0B070B5C)](trn01t-teams.md#team-0b070b5c) at waypoint 50 (cell 76, 42).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2183, Events line 2257, Actions line 2331.

<a id="trigger-0922ebfc"></a>

### 32. Objective 4 Reminder - 0922EBFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 5 (08FA96EC)](#trigger-08fa96ec).

Attached scope: tag definitions 0922EB1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 4: Move into the firing range and destroy the nearest target” (MISSION:TRN01d).
2. Create radar-event marker type 1 at waypoint 16 (cell 71, 40).
3. Play Anim At; main setting 476; location/duration field E.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2184, Events line 2258, Actions line 2332.

<a id="trigger-0922ea2c"></a>

### 33. Objective 5 Reminder - 0922EA2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 6 (07B7986C)](#trigger-07b7986c).

Attached scope: tag definitions 0922E94C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 5: Deploy(double-click) your men and destroy the far target” (MISSION:TRN01f).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2185, Events line 2259, Actions line 2333.

<a id="trigger-090c6e1c"></a>

### 34. Drill Sarge 7 Text - 090C6E1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 7 (07B7941C)](#trigger-07b7941c).

Attached scope: tag definitions 090C6A1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 40 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 6: Continue up the path and destroy the derelict tank” (MISSION:TRN01h).
2. Create radar-event marker type 1 at waypoint 0 (cell 55, 26).
3. Enable and reset applicable timers for [Point to Tank (0B3F91BC)](#trigger-0b3f91bc).
4. Enable and reset applicable timers for [Point to Tank Stop (0B3FCF3C)](#trigger-0b3fcf3c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2186, Events line 2260, Actions line 2334.

<a id="trigger-0ab5c41c"></a>

### 35. Drill Sarge 6 Text - 0AB5C41C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 6 (07B7986C)](#trigger-07b7986c).

Attached scope: tag definitions 0AB5894C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 5: Deploy(double-click) your men and destroy the far target” (MISSION:TRN01f).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2187, Events line 2261, Actions line 2335.

<a id="trigger-0b3f91bc"></a>

### 36. Point to Tank - 0B3F91BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 7 Text (090C6E1C)](#trigger-090c6e1c).

Attached scope: tag definitions 0B3FB17C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 476; location/duration field J.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2188, Events line 2262, Actions line 2336.

<a id="trigger-0b3fcf3c"></a>

### 37. Point to Tank Stop - 0B3FCF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 7 Text (090C6E1C)](#trigger-090c6e1c).

Attached scope: tag definitions 084D609C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Point to Tank (0B3F91BC)](#trigger-0b3f91bc).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2189, Events line 2263, Actions line 2337.

<a id="trigger-07b7879c"></a>

### 38. Near Target Destroyed - 07B7879C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Practice Target (CAMSC12), owner BadGuy1 House, cell (65, 44), tag 07B784AC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 4 (Near Target).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2190, Events line 2264, Actions line 2338.

<a id="trigger-07b7986c"></a>

### 39. Drill Sarge 6 - 07B7986C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B7966C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 4 Complete” (MISSION:TRN01e).
2. Disable [Objective 4 Reminder (0922EBFC)](#trigger-0922ebfc).
3. Enable and reset applicable timers for [Objective 5 Reminder (0922EA2C)](#trigger-0922ea2c).
4. Play voice notification Mis_T1_DrillSearg06.
5. Enable and reset applicable timers for [Drill Sarge 6 Text (0AB5C41C)](#trigger-0ab5c41c).
6. Disable [Drill Sarge 5 Text (0956E23C)](#trigger-0956e23c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2191, Events line 2265, Actions line 2339.

<a id="trigger-0956e23c"></a>

### 40. Drill Sarge 5 Text - 0956E23C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drill Sarge 5 (08FA96EC)](#trigger-08fa96ec).

Attached scope: tag definitions 0956E15C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 4: Move into the firing range and destroy the nearest target” (MISSION:TRN01d).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2192, Events line 2266, Actions line 2340.

<a id="trigger-07caa20c"></a>

### 41. Friendly Fire - 07CAA20C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07CABA4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2193, Events line 2267, Actions line 2341.

<a id="trigger-08f4ec1c"></a>

### 42. Helicopter Attacked - 08F4EC1C

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08F4E85C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create/recruit team [1 Blackhawk Team (0D7D821C)](trn01t-teams.md#team-0d7d821c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2194, Events line 2268, Actions line 2342.

<a id="trigger-08fa96ec"></a>

### 43. Drill Sarge 5 - 08FA96EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Target Range Sighted (08FA93FC)](#trigger-08fa93fc).

Attached scope: tag definitions 08FA94EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Objective 4 Reminder (0922EBFC)](#trigger-0922ebfc).
2. Play voice notification Mis_T1_DrillSearg05.
3. Enable and reset applicable timers for [Drill Sarge 5 Text (0956E23C)](#trigger-0956e23c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2195, Events line 2269, Actions line 2343.

<a id="trigger-08fa93fc"></a>

### 44. Target Range Sighted - 08FA93FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 29 tagged map cells: (74, 46), (75, 46), (76, 46), (77, 46), (78, 46), (79, 46), (80, 46), (74, 47), (75, 47), (76, 47), (77, 47), (78, 47), (79, 47), (80, 47), (74, 48), (75, 48), (79, 48), (80, 48), (74, 49), (75, 49), (79, 49), (80, 49), (74, 50), (75, 50), (79, 50), (80, 50), (79, 51), (80, 51), (80, 52); tag 08FA91FC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Drill Sarge 5 (08FA96EC)](#trigger-08fa96ec).
2. Reveal terrain around waypoint 7 (cell 65, 47).
3. Play sound HealCrate.
4. Reveal terrain around waypoint 16 (cell 71, 40).
5. Disable [Cross Bridge Reminder (086E174C)](#trigger-086e174c).
6. Enable and reset applicable timers for [Point to Range (0B45F65C)](#trigger-0b45f65c).
7. Enable and reset applicable timers for [Point to Range Stop (0B45F36C)](#trigger-0b45f36c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2196, Events line 2270, Actions line 2344.

<a id="trigger-086e174c"></a>

### 45. Cross Bridge Reminder - 086E174C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Engineer Enters Hut (0922739C)](#trigger-0922739c).

Attached scope: tag definitions 086E154C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Move your troops across the bridge” (MISSION:TRN01cc).
2. Play Anim At; main setting 472; location/duration field D.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2197, Events line 2271, Actions line 2345.

<a id="trigger-0b45f65c"></a>

### 46. Point to Range - 0B45F65C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Target Range Sighted (08FA93FC)](#trigger-08fa93fc).

Attached scope: tag definitions 0B45F45C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 476; location/duration field AW.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2198, Events line 2272, Actions line 2346.

<a id="trigger-0b45f36c"></a>

### 47. Point to Range Stop - 0B45F36C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Target Range Sighted (08FA93FC)](#trigger-08fa93fc).

Attached scope: tag definitions 084D7D8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Point to Range (0B45F65C)](#trigger-0b45f65c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2199, Events line 2273, Actions line 2347.

<a id="trigger-07b499ac"></a>

### 48. Tank Sighted - 07B499AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 27 tagged map cells: (65, 24), (65, 25), (66, 25), (65, 26), (66, 26), (66, 27), (66, 28), (67, 28), (64, 29), (65, 29), (66, 29), (67, 29), (63, 30), (64, 30), (65, 30), (66, 30), (62, 31), (63, 31), (61, 32), (62, 32), (63, 32), (61, 33), (62, 33), (63, 33), (61, 34), (62, 34), (61, 35); tag 07B4960C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Drill Sarge 8 (07B4951C)](#trigger-07b4951c).
2. Reveal terrain around waypoint 8 (cell 53, 24).
3. Play sound HealCrate.
4. Enable and reset applicable timers for [Smoke From Tank (07AD555C)](#trigger-07ad555c).
5. Enable and reset applicable timers for [Objective 6b Reminder (07AE7BAC)](#trigger-07ae7bac).
6. Disable [Objective 6a Reminder (0922E85C)](#trigger-0922e85c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2200, Events line 2274, Actions line 2348.

<a id="trigger-07b4951c"></a>

### 49. Drill Sarge 8 - 07B4951C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tank Sighted (07B499AC)](#trigger-07b499ac).

Attached scope: tag definitions 07B4931C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 6: Destroy the derelict tank” (MISSION:TRN01i).
2. Play voice notification Mis_T1_DrillSearg08.
3. Disable [Drill Sarge 7 Text (090C6E1C)](#trigger-090c6e1c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2201, Events line 2275, Actions line 2349.

<a id="trigger-07536f3c"></a>

### 50. Bridge Sighted - 07536F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0753052C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 13 (cell 43, 36).
2. Reveal terrain around waypoint 14 (cell 43, 41).
3. Reveal terrain around waypoint 15 (cell 43, 47).
4. Play sound HealCrate.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2202, Events line 2276, Actions line 2350.

<a id="trigger-0922739c"></a>

### 51. Engineer Enters Hut - 0922739C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Bridge Repair Hut (CABHUT), owner Civie1 House, cell (80, 65), tag 09223EAC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector -1 (unresolved or special selector).

**Then perform these actions in order:**

1. Display message “Objective 3 Complete” (MISSION:Objective3).
2. Disable [Objective 3 Reminder (0922D15C)](#trigger-0922d15c).
3. Display message “Move your troops across the bridge” (MISSION:TRN01cc).
4. Enable and reset applicable timers for [Cross Bridge Reminder (086E174C)](#trigger-086e174c).
5. Enable and reset applicable timers for [Point Across Bridge (0B45FC0C)](#trigger-0b45fc0c).
6. Enable and reset applicable timers for [Point Across Bridge Stop (0B45F91C)](#trigger-0b45f91c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2203, Events line 2277, Actions line 2351.

<a id="trigger-0b45fc0c"></a>

### 52. Point Across Bridge - 0B45FC0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Engineer Enters Hut (0922739C)](#trigger-0922739c).

Attached scope: tag definitions 0B45FA0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 472; location/duration field D.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2204, Events line 2278, Actions line 2352.

<a id="trigger-0b45f91c"></a>

### 53. Point Across Bridge Stop - 0B45F91C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Engineer Enters Hut (0922739C)](#trigger-0922739c).

Attached scope: tag definitions 084D7F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Point Across Bridge (0B45FC0C)](#trigger-0b45fc0c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2205, Events line 2279, Actions line 2353.

<a id="trigger-094b9f34"></a>

### 54. Copter - 094B9F34

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: NightHawk Transport (SHAD), owner Civie1 House, cell (37, 66), tag 094BA404, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Play sound HealCrate.
3. Reveal terrain around waypoint 17 (cell 36, 65).
4. Play sound BlackOpsSelect.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2206, Events line 2280, Actions line 2354.

<a id="trigger-094bce04"></a>

### 55. Farm_Cow - 094BCE04

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).

**Then perform these actions in order:**

1. Play sound CowDie.
2. Display message “Bovine rescued” (MISSION:All05j).
3. Enable and reset applicable timers for [Cow Prize (0AF1F7EC)](#trigger-0af1f7ec).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2207, Events line 2281, Actions line 2355.

<a id="trigger-0af1f7ec"></a>

### 56. Cow Prize - 0AF1F7EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Farm_Cow (094BCE04)](#trigger-094bce04).

Attached scope: tag definitions 0AF1F39C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound HealCrate.
2. Create crate type 8 at waypoint 18 (cell 61, 17).
3. Play voice notification Mis_T2_DrillSearg18.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2208, Events line 2282, Actions line 2356.

<a id="trigger-0972aa24"></a>

### 57. Con Destroyed - 0972AA24

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Construction Yard (GACNST), owner Other1 House, cell (47, 79), tag 0972A634, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [Special Engineer (0AF766CC)](trn01t-teams.md#team-0af766cc) at waypoint 19 (cell 48, 80).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2209, Events line 2283, Actions line 2357.

<a id="trigger-08dade24"></a>

### 58. Cow - 08DADE24

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Cow (COW), owner Civie1 House, cell (21, 60), tag 08DAD3F4, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).
2. Play sound CowSelect.
3. Reveal terrain around waypoint 20 (cell 20, 59).
4. Reveal terrain around waypoint 49 (cell 24, 57).
5. Enable and reset applicable timers for [Bought the Farm (0A3AFF3C)](#trigger-0a3aff3c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2210, Events line 2284, Actions line 2358.

<a id="trigger-0a3aff3c"></a>

### 59. Bought the Farm - 0A3AFF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Cow (08DADE24)](#trigger-08dade24).

Attached scope: Farm (CAFARM01), owner Civie1 House, cell (22, 56), tag 0A3AFE5C, persistence mode 0; Farm Silo (CAFARM02), owner Civie1 House, cell (24, 55), tag 0A3AFE5C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2211, Events line 2285, Actions line 2359.

<a id="trigger-07c4fb34"></a>

### 60. Friendly Destroyed - 07C4FB34

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Chrono Miner (CMIN), owner Other1 House, cell (48, 87), tag 07C4F3D4, persistence mode 0; Allied Barracks (GAPILE), owner Other1 House, cell (56, 85), tag 07C4F3D4, persistence mode 0; Allied Battle Lab (GATECH), owner Other1 House, cell (53, 80), tag 07C4F3D4, persistence mode 0; Allied Ore Refinery (GAREFN), owner Other1 House, cell (46, 89), tag 07C4F3D4, persistence mode 0; Allied War Factory (GAWEAP), owner Other1 House, cell (52, 95), tag 07C4F3D4, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (63, 79), tag 07C4F3D4, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (53, 75), tag 07C4F3D4, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (43, 74), tag 07C4F3D4, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (34, 76), tag 07C4F3D4, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (41, 89), tag 07C4F3D4, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (54, 102), tag 07C4F3D4, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (63, 109), tag 07C4F3D4, persistence mode 0; Power Plant (GAPOWR), owner Other1 House, cell (46, 76), tag 07C4F3D4, persistence mode 0; Power Plant (GAPOWR), owner Other1 House, cell (48, 93), tag 07C4F3D4, persistence mode 0; Power Plant (GAPOWR), owner Other1 House, cell (61, 98), tag 07C4F3D4, persistence mode 0; Power Plant (GAPOWR), owner Other1 House, cell (57, 82), tag 07C4F3D4, persistence mode 0; Prism Tower (ATESLA), owner Other2 House, cell (65, 96), tag 07C4F3D4, persistence mode 0; Prism Tower (ATESLA), owner Other2 House, cell (65, 90), tag 07C4F3D4, persistence mode 0; Air Force Command Headquarters (GAAIRC), owner Other1 House, cell (57, 100), tag 07C4F3D4, persistence mode 0; Allied Barracks (GAPILE), owner Other1 House, cell (75, 39), tag 07C4F3D4, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2212, Events line 2286, Actions line 2360.

<a id="trigger-07c57f34"></a>

### 61. Farm_Other - 07C57F34

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Farm_Cow (094BCE04)](#trigger-094bce04).

Attached scope: Farm (CAFARM01), owner Civie1 House, cell (60, 14), tag 094BCB94, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Play sound CowFear.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2213, Events line 2287, Actions line 2361.

<a id="trigger-07c412f4"></a>

### 62. Engineer Landed - 07C412F4

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C4A934 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Engineer Landed) is set.

**Then perform these actions in order:**

1. Create/recruit team [1 Engineer (0C1046CC)](trn01t-teams.md#team-0c1046cc).
2. Enable and reset applicable timers for [Point at Bridge Hut (0B45830C)](#trigger-0b45830c).
3. Enable and reset applicable timers for [Point at Bridge Hut Stop (0B45FE5C)](#trigger-0b45fe5c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2214, Events line 2288, Actions line 2362.

<a id="trigger-0b45830c"></a>

### 63. Point at Bridge Hut - 0B45830C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Engineer Landed (07C412F4)](#trigger-07c412f4).

Attached scope: tag definitions 0B45FF4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 479; location/duration field AT.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2215, Events line 2289, Actions line 2363.

<a id="trigger-0b45fe5c"></a>

### 64. Point at Bridge Hut Stop - 0B45FE5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Engineer Landed (07C412F4)](#trigger-07c412f4).

Attached scope: tag definitions 084D7E6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Point at Bridge Hut (0B45830C)](#trigger-0b45830c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2216, Events line 2290, Actions line 2364.

<a id="trigger-07b582d4"></a>

### 65. Helicopter Leaves - 07B582D4

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B97B64 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Helicopter Leaves) is set.

Flag writers in this mission: set local flag 1 (Helicopter Leaves) at [Heli Ready to Leave (0C4ABEBC)](#trigger-0c4abebc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [1 Blackhawk BadGuy2 (0D6E0A4C)](trn01t-teams.md#team-0d6e0a4c).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2217, Events line 2291, Actions line 2365.

<a id="trigger-0af1e1ac"></a>

### 66. Ambient River 1 - 0AF1E1AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AF1E0CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_River at waypoint 23 (cell 86, 96).
2. Play sound _Amb_River at waypoint 24 (cell 92, 85).
3. Play sound _Amb_River at waypoint 25 (cell 90, 72).
4. Play sound _Amb_River at waypoint 26 (cell 86, 59).
5. Play sound _Amb_River at waypoint 3 (cell 77, 58).
6. Play sound _Amb_River at waypoint 27 (cell 68, 47).
7. Play sound _Amb_River at waypoint 28 (cell 63, 37).
8. Play sound _Amb_River at waypoint 29 (cell 53, 39).
9. Play sound _Amb_River at waypoint 14 (cell 43, 41).
10. Reveal terrain around waypoint 44 (cell 40, 81).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2218, Events line 2292, Actions line 2366.

<a id="trigger-0af0a10c"></a>

### 67. Ambient River 2 - 0AF0A10C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AF091CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_River at waypoint 30 (cell 35, 39).
2. Play sound _Amb_River at waypoint 31 (cell 26, 36).
3. Play sound _Amb_River at waypoint 32 (cell 31, 49).
4. Play sound _Amb_River at waypoint 33 (cell 29, 67).
5. Play sound _Amb_River at waypoint 34 (cell 24, 73).
6. Play sound _Amb_River at waypoint 36 (cell 101, 73).
7. Play sound _Amb_River at waypoint 37 (cell 99, 59).
8. Play sound _Amb_River at waypoint 35 (cell 93, 51).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2219, Events line 2293, Actions line 2367.

<a id="trigger-07feadbc"></a>

### 68. Ambient Wind - 07FEADBC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FEA2AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindPlains at waypoint 38 (cell 72, 104).
2. Play sound _Amb_WindPlains at waypoint 12 (cell 69, 93).
3. Play sound _Amb_WindPlains at waypoint 39 (cell 73, 84).
4. Play sound _Amb_WindPlains at waypoint 40 (cell 76, 74).
5. Play sound _Amb_WindPlains at waypoint 8 (cell 53, 24).
6. Play sound _Amb_WindPlains at waypoint 41 (cell 50, 59).
7. Play sound _Amb_WindPlains at waypoint 42 (cell 60, 58).
8. Play sound _Amb_WindPlains at waypoint 43 (cell 57, 70).
9. Play sound _Amb_WindPlains at waypoint 21 (cell 38, 63).
10. Play sound _Amb_WindPlains at waypoint 20 (cell 20, 59).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2220, Events line 2294, Actions line 2368.

<a id="trigger-0c0cb4bc"></a>

### 69. Cow Country - 0C0CB4BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 28 tagged map cells: (45, 43), (46, 43), (40, 44), (41, 44), (45, 44), (46, 44), (40, 45), (41, 45), (45, 45), (46, 45), (40, 46), (41, 46), (45, 46), (46, 46), (40, 47), (41, 47), (42, 47), (43, 47), (44, 47), (45, 47), (46, 47), (40, 48), (41, 48), (42, 48), (43, 48), (44, 48), (45, 48), (46, 48); tag 0C0CB0DC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Display message “Hey! You're not supposed to be here!” (MISSION:Sov11e).
2. Play sound CowDie.

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2221, Events line 2295, Actions line 2369.

<a id="trigger-0b08da1c"></a>

### 70. Heli Preps to Leave - 0B08DA1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B08ED8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Annoyed) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Heli Ready to Leave (0C4ABEBC)](#trigger-0c4abebc).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2222, Events line 2296, Actions line 2370.

<a id="trigger-0c4abebc"></a>

### 71. Heli Ready to Leave - 0C4ABEBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Heli Preps to Leave (0B08DA1C)](#trigger-0b08da1c).

Attached scope: tag definitions 0C4ABA6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 1 (Helicopter Leaves).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2223, Events line 2297, Actions line 2371.

<a id="trigger-0893ee4c"></a>

### 72. Far Target Destroyed - 0893EE4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Practice Target (CAMSC12), owner BadGuy1 House, cell (65, 43), tag 0893EAEC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 5 (Far Target).

Source locator: MAPS01.MIX/trn01t.map; Triggers line 2224, Events line 2298, Actions line 2372.

[All team rosters and ordered plans](trn01t-teams.md) | [All mission overrides](trn01t-overrides.md)
