# Operation: Liberty

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all06u.map. **Effective extracted member:** MAPS01.MIX/all06u.map. **Trigger definitions:** 74.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all06u-teams.md) | [All mission overrides](all06u-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | URBAN |
| Map size | 0,0,95,105 |
| Visible local rectangle | 2,4,90,95 |
| Placed vehicles | 26 |
| Placed infantry | 37 |
| Placed structures | 165 |
| Placed aircraft | 0 |
| Team templates | 65 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 500 | BadGuy1 |
| 2 | BadGuy2 House | 500 | BadGuy2 |
| 3 | BadGuy3 House | 0 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 20 | Other1 |
| 6 | Other2 House | 0 | Other2 |
| 7 | Other3 House | 0 | Other3 |
| 8 | House Elania | 0 | Elania |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Player on Map,0 |
| 1 | NE1 Bridge Team,0 |
| 2 | NE1 Bridge Destroye,0 |
| 3 | SE2 Bridge Destroye,0 |
| 4 | SE2 Bridge Team,0 |
| 5 | Terror Uncovered,0 |
| 6 | Terror Drones Creat,0 |
| 7 | Fodder5 Go,0 |
| 8 | Bring Camera Back,0 |
| 9 | BO Still Alive,0 |
| 10 | BP Still Alive,0 |
| 11 | BN Still Alive,0 |
| 12 | BQ Still Alive,1 |
| 13 | N Bridge Fixed,0 |
| 14 | BG2 Bridge Team,0 |
| 15 | Drones Away,0 |
| 16 | Ready to Work,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [_Loss Game Over (0AD1988C)](#trigger-0ad1988c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [_Win Game Over (0AD1A66C)](#trigger-0ad1a66c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-03f0703c"></a>

### 1. Prism Fodder 1 Go (M&H) - 03F0703C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Prism Fodder1 (0902AB5C)](all06u-teams.md#team-0902ab5c).
2. Supply reinforcement team [Prism Fodder2 (09FBE48C)](all06u-teams.md#team-09fbe48c).
3. Supply reinforcement team [Prism Fodder3 (0902A1FC)](all06u-teams.md#team-0902a1fc).
4. Production Begins: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
5. AI triggers begin: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
6. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).
7. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6899, Events line 6975, Actions line 7051.

<a id="trigger-07519f3c"></a>

### 2. Player Start Forces Go - 07519F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (78, 140); tag 07519D3C, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Player Starting Forces1 (0AFF3C8C)](all06u-teams.md#team-0aff3c8c).
2. Supply reinforcement team [Player Starting Forces2 (09EE4B7C)](all06u-teams.md#team-09ee4b7c).
3. Supply reinforcement team [Player Starting Forces3 (09EE46CC)](all06u-teams.md#team-09ee46cc).
4. Reveal terrain around waypoint 7 (cell 91, 163).
5. Reveal terrain around waypoint 8 (cell 74, 148).
6. Reveal terrain around waypoint 9 (cell 77, 162).
7. Reveal terrain around waypoint 10 (cell 98, 154).
8. Reveal terrain around waypoint 11 (cell 95, 178).
9. Reveal terrain around waypoint 1 (cell 120, 169).
10. Reveal terrain around waypoint 12 (cell 84, 147).
11. Reveal terrain around waypoint 13 (cell 82, 170).
12. Reveal terrain around waypoint 33 (cell 20, 89).
13. Create radar-event marker type 1 at waypoint 42 (cell 51, 102).
14. Disable player input.
15. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6900, Events line 6976, Actions line 7052.

<a id="trigger-0a1fbadc"></a>

### 3. Player Takes Command - 0A1FBADC

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 63 tagged map cells: (125, 153), (126, 153), (127, 153), (128, 153), (129, 153), (130, 153), (131, 153), (136, 153), (137, 153), (138, 153), (139, 153), (140, 153), (141, 153), (142, 153), (125, 154), (126, 154), (127, 154), (128, 154), (129, 154), (130, 154), (131, 154), (136, 154), (137, 154), (138, 154), (139, 154), (140, 154), (141, 154), (142, 154), (126, 155), (127, 155), (128, 155), (129, 155), (130, 155), (137, 155), (138, 155), (139, 155), (140, 155), (141, 155), (87, 158), (88, 158), (87, 159), (88, 159), (89, 159), (88, 160), (89, 160), (88, 161), (89, 161), (88, 162), (89, 162), (88, 163), (89, 163), (88, 164), (89, 164), (88, 165), (89, 165), (88, 166), (89, 166), (87, 167), (88, 167), (89, 167), (87, 168), (88, 168), (89, 168); tag 0A1F9E1C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [_Loss (Pentagon) (0B1A8A1C)](#trigger-0b1a8a1c).
2. Enable and reset applicable timers for [Prism Fodder 2 Go (M&H) (0AFEA29C)](#trigger-0afea29c).
3. Display message “Pentagon forces transferred to your command” (Mission:All06d1).
4. Display message “Objective 1 Accomplished” (Mission:All06d2).
5. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).
6. Create radar-event marker type 1 at waypoint 31 (cell 111, 170).
7. Enable and reset applicable timers for [Objective 2 Statement (0A4DF5BC)](#trigger-0a4df5bc).
8. Enable and reset applicable timers for [Prism Fodder 2 Go (E) (07AFD59C)](#trigger-07afd59c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6901, Events line 6977, Actions line 7053.

<a id="trigger-0b1a8a1c"></a>

### 4. _Loss (Pentagon) - 0B1A8A1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pentagon (CAWA2B), owner Civie1 House, cell (107, 170), tag 0B46B9CC, persistence mode 1; Pentagon (CAWA2C), owner Civie1 House, cell (103, 170), tag 0B46B9CC, persistence mode 1; Pentagon (CAWA2D), owner Civie1 House, cell (103, 166), tag 0B46B9CC, persistence mode 1; Power Plant (GAPOWR), owner Player House, cell (100, 175), tag 0B46B9CC, persistence mode 1; Power Plant (GAPOWR), owner Player House, cell (102, 175), tag 0B46B9CC, persistence mode 1; Power Plant (GAPOWR), owner Player House, cell (100, 173), tag 0B46B9CC, persistence mode 1; Power Plant (GAPOWR), owner Player House, cell (100, 163), tag 0B46B9CC, persistence mode 1; Power Plant (GAPOWR), owner Player House, cell (102, 163), tag 0B46B9CC, persistence mode 1; Power Plant (GAPOWR), owner Player House, cell (100, 165), tag 0B46B9CC, persistence mode 1; Patriot Missile (NASAM), owner Player House, cell (113, 165), tag 0B46B9CC, persistence mode 1; Patriot Missile (NASAM), owner Player House, cell (113, 174), tag 0B46B9CC, persistence mode 1; Prism Tower (ATESLA), owner Player House, cell (100, 169), tag 0B46B9CC, persistence mode 1; Prism Tower (ATESLA), owner Player House, cell (104, 175), tag 0B46B9CC, persistence mode 1; Prism Tower (ATESLA), owner Player House, cell (114, 170), tag 0B46B9CC, persistence mode 1; Prism Tower (ATESLA), owner Player House, cell (115, 176), tag 0B46B9CC, persistence mode 1; Prism Tower (ATESLA), owner Player House, cell (110, 165), tag 0B46B9CC, persistence mode 1; Prism Tower (ATESLA), owner Player House, cell (115, 164), tag 0B46B9CC, persistence mode 1; Pill Box (GAPILL), owner Player House, cell (116, 168), tag 0B46B9CC, persistence mode 1; Pill Box (GAPILL), owner Player House, cell (116, 172), tag 0B46B9CC, persistence mode 1; Pentagon (CAWA2A), owner Civie1 House, cell (107, 166), tag 0B46B9CC, persistence mode 1; Prism Tower (ATESLA), owner Player House, cell (104, 163), tag 0B46B9CC, persistence mode 1; Prism Tower (ATESLA), owner Player House, cell (110, 174), tag 0B46B9CC, persistence mode 1; Pill Box (GAPILL), owner Player House, cell (97, 165), tag 0B46B9CC, persistence mode 1; Pill Box (GAPILL), owner Player House, cell (97, 173), tag 0B46B9CC, persistence mode 1; Pill Box (GAPILL), owner Player House, cell (112, 168), tag 0B46B9CC, persistence mode 1; Pill Box (GAPILL), owner Player House, cell (112, 171), tag 0B46B9CC, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss Game Over (0AD1988C)](#trigger-0ad1988c).
2. Jump the camera to waypoint 31 (cell 111, 170).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6902, Events line 6978, Actions line 7054.

<a id="trigger-0afea29c"></a>

### 5. Prism Fodder 2 Go (M&H) - 0AFEA29C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Prism Fodder 1 Go (M&H) (03F0703C)](#trigger-03f0703c).

Incoming activation links: enable from [Player Takes Command (0A1FBADC)](#trigger-0a1fbadc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Prism Fodder1 (0902AB5C)](all06u-teams.md#team-0902ab5c).
2. Supply reinforcement team [Prism Fodder2 (09FBE48C)](all06u-teams.md#team-09fbe48c).
3. Supply reinforcement team [Prism Fodder3 (0902A1FC)](all06u-teams.md#team-0902a1fc).
4. Production Begins: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
5. AI triggers begin: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
6. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).
7. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6903, Events line 6979, Actions line 7055.

<a id="trigger-0a4df5bc"></a>

### 6. Objective 2 Statement - 0A4DF5BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Takes Command (0A1FBADC)](#trigger-0a1fbadc).

Attached scope: tag definitions 0A4DE99C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Eliminate all Soviet forces” (MISSION:All06b1).
2. Display message “occupying Washington, DC” (MISSION:All06b2).
3. Play voice notification EVA_NewObjectiveReceived.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6904, Events line 6980, Actions line 7056.

<a id="trigger-07afd59c"></a>

### 7. Prism Fodder 2 Go (E) - 07AFD59C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Prism Fodder 2 Go (M&H) (0AFEA29C)](#trigger-0afea29c).

Incoming activation links: enable from [Player Takes Command (0A1FBADC)](#trigger-0a1fbadc).

Attached scope: tag definitions 03F0018C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Prism Fodder3 (0902A1FC)](all06u-teams.md#team-0902a1fc).
2. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
4. Production Begins: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
5. AI triggers begin: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6905, Events line 6981, Actions line 7057.

<a id="trigger-0ad1988c"></a>

### 8. _Loss Game Over - 0AD1988C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Loss (Pentagon) (0B1A8A1C)](#trigger-0b1a8a1c); enable from [_Loss (Player Only) (0AFEB45C)](#trigger-0afeb45c).

Attached scope: tag definitions 0AD1927C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6906, Events line 6982, Actions line 7058.

<a id="trigger-0afeb45c"></a>

### 9. _Loss (Player Only) - 0AFEB45C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Has Arrived (0AFEBD2C)](#trigger-0afebd2c).

Attached scope: tag definitions 0AFEB0CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss Game Over (0AD1988C)](#trigger-0ad1988c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6907, Events line 6983, Actions line 7059.

<a id="trigger-0afebd2c"></a>

### 10. Player Has Arrived - 0AFEBD2C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AFEB8EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss (Player Only) (0AFEB45C)](#trigger-0afeb45c).
2. Enable and reset applicable timers for [Flank Attack Go (090AF1CC)](#trigger-090af1cc).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6908, Events line 6984, Actions line 7060.

<a id="trigger-090af1cc"></a>

### 11. Flank Attack Go - 090AF1CC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Has Arrived (0AFEBD2C)](#trigger-0afebd2c).

Attached scope: tag definitions 090AC40C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Flank Attack (099FE32C)](all06u-teams.md#team-099fe32c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6909, Events line 6985, Actions line 7061.

<a id="trigger-0afeb7fc"></a>

### 12. _Win Occurs - 0AFEB7FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AFEB54C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
2. Destroyed,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Display message “Objective 2 Accomplished” (Mission:All09d).
2. Enable and reset applicable timers for [_Win Game Over (0AD1A66C)](#trigger-0ad1a66c).
3. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6910, Events line 6986, Actions line 7062.

<a id="trigger-0ad1a66c"></a>

### 13. _Win Game Over - 0AD1A66C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Win Occurs (0AFEB7FC)](#trigger-0afeb7fc).

Attached scope: tag definitions 0AD1A46C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6911, Events line 6987, Actions line 7063.

<a id="trigger-07b1087c"></a>

### 14. Bridge Destroyed (NE1) - 07B1087C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [N Bridge Fixers Go (0979640C)](#trigger-0979640c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 2 (NE1 Bridge Destroye).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6912, Events line 6988, Actions line 7064.

<a id="trigger-0979640c"></a>

### 15. N Bridge Fixers Go - 0979640C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Bridge Destroyed (N) (097CA03C)](#trigger-097ca03c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 13 (N Bridge Fixed) is set.

Flag writers in this mission: clear local flag 13 (N Bridge Fixed) at [N Bridge Fixers Go (0979640C)](#trigger-0979640c); set local flag 13 (N Bridge Fixed) at [Bridge Destroyed (N) (097CA03C)](#trigger-097ca03c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team 0 (template not recovered locally).
2. Clear local flag 13 (N Bridge Fixed).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6913, Events line 6989, Actions line 7065.

<a id="trigger-097ca03c"></a>

### 16. Bridge Destroyed (N) - 097CA03C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 13 (N Bridge Fixed).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6914, Events line 6990, Actions line 7066.

<a id="trigger-0b0a831c"></a>

### 17. Cancel All Bridge Teams - 0B0A831C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [SE2 Bridge Fixers Go (0A9E022C)](#trigger-0a9e022c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Bridge Destroyed (NE1) (07B1087C)](#trigger-07b1087c).
2. Disable [NE1 Fixers Made It? (07A396DC)](#trigger-07a396dc).
3. Disable [NE1 Bridge Fixers Go (07A39E6C)](#trigger-07a39e6c).
4. Disable [Bridge Destroyed (SE2) (03EAB81C)](#trigger-03eab81c).
5. Disable [SE2 Fixers Made It? (07A3ACEC)](#trigger-07a3acec).
6. Disable [SE2 Bridge Fixers Go (0A9E022C)](#trigger-0a9e022c).
7. Disable [Bridge Destroyed (N) (097CA03C)](#trigger-097ca03c).
8. Disable 0 (not a defined local trigger).
9. Disable [N Bridge Fixers Go (0979640C)](#trigger-0979640c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6915, Events line 6991, Actions line 7067.

<a id="trigger-0a9e022c"></a>

### 18. SE2 Bridge Fixers Go - 0A9E022C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Bridge Destroyed (SE2) (03EAB81C)](#trigger-03eab81c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (SE2 Bridge Destroye) is set.

Flag writers in this mission: clear local flag 3 (SE2 Bridge Destroye) at [SE2 Bridge Fixers Go (0A9E022C)](#trigger-0a9e022c); set local flag 3 (SE2 Bridge Destroye) at [Bridge Destroyed (SE2) (03EAB81C)](#trigger-03eab81c); set local flag 3 (SE2 Bridge Destroye) at [SE2 Fixers Made It? (07A3ACEC)](#trigger-07a3acec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [SE Bridge Repair Team 1 (09F9159C)](all06u-teams.md#team-09f9159c).
2. Clear local flag 3 (SE2 Bridge Destroye).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6916, Events line 6992, Actions line 7068.

<a id="trigger-07a396dc"></a>

### 19. NE1 Fixers Made It? - 07A396DC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Cancel All Bridge Teams (0B0A831C)](#trigger-0b0a831c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 2 (NE1 Bridge Destroye).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6917, Events line 6993, Actions line 7069.

<a id="trigger-07a39e6c"></a>

### 20. NE1 Bridge Fixers Go - 07A39E6C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Bridge Destroyed (NE1) (07B1087C)](#trigger-07b1087c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 2 (NE1 Bridge Destroye) is set.

Flag writers in this mission: set local flag 2 (NE1 Bridge Destroye) at [Bridge Destroyed (NE1) (07B1087C)](#trigger-07b1087c); set local flag 2 (NE1 Bridge Destroye) at [NE1 Fixers Made It? (07A396DC)](#trigger-07a396dc); clear local flag 2 (NE1 Bridge Destroye) at [NE1 Bridge Fixers Go (07A39E6C)](#trigger-07a39e6c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [NE Bridge Repair Team (0906DEFC)](all06u-teams.md#team-0906defc).
2. Clear local flag 2 (NE1 Bridge Destroye).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6918, Events line 6994, Actions line 7070.

<a id="trigger-03eab81c"></a>

### 21. Bridge Destroyed (SE2) - 03EAB81C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [NE1 Bridge Fixers Go (07A39E6C)](#trigger-07a39e6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 3 (SE2 Bridge Destroye).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6919, Events line 6995, Actions line 7071.

<a id="trigger-07a3acec"></a>

### 22. SE2 Fixers Made It? - 07A3ACEC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [NE1 Fixers Made It? (07A396DC)](#trigger-07a396dc).

Attached scope: tag definitions 097CD2FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 3 (SE2 Bridge Destroye).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6920, Events line 6996, Actions line 7072.

<a id="trigger-0876ee7c"></a>

### 23. BG1 Garrisoners 2 - 0876EE7C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Garrisoners 1 (087C194C)](#trigger-087c194c).

Attached scope: tag definitions 0879004C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 9 (BO Still Alive) is clear.

Flag writers in this mission: set local flag 9 (BO Still Alive) at [BO Still Kickin? (0BF02E3C)](#trigger-0bf02e3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Garrisoners_B (0BC9456C)](all06u-teams.md#team-0bc9456c).
2. Enable and reset applicable timers for [BG1 Garrisoners 3 (0BEAC89C)](#trigger-0beac89c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6921, Events line 6997, Actions line 7073.

<a id="trigger-0beac89c"></a>

### 24. BG1 Garrisoners 3 - 0BEAC89C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Garrisoners 2 (0876EE7C)](#trigger-0876ee7c).

Attached scope: tag definitions 0BEAC3AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 11 (BN Still Alive) is clear.

Flag writers in this mission: set local flag 11 (BN Still Alive) at [BN Still Kickin? (0988ED8C)](#trigger-0988ed8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Garrisoners_C (0BC941CC)](all06u-teams.md#team-0bc941cc).
2. Enable and reset applicable timers for [BG1 Garrisoners 4 (0BEACF3C)](#trigger-0beacf3c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6922, Events line 6998, Actions line 7074.

<a id="trigger-0beacf3c"></a>

### 25. BG1 Garrisoners 4 - 0BEACF3C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Garrisoners 3 (0BEAC89C)](#trigger-0beac89c).

Attached scope: tag definitions 0BEAC98C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 12 (BQ Still Alive) is clear.

Flag writers in this mission: set local flag 12 (BQ Still Alive) at [BQ Still Kickin? (0988ABBC)](#trigger-0988abbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Garrisoners_D (0BC95C8C)](all06u-teams.md#team-0bc95c8c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6923, Events line 6999, Actions line 7075.

<a id="trigger-087c194c"></a>

### 26. BG1 Garrisoners 1 - 087C194C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 43 tagged map cells: (34, 99), (35, 99), (36, 99), (37, 99), (38, 99), (34, 100), (35, 100), (36, 100), (37, 100), (34, 101), (35, 101), (36, 101), (37, 101), (38, 101), (126, 131), (127, 131), (128, 131), (129, 131), (130, 131), (131, 131), (136, 131), (137, 131), (138, 131), (139, 131), (140, 131), (141, 131), (142, 131), (126, 132), (127, 132), (128, 132), (129, 132), (130, 132), (131, 132), (136, 132), (137, 132), (138, 132), (139, 132), (140, 132), (141, 132), (125, 133), (131, 133), (136, 133), (142, 133); tag 087C135C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).
2. local flag 10 (BP Still Alive) is clear.

Flag writers in this mission: set local flag 10 (BP Still Alive) at [BP Still Kickin? (0988C92C)](#trigger-0988c92c); set local flag 10 (BP Still Alive) at [Did George Survive (0AE0737C)](#trigger-0ae0737c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Garrisoners_A (0AE4FB7C)](all06u-teams.md#team-0ae4fb7c).
2. Enable and reset applicable timers for [BG1 Garrisoners 2 (0876EE7C)](#trigger-0876ee7c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6924, Events line 7000, Actions line 7076.

<a id="trigger-0a6792ec"></a>

### 27. Street Patrols Start - 0A6792EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Production Start (t=10m) (0999341C)](#trigger-0999341c); enable from [BG1 Production Start (t=15m) (081C703C)](#trigger-081c703c); enable from [BG1 Production Start (t=30m) (081DB55C)](#trigger-081db55c); enable from [BG1 Production Start (Sees BG1) (081DE05C)](#trigger-081de05c).

Attached scope: tag definitions 0A67A0EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Street Patrol 1 (0B03493C)](all06u-teams.md#team-0b03493c).
2. Supply reinforcement team [Street Patrol 3 (0B033B5C)](all06u-teams.md#team-0b033b5c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6925, Events line 7001, Actions line 7077.

<a id="trigger-0999341c"></a>

### 28. BG1 Production Start (t=10m) - 0999341C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
4. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).
5. Create/recruit team [BG1 Hard (0BC9FDEC)](all06u-teams.md#team-0bc9fdec).
6. Enable and reset applicable timers for [Street Patrols Start (0A6792EC)](#trigger-0a6792ec).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6926, Events line 7002, Actions line 7078.

<a id="trigger-07af0f3c"></a>

### 29. All BG1 Bldgs KIA - 07AF0F3C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07AF09FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6927, Events line 7003, Actions line 7079.

<a id="trigger-0b0f0f3c"></a>

### 30. All BG2 Bldgs KIA - 0B0F0F3C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B0F067C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. All to Hunt: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6928, Events line 7004, Actions line 7080.

<a id="trigger-09a0e96c"></a>

### 31. Loose the Terror Drones - 09A0E96C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Terror Drone Movie Play (07ABD16C)](#trigger-07abd16c).

Attached scope: tag definitions 07A5DB7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 16 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Terror Inbound (0A9C6C8C)](all06u-teams.md#team-0a9c6c8c).
2. Create radar-event marker type 5 at waypoint 30 (cell 128, 72).
3. Reveal terrain around waypoint 30 (cell 128, 72).
4. Enable and reset applicable timers for [Service Depot Hint (0A4DE7FC)](#trigger-0a4de7fc).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6929, Events line 7005, Actions line 7081.

<a id="trigger-0a4de7fc"></a>

### 32. Service Depot Hint - 0A4DE7FC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Loose the Terror Drones (09A0E96C)](#trigger-09a0e96c).

Attached scope: tag definitions 0A4DE2BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_A6_EvaTerrorAttacks.
2. Display message “HINT: The SERVICE DEPOT can safely remove” (MISSION:All06c1).
3. Display message “Soviet TERROR DRONES from infected vehicles” (MISSION:All06c2).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6930, Events line 7006, Actions line 7082.

<a id="trigger-0a7bf17c"></a>

### 33. BG2 Declare War - 0A7BF17C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7BC0EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Make enemy: owner selector 18 (country/type OTHER1; placed owner Other1 House).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6931, Events line 7007, Actions line 7083.

<a id="trigger-07a6ae9c"></a>

### 34. Prism Fodder5 Go - 07A6AE9C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A6AC9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (Fodder5 Go) is set.

Flag writers in this mission: set local flag 7 (Fodder5 Go) at [Recenter Camera to AF (0C3D103C)](#trigger-0c3d103c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Prism Fodder5 (09E693AC)](all06u-teams.md#team-09e693ac).
2. Move the camera to waypoint 42 (cell 51, 102) with speed setting 4.
3. Display message “Objective 1: Reinforce and take command” (Mission:All06a1).
4. Enable and reset applicable timers for [Prism Fodder Demo1 (M & H) (07B8270C)](#trigger-07b8270c).
5. Enable and reset applicable timers for [Einstein Movie Play (0ADBCBDC)](#trigger-0adbcbdc).
6. Display message “of Allied forces near the Pentagon” (MISSION:All06a2).
7. Enable and reset applicable timers for [Bring Camera Back (07C9B91C)](#trigger-07c9b91c).
8. Play voice notification EVA_ReinforcementsHaveArrived.
9. Enable and reset applicable timers for [Prism Fodder Demo1 (E) (0B4F886C)](#trigger-0b4f886c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6932, Events line 7008, Actions line 7084.

<a id="trigger-07b8270c"></a>

### 35. Prism Fodder Demo1 (M & H) - 07B8270C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prism Fodder5 Go (07A6AE9C)](#trigger-07a6ae9c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Prism Fodder1 (0902AB5C)](all06u-teams.md#team-0902ab5c).
2. Enable and reset applicable timers for [Prism Fodder Demo2 (M & H) (07B83CFC)](#trigger-07b83cfc).
3. Supply reinforcement team [Prism Fodder3 (0902A1FC)](all06u-teams.md#team-0902a1fc).
4. Supply reinforcement team [Prism Fodder4 (0A149EFC)](all06u-teams.md#team-0a149efc).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6933, Events line 7009, Actions line 7085.

<a id="trigger-0adbcbdc"></a>

### 36. Einstein Movie Play - 0ADBCBDC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prism Fodder5 Go (07A6AE9C)](#trigger-07a6ae9c).

Attached scope: tag definitions 0ADBC78C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 88.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6934, Events line 7010, Actions line 7086.

<a id="trigger-07c9b91c"></a>

### 37. Bring Camera Back - 07C9B91C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prism Fodder5 Go (07A6AE9C)](#trigger-07a6ae9c).

Attached scope: tag definitions 07C9B1AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 31 (cell 111, 170) with speed setting 4.
2. Enable player input.
3. Display message “--Battle Control Online--” (MISSION:ALL01q).
4. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6935, Events line 7011, Actions line 7087.

<a id="trigger-0b4f886c"></a>

### 38. Prism Fodder Demo1 (E) - 0B4F886C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Prism Fodder Demo1 (M & H) (07B8270C)](#trigger-07b8270c).

Incoming activation links: enable from [Prism Fodder5 Go (07A6AE9C)](#trigger-07a6ae9c).

Attached scope: tag definitions 07B8211C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Prism Fodder1 (0902AB5C)](all06u-teams.md#team-0902ab5c).
2. Supply reinforcement team [Prism Fodder4 (0A149EFC)](all06u-teams.md#team-0a149efc).
3. Enable and reset applicable timers for [Prism Fodder Demo2 (E) (0B4FB28C)](#trigger-0b4fb28c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6936, Events line 7012, Actions line 7088.

<a id="trigger-07b83cfc"></a>

### 39. Prism Fodder Demo2 (M & H) - 07B83CFC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prism Fodder Demo1 (M & H) (07B8270C)](#trigger-07b8270c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Prism Fodder5 (09E693AC)](all06u-teams.md#team-09e693ac).
2. Supply reinforcement team [Prism Fodder1 (0902AB5C)](all06u-teams.md#team-0902ab5c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6937, Events line 7013, Actions line 7089.

<a id="trigger-0b4fb28c"></a>

### 40. Prism Fodder Demo2 (E) - 0B4FB28C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Prism Fodder Demo2 (M & H) (07B83CFC)](#trigger-07b83cfc).

Incoming activation links: enable from [Prism Fodder Demo1 (E) (0B4F886C)](#trigger-0b4f886c).

Attached scope: tag definitions 07B8396C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Prism Fodder5 (09E693AC)](all06u-teams.md#team-09e693ac).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6938, Events line 7014, Actions line 7090.

<a id="trigger-03ea390c"></a>

### 41. Play Water Sounds - 03EA390C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03EA313C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 37 (cell 29, 90).
2. Play sound _Amb_OceanLight at waypoint 42 (cell 51, 102).
3. Play sound _Amb_OceanHeavy at waypoint 52 (cell 67, 127).
4. Play sound _Amb_OceanLight at waypoint 53 (cell 108, 140).
5. Play sound _Amb_OceanLight at waypoint 54 (cell 93, 79).
6. Play sound _Amb_OceanLight at waypoint 55 (cell 89, 99).
7. Play sound _Amb_OceanLight at waypoint 56 (cell 133, 141).
8. Play sound _Amb_OceanLight at waypoint 57 (cell 177, 101).
9. Play sound _Amb_OceanLight at waypoint 58 (cell 133, 95).
10. Play sound _Amb_OceanLight at waypoint 58 (cell 133, 95).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6939, Events line 7015, Actions line 7091.

<a id="trigger-07411f3c"></a>

### 42. That's not Lincoln - 07411F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Light Post (INGALITE), owner Civie1 House, cell (49, 61), tag 0741191C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play voice notification Mis_A6_EvaNotLincoln.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6940, Events line 7016, Actions line 7092.

<a id="trigger-07a5ed6c"></a>

### 43. Play Park Sounds - 07A5ED6C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 2 tagged map cells: (110, 81), (155, 136); tag 07A5E7AC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsPark at waypoint 60 (cell 155, 136).
2. Play sound _Amb_BirdsPark at waypoint 61 (cell 110, 81).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6941, Events line 7017, Actions line 7093.

<a id="trigger-0b73381c"></a>

### 44. Play Pond Sounds - 0B73381C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B735C6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsPark at waypoint 62 (cell 74, 46).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6942, Events line 7018, Actions line 7094.

<a id="trigger-0adfdc6c"></a>

### 45. BG1 Firesale - 0ADFDC6C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ADF8DCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6943, Events line 7019, Actions line 7095.

<a id="trigger-0adf8cdc"></a>

### 46. BG2 Firesale - 0ADF8CDC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ADF8A2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
2. All to Hunt: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6944, Events line 7020, Actions line 7096.

<a id="trigger-0c140f3c"></a>

### 47. Reveal Reinforce Path - 0C140F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C1405CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 42 (cell 51, 102).
2. Reveal terrain around waypoint 39 (cell 44, 95).
3. Reveal terrain around waypoint 36 (cell 29, 89).
4. Reveal terrain around waypoint 33 (cell 20, 89).
5. Reveal terrain around waypoint 63 (cell 107, 179).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6945, Events line 7021, Actions line 7097.

<a id="trigger-0bf02e3c"></a>

### 48. BO Still Kickin? - 0BF02E3C

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BF0268C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 112 (global list position: Building (CAWASH11)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 9 (BO Still Alive).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6946, Events line 7022, Actions line 7098.

<a id="trigger-0988abbc"></a>

### 49. BQ Still Kickin? - 0988ABBC

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0988A40C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 75 (global list position: Building (CACITY02)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 12 (BQ Still Alive).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6947, Events line 7023, Actions line 7099.

<a id="trigger-0988cf3c"></a>

### 50. Lincoln Fixed Up - 0988CF3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 71 (cell 51, 66).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6948, Events line 7024, Actions line 7100.

<a id="trigger-0988c92c"></a>

### 51. BP Still Kickin? - 0988C92C

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AF4076C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 294 (global list position: Concession Stand (CAMOV02)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 10 (BP Still Alive).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6949, Events line 7025, Actions line 7101.

<a id="trigger-0988c63c"></a>

### 52. Washington Fixed Up - 0988C63C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 70 (cell 120, 62).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6950, Events line 7026, Actions line 7102.

<a id="trigger-0988ed8c"></a>

### 53. BN Still Kickin? - 0988ED8C

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0988E9BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 108 (global list position: Building (CAWASH05)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 11 (BN Still Alive).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6951, Events line 7027, Actions line 7103.

<a id="trigger-0988e7dc"></a>

### 54. Jefferson Fixed Up - 0988E7DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 69 (cell 107, 109).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6952, Events line 7028, Actions line 7104.

<a id="trigger-09e6c08c"></a>

### 55. White House Fixed Up - 09E6C08C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: White House (CAWASH01), owner Civie1 House, cell (97, 16), tag 09E731FC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 72 (cell 98, 20).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6953, Events line 7029, Actions line 7105.

<a id="trigger-0c3d103c"></a>

### 56. Recenter Camera to AF - 0C3D103C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C3EE04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set local flag 7 (Fodder5 Go).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6954, Events line 7030, Actions line 7106.

<a id="trigger-081c703c"></a>

### 57. BG1 Production Start (t=15m) - 081C703C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [BG1 Production Start (t=10m) (0999341C)](#trigger-0999341c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 900 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
4. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).
5. Create/recruit team [BG1 Medium (0BC9F93C)](all06u-teams.md#team-0bc9f93c).
6. Enable and reset applicable timers for [Street Patrols Start (0A6792EC)](#trigger-0a6792ec).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6955, Events line 7031, Actions line 7107.

<a id="trigger-081db55c"></a>

### 58. BG1 Production Start (t=30m) - 081DB55C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [BG1 Production Start (t=15m) (081C703C)](#trigger-081c703c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1800 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
4. Create/recruit team [BG1 Easy (0BC9F48C)](all06u-teams.md#team-0bc9f48c).
5. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).
6. Enable and reset applicable timers for [Street Patrols Start (0A6792EC)](#trigger-0a6792ec).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6956, Events line 7032, Actions line 7108.

<a id="trigger-081de05c"></a>

### 59. BG1 Production Start (Sees BG1) - 081DE05C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BG1 Production Start (t=30m) (081DB55C)](#trigger-081db55c).

Attached scope: Dumpster (CAMISC03), owner Civie1 House, cell (84, 70), tag 099930BC, persistence mode 0; Mr. Yummy's Hot Dogs! (CAMSC01), owner Civie1 House, cell (117, 86), tag 099930BC, persistence mode 0; Outhouse (CAFRMB), owner Civie1 House, cell (104, 78), tag 099930BC, persistence mode 0; Invisible Yellow Light Post (INYELWLAMP), owner Civie1 House, cell (48, 84), tag 099930BC, persistence mode 0; Invisible Yellow Light Post (INYELWLAMP), owner Civie1 House, cell (73, 84), tag 099930BC, persistence mode 0; Soviet Ore Refinery (NAREFN), owner BadGuy1 House, cell (56, 81), tag 099930BC, persistence mode 0; Sentry Gun (NALASR), owner BadGuy1 House, cell (62, 62), tag 099930BC, persistence mode 0; Invisible Light Post (INGALITE), owner Civie1 House, cell (34, 75), tag 099930BC, persistence mode 0; Invisible Light Post (INGALITE), owner Civie1 House, cell (92, 65), tag 099930BC, persistence mode 0; Invisible Light Post (INGALITE), owner Civie1 House, cell (134, 86), tag 099930BC, persistence mode 0; Invisible Light Post (INGALITE), owner Civie1 House, cell (142, 84), tag 099930BC, persistence mode 0; Invisible Light Post (INGALITE), owner Civie1 House, cell (154, 84), tag 099930BC, persistence mode 0; Invisible Light Post (INGALITE), owner Civie1 House, cell (162, 78), tag 099930BC, persistence mode 0; Invisible Light Post (INGALITE), owner Player House, cell (125, 90), tag 099930BC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
4. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).
5. Create/recruit team [BG1 Medium (0BC9F93C)](all06u-teams.md#team-0bc9f93c).
6. Enable and reset applicable timers for [Street Patrols Start (0A6792EC)](#trigger-0a6792ec).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6957, Events line 7033, Actions line 7109.

<a id="trigger-07abd16c"></a>

### 60. Terror Drone Movie Play - 07ABD16C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07ABABFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Terror Drones Creat) is set.

**Then perform these actions in order:**

1. Play in-game movie 87.
2. Enable and reset applicable timers for [Loose the Terror Drones (09A0E96C)](#trigger-09a0e96c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6958, Events line 7034, Actions line 7110.

<a id="trigger-07aba81c"></a>

### 61. Drones Away - 07ABA81C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07ABA4BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 15 (Drones Away) is set.

**Then perform these actions in order:**

1. Reshroud Map At; main setting 30; location/duration field AE.
2. Reshroud Map At; main setting 23; location/duration field X.
3. Reshroud Map At; main setting 22; location/duration field W.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6959, Events line 7035, Actions line 7111.

<a id="trigger-09d6c84c"></a>

### 62. Rubble States - 09D6C84C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09D6C30C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6960, Events line 7036, Actions line 7112.

<a id="trigger-0adf9b2c"></a>

### 63. Did Jeff Survive - 0ADF9B2C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Jefferson Fixed Up (0988E7DC)](#trigger-0988e7dc).

Attached scope: Jefferson Memorial (CAWASH14), owner Civie1 House, cell (106, 106), tag 0988E5DC, persistence mode 0.

**Wait for the recorded events:**

1. global flag 5 is set.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6961, Events line 7037, Actions line 7113.

<a id="trigger-0ae0737c"></a>

### 64. Did George Survive - 0AE0737C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Washington Fixed Up (0988C63C)](#trigger-0988c63c).

Attached scope: Washington Monument (CAWSH12), owner Civie1 House, cell (116, 61), tag 0988C72C, persistence mode 0.

**Wait for the recorded events:**

1. global flag 6 is set.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Set local flag 10 (BP Still Alive).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6962, Events line 7038, Actions line 7114.

<a id="trigger-0ae05b1c"></a>

### 65. Did Abe Survive - 0AE05B1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Lincoln Fixed Up (0988CF3C)](#trigger-0988cf3c).

Attached scope: Lincoln Memorial (CAWASH15), owner Civie1 House, cell (48, 62), tag 0988CC0C, persistence mode 0.

**Wait for the recorded events:**

1. global flag 4 is set.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6963, Events line 7039, Actions line 7115.

<a id="trigger-0ae0551c"></a>

### 66. Smithsonian Castle - 0AE0551C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Smithsonian Castle (CAWASH16), owner Civie1 House, cell (144, 65), tag 0AE0531C, persistence mode 0.

**Wait for the recorded events:**

1. global flag 7 is set.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6964, Events line 7040, Actions line 7116.

<a id="trigger-08339b7c"></a>

### 67. Empty Building at BO - 08339B7C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Eviction Notice (0835364C)](#trigger-0835364c).

Attached scope: Building (CAWASH11), owner Civie1 House, cell (133, 65), tag 0AF4068C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Evict occupants from the attached building.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6965, Events line 7041, Actions line 7117.

<a id="trigger-083393ac"></a>

### 68. Empty Building at BN - 083393AC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Eviction Notice (0835364C)](#trigger-0835364c).

Attached scope: Building (CAWASH05), owner Civie1 House, cell (143, 81), tag 0AF404BC, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Evict occupants from the attached building.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6966, Events line 7042, Actions line 7118.

<a id="trigger-08353dac"></a>

### 69. Empty Building at BQ - 08353DAC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Eviction Notice (0835364C)](#trigger-0835364c).

Attached scope: Building (CANEWY01), owner Civie1 House, cell (31, 76), tag 0AF40EEC, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Evict occupants from the attached building.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6967, Events line 7043, Actions line 7119.

<a id="trigger-0835385c"></a>

### 70. Empty Building at BP - 0835385C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Eviction Notice (0835364C)](#trigger-0835364c).

Attached scope: Bunker (CABUNK01), owner Civie1 House, cell (117, 65), tag 0B4FC35C, persistence mode 0.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Evict occupants from the attached building.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6968, Events line 7044, Actions line 7120.

<a id="trigger-0835364c"></a>

### 71. Eviction Notice - 0835364C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08354E9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Empty Building at BN (083393AC)](#trigger-083393ac).
2. Enable and reset applicable timers for [Empty Building at BO (08339B7C)](#trigger-08339b7c).
3. Enable and reset applicable timers for [Empty Building at BP (0835385C)](#trigger-0835385c).
4. Enable and reset applicable timers for [Empty Building at BQ (08353DAC)](#trigger-08353dac).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6969, Events line 7045, Actions line 7121.

<a id="trigger-06446dac"></a>

### 72. Reinforcements Ready - 06446DAC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0644103C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 16 (Ready to Work) is set.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsReady.

Source locator: MAPS01.MIX/all06u.map; Triggers line 6970, Events line 7046, Actions line 7122.

<a id="trigger-0cdbf51c"></a>

### 73. Civilian Panic-ers - 0CDBF51C

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 42 tagged map cells: (156, 73), (141, 74), (142, 74), (143, 74), (144, 74), (145, 74), (146, 74), (147, 74), (148, 74), (149, 74), (150, 74), (151, 74), (152, 74), (153, 74), (154, 74), (155, 74), (157, 74), (158, 74), (159, 74), (160, 74), (161, 74), (162, 74), (141, 75), (162, 75), (141, 76), (162, 76), (141, 77), (162, 77), (141, 78), (141, 79), (162, 79), (141, 80), (162, 80), (141, 81), (162, 81), (141, 82), (162, 82), (141, 83), (162, 83), (141, 84), (162, 84), (163, 84); tag 0CDC0F4C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Create/recruit team [Civilian Panic (0CDBD16C)](all06u-teams.md#team-0cdbd16c).
2. Play sound CivAllFear at waypoint 80 (cell 154, 80).
3. Enable and reset applicable timers for [Stop the Panic (0A410A3C)](#trigger-0a410a3c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6971, Events line 7047, Actions line 7123.

<a id="trigger-0a410a3c"></a>

### 74. Stop the Panic - 0A410A3C

Owner reference: Civilian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Civilian Panic-ers (0CDBF51C)](#trigger-0cdbf51c).

Attached scope: tag definitions 0A41052C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Civilian Panic (0CDBD16C)](all06u-teams.md#team-0cdbd16c).

Source locator: MAPS01.MIX/all06u.map; Triggers line 6972, Events line 7048, Actions line 7124.

[All team rosters and ordered plans](all06u-teams.md) | [All mission overrides](all06u-overrides.md)
