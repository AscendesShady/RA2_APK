# Operation: Sun Temple

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for all09t.map.](../../images/map-all09t.svg)

*Initial placement schematic for all09t.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** all09t.map. **Effective extracted member:** MAPS01.MIX/all09t.map. **Trigger definitions:** 80.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all09t-teams.md) | [All mission overrides](all09t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | TEMPERATE |
| Map size | 0,0,85,90 |
| Visible local rectangle | 5,5,75,79 |
| Placed vehicles | 17 |
| Placed infantry | 112 |
| Placed structures | 96 |
| Placed aircraft | 0 |
| Team templates | 37 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 25 | BadGuy1 |
| 2 | BadGuy2 House | 0 | BadGuy2 |
| 3 | BadGuy3 House | 0 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 0 | Other1 |
| 6 | Other2 House | 0 | Other2 |
| 7 | Other3 House | 0 | Other3 |
| 8 | House Balabos | 0 | Balabos |
| 9 | Hack House | 50 | Hack |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | SEALs onsite,0 |
| 1 | POWs Rescued,0 |
| 2 | POW Vehicles Freed,0 |
| 3 | Players Has Airport,0 |
| 4 | BG1 KIA,0 |
| 5 | Balabos KIA,0 |
| 6 | Barracks Destroyed,0 |
| 7 | War Fact Destroyed,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [_Loss (07C90E40)](#trigger-07c90e40) | Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House). | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [_Win Text (0D2B6F3C)](#trigger-0d2b6f3c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-03d82a60"></a>

### 1. Base Life - 03D82A60

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (80, 109); tag 03D86850, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Dog Patrol A (07B61310)](all09t-teams.md#team-07b61310).
2. Create/recruit team [BG1 Dog Patrol B (07B9DCA0)](all09t-teams.md#team-07b9dca0).
3. Create/recruit team [BG1 Perimeter Patrol A (099427E0)](all09t-teams.md#team-099427e0).
4. Create/recruit team [BG1 Perimeter Patrol B (0992EA00)](all09t-teams.md#team-0992ea00).
5. Create/recruit team [Shock @ Y (08BE8B80)](all09t-teams.md#team-08be8b80).
6. Create/recruit team [Shock @ Z (08BE8700)](all09t-teams.md#team-08be8700).
7. Create/recruit team [BG1 Beach Patrol (08C08A80)](all09t-teams.md#team-08c08a80).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4586, Events line 4668, Actions line 4750.

<a id="trigger-03d87830"></a>

### 2. SEAL Insertion GO - 03D87830

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (79, 19); tag 03D872D0, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [SEAL Insertion (0C1691FC)](all09t-teams.md#team-0c1691fc).
2. Enable and reset applicable timers for [Move Camera LZ (0A7956F0)](#trigger-0a7956f0).
3. Disable player input.
4. Reveal terrain around waypoint 98 (cell 74, 24).
5. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4587, Events line 4669, Actions line 4751.

<a id="trigger-0a7956f0"></a>

### 3. Move Camera LZ - 0A7956F0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [SEAL Insertion GO (03D87830)](#trigger-03d87830).

Attached scope: tag definitions 0A795210 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 10 (cell 73, 44) with speed setting 1.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4588, Events line 4670, Actions line 4752.

<a id="trigger-07ba0bd0"></a>

### 4. Seals have Landed - 07BA0BD0

Owner reference: Other3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 25 tagged map cells: (71, 43), (72, 43), (73, 43), (74, 43), (75, 43), (71, 44), (72, 44), (73, 44), (74, 44), (75, 44), (71, 45), (72, 45), (73, 45), (74, 45), (75, 45), (71, 46), (72, 46), (73, 46), (74, 46), (75, 46), (71, 47), (72, 47), (73, 47), (74, 47), (75, 47); tag 07BA4F50, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable player input.
2. Enable and reset applicable timers for [_Loss (07C90E40)](#trigger-07c90e40).
3. Remove instances of the team organization (not automatically its surviving objects) [SEAL Insertion (0C1691FC)](all09t-teams.md#team-0c1691fc).
4. Display message “Objective 1: Capture or Eliminate Soviet Research Facility within the Pyramid Ruins” (MISSION:All09a).
5. Display message “Objective 2: Destroy the Soviet base” (MISSION:All09b).
6. Play voice notification EVA_BattlefieldControlOnline.
7. Reveal terrain around waypoint 13 (cell 60, 81).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4589, Events line 4671, Actions line 4753.

<a id="trigger-07c90e40"></a>

### 5. _Loss - 07C90E40

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Seals have Landed (07BA0BD0)](#trigger-07ba0bd0).

Attached scope: tag definitions 07C90BE0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4590, Events line 4672, Actions line 4754.

<a id="trigger-09041cb0"></a>

### 6. Village Life - 09041CB0

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (60, 77); tag 0904B030, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Vehicle Guard (090EB140)](all09t-teams.md#team-090eb140).
2. Create/recruit team [BG2 Village Guard A (08B88BA0)](all09t-teams.md#team-08b88ba0).
3. Create/recruit team [BG2 Village Guard B (08B88820)](all09t-teams.md#team-08b88820).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4591, Events line 4673, Actions line 4755.

<a id="trigger-07a7e110"></a>

### 7. Rescue POWs - 07A7E110

Owner reference: Other2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Conscript (E2), owner BadGuy2 House, cell (64, 82), tag 07AB62E0, persistence mode 1; Conscript (E2), owner BadGuy2 House, cell (64, 81), tag 07AB62E0, persistence mode 1; Conscript (E2), owner BadGuy2 House, cell (63, 83), tag 07AB62E0, persistence mode 1; Conscript (E2), owner BadGuy2 House, cell (63, 79), tag 07AB62E0, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 1 (POWs Rescued).
2. Create radar-event marker type 1 at waypoint 18 (cell 55, 86).
3. Reveal terrain around waypoint 18 (cell 55, 86).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4592, Events line 4674, Actions line 4756.

<a id="trigger-07b23080"></a>

### 8. Rescue Vehicles - 07B23080

Owner reference: Other2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Conscript (E2), owner BadGuy2 House, cell (59, 86), tag 07B27F20, persistence mode 1; Conscript (E2), owner BadGuy2 House, cell (60, 86), tag 07B27F20, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 2 (POW Vehicles Freed).
2. Create radar-event marker type 1 at waypoint 13 (cell 60, 81).
3. Reveal terrain around waypoint 19 (cell 60, 79).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4593, Events line 4675, Actions line 4757.

<a id="trigger-07c90810"></a>

### 9. _Win - 07C90810

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C98130 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 21 (country/type BALABOS; placed owner House Balabos).
2. Destroyed,  Buildings,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Win Text (0D2B6F3C)](#trigger-0d2b6f3c).
2. Enable and reset applicable timers for [Cheer (0ADD32AC)](#trigger-0add32ac).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4594, Events line 4676, Actions line 4758.

<a id="trigger-0d2b6f3c"></a>

### 10. _Win Text - 0D2B6F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Win (07C90810)](#trigger-07c90810).

Attached scope: tag definitions 0D2B6E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4595, Events line 4677, Actions line 4759.

<a id="trigger-0add32ac"></a>

### 11. Cheer - 0ADD32AC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Win (07C90810)](#trigger-07c90810).

Attached scope: tag definitions 0ADD31CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4596, Events line 4678, Actions line 4760.

<a id="trigger-08f54b80"></a>

### 12. POW GI Freed - 08F54B80

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: GI (E1), owner Other2 House, cell (67, 82), tag 08F52120, persistence mode 0; GI (E1), owner Other2 House, cell (67, 82), tag 08F52120, persistence mode 0; GI (E1), owner Other2 House, cell (66, 82), tag 08F52120, persistence mode 0; GI (E1), owner Other2 House, cell (66, 80), tag 08F52120, persistence mode 0; GI (E1), owner Other2 House, cell (66, 81), tag 08F52120, persistence mode 0; GI (E1), owner Other2 House, cell (67, 81), tag 08F52120, persistence mode 0; GI (E1), owner Other2 House, cell (67, 80), tag 08F52120, persistence mode 0; GI (E1), owner Other2 House, cell (66, 81), tag 08F52120, persistence mode 0; GI (E1), owner Other2 House, cell (66, 80), tag 08F52120, persistence mode 0; GI (E1), owner Other2 House, cell (67, 81), tag 08F52120, persistence mode 0.

**Wait for the recorded events:**

1. local flag 1 (POWs Rescued) is set.

Flag writers in this mission: set local flag 1 (POWs Rescued) at [Rescue POWs (07A7E110)](#trigger-07a7e110). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Play voice notification Mis_A9_SealFightersJoining.
3. Enable and reset applicable timers for [POW Movie (09FCACFC)](#trigger-09fcacfc).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4597, Events line 4679, Actions line 4761.

<a id="trigger-09fcacfc"></a>

### 13. POW Movie - 09FCACFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [POW GI Freed (08F54B80)](#trigger-08f54b80).

Attached scope: tag definitions 09FCA84C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 129.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4598, Events line 4680, Actions line 4762.

<a id="trigger-08f55400"></a>

### 14. POW Vehicles Freed - 08F55400

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Grizzly Battle Tank (MTNK), owner Other2 House, cell (58, 88), tag 08F53CF0, persistence mode 0; Grizzly Battle Tank (MTNK), owner Other2 House, cell (60, 89), tag 08F53CF0, persistence mode 0.

**Wait for the recorded events:**

1. local flag 2 (POW Vehicles Freed) is set.

Flag writers in this mission: set local flag 2 (POW Vehicles Freed) at [Rescue Vehicles (07B23080)](#trigger-07b23080). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Supply reinforcement team [Heli_Engineer Reinforce (0F54A24C)](all09t-teams.md#team-0f54a24c).
3. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4599, Events line 4681, Actions line 4763.

<a id="trigger-07b21820"></a>

### 15. BG1 Check POW - 07B21820

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B21170 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (POW Vehicles Freed) is set.
2. local flag 1 (POWs Rescued) is set.

Flag writers in this mission: set local flag 2 (POW Vehicles Freed) at [Rescue Vehicles (07B23080)](#trigger-07b23080); set local flag 1 (POWs Rescued) at [Rescue POWs (07A7E110)](#trigger-07a7e110). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 POW Check A (07B093D0)](all09t-teams.md#team-07b093d0).
2. Supply reinforcement team [BG1 POW Check B (07B22790)](all09t-teams.md#team-07b22790).
3. Reveal terrain around waypoint 1 (cell 69, 112).
4. Reveal terrain around waypoint 3 (cell 72, 127).
5. Reveal terrain around waypoint 38 (cell 118, 124).
6. Reveal terrain around waypoint 46 (cell 80, 97).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4600, Events line 4682, Actions line 4764.

<a id="trigger-09947100"></a>

### 16. BG3 Airport Team KIA - 09947100

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09942680 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 3 (Players Has Airport).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4601, Events line 4683, Actions line 4765.

<a id="trigger-09940b80"></a>

### 17. Player Captures Airport - 09940B80

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 099409B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 70 (global list position: Tech Airport (CAAIRP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 3 (Players Has Airport).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4602, Events line 4684, Actions line 4766.

<a id="trigger-099408d0"></a>

### 18. BG3 Airport Engineers - 099408D0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09940630 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Players Has Airport) is set.

Flag writers in this mission: set local flag 3 (Players Has Airport) at [BG3 Airport Team KIA (09947100)](#trigger-09947100); set local flag 3 (Players Has Airport) at [Player Captures Airport (09940B80)](#trigger-09940b80); clear local flag 3 (Players Has Airport) at [BG3 Airport Engineers (099408D0)](#trigger-099408d0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [BG3 Assimilate Airport (08BA34E0)](all09t-teams.md#team-08ba34e0).
2. Clear local flag 3 (Players Has Airport).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4603, Events line 4685, Actions line 4767.

<a id="trigger-0a741b80"></a>

### 19. Stop BG3 Airport Engineers - 0A741B80

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7412A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 6.

**Then perform these actions in order:**

1. Disable [BG3 Airport Engineers (099408D0)](#trigger-099408d0).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4604, Events line 4686, Actions line 4768.

<a id="trigger-09a4e1c0"></a>

### 20. BG1 Attk Response 1 - 09A4E1C0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Rhino Heavy Tank (HTNK), owner BadGuy1 House, cell (69, 114), tag 07C10A50, persistence mode 0; Rhino Heavy Tank (HTNK), owner BadGuy1 House, cell (71, 112), tag 07C10A50, persistence mode 0; Tesla Trooper (SHK), owner BadGuy1 House, cell (69, 109), tag 07C10A50, persistence mode 0; Tesla Trooper (SHK), owner BadGuy1 House, cell (66, 112), tag 07C10A50, persistence mode 0; Tesla Coil (TESLA), owner BadGuy1 House, cell (65, 112), tag 07C10A50, persistence mode 0; Tesla Coil (TESLA), owner BadGuy1 House, cell (69, 108), tag 07C10A50, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Attk Response 1A (09A4D390)](all09t-teams.md#team-09a4d390).
2. Create/recruit team [BG1 Attk Response 1B (03DA2F00)](all09t-teams.md#team-03da2f00).
3. Create/recruit team [BG1 Attk Response 1C1 (03DA2590)](all09t-teams.md#team-03da2590).
4. Create/recruit team [BG1 Attk Response 1C2 (03DA1BB0)](all09t-teams.md#team-03da1bb0).
5. Create/recruit team [BG1 Attk Response 1C3 (03D57860)](all09t-teams.md#team-03d57860).
6. Create/recruit team [BG1 Attk Response 1C4 (03D5D810)](all09t-teams.md#team-03d5d810).
7. Create/recruit team [BG1 Attk Response 1C5 (03D70180)](all09t-teams.md#team-03d70180).
8. Create/recruit team [BG1 Attk Response D (03D73A40)](all09t-teams.md#team-03d73a40).
9. Disable [BG1 Attk Response 2 (09994840)](#trigger-09994840).
10. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
11. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4605, Events line 4687, Actions line 4769.

<a id="trigger-09994840"></a>

### 21. BG1 Attk Response 2 - 09994840

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Attacked Radar (0AF418FC)](#trigger-0af418fc).

Attached scope: Rhino Heavy Tank (HTNK), owner BadGuy1 House, cell (74, 128), tag 09991F50, persistence mode 0; Rhino Heavy Tank (HTNK), owner BadGuy1 House, cell (71, 125), tag 09991F50, persistence mode 0; Flak Track (HTK), owner BadGuy1 House, cell (77, 132), tag 09991F50, persistence mode 0; Sentry Gun (NALASR), owner BadGuy1 House, cell (68, 127), tag 09991F50, persistence mode 0; Sentry Gun (NALASR), owner BadGuy1 House, cell (72, 131), tag 09991F50, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Attk Response D (03D73A40)](all09t-teams.md#team-03d73a40).
2. Disable [BG1 Attk Response 1 (09A4E1C0)](#trigger-09a4e1c0).
3. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
4. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
5. Create/recruit team [BG1 Attk Response 2A (07BEAC60)](all09t-teams.md#team-07beac60).
6. Create/recruit team [BG1 Attk Response 2B (08B8C340)](all09t-teams.md#team-08b8c340).
7. Create/recruit team [BG1 Attk Response 2C1 (08B89DF0)](all09t-teams.md#team-08b89df0).
8. Create/recruit team [BG1 Attk Response 2C2 (08B897A0)](all09t-teams.md#team-08b897a0).
9. Create/recruit team [BG1 Attk Response 2C3 (08B73580)](all09t-teams.md#team-08b73580).
10. Create/recruit team [BG1 Attk Response 2C4 (08B71050)](all09t-teams.md#team-08b71050).
11. Create/recruit team [BG1 Attk Response 2C5 (08B87EC0)](all09t-teams.md#team-08b87ec0).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4606, Events line 4688, Actions line 4770.

<a id="trigger-0a7af510"></a>

### 22. BG1 Flak Patrol Begin - 0A7AF510

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Flak Patrol Enable (0A7AF750)](#trigger-0a7af750).

Attached scope: tag definitions 0A7AF2E0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 Flak Patrol (08C15280)](all09t-teams.md#team-08c15280).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4607, Events line 4689, Actions line 4771.

<a id="trigger-0a7af750"></a>

### 23. BG1 Flak Patrol Enable - 0A7AF750

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7AA3C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (POW Vehicles Freed) is set.

Flag writers in this mission: set local flag 2 (POW Vehicles Freed) at [Rescue Vehicles (07B23080)](#trigger-07b23080). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 Flak Patrol Begin (0A7AF510)](#trigger-0a7af510).
2. Supply reinforcement team [BG1 Flak Patrol (08C15280)](all09t-teams.md#team-08c15280).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4608, Events line 4690, Actions line 4772.

<a id="trigger-0a7aac10"></a>

### 24. Flak Patrol Disable (Easy) - 0A7AAC10

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable [BG1 Flak Patrol Begin (0A7AF510)](#trigger-0a7af510).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4609, Events line 4691, Actions line 4773.

<a id="trigger-0a7aed30"></a>

### 25. Flak Patrol Disable (Med) - 0A7AED30

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Flak Patrol Disable (Easy) (0A7AAC10)](#trigger-0a7aac10).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable [BG1 Flak Patrol Begin (0A7AF510)](#trigger-0a7af510).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4610, Events line 4692, Actions line 4774.

<a id="trigger-0a7abb20"></a>

### 26. Flak Patrol Disable (Hard) - 0A7ABB20

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Flak Patrol Disable (Med) (0A7AED30)](#trigger-0a7aed30).

Attached scope: tag definitions 0A7AE7B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [BG1 Flak Patrol Begin (0A7AF510)](#trigger-0a7af510).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4611, Events line 4693, Actions line 4775.

<a id="trigger-098d410c"></a>

### 27. Balabos KIA - 098D410C

Owner reference: Balabos. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 098D609C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 21 (country/type BALABOS; placed owner House Balabos).

**Then perform these actions in order:**

1. Set local flag 5 (Balabos KIA).
2. Display message “Objective 1 Accomplished” (MISSION:All09c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4612, Events line 4694, Actions line 4776.

<a id="trigger-098d135c"></a>

### 28. BG1 KIA - 098D135C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 098D30FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Set local flag 4 (BG1 KIA).
2. Display message “Objective 2 Accomplished” (MISSION:All09d).
3. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4613, Events line 4695, Actions line 4777.

<a id="trigger-08f5556c"></a>

### 29. Reveal Around AN - 08F5556C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08F5064C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 39 (cell 81, 27).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4614, Events line 4696, Actions line 4778.

<a id="trigger-08eae54c"></a>

### 30. Reveal Around AO - 08EAE54C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08EA9BBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 40 (cell 76, 37).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4615, Events line 4697, Actions line 4779.

<a id="trigger-079b5e3c"></a>

### 31. Reveal Around K - 079B5E3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079B59EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 21 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 10 (cell 73, 44).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4616, Events line 4698, Actions line 4780.

<a id="trigger-08b266fc"></a>

### 32. Hack of the Airport - 08B266FC

Owner reference: Hack. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tech Airport (CAAIRP), owner Other1 House, cell (18, 90), tag 08B2627C, persistence mode 2.

**Wait for the recorded events:**

1. Building exists: type index 70 (global list position: Tech Airport (CAAIRP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Switch the sidebar to tab 1.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4617, Events line 4699, Actions line 4781.

<a id="trigger-08b9b8dc"></a>

### 33. Player Owns Prism Pyramid - 08B9B8DC

Owner reference: Hack. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B9CF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 143 (global list position: Mayan Pyramid (MAYAN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 30 (cell 80, 118).
2. Reveal terrain around waypoint 2 (cell 67, 118).
3. Reveal terrain around waypoint 41 (cell 98, 124).
4. Reveal terrain around waypoint 4 (cell 88, 140).
5. Reveal terrain around waypoint 5 (cell 101, 140).
6. Reveal terrain around waypoint 33 (cell 86, 122).
7. Reveal terrain around waypoint 42 (cell 89, 107).
8. Reveal terrain around waypoint 43 (cell 84, 131).
9. Reveal terrain around waypoint 44 (cell 108, 132).
10. Reveal terrain around waypoint 45 (cell 106, 120).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4618, Events line 4700, Actions line 4782.

<a id="trigger-0af418fc"></a>

### 34. Attacked Radar - 0AF418FC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 Attk Response 2 (09994840)](#trigger-09994840).
2. Disable [Attacked Radar (0AF418FC)](#trigger-0af418fc).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4619, Events line 4701, Actions line 4783.

<a id="trigger-0af4172c"></a>

### 35. Captured Radar - 0AF4172C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Attacked Radar (0AF418FC)](#trigger-0af418fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Radar (0D55451C)](#trigger-0d55451c).
2. Disable [Captured Radar (0AF4172C)](#trigger-0af4172c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4620, Events line 4702, Actions line 4784.

<a id="trigger-0d55451c"></a>

### 36. Change Radar - 0D55451C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Captured Radar (0AF4172C)](#trigger-0af4172c).

Incoming activation links: enable from [Captured Radar (0AF4172C)](#trigger-0af4172c).

Attached scope: Radar Tower (NARADR), owner BadGuy1 House, cell (83, 133), tag 0AF4181C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Radar (0D55451C)](#trigger-0d55451c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4621, Events line 4703, Actions line 4785.

<a id="trigger-0a09df3c"></a>

### 37. Captured Barracks - 0A09DF3C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Barracks (0D5547DC)](#trigger-0d5547dc).
2. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
4. Disable [Captured Barracks (0A09DF3C)](#trigger-0a09df3c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4622, Events line 4704, Actions line 4786.

<a id="trigger-0d5547dc"></a>

### 38. Change Barracks - 0D5547DC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Destroyed Barracks (0A09EE9C)](#trigger-0a09ee9c).

Incoming activation links: enable from [Captured Barracks (0A09DF3C)](#trigger-0a09df3c).

Attached scope: Soviet Barracks (NAHAND), owner BadGuy1 House, cell (79, 116), tag 0A09DE5C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Barracks (0D5547DC)](#trigger-0d5547dc).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4623, Events line 4705, Actions line 4787.

<a id="trigger-0a09ee9c"></a>

### 39. Destroyed Barracks - 0A09EE9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Captured Barracks (0A09DF3C)](#trigger-0a09df3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 6 (Barracks Destroyed).
2. Disable [Destroyed Barracks (0A09EE9C)](#trigger-0a09ee9c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4624, Events line 4706, Actions line 4788.

<a id="trigger-0a0b9cdc"></a>

### 40. Destroyed War Factory - 0A0B9CDC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 7 (War Fact Destroyed).
2. Disable [Destroyed War Factory (0A0B9CDC)](#trigger-0a0b9cdc).
3. Disable [BG1 Flak Patrol Begin (0A7AF510)](#trigger-0a7af510).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4625, Events line 4707, Actions line 4789.

<a id="trigger-0a0b9b0c"></a>

### 41. Captured War Factory - 0A0B9B0C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Destroyed War Factory (0A0B9CDC)](#trigger-0a0b9cdc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change War Factory (0D55425C)](#trigger-0d55425c).
2. Disable [Captured War Factory (0A0B9B0C)](#trigger-0a0b9b0c).
3. Create/recruit team [Attack WarFactory (09848EFC)](all09t-teams.md#team-09848efc).
4. Disable [BG1 Flak Patrol Begin (0A7AF510)](#trigger-0a7af510).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4626, Events line 4708, Actions line 4790.

<a id="trigger-0d55425c"></a>

### 42. Change War Factory - 0D55425C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Captured War Factory (0A0B9B0C)](#trigger-0a0b9b0c).

Incoming activation links: enable from [Captured War Factory (0A0B9B0C)](#trigger-0a0b9b0c).

Attached scope: Soviet War Factory (NAWEAP), owner BadGuy1 House, cell (80, 125), tag 0A0B9BFC, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change War Factory (0D55425C)](#trigger-0d55425c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4627, Events line 4709, Actions line 4791.

<a id="trigger-0a0a2e5c"></a>

### 43. Captured Service Depot - 0A0A2E5C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change Service Depot (0D5549EC)](#trigger-0d5549ec).

Attached scope: Soviet Repair Depot (NADEPT), owner BadGuy1 House, cell (86, 120), tag 08A2017C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Service Depot (0D5549EC)](#trigger-0d5549ec).
2. Disable [Captured Service Depot (0A0A2E5C)](#trigger-0a0a2e5c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4628, Events line 4710, Actions line 4792.

<a id="trigger-0d5549ec"></a>

### 44. Change Service Depot - 0D5549EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Service Depot (0A0A2E5C)](#trigger-0a0a2e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Service Depot (0D5549EC)](#trigger-0d5549ec).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4629, Events line 4711, Actions line 4793.

<a id="trigger-0a0a156c"></a>

### 45. Captured Con Yard - 0A0A156C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change Con Yard (0D554BFC)](#trigger-0d554bfc).

Attached scope: Soviet Construction Yard (NACNST), owner BadGuy1 House, cell (89, 130), tag 0DCCF76C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Con Yard (0D554BFC)](#trigger-0d554bfc).
2. Create/recruit team [Attack ConYard (098487CC)](all09t-teams.md#team-098487cc).
3. Disable [Captured Con Yard (0A0A156C)](#trigger-0a0a156c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4630, Events line 4712, Actions line 4794.

<a id="trigger-0d554bfc"></a>

### 46. Change Con Yard - 0D554BFC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Con Yard (0A0A156C)](#trigger-0a0a156c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Con Yard (0D554BFC)](#trigger-0d554bfc).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4631, Events line 4713, Actions line 4795.

<a id="trigger-0a0a108c"></a>

### 47. Captured Battle Lab - 0A0A108C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change Battle Lab (0D554E0C)](#trigger-0d554e0c).

Attached scope: Soviet Battle Lab (NATECH), owner BadGuy1 House, cell (95, 125), tag 0DCB21EC, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Battle Lab (0D554E0C)](#trigger-0d554e0c).
2. Disable [Captured Battle Lab (0A0A108C)](#trigger-0a0a108c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4632, Events line 4714, Actions line 4796.

<a id="trigger-0d554e0c"></a>

### 48. Change Battle Lab - 0D554E0C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Battle Lab (0A0A108C)](#trigger-0a0a108c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Battle Lab (0D554E0C)](#trigger-0d554e0c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4633, Events line 4715, Actions line 4797.

<a id="trigger-0a0bb09c"></a>

### 49. Captured Refinery 1 - 0A0BB09C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Refinery 1 (0E803D6C)](#trigger-0e803d6c).
2. Disable [Captured Refinery 1 (0A0BB09C)](#trigger-0a0bb09c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4634, Events line 4716, Actions line 4798.

<a id="trigger-0e803d6c"></a>

### 50. Change Refinery 1 - 0E803D6C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Captured Refinery 1 (0A0BB09C)](#trigger-0a0bb09c).

Incoming activation links: enable from [Captured Refinery 1 (0A0BB09C)](#trigger-0a0bb09c).

Attached scope: Soviet Ore Refinery (NAREFN), owner BadGuy1 House, cell (98, 136), tag 0E803C8C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Refinery 1 (0E803D6C)](#trigger-0e803d6c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4635, Events line 4717, Actions line 4799.

<a id="trigger-0a0bf3ec"></a>

### 51. Captured Refinery 2 - 0A0BF3EC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Refinery 2 (0E80335C)](#trigger-0e80335c).
2. Disable [Captured Refinery 2 (0A0BF3EC)](#trigger-0a0bf3ec).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4636, Events line 4718, Actions line 4800.

<a id="trigger-0e80335c"></a>

### 52. Change Refinery 2 - 0E80335C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Captured Refinery 2 (0A0BF3EC)](#trigger-0a0bf3ec).

Incoming activation links: enable from [Captured Refinery 2 (0A0BF3EC)](#trigger-0a0bf3ec).

Attached scope: Soviet Ore Refinery (NAREFN), owner BadGuy1 House, cell (102, 131), tag 0E80327C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Refinery 2 (0E80335C)](#trigger-0e80335c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4637, Events line 4719, Actions line 4801.

<a id="trigger-0a0bccac"></a>

### 53. Captured Reactor 1 - 0A0BCCAC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change Reactor 1 (0D5519EC)](#trigger-0d5519ec).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy1 House, cell (85, 113), tag 0DCCF29C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Reactor 1 (0D5519EC)](#trigger-0d5519ec).
2. Disable [Captured Reactor 1 (0A0BCCAC)](#trigger-0a0bccac).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4638, Events line 4720, Actions line 4802.

<a id="trigger-0d5519ec"></a>

### 54. Change Reactor 1 - 0D5519EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Reactor 1 (0A0BCCAC)](#trigger-0a0bccac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Reactor 1 (0D5519EC)](#trigger-0d5519ec).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4639, Events line 4721, Actions line 4803.

<a id="trigger-0a0bcadc"></a>

### 55. Captured Reactor 2 - 0A0BCADC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change Reactor 2 (0D5514CC)](#trigger-0d5514cc).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy1 House, cell (90, 105), tag 0DCC8F4C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Reactor 2 (0D5514CC)](#trigger-0d5514cc).
2. Disable [Captured Reactor 2 (0A0BCADC)](#trigger-0a0bcadc).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4640, Events line 4722, Actions line 4804.

<a id="trigger-0d5514cc"></a>

### 56. Change Reactor 2 - 0D5514CC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Reactor 2 (0A0BCADC)](#trigger-0a0bcadc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Reactor 2 (0D5514CC)](#trigger-0d5514cc).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4641, Events line 4723, Actions line 4805.

<a id="trigger-0a0bc80c"></a>

### 57. Captured Reactor 3 - 0A0BC80C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change Reactor 3 (0D5512BC)](#trigger-0d5512bc).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy1 House, cell (90, 142), tag 0DCC8D7C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Reactor 3 (0D5512BC)](#trigger-0d5512bc).
2. Disable [Captured Reactor 3 (0A0BC80C)](#trigger-0a0bc80c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4642, Events line 4724, Actions line 4806.

<a id="trigger-0d5512bc"></a>

### 58. Change Reactor 3 - 0D5512BC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Reactor 3 (0A0BC80C)](#trigger-0a0bc80c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Reactor 3 (0D5512BC)](#trigger-0d5512bc).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4643, Events line 4725, Actions line 4807.

<a id="trigger-0a0bc63c"></a>

### 59. Captured Reactor 4 - 0A0BC63C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change Reactor 4 (0D556E9C)](#trigger-0d556e9c).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy1 House, cell (90, 138), tag 0DCC8AFC, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Reactor 4 (0D556E9C)](#trigger-0d556e9c).
2. Disable [Captured Reactor 4 (0A0BC63C)](#trigger-0a0bc63c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4644, Events line 4726, Actions line 4808.

<a id="trigger-0d556e9c"></a>

### 60. Change Reactor 4 - 0D556E9C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Reactor 4 (0A0BC63C)](#trigger-0a0bc63c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Reactor 4 (0D556E9C)](#trigger-0d556e9c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4645, Events line 4727, Actions line 4809.

<a id="trigger-0a0bc46c"></a>

### 61. Captured Reactor 5 - 0A0BC46C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change Reactor 5 (0D556C8C)](#trigger-0d556c8c).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy1 House, cell (109, 118), tag 0DCC887C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Reactor 5 (0D556C8C)](#trigger-0d556c8c).
2. Disable [Captured Reactor 5 (0A0BC46C)](#trigger-0a0bc46c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4646, Events line 4728, Actions line 4810.

<a id="trigger-0d556c8c"></a>

### 62. Change Reactor 5 - 0D556C8C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Reactor 5 (0A0BC46C)](#trigger-0a0bc46c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Reactor 5 (0D556C8C)](#trigger-0d556c8c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4647, Events line 4729, Actions line 4811.

<a id="trigger-0a0bc29c"></a>

### 63. Captured Reactor 6 - 0A0BC29C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change Reactor 6 (0D556A7C)](#trigger-0d556a7c).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy1 House, cell (107, 114), tag 0DCC85FC, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change Reactor 6 (0D556A7C)](#trigger-0d556a7c).
2. Disable [Captured Reactor 6 (0A0BC29C)](#trigger-0a0bc29c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4648, Events line 4730, Actions line 4812.

<a id="trigger-0d556a7c"></a>

### 64. Change Reactor 6 - 0D556A7C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Reactor 6 (0A0BC29C)](#trigger-0a0bc29c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Reactor 6 (0D556A7C)](#trigger-0d556a7c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4649, Events line 4731, Actions line 4813.

<a id="trigger-0a0a4e5c"></a>

### 65. All To Hunt - 0A0A4E5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A0A4B2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Barracks Destroyed) is set.
2. local flag 7 (War Fact Destroyed) is set.

Flag writers in this mission: set local flag 6 (Barracks Destroyed) at [Destroyed Barracks (0A09EE9C)](#trigger-0a09ee9c); set local flag 7 (War Fact Destroyed) at [Destroyed War Factory (0A0B9CDC)](#trigger-0a0b9cdc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. All to Hunt: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
3. All to Hunt: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4650, Events line 4732, Actions line 4814.

<a id="trigger-07c401dc"></a>

### 66. 1 Captured (Hack) - 07C401DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Disable [1 Captured (Hack) (07C401DC)](#trigger-07c401dc).
2. Disable [Pyramid 1 Destroyed (07C41C3C)](#trigger-07c41c3c).
3. Enable and reset applicable timers for [1 Seal (07C4A1AC)](#trigger-07c4a1ac).
4. Enable and reset applicable timers for [2 Seals (07C4BF3C)](#trigger-07c4bf3c).
5. Disable [1 Captured (Player) (0CB4203C)](#trigger-0cb4203c).
6. Enable and reset applicable timers for [Change Pyramid 1 (0F50E86C)](#trigger-0f50e86c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4651, Events line 4733, Actions line 4815.

<a id="trigger-07c41c3c"></a>

### 67. Pyramid 1 Destroyed - 07C41C3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [1 Captured (Hack) (07C401DC)](#trigger-07c401dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Pyramid 1 Destroyed (07C41C3C)](#trigger-07c41c3c).
2. Disable [1 Captured (Hack) (07C401DC)](#trigger-07c401dc).
3. Enable and reset applicable timers for [1 Seal (07C4A1AC)](#trigger-07c4a1ac).
4. Enable and reset applicable timers for [2 Seals (07C4BF3C)](#trigger-07c4bf3c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4652, Events line 4734, Actions line 4816.

<a id="trigger-07c4a1ac"></a>

### 68. 1 Seal - 07C4A1AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1 Captured (Hack) (07C401DC)](#trigger-07c401dc); enable from [Pyramid 1 Destroyed (07C41C3C)](#trigger-07c41c3c); enable from [1 Captured (Player) (0CB4203C)](#trigger-0cb4203c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.
2. Supply reinforcement team [1 Seal (0CF0ADEC)](all09t-teams.md#team-0cf0adec) at waypoint 42 (cell 89, 107).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4653, Events line 4735, Actions line 4817.

<a id="trigger-07c4bf3c"></a>

### 69. 2 Seals - 07C4BF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [1 Seal (07C4A1AC)](#trigger-07c4a1ac).

Incoming activation links: enable from [1 Captured (Hack) (07C401DC)](#trigger-07c401dc); enable from [Pyramid 1 Destroyed (07C41C3C)](#trigger-07c41c3c); enable from [1 Captured (Player) (0CB4203C)](#trigger-0cb4203c).

Attached scope: tag definitions 07C4A0CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.
2. Supply reinforcement team [2 Seals (07C496DC)](all09t-teams.md#team-07c496dc) at waypoint 42 (cell 89, 107).
3. Supply reinforcement team [1 Engineer (0CE2903C)](all09t-teams.md#team-0ce2903c) at waypoint 42 (cell 89, 107).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4654, Events line 4736, Actions line 4818.

<a id="trigger-0cb4203c"></a>

### 70. 1 Captured (Player) - 0CB4203C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player sees Pyramid 1 (07C41B4C)](#trigger-07c41b4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [1 Captured (Player) (0CB4203C)](#trigger-0cb4203c).
2. Disable [1 Captured (Hack) (07C401DC)](#trigger-07c401dc).
3. Disable [Pyramid 1 Destroyed (07C41C3C)](#trigger-07c41c3c).
4. Enable and reset applicable timers for [1 Seal (07C4A1AC)](#trigger-07c4a1ac).
5. Enable and reset applicable timers for [2 Seals (07C4BF3C)](#trigger-07c4bf3c).
6. Enable and reset applicable timers for [Change Pyramid 1 (0F50E86C)](#trigger-0f50e86c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4655, Events line 4737, Actions line 4819.

<a id="trigger-0f50e86c"></a>

### 71. Change Pyramid 1 - 0F50E86C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [1 Captured (Player) (0CB4203C)](#trigger-0cb4203c).

Incoming activation links: enable from [1 Captured (Hack) (07C401DC)](#trigger-07c401dc); enable from [1 Captured (Player) (0CB4203C)](#trigger-0cb4203c).

Attached scope: Mayan Pyramid (MAYAN), owner House Balabos, cell (86, 106), tag 07C400FC, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Pyramid 1 (0F50E86C)](#trigger-0f50e86c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4656, Events line 4738, Actions line 4820.

<a id="trigger-07c41b4c"></a>

### 72. Player sees Pyramid 1 - 07C41B4C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Pyramid 1 Destroyed (07C41C3C)](#trigger-07c41c3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Player sees Pyramid 1 (07C41B4C)](#trigger-07c41b4c).
2. Disable [Player sees Pyramid 2 (07C41A5C)](#trigger-07c41a5c).
3. Play voice notification Mis_A9_SealNoTemple.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4657, Events line 4739, Actions line 4821.

<a id="trigger-07c41a5c"></a>

### 73. Player sees Pyramid 2 - 07C41A5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Pyramid 2 Destroyed (07C41D2C)](#trigger-07c41d2c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Player sees Pyramid 2 (07C41A5C)](#trigger-07c41a5c).
2. Disable [Player sees Pyramid 1 (07C41B4C)](#trigger-07c41b4c).
3. Play voice notification Mis_A9_SealNoTemple.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4658, Events line 4740, Actions line 4822.

<a id="trigger-07c41d2c"></a>

### 74. Pyramid 2 Destroyed - 07C41D2C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [2 Captured (Hack) (07C41F3C)](#trigger-07c41f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Pyramid 2 Destroyed (07C41D2C)](#trigger-07c41d2c).
2. Disable [2 Captured (Hack) (07C41F3C)](#trigger-07c41f3c).
3. Enable and reset applicable timers for [1 Seal 2 (07C4BE4C)](#trigger-07c4be4c).
4. Enable and reset applicable timers for [2 Seals 2 (07C4BC7C)](#trigger-07c4bc7c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4659, Events line 4741, Actions line 4823.

<a id="trigger-07c41f3c"></a>

### 75. 2 Captured (Hack) - 07C41F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 22 (country/type HACK; placed owner Hack House).

**Then perform these actions in order:**

1. Disable [2 Captured (Hack) (07C41F3C)](#trigger-07c41f3c).
2. Disable [Pyramid 2 Destroyed (07C41D2C)](#trigger-07c41d2c).
3. Enable and reset applicable timers for [1 Seal 2 (07C4BE4C)](#trigger-07c4be4c).
4. Enable and reset applicable timers for [2 Seals 2 (07C4BC7C)](#trigger-07c4bc7c).
5. Disable [2 Captured (Player) (08E468AC)](#trigger-08e468ac).
6. Enable and reset applicable timers for [Change Pyramid 2 (0F50FE8C)](#trigger-0f50fe8c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4660, Events line 4742, Actions line 4824.

<a id="trigger-07c4be4c"></a>

### 76. 1 Seal 2 - 07C4BE4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Pyramid 2 Destroyed (07C41D2C)](#trigger-07c41d2c); enable from [2 Captured (Hack) (07C41F3C)](#trigger-07c41f3c); enable from [2 Captured (Player) (08E468AC)](#trigger-08e468ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.
2. Supply reinforcement team [1 Seal (0CF0ADEC)](all09t-teams.md#team-0cf0adec) at waypoint 6 (cell 111, 124).
3. Supply reinforcement team [1 Engineer (0CE2903C)](all09t-teams.md#team-0ce2903c) at waypoint 6 (cell 111, 124).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4661, Events line 4743, Actions line 4825.

<a id="trigger-07c4bc7c"></a>

### 77. 2 Seals 2 - 07C4BC7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [1 Seal 2 (07C4BE4C)](#trigger-07c4be4c).

Incoming activation links: enable from [Pyramid 2 Destroyed (07C41D2C)](#trigger-07c41d2c); enable from [2 Captured (Hack) (07C41F3C)](#trigger-07c41f3c); enable from [2 Captured (Player) (08E468AC)](#trigger-08e468ac).

Attached scope: tag definitions 07C4BD6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.
2. Supply reinforcement team [2 Seals (07C496DC)](all09t-teams.md#team-07c496dc) at waypoint 6 (cell 111, 124).
3. Supply reinforcement team [1 Engineer (0CE2903C)](all09t-teams.md#team-0ce2903c) at waypoint 6 (cell 111, 124).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4662, Events line 4744, Actions line 4826.

<a id="trigger-08e468ac"></a>

### 78. 2 Captured (Player) - 08E468AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player sees Pyramid 2 (07C41A5C)](#trigger-07c41a5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [2 Captured (Player) (08E468AC)](#trigger-08e468ac).
2. Disable [2 Captured (Hack) (07C41F3C)](#trigger-07c41f3c).
3. Disable [Pyramid 2 Destroyed (07C41D2C)](#trigger-07c41d2c).
4. Enable and reset applicable timers for [1 Seal 2 (07C4BE4C)](#trigger-07c4be4c).
5. Enable and reset applicable timers for [2 Seals 2 (07C4BC7C)](#trigger-07c4bc7c).
6. Enable and reset applicable timers for [Change Pyramid 2 (0F50FE8C)](#trigger-0f50fe8c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4663, Events line 4745, Actions line 4827.

<a id="trigger-0f50fe8c"></a>

### 79. Change Pyramid 2 - 0F50FE8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [2 Captured (Player) (08E468AC)](#trigger-08e468ac).

Incoming activation links: enable from [2 Captured (Hack) (07C41F3C)](#trigger-07c41f3c); enable from [2 Captured (Player) (08E468AC)](#trigger-08e468ac).

Attached scope: Mayan Pyramid (MAYAN), owner House Balabos, cell (105, 125), tag 07C41E5C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change Pyramid 2 (0F50FE8C)](#trigger-0f50fe8c).

Source locator: MAPS01.MIX/all09t.map; Triggers line 4664, Events line 4746, Actions line 4828.

<a id="trigger-0b67703c"></a>

### 80. Destroy Vehicles - 0B67703C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: War Miner (HARV), owner BadGuy1 House, cell (107, 132), tag 0B67E04C, persistence mode 0; Rhino Heavy Tank (HTNK), owner BadGuy1 House, cell (74, 121), tag 0B67E04C, persistence mode 0; Rhino Heavy Tank (HTNK), owner BadGuy1 House, cell (85, 125), tag 0B67E04C, persistence mode 0; Flak Track (HTK), owner BadGuy1 House, cell (95, 129), tag 0B67E04C, persistence mode 0; Flak Track (HTK), owner BadGuy1 House, cell (85, 110), tag 0B67E04C, persistence mode 0; Flak Track (HTK), owner BadGuy1 House, cell (111, 115), tag 0B67E04C, persistence mode 0; Flak Track (HTK), owner BadGuy1 House, cell (92, 117), tag 0B67E04C, persistence mode 0; Flak Track (HTK), owner BadGuy1 House, cell (76, 108), tag 0B67E04C, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: MAPS01.MIX/all09t.map; Triggers line 4665, Events line 4747, Actions line 4829.

[All team rosters and ordered plans](all09t-teams.md) | [All mission overrides](all09t-overrides.md)
