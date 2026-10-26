# Operation: Lone Guardian

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all01t.map. **Effective extracted member:** MAPS02.MIX/all01t.map. **Trigger definitions:** 130.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all01t-teams.md) | [All mission overrides](all01t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | URBAN |
| Map size | 0,0,50,64 |
| Visible local rectangle | 2,6,46,52 |
| Placed vehicles | 19 |
| Placed infantry | 40 |
| Placed structures | 190 |
| Placed aircraft | 0 |
| Team templates | 49 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 40 | Player |
| 1 | BadGuy1 House | 100 | BadGuy1 |
| 2 | BadGuy2 House | 100 | BadGuy2 |
| 3 | BadGuy3 House | 100 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 20 | Other1 |
| 6 | Other2 House | 20 | Other2 |
| 7 | Other3 House | 20 | Other3 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Transport 1,0 |
| 1 | Transport 2,1 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Mission Victory (075F22EC)](#trigger-075f22ec) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [Mission Failed (08B9BC5C)](#trigger-08b9bc5c) | 2 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-07a9578c"></a>

### 1. Mission Start - 07A9578C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A94ACC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [BG1 - Dreadnought 1 (0A67F6CC)](all01t-teams.md#team-0a67f6cc).
2. Create/recruit team [BG1 - Dreadnought 1 (0A67F6CC)](all01t-teams.md#team-0a67f6cc).
3. Create/recruit team [BG1 - Dreadnought 1 (0A67F6CC)](all01t-teams.md#team-0a67f6cc).
4. Create/recruit team [BG1 - Dreadnought 1 (0A67F6CC)](all01t-teams.md#team-0a67f6cc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4474, Events line 4606, Actions line 4738.

<a id="trigger-07a949dc"></a>

### 2. Mission Start 2 - 07A949DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A9467C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 1 (cell 62, 90).
2. Create radar-event marker type 3 at waypoint 1 (cell 62, 90).
3. Reveal terrain around waypoint 27 (cell 64, 82).
4. Reveal terrain around waypoint 49 (cell 64, 74).
5. Enable and reset applicable timers for [Mission Start 3 (07C3C37C)](#trigger-07c3c37c).
6. Reveal terrain around waypoint 20 (cell 63, 69).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4475, Events line 4607, Actions line 4739.

<a id="trigger-07c3c37c"></a>

### 3. Mission Start 3 - 07C3C37C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Mission Start 2 (07A949DC)](#trigger-07a949dc).

Attached scope: tag definitions 07C429CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound NukeSiren.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4476, Events line 4608, Actions line 4740.

<a id="trigger-076e465c"></a>

### 4. Enable Objective 1 - 076E465C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start Scroll (079C403C)](#trigger-079c403c).

Attached scope: tag definitions 076D9BBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 13 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Destroy all four Soviet DREADNOUGHTS” (MISSION:All01a).
2. Play sound MessageText.
3. Create radar-event marker type 1 at waypoint 1 (cell 62, 90).
4. Enable and reset applicable timers for [Objective 1 (076F572C)](#trigger-076f572c).
5. Play voice notification EVA_NewObjectiveReceived.
6. Flash team [BG1 - Dreadnought 1 (0A67F6CC)](all01t-teams.md#team-0a67f6cc) with duration setting 70.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4477, Events line 4609, Actions line 4741.

<a id="trigger-076f572c"></a>

### 5. Objective 1 - 076F572C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Objective 1 (076E465C)](#trigger-076e465c).

Attached scope: tag definitions 076F057C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Destroy all four Soviet DREADNOUGHTS” (MISSION:ALL01a).
2. Create radar-event marker type 1 at waypoint 1 (cell 62, 90).
3. Play sound MessageText.
4. Flash team [BG1 - Dreadnought 1 (0A67F6CC)](all01t-teams.md#team-0a67f6cc) with duration setting 90.
5. Flash team [Dreadnought Retreat (0B533EFC)](all01t-teams.md#team-0b533efc) with duration setting 90.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4478, Events line 4610, Actions line 4742.

<a id="trigger-07a707cc"></a>

### 6. Start Conscripts Attacking - 07A707CC

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Conscript Attack (0733A6CC)](#trigger-0733a6cc).

Attached scope: tag definitions 07A7012C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [BG1 - Conscripts2a (097531FC)](all01t-teams.md#team-097531fc).
2. Create/recruit team [BG1 - Conscripts2b (09752C8C)](all01t-teams.md#team-09752c8c).
3. Enable and reset applicable timers for [Enable GI's (07428AAC)](#trigger-07428aac).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4479, Events line 4611, Actions line 4743.

<a id="trigger-07428aac"></a>

### 7. Enable GI's - 07428AAC

Owner reference: Other3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start Conscripts Attacking (07A707CC)](#trigger-07a707cc); enable from [Initial Paratroopers 1 (07BA8C2C)](#trigger-07ba8c2c).

Attached scope: tag definitions 074284EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Player - GIs1 (0A7475CC)](all01t-teams.md#team-0a7475cc).
2. Enable and reset applicable timers for [ButtNugget (07BBD33C)](#trigger-07bbd33c).
3. Enable and reset applicable timers for [Enable GI's 2 (0828B83C)](#trigger-0828b83c).
4. Enable and reset applicable timers for [Hint: GI (0A96A5EC)](#trigger-0a96a5ec).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4480, Events line 4612, Actions line 4744.

<a id="trigger-07bbd33c"></a>

### 8. ButtNugget - 07BBD33C

Owner reference: Other3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable GI's (07428AAC)](#trigger-07428aac).

Attached scope: tag definitions 07BFF58C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All change house: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4481, Events line 4613, Actions line 4745.

<a id="trigger-0828b83c"></a>

### 9. Enable GI's 2 - 0828B83C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable GI's (07428AAC)](#trigger-07428aac).

Attached scope: tag definitions 0828FB3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash team [Player - GIs1 (0A7475CC)](all01t-teams.md#team-0a7475cc) with duration setting 40.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4482, Events line 4614, Actions line 4746.

<a id="trigger-0a96a5ec"></a>

### 10. Hint: GI - 0A96A5EC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable GI's (07428AAC)](#trigger-07428aac).

Attached scope: GI (E1), owner Other3 House, cell (58, 68), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (64, 67), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (65, 75), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (60, 66), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (66, 69), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (60, 74), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (62, 66), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (66, 73), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (67, 71), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (58, 71), tag 0A96BF4C, persistence mode 0; GI (E1), owner Other3 House, cell (62, 75), tag 0A96BF4C, persistence mode 0.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “These GI's have deployed their heavy machine guns.” (MISSION:All01u).
2. Play sound MessageText.
3. Create radar-event marker type 0 at waypoint 20 (cell 63, 69).
4. Enable and reset applicable timers for [Hint: GI 2 (0A96BE5C)](#trigger-0a96be5c).
5. Enable and reset applicable timers for [Hint: GI 3 (0A19262C)](#trigger-0a19262c).
6. Enable and reset applicable timers for [Hint: GI 4 (0A19574C)](#trigger-0a19574c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4483, Events line 4615, Actions line 4747.

<a id="trigger-0a96be5c"></a>

### 11. Hint: GI 2 - 0A96BE5C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: GI (0A96A5EC)](#trigger-0a96a5ec).

Attached scope: tag definitions 0A96BC1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “HINT: DOUBLE-CLICK the GI's to switch them between DEPLOYED and MOBILE states” (MISSION:All01t).
2. Play sound MessageText.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4484, Events line 4616, Actions line 4748.

<a id="trigger-0a19262c"></a>

### 12. Hint: GI 3 - 0A19262C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: GI (0A96A5EC)](#trigger-0a96a5ec).

Attached scope: tag definitions 0A19591C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
2. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
3. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
4. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
5. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
6. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
7. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
8. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
9. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
10. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).
11. Create/recruit team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4485, Events line 4617, Actions line 4749.

<a id="trigger-0a19574c"></a>

### 13. Hint: GI 4 - 0A19574C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: GI (0A96A5EC)](#trigger-0a96a5ec).

Attached scope: tag definitions 0A19530C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash team [Flash GI (0AC8730C)](all01t-teams.md#team-0ac8730c) with duration setting 90.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4486, Events line 4618, Actions line 4750.

<a id="trigger-0782da30"></a>

### 14. Enable Objective 2b - 0782DA30

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Play Soviet Movie 2 (081A1B4C)](#trigger-081a1b4c).

Attached scope: tag definitions 0782D140 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 63 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Enable Objective 2 (0874458C)](#trigger-0874458c).
2. Play voice notification Mis_A1_EvaReachFort.
3. Disable [Objective 1 (076F572C)](#trigger-076f572c).
4. Disable [Enable Objective 1 (076E465C)](#trigger-076e465c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4487, Events line 4619, Actions line 4751.

<a id="trigger-0874458c"></a>

### 15. Enable Objective 2 - 0874458C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Objective 2b (0782DA30)](#trigger-0782da30).

Attached scope: tag definitions 08747E9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Objective 2 (0874286C)](#trigger-0874286c).
2. Display message “Objective 2: Rendezvous with FORT BRADLEY” (MISSION:All01b).
3. Create radar-event marker type 1 at waypoint 16 (cell 74, 38).
4. Play sound MessageText.
5. Reveal terrain around waypoint 16 (cell 74, 38).
6. Enable and reset applicable timers for [Hint: First Bridge (09E42C7C)](#trigger-09e42c7c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4488, Events line 4620, Actions line 4752.

<a id="trigger-0874286c"></a>

### 16. Objective 2 - 0874286C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Objective 2 (0874458C)](#trigger-0874458c).

Attached scope: tag definitions 0874467C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Rendezvous with FORT BRADLEY” (MISSION:All01b).
2. Create radar-event marker type 1 at waypoint 16 (cell 74, 38).
3. Play sound MessageText.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4489, Events line 4621, Actions line 4753.

<a id="trigger-09e42c7c"></a>

### 17. Hint: First Bridge - 09E42C7C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Objective 2 (0874458C)](#trigger-0874458c).

Attached scope: 12 tagged map cells: (61, 60), (62, 60), (63, 60), (61, 61), (62, 61), (63, 61), (61, 62), (62, 62), (63, 62), (61, 63), (62, 63), (63, 63); tag 09E408FC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 80 (cell 62, 59).
2. Reveal terrain around waypoint 80 (cell 62, 59).
3. Play sound MessageText.
4. Play voice notification Mis_A1_EvaBridgeDestroyed.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4490, Events line 4622, Actions line 4754.

<a id="trigger-0871b6ec"></a>

### 18. Change House 1a - 0871B6EC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0871A4FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House 1b (0871A32C)](#trigger-0871a32c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4491, Events line 4623, Actions line 4755.

<a id="trigger-0871a32c"></a>

### 19. Change House 1b - 0871A32C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change House 1a (0871B6EC)](#trigger-0871b6ec).

Attached scope: tag definitions 0871A12C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4492, Events line 4624, Actions line 4756.

<a id="trigger-096564cc"></a>

### 20. Change House 2a - 096564CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 47 tagged map cells: (65, 28), (66, 28), (67, 28), (68, 28), (69, 28), (70, 28), (71, 28), (72, 28), (73, 28), (74, 28), (75, 28), (76, 28), (77, 28), (64, 29), (65, 29), (64, 30), (64, 31), (64, 32), (64, 33), (64, 34), (64, 35), (65, 35), (65, 36), (64, 37), (65, 37), (64, 38), (65, 38), (64, 39), (65, 39), (65, 40), (64, 41), (65, 41), (64, 42), (64, 43), (64, 44), (64, 45), (64, 46), (64, 47), (65, 47), (65, 48), (66, 48), (67, 48), (68, 48), (69, 48), (70, 48), (71, 48), (72, 48); tag 0965B06C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Change House 2b (0965E07C)](#trigger-0965e07c).
2. Reveal terrain around waypoint 10 (cell 69, 43).
3. Reveal terrain around waypoint 11 (cell 76, 43).
4. Reveal terrain around waypoint 13 (cell 69, 33).
5. Reveal terrain around waypoint 14 (cell 76, 33).
6. Reveal terrain around waypoint 15 (cell 84, 35).
7. Create radar-event marker type 1 at waypoint 16 (cell 74, 38).
8. Play voice notification Mis_A1_EvaControlFort.
9. Create/recruit team [Player Chrono Miners (2) (09B091FC)](all01t-teams.md#team-09b091fc).
10. Disable [Objective 2 (0874286C)](#trigger-0874286c).
11. Disable [Hint: First Bridge (09E42C7C)](#trigger-09e42c7c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4493, Events line 4625, Actions line 4757.

<a id="trigger-0965e07c"></a>

### 21. Change House 2b - 0965E07C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change House 2a (096564CC)](#trigger-096564cc).

Attached scope: Attack Dog (ADOG), owner Other1 House, cell (74, 40), tag 0965BDDC, persistence mode 0; Attack Dog (ADOG), owner Other1 House, cell (74, 36), tag 0965BDDC, persistence mode 0; Attack Dog (ADOG), owner Other1 House, cell (72, 38), tag 0965BDDC, persistence mode 0; Attack Dog (ADOG), owner Other1 House, cell (76, 37), tag 0965BDDC, persistence mode 0; Allied Construction Yard (GACNST), owner Other1 House, cell (71, 31), tag 0965BDDC, persistence mode 0; Allied Ore Refinery (GAREFN), owner Other1 House, cell (73, 44), tag 0965BDDC, persistence mode 0; Power Plant (GAPOWR), owner Other1 House, cell (67, 31), tag 0965BDDC, persistence mode 0; Power Plant (GAPOWR), owner Other1 House, cell (67, 34), tag 0965BDDC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (64, 40), tag 0965BDDC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (64, 36), tag 0965BDDC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (85, 48), tag 0965BDDC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (79, 48), tag 0965BDDC, persistence mode 0; Gate (GAGATE_A), owner Civie1 House, cell (81, 48), tag 0965BDDC, persistence mode 0; US Flag (CAUSFGL), owner Other1 House, cell (79, 46), tag 0965BDDC, persistence mode 0; US Flag (CAUSFGL), owner Other1 House, cell (85, 46), tag 0965BDDC, persistence mode 0; US Flag (CAUSFGL), owner Other1 House, cell (65, 33), tag 0965BDDC, persistence mode 0; US Flag (CAUSFGL), owner Other1 House, cell (65, 43), tag 0965BDDC, persistence mode 0; US Flag (CAUSFGL), owner Other1 House, cell (77, 34), tag 0965BDDC, persistence mode 0; Patriot Missile (NASAM), owner Other2 House, cell (59, 83), tag 0965BDDC, persistence mode 0; Patriot Missile (NASAM), owner Other2 House, cell (66, 83), tag 0965BDDC, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (65, 45), tag 0965BDDC, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (65, 31), tag 0965BDDC, persistence mode 0; Power Plant (GAPOWR), owner Other1 House, cell (67, 42), tag 0965BDDC, persistence mode 0; Power Plant (GAPOWR), owner Other1 House, cell (67, 45), tag 0965BDDC, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (80, 40), tag 0965BDDC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (70, 40), tag 0965BDDC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (70, 36), tag 0965BDDC, persistence mode 0.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Play sound MessageText.
3. Enable and reset applicable timers for [Con Yard Destroyed (0A08DB4C)](#trigger-0a08db4c).
4. Disable [Objective 2 (0874286C)](#trigger-0874286c).
5. Enable and reset applicable timers for [Enable Objective 3 (08CD8C30)](#trigger-08cd8c30).
6. Play in-game movie 68.
7. Supply reinforcement team [Chrono Harvester (1) (0831459C)](all01t-teams.md#team-0831459c) at waypoint 4 (cell 74, 43).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4494, Events line 4626, Actions line 4758.

<a id="trigger-0a08db4c"></a>

### 22. Con Yard Destroyed - 0A08DB4C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change House 2b (0965E07C)](#trigger-0965e07c).

Attached scope: tag definitions 0A08859C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Emergency Reinforcements (0A08512C)](all01t-teams.md#team-0a08512c).
2. Create radar-event marker type 2 at waypoint 16 (cell 74, 38).
3. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4495, Events line 4627, Actions line 4759.

<a id="trigger-08cd8c30"></a>

### 23. Enable Objective 3 - 08CD8C30

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Change House 2b (0965E07C)](#trigger-0965e07c).

Attached scope: tag definitions 03E2C110 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 52 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 32 (cell 96, 71).
2. Play sound MessageText.
3. Display message “Objective 3: Destroy the Soviet SUPPLY BASE” (MISSION:ALL01h).
4. Enable and reset applicable timers for [Objective 3 (08A6E100)](#trigger-08a6e100).
5. Reveal terrain around waypoint 32 (cell 96, 71).
6. Enable and reset applicable timers for [Enable Salvos (0B43F31C)](#trigger-0b43f31c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4496, Events line 4628, Actions line 4760.

<a id="trigger-08a6e100"></a>

### 24. Objective 3 - 08A6E100

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Objective 3 (08CD8C30)](#trigger-08cd8c30).

Attached scope: tag definitions 03E2ECF0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Destroy the Soviet SUPPLY BASE” (MISSION:ALL01h).
2. Create radar-event marker type 5 at waypoint 32 (cell 96, 71).
3. Play sound MessageText.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4497, Events line 4629, Actions line 4761.

<a id="trigger-0b43f31c"></a>

### 25. Enable Salvos - 0B43F31C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Objective 3 (08CD8C30)](#trigger-08cd8c30).

Attached scope: tag definitions 0B43FA8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create V3a (0B91CA1C)](#trigger-0b91ca1c).
2. Enable and reset applicable timers for [Create V3b (0B918B9C)](#trigger-0b918b9c).
3. Enable and reset applicable timers for [Create V3c (0B9188AC)](#trigger-0b9188ac).
4. Enable and reset applicable timers for [Create V3d (09481A9C)](#trigger-09481a9c).
5. Enable and reset applicable timers for [Create V3e (0949CD5C)](#trigger-0949cd5c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4498, Events line 4630, Actions line 4762.

<a id="trigger-0b91ca1c"></a>

### 26. Create V3a - 0B91CA1C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Salvos (0B43F31C)](#trigger-0b43f31c).

Attached scope: tag definitions 0B918D6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [V3 - Salvo (095B322C)](all01t-teams.md#team-095b322c) at waypoint 95 (cell 87, 56).
2. Create radar-event marker type 5 at waypoint 95 (cell 87, 56).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4499, Events line 4631, Actions line 4763.

<a id="trigger-0b918b9c"></a>

### 27. Create V3b - 0B918B9C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Salvos (0B43F31C)](#trigger-0b43f31c).

Attached scope: tag definitions 0B91899C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [V3 - Salvo (095B322C)](all01t-teams.md#team-095b322c) at waypoint 94 (cell 92, 56).
2. Create radar-event marker type 5 at waypoint 94 (cell 92, 56).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4500, Events line 4632, Actions line 4764.

<a id="trigger-0b9188ac"></a>

### 28. Create V3c - 0B9188AC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Salvos (0B43F31C)](#trigger-0b43f31c).

Attached scope: tag definitions 0B9186AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [V3 - Salvo (095B322C)](all01t-teams.md#team-095b322c) at waypoint 93 (cell 97, 56).
2. Create radar-event marker type 5 at waypoint 93 (cell 97, 56).
3. Reveal terrain around waypoint 94 (cell 92, 56).
4. Reveal terrain around waypoint 95 (cell 87, 56).
5. Reveal terrain around waypoint 93 (cell 97, 56).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4501, Events line 4633, Actions line 4765.

<a id="trigger-09481a9c"></a>

### 29. Create V3d - 09481A9C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Salvos (0B43F31C)](#trigger-0b43f31c).

Attached scope: tag definitions 094814BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 18 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [V3 Salvo 2 (094806FC)](all01t-teams.md#team-094806fc) at waypoint 51 (cell 77, 58).
2. Create radar-event marker type 5 at waypoint 51 (cell 77, 58).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4502, Events line 4634, Actions line 4766.

<a id="trigger-0949cd5c"></a>

### 30. Create V3e - 0949CD5C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Salvos (0B43F31C)](#trigger-0b43f31c).

Attached scope: tag definitions 0949C42C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 24 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [V3 Salvo 2 (094806FC)](all01t-teams.md#team-094806fc) at waypoint 12 (cell 77, 63).
2. Create radar-event marker type 5 at waypoint 12 (cell 77, 63).
3. Reveal terrain around waypoint 12 (cell 77, 63).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4503, Events line 4635, Actions line 4767.

<a id="trigger-0799590c"></a>

### 31. Paratroopers 1 - 0799590C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Paratroopers 1 (09C1A03C)](#trigger-09c1a03c).

Attached scope: tag definitions 0799C03C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 160 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 - Paratroopers1 (0AC446AC)](all01t-teams.md#team-0ac446ac).
2. Play sound AirRaidSiren.
3. Display message “WARNING: Soviet PARATROOPERS are incoming” (MISSION:ALL01i).
4. Supply reinforcement team [BG1 - Paratroopers2 (0AC42B7C)](all01t-teams.md#team-0ac42b7c).
5. Create radar-event marker type 5 at waypoint 17 (cell 39, 39).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4504, Events line 4636, Actions line 4768.

<a id="trigger-079bf40c"></a>

### 32. Lock Input - 079BF40C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079C504C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable player input.
2. Enable and reset applicable timers for [Start Scroll (079C403C)](#trigger-079c403c).
3. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4505, Events line 4637, Actions line 4769.

<a id="trigger-079c403c"></a>

### 33. Start Scroll - 079C403C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Lock Input (079BF40C)](#trigger-079bf40c).

Attached scope: tag definitions 079C804C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 18 (cell 57, 92) with speed setting 1.
2. Enable and reset applicable timers for [Start Transports (09BF43EC)](#trigger-09bf43ec).
3. Enable and reset applicable timers for [Enable Objective 1 (076E465C)](#trigger-076e465c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4506, Events line 4638, Actions line 4770.

<a id="trigger-09bf43ec"></a>

### 34. Start Transports - 09BF43EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start Scroll (079C403C)](#trigger-079c403c).

Attached scope: tag definitions 09BF1D4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 14 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound NavalUnitEmerge.
2. Supply reinforcement team [Transport 1 (0AB436CC)](all01t-teams.md#team-0ab436cc).
3. Supply reinforcement team [Transport 2 (0AB4321C)](all01t-teams.md#team-0ab4321c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4507, Events line 4639, Actions line 4771.

<a id="trigger-07fa0f3c"></a>

### 35. Unlock Input - 07FA0F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FA0A0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 14 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Unlock Input 2 (094DE03C)](#trigger-094de03c).
2. Play in-game movie 69.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4508, Events line 4640, Actions line 4772.

<a id="trigger-094de03c"></a>

### 36. Unlock Input 2 - 094DE03C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Unlock Input (07FA0F3C)](#trigger-07fa0f3c).

Attached scope: tag definitions 094DC36C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 36 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Unlock Input 3 (094D93DC)](#trigger-094d93dc).
2. Create/recruit team [Player - Tanya1 (094F68EC)](all01t-teams.md#team-094f68ec).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4509, Events line 4641, Actions line 4773.

<a id="trigger-094d93dc"></a>

### 37. Unlock Input 3 - 094D93DC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Unlock Input 2 (094DE03C)](#trigger-094de03c).

Attached scope: tag definitions 094D9D4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “--Battle Control Online--” (MISSION:ALL01q).
2. Play sound MessageText.
3. Play voice notification EVA_BattlefieldControlOnline.
4. Enable player input.
5. Enable and reset applicable timers for [Unlock Input 4 (0978603C)](#trigger-0978603c).
6. Reveal terrain around waypoint 50 (cell 63, 108).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4510, Events line 4642, Actions line 4774.

<a id="trigger-0978603c"></a>

### 38. Unlock Input 4 - 0978603C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Unlock Input 3 (094D93DC)](#trigger-094d93dc).

Attached scope: tag definitions 0978D04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound TanyaAttackCommand.
2. Flash team [Player - Tanya1 (094F68EC)](all01t-teams.md#team-094f68ec) with duration setting 120.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4511, Events line 4643, Actions line 4775.

<a id="trigger-073fe71c"></a>

### 39. Change House 3 - 073FE71C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 073FF2CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4512, Events line 4644, Actions line 4776.

<a id="trigger-075f22ec"></a>

### 40. Mission Victory - 075F22EC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Victory (07506C5C)](#trigger-07506c5c).

Attached scope: tag definitions 075F535C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4513, Events line 4645, Actions line 4777.

<a id="trigger-07506c5c"></a>

### 41. Enable Victory - 07506C5C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09F48B6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Mission Victory (075F22EC)](#trigger-075f22ec).
2. Disable [Objective 3 (08A6E100)](#trigger-08a6e100).
3. Disable [Paratroopers 1 (0799590C)](#trigger-0799590c).
4. Disable [Objective 2 (0874286C)](#trigger-0874286c).
5. Play voice notification EVA_PrimaryObjectiveAchieved.
6. Disable [AllyUnderAttack (0945BF3C)](#trigger-0945bf3c).
7. Disable [AllyUnderAttack2 (0945E7BC)](#trigger-0945e7bc).
8. Disable [AllyUnderAttack3 (094160BC)](#trigger-094160bc).
9. Disable [AllyUnderAttack4 (09415BAC)](#trigger-09415bac).
10. Enable and reset applicable timers for [Cheer (08BBBDBC)](#trigger-08bbbdbc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4514, Events line 4646, Actions line 4778.

<a id="trigger-0945bf3c"></a>

### 42. AllyUnderAttack - 0945BF3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AllyUnderAttack2 (0945E7BC)](#trigger-0945e7bc).

Attached scope: Building (CAPARS04), owner Other1 House, cell (87, 45), tag 0945AA7C, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create radar-event marker type 3 at waypoint 96 (cell 90, 46).
2. Enable and reset applicable timers for [AllyUnderAttack2 (0945E7BC)](#trigger-0945e7bc).
3. Disable [AllyUnderAttack (0945BF3C)](#trigger-0945bf3c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4515, Events line 4647, Actions line 4779.

<a id="trigger-0945e7bc"></a>

### 43. AllyUnderAttack2 - 0945E7BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AllyUnderAttack (0945BF3C)](#trigger-0945bf3c).

Attached scope: tag definitions 0945BA3C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [AllyUnderAttack (0945BF3C)](#trigger-0945bf3c).
2. Disable [AllyUnderAttack2 (0945E7BC)](#trigger-0945e7bc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4516, Events line 4648, Actions line 4780.

<a id="trigger-094160bc"></a>

### 44. AllyUnderAttack3 - 094160BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AllyUnderAttack4 (09415BAC)](#trigger-09415bac).

Attached scope: Building (CANEWY12), owner Civie1 House, cell (67, 50), tag 094119FC, persistence mode 2.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create radar-event marker type 3 at waypoint 52 (cell 67, 53).
2. Enable and reset applicable timers for [AllyUnderAttack4 (09415BAC)](#trigger-09415bac).
3. Disable [AllyUnderAttack3 (094160BC)](#trigger-094160bc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4517, Events line 4649, Actions line 4781.

<a id="trigger-09415bac"></a>

### 45. AllyUnderAttack4 - 09415BAC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AllyUnderAttack3 (094160BC)](#trigger-094160bc).

Attached scope: tag definitions 0941312C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [AllyUnderAttack3 (094160BC)](#trigger-094160bc).
2. Disable [AllyUnderAttack4 (09415BAC)](#trigger-09415bac).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4518, Events line 4650, Actions line 4782.

<a id="trigger-08bbbdbc"></a>

### 46. Cheer - 08BBBDBC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Victory (07506C5C)](#trigger-07506c5c).

Attached scope: tag definitions 08BBB60C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4519, Events line 4651, Actions line 4783.

<a id="trigger-08b9bc5c"></a>

### 47. Mission Failed - 08B9BC5C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Failure b (0B1C7E9C)](#trigger-0b1c7e9c); enable from [Enable Failure 2 (0A1C1330)](#trigger-0a1c1330); enable from [Enable Failure 3b (0B532E5C)](#trigger-0b532e5c).

Attached scope: tag definitions 08B9B71C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4520, Events line 4652, Actions line 4784.

<a id="trigger-08b9b62c"></a>

### 48. Enable Failure - 08B9B62C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tanya (TANY), owner Player House, cell (62, 108), tag 08B9B35C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Enable Failure b (0B1C7E9C)](#trigger-0b1c7e9c).
2. Play voice notification Mis_A1_EvaTanyaDeath.
3. Display message “Tanya has died - CRITICAL UNIT LOST” (MISSION:All05k).
4. Play sound MessageText.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4521, Events line 4653, Actions line 4785.

<a id="trigger-0b1c7e9c"></a>

### 49. Enable Failure b - 0B1C7E9C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Failure (08B9B62C)](#trigger-08b9b62c).

Attached scope: tag definitions 07BFF8DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Mission Failed (08B9BC5C)](#trigger-08b9bc5c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4522, Events line 4654, Actions line 4786.

<a id="trigger-09fabf3c"></a>

### 50. Create Crates - 09FABF3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09FAB76C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create crate type 10 at waypoint 8 (cell 81, 67).
2. Create crate type 2 at waypoint 5 (cell 81, 68).
3. Create crate type 9 at waypoint 21 (cell 22, 62).
4. Create crate type 11 at waypoint 7 (cell 22, 49).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4523, Events line 4655, Actions line 4787.

<a id="trigger-09fad67c"></a>

### 51. Bonus Crate 2 - 09FAD67C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09FAD22C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Bonus Crate 2b (079E5F3C)](#trigger-079e5f3c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4524, Events line 4656, Actions line 4788.

<a id="trigger-079e5f3c"></a>

### 52. Bonus Crate 2b - 079E5F3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bonus Crate 2 (09FAD67C)](#trigger-09fad67c).

Attached scope: tag definitions 079E7F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create crate type 10 at waypoint 29 (cell 62, 39).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4525, Events line 4657, Actions line 4789.

<a id="trigger-0733a6cc"></a>

### 53. Enable Conscript Attack - 0733A6CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0733A1AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Start Conscripts Attacking (07A707CC)](#trigger-07a707cc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4526, Events line 4658, Actions line 4790.

<a id="trigger-0a1c1330"></a>

### 54. Enable Failure 2 - 0A1C1330

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Statue of Liberty (CANEWY04), owner Other1 House, cell (61, 69), tag 0A1C2220, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable player input.
2. Move the camera to waypoint 0 (cell 62, 71) with speed setting 3.
3. Play voice notification EVA_CriticalStrucureLost.
4. Create radar-event marker type 3 at waypoint 33 (cell 60, 79).
5. Enable and reset applicable timers for [Mission Failed (08B9BC5C)](#trigger-08b9bc5c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4527, Events line 4659, Actions line 4791.

<a id="trigger-08bd5090"></a>

### 55. Initial Audio - 08BD5090

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08BD00A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_A1_EvaProtectStatue.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4528, Events line 4660, Actions line 4792.

<a id="trigger-072bf2d0"></a>

### 56. Bridge Destroyed - 072BF2D0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Building does not exist: type index 3 (global list position: Allied Barracks (GAPILE)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Mis_A1_EvaRepairBridge.
2. Create radar-event marker type 1 at waypoint 35 (cell 82, 51).
3. Display message “HINT: Construct a BARRACKS in order to produce ENGINEERS to repair the bridge” (MISSION:ALL01f).
4. Flash cameo/type 367; additional configured duration/location argument 120.
5. Switch the sidebar to tab 0.
6. Enable and reset applicable timers for [Bridge Hut Anim (0B4691FC)](#trigger-0b4691fc).
7. Enable and reset applicable timers for [Repair Bridge Hint (0CD4066C)](#trigger-0cd4066c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4529, Events line 4661, Actions line 4793.

<a id="trigger-0b4691fc"></a>

### 57. Bridge Hut Anim - 0B4691FC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge Destroyed (072BF2D0)](#trigger-072bf2d0); enable from [BridgeDestroyedB (09F0151C)](#trigger-09f0151c); enable from [Hint: Engineer 3 (0B4155CC)](#trigger-0b4155cc).

Attached scope: tag definitions 0B46AB0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play Anim At; main setting 479; location/duration field BE.
2. Play Anim At; main setting 479; location/duration field BH.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4530, Events line 4662, Actions line 4794.

<a id="trigger-0cd4066c"></a>

### 58. Repair Bridge Hint - 0CD4066C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Bridge Destroyed (072BF2D0)](#trigger-072bf2d0); enable from [BridgeDestroyedB (09F0151C)](#trigger-09f0151c).

Attached scope: tag definitions 0CD45E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 56 (cell 79, 47).
2. Display message “HINT: Construct a BARRACKS in order to produce ENGINEERS to repair the bridge” (MISSION:All01f).
3. Play sound MessageText.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4531, Events line 4663, Actions line 4795.

<a id="trigger-08cdd540"></a>

### 59. Urban Combat Hint - 08CDD540

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08CD8640 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 17 (cell 39, 39).
2. Play voice notification Mis_A1_EvaUrbanWarning.
3. Display message “HINT: Order your CONSCRIPTS to enter CIVILIAN BUILDINGS to fortify them” (MISSION:Sov1c).
4. Play sound MessageText.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4532, Events line 4664, Actions line 4796.

<a id="trigger-07b92f3c"></a>

### 60. Objective 1 Complete - 07B92F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B9329C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “Objective 1 Complete” (MISSION:Objective1).
3. Play voice notification EVA_PrimaryObjectiveAchieved.
4. Disable [Objective 1 (076F572C)](#trigger-076f572c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4533, Events line 4665, Actions line 4797.

<a id="trigger-07bc399c"></a>

### 61. Reveal Enemy Base - 07BC399C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07BC2F0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 32 (cell 96, 71).
2. Play sound MessageText.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4534, Events line 4666, Actions line 4798.

<a id="trigger-08f8484c"></a>

### 62. Disable Bridge Destroyed - 08F8484C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Bridge Repair Hut (CABHUT), owner Civie1 House, cell (80, 48), tag 08F8706C, persistence mode 0; Bridge Repair Hut (CABHUT), owner Civie1 House, cell (84, 48), tag 08F8706C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Disable [Bridge Destroyed (072BF2D0)](#trigger-072bf2d0).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
4. Disable [BridgeDestroyedB (09F0151C)](#trigger-09f0151c).
5. Destroy current instances of [Bridge Hut Anim (0B4691FC)](#trigger-0b4691fc).
6. Disable [Repair Bridge Hint (0CD4066C)](#trigger-0cd4066c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4535, Events line 4667, Actions line 4799.

<a id="trigger-09f0151c"></a>

### 63. BridgeDestroyedB - 09F0151C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Bridge Destroyed (072BF2D0)](#trigger-072bf2d0).

Attached scope: 10 tagged map cells: (82, 49), (83, 49), (81, 50), (82, 50), (83, 50), (81, 51), (82, 51), (83, 51), (82, 52), (83, 52); tag 072BAD70, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Building exists: type index 3 (global list position: Allied Barracks (GAPILE)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Display message “HINT: Order an ENGINEER into the BRIDGE HUT to repair the bridge” (MISSION:Sov1b).
2. Play voice notification Mis_A1_EvaRepairBridge.
3. Create radar-event marker type 1 at waypoint 35 (cell 82, 51).
4. Switch the sidebar to tab 2.
5. Flash cameo/type 367; additional configured duration/location argument 120.
6. Enable and reset applicable timers for [Bridge Hut Anim (0B4691FC)](#trigger-0b4691fc).
7. Enable and reset applicable timers for [Repair Bridge Hint (0CD4066C)](#trigger-0cd4066c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4536, Events line 4668, Actions line 4800.

<a id="trigger-09eac42c"></a>

### 64. Start Ambient Sounds - 09EAC42C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09EADB4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 1 (cell 62, 90).
2. Play sound _Amb_BirdsHarbor at waypoint 38 (cell 37, 82).
3. Play sound _Amb_BirdsHarbor at waypoint 39 (cell 75, 85).
4. Play sound _Amb_OceanHeavy at waypoint 40 (cell 79, 69).
5. Play sound _Amb_OceanHeavy at waypoint 41 (cell 39, 82).
6. Play sound _Amb_BirdsHarbor at waypoint 42 (cell 40, 52).
7. Play sound _Amb_BirdsHarbor at waypoint 43 (cell 38, 82).
8. Play sound _Amb_OceanLight at waypoint 44 (cell 62, 13).
9. Play sound _Amb_OceanHeavy at waypoint 45 (cell 34, 61).
10. Play sound _Amb_UrbanMurmur2 at waypoint 42 (cell 40, 52).
11. Play sound _Amb_UrbanMurmur2 at waypoint 91 (cell 33, 73).
12. Play sound _Amb_UrbanMurmur1 at waypoint 21 (cell 22, 62).
13. Play sound _Amb_UrbanMurmur2 at waypoint 7 (cell 22, 49).
14. Play sound _Amb_BirdsHarbor at waypoint 36 (cell 60, 99).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4537, Events line 4669, Actions line 4801.

<a id="trigger-0746d0cc"></a>

### 65. Hint: Explosive Barrels - 0746D0CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 6 tagged map cells: (81, 54), (82, 54), (83, 54), (81, 55), (82, 55), (83, 55); tag 0746E5CC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Play voice notification Mis_A1_EvaBarrelWarning.
2. Reveal terrain around waypoint 47 (cell 86, 61).
3. Create radar-event marker type 1 at waypoint 47 (cell 86, 61).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4538, Events line 4670, Actions line 4802.

<a id="trigger-07b3327c"></a>

### 66. Reveal Bonus 1 - 07B3327C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 31 tagged map cells: (63, 14), (63, 15), (63, 16), (50, 17), (63, 17), (50, 18), (63, 18), (50, 19), (63, 19), (50, 20), (63, 20), (50, 21), (63, 21), (50, 22), (63, 22), (50, 23), (63, 23), (50, 24), (51, 24), (52, 24), (53, 24), (54, 24), (55, 24), (56, 24), (57, 24), (58, 24), (59, 24), (60, 24), (61, 24), (62, 24), (63, 24); tag 07B34BFC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 28 (cell 57, 18).
2. Play sound Bonus.
3. Display message “Allied patrol discovered” (MISSION:All05g).
4. Create radar-event marker type 1 at waypoint 28 (cell 57, 18).
5. Enable and reset applicable timers for [Reveal Bonus 2 (07B37EDC)](#trigger-07b37edc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4539, Events line 4671, Actions line 4803.

<a id="trigger-07b37edc"></a>

### 67. Reveal Bonus 2 - 07B37EDC

Owner reference: Other2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reveal Bonus 1 (07B3327C)](#trigger-07b3327c).

Attached scope: tag definitions 07B37B4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_A5_AllSoldier3.
2. Enable and reset applicable timers for [Change House 4 (0B22DE4C)](#trigger-0b22de4c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4540, Events line 4672, Actions line 4804.

<a id="trigger-0b22de4c"></a>

### 68. Change House 4 - 0B22DE4C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reveal Bonus 2 (07B37EDC)](#trigger-07b37edc).

Attached scope: Grizzly Battle Tank (MTNK), owner Civie1 House, cell (55, 18), tag 0B2295AC, persistence mode 0; Grizzly Battle Tank (MTNK), owner Civie1 House, cell (59, 18), tag 0B2295AC, persistence mode 0; Grizzly Battle Tank (MTNK), owner Civie1 House, cell (57, 18), tag 0B2295AC, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4541, Events line 4673, Actions line 4805.

<a id="trigger-07b376bc"></a>

### 69. Hint: Seals - 07B376BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B3714C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “HINT: Seals can SWIM and PLANT C4 like Tanya” (MISSION:All01l).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4542, Events line 4674, Actions line 4806.

<a id="trigger-07478f3c"></a>

### 70. Hint: Cars - 07478F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0747889C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “HINT: Cars can be used to CARRY INFANTRY. To remove passengers, double-click on the car” (MISSION:All01m).
3. Create radar-event marker type 1 at waypoint 46 (cell 57, 40).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4543, Events line 4675, Actions line 4807.

<a id="trigger-07ba127c"></a>

### 71. Hint: Barracks - 07BA127C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07BA067C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 3 (global list position: Allied Barracks (GAPILE)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Barracks 2 (0747A7BC)](#trigger-0747a7bc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4544, Events line 4676, Actions line 4808.

<a id="trigger-0747a7bc"></a>

### 72. Hint: Barracks 2 - 0747A7BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: Barracks (07BA127C)](#trigger-07ba127c).

Attached scope: tag definitions 0747FF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash cameo/type 367; additional configured duration/location argument 90.
2. Switch the sidebar to tab 3.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4545, Events line 4677, Actions line 4809.

<a id="trigger-07ba8c2c"></a>

### 73. Initial Paratroopers 1 - 07BA8C2C

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 4 tagged map cells: (61, 84), (62, 84), (63, 84), (64, 84); tag 07BA863C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [Initial Paratroopers 1 (09A92A9C)](all01t-teams.md#team-09a92a9c).
2. Supply reinforcement team [Initial Paratroopers 2 (09A925EC)](all01t-teams.md#team-09a925ec).
3. Enable and reset applicable timers for [Initial Paratroopers 1b (07BB828C)](#trigger-07bb828c).
4. Supply reinforcement team [Initial Paratroopers 3 (09A9227C)](all01t-teams.md#team-09a9227c).
5. Enable and reset applicable timers for [Enable - Enable V3 - Liberty (0AE1890C)](#trigger-0ae1890c).
6. Enable and reset applicable timers for [Enable GI's (07428AAC)](#trigger-07428aac).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4546, Events line 4678, Actions line 4810.

<a id="trigger-07bb828c"></a>

### 74. Initial Paratroopers 1b - 07BB828C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Initial Paratroopers 1 (07BA8C2C)](#trigger-07ba8c2c).

Attached scope: tag definitions 07BB9B1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 34 (cell 62, 65).
2. Create radar-event marker type 5 at waypoint 34 (cell 62, 65).
3. Play sound AirRaidSiren.
4. Display message “WARNING: Soviet PARATROOPERS are incoming” (MISSION:All01i).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4547, Events line 4679, Actions line 4811.

<a id="trigger-0ae1890c"></a>

### 75. Enable - Enable V3 - Liberty - 0AE1890C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Initial Paratroopers 1 (07BA8C2C)](#trigger-07ba8c2c).

Attached scope: tag definitions 0AE1870C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [V3 - Attacks Liberty (0AE8203C)](#trigger-0ae8203c).
2. Enable and reset applicable timers for [Play Statue Movie (0B3E99EC)](#trigger-0b3e99ec).
3. Disable [Enable Failure 2 (0A1C1330)](#trigger-0a1c1330).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4548, Events line 4680, Actions line 4812.

<a id="trigger-0ae8203c"></a>

### 76. V3 - Attacks Liberty - 0AE8203C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable - Enable V3 - Liberty (0AE1890C)](#trigger-0ae1890c); enable from [Enable V3 - Attacks Liberty (0AE18F3C)](#trigger-0ae18f3c).

Attached scope: tag definitions 0AE7D04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [V3 - Liberty (0AE2849C)](all01t-teams.md#team-0ae2849c) at waypoint 82 (cell 77, 68).
2. Enable and reset applicable timers for [Reveal V3 (07BBA03C)](#trigger-07bba03c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4549, Events line 4681, Actions line 4813.

<a id="trigger-0b3e99ec"></a>

### 77. Play Statue Movie - 0B3E99EC

Owner reference: Other1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable - Enable V3 - Liberty (0AE1890C)](#trigger-0ae1890c).

Attached scope: tag definitions 09DB739C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 79 (global list position: Statue of Liberty (CANEWY04)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Play Soviet Movie 2 (081A1B4C)](#trigger-081a1b4c).
2. Create radar-event marker type 0 at waypoint 0 (cell 62, 71).
3. Enable and reset applicable timers for [Create Harriers b (0B53F83C)](#trigger-0b53f83c).
4. Enable and reset applicable timers for [Enable Retreat (0B536C2C)](#trigger-0b536c2c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4550, Events line 4682, Actions line 4814.

<a id="trigger-07bba03c"></a>

### 78. Reveal V3 - 07BBA03C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [V3 - Attacks Liberty (0AE8203C)](#trigger-0ae8203c).

Attached scope: tag definitions 07BDE0CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 40 (cell 79, 69).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4551, Events line 4683, Actions line 4815.

<a id="trigger-081a1b4c"></a>

### 79. Play Soviet Movie 2 - 081A1B4C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Play Statue Movie (0B3E99EC)](#trigger-0b3e99ec).

Attached scope: tag definitions 081A152C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 67.
2. Enable and reset applicable timers for [Enable Objective 2b (0782DA30)](#trigger-0782da30).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4552, Events line 4684, Actions line 4816.

<a id="trigger-0b53f83c"></a>

### 80. Create Harriers b - 0B53F83C

Owner reference: Other2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Create Harriers 1 (09D36F3C)](#trigger-09d36f3c).

Incoming activation links: enable from [Play Statue Movie (0B3E99EC)](#trigger-0b3e99ec).

Attached scope: 2 tagged map cells: (55, 69), (55, 70); tag 09D3664C, persistence mode 0.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Harrier 1 (0A68093C)](all01t-teams.md#team-0a68093c) at waypoint 71 (cell 32, 69).
2. Supply reinforcement team [Harrier 1 (0A68093C)](all01t-teams.md#team-0a68093c) at waypoint 72 (cell 32, 67).
3. Supply reinforcement team [Harrier 1 (0A68093C)](all01t-teams.md#team-0a68093c) at waypoint 70 (cell 34, 68).
4. Play sound IntruderTakeOff.
5. Enable and reset applicable timers for [Harriers Talk (0803EA6C)](#trigger-0803ea6c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4553, Events line 4685, Actions line 4817.

<a id="trigger-0b536c2c"></a>

### 81. Enable Retreat - 0B536C2C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Play Statue Movie (0B3E99EC)](#trigger-0b3e99ec).

Attached scope: tag definitions 0B536A2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Dreadnought Retreat (0B52B86C)](#trigger-0b52b86c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4554, Events line 4686, Actions line 4818.

<a id="trigger-09d36f3c"></a>

### 82. Create Harriers 1 - 09D36F3C

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [Harrier 1 (0A68093C)](all01t-teams.md#team-0a68093c) at waypoint 71 (cell 32, 69).
2. Supply reinforcement team [Harrier 1 (0A68093C)](all01t-teams.md#team-0a68093c) at waypoint 72 (cell 32, 67).
3. Supply reinforcement team [Harrier 1 (0A68093C)](all01t-teams.md#team-0a68093c) at waypoint 70 (cell 34, 68).
4. Play sound IntruderTakeOff.
5. Enable and reset applicable timers for [Harriers Talk (0803EA6C)](#trigger-0803ea6c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4555, Events line 4687, Actions line 4819.

<a id="trigger-0803ea6c"></a>

### 83. Harriers Talk - 0803EA6C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create Harriers b (0B53F83C)](#trigger-0b53f83c); enable from [Create Harriers 1 (09D36F3C)](#trigger-09d36f3c).

Attached scope: tag definitions 0803E5EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound IntruderAttackCommand.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4556, Events line 4688, Actions line 4820.

<a id="trigger-0b52b86c"></a>

### 84. Dreadnought Retreat - 0B52B86C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Retreat (0B536C2C)](#trigger-0b536c2c).

Attached scope: tag definitions 0B52740C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [BG1 - Dreadnought 1 (0A67F6CC)](all01t-teams.md#team-0a67f6cc).
2. Create/recruit team [Dreadnought Retreat (0B533EFC)](all01t-teams.md#team-0b533efc).
3. Create/recruit team [Dreadnought Retreat (0B533EFC)](all01t-teams.md#team-0b533efc).
4. Create/recruit team [Dreadnought Retreat (0B533EFC)](all01t-teams.md#team-0b533efc).
5. Create/recruit team [Dreadnought Retreat (0B533EFC)](all01t-teams.md#team-0b533efc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4557, Events line 4689, Actions line 4821.

<a id="trigger-0ae18f3c"></a>

### 85. Enable V3 - Attacks Liberty - 0AE18F3C

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE189FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  All: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [V3 - Attacks Liberty (0AE8203C)](#trigger-0ae8203c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4558, Events line 4690, Actions line 4822.

<a id="trigger-0a95e10c"></a>

### 86. Select Building 1 - 0A95E10C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Select Buildings (0A94FE9C)](#trigger-0a94fe9c).

Attached scope: tag definitions 0A95F8DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “HINT: To REMOVE your troops, DOUBLE-CLICK on the occupied building” (MISSION:All01s).
3. Create radar-event marker type 1 at waypoint 51 (cell 77, 58).
4. Disable [Select Building 2 (07D0BE1C)](#trigger-07d0be1c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4559, Events line 4691, Actions line 4823.

<a id="trigger-07d0be1c"></a>

### 87. Select Building 2 - 07D0BE1C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Select Buildings (0A94FE9C)](#trigger-0a94fe9c).

Attached scope: tag definitions 07D0B47C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “HINT: To REMOVE your troops, DOUBLE-CLICK on the occupied building” (MISSION:All01s).
3. Create radar-event marker type 1 at waypoint 52 (cell 67, 53).
4. Disable [Select Building 1 (0A95E10C)](#trigger-0a95e10c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4560, Events line 4692, Actions line 4824.

<a id="trigger-0a94fe9c"></a>

### 88. Enable Select Buildings - 0A94FE9C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A94F7FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 112 (global list position: Building (CAWASH11)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Select Building 1 (0A95E10C)](#trigger-0a95e10c).
2. Enable and reset applicable timers for [Select Building 2 (07D0BE1C)](#trigger-07d0be1c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4561, Events line 4693, Actions line 4825.

<a id="trigger-0a8c247c"></a>

### 89. Hint: Production - 0A8C247C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A8C3F1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 3 (global list position: Allied Barracks (GAPILE)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Production 2 (0A8C3E2C)](#trigger-0a8c3e2c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4562, Events line 4694, Actions line 4826.

<a id="trigger-0a8c3e2c"></a>

### 90. Hint: Production 2 - 0A8C3E2C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: Production (0A8C247C)](#trigger-0a8c247c).

Attached scope: tag definitions 0A8C3B7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “HINT: Select the infantry TAB to view additional PRODUCTION OPTIONS” (MISSION:All01o).
3. Flash cameo/type 358; additional configured duration/location argument 60.
4. Switch the sidebar to tab 2.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4563, Events line 4695, Actions line 4827.

<a id="trigger-07b9d89c"></a>

### 91. Hint: Engineer 2 - 07B9D89C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: Engineer 1 (0B415B3C)](#trigger-0b415b3c).

Attached scope: tag definitions 07B9D30C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Engineer (09F0AEFC)](all01t-teams.md#team-09f0aefc).
2. Flash team [Engineer (09F0AEFC)](all01t-teams.md#team-09f0aefc) with duration setting 90.
3. Play voice notification Unit_Eva_Engineer.
4. Enable and reset applicable timers for [Hint: Engineer 3 (0B4155CC)](#trigger-0b4155cc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4564, Events line 4696, Actions line 4828.

<a id="trigger-0b4155cc"></a>

### 92. Hint: Engineer 3 - 0B4155CC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: Engineer 2 (07B9D89C)](#trigger-07b9d89c).

Attached scope: tag definitions 0B4153CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 11 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “HINT: Order your ENGINEER into one of the REPAIR HUTS in order to fix the bridge” (MISSION:All01p).
2. Play sound MessageText.
3. Create radar-event marker type 1 at waypoint 56 (cell 79, 47).
4. Create radar-event marker type 1 at waypoint 59 (cell 83, 47).
5. Enable and reset applicable timers for [Bridge Hut Anim (0B4691FC)](#trigger-0b4691fc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4565, Events line 4697, Actions line 4829.

<a id="trigger-0a8dd70c"></a>

### 93. Hint: Harvester - 0A8DD70C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A8DEDFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “HINT: Chrono Harvesters HARVEST ore and then automatically TELEPORT back to their refinery” (MISSION:All01n).
3. Remove instances of the team organization (not automatically its surviving objects) [Chrono Harvester (1) (0831459C)](all01t-teams.md#team-0831459c).
4. Enable and reset applicable timers for [Hint: Harvester 2 (0A6BB12C)](#trigger-0a6bb12c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4566, Events line 4698, Actions line 4830.

<a id="trigger-0a6bb12c"></a>

### 94. Hint: Harvester 2 - 0A6BB12C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint: Harvester (0A8DD70C)](#trigger-0a8dd70c).

Attached scope: tag definitions 0A6C566C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Chrono Harvester Flash (0A967EFC)](all01t-teams.md#team-0a967efc).
2. Flash team [Chrono Harvester Flash (0A967EFC)](all01t-teams.md#team-0a967efc) with duration setting 90.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4567, Events line 4699, Actions line 4831.

<a id="trigger-0baf38bc"></a>

### 95. Car1 - 0BAF38BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BAF337C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Car 1b (0BAFB15C)](#trigger-0bafb15c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4568, Events line 4700, Actions line 4832.

<a id="trigger-0bafb15c"></a>

### 96. Car 1b - 0BAFB15C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Car1 (0BAF38BC)](#trigger-0baf38bc).

Attached scope: tag definitions 0BAFCC5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4569, Events line 4701, Actions line 4833.

<a id="trigger-0baf328c"></a>

### 97. Car 2 - 0BAF328C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BAF4E9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Car 2b (03ED228C)](#trigger-03ed228c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4570, Events line 4702, Actions line 4834.

<a id="trigger-03ed228c"></a>

### 98. Car 2b - 03ED228C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Car 2 (0BAF328C)](#trigger-0baf328c).

Attached scope: tag definitions 03ED3D2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4571, Events line 4703, Actions line 4835.

<a id="trigger-07a3789c"></a>

### 99. Enemy Paratroopers - 07A3789C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 40 tagged map cells: (24, 39), (25, 39), (25, 40), (26, 40), (26, 41), (27, 41), (27, 42), (28, 42), (28, 43), (29, 43), (29, 44), (30, 44), (30, 45), (31, 45), (30, 46), (30, 47), (30, 48), (30, 49), (31, 49), (32, 49), (33, 49), (34, 49), (34, 50), (35, 50), (36, 50), (37, 50), (37, 51), (37, 52), (38, 52), (39, 52), (40, 52), (41, 52), (42, 52), (43, 52), (44, 52), (44, 53), (44, 54), (44, 55), (44, 56), (45, 56); tag 07A3999C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Enable Paratroopers 1 (09C1A03C)](#trigger-09c1a03c).
2. Enable and reset applicable timers for [Enable Paratroopers 2 (09C2803C)](#trigger-09c2803c).
3. Enable and reset applicable timers for [Enable Paratroopers 3 (09C2E03C)](#trigger-09c2e03c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4572, Events line 4704, Actions line 4836.

<a id="trigger-09c1a03c"></a>

### 100. Enable Paratroopers 1 - 09C1A03C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enemy Paratroopers (07A3789C)](#trigger-07a3789c).

Attached scope: tag definitions 09C1203C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 25 (cell 39, 36).
2. Enable and reset applicable timers for [Paratroopers 1 (0799590C)](#trigger-0799590c).
3. Supply reinforcement team [BG1 - Paratroopers1 (0AC446AC)](all01t-teams.md#team-0ac446ac).
4. Supply reinforcement team [BG1 - Paratroopers2 (0AC42B7C)](all01t-teams.md#team-0ac42b7c).
5. Create radar-event marker type 5 at waypoint 17 (cell 39, 39).
6. Display message “WARNING: Soviet PARATROOPERS are incoming” (MISSION:All01i).
7. Play sound AirRaidSiren.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4573, Events line 4705, Actions line 4837.

<a id="trigger-09c2803c"></a>

### 101. Enable Paratroopers 2 - 09C2803C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enemy Paratroopers (07A3789C)](#trigger-07a3789c).

Attached scope: tag definitions 09C1804C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Paratroopers 2 (09BC303C)](#trigger-09bc303c).
2. Reveal terrain around waypoint 25 (cell 39, 36).
3. Play sound AirRaidSiren.
4. Display message “WARNING: Soviet PARATROOPERS are incoming” (MISSION:All01i).
5. Create radar-event marker type 5 at waypoint 17 (cell 39, 39).
6. Supply reinforcement team [BG1 - Paratroopers1 (0AC446AC)](all01t-teams.md#team-0ac446ac).
7. Supply reinforcement team [BG1 - Paratroopers2 (0AC42B7C)](all01t-teams.md#team-0ac42b7c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4574, Events line 4706, Actions line 4838.

<a id="trigger-09c2e03c"></a>

### 102. Enable Paratroopers 3 - 09C2E03C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enemy Paratroopers (07A3789C)](#trigger-07a3789c).

Attached scope: tag definitions 09C3904C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 25 (cell 39, 36).
2. Enable and reset applicable timers for [Paratroopers 3 (09E7118C)](#trigger-09e7118c).
3. Supply reinforcement team [BG1 - Paratroopers1 (0AC446AC)](all01t-teams.md#team-0ac446ac).
4. Supply reinforcement team [BG1 - Paratroopers2 (0AC42B7C)](all01t-teams.md#team-0ac42b7c).
5. Display message “WARNING: Soviet PARATROOPERS are incoming” (MISSION:All01i).
6. Create radar-event marker type 5 at waypoint 17 (cell 39, 39).
7. Play sound AirRaidSiren.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4575, Events line 4707, Actions line 4839.

<a id="trigger-09bc303c"></a>

### 103. Paratroopers 2 - 09BC303C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Paratroopers 2 (09C2803C)](#trigger-09c2803c).

Attached scope: tag definitions 09E6DBAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 130 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 - Paratroopers1 (0AC446AC)](all01t-teams.md#team-0ac446ac).
2. Supply reinforcement team [BG1 - Paratroopers2 (0AC42B7C)](all01t-teams.md#team-0ac42b7c).
3. Play sound AirRaidSiren.
4. Create radar-event marker type 5 at waypoint 17 (cell 39, 39).
5. Display message “WARNING: Soviet PARATROOPERS are incoming” (MISSION:All01i).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4576, Events line 4708, Actions line 4840.

<a id="trigger-09e7118c"></a>

### 104. Paratroopers 3 - 09E7118C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Paratroopers 3 (09C2E03C)](#trigger-09c2e03c).

Attached scope: tag definitions 09E7875C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 - Paratroopers1 (0AC446AC)](all01t-teams.md#team-0ac446ac).
2. Supply reinforcement team [BG1 - Paratroopers2 (0AC42B7C)](all01t-teams.md#team-0ac42b7c).
3. Create radar-event marker type 5 at waypoint 17 (cell 39, 39).
4. Play sound AirRaidSiren.
5. Display message “WARNING: Soviet PARATROOPERS are incoming” (MISSION:All01i).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4577, Events line 4709, Actions line 4841.

<a id="trigger-0b3c062c"></a>

### 105. Create Thugs - 0B3C062C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 4 tagged map cells: (39, 68), (40, 68), (39, 69), (40, 69); tag 0B3C6AEC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [Thugs 1 (0B3C142C)](all01t-teams.md#team-0b3c142c) at waypoint 64 (cell 33, 51).
2. Supply reinforcement team [Thugs 1 (0B3C142C)](all01t-teams.md#team-0b3c142c) at waypoint 65 (cell 24, 58).
3. Enable and reset applicable timers for [Change House 5 (0B3C53BC)](#trigger-0b3c53bc).
4. Enable and reset applicable timers for [Create Cop Car (0B30B03C)](#trigger-0b30b03c).
5. Reveal terrain around waypoint 68 (cell 34, 69).
6. Reveal terrain around waypoint 69 (cell 34, 62).
7. Create radar-event marker type 0 at waypoint 63 (cell 32, 59).
8. Enable and reset applicable timers for [Enable Traffic 1 (0B8E6ADC)](#trigger-0b8e6adc).
9. Enable and reset applicable timers for [Enable Traffic 2 (0B8E616C)](#trigger-0b8e616c).
10. Reshroud Map At; main setting 5; location/duration field F.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4578, Events line 4710, Actions line 4842.

<a id="trigger-0b3c53bc"></a>

### 106. Change House 5 - 0B3C53BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create Thugs (0B3C062C)](#trigger-0b3c062c).

Attached scope: GI (E1), owner Other1 House, cell (31, 59), tag 0B3C51BC, persistence mode 0; GI (E1), owner Other1 House, cell (32, 59), tag 0B3C51BC, persistence mode 0.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4579, Events line 4711, Actions line 4843.

<a id="trigger-0b30b03c"></a>

### 107. Create Cop Car - 0B30B03C

Owner reference: Other1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create Thugs (0B3C062C)](#trigger-0b3c062c).

Attached scope: tag definitions 0B31504C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Cop 1 (0A71FB7C)](all01t-teams.md#team-0a71fb7c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4580, Events line 4712, Actions line 4844.

<a id="trigger-0b8e6adc"></a>

### 108. Enable Traffic 1 - 0B8E6ADC

Owner reference: Civilian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create Thugs (0B3C062C)](#trigger-0b3c062c).

Attached scope: tag definitions 0B8E625C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Traffic 1 (0B8EDA2C)](#trigger-0b8eda2c).
2. Supply reinforcement team [Traffic 1 (0A71B33C)](all01t-teams.md#team-0a71b33c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4581, Events line 4713, Actions line 4845.

<a id="trigger-0b8e616c"></a>

### 109. Enable Traffic 2 - 0B8E616C

Owner reference: Civilian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create Thugs (0B3C062C)](#trigger-0b3c062c).

Attached scope: tag definitions 0B8E5E9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 52 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Traffic 2 (0B8ED3FC)](#trigger-0b8ed3fc).
2. Supply reinforcement team [Traffic2 (0A71B20C)](all01t-teams.md#team-0a71b20c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4582, Events line 4714, Actions line 4846.

<a id="trigger-0b8eda2c"></a>

### 110. Traffic 1 - 0B8EDA2C

Owner reference: Civilian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Traffic 1 (0B8E6ADC)](#trigger-0b8e6adc).

Attached scope: tag definitions 0B8ED4EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 110 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Traffic 1 (0A71B33C)](all01t-teams.md#team-0a71b33c) at waypoint 90 (cell 24, 73).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4583, Events line 4715, Actions line 4847.

<a id="trigger-0b8ed3fc"></a>

### 111. Traffic 2 - 0B8ED3FC

Owner reference: Civilian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Traffic 2 (0B8E616C)](#trigger-0b8e616c).

Attached scope: tag definitions 0B8ED1FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 130 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Traffic2 (0A71B20C)](all01t-teams.md#team-0a71b20c) at waypoint 97 (cell 16, 44).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4584, Events line 4716, Actions line 4848.

<a id="trigger-080777bc"></a>

### 112. Break Bridges - 080777BC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08080CFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Apply 100 damage at; main setting 80; location/duration field CC.
2. Apply 100 damage at; main setting 80; location/duration field CC.
3. Apply 100 damage at; main setting 80; location/duration field CC.
4. Apply 100 damage at; main setting 80; location/duration field CC.
5. Apply 100 damage at; main setting 80; location/duration field CC.
6. Apply 100 damage at; main setting 79; location/duration field CB.
7. Apply 100 damage at; main setting 79; location/duration field CB.
8. Apply 100 damage at; main setting 79; location/duration field CB.
9. Apply 100 damage at; main setting 79; location/duration field CB.
10. Apply 100 damage at; main setting 79; location/duration field CB.

Source locator: MAPS02.MIX/all01t.map; Triggers line 4585, Events line 4717, Actions line 4849.

<a id="trigger-0a61df3c"></a>

### 113. Cargo Plane 1 - 0A61DF3C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Cargo 1 (0A63DD1C)](#trigger-0a63dd1c).

Attached scope: tag definitions 0A6300CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 125 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Cargo 1 (0AB088EC)](all01t-teams.md#team-0ab088ec).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4586, Events line 4718, Actions line 4850.

<a id="trigger-0a63d7ec"></a>

### 114. Cargo Plane 2 - 0A63D7EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Cargo 2 (0A63DE5C)](#trigger-0a63de5c).

Attached scope: tag definitions 0A63D2DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 125 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Cargo 2 (0AB0843C)](all01t-teams.md#team-0ab0843c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4587, Events line 4719, Actions line 4851.

<a id="trigger-0a63d1ec"></a>

### 115. Cargo Plane 3 - 0A63D1EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Cargo 3 (0A63EC8C)](#trigger-0a63ec8c).

Attached scope: tag definitions 0A63FEAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 125 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Cargo 4 (0AB147DC)](all01t-teams.md#team-0ab147dc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4588, Events line 4720, Actions line 4852.

<a id="trigger-0a63fdbc"></a>

### 116. Cargo Plane 4 - 0A63FDBC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Cargo 4 (0A63E71C)](#trigger-0a63e71c).

Attached scope: tag definitions 0A63FBBC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 125 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Cargo 3 (0AB17EFC)](all01t-teams.md#team-0ab17efc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4589, Events line 4721, Actions line 4853.

<a id="trigger-0a63dd1c"></a>

### 117. Enable Cargo 1 - 0A63DD1C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A63DA6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Cargo Plane 1 (0A61DF3C)](#trigger-0a61df3c).
2. Supply reinforcement team [Cargo 1 (0AB088EC)](all01t-teams.md#team-0ab088ec) at waypoint 83 (cell 16, 43).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4590, Events line 4722, Actions line 4854.

<a id="trigger-0a63de5c"></a>

### 118. Enable Cargo 2 - 0A63DE5C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A63ED7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 55 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Cargo Plane 2 (0A63D7EC)](#trigger-0a63d7ec).
2. Supply reinforcement team [Cargo 2 (0AB0843C)](all01t-teams.md#team-0ab0843c) at waypoint 85 (cell 82, 96).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4591, Events line 4723, Actions line 4855.

<a id="trigger-0a63ec8c"></a>

### 119. Enable Cargo 3 - 0A63EC8C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A63E80C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Cargo 2 (0AB0843C)](all01t-teams.md#team-0ab0843c) at waypoint 87 (cell 25, 33).
2. Enable and reset applicable timers for [Cargo Plane 3 (0A63D1EC)](#trigger-0a63d1ec).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4592, Events line 4724, Actions line 4856.

<a id="trigger-0a63e71c"></a>

### 120. Enable Cargo 4 - 0A63E71C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A63E29C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Cargo 3 (0AB17EFC)](all01t-teams.md#team-0ab17efc) at waypoint 89 (cell 93, 85).
2. Enable and reset applicable timers for [Cargo Plane 4 (0A63FDBC)](#trigger-0a63fdbc).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4593, Events line 4725, Actions line 4857.

<a id="trigger-0b53665c"></a>

### 121. Enable Failure 3 - 0B53665C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 15 tagged map cells: (80, 90), (81, 90), (79, 91), (80, 91), (78, 92), (79, 92), (77, 93), (78, 93), (76, 94), (77, 94), (75, 95), (76, 95), (74, 96), (75, 96), (82, 96); tag 0B532F4C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Enable Failure 3b (0B532E5C)](#trigger-0b532e5c).
2. Disable [Objective 1 Complete (07B92F3C)](#trigger-07b92f3c).
3. Disable [Objective 1 (076F572C)](#trigger-076f572c).
4. Disable [Objective 2 (0874286C)](#trigger-0874286c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4594, Events line 4726, Actions line 4858.

<a id="trigger-0b532e5c"></a>

### 122. Enable Failure 3b - 0B532E5C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Failure 3 (0B53665C)](#trigger-0b53665c).

Attached scope: tag definitions 0B532A5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Play sound MessageText.
2. Display message “Objective 1: Destroy all four Soviet DREADNOUGHTS” (MISSION:ALL01a).
3. Enable and reset applicable timers for [Mission Failed (08B9BC5C)](#trigger-08b9bc5c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4595, Events line 4727, Actions line 4859.

<a id="trigger-09f7ff3c"></a>

### 123. Start Ambient Sounds 2 - 09F7FF3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09F7F96C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsHarbor at waypoint 41 (cell 39, 82).
2. Play sound _Amb_OceanHeavy at waypoint 22 (cell 47, 71).
3. Play sound _Amb_BirdsTemperate1 at waypoint 33 (cell 60, 79).
4. Play sound _Amb_WindCold at waypoint 0 (cell 62, 71).
5. Play sound _Amb_BirdsHarbor at waypoint 3 (cell 63, 66).
6. Play sound _Amb_OceanLight at waypoint 51 (cell 77, 58).
7. Play sound _Amb_BirdsBeach at waypoint 52 (cell 67, 53).
8. Play sound _Amb_OceanHeavy at waypoint 93 (cell 97, 56).
9. Play sound _Amb_BirdsHarbor at waypoint 95 (cell 87, 56).
10. Play sound _Amb_UrbanMurmur1 at waypoint 32 (cell 96, 71).
11. Play sound _Amb_BirdsPark at waypoint 16 (cell 74, 38).
12. Play sound _Amb_WindCold at waypoint 40 (cell 79, 69).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4596, Events line 4728, Actions line 4860.

<a id="trigger-0a97c4bc"></a>

### 124. Harvester Built - 0A97C4BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A97C11C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Unit Type: type index 33 (global list position: Chrono Miner (CMIN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Create/recruit team [Chrono Harvester (1) (0831459C)](all01t-teams.md#team-0831459c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4597, Events line 4729, Actions line 4861.

<a id="trigger-09d2bcfc"></a>

### 125. Secret Hint - 09D2BCFC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (42, 82); tag 09D3506C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Play sound Bonus.
2. Display message “Hey! You're not supposed to be here!” (MISSION:Sov11e).
3. Create crate type 9 at waypoint 41 (cell 39, 82).
4. Create crate type 11 at waypoint 62 (cell 40, 82).
5. Create crate type 13 at waypoint 43 (cell 38, 82).
6. Create crate type 0 at waypoint 38 (cell 37, 82).
7. Create radar-event marker type 1 at waypoint 62 (cell 40, 82).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4598, Events line 4730, Actions line 4862.

<a id="trigger-0bfd7f3c"></a>

### 126. Crate 1 - 0BFD7F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 8 tagged map cells: (22, 49), (22, 62), (81, 67), (81, 68), (37, 82), (38, 82), (39, 82), (40, 82); tag 0BFD78BC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Display message “Power-up Crate discovered!” (MISSION:Sov11g).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4599, Events line 4731, Actions line 4863.

<a id="trigger-0a7f298c"></a>

### 127. Stop Soviet Sound - 0A7F298C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Soviet Construction Yard (NACNST), owner BadGuy1 House, cell (93, 67), tag 0A7F264C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Stop location sound 32 at waypoint 32 (cell 96, 71).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4600, Events line 4732, Actions line 4864.

<a id="trigger-0b415b3c"></a>

### 128. Hint: Engineer 1 - 0B415B3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B41579C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Infantry Type: type index 3 (global list position: Engineer (ENGINEER)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint: Engineer 2 (07B9D89C)](#trigger-07b9d89c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4601, Events line 4733, Actions line 4865.

<a id="trigger-0860ea2c"></a>

### 129. Transport Retreat 1 - 0860EA2C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0860E82C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Transport 1) is set.

**Then perform these actions in order:**

1. Create/recruit team [Transport 1b (0AB4920C)](all01t-teams.md#team-0ab4920c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4602, Events line 4734, Actions line 4866.

<a id="trigger-0860e73c"></a>

### 130. Transport Retreat 2 - 0860E73C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0860E53C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Transport 2) is set.

**Then perform these actions in order:**

1. Create/recruit team [Transport 2b (0AB4AB7C)](all01t-teams.md#team-0ab4ab7c).

Source locator: MAPS02.MIX/all01t.map; Triggers line 4603, Events line 4735, Actions line 4867.

[All team rosters and ordered plans](all01t-teams.md) | [All mission overrides](all01t-overrides.md)
