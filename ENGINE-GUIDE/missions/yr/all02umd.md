# Operation: Hollywood and Vain

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all02umd.map. **Effective extracted member:** expandmd01.mix/all02umd.map. **Trigger definitions:** 253.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all02umd-teams.md) | [All mission overrides](all02umd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Americans |
| Theater | NEWURBAN |
| Map size | 0,0,113,108 |
| Visible local rectangle | 5,6,102,93 |
| Placed vehicles | 130 |
| Placed infantry | 98 |
| Placed structures | 375 |
| Placed aircraft | 0 |
| Team templates | 199 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 150 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 600 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 0 | Africans |
| 6 | Arabs | 0 | Arabs |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 0 | Russians |
| 9 | YuriCountry | 600 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 750 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |
| 14 | Yuri2 | 1000 | Yuri2Country |
| 15 | Yuri3 | 1000 | Yuri3Country |
| 16 | Yuri4 | 1000 | Yuri4Country |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Base_Gone,0 |
| 1 | Grinders_Gone,0 |
| 2 | Grinder1_Gone,0 |
| 3 | Grinder2_Gone,0 |
| 4 | Grinder3_Gone,0 |
| 5 | Grinder4_Gone,0 |
| 6 | Player_Has_AC,0 |
| 7 | Player_Has_SpySat,0 |
| 8 | Player_Has_Radar,0 |
| 9 | Bridge1_Fixed,1 |
| 10 | Bridge2_Fixed,1 |
| 11 | Bridge3_Fixed,1 |
| 12 | Bridge4_Fixed,1 |
| 13 | Barrack1_Gone,0 |
| 14 | CheeseFact_Gone,0 |
| 15 | 3L1G_Built,0 |
| 16 | Grinder1_BF_Done,0 |
| 17 | Grinder1_BM_Done,0 |
| 18 | Grinder1_SF_Done,0 |
| 19 | Grinder1_GM_Done,0 |
| 20 | Grinder1_F_Done,0 |
| 21 | Grinder1_TM_Done,0 |
| 22 | IE_Building_Gone,0 |
| 23 | Change_G1BeachF,0 |
| 24 | IF_Building_Gone,0 |
| 25 | Change_G1BeachM,0 |
| 26 | Change_G1Female,0 |
| 27 | IG_Building_Gone,0 |
| 28 | IH_Building_Gone,0 |
| 29 | Change_G1Green,0 |
| 30 | II_Building_Gone,0 |
| 31 | Change_G1SnowFat,0 |
| 32 | IJ_Building_Gone,0 |
| 33 | Change_G1ThinM,0 |
| 34 | Change_G2BeachM,0 |
| 35 | Change_G2Female,0 |
| 36 | Change_G2ThinM,0 |
| 37 | Change_G2SnowF,0 |
| 38 | Change_G2SnowM,0 |
| 39 | Change_G2BeachF,0 |
| 40 | IK_Building_Gone,0 |
| 41 | IL_Building_Gone,0 |
| 42 | IM_Building_Gone,0 |
| 43 | IN_Building_Gone,0 |
| 44 | IO_Building_Gone,0 |
| 45 | IP_Building_Gone,0 |
| 46 | Change_G4SnowFat,0 |
| 47 | Change_G4BeachF,0 |
| 48 | Change_G4Female,0 |
| 49 | Change_G4BeachM,0 |
| 50 | Change_G4Green,0 |
| 51 | Change_G4SnowF,0 |
| 52 | Change_G4SnowM,0 |
| 53 | Change_G4ThinM,0 |
| 54 | Change_G4BeachFat,0 |
| 55 | JA_Building_Gone,0 |
| 56 | JB_Building_Gone,0 |
| 57 | JC_Building_Gone,0 |
| 58 | JD_Building_Gone,0 |
| 59 | JE_Building_Gone,0 |
| 60 | JF_Building_Gone,0 |
| 61 | JG_Building_Gone,0 |
| 62 | JH_Building_Gone,0 |
| 63 | JI_Building_Gone,0 |
| 64 | Flint_Found,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Mission_Over (0CDDC22C)](#trigger-0cddc22c) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner. |
| [PlayerLose (0460D72C)](#trigger-0460d72c) | Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).<br>5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |

## Every trigger, in file order

<a id="trigger-0916b4cc"></a>

### 1. Make_Cowboy - 0916B4CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0916B2AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Cowboy (0902E90C)](all02umd-teams.md#team-0902e90c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14244, Events line 14499, Actions line 14754.

<a id="trigger-0916204c"></a>

### 2. Discover_Cowboy - 0916204C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: force from [Force_Fire_Flint (0926703C)](#trigger-0926703c); enable from [Cowboy_Backup (0464860C)](#trigger-0464860c); enable from [Select_Flint (07A40B2C)](#trigger-07a40b2c); enable from [Discover_Trigger (09D2968C)](#trigger-09d2968c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 64 (Flint_Found) is clear.

Flag writers in this mission: set local flag 64 (Flint_Found) at [Discover_Cowboy (0916204C)](#trigger-0916204c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Reveal terrain around waypoint 208 (cell 157, 123).
3. Set local flag 64 (Flint_Found).
4. Wakeup self; main setting 0.
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_Cowboy (0902E90C)](all02umd-teams.md#team-0902e90c).
6. Create/recruit team [TEAM_Flash_Cowboy (0903959C)](all02umd-teams.md#team-0903959c).
7. Enable and reset applicable timers for [Wakeup_Cowboy_Victims (09164ACC)](#trigger-09164acc).
8. Disable [Discover_Cowboy (0916204C)](#trigger-0916204c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14245, Events line 14500, Actions line 14755.

<a id="trigger-09164acc"></a>

### 3. Wakeup_Cowboy_Victims - 09164ACC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Discover_Cowboy (0916204C)](#trigger-0916204c).

Attached scope: tag definitions 0B90971C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Cowboy_Victims (0902D03C)](all02umd-teams.md#team-0902d03c).
2. Play voice notification Mis_xA2_EvaFoundClint.
3. Enable and reset applicable timers for [Activate_Cheese1 (045E609C)](#trigger-045e609c).
4. Enable and reset applicable timers for [Carville_Comment (05D9EE6C)](#trigger-05d9ee6c).
5. Disable [Wakeup_Cowboy_Victims (09164ACC)](#trigger-09164acc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14246, Events line 14501, Actions line 14756.

<a id="trigger-045e609c"></a>

### 4. Activate_Cheese1 - 045E609C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Wakeup_Cowboy_Victims (09164ACC)](#trigger-09164acc).

Attached scope: tag definitions 045E1B1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_2L1Y_Cheese1 (0EB3AB7C)](all02umd-teams.md#team-0eb3ab7c).
2. Enable and reset applicable timers for [Activate_Cheese2 (045E003C)](#trigger-045e003c).
3. Enable and reset applicable timers for [Yuri2_Gone (09635F3C)](#trigger-09635f3c).
4. Enable and reset applicable timers for [Main_Yuri_gone (0CEBD51C)](#trigger-0cebd51c).
5. Enable and reset applicable timers for [Grinder1_BeachFemale (0C745F3C)](#trigger-0c745f3c).
6. Enable and reset applicable timers for [Grinder2_ThinMale (0978639C)](#trigger-0978639c).
7. Enable and reset applicable timers for [Grinder4_SnowFat (097FD60C)](#trigger-097fd60c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14247, Events line 14502, Actions line 14757.

<a id="trigger-05d9ee6c"></a>

### 5. Carville_Comment - 05D9EE6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Wakeup_Cowboy_Victims (09164ACC)](#trigger-09164acc).

Attached scope: tag definitions 05D9C5DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 9.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14248, Events line 14503, Actions line 14758.

<a id="trigger-045e003c"></a>

### 6. Activate_Cheese2 - 045E003C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Activate_Cheese1 (045E609C)](#trigger-045e609c).

Attached scope: tag definitions 045E43DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Cheese2 (0C5AADEC)](all02umd-teams.md#team-0c5aadec).
2. Enable and reset applicable timers for [Tank_Cheese1 (09588C1C)](#trigger-09588c1c).
3. Enable and reset applicable timers for [Lame_Cheese_Tank1 (10CF24FC)](#trigger-10cf24fc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14249, Events line 14504, Actions line 14759.

<a id="trigger-09635f3c"></a>

### 7. Yuri2_Gone - 09635F3C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Activate_Cheese1 (045E609C)](#trigger-045e609c).

Attached scope: tag definitions 09635A1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Grinders_Gone) is set.
2. Building does not exist: type index 303 (global list position: Yuri Barracks (YABRCK)). A map-local type-list change can affect index interpretation.
3. Building does not exist: type index 302 (global list position: Bio Reactor (YAPOWR)). A map-local type-list change can affect index interpretation.

Flag writers in this mission: set local flag 1 (Grinders_Gone) at [Check_Grinders (0C42981C)](#trigger-0c42981c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Yuri2_SellOff (07A3955C)](#trigger-07a3955c).
2. All to Hunt: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14250, Events line 14505, Actions line 14760.

<a id="trigger-0cebd51c"></a>

### 8. Main_Yuri_gone - 0CEBD51C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Activate_Cheese1 (045E609C)](#trigger-045e609c).

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (92, 112), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (86, 113), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (59, 121), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (100, 108), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (107, 108), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (117, 93), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (119, 81), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (100, 78), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (99, 88), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (92, 97), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (83, 102), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (59, 129), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (47, 127), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (40, 127), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (55, 107), tag 0CEBD1DC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (49, 104), tag 0CEBD1DC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  #: 24.
2. Building does not exist: type index 311 (global list position: Industrial Plant (NAINDP)). A map-local type-list change can affect index interpretation.
3. Building does not exist: type index 303 (global list position: Yuri Barracks (YABRCK)). A map-local type-list change can affect index interpretation.
4. Building does not exist: type index 302 (global list position: Bio Reactor (YAPOWR)). A map-local type-list change can affect index interpretation.
5. Building does not exist: type index 300 (global list position: Bus Stop (CASTRT05)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Fire Sale: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Enable and reset applicable timers for [Main_Yuri_Hunt (0938862C)](#trigger-0938862c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14251, Events line 14506, Actions line 14761.

<a id="trigger-0c745f3c"></a>

### 9. Grinder1_BeachFemale - 0C745F3C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Activate_Cheese1 (045E609C)](#trigger-045e609c).

Attached scope: Civilian (CIVBF), owner Neutral, cell (108, 124), tag 0C745A4C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 9.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder1_BeachFemale (0BA8977C)](all02umd-teams.md#team-0ba8977c).
4. Enable and reset applicable timers for [Grinder1_SnowFat (0C73E69C)](#trigger-0c73e69c).
5. Disable [Grinder1_BeachFemale (0C745F3C)](#trigger-0c745f3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14252, Events line 14507, Actions line 14762.

<a id="trigger-0978639c"></a>

### 10. Grinder2_ThinMale - 0978639C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Activate_Cheese1 (045E609C)](#trigger-045e609c).

Attached scope: Civilian (CIV2), owner YuriCountry, cell (136, 78), tag 097BFEDC, persistence mode 2.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder2_ThinMale (0B1138FC)](all02umd-teams.md#team-0b1138fc).
4. Enable and reset applicable timers for [Grinder2_Female (097BAF3C)](#trigger-097baf3c).
5. Disable [Grinder2_ThinMale (0978639C)](#trigger-0978639c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14253, Events line 14508, Actions line 14763.

<a id="trigger-097fd60c"></a>

### 11. Grinder4_SnowFat - 097FD60C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Activate_Cheese1 (045E609C)](#trigger-045e609c).

Attached scope: Civilian (CIVSFM), owner Neutral, cell (201, 106), tag 097FD2BC, persistence mode 2.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder4_SnowFat (0BA9783C)](all02umd-teams.md#team-0ba9783c).
4. Enable and reset applicable timers for [Grinder4_BeachFemale (097EEE1C)](#trigger-097eee1c).
5. Disable [Grinder4_SnowFat (097FD60C)](#trigger-097fd60c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14254, Events line 14509, Actions line 14764.

<a id="trigger-09588c1c"></a>

### 12. Tank_Cheese1 - 09588C1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Activate_Cheese2 (045E003C)](#trigger-045e003c); enable from [Tank_Cheese6 (095A70EC)](#trigger-095a70ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese1 (0994A6FC)](all02umd-teams.md#team-0994a6fc).
2. Enable and reset applicable timers for [Tank_Cheese2 (094DCE7C)](#trigger-094dce7c).
3. Disable [Tank_Cheese1 (09588C1C)](#trigger-09588c1c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14255, Events line 14510, Actions line 14765.

<a id="trigger-10cf24fc"></a>

### 13. Lame_Cheese_Tank1 - 10CF24FC

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Activate_Cheese2 (045E003C)](#trigger-045e003c); enable from [Lame_Cheese_Tank5 (10D11F3C)](#trigger-10d11f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Lame_Tank1 (09101DEC)](all02umd-teams.md#team-09101dec).
2. Enable and reset applicable timers for [Lame_Cheese_Tank2 (10CF620C)](#trigger-10cf620c).
3. Disable [Lame_Cheese_Tank1 (10CF24FC)](#trigger-10cf24fc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14256, Events line 14511, Actions line 14766.

<a id="trigger-07a3955c"></a>

### 14. Yuri2_SellOff - 07A3955C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri2_Gone (09635F3C)](#trigger-09635f3c).

Attached scope: Yuri War Factory (YAWEAP), owner Yuri2, cell (24, 120), tag 07A3AC3C, persistence mode 0; Yuri Barracks (YABRCK), owner Yuri2, cell (30, 125), tag 07A3AC3C, persistence mode 0; Bio Reactor (YAPOWR), owner Yuri2, cell (20, 119), tag 07A3AC3C, persistence mode 0; Bio Reactor (YAPOWR), owner Yuri2, cell (22, 117), tag 07A3AC3C, persistence mode 0; Bio Reactor (YAPOWR), owner Yuri2, cell (20, 114), tag 07A3AC3C, persistence mode 0; Gattling Cannon (YAGGUN), owner Yuri2, cell (35, 131), tag 07A3AC3C, persistence mode 0; Bio Reactor (YAPOWR), owner Yuri2, cell (104, 133), tag 07A3AC3C, persistence mode 0; Bio Reactor (YAPOWR), owner Yuri2, cell (18, 116), tag 07A3AC3C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
2. Enable and reset applicable timers for [Yuri2_Hunt_All (0B20458C)](#trigger-0b20458c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14257, Events line 14512, Actions line 14767.

<a id="trigger-0938862c"></a>

### 15. Main_Yuri_Hunt - 0938862C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Main_Yuri_gone (0CEBD51C)](#trigger-0cebd51c).

Attached scope: tag definitions 093880DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14258, Events line 14513, Actions line 14768.

<a id="trigger-0c73e69c"></a>

### 16. Grinder1_SnowFat - 0C73E69C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder1_BeachFemale (0C745F3C)](#trigger-0c745f3c).

Attached scope: Civilian (CIVSFM), owner Neutral, cell (109, 124), tag 0C73E38C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 9.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder1_SnowFat (0BA89A9C)](all02umd-teams.md#team-0ba89a9c).
4. Enable and reset applicable timers for [Grinder1_GreenMale (0C74595C)](#trigger-0c74595c).
5. Disable [Grinder1_SnowFat (0C73E69C)](#trigger-0c73e69c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14259, Events line 14514, Actions line 14769.

<a id="trigger-097baf3c"></a>

### 17. Grinder2_Female - 097BAF3C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder2_ThinMale (0978639C)](#trigger-0978639c).

Attached scope: Civilian (CIV1), owner YuriCountry, cell (136, 79), tag 097BAE5C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder2_Female (0B11355C)](all02umd-teams.md#team-0b11355c).
4. Enable and reset applicable timers for [Grinder2_BeachMale (097BAABC)](#trigger-097baabc).
5. Disable [Grinder2_Female (097BAF3C)](#trigger-097baf3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14260, Events line 14515, Actions line 14770.

<a id="trigger-097eee1c"></a>

### 18. Grinder4_BeachFemale - 097EEE1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder4_SnowFat (097FD60C)](#trigger-097fd60c).

Attached scope: Civilian (CIVBF), owner Neutral, cell (199, 105), tag 097EED3C, persistence mode 2.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder4_BeachFemale (0BA90B5C)](all02umd-teams.md#team-0ba90b5c).
4. Enable and reset applicable timers for [Grinder4_Female (097FDF3C)](#trigger-097fdf3c).
5. Disable [Grinder4_BeachFemale (097EEE1C)](#trigger-097eee1c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14261, Events line 14516, Actions line 14771.

<a id="trigger-094dce7c"></a>

### 19. Tank_Cheese2 - 094DCE7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Tank_Cheese1 (09588C1C)](#trigger-09588c1c).

Incoming activation links: enable from [Tank_Cheese1 (09588C1C)](#trigger-09588c1c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese2 (0910445C)](all02umd-teams.md#team-0910445c).
2. Enable and reset applicable timers for [Tank_Cheese3 (094DBABC)](#trigger-094dbabc).
3. Disable [Tank_Cheese2 (094DCE7C)](#trigger-094dce7c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14262, Events line 14517, Actions line 14772.

<a id="trigger-10cf620c"></a>

### 20. Lame_Cheese_Tank2 - 10CF620C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Lame_Cheese_Tank1 (10CF24FC)](#trigger-10cf24fc).

Incoming activation links: enable from [Lame_Cheese_Tank1 (10CF24FC)](#trigger-10cf24fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 420 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Lame_Tank2 (09104DEC)](all02umd-teams.md#team-09104dec).
2. Enable and reset applicable timers for [Lame_Cheese_Tank3 (10D0E54C)](#trigger-10d0e54c).
3. Disable [Lame_Cheese_Tank2 (10CF620C)](#trigger-10cf620c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14263, Events line 14518, Actions line 14773.

<a id="trigger-0b20458c"></a>

### 21. Yuri2_Hunt_All - 0B20458C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri2_SellOff (07A3955C)](#trigger-07a3955c).

Attached scope: tag definitions 0B2038BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14264, Events line 14519, Actions line 14774.

<a id="trigger-0c74595c"></a>

### 22. Grinder1_GreenMale - 0C74595C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder1_SnowFat (0C73E69C)](#trigger-0c73e69c).

Attached scope: Civilian (CIV3), owner Neutral, cell (111, 124), tag 0C74557C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 9.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder1_GreenMale (0BA88BDC)](all02umd-teams.md#team-0ba88bdc).
4. Enable and reset applicable timers for [Grinder1_ThinMale (0C73DE4C)](#trigger-0c73de4c).
5. Disable [Grinder1_GreenMale (0C74595C)](#trigger-0c74595c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14265, Events line 14520, Actions line 14775.

<a id="trigger-097baabc"></a>

### 23. Grinder2_BeachMale - 097BAABC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder2_Female (097BAF3C)](#trigger-097baf3c).

Attached scope: Civilian (CIVBTM), owner YuriCountry, cell (136, 80), tag 097BA9DC, persistence mode 2.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder2_BeachMale (0B11342C)](all02umd-teams.md#team-0b11342c).
4. Enable and reset applicable timers for [Grinder2_BeachFemale (097BA8EC)](#trigger-097ba8ec).
5. Disable [Grinder2_BeachMale (097BAABC)](#trigger-097baabc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14266, Events line 14521, Actions line 14776.

<a id="trigger-097fdf3c"></a>

### 24. Grinder4_Female - 097FDF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder4_BeachFemale (097EEE1C)](#trigger-097eee1c).

Attached scope: Civilian (CIV1), owner Neutral, cell (200, 105), tag 097FDE5C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 5 (Grinder4_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder4_Female (0BA907EC)](all02umd-teams.md#team-0ba907ec).
4. Enable and reset applicable timers for [Grinder4_BeachMale (097F14FC)](#trigger-097f14fc).
5. Disable [Grinder4_Female (097FDF3C)](#trigger-097fdf3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14267, Events line 14522, Actions line 14777.

<a id="trigger-094dbabc"></a>

### 25. Tank_Cheese3 - 094DBABC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Tank_Cheese2 (094DCE7C)](#trigger-094dce7c).

Incoming activation links: enable from [Tank_Cheese2 (094DCE7C)](#trigger-094dce7c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese3 (09105EFC)](all02umd-teams.md#team-09105efc).
2. Enable and reset applicable timers for [Tank_Cheese4 (095C203C)](#trigger-095c203c).
3. Disable [Tank_Cheese3 (094DBABC)](#trigger-094dbabc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14268, Events line 14523, Actions line 14778.

<a id="trigger-10d0e54c"></a>

### 26. Lame_Cheese_Tank3 - 10D0E54C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Lame_Cheese_Tank2 (10CF620C)](#trigger-10cf620c).

Incoming activation links: enable from [Lame_Cheese_Tank2 (10CF620C)](#trigger-10cf620c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 420 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Lame_Tank3 (0910059C)](all02umd-teams.md#team-0910059c).
2. Enable and reset applicable timers for [Lame_Cheese_Tank4 (10D1255C)](#trigger-10d1255c).
3. Disable [Lame_Cheese_Tank3 (10D0E54C)](#trigger-10d0e54c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14269, Events line 14524, Actions line 14779.

<a id="trigger-0c73de4c"></a>

### 27. Grinder1_ThinMale - 0C73DE4C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder1_GreenMale (0C74595C)](#trigger-0c74595c).

Attached scope: Civilian (CIV2), owner Neutral, cell (108, 123), tag 0C73DD6C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 9.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder1_ThinMale1 (0BA8A27C)](all02umd-teams.md#team-0ba8a27c).
4. Enable and reset applicable timers for [Grinder1_Female (0C7452EC)](#trigger-0c7452ec).
5. Disable [Grinder1_ThinMale (0C73DE4C)](#trigger-0c73de4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14270, Events line 14525, Actions line 14780.

<a id="trigger-097ba8ec"></a>

### 28. Grinder2_BeachFemale - 097BA8EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder2_BeachMale (097BAABC)](#trigger-097baabc).

Attached scope: Civilian (CIVBF), owner YuriCountry, cell (137, 78), tag 097BA80C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder2_BeachFemale (0B1132FC)](all02umd-teams.md#team-0b1132fc).
4. Enable and reset applicable timers for [Grinder2_SnowMale (097BA71C)](#trigger-097ba71c).
5. Disable [Grinder2_BeachFemale (097BA8EC)](#trigger-097ba8ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14271, Events line 14526, Actions line 14781.

<a id="trigger-097f14fc"></a>

### 29. Grinder4_BeachMale - 097F14FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder4_Female (097FDF3C)](#trigger-097fdf3c).

Attached scope: Civilian (CIVBTM), owner Neutral, cell (201, 105), tag 097F141C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 5 (Grinder4_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder4_BeachMale (0BA90C8C)](all02umd-teams.md#team-0ba90c8c).
4. Enable and reset applicable timers for [Grinder4_GreenMale (097FDD6C)](#trigger-097fdd6c).
5. Disable [Grinder4_BeachMale (097F14FC)](#trigger-097f14fc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14272, Events line 14527, Actions line 14782.

<a id="trigger-095c203c"></a>

### 30. Tank_Cheese4 - 095C203C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Tank_Cheese3 (094DBABC)](#trigger-094dbabc).

Incoming activation links: enable from [Tank_Cheese3 (094DBABC)](#trigger-094dbabc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese4 (09105A4C)](all02umd-teams.md#team-09105a4c).
2. Enable and reset applicable timers for [Tank_Cheese5 (095A71DC)](#trigger-095a71dc).
3. Disable [Tank_Cheese4 (095C203C)](#trigger-095c203c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14273, Events line 14528, Actions line 14783.

<a id="trigger-10d1255c"></a>

### 31. Lame_Cheese_Tank4 - 10D1255C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Lame_Cheese_Tank3 (10D0E54C)](#trigger-10d0e54c).

Incoming activation links: enable from [Lame_Cheese_Tank3 (10D0E54C)](#trigger-10d0e54c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 420 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Lame_Tank4 (0910035C)](all02umd-teams.md#team-0910035c).
2. Enable and reset applicable timers for [Lame_Cheese_Tank5 (10D11F3C)](#trigger-10d11f3c).
3. Disable [Lame_Cheese_Tank4 (10D1255C)](#trigger-10d1255c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14274, Events line 14529, Actions line 14784.

<a id="trigger-0c7452ec"></a>

### 32. Grinder1_Female - 0C7452EC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder1_ThinMale (0C73DE4C)](#trigger-0c73de4c).

Attached scope: Civilian (CIV1), owner Neutral, cell (109, 123), tag 0C743E7C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 9.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder1_Female (0BA8945C)](all02umd-teams.md#team-0ba8945c).
4. Enable and reset applicable timers for [Grinder1_BeachMale (0C7439EC)](#trigger-0c7439ec).
5. Disable [Grinder1_Female (0C7452EC)](#trigger-0c7452ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14275, Events line 14530, Actions line 14785.

<a id="trigger-097ba71c"></a>

### 33. Grinder2_SnowMale - 097BA71C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder2_BeachFemale (097BA8EC)](#trigger-097ba8ec).

Attached scope: Civilian (CIVSTM), owner YuriCountry, cell (137, 79), tag 097BA3FC, persistence mode 2.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder2_SnowMale (0B1131CC)](all02umd-teams.md#team-0b1131cc).
4. Enable and reset applicable timers for [Grinder2_SnowFemale (097BA30C)](#trigger-097ba30c).
5. Disable [Grinder2_SnowMale (097BA71C)](#trigger-097ba71c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14276, Events line 14531, Actions line 14786.

<a id="trigger-097fdd6c"></a>

### 34. Grinder4_GreenMale - 097FDD6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder4_BeachMale (097F14FC)](#trigger-097f14fc).

Attached scope: Civilian (CIV3), owner Neutral, cell (202, 105), tag 097FDC8C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 5 (Grinder4_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder4_GreenMale (0BA9058C)](all02umd-teams.md#team-0ba9058c).
4. Enable and reset applicable timers for [Grinder4_SnowFemale (097FD7DC)](#trigger-097fd7dc).
5. Disable [Grinder4_GreenMale (097FDD6C)](#trigger-097fdd6c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14277, Events line 14532, Actions line 14787.

<a id="trigger-095a71dc"></a>

### 35. Tank_Cheese5 - 095A71DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Tank_Cheese4 (095C203C)](#trigger-095c203c).

Incoming activation links: enable from [Tank_Cheese4 (095C203C)](#trigger-095c203c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese5 (0910580C)](all02umd-teams.md#team-0910580c).
2. Enable and reset applicable timers for [Tank_Cheese6 (095A70EC)](#trigger-095a70ec).
3. Disable [Tank_Cheese5 (095A71DC)](#trigger-095a71dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14278, Events line 14533, Actions line 14788.

<a id="trigger-10d11f3c"></a>

### 36. Lame_Cheese_Tank5 - 10D11F3C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Lame_Cheese_Tank4 (10D1255C)](#trigger-10d1255c).

Incoming activation links: enable from [Lame_Cheese_Tank4 (10D1255C)](#trigger-10d1255c).

Attached scope: tag definitions 10CF62FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 420 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Lame_Tank5 (0910647C)](all02umd-teams.md#team-0910647c).
2. Enable and reset applicable timers for [Lame_Cheese_Tank1 (10CF24FC)](#trigger-10cf24fc).
3. Disable [Lame_Cheese_Tank5 (10D11F3C)](#trigger-10d11f3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14279, Events line 14534, Actions line 14789.

<a id="trigger-0c7439ec"></a>

### 37. Grinder1_BeachMale - 0C7439EC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder1_Female (0C7452EC)](#trigger-0c7452ec).

Attached scope: Civilian (CIVBTM), owner Neutral, cell (110, 123), tag 0C74360C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 9.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder1_BeachMale (0BA88EFC)](all02umd-teams.md#team-0ba88efc).
4. Disable [Grinder1_BeachMale (0C7439EC)](#trigger-0c7439ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14280, Events line 14535, Actions line 14790.

<a id="trigger-097ba30c"></a>

### 38. Grinder2_SnowFemale - 097BA30C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder2_SnowMale (097BA71C)](#trigger-097ba71c).

Attached scope: Civilian (CIVSF), owner YuriCountry, cell (137, 80), tag 097BA22C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder2_SnowFemale (0B114EFC)](all02umd-teams.md#team-0b114efc).
4. Disable [Grinder2_SnowFemale (097BA30C)](#trigger-097ba30c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14281, Events line 14536, Actions line 14791.

<a id="trigger-097fd7dc"></a>

### 39. Grinder4_SnowFemale - 097FD7DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder4_GreenMale (097FDD6C)](#trigger-097fdd6c).

Attached scope: Civilian (CIVSF), owner Neutral, cell (199, 104), tag 097FD6FC, persistence mode 2.

**Wait for the recorded events:**

1. local flag 5 (Grinder4_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder4_SnowFemale (0BA9045C)](all02umd-teams.md#team-0ba9045c).
4. Enable and reset applicable timers for [Grinder4_SnowMale (097FD9AC)](#trigger-097fd9ac).
5. Disable [Grinder4_SnowFemale (097FD7DC)](#trigger-097fd7dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14282, Events line 14537, Actions line 14792.

<a id="trigger-095a70ec"></a>

### 40. Tank_Cheese6 - 095A70EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Tank_Cheese5 (095A71DC)](#trigger-095a71dc).

Incoming activation links: enable from [Tank_Cheese5 (095A71DC)](#trigger-095a71dc).

Attached scope: tag definitions 09590F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese6 (091055CC)](all02umd-teams.md#team-091055cc).
2. Enable and reset applicable timers for [Tank_Cheese1 (09588C1C)](#trigger-09588c1c).
3. Disable [Tank_Cheese6 (095A70EC)](#trigger-095a70ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14283, Events line 14538, Actions line 14793.

<a id="trigger-097fd9ac"></a>

### 41. Grinder4_SnowMale - 097FD9AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder4_SnowFemale (097FD7DC)](#trigger-097fd7dc).

Attached scope: Civilian (CIVSTM), owner Neutral, cell (200, 104), tag 097FD8CC, persistence mode 2.

**Wait for the recorded events:**

1. local flag 5 (Grinder4_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder4_SnowMale (0BA9032C)](all02umd-teams.md#team-0ba9032c).
4. Enable and reset applicable timers for [Grinder4_ThinMale (097FE29C)](#trigger-097fe29c).
5. Disable [Grinder4_SnowMale (097FD9AC)](#trigger-097fd9ac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14284, Events line 14539, Actions line 14794.

<a id="trigger-097fe29c"></a>

### 42. Grinder4_ThinMale - 097FE29C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder4_SnowMale (097FD9AC)](#trigger-097fd9ac).

Attached scope: Civilian (CIV2), owner Neutral, cell (201, 104), tag 097FE1BC, persistence mode 2.

**Wait for the recorded events:**

1. local flag 5 (Grinder4_Gone) is clear.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder4_ThinMale (0BA906BC)](all02umd-teams.md#team-0ba906bc).
4. Enable and reset applicable timers for [Grinder4_BeachFat (097EEC4C)](#trigger-097eec4c).
5. Disable [Grinder4_ThinMale (097FE29C)](#trigger-097fe29c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14285, Events line 14540, Actions line 14795.

<a id="trigger-097eec4c"></a>

### 43. Grinder4_BeachFat - 097EEC4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder4_ThinMale (097FE29C)](#trigger-097fe29c).

Attached scope: Civilian (CIVBFM), owner Neutral, cell (202, 104), tag 097F9F4C, persistence mode 2.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Create/recruit team [Grinder4_BeachFat (0BA90A2C)](all02umd-teams.md#team-0ba90a2c).
4. Disable [Grinder4_BeachFat (097EEC4C)](#trigger-097eec4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14286, Events line 14541, Actions line 14796.

<a id="trigger-0796e03c"></a>

### 44. Hard_Cheese1 - 0796E03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hard_Cheese6 (0798F60C)](#trigger-0798f60c); enable from [Player_Builds_WF (04F2A9AC)](#trigger-04f2a9ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese1 (0994A6FC)](all02umd-teams.md#team-0994a6fc).
2. Enable and reset applicable timers for [Hard_Cheese2 (0798F9CC)](#trigger-0798f9cc).
3. Disable [Hard_Cheese1 (0796E03C)](#trigger-0796e03c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14287, Events line 14542, Actions line 14797.

<a id="trigger-0798f9cc"></a>

### 45. Hard_Cheese2 - 0798F9CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Hard_Cheese1 (0796E03C)](#trigger-0796e03c).

Incoming activation links: enable from [Hard_Cheese1 (0796E03C)](#trigger-0796e03c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese2 (0910445C)](all02umd-teams.md#team-0910445c).
2. Enable and reset applicable timers for [Hard_Cheese3 (0798F8DC)](#trigger-0798f8dc).
3. Disable [Hard_Cheese2 (0798F9CC)](#trigger-0798f9cc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14288, Events line 14543, Actions line 14798.

<a id="trigger-0798f8dc"></a>

### 46. Hard_Cheese3 - 0798F8DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Hard_Cheese2 (0798F9CC)](#trigger-0798f9cc).

Incoming activation links: enable from [Hard_Cheese2 (0798F9CC)](#trigger-0798f9cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese3 (09105EFC)](all02umd-teams.md#team-09105efc).
2. Enable and reset applicable timers for [Hard_Cheese4 (0798F7EC)](#trigger-0798f7ec).
3. Disable [Hard_Cheese3 (0798F8DC)](#trigger-0798f8dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14289, Events line 14544, Actions line 14799.

<a id="trigger-0798f7ec"></a>

### 47. Hard_Cheese4 - 0798F7EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Hard_Cheese3 (0798F8DC)](#trigger-0798f8dc).

Incoming activation links: enable from [Hard_Cheese3 (0798F8DC)](#trigger-0798f8dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese4 (09105A4C)](all02umd-teams.md#team-09105a4c).
2. Enable and reset applicable timers for [Hard_Cheese5 (0798F6FC)](#trigger-0798f6fc).
3. Disable [Hard_Cheese4 (0798F7EC)](#trigger-0798f7ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14290, Events line 14545, Actions line 14800.

<a id="trigger-0798f6fc"></a>

### 48. Hard_Cheese5 - 0798F6FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Hard_Cheese4 (0798F7EC)](#trigger-0798f7ec).

Incoming activation links: enable from [Hard_Cheese4 (0798F7EC)](#trigger-0798f7ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese5 (0910580C)](all02umd-teams.md#team-0910580c).
2. Enable and reset applicable timers for [Hard_Cheese6 (0798F60C)](#trigger-0798f60c).
3. Disable [Hard_Cheese5 (0798F6FC)](#trigger-0798f6fc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14291, Events line 14546, Actions line 14801.

<a id="trigger-0798f60c"></a>

### 49. Hard_Cheese6 - 0798F60C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Hard_Cheese5 (0798F6FC)](#trigger-0798f6fc).

Incoming activation links: enable from [Hard_Cheese5 (0798F6FC)](#trigger-0798f6fc).

Attached scope: tag definitions 0796D04C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nod_Tank_Cheese6 (091055CC)](all02umd-teams.md#team-091055cc).
2. Enable and reset applicable timers for [Hard_Cheese1 (0796E03C)](#trigger-0796e03c).
3. Disable [Hard_Cheese6 (0798F60C)](#trigger-0798f60c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14292, Events line 14547, Actions line 14802.

<a id="trigger-0b975c7c"></a>

### 50. Change_LAX_House - 0B975C7C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: LAX (CALA05), owner Special, cell (114, 178), tag 0B97578C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 11 (cell 116, 180).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14293, Events line 14548, Actions line 14803.

<a id="trigger-0b97536c"></a>

### 51. Camera_Start - 0B97536C

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B97514C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 8 (cell 167, 128).
2. Disable player input.
3. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).
4. Enable and reset applicable timers for [Start_Briefing (0930F29C)](#trigger-0930f29c).
5. Play voice notification EVA_EstablishBattlefieldControl.
6. Move the camera to waypoint 8 (cell 167, 128) with speed setting 2.
7. Enable and reset applicable timers for [Garrison_Hard (093C2ADC)](#trigger-093c2adc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14294, Events line 14549, Actions line 14804.

<a id="trigger-0930f29c"></a>

### 52. Start_Briefing - 0930F29C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_Start (0B97536C)](#trigger-0b97536c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 7.
2. Enable and reset applicable timers for [Briefing_Followup (0895FDFC)](#trigger-0895fdfc).
3. Disable [Start_Briefing (0930F29C)](#trigger-0930f29c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14295, Events line 14550, Actions line 14805.

<a id="trigger-093c2adc"></a>

### 53. Garrison_Hard - 093C2ADC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_Start (0B97536C)](#trigger-0b97536c).

Attached scope: tag definitions 093C248C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yuri_Gar_CS_CU (092C0B8C)](all02umd-teams.md#team-092c0b8c).
2. Supply reinforcement team [Yuri_Gar_CT_CV (092C050C)](all02umd-teams.md#team-092c050c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14296, Events line 14551, Actions line 14806.

<a id="trigger-0895fdfc"></a>

### 54. Briefing_Followup - 0895FDFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start_Briefing (0930F29C)](#trigger-0930f29c).

Incoming activation links: enable from [Start_Briefing (0930F29C)](#trigger-0930f29c).

Attached scope: tag definitions 093095BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 27 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification A02_p01.
2. Enable and reset applicable timers for [Camera_to_LAX (093093FC)](#trigger-093093fc).
3. Disable [Briefing_Followup (0895FDFC)](#trigger-0895fdfc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14297, Events line 14552, Actions line 14807.

<a id="trigger-093093fc"></a>

### 55. Camera_to_LAX - 093093FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Briefing_Followup (0895FDFC)](#trigger-0895fdfc).

Attached scope: tag definitions 093090FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 11 (cell 116, 180) with speed setting 3.
2. Enable and reset applicable timers for [LAX_Speech (0930CDEC)](#trigger-0930cdec).
3. Enable and reset applicable timers for [Point_at_LAX (099AEA1C)](#trigger-099aea1c).
4. Enable and reset applicable timers for [Pointer_Timer (099AFF3C)](#trigger-099aff3c).
5. Disable [Camera_to_LAX (093093FC)](#trigger-093093fc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14298, Events line 14553, Actions line 14808.

<a id="trigger-0930cdec"></a>

### 56. LAX_Speech - 0930CDEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_to_LAX (093093FC)](#trigger-093093fc).

Attached scope: tag definitions 0930CC3C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA2_EvaBriefing01.
2. Enable and reset applicable timers for [Camera_to_Grinder (0930C5CC)](#trigger-0930c5cc).
3. Disable [LAX_Speech (0930CDEC)](#trigger-0930cdec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14299, Events line 14554, Actions line 14809.

<a id="trigger-099aea1c"></a>

### 57. Point_at_LAX - 099AEA1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_to_LAX (093093FC)](#trigger-093093fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 483; location/duration field DK.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14300, Events line 14555, Actions line 14810.

<a id="trigger-099aff3c"></a>

### 58. Pointer_Timer - 099AFF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Point_at_LAX (099AEA1C)](#trigger-099aea1c).

Incoming activation links: enable from [Camera_to_LAX (093093FC)](#trigger-093093fc).

Attached scope: tag definitions 099AE55C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Point_at_LAX (099AEA1C)](#trigger-099aea1c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14301, Events line 14556, Actions line 14811.

<a id="trigger-0930c5cc"></a>

### 59. Camera_to_Grinder - 0930C5CC

Owner reference: Yuri3Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [LAX_Speech (0930CDEC)](#trigger-0930cdec).

Attached scope: tag definitions 0931F16C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 17 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 92 (cell 105, 128) with speed setting 3.
2. Enable and reset applicable timers for [Grinder_Movie (0932705C)](#trigger-0932705c).
3. Flash buildings of type YAGRND; duration argument 90.
4. Disable [Camera_to_Grinder (0930C5CC)](#trigger-0930c5cc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14302, Events line 14557, Actions line 14812.

<a id="trigger-0932705c"></a>

### 60. Grinder_Movie - 0932705C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_to_Grinder (0930C5CC)](#trigger-0930c5cc).

Attached scope: tag definitions 0932007C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 8.
2. Enable and reset applicable timers for [Briefing_Yuri (091B6F3C)](#trigger-091b6f3c).
3. Enable and reset applicable timers for [Civ_ThinMale1 (0462733C)](#trigger-0462733c).
4. Disable [Grinder_Movie (0932705C)](#trigger-0932705c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14303, Events line 14558, Actions line 14813.

<a id="trigger-091b6f3c"></a>

### 61. Briefing_Yuri - 091B6F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder_Movie (0932705C)](#trigger-0932705c).

Attached scope: tag definitions 091B428C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 43 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 203 (cell 133, 79) with speed setting 4.
2. Create/recruit team [Briefing_Clone (091C8E0C)](all02umd-teams.md#team-091c8e0c).
3. Enable and reset applicable timers for [Briefing_Yuri2 (088509DC)](#trigger-088509dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14304, Events line 14559, Actions line 14814.

<a id="trigger-0462733c"></a>

### 62. Civ_ThinMale1 - 0462733C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder_Movie (0932705C)](#trigger-0932705c).

Attached scope: Civilian (CIV2), owner Neutral, cell (109, 126), tag 04624AEC, persistence mode 0.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.
2. Change House: owner selector 15 (country/type YURI3COUNTRY; placed owner Yuri3).
3. Create/recruit team [Grinder1_ThinMale1 (0BA8A27C)](all02umd-teams.md#team-0ba8a27c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14305, Events line 14560, Actions line 14815.

<a id="trigger-088509dc"></a>

### 63. Briefing_Yuri2 - 088509DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Briefing_Yuri (091B6F3C)](#trigger-091b6f3c).

Attached scope: tag definitions 0885047C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_YuriClone.
2. Enable and reset applicable timers for [Camera_Return (04384E4C)](#trigger-04384e4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14306, Events line 14561, Actions line 14816.

<a id="trigger-04384e4c"></a>

### 64. Camera_Return - 04384E4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Briefing_Yuri2 (088509DC)](#trigger-088509dc).

Attached scope: tag definitions 043848EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 8 (cell 167, 128) with speed setting 3.
2. Enable and reset applicable timers for [Return_Control (043842DC)](#trigger-043842dc).
3. Disable [Camera_Return (04384E4C)](#trigger-04384e4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14307, Events line 14562, Actions line 14817.

<a id="trigger-043842dc"></a>

### 65. Return_Control - 043842DC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_Return (04384E4C)](#trigger-04384e4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Production Begins: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
3. AI triggers begin: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
4. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).
5. Enable and reset applicable timers for [Make_CheatA_1 (045B1B5C)](#trigger-045b1b5c).
6. Enable and reset applicable timers for [Start_Yuri2 (0921C8DC)](#trigger-0921c8dc).
7. Play voice notification EVA_BattlefieldControlOnline.
8. Disable [Return_Control (043842DC)](#trigger-043842dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14308, Events line 14563, Actions line 14818.

<a id="trigger-045b1b5c"></a>

### 66. Make_CheatA_1 - 045B1B5C

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Return_Control (043842DC)](#trigger-043842dc); enable from [Make_CheatB_Final (0B94417C)](#trigger-0b94417c); enable from [Create_New_Team_B (0B81D85C)](#trigger-0b81d85c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 13 (Barrack1_Gone) is clear.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Cheat_Initiate (0981521C)](all02umd-teams.md#team-0981521c).
2. Enable and reset applicable timers for [Make_CheatA_2 (045B127C)](#trigger-045b127c).
3. Disable [Make_CheatA_1 (045B1B5C)](#trigger-045b1b5c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14309, Events line 14564, Actions line 14819.

<a id="trigger-0921c8dc"></a>

### 67. Start_Yuri2 - 0921C8DC

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Return_Control (043842DC)](#trigger-043842dc).

Incoming activation links: enable from [Return_Control (043842DC)](#trigger-043842dc).

Attached scope: tag definitions 04382C5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
2. AI triggers begin: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).
4. Enable and reset applicable timers for [_Ambient_SlavePens (0463917C)](#trigger-0463917c).
5. Disable [Start_Yuri2 (0921C8DC)](#trigger-0921c8dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14310, Events line 14565, Actions line 14820.

<a id="trigger-045b127c"></a>

### 68. Make_CheatA_2 - 045B127C

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatA_1 (045B1B5C)](#trigger-045b1b5c).

Incoming activation links: enable from [Make_CheatA_1 (045B1B5C)](#trigger-045b1b5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 13 (Barrack1_Gone) is clear.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Cheat_Initiate (0981521C)](all02umd-teams.md#team-0981521c).
2. Enable and reset applicable timers for [Make_CheatA_3 (045B103C)](#trigger-045b103c).
3. Disable [Make_CheatA_2 (045B127C)](#trigger-045b127c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14311, Events line 14566, Actions line 14821.

<a id="trigger-0463917c"></a>

### 69. _Ambient_SlavePens - 0463917C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Yuri2 (0921C8DC)](#trigger-0921c8dc).

Attached scope: tag definitions 0463909C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 234 (cell 109, 124).
2. Play sound _Amb_LondonCivilians at waypoint 235 (cell 136, 79).
3. Play sound _Amb_LondonCivilians at waypoint 237 (cell 201, 105).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14312, Events line 14567, Actions line 14822.

<a id="trigger-045b103c"></a>

### 70. Make_CheatA_3 - 045B103C

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatA_2 (045B127C)](#trigger-045b127c).

Incoming activation links: enable from [Make_CheatA_2 (045B127C)](#trigger-045b127c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 13 (Barrack1_Gone) is clear.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Cheat_Initiate (0981521C)](all02umd-teams.md#team-0981521c).
2. Enable and reset applicable timers for [Make_CheatA_4 (045B0DEC)](#trigger-045b0dec).
3. Disable [Make_CheatA_3 (045B103C)](#trigger-045b103c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14313, Events line 14568, Actions line 14823.

<a id="trigger-045b0dec"></a>

### 71. Make_CheatA_4 - 045B0DEC

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatA_3 (045B103C)](#trigger-045b103c).

Incoming activation links: enable from [Make_CheatA_3 (045B103C)](#trigger-045b103c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 13 (Barrack1_Gone) is clear.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Cheat_Initiate (0981521C)](all02umd-teams.md#team-0981521c).
2. Enable and reset applicable timers for [Make_CheatA_5 (045B0BAC)](#trigger-045b0bac).
3. Disable [Make_CheatA_4 (045B0DEC)](#trigger-045b0dec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14314, Events line 14569, Actions line 14824.

<a id="trigger-045b0bac"></a>

### 72. Make_CheatA_5 - 045B0BAC

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatA_4 (045B0DEC)](#trigger-045b0dec).

Incoming activation links: enable from [Make_CheatA_4 (045B0DEC)](#trigger-045b0dec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 13 (Barrack1_Gone) is clear.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Cheat_Clone (09816B7C)](all02umd-teams.md#team-09816b7c).
2. Enable and reset applicable timers for [Destroy_Old_Team_A (0B81A8BC)](#trigger-0b81a8bc).
3. Disable [Make_CheatA_5 (045B0BAC)](#trigger-045b0bac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14315, Events line 14570, Actions line 14825.

<a id="trigger-0b81a8bc"></a>

### 73. Destroy_Old_Team_A - 0B81A8BC

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatA_Final (045B063C)](#trigger-045b063c).

Incoming activation links: enable from [Make_CheatA_5 (045B0BAC)](#trigger-045b0bac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_Cheat_Initiate (0981521C)](all02umd-teams.md#team-0981521c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_Cheat_Clone (09816B7C)](all02umd-teams.md#team-09816b7c).
3. Enable and reset applicable timers for [Create_New_Team_A (0B81A7CC)](#trigger-0b81a7cc).
4. Disable [Destroy_Old_Team_A (0B81A8BC)](#trigger-0b81a8bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14316, Events line 14571, Actions line 14826.

<a id="trigger-045b063c"></a>

### 74. Make_CheatA_Final - 045B063C

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatA_5 (045B0BAC)](#trigger-045b0bac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_Cheat_Initiate (0981521C)](all02umd-teams.md#team-0981521c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_Cheat_Clone (09816B7C)](all02umd-teams.md#team-09816b7c).
3. Create/recruit team [TEAM_Cheat_A (098166CC)](all02umd-teams.md#team-098166cc).
4. Enable and reset applicable timers for [Make_CheatB_1 (0B92F17C)](#trigger-0b92f17c).
5. Disable [Make_CheatA_Final (045B063C)](#trigger-045b063c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14317, Events line 14572, Actions line 14827.

<a id="trigger-0b81a7cc"></a>

### 75. Create_New_Team_A - 0B81A7CC

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Destroy_Old_Team_A (0B81A8BC)](#trigger-0b81a8bc).

Incoming activation links: enable from [Destroy_Old_Team_A (0B81A8BC)](#trigger-0b81a8bc).

Attached scope: tag definitions 045B136C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Cheat_A (098166CC)](all02umd-teams.md#team-098166cc).
2. Enable and reset applicable timers for [Make_CheatB_1 (0B92F17C)](#trigger-0b92f17c).
3. Disable [Create_New_Team_A (0B81A7CC)](#trigger-0b81a7cc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14318, Events line 14573, Actions line 14828.

<a id="trigger-0b92f17c"></a>

### 76. Make_CheatB_1 - 0B92F17C

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Make_CheatA_Final (045B063C)](#trigger-045b063c); enable from [Create_New_Team_A (0B81A7CC)](#trigger-0b81a7cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 13 (Barrack1_Gone) is clear.
2. 240 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_CheatB_Initiate (09819B7C)](all02umd-teams.md#team-09819b7c) at waypoint 104 (cell 158, 79).
2. Enable and reset applicable timers for [Make_CheatB_2 (0C87AAFC)](#trigger-0c87aafc).
3. Disable [Make_CheatB_1 (0B92F17C)](#trigger-0b92f17c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14319, Events line 14574, Actions line 14829.

<a id="trigger-0c87aafc"></a>

### 77. Make_CheatB_2 - 0C87AAFC

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatB_1 (0B92F17C)](#trigger-0b92f17c).

Incoming activation links: enable from [Make_CheatB_1 (0B92F17C)](#trigger-0b92f17c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 13 (Barrack1_Gone) is clear.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_CheatB_Initiate (09819B7C)](all02umd-teams.md#team-09819b7c) at waypoint 104 (cell 158, 79).
2. Enable and reset applicable timers for [Make_CheatB_3 (0B93017C)](#trigger-0b93017c).
3. Disable [Make_CheatB_2 (0C87AAFC)](#trigger-0c87aafc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14320, Events line 14575, Actions line 14830.

<a id="trigger-0b93017c"></a>

### 78. Make_CheatB_3 - 0B93017C

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatB_2 (0C87AAFC)](#trigger-0c87aafc).

Incoming activation links: enable from [Make_CheatB_2 (0C87AAFC)](#trigger-0c87aafc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 13 (Barrack1_Gone) is clear.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_CheatB_Initiate (09819B7C)](all02umd-teams.md#team-09819b7c) at waypoint 104 (cell 158, 79).
2. Enable and reset applicable timers for [Make_CheatB_4 (0B93D17C)](#trigger-0b93d17c).
3. Disable [Make_CheatB_3 (0B93017C)](#trigger-0b93017c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14321, Events line 14576, Actions line 14831.

<a id="trigger-0b93d17c"></a>

### 79. Make_CheatB_4 - 0B93D17C

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatB_3 (0B93017C)](#trigger-0b93017c).

Incoming activation links: enable from [Make_CheatB_3 (0B93017C)](#trigger-0b93017c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 13 (Barrack1_Gone) is clear.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_CheatB_Engineer (0981821C)](all02umd-teams.md#team-0981821c) at waypoint 104 (cell 158, 79).
2. Enable and reset applicable timers for [Make_CheatB_5 (0EE882DC)](#trigger-0ee882dc).
3. Disable [Make_CheatB_4 (0B93D17C)](#trigger-0b93d17c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14322, Events line 14577, Actions line 14832.

<a id="trigger-0ee882dc"></a>

### 80. Make_CheatB_5 - 0EE882DC

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatB_Final (0B94417C)](#trigger-0b94417c).

Incoming activation links: enable from [Make_CheatB_4 (0B93D17C)](#trigger-0b93d17c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 13 (Barrack1_Gone) is clear.

Flag writers in this mission: set local flag 13 (Barrack1_Gone) at [YuriBarrack_Gone (095FE79C)](#trigger-095fe79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_CheatB_Engineer (0981821C)](all02umd-teams.md#team-0981821c) at waypoint 104 (cell 158, 79).
2. Enable and reset applicable timers for [Destroy_Old_Team_B (0B81D9DC)](#trigger-0b81d9dc).
3. Disable [Make_CheatB_5 (0EE882DC)](#trigger-0ee882dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14323, Events line 14578, Actions line 14833.

<a id="trigger-0b94417c"></a>

### 81. Make_CheatB_Final - 0B94417C

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatB_4 (0B93D17C)](#trigger-0b93d17c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_CheatB_Initiate (09819B7C)](all02umd-teams.md#team-09819b7c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_CheatB_Engineer (0981821C)](all02umd-teams.md#team-0981821c).
3. Create/recruit team [TEAM_Cheat_B (098186CC)](all02umd-teams.md#team-098186cc).
4. Enable and reset applicable timers for [Make_CheatA_1 (045B1B5C)](#trigger-045b1b5c).
5. Disable [Make_CheatB_Final (0B94417C)](#trigger-0b94417c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14324, Events line 14579, Actions line 14834.

<a id="trigger-0b81d9dc"></a>

### 82. Destroy_Old_Team_B - 0B81D9DC

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_CheatB_5 (0EE882DC)](#trigger-0ee882dc).

Incoming activation links: enable from [Make_CheatB_5 (0EE882DC)](#trigger-0ee882dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_CheatB_Initiate (09819B7C)](all02umd-teams.md#team-09819b7c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_CheatB_Engineer (0981821C)](all02umd-teams.md#team-0981821c).
3. Enable and reset applicable timers for [Create_New_Team_B (0B81D85C)](#trigger-0b81d85c).
4. Disable [Destroy_Old_Team_B (0B81D9DC)](#trigger-0b81d9dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14325, Events line 14580, Actions line 14835.

<a id="trigger-0b81d85c"></a>

### 83. Create_New_Team_B - 0B81D85C

Owner reference: Yuri4Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Destroy_Old_Team_B (0B81D9DC)](#trigger-0b81d9dc).

Incoming activation links: enable from [Destroy_Old_Team_B (0B81D9DC)](#trigger-0b81d9dc).

Attached scope: tag definitions 0B93618C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Cheat_B (098186CC)](all02umd-teams.md#team-098186cc).
2. Enable and reset applicable timers for [Make_CheatA_1 (045B1B5C)](#trigger-045b1b5c).
3. Disable [Create_New_Team_B (0B81D85C)](#trigger-0b81d85c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14326, Events line 14581, Actions line 14836.

<a id="trigger-0b8e13ac"></a>

### 84. Make_Patrols - 0B8E13AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B8E68EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Patrol_A (0B9710EC)](all02umd-teams.md#team-0b9710ec).
2. Create/recruit team [TEAM_Patrol_B (0B97441C)](all02umd-teams.md#team-0b97441c).
3. Create/recruit team [TEAM_Patrol_C (08D7197C)](all02umd-teams.md#team-08d7197c).
4. Create/recruit team [TEAM_Hero_Patrol_1 (090347DC)](all02umd-teams.md#team-090347dc).
5. Create/recruit team [TEAM_Hero_Patrol_2 (0903432C)](all02umd-teams.md#team-0903432c).
6. Create/recruit team [TEAM_Patrol_1 (0BC7E21C)](all02umd-teams.md#team-0bc7e21c).
7. Create/recruit team [TEAM_Patrol_2 (0961CCEC)](all02umd-teams.md#team-0961ccec).
8. Create/recruit team [TEAM_Patrol_3 (095FFDFC)](all02umd-teams.md#team-095ffdfc).
9. Create/recruit team [TEAM_Patrol_4 (095FF47C)](all02umd-teams.md#team-095ff47c).
10. Create/recruit team [TEAM_Patrol_5 (095F8EFC)](all02umd-teams.md#team-095f8efc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14327, Events line 14582, Actions line 14837.

<a id="trigger-0930c39c"></a>

### 85. Change_to_Yuri - 0930C39C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0931D05C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14328, Events line 14583, Actions line 14838.

<a id="trigger-0d0983fc"></a>

### 86. Yuri_Base_Defenses - 0D0983FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D09CF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Yuri_BD_2 Lasher, 1 Gatt (0D092D8C)](all02umd-teams.md#team-0d092d8c).
2. Create/recruit team [Yuri_BD_3 Gatt (0C71EEFC)](all02umd-teams.md#team-0c71eefc).
3. Create/recruit team [Yuri_BD_3 Lasher, 2 Gatt (0D09087C)](all02umd-teams.md#team-0d09087c).
4. Create/recruit team [Nod_BD_1 (091027DC)](all02umd-teams.md#team-091027dc).
5. Create/recruit team [Nod_BD_2 (0910213C)](all02umd-teams.md#team-0910213c).
6. Create/recruit team [Nod_BD_3 (09103DEC)](all02umd-teams.md#team-09103dec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14329, Events line 14584, Actions line 14839.

<a id="trigger-0abae7bc"></a>

### 87. Change_Hero - 0ABAE7BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hero_Guns_Gone (0ABA8C5C)](#trigger-0aba8c5c); enable from [Grinder1_Attacked (07F7DACC)](#trigger-07f7dacc).

Attached scope: Hero (ARND), owner Neutral, cell (107, 131), tag 0ABAFD0C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Wakeup self; main setting 0.
3. Create radar-event marker type 11 at waypoint 468 (cell 107, 131).
4. Play voice notification Mis_xA2_GGIThankYou.
5. Create/recruit team [TEAM_Hero (0904272C)](all02umd-teams.md#team-0904272c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14330, Events line 14585, Actions line 14840.

<a id="trigger-0aba8c5c"></a>

### 88. Hero_Guns_Gone - 0ABA8C5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Initiate (INIT), owner YuriCountry, cell (106, 132), tag 0ABA86FC, persistence mode 0; Initiate (INIT), owner YuriCountry, cell (107, 132), tag 0ABA86FC, persistence mode 0; Initiate (INIT), owner YuriCountry, cell (109, 131), tag 0ABA86FC, persistence mode 0; Initiate (INIT), owner YuriCountry, cell (109, 132), tag 0ABA86FC, persistence mode 0; Initiate (INIT), owner YuriCountry, cell (105, 131), tag 0ABA86FC, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change_Hero (0ABAE7BC)](#trigger-0abae7bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14331, Events line 14586, Actions line 14841.

<a id="trigger-0acd381c"></a>

### 89. Wakeup_Prisms - 0ACD381C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Arabs_Gone (08D5E88C)](#trigger-08d5e88c).

Attached scope: tag definitions 0ACD0F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14332, Events line 14587, Actions line 14842.

<a id="trigger-08d5e88c"></a>

### 90. Arabs_Gone - 08D5E88C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Initiate (INIT), owner Arabs, cell (197, 105), tag 08D5E26C, persistence mode 0; Initiate (INIT), owner Arabs, cell (195, 107), tag 08D5E26C, persistence mode 0; Initiate (INIT), owner Arabs, cell (197, 109), tag 08D5E26C, persistence mode 0; Initiate (INIT), owner Arabs, cell (199, 111), tag 08D5E26C, persistence mode 0; Initiate (INIT), owner Arabs, cell (191, 103), tag 08D5E26C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 6 (country/type ARABS; placed owner Arabs).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Wakeup_Prisms (0ACD381C)](#trigger-0acd381c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14333, Events line 14588, Actions line 14843.

<a id="trigger-0cddb12c"></a>

### 91. Reveal_Shroud - 0CDDB12C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CDDC93C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 469 (cell 131, 81).
2. Reveal terrain around waypoint 470 (cell 156, 73).
3. Reveal terrain around waypoint 471 (cell 197, 105).
4. Reveal terrain around waypoint 92 (cell 105, 128).
5. Reveal terrain around waypoint 115 (cell 118, 177).
6. Reveal terrain around waypoint 116 (cell 109, 177).
7. Reveal terrain around waypoint 117 (cell 115, 175).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14334, Events line 14589, Actions line 14844.

<a id="trigger-0cddc84c"></a>

### 92. Grinders_Gone - 0CDDC84C

Owner reference: Yuri3Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Check_Grinders (0C42981C)](#trigger-0c42981c).

Attached scope: tag definitions 0CDDC62C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Grinders_Gone) is set.
2. local flag 0 (Base_Gone) is clear.

Flag writers in this mission: set local flag 1 (Grinders_Gone) at [Check_Grinders (0C42981C)](#trigger-0c42981c); set local flag 0 (Base_Gone) at [Base_Gone (0CDDD74C)](#trigger-0cddd74c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_xA2_EvaGrindersGone.
2. Enable and reset applicable timers for [New_Mission (094D906C)](#trigger-094d906c).
3. All change house: owner selector 12 (country/type NEUTRAL; placed owner Neutral).
4. Create/recruit team [Civ_Initiate_G1 (0913A8EC)](all02umd-teams.md#team-0913a8ec).
5. Create/recruit team [Civ_Initiate_G2 (09138CBC)](all02umd-teams.md#team-09138cbc).
6. Create/recruit team [Civ_Initiate_G3 (0913BDCC)](all02umd-teams.md#team-0913bdcc).
7. Create/recruit team [Civ_Initiate_G4 (0913AEFC)](all02umd-teams.md#team-0913aefc).
8. Stop location sound 234 at waypoint 234 (cell 109, 124).
9. Stop location sound 235 at waypoint 235 (cell 136, 79).
10. Stop location sound 236 at waypoint 236 (no location in this map's waypoint table).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14335, Events line 14590, Actions line 14845.

<a id="trigger-094d906c"></a>

### 93. New_Mission - 094D906C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinders_Gone (0CDDC84C)](#trigger-0cddc84c).

Attached scope: tag definitions 094DDCAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_NewMissionObjective.
2. Display message “Objective: Destroy all enemy buildings” (MISSION:YuriBase).
3. Enable and reset applicable timers for [NewMissionText (04627BCC)](#trigger-04627bcc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14336, Events line 14591, Actions line 14846.

<a id="trigger-04627bcc"></a>

### 94. NewMissionText - 04627BCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [New_Mission (094D906C)](#trigger-094d906c).

Attached scope: tag definitions 0462658C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Destroy all enemy buildings” (MISSION:YuriBase).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14337, Events line 14592, Actions line 14847.

<a id="trigger-08feb28c"></a>

### 95. Civ_CleanUp1A - 08FEB28C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_BeachFemale (0BA8977C)](all02umd-teams.md#team-0ba8977c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_BeachMale (0BA88EFC)](all02umd-teams.md#team-0ba88efc).
3. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_Female (0BA8945C)](all02umd-teams.md#team-0ba8945c).
4. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_GreenMale (0BA88BDC)](all02umd-teams.md#team-0ba88bdc).
5. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_SnowFat (0BA89A9C)](all02umd-teams.md#team-0ba89a9c).
6. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_ThinMale1 (0BA8A27C)](all02umd-teams.md#team-0ba8a27c).
7. Enable and reset applicable timers for [Civ_CleanUp1B (08FEA9EC)](#trigger-08fea9ec).
8. Disable [Civ_CleanUp1A (08FEB28C)](#trigger-08feb28c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14338, Events line 14593, Actions line 14848.

<a id="trigger-08fea9ec"></a>

### 96. Civ_CleanUp1B - 08FEA9EC

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Civ_CleanUp1A (08FEB28C)](#trigger-08feb28c).

Incoming activation links: enable from [Civ_CleanUp1A (08FEB28C)](#trigger-08feb28c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Civ_BeachFemale_Final (097451AC)](all02umd-teams.md#team-097451ac).
2. Create/recruit team [Civ_BeachMale_Final (0974585C)](all02umd-teams.md#team-0974585c).
3. Create/recruit team [Civ_Female_Final (09745ABC)](all02umd-teams.md#team-09745abc).
4. Create/recruit team [Civ_GreenMale_Final (097455FC)](all02umd-teams.md#team-097455fc).
5. Create/recruit team [Civ_SnowFat_Final (0974773C)](all02umd-teams.md#team-0974773c).
6. Create/recruit team [Civ_ThinMale_Final (0974572C)](all02umd-teams.md#team-0974572c).
7. Enable and reset applicable timers for [Civ_CleanUp2A (08FEA69C)](#trigger-08fea69c).
8. Disable [Civ_CleanUp1B (08FEA9EC)](#trigger-08fea9ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14339, Events line 14594, Actions line 14849.

<a id="trigger-08fea69c"></a>

### 97. Civ_CleanUp2A - 08FEA69C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Civ_CleanUp1B (08FEA9EC)](#trigger-08fea9ec).

Incoming activation links: enable from [Civ_CleanUp1B (08FEA9EC)](#trigger-08fea9ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_BeachFemale (0B1132FC)](all02umd-teams.md#team-0b1132fc).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_BeachMale (0B11342C)](all02umd-teams.md#team-0b11342c).
3. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_Female (0B11355C)](all02umd-teams.md#team-0b11355c).
4. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_SnowFemale (0B114EFC)](all02umd-teams.md#team-0b114efc).
5. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_SnowMale (0B1131CC)](all02umd-teams.md#team-0b1131cc).
6. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_ThinMale (0B1138FC)](all02umd-teams.md#team-0b1138fc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14340, Events line 14595, Actions line 14850.

<a id="trigger-0cddc53c"></a>

### 98. Cheer - 0CDDC53C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win_Check (0CDDECBC)](#trigger-0cddecbc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14341, Events line 14596, Actions line 14851.

<a id="trigger-0cddc22c"></a>

### 99. Mission_Over - 0CDDC22C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Cheer (0CDDC53C)](#trigger-0cddc53c).

Incoming activation links: enable from [Win_Check (0CDDECBC)](#trigger-0cddecbc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14342, Events line 14597, Actions line 14852.

<a id="trigger-0cddd74c"></a>

### 100. Base_Gone - 0CDDD74C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CDDD66C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
2. Destroyed,  Buildings,  All: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Set local flag 0 (Base_Gone).
2. Disable [Base_Gone (0CDDD74C)](#trigger-0cddd74c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14343, Events line 14598, Actions line 14853.

<a id="trigger-0cddecbc"></a>

### 101. Win_Check - 0CDDECBC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Mission_Over (0CDDC22C)](#trigger-0cddc22c).

Attached scope: tag definitions 0CDDC31C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Grinders_Gone) is set.
2. local flag 0 (Base_Gone) is set.

Flag writers in this mission: set local flag 1 (Grinders_Gone) at [Check_Grinders (0C42981C)](#trigger-0c42981c); set local flag 0 (Base_Gone) at [Base_Gone (0CDDD74C)](#trigger-0cddd74c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Cheer (0CDDC53C)](#trigger-0cddc53c).
2. Enable and reset applicable timers for [Mission_Over (0CDDC22C)](#trigger-0cddc22c).
3. Disable [Win_Check (0CDDECBC)](#trigger-0cddecbc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14344, Events line 14599, Actions line 14854.

<a id="trigger-065c3edc"></a>

### 102. BodyBuilder_Discovered - 065C3EDC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Stallone (08E32CFC)](#trigger-08e32cfc); enable from [Grinder3_Attacked (0464E91C)](#trigger-0464e91c).

Attached scope: Bodybuilder (STLN), owner Neutral, cell (156, 74), tag 065C688C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Create/recruit team [TEAM_BodyBuilder (090311FC)](all02umd-teams.md#team-090311fc).
3. Play voice notification Mis_xA2_GGIThankYou.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14345, Events line 14600, Actions line 14855.

<a id="trigger-08e7ff3c"></a>

### 103. All_Russkies_Gone - 08E7FF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08E7FC4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Wakeup_Tanks (08E7FB5C)](#trigger-08e7fb5c).
2. Disable [All_Russkies_Gone (08E7FF3C)](#trigger-08e7ff3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14346, Events line 14601, Actions line 14856.

<a id="trigger-08e7fb5c"></a>

### 104. Wakeup_Tanks - 08E7FB5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [All_Russkies_Gone (08E7FF3C)](#trigger-08e7ff3c).

Attached scope: tag definitions 08E7F47C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14347, Events line 14602, Actions line 14857.

<a id="trigger-08e32cfc"></a>

### 105. Start_Stallone - 08E32CFC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Lasher Light Tank (LTNK), owner YuriCountry, cell (158, 81), tag 08E3237C, persistence mode 2; Lasher Light Tank (LTNK), owner YuriCountry, cell (161, 79), tag 08E3237C, persistence mode 2; Yuri Barracks (YABRCK), owner Yuri4, cell (157, 77), tag 08E3237C, persistence mode 2; Bio Reactor (YAPOWR), owner Yuri4, cell (159, 74), tag 08E3237C, persistence mode 2; Bio Reactor (YAPOWR), owner Yuri2, cell (164, 78), tag 08E3237C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BodyBuilder_Discovered (065C3EDC)](#trigger-065c3edc).
2. Disable [Start_Stallone (08E32CFC)](#trigger-08e32cfc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14348, Events line 14603, Actions line 14858.

<a id="trigger-0439850c"></a>

### 106. Grinder1_Gone - 0439850C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 2 (Grinder1_Gone).
2. Create crate type 0 at waypoint 92 (cell 105, 128).
3. Disable [G1_Make_BeachFem (09802F3C)](#trigger-09802f3c).
4. Disable [G1_Make_BeachM (0CF2329C)](#trigger-0cf2329c).
5. Disable [G1_Make_Female (0BAD2BBC)](#trigger-0bad2bbc).
6. Disable [G1_Make_Green (0CB5C4BC)](#trigger-0cb5c4bc).
7. Disable [G1_Make_SnowFat (0CB5B3AC)](#trigger-0cb5b3ac).
8. Disable [G1_Make_ThinM (098219BC)](#trigger-098219bc).
9. Enable and reset applicable timers for [Yuri_Taunt_2 (07F40CAC)](#trigger-07f40cac).
10. Disable [Grinder1_Gone (0439850C)](#trigger-0439850c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14349, Events line 14604, Actions line 14859.

<a id="trigger-09802f3c"></a>

### 107. G1_Make_BeachFem - 09802F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1BeachF_Change (0980941C)](#trigger-0980941c).

Attached scope: tag definitions 09802CEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. local flag 22 (IE_Building_Gone) is clear.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c); set local flag 22 (IE_Building_Gone) at [IE_Building_Gone (09801C3C)](#trigger-09801c3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder1_BeachFemaleGo (0B11159C)](all02umd-teams.md#team-0b11159c).
2. Enable and reset applicable timers for [G1BeachF_Change (0980941C)](#trigger-0980941c).
3. Disable [G1_Make_BeachFem (09802F3C)](#trigger-09802f3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14350, Events line 14605, Actions line 14860.

<a id="trigger-0cf2329c"></a>

### 108. G1_Make_BeachM - 0CF2329C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1_BeachM_Change (0460404C)](#trigger-0460404c).

Attached scope: tag definitions 0CF2543C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. local flag 24 (IF_Building_Gone) is clear.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c); set local flag 24 (IF_Building_Gone) at [IF_Building_Gone (046049FC)](#trigger-046049fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder1_BeachMaleGo (0B1111FC)](all02umd-teams.md#team-0b1111fc).
2. Enable and reset applicable timers for [G1_BeachM_Change (0460404C)](#trigger-0460404c).
3. Disable [G1_Make_BeachM (0CF2329C)](#trigger-0cf2329c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14351, Events line 14606, Actions line 14861.

<a id="trigger-0bad2bbc"></a>

### 109. G1_Make_Female - 0BAD2BBC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1Female_Change (0CB5B1DC)](#trigger-0cb5b1dc).

Attached scope: tag definitions 0BAD26CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. local flag 27 (IG_Building_Gone) is clear.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c); set local flag 27 (IG_Building_Gone) at [IG_Building_Gone (09D28AFC)](#trigger-09d28afc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder1_FemaleGo (0B1110CC)](all02umd-teams.md#team-0b1110cc).
2. Enable and reset applicable timers for [G1Female_Change (0CB5B1DC)](#trigger-0cb5b1dc).
3. Disable [G1_Make_Female (0BAD2BBC)](#trigger-0bad2bbc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14352, Events line 14607, Actions line 14862.

<a id="trigger-0cb5c4bc"></a>

### 110. G1_Make_Green - 0CB5C4BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1Green_Change (04E513AC)](#trigger-04e513ac).

Attached scope: tag definitions 0CB5C3DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 28 (IH_Building_Gone) is clear.
2. local flag 2 (Grinder1_Gone) is clear.

Flag writers in this mission: set local flag 28 (IH_Building_Gone) at [IH_Building_Gone (09DE003C)](#trigger-09de003c); set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder1_GreenMaleGo (0B112A1C)](all02umd-teams.md#team-0b112a1c).
2. Enable and reset applicable timers for [G1Green_Change (04E513AC)](#trigger-04e513ac).
3. Disable [G1_Make_Green (0CB5C4BC)](#trigger-0cb5c4bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14353, Events line 14608, Actions line 14863.

<a id="trigger-0cb5b3ac"></a>

### 111. G1_Make_SnowFat - 0CB5B3AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1SnowFat_Change (09826D7C)](#trigger-09826d7c).

Attached scope: tag definitions 0CB5B2CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 30 (II_Building_Gone) is clear.
2. local flag 2 (Grinder1_Gone) is clear.

Flag writers in this mission: set local flag 30 (II_Building_Gone) at [II_Building_Gone (0982574C)](#trigger-0982574c); set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder1_SnowFatGo (0B11267C)](all02umd-teams.md#team-0b11267c).
2. Enable and reset applicable timers for [G1SnowFat_Change (09826D7C)](#trigger-09826d7c).
3. Disable [G1_Make_SnowFat (0CB5B3AC)](#trigger-0cb5b3ac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14354, Events line 14609, Actions line 14864.

<a id="trigger-098219bc"></a>

### 112. G1_Make_ThinM - 098219BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1ThinM_Change (0CB5C2EC)](#trigger-0cb5c2ec).

Attached scope: tag definitions 0982B5FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 32 (IJ_Building_Gone) is clear.
2. local flag 2 (Grinder1_Gone) is clear.

Flag writers in this mission: set local flag 32 (IJ_Building_Gone) at [IJ_Building_Gone (04EB32BC)](#trigger-04eb32bc); set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder1_ThinMaleGo (0B1122DC)](all02umd-teams.md#team-0b1122dc).
2. Enable and reset applicable timers for [G1ThinM_Change (0CB5C2EC)](#trigger-0cb5c2ec).
3. Disable [G1_Make_ThinM (098219BC)](#trigger-098219bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14355, Events line 14610, Actions line 14865.

<a id="trigger-07f40cac"></a>

### 113. Yuri_Taunt_2 - 07F40CAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder1_Gone (0439850C)](#trigger-0439850c); enable from [Grinder2_Gone (0439EDBC)](#trigger-0439edbc); enable from [Grinder3_Gone (0439EAAC)](#trigger-0439eaac); enable from [Grinder4_Gone (0439E79C)](#trigger-0439e79c).

Attached scope: tag definitions 07F4039C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_YuriLeave.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14356, Events line 14611, Actions line 14866.

<a id="trigger-0980941c"></a>

### 114. G1BeachF_Change - 0980941C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1_Make_BeachFem (09802F3C)](#trigger-09802f3c).

Attached scope: tag definitions 0980D67C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 60 configured time units expires (the editor describes a 50%-150% range).
2. local flag 23 (Change_G1BeachF) is set.

Flag writers in this mission: clear local flag 23 (Change_G1BeachF) at [G1BeachF_Change (0980941C)](#trigger-0980941c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_BeachFemaleGo (0B11159C)](all02umd-teams.md#team-0b11159c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_BeachF_Change (0CDC467C)](all02umd-teams.md#team-0cdc467c).
3. Create/recruit team [Grinder1_BeachF_Change (0CDC467C)](all02umd-teams.md#team-0cdc467c).
4. Clear local flag 23 (Change_G1BeachF).
5. Enable and reset applicable timers for [G1_Make_BeachFem (09802F3C)](#trigger-09802f3c).
6. Disable [G1BeachF_Change (0980941C)](#trigger-0980941c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14357, Events line 14612, Actions line 14867.

<a id="trigger-0460404c"></a>

### 115. G1_BeachM_Change - 0460404C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1_Make_BeachM (0CF2329C)](#trigger-0cf2329c).

Attached scope: tag definitions 04602B9C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 60 configured time units expires (the editor describes a 50%-150% range).
2. local flag 25 (Change_G1BeachM) is set.

Flag writers in this mission: clear local flag 25 (Change_G1BeachM) at [G1_BeachM_Change (0460404C)](#trigger-0460404c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_BeachMaleGo (0B1111FC)](all02umd-teams.md#team-0b1111fc).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_BeachM_Change (0974031C)](all02umd-teams.md#team-0974031c).
3. Create/recruit team [Grinder1_BeachM_Change (0974031C)](all02umd-teams.md#team-0974031c).
4. Clear local flag 25 (Change_G1BeachM).
5. Enable and reset applicable timers for [G1_Make_BeachM (0CF2329C)](#trigger-0cf2329c).
6. Disable [G1_BeachM_Change (0460404C)](#trigger-0460404c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14358, Events line 14613, Actions line 14868.

<a id="trigger-0cb5b1dc"></a>

### 116. G1Female_Change - 0CB5B1DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1_Make_Female (0BAD2BBC)](#trigger-0bad2bbc).

Attached scope: tag definitions 0CB5B0FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 60 configured time units expires (the editor describes a 50%-150% range).
2. local flag 26 (Change_G1Female) is set.

Flag writers in this mission: clear local flag 26 (Change_G1Female) at [G1Female_Change (0CB5B1DC)](#trigger-0cb5b1dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_FemaleGo (0B1110CC)](all02umd-teams.md#team-0b1110cc).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_Female_Change (09D29EFC)](all02umd-teams.md#team-09d29efc).
3. Create/recruit team [Grinder1_Female_Change (09D29EFC)](all02umd-teams.md#team-09d29efc).
4. Clear local flag 26 (Change_G1Female).
5. Enable and reset applicable timers for [G1_Make_Female (0BAD2BBC)](#trigger-0bad2bbc).
6. Disable [G1Female_Change (0CB5B1DC)](#trigger-0cb5b1dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14359, Events line 14614, Actions line 14869.

<a id="trigger-04e513ac"></a>

### 117. G1Green_Change - 04E513AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1_Make_Green (0CB5C4BC)](#trigger-0cb5c4bc).

Attached scope: tag definitions 04E5594C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 60 configured time units expires (the editor describes a 50%-150% range).
2. local flag 29 (Change_G1Green) is set.

Flag writers in this mission: clear local flag 29 (Change_G1Green) at [G1Green_Change (04E513AC)](#trigger-04e513ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_GreenMaleGo (0B112A1C)](all02umd-teams.md#team-0b112a1c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_Green_Change (0CA5D54C)](all02umd-teams.md#team-0ca5d54c).
3. Create/recruit team [Grinder1_Green_Change (0CA5D54C)](all02umd-teams.md#team-0ca5d54c).
4. Clear local flag 29 (Change_G1Green).
5. Enable and reset applicable timers for [G1_Make_Green (0CB5C4BC)](#trigger-0cb5c4bc).
6. Disable [G1Green_Change (04E513AC)](#trigger-04e513ac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14360, Events line 14615, Actions line 14870.

<a id="trigger-09826d7c"></a>

### 118. G1SnowFat_Change - 09826D7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1_Make_SnowFat (0CB5B3AC)](#trigger-0cb5b3ac).

Attached scope: tag definitions 098259DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 60 configured time units expires (the editor describes a 50%-150% range).
2. local flag 31 (Change_G1SnowFat) is set.

Flag writers in this mission: clear local flag 31 (Change_G1SnowFat) at [G1SnowFat_Change (09826D7C)](#trigger-09826d7c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_SnowFatGo (0B11267C)](all02umd-teams.md#team-0b11267c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_SnowFat_Change (0CA5D1AC)](all02umd-teams.md#team-0ca5d1ac).
3. Create/recruit team [Grinder1_SnowFat_Change (0CA5D1AC)](all02umd-teams.md#team-0ca5d1ac).
4. Clear local flag 31 (Change_G1SnowFat).
5. Enable and reset applicable timers for [G1_Make_SnowFat (0CB5B3AC)](#trigger-0cb5b3ac).
6. Disable [G1SnowFat_Change (09826D7C)](#trigger-09826d7c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14361, Events line 14616, Actions line 14871.

<a id="trigger-0cb5c2ec"></a>

### 119. G1ThinM_Change - 0CB5C2EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G1_Make_ThinM (098219BC)](#trigger-098219bc).

Attached scope: tag definitions 0CB5C20C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 60 configured time units expires (the editor describes a 50%-150% range).
2. local flag 33 (Change_G1ThinM) is set.

Flag writers in this mission: clear local flag 33 (Change_G1ThinM) at [G1ThinM_Change (0CB5C2EC)](#trigger-0cb5c2ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_ThinMaleGo (0B1122DC)](all02umd-teams.md#team-0b1122dc).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder1_ThinMale_Change (0CA5EC8C)](all02umd-teams.md#team-0ca5ec8c).
3. Create/recruit team [Grinder1_ThinMale_Change (0CA5EC8C)](all02umd-teams.md#team-0ca5ec8c).
4. Clear local flag 33 (Change_G1ThinM).
5. Enable and reset applicable timers for [G1_Make_ThinM (098219BC)](#trigger-098219bc).
6. Disable [G1ThinM_Change (0CB5C2EC)](#trigger-0cb5c2ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14362, Events line 14617, Actions line 14872.

<a id="trigger-0439edbc"></a>

### 120. Grinder2_Gone - 0439EDBC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Grinder (YAGRND), owner Yuri3, cell (128, 78), tag 0439EB9C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 3 (Grinder2_Gone).
2. Create crate type 0 at waypoint 91 (cell 129, 79).
3. Disable [Grinder2_BeachFemale (097BA8EC)](#trigger-097ba8ec).
4. Disable [Grinder2_BeachMale (097BAABC)](#trigger-097baabc).
5. Disable [Grinder2_Female (097BAF3C)](#trigger-097baf3c).
6. Disable [Grinder2_SnowFemale (097BA30C)](#trigger-097ba30c).
7. Disable [Grinder2_SnowMale (097BA71C)](#trigger-097ba71c).
8. Disable [Grinder2_ThinMale (0978639C)](#trigger-0978639c).
9. Enable and reset applicable timers for [Yuri_Taunt_2 (07F40CAC)](#trigger-07f40cac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14363, Events line 14618, Actions line 14873.

<a id="trigger-0439eaac"></a>

### 121. Grinder3_Gone - 0439EAAC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 4 (Grinder3_Gone).
2. Create crate type 0 at waypoint 90 (cell 153, 71).
3. Enable and reset applicable timers for [Yuri_Taunt_2 (07F40CAC)](#trigger-07f40cac).
4. Disable [Grinder3_Gone (0439EAAC)](#trigger-0439eaac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14364, Events line 14619, Actions line 14874.

<a id="trigger-0439e79c"></a>

### 122. Grinder4_Gone - 0439E79C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Grinder (YAGRND), owner Yuri3, cell (193, 102), tag 0439E57C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 5 (Grinder4_Gone).
2. Create crate type 0 at waypoint 89 (cell 194, 103).
3. Enable and reset applicable timers for [Yuri_Taunt_2 (07F40CAC)](#trigger-07f40cac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14365, Events line 14620, Actions line 14875.

<a id="trigger-0d20aa9c"></a>

### 123. Start_Grinder_Pings - 0D20AA9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Stop_Grinder_Pings (0D1FE81C)](#trigger-0d1fe81c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 8 (Player_Has_Radar) is set.

Flag writers in this mission: set local flag 8 (Player_Has_Radar) at [Player_Builds_AC (0C43BA4C)](#trigger-0c43ba4c); clear local flag 8 (Player_Has_Radar) at [Player_Lost_AC (08D7DCCC)](#trigger-08d7dccc); set local flag 8 (Player_Has_Radar) at [Player_Builds_SpySat (0C43CF3C)](#trigger-0c43cf3c); clear local flag 8 (Player_Has_Radar) at [Player_Lost_SpySat (08D7D2BC)](#trigger-08d7d2bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Grinder_Text_WP (0C43032C)](#trigger-0c43032c).
2. Enable and reset applicable timers for [Ping_Grinder1 (0D20A85C)](#trigger-0d20a85c).
3. Enable and reset applicable timers for [Ping_Grinder2 (08D7EBEC)](#trigger-08d7ebec).
4. Enable and reset applicable timers for [Ping_Grinder3 (08D7E3EC)](#trigger-08d7e3ec).
5. Enable and reset applicable timers for [Ping_Grinder4 (08D7FF3C)](#trigger-08d7ff3c).
6. Enable and reset applicable timers for [Stop_Grinder_Pings (0D1FE81C)](#trigger-0d1fe81c).
7. Disable [Grinder_Text_WoP (0D18503C)](#trigger-0d18503c).
8. Disable [Start_Grinder_Pings (0D20AA9C)](#trigger-0d20aa9c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14366, Events line 14621, Actions line 14876.

<a id="trigger-0c43032c"></a>

### 124. Grinder_Text_WP - 0C43032C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Grinder_Pings (0D20AA9C)](#trigger-0d20aa9c).

Attached scope: tag definitions 0C431DAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Grinders_Gone) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 1 (Grinders_Gone) at [Check_Grinders (0C42981C)](#trigger-0c42981c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Display message “Objective: Destroy all Grinders in the city” (MISSION:Grinders).
2. Enable and reset applicable timers for [LAX_Hint (088703CC)](#trigger-088703cc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14367, Events line 14622, Actions line 14877.

<a id="trigger-0d20a85c"></a>

### 125. Ping_Grinder1 - 0D20A85C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Grinder_Pings (0D20AA9C)](#trigger-0d20aa9c).

Attached scope: tag definitions 0D20A12C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create radar-event marker type 11 at waypoint 468 (cell 107, 131).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14368, Events line 14623, Actions line 14878.

<a id="trigger-08d7ebec"></a>

### 126. Ping_Grinder2 - 08D7EBEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Grinder_Pings (0D20AA9C)](#trigger-0d20aa9c).

Attached scope: tag definitions 08D7E88C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create radar-event marker type 11 at waypoint 469 (cell 131, 81).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14369, Events line 14624, Actions line 14879.

<a id="trigger-08d7e3ec"></a>

### 127. Ping_Grinder3 - 08D7E3EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Grinder_Pings (0D20AA9C)](#trigger-0d20aa9c).

Attached scope: tag definitions 08D7E08C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (Grinder3_Gone) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 4 (Grinder3_Gone) at [Grinder3_Gone (0439EAAC)](#trigger-0439eaac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create radar-event marker type 11 at waypoint 470 (cell 156, 73).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14370, Events line 14625, Actions line 14880.

<a id="trigger-08d7ff3c"></a>

### 128. Ping_Grinder4 - 08D7FF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Grinder_Pings (0D20AA9C)](#trigger-0d20aa9c).

Attached scope: tag definitions 08D7FBDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (Grinder4_Gone) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create radar-event marker type 11 at waypoint 471 (cell 197, 105).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14371, Events line 14626, Actions line 14881.

<a id="trigger-0d1fe81c"></a>

### 129. Stop_Grinder_Pings - 0D1FE81C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start_Grinder_Pings (0D20AA9C)](#trigger-0d20aa9c).

Incoming activation links: enable from [Start_Grinder_Pings (0D20AA9C)](#trigger-0d20aa9c).

Attached scope: tag definitions 0D20A94C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 8 (Player_Has_Radar) is clear.

Flag writers in this mission: set local flag 8 (Player_Has_Radar) at [Player_Builds_AC (0C43BA4C)](#trigger-0c43ba4c); clear local flag 8 (Player_Has_Radar) at [Player_Lost_AC (08D7DCCC)](#trigger-08d7dccc); set local flag 8 (Player_Has_Radar) at [Player_Builds_SpySat (0C43CF3C)](#trigger-0c43cf3c); clear local flag 8 (Player_Has_Radar) at [Player_Lost_SpySat (08D7D2BC)](#trigger-08d7d2bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Grinder_Text_WP (0C43032C)](#trigger-0c43032c).
2. Disable [Ping_Grinder1 (0D20A85C)](#trigger-0d20a85c).
3. Disable [Ping_Grinder2 (08D7EBEC)](#trigger-08d7ebec).
4. Disable [Ping_Grinder3 (08D7E3EC)](#trigger-08d7e3ec).
5. Disable [Ping_Grinder4 (08D7FF3C)](#trigger-08d7ff3c).
6. Enable and reset applicable timers for [Start_Grinder_Pings (0D20AA9C)](#trigger-0d20aa9c).
7. Enable and reset applicable timers for [Grinder_Text_WoP (0D18503C)](#trigger-0d18503c).
8. Disable [Stop_Grinder_Pings (0D1FE81C)](#trigger-0d1fe81c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14372, Events line 14627, Actions line 14882.

<a id="trigger-0d18503c"></a>

### 130. Grinder_Text_WoP - 0D18503C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Stop_Grinder_Pings (0D1FE81C)](#trigger-0d1fe81c).

Attached scope: tag definitions 0D17A04C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 1 (Grinders_Gone) is clear.

Flag writers in this mission: set local flag 1 (Grinders_Gone) at [Check_Grinders (0C42981C)](#trigger-0c42981c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Display message “Objective: Destroy all Grinders in the city” (MISSION:Grinders).
2. Enable and reset applicable timers for [LAX_Hint (088703CC)](#trigger-088703cc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14373, Events line 14628, Actions line 14883.

<a id="trigger-088703cc"></a>

### 131. LAX_Hint - 088703CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Grinder_Text_WP (0C43032C)](#trigger-0c43032c); enable from [Grinder_Text_WoP (0D18503C)](#trigger-0d18503c).

Attached scope: tag definitions 0887136C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building does not exist: type index 329 (global list position: Hollywood Bowl (CALA04)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Display message “Hint: Capture LAX to gain access to paratroopers” (MISSION:LAX).
2. Disable [LAX_Hint (088703CC)](#trigger-088703cc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14374, Events line 14629, Actions line 14884.

<a id="trigger-0c43ba4c"></a>

### 132. Player_Builds_AC - 0C43BA4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Lost_AC (08D7DCCC)](#trigger-08d7dccc).

Attached scope: tag definitions 0C43B75C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 135 (global list position: Air Force Command Headquarters (AMRADR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 6 (Player_Has_AC).
2. Set local flag 8 (Player_Has_Radar).
3. Enable and reset applicable timers for [Player_Lost_AC (08D7DCCC)](#trigger-08d7dccc).
4. Disable [Player_Builds_AC (0C43BA4C)](#trigger-0c43ba4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14375, Events line 14630, Actions line 14885.

<a id="trigger-08d7dccc"></a>

### 133. Player_Lost_AC - 08D7DCCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Builds_AC (0C43BA4C)](#trigger-0c43ba4c).

Attached scope: tag definitions 08D7D47C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 135 (global list position: Air Force Command Headquarters (AMRADR)). A map-local type-list change can affect index interpretation.
2. local flag 8 (Player_Has_Radar) is set.
3. local flag 7 (Player_Has_SpySat) is clear.

Flag writers in this mission: set local flag 8 (Player_Has_Radar) at [Player_Builds_AC (0C43BA4C)](#trigger-0c43ba4c); clear local flag 8 (Player_Has_Radar) at [Player_Lost_AC (08D7DCCC)](#trigger-08d7dccc); set local flag 8 (Player_Has_Radar) at [Player_Builds_SpySat (0C43CF3C)](#trigger-0c43cf3c); clear local flag 8 (Player_Has_Radar) at [Player_Lost_SpySat (08D7D2BC)](#trigger-08d7d2bc); set local flag 7 (Player_Has_SpySat) at [Player_Builds_SpySat (0C43CF3C)](#trigger-0c43cf3c); clear local flag 7 (Player_Has_SpySat) at [Player_Lost_SpySat (08D7D2BC)](#trigger-08d7d2bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 8 (Player_Has_Radar).
2. Clear local flag 6 (Player_Has_AC).
3. Enable and reset applicable timers for [Player_Builds_AC (0C43BA4C)](#trigger-0c43ba4c).
4. Disable [Player_Lost_AC (08D7DCCC)](#trigger-08d7dccc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14376, Events line 14631, Actions line 14886.

<a id="trigger-0c43cf3c"></a>

### 134. Player_Builds_SpySat - 0C43CF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Lost_SpySat (08D7D2BC)](#trigger-08d7d2bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Building Type: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 7 (Player_Has_SpySat).
2. Set local flag 8 (Player_Has_Radar).
3. Enable and reset applicable timers for [Force_Fire_Flint (0926703C)](#trigger-0926703c).
4. Disable [Player_Builds_SpySat (0C43CF3C)](#trigger-0c43cf3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14377, Events line 14632, Actions line 14887.

<a id="trigger-0926703c"></a>

### 135. Force_Fire_Flint - 0926703C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Builds_SpySat (0C43CF3C)](#trigger-0c43cf3c).

Incoming activation links: enable from [Player_Builds_SpySat (0C43CF3C)](#trigger-0c43cf3c).

Attached scope: tag definitions 0C43CBEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 64 (Flint_Found) is clear.

Flag writers in this mission: set local flag 64 (Flint_Found) at [Discover_Cowboy (0916204C)](#trigger-0916204c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Force [Discover_Cowboy (0916204C)](#trigger-0916204c).
2. Disable [Force_Fire_Flint (0926703C)](#trigger-0926703c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14378, Events line 14633, Actions line 14888.

<a id="trigger-08d7d2bc"></a>

### 136. Player_Lost_SpySat - 08D7D2BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D7ECDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.
2. local flag 8 (Player_Has_Radar) is set.
3. local flag 6 (Player_Has_AC) is clear.

Flag writers in this mission: set local flag 8 (Player_Has_Radar) at [Player_Builds_AC (0C43BA4C)](#trigger-0c43ba4c); clear local flag 8 (Player_Has_Radar) at [Player_Lost_AC (08D7DCCC)](#trigger-08d7dccc); set local flag 8 (Player_Has_Radar) at [Player_Builds_SpySat (0C43CF3C)](#trigger-0c43cf3c); clear local flag 8 (Player_Has_Radar) at [Player_Lost_SpySat (08D7D2BC)](#trigger-08d7d2bc); set local flag 6 (Player_Has_AC) at [Player_Builds_AC (0C43BA4C)](#trigger-0c43ba4c); clear local flag 6 (Player_Has_AC) at [Player_Lost_AC (08D7DCCC)](#trigger-08d7dccc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 8 (Player_Has_Radar).
2. Clear local flag 7 (Player_Has_SpySat).
3. Enable and reset applicable timers for [Player_Builds_SpySat (0C43CF3C)](#trigger-0c43cf3c).
4. Disable [Player_Lost_SpySat (08D7D2BC)](#trigger-08d7d2bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14379, Events line 14634, Actions line 14889.

<a id="trigger-0c42981c"></a>

### 137. Check_Grinders - 0C42981C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C42909C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Grinder1_Gone) is set.
2. local flag 3 (Grinder2_Gone) is set.
3. local flag 4 (Grinder3_Gone) is set.
4. local flag 5 (Grinder4_Gone) is set.

Flag writers in this mission: set local flag 2 (Grinder1_Gone) at [Grinder1_Gone (0439850C)](#trigger-0439850c); set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc); set local flag 4 (Grinder3_Gone) at [Grinder3_Gone (0439EAAC)](#trigger-0439eaac); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 1 (Grinders_Gone).
2. Enable and reset applicable timers for [Grinders_Gone (0CDDC84C)](#trigger-0cddc84c).
3. Disable [Check_Grinders (0C42981C)](#trigger-0c42981c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14380, Events line 14635, Actions line 14890.

<a id="trigger-0e69e72c"></a>

### 138. Bridge1_Broke - 0E69E72C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge1_Fixed (0BC61C6C)](#trigger-0bc61c6c).

Attached scope: 1 tagged map cells: (112, 155); tag 0E69E38C, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Clear local flag 9 (Bridge1_Fixed).
2. Enable and reset applicable timers for [Bridge1_Fixed (0BC61C6C)](#trigger-0bc61c6c).
3. Enable and reset applicable timers for [Bridge1_Fixer_Team (0D10FEDC)](#trigger-0d10fedc).
4. Disable [Bridge1_Broke (0E69E72C)](#trigger-0e69e72c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14381, Events line 14636, Actions line 14891.

<a id="trigger-0bc61c6c"></a>

### 139. Bridge1_Fixed - 0BC61C6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge1_Broke (0E69E72C)](#trigger-0e69e72c).

Attached scope: Bridge Repair Hut (CABHUT), owner Neutral, cell (102, 157), tag 0BC6588C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector -1 (unresolved or special selector).

**Then perform these actions in order:**

1. Set local flag 9 (Bridge1_Fixed).
2. Enable and reset applicable timers for [Bridge1_Broke (0E69E72C)](#trigger-0e69e72c).
3. Disable [Bridge1_Fixer_Team (0D10FEDC)](#trigger-0d10fedc).
4. Disable [Bridge1_Fixed (0BC61C6C)](#trigger-0bc61c6c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14382, Events line 14637, Actions line 14892.

<a id="trigger-0d10fedc"></a>

### 140. Bridge1_Fixer_Team - 0D10FEDC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge1_Broke (0E69E72C)](#trigger-0e69e72c).

Attached scope: tag definitions 0D10F76C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 9 (Bridge1_Fixed) is clear.

Flag writers in this mission: clear local flag 9 (Bridge1_Fixed) at [Bridge1_Broke (0E69E72C)](#trigger-0e69e72c); set local flag 9 (Bridge1_Fixed) at [Bridge1_Fixed (0BC61C6C)](#trigger-0bc61c6c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Bridge1_Fixer (0D10EEFC)](all02umd-teams.md#team-0d10eefc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14383, Events line 14638, Actions line 14893.

<a id="trigger-0e69db4c"></a>

### 141. Bridge2_Broke - 0E69DB4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge2_Fixed (0BC6785C)](#trigger-0bc6785c).

Attached scope: 1 tagged map cells: (112, 150); tag 0E69D91C, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Clear local flag 10 (Bridge2_Fixed).
2. Enable and reset applicable timers for [Bridge2_Fixed (0BC6785C)](#trigger-0bc6785c).
3. Enable and reset applicable timers for [Bridge2_Fixer_Team (08E06BAC)](#trigger-08e06bac).
4. Disable [Bridge2_Broke (0E69DB4C)](#trigger-0e69db4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14384, Events line 14639, Actions line 14894.

<a id="trigger-0bc6785c"></a>

### 142. Bridge2_Fixed - 0BC6785C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge2_Broke (0E69DB4C)](#trigger-0e69db4c).

Attached scope: Bridge Repair Hut (CABHUT), owner Neutral, cell (102, 148), tag 0437895C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector -1 (unresolved or special selector).

**Then perform these actions in order:**

1. Set local flag 10 (Bridge2_Fixed).
2. Enable and reset applicable timers for [Bridge2_Broke (0E69DB4C)](#trigger-0e69db4c).
3. Disable [Bridge2_Fixer_Team (08E06BAC)](#trigger-08e06bac).
4. Disable [Bridge2_Fixed (0BC6785C)](#trigger-0bc6785c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14385, Events line 14640, Actions line 14895.

<a id="trigger-08e06bac"></a>

### 143. Bridge2_Fixer_Team - 08E06BAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge2_Broke (0E69DB4C)](#trigger-0e69db4c).

Attached scope: tag definitions 08E065EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 10 (Bridge2_Fixed) is clear.

Flag writers in this mission: clear local flag 10 (Bridge2_Fixed) at [Bridge2_Broke (0E69DB4C)](#trigger-0e69db4c); set local flag 10 (Bridge2_Fixed) at [Bridge2_Fixed (0BC6785C)](#trigger-0bc6785c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Bridge2_Fixer (0D10D67C)](all02umd-teams.md#team-0d10d67c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14386, Events line 14641, Actions line 14896.

<a id="trigger-0e69bf3c"></a>

### 144. Bridge3_Broke - 0E69BF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge3_Fixed (0D15DE1C)](#trigger-0d15de1c).

Attached scope: 1 tagged map cells: (130, 61); tag 0E69CDFC, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Clear local flag 11 (Bridge3_Fixed).
2. Enable and reset applicable timers for [Bridge3_Fixer_Team (0D10E5CC)](#trigger-0d10e5cc).
3. Enable and reset applicable timers for [Bridge3_Fixed (0D15DE1C)](#trigger-0d15de1c).
4. Disable [Bridge3_Broke (0E69BF3C)](#trigger-0e69bf3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14387, Events line 14642, Actions line 14897.

<a id="trigger-0d10e5cc"></a>

### 145. Bridge3_Fixer_Team - 0D10E5CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge3_Broke (0E69BF3C)](#trigger-0e69bf3c).

Attached scope: tag definitions 0D10E31C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 11 (Bridge3_Fixed) is clear.

Flag writers in this mission: clear local flag 11 (Bridge3_Fixed) at [Bridge3_Broke (0E69BF3C)](#trigger-0e69bf3c); set local flag 11 (Bridge3_Fixed) at [Bridge3_Fixed (0D15DE1C)](#trigger-0d15de1c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Bridge3_Fixer (0D0D66EC)](all02umd-teams.md#team-0d0d66ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14388, Events line 14643, Actions line 14898.

<a id="trigger-0d15de1c"></a>

### 146. Bridge3_Fixed - 0D15DE1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge3_Broke (0E69BF3C)](#trigger-0e69bf3c).

Attached scope: Bridge Repair Hut (CABHUT), owner Neutral, cell (123, 63), tag 0D15D47C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector -1 (unresolved or special selector).

**Then perform these actions in order:**

1. Set local flag 11 (Bridge3_Fixed).
2. Enable and reset applicable timers for [Bridge3_Broke (0E69BF3C)](#trigger-0e69bf3c).
3. Disable [Bridge3_Fixer_Team (0D10E5CC)](#trigger-0d10e5cc).
4. Disable [Bridge3_Fixed (0D15DE1C)](#trigger-0d15de1c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14389, Events line 14644, Actions line 14899.

<a id="trigger-0e69cc1c"></a>

### 147. Bridge4_Broke - 0E69CC1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge4_Fixed (0D10E9BC)](#trigger-0d10e9bc).

Attached scope: 1 tagged map cells: (131, 56); tag 0E69C9EC, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Clear local flag 12 (Bridge4_Fixed).
2. Enable and reset applicable timers for [Bridge4_Fixer_Team (0D0D603C)](#trigger-0d0d603c).
3. Enable and reset applicable timers for [Bridge4_Fixed (0D10E9BC)](#trigger-0d10e9bc).
4. Disable [Bridge4_Broke (0E69CC1C)](#trigger-0e69cc1c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14390, Events line 14645, Actions line 14900.

<a id="trigger-0d0d603c"></a>

### 148. Bridge4_Fixer_Team - 0D0D603C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge4_Broke (0E69CC1C)](#trigger-0e69cc1c).

Attached scope: tag definitions 08E10AEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 12 (Bridge4_Fixed) is clear.

Flag writers in this mission: clear local flag 12 (Bridge4_Fixed) at [Bridge4_Broke (0E69CC1C)](#trigger-0e69cc1c); set local flag 12 (Bridge4_Fixed) at [Bridge4_Fixed (0D10E9BC)](#trigger-0d10e9bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Bridge4_Fixer (0D0D777C)](all02umd-teams.md#team-0d0d777c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14391, Events line 14646, Actions line 14901.

<a id="trigger-0d10e9bc"></a>

### 149. Bridge4_Fixed - 0D10E9BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge4_Broke (0E69CC1C)](#trigger-0e69cc1c).

Attached scope: Bridge Repair Hut (CABHUT), owner Neutral, cell (124, 52), tag 0D10E6BC, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector -1 (unresolved or special selector).

**Then perform these actions in order:**

1. Set local flag 12 (Bridge4_Fixed).
2. Enable and reset applicable timers for [Bridge4_Broke (0E69CC1C)](#trigger-0e69cc1c).
3. Disable [Bridge4_Fixer_Team (0D0D603C)](#trigger-0d0d603c).
4. Disable [Bridge4_Fixed (0D10E9BC)](#trigger-0d10e9bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14392, Events line 14647, Actions line 14902.

<a id="trigger-06c3cccc"></a>

### 150. Studio_Patrol - 06C3CCCC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06C3C75C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Studio_Patrol (06C394AC)](all02umd-teams.md#team-06c394ac).
2. Create/recruit team [TEAM_Patrol6 (0960071C)](all02umd-teams.md#team-0960071c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14393, Events line 14648, Actions line 14903.

<a id="trigger-095d099c"></a>

### 151. Germans_Attacked - 095D099C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Initiate (INIT), owner Germans, cell (148, 94), tag 095D042C, persistence mode 0; Initiate (INIT), owner Germans, cell (146, 93), tag 095D042C, persistence mode 0; Initiate (INIT), owner Germans, cell (145, 92), tag 095D042C, persistence mode 0; Initiate (INIT), owner Germans, cell (145, 90), tag 095D042C, persistence mode 0; Initiate (INIT), owner Germans, cell (149, 94), tag 095D042C, persistence mode 0; Initiate (INIT), owner Germans, cell (150, 92), tag 095D042C, persistence mode 0; Initiate (INIT), owner Germans, cell (150, 93), tag 095D042C, persistence mode 0; Initiate (INIT), owner Germans, cell (150, 90), tag 095D042C, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Wakeup_Prisoners (0958149C)](#trigger-0958149c).
2. Enable and reset applicable timers for [Prisoners_Panic (095D033C)](#trigger-095d033c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14394, Events line 14649, Actions line 14904.

<a id="trigger-0958149c"></a>

### 152. Wakeup_Prisoners - 0958149C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Germans_Attacked (095D099C)](#trigger-095d099c).

Attached scope: Civilian (CIVBF), owner Neutral, cell (149, 91), tag 0958AF4C, persistence mode 0; Civilian (CIVBTM), owner Neutral, cell (146, 91), tag 0958AF4C, persistence mode 0; Civilian (CIVSTM), owner Neutral, cell (146, 90), tag 0958AF4C, persistence mode 0; Civilian (CIVSF), owner Neutral, cell (148, 93), tag 0958AF4C, persistence mode 0; Civilian (CIV2), owner Neutral, cell (148, 90), tag 0958AF4C, persistence mode 0; Civilian (CIV1), owner Neutral, cell (149, 92), tag 0958AF4C, persistence mode 0; Civilian (CIVSFM), owner Neutral, cell (147, 92), tag 0958AF4C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Wakeup self; main setting 0.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14395, Events line 14650, Actions line 14905.

<a id="trigger-095d033c"></a>

### 153. Prisoners_Panic - 095D033C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Germans_Attacked (095D099C)](#trigger-095d099c).

Attached scope: tag definitions 095D1E7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Prisoners (096CEA1C)](all02umd-teams.md#team-096cea1c).
2. Disable [Prisoners_Panic (095D033C)](#trigger-095d033c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14396, Events line 14651, Actions line 14906.

<a id="trigger-095fe79c"></a>

### 154. YuriBarrack_Gone - 095FE79C

Owner reference: Yuri4Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 095D885C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 302 (global list position: Bio Reactor (YAPOWR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 13 (Barrack1_Gone).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14397, Events line 14652, Actions line 14907.

<a id="trigger-0c89504c"></a>

### 155. CheeseFactory_Gone - 0C89504C

Owner reference: Nod. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C8943FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 14 (CheeseFact_Gone).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14398, Events line 14653, Actions line 14908.

<a id="trigger-0963aa4c"></a>

### 156. 3L1G_Built - 0963AA4C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0963A2BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 15 (3L1G_Built) is set.

Flag writers in this mission: clear local flag 15 (3L1G_Built) at [3L1G_Built (0963AA4C)](#trigger-0963aa4c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Yuri_3I1G (0B9E4DEC)](all02umd-teams.md#team-0b9e4dec).
2. Clear local flag 15 (3L1G_Built).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14399, Events line 14654, Actions line 14909.

<a id="trigger-0460d72c"></a>

### 157. PlayerLose - 0460D72C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0460D14C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14400, Events line 14655, Actions line 14910.

<a id="trigger-097988cc"></a>

### 158. Player_Has_LAX - 097988CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0979ECDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 329 (global list position: Hollywood Bowl (CALA04)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Disable [Player_Has_LAX (097988CC)](#trigger-097988cc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14401, Events line 14656, Actions line 14911.

<a id="trigger-094d821c"></a>

### 159. Yuri_Taunt - 094D821C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 094D929C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 27 (global list position: Chrono Sphere (GACSPH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Mis_xA2_YuriTaunt.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14402, Events line 14657, Actions line 14912.

<a id="trigger-10a9144c"></a>

### 160. Easy_Money - 10A9144C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14403, Events line 14658, Actions line 14913.

<a id="trigger-096169cc"></a>

### 161. Find_Dino - 096169CC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 58 tagged map cells: (128, 125), (129, 125), (130, 125), (131, 125), (132, 125), (133, 125), (134, 125), (135, 125), (136, 125), (137, 125), (138, 125), (139, 125), (140, 125), (141, 125), (142, 125), (143, 125), (144, 125), (128, 126), (144, 126), (128, 127), (144, 127), (128, 128), (144, 128), (128, 129), (144, 129), (128, 130), (144, 130), (128, 131), (144, 131), (128, 132), (144, 132), (128, 133), (144, 133), (128, 134), (144, 134), (128, 135), (144, 135), (128, 136), (144, 136), (128, 137), (144, 137), (128, 138), (129, 138), (130, 138), (131, 138), (132, 138), (133, 138), (134, 138), (135, 138), (136, 138), (137, 138), (138, 138), (139, 138), (140, 138), (141, 138), (142, 138), (143, 138), (144, 138); tag 09617E0C, persistence mode 0.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Play voice notification Mis_xA2_EvaDinoMovie.
2. Reveal terrain around waypoint 62 (cell 140, 134).
3. Create/recruit team [Rexy (08E2D89C)](all02umd-teams.md#team-08e2d89c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14404, Events line 14659, Actions line 14914.

<a id="trigger-0eb68f3c"></a>

### 162. Easy_Money2 - 0EB68F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Easy_Money (10A9144C)](#trigger-10a9144c).

Attached scope: Flak Cannon (NAFLAK), owner Americans, cell (159, 165), tag 10A95F4C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 4 (country/type BRITISH; placed owner British).
2. Sell the attached building through the scripted sale action.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14405, Events line 14660, Actions line 14915.

<a id="trigger-0bcf2bec"></a>

### 163. Yuri2_Hate_Player - 0BCF2BEC

Owner reference: Yuri2Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BCF76DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14406, Events line 14661, Actions line 14916.

<a id="trigger-096947bc"></a>

### 164. BringOn_MCV - 096947BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09693EEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Allied_MCV (06C6434C)](all02umd-teams.md#team-06c6434c).
2. Supply reinforcement team [GGI_KA_KH (0C720ABC)](all02umd-teams.md#team-0c720abc).
3. Supply reinforcement team [GGI_KB_KG (0C7217DC)](all02umd-teams.md#team-0c7217dc).
4. Supply reinforcement team [GGI_KC_KF (0C72064C)](all02umd-teams.md#team-0c72064c).
5. Supply reinforcement team [GGI_KD_KI (0C72022C)](all02umd-teams.md#team-0c72022c).
6. Supply reinforcement team [GGI_KE_KJ (0C9CFA1C)](all02umd-teams.md#team-0c9cfa1c).
7. Reveal terrain around waypoint 302 (cell 176, 134).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14407, Events line 14662, Actions line 14917.

<a id="trigger-0967de9c"></a>

### 165. BringOn_GIs - 0967DE9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0967D60C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [GI_KP_KK (0C9593CC)](all02umd-teams.md#team-0c9593cc).
2. Supply reinforcement team [GI_KP_KL (0C95CD8C)](all02umd-teams.md#team-0c95cd8c).
3. Supply reinforcement team [GI_KP_KM (0C95C51C)](all02umd-teams.md#team-0c95c51c).
4. Supply reinforcement team [GI_KP_KN (0C809A1C)](all02umd-teams.md#team-0c809a1c).
5. Supply reinforcement team [GI_KP_KO (0C80967C)](all02umd-teams.md#team-0c80967c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14408, Events line 14663, Actions line 14918.

<a id="trigger-09801c3c"></a>

### 166. IE_Building_Gone - 09801C3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CASTL03), owner Neutral, cell (119, 121), tag 09801ACC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 22 (IE_Building_Gone).
2. Disable [G1_Make_BeachFem (09802F3C)](#trigger-09802f3c).
3. Disable [IE_Building_Gone (09801C3C)](#trigger-09801c3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14409, Events line 14664, Actions line 14919.

<a id="trigger-046049fc"></a>

### 167. IF_Building_Gone - 046049FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY12), owner Neutral, cell (114, 116), tag 0460447C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 24 (IF_Building_Gone).
2. Disable [G1_Make_BeachM (0CF2329C)](#trigger-0cf2329c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14410, Events line 14665, Actions line 14920.

<a id="trigger-09d28afc"></a>

### 168. IG_Building_Gone - 09D28AFC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CASTL01), owner Neutral, cell (109, 115), tag 09D2D1FC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 27 (IG_Building_Gone).
2. Disable [G1_Make_Female (0BAD2BBC)](#trigger-0bad2bbc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14411, Events line 14666, Actions line 14921.

<a id="trigger-09de003c"></a>

### 169. IH_Building_Gone - 09DE003C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAPARS13), owner Neutral, cell (88, 134), tag 04E5651C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 28 (IH_Building_Gone).
2. Disable [G1_Make_Green (0CB5C4BC)](#trigger-0cb5c4bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14412, Events line 14667, Actions line 14922.

<a id="trigger-0982574c"></a>

### 170. II_Building_Gone - 0982574C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAPARS06), owner Neutral, cell (114, 112), tag 098254CC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 30 (II_Building_Gone).
2. Disable [G1_Make_SnowFat (0CB5B3AC)](#trigger-0cb5b3ac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14413, Events line 14668, Actions line 14923.

<a id="trigger-04eb32bc"></a>

### 171. IJ_Building_Gone - 04EB32BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Office Building (CATEXS07), owner Neutral, cell (122, 130), tag 04EAA3FC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 32 (IJ_Building_Gone).
2. Disable [G1_Make_ThinM (098219BC)](#trigger-098219bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14414, Events line 14669, Actions line 14924.

<a id="trigger-0c829e5c"></a>

### 172. IK_Building_Gone - 0C829E5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CASTL03), owner Neutral, cell (141, 95), tag 0C829A1C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 40 (IK_Building_Gone).
2. Disable [G2_Make_ThinM (04F34E4C)](#trigger-04f34e4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14415, Events line 14670, Actions line 14925.

<a id="trigger-04f34e4c"></a>

### 173. G2_Make_ThinM - 04F34E4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2ThinM_Change (04F35F3C)](#trigger-04f35f3c).

Attached scope: tag definitions 04F34D6C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. local flag 40 (IK_Building_Gone) is clear.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc); set local flag 40 (IK_Building_Gone) at [IK_Building_Gone (0C829E5C)](#trigger-0c829e5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder2_ThinMaleGo (0B114CBC)](all02umd-teams.md#team-0b114cbc).
2. Enable and reset applicable timers for [G2ThinM_Change (04F35F3C)](#trigger-04f35f3c).
3. Disable [G2_Make_ThinM (04F34E4C)](#trigger-04f34e4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14416, Events line 14671, Actions line 14926.

<a id="trigger-04f35f3c"></a>

### 174. G2ThinM_Change - 04F35F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2_Make_ThinM (04F34E4C)](#trigger-04f34e4c).

Attached scope: tag definitions 04F35E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 36 (Change_G2ThinM) is set.
2. A random delay centered on 70 configured time units expires (the editor describes a 50%-150% range).

Flag writers in this mission: clear local flag 36 (Change_G2ThinM) at [G2ThinM_Change (04F35F3C)](#trigger-04f35f3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_ThinMaleGo (0B114CBC)](all02umd-teams.md#team-0b114cbc).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_ThinM_Change (0C82A68C)](all02umd-teams.md#team-0c82a68c).
3. Create/recruit team [Grinder2_ThinM_Change (0C82A68C)](all02umd-teams.md#team-0c82a68c).
4. Clear local flag 36 (Change_G2ThinM).
5. Enable and reset applicable timers for [G2_Make_ThinM (04F34E4C)](#trigger-04f34e4c).
6. Disable [G2ThinM_Change (04F35F3C)](#trigger-04f35f3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14417, Events line 14672, Actions line 14927.

<a id="trigger-04f2f1bc"></a>

### 175. G2_Make_BeachF - 04F2F1BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2BeachF_Change (04F2D2DC)](#trigger-04f2d2dc).

Attached scope: tag definitions 04F2B94C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. local flag 43 (IN_Building_Gone) is clear.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc); set local flag 43 (IN_Building_Gone) at [IN_Building_Gone (06C0D03C)](#trigger-06c0d03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder2_BeachFemaleGo (0B1141DC)](all02umd-teams.md#team-0b1141dc).
2. Enable and reset applicable timers for [G2BeachF_Change (04F2D2DC)](#trigger-04f2d2dc).
3. Disable [G2_Make_BeachF (04F2F1BC)](#trigger-04f2f1bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14418, Events line 14673, Actions line 14928.

<a id="trigger-04f2d2dc"></a>

### 176. G2BeachF_Change - 04F2D2DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2_Make_BeachF (04F2F1BC)](#trigger-04f2f1bc).

Attached scope: tag definitions 04F2D1FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 39 (Change_G2BeachF) is set.
2. A random delay centered on 70 configured time units expires (the editor describes a 50%-150% range).

Flag writers in this mission: clear local flag 39 (Change_G2BeachF) at [G2BeachF_Change (04F2D2DC)](#trigger-04f2d2dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_BeachFemaleGo (0B1141DC)](all02umd-teams.md#team-0b1141dc).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_BeachF_Change (0CDC42EC)](all02umd-teams.md#team-0cdc42ec).
3. Create/recruit team [Grinder2_BeachF_Change (0CDC42EC)](all02umd-teams.md#team-0cdc42ec).
4. Clear local flag 39 (Change_G2BeachF).
5. Enable and reset applicable timers for [G2_Make_BeachF (04F2F1BC)](#trigger-04f2f1bc).
6. Disable [G2BeachF_Change (04F2D2DC)](#trigger-04f2d2dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14419, Events line 14674, Actions line 14929.

<a id="trigger-04f2a42c"></a>

### 177. G2_Make_BeachM - 04F2A42C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2BeachM_Change (04F2A25C)](#trigger-04f2a25c).

Attached scope: tag definitions 04F2A34C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. local flag 42 (IM_Building_Gone) is clear.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc); set local flag 42 (IM_Building_Gone) at [IM_Building_Gone (06C0F03C)](#trigger-06c0f03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder2_BeachMaleGo (0B11457C)](all02umd-teams.md#team-0b11457c).
2. Enable and reset applicable timers for [G2BeachM_Change (04F2A25C)](#trigger-04f2a25c).
3. Disable [G2_Make_BeachM (04F2A42C)](#trigger-04f2a42c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14420, Events line 14675, Actions line 14930.

<a id="trigger-04f2a25c"></a>

### 178. G2BeachM_Change - 04F2A25C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2_Make_BeachM (04F2A42C)](#trigger-04f2a42c).

Attached scope: tag definitions 04F2A17C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 34 (Change_G2BeachM) is set.
2. A random delay centered on 70 configured time units expires (the editor describes a 50%-150% range).

Flag writers in this mission: clear local flag 34 (Change_G2BeachM) at [G2BeachM_Change (04F2A25C)](#trigger-04f2a25c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_BeachMaleGo (0B11457C)](all02umd-teams.md#team-0b11457c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_BeachM_Change (04EC545C)](all02umd-teams.md#team-04ec545c).
3. Create/recruit team [Grinder2_BeachM_Change (04EC545C)](all02umd-teams.md#team-04ec545c).
4. Clear local flag 34 (Change_G2BeachM).
5. Enable and reset applicable timers for [G2_Make_BeachM (04F2A42C)](#trigger-04f2a42c).
6. Disable [G2BeachM_Change (04F2A25C)](#trigger-04f2a25c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14421, Events line 14676, Actions line 14931.

<a id="trigger-04f3232c"></a>

### 179. G2_Make_Female - 04F3232C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2Female_Change (04F34F3C)](#trigger-04f34f3c).

Attached scope: tag definitions 04F3224C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. local flag 41 (IL_Building_Gone) is clear.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc); set local flag 41 (IL_Building_Gone) at [IL_Building_Gone (06C0703C)](#trigger-06c0703c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder2_FemaleGo (0B11491C)](all02umd-teams.md#team-0b11491c).
2. Enable and reset applicable timers for [G2Female_Change (04F34F3C)](#trigger-04f34f3c).
3. Disable [G2_Make_Female (04F3232C)](#trigger-04f3232c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14422, Events line 14677, Actions line 14932.

<a id="trigger-04f34f3c"></a>

### 180. G2Female_Change - 04F34F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2_Make_Female (04F3232C)](#trigger-04f3232c).

Attached scope: tag definitions 04F3216C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 35 (Change_G2Female) is set.
2. A random delay centered on 70 configured time units expires (the editor describes a 50%-150% range).

Flag writers in this mission: clear local flag 35 (Change_G2Female) at [G2Female_Change (04F34F3C)](#trigger-04f34f3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_FemaleGo (0B11491C)](all02umd-teams.md#team-0b11491c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_Female_Change (0C82B77C)](all02umd-teams.md#team-0c82b77c).
3. Create/recruit team [Grinder2_Female_Change (0C82B77C)](all02umd-teams.md#team-0c82b77c).
4. Clear local flag 35 (Change_G2Female).
5. Enable and reset applicable timers for [G2_Make_Female (04F3232C)](#trigger-04f3232c).
6. Disable [G2Female_Change (04F34F3C)](#trigger-04f34f3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14423, Events line 14678, Actions line 14933.

<a id="trigger-04f35d6c"></a>

### 181. G2_Make_SnowF - 04F35D6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2SnowF_Change (04F35B9C)](#trigger-04f35b9c).

Attached scope: tag definitions 04F35C8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. local flag 45 (IP_Building_Gone) is clear.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc); set local flag 45 (IP_Building_Gone) at [IP_Building_Gone (06C0803C)](#trigger-06c0803c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder2_SnowFemaleGo (0B115A1C)](all02umd-teams.md#team-0b115a1c).
2. Enable and reset applicable timers for [G2SnowF_Change (04F35B9C)](#trigger-04f35b9c).
3. Disable [G2_Make_SnowF (04F35D6C)](#trigger-04f35d6c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14424, Events line 14679, Actions line 14934.

<a id="trigger-04f35b9c"></a>

### 182. G2SnowF_Change - 04F35B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2_Make_SnowF (04F35D6C)](#trigger-04f35d6c).

Attached scope: tag definitions 04F35ABC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 37 (Change_G2SnowF) is set.
2. A random delay centered on 70 configured time units expires (the editor describes a 50%-150% range).

Flag writers in this mission: clear local flag 37 (Change_G2SnowF) at [G2SnowF_Change (04F35B9C)](#trigger-04f35b9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_SnowFemaleGo (0B115A1C)](all02umd-teams.md#team-0b115a1c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_SnowF_Change (0B11B2FC)](all02umd-teams.md#team-0b11b2fc).
3. Create/recruit team [Grinder2_SnowF_Change (0B11B2FC)](all02umd-teams.md#team-0b11b2fc).
4. Clear local flag 37 (Change_G2SnowF).
5. Enable and reset applicable timers for [G2_Make_SnowF (04F35D6C)](#trigger-04f35d6c).
6. Disable [G2SnowF_Change (04F35B9C)](#trigger-04f35b9c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14425, Events line 14680, Actions line 14935.

<a id="trigger-04f359cc"></a>

### 183. G2_Make_SnowM - 04F359CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2SnowM_Change (04F3558C)](#trigger-04f3558c).

Attached scope: tag definitions 04F358EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Grinder2_Gone) is clear.
2. local flag 44 (IO_Building_Gone) is clear.

Flag writers in this mission: set local flag 3 (Grinder2_Gone) at [Grinder2_Gone (0439EDBC)](#trigger-0439edbc); set local flag 44 (IO_Building_Gone) at [IO_Building_Gone (06C0E03C)](#trigger-06c0e03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder2_SnowMaleGo (0B1140AC)](all02umd-teams.md#team-0b1140ac).
2. Enable and reset applicable timers for [G2SnowM_Change (04F3558C)](#trigger-04f3558c).
3. Disable [G2_Make_SnowM (04F359CC)](#trigger-04f359cc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14426, Events line 14681, Actions line 14936.

<a id="trigger-04f3558c"></a>

### 184. G2SnowM_Change - 04F3558C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G2_Make_SnowM (04F359CC)](#trigger-04f359cc).

Attached scope: tag definitions 04F354AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 38 (Change_G2SnowM) is set.
2. A random delay centered on 70 configured time units expires (the editor describes a 50%-150% range).

Flag writers in this mission: clear local flag 38 (Change_G2SnowM) at [G2SnowM_Change (04F3558C)](#trigger-04f3558c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_SnowMaleGo (0B1140AC)](all02umd-teams.md#team-0b1140ac).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder2_SnowM_Change (0C82AAAC)](all02umd-teams.md#team-0c82aaac).
3. Create/recruit team [Grinder2_SnowM_Change (0C82AAAC)](all02umd-teams.md#team-0c82aaac).
4. Clear local flag 38 (Change_G2SnowM).
5. Enable and reset applicable timers for [G2_Make_SnowM (04F359CC)](#trigger-04f359cc).
6. Disable [G2SnowM_Change (04F3558C)](#trigger-04f3558c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14427, Events line 14682, Actions line 14937.

<a id="trigger-06c0703c"></a>

### 185. IL_Building_Gone - 06C0703C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Mini Mall (CALA15), owner Neutral, cell (131, 73), tag 06BF804C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 41 (IL_Building_Gone).
2. Disable [G2_Make_Female (04F3232C)](#trigger-04f3232c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14428, Events line 14683, Actions line 14938.

<a id="trigger-06c0f03c"></a>

### 186. IM_Building_Gone - 06C0F03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Mini Mall (CALA14), owner Neutral, cell (135, 67), tag 06C0C04C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 42 (IM_Building_Gone).
2. Disable [G2_Make_BeachM (04F2A42C)](#trigger-04f2a42c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14429, Events line 14684, Actions line 14939.

<a id="trigger-06c0d03c"></a>

### 187. IN_Building_Gone - 06C0D03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY08), owner Neutral, cell (146, 82), tag 06C0904C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 43 (IN_Building_Gone).
2. Disable [G2_Make_BeachF (04F2F1BC)](#trigger-04f2f1bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14430, Events line 14685, Actions line 14940.

<a id="trigger-06c0e03c"></a>

### 188. IO_Building_Gone - 06C0E03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY07), owner Neutral, cell (137, 94), tag 06C0B04C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 44 (IO_Building_Gone).
2. Disable [G2_Make_SnowM (04F359CC)](#trigger-04f359cc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14431, Events line 14686, Actions line 14941.

<a id="trigger-06c0803c"></a>

### 189. IP_Building_Gone - 06C0803C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAWASH06), owner Neutral, cell (137, 99), tag 06C0A04C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 45 (IP_Building_Gone).
2. Disable [G2_Make_SnowF (04F35D6C)](#trigger-04f35d6c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14432, Events line 14687, Actions line 14942.

<a id="trigger-04e50e1c"></a>

### 190. G4_Make_BeachFat - 04E50E1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4BeachFat_Change (04E5153C)](#trigger-04e5153c).

Attached scope: tag definitions 04E50D3C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 57 (JC_Building_Gone) is clear.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 57 (JC_Building_Gone) at [JC_Building_Gone (0981D57C)](#trigger-0981d57c); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder4_BeachFatGo (0CEC4B5C)](all02umd-teams.md#team-0cec4b5c).
2. Enable and reset applicable timers for [G4BeachFat_Change (04E5153C)](#trigger-04e5153c).
3. Disable [G4_Make_BeachFat (04E50E1C)](#trigger-04e50e1c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14433, Events line 14688, Actions line 14943.

<a id="trigger-04e5153c"></a>

### 191. G4BeachFat_Change - 04E5153C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4_Make_BeachFat (04E50E1C)](#trigger-04e50e1c).

Attached scope: tag definitions 04E5145C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 80 configured time units expires (the editor describes a 50%-150% range).
2. local flag 54 (Change_G4BeachFat) is set.

Flag writers in this mission: clear local flag 54 (Change_G4BeachFat) at [G4BeachFat_Change (04E5153C)](#trigger-04e5153c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_BeachFatGo (0CEC4B5C)](all02umd-teams.md#team-0cec4b5c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_BeachFat_Change (0C83311C)](all02umd-teams.md#team-0c83311c).
3. Create/recruit team [Grinder4_BeachFat_Change (0C83311C)](all02umd-teams.md#team-0c83311c).
4. Clear local flag 54 (Change_G4BeachFat).
5. Enable and reset applicable timers for [G4_Make_BeachFat (04E50E1C)](#trigger-04e50e1c).
6. Disable [G4BeachFat_Change (04E5153C)](#trigger-04e5153c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14434, Events line 14689, Actions line 14944.

<a id="trigger-04e50c4c"></a>

### 192. G4_Make_BeachFem - 04E50C4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4BeachFem_Change (04E5136C)](#trigger-04e5136c).

Attached scope: tag definitions 04E50B6C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 56 (JB_Building_Gone) is clear.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 56 (JB_Building_Gone) at [JB_Building_Gone (0981D97C)](#trigger-0981d97c); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder4_BeachFemaleGo (0CEC4C8C)](all02umd-teams.md#team-0cec4c8c).
2. Enable and reset applicable timers for [G4BeachFem_Change (04E5136C)](#trigger-04e5136c).
3. Disable [G4_Make_BeachFem (04E50C4C)](#trigger-04e50c4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14435, Events line 14690, Actions line 14945.

<a id="trigger-04e5136c"></a>

### 193. G4BeachFem_Change - 04E5136C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4_Make_BeachFem (04E50C4C)](#trigger-04e50c4c).

Attached scope: tag definitions 04E5128C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 80 configured time units expires (the editor describes a 50%-150% range).
2. local flag 47 (Change_G4BeachF) is set.

Flag writers in this mission: clear local flag 47 (Change_G4BeachF) at [G4BeachFem_Change (04E5136C)](#trigger-04e5136c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_BeachFemaleGo (0CEC4C8C)](all02umd-teams.md#team-0cec4c8c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_BeachF_Change (0C834EFC)](all02umd-teams.md#team-0c834efc).
3. Create/recruit team [Grinder4_BeachF_Change (0C834EFC)](all02umd-teams.md#team-0c834efc).
4. Clear local flag 47 (Change_G4BeachF).
5. Enable and reset applicable timers for [G4_Make_BeachFem (04E50C4C)](#trigger-04e50c4c).
6. Disable [G4BeachFem_Change (04E5136C)](#trigger-04e5136c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14436, Events line 14691, Actions line 14946.

<a id="trigger-04e50a7c"></a>

### 194. G4_Make_BeachMale - 04E50A7C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4BeachMale_Change (04E57F3C)](#trigger-04e57f3c).

Attached scope: tag definitions 04E5099C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 55 (JA_Building_Gone) is clear.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 55 (JA_Building_Gone) at [JA_Building_Gone (0981DF3C)](#trigger-0981df3c); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder4_BeachMaleGo (0CEC51DC)](all02umd-teams.md#team-0cec51dc).
2. Enable and reset applicable timers for [G4BeachMale_Change (04E57F3C)](#trigger-04e57f3c).
3. Disable [G4_Make_BeachMale (04E50A7C)](#trigger-04e50a7c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14437, Events line 14692, Actions line 14947.

<a id="trigger-04e57f3c"></a>

### 195. G4BeachMale_Change - 04E57F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4_Make_BeachMale (04E50A7C)](#trigger-04e50a7c).

Attached scope: tag definitions 04E57E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 80 configured time units expires (the editor describes a 50%-150% range).
2. local flag 49 (Change_G4BeachM) is set.

Flag writers in this mission: clear local flag 49 (Change_G4BeachM) at [G4BeachMale_Change (04E57F3C)](#trigger-04e57f3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_BeachMaleGo (0CEC51DC)](all02umd-teams.md#team-0cec51dc).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_BeachMale_Change (0C834DCC)](all02umd-teams.md#team-0c834dcc).
3. Create/recruit team [Grinder4_BeachMale_Change (0C834DCC)](all02umd-teams.md#team-0c834dcc).
4. Clear local flag 49 (Change_G4BeachM).
5. Enable and reset applicable timers for [G4_Make_BeachMale (04E50A7C)](#trigger-04e50a7c).
6. Disable [G4BeachMale_Change (04E57F3C)](#trigger-04e57f3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14438, Events line 14693, Actions line 14948.

<a id="trigger-04e508ac"></a>

### 196. G4_Make_Female - 04E508AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4Female_Change (04E57D6C)](#trigger-04e57d6c).

Attached scope: tag definitions 04E507CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 59 (JE_Building_Gone) is clear.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 59 (JE_Building_Gone) at [JE_Building_Gone (0981FB3C)](#trigger-0981fb3c); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder4_FemaleGo (0CEC48FC)](all02umd-teams.md#team-0cec48fc).
2. Enable and reset applicable timers for [G4Female_Change (04E57D6C)](#trigger-04e57d6c).
3. Disable [G4_Make_Female (04E508AC)](#trigger-04e508ac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14439, Events line 14694, Actions line 14949.

<a id="trigger-04e57d6c"></a>

### 197. G4Female_Change - 04E57D6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4_Make_Female (04E508AC)](#trigger-04e508ac).

Attached scope: tag definitions 04E57C8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 80 configured time units expires (the editor describes a 50%-150% range).
2. local flag 48 (Change_G4Female) is set.

Flag writers in this mission: clear local flag 48 (Change_G4Female) at [G4Female_Change (04E57D6C)](#trigger-04e57d6c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_FemaleGo (0CEC48FC)](all02umd-teams.md#team-0cec48fc).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_Female_Change (0C834C9C)](all02umd-teams.md#team-0c834c9c).
3. Create/recruit team [Grinder4_Female_Change (0C834C9C)](all02umd-teams.md#team-0c834c9c).
4. Clear local flag 48 (Change_G4Female).
5. Enable and reset applicable timers for [G4_Make_Female (04E508AC)](#trigger-04e508ac).
6. Disable [G4Female_Change (04E57D6C)](#trigger-04e57d6c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14440, Events line 14695, Actions line 14950.

<a id="trigger-04e5044c"></a>

### 198. G4_Make_GreenMale - 04E5044C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4Green_Change (04E57B9C)](#trigger-04e57b9c).

Attached scope: tag definitions 04E5036C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 60 (JF_Building_Gone) is clear.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 60 (JF_Building_Gone) at [JF_Building_Gone (0981F73C)](#trigger-0981f73c); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder4_GreenMaleGo (0CEC47CC)](all02umd-teams.md#team-0cec47cc).
2. Enable and reset applicable timers for [G4Green_Change (04E57B9C)](#trigger-04e57b9c).
3. Disable [G4_Make_GreenMale (04E5044C)](#trigger-04e5044c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14441, Events line 14696, Actions line 14951.

<a id="trigger-04e57b9c"></a>

### 199. G4Green_Change - 04E57B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4_Make_GreenMale (04E5044C)](#trigger-04e5044c).

Attached scope: tag definitions 04E57ABC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 80 configured time units expires (the editor describes a 50%-150% range).
2. local flag 50 (Change_G4Green) is set.

Flag writers in this mission: clear local flag 50 (Change_G4Green) at [G4Green_Change (04E57B9C)](#trigger-04e57b9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_GreenMaleGo (0CEC47CC)](all02umd-teams.md#team-0cec47cc).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_Green_Change (0C834B6C)](all02umd-teams.md#team-0c834b6c).
3. Create/recruit team [Grinder4_Green_Change (0C834B6C)](all02umd-teams.md#team-0c834b6c).
4. Clear local flag 50 (Change_G4Green).
5. Enable and reset applicable timers for [G4_Make_GreenMale (04E5044C)](#trigger-04e5044c).
6. Disable [G4Green_Change (04E57B9C)](#trigger-04e57b9c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14442, Events line 14697, Actions line 14952.

<a id="trigger-04e5027c"></a>

### 200. G4_Make_SnowFat - 04E5027C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4SnowFat_Change (04E506DC)](#trigger-04e506dc).

Attached scope: tag definitions 04E51F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 63 (JI_Building_Gone) is clear.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 63 (JI_Building_Gone) at [JI_Building_Gone (04E5256C)](#trigger-04e5256c); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder4_SnowFatGo (0CEC443C)](all02umd-teams.md#team-0cec443c).
2. Enable and reset applicable timers for [G4SnowFat_Change (04E506DC)](#trigger-04e506dc).
3. Disable [G4_Make_SnowFat (04E5027C)](#trigger-04e5027c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14443, Events line 14698, Actions line 14953.

<a id="trigger-04e506dc"></a>

### 201. G4SnowFat_Change - 04E506DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4_Make_SnowFat (04E5027C)](#trigger-04e5027c).

Attached scope: tag definitions 04E505FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 80 configured time units expires (the editor describes a 50%-150% range).
2. local flag 46 (Change_G4SnowFat) is set.

Flag writers in this mission: clear local flag 46 (Change_G4SnowFat) at [G4SnowFat_Change (04E506DC)](#trigger-04e506dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_SnowFatGo (0CEC443C)](all02umd-teams.md#team-0cec443c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_SnowFat_Change (0C834A3C)](all02umd-teams.md#team-0c834a3c).
3. Create/recruit team [Grinder4_SnowFat_Change (0C834A3C)](all02umd-teams.md#team-0c834a3c).
4. Clear local flag 46 (Change_G4SnowFat).
5. Enable and reset applicable timers for [G4_Make_SnowFat (04E5027C)](#trigger-04e5027c).
6. Disable [G4SnowFat_Change (04E506DC)](#trigger-04e506dc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14444, Events line 14699, Actions line 14954.

<a id="trigger-04e51e5c"></a>

### 202. G4_Make_SnowF - 04E51E5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4SnowFem_Change (04E5770C)](#trigger-04e5770c).

Attached scope: tag definitions 04E51A6C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 62 (JH_Building_Gone) is clear.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 62 (JH_Building_Gone) at [JH_Building_Gone (04E5781C)](#trigger-04e5781c); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder4_SnowFemaleGo (0CEC456C)](all02umd-teams.md#team-0cec456c).
2. Enable and reset applicable timers for [G4SnowFem_Change (04E5770C)](#trigger-04e5770c).
3. Disable [G4_Make_SnowF (04E51E5C)](#trigger-04e51e5c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14445, Events line 14700, Actions line 14955.

<a id="trigger-04e5770c"></a>

### 203. G4SnowFem_Change - 04E5770C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4_Make_SnowF (04E51E5C)](#trigger-04e51e5c).

Attached scope: tag definitions 04E5762C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 80 configured time units expires (the editor describes a 50%-150% range).
2. local flag 51 (Change_G4SnowF) is set.

Flag writers in this mission: clear local flag 51 (Change_G4SnowF) at [G4SnowFem_Change (04E5770C)](#trigger-04e5770c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_SnowFemaleGo (0CEC456C)](all02umd-teams.md#team-0cec456c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_SnowF_Change (0462C21C)](all02umd-teams.md#team-0462c21c).
3. Create/recruit team [Grinder4_SnowF_Change (0462C21C)](all02umd-teams.md#team-0462c21c).
4. Clear local flag 51 (Change_G4SnowF).
5. Enable and reset applicable timers for [G4_Make_SnowF (04E51E5C)](#trigger-04e51e5c).
6. Disable [G4SnowFem_Change (04E5770C)](#trigger-04e5770c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14446, Events line 14701, Actions line 14956.

<a id="trigger-04e5197c"></a>

### 204. G4_Make_SnowM - 04E5197C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4SnowMale_Change (04E5753C)](#trigger-04e5753c).

Attached scope: tag definitions 04E5189C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 61 (JG_Building_Gone) is clear.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 61 (JG_Building_Gone) at [JG_Building_Gone (04E50F3C)](#trigger-04e50f3c); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder4_SnowMaleGo (0CEC469C)](all02umd-teams.md#team-0cec469c).
2. Enable and reset applicable timers for [G4SnowMale_Change (04E5753C)](#trigger-04e5753c).
3. Disable [G4_Make_SnowM (04E5197C)](#trigger-04e5197c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14447, Events line 14702, Actions line 14957.

<a id="trigger-04e5753c"></a>

### 205. G4SnowMale_Change - 04E5753C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4_Make_SnowM (04E5197C)](#trigger-04e5197c).

Attached scope: tag definitions 04E51D7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 80 configured time units expires (the editor describes a 50%-150% range).
2. local flag 52 (Change_G4SnowM) is set.

Flag writers in this mission: clear local flag 52 (Change_G4SnowM) at [G4SnowMale_Change (04E5753C)](#trigger-04e5753c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_SnowMaleGo (0CEC469C)](all02umd-teams.md#team-0cec469c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_SnowM_Change (0462C0EC)](all02umd-teams.md#team-0462c0ec).
3. Create/recruit team [Grinder4_SnowM_Change (0462C0EC)](all02umd-teams.md#team-0462c0ec).
4. Clear local flag 52 (Change_G4SnowM).
5. Enable and reset applicable timers for [G4_Make_SnowM (04E5197C)](#trigger-04e5197c).
6. Disable [G4SnowMale_Change (04E5753C)](#trigger-04e5753c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14448, Events line 14703, Actions line 14958.

<a id="trigger-04e517ac"></a>

### 206. G4_Make_ThinMale - 04E517AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4ThinMale_Change (04E51C8C)](#trigger-04e51c8c).

Attached scope: tag definitions 04E516CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 58 (JD_Building_Gone) is clear.
2. local flag 5 (Grinder4_Gone) is clear.

Flag writers in this mission: set local flag 58 (JD_Building_Gone) at [JD_Building_Gone (0981FF3C)](#trigger-0981ff3c); set local flag 5 (Grinder4_Gone) at [Grinder4_Gone (0439E79C)](#trigger-0439e79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Grinder4_ThinMaleGo (0CEC4A2C)](all02umd-teams.md#team-0cec4a2c).
2. Enable and reset applicable timers for [G4ThinMale_Change (04E51C8C)](#trigger-04e51c8c).
3. Disable [G4_Make_ThinMale (04E517AC)](#trigger-04e517ac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14449, Events line 14704, Actions line 14959.

<a id="trigger-04e51c8c"></a>

### 207. G4ThinMale_Change - 04E51C8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [G4_Make_ThinMale (04E517AC)](#trigger-04e517ac).

Attached scope: tag definitions 04E51BAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 80 configured time units expires (the editor describes a 50%-150% range).
2. local flag 53 (Change_G4ThinM) is set.

Flag writers in this mission: clear local flag 53 (Change_G4ThinM) at [G4ThinMale_Change (04E51C8C)](#trigger-04e51c8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_ThinMaleGo (0CEC4A2C)](all02umd-teams.md#team-0cec4a2c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_ThinMale_Change (0462E2FC)](all02umd-teams.md#team-0462e2fc).
3. Create/recruit team [Grinder4_ThinMale_Change (0462E2FC)](all02umd-teams.md#team-0462e2fc).
4. Clear local flag 53 (Change_G4ThinM).
5. Enable and reset applicable timers for [G4_Make_ThinMale (04E517AC)](#trigger-04e517ac).
6. Disable [G4ThinMale_Change (04E51C8C)](#trigger-04e51c8c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14450, Events line 14705, Actions line 14960.

<a id="trigger-0981df3c"></a>

### 208. JA_Building_Gone - 0981DF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY11), owner Neutral, cell (190, 109), tag 0981DA6C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 55 (JA_Building_Gone).
2. Disable [G4_Make_BeachMale (04E50A7C)](#trigger-04e50a7c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14451, Events line 14706, Actions line 14961.

<a id="trigger-0981d97c"></a>

### 209. JB_Building_Gone - 0981D97C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY12), owner Neutral, cell (188, 111), tag 0981D66C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 56 (JB_Building_Gone).
2. Disable [G4_Make_BeachFem (04E50C4C)](#trigger-04e50c4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14452, Events line 14707, Actions line 14962.

<a id="trigger-0981d57c"></a>

### 210. JC_Building_Gone - 0981D57C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAWASH07), owner Neutral, cell (187, 115), tag 0981D26C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 57 (JC_Building_Gone).
2. Disable [G4_Make_BeachFat (04E50E1C)](#trigger-04e50e1c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14453, Events line 14708, Actions line 14963.

<a id="trigger-0981ff3c"></a>

### 211. JD_Building_Gone - 0981FF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAPARS06), owner Neutral, cell (176, 110), tag 0981FC2C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 58 (JD_Building_Gone).
2. Disable [G4_Make_ThinMale (04E517AC)](#trigger-04e517ac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14454, Events line 14709, Actions line 14964.

<a id="trigger-0981fb3c"></a>

### 212. JE_Building_Gone - 0981FB3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAPARS05), owner Neutral, cell (172, 112), tag 0981F82C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 59 (JE_Building_Gone).
2. Disable [G4_Make_Female (04E508AC)](#trigger-04e508ac).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14455, Events line 14710, Actions line 14965.

<a id="trigger-0981f73c"></a>

### 213. JF_Building_Gone - 0981F73C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY12), owner Neutral, cell (167, 105), tag 0981F42C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 60 (JF_Building_Gone).
2. Disable [G4_Make_GreenMale (04E5044C)](#trigger-04e5044c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14456, Events line 14711, Actions line 14966.

<a id="trigger-04e50f3c"></a>

### 214. JG_Building_Gone - 04E50F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY11), owner Neutral, cell (171, 101), tag 04E5790C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 61 (JG_Building_Gone).
2. Disable [G4_Make_SnowM (04E5197C)](#trigger-04e5197c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14457, Events line 14712, Actions line 14967.

<a id="trigger-04e5781c"></a>

### 215. JH_Building_Gone - 04E5781C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Office Building (CATEXS07), owner Neutral, cell (177, 97), tag 04E5265C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 62 (JH_Building_Gone).
2. Disable [G4_Make_SnowF (04E51E5C)](#trigger-04e51e5c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14458, Events line 14713, Actions line 14968.

<a id="trigger-04e5256c"></a>

### 216. JI_Building_Gone - 04E5256C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAPARS04), owner Neutral, cell (169, 112), tag 04E56D1C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 63 (JI_Building_Gone).
2. Disable [G4_Make_SnowFat (04E5027C)](#trigger-04e5027c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14459, Events line 14714, Actions line 14969.

<a id="trigger-0b0f83ec"></a>

### 217. Enter_Bunkers - 0B0F83EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B0F968C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TankBunk1 (0793150C)](all02umd-teams.md#team-0793150c).
2. Supply reinforcement team [TankBunk2 (0A0A42CC)](all02umd-teams.md#team-0a0a42cc).
3. Supply reinforcement team [TankBunk3 (060E1EFC)](all02umd-teams.md#team-060e1efc).
4. Supply reinforcement team [TankBunk4 (07ABF46C)](all02umd-teams.md#team-07abf46c).
5. Supply reinforcement team [TankBunk5 (07ABF33C)](all02umd-teams.md#team-07abf33c).
6. Supply reinforcement team [TankBunk6 (07ABF20C)](all02umd-teams.md#team-07abf20c).
7. Supply reinforcement team [TankBunk7 (07ABF0DC)](all02umd-teams.md#team-07abf0dc).
8. Supply reinforcement team [TankBunk8 (08CC9E2C)](all02umd-teams.md#team-08cc9e2c).
9. Supply reinforcement team [TankBunk9 (060F620C)](all02umd-teams.md#team-060f620c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14460, Events line 14715, Actions line 14970.

<a id="trigger-04ef835c"></a>

### 218. Enter_Reactors1 - 04EF835C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04EFF78C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [ReactorTeamBS (0915F83C)](all02umd-teams.md#team-0915f83c).
2. Supply reinforcement team [ReactorTeamBT (0915F2CC)](all02umd-teams.md#team-0915f2cc).
3. Supply reinforcement team [ReactorTeamBU (0915F19C)](all02umd-teams.md#team-0915f19c).
4. Supply reinforcement team [ReactorTeamBV (0915DEFC)](all02umd-teams.md#team-0915defc).
5. Supply reinforcement team [ReactorTeamBW (0915DDCC)](all02umd-teams.md#team-0915ddcc).
6. Supply reinforcement team [ReactorTeamBX (0915DC9C)](all02umd-teams.md#team-0915dc9c).
7. Supply reinforcement team [ReactorTeamBY (0915DB6C)](all02umd-teams.md#team-0915db6c).
8. Supply reinforcement team [ReactorTeamBZ (0915DA3C)](all02umd-teams.md#team-0915da3c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14461, Events line 14716, Actions line 14971.

<a id="trigger-0618f5cc"></a>

### 219. Explain_BattleFortress - 0618F5CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0618DC2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 6 (global list position: Allied Battle Lab (GATECH)). A map-local type-list change can affect index interpretation.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Switch the sidebar to tab 3.
2. Flash cameo/type BFRT; additional configured duration/location argument 120.
3. Play voice notification Unit_Eva_BattleFortress.
4. Enable and reset applicable timers for [BF_Reinforcement (07AC738C)](#trigger-07ac738c).
5. Supply reinforcement team [BattleFortress1 (07F0E85C)](all02umd-teams.md#team-07f0e85c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14462, Events line 14717, Actions line 14972.

<a id="trigger-07ac738c"></a>

### 220. BF_Reinforcement - 07AC738C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Explain_BattleFortress (0618F5CC)](#trigger-0618f5cc).

Attached scope: tag definitions 07AC8F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 95 (cell 170, 132).
2. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14463, Events line 14718, Actions line 14973.

<a id="trigger-07f39f3c"></a>

### 221. Control_Bus - 07F39F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F39A4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14464, Events line 14719, Actions line 14974.

<a id="trigger-07f31bac"></a>

### 222. Control_Bus2 - 07F31BAC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F3162C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14465, Events line 14720, Actions line 14975.

<a id="trigger-07f3122c"></a>

### 223. Control_Bus3 - 07F3122C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F32F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14466, Events line 14721, Actions line 14976.

<a id="trigger-092c9d5c"></a>

### 224. Garrison_Medium - 092C9D5C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 092C9A4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yuri_Gar_CW_CX (092BDBCC)](all02umd-teams.md#team-092bdbcc).
2. Supply reinforcement team [Yuri_Gar_CY_CZ (092BD7CC)](all02umd-teams.md#team-092bd7cc).
3. Supply reinforcement team [Yuri_Gar_DF (092B952C)](all02umd-teams.md#team-092b952c).
4. Supply reinforcement team [Yuri_Gar_DG (092BFC8C)](all02umd-teams.md#team-092bfc8c).
5. Supply reinforcement team [Yuri_Gar_DH (092BFB5C)](all02umd-teams.md#team-092bfb5c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14467, Events line 14722, Actions line 14977.

<a id="trigger-0976df3c"></a>

### 225. Amb_Traffic1 - 0976DF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0976DD1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 118 (cell 150, 128).
2. Play sound _Amb_UrbanMurmur2 at waypoint 119 (cell 164, 113).
3. Play sound _Amb_Traffic at waypoint 120 (cell 143, 101).
4. Play sound _Amb_UrbanMurmur1 at waypoint 121 (cell 138, 115).
5. Play sound _Amb_UrbanMurmur2 at waypoint 122 (cell 156, 92).
6. Play sound _Amb_Traffic at waypoint 123 (cell 174, 98).
7. Play sound _Amb_UrbanMurmur1 at waypoint 124 (cell 189, 103).
8. Play sound _Amb_UrbanMurmur2 at waypoint 125 (cell 151, 78).
9. Play sound _Amb_Traffic at waypoint 126 (cell 139, 88).
10. Play sound _Amb_UrbanMurmur1 at waypoint 127 (cell 125, 110).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14468, Events line 14723, Actions line 14978.

<a id="trigger-0799a05c"></a>

### 226. Amb_Traffic2 - 0799A05C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0799B5FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 128 (cell 143, 157).
2. Play sound _Amb_UrbanMurmur2 at waypoint 129 (cell 123, 151).
3. Play sound _Amb_Traffic at waypoint 133 (cell 110, 146).
4. Play sound _Amb_UrbanMurmur1 at waypoint 134 (cell 95, 151).
5. Play sound _Amb_UrbanMurmur2 at waypoint 135 (cell 119, 137).
6. Play sound _Amb_Traffic at waypoint 136 (cell 129, 120).
7. Play sound _Amb_UrbanMurmur1 at waypoint 137 (cell 171, 80).
8. Play sound _Amb_UrbanMurmur2 at waypoint 138 (cell 150, 58).
9. Play sound _Amb_Traffic at waypoint 127 (cell 125, 110).
10. Play sound _Amb_UrbanMurmur1 at waypoint 139 (cell 137, 59).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14469, Events line 14724, Actions line 14979.

<a id="trigger-079a7ccc"></a>

### 227. Amb_Traffic3 - 079A7CCC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079A075C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_Traffic at waypoint 137 (cell 171, 80).
2. Play sound _Amb_UrbanMurmur1 at waypoint 138 (cell 150, 58).
3. Play sound _Amb_UrbanMurmur2 at waypoint 139 (cell 137, 59).
4. Play sound _Amb_Traffic at waypoint 140 (cell 120, 55).
5. Play sound _Amb_UrbanMurmur1 at waypoint 141 (cell 134, 102).
6. Play sound _Amb_UrbanMurmur2 at waypoint 142 (cell 113, 167).
7. Play sound _Amb_Traffic at waypoint 143 (cell 89, 149).
8. Play sound _Amb_UrbanMurmur1 at waypoint 144 (cell 70, 135).
9. Play sound _Amb_UrbanMurmur2 at waypoint 145 (cell 48, 119).
10. Play sound _Amb_Traffic at waypoint 146 (cell 90, 118).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14470, Events line 14725, Actions line 14980.

<a id="trigger-0799254c"></a>

### 228. Amb_Beach1 - 0799254C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0799953C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsBeach at waypoint 147 (cell 51, 139).
2. Play sound _Amb_BirdsHarbor at waypoint 148 (cell 68, 143).
3. Play sound _Amb_BirdsBeach at waypoint 149 (cell 81, 151).
4. Play sound _Amb_BirdsHarbor at waypoint 150 (cell 90, 166).
5. Play sound _Amb_BirdsBeach at waypoint 151 (cell 99, 182).
6. Play sound _Amb_BirdsHarbor at waypoint 152 (cell 107, 188).
7. Play sound _Amb_BirdsBeach at waypoint 153 (cell 117, 191).
8. Play sound _Amb_BirdsHarbor at waypoint 154 (cell 97, 174).
9. Play sound _Amb_BirdsBeach at waypoint 155 (cell 103, 192).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14471, Events line 14726, Actions line 14981.

<a id="trigger-079a475c"></a>

### 229. Amb_Beach2 - 079A475C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079A57FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 160 (cell 111, 194).
2. Play sound _Amb_OceanLight at waypoint 161 (cell 100, 197).
3. Play sound _Amb_OceanHeavy at waypoint 162 (cell 93, 183).
4. Play sound _Amb_OceanLight at waypoint 163 (cell 81, 171).
5. Play sound _Amb_OceanHeavy at waypoint 164 (cell 81, 157).
6. Play sound _Amb_OceanLight at waypoint 165 (cell 70, 150).
7. Play sound _Amb_OceanHeavy at waypoint 166 (cell 51, 144).
8. Play sound _Amb_OceanLight at waypoint 167 (cell 59, 155).
9. Play sound _Amb_OceanHeavy at waypoint 168 (cell 73, 160).
10. Play sound _Amb_OceanLight at waypoint 169 (cell 83, 181).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14472, Events line 14727, Actions line 14982.

<a id="trigger-079a506c"></a>

### 230. Amb_Birds1 - 079A506C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079A4C4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsTemperate1 at waypoint 170 (cell 71, 119).
2. Play sound _Amb_BirdsTemperate2 at waypoint 171 (cell 118, 99).
3. Play sound _Amb_BirdsPark at waypoint 172 (cell 125, 81).
4. Play sound _Amb_BirdsTemperate1 at waypoint 173 (cell 182, 103).
5. Play sound _Amb_BirdsTemperate2 at waypoint 174 (cell 124, 90).
6. Play sound _Amb_BirdsPark at waypoint 175 (cell 108, 94).
7. Play sound _Amb_BirdsTemperate1 at waypoint 176 (cell 111, 76).
8. Play sound _Amb_BirdsTemperate2 at waypoint 177 (cell 121, 71).
9. Play sound _Amb_BirdsPark at waypoint 178 (cell 123, 31).
10. Play sound _Amb_BirdsTemperate1 at waypoint 179 (cell 118, 42).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14473, Events line 14728, Actions line 14983.

<a id="trigger-079966dc"></a>

### 231. Amb_Birds2 - 079966DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0799E68C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsTemperate1 at waypoint 180 (cell 101, 101).
2. Play sound _Amb_BirdsTemperate2 at waypoint 181 (cell 94, 108).
3. Play sound _Amb_BirdsPark at waypoint 183 (cell 78, 109).
4. Play sound _Amb_BirdsTemperate1 at waypoint 184 (cell 65, 110).
5. Play sound _Amb_BirdsTemperate2 at waypoint 185 (cell 35, 117).
6. Play sound _Amb_BirdsPark at waypoint 186 (cell 44, 106).
7. Play sound _Amb_BirdsTemperate1 at waypoint 187 (cell 57, 104).
8. Play sound _Amb_BirdsTemperate2 at waypoint 188 (cell 72, 102).
9. Play sound _Amb_BirdsPark at waypoint 189 (cell 87, 97).
10. Play sound _Amb_BirdsTemperate1 at waypoint 190 (cell 105, 85).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14474, Events line 14729, Actions line 14984.

<a id="trigger-079a666c"></a>

### 232. Amb_Birds3 - 079A666C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079A13FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsTemperate1 at waypoint 191 (cell 115, 65).
2. Play sound _Amb_BirdsTemperate2 at waypoint 192 (cell 103, 46).
3. Play sound _Amb_BirdsPark at waypoint 193 (cell 90, 49).
4. Play sound _Amb_BirdsTemperate1 at waypoint 194 (cell 98, 68).
5. Play sound _Amb_BirdsTemperate2 at waypoint 195 (cell 95, 83).
6. Play sound _Amb_BirdsPark at waypoint 196 (cell 62, 96).
7. Play sound _Amb_BirdsTemperate1 at waypoint 197 (cell 64, 83).
8. Play sound _Amb_BirdsTemperate2 at waypoint 198 (cell 80, 82).
9. Play sound _Amb_BirdsPark at waypoint 199 (cell 77, 65).
10. Play sound _Amb_BirdsTemperate1 at waypoint 200 (cell 87, 69).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14475, Events line 14730, Actions line 14985.

<a id="trigger-08fedb2c"></a>

### 233. Civ_CleanUp2B - 08FEDB2C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Civ_CleanUp2A (08FEA69C)](#trigger-08fea69c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Civ_BeachFemale_Final (097451AC)](all02umd-teams.md#team-097451ac).
2. Create/recruit team [Civ_BeachMale_Final (0974585C)](all02umd-teams.md#team-0974585c).
3. Create/recruit team [Civ_Female_Final (09745ABC)](all02umd-teams.md#team-09745abc).
4. Create/recruit team [Civ_SnowFemale_Final (0974598C)](all02umd-teams.md#team-0974598c).
5. Create/recruit team [Civ_ThinMale_Final (0974572C)](all02umd-teams.md#team-0974572c).
6. Create/recruit team [Civ_SnowMale_Final (097454CC)](all02umd-teams.md#team-097454cc).
7. Enable and reset applicable timers for [Civ_CleanUp4A (08FED55C)](#trigger-08fed55c).
8. Disable [Civ_CleanUp2B (08FEDB2C)](#trigger-08fedb2c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14476, Events line 14731, Actions line 14986.

<a id="trigger-08fed55c"></a>

### 234. Civ_CleanUp4A - 08FED55C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Civ_CleanUp2B (08FEDB2C)](#trigger-08fedb2c).

Incoming activation links: enable from [Civ_CleanUp2B (08FEDB2C)](#trigger-08fedb2c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_BeachFat (0BA90A2C)](all02umd-teams.md#team-0ba90a2c).
2. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_BeachFemale (0BA90B5C)](all02umd-teams.md#team-0ba90b5c).
3. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_BeachMale (0BA90C8C)](all02umd-teams.md#team-0ba90c8c).
4. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_Female (0BA907EC)](all02umd-teams.md#team-0ba907ec).
5. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_GreenMale (0BA9058C)](all02umd-teams.md#team-0ba9058c).
6. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_SnowFat (0BA9783C)](all02umd-teams.md#team-0ba9783c).
7. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_SnowFemale (0BA9045C)](all02umd-teams.md#team-0ba9045c).
8. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_SnowMale (0BA9032C)](all02umd-teams.md#team-0ba9032c).
9. Enable and reset applicable timers for [Civ_CleanUp4B (08FEFB2C)](#trigger-08fefb2c).
10. Disable [Civ_CleanUp4A (08FED55C)](#trigger-08fed55c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14477, Events line 14732, Actions line 14987.

<a id="trigger-08fefb2c"></a>

### 235. Civ_CleanUp4B - 08FEFB2C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Civ_CleanUp4A (08FED55C)](#trigger-08fed55c).

Incoming activation links: enable from [Civ_CleanUp4A (08FED55C)](#trigger-08fed55c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Grinder4_ThinMale (0BA906BC)](all02umd-teams.md#team-0ba906bc).
2. Create/recruit team [Civ_BeachFat_Final (0BC6669C)](all02umd-teams.md#team-0bc6669c).
3. Create/recruit team [Civ_BeachFemale_Final (097451AC)](all02umd-teams.md#team-097451ac).
4. Create/recruit team [Civ_BeachMale_Final (0974585C)](all02umd-teams.md#team-0974585c).
5. Create/recruit team [Civ_Female_Final (09745ABC)](all02umd-teams.md#team-09745abc).
6. Create/recruit team [Civ_GreenMale_Final (097455FC)](all02umd-teams.md#team-097455fc).
7. Create/recruit team [Civ_SnowFat_Final (0974773C)](all02umd-teams.md#team-0974773c).
8. Create/recruit team [Civ_SnowFemale_Final (0974598C)](all02umd-teams.md#team-0974598c).
9. Enable and reset applicable timers for [Civ_CleanUp4C (08FEC06C)](#trigger-08fec06c).
10. Disable [Civ_CleanUp4B (08FEFB2C)](#trigger-08fefb2c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14478, Events line 14733, Actions line 14988.

<a id="trigger-08fec06c"></a>

### 236. Civ_CleanUp4C - 08FEC06C

Owner reference: Yuri2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Civ_CleanUp4B (08FEFB2C)](#trigger-08fefb2c).

Incoming activation links: enable from [Civ_CleanUp4B (08FEFB2C)](#trigger-08fefb2c).

Attached scope: tag definitions 08FE9F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Civ_SnowMale_Final (097454CC)](all02umd-teams.md#team-097454cc).
2. Create/recruit team [Civ_ThinMale_Final (0974572C)](all02umd-teams.md#team-0974572c).
3. Disable [Civ_CleanUp4C (08FEC06C)](#trigger-08fec06c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14479, Events line 14734, Actions line 14989.

<a id="trigger-088f344c"></a>

### 237. Civ_Cheer - 088F344C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 088FB07C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 12 (country/type NEUTRAL; placed owner Neutral).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14480, Events line 14735, Actions line 14990.

<a id="trigger-0926286c"></a>

### 238. Generic_Male_Slave - 0926286C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Male_Slave_Delay (09261B4C)](#trigger-09261b4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound LCiv2Select.
2. Enable and reset applicable timers for [Male_Slave_Delay (09261B4C)](#trigger-09261b4c).
3. Disable [Generic_Male_Slave (0926286C)](#trigger-0926286c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14481, Events line 14736, Actions line 14991.

<a id="trigger-09261b4c"></a>

### 239. Male_Slave_Delay - 09261B4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Generic_Male_Slave (0926286C)](#trigger-0926286c).

Incoming activation links: enable from [Generic_Male_Slave (0926286C)](#trigger-0926286c).

Attached scope: tag definitions 0926160C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Generic_Male_Slave (0926286C)](#trigger-0926286c).
2. Disable [Male_Slave_Delay (09261B4C)](#trigger-09261b4c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14482, Events line 14737, Actions line 14992.

<a id="trigger-0926f53c"></a>

### 240. Generic_Female_Slave - 0926F53C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Female_Slave_Delay (0926F36C)](#trigger-0926f36c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound LCiv4Select.
2. Enable and reset applicable timers for [Female_Slave_Delay (0926F36C)](#trigger-0926f36c).
3. Disable [Generic_Female_Slave (0926F53C)](#trigger-0926f53c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14483, Events line 14738, Actions line 14993.

<a id="trigger-0926f36c"></a>

### 241. Female_Slave_Delay - 0926F36C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Generic_Female_Slave (0926F53C)](#trigger-0926f53c).

Incoming activation links: enable from [Generic_Female_Slave (0926F53C)](#trigger-0926f53c).

Attached scope: tag definitions 0926F45C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Generic_Female_Slave (0926F53C)](#trigger-0926f53c).
2. Disable [Female_Slave_Delay (0926F36C)](#trigger-0926f36c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14484, Events line 14739, Actions line 14994.

<a id="trigger-07bc86ec"></a>

### 242. Generic_Female_2 - 07BC86EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Generic_Female_2D (07BC81BC)](#trigger-07bc81bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound LCiv3Select.
2. Enable and reset applicable timers for [Generic_Female_2D (07BC81BC)](#trigger-07bc81bc).
3. Disable [Generic_Female_2 (07BC86EC)](#trigger-07bc86ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14485, Events line 14740, Actions line 14995.

<a id="trigger-07bc81bc"></a>

### 243. Generic_Female_2D - 07BC81BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Generic_Female_2 (07BC86EC)](#trigger-07bc86ec).

Incoming activation links: enable from [Generic_Female_2 (07BC86EC)](#trigger-07bc86ec).

Attached scope: tag definitions 07BC860C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Generic_Female_2 (07BC86EC)](#trigger-07bc86ec).
2. Disable [Generic_Female_2D (07BC81BC)](#trigger-07bc81bc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14486, Events line 14741, Actions line 14996.

<a id="trigger-07bcf5ec"></a>

### 244. Generic_Male_2 - 07BCF5EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Generic_Male_2D (07BCF41C)](#trigger-07bcf41c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound LCiv2Select.
2. Enable and reset applicable timers for [Generic_Male_2D (07BCF41C)](#trigger-07bcf41c).
3. Disable [Generic_Male_2 (07BCF5EC)](#trigger-07bcf5ec).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14487, Events line 14742, Actions line 14997.

<a id="trigger-07bcf41c"></a>

### 245. Generic_Male_2D - 07BCF41C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Generic_Male_2 (07BCF5EC)](#trigger-07bcf5ec).

Incoming activation links: enable from [Generic_Male_2 (07BCF5EC)](#trigger-07bcf5ec).

Attached scope: tag definitions 07BCF50C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Generic_Male_2 (07BCF5EC)](#trigger-07bcf5ec).
2. Disable [Generic_Male_2D (07BCF41C)](#trigger-07bcf41c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14488, Events line 14743, Actions line 14998.

<a id="trigger-090a9f3c"></a>

### 246. Find_Hospital - 090A9F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Civilian Hospital (CATHOSP), owner Special, cell (64, 129), tag 090A9A7C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.
2. global flag 13 is clear.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 201 (cell 67, 130).
2. Flash buildings of type CATHOSP; duration argument 40.
3. Create radar-event marker type 12 at waypoint 201 (cell 67, 130).
4. Play voice notification Unit_Eva_TechHospital.
5. Set global flag 13.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14489, Events line 14744, Actions line 14999.

<a id="trigger-0915431c"></a>

### 247. Find_MachineShop - 0915431C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tech Machine Shop (CAMACH), owner Special, cell (171, 91), tag 09155EBC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.
2. global flag 12 is clear.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 202 (cell 172, 92).
2. Flash buildings of type CAMACH; duration argument 40.
3. Create radar-event marker type 12 at waypoint 202 (cell 172, 92).
4. Play voice notification Unit_Eva_TechMachShop.
5. Set global flag 12.

Source locator: expandmd01.mix/all02umd.map; Triggers line 14490, Events line 14745, Actions line 15000.

<a id="trigger-04f2a9ac"></a>

### 248. Player_Builds_WF - 04F2A9AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04F2A21C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. At least 1 instances of Allied War Factory (GAWEAP) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hard_Cheese1 (0796E03C)](#trigger-0796e03c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14491, Events line 14746, Actions line 15001.

<a id="trigger-0464e91c"></a>

### 249. Grinder3_Attacked - 0464E91C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Grinder3_Gone (0439EAAC)](#trigger-0439eaac).

Attached scope: Grinder (YAGRND), owner Yuri3, cell (151, 69), tag 0439E88C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BodyBuilder_Discovered (065C3EDC)](#trigger-065c3edc).
2. Disable [Grinder3_Attacked (0464E91C)](#trigger-0464e91c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14492, Events line 14747, Actions line 15002.

<a id="trigger-07f7dacc"></a>

### 250. Grinder1_Attacked - 07F7DACC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Grinder1_Gone (0439850C)](#trigger-0439850c).

Attached scope: Grinder (YAGRND), owner Yuri3, cell (104, 127), tag 0439817C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change_Hero (0ABAE7BC)](#trigger-0abae7bc).
2. Disable [Grinder1_Attacked (07F7DACC)](#trigger-07f7dacc).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14493, Events line 14748, Actions line 15003.

<a id="trigger-0464860c"></a>

### 251. Cowboy_Backup - 0464860C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 36 tagged map cells: (155, 119), (156, 119), (157, 119), (155, 120), (156, 120), (157, 120), (158, 120), (159, 120), (155, 121), (159, 121), (154, 122), (155, 122), (159, 122), (160, 122), (161, 122), (154, 123), (159, 123), (160, 123), (161, 123), (154, 124), (155, 124), (158, 124), (159, 124), (160, 124), (161, 124), (155, 125), (158, 125), (159, 125), (160, 125), (155, 126), (156, 126), (157, 126), (158, 126), (159, 126), (157, 127), (158, 127); tag 09D2AE5C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 64 (Flint_Found) is clear.
2. Entered or Overflown By: owner selector 0 (country/type AMERICANS; placed owner Americans).

Flag writers in this mission: set local flag 64 (Flint_Found) at [Discover_Cowboy (0916204C)](#trigger-0916204c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Discover_Cowboy (0916204C)](#trigger-0916204c).
2. Disable [Select_Flint (07A40B2C)](#trigger-07a40b2c).
3. Disable [Discover_Trigger (09D2968C)](#trigger-09d2968c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14494, Events line 14749, Actions line 15004.

<a id="trigger-07a40b2c"></a>

### 252. Select_Flint - 07A40B2C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Discover_Cowboy (0916204C)](#trigger-0916204c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.
2. local flag 64 (Flint_Found) is clear.

Flag writers in this mission: set local flag 64 (Flint_Found) at [Discover_Cowboy (0916204C)](#trigger-0916204c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Discover_Cowboy (0916204C)](#trigger-0916204c).
2. Disable [Cowboy_Backup (0464860C)](#trigger-0464860c).
3. Disable [Discover_Trigger (09D2968C)](#trigger-09d2968c).
4. Disable [Select_Flint (07A40B2C)](#trigger-07a40b2c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14495, Events line 14750, Actions line 15005.

<a id="trigger-09d2968c"></a>

### 253. Discover_Trigger - 09D2968C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Select_Flint (07A40B2C)](#trigger-07a40b2c).

Attached scope: Cowboy (CLNT), owner Neutral, cell (157, 123), tag 09163AFC, persistence mode 2.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Discover_Cowboy (0916204C)](#trigger-0916204c).
2. Disable [Cowboy_Backup (0464860C)](#trigger-0464860c).
3. Disable [Select_Flint (07A40B2C)](#trigger-07a40b2c).
4. Disable [Discover_Trigger (09D2968C)](#trigger-09d2968c).

Source locator: expandmd01.mix/all02umd.map; Triggers line 14496, Events line 14751, Actions line 15006.

[All team rosters and ordered plans](all02umd-teams.md) | [All mission overrides](all02umd-overrides.md)
