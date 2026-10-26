# Operation: Power Play

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for all03umd.map.](../../images/map-all03umd.svg)

*Initial placement schematic for all03umd.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** all03umd.map. **Effective extracted member:** mapsmd03.mix/all03umd.map. **Trigger definitions:** 376.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all03umd-teams.md) | [All mission overrides](all03umd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Americans |
| Theater | NEWURBAN |
| Map size | 0,0,90,110 |
| Visible local rectangle | 15,13,60,80 |
| Placed vehicles | 80 |
| Placed infantry | 96 |
| Placed structures | 183 |
| Placed aircraft | 0 |
| Team templates | 204 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 100 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 0 | Africans |
| 6 | Arabs | 0 | Arabs |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 0 | Russians |
| 9 | YuriCountry | 400 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 0 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |
| 14 | PPTFHouse | 0 | PPTF Country |
| 15 | Backup1House | 0 | Backup1 Country |
| 16 | PPADHouse | 0 | PPAD Country |
| 17 | MSGuardHouse | 0 | MSGuard Country |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | PlantAA_Gone,0 |
| 1 | PlantAB_Gone,0 |
| 2 | PlantAC_Gone,0 |
| 3 | PlantAD_Gone,0 |
| 4 | Nuked_PPAA,0 |
| 5 | Player_Owns_AA,1 |
| 6 | Nuked_PPAB,0 |
| 7 | Engineer_AA,0 |
| 8 | TA_Team_Gone,0 |
| 9 | Nuked_MD,0 |
| 10 | Nuked_PPTA,0 |
| 11 | Backup1_Gone,0 |
| 12 | Nuked_MC,0 |
| 13 | Nuked_MA,0 |
| 14 | TB_Team_Gone,0 |
| 15 | TC_Team_Gone,0 |
| 16 | Nuked_MB,0 |
| 17 | TD_Team_Gone,0 |
| 18 | Nuked_PPAC,0 |
| 19 | Kill_GI,1 |
| 20 | Kill_GI_HF,0 |
| 21 | Kill_GI_HG,0 |
| 22 | Kill_GI_HH,0 |
| 23 | Kill_GI_HI,0 |
| 24 | Kill_GI_HJ,0 |
| 25 | Player_Owns_AB,1 |
| 26 | Player_Owns_AC,0 |
| 27 | Player_Owns_AD,1 |
| 28 | Player_Owns_TA,0 |
| 29 | Player_Owns_TB,0 |
| 30 | Player_Owns_TC,0 |
| 31 | Player_Owns_TD,0 |
| 32 | PlantTA_Gone,0 |
| 33 | PlantTB_Gone,0 |
| 34 | PlantTC_Gone,0 |
| 35 | PlantTD_Gone,0 |
| 36 | PlantA1_Gone,0 |
| 37 | PlantA2_Gone,0 |
| 38 | PlantTE_Gone,0 |
| 39 | PlantTF_Gone,0 |
| 40 | Player_Owns_TE,0 |
| 41 | Player_Owns_TF,0 |
| 42 | Nuked_PPAD,0 |
| 43 | PPTF_Gone,0 |
| 44 | French_Gone,0 |
| 45 | Nod_Gone,0 |
| 46 | Russia_Gone,0 |
| 47 | Arabs_Gone,0 |
| 48 | Confed_Gone,0 |
| 49 | GDI_Gone,0 |
| 50 | Nuked_PPTB,0 |
| 51 | Nuked_PPTC,0 |
| 52 | Nuked_PPTD,0 |
| 53 | Nuked_PPTE,0 |
| 54 | Nuked_PPTF,0 |
| 55 | Make_French_Hover,0 |
| 56 | Clear_French_Force,0 |
| 57 | Player_Power_Down,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [WeWin (0C61D87C)](#trigger-0c61d87c) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner. |
| [PlayerLose (0BE20ACC)](#trigger-0be20acc) | Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).<br>1 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |

## Every trigger, in file order

<a id="trigger-0affc4fc"></a>

### 1. Set_WC_Time - 0AFFC4FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AFF8E7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set Superweapon Charge; main setting 2; location/duration field 95.
2. Enable and reset applicable timers for [Player_Power_Back (0973308C)](#trigger-0973308c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13930, Events line 14308, Actions line 14686.

<a id="trigger-0973308c"></a>

### 2. Player_Power_Back - 0973308C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Set_WC_Time (0AFFC4FC)](#trigger-0affc4fc); enable from [Player_Power_Low (09704DDC)](#trigger-09704ddc).

Attached scope: tag definitions 0973520C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. At least 1 instances of Weather Controller (GAWEAT) exist on the map, under this event's ownership scope.
2. local flag 57 (Player_Power_Down) is set.
3. Power Full: owner selector 0 (country/type AMERICANS; placed owner Americans).

Flag writers in this mission: clear local flag 57 (Player_Power_Down) at [Player_Power_Back (0973308C)](#trigger-0973308c); set local flag 57 (Player_Power_Down) at [Player_Power_Low (09704DDC)](#trigger-09704ddc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_xA3_EvaWeatherOnline.
2. Clear local flag 57 (Player_Power_Down).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13931, Events line 14309, Actions line 14687.

<a id="trigger-0aff8d8c"></a>

### 3. Set_Nuke_Time - 0AFF8D8C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AFF8B5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set Superweapon Charge; main setting 0; location/duration field 70.
2. Preferred Target Cell Set; main setting 364; location/duration field NA.
3. Superweapon Set Recharge Time; main setting 0; location/duration field 4500.
4. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13932, Events line 14310, Actions line 14688.

<a id="trigger-0918703c"></a>

### 4. Camera_Start - 0918703C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0917A07C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 367 (cell 109, 123).
2. Disable player input.
3. Enable and reset applicable timers for [Nuke_Briefing (091603CC)](#trigger-091603cc).
4. Play voice notification EVA_EstablishBattlefieldControl.
5. Center Base Cell Set; main setting 389; location/duration field NZ.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13933, Events line 14311, Actions line 14689.

<a id="trigger-091603cc"></a>

### 5. Nuke_Briefing - 091603CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_Start (0918703C)](#trigger-0918703c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 365 (cell 49, 90) with speed setting 3.
2. Play in-game movie 11.
3. Enable and reset applicable timers for [Nuke_Briefing02 (08ED86CC)](#trigger-08ed86cc).
4. Set Superweapon Charge; main setting 2; location/duration field 85.
5. Disable [Nuke_Briefing (091603CC)](#trigger-091603cc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13934, Events line 14312, Actions line 14690.

<a id="trigger-08ed86cc"></a>

### 6. Nuke_Briefing02 - 08ED86CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_Briefing (091603CC)](#trigger-091603cc).

Incoming activation links: enable from [Nuke_Briefing (091603CC)](#trigger-091603cc).

Attached scope: tag definitions 09164D0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 18 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification A03_p01.
2. Enable and reset applicable timers for [WC_Briefing (09164A7C)](#trigger-09164a7c).
3. Disable [Nuke_Briefing02 (08ED86CC)](#trigger-08ed86cc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13935, Events line 14313, Actions line 14691.

<a id="trigger-09164a7c"></a>

### 7. WC_Briefing - 09164A7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Nuke_Briefing02 (08ED86CC)](#trigger-08ed86cc).

Attached scope: tag definitions 0916484C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 366 (cell 130, 136) with speed setting 3.
2. Perform no action.
3. Enable and reset applicable timers for [Needle_Briefing (091645BC)](#trigger-091645bc).
4. Disable [WC_Briefing (09164A7C)](#trigger-09164a7c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13936, Events line 14314, Actions line 14692.

<a id="trigger-091645bc"></a>

### 8. Needle_Briefing - 091645BC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WC_Briefing (09164A7C)](#trigger-09164a7c).

Attached scope: tag definitions 091644DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 19 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 367 (cell 109, 123) with speed setting 3.
2. Play voice notification Mis_xA3_EvaBriefing02.
3. Flash buildings of type CASEAT01; duration argument 90.
4. Enable and reset applicable timers for [MS_Briefing (0916417C)](#trigger-0916417c).
5. Enable and reset applicable timers for [MSGuard_Gone (0C7B443C)](#trigger-0c7b443c).
6. Disable [Needle_Briefing (091645BC)](#trigger-091645bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13937, Events line 14315, Actions line 14693.

<a id="trigger-0916417c"></a>

### 9. MS_Briefing - 0916417C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Needle_Briefing (091645BC)](#trigger-091645bc).

Attached scope: tag definitions 0916409C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 19 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 368 (cell 96, 92) with speed setting 3.
2. Play voice notification Mis_xA3_EvaBriefing01.
3. Flash buildings of type CASEAT02; duration argument 90.
4. Enable and reset applicable timers for [Return_to_Base (091654CC)](#trigger-091654cc).
5. Enable and reset applicable timers for [Player_Power_Low (09704DDC)](#trigger-09704ddc).
6. Disable [MS_Briefing (0916417C)](#trigger-0916417c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13938, Events line 14316, Actions line 14694.

<a id="trigger-0c7b443c"></a>

### 10. MSGuard_Gone - 0C7B443C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Needle_Briefing (091645BC)](#trigger-091645bc).

Attached scope: tag definitions 0C7B5E1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. At least 1 instances of MassiveSoft Campus (CASEAT02) exist on the map, under this event's ownership scope.
2. Destroyed,  All: owner selector 17 (country/type MSGUARD COUNTRY; placed owner MSGuardHouse).

**Then perform these actions in order:**

1. Play in-game movie 14.
2. Create crate type 0 at waypoint 312 (cell 98, 95).
3. Create crate type 0 at waypoint 313 (cell 99, 95).
4. Create crate type 0 at waypoint 314 (cell 100, 95).
5. Enable and reset applicable timers for [Secondary_Objective (0CDC3F3C)](#trigger-0cdc3f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13939, Events line 14317, Actions line 14695.

<a id="trigger-091654cc"></a>

### 11. Return_to_Base - 091654CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [MS_Briefing (0916417C)](#trigger-0916417c).

Attached scope: tag definitions 09163F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 18 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 364 (cell 126, 140) with speed setting 3.
2. Play voice notification EVA_BattlefieldControlOnline.
3. Superweapon Set Recharge Time; main setting 2; location/duration field 4500.
4. Enable and reset applicable timers for [Reshroud (0BF2B82C)](#trigger-0bf2b82c).
5. Enable and reset applicable timers for [Alliance_Reinforcements (06B87ACC)](#trigger-06b87acc).
6. Production Begins: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
7. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
8. Enable player input.
9. AI triggers begin: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
10. Disable [Return_to_Base (091654CC)](#trigger-091654cc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13940, Events line 14318, Actions line 14696.

<a id="trigger-09704ddc"></a>

### 12. Player_Power_Low - 09704DDC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [MS_Briefing (0916417C)](#trigger-0916417c).

Attached scope: tag definitions 0970489C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Low Power: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 57 (Player_Power_Down).
2. Enable and reset applicable timers for [Player_Power_Back (0973308C)](#trigger-0973308c).
3. Enable and reset applicable timers for [Power_Low_Warning (0F76680C)](#trigger-0f76680c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13941, Events line 14319, Actions line 14697.

<a id="trigger-0cdc3f3c"></a>

### 13. Secondary_Objective - 0CDC3F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [MSGuard_Gone (0C7B443C)](#trigger-0c7b443c).

Attached scope: tag definitions 0CDC3CAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_SecondaryObjectiveAchieved.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13942, Events line 14320, Actions line 14698.

<a id="trigger-0bf2b82c"></a>

### 14. Reshroud - 0BF2B82C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Return_to_Base (091654CC)](#trigger-091654cc).

Attached scope: tag definitions 0BF2B17C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reshroud Map; main setting 208; location/duration field HA.
2. Reveal terrain around waypoint 367 (cell 109, 123).
3. Reveal terrain around waypoint 368 (cell 96, 92).
4. Reveal terrain around waypoint 365 (cell 49, 90).
5. Reveal terrain around waypoint 32 (cell 120, 151).
6. Disable [Reshroud (0BF2B82C)](#trigger-0bf2b82c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13943, Events line 14321, Actions line 14699.

<a id="trigger-06b87acc"></a>

### 15. Alliance_Reinforcements - 06B87ACC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Return_to_Base (091654CC)](#trigger-091654cc).

Attached scope: tag definitions 06B8733C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 17.
2. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Alliance_Reinforce (08D650EC)](all03umd-teams.md#team-08d650ec).
2. Create radar-event marker type 12 at waypoint 53 (cell 135, 136).
3. Play voice notification EVA_ReinforcementsHaveArrived.
4. Enable and reset applicable timers for [Alliance_Reinforce2 (0460915C)](#trigger-0460915c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13944, Events line 14322, Actions line 14700.

<a id="trigger-0bf257bc"></a>

### 16. Yuri_Power_Low - 0BF257BC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Return_to_Base (091654CC)](#trigger-091654cc); enable from [PlantAA_Gone (093BEEDC)](#trigger-093beedc); enable from [Player_Takes_AA (0945ABBC)](#trigger-0945abbc); enable from [Yuri_Takes_AA (0945934C)](#trigger-0945934c); enable from [PlantAB_Gone (093BE2FC)](#trigger-093be2fc); enable from [Player_Takes_AB (0CF8179C)](#trigger-0cf8179c); enable from [Yuri_Takes_AB (0CF8110C)](#trigger-0cf8110c); enable from [PlantAC_Gone (093BFDDC)](#trigger-093bfddc); enable from [Player_Takes_AC (06B5EC6C)](#trigger-06b5ec6c); enable from [Yuri_Takes_AC (06B5D04C)](#trigger-06b5d04c); enable from [PlantAD_Gone (093BF8FC)](#trigger-093bf8fc); enable from [Player_Takes_AD (094D82BC)](#trigger-094d82bc); enable from [Yuri_Takes_AD (094D9C5C)](#trigger-094d9c5c); enable from [PlantTA_Gone (094E203C)](#trigger-094e203c); enable from [Player_Takes_TA (094E3ACC)](#trigger-094e3acc); enable from [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c); enable from [PlantTB_Gone (06B3ED3C)](#trigger-06b3ed3c); enable from [Player_Takes_TB (094D681C)](#trigger-094d681c); enable from [Yuri_Takes_TB (094D672C)](#trigger-094d672c); enable from [PlantTC_Gone (094F204C)](#trigger-094f204c); enable from [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec); enable from [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc); enable from [PlantTD_Gone (0B30790C)](#trigger-0b30790c); enable from [Player_Takes_TD (0B30121C)](#trigger-0b30121c); enable from [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c); enable from [PlantTE_Gone (045D673C)](#trigger-045d673c); enable from [Player_Takes_TE (045C109C)](#trigger-045c109c); enable from [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c); enable from [Player_Takes_TF (0C13364C)](#trigger-0c13364c); enable from [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c); enable from [PlantTF_Gone (09881BAC)](#trigger-09881bac).

Attached scope: tag definitions 0BF254AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Low Power: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Check_PPTF_True (0977807C)](#trigger-0977807c).
2. Enable and reset applicable timers for [Check_PPTF_False (0976132C)](#trigger-0976132c).
3. Disable [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13945, Events line 14323, Actions line 14701.

<a id="trigger-0f76680c"></a>

### 17. Power_Low_Warning - 0F76680C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Power_Low (09704DDC)](#trigger-09704ddc).

Attached scope: tag definitions 0F7642EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA3_EvaNeedPower.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13946, Events line 14324, Actions line 14702.

<a id="trigger-0460915c"></a>

### 18. Alliance_Reinforce2 - 0460915C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Alliance_Reinforcements (06B87ACC)](#trigger-06b87acc).

Attached scope: tag definitions 0460907C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 25.
2. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Alliance_Reinforce (08D650EC)](all03umd-teams.md#team-08d650ec).
2. Create radar-event marker type 12 at waypoint 0 (no location in this map's waypoint table).
3. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13947, Events line 14325, Actions line 14703.

<a id="trigger-0977807c"></a>

### 19. Check_PPTF_True - 0977807C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTE_False (0977816C)](#trigger-0977816c).

Incoming activation links: enable from [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 41 (Player_Owns_TF) is set.

Flag writers in this mission: set local flag 41 (Player_Owns_TF) at [Player_Takes_TF (0C13364C)](#trigger-0c13364c); clear local flag 41 (Player_Owns_TF) at [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c); clear local flag 41 (Player_Owns_TF) at [PlantTF_Gone (09881BAC)](#trigger-09881bac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTF_False (0976132C)](#trigger-0976132c).
2. Enable and reset applicable timers for [TF_Group_Alive_TF (097F10FC)](#trigger-097f10fc).
3. Enable and reset applicable timers for [TF_Group_Dead_TF (097F146C)](#trigger-097f146c).
4. Disable [Check_PPTF_True (0977807C)](#trigger-0977807c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13948, Events line 14326, Actions line 14704.

<a id="trigger-0976132c"></a>

### 20. Check_PPTF_False - 0976132C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTF_True (0977807C)](#trigger-0977807c).

Incoming activation links: enable from [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).

Attached scope: tag definitions 097AB10C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 41 (Player_Owns_TF) is clear.

Flag writers in this mission: set local flag 41 (Player_Owns_TF) at [Player_Takes_TF (0C13364C)](#trigger-0c13364c); clear local flag 41 (Player_Owns_TF) at [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c); clear local flag 41 (Player_Owns_TF) at [PlantTF_Gone (09881BAC)](#trigger-09881bac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTF_True (0977807C)](#trigger-0977807c).
2. Enable and reset applicable timers for [Check_PPTE_True (0977825C)](#trigger-0977825c).
3. Enable and reset applicable timers for [Check_PPTE_False (0977816C)](#trigger-0977816c).
4. Disable [Check_PPTF_False (0976132C)](#trigger-0976132c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13949, Events line 14327, Actions line 14705.

<a id="trigger-0977816c"></a>

### 21. Check_PPTE_False - 0977816C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTE_True (0977825C)](#trigger-0977825c).

Incoming activation links: enable from [Check_PPTF_False (0976132C)](#trigger-0976132c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 40 (Player_Owns_TE) is clear.

Flag writers in this mission: clear local flag 40 (Player_Owns_TE) at [PlantTE_Gone (045D673C)](#trigger-045d673c); set local flag 40 (Player_Owns_TE) at [Player_Takes_TE (045C109C)](#trigger-045c109c); clear local flag 40 (Player_Owns_TE) at [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTE_True (0977825C)](#trigger-0977825c).
2. Enable and reset applicable timers for [Check_PPTC_True (097AA17C)](#trigger-097aa17c).
3. Enable and reset applicable timers for [Check_PPTC_False (097AA08C)](#trigger-097aa08c).
4. Disable [Check_PPTE_False (0977816C)](#trigger-0977816c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13950, Events line 14328, Actions line 14706.

<a id="trigger-097f10fc"></a>

### 22. TF_Group_Alive_TF - 097F10FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Group_Dead_TF (097F146C)](#trigger-097f146c).

Incoming activation links: enable from [Check_PPTF_True (0977807C)](#trigger-0977807c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 43 (PPTF_Gone) is clear.

Flag writers in this mission: set local flag 43 (PPTF_Gone) at [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c); set local flag 43 (PPTF_Gone) at [Check_PPTF_Status (09761A8C)](#trigger-09761a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TF_Group_Dead_TF (097F146C)](#trigger-097f146c).
2. Enable and reset applicable timers for [Send_TF_Engineer (0BCB74FC)](#trigger-0bcb74fc).
3. Disable [TF_Group_Alive_TF (097F10FC)](#trigger-097f10fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13951, Events line 14329, Actions line 14707.

<a id="trigger-097f146c"></a>

### 23. TF_Group_Dead_TF - 097F146C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Check_PPTF_True (0977807C)](#trigger-0977807c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 43 (PPTF_Gone) is set.

Flag writers in this mission: set local flag 43 (PPTF_Gone) at [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c); set local flag 43 (PPTF_Gone) at [Check_PPTF_Status (09761A8C)](#trigger-09761a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TF_Group_Alive_TF (097F10FC)](#trigger-097f10fc).
2. Enable and reset applicable timers for [Backup1_Alive_TF (0985219C)](#trigger-0985219c).
3. Enable and reset applicable timers for [Backup1_Dead_TF (09856BDC)](#trigger-09856bdc).
4. Disable [TF_Group_Dead_TF (097F146C)](#trigger-097f146c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13952, Events line 14330, Actions line 14708.

<a id="trigger-0977825c"></a>

### 24. Check_PPTE_True - 0977825C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTD_False (097ABBDC)](#trigger-097abbdc).

Incoming activation links: enable from [Check_PPTF_False (0976132C)](#trigger-0976132c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 40 (Player_Owns_TE) is set.

Flag writers in this mission: clear local flag 40 (Player_Owns_TE) at [PlantTE_Gone (045D673C)](#trigger-045d673c); set local flag 40 (Player_Owns_TE) at [Player_Takes_TE (045C109C)](#trigger-045c109c); clear local flag 40 (Player_Owns_TE) at [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTE_False (0977816C)](#trigger-0977816c).
2. Enable and reset applicable timers for [Backup1_Alive_TE (0947703C)](#trigger-0947703c).
3. Enable and reset applicable timers for [Backup1_Dead_TE (0946F03C)](#trigger-0946f03c).
4. Disable [Check_PPTE_True (0977825C)](#trigger-0977825c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13953, Events line 14331, Actions line 14709.

<a id="trigger-097aa17c"></a>

### 25. Check_PPTC_True - 097AA17C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTB_False (097AA26C)](#trigger-097aa26c).

Incoming activation links: enable from [Check_PPTE_False (0977816C)](#trigger-0977816c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 30 (Player_Owns_TC) is set.

Flag writers in this mission: clear local flag 30 (Player_Owns_TC) at [PlantTC_Gone (094F204C)](#trigger-094f204c); set local flag 30 (Player_Owns_TC) at [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec); clear local flag 30 (Player_Owns_TC) at [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTC_False (097AA08C)](#trigger-097aa08c).
2. Enable and reset applicable timers for [Backup1_Alive_TC (0C0DCF3C)](#trigger-0c0dcf3c).
3. Enable and reset applicable timers for [Backup1_Dead_TC (0C0D8A8C)](#trigger-0c0d8a8c).
4. Disable [Check_PPTC_True (097AA17C)](#trigger-097aa17c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13954, Events line 14332, Actions line 14710.

<a id="trigger-097aa08c"></a>

### 26. Check_PPTC_False - 097AA08C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTC_True (097AA17C)](#trigger-097aa17c).

Incoming activation links: enable from [Check_PPTE_False (0977816C)](#trigger-0977816c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 30 (Player_Owns_TC) is clear.

Flag writers in this mission: clear local flag 30 (Player_Owns_TC) at [PlantTC_Gone (094F204C)](#trigger-094f204c); set local flag 30 (Player_Owns_TC) at [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec); clear local flag 30 (Player_Owns_TC) at [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTC_True (097AA17C)](#trigger-097aa17c).
2. Enable and reset applicable timers for [Check_PPTD_True (097ABCCC)](#trigger-097abccc).
3. Enable and reset applicable timers for [Check_PPTD_False (097ABBDC)](#trigger-097abbdc).
4. Disable [Check_PPTC_False (097AA08C)](#trigger-097aa08c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13955, Events line 14333, Actions line 14711.

<a id="trigger-0bcb74fc"></a>

### 27. Send_TF_Engineer - 0BCB74FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TF_Group_Alive_TF (097F10FC)](#trigger-097f10fc); enable from [Backup1_Alive_TF (0985219C)](#trigger-0985219c); enable from [TE_Group_Alive_TF (0960116C)](#trigger-0960116c); enable from [TC_Group_Alive_TF (0B43344C)](#trigger-0b43344c); enable from [TD_Group_Alive_TF (096DB61C)](#trigger-096db61c).

Attached scope: tag definitions 0BCB71EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TF_Engineer (0C85E1FC)](all03umd-teams.md#team-0c85e1fc).
2. Disable [Send_TF_Engineer (0BCB74FC)](#trigger-0bcb74fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13956, Events line 14334, Actions line 14712.

<a id="trigger-0985219c"></a>

### 28. Backup1_Alive_TF - 0985219C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Group_Alive_TF (097F10FC)](#trigger-097f10fc).

Incoming activation links: enable from [TF_Group_Dead_TF (097F146C)](#trigger-097f146c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 11 (Backup1_Gone) is clear.

Flag writers in this mission: set local flag 11 (Backup1_Gone) at [Check_Backup1_Stat (0DADB03C)](#trigger-0dadb03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Backup1_Dead_TF (09856BDC)](#trigger-09856bdc).
2. Enable and reset applicable timers for [Backup1_ChangeHouse (09565CCC)](#trigger-09565ccc).
3. Enable and reset applicable timers for [Send_TF_Engineer (0BCB74FC)](#trigger-0bcb74fc).
4. Disable [Backup1_Alive_TF (0985219C)](#trigger-0985219c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13957, Events line 14335, Actions line 14713.

<a id="trigger-09856bdc"></a>

### 29. Backup1_Dead_TF - 09856BDC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Alive_TF (0985219C)](#trigger-0985219c).

Incoming activation links: enable from [TF_Group_Dead_TF (097F146C)](#trigger-097f146c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 11 (Backup1_Gone) is set.

Flag writers in this mission: set local flag 11 (Backup1_Gone) at [Check_Backup1_Stat (0DADB03C)](#trigger-0dadb03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Backup1_Alive_TF (0985219C)](#trigger-0985219c).
2. Enable and reset applicable timers for [TE_Group_Alive_TF (0960116C)](#trigger-0960116c).
3. Enable and reset applicable timers for [TE_Group_Dead_TF (09606A4C)](#trigger-09606a4c).
4. Disable [Backup1_Dead_TF (09856BDC)](#trigger-09856bdc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13958, Events line 14336, Actions line 14714.

<a id="trigger-097abbdc"></a>

### 30. Check_PPTD_False - 097ABBDC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTD_True (097ABCCC)](#trigger-097abccc).

Incoming activation links: enable from [Check_PPTC_False (097AA08C)](#trigger-097aa08c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 31 (Player_Owns_TD) is clear.

Flag writers in this mission: clear local flag 31 (Player_Owns_TD) at [PlantTD_Gone (0B30790C)](#trigger-0b30790c); set local flag 31 (Player_Owns_TD) at [Player_Takes_TD (0B30121C)](#trigger-0b30121c); clear local flag 31 (Player_Owns_TD) at [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTD_True (097ABCCC)](#trigger-097abccc).
2. Enable and reset applicable timers for [Check_PPTB_True (097AA35C)](#trigger-097aa35c).
3. Enable and reset applicable timers for [Check_PPTB_False (097AA26C)](#trigger-097aa26c).
4. Disable [Check_PPTD_False (097ABBDC)](#trigger-097abbdc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13959, Events line 14337, Actions line 14715.

<a id="trigger-0947703c"></a>

### 31. Backup1_Alive_TE - 0947703C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Dead_TE (0946F03C)](#trigger-0946f03c).

Incoming activation links: enable from [Check_PPTE_True (0977825C)](#trigger-0977825c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Backup1_Dead_TE (0946F03C)](#trigger-0946f03c).
2. Enable and reset applicable timers for [Backup1_TE_Change (096D196C)](#trigger-096d196c).
3. Enable and reset applicable timers for [Send_TE_Engineer (0BCB659C)](#trigger-0bcb659c).
4. Disable [Backup1_Alive_TE (0947703C)](#trigger-0947703c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13960, Events line 14338, Actions line 14716.

<a id="trigger-0946f03c"></a>

### 32. Backup1_Dead_TE - 0946F03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Check_PPTE_True (0977825C)](#trigger-0977825c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 11 (Backup1_Gone) is set.

Flag writers in this mission: set local flag 11 (Backup1_Gone) at [Check_Backup1_Stat (0DADB03C)](#trigger-0dadb03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Backup1_Alive_TE (0947703C)](#trigger-0947703c).
2. Enable and reset applicable timers for [TF_Group_Alive_TE (0947203C)](#trigger-0947203c).
3. Enable and reset applicable timers for [TF_Group_Dead_TE (0947003C)](#trigger-0947003c).
4. Disable [Backup1_Dead_TE (0946F03C)](#trigger-0946f03c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13961, Events line 14339, Actions line 14717.

<a id="trigger-097aa26c"></a>

### 33. Check_PPTB_False - 097AA26C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTB_True (097AA35C)](#trigger-097aa35c).

Incoming activation links: enable from [Check_PPTD_False (097ABBDC)](#trigger-097abbdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 29 (Player_Owns_TB) is clear.

Flag writers in this mission: clear local flag 29 (Player_Owns_TB) at [PlantTB_Gone (06B3ED3C)](#trigger-06b3ed3c); set local flag 29 (Player_Owns_TB) at [Player_Takes_TB (094D681C)](#trigger-094d681c); clear local flag 29 (Player_Owns_TB) at [Yuri_Takes_TB (094D672C)](#trigger-094d672c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTB_True (097AA35C)](#trigger-097aa35c).
2. Enable and reset applicable timers for [Check_PPTA_True (097AB2DC)](#trigger-097ab2dc).
3. Enable and reset applicable timers for [Check_PPTA_False (097A821C)](#trigger-097a821c).
4. Disable [Check_PPTB_False (097AA26C)](#trigger-097aa26c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13962, Events line 14340, Actions line 14718.

<a id="trigger-0c0dcf3c"></a>

### 34. Backup1_Alive_TC - 0C0DCF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Check_PPTC_True (097AA17C)](#trigger-097aa17c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 11 (Backup1_Gone) is clear.

Flag writers in this mission: set local flag 11 (Backup1_Gone) at [Check_Backup1_Stat (0DADB03C)](#trigger-0dadb03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Backup1_Dead_TC (0C0D8A8C)](#trigger-0c0d8a8c).
2. Enable and reset applicable timers for [Backup1_TC_Change (06C80D0C)](#trigger-06c80d0c).
3. Enable and reset applicable timers for [Send_TC_Engineer (0BC4E24C)](#trigger-0bc4e24c).
4. Disable [Backup1_Alive_TC (0C0DCF3C)](#trigger-0c0dcf3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13963, Events line 14341, Actions line 14719.

<a id="trigger-0c0d8a8c"></a>

### 35. Backup1_Dead_TC - 0C0D8A8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Alive_TC (0C0DCF3C)](#trigger-0c0dcf3c).

Incoming activation links: enable from [Check_PPTC_True (097AA17C)](#trigger-097aa17c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 11 (Backup1_Gone) is set.

Flag writers in this mission: set local flag 11 (Backup1_Gone) at [Check_Backup1_Stat (0DADB03C)](#trigger-0dadb03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Backup1_Alive_TC (0C0DCF3C)](#trigger-0c0dcf3c).
2. Enable and reset applicable timers for [TF_Group_Alive_TC (0C0D899C)](#trigger-0c0d899c).
3. Enable and reset applicable timers for [TF_Group_Dead_TC (0C0D84FC)](#trigger-0c0d84fc).
4. Disable [Backup1_Dead_TC (0C0D8A8C)](#trigger-0c0d8a8c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13964, Events line 14342, Actions line 14720.

<a id="trigger-097abccc"></a>

### 36. Check_PPTD_True - 097ABCCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTC_False (097AA08C)](#trigger-097aa08c).

Incoming activation links: enable from [Check_PPTC_False (097AA08C)](#trigger-097aa08c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 31 (Player_Owns_TD) is set.

Flag writers in this mission: clear local flag 31 (Player_Owns_TD) at [PlantTD_Gone (0B30790C)](#trigger-0b30790c); set local flag 31 (Player_Owns_TD) at [Player_Takes_TD (0B30121C)](#trigger-0b30121c); clear local flag 31 (Player_Owns_TD) at [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTD_False (097ABBDC)](#trigger-097abbdc).
2. Enable and reset applicable timers for [Backup1_Alive_TD (096E4F3C)](#trigger-096e4f3c).
3. Enable and reset applicable timers for [Backup1_Dead_TD (0C13403C)](#trigger-0c13403c).
4. Disable [Check_PPTD_True (097ABCCC)](#trigger-097abccc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13965, Events line 14343, Actions line 14721.

<a id="trigger-09565ccc"></a>

### 37. Backup1_ChangeHouse - 09565CCC

Owner reference: Backup1 Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Backup1_Alive_TF (0985219C)](#trigger-0985219c); enable from [TF_Becomes_TC2 (0975C66C)](#trigger-0975c66c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 11 (Backup1_Gone) is clear.
2. 0 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 11 (Backup1_Gone) at [Check_Backup1_Stat (0DADB03C)](#trigger-0dadb03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 14 (country/type PPTF COUNTRY; placed owner PPTFHouse).
2. Enable and reset applicable timers for [Backup1_Becomes_TF1 (095656BC)](#trigger-095656bc).
3. Disable [Backup1_ChangeHouse (09565CCC)](#trigger-09565ccc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13966, Events line 14344, Actions line 14722.

<a id="trigger-0960116c"></a>

### 38. TE_Group_Alive_TF - 0960116C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Dead_TF (09856BDC)](#trigger-09856bdc).

Incoming activation links: enable from [Backup1_Dead_TF (09856BDC)](#trigger-09856bdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 49 (GDI_Gone) is clear.

Flag writers in this mission: set local flag 49 (GDI_Gone) at [Check_GDI_Status (097C766C)](#trigger-097c766c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TE_Group_Dead_TF (09606A4C)](#trigger-09606a4c).
2. Enable and reset applicable timers for [TE_TF_ChangeHouse (097A178C)](#trigger-097a178c).
3. Enable and reset applicable timers for [Send_TF_Engineer (0BCB74FC)](#trigger-0bcb74fc).
4. Disable [TE_Group_Alive_TF (0960116C)](#trigger-0960116c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13967, Events line 14345, Actions line 14723.

<a id="trigger-09606a4c"></a>

### 39. TE_Group_Dead_TF - 09606A4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_Group_Alive_TF (0960116C)](#trigger-0960116c).

Incoming activation links: enable from [Backup1_Dead_TF (09856BDC)](#trigger-09856bdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 49 (GDI_Gone) is set.

Flag writers in this mission: set local flag 49 (GDI_Gone) at [Check_GDI_Status (097C766C)](#trigger-097c766c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TE_Group_Alive_TF (0960116C)](#trigger-0960116c).
2. Enable and reset applicable timers for [TC_Group_Alive_TF (0B43344C)](#trigger-0b43344c).
3. Enable and reset applicable timers for [TC_Group_Dead_TF (0B43335C)](#trigger-0b43335c).
4. Disable [TE_Group_Dead_TF (09606A4C)](#trigger-09606a4c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13968, Events line 14346, Actions line 14724.

<a id="trigger-097aa35c"></a>

### 40. Check_PPTB_True - 097AA35C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTA_False (097A821C)](#trigger-097a821c).

Incoming activation links: enable from [Check_PPTD_False (097ABBDC)](#trigger-097abbdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 29 (Player_Owns_TB) is set.

Flag writers in this mission: clear local flag 29 (Player_Owns_TB) at [PlantTB_Gone (06B3ED3C)](#trigger-06b3ed3c); set local flag 29 (Player_Owns_TB) at [Player_Takes_TB (094D681C)](#trigger-094d681c); clear local flag 29 (Player_Owns_TB) at [Yuri_Takes_TB (094D672C)](#trigger-094d672c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTB_False (097AA26C)](#trigger-097aa26c).
2. Enable and reset applicable timers for [TA_Group_Alive_TB (0970D15C)](#trigger-0970d15c).
3. Enable and reset applicable timers for [TA_Group_Dead_TB (0970D06C)](#trigger-0970d06c).
4. Disable [Check_PPTB_True (097AA35C)](#trigger-097aa35c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13969, Events line 14347, Actions line 14725.

<a id="trigger-096d196c"></a>

### 41. Backup1_TE_Change - 096D196C

Owner reference: Backup1 Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Backup1_Alive_TE (0947703C)](#trigger-0947703c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 10 (country/type GDI; placed owner GDI).
2. Enable and reset applicable timers for [Backup1_Becomes_TE_1 (096D15BC)](#trigger-096d15bc).
3. Disable [Backup1_TE_Change (096D196C)](#trigger-096d196c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13970, Events line 14348, Actions line 14726.

<a id="trigger-0bcb659c"></a>

### 42. Send_TE_Engineer - 0BCB659C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Backup1_Alive_TE (0947703C)](#trigger-0947703c); enable from [TF_Group_Alive_TE (0947203C)](#trigger-0947203c); enable from [TC_Group_Alive_TE (096E07EC)](#trigger-096e07ec); enable from [TD_Group_Alive_TE (06C7812C)](#trigger-06c7812c).

Attached scope: tag definitions 0BCB5E4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TE_Engineer (0C94F90C)](all03umd-teams.md#team-0c94f90c).
2. Disable [Send_TE_Engineer (0BCB659C)](#trigger-0bcb659c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13971, Events line 14349, Actions line 14727.

<a id="trigger-0947203c"></a>

### 43. TF_Group_Alive_TE - 0947203C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Alive_TE (0947703C)](#trigger-0947703c).

Incoming activation links: enable from [Backup1_Dead_TE (0946F03C)](#trigger-0946f03c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 43 (PPTF_Gone) is clear.

Flag writers in this mission: set local flag 43 (PPTF_Gone) at [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c); set local flag 43 (PPTF_Gone) at [Check_PPTF_Status (09761A8C)](#trigger-09761a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TF_Group_Dead_TE (0947003C)](#trigger-0947003c).
2. Enable and reset applicable timers for [TF_TE_ChangeHouse (096E6E5C)](#trigger-096e6e5c).
3. Enable and reset applicable timers for [Send_TE_Engineer (0BCB659C)](#trigger-0bcb659c).
4. Disable [TF_Group_Alive_TE (0947203C)](#trigger-0947203c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13972, Events line 14350, Actions line 14728.

<a id="trigger-0947003c"></a>

### 44. TF_Group_Dead_TE - 0947003C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Group_Alive_TE (0947203C)](#trigger-0947203c).

Incoming activation links: enable from [Backup1_Dead_TE (0946F03C)](#trigger-0946f03c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 43 (PPTF_Gone) is set.

Flag writers in this mission: set local flag 43 (PPTF_Gone) at [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c); set local flag 43 (PPTF_Gone) at [Check_PPTF_Status (09761A8C)](#trigger-09761a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TF_Group_Alive_TE (0947203C)](#trigger-0947203c).
2. Enable and reset applicable timers for [TC_Group_Alive_TE (096E07EC)](#trigger-096e07ec).
3. Enable and reset applicable timers for [TC_Group_Dead_TE (096E06FC)](#trigger-096e06fc).
4. Disable [TF_Group_Dead_TE (0947003C)](#trigger-0947003c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13973, Events line 14351, Actions line 14729.

<a id="trigger-097ab2dc"></a>

### 45. Check_PPTA_True - 097AB2DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Check_PPTB_False (097AA26C)](#trigger-097aa26c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 28 (Player_Owns_TA) is set.

Flag writers in this mission: clear local flag 28 (Player_Owns_TA) at [PlantTA_Gone (094E203C)](#trigger-094e203c); set local flag 28 (Player_Owns_TA) at [Player_Takes_TA (094E3ACC)](#trigger-094e3acc); clear local flag 28 (Player_Owns_TA) at [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTA_False (097A821C)](#trigger-097a821c).
2. Enable and reset applicable timers for [French_Alive_TA (098CC24C)](#trigger-098cc24c).
3. Enable and reset applicable timers for [French_Dead_TA (098CC15C)](#trigger-098cc15c).
4. Disable [Check_PPTA_True (097AB2DC)](#trigger-097ab2dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13974, Events line 14352, Actions line 14730.

<a id="trigger-097a821c"></a>

### 46. Check_PPTA_False - 097A821C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PPTA_True (097AB2DC)](#trigger-097ab2dc).

Incoming activation links: enable from [Check_PPTB_False (097AA26C)](#trigger-097aa26c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 28 (Player_Owns_TA) is clear.

Flag writers in this mission: clear local flag 28 (Player_Owns_TA) at [PlantTA_Gone (094E203C)](#trigger-094e203c); set local flag 28 (Player_Owns_TA) at [Player_Takes_TA (094E3ACC)](#trigger-094e3acc); clear local flag 28 (Player_Owns_TA) at [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PPTA_True (097AB2DC)](#trigger-097ab2dc).
2. Disable [Check_PPTA_False (097A821C)](#trigger-097a821c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13975, Events line 14353, Actions line 14731.

<a id="trigger-06c80d0c"></a>

### 47. Backup1_TC_Change - 06C80D0C

Owner reference: Backup1 Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Backup1_Alive_TC (0C0DCF3C)](#trigger-0c0dcf3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. Enable and reset applicable timers for [Backup1_Becomes_TC_1 (0975588C)](#trigger-0975588c).
3. Disable [Backup1_TC_Change (06C80D0C)](#trigger-06c80d0c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13976, Events line 14354, Actions line 14732.

<a id="trigger-0bc4e24c"></a>

### 48. Send_TC_Engineer - 0BC4E24C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Backup1_Alive_TC (0C0DCF3C)](#trigger-0c0dcf3c); enable from [TF_Group_Alive_TC (0C0D899C)](#trigger-0c0d899c); enable from [TE_Group_Alive_TC (0C0D840C)](#trigger-0c0d840c); enable from [TD_Group_Alive_TC (0C0D822C)](#trigger-0c0d822c).

Attached scope: tag definitions 0BC4DBFC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TC_Engineer (0C94E2DC)](all03umd-teams.md#team-0c94e2dc).
2. Disable [Send_TC_Engineer (0BC4E24C)](#trigger-0bc4e24c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13977, Events line 14355, Actions line 14733.

<a id="trigger-0c0d899c"></a>

### 49. TF_Group_Alive_TC - 0C0D899C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Dead_TC (0C0D8A8C)](#trigger-0c0d8a8c).

Incoming activation links: enable from [Backup1_Dead_TC (0C0D8A8C)](#trigger-0c0d8a8c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 43 (PPTF_Gone) is clear.

Flag writers in this mission: set local flag 43 (PPTF_Gone) at [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c); set local flag 43 (PPTF_Gone) at [Check_PPTF_Status (09761A8C)](#trigger-09761a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TF_Group_Dead_TC (0C0D84FC)](#trigger-0c0d84fc).
2. Enable and reset applicable timers for [TF_Change_House (0975ABAC)](#trigger-0975abac).
3. Enable and reset applicable timers for [Send_TC_Engineer (0BC4E24C)](#trigger-0bc4e24c).
4. Disable [TF_Group_Alive_TC (0C0D899C)](#trigger-0c0d899c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13978, Events line 14356, Actions line 14734.

<a id="trigger-0c0d84fc"></a>

### 50. TF_Group_Dead_TC - 0C0D84FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Group_Alive_TC (0C0D899C)](#trigger-0c0d899c).

Incoming activation links: enable from [Backup1_Dead_TC (0C0D8A8C)](#trigger-0c0d8a8c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 43 (PPTF_Gone) is set.

Flag writers in this mission: set local flag 43 (PPTF_Gone) at [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c); set local flag 43 (PPTF_Gone) at [Check_PPTF_Status (09761A8C)](#trigger-09761a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TF_Group_Alive_TC (0C0D899C)](#trigger-0c0d899c).
2. Enable and reset applicable timers for [TE_Group_Alive_TC (0C0D840C)](#trigger-0c0d840c).
3. Enable and reset applicable timers for [TE_Group_Dead_TC (0C0D831C)](#trigger-0c0d831c).
4. Disable [TF_Group_Dead_TC (0C0D84FC)](#trigger-0c0d84fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13979, Events line 14357, Actions line 14735.

<a id="trigger-096e4f3c"></a>

### 51. Backup1_Alive_TD - 096E4F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Check_PPTD_True (097ABCCC)](#trigger-097abccc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 11 (Backup1_Gone) is clear.

Flag writers in this mission: set local flag 11 (Backup1_Gone) at [Check_Backup1_Stat (0DADB03C)](#trigger-0dadb03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Backup1_Dead_TD (0C13403C)](#trigger-0c13403c).
2. Enable and reset applicable timers for [Backup1_TD_Change (0C10304C)](#trigger-0c10304c).
3. Enable and reset applicable timers for [Send_TD_Engineer (0BC6A69C)](#trigger-0bc6a69c).
4. Disable [Backup1_Alive_TD (096E4F3C)](#trigger-096e4f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13980, Events line 14358, Actions line 14736.

<a id="trigger-0c13403c"></a>

### 52. Backup1_Dead_TD - 0C13403C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Alive_TD (096E4F3C)](#trigger-096e4f3c).

Incoming activation links: enable from [Check_PPTD_True (097ABCCC)](#trigger-097abccc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 11 (Backup1_Gone) is set.

Flag writers in this mission: set local flag 11 (Backup1_Gone) at [Check_Backup1_Stat (0DADB03C)](#trigger-0dadb03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Backup1_Alive_TD (096E4F3C)](#trigger-096e4f3c).
2. Enable and reset applicable timers for [TF_Group_Alive_TD (0C4F7B6C)](#trigger-0c4f7b6c).
3. Enable and reset applicable timers for [TF_Group_Dead_TD (0C4F70CC)](#trigger-0c4f70cc).
4. Disable [Backup1_Dead_TD (0C13403C)](#trigger-0c13403c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13981, Events line 14359, Actions line 14737.

<a id="trigger-095656bc"></a>

### 53. Backup1_Becomes_TF1 - 095656BC

Owner reference: PPTF Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_ChangeHouse (09565CCC)](#trigger-09565ccc).

Incoming activation links: enable from [Backup1_ChangeHouse (09565CCC)](#trigger-09565ccc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Gatt1 (095B536C)](all03umd-teams.md#team-095b536c).
2. Create/recruit team [TEAM_TF_Gatt2 (095B6D7C)](all03umd-teams.md#team-095b6d7c).
3. Create/recruit team [TEAM_TF_Init1 (095B68CC)](all03umd-teams.md#team-095b68cc).
4. Create/recruit team [TEAM_TF_Init2 (095B606C)](all03umd-teams.md#team-095b606c).
5. Create/recruit team [TEAM_TF_Init3 (095B7C0C)](all03umd-teams.md#team-095b7c0c).
6. Create/recruit team [TEAM_TF_Init4 (095B782C)](all03umd-teams.md#team-095b782c).
7. Create/recruit team [TEAM_TF_Lasher1 (095B740C)](all03umd-teams.md#team-095b740c).
8. Create/recruit team [TEAM_TF_Lasher2 (0BA5FC1C)](all03umd-teams.md#team-0ba5fc1c).
9. Enable and reset applicable timers for [Backup1_Becomes_TF2 (09566E6C)](#trigger-09566e6c).
10. Disable [Backup1_Becomes_TF1 (095656BC)](#trigger-095656bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13982, Events line 14360, Actions line 14738.

<a id="trigger-097a178c"></a>

### 54. TE_TF_ChangeHouse - 097A178C

Owner reference: GDI. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TE_Group_Alive_TF (0960116C)](#trigger-0960116c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 14 (country/type PPTF COUNTRY; placed owner PPTFHouse).
2. Enable and reset applicable timers for [TE_TF_DestroyTeam1 (097A4E2C)](#trigger-097a4e2c).
3. Disable [TE_TF_ChangeHouse (097A178C)](#trigger-097a178c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13983, Events line 14361, Actions line 14739.

<a id="trigger-0b43344c"></a>

### 55. TC_Group_Alive_TF - 0B43344C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_Group_Dead_TF (09606A4C)](#trigger-09606a4c).

Incoming activation links: enable from [TE_Group_Dead_TF (09606A4C)](#trigger-09606a4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 48 (Confed_Gone) is clear.

Flag writers in this mission: set local flag 48 (Confed_Gone) at [Check_Confed_Status (097E4A8C)](#trigger-097e4a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TC_Group_Dead_TF (0B43335C)](#trigger-0b43335c).
2. Enable and reset applicable timers for [TC_TF_ChangeHouse (0BD4750C)](#trigger-0bd4750c).
3. Enable and reset applicable timers for [Send_TF_Engineer (0BCB74FC)](#trigger-0bcb74fc).
4. Disable [TC_Group_Alive_TF (0B43344C)](#trigger-0b43344c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13984, Events line 14362, Actions line 14740.

<a id="trigger-0b43335c"></a>

### 56. TC_Group_Dead_TF - 0B43335C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_Group_Alive_TF (0B43344C)](#trigger-0b43344c).

Incoming activation links: enable from [TE_Group_Dead_TF (09606A4C)](#trigger-09606a4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 48 (Confed_Gone) is set.

Flag writers in this mission: set local flag 48 (Confed_Gone) at [Check_Confed_Status (097E4A8C)](#trigger-097e4a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TC_Group_Alive_TF (0B43344C)](#trigger-0b43344c).
2. Enable and reset applicable timers for [TD_Group_Alive_TF (096DB61C)](#trigger-096db61c).
3. Enable and reset applicable timers for [TD_Group_Dead_TF (096D9F3C)](#trigger-096d9f3c).
4. Disable [TC_Group_Dead_TF (0B43335C)](#trigger-0b43335c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13985, Events line 14363, Actions line 14741.

<a id="trigger-0970d15c"></a>

### 57. TA_Group_Alive_TB - 0970D15C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [French_Dead_TB (0970D39C)](#trigger-0970d39c).

Incoming activation links: enable from [Check_PPTB_True (097AA35C)](#trigger-097aa35c); enable from [French_Dead_TB (0970D39C)](#trigger-0970d39c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 46 (Russia_Gone) is clear.

Flag writers in this mission: set local flag 46 (Russia_Gone) at [Check_Russia_Status (0961FB5C)](#trigger-0961fb5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TA_Group_Dead_TB (0970D06C)](#trigger-0970d06c).
2. Enable and reset applicable timers for [TA_TB_ChangeHouse (0C53A03C)](#trigger-0c53a03c).
3. Enable and reset applicable timers for [Send_TB_Engineer (0BC4F34C)](#trigger-0bc4f34c).
4. Disable [TA_Group_Alive_TB (0970D15C)](#trigger-0970d15c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13986, Events line 14364, Actions line 14742.

<a id="trigger-0970d06c"></a>

### 58. TA_Group_Dead_TB - 0970D06C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TA_Group_Alive_TB (0970D15C)](#trigger-0970d15c).

Incoming activation links: enable from [Check_PPTB_True (097AA35C)](#trigger-097aa35c); enable from [French_Dead_TB (0970D39C)](#trigger-0970d39c).

Attached scope: tag definitions 0970D48C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 46 (Russia_Gone) is set.

Flag writers in this mission: set local flag 46 (Russia_Gone) at [Check_Russia_Status (0961FB5C)](#trigger-0961fb5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TA_Group_Alive_TB (0970D15C)](#trigger-0970d15c).
2. Disable [TA_Group_Dead_TB (0970D06C)](#trigger-0970d06c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13987, Events line 14365, Actions line 14743.

<a id="trigger-096d15bc"></a>

### 59. Backup1_Becomes_TE_1 - 096D15BC

Owner reference: GDI. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_TE_Change (096D196C)](#trigger-096d196c).

Incoming activation links: enable from [Backup1_TE_Change (096D196C)](#trigger-096d196c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TE_Gatt1 (0C0B821C)](all03umd-teams.md#team-0c0b821c).
2. Create/recruit team [TEAM_TE_Gatt2 (09502E2C)](all03umd-teams.md#team-09502e2c).
3. Create/recruit team [TEAM_TE_Init1 (0950297C)](all03umd-teams.md#team-0950297c).
4. Create/recruit team [TEAM_TE_Init2 (0950251C)](all03umd-teams.md#team-0950251c).
5. Create/recruit team [TEAM_TE_Init3 (095020BC)](all03umd-teams.md#team-095020bc).
6. Create/recruit team [TEAM_TE_Init4 (0950D50C)](all03umd-teams.md#team-0950d50c).
7. Create/recruit team [TEAM_TE_Lasher1 (0950D16C)](all03umd-teams.md#team-0950d16c).
8. Create/recruit team [TEAM_TE_Lasher2 (0950D03C)](all03umd-teams.md#team-0950d03c).
9. Enable and reset applicable timers for [Backup1_Becomes_TE_2 (096D14CC)](#trigger-096d14cc).
10. Disable [Backup1_Becomes_TE_1 (096D15BC)](#trigger-096d15bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13988, Events line 14366, Actions line 14744.

<a id="trigger-096e6e5c"></a>

### 60. TF_TE_ChangeHouse - 096E6E5C

Owner reference: PPTF Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TF_Group_Alive_TE (0947203C)](#trigger-0947203c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 10 (country/type GDI; placed owner GDI).
2. Enable and reset applicable timers for [TF_TE_DestroyTeam1 (096E6C8C)](#trigger-096e6c8c).
3. Disable [TF_TE_ChangeHouse (096E6E5C)](#trigger-096e6e5c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13989, Events line 14367, Actions line 14745.

<a id="trigger-096e07ec"></a>

### 61. TC_Group_Alive_TE - 096E07EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Group_Dead_TE (0947003C)](#trigger-0947003c).

Incoming activation links: enable from [TF_Group_Dead_TE (0947003C)](#trigger-0947003c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [TC_Group_Dead_TE (096E06FC)](#trigger-096e06fc).
2. Enable and reset applicable timers for [TC_TE_ChangeHouse (0C0DE0DC)](#trigger-0c0de0dc).
3. Enable and reset applicable timers for [Send_TE_Engineer (0BCB659C)](#trigger-0bcb659c).
4. Disable [TC_Group_Alive_TE (096E07EC)](#trigger-096e07ec).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13990, Events line 14368, Actions line 14746.

<a id="trigger-096e06fc"></a>

### 62. TC_Group_Dead_TE - 096E06FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_Group_Alive_TE (096E07EC)](#trigger-096e07ec).

Incoming activation links: enable from [TF_Group_Dead_TE (0947003C)](#trigger-0947003c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 48 (Confed_Gone) is set.

Flag writers in this mission: set local flag 48 (Confed_Gone) at [Check_Confed_Status (097E4A8C)](#trigger-097e4a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TC_Group_Alive_TE (096E07EC)](#trigger-096e07ec).
2. Enable and reset applicable timers for [TD_Group_Alive_TE (06C7812C)](#trigger-06c7812c).
3. Enable and reset applicable timers for [TD_Group_Dead_TE (06C7803C)](#trigger-06c7803c).
4. Disable [TC_Group_Dead_TE (096E06FC)](#trigger-096e06fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13991, Events line 14369, Actions line 14747.

<a id="trigger-098cc24c"></a>

### 63. French_Alive_TA - 098CC24C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_Group_Dead_TA (098C9A8C)](#trigger-098c9a8c).

Incoming activation links: enable from [Check_PPTA_True (097AB2DC)](#trigger-097ab2dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 44 (French_Gone) is clear.

Flag writers in this mission: set local flag 44 (French_Gone) at [Check_French_Status (096C58BC)](#trigger-096c58bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [French_Dead_TA (098CC15C)](#trigger-098cc15c).
2. Enable and reset applicable timers for [French_TA_Change (0B58A03C)](#trigger-0b58a03c).
3. Enable and reset applicable timers for [Send_TA_Engineer (096F185C)](#trigger-096f185c).
4. Disable [French_Alive_TA (098CC24C)](#trigger-098cc24c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13992, Events line 14370, Actions line 14748.

<a id="trigger-098cc15c"></a>

### 64. French_Dead_TA - 098CC15C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [French_Alive_TA (098CC24C)](#trigger-098cc24c).

Incoming activation links: enable from [Check_PPTA_True (097AB2DC)](#trigger-097ab2dc).

Attached scope: tag definitions 097A804C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 44 (French_Gone) is set.

Flag writers in this mission: set local flag 44 (French_Gone) at [Check_French_Status (096C58BC)](#trigger-096c58bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [French_Alive_TA (098CC24C)](#trigger-098cc24c).
2. Enable and reset applicable timers for [TB_Group_Alive_TA (098C9B7C)](#trigger-098c9b7c).
3. Enable and reset applicable timers for [TB_Group_Dead_TA (098C9A8C)](#trigger-098c9a8c).
4. Disable [French_Dead_TA (098CC15C)](#trigger-098cc15c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13993, Events line 14371, Actions line 14749.

<a id="trigger-0975588c"></a>

### 65. Backup1_Becomes_TC_1 - 0975588C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_TC_Change (06C80D0C)](#trigger-06c80d0c).

Incoming activation links: enable from [Backup1_TC_Change (06C80D0C)](#trigger-06c80d0c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Gatt1 (0967471C)](all03umd-teams.md#team-0967471c).
2. Create/recruit team [TEAM_TC_Gatt2 (09675EFC)](all03umd-teams.md#team-09675efc).
3. Create/recruit team [TEAM_TC_Init1 (09675B1C)](all03umd-teams.md#team-09675b1c).
4. Create/recruit team [TEAM_TC_Init2 (096756FC)](all03umd-teams.md#team-096756fc).
5. Create/recruit team [TEAM_TC_Init3 (0BE0D2BC)](all03umd-teams.md#team-0be0d2bc).
6. Create/recruit team [TEAM_TC_Init4 (06C6FEFC)](all03umd-teams.md#team-06c6fefc).
7. Create/recruit team [TEAM_TC_Lasher1 (06C6F82C)](all03umd-teams.md#team-06c6f82c).
8. Create/recruit team [TEAM_TC_Lasher2 (06C6F21C)](all03umd-teams.md#team-06c6f21c).
9. Enable and reset applicable timers for [Backup1_Becomes_TC_2 (0975579C)](#trigger-0975579c).
10. Disable [Backup1_Becomes_TC_1 (0975588C)](#trigger-0975588c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13994, Events line 14372, Actions line 14750.

<a id="trigger-0975abac"></a>

### 66. TF_Change_House - 0975ABAC

Owner reference: PPTF Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TF_Group_Alive_TC (0C0D899C)](#trigger-0c0d899c); enable from [TC_Becomes_TD2 (095FDF3C)](#trigger-095fdf3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. Enable and reset applicable timers for [TF_ChangeGuard1 (0975A12C)](#trigger-0975a12c).
3. Disable [TF_Change_House (0975ABAC)](#trigger-0975abac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13995, Events line 14373, Actions line 14751.

<a id="trigger-0c0d840c"></a>

### 67. TE_Group_Alive_TC - 0C0D840C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Group_Dead_TC (0C0D84FC)](#trigger-0c0d84fc).

Incoming activation links: enable from [TF_Group_Dead_TC (0C0D84FC)](#trigger-0c0d84fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 49 (GDI_Gone) is clear.

Flag writers in this mission: set local flag 49 (GDI_Gone) at [Check_GDI_Status (097C766C)](#trigger-097c766c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TE_Group_Dead_TC (0C0D831C)](#trigger-0c0d831c).
2. Enable and reset applicable timers for [TE_TC_ChangeHouse (06C87C7C)](#trigger-06c87c7c).
3. Enable and reset applicable timers for [Send_TC_Engineer (0BC4E24C)](#trigger-0bc4e24c).
4. Disable [TE_Group_Alive_TC (0C0D840C)](#trigger-0c0d840c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13996, Events line 14374, Actions line 14752.

<a id="trigger-0c0d831c"></a>

### 68. TE_Group_Dead_TC - 0C0D831C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_Group_Alive_TC (0C0D840C)](#trigger-0c0d840c).

Incoming activation links: enable from [TF_Group_Dead_TC (0C0D84FC)](#trigger-0c0d84fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 49 (GDI_Gone) is set.

Flag writers in this mission: set local flag 49 (GDI_Gone) at [Check_GDI_Status (097C766C)](#trigger-097c766c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TE_Group_Alive_TC (0C0D840C)](#trigger-0c0d840c).
2. Enable and reset applicable timers for [TD_Group_Alive_TC (0C0D822C)](#trigger-0c0d822c).
3. Enable and reset applicable timers for [TD_Group_Dead_TC (0C0D813C)](#trigger-0c0d813c).
4. Disable [TE_Group_Dead_TC (0C0D831C)](#trigger-0c0d831c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13997, Events line 14375, Actions line 14753.

<a id="trigger-0c10304c"></a>

### 69. Backup1_TD_Change - 0C10304C

Owner reference: Backup1 Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Backup1_Alive_TD (096E4F3C)](#trigger-096e4f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 6 (country/type ARABS; placed owner Arabs).
2. Enable and reset applicable timers for [Backup1_Becomes_TD_1 (0C10509C)](#trigger-0c10509c).
3. Disable [Backup1_TD_Change (0C10304C)](#trigger-0c10304c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13998, Events line 14376, Actions line 14754.

<a id="trigger-0bc6a69c"></a>

### 70. Send_TD_Engineer - 0BC6A69C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Backup1_Alive_TD (096E4F3C)](#trigger-096e4f3c); enable from [TF_Group_Alive_TD (0C4F7B6C)](#trigger-0c4f7b6c); enable from [TE_Group_Alive_TD (0C4F3F3C)](#trigger-0c4f3f3c); enable from [TC_Group_Alive_TD (0C4F3D5C)](#trigger-0c4f3d5c).

Attached scope: tag definitions 0BC6EF4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TD_Engineer (0C2E054C)](all03umd-teams.md#team-0c2e054c).
2. Disable [Send_TD_Engineer (0BC6A69C)](#trigger-0bc6a69c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 13999, Events line 14377, Actions line 14755.

<a id="trigger-0c4f7b6c"></a>

### 71. TF_Group_Alive_TD - 0C4F7B6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Dead_TD (0C13403C)](#trigger-0c13403c).

Incoming activation links: enable from [Backup1_Dead_TD (0C13403C)](#trigger-0c13403c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 43 (PPTF_Gone) is clear.

Flag writers in this mission: set local flag 43 (PPTF_Gone) at [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c); set local flag 43 (PPTF_Gone) at [Check_PPTF_Status (09761A8C)](#trigger-09761a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TF_Group_Dead_TD (0C4F70CC)](#trigger-0c4f70cc).
2. Enable and reset applicable timers for [TF_TD_ChangeHouse (0960459C)](#trigger-0960459c).
3. Enable and reset applicable timers for [Send_TD_Engineer (0BC6A69C)](#trigger-0bc6a69c).
4. Disable [TF_Group_Alive_TD (0C4F7B6C)](#trigger-0c4f7b6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14000, Events line 14378, Actions line 14756.

<a id="trigger-0c4f70cc"></a>

### 72. TF_Group_Dead_TD - 0C4F70CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Group_Alive_TD (0C4F7B6C)](#trigger-0c4f7b6c).

Incoming activation links: enable from [Backup1_Dead_TD (0C13403C)](#trigger-0c13403c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 43 (PPTF_Gone) is set.

Flag writers in this mission: set local flag 43 (PPTF_Gone) at [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c); set local flag 43 (PPTF_Gone) at [Check_PPTF_Status (09761A8C)](#trigger-09761a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TF_Group_Alive_TD (0C4F7B6C)](#trigger-0c4f7b6c).
2. Enable and reset applicable timers for [TE_Group_Alive_TD (0C4F3F3C)](#trigger-0c4f3f3c).
3. Enable and reset applicable timers for [TE_Group_Dead_TD (0C4F3E4C)](#trigger-0c4f3e4c).
4. Disable [TF_Group_Dead_TD (0C4F70CC)](#trigger-0c4f70cc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14001, Events line 14379, Actions line 14757.

<a id="trigger-09566e6c"></a>

### 73. Backup1_Becomes_TF2 - 09566E6C

Owner reference: PPTF Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Becomes_TF1 (095656BC)](#trigger-095656bc).

Incoming activation links: enable from [Backup1_Becomes_TF1 (095656BC)](#trigger-095656bc).

Attached scope: tag definitions 09565BEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Lasher3 (095B706C)](all03umd-teams.md#team-095b706c).
2. Create/recruit team [TEAM_TF_Virus (095B8A4C)](all03umd-teams.md#team-095b8a4c).
3. Create/recruit team [TEAM_TF_Yuri1 (095B859C)](all03umd-teams.md#team-095b859c).
4. Create/recruit team [TEAM_TF_Yuri2 (095B813C)](all03umd-teams.md#team-095b813c).
5. Disable [Backup1_Becomes_TF2 (09566E6C)](#trigger-09566e6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14002, Events line 14380, Actions line 14758.

<a id="trigger-097a4e2c"></a>

### 74. TE_TF_DestroyTeam1 - 097A4E2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_TF_ChangeHouse (097A178C)](#trigger-097a178c).

Incoming activation links: enable from [TE_TF_ChangeHouse (097A178C)](#trigger-097a178c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Gatt1 (0C0B821C)](all03umd-teams.md#team-0c0b821c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Gatt2 (09502E2C)](all03umd-teams.md#team-09502e2c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init1 (0950297C)](all03umd-teams.md#team-0950297c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init2 (0950251C)](all03umd-teams.md#team-0950251c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init3 (095020BC)](all03umd-teams.md#team-095020bc).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init4 (0950D50C)](all03umd-teams.md#team-0950d50c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Lasher1 (0950D16C)](all03umd-teams.md#team-0950d16c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Lasher2 (0950D03C)](all03umd-teams.md#team-0950d03c).
9. Enable and reset applicable timers for [TE_TF_DestroyTeam2 (097A4D3C)](#trigger-097a4d3c).
10. Disable [TE_TF_DestroyTeam1 (097A4E2C)](#trigger-097a4e2c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14003, Events line 14381, Actions line 14759.

<a id="trigger-0bd4750c"></a>

### 75. TC_TF_ChangeHouse - 0BD4750C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TC_Group_Alive_TF (0B43344C)](#trigger-0b43344c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 14 (country/type PPTF COUNTRY; placed owner PPTFHouse).
2. Enable and reset applicable timers for [TC_TF_DestroyTeam1 (0B42D7BC)](#trigger-0b42d7bc).
3. Disable [TC_TF_ChangeHouse (0BD4750C)](#trigger-0bd4750c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14004, Events line 14382, Actions line 14760.

<a id="trigger-096db61c"></a>

### 76. TD_Group_Alive_TF - 096DB61C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_Group_Dead_TF (0B43335C)](#trigger-0b43335c).

Incoming activation links: enable from [TC_Group_Dead_TF (0B43335C)](#trigger-0b43335c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 47 (Arabs_Gone) is clear.

Flag writers in this mission: set local flag 47 (Arabs_Gone) at [Check_Arab_Status (097E43EC)](#trigger-097e43ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TD_Group_Dead_TF (096D9F3C)](#trigger-096d9f3c).
2. Enable and reset applicable timers for [TD_TF_ChangeHouse (0C08ECFC)](#trigger-0c08ecfc).
3. Enable and reset applicable timers for [Send_TF_Engineer (0BCB74FC)](#trigger-0bcb74fc).
4. Disable [TD_Group_Alive_TF (096DB61C)](#trigger-096db61c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14005, Events line 14383, Actions line 14761.

<a id="trigger-096d9f3c"></a>

### 77. TD_Group_Dead_TF - 096D9F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_Group_Alive_TF (096DB61C)](#trigger-096db61c).

Incoming activation links: enable from [TC_Group_Dead_TF (0B43335C)](#trigger-0b43335c).

Attached scope: tag definitions 097F138C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 47 (Arabs_Gone) is set.

Flag writers in this mission: set local flag 47 (Arabs_Gone) at [Check_Arab_Status (097E43EC)](#trigger-097e43ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TD_Group_Alive_TF (096DB61C)](#trigger-096db61c).
2. Disable [TD_Group_Dead_TF (096D9F3C)](#trigger-096d9f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14006, Events line 14384, Actions line 14762.

<a id="trigger-0970d39c"></a>

### 78. French_Dead_TB - 0970D39C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [French_Alive_TB (0970D56C)](#trigger-0970d56c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 44 (French_Gone) is set.

Flag writers in this mission: set local flag 44 (French_Gone) at [Check_French_Status (096C58BC)](#trigger-096c58bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [French_Alive_TB (0970D56C)](#trigger-0970d56c).
2. Enable and reset applicable timers for [TA_Group_Alive_TB (0970D15C)](#trigger-0970d15c).
3. Enable and reset applicable timers for [TA_Group_Dead_TB (0970D06C)](#trigger-0970d06c).
4. Disable [French_Dead_TB (0970D39C)](#trigger-0970d39c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14007, Events line 14385, Actions line 14763.

<a id="trigger-0c53a03c"></a>

### 79. TA_TB_ChangeHouse - 0C53A03C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TA_Group_Alive_TB (0970D15C)](#trigger-0970d15c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 11 (country/type NOD; placed owner Nod).
2. Enable and reset applicable timers for [TA_TB_DestroyTeam1 (0C770F3C)](#trigger-0c770f3c).
3. Disable [TA_TB_ChangeHouse (0C53A03C)](#trigger-0c53a03c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14008, Events line 14386, Actions line 14764.

<a id="trigger-0bc4f34c"></a>

### 80. Send_TB_Engineer - 0BC4F34C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TA_Group_Alive_TB (0970D15C)](#trigger-0970d15c); enable from [French_Alive_TB (0970D56C)](#trigger-0970d56c).

Attached scope: tag definitions 0BC4DE7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TB_Engineer (0C886EFC)](all03umd-teams.md#team-0c886efc).
2. Disable [Send_TB_Engineer (0BC4F34C)](#trigger-0bc4f34c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14009, Events line 14387, Actions line 14765.

<a id="trigger-096d14cc"></a>

### 81. Backup1_Becomes_TE_2 - 096D14CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Becomes_TE_1 (096D15BC)](#trigger-096d15bc).

Incoming activation links: enable from [Backup1_Becomes_TE_1 (096D15BC)](#trigger-096d15bc).

Attached scope: tag definitions 096D188C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TE_Lasher3 (0950F66C)](all03umd-teams.md#team-0950f66c).
2. Create/recruit team [TEAM_TE_Virus (0950F20C)](all03umd-teams.md#team-0950f20c).
3. Create/recruit team [TEAM_TE_Yuri1 (0950EC8C)](all03umd-teams.md#team-0950ec8c).
4. Create/recruit team [TEAM_TE_Yuri2 (0950E65C)](all03umd-teams.md#team-0950e65c).
5. Disable [Backup1_Becomes_TE_2 (096D14CC)](#trigger-096d14cc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14010, Events line 14388, Actions line 14766.

<a id="trigger-096e6c8c"></a>

### 82. TF_TE_DestroyTeam1 - 096E6C8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_TE_ChangeHouse (096E6E5C)](#trigger-096e6e5c).

Incoming activation links: enable from [TF_TE_ChangeHouse (096E6E5C)](#trigger-096e6e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Gatt1 (095B536C)](all03umd-teams.md#team-095b536c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Gatt2 (095B6D7C)](all03umd-teams.md#team-095b6d7c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init1 (095B68CC)](all03umd-teams.md#team-095b68cc).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init2 (095B606C)](all03umd-teams.md#team-095b606c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init3 (095B7C0C)](all03umd-teams.md#team-095b7c0c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init4 (095B782C)](all03umd-teams.md#team-095b782c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Lasher1 (095B740C)](all03umd-teams.md#team-095b740c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Lasher2 (0BA5FC1C)](all03umd-teams.md#team-0ba5fc1c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14011, Events line 14389, Actions line 14767.

<a id="trigger-0c0de0dc"></a>

### 83. TC_TE_ChangeHouse - 0C0DE0DC

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TC_Group_Alive_TE (096E07EC)](#trigger-096e07ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 10 (country/type GDI; placed owner GDI).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14012, Events line 14390, Actions line 14768.

<a id="trigger-06c7812c"></a>

### 84. TD_Group_Alive_TE - 06C7812C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_Group_Dead_TE (096E06FC)](#trigger-096e06fc).

Incoming activation links: enable from [TC_Group_Dead_TE (096E06FC)](#trigger-096e06fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 47 (Arabs_Gone) is clear.

Flag writers in this mission: set local flag 47 (Arabs_Gone) at [Check_Arab_Status (097E43EC)](#trigger-097e43ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TD_Group_Dead_TE (06C7803C)](#trigger-06c7803c).
2. Enable and reset applicable timers for [TD_TE_ChangeHouse (0955BA5C)](#trigger-0955ba5c).
3. Enable and reset applicable timers for [Send_TE_Engineer (0BCB659C)](#trigger-0bcb659c).
4. Disable [TD_Group_Alive_TE (06C7812C)](#trigger-06c7812c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14013, Events line 14391, Actions line 14769.

<a id="trigger-06c7803c"></a>

### 85. TD_Group_Dead_TE - 06C7803C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_Group_Alive_TE (06C7812C)](#trigger-06c7812c).

Incoming activation links: enable from [TC_Group_Dead_TE (096E06FC)](#trigger-096e06fc).

Attached scope: tag definitions 0946804C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 47 (Arabs_Gone) is set.

Flag writers in this mission: set local flag 47 (Arabs_Gone) at [Check_Arab_Status (097E43EC)](#trigger-097e43ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TD_Group_Alive_TE (06C7812C)](#trigger-06c7812c).
2. Disable [TD_Group_Dead_TE (06C7803C)](#trigger-06c7803c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14014, Events line 14392, Actions line 14770.

<a id="trigger-098c9a8c"></a>

### 86. TB_Group_Dead_TA - 098C9A8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_Group_Alive_TA (098C9B7C)](#trigger-098c9b7c).

Incoming activation links: enable from [French_Dead_TA (098CC15C)](#trigger-098cc15c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 45 (Nod_Gone) is set.

Flag writers in this mission: set local flag 45 (Nod_Gone) at [Check_Nod_Status (0961F45C)](#trigger-0961f45c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TB_Group_Alive_TA (098C9B7C)](#trigger-098c9b7c).
2. Disable [TB_Group_Dead_TA (098C9A8C)](#trigger-098c9a8c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14015, Events line 14393, Actions line 14771.

<a id="trigger-0b58a03c"></a>

### 87. French_TA_Change - 0B58A03C

Owner reference: French. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [French_Alive_TA (098CC24C)](#trigger-098cc24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 8 (country/type RUSSIANS; placed owner Russians).
2. Enable and reset applicable timers for [French_Becomes_TA_1 (0C54603C)](#trigger-0c54603c).
3. Disable [French_TA_Change (0B58A03C)](#trigger-0b58a03c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14016, Events line 14394, Actions line 14772.

<a id="trigger-096f185c"></a>

### 88. Send_TA_Engineer - 096F185C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [French_Alive_TA (098CC24C)](#trigger-098cc24c); enable from [TB_Group_Alive_TA (098C9B7C)](#trigger-098c9b7c).

Attached scope: tag definitions 096ECB2C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TA_Engineer (0C88543C)](all03umd-teams.md#team-0c88543c).
2. Disable [Send_TA_Engineer (096F185C)](#trigger-096f185c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14017, Events line 14395, Actions line 14773.

<a id="trigger-098c9b7c"></a>

### 89. TB_Group_Alive_TA - 098C9B7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [French_Dead_TA (098CC15C)](#trigger-098cc15c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 45 (Nod_Gone) is clear.

Flag writers in this mission: set local flag 45 (Nod_Gone) at [Check_Nod_Status (0961F45C)](#trigger-0961f45c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TB_Group_Dead_TA (098C9A8C)](#trigger-098c9a8c).
2. Enable and reset applicable timers for [TB_Change_House (096AE6FC)](#trigger-096ae6fc).
3. Enable and reset applicable timers for [Send_TA_Engineer (096F185C)](#trigger-096f185c).
4. Disable [TB_Group_Alive_TA (098C9B7C)](#trigger-098c9b7c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14018, Events line 14396, Actions line 14774.

<a id="trigger-0975579c"></a>

### 90. Backup1_Becomes_TC_2 - 0975579C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Becomes_TC_1 (0975588C)](#trigger-0975588c).

Incoming activation links: enable from [Backup1_Becomes_TC_1 (0975588C)](#trigger-0975588c).

Attached scope: tag definitions 06C80C2C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Lasher3 (06C6E0FC)](all03umd-teams.md#team-06c6e0fc).
2. Create/recruit team [TEAM_TC_Virus (06C6B95C)](all03umd-teams.md#team-06c6b95c).
3. Create/recruit team [TEAM_TC_Yuri1 (06C6B53C)](all03umd-teams.md#team-06c6b53c).
4. Create/recruit team [TEAM_TC_Yuri2 (06C6B11C)](all03umd-teams.md#team-06c6b11c).
5. Disable [Backup1_Becomes_TC_2 (0975579C)](#trigger-0975579c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14019, Events line 14397, Actions line 14775.

<a id="trigger-0975a12c"></a>

### 91. TF_ChangeGuard1 - 0975A12C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Change_House (0975ABAC)](#trigger-0975abac).

Incoming activation links: enable from [TF_Change_House (0975ABAC)](#trigger-0975abac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Gatt1 (095B536C)](all03umd-teams.md#team-095b536c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Gatt2 (095B6D7C)](all03umd-teams.md#team-095b6d7c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init1 (095B68CC)](all03umd-teams.md#team-095b68cc).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init2 (095B606C)](all03umd-teams.md#team-095b606c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init3 (095B7C0C)](all03umd-teams.md#team-095b7c0c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init4 (095B782C)](all03umd-teams.md#team-095b782c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Lasher1 (095B740C)](all03umd-teams.md#team-095b740c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Lasher2 (0BA5FC1C)](all03umd-teams.md#team-0ba5fc1c).
9. Enable and reset applicable timers for [TF_ChangeGuard2 (0975B8BC)](#trigger-0975b8bc).
10. Disable [TF_ChangeGuard1 (0975A12C)](#trigger-0975a12c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14020, Events line 14398, Actions line 14776.

<a id="trigger-06c87c7c"></a>

### 92. TE_TC_ChangeHouse - 06C87C7C

Owner reference: GDI. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TE_Group_Alive_TC (0C0D840C)](#trigger-0c0d840c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. Enable and reset applicable timers for [TE_TC_DestroyTeam1 (06C87AAC)](#trigger-06c87aac).
3. Disable [TE_TC_ChangeHouse (06C87C7C)](#trigger-06c87c7c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14021, Events line 14399, Actions line 14777.

<a id="trigger-0c0d822c"></a>

### 93. TD_Group_Alive_TC - 0C0D822C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_Group_Dead_TC (0C0D831C)](#trigger-0c0d831c).

Incoming activation links: enable from [TE_Group_Dead_TC (0C0D831C)](#trigger-0c0d831c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 47 (Arabs_Gone) is clear.

Flag writers in this mission: set local flag 47 (Arabs_Gone) at [Check_Arab_Status (097E43EC)](#trigger-097e43ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TD_Group_Dead_TC (0C0D813C)](#trigger-0c0d813c).
2. Enable and reset applicable timers for [TD_TC_ChangeHouse (09490F3C)](#trigger-09490f3c).
3. Enable and reset applicable timers for [Send_TC_Engineer (0BC4E24C)](#trigger-0bc4e24c).
4. Disable [TD_Group_Alive_TC (0C0D822C)](#trigger-0c0d822c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14022, Events line 14400, Actions line 14778.

<a id="trigger-0c0d813c"></a>

### 94. TD_Group_Dead_TC - 0C0D813C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_Group_Alive_TC (0C0D822C)](#trigger-0c0d822c).

Incoming activation links: enable from [TE_Group_Dead_TC (0C0D831C)](#trigger-0c0d831c).

Attached scope: tag definitions 0C0DCE5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 47 (Arabs_Gone) is set.

Flag writers in this mission: set local flag 47 (Arabs_Gone) at [Check_Arab_Status (097E43EC)](#trigger-097e43ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TD_Group_Alive_TC (0C0D822C)](#trigger-0c0d822c).
2. Disable [TD_Group_Dead_TC (0C0D813C)](#trigger-0c0d813c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14023, Events line 14401, Actions line 14779.

<a id="trigger-0c10509c"></a>

### 95. Backup1_Becomes_TD_1 - 0C10509C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_TD_Change (0C10304C)](#trigger-0c10304c).

Incoming activation links: enable from [Backup1_TD_Change (0C10304C)](#trigger-0c10304c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TD_Gatt1 (096586BC)](all03umd-teams.md#team-096586bc).
2. Create/recruit team [TEAM_TD_Gatt2 (09650B4C)](all03umd-teams.md#team-09650b4c).
3. Create/recruit team [TEAM_TD_Init1 (0967732C)](all03umd-teams.md#team-0967732c).
4. Create/recruit team [TEAM_TD_Init2 (0967092C)](all03umd-teams.md#team-0967092c).
5. Create/recruit team [TEAM_TD_Init3 (0967047C)](all03umd-teams.md#team-0967047c).
6. Create/recruit team [TEAM_TD_Init4 (0967028C)](all03umd-teams.md#team-0967028c).
7. Create/recruit team [TEAM_TD_Lasher1 (09663E5C)](all03umd-teams.md#team-09663e5c).
8. Create/recruit team [TEAM_TD_Lasher2 (096639AC)](all03umd-teams.md#team-096639ac).
9. Enable and reset applicable timers for [Backup1_Becomes_TD_2 (0C1076FC)](#trigger-0c1076fc).
10. Disable [Backup1_Becomes_TD_1 (0C10509C)](#trigger-0c10509c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14024, Events line 14402, Actions line 14780.

<a id="trigger-0960459c"></a>

### 96. TF_TD_ChangeHouse - 0960459C

Owner reference: PPTF Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TF_Group_Alive_TD (0C4F7B6C)](#trigger-0c4f7b6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 6 (country/type ARABS; placed owner Arabs).
2. Enable and reset applicable timers for [TF_TD_DestroyTeam1 (096044AC)](#trigger-096044ac).
3. Disable [TF_TD_ChangeHouse (0960459C)](#trigger-0960459c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14025, Events line 14403, Actions line 14781.

<a id="trigger-0c4f3f3c"></a>

### 97. TE_Group_Alive_TD - 0C4F3F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Group_Dead_TD (0C4F70CC)](#trigger-0c4f70cc).

Incoming activation links: enable from [TF_Group_Dead_TD (0C4F70CC)](#trigger-0c4f70cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 49 (GDI_Gone) is clear.

Flag writers in this mission: set local flag 49 (GDI_Gone) at [Check_GDI_Status (097C766C)](#trigger-097c766c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TE_Group_Dead_TD (0C4F3E4C)](#trigger-0c4f3e4c).
2. Enable and reset applicable timers for [TE_TD_ChangeHouse (0B5B432C)](#trigger-0b5b432c).
3. Enable and reset applicable timers for [Send_TD_Engineer (0BC6A69C)](#trigger-0bc6a69c).
4. Disable [TE_Group_Alive_TD (0C4F3F3C)](#trigger-0c4f3f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14026, Events line 14404, Actions line 14782.

<a id="trigger-0c4f3e4c"></a>

### 98. TE_Group_Dead_TD - 0C4F3E4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_Group_Alive_TD (0C4F3F3C)](#trigger-0c4f3f3c).

Incoming activation links: enable from [TF_Group_Dead_TD (0C4F70CC)](#trigger-0c4f70cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 49 (GDI_Gone) is set.

Flag writers in this mission: set local flag 49 (GDI_Gone) at [Check_GDI_Status (097C766C)](#trigger-097c766c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TE_Group_Alive_TD (0C4F3F3C)](#trigger-0c4f3f3c).
2. Enable and reset applicable timers for [TC_Group_Alive_TD (0C4F3D5C)](#trigger-0c4f3d5c).
3. Enable and reset applicable timers for [TC_Group_Dead_TD (0C4F696C)](#trigger-0c4f696c).
4. Disable [TE_Group_Dead_TD (0C4F3E4C)](#trigger-0c4f3e4c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14027, Events line 14405, Actions line 14783.

<a id="trigger-097a4d3c"></a>

### 99. TE_TF_DestroyTeam2 - 097A4D3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_TF_DestroyTeam1 (097A4E2C)](#trigger-097a4e2c).

Incoming activation links: enable from [TE_TF_DestroyTeam1 (097A4E2C)](#trigger-097a4e2c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Lasher3 (0950F66C)](all03umd-teams.md#team-0950f66c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Virus (0950F20C)](all03umd-teams.md#team-0950f20c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Yuri1 (0950EC8C)](all03umd-teams.md#team-0950ec8c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Yuri2 (0950E65C)](all03umd-teams.md#team-0950e65c).
5. Enable and reset applicable timers for [TE_Becomes_TF_1 (097A417C)](#trigger-097a417c).
6. Disable [TE_TF_DestroyTeam2 (097A4D3C)](#trigger-097a4d3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14028, Events line 14406, Actions line 14784.

<a id="trigger-0b42d7bc"></a>

### 100. TC_TF_DestroyTeam1 - 0B42D7BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_TF_ChangeHouse (0BD4750C)](#trigger-0bd4750c).

Incoming activation links: enable from [TC_TF_ChangeHouse (0BD4750C)](#trigger-0bd4750c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Gatt1 (0967471C)](all03umd-teams.md#team-0967471c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Gatt2 (09675EFC)](all03umd-teams.md#team-09675efc).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init1 (09675B1C)](all03umd-teams.md#team-09675b1c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init2 (096756FC)](all03umd-teams.md#team-096756fc).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init3 (0BE0D2BC)](all03umd-teams.md#team-0be0d2bc).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init4 (06C6FEFC)](all03umd-teams.md#team-06c6fefc).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Lasher1 (06C6F82C)](all03umd-teams.md#team-06c6f82c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Lasher2 (06C6F21C)](all03umd-teams.md#team-06c6f21c).
9. Enable and reset applicable timers for [TC_TF_DestroyTeam2 (0B42D3BC)](#trigger-0b42d3bc).
10. Disable [TC_TF_DestroyTeam1 (0B42D7BC)](#trigger-0b42d7bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14029, Events line 14407, Actions line 14785.

<a id="trigger-0c08ecfc"></a>

### 101. TD_TF_ChangeHouse - 0C08ECFC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TD_Group_Alive_TF (096DB61C)](#trigger-096db61c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 47 (Arabs_Gone) is clear.

Flag writers in this mission: set local flag 47 (Arabs_Gone) at [Check_Arab_Status (097E43EC)](#trigger-097e43ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 14 (country/type PPTF COUNTRY; placed owner PPTFHouse).
2. Enable and reset applicable timers for [TD_TF_DestroyTeam1 (0C08E68C)](#trigger-0c08e68c).
3. Disable [TD_TF_ChangeHouse (0C08ECFC)](#trigger-0c08ecfc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14030, Events line 14408, Actions line 14786.

<a id="trigger-0970d56c"></a>

### 102. French_Alive_TB - 0970D56C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 44 (French_Gone) is clear.

Flag writers in this mission: set local flag 44 (French_Gone) at [Check_French_Status (096C58BC)](#trigger-096c58bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [French_Dead_TB (0970D39C)](#trigger-0970d39c).
2. Enable and reset applicable timers for [French_Change_House (0BB3B28C)](#trigger-0bb3b28c).
3. Enable and reset applicable timers for [Send_TB_Engineer (0BC4F34C)](#trigger-0bc4f34c).
4. Disable [French_Alive_TB (0970D56C)](#trigger-0970d56c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14031, Events line 14409, Actions line 14787.

<a id="trigger-0c770f3c"></a>

### 103. TA_TB_DestroyTeam1 - 0C770F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TA_TB_ChangeHouse (0C53A03C)](#trigger-0c53a03c).

Incoming activation links: enable from [TA_TB_ChangeHouse (0C53A03C)](#trigger-0c53a03c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Gatt1 (0DA10A7C)](all03umd-teams.md#team-0da10a7c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Gatt2 (0DA1083C)](all03umd-teams.md#team-0da1083c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Init1 (0DA105FC)](all03umd-teams.md#team-0da105fc).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Init2 (0DA103BC)](all03umd-teams.md#team-0da103bc).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Init3 (0DA1017C)](all03umd-teams.md#team-0da1017c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_AB_Init4 (0966954C)](all03umd-teams.md#team-0966954c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Lasher1 (0DA0F32C)](all03umd-teams.md#team-0da0f32c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Lasher2 (0DA10EFC)](all03umd-teams.md#team-0da10efc).
9. Enable and reset applicable timers for [TA_TB_DestroyTeam2 (0C772F3C)](#trigger-0c772f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14032, Events line 14410, Actions line 14788.

<a id="trigger-0955ba5c"></a>

### 104. TD_TE_ChangeHouse - 0955BA5C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TD_Group_Alive_TE (06C7812C)](#trigger-06c7812c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 10 (country/type GDI; placed owner GDI).
2. Enable and reset applicable timers for [TD_TE_DestroyTeam1 (0955B58C)](#trigger-0955b58c).
3. Disable [TD_TE_ChangeHouse (0955BA5C)](#trigger-0955ba5c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14033, Events line 14411, Actions line 14789.

<a id="trigger-0c54603c"></a>

### 105. French_Becomes_TA_1 - 0C54603C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [French_TA_Change (0B58A03C)](#trigger-0b58a03c).

Incoming activation links: enable from [French_TA_Change (0B58A03C)](#trigger-0b58a03c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TA_Gatt1 (0DA10A7C)](all03umd-teams.md#team-0da10a7c).
2. Create/recruit team [TEAM_TA_Gatt2 (0DA1083C)](all03umd-teams.md#team-0da1083c).
3. Create/recruit team [TEAM_TA_Init1 (0DA105FC)](all03umd-teams.md#team-0da105fc).
4. Create/recruit team [TEAM_TA_Init2 (0DA103BC)](all03umd-teams.md#team-0da103bc).
5. Create/recruit team [TEAM_TA_Init3 (0DA1017C)](all03umd-teams.md#team-0da1017c).
6. Create/recruit team [TEAM_TA_Init4 (0DA11DEC)](all03umd-teams.md#team-0da11dec).
7. Create/recruit team [TEAM_TA_Lasher1 (0DA0F32C)](all03umd-teams.md#team-0da0f32c).
8. Create/recruit team [TEAM_TA_Lasher2 (0DA10EFC)](all03umd-teams.md#team-0da10efc).
9. Enable and reset applicable timers for [French_Becomes_TA_2 (0C54F03C)](#trigger-0c54f03c).
10. Disable [French_Becomes_TA_1 (0C54603C)](#trigger-0c54603c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14034, Events line 14412, Actions line 14790.

<a id="trigger-096ae6fc"></a>

### 106. TB_Change_House - 096AE6FC

Owner reference: Nod. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_Change_Guard2 (0952630C)](#trigger-0952630c).

Incoming activation links: enable from [TB_Group_Alive_TA (098C9B7C)](#trigger-098c9b7c); enable from [Yuri_Attack_AA_2 (094BCBFC)](#trigger-094bcbfc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 8 (country/type RUSSIANS; placed owner Russians).
2. Enable and reset applicable timers for [TB_Change_Guard1 (0D45247C)](#trigger-0d45247c).
3. Disable [TB_Change_House (096AE6FC)](#trigger-096ae6fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14035, Events line 14413, Actions line 14791.

<a id="trigger-0975b8bc"></a>

### 107. TF_ChangeGuard2 - 0975B8BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_ChangeGuard1 (0975A12C)](#trigger-0975a12c).

Incoming activation links: enable from [TF_ChangeGuard1 (0975A12C)](#trigger-0975a12c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Lasher3 (095B706C)](all03umd-teams.md#team-095b706c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Virus (095B8A4C)](all03umd-teams.md#team-095b8a4c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Yuri1 (095B859C)](all03umd-teams.md#team-095b859c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Yuri2 (095B813C)](all03umd-teams.md#team-095b813c).
5. Enable and reset applicable timers for [TF_Becomes_TC1 (0975CE6C)](#trigger-0975ce6c).
6. Disable [TF_ChangeGuard2 (0975B8BC)](#trigger-0975b8bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14036, Events line 14414, Actions line 14792.

<a id="trigger-06c87aac"></a>

### 108. TE_TC_DestroyTeam1 - 06C87AAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_TC_ChangeHouse (06C87C7C)](#trigger-06c87c7c).

Incoming activation links: enable from [TE_TC_ChangeHouse (06C87C7C)](#trigger-06c87c7c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Gatt1 (0C0B821C)](all03umd-teams.md#team-0c0b821c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Gatt2 (09502E2C)](all03umd-teams.md#team-09502e2c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init1 (0950297C)](all03umd-teams.md#team-0950297c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init2 (0950251C)](all03umd-teams.md#team-0950251c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init3 (095020BC)](all03umd-teams.md#team-095020bc).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init4 (0950D50C)](all03umd-teams.md#team-0950d50c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Lasher1 (0950D16C)](all03umd-teams.md#team-0950d16c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Lasher2 (0950D03C)](all03umd-teams.md#team-0950d03c).
9. Enable and reset applicable timers for [TE_TC_DestroyTeam2 (06C879BC)](#trigger-06c879bc).
10. Disable [TE_TC_DestroyTeam1 (06C87AAC)](#trigger-06c87aac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14037, Events line 14415, Actions line 14793.

<a id="trigger-09490f3c"></a>

### 109. TD_TC_ChangeHouse - 09490F3C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TD_Group_Alive_TC (0C0D822C)](#trigger-0c0d822c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. Enable and reset applicable timers for [TD_TC_DestroyTeam1 (09490D6C)](#trigger-09490d6c).
3. Disable [TD_TC_ChangeHouse (09490F3C)](#trigger-09490f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14038, Events line 14416, Actions line 14794.

<a id="trigger-0c1076fc"></a>

### 110. Backup1_Becomes_TD_2 - 0C1076FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backup1_Becomes_TD_1 (0C10509C)](#trigger-0c10509c).

Incoming activation links: enable from [Backup1_Becomes_TD_1 (0C10509C)](#trigger-0c10509c).

Attached scope: tag definitions 0C10518C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TD_Lasher3 (09661CDC)](all03umd-teams.md#team-09661cdc).
2. Create/recruit team [TEAM_TD_Virus (0967699C)](all03umd-teams.md#team-0967699c).
3. Create/recruit team [TEAM_TD_Yuri1 (09668E2C)](all03umd-teams.md#team-09668e2c).
4. Create/recruit team [TEAM_TD_Yuri2 (0966897C)](all03umd-teams.md#team-0966897c).
5. Disable [Backup1_Becomes_TD_2 (0C1076FC)](#trigger-0c1076fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14039, Events line 14417, Actions line 14795.

<a id="trigger-096044ac"></a>

### 111. TF_TD_DestroyTeam1 - 096044AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_TD_ChangeHouse (0960459C)](#trigger-0960459c).

Incoming activation links: enable from [TF_TD_ChangeHouse (0960459C)](#trigger-0960459c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Gatt1 (095B536C)](all03umd-teams.md#team-095b536c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Gatt2 (095B6D7C)](all03umd-teams.md#team-095b6d7c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init1 (095B68CC)](all03umd-teams.md#team-095b68cc).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init2 (095B606C)](all03umd-teams.md#team-095b606c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init3 (095B7C0C)](all03umd-teams.md#team-095b7c0c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Init4 (095B782C)](all03umd-teams.md#team-095b782c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Lasher1 (095B740C)](all03umd-teams.md#team-095b740c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Lasher2 (0BA5FC1C)](all03umd-teams.md#team-0ba5fc1c).
9. Enable and reset applicable timers for [TF_TD_DestroyTeam2 (0960626C)](#trigger-0960626c).
10. Disable [TF_TD_DestroyTeam1 (096044AC)](#trigger-096044ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14040, Events line 14418, Actions line 14796.

<a id="trigger-0b5b432c"></a>

### 112. TE_TD_ChangeHouse - 0B5B432C

Owner reference: GDI. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TE_Group_Alive_TD (0C4F3F3C)](#trigger-0c4f3f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 6 (country/type ARABS; placed owner Arabs).
2. Enable and reset applicable timers for [TE_TD_DestroyTeam1 (0B5A1E5C)](#trigger-0b5a1e5c).
3. Disable [TE_TD_ChangeHouse (0B5B432C)](#trigger-0b5b432c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14041, Events line 14419, Actions line 14797.

<a id="trigger-0c4f3d5c"></a>

### 113. TC_Group_Alive_TD - 0C4F3D5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_Group_Dead_TD (0C4F3E4C)](#trigger-0c4f3e4c).

Incoming activation links: enable from [TE_Group_Dead_TD (0C4F3E4C)](#trigger-0c4f3e4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [TC_Group_Dead_TD (0C4F696C)](#trigger-0c4f696c).
2. Enable and reset applicable timers for [TC_ChangeHouse (095F27CC)](#trigger-095f27cc).
3. Enable and reset applicable timers for [Send_TD_Engineer (0BC6A69C)](#trigger-0bc6a69c).
4. Disable [TC_Group_Alive_TD (0C4F3D5C)](#trigger-0c4f3d5c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14042, Events line 14420, Actions line 14798.

<a id="trigger-0c4f696c"></a>

### 114. TC_Group_Dead_TD - 0C4F696C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_Group_Alive_TD (0C4F3D5C)](#trigger-0c4f3d5c).

Incoming activation links: enable from [TE_Group_Dead_TD (0C4F3E4C)](#trigger-0c4f3e4c).

Attached scope: tag definitions 096E4E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 48 (Confed_Gone) is set.

Flag writers in this mission: set local flag 48 (Confed_Gone) at [Check_Confed_Status (097E4A8C)](#trigger-097e4a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [TC_Group_Alive_TD (0C4F3D5C)](#trigger-0c4f3d5c).
2. Disable [TC_Group_Dead_TD (0C4F696C)](#trigger-0c4f696c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14043, Events line 14421, Actions line 14799.

<a id="trigger-097a417c"></a>

### 115. TE_Becomes_TF_1 - 097A417C

Owner reference: PPTF Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_TF_DestroyTeam2 (097A4D3C)](#trigger-097a4d3c).

Incoming activation links: enable from [TE_TF_DestroyTeam2 (097A4D3C)](#trigger-097a4d3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Gatt1 (095B536C)](all03umd-teams.md#team-095b536c).
2. Create/recruit team [TEAM_TF_Gatt2 (095B6D7C)](all03umd-teams.md#team-095b6d7c).
3. Create/recruit team [TEAM_TF_Init1 (095B68CC)](all03umd-teams.md#team-095b68cc).
4. Create/recruit team [TEAM_TF_Init2 (095B606C)](all03umd-teams.md#team-095b606c).
5. Create/recruit team [TEAM_TF_Init3 (095B7C0C)](all03umd-teams.md#team-095b7c0c).
6. Create/recruit team [TEAM_TF_Init4 (095B782C)](all03umd-teams.md#team-095b782c).
7. Create/recruit team [TEAM_TF_Lasher1 (095B740C)](all03umd-teams.md#team-095b740c).
8. Create/recruit team [TEAM_TF_Lasher2 (0BA5FC1C)](all03umd-teams.md#team-0ba5fc1c).
9. Enable and reset applicable timers for [TE_Becomes_TF_2 (097A408C)](#trigger-097a408c).
10. Disable [TE_Becomes_TF_1 (097A417C)](#trigger-097a417c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14044, Events line 14422, Actions line 14800.

<a id="trigger-0b42d3bc"></a>

### 116. TC_TF_DestroyTeam2 - 0B42D3BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_TF_DestroyTeam1 (0B42D7BC)](#trigger-0b42d7bc).

Incoming activation links: enable from [TC_TF_DestroyTeam1 (0B42D7BC)](#trigger-0b42d7bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Lasher3 (06C6E0FC)](all03umd-teams.md#team-06c6e0fc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Virus (06C6B95C)](all03umd-teams.md#team-06c6b95c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Yuri1 (06C6B53C)](all03umd-teams.md#team-06c6b53c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Yuri2 (06C6B11C)](all03umd-teams.md#team-06c6b11c).
5. Enable and reset applicable timers for [TC_Becomes_TF_1 (0B42CF3C)](#trigger-0b42cf3c).
6. Disable [TC_TF_DestroyTeam2 (0B42D3BC)](#trigger-0b42d3bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14045, Events line 14423, Actions line 14801.

<a id="trigger-0c08e68c"></a>

### 117. TD_TF_DestroyTeam1 - 0C08E68C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_TF_ChangeHouse (0C08ECFC)](#trigger-0c08ecfc).

Incoming activation links: enable from [TD_TF_ChangeHouse (0C08ECFC)](#trigger-0c08ecfc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Gatt1 (096586BC)](all03umd-teams.md#team-096586bc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Gatt2 (09650B4C)](all03umd-teams.md#team-09650b4c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init1 (0967732C)](all03umd-teams.md#team-0967732c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init2 (0967092C)](all03umd-teams.md#team-0967092c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init3 (0967047C)](all03umd-teams.md#team-0967047c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init4 (0967028C)](all03umd-teams.md#team-0967028c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher1 (09663E5C)](all03umd-teams.md#team-09663e5c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher2 (096639AC)](all03umd-teams.md#team-096639ac).
9. Enable and reset applicable timers for [TD_TF_DestroyTeam2 (0C08E59C)](#trigger-0c08e59c).
10. Disable [TC_TF_DestroyTeam1 (0B42D7BC)](#trigger-0b42d7bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14046, Events line 14424, Actions line 14802.

<a id="trigger-0bb3b28c"></a>

### 118. French_Change_House - 0BB3B28C

Owner reference: French. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [French_Alive_TB (0970D56C)](#trigger-0970d56c); enable from [TB_Becomes_TA_2 (096A2B2C)](#trigger-096a2b2c); enable from [TB_Becomes_AB_2 (09684AFC)](#trigger-09684afc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 44 (French_Gone) is clear.
2. 0 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 44 (French_Gone) at [Check_French_Status (096C58BC)](#trigger-096c58bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 11 (country/type NOD; placed owner Nod).
2. Enable and reset applicable timers for [Frnch_Become_TB1 (0D5B5E5C)](#trigger-0d5b5e5c).
3. Disable [French_Change_House (0BB3B28C)](#trigger-0bb3b28c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14047, Events line 14425, Actions line 14803.

<a id="trigger-0c772f3c"></a>

### 119. TA_TB_DestroyTeam2 - 0C772F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TA_TB_DestroyTeam1 (0C770F3C)](#trigger-0c770f3c).

Incoming activation links: enable from [TA_TB_DestroyTeam1 (0C770F3C)](#trigger-0c770f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Lasher3 (0DA10CBC)](all03umd-teams.md#team-0da10cbc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Virus1 (0DA1172C)](all03umd-teams.md#team-0da1172c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Yuri1 (0DA11BAC)](all03umd-teams.md#team-0da11bac).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Yuri2 (0DA1196C)](all03umd-teams.md#team-0da1196c).
5. Enable and reset applicable timers for [TA_Becomes_TB_1 (0C776F3C)](#trigger-0c776f3c).
6. Disable [TA_TB_DestroyTeam2 (0C772F3C)](#trigger-0c772f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14048, Events line 14426, Actions line 14804.

<a id="trigger-0955b58c"></a>

### 120. TD_TE_DestroyTeam1 - 0955B58C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_TE_ChangeHouse (0955BA5C)](#trigger-0955ba5c).

Incoming activation links: enable from [TD_TE_ChangeHouse (0955BA5C)](#trigger-0955ba5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Gatt1 (096586BC)](all03umd-teams.md#team-096586bc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Gatt2 (09650B4C)](all03umd-teams.md#team-09650b4c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init1 (0967732C)](all03umd-teams.md#team-0967732c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init2 (0967092C)](all03umd-teams.md#team-0967092c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init3 (0967047C)](all03umd-teams.md#team-0967047c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init4 (0967028C)](all03umd-teams.md#team-0967028c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher1 (09663E5C)](all03umd-teams.md#team-09663e5c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher2 (096639AC)](all03umd-teams.md#team-096639ac).
9. Enable and reset applicable timers for [TD_TE_DestroyTeam2 (0955B49C)](#trigger-0955b49c).
10. Disable [TD_TE_DestroyTeam1 (0955B58C)](#trigger-0955b58c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14049, Events line 14427, Actions line 14805.

<a id="trigger-0c54f03c"></a>

### 121. French_Becomes_TA_2 - 0C54F03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [French_Becomes_TA_1 (0C54603C)](#trigger-0c54603c).

Incoming activation links: enable from [French_Becomes_TA_1 (0C54603C)](#trigger-0c54603c).

Attached scope: tag definitions 0B5A074C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TA_Lasher3 (0DA10CBC)](all03umd-teams.md#team-0da10cbc).
2. Create/recruit team [TEAM_TA_Virus1 (0DA1172C)](all03umd-teams.md#team-0da1172c).
3. Create/recruit team [TEAM_TA_Yuri1 (0DA11BAC)](all03umd-teams.md#team-0da11bac).
4. Create/recruit team [TEAM_TA_Yuri2 (0DA1196C)](all03umd-teams.md#team-0da1196c).
5. Disable [French_Becomes_TA_2 (0C54F03C)](#trigger-0c54f03c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14050, Events line 14428, Actions line 14806.

<a id="trigger-0952630c"></a>

### 122. TB_Change_Guard2 - 0952630C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_Change_Guard1 (0D45247C)](#trigger-0d45247c).

Incoming activation links: enable from [TB_Change_Guard1 (0D45247C)](#trigger-0d45247c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Lasher3 (0AFC417C)](all03umd-teams.md#team-0afc417c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Virus (0AFC372C)](all03umd-teams.md#team-0afc372c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Yuri1 (0AFC34EC)](all03umd-teams.md#team-0afc34ec).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Yuri2 (0AFC59AC)](all03umd-teams.md#team-0afc59ac).
5. Enable and reset applicable timers for [TB_Becomes_TA_1 (096A593C)](#trigger-096a593c).
6. Disable [TB_Change_Guard2 (0952630C)](#trigger-0952630c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14051, Events line 14429, Actions line 14807.

<a id="trigger-0d45247c"></a>

### 123. TB_Change_Guard1 - 0D45247C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TB_Change_House (096AE6FC)](#trigger-096ae6fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 12 (Nuked_MC) is set.
2. 0 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 12 (Nuked_MC) at [Nuke_MC_True (094CE89C)](#trigger-094ce89c); clear local flag 12 (Nuked_MC) at [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Gatt1 (0AFC2DCC)](all03umd-teams.md#team-0afc2dcc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Gatt2 (0AFC322C)](all03umd-teams.md#team-0afc322c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Init1 (0AFC4EFC)](all03umd-teams.md#team-0afc4efc).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Init2 (0AFC4CBC)](all03umd-teams.md#team-0afc4cbc).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Init3 (0AFC4A7C)](all03umd-teams.md#team-0afc4a7c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Init4 (0AFC483C)](all03umd-teams.md#team-0afc483c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Lasher1 (0AFC45FC)](all03umd-teams.md#team-0afc45fc).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Lasher2 (0AFC43BC)](all03umd-teams.md#team-0afc43bc).
9. Enable and reset applicable timers for [TB_Change_Guard2 (0952630C)](#trigger-0952630c).
10. Disable [TB_Change_Guard1 (0D45247C)](#trigger-0d45247c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14052, Events line 14430, Actions line 14808.

<a id="trigger-0975ce6c"></a>

### 124. TF_Becomes_TC1 - 0975CE6C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_ChangeGuard2 (0975B8BC)](#trigger-0975b8bc).

Incoming activation links: enable from [TF_ChangeGuard2 (0975B8BC)](#trigger-0975b8bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Gatt1 (0967471C)](all03umd-teams.md#team-0967471c).
2. Create/recruit team [TEAM_TC_Gatt2 (09675EFC)](all03umd-teams.md#team-09675efc).
3. Create/recruit team [TEAM_TC_Init1 (09675B1C)](all03umd-teams.md#team-09675b1c).
4. Create/recruit team [TEAM_TC_Init2 (096756FC)](all03umd-teams.md#team-096756fc).
5. Create/recruit team [TEAM_TC_Init3 (0BE0D2BC)](all03umd-teams.md#team-0be0d2bc).
6. Create/recruit team [TEAM_TC_Init4 (06C6FEFC)](all03umd-teams.md#team-06c6fefc).
7. Create/recruit team [TEAM_TC_Lasher1 (06C6F82C)](all03umd-teams.md#team-06c6f82c).
8. Create/recruit team [TEAM_TC_Lasher2 (06C6F21C)](all03umd-teams.md#team-06c6f21c).
9. Enable and reset applicable timers for [TF_Becomes_TC2 (0975C66C)](#trigger-0975c66c).
10. Disable [TF_Becomes_TC1 (0975CE6C)](#trigger-0975ce6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14053, Events line 14431, Actions line 14809.

<a id="trigger-06c879bc"></a>

### 125. TE_TC_DestroyTeam2 - 06C879BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_TC_DestroyTeam1 (06C87AAC)](#trigger-06c87aac).

Incoming activation links: enable from [TE_TC_DestroyTeam1 (06C87AAC)](#trigger-06c87aac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Lasher3 (0950F66C)](all03umd-teams.md#team-0950f66c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Virus (0950F20C)](all03umd-teams.md#team-0950f20c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Yuri1 (0950EC8C)](all03umd-teams.md#team-0950ec8c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Yuri2 (0950E65C)](all03umd-teams.md#team-0950e65c).
5. Enable and reset applicable timers for [TE_Becomes_TC_1 (06C878CC)](#trigger-06c878cc).
6. Disable [TE_TC_DestroyTeam2 (06C879BC)](#trigger-06c879bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14054, Events line 14432, Actions line 14810.

<a id="trigger-09490d6c"></a>

### 126. TD_TC_DestroyTeam1 - 09490D6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_TC_ChangeHouse (09490F3C)](#trigger-09490f3c).

Incoming activation links: enable from [TD_TC_ChangeHouse (09490F3C)](#trigger-09490f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Gatt1 (096586BC)](all03umd-teams.md#team-096586bc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Gatt2 (09650B4C)](all03umd-teams.md#team-09650b4c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init1 (0967732C)](all03umd-teams.md#team-0967732c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init2 (0967092C)](all03umd-teams.md#team-0967092c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init3 (0967047C)](all03umd-teams.md#team-0967047c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init4 (0967028C)](all03umd-teams.md#team-0967028c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher1 (09663E5C)](all03umd-teams.md#team-09663e5c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher2 (096639AC)](all03umd-teams.md#team-096639ac).
9. Enable and reset applicable timers for [TD_TC_DestroyTeam2 (09490C7C)](#trigger-09490c7c).
10. Disable [TD_TC_DestroyTeam1 (09490D6C)](#trigger-09490d6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14055, Events line 14433, Actions line 14811.

<a id="trigger-0960626c"></a>

### 127. TF_TD_DestroyTeam2 - 0960626C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_TD_DestroyTeam1 (096044AC)](#trigger-096044ac).

Incoming activation links: enable from [TF_TD_DestroyTeam1 (096044AC)](#trigger-096044ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Lasher3 (095B706C)](all03umd-teams.md#team-095b706c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Virus (095B8A4C)](all03umd-teams.md#team-095b8a4c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Yuri1 (095B859C)](all03umd-teams.md#team-095b859c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TF_Yuri2 (095B813C)](all03umd-teams.md#team-095b813c).
5. Enable and reset applicable timers for [TF_Becomes_TD_1 (0960617C)](#trigger-0960617c).
6. Disable [TF_TD_DestroyTeam2 (0960626C)](#trigger-0960626c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14056, Events line 14434, Actions line 14812.

<a id="trigger-0b5a1e5c"></a>

### 128. TE_TD_DestroyTeam1 - 0B5A1E5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_TD_ChangeHouse (0B5B432C)](#trigger-0b5b432c).

Incoming activation links: enable from [TE_TD_ChangeHouse (0B5B432C)](#trigger-0b5b432c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Gatt1 (0C0B821C)](all03umd-teams.md#team-0c0b821c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Gatt2 (09502E2C)](all03umd-teams.md#team-09502e2c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init1 (0950297C)](all03umd-teams.md#team-0950297c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init2 (0950251C)](all03umd-teams.md#team-0950251c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init3 (095020BC)](all03umd-teams.md#team-095020bc).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Init4 (0950D50C)](all03umd-teams.md#team-0950d50c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Lasher1 (0950D16C)](all03umd-teams.md#team-0950d16c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Lasher2 (0950D03C)](all03umd-teams.md#team-0950d03c).
9. Enable and reset applicable timers for [TE_TD_DestroyTeam2 (0B5A1D6C)](#trigger-0b5a1d6c).
10. Disable [TE_TD_DestroyTeam1 (0B5A1E5C)](#trigger-0b5a1e5c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14057, Events line 14435, Actions line 14813.

<a id="trigger-095f27cc"></a>

### 129. TC_ChangeHouse - 095F27CC

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TC_Group_Alive_TD (0C4F3D5C)](#trigger-0c4f3d5c); enable from [TD_Becomes_AD_2 (096BABFC)](#trigger-096babfc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 48 (Confed_Gone) is clear.
2. 0 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 48 (Confed_Gone) at [Check_Confed_Status (097E4A8C)](#trigger-097e4a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 6 (country/type ARABS; placed owner Arabs).
2. Enable and reset applicable timers for [TC_ChangeGuard1 (095EA27C)](#trigger-095ea27c).
3. Disable [TC_ChangeHouse (095F27CC)](#trigger-095f27cc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14058, Events line 14436, Actions line 14814.

<a id="trigger-097a408c"></a>

### 130. TE_Becomes_TF_2 - 097A408C

Owner reference: PPTF Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_Becomes_TF_1 (097A417C)](#trigger-097a417c).

Incoming activation links: enable from [TE_Becomes_TF_1 (097A417C)](#trigger-097a417c).

Attached scope: tag definitions 097A4F1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Lasher3 (095B706C)](all03umd-teams.md#team-095b706c).
2. Create/recruit team [TEAM_TF_Virus (095B8A4C)](all03umd-teams.md#team-095b8a4c).
3. Create/recruit team [TEAM_TF_Yuri1 (095B859C)](all03umd-teams.md#team-095b859c).
4. Create/recruit team [TEAM_TF_Yuri2 (095B813C)](all03umd-teams.md#team-095b813c).
5. Disable [TE_Becomes_TF_2 (097A408C)](#trigger-097a408c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14059, Events line 14437, Actions line 14815.

<a id="trigger-0b42cf3c"></a>

### 131. TC_Becomes_TF_1 - 0B42CF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_TF_DestroyTeam2 (0B42D3BC)](#trigger-0b42d3bc).

Incoming activation links: enable from [TC_TF_DestroyTeam2 (0B42D3BC)](#trigger-0b42d3bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Gatt1 (095B536C)](all03umd-teams.md#team-095b536c).
2. Create/recruit team [TEAM_TF_Gatt2 (095B6D7C)](all03umd-teams.md#team-095b6d7c).
3. Create/recruit team [TEAM_TF_Init1 (095B68CC)](all03umd-teams.md#team-095b68cc).
4. Create/recruit team [TEAM_TF_Init2 (095B606C)](all03umd-teams.md#team-095b606c).
5. Create/recruit team [TEAM_TF_Init3 (095B7C0C)](all03umd-teams.md#team-095b7c0c).
6. Create/recruit team [TEAM_TF_Init4 (095B782C)](all03umd-teams.md#team-095b782c).
7. Create/recruit team [TEAM_TF_Lasher1 (095B740C)](all03umd-teams.md#team-095b740c).
8. Create/recruit team [TEAM_TF_Lasher2 (0BA5FC1C)](all03umd-teams.md#team-0ba5fc1c).
9. Enable and reset applicable timers for [TC_Becomes_TF_2 (0B42CE4C)](#trigger-0b42ce4c).
10. Disable [TC_Becomes_TF_1 (0B42CF3C)](#trigger-0b42cf3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14060, Events line 14438, Actions line 14816.

<a id="trigger-0c08e59c"></a>

### 132. TD_TF_DestroyTeam2 - 0C08E59C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_TF_DestroyTeam1 (0C08E68C)](#trigger-0c08e68c).

Incoming activation links: enable from [TD_TF_DestroyTeam1 (0C08E68C)](#trigger-0c08e68c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher3 (09661CDC)](all03umd-teams.md#team-09661cdc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Virus (0967699C)](all03umd-teams.md#team-0967699c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Yuri1 (09668E2C)](all03umd-teams.md#team-09668e2c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Yuri2 (0966897C)](all03umd-teams.md#team-0966897c).
5. Enable and reset applicable timers for [TD_Becomes_TF_1 (0C08E4AC)](#trigger-0c08e4ac).
6. Disable [TD_TF_DestroyTeam2 (0C08E59C)](#trigger-0c08e59c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14061, Events line 14439, Actions line 14817.

<a id="trigger-0d5b5e5c"></a>

### 133. Frnch_Become_TB1 - 0D5B5E5C

Owner reference: Nod. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [French_ChangeGuard2 (0BB0037C)](#trigger-0bb0037c).

Incoming activation links: enable from [French_Change_House (0BB3B28C)](#trigger-0bb3b28c); enable from [French_ChangeGuard2 (0BB0037C)](#trigger-0bb0037c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TB_Gatt1 (0AFC2DCC)](all03umd-teams.md#team-0afc2dcc).
2. Create/recruit team [TEAM_TB_Gatt2 (0AFC322C)](all03umd-teams.md#team-0afc322c).
3. Create/recruit team [TEAM_TB_Init1 (0AFC4EFC)](all03umd-teams.md#team-0afc4efc).
4. Create/recruit team [TEAM_TB_Init2 (0AFC4CBC)](all03umd-teams.md#team-0afc4cbc).
5. Create/recruit team [TEAM_TB_Init3 (0AFC4A7C)](all03umd-teams.md#team-0afc4a7c).
6. Create/recruit team [TEAM_TB_Init4 (0AFC483C)](all03umd-teams.md#team-0afc483c).
7. Create/recruit team [TEAM_TB_Lasher1 (0AFC45FC)](all03umd-teams.md#team-0afc45fc).
8. Create/recruit team [TEAM_TB_Lasher2 (0AFC43BC)](all03umd-teams.md#team-0afc43bc).
9. Enable and reset applicable timers for [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c).
10. Disable [Frnch_Become_TB1 (0D5B5E5C)](#trigger-0d5b5e5c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14062, Events line 14440, Actions line 14818.

<a id="trigger-0c776f3c"></a>

### 134. TA_Becomes_TB_1 - 0C776F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TA_TB_DestroyTeam2 (0C772F3C)](#trigger-0c772f3c).

Incoming activation links: enable from [TA_TB_DestroyTeam2 (0C772F3C)](#trigger-0c772f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TB_Gatt1 (0AFC2DCC)](all03umd-teams.md#team-0afc2dcc).
2. Create/recruit team [TEAM_TB_Gatt2 (0AFC322C)](all03umd-teams.md#team-0afc322c).
3. Create/recruit team [TEAM_TB_Init1 (0AFC4EFC)](all03umd-teams.md#team-0afc4efc).
4. Create/recruit team [TEAM_TB_Init2 (0AFC4CBC)](all03umd-teams.md#team-0afc4cbc).
5. Create/recruit team [TEAM_TB_Init3 (0AFC4A7C)](all03umd-teams.md#team-0afc4a7c).
6. Create/recruit team [TEAM_TB_Init4 (0AFC483C)](all03umd-teams.md#team-0afc483c).
7. Create/recruit team [TEAM_TB_Lasher1 (0AFC45FC)](all03umd-teams.md#team-0afc45fc).
8. Create/recruit team [TEAM_TB_Lasher2 (0AFC43BC)](all03umd-teams.md#team-0afc43bc).
9. Enable and reset applicable timers for [TA_Becomes_TB_2 (0C77277C)](#trigger-0c77277c).
10. Disable [TA_Becomes_TB_1 (0C776F3C)](#trigger-0c776f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14063, Events line 14441, Actions line 14819.

<a id="trigger-0955b49c"></a>

### 135. TD_TE_DestroyTeam2 - 0955B49C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_TE_DestroyTeam1 (0955B58C)](#trigger-0955b58c).

Incoming activation links: enable from [TD_TE_DestroyTeam1 (0955B58C)](#trigger-0955b58c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher3 (09661CDC)](all03umd-teams.md#team-09661cdc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Virus (0967699C)](all03umd-teams.md#team-0967699c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Yuri1 (09668E2C)](all03umd-teams.md#team-09668e2c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Yuri2 (0966897C)](all03umd-teams.md#team-0966897c).
5. Enable and reset applicable timers for [TD_Becomes_TE_1 (0955B3AC)](#trigger-0955b3ac).
6. Disable [TD_TE_DestroyTeam2 (0955B49C)](#trigger-0955b49c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14064, Events line 14442, Actions line 14820.

<a id="trigger-096a593c"></a>

### 136. TB_Becomes_TA_1 - 096A593C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_Change_House (096AE6FC)](#trigger-096ae6fc).

Incoming activation links: enable from [TB_Change_Guard2 (0952630C)](#trigger-0952630c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TA_Gatt1 (0DA10A7C)](all03umd-teams.md#team-0da10a7c).
2. Create/recruit team [TEAM_TA_Gatt2 (0DA1083C)](all03umd-teams.md#team-0da1083c).
3. Create/recruit team [TEAM_TA_Init1 (0DA105FC)](all03umd-teams.md#team-0da105fc).
4. Create/recruit team [TEAM_TA_Init2 (0DA103BC)](all03umd-teams.md#team-0da103bc).
5. Create/recruit team [TEAM_TA_Init3 (0DA1017C)](all03umd-teams.md#team-0da1017c).
6. Create/recruit team [TEAM_TA_Init4 (0DA11DEC)](all03umd-teams.md#team-0da11dec).
7. Create/recruit team [TEAM_TA_Lasher1 (0DA0F32C)](all03umd-teams.md#team-0da0f32c).
8. Create/recruit team [TEAM_TA_Lasher2 (0DA10EFC)](all03umd-teams.md#team-0da10efc).
9. Enable and reset applicable timers for [TB_Becomes_TA_2 (096A2B2C)](#trigger-096a2b2c).
10. Disable [TB_Becomes_TA_1 (096A593C)](#trigger-096a593c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14065, Events line 14443, Actions line 14821.

<a id="trigger-0975c66c"></a>

### 137. TF_Becomes_TC2 - 0975C66C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Becomes_TC1 (0975CE6C)](#trigger-0975ce6c).

Incoming activation links: enable from [TF_Becomes_TC1 (0975CE6C)](#trigger-0975ce6c).

Attached scope: tag definitions 0975A62C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Lasher3 (06C6E0FC)](all03umd-teams.md#team-06c6e0fc).
2. Create/recruit team [TEAM_TC_Virus (06C6B95C)](all03umd-teams.md#team-06c6b95c).
3. Create/recruit team [TEAM_TC_Yuri1 (06C6B53C)](all03umd-teams.md#team-06c6b53c).
4. Create/recruit team [TEAM_TC_Yuri2 (06C6B11C)](all03umd-teams.md#team-06c6b11c).
5. Enable and reset applicable timers for [Backup1_ChangeHouse (09565CCC)](#trigger-09565ccc).
6. Disable [TF_Becomes_TC2 (0975C66C)](#trigger-0975c66c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14066, Events line 14444, Actions line 14822.

<a id="trigger-06c878cc"></a>

### 138. TE_Becomes_TC_1 - 06C878CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_TC_DestroyTeam2 (06C879BC)](#trigger-06c879bc).

Incoming activation links: enable from [TE_TC_DestroyTeam2 (06C879BC)](#trigger-06c879bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Gatt1 (0967471C)](all03umd-teams.md#team-0967471c).
2. Create/recruit team [TEAM_TC_Gatt2 (09675EFC)](all03umd-teams.md#team-09675efc).
3. Create/recruit team [TEAM_TC_Init1 (09675B1C)](all03umd-teams.md#team-09675b1c).
4. Create/recruit team [TEAM_TC_Init2 (096756FC)](all03umd-teams.md#team-096756fc).
5. Create/recruit team [TEAM_TC_Init3 (0BE0D2BC)](all03umd-teams.md#team-0be0d2bc).
6. Create/recruit team [TEAM_TC_Init4 (06C6FEFC)](all03umd-teams.md#team-06c6fefc).
7. Create/recruit team [TEAM_TC_Lasher1 (06C6F82C)](all03umd-teams.md#team-06c6f82c).
8. Create/recruit team [TEAM_TC_Lasher2 (06C6F21C)](all03umd-teams.md#team-06c6f21c).
9. Enable and reset applicable timers for [TE_Becomes_TC_2 (06C877DC)](#trigger-06c877dc).
10. Disable [TE_Becomes_TC_1 (06C878CC)](#trigger-06c878cc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14067, Events line 14445, Actions line 14823.

<a id="trigger-09490c7c"></a>

### 139. TD_TC_DestroyTeam2 - 09490C7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_TC_DestroyTeam1 (09490D6C)](#trigger-09490d6c).

Incoming activation links: enable from [TD_TC_DestroyTeam1 (09490D6C)](#trigger-09490d6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher3 (09661CDC)](all03umd-teams.md#team-09661cdc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Virus (0967699C)](all03umd-teams.md#team-0967699c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Yuri1 (09668E2C)](all03umd-teams.md#team-09668e2c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Yuri2 (0966897C)](all03umd-teams.md#team-0966897c).
5. Enable and reset applicable timers for [TD_Becomes_TC_1 (09490B8C)](#trigger-09490b8c).
6. Disable [TD_TC_DestroyTeam2 (09490C7C)](#trigger-09490c7c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14068, Events line 14446, Actions line 14824.

<a id="trigger-0960617c"></a>

### 140. TF_Becomes_TD_1 - 0960617C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_TD_DestroyTeam2 (0960626C)](#trigger-0960626c).

Incoming activation links: enable from [TF_TD_DestroyTeam2 (0960626C)](#trigger-0960626c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TD_Gatt1 (096586BC)](all03umd-teams.md#team-096586bc).
2. Create/recruit team [TEAM_TD_Gatt2 (09650B4C)](all03umd-teams.md#team-09650b4c).
3. Create/recruit team [TEAM_TD_Init1 (0967732C)](all03umd-teams.md#team-0967732c).
4. Create/recruit team [TEAM_TD_Init2 (0967092C)](all03umd-teams.md#team-0967092c).
5. Create/recruit team [TEAM_TD_Init3 (0967047C)](all03umd-teams.md#team-0967047c).
6. Create/recruit team [TEAM_TD_Init4 (0967028C)](all03umd-teams.md#team-0967028c).
7. Create/recruit team [TEAM_TD_Lasher1 (09663E5C)](all03umd-teams.md#team-09663e5c).
8. Create/recruit team [TEAM_TD_Lasher2 (096639AC)](all03umd-teams.md#team-096639ac).
9. Enable and reset applicable timers for [TF_Becomes_TD_2 (0960608C)](#trigger-0960608c).
10. Disable [TF_Becomes_TD_1 (0960617C)](#trigger-0960617c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14069, Events line 14447, Actions line 14825.

<a id="trigger-0b5a1d6c"></a>

### 141. TE_TD_DestroyTeam2 - 0B5A1D6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_TD_DestroyTeam1 (0B5A1E5C)](#trigger-0b5a1e5c).

Incoming activation links: enable from [TE_TD_DestroyTeam1 (0B5A1E5C)](#trigger-0b5a1e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Lasher3 (0950F66C)](all03umd-teams.md#team-0950f66c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Virus (0950F20C)](all03umd-teams.md#team-0950f20c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Yuri1 (0950EC8C)](all03umd-teams.md#team-0950ec8c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TE_Yuri2 (0950E65C)](all03umd-teams.md#team-0950e65c).
5. Enable and reset applicable timers for [TE_Becomes_TD_1 (0B5BE03C)](#trigger-0b5be03c).
6. Disable [TE_TD_DestroyTeam2 (0B5A1D6C)](#trigger-0b5a1d6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14070, Events line 14448, Actions line 14826.

<a id="trigger-095ea27c"></a>

### 142. TC_ChangeGuard1 - 095EA27C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_ChangeHouse (095F27CC)](#trigger-095f27cc).

Incoming activation links: enable from [TC_ChangeHouse (095F27CC)](#trigger-095f27cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Gatt1 (0967471C)](all03umd-teams.md#team-0967471c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Gatt2 (09675EFC)](all03umd-teams.md#team-09675efc).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init1 (09675B1C)](all03umd-teams.md#team-09675b1c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init2 (096756FC)](all03umd-teams.md#team-096756fc).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init3 (0BE0D2BC)](all03umd-teams.md#team-0be0d2bc).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init4 (06C6FEFC)](all03umd-teams.md#team-06c6fefc).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Lasher1 (06C6F82C)](all03umd-teams.md#team-06c6f82c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Lasher2 (06C6F21C)](all03umd-teams.md#team-06c6f21c).
9. Enable and reset applicable timers for [TC_ChangeGuard2 (095EB71C)](#trigger-095eb71c).
10. Disable [TC_ChangeGuard1 (095EA27C)](#trigger-095ea27c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14071, Events line 14449, Actions line 14827.

<a id="trigger-0b42ce4c"></a>

### 143. TC_Becomes_TF_2 - 0B42CE4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_Becomes_TF_1 (0B42CF3C)](#trigger-0b42cf3c).

Incoming activation links: enable from [TC_Becomes_TF_1 (0B42CF3C)](#trigger-0b42cf3c).

Attached scope: tag definitions 0BD4483C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Lasher3 (095B706C)](all03umd-teams.md#team-095b706c).
2. Create/recruit team [TEAM_TF_Virus (095B8A4C)](all03umd-teams.md#team-095b8a4c).
3. Create/recruit team [TEAM_TF_Yuri1 (095B859C)](all03umd-teams.md#team-095b859c).
4. Create/recruit team [TEAM_TF_Yuri2 (095B813C)](all03umd-teams.md#team-095b813c).
5. Disable [TC_Becomes_TF_2 (0B42CE4C)](#trigger-0b42ce4c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14072, Events line 14450, Actions line 14828.

<a id="trigger-0c08e4ac"></a>

### 144. TD_Becomes_TF_1 - 0C08E4AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_TF_DestroyTeam2 (0C08E59C)](#trigger-0c08e59c).

Incoming activation links: enable from [TD_TF_DestroyTeam2 (0C08E59C)](#trigger-0c08e59c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Gatt1 (095B536C)](all03umd-teams.md#team-095b536c).
2. Create/recruit team [TEAM_TF_Gatt2 (095B6D7C)](all03umd-teams.md#team-095b6d7c).
3. Create/recruit team [TEAM_TF_Init1 (095B68CC)](all03umd-teams.md#team-095b68cc).
4. Create/recruit team [TEAM_TF_Init2 (095B606C)](all03umd-teams.md#team-095b606c).
5. Create/recruit team [TEAM_TF_Init3 (095B7C0C)](all03umd-teams.md#team-095b7c0c).
6. Create/recruit team [TEAM_TF_Init4 (095B782C)](all03umd-teams.md#team-095b782c).
7. Create/recruit team [TEAM_TF_Lasher1 (095B740C)](all03umd-teams.md#team-095b740c).
8. Create/recruit team [TEAM_TF_Lasher2 (0BA5FC1C)](all03umd-teams.md#team-0ba5fc1c).
9. Enable and reset applicable timers for [TD_Becomes_TF_2 (0C08E3BC)](#trigger-0c08e3bc).
10. Disable [TD_Becomes_TF_1 (0C08E4AC)](#trigger-0c08e4ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14073, Events line 14451, Actions line 14829.

<a id="trigger-0bb0037c"></a>

### 145. French_ChangeGuard2 - 0BB0037C

Owner reference: French. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [French_ChangeGuard1 (0BB3DBEC)](#trigger-0bb3dbec).

Incoming activation links: enable from [French_ChangeGuard1 (0BB3DBEC)](#trigger-0bb3dbec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Lasher3 (095CB13C)](all03umd-teams.md#team-095cb13c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Virus (095C813C)](all03umd-teams.md#team-095c813c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Yuri1 (095C913C)](all03umd-teams.md#team-095c913c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Yuri2 (095CA1AC)](all03umd-teams.md#team-095ca1ac).
5. Enable and reset applicable timers for [Frnch_Become_TB1 (0D5B5E5C)](#trigger-0d5b5e5c).
6. Disable [French_ChangeGuard2 (0BB0037C)](#trigger-0bb0037c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14074, Events line 14452, Actions line 14830.

<a id="trigger-0d5b6d9c"></a>

### 146. Frnch_Become_TB2 - 0D5B6D9C

Owner reference: Nod. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Frnch_Become_TB1 (0D5B5E5C)](#trigger-0d5b5e5c).

Incoming activation links: enable from [Frnch_Become_TB1 (0D5B5E5C)](#trigger-0d5b5e5c).

Attached scope: tag definitions 0BB3DCDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TB_Lasher3 (0AFC417C)](all03umd-teams.md#team-0afc417c).
2. Create/recruit team [TEAM_TB_Virus (0AFC372C)](all03umd-teams.md#team-0afc372c).
3. Create/recruit team [TEAM_TB_Yuri1 (0AFC34EC)](all03umd-teams.md#team-0afc34ec).
4. Create/recruit team [TEAM_TB_Yuri2 (0AFC59AC)](all03umd-teams.md#team-0afc59ac).
5. Set local flag 43 (PPTF_Gone).
6. Disable [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14075, Events line 14453, Actions line 14831.

<a id="trigger-0c77277c"></a>

### 147. TA_Becomes_TB_2 - 0C77277C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TA_Becomes_TB_1 (0C776F3C)](#trigger-0c776f3c).

Incoming activation links: enable from [TA_Becomes_TB_1 (0C776F3C)](#trigger-0c776f3c).

Attached scope: tag definitions 0C53B04C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TB_Lasher3 (0AFC417C)](all03umd-teams.md#team-0afc417c).
2. Create/recruit team [TEAM_TB_Virus (0AFC372C)](all03umd-teams.md#team-0afc372c).
3. Create/recruit team [TEAM_TB_Yuri1 (0AFC34EC)](all03umd-teams.md#team-0afc34ec).
4. Create/recruit team [TEAM_TB_Yuri2 (0AFC59AC)](all03umd-teams.md#team-0afc59ac).
5. Disable [TA_Becomes_TB_2 (0C77277C)](#trigger-0c77277c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14076, Events line 14454, Actions line 14832.

<a id="trigger-0955b3ac"></a>

### 148. TD_Becomes_TE_1 - 0955B3AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_TE_DestroyTeam2 (0955B49C)](#trigger-0955b49c).

Incoming activation links: enable from [TD_TE_DestroyTeam2 (0955B49C)](#trigger-0955b49c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TE_Gatt1 (0C0B821C)](all03umd-teams.md#team-0c0b821c).
2. Create/recruit team [TEAM_TE_Gatt2 (09502E2C)](all03umd-teams.md#team-09502e2c).
3. Create/recruit team [TEAM_TE_Init1 (0950297C)](all03umd-teams.md#team-0950297c).
4. Create/recruit team [TEAM_TE_Init2 (0950251C)](all03umd-teams.md#team-0950251c).
5. Create/recruit team [TEAM_TE_Init3 (095020BC)](all03umd-teams.md#team-095020bc).
6. Create/recruit team [TEAM_TE_Init4 (0950D50C)](all03umd-teams.md#team-0950d50c).
7. Create/recruit team [TEAM_TE_Lasher1 (0950D16C)](all03umd-teams.md#team-0950d16c).
8. Create/recruit team [TEAM_TE_Lasher2 (0950D03C)](all03umd-teams.md#team-0950d03c).
9. Enable and reset applicable timers for [TD_Becomes_TE_2 (0955B2BC)](#trigger-0955b2bc).
10. Disable [TD_Becomes_TE_1 (0955B3AC)](#trigger-0955b3ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14077, Events line 14455, Actions line 14833.

<a id="trigger-096a2b2c"></a>

### 149. TB_Becomes_TA_2 - 096A2B2C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_Becomes_TA_1 (096A593C)](#trigger-096a593c).

Incoming activation links: enable from [TB_Becomes_TA_1 (096A593C)](#trigger-096a593c).

Attached scope: tag definitions 0D4512BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TA_Lasher3 (0DA10CBC)](all03umd-teams.md#team-0da10cbc).
2. Create/recruit team [TEAM_TA_Virus1 (0DA1172C)](all03umd-teams.md#team-0da1172c).
3. Create/recruit team [TEAM_TA_Yuri1 (0DA11BAC)](all03umd-teams.md#team-0da11bac).
4. Create/recruit team [TEAM_TA_Yuri2 (0DA1196C)](all03umd-teams.md#team-0da1196c).
5. Enable and reset applicable timers for [French_Change_House (0BB3B28C)](#trigger-0bb3b28c).
6. Disable [TB_Becomes_TA_2 (096A2B2C)](#trigger-096a2b2c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14078, Events line 14456, Actions line 14834.

<a id="trigger-06c877dc"></a>

### 150. TE_Becomes_TC_2 - 06C877DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_Becomes_TC_1 (06C878CC)](#trigger-06c878cc).

Incoming activation links: enable from [TE_Becomes_TC_1 (06C878CC)](#trigger-06c878cc).

Attached scope: tag definitions 06C87B9C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Lasher3 (06C6E0FC)](all03umd-teams.md#team-06c6e0fc).
2. Create/recruit team [TEAM_TC_Virus (06C6B95C)](all03umd-teams.md#team-06c6b95c).
3. Create/recruit team [TEAM_TC_Yuri1 (06C6B53C)](all03umd-teams.md#team-06c6b53c).
4. Create/recruit team [TEAM_TC_Yuri2 (06C6B11C)](all03umd-teams.md#team-06c6b11c).
5. Disable [TE_Becomes_TC_2 (06C877DC)](#trigger-06c877dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14079, Events line 14457, Actions line 14835.

<a id="trigger-09490b8c"></a>

### 151. TD_Becomes_TC_1 - 09490B8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_TC_DestroyTeam2 (09490C7C)](#trigger-09490c7c).

Incoming activation links: enable from [TD_TC_DestroyTeam2 (09490C7C)](#trigger-09490c7c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Gatt1 (0967471C)](all03umd-teams.md#team-0967471c).
2. Create/recruit team [TEAM_TC_Gatt2 (09675EFC)](all03umd-teams.md#team-09675efc).
3. Create/recruit team [TEAM_TC_Init1 (09675B1C)](all03umd-teams.md#team-09675b1c).
4. Create/recruit team [TEAM_TC_Init2 (096756FC)](all03umd-teams.md#team-096756fc).
5. Create/recruit team [TEAM_TC_Init3 (0BE0D2BC)](all03umd-teams.md#team-0be0d2bc).
6. Create/recruit team [TEAM_TC_Init4 (06C6FEFC)](all03umd-teams.md#team-06c6fefc).
7. Create/recruit team [TEAM_TC_Lasher1 (06C6F82C)](all03umd-teams.md#team-06c6f82c).
8. Create/recruit team [TEAM_TC_Lasher2 (06C6F21C)](all03umd-teams.md#team-06c6f21c).
9. Enable and reset applicable timers for [TD_Becomes_TC_2 (09490A9C)](#trigger-09490a9c).
10. Disable [TD_Becomes_TC_1 (09490B8C)](#trigger-09490b8c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14080, Events line 14458, Actions line 14836.

<a id="trigger-0960608c"></a>

### 152. TF_Becomes_TD_2 - 0960608C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Becomes_TD_1 (0960617C)](#trigger-0960617c).

Incoming activation links: enable from [TF_Becomes_TD_1 (0960617C)](#trigger-0960617c).

Attached scope: tag definitions 09604D1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TD_Lasher3 (09661CDC)](all03umd-teams.md#team-09661cdc).
2. Create/recruit team [TEAM_TD_Virus (0967699C)](all03umd-teams.md#team-0967699c).
3. Create/recruit team [TEAM_TD_Yuri1 (09668E2C)](all03umd-teams.md#team-09668e2c).
4. Create/recruit team [TEAM_TD_Yuri2 (0966897C)](all03umd-teams.md#team-0966897c).
5. Disable [TF_Becomes_TD_2 (0960608C)](#trigger-0960608c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14081, Events line 14459, Actions line 14837.

<a id="trigger-0b5be03c"></a>

### 153. TE_Becomes_TD_1 - 0B5BE03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_TD_DestroyTeam2 (0B5A1D6C)](#trigger-0b5a1d6c).

Incoming activation links: enable from [TE_TD_DestroyTeam2 (0B5A1D6C)](#trigger-0b5a1d6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TD_Gatt1 (096586BC)](all03umd-teams.md#team-096586bc).
2. Create/recruit team [TEAM_TD_Gatt2 (09650B4C)](all03umd-teams.md#team-09650b4c).
3. Create/recruit team [TEAM_TD_Init1 (0967732C)](all03umd-teams.md#team-0967732c).
4. Create/recruit team [TEAM_TD_Init2 (0967092C)](all03umd-teams.md#team-0967092c).
5. Create/recruit team [TEAM_TD_Init3 (0967047C)](all03umd-teams.md#team-0967047c).
6. Create/recruit team [TEAM_TD_Init4 (0967028C)](all03umd-teams.md#team-0967028c).
7. Create/recruit team [TEAM_TD_Lasher1 (09663E5C)](all03umd-teams.md#team-09663e5c).
8. Create/recruit team [TEAM_TD_Lasher2 (096639AC)](all03umd-teams.md#team-096639ac).
9. Enable and reset applicable timers for [TE_Becomes_TD_2 (0B5B803C)](#trigger-0b5b803c).
10. Disable [TE_Becomes_TD_1 (0B5BE03C)](#trigger-0b5be03c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14082, Events line 14460, Actions line 14838.

<a id="trigger-095eb71c"></a>

### 154. TC_ChangeGuard2 - 095EB71C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_ChangeGuard1 (095EA27C)](#trigger-095ea27c).

Incoming activation links: enable from [TC_ChangeGuard1 (095EA27C)](#trigger-095ea27c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Lasher3 (06C6E0FC)](all03umd-teams.md#team-06c6e0fc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Virus (06C6B95C)](all03umd-teams.md#team-06c6b95c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Yuri1 (06C6B53C)](all03umd-teams.md#team-06c6b53c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Yuri2 (06C6B11C)](all03umd-teams.md#team-06c6b11c).
5. Enable and reset applicable timers for [TC_Becomes_TD1 (095FCA8C)](#trigger-095fca8c).
6. Disable [TC_ChangeGuard2 (095EB71C)](#trigger-095eb71c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14083, Events line 14461, Actions line 14839.

<a id="trigger-0c08e3bc"></a>

### 155. TD_Becomes_TF_2 - 0C08E3BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_Becomes_TF_1 (0C08E4AC)](#trigger-0c08e4ac).

Incoming activation links: enable from [TD_Becomes_TF_1 (0C08E4AC)](#trigger-0c08e4ac).

Attached scope: tag definitions 0C08E77C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Lasher3 (095B706C)](all03umd-teams.md#team-095b706c).
2. Create/recruit team [TEAM_TF_Virus (095B8A4C)](all03umd-teams.md#team-095b8a4c).
3. Create/recruit team [TEAM_TF_Yuri1 (095B859C)](all03umd-teams.md#team-095b859c).
4. Create/recruit team [TEAM_TF_Yuri2 (095B813C)](all03umd-teams.md#team-095b813c).
5. Disable [TD_Becomes_TF_2 (0C08E3BC)](#trigger-0c08e3bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14084, Events line 14462, Actions line 14840.

<a id="trigger-0bb3dbec"></a>

### 156. French_ChangeGuard1 - 0BB3DBEC

Owner reference: French. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [French_Change_House (0BB3B28C)](#trigger-0bb3b28c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Gatt1 (0950E09C)](all03umd-teams.md#team-0950e09c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Gatt2 (095A805C)](all03umd-teams.md#team-095a805c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Init1 (095AA06C)](all03umd-teams.md#team-095aa06c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Init2 (095AD13C)](all03umd-teams.md#team-095ad13c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Init3 (095AF13C)](all03umd-teams.md#team-095af13c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Init4 (095AB13C)](all03umd-teams.md#team-095ab13c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Lasher1 (0951303C)](all03umd-teams.md#team-0951303c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_French_Lasher2 (095CF8EC)](all03umd-teams.md#team-095cf8ec).
9. Enable and reset applicable timers for [French_ChangeGuard2 (0BB0037C)](#trigger-0bb0037c).
10. Disable [French_ChangeGuard1 (0BB3DBEC)](#trigger-0bb3dbec).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14085, Events line 14463, Actions line 14841.

<a id="trigger-0955b2bc"></a>

### 157. TD_Becomes_TE_2 - 0955B2BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_Becomes_TE_1 (0955B3AC)](#trigger-0955b3ac).

Incoming activation links: enable from [TD_Becomes_TE_1 (0955B3AC)](#trigger-0955b3ac).

Attached scope: tag definitions 0955B67C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TE_Lasher3 (0950F66C)](all03umd-teams.md#team-0950f66c).
2. Create/recruit team [TEAM_TE_Virus (0950F20C)](all03umd-teams.md#team-0950f20c).
3. Create/recruit team [TEAM_TE_Yuri1 (0950EC8C)](all03umd-teams.md#team-0950ec8c).
4. Create/recruit team [TEAM_TE_Yuri2 (0950E65C)](all03umd-teams.md#team-0950e65c).
5. Disable [TD_Becomes_TE_2 (0955B2BC)](#trigger-0955b2bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14086, Events line 14464, Actions line 14842.

<a id="trigger-09490a9c"></a>

### 158. TD_Becomes_TC_2 - 09490A9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_Becomes_TC_1 (09490B8C)](#trigger-09490b8c).

Incoming activation links: enable from [TD_Becomes_TC_1 (09490B8C)](#trigger-09490b8c).

Attached scope: tag definitions 09490E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Lasher3 (06C6E0FC)](all03umd-teams.md#team-06c6e0fc).
2. Create/recruit team [TEAM_TC_Virus (06C6B95C)](all03umd-teams.md#team-06c6b95c).
3. Create/recruit team [TEAM_TC_Yuri1 (06C6B53C)](all03umd-teams.md#team-06c6b53c).
4. Create/recruit team [TEAM_TC_Yuri2 (06C6B11C)](all03umd-teams.md#team-06c6b11c).
5. Disable [TD_Becomes_TC_2 (09490A9C)](#trigger-09490a9c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14087, Events line 14465, Actions line 14843.

<a id="trigger-0b5b803c"></a>

### 159. TE_Becomes_TD_2 - 0B5B803C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TE_Becomes_TD_1 (0B5BE03C)](#trigger-0b5be03c).

Incoming activation links: enable from [TE_Becomes_TD_1 (0B5BE03C)](#trigger-0b5be03c).

Attached scope: tag definitions 0B5B424C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TD_Lasher3 (09661CDC)](all03umd-teams.md#team-09661cdc).
2. Create/recruit team [TEAM_TD_Virus (0967699C)](all03umd-teams.md#team-0967699c).
3. Create/recruit team [TEAM_TD_Yuri1 (09668E2C)](all03umd-teams.md#team-09668e2c).
4. Create/recruit team [TEAM_TD_Yuri2 (0966897C)](all03umd-teams.md#team-0966897c).
5. Disable [TE_Becomes_TD_2 (0B5B803C)](#trigger-0b5b803c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14088, Events line 14466, Actions line 14844.

<a id="trigger-095fca8c"></a>

### 160. TC_Becomes_TD1 - 095FCA8C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_ChangeGuard2 (095EB71C)](#trigger-095eb71c).

Incoming activation links: enable from [TC_ChangeGuard2 (095EB71C)](#trigger-095eb71c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TD_Gatt1 (096586BC)](all03umd-teams.md#team-096586bc).
2. Create/recruit team [TEAM_TD_Gatt2 (09650B4C)](all03umd-teams.md#team-09650b4c).
3. Create/recruit team [TEAM_TD_Init1 (0967732C)](all03umd-teams.md#team-0967732c).
4. Create/recruit team [TEAM_TD_Init2 (0967092C)](all03umd-teams.md#team-0967092c).
5. Create/recruit team [TEAM_TD_Init3 (0967047C)](all03umd-teams.md#team-0967047c).
6. Create/recruit team [TEAM_TD_Init4 (0967028C)](all03umd-teams.md#team-0967028c).
7. Create/recruit team [TEAM_TD_Lasher1 (09663E5C)](all03umd-teams.md#team-09663e5c).
8. Create/recruit team [TEAM_TD_Lasher2 (096639AC)](all03umd-teams.md#team-096639ac).
9. Enable and reset applicable timers for [TC_Becomes_TD2 (095FDF3C)](#trigger-095fdf3c).
10. Disable [TC_Becomes_TD1 (095FCA8C)](#trigger-095fca8c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14089, Events line 14467, Actions line 14845.

<a id="trigger-095fdf3c"></a>

### 161. TC_Becomes_TD2 - 095FDF3C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_Becomes_TD1 (095FCA8C)](#trigger-095fca8c).

Incoming activation links: enable from [TC_Becomes_TD1 (095FCA8C)](#trigger-095fca8c).

Attached scope: tag definitions 0A9A518C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TD_Lasher3 (09661CDC)](all03umd-teams.md#team-09661cdc).
2. Create/recruit team [TEAM_TD_Virus (0967699C)](all03umd-teams.md#team-0967699c).
3. Create/recruit team [TEAM_TD_Yuri1 (09668E2C)](all03umd-teams.md#team-09668e2c).
4. Create/recruit team [TEAM_TD_Yuri2 (0966897C)](all03umd-teams.md#team-0966897c).
5. Enable and reset applicable timers for [TF_Change_House (0975ABAC)](#trigger-0975abac).
6. Disable [TC_Becomes_TD2 (095FDF3C)](#trigger-095fdf3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14090, Events line 14468, Actions line 14846.

<a id="trigger-093162bc"></a>

### 162. Reveal_Yuri_Base - 093162BC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09314A3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 365 (cell 49, 90).
2. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14091, Events line 14469, Actions line 14847.

<a id="trigger-09266c6c"></a>

### 163. Reveal_Other_Stuff - 09266C6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09261F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 367 (cell 109, 123).
2. Reveal terrain around waypoint 368 (cell 96, 92).
3. Reveal terrain around waypoint 309 (cell 124, 130).
4. Reveal terrain around waypoint 32 (cell 120, 151).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14092, Events line 14470, Actions line 14848.

<a id="trigger-0951b56c"></a>

### 164. Create_PP1_Team_A - 0951B56C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0951BDDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TA_Gatt1 (0DA10A7C)](all03umd-teams.md#team-0da10a7c).
2. Create/recruit team [TEAM_TA_Gatt2 (0DA1083C)](all03umd-teams.md#team-0da1083c).
3. Create/recruit team [TEAM_TA_Init1 (0DA105FC)](all03umd-teams.md#team-0da105fc).
4. Create/recruit team [TEAM_TA_Init2 (0DA103BC)](all03umd-teams.md#team-0da103bc).
5. Create/recruit team [TEAM_TA_Init3 (0DA1017C)](all03umd-teams.md#team-0da1017c).
6. Create/recruit team [TEAM_TA_Init4 (0DA11DEC)](all03umd-teams.md#team-0da11dec).
7. Create/recruit team [TEAM_TA_Lasher1 (0DA0F32C)](all03umd-teams.md#team-0da0f32c).
8. Create/recruit team [TEAM_TA_Lasher2 (0DA10EFC)](all03umd-teams.md#team-0da10efc).
9. Create/recruit team [TEAM_TA_Lasher3 (0DA10CBC)](all03umd-teams.md#team-0da10cbc).
10. Create/recruit team [TEAM_TA_Virus1 (0DA1172C)](all03umd-teams.md#team-0da1172c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14093, Events line 14471, Actions line 14849.

<a id="trigger-0941226c"></a>

### 165. Create_PP2_Team_A - 0941226C

Owner reference: Nod. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09411B9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TB_Gatt1 (0AFC2DCC)](all03umd-teams.md#team-0afc2dcc).
2. Create/recruit team [TEAM_TB_Gatt2 (0AFC322C)](all03umd-teams.md#team-0afc322c).
3. Create/recruit team [TEAM_TB_Init1 (0AFC4EFC)](all03umd-teams.md#team-0afc4efc).
4. Create/recruit team [TEAM_TB_Init2 (0AFC4CBC)](all03umd-teams.md#team-0afc4cbc).
5. Create/recruit team [TEAM_TB_Init3 (0AFC4A7C)](all03umd-teams.md#team-0afc4a7c).
6. Create/recruit team [TEAM_TB_Init4 (0AFC483C)](all03umd-teams.md#team-0afc483c).
7. Create/recruit team [TEAM_TB_Lasher1 (0AFC45FC)](all03umd-teams.md#team-0afc45fc).
8. Create/recruit team [TEAM_TB_Lasher2 (0AFC43BC)](all03umd-teams.md#team-0afc43bc).
9. Create/recruit team [TEAM_TB_Lasher3 (0AFC417C)](all03umd-teams.md#team-0afc417c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14094, Events line 14472, Actions line 14850.

<a id="trigger-09406c5c"></a>

### 166. Yuri_Attack_AA - 09406C5C

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroy_Old_Teams2 (095B721C)](#trigger-095b721c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 4 (Nuked_PPAA) is clear.

Flag writers in this mission: set local flag 4 (Nuked_PPAA) at [Nuke_AA_True (094F5C2C)](#trigger-094f5c2c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_AA_Gatt1 (0BA253BC)](all03umd-teams.md#team-0ba253bc).
2. Create/recruit team [TEAM_AA_Gatt2 (0BA2528C)](all03umd-teams.md#team-0ba2528c).
3. Create/recruit team [TEAM_AA_Init1 (0BA2515C)](all03umd-teams.md#team-0ba2515c).
4. Create/recruit team [TEAM_AA_Init2 (0BA26EFC)](all03umd-teams.md#team-0ba26efc).
5. Create/recruit team [TEAM_AA_Init3 (0BA26DCC)](all03umd-teams.md#team-0ba26dcc).
6. Create/recruit team [TEAM_AA_Lasher1 (0BA26B6C)](all03umd-teams.md#team-0ba26b6c).
7. Create/recruit team [TEAM_AA_Lasher2 (0BA26A3C)](all03umd-teams.md#team-0ba26a3c).
8. Enable and reset applicable timers for [Yuri_Attack_AA_2 (094BCBFC)](#trigger-094bcbfc).
9. Disable [Yuri_Attack_AA (09406C5C)](#trigger-09406c5c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14095, Events line 14473, Actions line 14851.

<a id="trigger-094bcbfc"></a>

### 167. Yuri_Attack_AA_2 - 094BCBFC

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Yuri_Attack_AA (09406C5C)](#trigger-09406c5c).

Incoming activation links: enable from [Yuri_Attack_AA (09406C5C)](#trigger-09406c5c).

Attached scope: tag definitions 0940695C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_AA_Virus (0BA2657C)](all03umd-teams.md#team-0ba2657c).
2. Create/recruit team [TEAM_AA_Yuri1 (0BA267DC)](all03umd-teams.md#team-0ba267dc).
3. Create/recruit team [TEAM_AA_Yuri2 (0BA266AC)](all03umd-teams.md#team-0ba266ac).
4. Create/recruit team [TEAM_AA_Lasher3 (0BA2690C)](all03umd-teams.md#team-0ba2690c).
5. Create/recruit team [TEAM_AA_Init4 (0BA26C9C)](all03umd-teams.md#team-0ba26c9c).
6. Enable and reset applicable timers for [TB_Change_House (096AE6FC)](#trigger-096ae6fc).
7. Disable [Yuri_Attack_AA_2 (094BCBFC)](#trigger-094bcbfc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14096, Events line 14474, Actions line 14852.

<a id="trigger-0a9a417c"></a>

### 168. Send_AA_Engineer - 0A9A417C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec).

Attached scope: tag definitions 0A97BA0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (Engineer_AA) is set.
2. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_AA_Engineer (0BA3C0EC)](all03umd-teams.md#team-0ba3c0ec) at waypoint 468 (cell 103, 61).
2. Disable [Send_AA_Engineer (0A9A417C)](#trigger-0a9a417c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14097, Events line 14475, Actions line 14853.

<a id="trigger-093beedc"></a>

### 169. PlantAA_Gone - 093BEEDC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Plant_AA (0D663A4C)](#trigger-0d663a4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRAA exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 0 (PlantAA_Gone).
2. Clear local flag 5 (Player_Owns_AA).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_AA (0945ABBC)](#trigger-0945abbc).
5. Disable [Yuri_Takes_AA (0945934C)](#trigger-0945934c).
6. Disable [PlantAA_Gone (093BEEDC)](#trigger-093beedc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14098, Events line 14476, Actions line 14854.

<a id="trigger-0945abbc"></a>

### 170. Player_Takes_AA - 0945ABBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_AA (0945934C)](#trigger-0945934c).

Incoming activation links: enable from [Yuri_Takes_AA (0945934C)](#trigger-0945934c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 5 (Player_Owns_AA).
2. Enable and reset applicable timers for [Yuri_Takes_AA (0945934C)](#trigger-0945934c).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_AA (0945ABBC)](#trigger-0945abbc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14099, Events line 14477, Actions line 14855.

<a id="trigger-0945934c"></a>

### 171. Yuri_Takes_AA - 0945934C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PlantAA_Gone (093BEEDC)](#trigger-093beedc).

Incoming activation links: enable from [Player_Takes_AA (0945ABBC)](#trigger-0945abbc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 5 (Player_Owns_AA).
2. Enable and reset applicable timers for [Player_Takes_AA (0945ABBC)](#trigger-0945abbc).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_AA (0945934C)](#trigger-0945934c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14100, Events line 14478, Actions line 14856.

<a id="trigger-093be2fc"></a>

### 172. PlantAB_Gone - 093BE2FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Plant_AB (0D664F3C)](#trigger-0d664f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRAB exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 1 (PlantAB_Gone).
2. Clear local flag 25 (Player_Owns_AB).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_AB (0CF8179C)](#trigger-0cf8179c).
5. Disable [Yuri_Takes_AB (0CF8110C)](#trigger-0cf8110c).
6. Disable [PlantAB_Gone (093BE2FC)](#trigger-093be2fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14101, Events line 14479, Actions line 14857.

<a id="trigger-0cf8179c"></a>

### 173. Player_Takes_AB - 0CF8179C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PlantAB_Gone (093BE2FC)](#trigger-093be2fc).

Incoming activation links: enable from [Yuri_Takes_AB (0CF8110C)](#trigger-0cf8110c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 25 (Player_Owns_AB).
2. Enable and reset applicable timers for [Yuri_Takes_AB (0CF8110C)](#trigger-0cf8110c).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_AB (0CF8179C)](#trigger-0cf8179c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14102, Events line 14480, Actions line 14858.

<a id="trigger-0cf8110c"></a>

### 174. Yuri_Takes_AB - 0CF8110C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Takes_AB (0CF8179C)](#trigger-0cf8179c).

Incoming activation links: enable from [Player_Takes_AB (0CF8179C)](#trigger-0cf8179c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 25 (Player_Owns_AB).
2. Enable and reset applicable timers for [Player_Takes_AB (0CF8179C)](#trigger-0cf8179c).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_AB (0CF8110C)](#trigger-0cf8110c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14103, Events line 14481, Actions line 14859.

<a id="trigger-093bfddc"></a>

### 175. PlantAC_Gone - 093BFDDC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Plant_AC (0D664C0C)](#trigger-0d664c0c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRAC exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 2 (PlantAC_Gone).
2. Clear local flag 26 (Player_Owns_AC).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_AC (06B5EC6C)](#trigger-06b5ec6c).
5. Disable [Yuri_Takes_AC (06B5D04C)](#trigger-06b5d04c).
6. Disable [PlantAC_Gone (093BFDDC)](#trigger-093bfddc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14104, Events line 14482, Actions line 14860.

<a id="trigger-06b5ec6c"></a>

### 176. Player_Takes_AC - 06B5EC6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_AC (06B5D04C)](#trigger-06b5d04c).

Incoming activation links: enable from [Yuri_Takes_AC (06B5D04C)](#trigger-06b5d04c).

Attached scope: CAPOWRAC, owner Special, cell (158, 115), tag 093BFADC, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 26 (Player_Owns_AC).
2. Enable and reset applicable timers for [Yuri_Takes_AC (06B5D04C)](#trigger-06b5d04c).
3. Enable and reset applicable timers for [PlantAC_Reinforce (0B67F2DC)](#trigger-0b67f2dc).
4. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
5. Disable [Player_Takes_AC (06B5EC6C)](#trigger-06b5ec6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14105, Events line 14483, Actions line 14861.

<a id="trigger-06b5d04c"></a>

### 177. Yuri_Takes_AC - 06B5D04C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PlantAC_Gone (093BFDDC)](#trigger-093bfddc).

Incoming activation links: enable from [Player_Takes_AC (06B5EC6C)](#trigger-06b5ec6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 26 (Player_Owns_AC).
2. Enable and reset applicable timers for [Player_Takes_AC (06B5EC6C)](#trigger-06b5ec6c).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_AC (06B5D04C)](#trigger-06b5d04c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14106, Events line 14484, Actions line 14862.

<a id="trigger-0b67f2dc"></a>

### 178. PlantAC_Reinforce - 0B67F2DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_AC (06B5EC6C)](#trigger-06b5ec6c); enable from [PlantAC_Reinforce (0B67F2DC)](#trigger-0b67f2dc).

Attached scope: tag definitions 0B67D92C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Grizzly_BD (0B6D745C)](all03umd-teams.md#team-0b6d745c).
2. Supply reinforcement team [TEAM_Grizzly_BE (0B6D6B5C)](all03umd-teams.md#team-0b6d6b5c).
3. Supply reinforcement team [TEAM_Grizzly_BF (0B6D66EC)](all03umd-teams.md#team-0b6d66ec).
4. Supply reinforcement team [TEAM_Mirage_BH (0B6D3EBC)](all03umd-teams.md#team-0b6d3ebc).
5. Supply reinforcement team [TEAM_IFV_BG (04F3226C)](all03umd-teams.md#team-04f3226c).
6. Supply reinforcement team [TEAM_IFV_BI (04F33C8C)](all03umd-teams.md#team-04f33c8c).
7. Enable and reset applicable timers for [PlantAC_Reinforce (0B67F2DC)](#trigger-0b67f2dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14107, Events line 14485, Actions line 14863.

<a id="trigger-093bf8fc"></a>

### 179. PlantAD_Gone - 093BF8FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Plant_AD (0D6648DC)](#trigger-0d6648dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRAD exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 3 (PlantAD_Gone).
2. Clear local flag 27 (Player_Owns_AD).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_AD (094D82BC)](#trigger-094d82bc).
5. Disable [Yuri_Takes_AD (094D9C5C)](#trigger-094d9c5c).
6. Disable [PlantAD_Gone (093BF8FC)](#trigger-093bf8fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14108, Events line 14486, Actions line 14864.

<a id="trigger-094d82bc"></a>

### 180. Player_Takes_AD - 094D82BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PlantAD_Gone (093BF8FC)](#trigger-093bf8fc).

Incoming activation links: enable from [Yuri_Takes_AD (094D9C5C)](#trigger-094d9c5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 27 (Player_Owns_AD).
2. Enable and reset applicable timers for [Yuri_Takes_AD (094D9C5C)](#trigger-094d9c5c).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_AD (094D82BC)](#trigger-094d82bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14109, Events line 14487, Actions line 14865.

<a id="trigger-094d9c5c"></a>

### 181. Yuri_Takes_AD - 094D9C5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Takes_AD (094D82BC)](#trigger-094d82bc).

Incoming activation links: enable from [Player_Takes_AD (094D82BC)](#trigger-094d82bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 27 (Player_Owns_AD).
2. Enable and reset applicable timers for [Player_Takes_AD (094D82BC)](#trigger-094d82bc).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_AD (094D9C5C)](#trigger-094d9c5c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14110, Events line 14488, Actions line 14866.

<a id="trigger-0be5f3bc"></a>

### 182. Create_PP3_Team_A - 0BE5F3BC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BE5B8FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Gatt1 (0967471C)](all03umd-teams.md#team-0967471c).
2. Create/recruit team [TEAM_TC_Gatt2 (09675EFC)](all03umd-teams.md#team-09675efc).
3. Create/recruit team [TEAM_TC_Init1 (09675B1C)](all03umd-teams.md#team-09675b1c).
4. Create/recruit team [TEAM_TC_Init2 (096756FC)](all03umd-teams.md#team-096756fc).
5. Create/recruit team [TEAM_TC_Init3 (0BE0D2BC)](all03umd-teams.md#team-0be0d2bc).
6. Create/recruit team [TEAM_TC_Init4 (06C6FEFC)](all03umd-teams.md#team-06c6fefc).
7. Create/recruit team [TEAM_TC_Lasher1 (06C6F82C)](all03umd-teams.md#team-06c6f82c).
8. Create/recruit team [TEAM_TC_Lasher2 (06C6F21C)](all03umd-teams.md#team-06c6f21c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14111, Events line 14489, Actions line 14867.

<a id="trigger-0be7a4ec"></a>

### 183. Deploy_AB_GI - 0BE7A4EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BE85B6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_AB_GI (0BE791BC)](all03umd-teams.md#team-0be791bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14112, Events line 14490, Actions line 14868.

<a id="trigger-0dd2eadc"></a>

### 184. TA_Change_House - 0DD2EADC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 5 (Player_Owns_AA) is set.

Flag writers in this mission: clear local flag 5 (Player_Owns_AA) at [PlantAA_Gone (093BEEDC)](#trigger-093beedc); set local flag 5 (Player_Owns_AA) at [Player_Takes_AA (0945ABBC)](#trigger-0945abbc); clear local flag 5 (Player_Owns_AA) at [Yuri_Takes_AA (0945934C)](#trigger-0945934c); set local flag 5 (Player_Owns_AA) at [Set_Locals (06B6627C)](#trigger-06b6627c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 5 (country/type AFRICANS; placed owner Africans).
2. Enable and reset applicable timers for [Destroy_Old_Teams1 (095B18AC)](#trigger-095b18ac).
3. Disable [TA_Change_House (0DD2EADC)](#trigger-0dd2eadc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14113, Events line 14491, Actions line 14869.

<a id="trigger-095b18ac"></a>

### 185. Destroy_Old_Teams1 - 095B18AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TA_Change_House (0DD2EADC)](#trigger-0dd2eadc).

Incoming activation links: enable from [TA_Change_House (0DD2EADC)](#trigger-0dd2eadc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Gatt1 (0DA10A7C)](all03umd-teams.md#team-0da10a7c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Gatt2 (0DA1083C)](all03umd-teams.md#team-0da1083c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Init2 (0DA103BC)](all03umd-teams.md#team-0da103bc).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Init3 (0DA1017C)](all03umd-teams.md#team-0da1017c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Init4 (0DA11DEC)](all03umd-teams.md#team-0da11dec).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Lasher1 (0DA0F32C)](all03umd-teams.md#team-0da0f32c).
7. Enable and reset applicable timers for [Destroy_Old_Teams2 (095B721C)](#trigger-095b721c).
8. Disable [Destroy_Old_Teams1 (095B18AC)](#trigger-095b18ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14114, Events line 14492, Actions line 14870.

<a id="trigger-095b721c"></a>

### 186. Destroy_Old_Teams2 - 095B721C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Destroy_Old_Teams1 (095B18AC)](#trigger-095b18ac).

Incoming activation links: enable from [Destroy_Old_Teams1 (095B18AC)](#trigger-095b18ac).

Attached scope: tag definitions 0D44DBEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Virus1 (0DA1172C)](all03umd-teams.md#team-0da1172c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Yuri1 (0DA11BAC)](all03umd-teams.md#team-0da11bac).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Yuri2 (0DA1196C)](all03umd-teams.md#team-0da1196c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Lasher3 (0DA10CBC)](all03umd-teams.md#team-0da10cbc).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Init1 (0DA105FC)](all03umd-teams.md#team-0da105fc).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TA_Lasher2 (0DA10EFC)](all03umd-teams.md#team-0da10efc).
7. Enable and reset applicable timers for [Yuri_Attack_AA (09406C5C)](#trigger-09406c5c).
8. Disable [Destroy_Old_Teams2 (095B721C)](#trigger-095b721c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14115, Events line 14493, Actions line 14871.

<a id="trigger-09519f3c"></a>

### 187. Found_Reinforcements - 09519F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0951961C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14116, Events line 14494, Actions line 14872.

<a id="trigger-06afbc7c"></a>

### 188. Dog1 - 06AFBC7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06AFB70C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Dog1 (06AF927C)](all03umd-teams.md#team-06af927c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14117, Events line 14495, Actions line 14873.

<a id="trigger-06afa57c"></a>

### 189. Dog2 - 06AFA57C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B2C9EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Dog2 (0954011C)](all03umd-teams.md#team-0954011c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14118, Events line 14496, Actions line 14874.

<a id="trigger-06afa26c"></a>

### 190. Dog3 - 06AFA26C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B2C90C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Dog3 (06AFE7DC)](all03umd-teams.md#team-06afe7dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14119, Events line 14497, Actions line 14875.

<a id="trigger-06af289c"></a>

### 191. Dog4 - 06AF289C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B2AE8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Dog4 (0B24C21C)](all03umd-teams.md#team-0b24c21c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14120, Events line 14498, Actions line 14876.

<a id="trigger-06b0990c"></a>

### 192. Kill_GI - 06B0990C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B0939C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 24 (Kill_GI_HJ) is set.
2. local flag 23 (Kill_GI_HI) is set.
3. local flag 22 (Kill_GI_HH) is set.
4. local flag 21 (Kill_GI_HG) is set.
5. local flag 20 (Kill_GI_HF) is set.
6. local flag 19 (Kill_GI) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Kill_GI_Again (06B0CCCC)](#trigger-06b0cccc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14121, Events line 14499, Actions line 14877.

<a id="trigger-06b0cccc"></a>

### 193. Kill_GI_Again - 06B0CCCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kill_GI (06B0990C)](#trigger-06b0990c).

Attached scope: tag definitions 06B0C8FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 4 (country/type BRITISH; placed owner British).
2. Destroy all of: owner selector 4 (country/type BRITISH; placed owner British).
3. Disable [Kill_GI_Again (06B0CCCC)](#trigger-06b0cccc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14122, Events line 14500, Actions line 14878.

<a id="trigger-04e56d6c"></a>

### 194. Dog5 - 04E56D6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04E5785C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Dog5 (04E50EFC)](all03umd-teams.md#team-04e50efc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14123, Events line 14501, Actions line 14879.

<a id="trigger-09492e0c"></a>

### 195. Dog6 - 09492E0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0949289C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Dog6 (0948FEFC)](all03umd-teams.md#team-0948fefc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14124, Events line 14502, Actions line 14880.

<a id="trigger-0cf7b65c"></a>

### 196. Create_PP1_Team_B - 0CF7B65C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CF7BCDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TA_Yuri1 (0DA11BAC)](all03umd-teams.md#team-0da11bac).
2. Create/recruit team [TEAM_TA_Yuri2 (0DA1196C)](all03umd-teams.md#team-0da1196c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14125, Events line 14503, Actions line 14881.

<a id="trigger-06b6627c"></a>

### 197. Set_Locals - 06B6627C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B6766C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 5 (Player_Owns_AA).
2. Set local flag 25 (Player_Owns_AB).
3. Set local flag 27 (Player_Owns_AD).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14126, Events line 14504, Actions line 14882.

<a id="trigger-094e203c"></a>

### 198. PlantTA_Gone - 094E203C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Plant_TA (0D6645AC)](#trigger-0d6645ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRTA exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 32 (PlantTA_Gone).
2. Clear local flag 28 (Player_Owns_TA).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_TA (094E3ACC)](#trigger-094e3acc).
5. Disable [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c).
6. Disable [PlantTA_Gone (094E203C)](#trigger-094e203c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14127, Events line 14505, Actions line 14883.

<a id="trigger-094e3acc"></a>

### 199. Player_Takes_TA - 094E3ACC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c).

Incoming activation links: enable from [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 28 (Player_Owns_TA).
2. Enable and reset applicable timers for [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c).
3. Enable and reset applicable timers for [TD_ChangeHouse (0BFE86FC)](#trigger-0bfe86fc).
4. Enable and reset applicable timers for [TA_Snipers (0BC69E1C)](#trigger-0bc69e1c).
5. Enable and reset applicable timers for [TA_Engineers (0BBFFDAC)](#trigger-0bbffdac).
6. Enable and reset applicable timers for [Yuri_Taunt_1 (0B2AF2FC)](#trigger-0b2af2fc).
7. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
8. Disable [Player_Takes_TA (094E3ACC)](#trigger-094e3acc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14128, Events line 14506, Actions line 14884.

<a id="trigger-094e3c3c"></a>

### 200. Yuri_Takes_TA - 094E3C3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PlantTA_Gone (094E203C)](#trigger-094e203c).

Incoming activation links: enable from [Player_Takes_TA (094E3ACC)](#trigger-094e3acc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 28 (Player_Owns_TA).
2. Enable and reset applicable timers for [Player_Takes_TA (094E3ACC)](#trigger-094e3acc).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14129, Events line 14507, Actions line 14885.

<a id="trigger-0bfe86fc"></a>

### 201. TD_ChangeHouse - 0BFE86FC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TA (094E3ACC)](#trigger-094e3acc); enable from [Player_Takes_TF (0C13364C)](#trigger-0c13364c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 47 (Arabs_Gone) is clear.
2. 15 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 47 (Arabs_Gone) at [Check_Arab_Status (097E43EC)](#trigger-097e43ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 16 (country/type PPAD COUNTRY; placed owner PPADHouse).
2. Enable and reset applicable timers for [TD_Change_Guard1 (0BF5E44C)](#trigger-0bf5e44c).
3. Disable [TD_ChangeHouse (0BFE86FC)](#trigger-0bfe86fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14130, Events line 14508, Actions line 14886.

<a id="trigger-0bc69e1c"></a>

### 202. TA_Snipers - 0BC69E1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TA (094E3ACC)](#trigger-094e3acc).

Attached scope: tag definitions 0BC69BDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TA_Snipers (0BC6D60C)](all03umd-teams.md#team-0bc6d60c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14131, Events line 14509, Actions line 14887.

<a id="trigger-0bbffdac"></a>

### 203. TA_Engineers - 0BBFFDAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TA (094E3ACC)](#trigger-094e3acc).

Attached scope: tag definitions 0BBFFCCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Yuri_TB_TA_Engineer (0B8E2DCC)](all03umd-teams.md#team-0b8e2dcc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14132, Events line 14510, Actions line 14888.

<a id="trigger-0b2af2fc"></a>

### 204. Yuri_Taunt_1 - 0B2AF2FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TA (094E3ACC)](#trigger-094e3acc); enable from [Player_Takes_TB (094D681C)](#trigger-094d681c); enable from [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec); enable from [Player_Takes_TD (0B30121C)](#trigger-0b30121c); enable from [Player_Takes_TE (045C109C)](#trigger-045c109c); enable from [Player_Takes_TF (0C13364C)](#trigger-0c13364c).

Attached scope: tag definitions 0B2AB22C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 14 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA3_YuriTaunt.
2. Enable and reset applicable timers for [Sniper_hint (0967142C)](#trigger-0967142c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14133, Events line 14511, Actions line 14889.

<a id="trigger-0bf5e44c"></a>

### 205. TD_Change_Guard1 - 0BF5E44C

Owner reference: PPAD Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_ChangeHouse (0BFE86FC)](#trigger-0bfe86fc).

Incoming activation links: enable from [TD_ChangeHouse (0BFE86FC)](#trigger-0bfe86fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Gatt1 (096586BC)](all03umd-teams.md#team-096586bc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Gatt2 (09650B4C)](all03umd-teams.md#team-09650b4c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init1 (0967732C)](all03umd-teams.md#team-0967732c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init2 (0967092C)](all03umd-teams.md#team-0967092c).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init3 (0967047C)](all03umd-teams.md#team-0967047c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Init4 (0967028C)](all03umd-teams.md#team-0967028c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher1 (09663E5C)](all03umd-teams.md#team-09663e5c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher2 (096639AC)](all03umd-teams.md#team-096639ac).
9. Enable and reset applicable timers for [TD_Change_Guard2 (0BF582FC)](#trigger-0bf582fc).
10. Disable [TD_Change_Guard1 (0BF5E44C)](#trigger-0bf5e44c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14134, Events line 14512, Actions line 14890.

<a id="trigger-0967142c"></a>

### 206. Sniper_hint - 0967142C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Taunt_1 (0B2AF2FC)](#trigger-0b2af2fc).

Attached scope: tag definitions 09672F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA3_EvaSnipersComing.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14135, Events line 14513, Actions line 14891.

<a id="trigger-0bf582fc"></a>

### 207. TD_Change_Guard2 - 0BF582FC

Owner reference: PPAD Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_Change_Guard1 (0BF5E44C)](#trigger-0bf5e44c).

Incoming activation links: enable from [TD_Change_Guard1 (0BF5E44C)](#trigger-0bf5e44c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Lasher3 (09661CDC)](all03umd-teams.md#team-09661cdc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Virus (0967699C)](all03umd-teams.md#team-0967699c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Yuri1 (09668E2C)](all03umd-teams.md#team-09668e2c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TD_Yuri2 (0966897C)](all03umd-teams.md#team-0966897c).
5. Enable and reset applicable timers for [TD_Becomes_AD_1 (096AB93C)](#trigger-096ab93c).
6. Disable [TD_Change_Guard2 (0BF582FC)](#trigger-0bf582fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14136, Events line 14514, Actions line 14892.

<a id="trigger-096ab93c"></a>

### 208. TD_Becomes_AD_1 - 096AB93C

Owner reference: PPAD Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_Change_Guard2 (0BF582FC)](#trigger-0bf582fc).

Incoming activation links: enable from [TD_Change_Guard2 (0BF582FC)](#trigger-0bf582fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_AD_Gatt1 (096AAEFC)](all03umd-teams.md#team-096aaefc).
2. Create/recruit team [TEAM_AD_Gatt2 (096AA94C)](all03umd-teams.md#team-096aa94c).
3. Create/recruit team [TEAM_AD_Init1 (096AA3FC)](all03umd-teams.md#team-096aa3fc).
4. Create/recruit team [TEAM_AD_Init2 (096AEC8C)](all03umd-teams.md#team-096aec8c).
5. Create/recruit team [TEAM_AD_Init3 (096AE8EC)](all03umd-teams.md#team-096ae8ec).
6. Create/recruit team [TEAM_AD_Init4 (096A9BDC)](all03umd-teams.md#team-096a9bdc).
7. Create/recruit team [TEAM_AD_Lasher1 (096A97BC)](all03umd-teams.md#team-096a97bc).
8. Create/recruit team [TEAM_AD_Lasher2 (096A939C)](all03umd-teams.md#team-096a939c).
9. Enable and reset applicable timers for [TD_Becomes_AD_2 (096BABFC)](#trigger-096babfc).
10. Disable [TD_Becomes_AD_1 (096AB93C)](#trigger-096ab93c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14137, Events line 14515, Actions line 14893.

<a id="trigger-096babfc"></a>

### 209. TD_Becomes_AD_2 - 096BABFC

Owner reference: PPAD Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TD_Becomes_AD_1 (096AB93C)](#trigger-096ab93c).

Incoming activation links: enable from [TD_Becomes_AD_1 (096AB93C)](#trigger-096ab93c).

Attached scope: tag definitions 0967EAEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_AD_Lasher3 (096A926C)](all03umd-teams.md#team-096a926c).
2. Create/recruit team [TEAM_AD_Virus (096B678C)](all03umd-teams.md#team-096b678c).
3. Create/recruit team [TEAM_AD_Yuri1 (096B1C0C)](all03umd-teams.md#team-096b1c0c).
4. Create/recruit team [TEAM_AD_Yuri2 (096B62DC)](all03umd-teams.md#team-096b62dc).
5. Enable and reset applicable timers for [TC_ChangeHouse (095F27CC)](#trigger-095f27cc).
6. Disable [TD_Becomes_AD_2 (096BABFC)](#trigger-096babfc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14138, Events line 14516, Actions line 14894.

<a id="trigger-094fc1dc"></a>

### 210. PlantA1_Gone - 094FC1DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Power Plant (GAPOWR), owner Americans, cell (125, 138), tag 094FDEAC, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 36 (PlantA1_Gone).
2. Disable [PlantA1_Gone (094FC1DC)](#trigger-094fc1dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14139, Events line 14517, Actions line 14895.

<a id="trigger-045ed3ac"></a>

### 211. PlantA2_Gone - 045ED3AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Power Plant (GAPOWR), owner Americans, cell (123, 139), tag 045EEA4C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 37 (PlantA2_Gone).
2. Disable [PlantA2_Gone (045ED3AC)](#trigger-045ed3ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14140, Events line 14518, Actions line 14896.

<a id="trigger-06b3ed3c"></a>

### 212. PlantTB_Gone - 06B3ED3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Plant_TB (0D66427C)](#trigger-0d66427c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRTB exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 33 (PlantTB_Gone).
2. Clear local flag 29 (Player_Owns_TB).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_TB (094D681C)](#trigger-094d681c).
5. Disable [Yuri_Takes_TB (094D672C)](#trigger-094d672c).
6. Disable [PlantTB_Gone (06B3ED3C)](#trigger-06b3ed3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14141, Events line 14519, Actions line 14897.

<a id="trigger-094d681c"></a>

### 213. Player_Takes_TB - 094D681C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PlantTB_Gone (06B3ED3C)](#trigger-06b3ed3c).

Incoming activation links: enable from [Yuri_Takes_TB (094D672C)](#trigger-094d672c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 29 (Player_Owns_TB).
2. Enable and reset applicable timers for [Yuri_Takes_TB (094D672C)](#trigger-094d672c).
3. Enable and reset applicable timers for [TB_Snipers (0BC6D8BC)](#trigger-0bc6d8bc).
4. Enable and reset applicable timers for [TB_Engineers (0BC5FF3C)](#trigger-0bc5ff3c).
5. Enable and reset applicable timers for [Yuri_Taunt_1 (0B2AF2FC)](#trigger-0b2af2fc).
6. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
7. Disable [Player_Takes_TB (094D681C)](#trigger-094d681c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14142, Events line 14520, Actions line 14898.

<a id="trigger-094d672c"></a>

### 214. Yuri_Takes_TB - 094D672C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Takes_TB (094D681C)](#trigger-094d681c).

Incoming activation links: enable from [Player_Takes_TB (094D681C)](#trigger-094d681c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 29 (Player_Owns_TB).
2. Enable and reset applicable timers for [Player_Takes_TB (094D681C)](#trigger-094d681c).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_TB (094D672C)](#trigger-094d672c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14143, Events line 14521, Actions line 14899.

<a id="trigger-0bc6d8bc"></a>

### 215. TB_Snipers - 0BC6D8BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TB (094D681C)](#trigger-094d681c).

Attached scope: tag definitions 0BC6BB9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TB_Snipers (0BC6AC4C)](all03umd-teams.md#team-0bc6ac4c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14144, Events line 14522, Actions line 14900.

<a id="trigger-0bc5ff3c"></a>

### 216. TB_Engineers - 0BC5FF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TB (094D681C)](#trigger-094d681c).

Attached scope: tag definitions 0BC5FA4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Yuri_FA_TB_Engineer (0BBFB72C)](all03umd-teams.md#team-0bbfb72c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14145, Events line 14523, Actions line 14901.

<a id="trigger-094f204c"></a>

### 217. PlantTC_Gone - 094F204C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Plant_TC (0D665F3C)](#trigger-0d665f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRTC exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 34 (PlantTC_Gone).
2. Clear local flag 30 (Player_Owns_TC).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec).
5. Disable [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc).
6. Disable [PlantTC_Gone (094F204C)](#trigger-094f204c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14146, Events line 14524, Actions line 14902.

<a id="trigger-06bda0ec"></a>

### 218. Player_Takes_TC - 06BDA0EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc).

Incoming activation links: enable from [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 30 (Player_Owns_TC).
2. Enable and reset applicable timers for [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc).
3. Enable and reset applicable timers for [TA_Change_House (0DD2EADC)](#trigger-0dd2eadc).
4. Enable and reset applicable timers for [Send_AA_Engineer (0A9A417C)](#trigger-0a9a417c).
5. Enable and reset applicable timers for [TC_Snipers (095D49DC)](#trigger-095d49dc).
6. Enable and reset applicable timers for [TC_Engineers (095D421C)](#trigger-095d421c).
7. Enable and reset applicable timers for [Yuri_Taunt_1 (0B2AF2FC)](#trigger-0b2af2fc).
8. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
9. Disable [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14147, Events line 14525, Actions line 14903.

<a id="trigger-06bda1dc"></a>

### 219. Yuri_Takes_TC - 06BDA1DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PlantTC_Gone (094F204C)](#trigger-094f204c).

Incoming activation links: enable from [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 30 (Player_Owns_TC).
2. Enable and reset applicable timers for [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14148, Events line 14526, Actions line 14904.

<a id="trigger-095d49dc"></a>

### 220. TC_Snipers - 095D49DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec).

Attached scope: tag definitions 095D448C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TC_Snipers (0954544C)](all03umd-teams.md#team-0954544c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14149, Events line 14527, Actions line 14905.

<a id="trigger-095d421c"></a>

### 221. TC_Engineers - 095D421C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec).

Attached scope: tag definitions 095D413C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TC_Engineer (0C94E2DC)](all03umd-teams.md#team-0c94e2dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14150, Events line 14528, Actions line 14906.

<a id="trigger-0b30790c"></a>

### 222. PlantTD_Gone - 0B30790C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Plant_TD (0D665C0C)](#trigger-0d665c0c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRTD exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 35 (PlantTD_Gone).
2. Clear local flag 31 (Player_Owns_TD).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_TD (0B30121C)](#trigger-0b30121c).
5. Disable [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c).
6. Disable [PlantTD_Gone (0B30790C)](#trigger-0b30790c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14151, Events line 14529, Actions line 14907.

<a id="trigger-0b30121c"></a>

### 223. Player_Takes_TD - 0B30121C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PlantTD_Gone (0B30790C)](#trigger-0b30790c).

Incoming activation links: enable from [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 31 (Player_Owns_TD).
2. Enable and reset applicable timers for [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c).
3. Enable and reset applicable timers for [TB_AB_ChangeHouse (0966845C)](#trigger-0966845c).
4. Enable and reset applicable timers for [TD_Snipers (0B6EAE0C)](#trigger-0b6eae0c).
5. Enable and reset applicable timers for [TD_Engineers (0BF9F64C)](#trigger-0bf9f64c).
6. Enable and reset applicable timers for [Yuri_Taunt_1 (0B2AF2FC)](#trigger-0b2af2fc).
7. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
8. Disable [Player_Takes_TD (0B30121C)](#trigger-0b30121c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14152, Events line 14530, Actions line 14908.

<a id="trigger-0b30112c"></a>

### 224. Yuri_Takes_TD - 0B30112C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Takes_TD (0B30121C)](#trigger-0b30121c).

Incoming activation links: enable from [Player_Takes_TD (0B30121C)](#trigger-0b30121c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 31 (Player_Owns_TD).
2. Enable and reset applicable timers for [Player_Takes_TD (0B30121C)](#trigger-0b30121c).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14153, Events line 14531, Actions line 14909.

<a id="trigger-0966845c"></a>

### 225. TB_AB_ChangeHouse - 0966845C

Owner reference: Nod. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TD (0B30121C)](#trigger-0b30121c); enable from [Player_Takes_TE (045C109C)](#trigger-045c109c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 25 (Player_Owns_AB) is set.
2. 15 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: clear local flag 25 (Player_Owns_AB) at [PlantAB_Gone (093BE2FC)](#trigger-093be2fc); set local flag 25 (Player_Owns_AB) at [Player_Takes_AB (0CF8179C)](#trigger-0cf8179c); clear local flag 25 (Player_Owns_AB) at [Yuri_Takes_AB (0CF8110C)](#trigger-0cf8110c); set local flag 25 (Player_Owns_AB) at [Set_Locals (06B6627C)](#trigger-06b6627c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 3 (country/type GERMANS; placed owner Germans).
2. Enable and reset applicable timers for [TB_Change_AB_1 (09681F3C)](#trigger-09681f3c).
3. Disable [TB_AB_ChangeHouse (0966845C)](#trigger-0966845c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14154, Events line 14532, Actions line 14910.

<a id="trigger-0b6eae0c"></a>

### 226. TD_Snipers - 0B6EAE0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TD (0B30121C)](#trigger-0b30121c).

Attached scope: tag definitions 0B6EAD2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TD_Snipers (0B6EF9BC)](all03umd-teams.md#team-0b6ef9bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14155, Events line 14533, Actions line 14911.

<a id="trigger-0bf9f64c"></a>

### 227. TD_Engineers - 0BF9F64C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TD (0B30121C)](#trigger-0b30121c).

Attached scope: tag definitions 0BF98E1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Yuri_TC_TD_Engineers (0B8DF08C)](all03umd-teams.md#team-0b8df08c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14156, Events line 14534, Actions line 14912.

<a id="trigger-09681f3c"></a>

### 228. TB_Change_AB_1 - 09681F3C

Owner reference: Nod. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_AB_ChangeHouse (0966845C)](#trigger-0966845c).

Incoming activation links: enable from [TB_AB_ChangeHouse (0966845C)](#trigger-0966845c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Gatt1 (0AFC2DCC)](all03umd-teams.md#team-0afc2dcc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Gatt2 (0AFC322C)](all03umd-teams.md#team-0afc322c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Init1 (0AFC4EFC)](all03umd-teams.md#team-0afc4efc).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Init2 (0AFC4CBC)](all03umd-teams.md#team-0afc4cbc).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Init3 (0AFC4A7C)](all03umd-teams.md#team-0afc4a7c).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Init4 (0AFC483C)](all03umd-teams.md#team-0afc483c).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Lasher1 (0AFC45FC)](all03umd-teams.md#team-0afc45fc).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Lasher2 (0AFC43BC)](all03umd-teams.md#team-0afc43bc).
9. Enable and reset applicable timers for [TB_Change_AB_2 (096813FC)](#trigger-096813fc).
10. Disable [TB_Change_AB_1 (09681F3C)](#trigger-09681f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14157, Events line 14535, Actions line 14913.

<a id="trigger-096813fc"></a>

### 229. TB_Change_AB_2 - 096813FC

Owner reference: Nod. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_Change_AB_1 (09681F3C)](#trigger-09681f3c).

Incoming activation links: enable from [TB_Change_AB_1 (09681F3C)](#trigger-09681f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Lasher3 (0AFC417C)](all03umd-teams.md#team-0afc417c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Virus (0AFC372C)](all03umd-teams.md#team-0afc372c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Yuri1 (0AFC34EC)](all03umd-teams.md#team-0afc34ec).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TB_Yuri2 (0AFC59AC)](all03umd-teams.md#team-0afc59ac).
5. Enable and reset applicable timers for [TB_Becomes_AB_1 (0967B85C)](#trigger-0967b85c).
6. Disable [TB_Change_AB_2 (096813FC)](#trigger-096813fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14158, Events line 14536, Actions line 14914.

<a id="trigger-0967b85c"></a>

### 230. TB_Becomes_AB_1 - 0967B85C

Owner reference: Germans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_Change_AB_2 (096813FC)](#trigger-096813fc).

Incoming activation links: enable from [TB_Change_AB_2 (096813FC)](#trigger-096813fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_AB_Gatt1 (0967B39C)](all03umd-teams.md#team-0967b39c).
2. Create/recruit team [TEAM_AB_Gatt2 (0967E61C)](all03umd-teams.md#team-0967e61c).
3. Create/recruit team [TEAM_AB_Init1 (0967FB7C)](all03umd-teams.md#team-0967fb7c).
4. Create/recruit team [TEAM_AB_Init2 (0967F51C)](all03umd-teams.md#team-0967f51c).
5. Create/recruit team [TEAM_AB_Init3 (0966041C)](all03umd-teams.md#team-0966041c).
6. Create/recruit team [TEAM_AB_Init4 (0966954C)](all03umd-teams.md#team-0966954c).
7. Create/recruit team [TEAM_AB_Lasher1 (09683A4C)](all03umd-teams.md#team-09683a4c).
8. Create/recruit team [TEAM_AB_Lasher2 (0968359C)](all03umd-teams.md#team-0968359c).
9. Enable and reset applicable timers for [TB_Becomes_AB_2 (09684AFC)](#trigger-09684afc).
10. Disable [TB_Becomes_AB_1 (0967B85C)](#trigger-0967b85c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14159, Events line 14537, Actions line 14915.

<a id="trigger-09684afc"></a>

### 231. TB_Becomes_AB_2 - 09684AFC

Owner reference: Germans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TB_Becomes_AB_1 (0967B85C)](#trigger-0967b85c).

Incoming activation links: enable from [TB_Becomes_AB_1 (0967B85C)](#trigger-0967b85c).

Attached scope: tag definitions 09669F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_AB_Lasher3 (09685EFC)](all03umd-teams.md#team-09685efc).
2. Create/recruit team [TEAM_AB_Virus (09685ADC)](all03umd-teams.md#team-09685adc).
3. Create/recruit team [TEAM_AB_Yuri1 (096856BC)](all03umd-teams.md#team-096856bc).
4. Create/recruit team [TEAM_AB_Yuri2 (0968529C)](all03umd-teams.md#team-0968529c).
5. Enable and reset applicable timers for [French_Change_House (0BB3B28C)](#trigger-0bb3b28c).
6. Enable and reset applicable timers for [Send_AB_Engineer (0963461C)](#trigger-0963461c).
7. Disable [TB_Becomes_AB_2 (09684AFC)](#trigger-09684afc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14160, Events line 14538, Actions line 14916.

<a id="trigger-0963461c"></a>

### 232. Send_AB_Engineer - 0963461C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TB_Becomes_AB_2 (09684AFC)](#trigger-09684afc).

Attached scope: tag definitions 09635F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_AB_Engineer (095C2E1C)](all03umd-teams.md#team-095c2e1c).
2. Disable [Send_AB_Engineer (0963461C)](#trigger-0963461c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14161, Events line 14539, Actions line 14917.

<a id="trigger-045d673c"></a>

### 233. PlantTE_Gone - 045D673C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Plant_TE (0D6658DC)](#trigger-0d6658dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRTE exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 38 (PlantTE_Gone).
2. Clear local flag 40 (Player_Owns_TE).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_TE (045C109C)](#trigger-045c109c).
5. Disable [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c).
6. Disable [PlantTE_Gone (045D673C)](#trigger-045d673c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14162, Events line 14540, Actions line 14918.

<a id="trigger-045c109c"></a>

### 234. Player_Takes_TE - 045C109C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PlantTE_Gone (045D673C)](#trigger-045d673c).

Incoming activation links: enable from [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 40 (Player_Owns_TE).
2. Enable and reset applicable timers for [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c).
3. Enable and reset applicable timers for [TB_AB_ChangeHouse (0966845C)](#trigger-0966845c).
4. Enable and reset applicable timers for [TE_Snipers (0BCAB56C)](#trigger-0bcab56c).
5. Enable and reset applicable timers for [TE_Engineers (0BC627BC)](#trigger-0bc627bc).
6. Enable and reset applicable timers for [Yuri_Taunt_1 (0B2AF2FC)](#trigger-0b2af2fc).
7. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
8. Disable [Player_Takes_TE (045C109C)](#trigger-045c109c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14163, Events line 14541, Actions line 14919.

<a id="trigger-045c3e3c"></a>

### 235. Yuri_Takes_TE - 045C3E3C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Takes_TE (045C109C)](#trigger-045c109c).

Incoming activation links: enable from [Player_Takes_TE (045C109C)](#trigger-045c109c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 40 (Player_Owns_TE).
2. Enable and reset applicable timers for [Player_Takes_TE (045C109C)](#trigger-045c109c).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14164, Events line 14542, Actions line 14920.

<a id="trigger-0bcab56c"></a>

### 236. TE_Snipers - 0BCAB56C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TE (045C109C)](#trigger-045c109c).

Attached scope: tag definitions 0BCA354C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TE_Snipers (0BCB4A1C)](all03umd-teams.md#team-0bcb4a1c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14165, Events line 14543, Actions line 14921.

<a id="trigger-0bc627bc"></a>

### 237. TE_Engineers - 0BC627BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TE (045C109C)](#trigger-045c109c).

Attached scope: tag definitions 0BC6223C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Yuri_TF_TE_Engineer (0B8E268C)](all03umd-teams.md#team-0b8e268c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14166, Events line 14544, Actions line 14922.

<a id="trigger-0c50d81c"></a>

### 238. Create_PP2_Team_B - 0C50D81C

Owner reference: Nod. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0DD2785C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TB_Virus (0AFC372C)](all03umd-teams.md#team-0afc372c).
2. Create/recruit team [TEAM_TB_Yuri1 (0AFC34EC)](all03umd-teams.md#team-0afc34ec).
3. Create/recruit team [TEAM_TB_Yuri2 (0AFC59AC)](all03umd-teams.md#team-0afc59ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14167, Events line 14545, Actions line 14923.

<a id="trigger-0967d64c"></a>

### 239. Create_PP3_Team_B - 0967D64C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0967CDAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TC_Lasher3 (06C6E0FC)](all03umd-teams.md#team-06c6e0fc).
2. Create/recruit team [TEAM_TC_Virus (06C6B95C)](all03umd-teams.md#team-06c6b95c).
3. Create/recruit team [TEAM_TC_Yuri1 (06C6B53C)](all03umd-teams.md#team-06c6b53c).
4. Create/recruit team [TEAM_TC_Yuri2 (06C6B11C)](all03umd-teams.md#team-06c6b11c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14168, Events line 14546, Actions line 14924.

<a id="trigger-06ae771c"></a>

### 240. Create_PP4_Team_A - 06AE771C

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06AE72AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TD_Gatt1 (096586BC)](all03umd-teams.md#team-096586bc).
2. Create/recruit team [TEAM_TD_Gatt2 (09650B4C)](all03umd-teams.md#team-09650b4c).
3. Create/recruit team [TEAM_TD_Lasher1 (09663E5C)](all03umd-teams.md#team-09663e5c).
4. Create/recruit team [TEAM_TD_Lasher2 (096639AC)](all03umd-teams.md#team-096639ac).
5. Create/recruit team [TEAM_TD_Lasher3 (09661CDC)](all03umd-teams.md#team-09661cdc).
6. Create/recruit team [TEAM_TD_Yuri1 (09668E2C)](all03umd-teams.md#team-09668e2c).
7. Create/recruit team [TEAM_TD_Yuri2 (0966897C)](all03umd-teams.md#team-0966897c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14169, Events line 14547, Actions line 14925.

<a id="trigger-096fcb2c"></a>

### 241. Create_PP5_Team_A - 096FCB2C

Owner reference: GDI. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096FDC0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TE_Gatt1 (0C0B821C)](all03umd-teams.md#team-0c0b821c).
2. Create/recruit team [TEAM_TE_Gatt2 (09502E2C)](all03umd-teams.md#team-09502e2c).
3. Create/recruit team [TEAM_TE_Init1 (0950297C)](all03umd-teams.md#team-0950297c).
4. Create/recruit team [TEAM_TE_Init2 (0950251C)](all03umd-teams.md#team-0950251c).
5. Create/recruit team [TEAM_TE_Init3 (095020BC)](all03umd-teams.md#team-095020bc).
6. Create/recruit team [TEAM_TE_Init4 (0950D50C)](all03umd-teams.md#team-0950d50c).
7. Create/recruit team [TEAM_TE_Lasher1 (0950D16C)](all03umd-teams.md#team-0950d16c).
8. Create/recruit team [TEAM_TE_Lasher2 (0950D03C)](all03umd-teams.md#team-0950d03c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14170, Events line 14548, Actions line 14926.

<a id="trigger-096fdb1c"></a>

### 242. Create_PP5_Team_B - 096FDB1C

Owner reference: GDI. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096F9B2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TE_Lasher3 (0950F66C)](all03umd-teams.md#team-0950f66c).
2. Create/recruit team [TEAM_TE_Virus (0950F20C)](all03umd-teams.md#team-0950f20c).
3. Create/recruit team [TEAM_TE_Yuri1 (0950EC8C)](all03umd-teams.md#team-0950ec8c).
4. Create/recruit team [TEAM_TE_Yuri2 (0950E65C)](all03umd-teams.md#team-0950e65c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14171, Events line 14549, Actions line 14927.

<a id="trigger-0978180c"></a>

### 243. Create_PP6_Team_A - 0978180C

Owner reference: PPTF Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09782C0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Gatt1 (095B536C)](all03umd-teams.md#team-095b536c).
2. Create/recruit team [TEAM_TF_Gatt2 (095B6D7C)](all03umd-teams.md#team-095b6d7c).
3. Create/recruit team [TEAM_TF_Init1 (095B68CC)](all03umd-teams.md#team-095b68cc).
4. Create/recruit team [TEAM_TF_Init2 (095B606C)](all03umd-teams.md#team-095b606c).
5. Create/recruit team [TEAM_TF_Init3 (095B7C0C)](all03umd-teams.md#team-095b7c0c).
6. Create/recruit team [TEAM_TF_Init4 (095B782C)](all03umd-teams.md#team-095b782c).
7. Create/recruit team [TEAM_TE_Lasher1 (0950D16C)](all03umd-teams.md#team-0950d16c).
8. Create/recruit team [TEAM_TF_Lasher2 (0BA5FC1C)](all03umd-teams.md#team-0ba5fc1c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14172, Events line 14550, Actions line 14928.

<a id="trigger-09782b1c"></a>

### 244. Create_PP6_Team_B - 09782B1C

Owner reference: PPTF Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097824DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TF_Lasher3 (095B706C)](all03umd-teams.md#team-095b706c).
2. Create/recruit team [TEAM_TF_Virus (095B8A4C)](all03umd-teams.md#team-095b8a4c).
3. Create/recruit team [TEAM_TF_Yuri1 (095B859C)](all03umd-teams.md#team-095b859c).
4. Create/recruit team [TEAM_TF_Yuri2 (095B813C)](all03umd-teams.md#team-095b813c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14173, Events line 14551, Actions line 14929.

<a id="trigger-0972627c"></a>

### 245. Create_Yuri_BD - 0972627C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097278FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_YuriBD1 (04646B6C)](all03umd-teams.md#team-04646b6c).
2. Create/recruit team [TEAM_YuriBD2 (046465FC)](all03umd-teams.md#team-046465fc).
3. Create/recruit team [TEAM_YuriBD3 (0464781C)](all03umd-teams.md#team-0464781c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14174, Events line 14552, Actions line 14930.

<a id="trigger-0c61dd8c"></a>

### 246. MakeCheer - 0C61DD8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Nuke_Gone (0C61D62C)](#trigger-0c61d62c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14175, Events line 14553, Actions line 14931.

<a id="trigger-0c61d87c"></a>

### 247. WeWin - 0C61D87C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [MakeCheer (0C61DD8C)](#trigger-0c61dd8c).

Incoming activation links: enable from [Nuke_Gone (0C61D62C)](#trigger-0c61d62c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14176, Events line 14554, Actions line 14932.

<a id="trigger-0c61d62c"></a>

### 248. Nuke_Gone - 0C61D62C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [WeWin (0C61D87C)](#trigger-0c61d87c).

Attached scope: Nuclear Missile Silo (NAMISL), owner YuriCountry, cell (48, 89), tag 0C61D96C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [MakeCheer (0C61DD8C)](#trigger-0c61dd8c).
2. Enable and reset applicable timers for [WeWin (0C61D87C)](#trigger-0c61d87c).
3. Disable [Nuke_Gone (0C61D62C)](#trigger-0c61d62c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14177, Events line 14555, Actions line 14933.

<a id="trigger-0c13364c"></a>

### 249. Player_Takes_TF - 0C13364C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Set local flag 41 (Player_Owns_TF).
2. Enable and reset applicable timers for [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c).
3. Enable and reset applicable timers for [TD_ChangeHouse (0BFE86FC)](#trigger-0bfe86fc).
4. Enable and reset applicable timers for [TF_Snipers (0BC6993C)](#trigger-0bc6993c).
5. Enable and reset applicable timers for [TF_Engineers (0929A19C)](#trigger-0929a19c).
6. Enable and reset applicable timers for [Yuri_Taunt_1 (0B2AF2FC)](#trigger-0b2af2fc).
7. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
8. Disable [Player_Takes_TF (0C13364C)](#trigger-0c13364c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14178, Events line 14556, Actions line 14934.

<a id="trigger-0c11f15c"></a>

### 250. Yuri_Takes_TF - 0C11F15C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Takes_TF (0C13364C)](#trigger-0c13364c).

Incoming activation links: enable from [Player_Takes_TF (0C13364C)](#trigger-0c13364c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. local flag 41 (Player_Owns_TF) is set.

Flag writers in this mission: set local flag 41 (Player_Owns_TF) at [Player_Takes_TF (0C13364C)](#trigger-0c13364c); clear local flag 41 (Player_Owns_TF) at [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c); clear local flag 41 (Player_Owns_TF) at [PlantTF_Gone (09881BAC)](#trigger-09881bac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 41 (Player_Owns_TF).
2. Enable and reset applicable timers for [Player_Takes_TF (0C13364C)](#trigger-0c13364c).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14179, Events line 14557, Actions line 14935.

<a id="trigger-0bc6993c"></a>

### 251. TF_Snipers - 0BC6993C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TF (0C13364C)](#trigger-0c13364c).

Attached scope: tag definitions 0BC693BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TF_Snipers (0BC4EDAC)](all03umd-teams.md#team-0bc4edac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14180, Events line 14558, Actions line 14936.

<a id="trigger-0929a19c"></a>

### 252. TF_Engineers - 0929A19C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Takes_TF (0C13364C)](#trigger-0c13364c).

Attached scope: tag definitions 0929BC0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Yuri_FB_TF_Engineer (0B8E22EC)](all03umd-teams.md#team-0b8e22ec).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14181, Events line 14559, Actions line 14937.

<a id="trigger-09881bac"></a>

### 253. PlantTF_Gone - 09881BAC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c).

Incoming activation links: enable from [Enable_Plant_TF (0D6655AC)](#trigger-0d6655ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWRTF exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 39 (PlantTF_Gone).
2. Clear local flag 41 (Player_Owns_TF).
3. Enable and reset applicable timers for [Yuri_Power_Low (0BF257BC)](#trigger-0bf257bc).
4. Disable [Player_Takes_TF (0C13364C)](#trigger-0c13364c).
5. Disable [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c).
6. Disable [PlantTF_Gone (09881BAC)](#trigger-09881bac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14182, Events line 14560, Actions line 14938.

<a id="trigger-0b67d83c"></a>

### 254. PlantAC_Notice - 0B67D83C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B67FEAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 11 at waypoint 59 (cell 155, 118).
2. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14183, Events line 14561, Actions line 14939.

<a id="trigger-0be20acc"></a>

### 255. PlayerLose - 0BE20ACC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BE2051C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14184, Events line 14562, Actions line 14940.

<a id="trigger-0bfa3f3c"></a>

### 256. Give_Player_Radar - 0BFA3F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enter_Needle (0BFA668C)](#trigger-0bfa668c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Disable [Give_Player_Radar (0BFA3F3C)](#trigger-0bfa3f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14185, Events line 14563, Actions line 14941.

<a id="trigger-0bfa668c"></a>

### 257. Enter_Needle - 0BFA668C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Exit_Needle (0B7BAC0C)](#trigger-0b7bac0c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Give_Player_Radar (0BFA3F3C)](#trigger-0bfa3f3c).
2. Enable and reset applicable timers for [Exit_Needle (0B7BAC0C)](#trigger-0b7bac0c).
3. Disable [Enter_Needle (0BFA668C)](#trigger-0bfa668c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14186, Events line 14564, Actions line 14942.

<a id="trigger-0b7bac0c"></a>

### 258. Exit_Needle - 0B7BAC0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Medium_Enter (092C7F3C)](#trigger-092c7f3c).

Incoming activation links: enable from [Enter_Needle (0BFA668C)](#trigger-0bfa668c).

Attached scope: Seattle Space Needle (CASEAT01), owner Neutral, cell (109, 123), tag 0BFA637C, persistence mode 2.

**Wait for the recorded events:**

1. Building does not exist: type index 341 (global list position: Alcatraz (CASANF05)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Take_Away_Radar (0B7BCAAC)](#trigger-0b7bcaac).
2. Enable and reset applicable timers for [Enter_Needle (0BFA668C)](#trigger-0bfa668c).
3. Disable [Exit_Needle (0B7BAC0C)](#trigger-0b7bac0c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14187, Events line 14565, Actions line 14943.

<a id="trigger-092c7f3c"></a>

### 259. Medium_Enter - 092C7F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Easy_Enter (092589AC)](#trigger-092589ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 520 (cell 101, 58).
2. Reveal terrain around waypoint 521 (cell 90, 72).
3. Reveal terrain around waypoint 522 (cell 90, 107).
4. Reveal terrain around waypoint 523 (cell 109, 109).
5. Reveal terrain around waypoint 524 (cell 84, 134).
6. Reveal terrain around waypoint 525 (cell 65, 113).
7. Play sound RadarOn.
8. Disable [Medium_Enter (092C7F3C)](#trigger-092c7f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14188, Events line 14566, Actions line 14944.

<a id="trigger-0b7bcaac"></a>

### 260. Take_Away_Radar - 0B7BCAAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Give_Player_Radar (0BFA3F3C)](#trigger-0bfa3f3c).

Incoming activation links: enable from [Exit_Needle (0B7BAC0C)](#trigger-0b7bac0c).

Attached scope: Air Force Command Headquarters (GAAIRC), owner Neutral, cell (170, 108), tag 0BFA6C7C, persistence mode 2.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 12 (country/type NEUTRAL; placed owner Neutral).
2. Disable [Take_Away_Radar (0B7BCAAC)](#trigger-0b7bcaac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14189, Events line 14567, Actions line 14945.

<a id="trigger-092589ac"></a>

### 261. Easy_Enter - 092589AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: [Enter_Needle (0BFA668C)](#trigger-0bfa668c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Reveal the whole map.
2. Play sound SpyUplinkOn.
3. Disable [Easy_Enter (092589AC)](#trigger-092589ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14190, Events line 14568, Actions line 14946.

<a id="trigger-0961fb5c"></a>

### 262. Check_Russia_Status - 0961FB5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0961F54C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).
2. local flag 46 (Russia_Gone) is clear.

Flag writers in this mission: set local flag 46 (Russia_Gone) at [Check_Russia_Status (0961FB5C)](#trigger-0961fb5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 46 (Russia_Gone).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14191, Events line 14569, Actions line 14947.

<a id="trigger-0961f45c"></a>

### 263. Check_Nod_Status - 0961F45C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096195EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 11 (country/type NOD; placed owner Nod).
2. local flag 45 (Nod_Gone) is clear.

Flag writers in this mission: set local flag 45 (Nod_Gone) at [Check_Nod_Status (0961F45C)](#trigger-0961f45c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 45 (Nod_Gone).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14192, Events line 14570, Actions line 14948.

<a id="trigger-097e4a8c"></a>

### 264. Check_Confed_Status - 097E4A8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097E44DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 48 (Confed_Gone) is clear.
2. Destroyed,  All: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

Flag writers in this mission: set local flag 48 (Confed_Gone) at [Check_Confed_Status (097E4A8C)](#trigger-097e4a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 48 (Confed_Gone).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14193, Events line 14571, Actions line 14949.

<a id="trigger-097e43ec"></a>

### 265. Check_Arab_Status - 097E43EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097E411C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 47 (Arabs_Gone) is clear.
2. Destroyed,  All: owner selector 6 (country/type ARABS; placed owner Arabs).

Flag writers in this mission: set local flag 47 (Arabs_Gone) at [Check_Arab_Status (097E43EC)](#trigger-097e43ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 47 (Arabs_Gone).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14194, Events line 14572, Actions line 14950.

<a id="trigger-097c766c"></a>

### 266. Check_GDI_Status - 097C766C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097C2D7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 49 (GDI_Gone) is clear.
2. Destroyed,  All: owner selector 10 (country/type GDI; placed owner GDI).

Flag writers in this mission: set local flag 49 (GDI_Gone) at [Check_GDI_Status (097C766C)](#trigger-097c766c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 49 (GDI_Gone).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14195, Events line 14573, Actions line 14951.

<a id="trigger-09761a8c"></a>

### 267. Check_PPTF_Status - 09761A8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0976119C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 43 (PPTF_Gone) is clear.
2. Destroyed,  All: owner selector 14 (country/type PPTF COUNTRY; placed owner PPTFHouse).

Flag writers in this mission: set local flag 43 (PPTF_Gone) at [Frnch_Become_TB2 (0D5B6D9C)](#trigger-0d5b6d9c); set local flag 43 (PPTF_Gone) at [Check_PPTF_Status (09761A8C)](#trigger-09761a8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 43 (PPTF_Gone).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14196, Events line 14574, Actions line 14952.

<a id="trigger-0dadb03c"></a>

### 268. Check_Backup1_Stat - 0DADB03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0DADDB0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 15 (country/type BACKUP1 COUNTRY; placed owner Backup1House).
2. local flag 11 (Backup1_Gone) is clear.

Flag writers in this mission: set local flag 11 (Backup1_Gone) at [Check_Backup1_Stat (0DADB03C)](#trigger-0dadb03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 11 (Backup1_Gone).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14197, Events line 14575, Actions line 14953.

<a id="trigger-096e6b9c"></a>

### 269. TF_TE_DestroyTeam2 - 096E6B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_TE_DestroyTeam1 (096E6C8C)](#trigger-096e6c8c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

No event entries. Reachability requires separate runtime interpretation.

**Then perform these actions in order:**

No action entries.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14198, Events line 14576, Actions line 14954.

<a id="trigger-096e6aac"></a>

### 270. TF_Becomes_TE_1 - 096E6AAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_TE_DestroyTeam2 (096E6B9C)](#trigger-096e6b9c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

No event entries. Reachability requires separate runtime interpretation.

**Then perform these actions in order:**

No action entries.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14199, Events line 14577, Actions line 14955.

<a id="trigger-096e69bc"></a>

### 271. TF_Becomes_TE_2 - 096E69BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TF_Becomes_TE_1 (096E6AAC)](#trigger-096e6aac).

Attached scope: tag definitions 096E6D7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

No event entries. Reachability requires separate runtime interpretation.

**Then perform these actions in order:**

No action entries.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14200, Events line 14578, Actions line 14956.

<a id="trigger-096e75dc"></a>

### 272. TC_TE_DestroyTeam1 - 096E75DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_TE_ChangeHouse (0C0DE0DC)](#trigger-0c0de0dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Gatt1 (0967471C)](all03umd-teams.md#team-0967471c).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Gatt2 (09675EFC)](all03umd-teams.md#team-09675efc).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init1 (09675B1C)](all03umd-teams.md#team-09675b1c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init2 (096756FC)](all03umd-teams.md#team-096756fc).
5. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init3 (0BE0D2BC)](all03umd-teams.md#team-0be0d2bc).
6. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Init4 (06C6FEFC)](all03umd-teams.md#team-06c6fefc).
7. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Lasher1 (06C6F82C)](all03umd-teams.md#team-06c6f82c).
8. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Lasher2 (06C6F21C)](all03umd-teams.md#team-06c6f21c).
9. Enable and reset applicable timers for [TC_TE_DestroyTeam2 (096E74EC)](#trigger-096e74ec).
10. Disable [TC_TE_DestroyTeam1 (096E75DC)](#trigger-096e75dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14201, Events line 14579, Actions line 14957.

<a id="trigger-096e74ec"></a>

### 273. TC_TE_DestroyTeam2 - 096E74EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_TE_DestroyTeam1 (096E75DC)](#trigger-096e75dc).

Incoming activation links: enable from [TC_TE_DestroyTeam1 (096E75DC)](#trigger-096e75dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Lasher3 (06C6E0FC)](all03umd-teams.md#team-06c6e0fc).
2. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Virus (06C6B95C)](all03umd-teams.md#team-06c6b95c).
3. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Yuri1 (06C6B53C)](all03umd-teams.md#team-06c6b53c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_TC_Yuri2 (06C6B11C)](all03umd-teams.md#team-06c6b11c).
5. Enable and reset applicable timers for [TC_Becomes_TE_1 (096E73FC)](#trigger-096e73fc).
6. Disable [TC_TE_DestroyTeam2 (096E74EC)](#trigger-096e74ec).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14202, Events line 14580, Actions line 14958.

<a id="trigger-096e73fc"></a>

### 274. TC_Becomes_TE_1 - 096E73FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_TE_DestroyTeam2 (096E74EC)](#trigger-096e74ec).

Incoming activation links: enable from [TC_TE_DestroyTeam2 (096E74EC)](#trigger-096e74ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TE_Gatt1 (0C0B821C)](all03umd-teams.md#team-0c0b821c).
2. Create/recruit team [TEAM_TE_Gatt2 (09502E2C)](all03umd-teams.md#team-09502e2c).
3. Create/recruit team [TEAM_TE_Init1 (0950297C)](all03umd-teams.md#team-0950297c).
4. Create/recruit team [TEAM_TE_Init2 (0950251C)](all03umd-teams.md#team-0950251c).
5. Create/recruit team [TEAM_TE_Init3 (095020BC)](all03umd-teams.md#team-095020bc).
6. Create/recruit team [TEAM_TE_Init4 (0950D50C)](all03umd-teams.md#team-0950d50c).
7. Create/recruit team [TEAM_TE_Lasher1 (0950D16C)](all03umd-teams.md#team-0950d16c).
8. Create/recruit team [TEAM_TE_Lasher2 (0950D03C)](all03umd-teams.md#team-0950d03c).
9. Enable and reset applicable timers for [TC_Becomes_TE_2 (096E730C)](#trigger-096e730c).
10. Disable [TC_Becomes_TE_1 (096E73FC)](#trigger-096e73fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14203, Events line 14581, Actions line 14959.

<a id="trigger-096e730c"></a>

### 275. TC_Becomes_TE_2 - 096E730C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TC_Becomes_TE_1 (096E73FC)](#trigger-096e73fc).

Incoming activation links: enable from [TC_Becomes_TE_1 (096E73FC)](#trigger-096e73fc).

Attached scope: tag definitions 0C0DF60C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_TE_Lasher3 (0950F66C)](all03umd-teams.md#team-0950f66c).
2. Create/recruit team [TEAM_TE_Virus (0950F20C)](all03umd-teams.md#team-0950f20c).
3. Create/recruit team [TEAM_TE_Yuri1 (0950EC8C)](all03umd-teams.md#team-0950ec8c).
4. Create/recruit team [TEAM_TE_Yuri2 (0950E65C)](all03umd-teams.md#team-0950e65c).
5. Disable [TC_Becomes_TE_2 (096E730C)](#trigger-096e730c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14204, Events line 14582, Actions line 14960.

<a id="trigger-096c58bc"></a>

### 276. Check_French_Status - 096C58BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096C533C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 44 (French_Gone) is clear.
2. Destroyed,  All: owner selector 2 (country/type FRENCH; placed owner French).

Flag writers in this mission: set local flag 44 (French_Gone) at [Check_French_Status (096C58BC)](#trigger-096c58bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 44 (French_Gone).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14205, Events line 14583, Actions line 14961.

<a id="trigger-094f5c2c"></a>

### 277. Nuke_AA_True - 094F5C2C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Nuke_Timer_PP (094DE72C)](#trigger-094de72c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 5 (Player_Owns_AA) is set.
2. local flag 4 (Nuked_PPAA) is clear.
3. 1 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: clear local flag 5 (Player_Owns_AA) at [PlantAA_Gone (093BEEDC)](#trigger-093beedc); set local flag 5 (Player_Owns_AA) at [Player_Takes_AA (0945ABBC)](#trigger-0945abbc); clear local flag 5 (Player_Owns_AA) at [Yuri_Takes_AA (0945934C)](#trigger-0945934c); set local flag 5 (Player_Owns_AA) at [Set_Locals (06B6627C)](#trigger-06b6627c); set local flag 4 (Nuked_PPAA) at [Nuke_AA_True (094F5C2C)](#trigger-094f5c2c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AA_False (094F5A5C)](#trigger-094f5a5c).
2. Disable [Nuke_AA_False2 (043A430C)](#trigger-043a430c).
3. Preferred Target Cell Clear; main setting 26; location/duration field AA.
4. Preferred Target Cell Set; main setting 26; location/duration field AA.
5. Set local flag 4 (Nuked_PPAA).
6. Disable [Nuke_AA_True (094F5C2C)](#trigger-094f5c2c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14206, Events line 14584, Actions line 14962.

<a id="trigger-094f5a5c"></a>

### 278. Nuke_AA_False - 094F5A5C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AA_True (094F5C2C)](#trigger-094f5c2c).

Incoming activation links: enable from [Nuke_Timer_PP (094DE72C)](#trigger-094de72c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 5 (Player_Owns_AA) is clear.
2. 1 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: clear local flag 5 (Player_Owns_AA) at [PlantAA_Gone (093BEEDC)](#trigger-093beedc); set local flag 5 (Player_Owns_AA) at [Player_Takes_AA (0945ABBC)](#trigger-0945abbc); clear local flag 5 (Player_Owns_AA) at [Yuri_Takes_AA (0945934C)](#trigger-0945934c); set local flag 5 (Player_Owns_AA) at [Set_Locals (06B6627C)](#trigger-06b6627c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AA_True (094F5C2C)](#trigger-094f5c2c).
2. Enable and reset applicable timers for [Nuke_AB_True (094F596C)](#trigger-094f596c).
3. Enable and reset applicable timers for [Nuke_AB_False (094F587C)](#trigger-094f587c).
4. Enable and reset applicable timers for [Nuke_AB_False2 (0D4FBBDC)](#trigger-0d4fbbdc).
5. Disable [Nuke_AA_False2 (043A430C)](#trigger-043a430c).
6. Disable [Nuke_AA_False (094F5A5C)](#trigger-094f5a5c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14207, Events line 14585, Actions line 14963.

<a id="trigger-043a430c"></a>

### 279. Nuke_AA_False2 - 043A430C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TF_False (094F68AC)](#trigger-094f68ac).

Incoming activation links: enable from [Nuke_Timer_PP (094DE72C)](#trigger-094de72c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 4 (Nuked_PPAA) is set.
2. 1 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 4 (Nuked_PPAA) at [Nuke_AA_True (094F5C2C)](#trigger-094f5c2c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AA_True (094F5C2C)](#trigger-094f5c2c).
2. Disable [Nuke_AA_False (094F5A5C)](#trigger-094f5a5c).
3. Enable and reset applicable timers for [Nuke_AB_True (094F596C)](#trigger-094f596c).
4. Enable and reset applicable timers for [Nuke_AB_False (094F587C)](#trigger-094f587c).
5. Enable and reset applicable timers for [Nuke_AB_False2 (0D4FBBDC)](#trigger-0d4fbbdc).
6. Disable [Nuke_AA_False2 (043A430C)](#trigger-043a430c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14208, Events line 14586, Actions line 14964.

<a id="trigger-094f596c"></a>

### 280. Nuke_AB_True - 094F596C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AA_False (094F5A5C)](#trigger-094f5a5c).

Incoming activation links: enable from [Nuke_AA_False (094F5A5C)](#trigger-094f5a5c); enable from [Nuke_AA_False2 (043A430C)](#trigger-043a430c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 25 (Player_Owns_AB) is set.
2. local flag 6 (Nuked_PPAB) is clear.

Flag writers in this mission: clear local flag 25 (Player_Owns_AB) at [PlantAB_Gone (093BE2FC)](#trigger-093be2fc); set local flag 25 (Player_Owns_AB) at [Player_Takes_AB (0CF8179C)](#trigger-0cf8179c); clear local flag 25 (Player_Owns_AB) at [Yuri_Takes_AB (0CF8110C)](#trigger-0cf8110c); set local flag 25 (Player_Owns_AB) at [Set_Locals (06B6627C)](#trigger-06b6627c); set local flag 6 (Nuked_PPAB) at [Nuke_AB_True (094F596C)](#trigger-094f596c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AB_False (094F587C)](#trigger-094f587c).
2. Disable [Nuke_AB_False2 (0D4FBBDC)](#trigger-0d4fbbdc).
3. Preferred Target Cell Set; main setting 27; location/duration field AB.
4. Set local flag 6 (Nuked_PPAB).
5. Disable [Nuke_AB_True (094F596C)](#trigger-094f596c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14209, Events line 14587, Actions line 14965.

<a id="trigger-094f587c"></a>

### 281. Nuke_AB_False - 094F587C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AB_True (094F596C)](#trigger-094f596c).

Incoming activation links: enable from [Nuke_AA_False (094F5A5C)](#trigger-094f5a5c); enable from [Nuke_AA_False2 (043A430C)](#trigger-043a430c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 25 (Player_Owns_AB) is clear.

Flag writers in this mission: clear local flag 25 (Player_Owns_AB) at [PlantAB_Gone (093BE2FC)](#trigger-093be2fc); set local flag 25 (Player_Owns_AB) at [Player_Takes_AB (0CF8179C)](#trigger-0cf8179c); clear local flag 25 (Player_Owns_AB) at [Yuri_Takes_AB (0CF8110C)](#trigger-0cf8110c); set local flag 25 (Player_Owns_AB) at [Set_Locals (06B6627C)](#trigger-06b6627c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AB_True (094F596C)](#trigger-094f596c).
2. Enable and reset applicable timers for [Nuke_AC_True (094F578C)](#trigger-094f578c).
3. Enable and reset applicable timers for [Nuke_AC_False (094F569C)](#trigger-094f569c).
4. Enable and reset applicable timers for [Nuke_AC_False2 (0D4FBAEC)](#trigger-0d4fbaec).
5. Disable [Nuke_AB_False2 (0D4FBBDC)](#trigger-0d4fbbdc).
6. Disable [Nuke_AB_False (094F587C)](#trigger-094f587c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14210, Events line 14588, Actions line 14966.

<a id="trigger-0d4fbbdc"></a>

### 282. Nuke_AB_False2 - 0D4FBBDC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AA_False2 (043A430C)](#trigger-043a430c).

Incoming activation links: enable from [Nuke_AA_False (094F5A5C)](#trigger-094f5a5c); enable from [Nuke_AA_False2 (043A430C)](#trigger-043a430c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 6 (Nuked_PPAB) is set.

Flag writers in this mission: set local flag 6 (Nuked_PPAB) at [Nuke_AB_True (094F596C)](#trigger-094f596c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AB_True (094F596C)](#trigger-094f596c).
2. Disable [Nuke_AB_False (094F587C)](#trigger-094f587c).
3. Enable and reset applicable timers for [Nuke_AC_True (094F578C)](#trigger-094f578c).
4. Enable and reset applicable timers for [Nuke_AC_False (094F569C)](#trigger-094f569c).
5. Enable and reset applicable timers for [Nuke_AC_False2 (0D4FBAEC)](#trigger-0d4fbaec).
6. Disable [Nuke_AB_False2 (0D4FBBDC)](#trigger-0d4fbbdc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14211, Events line 14589, Actions line 14967.

<a id="trigger-094f68ac"></a>

### 283. Nuke_TF_False - 094F68AC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TF_True (094F699C)](#trigger-094f699c).

Incoming activation links: enable from [Nuke_TE_False (094F6A8C)](#trigger-094f6a8c); enable from [Nuke_TE_False2 (0D4FB54C)](#trigger-0d4fb54c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 41 (Player_Owns_TF) is clear.

Flag writers in this mission: set local flag 41 (Player_Owns_TF) at [Player_Takes_TF (0C13364C)](#trigger-0c13364c); clear local flag 41 (Player_Owns_TF) at [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c); clear local flag 41 (Player_Owns_TF) at [PlantTF_Gone (09881BAC)](#trigger-09881bac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TF_True (094F699C)](#trigger-094f699c).
2. Disable [Nuke_TF_False2 (0D4FB45C)](#trigger-0d4fb45c).
3. Enable and reset applicable timers for [Nuke_MA_True (094CED3C)](#trigger-094ced3c).
4. Enable and reset applicable timers for [Nuke_MA_False (094CEB6C)](#trigger-094ceb6c).
5. Disable [Nuke_TF_True (094F699C)](#trigger-094f699c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14212, Events line 14590, Actions line 14968.

<a id="trigger-094f578c"></a>

### 284. Nuke_AC_True - 094F578C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AB_False (094F587C)](#trigger-094f587c).

Incoming activation links: enable from [Nuke_AB_False (094F587C)](#trigger-094f587c); enable from [Nuke_AB_False2 (0D4FBBDC)](#trigger-0d4fbbdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 26 (Player_Owns_AC) is set.
2. local flag 18 (Nuked_PPAC) is clear.

Flag writers in this mission: clear local flag 26 (Player_Owns_AC) at [PlantAC_Gone (093BFDDC)](#trigger-093bfddc); set local flag 26 (Player_Owns_AC) at [Player_Takes_AC (06B5EC6C)](#trigger-06b5ec6c); clear local flag 26 (Player_Owns_AC) at [Yuri_Takes_AC (06B5D04C)](#trigger-06b5d04c); set local flag 18 (Nuked_PPAC) at [Nuke_AC_True (094F578C)](#trigger-094f578c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AC_False (094F569C)](#trigger-094f569c).
2. Disable [Nuke_AC_False2 (0D4FBAEC)](#trigger-0d4fbaec).
3. Preferred Target Cell Set; main setting 28; location/duration field AC.
4. Set local flag 18 (Nuked_PPAC).
5. Disable [Nuke_AC_True (094F578C)](#trigger-094f578c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14213, Events line 14591, Actions line 14969.

<a id="trigger-094f569c"></a>

### 285. Nuke_AC_False - 094F569C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AC_True (094F578C)](#trigger-094f578c).

Incoming activation links: enable from [Nuke_AB_False (094F587C)](#trigger-094f587c); enable from [Nuke_AB_False2 (0D4FBBDC)](#trigger-0d4fbbdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 26 (Player_Owns_AC) is clear.

Flag writers in this mission: clear local flag 26 (Player_Owns_AC) at [PlantAC_Gone (093BFDDC)](#trigger-093bfddc); set local flag 26 (Player_Owns_AC) at [Player_Takes_AC (06B5EC6C)](#trigger-06b5ec6c); clear local flag 26 (Player_Owns_AC) at [Yuri_Takes_AC (06B5D04C)](#trigger-06b5d04c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AC_True (094F578C)](#trigger-094f578c).
2. Enable and reset applicable timers for [Nuke_AD_True (094F55AC)](#trigger-094f55ac).
3. Enable and reset applicable timers for [Nuke_AD_False (094F54BC)](#trigger-094f54bc).
4. Enable and reset applicable timers for [Nuke_AD_False2 (0D4FB9FC)](#trigger-0d4fb9fc).
5. Disable [Nuke_AC_False2 (0D4FBAEC)](#trigger-0d4fbaec).
6. Disable [Nuke_AC_False (094F569C)](#trigger-094f569c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14214, Events line 14592, Actions line 14970.

<a id="trigger-0d4fbaec"></a>

### 286. Nuke_AC_False2 - 0D4FBAEC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AB_False2 (0D4FBBDC)](#trigger-0d4fbbdc).

Incoming activation links: enable from [Nuke_AB_False (094F587C)](#trigger-094f587c); enable from [Nuke_AB_False2 (0D4FBBDC)](#trigger-0d4fbbdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 18 (Nuked_PPAC) is set.

Flag writers in this mission: set local flag 18 (Nuked_PPAC) at [Nuke_AC_True (094F578C)](#trigger-094f578c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AC_True (094F578C)](#trigger-094f578c).
2. Disable [Nuke_AC_False (094F569C)](#trigger-094f569c).
3. Enable and reset applicable timers for [Nuke_AD_True (094F55AC)](#trigger-094f55ac).
4. Enable and reset applicable timers for [Nuke_AD_False (094F54BC)](#trigger-094f54bc).
5. Enable and reset applicable timers for [Nuke_AD_False2 (0D4FB9FC)](#trigger-0d4fb9fc).
6. Disable [Nuke_AC_False2 (0D4FBAEC)](#trigger-0d4fbaec).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14215, Events line 14593, Actions line 14971.

<a id="trigger-094f699c"></a>

### 287. Nuke_TF_True - 094F699C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TE_False (094F6A8C)](#trigger-094f6a8c).

Incoming activation links: enable from [Nuke_TE_False (094F6A8C)](#trigger-094f6a8c); enable from [Nuke_TE_False2 (0D4FB54C)](#trigger-0d4fb54c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 41 (Player_Owns_TF) is set.

Flag writers in this mission: set local flag 41 (Player_Owns_TF) at [Player_Takes_TF (0C13364C)](#trigger-0c13364c); clear local flag 41 (Player_Owns_TF) at [Yuri_Takes_TF (0C11F15C)](#trigger-0c11f15c); clear local flag 41 (Player_Owns_TF) at [PlantTF_Gone (09881BAC)](#trigger-09881bac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TF_False (094F68AC)](#trigger-094f68ac).
2. Disable [Nuke_TF_False2 (0D4FB45C)](#trigger-0d4fb45c).
3. Preferred Target Cell Set; main setting 525; location/duration field TF.
4. Set local flag 54 (Nuked_PPTF).
5. Disable [Nuke_TF_True (094F699C)](#trigger-094f699c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14216, Events line 14594, Actions line 14972.

<a id="trigger-0d4fb45c"></a>

### 288. Nuke_TF_False2 - 0D4FB45C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TE_False2 (0D4FB54C)](#trigger-0d4fb54c).

Incoming activation links: enable from [Nuke_TE_False (094F6A8C)](#trigger-094f6a8c); enable from [Nuke_TE_False2 (0D4FB54C)](#trigger-0d4fb54c).

Attached scope: tag definitions 094F5B4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 54 (Nuked_PPTF) is set.

Flag writers in this mission: set local flag 54 (Nuked_PPTF) at [Nuke_TF_True (094F699C)](#trigger-094f699c); set local flag 54 (Nuked_PPTF) at [Nuke_TE_True (094F6B7C)](#trigger-094f6b7c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TF_True (094F699C)](#trigger-094f699c).
2. Disable [Nuke_TF_False (094F68AC)](#trigger-094f68ac).
3. Enable and reset applicable timers for [Nuke_MA_True (094CED3C)](#trigger-094ced3c).
4. Enable and reset applicable timers for [Nuke_MA_False (094CEB6C)](#trigger-094ceb6c).
5. Disable [Nuke_TF_False2 (0D4FB45C)](#trigger-0d4fb45c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14217, Events line 14595, Actions line 14973.

<a id="trigger-094ced3c"></a>

### 289. Nuke_MA_True - 094CED3C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Nuke_TF_False (094F68AC)](#trigger-094f68ac); enable from [Nuke_TF_False2 (0D4FB45C)](#trigger-0d4fb45c); enable from [Nuke_Timer_Misc (094DE55C)](#trigger-094de55c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 13 (Nuked_MA) is clear.

Flag writers in this mission: set local flag 13 (Nuked_MA) at [Nuke_MA_True (094CED3C)](#trigger-094ced3c); clear local flag 13 (Nuked_MA) at [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_MA_False (094CEB6C)](#trigger-094ceb6c).
2. Preferred Target Cell Set; main setting 338; location/duration field MA.
3. Set local flag 13 (Nuked_MA).
4. Disable [Nuke_MA_True (094CED3C)](#trigger-094ced3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14218, Events line 14596, Actions line 14974.

<a id="trigger-094ceb6c"></a>

### 290. Nuke_MA_False - 094CEB6C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_MA_True (094CED3C)](#trigger-094ced3c).

Incoming activation links: enable from [Nuke_TF_False (094F68AC)](#trigger-094f68ac); enable from [Nuke_TF_False2 (0D4FB45C)](#trigger-0d4fb45c); enable from [Nuke_Timer_Misc (094DE55C)](#trigger-094de55c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 13 (Nuked_MA) is set.

Flag writers in this mission: set local flag 13 (Nuked_MA) at [Nuke_MA_True (094CED3C)](#trigger-094ced3c); clear local flag 13 (Nuked_MA) at [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_MA_True (094CED3C)](#trigger-094ced3c).
2. Enable and reset applicable timers for [Nuke_MB_True (094CEA7C)](#trigger-094cea7c).
3. Enable and reset applicable timers for [Nuke_MB_False (094CE98C)](#trigger-094ce98c).
4. Disable [Nuke_MA_False (094CEB6C)](#trigger-094ceb6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14219, Events line 14597, Actions line 14975.

<a id="trigger-094f55ac"></a>

### 291. Nuke_AD_True - 094F55AC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AC_False (094F569C)](#trigger-094f569c).

Incoming activation links: enable from [Nuke_AC_False (094F569C)](#trigger-094f569c); enable from [Nuke_AC_False2 (0D4FBAEC)](#trigger-0d4fbaec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 27 (Player_Owns_AD) is set.
2. local flag 42 (Nuked_PPAD) is clear.

Flag writers in this mission: clear local flag 27 (Player_Owns_AD) at [PlantAD_Gone (093BF8FC)](#trigger-093bf8fc); set local flag 27 (Player_Owns_AD) at [Player_Takes_AD (094D82BC)](#trigger-094d82bc); clear local flag 27 (Player_Owns_AD) at [Yuri_Takes_AD (094D9C5C)](#trigger-094d9c5c); set local flag 27 (Player_Owns_AD) at [Set_Locals (06B6627C)](#trigger-06b6627c); set local flag 42 (Nuked_PPAD) at [Nuke_AD_True (094F55AC)](#trigger-094f55ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AD_False (094F54BC)](#trigger-094f54bc).
2. Disable [Nuke_AD_False2 (0D4FB9FC)](#trigger-0d4fb9fc).
3. Preferred Target Cell Set; main setting 29; location/duration field AD.
4. Set local flag 42 (Nuked_PPAD).
5. Disable [Nuke_AD_True (094F55AC)](#trigger-094f55ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14220, Events line 14598, Actions line 14976.

<a id="trigger-094f54bc"></a>

### 292. Nuke_AD_False - 094F54BC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AD_True (094F55AC)](#trigger-094f55ac).

Incoming activation links: enable from [Nuke_AC_False (094F569C)](#trigger-094f569c); enable from [Nuke_AC_False2 (0D4FBAEC)](#trigger-0d4fbaec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 27 (Player_Owns_AD) is clear.

Flag writers in this mission: clear local flag 27 (Player_Owns_AD) at [PlantAD_Gone (093BF8FC)](#trigger-093bf8fc); set local flag 27 (Player_Owns_AD) at [Player_Takes_AD (094D82BC)](#trigger-094d82bc); clear local flag 27 (Player_Owns_AD) at [Yuri_Takes_AD (094D9C5C)](#trigger-094d9c5c); set local flag 27 (Player_Owns_AD) at [Set_Locals (06B6627C)](#trigger-06b6627c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AD_True (094F55AC)](#trigger-094f55ac).
2. Enable and reset applicable timers for [Nuke_TA_True (094F53CC)](#trigger-094f53cc).
3. Enable and reset applicable timers for [Nuke_TA_False (094F52DC)](#trigger-094f52dc).
4. Enable and reset applicable timers for [Nuke_TA_False2 (0D4FB90C)](#trigger-0d4fb90c).
5. Disable [Nuke_AD_False2 (0D4FB9FC)](#trigger-0d4fb9fc).
6. Disable [Nuke_AD_False (094F54BC)](#trigger-094f54bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14221, Events line 14599, Actions line 14977.

<a id="trigger-0d4fb9fc"></a>

### 293. Nuke_AD_False2 - 0D4FB9FC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AC_False2 (0D4FBAEC)](#trigger-0d4fbaec).

Incoming activation links: enable from [Nuke_AC_False (094F569C)](#trigger-094f569c); enable from [Nuke_AC_False2 (0D4FBAEC)](#trigger-0d4fbaec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 42 (Nuked_PPAD) is set.

Flag writers in this mission: set local flag 42 (Nuked_PPAD) at [Nuke_AD_True (094F55AC)](#trigger-094f55ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_AD_True (094F55AC)](#trigger-094f55ac).
2. Disable [Nuke_AD_False (094F54BC)](#trigger-094f54bc).
3. Enable and reset applicable timers for [Nuke_TA_True (094F53CC)](#trigger-094f53cc).
4. Enable and reset applicable timers for [Nuke_TA_False (094F52DC)](#trigger-094f52dc).
5. Enable and reset applicable timers for [Nuke_TA_False2 (0D4FB90C)](#trigger-0d4fb90c).
6. Disable [Nuke_AD_False2 (0D4FB9FC)](#trigger-0d4fb9fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14222, Events line 14600, Actions line 14978.

<a id="trigger-094f6a8c"></a>

### 294. Nuke_TE_False - 094F6A8C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TE_True (094F6B7C)](#trigger-094f6b7c).

Incoming activation links: enable from [Nuke_TD_False2 (0D4FB63C)](#trigger-0d4fb63c); enable from [Nuke_TD_False (094F6C6C)](#trigger-094f6c6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 40 (Player_Owns_TE) is clear.

Flag writers in this mission: clear local flag 40 (Player_Owns_TE) at [PlantTE_Gone (045D673C)](#trigger-045d673c); set local flag 40 (Player_Owns_TE) at [Player_Takes_TE (045C109C)](#trigger-045c109c); clear local flag 40 (Player_Owns_TE) at [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TE_True (094F6B7C)](#trigger-094f6b7c).
2. Disable [Nuke_TE_False2 (0D4FB54C)](#trigger-0d4fb54c).
3. Enable and reset applicable timers for [Nuke_TF_True (094F699C)](#trigger-094f699c).
4. Enable and reset applicable timers for [Nuke_TF_False (094F68AC)](#trigger-094f68ac).
5. Enable and reset applicable timers for [Nuke_TF_False2 (0D4FB45C)](#trigger-0d4fb45c).
6. Disable [Nuke_TE_False (094F6A8C)](#trigger-094f6a8c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14223, Events line 14601, Actions line 14979.

<a id="trigger-0d4fb54c"></a>

### 295. Nuke_TE_False2 - 0D4FB54C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TD_False2 (0D4FB63C)](#trigger-0d4fb63c).

Incoming activation links: enable from [Nuke_TD_False2 (0D4FB63C)](#trigger-0d4fb63c); enable from [Nuke_TD_False (094F6C6C)](#trigger-094f6c6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 53 (Nuked_PPTE) is set.

**Then perform these actions in order:**

1. Disable [Nuke_TE_True (094F6B7C)](#trigger-094f6b7c).
2. Disable [Nuke_TE_False (094F6A8C)](#trigger-094f6a8c).
3. Enable and reset applicable timers for [Nuke_TF_True (094F699C)](#trigger-094f699c).
4. Enable and reset applicable timers for [Nuke_TF_False (094F68AC)](#trigger-094f68ac).
5. Enable and reset applicable timers for [Nuke_TF_False2 (0D4FB45C)](#trigger-0d4fb45c).
6. Disable [Nuke_TE_False2 (0D4FB54C)](#trigger-0d4fb54c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14224, Events line 14602, Actions line 14980.

<a id="trigger-094cea7c"></a>

### 296. Nuke_MB_True - 094CEA7C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_MA_False (094CEB6C)](#trigger-094ceb6c).

Incoming activation links: enable from [Nuke_MA_False (094CEB6C)](#trigger-094ceb6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 16 (Nuked_MB) is clear.

Flag writers in this mission: set local flag 16 (Nuked_MB) at [Nuke_MB_True (094CEA7C)](#trigger-094cea7c); clear local flag 16 (Nuked_MB) at [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_MB_False (094CE98C)](#trigger-094ce98c).
2. Preferred Target Cell Set; main setting 339; location/duration field MB.
3. Set local flag 16 (Nuked_MB).
4. Disable [Nuke_MB_True (094CEA7C)](#trigger-094cea7c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14225, Events line 14603, Actions line 14981.

<a id="trigger-094ce98c"></a>

### 297. Nuke_MB_False - 094CE98C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_MB_True (094CEA7C)](#trigger-094cea7c).

Incoming activation links: enable from [Nuke_MA_False (094CEB6C)](#trigger-094ceb6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 16 (Nuked_MB) is set.

Flag writers in this mission: set local flag 16 (Nuked_MB) at [Nuke_MB_True (094CEA7C)](#trigger-094cea7c); clear local flag 16 (Nuked_MB) at [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_MB_True (094CEA7C)](#trigger-094cea7c).
2. Enable and reset applicable timers for [Nuke_MC_True (094CE89C)](#trigger-094ce89c).
3. Enable and reset applicable timers for [Nuke_MC_False (094CE7AC)](#trigger-094ce7ac).
4. Disable [Nuke_MB_False (094CE98C)](#trigger-094ce98c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14226, Events line 14604, Actions line 14982.

<a id="trigger-094f53cc"></a>

### 298. Nuke_TA_True - 094F53CC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AD_False (094F54BC)](#trigger-094f54bc).

Incoming activation links: enable from [Nuke_AD_False (094F54BC)](#trigger-094f54bc); enable from [Nuke_AD_False2 (0D4FB9FC)](#trigger-0d4fb9fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 28 (Player_Owns_TA) is set.
2. local flag 10 (Nuked_PPTA) is clear.

Flag writers in this mission: clear local flag 28 (Player_Owns_TA) at [PlantTA_Gone (094E203C)](#trigger-094e203c); set local flag 28 (Player_Owns_TA) at [Player_Takes_TA (094E3ACC)](#trigger-094e3acc); clear local flag 28 (Player_Owns_TA) at [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c); set local flag 10 (Nuked_PPTA) at [Nuke_TA_True (094F53CC)](#trigger-094f53cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TA_False (094F52DC)](#trigger-094f52dc).
2. Disable [Nuke_TA_False2 (0D4FB90C)](#trigger-0d4fb90c).
3. Preferred Target Cell Set; main setting 520; location/duration field TA.
4. Set local flag 10 (Nuked_PPTA).
5. Disable [Nuke_TA_True (094F53CC)](#trigger-094f53cc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14227, Events line 14605, Actions line 14983.

<a id="trigger-094f52dc"></a>

### 299. Nuke_TA_False - 094F52DC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TA_True (094F53CC)](#trigger-094f53cc).

Incoming activation links: enable from [Nuke_AD_False (094F54BC)](#trigger-094f54bc); enable from [Nuke_AD_False2 (0D4FB9FC)](#trigger-0d4fb9fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 28 (Player_Owns_TA) is clear.

Flag writers in this mission: clear local flag 28 (Player_Owns_TA) at [PlantTA_Gone (094E203C)](#trigger-094e203c); set local flag 28 (Player_Owns_TA) at [Player_Takes_TA (094E3ACC)](#trigger-094e3acc); clear local flag 28 (Player_Owns_TA) at [Yuri_Takes_TA (094E3C3C)](#trigger-094e3c3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TA_True (094F53CC)](#trigger-094f53cc).
2. Enable and reset applicable timers for [Nuke_TB_True (094F51EC)](#trigger-094f51ec).
3. Enable and reset applicable timers for [Nuke_TB_False (094F50FC)](#trigger-094f50fc).
4. Enable and reset applicable timers for [Nuke_TB_False2 (0D4FB81C)](#trigger-0d4fb81c).
5. Disable [Nuke_TA_False2 (0D4FB90C)](#trigger-0d4fb90c).
6. Disable [Nuke_TA_False (094F52DC)](#trigger-094f52dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14228, Events line 14606, Actions line 14984.

<a id="trigger-0d4fb90c"></a>

### 300. Nuke_TA_False2 - 0D4FB90C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_AD_False2 (0D4FB9FC)](#trigger-0d4fb9fc).

Incoming activation links: enable from [Nuke_AD_False (094F54BC)](#trigger-094f54bc); enable from [Nuke_AD_False2 (0D4FB9FC)](#trigger-0d4fb9fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 10 (Nuked_PPTA) is set.

Flag writers in this mission: set local flag 10 (Nuked_PPTA) at [Nuke_TA_True (094F53CC)](#trigger-094f53cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TA_True (094F53CC)](#trigger-094f53cc).
2. Disable [Nuke_TA_False (094F52DC)](#trigger-094f52dc).
3. Enable and reset applicable timers for [Nuke_TB_True (094F51EC)](#trigger-094f51ec).
4. Enable and reset applicable timers for [Nuke_TB_False (094F50FC)](#trigger-094f50fc).
5. Enable and reset applicable timers for [Nuke_TB_False2 (0D4FB81C)](#trigger-0d4fb81c).
6. Disable [Nuke_TA_False2 (0D4FB90C)](#trigger-0d4fb90c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14229, Events line 14607, Actions line 14985.

<a id="trigger-094f6b7c"></a>

### 301. Nuke_TE_True - 094F6B7C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TD_False (094F6C6C)](#trigger-094f6c6c).

Incoming activation links: enable from [Nuke_TD_False2 (0D4FB63C)](#trigger-0d4fb63c); enable from [Nuke_TD_False (094F6C6C)](#trigger-094f6c6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 40 (Player_Owns_TE) is set.

Flag writers in this mission: clear local flag 40 (Player_Owns_TE) at [PlantTE_Gone (045D673C)](#trigger-045d673c); set local flag 40 (Player_Owns_TE) at [Player_Takes_TE (045C109C)](#trigger-045c109c); clear local flag 40 (Player_Owns_TE) at [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TE_False (094F6A8C)](#trigger-094f6a8c).
2. Disable [Nuke_TE_False2 (0D4FB54C)](#trigger-0d4fb54c).
3. Preferred Target Cell Set; main setting 524; location/duration field TE.
4. Set local flag 54 (Nuked_PPTF).
5. Disable [Nuke_TE_True (094F6B7C)](#trigger-094f6b7c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14230, Events line 14608, Actions line 14986.

<a id="trigger-0d4fb63c"></a>

### 302. Nuke_TD_False2 - 0D4FB63C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TC_False2 (0D4FB72C)](#trigger-0d4fb72c).

Incoming activation links: enable from [Nuke_TC_False2 (0D4FB72C)](#trigger-0d4fb72c); enable from [Nuke_TC_False (094F6E4C)](#trigger-094f6e4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 52 (Nuked_PPTD) is set.

Flag writers in this mission: set local flag 52 (Nuked_PPTD) at [Nuke_TD_True (094F6D5C)](#trigger-094f6d5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TD_True (094F6D5C)](#trigger-094f6d5c).
2. Disable [Nuke_TD_False (094F6C6C)](#trigger-094f6c6c).
3. Enable and reset applicable timers for [Nuke_TE_True (094F6B7C)](#trigger-094f6b7c).
4. Enable and reset applicable timers for [Nuke_TE_False (094F6A8C)](#trigger-094f6a8c).
5. Enable and reset applicable timers for [Nuke_TE_False2 (0D4FB54C)](#trigger-0d4fb54c).
6. Disable [Nuke_TD_False2 (0D4FB63C)](#trigger-0d4fb63c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14231, Events line 14609, Actions line 14987.

<a id="trigger-094ce89c"></a>

### 303. Nuke_MC_True - 094CE89C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_MB_False (094CE98C)](#trigger-094ce98c).

Incoming activation links: enable from [Nuke_MB_False (094CE98C)](#trigger-094ce98c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 12 (Nuked_MC) is clear.

Flag writers in this mission: set local flag 12 (Nuked_MC) at [Nuke_MC_True (094CE89C)](#trigger-094ce89c); clear local flag 12 (Nuked_MC) at [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_MC_False (094CE7AC)](#trigger-094ce7ac).
2. Preferred Target Cell Set; main setting 340; location/duration field MC.
3. Set local flag 12 (Nuked_MC).
4. Disable [Nuke_MC_True (094CE89C)](#trigger-094ce89c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14232, Events line 14610, Actions line 14988.

<a id="trigger-094ce7ac"></a>

### 304. Nuke_MC_False - 094CE7AC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_MC_True (094CE89C)](#trigger-094ce89c).

Incoming activation links: enable from [Nuke_MB_False (094CE98C)](#trigger-094ce98c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 12 (Nuked_MC) is set.

Flag writers in this mission: set local flag 12 (Nuked_MC) at [Nuke_MC_True (094CE89C)](#trigger-094ce89c); clear local flag 12 (Nuked_MC) at [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_MC_True (094CE89C)](#trigger-094ce89c).
2. Enable and reset applicable timers for [Nuke_MD_True (094CE6BC)](#trigger-094ce6bc).
3. Enable and reset applicable timers for [Nuke_MD_False (094CE5CC)](#trigger-094ce5cc).
4. Disable [Nuke_MC_False (094CE7AC)](#trigger-094ce7ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14233, Events line 14611, Actions line 14989.

<a id="trigger-094f51ec"></a>

### 305. Nuke_TB_True - 094F51EC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TA_False (094F52DC)](#trigger-094f52dc).

Incoming activation links: enable from [Nuke_TA_False (094F52DC)](#trigger-094f52dc); enable from [Nuke_TA_False2 (0D4FB90C)](#trigger-0d4fb90c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 29 (Player_Owns_TB) is set.

Flag writers in this mission: clear local flag 29 (Player_Owns_TB) at [PlantTB_Gone (06B3ED3C)](#trigger-06b3ed3c); set local flag 29 (Player_Owns_TB) at [Player_Takes_TB (094D681C)](#trigger-094d681c); clear local flag 29 (Player_Owns_TB) at [Yuri_Takes_TB (094D672C)](#trigger-094d672c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TB_False (094F50FC)](#trigger-094f50fc).
2. Disable [Nuke_TB_False2 (0D4FB81C)](#trigger-0d4fb81c).
3. Preferred Target Cell Set; main setting 521; location/duration field TB.
4. Set local flag 50 (Nuked_PPTB).
5. Disable [Nuke_TB_True (094F51EC)](#trigger-094f51ec).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14234, Events line 14612, Actions line 14990.

<a id="trigger-094f50fc"></a>

### 306. Nuke_TB_False - 094F50FC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TB_True (094F51EC)](#trigger-094f51ec).

Incoming activation links: enable from [Nuke_TA_False (094F52DC)](#trigger-094f52dc); enable from [Nuke_TA_False2 (0D4FB90C)](#trigger-0d4fb90c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 29 (Player_Owns_TB) is clear.

Flag writers in this mission: clear local flag 29 (Player_Owns_TB) at [PlantTB_Gone (06B3ED3C)](#trigger-06b3ed3c); set local flag 29 (Player_Owns_TB) at [Player_Takes_TB (094D681C)](#trigger-094d681c); clear local flag 29 (Player_Owns_TB) at [Yuri_Takes_TB (094D672C)](#trigger-094d672c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TB_True (094F51EC)](#trigger-094f51ec).
2. Disable [Nuke_TB_False2 (0D4FB81C)](#trigger-0d4fb81c).
3. Enable and reset applicable timers for [Nuke_TC_True (094F6F3C)](#trigger-094f6f3c).
4. Enable and reset applicable timers for [Nuke_TC_False (094F6E4C)](#trigger-094f6e4c).
5. Enable and reset applicable timers for [Nuke_TC_False2 (0D4FB72C)](#trigger-0d4fb72c).
6. Disable [Nuke_TB_False (094F50FC)](#trigger-094f50fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14235, Events line 14613, Actions line 14991.

<a id="trigger-0d4fb81c"></a>

### 307. Nuke_TB_False2 - 0D4FB81C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TA_False2 (0D4FB90C)](#trigger-0d4fb90c).

Incoming activation links: enable from [Nuke_TA_False (094F52DC)](#trigger-094f52dc); enable from [Nuke_TA_False2 (0D4FB90C)](#trigger-0d4fb90c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 50 (Nuked_PPTB) is set.

Flag writers in this mission: set local flag 50 (Nuked_PPTB) at [Nuke_TB_True (094F51EC)](#trigger-094f51ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TB_True (094F51EC)](#trigger-094f51ec).
2. Disable [Nuke_TB_False (094F50FC)](#trigger-094f50fc).
3. Enable and reset applicable timers for [Nuke_TC_True (094F6F3C)](#trigger-094f6f3c).
4. Enable and reset applicable timers for [Nuke_TC_False (094F6E4C)](#trigger-094f6e4c).
5. Enable and reset applicable timers for [Nuke_TC_False2 (0D4FB72C)](#trigger-0d4fb72c).
6. Disable [Nuke_TB_False2 (0D4FB81C)](#trigger-0d4fb81c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14236, Events line 14614, Actions line 14992.

<a id="trigger-094f6c6c"></a>

### 308. Nuke_TD_False - 094F6C6C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TD_True (094F6D5C)](#trigger-094f6d5c).

Incoming activation links: enable from [Nuke_TC_False2 (0D4FB72C)](#trigger-0d4fb72c); enable from [Nuke_TC_False (094F6E4C)](#trigger-094f6e4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 31 (Player_Owns_TD) is clear.

Flag writers in this mission: clear local flag 31 (Player_Owns_TD) at [PlantTD_Gone (0B30790C)](#trigger-0b30790c); set local flag 31 (Player_Owns_TD) at [Player_Takes_TD (0B30121C)](#trigger-0b30121c); clear local flag 31 (Player_Owns_TD) at [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TD_True (094F6D5C)](#trigger-094f6d5c).
2. Disable [Nuke_TD_False2 (0D4FB63C)](#trigger-0d4fb63c).
3. Enable and reset applicable timers for [Nuke_TE_True (094F6B7C)](#trigger-094f6b7c).
4. Enable and reset applicable timers for [Nuke_TE_False (094F6A8C)](#trigger-094f6a8c).
5. Enable and reset applicable timers for [Nuke_TE_False2 (0D4FB54C)](#trigger-0d4fb54c).
6. Disable [Nuke_TD_False (094F6C6C)](#trigger-094f6c6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14237, Events line 14615, Actions line 14993.

<a id="trigger-0d4fb72c"></a>

### 309. Nuke_TC_False2 - 0D4FB72C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TB_False2 (0D4FB81C)](#trigger-0d4fb81c).

Incoming activation links: enable from [Nuke_TB_False (094F50FC)](#trigger-094f50fc); enable from [Nuke_TB_False2 (0D4FB81C)](#trigger-0d4fb81c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 51 (Nuked_PPTC) is set.

Flag writers in this mission: set local flag 51 (Nuked_PPTC) at [Nuke_TC_True (094F6F3C)](#trigger-094f6f3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TC_True (094F6F3C)](#trigger-094f6f3c).
2. Disable [Nuke_TC_False (094F6E4C)](#trigger-094f6e4c).
3. Enable and reset applicable timers for [Nuke_TD_True (094F6D5C)](#trigger-094f6d5c).
4. Enable and reset applicable timers for [Nuke_TD_False (094F6C6C)](#trigger-094f6c6c).
5. Enable and reset applicable timers for [Nuke_TD_False2 (0D4FB63C)](#trigger-0d4fb63c).
6. Disable [Nuke_TC_False2 (0D4FB72C)](#trigger-0d4fb72c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14238, Events line 14616, Actions line 14994.

<a id="trigger-094f6d5c"></a>

### 310. Nuke_TD_True - 094F6D5C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TC_False (094F6E4C)](#trigger-094f6e4c).

Incoming activation links: enable from [Nuke_TC_False2 (0D4FB72C)](#trigger-0d4fb72c); enable from [Nuke_TC_False (094F6E4C)](#trigger-094f6e4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 31 (Player_Owns_TD) is set.

Flag writers in this mission: clear local flag 31 (Player_Owns_TD) at [PlantTD_Gone (0B30790C)](#trigger-0b30790c); set local flag 31 (Player_Owns_TD) at [Player_Takes_TD (0B30121C)](#trigger-0b30121c); clear local flag 31 (Player_Owns_TD) at [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TD_False (094F6C6C)](#trigger-094f6c6c).
2. Disable [Nuke_TD_False2 (0D4FB63C)](#trigger-0d4fb63c).
3. Preferred Target Cell Set; main setting 523; location/duration field TD.
4. Set local flag 52 (Nuked_PPTD).
5. Disable [Nuke_TD_True (094F6D5C)](#trigger-094f6d5c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14239, Events line 14617, Actions line 14995.

<a id="trigger-094ce6bc"></a>

### 311. Nuke_MD_True - 094CE6BC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_MC_False (094CE7AC)](#trigger-094ce7ac).

Incoming activation links: enable from [Nuke_MC_False (094CE7AC)](#trigger-094ce7ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 9 (Nuked_MD) is clear.

Flag writers in this mission: set local flag 9 (Nuked_MD) at [Nuke_MD_True (094CE6BC)](#trigger-094ce6bc); clear local flag 9 (Nuked_MD) at [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_MD_False (094CE5CC)](#trigger-094ce5cc).
2. Preferred Target Cell Set; main setting 341; location/duration field MD.
3. Set local flag 9 (Nuked_MD).
4. Disable [Nuke_MD_True (094CE6BC)](#trigger-094ce6bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14240, Events line 14618, Actions line 14996.

<a id="trigger-094ce5cc"></a>

### 312. Nuke_MD_False - 094CE5CC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_MD_True (094CE6BC)](#trigger-094ce6bc).

Incoming activation links: enable from [Nuke_MC_False (094CE7AC)](#trigger-094ce7ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 9 (Nuked_MD) is set.

Flag writers in this mission: set local flag 9 (Nuked_MD) at [Nuke_MD_True (094CE6BC)](#trigger-094ce6bc); clear local flag 9 (Nuked_MD) at [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_MD_True (094CE6BC)](#trigger-094ce6bc).
2. Enable and reset applicable timers for [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc).
3. Disable [Nuke_MD_False (094CE5CC)](#trigger-094ce5cc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14241, Events line 14619, Actions line 14997.

<a id="trigger-094f6f3c"></a>

### 313. Nuke_TC_True - 094F6F3C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TB_False (094F50FC)](#trigger-094f50fc).

Incoming activation links: enable from [Nuke_TB_False (094F50FC)](#trigger-094f50fc); enable from [Nuke_TB_False2 (0D4FB81C)](#trigger-0d4fb81c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 30 (Player_Owns_TC) is set.

Flag writers in this mission: clear local flag 30 (Player_Owns_TC) at [PlantTC_Gone (094F204C)](#trigger-094f204c); set local flag 30 (Player_Owns_TC) at [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec); clear local flag 30 (Player_Owns_TC) at [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TC_False (094F6E4C)](#trigger-094f6e4c).
2. Disable [Nuke_TC_False2 (0D4FB72C)](#trigger-0d4fb72c).
3. Preferred Target Cell Set; main setting 522; location/duration field TC.
4. Set local flag 51 (Nuked_PPTC).
5. Disable [Nuke_TC_True (094F6F3C)](#trigger-094f6f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14242, Events line 14620, Actions line 14998.

<a id="trigger-094f6e4c"></a>

### 314. Nuke_TC_False - 094F6E4C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_TC_True (094F6F3C)](#trigger-094f6f3c).

Incoming activation links: enable from [Nuke_TB_False (094F50FC)](#trigger-094f50fc); enable from [Nuke_TB_False2 (0D4FB81C)](#trigger-0d4fb81c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 30 (Player_Owns_TC) is clear.

Flag writers in this mission: clear local flag 30 (Player_Owns_TC) at [PlantTC_Gone (094F204C)](#trigger-094f204c); set local flag 30 (Player_Owns_TC) at [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec); clear local flag 30 (Player_Owns_TC) at [Yuri_Takes_TC (06BDA1DC)](#trigger-06bda1dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Nuke_TC_True (094F6F3C)](#trigger-094f6f3c).
2. Disable [Nuke_TC_False2 (0D4FB72C)](#trigger-0d4fb72c).
3. Enable and reset applicable timers for [Nuke_TD_True (094F6D5C)](#trigger-094f6d5c).
4. Enable and reset applicable timers for [Nuke_TD_False (094F6C6C)](#trigger-094f6c6c).
5. Enable and reset applicable timers for [Nuke_TD_False2 (0D4FB63C)](#trigger-0d4fb63c).
6. Disable [Nuke_TC_False (094F6E4C)](#trigger-094f6e4c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14243, Events line 14621, Actions line 14999.

<a id="trigger-094ce4dc"></a>

### 315. Nuke_ME_True - 094CE4DC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_MD_False (094CE5CC)](#trigger-094ce5cc).

Incoming activation links: enable from [Nuke_MD_False (094CE5CC)](#trigger-094ce5cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Preferred Target Cell Set; main setting 342; location/duration field ME.
2. Clear local flag 13 (Nuked_MA).
3. Clear local flag 16 (Nuked_MB).
4. Clear local flag 12 (Nuked_MC).
5. Clear local flag 9 (Nuked_MD).
6. Disable [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14244, Events line 14622, Actions line 15000.

<a id="trigger-0964f7ac"></a>

### 316. Nuke_Engineer_AA - 0964F7AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlantAA_Nuked (097729DC)](#trigger-097729dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_AA_Engineer (0BA3C0EC)](all03umd-teams.md#team-0ba3c0ec).
2. Disable [Nuke_Engineer_AA (0964F7AC)](#trigger-0964f7ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14245, Events line 14623, Actions line 15001.

<a id="trigger-0964b7ac"></a>

### 317. Nuke_Engineer_AB - 0964B7AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_Engineer_AA (0964F7AC)](#trigger-0964f7ac).

Incoming activation links: enable from [PlantAB_Nuked (097725DC)](#trigger-097725dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_AB_Engineer (095C2E1C)](all03umd-teams.md#team-095c2e1c).
2. Disable [Nuke_Engineer_AB (0964B7AC)](#trigger-0964b7ac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14246, Events line 14624, Actions line 15002.

<a id="trigger-0976e03c"></a>

### 318. Nuke_Engineer_TF - 0976E03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_Engineer_TE (0964B30C)](#trigger-0964b30c).

Incoming activation links: enable from [PlantTF_Nuked (09777F3C)](#trigger-09777f3c).

Attached scope: tag definitions 0964F6CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TF_Engineer (0C85E1FC)](all03umd-teams.md#team-0c85e1fc).
2. Disable [Nuke_Engineer_TF (0976E03C)](#trigger-0976e03c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14247, Events line 14625, Actions line 15003.

<a id="trigger-0964b30c"></a>

### 319. Nuke_Engineer_TE - 0964B30C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_Engineer_TD (0964B62C)](#trigger-0964b62c).

Incoming activation links: enable from [PlantTE_Nuked (097732BC)](#trigger-097732bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TE_Engineer (0C94F90C)](all03umd-teams.md#team-0c94f90c).
2. Disable [Nuke_Engineer_TE (0964B30C)](#trigger-0964b30c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14248, Events line 14626, Actions line 15004.

<a id="trigger-0964b62c"></a>

### 320. Nuke_Engineer_TD - 0964B62C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_Engineer_TC (0964843C)](#trigger-0964843c).

Incoming activation links: enable from [PlantTD_Nuked (097735DC)](#trigger-097735dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TD_Engineer (0C2E054C)](all03umd-teams.md#team-0c2e054c).
2. Disable [Nuke_Engineer_TD (0964B62C)](#trigger-0964b62c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14249, Events line 14627, Actions line 15005.

<a id="trigger-0964843c"></a>

### 321. Nuke_Engineer_TC - 0964843C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_Engineer_TB (0964875C)](#trigger-0964875c).

Incoming activation links: enable from [PlantTC_Nuked (097738FC)](#trigger-097738fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TC_Engineer (0C94E2DC)](all03umd-teams.md#team-0c94e2dc).
2. Disable [Nuke_Engineer_TC (0964843C)](#trigger-0964843c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14250, Events line 14628, Actions line 15006.

<a id="trigger-0964875c"></a>

### 322. Nuke_Engineer_TB - 0964875C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_Engineer_TA (09648A7C)](#trigger-09648a7c).

Incoming activation links: enable from [PlantTB_Nuked (09773C1C)](#trigger-09773c1c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TB_Engineer (0C886EFC)](all03umd-teams.md#team-0c886efc).
2. Disable [Nuke_Engineer_TB (0964875C)](#trigger-0964875c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14251, Events line 14629, Actions line 15007.

<a id="trigger-09648a7c"></a>

### 323. Nuke_Engineer_TA - 09648A7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_Engineer_AD (09648D9C)](#trigger-09648d9c).

Incoming activation links: enable from [PlantTA_Nuked (09773F3C)](#trigger-09773f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_TA_Engineer (0C88543C)](all03umd-teams.md#team-0c88543c).
2. Disable [Nuke_Engineer_TA (09648A7C)](#trigger-09648a7c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14252, Events line 14630, Actions line 15008.

<a id="trigger-09648d9c"></a>

### 324. Nuke_Engineer_AD - 09648D9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_Engineer_AB (0964B7AC)](#trigger-0964b7ac).

Incoming activation links: enable from [PlantAD_Nuked (097722BC)](#trigger-097722bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_AD_Engineer (0C11C0EC)](all03umd-teams.md#team-0c11c0ec).
2. Disable [Nuke_Engineer_AD (09648D9C)](#trigger-09648d9c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14253, Events line 14631, Actions line 15009.

<a id="trigger-094ce3ec"></a>

### 325. Nuke_ME_False - 094CE3EC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Nuke_ME_True (094CE4DC)](#trigger-094ce4dc).

Attached scope: tag definitions 094CEC5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

No event entries. Reachability requires separate runtime interpretation.

**Then perform these actions in order:**

No action entries.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14254, Events line 14632, Actions line 15010.

<a id="trigger-094de72c"></a>

### 326. Nuke_Timer_PP - 094DE72C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Nuke_Timer_Misc (094DE55C)](#trigger-094de55c).

Attached scope: tag definitions 094DE64C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 333 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Preferred Target Cell Clear; main setting 0.
2. Enable and reset applicable timers for [Nuke_AA_True (094F5C2C)](#trigger-094f5c2c).
3. Enable and reset applicable timers for [Nuke_AA_False (094F5A5C)](#trigger-094f5a5c).
4. Enable and reset applicable timers for [Nuke_AA_False2 (043A430C)](#trigger-043a430c).
5. Enable and reset applicable timers for [Nuke_Timer_Misc (094DE55C)](#trigger-094de55c).
6. Disable [Nuke_Timer_PP (094DE72C)](#trigger-094de72c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14255, Events line 14633, Actions line 15011.

<a id="trigger-094de55c"></a>

### 327. Nuke_Timer_Misc - 094DE55C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Nuke_Timer_PP (094DE72C)](#trigger-094de72c).

Attached scope: tag definitions 094DE47C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 333 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_MA_True (094CED3C)](#trigger-094ced3c).
2. Enable and reset applicable timers for [Nuke_MA_False (094CEB6C)](#trigger-094ceb6c).
3. Enable and reset applicable timers for [Nuke_Timer_PP (094DE72C)](#trigger-094de72c).
4. Disable [Nuke_Timer_Misc (094DE55C)](#trigger-094de55c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14256, Events line 14634, Actions line 15012.

<a id="trigger-0d663a4c"></a>

### 328. Enable_Plant_AA - 0D663A4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D66328C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantAA_Gone (093BEEDC)](#trigger-093beedc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14257, Events line 14635, Actions line 15013.

<a id="trigger-0d664f3c"></a>

### 329. Enable_Plant_AB - 0D664F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D664CFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantAB_Gone (093BE2FC)](#trigger-093be2fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14258, Events line 14636, Actions line 15014.

<a id="trigger-0d664c0c"></a>

### 330. Enable_Plant_AC - 0D664C0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D6649CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantAC_Gone (093BFDDC)](#trigger-093bfddc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14259, Events line 14637, Actions line 15015.

<a id="trigger-0d6648dc"></a>

### 331. Enable_Plant_AD - 0D6648DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D66469C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantAD_Gone (093BF8FC)](#trigger-093bf8fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14260, Events line 14638, Actions line 15016.

<a id="trigger-0d6645ac"></a>

### 332. Enable_Plant_TA - 0D6645AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D66436C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantTA_Gone (094E203C)](#trigger-094e203c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14261, Events line 14639, Actions line 15017.

<a id="trigger-0d66427c"></a>

### 333. Enable_Plant_TB - 0D66427C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D66403C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantTB_Gone (06B3ED3C)](#trigger-06b3ed3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14262, Events line 14640, Actions line 15018.

<a id="trigger-0d665f3c"></a>

### 334. Enable_Plant_TC - 0D665F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D665CFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantTC_Gone (094F204C)](#trigger-094f204c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14263, Events line 14641, Actions line 15019.

<a id="trigger-0d665c0c"></a>

### 335. Enable_Plant_TD - 0D665C0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D6659CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantTD_Gone (0B30790C)](#trigger-0b30790c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14264, Events line 14642, Actions line 15020.

<a id="trigger-0d6658dc"></a>

### 336. Enable_Plant_TE - 0D6658DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D66569C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantTE_Gone (045D673C)](#trigger-045d673c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14265, Events line 14643, Actions line 15021.

<a id="trigger-0d6655ac"></a>

### 337. Enable_Plant_TF - 0D6655AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D66536C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlantTF_Gone (09881BAC)](#trigger-09881bac).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14266, Events line 14644, Actions line 15022.

<a id="trigger-098610fc"></a>

### 338. Bring_In_Nuke_Guard - 098610FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Base_Defense_Gone (0986428C)](#trigger-0986428c).

Attached scope: tag definitions 0986451C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Nuke_Guard (0988192C)](all03umd-teams.md#team-0988192c).
2. Disable [Bring_In_Nuke_Guard (098610FC)](#trigger-098610fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14267, Events line 14645, Actions line 15023.

<a id="trigger-0986428c"></a>

### 339. Base_Defense_Gone - 0986428C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Tank (YTNK), owner YuriCountry, cell (58, 96), tag 0986404C, persistence mode 1; Gattling Tank (YTNK), owner YuriCountry, cell (58, 90), tag 0986404C, persistence mode 1; Gattling Tank (YTNK), owner YuriCountry, cell (58, 93), tag 0986404C, persistence mode 1; Lasher Light Tank (LTNK), owner YuriCountry, cell (60, 95), tag 0986404C, persistence mode 1; Lasher Light Tank (LTNK), owner YuriCountry, cell (60, 92), tag 0986404C, persistence mode 1; Yuri Clone (YURI), owner YuriCountry, cell (56, 88), tag 0986404C, persistence mode 1; Yuri Clone (YURI), owner YuriCountry, cell (56, 86), tag 0986404C, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Bring_In_Nuke_Guard (098610FC)](#trigger-098610fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14268, Events line 14646, Actions line 15024.

<a id="trigger-097729dc"></a>

### 340. PlantAA_Nuked - 097729DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Player_Takes_AA (0945ABBC)](#trigger-0945abbc).

Attached scope: CAPOWRAA, owner Americans, cell (115, 72), tag 093BE6AC, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_Engineer_AA (0964F7AC)](#trigger-0964f7ac).
2. Disable [PlantAA_Nuked (097729DC)](#trigger-097729dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14269, Events line 14647, Actions line 15025.

<a id="trigger-097725dc"></a>

### 341. PlantAB_Nuked - 097725DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_AB (0CF8110C)](#trigger-0cf8110c).

Attached scope: CAPOWRAB, owner Americans, cell (127, 96), tag 093BFF4C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_Engineer_AB (0964B7AC)](#trigger-0964b7ac).
2. Disable [PlantAB_Nuked (097725DC)](#trigger-097725dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14270, Events line 14648, Actions line 15026.

<a id="trigger-097722bc"></a>

### 342. PlantAD_Nuked - 097722BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_AD (094D9C5C)](#trigger-094d9c5c).

Attached scope: CAPOWRAD, owner Americans, cell (124, 123), tag 093BF54C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_Engineer_AD (09648D9C)](#trigger-09648d9c).
2. Disable [PlantAD_Nuked (097722BC)](#trigger-097722bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14271, Events line 14649, Actions line 15027.

<a id="trigger-09773f3c"></a>

### 343. PlantTA_Nuked - 09773F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Player_Takes_TA (094E3ACC)](#trigger-094e3acc).

Attached scope: CAPOWRTA, owner YuriCountry, cell (101, 58), tag 094E3D2C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_Engineer_TA (09648A7C)](#trigger-09648a7c).
2. Disable [PlantTA_Nuked (09773F3C)](#trigger-09773f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14272, Events line 14650, Actions line 15028.

<a id="trigger-09773c1c"></a>

### 344. PlantTB_Nuked - 09773C1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_TB (094D672C)](#trigger-094d672c).

Attached scope: CAPOWRTB, owner YuriCountry, cell (90, 72), tag 06B3EC5C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_Engineer_TB (0964875C)](#trigger-0964875c).
2. Disable [PlantTB_Nuked (09773C1C)](#trigger-09773c1c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14273, Events line 14651, Actions line 15029.

<a id="trigger-097738fc"></a>

### 345. PlantTC_Nuked - 097738FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Player_Takes_TC (06BDA0EC)](#trigger-06bda0ec).

Attached scope: CAPOWRTC, owner YuriCountry, cell (90, 107), tag 094F3A1C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_Engineer_TC (0964843C)](#trigger-0964843c).
2. Disable [PlantTC_Nuked (097738FC)](#trigger-097738fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14274, Events line 14652, Actions line 15030.

<a id="trigger-097735dc"></a>

### 346. PlantTD_Nuked - 097735DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_TD (0B30112C)](#trigger-0b30112c).

Attached scope: CAPOWRTD, owner YuriCountry, cell (109, 109), tag 0B30732C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_Engineer_TD (0964B62C)](#trigger-0964b62c).
2. Disable [PlantTD_Nuked (097735DC)](#trigger-097735dc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14275, Events line 14653, Actions line 15031.

<a id="trigger-097732bc"></a>

### 347. PlantTE_Nuked - 097732BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Yuri_Takes_TE (045C3E3C)](#trigger-045c3e3c).

Attached scope: CAPOWRTE, owner YuriCountry, cell (84, 134), tag 045D5ABC, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_Engineer_TE (0964B30C)](#trigger-0964b30c).
2. Disable [PlantTE_Nuked (097732BC)](#trigger-097732bc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14276, Events line 14654, Actions line 15032.

<a id="trigger-09777f3c"></a>

### 348. PlantTF_Nuked - 09777F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [PlantTF_Gone (09881BAC)](#trigger-09881bac).

Attached scope: CAPOWRTF, owner YuriCountry, cell (65, 113), tag 0C13356C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Nuke_Engineer_TF (0976E03C)](#trigger-0976e03c).
2. Disable [PlantTF_Nuked (09777F3C)](#trigger-09777f3c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14277, Events line 14655, Actions line 15033.

<a id="trigger-0b9c16cc"></a>

### 349. Water1 - 0B9C16CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B9C58CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WavesLake at waypoint 234 (cell 67, 83).
2. Play sound _Amb_OceanLight at waypoint 235 (cell 75, 88).
3. Play sound _Amb_WavesLake at waypoint 236 (cell 84, 84).
4. Play sound _Amb_OceanLight at waypoint 237 (cell 73, 73).
5. Play sound _Amb_WavesLake at waypoint 238 (cell 79, 67).
6. Play sound _Amb_OceanLight at waypoint 239 (cell 60, 69).
7. Play sound _Amb_WavesLake at waypoint 240 (cell 70, 56).
8. Play sound _Amb_OceanHeavy at waypoint 241 (cell 91, 140).
9. Play sound _Amb_OceanHeavy at waypoint 242 (cell 105, 143).
10. Play sound _Amb_OceanHeavy at waypoint 243 (cell 113, 154).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14278, Events line 14656, Actions line 15034.

<a id="trigger-0b9b73dc"></a>

### 350. Birds1 - 0B9B73DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsTemperate1 at waypoint 244 (cell 135, 146).
2. Play sound _Amb_BirdsTemperate2 at waypoint 245 (cell 128, 152).
3. Play sound _Amb_BirdsPark at waypoint 246 (cell 109, 117).
4. Play sound _Amb_BirdsTemperate1 at waypoint 247 (cell 101, 126).
5. Play sound _Amb_BirdsTemperate2 at waypoint 248 (cell 116, 146).
6. Play sound _Amb_BirdsPark at waypoint 249 (cell 108, 135).
7. Play sound _Amb_BirdsTemperate1 at waypoint 250 (cell 95, 116).
8. Play sound _Amb_BirdsTemperate2 at waypoint 251 (cell 87, 118).
9. Play sound _Amb_BirdsPark at waypoint 252 (cell 81, 133).
10. Play sound _Amb_BirdsTemperate1 at waypoint 253 (cell 143, 126).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14279, Events line 14657, Actions line 15035.

<a id="trigger-0ba3772c"></a>

### 351. Birds2 - 0BA3772C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Birds1 (0B9B73DC)](#trigger-0b9b73dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsTemperate2 at waypoint 254 (cell 101, 106).
2. Play sound _Amb_BirdsPark at waypoint 255 (cell 103, 89).
3. Play sound _Amb_BirdsTemperate1 at waypoint 256 (cell 105, 68).
4. Play sound _Amb_BirdsTemperate2 at waypoint 257 (cell 88, 66).
5. Play sound _Amb_BirdsPark at waypoint 258 (cell 82, 52).
6. Play sound _Amb_BirdsTemperate1 at waypoint 259 (cell 103, 81).
7. Play sound _Amb_BirdsTemperate2 at waypoint 260 (cell 125, 103).
8. Play sound _Amb_BirdsPark at waypoint 261 (cell 89, 95).
9. Play sound _Amb_BirdsTemperate1 at waypoint 262 (cell 51, 105).
10. Play sound _Amb_BirdsTemperate2 at waypoint 263 (cell 60, 85).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14280, Events line 14658, Actions line 15036.

<a id="trigger-0b9bf76c"></a>

### 352. Birds3 - 0B9BF76C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Birds2 (0BA3772C)](#trigger-0ba3772c).

Attached scope: tag definitions 0B9AF1EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsTemperate1 at waypoint 264 (cell 58, 103).
2. Play sound _Amb_BirdsTemperate2 at waypoint 265 (cell 62, 94).
3. Play sound _Amb_BirdsPark at waypoint 266 (cell 51, 74).
4. Play sound _Amb_BirdsTemperate1 at waypoint 267 (cell 98, 134).
5. Play sound _Amb_BirdsTemperate2 at waypoint 268 (cell 149, 111).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14281, Events line 14659, Actions line 15037.

<a id="trigger-0b9c321c"></a>

### 353. Traffic1 - 0B9C321C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 269 (cell 111, 132).
2. Play sound _Amb_UrbanMurmur2 at waypoint 270 (cell 120, 124).
3. Play sound _Amb_Traffic at waypoint 271 (cell 115, 112).
4. Play sound _Amb_UrbanMurmur1 at waypoint 272 (cell 94, 130).
5. Play sound _Amb_UrbanMurmur2 at waypoint 273 (cell 80, 118).
6. Play sound _Amb_Traffic at waypoint 274 (cell 78, 131).
7. Play sound _Amb_UrbanMurmur1 at waypoint 275 (cell 70, 120).
8. Play sound _Amb_UrbanMurmur2 at waypoint 276 (cell 59, 109).
9. Play sound _Amb_Traffic at waypoint 277 (cell 64, 101).
10. Play sound _Amb_UrbanMurmur1 at waypoint 278 (cell 83, 102).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14282, Events line 14660, Actions line 15038.

<a id="trigger-0b9b78bc"></a>

### 354. Traffic2 - 0B9B78BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Traffic1 (0B9C321C)](#trigger-0b9c321c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur2 at waypoint 279 (cell 99, 112).
2. Play sound _Amb_Traffic at waypoint 280 (cell 112, 104).
3. Play sound _Amb_UrbanMurmur1 at waypoint 281 (cell 138, 128).
4. Play sound _Amb_UrbanMurmur2 at waypoint 282 (cell 155, 122).
5. Play sound _Amb_Traffic at waypoint 283 (cell 140, 108).
6. Play sound _Amb_UrbanMurmur1 at waypoint 284 (cell 133, 92).
7. Play sound _Amb_UrbanMurmur2 at waypoint 285 (cell 118, 95).
8. Play sound _Amb_Traffic at waypoint 286 (cell 92, 78).
9. Play sound _Amb_UrbanMurmur1 at waypoint 287 (cell 106, 78).
10. Play sound _Amb_UrbanMurmur2 at waypoint 288 (cell 120, 78).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14283, Events line 14661, Actions line 15039.

<a id="trigger-0b9c220c"></a>

### 355. Traffic3 - 0B9C220C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Traffic2 (0B9B78BC)](#trigger-0b9b78bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_Traffic at waypoint 289 (cell 133, 78).
2. Play sound _Amb_UrbanMurmur1 at waypoint 290 (cell 143, 92).
3. Play sound _Amb_UrbanMurmur2 at waypoint 291 (cell 148, 106).
4. Play sound _Amb_Traffic at waypoint 292 (cell 154, 97).
5. Play sound _Amb_UrbanMurmur1 at waypoint 293 (cell 155, 111).
6. Play sound _Amb_UrbanMurmur2 at waypoint 294 (cell 146, 122).
7. Play sound _Amb_Traffic at waypoint 295 (cell 127, 116).
8. Play sound _Amb_UrbanMurmur1 at waypoint 296 (cell 97, 66).
9. Play sound _Amb_UrbanMurmur2 at waypoint 297 (cell 86, 58).
10. Play sound _Amb_Traffic at waypoint 298 (cell 94, 52).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14284, Events line 14662, Actions line 15040.

<a id="trigger-0b9c34bc"></a>

### 356. Traffic4 - 0B9C34BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Traffic3 (0B9C220C)](#trigger-0b9c220c).

Attached scope: tag definitions 0B9C244C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur2 at waypoint 299 (cell 106, 55).
2. Play sound _Amb_Traffic at waypoint 300 (cell 109, 64).
3. Play sound _Amb_UrbanMurmur1 at waypoint 301 (cell 121, 65).
4. Play sound _Amb_UrbanMurmur2 at waypoint 302 (cell 93, 103).
5. Play sound _Amb_Traffic at waypoint 303 (cell 86, 112).
6. Play sound _Amb_UrbanMurmur1 at waypoint 304 (cell 62, 120).
7. Play sound _Amb_UrbanMurmur2 at waypoint 305 (cell 121, 142).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14285, Events line 14663, Actions line 15041.

<a id="trigger-09794dfc"></a>

### 357. French_Gone1 - 09794DFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0979542C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 2 (country/type FRENCH; placed owner French).

**Then perform these actions in order:**

1. Supply reinforcement team 0 (template not recovered locally).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14286, Events line 14664, Actions line 15042.

<a id="trigger-06bb1c6c"></a>

### 358. Paradrop_WC1 - 06BB1C6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Paradrop_WC3 (06BB114C)](#trigger-06bb114c); enable from [Start_Paradrop (096ED24C)](#trigger-096ed24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Paradrop_WC1 (045EA05C)](all03umd-teams.md#team-045ea05c).
2. Enable and reset applicable timers for [Paradrop_Infantry1 (06BB15FC)](#trigger-06bb15fc).
3. Disable [Paradrop_WC1 (06BB1C6C)](#trigger-06bb1c6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14287, Events line 14665, Actions line 15043.

<a id="trigger-06bb15fc"></a>

### 359. Paradrop_Infantry1 - 06BB15FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Paradrop_WC1 (06BB1C6C)](#trigger-06bb1c6c).

Incoming activation links: enable from [Paradrop_WC1 (06BB1C6C)](#trigger-06bb1c6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Infantry_Hunter_1 (045E812C)](all03umd-teams.md#team-045e812c).
2. Enable and reset applicable timers for [Paradrop_Vehicle1 (06BB150C)](#trigger-06bb150c).
3. Disable [Paradrop_Infantry1 (06BB15FC)](#trigger-06bb15fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14288, Events line 14666, Actions line 15044.

<a id="trigger-06bb150c"></a>

### 360. Paradrop_Vehicle1 - 06BB150C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Paradrop_Infantry1 (06BB15FC)](#trigger-06bb15fc).

Incoming activation links: enable from [Paradrop_Infantry1 (06BB15FC)](#trigger-06bb15fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Vehicle_Hunter1 (096F77AC)](all03umd-teams.md#team-096f77ac).
2. Enable and reset applicable timers for [Paradrop_WC2 (06BB141C)](#trigger-06bb141c).
3. Disable [Paradrop_Vehicle1 (06BB150C)](#trigger-06bb150c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14289, Events line 14667, Actions line 15045.

<a id="trigger-06bb141c"></a>

### 361. Paradrop_WC2 - 06BB141C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Paradrop_Vehicle1 (06BB150C)](#trigger-06bb150c).

Incoming activation links: enable from [Paradrop_Vehicle1 (06BB150C)](#trigger-06bb150c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Paradrop_WC2 (0968684C)](all03umd-teams.md#team-0968684c).
2. Enable and reset applicable timers for [Paradrop_Infantry2 (06BB132C)](#trigger-06bb132c).
3. Disable [Paradrop_WC2 (06BB141C)](#trigger-06bb141c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14290, Events line 14668, Actions line 15046.

<a id="trigger-06bb132c"></a>

### 362. Paradrop_Infantry2 - 06BB132C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Paradrop_WC2 (06BB141C)](#trigger-06bb141c).

Incoming activation links: enable from [Paradrop_WC2 (06BB141C)](#trigger-06bb141c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Infantry_Hunter2 (045EA43C)](all03umd-teams.md#team-045ea43c).
2. Enable and reset applicable timers for [Paradrop_Vehicle2 (06BB123C)](#trigger-06bb123c).
3. Disable [Paradrop_Infantry2 (06BB132C)](#trigger-06bb132c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14291, Events line 14669, Actions line 15047.

<a id="trigger-06bb123c"></a>

### 363. Paradrop_Vehicle2 - 06BB123C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Paradrop_Infantry2 (06BB132C)](#trigger-06bb132c).

Incoming activation links: enable from [Paradrop_Infantry2 (06BB132C)](#trigger-06bb132c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Vehicle_Hunter2 (09718EFC)](all03umd-teams.md#team-09718efc).
2. Enable and reset applicable timers for [Paradrop_WC3 (06BB114C)](#trigger-06bb114c).
3. Disable [Paradrop_Vehicle2 (06BB123C)](#trigger-06bb123c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14292, Events line 14670, Actions line 15048.

<a id="trigger-06bb114c"></a>

### 364. Paradrop_WC3 - 06BB114C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Paradrop_Vehicle2 (06BB123C)](#trigger-06bb123c).

Incoming activation links: enable from [Paradrop_Vehicle2 (06BB123C)](#trigger-06bb123c).

Attached scope: tag definitions 06BB16EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Paradrop_WC3 (06BE73DC)](all03umd-teams.md#team-06be73dc).
2. Enable and reset applicable timers for [Paradrop_WC1 (06BB1C6C)](#trigger-06bb1c6c).
3. Disable [Paradrop_WC3 (06BB114C)](#trigger-06bb114c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14293, Events line 14671, Actions line 15049.

<a id="trigger-096ed24c"></a>

### 365. Start_Paradrop - 096ED24C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096EC97C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Low Power: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. 720 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Paradrop_WC1 (06BB1C6C)](#trigger-06bb1c6c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14294, Events line 14672, Actions line 15050.

<a id="trigger-0cdc177c"></a>

### 366. Main_Objective - 0CDC177C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CDC11FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Destroy Yuri's Nuclear Silo” (MISSION:KillNuke).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14295, Events line 14673, Actions line 15051.

<a id="trigger-0932bc0c"></a>

### 367. Destroying_City - 0932BC0C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY16), owner Neutral, cell (131, 118), tag 0932B4FC, persistence mode 0; Building (CANEWY07), owner Neutral, cell (136, 120), tag 0932B4FC, persistence mode 0; Building (CATEXS04), owner Neutral, cell (135, 115), tag 0932B4FC, persistence mode 0; Office Building (CATEXS08), owner Neutral, cell (135, 124), tag 0932B4FC, persistence mode 0; Building (CAPARS04), owner Neutral, cell (131, 127), tag 0932B4FC, persistence mode 0; Building (CAPARS05), owner Neutral, cell (128, 127), tag 0932B4FC, persistence mode 0; Building (CAWASH08), owner Neutral, cell (129, 121), tag 0932B4FC, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Play voice notification Mis_xA3_EvaDestroyNuke.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14296, Events line 14674, Actions line 15052.

<a id="trigger-08d63e4c"></a>

### 368. Easy_GiveOil - 08D63E4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: Tech Oil Derrick (CAOILD), owner Special, cell (118, 151), tag 08D6398C, persistence mode 0; Tech Oil Derrick (CAOILD), owner Special, cell (121, 151), tag 08D6398C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14297, Events line 14675, Actions line 15053.

<a id="trigger-089b3d3c"></a>

### 369. EASY_Patrols - 089B3D3C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089B37BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Patrol_AH_JS (089B368C)](all03umd-teams.md#team-089b368c).
2. Supply reinforcement team [Patrol_AI_AJ (089BEC9C)](all03umd-teams.md#team-089bec9c).
3. Supply reinforcement team [Patrol_AK_AL_AM (089B8A3C)](all03umd-teams.md#team-089b8a3c).
4. Supply reinforcement team [Patrol_KK_KO (089B83EC)](all03umd-teams.md#team-089b83ec).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14298, Events line 14676, Actions line 15054.

<a id="trigger-0b005b6c"></a>

### 370. MEDIUM_Patrols - 0B005B6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B00D4AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Patrol_AO_AQ (0AFFD42C)](all03umd-teams.md#team-0affd42c).
2. Supply reinforcement team [Patrol_JT_AH (0B0061AC)](all03umd-teams.md#team-0b0061ac).
3. Supply reinforcement team [Patrol_JN_AT (0B00159C)](all03umd-teams.md#team-0b00159c).
4. Supply reinforcement team [Patrol_KL_AO (0B007DBC)](all03umd-teams.md#team-0b007dbc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14299, Events line 14677, Actions line 15055.

<a id="trigger-0462c35c"></a>

### 371. MEDIUM_Garrison - 0462C35C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0462AAFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Garrision_AJ (0462B5AC)](all03umd-teams.md#team-0462b5ac).
2. Supply reinforcement team [Garrison_AN (0462CEFC)](all03umd-teams.md#team-0462cefc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14300, Events line 14678, Actions line 15056.

<a id="trigger-061a4b5c"></a>

### 372. HARD_Garrison - 061A4B5C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 061A443C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Garrison_AV (061A379C)](all03umd-teams.md#team-061a379c).
2. Supply reinforcement team [Garrison_AW (061A366C)](all03umd-teams.md#team-061a366c).
3. Supply reinforcement team [Garrison_EF (061A353C)](all03umd-teams.md#team-061a353c).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14301, Events line 14679, Actions line 15057.

<a id="trigger-061e7dcc"></a>

### 373. Backdoor1 - 061E7DCC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Backdoor3 (0619F5FC)](#trigger-0619f5fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Backdoor1 (061E6E5C)](all03umd-teams.md#team-061e6e5c).
2. Enable and reset applicable timers for [Backdoor2 (0619F6EC)](#trigger-0619f6ec).
3. Disable [Backdoor1 (061E7DCC)](#trigger-061e7dcc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14302, Events line 14680, Actions line 15058.

<a id="trigger-0619f6ec"></a>

### 374. Backdoor2 - 0619F6EC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backdoor1 (061E7DCC)](#trigger-061e7dcc).

Incoming activation links: enable from [Backdoor1 (061E7DCC)](#trigger-061e7dcc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Backdoor2 (0619684C)](all03umd-teams.md#team-0619684c).
2. Enable and reset applicable timers for [Backdoor3 (0619F5FC)](#trigger-0619f5fc).
3. Disable [Backdoor2 (0619F6EC)](#trigger-0619f6ec).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14303, Events line 14681, Actions line 15059.

<a id="trigger-0619f5fc"></a>

### 375. Backdoor3 - 0619F5FC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Backdoor2 (0619F6EC)](#trigger-0619f6ec).

Incoming activation links: enable from [Backdoor2 (0619F6EC)](#trigger-0619f6ec).

Attached scope: tag definitions 061E784C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Backdoor3 (0619E1BC)](all03umd-teams.md#team-0619e1bc).
2. Enable and reset applicable timers for [Backdoor1 (061E7DCC)](#trigger-061e7dcc).
3. Disable [Backdoor3 (0619F5FC)](#trigger-0619f5fc).

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14304, Events line 14682, Actions line 15060.

<a id="trigger-08f07e1c"></a>

### 376. Find_MachineShop - 08F07E1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tech Machine Shop (CAMACH), owner Special, cell (125, 109), tag 08F07B3C, persistence mode 0.

**Wait for the recorded events:**

1. global flag 12 is clear.
2. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 64 (cell 126, 110).
2. Flash buildings of type CAMACH; duration argument 40.
3. Create radar-event marker type 12 at waypoint 64 (cell 126, 110).
4. Play voice notification Unit_Eva_TechMachShop.
5. Set global flag 12.

Source locator: mapsmd03.mix/all03umd.map; Triggers line 14305, Events line 14683, Actions line 15061.

[All team rosters and ordered plans](all03umd-teams.md) | [All mission overrides](all03umd-overrides.md)
