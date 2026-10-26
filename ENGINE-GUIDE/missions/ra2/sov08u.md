# Operation: Desecration

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for sov08u.map.](../../images/map-sov08u.svg)

*Initial placement schematic for sov08u.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** sov08u.map. **Effective extracted member:** MAPS02.MIX/sov08u.map. **Trigger definitions:** 35.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov08u-teams.md) | [All mission overrides](sov08u-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | URBAN |
| Map size | 0,0,95,88 |
| Visible local rectangle | 18,4,74,70 |
| Placed vehicles | 25 |
| Placed infantry | 56 |
| Placed structures | 115 |
| Placed aircraft | 0 |
| Team templates | 36 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | Vlad1 House | 300 | Vlad1 |
| 2 | Vlad2 House | 200 | Vlad2 |
| 3 | CivilianArmy House | 100 | CivilianArmy |
| 4 | Civilian1 House | 0 | Civilian1 |
| 5 | Other1 House | 20 | Other1 |
| 6 | Other2 House | 20 | Other2 |
| 7 | Other3 House | 20 | Other3 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Bridge1Open,0 |
| 1 | Bridge2Open,1 |
| 2 | Bridge3Open,0 |
| 3 | VladSoldBase,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [PlayerLoss (0C2152A0)](#trigger-0c2152a0) | Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House). | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [WhiteHouseTaken2 (08012920)](#trigger-08012920) | 9 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-0c2152a0"></a>

### 1. PlayerLoss - 0C2152A0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C214BE0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5233, Events line 5270, Actions line 5307.

<a id="trigger-0c214b00"></a>

### 2. WHCaptured - 0C214B00

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [WhiteHouseTaken2 (08012920)](#trigger-08012920).
2. Reveal terrain around waypoint 21 (cell 100, 19).
3. Disable [RepeatObjective (0856B86C)](#trigger-0856b86c).
4. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).
5. Enable and reset applicable timers for [CheerMore (0B538DFC)](#trigger-0b538dfc).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5234, Events line 5271, Actions line 5308.

<a id="trigger-08012920"></a>

### 3. WhiteHouseTaken2 - 08012920

Owner reference: Vlad1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WHCaptured (0C214B00)](#trigger-0c214b00); enable from [WHDestroyed (0965C050)](#trigger-0965c050).

Attached scope: tag definitions 08012A00 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5235, Events line 5272, Actions line 5309.

<a id="trigger-0856b86c"></a>

### 4. RepeatObjective - 0856B86C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [!!DeliverObjective (07DB14FC)](#trigger-07db14fc).

Attached scope: tag definitions 0856CEDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Capture the White House so we can apprehend the traitor Vladimir” (MISSION:Sov08a).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5236, Events line 5273, Actions line 5310.

<a id="trigger-0b538dfc"></a>

### 5. CheerMore - 0B538DFC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WHCaptured (0C214B00)](#trigger-0c214b00); enable from [WHDestroyed (0965C050)](#trigger-0965c050).

Attached scope: tag definitions 0B538A5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5237, Events line 5274, Actions line 5311.

<a id="trigger-09ee5ab0"></a>

### 6. Send Scouts - 09EE5AB0

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09EE55E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Scouts1 (0BF1CB5C)](sov08u-teams.md#team-0bf1cb5c) at waypoint 22 (cell 91, 10).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5238, Events line 5275, Actions line 5312.

<a id="trigger-0a7aef40"></a>

### 7. Vlad1 Production - 0A7AEF40

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7AEC30 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Production Begins: owner selector 14 (country/type VLAD1; placed owner Vlad1 House).
3. AI triggers begin: owner selector 14 (country/type VLAD1; placed owner Vlad1 House).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5239, Events line 5276, Actions line 5313.

<a id="trigger-0e177cd0"></a>

### 8. StartPatrols - 0E177CD0

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E177800 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [ConscriptPatrol (0FBB359C)](sov08u-teams.md#team-0fbb359c).
2. Supply reinforcement team [ShockPatrol (08837EFC)](sov08u-teams.md#team-08837efc) at waypoint 0 (cell 111, 121).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5240, Events line 5277, Actions line 5314.

<a id="trigger-0b83e7a0"></a>

### 9. DesolatorSquad - 0B83E7A0

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B83E300 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [HarrassInfantry (0A11C93C)](sov08u-teams.md#team-0a11c93c).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5241, Events line 5278, Actions line 5315.

<a id="trigger-0e0f0110"></a>

### 10. BeaconDestroyed - 0E0F0110

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E0F1280 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BeaconDestroyed2 (0E0F10D0)](#trigger-0e0f10d0).
2. Enable and reset applicable timers for [BeaconDestroyed3 (098ABDA0)](#trigger-098abda0).
3. Enable and reset applicable timers for [BeaconDestroyed1 (0E02A7D0)](#trigger-0e02a7d0).
4. Create crate type 0 at waypoint 6 (cell 128, 71).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5242, Events line 5279, Actions line 5316.

<a id="trigger-0e0f10d0"></a>

### 11. BeaconDestroyed2 - 0E0F10D0

Owner reference: Vlad2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BeaconDestroyed (0E0F0110)](#trigger-0e0f0110).

Attached scope: GI (E1), owner Vlad2 House, cell (105, 75), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (107, 77), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (103, 74), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (106, 69), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (108, 69), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (109, 68), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (104, 71), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (127, 75), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (133, 71), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (132, 74), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (123, 57), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (122, 56), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (137, 58), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (124, 91), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (123, 90), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (133, 88), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (142, 87), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (132, 69), tag 0E0F2D10, persistence mode 0; GI (E1), owner Vlad2 House, cell (124, 68), tag 0E0F2D10, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 16 (country/type CIVILIANARMY; placed owner CivilianArmy House).
2. Make enemy: owner selector 16 (country/type CIVILIANARMY; placed owner CivilianArmy House).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5243, Events line 5280, Actions line 5317.

<a id="trigger-098abda0"></a>

### 12. BeaconDestroyed3 - 098ABDA0

Owner reference: Vlad1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BeaconDestroyed (0E0F0110)](#trigger-0e0f0110).

Attached scope: tag definitions 098ABA50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 16 (country/type CIVILIANARMY; placed owner CivilianArmy House).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5244, Events line 5281, Actions line 5318.

<a id="trigger-0e02a7d0"></a>

### 13. BeaconDestroyed1 - 0E02A7D0

Owner reference: Civilian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BeaconDestroyed (0E0F0110)](#trigger-0e0f0110).

Attached scope: Civilian (CIV3), owner Civilian1 House, cell (89, 83), tag 0E02A300, persistence mode 0; Civilian (CIV2), owner Civilian1 House, cell (72, 71), tag 0E02A300, persistence mode 0; Civilian (CIV1), owner Civilian1 House, cell (139, 103), tag 0E02A300, persistence mode 0; Civilian (CIV2), owner Civilian1 House, cell (138, 101), tag 0E02A300, persistence mode 0; Technician (CTECH), owner Civilian1 House, cell (136, 97), tag 0E02A300, persistence mode 0; Technician (CTECH), owner Civilian1 House, cell (135, 98), tag 0E02A300, persistence mode 0; Technician (CTECH), owner Civilian1 House, cell (75, 76), tag 0E02A300, persistence mode 0; Technician (CTECH), owner Civilian1 House, cell (87, 83), tag 0E02A300, persistence mode 0; Civilian (CIV1), owner Civilian1 House, cell (72, 70), tag 0E02A300, persistence mode 0; Civilian (CIV2), owner Civilian1 House, cell (87, 84), tag 0E02A300, persistence mode 0.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 16 (country/type CIVILIANARMY; placed owner CivilianArmy House).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5245, Events line 5282, Actions line 5319.

<a id="trigger-0965c050"></a>

### 14. WHDestroyed - 0965C050

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [WHCaptured (0C214B00)](#trigger-0c214b00).

Attached scope: White House (CAWASH01), owner Civilian1 House, cell (98, 14), tag 0C214930, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [WhiteHouseTaken2 (08012920)](#trigger-08012920).
2. Reveal terrain around waypoint 21 (cell 100, 19).
3. Disable [RepeatObjective (0856B86C)](#trigger-0856b86c).
4. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).
5. Enable and reset applicable timers for [CheerMore (0B538DFC)](#trigger-0b538dfc).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5246, Events line 5283, Actions line 5320.

<a id="trigger-07fb8f40"></a>

### 15. HuntAtBaseDie - 07FB8F40

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FB86E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  #: 18.

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type VLAD1; placed owner Vlad1 House).
2. Fire Sale: owner selector 14 (country/type VLAD1; placed owner Vlad1 House).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5247, Events line 5284, Actions line 5321.

<a id="trigger-08b35b40"></a>

### 16. VladTaunt - 08B35B40

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 2 tagged map cells: (96, 47), (96, 48); tag 08B357F0, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Horizontal Line: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Play in-game movie 110.

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5248, Events line 5285, Actions line 5322.

<a id="trigger-08b36f40"></a>

### 17. Monument Speech - 08B36F40

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B355A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 15 (global list position: Soviet Ore Refinery (NAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Mis_S8_SofiaMonHint.

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5249, Events line 5286, Actions line 5323.

<a id="trigger-09233c6c"></a>

### 18. !SendTanks - 09233C6C

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1400 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team 0 (template not recovered locally).
2. Create/recruit team [!WHAttack11 (0A11ADEC)](sov08u-teams.md#team-0a11adec).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5250, Events line 5287, Actions line 5324.

<a id="trigger-drones"></a>

### 19. SendTanks-Deso - DRONES

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0923367C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 800 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [!WHAttack12 (0A11AA4C)](sov08u-teams.md#team-0a11aa4c).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5251, Events line 5288, Actions line 5325.

<a id="trigger-07db14fc"></a>

### 20. !!DeliverObjective - 07DB14FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07DB11BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “Objective 1: Capture the White House so we can apprehend the traitor Vladimir” (MISSION:Sov08a).
2. Enable and reset applicable timers for [RepeatObjective (0856B86C)](#trigger-0856b86c).
3. Reveal terrain around waypoint 21 (cell 100, 19).
4. Create radar-event marker type 5 at waypoint 21 (cell 100, 19).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5252, Events line 5289, Actions line 5326.

<a id="trigger-07f40f3c"></a>

### 21. GarrisonTroops - 07F40F3C

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F409FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Garrison3 (0B60354C)](sov08u-teams.md#team-0b60354c) at waypoint 7 (cell 133, 103).
2. Supply reinforcement team [Garrison2 (0FBCEDEC)](sov08u-teams.md#team-0fbcedec) at waypoint 13 (cell 91, 24).
3. Supply reinforcement team [Garrison1 (0FBCD32C)](sov08u-teams.md#team-0fbcd32c) at waypoint 29 (cell 91, 30).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5253, Events line 5290, Actions line 5327.

<a id="trigger-09bab550"></a>

### 22. Reveal Monuments - 09BAB550

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09BACEB0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 5 (cell 109, 75).
2. Reveal terrain around waypoint 9 (cell 138, 89).
3. Reveal terrain around waypoint 18 (cell 138, 57).
4. Reveal terrain around waypoint 10 (cell 42, 77).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5254, Events line 5291, Actions line 5328.

<a id="trigger-09bac370"></a>

### 23. Beacon Speech - 09BAC370

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Beacon (NAPSYB), owner Vlad2 House, cell (128, 70), tag 09BAC0D0, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play voice notification Mis_S8_SofiaBeaconDest.

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5255, Events line 5292, Actions line 5329.

<a id="trigger-0ad7e200"></a>

### 24. Drop Paratroopers - 0AD7E200

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AD7FD90 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Paratroopers (09FDBB5C)](sov08u-teams.md#team-09fdbb5c) at waypoint 14 (cell 45, 94).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5256, Events line 5293, Actions line 5330.

<a id="trigger-0b312f3c"></a>

### 25. Vlad2 Production - 0B312F3C

Owner reference: Vlad2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B3126EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 250 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Production Begins: owner selector 15 (country/type VLAD2; placed owner Vlad2 House).
3. AI triggers begin: owner selector 15 (country/type VLAD2; placed owner Vlad2 House).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5257, Events line 5294, Actions line 5331.

<a id="trigger-08678dbc"></a>

### 26. SmithCastleDestroy - 08678DBC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Smithsonian Castle (CAWASH16), owner Civilian1 House, cell (136, 86), tag 0858449C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 9 (cell 138, 89).
2. Create crate type 10 at waypoint 25 (cell 136, 90).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5258, Events line 5295, Actions line 5332.

<a id="trigger-0858555c"></a>

### 27. SmithDestroyed - 0858555C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Smithsonian Natural History Museum (CAWASH17), owner Civilian1 House, cell (136, 53), tag 0858141C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 14 at waypoint 18 (cell 138, 57).
2. Create crate type 0 at waypoint 30 (cell 134, 51).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5259, Events line 5296, Actions line 5333.

<a id="trigger-07e0f3cc"></a>

### 28. WashDestroyed - 07E0F3CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Washington Monument (CAWSH12), owner Civilian1 House, cell (107, 72), tag 07E09C4C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 3 (cell 111, 73).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5260, Events line 5297, Actions line 5334.

<a id="trigger-0b657f3c"></a>

### 29. Water - 0B657F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B65034C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WavesLake at waypoint 20 (cell 54, 73).
2. Play sound _Amb_WavesLake at waypoint 23 (cell 66, 73).
3. Play sound _Amb_WavesLake at waypoint 24 (cell 63, 57).
4. Play sound _Amb_WavesLake at waypoint 51 (cell 125, 118).
5. Play sound _Amb_UrbanMurmur1 at waypoint 44 (cell 153, 98).
6. Play sound _Amb_UrbanMurmur2 at waypoint 52 (cell 26, 89).
7. Play sound _Amb_OceanLight at waypoint 45 (cell 139, 115).
8. Play sound _Amb_OceanLight at waypoint 46 (cell 106, 115).
9. Play sound _Amb_OceanLight at waypoint 47 (cell 85, 99).
10. Play sound _Amb_OceanLight at waypoint 48 (cell 86, 113).
11. Play sound _Amb_OceanLight at waypoint 49 (cell 78, 122).
12. Play sound _Amb_BirdsBeach at waypoint 50 (cell 92, 143).
13. Enable player input.

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5261, Events line 5298, Actions line 5335.

<a id="trigger-0b63a3bc"></a>

### 30. Birds - 0B63A3BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B63248C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsPark at waypoint 33 (cell 60, 83).
2. Play sound _Amb_BirdsTemperate1 at waypoint 34 (cell 65, 64).
3. Play sound _Amb_BirdsPark at waypoint 35 (cell 34, 86).
4. Play sound _Amb_BirdsTemperate1 at waypoint 36 (cell 69, 103).
5. Play sound _Amb_BirdsPark at waypoint 37 (cell 53, 109).
6. Play sound _Amb_BirdsTemperate1 at waypoint 38 (cell 72, 38).
7. Play sound _Amb_BirdsPark at waypoint 39 (cell 134, 62).
8. Play sound _Amb_BirdsTemperate1 at waypoint 40 (cell 160, 81).
9. Play sound _Amb_BirdsPark at waypoint 41 (cell 110, 88).
10. Play sound _Amb_BirdsTemperate1 at waypoint 42 (cell 88, 86).
11. Play sound _Amb_BirdsPark at waypoint 43 (cell 97, 107).
12. Play sound _Amb_BirdsBeach at waypoint 53 (cell 82, 116).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5262, Events line 5299, Actions line 5336.

<a id="trigger-0a229d4c"></a>

### 31. Drop Paratroopers - 0A229D4C

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A2298CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Paratroopers (09FDBB5C)](sov08u-teams.md#team-09fdbb5c) at waypoint 17 (cell 60, 112).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5263, Events line 5300, Actions line 5337.

<a id="trigger-0a22c0ec"></a>

### 32. Drop Paratroopers - 0A22C0EC

Owner reference: Vlad1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A22DE9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 210 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Paratroopers (09FDBB5C)](sov08u-teams.md#team-09fdbb5c) at waypoint 16 (cell 64, 90).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5264, Events line 5301, Actions line 5338.

<a id="trigger-087d3c5c"></a>

### 33. EliteApocGuard - H only - 087D3C5C

Owner reference: Vlad2. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 087D3B7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [EliteApocGuard (087D21EC)](sov08u-teams.md#team-087d21ec) at waypoint 15 (cell 100, 29).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5265, Events line 5302, Actions line 5339.

<a id="trigger-0b086e1c"></a>

### 34. MonLincolnDestroyed - 0B086E1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Lincoln Memorial (CAWASH15), owner Civilian1 House, cell (40, 72), tag 0B086D3C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 14 at waypoint 10 (cell 42, 77).
2. Create crate type 0 at waypoint 8 (cell 45, 73).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5266, Events line 5303, Actions line 5340.

<a id="trigger-0b084d8c"></a>

### 35. MonJeffersonDestroyed - 0B084D8C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Jefferson Memorial (CAWASH14), owner Civilian1 House, cell (98, 128), tag 0B084CAC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 54 (cell 95, 128).

Source locator: MAPS02.MIX/sov08u.map; Triggers line 5267, Events line 5304, Actions line 5341.

[All team rosters and ordered plans](sov08u-teams.md) | [All mission overrides](sov08u-overrides.md)
