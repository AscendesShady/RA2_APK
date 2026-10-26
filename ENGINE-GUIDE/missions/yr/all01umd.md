# Operation: Time Lapse

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all01umd.map. **Effective extracted member:** mapsmd03.mix/all01umd.map. **Trigger definitions:** 334.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all01umd-teams.md) | [All mission overrides](all01umd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Americans |
| Theater | NEWURBAN |
| Map size | 0,0,65,120 |
| Visible local rectangle | 12,5,47,100 |
| Placed vehicles | 18 |
| Placed infantry | 56 |
| Placed structures | 189 |
| Placed aircraft | 0 |
| Team templates | 102 |

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
| 7 | Confederation | 600 | Confederation |
| 8 | Russians | 0 | Russians |
| 9 | YuriCountry | 0 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 0 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |
| 14 | PowerHouse | 0 | PowerHouse Country |
| 15 | Soviet2House | 0 | Soviet2 Country |
| 16 | BridgeHouse | 0 | Bridge Country |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Hover1_Unloaded,0 |
| 1 | Hover_2_Unloaded,0 |
| 2 | Hover_3_Unloaded,0 |
| 3 | Time_Warp,0 |
| 4 | Tanya_Dead,0 |
| 5 | Gave_PP_Brief,0 |
| 6 | PP1_Entered,0 |
| 7 | PP2_Entered,0 |
| 8 | PP3_Entered,0 |
| 9 | PP4_Entered,0 |
| 10 | PP5_Entered,0 |
| 11 | PP6_Entered,0 |
| 12 | PP7_Entered,0 |
| 13 | PP8_Entered,0 |
| 14 | PP1_Group_Revealed,0 |
| 15 | PP2_Group_Revealed,0 |
| 16 | PP3_Group_Revealed,0 |
| 17 | PP4_Group_Revealed,0 |
| 18 | PP1_Gone,0 |
| 19 | PP2_Gone,0 |
| 20 | PP3_Gone,0 |
| 21 | PP4_Gone,0 |
| 22 | PP5_Gone,0 |
| 23 | PP6_Gone,0 |
| 24 | PP7_Gone,0 |
| 25 | PP8_Gone,1 |
| 26 | Lost_1_Power,0 |
| 27 | Lost_2_Power,0 |
| 28 | Lost_3_Power,0 |
| 29 | Lost_4_Power,0 |
| 30 | Lost_5_Power,0 |
| 31 | Lost_Tech01_USA,0 |
| 32 | Lost_Tech_01_Neu,0 |
| 33 | Lost_Tech02_USA,0 |
| 34 | Lost_Tech02_Neut,0 |
| 35 | Lost_Tech03_USA,0 |
| 36 | Lost_Tech04_USA,0 |
| 37 | Lost_Tech05_USA,0 |
| 38 | Lost_Tech06_USA,0 |
| 39 | Lost_Tech07_USA,0 |
| 40 | Lost_Tech08_USA,0 |
| 41 | Lost_Tech03_Neut,0 |
| 42 | Lost_Tech04_Neut,0 |
| 43 | Lost_Tech05_Neut,0 |
| 44 | Lost_Tech06_Neut,0 |
| 45 | Lost_Tech07_Neut,0 |
| 46 | Lost_Tech08_Neut,0 |
| 47 | Power_Online,0 |
| 48 | Nuke_Destroyed,0 |
| 49 | Player_Has_Plant,0 |
| 50 | Cannon1_Gone,0 |
| 51 | Cannon2_Gone,0 |
| 52 | Cannon3_Gone,0 |
| 53 | Cannon4_Gone,0 |
| 54 | Engineers_Landed,0 |
| 55 | LostPP1_Easy,0 |
| 56 | LostPP2_Easy,0 |
| 57 | LostPP3_Easy,0 |
| 58 | LostPP4_Easy,0 |
| 59 | LostPP5_Easy,0 |
| 60 | LostPP6_Easy,0 |
| 61 | LostPP7_Easy,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Time_Machine_Boom (08A3E03C)](#trigger-08a3e03c) | local flag 3 (Time_Warp) is clear.<br>Destroyed by anything. See attached-object/cell scope below. | Announce defeat. |
| [Time_Machine_Boom2 (08707A2C)](#trigger-08707a2c) | local flag 3 (Time_Warp) is set.<br>No instances of Tanya (TANY) exist on the map, under this event's ownership scope.<br>Destroyed by anything. See attached-object/cell scope below. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |
| [WeWin (089EC79C)](#trigger-089ec79c) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner. |
| [Player_Lost (06178D0C)](#trigger-06178d0c) | 0 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |

## Every trigger, in file order

<a id="trigger-08134e0c"></a>

### 1. Start_I_Drop - 08134E0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Final_Camera_Set (068F215C)](#trigger-068f215c).

Attached scope: tag definitions 0B850BDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Drop_I_Team (0813427C)](#trigger-0813427c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8571, Events line 8907, Actions line 9243.

<a id="trigger-0813427c"></a>

### 2. Drop_I_Team - 0813427C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_I_Drop (08134E0C)](#trigger-08134e0c); enable from [RA_Team_Death (0BB74AFC)](#trigger-0bb74afc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. 60 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_NW_Attack (089B3A4C)](all01umd-teams.md#team-089b3a4c) at waypoint 12 (cell 80, 128).
2. Enable and reset applicable timers for [Delay_ITeam_Check (08136ABC)](#trigger-08136abc).
3. Disable [Drop_I_Team (0813427C)](#trigger-0813427c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8572, Events line 8908, Actions line 9244.

<a id="trigger-08136abc"></a>

### 3. Delay_ITeam_Check - 08136ABC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drop_I_Team (0813427C)](#trigger-0813427c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. 3 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Paradrop_I_Death (08135C1C)](#trigger-08135c1c).
2. Disable [Delay_ITeam_Check (08136ABC)](#trigger-08136abc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8573, Events line 8909, Actions line 9245.

<a id="trigger-08135c1c"></a>

### 4. Paradrop_I_Death - 08135C1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Delay_ITeam_Check (08136ABC)](#trigger-08136abc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create_RM_RN_Team (06A0A20C)](#trigger-06a0a20c).
2. Disable [Paradrop_I_Death (08135C1C)](#trigger-08135c1c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8574, Events line 8910, Actions line 9246.

<a id="trigger-06a0a20c"></a>

### 5. Create_RM_RN_Team - 06A0A20C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Create_RA_Team (0BB731DC)](#trigger-0bb731dc).

Incoming activation links: enable from [Paradrop_I_Death (08135C1C)](#trigger-08135c1c).

Attached scope: tag definitions 08135D0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_RM_RN_Attack (0C36E6AC)](all01umd-teams.md#team-0c36e6ac).
2. Enable and reset applicable timers for [Delay_RMRN_Check (06A0A03C)](#trigger-06a0a03c).
3. Disable [Create_RM_RN_Team (06A0A20C)](#trigger-06a0a20c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8575, Events line 8911, Actions line 9247.

<a id="trigger-0bb731dc"></a>

### 6. Create_RA_Team - 0BB731DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Create_Hover_3 (0B16029C)](#trigger-0b16029c).

Incoming activation links: enable from [RMRN_Team_Death (06A0CC6C)](#trigger-06a0cc6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_RA_Tanks (0AA2AEFC)](all01umd-teams.md#team-0aa2aefc).
2. Enable and reset applicable timers for [Delay_RA_Check (0BB74DFC)](#trigger-0bb74dfc).
3. Disable [Create_RA_Team (0BB731DC)](#trigger-0bb731dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8576, Events line 8912, Actions line 9248.

<a id="trigger-06a0a03c"></a>

### 7. Delay_RMRN_Check - 06A0A03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Delay_RA_Check (0BB74DFC)](#trigger-0bb74dfc).

Incoming activation links: enable from [Create_RM_RN_Team (06A0A20C)](#trigger-06a0a20c).

Attached scope: tag definitions 0813683C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. 3 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [RMRN_Team_Death (06A0CC6C)](#trigger-06a0cc6c).
2. Disable [Delay_RMRN_Check (06A0A03C)](#trigger-06a0a03c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8577, Events line 8913, Actions line 9249.

<a id="trigger-0b16029c"></a>

### 8. Create_Hover_3 - 0B16029C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Create_Hover_2 (0895C19C)](#trigger-0895c19c).

Incoming activation links: enable from [Check_Hover3 (0B1613DC)](#trigger-0b1613dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Water3 (0A7F16AC)](all01umd-teams.md#team-0a7f16ac) at waypoint 37 (cell 42, 29).
2. Enable and reset applicable timers for [Hover3_Death (0B160E5C)](#trigger-0b160e5c).
3. Disable [Create_Hover_3 (0B16029C)](#trigger-0b16029c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8578, Events line 8914, Actions line 9250.

<a id="trigger-0bb74dfc"></a>

### 9. Delay_RA_Check - 0BB74DFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ping4_delay (08B5892C)](#trigger-08b5892c).

Incoming activation links: enable from [Create_RA_Team (0BB731DC)](#trigger-0bb731dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. 3 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [RA_Team_Death (0BB74AFC)](#trigger-0bb74afc).
2. Disable [Delay_RA_Check (0BB74DFC)](#trigger-0bb74dfc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8579, Events line 8915, Actions line 9251.

<a id="trigger-06a0cc6c"></a>

### 10. RMRN_Team_Death - 06A0CC6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RA_Team_Death (0BB74AFC)](#trigger-0bb74afc).

Incoming activation links: enable from [Delay_RMRN_Check (06A0A03C)](#trigger-06a0a03c).

Attached scope: tag definitions 0813589C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create_RA_Team (0BB731DC)](#trigger-0bb731dc).
2. Disable [RMRN_Team_Death (06A0CC6C)](#trigger-06a0cc6c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8580, Events line 8916, Actions line 9252.

<a id="trigger-0895c19c"></a>

### 11. Create_Hover_2 - 0895C19C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Create_Hover_One (0B7D4BCC)](#trigger-0b7d4bcc).

Incoming activation links: enable from [Check_Hover2 (089FC3DC)](#trigger-089fc3dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Water_Two (0A80332C)](all01umd-teams.md#team-0a80332c) at waypoint 24 (cell 56, 14).
2. Enable and reset applicable timers for [Hover2_Death (0895D88C)](#trigger-0895d88c).
3. Disable [Create_Hover_2 (0895C19C)](#trigger-0895c19c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8581, Events line 8917, Actions line 9253.

<a id="trigger-0b160e5c"></a>

### 12. Hover3_Death - 0B160E5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Hover2_Death (0895D88C)](#trigger-0895d88c).

Incoming activation links: enable from [Create_Hover_3 (0B16029C)](#trigger-0b16029c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed,  Units,  All: owner selector 3 (country/type GERMANS; placed owner Germans).

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Check_Hover1 (089FC90C)](#trigger-089fc90c).
2. Disable [Hover3_Death (0B160E5C)](#trigger-0b160e5c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8582, Events line 8918, Actions line 9254.

<a id="trigger-08b5892c"></a>

### 13. Ping4_delay - 08B5892C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_Hover3 (0B1613DC)](#trigger-0b1613dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Ping_PP_Four (08B4D3BC)](#trigger-08b4d3bc).
2. Disable [Ping4_delay (08B5892C)](#trigger-08b5892c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8583, Events line 8919, Actions line 9255.

<a id="trigger-0bb74afc"></a>

### 14. RA_Team_Death - 0BB74AFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Tanya_Death (089B82BC)](#trigger-089b82bc).

Incoming activation links: enable from [Delay_RA_Check (0BB74DFC)](#trigger-0bb74dfc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Drop_I_Team (0813427C)](#trigger-0813427c).
2. Disable [RA_Team_Death (0BB74AFC)](#trigger-0bb74afc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8584, Events line 8920, Actions line 9256.

<a id="trigger-0b7d4bcc"></a>

### 15. Create_Hover_One - 0B7D4BCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Drop_I_Team (0813427C)](#trigger-0813427c).

Incoming activation links: enable from [Check_Hover1 (089FC90C)](#trigger-089fc90c); enable from [Start_Hover_One (0B7D315C)](#trigger-0b7d315c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. 120 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Hover_Team_1 (0A2BD90C)](all01umd-teams.md#team-0a2bd90c) at waypoint 10 (cell 50, 21).
2. Enable and reset applicable timers for [Hover1_Death (0B7D615C)](#trigger-0b7d615c).
3. Disable [Create_Hover_One (0B7D4BCC)](#trigger-0b7d4bcc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8585, Events line 8921, Actions line 9257.

<a id="trigger-0895d88c"></a>

### 16. Hover2_Death - 0895D88C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Hover1_Death (0B7D615C)](#trigger-0b7d615c).

Incoming activation links: enable from [Create_Hover_2 (0895C19C)](#trigger-0895c19c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed,  Units,  All: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Check_Hover3 (0B1613DC)](#trigger-0b1613dc).
2. Disable [Hover2_Death (0895D88C)](#trigger-0895d88c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8586, Events line 8922, Actions line 9258.

<a id="trigger-089fc90c"></a>

### 17. Check_Hover1 - 089FC90C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ping2_to_Ping3 (089D698C)](#trigger-089d698c).

Incoming activation links: enable from [Hover3_Death (0B160E5C)](#trigger-0b160e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed,  All: owner selector 11 (country/type NOD; placed owner Nod).

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create_Hover_One (0B7D4BCC)](#trigger-0b7d4bcc).
2. Disable [Check_Hover1 (089FC90C)](#trigger-089fc90c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8587, Events line 8923, Actions line 9259.

<a id="trigger-0b1613dc"></a>

### 18. Check_Hover3 - 0B1613DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_Hover2 (089FC3DC)](#trigger-089fc3dc).

Incoming activation links: enable from [Hover2_Death (0895D88C)](#trigger-0895d88c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed,  Units,  All: owner selector 3 (country/type GERMANS; placed owner Germans).

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create_Hover_3 (0B16029C)](#trigger-0b16029c).
2. Disable [Check_Hover3 (0B1613DC)](#trigger-0b1613dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8588, Events line 8924, Actions line 9260.

<a id="trigger-08b4d3bc"></a>

### 19. Ping_PP_Four - 08B4D3BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Ping4_delay (08B5892C)](#trigger-08b5892c); enable from [Check_PP3_False (0BFCC50C)](#trigger-0bfcc50c).

Attached scope: tag definitions 08B4D2DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 47 (Power_Online) is clear.

Flag writers in this mission: set local flag 47 (Power_Online) at [Power_Online (0691357C)](#trigger-0691357c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play sound BeaconPlaced.
2. Create radar-event marker type 11 at waypoint 43 (cell 154, 107).
3. Disable [Ping_PP_Four (08B4D3BC)](#trigger-08b4d3bc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8589, Events line 8925, Actions line 9261.

<a id="trigger-089b82bc"></a>

### 20. Tanya_Death - 089B82BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [AP_Paradrop_Death (0BDF7BBC)](#trigger-0bdf7bbc).

Incoming activation links: enable from [Enter_Tanya (0AC85F3C)](#trigger-0ac85f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Tanya (TANY) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 4 (Tanya_Dead).
2. Play full-screen movie 5.
3. Enable and reset applicable timers for [Death_Reinforce (0BA104BC)](#trigger-0ba104bc).
4. Disable [Mission2_Text (046358AC)](#trigger-046358ac).
5. Disable [Tanya_Death (089B82BC)](#trigger-089b82bc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8590, Events line 8926, Actions line 9262.

<a id="trigger-0b7d615c"></a>

### 21. Hover1_Death - 0B7D615C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Paradrop_I_Death (08135C1C)](#trigger-08135c1c).

Incoming activation links: enable from [Create_Hover_One (0B7D4BCC)](#trigger-0b7d4bcc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 0 (Hover1_Unloaded) is clear.
2. Destroyed,  All: owner selector 11 (country/type NOD; placed owner Nod).

Flag writers in this mission: clear local flag 0 (Hover1_Unloaded) at [Hover1_Go_Home (0B7D6AAC)](#trigger-0b7d6aac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Check_Hover2 (089FC3DC)](#trigger-089fc3dc).
2. Disable [Hover1_Death (0B7D615C)](#trigger-0b7d615c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8591, Events line 8927, Actions line 9263.

<a id="trigger-089d698c"></a>

### 22. Ping2_to_Ping3 - 089D698C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [GGI_Flash_to_Final (0A81149C)](#trigger-0a81149c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Ping_PP_Three (089D668C)](#trigger-089d668c).
2. Disable [Ping2_to_Ping3 (089D698C)](#trigger-089d698c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8592, Events line 8928, Actions line 9264.

<a id="trigger-089fc3dc"></a>

### 23. Check_Hover2 - 089FC3DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_Hover1 (089FC90C)](#trigger-089fc90c).

Incoming activation links: enable from [Hover1_Death (0B7D615C)](#trigger-0b7d615c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed,  Units,  All: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create_Hover_2 (0895C19C)](#trigger-0895c19c).
2. Disable [Check_Hover2 (089FC3DC)](#trigger-089fc3dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8593, Events line 8929, Actions line 9265.

<a id="trigger-0bdf7bbc"></a>

### 24. AP_Paradrop_Death - 0BDF7BBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Hover3_Death (0B160E5C)](#trigger-0b160e5c).

Incoming activation links: enable from [AP_Paradrop (069B22FC)](#trigger-069b22fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed,  All: owner selector 5 (country/type AFRICANS; placed owner Africans).

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [AP_Paradrop (069B22FC)](#trigger-069b22fc).
2. Disable [AP_Paradrop_Death (0BDF7BBC)](#trigger-0bdf7bbc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8594, Events line 8930, Actions line 9266.

<a id="trigger-0ba104bc"></a>

### 25. Death_Reinforce - 0BA104BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ping_Carriers (0898812C)](#trigger-0898812c).

Incoming activation links: enable from [Tanya_Death (089B82BC)](#trigger-089b82bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 4 (Tanya_Dead) is set.
2. local flag 3 (Time_Warp) is set.

Flag writers in this mission: set local flag 4 (Tanya_Dead) at [Tanya_Death (089B82BC)](#trigger-089b82bc); set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Carriers (08071C8C)](all01umd-teams.md#team-08071c8c).
2. Enable and reset applicable timers for [Send_Carriers (089B1CCC)](#trigger-089b1ccc).
3. Disable [Death_Reinforce (0BA104BC)](#trigger-0ba104bc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8595, Events line 8931, Actions line 9267.

<a id="trigger-046358ac"></a>

### 26. Mission2_Text - 046358AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enter_Tanya (0AC85F3C)](#trigger-0ac85f3c).

Attached scope: tag definitions 046353EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Swim Tanya to Alcatraz Island and destroy the Psychic Dominator” (MISSION:Alcatraz).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8596, Events line 8932, Actions line 9268.

<a id="trigger-0a81149c"></a>

### 27. GGI_Flash_to_Final - 0A81149C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [GGI_to_GGI_Flash (0A81491C)](#trigger-0a81491c).

Incoming activation links: enable from [Flash_GGI (0A815AFC)](#trigger-0a815afc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Final_Camera_Set (068F215C)](#trigger-068f215c).
2. Disable [GGI_Flash_to_Final (0A81149C)](#trigger-0a81149c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8597, Events line 8933, Actions line 9269.

<a id="trigger-089d668c"></a>

### 28. Ping_PP_Three - 089D668C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Ping2_to_Ping3 (089D698C)](#trigger-089d698c); enable from [Check_PP4_False (0BFE471C)](#trigger-0bfe471c).

Attached scope: tag definitions 089D65AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 47 (Power_Online) is clear.

Flag writers in this mission: set local flag 47 (Power_Online) at [Power_Online (0691357C)](#trigger-0691357c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play sound BeaconPlaced.
2. Create radar-event marker type 11 at waypoint 18 (cell 126, 83).
3. Disable [Ping_PP_Three (089D668C)](#trigger-089d668c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8598, Events line 8934, Actions line 9270.

<a id="trigger-069b22fc"></a>

### 29. AP_Paradrop - 069B22FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AP_Paradrop_Death (0BDF7BBC)](#trigger-0bdf7bbc); enable from [Return_Control (089627FC)](#trigger-089627fc).

Attached scope: tag definitions 069B3D7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 135 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 3 (Time_Warp) is clear.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_AP_Paradrop (0D2AF91C)](all01umd-teams.md#team-0d2af91c) at waypoint 41 (cell 117, 112).
2. Enable and reset applicable timers for [AP_Paradrop_Death (0BDF7BBC)](#trigger-0bdf7bbc).
3. Disable [AP_Paradrop (069B22FC)](#trigger-069b22fc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8599, Events line 8935, Actions line 9271.

<a id="trigger-0898812c"></a>

### 30. Ping_Carriers - 0898812C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Send_Carriers (089B1CCC)](#trigger-089b1ccc).

Incoming activation links: enable from [Send_Carriers (089B1CCC)](#trigger-089b1ccc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 0 at waypoint 417 (cell 56, 89).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Enable and reset applicable timers for [Carriers_Killed (0792B79C)](#trigger-0792b79c).
4. Disable [Ping_Carriers (0898812C)](#trigger-0898812c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8600, Events line 8936, Actions line 9272.

<a id="trigger-089b1ccc"></a>

### 31. Send_Carriers - 089B1CCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Death_Reinforce (0BA104BC)](#trigger-0ba104bc); enable from [Carriers_Killed (0792B79C)](#trigger-0792b79c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Carriers (08071C8C)](all01umd-teams.md#team-08071c8c).
2. Enable and reset applicable timers for [Ping_Carriers (0898812C)](#trigger-0898812c).
3. Disable [Send_Carriers (089B1CCC)](#trigger-089b1ccc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8601, Events line 8937, Actions line 9273.

<a id="trigger-0a81491c"></a>

### 32. GGI_to_GGI_Flash - 0A81491C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ping3_to_GGI (08A868EC)](#trigger-08a868ec).

Incoming activation links: enable from [Camera_GGI (0A81253C)](#trigger-0a81253c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Flash_GGI (0A815AFC)](#trigger-0a815afc).
2. Disable [GGI_to_GGI_Flash (0A81491C)](#trigger-0a81491c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8602, Events line 8938, Actions line 9274.

<a id="trigger-068f215c"></a>

### 33. Final_Camera_Set - 068F215C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [GGI_Flash_to_Final (0A81149C)](#trigger-0a81149c).

Attached scope: tag definitions 068E136C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 14 (cell 100, 110) with speed setting 3.
2. Enable and reset applicable timers for [Start_I_Drop (08134E0C)](#trigger-08134e0c).
3. Enable and reset applicable timers for [Return_Control (089627FC)](#trigger-089627fc).
4. Enable and reset applicable timers for [Power_Online (0691357C)](#trigger-0691357c).
5. Disable [Final_Camera_Set (068F215C)](#trigger-068f215c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8603, Events line 8939, Actions line 9275.

<a id="trigger-0792b79c"></a>

### 34. Carriers_Killed - 0792B79C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Death_Reinforce (0BA104BC)](#trigger-0ba104bc).

Incoming activation links: enable from [Ping_Carriers (0898812C)](#trigger-0898812c).

Attached scope: tag definitions 04382B0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Aircraft Carrier (CARRIER) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Send_Carriers (089B1CCC)](#trigger-089b1ccc).
2. Disable [Carriers_Killed (0792B79C)](#trigger-0792b79c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8604, Events line 8940, Actions line 9276.

<a id="trigger-08a868ec"></a>

### 35. Ping3_to_GGI - 08A868EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ping1_to_Ping2 (08A8953C)](#trigger-08a8953c).

Incoming activation links: enable from [Ping_PP_Two (08A8E55C)](#trigger-08a8e55c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 14 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Camera_GGI (0A81253C)](#trigger-0a81253c).
2. Enable and reset applicable timers for [GGI_GuineaPig_Start (0AB41D9C)](#trigger-0ab41d9c).
3. Disable [Ping3_to_GGI (08A868EC)](#trigger-08a868ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8605, Events line 8941, Actions line 9277.

<a id="trigger-0a815afc"></a>

### 36. Flash_GGI - 0A815AFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [GGI_to_GGI_Flash (0A81491C)](#trigger-0a81491c).

Attached scope: tag definitions 0A815A1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_GGI_Flash (08B066CC)](all01umd-teams.md#team-08b066cc).
2. Enable and reset applicable timers for [GGI_Flash_to_Final (0A81149C)](#trigger-0a81149c).
3. Enable and reset applicable timers for [Attack_Tanya (089F2AAC)](#trigger-089f2aac).
4. Disable [Flash_GGI (0A815AFC)](#trigger-0a815afc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8606, Events line 8942, Actions line 9278.

<a id="trigger-089627fc"></a>

### 37. Return_Control - 089627FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Final_Camera_Set (068F215C)](#trigger-068f215c).

Attached scope: tag definitions 08963C5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Play voice notification EVA_BattlefieldControlOnline.
3. Enable and reset applicable timers for [AP_Paradrop (069B22FC)](#trigger-069b22fc).
4. Enable and reset applicable timers for [Mission1_Text (06CBE3FC)](#trigger-06cbe3fc).
5. Enable and reset applicable timers for [Time_Machine_Hit (097D15DC)](#trigger-097d15dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8607, Events line 8943, Actions line 9279.

<a id="trigger-0691357c"></a>

### 38. Power_Online - 0691357C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Final_Camera_Set (068F215C)](#trigger-068f215c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 49 (Player_Has_Plant) is set.
2. Power Full: owner selector 0 (country/type AMERICANS; placed owner Americans).

Flag writers in this mission: set local flag 49 (Player_Has_Plant) at [Player_Has_Plant1 (096E1F3C)](#trigger-096e1f3c); set local flag 49 (Player_Has_Plant) at [Player_Has_Plant2 (096E125C)](#trigger-096e125c); set local flag 49 (Player_Has_Plant) at [Player_Has_Plant3 (096E0D8C)](#trigger-096e0d8c); set local flag 49 (Player_Has_Plant) at [Player_Has_Plant4 (096E0AAC)](#trigger-096e0aac); set local flag 49 (Player_Has_Plant) at [Player_Has_Plant5 (096E07CC)](#trigger-096e07cc); set local flag 49 (Player_Has_Plant) at [Player_Has_Plant6 (096E04EC)](#trigger-096e04ec); set local flag 49 (Player_Has_Plant) at [Player_Has_Plant7 (096E020C)](#trigger-096e020c); set local flag 49 (Player_Has_Plant) at [Player_Has_Plant8 (096E2DDC)](#trigger-096e2ddc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Nuke_Repair (0DC53EFC)](all01umd-teams.md#team-0dc53efc).
2. Enable and reset applicable timers for [Change_Radar_House (0BE0B26C)](#trigger-0be0b26c).
3. Enable and reset applicable timers for [Start_Timer (0A8E573C)](#trigger-0a8e573c).
4. Disable [Find_Hospital (0462B74C)](#trigger-0462b74c).
5. Play sound SpyUplinkOn.
6. Reveal the whole map.
7. Set local flag 47 (Power_Online).
8. Enable and reset applicable timers for [Obj01_Complete_Text (09515B9C)](#trigger-09515b9c).
9. Disable [Power_Online (0691357C)](#trigger-0691357c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8608, Events line 8944, Actions line 9280.

<a id="trigger-08a8953c"></a>

### 39. Ping1_to_Ping2 - 08A8953C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TM_to_Radar_Ping (08A8FBCC)](#trigger-08a8fbcc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Ping_PP_Two (08A8E55C)](#trigger-08a8e55c).
2. Disable [Ping1_to_Ping2 (08A8953C)](#trigger-08a8953c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8609, Events line 8945, Actions line 9281.

<a id="trigger-0a81253c"></a>

### 40. Camera_GGI - 0A81253C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Ping3_to_GGI (08A868EC)](#trigger-08a868ec).

Attached scope: tag definitions 0A81245C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 13 (cell 88, 100) with speed setting 3.
2. Play voice notification Unit_Eva_GuardianGI.
3. Enable and reset applicable timers for [GGI_to_GGI_Flash (0A81491C)](#trigger-0a81491c).
4. Disable [Camera_GGI (0A81253C)](#trigger-0a81253c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8610, Events line 8946, Actions line 9282.

<a id="trigger-0ab41d9c"></a>

### 41. GGI_GuineaPig_Start - 0AB41D9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Ping3_to_GGI (08A868EC)](#trigger-08a868ec).

Attached scope: tag definitions 0AB41CBC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_GGI_GuineaPig (0BF1048C)](all01umd-teams.md#team-0bf1048c).
2. Disable [GGI_GuineaPig_Start (0AB41D9C)](#trigger-0ab41d9c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8611, Events line 8947, Actions line 9283.

<a id="trigger-089f2aac"></a>

### 42. Attack_Tanya - 089F2AAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Flash_GGI (0A815AFC)](#trigger-0a815afc).

Attached scope: tag definitions 089F79FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Attack_Tanya (09F3BC1C)](all01umd-teams.md#team-09f3bc1c) at waypoint 41 (cell 117, 112).
2. Disable [Attack_Tanya (089F2AAC)](#trigger-089f2aac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8612, Events line 8948, Actions line 9284.

<a id="trigger-06cbe3fc"></a>

### 43. Mission1_Text - 06CBE3FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Return_Control (089627FC)](#trigger-089627fc).

Attached scope: tag definitions 0E0AA3CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 150 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 3 (Time_Warp) is clear.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Display message “Objective: Capture Power Plants to bring the Time Machine online” (MISSION:GetPower).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8613, Events line 8949, Actions line 9285.

<a id="trigger-097d15dc"></a>

### 44. Time_Machine_Hit - 097D15DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Time_Machine_Boom (08A3E03C)](#trigger-08a3e03c).

Incoming activation links: enable from [Return_Control (089627FC)](#trigger-089627fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Tanya (TANY) exist on the map, under this event's ownership scope.
2. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Time_Machine_Attacked (097D02CC)](#trigger-097d02cc).
2. Disable [Time_Machine_Hit (097D15DC)](#trigger-097d15dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8614, Events line 8950, Actions line 9286.

<a id="trigger-0be0b26c"></a>

### 45. Change_Radar_House - 0BE0B26C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Power_Online (0691357C)](#trigger-0691357c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Disable [Change_Radar_House (0BE0B26C)](#trigger-0be0b26c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8615, Events line 8951, Actions line 9287.

<a id="trigger-0a8e573c"></a>

### 46. Start_Timer - 0A8E573C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Power_Online (0691357C)](#trigger-0691357c).

Incoming activation links: enable from [Power_Online (0691357C)](#trigger-0691357c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie with game pause 3.
2. Enable and reset applicable timers for [Timer_Movie (0A8EA21C)](#trigger-0a8ea21c).
3. Disable [Start_Timer (0A8E573C)](#trigger-0a8e573c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8616, Events line 8952, Actions line 9288.

<a id="trigger-0462b74c"></a>

### 47. Find_Hospital - 0462B74C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Civilian Hospital (CATHOSP), owner PowerHouse, cell (104, 79), tag 0462CD1C, persistence mode 0; 28 tagged map cells: (102, 78), (103, 78), (104, 78), (105, 78), (106, 78), (107, 78), (108, 78), (109, 78), (110, 78), (111, 78), (102, 79), (111, 79), (102, 80), (111, 80), (102, 81), (111, 81), (102, 82), (111, 82), (102, 83), (103, 83), (104, 83), (105, 83), (106, 83), (107, 83), (108, 83), (109, 83), (110, 83), (111, 83); tag 0462CD1C, persistence mode 0.

**Wait for the recorded events:**

1. global flag 13 is clear.
2. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 194 (cell 104, 78).
2. Flash buildings of type CATHOSP; duration argument 40.
3. Create radar-event marker type 12 at waypoint 56 (cell 110, 82).
4. Set global flag 13.
5. Play voice notification Unit_Eva_TechHospital.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8617, Events line 8953, Actions line 9289.

<a id="trigger-09515b9c"></a>

### 48. Obj01_Complete_Text - 09515B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Power_Online (0691357C)](#trigger-0691357c).

Attached scope: tag definitions 095159BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1 Complete” (MISSION:Objective1).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8618, Events line 8954, Actions line 9290.

<a id="trigger-08a8fbcc"></a>

### 49. TM_to_Radar_Ping - 08A8FBCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Camera_Base_to_TM (0B025F3C)](#trigger-0b025f3c).

Incoming activation links: enable from [Camera_Time_Machine (0B022DEC)](#trigger-0b022dec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Ping_PP_Two (08A8E55C)](#trigger-08a8e55c).
2. Disable [TM_to_Radar_Ping (08A8FBCC)](#trigger-08a8fbcc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8619, Events line 8955, Actions line 9291.

<a id="trigger-08a8e55c"></a>

### 50. Ping_PP_Two - 08A8E55C

Owner reference: PowerHouse Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Ping1_to_Ping2 (08A8953C)](#trigger-08a8953c); enable from [TM_to_Radar_Ping (08A8FBCC)](#trigger-08a8fbcc).

Attached scope: tag definitions 08A7737C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 47 (Power_Online) is clear.

Flag writers in this mission: set local flag 47 (Power_Online) at [Power_Online (0691357C)](#trigger-0691357c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play sound CameraSwitch.
2. Jump the camera to waypoint 17 (cell 130, 130).
3. Perform no action.
4. Flash buildings of type CAPOWR01; duration argument 60.
5. Flash buildings of type CAPOWR02; duration argument 60.
6. Enable and reset applicable timers for [Start_Pointing (087F3E6C)](#trigger-087f3e6c).
7. Create radar-event marker type 0 at waypoint 17 (cell 130, 130).
8. Enable and reset applicable timers for [Ping3_to_GGI (08A868EC)](#trigger-08a868ec).
9. Disable [Ping_PP_Two (08A8E55C)](#trigger-08a8e55c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8620, Events line 8956, Actions line 9292.

<a id="trigger-08a3e03c"></a>

### 51. Time_Machine_Boom - 08A3E03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Destroyed by anything. See attached-object/cell scope below.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Announce defeat.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8621, Events line 8957, Actions line 9293.

<a id="trigger-097d02cc"></a>

### 52. Time_Machine_Attacked - 097D02CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Time_Machine_Hit (097D15DC)](#trigger-097d15dc).

Attached scope: tag definitions 097D16CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA1_EvaProtectTimeMach.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8622, Events line 8958, Actions line 9294.

<a id="trigger-0a8ea21c"></a>

### 53. Timer_Movie - 0A8EA21C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Timer_Done (0A8E0E9C)](#trigger-0a8e0e9c).

Incoming activation links: enable from [Start_Timer (0A8E573C)](#trigger-0a8e573c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Timer_Done (0A8E0E9C)](#trigger-0a8e0e9c).
2. Enable and reset applicable timers for [Center_On_TimeMachine (0C6F847C)](#trigger-0c6f847c).
3. Disable [Timer_Movie (0A8EA21C)](#trigger-0a8ea21c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8623, Events line 8959, Actions line 9295.

<a id="trigger-0b025f3c"></a>

### 54. Camera_Base_to_TM - 0B025F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Delay_ITeam_Check (08136ABC)](#trigger-08136abc).

Incoming activation links: enable from [Camera_Base02 (0885DE3C)](#trigger-0885de3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Camera_Time_Machine (0B022DEC)](#trigger-0b022dec).
2. Disable [Camera_Base_to_TM (0B025F3C)](#trigger-0b025f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8624, Events line 8960, Actions line 9296.

<a id="trigger-087f3e6c"></a>

### 55. Start_Pointing - 087F3E6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Stop_Pointing (087F124C)](#trigger-087f124c).

Incoming activation links: enable from [Ping_PP_Two (08A8E55C)](#trigger-08a8e55c).

Attached scope: tag definitions 087F133C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Point_At_Power (087F198C)](#trigger-087f198c).
2. Enable and reset applicable timers for [Stop_Pointing (087F124C)](#trigger-087f124c).
3. Disable [Start_Pointing (087F3E6C)](#trigger-087f3e6c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8625, Events line 8961, Actions line 9297.

<a id="trigger-0a8e0e9c"></a>

### 56. Timer_Done - 0A8E0E9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start_Timer (0A8E573C)](#trigger-0a8e573c).

Incoming activation links: enable from [Timer_Movie (0A8EA21C)](#trigger-0a8ea21c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Chrono Screen Effect for; main setting 40.
3. Black out the trigger owner's radar for 40 configured frames.
4. Enable and reset applicable timers for [Evict_AJAK_Gar (089AE11C)](#trigger-089ae11c).
5. Enable and reset applicable timers for [Rebuild_Nuke (0930470C)](#trigger-0930470c).
6. Disable [Timer_Done (0A8E0E9C)](#trigger-0a8e0e9c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8626, Events line 8962, Actions line 9298.

<a id="trigger-0c6f847c"></a>

### 57. Center_On_TimeMachine - 0C6F847C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Timer_Movie (0A8EA21C)](#trigger-0a8ea21c).

Incoming activation links: enable from [Timer_Movie (0A8EA21C)](#trigger-0a8ea21c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable player input.
2. Move the camera to waypoint 57 (cell 91, 105) with speed setting 3.
3. Disable [Mission1_Text (06CBE3FC)](#trigger-06cbe3fc).
4. Disable [Center_On_TimeMachine (0C6F847C)](#trigger-0c6f847c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8627, Events line 8963, Actions line 9299.

<a id="trigger-0b022dec"></a>

### 58. Camera_Time_Machine - 0B022DEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_Base_to_TM (0B025F3C)](#trigger-0b025f3c).

Attached scope: tag definitions 0B022D0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 15 (cell 93, 106) with speed setting 3.
2. Perform no action.
3. Enable and reset applicable timers for [TM_to_Radar_Ping (08A8FBCC)](#trigger-08a8fbcc).
4. Flash buildings of type CATIME01; duration argument 75.
5. Disable [Camera_Time_Machine (0B022DEC)](#trigger-0b022dec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8628, Events line 8964, Actions line 9300.

<a id="trigger-087f124c"></a>

### 59. Stop_Pointing - 087F124C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Point_At_Power (087F198C)](#trigger-087f198c).

Incoming activation links: enable from [Start_Pointing (087F3E6C)](#trigger-087f3e6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Point_At_Power (087F198C)](#trigger-087f198c).
2. Disable [Stop_Pointing (087F124C)](#trigger-087f124c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8629, Events line 8965, Actions line 9301.

<a id="trigger-087f198c"></a>

### 60. Point_At_Power - 087F198C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Pointing (087F3E6C)](#trigger-087f3e6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 483; location/duration field CR.
2. Play Anim At; main setting 483; location/duration field CS.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8630, Events line 8966, Actions line 9302.

<a id="trigger-089ae11c"></a>

### 61. Evict_AJAK_Gar - 089AE11C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Timer_Done (0A8E0E9C)](#trigger-0a8e0e9c).

Attached scope: Gas Station (CAGAS01), owner Neutral, cell (144, 97), tag 089AFD2C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Evict occupants from the attached building.
2. Enable and reset applicable timers for [Evict_UT_Gar (089AE71C)](#trigger-089ae71c).
3. Disable [Evict_AJAK_Gar (089AE11C)](#trigger-089ae11c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8631, Events line 8967, Actions line 9303.

<a id="trigger-0930470c"></a>

### 62. Rebuild_Nuke - 0930470C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Timer_Done (0A8E0E9C)](#trigger-0a8e0e9c).

Attached scope: tag definitions 093044CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 48 (Nuke_Destroyed) is set.

Flag writers in this mission: set local flag 48 (Nuke_Destroyed) at [Nuke_Plant_Gone (0930139C)](#trigger-0930139c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create building NANRCT at waypoint 364 (cell 55, 72).
2. Disable [Rebuild_Nuke (0930470C)](#trigger-0930470c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8632, Events line 8968, Actions line 9304.

<a id="trigger-089ae71c"></a>

### 63. Evict_UT_Gar - 089AE71C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evict_AJAK_Gar (089AE11C)](#trigger-089ae11c).

Attached scope: Building (CASANF01), owner Neutral, cell (127, 96), tag 089AE20C, persistence mode 2.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Evict occupants from the attached building.
2. Enable and reset applicable timers for [Evict_ZAI_Gar (089AFC3C)](#trigger-089afc3c).
3. Disable [Evict_UT_Gar (089AE71C)](#trigger-089ae71c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8633, Events line 8969, Actions line 9305.

<a id="trigger-089afc3c"></a>

### 64. Evict_ZAI_Gar - 089AFC3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evict_UT_Gar (089AE71C)](#trigger-089ae71c).

Attached scope: Building (CASANF02), owner Neutral, cell (118, 122), tag 089AFA8C, persistence mode 2.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Evict occupants from the attached building.
2. Enable and reset applicable timers for [Evict_All (0D87303C)](#trigger-0d87303c).
3. Enable and reset applicable timers for [Kill_Triggers1 (067DD4BC)](#trigger-067dd4bc).
4. Disable [Evict_ZAI_Gar (089AFC3C)](#trigger-089afc3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8634, Events line 8970, Actions line 9306.

<a id="trigger-0d87303c"></a>

### 65. Evict_All - 0D87303C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evict_ZAI_Gar (089AFC3C)](#trigger-089afc3c).

Attached scope: Building (CANEWY18), owner Neutral, cell (112, 64), tag 0D86A04C, persistence mode 0; Building (CANEWY12), owner Neutral, cell (103, 133), tag 0D86A04C, persistence mode 0; Building (CASTL02), owner Neutral, cell (108, 141), tag 0D86A04C, persistence mode 0; Building (CAPARS04), owner Neutral, cell (104, 141), tag 0D86A04C, persistence mode 0; Building (CARUS05), owner Neutral, cell (114, 138), tag 0D86A04C, persistence mode 0; McBurger Kong (CAMSC10), owner Neutral, cell (104, 89), tag 0D86A04C, persistence mode 0; Warehouse (CANEWY21), owner Neutral, cell (97, 64), tag 0D86A04C, persistence mode 0; Building (CARUS05), owner Neutral, cell (131, 137), tag 0D86A04C, persistence mode 0; Building (CAPARS04), owner Neutral, cell (145, 143), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (109, 147), tag 0D86A04C, persistence mode 0; House (CAHSE07), owner Neutral, cell (131, 96), tag 0D86A04C, persistence mode 0; Building (CARUS06), owner Neutral, cell (131, 89), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (123, 96), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (116, 122), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (127, 92), tag 0D86A04C, persistence mode 0; Office Building (CATEXS07), owner Neutral, cell (123, 75), tag 0D86A04C, persistence mode 0; Building (CANEWY12), owner Neutral, cell (114, 133), tag 0D86A04C, persistence mode 0; Building (CACHIG03), owner Neutral, cell (143, 103), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (150, 115), tag 0D86A04C, persistence mode 0; Office Building (CATEXS08), owner Neutral, cell (158, 109), tag 0D86A04C, persistence mode 0; Warehouse (CANEWY21), owner Neutral, cell (158, 113), tag 0D86A04C, persistence mode 0; Mailbox (CAMISC04), owner Neutral, cell (148, 103), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (132, 121), tag 0D86A04C, persistence mode 0; Building (CAWASH10), owner Neutral, cell (137, 137), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (112, 96), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (112, 93), tag 0D86A04C, persistence mode 0; Building (CASTL02), owner Neutral, cell (110, 89), tag 0D86A04C, persistence mode 0; Building (CACHIG01), owner Neutral, cell (111, 80), tag 0D86A04C, persistence mode 0; Gas Station (CAGAS01), owner Neutral, cell (106, 97), tag 0D86A04C, persistence mode 0; Building (CAPARS04), owner Neutral, cell (107, 74), tag 0D86A04C, persistence mode 0; Building (CAWASH07), owner Neutral, cell (104, 128), tag 0D86A04C, persistence mode 0; Building (CAWASH05), owner Neutral, cell (108, 128), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (162, 121), tag 0D86A04C, persistence mode 0; Office Building (CATEXS08), owner Neutral, cell (100, 81), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (104, 122), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (108, 122), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (110, 122), tag 0D86A04C, persistence mode 0; Building (CAWASH05), owner Neutral, cell (162, 127), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (159, 132), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (159, 128), tag 0D86A04C, persistence mode 0; Building (CANEWY12), owner Neutral, cell (150, 118), tag 0D86A04C, persistence mode 0; Building (CAWASH08), owner Neutral, cell (155, 120), tag 0D86A04C, persistence mode 0; Hotel (CAMIAM03), owner Neutral, cell (77, 84), tag 0D86A04C, persistence mode 0; Building (CANEWY11), owner Neutral, cell (82, 82), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (87, 89), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (91, 89), tag 0D86A04C, persistence mode 0; Building (CAPARS14), owner Neutral, cell (79, 115), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (89, 122), tag 0D86A04C, persistence mode 0; Building (CAWASH03), owner Neutral, cell (110, 113), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (103, 137), tag 0D86A04C, persistence mode 0; Building (CAWASH05), owner Neutral, cell (106, 104), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (114, 128), tag 0D86A04C, persistence mode 0; Warehouse (CANEWY21), owner Neutral, cell (158, 116), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (170, 121), tag 0D86A04C, persistence mode 0; Building (CASANF02), owner Neutral, cell (91, 122), tag 0D86A04C, persistence mode 0; Building (CASANF03), owner Neutral, cell (94, 122), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (96, 122), tag 0D86A04C, persistence mode 0; Building (CASANF02), owner Neutral, cell (98, 122), tag 0D86A04C, persistence mode 0; Building (CASANF03), owner Neutral, cell (106, 122), tag 0D86A04C, persistence mode 0; Building (CASANF03), owner Neutral, cell (125, 96), tag 0D86A04C, persistence mode 0; Building (CASANF02), owner Neutral, cell (149, 121), tag 0D86A04C, persistence mode 0; Building (CASANF02), owner Neutral, cell (164, 121), tag 0D86A04C, persistence mode 0; Building (CASANF03), owner Neutral, cell (160, 121), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (154, 137), tag 0D86A04C, persistence mode 0; Water Tower (CAWT01), owner Neutral, cell (147, 124), tag 0D86A04C, persistence mode 0; Building (CASANF03), owner Neutral, cell (89, 89), tag 0D86A04C, persistence mode 0; Hotel (CAMIAM03), owner Neutral, cell (115, 153), tag 0D86A04C, persistence mode 0; Building (CAWASH08), owner Neutral, cell (119, 154), tag 0D86A04C, persistence mode 0; Building (CAWASH07), owner Neutral, cell (124, 154), tag 0D86A04C, persistence mode 0; Building (CANEWY12), owner Neutral, cell (125, 158), tag 0D86A04C, persistence mode 0; Building (CANWY23), owner Neutral, cell (121, 161), tag 0D86A04C, persistence mode 0; Building (CACHIG01), owner Neutral, cell (149, 128), tag 0D86A04C, persistence mode 0; Building (CAWASH07), owner Neutral, cell (153, 128), tag 0D86A04C, persistence mode 0; Building (CASTL02), owner Neutral, cell (153, 132), tag 0D86A04C, persistence mode 0; Building (CACHIG03), owner Neutral, cell (150, 133), tag 0D86A04C, persistence mode 0; Building (CASANF03), owner Neutral, cell (130, 121), tag 0D86A04C, persistence mode 0; Building (CASANF01), owner Neutral, cell (128, 121), tag 0D86A04C, persistence mode 0; Building (CACHIG01), owner Neutral, cell (118, 128), tag 0D86A04C, persistence mode 0; Gas Station (CAGAS01), owner Neutral, cell (118, 107), tag 0D86A04C, persistence mode 0; Office Building (CATEXS06), owner Neutral, cell (119, 113), tag 0D86A04C, persistence mode 0; Water Tower (CAWT01), owner Neutral, cell (123, 118), tag 0D86A04C, persistence mode 0; Water Tower (CAWT01), owner Neutral, cell (120, 85), tag 0D86A04C, persistence mode 0; Office Building (CATEXS08), owner Neutral, cell (122, 90), tag 0D86A04C, persistence mode 0; Dumpster (CAMISC03), owner Neutral, cell (128, 90), tag 0D86A04C, persistence mode 0; Office Building (CATEXS08), owner Neutral, cell (142, 113), tag 0D86A04C, persistence mode 0; Building (CAPARS04), owner Neutral, cell (135, 116), tag 0D86A04C, persistence mode 0; Building (CASANF03), owner Neutral, cell (133, 107), tag 0D86A04C, persistence mode 0; Building (CASANF02), owner Neutral, cell (140, 107), tag 0D86A04C, persistence mode 0; Dumpster (CAMISC03), owner Neutral, cell (153, 111), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (146, 103), tag 0D86A04C, persistence mode 0; Building (CACHIG02), owner Neutral, cell (147, 107), tag 0D86A04C, persistence mode 0; Building (CASANF08), owner Neutral, cell (129, 116), tag 0D86A04C, persistence mode 0; Building (CASANF06), owner Neutral, cell (128, 113), tag 0D86A04C, persistence mode 0; Building (CASANF07), owner Neutral, cell (127, 108), tag 0D86A04C, persistence mode 0; Building (CASANF06), owner Neutral, cell (126, 106), tag 0D86A04C, persistence mode 0; Building (CASANF07), owner Neutral, cell (126, 104), tag 0D86A04C, persistence mode 0; Building (CASTL01), owner Neutral, cell (85, 79), tag 0D86A04C, persistence mode 0; Office Building (CATEXS07), owner Neutral, cell (101, 72), tag 0D86A04C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Evict occupants from the attached building.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8635, Events line 8971, Actions line 9307.

<a id="trigger-067dd4bc"></a>

### 66. Kill_Triggers1 - 067DD4BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Create_Stuff (067DD9FC)](#trigger-067dd9fc).

Incoming activation links: enable from [Evict_ZAI_Gar (089AFC3C)](#trigger-089afc3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Delay_ITeam_Check (08136ABC)](#trigger-08136abc).
2. Disable [Create_Hover_One (0B7D4BCC)](#trigger-0b7d4bcc).
3. Disable [Drop_I_Team (0813427C)](#trigger-0813427c).
4. Disable [Hover1_Death (0B7D615C)](#trigger-0b7d615c).
5. Disable [Hover1_Go_Home (0B7D6AAC)](#trigger-0b7d6aac).
6. Disable [Paradrop_I_Death (08135C1C)](#trigger-08135c1c).
7. Enable and reset applicable timers for [Kill_Triggers2 (0CF0864C)](#trigger-0cf0864c).
8. Disable [AP_Paradrop_Death (0BDF7BBC)](#trigger-0bdf7bbc).
9. Disable [Kill_Triggers1 (067DD4BC)](#trigger-067dd4bc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8636, Events line 8972, Actions line 9308.

<a id="trigger-067dd9fc"></a>

### 67. Create_Stuff - 067DD9FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Fix_Buildings (085159EC)](#trigger-085159ec).

Incoming activation links: enable from [Fix_Buildings (085159EC)](#trigger-085159ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Clear all smudges; main setting 0.
2. Enable and reset applicable timers for [Create_Apocs(Easy) (05EE7C8C)](#trigger-05ee7c8c).
3. Enable and reset applicable timers for [Create_Apocs(MedHard) (05EE7B9C)](#trigger-05ee7b9c).
4. Supply reinforcement team [TEAM_Dred1 (0955BB7C)](all01umd-teams.md#team-0955bb7c) at waypoint 127 (cell 64, 90).
5. Supply reinforcement team [TEAM_Dred2 (0955B6CC)](all01umd-teams.md#team-0955b6cc) at waypoint 128 (cell 68, 87).
6. Perform no action.
7. Enable and reset applicable timers for [Create_Stuff2 (089D5A8C)](#trigger-089d5a8c).
8. Disable [Create_Stuff (067DD9FC)](#trigger-067dd9fc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8637, Events line 8973, Actions line 9309.

<a id="trigger-0b7d6aac"></a>

### 68. Hover1_Go_Home - 0B7D6AAC

Owner reference: Nod. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 0 (Hover1_Unloaded) is set.

Flag writers in this mission: clear local flag 0 (Hover1_Unloaded) at [Hover1_Go_Home (0B7D6AAC)](#trigger-0b7d6aac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 0 (Hover1_Unloaded).
2. Create/recruit team [Hover1_Home_Team (0B7D664C)](all01umd-teams.md#team-0b7d664c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8638, Events line 8974, Actions line 9310.

<a id="trigger-0cf0864c"></a>

### 69. Kill_Triggers2 - 0CF0864C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Kill_Triggers1 (067DD4BC)](#trigger-067dd4bc).

Incoming activation links: enable from [Kill_Triggers1 (067DD4BC)](#trigger-067dd4bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Check_Hover2 (089FC3DC)](#trigger-089fc3dc).
2. Disable [Check_Hover3 (0B1613DC)](#trigger-0b1613dc).
3. Disable [Create_Hover_2 (0895C19C)](#trigger-0895c19c).
4. Disable [Create_Hover_3 (0B16029C)](#trigger-0b16029c).
5. Disable [Hover2_Death (0895D88C)](#trigger-0895d88c).
6. Disable [Hover2_Go_Home (08A2318C)](#trigger-08a2318c).
7. Disable [Hover3_Death (0B160E5C)](#trigger-0b160e5c).
8. Disable [Hover3_Go_Home (0B1612EC)](#trigger-0b1612ec).
9. Enable and reset applicable timers for [Kill_Units (0693BF3C)](#trigger-0693bf3c).
10. Disable [Kill_Triggers2 (0CF0864C)](#trigger-0cf0864c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8639, Events line 8975, Actions line 9311.

<a id="trigger-085159ec"></a>

### 70. Fix_Buildings - 085159EC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kill_Units2 (08AE3E3C)](#trigger-08ae3e3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Restore Starting Buildings of: owner selector 12 (country/type NEUTRAL; placed owner Neutral).
2. Restore Starting Buildings of: owner selector 4 (country/type BRITISH; placed owner British).
3. Supply reinforcement team [TEAM_Dred4 (09569A4C)](all01umd-teams.md#team-09569a4c).
4. Supply reinforcement team [TEAM_Dred5 (0956959C)](all01umd-teams.md#team-0956959c).
5. Supply reinforcement team [TEAM_Dred6 (0956AEFC)](all01umd-teams.md#team-0956aefc).
6. Supply reinforcement team [TEAM_Dred7 (0B4FFC8C)](all01umd-teams.md#team-0b4ffc8c).
7. Restore Starting Buildings of: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
8. Enable and reset applicable timers for [Create_Stuff (067DD9FC)](#trigger-067dd9fc).
9. Disable [Fix_Buildings (085159EC)](#trigger-085159ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8640, Events line 8976, Actions line 9312.

<a id="trigger-05ee7c8c"></a>

### 71. Create_Apocs(Easy) - 05EE7C8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Send_Armor(Hard) (087C0D5C)](#trigger-087c0d5c).

Incoming activation links: enable from [Create_Stuff (067DD9FC)](#trigger-067dd9fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Apoc1 (093DDC8C)](all01umd-teams.md#team-093ddc8c) at waypoint 82 (cell 80, 100).
2. Supply reinforcement team [TEAM_Apoc2 (093DD7DC)](all01umd-teams.md#team-093dd7dc) at waypoint 83 (cell 80, 102).
3. Disable [Create_Apocs(Easy) (05EE7C8C)](#trigger-05ee7c8c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8641, Events line 8977, Actions line 9313.

<a id="trigger-05ee7b9c"></a>

### 72. Create_Apocs(MedHard) - 05EE7B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Create_Apocs(Easy) (05EE7C8C)](#trigger-05ee7c8c).

Incoming activation links: enable from [Create_Stuff (067DD9FC)](#trigger-067dd9fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Apoc1 (093DDC8C)](all01umd-teams.md#team-093ddc8c) at waypoint 82 (cell 80, 100).
2. Supply reinforcement team [TEAM_Apoc2 (093DD7DC)](all01umd-teams.md#team-093dd7dc) at waypoint 83 (cell 80, 102).
3. Supply reinforcement team [TEAM_Apoc3 (093DD32C)](all01umd-teams.md#team-093dd32c) at waypoint 84 (cell 82, 103).
4. Supply reinforcement team [TEAM_Apoc4 (093DFDEC)](all01umd-teams.md#team-093dfdec) at waypoint 85 (cell 82, 100).
5. Disable [Create_Apocs(MedHard) (05EE7B9C)](#trigger-05ee7b9c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8642, Events line 8978, Actions line 9314.

<a id="trigger-089d5a8c"></a>

### 73. Create_Stuff2 - 089D5A8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Kill_Units2 (08AE3E3C)](#trigger-08ae3e3c).

Incoming activation links: enable from [Create_Stuff (067DD9FC)](#trigger-067dd9fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Dred3 (0955B21C)](all01umd-teams.md#team-0955b21c) at waypoint 129 (cell 86, 65).
2. Supply reinforcement team [TEAM_Scorp1 (09645EFC)](all01umd-teams.md#team-09645efc) at waypoint 513 (cell 69, 79).
3. Supply reinforcement team [TEAM_Scorp2 (09645A4C)](all01umd-teams.md#team-09645a4c) at waypoint 514 (cell 77, 71).
4. Supply reinforcement team [TEAM_Scorp3 (0964580C)](all01umd-teams.md#team-0964580c) at waypoint 515 (cell 81, 62).
5. Supply reinforcement team [TEAM_Scorp4 (096455CC)](all01umd-teams.md#team-096455cc) at waypoint 516 (cell 73, 50).
6. Enable and reset applicable timers for [Play_Movies (0899832C)](#trigger-0899832c).
7. Disable [Create_Stuff2 (089D5A8C)](#trigger-089d5a8c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8643, Events line 8979, Actions line 9315.

<a id="trigger-08a2318c"></a>

### 74. Hover2_Go_Home - 08A2318C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Hover1_Go_Home (0B7D6AAC)](#trigger-0b7d6aac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 1 (Hover_2_Unloaded) is set.

Flag writers in this mission: clear local flag 1 (Hover_2_Unloaded) at [Hover2_Go_Home (08A2318C)](#trigger-08a2318c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 1 (Hover_2_Unloaded).
2. Create/recruit team [Hover2_Home_Team (0AB4AB7C)](all01umd-teams.md#team-0ab4ab7c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8644, Events line 8980, Actions line 9316.

<a id="trigger-0b1612ec"></a>

### 75. Hover3_Go_Home - 0B1612EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Hover2_Go_Home (08A2318C)](#trigger-08a2318c).

Attached scope: tag definitions 0B7D688C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Hover_3_Unloaded) is set.

Flag writers in this mission: clear local flag 2 (Hover_3_Unloaded) at [Hover3_Go_Home (0B1612EC)](#trigger-0b1612ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 2 (Hover_3_Unloaded).
2. Create/recruit team [Hover3_Home_Team (0B16493C)](all01umd-teams.md#team-0b16493c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8645, Events line 8981, Actions line 9317.

<a id="trigger-0693bf3c"></a>

### 76. Kill_Units - 0693BF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Kill_Triggers2 (0CF0864C)](#trigger-0cf0864c).

Incoming activation links: enable from [Kill_Triggers2 (0CF0864C)](#trigger-0cf0864c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy all Land Units of: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Destroy all Land Units of: owner selector 8 (country/type RUSSIANS; placed owner Russians).
3. Destroy all Land Units of: owner selector 11 (country/type NOD; placed owner Nod).
4. Destroy all Naval Units of: owner selector 11 (country/type NOD; placed owner Nod).
5. Destroy all Buildings of: owner selector 6 (country/type ARABS; placed owner Arabs).
6. Destroy all Land Units of: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
7. Destroy all Naval Units of: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
8. Restore Starting Buildings of: owner selector 16 (country/type BRIDGE COUNTRY; placed owner BridgeHouse).
9. Enable and reset applicable timers for [Kill_Units2 (08AE3E3C)](#trigger-08ae3e3c).
10. Disable [Kill_Units (0693BF3C)](#trigger-0693bf3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8646, Events line 8982, Actions line 9318.

<a id="trigger-087c0d5c"></a>

### 77. Send_Armor(Hard) - 087C0D5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Send_Armor(Easy) (087C0E4C)](#trigger-087c0e4c).

Incoming activation links: enable from [Start_Sounds2 (04C19E5C)](#trigger-04c19e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_SovArmor1 (0925E45C)](all01umd-teams.md#team-0925e45c).
2. Supply reinforcement team [TEAM_SovArmor2 (0925FDEC)](all01umd-teams.md#team-0925fdec).
3. Enable and reset applicable timers for [Apocs_Gone (0AC8355C)](#trigger-0ac8355c).
4. Disable [Send_Armor(Hard) (087C0D5C)](#trigger-087c0d5c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8647, Events line 8983, Actions line 9319.

<a id="trigger-08ae3e3c"></a>

### 78. Kill_Units2 - 08AE3E3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Kill_Units (0693BF3C)](#trigger-0693bf3c).

Incoming activation links: enable from [Kill_Units (0693BF3C)](#trigger-0693bf3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy all Land Units of: owner selector 3 (country/type GERMANS; placed owner Germans).
2. Destroy all Naval Units of: owner selector 3 (country/type GERMANS; placed owner Germans).
3. Destroy all Land Units of: owner selector 5 (country/type AFRICANS; placed owner Africans).
4. Destroy all of: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
5. Enable and reset applicable timers for [Fix_Buildings (085159EC)](#trigger-085159ec).
6. Enable and reset applicable timers for [Kill_Triggers_3 (0BBC1E3C)](#trigger-0bbc1e3c).
7. Disable [Kill_Units2 (08AE3E3C)](#trigger-08ae3e3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8648, Events line 8984, Actions line 9320.

<a id="trigger-0899832c"></a>

### 79. Play_Movies - 0899832C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Create_Stuff2 (089D5A8C)](#trigger-089d5a8c).

Incoming activation links: enable from [Create_Stuff2 (089D5A8C)](#trigger-089d5a8c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 4 (Tanya_Dead) is clear.

Flag writers in this mission: set local flag 4 (Tanya_Dead) at [Tanya_Death (089B82BC)](#trigger-089b82bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 3 (Time_Warp).
2. Enable and reset applicable timers for [Make_Civ_Cars1 (0B3778EC)](#trigger-0b3778ec).
3. Disable [Play_Movies (0899832C)](#trigger-0899832c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8649, Events line 8985, Actions line 9321.

<a id="trigger-087c0e4c"></a>

### 80. Send_Armor(Easy) - 087C0E4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Send_Armor(Med) (087C0F3C)](#trigger-087c0f3c).

Incoming activation links: enable from [Start_Sounds2 (04C19E5C)](#trigger-04c19e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_SovArmor1 (0925E45C)](all01umd-teams.md#team-0925e45c).
2. Supply reinforcement team [TEAM_SovArmor2 (0925FDEC)](all01umd-teams.md#team-0925fdec).
3. Enable and reset applicable timers for [Apocs_Gone (0AC8355C)](#trigger-0ac8355c).
4. Disable [Send_Armor(Easy) (087C0E4C)](#trigger-087c0e4c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8650, Events line 8986, Actions line 9322.

<a id="trigger-0ac8355c"></a>

### 81. Apocs_Gone - 0AC8355C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Send_Armor(Hard) (087C0D5C)](#trigger-087c0d5c); enable from [Send_Armor(Easy) (087C0E4C)](#trigger-087c0e4c); enable from [Send_Armor(Med) (087C0F3C)](#trigger-087c0f3c).

Attached scope: tag definitions 0AC86E7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type SPECIAL; placed owner Special).
2. Destroyed,  All: owner selector 15 (country/type SOVIET2 COUNTRY; placed owner Soviet2House).

**Then perform these actions in order:**

1. Disable player input.
2. Move the camera to waypoint 420 (cell 95, 106) with speed setting 4.
3. Enable and reset applicable timers for [Enter_Tanya (0AC85F3C)](#trigger-0ac85f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8651, Events line 8987, Actions line 9323.

<a id="trigger-0bbc1e3c"></a>

### 82. Kill_Triggers_3 - 0BBC1E3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start_Sounds2 (04C19E5C)](#trigger-04c19e5c).

Incoming activation links: enable from [Kill_Units2 (08AE3E3C)](#trigger-08ae3e3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Reveal_Gatt1 (0B94716C)](#trigger-0b94716c).
2. Disable [Reveal_Gatt2 (095259AC)](#trigger-095259ac).
3. Disable [Reveal_Gatt3 (0B94432C)](#trigger-0b94432c).
4. Disable [Reveal_Gatt4 (0B945A6C)](#trigger-0b945a6c).
5. Disable [TurnOff_Gatt1 (096109AC)](#trigger-096109ac).
6. Disable [TurnOff_Gatt2 (0D38F4CC)](#trigger-0d38f4cc).
7. Disable [TurnOff_Gatt4 (097303DC)](#trigger-097303dc).
8. Disable [TurnOn_Gatt1 (09610F3C)](#trigger-09610f3c).
9. Enable and reset applicable timers for [Kill_Triggers_4 (0BBCED7C)](#trigger-0bbced7c).
10. Disable [Kill_Triggers_3 (0BBC1E3C)](#trigger-0bbc1e3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8652, Events line 8988, Actions line 9324.

<a id="trigger-0b3778ec"></a>

### 83. Make_Civ_Cars1 - 0B3778EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Play_Movies (0899832C)](#trigger-0899832c).

Incoming activation links: enable from [Play_Movies (0899832C)](#trigger-0899832c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create_Kirov (0921804C)](#trigger-0921804c).
2. Supply reinforcement team [TEAM_Truck1 (0A7AB0CC)](all01umd-teams.md#team-0a7ab0cc).
3. Supply reinforcement team [TEAM_Cop1 (0A7ACC6C)](all01umd-teams.md#team-0a7acc6c).
4. Supply reinforcement team [TEAM_ConVehicle1 (0A7AC7BC)](all01umd-teams.md#team-0a7ac7bc).
5. Supply reinforcement team [TEAM_ConVehicle2 (0A7AC30C)](all01umd-teams.md#team-0a7ac30c).
6. Supply reinforcement team [TEAM_Cop2 (0A7ADDEC)](all01umd-teams.md#team-0a7addec).
7. Supply reinforcement team [TEAM_Stat_Stang (068FC13C)](all01umd-teams.md#team-068fc13c) at waypoint 182 (cell 156, 117).
8. Supply reinforcement team [TEAM_Stat_SUVW (068FDEFC)](all01umd-teams.md#team-068fdefc) at waypoint 183 (cell 155, 113).
9. Enable and reset applicable timers for [Make_Civ_Cars2 (0692A65C)](#trigger-0692a65c).
10. Disable [Make_Civ_Cars1 (0B3778EC)](#trigger-0b3778ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8653, Events line 8989, Actions line 9325.

<a id="trigger-087c0f3c"></a>

### 84. Send_Armor(Med) - 087C0F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Kill_Triggers_4 (0BBCED7C)](#trigger-0bbced7c).

Incoming activation links: enable from [Start_Sounds2 (04C19E5C)](#trigger-04c19e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_SovArmor1 (0925E45C)](all01umd-teams.md#team-0925e45c).
2. Supply reinforcement team [TEAM_SovArmor2 (0925FDEC)](all01umd-teams.md#team-0925fdec).
3. Enable and reset applicable timers for [Apocs_Gone (0AC8355C)](#trigger-0ac8355c).
4. Disable [Send_Armor(Med) (087C0F3C)](#trigger-087c0f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8654, Events line 8990, Actions line 9326.

<a id="trigger-0ac85f3c"></a>

### 85. Enter_Tanya - 0AC85F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Apocs_Gone (0AC8355C)](#trigger-0ac8355c).

Attached scope: tag definitions 0AC8581C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Tanya (088C1A4C)](all01umd-teams.md#team-088c1a4c).
2. Flash team [TEAM_Tanya (088C1A4C)](all01umd-teams.md#team-088c1a4c) with duration setting 40.
3. Enable player input.
4. Enable and reset applicable timers for [Tanya_Death (089B82BC)](#trigger-089b82bc).
5. Play voice notification Mis_xA1_TanyaSwimHint.
6. Enable and reset applicable timers for [Mission2_Text (046358AC)](#trigger-046358ac).
7. Disable [Time_Machine_Boom2 (08707A2C)](#trigger-08707a2c).
8. Disable [Enter_Tanya (0AC85F3C)](#trigger-0ac85f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8655, Events line 8991, Actions line 9327.

<a id="trigger-04c19e5c"></a>

### 86. Start_Sounds2 - 04C19E5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Incoming activation links: enable from [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Send_Armor(Easy) (087C0E4C)](#trigger-087c0e4c).
2. Enable and reset applicable timers for [Send_Armor(Med) (087C0F3C)](#trigger-087c0f3c).
3. Enable and reset applicable timers for [Sell_Psychic (0951879C)](#trigger-0951879c).
4. Supply reinforcement team [TEAM_CableCar2 (060FB74C)](all01umd-teams.md#team-060fb74c).
5. Enable and reset applicable timers for [Send_Armor(Hard) (087C0D5C)](#trigger-087c0d5c).
6. Enable and reset applicable timers for [Check_BridgePiece02 (092AF4AC)](#trigger-092af4ac).
7. Perform no action.
8. Disable [Start_Sounds2 (04C19E5C)](#trigger-04c19e5c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8656, Events line 8992, Actions line 9328.

<a id="trigger-0b94716c"></a>

### 87. Reveal_Gatt1 - 0B94716C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 62 (cell 120, 77).
2. Play sound WarningAlarm.
3. Create radar-event marker type 5 at waypoint 62 (cell 120, 77).
4. Enable and reset applicable timers for [Gatt_Brief (045A11CC)](#trigger-045a11cc).
5. Enable and reset applicable timers for [TurnOn_Gatt1 (09610F3C)](#trigger-09610f3c).
6. Enable and reset applicable timers for [TurnOff_Gatt1 (096109AC)](#trigger-096109ac).
7. Disable [Reveal_Gatt1 (0B94716C)](#trigger-0b94716c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8657, Events line 8993, Actions line 9329.

<a id="trigger-095259ac"></a>

### 88. Reveal_Gatt2 - 095259AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 61 (cell 139, 103).
2. Play sound WarningAlarm.
3. Create radar-event marker type 5 at waypoint 61 (cell 139, 103).
4. Enable and reset applicable timers for [Gatt_Brief (045A11CC)](#trigger-045a11cc).
5. Enable and reset applicable timers for [TurnOn_Gatt2 (0D39599C)](#trigger-0d39599c).
6. Enable and reset applicable timers for [TurnOff_Gatt2 (0D38F4CC)](#trigger-0d38f4cc).
7. Disable [Reveal_Gatt2 (095259AC)](#trigger-095259ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8658, Events line 8994, Actions line 9330.

<a id="trigger-0b94432c"></a>

### 89. Reveal_Gatt3 - 0B94432C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 63 tagged map cells: (124, 119), (125, 119), (126, 119), (118, 120), (119, 120), (120, 120), (121, 120), (122, 120), (123, 120), (124, 120), (125, 120), (128, 120), (129, 120), (130, 120), (131, 120), (132, 120), (133, 120), (134, 120), (135, 120), (118, 121), (135, 121), (118, 122), (135, 122), (118, 123), (135, 123), (118, 124), (135, 124), (118, 125), (118, 126), (118, 127), (135, 127), (118, 128), (135, 128), (118, 129), (135, 129), (118, 130), (135, 130), (118, 131), (135, 131), (118, 132), (135, 132), (118, 133), (119, 133), (126, 133), (135, 133), (119, 134), (120, 134), (121, 134), (122, 134), (123, 134), (124, 134), (125, 134), (126, 134), (127, 134), (128, 134), (129, 134), (130, 134), (131, 134), (132, 134), (133, 134), (134, 134), (135, 134), (121, 135); tag 0B945CDC, persistence mode 2.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 314 (cell 127, 127).
2. Play sound WarningAlarm.
3. Create radar-event marker type 5 at waypoint 314 (cell 127, 127).
4. Enable and reset applicable timers for [Gatt_Brief (045A11CC)](#trigger-045a11cc).
5. Disable [Reveal_Gatt3 (0B94432C)](#trigger-0b94432c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8659, Events line 8995, Actions line 9331.

<a id="trigger-0b945a6c"></a>

### 90. Reveal_Gatt4 - 0B945A6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 315 (cell 123, 146).
2. Play sound WarningAlarm.
3. Create radar-event marker type 5 at waypoint 315 (cell 123, 146).
4. Enable and reset applicable timers for [Gatt_Brief (045A11CC)](#trigger-045a11cc).
5. Enable and reset applicable timers for [TurnOn_Gatt4 (0973096C)](#trigger-0973096c).
6. Enable and reset applicable timers for [TurnOff_Gatt4 (097303DC)](#trigger-097303dc).
7. Disable [Reveal_Gatt4 (0B945A6C)](#trigger-0b945a6c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8660, Events line 8996, Actions line 9332.

<a id="trigger-096109ac"></a>

### 91. TurnOff_Gatt1 - 096109AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TurnOn_Gatt1 (09610F3C)](#trigger-09610f3c).

Incoming activation links: enable from [Reveal_Gatt1 (0B94716C)](#trigger-0b94716c).

Attached scope: 59 tagged map cells: (112, 70), (113, 70), (114, 70), (115, 70), (116, 70), (117, 70), (118, 70), (119, 70), (120, 70), (121, 70), (122, 70), (112, 71), (123, 71), (112, 72), (123, 72), (124, 72), (112, 73), (124, 73), (125, 73), (112, 74), (125, 74), (126, 74), (112, 75), (126, 75), (127, 75), (112, 76), (127, 76), (112, 77), (127, 77), (112, 78), (127, 78), (112, 79), (127, 79), (112, 80), (127, 80), (112, 81), (127, 81), (112, 82), (127, 82), (112, 83), (113, 83), (127, 83), (115, 84), (116, 84), (117, 84), (118, 84), (119, 84), (120, 84), (121, 84), (127, 84), (121, 85), (125, 85), (126, 85), (127, 85), (121, 86), (122, 86), (123, 86), (124, 86), (125, 86); tag 0B94708C, persistence mode 2.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [TurnOn_Gatt1 (09610F3C)](#trigger-09610f3c).
2. Disable [TurnOff_Gatt1 (096109AC)](#trigger-096109ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8661, Events line 8997, Actions line 9333.

<a id="trigger-0d38f4cc"></a>

### 92. TurnOff_Gatt2 - 0D38F4CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reveal_Gatt2 (095259AC)](#trigger-095259ac).

Incoming activation links: enable from [Reveal_Gatt2 (095259AC)](#trigger-095259ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [TurnOn_Gatt2 (0D39599C)](#trigger-0d39599c).
2. Disable [TurnOff_Gatt2 (0D38F4CC)](#trigger-0d38f4cc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8662, Events line 8998, Actions line 9334.

<a id="trigger-097303dc"></a>

### 93. TurnOff_Gatt4 - 097303DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TurnOn_Gatt4 (0973096C)](#trigger-0973096c).

Incoming activation links: enable from [Reveal_Gatt4 (0B945A6C)](#trigger-0b945a6c).

Attached scope: 63 tagged map cells: (118, 141), (119, 141), (120, 141), (121, 141), (122, 141), (123, 141), (124, 141), (125, 141), (126, 141), (127, 141), (128, 141), (129, 141), (130, 141), (131, 141), (116, 142), (117, 142), (118, 142), (131, 142), (116, 143), (131, 143), (116, 144), (131, 144), (116, 145), (131, 145), (116, 146), (131, 146), (116, 147), (130, 147), (131, 147), (116, 148), (130, 148), (116, 149), (130, 149), (116, 150), (130, 150), (116, 151), (117, 151), (129, 151), (130, 151), (117, 152), (128, 152), (129, 152), (117, 153), (127, 153), (128, 153), (117, 154), (127, 154), (117, 155), (127, 155), (117, 156), (118, 156), (126, 156), (127, 156), (118, 157), (119, 157), (120, 157), (121, 157), (122, 157), (123, 157), (124, 157), (125, 157), (126, 157), (127, 157); tag 0B94598C, persistence mode 2.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [TurnOn_Gatt4 (0973096C)](#trigger-0973096c).
2. Disable [TurnOff_Gatt4 (097303DC)](#trigger-097303dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8663, Events line 8999, Actions line 9335.

<a id="trigger-09610f3c"></a>

### 94. TurnOn_Gatt1 - 09610F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reveal_Gatt1 (0B94716C)](#trigger-0b94716c).

Incoming activation links: enable from [Reveal_Gatt1 (0B94716C)](#trigger-0b94716c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 483; location/duration field LA.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8664, Events line 9000, Actions line 9336.

<a id="trigger-0bbced7c"></a>

### 95. Kill_Triggers_4 - 0BBCED7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Kill_Triggers_3 (0BBC1E3C)](#trigger-0bbc1e3c).

Incoming activation links: enable from [Kill_Triggers_3 (0BBC1E3C)](#trigger-0bbc1e3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Connector_Gone (07A8917C)](#trigger-07a8917c).
2. Enable and reset applicable timers for [CenterPiece_Gone01 (0835813C)](#trigger-0835813c).
3. Enable and reset applicable timers for [Stop_Rebuild (0993F7BC)](#trigger-0993f7bc).
4. Enable and reset applicable timers for [Really_Play_Movie (05E9106C)](#trigger-05e9106c).
5. Disable [TurnOn_Gatt2 (0D39599C)](#trigger-0d39599c).
6. Disable [TurnOn_Gatt4 (0973096C)](#trigger-0973096c).
7. Disable [Kill_Triggers_4 (0BBCED7C)](#trigger-0bbced7c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8665, Events line 9001, Actions line 9337.

<a id="trigger-0921804c"></a>

### 96. Create_Kirov - 0921804C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Make_Civ_Cars1 (0B3778EC)](#trigger-0b3778ec).

Attached scope: tag definitions 092187BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Kirov_HT (0941632C)](all01umd-teams.md#team-0941632c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8666, Events line 9002, Actions line 9338.

<a id="trigger-0692a65c"></a>

### 97. Make_Civ_Cars2 - 0692A65C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_People (06A1D17C)](#trigger-06a1d17c).

Incoming activation links: enable from [Make_Civ_Cars1 (0B3778EC)](#trigger-0b3778ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_SUVW1 (0692D74C)](all01umd-teams.md#team-0692d74c).
2. Supply reinforcement team [TEAM_Cop3 (0692AB8C)](all01umd-teams.md#team-0692ab8c).
3. Supply reinforcement team [TEAM_Cop4 (069226CC)](all01umd-teams.md#team-069226cc).
4. Supply reinforcement team [TEAM_SUVB_LL (0C39AEFC)](all01umd-teams.md#team-0c39aefc) at waypoint 189 (cell 83, 93).
5. Supply reinforcement team [TEAM_WINI_UR (0C39803C)](all01umd-teams.md#team-0c39803c) at waypoint 190 (cell 82, 94).
6. Supply reinforcement team [TEAM_Stang2 (0C8992CC)](all01umd-teams.md#team-0c8992cc) at waypoint 113 (cell 84, 102).
7. Supply reinforcement team [TEAM_Bus1 (08BF127C)](all01umd-teams.md#team-08bf127c) at waypoint 55 (cell 127, 100).
8. Supply reinforcement team [TEAM_SUVB_2 (0A7C0A8C)](all01umd-teams.md#team-0a7c0a8c) at waypoint 28 (cell 135, 126).
9. Enable and reset applicable timers for [Make_People (06A1D17C)](#trigger-06a1d17c).
10. Disable [Make_Civ_Cars2 (0692A65C)](#trigger-0692a65c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8667, Events line 9003, Actions line 9339.

<a id="trigger-08707a2c"></a>

### 98. Time_Machine_Boom2 - 08707A2C

Owner reference: British. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Time_Machine_Hit (097D15DC)](#trigger-097d15dc).

Attached scope: Time Machine (CATIME01), owner Americans, cell (91, 105), tag 08A4004C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is set.
2. No instances of Tanya (TANY) exist on the map, under this event's ownership scope.
3. Destroyed by anything. See attached-object/cell scope below.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8668, Events line 9004, Actions line 9340.

<a id="trigger-04c2263c"></a>

### 99. Start_New_Sounds - 04C2263C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Kill_Sounds3 (04C24A8C)](#trigger-04c24a8c).

Incoming activation links: enable from [Kill_Sounds3 (04C24A8C)](#trigger-04c24a8c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Traffic_Sounds1 (04C2410C)](#trigger-04c2410c).
2. Enable and reset applicable timers for [Traffic_Sounds2 (04C2D1DC)](#trigger-04c2d1dc).
3. Enable and reset applicable timers for [Traffic_Sounds3 (089A6BAC)](#trigger-089a6bac).
4. Enable and reset applicable timers for [Traffic_Sounds4 (04BF608C)](#trigger-04bf608c).
5. Enable and reset applicable timers for [Traffic_Sounds5 (04C0776C)](#trigger-04c0776c).
6. Enable and reset applicable timers for [Bird_Sounds1 (089B776C)](#trigger-089b776c).
7. Enable and reset applicable timers for [Bird_Sounds2 (04BF8F3C)](#trigger-04bf8f3c).
8. Enable and reset applicable timers for [Bird_Sounds3 (04C3064C)](#trigger-04c3064c).
9. Enable and reset applicable timers for [Start_Sounds2 (04C19E5C)](#trigger-04c19e5c).
10. Disable [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8669, Events line 9005, Actions line 9341.

<a id="trigger-0951879c"></a>

### 100. Sell_Psychic - 0951879C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PsychicDead (089EC19C)](#trigger-089ec19c).

Incoming activation links: enable from [Start_Sounds2 (04C19E5C)](#trigger-04c19e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.
2. Enable and reset applicable timers for [Build_Dom (0B8A090C)](#trigger-0b8a090c).
3. Disable [Sell_Psychic (0951879C)](#trigger-0951879c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8670, Events line 9006, Actions line 9342.

<a id="trigger-092af4ac"></a>

### 101. Check_BridgePiece02 - 092AF4AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Sounds2 (04C19E5C)](#trigger-04c19e5c).

Attached scope: tag definitions 092AF1CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Golden Gate Bridge (CASANF10) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 78; location/duration field CA.
2. Apply 100 damage at; main setting 59; location/duration field BH.
3. Apply 100 damage at; main setting 59; location/duration field BH.
4. Apply 100 damage at; main setting 60; location/duration field BI.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8671, Events line 9007, Actions line 9343.

<a id="trigger-045a11cc"></a>

### 102. Gatt_Brief - 045A11CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reveal_Gatt1 (0B94716C)](#trigger-0b94716c); enable from [Reveal_Gatt2 (095259AC)](#trigger-095259ac); enable from [Reveal_Gatt3 (0B94432C)](#trigger-0b94432c); enable from [Reveal_Gatt4 (0B945A6C)](#trigger-0b945a6c).

Attached scope: tag definitions 045AECDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_GatCannon.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8672, Events line 9008, Actions line 9344.

<a id="trigger-0d39599c"></a>

### 103. TurnOn_Gatt2 - 0D39599C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TurnOff_Gatt2 (0D38F4CC)](#trigger-0d38f4cc).

Incoming activation links: enable from [Reveal_Gatt2 (095259AC)](#trigger-095259ac).

Attached scope: 64 tagged map cells: (138, 93), (140, 93), (132, 94), (133, 94), (134, 94), (135, 94), (136, 94), (137, 94), (138, 94), (139, 94), (140, 94), (141, 94), (142, 94), (130, 95), (131, 95), (132, 95), (142, 95), (130, 96), (142, 96), (143, 96), (144, 96), (145, 96), (146, 96), (130, 97), (130, 98), (130, 99), (130, 100), (146, 100), (130, 101), (146, 101), (130, 102), (146, 102), (130, 103), (146, 103), (130, 104), (146, 104), (130, 105), (146, 105), (130, 106), (131, 106), (132, 106), (146, 106), (132, 107), (146, 107), (132, 108), (135, 108), (136, 108), (146, 108), (132, 109), (133, 109), (134, 109), (135, 109), (137, 109), (146, 109), (137, 110), (138, 110), (139, 110), (140, 110), (141, 110), (142, 110), (143, 110), (144, 110), (145, 110), (146, 110); tag 0B94441C, persistence mode 2.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 483; location/duration field LB.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8673, Events line 9009, Actions line 9345.

<a id="trigger-0973096c"></a>

### 104. TurnOn_Gatt4 - 0973096C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reveal_Gatt4 (0B945A6C)](#trigger-0b945a6c).

Incoming activation links: enable from [Reveal_Gatt4 (0B945A6C)](#trigger-0b945a6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 483; location/duration field LD.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8674, Events line 9010, Actions line 9346.

<a id="trigger-07a8917c"></a>

### 105. Connector_Gone - 07A8917C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kill_Triggers_4 (0BBCED7C)](#trigger-0bbced7c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Golden Gate Bridge (CASANF09) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Connector_Step2 (07A8CCBC)](#trigger-07a8ccbc).
2. Apply 100 damage at; main setting 70; location/duration field BS.
3. Disable [Connector_Gone (07A8917C)](#trigger-07a8917c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8675, Events line 9011, Actions line 9347.

<a id="trigger-0835813c"></a>

### 106. CenterPiece_Gone01 - 0835813C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kill_Triggers_4 (0BBCED7C)](#trigger-0bbced7c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Golden Gate Bridge (CASANF04) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 97; location/duration field CT.
2. Apply 100 damage at; main setting 97; location/duration field CT.
3. Apply 100 damage at; main setting 97; location/duration field CT.
4. Apply 100 damage at; main setting 97; location/duration field CT.
5. Apply 100 damage at; main setting 144; location/duration field EO.
6. Apply 100 damage at; main setting 144; location/duration field EO.
7. Apply 100 damage at; main setting 144; location/duration field EO.
8. Apply 100 damage at; main setting 144; location/duration field EO.
9. Enable and reset applicable timers for [CenterPiece_Gone02 (0935A09C)](#trigger-0935a09c).
10. Disable [CenterPiece_Gone01 (0835813C)](#trigger-0835813c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8676, Events line 9012, Actions line 9348.

<a id="trigger-0993f7bc"></a>

### 107. Stop_Rebuild - 0993F7BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Create_Apocs(MedHard) (05EE7B9C)](#trigger-05ee7b9c).

Incoming activation links: enable from [Kill_Triggers_4 (0BBCED7C)](#trigger-0bbced7c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Rebuild_Cannon1 (08D5D50C)](#trigger-08d5d50c).
2. Disable [Rebuild_Cannon2 (08D5D1EC)](#trigger-08d5d1ec).
3. Disable [Rebuild_Cannon3 (08D5BD9C)](#trigger-08d5bd9c).
4. Disable [Rebuild_Cannon4 (08D5BA7C)](#trigger-08d5ba7c).
5. Disable [Stop_Rebuild (0993F7BC)](#trigger-0993f7bc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8677, Events line 9013, Actions line 9349.

<a id="trigger-05e9106c"></a>

### 108. Really_Play_Movie - 05E9106C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Stop_Rebuild (0993F7BC)](#trigger-0993f7bc).

Incoming activation links: enable from [Kill_Triggers_4 (0BBCED7C)](#trigger-0bbced7c).

Attached scope: tag definitions 0851548C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 4.
2. Enable and reset applicable timers for [Kirov_Reporting (0790DF3C)](#trigger-0790df3c).
3. Disable [Really_Play_Movie (05E9106C)](#trigger-05e9106c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8678, Events line 9014, Actions line 9350.

<a id="trigger-06a1d17c"></a>

### 109. Make_People - 06A1D17C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_Civ_Cars1 (0B3778EC)](#trigger-0b3778ec).

Incoming activation links: enable from [Make_Civ_Cars2 (0692A65C)](#trigger-0692a65c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Calm_Civ1 (068FE26C)](all01umd-teams.md#team-068fe26c) at waypoint 156 (cell 87, 95).
2. Supply reinforcement team [TEAM_Calm_Civ2 (068FFC5C)](all01umd-teams.md#team-068ffc5c) at waypoint 157 (cell 90, 95).
3. Supply reinforcement team [TEAM_Calm_Civ3 (068FFB2C)](all01umd-teams.md#team-068ffb2c) at waypoint 158 (cell 91, 97).
4. Supply reinforcement team [TEAM_Calm_Civ2 (068FFC5C)](all01umd-teams.md#team-068ffc5c) at waypoint 159 (cell 88, 93).
5. Supply reinforcement team [TEAM_Calm_Civ1 (068FE26C)](all01umd-teams.md#team-068fe26c) at waypoint 160 (cell 83, 121).
6. Supply reinforcement team [TEAM_Calm_Civ3 (068FFB2C)](all01umd-teams.md#team-068ffb2c) at waypoint 161 (cell 84, 123).
7. Supply reinforcement team [TEAM_Calm_Civ1 (068FE26C)](all01umd-teams.md#team-068fe26c) at waypoint 162 (cell 115, 108).
8. Supply reinforcement team [TEAM_Civ3 (06A1DEBC)](all01umd-teams.md#team-06a1debc) at waypoint 163 (cell 148, 104).
9. Enable and reset applicable timers for [Make_People2 (08A6340C)](#trigger-08a6340c).
10. Disable [Make_People (06A1D17C)](#trigger-06a1d17c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8679, Events line 9015, Actions line 9351.

<a id="trigger-04c24a8c"></a>

### 110. Kill_Sounds3 - 04C24A8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Kill_Sounds2 (04C230EC)](#trigger-04c230ec).

Incoming activation links: enable from [Kill_Sounds2 (04C230EC)](#trigger-04c230ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Stop location sound 686 at waypoint 686 (cell 124, 134).
2. Stop location sound 687 at waypoint 687 (cell 94, 129).
3. Stop location sound 688 at waypoint 688 (cell 134, 144).
4. Supply reinforcement team [TEAM_CruiseShip1 (0973710C)](all01umd-teams.md#team-0973710c).
5. Supply reinforcement team [TEAM_CruiseShip2 (0973241C)](all01umd-teams.md#team-0973241c).
6. Supply reinforcement team [TEAM_ScorpPatrol1 (09339C8C)](all01umd-teams.md#team-09339c8c).
7. Supply reinforcement team [TEAM_TugBoat2 (09735B1C)](all01umd-teams.md#team-09735b1c).
8. Supply reinforcement team [ScorpPatrol2 (0796497C)](all01umd-teams.md#team-0796497c).
9. Enable and reset applicable timers for [Start_New_Sounds (04C2263C)](#trigger-04c2263c).
10. Disable [Kill_Sounds3 (04C24A8C)](#trigger-04c24a8c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8680, Events line 9016, Actions line 9352.

<a id="trigger-04c2410c"></a>

### 111. Traffic_Sounds1 - 04C2410C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Attached scope: tag definitions 089BBF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 470 (cell 88, 118).
2. Play sound _Amb_Traffic at waypoint 469 (cell 101, 119).
3. Play sound _Amb_UrbanMurmur2 at waypoint 676 (cell 98, 126).
4. Play sound _Amb_Traffic at waypoint 137 (cell 111, 110).
5. Play sound _Amb_UrbanMurmur1 at waypoint 14 (cell 100, 110).
6. Play sound _Amb_UrbanMurmur2 at waypoint 187 (cell 87, 102).
7. Play sound _Amb_Traffic at waypoint 481 (cell 102, 100).
8. Play sound _Amb_Traffic at waypoint 157 (cell 90, 95).
9. Play sound _Amb_UrbanMurmur2 at waypoint 685 (cell 107, 131).
10. Play sound _Amb_UrbanMurmur1 at waypoint 138 (cell 111, 100).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8681, Events line 9017, Actions line 9353.

<a id="trigger-04c2d1dc"></a>

### 112. Traffic_Sounds2 - 04C2D1DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Attached scope: tag definitions 089BBE6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_Traffic at waypoint 479 (cell 112, 142).
2. Play sound _Amb_UrbanMurmur1 at waypoint 25 (cell 117, 125).
3. Play sound _Amb_UrbanMurmur2 at waypoint 477 (cell 117, 150).
4. Play sound _Amb_UrbanMurmur1 at waypoint 476 (cell 128, 150).
5. Play sound _Amb_UrbanMurmur2 at waypoint 30 (cell 129, 135).
6. Play sound _Amb_Traffic at waypoint 135 (cell 115, 118).
7. Play sound _Amb_Traffic at waypoint 28 (cell 135, 126).
8. Play sound _Amb_UrbanMurmur1 at waypoint 217 (cell 142, 135).
9. Play sound _Amb_UrbanMurmur2 at waypoint 202 (cell 132, 114).
10. Play sound _Amb_Traffic at waypoint 677 (cell 122, 110).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8682, Events line 9018, Actions line 9354.

<a id="trigger-089a6bac"></a>

### 113. Traffic_Sounds3 - 089A6BAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Attached scope: tag definitions 089BBD8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 204 (cell 130, 106).
2. Play sound _Amb_Traffic at waypoint 19 (cell 128, 97).
3. Play sound _Amb_UrbanMurmur2 at waypoint 45 (cell 110, 101).
4. Play sound _Amb_UrbanMurmur1 at waypoint 53 (cell 114, 89).
5. Play sound _Amb_Traffic at waypoint 481 (cell 102, 100).
6. Play sound _Amb_UrbanMurmur2 at waypoint 46 (cell 85, 101).
7. Play sound _Amb_UrbanMurmur1 at waypoint 38 (cell 81, 86).
8. Play sound _Amb_Traffic at waypoint 108 (cell 87, 83).
9. Play sound _Amb_UrbanMurmur2 at waypoint 21 (cell 81, 84).
10. Play sound _Amb_UrbanMurmur1 at waypoint 49 (cell 96, 83).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8683, Events line 9019, Actions line 9355.

<a id="trigger-04bf608c"></a>

### 114. Traffic_Sounds4 - 04BF608C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Attached scope: tag definitions 089BBCAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_Traffic at waypoint 50 (cell 101, 79).
2. Play sound _Amb_UrbanMurmur1 at waypoint 56 (cell 110, 82).
3. Play sound _Amb_UrbanMurmur2 at waypoint 23 (cell 104, 65).
4. Play sound _Amb_UrbanMurmur1 at waypoint 105 (cell 112, 72).
5. Play sound _Amb_Traffic at waypoint 118 (cell 115, 79).
6. Play sound _Amb_UrbanMurmur2 at waypoint 472 (cell 128, 79).
7. Play sound _Amb_UrbanMurmur1 at waypoint 474 (cell 129, 91).
8. Play sound _Amb_Traffic at waypoint 20 (cell 129, 101).
9. Play sound _Amb_Traffic at waypoint 35 (cell 150, 102).
10. Play sound _Amb_UrbanMurmur1 at waypoint 121 (cell 152, 112).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8684, Events line 9020, Actions line 9356.

<a id="trigger-04c0776c"></a>

### 115. Traffic_Sounds5 - 04C0776C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Attached scope: tag definitions 04C2272C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_Traffic at waypoint 205 (cell 152, 125).
2. Play sound _Amb_UrbanMurmur2 at waypoint 86 (cell 167, 114).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8685, Events line 9021, Actions line 9357.

<a id="trigger-089b776c"></a>

### 116. Bird_Sounds1 - 089B776C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Attached scope: tag definitions 089BA29C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsTemperate1 at waypoint 218 (cell 84, 113).
2. Play sound _Amb_BirdsPark at waypoint 687 (cell 94, 129).
3. Play sound _Amb_BirdsTemperate2 at waypoint 678 (cell 112, 135).
4. Play sound _Amb_BirdsMorning at waypoint 686 (cell 124, 134).
5. Play sound _Amb_BirdsTemperate1 at waypoint 133 (cell 113, 149).
6. Play sound _Amb_BirdsTemperate2 at waypoint 688 (cell 134, 144).
7. Play sound _Amb_BirdsPark at waypoint 135 (cell 115, 118).
8. Play sound _Amb_BirdsMorning at waypoint 39 (cell 98, 87).
9. Play sound _Amb_BirdsTemperate1 at waypoint 52 (cell 114, 84).
10. Play sound _Amb_BirdsTemperate2 at waypoint 117 (cell 105, 77).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8686, Events line 9022, Actions line 9358.

<a id="trigger-04bf8f3c"></a>

### 117. Bird_Sounds2 - 04BF8F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Attached scope: tag definitions 089BA1BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsPark at waypoint 104 (cell 114, 68).
2. Play sound _Amb_BirdsTemperate1 at waypoint 473 (cell 130, 81).
3. Play sound _Amb_BirdsTemperate2 at waypoint 219 (cell 139, 93).
4. Play sound _Amb_BirdsMorning at waypoint 203 (cell 131, 106).
5. Play sound _Amb_BirdsTemperate1 at waypoint 220 (cell 141, 120).
6. Play sound _Amb_BirdsPark at waypoint 221 (cell 141, 108).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8687, Events line 9023, Actions line 9359.

<a id="trigger-04c3064c"></a>

### 118. Bird_Sounds3 - 04C3064C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_New_Sounds (04C2263C)](#trigger-04c2263c).

Attached scope: tag definitions 089BA0DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsBeach at waypoint 11 (cell 89, 79).
2. Play sound _Amb_BirdsBeach at waypoint 124 (cell 75, 84).
3. Play sound _Amb_BirdsHarbor at waypoint 223 (cell 94, 63).
4. Play sound _Amb_BirdsHarbor at waypoint 224 (cell 102, 57).
5. Play sound _Amb_BirdsBeach at waypoint 123 (cell 76, 92).
6. Play sound _Amb_BirdsHarbor at waypoint 225 (cell 58, 43).
7. Play sound _Amb_BirdsBeach at waypoint 226 (cell 48, 45).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8688, Events line 9024, Actions line 9360.

<a id="trigger-089ec19c"></a>

### 119. PsychicDead - 089EC19C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Psychic Dominator (YAPPPT) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Cheer (089ECDEC)](#trigger-089ecdec).
2. Enable and reset applicable timers for [WeWin (089EC79C)](#trigger-089ec79c).
3. Disable [PsychicDead (089EC19C)](#trigger-089ec19c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8689, Events line 9025, Actions line 9361.

<a id="trigger-0b8a090c"></a>

### 120. Build_Dom - 0B8A090C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Sell_Psychic (0951879C)](#trigger-0951879c).

Attached scope: tag definitions 0B8A056C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. Enable and reset applicable timers for [New_Dom_Up (0BD650AC)](#trigger-0bd650ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8690, Events line 9026, Actions line 9362.

<a id="trigger-07a8ccbc"></a>

### 121. Connector_Step2 - 07A8CCBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Connector_Gone (07A8917C)](#trigger-07a8917c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 70; location/duration field BS.
2. Apply 100 damage at; main setting 70; location/duration field BS.
3. Apply 100 damage at; main setting 70; location/duration field BS.
4. Apply 100 damage at; main setting 70; location/duration field BS.
5. Apply 100 damage at; main setting 70; location/duration field BS.
6. Enable and reset applicable timers for [Connector_Step3 (07A8D3EC)](#trigger-07a8d3ec).
7. Disable [Connector_Step2 (07A8CCBC)](#trigger-07a8ccbc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8691, Events line 9027, Actions line 9363.

<a id="trigger-0935a09c"></a>

### 122. CenterPiece_Gone02 - 0935A09C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [CenterPiece_Gone01 (0835813C)](#trigger-0835813c).

Incoming activation links: enable from [CenterPiece_Gone01 (0835813C)](#trigger-0835813c).

Attached scope: tag definitions 0835A4DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 145; location/duration field EP.
2. Apply 100 damage at; main setting 145; location/duration field EP.
3. Apply 100 damage at; main setting 145; location/duration field EP.
4. Apply 100 damage at; main setting 145; location/duration field EP.
5. Apply 100 damage at; main setting 59; location/duration field BH.
6. Apply 100 damage at; main setting 59; location/duration field BH.
7. Apply 100 damage at; main setting 59; location/duration field BH.
8. Apply 100 damage at; main setting 59; location/duration field BH.
9. Disable [CenterPiece_Gone02 (0935A09C)](#trigger-0935a09c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8692, Events line 9028, Actions line 9364.

<a id="trigger-08d5d50c"></a>

### 123. Rebuild_Cannon1 - 08D5D50C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Center_On_TimeMachine (0C6F847C)](#trigger-0c6f847c).

Incoming activation links: enable from [Clean_Map (06A4918C)](#trigger-06a4918c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 50 (Cannon1_Gone) is set.

Flag writers in this mission: set local flag 50 (Cannon1_Gone) at [Cannon1_Gone (08D5F24C)](#trigger-08d5f24c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create building GTGCAN at waypoint 139 (cell 80, 105).
2. Disable [Rebuild_Cannon1 (08D5D50C)](#trigger-08d5d50c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8693, Events line 9029, Actions line 9365.

<a id="trigger-08d5d1ec"></a>

### 124. Rebuild_Cannon2 - 08D5D1EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Rebuild_Cannon1 (08D5D50C)](#trigger-08d5d50c).

Incoming activation links: enable from [Clean_Map (06A4918C)](#trigger-06a4918c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 51 (Cannon2_Gone) is set.

Flag writers in this mission: set local flag 51 (Cannon2_Gone) at [Cannon2_Gone (08D5DE6C)](#trigger-08d5de6c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create building GTGCAN at waypoint 140 (cell 83, 105).
2. Disable [Rebuild_Cannon2 (08D5D1EC)](#trigger-08d5d1ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8694, Events line 9030, Actions line 9366.

<a id="trigger-08d5bd9c"></a>

### 125. Rebuild_Cannon3 - 08D5BD9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Rebuild_Cannon2 (08D5D1EC)](#trigger-08d5d1ec).

Incoming activation links: enable from [Clean_Map (06A4918C)](#trigger-06a4918c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 52 (Cannon3_Gone) is set.

Flag writers in this mission: set local flag 52 (Cannon3_Gone) at [Cannon3_Gone (08D5DB4C)](#trigger-08d5db4c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create building GTGCAN at waypoint 98 (cell 77, 93).
2. Disable [Rebuild_Cannon3 (08D5BD9C)](#trigger-08d5bd9c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8695, Events line 9031, Actions line 9367.

<a id="trigger-08d5ba7c"></a>

### 126. Rebuild_Cannon4 - 08D5BA7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Rebuild_Cannon3 (08D5BD9C)](#trigger-08d5bd9c).

Incoming activation links: enable from [Clean_Map (06A4918C)](#trigger-06a4918c).

Attached scope: tag definitions 08A8361C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 53 (Cannon4_Gone) is set.

Flag writers in this mission: set local flag 53 (Cannon4_Gone) at [Cannon4_Gone (08D5D82C)](#trigger-08d5d82c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create building GTGCAN at waypoint 99 (cell 81, 97).
2. Disable [Rebuild_Cannon4 (08D5BA7C)](#trigger-08d5ba7c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8696, Events line 9032, Actions line 9368.

<a id="trigger-0790df3c"></a>

### 127. Kirov_Reporting - 0790DF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Really_Play_Movie (05E9106C)](#trigger-05e9106c).

Attached scope: tag definitions 0790D37C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since the trigger timer was initialized/reset.
2. No instances of Apocalypse (APOC) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Play sound KirovCreated.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8697, Events line 9033, Actions line 9369.

<a id="trigger-08a6340c"></a>

### 128. Make_People2 - 08A6340C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_Alcatraz_Men (0692C4AC)](#trigger-0692c4ac).

Incoming activation links: enable from [Make_People (06A1D17C)](#trigger-06a1d17c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Calm_Civ2 (068FFC5C)](all01umd-teams.md#team-068ffc5c) at waypoint 44 (cell 111, 99).
2. Supply reinforcement team [TEAM_Calm_Civ2 (068FFC5C)](all01umd-teams.md#team-068ffc5c) at waypoint 56 (cell 110, 82).
3. Supply reinforcement team [SovGar_BV (0788E0EC)](all01umd-teams.md#team-0788e0ec).
4. Supply reinforcement team [SovGarrision_BW (0788F21C)](all01umd-teams.md#team-0788f21c).
5. Supply reinforcement team [SovGarrision_BX (0788BC4C)](all01umd-teams.md#team-0788bc4c).
6. Supply reinforcement team [SovGar_CK (077D3BAC)](all01umd-teams.md#team-077d3bac).
7. Supply reinforcement team [SovGarr_CL (077D3A7C)](all01umd-teams.md#team-077d3a7c).
8. Supply reinforcement team [SovGarr_CM (077D394C)](all01umd-teams.md#team-077d394c).
9. Enable and reset applicable timers for [Make_Alcatraz_Men (0692C4AC)](#trigger-0692c4ac).
10. Disable [Make_People2 (08A6340C)](#trigger-08a6340c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8698, Events line 9034, Actions line 9370.

<a id="trigger-04c230ec"></a>

### 129. Kill_Sounds2 - 04C230EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Kill_Sounds1 (04C23C0C)](#trigger-04c23c0c).

Incoming activation links: enable from [Kill_Sounds1 (04C23C0C)](#trigger-04c23c0c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Stop location sound 680 at waypoint 680 (cell 134, 110).
2. Stop location sound 28 at waypoint 28 (cell 135, 126).
3. Stop location sound 32 at waypoint 32 (cell 138, 101).
4. Stop location sound 681 at waypoint 681 (cell 153, 114).
5. Stop location sound 682 at waypoint 682 (cell 150, 125).
6. Stop location sound 683 at waypoint 683 (cell 114, 87).
7. Stop location sound 684 at waypoint 684 (cell 84, 108).
8. Stop location sound 685 at waypoint 685 (cell 107, 131).
9. Enable and reset applicable timers for [Kill_Sounds3 (04C24A8C)](#trigger-04c24a8c).
10. Disable [Kill_Sounds2 (04C230EC)](#trigger-04c230ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8699, Events line 9035, Actions line 9371.

<a id="trigger-089ecdec"></a>

### 130. Cheer - 089ECDEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PsychicDead (089EC19C)](#trigger-089ec19c); enable from [Check_New_Dom (0BD6117C)](#trigger-0bd6117c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8700, Events line 9036, Actions line 9372.

<a id="trigger-089ec79c"></a>

### 131. WeWin - 089EC79C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Cheer (089ECDEC)](#trigger-089ecdec).

Incoming activation links: enable from [PsychicDead (089EC19C)](#trigger-089ec19c); enable from [Check_New_Dom (0BD6117C)](#trigger-0bd6117c).

Attached scope: tag definitions 089EC88C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner.
2. Disable [WeWin (089EC79C)](#trigger-089ec79c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8701, Events line 9037, Actions line 9373.

<a id="trigger-0bd650ac"></a>

### 132. New_Dom_Up - 0BD650AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Build_Dom (0B8A090C)](#trigger-0b8a090c).

Attached scope: tag definitions 0BD630BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Check_New_Dom (0BD6117C)](#trigger-0bd6117c).
2. Enable and reset applicable timers for [Kill_ConYard (045CEF3C)](#trigger-045cef3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8702, Events line 9038, Actions line 9374.

<a id="trigger-07a8d3ec"></a>

### 133. Connector_Step3 - 07A8D3EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Connector_Step2 (07A8CCBC)](#trigger-07a8ccbc).

Attached scope: tag definitions 07A8839C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 59; location/duration field BH.
2. Apply 100 damage at; main setting 59; location/duration field BH.
3. Apply 100 damage at; main setting 59; location/duration field BH.
4. Disable [Connector_Step3 (07A8D3EC)](#trigger-07a8d3ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8703, Events line 9039, Actions line 9375.

<a id="trigger-0692c4ac"></a>

### 134. Make_Alcatraz_Men - 0692C4AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Clean_Map (06A4918C)](#trigger-06a4918c).

Incoming activation links: enable from [Make_People2 (08A6340C)](#trigger-08a6340c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [SovGarr_CN (077D381C)](all01umd-teams.md#team-077d381c).
2. Supply reinforcement team [SovGar_CO (077D36EC)](all01umd-teams.md#team-077d36ec).
3. Supply reinforcement team [Alcatraz_Patrol (098A9B5C)](all01umd-teams.md#team-098a9b5c).
4. Perform no action.
5. Perform no action.
6. Perform no action.
7. Perform no action.
8. Perform no action.
9. Enable and reset applicable timers for [Clean_Map (06A4918C)](#trigger-06a4918c).
10. Disable [Make_Alcatraz_Men (0692C4AC)](#trigger-0692c4ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8704, Events line 9040, Actions line 9376.

<a id="trigger-04c23c0c"></a>

### 135. Kill_Sounds1 - 04C23C0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_People2 (08A6340C)](#trigger-08a6340c).

Incoming activation links: enable from [Clean_Map (06A4918C)](#trigger-06a4918c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Stop location sound 14 at waypoint 14 (cell 100, 110).
2. Stop location sound 676 at waypoint 676 (cell 98, 126).
3. Stop location sound 677 at waypoint 677 (cell 122, 110).
4. Stop location sound 40 at waypoint 40 (cell 92, 93).
5. Stop location sound 21 at waypoint 21 (cell 81, 84).
6. Stop location sound 678 at waypoint 678 (cell 112, 135).
7. Stop location sound 679 at waypoint 679 (cell 109, 77).
8. Stop location sound 474 at waypoint 474 (cell 129, 91).
9. Enable and reset applicable timers for [Kill_Sounds2 (04C230EC)](#trigger-04c230ec).
10. Disable [Kill_Sounds1 (04C23C0C)](#trigger-04c23c0c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8705, Events line 9041, Actions line 9377.

<a id="trigger-0bd6117c"></a>

### 136. Check_New_Dom - 0BD6117C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [New_Dom_Up (0BD650AC)](#trigger-0bd650ac).

Attached scope: tag definitions 0BD6008C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Psychic Dominator (YAPPPT) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Cheer (089ECDEC)](#trigger-089ecdec).
2. Enable and reset applicable timers for [WeWin (089EC79C)](#trigger-089ec79c).
3. Disable [Check_New_Dom (0BD6117C)](#trigger-0bd6117c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8706, Events line 9042, Actions line 9378.

<a id="trigger-045cef3c"></a>

### 137. Kill_ConYard - 045CEF3C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [New_Dom_Up (0BD650AC)](#trigger-0bd650ac).

Attached scope: Yuri Construction Yard (YACNST), owner Confederation, cell (103, 158), tag 045CE63C, persistence mode 0.

**Wait for the recorded events:**

1. Building exists: type index 355 (global list position: Yuri´s Command Center (YACOMD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 16 (country/type BRIDGE COUNTRY; placed owner BridgeHouse).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8707, Events line 9043, Actions line 9379.

<a id="trigger-06a4918c"></a>

### 138. Clean_Map - 06A4918C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Make_Civ_Cars2 (0692A65C)](#trigger-0692a65c).

Incoming activation links: enable from [Make_Alcatraz_Men (0692C4AC)](#trigger-0692c4ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Clear all smudges; main setting 0.
2. Create building GAPOWR at waypoint 302 (cell 92, 95).
3. Create building GAPOWR at waypoint 303 (cell 92, 97).
4. Enable and reset applicable timers for [Kill_Sounds1 (04C23C0C)](#trigger-04c23c0c).
5. Enable and reset applicable timers for [Rebuild_Cannon1 (08D5D50C)](#trigger-08d5d50c).
6. Enable and reset applicable timers for [Rebuild_Cannon2 (08D5D1EC)](#trigger-08d5d1ec).
7. Enable and reset applicable timers for [Rebuild_Cannon3 (08D5BD9C)](#trigger-08d5bd9c).
8. Enable and reset applicable timers for [Rebuild_Cannon4 (08D5BA7C)](#trigger-08d5ba7c).
9. Disable [Clean_Map (06A4918C)](#trigger-06a4918c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8708, Events line 9044, Actions line 9380.

<a id="trigger-08a71f3c"></a>

### 139. Ping_PP_One - 08A71F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec).

Attached scope: tag definitions 08A842AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 47 (Power_Online) is clear.

Flag writers in this mission: set local flag 47 (Power_Online) at [Power_Online (0691357C)](#trigger-0691357c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play sound BeaconPlaced.
2. Create radar-event marker type 11 at waypoint 87 (cell 120, 148).
3. Disable [Ping_PP_One (08A71F3C)](#trigger-08a71f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8709, Events line 9045, Actions line 9381.

<a id="trigger-0b7d315c"></a>

### 140. Start_Hover_One - 0B7D315C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 081343CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create_Hover_One (0B7D4BCC)](#trigger-0b7d4bcc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8710, Events line 9046, Actions line 9382.

<a id="trigger-080e410c"></a>

### 141. Uncover_Stuff - 080E410C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 080E5B9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal the zone associated with waypoint 495 (cell 57, 75).
2. Reveal terrain around waypoint 496 (cell 53, 69).
3. Reveal terrain around waypoint 141 (cell 133, 130).
4. Reveal terrain around waypoint 60 (cell 67, 101).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8711, Events line 9047, Actions line 9383.

<a id="trigger-043808cc"></a>

### 142. Return_Cannons1 - 043808CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [Return_Cannons2 (043772BC)](#trigger-043772bc).
3. Disable [Return_Cannons1 (043808CC)](#trigger-043808cc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8712, Events line 9048, Actions line 9384.

<a id="trigger-043772bc"></a>

### 143. Return_Cannons2 - 043772BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Return_Cannons1 (043808CC)](#trigger-043808cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [Return_Cannons3 (04378F3C)](#trigger-04378f3c).
3. Disable [Return_Cannons2 (043772BC)](#trigger-043772bc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8713, Events line 9049, Actions line 9385.

<a id="trigger-04378f3c"></a>

### 144. Return_Cannons3 - 04378F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Return_Cannons2 (043772BC)](#trigger-043772bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [Return_Cannons4 (0438076C)](#trigger-0438076c).
3. Disable [Return_Cannons3 (04378F3C)](#trigger-04378f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8714, Events line 9050, Actions line 9386.

<a id="trigger-0438076c"></a>

### 145. Return_Cannons4 - 0438076C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Return_Cannons3 (04378F3C)](#trigger-04378f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Disable [Return_Cannons4 (0438076C)](#trigger-0438076c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8715, Events line 9051, Actions line 9387.

<a id="trigger-0b03a5bc"></a>

### 146. Deploy_Start_GI - 0B03A5BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B03A39C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Starting_GI (0B03E84C)](all01umd-teams.md#team-0b03e84c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8716, Events line 9052, Actions line 9388.

<a id="trigger-068f288c"></a>

### 147. Deploy_Start_GGI - 068F288C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 068F232C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Starting_GGI (08B03A4C)](all01umd-teams.md#team-08b03a4c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8717, Events line 9053, Actions line 9389.

<a id="trigger-0b024e1c"></a>

### 148. Start_Briefing - 0B024E1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B0247BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Camera_Player_Base (0B0246CC)](#trigger-0b0246cc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8718, Events line 9054, Actions line 9390.

<a id="trigger-0b0246cc"></a>

### 149. Camera_Player_Base - 0B0246CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_Briefing (0B024E1C)](#trigger-0b024e1c); enable from [Camera_Harriers (0C077BCC)](#trigger-0c077bcc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 17 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 14 (cell 100, 110) with speed setting 3.
2. Play in-game movie 2.
3. Enable and reset applicable timers for [Camera_Base02 (0885DE3C)](#trigger-0885de3c).
4. Remove instances of the team organization (not automatically its surviving objects) [TEAM_Starting_GGI (08B03A4C)](all01umd-teams.md#team-08b03a4c).
5. Enable and reset applicable timers for [Load_Engineer (06C7108C)](#trigger-06c7108c).
6. Disable [Camera_Player_Base (0B0246CC)](#trigger-0b0246cc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8719, Events line 9055, Actions line 9391.

<a id="trigger-0885de3c"></a>

### 150. Camera_Base02 - 0885DE3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Camera_Player_Base (0B0246CC)](#trigger-0b0246cc).

Incoming activation links: enable from [Camera_Player_Base (0B0246CC)](#trigger-0b0246cc).

Attached scope: tag definitions 0B02421C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification A01_p01.
2. Enable and reset applicable timers for [Camera_Base_to_TM (0B025F3C)](#trigger-0b025f3c).
3. Disable [Camera_Base02 (0885DE3C)](#trigger-0885de3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8720, Events line 9056, Actions line 9392.

<a id="trigger-06c7108c"></a>

### 151. Load_Engineer - 06C7108C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_Player_Base (0B0246CC)](#trigger-0b0246cc).

Attached scope: tag definitions 06C728DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_Start_Engineer (0D3FA93C)](all01umd-teams.md#team-0d3fa93c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8721, Events line 9057, Actions line 9393.

<a id="trigger-08a77a5c"></a>

### 152. Camera_Start - 08A77A5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A7B6AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 14 (cell 100, 110).
2. Disable player input.
3. Play voice notification EVA_EstablishBattlefieldControl.
4. Center Base Cell Set; main setting 15; location/duration field P.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8722, Events line 9058, Actions line 9394.

<a id="trigger-0437e7ec"></a>

### 153. Garrison_UT - 0437E7EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0437E5CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_UT_Garrison (043998EC)](all01umd-teams.md#team-043998ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8723, Events line 9059, Actions line 9395.

<a id="trigger-0b12eafc"></a>

### 154. Start_AA_AB_Patrol - 0B12EAFC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B0B393C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_PP1_Group_PatrolA (0C8E7A8C)](all01umd-teams.md#team-0c8e7a8c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8724, Events line 9060, Actions line 9396.

<a id="trigger-0437c23c"></a>

### 155. Garrison_ZAI - 0437C23C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0437FB2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_ZAI_Garrison (0437F1EC)](all01umd-teams.md#team-0437f1ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8725, Events line 9061, Actions line 9397.

<a id="trigger-089cf54c"></a>

### 156. Garrison_AJAK - 089CF54C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089AD81C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_AJ_AK_Garrison (089CE49C)](all01umd-teams.md#team-089ce49c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8726, Events line 9062, Actions line 9398.

<a id="trigger-08a0367c"></a>

### 157. Start_AF_AH_Patrol - 08A0367C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A01EEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_AF_AG_Patrol (08A006AC)](all01umd-teams.md#team-08a006ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8727, Events line 9063, Actions line 9399.

<a id="trigger-043bb08c"></a>

### 158. Change_Einstein - 043BB08C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043BCA5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Disable [Change_Einstein (043BB08C)](#trigger-043bb08c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8728, Events line 9064, Actions line 9400.

<a id="trigger-043a703c"></a>

### 159. Change_House_PP1 - 043A703C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Enable and reset applicable timers for [PP1_Entered (108EA04C)](#trigger-108ea04c).
3. Enable and reset applicable timers for [PP1_Destroyed (108ECA9C)](#trigger-108eca9c).
4. Disable [Change_House_PP1 (043A703C)](#trigger-043a703c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8729, Events line 9065, Actions line 9401.

<a id="trigger-108ea04c"></a>

### 160. PP1_Entered - 108EA04C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change_House_PP1 (043A703C)](#trigger-043a703c).

Incoming activation links: enable from [Change_House_PP1 (043A703C)](#trigger-043a703c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 31 (Lost_Tech01_USA).
2. Enable and reset applicable timers for [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c).
3. Enable and reset applicable timers for [PP1_Group_Done_FalseA (0BADE25C)](#trigger-0bade25c).
4. Enable and reset applicable timers for [PP1_Group_Done_FalseB (0C18404C)](#trigger-0c18404c).
5. Enable and reset applicable timers for [Good_Job_1 (0C9733CC)](#trigger-0c9733cc).
6. Set local flag 6 (PP1_Entered).
7. Disable [PP1_Entered (108EA04C)](#trigger-108ea04c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8730, Events line 9066, Actions line 9402.

<a id="trigger-108eca9c"></a>

### 161. PP1_Destroyed - 108ECA9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP1_Entered (108EA04C)](#trigger-108ea04c).

Incoming activation links: enable from [Change_House_PP1 (043A703C)](#trigger-043a703c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR01 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Play voice notification EVA_CriticalStrucureLost.
2. Set local flag 18 (PP1_Gone).
3. Enable and reset applicable timers for [Losing_Power_1 (0617F12C)](#trigger-0617f12c).
4. Enable and reset applicable timers for [Lost_Power_1 (0617A39C)](#trigger-0617a39c).
5. Enable and reset applicable timers for [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c).
6. Enable and reset applicable timers for [PP1_Group_Done_FalseA (0BADE25C)](#trigger-0bade25c).
7. Enable and reset applicable timers for [PP1_Group_Done_FalseB (0C18404C)](#trigger-0c18404c).
8. Set local flag 6 (PP1_Entered).
9. Disable [PP1_Entered (108EA04C)](#trigger-108ea04c).
10. Disable [PP1_Destroyed (108ECA9C)](#trigger-108eca9c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8731, Events line 9067, Actions line 9403.

<a id="trigger-0bade68c"></a>

### 162. PP1_Group_Done_True - 0BADE68C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PP1_Entered (108EA04C)](#trigger-108ea04c); enable from [PP1_Destroyed (108ECA9C)](#trigger-108eca9c); enable from [PP2_Entered (095AE59C)](#trigger-095ae59c); enable from [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 7 (PP2_Entered) is set.
2. local flag 6 (PP1_Entered) is set.

Flag writers in this mission: set local flag 7 (PP2_Entered) at [PP2_Entered (095AE59C)](#trigger-095ae59c); set local flag 7 (PP2_Entered) at [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac); set local flag 6 (PP1_Entered) at [PP1_Entered (108EA04C)](#trigger-108ea04c); set local flag 6 (PP1_Entered) at [PP1_Destroyed (108ECA9C)](#trigger-108eca9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP1_Group_Done_FalseA (0BADE25C)](#trigger-0bade25c).
2. Disable [PP1_Group_Done_FalseB (0C18404C)](#trigger-0c18404c).
3. Enable and reset applicable timers for [Check_PP2_True (0BFCC7DC)](#trigger-0bfcc7dc).
4. Enable and reset applicable timers for [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec).
5. Disable [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8732, Events line 9068, Actions line 9404.

<a id="trigger-0bade25c"></a>

### 163. PP1_Group_Done_FalseA - 0BADE25C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c).

Incoming activation links: enable from [PP1_Entered (108EA04C)](#trigger-108ea04c); enable from [PP1_Destroyed (108ECA9C)](#trigger-108eca9c); enable from [PP2_Entered (095AE59C)](#trigger-095ae59c); enable from [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 7 (PP2_Entered) is clear.
2. local flag 6 (PP1_Entered) is set.

Flag writers in this mission: set local flag 7 (PP2_Entered) at [PP2_Entered (095AE59C)](#trigger-095ae59c); set local flag 7 (PP2_Entered) at [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac); set local flag 6 (PP1_Entered) at [PP1_Entered (108EA04C)](#trigger-108ea04c); set local flag 6 (PP1_Entered) at [PP1_Destroyed (108ECA9C)](#trigger-108eca9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c).
2. Disable [PP1_Group_Done_FalseB (0C18404C)](#trigger-0c18404c).
3. Disable [PP1_Group_Done_FalseA (0BADE25C)](#trigger-0bade25c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8733, Events line 9069, Actions line 9405.

<a id="trigger-0c18404c"></a>

### 164. PP1_Group_Done_FalseB - 0C18404C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP1_Group_Done_FalseA (0BADE25C)](#trigger-0bade25c).

Incoming activation links: enable from [PP1_Entered (108EA04C)](#trigger-108ea04c); enable from [PP1_Destroyed (108ECA9C)](#trigger-108eca9c); enable from [PP2_Entered (095AE59C)](#trigger-095ae59c); enable from [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac).

Attached scope: tag definitions 0BADE34C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (PP1_Entered) is clear.
2. local flag 7 (PP2_Entered) is set.

Flag writers in this mission: set local flag 6 (PP1_Entered) at [PP1_Entered (108EA04C)](#trigger-108ea04c); set local flag 6 (PP1_Entered) at [PP1_Destroyed (108ECA9C)](#trigger-108eca9c); set local flag 7 (PP2_Entered) at [PP2_Entered (095AE59C)](#trigger-095ae59c); set local flag 7 (PP2_Entered) at [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c).
2. Disable [PP1_Group_Done_FalseA (0BADE25C)](#trigger-0bade25c).
3. Disable [PP1_Group_Done_FalseB (0C18404C)](#trigger-0c18404c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8734, Events line 9070, Actions line 9406.

<a id="trigger-0c9733cc"></a>

### 165. Good_Job_1 - 0C9733CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PP1_Entered (108EA04C)](#trigger-108ea04c); enable from [PP2_Entered (095AE59C)](#trigger-095ae59c); enable from [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); enable from [PP4_Entered (0BAAD22C)](#trigger-0baad22c); enable from [PP5_Entered (0BAAE54C)](#trigger-0baae54c); enable from [PP6_Entered (0BAAE37C)](#trigger-0baae37c); enable from [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); enable from [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c).

Attached scope: tag definitions 0C9779FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA1_EvaMorePower.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8735, Events line 9071, Actions line 9407.

<a id="trigger-0617f12c"></a>

### 166. Losing_Power_1 - 0617F12C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PP1_Destroyed (108ECA9C)](#trigger-108eca9c); enable from [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac); enable from [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc); enable from [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c); enable from [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc); enable from [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc); enable from [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c); enable from [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 26 (Lost_1_Power) is clear.

Flag writers in this mission: set local flag 26 (Lost_1_Power) at [Losing_Power_1 (0617F12C)](#trigger-0617f12c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Lost_Power_1 (0617A39C)](#trigger-0617a39c).
2. Set local flag 26 (Lost_1_Power).
3. Disable [Losing_Power_1 (0617F12C)](#trigger-0617f12c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8736, Events line 9072, Actions line 9408.

<a id="trigger-0617a39c"></a>

### 167. Lost_Power_1 - 0617A39C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Losing_Power_4 (0617A79C)](#trigger-0617a79c).

Incoming activation links: enable from [PP1_Destroyed (108ECA9C)](#trigger-108eca9c); enable from [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac); enable from [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc); enable from [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c); enable from [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc); enable from [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc); enable from [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c); enable from [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 26 (Lost_1_Power) is set.

Flag writers in this mission: set local flag 26 (Lost_1_Power) at [Losing_Power_1 (0617F12C)](#trigger-0617f12c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Losing_Power_1 (0617F12C)](#trigger-0617f12c).
2. Enable and reset applicable timers for [Losing_Power_2 (0617F7AC)](#trigger-0617f7ac).
3. Enable and reset applicable timers for [Lost_Power_2 (06187F3C)](#trigger-06187f3c).
4. Disable [Lost_Power_1 (0617A39C)](#trigger-0617a39c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8737, Events line 9073, Actions line 9409.

<a id="trigger-0bfcc7dc"></a>

### 168. Check_PP2_True - 0BFCC7DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_Group_Done_FalseB (0BAC19BC)](#trigger-0bac19bc).

Incoming activation links: enable from [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c); enable from [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac); enable from [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c); enable from [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 15 (PP2_Group_Revealed) is set.

Flag writers in this mission: set local flag 15 (PP2_Group_Revealed) at [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec).
2. Enable and reset applicable timers for [Check_PP3_True (0BFCC5FC)](#trigger-0bfcc5fc).
3. Enable and reset applicable timers for [Check_PP3_False (0BFCC50C)](#trigger-0bfcc50c).
4. Disable [Check_PP2_True (0BFCC7DC)](#trigger-0bfcc7dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8738, Events line 9074, Actions line 9410.

<a id="trigger-0bfcc6ec"></a>

### 169. Check_PP2_False - 0BFCC6EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PP2_True (0BFCC7DC)](#trigger-0bfcc7dc).

Incoming activation links: enable from [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c); enable from [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac); enable from [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c); enable from [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 15 (PP2_Group_Revealed) is clear.

Flag writers in this mission: set local flag 15 (PP2_Group_Revealed) at [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PP2_True (0BFCC7DC)](#trigger-0bfcc7dc).
2. Reveal terrain around waypoint 87 (cell 120, 148).
3. Enable and reset applicable timers for [Ping_PP_One (08A71F3C)](#trigger-08a71f3c).
4. Set local flag 15 (PP2_Group_Revealed).
5. Disable [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8739, Events line 9075, Actions line 9411.

<a id="trigger-0617a79c"></a>

### 170. Losing_Power_4 - 0617A79C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Losing_Power_3 (0617AB0C)](#trigger-0617ab0c).

Incoming activation links: enable from [Lost_Power_3 (06187C1C)](#trigger-06187c1c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 29 (Lost_4_Power) is clear.
2. local flag 28 (Lost_3_Power) is set.
3. local flag 27 (Lost_2_Power) is set.
4. local flag 26 (Lost_1_Power) is set.

Flag writers in this mission: set local flag 29 (Lost_4_Power) at [Losing_Power_4 (0617A79C)](#trigger-0617a79c); set local flag 28 (Lost_3_Power) at [Losing_Power_3 (0617AB0C)](#trigger-0617ab0c); set local flag 27 (Lost_2_Power) at [Losing_Power_2 (0617F7AC)](#trigger-0617f7ac); set local flag 26 (Lost_1_Power) at [Losing_Power_1 (0617F12C)](#trigger-0617f12c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Lost_Power_4 (06187A9C)](#trigger-06187a9c).
2. Set local flag 29 (Lost_4_Power).
3. Disable [Losing_Power_4 (0617A79C)](#trigger-0617a79c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8740, Events line 9076, Actions line 9412.

<a id="trigger-0617f7ac"></a>

### 171. Losing_Power_2 - 0617F7AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Losing_Power_1 (0617F12C)](#trigger-0617f12c).

Incoming activation links: enable from [Lost_Power_1 (0617A39C)](#trigger-0617a39c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 27 (Lost_2_Power) is clear.
2. local flag 26 (Lost_1_Power) is set.

Flag writers in this mission: set local flag 27 (Lost_2_Power) at [Losing_Power_2 (0617F7AC)](#trigger-0617f7ac); set local flag 26 (Lost_1_Power) at [Losing_Power_1 (0617F12C)](#trigger-0617f12c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Lost_Power_2 (06187F3C)](#trigger-06187f3c).
2. Set local flag 27 (Lost_2_Power).
3. Disable [Losing_Power_2 (0617F7AC)](#trigger-0617f7ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8741, Events line 9077, Actions line 9413.

<a id="trigger-06187f3c"></a>

### 172. Lost_Power_2 - 06187F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Lost_Power_1 (0617A39C)](#trigger-0617a39c).

Incoming activation links: enable from [Lost_Power_1 (0617A39C)](#trigger-0617a39c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 27 (Lost_2_Power) is set.

Flag writers in this mission: set local flag 27 (Lost_2_Power) at [Losing_Power_2 (0617F7AC)](#trigger-0617f7ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Losing_Power_2 (0617F7AC)](#trigger-0617f7ac).
2. Enable and reset applicable timers for [Losing_Power_3 (0617AB0C)](#trigger-0617ab0c).
3. Enable and reset applicable timers for [Lost_Power_3 (06187C1C)](#trigger-06187c1c).
4. Disable [Lost_Power_2 (06187F3C)](#trigger-06187f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8742, Events line 9078, Actions line 9414.

<a id="trigger-0bac19bc"></a>

### 173. PP4_Group_Done_FalseB - 0BAC19BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_Group_Done_FalseA (0BAC1AAC)](#trigger-0bac1aac).

Incoming activation links: enable from [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); enable from [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c); enable from [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c); enable from [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 13 (PP8_Entered) is set.
2. local flag 12 (PP7_Entered) is clear.

Flag writers in this mission: set local flag 13 (PP8_Entered) at [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c); set local flag 13 (PP8_Entered) at [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c); set local flag 12 (PP7_Entered) at [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); set local flag 12 (PP7_Entered) at [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac).
2. Disable [PP4_Group_Done_FalseA (0BAC1AAC)](#trigger-0bac1aac).
3. Disable [PP4_Group_Done_FalseB (0BAC19BC)](#trigger-0bac19bc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8743, Events line 9079, Actions line 9415.

<a id="trigger-0bfcc5fc"></a>

### 174. Check_PP3_True - 0BFCC5FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec).

Incoming activation links: enable from [Check_PP2_True (0BFCC7DC)](#trigger-0bfcc7dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 16 (PP3_Group_Revealed) is set.

Flag writers in this mission: set local flag 16 (PP3_Group_Revealed) at [Check_PP3_False (0BFCC50C)](#trigger-0bfcc50c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PP3_False (0BFCC50C)](#trigger-0bfcc50c).
2. Enable and reset applicable timers for [Check_PP4_True (0BFE577C)](#trigger-0bfe577c).
3. Enable and reset applicable timers for [Check_PP4_False (0BFE471C)](#trigger-0bfe471c).
4. Disable [Check_PP3_True (0BFCC5FC)](#trigger-0bfcc5fc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8744, Events line 9080, Actions line 9416.

<a id="trigger-0bfcc50c"></a>

### 175. Check_PP3_False - 0BFCC50C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PP3_True (0BFCC5FC)](#trigger-0bfcc5fc).

Incoming activation links: enable from [Check_PP2_True (0BFCC7DC)](#trigger-0bfcc7dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 16 (PP3_Group_Revealed) is clear.

Flag writers in this mission: set local flag 16 (PP3_Group_Revealed) at [Check_PP3_False (0BFCC50C)](#trigger-0bfcc50c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PP3_True (0BFCC5FC)](#trigger-0bfcc5fc).
2. Reveal terrain around waypoint 43 (cell 154, 107).
3. Enable and reset applicable timers for [Ping_PP_Four (08B4D3BC)](#trigger-08b4d3bc).
4. Set local flag 16 (PP3_Group_Revealed).
5. Disable [Check_PP3_False (0BFCC50C)](#trigger-0bfcc50c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8745, Events line 9081, Actions line 9417.

<a id="trigger-0617ab0c"></a>

### 176. Losing_Power_3 - 0617AB0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Losing_Power_2 (0617F7AC)](#trigger-0617f7ac).

Incoming activation links: enable from [Lost_Power_2 (06187F3C)](#trigger-06187f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 28 (Lost_3_Power) is clear.
2. local flag 27 (Lost_2_Power) is set.
3. local flag 26 (Lost_1_Power) is set.

Flag writers in this mission: set local flag 28 (Lost_3_Power) at [Losing_Power_3 (0617AB0C)](#trigger-0617ab0c); set local flag 27 (Lost_2_Power) at [Losing_Power_2 (0617F7AC)](#trigger-0617f7ac); set local flag 26 (Lost_1_Power) at [Losing_Power_1 (0617F12C)](#trigger-0617f12c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Lost_Power_3 (06187C1C)](#trigger-06187c1c).
2. Set local flag 28 (Lost_3_Power).
3. Disable [Losing_Power_3 (0617AB0C)](#trigger-0617ab0c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8746, Events line 9082, Actions line 9418.

<a id="trigger-06187a9c"></a>

### 177. Lost_Power_4 - 06187A9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Lost_Power_3 (06187C1C)](#trigger-06187c1c).

Incoming activation links: enable from [Lost_Power_3 (06187C1C)](#trigger-06187c1c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 29 (Lost_4_Power) is set.

Flag writers in this mission: set local flag 29 (Lost_4_Power) at [Losing_Power_4 (0617A79C)](#trigger-0617a79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Losing_Power_4 (0617A79C)](#trigger-0617a79c).
2. Enable and reset applicable timers for [Losing_Power_5 (06179F3C)](#trigger-06179f3c).
3. Enable and reset applicable timers for [Lost_Power_5 (06179A4C)](#trigger-06179a4c).
4. Disable [Lost_Power_4 (06187A9C)](#trigger-06187a9c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8747, Events line 9083, Actions line 9419.

<a id="trigger-06187c1c"></a>

### 178. Lost_Power_3 - 06187C1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Lost_Power_2 (06187F3C)](#trigger-06187f3c).

Incoming activation links: enable from [Lost_Power_2 (06187F3C)](#trigger-06187f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 28 (Lost_3_Power) is set.

Flag writers in this mission: set local flag 28 (Lost_3_Power) at [Losing_Power_3 (0617AB0C)](#trigger-0617ab0c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Losing_Power_3 (0617AB0C)](#trigger-0617ab0c).
2. Enable and reset applicable timers for [Losing_Power_4 (0617A79C)](#trigger-0617a79c).
3. Enable and reset applicable timers for [Lost_Power_4 (06187A9C)](#trigger-06187a9c).
4. Disable [Lost_Power_3 (06187C1C)](#trigger-06187c1c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8748, Events line 9084, Actions line 9420.

<a id="trigger-0bac1aac"></a>

### 179. PP4_Group_Done_FalseA - 0BAC1AAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac).

Incoming activation links: enable from [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); enable from [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c); enable from [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c); enable from [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 12 (PP7_Entered) is set.
2. local flag 13 (PP8_Entered) is clear.

Flag writers in this mission: set local flag 12 (PP7_Entered) at [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); set local flag 12 (PP7_Entered) at [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c); set local flag 13 (PP8_Entered) at [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c); set local flag 13 (PP8_Entered) at [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac).
2. Disable [PP4_Group_Done_FalseB (0BAC19BC)](#trigger-0bac19bc).
3. Disable [PP4_Group_Done_FalseA (0BAC1AAC)](#trigger-0bac1aac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8749, Events line 9085, Actions line 9421.

<a id="trigger-0bfcdaac"></a>

### 180. PP4_Group_Done_True - 0BFCDAAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); enable from [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c); enable from [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c); enable from [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 12 (PP7_Entered) is set.
2. local flag 13 (PP8_Entered) is set.

Flag writers in this mission: set local flag 12 (PP7_Entered) at [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); set local flag 12 (PP7_Entered) at [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c); set local flag 13 (PP8_Entered) at [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c); set local flag 13 (PP8_Entered) at [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP4_Group_Done_FalseA (0BAC1AAC)](#trigger-0bac1aac).
2. Disable [PP4_Group_Done_FalseB (0BAC19BC)](#trigger-0bac19bc).
3. Enable and reset applicable timers for [Check_PP2_True (0BFCC7DC)](#trigger-0bfcc7dc).
4. Enable and reset applicable timers for [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec).
5. Disable [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8750, Events line 9086, Actions line 9422.

<a id="trigger-0bfe577c"></a>

### 181. Check_PP4_True - 0BFE577C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PP3_False (0BFCC50C)](#trigger-0bfcc50c).

Incoming activation links: enable from [Check_PP3_True (0BFCC5FC)](#trigger-0bfcc5fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 17 (PP4_Group_Revealed) is set.

Flag writers in this mission: set local flag 17 (PP4_Group_Revealed) at [Check_PP4_False (0BFE471C)](#trigger-0bfe471c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PP4_False (0BFE471C)](#trigger-0bfe471c).
2. Disable [Check_PP4_True (0BFE577C)](#trigger-0bfe577c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8751, Events line 9087, Actions line 9423.

<a id="trigger-0bfe471c"></a>

### 182. Check_PP4_False - 0BFE471C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Check_PP4_True (0BFE577C)](#trigger-0bfe577c).

Incoming activation links: enable from [Check_PP3_True (0BFCC5FC)](#trigger-0bfcc5fc).

Attached scope: tag definitions 0BFCD9CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 17 (PP4_Group_Revealed) is clear.

Flag writers in this mission: set local flag 17 (PP4_Group_Revealed) at [Check_PP4_False (0BFE471C)](#trigger-0bfe471c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Check_PP4_True (0BFE577C)](#trigger-0bfe577c).
2. Reveal terrain around waypoint 18 (cell 126, 83).
3. Enable and reset applicable timers for [Ping_PP_Three (089D668C)](#trigger-089d668c).
4. Set local flag 17 (PP4_Group_Revealed).
5. Disable [Check_PP4_False (0BFE471C)](#trigger-0bfe471c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8752, Events line 9088, Actions line 9424.

<a id="trigger-06179f3c"></a>

### 183. Losing_Power_5 - 06179F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Lost_Power_4 (06187A9C)](#trigger-06187a9c).

Incoming activation links: enable from [Lost_Power_4 (06187A9C)](#trigger-06187a9c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 30 (Lost_5_Power) is clear.
2. local flag 29 (Lost_4_Power) is set.

Flag writers in this mission: set local flag 30 (Lost_5_Power) at [Losing_Power_5 (06179F3C)](#trigger-06179f3c); set local flag 29 (Lost_4_Power) at [Losing_Power_4 (0617A79C)](#trigger-0617a79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Lost_Power_5 (06179A4C)](#trigger-06179a4c).
2. Set local flag 30 (Lost_5_Power).
3. Enable and reset applicable timers for [Player_Lost (06178D0C)](#trigger-06178d0c).
4. Disable [Losing_Power_5 (06179F3C)](#trigger-06179f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8753, Events line 9089, Actions line 9425.

<a id="trigger-06179a4c"></a>

### 184. Lost_Power_5 - 06179A4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Losing_Power_5 (06179F3C)](#trigger-06179f3c).

Incoming activation links: enable from [Lost_Power_4 (06187A9C)](#trigger-06187a9c).

Attached scope: tag definitions 0617ACCC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 30 (Lost_5_Power) is set.

Flag writers in this mission: set local flag 30 (Lost_5_Power) at [Losing_Power_5 (06179F3C)](#trigger-06179f3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Losing_Power_5 (06179F3C)](#trigger-06179f3c).
2. Disable [Lost_Power_5 (06179A4C)](#trigger-06179a4c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8754, Events line 9090, Actions line 9426.

<a id="trigger-06178d0c"></a>

### 185. Player_Lost - 06178D0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Losing_Power_5 (06179F3C)](#trigger-06179f3c); enable from [LosingPP7_Easy (04EB9CCC)](#trigger-04eb9ccc).

Attached scope: tag definitions 06178ACC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8755, Events line 9091, Actions line 9427.

<a id="trigger-0bb6491c"></a>

### 186. Start_RD_U_Patrol - 0BB6491C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BB73D5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_RDU_Patrol (0BB37C5C)](all01umd-teams.md#team-0bb37c5c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8756, Events line 9092, Actions line 9428.

<a id="trigger-0bb37f3c"></a>

### 187. Start_RHRL_Patrol - 0BB37F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BB363BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_RHRL_Patrol (0BB4625C)](all01umd-teams.md#team-0bb4625c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8757, Events line 9093, Actions line 9429.

<a id="trigger-08ad89ac"></a>

### 188. WindSounds1_Pre - 08AD89AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08AD86BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 14 (cell 100, 110).
2. Play sound _Amb_WindCold at waypoint 676 (cell 98, 126).
3. Play sound _Amb_WindPlains at waypoint 677 (cell 122, 110).
4. Play sound _Amb_WindPlains at waypoint 40 (cell 92, 93).
5. Play sound _Amb_WindCold at waypoint 21 (cell 81, 84).
6. Play sound _Amb_WindPlains at waypoint 678 (cell 112, 135).
7. Play sound _Amb_WindCold at waypoint 679 (cell 109, 77).
8. Play sound _Amb_WindPlains at waypoint 474 (cell 129, 91).
9. Play sound _Amb_WindPlains at waypoint 680 (cell 134, 110).
10. Play sound _Amb_WindCold at waypoint 28 (cell 135, 126).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8758, Events line 9094, Actions line 9430.

<a id="trigger-08adc8dc"></a>

### 189. WindSounds2_Pre - 08ADC8DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09F7B4BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 32 (cell 138, 101).
2. Play sound _Amb_WindPlains at waypoint 681 (cell 153, 114).
3. Play sound _Amb_WindCold at waypoint 682 (cell 150, 125).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8759, Events line 9095, Actions line 9431.

<a id="trigger-08adae2c"></a>

### 190. Crickets1 - 08ADAE2C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09F7B20C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_CricketChirps at waypoint 683 (cell 114, 87).
2. Play sound _Amb_CricketChirps at waypoint 684 (cell 84, 108).
3. Play sound _Amb_CricketChirps at waypoint 685 (cell 107, 131).
4. Play sound _Amb_CricketChirps at waypoint 686 (cell 124, 134).
5. Play sound _Amb_CricketChirps at waypoint 687 (cell 94, 129).
6. Play sound _Amb_CricketChirps at waypoint 688 (cell 134, 144).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8760, Events line 9096, Actions line 9432.

<a id="trigger-08a00f3c"></a>

### 191. Kill_Pipes - 08A00F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pipes (CAMISC05), owner Neutral, cell (45, 72), tag 08A0080C, persistence mode 0; Pipes (CAMISC05), owner Neutral, cell (49, 68), tag 08A0080C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8761, Events line 9097, Actions line 9433.

<a id="trigger-04c199bc"></a>

### 192. Water_Sounds1 - 04C199BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04C1986C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 227 (cell 62, 105).
2. Play sound _Amb_OceanLight at waypoint 78 (cell 75, 100).
3. Play sound _Amb_OceanHeavy at waypoint 228 (cell 72, 84).
4. Play sound _Amb_OceanLight at waypoint 229 (cell 77, 77).
5. Play sound _Amb_OceanHeavy at waypoint 230 (cell 84, 71).
6. Play sound _Amb_OceanLight at waypoint 231 (cell 92, 68).
7. Play sound _Amb_OceanHeavy at waypoint 232 (cell 93, 57).
8. Play sound _Amb_OceanLight at waypoint 233 (cell 105, 55).
9. Play sound _Amb_OceanHeavy at waypoint 127 (cell 64, 90).
10. Play sound _Amb_OceanLight at waypoint 234 (cell 70, 70).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8762, Events line 9098, Actions line 9434.

<a id="trigger-09f7b59c"></a>

### 193. Wind3 - 09F7B59C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09F7B3DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 46 (cell 85, 101).
2. Play sound _Amb_WindPlains at waypoint 470 (cell 88, 118).
3. Play sound _Amb_WindCold at waypoint 137 (cell 111, 110).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8763, Events line 9099, Actions line 9435.

<a id="trigger-0c077bcc"></a>

### 194. Camera_Harriers - 0C077BCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera_Bridge (0972981C)](#trigger-0972981c); enable from [Camera_HarrierStart (0972907C)](#trigger-0972907c).

Attached scope: tag definitions 0C0778DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_Harriers (0780F21C)](all01umd-teams.md#team-0780f21c).
2. Supply reinforcement team [TEAM_Harrier2 (0780BC8C)](all01umd-teams.md#team-0780bc8c).
3. Move the camera to waypoint 364 (cell 55, 72) with speed setting 1.
4. Enable and reset applicable timers for [Camera_Player_Base (0B0246CC)](#trigger-0b0246cc).
5. Disable [Camera_Harriers (0C077BCC)](#trigger-0c077bcc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8764, Events line 9100, Actions line 9436.

<a id="trigger-0a992f3c"></a>

### 195. Change_House_Yuri - 0A992F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A992A9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8765, Events line 9101, Actions line 9437.

<a id="trigger-096c466c"></a>

### 196. Start_CityP - 096C466C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096C783C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_City2 (089305FC)](all01umd-teams.md#team-089305fc).
2. Create/recruit team [TEAM_CityP3 (0AEB68DC)](all01umd-teams.md#team-0aeb68dc).
3. Create/recruit team [TEAM_CityP4 (08934B5C)](all01umd-teams.md#team-08934b5c).
4. Create/recruit team [TEAM_CityP6 (096C680C)](all01umd-teams.md#team-096c680c).
5. Create/recruit team [TEAM_CityP7 (096FCB5C)](all01umd-teams.md#team-096fcb5c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8766, Events line 9102, Actions line 9438.

<a id="trigger-0972981c"></a>

### 197. Camera_Bridge - 0972981C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0972916C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 126 (cell 45, 85) with speed setting 2.
2. Enable and reset applicable timers for [Camera_Harriers (0C077BCC)](#trigger-0c077bcc).
3. Disable [Camera_Bridge (0972981C)](#trigger-0972981c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8767, Events line 9103, Actions line 9439.

<a id="trigger-0972907c"></a>

### 198. Camera_HarrierStart - 0972907C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0972ADFC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 417 (cell 56, 89) with speed setting 1.
2. Enable and reset applicable timers for [Camera_Harriers (0C077BCC)](#trigger-0c077bcc).
3. Disable [Camera_HarrierStart (0972907C)](#trigger-0972907c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8768, Events line 9104, Actions line 9440.

<a id="trigger-0b7c0aec"></a>

### 199. Set_PsyDom_Time - 0B7C0AEC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B7C03FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set Superweapon Charge; main setting 7; location/duration field 90.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8769, Events line 9105, Actions line 9441.

<a id="trigger-0c44064c"></a>

### 200. Change_House_PP2 - 0C44064C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Enable and reset applicable timers for [PP2_Entered (095AE59C)](#trigger-095ae59c).
3. Enable and reset applicable timers for [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac).
4. Disable [Change_House_PP2 (0C44064C)](#trigger-0c44064c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8770, Events line 9106, Actions line 9442.

<a id="trigger-095ae59c"></a>

### 201. PP2_Entered - 095AE59C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change_House_PP2 (0C44064C)](#trigger-0c44064c).

Incoming activation links: enable from [Change_House_PP2 (0C44064C)](#trigger-0c44064c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 33 (Lost_Tech02_USA).
2. Enable and reset applicable timers for [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c).
3. Enable and reset applicable timers for [PP1_Group_Done_FalseA (0BADE25C)](#trigger-0bade25c).
4. Enable and reset applicable timers for [PP1_Group_Done_FalseB (0C18404C)](#trigger-0c18404c).
5. Enable and reset applicable timers for [Good_Job_1 (0C9733CC)](#trigger-0c9733cc).
6. Set local flag 7 (PP2_Entered).
7. Disable [PP2_Entered (095AE59C)](#trigger-095ae59c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8771, Events line 9107, Actions line 9443.

<a id="trigger-095ae4ac"></a>

### 202. PP2_Destroyed - 095AE4AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP2_Entered (095AE59C)](#trigger-095ae59c).

Incoming activation links: enable from [Change_House_PP2 (0C44064C)](#trigger-0c44064c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR02 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 19 (PP2_Gone).
2. Enable and reset applicable timers for [Losing_Power_1 (0617F12C)](#trigger-0617f12c).
3. Enable and reset applicable timers for [Lost_Power_1 (0617A39C)](#trigger-0617a39c).
4. Enable and reset applicable timers for [PP1_Group_Done_True (0BADE68C)](#trigger-0bade68c).
5. Enable and reset applicable timers for [PP1_Group_Done_FalseA (0BADE25C)](#trigger-0bade25c).
6. Enable and reset applicable timers for [PP1_Group_Done_FalseB (0C18404C)](#trigger-0c18404c).
7. Set local flag 7 (PP2_Entered).
8. Disable [PP2_Entered (095AE59C)](#trigger-095ae59c).
9. Disable [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8772, Events line 9108, Actions line 9444.

<a id="trigger-0baad3fc"></a>

### 203. PP3_Entered - 0BAAD3FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_PP3_Checks (09178C4C)](#trigger-09178c4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 35 (Lost_Tech03_USA).
2. Enable and reset applicable timers for [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c).
3. Enable and reset applicable timers for [PP2_Group_Done_FalseA (0BABF84C)](#trigger-0babf84c).
4. Enable and reset applicable timers for [PP2_Group_Done_FalseB (0BABF75C)](#trigger-0babf75c).
5. Enable and reset applicable timers for [Good_Job_1 (0C9733CC)](#trigger-0c9733cc).
6. Set local flag 8 (PP3_Entered).
7. Disable [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8773, Events line 9109, Actions line 9445.

<a id="trigger-0baba08c"></a>

### 204. PP2_Group_Done_True - 0BABA08C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); enable from [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc); enable from [PP4_Entered (0BAAD22C)](#trigger-0baad22c); enable from [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 8 (PP3_Entered) is set.
2. local flag 9 (PP4_Entered) is set.

Flag writers in this mission: set local flag 8 (PP3_Entered) at [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); set local flag 8 (PP3_Entered) at [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc); set local flag 9 (PP4_Entered) at [PP4_Entered (0BAAD22C)](#trigger-0baad22c); set local flag 9 (PP4_Entered) at [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP2_Group_Done_FalseA (0BABF84C)](#trigger-0babf84c).
2. Disable [PP2_Group_Done_FalseB (0BABF75C)](#trigger-0babf75c).
3. Enable and reset applicable timers for [Check_PP2_True (0BFCC7DC)](#trigger-0bfcc7dc).
4. Enable and reset applicable timers for [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec).
5. Disable [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8774, Events line 9110, Actions line 9446.

<a id="trigger-0babf84c"></a>

### 205. PP2_Group_Done_FalseA - 0BABF84C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c).

Incoming activation links: enable from [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); enable from [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc); enable from [PP4_Entered (0BAAD22C)](#trigger-0baad22c); enable from [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 8 (PP3_Entered) is set.
2. local flag 9 (PP4_Entered) is clear.

Flag writers in this mission: set local flag 8 (PP3_Entered) at [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); set local flag 8 (PP3_Entered) at [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc); set local flag 9 (PP4_Entered) at [PP4_Entered (0BAAD22C)](#trigger-0baad22c); set local flag 9 (PP4_Entered) at [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c).
2. Disable [PP2_Group_Done_FalseB (0BABF75C)](#trigger-0babf75c).
3. Disable [PP2_Group_Done_FalseA (0BABF84C)](#trigger-0babf84c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8775, Events line 9111, Actions line 9447.

<a id="trigger-0babf75c"></a>

### 206. PP2_Group_Done_FalseB - 0BABF75C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP2_Group_Done_FalseA (0BABF84C)](#trigger-0babf84c).

Incoming activation links: enable from [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); enable from [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc); enable from [PP4_Entered (0BAAD22C)](#trigger-0baad22c); enable from [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c).

Attached scope: tag definitions 0BABFBDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (PP4_Entered) is set.
2. local flag 8 (PP3_Entered) is clear.

Flag writers in this mission: set local flag 9 (PP4_Entered) at [PP4_Entered (0BAAD22C)](#trigger-0baad22c); set local flag 9 (PP4_Entered) at [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c); set local flag 8 (PP3_Entered) at [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); set local flag 8 (PP3_Entered) at [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c).
2. Disable [PP2_Group_Done_FalseA (0BABF84C)](#trigger-0babf84c).
3. Disable [PP2_Group_Done_FalseB (0BABF75C)](#trigger-0babf75c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8776, Events line 9112, Actions line 9448.

<a id="trigger-0babb5dc"></a>

### 207. PP3_Destroyed - 0BABB5DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc).

Incoming activation links: enable from [Start_PP3_Checks (09178C4C)](#trigger-09178c4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR03 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 20 (PP3_Gone).
2. Enable and reset applicable timers for [Losing_Power_1 (0617F12C)](#trigger-0617f12c).
3. Enable and reset applicable timers for [Lost_Power_1 (0617A39C)](#trigger-0617a39c).
4. Enable and reset applicable timers for [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c).
5. Enable and reset applicable timers for [PP2_Group_Done_FalseA (0BABF84C)](#trigger-0babf84c).
6. Enable and reset applicable timers for [PP2_Group_Done_FalseB (0BABF75C)](#trigger-0babf75c).
7. Set local flag 8 (PP3_Entered).
8. Disable [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc).
9. Disable [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8777, Events line 9113, Actions line 9449.

<a id="trigger-0baad22c"></a>

### 208. PP4_Entered - 0BAAD22C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_PP4_Check (091786BC)](#trigger-091786bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 36 (Lost_Tech04_USA).
2. Enable and reset applicable timers for [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c).
3. Enable and reset applicable timers for [PP2_Group_Done_FalseA (0BABF84C)](#trigger-0babf84c).
4. Enable and reset applicable timers for [PP2_Group_Done_FalseB (0BABF75C)](#trigger-0babf75c).
5. Enable and reset applicable timers for [Good_Job_1 (0C9733CC)](#trigger-0c9733cc).
6. Set local flag 9 (PP4_Entered).
7. Disable [PP4_Entered (0BAAD22C)](#trigger-0baad22c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8778, Events line 9114, Actions line 9450.

<a id="trigger-0bac2a9c"></a>

### 209. PP4_Destroyed - 0BAC2A9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_Entered (0BAAD22C)](#trigger-0baad22c).

Incoming activation links: enable from [Start_PP4_Check (091786BC)](#trigger-091786bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR04 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 21 (PP4_Gone).
2. Enable and reset applicable timers for [Losing_Power_1 (0617F12C)](#trigger-0617f12c).
3. Enable and reset applicable timers for [Lost_Power_1 (0617A39C)](#trigger-0617a39c).
4. Enable and reset applicable timers for [PP2_Group_Done_True (0BABA08C)](#trigger-0baba08c).
5. Enable and reset applicable timers for [PP2_Group_Done_FalseA (0BABF84C)](#trigger-0babf84c).
6. Enable and reset applicable timers for [PP2_Group_Done_FalseB (0BABF75C)](#trigger-0babf75c).
7. Set local flag 9 (PP4_Entered).
8. Disable [PP4_Entered (0BAAD22C)](#trigger-0baad22c).
9. Disable [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8779, Events line 9115, Actions line 9451.

<a id="trigger-0baae54c"></a>

### 210. PP5_Entered - 0BAAE54C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_PP5_Check (091782CC)](#trigger-091782cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 37 (Lost_Tech05_USA).
2. Enable and reset applicable timers for [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).
3. Enable and reset applicable timers for [PP3_Group_Done_FalseA (0BAB88EC)](#trigger-0bab88ec).
4. Enable and reset applicable timers for [PP3_Group_Done_FalseB (0BAB851C)](#trigger-0bab851c).
5. Enable and reset applicable timers for [Good_Job_1 (0C9733CC)](#trigger-0c9733cc).
6. Set local flag 10 (PP5_Entered).
7. Disable [PP5_Entered (0BAAE54C)](#trigger-0baae54c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8780, Events line 9116, Actions line 9452.

<a id="trigger-0baae1ac"></a>

### 211. PP3_Group_Done_True - 0BAAE1AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PP5_Entered (0BAAE54C)](#trigger-0baae54c); enable from [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc); enable from [PP6_Entered (0BAAE37C)](#trigger-0baae37c); enable from [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 10 (PP5_Entered) is set.
2. local flag 11 (PP6_Entered) is set.

Flag writers in this mission: set local flag 10 (PP5_Entered) at [PP5_Entered (0BAAE54C)](#trigger-0baae54c); set local flag 10 (PP5_Entered) at [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc); set local flag 11 (PP6_Entered) at [PP6_Entered (0BAAE37C)](#trigger-0baae37c); set local flag 11 (PP6_Entered) at [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP3_Group_Done_FalseA (0BAB88EC)](#trigger-0bab88ec).
2. Disable [PP3_Group_Done_FalseB (0BAB851C)](#trigger-0bab851c).
3. Enable and reset applicable timers for [Check_PP2_True (0BFCC7DC)](#trigger-0bfcc7dc).
4. Enable and reset applicable timers for [Check_PP2_False (0BFCC6EC)](#trigger-0bfcc6ec).
5. Disable [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8781, Events line 9117, Actions line 9453.

<a id="trigger-0bab88ec"></a>

### 212. PP3_Group_Done_FalseA - 0BAB88EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).

Incoming activation links: enable from [PP5_Entered (0BAAE54C)](#trigger-0baae54c); enable from [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc); enable from [PP6_Entered (0BAAE37C)](#trigger-0baae37c); enable from [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 10 (PP5_Entered) is set.
2. local flag 11 (PP6_Entered) is clear.

Flag writers in this mission: set local flag 10 (PP5_Entered) at [PP5_Entered (0BAAE54C)](#trigger-0baae54c); set local flag 10 (PP5_Entered) at [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc); set local flag 11 (PP6_Entered) at [PP6_Entered (0BAAE37C)](#trigger-0baae37c); set local flag 11 (PP6_Entered) at [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).
2. Disable [PP3_Group_Done_FalseB (0BAB851C)](#trigger-0bab851c).
3. Disable [PP3_Group_Done_FalseA (0BAB88EC)](#trigger-0bab88ec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8782, Events line 9118, Actions line 9454.

<a id="trigger-0bab851c"></a>

### 213. PP3_Group_Done_FalseB - 0BAB851C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP3_Group_Done_FalseA (0BAB88EC)](#trigger-0bab88ec).

Incoming activation links: enable from [PP5_Entered (0BAAE54C)](#trigger-0baae54c); enable from [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc); enable from [PP6_Entered (0BAAE37C)](#trigger-0baae37c); enable from [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc).

Attached scope: tag definitions 0BAAE0CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 11 (PP6_Entered) is set.
2. local flag 10 (PP5_Entered) is clear.

Flag writers in this mission: set local flag 11 (PP6_Entered) at [PP6_Entered (0BAAE37C)](#trigger-0baae37c); set local flag 11 (PP6_Entered) at [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc); set local flag 10 (PP5_Entered) at [PP5_Entered (0BAAE54C)](#trigger-0baae54c); set local flag 10 (PP5_Entered) at [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).
2. Disable [PP3_Group_Done_FalseA (0BAB88EC)](#trigger-0bab88ec).
3. Disable [PP3_Group_Done_FalseB (0BAB851C)](#trigger-0bab851c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8783, Events line 9119, Actions line 9455.

<a id="trigger-0bab8acc"></a>

### 214. PP5_Destroyed - 0BAB8ACC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP5_Entered (0BAAE54C)](#trigger-0baae54c).

Incoming activation links: enable from [Start_PP5_Check (091782CC)](#trigger-091782cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR05 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 22 (PP5_Gone).
2. Enable and reset applicable timers for [Losing_Power_1 (0617F12C)](#trigger-0617f12c).
3. Enable and reset applicable timers for [Lost_Power_1 (0617A39C)](#trigger-0617a39c).
4. Enable and reset applicable timers for [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).
5. Enable and reset applicable timers for [PP3_Group_Done_FalseA (0BAB88EC)](#trigger-0bab88ec).
6. Enable and reset applicable timers for [PP3_Group_Done_FalseB (0BAB851C)](#trigger-0bab851c).
7. Set local flag 10 (PP5_Entered).
8. Disable [PP5_Entered (0BAAE54C)](#trigger-0baae54c).
9. Disable [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8784, Events line 9120, Actions line 9456.

<a id="trigger-0baae37c"></a>

### 215. PP6_Entered - 0BAAE37C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_PP6_Check (09179E6C)](#trigger-09179e6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 38 (Lost_Tech06_USA).
2. Enable and reset applicable timers for [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).
3. Enable and reset applicable timers for [PP3_Group_Done_FalseA (0BAB88EC)](#trigger-0bab88ec).
4. Enable and reset applicable timers for [PP3_Group_Done_FalseB (0BAB851C)](#trigger-0bab851c).
5. Enable and reset applicable timers for [Good_Job_1 (0C9733CC)](#trigger-0c9733cc).
6. Set local flag 11 (PP6_Entered).
7. Disable [PP6_Entered (0BAAE37C)](#trigger-0baae37c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8785, Events line 9121, Actions line 9457.

<a id="trigger-0bab89dc"></a>

### 216. PP6_Destroyed - 0BAB89DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP6_Entered (0BAAE37C)](#trigger-0baae37c).

Incoming activation links: enable from [Start_PP6_Check (09179E6C)](#trigger-09179e6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR06 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 23 (PP6_Gone).
2. Enable and reset applicable timers for [Losing_Power_1 (0617F12C)](#trigger-0617f12c).
3. Enable and reset applicable timers for [Lost_Power_1 (0617A39C)](#trigger-0617a39c).
4. Enable and reset applicable timers for [PP3_Group_Done_True (0BAAE1AC)](#trigger-0baae1ac).
5. Enable and reset applicable timers for [PP3_Group_Done_FalseA (0BAB88EC)](#trigger-0bab88ec).
6. Enable and reset applicable timers for [PP3_Group_Done_FalseB (0BAB851C)](#trigger-0bab851c).
7. Set local flag 11 (PP6_Entered).
8. Disable [PP6_Entered (0BAAE37C)](#trigger-0baae37c).
9. Disable [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8786, Events line 9122, Actions line 9458.

<a id="trigger-0bfca59c"></a>

### 217. PP7_Entered - 0BFCA59C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_PP6_Check (09179E6C)](#trigger-09179e6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 39 (Lost_Tech07_USA).
2. Enable and reset applicable timers for [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac).
3. Enable and reset applicable timers for [PP4_Group_Done_FalseA (0BAC1AAC)](#trigger-0bac1aac).
4. Enable and reset applicable timers for [PP4_Group_Done_FalseB (0BAC19BC)](#trigger-0bac19bc).
5. Enable and reset applicable timers for [Good_Job_1 (0C9733CC)](#trigger-0c9733cc).
6. Set local flag 12 (PP7_Entered).
7. Disable [PP7_Entered (0BFCA59C)](#trigger-0bfca59c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8787, Events line 9123, Actions line 9459.

<a id="trigger-0baac68c"></a>

### 218. PP7_Destroyed - 0BAAC68C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP7_Entered (0BFCA59C)](#trigger-0bfca59c).

Incoming activation links: enable from [Start_PP6_Check (09179E6C)](#trigger-09179e6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR07 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 12 (PP7_Entered).
2. Enable and reset applicable timers for [Losing_Power_1 (0617F12C)](#trigger-0617f12c).
3. Enable and reset applicable timers for [Lost_Power_1 (0617A39C)](#trigger-0617a39c).
4. Enable and reset applicable timers for [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac).
5. Enable and reset applicable timers for [PP4_Group_Done_FalseA (0BAC1AAC)](#trigger-0bac1aac).
6. Enable and reset applicable timers for [PP4_Group_Done_FalseB (0BAC19BC)](#trigger-0bac19bc).
7. Set local flag 24 (PP7_Gone).
8. Disable [PP7_Entered (0BFCA59C)](#trigger-0bfca59c).
9. Disable [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8788, Events line 9124, Actions line 9460.

<a id="trigger-0bfcdc7c"></a>

### 219. PP8_Entered - 0BFCDC7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start_PP6_Check (09179E6C)](#trigger-09179e6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Clear local flag 40 (Lost_Tech08_USA).
2. Enable and reset applicable timers for [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac).
3. Enable and reset applicable timers for [PP4_Group_Done_FalseA (0BAC1AAC)](#trigger-0bac1aac).
4. Enable and reset applicable timers for [PP4_Group_Done_FalseB (0BAC19BC)](#trigger-0bac19bc).
5. Enable and reset applicable timers for [Good_Job_1 (0C9733CC)](#trigger-0c9733cc).
6. Set local flag 13 (PP8_Entered).
7. Disable [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8789, Events line 9125, Actions line 9461.

<a id="trigger-0baac59c"></a>

### 220. PP8_Destroyed - 0BAAC59C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c).

Incoming activation links: enable from [Start_PP6_Check (09179E6C)](#trigger-09179e6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR08 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 25 (PP8_Gone).
2. Enable and reset applicable timers for [Losing_Power_1 (0617F12C)](#trigger-0617f12c).
3. Enable and reset applicable timers for [Lost_Power_1 (0617A39C)](#trigger-0617a39c).
4. Enable and reset applicable timers for [PP4_Group_Done_True (0BFCDAAC)](#trigger-0bfcdaac).
5. Enable and reset applicable timers for [PP4_Group_Done_FalseA (0BAC1AAC)](#trigger-0bac1aac).
6. Enable and reset applicable timers for [PP4_Group_Done_FalseB (0BAC19BC)](#trigger-0bac19bc).
7. Set local flag 13 (PP8_Entered).
8. Disable [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c).
9. Disable [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8790, Events line 9126, Actions line 9462.

<a id="trigger-0e0f4dcc"></a>

### 221. Deploy_GGI_Group2 - 0E0F4DCC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E0F227C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_GGI_Group2 (0E0F469C)](all01umd-teams.md#team-0e0f469c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8791, Events line 9127, Actions line 9463.

<a id="trigger-06b9c76c"></a>

### 222. Start_AD_GD_Patrol - 06B9C76C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B9C1EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TEAM_PP1_Group_PatrolB (06B9CD4C)](all01umd-teams.md#team-06b9cd4c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8792, Events line 9128, Actions line 9464.

<a id="trigger-0e0ea53c"></a>

### 223. Select_Dominator - 0E0EA53C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Sell_Psychic (0951879C)](#trigger-0951879c).

Attached scope: Psychic Dominator (YAPPET), owner Confederation, cell (46, 69), tag 089ED98C, persistence mode 2.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_PsychicDomin.
2. Disable [Select_Dominator (0E0EA53C)](#trigger-0e0ea53c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8793, Events line 9129, Actions line 9465.

<a id="trigger-097d8cfc"></a>

### 224. GivePower1 - 097D8CFC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 6 (PP1_Entered) is set.

Flag writers in this mission: set local flag 6 (PP1_Entered) at [PP1_Entered (108EA04C)](#trigger-108ea04c); set local flag 6 (PP1_Entered) at [PP1_Destroyed (108ECA9C)](#trigger-108eca9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [TakePower1 (097D840C)](#trigger-097d840c).
3. Disable [GivePower1 (097D8CFC)](#trigger-097d8cfc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8794, Events line 9130, Actions line 9466.

<a id="trigger-097d840c"></a>

### 225. TakePower1 - 097D840C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [GivePower1 (097D8CFC)](#trigger-097d8cfc).

Incoming activation links: enable from [GivePower1 (097D8CFC)](#trigger-097d8cfc).

Attached scope: Power Plant (GAPOWR), owner PowerHouse, cell (42, 91), tag 097D8C1C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 18 (PP1_Gone) is set.

Flag writers in this mission: set local flag 18 (PP1_Gone) at [PP1_Destroyed (108ECA9C)](#trigger-108eca9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Disable [TakePower1 (097D840C)](#trigger-097d840c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8795, Events line 9131, Actions line 9467.

<a id="trigger-097def3c"></a>

### 226. GivePower2 - 097DEF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 7 (PP2_Entered) is set.

Flag writers in this mission: set local flag 7 (PP2_Entered) at [PP2_Entered (095AE59C)](#trigger-095ae59c); set local flag 7 (PP2_Entered) at [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [TakePower2 (097DEA0C)](#trigger-097dea0c).
3. Disable [GivePower2 (097DEF3C)](#trigger-097def3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8796, Events line 9132, Actions line 9468.

<a id="trigger-097dea0c"></a>

### 227. TakePower2 - 097DEA0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [GivePower2 (097DEF3C)](#trigger-097def3c).

Incoming activation links: enable from [GivePower2 (097DEF3C)](#trigger-097def3c).

Attached scope: Power Plant (GAPOWR), owner PowerHouse, cell (44, 91), tag 097DEAFC, persistence mode 2.

**Wait for the recorded events:**

1. local flag 19 (PP2_Gone) is set.

Flag writers in this mission: set local flag 19 (PP2_Gone) at [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Disable [TakePower2 (097DEA0C)](#trigger-097dea0c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8797, Events line 9133, Actions line 9469.

<a id="trigger-0bc3224c"></a>

### 228. GivePower3 - 0BC3224C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 8 (PP3_Entered) is set.

Flag writers in this mission: set local flag 8 (PP3_Entered) at [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); set local flag 8 (PP3_Entered) at [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [TakePower3 (0BC3207C)](#trigger-0bc3207c).
3. Disable [GivePower3 (0BC3224C)](#trigger-0bc3224c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8798, Events line 9134, Actions line 9470.

<a id="trigger-0bc3207c"></a>

### 229. TakePower3 - 0BC3207C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [GivePower3 (0BC3224C)](#trigger-0bc3224c).

Incoming activation links: enable from [GivePower3 (0BC3224C)](#trigger-0bc3224c).

Attached scope: Power Plant (GAPOWR), owner PowerHouse, cell (46, 91), tag 0BC3216C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 20 (PP3_Gone) is set.

Flag writers in this mission: set local flag 20 (PP3_Gone) at [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Disable [TakePower3 (0BC3207C)](#trigger-0bc3207c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8799, Events line 9135, Actions line 9471.

<a id="trigger-0bc33e9c"></a>

### 230. GivePower4 - 0BC33E9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 9 (PP4_Entered) is set.

Flag writers in this mission: set local flag 9 (PP4_Entered) at [PP4_Entered (0BAAD22C)](#trigger-0baad22c); set local flag 9 (PP4_Entered) at [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [TakePower4 (0BC33CCC)](#trigger-0bc33ccc).
3. Disable [GivePower4 (0BC33E9C)](#trigger-0bc33e9c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8800, Events line 9136, Actions line 9472.

<a id="trigger-0bc33ccc"></a>

### 231. TakePower4 - 0BC33CCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [GivePower4 (0BC33E9C)](#trigger-0bc33e9c).

Incoming activation links: enable from [GivePower4 (0BC33E9C)](#trigger-0bc33e9c).

Attached scope: Power Plant (GAPOWR), owner PowerHouse, cell (46, 93), tag 0BC33DBC, persistence mode 2.

**Wait for the recorded events:**

1. local flag 21 (PP4_Gone) is set.

Flag writers in this mission: set local flag 21 (PP4_Gone) at [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Disable [TakePower4 (0BC33CCC)](#trigger-0bc33ccc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8801, Events line 9137, Actions line 9473.

<a id="trigger-09148a0c"></a>

### 232. GivePower5 - 09148A0C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 10 (PP5_Entered) is set.

Flag writers in this mission: set local flag 10 (PP5_Entered) at [PP5_Entered (0BAAE54C)](#trigger-0baae54c); set local flag 10 (PP5_Entered) at [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [TakePower5 (0914866C)](#trigger-0914866c).
3. Disable [GivePower5 (09148A0C)](#trigger-09148a0c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8802, Events line 9138, Actions line 9474.

<a id="trigger-0914866c"></a>

### 233. TakePower5 - 0914866C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [GivePower5 (09148A0C)](#trigger-09148a0c).

Incoming activation links: enable from [GivePower5 (09148A0C)](#trigger-09148a0c).

Attached scope: Power Plant (GAPOWR), owner PowerHouse, cell (48, 93), tag 0914892C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 22 (PP5_Gone) is set.

Flag writers in this mission: set local flag 22 (PP5_Gone) at [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Disable [TakePower5 (0914866C)](#trigger-0914866c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8803, Events line 9139, Actions line 9475.

<a id="trigger-0914883c"></a>

### 234. GivePower6 - 0914883C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 11 (PP6_Entered) is set.

Flag writers in this mission: set local flag 11 (PP6_Entered) at [PP6_Entered (0BAAE37C)](#trigger-0baae37c); set local flag 11 (PP6_Entered) at [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [TakePower6 (091578AC)](#trigger-091578ac).
3. Disable [GivePower6 (0914883C)](#trigger-0914883c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8804, Events line 9140, Actions line 9476.

<a id="trigger-091578ac"></a>

### 235. TakePower6 - 091578AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [GivePower6 (0914883C)](#trigger-0914883c).

Incoming activation links: enable from [GivePower6 (0914883C)](#trigger-0914883c).

Attached scope: Power Plant (GAPOWR), owner PowerHouse, cell (44, 93), tag 0914875C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 23 (PP6_Gone) is set.

Flag writers in this mission: set local flag 23 (PP6_Gone) at [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Disable [TakePower6 (091578AC)](#trigger-091578ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8805, Events line 9141, Actions line 9477.

<a id="trigger-09b7ecec"></a>

### 236. GivePower7 - 09B7ECEC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 12 (PP7_Entered) is set.

Flag writers in this mission: set local flag 12 (PP7_Entered) at [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); set local flag 12 (PP7_Entered) at [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [TakePower7 (09B7E5CC)](#trigger-09b7e5cc).
3. Disable [GivePower7 (09B7ECEC)](#trigger-09b7ecec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8806, Events line 9142, Actions line 9478.

<a id="trigger-09b7e5cc"></a>

### 237. TakePower7 - 09B7E5CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [GivePower7 (09B7ECEC)](#trigger-09b7ecec).

Incoming activation links: enable from [GivePower7 (09B7ECEC)](#trigger-09b7ecec).

Attached scope: Power Plant (GAPOWR), owner PowerHouse, cell (44, 89), tag 09B7EC0C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 24 (PP7_Gone) is set.

Flag writers in this mission: set local flag 24 (PP7_Gone) at [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Disable [TakePower7 (09B7E5CC)](#trigger-09b7e5cc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8807, Events line 9143, Actions line 9479.

<a id="trigger-09b7eb1c"></a>

### 238. GivePower8 - 09B7EB1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 13 (PP8_Entered) is set.

Flag writers in this mission: set local flag 13 (PP8_Entered) at [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c); set local flag 13 (PP8_Entered) at [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [TakePower8 (09B7E4DC)](#trigger-09b7e4dc).
3. Disable [GivePower8 (09B7EB1C)](#trigger-09b7eb1c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8808, Events line 9144, Actions line 9480.

<a id="trigger-09b7e4dc"></a>

### 239. TakePower8 - 09B7E4DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [GivePower8 (09B7EB1C)](#trigger-09b7eb1c).

Incoming activation links: enable from [GivePower8 (09B7EB1C)](#trigger-09b7eb1c).

Attached scope: Power Plant (GAPOWR), owner PowerHouse, cell (42, 89), tag 09B7E6BC, persistence mode 2.

**Wait for the recorded events:**

1. Building does not exist: type index 409. A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).
2. Disable [TakePower8 (09B7E4DC)](#trigger-09b7e4dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8809, Events line 9145, Actions line 9481.

<a id="trigger-07a89e6c"></a>

### 240. BackBridge_Gone - 07A89E6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Kill_AllBackBridge (07A89C0C)](#trigger-07a89c0c).
2. Enable and reset applicable timers for [Destroy_Me (079B8BBC)](#trigger-079b8bbc).
3. Enable and reset applicable timers for [Damage_Me (079BAE6C)](#trigger-079bae6c).
4. Disable [BackBridge_Gone (07A89E6C)](#trigger-07a89e6c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8810, Events line 9146, Actions line 9482.

<a id="trigger-07a89c0c"></a>

### 241. Kill_AllBackBridge - 07A89C0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BackBridge_Gone (07A89E6C)](#trigger-07a89e6c).

Incoming activation links: enable from [BackBridge_Gone (07A89E6C)](#trigger-07a89e6c).

Attached scope: tag definitions 07A89CFC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Disable [Kill_AllBackBridge (07A89C0C)](#trigger-07a89c0c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8811, Events line 9147, Actions line 9483.

<a id="trigger-079b8bbc"></a>

### 242. Destroy_Me - 079B8BBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Connector_Step2 (07A8CCBC)](#trigger-07a8ccbc).

Incoming activation links: enable from [BackBridge_Gone (07A89E6C)](#trigger-07a89e6c).

Attached scope: tag definitions 07A8CBDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Disable [Destroy_Me (079B8BBC)](#trigger-079b8bbc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8812, Events line 9148, Actions line 9484.

<a id="trigger-079bae6c"></a>

### 243. Damage_Me - 079BAE6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Connector_Gone (07A8917C)](#trigger-07a8917c).

Incoming activation links: enable from [BackBridge_Gone (07A89E6C)](#trigger-07a89e6c).

Attached scope: tag definitions 07A8CDAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 78; location/duration field CA.
2. Disable [Damage_Me (079BAE6C)](#trigger-079bae6c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8813, Events line 9149, Actions line 9485.

<a id="trigger-0611babc"></a>

### 244. Kill_Harriers - 0611BABC

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (56, 77); tag 0611EEAC, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Vertical Line: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

**Then perform these actions in order:**

1. Destroy all of: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8814, Events line 9150, Actions line 9486.

<a id="trigger-098e903c"></a>

### 245. PP1_PlayerAttack - 098E903C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP1_Destroyed (108ECA9C)](#trigger-108eca9c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PowerAttacked (0617D71C)](#trigger-0617d71c).
2. Display message “WARNING - Do not attack Power Plants!” (MISSION:Attack3).
3. Disable [PP1_PlayerAttack (098E903C)](#trigger-098e903c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8815, Events line 9151, Actions line 9487.

<a id="trigger-0617d71c"></a>

### 246. PowerAttacked - 0617D71C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PP1_PlayerAttack (098E903C)](#trigger-098e903c); enable from [PP2_PlayerAttack (099A7ACC)](#trigger-099a7acc); enable from [PP3_PlayerAttack (099A753C)](#trigger-099a753c); enable from [PP4_PlayerAttack (099A714C)](#trigger-099a714c); enable from [PP5_PlayerAttack (099A436C)](#trigger-099a436c); enable from [PP6_PlayerAttack (099A0F3C)](#trigger-099a0f3c); enable from [PP7_PlayerAttack (099A0A6C)](#trigger-099a0a6c); enable from [PP8_PlayerAttack (099A067C)](#trigger-099a067c).

Attached scope: tag definitions 0617AF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA1_EvaPowerAttkWarn.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8816, Events line 9152, Actions line 9488.

<a id="trigger-099a7acc"></a>

### 247. PP2_PlayerAttack - 099A7ACC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP2_Destroyed (095AE4AC)](#trigger-095ae4ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PowerAttacked (0617D71C)](#trigger-0617d71c).
2. Display message “WARNING - Do not attack Power Plants!” (MISSION:Attack3).
3. Disable [PP2_PlayerAttack (099A7ACC)](#trigger-099a7acc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8817, Events line 9153, Actions line 9489.

<a id="trigger-099a753c"></a>

### 248. PP3_PlayerAttack - 099A753C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PowerAttacked (0617D71C)](#trigger-0617d71c).
2. Display message “WARNING - Do not attack Power Plants!” (MISSION:Attack3).
3. Disable [PP3_PlayerAttack (099A753C)](#trigger-099a753c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8818, Events line 9154, Actions line 9490.

<a id="trigger-099a714c"></a>

### 249. PP4_PlayerAttack - 099A714C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PowerAttacked (0617D71C)](#trigger-0617d71c).
2. Display message “WARNING - Do not attack Power Plants!” (MISSION:Attack3).
3. Disable [PP4_PlayerAttack (099A714C)](#trigger-099a714c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8819, Events line 9155, Actions line 9491.

<a id="trigger-099a436c"></a>

### 250. PP5_PlayerAttack - 099A436C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PowerAttacked (0617D71C)](#trigger-0617d71c).
2. Display message “WARNING - Do not attack Power Plants!” (MISSION:Attack3).
3. Disable [PP5_PlayerAttack (099A436C)](#trigger-099a436c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8820, Events line 9156, Actions line 9492.

<a id="trigger-099a0f3c"></a>

### 251. PP6_PlayerAttack - 099A0F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PowerAttacked (0617D71C)](#trigger-0617d71c).
2. Display message “WARNING - Do not attack Power Plants!” (MISSION:Attack3).
3. Disable [PP6_PlayerAttack (099A0F3C)](#trigger-099a0f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8821, Events line 9157, Actions line 9493.

<a id="trigger-099a0a6c"></a>

### 252. PP7_PlayerAttack - 099A0A6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PowerAttacked (0617D71C)](#trigger-0617d71c).
2. Display message “WARNING - Do not attack Power Plants!” (MISSION:Attack3).
3. Disable [PP7_PlayerAttack (099A0A6C)](#trigger-099a0a6c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8822, Events line 9158, Actions line 9494.

<a id="trigger-099a067c"></a>

### 253. PP8_PlayerAttack - 099A067C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PowerAttacked (0617D71C)](#trigger-0617d71c).
2. Display message “WARNING - Do not attack Power Plants!” (MISSION:Attack3).
3. Disable [PP8_PlayerAttack (099A067C)](#trigger-099a067c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8823, Events line 9159, Actions line 9495.

<a id="trigger-096d092c"></a>

### 254. Garrison_BY - 096D092C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096D019C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_BYgarrison (096D287C)](all01umd-teams.md#team-096d287c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8824, Events line 9160, Actions line 9496.

<a id="trigger-087857cc"></a>

### 255. Damage_Reactor - 087857CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0878524C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 364; location/duration field NA.

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8825, Events line 9161, Actions line 9497.

<a id="trigger-061ff03c"></a>

### 256. SpySat_Boom - 061FF03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change_Radar_House (0BE0B26C)](#trigger-0be0b26c).

Attached scope: SpySat Uplink (GASPYSAT), owner Americans, cell (85, 110), tag 0BE0AB4C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reshroud Map; main setting 0.
2. Reveal the zone associated with waypoint 496 (cell 53, 69).
3. Disable [SpySat_Boom (061FF03C)](#trigger-061ff03c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8826, Events line 9162, Actions line 9498.

<a id="trigger-07ec78ac"></a>

### 257. Power_Back_Down - 07EC78AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07EC725C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Low Power: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Stop the visible mission timer.
2. Disable [Power_Back_Down (07EC78AC)](#trigger-07ec78ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8827, Events line 9163, Actions line 9499.

<a id="trigger-07a67d1c"></a>

### 258. PP1_Is_America - 07A67D1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP1_PlayerAttack (098E903C)](#trigger-098e903c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 393 (global list position: Hollywood Sign (CALA13)). A map-local type-list change can affect index interpretation.
2. local flag 31 (Lost_Tech01_USA) is set.

Flag writers in this mission: clear local flag 31 (Lost_Tech01_USA) at [PP1_Entered (108EA04C)](#trigger-108ea04c); clear local flag 31 (Lost_Tech01_USA) at [PP1_Is_America (07A67D1C)](#trigger-07a67d1c); set local flag 31 (Lost_Tech01_USA) at [PP1_Not_America (07A6737C)](#trigger-07a6737c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 31 (Lost_Tech01_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8828, Events line 9164, Actions line 9500.

<a id="trigger-07a677bc"></a>

### 259. PP1_Is_Neutral - 07A677BC

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP1_Is_America (07A67D1C)](#trigger-07a67d1c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 393 (global list position: Hollywood Sign (CALA13)). A map-local type-list change can affect index interpretation.
2. local flag 32 (Lost_Tech_01_Neu) is set.

Flag writers in this mission: clear local flag 32 (Lost_Tech_01_Neu) at [PP1_Is_Neutral (07A677BC)](#trigger-07a677bc); set local flag 32 (Lost_Tech_01_Neu) at [PP1_Not_Neutral (07A671FC)](#trigger-07a671fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 32 (Lost_Tech_01_Neu).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8829, Events line 9165, Actions line 9501.

<a id="trigger-07a6737c"></a>

### 260. PP1_Not_America - 07A6737C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP1_Is_Neutral (07A677BC)](#trigger-07a677bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 393 (global list position: Hollywood Sign (CALA13)). A map-local type-list change can affect index interpretation.
2. local flag 31 (Lost_Tech01_USA) is clear.

Flag writers in this mission: clear local flag 31 (Lost_Tech01_USA) at [PP1_Entered (108EA04C)](#trigger-108ea04c); clear local flag 31 (Lost_Tech01_USA) at [PP1_Is_America (07A67D1C)](#trigger-07a67d1c); set local flag 31 (Lost_Tech01_USA) at [PP1_Not_America (07A6737C)](#trigger-07a6737c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 31 (Lost_Tech01_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8830, Events line 9166, Actions line 9502.

<a id="trigger-07a671fc"></a>

### 261. PP1_Not_Neutral - 07A671FC

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP1_Not_America (07A6737C)](#trigger-07a6737c).

Attached scope: CAPOWR01, owner PowerHouse, cell (130, 129), tag 043A29AC, persistence mode 2.

**Wait for the recorded events:**

1. Building does not exist: type index 393 (global list position: Hollywood Sign (CALA13)). A map-local type-list change can affect index interpretation.
2. local flag 32 (Lost_Tech_01_Neu) is clear.

Flag writers in this mission: clear local flag 32 (Lost_Tech_01_Neu) at [PP1_Is_Neutral (07A677BC)](#trigger-07a677bc); set local flag 32 (Lost_Tech_01_Neu) at [PP1_Not_Neutral (07A671FC)](#trigger-07a671fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 32 (Lost_Tech_01_Neu).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8831, Events line 9167, Actions line 9503.

<a id="trigger-095a8c3c"></a>

### 262. PP2_Is_America - 095A8C3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP2_PlayerAttack (099A7ACC)](#trigger-099a7acc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 394 (global list position: Park Bench (CAPARK04)). A map-local type-list change can affect index interpretation.
2. local flag 33 (Lost_Tech02_USA) is set.

Flag writers in this mission: clear local flag 33 (Lost_Tech02_USA) at [PP2_Entered (095AE59C)](#trigger-095ae59c); clear local flag 33 (Lost_Tech02_USA) at [PP2_Is_America (095A8C3C)](#trigger-095a8c3c); set local flag 33 (Lost_Tech02_USA) at [PP2_Not_America (095A828C)](#trigger-095a828c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 33 (Lost_Tech02_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8832, Events line 9168, Actions line 9504.

<a id="trigger-095a856c"></a>

### 263. PP2_Is_Neutral - 095A856C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP2_Is_America (095A8C3C)](#trigger-095a8c3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 394 (global list position: Park Bench (CAPARK04)). A map-local type-list change can affect index interpretation.
2. local flag 34 (Lost_Tech02_Neut) is set.

Flag writers in this mission: clear local flag 34 (Lost_Tech02_Neut) at [PP2_Is_Neutral (095A856C)](#trigger-095a856c); set local flag 34 (Lost_Tech02_Neut) at [PP2_Not_Neutral (095ABC2C)](#trigger-095abc2c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 34 (Lost_Tech02_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8833, Events line 9169, Actions line 9505.

<a id="trigger-095a828c"></a>

### 264. PP2_Not_America - 095A828C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP2_Is_Neutral (095A856C)](#trigger-095a856c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 394 (global list position: Park Bench (CAPARK04)). A map-local type-list change can affect index interpretation.
2. local flag 33 (Lost_Tech02_USA) is clear.

Flag writers in this mission: clear local flag 33 (Lost_Tech02_USA) at [PP2_Entered (095AE59C)](#trigger-095ae59c); clear local flag 33 (Lost_Tech02_USA) at [PP2_Is_America (095A8C3C)](#trigger-095a8c3c); set local flag 33 (Lost_Tech02_USA) at [PP2_Not_America (095A828C)](#trigger-095a828c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 33 (Lost_Tech02_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8834, Events line 9170, Actions line 9506.

<a id="trigger-095abc2c"></a>

### 265. PP2_Not_Neutral - 095ABC2C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP2_Not_America (095A828C)](#trigger-095a828c).

Attached scope: CAPOWR02, owner PowerHouse, cell (130, 131), tag 0C446E7C, persistence mode 2.

**Wait for the recorded events:**

1. Building does not exist: type index 394 (global list position: Park Bench (CAPARK04)). A map-local type-list change can affect index interpretation.
2. local flag 34 (Lost_Tech02_Neut) is clear.

Flag writers in this mission: clear local flag 34 (Lost_Tech02_Neut) at [PP2_Is_Neutral (095A856C)](#trigger-095a856c); set local flag 34 (Lost_Tech02_Neut) at [PP2_Not_Neutral (095ABC2C)](#trigger-095abc2c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 34 (Lost_Tech02_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8835, Events line 9171, Actions line 9507.

<a id="trigger-095ab94c"></a>

### 266. PP3_Is_America - 095AB94C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP3_PlayerAttack (099A753C)](#trigger-099a753c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 395 (global list position: Park Bench (CAPARK05)). A map-local type-list change can affect index interpretation.
2. local flag 35 (Lost_Tech03_USA) is set.

Flag writers in this mission: clear local flag 35 (Lost_Tech03_USA) at [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); clear local flag 35 (Lost_Tech03_USA) at [PP3_Is_America (095AB94C)](#trigger-095ab94c); set local flag 35 (Lost_Tech03_USA) at [PP3_Not_America (095AB38C)](#trigger-095ab38c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 35 (Lost_Tech03_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8836, Events line 9172, Actions line 9508.

<a id="trigger-095ab66c"></a>

### 267. PP3_Is_Neutral - 095AB66C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP3_Is_America (095AB94C)](#trigger-095ab94c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 395 (global list position: Park Bench (CAPARK05)). A map-local type-list change can affect index interpretation.
2. local flag 41 (Lost_Tech03_Neut) is set.

Flag writers in this mission: clear local flag 41 (Lost_Tech03_Neut) at [PP3_Is_Neutral (095AB66C)](#trigger-095ab66c); set local flag 41 (Lost_Tech03_Neut) at [PP3_Not_Neutral (095AAC9C)](#trigger-095aac9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 41 (Lost_Tech03_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8837, Events line 9173, Actions line 9509.

<a id="trigger-095ab38c"></a>

### 268. PP3_Not_America - 095AB38C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP3_Is_Neutral (095AB66C)](#trigger-095ab66c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 395 (global list position: Park Bench (CAPARK05)). A map-local type-list change can affect index interpretation.
2. local flag 35 (Lost_Tech03_USA) is clear.

Flag writers in this mission: clear local flag 35 (Lost_Tech03_USA) at [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc); clear local flag 35 (Lost_Tech03_USA) at [PP3_Is_America (095AB94C)](#trigger-095ab94c); set local flag 35 (Lost_Tech03_USA) at [PP3_Not_America (095AB38C)](#trigger-095ab38c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 35 (Lost_Tech03_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8838, Events line 9174, Actions line 9510.

<a id="trigger-095aac9c"></a>

### 269. PP3_Not_Neutral - 095AAC9C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP3_Not_America (095AB38C)](#trigger-095ab38c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 395 (global list position: Park Bench (CAPARK05)). A map-local type-list change can affect index interpretation.
2. local flag 41 (Lost_Tech03_Neut) is clear.

Flag writers in this mission: clear local flag 41 (Lost_Tech03_Neut) at [PP3_Is_Neutral (095AB66C)](#trigger-095ab66c); set local flag 41 (Lost_Tech03_Neut) at [PP3_Not_Neutral (095AAC9C)](#trigger-095aac9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 41 (Lost_Tech03_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8839, Events line 9175, Actions line 9511.

<a id="trigger-095aa92c"></a>

### 270. PP4_Is_America - 095AA92C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_PlayerAttack (099A714C)](#trigger-099a714c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 396 (global list position: Park Bench (CAPARK06)). A map-local type-list change can affect index interpretation.
2. local flag 36 (Lost_Tech04_USA) is set.

Flag writers in this mission: clear local flag 36 (Lost_Tech04_USA) at [PP4_Entered (0BAAD22C)](#trigger-0baad22c); clear local flag 36 (Lost_Tech04_USA) at [PP4_Is_America (095AA92C)](#trigger-095aa92c); set local flag 36 (Lost_Tech04_USA) at [PP4_Not_America (095AA36C)](#trigger-095aa36c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 36 (Lost_Tech04_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8840, Events line 9176, Actions line 9512.

<a id="trigger-095aa64c"></a>

### 271. PP4_Is_Neutral - 095AA64C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_Is_America (095AA92C)](#trigger-095aa92c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 396 (global list position: Park Bench (CAPARK06)). A map-local type-list change can affect index interpretation.
2. local flag 42 (Lost_Tech04_Neut) is set.

Flag writers in this mission: clear local flag 42 (Lost_Tech04_Neut) at [PP4_Is_Neutral (095AA64C)](#trigger-095aa64c); set local flag 42 (Lost_Tech04_Neut) at [PP4_Not_Neutral (095A9CFC)](#trigger-095a9cfc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 42 (Lost_Tech04_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8841, Events line 9177, Actions line 9513.

<a id="trigger-095aa36c"></a>

### 272. PP4_Not_America - 095AA36C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_Is_Neutral (095AA64C)](#trigger-095aa64c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 396 (global list position: Park Bench (CAPARK06)). A map-local type-list change can affect index interpretation.
2. local flag 36 (Lost_Tech04_USA) is clear.

Flag writers in this mission: clear local flag 36 (Lost_Tech04_USA) at [PP4_Entered (0BAAD22C)](#trigger-0baad22c); clear local flag 36 (Lost_Tech04_USA) at [PP4_Is_America (095AA92C)](#trigger-095aa92c); set local flag 36 (Lost_Tech04_USA) at [PP4_Not_America (095AA36C)](#trigger-095aa36c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 36 (Lost_Tech04_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8842, Events line 9178, Actions line 9514.

<a id="trigger-095a9cfc"></a>

### 273. PP4_Not_Neutral - 095A9CFC

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_Not_America (095AA36C)](#trigger-095aa36c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 396 (global list position: Park Bench (CAPARK06)). A map-local type-list change can affect index interpretation.
2. local flag 42 (Lost_Tech04_Neut) is clear.

Flag writers in this mission: clear local flag 42 (Lost_Tech04_Neut) at [PP4_Is_Neutral (095AA64C)](#trigger-095aa64c); set local flag 42 (Lost_Tech04_Neut) at [PP4_Not_Neutral (095A9CFC)](#trigger-095a9cfc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 42 (Lost_Tech04_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8843, Events line 9179, Actions line 9515.

<a id="trigger-095a998c"></a>

### 274. PP5_Is_America - 095A998C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP5_PlayerAttack (099A436C)](#trigger-099a436c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 397 (global list position: Mini Mall (CALA14)). A map-local type-list change can affect index interpretation.
2. local flag 37 (Lost_Tech05_USA) is set.

Flag writers in this mission: clear local flag 37 (Lost_Tech05_USA) at [PP5_Entered (0BAAE54C)](#trigger-0baae54c); clear local flag 37 (Lost_Tech05_USA) at [PP5_Is_America (095A998C)](#trigger-095a998c); set local flag 37 (Lost_Tech05_USA) at [PP5_Not_America (095A93CC)](#trigger-095a93cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 37 (Lost_Tech05_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8844, Events line 9180, Actions line 9516.

<a id="trigger-095a96ac"></a>

### 275. PP5_Is_Neutral - 095A96AC

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP5_Is_America (095A998C)](#trigger-095a998c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 397 (global list position: Mini Mall (CALA14)). A map-local type-list change can affect index interpretation.
2. local flag 43 (Lost_Tech05_Neut) is set.

Flag writers in this mission: clear local flag 43 (Lost_Tech05_Neut) at [PP5_Is_Neutral (095A96AC)](#trigger-095a96ac); set local flag 43 (Lost_Tech05_Neut) at [PP5_Not_Neutral (095B6F3C)](#trigger-095b6f3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 43 (Lost_Tech05_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8845, Events line 9181, Actions line 9517.

<a id="trigger-095a93cc"></a>

### 276. PP5_Not_America - 095A93CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP5_Is_Neutral (095A96AC)](#trigger-095a96ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 397 (global list position: Mini Mall (CALA14)). A map-local type-list change can affect index interpretation.
2. local flag 37 (Lost_Tech05_USA) is clear.

Flag writers in this mission: clear local flag 37 (Lost_Tech05_USA) at [PP5_Entered (0BAAE54C)](#trigger-0baae54c); clear local flag 37 (Lost_Tech05_USA) at [PP5_Is_America (095A998C)](#trigger-095a998c); set local flag 37 (Lost_Tech05_USA) at [PP5_Not_America (095A93CC)](#trigger-095a93cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 37 (Lost_Tech05_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8846, Events line 9182, Actions line 9518.

<a id="trigger-095b6f3c"></a>

### 277. PP5_Not_Neutral - 095B6F3C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP5_Not_America (095A93CC)](#trigger-095a93cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 397 (global list position: Mini Mall (CALA14)). A map-local type-list change can affect index interpretation.
2. local flag 43 (Lost_Tech05_Neut) is clear.

Flag writers in this mission: clear local flag 43 (Lost_Tech05_Neut) at [PP5_Is_Neutral (095A96AC)](#trigger-095a96ac); set local flag 43 (Lost_Tech05_Neut) at [PP5_Not_Neutral (095B6F3C)](#trigger-095b6f3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 43 (Lost_Tech05_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8847, Events line 9183, Actions line 9519.

<a id="trigger-095b688c"></a>

### 278. PP6_Is_America - 095B688C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP6_PlayerAttack (099A0F3C)](#trigger-099a0f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 398 (global list position: Mini Mall (CALA15)). A map-local type-list change can affect index interpretation.
2. local flag 38 (Lost_Tech06_USA) is set.

Flag writers in this mission: clear local flag 38 (Lost_Tech06_USA) at [PP6_Entered (0BAAE37C)](#trigger-0baae37c); clear local flag 38 (Lost_Tech06_USA) at [PP6_Is_America (095B688C)](#trigger-095b688c); set local flag 38 (Lost_Tech06_USA) at [PP6_Not_America (095B62CC)](#trigger-095b62cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 38 (Lost_Tech06_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8848, Events line 9184, Actions line 9520.

<a id="trigger-095b65ac"></a>

### 279. PP6_Is_Neutral - 095B65AC

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP6_Is_America (095B688C)](#trigger-095b688c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 398 (global list position: Mini Mall (CALA15)). A map-local type-list change can affect index interpretation.
2. local flag 44 (Lost_Tech06_Neut) is set.

Flag writers in this mission: clear local flag 44 (Lost_Tech06_Neut) at [PP6_Is_Neutral (095B65AC)](#trigger-095b65ac); set local flag 44 (Lost_Tech06_Neut) at [PP6_Not_Neutral (095B2E6C)](#trigger-095b2e6c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 44 (Lost_Tech06_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8849, Events line 9185, Actions line 9521.

<a id="trigger-095b62cc"></a>

### 280. PP6_Not_America - 095B62CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP6_Is_Neutral (095B65AC)](#trigger-095b65ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 398 (global list position: Mini Mall (CALA15)). A map-local type-list change can affect index interpretation.
2. local flag 38 (Lost_Tech06_USA) is clear.

Flag writers in this mission: clear local flag 38 (Lost_Tech06_USA) at [PP6_Entered (0BAAE37C)](#trigger-0baae37c); clear local flag 38 (Lost_Tech06_USA) at [PP6_Is_America (095B688C)](#trigger-095b688c); set local flag 38 (Lost_Tech06_USA) at [PP6_Not_America (095B62CC)](#trigger-095b62cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 38 (Lost_Tech06_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8850, Events line 9186, Actions line 9522.

<a id="trigger-095b2e6c"></a>

### 281. PP6_Not_Neutral - 095B2E6C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP6_Not_America (095B62CC)](#trigger-095b62cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 398 (global list position: Mini Mall (CALA15)). A map-local type-list change can affect index interpretation.
2. local flag 44 (Lost_Tech06_Neut) is clear.

Flag writers in this mission: clear local flag 44 (Lost_Tech06_Neut) at [PP6_Is_Neutral (095B65AC)](#trigger-095b65ac); set local flag 44 (Lost_Tech06_Neut) at [PP6_Not_Neutral (095B2E6C)](#trigger-095b2e6c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 44 (Lost_Tech06_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8851, Events line 9187, Actions line 9523.

<a id="trigger-095b2a5c"></a>

### 282. PP7_Is_America - 095B2A5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP7_PlayerAttack (099A0A6C)](#trigger-099a0a6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 399 (global list position: Bunker (CABUNK03)). A map-local type-list change can affect index interpretation.
2. local flag 39 (Lost_Tech07_USA) is set.

Flag writers in this mission: clear local flag 39 (Lost_Tech07_USA) at [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); clear local flag 39 (Lost_Tech07_USA) at [PP7_Is_America (095B2A5C)](#trigger-095b2a5c); set local flag 39 (Lost_Tech07_USA) at [PP7_Not_America (095B249C)](#trigger-095b249c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 39 (Lost_Tech07_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8852, Events line 9188, Actions line 9524.

<a id="trigger-095b277c"></a>

### 283. PP7_Is_Neutral - 095B277C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP7_Is_America (095B2A5C)](#trigger-095b2a5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 399 (global list position: Bunker (CABUNK03)). A map-local type-list change can affect index interpretation.
2. local flag 45 (Lost_Tech07_Neut) is set.

Flag writers in this mission: clear local flag 45 (Lost_Tech07_Neut) at [PP7_Is_Neutral (095B277C)](#trigger-095b277c); set local flag 45 (Lost_Tech07_Neut) at [PP7_Not_Neutral (095B21BC)](#trigger-095b21bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 45 (Lost_Tech07_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8853, Events line 9189, Actions line 9525.

<a id="trigger-095b249c"></a>

### 284. PP7_Not_America - 095B249C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP7_Is_Neutral (095B277C)](#trigger-095b277c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 399 (global list position: Bunker (CABUNK03)). A map-local type-list change can affect index interpretation.
2. local flag 39 (Lost_Tech07_USA) is clear.

Flag writers in this mission: clear local flag 39 (Lost_Tech07_USA) at [PP7_Entered (0BFCA59C)](#trigger-0bfca59c); clear local flag 39 (Lost_Tech07_USA) at [PP7_Is_America (095B2A5C)](#trigger-095b2a5c); set local flag 39 (Lost_Tech07_USA) at [PP7_Not_America (095B249C)](#trigger-095b249c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 39 (Lost_Tech07_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8854, Events line 9190, Actions line 9526.

<a id="trigger-095b21bc"></a>

### 285. PP7_Not_Neutral - 095B21BC

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP7_Not_America (095B249C)](#trigger-095b249c).

Attached scope: CAPOWR07, owner PowerHouse, cell (125, 83), tag 0BFCA4BC, persistence mode 2.

**Wait for the recorded events:**

1. Building does not exist: type index 399 (global list position: Bunker (CABUNK03)). A map-local type-list change can affect index interpretation.
2. local flag 45 (Lost_Tech07_Neut) is clear.

Flag writers in this mission: clear local flag 45 (Lost_Tech07_Neut) at [PP7_Is_Neutral (095B277C)](#trigger-095b277c); set local flag 45 (Lost_Tech07_Neut) at [PP7_Not_Neutral (095B21BC)](#trigger-095b21bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 45 (Lost_Tech07_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8855, Events line 9191, Actions line 9527.

<a id="trigger-095b0d4c"></a>

### 286. PP8_Is_America - 095B0D4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP8_PlayerAttack (099A067C)](#trigger-099a067c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 409. A map-local type-list change can affect index interpretation.
2. local flag 40 (Lost_Tech08_USA) is set.

Flag writers in this mission: clear local flag 40 (Lost_Tech08_USA) at [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c); clear local flag 40 (Lost_Tech08_USA) at [PP8_Is_America (095B0D4C)](#trigger-095b0d4c); set local flag 40 (Lost_Tech08_USA) at [PP8_Not_America (095B5C5C)](#trigger-095b5c5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 40 (Lost_Tech08_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8856, Events line 9192, Actions line 9528.

<a id="trigger-095b5f3c"></a>

### 287. PP8_Is_Neutral - 095B5F3C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP8_Is_America (095B0D4C)](#trigger-095b0d4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 400 (global list position: Bunker (CABUNK04)). A map-local type-list change can affect index interpretation.
2. local flag 46 (Lost_Tech08_Neut) is set.

Flag writers in this mission: clear local flag 46 (Lost_Tech08_Neut) at [PP8_Is_Neutral (095B5F3C)](#trigger-095b5f3c); set local flag 46 (Lost_Tech08_Neut) at [PP8_Not_Neutral (095B597C)](#trigger-095b597c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 46 (Lost_Tech08_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8857, Events line 9193, Actions line 9529.

<a id="trigger-095b5c5c"></a>

### 288. PP8_Not_America - 095B5C5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP8_Is_Neutral (095B5F3C)](#trigger-095b5f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 400 (global list position: Bunker (CABUNK04)). A map-local type-list change can affect index interpretation.
2. local flag 40 (Lost_Tech08_USA) is clear.

Flag writers in this mission: clear local flag 40 (Lost_Tech08_USA) at [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c); clear local flag 40 (Lost_Tech08_USA) at [PP8_Is_America (095B0D4C)](#trigger-095b0d4c); set local flag 40 (Lost_Tech08_USA) at [PP8_Not_America (095B5C5C)](#trigger-095b5c5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 40 (Lost_Tech08_USA).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8858, Events line 9194, Actions line 9530.

<a id="trigger-095b597c"></a>

### 289. PP8_Not_Neutral - 095B597C

Owner reference: PowerHouse Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP8_Not_America (095B5C5C)](#trigger-095b5c5c).

Attached scope: CAPOWR08, owner PowerHouse, cell (125, 81), tag 0BFCDB9C, persistence mode 2.

**Wait for the recorded events:**

1. Building does not exist: type index 409. A map-local type-list change can affect index interpretation.
2. local flag 46 (Lost_Tech08_Neut) is clear.

Flag writers in this mission: clear local flag 46 (Lost_Tech08_Neut) at [PP8_Is_Neutral (095B5F3C)](#trigger-095b5f3c); set local flag 46 (Lost_Tech08_Neut) at [PP8_Not_Neutral (095B597C)](#trigger-095b597c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 46 (Lost_Tech08_Neut).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8859, Events line 9195, Actions line 9531.

<a id="trigger-0930139c"></a>

### 290. Nuke_Plant_Gone - 0930139C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Nuclear Reactor (NANRCT), owner Confederation, cell (55, 72), tag 09304F4C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.
2. Destroyed by anything. See attached-object/cell scope below.
3. local flag 3 (Time_Warp) is clear.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 48 (Nuke_Destroyed).
2. Disable [Nuke_Plant_Gone (0930139C)](#trigger-0930139c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8860, Events line 9196, Actions line 9532.

<a id="trigger-096e1f3c"></a>

### 291. Player_Has_Plant1 - 096E1F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 402 (global list position: US Flag (CALUNR02)). A map-local type-list change can affect index interpretation.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 49 (Player_Has_Plant).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8861, Events line 9197, Actions line 9533.

<a id="trigger-096e125c"></a>

### 292. Player_Has_Plant2 - 096E125C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Has_Plant1 (096E1F3C)](#trigger-096e1f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 403. A map-local type-list change can affect index interpretation.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 49 (Player_Has_Plant).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8862, Events line 9198, Actions line 9534.

<a id="trigger-096e0d8c"></a>

### 293. Player_Has_Plant3 - 096E0D8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Has_Plant2 (096E125C)](#trigger-096e125c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 404. A map-local type-list change can affect index interpretation.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 49 (Player_Has_Plant).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8863, Events line 9199, Actions line 9535.

<a id="trigger-096e0aac"></a>

### 294. Player_Has_Plant4 - 096E0AAC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Has_Plant3 (096E0D8C)](#trigger-096e0d8c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 405. A map-local type-list change can affect index interpretation.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 49 (Player_Has_Plant).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8864, Events line 9200, Actions line 9536.

<a id="trigger-096e07cc"></a>

### 295. Player_Has_Plant5 - 096E07CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Has_Plant4 (096E0AAC)](#trigger-096e0aac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 406. A map-local type-list change can affect index interpretation.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 49 (Player_Has_Plant).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8865, Events line 9201, Actions line 9537.

<a id="trigger-096e04ec"></a>

### 296. Player_Has_Plant6 - 096E04EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Has_Plant5 (096E07CC)](#trigger-096e07cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 407. A map-local type-list change can affect index interpretation.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 49 (Player_Has_Plant).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8866, Events line 9202, Actions line 9538.

<a id="trigger-096e020c"></a>

### 297. Player_Has_Plant7 - 096E020C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Has_Plant6 (096E04EC)](#trigger-096e04ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 408. A map-local type-list change can affect index interpretation.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 49 (Player_Has_Plant).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8867, Events line 9203, Actions line 9539.

<a id="trigger-096e2ddc"></a>

### 298. Player_Has_Plant8 - 096E2DDC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player_Has_Plant7 (096E020C)](#trigger-096e020c).

Attached scope: tag definitions 096E134C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 409. A map-local type-list change can affect index interpretation.
2. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 49 (Player_Has_Plant).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8868, Events line 9204, Actions line 9540.

<a id="trigger-08d5f24c"></a>

### 299. Cannon1_Gone - 08D5F24C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Return_Cannons1 (043808CC)](#trigger-043808cc).

Attached scope: Grand Cannon (GTGCAN), owner Americans, cell (80, 105), tag 08A9AACC, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 50 (Cannon1_Gone).
2. Disable [Cannon1_Gone (08D5F24C)](#trigger-08d5f24c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8869, Events line 9205, Actions line 9541.

<a id="trigger-08d5de6c"></a>

### 300. Cannon2_Gone - 08D5DE6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Return_Cannons2 (043772BC)](#trigger-043772bc).

Attached scope: Grand Cannon (GTGCAN), owner Americans, cell (83, 105), tag 08A9A9EC, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 51 (Cannon2_Gone).
2. Disable [Cannon2_Gone (08D5DE6C)](#trigger-08d5de6c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8870, Events line 9206, Actions line 9542.

<a id="trigger-08d5db4c"></a>

### 301. Cannon3_Gone - 08D5DB4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Return_Cannons3 (04378F3C)](#trigger-04378f3c).

Attached scope: Grand Cannon (GTGCAN), owner Americans, cell (77, 93), tag 08A9A90C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 52 (Cannon3_Gone).
2. Disable [Cannon3_Gone (08D5DB4C)](#trigger-08d5db4c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8871, Events line 9207, Actions line 9543.

<a id="trigger-08d5d82c"></a>

### 302. Cannon4_Gone - 08D5D82C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Return_Cannons4 (0438076C)](#trigger-0438076c).

Attached scope: Grand Cannon (GTGCAN), owner Americans, cell (81, 97), tag 08A9A82C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 53 (Cannon4_Gone).
2. Disable [Cannon4_Gone (08D5D82C)](#trigger-08d5d82c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8872, Events line 9208, Actions line 9544.

<a id="trigger-08e56b3c"></a>

### 303. Barracks_Gone - 08E56B3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Engineer_Check (08E568DC)](#trigger-08e568dc).
2. Disable [Barracks_Gone (08E56B3C)](#trigger-08e56b3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8873, Events line 9209, Actions line 9545.

<a id="trigger-08e568dc"></a>

### 304. Engineer_Check - 08E568DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Barracks_Gone (08E56B3C)](#trigger-08e56b3c).

Incoming activation links: enable from [Barracks_Gone (08E56B3C)](#trigger-08e56b3c); enable from [Engineers_Arrived (090AB04C)](#trigger-090ab04c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Time_Warp) is clear.
2. Low Power: owner selector 0 (country/type AMERICANS; placed owner Americans).
3. No instances of Engineer (ENGINEER) exist on the map, under this event's ownership scope.

Flag writers in this mission: set local flag 3 (Time_Warp) at [Play_Movies (0899832C)](#trigger-0899832c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Engineers (0908B07C)](all01umd-teams.md#team-0908b07c).
2. Enable and reset applicable timers for [Engineers_Arrived (090AB04C)](#trigger-090ab04c).
3. Disable [Engineer_Check (08E568DC)](#trigger-08e568dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8874, Events line 9210, Actions line 9546.

<a id="trigger-090ab04c"></a>

### 305. Engineers_Arrived - 090AB04C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Engineer_Check (08E568DC)](#trigger-08e568dc).

Incoming activation links: enable from [Engineer_Check (08E568DC)](#trigger-08e568dc).

Attached scope: Allied Barracks (GAPILE), owner Americans, cell (97, 105), tag 08E569CC, persistence mode 2.

**Wait for the recorded events:**

1. local flag 54 (Engineers_Landed) is set.

Flag writers in this mission: clear local flag 54 (Engineers_Landed) at [Engineers_Arrived (090AB04C)](#trigger-090ab04c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 54 (Engineers_Landed).
2. Create radar-event marker type 2 at waypoint 142 (cell 88, 105).
3. Play voice notification EVA_ReinforcementsHaveArrived.
4. Enable and reset applicable timers for [Engineer_Check (08E568DC)](#trigger-08e568dc).
5. Disable [Engineers_Arrived (090AB04C)](#trigger-090ab04c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8875, Events line 9211, Actions line 9547.

<a id="trigger-07adf47c"></a>

### 306. Start_ZC_EE_Patrol - 07ADF47C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07AD8ADC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_CityP1 (0AEB2EFC)](all01umd-teams.md#team-0aeb2efc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8876, Events line 9212, Actions line 9548.

<a id="trigger-05eff13c"></a>

### 307. Start_AB_GX_Patrol - 05EFF13C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05EF8A4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TEAM_CityP5 (0AEB564C)](all01umd-teams.md#team-0aeb564c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8877, Events line 9213, Actions line 9549.

<a id="trigger-04ebcacc"></a>

### 308. LosingPP1_Easy - 04EBCACC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PP1_Check_Easy (04EBA4DC)](#trigger-04eba4dc); enable from [PP2_Check_Easy (04EBBCBC)](#trigger-04ebbcbc); enable from [PP3_Check_Easy (04EBBBCC)](#trigger-04ebbbcc); enable from [PP4_Check_Easy (04E95DAC)](#trigger-04e95dac); enable from [PP5_Check_Easy (04E95CBC)](#trigger-04e95cbc); enable from [PP6_Check_Easy (04EC0C5C)](#trigger-04ec0c5c); enable from [PP7_Check_Easy (04EC0F3C)](#trigger-04ec0f3c); enable from [PP8_Check_Easy (04EC63AC)](#trigger-04ec63ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 55 (LostPP1_Easy) is clear.

Flag writers in this mission: set local flag 55 (LostPP1_Easy) at [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).
2. Set local flag 55 (LostPP1_Easy).
3. Disable [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8878, Events line 9214, Actions line 9550.

<a id="trigger-04ebc8fc"></a>

### 309. LostPP1_Easy - 04EBC8FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).

Incoming activation links: enable from [PP1_Check_Easy (04EBA4DC)](#trigger-04eba4dc); enable from [PP2_Check_Easy (04EBBCBC)](#trigger-04ebbcbc); enable from [PP3_Check_Easy (04EBBBCC)](#trigger-04ebbbcc); enable from [PP4_Check_Easy (04E95DAC)](#trigger-04e95dac); enable from [PP5_Check_Easy (04E95CBC)](#trigger-04e95cbc); enable from [PP6_Check_Easy (04EC0C5C)](#trigger-04ec0c5c); enable from [PP7_Check_Easy (04EC0F3C)](#trigger-04ec0f3c); enable from [PP8_Check_Easy (04EC63AC)](#trigger-04ec63ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 55 (LostPP1_Easy) is set.

Flag writers in this mission: set local flag 55 (LostPP1_Easy) at [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP2_Easy (04EBB62C)](#trigger-04ebb62c).
2. Enable and reset applicable timers for [LostPP2_Easy (04EB9BDC)](#trigger-04eb9bdc).
3. Disable [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8879, Events line 9215, Actions line 9551.

<a id="trigger-04ebb62c"></a>

### 310. LosingPP2_Easy - 04EBB62C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).

Incoming activation links: enable from [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 56 (LostPP2_Easy) is clear.
2. local flag 55 (LostPP1_Easy) is set.

Flag writers in this mission: set local flag 56 (LostPP2_Easy) at [LosingPP2_Easy (04EBB62C)](#trigger-04ebb62c); set local flag 55 (LostPP1_Easy) at [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [LostPP2_Easy (04EB9BDC)](#trigger-04eb9bdc).
2. Set local flag 56 (LostPP2_Easy).
3. Disable [LosingPP2_Easy (04EBB62C)](#trigger-04ebb62c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8880, Events line 9216, Actions line 9552.

<a id="trigger-04eb9bdc"></a>

### 311. LostPP2_Easy - 04EB9BDC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LosingPP7_Easy (04EB9CCC)](#trigger-04eb9ccc).

Incoming activation links: enable from [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 56 (LostPP2_Easy) is set.

Flag writers in this mission: set local flag 56 (LostPP2_Easy) at [LosingPP2_Easy (04EBB62C)](#trigger-04ebb62c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP3_Easy (04EBB53C)](#trigger-04ebb53c).
2. Enable and reset applicable timers for [LostPP3_Easy (04EB9AEC)](#trigger-04eb9aec).
3. Disable [LostPP2_Easy (04EB9BDC)](#trigger-04eb9bdc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8881, Events line 9217, Actions line 9553.

<a id="trigger-04eb9ccc"></a>

### 312. LosingPP7_Easy - 04EB9CCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LosingPP6_Easy (04EB9DBC)](#trigger-04eb9dbc).

Incoming activation links: enable from [LostPP6_Easy (04EB981C)](#trigger-04eb981c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 61 (LostPP7_Easy) is clear.
2. local flag 60 (LostPP6_Easy) is set.

Flag writers in this mission: set local flag 61 (LostPP7_Easy) at [LosingPP7_Easy (04EB9CCC)](#trigger-04eb9ccc); set local flag 60 (LostPP6_Easy) at [LosingPP6_Easy (04EB9DBC)](#trigger-04eb9dbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [LostPP7_Easy (04EB972C)](#trigger-04eb972c).
2. Set local flag 61 (LostPP7_Easy).
3. Enable and reset applicable timers for [Player_Lost (06178D0C)](#trigger-06178d0c).
4. Disable [LosingPP7_Easy (04EB9CCC)](#trigger-04eb9ccc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8882, Events line 9218, Actions line 9554.

<a id="trigger-04ebb53c"></a>

### 313. LosingPP3_Easy - 04EBB53C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LosingPP2_Easy (04EBB62C)](#trigger-04ebb62c).

Incoming activation links: enable from [LostPP2_Easy (04EB9BDC)](#trigger-04eb9bdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 57 (LostPP3_Easy) is clear.
2. local flag 56 (LostPP2_Easy) is set.

Flag writers in this mission: set local flag 57 (LostPP3_Easy) at [LosingPP3_Easy (04EBB53C)](#trigger-04ebb53c); set local flag 56 (LostPP2_Easy) at [LosingPP2_Easy (04EBB62C)](#trigger-04ebb62c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [LostPP3_Easy (04EB9AEC)](#trigger-04eb9aec).
2. Set local flag 57 (LostPP3_Easy).
3. Disable [LosingPP3_Easy (04EBB53C)](#trigger-04ebb53c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8883, Events line 9219, Actions line 9555.

<a id="trigger-04eb9aec"></a>

### 314. LostPP3_Easy - 04EB9AEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LostPP2_Easy (04EB9BDC)](#trigger-04eb9bdc).

Incoming activation links: enable from [LostPP2_Easy (04EB9BDC)](#trigger-04eb9bdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 57 (LostPP3_Easy) is set.

Flag writers in this mission: set local flag 57 (LostPP3_Easy) at [LosingPP3_Easy (04EBB53C)](#trigger-04ebb53c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP4_Easy (04EBB44C)](#trigger-04ebb44c).
2. Enable and reset applicable timers for [LostPP4_Easy (04EB99FC)](#trigger-04eb99fc).
3. Disable [LostPP3_Easy (04EB9AEC)](#trigger-04eb9aec).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8884, Events line 9220, Actions line 9556.

<a id="trigger-04eb9dbc"></a>

### 315. LosingPP6_Easy - 04EB9DBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LosingPP5_Easy (04EBB35C)](#trigger-04ebb35c).

Incoming activation links: enable from [LostPP5_Easy (04EB990C)](#trigger-04eb990c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 60 (LostPP6_Easy) is clear.
2. local flag 59 (LostPP5_Easy) is set.

Flag writers in this mission: set local flag 60 (LostPP6_Easy) at [LosingPP6_Easy (04EB9DBC)](#trigger-04eb9dbc); set local flag 59 (LostPP5_Easy) at [LosingPP5_Easy (04EBB35C)](#trigger-04ebb35c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [LostPP6_Easy (04EB981C)](#trigger-04eb981c).
2. Set local flag 60 (LostPP6_Easy).
3. Disable [LosingPP6_Easy (04EB9DBC)](#trigger-04eb9dbc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8885, Events line 9221, Actions line 9557.

<a id="trigger-04eb972c"></a>

### 316. LostPP7_Easy - 04EB972C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LostPP6_Easy (04EB981C)](#trigger-04eb981c).

Incoming activation links: enable from [LostPP6_Easy (04EB981C)](#trigger-04eb981c).

Attached scope: tag definitions 04EBC9EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 61 (LostPP7_Easy) is set.

Flag writers in this mission: set local flag 61 (LostPP7_Easy) at [LosingPP7_Easy (04EB9CCC)](#trigger-04eb9ccc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [LosingPP7_Easy (04EB9CCC)](#trigger-04eb9ccc).
2. Disable [LostPP7_Easy (04EB972C)](#trigger-04eb972c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8886, Events line 9222, Actions line 9558.

<a id="trigger-04ebb44c"></a>

### 317. LosingPP4_Easy - 04EBB44C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LosingPP3_Easy (04EBB53C)](#trigger-04ebb53c).

Incoming activation links: enable from [LostPP3_Easy (04EB9AEC)](#trigger-04eb9aec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 58 (LostPP4_Easy) is clear.
2. local flag 57 (LostPP3_Easy) is set.

Flag writers in this mission: set local flag 58 (LostPP4_Easy) at [LosingPP4_Easy (04EBB44C)](#trigger-04ebb44c); set local flag 57 (LostPP3_Easy) at [LosingPP3_Easy (04EBB53C)](#trigger-04ebb53c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [LostPP4_Easy (04EB99FC)](#trigger-04eb99fc).
2. Set local flag 58 (LostPP4_Easy).
3. Disable [LosingPP4_Easy (04EBB44C)](#trigger-04ebb44c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8887, Events line 9223, Actions line 9559.

<a id="trigger-04eb99fc"></a>

### 318. LostPP4_Easy - 04EB99FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LostPP3_Easy (04EB9AEC)](#trigger-04eb9aec).

Incoming activation links: enable from [LostPP3_Easy (04EB9AEC)](#trigger-04eb9aec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 58 (LostPP4_Easy) is set.

Flag writers in this mission: set local flag 58 (LostPP4_Easy) at [LosingPP4_Easy (04EBB44C)](#trigger-04ebb44c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP5_Easy (04EBB35C)](#trigger-04ebb35c).
2. Enable and reset applicable timers for [LostPP5_Easy (04EB990C)](#trigger-04eb990c).
3. Disable [LostPP4_Easy (04EB99FC)](#trigger-04eb99fc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8888, Events line 9224, Actions line 9560.

<a id="trigger-04ebb35c"></a>

### 319. LosingPP5_Easy - 04EBB35C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LosingPP4_Easy (04EBB44C)](#trigger-04ebb44c).

Incoming activation links: enable from [LostPP4_Easy (04EB99FC)](#trigger-04eb99fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 59 (LostPP5_Easy) is clear.
2. local flag 58 (LostPP4_Easy) is set.

Flag writers in this mission: set local flag 59 (LostPP5_Easy) at [LosingPP5_Easy (04EBB35C)](#trigger-04ebb35c); set local flag 58 (LostPP4_Easy) at [LosingPP4_Easy (04EBB44C)](#trigger-04ebb44c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [LostPP5_Easy (04EB990C)](#trigger-04eb990c).
2. Set local flag 59 (LostPP5_Easy).
3. Disable [LosingPP5_Easy (04EBB35C)](#trigger-04ebb35c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8889, Events line 9225, Actions line 9561.

<a id="trigger-04eb981c"></a>

### 320. LostPP6_Easy - 04EB981C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LostPP5_Easy (04EB990C)](#trigger-04eb990c).

Incoming activation links: enable from [LostPP5_Easy (04EB990C)](#trigger-04eb990c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 60 (LostPP6_Easy) is set.

Flag writers in this mission: set local flag 60 (LostPP6_Easy) at [LosingPP6_Easy (04EB9DBC)](#trigger-04eb9dbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP7_Easy (04EB9CCC)](#trigger-04eb9ccc).
2. Enable and reset applicable timers for [LostPP7_Easy (04EB972C)](#trigger-04eb972c).
3. Disable [LostPP6_Easy (04EB981C)](#trigger-04eb981c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8890, Events line 9226, Actions line 9562.

<a id="trigger-04eb990c"></a>

### 321. LostPP5_Easy - 04EB990C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LostPP4_Easy (04EB99FC)](#trigger-04eb99fc).

Incoming activation links: enable from [LostPP4_Easy (04EB99FC)](#trigger-04eb99fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 59 (LostPP5_Easy) is set.

Flag writers in this mission: set local flag 59 (LostPP5_Easy) at [LosingPP5_Easy (04EBB35C)](#trigger-04ebb35c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP6_Easy (04EB9DBC)](#trigger-04eb9dbc).
2. Enable and reset applicable timers for [LostPP6_Easy (04EB981C)](#trigger-04eb981c).
3. Disable [LostPP5_Easy (04EB990C)](#trigger-04eb990c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8891, Events line 9227, Actions line 9563.

<a id="trigger-04eba4dc"></a>

### 322. PP1_Check_Easy - 04EBA4DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable_EasyPP_Check (04EC206C)](#trigger-04ec206c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR01 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).
2. Enable and reset applicable timers for [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).
3. Disable [PP1_Check_Easy (04EBA4DC)](#trigger-04eba4dc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8892, Events line 9228, Actions line 9564.

<a id="trigger-04ebbcbc"></a>

### 323. PP2_Check_Easy - 04EBBCBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [PP1_Check_Easy (04EBA4DC)](#trigger-04eba4dc).

Incoming activation links: enable from [Enable_EasyPP_Check (04EC206C)](#trigger-04ec206c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR02 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).
2. Enable and reset applicable timers for [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).
3. Disable [PP2_Check_Easy (04EBBCBC)](#trigger-04ebbcbc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8893, Events line 9229, Actions line 9565.

<a id="trigger-04ebbbcc"></a>

### 324. PP3_Check_Easy - 04EBBBCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [PP2_Check_Easy (04EBBCBC)](#trigger-04ebbcbc).

Incoming activation links: enable from [Enable_EasyPP_Check (04EC206C)](#trigger-04ec206c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR03 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).
2. Enable and reset applicable timers for [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).
3. Disable [PP3_Check_Easy (04EBBBCC)](#trigger-04ebbbcc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8894, Events line 9230, Actions line 9566.

<a id="trigger-04e95dac"></a>

### 325. PP4_Check_Easy - 04E95DAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [PP3_Check_Easy (04EBBBCC)](#trigger-04ebbbcc).

Incoming activation links: enable from [Enable_EasyPP_Check (04EC206C)](#trigger-04ec206c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR04 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).
2. Enable and reset applicable timers for [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).
3. Disable [PP4_Check_Easy (04E95DAC)](#trigger-04e95dac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8895, Events line 9231, Actions line 9567.

<a id="trigger-04e95cbc"></a>

### 326. PP5_Check_Easy - 04E95CBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [PP4_Check_Easy (04E95DAC)](#trigger-04e95dac).

Incoming activation links: enable from [Enable_EasyPP_Check (04EC206C)](#trigger-04ec206c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR05 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).
2. Enable and reset applicable timers for [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).
3. Disable [PP5_Check_Easy (04E95CBC)](#trigger-04e95cbc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8896, Events line 9232, Actions line 9568.

<a id="trigger-04ec0c5c"></a>

### 327. PP6_Check_Easy - 04EC0C5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [PP5_Check_Easy (04E95CBC)](#trigger-04e95cbc).

Incoming activation links: enable from [Enable_EasyPP_Check (04EC206C)](#trigger-04ec206c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR06 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).
2. Enable and reset applicable timers for [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).
3. Disable [PP6_Check_Easy (04EC0C5C)](#trigger-04ec0c5c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8897, Events line 9233, Actions line 9569.

<a id="trigger-04ec0f3c"></a>

### 328. PP7_Check_Easy - 04EC0F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [PP6_Check_Easy (04EC0C5C)](#trigger-04ec0c5c).

Incoming activation links: enable from [Enable_EasyPP_Check (04EC206C)](#trigger-04ec206c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of CAPOWR07 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).
2. Enable and reset applicable timers for [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).
3. Disable [PP7_Check_Easy (04EC0F3C)](#trigger-04ec0f3c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8898, Events line 9234, Actions line 9570.

<a id="trigger-04ec63ac"></a>

### 329. PP8_Check_Easy - 04EC63AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [PP7_Check_Easy (04EC0F3C)](#trigger-04ec0f3c).

Incoming activation links: enable from [Enable_EasyPP_Check (04EC206C)](#trigger-04ec206c).

Attached scope: tag definitions 04EBA3FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of CAPOWR08 exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [LosingPP1_Easy (04EBCACC)](#trigger-04ebcacc).
2. Enable and reset applicable timers for [LostPP1_Easy (04EBC8FC)](#trigger-04ebc8fc).
3. Disable [PP8_Check_Easy (04EC63AC)](#trigger-04ec63ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8899, Events line 9235, Actions line 9571.

<a id="trigger-04ec206c"></a>

### 330. Enable_EasyPP_Check - 04EC206C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04EC569C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PP1_Check_Easy (04EBA4DC)](#trigger-04eba4dc).
2. Enable and reset applicable timers for [PP2_Check_Easy (04EBBCBC)](#trigger-04ebbcbc).
3. Enable and reset applicable timers for [PP3_Check_Easy (04EBBBCC)](#trigger-04ebbbcc).
4. Enable and reset applicable timers for [PP4_Check_Easy (04E95DAC)](#trigger-04e95dac).
5. Enable and reset applicable timers for [PP5_Check_Easy (04E95CBC)](#trigger-04e95cbc).
6. Enable and reset applicable timers for [PP6_Check_Easy (04EC0C5C)](#trigger-04ec0c5c).
7. Enable and reset applicable timers for [PP7_Check_Easy (04EC0F3C)](#trigger-04ec0f3c).
8. Enable and reset applicable timers for [PP8_Check_Easy (04EC63AC)](#trigger-04ec63ac).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8900, Events line 9236, Actions line 9572.

<a id="trigger-09178c4c"></a>

### 331. Start_PP3_Checks - 09178C4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP3_Not_Neutral (095AAC9C)](#trigger-095aac9c).

Attached scope: CAPOWR03, owner PowerHouse, cell (119, 146), tag 0BAAD31C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PP3_Destroyed (0BABB5DC)](#trigger-0babb5dc).
2. Enable and reset applicable timers for [PP3_Entered (0BAAD3FC)](#trigger-0baad3fc).
3. Disable [Start_PP3_Checks (09178C4C)](#trigger-09178c4c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8901, Events line 9237, Actions line 9573.

<a id="trigger-091786bc"></a>

### 332. Start_PP4_Check - 091786BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP4_Not_Neutral (095A9CFC)](#trigger-095a9cfc).

Attached scope: CAPOWR04, owner PowerHouse, cell (121, 146), tag 0BAAD14C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PP4_Destroyed (0BAC2A9C)](#trigger-0bac2a9c).
2. Enable and reset applicable timers for [PP4_Entered (0BAAD22C)](#trigger-0baad22c).
3. Disable [Start_PP4_Check (091786BC)](#trigger-091786bc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8902, Events line 9238, Actions line 9574.

<a id="trigger-091782cc"></a>

### 333. Start_PP5_Check - 091782CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP5_Not_Neutral (095B6F3C)](#trigger-095b6f3c).

Attached scope: CAPOWR05, owner PowerHouse, cell (153, 108), tag 0BAAE46C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PP5_Destroyed (0BAB8ACC)](#trigger-0bab8acc).
2. Enable and reset applicable timers for [PP5_Entered (0BAAE54C)](#trigger-0baae54c).
3. Disable [Start_PP5_Check (091782CC)](#trigger-091782cc).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8903, Events line 9239, Actions line 9575.

<a id="trigger-09179e6c"></a>

### 334. Start_PP6_Check - 09179E6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [PP6_Not_Neutral (095B2E6C)](#trigger-095b2e6c).

Attached scope: CAPOWR06, owner PowerHouse, cell (153, 106), tag 0BAAE29C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PP6_Destroyed (0BAB89DC)](#trigger-0bab89dc).
2. Enable and reset applicable timers for [PP6_Entered (0BAAE37C)](#trigger-0baae37c).
3. Enable and reset applicable timers for [PP7_Destroyed (0BAAC68C)](#trigger-0baac68c).
4. Enable and reset applicable timers for [PP7_Entered (0BFCA59C)](#trigger-0bfca59c).
5. Enable and reset applicable timers for [PP8_Destroyed (0BAAC59C)](#trigger-0baac59c).
6. Enable and reset applicable timers for [PP8_Entered (0BFCDC7C)](#trigger-0bfcdc7c).
7. Disable [Start_PP6_Check (09179E6C)](#trigger-09179e6c).

Source locator: mapsmd03.mix/all01umd.map; Triggers line 8904, Events line 9240, Actions line 9576.

[All team rosters and ordered plans](all01umd-teams.md) | [All mission overrides](all01umd-overrides.md)
