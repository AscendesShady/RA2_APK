# Operation: Chrono Defense

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for sov07s.map.](../../images/map-sov07s.svg)

*Initial placement schematic for sov07s.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** sov07s.map. **Effective extracted member:** MAPS02.MIX/sov07s.map. **Trigger definitions:** 62.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov07s-teams.md) | [All mission overrides](sov07s-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | SNOW |
| Map size | 0,0,90,75 |
| Visible local rectangle | 2,6,86,63 |
| Placed vehicles | 1 |
| Placed infantry | 42 |
| Placed structures | 50 |
| Placed aircraft | 0 |
| Team templates | 45 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 200 | Player |
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
| 0 | PropTruckArrived,0 |
| 1 | CitizensArrived,0 |
| 2 | SuppliesArrived,0 |
| 3 | CitizensGathered,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [LabDestroyed (0A7F6220)](#trigger-0a7f6220) | Destroyed by anything. See attached-object/cell scope below. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [PlayerWin2 (0C11377C)](#trigger-0c11377c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [LabCaptured (096C55C0)](#trigger-096c55c0) | Entered by: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House). | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |
| [LabSpied (096C4DF0)](#trigger-096c4df0) | Spied upon. See attached-object/cell scope below. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-08d65730"></a>

### 1. Propaganda Truck Start - 08D65730

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D642B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Propaganda Truck (0B12F93C)](sov07s-teams.md#team-0b12f93c).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5274, Events line 5338, Actions line 5402.

<a id="trigger-08d5cf00"></a>

### 2. PropagandaSpout - 08D5CF00

Owner reference: Civilian1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PropEnableSpout (08D58560)](#trigger-08d58560).

Attached scope: tag definitions 08D5CA50 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 450 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [ConvertedSoviets1 (0C13F1FC)](sov07s-teams.md#team-0c13f1fc).
2. Enable and reset applicable timers for [AngryMob (07FC08DC)](#trigger-07fc08dc).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5275, Events line 5339, Actions line 5403.

<a id="trigger-07fc08dc"></a>

### 3. AngryMob - 07FC08DC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PropagandaSpout (08D5CF00)](#trigger-08d5cf00).

Attached scope: tag definitions 07FC045C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [ConvertedSoviets2 (0C24C7EC)](sov07s-teams.md#team-0c24c7ec).
2. Enable and reset applicable timers for [AngryMob2 (08A27E5C)](#trigger-08a27e5c).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5276, Events line 5340, Actions line 5404.

<a id="trigger-08a27e5c"></a>

### 4. AngryMob2 - 08A27E5C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [AngryMob (07FC08DC)](#trigger-07fc08dc).

Attached scope: tag definitions 08A27D7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [AngryMob (07FC08DC)](#trigger-07fc08dc).
2. Disable [AngryMob2 (08A27E5C)](#trigger-08a27e5c).
3. Supply reinforcement team [TownRefill (0884B39C)](sov07s-teams.md#team-0884b39c).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5277, Events line 5341, Actions line 5405.

<a id="trigger-08d58560"></a>

### 5. PropEnableSpout - 08D58560

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D581E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (PropTruckArrived) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PropagandaSpout (08D5CF00)](#trigger-08d5cf00).
2. Enable and reset applicable timers for [PropTruckWarn (089CCF40)](#trigger-089ccf40).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5278, Events line 5342, Actions line 5406.

<a id="trigger-089ccf40"></a>

### 6. PropTruckWarn - 089CCF40

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PropEnableSpout (08D58560)](#trigger-08d58560).

Attached scope: tag definitions 089CA920 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 19 (cell 28, 91).
2. Play in-game movie 94.
3. Reveal terrain around waypoint 69 (cell 26, 93).
4. Reveal terrain around waypoint 70 (cell 33, 91).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5279, Events line 5343, Actions line 5407.

<a id="trigger-08dda070"></a>

### 7. PropagandaTruckDestroyed - 08DDA070

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Propaganda Truck (PROPA), owner Other1 House, cell (138, 76), tag 08DDD760, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [PropagandaSpout (08D5CF00)](#trigger-08d5cf00).
2. Reveal the whole map.
3. Display message “Allied Spy Sat maps were found in the Propaganda Truck wreckage... updating map.” (MISSION:Sov07k).
4. Disable [PropTruckWarn (089CCF40)](#trigger-089ccf40).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5280, Events line 5344, Actions line 5408.

<a id="trigger-0a7f6220"></a>

### 8. LabDestroyed - 0A7F6220

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.
2. Display message “CRITICAL STRUCTURE LOST: Our Battle Lab has been destroyed” (MISSION:Sov07j).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5281, Events line 5345, Actions line 5409.

<a id="trigger-0a7f7830"></a>

### 9. PlayerWin1 - 0A7F7830

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Massive Last Attempt (08E14EC0)](#trigger-08e14ec0).

Attached scope: tag definitions 0A7F7680 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Enable and reset applicable timers for [PlayerWin2 (0C11377C)](#trigger-0c11377c).
3. Enable and reset applicable timers for [CheerMore (0C114D1C)](#trigger-0c114d1c).
4. Play voice notification EVA_PrimaryObjectiveAchieved.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5282, Events line 5346, Actions line 5410.

<a id="trigger-0c11377c"></a>

### 10. PlayerWin2 - 0C11377C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerWin1 (0A7F7830)](#trigger-0a7f7830).

Attached scope: tag definitions 0C11369C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5283, Events line 5347, Actions line 5411.

<a id="trigger-0c114d1c"></a>

### 11. CheerMore - 0C114D1C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PlayerWin1 (0A7F7830)](#trigger-0a7f7830).

Attached scope: tag definitions 0C114B1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5284, Events line 5348, Actions line 5412.

<a id="trigger-08d65820"></a>

### 12. Sniper - 08D65820

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D65370 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 150 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Sniper/GI Squad - Inf (0EF6B6CC)](sov07s-teams.md#team-0ef6b6cc) at waypoint 31 (cell 103, 95).
2. Display message “The first wave of Allied troops have entered the Chronosphere” (MISSION:Sov07d).
3. Play voice notification Mis_S7_SofiaChrono1.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5285, Events line 5349, Actions line 5413.

<a id="trigger-08d80260"></a>

### 13. Sniper/GI - 08D80260

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D81120 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 320 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Sniper/GI Squad - Inf (0EF6B6CC)](sov07s-teams.md#team-0ef6b6cc) at waypoint 26 (cell 99, 20).
2. Supply reinforcement team [!GI Rush (10) - Buildings, Any (0EF7093C)](sov07s-teams.md#team-0ef7093c) at waypoint 27 (cell 103, 110).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5286, Events line 5350, Actions line 5414.

<a id="trigger-0a7d50b0"></a>

### 14. GI/Tank/Rkt - 0A7D50B0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7D7030 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 400 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!GI Rush (10) - Power (0EF6C21C)](sov07s-teams.md#team-0ef6c21c) at waypoint 28 (cell 105, 53).
2. Supply chrono reinforcement team [!Tank Team (2) - Def,Any (0EF7543C)](sov07s-teams.md#team-0ef7543c) at waypoint 34 (cell 52, 132).
3. Supply reinforcement team [!Rocketeer (2) - BattleLab (0EF6DB7C)](sov07s-teams.md#team-0ef6db7c) at waypoint 49 (cell 131, 46).
4. Supply reinforcement team [!Rocketeer (3) - Buildings, Any (0F99B1FC)](sov07s-teams.md#team-0f99b1fc) at waypoint 15 (cell 96, 139).
5. Supply reinforcement team [!GI Rush (10) - Buildings, Any (0EF7093C)](sov07s-teams.md#team-0ef7093c) at waypoint 35 (cell 42, 80).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5287, Events line 5351, Actions line 5415.

<a id="trigger-08d04ae0"></a>

### 15. IFVs - 08D04AE0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D04990 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 650 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [!IFV (2) -  Veh,Any (0F8BA20C)](sov07s-teams.md#team-0f8ba20c) at waypoint 68 (cell 86, 70).
2. Display message “Another Allied force has entered the Chronosphere” (MISSION:Sov07e).
3. Play voice notification Mis_S7_SofiaChrono2.
4. Enable and reset applicable timers for [Hint-Spies(Audio) (07F48DBC)](#trigger-07f48dbc).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5288, Events line 5352, Actions line 5416.

<a id="trigger-07f48dbc"></a>

### 16. Hint-Spies(Audio) - 07F48DBC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [IFVs (08D04AE0)](#trigger-08d04ae0).

Attached scope: tag definitions 07F48ACC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since the trigger timer was initialized/reset.
2. Build Infantry Type: type index 9 (global list position: Attack Dog (DOG)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_Spy.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5289, Events line 5353, Actions line 5417.

<a id="trigger-08d03a10"></a>

### 17. MoreSpies - 08D03A10

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D03860 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 670 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Spy (1) - Radar (0EF6FB7C)](sov07s-teams.md#team-0ef6fb7c) at waypoint 28 (cell 105, 53).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5290, Events line 5354, Actions line 5418.

<a id="trigger-08d091a0"></a>

### 18. GI/Tanks/Prism - 08D091A0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D0F1B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 700 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Sniper/GI Squad - Inf (0EF6B6CC)](sov07s-teams.md#team-0ef6b6cc) at waypoint 37 (cell 48, 86).
2. Supply chrono reinforcement team [!Tank Team (4) - Def,Any (0C32E21C)](sov07s-teams.md#team-0c32e21c) at waypoint 36 (cell 42, 91).
3. Supply chrono reinforcement team [!Tank Team (6) - Def, Battle Lab (0EF7124C)](sov07s-teams.md#team-0ef7124c) at waypoint 35 (cell 42, 80).
4. Supply chrono reinforcement team [!Solar Hint (3) - Veh,Def,Fact,Any (0C1C046C)](sov07s-teams.md#team-0c1c046c) at waypoint 26 (cell 99, 20).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5291, Events line 5355, Actions line 5419.

<a id="trigger-07f5bd2c"></a>

### 19. Hint-Prism - 07F5BD2C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F5B98C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_PrismTank.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5292, Events line 5356, Actions line 5420.

<a id="trigger-08d638b0"></a>

### 20. Rocketeers - 08D638B0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D63B60 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 850 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Rocketeer (3) - Buildings, Any (0F99B1FC)](sov07s-teams.md#team-0f99b1fc) at waypoint 15 (cell 96, 139).
2. Supply reinforcement team [!Rocketeer (3) - Vehicles (09F724E0)](sov07s-teams.md#team-09f724e0) at waypoint 49 (cell 131, 46).
3. Supply reinforcement team [!Rocketeer (5) - Vehicles, BatLab (0922F6FC)](sov07s-teams.md#team-0922f6fc) at waypoint 17 (cell 61, 146).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5293, Events line 5357, Actions line 5421.

<a id="trigger-08e00450"></a>

### 21. Tank/Harrier/Rkt - 08E00450

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08E06CC0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1150 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [!Tank Team (4) - Def,Power (0EF6F43C)](sov07s-teams.md#team-0ef6f43c) at waypoint 11 (cell 69, 125).
2. Supply reinforcement team [!Harriers (4) - Power (0B135DEC)](sov07s-teams.md#team-0b135dec) at waypoint 15 (cell 96, 139).
3. Supply reinforcement team [!Rocketeer (3) - Buildings, Any (0F99B1FC)](sov07s-teams.md#team-0f99b1fc) at waypoint 49 (cell 131, 46).
4. Supply reinforcement team [!Rocketeer (3) - Buildings, Any (0F99B1FC)](sov07s-teams.md#team-0f99b1fc) at waypoint 17 (cell 61, 146).
5. Display message “Another Allied force has entered the Chronosphere” (MISSION:Sov07e).
6. Play voice notification Mis_S7_SofiaChrono2.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5294, Events line 5358, Actions line 5422.

<a id="trigger-0a7dc080"></a>

### 22. GI/IFV/Solar - 0A7DC080

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7DC730 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1600 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [!IFV (2) -  Veh,Any (0F8BA20C)](sov07s-teams.md#team-0f8ba20c) at waypoint 67 (cell 61, 64).
2. Supply reinforcement team [!GI Rush (10) - Power (0EF6C21C)](sov07s-teams.md#team-0ef6c21c) at waypoint 28 (cell 105, 53).
3. Supply chrono reinforcement team [!GI/IFV Combo - Inf, Buildings Any (0B2A580C)](sov07s-teams.md#team-0b2a580c) at waypoint 29 (cell 126, 63).
4. Supply chrono reinforcement team [!GI/IFV Combo - Inf, Buildings Any (0B2A580C)](sov07s-teams.md#team-0b2a580c) at waypoint 30 (cell 113, 65).
5. Supply chrono reinforcement team [!Solar (6) - Fact,Ref,BattleLab (0EF74C8C)](sov07s-teams.md#team-0ef74c8c) at waypoint 36 (cell 42, 91).
6. Display message “Another Allied force has entered the Chronosphere” (MISSION:Sov07e).
7. Play voice notification Mis_S7_SofiaChrono2.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5295, Events line 5359, Actions line 5423.

<a id="trigger-0a7dbb40"></a>

### 23. GI/Harriers - 0A7DBB40

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7DB990 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1670 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [!IFV (2) -  Veh,Any (0F8BA20C)](sov07s-teams.md#team-0f8ba20c) at waypoint 51 (cell 80, 56).
2. Supply reinforcement team [!Harriers (5) - Refinery (0922B1FC)](sov07s-teams.md#team-0922b1fc) at waypoint 15 (cell 96, 139).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5296, Events line 5360, Actions line 5424.

<a id="trigger-0a7db8d0"></a>

### 24. 2Snipers - 0A7DB8D0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7DB680 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2000 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Sniper - Inf (0EF6BB7C)](sov07s-teams.md#team-0ef6bb7c) at waypoint 26 (cell 99, 20).
2. Supply reinforcement team [!Sniper - Inf (0EF6BB7C)](sov07s-teams.md#team-0ef6bb7c) at waypoint 36 (cell 42, 91).
3. Display message “Another Allied force has entered the Chronosphere” (MISSION:Sov07e).
4. Play voice notification Mis_S7_SofiaChrono2.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5297, Events line 5361, Actions line 5425.

<a id="trigger-0a7c80e0"></a>

### 25. Eng/Rkt/GI-IFV - 0A7C80E0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7CA090 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2050 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Engineer (3), GI (10) - Battle Lab (0DE5F1DC)](sov07s-teams.md#team-0de5f1dc) at waypoint 45 (cell 100, 35).
2. Supply reinforcement team [!Rocketeer (5) - Vehicles (09F7E100)](sov07s-teams.md#team-09f7e100) at waypoint 49 (cell 131, 46).
3. Supply chrono reinforcement team [!GI/IFV Combo - Inf, Buildings Any (0B2A580C)](sov07s-teams.md#team-0b2a580c) at waypoint 37 (cell 48, 86).
4. Supply chrono reinforcement team [!GI/IFV Combo - Inf, Buildings Any (0B2A580C)](sov07s-teams.md#team-0b2a580c) at waypoint 75 (cell 50, 91).
5. Supply chrono reinforcement team [!GI/IFV Combo - Inf, Buildings Any (0B2A580C)](sov07s-teams.md#team-0b2a580c) at waypoint 35 (cell 42, 80).
6. Supply chrono reinforcement team [!GI/IFV Combo - Inf, Buildings Any (0B2A580C)](sov07s-teams.md#team-0b2a580c) at waypoint 36 (cell 42, 91).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5298, Events line 5362, Actions line 5426.

<a id="trigger-0a825e30"></a>

### 26. Engineers - 0A825E30

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A826F40 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2100 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Engineer (4), GIs (10) - Battle Lab (0DE5DEFC)](sov07s-teams.md#team-0de5defc) at waypoint 35 (cell 42, 80).
2. Supply chrono reinforcement team [!Engineer/IFV 1 (0EF7432C)](sov07s-teams.md#team-0ef7432c) at waypoint 35 (cell 42, 80).
3. Supply chrono reinforcement team [!Engineer/IFV 1 (0EF7432C)](sov07s-teams.md#team-0ef7432c) at waypoint 26 (cell 99, 20).
4. Supply chrono reinforcement team [!Engineer/IFV 2 (0EF75C8C)](sov07s-teams.md#team-0ef75c8c) at waypoint 86 (cell 103, 27).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5299, Events line 5363, Actions line 5427.

<a id="trigger-08e10b10"></a>

### 27. GI-IFV/Solar/Tanks - 08E10B10

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08E10660 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2160 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [!GI/IFV Combo - Inf, Battle Lab (0B2A38EC)](sov07s-teams.md#team-0b2a38ec) at waypoint 37 (cell 48, 86).
2. Supply chrono reinforcement team [!Solar (6) - Fact,Ref,BattleLab (0EF74C8C)](sov07s-teams.md#team-0ef74c8c) at waypoint 29 (cell 126, 63).
3. Supply chrono reinforcement team [!GI/IFV Combo - Inf, Buildings Any (0B2A580C)](sov07s-teams.md#team-0b2a580c) at waypoint 75 (cell 50, 91).
4. Supply chrono reinforcement team [!Tank Team (4) - Def,Any (0C32E21C)](sov07s-teams.md#team-0c32e21c) at waypoint 30 (cell 113, 65).
5. Supply chrono reinforcement team [!Tank Team (4) - Def,Power (0EF6F43C)](sov07s-teams.md#team-0ef6f43c) at waypoint 32 (cell 96, 120).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5300, Events line 5364, Actions line 5428.

<a id="trigger-08e10420"></a>

### 28. Spies - 08E10420

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08E10270 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2450 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Spy (1) - Power (0EF6D6CC)](sov07s-teams.md#team-0ef6d6cc) at waypoint 35 (cell 42, 80).
2. Supply reinforcement team [!Spy (1) - Power (0EF6D6CC)](sov07s-teams.md#team-0ef6d6cc) at waypoint 37 (cell 48, 86).
3. Supply reinforcement team [!Spy (1) - Power (0EF6D6CC)](sov07s-teams.md#team-0ef6d6cc) at waypoint 26 (cell 99, 20).
4. Supply reinforcement team [!Spy (1) - Power (0EF6D6CC)](sov07s-teams.md#team-0ef6d6cc) at waypoint 86 (cell 103, 27).
5. Display message “The final Allied troops have entered the Chronosphere” (MISSION:Sov07f).
6. Play voice notification Mis_S7_SofiaChrono3.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5301, Events line 5365, Actions line 5429.

<a id="trigger-08e14ec0"></a>

### 29. Massive Last Attempt - 08E14EC0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09F0AF50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2550 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Rocketeer (5) - Vehicles, BatLab (0922F6FC)](sov07s-teams.md#team-0922f6fc) at waypoint 49 (cell 131, 46).
2. Supply reinforcement team [!Harriers (6) - Battle Lab (0922F35C)](sov07s-teams.md#team-0922f35c) at waypoint 15 (cell 96, 139).
3. Enable and reset applicable timers for [PlayerWin1 (0A7F7830)](#trigger-0a7f7830).
4. Supply chrono reinforcement team [!Tank Team (6) - Def, Battle Lab (0EF7124C)](sov07s-teams.md#team-0ef7124c) at waypoint 36 (cell 42, 91).
5. Supply chrono reinforcement team [!GI/IFV Combo - Inf, Battle Lab (0B2A38EC)](sov07s-teams.md#team-0b2a38ec) at waypoint 75 (cell 50, 91).
6. Supply chrono reinforcement team [!Tank Team (4) - Def,Power (0EF6F43C)](sov07s-teams.md#team-0ef6f43c) at waypoint 37 (cell 48, 86).
7. Supply chrono reinforcement team [!Solar (6) - Fact,Ref,BattleLab (0EF74C8C)](sov07s-teams.md#team-0ef74c8c) at waypoint 32 (cell 96, 120).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5302, Events line 5366, Actions line 5430.

<a id="trigger-09a02880"></a>

### 30. SupplyTrucks - 09A02880

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09A026B0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1800 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [SupplyTrucks (0AE23310)](sov07s-teams.md#team-0ae23310) at waypoint 18 (cell 80, 19).
2. Play sound MCVMoveStart at waypoint 52 (cell 84, 26).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5303, Events line 5367, Actions line 5431.

<a id="trigger-08970e20"></a>

### 31. SuppliesArrived - 08970E20

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08970AD0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (SuppliesArrived) is set.

**Then perform these actions in order:**

1. Supply reinforcement team [TraitorousSoviets (0E003EFC)](sov07s-teams.md#team-0e003efc) at waypoint 77 (cell 136, 69).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5304, Events line 5368, Actions line 5432.

<a id="trigger-08a65240"></a>

### 32. Spies - 08A65240

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A665C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 250 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Spy (1) - Power (0EF6D6CC)](sov07s-teams.md#team-0ef6d6cc) at waypoint 26 (cell 99, 20).
2. Enable and reset applicable timers for [Hint-Spies(Movie) (0C60D48C)](#trigger-0c60d48c).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5305, Events line 5369, Actions line 5433.

<a id="trigger-0c60d48c"></a>

### 33. Hint-Spies(Movie) - 0C60D48C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Spies (08A65240)](#trigger-08a65240).

Attached scope: tag definitions 0C60E23C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 109.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5306, Events line 5370, Actions line 5434.

<a id="trigger-096512b0"></a>

### 34. MusterAnyStuckForces - 096512B0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BA6CE50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2700 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. All to Hunt: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5307, Events line 5371, Actions line 5435.

<a id="trigger-096c55c0"></a>

### 35. LabCaptured - 096C55C0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LabDestroyed (0A7F6220)](#trigger-0a7f6220).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.
2. Display message “CRITICAL STRUCTURE LOST: Our Battle Lab has been captured” (MISSION:Sov07h).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5308, Events line 5372, Actions line 5436.

<a id="trigger-096c4df0"></a>

### 36. LabSpied - 096C4DF0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [LabCaptured (096C55C0)](#trigger-096c55c0).

Attached scope: Soviet Battle Lab (NATECH), owner Player House, cell (76, 65), tag 0A7F7D80, persistence mode 0.

**Wait for the recorded events:**

1. Spied upon. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.
2. Display message “CRITICAL STRUCTURE LOST: Spies have infiltrated our Battle Lab” (MISSION:Sov07i).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5309, Events line 5373, Actions line 5437.

<a id="trigger-0ae532fc"></a>

### 37. !DeliverObjective - 0AE532FC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE50F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “Objective 1: Defend your Battle Lab against waves of Allied attackers” (MISSION:Sov07a).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5310, Events line 5374, Actions line 5438.

<a id="trigger-0cb987ec"></a>

### 38. Rocketeers - 0CB987EC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CB9870C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1300 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Rocketeer (3) - Buildings, Any (0F99B1FC)](sov07s-teams.md#team-0f99b1fc) at waypoint 15 (cell 96, 139).
2. Supply reinforcement team [!Rocketeer (4) - Flak,BaseDef (0C48218C)](sov07s-teams.md#team-0c48218c) at waypoint 17 (cell 61, 146).
3. Supply reinforcement team [!Rocketeer (3) - BaseDef,BatLab (0EF6EDEC)](sov07s-teams.md#team-0ef6edec) at waypoint 49 (cell 131, 46).
4. Supply reinforcement team [!Rocketeer (3) - Vehicles (09F724E0)](sov07s-teams.md#team-09f724e0) at waypoint 76 (cell 158, 74).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5311, Events line 5375, Actions line 5439.

<a id="trigger-04005e8c"></a>

### 39. AmbientSounds1 - 04005E8C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04005B9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WavesLake at waypoint 41 (cell 124, 101).
2. Play sound _Amb_WavesLake at waypoint 42 (cell 115, 113).
3. Play sound _Amb_WavesLake at waypoint 40 (cell 73, 92).
4. Play sound _Amb_River at waypoint 20 (cell 31, 109).
5. Play sound _Amb_River at waypoint 21 (cell 44, 109).
6. Play sound _Amb_River at waypoint 22 (cell 50, 107).
7. Play sound _Amb_River at waypoint 23 (cell 55, 104).
8. Play sound _Amb_River at waypoint 24 (cell 59, 101).
9. Play sound _Amb_River at waypoint 25 (cell 65, 99).
10. Enable player input.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5312, Events line 5376, Actions line 5440.

<a id="trigger-040052dc"></a>

### 40. AmbientSounds2 - 040052DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0400518C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 34 (cell 52, 132).
2. Play sound _Amb_WindCold at waypoint 33 (cell 76, 133).
3. Play sound _Amb_WindCold at waypoint 37 (cell 48, 86).
4. Play sound _Amb_WindCold at waypoint 43 (cell 53, 73).
5. Play sound _Amb_WindCold at waypoint 44 (cell 70, 96).
6. Play sound _Amb_WindCold at waypoint 38 (cell 92, 93).
7. Play sound _Amb_WindCold at waypoint 27 (cell 103, 110).
8. Play sound _Amb_WindCold at waypoint 39 (cell 114, 91).
9. Play sound _Amb_WindCold at waypoint 26 (cell 99, 20).
10. Play sound _Amb_WindCold at waypoint 28 (cell 105, 53).
11. Play sound _Amb_WindCold at waypoint 30 (cell 113, 65).
12. Play sound _Amb_WindCold at waypoint 29 (cell 126, 63).
13. Play sound _Amb_WindCold at waypoint 45 (cell 100, 35).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5313, Events line 5377, Actions line 5441.

<a id="trigger-080866cc"></a>

### 41. AmbientSounds3 - 080866CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 080822EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsNightOwl at waypoint 35 (cell 42, 80).
2. Play sound _Amb_BirdsNightOwl at waypoint 46 (cell 126, 83).
3. Play sound _Amb_WindCold at waypoint 47 (cell 64, 46).
4. Play sound _Amb_WindCold at waypoint 48 (cell 60, 134).
5. Play sound _Amb_WindCold at waypoint 50 (cell 72, 136).
6. Play sound _Amb_BirdsNightOwl at waypoint 73 (cell 90, 83).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5314, Events line 5378, Actions line 5442.

<a id="trigger-0b4355bc"></a>

### 42. CapturedOutpost - 0B4355BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tech Outpost (CAOUTP), owner Other3 House, cell (112, 42), tag 0B4354DC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Supply reinforcement team [OutpostGuards (0B4352BC)](sov07s-teams.md#team-0b4352bc) at waypoint 64 (cell 111, 45).
2. Supply reinforcement team [OutpostGuards (0B4352BC)](sov07s-teams.md#team-0b4352bc) at waypoint 65 (cell 110, 40).
3. Supply reinforcement team [OutpostGuards (0B4352BC)](sov07s-teams.md#team-0b4352bc) at waypoint 66 (cell 115, 41).
4. Supply reinforcement team [OutpostGuards (0B4352BC)](sov07s-teams.md#team-0b4352bc) at waypoint 63 (cell 115, 46).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5315, Events line 5379, Actions line 5443.

<a id="trigger-0b44b9dc"></a>

### 43. HouseCrate1 - 0B44B9DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Barn (CABARN02), owner Civie1 House, cell (21, 97), tag 0B44B50C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 9 at waypoint 83 (cell 22, 95).
2. Play sound Bonus at waypoint 83 (cell 22, 95).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5316, Events line 5380, Actions line 5444.

<a id="trigger-0b44cdbc"></a>

### 44. HouseCrate2 - 0B44CDBC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: House (CAHSE01), owner Civie1 House, cell (28, 87), tag 0B44CBBC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 81 (cell 25, 85).
2. Play sound Bonus at waypoint 81 (cell 25, 85).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5317, Events line 5381, Actions line 5445.

<a id="trigger-07f5b5ac"></a>

### 45. Hint-Apocalypse part2 - 07F5B5AC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hint-Apocalypse part1 (07F3505C)](#trigger-07f3505c).

Attached scope: tag definitions 07F48F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_Apocalypse.
2. Switch the sidebar to tab 3.
3. Flash cameo/type 302; additional configured duration/location argument 150.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5318, Events line 5382, Actions line 5446.

<a id="trigger-07f3505c"></a>

### 46. Hint-Apocalypse part1 - 07F3505C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F3D04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 14 (global list position: Soviet War Factory (NAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Hint-Apocalypse part2 (07F5B5AC)](#trigger-07f5b5ac).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5319, Events line 5383, Actions line 5447.

<a id="trigger-0a2487cc"></a>

### 47. Harriers/Prism-HardOnly - 0A2487CC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A2514AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2550 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Harriers (4) - Power (0B135DEC)](sov07s-teams.md#team-0b135dec) at waypoint 17 (cell 61, 146).
2. Supply chrono reinforcement team [!Solar (6) - Fact,Ref,BattleLab (0EF74C8C)](sov07s-teams.md#team-0ef74c8c) at waypoint 27 (cell 103, 110).
3. Supply chrono reinforcement team [!Solar (3) - Veh,Def,Fact,Any (0EF751FC)](sov07s-teams.md#team-0ef751fc) at waypoint 0 (cell 137, 84).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5320, Events line 5384, Actions line 5448.

<a id="trigger-0a252c6c"></a>

### 48. GI/Prism-DiffOnly - 0A252C6C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A25334C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2160 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!GI Rush (10) - Power (0EF6C21C)](sov07s-teams.md#team-0ef6c21c) at waypoint 26 (cell 99, 20).
2. Supply chrono reinforcement team [!Solar (6) - Fact,Ref,BattleLab (0EF74C8C)](sov07s-teams.md#team-0ef74c8c) at waypoint 45 (cell 100, 35).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5321, Events line 5385, Actions line 5449.

<a id="trigger-088d420c"></a>

### 49. Crate-Tent1 - 088D420C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Army Tents (CAARMY01), owner Civie1 House, cell (131, 65), tag 088D359C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 71 (cell 133, 66).
2. Play sound Bonus at waypoint 71 (cell 133, 66).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5322, Events line 5386, Actions line 5450.

<a id="trigger-088d4f3c"></a>

### 50. Crate-Tent2 - 088D4F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Army Tents (CAARMY01), owner Civie1 House, cell (139, 62), tag 088D4E5C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 72 (cell 141, 63).
2. Play sound Bonus at waypoint 72 (cell 141, 63).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5323, Events line 5387, Actions line 5451.

<a id="trigger-08a5d06c"></a>

### 51. 1st Timer - 08A5D06C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A5EF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set the mission timer to 135 configured time units.
2. Use countdown label “Enemy Forces Arriving In:” (MISSION:Sov07l).
3. Start the visible mission timer.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5324, Events line 5388, Actions line 5452.

<a id="trigger-08a5ea6c"></a>

### 52. 2nd Timer - 08A5EA6C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A5E98C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 400 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set the mission timer to 250 configured time units.
2. Start the visible mission timer.
3. Use countdown label “Enemy Forces Arriving In:” (MISSION:Sov07l).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5325, Events line 5389, Actions line 5453.

<a id="trigger-08a5e20c"></a>

### 53. 3rd Timer - 08A5E20C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A5E12C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 900 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set the mission timer to 250 configured time units.
2. Use countdown label “Enemy Forces Arriving In:” (MISSION:Sov07l).
3. Start the visible mission timer.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5326, Events line 5390, Actions line 5454.

<a id="trigger-08a5fd2c"></a>

### 54. 4th Timer - 08A5FD2C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A5FC4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1350 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set the mission timer to 250 configured time units.
2. Use countdown label “Enemy Forces Arriving In:” (MISSION:Sov07l).
3. Start the visible mission timer.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5327, Events line 5391, Actions line 5455.

<a id="trigger-08a5f94c"></a>

### 55. 5th Timer - 08A5F94C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A5F86C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1750 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set the mission timer to 250 configured time units.
2. Use countdown label “Enemy Forces Arriving In:” (MISSION:Sov07l).
3. Start the visible mission timer.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5328, Events line 5392, Actions line 5456.

<a id="trigger-08a5e59c"></a>

### 56. 6th Timer - 08A5E59C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A5E4BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2200 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set the mission timer to 250 configured time units.
2. Use countdown label “Enemy Forces Arriving In:” (MISSION:Sov07l).
3. Start the visible mission timer.

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5329, Events line 5393, Actions line 5457.

<a id="trigger-0c3e0e5c"></a>

### 57. GIs-Solar--M/H Only - 0C3E0E5C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C3E0D7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2550 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!GI Rush (10) - Buildings, Any (0EF7093C)](sov07s-teams.md#team-0ef7093c) at waypoint 26 (cell 99, 20).
2. Supply chrono reinforcement team [!Solar (4) - Veh,Def,Fact,Any (0C2AF7DC)](sov07s-teams.md#team-0c2af7dc) at waypoint 45 (cell 100, 35).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5330, Events line 5394, Actions line 5458.

<a id="trigger-0fbd96bc"></a>

### 58. Spies - 0FBD96BC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0FBD95DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 650 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Spy (1) - Power (0EF6D6CC)](sov07s-teams.md#team-0ef6d6cc) at waypoint 34 (cell 52, 132).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5331, Events line 5395, Actions line 5459.

<a id="trigger-0fbd8e6c"></a>

### 59. Spies - 0FBD8E6C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0FBD8D1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1150 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Spy (1) - Radar (0EF671FC)](sov07s-teams.md#team-0ef671fc) at waypoint 52 (cell 84, 26).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5332, Events line 5396, Actions line 5460.

<a id="trigger-0fbd8b7c"></a>

### 60. Spies - 0FBD8B7C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0FBD8A9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2050 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [!Spy (1) - Radar (0EF6FB7C)](sov07s-teams.md#team-0ef6fb7c) at waypoint 35 (cell 42, 80).
2. Supply reinforcement team [!Spy (1) - Power (0EF6D6CC)](sov07s-teams.md#team-0ef6d6cc) at waypoint 26 (cell 99, 20).
3. Supply reinforcement team [!Spy (1) - Power (0EF6D6CC)](sov07s-teams.md#team-0ef6d6cc) at waypoint 86 (cell 103, 27).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5333, Events line 5397, Actions line 5461.

<a id="trigger-0fd6b8dc"></a>

### 61. MakeBG1Hate - 0FD6B8DC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0FD6B32C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5334, Events line 5398, Actions line 5462.

<a id="trigger-0fd6b23c"></a>

### 62. MakeBG2Hate - 0FD6B23C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0FD6B03C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov07s.map; Triggers line 5335, Events line 5399, Actions line 5463.

[All team rosters and ordered plans](sov07s-teams.md) | [All mission overrides](sov07s-overrides.md)
