# Operation: Brain Wash

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov03umd.map. **Effective extracted member:** mapsmd03.mix/sov03umd.map. **Trigger definitions:** 139.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov03umd-teams.md) | [All mission overrides](sov03umd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Soviets |
| Theater | NEWURBAN |
| Map size | 0,0,60,85 |
| Visible local rectangle | 2,30,56,49 |
| Placed vehicles | 70 |
| Placed infantry | 45 |
| Placed structures | 265 |
| Placed aircraft | 0 |
| Team templates | 28 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Allies | 0 | AlliesCountry |
| 1 | GoodGuy1 | 0 | GoodGuy1Country |
| 2 | GoodGuy2 | 0 | GoodGuy2Country |
| 3 | BadGuy1 | 500 | BadGuy1Country |
| 4 | BadGuy2 | 0 | BadGuy2Country |
| 5 | Civie1 | 0 | Civie1Country |
| 6 | Civie2 | 0 | Civie2Country |
| 7 | Civie3 | 0 | Civie3Country |
| 8 | Soviets | 25 | SovietsCountry |
| 9 | YuriCountry | 100 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 0 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | YuriSeesTanya,0 |
| 1 | TanyaRetortYuri,0 |
| 2 | @AA Destroyed,0 |
| 3 | @AB Destroyed,0 |
| 4 | @AC Destroyed,0 |
| 5 | @AD Destroyed,0 |
| 6 | @AE Destroyed,0 |
| 7 | @AF Destroyed,0 |
| 8 | @AG Destroyed,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Player Wins (0BF382DC)](#trigger-0bf382dc) | 3 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets) the winner. |
| [Player Loses (0BEC10EC)](#trigger-0bec10ec) | Destroyed,  Buildings,  All: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).<br>Destroyed,  Units,  All: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets). | Declare owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets) the loser. |

## Every trigger, in file order

<a id="trigger-0d1dacfc"></a>

### 1. SP1.1_Movie_Zofia Brief - 0D1DACFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Setup_Sov03 (0957D3FC)](#trigger-0957d3fc).

Attached scope: tag definitions 0CC24BAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 40.
2. Enable and reset applicable timers for [SP1.1a_VO_ZofiaREBeacon (08C029CC)](#trigger-08c029cc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5077, Events line 5218, Actions line 5359.

<a id="trigger-08c029cc"></a>

### 2. SP1.1a_VO_ZofiaREBeacon - 08C029CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.1_Movie_Zofia Brief (0D1DACFC)](#trigger-0d1dacfc).

Attached scope: tag definitions 08C028EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification S03_p01.
2. Enable and reset applicable timers for [SP1.2_Movie_Yuri Threat (0D1DA24C)](#trigger-0d1da24c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5078, Events line 5219, Actions line 5360.

<a id="trigger-0d1da24c"></a>

### 3. SP1.2_Movie_Yuri Threat - 0D1DA24C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.1a_VO_ZofiaREBeacon (08C029CC)](#trigger-08c029cc).

Attached scope: tag definitions 0D1DA39C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 41.
2. Enable and reset applicable timers for [SP1.3_VO_Zofia-->Beacon (09AF270C)](#trigger-09af270c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5079, Events line 5220, Actions line 5361.

<a id="trigger-09af270c"></a>

### 4. SP1.3_VO_Zofia-->Beacon - 09AF270C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.2_Movie_Yuri Threat (0D1DA24C)](#trigger-0d1da24c).

Attached scope: tag definitions 09AF1E3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 70 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_ZofiaBriefing01.
2. Enable and reset applicable timers for [SP1.4_Reveal/Ping Beacn (09AF146C)](#trigger-09af146c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5080, Events line 5221, Actions line 5362.

<a id="trigger-09af146c"></a>

### 5. SP1.4_Reveal/Ping Beacn - 09AF146C

Owner reference: BadGuy1Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.3_VO_Zofia-->Beacon (09AF270C)](#trigger-09af270c).

Attached scope: tag definitions 070A5E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 12 (cell 47, 94).
2. Create radar-event marker type 5 at waypoint 12 (cell 47, 94).
3. Enable and reset applicable timers for [SP1.6_Startup BG1 House (0D44603C)](#trigger-0d44603c).
4. Enable and reset applicable timers for [SP1.5_Unlock Input (0D99DC0C)](#trigger-0d99dc0c).
5. Move the camera to waypoint 18 (cell 50, 97) with speed setting 4.
6. Flash buildings of type NAPSYB; duration argument 120.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5081, Events line 5222, Actions line 5363.

<a id="trigger-0d44603c"></a>

### 6. SP1.6_Startup BG1 House - 0D44603C

Owner reference: BadGuy1Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.4_Reveal/Ping Beacn (09AF146C)](#trigger-09af146c).

Attached scope: tag definitions 0D44730C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 17 (country/type BADGUY1COUNTRY; placed owner BadGuy1).
2. AI triggers begin: owner selector 17 (country/type BADGUY1COUNTRY; placed owner BadGuy1).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5082, Events line 5223, Actions line 5364.

<a id="trigger-0d99dc0c"></a>

### 7. SP1.5_Unlock Input - 0D99DC0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.4_Reveal/Ping Beacn (09AF146C)](#trigger-09af146c).

Attached scope: tag definitions 0D99DB2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Play voice notification EVA_BattlefieldControlOnline.
3. Enable and reset applicable timers for [SP1.5a_Objective 1 (08FCFADC)](#trigger-08fcfadc).
4. Jump the camera to waypoint 699 (cell 91, 107).
5. Play sound CameraSwitch.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5083, Events line 5224, Actions line 5365.

<a id="trigger-08fcfadc"></a>

### 8. SP1.5a_Objective 1 - 08FCFADC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.5_Unlock Input (0D99DC0C)](#trigger-0d99dc0c).

Attached scope: tag definitions 08FCF9FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Destroy the Psychic Beacon.” (MISSION:Sov3Obj1).
2. Create radar-event marker type 5 at waypoint 12 (cell 47, 94).
3. Play sound BeaconPlaced.
4. Enable and reset applicable timers for [Repeat_Objective 1 (08FCD15C)](#trigger-08fcd15c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5084, Events line 5225, Actions line 5366.

<a id="trigger-08fcd15c"></a>

### 9. Repeat_Objective 1 - 08FCD15C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.5a_Objective 1 (08FCFADC)](#trigger-08fcfadc).

Attached scope: tag definitions 08FCD07C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Destroy the Psychic Beacon.” (MISSION:Sov3Obj1).
2. Create radar-event marker type 5 at waypoint 12 (cell 47, 94).
3. Play sound BeaconPlaced.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5085, Events line 5226, Actions line 5367.

<a id="trigger-0cc121ac"></a>

### 10. _Set_Sov03_Part2 - 0CC121AC

Owner reference: BadGuy2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.13_Unlock/End (0F189D9C)](#trigger-0f189d9c).

Attached scope: tag definitions 0BC6216C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Resize Player View; main setting 0; parameter 1: 2, parameter 2: 6, parameter 3: 56, parameter 4: 73.
2. Enable and reset applicable timers for [Startup Yuri House (0BCE216C)](#trigger-0bce216c).
3. Enable and reset applicable timers for [VO_Zofia_RE_TeslaTank (0D3F1D6C)](#trigger-0d3f1d6c).
4. Reveal terrain around waypoint 19 (cell 63, 22).
5. All change house: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
6. Play music theme DefendTheBase.
7. Enable and reset applicable timers for [_Setup_Sov03_Part2a (095AC33C)](#trigger-095ac33c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5086, Events line 5227, Actions line 5368.

<a id="trigger-0bce216c"></a>

### 11. Startup Yuri House - 0BCE216C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Set_Sov03_Part2 (0CC121AC)](#trigger-0cc121ac).

Attached scope: tag definitions 0BCE7F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. AI triggers begin: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
3. Play voice notification EVA_PsychicDominatorDetected.
4. Display message “WARNING - The Psychic Dominator is Armed!!!” (MISSION:WarnArmd).
5. Enable and reset applicable timers for [Taunt_Yuri RE Psy Dom (0BF6D8BC)](#trigger-0bf6d8bc).
6. Enable and reset applicable timers for [Disable Yuri Taunt (048B323C)](#trigger-048b323c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5087, Events line 5228, Actions line 5369.

<a id="trigger-0d3f1d6c"></a>

### 12. VO_Zofia_RE_TeslaTank - 0D3F1D6C

Owner reference: SovietsCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Set_Sov03_Part2 (0CC121AC)](#trigger-0cc121ac).

Attached scope: tag definitions 0D3F1C8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building exists: type index 7 (global list position: Allied War Factory (GAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_ZofiaTeslaTankReady.
2. Set Tech Level (Techno)[Level]; main setting TTNK; location/duration field 1.
3. Switch the sidebar to tab 3.
4. Flash cameo/type TTNK; additional configured duration/location argument 100.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5088, Events line 5229, Actions line 5370.

<a id="trigger-095ac33c"></a>

### 13. _Setup_Sov03_Part2a - 095AC33C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Set_Sov03_Part2 (0CC121AC)](#trigger-0cc121ac).

Attached scope: tag definitions 095AC25C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create building YAWEAP at waypoint 51 (cell 57, 37).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5089, Events line 5230, Actions line 5371.

<a id="trigger-0bf6d8bc"></a>

### 14. Taunt_Yuri RE Psy Dom - 0BF6D8BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Startup Yuri House (0BCE216C)](#trigger-0bce216c).

Attached scope: tag definitions 0BF6C10C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 420 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_YuriAlmostReady.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5090, Events line 5231, Actions line 5372.

<a id="trigger-048b323c"></a>

### 15. Disable Yuri Taunt - 048B323C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Startup Yuri House (0BCE216C)](#trigger-0bce216c).

Attached scope: tag definitions 048BFABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Low Power: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Disable [Taunt_Yuri RE Psy Dom (0BF6D8BC)](#trigger-0bf6d8bc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5091, Events line 5232, Actions line 5373.

<a id="trigger-0bf382dc"></a>

### 16. Player Wins - 0BF382DC

Owner reference: SovietsCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Complete_Objective 3 (092C8A9C)](#trigger-092c8a9c).

Attached scope: tag definitions 0BF3C2DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets) the winner.
2. Disable [Repeat_Objective 3 (08FCEF3C)](#trigger-08fcef3c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5092, Events line 5233, Actions line 5374.

<a id="trigger-08fcef3c"></a>

### 17. Repeat_Objective 3 - 08FCEF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_PsyDom Obj3 (0B287C9C)](#trigger-0b287c9c).

Attached scope: tag definitions 08FCEE5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Finish off Yuri's forces.” (MISSION:Sov3Obj3).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5093, Events line 5234, Actions line 5375.

<a id="trigger-09b95c1c"></a>

### 18. SP_Seal1_Trigger_Bridge - 09B95C1C

Owner reference: SovietsCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 24 tagged map cells: (61, 111), (62, 111), (63, 111), (64, 111), (65, 111), (66, 111), (67, 111), (68, 111), (69, 111), (61, 112), (61, 113), (61, 114), (60, 115), (61, 115), (60, 116), (79, 117), (79, 118), (79, 119), (76, 129), (77, 129), (75, 130), (76, 130), (74, 131), (75, 131); tag 09B9567C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Play sound SealSpecialAttack.
2. Reveal terrain around waypoint 9 (cell 69, 120).
3. Create/recruit team [TM_Seal (093AD32C)](sov03umd-teams.md#team-093ad32c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5094, Events line 5235, Actions line 5376.

<a id="trigger-0cc3bb5c"></a>

### 19. SP2.2_Allies Freed - 0CC3BB5C

Owner reference: BadGuy1Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.1_Destroyed_Beacon (09A29C5C)](#trigger-09a29c5c).

Attached scope: tag definitions 0704D60C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP2.3_Cheer_Allies (0BB9BDAC)](#trigger-0bb9bdac).
2. All change house: owner selector 14 (country/type ALLIESCOUNTRY; placed owner Allies).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5095, Events line 5236, Actions line 5377.

<a id="trigger-0bb9bdac"></a>

### 20. SP2.3_Cheer_Allies - 0BB9BDAC

Owner reference: AlliesCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.2_Allies Freed (0CC3BB5C)](#trigger-0cc3bb5c).

Attached scope: tag definitions 0BB9BCCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 14 (country/type ALLIESCOUNTRY; placed owner Allies).
2. Enable and reset applicable timers for [SP2.3a_Camera_Move to M (0BF590FC)](#trigger-0bf590fc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5096, Events line 5237, Actions line 5378.

<a id="trigger-0bf590fc"></a>

### 21. SP2.3a_Camera_Move to M - 0BF590FC

Owner reference: SovietsCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.3_Cheer_Allies (0BB9BDAC)](#trigger-0bb9bdac).

Attached scope: tag definitions 0BF5A44C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 12 (cell 47, 94).
2. Disable player input.
3. Play voice notification EVA_BattleControlOnline.
4. Play sound CameraSwitch.
5. Enable and reset applicable timers for [Evict_All from Tent (079D72CC)](#trigger-079d72cc).
6. Disable [Player Loses (0BEC10EC)](#trigger-0bec10ec).
7. Enable and reset applicable timers for [SP2.3b_Stop Player Chez (0441A60C)](#trigger-0441a60c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5097, Events line 5238, Actions line 5379.

<a id="trigger-079d72cc"></a>

### 22. Evict_All from Tent - 079D72CC

Owner reference: GoodGuy1Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.3a_Camera_Move to M (0BF590FC)](#trigger-0bf590fc); enable from [SP2.12_VO_Zofia Sorry (0BBDBF3C)](#trigger-0bbdbf3c).

Attached scope: Army Tents (CAARMY01), owner GoodGuy1, cell (43, 97), tag 079D67EC, persistence mode 2.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Evict_All from Tent (079D72CC)](#trigger-079d72cc).
2. Evict occupants from the attached building.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5098, Events line 5239, Actions line 5380.

<a id="trigger-0bec10ec"></a>

### 23. Player Loses - 0BEC10EC

Owner reference: SovietsCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.3d_Reset Lose Chek (0B2F957C)](#trigger-0b2f957c).

Attached scope: tag definitions 0BF383CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).
2. Destroyed,  Units,  All: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Declare owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets) the loser.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5099, Events line 5240, Actions line 5381.

<a id="trigger-0441a60c"></a>

### 24. SP2.3b_Stop Player Chez - 0441A60C

Owner reference: SovietsCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.3a_Camera_Move to M (0BF590FC)](#trigger-0bf590fc).

Attached scope: tag definitions 0441A52C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 16 (country/type GOODGUY2COUNTRY; placed owner GoodGuy2).
2. Enable and reset applicable timers for [SP2.3c_Chez on Brother! (0B2F819C)](#trigger-0b2f819c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5100, Events line 5241, Actions line 5382.

<a id="trigger-0b2f819c"></a>

### 25. SP2.3c_Chez on Brother! - 0B2F819C

Owner reference: GoodGuy2Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.3b_Stop Player Chez (0441A60C)](#trigger-0441a60c).

Attached scope: tag definitions 0B2F9F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).
2. Enable and reset applicable timers for [SP2.3d_Reset Lose Chek (0B2F957C)](#trigger-0b2f957c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5101, Events line 5242, Actions line 5383.

<a id="trigger-0b2f957c"></a>

### 26. SP2.3d_Reset Lose Chek - 0B2F957C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.3c_Chez on Brother! (0B2F819C)](#trigger-0b2f819c).

Attached scope: tag definitions 0B2F949C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Player Loses (0BEC10EC)](#trigger-0bec10ec).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5102, Events line 5243, Actions line 5384.

<a id="trigger-09a29c5c"></a>

### 27. SP2.1_Destroyed_Beacon - 09A29C5C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Beacon (NAPSYB), owner BadGuy1, cell (47, 94), tag 09A2942C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP2.2_Allies Freed (0CC3BB5C)](#trigger-0cc3bb5c).
2. Enable and reset applicable timers for [SP2.4_Reinforce_Tanya (048BFC1C)](#trigger-048bfc1c).
3. Disable [VO_Zofia_BridgeWarning1 (09BAF07C)](#trigger-09baf07c).
4. Disable [VO_Zofia_BridgeWarning3 (09AC503C)](#trigger-09ac503c).
5. Disable [V0_Zofia_BridgeWarning2 (09BAB47C)](#trigger-09bab47c).
6. Play voice notification Mis_xS3_YuriAlliesFreed.
7. Disable [SP_Seal1_Trigger_Bridge (09B95C1C)](#trigger-09b95c1c).
8. Disable [SP_Seal2_Bomb Placed (0B2FCF3C)](#trigger-0b2fcf3c).
9. Disable [SP_Seal3_Seal Dies (0B3BE93C)](#trigger-0b3be93c).
10. Disable [VO_Zofia_RE_Sniper (09B978DC)](#trigger-09b978dc).
11. Disable [Create_BG1 5 GI Team (0C72C22C)](#trigger-0c72c22c).
12. Disable [Repeat_Objective 1 (08FCD15C)](#trigger-08fcd15c).
13. Destroy current instances of [Create_BG1_1 Grizzly TM (086D7C6C)](#trigger-086d7c6c).
14. Destroy current instances of [Create_BG1_2 IFV Team (086D555C)](#trigger-086d555c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5103, Events line 5244, Actions line 5385.

<a id="trigger-048bfc1c"></a>

### 28. SP2.4_Reinforce_Tanya - 048BFC1C

Owner reference: AlliesCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.1_Destroyed_Beacon (09A29C5C)](#trigger-09a29c5c).

Attached scope: tag definitions 048BF8BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 16 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Tanya_IFV (0879E52C)](sov03umd-teams.md#team-0879e52c).
2. Restore Starting Buildings of: owner selector 15 (country/type GOODGUY1COUNTRY; placed owner GoodGuy1).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5104, Events line 5245, Actions line 5386.

<a id="trigger-09baf07c"></a>

### 29. VO_Zofia_BridgeWarning1 - 09BAF07C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 6 tagged map cells: (83, 87), (84, 87), (83, 88), (84, 88), (83, 89), (84, 89); tag 09BABD3C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Display message “WARNING - Possible Ambush Ahead!” (MISSION:WrnAmbsh).
3. Reveal terrain around waypoint 13 (cell 71, 88).
4. Create radar-event marker type 5 at waypoint 13 (cell 71, 88).
5. Play voice notification Mis_xS3_ZofiaEnemyIsPrepared.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5105, Events line 5246, Actions line 5387.

<a id="trigger-09ac503c"></a>

### 30. VO_Zofia_BridgeWarning3 - 09AC503C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 6 tagged map cells: (99, 51), (100, 51), (99, 52), (100, 52), (99, 53), (100, 53); tag 09AC204C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Display message “WARNING - Possible Ambush Ahead!” (MISSION:WrnAmbsh).
3. Reveal terrain around waypoint 15 (cell 87, 52).
4. Create radar-event marker type 5 at waypoint 15 (cell 87, 52).
5. Play voice notification Mis_xS3_ZofiaAmbushBeReady.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5106, Events line 5247, Actions line 5388.

<a id="trigger-09bab47c"></a>

### 31. V0_Zofia_BridgeWarning2 - 09BAB47C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 6 tagged map cells: (91, 68), (92, 68), (91, 69), (92, 69), (91, 70), (92, 70); tag 09BAB39C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Display message “WARNING - Possible Ambush Ahead!” (MISSION:WrnAmbsh).
3. Reveal terrain around waypoint 14 (cell 71, 69).
4. Create radar-event marker type 5 at waypoint 14 (cell 71, 69).
5. Play voice notification Mis_xS3_ZofiaDefensesAhead.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5107, Events line 5248, Actions line 5389.

<a id="trigger-0b2fcf3c"></a>

### 32. SP_Seal2_Bomb Placed - 0B2FCF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Bridge Repair Hut (CABHUT), owner Neutral, cell (69, 120), tag 0B2FD10C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 17 (country/type BADGUY1COUNTRY; placed owner BadGuy1).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP_Seal3_Seal Dies (0B3BE93C)](#trigger-0b3be93c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5108, Events line 5249, Actions line 5390.

<a id="trigger-0b3be93c"></a>

### 33. SP_Seal3_Seal Dies - 0B3BE93C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP_Seal2_Bomb Placed (0B2FCF3C)](#trigger-0b2fcf3c).

Attached scope: SEAL (GHOST), owner BadGuy1, cell (68, 122), tag 0B3B845C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Do Explosion At; main setting 50; location/duration field K.
3. Create/recruit team [TM_South Bridge Guard (0BC5C90C)](sov03umd-teams.md#team-0bc5c90c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5109, Events line 5250, Actions line 5391.

<a id="trigger-09b978dc"></a>

### 34. VO_Zofia_RE_Sniper - 09B978DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 28 tagged map cells: (67, 115), (68, 115), (69, 115), (67, 116), (66, 117), (67, 117), (87, 117), (88, 117), (89, 117), (65, 118), (66, 118), (87, 118), (88, 118), (89, 118), (65, 119), (87, 119), (88, 119), (89, 119), (65, 120), (65, 121), (81, 129), (82, 129), (83, 129), (84, 129), (85, 129), (86, 129), (81, 130), (86, 130); tag 09B9692C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 11 (cell 79, 131).
2. Play sound WarningAlarm.
3. Display message “WARNING - Sniper detected!” (MISSION:WarnSnpe).
4. Create radar-event marker type 5 at waypoint 11 (cell 79, 131).
5. Play voice notification Mis_xS3_ZofiaLookOutForSniper.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5110, Events line 5251, Actions line 5392.

<a id="trigger-0c72c22c"></a>

### 35. Create_BG1 5 GI Team - 0C72C22C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C72FB0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 250 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TM_5 GIs Attack (0C4297BC)](sov03umd-teams.md#team-0c4297bc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5111, Events line 5252, Actions line 5393.

<a id="trigger-086d7c6c"></a>

### 36. Create_BG1_1 Grizzly TM - 086D7C6C

Owner reference: BadGuy1Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Delay_Grizzly/IFV Teams (08723A1C)](#trigger-08723a1c).

Attached scope: tag definitions 086D7B8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 325 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_BG1_1 Grizzly (086D763C)](sov03umd-teams.md#team-086d763c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5112, Events line 5253, Actions line 5394.

<a id="trigger-086d555c"></a>

### 37. Create_BG1_2 IFV Team - 086D555C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Delay_Grizzly/IFV Teams (08723A1C)](#trigger-08723a1c).

Attached scope: tag definitions 086D547C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 175 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_2 IFVs (08E1245C)](sov03umd-teams.md#team-08e1245c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5113, Events line 5254, Actions line 5395.

<a id="trigger-048c0c6c"></a>

### 38. VO_Zofia_RE_Grinder - 048C0C6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 68 tagged map cells: (101, 48), (102, 48), (102, 49), (103, 49), (103, 50), (103, 51), (103, 52), (103, 53), (103, 54), (102, 55), (103, 55), (102, 56), (101, 57), (102, 57), (95, 63), (96, 63), (96, 64), (97, 64), (123, 64), (97, 65), (98, 65), (123, 65), (98, 66), (99, 66), (123, 66), (99, 67), (100, 67), (101, 67), (123, 67), (101, 68), (123, 68), (101, 69), (102, 69), (120, 69), (121, 69), (122, 69), (123, 69), (102, 70), (103, 70), (104, 70), (120, 70), (104, 71), (105, 71), (116, 71), (117, 71), (118, 71), (119, 71), (120, 71), (105, 72), (106, 72), (115, 72), (116, 72), (106, 73), (107, 73), (115, 73), (107, 74), (115, 74), (107, 75), (113, 75), (114, 75), (115, 75), (107, 76), (108, 76), (109, 76), (110, 76), (111, 76), (112, 76), (113, 76); tag 06F1CF4C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_ZofiaDestroyGrinder.
2. Reveal terrain around waypoint 16 (cell 109, 65).
3. Create radar-event marker type 5 at waypoint 16 (cell 109, 65).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5114, Events line 5255, Actions line 5396.

<a id="trigger-0995432c"></a>

### 39. Destroyed_PsyDom - 0995432C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Dominator (YAPPET), owner YuriCountry, cell (61, 20), tag 0995424C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_YuriEveryoneAttack.
2. Reveal the whole map.
3. Enable and reset applicable timers for [Player Wins_Delay (043F3B9C)](#trigger-043f3b9c).
4. Fire Sale: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
5. Disable [Repeat_Objective 2 (08FCD32C)](#trigger-08fcd32c).
6. Enable and reset applicable timers for [Destroyed_PsyDom Obj3 (0B287C9C)](#trigger-0b287c9c).
7. Supply reinforcement team [TM_Yuri_"Everyone Attack" (0440DB8C)](sov03umd-teams.md#team-0440db8c).
8. Enable and reset applicable timers for ["Everyone Attack!" (0441591C)](#trigger-0441591c).
9. Enable and reset applicable timers for [_Amb_Stop all Drones (05C1C75C)](#trigger-05c1c75c).
10. Enable and reset applicable timers for [Sell_Bio Reactor Civ3 (09206F3C)](#trigger-09206f3c).
11. Enable and reset applicable timers for [Sell_Bio Reactor@Grind (0786714C)](#trigger-0786714c).
12. Enable and reset applicable timers for [Sell_Left Grind Gatt (07867E5C)](#trigger-07867e5c).
13. Enable and reset applicable timers for [Sell_Right Grind Gatt (0786756C)](#trigger-0786756c).
14. Enable and reset applicable timers for [Sell_Grinder (09259C7C)](#trigger-09259c7c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5115, Events line 5256, Actions line 5397.

<a id="trigger-043f3b9c"></a>

### 40. Player Wins_Delay - 043F3B9C

Owner reference: SovietsCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_PsyDom (0995432C)](#trigger-0995432c).

Attached scope: tag definitions 043F3ABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Complete_Objective 3 (092C8A9C)](#trigger-092c8a9c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5116, Events line 5257, Actions line 5398.

<a id="trigger-08fcd32c"></a>

### 41. Repeat_Objective 2 - 08FCD32C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.14_Objective 2 (08FC8A0C)](#trigger-08fc8a0c).

Attached scope: tag definitions 08FCD24C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy the Psychic Dominator.” (MISSION:Sov3Obj2).
2. Create radar-event marker type 5 at waypoint 19 (cell 63, 22).
3. Play sound BeaconPlaced.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5117, Events line 5258, Actions line 5399.

<a id="trigger-0b287c9c"></a>

### 42. Destroyed_PsyDom Obj3 - 0B287C9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_PsyDom (0995432C)](#trigger-0995432c).

Attached scope: tag definitions 0B287BBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Finish off Yuri's forces.” (MISSION:Sov3Obj3).
2. Enable and reset applicable timers for [Repeat_Objective 3 (08FCEF3C)](#trigger-08fcef3c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5118, Events line 5259, Actions line 5400.

<a id="trigger-0441591c"></a>

### 43. "Everyone Attack!" - 0441591C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_PsyDom (0995432C)](#trigger-0995432c).

Attached scope: tag definitions 0441583C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. All to Hunt: owner selector 21 (country/type CIVIE3COUNTRY; placed owner Civie3).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5119, Events line 5260, Actions line 5401.

<a id="trigger-05c1c75c"></a>

### 44. _Amb_Stop all Drones - 05C1C75C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_PsyDom (0995432C)](#trigger-0995432c); enable from [Destoyed_Grinder (05FB472C)](#trigger-05fb472c).

Attached scope: tag definitions 05C1C67C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Stop location sound 26 at waypoint 26 (cell 131, 84).
2. Stop location sound 27 at waypoint 27 (cell 115, 107).
3. Stop location sound 28 at waypoint 28 (cell 97, 86).
4. Stop location sound 29 at waypoint 29 (cell 90, 81).
5. Stop location sound 30 at waypoint 30 (cell 93, 78).
6. Stop location sound 31 at waypoint 31 (cell 109, 88).
7. Stop location sound 32 at waypoint 32 (cell 97, 118).
8. Stop location sound 48 at waypoint 48 (cell 104, 107).
9. Stop location sound 49 at waypoint 49 (cell 114, 76).
10. Stop location sound 50 at waypoint 50 (cell 99, 73).
11. Stop location sound 503 at waypoint 503 (cell 111, 100).
12. Stop location sound 504 at waypoint 504 (cell 104, 82).
13. Stop location sound 530 at waypoint 530 (cell 113, 69).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5120, Events line 5261, Actions line 5402.

<a id="trigger-09206f3c"></a>

### 45. Sell_Bio Reactor Civ3 - 09206F3C

Owner reference: Civie3Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_PsyDom (0995432C)](#trigger-0995432c); enable from [Sell_Left Grind Gatt (07867E5C)](#trigger-07867e5c); enable from [Sell_Right Grind Gatt (0786756C)](#trigger-0786756c); enable from [Detect_Grind Bio Dead (092076DC)](#trigger-092076dc).

Attached scope: Bio Reactor (YAPOWR), owner Civie3, cell (109, 51), tag 09206E5C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5121, Events line 5262, Actions line 5403.

<a id="trigger-0786714c"></a>

### 46. Sell_Bio Reactor@Grind - 0786714C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Grind Bio Dead (092076DC)](#trigger-092076dc).

Incoming activation links: enable from [Destroyed_PsyDom (0995432C)](#trigger-0995432c); enable from [Destoyed_Grinder (05FB472C)](#trigger-05fb472c).

Attached scope: Bio Reactor (YAPOWR), owner YuriCountry, cell (101, 59), tag 092075FC, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building exists: type index 301 (global list position: Yuri Construction Yard (YACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Disable [Sell_Bio Reactor@Grind (0786714C)](#trigger-0786714c).
2. Sell the attached building through the scripted sale action.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5122, Events line 5263, Actions line 5404.

<a id="trigger-07867e5c"></a>

### 47. Sell_Left Grind Gatt - 07867E5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_PsyDom (0995432C)](#trigger-0995432c); enable from [Destoyed_Grinder (05FB472C)](#trigger-05fb472c).

Attached scope: Gattling Cannon (YAGGUN), owner Civie3, cell (107, 68), tag 078673DC, persistence mode 0.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.
2. Enable and reset applicable timers for [Sell_Bio Reactor Civ3 (09206F3C)](#trigger-09206f3c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5123, Events line 5264, Actions line 5405.

<a id="trigger-0786756c"></a>

### 48. Sell_Right Grind Gatt - 0786756C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_PsyDom (0995432C)](#trigger-0995432c); enable from [Destoyed_Grinder (05FB472C)](#trigger-05fb472c).

Attached scope: Gattling Cannon (YAGGUN), owner Civie3, cell (112, 63), tag 07867F4C, persistence mode 0.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.
2. Enable and reset applicable timers for [Sell_Bio Reactor Civ3 (09206F3C)](#trigger-09206f3c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5124, Events line 5265, Actions line 5406.

<a id="trigger-09259c7c"></a>

### 49. Sell_Grinder - 09259C7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_PsyDom (0995432C)](#trigger-0995432c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Sell_Grinder (09259C7C)](#trigger-09259c7c).
2. Sell the attached building through the scripted sale action.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5125, Events line 5266, Actions line 5407.

<a id="trigger-092c8a9c"></a>

### 50. Complete_Objective 3 - 092C8A9C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Wins_Delay (043F3B9C)](#trigger-043f3b9c).

Attached scope: tag definitions 092C89BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  All: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Display message “Objective 3 Complete.” (MISSION:Obj3Comp).
2. Play voice notification EVA_ObjectiveComplete.
3. Enable and reset applicable timers for [Player Wins (0BF382DC)](#trigger-0bf382dc).
4. Make side cheer: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5126, Events line 5267, Actions line 5408.

<a id="trigger-092076dc"></a>

### 51. Detect_Grind Bio Dead - 092076DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Detect_Grind Bio Dead (092076DC)](#trigger-092076dc).
2. Enable and reset applicable timers for [Sell_Bio Reactor Civ3 (09206F3C)](#trigger-09206f3c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5127, Events line 5268, Actions line 5409.

<a id="trigger-099e9d1c"></a>

### 52. SP2.5_VO_Yuri-->Tanya - 099E9D1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 099E9C3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (YuriSeesTanya) is set.

Flag writers in this mission: clear local flag 0 (YuriSeesTanya) at [SP2.5_VO_Yuri-->Tanya (099E9D1C)](#trigger-099e9d1c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 0 (YuriSeesTanya).
2. Enable and reset applicable timers for [SP2.5a_VO_Yuri-->Tanya (0C5E6AEC)](#trigger-0c5e6aec).
3. Supply reinforcement team [TM_Allies_4 GIs to Tent (091F77BC)](sov03umd-teams.md#team-091f77bc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5128, Events line 5269, Actions line 5410.

<a id="trigger-0c5e6aec"></a>

### 53. SP2.5a_VO_Yuri-->Tanya - 0C5E6AEC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.5_VO_Yuri-->Tanya (099E9D1C)](#trigger-099e9d1c).

Attached scope: tag definitions 0C5E6A0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_YuriTanyaTaunt1.
2. Enable and reset applicable timers for [SP2.6_VO_Tanya-->Yuri (099E9B4C)](#trigger-099e9b4c).
3. Supply reinforcement team [TM_Allies_Chrono Arrives (08FFFEFC)](sov03umd-teams.md#team-08fffefc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5129, Events line 5270, Actions line 5411.

<a id="trigger-099e9b4c"></a>

### 54. SP2.6_VO_Tanya-->Yuri - 099E9B4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.5a_VO_Yuri-->Tanya (0C5E6AEC)](#trigger-0c5e6aec).

Attached scope: tag definitions 099E9A6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Clear local flag 1 (TanyaRetortYuri).
2. Play voice notification Mis_xS3_TanyaTanyaWithSov2.
3. Enable and reset applicable timers for [SP2.7_Movie_Tanya Intro (0DE526AC)](#trigger-0de526ac).
4. Create/recruit team [TM_Tanya (Allied)_100 Flash (087A1EFC)](sov03umd-teams.md#team-087a1efc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5130, Events line 5271, Actions line 5412.

<a id="trigger-0de526ac"></a>

### 55. SP2.7_Movie_Tanya Intro - 0DE526AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.6_VO_Tanya-->Yuri (099E9B4C)](#trigger-099e9b4c).

Attached scope: tag definitions 0DE525CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 42.
2. Enable and reset applicable timers for [SP2.8_Movie_Tanya Thank (099E997C)](#trigger-099e997c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5131, Events line 5272, Actions line 5413.

<a id="trigger-099e997c"></a>

### 56. SP2.8_Movie_Tanya Thank - 099E997C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.7_Movie_Tanya Intro (0DE526AC)](#trigger-0de526ac).

Attached scope: tag definitions 099E871C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP2.9_Allies Turn Red (0BD31ABC)](#trigger-0bd31abc).
2. Create/recruit team [TM_Tanya (Allied)_350 Flash (087A10FC)](sov03umd-teams.md#team-087a10fc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5132, Events line 5273, Actions line 5414.

<a id="trigger-0bd31abc"></a>

### 57. SP2.9_Allies Turn Red - 0BD31ABC

Owner reference: AlliesCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.8_Movie_Tanya Thank (099E997C)](#trigger-099e997c).

Attached scope: tag definitions 0BD319DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).
2. Enable and reset applicable timers for [SP2.10_Audio_ZofRETanya (0BBDB3EC)](#trigger-0bbdb3ec).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5133, Events line 5274, Actions line 5415.

<a id="trigger-0bbdb3ec"></a>

### 58. SP2.10_Audio_ZofRETanya - 0BBDB3EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.9_Allies Turn Red (0BD31ABC)](#trigger-0bd31abc).

Attached scope: tag definitions 0BBDB30C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_ZofiaTanyaWithSov1.
2. Enable and reset applicable timers for [SP2.11_VO_TanyaREBoris (0BBDB21C)](#trigger-0bbdb21c).
3. Supply reinforcement team [TM_Tanya (Soviet)_100 Flash (087A1A4C)](sov03umd-teams.md#team-087a1a4c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5134, Events line 5275, Actions line 5416.

<a id="trigger-0bbdb21c"></a>

### 59. SP2.11_VO_TanyaREBoris - 0BBDB21C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.10_Audio_ZofRETanya (0BBDB3EC)](#trigger-0bbdb3ec).

Attached scope: tag definitions 0BBDB13C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 16 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_TanyaTanyaWithSov1.
2. Enable and reset applicable timers for [SP2.12_VO_Zofia Sorry (0BBDBF3C)](#trigger-0bbdbf3c).
3. Create/recruit team [TM_Tanya (Soviet)_250 Flash (087A130C)](sov03umd-teams.md#team-087a130c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5135, Events line 5276, Actions line 5417.

<a id="trigger-0bbdbf3c"></a>

### 60. SP2.12_VO_Zofia Sorry - 0BBDBF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.11_VO_TanyaREBoris (0BBDB21C)](#trigger-0bbdb21c).

Attached scope: tag definitions 0BBDBE5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 18 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_ZofiaTanyaWithSov2.
2. Enable and reset applicable timers for [SP2.13_Unlock/End (0F189D9C)](#trigger-0f189d9c).
3. Enable and reset applicable timers for [Evict_All from Tent (079D72CC)](#trigger-079d72cc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5136, Events line 5277, Actions line 5418.

<a id="trigger-0f189d9c"></a>

### 61. SP2.13_Unlock/End - 0F189D9C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.12_VO_Zofia Sorry (0BBDBF3C)](#trigger-0bbdbf3c).

Attached scope: tag definitions 0F189CBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Set_Sov03_Part2 (0CC121AC)](#trigger-0cc121ac).
2. Enable player input.
3. Play voice notification EVA_BattlefieldControlOnline.
4. Enable and reset applicable timers for [SP2.14_Objective 2 (08FC8A0C)](#trigger-08fc8a0c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5137, Events line 5278, Actions line 5419.

<a id="trigger-08fc8a0c"></a>

### 62. SP2.14_Objective 2 - 08FC8A0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.13_Unlock/End (0F189D9C)](#trigger-0f189d9c).

Attached scope: tag definitions 08FC892C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy the Psychic Dominator.” (MISSION:Sov3Obj2).
2. Create radar-event marker type 5 at waypoint 19 (cell 63, 22).
3. Play sound BeaconPlaced.
4. Enable and reset applicable timers for [Repeat_Objective 2 (08FCD32C)](#trigger-08fcd32c).
5. Play voice notification Mis_xS3_ZofiaDominatorReady.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5138, Events line 5279, Actions line 5420.

<a id="trigger-0bf42a9c"></a>

### 63. Disable Bridge1 Warn - 0BF42A9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 6 tagged map cells: (70, 87), (71, 87), (70, 88), (71, 88), (70, 89), (71, 89); tag 0BF429BC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Disable [VO_Zofia_BridgeWarning1 (09BAF07C)](#trigger-09baf07c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5139, Events line 5280, Actions line 5421.

<a id="trigger-0bf442fc"></a>

### 64. Disable Bridge2 Warn - 0BF442FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 6 tagged map cells: (70, 68), (71, 68), (70, 69), (71, 69), (70, 70), (71, 70); tag 0BF4421C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Disable [V0_Zofia_BridgeWarning2 (09BAB47C)](#trigger-09bab47c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5140, Events line 5281, Actions line 5422.

<a id="trigger-0bf42ecc"></a>

### 65. Disable Bridge3 Warn - 0BF42ECC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 6 tagged map cells: (77, 51), (78, 51), (77, 52), (78, 52), (77, 53), (78, 53); tag 0BF4C03C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Disable [VO_Zofia_BridgeWarning3 (09AC503C)](#trigger-09ac503c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5141, Events line 5282, Actions line 5423.

<a id="trigger-0bf365cc"></a>

### 66. Warning_Yuri Mad - 0BF365CC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 71 tagged map cells: (48, 21), (49, 21), (78, 21), (49, 22), (50, 22), (78, 22), (50, 23), (78, 23), (50, 24), (78, 24), (50, 25), (78, 25), (50, 26), (78, 26), (50, 27), (51, 27), (52, 27), (78, 27), (52, 28), (78, 28), (52, 29), (78, 29), (52, 30), (77, 30), (78, 30), (52, 31), (76, 31), (77, 31), (52, 32), (68, 32), (69, 32), (70, 32), (71, 32), (72, 32), (73, 32), (74, 32), (75, 32), (76, 32), (52, 33), (68, 33), (52, 34), (68, 34), (52, 35), (68, 35), (52, 36), (68, 36), (52, 37), (68, 37), (52, 38), (68, 38), (52, 39), (68, 39), (52, 40), (60, 40), (61, 40), (62, 40), (63, 40), (64, 40), (65, 40), (66, 40), (67, 40), (68, 40), (52, 41), (53, 41), (54, 41), (55, 41), (56, 41), (57, 41), (58, 41), (59, 41), (60, 41); tag 0BF3732C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_YuriLastChance.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5142, Events line 5283, Actions line 5424.

<a id="trigger-0bf390cc"></a>

### 67. Warning_Yuri Annoyed - 0BF390CC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 87 tagged map cells: (35, 34), (36, 34), (36, 35), (37, 35), (85, 35), (37, 36), (85, 36), (37, 37), (85, 37), (37, 38), (38, 38), (39, 38), (85, 38), (39, 39), (85, 39), (39, 40), (85, 40), (39, 41), (85, 41), (39, 42), (85, 42), (39, 43), (83, 43), (84, 43), (85, 43), (39, 44), (39, 45), (40, 45), (40, 46), (41, 46), (42, 46), (43, 46), (44, 46), (45, 46), (45, 47), (45, 48), (74, 48), (75, 48), (76, 48), (45, 49), (74, 49), (45, 50), (74, 50), (45, 51), (74, 51), (44, 52), (45, 52), (74, 52), (44, 53), (74, 53), (44, 54), (74, 54), (44, 55), (74, 55), (44, 56), (57, 56), (58, 56), (59, 56), (60, 56), (61, 56), (62, 56), (63, 56), (64, 56), (65, 56), (66, 56), (67, 56), (68, 56), (69, 56), (70, 56), (71, 56), (72, 56), (73, 56), (74, 56), (44, 57), (45, 57), (46, 57), (47, 57), (48, 57), (49, 57), (50, 57), (51, 57), (52, 57), (53, 57), (54, 57), (55, 57), (56, 57), (57, 57); tag 0BF3C5BC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_YuriLeave.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5143, Events line 5284, Actions line 5425.

<a id="trigger-0bd087bc"></a>

### 68. SMidBridge Attacked - 0BD087BC

Owner reference: BadGuy1Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Grizzly Battle Tank (MTNK), owner BadGuy1, cell (71, 89), tag 0BD09EDC, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy1, cell (71, 87), tag 0BD09EDC, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [TM_SMiddle Backup (0BCF01BC)](sov03umd-teams.md#team-0bcf01bc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5144, Events line 5285, Actions line 5426.

<a id="trigger-0957d3fc"></a>

### 69. _Setup_Sov03 - 0957D3FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0957ED0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 20 (cell 88, 100).
2. Create crate type 0 at waypoint 20 (cell 88, 100).
3. Enable and reset applicable timers for [SP1.1_Movie_Zofia Brief (0D1DACFC)](#trigger-0d1dacfc).
4. Disable player input.
5. Play voice notification EVA_EstablishBattlefieldControl.
6. Create crate type 0 at waypoint 22 (cell 81, 129).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5145, Events line 5286, Actions line 5427.

<a id="trigger-0d982e3c"></a>

### 70. Detect_Sniper Dead - 0D982E3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Sniper (SNIPE), owner BadGuy1, cell (77, 130), tag 0D98291C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [VO_Zofia_RE_Sniper (09B978DC)](#trigger-09b978dc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5146, Events line 5287, Actions line 5428.

<a id="trigger-06b552fc"></a>

### 71. Detect_Refinery Entered - 06B552FC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Ore Refinery (GAREFN), owner Neutral, cell (120, 92), tag 06B5521C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change_To Soviet (06B56DFC)](#trigger-06b56dfc).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5147, Events line 5288, Actions line 5429.

<a id="trigger-06b56dfc"></a>

### 72. Change_To Soviet - 06B56DFC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Refinery Entered (06B552FC)](#trigger-06b552fc).

Attached scope: Chrono Miner (CMIN), owner Civie2, cell (124, 93), tag 06B56D1C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5148, Events line 5289, Actions line 5430.

<a id="trigger-0c5e01ec"></a>

### 73. SPTanya 1_ Detect Dead - 0C5E01EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C5E1D7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SPTanya 2_VO_Yuri Taunt (0F951BEC)](#trigger-0f951bec).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5149, Events line 5290, Actions line 5431.

<a id="trigger-0f951bec"></a>

### 74. SPTanya 2_VO_Yuri Taunt - 0F951BEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SPTanya 1_ Detect Dead (0C5E01EC)](#trigger-0c5e01ec).

Attached scope: tag definitions 0F957F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_YuriTanyaTaunt2.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5150, Events line 5291, Actions line 5432.

<a id="trigger-0c74d75c"></a>

### 75. Detect_Barracks Dead - 0C74D75C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Barracks (GAPILE), owner BadGuy1, cell (60, 98), tag 0C74D67C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Create_BG1 5 GI Team (0C72C22C)](#trigger-0c72c22c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5151, Events line 5292, Actions line 5433.

<a id="trigger-07a64a1c"></a>

### 76. Reinforce_CIV1 @ AA - 07A64A1C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 81 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV1 (female) (0B0D66AC)](sov03umd-teams.md#team-0b0d66ac) at waypoint 26 (cell 131, 84).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5152, Events line 5293, Actions line 5434.

<a id="trigger-07a647dc"></a>

### 77. Reinforce_CIV1 @ AB - 07A647DC

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV1 @ AA (07A64A1C)](#trigger-07a64a1c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 61 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV1 (female) (0B0D66AC)](sov03umd-teams.md#team-0b0d66ac) at waypoint 27 (cell 115, 107).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5153, Events line 5294, Actions line 5435.

<a id="trigger-07a646ec"></a>

### 78. Reinforce_CIV1 @ AC - 07A646EC

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV1 @ AB (07A647DC)](#trigger-07a647dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 96 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV1 (female) (0B0D66AC)](sov03umd-teams.md#team-0b0d66ac) at waypoint 28 (cell 97, 86).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5154, Events line 5295, Actions line 5436.

<a id="trigger-07a645fc"></a>

### 79. Reinforce_CIV1 @ AD - 07A645FC

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV1 @ AC (07A646EC)](#trigger-07a646ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 76 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV1 (female) (0B0D66AC)](sov03umd-teams.md#team-0b0d66ac) at waypoint 29 (cell 90, 81).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5155, Events line 5296, Actions line 5437.

<a id="trigger-07a6438c"></a>

### 80. Reinforce_CIV1 @ AE - 07A6438C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV1 @ AD (07A645FC)](#trigger-07a645fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 67 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV1 (female) (0B0D66AC)](sov03umd-teams.md#team-0b0d66ac) at waypoint 30 (cell 93, 78).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5156, Events line 5297, Actions line 5438.

<a id="trigger-07a6429c"></a>

### 81. Reinforce_CIV1 @ AF - 07A6429C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV1 @ AE (07A6438C)](#trigger-07a6438c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 72 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV1 (female) (0B0D66AC)](sov03umd-teams.md#team-0b0d66ac) at waypoint 31 (cell 109, 88).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5157, Events line 5298, Actions line 5439.

<a id="trigger-07a641ac"></a>

### 82. Reinforce_CIV1 @ AG - 07A641AC

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV1 @ AF (07A6429C)](#trigger-07a6429c).

Attached scope: tag definitions 07A648CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 63 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV1 (female) (0B0D66AC)](sov03umd-teams.md#team-0b0d66ac) at waypoint 32 (cell 97, 118).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5158, Events line 5299, Actions line 5440.

<a id="trigger-08ef363c"></a>

### 83. Reinforce_CIV2 @ AA - 08EF363C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 63 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV2 (0B0D61FC)](sov03umd-teams.md#team-0b0d61fc) at waypoint 26 (cell 131, 84).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5159, Events line 5300, Actions line 5441.

<a id="trigger-08ef48ec"></a>

### 84. Reinforce_CIV2 @ AB - 08EF48EC

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV2 @ AA (08EF363C)](#trigger-08ef363c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 81 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV2 (0B0D61FC)](sov03umd-teams.md#team-0b0d61fc) at waypoint 27 (cell 115, 107).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5160, Events line 5301, Actions line 5442.

<a id="trigger-08ef47fc"></a>

### 85. Reinforce_CIV2 @ AC - 08EF47FC

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV2 @ AB (08EF48EC)](#trigger-08ef48ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 61 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV2 (0B0D61FC)](sov03umd-teams.md#team-0b0d61fc) at waypoint 28 (cell 97, 86).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5161, Events line 5302, Actions line 5443.

<a id="trigger-08f47f3c"></a>

### 86. Reinforce_CIV2 @ AD - 08F47F3C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV2 @ AC (08EF47FC)](#trigger-08ef47fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 96 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV2 (0B0D61FC)](sov03umd-teams.md#team-0b0d61fc) at waypoint 29 (cell 90, 81).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5162, Events line 5303, Actions line 5444.

<a id="trigger-043f1b1c"></a>

### 87. Reinforce_CIV2 @ AE - 043F1B1C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV2 @ AD (08F47F3C)](#trigger-08f47f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 76 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV2 (0B0D61FC)](sov03umd-teams.md#team-0b0d61fc) at waypoint 30 (cell 93, 78).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5163, Events line 5304, Actions line 5445.

<a id="trigger-043f1a2c"></a>

### 88. Reinforce_CIV2 @ AF - 043F1A2C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV2 @ AE (043F1B1C)](#trigger-043f1b1c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 67 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV2 (0B0D61FC)](sov03umd-teams.md#team-0b0d61fc) at waypoint 31 (cell 109, 88).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5164, Events line 5305, Actions line 5446.

<a id="trigger-043f193c"></a>

### 89. Reinforce_CIV2 @ AG - 043F193C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV2 @ AF (043F1A2C)](#trigger-043f1a2c).

Attached scope: tag definitions 08EF49DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 72 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV2 (0B0D61FC)](sov03umd-teams.md#team-0b0d61fc) at waypoint 32 (cell 97, 118).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5165, Events line 5306, Actions line 5447.

<a id="trigger-043f241c"></a>

### 90. Reinforce_CIV3 @ AA - 043F241C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 72 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV3 (0B0D7DEC)](sov03umd-teams.md#team-0b0d7dec) at waypoint 26 (cell 131, 84).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5166, Events line 5307, Actions line 5448.

<a id="trigger-043f224c"></a>

### 91. Reinforce_CIV3 @ AB - 043F224C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV3 @ AA (043F241C)](#trigger-043f241c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 63 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV3 (0B0D7DEC)](sov03umd-teams.md#team-0b0d7dec) at waypoint 27 (cell 115, 107).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5167, Events line 5308, Actions line 5449.

<a id="trigger-043f215c"></a>

### 92. Reinforce_CIV3 @ AC - 043F215C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV3 @ AB (043F224C)](#trigger-043f224c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 81 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV3 (0B0D7DEC)](sov03umd-teams.md#team-0b0d7dec) at waypoint 28 (cell 97, 86).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5168, Events line 5309, Actions line 5450.

<a id="trigger-043f206c"></a>

### 93. Reinforce_CIV3 @ AD - 043F206C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV3 @ AC (043F215C)](#trigger-043f215c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 61 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV3 (0B0D7DEC)](sov03umd-teams.md#team-0b0d7dec) at waypoint 29 (cell 90, 81).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5169, Events line 5310, Actions line 5451.

<a id="trigger-043f2f3c"></a>

### 94. Reinforce_CIV3 @ AE - 043F2F3C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV3 @ AD (043F206C)](#trigger-043f206c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 96 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV3 (0B0D7DEC)](sov03umd-teams.md#team-0b0d7dec) at waypoint 30 (cell 93, 78).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5170, Events line 5311, Actions line 5452.

<a id="trigger-043f2e4c"></a>

### 95. Reinforce_CIV3 @ AF - 043F2E4C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV3 @ AE (043F2F3C)](#trigger-043f2f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 76 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV3 (0B0D7DEC)](sov03umd-teams.md#team-0b0d7dec) at waypoint 31 (cell 109, 88).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5171, Events line 5312, Actions line 5453.

<a id="trigger-043f2d5c"></a>

### 96. Reinforce_CIV3 @ AG - 043F2D5C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIV3 @ AF (043F2E4C)](#trigger-043f2e4c).

Attached scope: tag definitions 043F233C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 67 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_CIV3 (0B0D7DEC)](sov03umd-teams.md#team-0b0d7dec) at waypoint 32 (cell 97, 118).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5172, Events line 5313, Actions line 5454.

<a id="trigger-043f2c6c"></a>

### 97. Reinforce_CIVs @ AA - 043F2C6C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 67 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Civ Snow Female (0B0D7BAC)](sov03umd-teams.md#team-0b0d7bac) at waypoint 26 (cell 131, 84).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5173, Events line 5314, Actions line 5455.

<a id="trigger-043f291c"></a>

### 98. Reinforce_CIVs @ AB - 043F291C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIVs @ AA (043F2C6C)](#trigger-043f2c6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 72 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Civ Snow Female (0B0D7BAC)](sov03umd-teams.md#team-0b0d7bac) at waypoint 27 (cell 115, 107).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5174, Events line 5315, Actions line 5456.

<a id="trigger-043f282c"></a>

### 99. Reinforce_CIVs @ AC - 043F282C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIVs @ AB (043F291C)](#trigger-043f291c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 63 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Civ Snow Female (0B0D7BAC)](sov03umd-teams.md#team-0b0d7bac) at waypoint 28 (cell 97, 86).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5175, Events line 5316, Actions line 5457.

<a id="trigger-043f25bc"></a>

### 100. Reinforce_CIVs @ AD - 043F25BC

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIVs @ AC (043F282C)](#trigger-043f282c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 81 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Civ Snow Female (0B0D7BAC)](sov03umd-teams.md#team-0b0d7bac) at waypoint 29 (cell 90, 81).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5176, Events line 5317, Actions line 5458.

<a id="trigger-043f3d6c"></a>

### 101. Reinforce_CIVs @ AE - 043F3D6C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIVs @ AD (043F25BC)](#trigger-043f25bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 61 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Civ Snow Female (0B0D7BAC)](sov03umd-teams.md#team-0b0d7bac) at waypoint 30 (cell 93, 78).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5177, Events line 5318, Actions line 5459.

<a id="trigger-043f3c7c"></a>

### 102. Reinforce_CIVs @ AF - 043F3C7C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIVs @ AE (043F3D6C)](#trigger-043f3d6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 96 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Civ Snow Female (0B0D7BAC)](sov03umd-teams.md#team-0b0d7bac) at waypoint 31 (cell 109, 88).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5178, Events line 5319, Actions line 5460.

<a id="trigger-043f3b8c"></a>

### 103. Reinforce_CIVs @ AG - 043F3B8C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reinforce_CIVs @ AF (043F3C7C)](#trigger-043f3c7c).

Attached scope: tag definitions 043F2B8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 76 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Civ Snow Female (0B0D7BAC)](sov03umd-teams.md#team-0b0d7bac) at waypoint 32 (cell 97, 118).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5179, Events line 5320, Actions line 5461.

<a id="trigger-043f3a9c"></a>

### 104. Destroyed_Building @ AA - 043F3A9C

Owner reference: Civie1Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CALOND03), owner Civie1, cell (130, 82), tag 043F39BC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Reinforce_CIV1 @ AA (07A64A1C)](#trigger-07a64a1c).
2. Disable [Reinforce_CIV2 @ AA (08EF363C)](#trigger-08ef363c).
3. Disable [Reinforce_CIV3 @ AA (043F241C)](#trigger-043f241c).
4. Disable [Reinforce_CIVs @ AA (043F2C6C)](#trigger-043f2c6c).
5. Set local flag 2 (@AA Destroyed).
6. Stop location sound 26 at waypoint 26 (cell 131, 84).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5180, Events line 5321, Actions line 5462.

<a id="trigger-07a0a27c"></a>

### 105. _Amb_Drone @ AA - 07A0A27C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0A19C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 70 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 26 (cell 131, 84).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5181, Events line 5322, Actions line 5463.

<a id="trigger-043f46ac"></a>

### 106. Destroyed_Building @ AD - 043F46AC

Owner reference: Civie1Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM03), owner Civie1, cell (88, 80), tag 043F45CC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Reinforce_CIV1 @ AD (07A645FC)](#trigger-07a645fc).
2. Disable [Reinforce_CIV2 @ AD (08F47F3C)](#trigger-08f47f3c).
3. Disable [Reinforce_CIV3 @ AD (043F206C)](#trigger-043f206c).
4. Disable [Reinforce_CIVs @ AD (043F25BC)](#trigger-043f25bc).
5. Set local flag 5 (@AD Destroyed).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5182, Events line 5323, Actions line 5464.

<a id="trigger-043f44dc"></a>

### 107. Destroyed_Building @ AE - 043F44DC

Owner reference: Civie1Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM02), owner Civie1, cell (92, 76), tag 043F43FC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Reinforce_CIV1 @ AE (07A6438C)](#trigger-07a6438c).
2. Disable [Reinforce_CIV2 @ AE (043F1B1C)](#trigger-043f1b1c).
3. Disable [Reinforce_CIV3 @ AE (043F2F3C)](#trigger-043f2f3c).
4. Disable [Reinforce_CIVs @ AE (043F3D6C)](#trigger-043f3d6c).
5. Set local flag 6 (@AE Destroyed).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5183, Events line 5324, Actions line 5465.

<a id="trigger-043f430c"></a>

### 108. Destroyed_Building @ AF - 043F430C

Owner reference: Civie1Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CATEXS04), owner Civie1, cell (108, 86), tag 043F422C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Reinforce_CIV1 @ AF (07A6429C)](#trigger-07a6429c).
2. Disable [Reinforce_CIV2 @ AF (043F1A2C)](#trigger-043f1a2c).
3. Disable [Reinforce_CIV3 @ AF (043F2E4C)](#trigger-043f2e4c).
4. Disable [Reinforce_CIVs @ AF (043F3C7C)](#trigger-043f3c7c).
5. Set local flag 7 (@AF Destroyed).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5184, Events line 5325, Actions line 5466.

<a id="trigger-043f413c"></a>

### 109. Destroyed_Building @ AG - 043F413C

Owner reference: Civie1Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAWASH05), owner Civie1, cell (96, 116), tag 043F405C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Reinforce_CIV1 @ AG (07A641AC)](#trigger-07a641ac).
2. Disable [Reinforce_CIV2 @ AG (043F193C)](#trigger-043f193c).
3. Disable [Reinforce_CIV3 @ AG (043F2D5C)](#trigger-043f2d5c).
4. Disable [Reinforce_CIVs @ AG (043F3B8C)](#trigger-043f3b8c).
5. Set local flag 8 (@AG Destroyed).
6. Stop location sound 32 at waypoint 32 (cell 97, 118).
7. Stop location sound 48 at waypoint 48 (cell 104, 107).
8. Stop location sound 503 at waypoint 503 (cell 111, 100).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5185, Events line 5326, Actions line 5467.

<a id="trigger-07a0b8ec"></a>

### 110. _Amb_Drone @ AG - 07A0B8EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0B80C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 62 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 32 (cell 97, 118).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5186, Events line 5327, Actions line 5468.

<a id="trigger-07a0babc"></a>

### 111. _Amb_Drone @ AW - 07A0BABC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0B9DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 113 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 48 (cell 104, 107).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5187, Events line 5328, Actions line 5469.

<a id="trigger-07a0a0ac"></a>

### 112. _Amb_Drone @ SJ - 07A0A0AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0BF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 72 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 503 (cell 111, 100).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5188, Events line 5329, Actions line 5470.

<a id="trigger-07a6450c"></a>

### 113. Destroyed_Building @ AB - 07A6450C

Owner reference: Civie1Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Smithsonian Natural History Museum (CAWASH17), owner Civie1, cell (113, 103), tag 07A10D5C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Reinforce_CIV1 @ AB (07A647DC)](#trigger-07a647dc).
2. Disable [Reinforce_CIV2 @ AB (08EF48EC)](#trigger-08ef48ec).
3. Disable [Reinforce_CIV3 @ AB (043F224C)](#trigger-043f224c).
4. Disable [Reinforce_CIVs @ AB (043F291C)](#trigger-043f291c).
5. Set local flag 3 (@AB Destroyed).
6. Stop location sound 27 at waypoint 27 (cell 115, 107).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5189, Events line 5330, Actions line 5471.

<a id="trigger-07a0b1ac"></a>

### 114. _Amb_Drone @ AB - 07A0B1AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0B0CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 68 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 27 (cell 115, 107).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5190, Events line 5331, Actions line 5472.

<a id="trigger-07a10c6c"></a>

### 115. Destroyed_Building @ AC - 07A10C6C

Owner reference: Civie1Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAPARS10), owner Civie1, cell (95, 83), tag 07A10B8C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Reinforce_CIV1 @ AC (07A646EC)](#trigger-07a646ec).
2. Disable [Reinforce_CIV2 @ AC (08EF47FC)](#trigger-08ef47fc).
3. Disable [Reinforce_CIV3 @ AC (043F215C)](#trigger-043f215c).
4. Disable [Reinforce_CIVs @ AC (043F282C)](#trigger-043f282c).
5. Set local flag 4 (@AC Destroyed).
6. Stop location sound 28 at waypoint 28 (cell 97, 86).
7. Stop location sound 504 at waypoint 504 (cell 104, 82).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5191, Events line 5332, Actions line 5473.

<a id="trigger-07a0b37c"></a>

### 116. _Amb_Drone @ AC - 07A0B37C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0B29C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 101 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 28 (cell 97, 86).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5192, Events line 5333, Actions line 5474.

<a id="trigger-07a1355c"></a>

### 117. _Amb_Drone @ SK - 07A1355C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A1227C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 97 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 504 (cell 104, 82).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5193, Events line 5334, Actions line 5475.

<a id="trigger-05fb472c"></a>

### 118. Destoyed_Grinder - 05FB472C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Sell_Grinder (09259C7C)](#trigger-09259c7c).

Attached scope: Grinder (YAGRND), owner Civie3, cell (108, 64), tag 09259B9C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Destoyed_Grinder (05FB472C)](#trigger-05fb472c).
2. Destroy Tag; main setting 07A648CC.
3. Destroy Tag; main setting 08EF49DC.
4. Destroy Tag; main setting 043F233C.
5. Destroy Tag; main setting 043F2B8C.
6. Enable and reset applicable timers for [Sell_Left Grind Gatt (07867E5C)](#trigger-07867e5c).
7. Enable and reset applicable timers for [Sell_Right Grind Gatt (0786756C)](#trigger-0786756c).
8. Enable and reset applicable timers for [Sell_Bio Reactor@Grind (0786714C)](#trigger-0786714c).
9. Enable and reset applicable timers for [Destroyed_Grnd Free Civ (0603712C)](#trigger-0603712c).
10. Create crate type 0 at waypoint 16 (cell 109, 65).
11. Disable [VO_Zofia_RE_Grinder (048C0C6C)](#trigger-048c0c6c).
12. Enable and reset applicable timers for [_Amb_Stop all Drones (05C1C75C)](#trigger-05c1c75c).
13. Make side cheer: owner selector 22 (country/type SOVIETSCOUNTRY; placed owner Soviets).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5194, Events line 5335, Actions line 5476.

<a id="trigger-0603712c"></a>

### 119. Destroyed_Grnd Free Civ - 0603712C

Owner reference: Civie3Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destoyed_Grinder (05FB472C)](#trigger-05fb472c).

Attached scope: tag definitions 060313EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 19 (country/type CIVIE1COUNTRY; placed owner Civie1).
2. Make side cheer: owner selector 19 (country/type CIVIE1COUNTRY; placed owner Civie1).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5195, Events line 5336, Actions line 5477.

<a id="trigger-08cbacbc"></a>

### 120. _Amb_Lon_Wind Cold - 08CBACBC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CBABDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 520 (cell 86, 108).
2. Play sound _Amb_WindCold at waypoint 521 (cell 59, 101).
3. Play sound _Amb_WindCold at waypoint 522 (cell 26, 62).
4. Play sound _Amb_WindCold at waypoint 523 (cell 55, 42).
5. Play sound _Amb_WindCold at waypoint 524 (cell 65, 47).
6. Play sound _Amb_WindCold at waypoint 525 (cell 75, 40).
7. Play sound _Amb_WindCold at waypoint 526 (cell 62, 27).
8. Play sound _Amb_WindCold at waypoint 527 (cell 53, 29).
9. Play sound _Amb_WindCold at waypoint 528 (cell 78, 26).
10. Play sound _Amb_WindCold at waypoint 529 (cell 119, 87).
11. Play sound _Amb_WindCold at waypoint 530 (cell 113, 69).
12. Play sound _Amb_WindCold at waypoint 531 (cell 105, 58).
13. Play sound _Amb_WindCold at waypoint 532 (cell 99, 67).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5196, Events line 5337, Actions line 5478.

<a id="trigger-08cbaaec"></a>

### 121. _Amb_Thames_Waves Lake1 - 08CBAAEC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CBAA0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WavesLake at waypoint 506 (cell 83, 126).
2. Play sound _Amb_WavesLake at waypoint 507 (cell 75, 120).
3. Play sound _Amb_WavesLake at waypoint 508 (cell 81, 113).
4. Play sound _Amb_WavesLake at waypoint 509 (cell 72, 101).
5. Play sound _Amb_WavesLake at waypoint 510 (cell 80, 96).
6. Play sound _Amb_WavesLake at waypoint 511 (cell 72, 84).
7. Play sound _Amb_WavesLake at waypoint 512 (cell 77, 79).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5197, Events line 5338, Actions line 5479.

<a id="trigger-08cba91c"></a>

### 122. _Amb_Lon_Urban Murmur1b - 08CBA91C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CBA83C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 501 (cell 56, 74).
2. Play sound _Amb_UrbanMurmur1 at waypoint 502 (cell 48, 63).
3. Play sound _Amb_UrbanMurmur1 at waypoint 503 (cell 111, 100).
4. Play sound _Amb_UrbanMurmur1 at waypoint 504 (cell 104, 82).
5. Play sound _Amb_UrbanMurmur1 at waypoint 505 (cell 134, 82).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5198, Events line 5339, Actions line 5480.

<a id="trigger-08cba74c"></a>

### 123. _Amb_Lon_Urban Murmur1a - 08CBA74C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CBA66C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 494 (cell 21, 68).
2. Play sound _Amb_UrbanMurmur1 at waypoint 495 (cell 25, 54).
3. Play sound _Amb_UrbanMurmur1 at waypoint 496 (cell 33, 47).
4. Play sound _Amb_UrbanMurmur1 at waypoint 497 (cell 36, 37).
5. Play sound _Amb_UrbanMurmur1 at waypoint 498 (cell 31, 85).
6. Play sound _Amb_UrbanMurmur1 at waypoint 499 (cell 45, 56).
7. Play sound _Amb_UrbanMurmur1 at waypoint 500 (cell 43, 78).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5199, Events line 5340, Actions line 5481.

<a id="trigger-044128bc"></a>

### 124. _Amb_Thames_Waves Lake2 - 044128BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 044127DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WavesLake at waypoint 513 (cell 76, 71).
2. Play sound _Amb_WavesLake at waypoint 514 (cell 83, 64).
3. Play sound _Amb_WavesLake at waypoint 515 (cell 75, 58).
4. Play sound _Amb_WavesLake at waypoint 516 (cell 92, 57).
5. Play sound _Amb_WavesLake at waypoint 517 (cell 82, 45).
6. Play sound _Amb_WavesLake at waypoint 518 (cell 96, 43).
7. Play sound _Amb_WavesLake at waypoint 519 (cell 87, 38).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5200, Events line 5341, Actions line 5482.

<a id="trigger-09d40d1c"></a>

### 125. _Amb_Storm Sounds - 09D40D1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09D4403C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 250 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Play sound WeatherStrike.

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5201, Events line 5342, Actions line 5483.

<a id="trigger-08af298c"></a>

### 126. _Setup_Civ3 Inits 2 Bio - 08AF298C

Owner reference: Civie3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08AF28AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_3 Inits 2 Grinder Bio (07F33A4C)](sov03umd-teams.md#team-07f33a4c) at waypoint 33 (cell 103, 59).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5202, Events line 5343, Actions line 5484.

<a id="trigger-08af27bc"></a>

### 127. _Setup_Yuri Inits 2 Bio - 08AF27BC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08AF26DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 34 (cell 75, 43).
2. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 35 (cell 72, 39).
3. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 36 (cell 66, 42).
4. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 37 (cell 70, 45).
5. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 38 (cell 68, 47).
6. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 39 (cell 59, 43).
7. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 40 (cell 55, 47).
8. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 41 (cell 53, 40).
9. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 42 (cell 54, 29).
10. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 43 (cell 55, 20).
11. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 44 (cell 62, 14).
12. Supply reinforcement team [TM_BG2_6 Initiates into Bio (08FC8B7C)](sov03umd-teams.md#team-08fc8b7c) at waypoint 45 (cell 69, 15).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5203, Events line 5344, Actions line 5485.

<a id="trigger-086d316c"></a>

### 128. Detect_War Factory Dead - 086D316C

Owner reference: BadGuy1Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied War Factory (GAWEAP), owner BadGuy1, cell (55, 100), tag 086D308C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Create_BG1_1 Grizzly TM (086D7C6C)](#trigger-086d7c6c).
2. Disable [Create_BG1_2 IFV Team (086D555C)](#trigger-086d555c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5204, Events line 5345, Actions line 5486.

<a id="trigger-08723a1c"></a>

### 129. Delay_Grizzly/IFV Teams - 08723A1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0872393C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 250 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create_BG1_1 Grizzly TM (086D7C6C)](#trigger-086d7c6c).
2. Enable and reset applicable timers for [Create_BG1_2 IFV Team (086D555C)](#trigger-086d555c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5205, Events line 5346, Actions line 5487.

<a id="trigger-07a0be5c"></a>

### 130. _Amb_Drone @ AY - 07A0BE5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0BD7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 131 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 50 (cell 99, 73).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5206, Events line 5347, Actions line 5488.

<a id="trigger-07a0bc8c"></a>

### 131. _Amb_Drone @ AX - 07A0BC8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0BBAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 84 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 49 (cell 114, 76).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5207, Events line 5348, Actions line 5489.

<a id="trigger-07a0b71c"></a>

### 132. _Amb_Drone @ AF - 07A0B71C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0B63C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 141 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 31 (cell 109, 88).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5208, Events line 5349, Actions line 5490.

<a id="trigger-07a0b54c"></a>

### 133. _Amb_Drone @ AD - 07A0B54C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A0B46C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 86 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 29 (cell 90, 81).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5209, Events line 5350, Actions line 5491.

<a id="trigger-07a15dbc"></a>

### 134. _Amb_Drone @ TK - 07A15DBC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A12ACC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 110 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_LondonCivilians at waypoint 530 (cell 113, 69).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5210, Events line 5351, Actions line 5492.

<a id="trigger-091ed06c"></a>

### 135. _Amb_Detect_AD_AE Dead - 091ED06C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 091EA07C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (@AD Destroyed) is set.
2. local flag 6 (@AE Destroyed) is set.

Flag writers in this mission: set local flag 5 (@AD Destroyed) at [Destroyed_Building @ AD (043F46AC)](#trigger-043f46ac); set local flag 6 (@AE Destroyed) at [Destroyed_Building @ AE (043F44DC)](#trigger-043f44dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Stop location sound 29 at waypoint 29 (cell 90, 81).
2. Stop location sound 50 at waypoint 50 (cell 99, 73).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5211, Events line 5352, Actions line 5493.

<a id="trigger-091ef07c"></a>

### 136. _Amb_Detect_AB_AF Dead - 091EF07C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 091EAF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (@AB Destroyed) is set.
2. local flag 7 (@AF Destroyed) is set.

Flag writers in this mission: set local flag 3 (@AB Destroyed) at [Destroyed_Building @ AB (07A6450C)](#trigger-07a6450c); set local flag 7 (@AF Destroyed) at [Destroyed_Building @ AF (043F430C)](#trigger-043f430c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Stop location sound 31 at waypoint 31 (cell 109, 88).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5212, Events line 5353, Actions line 5494.

<a id="trigger-091efe5c"></a>

### 137. _Amb_Detect_AA->AG Dead - 091EFE5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 091EFD7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (@AA Destroyed) is set.
2. local flag 3 (@AB Destroyed) is set.
3. local flag 4 (@AC Destroyed) is set.
4. local flag 5 (@AD Destroyed) is set.
5. local flag 6 (@AE Destroyed) is set.
6. local flag 7 (@AF Destroyed) is set.
7. local flag 8 (@AG Destroyed) is set.

Flag writers in this mission: set local flag 2 (@AA Destroyed) at [Destroyed_Building @ AA (043F3A9C)](#trigger-043f3a9c); set local flag 3 (@AB Destroyed) at [Destroyed_Building @ AB (07A6450C)](#trigger-07a6450c); set local flag 4 (@AC Destroyed) at [Destroyed_Building @ AC (07A10C6C)](#trigger-07a10c6c); set local flag 5 (@AD Destroyed) at [Destroyed_Building @ AD (043F46AC)](#trigger-043f46ac); set local flag 6 (@AE Destroyed) at [Destroyed_Building @ AE (043F44DC)](#trigger-043f44dc); set local flag 7 (@AF Destroyed) at [Destroyed_Building @ AF (043F430C)](#trigger-043f430c); set local flag 8 (@AG Destroyed) at [Destroyed_Building @ AG (043F413C)](#trigger-043f413c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Stop location sound 530 at waypoint 530 (cell 113, 69).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5213, Events line 5354, Actions line 5495.

<a id="trigger-091efc8c"></a>

### 138. _Amb_AA - 091EFC8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 2 (@AA Destroyed) is set.
2. local flag 3 (@AB Destroyed) is set.
3. local flag 4 (@AC Destroyed) is set.
4. local flag 7 (@AF Destroyed) is set.

Flag writers in this mission: set local flag 2 (@AA Destroyed) at [Destroyed_Building @ AA (043F3A9C)](#trigger-043f3a9c); set local flag 3 (@AB Destroyed) at [Destroyed_Building @ AB (07A6450C)](#trigger-07a6450c); set local flag 4 (@AC Destroyed) at [Destroyed_Building @ AC (07A10C6C)](#trigger-07a10c6c); set local flag 7 (@AF Destroyed) at [Destroyed_Building @ AF (043F430C)](#trigger-043f430c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [_Amb_Drone @ AX (07A0BC8C)](#trigger-07a0bc8c).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5214, Events line 5355, Actions line 5496.

<a id="trigger-ab"></a>

### 139. _Amb_AA_AB_AC_AF Dead - AB

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 091EFBAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (@AA Destroyed) is set.
2. local flag 3 (@AB Destroyed) is set.
3. local flag 4 (@AC Destroyed) is set.
4. local flag 7 (@AF Destroyed) is set.

Flag writers in this mission: set local flag 2 (@AA Destroyed) at [Destroyed_Building @ AA (043F3A9C)](#trigger-043f3a9c); set local flag 3 (@AB Destroyed) at [Destroyed_Building @ AB (07A6450C)](#trigger-07a6450c); set local flag 4 (@AC Destroyed) at [Destroyed_Building @ AC (07A10C6C)](#trigger-07a10c6c); set local flag 7 (@AF Destroyed) at [Destroyed_Building @ AF (043F430C)](#trigger-043f430c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Stop location sound 49 at waypoint 49 (cell 114, 76).

Source locator: mapsmd03.mix/sov03umd.map; Triggers line 5215, Events line 5356, Actions line 5497.

[All team rosters and ordered plans](sov03umd-teams.md) | [All mission overrides](sov03umd-overrides.md)
