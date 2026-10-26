# Operation: Chrono Storm

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for all12s.map.](../../images/map-all12s.svg)

*Initial placement schematic for all12s.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** all12s.map. **Effective extracted member:** MAPS01.MIX/all12s.map. **Trigger definitions:** 61.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all12s-teams.md) | [All mission overrides](all12s-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | SNOW |
| Map size | 0,0,70,96 |
| Visible local rectangle | 2,9,66,81 |
| Placed vehicles | 41 |
| Placed infantry | 38 |
| Placed structures | 268 |
| Placed aircraft | 0 |
| Team templates | 37 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 120 | Player |
| 1 | BadGuy1 House | 1500 | BadGuy1 |
| 2 | BadGuy2 House | 300 | BadGuy2 |
| 3 | BadGuy3 House | 300 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 0 | Other1 |
| 6 | Other2 House | 0 | Other2 |
| 7 | Other3 House | 500 | Other3 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Play Final Movie,0 |
| 1 | MammothDead1,0 |
| 2 | MammothDead2,0 |
| 3 | MammothDead3,0 |
| 4 | MammothDead4,0 |
| 5 | TanyaLaugh,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Mission Failed (0798A3B0)](#trigger-0798a3b0) | 2 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [Mission Victory (09726B10)](#trigger-09726b10) | 3 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-0798a3b0"></a>

### 1. Mission Failed - 0798A3B0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin is Destroyed 2 (0A92464C)](#trigger-0a92464c); enable from [Player Dead (0A65881C)](#trigger-0a65881c).

Attached scope: tag definitions 0798A1E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4531, Events line 4594, Actions line 4657.

<a id="trigger-09726b10"></a>

### 2. Mission Victory - 09726B10

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tanya enters Kremlin (07F38664)](#trigger-07f38664); enable from [Failsafe End Mission (0886803C)](#trigger-0886803c); enable from [Kremlin Secured 4b (0A40787C)](#trigger-0a40787c); enable from [Kremlin Secured 6 (0A0C79EC)](#trigger-0a0c79ec).

Attached scope: tag definitions 09726940 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4532, Events line 4595, Actions line 4658.

<a id="trigger-078c35f0"></a>

### 3. ParaSEALS - 078C35F0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078C3120 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [aaaParaSEALS (0ABE46AC)](all12s-teams.md#team-0abe46ac) at waypoint 3 (cell 63, 61).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4533, Events line 4596, Actions line 4659.

<a id="trigger-0798af40"></a>

### 4. Reveal Starting area - 0798AF40

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0798AAA0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 3 (cell 63, 61).
2. Reveal terrain around waypoint 6 (cell 55, 61).
3. Reveal terrain around waypoint 7 (cell 62, 54).
4. Reveal terrain around waypoint 8 (cell 55, 67).
5. Reveal terrain around waypoint 9 (cell 68, 54).
6. Reveal terrain around waypoint 10 (cell 64, 62).
7. Reveal terrain around waypoint 99 (cell 62, 61).
8. Reveal terrain around waypoint 1 (cell 62, 71).
9. Reveal terrain around waypoint 2 (cell 72, 61).
10. Reveal terrain around waypoint 11 (cell 71, 70).
11. Reveal terrain around waypoint 52 (cell 54, 53).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4534, Events line 4597, Actions line 4660.

<a id="trigger-08e4d220"></a>

### 5. Prepare to Chrono - 08E4D220

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Generators Destroyed 2 (0861E7EC)](#trigger-0861e7ec).

Attached scope: tag definitions 08E5E190 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_A12_EvaCountdown.
2. Enable and reset applicable timers for [Chrono 1 (08E800F0)](#trigger-08e800f0).
3. Enable and reset applicable timers for [Chrono 2 (08DAF030)](#trigger-08daf030).
4. Enable and reset applicable timers for [Prepare to Chrono 2 (0861A71C)](#trigger-0861a71c).
5. Enable and reset applicable timers for [Prepare to Chrono 3 (0861A29C)](#trigger-0861a29c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4535, Events line 4598, Actions line 4661.

<a id="trigger-08e800f0"></a>

### 6. Chrono 1 - 08E800F0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prepare to Chrono (08E4D220)](#trigger-08e4d220).

Attached scope: tag definitions 0859404C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono MCV (08E71100)](all12s-teams.md#team-08e71100) at waypoint 10 (cell 64, 62).
2. Enable and reset applicable timers for [Begin Prod: Bad Guy 1 (09087AE4)](#trigger-09087ae4).
3. Enable and reset applicable timers for 0 (not a defined local trigger).
4. Enable and reset applicable timers for [Chrono 1b (0AE8DA4C)](#trigger-0ae8da4c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4536, Events line 4599, Actions line 4662.

<a id="trigger-08daf030"></a>

### 7. Chrono 2 - 08DAF030

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prepare to Chrono (08E4D220)](#trigger-08e4d220).

Attached scope: tag definitions 09131050 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 14 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 1 (cell 62, 71).
2. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 2 (cell 72, 61).
3. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 14 (cell 64, 71).
4. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 12 (cell 62, 69).
5. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 13 (cell 64, 69).
6. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 17 (cell 70, 61).
7. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 15 (cell 72, 63).
8. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 16 (cell 70, 63).
9. Create radar-event marker type 2 at waypoint 18 (cell 64, 72).
10. Create radar-event marker type 2 at waypoint 19 (cell 72, 64).
11. Enable and reset applicable timers for [Chrono 2b (0AE8D60C)](#trigger-0ae8d60c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4537, Events line 4600, Actions line 4663.

<a id="trigger-0861a71c"></a>

### 8. Prepare to Chrono 2 - 0861A71C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prepare to Chrono (08E4D220)](#trigger-08e4d220).

Attached scope: tag definitions 0861A38C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_A12_EvaCountdown.
2. Enable and reset applicable timers for [Chrono 3 (0861DA8C)](#trigger-0861da8c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4538, Events line 4601, Actions line 4664.

<a id="trigger-0861a29c"></a>

### 9. Prepare to Chrono 3 - 0861A29C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prepare to Chrono (08E4D220)](#trigger-08e4d220).

Attached scope: tag definitions 0861BF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 500 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_A12_EvaCountdown.
2. Enable and reset applicable timers for [Chrono 4 (0861C7AC)](#trigger-0861c7ac).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4539, Events line 4602, Actions line 4665.

<a id="trigger-09087ae4"></a>

### 10. Begin Prod: Bad Guy 1 - 09087AE4

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono 1 (08E800F0)](#trigger-08e800f0).

Attached scope: tag definitions 09087074 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4540, Events line 4603, Actions line 4666.

<a id="trigger-0ae8da4c"></a>

### 11. Chrono 1b - 0AE8DA4C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono 1 (08E800F0)](#trigger-08e800f0).

Attached scope: tag definitions 0AE8D80C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 253; location/duration field U.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4541, Events line 4604, Actions line 4667.

<a id="trigger-0ae8d60c"></a>

### 12. Chrono 2b - 0AE8D60C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono 2 (08DAF030)](#trigger-08daf030).

Attached scope: tag definitions 0AE939FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 253; location/duration field S.
2. Play Anim At; main setting 253; location/duration field T.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4542, Events line 4605, Actions line 4668.

<a id="trigger-0861da8c"></a>

### 13. Chrono 3 - 0861DA8C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prepare to Chrono 2 (0861A71C)](#trigger-0861a71c).

Attached scope: tag definitions 0861CEAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono 3 (0AA18A4C)](all12s-teams.md#team-0aa18a4c) at waypoint 1 (cell 62, 71).
2. Supply chrono reinforcement team [Chrono 3 (0AA18A4C)](all12s-teams.md#team-0aa18a4c) at waypoint 2 (cell 72, 61).
3. Supply chrono reinforcement team [Chrono 3 (0AA18A4C)](all12s-teams.md#team-0aa18a4c) at waypoint 14 (cell 64, 71).
4. Supply chrono reinforcement team [Chrono 3 (0AA18A4C)](all12s-teams.md#team-0aa18a4c) at waypoint 12 (cell 62, 69).
5. Supply chrono reinforcement team [Chrono 3 (0AA18A4C)](all12s-teams.md#team-0aa18a4c) at waypoint 13 (cell 64, 69).
6. Supply chrono reinforcement team [Chrono 3 (0AA18A4C)](all12s-teams.md#team-0aa18a4c) at waypoint 17 (cell 70, 61).
7. Supply chrono reinforcement team [Chrono 3 (0AA18A4C)](all12s-teams.md#team-0aa18a4c) at waypoint 15 (cell 72, 63).
8. Supply chrono reinforcement team [Chrono 3 (0AA18A4C)](all12s-teams.md#team-0aa18a4c) at waypoint 16 (cell 70, 63).
9. Create radar-event marker type 2 at waypoint 18 (cell 64, 72).
10. Create radar-event marker type 2 at waypoint 19 (cell 72, 64).
11. Enable and reset applicable timers for [Chrono 3b (0861CDBC)](#trigger-0861cdbc).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4543, Events line 4606, Actions line 4669.

<a id="trigger-0861c7ac"></a>

### 14. Chrono 4 - 0861C7AC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prepare to Chrono 3 (0861A29C)](#trigger-0861a29c).

Attached scope: tag definitions 08624BAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 11 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono 2 (09747E70)](all12s-teams.md#team-09747e70) at waypoint 1 (cell 62, 71).
2. Supply chrono reinforcement team [Chrono 2 (09747E70)](all12s-teams.md#team-09747e70) at waypoint 14 (cell 64, 71).
3. Supply chrono reinforcement team [Chrono 2 (09747E70)](all12s-teams.md#team-09747e70) at waypoint 15 (cell 72, 63).
4. Supply chrono reinforcement team [Chrono 2 (09747E70)](all12s-teams.md#team-09747e70) at waypoint 2 (cell 72, 61).
5. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 12 (cell 62, 69).
6. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 13 (cell 64, 69).
7. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 17 (cell 70, 61).
8. Supply chrono reinforcement team [Chrono 4 (0C6B624C)](all12s-teams.md#team-0c6b624c) at waypoint 16 (cell 70, 63).
9. Create radar-event marker type 2 at waypoint 18 (cell 64, 72).
10. Create radar-event marker type 2 at waypoint 19 (cell 72, 64).
11. Enable and reset applicable timers for [Chrono 4b (08624E2C)](#trigger-08624e2c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4544, Events line 4607, Actions line 4670.

<a id="trigger-0861cdbc"></a>

### 15. Chrono 3b - 0861CDBC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono 3 (0861DA8C)](#trigger-0861da8c).

Attached scope: tag definitions 0861CB0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 253; location/duration field S.
2. Play Anim At; main setting 253; location/duration field T.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4545, Events line 4608, Actions line 4671.

<a id="trigger-08624e2c"></a>

### 16. Chrono 4b - 08624E2C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono 4 (0861C7AC)](#trigger-0861c7ac).

Attached scope: tag definitions 0862334C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 253; location/duration field S.
2. Play Anim At; main setting 253; location/duration field T.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4546, Events line 4609, Actions line 4672.

<a id="trigger-0ad699ec"></a>

### 17. Play MCV Movie - 0AD699EC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AD694AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 105.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4547, Events line 4610, Actions line 4673.

<a id="trigger-07e91990"></a>

### 18. Generators Destroyed - 07E91990

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E91820 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 9 (global list position: Tesla Reactor (NAPOWR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Generators Destroyed 2 (0861E7EC)](#trigger-0861e7ec).
2. Play sound PowerOff.
3. Play voice notification EVA_PrimaryObjectiveAchieved.
4. Play sound MessageText.
5. Display message “Objective 1 Accomplished - Chrono Reinforcements can now arrive” (MISSION:All12d).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4548, Events line 4611, Actions line 4674.

<a id="trigger-0861e7ec"></a>

### 19. Generators Destroyed 2 - 0861E7EC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Generators Destroyed (07E91990)](#trigger-07e91990).

Attached scope: tag definitions 0861D94C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 105.
2. Enable and reset applicable timers for [Prepare to Chrono (08E4D220)](#trigger-08e4d220).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4549, Events line 4612, Actions line 4675.

<a id="trigger-096910a0"></a>

### 20. Enable Objective 1 - 096910A0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09692A80 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “Objective 1: Clear the area so Chrono Reinforcements can arrive” (MISSION:All12a).
3. Create radar-event marker type 1 at waypoint 10 (cell 64, 62).
4. Play voice notification EVA_NewObjectiveReceived.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4550, Events line 4613, Actions line 4676.

<a id="trigger-0907a234"></a>

### 21. Enable Objective 2 - 0907A234

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0907B424 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Enable Objective 2b (090739C4)](#trigger-090739c4).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4551, Events line 4614, Actions line 4677.

<a id="trigger-090739c4"></a>

### 22. Enable Objective 2b - 090739C4

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Objective 2 (0907A234)](#trigger-0907a234).

Attached scope: tag definitions 0907D624 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 26 (cell 125, 124).
2. Create radar-event marker type 5 at waypoint 26 (cell 125, 124).
3. Display message “Objective 2: Eliminate Romanov's Elite Black Guard around the Kremlin.” (MISSION:All12b).
4. Play sound MessageText.
5. Enable and reset applicable timers for [Objective 2 (09087CB4)](#trigger-09087cb4).
6. Play voice notification EVA_NewObjectiveReceived.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4552, Events line 4615, Actions line 4678.

<a id="trigger-09087cb4"></a>

### 23. Objective 2 - 09087CB4

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Objective 2b (090739C4)](#trigger-090739c4).

Attached scope: tag definitions 09084DC4 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 26 (cell 125, 124).
2. Display message “Objective 2: Eliminate Romanov's Elite Black Guard around the Kremlin.” (MISSION:All12b).
3. Play sound MessageText.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4553, Events line 4616, Actions line 4679.

<a id="trigger-07f38664"></a>

### 24. Tanya enters Kremlin - 07F38664

Owner reference: Other2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Kremlin (CARUS03), owner Civie1 House, cell (125, 122), tag 07F3F674, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 19 (country/type OTHER2; placed owner Other2 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Mission Victory (09726B10)](#trigger-09726b10).
2. Play sound MessageText.
3. Display message “Objective 2 Accomplished - Romanov has been captured” (MISSION:All12c).
4. Play voice notification EVA_PrimaryObjectiveAchieved.
5. Destroy current instances of [Kremlin is Destroyed (0A92362C)](#trigger-0a92362c).
6. Destroy current instances of [Kremlin is Destroyed 2 (0A92464C)](#trigger-0a92464c).
7. Destroy current instances of [Mission Failed (0798A3B0)](#trigger-0798a3b0).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4554, Events line 4617, Actions line 4680.

<a id="trigger-0a92362c"></a>

### 25. Kremlin is Destroyed - 0A92362C

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A92318C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 160 (global list position: Kremlin (CARUS03)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Kremlin is Destroyed 2 (0A92464C)](#trigger-0a92464c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4555, Events line 4618, Actions line 4681.

<a id="trigger-0a92464c"></a>

### 26. Kremlin is Destroyed 2 - 0A92464C

Owner reference: Civilian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin is Destroyed (0A92362C)](#trigger-0a92362c).

Attached scope: tag definitions 0A92444C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Mission Failed (0798A3B0)](#trigger-0798a3b0).
2. Create radar-event marker type 1 at waypoint 26 (cell 125, 124).
3. Play voice notification EVA_CriticalStrucureLost.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4556, Events line 4619, Actions line 4682.

<a id="trigger-078e54ac"></a>

### 27. Start Ambient Sounds 1 - 078E54AC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078E3DDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 6 (cell 55, 61).
2. Play sound _Amb_WindPlains at waypoint 2 (cell 72, 61).
3. Play sound _Amb_UrbanMurmur1 at waypoint 27 (cell 39, 64).
4. Play sound _Amb_UrbanMurmur2 at waypoint 37 (cell 131, 67).
5. Play sound _Amb_WindCold at waypoint 28 (cell 24, 85).
6. Play sound _Amb_BirdsMorning at waypoint 29 (cell 43, 99).
7. Play sound _Amb_BirdsMorning at waypoint 32 (cell 98, 40).
8. Play sound _Amb_WindCold at waypoint 30 (cell 60, 99).
9. Play sound _Amb_WindPlains at waypoint 24 (cell 75, 99).
10. Play sound _Amb_WindCold at waypoint 22 (cell 94, 98).
11. Play sound _Amb_WindPlains at waypoint 21 (cell 99, 93).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4557, Events line 4620, Actions line 4683.

<a id="trigger-078de70c"></a>

### 28. Start Ambient Sounds 2 - 078DE70C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078DB6AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 18 (cell 64, 72).
2. Play sound _Amb_WindCold at waypoint 31 (cell 100, 56).
3. Play sound _Amb_WindPlains at waypoint 33 (cell 85, 22).
4. Play sound _Amb_UrbanMurmur2 at waypoint 34 (cell 73, 35).
5. Play sound _Amb_WavesLake at waypoint 35 (cell 117, 64).
6. Play sound _Amb_WavesLake at waypoint 36 (cell 129, 85).
7. Play sound _Amb_WavesLake at waypoint 38 (cell 66, 114).
8. Play sound _Amb_WavesLake at waypoint 39 (cell 87, 133).
9. Play sound _Amb_UrbanMurmur2 at waypoint 40 (cell 69, 129).
10. Play sound _Amb_WindCold at waypoint 41 (cell 98, 130).
11. Play sound _Amb_WindPlains at waypoint 42 (cell 132, 97).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4558, Events line 4621, Actions line 4684.

<a id="trigger-078e314c"></a>

### 29. Start Ambient Sounds 3 - 078E314C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078E5DEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 43 (cell 122, 105).
2. Play sound _Amb_WindPlains at waypoint 44 (cell 110, 116).
3. Play sound _Amb_BirdsTemperate1 at waypoint 26 (cell 125, 124).
4. Play sound _Amb_BirdsPark at waypoint 45 (cell 138, 103).
5. Play sound _Amb_BirdsTemperate2 at waypoint 46 (cell 104, 137).
6. Play sound _Amb_BirdsTemperate1 at waypoint 47 (cell 48, 45).
7. Play sound _Amb_BirdsMorning at waypoint 48 (cell 55, 75).
8. Play sound _Amb_BirdsTemperate1 at waypoint 49 (cell 81, 80).
9. Play sound _Amb_BirdsTemperate2 at waypoint 50 (cell 75, 52).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4559, Events line 4622, Actions line 4685.

<a id="trigger-0cc8e1ac"></a>

### 30. Weather Storm Movie - 0CC8E1AC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CC9606C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 29 (global list position: Weather Controller (GAWEAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Weather Storm Movie 2 (0CC9505C)](#trigger-0cc9505c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4560, Events line 4623, Actions line 4686.

<a id="trigger-0cc9505c"></a>

### 31. Weather Storm Movie 2 - 0CC9505C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Weather Storm Movie (0CC8E1AC)](#trigger-0cc8e1ac).

Attached scope: tag definitions 0CC9107C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 145.
2. Switch the sidebar to tab 2.
3. Flash cameo/type 29; additional configured duration/location argument 200.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4561, Events line 4624, Actions line 4687.

<a id="trigger-0aba865c"></a>

### 32. Prisoners 1b - 0ABA865C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prisoners 1a (0ABAC4EC)](#trigger-0abac4ec); enable from [Prisoners 1c (0ABAAEBC)](#trigger-0abaaebc).

Attached scope: GI (E1), owner Other1 House, cell (52, 51), tag 0ABACADC, persistence mode 0; GI (E1), owner Other1 House, cell (51, 51), tag 0ABACADC, persistence mode 0; GI (E1), owner Other1 House, cell (52, 52), tag 0ABACADC, persistence mode 0; GI (E1), owner Other1 House, cell (53, 51), tag 0ABACADC, persistence mode 0; GI (E1), owner Other1 House, cell (52, 50), tag 0ABACADC, persistence mode 0; GI (E1), owner Other1 House, cell (53, 52), tag 0ABACADC, persistence mode 0; Engineer (ENGINEER), owner Other1 House, cell (52, 52), tag 0ABACADC, persistence mode 0; Engineer (ENGINEER), owner Other1 House, cell (53, 52), tag 0ABACADC, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_A5_AllSoldier2.
2. Play sound MessageText.
3. Display message “Additional troops gained” (MISSION:All01r).
4. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
5. Create radar-event marker type 1 at waypoint 52 (cell 54, 53).
6. Create/recruit team [Flash Engineer (08488A8C)](all12s-teams.md#team-08488a8c).
7. Create/recruit team [Flash GI (0848715C)](all12s-teams.md#team-0848715c).
8. Create/recruit team [Flash Engineer (08488A8C)](all12s-teams.md#team-08488a8c).
9. Create/recruit team [Flash GI (0848715C)](all12s-teams.md#team-0848715c).
10. Create/recruit team [Flash GI (0848715C)](all12s-teams.md#team-0848715c).
11. Create/recruit team [Flash GI (0848715C)](all12s-teams.md#team-0848715c).
12. Create/recruit team [Flash GI (0848715C)](all12s-teams.md#team-0848715c).
13. Create/recruit team [Flash GI (0848715C)](all12s-teams.md#team-0848715c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4562, Events line 4625, Actions line 4688.

<a id="trigger-0abac4ec"></a>

### 33. Prisoners 1a - 0ABAC4EC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Barrel (CAMISC02), owner Civie1 House, cell (56, 52), tag 0ABAC2EC, persistence mode 0; Barrels (CAMISC01), owner Civie1 House, cell (52, 55), tag 0ABAC2EC, persistence mode 0; Barrel (CAMISC02), owner Civie1 House, cell (53, 55), tag 0ABAC2EC, persistence mode 0; Barrels (CAMISC01), owner Civie1 House, cell (56, 51), tag 0ABAC2EC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Prisoners 1b (0ABA865C)](#trigger-0aba865c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4563, Events line 4626, Actions line 4689.

<a id="trigger-0abaaebc"></a>

### 34. Prisoners 1c - 0ABAAEBC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 12 tagged map cells: (51, 50), (52, 50), (53, 50), (54, 50), (51, 51), (54, 51), (51, 52), (54, 52), (51, 53), (52, 53), (53, 53), (54, 53); tag 0ABAACBC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Prisoners 1b (0ABA865C)](#trigger-0aba865c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4564, Events line 4627, Actions line 4690.

<a id="trigger-0a65881c"></a>

### 35. Player Dead - 0A65881C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A65E06C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since scenario start.
2. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Mission Failed (0798A3B0)](#trigger-0798a3b0).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4565, Events line 4628, Actions line 4691.

<a id="trigger-0a5e6e1c"></a>

### 36. Kremlin Secured 1 - 0A5E6E1C

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A5E693C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (MammothDead4) is set.
2. local flag 3 (MammothDead3) is set.
3. local flag 2 (MammothDead2) is set.
4. local flag 1 (MammothDead1) is set.
5. Building does not exist: type index 20 (global list position: Sentry Gun (NALASR)). A map-local type-list change can affect index interpretation.
6. Building does not exist: type index 67 (global list position: Flak Cannon (NAFLAK)). A map-local type-list change can affect index interpretation.
7. Building does not exist: type index 53 (global list position: Tesla Coil (TESLA)). A map-local type-list change can affect index interpretation.

Flag writers in this mission: set local flag 4 (MammothDead4) at [MammothDead4 (0A66D32C)](#trigger-0a66d32c); set local flag 3 (MammothDead3) at [MammothDead3 (0A66D87C)](#trigger-0a66d87c); set local flag 2 (MammothDead2) at [MammothDead2 (0A66DAFC)](#trigger-0a66dafc); set local flag 1 (MammothDead1) at [MammothDead1 (0A66C3BC)](#trigger-0a66c3bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Kremlin Secured 1b (086BC03C)](#trigger-086bc03c).
2. Play voice notification Mis_A12_SoldierNoSurrender.
3. Disable player input.
4. Disable [Player Dead (0A65881C)](#trigger-0a65881c).
5. Disable [Chrono 3 (0861DA8C)](#trigger-0861da8c).
6. Disable [Chrono 3b (0861CDBC)](#trigger-0861cdbc).
7. Disable [Chrono 4 (0861C7AC)](#trigger-0861c7ac).
8. Disable [Chrono 4b (08624E2C)](#trigger-08624e2c).
9. Disable [Objective 2 (09087CB4)](#trigger-09087cb4).
10. Enable and reset applicable timers for [Ally with Player (062329FC)](#trigger-062329fc).
11. Enable and reset applicable timers for [Ally With Bad Guy (062323EC)](#trigger-062323ec).
12. Enable and reset applicable timers for [Kremlin Secured 1a (087AC2BC)](#trigger-087ac2bc).
13. Enable and reset applicable timers for [Failsafe End Mission (0886803C)](#trigger-0886803c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4566, Events line 4629, Actions line 4692.

<a id="trigger-086bc03c"></a>

### 37. Kremlin Secured 1b - 086BC03C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin Secured 1 (0A5E6E1C)](#trigger-0a5e6e1c).

Attached scope: tag definitions 086C004C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_PrimaryObjectiveAchieved.
2. Enable and reset applicable timers for [Kremlin Secured 2 (0A5E684C)](#trigger-0a5e684c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4567, Events line 4630, Actions line 4693.

<a id="trigger-062329fc"></a>

### 38. Ally with Player - 062329FC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin Secured 1 (0A5E6E1C)](#trigger-0a5e6e1c).

Attached scope: tag definitions 062324DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make ally: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4568, Events line 4631, Actions line 4694.

<a id="trigger-062323ec"></a>

### 39. Ally With Bad Guy - 062323EC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin Secured 1 (0A5E6E1C)](#trigger-0a5e6e1c).

Attached scope: tag definitions 062321EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make ally: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4569, Events line 4632, Actions line 4695.

<a id="trigger-087ac2bc"></a>

### 40. Kremlin Secured 1a - 087AC2BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin Secured 1 (0A5E6E1C)](#trigger-0a5e6e1c).

Attached scope: tag definitions 087A849C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 57 (cell 120, 119) with speed setting 3.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4570, Events line 4633, Actions line 4696.

<a id="trigger-0886803c"></a>

### 41. Failsafe End Mission - 0886803C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin Secured 1 (0A5E6E1C)](#trigger-0a5e6e1c).

Attached scope: tag definitions 0D99804C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Mission Victory (09726B10)](#trigger-09726b10).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4571, Events line 4634, Actions line 4697.

<a id="trigger-0a5e684c"></a>

### 42. Kremlin Secured 2 - 0A5E684C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin Secured 1b (086BC03C)](#trigger-086bc03c).

Attached scope: tag definitions 0A5E664C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play full-screen movie 139.
2. Enable and reset applicable timers for [Kremlin Secured 3 (0AEDD8CC)](#trigger-0aedd8cc).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4572, Events line 4635, Actions line 4698.

<a id="trigger-0aedd8cc"></a>

### 43. Kremlin Secured 3 - 0AEDD8CC

Owner reference: Other2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin Secured 2 (0A5E684C)](#trigger-0a5e684c).

Attached scope: tag definitions 0AEE09CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [IFV-Tanya (0D80934C)](all12s-teams.md#team-0d80934c) at waypoint 58 (cell 119, 117).
2. Enable and reset applicable timers for [Kremlin Secured 3b (0AEB998C)](#trigger-0aeb998c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4573, Events line 4636, Actions line 4699.

<a id="trigger-0aeb998c"></a>

### 44. Kremlin Secured 3b - 0AEB998C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin Secured 3 (0AEDD8CC)](#trigger-0aedd8cc).

Attached scope: tag definitions 0AEB951C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 253; location/duration field BF.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4574, Events line 4637, Actions line 4700.

<a id="trigger-0aee1f3c"></a>

### 45. Kremlin is Secured 4 - 0AEE1F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AEE715C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Play Final Movie) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Cheers (0640A0CC)](#trigger-0640a0cc).
2. Play sound BuildingGarrisoned.
3. Play sound WallCrushSandbag.
4. Enable and reset applicable timers for [Kremlin Secured 4b (0A40787C)](#trigger-0a40787c).
5. Enable and reset applicable timers for [Stop Cheers (0ABB5D7C)](#trigger-0abb5d7c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4575, Events line 4638, Actions line 4701.

<a id="trigger-0640a0cc"></a>

### 46. Cheers - 0640A0CC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin is Secured 4 (0AEE1F3C)](#trigger-0aee1f3c); enable from [Kremlin Secured 5 (0AEE6E7C)](#trigger-0aee6e7c).

Attached scope: tag definitions 064095AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4576, Events line 4639, Actions line 4702.

<a id="trigger-0a40787c"></a>

### 47. Kremlin Secured 4b - 0A40787C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin is Secured 4 (0AEE1F3C)](#trigger-0aee1f3c).

Attached scope: tag definitions 0A40751C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “Objective 2 Accomplished - Romanov has been captured” (MISSION:All12c).
3. Enable and reset applicable timers for [Mission Victory (09726B10)](#trigger-09726b10).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4577, Events line 4640, Actions line 4703.

<a id="trigger-0abb5d7c"></a>

### 48. Stop Cheers - 0ABB5D7C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin is Secured 4 (0AEE1F3C)](#trigger-0aee1f3c).

Attached scope: tag definitions 0ABB536C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Cheers (0640A0CC)](#trigger-0640a0cc).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4578, Events line 4641, Actions line 4704.

<a id="trigger-0aee6e7c"></a>

### 49. Kremlin Secured 5 - 0AEE6E7C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AEE0D0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play full-screen movie 143.
2. Enable and reset applicable timers for [Kremlin Secured 6 (0A0C79EC)](#trigger-0a0c79ec).
3. Enable and reset applicable timers for [Cheers (0640A0CC)](#trigger-0640a0cc).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4579, Events line 4642, Actions line 4705.

<a id="trigger-0a0c79ec"></a>

### 50. Kremlin Secured 6 - 0A0C79EC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kremlin Secured 5 (0AEE6E7C)](#trigger-0aee6e7c).

Attached scope: tag definitions 0A0C74AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Mission Victory (09726B10)](#trigger-09726b10).
2. Play sound MessageText.
3. Display message “Objective 2 Accomplished - Romanov has been captured” (MISSION:All12c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4580, Events line 4643, Actions line 4706.

<a id="trigger-0a1c640c"></a>

### 51. Kremlin Secured 6b - 0A1C640C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A1D3B8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4581, Events line 4644, Actions line 4707.

<a id="trigger-0ada748c"></a>

### 52. Secret 1 - 0ADA748C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 27 tagged map cells: (19, 80), (21, 80), (18, 81), (21, 81), (20, 82), (19, 83), (22, 83), (21, 84), (22, 84), (25, 87), (27, 87), (25, 88), (26, 88), (27, 88), (26, 89), (27, 89), (32, 91), (31, 93), (32, 93), (33, 93), (34, 93), (31, 94), (32, 94), (33, 94), (34, 94), (32, 95), (33, 95); tag 0ADA6C6C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Play sound HealCrate.
2. Play sound MessageText.
3. Display message “TSC&ACC” (MISSION:Sov11k).
4. Enable and reset applicable timers for [Secret 2 (0ADA6B7C)](#trigger-0ada6b7c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4582, Events line 4645, Actions line 4708.

<a id="trigger-0ada6b7c"></a>

### 53. Secret 2 - 0ADA6B7C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Secret 1 (0ADA748C)](#trigger-0ada748c).

Attached scope: tag definitions 0ADA68CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “11/21/98” (MISSION:Sov11f).
2. Play sound MessageText.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4583, Events line 4646, Actions line 4709.

<a id="trigger-0a66c3bc"></a>

### 54. MammothDead1 - 0A66C3BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Apocalypse (APOC), owner BadGuy3 House, cell (124, 117), tag 0A66DBEC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 1 (MammothDead1).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4584, Events line 4647, Actions line 4710.

<a id="trigger-0a66dafc"></a>

### 55. MammothDead2 - 0A66DAFC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Apocalypse (APOC), owner BadGuy3 House, cell (122, 117), tag 0A66D96C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 2 (MammothDead2).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4585, Events line 4648, Actions line 4711.

<a id="trigger-0a66d87c"></a>

### 56. MammothDead3 - 0A66D87C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Apocalypse (APOC), owner BadGuy3 House, cell (118, 121), tag 0A66D54C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 3 (MammothDead3).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4586, Events line 4649, Actions line 4712.

<a id="trigger-0a66d32c"></a>

### 57. MammothDead4 - 0A66D32C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Apocalypse (APOC), owner BadGuy3 House, cell (118, 123), tag 0A66D12C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 4 (MammothDead4).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4587, Events line 4650, Actions line 4713.

<a id="trigger-0c49f06c"></a>

### 58. Hint: Chrono Guy 2 - 0C49F06C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: Chrono Guy (0C49C4CC)](#trigger-0c49c4cc).

Attached scope: tag definitions 0C49CC7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_ChronoLegion.
2. Create/recruit team [Hint: Chrono Guy (0A49F17C)](all12s-teams.md#team-0a49f17c).
3. Flash team [Hint: Chrono Guy (0A49F17C)](all12s-teams.md#team-0a49f17c) with duration setting 120.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4588, Events line 4651, Actions line 4714.

<a id="trigger-0c49c4cc"></a>

### 59. Hint: Chrono Guy - 0C49C4CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C49C08C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Infantry Type: type index 15 (global list position: Chrono Legionnaire (CLEG)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Chrono Guy 2 (0C49F06C)](#trigger-0c49f06c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4589, Events line 4652, Actions line 4715.

<a id="trigger-0d9e803c"></a>

### 60. Tanya Laugh - 0D9E803C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D9F104C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (TanyaLaugh) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Tanya Laugh 2 (0D9F203C)](#trigger-0d9f203c).

Source locator: MAPS01.MIX/all12s.map; Triggers line 4590, Events line 4653, Actions line 4716.

<a id="trigger-0d9f203c"></a>

### 61. Tanya Laugh 2 - 0D9F203C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tanya Laugh (0D9E803C)](#trigger-0d9e803c).

Attached scope: tag definitions 0DCD8A2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound TanyaCreated.

Source locator: MAPS01.MIX/all12s.map; Triggers line 4591, Events line 4654, Actions line 4717.

[All team rosters and ordered plans](all12s-teams.md) | [All mission overrides](all12s-overrides.md)
