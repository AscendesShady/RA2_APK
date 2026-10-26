# Operation: Brain Dead

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all07smd.map. **Effective extracted member:** mapsmd03.mix/all07smd.map. **Trigger definitions:** 88.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all07smd-teams.md) | [All mission overrides](all07smd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Americans |
| Theater | SNOW |
| Map size | 0,0,130,140 |
| Visible local rectangle | 15,13,100,110 |
| Placed vehicles | 53 |
| Placed infantry | 38 |
| Placed structures | 136 |
| Placed aircraft | 0 |
| Team templates | 118 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 150 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 1000 | Africans |
| 6 | Arabs | 100 | Arabs |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 0 | Russians |
| 9 | YuriCountry | 1000 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 0 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |
| 14 | Yuri2 | 1000 | Yuri2Country |
| 15 | Yuri3 | 1000 | Yuri3Country |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Has_Soviet_Barrack,0 |
| 1 | Has_Soviet_WarFac,0 |
| 2 | Make_Hover1,0 |
| 3 | Make_HoverTD,0 |
| 4 | Send_Barracks1,0 |
| 5 | Send_Barracks2,0 |
| 6 | Send_Barracks3,0 |
| 7 | Make_HoverTF,0 |
| 8 | Send_Barracks4,0 |
| 9 | Make_HoverTH,0 |
| 10 | Send_WarFac1,0 |
| 11 | Send_WarFac2,0 |
| 12 | Send_WarFac3,0 |
| 13 | Send_WarFac4,0 |
| 14 | Send_WarFac5,0 |
| 15 | Has_Soviet_Radar,1 |
| 16 | Make_HoverTJ,0 |
| 17 | Has_Naval_Yard,0 |
| 18 | Make_HoverTL,0 |
| 19 | Make_HoverTN,0 |
| 20 | Make_HoverTP,0 |
| 21 | Make_HoverTR,0 |
| 22 | Send_Barracks5,0 |
| 23 | MCV_Arrived,0 |
| 24 | Main_ConYards_Gone,0 |
| 25 | Yuri_ConYard_Gone,0 |
| 26 | Yuri2_ConYard_Gone,0 |
| 27 | WarTeam1_Gone,1 |
| 28 | Yuri_Prime_Built,0 |
| 29 | Has_Allied_BLab,0 |
| 30 | Has_Allied_WarF,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [PlayerLose (08ED7A3C)](#trigger-08ed7a3c) | Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).<br>3 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |
| [PlayerWin (06B9B43C)](#trigger-06b9b43c) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner. |
| [Announce_Tierra_Lose (0A57B28C)](#trigger-0a57b28c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |

## Every trigger, in file order

<a id="trigger-0de26e5c"></a>

### 1. Camera_Start - 0DE26E5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0DE2670C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 79 (cell 67, 96).
2. Reveal terrain around waypoint 79 (cell 67, 96).
3. Reveal terrain around waypoint 81 (cell 71, 102).
4. Reveal terrain around waypoint 80 (cell 77, 110).
5. Disable player input.
6. Play in-game movie 28.
7. Reveal terrain around waypoint 78 (cell 84, 125).
8. Set local flag 27 (WarTeam1_Gone).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10651, Events line 10741, Actions line 10831.

<a id="trigger-0de1124c"></a>

### 2. Send_Engineer1 - 0DE1124C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0DE12CAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Player_Engineer1 (0B1DF85C)](all07smd-teams.md#team-0b1df85c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10652, Events line 10742, Actions line 10832.

<a id="trigger-06c3397c"></a>

### 3. Change_to_USSR - 06C3397C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06C37DDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type SPECIAL; placed owner Special).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10653, Events line 10743, Actions line 10833.

<a id="trigger-0de086ac"></a>

### 4. Follow_Engineers - 0DE086AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0DE0838C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 78 (cell 84, 125) with speed setting 1.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10654, Events line 10744, Actions line 10834.

<a id="trigger-094e805c"></a>

### 5. Eva_Briefing - 094E805C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 094EA10C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification A07_p01.
2. Enable and reset applicable timers for [Control_Return (0BB2E0FC)](#trigger-0bb2e0fc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10655, Events line 10745, Actions line 10835.

<a id="trigger-0bb2e0fc"></a>

### 6. Control_Return - 0BB2E0FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Eva_Briefing (094E805C)](#trigger-094e805c).

Attached scope: tag definitions 0BB2828C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 38 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_BattlefieldControlOnline.
2. Enable player input.
3. Enable and reset applicable timers for [PlayerLose (08ED7A3C)](#trigger-08ed7a3c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10656, Events line 10746, Actions line 10836.

<a id="trigger-08ed7a3c"></a>

### 7. PlayerLose - 08ED7A3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Control_Return (0BB2E0FC)](#trigger-0bb2e0fc).

Attached scope: tag definitions 08ED74BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10657, Events line 10747, Actions line 10837.

<a id="trigger-0c8d4f3c"></a>

### 8. Cheer - 0C8D4F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win_Check (07CA72BC)](#trigger-07ca72bc).

Attached scope: tag definitions 0C8D485C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10658, Events line 10748, Actions line 10838.

<a id="trigger-06b9b43c"></a>

### 9. PlayerWin - 06B9B43C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win_Check (07CA72BC)](#trigger-07ca72bc).

Attached scope: tag definitions 06B98DDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10659, Events line 10749, Actions line 10839.

<a id="trigger-0955dd2c"></a>

### 10. Start_GIs - 0955DD2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0955D4DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Start_GIs (0955CEFC)](all07smd-teams.md#team-0955cefc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10660, Events line 10750, Actions line 10840.

<a id="trigger-0960df3c"></a>

### 11. SBarracks_Built - 0960DF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0960DA2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 11 (global list position: Soviet Barracks (NAHAND)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 0 (Has_Soviet_Barrack).
2. Set local flag 4 (Send_Barracks1).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10661, Events line 10751, Actions line 10841.

<a id="trigger-0960d93c"></a>

### 12. Yuri_Barracks1 - 0960D93C

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Barracks_5 (0B829CAC)](#trigger-0b829cac).

Attached scope: tag definitions 0960D35C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Has_Soviet_WarFac) is clear.
2. local flag 4 (Send_Barracks1) is set.
3. local flag 0 (Has_Soviet_Barrack) is set.
4. 75 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 4 (Send_Barracks1) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriBarracks_1 (08D5D5FC)](all07smd-teams.md#team-08d5d5fc).
2. Enable and reset applicable timers for [Send_Hover1_Home (0BDCA03C)](#trigger-0bdca03c).
3. Enable and reset applicable timers for [Yuri_Barracks2 (0464C5FC)](#trigger-0464c5fc).
4. Disable [Yuri_Barracks1 (0960D93C)](#trigger-0960d93c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10662, Events line 10752, Actions line 10842.

<a id="trigger-0bdca03c"></a>

### 13. Send_Hover1_Home - 0BDCA03C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Barracks1 (0960D93C)](#trigger-0960d93c).

Attached scope: tag definitions 0DE78B6C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Make_Hover1) is set.

Flag writers in this mission: clear local flag 2 (Make_Hover1) at [Send_Hover1_Home (0BDCA03C)](#trigger-0bdca03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Hover_TA (08D68B7C)](all07smd-teams.md#team-08d68b7c).
2. Clear local flag 2 (Make_Hover1).
3. Disable [Send_Hover1_Home (0BDCA03C)](#trigger-0bdca03c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10663, Events line 10753, Actions line 10843.

<a id="trigger-0464c5fc"></a>

### 14. Yuri_Barracks2 - 0464C5FC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Barracks1 (0960D93C)](#trigger-0960d93c).

Attached scope: tag definitions 0464D33C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Has_Soviet_WarFac) is clear.
2. local flag 5 (Send_Barracks2) is set.
3. local flag 0 (Has_Soviet_Barrack) is set.
4. 75 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriBarracks_2 (08D686CC)](all07smd-teams.md#team-08d686cc).
2. Enable and reset applicable timers for [Send_HoverTD_Home (0464D1BC)](#trigger-0464d1bc).
3. Enable and reset applicable timers for [Yuri_Barracks3 (0B7AE1EC)](#trigger-0b7ae1ec).
4. Disable [Yuri_Barracks2 (0464C5FC)](#trigger-0464c5fc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10664, Events line 10754, Actions line 10844.

<a id="trigger-0464d1bc"></a>

### 15. Send_HoverTD_Home - 0464D1BC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Barracks2 (0464C5FC)](#trigger-0464c5fc).

Attached scope: tag definitions 0464D04C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Make_HoverTD) is set.

Flag writers in this mission: clear local flag 3 (Make_HoverTD) at [Send_HoverTD_Home (0464D1BC)](#trigger-0464d1bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Hover_TD (08D6821C)](all07smd-teams.md#team-08d6821c).
2. Clear local flag 3 (Make_HoverTD).
3. Disable [Send_HoverTD_Home (0464D1BC)](#trigger-0464d1bc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10665, Events line 10755, Actions line 10845.

<a id="trigger-0b7ae1ec"></a>

### 16. Yuri_Barracks3 - 0B7AE1EC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Barracks2 (0464C5FC)](#trigger-0464c5fc).

Attached scope: tag definitions 0B7A96EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Has_Soviet_WarFac) is clear.
2. local flag 6 (Send_Barracks3) is set.
3. local flag 0 (Has_Soviet_Barrack) is set.
4. 90 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriBarracks_3 (08D680EC)](all07smd-teams.md#team-08d680ec).
2. Enable and reset applicable timers for [Send_HoverTF_Home (0B7A95FC)](#trigger-0b7a95fc).
3. Enable and reset applicable timers for [Yuri_Barracks4 (0B2E9EDC)](#trigger-0b2e9edc).
4. Disable [Yuri_Barracks3 (0B7AE1EC)](#trigger-0b7ae1ec).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10666, Events line 10756, Actions line 10846.

<a id="trigger-0b7a95fc"></a>

### 17. Send_HoverTF_Home - 0B7A95FC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Barracks3 (0B7AE1EC)](#trigger-0b7ae1ec).

Attached scope: tag definitions 0B7A948C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (Make_HoverTF) is set.

Flag writers in this mission: clear local flag 7 (Make_HoverTF) at [Send_HoverTF_Home (0B7A95FC)](#trigger-0b7a95fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_HoverTF (08D6990C)](all07smd-teams.md#team-08d6990c).
2. Clear local flag 7 (Make_HoverTF).
3. Disable [Send_HoverTF_Home (0B7A95FC)](#trigger-0b7a95fc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10667, Events line 10757, Actions line 10847.

<a id="trigger-0b2e9edc"></a>

### 18. Yuri_Barracks4 - 0B2E9EDC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Barracks3 (0B7AE1EC)](#trigger-0b7ae1ec).

Attached scope: tag definitions 0B2E96BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Has_Soviet_WarFac) is clear.
2. 90 configured time units have elapsed since the trigger timer was initialized/reset.
3. local flag 8 (Send_Barracks4) is set.
4. local flag 0 (Has_Soviet_Barrack) is set.

Flag writers in this mission: set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriBarracks_4 (08D6945C)](all07smd-teams.md#team-08d6945c).
2. Enable and reset applicable timers for [Send_HoverTH_Home (0B2BD0FC)](#trigger-0b2bd0fc).
3. Enable and reset applicable timers for [Yuri_Barracks_5 (0B829CAC)](#trigger-0b829cac).
4. Disable [Yuri_Barracks4 (0B2E9EDC)](#trigger-0b2e9edc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10668, Events line 10758, Actions line 10848.

<a id="trigger-0b2bd0fc"></a>

### 19. Send_HoverTH_Home - 0B2BD0FC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Barracks4 (0B2E9EDC)](#trigger-0b2e9edc).

Attached scope: tag definitions 0B2B893C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (Make_HoverTH) is set.

Flag writers in this mission: clear local flag 9 (Make_HoverTH) at [Send_HoverTH_Home (0B2BD0FC)](#trigger-0b2bd0fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_HoverTH (08D6AD2C)](all07smd-teams.md#team-08d6ad2c).
2. Clear local flag 9 (Make_HoverTH).
3. Disable [Send_HoverTH_Home (0B2BD0FC)](#trigger-0b2bd0fc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10669, Events line 10759, Actions line 10849.

<a id="trigger-0b829cac"></a>

### 20. Yuri_Barracks_5 - 0B829CAC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_Barracks4 (0B2E9EDC)](#trigger-0b2e9edc).

Attached scope: tag definitions 0B82E89C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Has_Soviet_WarFac) is clear.
2. local flag 22 (Send_Barracks5) is set.
3. local flag 0 (Has_Soviet_Barrack) is set.
4. 90 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriBarracks5 (08D6A1CC)](all07smd-teams.md#team-08d6a1cc).
2. Enable and reset applicable timers for [Yuri_Barracks1 (0960D93C)](#trigger-0960d93c).
3. Disable [Yuri_Barracks_5 (0B829CAC)](#trigger-0b829cac).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10670, Events line 10760, Actions line 10850.

<a id="trigger-046336ec"></a>

### 21. SWarFac_Built - 046336EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0463122C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 14 (global list position: Soviet War Factory (NAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 1 (Has_Soviet_WarFac).
2. Set local flag 10 (Send_WarFac1).
3. Enable and reset applicable timers for [Yuri_WarFac1 (09713F3C)](#trigger-09713f3c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10671, Events line 10761, Actions line 10851.

<a id="trigger-09713f3c"></a>

### 22. Yuri_WarFac1 - 09713F3C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SWarFac_Built (046336EC)](#trigger-046336ec); enable from [Yuri_WarFac5 (0B807B1C)](#trigger-0b807b1c).

Attached scope: tag definitions 09713E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 27 (WarTeam1_Gone) is set.
2. local flag 0 (Has_Soviet_Barrack) is set.
3. local flag 1 (Has_Soviet_WarFac) is set.
4. local flag 10 (Send_WarFac1) is set.
5. 90 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 27 (WarTeam1_Gone) at [Camera_Start (0DE26E5C)](#trigger-0de26e5c); clear local flag 27 (WarTeam1_Gone) at [Yuri_WarFac1 (09713F3C)](#trigger-09713f3c); set local flag 27 (WarTeam1_Gone) at [Confed_Check (079B37CC)](#trigger-079b37cc); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c); set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 10 (Send_WarFac1) at [SWarFac_Built (046336EC)](#trigger-046336ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriWarFac1 (08D57B5C)](all07smd-teams.md#team-08d57b5c).
2. Enable and reset applicable timers for [Send_HoverTJ_Home (096A485C)](#trigger-096a485c).
3. Enable and reset applicable timers for [Yuri_WarFac2 (0B8000CC)](#trigger-0b8000cc).
4. Clear local flag 27 (WarTeam1_Gone).
5. Enable and reset applicable timers for [Confed_Check (079B37CC)](#trigger-079b37cc).
6. Disable [Yuri_WarFac1 (09713F3C)](#trigger-09713f3c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10672, Events line 10762, Actions line 10852.

<a id="trigger-096a485c"></a>

### 23. Send_HoverTJ_Home - 096A485C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac1 (09713F3C)](#trigger-09713f3c).

Attached scope: tag definitions 096A454C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 16 (Make_HoverTJ) is set.

Flag writers in this mission: clear local flag 16 (Make_HoverTJ) at [Send_HoverTJ_Home (096A485C)](#trigger-096a485c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_HoverTJ (08D68C8C)](all07smd-teams.md#team-08d68c8c).
2. Clear local flag 16 (Make_HoverTJ).
3. Disable [Send_HoverTJ_Home (096A485C)](#trigger-096a485c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10673, Events line 10763, Actions line 10853.

<a id="trigger-0b8000cc"></a>

### 24. Yuri_WarFac2 - 0B8000CC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac1 (09713F3C)](#trigger-09713f3c).

Attached scope: tag definitions 0B80048C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 11 (Send_WarFac2) is set.
2. local flag 1 (Has_Soviet_WarFac) is set.
3. local flag 0 (Has_Soviet_Barrack) is set.
4. 90 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriWarFac2 (08D6BA4C)](all07smd-teams.md#team-08d6ba4c).
2. Enable and reset applicable timers for [Send_HoverTL_Home (0B7F91AC)](#trigger-0b7f91ac).
3. Enable and reset applicable timers for [Yuri_WarFac3 (0B80C2BC)](#trigger-0b80c2bc).
4. Disable [Yuri_WarFac2 (0B8000CC)](#trigger-0b8000cc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10674, Events line 10764, Actions line 10854.

<a id="trigger-079b37cc"></a>

### 25. Confed_Check - 079B37CC

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac1 (09713F3C)](#trigger-09713f3c).

Attached scope: tag definitions 079B311C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 27 (WarTeam1_Gone).
2. Disable [Confed_Check (079B37CC)](#trigger-079b37cc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10675, Events line 10765, Actions line 10855.

<a id="trigger-0b7f91ac"></a>

### 26. Send_HoverTL_Home - 0B7F91AC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac2 (0B8000CC)](#trigger-0b8000cc).

Attached scope: tag definitions 0B80F9CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 18 (Make_HoverTL) is set.

Flag writers in this mission: clear local flag 18 (Make_HoverTL) at [Send_HoverTL_Home (0B7F91AC)](#trigger-0b7f91ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_HoverTL (08D6B59C)](all07smd-teams.md#team-08d6b59c).
2. Clear local flag 18 (Make_HoverTL).
3. Disable [Send_HoverTL_Home (0B7F91AC)](#trigger-0b7f91ac).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10676, Events line 10766, Actions line 10856.

<a id="trigger-0b80c2bc"></a>

### 27. Yuri_WarFac3 - 0B80C2BC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac2 (0B8000CC)](#trigger-0b8000cc).

Attached scope: tag definitions 0B80B08C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 12 (Send_WarFac3) is set.
2. local flag 1 (Has_Soviet_WarFac) is set.
3. local flag 0 (Has_Soviet_Barrack) is set.
4. 90 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriWarFac3 (08D6CB7C)](all07smd-teams.md#team-08d6cb7c).
2. Enable and reset applicable timers for [Send_HoverTN_Home (0B7FE1AC)](#trigger-0b7fe1ac).
3. Enable and reset applicable timers for [Yuri_WarFac4 (0B82737C)](#trigger-0b82737c).
4. Disable [Yuri_WarFac3 (0B80C2BC)](#trigger-0b80c2bc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10677, Events line 10767, Actions line 10857.

<a id="trigger-0b7fe1ac"></a>

### 28. Send_HoverTN_Home - 0B7FE1AC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac3 (0B80C2BC)](#trigger-0b80c2bc).

Attached scope: tag definitions 0B80763C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 19 (Make_HoverTN) is set.

Flag writers in this mission: clear local flag 19 (Make_HoverTN) at [Send_HoverTN_Home (0B7FE1AC)](#trigger-0b7fe1ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_HoverTN (08D6C6CC)](all07smd-teams.md#team-08d6c6cc).
2. Clear local flag 19 (Make_HoverTN).
3. Disable [Send_HoverTN_Home (0B7FE1AC)](#trigger-0b7fe1ac).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10678, Events line 10768, Actions line 10858.

<a id="trigger-0b82737c"></a>

### 29. Yuri_WarFac4 - 0B82737C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac3 (0B80C2BC)](#trigger-0b80c2bc).

Attached scope: tag definitions 0B82462C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 13 (Send_WarFac4) is set.
2. local flag 1 (Has_Soviet_WarFac) is set.
3. local flag 0 (Has_Soviet_Barrack) is set.
4. 90 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriWarFac4 (08D6DC8C)](all07smd-teams.md#team-08d6dc8c).
2. Enable and reset applicable timers for [Send_HoverTP_Home (0B84B0FC)](#trigger-0b84b0fc).
3. Enable and reset applicable timers for [Yuri_WarFac5 (0B807B1C)](#trigger-0b807b1c).
4. Disable [Yuri_WarFac4 (0B82737C)](#trigger-0b82737c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10679, Events line 10769, Actions line 10859.

<a id="trigger-0b84b0fc"></a>

### 30. Send_HoverTP_Home - 0B84B0FC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac4 (0B82737C)](#trigger-0b82737c).

Attached scope: tag definitions 0B825B8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 20 (Make_HoverTP) is set.

Flag writers in this mission: clear local flag 20 (Make_HoverTP) at [Send_HoverTP_Home (0B84B0FC)](#trigger-0b84b0fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_HoverTP (08D6C21C)](all07smd-teams.md#team-08d6c21c).
2. Clear local flag 20 (Make_HoverTP).
3. Disable [Send_HoverTP_Home (0B84B0FC)](#trigger-0b84b0fc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10680, Events line 10770, Actions line 10860.

<a id="trigger-0b807b1c"></a>

### 31. Yuri_WarFac5 - 0B807B1C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac4 (0B82737C)](#trigger-0b82737c).

Attached scope: tag definitions 0B8A182C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 14 (Send_WarFac5) is set.
2. local flag 1 (Has_Soviet_WarFac) is set.
3. local flag 0 (Has_Soviet_Barrack) is set.
4. 90 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 1 (Has_Soviet_WarFac) at [SWarFac_Built (046336EC)](#trigger-046336ec); set local flag 0 (Has_Soviet_Barrack) at [SBarracks_Built (0960DF3C)](#trigger-0960df3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_YuriWarFac5 (08D6D18C)](all07smd-teams.md#team-08d6d18c).
2. Enable and reset applicable timers for [Send_HoverTR_Home (0B7F92FC)](#trigger-0b7f92fc).
3. Enable and reset applicable timers for [Yuri_WarFac1 (09713F3C)](#trigger-09713f3c).
4. Disable [Yuri_WarFac5 (0B807B1C)](#trigger-0b807b1c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10681, Events line 10771, Actions line 10861.

<a id="trigger-0b7f92fc"></a>

### 32. Send_HoverTR_Home - 0B7F92FC

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_WarFac5 (0B807B1C)](#trigger-0b807b1c).

Attached scope: tag definitions 0B80218C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 21 (Make_HoverTR) is set.

Flag writers in this mission: clear local flag 21 (Make_HoverTR) at [Send_HoverTR_Home (0B7F92FC)](#trigger-0b7f92fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_HoverTR (08D6D6FC)](all07smd-teams.md#team-08d6d6fc).
2. Clear local flag 21 (Make_HoverTR).
3. Disable [Send_HoverTR_Home (0B7F92FC)](#trigger-0b7f92fc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10682, Events line 10772, Actions line 10862.

<a id="trigger-0b2eb76c"></a>

### 33. SRadar_Built - 0B2EB76C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B2EB1BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 13 (global list position: Radar Tower (NARADR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 15 (Has_Soviet_Radar).
2. Enable and reset applicable timers for [Radar_Congrats (0F823B7C)](#trigger-0f823b7c).
3. Enable and reset applicable timers for [Countdown (0967D33C)](#trigger-0967d33c).
4. Disable [Player_Lose_Tierra (0A57F46C)](#trigger-0a57f46c).
5. Disable [Radar_Text (08F6724C)](#trigger-08f6724c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10683, Events line 10773, Actions line 10863.

<a id="trigger-0f823b7c"></a>

### 34. Radar_Congrats - 0F823B7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SRadar_Built (0B2EB76C)](#trigger-0b2eb76c).

Attached scope: tag definitions 0F83170C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA7_EvaMCVInbound.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10684, Events line 10774, Actions line 10864.

<a id="trigger-0967d33c"></a>

### 35. Countdown - 0967D33C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SRadar_Built (0B2EB76C)](#trigger-0b2eb76c).

Attached scope: tag definitions 0969795C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_A12_EvaCountdown.
2. Enable and reset applicable timers for [Chrono_MCV (0964B13C)](#trigger-0964b13c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10685, Events line 10775, Actions line 10865.

<a id="trigger-0a57f46c"></a>

### 36. Player_Lose_Tierra - 0A57F46C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change_RocketHouse (08E89B1C)](#trigger-08e89b1c).

Attached scope: tag definitions 0A57B37C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Soviet Construction Yard (NACNST) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Play voice notification EVA_CriticalStrucureLost.
2. Enable and reset applicable timers for [Announce_Tierra_Lose (0A57B28C)](#trigger-0a57b28c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10686, Events line 10776, Actions line 10866.

<a id="trigger-08f6724c"></a>

### 37. Radar_Text - 08F6724C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08F6F15C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Build a Soviet Radar Dish” (MISSION:Radar).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10687, Events line 10777, Actions line 10867.

<a id="trigger-0964b13c"></a>

### 38. Chrono_MCV - 0964B13C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Countdown (0967D33C)](#trigger-0967d33c).

Attached scope: tag definitions 0964F4BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [TEAM_Chrono_MCV (0964C97C)](all07smd-teams.md#team-0964c97c) at waypoint 26 (cell 105, 194).
2. Center Base Cell Set; main setting 26; location/duration field AA.
3. Enable and reset applicable timers for [Build_Yuri_SW (0460BDBC)](#trigger-0460bdbc).
4. Play sound ChronosphereMove.
5. Create radar-event marker type 1 at waypoint 26 (cell 105, 194).
6. Enable and reset applicable timers for [Build_Yuri_SW (0460BDBC)](#trigger-0460bdbc).
7. Set local flag 23 (MCV_Arrived).
8. Enable and reset applicable timers for [Chrono_Support (098DB96C)](#trigger-098db96c).
9. Enable and reset applicable timers for [Allied_MCV_Gone[Easy] (0908B62C)](#trigger-0908b62c).
10. Enable and reset applicable timers for [Allied_MCV_Gone(Med) (078BFF3C)](#trigger-078bff3c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10688, Events line 10778, Actions line 10868.

<a id="trigger-0a57b28c"></a>

### 39. Announce_Tierra_Lose - 0A57B28C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Lose_Tierra (0A57F46C)](#trigger-0a57f46c).

Attached scope: tag definitions 0A57B04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10689, Events line 10779, Actions line 10869.

<a id="trigger-0460bdbc"></a>

### 40. Build_Yuri_SW - 0460BDBC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono_MCV (0964B13C)](#trigger-0964b13c); enable from [Chrono_MCV (0964B13C)](#trigger-0964b13c).

Attached scope: tag definitions 0460BCDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create building YAGNTC at waypoint 194 (cell 168, 108).
2. Create building YAPPET at waypoint 419 (cell 221, 144).
3. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).
4. Superweapon Set Recharge Time; main setting 7; location/duration field 13500.
5. Enable and reset applicable timers for [Dominator_Gone (09000CDC)](#trigger-09000cdc).
6. Enable and reset applicable timers for [Detect_PD (0901213C)](#trigger-0901213c).
7. Enable and reset applicable timers for [Yuri_All_Attack (0780A03C)](#trigger-0780a03c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10690, Events line 10780, Actions line 10870.

<a id="trigger-098db96c"></a>

### 41. Chrono_Support - 098DB96C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono_MCV (0964B13C)](#trigger-0964b13c).

Attached scope: tag definitions 098DB65C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [TEAM_Chrono_Grizzly1 (04E3AA8C)](all07smd-teams.md#team-04e3aa8c) at waypoint 27 (cell 105, 190).
2. Supply chrono reinforcement team [TEAM_Chrono_Grizzly2 (04E3A75C)](all07smd-teams.md#team-04e3a75c) at waypoint 28 (cell 102, 192).
3. Supply chrono reinforcement team [TEAM_Chrono_Grizzly3 (04E40B3C)](all07smd-teams.md#team-04e40b3c) at waypoint 34 (cell 108, 192).
4. Supply chrono reinforcement team [TEAM_Chrono_IFV1 (04E403BC)](all07smd-teams.md#team-04e403bc) at waypoint 30 (cell 102, 196).
5. Supply chrono reinforcement team [TEAM_Chrono_IFV2 (04E4077C)](all07smd-teams.md#team-04e4077c) at waypoint 32 (cell 108, 196).
6. Supply chrono reinforcement team [TEAM_Chrono_Mirage1 (04E39A4C)](all07smd-teams.md#team-04e39a4c) at waypoint 29 (cell 102, 194).
7. Supply chrono reinforcement team [TEAM_Chrono_Mirage2 (04E4064C)](all07smd-teams.md#team-04e4064c) at waypoint 33 (cell 108, 194).
8. Supply chrono reinforcement team [TEAM_Chrono_Prism1 (04E4028C)](all07smd-teams.md#team-04e4028c) at waypoint 31 (cell 105, 198).
9. Display message “Objective: Destroy the Psychic Dominator on Antarctica” (MISSION:KillPD).
10. Enable and reset applicable timers for [Text_KillDominator (08F9A04C)](#trigger-08f9a04c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10691, Events line 10781, Actions line 10871.

<a id="trigger-0908b62c"></a>

### 42. Allied_MCV_Gone[Easy] - 0908B62C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [New_Countdown (0908B71C)](#trigger-0908b71c).

Incoming activation links: enable from [Chrono_MCV (0964B13C)](#trigger-0964b13c); enable from [New_MCV (098DC46C)](#trigger-098dc46c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 29 (Has_Allied_BLab) is clear.
2. No instances of Allied Construction Vehicle (AMCV) exist on the map, under this event's ownership scope.
3. Building does not exist: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

Flag writers in this mission: set local flag 29 (Has_Allied_BLab) at [Player_Built_AlliedBLab (078C04BC)](#trigger-078c04bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [New_Countdown (0908B71C)](#trigger-0908b71c).
2. Disable [Allied_MCV_Gone[Easy] (0908B62C)](#trigger-0908b62c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10692, Events line 10782, Actions line 10872.

<a id="trigger-078bff3c"></a>

### 43. Allied_MCV_Gone(Med) - 078BFF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Allied_MCV_Gone[Easy] (0908B62C)](#trigger-0908b62c).

Incoming activation links: enable from [Chrono_MCV (0964B13C)](#trigger-0964b13c); enable from [New_MCV (098DC46C)](#trigger-098dc46c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 30 (Has_Allied_WarF) is clear.
2. No instances of Allied Construction Vehicle (AMCV) exist on the map, under this event's ownership scope.
3. Building does not exist: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

Flag writers in this mission: set local flag 30 (Has_Allied_WarF) at [Player_Built_AlliedWarF (078C00BC)](#trigger-078c00bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [New_Countdown (0908B71C)](#trigger-0908b71c).
2. Disable [Allied_MCV_Gone(Med) (078BFF3C)](#trigger-078bff3c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10693, Events line 10783, Actions line 10873.

<a id="trigger-09000cdc"></a>

### 44. Dominator_Gone - 09000CDC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Build_Yuri_SW (0460BDBC)](#trigger-0460bdbc).

Attached scope: tag definitions 0900240C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Psychic Dominator (YAPPET) exist on the map, under this event's ownership scope.
2. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Text_KillAll (0900786C)](#trigger-0900786c).
2. Display message “Objective: Destroy all Yuri forces” (MISSION:StopYuri).
3. Disable [Text_KillDominator (08F9A04C)](#trigger-08f9a04c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10694, Events line 10784, Actions line 10874.

<a id="trigger-0901213c"></a>

### 45. Detect_PD - 0901213C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Build_Yuri_SW (0460BDBC)](#trigger-0460bdbc).

Attached scope: tag definitions 0901657C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_PsychicDominatorDetected.
2. Enable and reset applicable timers for [Detect_GM (0901648C)](#trigger-0901648c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10695, Events line 10785, Actions line 10875.

<a id="trigger-0780a03c"></a>

### 46. Yuri_All_Attack - 0780A03C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Build_Yuri_SW (0460BDBC)](#trigger-0460bdbc).

Attached scope: tag definitions 0780E20C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  #: 60.
2. No instances of Psychic Dominator (YAPPET) exist on the map, under this event's ownership scope.
3. No instances of Genetic Mutator (YAGNTC) exist on the map, under this event's ownership scope.
4. Building does not exist: type index 300 (global list position: Bus Stop (CASTRT05)). A map-local type-list change can affect index interpretation.
5. Building does not exist: type index 303 (global list position: Yuri Barracks (YABRCK)). A map-local type-list change can affect index interpretation.
6. Building does not exist: type index 302 (global list position: Bio Reactor (YAPOWR)). A map-local type-list change can affect index interpretation.
7. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. All to Hunt: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
3. Enable and reset applicable timers for [Yuri_Hunt_Again (0BA8052C)](#trigger-0ba8052c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10696, Events line 10786, Actions line 10876.

<a id="trigger-08f9a04c"></a>

### 47. Text_KillDominator - 08F9A04C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono_Support (098DB96C)](#trigger-098db96c).

Attached scope: tag definitions 08F9D0FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Destroy the Psychic Dominator on Antarctica” (MISSION:KillPD).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10697, Events line 10787, Actions line 10877.

<a id="trigger-0908b71c"></a>

### 48. New_Countdown - 0908B71C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [New_MCV (098DC46C)](#trigger-098dc46c).

Incoming activation links: enable from [Allied_MCV_Gone[Easy] (0908B62C)](#trigger-0908b62c); enable from [Allied_MCV_Gone(Med) (078BFF3C)](#trigger-078bff3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 29 (Has_Allied_BLab) is clear.
3. local flag 30 (Has_Allied_WarF) is clear.

Flag writers in this mission: set local flag 29 (Has_Allied_BLab) at [Player_Built_AlliedBLab (078C04BC)](#trigger-078c04bc); set local flag 30 (Has_Allied_WarF) at [Player_Built_AlliedWarF (078C00BC)](#trigger-078c00bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_A12_EvaCountdown.
2. Enable and reset applicable timers for [New_MCV (098DC46C)](#trigger-098dc46c).
3. Disable [New_Countdown (0908B71C)](#trigger-0908b71c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10698, Events line 10788, Actions line 10878.

<a id="trigger-0900786c"></a>

### 49. Text_KillAll - 0900786C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Dominator_Gone (09000CDC)](#trigger-09000cdc).

Attached scope: tag definitions 09002B4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 150 configured time units have elapsed since the trigger timer was initialized/reset.
2. No instances of Psychic Dominator (YAPPET) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Display message “Objective: Destroy all Yuri forces” (MISSION:StopYuri).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10699, Events line 10789, Actions line 10879.

<a id="trigger-0901648c"></a>

### 50. Detect_GM - 0901648C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_PD (0901213C)](#trigger-0901213c).

Attached scope: tag definitions 090162DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_GeneticMutatorDetected.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10700, Events line 10790, Actions line 10880.

<a id="trigger-0ba8052c"></a>

### 51. Yuri_Hunt_Again - 0BA8052C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri_All_Attack (0780A03C)](#trigger-0780a03c).

Attached scope: tag definitions 0BA870AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10701, Events line 10791, Actions line 10881.

<a id="trigger-098dc46c"></a>

### 52. New_MCV - 098DC46C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [New_Countdown (0908B71C)](#trigger-0908b71c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [TEAM_Chrono_MCV (0964C97C)](all07smd-teams.md#team-0964c97c) at waypoint 26 (cell 105, 194).
2. Enable and reset applicable timers for [Allied_MCV_Gone[Easy] (0908B62C)](#trigger-0908b62c).
3. Enable and reset applicable timers for [Allied_MCV_Gone(Med) (078BFF3C)](#trigger-078bff3c).
4. Enable and reset applicable timers for [New_MCV_Support (078BF6AC)](#trigger-078bf6ac).
5. Disable [New_MCV (098DC46C)](#trigger-098dc46c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10702, Events line 10792, Actions line 10882.

<a id="trigger-078bf6ac"></a>

### 53. New_MCV_Support - 078BF6AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: [Allied_MCV_Gone(Med) (078BFF3C)](#trigger-078bff3c).

Incoming activation links: enable from [New_MCV (098DC46C)](#trigger-098dc46c).

Attached scope: tag definitions 098DC26C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [TEAM_Chrono_Grizzly1 (04E3AA8C)](all07smd-teams.md#team-04e3aa8c) at waypoint 27 (cell 105, 190).
2. Supply chrono reinforcement team [TEAM_Chrono_Grizzly2 (04E3A75C)](all07smd-teams.md#team-04e3a75c) at waypoint 28 (cell 102, 192).
3. Supply chrono reinforcement team [TEAM_Chrono_Grizzly3 (04E40B3C)](all07smd-teams.md#team-04e40b3c) at waypoint 34 (cell 108, 192).
4. Supply chrono reinforcement team [TEAM_Chrono_IFV1 (04E403BC)](all07smd-teams.md#team-04e403bc) at waypoint 30 (cell 102, 196).
5. Supply chrono reinforcement team [TEAM_Chrono_IFV2 (04E4077C)](all07smd-teams.md#team-04e4077c) at waypoint 32 (cell 108, 196).
6. Supply chrono reinforcement team [TEAM_Chrono_Mirage1 (04E39A4C)](all07smd-teams.md#team-04e39a4c) at waypoint 29 (cell 102, 194).
7. Supply chrono reinforcement team [TEAM_Chrono_Mirage2 (04E4064C)](all07smd-teams.md#team-04e4064c) at waypoint 33 (cell 108, 194).
8. Supply chrono reinforcement team [TEAM_Chrono_Prism1 (04E4028C)](all07smd-teams.md#team-04e4028c) at waypoint 31 (cell 105, 198).
9. Disable [New_MCV_Support (078BF6AC)](#trigger-078bf6ac).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10703, Events line 10793, Actions line 10883.

<a id="trigger-0b8152bc"></a>

### 54. Naval_Yard_Built - 0B8152BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B8111CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 61 (global list position: Soviet Shipyard (NAYARD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 17 (Has_Naval_Yard).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10704, Events line 10794, Actions line 10884.

<a id="trigger-0960ee5c"></a>

### 55. Establish_Base_D - 0960EE5C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0960E70C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Yuri_BD_1 (0CA2EB7C)](all07smd-teams.md#team-0ca2eb7c).
2. Create/recruit team [Yuri_BD_2 (0CA2DA4C)](all07smd-teams.md#team-0ca2da4c).
3. Create/recruit team [Yuri_BD_3 (0CA2D80C)](all07smd-teams.md#team-0ca2d80c).
4. Create/recruit team [BioReactor_Men1 (0965042C)](all07smd-teams.md#team-0965042c).
5. Create/recruit team [BioReactor_Men2 (09654D7C)](all07smd-teams.md#team-09654d7c).
6. Create/recruit team [BioReactor_Men3 (09654C4C)](all07smd-teams.md#team-09654c4c).
7. Create/recruit team [BioReactor_Men4 (09654B1C)](all07smd-teams.md#team-09654b1c).
8. Supply reinforcement team [BioReactor_Men5 (08FFE99C)](all07smd-teams.md#team-08ffe99c).
9. Supply reinforcement team [BioReactor_Men6 (08FFEC1C)](all07smd-teams.md#team-08ffec1c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10705, Events line 10795, Actions line 10885.

<a id="trigger-0be87edc"></a>

### 56. Conyard_Fixed - 0BE87EDC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Soviet Construction Yard (NACNST), owner Special, cell (82, 123), tag 0BE87C8C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [Change_RocketHouse (08E89B1C)](#trigger-08e89b1c).
3. Disable [Conyard_Fixed (0BE87EDC)](#trigger-0be87edc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10706, Events line 10796, Actions line 10886.

<a id="trigger-08e89b1c"></a>

### 57. Change_RocketHouse - 08E89B1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Conyard_Fixed (0BE87EDC)](#trigger-0be87edc).

Attached scope: V3 Ammunition (CAMISC06), owner Russians, cell (90, 118), tag 08E8965C, persistence mode 0; V3 Ammunition (CAMISC06), owner Russians, cell (90, 117), tag 08E8965C, persistence mode 0; V3 Ammunition (CAMISC06), owner Russians, cell (90, 128), tag 08E8965C, persistence mode 0; V3 Ammunition (CAMISC06), owner Russians, cell (90, 129), tag 08E8965C, persistence mode 0; Sentry Gun (NALASR), owner Special, cell (87, 131), tag 08E8965C, persistence mode 0; Sentry Gun (NALASR), owner Special, cell (87, 114), tag 08E8965C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [Player_Lose_Tierra (0A57F46C)](#trigger-0a57f46c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10707, Events line 10797, Actions line 10887.

<a id="trigger-0be87b9c"></a>

### 58. Reactor_Fixed - 0BE87B9C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Reactor (NAPOWR), owner Special, cell (80, 128), tag 0BE8788C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Disable [Reactor_Fixed (0BE87B9C)](#trigger-0be87b9c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10708, Events line 10798, Actions line 10888.

<a id="trigger-0c028afc"></a>

### 59. Build_Allied_WarFactory - 0C028AFC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C029C8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.
2. Build Building Type: type index 7 (global list position: Allied War Factory (GAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Mis_xA7_EvaUnholyAlliance.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10709, Events line 10799, Actions line 10889.

<a id="trigger-0e6533ec"></a>

### 60. Control_Offline - 0E6533EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E654F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10710, Events line 10800, Actions line 10890.

<a id="trigger-0f22154c"></a>

### 61. Conyard_Deployed - 0F22154C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0F22F04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.
2. Building exists: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Mis_xA7_EvaBuildUpQuickly.
2. Enable and reset applicable timers for [Enable_Oil_Grabbers (078F61FC)](#trigger-078f61fc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10711, Events line 10801, Actions line 10891.

<a id="trigger-078f61fc"></a>

### 62. Enable_Oil_Grabbers - 078F61FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Conyard_Deployed (0F22154C)](#trigger-0f22154c).

Attached scope: tag definitions 078F7B6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Activate_Oil_Grabbers (061BD4EC)](#trigger-061bd4ec).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10712, Events line 10802, Actions line 10892.

<a id="trigger-061bd4ec"></a>

### 63. Activate_Oil_Grabbers - 061BD4EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_Oil_Grabbers (078F61FC)](#trigger-078f61fc).

Attached scope: tag definitions 061B9DDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yuri3_AQ_Engineer (092F5EFC)](all07smd-teams.md#team-092f5efc).
2. Supply reinforcement team [Yuri3_AT_Engineer (092F59DC)](all07smd-teams.md#team-092f59dc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10713, Events line 10803, Actions line 10893.

<a id="trigger-0ee0857c"></a>

### 64. Set_Charge - 0EE0857C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0EE0881C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Superweapon Set Recharge Time; main setting 7; location/duration field 13500.
2. Superweapon Set Recharge Time; main setting 9; location/duration field 9000.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10714, Events line 10804, Actions line 10894.

<a id="trigger-0988e66c"></a>

### 65. Start_AI_Triggers - 0988E66C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0989723C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Production Begins: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. AI triggers begin: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
3. Production Begins: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
4. AI triggers begin: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10715, Events line 10805, Actions line 10895.

<a id="trigger-04f32afc"></a>

### 66. Africa_Defenses - 04F32AFC

Owner reference: Yuri2Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04F3227C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Africa_BD1 (09321C8C)](all07smd-teams.md#team-09321c8c).
2. Create/recruit team [Africa_BD2 (093217DC)](all07smd-teams.md#team-093217dc).
3. Create/recruit team [Africa_BD3 (0932132C)](all07smd-teams.md#team-0932132c).
4. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).
5. Supply reinforcement team [Yuri2_Garrison1 (0900E65C)](all07smd-teams.md#team-0900e65c).
6. Supply reinforcement team [Yuri2_Garrison2 (0900B27C)](all07smd-teams.md#team-0900b27c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10716, Events line 10806, Actions line 10896.

<a id="trigger-08e97bec"></a>

### 67. Irritate_Player - 08E97BEC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08E9766C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 27 (global list position: Chrono Sphere (GACSPH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Irritate_Player2 (08E9757C)](#trigger-08e9757c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10717, Events line 10807, Actions line 10897.

<a id="trigger-08e9757c"></a>

### 68. Irritate_Player2 - 08E9757C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Irritate_Player (08E97BEC)](#trigger-08e97bec).

Attached scope: tag definitions 08E9749C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_YuriTacticsTaunt.
2. Create/recruit team [Yuri_Floater3 (08E9634C)](all07smd-teams.md#team-08e9634c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10718, Events line 10808, Actions line 10898.

<a id="trigger-04e8103c"></a>

### 69. Arabs_Hate_Player - 04E8103C

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04E8C04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10719, Events line 10809, Actions line 10899.

<a id="trigger-090ad17c"></a>

### 70. PrismCheese1 - 090AD17C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 090A9BDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Yuri_PrismCheese_Team (090AF55C)](all07smd-teams.md#team-090af55c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10720, Events line 10810, Actions line 10900.

<a id="trigger-0930a91c"></a>

### 71. Yuri_Grabs_OilAR - 0930A91C

Owner reference: Yuri3Country. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 15 (country/type YURI3COUNTRY; placed owner Yuri3).

**Then perform these actions in order:**

1. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Production Begins: owner selector 15 (country/type YURI3COUNTRY; placed owner Yuri3).
3. AI triggers begin: owner selector 15 (country/type YURI3COUNTRY; placed owner Yuri3).
4. Enable and reset applicable timers for [Oil_Derricks_Gone (08CBA40C)](#trigger-08cba40c).
5. Disable [Yuri_Grabs_OilAR (0930A91C)](#trigger-0930a91c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10721, Events line 10811, Actions line 10901.

<a id="trigger-08cba40c"></a>

### 72. Oil_Derricks_Gone - 08CBA40C

Owner reference: Yuri3Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [ConYards_Gone_Yuri3 (08CBA88C)](#trigger-08cba88c).

Incoming activation links: enable from [Yuri_Grabs_OilAR (0930A91C)](#trigger-0930a91c); enable from [Yuri_Grabs_OilAS (093138DC)](#trigger-093138dc).

Attached scope: Yuri Construction Yard (YACNST), owner Yuri3, cell (138, 252), tag 08CBA4FC, persistence mode 0; Bio Reactor (YAPOWR), owner Yuri3, cell (137, 248), tag 08CBA4FC, persistence mode 0; Bio Reactor (YAPOWR), owner Yuri3, cell (140, 248), tag 08CBA4FC, persistence mode 0; Bio Reactor (YAPOWR), owner Yuri3, cell (143, 248), tag 08CBA4FC, persistence mode 0.

**Wait for the recorded events:**

1. Building does not exist: type index 71 (global list position: Tech Oil Derrick (CAOILD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 2 (country/type FRENCH; placed owner French).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10722, Events line 10812, Actions line 10902.

<a id="trigger-08cba88c"></a>

### 73. ConYards_Gone_Yuri3 - 08CBA88C

Owner reference: Yuri3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 24 (Main_ConYards_Gone) is set.

Flag writers in this mission: set local flag 24 (Main_ConYards_Gone) at [ConYards_Gone (08CBEF3C)](#trigger-08cbef3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 2 (country/type FRENCH; placed owner French).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10723, Events line 10813, Actions line 10903.

<a id="trigger-093138dc"></a>

### 74. Yuri_Grabs_OilAS - 093138DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 15 (country/type YURI3COUNTRY; placed owner Yuri3).

**Then perform these actions in order:**

1. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Production Begins: owner selector 15 (country/type YURI3COUNTRY; placed owner Yuri3).
3. AI triggers begin: owner selector 15 (country/type YURI3COUNTRY; placed owner Yuri3).
4. Enable and reset applicable timers for [Oil_Derricks_Gone (08CBA40C)](#trigger-08cba40c).
5. Disable [Yuri_Grabs_OilAS (093138DC)](#trigger-093138dc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10724, Events line 10814, Actions line 10904.

<a id="trigger-09197edc"></a>

### 75. Yuri3_Lose_ConYard - 09197EDC

Owner reference: Yuri3Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09197BCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 71 (global list position: Tech Oil Derrick (CAOILD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

No action entries.

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10725, Events line 10815, Actions line 10905.

<a id="trigger-08cb932c"></a>

### 76. Yuri_ConYard_Gone - 08CB932C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CBACAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 300 (global list position: Bus Stop (CASTRT05)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 25 (Yuri_ConYard_Gone).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10726, Events line 10816, Actions line 10906.

<a id="trigger-08cbabbc"></a>

### 77. Yuri2_ConYard_Gone - 08CBABBC

Owner reference: Yuri2Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CBA97C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 300 (global list position: Bus Stop (CASTRT05)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 26 (Yuri2_ConYard_Gone).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10727, Events line 10817, Actions line 10907.

<a id="trigger-08cbef3c"></a>

### 78. ConYards_Gone - 08CBEF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CBEC6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 25 (Yuri_ConYard_Gone) is set.
2. local flag 26 (Yuri2_ConYard_Gone) is set.

Flag writers in this mission: set local flag 25 (Yuri_ConYard_Gone) at [Yuri_ConYard_Gone (08CB932C)](#trigger-08cb932c); set local flag 26 (Yuri2_ConYard_Gone) at [Yuri2_ConYard_Gone (08CBABBC)](#trigger-08cbabbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 24 (Main_ConYards_Gone).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10728, Events line 10818, Actions line 10908.

<a id="trigger-07ca72bc"></a>

### 79. Win_Check - 07CA72BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07CA895C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  All: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
2. Destroyed,  Units,  All: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Cheer (0C8D4F3C)](#trigger-0c8d4f3c).
2. Enable and reset applicable timers for [PlayerWin (06B9B43C)](#trigger-06b9b43c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10729, Events line 10819, Actions line 10909.

<a id="trigger-0901606c"></a>

### 80. Yuri2_All_Attack - 0901606C

Owner reference: Yuri2Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09015F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  #: 11.
2. Building does not exist: type index 303 (global list position: Yuri Barracks (YABRCK)). A map-local type-list change can affect index interpretation.
3. Building does not exist: type index 302 (global list position: Bio Reactor (YAPOWR)). A map-local type-list change can affect index interpretation.
4. Building does not exist: type index 300 (global list position: Bus Stop (CASTRT05)). A map-local type-list change can affect index interpretation.
5. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
2. All to Hunt: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).
3. Enable and reset applicable timers for [Yuri2_Attack_Again (0BA8312C)](#trigger-0ba8312c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10730, Events line 10820, Actions line 10910.

<a id="trigger-0ba8312c"></a>

### 81. Yuri2_Attack_Again - 0BA8312C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri2_All_Attack (0901606C)](#trigger-0901606c).

Attached scope: tag definitions 0BA4304C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type YURI2COUNTRY; placed owner Yuri2).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10731, Events line 10821, Actions line 10911.

<a id="trigger-0462be5c"></a>

### 82. Player_Goes_Naval - 0462BE5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0462DA6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 23 (global list position: Allied Shipyard (GAYARD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Create/recruit team [Yuri_Boomer_Solo (07AB65CC)](all07smd-teams.md#team-07ab65cc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10732, Events line 10822, Actions line 10912.

<a id="trigger-078f6e5c"></a>

### 83. Derrick_AR_Found - 078F6E5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Yuri_Grabs_OilAR (0930A91C)](#trigger-0930a91c).

Attached scope: Tech Oil Derrick (CAOILD), owner Neutral, cell (141, 228), tag 093139CC, persistence mode 2.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Activate_Oil_Grab(Med) (078F71EC)](#trigger-078f71ec).
2. Disable [Derrick_AR_Found (078F6E5C)](#trigger-078f6e5c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10733, Events line 10823, Actions line 10913.

<a id="trigger-078f71ec"></a>

### 84. Activate_Oil_Grab(Med) - 078F71EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Derrick_AR_Found (078F6E5C)](#trigger-078f6e5c); enable from [Derrick_AS_Found (078F692C)](#trigger-078f692c).

Attached scope: tag definitions 078F781C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yuri3_AQ_Engineer (092F5EFC)](all07smd-teams.md#team-092f5efc).
2. Supply reinforcement team [Yuri3_AT_Engineer (092F59DC)](all07smd-teams.md#team-092f59dc).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10734, Events line 10824, Actions line 10914.

<a id="trigger-078f692c"></a>

### 85. Derrick_AS_Found - 078F692C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Yuri_Grabs_OilAS (093138DC)](#trigger-093138dc).

Attached scope: Tech Oil Derrick (CAOILD), owner Neutral, cell (141, 232), tag 09311E7C, persistence mode 2.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Activate_Oil_Grab(Med) (078F71EC)](#trigger-078f71ec).
2. Disable [Derrick_AS_Found (078F692C)](#trigger-078f692c).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10735, Events line 10825, Actions line 10915.

<a id="trigger-078c04bc"></a>

### 86. Player_Built_AlliedBLab - 078C04BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078C01AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. At least 1 instances of Allied Battle Lab (GATECH) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 29 (Has_Allied_BLab).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10736, Events line 10826, Actions line 10916.

<a id="trigger-078c00bc"></a>

### 87. Player_Built_AlliedWarF - 078C00BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078C1EBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. At least 1 instances of Allied Battle Lab (GATECH) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 30 (Has_Allied_WarF).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10737, Events line 10827, Actions line 10917.

<a id="trigger-04f0aacc"></a>

### 88. Create_Crates - 04F0AACC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04F0A30C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 46 (cell 42, 136).
2. Create crate type 0 at waypoint 47 (cell 138, 227).

Source locator: mapsmd03.mix/all07smd.map; Triggers line 10738, Events line 10828, Actions line 10918.

[All team rosters and ordered plans](all07smd-teams.md) | [All mission overrides](all07smd-overrides.md)
