# Operation: To The Moon

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov06lmd.map. **Effective extracted member:** mapsmd03.mix/sov06lmd.map. **Trigger definitions:** 81.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov06lmd-teams.md) | [All mission overrides](sov06lmd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Russians |
| Theater | LUNAR |
| Map size | 0,0,40,120 |
| Visible local rectangle | 2,4,36,110 |
| Placed vehicles | 23 |
| Placed infantry | 35 |
| Placed structures | 80 |
| Placed aircraft | 0 |
| Team templates | 44 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 500 | Americans |
| 1 | Alliance | 500 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 0 | Africans |
| 6 | Arabs | 0 | Arabs |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 700 | Russians |
| 9 | YuriCountry | 2000 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 0 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Mastermind Exposed,0 |
| 1 | Base 1 Down,0 |
| 2 | Base 2 Down,0 |
| 3 | Base 3 Down,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [It's Over : ( (0B1E809C)](#trigger-0b1e809c) | Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians). | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser. |
| [It's Over! 2 (068847BC)](#trigger-068847bc) | 8 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner. |

## Every trigger, in file order

<a id="trigger-0923103c"></a>

### 1. _welcome! - 0923103C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09231D4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable player input.
2. Play in-game movie 52.
3. Enable and reset applicable timers for [_welcome! unlock (09231BFC)](#trigger-09231bfc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4032, Events line 4115, Actions line 4198.

<a id="trigger-09231bfc"></a>

### 2. _welcome! unlock - 09231BFC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome! (0923103C)](#trigger-0923103c).

Attached scope: tag definitions 09232F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 119 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Play voice notification EVA_BattlefieldControlOnline.
3. Create/recruit team [_BaseDef1 (0890193C)](sov06lmd-teams.md#team-0890193c).
4. Create/recruit team [_BaseDef2 (0890148C)](sov06lmd-teams.md#team-0890148c).
5. AI triggers begin: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
6. Create/recruit team [_BaseDef-Left1 (092BA62C)](sov06lmd-teams.md#team-092ba62c).
7. Create/recruit team [_BaseDef-Left2 (092BB81C)](sov06lmd-teams.md#team-092bb81c).
8. Create/recruit team [_BaseDef-Right1 (0BE0132C)](sov06lmd-teams.md#team-0be0132c).
9. Create/recruit team [_BaseDef-Right2 (0BE0351C)](sov06lmd-teams.md#team-0be0351c).
10. Production Begins: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
11. Enable and reset applicable timers for [It's Over : ( (0B1E809C)](#trigger-0b1e809c).
12. Enable and reset applicable timers for [_welcome teams (069BBD3C)](#trigger-069bbd3c).
13. Enable and reset applicable timers for [Place to Build (077B9E1C)](#trigger-077b9e1c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4033, Events line 4116, Actions line 4199.

<a id="trigger-0b1e809c"></a>

### 3. It's Over : ( - 0B1E809C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome! unlock (09231BFC)](#trigger-09231bfc).

Attached scope: tag definitions 0B1F4C7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4034, Events line 4117, Actions line 4200.

<a id="trigger-069bbd3c"></a>

### 4. _welcome teams - 069BBD3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome! unlock (09231BFC)](#trigger-09231bfc).

Attached scope: tag definitions 069BB59C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Laser Jerks Easy (09847DFC)](#trigger-09847dfc).
2. Enable and reset applicable timers for [Laser Jerks Medium (0984778C)](#trigger-0984778c).
3. Enable and reset applicable timers for [Laser Jerks Hard (0B99436C)](#trigger-0b99436c).
4. Enable and reset applicable timers for [Tons O Mooners 2 (0B9B744C)](#trigger-0b9b744c).
5. Enable and reset applicable timers for [Tons O Mooners Easy (09847C7C)](#trigger-09847c7c).
6. Enable and reset applicable timers for [Tons O Mooners Medium (0984721C)](#trigger-0984721c).
7. Enable and reset applicable timers for [Tons O Mooners Hard (0B9A36DC)](#trigger-0b9a36dc).
8. Enable and reset applicable timers for [Mastermind 1 (0C746A2C)](#trigger-0c746a2c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4035, Events line 4118, Actions line 4201.

<a id="trigger-077b9e1c"></a>

### 5. Place to Build - 077B9E1C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome! unlock (09231BFC)](#trigger-09231bfc).

Attached scope: tag definitions 077B953C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS6_ZofiaGoToTheEast.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4036, Events line 4119, Actions line 4202.

<a id="trigger-09847dfc"></a>

### 6. Laser Jerks Easy - 09847DFC

Owner reference: Alliance. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome teams (069BBD3C)](#trigger-069bbd3c).

Attached scope: tag definitions 09847AEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 500 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Laser Jerks (099A9B7C)](sov06lmd-teams.md#team-099a9b7c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4037, Events line 4120, Actions line 4203.

<a id="trigger-0984778c"></a>

### 7. Laser Jerks Medium - 0984778C

Owner reference: Alliance. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome teams (069BBD3C)](#trigger-069bbd3c).

Attached scope: tag definitions 098476AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 300 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Laser Jerks (099A9B7C)](sov06lmd-teams.md#team-099a9b7c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4038, Events line 4121, Actions line 4204.

<a id="trigger-0b99436c"></a>

### 8. Laser Jerks Hard - 0B99436C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome teams (069BBD3C)](#trigger-069bbd3c).

Attached scope: tag definitions 0B992C7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 200 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Laser Jerks (099A9B7C)](sov06lmd-teams.md#team-099a9b7c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4039, Events line 4122, Actions line 4205.

<a id="trigger-0b9b744c"></a>

### 9. Tons O Mooners 2 - 0B9B744C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome teams (069BBD3C)](#trigger-069bbd3c).

Attached scope: tag definitions 0B9B710C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 325 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Tons O Mooners 2 (08900EFC)](sov06lmd-teams.md#team-08900efc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4040, Events line 4123, Actions line 4206.

<a id="trigger-09847c7c"></a>

### 10. Tons O Mooners Easy - 09847C7C

Owner reference: Alliance. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome teams (069BBD3C)](#trigger-069bbd3c).

Attached scope: tag definitions 0CA1409C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 350 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Tons O Mooners (089037DC)](sov06lmd-teams.md#team-089037dc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4041, Events line 4124, Actions line 4207.

<a id="trigger-0984721c"></a>

### 11. Tons O Mooners Medium - 0984721C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome teams (069BBD3C)](#trigger-069bbd3c).

Attached scope: tag definitions 0983FE6C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 300 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Tons O Mooners (089037DC)](sov06lmd-teams.md#team-089037dc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4042, Events line 4125, Actions line 4208.

<a id="trigger-0b9a36dc"></a>

### 12. Tons O Mooners Hard - 0B9A36DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome teams (069BBD3C)](#trigger-069bbd3c).

Attached scope: tag definitions 0B9B604C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 175 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Tons O Mooners (089037DC)](sov06lmd-teams.md#team-089037dc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4043, Events line 4126, Actions line 4209.

<a id="trigger-0c746a2c"></a>

### 13. Mastermind 1 - 0C746A2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome teams (069BBD3C)](#trigger-069bbd3c).

Attached scope: tag definitions 0C7464AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 400 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [MasterMind 1 (0890063C)](sov06lmd-teams.md#team-0890063c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4044, Events line 4127, Actions line 4210.

<a id="trigger-0d6bf95c"></a>

### 14. Yuri Cash Taunt - 0D6BF95C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D6BF7EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The trigger owner's credits are below 10000.

**Then perform these actions in order:**

1. Play voice notification Mis_xs6_YuriCashTaunt.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4045, Events line 4128, Actions line 4211.

<a id="trigger-0ba3216c"></a>

### 15. Yuri Taunt Hideaway - 0BA3216C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner Americans, cell (81, 108), tag 0BA3B1CC, persistence mode 0; Psychic Tower (YAPSYT), owner Americans, cell (84, 102), tag 0BA3B1CC, persistence mode 0; Psychic Tower (YAPSYT), owner Americans, cell (77, 92), tag 0BA3B1CC, persistence mode 0; Psychic Tower (YAPSYT), owner Americans, cell (69, 95), tag 0BA3B1CC, persistence mode 0; Bio Reactor (YAPOWR), owner Americans, cell (65, 99), tag 0BA3B1CC, persistence mode 0; Psychic Tower (YAPSYT), owner YuriCountry, cell (41, 47), tag 0BA3B1CC, persistence mode 0; Bio Reactor (YAPOWR), owner Alliance, cell (78, 58), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner Alliance, cell (76, 54), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner Alliance, cell (90, 66), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner Alliance, cell (81, 64), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner Alliance, cell (84, 66), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner Alliance, cell (77, 45), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner Alliance, cell (94, 61), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (31, 61), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (38, 53), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (44, 44), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (50, 43), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (55, 38), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (57, 32), tag 0BA3B1CC, persistence mode 0; Bio Reactor (YAPOWR), owner Americans, cell (77, 110), tag 0BA3B1CC, persistence mode 0; Gattling Cannon (YAGGUN), owner YuriCountry, cell (63, 28), tag 0BA3B1CC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play voice notification Mis_xs6_YuriScreamTaunt.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4046, Events line 4129, Actions line 4212.

<a id="trigger-0bbde20c"></a>

### 16. Enemy Russia - 0BBDE20C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BBEE10C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4047, Events line 4130, Actions line 4213.

<a id="trigger-0bbf018c"></a>

### 17. Enemy Russia 2 - 0BBF018C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BBF414C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4048, Events line 4131, Actions line 4214.

<a id="trigger-0bbde11c"></a>

### 18. Enemy Russia 3 - 0BBDE11C

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BBF221C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4049, Events line 4132, Actions line 4215.

<a id="trigger-092630bc"></a>

### 19. Limited Troops 1a - 092630BC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Limited Troops 1 (08B7F03C)](#trigger-08b7f03c).

Attached scope: tag definitions 092601CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 53.
2. Enable and reset applicable timers for [Limited Troops 2 (0B0BDBBC)](#trigger-0b0bdbbc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4050, Events line 4133, Actions line 4216.

<a id="trigger-0b0bdbbc"></a>

### 20. Limited Troops 2 - 0B0BDBBC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Limited Troops 1a (092630BC)](#trigger-092630bc).

Attached scope: tag definitions 0B0BD53C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 32 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Limited Troops 2a (08DBCDCC)](#trigger-08dbcdcc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4051, Events line 4134, Actions line 4217.

<a id="trigger-08dbcdcc"></a>

### 21. Limited Troops 2a - 08DBCDCC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Limited Troops 2 (0B0BDBBC)](#trigger-0b0bdbbc).

Attached scope: tag definitions 08DBC7FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification S06_p02.
2. Switch the sidebar to tab 2.
3. Flash cameo/type LUNR; additional configured duration/location argument 90.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4052, Events line 4135, Actions line 4218.

<a id="trigger-077b937c"></a>

### 22. No Resources - 077B937C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [No Resources 0 (084F7E0C)](#trigger-084f7e0c).

Attached scope: tag definitions 077BBE7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS6_ZofiaNoResources.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4053, Events line 4136, Actions line 4219.

<a id="trigger-0ba3903c"></a>

### 23. Start Suprise 1 - 0BA3903C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 29 tagged map cells: (113, 109), (114, 109), (111, 110), (112, 110), (113, 110), (114, 110), (112, 111), (113, 111), (114, 111), (109, 112), (110, 112), (111, 112), (112, 112), (113, 112), (114, 112), (108, 113), (109, 113), (110, 113), (111, 113), (112, 113), (113, 113), (114, 113), (111, 114), (112, 114), (113, 114), (114, 114), (111, 115), (112, 115), (113, 115); tag 0BA3C08C, persistence mode 0.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Supply reinforcement team [_ScareTeam1 (08900CBC)](sov06lmd-teams.md#team-08900cbc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4054, Events line 4137, Actions line 4220.

<a id="trigger-091bcb2c"></a>

### 24. Start Suprise 2 - 091BCB2C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 25 tagged map cells: (69, 63), (65, 65), (71, 65), (66, 67), (68, 67), (70, 67), (62, 68), (65, 68), (67, 68), (68, 68), (73, 68), (64, 69), (63, 70), (70, 70), (71, 70), (66, 71), (69, 71), (69, 72), (72, 72), (73, 72), (63, 73), (65, 73), (67, 73), (70, 74), (67, 75); tag 091BC62C, persistence mode 0.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Supply reinforcement team [_ScareTeam2 (091BD49C)](sov06lmd-teams.md#team-091bd49c).
2. Supply reinforcement team [_ScareTeam3 (091BAD9C)](sov06lmd-teams.md#team-091bad9c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4055, Events line 4138, Actions line 4221.

<a id="trigger-0bcef55c"></a>

### 25. Kill Suprise 2 - 0BCEF55C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 28 tagged map cells: (40, 63), (41, 63), (42, 63), (43, 63), (44, 63), (45, 63), (46, 63), (47, 63), (40, 64), (47, 64), (40, 65), (47, 65), (40, 66), (47, 66), (40, 67), (47, 67), (40, 68), (47, 68), (40, 69), (47, 69), (40, 70), (41, 70), (42, 70), (43, 70), (44, 70), (45, 70), (46, 70), (47, 70); tag 0BCF4DCC, persistence mode 0.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Disable [Start Suprise 2 (091BCB2C)](#trigger-091bcb2c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4056, Events line 4139, Actions line 4222.

<a id="trigger-0b99bbfc"></a>

### 26. Gattling Isn't For The Weak - 0B99BBFC

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B99B67C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 500 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Gattling Isn't For The Weak (089046CC)](sov06lmd-teams.md#team-089046cc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4057, Events line 4140, Actions line 4223.

<a id="trigger-0b1ee03c"></a>

### 27. It's Over! - 0B1EE03C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Fire Sale Countdown (09078A2C)](#trigger-09078a2c).

Attached scope: tag definitions 0B1EF03C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_YuriInevitable.
2. Enable and reset applicable timers for [It's Over! 2 (068847BC)](#trigger-068847bc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4058, Events line 4141, Actions line 4224.

<a id="trigger-068847bc"></a>

### 28. It's Over! 2 - 068847BC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [It's Over! (0B1EE03C)](#trigger-0b1ee03c).

Attached scope: tag definitions 06885E4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4059, Events line 4142, Actions line 4225.

<a id="trigger-0bf1bb4c"></a>

### 29. Kill Suprise 1 - 0BF1BB4C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 30 tagged map cells: (91, 114), (92, 114), (93, 114), (94, 114), (95, 114), (96, 114), (97, 114), (98, 114), (91, 115), (98, 115), (91, 116), (98, 116), (91, 117), (98, 117), (91, 118), (98, 118), (91, 119), (98, 119), (91, 120), (93, 120), (94, 120), (98, 120), (91, 121), (92, 121), (93, 121), (94, 121), (95, 121), (96, 121), (97, 121), (98, 121); tag 0BF1B55C, persistence mode 0.

**Wait for the recorded events:**

1. Entered or Overflown By: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Disable [Start Suprise 1 (0BA3903C)](#trigger-0ba3903c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4060, Events line 4143, Actions line 4226.

<a id="trigger-0bfccf3c"></a>

### 30. _Don't Stop Lasers - 0BFCCF3C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Start Don't Stop Lasers (0BFC984C)](#trigger-0bfc984c).

Attached scope: tag definitions 0BFC912C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 500 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [_Don't Stop Lasers (08908B5C)](sov06lmd-teams.md#team-08908b5c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4061, Events line 4144, Actions line 4227.

<a id="trigger-0bfc984c"></a>

### 31. _Start Don't Stop Lasers - 0BFC984C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BFCA0DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Don't Stop Lasers (0BFCCF3C)](#trigger-0bfccf3c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4062, Events line 4145, Actions line 4228.

<a id="trigger-0bfcaf3c"></a>

### 32. Barracks Gone - 0BFCAF3C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Barracks (YABRCK), owner YuriCountry, cell (23, 46), tag 0BFCAB9C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Kill Blue Light 5 (090EB69C)](#trigger-090eb69c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4063, Events line 4146, Actions line 4229.

<a id="trigger-090eb69c"></a>

### 33. Kill Blue Light 5 - 090EB69C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Barracks Gone (0BFCAF3C)](#trigger-0bfcaf3c).

Attached scope: Invisible Blue Light Post (INBLULMP), owner Neutral, cell (21, 46), tag 090EB45C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4064, Events line 4147, Actions line 4230.

<a id="trigger-0c04613c"></a>

### 34. _Extra Taunt - 0C04613C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C04049C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Play voice notification Mis_xA3_YuriTaunt.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4065, Events line 4148, Actions line 4231.

<a id="trigger-0c04667c"></a>

### 35. _Extra Taunt 2 - 0C04667C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C04514C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

**Then perform these actions in order:**

1. Play voice notification Mis_xS3_YuriLeave.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4066, Events line 4149, Actions line 4232.

<a id="trigger-0c9d724c"></a>

### 36. Protect Lunar Base - 0C9D724C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CA0E59C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_S06_MM Guard LB AA (069E632C)](sov06lmd-teams.md#team-069e632c).
2. Create/recruit team [_S06_MM Guard LB Z (069E67DC)](sov06lmd-teams.md#team-069e67dc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4067, Events line 4150, Actions line 4233.

<a id="trigger-0c994d4c"></a>

### 37. Revealing Shroud - 0C994D4C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C993F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 0 (cell 118, 145).
2. Reveal terrain around waypoint 5 (cell 124, 143).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4068, Events line 4151, Actions line 4234.

<a id="trigger-0994531c"></a>

### 38. Objective 1 - 0994531C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09944D7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Find a location to set up base” (MISSION:BuildBase).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4069, Events line 4152, Actions line 4235.

<a id="trigger-09944c8c"></a>

### 39. Objective 2 - 09944C8C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Soviet MCV Exists (0994422C)](#trigger-0994422c).

Attached scope: tag definitions 09944A4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Locate and destroy Yuri's Lunar Command Center” (MISSION:DestroyLunarCommand).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4070, Events line 4153, Actions line 4236.

<a id="trigger-0994495c"></a>

### 40. Objective 3 - 0994495C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Lunar Command Gone (0994462C)](#trigger-0994462c); enable from [Lunar Destroyed (0951F89C)](#trigger-0951f89c).

Attached scope: tag definitions 0994471C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Destroy all remaining Yuri buildings” (MISSION:DestroyYuri06S).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4071, Events line 4154, Actions line 4237.

<a id="trigger-0994462c"></a>

### 41. Lunar Command Gone - 0994462C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0994431C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Objective 2 (09944C8C)](#trigger-09944c8c).
2. Enable and reset applicable timers for [Objective 3 (0994495C)](#trigger-0994495c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4072, Events line 4155, Actions line 4238.

<a id="trigger-0994422c"></a>

### 42. Soviet MCV Exists - 0994422C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09943E7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. At least 1 instances of Soviet Construction Yard (NACNST) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Disable [Objective 1 (0994531C)](#trigger-0994531c).
2. Enable and reset applicable timers for [Objective 2 (09944C8C)](#trigger-09944c8c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4073, Events line 4156, Actions line 4239.

<a id="trigger-0951f89c"></a>

### 43. Lunar Destroyed - 0951F89C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri´s Command Center (YACOMD), owner YuriCountry, cell (45, 14), tag 0951F21C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Objective 1 (0994531C)](#trigger-0994531c).
2. Disable [Objective 2 (09944C8C)](#trigger-09944c8c).
3. Enable and reset applicable timers for [Objective 3 (0994495C)](#trigger-0994495c).
4. Play voice notification Mis_xS6_ZofiaWellDone.
5. Display message “Objective: Destroy all remaining Yuri buildings” (MISSION:DestroyYuri06S).
6. Enable and reset applicable timers for [Kill Blue Light 3 (090EC3FC)](#trigger-090ec3fc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4074, Events line 4157, Actions line 4240.

<a id="trigger-090ec3fc"></a>

### 44. Kill Blue Light 3 - 090EC3FC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Lunar Destroyed (0951F89C)](#trigger-0951f89c).

Attached scope: Invisible Blue Light Post (INBLULMP), owner Neutral, cell (46, 12), tag 090EC1BC, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4075, Events line 4158, Actions line 4241.

<a id="trigger-079e07ec"></a>

### 45. Demo Floating Disk 1 - 079E07EC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Demo Floating Disk 0 (095408BC)](#trigger-095408bc).

Attached scope: tag definitions 079E22EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_S06_Demo Floating Disk (08F7BDEC)](sov06lmd-teams.md#team-08f7bdec).
2. Enable and reset applicable timers for [Floating Disk Timer (0915944C)](#trigger-0915944c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4076, Events line 4159, Actions line 4242.

<a id="trigger-0915944c"></a>

### 46. Floating Disk Timer - 0915944C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Demo Floating Disk 1 (079E07EC)](#trigger-079e07ec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 70 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Demo Floating Disk 2 (079E21FC)](#trigger-079e21fc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4077, Events line 4160, Actions line 4243.

<a id="trigger-079e21fc"></a>

### 47. Demo Floating Disk 2 - 079E21FC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Floating Disk Timer (0915944C)](#trigger-0915944c); enable from [Shot On (05A800AC)](#trigger-05a800ac).

Attached scope: tag definitions 079E38CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash team [_S06_Demo Floating Disk (08F7BDEC)](sov06lmd-teams.md#team-08f7bdec) with duration setting 90.
2. Play voice notification Unit_Sofia_FloatDisc.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4078, Events line 4161, Actions line 4244.

<a id="trigger-08daaadc"></a>

### 48. _welcome! Mastermind - 08DAAADC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DAB9BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 58 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_S06_Mastermind Intro (0853DB7C)](sov06lmd-teams.md#team-0853db7c).
2. Enable and reset applicable timers for [_welcome! MM Speech (08EFDB7C)](#trigger-08efdb7c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4079, Events line 4162, Actions line 4245.

<a id="trigger-08efdb7c"></a>

### 49. _welcome! MM Speech - 08EFDB7C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome! Mastermind (08DAAADC)](#trigger-08daaadc).

Attached scope: tag definitions 08EFD47C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash team [_S06_Mastermind Intro (0853DB7C)](sov06lmd-teams.md#team-0853db7c) with duration setting 90.
2. Play voice notification Unit_Sofia_MasterMind.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4080, Events line 4163, Actions line 4246.

<a id="trigger-08dab8cc"></a>

### 50. _welcome! Mag Speech - 08DAB8CC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_welcome! Magentron (043FDD9C)](#trigger-043fdd9c).

Attached scope: tag definitions 08DAB71C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS6_ZofiaMagnetronIntro.
2. Flash team [_S06_Magnetron Start (0A2A809C)](sov06lmd-teams.md#team-0a2a809c) with duration setting 90.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4081, Events line 4164, Actions line 4247.

<a id="trigger-08dab62c"></a>

### 51. _welcome!zzz - 08DAB62C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DAB4BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

No action entries.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4082, Events line 4165, Actions line 4248.

<a id="trigger-043feb4c"></a>

### 52. _welcome! rhinos - 043FEB4C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043FAB6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [S6_start_rhino (08B506CC)](sov06lmd-teams.md#team-08b506cc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4083, Events line 4166, Actions line 4249.

<a id="trigger-043fdd9c"></a>

### 53. _welcome! Magentron - 043FDD9C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043FDBEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 44 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 36 (cell 114, 129).
2. Create/recruit team [_S06_Magnetron Start (0A2A809C)](sov06lmd-teams.md#team-0a2a809c).
3. Enable and reset applicable timers for [_welcome! Mag Speech (08DAB8CC)](#trigger-08dab8cc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4084, Events line 4167, Actions line 4250.

<a id="trigger-05e805ac"></a>

### 54. _welcome! Cosmonaunts - 05E805AC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05E81CDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [S6_start_moontroops (0932B32C)](sov06lmd-teams.md#team-0932b32c).
2. Supply reinforcement team [S6_Moontroops 2 (0C430EFC)](sov06lmd-teams.md#team-0c430efc).
3. Supply reinforcement team [S6_Moontroops 3 (043A463C)](sov06lmd-teams.md#team-043a463c).
4. Supply reinforcement team [S6_Moontroops 4 (043AF7DC)](sov06lmd-teams.md#team-043af7dc).
5. Supply reinforcement team [S6_Moontroops 5 (0932712C)](sov06lmd-teams.md#team-0932712c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4085, Events line 4168, Actions line 4251.

<a id="trigger-05e81bec"></a>

### 55. _welcome! MCV - 05E81BEC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05E8134C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [S6_start_MCV (0C65889C)](sov06lmd-teams.md#team-0c65889c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4086, Events line 4169, Actions line 4252.

<a id="trigger-05e9bcac"></a>

### 56. _welcome! Cos Attack - 05E9BCAC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05E9B72C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_S06_Cos Attack (08EC7C8C)](sov06lmd-teams.md#team-08ec7c8c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4087, Events line 4170, Actions line 4253.

<a id="trigger-08aad06c"></a>

### 57. Kill Blue Light 1 - 08AAD06C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Blue Light Post (INBLULMP), owner Neutral, cell (68, 104), tag 08EEA05C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4088, Events line 4171, Actions line 4254.

<a id="trigger-090ecf3c"></a>

### 58. Kill Blue Light 2 - 090ECF3C

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Blue Light Post (INBLULMP), owner Neutral, cell (88, 51), tag 090EC9EC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4089, Events line 4172, Actions line 4255.

<a id="trigger-090ebe6c"></a>

### 59. Kill Blue Light 4 - 090EBE6C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri MCV Gone (090EBABC)](#trigger-090ebabc).

Attached scope: Invisible Blue Light Post (INBLULMP), owner Neutral, cell (26, 23), tag 090EBC2C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4090, Events line 4173, Actions line 4256.

<a id="trigger-090ebabc"></a>

### 60. Yuri MCV Gone - 090EBABC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Construction Yard (YACNST), owner YuriCountry, cell (28, 26), tag 090EB87C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Kill Blue Light 4 (090EBE6C)](#trigger-090ebe6c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4091, Events line 4174, Actions line 4257.

<a id="trigger-096c769c"></a>

### 61. Show the base! - 096C769C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096C732C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 78 (cell 45, 12).
2. Reveal terrain around waypoint 80 (cell 43, 18).
3. Reveal terrain around waypoint 81 (cell 51, 18).
4. Move the camera to waypoint 78 (cell 45, 12) with speed setting 3.
5. Enable and reset applicable timers for [Show the base! 2 (096E96AC)](#trigger-096e96ac).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4092, Events line 4175, Actions line 4258.

<a id="trigger-096e96ac"></a>

### 62. Show the base! 2 - 096E96AC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Show the base! (096C769C)](#trigger-096c769c).

Attached scope: tag definitions 096E92CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 22 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 33 (cell 116, 136) with speed setting 3.

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4093, Events line 4176, Actions line 4259.

<a id="trigger-0907e1dc"></a>

### 63. Fire Sale - 0907E1DC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09078B1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Base 1 Down) is set.
2. local flag 2 (Base 2 Down) is set.
3. local flag 3 (Base 3 Down) is set.

Flag writers in this mission: set local flag 1 (Base 1 Down) at [Fire Sale A (08B8E03C)](#trigger-08b8e03c); set local flag 2 (Base 2 Down) at [Fire Sale B (08BE205C)](#trigger-08be205c); set local flag 3 (Base 3 Down) at [Fire Sale C (08BEB06C)](#trigger-08beb06c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Fire Sale Countdown (09078A2C)](#trigger-09078a2c).
2. Disable [_Extra Taunt (0C04613C)](#trigger-0c04613c).
3. Disable [_Extra Taunt 2 (0C04667C)](#trigger-0c04667c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4094, Events line 4177, Actions line 4260.

<a id="trigger-09078a2c"></a>

### 64. Fire Sale Countdown - 09078A2C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Fire Sale (0907E1DC)](#trigger-0907e1dc).

Attached scope: tag definitions 090787EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Enable and reset applicable timers for [Fire Sale - 2 Alliance (07B9CE5C)](#trigger-07b9ce5c).
3. Enable and reset applicable timers for [Fire Sale - 1 America (07B9BA5C)](#trigger-07b9ba5c).
4. Enable and reset applicable timers for [Fire Sale Countdown 2 (0782720C)](#trigger-0782720c).
5. Enable and reset applicable timers for [It's Over! (0B1EE03C)](#trigger-0b1ee03c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4095, Events line 4178, Actions line 4261.

<a id="trigger-07b9ce5c"></a>

### 65. Fire Sale - 2 Alliance - 07B9CE5C

Owner reference: Alliance. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Fire Sale Countdown (09078A2C)](#trigger-09078a2c).

Attached scope: tag definitions 07B9CCAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4096, Events line 4179, Actions line 4262.

<a id="trigger-07b9ba5c"></a>

### 66. Fire Sale - 1 America - 07B9BA5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Fire Sale Countdown (09078A2C)](#trigger-09078a2c).

Attached scope: tag definitions 07B9CF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4097, Events line 4180, Actions line 4263.

<a id="trigger-0782720c"></a>

### 67. Fire Sale Countdown 2 - 0782720C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Fire Sale Countdown (09078A2C)](#trigger-09078a2c).

Attached scope: tag definitions 07826B8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy all of: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Enable and reset applicable timers for [Fire Sale Countdown 2b (09A0EC1C)](#trigger-09a0ec1c).
3. Enable and reset applicable timers for [Fire Sale Countdown 2a (09A0C36C)](#trigger-09a0c36c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4098, Events line 4181, Actions line 4264.

<a id="trigger-09a0ec1c"></a>

### 68. Fire Sale Countdown 2b - 09A0EC1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Fire Sale Countdown 2 (0782720C)](#trigger-0782720c).

Attached scope: tag definitions 09A0A4AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy all of: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4099, Events line 4182, Actions line 4265.

<a id="trigger-09a0c36c"></a>

### 69. Fire Sale Countdown 2a - 09A0C36C

Owner reference: Alliance. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Fire Sale Countdown 2 (0782720C)](#trigger-0782720c).

Attached scope: tag definitions 09A0ED0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy all of: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4100, Events line 4183, Actions line 4266.

<a id="trigger-093bdcbc"></a>

### 70. More Rhinos - 093BDCBC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 093BD66C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [S6_start_rhino (08B506CC)](sov06lmd-teams.md#team-08b506cc).
2. Supply reinforcement team [S6_start_rhino (08B506CC)](sov06lmd-teams.md#team-08b506cc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4101, Events line 4184, Actions line 4267.

<a id="trigger-05e4bf3c"></a>

### 71. Production - 05E4BF3C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05E4BA5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Production Begins: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4102, Events line 4185, Actions line 4268.

<a id="trigger-08916d7c"></a>

### 72. Bonus Money 1 - 08916D7C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089167FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 16 (cell 75, 101).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4103, Events line 4186, Actions line 4269.

<a id="trigger-0891670c"></a>

### 73. Bonus Money 2 - 0891670C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089164CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 13 (cell 86, 54).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4104, Events line 4187, Actions line 4270.

<a id="trigger-08b7f03c"></a>

### 74. Limited Troops 1 - 08B7F03C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B86F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 11 (global list position: Soviet Barracks (NAHAND)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Limited Troops 1a (092630BC)](#trigger-092630bc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4105, Events line 4188, Actions line 4271.

<a id="trigger-084f7e0c"></a>

### 75. No Resources 0 - 084F7E0C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 084F1DAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 14 (global list position: Soviet War Factory (NAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [No Resources (077B937C)](#trigger-077b937c).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4106, Events line 4189, Actions line 4272.

<a id="trigger-08b8e03c"></a>

### 76. Fire Sale A - 08B8E03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B9604C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 302 (global list position: Bio Reactor (YAPOWR)). A map-local type-list change can affect index interpretation.
2. Building does not exist: type index 300 (global list position: Bus Stop (CASTRT05)). A map-local type-list change can affect index interpretation.
3. Building does not exist: type index 303 (global list position: Yuri Barracks (YABRCK)). A map-local type-list change can affect index interpretation.
4. Building does not exist: type index 301 (global list position: Yuri Construction Yard (YACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 1 (Base 1 Down).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4107, Events line 4190, Actions line 4273.

<a id="trigger-08be205c"></a>

### 77. Fire Sale B - 08BE205C

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08BEE06C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 302 (global list position: Bio Reactor (YAPOWR)). A map-local type-list change can affect index interpretation.
2. Building does not exist: type index 303 (global list position: Yuri Barracks (YABRCK)). A map-local type-list change can affect index interpretation.
3. Building does not exist: type index 301 (global list position: Yuri Construction Yard (YACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 2 (Base 2 Down).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4108, Events line 4191, Actions line 4274.

<a id="trigger-08beb06c"></a>

### 78. Fire Sale C - 08BEB06C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08BF607C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 302 (global list position: Bio Reactor (YAPOWR)). A map-local type-list change can affect index interpretation.
2. Building does not exist: type index 354 (global list position: MassiveSoft Campus (CASEAT02)). A map-local type-list change can affect index interpretation.
3. Building does not exist: type index 300 (global list position: Bus Stop (CASTRT05)). A map-local type-list change can affect index interpretation.
4. Building does not exist: type index 303 (global list position: Yuri Barracks (YABRCK)). A map-local type-list change can affect index interpretation.
5. Building does not exist: type index 301 (global list position: Yuri Construction Yard (YACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 3 (Base 3 Down).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4109, Events line 4192, Actions line 4275.

<a id="trigger-095408bc"></a>

### 79. Demo Floating Disk 0 - 095408BC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09544C9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 14 (global list position: Soviet War Factory (NAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Demo Floating Disk 1 (079E07EC)](#trigger-079e07ec).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4110, Events line 4193, Actions line 4276.

<a id="trigger-05a800ac"></a>

### 80. Shot On - 05A800AC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Floating Disk Timer (0915944C)](#trigger-0915944c).

Attached scope: tag definitions 0915BD6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Demo Floating Disk 2 (079E21FC)](#trigger-079e21fc).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4111, Events line 4194, Actions line 4277.

<a id="trigger-07706adc"></a>

### 81. Yuri Hates Russia - 07706ADC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0770661C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: mapsmd03.mix/sov06lmd.map; Triggers line 4112, Events line 4195, Actions line 4278.

[All team rosters and ordered plans](sov06lmd-teams.md) | [All mission overrides](sov06lmd-overrides.md)
