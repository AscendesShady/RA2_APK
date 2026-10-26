# Operation: Time Shift

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov01umd.map. **Effective extracted member:** mapsmd03.mix/sov01umd.map. **Trigger definitions:** 302.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov01umd-teams.md) | [All mission overrides](sov01umd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Russians |
| Theater | NEWURBAN |
| Map size | 0,0,58,140 |
| Visible local rectangle | 4,29,52,60 |
| Placed vehicles | 44 |
| Placed infantry | 23 |
| Placed structures | 155 |
| Placed aircraft | 0 |
| Team templates | 130 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 0 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 0 | Africans |
| 6 | Arabs | 0 | Arabs |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 250 | Russians |
| 9 | YuriCountry | 750 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 100 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |
| 14 | PowerHouse | 0 | PowerHouse Country |
| 15 | Soviet2House | 0 | Soviet2 Country |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Hover1_Unloaded,0 |
| 1 | Hover_2_Unloaded,0 |
| 2 | Hover_3_Unloaded,0 |
| 3 | Time_Warp,0 |
| 4 | Tanya_Dead,0 |
| 5 | Gave_PP_Brief,0 |
| 6 | Trans 1 Unloaded,0 |
| 7 | Trans 2 Unloaded,0 |
| 8 | Trans 3 Unloaded,0 |
| 9 | Trans 4 Unloaded,0 |
| 10 | Sub1 Dead,0 |
| 11 | Sub2 Dead,0 |
| 12 | Sub3 Dead,0 |
| 13 | Squid1 Dead,0 |
| 14 | Squid2 Dead,0 |
| 15 | Scorp1 Dead,0 |
| 16 | Scorp2 Dead,0 |
| 17 | Scorp3 Dead,0 |
| 18 | Scorp4 Dead,0 |
| 19 | Scorp5 Dead,0 |
| 20 | Dread1 Dead,0 |
| 21 | Dread2 Dead,0 |
| 22 | Dread3 Dead,0 |
| 23 | Boris Intro,0 |
| 24 | BorisDead,0 |
| 25 | BorisDeadAgain,0 |
| 26 | BorisTalks,0 |
| 27 | Grand Atk_Unloaded,0 |
| 28 | Statue Atk_Unloaded,0 |
| 29 | Park Atk_Unloaded,0 |
| 30 | Gas Atk_Unloaded,0 |
| 31 | NTime Atk_Unloaded,0 |
| 32 | STime Atk_Unloaded,0 |
| 33 | Grand Cap_Unloaded,0 |
| 34 | Statue Cap_Unloaded,0 |
| 35 | Park Cap_Unloaded,0 |
| 36 | Gas Cap_Unloaded,0 |
| 37 | NTime Cap_Unloaded,0 |
| 38 | STime Cap_Unloaded,0 |
| 39 | NoMoreCapTeams,0 |
| 40 | 1 PP Gone,0 |
| 41 | 2 PP Gone,0 |
| 42 | 3 PP Gone,0 |
| 43 | Player Reinforce 1 ,0 |
| 44 | Player Reinforce 2 ,0 |
| 45 | 1st Tanks Arrive,0 |
| 46 | Rhinos to Russia,0 |
| 47 | Conscripts to Russi,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [_End_Lose (06B602BC)](#trigger-06b602bc) | 15 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser. |
| [_End_Win (06B600EC)](#trigger-06b600ec) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner. |

## Every trigger, in file order

<a id="trigger-094b2a9c"></a>

### 1. SP1.2_Camera to CA - 094B2A9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 094B29BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 78 (cell 52, 91) with speed setting 1.
2. Enable and reset applicable timers for [SP1.8_Camera to CB (094BE2BC)](#trigger-094be2bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9367, Events line 9671, Actions line 9975.

<a id="trigger-094be2bc"></a>

### 2. SP1.8_Camera to CB - 094BE2BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.2_Camera to CA (094B2A9C)](#trigger-094b2a9c).

Attached scope: tag definitions 094BE0DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 79 (cell 63, 89) with speed setting 2.
2. Enable and reset applicable timers for [SP1.9_Target Ship (0D0E096C)](#trigger-0d0e096c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9368, Events line 9672, Actions line 9976.

<a id="trigger-0d0e096c"></a>

### 3. SP1.9_Target Ship - 0D0E096C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.8_Camera to CB (094BE2BC)](#trigger-094be2bc).

Attached scope: tag definitions 0D0E07DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP1.11_Target Cannon (0D0E024C)](#trigger-0d0e024c).
2. Create/recruit team [TM_Allies_Flash 1 Carrier (0D0F7CCC)](sov01umd-teams.md#team-0d0f7ccc).
3. Create/recruit team [TM_Allies_Flash 1 Carrier (0D0F7CCC)](sov01umd-teams.md#team-0d0f7ccc).
4. Create/recruit team [TM_Allies_Flash 1 Destroyer (0D0F667C)](sov01umd-teams.md#team-0d0f667c).
5. Create/recruit team [TM_Allies_Flash 1 Destroyer (0D0F667C)](sov01umd-teams.md#team-0d0f667c).
6. Create/recruit team [TM_Allies_Flash 1 Destroyer (0D0F667C)](sov01umd-teams.md#team-0d0f667c).
7. Display message “Objective 1: Destroy the Allied Navy and Grand Cannons.” (MISSION:Sov1Obj1).
8. Enable and reset applicable timers for [Text_Objective 1 (094D448C)](#trigger-094d448c).
9. Enable and reset applicable timers for [SP1.10_Audio_Objective1 (094C722C)](#trigger-094c722c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9369, Events line 9673, Actions line 9977.

<a id="trigger-0d0e024c"></a>

### 4. SP1.11_Target Cannon - 0D0E024C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.9_Target Ship (0D0E096C)](#trigger-0d0e096c).

Attached scope: tag definitions 0D0E016C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 483; location/duration field BH.
2. Play Anim At; main setting 483; location/duration field BI.
3. Enable and reset applicable timers for [SP1.12_Camera to CD (06B6F36C)](#trigger-06b6f36c).
4. Enable and reset applicable timers for [SP1.13_Anim_Arrow Loop1 (0D9BA33C)](#trigger-0d9ba33c).
5. Enable and reset applicable timers for [SP1.15_End_Arrow Loop1 (0D9BA16C)](#trigger-0d9ba16c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9370, Events line 9674, Actions line 9978.

<a id="trigger-094d448c"></a>

### 5. Text_Objective 1 - 094D448C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.9_Target Ship (0D0E096C)](#trigger-0d0e096c).

Attached scope: tag definitions 094920FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Destroy the Allied Navy and Grand Cannons.” (MISSION:Sov1Obj1).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9371, Events line 9675, Actions line 9979.

<a id="trigger-094c722c"></a>

### 6. SP1.10_Audio_Objective1 - 094C722C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.9_Target Ship (0D0E096C)](#trigger-0d0e096c).

Attached scope: tag definitions 094C422C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaNavalAttack.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9372, Events line 9676, Actions line 9980.

<a id="trigger-06b6f36c"></a>

### 7. SP1.12_Camera to CD - 06B6F36C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.11_Target Cannon (0D0E024C)](#trigger-0d0e024c).

Attached scope: tag definitions 06B6F28C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 81 (cell 58, 91) with speed setting 2.
2. Enable and reset applicable timers for [SP1.14_Unlock (0D0E418C)](#trigger-0d0e418c).
3. Supply reinforcement team [TM_Allies_1 Intruder_e (08FCE74C)](sov01umd-teams.md#team-08fce74c).
4. Supply reinforcement team [TM_Allies_1 Intruder_f (05D3B8BC)](sov01umd-teams.md#team-05d3b8bc).
5. Supply reinforcement team [TM_Allies_1 Intruder_g (05D3BB6C)](sov01umd-teams.md#team-05d3bb6c).
6. Supply reinforcement team [TM_Allies_1 Intruder_h (05D3878C)](sov01umd-teams.md#team-05d3878c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9373, Events line 9677, Actions line 9981.

<a id="trigger-0d9ba33c"></a>

### 8. SP1.13_Anim_Arrow Loop1 - 0D9BA33C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.11_Target Cannon (0D0E024C)](#trigger-0d0e024c).

Attached scope: tag definitions 0D9BA25C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 483; location/duration field BH.
2. Play Anim At; main setting 483; location/duration field BI.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9374, Events line 9678, Actions line 9982.

<a id="trigger-0d9ba16c"></a>

### 9. SP1.15_End_Arrow Loop1 - 0D9BA16C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.11_Target Cannon (0D0E024C)](#trigger-0d0e024c).

Attached scope: tag definitions 0D9BCF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [SP1.13_Anim_Arrow Loop1 (0D9BA33C)](#trigger-0d9ba33c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9375, Events line 9679, Actions line 9983.

<a id="trigger-0d0e418c"></a>

### 10. SP1.14_Unlock - 0D0E418C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.12_Camera to CD (06B6F36C)](#trigger-06b6f36c).

Attached scope: tag definitions 0D0E5F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Play voice notification EVA_BattlefieldControlOnline.
3. Enable and reset applicable timers for [SP1.16_Carrier Atk (094C5E4C)](#trigger-094c5e4c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9376, Events line 9680, Actions line 9984.

<a id="trigger-094c5e4c"></a>

### 11. SP1.16_Carrier Atk - 094C5E4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.14_Unlock (0D0E418C)](#trigger-0d0e418c).

Attached scope: tag definitions 094C5D6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TM_Allies_2 Carrier (0BCF57DC)](sov01umd-teams.md#team-0bcf57dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9377, Events line 9681, Actions line 9985.

<a id="trigger-0b8913ec"></a>

### 12. SP1.1_Subs move - 0B8913EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B89130C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Sub 1 (0C0A612C)](sov01umd-teams.md#team-0c0a612c).
2. Supply reinforcement team [TM_Sov_Sub 2 (0C0A790C)](sov01umd-teams.md#team-0c0a790c).
3. Supply reinforcement team [TM_Sov_Sub 3 (0C0A756C)](sov01umd-teams.md#team-0c0a756c).
4. Enable and reset applicable timers for [SP1.5_Squids move (0B890BCC)](#trigger-0b890bcc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9378, Events line 9682, Actions line 9986.

<a id="trigger-0b890bcc"></a>

### 13. SP1.5_Squids move - 0B890BCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.1_Subs move (0B8913EC)](#trigger-0b8913ec).

Attached scope: tag definitions 0B890AEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Squid 1 (0C0A71CC)](sov01umd-teams.md#team-0c0a71cc).
2. Supply reinforcement team [TM_Sov_Squid 2 (0C0A8B7C)](sov01umd-teams.md#team-0c0a8b7c).
3. Enable and reset applicable timers for [SP1.6_Scorps move (0B8906FC)](#trigger-0b8906fc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9379, Events line 9683, Actions line 9987.

<a id="trigger-0b8906fc"></a>

### 14. SP1.6_Scorps move - 0B8906FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.5_Squids move (0B890BCC)](#trigger-0b890bcc).

Attached scope: tag definitions 0B89061C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Sea Scorpion 2 (0C0A824C)](sov01umd-teams.md#team-0c0a824c).
2. Supply reinforcement team [TM_Sov_Sea Scorpion 3 (0C0A9C8C)](sov01umd-teams.md#team-0c0a9c8c).
3. Supply reinforcement team [TM_Sov_Sea Scorpion 4 (0C0A98EC)](sov01umd-teams.md#team-0c0a98ec).
4. Enable and reset applicable timers for [SP1.7_Dreads move (0B896E6C)](#trigger-0b896e6c).
5. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9380, Events line 9684, Actions line 9988.

<a id="trigger-0b896e6c"></a>

### 15. SP1.7_Dreads move - 0B896E6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.6_Scorps move (0B8906FC)](#trigger-0b8906fc).

Attached scope: tag definitions 0B896D8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Dreadnought 2 (0C04FEFC)](sov01umd-teams.md#team-0c04fefc).
2. Enable and reset applicable timers for [SP1.7a_Audio_Sub Select (088966DC)](#trigger-088966dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9381, Events line 9685, Actions line 9989.

<a id="trigger-088966dc"></a>

### 16. SP1.7a_Audio_Sub Select - 088966DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.7_Dreads move (0B896E6C)](#trigger-0b896e6c).

Attached scope: tag definitions 088965FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound TyphoonSubSelect.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9382, Events line 9686, Actions line 9990.

<a id="trigger-0bbefe3c"></a>

### 17. SP1.3a_Intruder_a move - 0BBEFE3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BBEFD5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Allies_1 Intruder_a (0881B38C)](sov01umd-teams.md#team-0881b38c).
2. Enable and reset applicable timers for [SP1.3b_Intruder_b move (094848DC)](#trigger-094848dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9383, Events line 9687, Actions line 9991.

<a id="trigger-094848dc"></a>

### 18. SP1.3b_Intruder_b move - 094848DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.3a_Intruder_a move (0BBEFE3C)](#trigger-0bbefe3c).

Attached scope: tag definitions 094823BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Allies_1 Intruder_b (07A2155C)](sov01umd-teams.md#team-07a2155c).
2. Enable and reset applicable timers for [SP1.3c_Intruder_c move (0948645C)](#trigger-0948645c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9384, Events line 9688, Actions line 9992.

<a id="trigger-0948645c"></a>

### 19. SP1.3c_Intruder_c move - 0948645C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.3b_Intruder_b move (094848DC)](#trigger-094848dc).

Attached scope: tag definitions 094849CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Allies_1 Intruder_c (07A2142C)](sov01umd-teams.md#team-07a2142c).
2. Enable and reset applicable timers for [SP1.3d_Intruder_d move (094822CC)](#trigger-094822cc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9385, Events line 9689, Actions line 9993.

<a id="trigger-094822cc"></a>

### 20. SP1.3d_Intruder_d move - 094822CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.3c_Intruder_c move (0948645C)](#trigger-0948645c).

Attached scope: tag definitions 09484E8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Allies_1 Intruder_d (07A21A6C)](sov01umd-teams.md#team-07a21a6c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9386, Events line 9690, Actions line 9994.

<a id="trigger-0b76df3c"></a>

### 21. _Setup_Soviet Mission 1 - 0B76DF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B76DE5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable player input.
2. Play voice notification EVA_EstablishBattlefieldControl.
3. Enable and reset applicable timers for [SP1.4_Audio_Sov01 Intro (0DD8E18C)](#trigger-0dd8e18c).
4. Supply reinforcement team [TM_Allies_2 Grizzly PQ->PR (0BD6841C)](sov01umd-teams.md#team-0bd6841c).
5. Supply reinforcement team [TM_Allies_2 Grizzly PS->PT (0B4FF03C)](sov01umd-teams.md#team-0b4ff03c).
6. Supply reinforcement team [TM_Allies_2 Grizzly PU->PV (0B4F889C)](sov01umd-teams.md#team-0b4f889c).
7. Supply reinforcement team [TM_Allies_2 Grizzly PW->PX (0B4F83FC)](sov01umd-teams.md#team-0b4f83fc).
8. Supply reinforcement team [TM_Allies_2 Grizzly PY->PZ (0B4FAC4C)](sov01umd-teams.md#team-0b4fac4c).
9. Supply reinforcement team [TM_Allies_2 Grizzly QA->QB (0B4FA76C)](sov01umd-teams.md#team-0b4fa76c).
10. Supply reinforcement team [TM_Allies_4 GI QC->QD->QE->QF (0B4FA0FC)](sov01umd-teams.md#team-0b4fa0fc).
11. Supply reinforcement team [TM_Allies_4 GI QG->QH (0B4F9BFC)](sov01umd-teams.md#team-0b4f9bfc).
12. Supply reinforcement team [TM_Allies_4 GI QI->QJ->QK->QL (0B4F979C)](sov01umd-teams.md#team-0b4f979c).
13. Supply reinforcement team [TM_Allies_4 GI QM->QN (0B4F923C)](sov01umd-teams.md#team-0b4f923c).
14. Supply reinforcement team [TM_Allies_4 GI QO->QP (0B4F904C)](sov01umd-teams.md#team-0b4f904c).
15. Supply reinforcement team [TM_Allies_4 GI QQ->QR (0B4FB95C)](sov01umd-teams.md#team-0b4fb95c).
16. Supply reinforcement team [TM_Allies_4 GI QS->QT (0B4FB4FC)](sov01umd-teams.md#team-0b4fb4fc).
17. Supply reinforcement team [TM_Allies_4 GI QU->QV->QW (0B4FB09C)](sov01umd-teams.md#team-0b4fb09c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9387, Events line 9691, Actions line 9995.

<a id="trigger-0dd8e18c"></a>

### 22. SP1.4_Audio_Sov01 Intro - 0DD8E18C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Setup_Soviet Mission 1 (0B76DF3C)](#trigger-0b76df3c).

Attached scope: tag definitions 0DD8D6DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaAlcatrazIntro.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9388, Events line 9692, Actions line 9996.

<a id="trigger-0b752f3c"></a>

### 23. SP2.1_Destroy_AlliedDef - 0B752F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Aircraft Carrier (CARRIER), owner Americans, cell (64, 83), tag 0B75455C, persistence mode 1; Aircraft Carrier (CARRIER), owner Americans, cell (65, 85), tag 0B75455C, persistence mode 1; Destroyer (DEST), owner Americans, cell (64, 78), tag 0B75455C, persistence mode 1; Destroyer (DEST), owner Americans, cell (64, 87), tag 0B75455C, persistence mode 1; Destroyer (DEST), owner Americans, cell (64, 80), tag 0B75455C, persistence mode 1; Grand Cannon (GTGCAN), owner Alliance, cell (74, 97), tag 0B75455C, persistence mode 1; Grand Cannon (GTGCAN), owner Alliance, cell (70, 93), tag 0B75455C, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Make side cheer: owner selector 8 (country/type RUSSIANS; placed owner Russians).
2. Disable player input.
3. Create/recruit team [TM_Sov_Exit 1 Dread (0C65EA7C)](sov01umd-teams.md#team-0c65ea7c).
4. Create/recruit team [TM_Sov_Exit 1 Dread (0C65EA7C)](sov01umd-teams.md#team-0c65ea7c).
5. Create/recruit team [TM_Sov_Exit 1 Dread (0C65EA7C)](sov01umd-teams.md#team-0c65ea7c).
6. Create/recruit team [TM_Sov_Exit 1 Scorpion (0C65E6DC)](sov01umd-teams.md#team-0c65e6dc).
7. Create/recruit team [TM_Sov_Exit 1 Scorpion (0C65E6DC)](sov01umd-teams.md#team-0c65e6dc).
8. Create/recruit team [TM_Sov_Exit 1 Scorpion (0C65E6DC)](sov01umd-teams.md#team-0c65e6dc).
9. Create/recruit team [TM_Sov_Exit 1 Scorpion (0C65E6DC)](sov01umd-teams.md#team-0c65e6dc).
10. Create/recruit team [TM_Sov_Exit 1 Scorpion (0C65E6DC)](sov01umd-teams.md#team-0c65e6dc).
11. Create/recruit team [TM_Sov_Exit 1 Squid (0C65E33C)](sov01umd-teams.md#team-0c65e33c).
12. Create/recruit team [TM_Sov_Exit 1 Squid (0C65E33C)](sov01umd-teams.md#team-0c65e33c).
13. Create/recruit team [TM_Sov_Exit 1 Sub (0C65FEFC)](sov01umd-teams.md#team-0c65fefc).
14. Create/recruit team [TM_Sov_Exit 1 Sub (0C65FEFC)](sov01umd-teams.md#team-0c65fefc).
15. Create/recruit team [TM_Sov_Exit 1 Sub (0C65FEFC)](sov01umd-teams.md#team-0c65fefc).
16. Enable and reset applicable timers for [SP2.3_Sov Landing (0B92C6AC)](#trigger-0b92c6ac).
17. Disable [Reinforce_Dreads (0968EE5C)](#trigger-0968ee5c).
18. Disable [Reinforce_Scorpions (0968D20C)](#trigger-0968d20c).
19. Disable [Reinforce_Squids (0966170C)](#trigger-0966170c).
20. Disable [Reinforce_Subs (0966AC6C)](#trigger-0966ac6c).
21. Disable [Text_Objective 1 (094D448C)](#trigger-094d448c).
22. Enable and reset applicable timers for [SP2.2_Disable_DetectSea (0BBB5C6C)](#trigger-0bbb5c6c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9389, Events line 9693, Actions line 9997.

<a id="trigger-0b92c6ac"></a>

### 24. SP2.3_Sov Landing - 0B92C6AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.1_Destroy_AlliedDef (0B752F3C)](#trigger-0b752f3c).

Attached scope: tag definitions 0B92C5CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.
2. Jump the camera to waypoint 78 (cell 52, 91).
3. Enable and reset applicable timers for [SP2.8_Camera to CC (0B8A28BC)](#trigger-0b8a28bc).
4. Enable and reset applicable timers for [SP2.4_Transport 1 (0BAFDF3C)](#trigger-0bafdf3c).
5. Play sound CameraSwitch.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9390, Events line 9694, Actions line 9998.

<a id="trigger-0968ee5c"></a>

### 25. Reinforce_Dreads - 0968EE5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Dread2 Dead (09665A4C)](#trigger-09665a4c).

Attached scope: tag definitions 0968ED7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Reinforce_Dreads (0968EE5C)](#trigger-0968ee5c).
2. Supply reinforcement team [TM_Sov_Dreadnought 2 (0C04FEFC)](sov01umd-teams.md#team-0c04fefc).
3. Enable and reset applicable timers for [Audio_Announce Dreads (0968E62C)](#trigger-0968e62c).
4. Enable and reset applicable timers for [Detect_Dread2 Enable (0900AB1C)](#trigger-0900ab1c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9391, Events line 9695, Actions line 9999.

<a id="trigger-0968d20c"></a>

### 26. Reinforce_Scorpions - 0968D20C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0968EF4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 16 (Scorp2 Dead) is set.
2. local flag 17 (Scorp3 Dead) is set.
3. local flag 18 (Scorp4 Dead) is set.

Flag writers in this mission: set local flag 16 (Scorp2 Dead) at [Detect_Scorpion2 Dead (09660C6C)](#trigger-09660c6c); set local flag 17 (Scorp3 Dead) at [Detect_Scorpion3 Dead (0966136C)](#trigger-0966136c); set local flag 18 (Scorp4 Dead) at [Detect_Scorpion4 Dead (0966153C)](#trigger-0966153c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Sea Scorpion 2 (0C0A824C)](sov01umd-teams.md#team-0c0a824c).
2. Supply reinforcement team [TM_Sov_Sea Scorpion 3 (0C0A9C8C)](sov01umd-teams.md#team-0c0a9c8c).
3. Supply reinforcement team [TM_Sov_Sea Scorpion 4 (0C0A98EC)](sov01umd-teams.md#team-0c0a98ec).
4. Enable and reset applicable timers for [Audio_AnnounceScorpions (0968EABC)](#trigger-0968eabc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9392, Events line 9696, Actions line 10000.

<a id="trigger-0966170c"></a>

### 27. Reinforce_Squids - 0966170C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0968D3DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 13 (Squid1 Dead) is set.
2. local flag 14 (Squid2 Dead) is set.

Flag writers in this mission: set local flag 13 (Squid1 Dead) at [Detect_Squid1 Dead (0966E65C)](#trigger-0966e65c); set local flag 14 (Squid2 Dead) at [Detect_Squid2 Dead (096534FC)](#trigger-096534fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Squid 1 (0C0A71CC)](sov01umd-teams.md#team-0c0a71cc).
2. Supply reinforcement team [TM_Sov_Squid 2 (0C0A8B7C)](sov01umd-teams.md#team-0c0a8b7c).
3. Enable and reset applicable timers for [Audio_Announce Squids (0968EC8C)](#trigger-0968ec8c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9393, Events line 9697, Actions line 10001.

<a id="trigger-0966ac6c"></a>

### 28. Reinforce_Subs - 0966AC6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0966A3AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Sub1 Dead) is set.
2. local flag 11 (Sub2 Dead) is set.
3. local flag 12 (Sub3 Dead) is set.

Flag writers in this mission: set local flag 10 (Sub1 Dead) at [Detect_Sub1 Dead (0966B44C)](#trigger-0966b44c); set local flag 11 (Sub2 Dead) at [Detect_Sub2 Dead (0965FF3C)](#trigger-0965ff3c); set local flag 12 (Sub3 Dead) at [Detect_Sub3 Dead (0965A36C)](#trigger-0965a36c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Sub 1 (0C0A612C)](sov01umd-teams.md#team-0c0a612c).
2. Supply reinforcement team [TM_Sov_Sub 2 (0C0A790C)](sov01umd-teams.md#team-0c0a790c).
3. Supply reinforcement team [TM_Sov_Sub 3 (0C0A756C)](sov01umd-teams.md#team-0c0a756c).
4. Enable and reset applicable timers for [Audio_Announce Subs (0966A2BC)](#trigger-0966a2bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9394, Events line 9698, Actions line 10002.

<a id="trigger-0bbb5c6c"></a>

### 29. SP2.2_Disable_DetectSea - 0BBB5C6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.1_Destroy_AlliedDef (0B752F3C)](#trigger-0b752f3c).

Attached scope: tag definitions 0BBB5B8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Detect_Dread1 Dead (0966E2BC)](#trigger-0966e2bc).
2. Disable [Detect_Dread2 Dead (09665A4C)](#trigger-09665a4c).
3. Disable [Detect_Dread3 Dead (096657DC)](#trigger-096657dc).
4. Disable [Detect_Scorpion1 Dead (0966E48C)](#trigger-0966e48c).
5. Disable [Detect_Scorpion2 Dead (09660C6C)](#trigger-09660c6c).
6. Disable [Detect_Scorpion3 Dead (0966136C)](#trigger-0966136c).
7. Disable [Detect_Scorpion4 Dead (0966153C)](#trigger-0966153c).
8. Disable [Detect_Scorpion5 Dead (09660E3C)](#trigger-09660e3c).
9. Disable [Detect_Squid1 Dead (0966E65C)](#trigger-0966e65c).
10. Disable [Detect_Squid2 Dead (096534FC)](#trigger-096534fc).
11. Disable [Detect_Sub1 Dead (0966B44C)](#trigger-0966b44c).
12. Disable [Detect_Sub2 Dead (0965FF3C)](#trigger-0965ff3c).
13. Disable [Detect_Sub3 Dead (0965A36C)](#trigger-0965a36c).
14. Enable and reset applicable timers for [Complete_Objective 1 (08E4940C)](#trigger-08e4940c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9395, Events line 9699, Actions line 10003.

<a id="trigger-0b8a28bc"></a>

### 30. SP2.8_Camera to CC - 0B8A28BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.3_Sov Landing (0B92C6AC)](#trigger-0b92c6ac).

Attached scope: tag definitions 0B8A27DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 80 (cell 79, 72) with speed setting 0.
2. Enable and reset applicable timers for [SP2.9_Movie_ZofTimeMach (094DC05C)](#trigger-094dc05c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9396, Events line 9700, Actions line 10004.

<a id="trigger-0bafdf3c"></a>

### 31. SP2.4_Transport 1 - 0BAFDF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.3_Sov Landing (0B92C6AC)](#trigger-0b92c6ac).

Attached scope: tag definitions 0BAF9BEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_1 Trans_4 Rhino (08816EFC)](sov01umd-teams.md#team-08816efc).
2. Enable and reset applicable timers for [SP2.5_Transport 2 (0BAF8ABC)](#trigger-0baf8abc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9397, Events line 9701, Actions line 10005.

<a id="trigger-0968e62c"></a>

### 32. Audio_Announce Dreads - 0968E62C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Dreads (0968EE5C)](#trigger-0968ee5c).

Attached scope: tag definitions 0966E8FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Audio_Announce Dreads (0968E62C)](#trigger-0968e62c).
2. Create radar-event marker type 2 at waypoint 14 (cell 51, 93).
3. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9398, Events line 9702, Actions line 10006.

<a id="trigger-0900ab1c"></a>

### 33. Detect_Dread2 Enable - 0900AB1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Dreads (0968EE5C)](#trigger-0968ee5c).

Attached scope: tag definitions 0900AA3C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Detect_Dread2 Enable (0900AB1C)](#trigger-0900ab1c).
2. Enable and reset applicable timers for [Detect_Dread2 Dead (09665A4C)](#trigger-09665a4c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9399, Events line 9703, Actions line 10007.

<a id="trigger-0968eabc"></a>

### 34. Audio_AnnounceScorpions - 0968EABC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Scorpions (0968D20C)](#trigger-0968d20c).

Attached scope: tag definitions 0968E71C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Audio_AnnounceScorpions (0968EABC)](#trigger-0968eabc).
2. Create radar-event marker type 2 at waypoint 20 (cell 54, 91).
3. Create radar-event marker type 2 at waypoint 19 (cell 53, 92).
4. Create radar-event marker type 2 at waypoint 18 (cell 54, 93).
5. Create radar-event marker type 2 at waypoint 17 (cell 53, 94).
6. Create radar-event marker type 2 at waypoint 16 (cell 54, 95).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9400, Events line 9704, Actions line 10008.

<a id="trigger-0968ec8c"></a>

### 35. Audio_Announce Squids - 0968EC8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Squids (0966170C)](#trigger-0966170c).

Attached scope: tag definitions 0968EBAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Audio_Announce Squids (0968EC8C)](#trigger-0968ec8c).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Create radar-event marker type 2 at waypoint 22 (cell 55, 92).
4. Create radar-event marker type 2 at waypoint 21 (cell 55, 94).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9401, Events line 9705, Actions line 10009.

<a id="trigger-0966a2bc"></a>

### 36. Audio_Announce Subs - 0966A2BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Subs (0966AC6C)](#trigger-0966ac6c).

Attached scope: tag definitions 0966EB7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Audio_Announce Subs (0966A2BC)](#trigger-0966a2bc).
2. Create radar-event marker type 2 at waypoint 25 (cell 57, 91).
3. Create radar-event marker type 2 at waypoint 24 (cell 57, 93).
4. Create radar-event marker type 2 at waypoint 23 (cell 57, 95).
5. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9402, Events line 9706, Actions line 10010.

<a id="trigger-0966e2bc"></a>

### 37. Detect_Dread1 Dead - 0966E2BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096617FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 20 (Dread1 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9403, Events line 9707, Actions line 10011.

<a id="trigger-09665a4c"></a>

### 38. Detect_Dread2 Dead - 09665A4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Dread2 Enable (0900AB1C)](#trigger-0900ab1c).

Attached scope: tag definitions 096658CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Detect_Dread2 Dead (09665A4C)](#trigger-09665a4c).
2. Enable and reset applicable timers for [Reinforce_Dreads (0968EE5C)](#trigger-0968ee5c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9404, Events line 9708, Actions line 10012.

<a id="trigger-096657dc"></a>

### 39. Detect_Dread3 Dead - 096657DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096656FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 22 (Dread3 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9405, Events line 9709, Actions line 10013.

<a id="trigger-0966e48c"></a>

### 40. Detect_Scorpion1 Dead - 0966E48C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0966E3AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 15 (Scorp1 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9406, Events line 9710, Actions line 10014.

<a id="trigger-09660c6c"></a>

### 41. Detect_Scorpion2 Dead - 09660C6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09667F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 16 (Scorp2 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9407, Events line 9711, Actions line 10015.

<a id="trigger-0966136c"></a>

### 42. Detect_Scorpion3 Dead - 0966136C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0966163C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 17 (Scorp3 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9408, Events line 9712, Actions line 10016.

<a id="trigger-0966153c"></a>

### 43. Detect_Scorpion4 Dead - 0966153C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0966145C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 18 (Scorp4 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9409, Events line 9713, Actions line 10017.

<a id="trigger-09660e3c"></a>

### 44. Detect_Scorpion5 Dead - 09660E3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09660D5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 19 (Scorp5 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9410, Events line 9714, Actions line 10018.

<a id="trigger-0966e65c"></a>

### 45. Detect_Squid1 Dead - 0966E65C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0966E57C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 13 (Squid1 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9411, Events line 9715, Actions line 10019.

<a id="trigger-096534fc"></a>

### 46. Detect_Squid2 Dead - 096534FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0965341C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 14 (Squid2 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9412, Events line 9716, Actions line 10020.

<a id="trigger-0966b44c"></a>

### 47. Detect_Sub1 Dead - 0966B44C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0966B2BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 10 (Sub1 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9413, Events line 9717, Actions line 10021.

<a id="trigger-0965ff3c"></a>

### 48. Detect_Sub2 Dead - 0965FF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0965FE5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 11 (Sub2 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9414, Events line 9718, Actions line 10022.

<a id="trigger-0965a36c"></a>

### 49. Detect_Sub3 Dead - 0965A36C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0965A28C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 12 (Sub3 Dead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9415, Events line 9719, Actions line 10023.

<a id="trigger-08e4940c"></a>

### 50. Complete_Objective 1 - 08E4940C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.2_Disable_DetectSea (0BBB5C6C)](#trigger-0bbb5c6c).

Attached scope: tag definitions 08E4932C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1 Complete.” (MISSION:Obj1Comp).
2. Play voice notification EVA_ObjectiveComplete.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9416, Events line 9720, Actions line 10024.

<a id="trigger-094dc05c"></a>

### 51. SP2.9_Movie_ZofTimeMach - 094DC05C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.8_Camera to CC (0B8A28BC)](#trigger-0b8a28bc).

Attached scope: tag definitions 094DC30C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 34.
2. Enable and reset applicable timers for [SP2.9a_Zofia Time VO (0833254C)](#trigger-0833254c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9417, Events line 9721, Actions line 10025.

<a id="trigger-0baf8abc"></a>

### 52. SP2.5_Transport 2 - 0BAF8ABC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.4_Transport 1 (0BAFDF3C)](#trigger-0bafdf3c).

Attached scope: tag definitions 0BAF9F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_1 Trans_12 Conscript (08DF843C)](sov01umd-teams.md#team-08df843c).
2. Enable and reset applicable timers for [SP2.6_Transport 3 (0BAFCC3C)](#trigger-0bafcc3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9418, Events line 9722, Actions line 10026.

<a id="trigger-0833254c"></a>

### 53. SP2.9a_Zofia Time VO - 0833254C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.9_Movie_ZofTimeMach (094DC05C)](#trigger-094dc05c).

Attached scope: tag definitions 0833246C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 18 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification S01_p01.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9419, Events line 9723, Actions line 10027.

<a id="trigger-0bafcc3c"></a>

### 54. SP2.6_Transport 3 - 0BAFCC3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.5_Transport 2 (0BAF8ABC)](#trigger-0baf8abc).

Attached scope: tag definitions 0BAFF48C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_1 Trans_4 Flak Trak (0B5CAEFC)](sov01umd-teams.md#team-0b5caefc).
2. Enable and reset applicable timers for [SP2.7_Transport 4 (0BAF845C)](#trigger-0baf845c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9420, Events line 9724, Actions line 10028.

<a id="trigger-0baf845c"></a>

### 55. SP2.7_Transport 4 - 0BAF845C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.6_Transport 3 (0BAFCC3C)](#trigger-0bafcc3c).

Attached scope: tag definitions 0BAFE22C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_1 Trans_1 Boris_5 Tesla_3 Dog_3 Eng (0B244DEC)](sov01umd-teams.md#team-0b244dec).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9421, Events line 9725, Actions line 10029.

<a id="trigger-0b8a231c"></a>

### 56. SP2.13_Unlock - 0B8A231C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.12a_Audio_Goodluck (091B431C)](#trigger-091b431c).

Attached scope: tag definitions 0B8A223C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_BattlefieldControlOnline.
2. Enable player input.
3. Display message “Objective 2: Destroy Pill Boxes around Time Machine to capture it.” (MISSION:Sov1Obj2).
4. Create radar-event marker type 1 at waypoint 62 (cell 147, 99).
5. Enable and reset applicable timers for [Text_Objective 2 (09577E1C)](#trigger-09577e1c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9422, Events line 9726, Actions line 10030.

<a id="trigger-09577e1c"></a>

### 57. Text_Objective 2 - 09577E1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.13_Unlock (0B8A231C)](#trigger-0b8a231c).

Attached scope: tag definitions 09577D3C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy Pill Boxes around Time Machine to capture it.” (MISSION:Sov1Obj2).
2. Create radar-event marker type 1 at waypoint 62 (cell 147, 99).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9423, Events line 9727, Actions line 10031.

<a id="trigger-0d17f50c"></a>

### 58. SP2.14_Audio_Obj 2a - 0D17F50C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D17F42C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (Trans 4 Unloaded) is set.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaBriefing01.
2. Enable and reset applicable timers for [SP2.15_Audio_Obj 2b (0DD8E32C)](#trigger-0dd8e32c).
3. Enable and reset applicable timers for [SP2.14a_Camera to Time (05D70C3C)](#trigger-05d70c3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9424, Events line 9728, Actions line 10032.

<a id="trigger-0dd8e32c"></a>

### 59. SP2.15_Audio_Obj 2b - 0DD8E32C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.14_Audio_Obj 2a (0D17F50C)](#trigger-0d17f50c).

Attached scope: tag definitions 0DD8D9EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaBriefing02.
2. Enable and reset applicable timers for [SP2.16_Audio_Obj 2c (0DE581DC)](#trigger-0de581dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9425, Events line 9729, Actions line 10033.

<a id="trigger-05d70c3c"></a>

### 60. SP2.14a_Camera to Time - 05D70C3C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.14_Audio_Obj 2a (0D17F50C)](#trigger-0d17f50c).

Attached scope: tag definitions 05D70B5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 82 (cell 138, 97).
2. Play sound CameraSwitch.
3. Reveal terrain around waypoint 62 (cell 147, 99).
4. Create radar-event marker type 5 at waypoint 62 (cell 147, 99).
5. Flash buildings of type CATIME01; duration argument 120.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9426, Events line 9730, Actions line 10034.

<a id="trigger-0de581dc"></a>

### 61. SP2.16_Audio_Obj 2c - 0DE581DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.15_Audio_Obj 2b (0DD8E32C)](#trigger-0dd8e32c).

Attached scope: tag definitions 0DE5EF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 61 (cell 86, 81).
2. Play sound CameraSwitch.
3. Enable and reset applicable timers for [SP2.10_BorisIntro (0D17008C)](#trigger-0d17008c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9427, Events line 9731, Actions line 10035.

<a id="trigger-0d17008c"></a>

### 62. SP2.10_BorisIntro - 0D17008C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.16_Audio_Obj 2c (0DE581DC)](#trigger-0de581dc).

Attached scope: tag definitions 0D176A7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TM_Sov_1 Boris (093DE24C)](sov01umd-teams.md#team-093de24c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9428, Events line 9732, Actions line 10036.

<a id="trigger-0439013c"></a>

### 63. Audio_Don't Attack Yuri - 0439013C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 77 tagged map cells: (72, 15), (72, 16), (72, 17), (72, 18), (72, 19), (72, 20), (72, 21), (72, 22), (72, 23), (72, 24), (72, 25), (72, 26), (72, 27), (72, 28), (72, 29), (72, 30), (72, 31), (72, 32), (72, 33), (72, 34), (72, 35), (72, 36), (72, 37), (72, 38), (72, 39), (72, 40), (72, 41), (72, 42), (72, 43), (72, 44), (72, 45), (72, 46), (72, 47), (72, 48), (72, 49), (72, 50), (72, 51), (72, 52), (72, 53), (72, 54), (72, 55), (72, 56), (72, 57), (72, 58), (71, 59), (72, 59), (71, 60), (69, 61), (70, 61), (71, 61), (69, 62), (68, 63), (69, 63), (67, 64), (68, 64), (66, 65), (67, 65), (65, 66), (66, 66), (64, 67), (65, 67), (63, 68), (64, 68), (62, 69), (63, 69), (61, 70), (62, 70), (60, 71), (61, 71), (55, 72), (56, 72), (59, 72), (60, 72), (56, 73), (57, 73), (58, 73), (59, 73); tag 0439005C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaCapTimeMachine.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9429, Events line 9733, Actions line 10037.

<a id="trigger-0d17876c"></a>

### 64. SP2.12_ZofiaREBoris - 0D17876C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.11_BorisReports (0D17FAAC)](#trigger-0d17faac).

Attached scope: tag definitions 0D17C89C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_Boris.
2. Enable and reset applicable timers for [SP2.12a_Audio_Goodluck (091B431C)](#trigger-091b431c).
3. Move the camera to waypoint 61 (cell 86, 81) with speed setting 3.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9430, Events line 9734, Actions line 10038.

<a id="trigger-091b431c"></a>

### 65. SP2.12a_Audio_Goodluck - 091B431C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.12_ZofiaREBoris (0D17876C)](#trigger-0d17876c).

Attached scope: tag definitions 091B423C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 23 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaBriefing03.
2. Enable and reset applicable timers for [SP2.13_Unlock (0B8A231C)](#trigger-0b8a231c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9431, Events line 9735, Actions line 10039.

<a id="trigger-0d17faac"></a>

### 66. SP2.11_BorisReports - 0D17FAAC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D17F9CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 23 (Boris Intro) is set.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_BorisReporting.
2. Enable and reset applicable timers for [SP2.12_ZofiaREBoris (0D17876C)](#trigger-0d17876c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9432, Events line 9736, Actions line 10040.

<a id="trigger-079db44c"></a>

### 67. Audio_YuriCapturePower - 079DB44C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Time Machine Off (094A4ADC)](#trigger-094a4adc).

Attached scope: tag definitions 079DB36C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaYuriNeedsPower.
2. Enable and reset applicable timers for [Reinforce_Atk Group 1 (043DF33C)](#trigger-043df33c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9433, Events line 9737, Actions line 10041.

<a id="trigger-043df33c"></a>

### 68. Reinforce_Atk Group 1 - 043DF33C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_YuriCapturePower (079DB44C)](#trigger-079db44c); enable from [Reinforce_Cap Delay (06A6663C)](#trigger-06a6663c).

Attached scope: tag definitions 043DF25C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_NTime Plant Attack (0946F03C)](sov01umd-teams.md#team-0946f03c).
2. Supply reinforcement team [TM_Yuri_STime Plant Attack (094708CC)](sov01umd-teams.md#team-094708cc).
3. Supply reinforcement team [TM_Yuri_Gas Plant Attack (092A27BC)](sov01umd-teams.md#team-092a27bc).
4. Enable and reset applicable timers for [Reinforce_Cap Group 1 (0B454BBC)](#trigger-0b454bbc).
5. Disable [Reinforce_Atk Group 1 (043DF33C)](#trigger-043df33c).
6. Display message “Yuri Hover Transports approaching!” (MISSION:YuriHovr).
7. Enable and reset applicable timers for [Reinforce_Atk Ping 1 (08FC09DC)](#trigger-08fc09dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9434, Events line 9738, Actions line 10042.

<a id="trigger-0b454bbc"></a>

### 69. Reinforce_Cap Group 1 - 0B454BBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Atk Group 1 (043DF33C)](#trigger-043df33c).

Attached scope: tag definitions 043DF42C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Arab_NTime Plant Capture (0C3121AC)](sov01umd-teams.md#team-0c3121ac).
2. Supply reinforcement team [TM_Arab_STime Plant Capture (0C311C8C)](sov01umd-teams.md#team-0c311c8c).
3. Supply reinforcement team [TM_Arab_Gas Plant Capture (0C31254C)](sov01umd-teams.md#team-0c31254c).
4. Enable and reset applicable timers for [Reinforce_Atk Group 2 (06A6629C)](#trigger-06a6629c).
5. Disable [Reinforce_Cap Group 1 (0B454BBC)](#trigger-0b454bbc).
6. Display message “Yuri is trying to capture the Power Plants!” (MISSION:YuriPowr).
7. Apply 100 damage at; main setting 120; location/duration field DQ.
8. Apply 100 damage at; main setting 119; location/duration field DP.
9. Apply 100 damage at; main setting 118; location/duration field DO.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9435, Events line 9739, Actions line 10043.

<a id="trigger-08fc09dc"></a>

### 70. Reinforce_Atk Ping 1 - 08FC09DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Atk Group 1 (043DF33C)](#trigger-043df33c).

Attached scope: tag definitions 08FC08FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Reinforce_Atk Ping 1 (08FC09DC)](#trigger-08fc09dc).
2. Create radar-event marker type 5 at waypoint 496 (cell 68, 55).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9436, Events line 9740, Actions line 10044.

<a id="trigger-06a6629c"></a>

### 71. Reinforce_Atk Group 2 - 06A6629C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Cap Group 1 (0B454BBC)](#trigger-0b454bbc).

Attached scope: tag definitions 06A661BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_Park Plant Attack (092A2B5C)](sov01umd-teams.md#team-092a2b5c).
2. Supply reinforcement team [TM_Yuri_Statue Plant Attack (0946E06C)](sov01umd-teams.md#team-0946e06c).
3. Supply reinforcement team [TM_Yuri_Grand Plant Attack (0946E7DC)](sov01umd-teams.md#team-0946e7dc).
4. Enable and reset applicable timers for [Reinforce_Cap Group 2 (06A6646C)](#trigger-06a6646c).
5. Disable [Reinforce_Atk Group 2 (06A6629C)](#trigger-06a6629c).
6. Enable and reset applicable timers for [Reinforce_Atk Ping 2 (08FC0BAC)](#trigger-08fc0bac).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9437, Events line 9741, Actions line 10045.

<a id="trigger-06a6646c"></a>

### 72. Reinforce_Cap Group 2 - 06A6646C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Atk Group 2 (06A6629C)](#trigger-06a6629c).

Attached scope: tag definitions 06A6638C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Arab_Park Plant Capture (0C3128EC)](sov01umd-teams.md#team-0c3128ec).
2. Supply reinforcement team [TM_Arab_Statue Plant Capture (0C312C8C)](sov01umd-teams.md#team-0c312c8c).
3. Supply reinforcement team [TM_Arab_Grand Plant Capture (0C3132DC)](sov01umd-teams.md#team-0c3132dc).
4. Enable and reset applicable timers for [Reinforce_Cap Delay (06A6663C)](#trigger-06a6663c).
5. Disable [Reinforce_Cap Group 2 (06A6646C)](#trigger-06a6646c).
6. Display message “Yuri is trying to capture the Power Plants!” (MISSION:YuriPowr).
7. Apply 100 damage at; main setting 117; location/duration field DN.
8. Apply 100 damage at; main setting 116; location/duration field DM.
9. Apply 100 damage at; main setting 115; location/duration field DL.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9438, Events line 9742, Actions line 10046.

<a id="trigger-08fc0bac"></a>

### 73. Reinforce_Atk Ping 2 - 08FC0BAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Atk Group 2 (06A6629C)](#trigger-06a6629c).

Attached scope: tag definitions 08FC0ACC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Reinforce_Atk Ping 2 (08FC0BAC)](#trigger-08fc0bac).
2. Create radar-event marker type 5 at waypoint 496 (cell 68, 55).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9439, Events line 9743, Actions line 10047.

<a id="trigger-06a6663c"></a>

### 74. Reinforce_Cap Delay - 06A6663C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_Cap Group 2 (06A6646C)](#trigger-06a6646c).

Attached scope: tag definitions 06A6655C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 39 (NoMoreCapTeams) is clear.

Flag writers in this mission: set local flag 39 (NoMoreCapTeams) at [Reinforce_Cap Delay (06A6663C)](#trigger-06a6663c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 39 (NoMoreCapTeams).
2. Enable and reset applicable timers for [Reinforce_Atk Group 1 (043DF33C)](#trigger-043df33c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9440, Events line 9744, Actions line 10048.

<a id="trigger-094a4e1c"></a>

### 75. Destroy_Time Defenses - 094A4E1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pill Box (GAPILL), owner Confederation, cell (146, 97), tag 094A4D3C, persistence mode 1; Pill Box (GAPILL), owner Confederation, cell (143, 99), tag 094A4D3C, persistence mode 1; Pill Box (GAPILL), owner Confederation, cell (144, 95), tag 094A4D3C, persistence mode 1; Pill Box (GAPILL), owner Confederation, cell (141, 97), tag 094A4D3C, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Audio_Time Machine Off (094A4ADC)](#trigger-094a4adc).
2. Enable and reset applicable timers for [Sell_Time Defenses (096012AC)](#trigger-096012ac).
3. Enable and reset applicable timers for [Give_Time to Russians (0DECD98C)](#trigger-0decd98c).
4. Disable [Text_Objective 2a (043E7EDC)](#trigger-043e7edc).
5. Enable and reset applicable timers for [Complete_Objective 2 (07EF7AEC)](#trigger-07ef7aec).
6. Disable [Time Machine Neutral (095180BC)](#trigger-095180bc).
7. Enable and reset applicable timers for [Time Machine Russian (079D7E1C)](#trigger-079d7e1c).
8. Enable and reset applicable timers for [Detect_(US) Mach Shop (05BF392C)](#trigger-05bf392c).
9. Enable and reset applicable timers for [Detect_(Sov) Mach Shop (05BF375C)](#trigger-05bf375c).
10. Disable [Audio_Destroy Time Defs (094A51CC)](#trigger-094a51cc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9441, Events line 9745, Actions line 10049.

<a id="trigger-094a4adc"></a>

### 76. Audio_Time Machine Off - 094A4ADC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroy_Time Defenses (094A4E1C)](#trigger-094a4e1c).

Attached scope: tag definitions 094A49FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaEngineersForPower.
2. Enable and reset applicable timers for [SP3.1_Detect_Full Power (0BDE024C)](#trigger-0bde024c).
3. Display message “Objective 3: Capture 4 Power Plants to Power Time Machine.” (MISSION:Sov1Obj3).
4. Reveal terrain around waypoint 115 (cell 79, 111).
5. Reveal terrain around waypoint 116 (cell 80, 126).
6. Reveal terrain around waypoint 117 (cell 92, 117).
7. Reveal terrain around waypoint 118 (cell 112, 113).
8. Reveal terrain around waypoint 119 (cell 128, 116).
9. Reveal terrain around waypoint 120 (cell 120, 82).
10. Create radar-event marker type 1 at waypoint 115 (cell 79, 111).
11. Create radar-event marker type 1 at waypoint 116 (cell 80, 126).
12. Create radar-event marker type 1 at waypoint 117 (cell 92, 117).
13. Create radar-event marker type 1 at waypoint 118 (cell 112, 113).
14. Create radar-event marker type 1 at waypoint 119 (cell 128, 116).
15. Create radar-event marker type 1 at waypoint 120 (cell 120, 82).
16. Enable and reset applicable timers for [Text_Objective 3 (09577C4C)](#trigger-09577c4c).
17. Enable and reset applicable timers for [Audio_YuriCapturePower (079DB44C)](#trigger-079db44c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9442, Events line 9746, Actions line 10050.

<a id="trigger-096012ac"></a>

### 77. Sell_Time Defenses - 096012AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroy_Time Defenses (094A4E1C)](#trigger-094a4e1c).

Attached scope: Pill Box (GAPILL), owner Americans, cell (132, 99), tag 0959237C, persistence mode 2; Pill Box (GAPILL), owner Americans, cell (132, 103), tag 0959237C, persistence mode 2; Patriot Missile (NASAM), owner Alliance, cell (137, 104), tag 0959237C, persistence mode 2; Patriot Missile (NASAM), owner Alliance, cell (145, 104), tag 0959237C, persistence mode 2; Patriot Missile (NASAM), owner Alliance, cell (137, 94), tag 0959237C, persistence mode 2; Patriot Missile (NASAM), owner Alliance, cell (137, 87), tag 0959237C, persistence mode 2.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Sell_Time Defenses (096012AC)](#trigger-096012ac).
2. Sell the attached building through the scripted sale action.
3. Enable and reset applicable timers for [Reinforce_10 Engineers (06AF616C)](#trigger-06af616c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9443, Events line 9747, Actions line 10051.

<a id="trigger-0decd98c"></a>

### 78. Give_Time to Russians - 0DECD98C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Audio_Don't Attack Time (06C0F45C)](#trigger-06c0f45c).

Incoming activation links: enable from [Destroy_Time Defenses (094A4E1C)](#trigger-094a4e1c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 8 (country/type RUSSIANS; placed owner Russians).
2. Disable [Give_Time to Russians (0DECD98C)](#trigger-0decd98c).
3. Disable [Text_Objective 2 (09577E1C)](#trigger-09577e1c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9444, Events line 9748, Actions line 10052.

<a id="trigger-043e7edc"></a>

### 79. Text_Objective 2a - 043E7EDC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Destroy Time Defs (094A51CC)](#trigger-094a51cc).

Attached scope: tag definitions 043E7DFC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Destroy the Pill Boxes surrounding the Time Machine.” (MISSION:Sov1Obj2a).
2. Create radar-event marker type 5 at waypoint 66 (cell 147, 98).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9445, Events line 9749, Actions line 10053.

<a id="trigger-07ef7aec"></a>

### 80. Complete_Objective 2 - 07EF7AEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroy_Time Defenses (094A4E1C)](#trigger-094a4e1c).

Attached scope: tag definitions 07EF7A0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ObjectiveComplete.
2. Display message “Objective 2 Complete.” (MISSION:Obj2Comp).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9446, Events line 9750, Actions line 10054.

<a id="trigger-095180bc"></a>

### 81. Time Machine Neutral - 095180BC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [SP3.1_Detect_Full Power (0BDE024C)](#trigger-0bde024c).
2. Disable [Time Machine Neutral (095180BC)](#trigger-095180bc).
3. Play voice notification Mis_xS1_ZofiaLostTimeMach.
4. Enable and reset applicable timers for [_End_Lose (06B602BC)](#trigger-06b602bc).
5. Disable [Destroy_Time Defenses (094A4E1C)](#trigger-094a4e1c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9447, Events line 9751, Actions line 10055.

<a id="trigger-079d7e1c"></a>

### 82. Time Machine Russian - 079D7E1C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Give_Back to Allies (09601D2C)](#trigger-09601d2c).

Incoming activation links: enable from [Destroy_Time Defenses (094A4E1C)](#trigger-094a4e1c).

Attached scope: Time Machine (CATIME01), owner Neutral, cell (142, 96), tag 09519F4C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [SP3.1_Detect_Full Power (0BDE024C)](#trigger-0bde024c).
2. Disable [Time Machine Russian (079D7E1C)](#trigger-079d7e1c).
3. Play voice notification Mis_xS1_ZofiaLostTimeMach.
4. Enable and reset applicable timers for [_End_Lose (06B602BC)](#trigger-06b602bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9448, Events line 9752, Actions line 10056.

<a id="trigger-05bf392c"></a>

### 83. Detect_(US) Mach Shop - 05BF392C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroy_Time Defenses (094A4E1C)](#trigger-094a4e1c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 56 (global list position: Tech Machine Shop (CAMACH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Audio_American Mach Shop (05BF366C)](#trigger-05bf366c).
2. Disable [Detect_(Sov) Mach Shop (05BF375C)](#trigger-05bf375c).
3. Disable [Audio_Russian Mach Shop (05BF4E3C)](#trigger-05bf4e3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9449, Events line 9753, Actions line 10057.

<a id="trigger-05bf375c"></a>

### 84. Detect_(Sov) Mach Shop - 05BF375C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_(US) Mach Shop (05BF392C)](#trigger-05bf392c).

Incoming activation links: enable from [Destroy_Time Defenses (094A4E1C)](#trigger-094a4e1c).

Attached scope: tag definitions 05BF384C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 56 (global list position: Tech Machine Shop (CAMACH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Audio_Russian Mach Shop (05BF4E3C)](#trigger-05bf4e3c).
2. Disable [Detect_(US) Mach Shop (05BF392C)](#trigger-05bf392c).
3. Disable [Audio_American Mach Shop (05BF366C)](#trigger-05bf366c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9450, Events line 9754, Actions line 10058.

<a id="trigger-094a51cc"></a>

### 85. Audio_Destroy Time Defs - 094A51CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 35 tagged map cells: (138, 87), (139, 87), (140, 87), (141, 87), (136, 88), (137, 88), (138, 88), (136, 89), (136, 90), (136, 91), (136, 92), (136, 93), (136, 94), (136, 95), (136, 96), (136, 97), (136, 98), (136, 99), (136, 100), (137, 100), (137, 101), (138, 101), (138, 102), (139, 102), (139, 103), (139, 104), (139, 105), (140, 105), (141, 105), (142, 105), (143, 105), (144, 105), (145, 105), (146, 105), (147, 105); tag 094A8F4C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaTimeDefenses.
2. Enable and reset applicable timers for [SP1.14_Anim_Arrow Loop2 (094A883C)](#trigger-094a883c).
3. Enable and reset applicable timers for [End_Arrow Loop2 (094A989C)](#trigger-094a989c).
4. Create radar-event marker type 5 at waypoint 66 (cell 147, 98).
5. Enable and reset applicable timers for [Text_Objective 2a (043E7EDC)](#trigger-043e7edc).
6. Disable [Text_Objective 2 (09577E1C)](#trigger-09577e1c).
7. Display message “Destroy the Pill Boxes surrounding the Time Machine.” (MISSION:Sov1Obj2a).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9451, Events line 9755, Actions line 10059.

<a id="trigger-0bde024c"></a>

### 86. SP3.1_Detect_Full Power - 0BDE024C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Time Machine Off (094A4ADC)](#trigger-094a4adc); enable from [Detect_Player Has Time (095183EC)](#trigger-095183ec).

Attached scope: tag definitions 0BDE016C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Power Full: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP3.2_Audio_EnoughPower (0951864C)](#trigger-0951864c).
2. Disable [Text_Objective 3 (09577C4C)](#trigger-09577c4c).
3. Enable and reset applicable timers for [Complete_Objective 3 (08E495DC)](#trigger-08e495dc).
4. Disable [Hint_Capture Power (0970A63C)](#trigger-0970a63c).
5. Disable [Audio_YuriCapturePower (079DB44C)](#trigger-079db44c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9452, Events line 9756, Actions line 10060.

<a id="trigger-09577c4c"></a>

### 87. Text_Objective 3 - 09577C4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Time Machine Off (094A4ADC)](#trigger-094a4adc).

Attached scope: tag definitions 09577B6C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Capture 4 Power Plants to Power Time Machine.” (MISSION:Sov1Obj3).
2. Create radar-event marker type 1 at waypoint 115 (cell 79, 111).
3. Create radar-event marker type 1 at waypoint 116 (cell 80, 126).
4. Create radar-event marker type 1 at waypoint 117 (cell 92, 117).
5. Create radar-event marker type 1 at waypoint 118 (cell 112, 113).
6. Create radar-event marker type 1 at waypoint 119 (cell 128, 116).
7. Create radar-event marker type 1 at waypoint 120 (cell 120, 82).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9453, Events line 9757, Actions line 10061.

<a id="trigger-06af616c"></a>

### 88. Reinforce_10 Engineers - 06AF616C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Sell_Time Defenses (096012AC)](#trigger-096012ac).

Attached scope: tag definitions 093BF03C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_10 Engineers (0957AE2C)](sov01umd-teams.md#team-0957ae2c).
2. Enable and reset applicable timers for [Reinforce_10 Eng Audio (077B395C)](#trigger-077b395c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9454, Events line 9758, Actions line 10062.

<a id="trigger-06c0f45c"></a>

### 89. Audio_Don't Attack Time - 06C0F45C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Time Machine Neutral (095180BC)](#trigger-095180bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaSaveTimeMach.
2. Disable [Audio_Don't Attack Time (06C0F45C)](#trigger-06c0f45c).
3. Display message “WARNING - Critical structure. Do not destroy!!!” (MISSION:WarnStct).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9455, Events line 9759, Actions line 10063.

<a id="trigger-06b602bc"></a>

### 90. _End_Lose - 06B602BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Time Machine Neutral (095180BC)](#trigger-095180bc); enable from [Time Machine Russian (079D7E1C)](#trigger-079d7e1c); enable from [Detect_All Sov Dead (097154CC)](#trigger-097154cc); enable from [Detect_< 4 Power (06B6156C)](#trigger-06b6156c); enable from [Detect_Time 2 Destroyed (0BB91C2C)](#trigger-0bb91c2c); enable from [_Lose_Condition (05CAF0BC)](#trigger-05caf0bc).

Attached scope: tag definitions 06B601DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9456, Events line 9760, Actions line 10064.

<a id="trigger-09601d2c"></a>

### 91. Give_Back to Allies - 09601D2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Give_Time to Russians (0DECD98C)](#trigger-0decd98c).

Incoming activation links: enable from [SP3.5_Enable_TimeEffect (0BDE287C)](#trigger-0bde287c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Give_Back to Allies (09601D2C)](#trigger-09601d2c).
2. Change House: owner selector 15 (country/type SOVIET2 COUNTRY; placed owner Soviet2House).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9457, Events line 9761, Actions line 10065.

<a id="trigger-05bf366c"></a>

### 92. Audio_American Mach Shop - 05BF366C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Audio_Russian Mach Shop (05BF4E3C)](#trigger-05bf4e3c).

Incoming activation links: enable from [Detect_(US) Mach Shop (05BF392C)](#trigger-05bf392c).

Attached scope: tag definitions 087D579C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_TechMachShop.
2. Flash buildings of type CAMACH; duration argument 200.
3. Jump the camera to waypoint 64 (cell 142, 93).
4. Set global flag 12.
5. Play sound CameraSwitch.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9458, Events line 9762, Actions line 10066.

<a id="trigger-05bf4e3c"></a>

### 93. Audio_Russian Mach Shop - 05BF4E3C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_(Sov) Mach Shop (05BF375C)](#trigger-05bf375c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_TechMachShop.
2. Flash buildings of type CAMACH; duration argument 200.
3. Jump the camera to waypoint 64 (cell 142, 93).
4. Play sound CameraSwitch.
5. Set global flag 12.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9459, Events line 9763, Actions line 10067.

<a id="trigger-094a883c"></a>

### 94. SP1.14_Anim_Arrow Loop2 - 094A883C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Destroy Time Defs (094A51CC)](#trigger-094a51cc).

Attached scope: tag definitions 094A860C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 483; location/duration field BL.
2. Play Anim At; main setting 483; location/duration field BM.
3. Play Anim At; main setting 480; location/duration field BN.
4. Play Anim At; main setting 480; location/duration field BO.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9460, Events line 9764, Actions line 10068.

<a id="trigger-094a989c"></a>

### 95. End_Arrow Loop2 - 094A989C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Destroy Time Defs (094A51CC)](#trigger-094a51cc).

Attached scope: tag definitions 07DA2D1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [End_Arrow Loop2 (094A989C)](#trigger-094a989c).
2. Disable [SP1.14_Anim_Arrow Loop2 (094A883C)](#trigger-094a883c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9461, Events line 9765, Actions line 10069.

<a id="trigger-0951864c"></a>

### 96. SP3.2_Audio_EnoughPower - 0951864C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.1_Detect_Full Power (0BDE024C)](#trigger-0bde024c).

Attached scope: tag definitions 0951856C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaEnoughPower.
2. Enable and reset applicable timers for [SP3.5_Enable_TimeEffect (0BDE287C)](#trigger-0bde287c).
3. Enable and reset applicable timers for [SP3.3_Setup_Part II (0951740C)](#trigger-0951740c).
4. Enable and reset applicable timers for [SP3.2a_Camera_Jump 2 BK (0BDE0ADC)](#trigger-0bde0adc).
5. Disable [Reinforce_10 Engineers (06AF616C)](#trigger-06af616c).
6. Disable [Reinforce_6 Engineers (06A25F3C)](#trigger-06a25f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9462, Events line 9766, Actions line 10070.

<a id="trigger-08e495dc"></a>

### 97. Complete_Objective 3 - 08E495DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.1_Detect_Full Power (0BDE024C)](#trigger-0bde024c).

Attached scope: tag definitions 08E494FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3 Complete.” (MISSION:Obj3Comp).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9463, Events line 9767, Actions line 10071.

<a id="trigger-0970a63c"></a>

### 98. Hint_Capture Power - 0970A63C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_10 Eng Audio (077B395C)](#trigger-077b395c).

Attached scope: tag definitions 0970A55C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Hint: Capture Power Plants with Engineers” (MISSION:HintPowr).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9464, Events line 9768, Actions line 10072.

<a id="trigger-077b395c"></a>

### 99. Reinforce_10 Eng Audio - 077B395C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_10 Engineers (06AF616C)](#trigger-06af616c).

Attached scope: tag definitions 077B387C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Engineers have arrived near the Time Machine” (MISSION:MoreEngn).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Enable and reset applicable timers for [Hint_Capture Power (0970A63C)](#trigger-0970a63c).
4. Create radar-event marker type 2 at waypoint 114 (cell 130, 101).
5. Jump the camera to waypoint 114 (cell 130, 101).
6. Reveal terrain around waypoint 114 (cell 130, 101).
7. Reveal terrain around waypoint 437 (cell 137, 110).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9465, Events line 9769, Actions line 10073.

<a id="trigger-0bde287c"></a>

### 100. SP3.5_Enable_TimeEffect - 0BDE287C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.2_Audio_EnoughPower (0951864C)](#trigger-0951864c).

Attached scope: tag definitions 0BDE279C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Animation_Time Effect (0951A8BC)](#trigger-0951a8bc).
2. Enable and reset applicable timers for [SP3.5a_Evict Occupiers (0E626A2C)](#trigger-0e626a2c).
3. Teleport the trigger owner's supported objects toward waypoint 15 (cell 51, 91).
4. Enable and reset applicable timers for [Give_Back to Allies (09601D2C)](#trigger-09601d2c).
5. Disable [Time Machine Russian (079D7E1C)](#trigger-079d7e1c).
6. Enable and reset applicable timers for [SP3.6_Move_2 Jurassic (0952ED0C)](#trigger-0952ed0c).
7. Enable and reset applicable timers for [SP3.7a_Camera Move 2 BQ (0999579C)](#trigger-0999579c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9466, Events line 9770, Actions line 10074.

<a id="trigger-0951740c"></a>

### 101. SP3.3_Setup_Part II - 0951740C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.2_Audio_EnoughPower (0951864C)](#trigger-0951864c).

Attached scope: tag definitions 095171AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP3.4_TimeMachine II (0952C96C)](#trigger-0952c96c).
2. Reveal terrain around waypoint 68 (cell 182, 138).
3. Reveal terrain around waypoint 502 (cell 174, 136).
4. Reveal terrain around waypoint 503 (cell 164, 129).
5. Teleport the trigger owner's supported objects toward waypoint 478 (cell 43, 86).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9467, Events line 9771, Actions line 10075.

<a id="trigger-0bde0adc"></a>

### 102. SP3.2a_Camera_Jump 2 BK - 0BDE0ADC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.2_Audio_EnoughPower (0951864C)](#trigger-0951864c).

Attached scope: tag definitions 0BDE089C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 62 (cell 147, 99).
2. Play sound CameraSwitch.
3. Disable player input.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9468, Events line 9772, Actions line 10076.

<a id="trigger-06a25f3c"></a>

### 103. Reinforce_6 Engineers - 06A25F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Engineers Dead (0DD0203C)](#trigger-0dd0203c).

Attached scope: tag definitions 06A48D5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Reinforce_6 Engineers (06A25F3C)](#trigger-06a25f3c).
2. Supply reinforcement team [TM_Sov_6 Engineers (093D0EFC)](sov01umd-teams.md#team-093d0efc).
3. Enable and reset applicable timers for [Reinforce_6 Eng Audio (09FF490C)](#trigger-09ff490c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9469, Events line 9773, Actions line 10077.

<a id="trigger-0951a8bc"></a>

### 104. Animation_Time Effect - 0951A8BC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.5_Enable_TimeEffect (0BDE287C)](#trigger-0bde287c); enable from [SP4.4_Enable_TimeEffect (0BDCDD0C)](#trigger-0bdcdd0c).

Attached scope: tag definitions 0951A67C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Animation_Time Effect (0951A8BC)](#trigger-0951a8bc).
2. Chrono Screen Effect for; main setting 40.
3. Black out the trigger owner's radar for 60 configured frames.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9470, Events line 9774, Actions line 10078.

<a id="trigger-0e626a2c"></a>

### 105. SP3.5a_Evict Occupiers - 0E626A2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.5_Enable_TimeEffect (0BDE287C)](#trigger-0bde287c).

Attached scope: Office Building (CATEXS07), owner Neutral, cell (105, 105), tag 043E010C, persistence mode 2; Building (CANEWY18), owner Neutral, cell (105, 64), tag 043E010C, persistence mode 2; Building (CANEWY12), owner Neutral, cell (96, 133), tag 043E010C, persistence mode 2; Building (CAPARS04), owner Neutral, cell (97, 141), tag 043E010C, persistence mode 2; McBurger Kong (CAMSC10), owner Neutral, cell (97, 89), tag 043E010C, persistence mode 2; Warehouse (CANEWY21), owner Neutral, cell (90, 64), tag 043E010C, persistence mode 2; Building (CASTL02), owner Neutral, cell (122, 115), tag 043E010C, persistence mode 2; Building (CACHIG02), owner Neutral, cell (120, 104), tag 043E010C, persistence mode 2; Building (CAPARS06), owner Neutral, cell (120, 107), tag 043E010C, persistence mode 2; House (CAHSE07), owner Neutral, cell (124, 96), tag 043E010C, persistence mode 2; Building (CARUS06), owner Neutral, cell (124, 89), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (116, 96), tag 043E010C, persistence mode 2; Building (CACHIG02), owner Neutral, cell (122, 112), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (108, 122), tag 043E010C, persistence mode 2; Building (CACHIG02), owner Neutral, cell (120, 92), tag 043E010C, persistence mode 2; Office Building (CATEXS07), owner Neutral, cell (116, 75), tag 043E010C, persistence mode 2; Building (CANEWY12), owner Neutral, cell (107, 133), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (125, 121), tag 043E010C, persistence mode 2; Building (CACHIG02), owner Neutral, cell (105, 96), tag 043E010C, persistence mode 2; Building (CACHIG02), owner Neutral, cell (105, 93), tag 043E010C, persistence mode 2; Building (CASTL02), owner Neutral, cell (103, 89), tag 043E010C, persistence mode 2; Building (CACHIG01), owner Neutral, cell (104, 81), tag 043E010C, persistence mode 2; Gas Station (CAGAS01), owner Neutral, cell (99, 97), tag 043E010C, persistence mode 2; Building (CAPARS04), owner Neutral, cell (100, 74), tag 043E010C, persistence mode 2; Building (CAWASH07), owner Neutral, cell (97, 128), tag 043E010C, persistence mode 2; Building (CAWASH05), owner Neutral, cell (101, 128), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (118, 96), tag 043E010C, persistence mode 2; Office Building (CATEXS08), owner Neutral, cell (93, 81), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (99, 122), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (97, 122), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (101, 122), tag 043E010C, persistence mode 2; Hotel (CAMIAM03), owner Neutral, cell (70, 84), tag 043E010C, persistence mode 2; Building (CANEWY11), owner Neutral, cell (75, 82), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (80, 89), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (84, 89), tag 043E010C, persistence mode 2; Building (CAPARS14), owner Neutral, cell (72, 115), tag 043E010C, persistence mode 2; Building (CAWASH03), owner Neutral, cell (103, 113), tag 043E010C, persistence mode 2; Building (CACHIG02), owner Neutral, cell (96, 137), tag 043E010C, persistence mode 2; Building (CAWASH05), owner Neutral, cell (99, 104), tag 043E010C, persistence mode 2; Building (CACHIG02), owner Neutral, cell (107, 128), tag 043E010C, persistence mode 2; Building (CASANF02), owner Neutral, cell (84, 122), tag 043E010C, persistence mode 2; Building (CASANF03), owner Neutral, cell (87, 122), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (89, 122), tag 043E010C, persistence mode 2; Building (CASANF02), owner Neutral, cell (91, 122), tag 043E010C, persistence mode 2; Building (CASANF03), owner Neutral, cell (103, 122), tag 043E010C, persistence mode 2; Building (CASANF02), owner Neutral, cell (110, 122), tag 043E010C, persistence mode 2; Building (CASANF03), owner Neutral, cell (120, 96), tag 043E010C, persistence mode 2; Building (CASANF03), owner Neutral, cell (82, 89), tag 043E010C, persistence mode 2; Building (CASANF03), owner Neutral, cell (123, 121), tag 043E010C, persistence mode 2; Building (CASANF01), owner Neutral, cell (121, 121), tag 043E010C, persistence mode 2; Building (CACHIG01), owner Neutral, cell (111, 128), tag 043E010C, persistence mode 2; Gas Station (CAGAS01), owner Neutral, cell (111, 107), tag 043E010C, persistence mode 2; Office Building (CATEXS08), owner Neutral, cell (115, 90), tag 043E010C, persistence mode 2; Building (CASANF03), owner Neutral, cell (126, 107), tag 043E010C, persistence mode 2; Communications Center (CATECH01), owner Neutral, cell (137, 90), tag 043E010C, persistence mode 2; Building (CACHIG01), owner Neutral, cell (101, 81), tag 043E010C, persistence mode 2; Building (CACHIG01), owner Neutral, cell (98, 81), tag 043E010C, persistence mode 2; Outhouse (CAFRMB), owner Neutral, cell (119, 85), tag 043E010C, persistence mode 2; Building (CACHIG03), owner Neutral, cell (91, 103), tag 043E010C, persistence mode 2; Building (CACHIG03), owner Neutral, cell (91, 106), tag 043E010C, persistence mode 2; Building (CASTL01), owner Neutral, cell (78, 79), tag 043E010C, persistence mode 2; Office Building (CATEXS07), owner Neutral, cell (94, 72), tag 043E010C, persistence mode 2.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Disable [SP3.5a_Evict Occupiers (0E626A2C)](#trigger-0e626a2c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9471, Events line 9775, Actions line 10079.

<a id="trigger-0952ed0c"></a>

### 106. SP3.6_Move_2 Jurassic - 0952ED0C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.5_Enable_TimeEffect (0BDE287C)](#trigger-0bde287c).

Attached scope: tag definitions 0952EC2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Resize Player View; main setting 0; parameter 1: 4, parameter 2: 104, parameter 3: 54, parameter 4: 33.
2. Jump the camera to waypoint 50 (cell 158, 124).
3. Enable and reset applicable timers for [SP3.7_Movie_ZofiaDino (0952E0FC)](#trigger-0952e0fc).
4. Destroy all Land Units of: owner selector 0 (country/type AMERICANS; placed owner Americans).
5. Destroy all Land Units of: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
6. Destroy all Land Units of: owner selector 11 (country/type NOD; placed owner Nod).
7. Teleport the trigger owner's supported objects toward waypoint 68 (cell 182, 138).
8. Enable and reset applicable timers for [SP3.6a_Close Out SF (0C4A628C)](#trigger-0c4a628c).
9. Destroy all Land Units of: owner selector 6 (country/type ARABS; placed owner Arabs).
10. Destroy all Naval Units of: owner selector 6 (country/type ARABS; placed owner Arabs).
11. Enable and reset applicable timers for [Detect_All Sov Dead (097154CC)](#trigger-097154cc).
12. Enable and reset applicable timers for [Give_TimeTroops2Player (05BF138C)](#trigger-05bf138c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9472, Events line 9776, Actions line 10080.

<a id="trigger-0999579c"></a>

### 107. SP3.7a_Camera Move 2 BQ - 0999579C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.5_Enable_TimeEffect (0BDE287C)](#trigger-0bde287c).

Attached scope: tag definitions 099956BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 16 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 68 (cell 182, 138) with speed setting 1.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9473, Events line 9777, Actions line 10081.

<a id="trigger-0952c96c"></a>

### 108. SP3.4_TimeMachine II - 0952C96C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.3_Setup_Part II (0951740C)](#trigger-0951740c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [SP3.4_TimeMachine II (0952C96C)](#trigger-0952c96c).
2. Change House: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9474, Events line 9778, Actions line 10082.

<a id="trigger-09ff490c"></a>

### 109. Reinforce_6 Eng Audio - 09FF490C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce_6 Engineers (06A25F3C)](#trigger-06a25f3c).

Attached scope: tag definitions 09FF482C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Reinforce_6 Eng Audio (09FF490C)](#trigger-09ff490c).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Create radar-event marker type 2 at waypoint 114 (cell 130, 101).
4. Display message “Engineers have arrived near the Time Machine” (MISSION:MoreEngn).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9475, Events line 9779, Actions line 10083.

<a id="trigger-0952e0fc"></a>

### 110. SP3.7_Movie_ZofiaDino - 0952E0FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6_Move_2 Jurassic (0952ED0C)](#trigger-0952ed0c).

Attached scope: tag definitions 0952FDAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 24 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 35.
2. Enable and reset applicable timers for [SP3.8_Timer_Recharge (0952F87C)](#trigger-0952f87c).
3. Disable player input.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9476, Events line 9780, Actions line 10084.

<a id="trigger-0c4a628c"></a>

### 111. SP3.6a_Close Out SF - 0C4A628C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6_Move_2 Jurassic (0952ED0C)](#trigger-0952ed0c).

Attached scope: tag definitions 0C4A61AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Audio_Don't Attack Time (06C0F45C)](#trigger-06c0f45c).
2. Disable [Audio_Don't Attack Yuri (0439013C)](#trigger-0439013c).
3. Disable [Audio_Time Machine Off (094A4ADC)](#trigger-094a4adc).
4. Disable [Detect_Engineers Dead (0DD0203C)](#trigger-0dd0203c).
5. Disable [Detect_Plant1 Destroyed (06B369EC)](#trigger-06b369ec).
6. Disable [Detect_Plant2 Destroyed (06B3647C)](#trigger-06b3647c).
7. Disable [Detect_Plant3 Destroyed (06B3664C)](#trigger-06b3664c).
8. Disable [Detect_Plant4 Destroyed (06B3681C)](#trigger-06b3681c).
9. Disable [Detect_Plant5 Destroyed (06B37D6C)](#trigger-06b37d6c).
10. Disable [Detect_Plant6 Destroyed (06B37F3C)](#trigger-06b37f3c).
11. Disable [Detect_Power Attacked (0951918C)](#trigger-0951918c).
12. Disable [Detect_Tech Power 1 (0951972C)](#trigger-0951972c).
13. Disable [Detect_< 4 Power (06B6156C)](#trigger-06b6156c).
14. Enable and reset applicable timers for [SP3.6b_Remove_Dominator (0961762C)](#trigger-0961762c).
15. Enable and reset applicable timers for [SP3.6d_House 2 Allies (0441BAAC)](#trigger-0441baac).
16. Enable and reset applicable timers for [SP3.6e_Close Out SF 2 (0C57BA6C)](#trigger-0c57ba6c).
17. Disable [Detect_Dominator Active (0971599C)](#trigger-0971599c).
18. Enable and reset applicable timers for [SP3.6aa_Close Out SF (07FA53DC)](#trigger-07fa53dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9477, Events line 9781, Actions line 10085.

<a id="trigger-097154cc"></a>

### 112. Detect_All Sov Dead - 097154CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6_Move_2 Jurassic (0952ED0C)](#trigger-0952ed0c).

Attached scope: tag definitions 097153EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Display message “All Soviet forces lost” (MISSION:LostAll).
2. Enable and reset applicable timers for [_End_Lose (06B602BC)](#trigger-06b602bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9478, Events line 9782, Actions line 10086.

<a id="trigger-05bf138c"></a>

### 113. Give_TimeTroops2Player - 05BF138C

Owner reference: Soviet2 Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6_Move_2 Jurassic (0952ED0C)](#trigger-0952ed0c).

Attached scope: Rhino Heavy Tank (HTNK), owner Soviet2House, cell (186, 136), tag 05BF034C, persistence mode 2; Rhino Heavy Tank (HTNK), owner Soviet2House, cell (186, 134), tag 05BF034C, persistence mode 2; Rhino Heavy Tank (HTNK), owner Soviet2House, cell (188, 136), tag 05BF034C, persistence mode 2; Rhino Heavy Tank (HTNK), owner Soviet2House, cell (186, 142), tag 05BF034C, persistence mode 2; Rhino Heavy Tank (HTNK), owner Soviet2House, cell (186, 140), tag 05BF034C, persistence mode 2; Rhino Heavy Tank (HTNK), owner Soviet2House, cell (188, 140), tag 05BF034C, persistence mode 2; Conscript (E2), owner Soviet2House, cell (187, 142), tag 05BF034C, persistence mode 2; Conscript (E2), owner Soviet2House, cell (185, 141), tag 05BF034C, persistence mode 2; Conscript (E2), owner Soviet2House, cell (187, 135), tag 05BF034C, persistence mode 2; Conscript (E2), owner Soviet2House, cell (186, 135), tag 05BF034C, persistence mode 2; Conscript (E2), owner Soviet2House, cell (185, 135), tag 05BF034C, persistence mode 2; Conscript (E2), owner Soviet2House, cell (186, 141), tag 05BF034C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Give_TimeTroops2Player (05BF138C)](#trigger-05bf138c).
2. Change House: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9479, Events line 9783, Actions line 10087.

<a id="trigger-0952f87c"></a>

### 114. SP3.8_Timer_Recharge - 0952F87C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.7_Movie_ZofiaDino (0952E0FC)](#trigger-0952e0fc).

Attached scope: tag definitions 0952F79C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 62 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 120 configured time units.
2. Start the visible mission timer.
3. Use countdown label “Time Machine Recharged in:” (MISSION:TmeTimer).
4. Enable and reset applicable timers for [SP4.1_Detect_Timer Exp (0BDE333C)](#trigger-0bde333c).
5. Enable and reset applicable timers for [SP3.9_Reinforce_Dino1 (0B554AFC)](#trigger-0b554afc).
6. Display message “Objective: Defend the Time Machine until it can be reactivated.” (MISSION:Sov1Obj5).
7. Enable and reset applicable timers for [Text_Objective 3a (043E763C)](#trigger-043e763c).
8. Enable player input.
9. Play voice notification EVA_BattlefieldControlOnline.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9480, Events line 9784, Actions line 10088.

<a id="trigger-0dd0203c"></a>

### 115. Detect_Engineers Dead - 0DD0203C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0DD105AC (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Reinforce_6 Engineers (06A25F3C)](#trigger-06a25f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9481, Events line 9785, Actions line 10089.

<a id="trigger-06b369ec"></a>

### 116. Detect_Plant1 Destroyed - 06B369EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B3690C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of GAPOWRA exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).
2. Enable and reset applicable timers for [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9482, Events line 9786, Actions line 10090.

<a id="trigger-06b3647c"></a>

### 117. Detect_Plant2 Destroyed - 06B3647C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B360DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of GAPOWRB exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).
2. Enable and reset applicable timers for [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9483, Events line 9787, Actions line 10091.

<a id="trigger-06b3664c"></a>

### 118. Detect_Plant3 Destroyed - 06B3664C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B3656C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of GAPOWRC exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).
2. Enable and reset applicable timers for [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9484, Events line 9788, Actions line 10092.

<a id="trigger-06b3681c"></a>

### 119. Detect_Plant4 Destroyed - 06B3681C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B3673C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of GAPOWRD exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).
2. Enable and reset applicable timers for [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9485, Events line 9789, Actions line 10093.

<a id="trigger-06b37d6c"></a>

### 120. Detect_Plant5 Destroyed - 06B37D6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B37C8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of GAPOWRE exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).
2. Enable and reset applicable timers for [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9486, Events line 9790, Actions line 10094.

<a id="trigger-06b37f3c"></a>

### 121. Detect_Plant6 Destroyed - 06B37F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B37E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of GAPOWRF exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).
2. Enable and reset applicable timers for [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9487, Events line 9791, Actions line 10095.

<a id="trigger-0951918c"></a>

### 122. Detect_Power Attacked - 0951918C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change_Power 2 Allies (0C46AB3C)](#trigger-0c46ab3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Disable [Detect_Power Attacked (0951918C)](#trigger-0951918c).
2. Play voice notification Mis_xS1_ZofiaDoNotKillPower.
3. Display message “WARNING - Critical structure. Do not destroy!!!” (MISSION:WarnStct).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9488, Events line 9792, Actions line 10096.

<a id="trigger-0951972c"></a>

### 123. Detect_Tech Power 1 - 0951972C

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 369 (global list position: Spotlight (CAURB03)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Disable_All Tech Checks (0442C90C)](#trigger-0442c90c).
2. Enable and reset applicable timers for [Audio_Yuri Almost Power (04429F3C)](#trigger-04429f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9489, Events line 9793, Actions line 10097.

<a id="trigger-06b6156c"></a>

### 124. Detect_< 4 Power - 06B6156C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_3 PP Gone False (06B8F9CC)](#trigger-06b8f9cc).

Attached scope: tag definitions 06B6148C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaNoPowerLeft.
2. Enable and reset applicable timers for [_End_Lose (06B602BC)](#trigger-06b602bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9490, Events line 9794, Actions line 10098.

<a id="trigger-0961762c"></a>

### 125. SP3.6b_Remove_Dominator - 0961762C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6a_Close Out SF (0C4A628C)](#trigger-0c4a628c).

Attached scope: Psychic Dominator (YAPPET), owner Arabs, cell (18, 48), tag 0C479C7C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.
2. Enable and reset applicable timers for [SP3.6c_Psy Dom 2 Dead (0C47F71C)](#trigger-0c47f71c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9491, Events line 9795, Actions line 10099.

<a id="trigger-0441baac"></a>

### 126. SP3.6d_House 2 Allies - 0441BAAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6a_Close Out SF (0C4A628C)](#trigger-0c4a628c).

Attached scope: tag definitions 0975F31C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9492, Events line 9796, Actions line 10100.

<a id="trigger-0c57ba6c"></a>

### 127. SP3.6e_Close Out SF 2 - 0C57BA6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6a_Close Out SF (0C4A628C)](#trigger-0c4a628c).

Attached scope: tag definitions 0C57B98C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Reinforce_Atk Group 1 (043DF33C)](#trigger-043df33c).
2. Disable [Reinforce_Atk Group 2 (06A6629C)](#trigger-06a6629c).
3. Disable [Reinforce_Cap Delay (06A6663C)](#trigger-06a6663c).
4. Disable [Reinforce_Cap Group 1 (0B454BBC)](#trigger-0b454bbc).
5. Disable [Reinforce_Cap Group 2 (06A6646C)](#trigger-06a6646c).
6. Disable [Create_Gas Atk Trans (06A672DC)](#trigger-06a672dc).
7. Disable [Create_Gas Cap Trans (06A68F3C)](#trigger-06a68f3c).
8. Disable [Create_Grand Atk Trans (06A6680C)](#trigger-06a6680c).
9. Disable [Create_Grand Cap Trans (06A67A6C)](#trigger-06a67a6c).
10. Disable [Create_NTime Atk Trans (06A674AC)](#trigger-06a674ac).
11. Disable [Create_NTime Cap Trans (06A6710C)](#trigger-06a6710c).
12. Disable [Create_Park Atk Trans (06A66BAC)](#trigger-06a66bac).
13. Disable [Create_Park Cap Trans (06A660CC)](#trigger-06a660cc).
14. Disable [Create_Statue Atk Trans (06A669DC)](#trigger-06a669dc).
15. Disable [Create_Statue Cap Trans (06A67E5C)](#trigger-06a67e5c).
16. Disable [Create_STime Atk Trans (06A6767C)](#trigger-06a6767c).
17. Disable [Create_STime Cap Trans (0B44E12C)](#trigger-0b44e12c).
18. Enable and reset applicable timers for [SP3.6f_Take Hospital (06B5FB2C)](#trigger-06b5fb2c).
19. Enable and reset applicable timers for [SP3.6h_Clean up SF (096879AC)](#trigger-096879ac).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9493, Events line 9797, Actions line 10101.

<a id="trigger-0971599c"></a>

### 128. Detect_Dominator Active - 0971599C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097158BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Power Full: owner selector 6 (country/type ARABS; placed owner Arabs).

**Then perform these actions in order:**

1. Play sound AirRaidSiren.
2. Display message “The Psychic Dominator is now armed!!!” (MISSION:DomArmed).
3. Play voice notification EVA_PsychicDominatorDetected.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9494, Events line 9798, Actions line 10102.

<a id="trigger-07fa53dc"></a>

### 129. SP3.6aa_Close Out SF - 07FA53DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6a_Close Out SF (0C4A628C)](#trigger-0c4a628c).

Attached scope: tag definitions 07FA52FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Detect_Backup 1 Unload (0B603E5C)](#trigger-0b603e5c).
2. Destroy current instances of [Detect_Backup 2 Unload (0B60744C)](#trigger-0b60744c).
3. Destroy current instances of [Reinforce_6 Engineers (06A25F3C)](#trigger-06a25f3c).
4. Destroy current instances of [Reinforce_6 Eng Audio (09FF490C)](#trigger-09ff490c).
5. Destroy current instances of [Reinforce_Backup Cons (082C467C)](#trigger-082c467c).
6. Destroy current instances of [Reinforce_Backup Rhinos (082C44AC)](#trigger-082c44ac).
7. Destroy current instances of [Detect_Engineers Dead (0DD0203C)](#trigger-0dd0203c).
8. Destroy current instances of [Detect_Lost 1st Tanks (082C3CEC)](#trigger-082c3cec).
9. Destroy current instances of [Detect_Dead Conscripts (082C79BC)](#trigger-082c79bc).
10. Destroy current instances of [Detect_Dead Rhinos (082C77EC)](#trigger-082c77ec).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9495, Events line 9799, Actions line 10103.

<a id="trigger-0bde333c"></a>

### 130. SP4.1_Detect_Timer Exp - 0BDE333C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.8_Timer_Recharge (0952F87C)](#trigger-0952f87c).

Attached scope: tag definitions 0BDE0C9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The visible mission countdown has expired.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP4.2_Audio_Time Ready (0BDE064C)](#trigger-0bde064c).
2. Disable [SP3.9_Reinforce_Dino1 (0B554AFC)](#trigger-0b554afc).
3. Disable [SP3.10_Reinforce_Dino2 (0B557E6C)](#trigger-0b557e6c).
4. Disable [Text_Objective 3a (043E763C)](#trigger-043e763c).
5. Enable and reset applicable timers for [Text_Objective Complete (07EF43CC)](#trigger-07ef43cc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9496, Events line 9800, Actions line 10104.

<a id="trigger-0b554afc"></a>

### 131. SP3.9_Reinforce_Dino1 - 0B554AFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.8_Timer_Recharge (0952F87C)](#trigger-0952f87c); enable from [SP3.10_Reinforce_Dino2 (0B557E6C)](#trigger-0b557e6c).

Attached scope: tag definitions 0B5563BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 10 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Disable [SP3.9_Reinforce_Dino1 (0B554AFC)](#trigger-0b554afc).
2. Supply reinforcement team [TM_Jurassic_TRex @ BR (0BB6F1DC)](sov01umd-teams.md#team-0bb6f1dc).
3. Enable and reset applicable timers for [SP3.10_Reinforce_Dino2 (0B557E6C)](#trigger-0b557e6c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9497, Events line 9801, Actions line 10105.

<a id="trigger-043e763c"></a>

### 132. Text_Objective 3a - 043E763C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.8_Timer_Recharge (0952F87C)](#trigger-0952f87c).

Attached scope: tag definitions 043E755C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Defend the Time Machine until it can be reactivated.” (MISSION:Sov1Obj5).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9498, Events line 9802, Actions line 10106.

<a id="trigger-06b8e14c"></a>

### 133. Detect_1 PP Gone False - 06B8E14C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Plant1 Destroyed (06B369EC)](#trigger-06b369ec); enable from [Detect_Plant2 Destroyed (06B3647C)](#trigger-06b3647c); enable from [Detect_Plant3 Destroyed (06B3664C)](#trigger-06b3664c); enable from [Detect_Plant4 Destroyed (06B3681C)](#trigger-06b3681c); enable from [Detect_Plant5 Destroyed (06B37D6C)](#trigger-06b37d6c); enable from [Detect_Plant6 Destroyed (06B37F3C)](#trigger-06b37f3c).

Attached scope: tag definitions 06B9006C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 40 (1 PP Gone) is set.

Flag writers in this mission: set local flag 40 (1 PP Gone) at [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c).
2. Disable [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).
3. Enable and reset applicable timers for [Detect_2 PP Gone True (06B8FF3C)](#trigger-06b8ff3c).
4. Enable and reset applicable timers for [Detect_2 PP Gone False (06B8FD6C)](#trigger-06b8fd6c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9499, Events line 9803, Actions line 10107.

<a id="trigger-06b8e31c"></a>

### 134. Detect_1 PP Gone True - 06B8E31C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Plant1 Destroyed (06B369EC)](#trigger-06b369ec); enable from [Detect_Plant2 Destroyed (06B3647C)](#trigger-06b3647c); enable from [Detect_Plant3 Destroyed (06B3664C)](#trigger-06b3664c); enable from [Detect_Plant4 Destroyed (06B3681C)](#trigger-06b3681c); enable from [Detect_Plant5 Destroyed (06B37D6C)](#trigger-06b37d6c); enable from [Detect_Plant6 Destroyed (06B37F3C)](#trigger-06b37f3c).

Attached scope: tag definitions 06B9051C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 40 (1 PP Gone) is clear.

Flag writers in this mission: set local flag 40 (1 PP Gone) at [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).
2. Set local flag 40 (1 PP Gone).
3. Disable [Detect_1 PP Gone True (06B8E31C)](#trigger-06b8e31c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9500, Events line 9804, Actions line 10108.

<a id="trigger-0c46ab3c"></a>

### 135. Change_Power 2 Allies - 0C46AB3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.4_Enable_TimeEffect (0BDCDD0C)](#trigger-0bdcdd0c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Change_Power 2 Allies (0C46AB3C)](#trigger-0c46ab3c).
2. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9501, Events line 9805, Actions line 10109.

<a id="trigger-0442c90c"></a>

### 136. Disable_All Tech Checks - 0442C90C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Tech Power 1 (0951972C)](#trigger-0951972c); enable from [Detect_Tech Power A (0442A5EC)](#trigger-0442a5ec); enable from [Detect_Tech Power B (0442A4FC)](#trigger-0442a4fc); enable from [Detect_Tech Power C (0442A40C)](#trigger-0442a40c); enable from [Detect_Tech Power D (0442A31C)](#trigger-0442a31c); enable from [Detect_Tech Power E (0442A22C)](#trigger-0442a22c); enable from [Detect_Tech Power F (0442A13C)](#trigger-0442a13c).

Attached scope: tag definitions 0442C82C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Detect_Tech Power 1 (0951972C)](#trigger-0951972c).
2. Disable [Detect_Tech Power A (0442A5EC)](#trigger-0442a5ec).
3. Disable [Detect_Tech Power B (0442A4FC)](#trigger-0442a4fc).
4. Disable [Detect_Tech Power C (0442A40C)](#trigger-0442a40c).
5. Disable [Detect_Tech Power D (0442A31C)](#trigger-0442a31c).
6. Disable [Detect_Tech Power E (0442A22C)](#trigger-0442a22c).
7. Disable [Detect_Tech Power F (0442A13C)](#trigger-0442a13c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9502, Events line 9806, Actions line 10110.

<a id="trigger-04429f3c"></a>

### 137. Audio_Yuri Almost Power - 04429F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Tech Power 1 (0951972C)](#trigger-0951972c); enable from [Detect_Tech Power A (0442A5EC)](#trigger-0442a5ec); enable from [Detect_Tech Power B (0442A4FC)](#trigger-0442a4fc); enable from [Detect_Tech Power C (0442A40C)](#trigger-0442a40c); enable from [Detect_Tech Power D (0442A31C)](#trigger-0442a31c); enable from [Detect_Tech Power E (0442A22C)](#trigger-0442a22c); enable from [Detect_Tech Power F (0442A13C)](#trigger-0442a13c).

Attached scope: tag definitions 04429E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaYuriAlmostPowered.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9503, Events line 9807, Actions line 10111.

<a id="trigger-0c47f71c"></a>

### 138. SP3.6c_Psy Dom 2 Dead - 0C47F71C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6b_Remove_Dominator (0961762C)](#trigger-0961762c).

Attached scope: Psychic Dominator (YAPPPT), owner YuriCountry, cell (39, 69), tag 0C47FB1C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_End_Win (06B600EC)](#trigger-06b600ec).
2. Disable [Text_Objective 4b (043E7D0C)](#trigger-043e7d0c).
3. Enable and reset applicable timers for [Complete_Objective 4 (08E497AC)](#trigger-08e497ac).
4. Make side cheer: owner selector 8 (country/type RUSSIANS; placed owner Russians).
5. Jump the camera to waypoint 144 (cell 40, 70).
6. Play sound CameraSwitch.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9504, Events line 9808, Actions line 10112.

<a id="trigger-06a672dc"></a>

### 139. Create_Gas Atk Trans - 06A672DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_GasAtk_Unloaded (0C123B9C)](#trigger-0c123b9c).

Attached scope: tag definitions 06A671FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 30 (Gas Atk_Unloaded) is set.

Flag writers in this mission: clear local flag 30 (Gas Atk_Unloaded) at [Clear_GasAtk_Unloaded (0C123B9C)](#trigger-0c123b9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Yuri_Gas Trans Unloaded (0BB936AC)](sov01umd-teams.md#team-0bb936ac).
2. Disable [Create_Gas Atk Trans (06A672DC)](#trigger-06a672dc).
3. Enable and reset applicable timers for [Clear_GasAtk_Unloaded (0C123B9C)](#trigger-0c123b9c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9505, Events line 9809, Actions line 10113.

<a id="trigger-06a68f3c"></a>

### 140. Create_Gas Cap Trans - 06A68F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_GasCap_Unloaded (0C123D6C)](#trigger-0c123d6c).

Attached scope: tag definitions 06A68E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 36 (Gas Cap_Unloaded) is set.

Flag writers in this mission: clear local flag 36 (Gas Cap_Unloaded) at [Clear_GasCap_Unloaded (0C123D6C)](#trigger-0c123d6c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Arab_Gas Trans Unloaded (0BB91C8C)](sov01umd-teams.md#team-0bb91c8c).
2. Disable [Create_Gas Cap Trans (06A68F3C)](#trigger-06a68f3c).
3. Enable and reset applicable timers for [Clear_GasCap_Unloaded (0C123D6C)](#trigger-0c123d6c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9506, Events line 9810, Actions line 10114.

<a id="trigger-06a6680c"></a>

### 141. Create_Grand Atk Trans - 06A6680C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_GrandAtk_Unloaded (0C122A1C)](#trigger-0c122a1c).

Attached scope: tag definitions 06A6672C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 27 (Grand Atk_Unloaded) is set.

Flag writers in this mission: clear local flag 27 (Grand Atk_Unloaded) at [Clear_GrandAtk_Unloaded (0C122A1C)](#trigger-0c122a1c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Yuri_Grand Trans Unloaded (0BB9441C)](sov01umd-teams.md#team-0bb9441c).
2. Disable [Create_Grand Atk Trans (06A6680C)](#trigger-06a6680c).
3. Enable and reset applicable timers for [Clear_GrandAtk_Unloaded (0C122A1C)](#trigger-0c122a1c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9507, Events line 9811, Actions line 10115.

<a id="trigger-06a67a6c"></a>

### 142. Create_Grand Cap Trans - 06A67A6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_GrandCap_Unloaded (0C122E5C)](#trigger-0c122e5c).

Attached scope: tag definitions 06A6798C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 36 (Gas Cap_Unloaded) is set.

Flag writers in this mission: clear local flag 36 (Gas Cap_Unloaded) at [Clear_GasCap_Unloaded (0C123D6C)](#trigger-0c123d6c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Arab_Grand Trans Unloaded (0BB92A1C)](sov01umd-teams.md#team-0bb92a1c).
2. Disable [Create_Grand Cap Trans (06A67A6C)](#trigger-06a67a6c).
3. Enable and reset applicable timers for [Clear_GrandCap_Unloaded (0C122E5C)](#trigger-0c122e5c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9508, Events line 9812, Actions line 10116.

<a id="trigger-06a674ac"></a>

### 143. Create_NTime Atk Trans - 06A674AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_NTimeAtk_Unloaded (0BE602DC)](#trigger-0be602dc).

Attached scope: tag definitions 06A673CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 31 (NTime Atk_Unloaded) is set.

Flag writers in this mission: clear local flag 31 (NTime Atk_Unloaded) at [Clear_NTimeAtk_Unloaded (0BE602DC)](#trigger-0be602dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Yuri_NTime Trans Unloaded (0BB9330C)](sov01umd-teams.md#team-0bb9330c).
2. Disable [Create_NTime Atk Trans (06A674AC)](#trigger-06a674ac).
3. Enable and reset applicable timers for [Clear_NTimeAtk_Unloaded (0BE602DC)](#trigger-0be602dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9509, Events line 9813, Actions line 10117.

<a id="trigger-06a6710c"></a>

### 144. Create_NTime Cap Trans - 06A6710C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_NTimeCap_Unloaded (0C123F3C)](#trigger-0c123f3c).

Attached scope: tag definitions 0B44E21C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 37 (NTime Cap_Unloaded) is set.

Flag writers in this mission: clear local flag 37 (NTime Cap_Unloaded) at [Clear_NTimeCap_Unloaded (0C123F3C)](#trigger-0c123f3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Arab_NTime Trans Unloaded (0BB918EC)](sov01umd-teams.md#team-0bb918ec).
2. Disable [Create_NTime Cap Trans (06A6710C)](#trigger-06a6710c).
3. Enable and reset applicable timers for [Clear_NTimeCap_Unloaded (0C123F3C)](#trigger-0c123f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9510, Events line 9814, Actions line 10118.

<a id="trigger-06a66bac"></a>

### 145. Create_Park Atk Trans - 06A66BAC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_ParkAtk_Unloaded (0C1237FC)](#trigger-0c1237fc).

Attached scope: tag definitions 06A66ACC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 29 (Park Atk_Unloaded) is set.

Flag writers in this mission: clear local flag 29 (Park Atk_Unloaded) at [Clear_ParkAtk_Unloaded (0C1237FC)](#trigger-0c1237fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Yuri_Park Trans Unloaded (0BB93A4C)](sov01umd-teams.md#team-0bb93a4c).
2. Disable [Create_Park Atk Trans (06A66BAC)](#trigger-06a66bac).
3. Enable and reset applicable timers for [Clear_ParkAtk_Unloaded (0C1237FC)](#trigger-0c1237fc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9511, Events line 9815, Actions line 10119.

<a id="trigger-06a660cc"></a>

### 146. Create_Park Cap Trans - 06A660CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_ParkCap_Unloaded (0C1239CC)](#trigger-0c1239cc).

Attached scope: tag definitions 06A67F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 35 (Park Cap_Unloaded) is set.

Flag writers in this mission: clear local flag 35 (Park Cap_Unloaded) at [Clear_ParkCap_Unloaded (0C1239CC)](#trigger-0c1239cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Arab_Park Trans Unloaded (0BB921CC)](sov01umd-teams.md#team-0bb921cc).
2. Disable [Create_Park Cap Trans (06A660CC)](#trigger-06a660cc).
3. Enable and reset applicable timers for [Clear_ParkCap_Unloaded (0C1239CC)](#trigger-0c1239cc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9512, Events line 9816, Actions line 10120.

<a id="trigger-06a669dc"></a>

### 147. Create_Statue Atk Trans - 06A669DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_StatueAtk_Unloade (0C12345C)](#trigger-0c12345c).

Attached scope: tag definitions 06A668FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 28 (Statue Atk_Unloaded) is set.

Flag writers in this mission: clear local flag 28 (Statue Atk_Unloaded) at [Clear_StatueAtk_Unloade (0C12345C)](#trigger-0c12345c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Yuri_Statue Trans Unloaded (0BB93DEC)](sov01umd-teams.md#team-0bb93dec).
2. Disable [Create_Statue Atk Trans (06A669DC)](#trigger-06a669dc).
3. Enable and reset applicable timers for [Clear_StatueAtk_Unloade (0C12345C)](#trigger-0c12345c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9513, Events line 9817, Actions line 10121.

<a id="trigger-06a67e5c"></a>

### 148. Create_Statue Cap Trans - 06A67E5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_StatueCap_Unloade (0C12362C)](#trigger-0c12362c).

Attached scope: tag definitions 06A67B5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 34 (Statue Cap_Unloaded) is set.

Flag writers in this mission: clear local flag 34 (Statue Cap_Unloaded) at [Clear_StatueCap_Unloade (0C12362C)](#trigger-0c12362c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Arab_Statue Trans Unloaded (0BB9256C)](sov01umd-teams.md#team-0bb9256c).
2. Disable [Create_Statue Cap Trans (06A67E5C)](#trigger-06a67e5c).
3. Enable and reset applicable timers for [Clear_StatueCap_Unloade (0C12362C)](#trigger-0c12362c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9514, Events line 9818, Actions line 10122.

<a id="trigger-06a6767c"></a>

### 149. Create_STime Atk Trans - 06A6767C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_STimeAtk_Unloaded (0C12423C)](#trigger-0c12423c).

Attached scope: tag definitions 06A6759C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 32 (STime Atk_Unloaded) is set.

Flag writers in this mission: clear local flag 32 (STime Atk_Unloaded) at [Clear_STimeAtk_Unloaded (0C12423C)](#trigger-0c12423c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Yuri_STime Trans Unloaded (0BB931DC)](sov01umd-teams.md#team-0bb931dc).
2. Disable [Create_STime Atk Trans (06A6767C)](#trigger-06a6767c).
3. Enable and reset applicable timers for [Clear_STimeAtk_Unloaded (0C12423C)](#trigger-0c12423c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9515, Events line 9819, Actions line 10123.

<a id="trigger-0b44e12c"></a>

### 150. Create_STime Cap Trans - 0B44E12C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Clear_STimeCap_Unloaded (0C12440C)](#trigger-0c12440c).

Attached scope: tag definitions 0B454CAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 38 (STime Cap_Unloaded) is set.

Flag writers in this mission: clear local flag 38 (STime Cap_Unloaded) at [Clear_STimeCap_Unloaded (0C12440C)](#trigger-0c12440c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Arab_STime Trans Unloaded (0BB9154C)](sov01umd-teams.md#team-0bb9154c).
2. Disable [Create_STime Cap Trans (0B44E12C)](#trigger-0b44e12c).
3. Enable and reset applicable timers for [Clear_STimeCap_Unloaded (0C12440C)](#trigger-0c12440c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9516, Events line 9820, Actions line 10124.

<a id="trigger-06b5fb2c"></a>

### 151. SP3.6f_Take Hospital - 06B5FB2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Audio_Intro Hospital (07837A2C)](#trigger-07837a2c).

Incoming activation links: enable from [SP3.6e_Close Out SF 2 (0C57BA6C)](#trigger-0c57ba6c).

Attached scope: Civilian Hospital (CATHOSP), owner Alliance, cell (90, 96), tag 0783794C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [SP3.6f_Take Hospital (06B5FB2C)](#trigger-06b5fb2c).
2. Enable and reset applicable timers for [SP3.6g_Take Mach Shop (06B5F54C)](#trigger-06b5f54c).
3. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9517, Events line 9821, Actions line 10125.

<a id="trigger-096879ac"></a>

### 152. SP3.6h_Clean up SF - 096879AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6e_Close Out SF 2 (0C57BA6C)](#trigger-0c57ba6c).

Attached scope: tag definitions 0968345C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy all Land Units of: owner selector 6 (country/type ARABS; placed owner Arabs).
2. Destroy all Naval Units of: owner selector 6 (country/type ARABS; placed owner Arabs).
3. Destroy all Land Units of: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
4. Destroy all Naval Units of: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
5. Destroy all of: owner selector 6 (country/type ARABS; placed owner Arabs).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9518, Events line 9822, Actions line 10126.

<a id="trigger-0b603e5c"></a>

### 153. Detect_Backup 1 Unload - 0B603E5C

Owner reference: Soviet2 Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B603D7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 43 (Player Reinforce 1 ) is set.

Flag writers in this mission: clear local flag 43 (Player Reinforce 1 ) at [Detect_Backup 1 Unload (0B603E5C)](#trigger-0b603e5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 43 (Player Reinforce 1 ).
2. Create/recruit team [TM_Sov2_Re_4 Rhino (07EC346C)](sov01umd-teams.md#team-07ec346c).
3. Play voice notification EVA_ReinforcementsHaveArrived.
4. Display message “More of our troops have arrived on the beach” (MISSION:MoreTrps).
5. Create radar-event marker type 2 at waypoint 56 (cell 79, 74).
6. Disable [Detect_Trans(Rhino)Dead (0959CAFC)](#trigger-0959cafc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9519, Events line 9823, Actions line 10127.

<a id="trigger-0b60744c"></a>

### 154. Detect_Backup 2 Unload - 0B60744C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B603F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 44 (Player Reinforce 2 ) is set.

Flag writers in this mission: clear local flag 44 (Player Reinforce 2 ) at [Detect_Backup 2 Unload (0B60744C)](#trigger-0b60744c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 44 (Player Reinforce 2 ).
2. Create/recruit team [TM_Sov2_Re_12 Conscript (07EC467C)](sov01umd-teams.md#team-07ec467c).
3. Play voice notification EVA_ReinforcementsHaveArrived.
4. Display message “More of our troops have arrived on the beach” (MISSION:MoreTrps).
5. Create radar-event marker type 2 at waypoint 55 (cell 78, 79).
6. Disable [Detect_Trans (Con) Dead (0959C92C)](#trigger-0959c92c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9520, Events line 9824, Actions line 10128.

<a id="trigger-082c467c"></a>

### 155. Reinforce_Backup Cons - 082C467C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Dead Conscripts (082C79BC)](#trigger-082c79bc); enable from [Detect_Trans (Con) Dead (0959C92C)](#trigger-0959c92c).

Attached scope: tag definitions 082C459C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Reinforce_Backup Cons (082C467C)](#trigger-082c467c).
2. Supply reinforcement team [TM_Sov2_1 Trans 12 Conscript (0999AEFC)](sov01umd-teams.md#team-0999aefc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9521, Events line 9825, Actions line 10129.

<a id="trigger-082c44ac"></a>

### 156. Reinforce_Backup Rhinos - 082C44AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Dead Rhinos (082C77EC)](#trigger-082c77ec); enable from [Detect_Trans(Rhino)Dead (0959CAFC)](#trigger-0959cafc).

Attached scope: tag definitions 082C43CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Reinforce_Backup Rhinos (082C44AC)](#trigger-082c44ac).
2. Supply reinforcement team [TM_Sov2_1 Trans 4 Rhino (0999948C)](sov01umd-teams.md#team-0999948c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9522, Events line 9826, Actions line 10130.

<a id="trigger-082c3cec"></a>

### 157. Detect_Lost 1st Tanks - 082C3CEC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 082C34CC (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov2_1 Trans 12 Conscript (0999AEFC)](sov01umd-teams.md#team-0999aefc).
2. Supply reinforcement team [TM_Sov2_1 Trans 4 Rhino (0999948C)](sov01umd-teams.md#team-0999948c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9523, Events line 9827, Actions line 10131.

<a id="trigger-082c79bc"></a>

### 158. Detect_Dead Conscripts - 082C79BC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 082C78DC (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Reinforce_Backup Cons (082C467C)](#trigger-082c467c).
2. Enable and reset applicable timers for [Detect_Trans (Con) Dead (0959C92C)](#trigger-0959c92c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9524, Events line 9828, Actions line 10132.

<a id="trigger-082c77ec"></a>

### 159. Detect_Dead Rhinos - 082C77EC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 082C770C (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Reinforce_Backup Rhinos (082C44AC)](#trigger-082c44ac).
2. Enable and reset applicable timers for [Detect_Trans(Rhino)Dead (0959CAFC)](#trigger-0959cafc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9525, Events line 9829, Actions line 10133.

<a id="trigger-0bde064c"></a>

### 160. SP4.2_Audio_Time Ready - 0BDE064C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.1_Detect_Timer Exp (0BDE333C)](#trigger-0bde333c).

Attached scope: tag definitions 0BDE056C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaTimeMachineReady.
2. Enable and reset applicable timers for [SP4.3_Camera_Jump to BQ (0BDC985C)](#trigger-0bdc985c).
3. Enable and reset applicable timers for [SP4.2a_Detect_BorisDead (0439E3FC)](#trigger-0439e3fc).
4. Enable and reset applicable timers for [SP4.2c_Detect_BorisLive (097651DC)](#trigger-097651dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9526, Events line 9830, Actions line 10134.

<a id="trigger-0b557e6c"></a>

### 161. SP3.10_Reinforce_Dino2 - 0B557E6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.9_Reinforce_Dino1 (0B554AFC)](#trigger-0b554afc).

Attached scope: tag definitions 0B557D8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 10 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Disable [SP3.10_Reinforce_Dino2 (0B557E6C)](#trigger-0b557e6c).
2. Supply reinforcement team [TM_Jurassic_TRex @ BS (095F399C)](sov01umd-teams.md#team-095f399c).
3. Enable and reset applicable timers for [SP3.9_Reinforce_Dino1 (0B554AFC)](#trigger-0b554afc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9527, Events line 9831, Actions line 10135.

<a id="trigger-07ef43cc"></a>

### 162. Text_Objective Complete - 07EF43CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.1_Detect_Timer Exp (0BDE333C)](#trigger-0bde333c); enable from [Audio_Sov Base Gained (0962D87C)](#trigger-0962d87c).

Attached scope: tag definitions 07EF42EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Text_Objective Complete (07EF43CC)](#trigger-07ef43cc).
2. Display message “Objective Complete” (MISSION:ObjCompleteSov04md).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9528, Events line 9832, Actions line 10136.

<a id="trigger-06b8ff3c"></a>

### 163. Detect_2 PP Gone True - 06B8FF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).

Attached scope: tag definitions 06B917DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 41 (2 PP Gone) is clear.

Flag writers in this mission: set local flag 41 (2 PP Gone) at [Detect_2 PP Gone True (06B8FF3C)](#trigger-06b8ff3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Detect_2 PP Gone False (06B8FD6C)](#trigger-06b8fd6c).
2. Set local flag 41 (2 PP Gone).
3. Disable [Detect_2 PP Gone True (06B8FF3C)](#trigger-06b8ff3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9529, Events line 9833, Actions line 10137.

<a id="trigger-06b8fd6c"></a>

### 164. Detect_2 PP Gone False - 06B8FD6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_1 PP Gone False (06B8E14C)](#trigger-06b8e14c).

Attached scope: tag definitions 06B9160C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 41 (2 PP Gone) is set.

Flag writers in this mission: set local flag 41 (2 PP Gone) at [Detect_2 PP Gone True (06B8FF3C)](#trigger-06b8ff3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Detect_2 PP Gone True (06B8FF3C)](#trigger-06b8ff3c).
2. Disable [Detect_2 PP Gone False (06B8FD6C)](#trigger-06b8fd6c).
3. Enable and reset applicable timers for [Detect_3 PP Gone True (06B8FB9C)](#trigger-06b8fb9c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9530, Events line 9834, Actions line 10138.

<a id="trigger-0442a5ec"></a>

### 165. Detect_Tech Power A - 0442A5EC

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Tech Power 1 (0951972C)](#trigger-0951972c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 402 (global list position: US Flag (CALUNR02)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Disable_All Tech Checks (0442C90C)](#trigger-0442c90c).
2. Enable and reset applicable timers for [Audio_Yuri Almost Power (04429F3C)](#trigger-04429f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9531, Events line 9835, Actions line 10139.

<a id="trigger-0442a4fc"></a>

### 166. Detect_Tech Power B - 0442A4FC

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Tech Power A (0442A5EC)](#trigger-0442a5ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 403. A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Disable_All Tech Checks (0442C90C)](#trigger-0442c90c).
2. Enable and reset applicable timers for [Audio_Yuri Almost Power (04429F3C)](#trigger-04429f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9532, Events line 9836, Actions line 10140.

<a id="trigger-0442a40c"></a>

### 167. Detect_Tech Power C - 0442A40C

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Tech Power B (0442A4FC)](#trigger-0442a4fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 404. A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Disable_All Tech Checks (0442C90C)](#trigger-0442c90c).
2. Enable and reset applicable timers for [Audio_Yuri Almost Power (04429F3C)](#trigger-04429f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9533, Events line 9837, Actions line 10141.

<a id="trigger-0442a31c"></a>

### 168. Detect_Tech Power D - 0442A31C

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Tech Power C (0442A40C)](#trigger-0442a40c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 405. A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Disable_All Tech Checks (0442C90C)](#trigger-0442c90c).
2. Enable and reset applicable timers for [Audio_Yuri Almost Power (04429F3C)](#trigger-04429f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9534, Events line 9838, Actions line 10142.

<a id="trigger-0442a22c"></a>

### 169. Detect_Tech Power E - 0442A22C

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Tech Power D (0442A31C)](#trigger-0442a31c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 406. A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Disable_All Tech Checks (0442C90C)](#trigger-0442c90c).
2. Enable and reset applicable timers for [Audio_Yuri Almost Power (04429F3C)](#trigger-04429f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9535, Events line 9839, Actions line 10143.

<a id="trigger-0442a13c"></a>

### 170. Detect_Tech Power F - 0442A13C

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Tech Power E (0442A22C)](#trigger-0442a22c).

Attached scope: tag definitions 0951964C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 407. A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Disable_All Tech Checks (0442C90C)](#trigger-0442c90c).
2. Enable and reset applicable timers for [Audio_Yuri Almost Power (04429F3C)](#trigger-04429f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9536, Events line 9840, Actions line 10144.

<a id="trigger-06b600ec"></a>

### 171. _End_Win - 06B600EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6c_Psy Dom 2 Dead (0C47F71C)](#trigger-0c47f71c).

Attached scope: tag definitions 06B61F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9537, Events line 9841, Actions line 10145.

<a id="trigger-043e7d0c"></a>

### 172. Text_Objective 4b - 043E7D0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Text/Ping_Obj7 Easy (07A255BC)](#trigger-07a255bc); enable from [Text/Ping_Obj7 Med (043EC4DC)](#trigger-043ec4dc); enable from [Text/Ping_Obj7 Hard (07A256AC)](#trigger-07a256ac).

Attached scope: tag definitions 043E7C2C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Destroy the Psychic Dominator.” (MISSION:Sov1Obj7).
2. Create radar-event marker type 12 at waypoint 144 (cell 40, 70).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9538, Events line 9842, Actions line 10146.

<a id="trigger-08e497ac"></a>

### 173. Complete_Objective 4 - 08E497AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6c_Psy Dom 2 Dead (0C47F71C)](#trigger-0c47f71c).

Attached scope: tag definitions 08E496CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 4 Complete.” (MISSION:Obj4Comp).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9539, Events line 9843, Actions line 10147.

<a id="trigger-0c123b9c"></a>

### 174. Clear_GasAtk_Unloaded - 0C123B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_Gas Atk Trans (06A672DC)](#trigger-06a672dc).

Attached scope: tag definitions 0C123ABC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_GasAtk_Unloaded (0C123B9C)](#trigger-0c123b9c).
2. Clear local flag 30 (Gas Atk_Unloaded).
3. Enable and reset applicable timers for [Create_Gas Atk Trans (06A672DC)](#trigger-06a672dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9540, Events line 9844, Actions line 10148.

<a id="trigger-0c123d6c"></a>

### 175. Clear_GasCap_Unloaded - 0C123D6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_Gas Cap Trans (06A68F3C)](#trigger-06a68f3c).

Attached scope: tag definitions 0C123C8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_GasCap_Unloaded (0C123D6C)](#trigger-0c123d6c).
2. Clear local flag 36 (Gas Cap_Unloaded).
3. Enable and reset applicable timers for [Create_Gas Cap Trans (06A68F3C)](#trigger-06a68f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9541, Events line 9845, Actions line 10149.

<a id="trigger-0c122a1c"></a>

### 176. Clear_GrandAtk_Unloaded - 0C122A1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_Grand Atk Trans (06A6680C)](#trigger-06a6680c).

Attached scope: tag definitions 0C12293C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_GrandAtk_Unloaded (0C122A1C)](#trigger-0c122a1c).
2. Clear local flag 27 (Grand Atk_Unloaded).
3. Enable and reset applicable timers for [Create_Grand Atk Trans (06A6680C)](#trigger-06a6680c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9542, Events line 9846, Actions line 10150.

<a id="trigger-0c122e5c"></a>

### 177. Clear_GrandCap_Unloaded - 0C122E5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_Grand Cap Trans (06A67A6C)](#trigger-06a67a6c).

Attached scope: tag definitions 0C122D7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_GrandCap_Unloaded (0C122E5C)](#trigger-0c122e5c).
2. Clear local flag 33 (Grand Cap_Unloaded).
3. Enable and reset applicable timers for [Create_Grand Cap Trans (06A67A6C)](#trigger-06a67a6c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9543, Events line 9847, Actions line 10151.

<a id="trigger-0be602dc"></a>

### 178. Clear_NTimeAtk_Unloaded - 0BE602DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_NTime Atk Trans (06A674AC)](#trigger-06a674ac).

Attached scope: tag definitions 0BE611CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_NTimeAtk_Unloaded (0BE602DC)](#trigger-0be602dc).
2. Clear local flag 31 (NTime Atk_Unloaded).
3. Enable and reset applicable timers for [Create_NTime Atk Trans (06A674AC)](#trigger-06a674ac).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9544, Events line 9848, Actions line 10152.

<a id="trigger-0c123f3c"></a>

### 179. Clear_NTimeCap_Unloaded - 0C123F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_NTime Cap Trans (06A6710C)](#trigger-06a6710c).

Attached scope: tag definitions 0C123E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_NTimeCap_Unloaded (0C123F3C)](#trigger-0c123f3c).
2. Clear local flag 37 (NTime Cap_Unloaded).
3. Enable and reset applicable timers for [Create_NTime Cap Trans (06A6710C)](#trigger-06a6710c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9545, Events line 9849, Actions line 10153.

<a id="trigger-0c1237fc"></a>

### 180. Clear_ParkAtk_Unloaded - 0C1237FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_Park Atk Trans (06A66BAC)](#trigger-06a66bac).

Attached scope: tag definitions 0C12371C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_ParkAtk_Unloaded (0C1237FC)](#trigger-0c1237fc).
2. Clear local flag 29 (Park Atk_Unloaded).
3. Enable and reset applicable timers for [Create_Park Atk Trans (06A66BAC)](#trigger-06a66bac).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9546, Events line 9850, Actions line 10154.

<a id="trigger-0c1239cc"></a>

### 181. Clear_ParkCap_Unloaded - 0C1239CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_Park Cap Trans (06A660CC)](#trigger-06a660cc).

Attached scope: tag definitions 0C1238EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_ParkCap_Unloaded (0C1239CC)](#trigger-0c1239cc).
2. Clear local flag 35 (Park Cap_Unloaded).
3. Enable and reset applicable timers for [Create_Park Cap Trans (06A660CC)](#trigger-06a660cc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9547, Events line 9851, Actions line 10155.

<a id="trigger-0c12345c"></a>

### 182. Clear_StatueAtk_Unloade - 0C12345C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_Statue Atk Trans (06A669DC)](#trigger-06a669dc).

Attached scope: tag definitions 0C122F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_StatueAtk_Unloade (0C12345C)](#trigger-0c12345c).
2. Clear local flag 28 (Statue Atk_Unloaded).
3. Enable and reset applicable timers for [Create_Statue Atk Trans (06A669DC)](#trigger-06a669dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9548, Events line 9852, Actions line 10156.

<a id="trigger-0c12362c"></a>

### 183. Clear_StatueCap_Unloade - 0C12362C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_Statue Cap Trans (06A67E5C)](#trigger-06a67e5c).

Attached scope: tag definitions 0C12354C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_StatueCap_Unloade (0C12362C)](#trigger-0c12362c).
2. Clear local flag 34 (Statue Cap_Unloaded).
3. Enable and reset applicable timers for [Create_Statue Cap Trans (06A67E5C)](#trigger-06a67e5c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9549, Events line 9853, Actions line 10157.

<a id="trigger-0c12423c"></a>

### 184. Clear_STimeAtk_Unloaded - 0C12423C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_STime Atk Trans (06A6767C)](#trigger-06a6767c).

Attached scope: tag definitions 0C12415C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_STimeAtk_Unloaded (0C12423C)](#trigger-0c12423c).
2. Clear local flag 32 (STime Atk_Unloaded).
3. Enable and reset applicable timers for [Create_STime Atk Trans (06A6767C)](#trigger-06a6767c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9550, Events line 9854, Actions line 10158.

<a id="trigger-0c12440c"></a>

### 185. Clear_STimeCap_Unloaded - 0C12440C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_STime Cap Trans (0B44E12C)](#trigger-0b44e12c).

Attached scope: tag definitions 0C12432C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Clear_STimeCap_Unloaded (0C12440C)](#trigger-0c12440c).
2. Clear local flag 38 (STime Cap_Unloaded).
3. Enable and reset applicable timers for [Create_STime Cap Trans (0B44E12C)](#trigger-0b44e12c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9551, Events line 9855, Actions line 10159.

<a id="trigger-07837a2c"></a>

### 186. Audio_Intro Hospital - 07837A2C

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Audio_Intro Hospital (07837A2C)](#trigger-07837a2c).
2. Play voice notification Unit_Sofia_TechHospital.
3. Reveal terrain around waypoint 98 (cell 93, 100).
4. Flash buildings of type CATHOSP; duration argument 120.
5. Jump the camera to waypoint 98 (cell 93, 100).
6. Set global flag 13.
7. Play sound CameraSwitch.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9552, Events line 9856, Actions line 10160.

<a id="trigger-06b5f54c"></a>

### 187. SP3.6g_Take Mach Shop - 06B5F54C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6f_Take Hospital (06B5FB2C)](#trigger-06b5fb2c).

Attached scope: Tech Machine Shop (CAMACH), owner Americans, cell (142, 91), tag 06B5F46C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Enable and reset applicable timers for [SP3.6i_Take Depot (0C55D39C)](#trigger-0c55d39c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9553, Events line 9857, Actions line 10161.

<a id="trigger-0959cafc"></a>

### 188. Detect_Trans(Rhino)Dead - 0959CAFC

Owner reference: Soviet2 Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Dead Rhinos (082C77EC)](#trigger-082c77ec).

Attached scope: tag definitions 0959CA1C (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Reinforce_Backup Rhinos (082C44AC)](#trigger-082c44ac).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9554, Events line 9858, Actions line 10162.

<a id="trigger-0959c92c"></a>

### 189. Detect_Trans (Con) Dead - 0959C92C

Owner reference: Soviet2 Country. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Dead Conscripts (082C79BC)](#trigger-082c79bc).

Attached scope: tag definitions 0959C84C (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Reinforce_Backup Cons (082C467C)](#trigger-082c467c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9555, Events line 9859, Actions line 10163.

<a id="trigger-0bdc985c"></a>

### 190. SP4.3_Camera_Jump to BQ - 0BDC985C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.2_Audio_Time Ready (0BDE064C)](#trigger-0bde064c).

Attached scope: tag definitions 0BDC977C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable player input.
2. Jump the camera to waypoint 68 (cell 182, 138).
3. Play sound CameraSwitch.
4. Enable and reset applicable timers for [SP4.4_Enable_TimeEffect (0BDCDD0C)](#trigger-0bdcdd0c).
5. Disable [Detect_Time 2 Destroyed (0BB91C2C)](#trigger-0bb91c2c).
6. Enable and reset applicable timers for [Give_Back2Sov2 (0CAAF7DC)](#trigger-0caaf7dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9556, Events line 9860, Actions line 10164.

<a id="trigger-0439e3fc"></a>

### 191. SP4.2a_Detect_BorisDead - 0439E3FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.2_Audio_Time Ready (0BDE064C)](#trigger-0bde064c).

Attached scope: tag definitions 0439E31C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 24 (BorisDead) is set.

Flag writers in this mission: set local flag 24 (BorisDead) at [Detect_Boris Dead (06B627BC)](#trigger-06b627bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP4.2b_Audio_ZofREBor (0439E05C)](#trigger-0439e05c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9557, Events line 9861, Actions line 10165.

<a id="trigger-097651dc"></a>

### 192. SP4.2c_Detect_BorisLive - 097651DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.2_Audio_Time Ready (0BDE064C)](#trigger-0bde064c).

Attached scope: tag definitions 097650FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 24 (BorisDead) is clear.

Flag writers in this mission: set local flag 24 (BorisDead) at [Detect_Boris Dead (06B627BC)](#trigger-06b627bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy Tag; main setting 0439F23C.
2. Destroy Tag; main setting 0439FF4C.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9558, Events line 9862, Actions line 10166.

<a id="trigger-06b8fb9c"></a>

### 193. Detect_3 PP Gone True - 06B8FB9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_2 PP Gone False (06B8FD6C)](#trigger-06b8fd6c).

Attached scope: tag definitions 06B91E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 42 (3 PP Gone) is clear.

Flag writers in this mission: set local flag 42 (3 PP Gone) at [Detect_3 PP Gone True (06B8FB9C)](#trigger-06b8fb9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Detect_3 PP Gone True (06B8FB9C)](#trigger-06b8fb9c).
2. Set local flag 42 (3 PP Gone).
3. Enable and reset applicable timers for [Detect_3 PP Gone False (06B8F9CC)](#trigger-06b8f9cc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9559, Events line 9863, Actions line 10167.

<a id="trigger-0c55d39c"></a>

### 194. SP3.6i_Take Depot - 0C55D39C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP3.6g_Take Mach Shop (06B5F54C)](#trigger-06b5f54c).

Attached scope: Allied Repair Depot (GADEPT), owner Americans, cell (137, 96), tag 0C55D2BC, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9560, Events line 9864, Actions line 10168.

<a id="trigger-0bdcdd0c"></a>

### 195. SP4.4_Enable_TimeEffect - 0BDCDD0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.3_Camera_Jump to BQ (0BDC985C)](#trigger-0bdc985c).

Attached scope: tag definitions 0BDCDA5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change_Power 2 Allies (0C46AB3C)](#trigger-0c46ab3c).
2. Enable and reset applicable timers for [Animation_Time Effect (0951A8BC)](#trigger-0951a8bc).
3. Enable and reset applicable timers for [SP4.4a_Open Local (0937049C)](#trigger-0937049c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9561, Events line 9865, Actions line 10169.

<a id="trigger-0bb91c2c"></a>

### 196. Detect_Time 2 Destroyed - 0BB91C2C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [SP3.4_TimeMachine II (0952C96C)](#trigger-0952c96c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Detect_Time 2 Destroyed (0BB91C2C)](#trigger-0bb91c2c).
2. Enable and reset applicable timers for [_End_Lose (06B602BC)](#trigger-06b602bc).
3. Play voice notification Mis_xS1_ZofiaLostTimeMach.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9562, Events line 9866, Actions line 10170.

<a id="trigger-0caaf7dc"></a>

### 197. Give_Back2Sov2 - 0CAAF7DC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Time 2 Destroyed (0BB91C2C)](#trigger-0bb91c2c).

Incoming activation links: enable from [SP4.3_Camera_Jump to BQ (0BDC985C)](#trigger-0bdc985c).

Attached scope: Time Machine (CATIME02), owner Soviet2House, cell (185, 137), tag 0BB91B4C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Give_Back2Sov2 (0CAAF7DC)](#trigger-0caaf7dc).
2. Change House: owner selector 15 (country/type SOVIET2 COUNTRY; placed owner Soviet2House).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9563, Events line 9867, Actions line 10171.

<a id="trigger-0439e05c"></a>

### 198. SP4.2b_Audio_ZofREBor - 0439E05C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.2a_Detect_BorisDead (0439E3FC)](#trigger-0439e3fc).

Attached scope: tag definitions 0439FF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaFindBoris.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9564, Events line 9868, Actions line 10172.

<a id="trigger-06b8f9cc"></a>

### 199. Detect_3 PP Gone False - 06B8F9CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_3 PP Gone True (06B8FB9C)](#trigger-06b8fb9c).

Attached scope: tag definitions 06B91C8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 42 (3 PP Gone) is set.

Flag writers in this mission: set local flag 42 (3 PP Gone) at [Detect_3 PP Gone True (06B8FB9C)](#trigger-06b8fb9c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Detect_3 PP Gone False (06B8F9CC)](#trigger-06b8f9cc).
2. Enable and reset applicable timers for [Detect_< 4 Power (06B6156C)](#trigger-06b6156c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9565, Events line 9869, Actions line 10173.

<a id="trigger-0937049c"></a>

### 200. SP4.4a_Open Local - 0937049C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.4_Enable_TimeEffect (0BDCDD0C)](#trigger-0bdcdd0c).

Attached scope: tag definitions 093703BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Resize Player View; main setting 0; parameter 1: 4, parameter 2: 5, parameter 3: 52, parameter 4: 84.
2. Enable and reset applicable timers for [SP4.6_Setup_Part III (0439097C)](#trigger-0439097c).
3. Enable and reset applicable timers for [SP4.5_Move_2 San Fran (0BDCD47C)](#trigger-0bdcd47c).
4. Enable and reset applicable timers for [SP4.4aa_Reshroud Map (044286FC)](#trigger-044286fc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9566, Events line 9870, Actions line 10174.

<a id="trigger-0439097c"></a>

### 201. SP4.6_Setup_Part III - 0439097C

Owner reference: Soviet2 Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.4a_Open Local (0937049C)](#trigger-0937049c).

Attached scope: tag definitions 0439089C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Clear all smudges; main setting 0.
2. Restore Starting Buildings of: owner selector 0 (country/type AMERICANS; placed owner Americans).
3. Restore Starting Buildings of: owner selector 12 (country/type NEUTRAL; placed owner Neutral).
4. Restore Starting Buildings of: owner selector 8 (country/type RUSSIANS; placed owner Russians).
5. Create building NAHAND at waypoint 108 (cell 91, 111).
6. Create building NACNST at waypoint 104 (cell 85, 115).
7. Create building NAWEAP at waypoint 105 (cell 85, 110).
8. Create building NAPOWR at waypoint 106 (cell 86, 105).
9. Create building NALASR at waypoint 107 (cell 83, 106).
10. Create building NAPOWR at waypoint 109 (cell 96, 113).
11. Create building NAPOWR at waypoint 110 (cell 97, 108).
12. Create building NALASR at waypoint 111 (cell 96, 106).
13. Create building NALASR at waypoint 112 (cell 100, 109).
14. Create building NALASR at waypoint 113 (cell 100, 112).
15. Enable and reset applicable timers for [SP4.6a_Setup Part III (06B2A4DC)](#trigger-06b2a4dc).
16. Create building NAREFN at waypoint 141 (cell 78, 116).
17. Create building NAYARD at waypoint 492 (cell 63, 109).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9567, Events line 9871, Actions line 10175.

<a id="trigger-0bdcd47c"></a>

### 202. SP4.5_Move_2 San Fran - 0BDCD47C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.4a_Open Local (0937049C)](#trigger-0937049c).

Attached scope: tag definitions 0BDCD39C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Teleport the trigger owner's supported objects toward waypoint 71 (cell 141, 100).
2. Enable and reset applicable timers for [SP4.7_Movie_ZofSanFra (095F1B8C)](#trigger-095f1b8c).
3. Jump the camera to waypoint 71 (cell 141, 100).
4. Enable and reset applicable timers for [SP4.5a_US/Sov Friends (07F2978C)](#trigger-07f2978c).
5. Enable and reset applicable timers for [SP4.5b_Close Local (0937687C)](#trigger-0937687c).
6. Reshroud Map; main setting 0.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9568, Events line 9872, Actions line 10176.

<a id="trigger-044286fc"></a>

### 203. SP4.4aa_Reshroud Map - 044286FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.4a_Open Local (0937049C)](#trigger-0937049c).

Attached scope: tag definitions 09144B3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reshroud Map; main setting 0.
2. Enable and reset applicable timers for [SP4.4b_Reveal Allied (0885994C)](#trigger-0885994c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9569, Events line 9873, Actions line 10177.

<a id="trigger-06b2a4dc"></a>

### 204. SP4.6a_Setup Part III - 06B2A4DC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.6_Setup_Part III (0439097C)](#trigger-0439097c).

Attached scope: tag definitions 06B2A3FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_Lasher Guard East (095A903C)](sov01umd-teams.md#team-095a903c).
2. Supply reinforcement team [TM_Yuri_Lasher Guard Mid (095A916C)](sov01umd-teams.md#team-095a916c).
3. Supply reinforcement team [TM_Yuri_Lasher Guard West (095A970C)](sov01umd-teams.md#team-095a970c).
4. Supply reinforcement team [TM_Yuri_Lasher Patrol East (095B5EFC)](sov01umd-teams.md#team-095b5efc).
5. Supply reinforcement team [TM_Yuri_Lasher Patrol Mid (095A805C)](sov01umd-teams.md#team-095a805c).
6. Supply reinforcement team [TM_Yuri_Lasher Patrol West (095A83FC)](sov01umd-teams.md#team-095a83fc).
7. Enable and reset applicable timers for [SP4.6b_Setup Part III (0B63FB2C)](#trigger-0b63fb2c).
8. Supply reinforcement team [TM_Yuri_5 Initiate Island Guard (0930D91C)](sov01umd-teams.md#team-0930d91c).
9. Supply reinforcement team [TM_Yuri_1 Engineer 4 Reactor (0442B86C)](sov01umd-teams.md#team-0442b86c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9570, Events line 9874, Actions line 10178.

<a id="trigger-095f1b8c"></a>

### 205. SP4.7_Movie_ZofSanFra - 095F1B8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.5_Move_2 San Fran (0BDCD47C)](#trigger-0bdcd47c).

Attached scope: tag definitions 095F1AAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 36.
2. Enable and reset applicable timers for [SP4.8_Audio_ZofiaRETime (090435FC)](#trigger-090435fc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9571, Events line 9875, Actions line 10179.

<a id="trigger-07f2978c"></a>

### 206. SP4.5a_US/Sov Friends - 07F2978C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.5_Move_2 San Fran (0BDCD47C)](#trigger-0bdcd47c).

Attached scope: tag definitions 07F296AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 14 (country/type POWERHOUSE COUNTRY; placed owner PowerHouse).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9572, Events line 9876, Actions line 10180.

<a id="trigger-0937687c"></a>

### 207. SP4.5b_Close Local - 0937687C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.5_Move_2 San Fran (0BDCD47C)](#trigger-0bdcd47c).

Attached scope: tag definitions 0937058C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Resize Player View; main setting 0; parameter 1: 4, parameter 2: 11, parameter 3: 53, parameter 4: 78.
2. Reshroud Map At; main setting 474; location/duration field RG.
3. Reshroud Map At; main setting 83; location/duration field CF.
4. Reshroud Map At; main setting 84; location/duration field CG.
5. Reshroud Map At; main setting 85; location/duration field CH.
6. Reshroud Map At; main setting 490; location/duration field RW.
7. Reshroud Map At; main setting 136; location/duration field EG.
8. Reshroud Map At; main setting 58; location/duration field BG.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9573, Events line 9877, Actions line 10181.

<a id="trigger-0885994c"></a>

### 208. SP4.4b_Reveal Allied - 0885994C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.4aa_Reshroud Map (044286FC)](#trigger-044286fc).

Attached scope: tag definitions 0885986C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 63 (cell 139, 95).
2. Reveal terrain around waypoint 66 (cell 147, 98).
3. Reveal terrain around waypoint 71 (cell 141, 100).
4. Reveal terrain around waypoint 99 (cell 131, 82).
5. Reveal terrain around waypoint 100 (cell 132, 89).
6. Reveal terrain around waypoint 114 (cell 130, 101).
7. Reveal terrain around waypoint 437 (cell 137, 110).
8. Reveal terrain around waypoint 647 (cell 140, 89).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9574, Events line 9878, Actions line 10182.

<a id="trigger-0b63fb2c"></a>

### 209. SP4.6b_Setup Part III - 0B63FB2C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.6a_Setup Part III (06B2A4DC)](#trigger-06b2a4dc).

Attached scope: tag definitions 0B63FA4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create building YAGGUN at waypoint 74 (cell 75, 93).
2. Create building YAGGUN at waypoint 75 (cell 89, 84).
3. Create building YAGGUN at waypoint 76 (cell 100, 71).
4. Enable and reset applicable timers for [SP4.6c_Setup Part III (0B63F5EC)](#trigger-0b63f5ec).
5. Enable and reset applicable timers for [SP4.6d_Place Civilians (0905A37C)](#trigger-0905a37c).
6. Enable and reset applicable timers for [SP4.6e_Place Civilians (0905A54C)](#trigger-0905a54c).
7. Enable and reset applicable timers for [SP4.6f_Place Civilians (0905A89C)](#trigger-0905a89c).
8. Enable and reset applicable timers for [SP4.6g_Place Civilians (0905B51C)](#trigger-0905b51c).
9. Enable and reset applicable timers for [SP4.6h_Place GIs @ Base (090D21BC)](#trigger-090d21bc).
10. Supply reinforcement team [TM_Sov2_1 Transport (05DC684C)](sov01umd-teams.md#team-05dc684c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9575, Events line 9879, Actions line 10183.

<a id="trigger-090435fc"></a>

### 210. SP4.8_Audio_ZofiaRETime - 090435FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.7_Movie_ZofSanFra (095F1B8C)](#trigger-095f1b8c).

Attached scope: tag definitions 0904351C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification S01_p03.
2. Enable and reset applicable timers for [SP4.8a_Unlock Input (09040ADC)](#trigger-09040adc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9576, Events line 9880, Actions line 10184.

<a id="trigger-0b63f5ec"></a>

### 211. SP4.6c_Setup Part III - 0B63F5EC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.6b_Setup Part III (0B63FB2C)](#trigger-0b63fb2c).

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (42, 64), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (37, 59), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (51, 63), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (47, 77), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (43, 60), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (43, 79), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (35, 63), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (40, 58), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (51, 60), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (53, 74), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (50, 69), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (39, 79), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (50, 76), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (35, 76), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (33, 70), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (45, 75), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (42, 72), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (38, 68), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (42, 68), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (38, 72), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (47, 69), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (47, 66), tag 0B63F50C, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (37, 76), tag 0B63F50C, persistence mode 0; Nuclear Reactor (NANRCT), owner YuriCountry, cell (20, 44), tag 0B63F50C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Supply reinforcement team [TM_Neutral_1 Cable Car (0A9680AC)](sov01umd-teams.md#team-0a9680ac).
3. Create building CAMSC03 at waypoint 56 (cell 79, 74).
4. Create building CAMSC04 at waypoint 83 (cell 85, 73).
5. Create building CAMSC05 at waypoint 84 (cell 83, 74).
6. Create building CAMSC04 at waypoint 85 (cell 80, 74).
7. Create building CAMSC02 at waypoint 86 (cell 79, 76).
8. Create building CAMSC03 at waypoint 87 (cell 75, 79).
9. Create building CAMSC05 at waypoint 88 (cell 75, 78).
10. Create building CAMSC04 at waypoint 89 (cell 71, 81).
11. Restore Starting Buildings of: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9577, Events line 9881, Actions line 10185.

<a id="trigger-0905a37c"></a>

### 212. SP4.6d_Place Civilians - 0905A37C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.6b_Setup Part III (0B63FB2C)](#trigger-0b63fb2c).

Attached scope: tag definitions 0905A29C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Neutral_1 Beach Fat Male (07809D4C)](sov01umd-teams.md#team-07809d4c) at waypoint 490 (cell 81, 78).
2. Supply reinforcement team [TM_Neutral_1 Beach Female (0871030C)](sov01umd-teams.md#team-0871030c) at waypoint 58 (cell 80, 82).
3. Supply reinforcement team [TM_Neutral_1 Beach Female (0871030C)](sov01umd-teams.md#team-0871030c) at waypoint 84 (cell 83, 74).
4. Supply reinforcement team [TM_Neutral_1 Beach Thin Male (087101DC)](sov01umd-teams.md#team-087101dc) at waypoint 77 (cell 73, 88).
5. Supply reinforcement team [TM_Neutral_1 Civ3 (087136EC)](sov01umd-teams.md#team-087136ec) at waypoint 438 (cell 79, 123).
6. Supply reinforcement team [TM_Neutral_1 Civ3 (087136EC)](sov01umd-teams.md#team-087136ec) at waypoint 132 (cell 122, 76).
7. Supply reinforcement team [TM_Neutral_1 Civ3 (087136EC)](sov01umd-teams.md#team-087136ec) at waypoint 424 (cell 110, 110).
8. Supply reinforcement team [TM_Neutral_1 Snow Fat Male (087135BC)](sov01umd-teams.md#team-087135bc) at waypoint 141 (cell 78, 116).
9. Supply reinforcement team [TM_Neutral_1 Snow Fat Male (087135BC)](sov01umd-teams.md#team-087135bc) at waypoint 458 (cell 95, 81).
10. Supply reinforcement team [TM_Neutral_1 Snow Fat Male (087135BC)](sov01umd-teams.md#team-087135bc) at waypoint 425 (cell 114, 110).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9578, Events line 9882, Actions line 10186.

<a id="trigger-0905a54c"></a>

### 213. SP4.6e_Place Civilians - 0905A54C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.6b_Setup Part III (0B63FB2C)](#trigger-0b63fb2c).

Attached scope: tag definitions 0905A46C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 74 (cell 75, 93).
2. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 128 (cell 73, 120).
3. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 451 (cell 107, 118).
4. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 75 (cell 89, 84).
5. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 457 (cell 98, 76).
6. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 456 (cell 98, 65).
7. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 463 (cell 106, 69).
8. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 431 (cell 122, 85).
9. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 427 (cell 127, 118).
10. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 130 (cell 108, 107).
11. Supply reinforcement team [TM_Neutral_1 Civ1 (087100AC)](sov01umd-teams.md#team-087100ac) at waypoint 450 (cell 107, 112).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9579, Events line 9883, Actions line 10187.

<a id="trigger-0905a89c"></a>

### 214. SP4.6f_Place Civilians - 0905A89C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.6b_Setup Part III (0B63FB2C)](#trigger-0b63fb2c).

Attached scope: tag definitions 0905A63C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Neutral_1 Civ2 (0871381C)](sov01umd-teams.md#team-0871381c) at waypoint 417 (cell 80, 109).
2. Supply reinforcement team [TM_Neutral_1 Civ2 (0871381C)](sov01umd-teams.md#team-0871381c) at waypoint 421 (cell 83, 129).
3. Supply reinforcement team [TM_Neutral_1 Civ2 (0871381C)](sov01umd-teams.md#team-0871381c) at waypoint 459 (cell 98, 99).
4. Supply reinforcement team [TM_Neutral_1 Civ2 (0871381C)](sov01umd-teams.md#team-0871381c) at waypoint 135 (cell 87, 91).
5. Supply reinforcement team [TM_Neutral_1 Civ2 (0871381C)](sov01umd-teams.md#team-0871381c) at waypoint 136 (cell 91, 79).
6. Supply reinforcement team [TM_Neutral_1 Civ2 (0871381C)](sov01umd-teams.md#team-0871381c) at waypoint 125 (cell 126, 116).
7. Supply reinforcement team [TM_Neutral_1 Civ2 (0871381C)](sov01umd-teams.md#team-0871381c) at waypoint 454 (cell 107, 84).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9580, Events line 9884, Actions line 10188.

<a id="trigger-0905b51c"></a>

### 215. SP4.6g_Place Civilians - 0905B51C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.6b_Setup Part III (0B63FB2C)](#trigger-0b63fb2c).

Attached scope: tag definitions 0905B43C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Neutral_1 Snow Female (0871591C)](sov01umd-teams.md#team-0871591c) at waypoint 123 (cell 92, 119).
2. Supply reinforcement team [TM_Neutral_1 Snow Female (0871591C)](sov01umd-teams.md#team-0871591c) at waypoint 76 (cell 100, 71).
3. Supply reinforcement team [TM_Neutral_1 Snow Female (0871591C)](sov01umd-teams.md#team-0871591c) at waypoint 442 (cell 108, 88).
4. Supply reinforcement team [TM_Neutral_1 Snow Female (0871591C)](sov01umd-teams.md#team-0871591c) at waypoint 124 (cell 112, 111).
5. Supply reinforcement team [TM_Neutral_1 Snow Thin Male (087157EC)](sov01umd-teams.md#team-087157ec) at waypoint 452 (cell 105, 118).
6. Supply reinforcement team [TM_Neutral_1 Snow Thin Male (087157EC)](sov01umd-teams.md#team-087157ec) at waypoint 134 (cell 86, 92).
7. Supply reinforcement team [TM_Neutral_1 Snow Thin Male (087157EC)](sov01umd-teams.md#team-087157ec) at waypoint 464 (cell 105, 76).
8. Supply reinforcement team [TM_Neutral_1 Snow Thin Male (087157EC)](sov01umd-teams.md#team-087157ec) at waypoint 455 (cell 107, 99).
9. Supply reinforcement team [TM_Neutral_1 Cruise Ship (05C1DC5C)](sov01umd-teams.md#team-05c1dc5c) at waypoint 474 (cell 88, 68).
10. Supply reinforcement team [TM_Neutral_1 Cruise Ship (05C1DC5C)](sov01umd-teams.md#team-05c1dc5c) at waypoint 486 (cell 88, 56).
11. Supply reinforcement team [TM_Neutral_1 Tug Boat (05C1D6BC)](sov01umd-teams.md#team-05c1d6bc) at waypoint 485 (cell 79, 60).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9581, Events line 9885, Actions line 10189.

<a id="trigger-090d21bc"></a>

### 216. SP4.6h_Place GIs @ Base - 090D21BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.6b_Setup Part III (0B63FB2C)](#trigger-0b63fb2c).

Attached scope: tag definitions 090D20DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Allies_1 GI (090C973C)](sov01umd-teams.md#team-090c973c) at waypoint 63 (cell 139, 95).
2. Supply reinforcement team [TM_Allies_1 GI (090C973C)](sov01umd-teams.md#team-090c973c) at waypoint 647 (cell 140, 89).
3. Supply reinforcement team [TM_Allies_1 GI (090C973C)](sov01umd-teams.md#team-090c973c) at waypoint 648 (cell 141, 89).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9582, Events line 9886, Actions line 10190.

<a id="trigger-09040adc"></a>

### 217. SP4.8a_Unlock Input - 09040ADC

Owner reference: PowerHouse Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.8_Audio_ZofiaRETime (090435FC)](#trigger-090435fc).

Attached scope: tag definitions 090409FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 48 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Play voice notification EVA_BattlefieldControlOnline.
3. Enable and reset applicable timers for [SP4.9_Audio_ZofiaObj4 (090437CC)](#trigger-090437cc).
4. Enable and reset applicable timers for [Audio_Sov Base Gained (0962D87C)](#trigger-0962d87c).
5. Enable and reset applicable timers for [SP4.8aa_Setup GG Bridge (07A5F24C)](#trigger-07a5f24c).
6. All change house: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9583, Events line 9887, Actions line 10191.

<a id="trigger-090437cc"></a>

### 218. SP4.9_Audio_ZofiaObj4 - 090437CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.8a_Unlock Input (09040ADC)](#trigger-09040adc).

Attached scope: tag definitions 090436EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaSovietBase.
2. Enable and reset applicable timers for [SP4.10_Text_Objective 4 (044163EC)](#trigger-044163ec).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9584, Events line 9888, Actions line 10192.

<a id="trigger-0962d87c"></a>

### 219. Audio_Sov Base Gained - 0962D87C

Owner reference: Soviet2 Country. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.8a_Unlock Input (09040ADC)](#trigger-09040adc).

Attached scope: 82 tagged map cells: (82, 103), (83, 103), (84, 103), (85, 103), (86, 103), (87, 103), (88, 103), (89, 103), (90, 103), (82, 104), (90, 104), (82, 105), (90, 105), (82, 106), (90, 106), (94, 106), (95, 106), (96, 106), (97, 106), (98, 106), (99, 106), (100, 106), (101, 106), (82, 107), (90, 107), (94, 107), (101, 107), (82, 108), (90, 108), (91, 108), (92, 108), (93, 108), (94, 108), (101, 108), (82, 109), (101, 109), (82, 110), (101, 110), (82, 111), (101, 111), (82, 112), (101, 112), (82, 113), (101, 113), (82, 114), (89, 114), (90, 114), (91, 114), (92, 114), (93, 114), (94, 114), (101, 114), (82, 115), (89, 115), (94, 115), (101, 115), (82, 116), (89, 116), (94, 116), (101, 116), (82, 117), (89, 117), (94, 117), (101, 117), (82, 118), (83, 118), (84, 118), (85, 118), (86, 118), (87, 118), (88, 118), (89, 118), (94, 118), (101, 118), (94, 119), (95, 119), (96, 119), (97, 119), (98, 119), (99, 119), (100, 119), (101, 119); tag 0962FB1C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaSovietCommand.
2. All change house: owner selector 8 (country/type RUSSIANS; placed owner Russians).
3. Enable and reset applicable timers for [SP5.1_Detect_BorisDead (0439F31C)](#trigger-0439f31c).
4. Resize Player View; main setting 0; parameter 1: 4, parameter 2: 11, parameter 3: 53, parameter 4: 78.
5. Disable [Text_Objective 4a (043E7B3C)](#trigger-043e7b3c).
6. Reveal terrain around waypoint 492 (cell 63, 109).
7. Supply reinforcement team [TM_Sov_1 War Miner (09376A2C)](sov01umd-teams.md#team-09376a2c).
8. Enable and reset applicable timers for [Create_Mixed Yuri Team (0442182C)](#trigger-0442182c).
9. Enable and reset applicable timers for [Text_Objective Complete (07EF43CC)](#trigger-07ef43cc).
10. Enable and reset applicable timers for [SP5.1a_Detect_BorisLive (0443FBCC)](#trigger-0443fbcc).
11. Enable and reset applicable timers for [_Lose_Condition (05CAF0BC)](#trigger-05caf0bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9585, Events line 9889, Actions line 10193.

<a id="trigger-07a5f24c"></a>

### 220. SP4.8aa_Setup GG Bridge - 07A5F24C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.8a_Unlock Input (09040ADC)](#trigger-09040adc).

Attached scope: tag definitions 07A5F16C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Part 2_Damage GG01 (0441445C)](#trigger-0441445c).
2. Enable and reset applicable timers for [Part 2_Damage GG03 (0441427C)](#trigger-0441427c).
3. Enable and reset applicable timers for [Part 2_Destroy GG02 (0441436C)](#trigger-0441436c).
4. Enable and reset applicable timers for [Part 2_Detect GG03 (0441418C)](#trigger-0441418c).
5. Enable and reset applicable timers for [Part 2_Detect GG04 (0441409C)](#trigger-0441409c).
6. Enable and reset applicable timers for [Part 2_Detect GG05 (04415F3C)](#trigger-04415f3c).
7. Enable and reset applicable timers for [Part 2_Detect GG06 (04415E4C)](#trigger-04415e4c).
8. Enable and reset applicable timers for [Part 2_Detect GG07 (04415D5C)](#trigger-04415d5c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9586, Events line 9890, Actions line 10194.

<a id="trigger-044163ec"></a>

### 221. SP4.10_Text_Objective 4 - 044163EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.9_Audio_ZofiaObj4 (090437CC)](#trigger-090437cc).

Attached scope: tag definitions 0441630C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 4: Take Control of Soviet Base and use it to Destroy the Psychic Dominator.” (MISSION:Sov1Obj4).
2. Enable and reset applicable timers for [Text_Objective 4a (043E7B3C)](#trigger-043e7b3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9587, Events line 9891, Actions line 10195.

<a id="trigger-0439f31c"></a>

### 222. SP5.1_Detect_BorisDead - 0439F31C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Sov Base Gained (0962D87C)](#trigger-0962d87c).

Attached scope: tag definitions 0439F23C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 24 (BorisDead) is set.

Flag writers in this mission: set local flag 24 (BorisDead) at [Detect_Boris Dead (06B627BC)](#trigger-06b627bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable player input.
2. Enable and reset applicable timers for [SP5.2_Reinforce_Boris (0439F14C)](#trigger-0439f14c).
3. Enable and reset applicable timers for [SP5.3_Audio_BorisReport (0439CF3C)](#trigger-0439cf3c).
4. Enable and reset applicable timers for [SP5.1c_Obj 4b Delayed (0443F8AC)](#trigger-0443f8ac).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9588, Events line 9892, Actions line 10196.

<a id="trigger-043e7b3c"></a>

### 223. Text_Objective 4a - 043E7B3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.10_Text_Objective 4 (044163EC)](#trigger-044163ec).

Attached scope: tag definitions 043E7A5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Find the Soviet Base.” (MISSION:Sov1Obj6).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9589, Events line 9893, Actions line 10197.

<a id="trigger-0442182c"></a>

### 224. Create_Mixed Yuri Team - 0442182C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Sov Base Gained (0962D87C)](#trigger-0962d87c); enable from [Detect_Mixed Team Dead (04421A8C)](#trigger-04421a8c).

Attached scope: tag definitions 0442375C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 20 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Disable [Create_Mixed Yuri Team (0442182C)](#trigger-0442182c).
2. Supply reinforcement team [TM_Yuri_Mixed Attack Team (05D6993C)](sov01umd-teams.md#team-05d6993c).
3. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).
4. Enable and reset applicable timers for [Create_Mixed Yuri Team2 (092FB88C)](#trigger-092fb88c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9590, Events line 9894, Actions line 10198.

<a id="trigger-0443fbcc"></a>

### 225. SP5.1a_Detect_BorisLive - 0443FBCC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Sov Base Gained (0962D87C)](#trigger-0962d87c).

Attached scope: tag definitions 05BE0BEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 24 (BorisDead) is clear.

Flag writers in this mission: set local flag 24 (BorisDead) at [Detect_Boris Dead (06B627BC)](#trigger-06b627bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP5.1b_Objective 4b (0443F6DC)](#trigger-0443f6dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9591, Events line 9895, Actions line 10199.

<a id="trigger-05caf0bc"></a>

### 226. _Lose_Condition - 05CAF0BC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Sov Base Gained (0962D87C)](#trigger-0962d87c).

Attached scope: tag definitions 05CAB32C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Amphibious Transport (SAPC) exist on the map, under this event's ownership scope.
2. Building does not exist: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.
3. Building does not exist: type index 61 (global list position: Soviet Shipyard (NAYARD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_End_Lose (06B602BC)](#trigger-06b602bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9592, Events line 9896, Actions line 10200.

<a id="trigger-0441445c"></a>

### 227. Part 2_Damage GG01 - 0441445C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP4.8aa_Setup GG Bridge (07A5F24C)](#trigger-07a5f24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 90; location/duration field CM.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9593, Events line 9897, Actions line 10201.

<a id="trigger-0441427c"></a>

### 228. Part 2_Damage GG03 - 0441427C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Destroy GG02 (0441436C)](#trigger-0441436c).

Incoming activation links: enable from [SP4.8aa_Setup GG Bridge (07A5F24C)](#trigger-07a5f24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 92; location/duration field CO.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9594, Events line 9898, Actions line 10202.

<a id="trigger-0441436c"></a>

### 229. Part 2_Destroy GG02 - 0441436C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Damage GG01 (0441445C)](#trigger-0441445c).

Incoming activation links: enable from [SP4.8aa_Setup GG Bridge (07A5F24C)](#trigger-07a5f24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 91; location/duration field CN.
2. Apply 100 damage at; main setting 91; location/duration field CN.
3. Apply 100 damage at; main setting 91; location/duration field CN.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9595, Events line 9899, Actions line 10203.

<a id="trigger-0441418c"></a>

### 230. Part 2_Detect GG03 - 0441418C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Damage GG03 (0441427C)](#trigger-0441427c).

Incoming activation links: enable from [SP4.8aa_Setup GG Bridge (07A5F24C)](#trigger-07a5f24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Golden Gate Bridge (CASANF11) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Part 2_Destroy GG_1 (04412A6C)](#trigger-04412a6c).
2. Enable and reset applicable timers for [Part 2_Destroy GG_2 (04418C8C)](#trigger-04418c8c).
3. Enable and reset applicable timers for [Part 2_Destroy GG_3 (07A190BC)](#trigger-07a190bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9596, Events line 9900, Actions line 10204.

<a id="trigger-0441409c"></a>

### 231. Part 2_Detect GG04 - 0441409C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Detect GG03 (0441418C)](#trigger-0441418c).

Incoming activation links: enable from [SP4.8aa_Setup GG Bridge (07A5F24C)](#trigger-07a5f24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Golden Gate Bridge (CASANF04) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Part 2_Destroy GG_1 (04412A6C)](#trigger-04412a6c).
2. Enable and reset applicable timers for [Part 2_Destroy GG_2 (04418C8C)](#trigger-04418c8c).
3. Enable and reset applicable timers for [Part 2_Destroy GG_3 (07A190BC)](#trigger-07a190bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9597, Events line 9901, Actions line 10205.

<a id="trigger-04415f3c"></a>

### 232. Part 2_Detect GG05 - 04415F3C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Detect GG04 (0441409C)](#trigger-0441409c).

Incoming activation links: enable from [SP4.8aa_Setup GG Bridge (07A5F24C)](#trigger-07a5f24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Golden Gate Bridge (CASANF12) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Part 2_Destroy GG_1 (04412A6C)](#trigger-04412a6c).
2. Enable and reset applicable timers for [Part 2_Destroy GG_2 (04418C8C)](#trigger-04418c8c).
3. Enable and reset applicable timers for [Part 2_Destroy GG_3 (07A190BC)](#trigger-07a190bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9598, Events line 9902, Actions line 10206.

<a id="trigger-04415e4c"></a>

### 233. Part 2_Detect GG06 - 04415E4C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Detect GG05 (04415F3C)](#trigger-04415f3c).

Incoming activation links: enable from [SP4.8aa_Setup GG Bridge (07A5F24C)](#trigger-07a5f24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Golden Gate Bridge (CASANF13) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Part 2_Destroy GG_1 (04412A6C)](#trigger-04412a6c).
2. Enable and reset applicable timers for [Part 2_Destroy GG_2 (04418C8C)](#trigger-04418c8c).
3. Enable and reset applicable timers for [Part 2_Destroy GG_3 (07A190BC)](#trigger-07a190bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9599, Events line 9903, Actions line 10207.

<a id="trigger-04415d5c"></a>

### 234. Part 2_Detect GG07 - 04415D5C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Detect GG06 (04415E4C)](#trigger-04415e4c).

Incoming activation links: enable from [SP4.8aa_Setup GG Bridge (07A5F24C)](#trigger-07a5f24c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. No instances of Golden Gate Bridge (CASANF14) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Part 2_Destroy GG_1 (04412A6C)](#trigger-04412a6c).
2. Enable and reset applicable timers for [Part 2_Destroy GG_2 (04418C8C)](#trigger-04418c8c).
3. Enable and reset applicable timers for [Part 2_Destroy GG_3 (07A190BC)](#trigger-07a190bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9600, Events line 9904, Actions line 10208.

<a id="trigger-0439f14c"></a>

### 235. SP5.2_Reinforce_Boris - 0439F14C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.1_Detect_BorisDead (0439F31C)](#trigger-0439f31c).

Attached scope: tag definitions 0439F06C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 72 (cell 94, 110).
2. Supply reinforcement team [TM_Sov_Boris from Barracks (093EEB5C)](sov01umd-teams.md#team-093eeb5c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9601, Events line 9905, Actions line 10209.

<a id="trigger-0439cf3c"></a>

### 236. SP5.3_Audio_BorisReport - 0439CF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.1_Detect_BorisDead (0439F31C)](#trigger-0439f31c).

Attached scope: tag definitions 0439CE5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 26 (BorisTalks) is set.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_BorisReporting.
2. Enable and reset applicable timers for [SP5.4_Audio_Zof2Bor (0439CD6C)](#trigger-0439cd6c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9602, Events line 9906, Actions line 10210.

<a id="trigger-0443f8ac"></a>

### 237. SP5.1c_Obj 4b Delayed - 0443F8AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.1_Detect_BorisDead (0439F31C)](#trigger-0439f31c).

Attached scope: tag definitions 0443F7CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 32 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP5.1b_Objective 4b (0443F6DC)](#trigger-0443f6dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9603, Events line 9907, Actions line 10211.

<a id="trigger-092fb88c"></a>

### 238. Create_Mixed Yuri Team2 - 092FB88C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create_Mixed Yuri Team (0442182C)](#trigger-0442182c).

Attached scope: tag definitions 092FB7AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 40 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Disable [Create_Mixed Yuri Team2 (092FB88C)](#trigger-092fb88c).
2. Supply reinforcement team [TM_Yuri_Mixed Attack Team 2 (05C99EFC)](sov01umd-teams.md#team-05c99efc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9604, Events line 9908, Actions line 10212.

<a id="trigger-0443f6dc"></a>

### 239. SP5.1b_Objective 4b - 0443F6DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.1a_Detect_BorisLive (0443FBCC)](#trigger-0443fbcc); enable from [SP5.1c_Obj 4b Delayed (0443F8AC)](#trigger-0443f8ac).

Attached scope: tag definitions 0443F5FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TM_Sov_1 War Miner (09376A2C)](sov01umd-teams.md#team-09376a2c).
2. Create/recruit team [TM_Sov_1 War Miner (09376A2C)](sov01umd-teams.md#team-09376a2c).
3. Enable and reset applicable timers for [Text/Ping_Obj7 Easy (07A255BC)](#trigger-07a255bc).
4. Enable and reset applicable timers for [Text/Ping_Obj7 Med (043EC4DC)](#trigger-043ec4dc).
5. Enable and reset applicable timers for [Text/Ping_Obj7 Hard (07A256AC)](#trigger-07a256ac).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9605, Events line 9909, Actions line 10213.

<a id="trigger-04412a6c"></a>

### 240. Part 2_Destroy GG_1 - 04412A6C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Detect GG07 (04415D5C)](#trigger-04415d5c).

Incoming activation links: enable from [Part 2_Detect GG03 (0441418C)](#trigger-0441418c); enable from [Part 2_Detect GG04 (0441409C)](#trigger-0441409c); enable from [Part 2_Detect GG05 (04415F3C)](#trigger-04415f3c); enable from [Part 2_Detect GG06 (04415E4C)](#trigger-04415e4c); enable from [Part 2_Detect GG07 (04415D5C)](#trigger-04415d5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 92; location/duration field CO.
2. Apply 100 damage at; main setting 92; location/duration field CO.
3. Apply 100 damage at; main setting 92; location/duration field CO.
4. Apply 100 damage at; main setting 92; location/duration field CO.
5. Apply 100 damage at; main setting 92; location/duration field CO.
6. Apply 100 damage at; main setting 92; location/duration field CO.
7. Apply 100 damage at; main setting 92; location/duration field CO.
8. Apply 100 damage at; main setting 92; location/duration field CO.
9. Apply 100 damage at; main setting 93; location/duration field CP.
10. Apply 100 damage at; main setting 93; location/duration field CP.
11. Apply 100 damage at; main setting 93; location/duration field CP.
12. Apply 100 damage at; main setting 93; location/duration field CP.
13. Apply 100 damage at; main setting 93; location/duration field CP.
14. Apply 100 damage at; main setting 93; location/duration field CP.
15. Apply 100 damage at; main setting 93; location/duration field CP.
16. Apply 100 damage at; main setting 93; location/duration field CP.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9606, Events line 9910, Actions line 10214.

<a id="trigger-04418c8c"></a>

### 241. Part 2_Destroy GG_2 - 04418C8C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Destroy GG_1 (04412A6C)](#trigger-04412a6c).

Incoming activation links: enable from [Part 2_Detect GG03 (0441418C)](#trigger-0441418c); enable from [Part 2_Detect GG04 (0441409C)](#trigger-0441409c); enable from [Part 2_Detect GG05 (04415F3C)](#trigger-04415f3c); enable from [Part 2_Detect GG06 (04415E4C)](#trigger-04415e4c); enable from [Part 2_Detect GG07 (04415D5C)](#trigger-04415d5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 94; location/duration field CQ.
2. Apply 100 damage at; main setting 94; location/duration field CQ.
3. Apply 100 damage at; main setting 94; location/duration field CQ.
4. Apply 100 damage at; main setting 94; location/duration field CQ.
5. Apply 100 damage at; main setting 94; location/duration field CQ.
6. Apply 100 damage at; main setting 94; location/duration field CQ.
7. Apply 100 damage at; main setting 94; location/duration field CQ.
8. Apply 100 damage at; main setting 94; location/duration field CQ.
9. Apply 100 damage at; main setting 95; location/duration field CR.
10. Apply 100 damage at; main setting 95; location/duration field CR.
11. Apply 100 damage at; main setting 95; location/duration field CR.
12. Apply 100 damage at; main setting 95; location/duration field CR.
13. Apply 100 damage at; main setting 95; location/duration field CR.
14. Apply 100 damage at; main setting 95; location/duration field CR.
15. Apply 100 damage at; main setting 95; location/duration field CR.
16. Apply 100 damage at; main setting 95; location/duration field CR.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9607, Events line 9911, Actions line 10215.

<a id="trigger-07a190bc"></a>

### 242. Part 2_Destroy GG_3 - 07A190BC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Part 2_Destroy GG_2 (04418C8C)](#trigger-04418c8c).

Incoming activation links: enable from [Part 2_Detect GG03 (0441418C)](#trigger-0441418c); enable from [Part 2_Detect GG04 (0441409C)](#trigger-0441409c); enable from [Part 2_Detect GG05 (04415F3C)](#trigger-04415f3c); enable from [Part 2_Detect GG06 (04415E4C)](#trigger-04415e4c); enable from [Part 2_Detect GG07 (04415D5C)](#trigger-04415d5c).

Attached scope: tag definitions 0441490C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 96; location/duration field CS.
2. Apply 100 damage at; main setting 96; location/duration field CS.
3. Apply 100 damage at; main setting 96; location/duration field CS.
4. Apply 100 damage at; main setting 96; location/duration field CS.
5. Apply 100 damage at; main setting 96; location/duration field CS.
6. Apply 100 damage at; main setting 96; location/duration field CS.
7. Apply 100 damage at; main setting 96; location/duration field CS.
8. Apply 100 damage at; main setting 96; location/duration field CS.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9608, Events line 9912, Actions line 10216.

<a id="trigger-0439cd6c"></a>

### 243. SP5.4_Audio_Zof2Bor - 0439CD6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.3_Audio_BorisReport (0439CF3C)](#trigger-0439cf3c).

Attached scope: tag definitions 0439C9FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaBorisInPast.
2. Enable and reset applicable timers for [SP5.5_Audio_Bor2Zof (0439C90C)](#trigger-0439c90c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9609, Events line 9913, Actions line 10217.

<a id="trigger-07a255bc"></a>

### 244. Text/Ping_Obj7 Easy - 07A255BC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Text/Ping_Obj7 Hard (07A256AC)](#trigger-07a256ac).

Incoming activation links: enable from [SP5.1b_Objective 4b (0443F6DC)](#trigger-0443f6dc).

Attached scope: tag definitions 043EBBCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Destroy the Psychic Dominator.” (MISSION:Sov1Obj7).
2. Create radar-event marker type 12 at waypoint 144 (cell 40, 70).
3. Move the camera to waypoint 144 (cell 40, 70) with speed setting 3.
4. Flash buildings of type YAPPPT; duration argument 150.
5. Reveal terrain around waypoint 144 (cell 40, 70).
6. Reveal terrain around waypoint 699 (cell 41, 80).
7. Reveal terrain around waypoint 145 (cell 40, 65).
8. Reveal terrain around waypoint 143 (cell 45, 65).
9. Reveal terrain around waypoint 54 (cell 39, 72).
10. Reveal terrain around waypoint 475 (cell 51, 55).
11. Reveal terrain around waypoint 479 (cell 54, 68).
12. Enable and reset applicable timers for [Text_Objective 4b (043E7D0C)](#trigger-043e7d0c).
13. Enable and reset applicable timers for [SP5.1d_Hint_Amphib (097DB5BC)](#trigger-097db5bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9610, Events line 9914, Actions line 10218.

<a id="trigger-043ec4dc"></a>

### 245. Text/Ping_Obj7 Med - 043EC4DC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.1b_Objective 4b (0443F6DC)](#trigger-0443f6dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Destroy the Psychic Dominator.” (MISSION:Sov1Obj7).
2. Create radar-event marker type 12 at waypoint 144 (cell 40, 70).
3. Enable and reset applicable timers for [Text_Objective 4b (043E7D0C)](#trigger-043e7d0c).
4. Enable and reset applicable timers for [SP5.1d_Hint_Amphib (097DB5BC)](#trigger-097db5bc).
5. Move the camera to waypoint 144 (cell 40, 70) with speed setting 3.
6. Flash buildings of type YAPPPT; duration argument 150.
7. Reveal terrain around waypoint 143 (cell 45, 65).
8. Reveal terrain around waypoint 475 (cell 51, 55).
9. Reveal terrain around waypoint 144 (cell 40, 70).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9611, Events line 9915, Actions line 10219.

<a id="trigger-07a256ac"></a>

### 246. Text/Ping_Obj7 Hard - 07A256AC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Text/Ping_Obj7 Med (043EC4DC)](#trigger-043ec4dc).

Incoming activation links: enable from [SP5.1b_Objective 4b (0443F6DC)](#trigger-0443f6dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Destroy the Psychic Dominator.” (MISSION:Sov1Obj7).
2. Create radar-event marker type 12 at waypoint 144 (cell 40, 70).
3. Move the camera to waypoint 144 (cell 40, 70) with speed setting 3.
4. Flash buildings of type YAPPPT; duration argument 150.
5. Reveal terrain around waypoint 144 (cell 40, 70).
6. Enable and reset applicable timers for [Text_Objective 4b (043E7D0C)](#trigger-043e7d0c).
7. Enable and reset applicable timers for [SP5.1d_Hint_Amphib (097DB5BC)](#trigger-097db5bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9612, Events line 9916, Actions line 10220.

<a id="trigger-0439c90c"></a>

### 247. SP5.5_Audio_Bor2Zof - 0439C90C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.4_Audio_Zof2Bor (0439CD6C)](#trigger-0439cd6c).

Attached scope: tag definitions 0439C82C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_BorisPuzzled.
2. Enable and reset applicable timers for [SP5.6_Audio_Zof2Bor (0439C73C)](#trigger-0439c73c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9613, Events line 9917, Actions line 10221.

<a id="trigger-097db5bc"></a>

### 248. SP5.1d_Hint_Amphib - 097DB5BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Text/Ping_Obj7 Easy (07A255BC)](#trigger-07a255bc); enable from [Text/Ping_Obj7 Med (043EC4DC)](#trigger-043ec4dc); enable from [Text/Ping_Obj7 Hard (07A256AC)](#trigger-07a256ac).

Attached scope: tag definitions 097DFF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Hint: Build Amphibious Transports” (MISSION:TranHint).
2. Switch the sidebar to tab 3.
3. Flash cameo/type SAPC; additional configured duration/location argument 100.
4. Play voice notification Mis_xS1_BorisWantsBoat.
5. Enable and reset applicable timers for [SP5.1e_Camera Back2Sov (091696FC)](#trigger-091696fc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9614, Events line 9918, Actions line 10222.

<a id="trigger-0439c73c"></a>

### 249. SP5.6_Audio_Zof2Bor - 0439C73C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.5_Audio_Bor2Zof (0439C90C)](#trigger-0439c90c).

Attached scope: tag definitions 0439C65C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaRespondsToBoris.
2. Enable and reset applicable timers for [SP5.7_End Setpiece (0439C2DC)](#trigger-0439c2dc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9615, Events line 9919, Actions line 10223.

<a id="trigger-091696fc"></a>

### 250. SP5.1e_Camera Back2Sov - 091696FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.1d_Hint_Amphib (097DB5BC)](#trigger-097db5bc).

Attached scope: tag definitions 0916961C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 72 (cell 94, 110).
2. Play sound CameraSwitch.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9616, Events line 9920, Actions line 10224.

<a id="trigger-0439c2dc"></a>

### 251. SP5.7_End Setpiece - 0439C2DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP5.6_Audio_Zof2Bor (0439C73C)](#trigger-0439c73c).

Attached scope: tag definitions 0439C1FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_BattlefieldControlOnline.
2. Enable player input.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9617, Events line 9921, Actions line 10225.

<a id="trigger-07ef508c"></a>

### 252. Text/Audio_Obj Complete - 07EF508C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07EF5F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Text/Audio_Obj Complete (07EF508C)](#trigger-07ef508c).
2. Play voice notification EVA_ObjectiveComplete.
3. Display message “Objective Complete” (MISSION:ObjCompleteSov04md).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9618, Events line 9922, Actions line 10226.

<a id="trigger-06b627bc"></a>

### 253. Detect_Boris Dead - 06B627BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06B6249C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaBorisDeadMourn.
2. Set local flag 24 (BorisDead).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9619, Events line 9923, Actions line 10227.

<a id="trigger-095183ec"></a>

### 254. Detect_Player Has Time - 095183EC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0951830C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 314 (global list position: Tech Secret Lab (CASLAB)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP3.1_Detect_Full Power (0BDE024C)](#trigger-0bde024c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9620, Events line 9924, Actions line 10228.

<a id="trigger-0951a4bc"></a>

### 255. Move_Player to Jurassic - 0951A4BC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0951A3DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Teleport the trigger owner's supported objects toward waypoint 68 (cell 182, 138).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9621, Events line 9925, Actions line 10229.

<a id="trigger-094d21ac"></a>

### 256. _Setup_Part I - 094D21AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 094D1F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Allies_Patrol Gas Plant (0965BB5C)](sov01umd-teams.md#team-0965bb5c).
2. Supply reinforcement team [TM_Allies_Patrol Grand Plant (088B391C)](sov01umd-teams.md#team-088b391c).
3. Supply reinforcement team [TM_Allies_Patrol Park Plant (088B348C)](sov01umd-teams.md#team-088b348c).
4. Supply reinforcement team [TM_Allies_Patrol Statue Plant (088B3DCC)](sov01umd-teams.md#team-088b3dcc).
5. Supply reinforcement team [TM_Allies_Patrol TopTime Plant (088B47FC)](sov01umd-teams.md#team-088b47fc).
6. Supply reinforcement team [TM_Allies_Patrol BottomTime Plant (088B05BC)](sov01umd-teams.md#team-088b05bc).
7. Reveal terrain around waypoint 468 (cell 19, 62).
8. Reveal terrain around waypoint 469 (cell 31, 50).
9. Reveal terrain around waypoint 470 (cell 42, 37).
10. Reveal terrain around waypoint 471 (cell 54, 25).
11. Reveal terrain around waypoint 472 (cell 63, 15).
12. Reveal terrain around waypoint 473 (cell 32, 80).
13. Reveal terrain around waypoint 474 (cell 88, 68).
14. Reveal terrain around waypoint 475 (cell 51, 55).
15. Reveal terrain around waypoint 476 (cell 62, 42).
16. Reveal terrain around waypoint 53 (cell 48, 76).
17. Reveal terrain around waypoint 699 (cell 41, 80).
18. Reveal terrain around waypoint 13 (cell 51, 95).
19. Reveal terrain around waypoint 152 (cell 54, 77).
20. Reveal terrain around waypoint 59 (cell 68, 91).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9622, Events line 9926, Actions line 10230.

<a id="trigger-095714fc"></a>

### 257. Detect_Boris Dead Again - 095714FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0957141C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play voice notification Mis_xS1_ZofiaBorisDeadAgain.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9623, Events line 9927, Actions line 10231.

<a id="trigger-09533a5c"></a>

### 258. _Setup_Part Ia - 09533A5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0953397C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 477 (cell 86, 39).
2. Reveal terrain around waypoint 478 (cell 43, 86).
3. Reveal terrain around waypoint 479 (cell 54, 68).
4. Reveal terrain around waypoint 480 (cell 62, 63).
5. Reveal terrain around waypoint 481 (cell 76, 46).
6. Reveal terrain around waypoint 482 (cell 97, 48).
7. Reveal terrain around waypoint 483 (cell 59, 91).
8. Reveal terrain around waypoint 484 (cell 66, 72).
9. Reveal terrain around waypoint 485 (cell 79, 60).
10. Reveal terrain around waypoint 486 (cell 88, 56).
11. Reveal terrain around waypoint 487 (cell 54, 105).
12. Reveal terrain around waypoint 488 (cell 73, 95).
13. Reveal terrain around waypoint 489 (cell 94, 62).
14. Reveal terrain around waypoint 490 (cell 81, 78).
15. Reveal terrain around waypoint 491 (cell 55, 82).
16. Reveal terrain around waypoint 492 (cell 63, 109).
17. Reveal terrain around waypoint 493 (cell 75, 29).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9624, Events line 9928, Actions line 10232.

<a id="trigger-0c331d8c"></a>

### 259. _Setup_Part Ib - 0C331D8C

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C331CAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 494 (cell 67, 105).
2. Reveal terrain around waypoint 495 (cell 60, 77).
3. Reveal terrain around waypoint 496 (cell 68, 55).
4. Reveal terrain around waypoint 497 (cell 66, 32).
5. Reveal terrain around waypoint 498 (cell 53, 95).
6. Reveal terrain around waypoint 499 (cell 69, 77).
7. Reveal terrain around waypoint 500 (cell 74, 68).
8. Reveal terrain around waypoint 501 (cell 59, 51).
9. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).
10. Reveal terrain around waypoint 699 (cell 41, 80).
11. Reshroud Map At; main setting 145; location/duration field EP.
12. Reveal terrain around waypoint 54 (cell 39, 72).
13. Reveal terrain around waypoint 53 (cell 48, 76).
14. Reveal terrain around waypoint 51 (cell 51, 70).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9625, Events line 9929, Actions line 10233.

<a id="trigger-0954f76c"></a>

### 260. Secret_Rexy To Player - 0954F76C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Secret_Rexy To Player (0954F76C)](#trigger-0954f76c).
2. Enable and reset applicable timers for [Rexy_Helped (097DF8EC)](#trigger-097df8ec).
3. Change House: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9626, Events line 9930, Actions line 10234.

<a id="trigger-097df8ec"></a>

### 261. Rexy_Helped - 097DF8EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Secret_Rexy To Player (0954F76C)](#trigger-0954f76c).

Attached scope: tag definitions 097DF4DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound Cheer.
2. Display message “Rexy is now your friend to the end!” (MISSION:RexyFrnd).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9627, Events line 9931, Actions line 10235.

<a id="trigger-097dfabc"></a>

### 262. Rexy_Help - 097DFABC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Secret_Rexy To Player (0954F76C)](#trigger-0954f76c).

Attached scope: DNOAA, owner British, cell (127, 161), tag 06D15C5C, persistence mode 2.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Rexy_Help (097DFABC)](#trigger-097dfabc).
2. Play sound CivAllFear.
3. Play sound TrexRoar.
4. Display message “Rexy is trapped! Won't you help him?” (MISSION:RexyHelp).
5. Reveal terrain around waypoint 465 (cell 128, 160).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9628, Events line 9932, Actions line 10236.

<a id="trigger-097dde6c"></a>

### 263. Detect_Yuri Got Power - 097DDE6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Power Attacked (0951918C)](#trigger-0951918c).

Attached scope: GAPOWRA, owner Alliance, cell (78, 111), tag 0C46AA5C, persistence mode 2; GAPOWRB, owner Alliance, cell (80, 126), tag 0C46AA5C, persistence mode 2; GAPOWRC, owner Alliance, cell (91, 116), tag 0C46AA5C, persistence mode 2; GAPOWRD, owner Alliance, cell (112, 113), tag 0C46AA5C, persistence mode 2; GAPOWRE, owner Alliance, cell (128, 116), tag 0C46AA5C, persistence mode 2; GAPOWRF, owner Alliance, cell (119, 82), tag 0C46AA5C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Disable [Detect_Yuri Got Power (097DDE6C)](#trigger-097dde6c).
2. Play sound BaseUnderAttackSiren.
3. Display message “Yuri captured a Power Plant!” (MISSION:YGotPowr).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9629, Events line 9933, Actions line 10237.

<a id="trigger-0970a22c"></a>

### 264. Hint_Stop Dominator - 0970A22C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09715F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Hint: Capturing Power Plants will stop the Psychic Dominator” (MISSION:HintDom).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9630, Events line 9934, Actions line 10238.

<a id="trigger-0942bc2c"></a>

### 265. _Amb_SF_Urban Murmur 2a - 0942BC2C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0942CDCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur2 at waypoint 458 (cell 95, 81).
2. Play sound _Amb_UrbanMurmur2 at waypoint 440 (cell 106, 78).
3. Play sound _Amb_UrbanMurmur2 at waypoint 443 (cell 122, 89).
4. Play sound _Amb_UrbanMurmur2 at waypoint 442 (cell 108, 88).
5. Play sound _Amb_UrbanMurmur2 at waypoint 459 (cell 98, 99).
6. Play sound _Amb_UrbanMurmur2 at waypoint 130 (cell 108, 107).
7. Play sound _Amb_UrbanMurmur2 at waypoint 125 (cell 126, 116).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9631, Events line 9935, Actions line 10239.

<a id="trigger-0942ccdc"></a>

### 266. _Amb_SF_Birds Beach - 0942CCDC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0942CBFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsBeach at waypoint 55 (cell 78, 79).
2. Play sound _Amb_BirdsBeach at waypoint 490 (cell 81, 78).
3. Play sound _Amb_BirdsBeach at waypoint 77 (cell 73, 88).
4. Play sound _Amb_BirdsBeach at waypoint 499 (cell 69, 77).
5. Play sound _Amb_BirdsPark at waypoint 67 (cell 75, 106).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9632, Events line 9936, Actions line 10240.

<a id="trigger-0942e17c"></a>

### 267. _Amb_SF_Wind Plains 1 - 0942E17C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0942E09C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindPlains at waypoint 72 (cell 94, 110).
2. Play sound _Amb_WindPlains at waypoint 105 (cell 85, 110).
3. Play sound _Amb_WindPlains at waypoint 141 (cell 78, 116).
4. Play sound _Amb_WindPlains at waypoint 128 (cell 73, 120).
5. Play sound _Amb_WindPlains at waypoint 453 (cell 105, 136).
6. Play sound _Amb_WindPlains at waypoint 439 (cell 120, 126).
7. Play sound _Amb_WindPlains at waypoint 442 (cell 108, 88).
8. Play sound _Amb_WindPlains at waypoint 114 (cell 130, 101).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9633, Events line 9937, Actions line 10241.

<a id="trigger-094492ec"></a>

### 268. _Amb_SF_Ocean Light 1 - 094492EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043E54EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 468 (cell 19, 62).
2. Play sound _Amb_OceanLight at waypoint 469 (cell 31, 50).
3. Play sound _Amb_OceanLight at waypoint 470 (cell 42, 37).
4. Play sound _Amb_OceanLight at waypoint 471 (cell 54, 25).
5. Play sound _Amb_OceanLight at waypoint 472 (cell 63, 15).
6. Play sound _Amb_OceanLight at waypoint 473 (cell 32, 80).
7. Play sound _Amb_OceanLight at waypoint 475 (cell 51, 55).
8. Play sound _Amb_OceanLight at waypoint 476 (cell 62, 42).
9. Play sound _Amb_OceanLight at waypoint 493 (cell 75, 29).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9634, Events line 9938, Actions line 10242.

<a id="trigger-043ec6cc"></a>

### 269. _Amb_Jur_Ocean Heavy 1 - 043EC6CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043EC5EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 26 (cell 114, 160).
2. Play sound _Amb_OceanHeavy at waypoint 27 (cell 122, 152).
3. Play sound _Amb_OceanHeavy at waypoint 28 (cell 130, 143).
4. Play sound _Amb_OceanHeavy at waypoint 29 (cell 138, 134).
5. Play sound _Amb_OceanHeavy at waypoint 30 (cell 147, 125).
6. Play sound _Amb_OceanHeavy at waypoint 31 (cell 157, 111).
7. Play sound _Amb_OceanHeavy at waypoint 32 (cell 126, 172).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9635, Events line 9939, Actions line 10243.

<a id="trigger-043ec4fc"></a>

### 270. _Amb_Jur_Birds Jungl 2a - 043EC4FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043ECB3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsJungle2 at waypoint 68 (cell 182, 138).
2. Play sound _Amb_BirdsJungle2 at waypoint 502 (cell 174, 136).
3. Play sound _Amb_BirdsJungle2 at waypoint 70 (cell 165, 171).
4. Play sound _Amb_BirdsJungle2 at waypoint 503 (cell 164, 129).
5. Play sound _Amb_BirdsJungle2 at waypoint 69 (cell 166, 111).
6. Play sound _Amb_BirdsJungle2 at waypoint 465 (cell 128, 160).
7. Play sound _Amb_BirdsJungle2 at waypoint 41 (cell 166, 116).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9636, Events line 9940, Actions line 10244.

<a id="trigger-043ed65c"></a>

### 271. _Amb_SF_Ocean Light 2 - 043ED65C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043ED57C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 477 (cell 86, 39).
2. Play sound _Amb_OceanLight at waypoint 481 (cell 76, 46).
3. Play sound _Amb_OceanLight at waypoint 496 (cell 68, 55).
4. Play sound _Amb_OceanLight at waypoint 480 (cell 62, 63).
5. Play sound _Amb_OceanLight at waypoint 492 (cell 63, 109).
6. Play sound _Amb_OceanLight at waypoint 495 (cell 60, 77).
7. Play sound _Amb_OceanLight at waypoint 491 (cell 55, 82).
8. Play sound _Amb_OceanLight at waypoint 78 (cell 52, 91).
9. Play sound _Amb_OceanLight at waypoint 478 (cell 43, 86).
10. Play sound _Amb_OceanLight at waypoint 487 (cell 54, 105).
11. Play sound _Amb_OceanLight at waypoint 494 (cell 67, 105).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9637, Events line 9941, Actions line 10245.

<a id="trigger-060365bc"></a>

### 272. _Amb_SF_Birds Harbor 1 - 060365BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 060364DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsHarbor at waypoint 479 (cell 54, 68).
2. Play sound _Amb_BirdsHarbor at waypoint 53 (cell 48, 76).
3. Play sound _Amb_BirdsHarbor at waypoint 478 (cell 43, 86).
4. Play sound _Amb_BirdsHarbor at waypoint 473 (cell 32, 80).
5. Play sound _Amb_BirdsHarbor at waypoint 469 (cell 31, 50).
6. Play sound _Amb_BirdsHarbor at waypoint 475 (cell 51, 55).
7. Play sound _Amb_BirdsHarbor at waypoint 499 (cell 69, 77).
8. Play sound _Amb_BirdsHarbor at waypoint 79 (cell 63, 89).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9638, Events line 9942, Actions line 10246.

<a id="trigger-07dc3a4c"></a>

### 273. _Amb_SF_Birds Harbor 2 - 07DC3A4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07DC396C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsHarbor at waypoint 494 (cell 67, 105).
2. Play sound _Amb_BirdsHarbor at waypoint 142 (cell 65, 110).
3. Play sound _Amb_BirdsHarbor at waypoint 500 (cell 74, 68).
4. Play sound _Amb_BirdsHarbor at waypoint 474 (cell 88, 68).
5. Play sound _Amb_BirdsHarbor at waypoint 485 (cell 79, 60).
6. Play sound _Amb_BirdsHarbor at waypoint 486 (cell 88, 56).
7. Play sound _Amb_BirdsHarbor at waypoint 482 (cell 97, 48).
8. Play sound _Amb_BirdsHarbor at waypoint 489 (cell 94, 62).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9639, Events line 9943, Actions line 10247.

<a id="trigger-0612d2dc"></a>

### 274. _Amb_SF_Urban Murmur 2b - 0612D2DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0612D1FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur2 at waypoint 131 (cell 124, 110).
2. Play sound _Amb_UrbanMurmur2 at waypoint 451 (cell 107, 118).
3. Play sound _Amb_UrbanMurmur2 at waypoint 453 (cell 105, 136).
4. Play sound _Amb_UrbanMurmur2 at waypoint 448 (cell 94, 120).
5. Play sound _Amb_UrbanMurmur2 at waypoint 421 (cell 83, 129).
6. Play sound _Amb_UrbanMurmur2 at waypoint 446 (cell 78, 119).
7. Play sound _Amb_UrbanMurmur2 at waypoint 111 (cell 96, 106).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9640, Events line 9944, Actions line 10248.

<a id="trigger-0612f98c"></a>

### 275. _Amb_SF_Wind Plains 2 - 0612F98C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0612F8AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindPlains at waypoint 132 (cell 122, 76).
2. Play sound _Amb_WindPlains at waypoint 462 (cell 112, 63).
3. Play sound _Amb_WindPlains at waypoint 463 (cell 106, 69).
4. Play sound _Amb_WindPlains at waypoint 458 (cell 95, 81).
5. Play sound _Amb_WindPlains at waypoint 75 (cell 89, 84).
6. Play sound _Amb_WindPlains at waypoint 135 (cell 87, 91).
7. Play sound _Amb_WindPlains at waypoint 432 (cell 81, 100).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9641, Events line 9945, Actions line 10249.

<a id="trigger-0606fa0c"></a>

### 276. _Amb_Jur_Birds Jungl 2b - 0606FA0C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0606F92C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsJungle2 at waypoint 42 (cell 168, 126).
2. Play sound _Amb_BirdsJungle2 at waypoint 43 (cell 179, 128).
3. Play sound _Amb_BirdsJungle2 at waypoint 44 (cell 163, 135).
4. Play sound _Amb_BirdsJungle2 at waypoint 45 (cell 170, 143).
5. Play sound _Amb_BirdsJungle2 at waypoint 46 (cell 168, 152).
6. Play sound _Amb_BirdsJungle2 at waypoint 47 (cell 164, 157).
7. Play sound _Amb_BirdsJungle2 at waypoint 48 (cell 181, 149).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9642, Events line 9946, Actions line 10250.

<a id="trigger-07e30bfc"></a>

### 277. _Amb_Jur_Ocean Heavy 2 - 07E30BFC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E30B1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 33 (cell 137, 162).
2. Play sound _Amb_OceanHeavy at waypoint 34 (cell 147, 150).
3. Play sound _Amb_OceanHeavy at waypoint 35 (cell 155, 136).
4. Play sound _Amb_OceanHeavy at waypoint 36 (cell 138, 183).
5. Play sound _Amb_OceanHeavy at waypoint 37 (cell 149, 172).
6. Play sound _Amb_OceanHeavy at waypoint 38 (cell 161, 145).
7. Play sound _Amb_OceanHeavy at waypoint 39 (cell 158, 154).
8. Play sound _Amb_OceanHeavy at waypoint 40 (cell 157, 169).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9643, Events line 9947, Actions line 10251.

<a id="trigger-087d15ec"></a>

### 278. Create_1st 4 Rhinos - 087D15EC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 087D150C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 45 (1st Tanks Arrive) is set.

**Then perform these actions in order:**

1. Create/recruit team [TM_Sov_1st_4 Rhino (08E15EFC)](sov01umd-teams.md#team-08e15efc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9644, Events line 9948, Actions line 10252.

<a id="trigger-082b950c"></a>

### 279. Detect_Cons to Russia - 082B950C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 082B942C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 47 (Conscripts to Russi) is set.

Flag writers in this mission: clear local flag 47 (Conscripts to Russi) at [Detect_Cons to Russia (082B950C)](#trigger-082b950c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Sov_Re_12 Conscript (060884EC)](sov01umd-teams.md#team-060884ec).
2. Clear local flag 47 (Conscripts to Russi).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9645, Events line 9949, Actions line 10253.

<a id="trigger-082b933c"></a>

### 280. Detect_Rhino to Russia - 082B933C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 082B925C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 46 (Rhinos to Russia) is set.

Flag writers in this mission: clear local flag 46 (Rhinos to Russia) at [Detect_Rhino to Russia (082B933C)](#trigger-082b933c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [TM_Sov_RE_4 Rhino (0882794C)](sov01umd-teams.md#team-0882794c).
2. Clear local flag 46 (Rhinos to Russia).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9646, Events line 9950, Actions line 10254.

<a id="trigger-07907f3c"></a>

### 281. _Amb_Jur_Dino - 07907F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0790659C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_JurrasicTrexRoar at waypoint 41 (cell 166, 116).
2. Play sound _Amb_JurrasicTrexRoar at waypoint 42 (cell 168, 126).
3. Play sound _Amb_JurrasicTrexRoar at waypoint 46 (cell 168, 152).
4. Play sound _Amb_JurrasicTrexRoar at waypoint 47 (cell 164, 157).
5. Play sound _Amb_JurrasicTrexRoar at waypoint 69 (cell 166, 111).
6. Play sound _Amb_JurrasicTrexRoar at waypoint 70 (cell 165, 171).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9647, Events line 9951, Actions line 10255.

<a id="trigger-05cb7d1c"></a>

### 282. _Amb_Jur_Howl - 05CB7D1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05CBF0DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_JurrasicHowls at waypoint 43 (cell 179, 128).
2. Play sound _Amb_JurrasicHowls at waypoint 45 (cell 170, 143).
3. Play sound _Amb_JurrasicHowls at waypoint 48 (cell 181, 149).
4. Play sound _Amb_JurrasicHowls at waypoint 502 (cell 174, 136).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9648, Events line 9952, Actions line 10256.

<a id="trigger-05ccf03c"></a>

### 283. _Amb_Jur_Bed - 05CCF03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05CD704C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_JurrasicBed at waypoint 41 (cell 166, 116).
2. Play sound _Amb_JurrasicBed at waypoint 43 (cell 179, 128).
3. Play sound _Amb_JurrasicBed at waypoint 47 (cell 164, 157).
4. Play sound _Amb_JurrasicBed at waypoint 48 (cell 181, 149).
5. Play sound _Amb_JurrasicBed at waypoint 68 (cell 182, 138).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9649, Events line 9953, Actions line 10257.

<a id="trigger-04421a8c"></a>

### 284. Detect_Mixed Team Dead - 04421A8C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 044219AC (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create_Mixed Yuri Team (0442182C)](#trigger-0442182c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9650, Events line 9954, Actions line 10258.

<a id="trigger-04415afc"></a>

### 285. Destroy_GG Bridge - 04415AFC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Piece Destroyed (044149EC)](#trigger-044149ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Destroy_GG Bridge (04415AFC)](#trigger-04415afc).
2. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9651, Events line 9955, Actions line 10259.

<a id="trigger-044149ec"></a>

### 286. Detect_Piece Destroyed - 044149EC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Destroy_GG Bridge (04415AFC)](#trigger-04415afc).

Incoming activation links: enable from [Fucking Shroud 2 (079BB93C)](#trigger-079bb93c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Detect_Piece Destroyed (044149EC)](#trigger-044149ec).
2. Enable and reset applicable timers for [Destroy_GG Bridge (04415AFC)](#trigger-04415afc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9652, Events line 9956, Actions line 10260.

<a id="trigger-0919e26c"></a>

### 287. Intro_Guardian_Audio - 0919E26C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Intro_Guardian @ PV (09198F3C)](#trigger-09198f3c); enable from [Intro_Guardian @ CV (09198B9C)](#trigger-09198b9c); enable from [Intro_Guardian @ CW (09198D6C)](#trigger-09198d6c); enable from [Intro_Guardian @ PA (0919965C)](#trigger-0919965c); enable from [Intro_Guardian @ PC (09199BCC)](#trigger-09199bcc); enable from [Intro_Guardian @ PG (0919948C)](#trigger-0919948c); enable from [Intro_Guardian @ PI (0919982C)](#trigger-0919982c); enable from [Intro_Guardian @ PK (091999FC)](#trigger-091999fc); enable from [Intro_Guardian @ PM (09199D9C)](#trigger-09199d9c).

Attached scope: tag definitions 0919E18C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_GuardianGi.

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9653, Events line 9957, Actions line 10261.

<a id="trigger-09198f3c"></a>

### 288. Intro_Guardian @ PV - 09198F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09198E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Intro_Guardian @ CV (09198B9C)](#trigger-09198b9c).
2. Disable [Intro_Guardian @ CW (09198D6C)](#trigger-09198d6c).
3. Enable and reset applicable timers for [Intro_Guardian_Audio (0919E26C)](#trigger-0919e26c).
4. Jump the camera to waypoint 437 (cell 137, 110).
5. Create/recruit team [TM_Allies_2 Guardian @ PV Intro (05C6F97C)](sov01umd-teams.md#team-05c6f97c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9654, Events line 9958, Actions line 10262.

<a id="trigger-09198b9c"></a>

### 289. Intro_Guardian @ CV - 09198B9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Guardian GI (GGI), owner Americans, cell (132, 82), tag 09198ABC, persistence mode 0; Guardian GI (GGI), owner Americans, cell (132, 83), tag 09198ABC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 99 (cell 131, 82).
2. Jump the camera to waypoint 99 (cell 131, 82).
3. Enable and reset applicable timers for [Intro_Guardian_Shutdown (091992BC)](#trigger-091992bc).
4. Enable and reset applicable timers for [Intro_Guardian_Audio (0919E26C)](#trigger-0919e26c).
5. Create/recruit team [TM_Allies_2 Guardian @ CV Intro (05C6FEFC)](sov01umd-teams.md#team-05c6fefc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9655, Events line 9959, Actions line 10263.

<a id="trigger-09198d6c"></a>

### 290. Intro_Guardian @ CW - 09198D6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09198C8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 100 (cell 132, 89).
2. Jump the camera to waypoint 100 (cell 132, 89).
3. Enable and reset applicable timers for [Intro_Guardian_Audio (0919E26C)](#trigger-0919e26c).
4. Enable and reset applicable timers for [Intro_Guardian_Shutdown (091992BC)](#trigger-091992bc).
5. Create/recruit team [TM_Allies_2 Guardian @ CW Intro (05C6FAEC)](sov01umd-teams.md#team-05c6faec).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9656, Events line 9960, Actions line 10264.

<a id="trigger-091992bc"></a>

### 291. Intro_Guardian_Shutdown - 091992BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Intro_Guardian @ CV (09198B9C)](#trigger-09198b9c); enable from [Intro_Guardian @ CW (09198D6C)](#trigger-09198d6c); enable from [Intro_Guardian @ PA (0919965C)](#trigger-0919965c); enable from [Intro_Guardian @ PC (09199BCC)](#trigger-09199bcc); enable from [Intro_Guardian @ PG (0919948C)](#trigger-0919948c); enable from [Intro_Guardian @ PI (0919982C)](#trigger-0919982c); enable from [Intro_Guardian @ PK (091999FC)](#trigger-091999fc); enable from [Intro_Guardian @ PM (09199D9C)](#trigger-09199d9c).

Attached scope: tag definitions 091991DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Intro_Guardian @ CV (09198B9C)](#trigger-09198b9c).
2. Disable [Intro_Guardian @ CW (09198D6C)](#trigger-09198d6c).
3. Disable [Intro_Guardian @ PA (0919965C)](#trigger-0919965c).
4. Disable [Intro_Guardian @ PC (09199BCC)](#trigger-09199bcc).
5. Disable [Intro_Guardian @ PG (0919948C)](#trigger-0919948c).
6. Disable [Intro_Guardian @ PI (0919982C)](#trigger-0919982c).
7. Disable [Intro_Guardian @ PK (091999FC)](#trigger-091999fc).
8. Disable [Intro_Guardian @ PM (09199D9C)](#trigger-09199d9c).
9. Disable [Intro_Guardian @ PV (09198F3C)](#trigger-09198f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9657, Events line 9961, Actions line 10265.

<a id="trigger-0919965c"></a>

### 292. Intro_Guardian @ PA - 0919965C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0919957C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 416 (cell 80, 114).
2. Jump the camera to waypoint 416 (cell 80, 114).
3. Enable and reset applicable timers for [Intro_Guardian_Audio (0919E26C)](#trigger-0919e26c).
4. Enable and reset applicable timers for [Intro_Guardian_Shutdown (091992BC)](#trigger-091992bc).
5. Create/recruit team [TM_Allies_Patrol Grand (PA) Intro (0442F2BC)](sov01umd-teams.md#team-0442f2bc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9658, Events line 9962, Actions line 10266.

<a id="trigger-09199bcc"></a>

### 293. Intro_Guardian @ PC - 09199BCC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09199AEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 418 (cell 79, 128).
2. Jump the camera to waypoint 418 (cell 79, 128).
3. Enable and reset applicable timers for [Intro_Guardian_Audio (0919E26C)](#trigger-0919e26c).
4. Enable and reset applicable timers for [Intro_Guardian_Shutdown (091992BC)](#trigger-091992bc).
5. Create/recruit team [TM_Allies_Patrol Statue (PC) Intro (0442D72C)](sov01umd-teams.md#team-0442d72c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9659, Events line 9963, Actions line 10267.

<a id="trigger-0919948c"></a>

### 294. Intro_Guardian @ PG - 0919948C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 091993AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 422 (cell 89, 119).
2. Jump the camera to waypoint 422 (cell 89, 119).
3. Enable and reset applicable timers for [Intro_Guardian_Audio (0919E26C)](#trigger-0919e26c).
4. Enable and reset applicable timers for [Intro_Guardian_Shutdown (091992BC)](#trigger-091992bc).
5. Create/recruit team [TM_Allies_Patrol Park (PG) Intro (0442DB4C)](sov01umd-teams.md#team-0442db4c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9660, Events line 9964, Actions line 10268.

<a id="trigger-0919982c"></a>

### 295. Intro_Guardian @ PI - 0919982C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0919974C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 424 (cell 110, 110).
2. Jump the camera to waypoint 424 (cell 110, 110).
3. Enable and reset applicable timers for [Intro_Guardian_Audio (0919E26C)](#trigger-0919e26c).
4. Enable and reset applicable timers for [Intro_Guardian_Shutdown (091992BC)](#trigger-091992bc).
5. Create/recruit team [TM_Allies_Patrol Gas (PI) Intro (0442F79C)](sov01umd-teams.md#team-0442f79c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9661, Events line 9965, Actions line 10269.

<a id="trigger-091999fc"></a>

### 296. Intro_Guardian @ PK - 091999FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0919991C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 426 (cell 127, 114).
2. Jump the camera to waypoint 426 (cell 127, 114).
3. Enable and reset applicable timers for [Intro_Guardian_Audio (0919E26C)](#trigger-0919e26c).
4. Enable and reset applicable timers for [Intro_Guardian_Shutdown (091992BC)](#trigger-091992bc).
5. Create/recruit team [TM_Allies_Patrol BottomTime (PK) Intro (0442F9EC)](sov01umd-teams.md#team-0442f9ec).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9662, Events line 9966, Actions line 10270.

<a id="trigger-09199d9c"></a>

### 297. Intro_Guardian @ PM - 09199D9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09199CBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 428 (cell 117, 85).
2. Jump the camera to waypoint 428 (cell 117, 85).
3. Enable and reset applicable timers for [Intro_Guardian_Audio (0919E26C)](#trigger-0919e26c).
4. Enable and reset applicable timers for [Intro_Guardian_Shutdown (091992BC)](#trigger-091992bc).
5. Create/recruit team [TM_Allies_Patrol TopTime (PM) Intro (0442D2CC)](sov01umd-teams.md#team-0442d2cc).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9663, Events line 9967, Actions line 10271.

<a id="trigger-079f9b1c"></a>

### 298. SP2.6a_Trans 3 Ready - 079F9B1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079F9A3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 8 (Trans 3 Unloaded) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP2.6b_Trans 3 Leaves (05DB7F3C)](#trigger-05db7f3c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9664, Events line 9968, Actions line 10272.

<a id="trigger-05db7f3c"></a>

### 299. SP2.6b_Trans 3 Leaves - 05DB7F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.6a_Trans 3 Ready (079F9B1C)](#trigger-079f9b1c).

Attached scope: tag definitions 05DB7E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TM_Sov_1 Trans (Flak) (0B4AA55C)](sov01umd-teams.md#team-0b4aa55c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9665, Events line 9969, Actions line 10273.

<a id="trigger-088beb4c"></a>

### 300. _Setup_Part Ic - 088BEB4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 088BEA6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 102 (cell 22, 71).
2. Reveal terrain around waypoint 103 (cell 28, 60).
3. Reveal terrain around waypoint 133 (cell 52, 35).
4. Reveal terrain around waypoint 146 (cell 32, 55).
5. Reveal terrain around waypoint 147 (cell 42, 60).
6. Reveal terrain around waypoint 148 (cell 43, 49).
7. Reveal terrain around waypoint 149 (cell 50, 44).
8. Reveal terrain around waypoint 150 (cell 69, 21).
9. Reveal terrain around waypoint 101 (cell 49, 73).
10. Reveal terrain around waypoint 151 (cell 49, 80).
11. Reveal terrain around waypoint 152 (cell 54, 77).
12. Reveal terrain around waypoint 153 (cell 56, 73).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9666, Events line 9970, Actions line 10274.

<a id="trigger-078c97ec"></a>

### 301. Fucking Shroud 1 - 078C97EC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Detect_Piece Destroyed (044149EC)](#trigger-044149ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Change House: owner selector 8 (country/type RUSSIANS; placed owner Russians).
2. Disable [Fucking Shroud 1 (078C97EC)](#trigger-078c97ec).
3. Enable and reset applicable timers for [Fucking Shroud 2 (079BB93C)](#trigger-079bb93c).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9667, Events line 9971, Actions line 10275.

<a id="trigger-079bb93c"></a>

### 302. Fucking Shroud 2 - 079BB93C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Fucking Shroud 1 (078C97EC)](#trigger-078c97ec).

Incoming activation links: enable from [Fucking Shroud 1 (078C97EC)](#trigger-078c97ec).

Attached scope: Golden Gate Bridge (CASANF04), owner Neutral, cell (59, 99), tag 04415A1C, persistence mode 2; Golden Gate Bridge (CASANF11), owner Neutral, cell (62, 99), tag 04415A1C, persistence mode 2; Golden Gate Bridge (CASANF12), owner Neutral, cell (56, 99), tag 04415A1C, persistence mode 2; Golden Gate Bridge (CASANF13), owner Neutral, cell (53, 99), tag 04415A1C, persistence mode 2; Golden Gate Bridge (CASANF14), owner Neutral, cell (50, 99), tag 04415A1C, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 12 (country/type NEUTRAL; placed owner Neutral).
2. Disable [Fucking Shroud 2 (079BB93C)](#trigger-079bb93c).
3. Enable and reset applicable timers for [Detect_Piece Destroyed (044149EC)](#trigger-044149ec).

Source locator: mapsmd03.mix/sov01umd.map; Triggers line 9668, Events line 9972, Actions line 10276.

[All team rosters and ordered plans](sov01umd-teams.md) | [All mission overrides](sov01umd-overrides.md)
