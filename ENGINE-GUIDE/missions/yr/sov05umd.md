# Operation: Escape Velocity

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for sov05umd.map.](../../images/map-sov05umd.svg)

*Initial placement schematic for sov05umd.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** sov05umd.map. **Effective extracted member:** mapsmd03.mix/sov05umd.map. **Trigger definitions:** 115.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov05umd-teams.md) | [All mission overrides](sov05umd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Russians |
| Theater | NEWURBAN |
| Map size | 0,0,135,145 |
| Visible local rectangle | 2,4,131,135 |
| Placed vehicles | 20 |
| Placed infantry | 122 |
| Placed structures | 92 |
| Placed aircraft | 0 |
| Team templates | 122 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 0 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 500 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 0 | Africans |
| 6 | Arabs | 0 | Arabs |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 100 | Russians |
| 9 | YuriCountry | 500 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 0 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |
| 14 | Yuri2Country | 500 | Yuri2 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Sub Pen Destroyed,0 |
| 1 | MCV @ AI,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [_Loser (09442BBC)](#trigger-09442bbc) | Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians). | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser. |
| [_Winner (094429EC)](#trigger-094429ec) | 35 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner. |

## Every trigger, in file order

<a id="trigger-09563d6c"></a>

### 1. SP1.1_Movie_Zof Intro - 09563D6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0956367C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable player input.
2. Play in-game movie 49.
3. Enable and reset applicable timers for [SP1.2_Squids Move (0956358C)](#trigger-0956358c).
4. Reveal terrain around waypoint 699 (cell 138, 21).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11039, Events line 11156, Actions line 11273.

<a id="trigger-0956358c"></a>

### 2. SP1.2_Squids Move - 0956358C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.1_Movie_Zof Intro (09563D6C)](#trigger-09563d6c).

Attached scope: tag definitions 095634AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Squid 1 (095EBDBC)](sov05umd-teams.md#team-095ebdbc).
2. Supply reinforcement team [TM_Sov_Squid 2 (095EB94C)](sov05umd-teams.md#team-095eb94c).
3. Supply reinforcement team [TM_Sov_Squid 3 (095EB52C)](sov05umd-teams.md#team-095eb52c).
4. Enable and reset applicable timers for [SP1.3_Subs Move (095633BC)](#trigger-095633bc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11040, Events line 11157, Actions line 11274.

<a id="trigger-095633bc"></a>

### 3. SP1.3_Subs Move - 095633BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.2_Squids Move (0956358C)](#trigger-0956358c).

Attached scope: tag definitions 095632DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Sub 1 (095EB14C)](sov05umd-teams.md#team-095eb14c).
2. Supply reinforcement team [TM_Sov_Sub 2 (095ECC8C)](sov05umd-teams.md#team-095ecc8c).
3. Supply reinforcement team [TM_Sov_Sub 3 (095EC8EC)](sov05umd-teams.md#team-095ec8ec).
4. Supply reinforcement team [TM_Sov_Sub 4 (095EC54C)](sov05umd-teams.md#team-095ec54c).
5. Enable and reset applicable timers for [SP1.4_Scorpion 1 Move (095631EC)](#trigger-095631ec).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11041, Events line 11158, Actions line 11275.

<a id="trigger-095631ec"></a>

### 4. SP1.4_Scorpion 1 Move - 095631EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.3_Subs Move (095633BC)](#trigger-095633bc).

Attached scope: tag definitions 0956310C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Scorpion 1 (095EC1AC)](sov05umd-teams.md#team-095ec1ac).
2. Enable and reset applicable timers for [SP1.5_MCV Trans Move (09564F3C)](#trigger-09564f3c).
3. Enable and reset applicable timers for [_Loser (09442BBC)](#trigger-09442bbc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11042, Events line 11159, Actions line 11276.

<a id="trigger-09564f3c"></a>

### 5. SP1.5_MCV Trans Move - 09564F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.4_Scorpion 1 Move (095631EC)](#trigger-095631ec).

Attached scope: tag definitions 09564E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_1 Trans_1 MCV_2 Rhino (094B31CC)](sov05umd-teams.md#team-094b31cc).
2. Enable and reset applicable timers for [SP1.6_Battle Group Move (09564D6C)](#trigger-09564d6c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11043, Events line 11160, Actions line 11277.

<a id="trigger-09442bbc"></a>

### 6. _Loser - 09442BBC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.4_Scorpion 1 Move (095631EC)](#trigger-095631ec).

Attached scope: tag definitions 09442ADC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11044, Events line 11161, Actions line 11278.

<a id="trigger-09564d6c"></a>

### 7. SP1.6_Battle Group Move - 09564D6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.5_MCV Trans Move (09564F3C)](#trigger-09564f3c).

Attached scope: tag definitions 09564C8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_Dreadnought 1 (095ED64C)](sov05umd-teams.md#team-095ed64c).
2. Supply reinforcement team [TM_Sov_Dreadnought 2 (095ED26C)](sov05umd-teams.md#team-095ed26c).
3. Supply reinforcement team [TM_Sov_Dreadnought 3 (095ED0FC)](sov05umd-teams.md#team-095ed0fc).
4. Supply reinforcement team [TM_Sov_Scorpion 2 (095EE67C)](sov05umd-teams.md#team-095ee67c).
5. Supply reinforcement team [TM_Sov_Scorpion 3 (095EE2DC)](sov05umd-teams.md#team-095ee2dc).
6. Supply reinforcement team [TM_Sov_Scorpion 4 (095EFEBC)](sov05umd-teams.md#team-095efebc).
7. Supply reinforcement team [TM_Sov_Scorpion 5 (095EFB1C)](sov05umd-teams.md#team-095efb1c).
8. Supply reinforcement team [TM_Sov_1 Trans_12 Conscript (0C942C8C)](sov05umd-teams.md#team-0c942c8c).
9. Supply reinforcement team [TM_Sov_1 Trans_3 Flak Trak (095EEA1C)](sov05umd-teams.md#team-095eea1c).
10. Enable and reset applicable timers for [SP1.7_Audio_Brief 1 (09564B9C)](#trigger-09564b9c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11045, Events line 11162, Actions line 11279.

<a id="trigger-09564b9c"></a>

### 8. SP1.7_Audio_Brief 1 - 09564B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.6_Battle Group Move (09564D6C)](#trigger-09564d6c).

Attached scope: tag definitions 09564ABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaBriefing01.
2. Enable and reset applicable timers for [SP1.8_Audio_Brief 2 (095649CC)](#trigger-095649cc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11046, Events line 11163, Actions line 11280.

<a id="trigger-095649cc"></a>

### 9. SP1.8_Audio_Brief 2 - 095649CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.7_Audio_Brief 1 (09564B9C)](#trigger-09564b9c).

Attached scope: tag definitions 095648EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaBriefing02.
2. Jump the camera to waypoint 35 (cell 49, 138).
3. Play sound CameraSwitch.
4. Enable and reset applicable timers for [SP1.9_Audio_Brief 3 (095647FC)](#trigger-095647fc).
5. Reveal terrain around waypoint 35 (cell 49, 138).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11047, Events line 11164, Actions line 11281.

<a id="trigger-095647fc"></a>

### 10. SP1.9_Audio_Brief 3 - 095647FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.8_Audio_Brief 2 (095649CC)](#trigger-095649cc).

Attached scope: tag definitions 0956471C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaBriefing03.
2. Jump the camera to waypoint 36 (cell 115, 66).
3. Play sound CameraSwitch.
4. Enable and reset applicable timers for [SP1.10_Audio_Brief 4 (0956462C)](#trigger-0956462c).
5. Reveal terrain around waypoint 36 (cell 115, 66).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11048, Events line 11165, Actions line 11282.

<a id="trigger-0956462c"></a>

### 11. SP1.10_Audio_Brief 4 - 0956462C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.9_Audio_Brief 3 (095647FC)](#trigger-095647fc).

Attached scope: tag definitions 0956454C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaBriefing04.
2. Jump the camera to waypoint 37 (cell 214, 122).
3. Play sound CameraSwitch.
4. Enable and reset applicable timers for [SP1.11_Audio_Brief 5 (0956436C)](#trigger-0956436c).
5. Reveal terrain around waypoint 37 (cell 214, 122).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11049, Events line 11166, Actions line 11283.

<a id="trigger-0956436c"></a>

### 12. SP1.11_Audio_Brief 5 - 0956436C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.10_Audio_Brief 4 (0956462C)](#trigger-0956462c).

Attached scope: tag definitions 0956428C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaBriefing05.
2. Create radar-event marker type 0 at waypoint 61 (cell 137, 150).
3. Enable and reset applicable timers for [SP1.12_Audio_Brief 6 (0956419C)](#trigger-0956419c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11050, Events line 11167, Actions line 11284.

<a id="trigger-0956419c"></a>

### 13. SP1.12_Audio_Brief 6 - 0956419C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.11_Audio_Brief 5 (0956436C)](#trigger-0956436c).

Attached scope: tag definitions 095640BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaBriefing06.
2. Jump the camera to waypoint 38 (cell 139, 183).
3. Play sound CameraSwitch.
4. Enable and reset applicable timers for [SP1.13_Audio_Brief 7 (09565F3C)](#trigger-09565f3c).
5. Reveal terrain around waypoint 38 (cell 139, 183).
6. Reveal terrain around waypoint 62 (cell 154, 180).
7. Reveal terrain around waypoint 63 (cell 159, 183).
8. Enable and reset applicable timers for [SP1.12a_Camera Move (0E6D433C)](#trigger-0e6d433c).
9. Reveal terrain around waypoint 69 (cell 146, 180).
10. Reveal terrain around waypoint 70 (cell 148, 186).
11. Reveal terrain around waypoint 71 (cell 137, 182).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11051, Events line 11168, Actions line 11285.

<a id="trigger-09565f3c"></a>

### 14. SP1.13_Audio_Brief 7 - 09565F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.12_Audio_Brief 6 (0956419C)](#trigger-0956419c).

Attached scope: tag definitions 09565E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 17 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaBriefing07.
2. Enable and reset applicable timers for [SP1.14_Radar Ping 1 (09565D6C)](#trigger-09565d6c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11052, Events line 11169, Actions line 11286.

<a id="trigger-0e6d433c"></a>

### 15. SP1.12a_Camera Move - 0E6D433C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.12_Audio_Brief 6 (0956419C)](#trigger-0956419c).

Attached scope: tag definitions 0E6D410C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 68 (cell 155, 183) with speed setting 2.
2. Enable and reset applicable timers for [SP1.12b_Camera Move 2 (0796B7CC)](#trigger-0796b7cc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11053, Events line 11170, Actions line 11287.

<a id="trigger-09565d6c"></a>

### 16. SP1.14_Radar Ping 1 - 09565D6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.13_Audio_Brief 7 (09565F3C)](#trigger-09565f3c).

Attached scope: tag definitions 09565C8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 39 (cell 123, 39).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.15_Radar Ping 2 (09565B9C)](#trigger-09565b9c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11054, Events line 11171, Actions line 11288.

<a id="trigger-0796b7cc"></a>

### 17. SP1.12b_Camera Move 2 - 0796B7CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.12a_Camera Move (0E6D433C)](#trigger-0e6d433c).

Attached scope: tag definitions 0796B4FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 38 (cell 139, 183) with speed setting 2.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11055, Events line 11172, Actions line 11289.

<a id="trigger-09565b9c"></a>

### 18. SP1.15_Radar Ping 2 - 09565B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.14_Radar Ping 1 (09565D6C)](#trigger-09565d6c).

Attached scope: tag definitions 09565ABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 40 (cell 106, 48).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.16_Radar Ping 3 (095659CC)](#trigger-095659cc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11056, Events line 11173, Actions line 11290.

<a id="trigger-095659cc"></a>

### 19. SP1.16_Radar Ping 3 - 095659CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.15_Radar Ping 2 (09565B9C)](#trigger-09565b9c).

Attached scope: tag definitions 095658EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 41 (cell 93, 62).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.17_Radar Ping 4 (095657FC)](#trigger-095657fc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11057, Events line 11174, Actions line 11291.

<a id="trigger-095657fc"></a>

### 20. SP1.17_Radar Ping 4 - 095657FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.16_Radar Ping 3 (095659CC)](#trigger-095659cc).

Attached scope: tag definitions 0956571C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 42 (cell 76, 75).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.18_Radar Ping 5 (0956562C)](#trigger-0956562c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11058, Events line 11175, Actions line 11292.

<a id="trigger-0956562c"></a>

### 21. SP1.18_Radar Ping 5 - 0956562C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.17_Radar Ping 4 (095657FC)](#trigger-095657fc).

Attached scope: tag definitions 0956554C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 43 (cell 64, 94).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.19_Radar Ping 6 (0956545C)](#trigger-0956545c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11059, Events line 11176, Actions line 11293.

<a id="trigger-0956545c"></a>

### 22. SP1.19_Radar Ping 6 - 0956545C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.18_Radar Ping 5 (0956562C)](#trigger-0956562c).

Attached scope: tag definitions 0956537C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 44 (cell 53, 113).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.20_Radar Ping 7 (0956528C)](#trigger-0956528c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11060, Events line 11177, Actions line 11294.

<a id="trigger-0956528c"></a>

### 23. SP1.20_Radar Ping 7 - 0956528C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.19_Radar Ping 6 (0956545C)](#trigger-0956545c).

Attached scope: tag definitions 095651AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 45 (cell 36, 128).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.21_Radar Ping 8 (095650BC)](#trigger-095650bc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11061, Events line 11178, Actions line 11295.

<a id="trigger-095650bc"></a>

### 24. SP1.21_Radar Ping 8 - 095650BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.20_Radar Ping 7 (0956528C)](#trigger-0956528c).

Attached scope: tag definitions 09566F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 46 (cell 47, 159).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.22_Radar Ping 9 (09566E5C)](#trigger-09566e5c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11062, Events line 11179, Actions line 11296.

<a id="trigger-09566e5c"></a>

### 25. SP1.22_Radar Ping 9 - 09566E5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.21_Radar Ping 8 (095650BC)](#trigger-095650bc).

Attached scope: tag definitions 09566D7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 47 (cell 65, 179).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.23_Radar Ping 10 (0E98EE5C)](#trigger-0e98ee5c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11063, Events line 11180, Actions line 11297.

<a id="trigger-0e98ee5c"></a>

### 26. SP1.23_Radar Ping 10 - 0E98EE5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.22_Radar Ping 9 (09566E5C)](#trigger-09566e5c).

Attached scope: tag definitions 0E98ED7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 48 (cell 84, 204).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.24_Radar Ping 11 (0E98EC8C)](#trigger-0e98ec8c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11064, Events line 11181, Actions line 11298.

<a id="trigger-0e98ec8c"></a>

### 27. SP1.24_Radar Ping 11 - 0E98EC8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.23_Radar Ping 10 (0E98EE5C)](#trigger-0e98ee5c).

Attached scope: tag definitions 0E98EBAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 49 (cell 108, 223).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.25_Radar Ping 12 (0E98EABC)](#trigger-0e98eabc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11065, Events line 11182, Actions line 11299.

<a id="trigger-0e98eabc"></a>

### 28. SP1.25_Radar Ping 12 - 0E98EABC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.24_Radar Ping 11 (0E98EC8C)](#trigger-0e98ec8c).

Attached scope: tag definitions 0E98E9DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 50 (cell 134, 224).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.26_Radar Ping 13 (0E98E8EC)](#trigger-0e98e8ec).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11066, Events line 11183, Actions line 11300.

<a id="trigger-0e98e8ec"></a>

### 29. SP1.26_Radar Ping 13 - 0E98E8EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.25_Radar Ping 12 (0E98EABC)](#trigger-0e98eabc).

Attached scope: tag definitions 0E98E80C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 51 (cell 152, 199).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.27_Radar Ping 14 (0E98E71C)](#trigger-0e98e71c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11067, Events line 11184, Actions line 11301.

<a id="trigger-0e98e71c"></a>

### 30. SP1.27_Radar Ping 14 - 0E98E71C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.26_Radar Ping 13 (0E98E8EC)](#trigger-0e98e8ec).

Attached scope: tag definitions 0E98E63C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 52 (cell 182, 205).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.28_Radar Ping 15 (0E98E54C)](#trigger-0e98e54c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11068, Events line 11185, Actions line 11302.

<a id="trigger-0e98e54c"></a>

### 31. SP1.28_Radar Ping 15 - 0E98E54C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.27_Radar Ping 14 (0E98E71C)](#trigger-0e98e71c).

Attached scope: tag definitions 0E98E46C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 53 (cell 205, 200).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.29_Radar Ping 16 (0E98E37C)](#trigger-0e98e37c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11069, Events line 11186, Actions line 11303.

<a id="trigger-0e98e37c"></a>

### 32. SP1.29_Radar Ping 16 - 0E98E37C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.28_Radar Ping 15 (0E98E54C)](#trigger-0e98e54c).

Attached scope: tag definitions 0E98E29C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 54 (cell 221, 182).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.30_Radar Ping 17 (0E98E1AC)](#trigger-0e98e1ac).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11070, Events line 11187, Actions line 11304.

<a id="trigger-0e98e1ac"></a>

### 33. SP1.30_Radar Ping 17 - 0E98E1AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.29_Radar Ping 16 (0E98E37C)](#trigger-0e98e37c).

Attached scope: tag definitions 0E98E0CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 55 (cell 237, 165).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.31_Radar Ping 18 (0E98FF3C)](#trigger-0e98ff3c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11071, Events line 11188, Actions line 11305.

<a id="trigger-0e98ff3c"></a>

### 34. SP1.31_Radar Ping 18 - 0E98FF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.30_Radar Ping 17 (0E98E1AC)](#trigger-0e98e1ac).

Attached scope: tag definitions 0E98FE5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 56 (cell 253, 145).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.32_Radar Ping 19 (0E98FD6C)](#trigger-0e98fd6c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11072, Events line 11189, Actions line 11306.

<a id="trigger-0e98fd6c"></a>

### 35. SP1.32_Radar Ping 19 - 0E98FD6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.31_Radar Ping 18 (0E98FF3C)](#trigger-0e98ff3c).

Attached scope: tag definitions 0E98FC8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 57 (cell 231, 121).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.33_Radar Ping 20 (0E98FB9C)](#trigger-0e98fb9c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11073, Events line 11190, Actions line 11307.

<a id="trigger-0e98fb9c"></a>

### 36. SP1.33_Radar Ping 20 - 0E98FB9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.32_Radar Ping 19 (0E98FD6C)](#trigger-0e98fd6c).

Attached scope: tag definitions 0E98FABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 58 (cell 204, 97).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.34_Radar Ping 21 (0E98F9CC)](#trigger-0e98f9cc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11074, Events line 11191, Actions line 11308.

<a id="trigger-0e98f9cc"></a>

### 37. SP1.34_Radar Ping 21 - 0E98F9CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.33_Radar Ping 20 (0E98FB9C)](#trigger-0e98fb9c).

Attached scope: tag definitions 0E98F8EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 59 (cell 181, 75).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.35_Radar Ping 22 (0E98F7FC)](#trigger-0e98f7fc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11075, Events line 11192, Actions line 11309.

<a id="trigger-0e98f7fc"></a>

### 38. SP1.35_Radar Ping 22 - 0E98F7FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.34_Radar Ping 21 (0E98F9CC)](#trigger-0e98f9cc).

Attached scope: tag definitions 0E98F71C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 60 (cell 162, 48).
2. Play sound MessageText.
3. Enable and reset applicable timers for [SP1.36_Audio_Briefing 8 (0E98F62C)](#trigger-0e98f62c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11076, Events line 11193, Actions line 11310.

<a id="trigger-0e98f62c"></a>

### 39. SP1.36_Audio_Briefing 8 - 0E98F62C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.35_Radar Ping 22 (0E98F7FC)](#trigger-0e98f7fc).

Attached scope: tag definitions 0E98F54C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaBriefing08.
2. Jump the camera to waypoint 699 (cell 138, 21).
3. Play sound CameraSwitch.
4. Enable and reset applicable timers for [SP1.37_End/Unlock (0E98F45C)](#trigger-0e98f45c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11077, Events line 11194, Actions line 11311.

<a id="trigger-0e98f45c"></a>

### 40. SP1.37_End/Unlock - 0E98F45C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.36_Audio_Briefing 8 (0E98F62C)](#trigger-0e98f62c).

Attached scope: tag definitions 0E98F37C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Play voice notification EVA_BattlefieldControlOnline.
3. Enable and reset applicable timers for [Text/Ping_Objective 1 (079AC3AC)](#trigger-079ac3ac).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11078, Events line 11195, Actions line 11312.

<a id="trigger-079ac3ac"></a>

### 41. Text/Ping_Objective 1 - 079AC3AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP1.37_End/Unlock (0E98F45C)](#trigger-0e98f45c).

Attached scope: tag definitions 079AC2CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Pick a landing zone and construct a base.” (MISSION:Sov5Obj1).
2. Create radar-event marker type 1 at waypoint 35 (cell 49, 138).
3. Create radar-event marker type 1 at waypoint 36 (cell 115, 66).
4. Create radar-event marker type 1 at waypoint 37 (cell 214, 122).
5. Enable and reset applicable timers for [Repeat_Text/Ping_Obj 1 (079B57EC)](#trigger-079b57ec).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11079, Events line 11196, Actions line 11313.

<a id="trigger-079b57ec"></a>

### 42. Repeat_Text/Ping_Obj 1 - 079B57EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Text/Ping_Objective 1 (079AC3AC)](#trigger-079ac3ac).

Attached scope: tag definitions 079B570C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Pick a landing zone and construct a base.” (MISSION:Sov5Obj1).
2. Create radar-event marker type 1 at waypoint 35 (cell 49, 138).
3. Create radar-event marker type 1 at waypoint 36 (cell 115, 66).
4. Create radar-event marker type 1 at waypoint 37 (cell 214, 122).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11080, Events line 11197, Actions line 11314.

<a id="trigger-0976785c"></a>

### 43. _Setup_Sov05_1 - 0976785C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097673CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_Boomer @ AN (095AB25C)](sov05umd-teams.md#team-095ab25c).
2. Supply reinforcement team [TM_Yuri_Boomer @ AO (095AC88C)](sov05umd-teams.md#team-095ac88c).
3. Supply reinforcement team [TM_Yuri_Boomer @ AP (095AC39C)](sov05umd-teams.md#team-095ac39c).
4. Supply reinforcement team [TM_Yuri_Boomer @ AQ (095ADEBC)](sov05umd-teams.md#team-095adebc).
5. Supply reinforcement team [TM_Yuri_Boomer @ AR (095ADA9C)](sov05umd-teams.md#team-095ada9c).
6. Supply reinforcement team [TM_Yuri_Boomer @ AS (06B623CC)](sov05umd-teams.md#team-06b623cc).
7. Supply reinforcement team [TM_Yuri_Boomer @ AT (06B63D8C)](sov05umd-teams.md#team-06b63d8c).
8. Supply reinforcement team [TM_Yuri_Boomer @ AU (06B6389C)](sov05umd-teams.md#team-06b6389c).
9. Supply reinforcement team [TM_Yuri_Boomer @ AV (06B633FC)](sov05umd-teams.md#team-06b633fc).
10. Supply reinforcement team [TM_Yuri_Boomer @ AW (06B64EFC)](sov05umd-teams.md#team-06b64efc).
11. Supply reinforcement team [TM_Yuri_Boomer @ AX (06B64ADC)](sov05umd-teams.md#team-06b64adc).
12. Supply reinforcement team [TM_Yuri_Boomer @ AY (06B6426C)](sov05umd-teams.md#team-06b6426c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11081, Events line 11198, Actions line 11315.

<a id="trigger-0ee100bc"></a>

### 44. _Setup_Sov05_2 - 0EE100BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0EE11F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_Boomer @ BA (097A5EFC)](sov05umd-teams.md#team-097a5efc).
2. Supply reinforcement team [TM_Yuri_Boomer @ BB (097A59FC)](sov05umd-teams.md#team-097a59fc).
3. Supply reinforcement team [TM_Yuri_Boomer @ BC (097A7C8C)](sov05umd-teams.md#team-097a7c8c).
4. Supply reinforcement team [TM_Yuri_Boomer @ BD (097A78EC)](sov05umd-teams.md#team-097a78ec).
5. Supply reinforcement team [TM_Yuri_Boomer @ BE (097A748C)](sov05umd-teams.md#team-097a748c).
6. Supply reinforcement team [TM_Yuri_Boomer @ BF (0979E77C)](sov05umd-teams.md#team-0979e77c).
7. Supply reinforcement team [TM_Yuri_Boomer @ BG (095AAC8C)](sov05umd-teams.md#team-095aac8c).
8. Supply reinforcement team [TM_Yuri_Boomer @ BH (095AA7EC)](sov05umd-teams.md#team-095aa7ec).
9. Supply reinforcement team [TM_Yuri_Boomer @ BI (095AA38C)](sov05umd-teams.md#team-095aa38c).
10. Supply reinforcement team [TM_Yuri_3 Init_Back Base Def (0940FDEC)](sov05umd-teams.md#team-0940fdec).
11. Supply reinforcement team [TM_Yuri_3 Init_Base Left Def (0968424C)](sov05umd-teams.md#team-0968424c).
12. Supply reinforcement team [TM_Yuri_3 Init_Base Right Def (09683C8C)](sov05umd-teams.md#team-09683c8c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11082, Events line 11199, Actions line 11316.

<a id="trigger-0baf671c"></a>

### 45. _Setup_Sov05_3 - 0BAF671C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BAF663C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_2 Brute_2 Gatt_Back Base (0C81854C)](sov05umd-teams.md#team-0c81854c).
2. Supply reinforcement team [TM_Yuri_4 Gatt_Sub Pen (0C8B6A4C)](sov05umd-teams.md#team-0c8b6a4c).
3. Supply reinforcement team [TM_Yuri_3 Clone_2 Brute_L Top Base (0C8B156C)](sov05umd-teams.md#team-0c8b156c).
4. Supply reinforcement team [TM_Yuri_3 Clone_2 Brute_LB Low In (0C8B2A4C)](sov05umd-teams.md#team-0c8b2a4c).
5. Supply reinforcement team [TM_Yuri_3 Clone_2 Brute_LF Low In (0C8B26AC)](sov05umd-teams.md#team-0c8b26ac).
6. Supply reinforcement team [TM_Yuri_3 Clone_2 Brute_R Top Base (0C8B2DEC)](sov05umd-teams.md#team-0c8b2dec).
7. Supply reinforcement team [TM_Yuri_3 Clone_2 Brute_RB Low In (0C8B230C)](sov05umd-teams.md#team-0c8b230c).
8. Supply reinforcement team [TM_Yuri_3 Clone_2 Brute_RF Low In (0C8B3C8C)](sov05umd-teams.md#team-0c8b3c8c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11083, Events line 11200, Actions line 11317.

<a id="trigger-0bafe7ac"></a>

### 46. _Setup_Sov05_4 - 0BAFE7AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BAFE5CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_3 Gatt_L Base Ramp (0C81BC8C)](sov05umd-teams.md#team-0c81bc8c).
2. Supply reinforcement team [TM_Yuri_3 Gatt_R Base Ramp (0C81B7DC)](sov05umd-teams.md#team-0c81b7dc).
3. Supply reinforcement team [TM_Yuri_3 Lash_LB Low Out (0C4C58EC)](sov05umd-teams.md#team-0c4c58ec).
4. Supply reinforcement team [TM_Yuri_3 Lash_LF Low Out (0C8B530C)](sov05umd-teams.md#team-0c8b530c).
5. Supply reinforcement team [TM_Yuri_3 Lash_RB Low Out (0C4C8B7C)](sov05umd-teams.md#team-0c4c8b7c).
6. Supply reinforcement team [TM_Yuri_3 Lash_RF Low Out (0C4C87DC)](sov05umd-teams.md#team-0c4c87dc).
7. Supply reinforcement team [TM_Yuri_3 Virus_8 Init_LB Up (0C8B5B7C)](sov05umd-teams.md#team-0c8b5b7c).
8. Supply reinforcement team [TM_Yuri_3 Virus_8 Init_LF Up (0C8ADA4C)](sov05umd-teams.md#team-0c8ada4c).
9. Supply reinforcement team [TM_Yuri_3 Virus_8 Init_RB Up (0C8F47BC)](sov05umd-teams.md#team-0c8f47bc).
10. Supply reinforcement team [TM_Yuri_3 Virus_8 Init_RF Up (0C8B57DC)](sov05umd-teams.md#team-0c8b57dc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11084, Events line 11201, Actions line 11318.

<a id="trigger-0baef32c"></a>

### 47. _Setup_Sov05_5 - 0BAEF32C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BAECF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_4 Brute_3 Gatt_L In Beach (0C8B38EC)](sov05umd-teams.md#team-0c8b38ec).
2. Supply reinforcement team [TM_Yuri_4 Brute_3 Gatt_R In Beach (0C8B343C)](sov05umd-teams.md#team-0c8b343c).
3. Supply reinforcement team [TM_Yuri_4 Brute_F Base (0C81B43C)](sov05umd-teams.md#team-0c81b43c).
4. Supply reinforcement team [TM_Yuri_4 Brute_R Base (0C81CDEC)](sov05umd-teams.md#team-0c81cdec).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11085, Events line 11202, Actions line 11319.

<a id="trigger-096bdcfc"></a>

### 48. _Setup_Sov05_6 - 096BDCFC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096BDC1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11086, Events line 11203, Actions line 11320.

<a id="trigger-096bd35c"></a>

### 49. _Setup_Sov05_7 - 096BD35C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096BD27C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11087, Events line 11204, Actions line 11321.

<a id="trigger-0d409afc"></a>

### 50. Lunching Pad Off - 0D409AFC

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable [Lunching Pad Off (0D409AFC)](#trigger-0d409afc).
2. Change House: owner selector 2 (country/type FRENCH; placed owner French).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11088, Events line 11205, Actions line 11322.

<a id="trigger-0d40992c"></a>

### 51. Lunching Pad On - 0D40992C

Owner reference: French. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Lunching Pad Off (0D409AFC)](#trigger-0d409afc).

Incoming activation links: enable from [SP2.3_Iris Open (092E05BC)](#trigger-092e05bc).

Attached scope: Unknown Building (YAROCK), owner French, cell (136, 135), tag 0D409A1C, persistence mode 2.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Lunching Pad On (0D40992C)](#trigger-0d40992c).
2. Change House: owner selector 3 (country/type GERMANS; placed owner Germans).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11089, Events line 11206, Actions line 11323.

<a id="trigger-06a4894c"></a>

### 52. Audio_Zof_Iron Curtain - 06A4894C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 37 tagged map cells: (166, 174), (167, 174), (168, 174), (196, 174), (165, 175), (166, 175), (196, 175), (197, 175), (198, 175), (164, 176), (165, 176), (198, 176), (199, 176), (200, 176), (164, 177), (200, 177), (164, 178), (200, 178), (164, 179), (165, 179), (166, 179), (167, 179), (200, 179), (167, 180), (200, 180), (167, 181), (198, 181), (199, 181), (200, 181), (193, 182), (194, 182), (198, 182), (194, 183), (195, 183), (196, 183), (197, 183), (198, 183); tag 06A49DAC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaIronCurtainSuggest.
2. Destroy current instances of [Audio_Zof_Iron Curtain2 (09701F3C)](#trigger-09701f3c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11090, Events line 11207, Actions line 11324.

<a id="trigger-09701f3c"></a>

### 53. Audio_Zof_Iron Curtain2 - 09701F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Statues (0ED7151C)](#trigger-0ed7151c).

Attached scope: tag definitions 09701E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaIronCurtainSuggest.
2. Disable [Audio_Zof_Iron Curtain (06A4894C)](#trigger-06a4894c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11091, Events line 11208, Actions line 11325.

<a id="trigger-06a49bcc"></a>

### 54. Audio_Zof_Siege Chop - 06A49BCC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06A49AEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 14 (global list position: Soviet War Factory (NAWEAP)). A map-local type-list change can affect index interpretation.
2. Building exists: type index 10 (global list position: Soviet Battle Lab (NATECH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaSiegeChopperIntro.
2. Enable and reset applicable timers for [Audio_Zof_Siege Flash (08D17B5C)](#trigger-08d17b5c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11092, Events line 11209, Actions line 11326.

<a id="trigger-08d17b5c"></a>

### 55. Audio_Zof_Siege Flash - 08D17B5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Zof_Siege Chop (06A49BCC)](#trigger-06a49bcc).

Attached scope: tag definitions 08D149DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Switch the sidebar to tab 3.
2. Flash cameo/type SCHP; additional configured duration/location argument 120.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11093, Events line 11210, Actions line 11327.

<a id="trigger-06a4951c"></a>

### 56. Audio_Zof_Iris - 06A4951C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 0 (Sub Pen Destroyed) is clear.
2. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Flag writers in this mission: set local flag 0 (Sub Pen Destroyed) at [Destroyed_Sub Pen (0ED70C8C)](#trigger-0ed70c8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaWhatIsIris.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11094, Events line 11211, Actions line 11328.

<a id="trigger-0ed70e5c"></a>

### 57. Discovered_Sub Pen - 0ED70E5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Discovered_Sub Pen (0ED70E5C)](#trigger-0ed70e5c).
2. Play voice notification Mis_xS5_YuriWarnsPlayer.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11095, Events line 11212, Actions line 11329.

<a id="trigger-0ed70c8c"></a>

### 58. Destroyed_Sub Pen - 0ED70C8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Discovered_Sub Pen (0ED70E5C)](#trigger-0ed70e5c).

Attached scope: Yuri Naval Yard (YAYARD), owner YuriCountry, cell (136, 149), tag 0ED70D7C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Destroyed_Sub Pen (0ED70C8C)](#trigger-0ed70c8c).
2. Disable [Detect_All Factory Dead (07A6B3FC)](#trigger-07a6b3fc).
3. Set local flag 0 (Sub Pen Destroyed).
4. Enable and reset applicable timers for [_Win Conditions_Ez/Med (08711D8C)](#trigger-08711d8c).
5. Enable and reset applicable timers for [_Win Conditions_ Hard (0871480C)](#trigger-0871480c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11096, Events line 11213, Actions line 11330.

<a id="trigger-07a6b3fc"></a>

### 59. Detect_All Factory Dead - 07A6B3FC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A6B31C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Fire Sale: owner selector 14 (country/type YURI2; placed owner Yuri2Country).
3. All to Hunt: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
4. All to Hunt: owner selector 14 (country/type YURI2; placed owner Yuri2Country).
5. Enable and reset applicable timers for [Detect_Yuri Land Dead (043AB6AC)](#trigger-043ab6ac).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11097, Events line 11214, Actions line 11331.

<a id="trigger-08711d8c"></a>

### 60. _Win Conditions_Ez/Med - 08711D8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_Sub Pen (0ED70C8C)](#trigger-0ed70c8c).

Attached scope: tag definitions 087101EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 8 (country/type RUSSIANS; placed owner Russians).
2. Enable and reset applicable timers for [Completed_Obj 2_Ez/Med (08713CBC)](#trigger-08713cbc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11098, Events line 11215, Actions line 11332.

<a id="trigger-0871480c"></a>

### 61. _Win Conditions_ Hard - 0871480C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyed_Sub Pen (0ED70C8C)](#trigger-0ed70c8c).

Attached scope: tag definitions 0871460C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Detect_Yuri Land Dead (043AB6AC)](#trigger-043ab6ac).
2. Enable and reset applicable timers for [Completed_Objective 2 (079B2F3C)](#trigger-079b2f3c).
3. Fire Sale: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
4. Fire Sale: owner selector 14 (country/type YURI2; placed owner Yuri2Country).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11099, Events line 11216, Actions line 11333.

<a id="trigger-043ab6ac"></a>

### 62. Detect_Yuri Land Dead - 043AB6AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_All Factory Dead (07A6B3FC)](#trigger-07a6b3fc); enable from [_Win Conditions_ Hard (0871480C)](#trigger-0871480c).

Attached scope: tag definitions 043AB5CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  Land: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Destroyed,  Units,  Land: owner selector 14 (country/type YURI2; placed owner Yuri2Country).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Completed_Objective 3 (079B2B9C)](#trigger-079b2b9c).
2. Disable [Repeat_Text_Obj 3 (079B561C)](#trigger-079b561c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11100, Events line 11217, Actions line 11334.

<a id="trigger-08713cbc"></a>

### 63. Completed_Obj 2_Ez/Med - 08713CBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Win Conditions_Ez/Med (08711D8C)](#trigger-08711d8c).

Attached scope: tag definitions 08713ABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2 Complete.” (MISSION:Obj2Comp).
2. Enable and reset applicable timers for [Disable_RepeatObj2EzMed (087110CC)](#trigger-087110cc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11101, Events line 11218, Actions line 11335.

<a id="trigger-079b2f3c"></a>

### 64. Completed_Objective 2 - 079B2F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Win Conditions_ Hard (0871480C)](#trigger-0871480c).

Attached scope: tag definitions 079B2E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2 Complete.” (MISSION:Obj2Comp).
2. Play voice notification EVA_ObjectiveComplete.
3. Enable and reset applicable timers for [Disable_Repeat Obj 2 (079B4F3C)](#trigger-079b4f3c).
4. Enable and reset applicable timers for [Text_Objective 3 (079AC1DC)](#trigger-079ac1dc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11102, Events line 11219, Actions line 11336.

<a id="trigger-079b2b9c"></a>

### 65. Completed_Objective 3 - 079B2B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Yuri Land Dead (043AB6AC)](#trigger-043ab6ac).

Attached scope: tag definitions 079B7D2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3 Complete.” (MISSION:Obj3Comp).
2. Play voice notification EVA_ObjectiveComplete.
3. Make side cheer: owner selector 8 (country/type RUSSIANS; placed owner Russians).
4. Enable and reset applicable timers for [SP2.1_Camera_To Iris (043AB44C)](#trigger-043ab44c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11103, Events line 11220, Actions line 11337.

<a id="trigger-079b561c"></a>

### 66. Repeat_Text_Obj 3 - 079B561C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Text_Objective 3 (079AC1DC)](#trigger-079ac1dc).

Attached scope: tag definitions 079B18EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Finish off all remaining Yuri land forces.” (MISSION:Sov5Obj3).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11104, Events line 11221, Actions line 11338.

<a id="trigger-087110cc"></a>

### 67. Disable_RepeatObj2EzMed - 087110CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Completed_Obj 2_Ez/Med (08713CBC)](#trigger-08713cbc).

Attached scope: tag definitions 08712B7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_YuriNoMoreFriends.
2. Enable and reset applicable timers for [SP2.0_Delay_To Iris (08711B7C)](#trigger-08711b7c).
3. Disable [Repeat_Text/Ping_Obj 2 (079B17FC)](#trigger-079b17fc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11105, Events line 11222, Actions line 11339.

<a id="trigger-079b4f3c"></a>

### 68. Disable_Repeat Obj 2 - 079B4F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Completed_Objective 2 (079B2F3C)](#trigger-079b2f3c).

Attached scope: tag definitions 079B4E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_YuriNoMoreFriends.
2. All to Hunt: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
3. All to Hunt: owner selector 14 (country/type YURI2; placed owner Yuri2Country).
4. Disable [Repeat_Text/Ping_Obj 2 (079B17FC)](#trigger-079b17fc).
5. Enable and reset applicable timers for [Text_Objective 3 (079AC1DC)](#trigger-079ac1dc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11106, Events line 11223, Actions line 11340.

<a id="trigger-079ac1dc"></a>

### 69. Text_Objective 3 - 079AC1DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Completed_Objective 2 (079B2F3C)](#trigger-079b2f3c); enable from [Disable_Repeat Obj 2 (079B4F3C)](#trigger-079b4f3c).

Attached scope: tag definitions 079AD4AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Finish off all remaining Yuri land forces.” (MISSION:Sov5Obj3).
2. Enable and reset applicable timers for [Repeat_Text_Obj 3 (079B561C)](#trigger-079b561c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11107, Events line 11224, Actions line 11341.

<a id="trigger-043ab44c"></a>

### 70. SP2.1_Camera_To Iris - 043AB44C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Completed_Objective 3 (079B2B9C)](#trigger-079b2b9c); enable from [SP2.0_Delay_To Iris (08711B7C)](#trigger-08711b7c).

Attached scope: tag definitions 043AB36C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 700 (cell 137, 136).
2. Make side cheer: owner selector 8 (country/type RUSSIANS; placed owner Russians).
3. Enable and reset applicable timers for [SP2.2_Movie_Zof RE Iris (043A42BC)](#trigger-043a42bc).
4. Reveal terrain around waypoint 700 (cell 137, 136).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11108, Events line 11225, Actions line 11342.

<a id="trigger-08711b7c"></a>

### 71. SP2.0_Delay_To Iris - 08711B7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Disable_RepeatObj2EzMed (087110CC)](#trigger-087110cc).

Attached scope: tag definitions 08710BDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [SP2.1_Camera_To Iris (043AB44C)](#trigger-043ab44c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11109, Events line 11226, Actions line 11343.

<a id="trigger-079b17fc"></a>

### 72. Repeat_Text/Ping_Obj 2 - 079B17FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Text/Ping_Objective 2 (079AD3BC)](#trigger-079ad3bc).

Attached scope: tag definitions 079B171C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Locate and destroy Yuri's Submarine Pen.” (MISSION:Sov5Obj2).
2. Create radar-event marker type 0 at waypoint 61 (cell 137, 150).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11110, Events line 11227, Actions line 11344.

<a id="trigger-043a42bc"></a>

### 73. SP2.2_Movie_Zof RE Iris - 043A42BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.1_Camera_To Iris (043AB44C)](#trigger-043ab44c).

Attached scope: tag definitions 043A41DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 50.
2. Enable and reset applicable timers for [_Winner (094429EC)](#trigger-094429ec).
3. Enable and reset applicable timers for [SP2.3_Iris Open (092E05BC)](#trigger-092e05bc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11111, Events line 11228, Actions line 11345.

<a id="trigger-094429ec"></a>

### 74. _Winner - 094429EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.2_Movie_Zof RE Iris (043A42BC)](#trigger-043a42bc).

Attached scope: tag definitions 0944290C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11112, Events line 11229, Actions line 11346.

<a id="trigger-092e05bc"></a>

### 75. SP2.3_Iris Open - 092E05BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SP2.2_Movie_Zof RE Iris (043A42BC)](#trigger-043a42bc).

Attached scope: tag definitions 092E04DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Lunching Pad On (0D40992C)](#trigger-0d40992c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11113, Events line 11230, Actions line 11347.

<a id="trigger-0ed7151c"></a>

### 76. Statues - 0ED7151C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Statue @ BU (0B6AF1FC)](#trigger-0b6af1fc); enable from [Statue @ BV (0B6AD5BC)](#trigger-0b6ad5bc); enable from [Statue @ BW (0B6AD78C)](#trigger-0b6ad78c); enable from [Statue @ BX (0B6AD95C)](#trigger-0b6ad95c); enable from [Statue @ BY (0B6AE2AC)](#trigger-0b6ae2ac); enable from [Statue @ BZ (0B6AE47C)](#trigger-0b6ae47c); enable from [Statue @ CA (0B6AE64C)](#trigger-0b6ae64c); enable from [Statue @ CB (0B6AE81C)](#trigger-0b6ae81c); enable from [Statue @ CC (0B6AE9EC)](#trigger-0b6ae9ec); enable from [Statue @ CD (0B6AE0DC)](#trigger-0b6ae0dc).

Attached scope: tag definitions 0ED7143C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaStrangeReadings.
2. Enable and reset applicable timers for [Statues_Enable (0ED72A8C)](#trigger-0ed72a8c).
3. Enable and reset applicable timers for [Audio_Zof_Iron Curtain2 (09701F3C)](#trigger-09701f3c).
4. Flash buildings of type CAEAST02; duration argument 160.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11114, Events line 11231, Actions line 11348.

<a id="trigger-0ed72a8c"></a>

### 77. Statues_Enable - 0ED72A8C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Statues (0ED7151C)](#trigger-0ed7151c).

Attached scope: tag definitions 0ED729AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Enable and reset applicable timers for [Audio_Statue Fired (0ED7111C)](#trigger-0ed7111c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11115, Events line 11232, Actions line 11349.

<a id="trigger-0ed7111c"></a>

### 78. Audio_Statue Fired - 0ED7111C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Statues_Enable (0ED72A8C)](#trigger-0ed72a8c).

Attached scope: tag definitions 0ED7103C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaEasterIsleWarning.
2. Enable and reset applicable timers for [Audio_Statue Engineer (0ED721BC)](#trigger-0ed721bc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11116, Events line 11233, Actions line 11350.

<a id="trigger-0ed721bc"></a>

### 79. Audio_Statue Engineer - 0ED721BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Audio_Statue Fired (0ED7111C)](#trigger-0ed7111c).

Attached scope: tag definitions 0ED722AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS5_ZofiaMaybeAnEngineer.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11117, Events line 11234, Actions line 11351.

<a id="trigger-0783450c"></a>

### 80. _Amb_Ocean Heavy 1 - 0783450C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0783442C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 34 (cell 139, 27).
2. Play sound _Amb_OceanHeavy at waypoint 39 (cell 123, 39).
3. Play sound _Amb_OceanHeavy at waypoint 40 (cell 106, 48).
4. Play sound _Amb_OceanHeavy at waypoint 41 (cell 93, 62).
5. Play sound _Amb_OceanHeavy at waypoint 42 (cell 76, 75).
6. Play sound _Amb_OceanHeavy at waypoint 43 (cell 64, 94).
7. Play sound _Amb_OceanHeavy at waypoint 44 (cell 53, 113).
8. Play sound _Amb_OceanHeavy at waypoint 45 (cell 36, 128).
9. Play sound _Amb_OceanHeavy at waypoint 46 (cell 47, 159).
10. Play sound _Amb_OceanHeavy at waypoint 47 (cell 65, 179).
11. Play sound _Amb_OceanHeavy at waypoint 59 (cell 181, 75).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11118, Events line 11235, Actions line 11352.

<a id="trigger-07848dec"></a>

### 81. _Amb_Bird Jungle 2c - 07848DEC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07848D0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsJungle2 at waypoint 66 (cell 113, 125).
2. Play sound _Amb_BirdsJungle2 at waypoint 158 (cell 128, 189).
3. Play sound _Amb_BirdsJungle2 at waypoint 139 (cell 79, 155).
4. Play sound _Amb_BirdsJungle2 at waypoint 130 (cell 107, 194).
5. Play sound _Amb_BirdsJungle2 at waypoint 529 (cell 66, 138).
6. Play sound _Amb_BirdsJungle2 at waypoint 530 (cell 74, 113).
7. Play sound _Amb_BirdsJungle2 at waypoint 531 (cell 115, 96).
8. Play sound _Amb_BirdsJungle2 at waypoint 132 (cell 83, 136).
9. Play sound _Amb_BirdsJungle2 at waypoint 136 (cell 197, 152).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11119, Events line 11236, Actions line 11353.

<a id="trigger-07848c1c"></a>

### 82. _Amb_Bird Jungle 2b - 07848C1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07848B3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsJungle2 at waypoint 520 (cell 198, 109).
2. Play sound _Amb_BirdsJungle2 at waypoint 521 (cell 210, 150).
3. Play sound _Amb_BirdsJungle2 at waypoint 522 (cell 223, 161).
4. Play sound _Amb_BirdsJungle2 at waypoint 523 (cell 169, 179).
5. Play sound _Amb_BirdsJungle2 at waypoint 524 (cell 105, 130).
6. Play sound _Amb_BirdsJungle2 at waypoint 525 (cell 92, 164).
7. Play sound _Amb_BirdsJungle2 at waypoint 526 (cell 106, 184).
8. Play sound _Amb_BirdsJungle2 at waypoint 527 (cell 94, 194).
9. Play sound _Amb_BirdsJungle2 at waypoint 528 (cell 68, 154).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11120, Events line 11237, Actions line 11354.

<a id="trigger-07848a4c"></a>

### 83. _Amb_Bird Jungle 2a - 07848A4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0784896C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsJungle2 at waypoint 148 (cell 157, 69).
2. Play sound _Amb_BirdsJungle2 at waypoint 149 (cell 141, 58).
3. Play sound _Amb_BirdsJungle2 at waypoint 150 (cell 144, 70).
4. Play sound _Amb_BirdsJungle2 at waypoint 517 (cell 127, 59).
5. Play sound _Amb_BirdsJungle2 at waypoint 518 (cell 97, 93).
6. Play sound _Amb_BirdsJungle2 at waypoint 519 (cell 142, 77).
7. Play sound _Amb_BirdsJungle2 at waypoint 143 (cell 200, 125).
8. Play sound _Amb_BirdsJungle2 at waypoint 180 (cell 172, 115).
9. Play sound _Amb_BirdsJungle2 at waypoint 153 (cell 119, 104).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11121, Events line 11238, Actions line 11355.

<a id="trigger-0784887c"></a>

### 84. _Amb_Wind Plains 2 - 0784887C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0784879C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindPlains at waypoint 36 (cell 115, 66).
2. Play sound _Amb_WindPlains at waypoint 35 (cell 49, 138).
3. Play sound _Amb_WindPlains at waypoint 158 (cell 128, 189).
4. Play sound _Amb_WindPlains at waypoint 159 (cell 98, 151).
5. Play sound _Amb_WindPlains at waypoint 66 (cell 113, 125).
6. Play sound _Amb_WindPlains at waypoint 65 (cell 159, 126).
7. Play sound _Amb_WindPlains at waypoint 157 (cell 172, 128).
8. Play sound _Amb_WindPlains at waypoint 37 (cell 214, 122).
9. Play sound _Amb_WindPlains at waypoint 146 (cell 138, 90).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11122, Events line 11239, Actions line 11356.

<a id="trigger-078486ac"></a>

### 85. _Amb_Wind Plains 1 - 078486AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078485CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindPlains at waypoint 507 (cell 127, 70).
2. Play sound _Amb_WindPlains at waypoint 508 (cell 104, 80).
3. Play sound _Amb_WindPlains at waypoint 509 (cell 222, 138).
4. Play sound _Amb_WindPlains at waypoint 510 (cell 224, 153).
5. Play sound _Amb_WindPlains at waypoint 511 (cell 201, 182).
6. Play sound _Amb_WindPlains at waypoint 512 (cell 97, 131).
7. Play sound _Amb_WindPlains at waypoint 513 (cell 58, 150).
8. Play sound _Amb_WindPlains at waypoint 514 (cell 71, 164).
9. Play sound _Amb_WindPlains at waypoint 515 (cell 84, 189).
10. Play sound _Amb_WindPlains at waypoint 516 (cell 106, 204).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11123, Events line 11240, Actions line 11357.

<a id="trigger-078484dc"></a>

### 86. _Amb_Ocean Light 2 - 078484DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078483FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 501 (cell 107, 137).
2. Play sound _Amb_OceanLight at waypoint 502 (cell 117, 135).
3. Play sound _Amb_OceanLight at waypoint 503 (cell 165, 157).
4. Play sound _Amb_OceanLight at waypoint 504 (cell 157, 149).
5. Play sound _Amb_OceanLight at waypoint 505 (cell 169, 144).
6. Play sound _Amb_OceanLight at waypoint 506 (cell 157, 136).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11124, Events line 11241, Actions line 11358.

<a id="trigger-0784830c"></a>

### 87. _Amb_Ocean Light 1 - 0784830C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0784822C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 494 (cell 140, 169).
2. Play sound _Amb_OceanLight at waypoint 495 (cell 137, 155).
3. Play sound _Amb_OceanLight at waypoint 496 (cell 155, 166).
4. Play sound _Amb_OceanLight at waypoint 497 (cell 127, 169).
5. Play sound _Amb_OceanLight at waypoint 498 (cell 121, 154).
6. Play sound _Amb_OceanLight at waypoint 499 (cell 112, 166).
7. Play sound _Amb_OceanLight at waypoint 500 (cell 108, 150).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11125, Events line 11242, Actions line 11359.

<a id="trigger-0784813c"></a>

### 88. _Amb_Ocean Heavy 2 - 0784813C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0784805C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 48 (cell 84, 204).
2. Play sound _Amb_OceanHeavy at waypoint 49 (cell 108, 223).
3. Play sound _Amb_OceanHeavy at waypoint 50 (cell 134, 224).
4. Play sound _Amb_OceanHeavy at waypoint 51 (cell 152, 199).
5. Play sound _Amb_OceanHeavy at waypoint 52 (cell 182, 205).
6. Play sound _Amb_OceanHeavy at waypoint 53 (cell 205, 200).
7. Play sound _Amb_OceanHeavy at waypoint 54 (cell 221, 182).
8. Play sound _Amb_OceanHeavy at waypoint 55 (cell 237, 165).
9. Play sound _Amb_OceanHeavy at waypoint 56 (cell 253, 145).
10. Play sound _Amb_OceanHeavy at waypoint 57 (cell 231, 121).
11. Play sound _Amb_OceanHeavy at waypoint 58 (cell 204, 97).
12. Play sound _Amb_OceanHeavy at waypoint 60 (cell 162, 48).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11126, Events line 11243, Actions line 11360.

<a id="trigger-0ba3e3cc"></a>

### 89. No Audio_Pen Dead - 0BA3E3CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Audio_Zof_Iris (06A4951C)](#trigger-06a4951c).

Attached scope: 40 tagged map cells: (132, 131), (133, 131), (134, 131), (135, 131), (136, 131), (137, 131), (138, 131), (139, 131), (140, 131), (141, 131), (142, 131), (132, 132), (142, 132), (132, 133), (142, 133), (132, 134), (142, 134), (132, 135), (142, 135), (132, 136), (142, 136), (132, 137), (142, 137), (132, 138), (142, 138), (132, 139), (142, 139), (132, 140), (142, 140), (132, 141), (133, 141), (134, 141), (135, 141), (136, 141), (137, 141), (138, 141), (139, 141), (140, 141), (141, 141), (142, 141); tag 06A4934C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 0 (Sub Pen Destroyed) is set.
2. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Flag writers in this mission: set local flag 0 (Sub Pen Destroyed) at [Destroyed_Sub Pen (0ED70C8C)](#trigger-0ed70c8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Perform no action.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11127, Events line 11244, Actions line 11361.

<a id="trigger-04403d3c"></a>

### 90. _Setup_Sov05_9 - 04403D3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04403C5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [TM_Yuri_Bio Stuffer @ FO (0442383C)](sov05umd-teams.md#team-0442383c).
2. Create/recruit team [TM_Yuri_Bio Stuffer @ FO (0442383C)](sov05umd-teams.md#team-0442383c).
3. Create/recruit team [TM_Yuri_Bio Stuffer @ FO (0442383C)](sov05umd-teams.md#team-0442383c).
4. Create/recruit team [TM_Yuri_Bio Stuffer @ FP (04424E1C)](sov05umd-teams.md#team-04424e1c).
5. Create/recruit team [TM_Yuri_Bio Stuffer @ FP (04424E1C)](sov05umd-teams.md#team-04424e1c).
6. Create/recruit team [TM_Yuri_Bio Stuffer @ FP (04424E1C)](sov05umd-teams.md#team-04424e1c).
7. Create/recruit team [TM_Yuri_Bio Stuffer @ FP (04424E1C)](sov05umd-teams.md#team-04424e1c).
8. Create/recruit team [TM_Yuri_Bio Stuffer @ FP (04424E1C)](sov05umd-teams.md#team-04424e1c).
9. Create/recruit team [TM_Yuri2_Bio Stuffer @ TL (096DBC9C)](sov05umd-teams.md#team-096dbc9c).
10. Create/recruit team [TM_Yuri2_Bio Stuffer @ TL (096DBC9C)](sov05umd-teams.md#team-096dbc9c).
11. Enable and reset applicable timers for [_Setup_Sov05_10 (087D92FC)](#trigger-087d92fc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11128, Events line 11245, Actions line 11362.

<a id="trigger-087d92fc"></a>

### 91. _Setup_Sov05_10 - 087D92FC

Owner reference: Yuri2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Setup_Sov05_9 (04403D3C)](#trigger-04403d3c).

Attached scope: tag definitions 087D9ADC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type YURI2; placed owner Yuri2Country).
2. AI triggers begin: owner selector 14 (country/type YURI2; placed owner Yuri2Country).
3. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).
4. Create/recruit team [TM_Yuri2_2 Slave Miner (0954BBFC)](sov05umd-teams.md#team-0954bbfc).
5. Create/recruit team [TM_Yuri_2 Slave Miner (077BCBFC)](sov05umd-teams.md#team-077bcbfc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11129, Events line 11246, Actions line 11363.

<a id="trigger-04404dbc"></a>

### 92. _Setup_Sov05_8 - 04404DBC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 044036EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [TM_Yuri_Bio Stuffer @ EV (044234AC)](sov05umd-teams.md#team-044234ac).
2. Create/recruit team [TM_Yuri_Bio Stuffer @ EX (0442337C)](sov05umd-teams.md#team-0442337c).
3. Create/recruit team [TM_Yuri_Bio Stuffer @ EX (0442337C)](sov05umd-teams.md#team-0442337c).
4. Create/recruit team [TM_Yuri_Bio Stuffer @ FK (044235DC)](sov05umd-teams.md#team-044235dc).
5. Create/recruit team [TM_Yuri_Bio Stuffer @ FM (0442370C)](sov05umd-teams.md#team-0442370c).
6. Create/recruit team [TM_Yuri_Bio Stuffer @ FN (0441A14C)](sov05umd-teams.md#team-0441a14c).
7. Create/recruit team [TM_Yuri_Bio Stuffer @ FN (0441A14C)](sov05umd-teams.md#team-0441a14c).
8. Create/recruit team [TM_Yuri_Bio Stuffer @ FN (0441A14C)](sov05umd-teams.md#team-0441a14c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11130, Events line 11247, Actions line 11364.

<a id="trigger-079ad3bc"></a>

### 93. Text/Ping_Objective 2 - 079AD3BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Completed_Objective 1 (079B2D6C)](#trigger-079b2d6c).

Attached scope: tag definitions 079AD2DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Locate and destroy Yuri's Submarine Pen.” (MISSION:Sov5Obj2).
2. Create radar-event marker type 0 at waypoint 61 (cell 137, 150).
3. Enable and reset applicable timers for [Repeat_Text/Ping_Obj 2 (079B17FC)](#trigger-079b17fc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11131, Events line 11248, Actions line 11365.

<a id="trigger-079b36ec"></a>

### 94. Disable_Repeat Obj 1 - 079B36EC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079B360C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Disable [Repeat_Text/Ping_Obj 1 (079B57EC)](#trigger-079b57ec).
2. Enable and reset applicable timers for [Completed_Objective 1 (079B2D6C)](#trigger-079b2d6c).
3. Disable [Reinforce_MCV (Easy) (0441CC8C)](#trigger-0441cc8c).
4. Disable [Reinforce_MCV (Med) (0441CE5C)](#trigger-0441ce5c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11132, Events line 11249, Actions line 11366.

<a id="trigger-079b2d6c"></a>

### 95. Completed_Objective 1 - 079B2D6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Disable_Repeat Obj 1 (079B36EC)](#trigger-079b36ec).

Attached scope: tag definitions 079B2C8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ObjectiveComplete.
2. Display message “Objective 1 Complete.” (MISSION:Obj1Comp).
3. Enable and reset applicable timers for [Text/Ping_Objective 2 (079AD3BC)](#trigger-079ad3bc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11133, Events line 11250, Actions line 11367.

<a id="trigger-0441cc8c"></a>

### 96. Reinforce_MCV (Easy) - 0441CC8C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_MCV Trans Dead (0441D09C)](#trigger-0441d09c).

Attached scope: tag definitions 087D4C6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.
2. No instances of Soviet Construction Vehicle (SMCV) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_1 Trans_1 MCV (Easy2) (095D70DC)](sov05umd-teams.md#team-095d70dc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11134, Events line 11251, Actions line 11368.

<a id="trigger-0441ce5c"></a>

### 97. Reinforce_MCV (Med) - 0441CE5C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_MCV Trans Dead (0441D09C)](#trigger-0441d09c).

Attached scope: tag definitions 087D4D4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.
2. No instances of Soviet Construction Vehicle (SMCV) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_1 Trans_1 MCV (Med2) (0441C3BC)](sov05umd-teams.md#team-0441c3bc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11135, Events line 11252, Actions line 11369.

<a id="trigger-079b75fc"></a>

### 98. Disable_Repeat Obj 3 - 079B75FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079B751C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

No event entries. Reachability requires separate runtime interpretation.

**Then perform these actions in order:**

No action entries.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11136, Events line 11253, Actions line 11370.

<a id="trigger-05d37eac"></a>

### 99. Text_Lab Acquired - 05D37EAC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Disable [Text_Lab Acquired (05D37EAC)](#trigger-05d37eac).
2. Display message “Secret Laboratory Acquired!” (MISSION:SecrtLab).
3. Play voice notification EVA_SecretLabCaptured.
4. Enable and reset applicable timers for [Text_Tech Acquired (05D37CDC)](#trigger-05d37cdc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11137, Events line 11254, Actions line 11371.

<a id="trigger-05d37cdc"></a>

### 100. Text_Tech Acquired - 05D37CDC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Text_Lab Acquired (05D37EAC)](#trigger-05d37eac).

Incoming activation links: enable from [Text_Lab Acquired (05D37EAC)](#trigger-05d37eac).

Attached scope: Tech Secret Lab (CASLAB), owner YuriCountry, cell (124, 103), tag 05D37DCC, persistence mode 2.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Text_Tech Acquired (05D37CDC)](#trigger-05d37cdc).
2. Switch the sidebar to tab 2.
3. Flash cameo/type DESO; additional configured duration/location argument 120.
4. Display message “Secret Technology Acquired!” (MISSION:ScrtTech).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11138, Events line 11255, Actions line 11372.

<a id="trigger-0441d09c"></a>

### 101. Detect_MCV Trans Dead - 0441D09C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0441CF4C (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Reinforce_MCV (Easy) (0441CC8C)](#trigger-0441cc8c).
2. Enable and reset applicable timers for [Reinforce_MCV (Med) (0441CE5C)](#trigger-0441ce5c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11139, Events line 11256, Actions line 11373.

<a id="trigger-0441bafc"></a>

### 102. Announce_MCV Trans @ AI - 0441BAFC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0441BA1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (MCV @ AI) is set.

Flag writers in this mission: clear local flag 1 (MCV @ AI) at [Announce_MCV Trans @ AI (0441BAFC)](#trigger-0441bafc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 1 (MCV @ AI).
2. Create radar-event marker type 2 at waypoint 34 (cell 139, 27).
3. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11140, Events line 11257, Actions line 11374.

<a id="trigger-09303f3c"></a>

### 103. Detect_MCV Easy2 Dead - 09303F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09303E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Reinforce_MCV Easy3 (0930275C)](#trigger-0930275c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11141, Events line 11258, Actions line 11375.

<a id="trigger-0930275c"></a>

### 104. Reinforce_MCV Easy3 - 0930275C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_MCV Easy2 Dead (09303F3C)](#trigger-09303f3c).

Attached scope: tag definitions 0930267C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Soviet Construction Vehicle (SMCV) exist on the map, under this event's ownership scope.
2. Building does not exist: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Sov_1 Trans_1 MCV (Easy3) (0930734C)](sov05umd-teams.md#team-0930734c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11142, Events line 11259, Actions line 11376.

<a id="trigger-0b6af1fc"></a>

### 105. Statue @ BU - 0B6AF1FC

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (87, 142), tag 0B6AF11C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 72 (cell 88, 142).
2. Reveal terrain around waypoint 72 (cell 88, 142).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11143, Events line 11260, Actions line 11377.

<a id="trigger-0b6adb2c"></a>

### 106. Statue_Shutdown - 0B6ADB2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Statue @ BU (0B6AF1FC)](#trigger-0b6af1fc); enable from [Statue @ BV (0B6AD5BC)](#trigger-0b6ad5bc); enable from [Statue @ BW (0B6AD78C)](#trigger-0b6ad78c); enable from [Statue @ BX (0B6AD95C)](#trigger-0b6ad95c); enable from [Statue @ BY (0B6AE2AC)](#trigger-0b6ae2ac); enable from [Statue @ BZ (0B6AE47C)](#trigger-0b6ae47c); enable from [Statue @ CA (0B6AE64C)](#trigger-0b6ae64c); enable from [Statue @ CB (0B6AE81C)](#trigger-0b6ae81c); enable from [Statue @ CC (0B6AE9EC)](#trigger-0b6ae9ec); enable from [Statue @ CD (0B6AE0DC)](#trigger-0b6ae0dc).

Attached scope: tag definitions 0B6ADA4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Statue @ BU (0B6AF1FC)](#trigger-0b6af1fc).
2. Disable [Statue @ BV (0B6AD5BC)](#trigger-0b6ad5bc).
3. Disable [Statue @ BW (0B6AD78C)](#trigger-0b6ad78c).
4. Disable [Statue @ BX (0B6AD95C)](#trigger-0b6ad95c).
5. Disable [Statue @ BY (0B6AE2AC)](#trigger-0b6ae2ac).
6. Disable [Statue @ BZ (0B6AE47C)](#trigger-0b6ae47c).
7. Disable [Statue @ CA (0B6AE64C)](#trigger-0b6ae64c).
8. Disable [Statue @ CB (0B6AE81C)](#trigger-0b6ae81c).
9. Disable [Statue @ CC (0B6AE9EC)](#trigger-0b6ae9ec).
10. Disable [Statue @ CD (0B6AE0DC)](#trigger-0b6ae0dc).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11144, Events line 11261, Actions line 11378.

<a id="trigger-0b6ad5bc"></a>

### 107. Statue @ BV - 0B6AD5BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (95, 98), tag 0B6AD4DC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 73 (cell 96, 98).
2. Reveal terrain around waypoint 73 (cell 96, 98).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11145, Events line 11262, Actions line 11379.

<a id="trigger-0b6ad78c"></a>

### 108. Statue @ BW - 0B6AD78C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (130, 102), tag 0B6AD6AC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 74 (cell 131, 102).
2. Reveal terrain around waypoint 74 (cell 131, 102).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11146, Events line 11263, Actions line 11380.

<a id="trigger-0b6ad95c"></a>

### 109. Statue @ BX - 0B6AD95C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (132, 118), tag 0B6AD87C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 75 (cell 133, 119).
2. Reveal terrain around waypoint 75 (cell 133, 119).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11147, Events line 11264, Actions line 11381.

<a id="trigger-0b6ae2ac"></a>

### 110. Statue @ BY - 0B6AE2AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (161, 97), tag 0B6AE1CC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 76 (cell 162, 97).
2. Reveal terrain around waypoint 76 (cell 162, 97).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11148, Events line 11265, Actions line 11382.

<a id="trigger-0b6ae47c"></a>

### 111. Statue @ BZ - 0B6AE47C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (163, 122), tag 0B6AE39C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 77 (cell 163, 123).
2. Reveal terrain around waypoint 77 (cell 163, 123).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11149, Events line 11266, Actions line 11383.

<a id="trigger-0b6ae64c"></a>

### 112. Statue @ CA - 0B6AE64C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (184, 147), tag 0B6AE56C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 78 (cell 184, 148).
2. Reveal terrain around waypoint 78 (cell 184, 148).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11150, Events line 11267, Actions line 11384.

<a id="trigger-0b6ae81c"></a>

### 113. Statue @ CB - 0B6AE81C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (170, 190), tag 0B6AE73C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 79 (cell 170, 191).
2. Reveal terrain around waypoint 79 (cell 170, 191).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11151, Events line 11268, Actions line 11385.

<a id="trigger-0b6ae9ec"></a>

### 114. Statue @ CC - 0B6AE9EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (127, 198), tag 0B6AE90C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 80 (cell 128, 198).
2. Reveal terrain around waypoint 80 (cell 128, 198).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11152, Events line 11269, Actions line 11386.

<a id="trigger-0b6ae0dc"></a>

### 115. Statue @ CD - 0B6AE0DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Statue (CAEAST02), owner Arabs, cell (69, 149), tag 0B6AAF4C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 81 (cell 69, 150).
2. Reveal terrain around waypoint 81 (cell 69, 150).
3. Enable and reset applicable timers for [Statues (0ED7151C)](#trigger-0ed7151c).
4. Enable and reset applicable timers for [Statue_Shutdown (0B6ADB2C)](#trigger-0b6adb2c).

Source locator: mapsmd03.mix/sov05umd.map; Triggers line 11153, Events line 11270, Actions line 11387.

[All team rosters and ordered plans](sov05umd-teams.md) | [All mission overrides](sov05umd-overrides.md)
