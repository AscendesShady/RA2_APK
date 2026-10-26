# Operation: Dark Night

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for all05s.map.](../../images/map-all05s.svg)

*Initial placement schematic for all05s.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** all05s.map. **Effective extracted member:** MAPS01.MIX/all05s.map. **Trigger definitions:** 128.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all05s-teams.md) | [All mission overrides](all05s-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | SNOW |
| Map size | 0,0,50,130 |
| Visible local rectangle | 2,53,45,71 |
| Placed vehicles | 5 |
| Placed infantry | 91 |
| Placed structures | 171 |
| Placed aircraft | 0 |
| Team templates | 42 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Tanya House | 0 | Tanya |
| 1 | Spies House | 0 | Spies |
| 2 | Engineers House | 100 | Engineers |
| 3 | RedTeam House | 100 | RedTeam |
| 4 | Reinforcement House | 0 | Reinforcements |
| 5 | YellowTeam House | 100 | YellowTeam |
| 6 | OrangeTeam House | 100 | OrangeTeam |
| 7 | Rebels House | 0 | Rebels |
| 8 | Civilians House | 0 | Civilians |
| 9 | Player House | 100 | Player |
| 10 | Mr. Neutral House | 0 | Mr. Neutral |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Nuke1Complete,0 |
| 1 | Nuke 2 Complete,0 |
| 2 | BattleLab Infiltrat,0 |
| 3 | Tesla 1 Activated,0 |
| 4 | Tesla 2 Activated,0 |
| 5 | Nuke1Captured,0 |
| 6 | Nuke 2 Captured,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Mission Failed (07474A30)](#trigger-07474a30) | 4 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 22 (country/type PLAYER; placed owner Player House) the loser. |
| [Victory 2 (09F98660)](#trigger-09f98660) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 22 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-06b41da0"></a>

### 1. BattleLab Entered 2 - 06B41DA0

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BattleLab Entered (0A19C0CC)](#trigger-0a19c0cc).

Attached scope: tag definitions 0A1918EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 2 (BattleLab Infiltrat).
2. Play sound MessageText.
3. Disable [Objective 1 (074734A0)](#trigger-074734a0).
4. Enable and reset applicable timers for [Objective 1 Complete (03E8CADC)](#trigger-03e8cadc).
5. Play voice notification Mis_A5_EvaMapEnlarging.
6. Display message “Silo coordinates acquired successfully - Enlarging map size to compensate” (MISSION:All05p).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6102, Events line 6232, Actions line 6362.

<a id="trigger-074734a0"></a>

### 2. Objective 1 - 074734A0

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 1 Given (0747E330)](#trigger-0747e330).

Attached scope: tag definitions 07477C80 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 40 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “Objective 1: Infiltrate the Soviet Battle Lab with a Spy” (MISSION:All05a).
3. Create radar-event marker type 1 at waypoint 11 (cell 101, 95).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6103, Events line 6233, Actions line 6363.

<a id="trigger-03e8cadc"></a>

### 3. Objective 1 Complete - 03E8CADC

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BattleLab Entered 2 (06B41DA0)](#trigger-06b41da0).

Attached scope: tag definitions 03E8C0EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Secondary Objective Complete” (MISSION:All01J).
2. Play voice notification EVA_SecondaryObjectiveAchieved.
3. Play sound MessageText.
4. Enable and reset applicable timers for [Objective 1 Complete b (0B577F3C)](#trigger-0b577f3c).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6104, Events line 6234, Actions line 6364.

<a id="trigger-0b577f3c"></a>

### 4. Objective 1 Complete b - 0B577F3C

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 1 Complete (03E8CADC)](#trigger-03e8cadc).

Attached scope: tag definitions 0B57793C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Objective 2 Given (098CFF60)](#trigger-098cff60).
2. Enable and reset applicable timers for [Resize Player View (07479F60)](#trigger-07479f60).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6105, Events line 6235, Actions line 6365.

<a id="trigger-098cff60"></a>

### 5. Objective 2 Given - 098CFF60

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 1 Complete b (0B577F3C)](#trigger-0b577f3c).

Attached scope: tag definitions 098CBB70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 23 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Objective 2 (098CEB70)](#trigger-098ceb70).
2. Display message “Objective 2: Eliminate the two Soviet Nuclear Missile Silos” (MISSION:All05b).
3. Play sound MessageText.
4. Create radar-event marker type 1 at waypoint 9 (cell 66, 41).
5. Create radar-event marker type 1 at waypoint 10 (cell 59, 66).
6. Enable and reset applicable timers for [Objective 2b (09C205E0)](#trigger-09c205e0).
7. Enable and reset applicable timers for [Objective 2c (09C20090)](#trigger-09c20090).
8. Enable and reset applicable timers for [Enable Yellow Patrols (07CE5F60)](#trigger-07ce5f60).
9. Enable and reset applicable timers for [Enable Orange Patrols (086E46D0)](#trigger-086e46d0).
10. Reveal terrain around waypoint 9 (cell 66, 41).
11. Reveal terrain around waypoint 10 (cell 59, 66).
12. Play voice notification EVA_NewObjectiveReceived.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6106, Events line 6236, Actions line 6366.

<a id="trigger-07479f60"></a>

### 6. Resize Player View - 07479F60

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 1 Complete b (0B577F3C)](#trigger-0b577f3c).

Attached scope: tag definitions 0747EF70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Resize Player View; main setting 0; parameter 1: 2, parameter 2: 4, parameter 3: 45, parameter 4: 120.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6107, Events line 6237, Actions line 6367.

<a id="trigger-098ceb70"></a>

### 7. Objective 2 - 098CEB70

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 2 Given (098CFF60)](#trigger-098cff60).

Attached scope: tag definitions 098C9E70 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 40 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Eliminate the two Soviet Nuclear Missile Silos” (MISSION:All05b).
2. Play sound MessageText.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6108, Events line 6238, Actions line 6368.

<a id="trigger-09c205e0"></a>

### 8. Objective 2b - 09C205E0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 2 Given (098CFF60)](#trigger-098cff60).

Attached scope: tag definitions 09C20150 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 40 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 9 (cell 66, 41).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6109, Events line 6239, Actions line 6369.

<a id="trigger-09c20090"></a>

### 9. Objective 2c - 09C20090

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 2 Given (098CFF60)](#trigger-098cff60).

Attached scope: tag definitions 09C21D30 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 40 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 10 (cell 59, 66).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6110, Events line 6240, Actions line 6370.

<a id="trigger-07ce5f60"></a>

### 10. Enable Yellow Patrols - 07CE5F60

Owner reference: YellowTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 2 Given (098CFF60)](#trigger-098cff60).

Attached scope: tag definitions 07CE7350 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Yellow Patrol 1 (07D01310)](#trigger-07d01310).
2. Enable and reset applicable timers for [Yellow Patrol 2 (06F87F60)](#trigger-06f87f60).
3. Enable and reset applicable timers for [Yellow Patrol 3 (07CA1DC0)](#trigger-07ca1dc0).
4. Enable and reset applicable timers for [Yellow Patrol 4 (07CE4030)](#trigger-07ce4030).
5. Enable and reset applicable timers for [Yellow Patrol 5 (07CE0B60)](#trigger-07ce0b60).
6. Enable and reset applicable timers for [Yellow Patrol 6 (07CE0350)](#trigger-07ce0350).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6111, Events line 6241, Actions line 6371.

<a id="trigger-086e46d0"></a>

### 11. Enable Orange Patrols - 086E46D0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 2 Given (098CFF60)](#trigger-098cff60).

Attached scope: tag definitions 086E6EF0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Orange Patrol 2 (087DF160)](#trigger-087df160).
2. Enable and reset applicable timers for [Orange Patrol 3 (087DACF0)](#trigger-087dacf0).
3. Enable and reset applicable timers for [Orange Patrol 4 (087DAAA0)](#trigger-087daaa0).
4. Enable and reset applicable timers for [Orange Patrol 5 (087DA850)](#trigger-087da850).
5. Enable and reset applicable timers for [Orange Patrol 6 (087DA600)](#trigger-087da600).
6. Enable and reset applicable timers for [Orange Patrol 7 (087DA1A0)](#trigger-087da1a0).
7. Enable and reset applicable timers for [Orange Patrol 8 (087DBEB0)](#trigger-087dbeb0).
8. Enable and reset applicable timers for [Orange Patrol 9 (087DBAB0)](#trigger-087dbab0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6112, Events line 6242, Actions line 6372.

<a id="trigger-07d01310"></a>

### 12. Yellow Patrol 1 - 07D01310

Owner reference: YellowTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Yellow Patrols (07CE5F60)](#trigger-07ce5f60).

Attached scope: tag definitions 07D02470 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yellow Patrol 1 (070290C0)](all05s-teams.md#team-070290c0) at waypoint 45 (cell 69, 44).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6113, Events line 6243, Actions line 6373.

<a id="trigger-06f87f60"></a>

### 13. Yellow Patrol 2 - 06F87F60

Owner reference: YellowTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Yellow Patrols (07CE5F60)](#trigger-07ce5f60).

Attached scope: tag definitions 06F85910 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yellow Patrol 2 (07CECF30)](all05s-teams.md#team-07cecf30) at waypoint 56 (cell 62, 36).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6114, Events line 6244, Actions line 6374.

<a id="trigger-07ca1dc0"></a>

### 14. Yellow Patrol 3 - 07CA1DC0

Owner reference: YellowTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Yellow Patrols (07CE5F60)](#trigger-07ce5f60).

Attached scope: tag definitions 07CA6F70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yellow Patrol 3 (07CEFC70)](all05s-teams.md#team-07cefc70) at waypoint 49 (cell 66, 31).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6115, Events line 6245, Actions line 6375.

<a id="trigger-07ce4030"></a>

### 15. Yellow Patrol 4 - 07CE4030

Owner reference: YellowTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Yellow Patrols (07CE5F60)](#trigger-07ce5f60).

Attached scope: tag definitions 07CE0C20 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yellow Patrol 4 (07CE9E80)](all05s-teams.md#team-07ce9e80) at waypoint 52 (cell 75, 35).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6116, Events line 6246, Actions line 6376.

<a id="trigger-07ce0b60"></a>

### 16. Yellow Patrol 5 - 07CE0B60

Owner reference: YellowTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Yellow Patrols (07CE5F60)](#trigger-07ce5f60).

Attached scope: tag definitions 07CE2C80 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yellow Patrol 5 (07CEA3C0)](all05s-teams.md#team-07cea3c0) at waypoint 53 (cell 72, 43).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6117, Events line 6247, Actions line 6377.

<a id="trigger-07ce0350"></a>

### 17. Yellow Patrol 6 - 07CE0350

Owner reference: YellowTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Yellow Patrols (07CE5F60)](#trigger-07ce5f60).

Attached scope: tag definitions 07CE01C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yellow Patrol 6 (06F85F30)](all05s-teams.md#team-06f85f30) at waypoint 60 (cell 84, 59).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6118, Events line 6248, Actions line 6378.

<a id="trigger-087df160"></a>

### 18. Orange Patrol 2 - 087DF160

Owner reference: OrangeTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Orange Patrols (086E46D0)](#trigger-086e46d0).

Attached scope: tag definitions 087DAF70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Orange Patrol 2 (087DFB40)](all05s-teams.md#team-087dfb40) at waypoint 75 (cell 59, 61).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6119, Events line 6249, Actions line 6379.

<a id="trigger-087dacf0"></a>

### 19. Orange Patrol 3 - 087DACF0

Owner reference: OrangeTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Orange Patrols (086E46D0)](#trigger-086e46d0).

Attached scope: tag definitions 087DAB60 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Orange Patrol 3 (087DFA50)](all05s-teams.md#team-087dfa50) at waypoint 77 (cell 47, 69).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6120, Events line 6250, Actions line 6380.

<a id="trigger-087daaa0"></a>

### 20. Orange Patrol 4 - 087DAAA0

Owner reference: OrangeTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Orange Patrols (086E46D0)](#trigger-086e46d0).

Attached scope: tag definitions 087DA910 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Orange Patrol 4 (087DF960)](all05s-teams.md#team-087df960) at waypoint 79 (cell 42, 65).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6121, Events line 6251, Actions line 6381.

<a id="trigger-087da850"></a>

### 21. Orange Patrol 5 - 087DA850

Owner reference: OrangeTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Orange Patrols (086E46D0)](#trigger-086e46d0).

Attached scope: tag definitions 087DA6C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Orange Patrol 5 (087D9CE0)](all05s-teams.md#team-087d9ce0) at waypoint 81 (cell 29, 48).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6122, Events line 6252, Actions line 6382.

<a id="trigger-087da600"></a>

### 22. Orange Patrol 6 - 087DA600

Owner reference: OrangeTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Orange Patrols (086E46D0)](#trigger-086e46d0).

Attached scope: tag definitions 087DA260 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Orange Patrol 6 (087D9BF0)](all05s-teams.md#team-087d9bf0) at waypoint 83 (cell 36, 69).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6123, Events line 6253, Actions line 6383.

<a id="trigger-087da1a0"></a>

### 23. Orange Patrol 7 - 087DA1A0

Owner reference: OrangeTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Orange Patrols (086E46D0)](#trigger-086e46d0).

Attached scope: tag definitions 087DBF70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Orange Patrol 7 (087D9B00)](all05s-teams.md#team-087d9b00) at waypoint 85 (cell 47, 80).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6124, Events line 6254, Actions line 6384.

<a id="trigger-087dbeb0"></a>

### 24. Orange Patrol 8 - 087DBEB0

Owner reference: OrangeTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Orange Patrols (086E46D0)](#trigger-086e46d0).

Attached scope: tag definitions 087DBB70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Orange Patrol 8 (087D9F30)](all05s-teams.md#team-087d9f30) at waypoint 89 (cell 38, 61).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6125, Events line 6255, Actions line 6385.

<a id="trigger-087dbab0"></a>

### 25. Orange Patrol 9 - 087DBAB0

Owner reference: OrangeTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Orange Patrols (086E46D0)](#trigger-086e46d0).

Attached scope: tag definitions 087DB980 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Orange Patrol 9 (087D9E40)](all05s-teams.md#team-087d9e40) at waypoint 93 (cell 24, 50).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6126, Events line 6256, Actions line 6386.

<a id="trigger-07476a30"></a>

### 26. BattleLab Destroyed - 07476A30

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “The Battle Lab has been destroyed - CRITICAL STRUCTURE LOST” (MISSION:All05l).
2. Enable and reset applicable timers for [Mission Failed (07474A30)](#trigger-07474a30).
3. Play sound MessageText.
4. Play voice notification Mis_A5_EvaBattleLabDestroyed.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6127, Events line 6257, Actions line 6387.

<a id="trigger-07474a30"></a>

### 27. Mission Failed - 07474A30

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BattleLab Destroyed (07476A30)](#trigger-07476a30); enable from [Tanya Dies 2 (08FEB83C)](#trigger-08feb83c).

Attached scope: tag definitions 07474740 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 22 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6128, Events line 6258, Actions line 6388.

<a id="trigger-078f7090"></a>

### 28. Nuke 1 Entered - 078F7090

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke 1 Destroyed (07914350)](#trigger-07914350).

Attached scope: Nuclear Missile Silo (NAMISL), owner YellowTeam House, cell (65, 40), tag 07910D30, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Set local flag 5 (Nuke1Captured).
2. Disable [Objective 2b (09C205E0)](#trigger-09c205e0).
3. All to Hunt: owner selector 18 (country/type YELLOWTEAM; placed owner YellowTeam House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6129, Events line 6259, Actions line 6389.

<a id="trigger-07914350"></a>

### 29. Nuke 1 Destroyed - 07914350

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 0 (Nuke1Complete).
2. Disable [Objective 2b (09C205E0)](#trigger-09c205e0).
3. All to Hunt: owner selector 18 (country/type YELLOWTEAM; placed owner YellowTeam House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6130, Events line 6260, Actions line 6390.

<a id="trigger-0747e330"></a>

### 30. Objective 1 Given - 0747E330

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Helicopter Lands (078E70A0)](#trigger-078e70a0).

Attached scope: tag definitions 0747B3F0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 73 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “Objective 1: Infiltrate the Soviet Battle Lab with a Spy” (MISSION:All05a).
3. Create radar-event marker type 1 at waypoint 11 (cell 101, 95).
4. Enable and reset applicable timers for [Objective 1 (074734A0)](#trigger-074734a0).
5. Reveal terrain around waypoint 11 (cell 101, 95).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6131, Events line 6261, Actions line 6391.

<a id="trigger-08836b30"></a>

### 31. Tanya Dies - 08836B30

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Tanya Dies (080906B0)](#trigger-080906b0).

Attached scope: tag definitions 088361A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “Tanya has died - CRITICAL UNIT LOST” (MISSION:All05k).
2. Play sound MessageText.
3. Enable and reset applicable timers for [Tanya Dies 2 (08FEB83C)](#trigger-08feb83c).
4. Play voice notification Mis_A1_EvaTanyaDeath.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6132, Events line 6262, Actions line 6392.

<a id="trigger-08feb83c"></a>

### 32. Tanya Dies 2 - 08FEB83C

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tanya Dies (08836B30)](#trigger-08836b30).

Attached scope: tag definitions 08FE93EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_CriticalUnitLost.
2. Enable and reset applicable timers for [Mission Failed (07474A30)](#trigger-07474a30).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6133, Events line 6263, Actions line 6393.

<a id="trigger-06b4b050"></a>

### 33. Red Patrol 1 - 06B4B050

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B4C800 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Red Patrol 1 (082ABA4C)](all05s-teams.md#team-082aba4c) at waypoint 2 (cell 127, 141).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6134, Events line 6264, Actions line 6394.

<a id="trigger-06b5f920"></a>

### 34. Red Patrol 2 - 06B5F920

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B5D930 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Red Patrol 2 (0A55348C)](all05s-teams.md#team-0a55348c) at waypoint 14 (cell 106, 83).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6135, Events line 6265, Actions line 6395.

<a id="trigger-06b5a430"></a>

### 35. Tesla Coil Spotted 1 - 06B5A430

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner RedTeam House, cell (97, 110), tag 06B5A0F0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 18 (cell 97, 110).
2. Create radar-event marker type 5 at waypoint 18 (cell 97, 110).
3. Play sound WarningAlarm.
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6136, Events line 6266, Actions line 6396.

<a id="trigger-06b74f60"></a>

### 36. Tesla Coil Spotted 2 - 06B74F60

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner RedTeam House, cell (107, 110), tag 06B74C00, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 19 (cell 107, 110).
2. Create radar-event marker type 5 at waypoint 19 (cell 107, 110).
3. Play sound WarningAlarm.
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6137, Events line 6267, Actions line 6397.

<a id="trigger-06b731f0"></a>

### 37. Hint: Power Plant 1 - 06B731F0

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Hint:Power 1 (0824AC2C)](#trigger-0824ac2c); enable from [Enable Hint:Power1b (08249B4C)](#trigger-08249b4c); enable from [Enable Hint:Power1c (0824989C)](#trigger-0824989c); enable from [Enable Hint:Power1d (0824965C)](#trigger-0824965c).

Attached scope: Tesla Reactor (NAPOWR), owner RedTeam House, cell (104, 102), tag 06B73790, persistence mode 0; Tesla Reactor (NAPOWR), owner RedTeam House, cell (98, 102), tag 06B73790, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 16 (cell 98, 101).
2. Reveal terrain around waypoint 22 (cell 104, 101).
3. Play voice notification Mis_A5_EvaSpyHint.
4. Create radar-event marker type 1 at waypoint 16 (cell 98, 101).
5. Create radar-event marker type 1 at waypoint 22 (cell 104, 101).
6. Destroy current instances of [Enable Hint:Power2a (0BEEAA2C)](#trigger-0beeaa2c).
7. Display message “HINT: Send a SPY into a TESLA REACTOR to shut down all base defenses” (MISSION:All05o).
8. Play sound MessageText.
9. Destroy current instances of [Enable Hint:Power2b (0BEEA3FC)](#trigger-0beea3fc).
10. Destroy current instances of [Enable Hint:Power2c (0BEEA1EC)](#trigger-0beea1ec).
11. Destroy current instances of [Enable Hint:Power2d (0BEEBF3C)](#trigger-0beebf3c).
12. Destroy current instances of [Hint: Power Plant 2 (0B5855E0)](#trigger-0b5855e0).
13. Enable and reset applicable timers for [Anim: Power Plants (0433F0DC)](#trigger-0433f0dc).
14. Enable and reset applicable timers for [Anim: Power Plants 2 (0433F61C)](#trigger-0433f61c).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6138, Events line 6268, Actions line 6398.

<a id="trigger-0beeaa2c"></a>

### 38. Enable Hint:Power2a - 0BEEAA2C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Power Plant 2 (0B5855E0)](#trigger-0b5855e0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6139, Events line 6269, Actions line 6399.

<a id="trigger-0beea3fc"></a>

### 39. Enable Hint:Power2b - 0BEEA3FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Enable Hint:Power2a (0BEEAA2C)](#trigger-0beeaa2c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type TANYA; placed owner Tanya House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Power Plant 2 (0B5855E0)](#trigger-0b5855e0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6140, Events line 6270, Actions line 6400.

<a id="trigger-0beea1ec"></a>

### 40. Enable Hint:Power2c - 0BEEA1EC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Enable Hint:Power2b (0BEEA3FC)](#trigger-0beea3fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 14 (country/type SPIES; placed owner Spies House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Power Plant 2 (0B5855E0)](#trigger-0b5855e0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6141, Events line 6271, Actions line 6401.

<a id="trigger-0beebf3c"></a>

### 41. Enable Hint:Power2d - 0BEEBF3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Enable Hint:Power2c (0BEEA1EC)](#trigger-0beea1ec).

Attached scope: 31 tagged map cells: (100, 80), (101, 80), (95, 81), (96, 81), (97, 81), (98, 81), (99, 81), (100, 81), (101, 81), (102, 81), (103, 81), (104, 81), (105, 81), (106, 81), (95, 82), (106, 82), (95, 83), (106, 83), (95, 84), (106, 84), (95, 85), (106, 85), (92, 86), (94, 86), (95, 86), (107, 86), (108, 86), (109, 86), (110, 86), (111, 86), (112, 86); tag 0BEEA4EC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type REBELS; placed owner Rebels House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Power Plant 2 (0B5855E0)](#trigger-0b5855e0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6142, Events line 6272, Actions line 6402.

<a id="trigger-0b5855e0"></a>

### 42. Hint: Power Plant 2 - 0B5855E0

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Hint:Power2a (0BEEAA2C)](#trigger-0beeaa2c); enable from [Enable Hint:Power2b (0BEEA3FC)](#trigger-0beea3fc); enable from [Enable Hint:Power2c (0BEEA1EC)](#trigger-0beea1ec); enable from [Enable Hint:Power2d (0BEEBF3C)](#trigger-0beebf3c).

Attached scope: Tesla Reactor (NAPOWR), owner RedTeam House, cell (100, 85), tag 0B582F50, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Hint: Power Plant 1 (06B731F0)](#trigger-06b731f0).
2. Play voice notification Mis_A5_EvaSpyHint.
3. Create radar-event marker type 1 at waypoint 20 (cell 100, 84).
4. Reveal terrain around waypoint 20 (cell 100, 84).
5. Play sound MessageText.
6. Display message “HINT: Send a SPY into a TESLA REACTOR to shut down all base defenses” (MISSION:All05o).
7. Destroy current instances of [Enable Hint:Power 1 (0824AC2C)](#trigger-0824ac2c).
8. Destroy current instances of [Enable Hint:Power1b (08249B4C)](#trigger-08249b4c).
9. Destroy current instances of [Enable Hint:Power1c (0824989C)](#trigger-0824989c).
10. Destroy current instances of [Enable Hint:Power1d (0824965C)](#trigger-0824965c).
11. Enable and reset applicable timers for [Anim: Power Plants (0433F0DC)](#trigger-0433f0dc).
12. Enable and reset applicable timers for [Anim: Power Plants 2 (0433F61C)](#trigger-0433f61c).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6143, Events line 6273, Actions line 6403.

<a id="trigger-0433f0dc"></a>

### 43. Anim: Power Plants - 0433F0DC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: Power Plant 1 (06B731F0)](#trigger-06b731f0); enable from [Hint: Power Plant 2 (0B5855E0)](#trigger-0b5855e0).

Attached scope: tag definitions 0433F70C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 479; location/duration field Q.
2. Play Anim At; main setting 479; location/duration field W.
3. Play Anim At; main setting 471; location/duration field U.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6144, Events line 6274, Actions line 6404.

<a id="trigger-0433f61c"></a>

### 44. Anim: Power Plants 2 - 0433F61C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: Power Plant 1 (06B731F0)](#trigger-06b731f0); enable from [Hint: Power Plant 2 (0B5855E0)](#trigger-0b5855e0).

Attached scope: tag definitions 0433D78C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Anim: Power Plants (0433F0DC)](#trigger-0433f0dc).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6145, Events line 6275, Actions line 6405.

<a id="trigger-0824ac2c"></a>

### 45. Enable Hint:Power 1 - 0824AC2C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Power Plant 1 (06B731F0)](#trigger-06b731f0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6146, Events line 6276, Actions line 6406.

<a id="trigger-08249b4c"></a>

### 46. Enable Hint:Power1b - 08249B4C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Enable Hint:Power 1 (0824AC2C)](#trigger-0824ac2c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type TANYA; placed owner Tanya House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Power Plant 1 (06B731F0)](#trigger-06b731f0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6147, Events line 6277, Actions line 6407.

<a id="trigger-0824989c"></a>

### 47. Enable Hint:Power1c - 0824989C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Enable Hint:Power1b (08249B4C)](#trigger-08249b4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 14 (country/type SPIES; placed owner Spies House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Power Plant 1 (06B731F0)](#trigger-06b731f0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6148, Events line 6278, Actions line 6408.

<a id="trigger-0824965c"></a>

### 48. Enable Hint:Power1d - 0824965C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Enable Hint:Power1c (0824989C)](#trigger-0824989c).

Attached scope: 41 tagged map cells: (89, 97), (89, 98), (89, 99), (89, 100), (89, 101), (89, 102), (89, 103), (89, 104), (89, 105), (90, 105), (90, 106), (98, 106), (99, 106), (100, 106), (101, 106), (103, 106), (104, 106), (105, 106), (106, 106), (90, 107), (91, 107), (92, 107), (98, 107), (101, 107), (102, 107), (103, 107), (106, 107), (92, 108), (93, 108), (94, 108), (95, 108), (96, 108), (97, 108), (98, 108), (106, 108), (107, 108), (108, 108), (109, 108), (110, 108), (111, 108), (112, 108); tag 08249C3C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type REBELS; placed owner Rebels House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Power Plant 1 (06B731F0)](#trigger-06b731f0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6149, Events line 6279, Actions line 6409.

<a id="trigger-03d734f0"></a>

### 49. Spies Dead 1 - 03D734F0

Owner reference: Reinforcements. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Spies Dead (06EF68E0)](#trigger-06ef68e0); enable from [Spies Dead 4d (0991D6A0)](#trigger-0991d6a0).

Attached scope: tag definitions 03D73060 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 14 (country/type SPIES; placed owner Spies House).

**Then perform these actions in order:**

1. Disable [Spies Dead 1 (03D734F0)](#trigger-03d734f0).
2. Enable and reset applicable timers for [Spies Dead 1b (03D72D50)](#trigger-03d72d50).
3. Supply reinforcement team [Reinforcements 1 (08533A2C)](all05s-teams.md#team-08533a2c).
4. Play voice notification Mis_A5_TanyaNeedSpies1.
5. Enable and reset applicable timers for [Helicopter Lands (078E70A0)](#trigger-078e70a0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6150, Events line 6280, Actions line 6410.

<a id="trigger-03d72d50"></a>

### 50. Spies Dead 1b - 03D72D50

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 1 (03D734F0)](#trigger-03d734f0).

Attached scope: tag definitions 03D72830 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Spies Dead 1b (03D72D50)](#trigger-03d72d50).
2. Enable and reset applicable timers for [Spies Dead 1c (03D72770)](#trigger-03d72770).
3. Play sound MessageText.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6151, Events line 6281, Actions line 6411.

<a id="trigger-078e70a0"></a>

### 51. Helicopter Lands - 078E70A0

Owner reference: Reinforcements. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 1 (03D734F0)](#trigger-03d734f0); enable from [Spies Dead 2 (083775A0)](#trigger-083775a0); enable from [Spies Dead 3 (08370580)](#trigger-08370580); enable from [Spies Dead 4 (083703F0)](#trigger-083703f0).

Attached scope: 36 tagged map cells: (113, 138), (111, 139), (112, 139), (113, 139), (114, 139), (110, 140), (111, 140), (112, 140), (113, 140), (114, 140), (115, 140), (109, 141), (110, 141), (111, 141), (112, 141), (113, 141), (114, 141), (115, 141), (111, 142), (112, 142), (113, 142), (114, 142), (115, 142), (116, 142), (110, 143), (111, 143), (112, 143), (113, 143), (114, 143), (115, 143), (116, 143), (111, 144), (112, 144), (113, 144), (113, 145), (115, 145); tag 078E0180, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 17 (country/type REINFORCEMENTS; placed owner Reinforcement House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Spies House (079B4660)](#trigger-079b4660).
2. Enable and reset applicable timers for [Objective 1 Given (0747E330)](#trigger-0747e330).
3. Enable and reset applicable timers for [Mission Start 4 (08A40F60)](#trigger-08a40f60).
4. Enable and reset applicable timers for [Play Spies Movie (07D4739C)](#trigger-07d4739c).
5. Disable [Helicopter Lands (078E70A0)](#trigger-078e70a0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6152, Events line 6282, Actions line 6412.

<a id="trigger-03d72770"></a>

### 52. Spies Dead 1c - 03D72770

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 1b (03D72D50)](#trigger-03d72d50).

Attached scope: tag definitions 03D72530 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Additional Spies have arrived” (MISSION:All05f).
2. Create radar-event marker type 2 at waypoint 0 (cell 112, 141).
3. Disable [Spies Dead 1c (03D72770)](#trigger-03d72770).
4. Enable and reset applicable timers for [Spies Dead 1d (0991C520)](#trigger-0991c520).
5. Play sound MessageText.
6. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6153, Events line 6283, Actions line 6413.

<a id="trigger-079b4660"></a>

### 53. Change Spies House - 079B4660

Owner reference: Reinforcements. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Helicopter Lands (078E70A0)](#trigger-078e70a0).

Attached scope: tag definitions 079B6F70 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Spies (088BE7DC)](all05s-teams.md#team-088be7dc).
2. Enable and reset applicable timers for [Unally 2 (06F25E70)](#trigger-06f25e70).
3. Enable and reset applicable timers for [Enable Spies Dead (06EF68E0)](#trigger-06ef68e0).
4. Disable [Change Spies House (079B4660)](#trigger-079b4660).
5. Create/recruit team [Spies (088BE7DC)](all05s-teams.md#team-088be7dc).
6. Create/recruit team [Spies (088BE7DC)](all05s-teams.md#team-088be7dc).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6154, Events line 6284, Actions line 6414.

<a id="trigger-08a40f60"></a>

### 54. Mission Start 4 - 08A40F60

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Helicopter Lands (078E70A0)](#trigger-078e70a0).

Attached scope: tag definitions 08A40BA0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Play sound MessageText.
3. Display message “--Battle Control Online--” (MISSION:All05q).
4. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6155, Events line 6285, Actions line 6415.

<a id="trigger-07d4739c"></a>

### 55. Play Spies Movie - 07D4739C

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Helicopter Lands (078E70A0)](#trigger-078e70a0).

Attached scope: tag definitions 07D44E4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 86.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6156, Events line 6286, Actions line 6416.

<a id="trigger-0991c520"></a>

### 56. Spies Dead 1d - 0991C520

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 1c (03D72770)](#trigger-03d72770).

Attached scope: tag definitions 0991DC20 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Spies Dead 2 (083775A0)](#trigger-083775a0).
2. Disable [Spies Dead 1d (0991C520)](#trigger-0991c520).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6157, Events line 6287, Actions line 6417.

<a id="trigger-06f25e70"></a>

### 57. Unally 2 - 06F25E70

Owner reference: YellowTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change Spies House (079B4660)](#trigger-079b4660).

Attached scope: tag definitions 06F257F0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 13 (country/type TANYA; placed owner Tanya House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6158, Events line 6288, Actions line 6418.

<a id="trigger-06ef68e0"></a>

### 58. Enable Spies Dead - 06EF68E0

Owner reference: Reinforcements. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change Spies House (079B4660)](#trigger-079b4660).

Attached scope: tag definitions 06EF4D60 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Spies Dead 1 (03D734F0)](#trigger-03d734f0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6159, Events line 6289, Actions line 6419.

<a id="trigger-083775a0"></a>

### 59. Spies Dead 2 - 083775A0

Owner reference: Reinforcements. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 1d (0991C520)](#trigger-0991c520).

Attached scope: tag definitions 08370640 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 14 (country/type SPIES; placed owner Spies House).

**Then perform these actions in order:**

1. Disable [Spies Dead 2 (083775A0)](#trigger-083775a0).
2. Enable and reset applicable timers for [Spies Dead 2b (03D59E90)](#trigger-03d59e90).
3. Supply reinforcement team [Reinforcements 1 (08533A2C)](all05s-teams.md#team-08533a2c).
4. Play voice notification Mis_A5_TanyaNeedSpies2.
5. Enable and reset applicable timers for [Helicopter Lands (078E70A0)](#trigger-078e70a0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6160, Events line 6290, Actions line 6420.

<a id="trigger-03d59e90"></a>

### 60. Spies Dead 2b - 03D59E90

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 2 (083775A0)](#trigger-083775a0).

Attached scope: tag definitions 03D751E0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Spies Dead 2b (03D59E90)](#trigger-03d59e90).
2. Enable and reset applicable timers for [Spies Dead 2c (03D75090)](#trigger-03d75090).
3. Play sound MessageText.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6161, Events line 6291, Actions line 6421.

<a id="trigger-03d75090"></a>

### 61. Spies Dead 2c - 03D75090

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 2b (03D59E90)](#trigger-03d59e90).

Attached scope: tag definitions 03D75520 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Spies Dead 2d (0991DB60)](#trigger-0991db60).
2. Disable [Spies Dead 2c (03D75090)](#trigger-03d75090).
3. Create radar-event marker type 2 at waypoint 0 (cell 112, 141).
4. Display message “Additional Spies have arrived” (MISSION:All05f).
5. Play sound MessageText.
6. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6162, Events line 6292, Actions line 6422.

<a id="trigger-0991db60"></a>

### 62. Spies Dead 2d - 0991DB60

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 2c (03D75090)](#trigger-03d75090).

Attached scope: tag definitions 0991D9E0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Spies Dead 3 (08370580)](#trigger-08370580).
2. Disable [Spies Dead 2d (0991DB60)](#trigger-0991db60).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6163, Events line 6293, Actions line 6423.

<a id="trigger-08370580"></a>

### 63. Spies Dead 3 - 08370580

Owner reference: Reinforcements. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 2d (0991DB60)](#trigger-0991db60).

Attached scope: tag definitions 083771C0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 14 (country/type SPIES; placed owner Spies House).

**Then perform these actions in order:**

1. Disable [Spies Dead 3 (08370580)](#trigger-08370580).
2. Enable and reset applicable timers for [Spies Dead 3b (03D725E0)](#trigger-03d725e0).
3. Supply reinforcement team [Reinforcements 1 (08533A2C)](all05s-teams.md#team-08533a2c).
4. Play voice notification Mis_A5_TanyaNeedSpies3.
5. Enable and reset applicable timers for [Helicopter Lands (078E70A0)](#trigger-078e70a0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6164, Events line 6294, Actions line 6424.

<a id="trigger-03d725e0"></a>

### 64. Spies Dead 3b - 03D725E0

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 3 (08370580)](#trigger-08370580).

Attached scope: tag definitions 03D724A0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Spies Dead 3b (03D725E0)](#trigger-03d725e0).
2. Enable and reset applicable timers for [Spies Dead 3c (03D723E0)](#trigger-03d723e0).
3. Play sound MessageText.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6165, Events line 6295, Actions line 6425.

<a id="trigger-03d723e0"></a>

### 65. Spies Dead 3c - 03D723E0

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 3b (03D725E0)](#trigger-03d725e0).

Attached scope: tag definitions 03D778B0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Spies Dead 3c (03D723E0)](#trigger-03d723e0).
2. Enable and reset applicable timers for [Spies Dead 3d (0991D920)](#trigger-0991d920).
3. Create radar-event marker type 2 at waypoint 0 (cell 112, 141).
4. Display message “Additional Spies have arrived” (MISSION:All05f).
5. Play sound MessageText.
6. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6166, Events line 6296, Actions line 6426.

<a id="trigger-0991d920"></a>

### 66. Spies Dead 3d - 0991D920

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 3c (03D723E0)](#trigger-03d723e0).

Attached scope: tag definitions 0991D760 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Spies Dead 4 (083703F0)](#trigger-083703f0).
2. Disable [Spies Dead 3d (0991D920)](#trigger-0991d920).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6167, Events line 6297, Actions line 6427.

<a id="trigger-083703f0"></a>

### 67. Spies Dead 4 - 083703F0

Owner reference: Reinforcements. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 3d (0991D920)](#trigger-0991d920).

Attached scope: tag definitions 08370340 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 14 (country/type SPIES; placed owner Spies House).

**Then perform these actions in order:**

1. Disable [Spies Dead 4 (083703F0)](#trigger-083703f0).
2. Enable and reset applicable timers for [Spies Dead 4b (03D777F0)](#trigger-03d777f0).
3. Supply reinforcement team [Reinforcements 1 (08533A2C)](all05s-teams.md#team-08533a2c).
4. Play voice notification Mis_A5_TanyaNeedSpies1.
5. Enable and reset applicable timers for [Helicopter Lands (078E70A0)](#trigger-078e70a0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6168, Events line 6298, Actions line 6428.

<a id="trigger-03d777f0"></a>

### 68. Spies Dead 4b - 03D777F0

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 4 (083703F0)](#trigger-083703f0).

Attached scope: tag definitions 03D775C0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Spies Dead 4b (03D777F0)](#trigger-03d777f0).
2. Enable and reset applicable timers for [Spies Dead 4c (03D77470)](#trigger-03d77470).
3. Play sound MessageText.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6169, Events line 6299, Actions line 6429.

<a id="trigger-03d77470"></a>

### 69. Spies Dead 4c - 03D77470

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 4b (03D777F0)](#trigger-03d777f0).

Attached scope: tag definitions 03D773C0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Spies Dead 4c (03D77470)](#trigger-03d77470).
2. Enable and reset applicable timers for [Spies Dead 4d (0991D6A0)](#trigger-0991d6a0).
3. Create radar-event marker type 2 at waypoint 0 (cell 112, 141).
4. Display message “Additional Spies have arrived” (MISSION:All05f).
5. Play sound MessageText.
6. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6170, Events line 6300, Actions line 6430.

<a id="trigger-0991d6a0"></a>

### 70. Spies Dead 4d - 0991D6A0

Owner reference: Spies. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies Dead 4c (03D77470)](#trigger-03d77470).

Attached scope: tag definitions 0991D500 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Spies Dead 1 (03D734F0)](#trigger-03d734f0).
2. Disable [Spies Dead 4d (0991D6A0)](#trigger-0991d6a0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6171, Events line 6301, Actions line 6431.

<a id="trigger-0875a270"></a>

### 71. Starting Forces - 0875A270

Owner reference: Reinforcements. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03D79890 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Reinforcements 1 (08533A2C)](all05s-teams.md#team-08533a2c).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6172, Events line 6302, Actions line 6432.

<a id="trigger-06c8dad0"></a>

### 72. Change Tanya House - 06C8DAD0

Owner reference: Reinforcements. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Mission Start 2 (07EFD7A0)](#trigger-07efd7a0).

Attached scope: tag definitions 06C88870 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Tanya (1) (07F21C10)](all05s-teams.md#team-07f21c10).
2. Enable and reset applicable timers for [Change Tanya House 2 (07EBB590)](#trigger-07ebb590).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6173, Events line 6303, Actions line 6433.

<a id="trigger-07ebb590"></a>

### 73. Change Tanya House 2 - 07EBB590

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change Tanya House (06C8DAD0)](#trigger-06c8dad0).

Attached scope: tag definitions 07EBC510 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Tanya (2) (08AB2210)](all05s-teams.md#team-08ab2210).
2. Enable and reset applicable timers for [Enable Tanya Dies (080906B0)](#trigger-080906b0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6174, Events line 6304, Actions line 6434.

<a id="trigger-080906b0"></a>

### 74. Enable Tanya Dies - 080906B0

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change Tanya House 2 (07EBB590)](#trigger-07ebb590).

Attached scope: tag definitions 08091E50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Tanya Dies (08836B30)](#trigger-08836b30).
2. Enable and reset applicable timers for [Unally (07E3A0D0)](#trigger-07e3a0d0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6175, Events line 6305, Actions line 6435.

<a id="trigger-07e3a0d0"></a>

### 75. Unally - 07E3A0D0

Owner reference: Tanya. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Tanya Dies (080906B0)](#trigger-080906b0).

Attached scope: tag definitions 07E39850 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 18 (country/type YELLOWTEAM; placed owner YellowTeam House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6176, Events line 6306, Actions line 6436.

<a id="trigger-08a40330"></a>

### 76. Mission Start 1 - 08A40330

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A42E50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Move the camera to waypoint 98 (cell 123, 152) with speed setting 3.
2. Enable and reset applicable timers for [Mission Start 2 (07EFD7A0)](#trigger-07efd7a0).
3. Reveal terrain around waypoint 98 (cell 123, 152).
4. Disable player input.
5. Reveal terrain around waypoint 97 (cell 119, 148).
6. Reveal terrain around waypoint 100 (cell 125, 154).
7. Display message “Somewhere in Poland...” (MISSION:All05r).
8. Enable and reset applicable timers for [Mission Start 3 (08A3F1B0)](#trigger-08a3f1b0).
9. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6177, Events line 6307, Actions line 6437.

<a id="trigger-07efd7a0"></a>

### 77. Mission Start 2 - 07EFD7A0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Mission Start 1 (08A40330)](#trigger-08a40330).

Attached scope: tag definitions 07EFD0C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Particle Anim at; main setting 2.
2. Enable and reset applicable timers for [Change Tanya House (06C8DAD0)](#trigger-06c8dad0).
3. Reveal terrain around waypoint 12 (cell 112, 140).
4. Play sound Flare.
5. Display message “Signal Flare Detected” (MISSION:All05s).
6. Play sound MessageText.
7. Enable and reset applicable timers for [Create Seals (0B9ECBBC)](#trigger-0b9ecbbc).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6178, Events line 6308, Actions line 6438.

<a id="trigger-08a3f1b0"></a>

### 78. Mission Start 3 - 08A3F1B0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Mission Start 1 (08A40330)](#trigger-08a40330).

Attached scope: tag definitions 08A40080 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 99 (cell 113, 142) with speed setting 2.
2. Play sound TanyaCreated.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6179, Events line 6309, Actions line 6439.

<a id="trigger-0b9ecbbc"></a>

### 79. Create Seals - 0B9ECBBC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Mission Start 2 (07EFD7A0)](#trigger-07efd7a0).

Attached scope: tag definitions 0B9EC87C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Elite GI's (0F1097DC)](all05s-teams.md#team-0f1097dc) at waypoint 7 (cell 110, 141).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6180, Events line 6310, Actions line 6440.

<a id="trigger-08a40730"></a>

### 80. Cow 1 - 08A40730

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Barrels (CAMISC01), owner RedTeam House, cell (92, 122), tag 08A45610, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Cow 1b (08A45080)](#trigger-08a45080).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6181, Events line 6311, Actions line 6441.

<a id="trigger-08a45080"></a>

### 81. Cow 1b - 08A45080

Owner reference: Rebels. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Cow 1 (08A40730)](#trigger-08a40730); enable from [Cow 1c (04353B3C)](#trigger-04353b3c).

Attached scope: Cow (COW), owner Civilians House, cell (94, 119), tag 08A5DE50, persistence mode 0; Cow (COW), owner Civilians House, cell (93, 120), tag 08A5DE50, persistence mode 0; Cow (COW), owner Civilians House, cell (92, 120), tag 08A5DE50, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 20 (country/type REBELS; placed owner Rebels House).
2. Play sound CowFear.
3. Create radar-event marker type 0 at waypoint 21 (cell 93, 119).
4. Display message “Bovine rescued” (MISSION:All05j).
5. Play sound MessageText.
6. Enable and reset applicable timers for [Cow 1c (0838ED2C)](#trigger-0838ed2c).
7. Create/recruit team [Cows1 (0E584EFC)](all05s-teams.md#team-0e584efc).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6182, Events line 6312, Actions line 6442.

<a id="trigger-0838ed2c"></a>

### 82. Cow 1c - 0838ED2C

Owner reference: Rebels. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Cow 1b (08A45080)](#trigger-08a45080).

Attached scope: tag definitions 0838E73C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash team [Cows1 (0E584EFC)](all05s-teams.md#team-0e584efc) with duration setting 90.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6183, Events line 6313, Actions line 6443.

<a id="trigger-07db9e80"></a>

### 83. Start Red Patrols - 07DB9E80

Owner reference: Engineers. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07DBB7F0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 15 (country/type ENGINEERS; placed owner Engineers House).
2. Production Begins: owner selector 15 (country/type ENGINEERS; placed owner Engineers House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6184, Events line 6314, Actions line 6444.

<a id="trigger-08a70ce0"></a>

### 84. Red Patrol 3 - 08A70CE0

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A709C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Red Patrol 3 (03D48870)](all05s-teams.md#team-03d48870) at waypoint 30 (cell 87, 72).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6185, Events line 6315, Actions line 6445.

<a id="trigger-08a70900"></a>

### 85. Red Patrol 4 - 08A70900

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A703A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Red Patrol 4 (03D4B940)](all05s-teams.md#team-03d4b940) at waypoint 26 (cell 105, 92).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6186, Events line 6316, Actions line 6446.

<a id="trigger-08a702e0"></a>

### 86. Red Patrol 5 - 08A702E0

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A70160 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Red Patrol 5 (08AF15E0)](all05s-teams.md#team-08af15e0) at waypoint 23 (cell 95, 106).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6187, Events line 6317, Actions line 6447.

<a id="trigger-06f51870"></a>

### 87. Rebels 1b - 06F51870

Owner reference: Mr. Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: GI (E1), owner Civilians House, cell (151, 124), tag 06F51730, persistence mode 0; GI (E1), owner Civilians House, cell (150, 125), tag 06F51730, persistence mode 0; GI (E1), owner Civilians House, cell (150, 126), tag 06F51730, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “Allied patrol discovered” (MISSION:All05g).
3. Create radar-event marker type 1 at waypoint 37 (cell 152, 125).
4. Reveal terrain around waypoint 37 (cell 152, 125).
5. Change House: owner selector 22 (country/type PLAYER; placed owner Player House).
6. Play voice notification Mis_A5_AllSoldier2.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6188, Events line 6318, Actions line 6448.

<a id="trigger-06ff94d0"></a>

### 88. Red Patrol 6 - 06FF94D0

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06FF91B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Red Patrol 7 (0A55580C)](all05s-teams.md#team-0a55580c) at waypoint 38 (cell 109, 113).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6189, Events line 6319, Actions line 6449.

<a id="trigger-06fb7f60"></a>

### 89. Red Patrol 7 - 06FB7F60

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06FB75E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Red Patrol 8 (0A55D54C)](all05s-teams.md#team-0a55d54c) at waypoint 23 (cell 95, 106).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6190, Events line 6320, Actions line 6450.

<a id="trigger-07c56120"></a>

### 90. Rebels 2b - 07C56120

Owner reference: Rebels. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: GI (E1), owner Civilians House, cell (128, 121), tag 07C43260, persistence mode 0; GI (E1), owner Civilians House, cell (126, 120), tag 07C43260, persistence mode 0; GI (E1), owner Civilians House, cell (129, 121), tag 07C43260, persistence mode 0; Engineer (ENGINEER), owner Civilians House, cell (124, 119), tag 07C43260, persistence mode 0; Engineer (ENGINEER), owner Civilians House, cell (128, 120), tag 07C43260, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Create radar-event marker type 1 at waypoint 43 (cell 55, 84).
3. Display message “Allied patrol discovered” (MISSION:All05g).
4. Reveal terrain around waypoint 44 (cell 126, 117).
5. Play voice notification Mis_A5_AllSoldier1.
6. Change House: owner selector 22 (country/type PLAYER; placed owner Player House).
7. Particle Anim at; main setting 2; location/duration field AS.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6191, Events line 6321, Actions line 6451.

<a id="trigger-07d21d60"></a>

### 91. Change Hospital Owner - 07D21D60

Owner reference: Civilians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07D267E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 20 (country/type REBELS; placed owner Rebels House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6192, Events line 6322, Actions line 6452.

<a id="trigger-07d0b360"></a>

### 92. Hint: Spies - 07D0B360

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07D361B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 48 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “HINT: SPIES can disguise themselves as ENEMY TROOPS” (MISSION:All05c).
2. Play sound MessageText.
3. Enable and reset applicable timers for [Hint: Spies 2 (07D15520)](#trigger-07d15520).
4. Remove instances of the team organization (not automatically its surviving objects) [Spies (088BE7DC)](all05s-teams.md#team-088be7dc).
5. Create/recruit team [Hint: Spies (0A7CFDBC)](all05s-teams.md#team-0a7cfdbc).
6. Create/recruit team [Hint: Spies (0A7CFDBC)](all05s-teams.md#team-0a7cfdbc).
7. Create/recruit team [Hint: Spies (0A7CFDBC)](all05s-teams.md#team-0a7cfdbc).
8. Flash team [Hint: Spies (0A7CFDBC)](all05s-teams.md#team-0a7cfdbc) with duration setting 70.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6193, Events line 6323, Actions line 6453.

<a id="trigger-07d15520"></a>

### 93. Hint: Spies 2 - 07D15520

Owner reference: RedTeam. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: Spies (07D0B360)](#trigger-07d0b360).

Attached scope: tag definitions 07D15190 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “HINT: To disguise a SPY, select him and left click on an ENEMY SOLDIER” (MISSION:All05d).
2. Play sound MessageText.
3. Create/recruit team [Flash Conscript (0BECEC1C)](all05s-teams.md#team-0becec1c).
4. Create/recruit team [Flash Conscript (0BECEC1C)](all05s-teams.md#team-0becec1c).
5. Create/recruit team [Flash Conscript (0BECEC1C)](all05s-teams.md#team-0becec1c).
6. Create/recruit team [Flash Conscript (0BECEC1C)](all05s-teams.md#team-0becec1c).
7. Create/recruit team [Flash Conscript (0BECEC1C)](all05s-teams.md#team-0becec1c).
8. Create/recruit team [Flash Conscript (0BECEC1C)](all05s-teams.md#team-0becec1c).
9. Create/recruit team [Flash Conscript (0BECEC1C)](all05s-teams.md#team-0becec1c).
10. Create/recruit team [Flash Conscript (0BECEC1C)](all05s-teams.md#team-0becec1c).
11. Flash team [Flash Conscript (0BECEC1C)](all05s-teams.md#team-0becec1c) with duration setting 70.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6194, Events line 6324, Actions line 6454.

<a id="trigger-09f99e80"></a>

### 94. Tesla Coil Spotted 3 - 09F99E80

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner RedTeam House, cell (107, 92), tag 09F99A20, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 61 (cell 107, 92).
3. Create radar-event marker type 5 at waypoint 61 (cell 107, 92).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6195, Events line 6325, Actions line 6455.

<a id="trigger-09f99960"></a>

### 95. Tesla Coil Spotted 4 - 09F99960

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner RedTeam House, cell (94, 92), tag 09F997D0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 62 (cell 94, 92).
3. Create radar-event marker type 5 at waypoint 62 (cell 94, 92).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6196, Events line 6326, Actions line 6456.

<a id="trigger-0b656d30"></a>

### 96. Tesla Coil Spotted 5 - 0B656D30

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner RedTeam House, cell (97, 78), tag 0B6568A0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 63 (cell 97, 78).
3. Create radar-event marker type 5 at waypoint 63 (cell 97, 78).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6197, Events line 6327, Actions line 6457.

<a id="trigger-0b6567e0"></a>

### 97. Tesla Coil Spotted 6 - 0B6567E0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner RedTeam House, cell (104, 78), tag 0B656650, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 64 (cell 104, 78).
3. Create radar-event marker type 5 at waypoint 64 (cell 104, 78).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6198, Events line 6328, Actions line 6458.

<a id="trigger-0b656590"></a>

### 98. Tesla Coil Spotted 7 - 0B656590

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner YellowTeam House, cell (73, 40), tag 0B656400, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 65 (cell 73, 40).
3. Create radar-event marker type 5 at waypoint 65 (cell 73, 40).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6199, Events line 6329, Actions line 6459.

<a id="trigger-0b655330"></a>

### 99. Tesla Coil Spotted 8 - 0B655330

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner YellowTeam House, cell (58, 39), tag 0B6551A0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 66 (cell 58, 39).
3. Create radar-event marker type 5 at waypoint 66 (cell 58, 39).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6200, Events line 6330, Actions line 6460.

<a id="trigger-0b6550e0"></a>

### 100. Tesla Coil Spotted 9 - 0B6550E0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner YellowTeam House, cell (62, 30), tag 0B652EF0, persistence mode 0; Tesla Coil (TESLA), owner YellowTeam House, cell (66, 30), tag 0B652EF0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 67 (cell 64, 30).
3. Create radar-event marker type 5 at waypoint 67 (cell 64, 30).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6201, Events line 6331, Actions line 6461.

<a id="trigger-0b652e30"></a>

### 101. Tesla Coil Spotted 10 - 0B652E30

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner OrangeTeam House, cell (44, 61), tag 0B652CA0, persistence mode 0; Tesla Coil (TESLA), owner OrangeTeam House, cell (44, 65), tag 0B652CA0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 68 (cell 44, 63).
3. Create radar-event marker type 5 at waypoint 68 (cell 44, 63).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6202, Events line 6332, Actions line 6462.

<a id="trigger-0b652be0"></a>

### 102. Tesla Coil Spotted 11 - 0B652BE0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner OrangeTeam House, cell (49, 64), tag 0B652A50, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 69 (cell 49, 64).
3. Create radar-event marker type 5 at waypoint 69 (cell 49, 64).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6203, Events line 6333, Actions line 6463.

<a id="trigger-0b652990"></a>

### 103. Tesla Coil Spotted 12 - 0B652990

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner OrangeTeam House, cell (31, 45), tag 0B652800, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 70 (cell 37, 45).
3. Create radar-event marker type 5 at waypoint 70 (cell 37, 45).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6204, Events line 6334, Actions line 6464.

<a id="trigger-0b652740"></a>

### 104. Tesla Coil Spotted 13 - 0B652740

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Coil (TESLA), owner OrangeTeam House, cell (37, 45), tag 0B6525B0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 71 (cell 31, 45).
3. Create radar-event marker type 5 at waypoint 71 (cell 31, 45).
4. Display message “Tesla Coil detected - CAUTION: EXTREME DANGER” (MISSION:All05e).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6205, Events line 6335, Actions line 6465.

<a id="trigger-09f99710"></a>

### 105. Nuke 2 Entered - 09F99710

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [Objective 2c (09C20090)](#trigger-09c20090).
2. Set local flag 6 (Nuke 2 Captured).
3. All to Hunt: owner selector 19 (country/type ORANGETEAM; placed owner OrangeTeam House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6206, Events line 6336, Actions line 6466.

<a id="trigger-09f993a0"></a>

### 106. Nuke 2 Destroyed - 09F993A0

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke 2 Entered (09F99710)](#trigger-09f99710).

Attached scope: Nuclear Missile Silo (NAMISL), owner OrangeTeam House, cell (56, 63), tag 09F99460, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Objective 2c (09C20090)](#trigger-09c20090).
2. Set local flag 1 (Nuke 2 Complete).
3. All to Hunt: owner selector 19 (country/type ORANGETEAM; placed owner OrangeTeam House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6207, Events line 6337, Actions line 6467.

<a id="trigger-09f9e650"></a>

### 107. Victory 1 - 09F9E650

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 1 (Nuke 2 Complete) is set.
2. local flag 0 (Nuke1Complete) is set.

Flag writers in this mission: set local flag 1 (Nuke 2 Complete) at [Nuke 2 Destroyed (09F993A0)](#trigger-09f993a0); set local flag 0 (Nuke1Complete) at [Nuke 1 Destroyed (07914350)](#trigger-07914350). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Victory 2 (09F98660)](#trigger-09f98660).
2. Play voice notification EVA_PrimaryObjectiveAchieved.
3. Disable [Objective 2 (098CEB70)](#trigger-098ceb70).
4. Disable [Objective 2b (09C205E0)](#trigger-09c205e0).
5. Disable [Objective 2c (09C20090)](#trigger-09c20090).
6. Enable and reset applicable timers for [Cheer (0A30A8FC)](#trigger-0a30a8fc).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6208, Events line 6338, Actions line 6468.

<a id="trigger-09f98660"></a>

### 108. Victory 2 - 09F98660

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Victory 1 (09F9E650)](#trigger-09f9e650); enable from [Victory 1b (0799FF3C)](#trigger-0799ff3c); enable from [Victory 1c (0799FC0C)](#trigger-0799fc0c); enable from [Victory 1d (0799F8DC)](#trigger-0799f8dc).

Attached scope: tag definitions 09F984D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 22 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6209, Events line 6339, Actions line 6469.

<a id="trigger-0a30a8fc"></a>

### 109. Cheer - 0A30A8FC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Victory 1 (09F9E650)](#trigger-09f9e650); enable from [Victory 1b (0799FF3C)](#trigger-0799ff3c); enable from [Victory 1c (0799FC0C)](#trigger-0799fc0c); enable from [Victory 1d (0799F8DC)](#trigger-0799f8dc).

Attached scope: tag definitions 0A30A2DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 22 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6210, Events line 6340, Actions line 6470.

<a id="trigger-09f98a50"></a>

### 110. Victory 0 - 09F98A50

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 0 (Nuke1Complete) is set.

Flag writers in this mission: set local flag 0 (Nuke1Complete) at [Nuke 1 Destroyed (07914350)](#trigger-07914350). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_A5_EvaMissileDestroyed.
2. Play sound MessageText.
3. Display message “First Nuclear Missile Silo destroyed - one remaining” (MISSION:All05m).
4. Create radar-event marker type 1 at waypoint 9 (cell 66, 41).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6211, Events line 6341, Actions line 6471.

<a id="trigger-09f98800"></a>

### 111. Victory 0b - 09F98800

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Victory 0 (09F98A50)](#trigger-09f98a50).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 1 (Nuke 2 Complete) is set.

Flag writers in this mission: set local flag 1 (Nuke 2 Complete) at [Nuke 2 Destroyed (09F993A0)](#trigger-09f993a0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_A5_EvaMissileDestroyed.
2. Display message “First Nuclear Missile Silo destroyed - one remaining” (MISSION:All05m).
3. Play sound MessageText.
4. Create radar-event marker type 1 at waypoint 74 (cell 59, 66).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6212, Events line 6342, Actions line 6472.

<a id="trigger-08802960"></a>

### 112. Prisoners 1b - 08802960

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prisoners 1 (087E1F20)](#trigger-087e1f20); enable from [Prisoners 1c (0A4D262C)](#trigger-0a4d262c).

Attached scope: Grizzly Battle Tank (MTNK), owner Civilians House, cell (44, 83), tag 08800E10, persistence mode 0; GI (E1), owner Civilians House, cell (43, 82), tag 08800E10, persistence mode 0; GI (E1), owner Civilians House, cell (43, 83), tag 08800E10, persistence mode 0; GI (E1), owner Civilians House, cell (45, 83), tag 08800E10, persistence mode 0; GI (E1), owner Civilians House, cell (45, 84), tag 08800E10, persistence mode 0.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 22 (country/type PLAYER; placed owner Player House).
2. Play sound MessageText.
3. Create radar-event marker type 1 at waypoint 72 (cell 44, 83).
4. Display message “Allied patrol discovered” (MISSION:All05g).
5. Play voice notification Mis_A5_AllSoldier3.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6213, Events line 6343, Actions line 6473.

<a id="trigger-087e1f20"></a>

### 113. Prisoners 1 - 087E1F20

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Barrels (CAMISC01), owner OrangeTeam House, cell (45, 86), tag 087E1670, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Prisoners 1b (08802960)](#trigger-08802960).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6214, Events line 6344, Actions line 6474.

<a id="trigger-0806a03c"></a>

### 114. Create Crate - 0806A03C

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0807204C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create crate type 10 at waypoint 41 (cell 126, 165).
2. Create crate type 9 at waypoint 42 (cell 66, 98).
3. Create crate type 2 at waypoint 43 (cell 55, 84).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6215, Events line 6345, Actions line 6475.

<a id="trigger-07bc6e5c"></a>

### 115. Start Ambient Sounds - 07BC6E5C

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07BC4D5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 99 (cell 113, 142).
2. Play sound _Amb_CricketBed at waypoint 12 (cell 112, 140).
3. Play sound _Amb_BirdsTemperate2 at waypoint 4 (cell 120, 133).
4. Play sound _Amb_WindCold at waypoint 6 (cell 109, 128).
5. Play sound _Amb_WindCold at waypoint 37 (cell 152, 125).
6. Play sound _Amb_WindPlains at waypoint 39 (cell 95, 113).
7. Play sound _Amb_CricketBed at waypoint 36 (cell 76, 114).
8. Play sound _Amb_CricketChirps at waypoint 42 (cell 66, 98).
9. Play sound _Amb_WindCold at waypoint 31 (cell 87, 77).
10. Play sound _Amb_WindPlains at waypoint 35 (cell 101, 72).
11. Play sound _Amb_CricketBed at waypoint 57 (cell 79, 59).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6216, Events line 6346, Actions line 6476.

<a id="trigger-0a19c0cc"></a>

### 116. BattleLab Entered - 0A19C0CC

Owner reference: Tanya. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BattleLab Destroyed (07476A30)](#trigger-07476a30).

Attached scope: Soviet Battle Lab (NATECH), owner RedTeam House, cell (100, 94), tag 06B416F0, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 14 (country/type SPIES; placed owner Spies House).

**Then perform these actions in order:**

1. Play in-game movie 84.
2. Enable and reset applicable timers for [BattleLab Entered 2 (06B41DA0)](#trigger-06b41da0).
3. Disable [Objective 1 (074734A0)](#trigger-074734a0).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6217, Events line 6347, Actions line 6477.

<a id="trigger-09e7015c"></a>

### 117. No Power Plants - 09E7015C

Owner reference: RedTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Nuclear Reactor (NANRCT), owner RedTeam House, cell (143, 97), tag 09E7864C, persistence mode 0.

**Wait for the recorded events:**

1. Building does not exist: type index 9 (global list position: Tesla Reactor (NAPOWR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 23 (country/type MR. NEUTRAL; placed owner Mr. Neutral House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6218, Events line 6348, Actions line 6478.

<a id="trigger-0824769c"></a>

### 118. No Power Plants 2 - 0824769C

Owner reference: OrangeTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Nuclear Reactor (NANRCT), owner OrangeTeam House, cell (138, 92), tag 082434BC, persistence mode 0.

**Wait for the recorded events:**

1. Building does not exist: type index 9 (global list position: Tesla Reactor (NAPOWR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 23 (country/type MR. NEUTRAL; placed owner Mr. Neutral House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6219, Events line 6349, Actions line 6479.

<a id="trigger-08240c2c"></a>

### 119. No Power Plants 3 - 08240C2C

Owner reference: YellowTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Nuclear Reactor (NANRCT), owner YellowTeam House, cell (133, 87), tag 08240A2C, persistence mode 0.

**Wait for the recorded events:**

1. Building does not exist: type index 9 (global list position: Tesla Reactor (NAPOWR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 23 (country/type MR. NEUTRAL; placed owner Mr. Neutral House).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6220, Events line 6350, Actions line 6480.

<a id="trigger-0799ddbc"></a>

### 120. Victory 0c - 0799DDBC

Owner reference: YellowTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Victory 0b (09F98800)](#trigger-09f98800).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 5 (Nuke1Captured) is set.

Flag writers in this mission: set local flag 5 (Nuke1Captured) at [Nuke 1 Entered (078F7090)](#trigger-078f7090). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “First Nuclear Missile Silo has been captured - one remaining” (MISSION:All05n).
3. Play voice notification Mis_A5_EvaMissileCaptured.
4. Create radar-event marker type 1 at waypoint 9 (cell 66, 41).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6221, Events line 6351, Actions line 6481.

<a id="trigger-0799d38c"></a>

### 121. Victory 0d - 0799D38C

Owner reference: OrangeTeam. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Victory 0c (0799DDBC)](#trigger-0799ddbc).

Attached scope: tag definitions 09F988C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Nuke 2 Captured) is set.

Flag writers in this mission: set local flag 6 (Nuke 2 Captured) at [Nuke 2 Entered (09F99710)](#trigger-09f99710). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “First Nuclear Missile Silo has been captured - one remaining” (MISSION:All05n).
3. Play voice notification Mis_A5_EvaMissileCaptured.
4. Create radar-event marker type 1 at waypoint 74 (cell 59, 66).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6222, Events line 6352, Actions line 6482.

<a id="trigger-0799ff3c"></a>

### 122. Victory 1b - 0799FF3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Victory 1 (09F9E650)](#trigger-09f9e650).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 6 (Nuke 2 Captured) is set.
2. local flag 5 (Nuke1Captured) is set.

Flag writers in this mission: set local flag 6 (Nuke 2 Captured) at [Nuke 2 Entered (09F99710)](#trigger-09f99710); set local flag 5 (Nuke1Captured) at [Nuke 1 Entered (078F7090)](#trigger-078f7090). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification EVA_PrimaryObjectiveAchieved.
2. Enable and reset applicable timers for [Victory 2 (09F98660)](#trigger-09f98660).
3. Disable [Objective 2 (098CEB70)](#trigger-098ceb70).
4. Disable [Objective 2b (09C205E0)](#trigger-09c205e0).
5. Disable [Objective 2c (09C20090)](#trigger-09c20090).
6. Enable and reset applicable timers for [Cheer (0A30A8FC)](#trigger-0a30a8fc).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6223, Events line 6353, Actions line 6483.

<a id="trigger-0799fc0c"></a>

### 123. Victory 1c - 0799FC0C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Victory 1b (0799FF3C)](#trigger-0799ff3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 6 (Nuke 2 Captured) is set.
2. local flag 0 (Nuke1Complete) is set.

Flag writers in this mission: set local flag 6 (Nuke 2 Captured) at [Nuke 2 Entered (09F99710)](#trigger-09f99710); set local flag 0 (Nuke1Complete) at [Nuke 1 Destroyed (07914350)](#trigger-07914350). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification EVA_PrimaryObjectiveAchieved.
2. Enable and reset applicable timers for [Victory 2 (09F98660)](#trigger-09f98660).
3. Disable [Objective 2 (098CEB70)](#trigger-098ceb70).
4. Disable [Objective 2b (09C205E0)](#trigger-09c205e0).
5. Disable [Objective 2c (09C20090)](#trigger-09c20090).
6. Enable and reset applicable timers for [Cheer (0A30A8FC)](#trigger-0a30a8fc).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6224, Events line 6354, Actions line 6484.

<a id="trigger-0799f8dc"></a>

### 124. Victory 1d - 0799F8DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Victory 1c (0799FC0C)](#trigger-0799fc0c).

Attached scope: tag definitions 09F98B10 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Nuke 2 Complete) is set.
2. local flag 5 (Nuke1Captured) is set.

Flag writers in this mission: set local flag 1 (Nuke 2 Complete) at [Nuke 2 Destroyed (09F993A0)](#trigger-09f993a0); set local flag 5 (Nuke1Captured) at [Nuke 1 Entered (078F7090)](#trigger-078f7090). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification EVA_PrimaryObjectiveAchieved.
2. Enable and reset applicable timers for [Victory 2 (09F98660)](#trigger-09f98660).
3. Disable [Objective 2 (098CEB70)](#trigger-098ceb70).
4. Disable [Objective 2b (09C205E0)](#trigger-09c205e0).
5. Disable [Objective 2c (09C20090)](#trigger-09c20090).
6. Enable and reset applicable timers for [Cheer (0A30A8FC)](#trigger-0a30a8fc).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6225, Events line 6355, Actions line 6485.

<a id="trigger-07a2c03c"></a>

### 125. Hint: Seals - 07A2C03C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0825149C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “HINT: Seals can SWIM and PLANT C4 like Tanya” (MISSION:All01l).
2. Play sound MessageText.

Source locator: MAPS01.MIX/all05s.map; Triggers line 6226, Events line 6356, Actions line 6486.

<a id="trigger-0ac5382c"></a>

### 126. Start Ambient Sounds 2 - 0AC5382C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AC52D0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WindPlains at waypoint 59 (cell 84, 64).
2. Play sound _Amb_BirdsNightOwl at waypoint 58 (cell 79, 64).
3. Play sound _Amb_CricketBed at waypoint 37 (cell 152, 125).
4. Play sound _Amb_WindCold at waypoint 67 (cell 64, 30).
5. Play sound _Amb_WindPlains at waypoint 48 (cell 62, 44).
6. Play sound _Amb_BirdsMorning at waypoint 75 (cell 59, 61).
7. Play sound _Amb_WindCold at waypoint 70 (cell 37, 45).
8. Play sound _Amb_WindPlains at waypoint 89 (cell 38, 61).
9. Play sound _Amb_BirdsNightOwl at waypoint 94 (cell 24, 59).
10. Play sound _Amb_CricketBed at waypoint 86 (cell 41, 80).
11. Play sound _Amb_BirdsMorning at waypoint 43 (cell 55, 84).
12. Play sound _Amb_WindCold at waypoint 69 (cell 49, 64).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6227, Events line 6357, Actions line 6487.

<a id="trigger-0a4d262c"></a>

### 127. Prisoners 1c - 0A4D262C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 16 tagged map cells: (42, 81), (43, 81), (44, 81), (45, 81), (46, 81), (42, 82), (46, 82), (42, 83), (46, 83), (42, 84), (46, 84), (42, 85), (43, 85), (44, 85), (45, 85), (46, 85); tag 0A4D3DAC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector -1 (unresolved or special selector).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Prisoners 1b (08802960)](#trigger-08802960).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6228, Events line 6358, Actions line 6488.

<a id="trigger-04353b3c"></a>

### 128. Cow 1c - 04353B3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 14 tagged map cells: (91, 118), (92, 118), (93, 118), (94, 118), (95, 118), (91, 119), (95, 119), (91, 120), (95, 120), (91, 121), (92, 121), (93, 121), (94, 121), (95, 121); tag 0435396C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector -1 (unresolved or special selector).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Cow 1b (08A45080)](#trigger-08a45080).

Source locator: MAPS01.MIX/all05s.map; Triggers line 6229, Events line 6359, Actions line 6489.

[All team rosters and ordered plans](all05s-teams.md) | [All mission overrides](all05s-overrides.md)
