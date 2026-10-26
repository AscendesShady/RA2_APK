# Operation: Tomb Raided

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all04dmd.map. **Effective extracted member:** mapsmd03.mix/all04dmd.map. **Trigger definitions:** 142.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all04dmd-teams.md) | [All mission overrides](all04dmd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Americans |
| Theater | DESERT |
| Map size | 0,0,119,82 |
| Visible local rectangle | 2,5,115,71 |
| Placed vehicles | 25 |
| Placed infantry | 38 |
| Placed structures | 85 |
| Placed aircraft | 0 |
| Team templates | 82 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 80 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 0 | Africans |
| 6 | Arabs | 50 | YuriCountry2 |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 50 | Russians |
| 9 | YuriCountry | 480 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 0 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | HoverDeliver,0 |
| 1 | PsychicDomKilled,0 |
| 2 | Tanya Dead,0 |
| 3 | Obj1Complete,0 |
| 4 | HoverDeliver2,0 |
| 5 | InPlace1,0 |
| 6 | InPlace2,0 |
| 7 | InPlace3,0 |
| 8 | Tanya Crossed,0 |
| 9 | TanyaOut,0 |
| 10 | Obj2 Complete,0 |
| 11 | Oil Derricks Taken,0 |
| 12 | EinsteinIn,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [It's Over! 2 (0682668C)](#trigger-0682668c) | 2 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner. |
| [We Won! (0A2F818C)](#trigger-0a2f818c) | 15 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner. |
| [It's Over : ( (09F7C5BC)](#trigger-09f7c5bc) | Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans). | Announce defeat. |

## Every trigger, in file order

<a id="trigger-088e9f3c"></a>

### 1. START! - 088E9F3C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 088E969C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable player input.
2. Play voice notification EVA_EstablishBattlefieldControl.
3. Create/recruit team [_Tank Des 1 (0C1EAC8C)](all04dmd-teams.md#team-0c1eac8c).
4. Create/recruit team [_Tank Des 2 (0C1EA7DC)](all04dmd-teams.md#team-0c1ea7dc).
5. Create/recruit team [_Tank Des 3 (0C1EA15C)](all04dmd-teams.md#team-0c1ea15c).
6. Create/recruit team [_Tank Des 4 (0C1EBC8C)](all04dmd-teams.md#team-0c1ebc8c).
7. Production Begins: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
8. AI triggers begin: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
9. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).
10. Play in-game movie 16.
11. Enable and reset applicable timers for [_Introduce Tank Destroyer (092600DC)](#trigger-092600dc).
12. Move the camera to waypoint 0 (cell 82, 162) with speed setting 1.
13. Create/recruit team [Engin1Move (0BA1E1AC)](all04dmd-teams.md#team-0ba1e1ac).
14. Create/recruit team [Engin2Move (0BA176CC)](all04dmd-teams.md#team-0ba176cc).
15. Create/recruit team [GI1Move (0BA260EC)](all04dmd-teams.md#team-0ba260ec).
16. Create/recruit team [GI2Move (0BA275EC)](all04dmd-teams.md#team-0ba275ec).
17. Create/recruit team [MVC Move (0933DB7C)](all04dmd-teams.md#team-0933db7c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8182, Events line 8326, Actions line 8470.

<a id="trigger-092600dc"></a>

### 2. _Introduce Tank Destroyer - 092600DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [START! (088E9F3C)](#trigger-088e9f3c).

Attached scope: tag definitions 09261D0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 61 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_TankDestroyer.
2. Flash team [_Tank Des 1 (0C1EAC8C)](all04dmd-teams.md#team-0c1eac8c) with duration setting 60.
3. Flash team [_Tank Des 2 (0C1EA7DC)](all04dmd-teams.md#team-0c1ea7dc) with duration setting 60.
4. Flash team [_Tank Des 3 (0C1EA15C)](all04dmd-teams.md#team-0c1ea15c) with duration setting 60.
5. Flash team [_Tank Des 4 (0C1EBC8C)](all04dmd-teams.md#team-0c1ebc8c) with duration setting 60.
6. Enable and reset applicable timers for [_Send DUMMY 1 (0BA91B3C)](#trigger-0ba91b3c).
7. Enable and reset applicable timers for [_Send DUMMY 2 (0BA9151C)](#trigger-0ba9151c).
8. Enable and reset applicable timers for [_Resume Some Control (00000000)](#trigger-00000000).
9. Enable and reset applicable timers for [Mission Obj 1 (0A6CFA2C)](#trigger-0a6cfa2c).
10. Enable and reset applicable timers for [Rescue Einstein! (0AB1EF3C)](#trigger-0ab1ef3c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8183, Events line 8327, Actions line 8471.

<a id="trigger-0ba91b3c"></a>

### 3. _Send DUMMY 1 - 0BA91B3C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Introduce Tank Destroyer (092600DC)](#trigger-092600dc).

Attached scope: tag definitions 0BA9160C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_Dummy Team 1 (0B3C604C)](all04dmd-teams.md#team-0b3c604c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8184, Events line 8328, Actions line 8472.

<a id="trigger-0ba9151c"></a>

### 4. _Send DUMMY 2 - 0BA9151C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Introduce Tank Destroyer (092600DC)](#trigger-092600dc).

Attached scope: tag definitions 0BA912FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_Dummy Team 2 (0B3C129C)](all04dmd-teams.md#team-0b3c129c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8185, Events line 8329, Actions line 8473.

<a id="trigger-00000000"></a>

### 5. _Resume Some Control - 00000000

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Introduce Tank Destroyer (092600DC)](#trigger-092600dc).

Attached scope: tag definitions 0925DEDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 67 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Play voice notification EVA_BattlefieldControlOnline.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8186, Events line 8330, Actions line 8474.

<a id="trigger-0a6cfa2c"></a>

### 6. Mission Obj 1 - 0A6CFA2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Introduce Tank Destroyer (092600DC)](#trigger-092600dc); enable from [_Introduce Psychic Towers (0BDA918C)](#trigger-0bda918c).

Attached scope: tag definitions 0A6C8CEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Rescue Einstein from Yuri's secret base near the Great Pyramid” (MISSION:RescueEinstein).
2. Create radar-event marker type 1 at waypoint 29 (cell 90, 103).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8187, Events line 8331, Actions line 8475.

<a id="trigger-0ab1ef3c"></a>

### 7. Rescue Einstein! - 0AB1EF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Introduce Tank Destroyer (092600DC)](#trigger-092600dc).

Attached scope: tag definitions 0AB1FDCC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA4_EvaRescueEinstein.
2. Disable [Rescue Einstein! (0AB1EF3C)](#trigger-0ab1ef3c).
3. Enable and reset applicable timers for [Mission Obj 1c (0DE1DF3C)](#trigger-0de1df3c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8188, Events line 8332, Actions line 8476.

<a id="trigger-0de1df3c"></a>

### 8. Mission Obj 1c - 0DE1DF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Rescue Einstein! (0AB1EF3C)](#trigger-0ab1ef3c); enable from [_Introduce Psychic Towers (0BDA918C)](#trigger-0bda918c).

Attached scope: tag definitions 0DE1D94C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA4_EinsteinSaveMe.
2. Disable [Mission Obj 1c (0DE1DF3C)](#trigger-0de1df3c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8189, Events line 8333, Actions line 8477.

<a id="trigger-0440dd8c"></a>

### 9. _START2 - 0440DD8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0440EC6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 26 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification A04_p01.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8190, Events line 8334, Actions line 8478.

<a id="trigger-067e815c"></a>

### 10. Immediate Rush - 067E815C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 067EBA3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Yuri Foot Attack (0BA0EA9C)](all04dmd-teams.md#team-0ba0ea9c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8191, Events line 8335, Actions line 8479.

<a id="trigger-0c92903c"></a>

### 11. Yuri Hover Attack - 0C92903C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C92EF4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 135 (global list position: Air Force Command Headquarters (AMRADR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Yuri Hover Attack (0C1DD59C)](all04dmd-teams.md#team-0c1dd59c).
2. Disable [Yuri Hover Attack (0C92903C)](#trigger-0c92903c).
3. Enable and reset applicable timers for [Hover Return (0A6B4C6C)](#trigger-0a6b4c6c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8192, Events line 8336, Actions line 8480.

<a id="trigger-0a6b4c6c"></a>

### 12. Hover Return - 0A6B4C6C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Hover Attack (0C92903C)](#trigger-0c92903c).

Attached scope: tag definitions 0A6BCF1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (HoverDeliver) is set.

Flag writers in this mission: clear local flag 0 (HoverDeliver) at [Y Auto Hover 1b (0AE4A3CC)](#trigger-0ae4a3cc); clear local flag 0 (HoverDeliver) at [Y Auto Hover 1b Alt (0687F03C)](#trigger-0687f03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Hover Return (0C1E1B7C)](all04dmd-teams.md#team-0c1e1b7c).
2. Disable [Hover Return (0A6B4C6C)](#trigger-0a6b4c6c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8193, Events line 8337, Actions line 8481.

<a id="trigger-0bb9207c"></a>

### 13. Bridge Detect - 0BB9207C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Restart Bridge Detect (0AEBE63C)](#trigger-0aebe63c).

Attached scope: 1 tagged map cells: (161, 68); tag 0BB9410C, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Bridge Detect (0BB9207C)](#trigger-0bb9207c).
2. Enable and reset applicable timers for [Engineer Delay (0AEBEF3C)](#trigger-0aebef3c).
3. Enable and reset applicable timers for [Restart Bridge Detect (0AEBE63C)](#trigger-0aebe63c).
4. Create/recruit team [No Bridge Hover Attack (0C1E16CC)](all04dmd-teams.md#team-0c1e16cc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8194, Events line 8338, Actions line 8482.

<a id="trigger-0aebef3c"></a>

### 14. Engineer Delay - 0AEBEF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge Detect (0BB9207C)](#trigger-0bb9207c); enable from [Engineer Dead? (088801BC)](#trigger-088801bc).

Attached scope: tag definitions 0AEBEA0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 13 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Engineer Delay (0AEBEF3C)](#trigger-0aebef3c).
2. Supply reinforcement team [Engineer Repair Task (0C1DD0EC)](all04dmd-teams.md#team-0c1dd0ec) at waypoint 3 (cell 144, 32).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8195, Events line 8339, Actions line 8483.

<a id="trigger-0aebe63c"></a>

### 15. Restart Bridge Detect - 0AEBE63C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge Detect (0BB9207C)](#trigger-0bb9207c).

Attached scope: Bridge Repair Hut (CABHUT), owner Neutral, cell (154, 66), tag 0AEBE3FC, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Bridge Detect (0BB9207C)](#trigger-0bb9207c).
2. Disable [Restart Bridge Detect (0AEBE63C)](#trigger-0aebe63c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8196, Events line 8340, Actions line 8484.

<a id="trigger-089ac7fc"></a>

### 16. End All - 089AC7FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Barracks (YABRCK), owner YuriCountry, cell (142, 30), tag 089AEAAC, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Destroy current instances of [Bridge Detect (0BB9207C)](#trigger-0bb9207c).
2. Destroy current instances of [Engineer Delay (0AEBEF3C)](#trigger-0aebef3c).
3. Destroy current instances of [Restart Bridge Detect (0AEBE63C)](#trigger-0aebe63c).
4. Destroy current instances of [2nd Bridge Detect (0B24E20C)](#trigger-0b24e20c).
5. Destroy current instances of [2nd Engineer Delay (0B24930C)](#trigger-0b24930c).
6. Destroy current instances of [2nd Restart Bridge Detect (0B2495EC)](#trigger-0b2495ec).
7. Remove instances of the team organization (not automatically its surviving objects) [Yuri Hover Attack (0C1DD59C)](all04dmd-teams.md#team-0c1dd59c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8197, Events line 8341, Actions line 8485.

<a id="trigger-0b24e20c"></a>

### 17. 2nd Bridge Detect - 0B24E20C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [2nd Restart Bridge Detect (0B2495EC)](#trigger-0b2495ec).

Attached scope: 1 tagged map cells: (146, 110); tag 0B2493FC, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [2nd Bridge Detect (0B24E20C)](#trigger-0b24e20c).
2. Enable and reset applicable timers for [2nd Restart Bridge Detect (0B2495EC)](#trigger-0b2495ec).
3. Enable and reset applicable timers for [2nd Engineer Delay (0B24930C)](#trigger-0b24930c).
4. Create/recruit team [No Bridge Hover Attack 2 (0BCE121C)](all04dmd-teams.md#team-0bce121c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8198, Events line 8342, Actions line 8486.

<a id="trigger-0b24930c"></a>

### 18. 2nd Engineer Delay - 0B24930C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [2nd Bridge Detect (0B24E20C)](#trigger-0b24e20c); enable from [2nd Engineer Dead? (0888103C)](#trigger-0888103c).

Attached scope: tag definitions 0B24915C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Engineer Unit 2 (0C1DEB7C)](all04dmd-teams.md#team-0c1deb7c) at waypoint 3 (cell 144, 32).
2. Disable [2nd Engineer Delay (0B24930C)](#trigger-0b24930c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8199, Events line 8343, Actions line 8487.

<a id="trigger-0b2495ec"></a>

### 19. 2nd Restart Bridge Detect - 0B2495EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [2nd Bridge Detect (0B24E20C)](#trigger-0b24e20c).

Attached scope: Bridge Repair Hut (CABHUT), owner Neutral, cell (154, 112), tag 0B25504C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [2nd Bridge Detect (0B24E20C)](#trigger-0b24e20c).
2. Disable [2nd Restart Bridge Detect (0B2495EC)](#trigger-0b2495ec).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8200, Events line 8344, Actions line 8488.

<a id="trigger-0895f93c"></a>

### 20. _START_Oil Guard  - 0895F93C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0895F30C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Oil Derreck 1 (0B3AAA4C)](all04dmd-teams.md#team-0b3aaa4c).
2. Supply reinforcement team [Oil Derreck 2 (0B3AA59C)](all04dmd-teams.md#team-0b3aa59c).
3. Supply reinforcement team [Oil Derreck 3 (0B3AFEFC)](all04dmd-teams.md#team-0b3afefc).
4. Supply reinforcement team [Oil Derreck 4 (0B3AFA4C)](all04dmd-teams.md#team-0b3afa4c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8201, Events line 8345, Actions line 8489.

<a id="trigger-08877e1c"></a>

### 21. It's OVER! - 08877E1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08875CFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. local flag 3 (Obj1Complete) is set.

Flag writers in this mission: set local flag 3 (Obj1Complete) at [EinsRescue1 (08A2A46C)](#trigger-08a2a46c); set local flag 3 (Obj1Complete) at [EinsRescue2 (09EFDF3C)](#trigger-09efdf3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [It's Over! 2 (0682668C)](#trigger-0682668c).
2. Play sound Cheer.
3. Disable [It's OVER! (08877E1C)](#trigger-08877e1c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8202, Events line 8346, Actions line 8490.

<a id="trigger-0682668c"></a>

### 22. It's Over! 2 - 0682668C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [It's OVER! (08877E1C)](#trigger-08877e1c).

Attached scope: tag definitions 0682639C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound Cheer.
2. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8203, Events line 8347, Actions line 8491.

<a id="trigger-088801bc"></a>

### 23. Engineer Dead? - 088801BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08875A7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Engineer Delay (0AEBEF3C)](#trigger-0aebef3c).
2. Disable [Engineer Dead? (088801BC)](#trigger-088801bc).
3. Disable [Engineer Dead? (088801BC)](#trigger-088801bc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8204, Events line 8348, Actions line 8492.

<a id="trigger-0888103c"></a>

### 24. 2nd Engineer Dead? - 0888103C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 088804DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [2nd Engineer Delay (0B24930C)](#trigger-0b24930c).
2. Disable [2nd Engineer Dead? (0888103C)](#trigger-0888103c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8205, Events line 8349, Actions line 8493.

<a id="trigger-0897db9c"></a>

### 25. Y MB Guards - 0897DB9C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0897D2FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Y MB Guard 1 (089795DC)](all04dmd-teams.md#team-089795dc) at waypoint 17 (cell 129, 46).
2. Supply reinforcement team [Y MB Guard 2 (0897B4CC)](all04dmd-teams.md#team-0897b4cc) at waypoint 19 (cell 135, 54).
3. Supply reinforcement team [Y MB Guard 3 (0897CEFC)](all04dmd-teams.md#team-0897cefc) at waypoint 21 (cell 145, 54).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8206, Events line 8350, Actions line 8494.

<a id="trigger-08a2a46c"></a>

### 26. EinsRescue1 - 08A2A46C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Rescued (O) (092711DC)](#trigger-092711dc).

Attached scope: tag definitions 08A29E4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Obj2 Complete) is clear.
2. local flag 1 (PsychicDomKilled) is clear.

Flag writers in this mission: set local flag 10 (Obj2 Complete) at [Yuri's Gone (07C9797C)](#trigger-07c9797c); set local flag 1 (PsychicDomKilled) at [Psychic Dominator KILLED (0A82A2EC)](#trigger-0a82a2ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PsyDomiV0 (08E7DCFC)](#trigger-08e7dcfc).
2. Disable [Mission Obj 1 (0A6CFA2C)](#trigger-0a6cfa2c).
3. Enable and reset applicable timers for [Mission Obj 2 (0B44B2CC)](#trigger-0b44b2cc).
4. Set local flag 3 (Obj1Complete).
5. Disable [Rescue Einstein! (0AB1EF3C)](#trigger-0ab1ef3c).
6. Disable [EinsRescue2 (09EFDF3C)](#trigger-09efdf3c).
7. Disable [Mission Obj 1c (0DE1DF3C)](#trigger-0de1df3c).
8. Disable player input.
9. Disable [EinsRescue3 (07BC56CC)](#trigger-07bc56cc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8207, Events line 8351, Actions line 8495.

<a id="trigger-08e7dcfc"></a>

### 27. PsyDomiV0 - 08E7DCFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [EinsRescue1 (08A2A46C)](#trigger-08a2a46c).

Attached scope: tag definitions 08E7D9EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (PsychicDomKilled) is clear.

Flag writers in this mission: set local flag 1 (PsychicDomKilled) at [Psychic Dominator KILLED (0A82A2EC)](#trigger-0a82a2ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 29 (cell 90, 103).
2. Supply reinforcement team [Einstein (0BB0D7DC)](all04dmd-teams.md#team-0bb0d7dc).
3. Supply reinforcement team [Einstein Helicopter Rescue (0BB0E7DC)](all04dmd-teams.md#team-0bb0e7dc).
4. Enable and reset applicable timers for [Einstein Timer 1 (079F1A6C)](#trigger-079f1a6c).
5. Play voice notification Mis_xA4_EinsteinSaved.
6. Enable and reset applicable timers for [Eva Well Done (068945AC)](#trigger-068945ac).
7. Enable and reset applicable timers for [PsyDomV1 (0C17497C)](#trigger-0c17497c).
8. Enable and reset applicable timers for [PD Doesn't Exist (05ABD16C)](#trigger-05abd16c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8208, Events line 8352, Actions line 8496.

<a id="trigger-0b44b2cc"></a>

### 28. Mission Obj 2 - 0B44B2CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [EinsRescue1 (08A2A46C)](#trigger-08a2a46c); enable from [EinsRescue2 (09EFDF3C)](#trigger-09efdf3c).

Attached scope: tag definitions 0B44F86C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Destroy Yuri's main base in the East” (MISSION:DestroyYuri04A).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8209, Events line 8353, Actions line 8497.

<a id="trigger-09efdf3c"></a>

### 29. EinsRescue2 - 09EFDF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Rescued (O) (092711DC)](#trigger-092711dc).

Attached scope: tag definitions 09EFDDEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Obj2 Complete) is clear.
2. local flag 1 (PsychicDomKilled) is set.

Flag writers in this mission: set local flag 10 (Obj2 Complete) at [Yuri's Gone (07C9797C)](#trigger-07c9797c); set local flag 1 (PsychicDomKilled) at [Psychic Dominator KILLED (0A82A2EC)](#trigger-0a82a2ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PsyDomV2 (09EFB69C)](#trigger-09efb69c).
2. Disable [Mission Obj 1 (0A6CFA2C)](#trigger-0a6cfa2c).
3. Enable and reset applicable timers for [Mission Obj 2 (0B44B2CC)](#trigger-0b44b2cc).
4. Set local flag 3 (Obj1Complete).
5. Disable player input.
6. Disable [Rescue Einstein! (0AB1EF3C)](#trigger-0ab1ef3c).
7. Disable [EinsRescue1 (08A2A46C)](#trigger-08a2a46c).
8. Disable [EinsRescue3 (07BC56CC)](#trigger-07bc56cc).
9. Disable [Mission Obj 1c (0DE1DF3C)](#trigger-0de1df3c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8210, Events line 8354, Actions line 8498.

<a id="trigger-07bc56cc"></a>

### 30. EinsRescue3 - 07BC56CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Rescued (O) (092711DC)](#trigger-092711dc).

Attached scope: tag definitions 07C9780C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Obj2 Complete) is set.

Flag writers in this mission: set local flag 10 (Obj2 Complete) at [Yuri's Gone (07C9797C)](#trigger-07c9797c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable player input.
2. Jump the camera to waypoint 29 (cell 90, 103).
3. Supply reinforcement team [Einstein (0BB0D7DC)](all04dmd-teams.md#team-0bb0d7dc).
4. Supply reinforcement team [Einstein Helicopter Rescue (0BB0E7DC)](all04dmd-teams.md#team-0bb0e7dc).
5. Enable and reset applicable timers for [Einstein Timer 3 (0A2FCF3C)](#trigger-0a2fcf3c).
6. Play voice notification Mis_xA4_EinsteinSaved.
7. Enable and reset applicable timers for [Eva Well Done (068945AC)](#trigger-068945ac).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8211, Events line 8355, Actions line 8499.

<a id="trigger-079f1a6c"></a>

### 31. Einstein Timer 1 - 079F1A6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomiV0 (08E7DCFC)](#trigger-08e7dcfc).

Attached scope: tag definitions 079F198C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Einstein (0BB0D7DC)](all04dmd-teams.md#team-0bb0d7dc).
2. Remove instances of the team organization (not automatically its surviving objects) [Einstein Helicopter Rescue (0BB0E7DC)](all04dmd-teams.md#team-0bb0e7dc).
3. Create/recruit team [Einstein 3 (0B0637DC)](all04dmd-teams.md#team-0b0637dc).
4. Enable and reset applicable timers for [Control Back (092C67FC)](#trigger-092c67fc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8212, Events line 8356, Actions line 8500.

<a id="trigger-068945ac"></a>

### 32. Eva Well Done - 068945AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomiV0 (08E7DCFC)](#trigger-08e7dcfc); enable from [EinsRescue3 (07BC56CC)](#trigger-07bc56cc); enable from [PsyDomV2 (09EFB69C)](#trigger-09efb69c).

Attached scope: tag definitions 06894F0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA4_EvaEinstienRescued.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8213, Events line 8357, Actions line 8501.

<a id="trigger-0c17497c"></a>

### 33. PsyDomV1 - 0C17497C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomiV0 (08E7DCFC)](#trigger-08e7dcfc).

Attached scope: tag definitions 0C17509C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 12 (EinsteinIn) is set.

**Then perform these actions in order:**

1. Play full-screen movie 17.
2. Enable and reset applicable timers for [PsyDomV1b (0B425AEC)](#trigger-0b425aec).
3. Disable [PsyDomV2 (09EFB69C)](#trigger-09efb69c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8214, Events line 8358, Actions line 8502.

<a id="trigger-05abd16c"></a>

### 34. PD Doesn't Exist - 05ABD16C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomiV0 (08E7DCFC)](#trigger-08e7dcfc).

Attached scope: tag definitions 05ABFC2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 315 (global list position: CATIME). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Stop the visible mission timer.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8215, Events line 8359, Actions line 8503.

<a id="trigger-09efb69c"></a>

### 35. PsyDomV2 - 09EFB69C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [EinsRescue2 (09EFDF3C)](#trigger-09efdf3c).

Attached scope: tag definitions 0B425F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (PsychicDomKilled) is set.

Flag writers in this mission: set local flag 1 (PsychicDomKilled) at [Psychic Dominator KILLED (0A82A2EC)](#trigger-0a82a2ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 29 (cell 90, 103).
2. Supply reinforcement team [Einstein (0BB0D7DC)](all04dmd-teams.md#team-0bb0d7dc).
3. Supply reinforcement team [Einstein Helicopter Rescue (0BB0E7DC)](all04dmd-teams.md#team-0bb0e7dc).
4. Disable [PsyDomiV0 (08E7DCFC)](#trigger-08e7dcfc).
5. Enable and reset applicable timers for [Einstein Timer 2 (0913B68C)](#trigger-0913b68c).
6. Play voice notification Mis_xA4_EinsteinSaved.
7. Enable and reset applicable timers for [Eva Well Done (068945AC)](#trigger-068945ac).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8216, Events line 8360, Actions line 8504.

<a id="trigger-0a2fcf3c"></a>

### 36. Einstein Timer 3 - 0A2FCF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [EinsRescue3 (07BC56CC)](#trigger-07bc56cc).

Attached scope: tag definitions 0A2FBB8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Einstein (0BB0D7DC)](all04dmd-teams.md#team-0bb0d7dc).
2. Remove instances of the team organization (not automatically its surviving objects) [Einstein Helicopter Rescue (0BB0E7DC)](all04dmd-teams.md#team-0bb0e7dc).
3. Create/recruit team [Einstein 3a (0780644C)](all04dmd-teams.md#team-0780644c).
4. Enable and reset applicable timers for [We Won! (0A2F818C)](#trigger-0a2f818c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8217, Events line 8361, Actions line 8505.

<a id="trigger-092c67fc"></a>

### 37. Control Back - 092C67FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Timer 1 (079F1A6C)](#trigger-079f1a6c); enable from [Einstein Timer 2 (0913B68C)](#trigger-0913b68c).

Attached scope: tag definitions 092C3C0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 18 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Enable and reset applicable timers for [Easy-Med Bonus (076EB1BC)](#trigger-076eb1bc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8218, Events line 8362, Actions line 8506.

<a id="trigger-0b425aec"></a>

### 38. PsyDomV1b - 0B425AEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomV1 (0C17497C)](#trigger-0c17497c).

Attached scope: tag definitions 0B4257EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Reveal Yuri Base (07677F3C)](#trigger-07677f3c).
2. Jump the camera to waypoint 50 (cell 140, 42).
3. Play voice notification Mis_xA4_EvaDestroyYuriBase.
4. Create radar-event marker type 1 at waypoint 50 (cell 140, 42).
5. Enable and reset applicable timers for [PsyDomV1c (0B425E5C)](#trigger-0b425e5c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8219, Events line 8363, Actions line 8507.

<a id="trigger-0913b68c"></a>

### 39. Einstein Timer 2 - 0913B68C

Owner reference: Germans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomV2 (09EFB69C)](#trigger-09efb69c).

Attached scope: tag definitions 0914307C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Einstein (0BB0D7DC)](all04dmd-teams.md#team-0bb0d7dc).
2. Remove instances of the team organization (not automatically its surviving objects) [Einstein Helicopter Rescue (0BB0E7DC)](all04dmd-teams.md#team-0bb0e7dc).
3. Create/recruit team [Einstein 3a (0780644C)](all04dmd-teams.md#team-0780644c).
4. Enable and reset applicable timers for [Control Back (092C67FC)](#trigger-092c67fc).
5. Enable and reset applicable timers for [PsyDomV2b (0BC5FB3C)](#trigger-0bc5fb3c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8220, Events line 8364, Actions line 8508.

<a id="trigger-0a2f818c"></a>

### 40. We Won! - 0A2F818C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Timer 3 (0A2FCF3C)](#trigger-0a2fcf3c).

Attached scope: tag definitions 0A2FA77C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner.
2. Play sound Cheer.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8221, Events line 8365, Actions line 8509.

<a id="trigger-076eb1bc"></a>

### 41. Easy-Med Bonus - 076EB1BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Control Back (092C67FC)](#trigger-092c67fc).

Attached scope: tag definitions 076ECC3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 29 (cell 90, 103).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8222, Events line 8366, Actions line 8510.

<a id="trigger-07677f3c"></a>

### 42. Reveal Yuri Base - 07677F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomV1b (0B425AEC)](#trigger-0b425aec); enable from [PsyDomV2b (0BC5FB3C)](#trigger-0bc5fb3c).

Attached scope: tag definitions 076748CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 52 (cell 144, 38).
2. Reveal terrain around waypoint 3 (cell 144, 32).
3. Reveal terrain around waypoint 50 (cell 140, 42).
4. Reveal terrain around waypoint 49 (cell 133, 36).
5. Reveal terrain around waypoint 51 (cell 155, 45).
6. Reveal terrain around waypoint 22 (cell 149, 54).
7. Reveal terrain around waypoint 21 (cell 145, 54).
8. Reveal terrain around waypoint 20 (cell 139, 54).
9. Reveal terrain around waypoint 19 (cell 135, 54).
10. Reveal terrain around waypoint 15 (cell 135, 50).
11. Reveal terrain around waypoint 17 (cell 129, 46).
12. Reveal terrain around waypoint 18 (cell 129, 42).
13. Reveal terrain around waypoint 53 (cell 130, 51).
14. Reveal terrain around waypoint 54 (cell 139, 28).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8223, Events line 8367, Actions line 8511.

<a id="trigger-0b425e5c"></a>

### 43. PsyDomV1c - 0B425E5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomV1b (0B425AEC)](#trigger-0b425aec).

Attached scope: tag definitions 0B425BDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 24 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA4_EvaDominatorDescribed.
2. Enable and reset applicable timers for [_Yuri - Einstein Escapes (0933A38C)](#trigger-0933a38c).
3. Enable and reset applicable timers for [New Timer for PD (0C154F3C)](#trigger-0c154f3c).
4. Enable and reset applicable timers for [Countdown to PD Gone (0934528C)](#trigger-0934528c).
5. Enable and reset applicable timers for [Countdown to PD Gone Easy (0C6AE29C)](#trigger-0c6ae29c).
6. Enable and reset applicable timers for [Countdown to PD Gone Hard (0C6A87FC)](#trigger-0c6a87fc).
7. Switch the sidebar to tab 1.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8224, Events line 8368, Actions line 8512.

<a id="trigger-0bc5fb3c"></a>

### 44. PsyDomV2b - 0BC5FB3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Timer 2 (0913B68C)](#trigger-0913b68c).

Attached scope: tag definitions 0BC5FA5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Reveal Yuri Base (07677F3C)](#trigger-07677f3c).
2. Jump the camera to waypoint 50 (cell 140, 42).
3. Play voice notification Mis_xA4_EvaDestroyYuriBase.
4. Create radar-event marker type 1 at waypoint 50 (cell 140, 42).
5. Enable and reset applicable timers for [_Yuri - Einstein Escapes (0933A38C)](#trigger-0933a38c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8225, Events line 8369, Actions line 8513.

<a id="trigger-0933a38c"></a>

### 45. _Yuri - Einstein Escapes - 0933A38C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomV1c (0B425E5C)](#trigger-0b425e5c); enable from [PsyDomV2b (0BC5FB3C)](#trigger-0bc5fb3c).

Attached scope: tag definitions 09339E7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA4_YuriTaunt.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8226, Events line 8370, Actions line 8514.

<a id="trigger-0c154f3c"></a>

### 46. New Timer for PD - 0C154F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomV1c (0B425E5C)](#trigger-0b425e5c).

Attached scope: tag definitions 0C15496C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Superweapon Set Recharge Time; main setting 7; location/duration field 9000.
2. Enable and reset applicable timers for [Bye Bye PD (092CC78C)](#trigger-092cc78c).
3. Enable and reset applicable timers for [Bye Bye PD Easy (0C6AE6CC)](#trigger-0c6ae6cc).
4. Enable and reset applicable timers for [Bye Bye PD Hard (0C6A8BFC)](#trigger-0c6a8bfc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8227, Events line 8371, Actions line 8515.

<a id="trigger-0934528c"></a>

### 47. Countdown to PD Gone - 0934528C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomV1c (0B425E5C)](#trigger-0b425e5c).

Attached scope: tag definitions 09343A3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 302 configured time units.
2. Use countdown label “Psychic Dominator Self Destruct” (MISSION:DominatorSelfDestruct).
3. Start the visible mission timer.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8228, Events line 8372, Actions line 8516.

<a id="trigger-0c6ae29c"></a>

### 48. Countdown to PD Gone Easy - 0C6AE29C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomV1c (0B425E5C)](#trigger-0b425e5c).

Attached scope: tag definitions 0C6AE1BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 482 configured time units.
2. Use countdown label “Psychic Dominator Self Destruct” (MISSION:DominatorSelfDestruct).
3. Start the visible mission timer.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8229, Events line 8373, Actions line 8517.

<a id="trigger-0c6a87fc"></a>

### 49. Countdown to PD Gone Hard - 0C6A87FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsyDomV1c (0B425E5C)](#trigger-0b425e5c).

Attached scope: tag definitions 0C6A85BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 122 configured time units.
2. Use countdown label “Psychic Dominator Self Destruct” (MISSION:DominatorSelfDestruct).
3. Start the visible mission timer.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8230, Events line 8374, Actions line 8518.

<a id="trigger-092cc78c"></a>

### 50. Bye Bye PD - 092CC78C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [New Timer for PD (0C154F3C)](#trigger-0c154f3c).

Attached scope: tag definitions 092CC24C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Destroy This (0779A30C)](#trigger-0779a30c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8231, Events line 8375, Actions line 8519.

<a id="trigger-0c6ae6cc"></a>

### 51. Bye Bye PD Easy - 0C6AE6CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [New Timer for PD (0C154F3C)](#trigger-0c154f3c).

Attached scope: tag definitions 0C6AE55C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 480 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Destroy This (0779A30C)](#trigger-0779a30c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8232, Events line 8376, Actions line 8520.

<a id="trigger-0c6a8bfc"></a>

### 52. Bye Bye PD Hard - 0C6A8BFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [New Timer for PD (0C154F3C)](#trigger-0c154f3c).

Attached scope: tag definitions 0C6A8A8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Destroy This (0779A30C)](#trigger-0779a30c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8233, Events line 8377, Actions line 8521.

<a id="trigger-0779a30c"></a>

### 53. Destroy This - 0779A30C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change House (0AA95F3C)](#trigger-0aa95f3c).

Incoming activation links: enable from [Bye Bye PD (092CC78C)](#trigger-092cc78c); enable from [Bye Bye PD Easy (0C6AE6CC)](#trigger-0c6ae6cc); enable from [Bye Bye PD Hard (0C6A8BFC)](#trigger-0c6a8bfc).

Attached scope: Psychic Dominator (YAPPET), owner Arabs, cell (83, 93), tag 0A82822C, persistence mode 2.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8234, Events line 8378, Actions line 8522.

<a id="trigger-0aa95f3c"></a>

### 54. Change House - 0AA95F3C

Owner reference: YuriCountry2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Psychic Dominator KILLED (0A82A2EC)](#trigger-0a82a2ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Obj1Complete) is set.

Flag writers in this mission: set local flag 3 (Obj1Complete) at [EinsRescue1 (08A2A46C)](#trigger-08a2a46c); set local flag 3 (Obj1Complete) at [EinsRescue2 (09EFDF3C)](#trigger-09efdf3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Disable [Psychic Dominator KILLED (0A82A2EC)](#trigger-0a82a2ec).
3. Remove instances of the team organization (not automatically its surviving objects) [Y SB Guard 1 (0B25259C)](all04dmd-teams.md#team-0b25259c).
4. Remove instances of the team organization (not automatically its surviving objects) [Y SB Guard 2 (0B253EFC)](all04dmd-teams.md#team-0b253efc).
5. Disable [Change House (0AA95F3C)](#trigger-0aa95f3c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8235, Events line 8379, Actions line 8523.

<a id="trigger-0a82a2ec"></a>

### 55. Psychic Dominator KILLED - 0A82A2EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 1 (PsychicDomKilled).
2. Disable [Change House (0AA95F3C)](#trigger-0aa95f3c).
3. Remove instances of the team organization (not automatically its surviving objects) [Y SB Guard 1 (0B25259C)](all04dmd-teams.md#team-0b25259c).
4. Remove instances of the team organization (not automatically its surviving objects) [Y SB Guard 2 (0B253EFC)](all04dmd-teams.md#team-0b253efc).
5. Enable and reset applicable timers for [Kill SB Front Guards (091D8F3C)](#trigger-091d8f3c).
6. Disable [Psychic Dominator KILLED (0A82A2EC)](#trigger-0a82a2ec).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8236, Events line 8380, Actions line 8524.

<a id="trigger-091d8f3c"></a>

### 56. Kill SB Front Guards - 091D8F3C

Owner reference: YuriCountry2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Psychic Dominator KILLED (0A82A2EC)](#trigger-0a82a2ec).

Attached scope: tag definitions 091D890C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Y SB Guard 1 (0B25259C)](all04dmd-teams.md#team-0b25259c).
2. Remove instances of the team organization (not automatically its surviving objects) [Y SB Guard 2 (0B253EFC)](all04dmd-teams.md#team-0b253efc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8237, Events line 8381, Actions line 8525.

<a id="trigger-068ea7ec"></a>

### 57. Y SB Guards - 068EA7EC

Owner reference: YuriCountry2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 068EA35C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Y SB Guard 1 (0B25259C)](all04dmd-teams.md#team-0b25259c) at waypoint 23 (cell 81, 90).
2. Supply reinforcement team [Y SB Guard 2 (0B253EFC)](all04dmd-teams.md#team-0b253efc) at waypoint 24 (cell 86, 90).
3. Supply reinforcement team [Y SB Back Guard (0B251DEC)](all04dmd-teams.md#team-0b251dec) at waypoint 30 (cell 73, 106).
4. Supply reinforcement team [Y SB Top Left Guard (0B25412C)](all04dmd-teams.md#team-0b25412c) at waypoint 33 (cell 73, 88).
5. Supply reinforcement team [Y SB Botm Rigt Guard (0B255B7C)](all04dmd-teams.md#team-0b255b7c) at waypoint 31 (cell 94, 106).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8238, Events line 8382, Actions line 8526.

<a id="trigger-068e27cc"></a>

### 58. Y Hover Team - 068E27CC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 068E247C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 500 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Y Hover Team (0C1E4B0C)](all04dmd-teams.md#team-0c1e4b0c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8239, Events line 8383, Actions line 8527.

<a id="trigger-09f7c5bc"></a>

### 59. It's Over : ( - 09F7C5BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09F7ADAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Announce defeat.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8240, Events line 8384, Actions line 8528.

<a id="trigger-0b19949c"></a>

### 60. Oil Under Attack - 0B19949C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gate (GAGATE_A), owner Russians, cell (164, 100), tag 0B19B9BC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck 1 (0B3AAA4C)](all04dmd-teams.md#team-0b3aaa4c).
2. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck 2 (0B3AA59C)](all04dmd-teams.md#team-0b3aa59c).
3. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck Tank 1 (0B3AF59C)](all04dmd-teams.md#team-0b3af59c).
4. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck Tank 2 (0B3ADEFC)](all04dmd-teams.md#team-0b3adefc).
5. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck Tank 3 (0B3ADA4C)](all04dmd-teams.md#team-0b3ada4c).
6. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck Tank 4 (0B3AD59C)](all04dmd-teams.md#team-0b3ad59c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8241, Events line 8385, Actions line 8529.

<a id="trigger-0b19f0fc"></a>

### 61. Oil Under Attack 2 - 0B19F0FC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gate (GAGATE_A), owner Russians, cell (174, 84), tag 0B18A37C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck 3 (0B3AFEFC)](all04dmd-teams.md#team-0b3afefc).
2. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck 4 (0B3AFA4C)](all04dmd-teams.md#team-0b3afa4c).
3. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck Tank 1 (0B3AF59C)](all04dmd-teams.md#team-0b3af59c).
4. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck Tank 2 (0B3ADEFC)](all04dmd-teams.md#team-0b3adefc).
5. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck Tank 3 (0B3ADA4C)](all04dmd-teams.md#team-0b3ada4c).
6. Remove instances of the team organization (not automatically its surviving objects) [Oil Derreck Tank 4 (0B3AD59C)](all04dmd-teams.md#team-0b3ad59c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8242, Events line 8386, Actions line 8530.

<a id="trigger-0437eecc"></a>

### 62. Y Auto Hover 1 - 0437EECC

Owner reference: YuriCountry2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Y Auto Hover 1b Alt (0687F03C)](#trigger-0687f03c).

Attached scope: tag definitions 0437ECAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 300 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Supply reinforcement team [Y Auto Hover 1 (094146CC)](all04dmd-teams.md#team-094146cc).
2. Disable [Y Auto Hover 1 (0437EECC)](#trigger-0437eecc).
3. Enable and reset applicable timers for [Y Auto Hover 1b (0AE4A3CC)](#trigger-0ae4a3cc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8243, Events line 8387, Actions line 8531.

<a id="trigger-0ae4a3cc"></a>

### 63. Y Auto Hover 1b - 0AE4A3CC

Owner reference: YuriCountry2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Y Auto Hover 1 (0437EECC)](#trigger-0437eecc).

Attached scope: tag definitions 0AE3904C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (HoverDeliver) is set.

Flag writers in this mission: clear local flag 0 (HoverDeliver) at [Y Auto Hover 1b (0AE4A3CC)](#trigger-0ae4a3cc); clear local flag 0 (HoverDeliver) at [Y Auto Hover 1b Alt (0687F03C)](#trigger-0687f03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Y Auto Hover 1b (0C1E41AC)](all04dmd-teams.md#team-0c1e41ac).
2. Clear local flag 0 (HoverDeliver).
3. Disable [Y Auto Hover 1b (0AE4A3CC)](#trigger-0ae4a3cc).
4. Enable and reset applicable timers for [Y Auto Hover 1 Alt (068B050C)](#trigger-068b050c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8244, Events line 8388, Actions line 8532.

<a id="trigger-068b050c"></a>

### 64. Y Auto Hover 1 Alt - 068B050C

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Y Auto Hover 1b (0AE4A3CC)](#trigger-0ae4a3cc).

Attached scope: tag definitions 0685E4CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 500 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Supply reinforcement team [Y Auto Hover 1 Alt (09417B7C)](all04dmd-teams.md#team-09417b7c).
2. Disable [Y Auto Hover 1 Alt (068B050C)](#trigger-068b050c).
3. Enable and reset applicable timers for [Y Auto Hover 1b Alt (0687F03C)](#trigger-0687f03c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8245, Events line 8389, Actions line 8533.

<a id="trigger-0687f03c"></a>

### 65. Y Auto Hover 1b Alt - 0687F03C

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Y Auto Hover 1 Alt (068B050C)](#trigger-068b050c).

Attached scope: tag definitions 06897B0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (HoverDeliver) is set.

Flag writers in this mission: clear local flag 0 (HoverDeliver) at [Y Auto Hover 1b (0AE4A3CC)](#trigger-0ae4a3cc); clear local flag 0 (HoverDeliver) at [Y Auto Hover 1b Alt (0687F03C)](#trigger-0687f03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Y Auto Hover 1b Alt (0C1E78AC)](all04dmd-teams.md#team-0c1e78ac).
2. Clear local flag 0 (HoverDeliver).
3. Disable [Y Auto Hover 1b Alt (0687F03C)](#trigger-0687f03c).
4. Enable and reset applicable timers for [Y Auto Hover 1 (0437EECC)](#trigger-0437eecc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8246, Events line 8390, Actions line 8534.

<a id="trigger-0a35f42c"></a>

### 66. Destroy MB Guard 1 - 0A35F42C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (126, 46), tag 0A35ADDC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (126, 42), tag 0A35ADDC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Y MB Guard 1 (089795DC)](all04dmd-teams.md#team-089795dc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8247, Events line 8391, Actions line 8535.

<a id="trigger-0a35a47c"></a>

### 67. Destroy MB Guard 2 - 0A35A47C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (135, 56), tag 0A35A25C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (139, 56), tag 0A35A25C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Y MB Guard 2 (0897B4CC)](all04dmd-teams.md#team-0897b4cc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8248, Events line 8392, Actions line 8536.

<a id="trigger-0a365f3c"></a>

### 68. Destroy MB Guard 3 - 0A365F3C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (145, 56), tag 0A3656FC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (149, 56), tag 0A3656FC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Y MB Guard 3 (0897CEFC)](all04dmd-teams.md#team-0897cefc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8249, Events line 8393, Actions line 8537.

<a id="trigger-0acb6dbc"></a>

### 69. Y Auto Hover 2 - 0ACB6DBC

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ACB685C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 500 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Supply reinforcement team [Y Auto Hover 2 (0C1E6C8C)](all04dmd-teams.md#team-0c1e6c8c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8250, Events line 8394, Actions line 8538.

<a id="trigger-068c2c0c"></a>

### 70. Y Auto Hover 2b - 068C2C0C

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 068C233C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (HoverDeliver2) is set.

Flag writers in this mission: clear local flag 4 (HoverDeliver2) at [Y Auto Hover 2b (068C2C0C)](#trigger-068c2c0c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Y Auto Hover 2b (0C1E67DC)](all04dmd-teams.md#team-0c1e67dc).
2. Clear local flag 4 (HoverDeliver2).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8251, Events line 8395, Actions line 8539.

<a id="trigger-068d21dc"></a>

### 71. Oil Field Free - 068D21DC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Z_Trigger (0B99803C)](#trigger-0b99803c).

Attached scope: tag definitions 068D3F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Play voice notification Mis_xA4_EvaCaptureDerricks.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8252, Events line 8396, Actions line 8540.

<a id="trigger-0b99803c"></a>

### 72. Z_Trigger - 0B99803C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BA76B6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Oil Field Free (068D21DC)](#trigger-068d21dc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8253, Events line 8397, Actions line 8541.

<a id="trigger-091ff40c"></a>

### 73. End Hovers - 091FF40C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri War Factory (YAWEAP), owner YuriCountry, cell (137, 36), tag 0920056C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Destroy current instances of [Y Auto Hover 1 (0437EECC)](#trigger-0437eecc).
2. Destroy current instances of [Y Auto Hover 1 Alt (068B050C)](#trigger-068b050c).
3. Destroy current instances of [Y Auto Hover 1b (0AE4A3CC)](#trigger-0ae4a3cc).
4. Destroy current instances of [Y Auto Hover 2 (0ACB6DBC)](#trigger-0acb6dbc).
5. Destroy current instances of [Y Auto Hover 1b Alt (0687F03C)](#trigger-0687f03c).
6. Destroy current instances of [Y Auto Hover 2b (068C2C0C)](#trigger-068c2c0c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8254, Events line 8398, Actions line 8542.

<a id="trigger-0aac204c"></a>

### 74. Get The Derreck!! - 0AAC204C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reset Oil Hint (0778136C)](#trigger-0778136c).

Attached scope: tag definitions 0AAC7B8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 250 configured time units have elapsed since the trigger timer was initialized/reset.
2. The trigger owner's credits are below 1500.

**Then perform these actions in order:**

1. Play voice notification Mis_xA4_EvaOilFieldsToEast.
2. Display message “Hint: Send engineers into the oil derricks in the East to increase cash flow” (MISSION:DerrickHint).
3. Create radar-event marker type 1 at waypoint 97 (cell 172, 93).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8255, Events line 8399, Actions line 8543.

<a id="trigger-0925e3ec"></a>

### 75. Shut Up Eva! Oil - 0925E3EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tech Oil Derrick (CAOILD), owner Neutral, cell (162, 83), tag 0925D83C, persistence mode 0; Tech Oil Derrick (CAOILD), owner Neutral, cell (161, 100), tag 0925D83C, persistence mode 0; Tech Oil Derrick (CAOILD), owner Neutral, cell (178, 83), tag 0925D83C, persistence mode 0; Tech Oil Derrick (CAOILD), owner Neutral, cell (169, 94), tag 0925D83C, persistence mode 0; Tech Oil Derrick (CAOILD), owner Neutral, cell (173, 89), tag 0925D83C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Destroy current instances of [Get The Derreck!! (0AAC204C)](#trigger-0aac204c).
2. Destroy current instances of [Oil Field Free (068D21DC)](#trigger-068d21dc).
3. Set local flag 11 (Oil Derricks Taken).
4. All to Hunt: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8256, Events line 8400, Actions line 8544.

<a id="trigger-0920dedc"></a>

### 76. Oil Explodes! - 0920DEDC

Owner reference: YuriCountry2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Barrel (CAMISC02), owner Arabs, cell (84, 108), tag 0920D82C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Y SB Back Guard (0B251DEC)](all04dmd-teams.md#team-0b251dec).
2. Enable and reset applicable timers for [Miss Obj Einstein TXT (077BA89C)](#trigger-077ba89c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8257, Events line 8401, Actions line 8545.

<a id="trigger-077ba89c"></a>

### 77. Miss Obj Einstein TXT - 077BA89C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Oil Explodes! (0920DEDC)](#trigger-0920dedc).

Attached scope: tag definitions 077BA65C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Obj1Complete) is clear.

Flag writers in this mission: set local flag 3 (Obj1Complete) at [EinsRescue1 (08A2A46C)](#trigger-08a2a46c); set local flag 3 (Obj1Complete) at [EinsRescue2 (09EFDF3C)](#trigger-09efdf3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Display message “Objective: Rescue Einstein from Yuri's secret base near the Great Pyramid” (MISSION:RescueEinstein).
2. Create radar-event marker type 1 at waypoint 29 (cell 90, 103).
3. Enable and reset applicable timers for [Easy - Flash Bio Reactors (076BB86C)](#trigger-076bb86c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8258, Events line 8402, Actions line 8546.

<a id="trigger-076bb86c"></a>

### 78. Easy - Flash Bio Reactors - 076BB86C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Miss Obj Einstein TXT (077BA89C)](#trigger-077ba89c).

Attached scope: tag definitions 076BB78C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 121 (cell 76, 92).
2. Reveal terrain around waypoint 122 (cell 76, 100).
3. Reveal terrain around waypoint 123 (cell 94, 92).
4. Reveal terrain around waypoint 124 (cell 94, 101).
5. Flash buildings of type YAPOWR; duration argument 90.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8259, Events line 8403, Actions line 8547.

<a id="trigger-0438464c"></a>

### 79. Kill SB Guard 1 - 0438464C

Owner reference: YuriCountry2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner Arabs, cell (80, 88), tag 043842BC, persistence mode 0; Gattling Cannon (YAGGUN), owner Arabs, cell (70, 97), tag 043842BC, persistence mode 0; Gattling Cannon (YAGGUN), owner Arabs, cell (71, 87), tag 043842BC, persistence mode 0; Gattling Cannon (YAGGUN), owner Arabs, cell (71, 107), tag 043842BC, persistence mode 0; Psychic Tower (YAPSYT), owner Arabs, cell (72, 99), tag 043842BC, persistence mode 0; Psychic Tower (YAPSYT), owner Arabs, cell (78, 106), tag 043842BC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Y SB Top Left Guard (0B25412C)](all04dmd-teams.md#team-0b25412c).
2. Disable [PT Warning 4 (084C6F3C)](#trigger-084c6f3c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8260, Events line 8404, Actions line 8548.

<a id="trigger-084c6f3c"></a>

### 80. PT Warning 4 - 084C6F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 15 tagged map cells: (80, 105), (80, 106), (73, 108), (80, 108), (73, 109), (80, 109), (74, 110), (80, 110), (75, 111), (76, 111), (80, 111), (77, 112), (78, 112), (79, 112), (80, 112); tag 084C66AC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 114 (cell 78, 106).
3. Display message “WARNING - Psychic Towers can mind control enemy units that get too close to them!” (MISSION:PsychicTowers).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8261, Events line 8405, Actions line 8549.

<a id="trigger-0438407c"></a>

### 81. Kill SB Guard 2 - 0438407C

Owner reference: YuriCountry2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner Arabs, cell (87, 88), tag 043844FC, persistence mode 0; Gattling Cannon (YAGGUN), owner Arabs, cell (97, 97), tag 043844FC, persistence mode 0; Gattling Cannon (YAGGUN), owner Arabs, cell (96, 87), tag 043844FC, persistence mode 0; Gattling Cannon (YAGGUN), owner Arabs, cell (96, 107), tag 043844FC, persistence mode 0; Psychic Tower (YAPSYT), owner Arabs, cell (95, 99), tag 043844FC, persistence mode 0; Psychic Tower (YAPSYT), owner Arabs, cell (91, 106), tag 043844FC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Y SB Botm Rigt Guard (0B255B7C)](all04dmd-teams.md#team-0b255b7c).
2. Disable [PT Warning 3 (084C7D2C)](#trigger-084c7d2c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8262, Events line 8406, Actions line 8550.

<a id="trigger-084c7d2c"></a>

### 82. PT Warning 3 - 084C7D2C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 17 tagged map cells: (87, 105), (87, 106), (86, 107), (96, 108), (87, 109), (96, 109), (88, 110), (96, 110), (96, 111), (89, 112), (90, 112), (91, 112), (95, 112), (92, 113), (93, 113), (94, 113), (95, 113); tag 084C769C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 115 (cell 91, 106).
3. Display message “WARNING - Psychic Towers can mind control enemy units that get too close to them!” (MISSION:PsychicTowers).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8263, Events line 8407, Actions line 8551.

<a id="trigger-092711dc"></a>

### 83. Einstein Rescued (O) - 092711DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Bio Reactor (YAPOWR), owner Arabs, cell (92, 90), tag 09275E6C, persistence mode 1; Bio Reactor (YAPOWR), owner Arabs, cell (92, 94), tag 09275E6C, persistence mode 1; Bio Reactor (YAPOWR), owner Arabs, cell (74, 90), tag 09275E6C, persistence mode 1; Bio Reactor (YAPOWR), owner Arabs, cell (74, 94), tag 09275E6C, persistence mode 1; Bio Reactor (YAPOWR), owner Arabs, cell (74, 102), tag 09275E6C, persistence mode 1; Bio Reactor (YAPOWR), owner Arabs, cell (92, 102), tag 09275E6C, persistence mode 1; Bio Reactor (YAPOWR), owner Arabs, cell (92, 98), tag 09275E6C, persistence mode 1; Bio Reactor (YAPOWR), owner Arabs, cell (74, 98), tag 09275E6C, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [EinsRescue1 (08A2A46C)](#trigger-08a2a46c).
2. Enable and reset applicable timers for [EinsRescue2 (09EFDF3C)](#trigger-09efdf3c).
3. Enable and reset applicable timers for [EinsRescue3 (07BC56CC)](#trigger-07bc56cc).
4. Enable and reset applicable timers for [Reset Oil Hint (0778136C)](#trigger-0778136c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8264, Events line 8408, Actions line 8552.

<a id="trigger-0778136c"></a>

### 84. Reset Oil Hint - 0778136C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Rescued (O) (092711DC)](#trigger-092711dc).

Attached scope: tag definitions 0777FF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 11 (Oil Derricks Taken) is clear.

Flag writers in this mission: set local flag 11 (Oil Derricks Taken) at [Shut Up Eva! Oil (0925E3EC)](#trigger-0925e3ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Get The Derreck!! (0AAC204C)](#trigger-0aac204c).
2. Enable and reset applicable timers for [Get The Derreck!! (0AAC204C)](#trigger-0aac204c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8265, Events line 8409, Actions line 8553.

<a id="trigger-092a7bbc"></a>

### 85. Flash Robot Control - 092A7BBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Flash Robot Control 1 (0A61B7EC)](#trigger-0a61b7ec).

Attached scope: tag definitions 092A721C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Switch the sidebar to tab 0.
2. Flash cameo/type GAROBO; additional configured duration/location argument 120.
3. Play voice notification Unit_Eva_RobotControl.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8266, Events line 8410, Actions line 8554.

<a id="trigger-067f21dc"></a>

### 86. Tanya Die? - 067F21DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tanya's Coming! 3 (0958E03C)](#trigger-0958e03c).

Attached scope: tag definitions 067F5BBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Tanya (TANY) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Play full-screen movie 5.
2. Set local flag 2 (Tanya Dead).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8267, Events line 8411, Actions line 8555.

<a id="trigger-0931847c"></a>

### 87. Tanya Swim Hint Pt 2 - 0931847C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tanya Swim Hint Pt 1 (0D3A203C)](#trigger-0d3a203c).

Attached scope: tag definitions 0931BF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 8 (Tanya Crossed) is clear.
2. local flag 2 (Tanya Dead) is clear.

Flag writers in this mission: set local flag 8 (Tanya Crossed) at [Tanya Crossed (0DF6503C)](#trigger-0df6503c); set local flag 2 (Tanya Dead) at [Tanya Die? (067F21DC)](#trigger-067f21dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_xA4_TanyaSwimHint.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8268, Events line 8412, Actions line 8556.

<a id="trigger-0d3a203c"></a>

### 88. Tanya Swim Hint Pt 1 - 0D3A203C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 8 tagged map cells: (140, 108), (141, 108), (139, 109), (139, 110), (139, 111), (139, 112), (140, 112), (141, 112); tag 0D3AC4AC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Tanya Swim Hint Pt 2 (0931847C)](#trigger-0931847c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8269, Events line 8413, Actions line 8557.

<a id="trigger-0bdaba2c"></a>

### 89. Tanya No Psychic Hint - 0BDABA2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Introduce Psychic Towers (0BDA918C)](#trigger-0bda918c).

Attached scope: tag definitions 0BDA97EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Tanya Dead) is clear.

Flag writers in this mission: set local flag 2 (Tanya Dead) at [Tanya Die? (067F21DC)](#trigger-067f21dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Tanya No Psychic Hint 2 (0BDA96FC)](#trigger-0bda96fc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8270, Events line 8414, Actions line 8558.

<a id="trigger-0bda96fc"></a>

### 90. Tanya No Psychic Hint 2 - 0BDA96FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tanya No Psychic Hint (0BDABA2C)](#trigger-0bdaba2c).

Attached scope: tag definitions 0BDA94BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 22 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA4_TanyaResistHint.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8271, Events line 8415, Actions line 8559.

<a id="trigger-0bda918c"></a>

### 91. _Introduce Psychic Towers - 0BDA918C

Owner reference: YuriCountry2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tanya Crossed (0DF6503C)](#trigger-0df6503c).

Attached scope: Psychic Tower (YAPSYT), owner YuriCountry, cell (155, 46), tag 0BDAC7DC, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_PsychicTower.
2. Enable and reset applicable timers for [Tanya No Psychic Hint (0BDABA2C)](#trigger-0bdaba2c).
3. Disable [Mission Obj 1 (0A6CFA2C)](#trigger-0a6cfa2c).
4. Disable [Rescue Einstein! (0AB1EF3C)](#trigger-0ab1ef3c).
5. Disable [Mission Obj 1c (0DE1DF3C)](#trigger-0de1df3c).
6. Enable and reset applicable timers for [Mission Obj 1 (0A6CFA2C)](#trigger-0a6cfa2c).
7. Enable and reset applicable timers for [Mission Obj 1c (0DE1DF3C)](#trigger-0de1df3c).
8. Flash buildings of type YAPSYT; duration argument 90.
9. Enable and reset applicable timers for [_Introduce Psychic T Y (084DE39C)](#trigger-084de39c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8272, Events line 8416, Actions line 8560.

<a id="trigger-084de39c"></a>

### 92. _Introduce Psychic T Y - 084DE39C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Introduce Psychic Towers (0BDA918C)](#trigger-0bda918c).

Attached scope: tag definitions 084DA52C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash buildings of type YAPSYT; duration argument 90.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8273, Events line 8417, Actions line 8561.

<a id="trigger-0bbf6e9c"></a>

### 93. Friendly Dinos! - 0BBF6E9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BBF1E2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (InPlace1) is set.
2. local flag 6 (InPlace2) is set.
3. local flag 7 (InPlace3) is set.

Flag writers in this mission: set local flag 5 (InPlace1) at [InPlace1 (0BBF269C)](#trigger-0bbf269c); clear local flag 5 (InPlace1) at [InPlace1Undo (0BB758CC)](#trigger-0bb758cc); set local flag 6 (InPlace2) at [InPlace2 (093E103C)](#trigger-093e103c); clear local flag 6 (InPlace2) at [InPlace2Undo (093E803C)](#trigger-093e803c); set local flag 7 (InPlace3) at [InPlace3 (0941A27C)](#trigger-0941a27c); clear local flag 7 (InPlace3) at [InPlace3Undo (093E60DC)](#trigger-093e60dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play Anim At; main setting 254; location/duration field BV.
2. Supply chrono reinforcement team [_FriendlyDinos (093A031C)](all04dmd-teams.md#team-093a031c) at waypoint 73 (cell 19, 129).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8274, Events line 8418, Actions line 8562.

<a id="trigger-0bbf269c"></a>

### 94. InPlace1 - 0BBF269C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (17, 126); tag 0BB71D6C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 5 (InPlace1).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8275, Events line 8419, Actions line 8563.

<a id="trigger-0bb758cc"></a>

### 95. InPlace1Undo - 0BB758CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 8 tagged map cells: (16, 125), (17, 125), (18, 125), (16, 126), (18, 126), (16, 127), (17, 127), (18, 127); tag 0BB76A1C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 5 (InPlace1).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8276, Events line 8420, Actions line 8564.

<a id="trigger-093e103c"></a>

### 96. InPlace2 - 093E103C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (22, 128); tag 093E904C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 6 (InPlace2).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8277, Events line 8421, Actions line 8565.

<a id="trigger-093e803c"></a>

### 97. InPlace2Undo - 093E803C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 8 tagged map cells: (21, 127), (22, 127), (23, 127), (21, 128), (23, 128), (21, 129), (22, 129), (23, 129); tag 093E204C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 6 (InPlace2).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8278, Events line 8422, Actions line 8566.

<a id="trigger-0941a27c"></a>

### 98. InPlace3 - 0941A27C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (19, 133); tag 093E704C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 7 (InPlace3).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8279, Events line 8423, Actions line 8567.

<a id="trigger-093e60dc"></a>

### 99. InPlace3Undo - 093E60DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 8 tagged map cells: (18, 132), (19, 132), (20, 132), (18, 133), (20, 133), (18, 134), (19, 134), (20, 134); tag 09405C4C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 7 (InPlace3).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8280, Events line 8424, Actions line 8568.

<a id="trigger-0df6503c"></a>

### 100. Tanya Crossed - 0DF6503C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 220 tagged map cells: (156, 56), (156, 57), (156, 58), (156, 59), (156, 60), (156, 61), (156, 62), (156, 63), (156, 64), (156, 65), (156, 66), (157, 70), (157, 71), (157, 72), (148, 73), (149, 73), (150, 73), (151, 73), (152, 73), (153, 73), (154, 73), (155, 73), (156, 73), (157, 73), (148, 74), (149, 74), (148, 75), (147, 76), (148, 76), (147, 77), (147, 78), (147, 79), (147, 80), (147, 81), (147, 82), (147, 83), (147, 84), (147, 85), (147, 86), (147, 87), (147, 88), (147, 89), (147, 90), (147, 91), (147, 92), (147, 93), (146, 94), (147, 94), (130, 95), (131, 95), (132, 95), (133, 95), (134, 95), (135, 95), (136, 95), (137, 95), (138, 95), (139, 95), (140, 95), (141, 95), (142, 95), (143, 95), (144, 95), (145, 95), (146, 95), (147, 95), (129, 96), (129, 97), (129, 98), (129, 99), (126, 100), (127, 100), (128, 100), (129, 100), (126, 101), (126, 102), (126, 103), (126, 104), (126, 105), (126, 106), (125, 107), (126, 107), (122, 108), (123, 108), (124, 108), (125, 108), (122, 109), (118, 110), (119, 110), (120, 110), (121, 110), (122, 110), (115, 111), (116, 111), (117, 111), (118, 111), (113, 112), (114, 112), (115, 112), (116, 112), (112, 113), (113, 113), (114, 113), (48, 114), (49, 114), (50, 114), (51, 114), (52, 114), (53, 114), (54, 114), (55, 114), (56, 114), (57, 114), (58, 114), (59, 114), (60, 114), (61, 114), (62, 114), (63, 114), (64, 114), (65, 114), (66, 114), (67, 114), (68, 114), (69, 114), (70, 114), (71, 114), (72, 114), (73, 114), (74, 114), (75, 114), (76, 114), (77, 114), (78, 114), (79, 114), (80, 114), (81, 114), (82, 114), (83, 114), (84, 114), (85, 114), (86, 114), (87, 114), (88, 114), (89, 114), (90, 114), (91, 114), (92, 114), (93, 114), (94, 114), (95, 114), (96, 114), (97, 114), (98, 114), (99, 114), (100, 114), (101, 114), (102, 114), (103, 114), (104, 114), (105, 114), (106, 114), (107, 114), (108, 114), (109, 114), (110, 114), (111, 114), (112, 114), (48, 115), (48, 116), (48, 117), (48, 118), (48, 119), (48, 120), (48, 121), (39, 122), (40, 122), (41, 122), (42, 122), (43, 122), (44, 122), (45, 122), (46, 122), (47, 122), (48, 122), (39, 123), (39, 124), (39, 125), (39, 126), (39, 127), (39, 128), (39, 129), (39, 130), (39, 131), (34, 132), (35, 132), (36, 132), (37, 132), (38, 132), (39, 132), (34, 133), (34, 134), (34, 135), (34, 136), (34, 137), (34, 138), (34, 139), (34, 140), (34, 141), (34, 142), (34, 143), (34, 144), (34, 145), (34, 146), (34, 147), (34, 148), (34, 149), (33, 150), (34, 150), (33, 151); tag 0DF5804C, persistence mode 0.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 8 (Tanya Crossed).
2. Enable and reset applicable timers for [_Introduce Psychic Towers (0BDA918C)](#trigger-0bda918c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8281, Events line 8425, Actions line 8569.

<a id="trigger-094c7f3c"></a>

### 101. Create Tanks Guarding Oil - 094C7F3C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 094C766C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Oil Derreck Tank 1 (0B3AF59C)](all04dmd-teams.md#team-0b3af59c).
2. Supply reinforcement team [Oil Derreck Tank 4 (0B3AD59C)](all04dmd-teams.md#team-0b3ad59c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8282, Events line 8426, Actions line 8570.

<a id="trigger-093b41cc"></a>

### 102. _Easy Reinforcement 1 - 093B41CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 093B571C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 6.

**Then perform these actions in order:**

1. Supply reinforcement team [_Easy Reinforcements (0997621C)](all04dmd-teams.md#team-0997621c).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Enable and reset applicable timers for [_Easy 1 (08AEAF3C)](#trigger-08aeaf3c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8283, Events line 8427, Actions line 8571.

<a id="trigger-08aeaf3c"></a>

### 103. _Easy 1 - 08AEAF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Easy Reinforcement 1 (093B41CC)](#trigger-093b41cc).

Attached scope: tag definitions 08AEAE5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound GuardianGIAttackCommand.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8284, Events line 8428, Actions line 8572.

<a id="trigger-093b548c"></a>

### 104. _Easy Reinforcement 2 - 093B548C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 093B531C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 30.

**Then perform these actions in order:**

1. Supply reinforcement team [_Easy Reinforcment 2 (09975B7C)](all04dmd-teams.md#team-09975b7c).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Enable and reset applicable timers for [_Easy 2 (08AEAAFC)](#trigger-08aeaafc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8285, Events line 8429, Actions line 8573.

<a id="trigger-08aeaafc"></a>

### 105. _Easy 2 - 08AEAAFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Easy Reinforcement 2 (093B548C)](#trigger-093b548c).

Attached scope: tag definitions 08AEAA1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound SniperSelect.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8286, Events line 8430, Actions line 8574.

<a id="trigger-093b522c"></a>

### 106. _Easy Reinforcement 3 - 093B522C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 093B50BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  #: 4.

**Then perform these actions in order:**

1. Supply reinforcement team [_Easy Reinforcment 3 (08D1D32C)](all04dmd-teams.md#team-08d1d32c).
2. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8287, Events line 8431, Actions line 8575.

<a id="trigger-0686b36c"></a>

### 107. _Medium Power - 0686B36C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0686A7CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Medium Power CF (086197DC)](all04dmd-teams.md#team-086197dc).
2. Supply reinforcement team [Medium Power CI (0861943C)](all04dmd-teams.md#team-0861943c).
3. Supply reinforcement team [Medium Power CL (0861A65C)](all04dmd-teams.md#team-0861a65c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8288, Events line 8432, Actions line 8576.

<a id="trigger-0686a6dc"></a>

### 108. _Hard Power - 0686A6DC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0686A15C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Hard Power CG (0BA2423C)](all04dmd-teams.md#team-0ba2423c).
2. Supply reinforcement team [Hard Power CH (0BA245DC)](all04dmd-teams.md#team-0ba245dc).
3. Supply reinforcement team [Hard Power CK (0BA230CC)](all04dmd-teams.md#team-0ba230cc).
4. Supply reinforcement team [Hard Power CM (0BA2497C)](all04dmd-teams.md#team-0ba2497c).
5. Supply reinforcement team [Hard Power CP (0BA2410C)](all04dmd-teams.md#team-0ba2410c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8289, Events line 8433, Actions line 8577.

<a id="trigger-097ba1cc"></a>

### 109. Yuri's Harvesters - 097BA1CC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097BBD0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yuri Harvester 1 (0D89C48C)](all04dmd-teams.md#team-0d89c48c).
2. Supply reinforcement team [Yuri Harvester 2 (0D8A3EBC)](all04dmd-teams.md#team-0d8a3ebc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8290, Events line 8434, Actions line 8578.

<a id="trigger-0cf472bc"></a>

### 110. Cam to Pyramid - 0CF472BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CF43C7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 37 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 29 (cell 90, 103).
2. Jump the camera to waypoint 29 (cell 90, 103).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8291, Events line 8435, Actions line 8579.

<a id="trigger-0cf43a2c"></a>

### 111. Cam to Oil Derricks 1 - 0CF43A2C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CF437EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 11 (cell 171, 85).
2. Reveal terrain around waypoint 10 (cell 165, 86).
3. Reveal terrain around waypoint 14 (cell 180, 89).
4. Reveal terrain around waypoint 8 (cell 177, 85).
5. Reveal terrain around waypoint 12 (cell 173, 99).
6. Reveal terrain around waypoint 9 (cell 164, 95).
7. Reveal terrain around waypoint 5 (cell 163, 99).
8. Reveal terrain around waypoint 97 (cell 172, 93).
9. Jump the camera to waypoint 8 (cell 177, 85).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8292, Events line 8436, Actions line 8580.

<a id="trigger-0cf4362c"></a>

### 112. Cam Back Home - 0CF4362C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CF44C1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 59 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 0 (cell 82, 162).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8293, Events line 8437, Actions line 8581.

<a id="trigger-0cb1224c"></a>

### 113. Bonus Trigger - 0CB1224C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 18 tagged map cells: (14, 116), (15, 116), (16, 117), (17, 118), (17, 119), (16, 120), (17, 120), (17, 121), (17, 122), (16, 123), (17, 123), (10, 124), (11, 124), (12, 124), (13, 124), (14, 124), (15, 124), (16, 124); tag 0CB16E7C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Supply reinforcement team [Bonus Team (0C8608EC)](all04dmd-teams.md#team-0c8608ec).
2. Play sound SniperMove.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8294, Events line 8438, Actions line 8582.

<a id="trigger-0984d66c"></a>

### 114. Intro Robot Tank 1 - 0984D66C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0984D28C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 356 (global list position: Psychic Dominator (YAPPPT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Intro Robot Tank 2 (0970928C)](#trigger-0970928c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8295, Events line 8439, Actions line 8583.

<a id="trigger-0970928c"></a>

### 115. Intro Robot Tank 2 - 0970928C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Intro Robot Tank 1 (0984D66C)](#trigger-0984d66c).

Attached scope: tag definitions 0970AAAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Switch the sidebar to tab 3.
2. Flash cameo/type ROBO; additional configured duration/location argument 90.
3. Play voice notification Unit_Eva_RobotTank.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8296, Events line 8440, Actions line 8584.

<a id="trigger-079b254c"></a>

### 116. Camels Are Fun - 079B254C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079B3E7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 65 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A04_Camels AK (079AF23C)](all04dmd-teams.md#team-079af23c).
2. Create/recruit team [_A04_Camels CY (079B093C)](all04dmd-teams.md#team-079b093c).
3. Create/recruit team [_A04_Camels Z (092B87DC)](all04dmd-teams.md#team-092b87dc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8297, Events line 8441, Actions line 8585.

<a id="trigger-07a5f86c"></a>

### 117. _Start Oil Tanks 2 - 07A5F86C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A5F27C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Oil Derreck Tank 2 (0B3ADEFC)](all04dmd-teams.md#team-0b3adefc).
2. Supply reinforcement team [Oil Derreck Tank 3 (0B3ADA4C)](all04dmd-teams.md#team-0b3ada4c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8298, Events line 8442, Actions line 8586.

<a id="trigger-07ba407c"></a>

### 118. Mummy1 - 07BA407C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pyramid (CAEGYP02), owner Neutral, cell (77, 139), tag 07BA5C0C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A04_Mummy 1 (09070B7C)](all04dmd-teams.md#team-09070b7c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8299, Events line 8443, Actions line 8587.

<a id="trigger-07c78b2c"></a>

### 119. New Mission Objective - 07C78B2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C7979C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_NewMissionObjective.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8300, Events line 8444, Actions line 8588.

<a id="trigger-08fd26fc"></a>

### 120. Mummy 2 - 08FD26FC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pyramid (CAEGYP02), owner Neutral, cell (74, 61), tag 08FD034C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A04_Mummy 2 (090706CC)](all04dmd-teams.md#team-090706cc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8301, Events line 8445, Actions line 8589.

<a id="trigger-08fd092c"></a>

### 121. Mummy 3 - 08FD092C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pyramid (CAEGYP02), owner Neutral, cell (71, 77), tag 08FD06EC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A04_Mummy 3 (0907032C)](all04dmd-teams.md#team-0907032c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8302, Events line 8446, Actions line 8590.

<a id="trigger-08fd7e0c"></a>

### 122. Mummy 4 - 08FD7E0C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pyramid (CAEGYP02), owner Neutral, cell (93, 56), tag 08FD7BCC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A04_Mummy 4 (090701FC)](all04dmd-teams.md#team-090701fc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8303, Events line 8447, Actions line 8591.

<a id="trigger-07c383cc"></a>

### 123. Tanya's Coming! 1 - 07C383CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C3BC0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 75 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 18.
2. Enable and reset applicable timers for [Tanya's Coming! 2 (08FF115C)](#trigger-08ff115c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8304, Events line 8448, Actions line 8592.

<a id="trigger-08ff115c"></a>

### 124. Tanya's Coming! 2 - 08FF115C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tanya's Coming! 1 (07C383CC)](#trigger-07c383cc).

Attached scope: tag definitions 08FF4BAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A04_Tanya Intro (094FE68C)](all04dmd-teams.md#team-094fe68c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8305, Events line 8449, Actions line 8593.

<a id="trigger-0958e03c"></a>

### 125. Tanya's Coming! 3 - 0958E03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0958004C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (TanyaOut) is set.

**Then perform these actions in order:**

1. Play sound Tanya_NoFear.
2. Enable and reset applicable timers for [Tanya Die? (067F21DC)](#trigger-067f21dc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8306, Events line 8450, Actions line 8594.

<a id="trigger-0a2ef04c"></a>

### 126. Yuri Force Sell - 0A2EF04C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A2EE1CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 300 (global list position: Bus Stop (CASTRT05)). A map-local type-list change can affect index interpretation.
2. Building does not exist: type index 303 (global list position: Yuri Barracks (YABRCK)). A map-local type-list change can affect index interpretation.
3. Building does not exist: type index 302 (global list position: Bio Reactor (YAPOWR)). A map-local type-list change can affect index interpretation.
4. Low Power: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Yuri Force Sell 2 (0A2EB9BC)](#trigger-0a2eb9bc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8307, Events line 8451, Actions line 8595.

<a id="trigger-0a2eb9bc"></a>

### 127. Yuri Force Sell 2 - 0A2EB9BC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Force Sell (0A2EF04C)](#trigger-0a2ef04c).

Attached scope: tag definitions 0A2EF50C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Enable and reset applicable timers for [Yuri Force Sell 3 (077DCABC)](#trigger-077dcabc).
3. Enable and reset applicable timers for [Yuri Force Sell 3a (08FB958C)](#trigger-08fb958c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8308, Events line 8452, Actions line 8596.

<a id="trigger-077dcabc"></a>

### 128. Yuri Force Sell 3 - 077DCABC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Force Sell 2 (0A2EB9BC)](#trigger-0a2eb9bc).

Attached scope: tag definitions 077DC5CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8309, Events line 8453, Actions line 8597.

<a id="trigger-08fb958c"></a>

### 129. Yuri Force Sell 3a - 08FB958C

Owner reference: French. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Force Sell 2 (0A2EB9BC)](#trigger-0a2eb9bc).

Attached scope: tag definitions 08FBCF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 2 (country/type FRENCH; placed owner French).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8310, Events line 8454, Actions line 8598.

<a id="trigger-07c9797c"></a>

### 130. Yuri's Gone - 07C9797C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C973FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Set local flag 10 (Obj2 Complete).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8311, Events line 8455, Actions line 8599.

<a id="trigger-05fe018c"></a>

### 131. SideChanger - 05FE018C

Owner reference: French. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Psychic Dominator (YAPPET) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Change House: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8312, Events line 8456, Actions line 8600.

<a id="trigger-0ac0983c"></a>

### 132. Destroyed - 0AC0983C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [SideChanger (05FE018C)](#trigger-05fe018c).

Attached scope: Gattling Tank (YTNK), owner French, cell (138, 45), tag 07BC6D9C, persistence mode 0; Gattling Tank (YTNK), owner French, cell (137, 45), tag 07BC6D9C, persistence mode 0; Gattling Tank (YTNK), owner French, cell (136, 45), tag 07BC6D9C, persistence mode 0; Lasher Light Tank (LTNK), owner French, cell (136, 46), tag 07BC6D9C, persistence mode 0; Lasher Light Tank (LTNK), owner French, cell (137, 46), tag 07BC6D9C, persistence mode 0; Lasher Light Tank (LTNK), owner French, cell (138, 46), tag 07BC6D9C, persistence mode 0; Lasher Light Tank (LTNK), owner French, cell (136, 44), tag 07BC6D9C, persistence mode 0; Lasher Light Tank (LTNK), owner French, cell (137, 44), tag 07BC6D9C, persistence mode 0; Lasher Light Tank (LTNK), owner French, cell (138, 44), tag 07BC6D9C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [SideChanger (05FE018C)](#trigger-05fe018c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8313, Events line 8457, Actions line 8601.

<a id="trigger-0a2ba33c"></a>

### 133. PT Warning 1 - 0A2BA33C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 11 tagged map cells: (148, 55), (148, 56), (148, 57), (148, 58), (149, 59), (150, 60), (151, 61), (152, 61), (153, 61), (154, 61), (155, 61); tag 0A2CE10C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 116 (cell 153, 55).
2. Play sound WarningAlarm.
3. Display message “WARNING - Psychic Towers can mind control enemy units that get too close to them!” (MISSION:PsychicTowers).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8314, Events line 8458, Actions line 8602.

<a id="trigger-0a2c9f3c"></a>

### 134. PT Warning 2 - 0A2C9F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 20 tagged map cells: (136, 54), (136, 55), (136, 56), (147, 56), (136, 57), (147, 57), (137, 58), (147, 58), (138, 59), (146, 59), (147, 59), (139, 60), (145, 60), (146, 60), (140, 61), (141, 61), (142, 61), (143, 61), (144, 61), (145, 61); tag 0A2CE4BC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Reveal terrain around waypoint 117 (cell 142, 55).
3. Display message “WARNING - Psychic Towers can mind control enemy units that get too close to them!” (MISSION:PsychicTowers).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8315, Events line 8459, Actions line 8603.

<a id="trigger-0a61b7ec"></a>

### 135. Flash Robot Control 1 - 0A61B7EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A61B1CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 7 (global list position: Allied War Factory (GAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Flash Robot Control (092A7BBC)](#trigger-092a7bbc).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8316, Events line 8460, Actions line 8604.

<a id="trigger-084ff22c"></a>

### 136. Cam To River - 084FF22C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 084FE33C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 88 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 118 (cell 87, 117).
2. Jump the camera to waypoint 118 (cell 87, 117).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8317, Events line 8461, Actions line 8605.

<a id="trigger-084fe24c"></a>

### 137. Cam Home 4 Good - 084FE24C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 084FF59C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 0 (cell 82, 162) with speed setting 2.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8318, Events line 8462, Actions line 8606.

<a id="trigger-08b7415c"></a>

### 138. Cam to Oil Derricks 2 - 08B7415C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B7677C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 48 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 5 (cell 163, 99) with speed setting 2.

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8319, Events line 8463, Actions line 8607.

<a id="trigger-084d7a2c"></a>

### 139. Kill PT Warning 2 - 084D7A2C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner YuriCountry, cell (142, 55), tag 084D73BC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [PT Warning 2 (0A2C9F3C)](#trigger-0a2c9f3c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8320, Events line 8464, Actions line 8608.

<a id="trigger-084d3c1c"></a>

### 140. Kill PT Warning 1 - 084D3C1C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner YuriCountry, cell (153, 55), tag 084D39DC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [PT Warning 1 (0A2BA33C)](#trigger-0a2ba33c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8321, Events line 8465, Actions line 8609.

<a id="trigger-08fbcd8c"></a>

### 141. French Hate America - 08FBCD8C

Owner reference: French. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08FBC8BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8322, Events line 8466, Actions line 8610.

<a id="trigger-0865dcfc"></a>

### 142. _Easy Power - 0865DCFC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 086584EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Medium Power CN (0861A9FC)](all04dmd-teams.md#team-0861a9fc).
2. Supply reinforcement team [Medium Power CR (08619C8C)](all04dmd-teams.md#team-08619c8c).

Source locator: mapsmd03.mix/all04dmd.map; Triggers line 8323, Events line 8467, Actions line 8611.

[All team rosters and ordered plans](all04dmd-teams.md) | [All mission overrides](all04dmd-overrides.md)
