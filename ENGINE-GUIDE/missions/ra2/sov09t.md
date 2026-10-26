# sov09t.map

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov09t.map. **Effective extracted member:** MAPS02.MIX/sov09t.map. **Trigger definitions:** 16.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov09t-teams.md) | [All mission overrides](sov09t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | SovStar House |
| Theater | TEMPERATE |
| Map size | 0,0,90,65 |
| Visible local rectangle | 5,8,80,50 |
| Placed vehicles | 6 |
| Placed infantry | 14 |
| Placed structures | 50 |
| Placed aircraft | 0 |
| Team templates | 29 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | President House | 50 | President |
| 1 | SecretService House | 100 | SecretService |
| 2 | USA1 House | 100 | USA1 |
| 3 | USA2 House | 100 | USA2 |
| 4 | Alamo | 0 | Neutral |
| 5 | SovStar House | 50 | SovStar |
| 6 | SovReg House | 100 | SovReg |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | PresOnGround,0 |
| 1 | SS Breakup,0 |
| 2 | 1st Retreat,0 |
| 3 | PrmaryBlown,0 |
| 4 | 1st Retreat A,0 |
| 5 | Call 2nd Retreat,0 |
| 6 | 1st Retreat B,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |

## Every trigger, in file order

<a id="trigger-08b415a0"></a>

### 1. AF1 Landing - 08B415A0

Owner reference: President. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B46C90 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [PresLoadIn (08942CE0)](sov09t-teams.md#team-08942ce0) at waypoint 16 (cell 121, 42).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2655, Events line 2673, Actions line 2691.

<a id="trigger-08b46880"></a>

### 2. Create POTUS - 08B46880

Owner reference: President. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B466B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (PresOnGround) is set.

**Then perform these actions in order:**

1. Create/recruit team [POTUS 00 (089394E0)](sov09t-teams.md#team-089394e0).
2. Create/recruit team [SS1 to be (078F8940)](sov09t-teams.md#team-078f8940).
3. Enable and reset applicable timers for [Create SS1 (08B465D0)](#trigger-08b465d0).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2656, Events line 2674, Actions line 2692.

<a id="trigger-08b465d0"></a>

### 3. Create SS1 - 08B465D0

Owner reference: SecretService. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create POTUS (08B46880)](#trigger-08b46880).

Attached scope: tag definitions 08B46400 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [SS1 to be (078F8940)](sov09t-teams.md#team-078f8940).
2. Create/recruit team [SS1 00 (08942180)](sov09t-teams.md#team-08942180).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2657, Events line 2675, Actions line 2693.

<a id="trigger-08b3f860"></a>

### 4. Call Vanguard - 08B3F860

Owner reference: USA1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B3F390 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (PresOnGround) is set.

**Then perform these actions in order:**

1. Supply reinforcement team [Defend POTUS 1 (08B3C780)](sov09t-teams.md#team-08b3c780) at waypoint 18 (cell 68, 74).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2658, Events line 2676, Actions line 2694.

<a id="trigger-08dc06b0"></a>

### 5. Call SS2 Reinforce - 08DC06B0

Owner reference: SecretService. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (50, 91); tag 08DC02D0, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Vertical Line: owner selector 13 (country/type PRESIDENT; placed owner President House).

**Then perform these actions in order:**

1. Supply reinforcement team [SS2 00 (089414A0)](sov09t-teams.md#team-089414a0) at waypoint 22 (cell 40, 94).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2659, Events line 2677, Actions line 2695.

<a id="trigger-08d4bca0"></a>

### 6. Turrets Blown - 08D4BCA0

Owner reference: President. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Prism Tower (ATESLA), owner USA1 House, cell (70, 81), tag 08D4B7D0, persistence mode 1; Pill Box (GAPILL), owner USA1 House, cell (74, 76), tag 08D4B7D0, persistence mode 1; Pill Box (GAPILL), owner USA1 House, cell (74, 71), tag 08D4B7D0, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 3 (PrmaryBlown).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2660, Events line 2678, Actions line 2696.

<a id="trigger-08d4b5d0"></a>

### 7. VertRetreat1 - 08D4B5D0

Owner reference: President. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (74, 74); tag 08D4AAF0, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Vertical Line: owner selector 17 (country/type SOVSTAR; placed owner SovStar House).

**Then perform these actions in order:**

1. Set local flag 4 (1st Retreat A).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2661, Events line 2679, Actions line 2697.

<a id="trigger-08d4a7c0"></a>

### 8. Crossed Line - 08D4A7C0

Owner reference: President. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 4 (1st Retreat A) is set.

Flag writers in this mission: set local flag 4 (1st Retreat A) at [VertRetreat1 (08D4B5D0)](#trigger-08d4b5d0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [POTUS 00 (089394E0)](sov09t-teams.md#team-089394e0).
2. Create/recruit team [POTUS 01 (08947F00)](sov09t-teams.md#team-08947f00).
3. Set local flag 2 (1st Retreat).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2662, Events line 2680, Actions line 2698.

<a id="trigger-08d4a3d0"></a>

### 9. Blew Primaries - 08D4A3D0

Owner reference: President. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Crossed Line (08D4A7C0)](#trigger-08d4a7c0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (PrmaryBlown) is set.

Flag writers in this mission: set local flag 3 (PrmaryBlown) at [Turrets Blown (08D4BCA0)](#trigger-08d4bca0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [POTUS 00 (089394E0)](sov09t-teams.md#team-089394e0).
2. Create/recruit team [POTUS 01 (08947F00)](sov09t-teams.md#team-08947f00).
3. Set local flag 2 (1st Retreat).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2663, Events line 2681, Actions line 2699.

<a id="trigger-08d45a50"></a>

### 10. 2ndCrossVert - 08D45A50

Owner reference: SovStar. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (48, 96); tag 08D456A0, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Vertical Line: owner selector 17 (country/type SOVSTAR; placed owner SovStar House).

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [POTUS 01 (08947F00)](sov09t-teams.md#team-08947f00).
2. Create/recruit team [POTUS 02 (08953160)](sov09t-teams.md#team-08953160).
3. Set local flag 5 (Call 2nd Retreat).
4. Supply reinforcement team [IFV Rollout (08DB9AB0)](sov09t-teams.md#team-08db9ab0) at waypoint 23 (cell 67, 79).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2664, Events line 2682, Actions line 2700.

<a id="trigger-08d42580"></a>

### 11. Bridges Blown - 08D42580

Owner reference: President. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 3 tagged map cells: (82, 62), (79, 78), (74, 87); tag 08D42230, persistence mode 1.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 6 (1st Retreat B).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2665, Events line 2683, Actions line 2701.

<a id="trigger-08d42150"></a>

### 12. Bridges Destroyed - 08D42150

Owner reference: President. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Blew Primaries (08D4A3D0)](#trigger-08d4a3d0).

Attached scope: tag definitions 08D4A550 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (1st Retreat B) is set.

Flag writers in this mission: set local flag 6 (1st Retreat B) at [Bridges Blown (08D42580)](#trigger-08d42580). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [POTUS 00 (089394E0)](sov09t-teams.md#team-089394e0).
2. Create/recruit team [POTUS 01 (08947F00)](sov09t-teams.md#team-08947f00).
3. Set local flag 2 (1st Retreat).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2666, Events line 2684, Actions line 2702.

<a id="trigger-08d51f40"></a>

### 13. Set up 2nd base - 08D51F40

Owner reference: USA2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D519B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (1st Retreat) is set.

Flag writers in this mission: set local flag 2 (1st Retreat) at [Crossed Line (08D4A7C0)](#trigger-08d4a7c0); set local flag 2 (1st Retreat) at [Blew Primaries (08D4A3D0)](#trigger-08d4a3d0); set local flag 2 (1st Retreat) at [Bridges Destroyed (08D42150)](#trigger-08d42150). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [1R MCV (08D4C630)](sov09t-teams.md#team-08d4c630) at waypoint 23 (cell 67, 79).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2667, Events line 2685, Actions line 2703.

<a id="trigger-08dbb890"></a>

### 14. Cover 2nd Retreat - 08DBB890

Owner reference: SecretService. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DBB320 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (Call 2nd Retreat) is set.

Flag writers in this mission: set local flag 5 (Call 2nd Retreat) at [2ndCrossVert (08D45A50)](#trigger-08d45a50). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [SS2 01 (0895B6F0)](sov09t-teams.md#team-0895b6f0) at waypoint 26 (cell 30, 94).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2668, Events line 2686, Actions line 2704.

<a id="trigger-08dbfe80"></a>

### 15. Intercept 2nd Retreat - 08DBFE80

Owner reference: SecretService. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DBFCB0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (Call 2nd Retreat) is set.

Flag writers in this mission: set local flag 5 (Call 2nd Retreat) at [2ndCrossVert (08D45A50)](#trigger-08d45a50). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [SS2 02 (0895B5D0)](sov09t-teams.md#team-0895b5d0) at waypoint 22 (cell 40, 94).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2669, Events line 2687, Actions line 2705.

<a id="trigger-08dba880"></a>

### 16. Airfield Discovered - 08DBA880

Owner reference: USA1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Air Force Command Headquarters (GAAIRC), owner USA1 House, cell (66, 57), tag 08DBA530, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [Air Discovery (08DBA410)](sov09t-teams.md#team-08dba410) at waypoint 31 (cell 62, 43).

Source locator: MAPS02.MIX/sov09t.map; Triggers line 2670, Events line 2688, Actions line 2706.

[All team rosters and ordered plans](sov09t-teams.md) | [All mission overrides](sov09t-overrides.md)
