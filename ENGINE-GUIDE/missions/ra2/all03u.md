# Operation: Hail to the Chief

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for all03u.map.](../../images/map-all03u.svg)

*Initial placement schematic for all03u.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** all03u.map. **Effective extracted member:** MAPS01.MIX/all03u.map. **Trigger definitions:** 62.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all03u-teams.md) | [All mission overrides](all03u-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | URBAN |
| Map size | 0,0,77,105 |
| Visible local rectangle | 6,4,69,84 |
| Placed vehicles | 21 |
| Placed infantry | 52 |
| Placed structures | 111 |
| Placed aircraft | 0 |
| Team templates | 58 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | Russian1 House | 300 | Russian1 |
| 2 | Russian2 House | 200 | Russian2 |
| 3 | CivilianArmy House | 100 | CivilianArmy |
| 4 | Civilian1 House | 0 | Civilian1 |
| 5 | Other1 House | 20 | Other1 |
| 6 | Other2 House | 20 | Other2 |
| 7 | Civilian2 House | 0 | Civilian2 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Bridge1Open,1 |
| 1 | Bridge2Open,1 |
| 2 | Bridge3Open,1 |
| 3 | BackBridgeOpen,1 |
| 4 | IFVRepaired,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [PlayerDestroyed (0B71A25C)](#trigger-0b71a25c) | Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House). | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [WhiteHouseDestroyed (0B71C87C)](#trigger-0b71c87c) | Destroyed by anything. See attached-object/cell scope below. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [GameEnds (0AC2BA3C)](#trigger-0ac2ba3c) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-0e0f0110"></a>

### 1. BeaconDestroyed - 0E0F0110

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Beacon (NAPSYB), owner Russian1 House, cell (75, 34), tag 0E0F1280, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [MoveCam2WhiteHouse (08C7072C)](#trigger-08c7072c).
2. Disable [PlayerDestroyed (0B71A25C)](#trigger-0b71a25c).
3. Disable [WhiteHouseDestroyed (0B71C87C)](#trigger-0b71c87c).
4. Make ally: owner selector 13 (country/type PLAYER; placed owner Player House).
5. Disable player input.
6. Disable [ProtectWhiteHouseHint (0BEFBD5C)](#trigger-0befbd5c).
7. Destroy current instances of [RepeatObjective (0B58A03C)](#trigger-0b58a03c).
8. Disable [Hint-IFV -- pt1 (0BF57ABC)](#trigger-0bf57abc).
9. Disable [EnemyGarrisonHint (0B82203C)](#trigger-0b82203c).
10. Disable [Hint-RepairBuildings (0B26E24C)](#trigger-0b26e24c).
11. Disable [ShockTrooperHint-pt1 (0B71BBFC)](#trigger-0b71bbfc).
12. Disable [ShockTrooperHint-pt2 (086B4E5C)](#trigger-086b4e5c).
13. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).
14. Disable [PingObjective (0B2E0B6C)](#trigger-0b2e0b6c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5530, Events line 5594, Actions line 5658.

<a id="trigger-08c7072c"></a>

### 2. MoveCam2WhiteHouse - 08C7072C

Owner reference: Russian2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BeaconDestroyed (0E0F0110)](#trigger-0e0f0110).

Attached scope: tag definitions 08C7064C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 22 (cell 79, 17) with speed setting 4.
2. Reveal terrain around waypoint 22 (cell 79, 17).
3. Enable and reset applicable timers for [SSExit-CopterFliesOn (0AC0AB8C)](#trigger-0ac0ab8c).
4. Make ally: owner selector 13 (country/type PLAYER; placed owner Player House).
5. Play voice notification EVA_PrimaryObjectiveAchieved.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5531, Events line 5595, Actions line 5659.

<a id="trigger-0b71a25c"></a>

### 3. PlayerDestroyed - 0B71A25C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B71A05C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5532, Events line 5596, Actions line 5660.

<a id="trigger-0b71c87c"></a>

### 4. WhiteHouseDestroyed - 0B71C87C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: White House (CAWASH01), owner Civilian1 House, cell (77, 13), tag 0B71C39C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.
2. Display message “MISSION FAILED: Nice job commander. You've managed to crush the President under a huge slab of concrete...” (MISSION:All03e).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5533, Events line 5597, Actions line 5661.

<a id="trigger-0befbd5c"></a>

### 5. ProtectWhiteHouseHint - 0BEFBD5C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Fountain (CAWASH18), owner Civilian1 House, cell (78, 21), tag 0BEFB9BC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “HINT: Be careful NOT to destroy the White House... we don't want to endanger the President” (MISSION:All03d).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5534, Events line 5598, Actions line 5662.

<a id="trigger-0b58a03c"></a>

### 6. RepeatObjective - 0B58A03C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [StateObjective (0917E3EC)](#trigger-0917e3ec).

Attached scope: tag definitions 0B59004C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Destroy the Psychic Beacon” (MISSION:All03a).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5535, Events line 5599, Actions line 5663.

<a id="trigger-0bf57abc"></a>

### 7. Hint-IFV -- pt1 - 0BF57ABC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BF579DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [FlashIFV1 (0AF2DAFC)](all03u-teams.md#team-0af2dafc).
2. Create/recruit team [FlashIFV2 (0AF2930C)](all03u-teams.md#team-0af2930c).
3. Create/recruit team [FlashIFV3 (0AF2AEFC)](all03u-teams.md#team-0af2aefc).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5536, Events line 5600, Actions line 5664.

<a id="trigger-0b82203c"></a>

### 8. EnemyGarrisonHint - 0B82203C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAWASH10), owner Civilian1 House, cell (103, 49), tag 0B82804C, persistence mode 0; Building (CAWASH03), owner Civilian1 House, cell (119, 94), tag 0B82804C, persistence mode 0; Building (CAWASH04), owner Civilian1 House, cell (102, 35), tag 0B82804C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “HINT: Beware of SOVIET TROOPS garrisoned in CIVILIAN STRUCTURES” (MISSION:All03c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5537, Events line 5601, Actions line 5665.

<a id="trigger-0b26e24c"></a>

### 9. Hint-RepairBuildings - 0B26E24C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Engineer (ENGINEER), owner Player House, cell (79, 123), tag 0B27427C, persistence mode 0.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “HINT: Send an ENGINEER into a damaged CIVILIAN STRUCTURE to repair it” (MISSION:All03f).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5538, Events line 5602, Actions line 5666.

<a id="trigger-0b71bbfc"></a>

### 10. ShockTrooperHint-pt1 - 0B71BBFC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Trooper (SHK), owner Russian2 House, cell (92, 99), tag 0B71BB1C, persistence mode 0; Tesla Trooper (SHK), owner Russian2 House, cell (91, 98), tag 0B71BB1C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [ShockTrooperHint-pt2 (086B4E5C)](#trigger-086b4e5c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5539, Events line 5603, Actions line 5667.

<a id="trigger-086b4e5c"></a>

### 11. ShockTrooperHint-pt2 - 086B4E5C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ShockTrooperHint-pt1 (0B71BBFC)](#trigger-0b71bbfc).

Attached scope: tag definitions 086B4D7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_ShockTrooper.
2. Flash team [ShockAttack-Intro (0C33ADCC)](all03u-teams.md#team-0c33adcc) with duration setting 200.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5540, Events line 5604, Actions line 5668.

<a id="trigger-0b2e0b6c"></a>

### 12. PingObjective - 0B2E0B6C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [StateObjective (0917E3EC)](#trigger-0917e3ec).

Attached scope: tag definitions 0B2E087C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 150 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 57 (cell 75, 34).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5541, Events line 5605, Actions line 5669.

<a id="trigger-0ac0ab8c"></a>

### 13. SSExit-CopterFliesOn - 0AC0AB8C

Owner reference: Other1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [MoveCam2WhiteHouse (08C7072C)](#trigger-08c7072c).

Attached scope: tag definitions 0AC0A3CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [*PresidentialHelicopter (0ECAB6AC)](all03u-teams.md#team-0ecab6ac).
2. Supply reinforcement team [*SecretService1 (0C4EA7DC)](all03u-teams.md#team-0c4ea7dc) at waypoint 62 (cell 78, 17).
3. Supply reinforcement team [*SecretService2 (0C4EA32C)](all03u-teams.md#team-0c4ea32c) at waypoint 22 (cell 79, 17).
4. Enable and reset applicable timers for [PresExits (0C3E51DC)](#trigger-0c3e51dc).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5542, Events line 5606, Actions line 5670.

<a id="trigger-0c3e51dc"></a>

### 14. PresExits - 0C3E51DC

Owner reference: Other1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SSExit-CopterFliesOn (0AC0AB8C)](#trigger-0ac0ab8c).

Attached scope: tag definitions 0C3E50FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [*President (0C4E57BC)](all03u-teams.md#team-0c4e57bc) at waypoint 62 (cell 78, 17).
2. Enable and reset applicable timers for [PlayMovie (03F52A4C)](#trigger-03f52a4c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5543, Events line 5607, Actions line 5671.

<a id="trigger-03f52a4c"></a>

### 15. PlayMovie - 03F52A4C

Owner reference: Other1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PresExits (0C3E51DC)](#trigger-0c3e51dc).

Attached scope: tag definitions 03F528BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 71.
2. Enable and reset applicable timers for [Dugan&SSBoardHeli (0865FC3C)](#trigger-0865fc3c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5544, Events line 5608, Actions line 5672.

<a id="trigger-0865fc3c"></a>

### 16. Dugan&SSBoardHeli - 0865FC3C

Owner reference: Other1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayMovie (03F52A4C)](#trigger-03f52a4c).

Attached scope: tag definitions 0865FF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 34 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [*PresDuganAndHeli (0B88567C)](all03u-teams.md#team-0b88567c).
2. Enable and reset applicable timers for [GameEnds (0AC2BA3C)](#trigger-0ac2ba3c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5545, Events line 5609, Actions line 5673.

<a id="trigger-0ac2ba3c"></a>

### 17. GameEnds - 0AC2BA3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Dugan&SSBoardHeli (0865FC3C)](#trigger-0865fc3c).

Attached scope: tag definitions 0AC2B8AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5546, Events line 5610, Actions line 5674.

<a id="trigger-09ddf1bc"></a>

### 18. Hint-IFV -- pt3 - 09DDF1BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09DDF0DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [UnlockInput (0AFC405C)](#trigger-0afc405c).
2. Display message “HINT: Try putting different INFANTRY in your new IFV to use its morphing ability” (MISSION:All03g).
3. Create/recruit team [Hint(IFV/GI) (0C15D2AC)](all03u-teams.md#team-0c15d2ac).
4. Create/recruit team [Hint(IFV/Engineer) (0C15D3DC)](all03u-teams.md#team-0c15d3dc).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5547, Events line 5611, Actions line 5675.

<a id="trigger-0afc405c"></a>

### 19. UnlockInput - 0AFC405C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint-IFV -- pt3 (09DDF1BC)](#trigger-09ddf1bc).

Attached scope: tag definitions 0AFC004C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 18 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Enable and reset applicable timers for [StateObjective (0917E3EC)](#trigger-0917e3ec).
3. Remove instances of the team organization (not automatically its surviving objects) [Hint(IFV/Engineer) (0C15D3DC)](all03u-teams.md#team-0c15d3dc).
4. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5548, Events line 5612, Actions line 5676.

<a id="trigger-0917e3ec"></a>

### 20. StateObjective - 0917E3EC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [UnlockInput (0AFC405C)](#trigger-0afc405c).

Attached scope: tag definitions 09179E4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Destroy the Psychic Beacon” (MISSION:All03a).
2. Enable and reset applicable timers for [RepeatObjective (0B58A03C)](#trigger-0b58a03c).
3. Enable and reset applicable timers for [PingObjective (0B2E0B6C)](#trigger-0b2e0b6c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5549, Events line 5613, Actions line 5677.

<a id="trigger-07aff9e0"></a>

### 21. CivAttack1 - 07AFF9E0

Owner reference: CivilianArmy. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0809BE80 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [ArmedHordes1 (0B76EA4C)](all03u-teams.md#team-0b76ea4c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5550, Events line 5614, Actions line 5678.

<a id="trigger-095a49f0"></a>

### 22. CivAttack2 - 095A49F0

Owner reference: CivilianArmy. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 095A0B60 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 220 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [ArmedHordes2 (0B76E59C)](all03u-teams.md#team-0b76e59c).
2. Supply reinforcement team [ArmedHordes3 (0A148DCC)](all03u-teams.md#team-0a148dcc).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5551, Events line 5615, Actions line 5679.

<a id="trigger-0adc0f40"></a>

### 23. CivAttack3 - 0ADC0F40

Owner reference: CivilianArmy. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ADC0930 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [ArmedHordes1 (0B76EA4C)](all03u-teams.md#team-0b76ea4c).
2. Supply reinforcement team [ArmedHordes2 (0B76E59C)](all03u-teams.md#team-0b76e59c).
3. Supply reinforcement team [ArmedHordes3 (0A148DCC)](all03u-teams.md#team-0a148dcc).
4. Enable and reset applicable timers for [CivAttackRepeater1 (0ADC0850)](#trigger-0adc0850).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5552, Events line 5616, Actions line 5680.

<a id="trigger-0adc0850"></a>

### 24. CivAttackRepeater1 - 0ADC0850

Owner reference: CivilianArmy. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CivAttack3 (0ADC0F40)](#trigger-0adc0f40).

Attached scope: tag definitions 0ADC0680 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [ArmedHordes3 (0A148DCC)](all03u-teams.md#team-0a148dcc).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5553, Events line 5617, Actions line 5681.

<a id="trigger-079a692c"></a>

### 25. StartProduction1 - 079A692C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079A639C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 470 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type RUSSIAN1; placed owner Russian1 House).
2. AI triggers begin: owner selector 14 (country/type RUSSIAN1; placed owner Russian1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5554, Events line 5618, Actions line 5682.

<a id="trigger-07b3216c"></a>

### 26. RepairBridge - 07B3216C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ReenableRB (0B0B4D0C)](#trigger-0b0b4d0c).

Attached scope: 1 tagged map cells: (98, 115); tag 07B31C8C, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [EngineerBridgeRepair (0B2A832C)](all03u-teams.md#team-0b2a832c).
2. Disable [RepairBridge (07B3216C)](#trigger-07b3216c).
3. Clear local flag 1 (Bridge2Open).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5555, Events line 5619, Actions line 5683.

<a id="trigger-0b0b4d0c"></a>

### 27. ReenableRB - 0B0B4D0C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Bridge Repair Hut (CABHUT), owner Civilian1 House, cell (95, 108), tag 0B0B4B0C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 14 (country/type RUSSIAN1; placed owner Russian1 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [RepairBridge (07B3216C)](#trigger-07b3216c).
2. Set local flag 1 (Bridge2Open).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5556, Events line 5620, Actions line 5684.

<a id="trigger-0b1a2eec"></a>

### 28. ReinforcementsEastA - 0B1A2EEC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B1A0C7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 700 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [ReinforcementsEast (0B90B59C)](all03u-teams.md#team-0b90b59c).
2. Enable and reset applicable timers for [ReinforcementsEastB (09B6A97C)](#trigger-09b6a97c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5557, Events line 5621, Actions line 5685.

<a id="trigger-09b6a97c"></a>

### 29. ReinforcementsEastB - 09B6A97C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ReinforcementsEastA (0B1A2EEC)](#trigger-0b1a2eec).

Attached scope: tag definitions 09B6A51C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 49 (cell 147, 90).
2. Reveal terrain around waypoint 49 (cell 147, 90).
3. Display message “A brave group of Allied survivors has scraped together a squad near the Smithsonian” (MISSION:All03j).
4. Play voice notification EVA_ReinforcementsHaveArrived.
5. Play sound Bonus.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5558, Events line 5622, Actions line 5686.

<a id="trigger-08bd304c"></a>

### 30. AttackParty - 08BD304C

Owner reference: Russian2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (107, 101); tag 08BD70EC, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Horizontal Line: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create/recruit team [Hunters(Shock&Flak) (0B63732C)](all03u-teams.md#team-0b63732c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5559, Events line 5623, Actions line 5687.

<a id="trigger-086d811c"></a>

### 31. Garrison1 - 086D811C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 086D94AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [GarrisonWash03 (0B7618DC)](all03u-teams.md#team-0b7618dc) at waypoint 40 (cell 119, 92).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5560, Events line 5624, Actions line 5688.

<a id="trigger-0b77db7c"></a>

### 32. !CreateCrate - 0B77DB7C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B779D0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 4 (cell 127, 84).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5561, Events line 5625, Actions line 5689.

<a id="trigger-0b779c1c"></a>

### 33. RepairedSmithCastle - 0B779C1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 3 (cell 115, 85).
2. Create crate type 10 at waypoint 59 (cell 118, 87).
3. Play sound Bonus.
4. Disable [RepairedSmithCastle (0B779C1C)](#trigger-0b779c1c).
5. Display message “Power-up Crate discovered!” (MISSION:Sov11g).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5562, Events line 5626, Actions line 5690.

<a id="trigger-0b77945c"></a>

### 34. RepairedSmithsonian - 0B77945C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 1 (cell 115, 53).
2. Create crate type 9 at waypoint 65 (cell 120, 53).
3. Play sound Bonus.
4. Disable [RepairedSmithsonian (0B77945C)](#trigger-0b77945c).
5. Display message “Power-up Crate discovered!” (MISSION:Sov11g).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5563, Events line 5627, Actions line 5691.

<a id="trigger-0b816b2c"></a>

### 35. Garrison2 - 0B816B2C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B816A4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [GarrisonWash10 (095F8A4C)](all03u-teams.md#team-095f8a4c) at waypoint 39 (cell 109, 51).
2. Supply reinforcement team [GarrisonWash04 (0B7614BC)](all03u-teams.md#team-0b7614bc) at waypoint 42 (cell 103, 40).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5564, Events line 5628, Actions line 5692.

<a id="trigger-0b84304c"></a>

### 36. Garrison3 - 0B84304C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B844AEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [GarrisonWash11 (0B740EFC)](all03u-teams.md#team-0b740efc) at waypoint 8 (cell 53, 44).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5565, Events line 5629, Actions line 5693.

<a id="trigger-098f0f3c"></a>

### 37. ReinforcementsWestA - 098F0F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 098F091C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 950 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [ReinforcementsWest1 (0B90BA4C)](all03u-teams.md#team-0b90ba4c).
2. Enable and reset applicable timers for [ReinforcementsWestB (09B6A2CC)](#trigger-09b6a2cc).
3. Supply reinforcement team [ReinforcementsWest2 (087606AC)](all03u-teams.md#team-087606ac).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5566, Events line 5630, Actions line 5694.

<a id="trigger-09b6a2cc"></a>

### 38. ReinforcementsWestB - 09B6A2CC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ReinforcementsWestA (098F0F3C)](#trigger-098f0f3c).

Attached scope: tag definitions 09B6A1EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 48 (cell 47, 90).
2. Reveal terrain around waypoint 48 (cell 47, 90).
3. Display message “Straggler units from across the Potomac have gathered up near the Lincoln Memorial” (MISSION:All03i).
4. Play voice notification EVA_ReinforcementsHaveArrived.
5. Play sound Bonus.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5567, Events line 5631, Actions line 5695.

<a id="trigger-07e870ac"></a>

### 39. AmbientSounds1 - 07E870AC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E8131C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_CricketChirps at waypoint 9 (cell 76, 127).
2. Play sound _Amb_CricketBed at waypoint 11 (cell 78, 123).
3. Play sound _Amb_CricketBed at waypoint 12 (cell 121, 141).
4. Play sound _Amb_CricketChirps at waypoint 10 (cell 125, 132).
5. Play sound _Amb_CricketBed at waypoint 13 (cell 108, 75).
6. Play sound _Amb_CricketChirps at waypoint 14 (cell 113, 58).
7. Play sound _Amb_CricketBed at waypoint 15 (cell 42, 62).
8. Play sound _Amb_WavesLake at waypoint 16 (cell 43, 53).
9. Play sound _Amb_CricketChirps at waypoint 17 (cell 23, 72).
10. Play sound _Amb_OceanLight at waypoint 18 (cell 103, 159).
11. Play sound _Amb_OceanLight at waypoint 19 (cell 58, 96).
12. Play sound _Amb_OceanLight at waypoint 20 (cell 137, 108).
13. Play sound _Amb_OceanLight at waypoint 21 (cell 117, 115).
14. Play sound _Amb_OceanLight at waypoint 23 (cell 76, 112).
15. Play sound _Amb_OceanLight at waypoint 32 (cell 65, 125).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5568, Events line 5632, Actions line 5696.

<a id="trigger-07fefe9c"></a>

### 40. Russia1Hunt - 07FEFE9C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FEFA1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  #: 20.

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type RUSSIAN1; placed owner Russian1 House).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5569, Events line 5633, Actions line 5697.

<a id="trigger-0bb7215c"></a>

### 41. AmbientSounds2 - 0BB7215C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BB7392C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_CricketChirps at waypoint 33 (cell 84, 85).
2. Play sound _Amb_CricketBed at waypoint 34 (cell 77, 87).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5570, Events line 5634, Actions line 5698.

<a id="trigger-0bb74dec"></a>

### 42. BridgeEngDied - 0BB74DEC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BB74B7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Bridge2Open) is clear.
2. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

Flag writers in this mission: clear local flag 1 (Bridge2Open) at [RepairBridge (07B3216C)](#trigger-07b3216c); set local flag 1 (Bridge2Open) at [ReenableRB (0B0B4D0C)](#trigger-0b0b4d0c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [EngineerBridgeRepair (0B2A832C)](all03u-teams.md#team-0b2a832c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5571, Events line 5635, Actions line 5699.

<a id="trigger-09b6c5bc"></a>

### 43. RepairedLincoln - 09B6C5BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 52 (cell 28, 71).
2. Create crate type 0 at waypoint 28 (cell 29, 68).
3. Play sound Bonus.
4. Disable [RepairedLincoln (09B6C5BC)](#trigger-09b6c5bc).
5. Display message “Power-up Crate discovered!” (MISSION:Sov11g).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5572, Events line 5636, Actions line 5700.

<a id="trigger-09b6997c"></a>

### 44. RepairedWash - 09B6997C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 50 (cell 87, 71).
2. Create crate type 0 at waypoint 51 (cell 84, 70).
3. Play sound Bonus.
4. Disable [RepairedWash (09B6997C)](#trigger-09b6997c).
5. Display message “Power-up Crate discovered!” (MISSION:Sov11g).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5573, Events line 5637, Actions line 5701.

<a id="trigger-0a2281bc"></a>

### 45. RepairedJefferson - 0A2281BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 14 at waypoint 9 (cell 76, 127).
2. Create crate type 0 at waypoint 11 (cell 78, 123).
3. Play sound Bonus.
4. Disable [RepairedJefferson (0A2281BC)](#trigger-0a2281bc).
5. Display message “Power-up Crate discovered!” (MISSION:Sov11g).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5574, Events line 5638, Actions line 5702.

<a id="trigger-0c3f9cfc"></a>

### 46. !!Lock/Reveal - 0C3F9CFC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C3F995C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable player input.
2. Reveal terrain around waypoint 98 (cell 81, 125).
3. Reveal terrain around waypoint 52 (cell 28, 71).
4. Reveal terrain around waypoint 50 (cell 87, 71).
5. Reveal terrain around waypoint 59 (cell 118, 87).
6. Reveal terrain around waypoint 65 (cell 120, 53).
7. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5575, Events line 5639, Actions line 5703.

<a id="trigger-0a05decc"></a>

### 47. ShockTroopIntro - 0A05DECC

Owner reference: Russian2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A0461CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 250 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [ShockAttack-Intro (0C33ADCC)](all03u-teams.md#team-0c33adcc).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5576, Events line 5640, Actions line 5704.

<a id="trigger-0861931c"></a>

### 48. StartProduction2 - 0861931C

Owner reference: Russian2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0861ACBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 270 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 15 (country/type RUSSIAN2; placed owner Russian2 House).
2. AI triggers begin: owner selector 15 (country/type RUSSIAN2; placed owner Russian2 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5577, Events line 5641, Actions line 5705.

<a id="trigger-086221cc"></a>

### 49. DestroyedJefferson - 086221CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RepairedJefferson (0A2281BC)](#trigger-0a2281bc).

Attached scope: Jefferson Memorial (CAWASH14), owner Civilian1 House, cell (76, 124), tag 0A16C04C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set global flag 5.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5578, Events line 5642, Actions line 5706.

<a id="trigger-086220dc"></a>

### 50. DestroyedLincoln - 086220DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RepairedLincoln (09B6C5BC)](#trigger-09b6c5bc).

Attached scope: Lincoln Memorial (CAWASH15), owner Civilian1 House, cell (25, 68), tag 09B6C42C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set global flag 4.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5579, Events line 5643, Actions line 5707.

<a id="trigger-08621f3c"></a>

### 51. DestroyedSmithCastle - 08621F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RepairedSmithCastle (0B779C1C)](#trigger-0b779c1c).

Attached scope: Smithsonian Castle (CAWASH16), owner Civilian1 House, cell (114, 82), tag 0B779A1C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set global flag 7.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5580, Events line 5644, Actions line 5708.

<a id="trigger-08621e4c"></a>

### 52. DestroyedSmithsonian - 08621E4C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RepairedSmithsonian (0B77945C)](#trigger-0b77945c).

Attached scope: Smithsonian Natural History Museum (CAWASH17), owner Civilian1 House, cell (114, 49), tag 0B761ACC, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set global flag 3.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5581, Events line 5645, Actions line 5709.

<a id="trigger-08621d5c"></a>

### 53. DestroyedWashMon - 08621D5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RepairedWash (09B6997C)](#trigger-09b6997c).

Attached scope: Washington Monument (CAWSH12), owner Civilian1 House, cell (85, 68), tag 09B6982C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set global flag 6.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5582, Events line 5646, Actions line 5710.

<a id="trigger-0a33d0dc"></a>

### 54. Russia2Hunt - 0A33D0DC

Owner reference: Russian2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A34418C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 15 (country/type RUSSIAN2; placed owner Russian2 House).

**Then perform these actions in order:**

1. All change house: owner selector 14 (country/type RUSSIAN1; placed owner Russian1 House).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5583, Events line 5647, Actions line 5711.

<a id="trigger-0c224d4c"></a>

### 55. RevealBeacon - 0C224D4C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Sentry Gun (NALASR), owner Russian1 House, cell (80, 34), tag 0C23711C, persistence mode 0; Sentry Gun (NALASR), owner Russian1 House, cell (71, 34), tag 0C23711C, persistence mode 0; Invisible Red Light Post (INREDLMP), owner Civilian1 House, cell (76, 38), tag 0C23711C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 57 (cell 75, 34).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5584, Events line 5648, Actions line 5712.

<a id="trigger-0897f36c"></a>

### 56. Hint - Garrison pt1 - 0897F36C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: Mailbox (CAMISC04), owner Civilian1 House, cell (96, 125), tag 0897F28C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Arrows - Garrison (0897D9DC)](#trigger-0897d9dc).
2. Enable and reset applicable timers for [Hint - Garrison pt2 (0897EF3C)](#trigger-0897ef3c).
3. Display message “HINT: Order GIs into nearby CIVILIAN BUILDINGS to fortify them.” (MISSION:All03m).
4. Reveal terrain around waypoint 60 (cell 89, 122).
5. Reveal terrain around waypoint 66 (cell 89, 119).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5585, Events line 5649, Actions line 5713.

<a id="trigger-0897d9dc"></a>

### 57. Arrows - Garrison - 0897D9DC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint - Garrison pt1 (0897F36C)](#trigger-0897f36c).

Attached scope: tag definitions 0897D44C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 471; location/duration field BI.
2. Play Anim At; main setting 471; location/duration field BO.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5586, Events line 5650, Actions line 5714.

<a id="trigger-0897ef3c"></a>

### 58. Hint - Garrison pt2 - 0897EF3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint - Garrison pt1 (0897F36C)](#trigger-0897f36c).

Attached scope: tag definitions 0897ED3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 16 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Arrows - Garrison (0897D9DC)](#trigger-0897d9dc).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5587, Events line 5651, Actions line 5715.

<a id="trigger-0c1c37cc"></a>

### 59. Hint - Hospital - 0C1C37CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Civilian Hospital (CAHOSP), owner Civilian2 House, cell (119, 125), tag 0C1C342C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “HINT: Send INFANTRY into the HOSPITAL to restore them to full health” (MISSION:All04h).
2. Reveal terrain around waypoint 70 (cell 122, 126).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5588, Events line 5652, Actions line 5716.

<a id="trigger-08aa22ac"></a>

### 60. Hint-IFV -- pt2 - 08AA22AC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08AA21CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Flash team [FlashIFV1 (0AF2DAFC)](all03u-teams.md#team-0af2dafc) with duration setting 50.
2. Flash team [FlashIFV2 (0AF2930C)](all03u-teams.md#team-0af2930c) with duration setting 50.
3. Flash team [FlashIFV3 (0AF2AEFC)](all03u-teams.md#team-0af2aefc) with duration setting 50.
4. Play voice notification Unit_Eva_IFV.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5589, Events line 5653, Actions line 5717.

<a id="trigger-0af78d3c"></a>

### 61. DamagedIFVSparks - 0AF78D3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AF7891C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Particle Anim at; main setting 11; location/duration field BR.

Source locator: MAPS01.MIX/all03u.map; Triggers line 5590, Events line 5654, Actions line 5718.

<a id="trigger-0af7882c"></a>

### 62. Hint-IFV -- pt4 - 0AF7882C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AF7874C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable [DamagedIFVSparks (0AF78D3C)](#trigger-0af78d3c).

Source locator: MAPS01.MIX/all03u.map; Triggers line 5591, Events line 5655, Actions line 5719.

[All team rosters and ordered plans](all03u-teams.md) | [All mission overrides](all03u-overrides.md)
