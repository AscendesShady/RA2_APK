# Operation: Red Revolution

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov11s.map. **Effective extracted member:** MAPS02.MIX/sov11s.map. **Trigger definitions:** 46.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov11s-teams.md) | [All mission overrides](sov11s-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | SNOW |
| Map size | 0,0,60,115 |
| Visible local rectangle | 2,7,56,102 |
| Placed vehicles | 25 |
| Placed infantry | 61 |
| Placed structures | 223 |
| Placed aircraft | 0 |
| Team templates | 32 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 2000 | BadGuy1 |
| 2 | BadGuy2 House | 2000 | BadGuy2 |
| 3 | BadGuy3 House | 200 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 20 | Other1 |
| 6 | Other2 House | 20 | Other2 |
| 7 | Other3 House | 20 | Other3 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Play IC Movie,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [MISSION FAIL (092D76FC)](#trigger-092d76fc) | 4 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [MISSION VICTORY (092D6E5C)](#trigger-092d6e5c) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-08fdb280"></a>

### 1. Enable Production: BadGuy1 - 08FDB280

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08FE2CB0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4602, Events line 4650, Actions line 4698.

<a id="trigger-091d1710"></a>

### 2. Enable Production: Bad2 - 091D1710

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 091DFD60 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 280 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
2. AI triggers begin: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4603, Events line 4651, Actions line 4699.

<a id="trigger-092d76fc"></a>

### 3. MISSION FAIL - 092D76FC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Lose Condition 1 (092D6BDC)](#trigger-092d6bdc).

Attached scope: tag definitions 092D6F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4604, Events line 4652, Actions line 4700.

<a id="trigger-092d6e5c"></a>

### 4. MISSION VICTORY - 092D6E5C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Defeated (089FDF3C)](#trigger-089fdf3c).

Attached scope: tag definitions 092D6CCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4605, Events line 4653, Actions line 4701.

<a id="trigger-092d6bdc"></a>

### 5. Lose Condition 1 - 092D6BDC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 092D673C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [MISSION FAIL (092D76FC)](#trigger-092d76fc).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4606, Events line 4654, Actions line 4702.

<a id="trigger-073837cc"></a>

### 6. Base Attack 1 - 073837CC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 073831AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create/recruit team [Conscripts6 (0A669CBC)](sov11s-teams.md#team-0a669cbc).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4607, Events line 4655, Actions line 4703.

<a id="trigger-089fdf3c"></a>

### 7. Yuri Defeated - 089FDF3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Kremlin (CARUS03), owner BadGuy3 House, cell (46, 43), tag 089FA21C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [MISSION VICTORY (092D6E5C)](#trigger-092d6e5c).
2. Enable and reset applicable timers for [Cheer (0CEDB2BC)](#trigger-0cedb2bc).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4608, Events line 4656, Actions line 4704.

<a id="trigger-0cedb2bc"></a>

### 8. Cheer - 0CEDB2BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Defeated (089FDF3C)](#trigger-089fdf3c).

Attached scope: tag definitions 0CEDE1CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4609, Events line 4657, Actions line 4705.

<a id="trigger-07924bec"></a>

### 9. Reinforcements Arrive - 07924BEC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0792438C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 450 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 6 (cell 113, 161).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Supply reinforcement team [Reinforcements (0AB8657C)](sov11s-teams.md#team-0ab8657c) at waypoint 5 (cell 113, 166).
4. Enable and reset applicable timers for [Ping2 (0B75A2FC)](#trigger-0b75a2fc).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4610, Events line 4658, Actions line 4706.

<a id="trigger-0b75a2fc"></a>

### 10. Ping2 - 0B75A2FC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforcements Arrive (07924BEC)](#trigger-07924bec).

Attached scope: tag definitions 0B75BADC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 6 (cell 113, 161).
2. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4611, Events line 4659, Actions line 4707.

<a id="trigger-0adef33c"></a>

### 11. Mission Start - 0ADEF33C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ADF0A3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “Objective 1: Destroy the KREMLIN, where YURI is cowering” (MISSION:Sov11a).
3. Play voice notification Mis_S11_SofiaStopYuri.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4612, Events line 4660, Actions line 4708.

<a id="trigger-0adf094c"></a>

### 12. Mission Start 2 - 0ADF094C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ADF041C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 98 (cell 49, 47).
2. Reveal terrain around waypoint 7 (cell 44, 45).
3. Reveal terrain around waypoint 8 (cell 47, 48).
4. Reveal terrain around waypoint 9 (cell 50, 45).
5. Reveal terrain around waypoint 10 (cell 47, 42).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4613, Events line 4661, Actions line 4709.

<a id="trigger-0adf032c"></a>

### 13. Ping Yuri's Base - 0ADF032C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ADF1DFC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 98 (cell 49, 47).
2. Play sound MessageText.
3. Display message “Objective 1: Destroy the KREMLIN, where YURI is cowering” (MISSION:Sov11a).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4614, Events line 4662, Actions line 4710.

<a id="trigger-0b75b6fc"></a>

### 14. Disable Ping2 - 0B75B6FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B75B4FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Ping2 (0B75A2FC)](#trigger-0b75a2fc).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4615, Events line 4663, Actions line 4711.

<a id="trigger-080a2d3c"></a>

### 15. Create Crates - 080A2D3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 080A69DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 11 (cell 140, 111).
2. Create crate type 11 at waypoint 12 (cell 101, 103).
3. Create crate type 2 at waypoint 13 (cell 56, 106).
4. Create crate type 0 at waypoint 14 (cell 66, 119).
5. Create crate type 2 at waypoint 15 (cell 95, 51).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4616, Events line 4664, Actions line 4712.

<a id="trigger-080a6e9c"></a>

### 16. Start Ambient Sounds 1 - 080A6E9C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 080AAE1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 6 (cell 113, 161).
2. Play sound _Amb_BirdsNightOwl at waypoint 16 (cell 95, 133).
3. Play sound _Amb_WindPlains at waypoint 4 (cell 91, 118).
4. Play sound _Amb_CricketBed at waypoint 17 (cell 107, 124).
5. Play sound _Amb_WindCold at waypoint 18 (cell 124, 141).
6. Play sound _Amb_BirdsNightOwl at waypoint 0 (cell 129, 127).
7. Play sound _Amb_WindCold at waypoint 3 (cell 115, 104).
8. Play sound _Amb_WindPlains at waypoint 19 (cell 94, 96).
9. Play sound _Amb_CricketChirps at waypoint 20 (cell 72, 111).
10. Play sound _Amb_BirdsNightOwl at waypoint 38 (cell 76, 101).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4617, Events line 4665, Actions line 4713.

<a id="trigger-080aa86c"></a>

### 17. Start Ambient Sounds 2 - 080AA86C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 080A8A7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 21 (cell 32, 78).
2. Play sound _Amb_UrbanMurmur2 at waypoint 22 (cell 56, 54).
3. Play sound _Amb_UrbanMurmur1 at waypoint 23 (cell 79, 33).
4. Play sound _Amb_BirdsNightOwl at waypoint 15 (cell 95, 51).
5. Play sound _Amb_WindCold at waypoint 24 (cell 93, 74).
6. Play sound _Amb_WindPlains at waypoint 25 (cell 115, 84).
7. Play sound _Amb_WindCold at waypoint 26 (cell 78, 76).
8. Play sound _Amb_WindCold at waypoint 27 (cell 32, 57).
9. Play sound _Amb_WindPlains at waypoint 28 (cell 59, 28).
10. Play sound _Amb_CricketBed at waypoint 39 (cell 145, 101).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4618, Events line 4666, Actions line 4714.

<a id="trigger-0808a73c"></a>

### 18. Start Ambient Sounds 3 - 0808A73C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 080AABBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WavesLake at waypoint 29 (cell 65, 63).
2. Play sound _Amb_WavesLake at waypoint 30 (cell 47, 86).
3. Play sound _Amb_WavesLake at waypoint 31 (cell 84, 62).
4. Play sound _Amb_WavesLake at waypoint 32 (cell 126, 76).
5. Play sound _Amb_WavesLake at waypoint 33 (cell 164, 112).
6. Play sound _Amb_WavesLake at waypoint 34 (cell 153, 124).
7. Play sound _Amb_WavesLake at waypoint 35 (cell 137, 143).
8. Play sound _Amb_WavesLake at waypoint 36 (cell 125, 151).
9. Play sound _Amb_WavesLake at waypoint 37 (cell 86, 140).
10. Play sound _Amb_WindCold at waypoint 11 (cell 140, 111).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4619, Events line 4667, Actions line 4715.

<a id="trigger-080d491c"></a>

### 19. Bad Guy 3 - 080D491C

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 080DFB2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Production Begins: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).
3. AI triggers begin: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4620, Events line 4668, Actions line 4716.

<a id="trigger-0b81c44c"></a>

### 20. Create Kirovs Easy a - 0B81C44C

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kirov Timer (0B34751C)](#trigger-0b34751c); enable from [Start Nuke Attacks 4 (078C31CC)](#trigger-078c31cc).

Attached scope: tag definitions 0B83B06C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG3 - Kirovs2 (Left) (0A52E3DC)](sov11s-teams.md#team-0a52e3dc) at waypoint 42 (cell 51, 108).
2. Create radar-event marker type 5 at waypoint 42 (cell 51, 108).
3. Disable [Create Kirovs Easy a (0B81C44C)](#trigger-0b81c44c).
4. Enable and reset applicable timers for [Kirov Timer (0B34751C)](#trigger-0b34751c).
5. Supply reinforcement team [BG3 - Kirovs 1 (07A4966C)](sov11s-teams.md#team-07a4966c) at waypoint 49 (cell 127, 69).
6. Create radar-event marker type 5 at waypoint 49 (cell 127, 69).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4621, Events line 4669, Actions line 4717.

<a id="trigger-0b34751c"></a>

### 21. Kirov Timer - 0B34751C

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create Kirovs Easy a (0B81C44C)](#trigger-0b81c44c); enable from [Create Kirovs Hard a (0B83E7FC)](#trigger-0b83e7fc); enable from [Create Kirovs Medium a (0B83EE5C)](#trigger-0b83ee5c); enable from [Start Nuke Attacks 4 (078C31CC)](#trigger-078c31cc).

Attached scope: tag definitions 0B347D3C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create Kirovs Easy a (0B81C44C)](#trigger-0b81c44c).
2. Enable and reset applicable timers for [Create Kirovs Hard a (0B83E7FC)](#trigger-0b83e7fc).
3. Enable and reset applicable timers for [Create Kirovs Medium a (0B83EE5C)](#trigger-0b83ee5c).
4. Disable [Kirov Timer (0B34751C)](#trigger-0b34751c).
5. Play voice notification EVA_EnemyAirArmadaDetected.
6. Play sound MessageText.
7. Display message “WARNING: Enemy air armada detected” (MISSION:Sov11b).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4622, Events line 4670, Actions line 4718.

<a id="trigger-0b83e7fc"></a>

### 22. Create Kirovs Hard a - 0B83E7FC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kirov Timer (0B34751C)](#trigger-0b34751c); enable from [Start Nuke Attacks 4 (078C31CC)](#trigger-078c31cc).

Attached scope: tag definitions 0B83E1DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG3 - Kirovs2 (Left) (0A52E3DC)](sov11s-teams.md#team-0a52e3dc) at waypoint 42 (cell 51, 108).
2. Supply reinforcement team [BG3 - Kirovs2 (Left) (0A52E3DC)](sov11s-teams.md#team-0a52e3dc) at waypoint 41 (cell 56, 113).
3. Supply reinforcement team [BG3 - Kirovs2 (Left) (0A52E3DC)](sov11s-teams.md#team-0a52e3dc) at waypoint 40 (cell 64, 121).
4. Create radar-event marker type 5 at waypoint 40 (cell 64, 121).
5. Disable [Create Kirovs Hard a (0B83E7FC)](#trigger-0b83e7fc).
6. Enable and reset applicable timers for [Kirov Timer (0B34751C)](#trigger-0b34751c).
7. Supply reinforcement team [BG3 - Kirovs 1 (07A4966C)](sov11s-teams.md#team-07a4966c) at waypoint 49 (cell 127, 69).
8. Supply reinforcement team [BG3 - Kirovs 1 (07A4966C)](sov11s-teams.md#team-07a4966c) at waypoint 48 (cell 132, 74).
9. Supply reinforcement team [BG3 - Kirovs 1 (07A4966C)](sov11s-teams.md#team-07a4966c) at waypoint 49 (cell 127, 69).
10. Create radar-event marker type 5 at waypoint 48 (cell 132, 74).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4623, Events line 4671, Actions line 4719.

<a id="trigger-0b83ee5c"></a>

### 23. Create Kirovs Medium a - 0B83EE5C

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kirov Timer (0B34751C)](#trigger-0b34751c); enable from [Start Nuke Attacks 4 (078C31CC)](#trigger-078c31cc).

Attached scope: tag definitions 0B83E8EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG3 - Kirovs2 (Left) (0A52E3DC)](sov11s-teams.md#team-0a52e3dc) at waypoint 42 (cell 51, 108).
2. Supply reinforcement team [BG3 - Kirovs2 (Left) (0A52E3DC)](sov11s-teams.md#team-0a52e3dc) at waypoint 41 (cell 56, 113).
3. Create radar-event marker type 5 at waypoint 41 (cell 56, 113).
4. Disable [Create Kirovs Medium a (0B83EE5C)](#trigger-0b83ee5c).
5. Enable and reset applicable timers for [Kirov Timer (0B34751C)](#trigger-0b34751c).
6. Supply reinforcement team [BG3 - Kirovs 1 (07A4966C)](sov11s-teams.md#team-07a4966c) at waypoint 49 (cell 127, 69).
7. Supply reinforcement team [BG3 - Kirovs 1 (07A4966C)](sov11s-teams.md#team-07a4966c) at waypoint 48 (cell 132, 74).
8. Create radar-event marker type 5 at waypoint 48 (cell 132, 74).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4624, Events line 4672, Actions line 4720.

<a id="trigger-078c3d3c"></a>

### 24. Start Nuke Attacks - 078C3D3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Nuke Destroyed (0C46503C)](#trigger-0c46503c).

Attached scope: tag definitions 078C397C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 54 (global list position: Nuclear Missile Silo (NAMISL)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Start Nuke Attacks 2 (078C388C)](#trigger-078c388c).
2. Disable [Start Nuke Attacks (078C3D3C)](#trigger-078c3d3c).
3. Enable and reset applicable timers for [Nuke Destroyed (0C46503C)](#trigger-0c46503c).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4625, Events line 4673, Actions line 4721.

<a id="trigger-078c388c"></a>

### 25. Start Nuke Attacks 2 - 078C388C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start Nuke Attacks (078C3D3C)](#trigger-078c3d3c).

Attached scope: tag definitions 078C35AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S11_YuriTaunt4.
2. Enable and reset applicable timers for [Start Nuke Attacks 3 (078C34BC)](#trigger-078c34bc).
3. Disable [Start Nuke Attacks 2 (078C388C)](#trigger-078c388c).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4626, Events line 4674, Actions line 4722.

<a id="trigger-0c46503c"></a>

### 26. Nuke Destroyed - 0C46503C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start Nuke Attacks (078C3D3C)](#trigger-078c3d3c).

Attached scope: tag definitions 0C45FE0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 54 (global list position: Nuclear Missile Silo (NAMISL)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Start Nuke Attacks (078C3D3C)](#trigger-078c3d3c).
2. Disable [Kirov Timer (0B34751C)](#trigger-0b34751c).
3. Disable [Nuke Destroyed (0C46503C)](#trigger-0c46503c).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4627, Events line 4675, Actions line 4723.

<a id="trigger-078c34bc"></a>

### 27. Start Nuke Attacks 3 - 078C34BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start Nuke Attacks 2 (078C388C)](#trigger-078c388c).

Attached scope: tag definitions 078C32BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound NukeSiren.
2. Enable and reset applicable timers for [Start Nuke Attacks 4 (078C31CC)](#trigger-078c31cc).
3. Disable [Start Nuke Attacks 3 (078C34BC)](#trigger-078c34bc).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4628, Events line 4676, Actions line 4724.

<a id="trigger-078c31cc"></a>

### 28. Start Nuke Attacks 4 - 078C31CC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start Nuke Attacks 3 (078C34BC)](#trigger-078c34bc).

Attached scope: tag definitions 078CC31C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S11_SofiaKirovWarning.
2. Enable and reset applicable timers for [Create Kirovs Easy a (0B81C44C)](#trigger-0b81c44c).
3. Enable and reset applicable timers for [Create Kirovs Hard a (0B83E7FC)](#trigger-0b83e7fc).
4. Enable and reset applicable timers for [Create Kirovs Medium a (0B83EE5C)](#trigger-0b83ee5c).
5. Enable and reset applicable timers for [Start Nuke Attacks 5 (078C44DC)](#trigger-078c44dc).
6. Disable [Start Nuke Attacks 4 (078C31CC)](#trigger-078c31cc).
7. Enable and reset applicable timers for [Kirov Timer (0B34751C)](#trigger-0b34751c).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4629, Events line 4677, Actions line 4725.

<a id="trigger-078c44dc"></a>

### 29. Start Nuke Attacks 5 - 078C44DC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start Nuke Attacks 4 (078C31CC)](#trigger-078c31cc).

Attached scope: tag definitions 078C064C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 11 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S11_SofiaBuildFlakCannons.
2. Display message “HINT: To stop Kirov Airships, build lots of Flak Cannons” (MISSION:Sov11d).
3. Play sound MessageText.
4. Disable [Start Nuke Attacks 5 (078C44DC)](#trigger-078c44dc).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4630, Events line 4678, Actions line 4726.

<a id="trigger-0807066c"></a>

### 30. Secret - 0807066C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 8 tagged map cells: (140, 103), (141, 103), (142, 103), (140, 104), (141, 104), (142, 104), (141, 105), (142, 105); tag 08075C0C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “TSC&ACC” (MISSION:Sov11k).
3. Play sound HealCrate.
4. Enable and reset applicable timers for [Secret 2 (0D117D9C)](#trigger-0d117d9c).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4631, Events line 4679, Actions line 4727.

<a id="trigger-0d117d9c"></a>

### 31. Secret 2 - 0D117D9C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Secret (0807066C)](#trigger-0807066c).

Attached scope: tag definitions 0D11791C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “11/21/98” (MISSION:Sov11f).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4632, Events line 4680, Actions line 4728.

<a id="trigger-08065b0c"></a>

### 32. Psychic Sensor Movie - 08065B0C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0806A99C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 10 (global list position: Soviet Battle Lab (NATECH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play in-game movie 120.
2. Switch the sidebar to tab 1.
3. Flash cameo/type 18; additional configured duration/location argument 120.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4633, Events line 4681, Actions line 4729.

<a id="trigger-096aa3ec"></a>

### 33. Starting Forces - 096AA3EC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096AF7FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Player Kirov 1 (096ACEFC)](sov11s-teams.md#team-096acefc).
2. Create/recruit team [Player Kirov 2 (096A857C)](sov11s-teams.md#team-096a857c).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4634, Events line 4682, Actions line 4730.

<a id="trigger-0ac3f51c"></a>

### 34. Yuri Taunt Movie - 0AC3F51C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AC3839C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).

**Then perform these actions in order:**

1. Play in-game movie 80.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4635, Events line 4683, Actions line 4731.

<a id="trigger-082aa26c"></a>

### 35. Play IC Movie - 082AA26C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 082AB97C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 119.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4636, Events line 4684, Actions line 4732.

<a id="trigger-084b533c"></a>

### 36. Lock Input - 084B533C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 084B6A5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable player input.
2. Enable and reset applicable timers for [Start Scroll (084B696C)](#trigger-084b696c).
3. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4637, Events line 4685, Actions line 4733.

<a id="trigger-084b696c"></a>

### 37. Start Scroll - 084B696C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Lock Input (084B533C)](#trigger-084b533c).

Attached scope: tag definitions 084B668C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 14 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 99 (cell 111, 152) with speed setting 4.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4638, Events line 4686, Actions line 4734.

<a id="trigger-0c3a654c"></a>

### 38. Unlock Input - 0C3A654C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C3A61AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Unlock Input 2 (0C3A60BC)](#trigger-0c3a60bc).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4639, Events line 4687, Actions line 4735.

<a id="trigger-0c3a60bc"></a>

### 39. Unlock Input 2 - 0C3A60BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Unlock Input (0C3A654C)](#trigger-0c3a654c).

Attached scope: tag definitions 0C3A751C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_BattlefieldControlOnline.
2. Display message “--Battle Control Online--” (MISSION:All01q).
3. Play sound MessageText.
4. Enable player input.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4640, Events line 4688, Actions line 4736.

<a id="trigger-0769050c"></a>

### 40. Yuri Audio 1 - 0769050C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0769FEDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 14 (global list position: Soviet War Factory (NAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Yuri Audio 1b (0769FDEC)](#trigger-0769fdec).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4641, Events line 4689, Actions line 4737.

<a id="trigger-0769fdec"></a>

### 41. Yuri Audio 1b - 0769FDEC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Audio 1 (0769050C)](#trigger-0769050c).

Attached scope: tag definitions 0769B88C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S11_YuriTaunt1.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4642, Events line 4690, Actions line 4738.

<a id="trigger-0ae8909c"></a>

### 42. Yuri Audio 2b - 0AE8909C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Audio 2 (0AE930AC)](#trigger-0ae930ac).

Attached scope: tag definitions 0AE9319C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S11_YuriTaunt2.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4643, Events line 4691, Actions line 4739.

<a id="trigger-0ae930ac"></a>

### 43. Yuri Audio 2 - 0AE930AC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE960EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Unit Type: type index 15 (global list position: Kirov Airship (ZEP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Yuri Audio 2b (0AE8909C)](#trigger-0ae8909c).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4644, Events line 4692, Actions line 4740.

<a id="trigger-0ae911bc"></a>

### 44. Yuri Audio 3b - 0AE911BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Audio 3 (0AE951BC)](#trigger-0ae951bc).

Attached scope: tag definitions 0AE9207C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S11_YuriTaunt5.

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4645, Events line 4693, Actions line 4741.

<a id="trigger-0ae951bc"></a>

### 45. Yuri Audio 3 - 0AE951BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE941CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Unit Type: type index 16 (global list position: Terror Drone (DRON)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Yuri Audio 3b (0AE911BC)](#trigger-0ae911bc).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4646, Events line 4694, Actions line 4742.

<a id="trigger-064ba67c"></a>

### 46. Starting Forces 2 - 064BA67C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 064BA19C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Player MCV (096A167C)](sov11s-teams.md#team-096a167c).

Source locator: MAPS02.MIX/sov11s.map; Triggers line 4647, Events line 4695, Actions line 4743.

[All team rosters and ordered plans](sov11s-teams.md) | [All mission overrides](sov11s-overrides.md)
