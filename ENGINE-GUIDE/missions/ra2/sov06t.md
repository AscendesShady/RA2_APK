# Operation: Sub-Divide

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for sov06t.map.](../../images/map-sov06t.svg)

*Initial placement schematic for sov06t.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** sov06t.map. **Effective extracted member:** MAPS02.MIX/sov06t.map. **Trigger definitions:** 43.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov06t-teams.md) | [All mission overrides](sov06t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | TEMPERATE |
| Map size | 0,0,148,78 |
| Visible local rectangle | 2,4,144,68 |
| Placed vehicles | 44 |
| Placed infantry | 23 |
| Placed structures | 105 |
| Placed aircraft | 0 |
| Team templates | 45 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 500 | BadGuy1 |
| 2 | KoreanFleet House | 0 | KoreanFleet |
| 3 | BadGuy3 House | 1000 | BadGuy3 |
| 4 | Neutral House | 0 | Neutral |
| 5 | Other1 House | 0 | Other1 |
| 6 | Other2 House | 0 | Other2 |
| 7 | Other3 House | 0 | Other3 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | TransportArrived,0 |
| 1 | TransportsUnloaded,0 |
| 2 | TransportArrived2,0 |
| 3 | TransportUnloaded2,0 |
| 4 | AirHarrassArrived,0 |
| 5 | TransportArrived1,0 |
| 6 | DreadsHome,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [PlayerWin2 (0B0B04AC)](#trigger-0b0b04ac) | 9 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [PlayerLoss (0907B050)](#trigger-0907b050) | Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House). | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-06c50b60"></a>

### 1. AlliedScouts1 - 06C50B60

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 06C50460 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Scouts1 (0E4FE57C)](sov06t-teams.md#team-0e4fe57c).
2. Enable and reset applicable timers for [AlliedHarassment1 (0907FF60)](#trigger-0907ff60).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6044, Events line 6089, Actions line 6134.

<a id="trigger-0907ff60"></a>

### 2. AlliedHarassment1 - 0907FF60

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AlliedScouts1 (06C50B60)](#trigger-06c50b60).

Attached scope: tag definitions 0907FB40 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [AlliedHarrassment2 (0A6C6830)](#trigger-0a6c6830).
2. Create/recruit team [Harrass1 (0E4FC48C)](sov06t-teams.md#team-0e4fc48c).
3. Create/recruit team [Harrass1 (0E4FC48C)](sov06t-teams.md#team-0e4fc48c).
4. Create/recruit team [Harrass2 (0E4FBDEC)](sov06t-teams.md#team-0e4fbdec).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6045, Events line 6090, Actions line 6135.

<a id="trigger-0a6c6830"></a>

### 3. AlliedHarrassment2 - 0A6C6830

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AlliedHarassment1 (0907FF60)](#trigger-0907ff60); enable from [AlliedScouts2 (0888B070)](#trigger-0888b070).

Attached scope: tag definitions 0A6C5B50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 150 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Harrass1 (0E4FC48C)](sov06t-teams.md#team-0e4fc48c).
2. Create/recruit team [Harrass1 (0E4FC48C)](sov06t-teams.md#team-0e4fc48c).
3. Create/recruit team [Harrass3 (0E50354C)](sov06t-teams.md#team-0e50354c).
4. Create/recruit team [Harrass3 (0E50354C)](sov06t-teams.md#team-0e50354c).
5. Create/recruit team [Harrass2 (0E4FBDEC)](sov06t-teams.md#team-0e4fbdec).
6. Create/recruit team [Harrass2 (0E4FBDEC)](sov06t-teams.md#team-0e4fbdec).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6046, Events line 6091, Actions line 6136.

<a id="trigger-0888b070"></a>

### 4. AlliedScouts2 - 0888B070

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08868440 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 350 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Scouts2 (0E4FDEFC)](sov06t-teams.md#team-0e4fdefc).
2. Enable and reset applicable timers for [AlliedHarrassment2 (0A6C6830)](#trigger-0a6c6830).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6047, Events line 6092, Actions line 6137.

<a id="trigger-070454a0"></a>

### 5. AsianFleetSpawn - 070454A0

Owner reference: KoreanFleet. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0848ACB0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The visible mission countdown has expired.

**Then perform these actions in order:**

1. Supply reinforcement team [AsianFleet1 (0FCA056C)](sov06t-teams.md#team-0fca056c).
2. Supply reinforcement team [AsianFleet2 (0FCAFEFC)](sov06t-teams.md#team-0fcafefc).
3. Supply reinforcement team [AsianFleet3 (0B0DC7DC)](sov06t-teams.md#team-0b0dc7dc).
4. Supply reinforcement team [AsianFleet4 (0FCAF80C)](sov06t-teams.md#team-0fcaf80c).
5. Create radar-event marker type 5 at waypoint 32 (cell 152, 20).
6. Reveal terrain around waypoint 32 (cell 152, 20).
7. Enable and reset applicable timers for [CarrierAttack (0A26ADB0)](#trigger-0a26adb0).
8. Play in-game movie 112.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6048, Events line 6093, Actions line 6138.

<a id="trigger-0a26adb0"></a>

### 6. CarrierAttack - 0A26ADB0

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AsianFleetSpawn (070454A0)](#trigger-070454a0).

Attached scope: tag definitions 0A26A4B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 400 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [3Carriers (0AB9932C)](sov06t-teams.md#team-0ab9932c).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6049, Events line 6094, Actions line 6139.

<a id="trigger-07f8c4b0"></a>

### 7. BG1 Produce - 07F8C4B0

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F8B8F0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The visible mission countdown has expired.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6050, Events line 6095, Actions line 6140.

<a id="trigger-07a8fca0"></a>

### 8. AllNavyDestroyed - 07A8FCA0

Owner reference: KoreanFleet. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A8FB90 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  Naval: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. Destroyed,  Units,  Naval: owner selector 15 (country/type KOREANFLEET; placed owner KoreanFleet House).

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Enable and reset applicable timers for [PlayerWin2 (0B0B04AC)](#trigger-0b0b04ac).
3. Disable [PlayerLoss (0907B050)](#trigger-0907b050).
4. Disable [RepeatObjective1 (0C02103C)](#trigger-0c02103c).
5. Disable [RepeatObjective2 (0C09D06C)](#trigger-0c09d06c).
6. Enable and reset applicable timers for [CheerMore (0B0D333C)](#trigger-0b0d333c).
7. Play voice notification EVA_PrimaryObjectiveAchieved.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6051, Events line 6096, Actions line 6141.

<a id="trigger-0b0b04ac"></a>

### 9. PlayerWin2 - 0B0B04AC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AllNavyDestroyed (07A8FCA0)](#trigger-07a8fca0).

Attached scope: tag definitions 0B0CA38C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6052, Events line 6097, Actions line 6142.

<a id="trigger-0907b050"></a>

### 10. PlayerLoss - 0907B050

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerForcesLand3 (09688700)](#trigger-09688700).

Attached scope: tag definitions 0907CA50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6053, Events line 6098, Actions line 6143.

<a id="trigger-0c02103c"></a>

### 11. RepeatObjective1 - 0C02103C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [!StateObjective1 (09286080)](#trigger-09286080).

Attached scope: tag definitions 0C02707C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Establish a base on the Hawaiian Islands” (MISSION:Sov6a).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6054, Events line 6099, Actions line 6144.

<a id="trigger-0c09d06c"></a>

### 12. RepeatObjective2 - 0C09D06C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [StateObjective2 (0B1503BC)](#trigger-0b1503bc).

Attached scope: tag definitions 0C09B08C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy the Allied fleet” (MISSION:Sov06g).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6055, Events line 6100, Actions line 6145.

<a id="trigger-0b0d333c"></a>

### 13. CheerMore - 0B0D333C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AllNavyDestroyed (07A8FCA0)](#trigger-07a8fca0).

Attached scope: tag definitions 0B0D237C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6056, Events line 6101, Actions line 6146.

<a id="trigger-0740c320"></a>

### 14. Start1 - 0740C320

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E0BF70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Create/recruit team [BaseDef1 (0AF5C0D4)](sov06t-teams.md#team-0af5c0d4).
3. Create/recruit team [BaseDef2 (0B0A3EFC)](sov06t-teams.md#team-0b0a3efc).
4. Create/recruit team [BaseDef3 (0AF5D9E4)](sov06t-teams.md#team-0af5d9e4).
5. Create/recruit team [BaseDef4(Navy) (0BFA0DCC)](sov06t-teams.md#team-0bfa0dcc).
6. Enable and reset applicable timers for [!StateObjective1 (09286080)](#trigger-09286080).
7. Supply reinforcement team [BaseDef5(Harriers) (0C1BF43C)](sov06t-teams.md#team-0c1bf43c) at waypoint 95 (cell 52, 103).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6057, Events line 6102, Actions line 6147.

<a id="trigger-09286080"></a>

### 15. !StateObjective1 - 09286080

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start1 (0740C320)](#trigger-0740c320).

Attached scope: tag definitions 09289090 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Establish a base on the Hawaiian Islands” (MISSION:Sov6a).
2. Enable and reset applicable timers for [RepeatObjective1 (0C02103C)](#trigger-0c02103c).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6058, Events line 6103, Actions line 6148.

<a id="trigger-09fef960"></a>

### 16. StartCoastGuard - 09FEF960

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09FE8880 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [CoastGuard1 (0BF9232C)](sov06t-teams.md#team-0bf9232c).
2. Create/recruit team [CoastGuard2 (0BF91B7C)](sov06t-teams.md#team-0bf91b7c).
3. Create/recruit team [CoastGuard3 (0BF917DC)](sov06t-teams.md#team-0bf917dc).
4. Create/recruit team [CoastGuard4 (0BF9143C)](sov06t-teams.md#team-0bf9143c).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6059, Events line 6104, Actions line 6149.

<a id="trigger-08c5d690"></a>

### 17. AirportTaken - 08C5D690

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tech Airport (CAAIRP), owner Neutral House, cell (69, 193), tag 08C5D350, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [AirportTaken2 (083828C0)](#trigger-083828c0).
2. Create crate type 0 at waypoint 28 (cell 70, 197).
3. Create crate type 0 at waypoint 29 (cell 45, 180).
4. Play in-game movie 113.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6060, Events line 6105, Actions line 6150.

<a id="trigger-083828c0"></a>

### 18. AirportTaken2 - 083828C0

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AirportTaken (08C5D690)](#trigger-08c5d690).

Attached scope: tag definitions 083825E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [AirportHarass (0ADCEB54)](sov06t-teams.md#team-0adceb54).
2. Create/recruit team [AirportHarass (0ADCEB54)](sov06t-teams.md#team-0adceb54).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6061, Events line 6106, Actions line 6151.

<a id="trigger-0968a9f0"></a>

### 19. PlayerForcesLand1 - 0968A9F0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09688860 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 98 (cell 201, 89).
2. Disable player input.
3. Enable and reset applicable timers for [UnlockInput (09701390)](#trigger-09701390).
4. Enable and reset applicable timers for [MoveCamera (08E1CC80)](#trigger-08e1cc80).
5. Supply reinforcement team [StartForce2 (08D49CB0)](sov06t-teams.md#team-08d49cb0).
6. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6062, Events line 6107, Actions line 6152.

<a id="trigger-09701390"></a>

### 20. UnlockInput - 09701390

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerForcesLand1 (0968A9F0)](#trigger-0968a9f0).

Attached scope: tag definitions 0970AF70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6063, Events line 6108, Actions line 6153.

<a id="trigger-08e1cc80"></a>

### 21. MoveCamera - 08E1CC80

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerForcesLand1 (0968A9F0)](#trigger-0968a9f0).

Attached scope: tag definitions 08E1C7D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 73 (cell 203, 76) with speed setting 1.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6064, Events line 6109, Actions line 6154.

<a id="trigger-09688700"></a>

### 22. PlayerForcesLand3 - 09688700

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09688520 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlayerLoss (0907B050)](#trigger-0907b050).
2. Supply reinforcement team [StartForce1a (09AD6520)](sov06t-teams.md#team-09ad6520).
3. Supply reinforcement team [StartForce1b (09ADFA80)](sov06t-teams.md#team-09adfa80).
4. Supply reinforcement team [StartForce1c (09ADFE00)](sov06t-teams.md#team-09adfe00).
5. Supply reinforcement team [StartForce1d (09ADF700)](sov06t-teams.md#team-09adf700).
6. Supply reinforcement team [StartForce1e (09ADF280)](sov06t-teams.md#team-09adf280).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6065, Events line 6110, Actions line 6155.

<a id="trigger-08cfef60"></a>

### 23. PlayerForcesLand2 - 08CFEF60

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CFECB0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [StartForce3 (08D49840)](sov06t-teams.md#team-08d49840).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6066, Events line 6111, Actions line 6156.

<a id="trigger-0a91d700"></a>

### 24. HarriersAttack - 0A91D700

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A91D560 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [BaseDef5(Harriers) (0C1BF43C)](sov06t-teams.md#team-0c1bf43c).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6067, Events line 6112, Actions line 6157.

<a id="trigger-077c80d0"></a>

### 25. AsianFleetTimer - 077C80D0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [StartAsianFleetTimer (077C9DD0)](#trigger-077c9dd0).

Attached scope: tag definitions 077C9EB0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 900 configured time units.
2. Use countdown label “Estimated time until Korean Fleet arrives:” (MISSION:Sov06b).
3. Start the visible mission timer.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6068, Events line 6113, Actions line 6158.

<a id="trigger-077c9dd0"></a>

### 26. StartAsianFleetTimer - 077C9DD0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 077C9B60 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [AsianFleetTimer (077C80D0)](#trigger-077c80d0).
2. Enable and reset applicable timers for [Obj1CompleteSpeech (0C22FF3C)](#trigger-0c22ff3c).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6069, Events line 6114, Actions line 6159.

<a id="trigger-0c22ff3c"></a>

### 27. Obj1CompleteSpeech - 0C22FF3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [StartAsianFleetTimer (077C9DD0)](#trigger-077c9dd0).

Attached scope: tag definitions 0C22F91C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_PrimaryObjectiveAchieved.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6070, Events line 6115, Actions line 6160.

<a id="trigger-07e85310"></a>

### 28. CarrierVsConYard - 07E85310

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E86F50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1400 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Naval3 (0BFA22CC)](sov06t-teams.md#team-0bfa22cc).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6071, Events line 6116, Actions line 6161.

<a id="trigger-0a14b2c4"></a>

### 29. DreadReinforcements1 - 0A14B2C4

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A14AC44 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 800 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [GiftFleet (0868F29C)](sov06t-teams.md#team-0868f29c).
2. Enable and reset applicable timers for [DreadReinforcements2 (0ADE2C14)](#trigger-0ade2c14).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6072, Events line 6117, Actions line 6162.

<a id="trigger-0ade2c14"></a>

### 30. DreadReinforcements2 - 0ADE2C14

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [DreadReinforcements1 (0A14B2C4)](#trigger-0a14b2c4).

Attached scope: tag definitions 0ADE2B24 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 26 (cell 120, 46).
2. Create radar-event marker type 1 at waypoint 26 (cell 120, 46).
3. Display message “A small fleet of the new Soviet Dreadnought has arrived” (MISSION:Sov06c).
4. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6073, Events line 6118, Actions line 6163.

<a id="trigger-090e6394"></a>

### 31. FreeCrate - 090E6394

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Cow (COW), owner Neutral House, cell (174, 48), tag 090E1EA4, persistence mode 1; Cow (COW), owner Neutral House, cell (171, 49), tag 090E1EA4, persistence mode 1; Cow (COW), owner Neutral House, cell (172, 47), tag 090E1EA4, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 19 (cell 173, 48).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6074, Events line 6119, Actions line 6164.

<a id="trigger-08212a04"></a>

### 32. CreateCrates - 08212A04

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08213AF4 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 30 (cell 30, 168).
2. Create crate type 0 at waypoint 34 (cell 76, 207).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6075, Events line 6120, Actions line 6165.

<a id="trigger-0b3ac804"></a>

### 33. BunkerCaptured(Crate) - 0B3AC804

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Bunker (CABUNK01), owner Neutral House, cell (159, 81), tag 0B3AC494, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 50 (cell 164, 82).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6076, Events line 6121, Actions line 6166.

<a id="trigger-097137d4"></a>

### 34. Hint - 097137D4

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 53 (global list position: Tesla Coil (TESLA)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

No action entries.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6077, Events line 6122, Actions line 6167.

<a id="trigger-096a9d1c"></a>

### 35. AmbientSounds1 - 096A9D1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 096A9A2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsHarbor at waypoint 52 (cell 91, 104).
2. Play sound _Amb_BirdsHarbor at waypoint 51 (cell 81, 114).
3. Play sound _Amb_OceanHeavy at waypoint 54 (cell 179, 96).
4. Play sound _Amb_OceanHeavy at waypoint 55 (cell 151, 68).
5. Play sound _Amb_OceanHeavy at waypoint 56 (cell 159, 41).
6. Play sound _Amb_OceanHeavy at waypoint 57 (cell 115, 60).
7. Play sound _Amb_OceanHeavy at waypoint 58 (cell 146, 92).
8. Play sound _Amb_OceanHeavy at waypoint 59 (cell 132, 126).
9. Play sound _Amb_OceanHeavy at waypoint 60 (cell 104, 161).
10. Play sound _Amb_OceanHeavy at waypoint 61 (cell 63, 149).
11. Play sound _Amb_OceanHeavy at waypoint 62 (cell 17, 157).
12. Play sound _Amb_OceanHeavy at waypoint 63 (cell 63, 169).
13. Play sound _Amb_OceanHeavy at waypoint 64 (cell 80, 185).
14. Play sound _Amb_BirdsHarbor at waypoint 53 (cell 99, 104).
15. Play sound _Amb_BirdsBeach at waypoint 65 (cell 201, 76).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6078, Events line 6123, Actions line 6168.

<a id="trigger-09ad17dc"></a>

### 36. AmbientSounds2 - 09AD17DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09AD2A4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsTemperate1 at waypoint 66 (cell 99, 143).
2. Play sound _Amb_BirdsTemperate1 at waypoint 67 (cell 72, 137).
3. Play sound _Amb_BirdsTemperate1 at waypoint 68 (cell 35, 173).
4. Play sound _Amb_BirdsTemperate2 at waypoint 69 (cell 52, 176).
5. Play sound _Amb_BirdsTemperate1 at waypoint 70 (cell 55, 188).
6. Play sound _Amb_BirdsJungle1 at waypoint 71 (cell 118, 79).
7. Play sound _Amb_BirdsTemperate2 at waypoint 72 (cell 112, 79).
8. Play sound _Amb_OceanLight at waypoint 75 (cell 192, 89).
9. Play sound _Amb_River at waypoint 76 (cell 182, 74).
10. Play sound _Amb_OceanHeavy at waypoint 77 (cell 172, 31).
11. Play sound _Amb_BirdsJungle1 at waypoint 90 (cell 208, 65).
12. Play sound _Amb_BirdsTemperate1 at waypoint 91 (cell 188, 63).
13. Play sound _Amb_BirdsJungle1 at waypoint 92 (cell 172, 56).
14. Play sound _Amb_BirdsPark at waypoint 93 (cell 161, 57).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6079, Events line 6124, Actions line 6169.

<a id="trigger-086298fc"></a>

### 37. Hint-TeslaCoilCharge - 086298FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0862E88C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 53 (global list position: Tesla Coil (TESLA)). A map-local type-list change can affect index interpretation.
2. Build Infantry Type: type index 2 (global list position: Tesla Trooper (SHK)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play in-game movie 93.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6080, Events line 6125, Actions line 6170.

<a id="trigger-085fd83c"></a>

### 38. ArizonaMemDestroyed - 085FD83C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Arizona Memorial (CAMIAM08), owner Neutral House, cell (92, 112), tag 0860F26C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 74 (cell 89, 112).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6081, Events line 6126, Actions line 6171.

<a id="trigger-0893939c"></a>

### 39. DreadReinforcements3 - 0893939C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089392BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (DreadsHome) is set.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 11 (cell 195, 86).
2. Play voice notification EVA_ReinforcementsReady.

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6082, Events line 6127, Actions line 6172.

<a id="trigger-0b1503bc"></a>

### 40. StateObjective2 - 0B1503BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B15D04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy the Allied fleet” (MISSION:Sov06g).
2. Disable [RepeatObjective1 (0C02103C)](#trigger-0c02103c).
3. Enable and reset applicable timers for [RepeatObjective2 (0C09D06C)](#trigger-0c09d06c).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6083, Events line 6128, Actions line 6173.

<a id="trigger-0c12ec8c"></a>

### 41. AmbientSounds3 - 0C12EC8C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C12EBAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsJungle2 at waypoint 94 (cell 88, 75).
2. Play sound _Amb_BirdsTemperate1 at waypoint 95 (cell 52, 103).
3. Play sound _Amb_BirdsJungle1 at waypoint 96 (cell 42, 123).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6084, Events line 6129, Actions line 6174.

<a id="trigger-0a5d654c"></a>

### 42. WilliamsHouse - 0A5D654C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: House (CAHSE07), owner Neutral House, cell (78, 85), tag 0A5D3DFC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 14 at waypoint 97 (cell 81, 87).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6085, Events line 6130, Actions line 6175.

<a id="trigger-08cea10c"></a>

### 43. Start2 - 08CEA10C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CEBF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [BaseDef5(Harriers) (0C1BF43C)](sov06t-teams.md#team-0c1bf43c).

Source locator: MAPS02.MIX/sov06t.map; Triggers line 6086, Events line 6131, Actions line 6176.

[All team rosters and ordered plans](sov06t-teams.md) | [All mission overrides](sov06t-overrides.md)
