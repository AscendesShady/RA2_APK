# Operation: Last Chance

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all04u.map. **Effective extracted member:** MAPS01.MIX/all04u.map. **Trigger definitions:** 85.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all04u-teams.md) | [All mission overrides](all04u-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | URBAN |
| Map size | 0,0,110,70 |
| Visible local rectangle | 2,4,104,60 |
| Placed vehicles | 44 |
| Placed infantry | 29 |
| Placed structures | 127 |
| Placed aircraft | 0 |
| Team templates | 73 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | Russian1 House | 200 | Russian1 |
| 2 | Russian2 House | 100 | Russian2 |
| 3 | Cops House | 100 | Cops |
| 4 | Civilian1 House | 0 | Civilian1 |
| 5 | Other1 House | 10 | Other1 |
| 6 | Other2 House | 20 | Other2 |
| 7 | Russian3 House | 300 | Russian3 |
| 8 | CivilianTech House | 0 | CivilianTech |
| 9 | PlayerAlt House | 0 | PlayerAlt |
| 10 | PlayerAlt2 House | 0 | PlayerAlt2 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Reactor1Taken,0 |
| 1 | Reactor2Taken,0 |
| 2 | Reactor3Taken,0 |
| 3 | BridgeOpen,1 |
| 4 | CopsArrived,0 |
| 5 | mcvUnloaded,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [PlayerLoss2 (099359DC)](#trigger-099359dc) | Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).<br>Destroyed,  All: owner selector 22 (country/type PLAYERALT; placed owner PlayerAlt House).<br>Destroyed,  All: owner selector 23 (country/type PLAYERALT2; placed owner PlayerAlt2 House). | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [PlayerLoss1e (0BCE203C)](#trigger-0bce203c) | 20 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [PlayerWin4 (DeclareWin) (0883C03C)](#trigger-0883c03c) | 1 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [PlayerLoss3 (0BB8CADC)](#trigger-0bb8cadc) | Destroyed by anything. See attached-object/cell scope below. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-0993264c"></a>

### 1. StartNavyEnters1 - 0993264C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09935ACC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [StartingDest1 (0B1B559C)](all04u-teams.md#team-0b1b559c).
2. Create/recruit team [StartingDest2 (0B1BE6AC)](all04u-teams.md#team-0b1be6ac).
3. Create/recruit team [StartingDest3 (0B1BE30C)](all04u-teams.md#team-0b1be30c).
4. Create/recruit team [StartingDest4 (0B1BDC8C)](all04u-teams.md#team-0b1bdc8c).
5. Create/recruit team [StartingDest5 (0B1BD8EC)](all04u-teams.md#team-0b1bd8ec).
6. Create/recruit team [StartingDest6 (0B1BE1DC)](all04u-teams.md#team-0b1be1dc).
7. Reveal terrain around waypoint 98 (cell 142, 89).
8. Enable and reset applicable timers for [StartNavyEnters3 (08556A2C)](#trigger-08556a2c).
9. Disable player input.
10. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6275, Events line 6362, Actions line 6449.

<a id="trigger-08556a2c"></a>

### 2. StartNavyEnters3 - 08556A2C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [StartNavyEnters1 (0993264C)](#trigger-0993264c).

Attached scope: tag definitions 0855682C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Reinforcements have just arrived from our Canadian base” (MISSION:All04d).
2. Enable and reset applicable timers for [StartNavyEnters4 (0B89027C)](#trigger-0b89027c).
3. Enable and reset applicable timers for [PlayerLoss2 (099359DC)](#trigger-099359dc).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6276, Events line 6363, Actions line 6450.

<a id="trigger-0b89027c"></a>

### 3. StartNavyEnters4 - 0B89027C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [StartNavyEnters3 (08556A2C)](#trigger-08556a2c).

Attached scope: tag definitions 0B891F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Display message “Objective 1: Clear enemy shore defenses with your Destroyers, then land and establish a base” (MISSION:All04a).
3. Reveal terrain around waypoint 49 (cell 80, 124).
4. Reveal terrain around waypoint 50 (cell 80, 118).
5. Reveal terrain around waypoint 24 (cell 118, 116).
6. Reveal terrain around waypoint 8 (cell 117, 111).
7. Reveal terrain around waypoint 9 (cell 118, 106).
8. Create radar-event marker type 5 at waypoint 24 (cell 118, 116).
9. Create radar-event marker type 5 at waypoint 9 (cell 118, 106).
10. Enable and reset applicable timers for [RestateObjective1 (0400805C)](#trigger-0400805c).
11. Reveal terrain around waypoint 88 (cell 80, 130).
12. Reveal terrain around waypoint 89 (cell 80, 136).
13. Reveal terrain around waypoint 90 (cell 80, 111).
14. Reveal terrain around waypoint 91 (cell 80, 105).
15. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6277, Events line 6364, Actions line 6451.

<a id="trigger-099359dc"></a>

### 4. PlayerLoss2 - 099359DC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [StartNavyEnters3 (08556A2C)](#trigger-08556a2c).

Attached scope: tag definitions 099357DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Destroyed,  All: owner selector 22 (country/type PLAYERALT; placed owner PlayerAlt House).
3. Destroyed,  All: owner selector 23 (country/type PLAYERALT2; placed owner PlayerAlt2 House).

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6278, Events line 6365, Actions line 6452.

<a id="trigger-0400805c"></a>

### 5. RestateObjective1 - 0400805C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [StartNavyEnters4 (0B89027C)](#trigger-0b89027c).

Attached scope: tag definitions 0400FDAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Establish a base” (MISSION:All04l).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6279, Events line 6366, Actions line 6453.

<a id="trigger-0dd18dfc"></a>

### 6. Hint -- Destroyer - 0DD18DFC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0DD1867C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_Destroyer.
2. Flash team [StartingDest1 (0B1B559C)](all04u-teams.md#team-0b1b559c) with duration setting 80.
3. Flash team [StartingDest2 (0B1BE6AC)](all04u-teams.md#team-0b1be6ac) with duration setting 80.
4. Flash team [StartingDest3 (0B1BE30C)](all04u-teams.md#team-0b1be30c) with duration setting 80.
5. Flash team [StartingDest4 (0B1BDC8C)](all04u-teams.md#team-0b1bdc8c) with duration setting 80.
6. Flash team [StartingDest5 (0B1BD8EC)](all04u-teams.md#team-0b1bd8ec) with duration setting 80.
7. Flash team [StartingDest6 (0B1BE1DC)](all04u-teams.md#team-0b1be1dc) with duration setting 80.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6280, Events line 6367, Actions line 6454.

<a id="trigger-0908e13c"></a>

### 7. DisplayObjective2 - 0908E13C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ConYdBuilt-Obj2Movie (0854A38C)](#trigger-0854a38c).

Attached scope: tag definitions 09089E2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy the Soviet's Psychic Amplifier before it comes online” (MISSION:All04b).
2. Enable and reset applicable timers for [StartEnemyProduction (09956E2C)](#trigger-09956e2c).
3. Enable and reset applicable timers for [CountdownBegins (08004A1C)](#trigger-08004a1c).
4. Enable and reset applicable timers for [RestateObjective2 (0BBB294C)](#trigger-0bbb294c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6281, Events line 6368, Actions line 6455.

<a id="trigger-09956e2c"></a>

### 8. StartEnemyProduction - 09956E2C

Owner reference: Russian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [DisplayObjective2 (0908E13C)](#trigger-0908e13c).

Attached scope: tag definitions 0995683C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 250 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type RUSSIAN1; placed owner Russian1 House).
2. AI triggers begin: owner selector 14 (country/type RUSSIAN1; placed owner Russian1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6282, Events line 6369, Actions line 6456.

<a id="trigger-08004a1c"></a>

### 9. CountdownBegins - 08004A1C

Owner reference: Russian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [DisplayObjective2 (0908E13C)](#trigger-0908e13c).

Attached scope: tag definitions 08007B3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 3000 configured time units.
2. Start the visible mission timer.
3. Use countdown label “Estimated time until Psychic Amplifier is online:” (MISSION:All04c).
4. Enable and reset applicable timers for [PlayerLoss1a (09AA2F3C)](#trigger-09aa2f3c).
5. Enable and reset applicable timers for [TimerWarn - 10min (0A42687C)](#trigger-0a42687c).
6. Enable and reset applicable timers for [TimerWarn - 1min (0A426B6C)](#trigger-0a426b6c).
7. Enable and reset applicable timers for [TimerWarn - 2min (0A426F3C)](#trigger-0a426f3c).
8. Enable and reset applicable timers for [TimerWarn - 3min (0A42434C)](#trigger-0a42434c).
9. Enable and reset applicable timers for [TimerWarn - 4min (0A42478C)](#trigger-0a42478c).
10. Enable and reset applicable timers for [TimerWarn - 5min (0A424DDC)](#trigger-0a424ddc).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6283, Events line 6370, Actions line 6457.

<a id="trigger-0bbb294c"></a>

### 10. RestateObjective2 - 0BBB294C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [DisplayObjective2 (0908E13C)](#trigger-0908e13c).

Attached scope: tag definitions 0BBB286C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy the Psychic Amplifier before it comes online” (MISSION:All04g).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6284, Events line 6371, Actions line 6458.

<a id="trigger-09aa2f3c"></a>

### 11. PlayerLoss1a - 09AA2F3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CountdownBegins (08004A1C)](#trigger-08004a1c).

Attached scope: tag definitions 09AA2B8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The visible mission countdown has expired.

**Then perform these actions in order:**

1. Disable player input.
2. Jump the camera to waypoint 10 (cell 47, 84).
3. All change house: owner selector 18 (country/type OTHER1; placed owner Other1 House).
4. Enable and reset applicable timers for [PlayerLoss1c (0BC6390C)](#trigger-0bc6390c).
5. Disable [PlayerLoss2 (099359DC)](#trigger-099359dc).
6. Supply reinforcement team [HackCivilianForEnding (0867773C)](all04u-teams.md#team-0867773c) at waypoint 67 (cell 34, 91).
7. Play sound CameraSwitch.
8. Ion Storm start; main setting 200000.
9. Enable and reset applicable timers for [PlayerLoss1b (0A89A31C)](#trigger-0a89a31c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6285, Events line 6372, Actions line 6459.

<a id="trigger-0a42687c"></a>

### 12. TimerWarn - 10min - 0A42687C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CountdownBegins (08004A1C)](#trigger-08004a1c).

Attached scope: tag definitions 0A42667C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2400 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_10MinutesRemaining.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6286, Events line 6373, Actions line 6460.

<a id="trigger-0a426b6c"></a>

### 13. TimerWarn - 1min - 0A426B6C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CountdownBegins (08004A1C)](#trigger-08004a1c).

Attached scope: tag definitions 0A42696C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2940 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_1MinuteRemaining.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6287, Events line 6374, Actions line 6461.

<a id="trigger-0a426f3c"></a>

### 14. TimerWarn - 2min - 0A426F3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CountdownBegins (08004A1C)](#trigger-08004a1c).

Attached scope: tag definitions 0A426C5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2880 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_2MinutesRemaining.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6288, Events line 6375, Actions line 6462.

<a id="trigger-0a42434c"></a>

### 15. TimerWarn - 3min - 0A42434C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CountdownBegins (08004A1C)](#trigger-08004a1c).

Attached scope: tag definitions 0A42414C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2820 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_3MinutesRemaining.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6289, Events line 6376, Actions line 6463.

<a id="trigger-0a42478c"></a>

### 16. TimerWarn - 4min - 0A42478C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CountdownBegins (08004A1C)](#trigger-08004a1c).

Attached scope: tag definitions 0A42443C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2760 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_4MinutesRemaining.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6290, Events line 6377, Actions line 6464.

<a id="trigger-0a424ddc"></a>

### 17. TimerWarn - 5min - 0A424DDC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CountdownBegins (08004A1C)](#trigger-08004a1c).

Attached scope: tag definitions 0A42487C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2700 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_5MinutesRemaining.
2. Reveal terrain around waypoint 10 (cell 47, 84).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6291, Events line 6378, Actions line 6465.

<a id="trigger-0bc6390c"></a>

### 18. PlayerLoss1c - 0BC6390C

Owner reference: Russian3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerLoss1a (09AA2F3C)](#trigger-09aa2f3c).

Attached scope: tag definitions 0BCD704C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 19 (country/type OTHER2; placed owner Other2 House).
2. Enable and reset applicable timers for [PlayerLoss1d (0BCDE03C)](#trigger-0bcde03c).
3. All change house: owner selector 15 (country/type RUSSIAN2; placed owner Russian2 House).
4. Play sound PowerOn at waypoint 10 (cell 47, 84).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6292, Events line 6379, Actions line 6466.

<a id="trigger-0a89a31c"></a>

### 19. PlayerLoss1b - 0A89A31C

Owner reference: PlayerAlt. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerLoss1a (09AA2F3C)](#trigger-09aa2f3c).

Attached scope: tag definitions 0A89A23C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 18 (country/type OTHER1; placed owner Other1 House).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6293, Events line 6380, Actions line 6467.

<a id="trigger-0bcde03c"></a>

### 20. PlayerLoss1d - 0BCDE03C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerLoss1c (0BC6390C)](#trigger-0bc6390c).

Attached scope: tag definitions 0BCDC04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Enable and reset applicable timers for [PlayerLoss1e (0BCE203C)](#trigger-0bce203c).
3. Fire Sale: owner selector 18 (country/type OTHER1; placed owner Other1 House).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6294, Events line 6381, Actions line 6468.

<a id="trigger-0bce203c"></a>

### 21. PlayerLoss1e - 0BCE203C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerLoss1d (0BCDE03C)](#trigger-0bcde03c).

Attached scope: tag definitions 0BCF199C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6295, Events line 6382, Actions line 6469.

<a id="trigger-079d905c"></a>

### 22. BringInTransports - 079D905C

Owner reference: Russian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ConYdBuilt-Obj2Movie (0854A38C)](#trigger-0854a38c).

Attached scope: tag definitions 079DB99C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [EnemySubs (0C1CC67C)](all04u-teams.md#team-0c1cc67c).
2. Supply reinforcement team [Reinforce1-Trans (0C1A3C8C)](all04u-teams.md#team-0c1a3c8c).
3. Supply reinforcement team [Reinforce2-Trans (0C1A37DC)](all04u-teams.md#team-0c1a37dc).
4. Supply reinforcement team [Reinforce3-Trans (0C1A343C)](all04u-teams.md#team-0c1a343c).
5. Supply reinforcement team [Reinforce4-Trans (0C1A4C8C)](all04u-teams.md#team-0c1a4c8c).
6. Enable and reset applicable timers for [PingTextTransports (07E84E9C)](#trigger-07e84e9c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6296, Events line 6383, Actions line 6470.

<a id="trigger-07e84e9c"></a>

### 23. PingTextTransports - 07E84E9C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BringInTransports (079D905C)](#trigger-079d905c).

Attached scope: tag definitions 07E84BEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 22 (cell 142, 92).
2. Display message “More reinforcements have just arrived from across Lake Michigan” (MISSION:All04e).
3. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6297, Events line 6384, Actions line 6471.

<a id="trigger-099353fc"></a>

### 24. AmplifierDestroyed - 099353FC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Amplifier (NAPSYA), owner Russian2 House, cell (43, 82), tag 0993531C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Move the camera to waypoint 10 (cell 47, 84) with speed setting 4.
2. Enable and reset applicable timers for [PlayerWin3 (Siren) (09AA188C)](#trigger-09aa188c).
3. Disable [RestateObjective2 (0BBB294C)](#trigger-0bbb294c).
4. Disable [PlayerLoss1a (09AA2F3C)](#trigger-09aa2f3c).
5. Disable [PlayerLoss2 (099359DC)](#trigger-099359dc).
6. Play sound CameraSwitch.
7. Stop the visible mission timer.
8. Make ally: owner selector 13 (country/type PLAYER; placed owner Player House).
9. Disable player input.
10. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).
11. Play voice notification EVA_PrimaryObjectiveAchieved.
12. Enable and reset applicable timers for [PlayerWin2 (NukeBuilds) (0BC6598C)](#trigger-0bc6598c).
13. Play in-game movie 107.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6298, Events line 6385, Actions line 6472.

<a id="trigger-09aa188c"></a>

### 25. PlayerWin3 (Siren) - 09AA188C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AmplifierDestroyed (099353FC)](#trigger-099353fc).

Attached scope: tag definitions 09AA14EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 76 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PlayerWin4 (DeclareWin) (0883C03C)](#trigger-0883c03c).
2. Play sound AirRaidSiren at waypoint 80 (cell 53, 97).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6299, Events line 6386, Actions line 6473.

<a id="trigger-0bc6598c"></a>

### 26. PlayerWin2 (NukeBuilds) - 0BC6598C

Owner reference: Russian3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AmplifierDestroyed (099353FC)](#trigger-099353fc).

Attached scope: tag definitions 0BC658AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 20 (country/type RUSSIAN3; placed owner Russian3 House).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6300, Events line 6387, Actions line 6474.

<a id="trigger-0883c03c"></a>

### 27. PlayerWin4 (DeclareWin) - 0883C03C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerWin3 (Siren) (09AA188C)](#trigger-09aa188c).

Attached scope: tag definitions 0886B15C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6301, Events line 6388, Actions line 6475.

<a id="trigger-0a6e492c"></a>

### 28. RussianPatrols - 0A6E492C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A6EC04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Patrol1 (0C51EC8C)](all04u-teams.md#team-0c51ec8c).
2. Supply reinforcement team [Patrol2 (0C51E7DC)](all04u-teams.md#team-0c51e7dc).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6302, Events line 6389, Actions line 6476.

<a id="trigger-080f7a2c"></a>

### 29. CreateNewPatrol3 - 080F7A2C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 080F5B5C (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [Patrol3 (0C51E43C)](all04u-teams.md#team-0c51e43c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6303, Events line 6390, Actions line 6477.

<a id="trigger-099535dc"></a>

### 30. CheckBridge - 099535DC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BridgeRepaired (0995783C)](#trigger-0995783c).

Attached scope: 1 tagged map cells: (53, 84); tag 0995344C, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [EngineerBridge (0C6A76DC)](all04u-teams.md#team-0c6a76dc).
2. Disable [CheckBridge (099535DC)](#trigger-099535dc).
3. Enable and reset applicable timers for [BridgeEngDied (0C35F45C)](#trigger-0c35f45c).
4. Clear local flag 3 (BridgeOpen).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6304, Events line 6391, Actions line 6478.

<a id="trigger-0c35f45c"></a>

### 31. BridgeEngDied - 0C35F45C

Owner reference: Russian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [CheckBridge (099535DC)](#trigger-099535dc).

Attached scope: tag definitions 0C35F04C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.
2. local flag 3 (BridgeOpen) is clear.

Flag writers in this mission: clear local flag 3 (BridgeOpen) at [CheckBridge (099535DC)](#trigger-099535dc); set local flag 3 (BridgeOpen) at [BridgeRepaired (0995783C)](#trigger-0995783c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [EngineerBridge (0C6A76DC)](all04u-teams.md#team-0c6a76dc).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6305, Events line 6392, Actions line 6479.

<a id="trigger-0995783c"></a>

### 32. BridgeRepaired - 0995783C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Bridge Repair Hut (CABHUT), owner Civilian1 House, cell (50, 91), tag 0995763C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector -1 (unresolved or special selector).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [CheckBridge (099535DC)](#trigger-099535dc).
2. Set local flag 3 (BridgeOpen).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6306, Events line 6393, Actions line 6480.

<a id="trigger-086ab56c"></a>

### 33. EnemySubReinforce - 086AB56C

Owner reference: Russian1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ConYdBuilt-Obj2Movie (0854A38C)](#trigger-0854a38c).

Attached scope: tag definitions 086A8DDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [SubReinforcments (086ABBFC)](all04u-teams.md#team-086abbfc).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6307, Events line 6394, Actions line 6481.

<a id="trigger-0c4092ac"></a>

### 34. RuskySellConYard - 0C4092AC

Owner reference: Russian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ConYdBuilt-Obj2Movie (0854A38C)](#trigger-0854a38c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.
2. Enable and reset applicable timers for [RuskySellRefinery (0878081C)](#trigger-0878081c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6308, Events line 6395, Actions line 6482.

<a id="trigger-0878081c"></a>

### 35. RuskySellRefinery - 0878081C

Owner reference: Russian2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [RuskySellConYard (0C4092AC)](#trigger-0c4092ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6309, Events line 6396, Actions line 6483.

<a id="trigger-0802f68c"></a>

### 36. PlayerCapturedAirport - 0802F68C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tech Airport (CAAIRP), owner CivilianTech House, cell (86, 55), tag 0802F48C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create/recruit team [!DestroyAirport (087F2A4C)](all04u-teams.md#team-087f2a4c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6310, Events line 6397, Actions line 6484.

<a id="trigger-07f3bcfc"></a>

### 37. Garrison1 - 07F3BCFC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F3B7BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Garrison2 (07F3B68C)](all04u-teams.md#team-07f3b68c) at waypoint 14 (cell 32, 96).
2. Supply reinforcement team [Garrison2 (07F3B68C)](all04u-teams.md#team-07f3b68c) at waypoint 78 (cell 25, 112).
3. Supply reinforcement team [Garrison8 (0949D97C)](all04u-teams.md#team-0949d97c) at waypoint 12 (cell 59, 67).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6311, Events line 6398, Actions line 6485.

<a id="trigger-07f3be6c"></a>

### 38. Garrison2 - 07F3BE6C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F3CBBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Garrison1 (09868EFC)](all04u-teams.md#team-09868efc) at waypoint 82 (cell 36, 125).
2. Supply reinforcement team [Garrison6 (094B663C)](all04u-teams.md#team-094b663c) at waypoint 14 (cell 32, 96).
3. Supply reinforcement team [Garrison3 (098685EC)](all04u-teams.md#team-098685ec) at waypoint 54 (cell 38, 96).
4. Supply reinforcement team [Garrison4 (094B207C)](all04u-teams.md#team-094b207c) at waypoint 15 (cell 48, 97).
5. Supply reinforcement team [Garrison6 (094B663C)](all04u-teams.md#team-094b663c) at waypoint 25 (cell 62, 97).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6312, Events line 6399, Actions line 6486.

<a id="trigger-094b7c1c"></a>

### 39. Garrison3 - 094B7C1C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 093D3F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Garrison7 (094B59EC)](all04u-teams.md#team-094b59ec) at waypoint 15 (cell 48, 97).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6313, Events line 6400, Actions line 6487.

<a id="trigger-0980097c"></a>

### 40. AllRussianHunt - 0980097C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0980068C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 14 (country/type RUSSIAN1; placed owner Russian1 House).

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type RUSSIAN1; placed owner Russian1 House).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6314, Events line 6401, Actions line 6488.

<a id="trigger-0790369c"></a>

### 41. AmbientSounds1 - 0790369C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079030AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 23 (cell 112, 20).
2. Play sound _Amb_OceanLight at waypoint 29 (cell 131, 46).
3. Play sound _Amb_OceanLight at waypoint 30 (cell 130, 65).
4. Play sound _Amb_OceanLight at waypoint 31 (cell 108, 74).
5. Play sound _Amb_OceanLight at waypoint 32 (cell 131, 102).
6. Play sound _Amb_OceanLight at waypoint 33 (cell 90, 139).
7. Play sound _Amb_OceanLight at waypoint 34 (cell 93, 125).
8. Play sound _Amb_OceanLight at waypoint 35 (cell 95, 108).
9. Play sound _Amb_OceanLight at waypoint 36 (cell 102, 92).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6315, Events line 6402, Actions line 6489.

<a id="trigger-07906b3c"></a>

### 42. AmbientSounds2 - 07906B3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0790693C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsHarbor at waypoint 37 (cell 142, 55).
2. Play sound _Amb_BirdsPark at waypoint 38 (cell 65, 160).
3. Play sound _Amb_BirdsPark at waypoint 39 (cell 72, 143).
4. Play sound _Amb_BirdsPark at waypoint 41 (cell 82, 96).
5. Play sound _Amb_BirdsTemperate1 at waypoint 40 (cell 85, 87).
6. Play sound _Amb_BirdsHarbor at waypoint 42 (cell 106, 68).
7. Play sound _Amb_UrbanMurmur1 at waypoint 43 (cell 68, 53).
8. Play sound _Amb_UrbanMurmur1 at waypoint 44 (cell 21, 127).
9. Play sound _Amb_UrbanMurmur2 at waypoint 45 (cell 40, 147).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6316, Events line 6403, Actions line 6490.

<a id="trigger-03faddfc"></a>

### 43. RuskySellShipyard - 03FADDFC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Soviet Shipyard (NAYARD), owner Russian1 House, cell (87, 120), tag 03FAD46C, persistence mode 0.

**Wait for the recorded events:**

1. Half health (combat only). See attached-object/cell scope below.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6317, Events line 6404, Actions line 6491.

<a id="trigger-03faed1c"></a>

### 44. RuskySellPower1 - 03FAED1C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Quarter health (combat only). See attached-object/cell scope below.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6318, Events line 6405, Actions line 6492.

<a id="trigger-03fae58c"></a>

### 45. RuskySellPower2 - 03FAE58C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Quarter health (combat only). See attached-object/cell scope below.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6319, Events line 6406, Actions line 6493.

<a id="trigger-03fae1ac"></a>

### 46. RuskySellPower3 - 03FAE1AC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Quarter health (combat only). See attached-object/cell scope below.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6320, Events line 6407, Actions line 6494.

<a id="trigger-0854a38c"></a>

### 47. ConYdBuilt-Obj2Movie - 0854A38C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0854BE1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play in-game movie 106.
2. Enable and reset applicable timers for [DisplayObjective2 (0908E13C)](#trigger-0908e13c).
3. Enable and reset applicable timers for [EnemySubReinforce (086AB56C)](#trigger-086ab56c).
4. Enable and reset applicable timers for [RuskySellConYard (0C4092AC)](#trigger-0c4092ac).
5. Enable and reset applicable timers for [BringInTransports (079D905C)](#trigger-079d905c).
6. Disable [RestateObjective1 (0400805C)](#trigger-0400805c).
7. Disable [PlayerLoss3 (0BB8CADC)](#trigger-0bb8cadc).
8. Enable and reset applicable timers for [Obj1CompleteSpeech (0F874D0C)](#trigger-0f874d0c).
9. Enable and reset applicable timers for [ChangePlayerAlt2House (0D2D687C)](#trigger-0d2d687c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6321, Events line 6408, Actions line 6495.

<a id="trigger-0bb8cadc"></a>

### 48. PlayerLoss3 - 0BB8CADC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BB8C9FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6322, Events line 6409, Actions line 6496.

<a id="trigger-0f874d0c"></a>

### 49. Obj1CompleteSpeech - 0F874D0C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ConYdBuilt-Obj2Movie (0854A38C)](#trigger-0854a38c).

Attached scope: tag definitions 0F87493C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_PrimaryObjectiveAchieved.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6323, Events line 6410, Actions line 6497.

<a id="trigger-0d2d687c"></a>

### 50. ChangePlayerAlt2House - 0D2D687C

Owner reference: PlayerAlt2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [ConYdBuilt-Obj2Movie (0854A38C)](#trigger-0854a38c).

Attached scope: tag definitions 0D2D679C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6324, Events line 6411, Actions line 6498.

<a id="trigger-03ffd78c"></a>

### 51. MonkeyForce5 - 03FFD78C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: McBurger Kong (CAMSC10), owner Civilian1 House, cell (62, 63), tag 03FFBF4C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [MonkeyForce5 (0C1A48EC)](all04u-teams.md#team-0c1a48ec) at waypoint 3 (cell 65, 62).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6325, Events line 6412, Actions line 6499.

<a id="trigger-085a4b1c"></a>

### 52. PlayerCap-Disable1 - 085A4B1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RuskySellPower1 (03FAED1C)](#trigger-03faed1c).

Attached scope: Tesla Reactor (NAPOWR), owner Russian1 House, cell (79, 118), tag 03FAE76C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [RuskySellPower1 (03FAED1C)](#trigger-03faed1c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6326, Events line 6413, Actions line 6500.

<a id="trigger-085a3d6c"></a>

### 53. PlayerCap-Disable2 - 085A3D6C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RuskySellPower2 (03FAE58C)](#trigger-03fae58c).

Attached scope: Tesla Reactor (NAPOWR), owner Russian1 House, cell (79, 115), tag 03FAE38C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [RuskySellPower2 (03FAE58C)](#trigger-03fae58c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6327, Events line 6414, Actions line 6501.

<a id="trigger-085a28fc"></a>

### 54. PlayerCap-Disable3 - 085A28FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RuskySellPower3 (03FAE1AC)](#trigger-03fae1ac).

Attached scope: Tesla Reactor (NAPOWR), owner Russian1 House, cell (79, 112), tag 03FAFF4C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [RuskySellPower3 (03FAE1AC)](#trigger-03fae1ac).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6328, Events line 6415, Actions line 6502.

<a id="trigger-0860f28c"></a>

### 55. ConYardCaptured - 0860F28C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RuskySellConYard (0C4092AC)](#trigger-0c4092ac).

Attached scope: Soviet Construction Yard (NACNST), owner Russian1 House, cell (70, 114), tag 0C40911C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Destroy current instances of [RuskySellConYard (0C4092AC)](#trigger-0c4092ac).
2. Destroy current instances of [RuskySellRefinery (0878081C)](#trigger-0878081c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6329, Events line 6416, Actions line 6503.

<a id="trigger-086d2aec"></a>

### 56. GarrByBase - Easy - 086D2AEC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 086D6BBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [GarrNY18Easy (086D29BC)](all04u-teams.md#team-086d29bc) at waypoint 7 (cell 42, 103).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6330, Events line 6417, Actions line 6504.

<a id="trigger-086d06dc"></a>

### 57. GarrByBase - Med - 086D06DC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 087E4D5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [GarrNY18Medium (08762EFC)](all04u-teams.md#team-08762efc) at waypoint 7 (cell 42, 103).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6331, Events line 6418, Actions line 6505.

<a id="trigger-087f44cc"></a>

### 58. GarrByBase - Hard - 087F44CC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0880261C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [GarrNY18Hard (086E876C)](all04u-teams.md#team-086e876c) at waypoint 7 (cell 42, 103).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6332, Events line 6419, Actions line 6506.

<a id="trigger-07e8f8cc"></a>

### 59. BringInDestroyers1 - 07E8F8CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create/recruit team [EnemySubs (0C1CC67C)](all04u-teams.md#team-0c1cc67c).
2. Supply reinforcement team [Reinforce5-Dest (0D57225C)](all04u-teams.md#team-0d57225c).
3. Supply reinforcement team [Reinforce6-Dest (0D57212C)](all04u-teams.md#team-0d57212c).
4. Supply reinforcement team [Reinforce7-Dest (0D571EFC)](all04u-teams.md#team-0d571efc).
5. Supply reinforcement team [Reinforce8-Dest (0D571DCC)](all04u-teams.md#team-0d571dcc).
6. Enable and reset applicable timers for [PingTextDestroyers (07E8F09C)](#trigger-07e8f09c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6333, Events line 6420, Actions line 6507.

<a id="trigger-07e8f09c"></a>

### 60. PingTextDestroyers - 07E8F09C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BringInDestroyers1 (07E8F8CC)](#trigger-07e8f8cc); enable from [BringInDestroyers2 (0B910C3C)](#trigger-0b910c3c).

Attached scope: tag definitions 0866F28C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 22 (cell 142, 92).
2. Display message “More reinforcements have just arrived from across Lake Michigan” (MISSION:All04e).
3. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6334, Events line 6421, Actions line 6508.

<a id="trigger-0a56660c"></a>

### 61. BringInRocketeers - 0A56660C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Flak Cannon (NAFLAK), owner Russian1 House, cell (55, 95), tag 0A56652C, persistence mode 0; Flak Cannon (NAFLAK), owner Russian1 House, cell (57, 76), tag 0A56652C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [Reinforce9-Rocketeers (0D571C9C)](all04u-teams.md#team-0d571c9c).
2. Enable and reset applicable timers for [PingTextRocketeers (0A57B3DC)](#trigger-0a57b3dc).
3. Supply reinforcement team [ShockBridgeGuards (0BA2932C)](all04u-teams.md#team-0ba2932c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6335, Events line 6422, Actions line 6509.

<a id="trigger-0a57b3dc"></a>

### 62. PingTextRocketeers - 0A57B3DC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BringInRocketeers (0A56660C)](#trigger-0a56660c).

Attached scope: tag definitions 0A57BF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 28 (cell 87, 53).
2. Display message “Reinforcements have just arrived from our Canadian base” (MISSION:All04d).
3. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6336, Events line 6423, Actions line 6510.

<a id="trigger-08777f3c"></a>

### 63. Hint-Garrison - 08777F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Chicago Associates Center (CACHIG04), owner Civilian1 House, cell (49, 94), tag 087772AC, persistence mode 0; Building (CACHIG03), owner Civilian1 House, cell (48, 107), tag 087772AC, persistence mode 0; Building (CACHIG03), owner Civilian1 House, cell (48, 145), tag 087772AC, persistence mode 0; Building (CANWY22), owner Civilian1 House, cell (61, 69), tag 087772AC, persistence mode 0; Building (CANEWY18), owner Civilian1 House, cell (49, 127), tag 087772AC, persistence mode 0; Building (CATEXS05), owner Civilian1 House, cell (49, 133), tag 087772AC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “HINT: AIR UNITS are very effective for assaults on Soviet-occupied civilian structures” (MISSION:All04k).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6337, Events line 6424, Actions line 6511.

<a id="trigger-0a965cfc"></a>

### 64. TriggeredByAir - 0A965CFC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [CopCar1 (0446F20C)](all04u-teams.md#team-0446f20c).
2. Supply reinforcement team [CopCar2 (08CD76AC)](all04u-teams.md#team-08cd76ac).
3. Supply reinforcement team [CopCar3 (08CD730C)](all04u-teams.md#team-08cd730c).
4. Destroy current instances of [TriggeredByGround (0E4B05BC)](#trigger-0e4b05bc).
5. Destroy current instances of [TriggeredByGroundAlt (0E4B1F3C)](#trigger-0e4b1f3c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6338, Events line 6425, Actions line 6512.

<a id="trigger-0e4b05bc"></a>

### 65. TriggeredByGround - 0E4B05BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TriggeredByAir (0A965CFC)](#trigger-0a965cfc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Crosses Vertical Line: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [CopCar1 (0446F20C)](all04u-teams.md#team-0446f20c).
2. Supply reinforcement team [CopCar2 (08CD76AC)](all04u-teams.md#team-08cd76ac).
3. Supply reinforcement team [CopCar3 (08CD730C)](all04u-teams.md#team-08cd730c).
4. Destroy current instances of [TriggeredByAir (0A965CFC)](#trigger-0a965cfc).
5. Destroy current instances of [TriggeredByGroundAlt (0E4B1F3C)](#trigger-0e4b1f3c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6339, Events line 6426, Actions line 6513.

<a id="trigger-0e4b1f3c"></a>

### 66. TriggeredByGroundAlt - 0E4B1F3C

Owner reference: PlayerAlt2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [TriggeredByGround (0E4B05BC)](#trigger-0e4b05bc).

Attached scope: Tesla Trooper (SHK), owner Russian3 House, cell (60, 127), tag 08780B4C, persistence mode 0; Tesla Trooper (SHK), owner Russian3 House, cell (59, 126), tag 08780B4C, persistence mode 0; Tesla Trooper (SHK), owner Russian3 House, cell (60, 125), tag 08780B4C, persistence mode 0; 2 tagged map cells: (72, 122), (73, 122); tag 08780B4C, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Vertical Line: owner selector 23 (country/type PLAYERALT2; placed owner PlayerAlt2 House).

**Then perform these actions in order:**

1. Supply reinforcement team [CopCar1 (0446F20C)](all04u-teams.md#team-0446f20c).
2. Supply reinforcement team [CopCar2 (08CD76AC)](all04u-teams.md#team-08cd76ac).
3. Supply reinforcement team [CopCar3 (08CD730C)](all04u-teams.md#team-08cd730c).
4. Destroy current instances of [TriggeredByAir (0A965CFC)](#trigger-0a965cfc).
5. Destroy current instances of [TriggeredByGround (0E4B05BC)](#trigger-0e4b05bc).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6340, Events line 6427, Actions line 6514.

<a id="trigger-0868d03c"></a>

### 67. CopCarSetpiece2 - 0868D03C

Owner reference: Russian3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0868904C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (CopsArrived) is set.

**Then perform these actions in order:**

1. Create/recruit team [CopKillers (08CD6EFC)](all04u-teams.md#team-08cd6efc).
2. Make enemy: owner selector 16 (country/type COPS; placed owner Cops House).
3. Reveal terrain around waypoint 62 (cell 62, 126).
4. All to Hunt: owner selector 20 (country/type RUSSIAN3; placed owner Russian3 House).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6341, Events line 6428, Actions line 6515.

<a id="trigger-0b910c3c"></a>

### 68. BringInDestroyers2 - 0B910C3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BringInDestroyers1 (07E8F8CC)](#trigger-07e8f8cc).

Attached scope: Soviet Construction Yard (NACNST), owner Russian1 House, cell (38, 107), tag 07E8F69C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [EnemySubs (0C1CC67C)](all04u-teams.md#team-0c1cc67c).
2. Supply reinforcement team [Reinforce5-Dest (0D57225C)](all04u-teams.md#team-0d57225c).
3. Supply reinforcement team [Reinforce6-Dest (0D57212C)](all04u-teams.md#team-0d57212c).
4. Supply reinforcement team [Reinforce7-Dest (0D571EFC)](all04u-teams.md#team-0d571efc).
5. Supply reinforcement team [Reinforce8-Dest (0D571DCC)](all04u-teams.md#team-0d571dcc).
6. Enable and reset applicable timers for [PingTextDestroyers (07E8F09C)](#trigger-07e8f09c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6342, Events line 6429, Actions line 6516.

<a id="trigger-0bc2b68c"></a>

### 69. TankAttackGar1 - 0BC2B68C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY06), owner Civilian1 House, cell (48, 122), tag 0BC2B14C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [TankAttackWSO (0BC2A80C)](all04u-teams.md#team-0bc2a80c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6343, Events line 6430, Actions line 6517.

<a id="trigger-0bc2db3c"></a>

### 70. TankAttackGar2 - 0BC2DB3C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CATEXS03), owner Civilian1 House, cell (48, 119), tag 0BC2D93C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [TankAttackSAO (0BC2A11C)](all04u-teams.md#team-0bc2a11c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6344, Events line 6431, Actions line 6518.

<a id="trigger-0bc2ad8c"></a>

### 71. TankAttackGar3 - 0BC2AD8C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANWY23), owner Civilian1 House, cell (48, 117), tag 0BC28F4C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [TankAttackNY23 (0BC2CA5C)](all04u-teams.md#team-0bc2ca5c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6345, Events line 6432, Actions line 6519.

<a id="trigger-0bc28ddc"></a>

### 72. TankAttackGar4 - 0BC28DDC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CACHIG02), owner Civilian1 House, cell (49, 114), tag 0BC288FC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [TankAttackChigoBrick2 (0BC2F4FC)](all04u-teams.md#team-0bc2f4fc).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6346, Events line 6433, Actions line 6520.

<a id="trigger-0c032e5c"></a>

### 73. Crate - WaterTreatment - 0C032E5C

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Office Building (CATEXS08), owner Civilian1 House, cell (122, 31), tag 0C0322DC, persistence mode 0; Office Building (CATEXS08), owner Civilian1 House, cell (122, 34), tag 0C0322DC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 71 (cell 118, 33).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6347, Events line 6434, Actions line 6521.

<a id="trigger-089c433c"></a>

### 74. StartingDestroyersDead - Easy - 089C433C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: Destroyer (DEST), owner Player House, cell (155, 92), tag 089C749C, persistence mode 1; Destroyer (DEST), owner Player House, cell (156, 91), tag 089C749C, persistence mode 1; Destroyer (DEST), owner Player House, cell (157, 90), tag 089C749C, persistence mode 1; Destroyer (DEST), owner Player House, cell (158, 89), tag 089C749C, persistence mode 1; Destroyer (DEST), owner Player House, cell (159, 88), tag 089C749C, persistence mode 1; Destroyer (DEST), owner Player House, cell (160, 87), tag 089C749C, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [StartingDest1 (0B1B559C)](all04u-teams.md#team-0b1b559c).
2. Supply reinforcement team [StartingDest2 (0B1BE6AC)](all04u-teams.md#team-0b1be6ac).
3. Supply reinforcement team [StartingDest3 (0B1BE30C)](all04u-teams.md#team-0b1be30c).
4. Supply reinforcement team [StartingDest4 (0B1BDC8C)](all04u-teams.md#team-0b1bdc8c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6348, Events line 6435, Actions line 6522.

<a id="trigger-0afed8fc"></a>

### 75. RefineryCaptured - 0AFED8FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [RuskySellRefinery (0878081C)](#trigger-0878081c).

Attached scope: Soviet Ore Refinery (NAREFN), owner Russian1 House, cell (66, 110), tag 0878039C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Destroy current instances of [RuskySellRefinery (0878081C)](#trigger-0878081c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6349, Events line 6436, Actions line 6523.

<a id="trigger-088202ec"></a>

### 76. GenerateSubs - HARD - 088202EC

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0882008C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [SpawnedSubs (08821D2C)](all04u-teams.md#team-08821d2c) at waypoint 92 (cell 98, 122).
2. Supply reinforcement team [SpawnedSubs (08821D2C)](all04u-teams.md#team-08821d2c) at waypoint 93 (cell 102, 106).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6350, Events line 6437, Actions line 6524.

<a id="trigger-08821f3c"></a>

### 77. GenerateSubs - MED - 08821F3C

Owner reference: Russian1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08821E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [SpawnedSubs (08821D2C)](all04u-teams.md#team-08821d2c) at waypoint 93 (cell 102, 106).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6351, Events line 6438, Actions line 6525.

<a id="trigger-0afb803c"></a>

### 78. StartRocketeers - EASY - 0AFB803C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AFC104C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [StartingRocket(L) - EASY (044699CC)](all04u-teams.md#team-044699cc) at waypoint 18 (cell 155, 89).
2. Supply reinforcement team [StartingRocket(R) - EASY (0D57E67C)](all04u-teams.md#team-0d57e67c) at waypoint 18 (cell 155, 89).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6352, Events line 6439, Actions line 6526.

<a id="trigger-087dfc8c"></a>

### 79. StartRocketeers - MED - 087DFC8C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 087DF73C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [StartingRocket(L) - MED (0D57DC8C)](all04u-teams.md#team-0d57dc8c) at waypoint 18 (cell 155, 89).
2. Supply reinforcement team [StartingRocket(R) - MED (0D57D7DC)](all04u-teams.md#team-0d57d7dc) at waypoint 18 (cell 155, 89).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6353, Events line 6440, Actions line 6527.

<a id="trigger-087dbccc"></a>

### 80. StartRocketeers - HARD - 087DBCCC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 087DBACC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [StartingRocket - HARD (0D57D43C)](all04u-teams.md#team-0d57d43c) at waypoint 18 (cell 155, 89).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6354, Events line 6441, Actions line 6528.

<a id="trigger-0f3eb96c"></a>

### 81. GrabMCV - 0F3EB96C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0F3EB2FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [PlayerMCV (0B1C230C)](all04u-teams.md#team-0b1c230c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6355, Events line 6442, Actions line 6529.

<a id="trigger-0f3eb20c"></a>

### 82. Hint-MCV - 0F3EB20C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0F3EEF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (mcvUnloaded) is set.

**Then perform these actions in order:**

1. Flash team [PlayerMCV (0B1C230C)](all04u-teams.md#team-0b1c230c) with duration setting 80.
2. Disable [GrabMCV (0F3EB96C)](#trigger-0f3eb96c).
3. Display message “Deploy your Mobile Construction Vehicle into a Construction Yard” (MISSION:All04m).
4. Enable and reset applicable timers for [Hint-MCV2 (0AEB7A4C)](#trigger-0aeb7a4c).
5. Disable [PlayerLoss3 (0BB8CADC)](#trigger-0bb8cadc).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6356, Events line 6443, Actions line 6530.

<a id="trigger-0aeb7a4c"></a>

### 83. Hint-MCV2 - 0AEB7A4C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint-MCV (0F3EB20C)](#trigger-0f3eb20c).

Attached scope: tag definitions 0AEB796C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [PlayerMCV (0B1C230C)](all04u-teams.md#team-0b1c230c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6357, Events line 6444, Actions line 6531.

<a id="trigger-08953eac"></a>

### 84. SearsCaptured - 08953EAC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Sears Tower (CACHIG05), owner Civilian1 House, cell (16, 114), tag 08953A0C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Reveal the whole map.

Source locator: MAPS01.MIX/all04u.map; Triggers line 6358, Events line 6445, Actions line 6532.

<a id="trigger-0b0d117c"></a>

### 85. StartNavyEnters2 - 0B0D117C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B0D71FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [StartingForce1 (0A6A8B3C)](all04u-teams.md#team-0a6a8b3c).
2. Supply reinforcement team [StartingForce2 (0D592A4C)](all04u-teams.md#team-0d592a4c).
3. Supply reinforcement team [StartingForce3 (0D59259C)](all04u-teams.md#team-0d59259c).
4. Supply reinforcement team [StartingForce4 (0D59946C)](all04u-teams.md#team-0d59946c).

Source locator: MAPS01.MIX/all04u.map; Triggers line 6359, Events line 6446, Actions line 6533.

[All team rosters and ordered plans](all04u-teams.md) | [All mission overrides](all04u-overrides.md)
