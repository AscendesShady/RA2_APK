# Operation: Free Gateway

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for all08u.map.](../../images/map-all08u.svg)

*Initial placement schematic for all08u.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** all08u.map. **Effective extracted member:** MAPS01.MIX/all08u.map. **Trigger definitions:** 109.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all08u-teams.md) | [All mission overrides](all08u-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | URBAN |
| Map size | 0,0,80,80 |
| Visible local rectangle | 5,5,70,69 |
| Placed vehicles | 4 |
| Placed infantry | 66 |
| Placed structures | 138 |
| Placed aircraft | 0 |
| Team templates | 64 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 20 | Player |
| 1 | BadGuy1 House | 400 | BadGuy1 |
| 2 | BadGuy2 House | 200 | BadGuy2 |
| 3 | Evil House | 0 | Evil |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | TanyaLand House | 0 | TanyaLand |
| 6 | GILand House | 0 | GILand |
| 7 | EngineerLand House | 0 | EngineerLand |
| 8 | House Elania | 0 | Elania |
| 9 | Reinforcers House | 0 | Reinforcers |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Tanya Converted,0 |
| 1 | Reinforcments Arriv,0 |
| 2 | Beacon Destroyed,0 |
| 3 | Engineers Evil,0 |
| 4 | GIs Evil,0 |
| 5 | GIs KIA,0 |
| 6 | Engineers KIA,0 |
| 7 | Refinery Reclaimed,0 |
| 8 | War Factory Reclaim,0 |
| 9 | Desolator Gooing,0 |
| 10 | Prism 1 Unloaded,0 |
| 11 | Prism 2 Unloaded,0 |
| 12 | Engineer Fix,0 |
| 13 | Evil Armor Redempti,0 |
| 14 | Goto AW,0 |
| 15 | 3 Unloaded,0 |
| 16 | 4 Unloaded,0 |
| 17 | 5e1 Unloaded,0 |
| 18 | 5e2 Unloaded,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [_Loss Game Over (0A0641FC)](#trigger-0a0641fc) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [_Loss (Tanya Movie Over) (0B8A82CC)](#trigger-0b8a82cc) | 93 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [_Win Game Over (0A0661FC)](#trigger-0a0661fc) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-07a3b77c"></a>

### 1. Player Start Force Go - 07A3B77C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A3B23C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Player Start Force (0A99211C)](all08u-teams.md#team-0a99211c).
2. Reveal terrain around waypoint 1 (cell 90, 27).
3. Disable player input.
4. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5731, Events line 5842, Actions line 5953.

<a id="trigger-08d59f3c"></a>

### 2. Each to His Own House - 08D59F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D5987C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 27 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [GILanders (09B81684)](all08u-teams.md#team-09b81684).
2. Create/recruit team [TanyaLanders (09B80694)](all08u-teams.md#team-09b80694).
3. Create/recruit team [EngineerLanders (0AC59B7C)](all08u-teams.md#team-0ac59b7c).
4. Set the mission timer to 1200 configured time units.
5. Start the visible mission timer.
6. Use countdown label “Time until Beacon affects Tanya:” (MISSION:All08T).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5732, Events line 5843, Actions line 5954.

<a id="trigger-09c3c9bc"></a>

### 3. _Loss (Tanya KIA) - 09C3C9BC

Owner reference: TanyaLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [_Loss (Player KIA) (07BB9A0C)](#trigger-07bb9a0c).

Incoming activation links: enable from [_Loss (Tanya KIA) enabled (08DBCF3C)](#trigger-08dbcf3c).

Attached scope: tag definitions 07BB9AFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 18 (country/type TANYALAND; placed owner TanyaLand House).
2. local flag 0 (Tanya Converted) is clear.

Flag writers in this mission: set local flag 0 (Tanya Converted) at [Tanya Go Evil (0B8A96EC)](#trigger-0b8a96ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss Game Over (0A0641FC)](#trigger-0a0641fc).
2. Play voice notification Mis_A1_EvaTanyaDeath.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5733, Events line 5844, Actions line 5955.

<a id="trigger-07bb9a0c"></a>

### 4. _Loss (Player KIA) - 07BB9A0C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [_Loss (Tanya Converted) (07BBC47C)](#trigger-07bbc47c).

Incoming activation links: enable from [_Loss (player KIA) enabled (07BBC1AC)](#trigger-07bbc1ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 18 (country/type TANYALAND; placed owner TanyaLand House).
2. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss Game Over (0A0641FC)](#trigger-0a0641fc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5734, Events line 5845, Actions line 5956.

<a id="trigger-0a0641fc"></a>

### 5. _Loss Game Over - 0A0641FC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Loss (Tanya KIA) (09C3C9BC)](#trigger-09c3c9bc); enable from [_Loss (Player KIA) (07BB9A0C)](#trigger-07bb9a0c).

Attached scope: tag definitions 0A06320C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5735, Events line 5846, Actions line 5957.

<a id="trigger-07bbc47c"></a>

### 6. _Loss (Tanya Converted) - 07BBC47C

Owner reference: TanyaLand. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 0 (Tanya Converted) is set.

Flag writers in this mission: set local flag 0 (Tanya Converted) at [Tanya Go Evil (0B8A96EC)](#trigger-0b8a96ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss (Tanya Movie) (07BB974C)](#trigger-07bb974c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5736, Events line 5847, Actions line 5958.

<a id="trigger-07bb974c"></a>

### 7. _Loss (Tanya Movie) - 07BB974C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Loss (Tanya Converted) (07BBC47C)](#trigger-07bbc47c).

Attached scope: tag definitions 07BB935C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 72.
2. Enable and reset applicable timers for [_Loss (Tanya Movie Over) (0B8A82CC)](#trigger-0b8a82cc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5737, Events line 5848, Actions line 5959.

<a id="trigger-0b8a82cc"></a>

### 8. _Loss (Tanya Movie Over) - 0B8A82CC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Loss (Tanya Movie) (07BB974C)](#trigger-07bb974c).

Attached scope: tag definitions 0B8AAF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 93 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reshroud Map; main setting 0.
2. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5738, Events line 5849, Actions line 5960.

<a id="trigger-07bb91bc"></a>

### 9. Psychic Beacon KIA - 07BB91BC

Owner reference: Evil. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 2 (Beacon Destroyed).
2. Enable and reset applicable timers for [Player Reinforcements Go (0B89FCFC)](#trigger-0b89fcfc).
3. Display message “Objective 1 Accomplished” (MISSION:All09c).
4. Stop the visible mission timer.
5. Play voice notification EVA_PrimaryObjectiveAchieved.
6. Disable [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc).
7. Disable [Psychic Beacon Captured (08511C5C)](#trigger-08511c5c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5739, Events line 5850, Actions line 5961.

<a id="trigger-0b89fcfc"></a>

### 10. Player Reinforcements Go - 0B89FCFC

Owner reference: Reinforcers. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); enable from [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc).

Attached scope: tag definitions 0B8A0BFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Player Reinforcements 1 (0CE11DEC)](all08u-teams.md#team-0ce11dec).
2. Create radar-event marker type 2 at waypoint 5 (cell 148, 81).
3. Reveal terrain around waypoint 5 (cell 148, 81).
4. Supply reinforcement team [Player Reinforcements 2 (0CE10DEC)](all08u-teams.md#team-0ce10dec).
5. Supply reinforcement team [Player Reinforcements 3 (0CE1093C)](all08u-teams.md#team-0ce1093c).
6. Supply reinforcement team [Player Reinforcements 4 (0CE1048C)](all08u-teams.md#team-0ce1048c).
7. Create crate type 0 at waypoint 21 (cell 103, 80).
8. Display message “Objective 2: Drive all Soviet forces out” (MISSION:All08b1).
9. Display message “of St. Louis” (MISSION:All08b2).
10. Play sound Bonus at waypoint 21 (cell 103, 80).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5740, Events line 5851, Actions line 5962.

<a id="trigger-08511c5c"></a>

### 11. Psychic Beacon Captured - 08511C5C

Owner reference: Evil. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc).
2. Disable [Psychic Beacon Captured (08511C5C)](#trigger-08511c5c).
3. Disable [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5741, Events line 5852, Actions line 5963.

<a id="trigger-0cf745dc"></a>

### 12. Psychic Beacon Change House - 0CF745DC

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Psychic Beacon Captured (08511C5C)](#trigger-08511c5c).

Incoming activation links: enable from [Psychic Beacon Captured (08511C5C)](#trigger-08511c5c).

Attached scope: Psychic Beacon (NAPSYB), owner BadGuy2 House, cell (47, 100), tag 07BBBBEC, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Sell the attached building through the scripted sale action.
3. Set local flag 2 (Beacon Destroyed).
4. Enable and reset applicable timers for [Player Reinforcements Go (0B89FCFC)](#trigger-0b89fcfc).
5. Display message “Objective 1 Accomplished” (MISSION:All09c).
6. Stop the visible mission timer.
7. Play voice notification EVA_PrimaryObjectiveAchieved.
8. Disable [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5742, Events line 5853, Actions line 5964.

<a id="trigger-0aeeb75c"></a>

### 13. Play Reinforcements Arrived - 0AEEB75C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AEEB16C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Reinforcments Arriv) is set.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5743, Events line 5854, Actions line 5965.

<a id="trigger-075a9adc"></a>

### 14. Prism Tank Movie Play - 075A9ADC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Prism Flashers Enable (0D2533DC)](#trigger-0d2533dc).

Attached scope: tag definitions 075A96BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 4 (cell 114, 80) with speed setting 4.
2. Create/recruit team [Prism Flashers! (0A2BD7DC)](all08u-teams.md#team-0a2bd7dc).
3. Play in-game movie 99.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5744, Events line 5855, Actions line 5966.

<a id="trigger-07bbc1ac"></a>

### 15. _Loss (player KIA) enabled - 07BBC1AC

Owner reference: TanyaLand. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B89FF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Reinforcments Arriv) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss (Player KIA) (07BB9A0C)](#trigger-07bb9a0c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5745, Events line 5856, Actions line 5967.

<a id="trigger-0b89fe5c"></a>

### 16. GI Back to Player - 0B89FE5C

Owner reference: GILand. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B89E35C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Reinforcments Arriv) is set.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5746, Events line 5857, Actions line 5968.

<a id="trigger-079f9aec"></a>

### 17. Engineers Back to Player - 079F9AEC

Owner reference: EngineerLand. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07BB87DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Reinforcments Arriv) is set.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5747, Events line 5858, Actions line 5969.

<a id="trigger-0b8a09ac"></a>

### 18. Evil Redeemed 1 - 0B8A09AC

Owner reference: Evil. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Engineers Evil) is set.
2. local flag 4 (GIs Evil) is set.
3. local flag 2 (Beacon Destroyed) is set.

Flag writers in this mission: set local flag 3 (Engineers Evil) at [Engineers Go Evil (0B8A848C)](#trigger-0b8a848c); set local flag 4 (GIs Evil) at [GIs go Evil (0B8A9B6C)](#trigger-0b8a9b6c); set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Enable and reset applicable timers for [Cons & Techs Redeemed (09ABB17C)](#trigger-09abb17c).
3. Play voice notification Mis_A8_AllSoldierFreed.
4. Enable and reset applicable timers for [Techs Goto Arch Start (0BE8EE3C)](#trigger-0be8ee3c).
5. Enable and reset applicable timers for [Techs Goto Arch End (09366E6C)](#trigger-09366e6c).
6. Enable and reset applicable timers for [Engineerland Revert to Player (082E3C9C)](#trigger-082e3c9c).
7. Enable and reset applicable timers for [Evil Armor 2 Redemption (0D2A2A0C)](#trigger-0d2a2a0c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5748, Events line 5859, Actions line 5970.

<a id="trigger-09abb17c"></a>

### 19. Cons & Techs Redeemed - 09ABB17C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil Redeemed 1 (0B8A09AC)](#trigger-0b8a09ac); enable from [Evil Redeemed 2 (08FC4564)](#trigger-08fc4564); enable from [Evil Redeemed 3 (08FC3834)](#trigger-08fc3834); enable from [Evil Redeemed 4 (08FC3374)](#trigger-08fc3374).

Attached scope: tag definitions 09AB9DEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Play voice notification Mis_S3_UnYuriedCiv.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5749, Events line 5860, Actions line 5971.

<a id="trigger-0be8ee3c"></a>

### 20. Techs Goto Arch Start - 0BE8EE3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil Redeemed 1 (0B8A09AC)](#trigger-0b8a09ac); enable from [Evil Redeemed 2 (08FC4564)](#trigger-08fc4564); enable from [Evil Redeemed 3 (08FC3834)](#trigger-08fc3834); enable from [Evil Redeemed 4 (08FC3374)](#trigger-08fc3374).

Attached scope: tag definitions 0BE8E4FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Techs Goto Arch (0BE8B86C)](all08u-teams.md#team-0be8b86c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5750, Events line 5861, Actions line 5972.

<a id="trigger-09366e6c"></a>

### 21. Techs Goto Arch End - 09366E6C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil Redeemed 1 (0B8A09AC)](#trigger-0b8a09ac); enable from [Evil Redeemed 2 (08FC4564)](#trigger-08fc4564); enable from [Evil Redeemed 3 (08FC3834)](#trigger-08fc3834); enable from [Evil Redeemed 4 (08FC3374)](#trigger-08fc3374).

Attached scope: tag definitions 093668DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 21 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Techs Goto Arch Start (0BE8EE3C)](#trigger-0be8ee3c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5751, Events line 5862, Actions line 5973.

<a id="trigger-082e3c9c"></a>

### 22. Engineerland Revert to Player - 082E3C9C

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil Redeemed 1 (0B8A09AC)](#trigger-0b8a09ac); enable from [Evil Redeemed 2 (08FC4564)](#trigger-08fc4564); enable from [Evil Redeemed 3 (08FC3834)](#trigger-08fc3834); enable from [Evil Redeemed 4 (08FC3374)](#trigger-08fc3374).

Attached scope: tag definitions 082E373C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5752, Events line 5863, Actions line 5974.

<a id="trigger-0d2a2a0c"></a>

### 23. Evil Armor 2 Redemption - 0D2A2A0C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil Redeemed 1 (0B8A09AC)](#trigger-0b8a09ac); enable from [Evil Redeemed 2 (08FC4564)](#trigger-08fc4564); enable from [Evil Redeemed 3 (08FC3834)](#trigger-08fc3834); enable from [Evil Redeemed 4 (08FC3374)](#trigger-08fc3374).

Attached scope: tag definitions 0D2A0AFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Evil Armor 2 Redemption (0CF25A4C)](all08u-teams.md#team-0cf25a4c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5753, Events line 5864, Actions line 5975.

<a id="trigger-0b8a848c"></a>

### 24. Engineers Go Evil - 0B8A848C

Owner reference: EngineerLand. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B8A9C5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Engineers KIA) is clear.
2. local flag 2 (Beacon Destroyed) is clear.
3. 900 configured time units have elapsed since scenario start.

Flag writers in this mission: set local flag 6 (Engineers KIA) at [Engineers KIA (08FC2D34)](#trigger-08fc2d34); set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 16 (country/type EVIL; placed owner Evil House).
2. Play voice notification Mis_A8_AllSoldierTurned.
3. Set local flag 3 (Engineers Evil).
4. Display message “WARNING: The Psychic Beacon has affected” (MISSION:All08d1).
5. Display message “your team” (MISSION:All08d2).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5754, Events line 5865, Actions line 5976.

<a id="trigger-0b8a9b6c"></a>

### 25. GIs go Evil - 0B8A9B6C

Owner reference: GILand. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B8A98BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (GIs KIA) is clear.
2. local flag 2 (Beacon Destroyed) is clear.
3. 1080 configured time units have elapsed since scenario start.

Flag writers in this mission: set local flag 5 (GIs KIA) at [GIs KIA (08FC3104)](#trigger-08fc3104); set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 16 (country/type EVIL; placed owner Evil House).
2. Play voice notification Mis_A8_AllSoldierTurned.
3. Set local flag 4 (GIs Evil).
4. Display message “WARNING: The Psychic Beacon has affected” (MISSION:All08d1).
5. Display message “your team” (MISSION:All08d2).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5755, Events line 5866, Actions line 5977.

<a id="trigger-0b8a96ec"></a>

### 26. Tanya Go Evil - 0B8A96EC

Owner reference: TanyaLand. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B8A93CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Beacon Destroyed) is clear.
2. The visible mission countdown has expired.

Flag writers in this mission: set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Set local flag 0 (Tanya Converted).
2. Disable [_Loss (Tanya KIA) (09C3C9BC)](#trigger-09c3c9bc).
3. Create/recruit team [Tanya Converted (08352E1C)](all08u-teams.md#team-08352e1c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5756, Events line 5867, Actions line 5978.

<a id="trigger-08d4b9ec"></a>

### 27. BG2 Bldgs KIA - 08D4B9EC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D4B78C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [2x Check BG2 is Hunting (0D4CAB7C)](#trigger-0d4cab7c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5757, Events line 5868, Actions line 5979.

<a id="trigger-0d4cab7c"></a>

### 28. 2x Check BG2 is Hunting - 0D4CAB7C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG2 Bldgs KIA (08D4B9EC)](#trigger-08d4b9ec).

Attached scope: tag definitions 0D4CA63C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5758, Events line 5869, Actions line 5980.

<a id="trigger-08d4b69c"></a>

### 29. BG1 Bldgs KIA - 08D4B69C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D4B49C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5759, Events line 5870, Actions line 5981.

<a id="trigger-08dbcf3c"></a>

### 30. _Loss (Tanya KIA) enabled - 08DBCF3C

Owner reference: TanyaLand. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DBCA5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss (Tanya KIA) (09C3C9BC)](#trigger-09c3c9bc).
2. Enable and reset applicable timers for [GIs KIA (08FC3104)](#trigger-08fc3104).
3. Enable and reset applicable timers for [Engineers KIA (08FC2D34)](#trigger-08fc2d34).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5760, Events line 5871, Actions line 5982.

<a id="trigger-08fc3104"></a>

### 31. GIs KIA - 08FC3104

Owner reference: GILand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Loss (Tanya KIA) enabled (08DBCF3C)](#trigger-08dbcf3c).

Attached scope: tag definitions 08FC2744 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 19 (country/type GILAND; placed owner GILand House).

**Then perform these actions in order:**

1. Set local flag 5 (GIs KIA).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5761, Events line 5872, Actions line 5983.

<a id="trigger-08fc2d34"></a>

### 32. Engineers KIA - 08FC2D34

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Loss (Tanya KIA) enabled (08DBCF3C)](#trigger-08dbcf3c).

Attached scope: tag definitions 08FC3204 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Set local flag 6 (Engineers KIA).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5762, Events line 5873, Actions line 5984.

<a id="trigger-09af2ccc"></a>

### 33. GIs Are Evil - 09AF2CCC

Owner reference: Evil. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09AF26AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (GIs Evil) is set.

Flag writers in this mission: set local flag 4 (GIs Evil) at [GIs go Evil (0B8A9B6C)](#trigger-0b8a9b6c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All to Hunt: owner selector 16 (country/type EVIL; placed owner Evil House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5763, Events line 5874, Actions line 5985.

<a id="trigger-09af25bc"></a>

### 34. Engineers Are Evil - 09AF25BC

Owner reference: Evil. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09AF0F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Engineers Evil) is set.

Flag writers in this mission: set local flag 3 (Engineers Evil) at [Engineers Go Evil (0B8A848C)](#trigger-0b8a848c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All to Hunt: owner selector 16 (country/type EVIL; placed owner Evil House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5764, Events line 5875, Actions line 5986.

<a id="trigger-09ab895c"></a>

### 35. BG Patrols Start (Hard) - 09AB895C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Beacon Perimeter Patrol (081104F4)](all08u-teams.md#team-081104f4).
2. Supply reinforcement team [Evil Patrol 1 (0B996384)](all08u-teams.md#team-0b996384).
3. Supply reinforcement team [Evil Patrol 2 (08F73AF4)](all08u-teams.md#team-08f73af4).
4. Supply reinforcement team [Evil Patrol 3 (07A458C4)](all08u-teams.md#team-07a458c4).
5. Supply reinforcement team [Evil Armor 1 (08DA8F04)](all08u-teams.md#team-08da8f04).
6. Supply reinforcement team [Evil Armor 2 (0A632EFC)](all08u-teams.md#team-0a632efc).
7. Supply reinforcement team [Terror On Patrol (0C1B17B4)](all08u-teams.md#team-0c1b17b4).
8. Supply reinforcement team [POW Patrol 1 (0A300CBC)](all08u-teams.md#team-0a300cbc).
9. Supply reinforcement team [POW Patrol 2 (0AF7132C)](all08u-teams.md#team-0af7132c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5765, Events line 5876, Actions line 5987.

<a id="trigger-08fc4564"></a>

### 36. Evil Redeemed 2 - 08FC4564

Owner reference: Evil. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Evil Redeemed 1 (0B8A09AC)](#trigger-0b8a09ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 6 (Engineers KIA) is set.
2. local flag 4 (GIs Evil) is set.
3. local flag 2 (Beacon Destroyed) is set.

Flag writers in this mission: set local flag 6 (Engineers KIA) at [Engineers KIA (08FC2D34)](#trigger-08fc2d34); set local flag 4 (GIs Evil) at [GIs go Evil (0B8A9B6C)](#trigger-0b8a9b6c); set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Enable and reset applicable timers for [Cons & Techs Redeemed (09ABB17C)](#trigger-09abb17c).
3. Play voice notification Mis_A8_AllSoldierFreed.
4. Enable and reset applicable timers for [Techs Goto Arch Start (0BE8EE3C)](#trigger-0be8ee3c).
5. Enable and reset applicable timers for [Techs Goto Arch End (09366E6C)](#trigger-09366e6c).
6. Enable and reset applicable timers for [Engineerland Revert to Player (082E3C9C)](#trigger-082e3c9c).
7. Enable and reset applicable timers for [Evil Armor 2 Redemption (0D2A2A0C)](#trigger-0d2a2a0c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5766, Events line 5877, Actions line 5988.

<a id="trigger-08fc3834"></a>

### 37. Evil Redeemed 3 - 08FC3834

Owner reference: Evil. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Evil Redeemed 2 (08FC4564)](#trigger-08fc4564).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (Engineers Evil) is set.
2. local flag 5 (GIs KIA) is set.
3. local flag 2 (Beacon Destroyed) is set.

Flag writers in this mission: set local flag 3 (Engineers Evil) at [Engineers Go Evil (0B8A848C)](#trigger-0b8a848c); set local flag 5 (GIs KIA) at [GIs KIA (08FC3104)](#trigger-08fc3104); set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Enable and reset applicable timers for [Cons & Techs Redeemed (09ABB17C)](#trigger-09abb17c).
3. Play voice notification Mis_A8_AllSoldierFreed.
4. Enable and reset applicable timers for [Techs Goto Arch Start (0BE8EE3C)](#trigger-0be8ee3c).
5. Enable and reset applicable timers for [Techs Goto Arch End (09366E6C)](#trigger-09366e6c).
6. Enable and reset applicable timers for [Engineerland Revert to Player (082E3C9C)](#trigger-082e3c9c).
7. Enable and reset applicable timers for [Evil Armor 2 Redemption (0D2A2A0C)](#trigger-0d2a2a0c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5767, Events line 5878, Actions line 5989.

<a id="trigger-08fc3374"></a>

### 38. Evil Redeemed 4 - 08FC3374

Owner reference: Evil. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Evil Redeemed 3 (08FC3834)](#trigger-08fc3834).

Attached scope: tag definitions 0B8A047C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Engineers KIA) is set.
2. local flag 5 (GIs KIA) is set.
3. local flag 2 (Beacon Destroyed) is set.

Flag writers in this mission: set local flag 6 (Engineers KIA) at [Engineers KIA (08FC2D34)](#trigger-08fc2d34); set local flag 5 (GIs KIA) at [GIs KIA (08FC3104)](#trigger-08fc3104); set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Enable and reset applicable timers for [Cons & Techs Redeemed (09ABB17C)](#trigger-09abb17c).
3. Enable and reset applicable timers for [Techs Goto Arch Start (0BE8EE3C)](#trigger-0be8ee3c).
4. Enable and reset applicable timers for [Techs Goto Arch End (09366E6C)](#trigger-09366e6c).
5. Enable and reset applicable timers for [Engineerland Revert to Player (082E3C9C)](#trigger-082e3c9c).
6. Enable and reset applicable timers for [Evil Armor 2 Redemption (0D2A2A0C)](#trigger-0d2a2a0c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5768, Events line 5879, Actions line 5990.

<a id="trigger-07aefa84"></a>

### 39. Reclaimed Refinery (Engineerland) - 07AEFA84

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Set local flag 7 (Refinery Reclaimed).
2. Enable and reset applicable timers for [Change House Refinery (Engineerland) (0ABE07DC)](#trigger-0abe07dc).
3. Disable [Reclaimed Refinery (Engineerland) (07AEFA84)](#trigger-07aefa84).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5769, Events line 5880, Actions line 5991.

<a id="trigger-0abe07dc"></a>

### 40. Change House Refinery (Engineerland) - 0ABE07DC

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Refinery (Engineerland) (07AEFA84)](#trigger-07aefa84).

Incoming activation links: enable from [Reclaimed Refinery (Engineerland) (07AEFA84)](#trigger-07aefa84).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Refinery (Engineerland) (0ABE07DC)](#trigger-0abe07dc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5770, Events line 5881, Actions line 5992.

<a id="trigger-08cd3194"></a>

### 41. Reclaimed War Factory (Engineerland) - 08CD3194

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Set local flag 8 (War Factory Reclaim).
2. Enable and reset applicable timers for [Change House War Factory (Engineerland) (0ABE8C3C)](#trigger-0abe8c3c).
3. Disable [Reclaimed War Factory (Engineerland) (08CD3194)](#trigger-08cd3194).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5771, Events line 5882, Actions line 5993.

<a id="trigger-0abe8c3c"></a>

### 42. Change House War Factory (Engineerland) - 0ABE8C3C

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed War Factory (Engineerland) (08CD3194)](#trigger-08cd3194).

Incoming activation links: enable from [Reclaimed War Factory (Engineerland) (08CD3194)](#trigger-08cd3194); enable from [Reclaimed War Factory (Player) (087D4AEC)](#trigger-087d4aec).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House War Factory (Engineerland) (0ABE8C3C)](#trigger-0abe8c3c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5772, Events line 5883, Actions line 5994.

<a id="trigger-0bdea2c4"></a>

### 43. Send Desolators - 0BDEA2C4

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BDEB944 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Prism 1 Unloaded) is set.
2. local flag 11 (Prism 2 Unloaded) is set.

**Then perform these actions in order:**

1. Create/recruit team [1st Desolator Usage (0C48359C)](all08u-teams.md#team-0c48359c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5773, Events line 5884, Actions line 5995.

<a id="trigger-077f3084"></a>

### 44. BG2 Production Begin - 077F3084

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 077F4514 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 52 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
2. AI triggers begin: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
3. Make enemy: owner selector 18 (country/type TANYALAND; placed owner TanyaLand House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5774, Events line 5885, Actions line 5996.

<a id="trigger-077f4414"></a>

### 45. BG1 Production Begin - 077F4414

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 077F5F44 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 150 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. Make enemy: owner selector 18 (country/type TANYALAND; placed owner TanyaLand House).
3. Create/recruit team [Def_GI (0BDEF684)](all08u-teams.md#team-0bdef684).
4. Create/recruit team [Def_IFV (0BDEDA74)](all08u-teams.md#team-0bdeda74).
5. Create/recruit team [Def_Spy (0BE84804)](all08u-teams.md#team-0be84804).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5775, Events line 5886, Actions line 5997.

<a id="trigger-08d39954"></a>

### 46. Reveal Beacon - 08D39954

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D39214 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 0 (cell 47, 100).
2. Display message “Objective 1: Capture or Destroy the” (MISSION:All08a1).
3. Create radar-event marker type 5 at waypoint 0 (cell 47, 100).
4. Reveal terrain around waypoint 38 (cell 47, 105).
5. Reveal terrain around waypoint 37 (cell 48, 96).
6. Move the camera to waypoint 0 (cell 47, 100) with speed setting 4.
7. Enable and reset applicable timers for [Camera Back to Paratroops (0D0BB03C)](#trigger-0d0bb03c).
8. Display message “Psychic Beacon before it affects your team” (MISSION:All08a2).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5776, Events line 5887, Actions line 5998.

<a id="trigger-0d0bb03c"></a>

### 47. Camera Back to Paratroops - 0D0BB03C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reveal Beacon (08D39954)](#trigger-08d39954).

Attached scope: tag definitions 0D3B892C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 13 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 1 (cell 90, 27) with speed setting 4.
2. Enable player input.
3. Display message “--Battle Control Online--” (MISSION:ALL01q).
4. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5777, Events line 5888, Actions line 5999.

<a id="trigger-0a28a3f4"></a>

### 48. 2x Check on BG2 - 0A28A3F4

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A28BE44 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [2x Check on BG2 (0A287514)](all08u-teams.md#team-0a287514).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5778, Events line 5889, Actions line 6000.

<a id="trigger-0a1d7e04"></a>

### 49. Harrassment Teams - 0A1D7E04

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A1D77A4 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Harrassment Team (09D7F8D4)](all08u-teams.md#team-09d7f8d4).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5779, Events line 5890, Actions line 6001.

<a id="trigger-079d0b74"></a>

### 50. BG1 Hates Player - 079D0B74

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079D3534 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Beacon Destroyed) is set.

Flag writers in this mission: set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5780, Events line 5891, Actions line 6002.

<a id="trigger-0963903c"></a>

### 51. _Win Occurred - 0963903C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0963703C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. Destroyed,  All: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Win Game Over (0A0661FC)](#trigger-0a0661fc).
2. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).
3. Make side cheer: owner selector 18 (country/type TANYALAND; placed owner TanyaLand House).
4. Make side cheer: owner selector 17 (country/type CIVILIAN1; placed owner Civie1 House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5781, Events line 5892, Actions line 6003.

<a id="trigger-0a0661fc"></a>

### 52. _Win Game Over - 0A0661FC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Win Occurred (0963903C)](#trigger-0963903c).

Attached scope: tag definitions 0A06115C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5782, Events line 5893, Actions line 6004.

<a id="trigger-09b9297c"></a>

### 53. Desolator Gooing - 09B9297C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09BDA90C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (Desolator Gooing) is set.

**Then perform these actions in order:**

1. Create radar-event marker type 0 at waypoint 20 (cell 71, 80).
2. Reveal terrain around waypoint 20 (cell 71, 80).
3. Flash team [1st Desolator Usage (0C48359C)](all08u-teams.md#team-0c48359c) with duration setting 30.
4. Move the camera to waypoint 20 (cell 71, 80) with speed setting 4.
5. Enable and reset applicable timers for [Desolator Description (0D9C1F3C)](#trigger-0d9c1f3c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5783, Events line 5894, Actions line 6005.

<a id="trigger-0d9c1f3c"></a>

### 54. Desolator Description - 0D9C1F3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Desolator Gooing (09B9297C)](#trigger-09b9297c).

Attached scope: tag definitions 0D9C783C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Eva_Desolator.
2. Display message “WARNING: Soviet Desolators have irradiated” (MISSION:All08c1).
3. Display message “the ground at this location” (MISSION:All08c2).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5784, Events line 5895, Actions line 6006.

<a id="trigger-03e6423c"></a>

### 55. Play Shore Sounds - 03E6423C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (127, 83); tag 03E63F4C, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 39 (cell 127, 83).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5785, Events line 5896, Actions line 6007.

<a id="trigger-07a2b48c"></a>

### 56. Play Winds Sound - 07A2B48C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (101, 131); tag 07AF00FC, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_WindPlains at waypoint 40 (cell 101, 131).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5786, Events line 5897, Actions line 6008.

<a id="trigger-079f0d5c"></a>

### 57. Play City1 Sounds - 079F0D5C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (66, 47); tag 079F05FC, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 28 (cell 66, 47).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5787, Events line 5898, Actions line 6009.

<a id="trigger-0be67dac"></a>

### 58. Play City2 Sounds - 0BE67DAC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BE674CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur2 at waypoint 36 (cell 22, 88).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5788, Events line 5899, Actions line 6010.

<a id="trigger-09db4d9c"></a>

### 59. BG1 Firesale - 09DB4D9C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09DB47EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. All to Hunt: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
4. All to Hunt: owner selector 16 (country/type EVIL; placed owner Evil House).
5. Enable and reset applicable timers for [No Really Go Hunt (0ACA12CC)](#trigger-0aca12cc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5789, Events line 5900, Actions line 6011.

<a id="trigger-0aca12cc"></a>

### 60. No Really Go Hunt - 0ACA12CC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Firesale (09DB4D9C)](#trigger-09db4d9c).

Attached scope: tag definitions 0ACA21AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. All to Hunt: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
3. All to Hunt: owner selector 16 (country/type EVIL; placed owner Evil House).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5790, Events line 5901, Actions line 6012.

<a id="trigger-0a6c003c"></a>

### 61. Reclaimed Hospital (Engineerland) - 0A6C003C

Owner reference: Elania. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Hospital (0ABA31BC)](#trigger-0aba31bc).
2. Disable [Reclaimed Hospital (Engineerland) (0A6C003C)](#trigger-0a6c003c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5791, Events line 5902, Actions line 6013.

<a id="trigger-0aba31bc"></a>

### 62. Change House Hospital - 0ABA31BC

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Hospital (Engineerland) (0A6C003C)](#trigger-0a6c003c).

Incoming activation links: enable from [Reclaimed Hospital (Engineerland) (0A6C003C)](#trigger-0a6c003c).

Attached scope: Civilian Hospital (CAHOSP), owner House Elania, cell (71, 95), tag 0A6CB04C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Hospital (0ABA31BC)](#trigger-0aba31bc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5792, Events line 5903, Actions line 6014.

<a id="trigger-0a867e5c"></a>

### 63. Pop Beacon Light - 0A867E5C

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Red Light Post (INREDLMP), owner Civie1 House, cell (47, 102), tag 0A86791C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 2 (Beacon Destroyed) is set.

Flag writers in this mission: set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5793, Events line 5904, Actions line 6015.

<a id="trigger-09d56c6c"></a>

### 64. Reclaimed Tesla 01 - 09D56C6C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Tesla 01 (0ABE3A3C)](#trigger-0abe3a3c).
2. Disable [Reclaimed Tesla 01 (09D56C6C)](#trigger-09d56c6c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5794, Events line 5905, Actions line 6016.

<a id="trigger-0abe3a3c"></a>

### 65. Change House Tesla 01 - 0ABE3A3C

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Tesla 01 (09D56C6C)](#trigger-09d56c6c).

Incoming activation links: enable from [Reclaimed Tesla 01 (09D56C6C)](#trigger-09d56c6c).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy2 House, cell (42, 109), tag 09D5672C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Tesla 01 (0ABE3A3C)](#trigger-0abe3a3c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5795, Events line 5906, Actions line 6017.

<a id="trigger-09d5613c"></a>

### 66. Reclaimed Tesla 02 - 09D5613C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Tesla 02 (0ABE1F3C)](#trigger-0abe1f3c).
2. Disable [Reclaimed Tesla 02 (09D5613C)](#trigger-09d5613c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5796, Events line 5907, Actions line 6018.

<a id="trigger-0abe1f3c"></a>

### 67. Change House Tesla 02 - 0ABE1F3C

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Tesla 02 (09D5613C)](#trigger-09d5613c).

Incoming activation links: enable from [Reclaimed Tesla 02 (09D5613C)](#trigger-09d5613c).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy2 House, cell (51, 109), tag 09D54E2C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Tesla 02 (0ABE1F3C)](#trigger-0abe1f3c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5797, Events line 5908, Actions line 6019.

<a id="trigger-07acfd0c"></a>

### 68. Reclaimed Tesla 03 - 07ACFD0C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Tesla 03 (0ABE1A4C)](#trigger-0abe1a4c).
2. Disable [Reclaimed Tesla 03 (07ACFD0C)](#trigger-07acfd0c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5798, Events line 5909, Actions line 6020.

<a id="trigger-0abe1a4c"></a>

### 69. Change House Tesla 03 - 0ABE1A4C

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Tesla 03 (07ACFD0C)](#trigger-07acfd0c).

Incoming activation links: enable from [Reclaimed Tesla 03 (07ACFD0C)](#trigger-07acfd0c).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy2 House, cell (42, 91), tag 07ACFC2C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Tesla 03 (0ABE1A4C)](#trigger-0abe1a4c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5799, Events line 5910, Actions line 6021.

<a id="trigger-07acf66c"></a>

### 70. Reclaimed Tesla 04 - 07ACF66C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Tesla 04 (0ABE2DDC)](#trigger-0abe2ddc).
2. Disable [Reclaimed Tesla 04 (07ACF66C)](#trigger-07acf66c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5800, Events line 5911, Actions line 6022.

<a id="trigger-0abe2ddc"></a>

### 71. Change House Tesla 04 - 0ABE2DDC

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Tesla 04 (07ACF66C)](#trigger-07acf66c).

Incoming activation links: enable from [Reclaimed Tesla 04 (07ACF66C)](#trigger-07acf66c).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy2 House, cell (42, 93), tag 07ACF46C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Tesla 04 (0ABE2DDC)](#trigger-0abe2ddc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5801, Events line 5912, Actions line 6023.

<a id="trigger-079febbc"></a>

### 72. Reclaimed Tesla 05 - 079FEBBC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Tesla 05 (0ABE3DEC)](#trigger-0abe3dec).
2. Disable [Reclaimed Tesla 05 (079FEBBC)](#trigger-079febbc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5802, Events line 5913, Actions line 6024.

<a id="trigger-0abe3dec"></a>

### 73. Change House Tesla 05 - 0ABE3DEC

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Tesla 05 (079FEBBC)](#trigger-079febbc).

Incoming activation links: enable from [Reclaimed Tesla 05 (079FEBBC)](#trigger-079febbc).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy2 House, cell (45, 91), tag 079FE65C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Tesla 05 (0ABE3DEC)](#trigger-0abe3dec).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5803, Events line 5914, Actions line 6025.

<a id="trigger-079fe06c"></a>

### 74. Reclaimed Tesla 06 - 079FE06C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Tesla 06 (0ABA227C)](#trigger-0aba227c).
2. Disable [Reclaimed Tesla 06 (079FE06C)](#trigger-079fe06c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5804, Events line 5915, Actions line 6026.

<a id="trigger-0aba227c"></a>

### 75. Change House Tesla 06 - 0ABA227C

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Tesla 06 (079FE06C)](#trigger-079fe06c).

Incoming activation links: enable from [Reclaimed Tesla 06 (079FE06C)](#trigger-079fe06c).

Attached scope: Tesla Reactor (NAPOWR), owner BadGuy2 House, cell (45, 93), tag 079F852C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Tesla 06 (0ABA227C)](#trigger-0aba227c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5805, Events line 5916, Actions line 6027.

<a id="trigger-079f81fc"></a>

### 76. Reclaimed Sov Barracks2 - 079F81FC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Sov Barracks2 (0ABE5B2C)](#trigger-0abe5b2c).
2. Disable [Reclaimed Sov Barracks2 (079F81FC)](#trigger-079f81fc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5806, Events line 5917, Actions line 6028.

<a id="trigger-0abe5b2c"></a>

### 77. Change House Sov Barracks2 - 0ABE5B2C

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Sov Barracks2 (079F81FC)](#trigger-079f81fc).

Incoming activation links: enable from [Reclaimed Sov Barracks2 (079F81FC)](#trigger-079f81fc).

Attached scope: Soviet Barracks (NAHAND), owner BadGuy2 House, cell (52, 92), tag 079FB3DC, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Sov Barracks2 (0ABE5B2C)](#trigger-0abe5b2c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5807, Events line 5918, Actions line 6029.

<a id="trigger-079fb26c"></a>

### 78. Reclaimed Sov Refinery 1 - 079FB26C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Sov Refinery 1 (0ABE31EC)](#trigger-0abe31ec).
2. Disable [Reclaimed Sov Refinery 1 (079FB26C)](#trigger-079fb26c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5808, Events line 5919, Actions line 6030.

<a id="trigger-0abe31ec"></a>

### 79. Change House Sov Refinery 1 - 0ABE31EC

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Sov Refinery 1 (079FB26C)](#trigger-079fb26c).

Incoming activation links: enable from [Reclaimed Sov Refinery 1 (079FB26C)](#trigger-079fb26c).

Attached scope: Soviet Ore Refinery (NAREFN), owner BadGuy1 House, cell (44, 75), tag 079FB06C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Sov Refinery 1 (0ABE31EC)](#trigger-0abe31ec).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5809, Events line 5920, Actions line 6031.

<a id="trigger-079fdb4c"></a>

### 80. Reclaimed Sov Refinery 2 - 079FDB4C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Sov Refinery 2 (0ABE76CC)](#trigger-0abe76cc).
2. Disable [Reclaimed Sov Refinery 2 (079FDB4C)](#trigger-079fdb4c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5810, Events line 5921, Actions line 6032.

<a id="trigger-0abe76cc"></a>

### 81. Change House Sov Refinery 2 - 0ABE76CC

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Sov Refinery 2 (079FDB4C)](#trigger-079fdb4c).

Incoming activation links: enable from [Reclaimed Sov Refinery 2 (079FDB4C)](#trigger-079fdb4c).

Attached scope: Soviet Ore Refinery (NAREFN), owner BadGuy1 House, cell (57, 75), tag 079FD94C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Sov Refinery 2 (0ABE76CC)](#trigger-0abe76cc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5811, Events line 5922, Actions line 6033.

<a id="trigger-079fd76c"></a>

### 82. Reclaimed Sov Barracks1 - 079FD76C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Sov Barracks1 (0ABE5E9C)](#trigger-0abe5e9c).
2. Disable [Reclaimed Sov Barracks1 (079FD76C)](#trigger-079fd76c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5812, Events line 5923, Actions line 6034.

<a id="trigger-0abe5e9c"></a>

### 83. Change House Sov Barracks1 - 0ABE5E9C

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Sov Barracks1 (079FD76C)](#trigger-079fd76c).

Incoming activation links: enable from [Reclaimed Sov Barracks1 (079FD76C)](#trigger-079fd76c).

Attached scope: Soviet Barracks (NAHAND), owner BadGuy1 House, cell (61, 60), tag 07A0221C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Sov Barracks1 (0ABE5E9C)](#trigger-0abe5e9c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5813, Events line 5924, Actions line 6035.

<a id="trigger-07a040ac"></a>

### 84. Reclaimed Sov ConYard - 07A040AC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Sov ConYard (0ABE34EC)](#trigger-0abe34ec).
2. Disable [Reclaimed Sov ConYard (07A040AC)](#trigger-07a040ac).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5814, Events line 5925, Actions line 6036.

<a id="trigger-0abe34ec"></a>

### 85. Change House Sov ConYard - 0ABE34EC

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Sov ConYard (07A040AC)](#trigger-07a040ac).

Incoming activation links: enable from [Reclaimed Sov ConYard (07A040AC)](#trigger-07a040ac).

Attached scope: Soviet Construction Yard (NACNST), owner BadGuy1 House, cell (59, 65), tag 07A0542C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Sov ConYard (0ABE34EC)](#trigger-0abe34ec).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5815, Events line 5926, Actions line 6037.

<a id="trigger-07a0662c"></a>

### 86. Reclaimed Sov WarFactory - 07A0662C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type ENGINEERLAND; placed owner EngineerLand House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Sov WarFactory (0ABE735C)](#trigger-0abe735c).
2. Disable [Reclaimed Sov WarFactory (07A0662C)](#trigger-07a0662c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5816, Events line 5927, Actions line 6038.

<a id="trigger-0abe735c"></a>

### 87. Change House Sov WarFactory - 0ABE735C

Owner reference: EngineerLand. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Sov WarFactory (07A0662C)](#trigger-07a0662c).

Incoming activation links: enable from [Reclaimed Sov WarFactory (07A0662C)](#trigger-07a0662c).

Attached scope: Soviet War Factory (NAWEAP), owner BadGuy1 House, cell (50, 61), tag 07A0642C, persistence mode 2.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Sov WarFactory (0ABE735C)](#trigger-0abe735c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5817, Events line 5928, Actions line 6039.

<a id="trigger-0844203c"></a>

### 88. BG Patrols Start (Med) - 0844203C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [BG Patrols Start (Hard) (09AB895C)](#trigger-09ab895c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Beacon Perimeter Patrol (081104F4)](all08u-teams.md#team-081104f4).
2. Supply reinforcement team [Evil Patrol 1 (0B996384)](all08u-teams.md#team-0b996384).
3. Supply reinforcement team [Evil Patrol 2 (08F73AF4)](all08u-teams.md#team-08f73af4).
4. Supply reinforcement team [Evil Patrol 3 (07A458C4)](all08u-teams.md#team-07a458c4).
5. Supply reinforcement team [Evil Armor 1 (08DA8F04)](all08u-teams.md#team-08da8f04).
6. Supply reinforcement team [Evil Armor 2 (0A632EFC)](all08u-teams.md#team-0a632efc).
7. Supply reinforcement team [POW Patrol 1 (0A300CBC)](all08u-teams.md#team-0a300cbc).
8. Supply reinforcement team [POW Patrol 2 (0AF7132C)](all08u-teams.md#team-0af7132c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5818, Events line 5929, Actions line 6040.

<a id="trigger-09e9d56c"></a>

### 89. BG Patrols Start (Easy) - 09E9D56C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [BG Patrols Start (Med) (0844203C)](#trigger-0844203c).

Attached scope: tag definitions 09AB81CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Beacon Perimeter Patrol (081104F4)](all08u-teams.md#team-081104f4).
2. Supply reinforcement team [Evil Armor 1 (08DA8F04)](all08u-teams.md#team-08da8f04).
3. Supply reinforcement team [Evil Patrol 1 (0B996384)](all08u-teams.md#team-0b996384).
4. Supply reinforcement team [Evil Patrol 2 (08F73AF4)](all08u-teams.md#team-08f73af4).
5. Supply reinforcement team [Evil Patrol 3 (07A458C4)](all08u-teams.md#team-07a458c4).
6. Supply reinforcement team [POW Patrol 1 (0A300CBC)](all08u-teams.md#team-0a300cbc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5819, Events line 5930, Actions line 6041.

<a id="trigger-0a7998fc"></a>

### 90. BG1 AITrig Begin - 0A7998FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A79BB6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
3. Play music theme Destroy.
4. Enable and reset applicable timers for [Player Reinforcers2E Go (0A197B2C)](#trigger-0a197b2c).
5. Enable and reset applicable timers for [Player Reinforcers2M Go (0A19AAFC)](#trigger-0a19aafc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5820, Events line 5931, Actions line 6042.

<a id="trigger-0a197b2c"></a>

### 91. Player Reinforcers2E Go - 0A197B2C

Owner reference: Reinforcers. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 AITrig Begin (0A7998FC)](#trigger-0a7998fc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Player Reinforcements 5E_1 (0CE2448C)](all08u-teams.md#team-0ce2448c).
2. Supply reinforcement team [Player Reinforcements 5E_2 (0CE23DEC)](all08u-teams.md#team-0ce23dec).
3. Create radar-event marker type 2 at waypoint 5 (cell 148, 81).
4. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5821, Events line 5932, Actions line 6043.

<a id="trigger-0a19aafc"></a>

### 92. Player Reinforcers2M Go - 0A19AAFC

Owner reference: Reinforcers. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Player Reinforcers2E Go (0A197B2C)](#trigger-0a197b2c).

Incoming activation links: enable from [BG1 AITrig Begin (0A7998FC)](#trigger-0a7998fc).

Attached scope: tag definitions 0A19753C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Player Reinforcements 5E_1 (0CE2448C)](all08u-teams.md#team-0ce2448c).
2. Create radar-event marker type 2 at waypoint 5 (cell 148, 81).
3. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5822, Events line 5933, Actions line 6044.

<a id="trigger-0a78f81c"></a>

### 93. Extra Cash - 0A78F81C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A78B1FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Beacon Destroyed) is set.

Flag writers in this mission: set local flag 2 (Beacon Destroyed) at [Psychic Beacon KIA (07BB91BC)](#trigger-07bb91bc); set local flag 2 (Beacon Destroyed) at [Psychic Beacon Change House (0CF745DC)](#trigger-0cf745dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 0 (cell 47, 100).
2. Play sound Bonus at waypoint 0 (cell 47, 100).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5823, Events line 5934, Actions line 6045.

<a id="trigger-087966dc"></a>

### 94. Bonus Timer Extension (WF) - 087966DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 8 (War Factory Reclaim) is set.

Flag writers in this mission: set local flag 8 (War Factory Reclaim) at [Reclaimed War Factory (Engineerland) (08CD3194)](#trigger-08cd3194). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Display message “Bonus Discovered. Timer Extended.” (MISSION:All08e).
2. Extend the mission timer by 600 configured time units.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5824, Events line 5935, Actions line 6046.

<a id="trigger-087965ec"></a>

### 95. Bonus Timer Extension (Ref) - 087965EC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: [Bonus Timer Extension (WF) (087966DC)](#trigger-087966dc).

Attached scope: tag definitions 0879689C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (Refinery Reclaimed) is set.

Flag writers in this mission: set local flag 7 (Refinery Reclaimed) at [Reclaimed Refinery (Engineerland) (07AEFA84)](#trigger-07aefa84). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Display message “Bonus Discovered. Timer Extended.” (MISSION:All08e).
2. Extend the mission timer by 600 configured time units.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5825, Events line 5936, Actions line 6047.

<a id="trigger-087d4aec"></a>

### 96. Reclaimed War Factory (Player) - 087D4AEC

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change House War Factory (Engineerland) (0ABE8C3C)](#trigger-0abe8c3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).
2. local flag 8 (War Factory Reclaim) is clear.

Flag writers in this mission: set local flag 8 (War Factory Reclaim) at [Reclaimed War Factory (Engineerland) (08CD3194)](#trigger-08cd3194). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House War Factory (Engineerland) (0ABE8C3C)](#trigger-0abe8c3c).
2. Disable [Reclaimed War Factory (Player) (087D4AEC)](#trigger-087d4aec).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5826, Events line 5937, Actions line 6048.

<a id="trigger-087d5e8c"></a>

### 97. Change House War Factory (Player) - 087D5E8C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed War Factory (Player) (087D4AEC)](#trigger-087d4aec).

Attached scope: Allied War Factory (GAWEAP), owner Civie1 House, cell (103, 120), tag 08CD4B94, persistence mode 2.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House War Factory (Player) (087D5E8C)](#trigger-087d5e8c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5827, Events line 5938, Actions line 6049.

<a id="trigger-087d593c"></a>

### 98. Change House Refinery (Player) - 087D593C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change House Refinery (Engineerland) (0ABE07DC)](#trigger-0abe07dc).

Incoming activation links: enable from [Reclaimed Refinery (Player) (087D567C)](#trigger-087d567c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Disable [Change House Refinery (Player) (087D593C)](#trigger-087d593c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5828, Events line 5939, Actions line 6050.

<a id="trigger-087d567c"></a>

### 99. Reclaimed Refinery (Player) - 087D567C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Change House Refinery (Player) (087D593C)](#trigger-087d593c).

Attached scope: Allied Ore Refinery (GAREFN), owner Civie1 House, cell (87, 139), tag 079F4E24, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).
2. local flag 7 (Refinery Reclaimed) is clear.

Flag writers in this mission: set local flag 7 (Refinery Reclaimed) at [Reclaimed Refinery (Engineerland) (07AEFA84)](#trigger-07aefa84). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House Refinery (Player) (087D593C)](#trigger-087d593c).
2. Disable [Reclaimed Refinery (Player) (087D567C)](#trigger-087d567c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5829, Events line 5940, Actions line 6051.

<a id="trigger-0d1a8c6c"></a>

### 100. POW Panic Begin - 0D1A8C6C

Owner reference: Civilian1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D1A867C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (Desolator Gooing) is set.

**Then perform these actions in order:**

1. Create/recruit team [POW Panic (0D1A928C)](all08u-teams.md#team-0d1a928c).
2. Play sound CivAllFear at waypoint 20 (cell 71, 80).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5830, Events line 5941, Actions line 6052.

<a id="trigger-0a5c417c"></a>

### 101. Evil Armor Redemption MkII - 0A5C417C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A5C334C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 13 (Evil Armor Redempti) is set.

**Then perform these actions in order:**

1. Create/recruit team [Evil Armor Redemption MkII (0A5C531C)](all08u-teams.md#team-0a5c531c).
2. Play voice notification Mis_A8_AllSoldierFreed.

Source locator: MAPS01.MIX/all08u.map; Triggers line 5831, Events line 5942, Actions line 6053.

<a id="trigger-0a5db64c"></a>

### 102. Get Thee to the Arch - 0A5DB64C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A5DFE7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 14 (Goto AW) is set.

**Then perform these actions in order:**

1. Create/recruit team [Get thee to the Arch (0A5C321C)](all08u-teams.md#team-0a5c321c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5832, Events line 5943, Actions line 6054.

<a id="trigger-0d28c05c"></a>

### 103. Reinforcers 1 Here - 0D28C05C

Owner reference: Reinforcers. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D28BDCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Prism 1 Unloaded) is set.

**Then perform these actions in order:**

1. Create/recruit team [Player Reinforcers 1a (0CDAAEFC)](all08u-teams.md#team-0cdaaefc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5833, Events line 5944, Actions line 6055.

<a id="trigger-0d28bcdc"></a>

### 104. Reinforcers 2 Here - 0D28BCDC

Owner reference: Reinforcers. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D289A1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 11 (Prism 2 Unloaded) is set.

**Then perform these actions in order:**

1. Create/recruit team [Player Reinforcers 2a (0CDAAB5C)](all08u-teams.md#team-0cdaab5c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5834, Events line 5945, Actions line 6056.

<a id="trigger-0d255cfc"></a>

### 105. Reinforcers 3 Here - 0D255CFC

Owner reference: Reinforcers. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D253B2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 15 (3 Unloaded) is set.

**Then perform these actions in order:**

1. Create/recruit team [Player Reinforcers 3a (0CDAA91C)](all08u-teams.md#team-0cdaa91c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5835, Events line 5946, Actions line 6057.

<a id="trigger-0d254f3c"></a>

### 106. Reinforcers 4 Here - 0D254F3C

Owner reference: Reinforcers. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D252C4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 16 (4 Unloaded) is set.

**Then perform these actions in order:**

1. Create/recruit team [Player Reinforcers 4a (0CDAA6DC)](all08u-teams.md#team-0cdaa6dc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5836, Events line 5947, Actions line 6058.

<a id="trigger-0d2568bc"></a>

### 107. Reinforcers 5e1 Here - 0D2568BC

Owner reference: Reinforcers. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D2520CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 17 (5e1 Unloaded) is set.

**Then perform these actions in order:**

1. Create/recruit team [Player Reinforcers 5e1a (0CDAA49C)](all08u-teams.md#team-0cdaa49c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5837, Events line 5948, Actions line 6059.

<a id="trigger-0d256f3c"></a>

### 108. Reinforcers 5e2 Here - 0D256F3C

Owner reference: Reinforcers. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D25758C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 18 (5e2 Unloaded) is set.

**Then perform these actions in order:**

1. Create/recruit team [Player Reinforcers 5e2a (0CDAA25C)](all08u-teams.md#team-0cdaa25c).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5838, Events line 5949, Actions line 6060.

<a id="trigger-0d2533dc"></a>

### 109. Prism Flashers Enable - 0D2533DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D256B9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Prism 1 Unloaded) is set.
2. local flag 11 (Prism 2 Unloaded) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Prism Tank Movie Play (075A9ADC)](#trigger-075a9adc).

Source locator: MAPS01.MIX/all08u.map; Triggers line 5839, Events line 5950, Actions line 6061.

[All team rosters and ordered plans](all08u-teams.md) | [All mission overrides](all08u-overrides.md)
