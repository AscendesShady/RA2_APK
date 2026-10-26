# Operation: Mirage

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all10s.map. **Effective extracted member:** MAPS01.MIX/all10s.map. **Trigger definitions:** 89.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all10s-teams.md) | [All mission overrides](all10s-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | SNOW |
| Map size | 0,0,105,105 |
| Visible local rectangle | 5,5,95,94 |
| Placed vehicles | 10 |
| Placed infantry | 43 |
| Placed structures | 140 |
| Placed aircraft | 0 |
| Team templates | 66 |

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
| 0 | Einsteins Gift FLG,0 |
| 1 | Einstein Audio1,0 |
| 2 | Einstein Audio2,0 |
| 3 | Einstein Audio3,0 |
| 4 | SpySat Audio Played,0 |
| 5 | Polar Bears Gone,0 |
| 6 | Woman in Car,0 |
| 7 | Spawn Crate,0 |
| 8 | Spawn Crate2,0 |
| 9 | Spawn Crate3,0 |
| 10 | Spawn Crate4,0 |
| 11 | Spawn Crate5,0 |
| 12 | Spawn Crate6,0 |
| 13 | Spawn Crate7,0 |
| 14 | Purifier Exists,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [_Loss (Game Over) (09F7978C)](#trigger-09f7978c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 14 (country/type PLAYER; placed owner Player House) the loser. |
| [_Win (Game Over) (09F864EC)](#trigger-09f864ec) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 14 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-0912ca20"></a>

### 1. Reveal Allies - 0912CA20

Owner reference: Einstein. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0912C4D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 0 (cell 98, 172).
2. Reveal terrain around waypoint 1 (cell 80, 58).
3. Reveal terrain around waypoint 2 (cell 111, 40).
4. Reveal terrain around waypoint 3 (cell 145, 72).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7238, Events line 7329, Actions line 7420.

<a id="trigger-03d8b8d0"></a>

### 2. _2 Move Camera to Einstein - 03D8B8D0

Owner reference: Einstein. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03D8B210 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Move the camera to waypoint 4 (cell 107, 175) with speed setting 4.
2. Create radar-event marker type 1 at waypoint 4 (cell 107, 175).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7239, Events line 7330, Actions line 7421.

<a id="trigger-03d8ce20"></a>

### 3. _5 Player Start - 03D8CE20

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_4 Enable Player Start (0BF2B960)](#trigger-0bf2b960).

Attached scope: tag definitions 03D8CC90 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Remove instances of the team organization (not automatically its surviving objects) [Einsteins Gift (0E5FA71C)](all10s-teams.md#team-0e5fa71c).
3. Enable and reset applicable timers for [_6 Begin Sov Invasion (092A3410)](#trigger-092a3410).
4. Display message “--Battle Control Online--” (MISSION:ALL01q).
5. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7240, Events line 7331, Actions line 7422.

<a id="trigger-092a3410"></a>

### 4. _6 Begin Sov Invasion - 092A3410

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_5 Player Start (03D8CE20)](#trigger-03d8ce20).

Attached scope: tag definitions 092A1DB0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 Invasion 2 (09E7F0C0)](all10s-teams.md#team-09e7f0c0).
2. Supply reinforcement team [BG2 Invasion 2 (0B5A8190)](all10s-teams.md#team-0b5a8190).
3. Supply reinforcement team [BG3 Invasion 2 (09D44B20)](all10s-teams.md#team-09d44b20).
4. Enable and reset applicable timers for [_7 Second Wave (0B5B32F0)](#trigger-0b5b32f0).
5. Display message “ALERT! Soviet Invasion Forces Detected. ALERT!” (MISSION:All10b1).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7241, Events line 7332, Actions line 7423.

<a id="trigger-0b5b32f0"></a>

### 5. _7 Second Wave - 0B5B32F0

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_6 Begin Sov Invasion (092A3410)](#trigger-092a3410).

Attached scope: tag definitions 0B5B5ED0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 Invasion 1 (0ADAEEFC)](all10s-teams.md#team-0adaeefc).
2. Supply reinforcement team [BG2 Invasion 1 (09D45C10)](all10s-teams.md#team-09d45c10).
3. Supply reinforcement team [BG3 Invasion 1 (09EE54D0)](all10s-teams.md#team-09ee54d0).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7242, Events line 7333, Actions line 7424.

<a id="trigger-0bf20f60"></a>

### 6. _3 Move Camera to F - 0BF20F60

Owner reference: Einstein. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 9 tagged map cells: (110, 179), (111, 179), (112, 179), (110, 180), (111, 180), (112, 180), (110, 181), (111, 181), (112, 181); tag 0BF20CF0, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type EINSTEIN; placed owner Einstein House).

**Then perform these actions in order:**

1. Move the camera to waypoint 5 (cell 117, 169) with speed setting 1.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7243, Events line 7334, Actions line 7425.

<a id="trigger-0bf2b960"></a>

### 7. _4 Enable Player Start - 0BF2B960

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BF2B3D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Einsteins Gift FLG) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_5 Player Start (03D8CE20)](#trigger-03d8ce20).
2. Display message “HINT: When the MIRAGE TANK stops, it” (MISSION:All10a1).
3. Display message “cloaks itself as a TREE and waits to ambush” (MISSION:All10a2).
4. Display message “passing enemy forces” (MISSION:All10a3).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7244, Events line 7335, Actions line 7426.

<a id="trigger-08dc0ba0"></a>

### 8. _1 Spawn Mirages - 08DC0BA0

Owner reference: Einstein. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DC09C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Einsteins Gift (0E5FA71C)](all10s-teams.md#team-0e5fa71c).
2. Make enemy: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).
3. Make enemy: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).
4. Make enemy: owner selector 17 (country/type BADGUY3; placed owner BadGuy3 House).
5. Play in-game movie 111.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7245, Events line 7336, Actions line 7427.

<a id="trigger-0b0cf040"></a>

### 9. Loss Einstein KIA - 0B0CF040

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Jump the camera to waypoint 0 (cell 98, 172).
2. Enable and reset applicable timers for [_Loss (Game Over) (09F7978C)](#trigger-09f7978c).
3. Play voice notification EVA_CriticalStrucureLost.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7246, Events line 7337, Actions line 7428.

<a id="trigger-09f7978c"></a>

### 10. _Loss (Game Over) - 09F7978C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Loss Einstein KIA (0B0CF040)](#trigger-0b0cf040); enable from [Loss Player KIA (0B0CC050)](#trigger-0b0cc050); enable from [Loss Captured by BG1 (089C46E0)](#trigger-089c46e0); enable from [Loss Captured by BG2 (09FA7F40)](#trigger-09fa7f40); enable from [Loss Captured by BG3 (0A37DCE0)](#trigger-0a37dce0).

Attached scope: tag definitions 09F7933C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 14 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7247, Events line 7338, Actions line 7429.

<a id="trigger-0b0cc050"></a>

### 11. Loss Player KIA - 0B0CC050

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Loss Einstein KIA (0B0CF040)](#trigger-0b0cf040).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 14 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss (Game Over) (09F7978C)](#trigger-09f7978c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7248, Events line 7339, Actions line 7430.

<a id="trigger-08db0bd0"></a>

### 12. German1 Attacked - 08DB0BD0

Owner reference: Germany1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: GI (E1), owner German1 House, cell (79, 52), tag 08DB0570, persistence mode 0; GI (E1), owner German1 House, cell (81, 52), tag 08DB0570, persistence mode 0; Pill Box (GAPILL), owner German1 House, cell (82, 52), tag 08DB0570, persistence mode 0; Pill Box (GAPILL), owner German1 House, cell (78, 52), tag 08DB0570, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [German1 Guards (09DD39D0)](all10s-teams.md#team-09dd39d0).
2. Create radar-event marker type 0 at waypoint 1 (cell 80, 58).
3. Enable and reset applicable timers for [German1 Explode (09EE4770)](#trigger-09ee4770).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7249, Events line 7340, Actions line 7431.

<a id="trigger-09ee4770"></a>

### 13. German1 Explode - 09EE4770

Owner reference: Germany1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [German1 Attacked (08DB0BD0)](#trigger-08db0bd0).

Attached scope: Barrels (CAMISC01), owner German1 House, cell (86, 54), tag 09EE6F70, persistence mode 0; Barrels (CAMISC01), owner German1 House, cell (82, 61), tag 09EE6F70, persistence mode 0; Barrel (CAMISC02), owner German1 House, cell (78, 54), tag 09EE6F70, persistence mode 0; Barrel (CAMISC02), owner German1 House, cell (76, 61), tag 09EE6F70, persistence mode 0; Barrel (CAMISC02), owner German2 House, cell (115, 38), tag 09EE6F70, persistence mode 0.

**Wait for the recorded events:**

1. A random delay centered on 6 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Supply reinforcement team [BG1 Invasion 3 (0AD31B7C)](all10s-teams.md#team-0ad31b7c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7250, Events line 7341, Actions line 7432.

<a id="trigger-0931e830"></a>

### 14. German2 Attacked - 0931E830

Owner reference: Germany2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: GI (E1), owner German2 House, cell (112, 36), tag 0931E250, persistence mode 0; GI (E1), owner German2 House, cell (109, 36), tag 0931E250, persistence mode 0; Pill Box (GAPILL), owner German2 House, cell (113, 36), tag 0931E250, persistence mode 0; Pill Box (GAPILL), owner German2 House, cell (108, 36), tag 0931E250, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [German2 Guards (09DD3560)](all10s-teams.md#team-09dd3560).
2. Create radar-event marker type 0 at waypoint 2 (cell 111, 40).
3. Enable and reset applicable timers for [German2 Explode (09EE67B0)](#trigger-09ee67b0).
4. Do Explosion At; main setting 35; location/duration field AF.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7251, Events line 7342, Actions line 7433.

<a id="trigger-09ee67b0"></a>

### 15. German2 Explode - 09EE67B0

Owner reference: Germany2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [German2 Attacked (0931E830)](#trigger-0931e830).

Attached scope: Barrels (CAMISC01), owner German2 House, cell (108, 44), tag 09EE65D0, persistence mode 0; Barrels (CAMISC01), owner German2 House, cell (106, 40), tag 09EE65D0, persistence mode 0; Barrels (CAMISC01), owner German2 House, cell (109, 38), tag 09EE65D0, persistence mode 0; Barrel (CAMISC02), owner German2 House, cell (115, 41), tag 09EE65D0, persistence mode 0.

**Wait for the recorded events:**

1. A random delay centered on 8 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Supply reinforcement team [BG2 Invasion 3 (0AD316CC)](all10s-teams.md#team-0ad316cc).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7252, Events line 7343, Actions line 7434.

<a id="trigger-0931e070"></a>

### 16. German3 Attacked - 0931E070

Owner reference: Germany3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: GI (E1), owner German3 House, cell (150, 72), tag 09319BA0, persistence mode 0; GI (E1), owner German3 House, cell (150, 70), tag 09319BA0, persistence mode 0; Pill Box (GAPILL), owner German3 House, cell (150, 74), tag 09319BA0, persistence mode 0; Pill Box (GAPILL), owner German3 House, cell (150, 68), tag 09319BA0, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create radar-event marker type 0 at waypoint 3 (cell 145, 72).
2. Create/recruit team [German3 Guards (09DD30F0)](all10s-teams.md#team-09dd30f0).
3. Enable and reset applicable timers for [German3 Explode (09EE63A0)](#trigger-09ee63a0).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7253, Events line 7344, Actions line 7435.

<a id="trigger-09ee63a0"></a>

### 17. German3 Explode - 09EE63A0

Owner reference: Germany3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [German3 Attacked (0931E070)](#trigger-0931e070).

Attached scope: Barrel (CAMISC02), owner German3 House, cell (140, 67), tag 09EE6210, persistence mode 0; Barrel (CAMISC02), owner German3 House, cell (148, 67), tag 09EE6210, persistence mode 0; Barrels (CAMISC01), owner German3 House, cell (148, 74), tag 09EE6210, persistence mode 0; Barrels (CAMISC01), owner German3 House, cell (141, 77), tag 09EE6210, persistence mode 0; Barrels (CAMISC01), owner German3 House, cell (143, 72), tag 09EE6210, persistence mode 0.

**Wait for the recorded events:**

1. A random delay centered on 8 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Supply reinforcement team [BG3 Invasion 3 (0AD3121C)](all10s-teams.md#team-0ad3121c).
3. Do Explosion At; main setting 35; location/duration field AA.
4. Do Explosion At; main setting 35; location/duration field Z.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7254, Events line 7345, Actions line 7436.

<a id="trigger-08db3810"></a>

### 18. German1 KIA - 08DB3810

Owner reference: Germany1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DB3370 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 18 (country/type GERMANY1; placed owner German1 House).

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 MCV (0A287950)](all10s-teams.md#team-0a287950).
2. Reshroud Map At; main setting 1; location/duration field B.
3. Remove instances of the team organization (not automatically its surviving objects) [BG1 Invasion 1 (0ADAEEFC)](all10s-teams.md#team-0adaeefc).
4. Remove instances of the team organization (not automatically its surviving objects) [BG1 Invasion 2 (09E7F0C0)](all10s-teams.md#team-09e7f0c0).
5. Remove instances of the team organization (not automatically its surviving objects) [BG1 Invasion 3 (0AD31B7C)](all10s-teams.md#team-0ad31b7c).
6. Enable and reset applicable timers for [BG1 Invaders Reform (0925E080)](#trigger-0925e080).
7. Reshroud Map At; main setting 11; location/duration field L.
8. Reshroud Map At; main setting 32; location/duration field AG.
9. Reshroud Map At; main setting 33; location/duration field AH.
10. Reshroud Map At; main setting 34; location/duration field AI.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7255, Events line 7346, Actions line 7437.

<a id="trigger-0925e080"></a>

### 19. BG1 Invaders Reform - 0925E080

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [German1 KIA (08DB3810)](#trigger-08db3810).

Attached scope: tag definitions 0925F310 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Invasion 1a (09D599A0)](all10s-teams.md#team-09d599a0).
2. Create/recruit team [BG1 Invasion 2a (09E7A4D0)](all10s-teams.md#team-09e7a4d0).
3. Create/recruit team [BG1 Invasion 3a (09D592C0)](all10s-teams.md#team-09d592c0).
4. Make enemy: owner selector 13 (country/type EINSTEIN; placed owner Einstein House).
5. Make enemy: owner selector 14 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7256, Events line 7347, Actions line 7438.

<a id="trigger-08db4f60"></a>

### 20. German2 KIA - 08DB4F60

Owner reference: Germany2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DB1BA0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 19 (country/type GERMANY2; placed owner German2 House).

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 MCV (08DB22A0)](all10s-teams.md#team-08db22a0).
2. Reshroud Map At; main setting 2; location/duration field C.
3. Remove instances of the team organization (not automatically its surviving objects) [BG2 Invasion 1 (09D45C10)](all10s-teams.md#team-09d45c10).
4. Remove instances of the team organization (not automatically its surviving objects) [BG2 Invasion 2 (0B5A8190)](all10s-teams.md#team-0b5a8190).
5. Remove instances of the team organization (not automatically its surviving objects) [BG2 Invasion 3 (0AD316CC)](all10s-teams.md#team-0ad316cc).
6. Enable and reset applicable timers for [BG2 Invaders Reform (0924E6D0)](#trigger-0924e6d0).
7. Reshroud Map At; main setting 35; location/duration field AJ.
8. Reshroud Map At; main setting 12; location/duration field M.
9. Reshroud Map At; main setting 36; location/duration field AK.
10. Reshroud Map At; main setting 29; location/duration field AD.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7257, Events line 7348, Actions line 7439.

<a id="trigger-0924e6d0"></a>

### 21. BG2 Invaders Reform - 0924E6D0

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [German2 KIA (08DB4F60)](#trigger-08db4f60).

Attached scope: tag definitions 092520E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Invasion 1a (09D591B0)](all10s-teams.md#team-09d591b0).
2. Create/recruit team [BG2 Invasion 2a (09D58A50)](all10s-teams.md#team-09d58a50).
3. Create/recruit team [BG2 Invasion 3a (09E795D0)](all10s-teams.md#team-09e795d0).
4. Make enemy: owner selector 13 (country/type EINSTEIN; placed owner Einstein House).
5. Make enemy: owner selector 14 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7258, Events line 7349, Actions line 7440.

<a id="trigger-08db49a0"></a>

### 22. German3 KIA - 08DB49A0

Owner reference: Germany3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DB4550 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 20 (country/type GERMANY3; placed owner German3 House).

**Then perform these actions in order:**

1. Supply reinforcement team [BG3 MCV (08DB1420)](all10s-teams.md#team-08db1420).
2. Reshroud Map At; main setting 3; location/duration field D.
3. Remove instances of the team organization (not automatically its surviving objects) [BG3 Invasion 1 (09EE54D0)](all10s-teams.md#team-09ee54d0).
4. Remove instances of the team organization (not automatically its surviving objects) [BG3 Invasion 2 (09D44B20)](all10s-teams.md#team-09d44b20).
5. Remove instances of the team organization (not automatically its surviving objects) [BG3 Invasion 3 (0AD3121C)](all10s-teams.md#team-0ad3121c).
6. Enable and reset applicable timers for [BG3 Invaders Reform (09250A70)](#trigger-09250a70).
7. Reshroud Map At; main setting 37; location/duration field AL.
8. Reshroud Map At; main setting 38; location/duration field AM.
9. Reshroud Map At; main setting 39; location/duration field AN.
10. Reshroud Map At; main setting 40; location/duration field AO.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7259, Events line 7350, Actions line 7441.

<a id="trigger-09250a70"></a>

### 23. BG3 Invaders Reform - 09250A70

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [German3 KIA (08DB49A0)](#trigger-08db49a0).

Attached scope: tag definitions 09273220 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [BG3 Invasion 1a (09D58370)](all10s-teams.md#team-09d58370).
2. Create/recruit team [BG3 Invasion 2a (09E79150)](all10s-teams.md#team-09e79150).
3. Create/recruit team [BG3 Invasion 3a (09D67BA0)](all10s-teams.md#team-09d67ba0).
4. Make enemy: owner selector 13 (country/type EINSTEIN; placed owner Einstein House).
5. Make enemy: owner selector 14 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7260, Events line 7351, Actions line 7442.

<a id="trigger-08dc9190"></a>

### 24. BG1 Production Start - 08DC9190

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Production Start Enable (0A46D390)](#trigger-0a46d390).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).
3. Destroy the attached object through the scripted destruction action.
4. Enable and reset applicable timers for [BG1 Firesale Enabler (0AC09D2C)](#trigger-0ac09d2c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7261, Events line 7352, Actions line 7443.

<a id="trigger-0ac09d2c"></a>

### 25. BG1 Firesale Enabler - 0AC09D2C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Production Start (08DC9190)](#trigger-08dc9190); enable from [Kill BG1 Local Guy (0AD3822C)](#trigger-0ad3822c).

Attached scope: tag definitions 0AC0BA5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 Firesale (0AC0257C)](#trigger-0ac0257c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7262, Events line 7353, Actions line 7444.

<a id="trigger-0ac0257c"></a>

### 26. BG1 Firesale - 0AC0257C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Firesale Enabler (0AC09D2C)](#trigger-0ac09d2c).

Attached scope: tag definitions 0AC066DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).
2. Enable and reset applicable timers for [BG1 All to Hunt (08FB68BC)](#trigger-08fb68bc).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7263, Events line 7354, Actions line 7445.

<a id="trigger-08fb68bc"></a>

### 27. BG1 All to Hunt - 08FB68BC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Firesale (0AC0257C)](#trigger-0ac0257c).

Attached scope: tag definitions 08FB73EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7264, Events line 7355, Actions line 7446.

<a id="trigger-08dc95c0"></a>

### 28. BG2 Production Start - 08DC95C0

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG2 Production Enable (0A468930)](#trigger-0a468930).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).
2. AI triggers begin: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).
3. Destroy the attached object through the scripted destruction action.
4. Enable and reset applicable timers for [BG2 Firesale Enabler (0AC0326C)](#trigger-0ac0326c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7265, Events line 7356, Actions line 7447.

<a id="trigger-0ac0326c"></a>

### 29. BG2 Firesale Enabler - 0AC0326C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG2 Production Start (08DC95C0)](#trigger-08dc95c0); enable from [Kill BG2 Local Guy (0AD3EBBC)](#trigger-0ad3ebbc).

Attached scope: tag definitions 0AC09F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG2 Firesale (0AC065EC)](#trigger-0ac065ec).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7266, Events line 7357, Actions line 7448.

<a id="trigger-0ac0044c"></a>

### 30. BG3 Firesale Enabler - 0AC0044C

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG3 Production Start (08DCA960)](#trigger-08dca960); enable from [Kill BG3 Local Guy (0AD3E9AC)](#trigger-0ad3e9ac).

Attached scope: tag definitions 0AC057BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG3 Firesale (0AC00A8C)](#trigger-0ac00a8c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7267, Events line 7358, Actions line 7449.

<a id="trigger-0ac00a8c"></a>

### 31. BG3 Firesale - 0AC00A8C

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG3 Firesale Enabler (0AC0044C)](#trigger-0ac0044c).

Attached scope: tag definitions 0AC0053C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 17 (country/type BADGUY3; placed owner BadGuy3 House).
2. Enable and reset applicable timers for [BG3 All to Hunt (08FB1E5C)](#trigger-08fb1e5c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7268, Events line 7359, Actions line 7450.

<a id="trigger-0ac065ec"></a>

### 32. BG2 Firesale - 0AC065EC

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG2 Firesale Enabler (0AC0326C)](#trigger-0ac0326c).

Attached scope: tag definitions 0AC063AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).
2. Enable and reset applicable timers for [BG2 All to Hunt (08FB473C)](#trigger-08fb473c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7269, Events line 7360, Actions line 7451.

<a id="trigger-08fb1e5c"></a>

### 33. BG3 All to Hunt - 08FB1E5C

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG3 Firesale (0AC00A8C)](#trigger-0ac00a8c).

Attached scope: tag definitions 08FBB30C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 17 (country/type BADGUY3; placed owner BadGuy3 House).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7270, Events line 7361, Actions line 7452.

<a id="trigger-08fb473c"></a>

### 34. BG2 All to Hunt - 08FB473C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG2 Firesale (0AC065EC)](#trigger-0ac065ec).

Attached scope: tag definitions 08FB1F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7271, Events line 7362, Actions line 7453.

<a id="trigger-08dca960"></a>

### 35. BG3 Production Start - 08DCA960

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG3 Production Enable (0A4685D0)](#trigger-0a4685d0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 17 (country/type BADGUY3; placed owner BadGuy3 House).
2. AI triggers begin: owner selector 17 (country/type BADGUY3; placed owner BadGuy3 House).
3. Destroy the attached object through the scripted destruction action.
4. Enable and reset applicable timers for [BG3 Firesale Enabler (0AC0044C)](#trigger-0ac0044c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7272, Events line 7363, Actions line 7454.

<a id="trigger-0924eb00"></a>

### 36. Win - 0924EB00

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09250080 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).
2. Destroyed,  All: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).
3. Destroyed,  All: owner selector 17 (country/type BADGUY3; placed owner BadGuy3 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Win (Game Over) (09F864EC)](#trigger-09f864ec).
2. Make side cheer: owner selector 14 (country/type PLAYER; placed owner Player House).
3. Make side cheer: owner selector 13 (country/type EINSTEIN; placed owner Einstein House).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7273, Events line 7364, Actions line 7455.

<a id="trigger-09f864ec"></a>

### 37. _Win (Game Over) - 09F864EC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win (0924EB00)](#trigger-0924eb00).

Attached scope: tag definitions 09F8623C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 14 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7274, Events line 7365, Actions line 7456.

<a id="trigger-0a46d390"></a>

### 38. BG1 Production Start Enable - 0A46D390

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A468DD0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 Production Start (08DC9190)](#trigger-08dc9190).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7275, Events line 7366, Actions line 7457.

<a id="trigger-0a468930"></a>

### 39. BG2 Production Enable - 0A468930

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A4686B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG2 Production Start (08DC95C0)](#trigger-08dc95c0).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7276, Events line 7367, Actions line 7458.

<a id="trigger-0a4685d0"></a>

### 40. BG3 Production Enable - 0A4685D0

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A468400 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG3 Production Start (08DCA960)](#trigger-08dca960).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7277, Events line 7368, Actions line 7459.

<a id="trigger-0a468320"></a>

### 41. Apocalypse Created (SpySat) - 0A468320

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Building Type: type index 62 (global list position: SpySat Uplink (GASPYSAT)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [First Apocalypse Sighting (0AD0D6CC)](all10s-teams.md#team-0ad0d6cc).
2. Enable and reset applicable timers for [Apoc Sighted (SpySat) (0A46CAF0)](#trigger-0a46caf0).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7278, Events line 7369, Actions line 7460.

<a id="trigger-0a46caf0"></a>

### 42. Apoc Sighted (SpySat) - 0A46CAF0

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Apocalypse Created (SpySat) (0A468320)](#trigger-0a468320).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Play in-game movie 102.
2. Reveal terrain around waypoint 27 (cell 111, 19).
3. Jump the camera to waypoint 27 (cell 111, 19).
4. Flash team [First Apocalypse Sighting (0AD0D6CC)](all10s-teams.md#team-0ad0d6cc) with duration setting 30.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7279, Events line 7370, Actions line 7461.

<a id="trigger-08933b30"></a>

### 43. BG1 Summon Harvester - 08933B30

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08932C70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 15 (global list position: Soviet Ore Refinery (NAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 Extra Harvester (0A0CA0D0)](all10s-teams.md#team-0a0ca0d0) at waypoint 8 (cell 80, 32).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7280, Events line 7371, Actions line 7462.

<a id="trigger-0893ae50"></a>

### 44. BG3 Summon Harvester - 0893AE50

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0893A970 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 15 (global list position: Soviet Ore Refinery (NAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [BG3 Extra Harvester (0893D580)](all10s-teams.md#team-0893d580) at waypoint 10 (cell 169, 71).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7281, Events line 7372, Actions line 7463.

<a id="trigger-0893a890"></a>

### 45. BG2 Summon Harvester - 0893A890

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0893A690 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 15 (global list position: Soviet Ore Refinery (NAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 Extra Harvester (08938F10)](all10s-teams.md#team-08938f10) at waypoint 9 (cell 111, 13).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7282, Events line 7373, Actions line 7464.

<a id="trigger-09d79700"></a>

### 46. Apocalypse Created (timed) - 09D79700

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Apocalypse Created (SpySat) (0A468320)](#trigger-0a468320).

Incoming activation links: enable from [Apocalypse Created (timed) (09D79700)](#trigger-09d79700).

Attached scope: tag definitions 0A46D780 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 900 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [First Apocalypse Sighting (0AD0D6CC)](all10s-teams.md#team-0ad0d6cc).
2. Enable and reset applicable timers for [Apocalypse Created (timed) (09D79700)](#trigger-09d79700).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7283, Events line 7374, Actions line 7465.

<a id="trigger-089c46e0"></a>

### 47. Loss Captured by BG1 - 089C46E0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Loss Player KIA (0B0CC050)](#trigger-0b0cc050).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 8 (global list position: Einstein's Laboratory (CALAB)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss (Game Over) (09F7978C)](#trigger-09f7978c).
2. Jump the camera to waypoint 0 (cell 98, 172).
3. Play voice notification EVA_CriticalStrucureLost.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7284, Events line 7375, Actions line 7466.

<a id="trigger-09fa7f40"></a>

### 48. Loss Captured by BG2 - 09FA7F40

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Loss Captured by BG1 (089C46E0)](#trigger-089c46e0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 8 (global list position: Einstein's Laboratory (CALAB)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss (Game Over) (09F7978C)](#trigger-09f7978c).
2. Jump the camera to waypoint 0 (cell 98, 172).
3. Play voice notification EVA_CriticalStrucureLost.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7285, Events line 7376, Actions line 7467.

<a id="trigger-0a37dce0"></a>

### 49. Loss Captured by BG3 - 0A37DCE0

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Loss Captured by BG2 (09FA7F40)](#trigger-09fa7f40).

Attached scope: Einstein's Laboratory (CALAB), owner Einstein House, cell (99, 173), tag 0B0CF980, persistence mode 0.

**Wait for the recorded events:**

1. Building exists: type index 8 (global list position: Einstein's Laboratory (CALAB)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss (Game Over) (09F7978C)](#trigger-09f7978c).
2. Jump the camera to waypoint 0 (cell 98, 172).
3. Play voice notification EVA_CriticalStrucureLost.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7286, Events line 7377, Actions line 7468.

<a id="trigger-0b155310"></a>

### 50. Einstein Audio 1 Play - 0B155310

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Asslt Sqd 1 Go (08962F40)](#trigger-08962f40).

Attached scope: 35 tagged map cells: (57, 93), (58, 93), (59, 93), (60, 93), (61, 93), (62, 93), (63, 93), (57, 94), (58, 94), (59, 94), (60, 94), (61, 94), (62, 94), (63, 94), (57, 95), (58, 95), (59, 95), (60, 95), (61, 95), (62, 95), (63, 95), (57, 96), (58, 96), (59, 96), (60, 96), (61, 96), (62, 96), (63, 96), (57, 97), (58, 97), (59, 97), (60, 97), (61, 97), (62, 97), (63, 97); tag 0B157D00, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Play voice notification Mis_A10_Einstein1.
2. Reveal terrain around waypoint 42 (cell 60, 95).
3. Create radar-event marker type 5 at waypoint 42 (cell 60, 95).
4. Set local flag 1 (Einstein Audio1).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7287, Events line 7378, Actions line 7469.

<a id="trigger-08962f40"></a>

### 51. Einstein Asslt Sqd 1 Go - 08962F40

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089A0800 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Einstein Assualt Squad 1 (09D6743C)](all10s-teams.md#team-09d6743c).
2. Enable and reset applicable timers for [Einstein Audio 1 Play (0B155310)](#trigger-0b155310).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7288, Events line 7379, Actions line 7470.

<a id="trigger-0bfba880"></a>

### 52. Einstein Asslt Sqd 2 Go - 0BFBA880

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BFBA370 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Einstein Audio1) is set.
2. 900 configured time units have elapsed since scenario start.

Flag writers in this mission: set local flag 1 (Einstein Audio1) at [Einstein Audio 1 Play (0B155310)](#trigger-0b155310). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Einstein Assualt Squad 2 (09D6C96C)](all10s-teams.md#team-09d6c96c).
2. Enable and reset applicable timers for [Einstein Audio 2 Play (0BFBBEB0)](#trigger-0bfbbeb0).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7289, Events line 7380, Actions line 7471.

<a id="trigger-0bfbbeb0"></a>

### 53. Einstein Audio 2 Play - 0BFBBEB0

Owner reference: Einstein. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Asslt Sqd 2 Go (0BFBA880)](#trigger-0bfba880).

Attached scope: 43 tagged map cells: (168, 106), (169, 106), (165, 107), (166, 107), (167, 107), (168, 107), (169, 107), (171, 107), (166, 108), (167, 108), (168, 108), (169, 108), (171, 108), (165, 109), (166, 109), (167, 109), (168, 109), (169, 109), (170, 109), (171, 109), (166, 110), (167, 110), (169, 110), (170, 110), (171, 110), (165, 111), (166, 111), (167, 111), (168, 111), (169, 111), (170, 111), (171, 111), (165, 112), (166, 112), (167, 112), (168, 112), (169, 112), (170, 112), (171, 112), (165, 113), (166, 113), (167, 113), (168, 113); tag 0BFBB700, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 17 (country/type BADGUY3; placed owner BadGuy3 House).

**Then perform these actions in order:**

1. Play voice notification Mis_A10_Einstein2.
2. Reveal terrain around waypoint 41 (cell 168, 110).
3. Create radar-event marker type 5 at waypoint 41 (cell 168, 110).
4. Set local flag 2 (Einstein Audio2).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7290, Events line 7381, Actions line 7472.

<a id="trigger-0bfbc710"></a>

### 54. Einstein Asslt Sqd 3 Go - 0BFBC710

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BFBC500 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Einstein Audio2) is set.
2. 1200 configured time units have elapsed since scenario start.

Flag writers in this mission: set local flag 2 (Einstein Audio2) at [Einstein Audio 2 Play (0BFBBEB0)](#trigger-0bfbbeb0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Einstein Assualt Squad 3 (09D6CEFC)](all10s-teams.md#team-09d6cefc).
2. Enable and reset applicable timers for [Einstein Audio 3 Play (0BFBC420)](#trigger-0bfbc420).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7291, Events line 7382, Actions line 7473.

<a id="trigger-0bfbc420"></a>

### 55. Einstein Audio 3 Play - 0BFBC420

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Asslt Sqd 3 Go (0BFBC710)](#trigger-0bfbc710).

Attached scope: 41 tagged map cells: (145, 145), (146, 145), (147, 145), (148, 145), (149, 145), (150, 145), (144, 146), (145, 146), (146, 146), (147, 146), (148, 146), (149, 146), (150, 146), (144, 147), (145, 147), (146, 147), (147, 147), (148, 147), (149, 147), (150, 147), (144, 148), (145, 148), (146, 148), (147, 148), (148, 148), (149, 148), (150, 148), (144, 149), (145, 149), (146, 149), (147, 149), (148, 149), (149, 149), (150, 149), (144, 150), (145, 150), (146, 150), (147, 150), (148, 150), (149, 150), (150, 150); tag 0BFBC090, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Play voice notification Mis_A10_Einstein3.
2. Create radar-event marker type 5 at waypoint 43 (cell 147, 148).
3. Reveal terrain around waypoint 43 (cell 147, 148).
4. Set local flag 3 (Einstein Audio3).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7292, Events line 7383, Actions line 7474.

<a id="trigger-0895ba00"></a>

### 56. Einstein Audio 4 Enable - 0895BA00

Owner reference: Einstein. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0895B400 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Einstein Audio2) is set.
2. local flag 3 (Einstein Audio3) is set.

Flag writers in this mission: set local flag 2 (Einstein Audio2) at [Einstein Audio 2 Play (0BFBBEB0)](#trigger-0bfbbeb0); set local flag 3 (Einstein Audio3) at [Einstein Audio 3 Play (0BFBC420)](#trigger-0bfbc420). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Entered by BG1 (0895B320)](#trigger-0895b320).
2. Enable and reset applicable timers for [Entered by BG2 (0895AD70)](#trigger-0895ad70).
3. Enable and reset applicable timers for [Entered by BG3 (0895A960)](#trigger-0895a960).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7293, Events line 7384, Actions line 7475.

<a id="trigger-0895b320"></a>

### 57. Entered by BG1 - 0895B320

Owner reference: Einstein. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Einstein Audio 4 Enable (0895BA00)](#trigger-0895ba00).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Play voice notification Mis_A10_Einstein4.
2. Create radar-event marker type 5 at waypoint 5 (cell 117, 169).
3. Reveal terrain around waypoint 5 (cell 117, 169).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7294, Events line 7385, Actions line 7476.

<a id="trigger-0895ad70"></a>

### 58. Entered by BG2 - 0895AD70

Owner reference: Einstein. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Entered by BG1 (0895B320)](#trigger-0895b320).

Incoming activation links: enable from [Einstein Audio 4 Enable (0895BA00)](#trigger-0895ba00).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Play voice notification Mis_A10_Einstein4.
2. Create radar-event marker type 5 at waypoint 5 (cell 117, 169).
3. Reveal terrain around waypoint 5 (cell 117, 169).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7295, Events line 7386, Actions line 7477.

<a id="trigger-0895a960"></a>

### 59. Entered by BG3 - 0895A960

Owner reference: Einstein. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Entered by BG2 (0895AD70)](#trigger-0895ad70).

Incoming activation links: enable from [Einstein Audio 4 Enable (0895BA00)](#trigger-0895ba00).

Attached scope: 35 tagged map cells: (115, 166), (116, 166), (117, 166), (118, 166), (119, 166), (120, 166), (116, 167), (117, 167), (118, 167), (119, 167), (120, 167), (115, 168), (116, 168), (117, 168), (118, 168), (119, 168), (120, 168), (115, 169), (116, 169), (117, 169), (118, 169), (119, 169), (120, 169), (115, 170), (116, 170), (117, 170), (118, 170), (119, 170), (120, 170), (115, 171), (116, 171), (117, 171), (118, 171), (119, 171), (120, 171); tag 0895AF50, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 17 (country/type BADGUY3; placed owner BadGuy3 House).

**Then perform these actions in order:**

1. Play voice notification Mis_A10_Einstein4.
2. Create radar-event marker type 5 at waypoint 5 (cell 117, 169).
3. Reveal terrain around waypoint 5 (cell 117, 169).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7296, Events line 7387, Actions line 7478.

<a id="trigger-0b17b1f0"></a>

### 60. Build SpySat Audio Play - 0B17B1F0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B17C740 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 6 (global list position: Allied Battle Lab (GATECH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Mis_A10_EvaSpySat.
2. Set local flag 4 (SpySat Audio Played).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7297, Events line 7388, Actions line 7479.

<a id="trigger-0b17c1f0"></a>

### 61. Build Purifier Audio Play - 0B17C1F0

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Purifier Audio (03D64400)](#trigger-03d64400).

Attached scope: tag definitions 0B17C120 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 14 (Purifier Exists) is clear.
2. The trigger owner's credits are below 2000.
3. 30 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 14 (Purifier Exists) at [Does Purifier Exist (0CF6E22C)](#trigger-0cf6e22c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_A10_EvaOrePurifier.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7298, Events line 7389, Actions line 7480.

<a id="trigger-03d64400"></a>

### 62. Enable Purifier Audio - 03D64400

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03D65040 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (SpySat Audio Played) is set.

Flag writers in this mission: set local flag 4 (SpySat Audio Played) at [Build SpySat Audio Play (0B17B1F0)](#trigger-0b17b1f0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Build Purifier Audio Play (0B17C1F0)](#trigger-0b17c1f0).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7299, Events line 7390, Actions line 7481.

<a id="trigger-03d7c6b0"></a>

### 63. Objective Statements - 03D7C6B0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03D63F50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 20 (country/type GERMANY3; placed owner German3 House).
2. Destroyed,  All: owner selector 19 (country/type GERMANY2; placed owner German2 House).
3. Destroyed,  All: owner selector 18 (country/type GERMANY1; placed owner German1 House).

**Then perform these actions in order:**

1. Display message “Objective 1: Defend Professor Einstein's” (MISSION:All10d1).
2. Display message “Laboratory” (MISSION:All10d2).
3. Display message “Objective 2: Destroy all Soviet invaders” (MISSION:All10e).
4. Play voice notification EVA_NewObjectiveReceived.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7300, Events line 7391, Actions line 7482.

<a id="trigger-0ac0456c"></a>

### 64. Play Cold Wind Sounds - 0AC0456C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AC0266C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 17 (cell 96, 95).
2. Play sound _Amb_WindCold at waypoint 45 (cell 36, 99).
3. Play sound _Amb_WindCold at waypoint 46 (cell 47, 78).
4. Play sound _Amb_WindCold at waypoint 47 (cell 171, 102).
5. Play sound _Amb_WindCold at waypoint 48 (cell 170, 132).
6. Play sound _Amb_WindCold at waypoint 98 (cell 114, 128).
7. Play sound _Amb_WindCold at waypoint 49 (cell 59, 74).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7301, Events line 7392, Actions line 7483.

<a id="trigger-0b5bd66c"></a>

### 65. Einstein Under Attk - 0B5BD66C

Owner reference: Einstein. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Power Plant (GAPOWR), owner Einstein House, cell (96, 176), tag 0B5BD58C, persistence mode 0; Power Plant (GAPOWR), owner Einstein House, cell (103, 176), tag 0B5BD58C, persistence mode 0; Pill Box (GAPILL), owner Einstein House, cell (106, 172), tag 0B5BD58C, persistence mode 0; Pill Box (GAPILL), owner Einstein House, cell (106, 177), tag 0B5BD58C, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “WARNING: Einstein's Laboratory is under attack” (MISSION:All10c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7302, Events line 7393, Actions line 7484.

<a id="trigger-0ae4646c"></a>

### 66. Apoc Sighted (timed) - 0AE4646C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Apoc Sighted (SpySat) (0A46CAF0)](#trigger-0a46caf0).

Attached scope: 38 tagged map cells: (107, 16), (108, 16), (109, 16), (110, 16), (107, 17), (108, 17), (110, 17), (111, 17), (107, 18), (108, 18), (109, 18), (110, 18), (111, 18), (112, 18), (107, 19), (108, 19), (109, 19), (110, 19), (111, 19), (112, 19), (113, 19), (107, 20), (108, 20), (109, 20), (110, 20), (111, 20), (112, 20), (113, 20), (114, 20), (107, 21), (108, 21), (109, 21), (110, 21), (111, 21), (112, 21), (113, 21), (114, 21), (115, 21); tag 0A46C6B0, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 16 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Jump the camera to waypoint 27 (cell 111, 19).
2. Create radar-event marker type 5 at waypoint 27 (cell 111, 19).
3. Flash team [First Apocalypse Sighting (0AD0D6CC)](all10s-teams.md#team-0ad0d6cc) with duration setting 30.
4. Play voice notification Unit_Eva_Apocalypse.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7303, Events line 7394, Actions line 7485.

<a id="trigger-0881557c"></a>

### 67. _0 Lock Input - 0881557C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 088111DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Disable player input.
2. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7304, Events line 7395, Actions line 7486.

<a id="trigger-0ae73f3c"></a>

### 68. Polar Bears - 0AE73F3C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Polar Bears Enable I (0A0F1D9C)](#trigger-0a0f1d9c); enable from [Polar Bears Enable II (0AB2E52C)](#trigger-0ab2e52c).

Attached scope: tag definitions 0AE739FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Polar Bears (0AD98B7C)](all10s-teams.md#team-0ad98b7c).
2. Play sound BearSelect at waypoint 52 (cell 23, 115).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7305, Events line 7396, Actions line 7487.

<a id="trigger-0ae79edc"></a>

### 69. Polar Bear Woman - 0AE79EDC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE79B3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (Polar Bears Gone) is set.

**Then perform these actions in order:**

1. Create/recruit team [Polar Bear Woman (0AE789FC)](all10s-teams.md#team-0ae789fc).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7306, Events line 7397, Actions line 7488.

<a id="trigger-0ae7debc"></a>

### 70. Polar Bear Woman Car - 0AE7DEBC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE7DCBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Woman in Car) is set.

**Then perform these actions in order:**

1. Create/recruit team [Polar Bear Woman Car (0ACF76CC)](all10s-teams.md#team-0acf76cc).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7307, Events line 7398, Actions line 7489.

<a id="trigger-0ae7d53c"></a>

### 71. Bear Crate Spawn 1 - 0AE7D53C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE7D3AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (Spawn Crate) is set.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 54 (cell 38, 131).
2. Play sound Bonus at waypoint 54 (cell 38, 131).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7308, Events line 7399, Actions line 7490.

<a id="trigger-0ae7d2bc"></a>

### 72. Bear Crate Spawn 2 - 0AE7D2BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE7BE2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 8 (Spawn Crate2) is set.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 55 (cell 42, 129).
2. Play sound Bonus at waypoint 55 (cell 42, 129).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7309, Events line 7400, Actions line 7491.

<a id="trigger-0ae7bd3c"></a>

### 73. Bear Crate Spawn 3 - 0AE7BD3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE7BB3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (Spawn Crate3) is set.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 56 (cell 51, 130).
2. Play sound Bonus at waypoint 56 (cell 51, 130).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7310, Events line 7401, Actions line 7492.

<a id="trigger-0ae7ba4c"></a>

### 74. Bear Crate Spawn 4 - 0AE7BA4C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE7B84C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Spawn Crate4) is set.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 57 (cell 52, 135).
2. Play sound Bonus at waypoint 57 (cell 52, 135).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7311, Events line 7402, Actions line 7493.

<a id="trigger-0ae7b75c"></a>

### 75. Bear Crate Spawn 5 - 0AE7B75C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE7B55C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 11 (Spawn Crate5) is set.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 58 (cell 55, 136).
2. Play sound Bonus at waypoint 58 (cell 55, 136).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7312, Events line 7403, Actions line 7494.

<a id="trigger-0ae7b46c"></a>

### 76. Bear Crate Spawn 6 - 0AE7B46C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE77E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 12 (Spawn Crate6) is set.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 59 (cell 64, 145).
2. Play sound Bonus at waypoint 59 (cell 64, 145).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7313, Events line 7404, Actions line 7495.

<a id="trigger-0ae71f3c"></a>

### 77. Bear Crate Spawn 7 - 0AE71F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE7591C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 13 (Spawn Crate7) is set.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 60 (cell 63, 153).
2. Play sound Bonus at waypoint 60 (cell 63, 153).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7314, Events line 7405, Actions line 7496.

<a id="trigger-0a0f1d9c"></a>

### 78. Polar Bears Enable I - 0A0F1D9C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Polar Bears (0AE73F3C)](#trigger-0ae73f3c).
2. Play sound BearSelect at waypoint 52 (cell 23, 115).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7315, Events line 7406, Actions line 7497.

<a id="trigger-0aae8dcc"></a>

### 79. Reclaimed Refinery - 0AAE8DCC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Ore Refinery (GAREFN), owner Civilian House, cell (178, 128), tag 0AAEA9EC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 14 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Change House: owner selector 14 (country/type PLAYER; placed owner Player House).
2. Create crate type 1 at waypoint 63 (cell 181, 126).
3. Play sound Bonus at waypoint 63 (cell 181, 126).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7316, Events line 7407, Actions line 7498.

<a id="trigger-0ab2e52c"></a>

### 80. Polar Bears Enable II - 0AB2E52C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Polar Bears Enable I (0A0F1D9C)](#trigger-0a0f1d9c).

Attached scope: tag definitions 0A0F475C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Polar Bears (0AE73F3C)](#trigger-0ae73f3c).
2. Play sound BearSelect at waypoint 52 (cell 23, 115).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7317, Events line 7408, Actions line 7499.

<a id="trigger-0c701bbc"></a>

### 81. Chrono Power Off - 0C701BBC

Owner reference: Einstein. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C7016DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Set the attached building offline.

Source locator: MAPS01.MIX/all10s.map; Triggers line 7318, Events line 7409, Actions line 7500.

<a id="trigger-08b3cf3c"></a>

### 82. Crate at BM - 08B3CF3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (54, 148); tag 08B3A1BC, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 64 (cell 54, 148).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7319, Events line 7410, Actions line 7501.

<a id="trigger-0b02e3ec"></a>

### 83. BG1 Babysitters Spawn - 0B02E3EC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B02FD9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 Baby Sitters (0B02B25C)](all10s-teams.md#team-0b02b25c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7320, Events line 7411, Actions line 7502.

<a id="trigger-0b02fcac"></a>

### 84. BG2 Babysitters Spawn - 0B02FCAC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B02F90C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 Baby Sitters (0B02EEFC)](all10s-teams.md#team-0b02eefc).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7321, Events line 7412, Actions line 7503.

<a id="trigger-0b02f81c"></a>

### 85. BG3 Babysitters Spawn - 0B02F81C

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B02F44C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [BG3 Baby Sitters (0B02EDCC)](all10s-teams.md#team-0b02edcc).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7322, Events line 7413, Actions line 7504.

<a id="trigger-0cf6e22c"></a>

### 86. Does Purifier Exist - 0CF6E22C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CF6FD6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 73 (global list position: Ore Purifier (GAOREP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 14 (Purifier Exists).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7323, Events line 7414, Actions line 7505.

<a id="trigger-0ad3822c"></a>

### 87. Kill BG1 Local Guy - 0AD3822C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BG1 Production Start (08DC9190)](#trigger-08dc9190).

Attached scope: Conscript (E2), owner BadGuy1 House, cell (80, 30), tag 08DC9680, persistence mode 0.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Enable and reset applicable timers for [BG1 Firesale Enabler (0AC09D2C)](#trigger-0ac09d2c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7324, Events line 7415, Actions line 7506.

<a id="trigger-0ad3ebbc"></a>

### 88. Kill BG2 Local Guy - 0AD3EBBC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BG2 Production Start (08DC95C0)](#trigger-08dc95c0).

Attached scope: Conscript (E2), owner BadGuy2 House, cell (111, 12), tag 08DCAA20, persistence mode 0.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Enable and reset applicable timers for [BG2 Firesale Enabler (0AC0326C)](#trigger-0ac0326c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7325, Events line 7416, Actions line 7507.

<a id="trigger-0ad3e9ac"></a>

### 89. Kill BG3 Local Guy - 0AD3E9AC

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BG3 Production Start (08DCA960)](#trigger-08dca960).

Attached scope: Conscript (E2), owner BadGuy3 House, cell (170, 71), tag 08DCA5D0, persistence mode 0.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Enable and reset applicable timers for [BG3 Firesale Enabler (0AC0044C)](#trigger-0ac0044c).

Source locator: MAPS01.MIX/all10s.map; Triggers line 7326, Events line 7417, Actions line 7508.

[All team rosters and ordered plans](all10s-teams.md) | [All mission overrides](all10s-overrides.md)
