# Operation: Big Apple

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov03u.map. **Effective extracted member:** MAPS02.MIX/sov03u.map. **Trigger definitions:** 70.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov03u-teams.md) | [All mission overrides](sov03u-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | URBAN |
| Map size | 0,0,98,68 |
| Visible local rectangle | 2,8,94,54 |
| Placed vehicles | 46 |
| Placed infantry | 6 |
| Placed structures | 134 |
| Placed aircraft | 0 |
| Team templates | 32 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 1000 | BadGuy1 |
| 2 | BadGuy2 House | 100 | BadGuy2 |
| 3 | BadGuy3 House | 0 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 100 | Other1 |
| 6 | Other2 House | 20 | Other2 |
| 7 | Other3 House | 100 | Other3 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Stop_Looping,0 |
| 1 | Play Yuri Movie,0 |
| 2 | Play Yuri Audio,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Player Loses (03D95C60)](#trigger-03d95c60) | 3 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [Player Wins (03D95F40)](#trigger-03d95f40) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-0b487180"></a>

### 1. BG1 Startup - 0B487180

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B488070 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Reveal terrain around waypoint 0 (cell 102, 28).
4. Reveal terrain around waypoint 98 (cell 71, 134).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4150, Events line 4222, Actions line 4294.

<a id="trigger-09ac9c20"></a>

### 2. Entered Battle Lab - 09AC9C20

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Lab Destroyed (0A1E37BC)](#trigger-0a1e37bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Objective 1 (08E025BC)](#trigger-08e025bc).
2. Disable [Lab Destroyed (0A1E37BC)](#trigger-0a1e37bc).
3. Enable and reset applicable timers for [Beacon Placed (0ADB3CB4)](#trigger-0adb3cb4).
4. Enable and reset applicable timers for [Sell Lab (08AAA2DC)](#trigger-08aaa2dc).
5. Disable [Entered Battle Lab (09AC9C20)](#trigger-09ac9c20).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4151, Events line 4223, Actions line 4295.

<a id="trigger-0a1e37bc"></a>

### 3. Lab Destroyed - 0A1E37BC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Player Loses (03D95C60)](#trigger-03d95c60).
2. Disable [Lab Destroyed (0A1E37BC)](#trigger-0a1e37bc).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4152, Events line 4224, Actions line 4296.

<a id="trigger-08e025bc"></a>

### 4. Objective 1 - 08E025BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Entered Battle Lab (09AC9C20)](#trigger-09ac9c20).

Attached scope: tag definitions 08E03F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1 Complete” (MISSION:Objective1).
2. Disable [Objective 1 Reminder (08349ACC)](#trigger-08349acc).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4153, Events line 4225, Actions line 4297.

<a id="trigger-0adb3cb4"></a>

### 5. Beacon Placed - 0ADB3CB4

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Entered Battle Lab (09AC9C20)](#trigger-09ac9c20).

Attached scope: tag definitions 0ADB3684 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 20 (country/type OTHER3; placed owner Other3 House).
2. Enable and reset applicable timers for [Change Beacon House (09462D4C)](#trigger-09462d4c).
3. Enable and reset applicable timers for [6 Psi-Corp Create (08345BFC)](#trigger-08345bfc).
4. Enable and reset applicable timers for [Play Audio (09A2903C)](#trigger-09a2903c).
5. Enable and reset applicable timers for [Play Movie (09A2603C)](#trigger-09a2603c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4154, Events line 4226, Actions line 4298.

<a id="trigger-08aaa2dc"></a>

### 6. Sell Lab - 08AAA2DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Entered Battle Lab (09AC9C20)](#trigger-09ac9c20).

Incoming activation links: enable from [Entered Battle Lab (09AC9C20)](#trigger-09ac9c20).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Sell the attached building through the scripted sale action.
2. Disable [Sell Lab (08AAA2DC)](#trigger-08aaa2dc).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4155, Events line 4227, Actions line 4299.

<a id="trigger-03d95c60"></a>

### 7. Player Loses - 03D95C60

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Lab Destroyed (0A1E37BC)](#trigger-0a1e37bc); enable from [Beacon Destroyed (07C6E684)](#trigger-07c6e684); enable from [Player Lose Conditions (03DA6100)](#trigger-03da6100).

Attached scope: tag definitions 03DA6240 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4156, Events line 4228, Actions line 4300.

<a id="trigger-08349acc"></a>

### 8. Objective 1 Reminder - 08349ACC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Sofia 1 (0BD70F40)](#trigger-0bd70f40).

Attached scope: tag definitions 0834958C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Capture the Allied BATTLE LAB with an ENGINEER” (MISSION:Sov03a).
2. Create radar-event marker type 5 at waypoint 22 (cell 101, 27).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4157, Events line 4229, Actions line 4301.

<a id="trigger-09462d4c"></a>

### 9. Change Beacon House - 09462D4C

Owner reference: Other3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Beacon Placed (0ADB3CB4)](#trigger-0adb3cb4).

Attached scope: tag definitions 0946293C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Enable and reset applicable timers for [Beacon Destroyed (07C6E684)](#trigger-07c6e684).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4158, Events line 4230, Actions line 4302.

<a id="trigger-08345bfc"></a>

### 10. 6 Psi-Corp Create - 08345BFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Beacon Placed (0ADB3CB4)](#trigger-0adb3cb4).

Attached scope: tag definitions 083459FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [6 Psi-Corp Team (0AE6F1EC)](sov03u-teams.md#team-0ae6f1ec).
2. Supply reinforcement team [2 Grizzly RE Team (0AF10B5C)](sov03u-teams.md#team-0af10b5c).
3. Supply reinforcement team [2 Grizzly RE Team (0AF10B5C)](sov03u-teams.md#team-0af10b5c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4159, Events line 4231, Actions line 4303.

<a id="trigger-09a2903c"></a>

### 11. Play Audio - 09A2903C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Play Movie (09A2603C)](#trigger-09a2603c).

Incoming activation links: enable from [Beacon Placed (0ADB3CB4)](#trigger-0adb3cb4); enable from [WF_Captured (083243CC)](#trigger-083243cc); enable from [WF_Destroyed (083241FC)](#trigger-083241fc); enable from [Build War_Yuri Appears (0858B41C)](#trigger-0858b41c).

Attached scope: tag definitions 09A2016C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Play Yuri Movie) is set.

Flag writers in this mission: set local flag 1 (Play Yuri Movie) at [Yuri Movie (09A2B03C)](#trigger-09a2b03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Play Audio (09A2903C)](#trigger-09a2903c).
2. Disable [Play Movie (09A2603C)](#trigger-09a2603c).
3. Enable and reset applicable timers for [Yuri Audio (09A2403C)](#trigger-09a2403c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4160, Events line 4232, Actions line 4304.

<a id="trigger-09a2603c"></a>

### 12. Play Movie - 09A2603C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Beacon Placed (0ADB3CB4)](#trigger-0adb3cb4); enable from [WF_Captured (083243CC)](#trigger-083243cc); enable from [WF_Destroyed (083241FC)](#trigger-083241fc); enable from [Build War_Yuri Appears (0858B41C)](#trigger-0858b41c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 1 (Play Yuri Movie) is clear.

Flag writers in this mission: set local flag 1 (Play Yuri Movie) at [Yuri Movie (09A2B03C)](#trigger-09a2b03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Play Movie (09A2603C)](#trigger-09a2603c).
2. Disable [Play Audio (09A2903C)](#trigger-09a2903c).
3. Enable and reset applicable timers for [Yuri Movie (09A2B03C)](#trigger-09a2b03c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4161, Events line 4233, Actions line 4305.

<a id="trigger-07c6e684"></a>

### 13. Beacon Destroyed - 07C6E684

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change Beacon House (09462D4C)](#trigger-09462d4c).

Attached scope: tag definitions 07C68244 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 183 (global list position: Psychic Beacon (NAPSYB)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Stop the visible mission timer.
2. Enable and reset applicable timers for [Player Loses (03D95C60)](#trigger-03d95c60).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4162, Events line 4234, Actions line 4306.

<a id="trigger-09a2403c"></a>

### 14. Yuri Audio - 09A2403C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Play Audio (09A2903C)](#trigger-09a2903c).

Attached scope: tag definitions 09A3503C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S10_Yuri.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4163, Events line 4235, Actions line 4307.

<a id="trigger-09a2b03c"></a>

### 15. Yuri Movie - 09A2B03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Play Movie (09A2603C)](#trigger-09a2603c).

Attached scope: tag definitions 09A280AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 75.
2. Set local flag 1 (Play Yuri Movie).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4164, Events line 4236, Actions line 4308.

<a id="trigger-08e03dac"></a>

### 16. Objective 2 - 08E03DAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08E03AEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Technology gained - Build a PSYCHIC BEACON” (MISSION:Sov03b).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4165, Events line 4237, Actions line 4309.

<a id="trigger-09e00840"></a>

### 17. Beacon Attack Teams - 09E00840

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Beacon Built (0DC7AB70)](#trigger-0dc7ab70).

Attached scope: tag definitions 09E0F480 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Re_GI (096948D4)](sov03u-teams.md#team-096948d4) at waypoint 11 (cell 82, 46).
2. Supply reinforcement team [Re_IFV (099FE8EC)](sov03u-teams.md#team-099fe8ec) at waypoint 11 (cell 82, 46).
3. Supply reinforcement team [Re_Tank (08D1E180)](sov03u-teams.md#team-08d1e180) at waypoint 7 (cell 108, 51).
4. Supply reinforcement team [Re_Rocket (08D1C6E0)](sov03u-teams.md#team-08d1c6e0) at waypoint 11 (cell 82, 46).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4166, Events line 4238, Actions line 4310.

<a id="trigger-04386a7c"></a>

### 18. Disable Beacon Attack - 04386A7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0438699C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 420 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Beacon Attack Teams (09E00840)](#trigger-09e00840).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4167, Events line 4239, Actions line 4311.

<a id="trigger-09642890"></a>

### 19. Create Outpost B Team - 09642890

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09642440 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Outpost B (08D1DCA0)](sov03u-teams.md#team-08d1dca0) at waypoint 1 (cell 138, 72).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4168, Events line 4240, Actions line 4312.

<a id="trigger-0965f670"></a>

### 20. Create IFV Patrol - 0965F670

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0965F190 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [4IFV Patrol (099FDB5C)](sov03u-teams.md#team-099fdb5c) at waypoint 2 (cell 130, 78).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4169, Events line 4241, Actions line 4313.

<a id="trigger-03d97540"></a>

### 21. Beacon Deployed - 03D97540

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03D97300 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The visible mission countdown has expired.

**Then perform these actions in order:**

1. Disable [Beacon Attack Teams (09E00840)](#trigger-09e00840).
2. Enable and reset applicable timers for [Sofia 3 (099DFE70)](#trigger-099dfe70).
3. Display message “Objective 2 Complete” (MISSION:Objective2).
4. Play sound ChronoLegionAttack.
5. Enable and reset applicable timers for [Give Buildings (07500224)](#trigger-07500224).
6. Enable and reset applicable timers for [Allied Conversion (09152DB0)](#trigger-09152db0).
7. AI triggers stop: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
8. Lightning Storm strike at waypoint 3 (cell 77, 78).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4170, Events line 4242, Actions line 4314.

<a id="trigger-099dfe70"></a>

### 22. Sofia 3 - 099DFE70

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Beacon Deployed (03D97540)](#trigger-03d97540).

Attached scope: tag definitions 099DFCA0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S3_Sofia3.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4171, Events line 4243, Actions line 4315.

<a id="trigger-07500224"></a>

### 23. Give Buildings - 07500224

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Beacon Deployed (03D97540)](#trigger-03d97540).

Attached scope: Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (141, 69), tag 07506BC4, persistence mode 0; Allied Construction Yard (GACNST), owner BadGuy1 House, cell (107, 18), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (122, 39), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (95, 39), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (98, 39), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (116, 39), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (101, 39), tag 07506BC4, persistence mode 0; Allied Ore Refinery (GAREFN), owner BadGuy1 House, cell (94, 33), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (113, 39), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (104, 39), tag 07506BC4, persistence mode 0; Allied Barracks (GAPILE), owner BadGuy1 House, cell (82, 91), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (110, 39), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (107, 39), tag 07506BC4, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (119, 39), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (91, 38), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (115, 48), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (127, 38), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (100, 48), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (127, 41), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (103, 48), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (118, 48), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (91, 41), tag 07506BC4, persistence mode 0; Air Force Command Headquarters (GAAIRC), owner BadGuy1 House, cell (95, 44), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (125, 66), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (111, 66), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (94, 80), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (71, 76), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (85, 54), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (99, 100), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (99, 56), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (107, 105), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (110, 84), tag 07506BC4, persistence mode 0; Gate (GAGATE_A), owner BadGuy1 House, cell (100, 47), tag 07506BC4, persistence mode 0; Gate (GAGATE_A), owner BadGuy1 House, cell (115, 47), tag 07506BC4, persistence mode 0; Allied Barracks (GAPILE), owner BadGuy1 House, cell (113, 27), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (117, 34), tag 07506BC4, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (113, 24), tag 07506BC4, persistence mode 0; Allied War Factory (GAWEAP), owner BadGuy1 House, cell (106, 43), tag 07506BC4, persistence mode 0; Allied Repair Depot (GADEPT), owner BadGuy1 House, cell (107, 23), tag 07506BC4, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [WF_Captured (083243CC)](#trigger-083243cc).
3. Disable [WF_Destroyed (083241FC)](#trigger-083241fc).
4. Enable and reset applicable timers for [WF_Give Buildings (0832410C)](#trigger-0832410c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4172, Events line 4244, Actions line 4316.

<a id="trigger-09152db0"></a>

### 24. Allied Conversion - 09152DB0

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Beacon Deployed (03D97540)](#trigger-03d97540).

Attached scope: tag definitions 09152A60 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 0 (Stop_Looping) is clear.

Flag writers in this mission: set local flag 0 (Stop_Looping) at [Allied Conversion (09152DB0)](#trigger-09152db0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 0 (Stop_Looping).
2. Enable and reset applicable timers for [Allied Conversion Talk (0AC77DD0)](#trigger-0ac77dd0).
3. Display message “Allied troops are now under Soviet control” (MISSION:Sov03e).
4. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).
5. Reveal the whole map.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4173, Events line 4245, Actions line 4317.

<a id="trigger-083243cc"></a>

### 25. WF_Captured - 083243CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [WF_Destroyed (083241FC)](#trigger-083241fc).
2. Enable and reset applicable timers for [4 Psi-Corp Create (0834438C)](#trigger-0834438c).
3. Disable [WF_Captured (083243CC)](#trigger-083243cc).
4. Enable and reset applicable timers for [Play Audio (09A2903C)](#trigger-09a2903c).
5. Enable and reset applicable timers for [Play Movie (09A2603C)](#trigger-09a2603c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4174, Events line 4246, Actions line 4318.

<a id="trigger-083241fc"></a>

### 26. WF_Destroyed - 083241FC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [WF_Captured (083243CC)](#trigger-083243cc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [WF_Captured (083243CC)](#trigger-083243cc).
2. Enable and reset applicable timers for [4 Psi-Corp Create (0834438C)](#trigger-0834438c).
3. Disable [WF_Destroyed (083241FC)](#trigger-083241fc).
4. Enable and reset applicable timers for [Play Audio (09A2903C)](#trigger-09a2903c).
5. Enable and reset applicable timers for [Play Movie (09A2603C)](#trigger-09a2603c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4175, Events line 4247, Actions line 4319.

<a id="trigger-0832410c"></a>

### 27. WF_Give Buildings - 0832410C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [WF_Destroyed (083241FC)](#trigger-083241fc).

Incoming activation links: enable from [Give Buildings (07500224)](#trigger-07500224).

Attached scope: Allied War Factory (GAWEAP), owner BadGuy1 House, cell (111, 86), tag 083242EC, persistence mode 2.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [WF_Give Buildings (0832410C)](#trigger-0832410c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4176, Events line 4248, Actions line 4320.

<a id="trigger-0ac77dd0"></a>

### 28. Allied Conversion Talk - 0AC77DD0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Allied Conversion (09152DB0)](#trigger-09152db0).

Attached scope: tag definitions 0AC77B10 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_A8_AllSoldierTurned.
2. Enable and reset applicable timers for [Allies Yuried (0A4CF7A0)](#trigger-0a4cf7a0).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4177, Events line 4249, Actions line 4321.

<a id="trigger-0834438c"></a>

### 29. 4 Psi-Corp Create - 0834438C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WF_Captured (083243CC)](#trigger-083243cc); enable from [WF_Destroyed (083241FC)](#trigger-083241fc); enable from [Build War_Yuri Appears (0858B41C)](#trigger-0858b41c).

Attached scope: tag definitions 08345E1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [4 Psi-Corp Team (0ADE8A3C)](sov03u-teams.md#team-0ade8a3c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4178, Events line 4250, Actions line 4322.

<a id="trigger-0a4cf7a0"></a>

### 30. Allies Yuried - 0A4CF7A0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Allied Conversion Talk (0AC77DD0)](#trigger-0ac77dd0).

Attached scope: tag definitions 0A4CF630 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Sofia 4 (099DFBC0)](#trigger-099dfbc0).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4179, Events line 4251, Actions line 4323.

<a id="trigger-099dfbc0"></a>

### 31. Sofia 4 - 099DFBC0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Allies Yuried (0A4CF7A0)](#trigger-0a4cf7a0).

Attached scope: tag definitions 099DF9F0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Annouce Win (0D0211D0)](#trigger-0d0211d0).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4180, Events line 4252, Actions line 4324.

<a id="trigger-0d0211d0"></a>

### 32. Annouce Win - 0D0211D0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Sofia 4 (099DFBC0)](#trigger-099dfbc0).

Attached scope: tag definitions 0D022C80 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Player Wins (03D95F40)](#trigger-03d95f40).
2. Enable and reset applicable timers for [Cheer (0CD9599C)](#trigger-0cd9599c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4181, Events line 4253, Actions line 4325.

<a id="trigger-03d95f40"></a>

### 33. Player Wins - 03D95F40

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Annouce Win (0D0211D0)](#trigger-0d0211d0).

Attached scope: tag definitions 03D95D40 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4182, Events line 4254, Actions line 4326.

<a id="trigger-0cd9599c"></a>

### 34. Cheer - 0CD9599C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Annouce Win (0D0211D0)](#trigger-0d0211d0).

Attached scope: tag definitions 0CD9534C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4183, Events line 4255, Actions line 4327.

<a id="trigger-08e29c44"></a>

### 35. Final Announce Air - 08E29C44

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Final Rush (0BA1C78C)](#trigger-0ba1c78c).

Attached scope: tag definitions 08E29594 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_EnemyAirArmadaDetected.
2. Enable and reset applicable timers for [Final Announce Armor (08E29164)](#trigger-08e29164).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4184, Events line 4256, Actions line 4328.

<a id="trigger-08e29164"></a>

### 36. Final Announce Armor - 08E29164

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Final Announce Air (08E29C44)](#trigger-08e29c44).

Attached scope: tag definitions 08E2EA54 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ArmorBattallianDetected.
2. Enable and reset applicable timers for [Final Attack Teams (099DF7D0)](#trigger-099df7d0).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4185, Events line 4257, Actions line 4329.

<a id="trigger-099df7d0"></a>

### 37. Final Attack Teams - 099DF7D0

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Final Announce Armor (08E29164)](#trigger-08e29164).

Attached scope: tag definitions 099DF350 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Final_Tank (0C19E93C)](sov03u-teams.md#team-0c19e93c) at waypoint 14 (cell 150, 58).
2. Supply reinforcement team [Final_IFV (0C19EB7C)](sov03u-teams.md#team-0c19eb7c) at waypoint 2 (cell 130, 78).
3. Supply reinforcement team [Final_Rocket (0C19E80C)](sov03u-teams.md#team-0c19e80c).
4. Supply reinforcement team [Final_Tank2 (0C19F1BC)](sov03u-teams.md#team-0c19f1bc) at waypoint 15 (cell 117, 74).
5. Supply reinforcement team [Final IFV 2 (0C19E36C)](sov03u-teams.md#team-0c19e36c) at waypoint 6 (cell 109, 112).
6. Supply reinforcement team [Death Rocketeers (0C1D87BC)](sov03u-teams.md#team-0c1d87bc) at waypoint 5 (cell 130, 92).
7. Supply reinforcement team [Death GIs (0C1D88EC)](sov03u-teams.md#team-0c1d88ec) at waypoint 15 (cell 117, 74).
8. Supply reinforcement team [Death GIs (0C1D88EC)](sov03u-teams.md#team-0c1d88ec) at waypoint 1 (cell 138, 72).
9. Supply reinforcement team [Death Tanks (0C1DF0CC)](sov03u-teams.md#team-0c1df0cc) at waypoint 18 (cell 73, 51).
10. Supply reinforcement team [Death Tanks (0C1DF0CC)](sov03u-teams.md#team-0c1df0cc) at waypoint 17 (cell 139, 46).
11. Supply reinforcement team [Death IFVs (0C1D8EFC)](sov03u-teams.md#team-0c1d8efc) at waypoint 3 (cell 77, 78).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4186, Events line 4258, Actions line 4330.

<a id="trigger-03da6100"></a>

### 38. Player Lose Conditions - 03DA6100

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03DA7210 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Player Loses (03D95C60)](#trigger-03d95c60).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4187, Events line 4259, Actions line 4331.

<a id="trigger-097851d0"></a>

### 39. Create IFVa Patrol - 097851D0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B45C060 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [4aIFV Patrol (099FD6AC)](sov03u-teams.md#team-099fd6ac) at waypoint 4 (cell 130, 38).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4188, Events line 4260, Actions line 4332.

<a id="trigger-0be3f060"></a>

### 40. Create IFVb Patrol - 0BE3F060

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BE3FE70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [4bIFV Patrol (099FD30C)](sov03u-teams.md#team-099fd30c) at waypoint 6 (cell 109, 112).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4189, Events line 4261, Actions line 4333.

<a id="trigger-0be3eec0"></a>

### 41. Create IFVc Patrol - 0BE3EEC0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BE3EDF0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [4cIFV Patrol (0D33D8EC)](sov03u-teams.md#team-0d33d8ec) at waypoint 9 (cell 81, 36).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4190, Events line 4262, Actions line 4334.

<a id="trigger-0dc7ab70"></a>

### 42. Beacon Built - 0DC7AB70

Owner reference: Other3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0DC7A690 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 183 (global list position: Psychic Beacon (NAPSYB)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Beacon Attack Teams (09E00840)](#trigger-09e00840).
2. Set the mission timer to 300 configured time units.
3. Start the visible mission timer.
4. Use countdown label “Beacon Deployment in:” (MISSION:Sov03d).
5. Display message “Objective 2: Defend the PSYCHIC BEACON from Allied attack” (MISSION:Sov03c).
6. Enable and reset applicable timers for [Sofia 2 (099DE8C0)](#trigger-099de8c0).
7. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
8. Enable and reset applicable timers for [Final Rush (0BA1C78C)](#trigger-0ba1c78c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4191, Events line 4263, Actions line 4335.

<a id="trigger-099de8c0"></a>

### 43. Sofia 2 - 099DE8C0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Beacon Built (0DC7AB70)](#trigger-0dc7ab70).

Attached scope: tag definitions 099DFF50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S3_Sofia2.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4192, Events line 4264, Actions line 4336.

<a id="trigger-0ba1c78c"></a>

### 44. Final Rush - 0BA1C78C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Beacon Built (0DC7AB70)](#trigger-0dc7ab70).

Attached scope: tag definitions 0BA1C03C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 175 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Final Announce Air (08E29C44)](#trigger-08e29c44).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4193, Events line 4265, Actions line 4337.

<a id="trigger-0bd70f40"></a>

### 45. Sofia 1 - 0BD70F40

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Radar Movie (0A3A685C)](#trigger-0a3a685c).

Attached scope: tag definitions 0BD709A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 40 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PIng Battle Lab (0ADEA2E0)](#trigger-0adea2e0).
2. Play voice notification Mis_S3_Sofia1.
3. Display message “Objective 1: Capture the Allied BATTLE LAB with an ENGINEER” (MISSION:Sov03a).
4. Enable and reset applicable timers for [Objective 1 Reminder (08349ACC)](#trigger-08349acc).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4194, Events line 4266, Actions line 4338.

<a id="trigger-0adea2e0"></a>

### 46. PIng Battle Lab - 0ADEA2E0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Sofia 1 (0BD70F40)](#trigger-0bd70f40).

Attached scope: tag definitions 0ADEC700 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 22 (cell 101, 27).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4195, Events line 4267, Actions line 4339.

<a id="trigger-078eeb1c"></a>

### 47. V3 New Build Option - 078EEB1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078ED58C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Unit Type: type index 14 (global list position: V3 Launcher (V3)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [V3 Audio (0BDAB35C)](#trigger-0bdab35c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4196, Events line 4268, Actions line 4340.

<a id="trigger-0bdab35c"></a>

### 48. V3 Audio - 0BDAB35C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [V3 New Build Option (078EEB1C)](#trigger-078eeb1c).

Attached scope: tag definitions 0BDAC95C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_V3.
2. Switch the sidebar to tab 3.
3. Flash cameo/type 314; additional configured duration/location argument 100.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4197, Events line 4269, Actions line 4341.

<a id="trigger-091fcc64"></a>

### 49. Reveal 2nd Ore - 091FCC64

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 091FC8B4 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 12 (cell 68, 150).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4198, Events line 4270, Actions line 4342.

<a id="trigger-07b00f3c"></a>

### 50. Hint_Oil Derricks - 07B00F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 8 tagged map cells: (79, 129), (80, 129), (79, 130), (80, 130), (79, 131), (80, 131), (79, 132), (80, 132); tag 07B01AEC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Display message “HINT: Capture the OIL DERRICKS for extra resources” (MISSION:Sov03aa).
2. Reveal terrain around waypoint 13 (cell 86, 136).
3. Play sound HealCrate.
4. Create radar-event marker type 1 at waypoint 13 (cell 86, 136).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4199, Events line 4271, Actions line 4343.

<a id="trigger-089e7b5c"></a>

### 51. Opening Harass 1 - 089E7B5C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089E77BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [4Rocket Team (0C199C8C)](sov03u-teams.md#team-0c199c8c).
2. Create/recruit team [6 Rocket Team (0C19E23C)](sov03u-teams.md#team-0c19e23c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4200, Events line 4272, Actions line 4344.

<a id="trigger-089e76cc"></a>

### 52. Opening Harass 2 - 089E76CC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089E270C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 360 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [10 GIs (0C19E6DC)](sov03u-teams.md#team-0c19e6dc).
2. Create/recruit team [2Grizzly Team (0A0E259C)](sov03u-teams.md#team-0a0e259c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4201, Events line 4273, Actions line 4345.

<a id="trigger-089e261c"></a>

### 53. Opening Harass 3 - 089E261C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089E21EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 500 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [2Grizzly Team (0A0E259C)](sov03u-teams.md#team-0a0e259c).
2. Create/recruit team [4Rocket Team (0C199C8C)](sov03u-teams.md#team-0c199c8c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4202, Events line 4274, Actions line 4346.

<a id="trigger-089e10fc"></a>

### 54. Opening Harass 4 - 089E10FC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089E65BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [6 Grizzly Team (0C19E49C)](sov03u-teams.md#team-0c19e49c).
2. Create/recruit team [10 GIs (0C19E6DC)](sov03u-teams.md#team-0c19e6dc).
3. Create/recruit team [6 Rocket Team (0C19E23C)](sov03u-teams.md#team-0c19e23c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4203, Events line 4275, Actions line 4347.

<a id="trigger-0765551c"></a>

### 55. Ambient Ocean - 0765551C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07657E3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsHarbor at waypoint 19 (cell 67, 65).
2. Play sound _Amb_OceanHeavy at waypoint 19 (cell 67, 65).
3. Play sound _Amb_OceanHeavy at waypoint 20 (cell 60, 82).
4. Play sound _Amb_OceanLight at waypoint 21 (cell 66, 101).
5. Play sound _Amb_OceanLight at waypoint 23 (cell 56, 116).
6. Play sound _Amb_BirdsHarbor at waypoint 23 (cell 56, 116).
7. Play sound _Amb_OceanHeavy at waypoint 24 (cell 57, 145).
8. Play sound _Amb_BirdsHarbor at waypoint 24 (cell 57, 145).
9. Play sound _Amb_OceanLight at waypoint 25 (cell 114, 106).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4204, Events line 4276, Actions line 4348.

<a id="trigger-0765787c"></a>

### 56. Ambient City - 0765787C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0765772C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_Traffic at waypoint 26 (cell 117, 90).
2. Play sound _Amb_UrbanMurmur1 at waypoint 26 (cell 117, 90).
3. Play sound _Amb_Traffic at waypoint 14 (cell 150, 58).
4. Play sound _Amb_UrbanMurmur2 at waypoint 14 (cell 150, 58).
5. Play sound _Amb_Traffic at waypoint 3 (cell 77, 78).
6. Play sound _Amb_UrbanMurmur1 at waypoint 3 (cell 77, 78).
7. Play sound _Amb_Traffic at waypoint 11 (cell 82, 46).
8. Play sound _Amb_UrbanMurmur2 at waypoint 11 (cell 82, 46).
9. Play sound _Amb_Traffic at waypoint 27 (cell 83, 117).
10. Play sound _Amb_UrbanMurmur1 at waypoint 27 (cell 83, 117).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4205, Events line 4277, Actions line 4349.

<a id="trigger-0a3a685c"></a>

### 57. _Radar Movie - 0A3A685C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A3AB1CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play in-game movie 79.
2. Enable and reset applicable timers for [Sofia 1 (0BD70F40)](#trigger-0bd70f40).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4206, Events line 4278, Actions line 4350.

<a id="trigger-0bdac86c"></a>

### 58. Rocketeer Detected - 0BDAC86C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BD6810C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Infantry Type: type index 4 (global list position: Rocketeer (JUMPJET)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification EVA_EnemyAirArmadaDetected.
2. Enable and reset applicable timers for [Rocketeer Audio (0BDAC57C)](#trigger-0bdac57c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4207, Events line 4279, Actions line 4351.

<a id="trigger-0bdac57c"></a>

### 59. Rocketeer Audio - 0BDAC57C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Rocketeer Detected (0BDAC86C)](#trigger-0bdac86c).

Attached scope: tag definitions 0BDAC66C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_Rocketeer.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4208, Events line 4280, Actions line 4352.

<a id="trigger-0c11663c"></a>

### 60. Hint_Oil Derricks_2 - 0C11663C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tech Oil Derrick (CAOILD), owner Other2 House, cell (84, 138), tag 0C110EAC, persistence mode 0; Tech Oil Derrick (CAOILD), owner Other2 House, cell (88, 134), tag 0C110EAC, persistence mode 0; Tech Oil Derrick (CAOILD), owner Other2 House, cell (84, 134), tag 0C110EAC, persistence mode 0.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “HINT: Capture the OIL DERRICKS for extra resources” (MISSION:Sov03aa).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4209, Events line 4281, Actions line 4353.

<a id="trigger-083ee33c"></a>

### 61. Rubblizer - 083EE33C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CANEWY13), owner Civie1 House, cell (110, 90), tag 083EAD7C, persistence mode 0; Building (CANEWY15), owner Civie1 House, cell (118, 85), tag 083EAD7C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4210, Events line 4282, Actions line 4354.

<a id="trigger-0a50ac5c"></a>

### 62. Garrison Teams - 0A50AC5C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A50A50C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Garrison AF Team (0C1D959C)](sov03u-teams.md#team-0c1d959c).
2. Create/recruit team [Garrison AG Team (0C1D91FC)](sov03u-teams.md#team-0c1d91fc).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4211, Events line 4283, Actions line 4355.

<a id="trigger-082e894c"></a>

### 63. Truck_Smoke - 082E894C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Automobile (SUVW), owner Civie1 House, cell (98, 74), tag 082EDF4C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Particle Anim at; main setting 2; location/duration field AH.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4212, Events line 4284, Actions line 4356.

<a id="trigger-0a07003c"></a>

### 64. Crater_Smoke - 0A07003C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A060AEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Particle Anim at; main setting 2; location/duration field AI.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4213, Events line 4285, Actions line 4357.

<a id="trigger-0991ce5c"></a>

### 65. Left Tower Destroyed - 0991CE5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Left Tower Garrisoned (06526E3C)](#trigger-06526e3c).

Attached scope: Building (CANWY05), owner Civie1 House, cell (95, 27), tag 06526D5C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Left Tower Destroyed (0991CE5C)](#trigger-0991ce5c).
2. Create crate type 2 at waypoint 29 (cell 97, 29).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4214, Events line 4286, Actions line 4358.

<a id="trigger-06526e3c"></a>

### 66. Left Tower Garrisoned - 06526E3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [Left Tower Garrisoned (06526E3C)](#trigger-06526e3c).
2. Reveal the whole map.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4215, Events line 4287, Actions line 4359.

<a id="trigger-09919abc"></a>

### 67. Right Tower Destroyed - 09919ABC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Right Tower Garrisoned (06522F3C)](#trigger-06522f3c).

Attached scope: Building (CANWY05), owner Civie1 House, cell (101, 21), tag 06522E5C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Right Tower Destroyed (09919ABC)](#trigger-09919abc).
2. Create crate type 14 at waypoint 30 (cell 103, 23).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4216, Events line 4288, Actions line 4360.

<a id="trigger-06522f3c"></a>

### 68. Right Tower Garrisoned - 06522F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [Right Tower Garrisoned (06522F3C)](#trigger-06522f3c).
2. Reveal the whole map.

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4217, Events line 4289, Actions line 4361.

<a id="trigger-0858b41c"></a>

### 69. Build War_Yuri Appears - 0858B41C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0858B33C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 14 (global list position: Soviet War Factory (NAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Play Audio (09A2903C)](#trigger-09a2903c).
2. Enable and reset applicable timers for [Play Movie (09A2603C)](#trigger-09a2603c).
3. Enable and reset applicable timers for [4 Psi-Corp Create (0834438C)](#trigger-0834438c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4218, Events line 4290, Actions line 4362.

<a id="trigger-0489224c"></a>

### 70. Lab Damaged - 0489224C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Sell Lab (08AAA2DC)](#trigger-08aaa2dc).

Attached scope: Allied Battle Lab (GATECH), owner BadGuy1 House, cell (101, 27), tag 08AAA1FC, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound WarningAlarm.
2. Display message “MISSION CRITICAL STRUCTURE - Do not destroy!” (MISSION:Sov10d).
3. Disable [Lab Damaged (0489224C)](#trigger-0489224c).

Source locator: MAPS02.MIX/sov03u.map; Triggers line 4219, Events line 4291, Actions line 4363.

[All team rosters and ordered plans](sov03u-teams.md) | [All mission overrides](sov03u-overrides.md)
