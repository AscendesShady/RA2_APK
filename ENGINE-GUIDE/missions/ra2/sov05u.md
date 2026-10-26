# Operation: City of Lights

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov05u.map. **Effective extracted member:** MAPS02.MIX/sov05u.map. **Trigger definitions:** 53.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov05u-teams.md) | [All mission overrides](sov05u-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | URBAN |
| Map size | 0,0,34,66 |
| Visible local rectangle | 2,4,30,56 |
| Placed vehicles | 47 |
| Placed infantry | 50 |
| Placed structures | 150 |
| Placed aircraft | 0 |
| Team templates | 16 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 25 | Player |
| 1 | BadGuy1 House | 100 | BadGuy1 |
| 2 | BadGuy2 House | 100 | BadGuy2 |
| 3 | BadGuy3 House | 0 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 20 | Other1 |
| 6 | Other2 House | 100 | Other2 |
| 7 | Other3 House | 0 | Other3 |

### Local state flags at initialization

No named local flags were found.

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Tower Destroyed Backup (0A70764C)](#trigger-0a70764c) | Building does not exist: type index 104 (global list position: Paris Tower (CAPARS01)). A map-local type-list change can affect index interpretation. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [Win (0A67AC6C)](#trigger-0a67ac6c) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [Player Loses (08AB8D40)](#trigger-08ab8d40) | Destroyed,  All: owner selector 20 (country/type OTHER3; placed owner Other3 House).<br>Building does not exist: type index 11 (global list position: Soviet Barracks (NAHAND)). A map-local type-list change can affect index interpretation. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [Tower Destroyed (0AD6F19C)](#trigger-0ad6f19c) | Destroyed by anything. See attached-object/cell scope below. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-088601b0"></a>

### 1. Reveal Way A - 088601B0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pill Box (GAPILL), owner BadGuy1 House, cell (65, 56), tag 08907F50, persistence mode 0; Building (CAPARS10), owner Civie1 House, cell (61, 63), tag 08907F50, persistence mode 0; Building (CAPARS14), owner Civie1 House, cell (70, 61), tag 08907F50, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 0 (cell 71, 67).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2352, Events line 2407, Actions line 2462.

<a id="trigger-089d6140"></a>

### 2. Reveal Way C - 089D6140

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pickup Truck (PICK), owner Civie1 House, cell (78, 60), tag 089D5B70, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (84, 57), tag 089D5B70, persistence mode 0; Barrel (CAMISC02), owner Civie1 House, cell (81, 64), tag 089D5B70, persistence mode 0; Building (CAPARS05), owner Civie1 House, cell (86, 64), tag 089D5B70, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 2 (cell 85, 66).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2353, Events line 2408, Actions line 2463.

<a id="trigger-089de250"></a>

### 3. Suicide GI - 089DE250

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089DDCD0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Suicide GI (07701760)](sov05u-teams.md#team-07701760).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2354, Events line 2409, Actions line 2464.

<a id="trigger-089ba6a0"></a>

### 4. Suicide Dies - 089BA6A0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089BA130 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 1 (cell 79, 81).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2355, Events line 2410, Actions line 2465.

<a id="trigger-0915f590"></a>

### 5. Tesla Talk - 0915F590

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tesla Selected (087D3A80)](#trigger-087d3a80).

Attached scope: tag definitions 0915F1B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S5_TeslaGuy.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2356, Events line 2411, Actions line 2466.

<a id="trigger-08930180"></a>

### 6. CreateCivCar1Team - 08930180

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 088C9910 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [CivCar1Team (08AB64E0)](sov05u-teams.md#team-08ab64e0).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2357, Events line 2412, Actions line 2467.

<a id="trigger-0844f520"></a>

### 7. CreateCivCar2Team - 0844F520

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0844AF50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [CivCar2Team (076E4560)](sov05u-teams.md#team-076e4560).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2358, Events line 2413, Actions line 2468.

<a id="trigger-089c1f40"></a>

### 8. CreateCivCar3Team - 089C1F40

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089C1B00 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [CivCar3Team (076E41E0)](sov05u-teams.md#team-076e41e0).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2359, Events line 2414, Actions line 2469.

<a id="trigger-088d0a90"></a>

### 9. Reveal Way E - 088D0A90

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAPARS05), owner Civie1 House, cell (73, 87), tag 088D0650, persistence mode 0; Building (CAPARS06), owner Civie1 House, cell (57, 86), tag 088D0650, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 4 (cell 67, 93).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2360, Events line 2415, Actions line 2470.

<a id="trigger-088d00e0"></a>

### 10. Reveal Way F - 088D00E0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAWASH07), owner Civie1 House, cell (54, 79), tag 088D5E50, persistence mode 0; Building (CAPARS05), owner Civie1 House, cell (64, 72), tag 088D5E50, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 5 (cell 62, 76).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2361, Events line 2416, Actions line 2471.

<a id="trigger-092cfe40"></a>

### 11. Reveal Way G - 092CFE40

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (55, 32), tag 092CF9A0, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (58, 32), tag 092CF9A0, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (58, 35), tag 092CF9A0, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (55, 35), tag 092CF9A0, persistence mode 0; GI (E1), owner BadGuy1 House, cell (54, 36), tag 092CF9A0, persistence mode 0; GI (E1), owner BadGuy1 House, cell (53, 30), tag 092CF9A0, persistence mode 0; Building (CAWASH07), owner Civie1 House, cell (53, 26), tag 092CF9A0, persistence mode 0; Dumpster (CAMISC03), owner Civie1 House, cell (58, 39), tag 092CF9A0, persistence mode 0; Dumpster (CAMISC03), owner Civie1 House, cell (64, 39), tag 092CF9A0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 6 (cell 57, 33).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2362, Events line 2417, Actions line 2472.

<a id="trigger-092cf430"></a>

### 12. Reveal Way H - 092CF430

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pill Box (GAPILL), owner BadGuy1 House, cell (49, 23), tag 092CF260, persistence mode 0; Dumpster (CAMISC03), owner Civie1 House, cell (45, 38), tag 092CF260, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (41, 36), tag 092CF260, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 7 (cell 50, 33).
2. Reveal terrain around waypoint 6 (cell 57, 33).
3. Reveal terrain around waypoint 53 (cell 40, 29).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2363, Events line 2418, Actions line 2473.

<a id="trigger-092cb280"></a>

### 13. Flak Trak 1 Discovered - 092CB280

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 092C8810 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 8 (cell 94, 65).
2. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
3. Create radar-event marker type 2 at waypoint 36 (cell 92, 65).
4. Play sound FlakTroopAttackCommand.
5. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2364, Events line 2419, Actions line 2474.

<a id="trigger-08a67270"></a>

### 14. Flak Trak 2 Discovered - 08A67270

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Flak Track (HTK), owner Other1 House, cell (51, 79), tag 08A67870, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 10 (cell 50, 83).
2. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
3. Create radar-event marker type 2 at waypoint 25 (cell 51, 79).
4. Play sound FlakTroopAttackCommand.
5. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2365, Events line 2420, Actions line 2475.

<a id="trigger-089f31a0"></a>

### 15. Transport Discovered - 089F31A0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pickup Truck (PICK), owner Other1 House, cell (38, 50), tag 089F2850, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [Full Transport Team (0EBF61CC)](sov05u-teams.md#team-0ebf61cc) at waypoint 11 (cell 26, 50).
2. Reveal terrain around waypoint 11 (cell 26, 50).
3. Create radar-event marker type 2 at waypoint 11 (cell 26, 50).
4. Play sound GenSovWaterSelect.
5. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2366, Events line 2421, Actions line 2476.

<a id="trigger-078df210"></a>

### 16. Reveal Way M - 078DF210

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Blue Light Post (INBLULMP), owner Civie1 House, cell (38, 43), tag 078D8C10, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 12 (cell 34, 42).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2367, Events line 2422, Actions line 2477.

<a id="trigger-078d86a0"></a>

### 17. Reveal Way N - 078D86A0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 078D84D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 13 (cell 31, 35).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2368, Events line 2423, Actions line 2478.

<a id="trigger-078d8320"></a>

### 18. Reveal Way O - 078D8320

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Blue Light Post (INBLULMP), owner Civie1 House, cell (38, 25), tag 078D8150, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 14 (cell 27, 21).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2369, Events line 2424, Actions line 2479.

<a id="trigger-078d9f40"></a>

### 19. Reveal Way P - 078D9F40

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Blue Light Post (INBLULMP), owner Civie1 House, cell (12, 35), tag 078D9D70, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 15 (cell 20, 42).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2370, Events line 2425, Actions line 2480.

<a id="trigger-078d9c90"></a>

### 20. Reveal Way Q - 078D9C90

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Blue Light Post (INBLULMP), owner Civie1 House, cell (27, 30), tag 078D9AC0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 16 (cell 23, 28).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2371, Events line 2426, Actions line 2481.

<a id="trigger-0843cca0"></a>

### 21. Full Trak Discovered - 0843CCA0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAWASH07), owner Civie1 House, cell (43, 12), tag 0843C690, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [Full Trak Team (088B124C)](sov05u-teams.md#team-088b124c) at waypoint 17 (cell 43, 15).
2. Reveal terrain around waypoint 17 (cell 43, 15).
3. Create radar-event marker type 2 at waypoint 17 (cell 43, 15).
4. Play sound FlakTroopAttackCommand.
5. Enable and reset applicable timers for [Full Trak Change (09EEBF3C)](#trigger-09eebf3c).
6. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2372, Events line 2427, Actions line 2482.

<a id="trigger-09eebf3c"></a>

### 22. Full Trak Change - 09EEBF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Full Trak Discovered (0843CCA0)](#trigger-0843cca0).

Attached scope: tag definitions 09EEBE5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [1 Flak Trak Team (0A0EC38C)](sov05u-teams.md#team-0a0ec38c).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2373, Events line 2428, Actions line 2483.

<a id="trigger-08a11920"></a>

### 23. Reveal Way S - 08A11920

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pickup Truck (PICK), owner Civie1 House, cell (70, 50), tag 08A11500, persistence mode 0; Pickup Truck (PICK), owner Civie1 House, cell (79, 51), tag 08A11500, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 18 (cell 78, 50).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2374, Events line 2429, Actions line 2484.

<a id="trigger-08a829a0"></a>

### 24. Reveal Way T - 08A829A0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (59, 43), tag 08A828D0, persistence mode 0; Building (CAWASH07), owner Civie1 House, cell (62, 47), tag 08A828D0, persistence mode 0; Building (CAWASH07), owner Civie1 House, cell (56, 47), tag 08A828D0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 19 (cell 67, 54).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2375, Events line 2430, Actions line 2485.

<a id="trigger-08a82380"></a>

### 25. Reveal Way U - 08A82380

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (50, 43), tag 08A82110, persistence mode 0; Building (CAWASH07), owner Civie1 House, cell (53, 47), tag 08A82110, persistence mode 0; Building (CAPARS06), owner Civie1 House, cell (46, 46), tag 08A82110, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 20 (cell 55, 54).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2376, Events line 2431, Actions line 2486.

<a id="trigger-08b4bb20"></a>

### 26. Reveal Way V - 08B4BB20

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B4B3C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 21 (cell 52, 59).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2377, Events line 2432, Actions line 2487.

<a id="trigger-08b4b0f0"></a>

### 27. Reveal Way W and X - 08B4B0F0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pickup Truck (PICK), owner Civie1 House, cell (49, 68), tag 08B4ABF0, persistence mode 0; Building (CAPARS05), owner Civie1 House, cell (53, 60), tag 08B4ABF0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 22 (cell 45, 67).
2. Reveal terrain around waypoint 23 (cell 43, 71).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2378, Events line 2433, Actions line 2488.

<a id="trigger-08b37710"></a>

### 28. Reveal Way Y - 08B37710

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Building (CAPARS04), owner Civie1 House, cell (42, 46), tag 08B381A0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 24 (cell 52, 54).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2379, Events line 2434, Actions line 2489.

<a id="trigger-0897d490"></a>

### 29. Player Near Tower - 0897D490

Owner reference: Other2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 20 tagged map cells: (45, 31), (46, 31), (47, 31), (48, 31), (49, 31), (50, 31), (45, 32), (50, 32), (45, 33), (50, 33), (45, 34), (50, 34), (45, 35), (50, 35), (45, 36), (46, 36), (47, 36), (48, 36), (49, 36), (50, 36); tag 0897DA60, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type OTHER3; placed owner Other3 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Final Rush (08978F40)](#trigger-08978f40).
2. Display message “Objective 1 Complete” (MISSION:Objective1).
3. Enable and reset applicable timers for [Objective 2 (08B82CBC)](#trigger-08b82cbc).
4. Enable and reset applicable timers for [Win Timer (08AB8750)](#trigger-08ab8750).
5. Disable [Reinforce BG1 (08445DBC)](#trigger-08445dbc).
6. Disable [Re-enable Reinforce BG1 (08445BEC)](#trigger-08445bec).
7. Enable and reset applicable timers for [Tower Energized (0AD6A15C)](#trigger-0ad6a15c).
8. Disable [Tesla Selected (087D3A80)](#trigger-087d3a80).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2380, Events line 2435, Actions line 2490.

<a id="trigger-08978f40"></a>

### 30. Final Rush - 08978F40

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Near Tower (0897D490)](#trigger-0897d490).

Attached scope: tag definitions 08978D70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. Display message “Objective 3: Defeat all remaining Allied troops” (MISSION:Sov05c).
3. Enable and reset applicable timers for [Objective 3 Reminder (0857BEFC)](#trigger-0857befc).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2381, Events line 2436, Actions line 2491.

<a id="trigger-08b82cbc"></a>

### 31. Objective 2 - 08B82CBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Near Tower (0897D490)](#trigger-0897d490).

Attached scope: tag definitions 08B82ABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Defend the PARIS TOWER from Allied attack” (MISSION:Sov05b).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2382, Events line 2437, Actions line 2492.

<a id="trigger-08ab8750"></a>

### 32. Win Timer - 08AB8750

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Near Tower (0897D490)](#trigger-0897d490).

Attached scope: tag definitions 08AB84E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Win Delay (0CB2164C)](#trigger-0cb2164c).
2. Display message “Objective 2 Complete” (MISSION:Objective2).
3. Disable [Objective 3 Reminder (0857BEFC)](#trigger-0857befc).
4. Display message “Objective 3 Complete” (MISSION:Objective3).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2383, Events line 2438, Actions line 2493.

<a id="trigger-08445dbc"></a>

### 33. Reinforce BG1 - 08445DBC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Re-enable Reinforce BG1 (08445BEC)](#trigger-08445bec).

Attached scope: tag definitions 08445CDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Supply reinforcement team [Re_3 IFV Team (08444A1C)](sov05u-teams.md#team-08444a1c).
2. Supply reinforcement team [Re_6 GIs_2 Tanks Team (084413FC)](sov05u-teams.md#team-084413fc).
3. Disable [Reinforce BG1 (08445DBC)](#trigger-08445dbc).
4. Enable and reset applicable timers for [Re-enable Reinforce BG1 (08445BEC)](#trigger-08445bec).
5. Display message “Objective 1: Energize the PARIS TOWER with 3 TESLA TROOPERS” (MISSION:Sov05a).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2384, Events line 2439, Actions line 2494.

<a id="trigger-08445bec"></a>

### 34. Re-enable Reinforce BG1 - 08445BEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reinforce BG1 (08445DBC)](#trigger-08445dbc).

Attached scope: tag definitions 08445B0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Re-enable Reinforce BG1 (08445BEC)](#trigger-08445bec).
2. Enable and reset applicable timers for [Reinforce BG1 (08445DBC)](#trigger-08445dbc).
3. Play voice notification EVA_EnemyAirArmadaDetected.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2385, Events line 2440, Actions line 2495.

<a id="trigger-0ad6a15c"></a>

### 35. Tower Energized - 0AD6A15C

Owner reference: Other2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Near Tower (0897D490)](#trigger-0897d490).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 20 (country/type OTHER3; placed owner Other3 House).
2. Enable and reset applicable timers for [Tower Destroyed Backup (0A70764C)](#trigger-0a70764c).
3. Disable [Tower Energized (0AD6A15C)](#trigger-0ad6a15c).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2386, Events line 2441, Actions line 2496.

<a id="trigger-0857befc"></a>

### 36. Objective 3 Reminder - 0857BEFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Final Rush (08978F40)](#trigger-08978f40).

Attached scope: tag definitions 0857BAAC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 3: Defeat all remaining Allied troops” (MISSION:Sov05c).
2. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2387, Events line 2442, Actions line 2497.

<a id="trigger-0cb2164c"></a>

### 37. Win Delay - 0CB2164C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win Timer (08AB8750)](#trigger-08ab8750).

Attached scope: tag definitions 0CB23C9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Win (0A67AC6C)](#trigger-0a67ac6c).
2. Enable and reset applicable timers for [Cheer (0A67A58C)](#trigger-0a67a58c).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2388, Events line 2443, Actions line 2498.

<a id="trigger-0a70764c"></a>

### 38. Tower Destroyed Backup - 0A70764C

Owner reference: Other3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tower Energized (0AD6A15C)](#trigger-0ad6a15c).

Attached scope: tag definitions 0A70756C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 104 (global list position: Paris Tower (CAPARS01)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2389, Events line 2444, Actions line 2499.

<a id="trigger-0a67ac6c"></a>

### 39. Win - 0A67AC6C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win Delay (0CB2164C)](#trigger-0cb2164c).

Attached scope: tag definitions 0A67AB8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2390, Events line 2445, Actions line 2500.

<a id="trigger-0a67a58c"></a>

### 40. Cheer - 0A67A58C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win Delay (0CB2164C)](#trigger-0cb2164c).

Attached scope: tag definitions 0A67A4AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2391, Events line 2446, Actions line 2501.

<a id="trigger-08ab8d40"></a>

### 41. Player Loses - 08AB8D40

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08AB8B50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 20 (country/type OTHER3; placed owner Other3 House).
2. Building does not exist: type index 11 (global list position: Soviet Barracks (NAHAND)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2392, Events line 2447, Actions line 2502.

<a id="trigger-08b8375c"></a>

### 42. Objective1 - 08B8375C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B82DAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “Objective 1: Energize the PARIS TOWER with 3 TESLA TROOPERS” (MISSION:Sov05a).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2393, Events line 2448, Actions line 2503.

<a id="trigger-087d3a80"></a>

### 43. Tesla Selected - 087D3A80

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tesla Trooper (SHK), owner Other3 House, cell (81, 79), tag 087D3730, persistence mode 0; Tesla Trooper (SHK), owner Other3 House, cell (81, 78), tag 087D3730, persistence mode 0; Tesla Trooper (SHK), owner Other3 House, cell (79, 78), tag 087D3730, persistence mode 0; Tesla Trooper (SHK), owner Other3 House, cell (79, 77), tag 087D3730, persistence mode 0.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Tesla Talk (0915F590)](#trigger-0915f590).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2394, Events line 2449, Actions line 2504.

<a id="trigger-08dff090"></a>

### 44. Ivan Hint - 08DFF090

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Crazy Ivan (IVAN), owner Player House, cell (83, 76), tag 08E000A0, persistence mode 0; Crazy Ivan (IVAN), owner Player House, cell (83, 76), tag 08E000A0, persistence mode 0.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play in-game movie 116.
2. Switch the sidebar to tab 2.
3. Flash cameo/type 371; additional configured duration/location argument 120.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2395, Events line 2450, Actions line 2505.

<a id="trigger-0a1201bc"></a>

### 45. Ambient Ocean - 0A1201BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A12E50C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 52 (cell 38, 29).
2. Play sound _Amb_BirdsHarbor at waypoint 52 (cell 38, 29).
3. Play sound _Amb_OceanLight at waypoint 57 (cell 38, 58).
4. Play sound _Amb_BirdsHarbor at waypoint 57 (cell 38, 58).
5. Play sound _Amb_OceanLight at waypoint 13 (cell 31, 35).
6. Play sound _Amb_BirdsHarbor at waypoint 13 (cell 31, 35).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2396, Events line 2451, Actions line 2506.

<a id="trigger-0a12a7ac"></a>

### 46. Ambient City - 0A12A7AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A12BDCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 80 (cell 71, 75).
2. Play sound _Amb_UrbanMurmur2 at waypoint 83 (cell 60, 67).
3. Play sound _Amb_UrbanMurmur1 at waypoint 28 (cell 64, 57).
4. Play sound _Amb_UrbanMurmur2 at waypoint 2 (cell 85, 66).
5. Play sound _Amb_UrbanMurmur1 at waypoint 26 (cell 50, 50).
6. Play sound _Amb_UrbanMurmur2 at waypoint 17 (cell 43, 15).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2397, Events line 2452, Actions line 2507.

<a id="trigger-0b49294c"></a>

### 47. Start Patrols - 0B49294C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B493DEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [GI Patrol 1 (0B458E1C)](sov05u-teams.md#team-0b458e1c).
2. Supply reinforcement team [GI Patrol 2 (0B45856C)](sov05u-teams.md#team-0b45856c).
3. Supply reinforcement team [GI Patrol 3 (0B4586BC)](sov05u-teams.md#team-0b4586bc).
4. Supply reinforcement team [GI Patrol 4 (0B45991C)](sov05u-teams.md#team-0b45991c).
5. Supply reinforcement team [GI Patrol 5 (09FF31AC)](sov05u-teams.md#team-09ff31ac).
6. Supply reinforcement team [GI Patrol 6 (0A0912DC)](sov05u-teams.md#team-0a0912dc).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2398, Events line 2453, Actions line 2508.

<a id="trigger-0b00823c"></a>

### 48. _Radar Movie 1 - 0B00823C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B009BFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play in-game movie 91.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2399, Events line 2454, Actions line 2509.

<a id="trigger-0b009b0c"></a>

### 49. _Radar Movie 2 - 0B009B0C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 49 tagged map cells: (36, 24), (36, 25), (37, 25), (36, 26), (37, 26), (36, 27), (37, 27), (67, 37), (67, 38), (67, 39), (67, 40), (67, 41), (49, 42), (50, 42), (51, 42), (52, 42), (58, 42), (59, 42), (60, 42), (61, 42), (67, 42), (39, 43), (40, 43), (41, 43), (42, 43), (43, 43), (44, 43), (45, 43), (46, 43), (47, 43), (48, 43), (49, 43), (52, 43), (53, 43), (54, 43), (55, 43), (56, 43), (57, 43), (58, 43), (61, 43), (62, 43), (63, 43), (64, 43), (65, 43), (66, 43), (67, 43), (37, 44), (38, 44), (39, 44); tag 0B009A2C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 20 (country/type OTHER3; placed owner Other3 House).

**Then perform these actions in order:**

1. Play in-game movie 92.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2400, Events line 2455, Actions line 2510.

<a id="trigger-083b646c"></a>

### 50. _Flip Build Tab - 083B646C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 083B76BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Switch the sidebar to tab 2.

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2401, Events line 2456, Actions line 2511.

<a id="trigger-084afe9c"></a>

### 51. Tesla Built By Player - 084AFE9C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tesla To Other3 (0A0ACC3C)](#trigger-0a0acc3c).

Attached scope: tag definitions 084AFC6C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Infantry Type: type index 2 (global list position: Tesla Trooper (SHK)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Disable [Tesla Built By Player (084AFE9C)](#trigger-084afe9c).
2. Enable and reset applicable timers for [Tesla To Other3 (0A0ACC3C)](#trigger-0a0acc3c).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2402, Events line 2457, Actions line 2512.

<a id="trigger-0a0acc3c"></a>

### 52. Tesla To Other3 - 0A0ACC3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Tesla Built By Player (084AFE9C)](#trigger-084afe9c).

Attached scope: tag definitions 0A0A9BCC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Tesla To Other3 (0A0ACC3C)](#trigger-0a0acc3c).
2. Create/recruit team [1 Tesla Trooper Team (083D089C)](sov05u-teams.md#team-083d089c).
3. Enable and reset applicable timers for [Tesla Built By Player (084AFE9C)](#trigger-084afe9c).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2403, Events line 2458, Actions line 2513.

<a id="trigger-0ad6f19c"></a>

### 53. Tower Destroyed - 0AD6F19C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Tower Energized (0AD6A15C)](#trigger-0ad6a15c).

Attached scope: Paris Tower (CAPARS01), owner Other2 House, cell (46, 32), tag 0AD6CDCC, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.
2. Disable [Tower Destroyed (0AD6F19C)](#trigger-0ad6f19c).

Source locator: MAPS02.MIX/sov05u.map; Triggers line 2404, Events line 2459, Actions line 2514.

[All team rosters and ordered plans](sov05u-teams.md) | [All mission overrides](sov05u-overrides.md)
