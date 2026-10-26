# Operation: Clones Down Under

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for all05umd.map.](../../images/map-all05umd.svg)

*Initial placement schematic for all05umd.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** all05umd.map. **Effective extracted member:** mapsmd03.mix/all05umd.map. **Trigger definitions:** 108.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all05umd-teams.md) | [All mission overrides](all05umd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | URBAN |
| Map size | 0,0,70,120 |
| Visible local rectangle | 5,5,60,109 |
| Placed vehicles | 59 |
| Placed infantry | 43 |
| Placed structures | 180 |
| Placed aircraft | 0 |
| Team templates | 125 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 400 | BadGuy1 |
| 2 | BadGuy2 House | 400 | BadGuy2 |
| 3 | German1 House | 0 | Germany1 |
| 4 | Civilian House | 0 | Neutral |
| 5 | Einstein House | 0 | Einstein |
| 6 | BadGuy3 House | 400 | BadGuy3 |
| 7 | German2 House | 0 | Germany2 |
| 8 | German3 House | 0 | Germany3 |
| 9 | Temp House | 0 | Temp |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Black Eagle 1,0 |
| 1 | Black Eagle 2,0 |
| 2 | Black Eagle 3,0 |
| 3 | Garrison Time,0 |
| 4 | Building 1 Fallen,0 |
| 5 | Building 2 Fallen,0 |
| 6 | Building 3 Fallen,0 |
| 7 | Building 4 Fallen,0 |
| 8 | Building 5 Fallen,0 |
| 9 | Building 6 Fallen,0 |
| 10 | Building 7 Fallen,0 |
| 11 | Building 8 Fallen,0 |
| 12 | BadGuy1 Dead,0 |
| 13 | BadGuy2 Dead,0 |
| 14 | Virus Dropped Off,0 |
| 15 | Boomers There?,0 |
| 16 | Chaos Revealed?,0 |
| 17 | Obj 1 Complete,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [It's Over : ( (068969FC)](#trigger-068969fc) | Destroyed,  Buildings,  All: owner selector 15 (country/type PLAYER; placed owner Player House). | Declare owner selector 15 (country/type PLAYER; placed owner Player House) the loser. |
| [Player Wins (093759FC)](#trigger-093759fc) | local flag 12 (BadGuy1 Dead) is set.<br>local flag 13 (BadGuy2 Dead) is set. | Declare owner selector 15 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-0e6bc74c"></a>

### 1. __Welcome - 0E6BC74C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E6BFBCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable player input.
2. Switch the sidebar to tab 0.
3. Play voice notification EVA_EstablishBattlefieldControl.
4. Play in-game movie 20.
5. Enable and reset applicable timers for [__Welcome 2 (0E6BFADC)](#trigger-0e6bfadc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8745, Events line 8855, Actions line 8965.

<a id="trigger-0e6bfadc"></a>

### 2. __Welcome 2 - 0E6BFADC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [__Welcome (0E6BC74C)](#trigger-0e6bc74c).

Attached scope: tag definitions 0E6BF89C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 93 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Supply reinforcement team [_A05_Initiate Rush 1 (08F84DEC)](all05umd-teams.md#team-08f84dec).
3. Supply reinforcement team [_A05_Initiate Rush 2 (08F8493C)](all05umd-teams.md#team-08f8493c).
4. Supply reinforcement team [_A05_Initiate Rush 3 (08F8459C)](all05umd-teams.md#team-08f8459c).
5. Supply reinforcement team [_A05_Yuri Base Defense 1 (093A0BCC)](all05umd-teams.md#team-093a0bcc).
6. Supply reinforcement team [_A05_Yuri Base Defense 2 (093A4A8C)](all05umd-teams.md#team-093a4a8c).
7. Supply reinforcement team [_A05_Yuri Base 2 Defense 1 (08640C8C)](all05umd-teams.md#team-08640c8c).
8. Supply reinforcement team [_A05_Yuri Base 2 Defense 2 (0B85E94C)](all05umd-teams.md#team-0b85e94c).
9. Play voice notification EVA_BattlefieldControlOnline.
10. Enable and reset applicable timers for [Hard Initiate Rush (069AC0AC)](#trigger-069ac0ac).
11. Enable and reset applicable timers for [Med Initiate Rush (069AC6EC)](#trigger-069ac6ec).
12. Create/recruit team [_A05_DEMO PLAYER MOVE (08AF81DC)](all05umd-teams.md#team-08af81dc).
13. Enable and reset applicable timers for [Intro Chaos Drone (08BB40FC)](#trigger-08bb40fc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8746, Events line 8856, Actions line 8966.

<a id="trigger-069ac0ac"></a>

### 3. Hard Initiate Rush - 069AC0AC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [__Welcome 2 (0E6BFADC)](#trigger-0e6bfadc).

Attached scope: tag definitions 069ADDEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Initiate Rush 6 (069B49AC)](all05umd-teams.md#team-069b49ac).
2. Supply reinforcement team [_A05_Initiate Rush 7 (069B419C)](all05umd-teams.md#team-069b419c).
3. Supply reinforcement team [_A05_Initiate Rush 8 (069B6C8C)](all05umd-teams.md#team-069b6c8c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8747, Events line 8857, Actions line 8967.

<a id="trigger-069ac6ec"></a>

### 4. Med Initiate Rush - 069AC6EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [__Welcome 2 (0E6BFADC)](#trigger-0e6bfadc).

Attached scope: tag definitions 069AC19C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Initiate Rush 4 (069ADCBC)](all05umd-teams.md#team-069adcbc).
2. Supply reinforcement team [_A05_Initiate Rush 5 (069B216C)](all05umd-teams.md#team-069b216c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8748, Events line 8858, Actions line 8968.

<a id="trigger-08bb40fc"></a>

### 5. Intro Chaos Drone - 08BB40FC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [__Welcome 2 (0E6BFADC)](#trigger-0e6bfadc).

Attached scope: tag definitions 08BB798C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Intro Chaos Drone (0B6D57DC)](all05umd-teams.md#team-0b6d57dc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8749, Events line 8859, Actions line 8969.

<a id="trigger-0e6bf7ac"></a>

### 6. Subs Are Coming - 0E6BF7AC

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Boomer Creation Part 1 (092A219C)](#trigger-092a219c).

Attached scope: tag definitions 0E6BF56C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 22.
2. Display message “WARNING - Yuri is sending Boomer subs our way! Prepare for confrontation!” (MISSION:BoomerAttack).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8750, Events line 8860, Actions line 8970.

<a id="trigger-092a219c"></a>

### 7. Boomer Creation Part 1 - 092A219C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 092A6E8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Boomer Team 1 (08AE9CBC)](all05umd-teams.md#team-08ae9cbc).
2. Enable and reset applicable timers for [Boomer Creation Part 2 (09262BAC)](#trigger-09262bac).
3. Enable and reset applicable timers for [Subs Are Coming (0E6BF7AC)](#trigger-0e6bf7ac).
4. AI triggers stop: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).
5. AI triggers stop: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8751, Events line 8861, Actions line 8971.

<a id="trigger-09262bac"></a>

### 8. Boomer Creation Part 2 - 09262BAC

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Boomer Creation Part 1 (092A219C)](#trigger-092a219c).

Attached scope: tag definitions 0926262C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Boomer Team 2 (08DC8CBC)](all05umd-teams.md#team-08dc8cbc).
2. Enable and reset applicable timers for [Boomer Creation Part 3 (0926253C)](#trigger-0926253c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8752, Events line 8862, Actions line 8972.

<a id="trigger-0926253c"></a>

### 9. Boomer Creation Part 3 - 0926253C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Boomer Creation Part 2 (09262BAC)](#trigger-09262bac).

Attached scope: tag definitions 0926224C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 75 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Boomer Team 3 (08DC891C)](all05umd-teams.md#team-08dc891c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8753, Events line 8863, Actions line 8973.

<a id="trigger-0689427c"></a>

### 10. It's Over Part 1 - 0689427C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06896AEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Set local flag 12 (BadGuy1 Dead).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8754, Events line 8864, Actions line 8974.

<a id="trigger-068969fc"></a>

### 11. It's Over : ( - 068969FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06895D0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 15 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Declare owner selector 15 (country/type PLAYER; placed owner Player House) the loser.

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8755, Events line 8865, Actions line 8975.

<a id="trigger-0e10896c"></a>

### 12. Boomer Placement Easy - 0E10896C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E10835C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_1 Yuri Boomer P (092D206C)](all05umd-teams.md#team-092d206c).
2. Supply reinforcement team [_A05_1 Yuri Boomer Q (092D3D2C)](all05umd-teams.md#team-092d3d2c).
3. Supply reinforcement team [_A05_1 Yuri Boomer R (092D39BC)](all05umd-teams.md#team-092d39bc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8756, Events line 8866, Actions line 8976.

<a id="trigger-0e109e5c"></a>

### 13. Boomer Placement Medium - 0E109E5C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E1099EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_1 Yuri Boomer M (0C1541FC)](all05umd-teams.md#team-0c1541fc).
2. Supply reinforcement team [_A05_1 Yuri Boomer N (092D22CC)](all05umd-teams.md#team-092d22cc).
3. Supply reinforcement team [_A05_1 Yuri Boomer O (092D219C)](all05umd-teams.md#team-092d219c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8757, Events line 8867, Actions line 8977.

<a id="trigger-0e10986c"></a>

### 14. Boomer Placement Hard - 0E10986C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E10940C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_1 Yuri Boomer S (092D376C)](all05umd-teams.md#team-092d376c).
2. Supply reinforcement team [_A05_1 Yuri Boomer T (092D363C)](all05umd-teams.md#team-092d363c).
3. Supply reinforcement team [_A05_1 Yuri Boomer U (092D350C)](all05umd-teams.md#team-092d350c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8758, Events line 8868, Actions line 8978.

<a id="trigger-068397dc"></a>

### 15. Replace Harriers - 068397DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0683CDDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  Naval: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Set Tech Level (Techno)[Level]; main setting ORCA; location/duration field 11.
2. Set Tech Level (Techno)[Level]; main setting BEAG; location/duration field 3.
3. Enable and reset applicable timers for [Black Eagle Attack (0E5CDB7C)](#trigger-0e5cdb7c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8759, Events line 8869, Actions line 8979.

<a id="trigger-0e5cdb7c"></a>

### 16. Black Eagle Attack - 0E5CDB7C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Replace Harriers (068397DC)](#trigger-068397dc); enable from [Black Eagle Initiate (0E5FA1BC)](#trigger-0e5fa1bc).

Attached scope: tag definitions 0E5CD72C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 21 (cell 121, 85).
2. Reveal terrain around waypoint 24 (cell 118, 92).
3. Reveal terrain around waypoint 25 (cell 130, 89).
4. Jump the camera to waypoint 21 (cell 121, 85).
5. Enable and reset applicable timers for [Stop Control! (0893A37C)](#trigger-0893a37c).
6. Supply reinforcement team [_A05_Black Eagle 2 (0E5A071C)](all05umd-teams.md#team-0e5a071c).
7. Supply reinforcement team [_A05_Black Eagle 1 (0E5A5B8C)](all05umd-teams.md#team-0e5a5b8c).
8. Supply reinforcement team [_A05_Black Eagle 3 (0E5A40BC)](all05umd-teams.md#team-0e5a40bc).
9. Supply reinforcement team [_A05_Black Eagle 4 (0E5A5EFC)](all05umd-teams.md#team-0e5a5efc).
10. Enable and reset applicable timers for [Flash Black Eagles (097EFF3C)](#trigger-097eff3c).
11. Enable and reset applicable timers for [Introduce Virus (092A4DEC)](#trigger-092a4dec).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8760, Events line 8870, Actions line 8980.

<a id="trigger-0893a37c"></a>

### 17. Stop Control! - 0893A37C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Black Eagle Attack (0E5CDB7C)](#trigger-0e5cdb7c).

Attached scope: tag definitions 08932B4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable player input.
2. Enable and reset applicable timers for [Stop Control! Return (08947F3C)](#trigger-08947f3c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8761, Events line 8871, Actions line 8981.

<a id="trigger-097eff3c"></a>

### 18. Flash Black Eagles - 097EFF3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Black Eagle Attack (0E5CDB7C)](#trigger-0e5cdb7c).

Attached scope: tag definitions 097EFB4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Switch the sidebar to tab 3.
2. Flash cameo/type BEAG; additional configured duration/location argument 60.
3. Enable and reset applicable timers for [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8762, Events line 8872, Actions line 8982.

<a id="trigger-092a4dec"></a>

### 19. Introduce Virus - 092A4DEC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Black Eagle Attack (0E5CDB7C)](#trigger-0e5cdb7c).

Attached scope: tag definitions 092B1CFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Hover Virus (0C7AD1CC)](all05umd-teams.md#team-0c7ad1cc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8763, Events line 8873, Actions line 8983.

<a id="trigger-08947f3c"></a>

### 20. Stop Control! Return - 08947F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Stop Control! (0893A37C)](#trigger-0893a37c).

Attached scope: tag definitions 08947C8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8764, Events line 8874, Actions line 8984.

<a id="trigger-0cc7e49c"></a>

### 21. *Garrison Time Start! - 0CC7E49C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Flash Black Eagles (097EFF3C)](#trigger-097eff3c).

Attached scope: tag definitions 0CC7F7BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 85 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [*Garrison Time 1 (0692E3AC)](#trigger-0692e3ac).
2. Enable and reset applicable timers for [*Garrison Time 2 (0CC78D8C)](#trigger-0cc78d8c).
3. Play voice notification Mis_xA5_EvaGarrison.
4. Enable and reset applicable timers for [*Garrison Time 3 (0CC6F07C)](#trigger-0cc6f07c).
5. Enable and reset applicable timers for [*Garrison Time 4 (0DCC216C)](#trigger-0dcc216c).
6. Enable and reset applicable timers for [*Garrison Time 5 (0DCC636C)](#trigger-0dcc636c).
7. Enable and reset applicable timers for [*Garrison Time 6 (0DCD607C)](#trigger-0dcd607c).
8. Enable and reset applicable timers for [*Garrison Time 7 (0DCD938C)](#trigger-0dcd938c).
9. Enable and reset applicable timers for [*Garrison Time 8 (0DCDF99C)](#trigger-0dcdf99c).
10. Enable and reset applicable timers for [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8765, Events line 8875, Actions line 8985.

<a id="trigger-0692e3ac"></a>

### 22. *Garrison Time 1 - 0692E3AC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Attached scope: tag definitions 06936DFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (Building 1 Fallen) is clear.

Flag writers in this mission: set local flag 4 (Building 1 Fallen) at [Building 1 Stands (0CC7C45C)](#trigger-0cc7c45c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Garrison Team 1 (08BBDB7C)](all05umd-teams.md#team-08bbdb7c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8766, Events line 8876, Actions line 8986.

<a id="trigger-0cc78d8c"></a>

### 23. *Garrison Time 2 - 0CC78D8C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Attached scope: tag definitions 0CC7C23C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (Building 2 Fallen) is clear.

Flag writers in this mission: set local flag 5 (Building 2 Fallen) at [*Building 2 Stands (0CC7F0FC)](#trigger-0cc7f0fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Garrison Team 2 (08BBD6CC)](all05umd-teams.md#team-08bbd6cc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8767, Events line 8877, Actions line 8987.

<a id="trigger-0cc6f07c"></a>

### 24. *Garrison Time 3 - 0CC6F07C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Attached scope: tag definitions 0CC7704C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Building 3 Fallen) is clear.

Flag writers in this mission: set local flag 6 (Building 3 Fallen) at [*Building 3 Stands (0CC6E6DC)](#trigger-0cc6e6dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Garrison Team 3 (08BBD32C)](all05umd-teams.md#team-08bbd32c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8768, Events line 8878, Actions line 8988.

<a id="trigger-0dcc216c"></a>

### 25. *Garrison Time 4 - 0DCC216C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Attached scope: tag definitions 0DCC6E4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (Building 4 Fallen) is clear.

Flag writers in this mission: set local flag 7 (Building 4 Fallen) at [*Building 4 Stands (0938DE7C)](#trigger-0938de7c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Garrison Team 4 (08BBD1FC)](all05umd-teams.md#team-08bbd1fc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8769, Events line 8879, Actions line 8989.

<a id="trigger-0dcc636c"></a>

### 26. *Garrison Time 5 - 0DCC636C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Attached scope: tag definitions 0DCC61FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 8 (Building 5 Fallen) is clear.

Flag writers in this mission: set local flag 8 (Building 5 Fallen) at [*Building 5 Stands (093AA33C)](#trigger-093aa33c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Garrison Team 5 (08BBEA1C)](all05umd-teams.md#team-08bbea1c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8770, Events line 8880, Actions line 8990.

<a id="trigger-0dcd607c"></a>

### 27. *Garrison Time 6 - 0DCD607C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Attached scope: tag definitions 0DCC6F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (Building 6 Fallen) is clear.

Flag writers in this mission: set local flag 9 (Building 6 Fallen) at [*Building 6 Stands (093AEACC)](#trigger-093aeacc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Garrison Team 6 (08BBE67C)](all05umd-teams.md#team-08bbe67c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8771, Events line 8881, Actions line 8991.

<a id="trigger-0dcd938c"></a>

### 28. *Garrison Time 7 - 0DCD938C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Attached scope: tag definitions 0DCDCD5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Building 7 Fallen) is clear.

Flag writers in this mission: set local flag 10 (Building 7 Fallen) at [*Building 7 Stands (093AE79C)](#trigger-093ae79c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Garrison Team 7 (08BBE2DC)](all05umd-teams.md#team-08bbe2dc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8772, Events line 8882, Actions line 8992.

<a id="trigger-0dcdf99c"></a>

### 29. *Garrison Time 8 - 0DCDF99C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Attached scope: tag definitions 0DCDECBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 11 (Building 8 Fallen) is clear.

Flag writers in this mission: set local flag 11 (Building 8 Fallen) at [*Building 8 Stands (093AE46C)](#trigger-093ae46c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Garrison Team 8 (08BBE1AC)](all05umd-teams.md#team-08bbe1ac).
2. Enable and reset applicable timers for [Chaos Drones Easy (097F109C)](#trigger-097f109c).
3. Enable and reset applicable timers for [Chaos Drones Med (097F24AC)](#trigger-097f24ac).
4. Enable and reset applicable timers for [Chaos Drones Hard (097F20AC)](#trigger-097f20ac).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8773, Events line 8883, Actions line 8993.

<a id="trigger-0984d26c"></a>

### 30. %Garrison Made Teams - 0984D26C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time Start! (0CC7E49C)](#trigger-0cc7e49c).

Attached scope: tag definitions 0985232C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [% Garrison 01 BG (069A103C)](#trigger-069a103c).
2. Enable and reset applicable timers for [% Garrison 02 AL (09377BEC)](#trigger-09377bec).
3. Enable and reset applicable timers for [% Garrison 03 AZ (0937743C)](#trigger-0937743c).
4. Enable and reset applicable timers for [% Garrison 04 AN (09376F3C)](#trigger-09376f3c).
5. Enable and reset applicable timers for [% Garrison 05 AY (09376C9C)](#trigger-09376c9c).
6. Enable and reset applicable timers for [% Garrison 06 BA (0937676C)](#trigger-0937676c).
7. Enable and reset applicable timers for [% Garrison 07 BC (0937764C)](#trigger-0937764c).
8. Enable and reset applicable timers for [% Garrison 08 BD (0937609C)](#trigger-0937609c).
9. Enable and reset applicable timers for [% Garrison 09 BE (09375CFC)](#trigger-09375cfc).
10. Enable and reset applicable timers for [% Garrison 10 BF (093757FC)](#trigger-093757fc).
11. Enable and reset applicable timers for [% Garrison 11 BB (0937555C)](#trigger-0937555c).
12. Enable and reset applicable timers for [$ Random Garrison 01 (05F7BB0C)](#trigger-05f7bb0c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8774, Events line 8884, Actions line 8994.

<a id="trigger-097f109c"></a>

### 31. Chaos Drones Easy - 097F109C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time 8 (0DCDF99C)](#trigger-0dcdf99c).

Attached scope: tag definitions 097F259C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_ChaosDroneEasy1 (086AA45C)](all05umd-teams.md#team-086aa45c).
2. Create/recruit team [_A05_ChaosDroneEasy2 (086ABDEC)](all05umd-teams.md#team-086abdec).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8775, Events line 8885, Actions line 8995.

<a id="trigger-097f24ac"></a>

### 32. Chaos Drones Med - 097F24AC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time 8 (0DCDF99C)](#trigger-0dcdf99c).

Attached scope: tag definitions 097F219C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_ChaosDroneMed1 (086ABA4C)](all05umd-teams.md#team-086aba4c).
2. Create/recruit team [_A05_ChaosDroneMed2 (086A87DC)](all05umd-teams.md#team-086a87dc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8776, Events line 8886, Actions line 8996.

<a id="trigger-097f20ac"></a>

### 33. Chaos Drones Hard - 097F20AC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [*Garrison Time 8 (0DCDF99C)](#trigger-0dcdf99c).

Attached scope: tag definitions 097F3D1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_ChaosDroneHard1 (086AB6AC)](all05umd-teams.md#team-086ab6ac).
2. Create/recruit team [_A05_ChaosDroneHard2 (086AB04C)](all05umd-teams.md#team-086ab04c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8777, Events line 8887, Actions line 8997.

<a id="trigger-069a103c"></a>

### 34. % Garrison 01 BG - 069A103C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 09377CDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison BG (08BC054C)](all05umd-teams.md#team-08bc054c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8778, Events line 8888, Actions line 8998.

<a id="trigger-09377bec"></a>

### 35. % Garrison 02 AL - 09377BEC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 0937752C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison AL (08BC01AC)](all05umd-teams.md#team-08bc01ac).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8779, Events line 8889, Actions line 8999.

<a id="trigger-0937743c"></a>

### 36. % Garrison 03 AZ - 0937743C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 093770FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison AZ (08BC1B7C)](all05umd-teams.md#team-08bc1b7c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8780, Events line 8890, Actions line 9000.

<a id="trigger-09376f3c"></a>

### 37. % Garrison 04 AN - 09376F3C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 09376D8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 40 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison AN (08BC17DC)](all05umd-teams.md#team-08bc17dc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8781, Events line 8891, Actions line 9001.

<a id="trigger-09376c9c"></a>

### 38. % Garrison 05 AY - 09376C9C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 0937695C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison AY (08BC143C)](all05umd-teams.md#team-08bc143c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8782, Events line 8892, Actions line 9002.

<a id="trigger-0937676c"></a>

### 39. % Garrison 06 BA - 0937676C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 0937773C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison BA (08BC2EFC)](all05umd-teams.md#team-08bc2efc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8783, Events line 8893, Actions line 9003.

<a id="trigger-0937764c"></a>

### 40. % Garrison 07 BC - 0937764C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 0937618C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 70 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison BC (08BC2B5C)](all05umd-teams.md#team-08bc2b5c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8784, Events line 8894, Actions line 9004.

<a id="trigger-0937609c"></a>

### 41. % Garrison 08 BD - 0937609C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 09375DEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison BD (08BC27BC)](all05umd-teams.md#team-08bc27bc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8785, Events line 8895, Actions line 9005.

<a id="trigger-09375cfc"></a>

### 42. % Garrison 09 BE - 09375CFC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 093758EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison BE (08BC241C)](all05umd-teams.md#team-08bc241c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8786, Events line 8896, Actions line 9006.

<a id="trigger-093757fc"></a>

### 43. % Garrison 10 BF - 093757FC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 0937564C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison BF (08BC3EFC)](all05umd-teams.md#team-08bc3efc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8787, Events line 8897, Actions line 9007.

<a id="trigger-0937555c"></a>

### 44. % Garrison 11 BB - 0937555C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 0937531C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 110 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_AI Garrison BB (08BC3A4C)](all05umd-teams.md#team-08bc3a4c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8788, Events line 8898, Actions line 9008.

<a id="trigger-05f7bb0c"></a>

### 45. $ Random Garrison 01 - 05F7BB0C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [%Garrison Made Teams (0984D26C)](#trigger-0984d26c).

Attached scope: tag definitions 05F7BA2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).
2. Enable and reset applicable timers for [$ Random Garrison 02 (05F7B4CC)](#trigger-05f7b4cc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8789, Events line 8899, Actions line 9009.

<a id="trigger-05f7b4cc"></a>

### 46. $ Random Garrison 02 - 05F7B4CC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [$ Random Garrison 01 (05F7BB0C)](#trigger-05f7bb0c).

Attached scope: tag definitions 05F7B28C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).
2. Enable and reset applicable timers for [$ Random Garrison 03 (05F7B19C)](#trigger-05f7b19c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8790, Events line 8900, Actions line 9010.

<a id="trigger-05f7b19c"></a>

### 47. $ Random Garrison 03 - 05F7B19C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [$ Random Garrison 02 (05F7B4CC)](#trigger-05f7b4cc).

Attached scope: tag definitions 05F7CF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).
2. Enable and reset applicable timers for [$ Random Garrison 04 (05F7CE5C)](#trigger-05f7ce5c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8791, Events line 8901, Actions line 9011.

<a id="trigger-05f7ce5c"></a>

### 48. $ Random Garrison 04 - 05F7CE5C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [$ Random Garrison 03 (05F7B19C)](#trigger-05f7b19c).

Attached scope: tag definitions 05F7C84C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).
2. Enable and reset applicable timers for [$ Random Garrison 05 (05F7C64C)](#trigger-05f7c64c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8792, Events line 8902, Actions line 9012.

<a id="trigger-05f7c64c"></a>

### 49. $ Random Garrison 05 - 05F7C64C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [$ Random Garrison 04 (05F7CE5C)](#trigger-05f7ce5c).

Attached scope: tag definitions 05F7C40C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).
2. Enable and reset applicable timers for [$ Random Garrison 06 (07BEF0FC)](#trigger-07bef0fc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8793, Events line 8903, Actions line 9013.

<a id="trigger-07bef0fc"></a>

### 50. $ Random Garrison 06 - 07BEF0FC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [$ Random Garrison 05 (05F7C64C)](#trigger-05f7c64c).

Attached scope: tag definitions 0963D5EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).
2. Enable and reset applicable timers for [$ Random Garrison 07 (0963AC0C)](#trigger-0963ac0c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8794, Events line 8904, Actions line 9014.

<a id="trigger-0963ac0c"></a>

### 51. $ Random Garrison 07 - 0963AC0C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [$ Random Garrison 06 (07BEF0FC)](#trigger-07bef0fc).

Attached scope: tag definitions 0965D24C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).
2. Enable and reset applicable timers for [$ Random Garrison 08 (0965C5CC)](#trigger-0965c5cc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8795, Events line 8905, Actions line 9015.

<a id="trigger-0965c5cc"></a>

### 52. $ Random Garrison 08 - 0965C5CC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [$ Random Garrison 07 (0963AC0C)](#trigger-0963ac0c).

Attached scope: tag definitions 0965EB3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).
2. Enable and reset applicable timers for [$ Random Garrison 09 (0965EA4C)](#trigger-0965ea4c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8796, Events line 8906, Actions line 9016.

<a id="trigger-0965ea4c"></a>

### 53. $ Random Garrison 09 - 0965EA4C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [$ Random Garrison 08 (0965C5CC)](#trigger-0965c5cc).

Attached scope: tag definitions 0965E6CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).
2. Enable and reset applicable timers for [$ Random Garrison 10 (0965E40C)](#trigger-0965e40c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8797, Events line 8907, Actions line 9017.

<a id="trigger-0965e40c"></a>

### 54. $ Random Garrison 10 - 0965E40C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [$ Random Garrison 09 (0965EA4C)](#trigger-0965ea4c).

Attached scope: tag definitions 0965E1CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Random Garrison (08BD08EC)](all05umd-teams.md#team-08bd08ec).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8798, Events line 8908, Actions line 9018.

<a id="trigger-0e5fa1bc"></a>

### 55. Black Eagle Initiate - 0E5FA1BC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E5FB56C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  Naval: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Black Eagle Attack (0E5CDB7C)](#trigger-0e5cdb7c).
2. Play voice notification Mis_xA5_EvaBlackEagles.
3. Enable and reset applicable timers for [AI Production (0778A83C)](#trigger-0778a83c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8799, Events line 8909, Actions line 9019.

<a id="trigger-0778a83c"></a>

### 56. AI Production - 0778A83C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Black Eagle Initiate (0E5FA1BC)](#trigger-0e5fa1bc).

Attached scope: tag definitions 077A6CAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).
3. Production Begins: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).
4. Production Begins: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).
5. Create/recruit team [_A05_Base Defense (0771D13C)](all05umd-teams.md#team-0771d13c).
6. Create/recruit team [_A05_Base Defense 2 (0913653C)](all05umd-teams.md#team-0913653c).
7. Create/recruit team [_A05_Defense B1 (0913788C)](all05umd-teams.md#team-0913788c).
8. Create/recruit team [_A05_Defense B2 (091330CC)](all05umd-teams.md#team-091330cc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8800, Events line 8910, Actions line 9020.

<a id="trigger-0685c9bc"></a>

### 57. Engineer Tech Airport - Hard - 0685C9BC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0685C64C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Engineer Airport - Hard (0692ECCC)](all05umd-teams.md#team-0692eccc).
2. Enable and reset applicable timers for [Airport Warning (097D4E9C)](#trigger-097d4e9c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8801, Events line 8911, Actions line 9021.

<a id="trigger-097d4e9c"></a>

### 58. Airport Warning - 097D4E9C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Engineer Tech Airport - Hard (0685C9BC)](#trigger-0685c9bc).

Attached scope: tag definitions 097D444C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 70 (global list position: Tech Airport (CAAIRP)). A map-local type-list change can affect index interpretation.
2. 710 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA5_EvaAirportHint.
2. Reveal terrain around waypoint 81 (cell 143, 159).
3. Create radar-event marker type 1 at waypoint 81 (cell 143, 159).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8802, Events line 8912, Actions line 9022.

<a id="trigger-0cc7c45c"></a>

### 59. Building 1 Stands - 0CC7C45C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CARUS04), owner Civilian House, cell (138, 147), tag 0CC7E99C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 4 (Building 1 Fallen).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8803, Events line 8913, Actions line 9023.

<a id="trigger-0cc7f0fc"></a>

### 60. *Building 2 Stands - 0CC7F0FC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANWY09), owner Civilian House, cell (133, 119), tag 0CC78E7C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 5 (Building 2 Fallen).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8804, Events line 8914, Actions line 9024.

<a id="trigger-0cc6e6dc"></a>

### 61. *Building 3 Stands - 0CC6E6DC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANWY23), owner Civilian House, cell (116, 137), tag 0CC6965C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 6 (Building 3 Fallen).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8805, Events line 8915, Actions line 9025.

<a id="trigger-0938de7c"></a>

### 62. *Building 4 Stands - 0938DE7C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY06), owner Civilian House, cell (112, 112), tag 093AB62C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 7 (Building 4 Fallen).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8806, Events line 8916, Actions line 9026.

<a id="trigger-093aa33c"></a>

### 63. *Building 5 Stands - 093AA33C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM02), owner Civilian House, cell (106, 149), tag 093AEBBC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 8 (Building 5 Fallen).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8807, Events line 8917, Actions line 9027.

<a id="trigger-093aeacc"></a>

### 64. *Building 6 Stands - 093AEACC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY06), owner Civilian House, cell (86, 125), tag 093AE88C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 9 (Building 6 Fallen).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8808, Events line 8918, Actions line 9028.

<a id="trigger-093ae79c"></a>

### 65. *Building 7 Stands - 093AE79C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY16), owner Civilian House, cell (108, 137), tag 093AE55C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 10 (Building 7 Fallen).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8809, Events line 8919, Actions line 9029.

<a id="trigger-093ae46c"></a>

### 66. *Building 8 Stands - 093AE46C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANWY26), owner Civilian House, cell (112, 126), tag 093AEE7C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 11 (Building 8 Fallen).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8810, Events line 8920, Actions line 9030.

<a id="trigger-093759fc"></a>

### 67. Player Wins - 093759FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09374E4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 12 (BadGuy1 Dead) is set.
2. local flag 13 (BadGuy2 Dead) is set.

Flag writers in this mission: set local flag 12 (BadGuy1 Dead) at [It's Over Part 1 (0689427C)](#trigger-0689427c); set local flag 13 (BadGuy2 Dead) at [It's Over Part 2 (09374A1C)](#trigger-09374a1c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play sound Cheer.
2. Declare owner selector 15 (country/type PLAYER; placed owner Player House) the winner.

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8811, Events line 8921, Actions line 9031.

<a id="trigger-09374a1c"></a>

### 68. It's Over Part 2 - 09374A1C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 093747DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Set local flag 13 (BadGuy2 Dead).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8812, Events line 8922, Actions line 9032.

<a id="trigger-0928a36c"></a>

### 69. Introduce Chaos Drone - 0928A36C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0928B5EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 16 (Chaos Revealed?) is set.

Flag writers in this mission: set local flag 16 (Chaos Revealed?) at [Chaos Drone Seen? (043D1B8C)](#trigger-043d1b8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_xA5_EvaChaosDrone.
2. Flash team [_A05_Chaos Drone (090DB8EC)](all05umd-teams.md#team-090db8ec) with duration setting 90.
3. Flash team [_A05_ChaosDroneEasy1 (086AA45C)](all05umd-teams.md#team-086aa45c) with duration setting 90.
4. Flash team [_A05_ChaosDroneEasy2 (086ABDEC)](all05umd-teams.md#team-086abdec) with duration setting 90.
5. Flash team [_A05_ChaosDroneHard1 (086AB6AC)](all05umd-teams.md#team-086ab6ac) with duration setting 90.
6. Flash team [_A05_ChaosDroneHard2 (086AB04C)](all05umd-teams.md#team-086ab04c) with duration setting 90.
7. Flash team [_A05_ChaosDroneMed1 (086ABA4C)](all05umd-teams.md#team-086aba4c) with duration setting 90.
8. Flash team [_A05_ChaosDroneMed2 (086A87DC)](all05umd-teams.md#team-086a87dc) with duration setting 90.
9. Flash team [_A05_Intro Chaos Drone (0B6D57DC)](all05umd-teams.md#team-0b6d57dc) with duration setting 90.

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8813, Events line 8923, Actions line 9033.

<a id="trigger-0c73968c"></a>

### 70. Wow! - 0C73968C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C7391CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 32 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification A05_p01.

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8814, Events line 8924, Actions line 9034.

<a id="trigger-0c22514c"></a>

### 71. Cam Move - 0C22514C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C22454C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 36 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 70 (cell 157, 138).
2. Reveal terrain around waypoint 69 (cell 160, 132).
3. Reveal terrain around waypoint 71 (cell 154, 131).
4. Move the camera to waypoint 116 (cell 157, 133) with speed setting 4.
5. Enable and reset applicable timers for [Cam Move to Sub (0979D9AC)](#trigger-0979d9ac).
6. Enable and reset applicable timers for [Create Boomer Drama (0CA4E3CC)](#trigger-0ca4e3cc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8815, Events line 8925, Actions line 9035.

<a id="trigger-0979d9ac"></a>

### 72. Cam Move to Sub - 0979D9AC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Cam Move (0C22514C)](#trigger-0c22514c).

Attached scope: tag definitions 0979D45C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 87 (cell 59, 73).
2. Reveal terrain around waypoint 86 (cell 56, 41).
3. Move the camera to waypoint 89 (cell 53, 73) with speed setting 4.
4. Enable and reset applicable timers for [Cam Move to Sub Back (0979D36C)](#trigger-0979d36c).
5. Flash team [_A05_DEMO BOOMER (08C0B1FC)](all05umd-teams.md#team-08c0b1fc) with duration setting 90.
6. Enable and reset applicable timers for [Eva Introduces Boomers (0CC391BC)](#trigger-0cc391bc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8816, Events line 8926, Actions line 9036.

<a id="trigger-0ca4e3cc"></a>

### 73. Create Boomer Drama - 0CA4E3CC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Cam Move (0C22514C)](#trigger-0c22514c).

Attached scope: tag definitions 0CA48E1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_DEMO PLAYER (08A71DEC)](all05umd-teams.md#team-08a71dec).
2. Create/recruit team [_A05_DEMO BOOMER (08C0B1FC)](all05umd-teams.md#team-08c0b1fc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8817, Events line 8927, Actions line 9037.

<a id="trigger-0979d36c"></a>

### 74. Cam Move to Sub Back - 0979D36C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Cam Move to Sub (0979D9AC)](#trigger-0979d9ac).

Attached scope: tag definitions 0979D12C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 44 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 38 (cell 50, 90) with speed setting 3.

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8818, Events line 8928, Actions line 9038.

<a id="trigger-0cc391bc"></a>

### 75. Eva Introduces Boomers - 0CC391BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Cam Move to Sub (0979D9AC)](#trigger-0979d9ac).

Attached scope: tag definitions 0CC3BC1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_Boomer.

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8819, Events line 8929, Actions line 9039.

<a id="trigger-099bd73c"></a>

### 76. Reveal Opera House - 099BD73C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 099AF46C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 72 (cell 47, 72).
2. Reveal terrain around waypoint 82 (cell 42, 74).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8820, Events line 8930, Actions line 9040.

<a id="trigger-0995ce2c"></a>

### 77. Virus Mission - 0995CE2C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0995CA4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 14 (Virus Dropped Off) is set.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Virus On A Mission (0995C91C)](all05umd-teams.md#team-0995c91c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8821, Events line 8931, Actions line 9041.

<a id="trigger-097c771c"></a>

### 78. Engineer Tech Machine Shop - 097C771C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097C763C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Engineer Machine Shop (097C5E6C)](all05umd-teams.md#team-097c5e6c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8822, Events line 8932, Actions line 9042.

<a id="trigger-097c72ac"></a>

### 79. Engineer Tech Hospital - 097C72AC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 097C705C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Engineer Tech Hospital (097E359C)](all05umd-teams.md#team-097e359c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8823, Events line 8933, Actions line 9043.

<a id="trigger-0970ee6c"></a>

### 80. Boomers There? - 0970EE6C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0970D6DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 15 (Boomers There?) is set.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Boomer Split 1 (08DD645C)](all05umd-teams.md#team-08dd645c).
2. Create/recruit team [_A05_Boomer Split 2 (08DD60BC)](all05umd-teams.md#team-08dd60bc).
3. Create/recruit team [_A05_Boomer Split 3 (08DD7C8C)](all05umd-teams.md#team-08dd7c8c).
4. Enable and reset applicable timers for [Boomer Cleanup (085AE04C)](#trigger-085ae04c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8824, Events line 8934, Actions line 9044.

<a id="trigger-085ae04c"></a>

### 81. Boomer Cleanup - 085AE04C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Boomers There? (0970EE6C)](#trigger-0970ee6c).

Attached scope: tag definitions 085AD39C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. At least 1 instances of Boomer (BSUB) exist on the map, under this event's ownership scope.
2. No instances of Allied Shipyard (GAYARD) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Boomer Cleanup 1 (085A665C)](all05umd-teams.md#team-085a665c).
2. Create/recruit team [_A05_Boomer Cleanup 2 (085AFEFC)](all05umd-teams.md#team-085afefc).
3. Create/recruit team [_A05_Boomer Cleanup 3 (085AFDCC)](all05umd-teams.md#team-085afdcc).
4. Create/recruit team [_A05_Boomer Cleanup 4 (085AFC9C)](all05umd-teams.md#team-085afc9c).
5. Create/recruit team [_A05_Boomer Cleanup 5 (085AFB6C)](all05umd-teams.md#team-085afb6c).
6. Create/recruit team [_A05_Boomer Cleanup 6 (085AFA3C)](all05umd-teams.md#team-085afa3c).
7. Create/recruit team [_A05_Boomer Cleanup 7 (085AF4AC)](all05umd-teams.md#team-085af4ac).
8. Create/recruit team [_A05_Boomer Cleanup 8 (085AF37C)](all05umd-teams.md#team-085af37c).
9. Create/recruit team [_A05_Boomer Cleanup 9 (085AF24C)](all05umd-teams.md#team-085af24c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8825, Events line 8935, Actions line 9045.

<a id="trigger-043d1b8c"></a>

### 82. Chaos Drone Seen? - 043D1B8C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043D109C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 16 (Chaos Revealed?).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8826, Events line 8936, Actions line 9046.

<a id="trigger-0977d75c"></a>

### 83. Garrison Tank Bunkers 1 - 0977D75C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0977D26C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Tank Bunker 1a (0C86F54C)](all05umd-teams.md#team-0c86f54c).
2. Create/recruit team [_A05_Tank Bunker 1b (0C86F1AC)](all05umd-teams.md#team-0c86f1ac).
3. Create/recruit team [_A05_Tank Bunker 1aa (0684C56C)](all05umd-teams.md#team-0684c56c).
4. Create/recruit team [_A05_Tank Bunker 1bb (0684C43C)](all05umd-teams.md#team-0684c43c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8827, Events line 8937, Actions line 9047.

<a id="trigger-0977d17c"></a>

### 84. Garrison Tank Bunkers 2 - 0977D17C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0977ECFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Tank Bunker 2a (08FD86AC)](all05umd-teams.md#team-08fd86ac).
2. Create/recruit team [_A05_Tank Bunker 2aa (0761B8EC)](all05umd-teams.md#team-0761b8ec).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8828, Events line 8938, Actions line 9048.

<a id="trigger-043cf47c"></a>

### 85. Deploy Guardian GI - 043CF47C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043CECAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Guardian GI Deploy 1 (0C7B854C)](all05umd-teams.md#team-0c7b854c).
2. Create/recruit team [_A05_Guardian GI Deploy 2 (0683F32C)](all05umd-teams.md#team-0683f32c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8829, Events line 8939, Actions line 9049.

<a id="trigger-0975827c"></a>

### 86. Travelers N1 - 0975827C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Travelers N2 (0975ACDC)](#trigger-0975acdc).

Attached scope: tag definitions 0975AF4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Civilian Vehicle CU 1 (0686A6BC)](all05umd-teams.md#team-0686a6bc).
2. Disable [Travelers N1 (0975827C)](#trigger-0975827c).
3. Enable and reset applicable timers for [Travelers N2 (0975ACDC)](#trigger-0975acdc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8830, Events line 8940, Actions line 9050.

<a id="trigger-0975acdc"></a>

### 87. Travelers N2 - 0975ACDC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Travelers N1 (0975827C)](#trigger-0975827c).

Attached scope: tag definitions 0975A8FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Civilian Vehicle CU 2 (0BA195DC)](all05umd-teams.md#team-0ba195dc).
2. Enable and reset applicable timers for [Travelers N1 (0975827C)](#trigger-0975827c).
3. Disable [Travelers N2 (0975ACDC)](#trigger-0975acdc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8831, Events line 8941, Actions line 9051.

<a id="trigger-0ca6e43c"></a>

### 88. Travelers S1 - 0CA6E43C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Travelers S2 (0CA69CFC)](#trigger-0ca69cfc).

Attached scope: tag definitions 0CA69DEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Civilian Vehicle CX 1 (0BA1939C)](all05umd-teams.md#team-0ba1939c).
2. Disable [Travelers S1 (0CA6E43C)](#trigger-0ca6e43c).
3. Enable and reset applicable timers for [Travelers S2 (0CA69CFC)](#trigger-0ca69cfc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8832, Events line 8942, Actions line 9052.

<a id="trigger-0ca69cfc"></a>

### 89. Travelers S2 - 0CA69CFC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Travelers S1 (0CA6E43C)](#trigger-0ca6e43c).

Attached scope: tag definitions 0CA69ABC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Civilian Vehicle CX 2 (0BA1ABFC)](all05umd-teams.md#team-0ba1abfc).
2. Disable [Travelers S2 (0CA69CFC)](#trigger-0ca69cfc).
3. Enable and reset applicable timers for [Travelers S1 (0CA6E43C)](#trigger-0ca6e43c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8833, Events line 8943, Actions line 9053.

<a id="trigger-097be04c"></a>

### 90. More Travelers S1 - 097BE04C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [More Travelers S2 (097BF0BC)](#trigger-097bf0bc).

Attached scope: tag definitions 097BFADC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 42 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Civilian Vehicle DC 1 (0C82F4BC)](all05umd-teams.md#team-0c82f4bc).
2. Disable [More Travelers S1 (097BE04C)](#trigger-097be04c).
3. Enable and reset applicable timers for [More Travelers S2 (097BF0BC)](#trigger-097bf0bc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8834, Events line 8944, Actions line 9054.

<a id="trigger-097bf0bc"></a>

### 91. More Travelers S2 - 097BF0BC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [More Travelers S1 (097BE04C)](#trigger-097be04c).

Attached scope: tag definitions 068D583C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Civilian Vehicle DC 2 (0C830EFC)](all05umd-teams.md#team-0c830efc).
2. Disable [More Travelers S2 (097BF0BC)](#trigger-097bf0bc).
3. Enable and reset applicable timers for [More Travelers S1 (097BE04C)](#trigger-097be04c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8835, Events line 8945, Actions line 9055.

<a id="trigger-0979832c"></a>

### 92. More Travelers N1 - 0979832C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [More Travelers N2 (09799BBC)](#trigger-09799bbc).

Attached scope: tag definitions 09799CAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Civilian Vehicle DH 1 (097C053C)](all05umd-teams.md#team-097c053c).
2. Disable [More Travelers N1 (0979832C)](#trigger-0979832c).
3. Enable and reset applicable timers for [More Travelers N2 (09799BBC)](#trigger-09799bbc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8836, Events line 8946, Actions line 9056.

<a id="trigger-09799bbc"></a>

### 93. More Travelers N2 - 09799BBC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [More Travelers N1 (0979832C)](#trigger-0979832c).

Attached scope: tag definitions 0979947C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 22 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_A05_Civilian Vehicle DH 2 (097C272C)](all05umd-teams.md#team-097c272c).
2. Disable [More Travelers N2 (09799BBC)](#trigger-09799bbc).
3. Enable and reset applicable timers for [More Travelers N1 (0979832C)](#trigger-0979832c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8837, Events line 8947, Actions line 9057.

<a id="trigger-0cb5ecfc"></a>

### 94. Objective 1 - 0CB5ECFC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CB5E96C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Destroy Yuri's Cloning facility in the South” (MISSION:DestroyCloning).
2. Create radar-event marker type 1 at waypoint 116 (cell 157, 133).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8838, Events line 8948, Actions line 9058.

<a id="trigger-0cb5f48c"></a>

### 95. Dead Cloning Vats - 0CB5F48C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Cloning Vats (NACLON), owner BadGuy1 House, cell (155, 136), tag 0CB66BDC, persistence mode 1; Cloning Vats (NACLON), owner BadGuy1 House, cell (152, 129), tag 0CB66BDC, persistence mode 1; Cloning Vats (NACLON), owner BadGuy1 House, cell (158, 130), tag 0CB66BDC, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play voice notification EVA_NewMissionObjective.
2. Display message “Objective: Destroy Yuri's remaining forces.” (MISSION:DestroyYuri05A).
3. Disable [Objective 1 (0CB5ECFC)](#trigger-0cb5ecfc).
4. Enable and reset applicable timers for [Objective 2 (0CB6677C)](#trigger-0cb6677c).
5. Set local flag 17 (Obj 1 Complete).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8839, Events line 8949, Actions line 9059.

<a id="trigger-0cb6677c"></a>

### 96. Objective 2 - 0CB6677C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Dead Cloning Vats (0CB5F48C)](#trigger-0cb5f48c).

Attached scope: tag definitions 0CB663FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Destroy Yuri's remaining forces.” (MISSION:DestroyYuri05A).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8840, Events line 8950, Actions line 9060.

<a id="trigger-07a5295c"></a>

### 97. Kill Init Boomer Teams - 07A5295C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A5113C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [_A05_1 Yuri Boomer M (0C1541FC)](all05umd-teams.md#team-0c1541fc).
2. Remove instances of the team organization (not automatically its surviving objects) [_A05_1 Yuri Boomer N (092D22CC)](all05umd-teams.md#team-092d22cc).
3. Remove instances of the team organization (not automatically its surviving objects) [_A05_1 Yuri Boomer O (092D219C)](all05umd-teams.md#team-092d219c).
4. Remove instances of the team organization (not automatically its surviving objects) [_A05_1 Yuri Boomer P (092D206C)](all05umd-teams.md#team-092d206c).
5. Remove instances of the team organization (not automatically its surviving objects) [_A05_1 Yuri Boomer Q (092D3D2C)](all05umd-teams.md#team-092d3d2c).
6. Remove instances of the team organization (not automatically its surviving objects) [_A05_1 Yuri Boomer R (092D39BC)](all05umd-teams.md#team-092d39bc).
7. Remove instances of the team organization (not automatically its surviving objects) [_A05_1 Yuri Boomer S (092D376C)](all05umd-teams.md#team-092d376c).
8. Remove instances of the team organization (not automatically its surviving objects) [_A05_1 Yuri Boomer T (092D363C)](all05umd-teams.md#team-092d363c).
9. Remove instances of the team organization (not automatically its surviving objects) [_A05_1 Yuri Boomer U (092D350C)](all05umd-teams.md#team-092d350c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8841, Events line 8951, Actions line 9061.

<a id="trigger-079d370c"></a>

### 98. Powered Down - 079D370C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079D32BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Low Power: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Create/recruit team [_A05_Power Team (090EF1DC)](all05umd-teams.md#team-090ef1dc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8842, Events line 8952, Actions line 9062.

<a id="trigger-07aada3c"></a>

### 99. Kill Garrison 1 - 07AADA3C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAPARS13), owner Civilian House, cell (59, 91), tag 07AAD5AC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Kill Bldg DN (07AAEB1C)](all05umd-teams.md#team-07aaeb1c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8843, Events line 8953, Actions line 9063.

<a id="trigger-07aad4bc"></a>

### 100. Kill Garrison 2 - 07AAD4BC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM06), owner Civilian House, cell (47, 103), tag 07AAD27C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Kill Bldg DG (07AAD14C)](all05umd-teams.md#team-07aad14c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8844, Events line 8954, Actions line 9064.

<a id="trigger-05b83b2c"></a>

### 101. Factories Gone BG1a - 05B83B2C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05B8336C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 17 (Obj 1 Complete) is set.
2. No Factories left. See attached-object/cell scope below.

Flag writers in this mission: set local flag 17 (Obj 1 Complete) at [Dead Cloning Vats (0CB5F48C)](#trigger-0cb5f48c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Factories Gone BG1b (05B8327C)](#trigger-05b8327c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8845, Events line 8955, Actions line 9065.

<a id="trigger-05b8327c"></a>

### 102. Factories Gone BG1b - 05B8327C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Factories Gone BG1a (05B83B2C)](#trigger-05b83b2c).

Attached scope: tag definitions 05B8303C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).
2. Enable and reset applicable timers for [Factories Gone BG1c (05B84F3C)](#trigger-05b84f3c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8846, Events line 8956, Actions line 9066.

<a id="trigger-05b84f3c"></a>

### 103. Factories Gone BG1c - 05B84F3C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Factories Gone BG1b (05B8327C)](#trigger-05b8327c).

Attached scope: tag definitions 05B84B0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8847, Events line 8957, Actions line 9067.

<a id="trigger-05b8475c"></a>

### 104. Factories Gone BG2a - 05B8475C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05B8451C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Factories Gone BG2b (05B8442C)](#trigger-05b8442c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8848, Events line 8958, Actions line 9068.

<a id="trigger-05b8442c"></a>

### 105. Factories Gone BG2b - 05B8442C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Factories Gone BG2a (05B8475C)](#trigger-05b8475c).

Attached scope: tag definitions 05B841EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).
2. Enable and reset applicable timers for [Factories Gone BG2c (05B840FC)](#trigger-05b840fc).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8849, Events line 8959, Actions line 9069.

<a id="trigger-05b840fc"></a>

### 106. Factories Gone BG2c - 05B840FC

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Factories Gone BG2b (05B8442C)](#trigger-05b8442c).

Attached scope: tag definitions 05B85E7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8850, Events line 8960, Actions line 9070.

<a id="trigger-077835ac"></a>

### 107. Create Help! - 077835AC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner BadGuy1 House, cell (142, 119), tag 07787C6C, persistence mode 0; Bio Reactor (YAPOWR), owner BadGuy1 House, cell (151, 138), tag 07787C6C, persistence mode 0; Bio Reactor (YAPOWR), owner BadGuy1 House, cell (160, 138), tag 07787C6C, persistence mode 0; Bio Reactor (YAPOWR), owner BadGuy1 House, cell (151, 116), tag 07787C6C, persistence mode 0; Bio Reactor (YAPOWR), owner BadGuy1 House, cell (160, 116), tag 07787C6C, persistence mode 0; Psychic Radar (NAPSIS), owner BadGuy1 House, cell (157, 120), tag 07787C6C, persistence mode 0; Gattling Cannon (YAGGUN), owner BadGuy1 House, cell (161, 132), tag 07787C6C, persistence mode 0; Gattling Cannon (YAGGUN), owner BadGuy1 House, cell (161, 120), tag 07787C6C, persistence mode 0; Gattling Cannon (YAGGUN), owner BadGuy1 House, cell (151, 120), tag 07787C6C, persistence mode 0; Bio Reactor (YAPOWR), owner BadGuy1 House, cell (160, 126), tag 07787C6C, persistence mode 0.

**Wait for the recorded events:**

1. First damaged (any source). See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Base Defense (0771D13C)](all05umd-teams.md#team-0771d13c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8851, Events line 8961, Actions line 9071.

<a id="trigger-0867518c"></a>

### 108. Deploy GI - 0867518C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0867424C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_A05_Deploy GI 1 (08BE4DEC)](all05umd-teams.md#team-08be4dec).
2. Create/recruit team [_A05_Deploy GI 2 (08BE493C)](all05umd-teams.md#team-08be493c).
3. Create/recruit team [_A05_Deploy GI 3 (07686CAC)](all05umd-teams.md#team-07686cac).
4. Create/recruit team [_A05_Deploy GI 4 (07686B7C)](all05umd-teams.md#team-07686b7c).

Source locator: mapsmd03.mix/all05umd.map; Triggers line 8852, Events line 8962, Actions line 9072.

[All team rosters and ordered plans](all05umd-teams.md) | [All mission overrides](all05umd-overrides.md)
