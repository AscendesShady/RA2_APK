# Operation: Home Front

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov04s.map. **Effective extracted member:** MAPS02.MIX/sov04s.map. **Trigger definitions:** 38.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov04s-teams.md) | [All mission overrides](sov04s-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | SNOW |
| Map size | 0,0,105,80 |
| Visible local rectangle | 5,5,95,65 |
| Placed vehicles | 5 |
| Placed infantry | 31 |
| Placed structures | 48 |
| Placed aircraft | 0 |
| Team templates | 53 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 400 | BadGuy1 |
| 2 | BadGuy2 House | 400 | BadGuy2 |
| 3 | German1 House | 0 | Germany1 |
| 4 | Civilian House | 0 | Neutral |
| 5 | Other1 House | 0 | Other1 |
| 6 | BadGuy3 House | 100 | BadGuy3 |
| 7 | German2 House | 0 | Germany2 |
| 8 | German3 House | 0 | Germany3 |
| 9 | Temp House | 0 | Temp |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Flak Cannons Up,0 |
| 1 | GIs ashore,0 |
| 2 | Grizzly ashore,0 |
| 3 | MCV ashore,0 |
| 4 | Grizzly2 ashore,0 |
| 5 | GI2 ashore,0 |
| 6 | Allied Fleet Here,0 |
| 7 | Feint GI Landing 1,0 |
| 8 | Feint GI Landing 2,0 |
| 9 | Feint Tank Landing ,0 |
| 10 | Feint Tank Landing ,0 |
| 11 | Feint Tank Landing ,0 |
| 12 | Feint Tank 1,0 |
| 13 | Feint Tank 2,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Win (0A6E825C)](#trigger-0a6e825c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 14 (country/type PLAYER; placed owner Player House) the winner. |
| [Loss (095078B0)](#trigger-095078b0) | Destroyed,  All: owner selector 14 (country/type PLAYER; placed owner Player House). | Declare owner selector 14 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-0b454a10"></a>

### 1. Begin Allied Timer - 0B454A10

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B454AF0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set the mission timer to 600 configured time units.
2. Start the visible mission timer.
3. Play voice notification Mis_S4_SofiaTimerStarted.
4. Use countdown label “Time until Allied invasion begins:” (MISSION:sov04a).
5. Display message “Objective 1: Establish a base to defend our motherland” (MISSION:Sov04d).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5169, Events line 5209, Actions line 5249.

<a id="trigger-09af4700"></a>

### 2. Intruder Harrass Attk 1 - 09AF4700

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09AF4320 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 250 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Intruder Harrassment 1 (0D9E646C)](sov04s-teams.md#team-0d9e646c).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5170, Events line 5210, Actions line 5250.

<a id="trigger-09e1b42c"></a>

### 3. Zofia RE Intruders - 09E1B42C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09E18A3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_Intruder.
2. Enable and reset applicable timers for [Zofia RE Terror Drones (09EB22AC)](#trigger-09eb22ac).
3. Create/recruit team [1 Intruder (Attacks Navy) (09E6CBFC)](sov04s-teams.md#team-09e6cbfc).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5171, Events line 5211, Actions line 5251.

<a id="trigger-09eb22ac"></a>

### 4. Zofia RE Terror Drones - 09EB22AC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Zofia RE Intruders (09E1B42C)](#trigger-09e1b42c).

Attached scope: tag definitions 09EB5D6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 14 (global list position: Soviet War Factory (NAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play in-game movie 101.
2. Switch the sidebar to tab 3.
3. Flash cameo/type 316; additional configured duration/location argument 120.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5172, Events line 5212, Actions line 5252.

<a id="trigger-09a1ff40"></a>

### 5. Intruder Harrass Attk 2a - 09A1FF40

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Intruder Harrassment 2 (0D9E5DEC)](sov04s-teams.md#team-0d9e5dec).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5173, Events line 5213, Actions line 5253.

<a id="trigger-09a1f8c0"></a>

### 6. Zofia Suggest Flak Cannons - 09A1F8C0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09A1BA00 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 160 configured time units have elapsed since scenario start.
2. local flag 0 (Flak Cannons Up) is clear.

Flag writers in this mission: set local flag 0 (Flak Cannons Up) at [Flak Cannons Built? (09A1B850)](#trigger-09a1b850). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_S4_SofiaBuildFlak.
2. Display message “Hint: Build Flak Cannons to engage Allied aircraft” (MISSION:sov04b).
3. Switch the sidebar to tab 1.
4. Flash cameo/type 67; additional configured duration/location argument 120.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5174, Events line 5214, Actions line 5254.

<a id="trigger-09a1b850"></a>

### 7. Flak Cannons Built? - 09A1B850

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09A1B6E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 67 (global list position: Flak Cannon (NAFLAK)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 0 (Flak Cannons Up).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5175, Events line 5215, Actions line 5255.

<a id="trigger-0b3fb820"></a>

### 8. Allied Fleet Arrival - 0B3FB820

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Allied Feint Attack (09E5E25C)](#trigger-09e5e25c).

Attached scope: tag definitions 0B3FB390 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Allied Assault Fleet a (0BEFCB5C)](sov04s-teams.md#team-0befcb5c).
2. Supply reinforcement team [Allied Assault Fleet b (0BEFC6AC)](sov04s-teams.md#team-0befc6ac).
3. Supply reinforcement team [Allied Landing Fleet LZ@A a (0434C1FC)](sov04s-teams.md#team-0434c1fc).
4. Supply reinforcement team [Allied Landing Fleet LZ@K a (0434DB7C)](sov04s-teams.md#team-0434db7c).
5. Supply reinforcement team [Allied Landing Fleet LZ@M a (0434D6CC)](sov04s-teams.md#team-0434d6cc).
6. Enable and reset applicable timers for [_Allied MCV Arrival (0B3F9C90)](#trigger-0b3f9c90).
7. Enable and reset applicable timers for [Win Timer (09506090)](#trigger-09506090).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5176, Events line 5216, Actions line 5256.

<a id="trigger-0b3f9c90"></a>

### 9. _Allied MCV Arrival - 0B3F9C90

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Allied Fleet Arrival (0B3FB820)](#trigger-0b3fb820).

Attached scope: tag definitions 0B3F99F0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Allied Landing MCV@K (0434D32C)](sov04s-teams.md#team-0434d32c).
2. Supply reinforcement team [Allied Landing Fleet LZ@A a (0434C1FC)](sov04s-teams.md#team-0434c1fc).
3. Destroy the attached object through the scripted destruction action.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5177, Events line 5217, Actions line 5257.

<a id="trigger-09506090"></a>

### 10. Win Timer - 09506090

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Allied Fleet Arrival (0B3FB820)](#trigger-0b3fb820).

Attached scope: tag definitions 09507990 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Win (0A6E825C)](#trigger-0a6e825c).
2. Enable and reset applicable timers for [Cheer (0A6E956C)](#trigger-0a6e956c).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5178, Events line 5218, Actions line 5258.

<a id="trigger-0a6e825c"></a>

### 11. Win - 0A6E825C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win Timer (09506090)](#trigger-09506090).

Attached scope: tag definitions 0A6E817C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 14 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5179, Events line 5219, Actions line 5259.

<a id="trigger-0a6e956c"></a>

### 12. Cheer - 0A6E956C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win Timer (09506090)](#trigger-09506090).

Attached scope: tag definitions 0A6E948C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 14 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5180, Events line 5220, Actions line 5260.

<a id="trigger-09b5dbe0"></a>

### 13. GIs Landed - 09B5DBE0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09B5D730 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (GIs ashore) is set.

**Then perform these actions in order:**

1. Create/recruit team [GIs Landed (0B135360)](sov04s-teams.md#team-0b135360).
2. Display message “Allied Forces have landed!” (MISSION:sov04c).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5181, Events line 5221, Actions line 5261.

<a id="trigger-09b5d650"></a>

### 14. Grizz@K Landed - 09B5D650

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09B5D450 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Grizzly ashore) is set.

**Then perform these actions in order:**

1. Create/recruit team [Grizz Landed @K (09987040)](sov04s-teams.md#team-09987040).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5182, Events line 5222, Actions line 5262.

<a id="trigger-09b5d370"></a>

### 15. Grizz Landed @M - 09B5D370

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09B5D1C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (Grizzly2 ashore) is set.

**Then perform these actions in order:**

1. Create/recruit team [Grizz Landed @M (099B1610)](sov04s-teams.md#team-099b1610).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5183, Events line 5223, Actions line 5263.

<a id="trigger-09b5d0e0"></a>

### 16. MCV Landed - 09B5D0E0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09B76CF0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (MCV ashore) is set.

**Then perform these actions in order:**

1. Create/recruit team [MCV Landed (099B3350)](sov04s-teams.md#team-099b3350).
2. Enable and reset applicable timers for [Korean Taunt (09E1086C)](#trigger-09e1086c).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5184, Events line 5224, Actions line 5264.

<a id="trigger-09e1086c"></a>

### 17. Korean Taunt - 09E1086C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [MCV Landed (09B5D0E0)](#trigger-09b5d0e0).

Attached scope: tag definitions 09E1062C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 90.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5185, Events line 5225, Actions line 5265.

<a id="trigger-0a4300d0"></a>

### 18. BG1 Production Begin - 0A4300D0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A436030 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).
2. Production Begins: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).
3. Make enemy: owner selector 14 (country/type PLAYER; placed owner Player House).
4. Remove instances of the team organization (not automatically its surviving objects) [GI2 Landed (0A3CB920)](sov04s-teams.md#team-0a3cb920).
5. Remove instances of the team organization (not automatically its surviving objects) [GIs Landed (0B135360)](sov04s-teams.md#team-0b135360).
6. Remove instances of the team organization (not automatically its surviving objects) [Grizz Landed @K (09987040)](sov04s-teams.md#team-09987040).
7. Remove instances of the team organization (not automatically its surviving objects) [Grizz Landed @M (099B1610)](sov04s-teams.md#team-099b1610).
8. Enable and reset applicable timers for [Attacking Lighthouse (0B9F1E9C)](#trigger-0b9f1e9c).
9. Enable and reset applicable timers for [BG1 All to Hunt (08BA2DC0)](#trigger-08ba2dc0).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5186, Events line 5226, Actions line 5266.

<a id="trigger-0b9f1e9c"></a>

### 19. Attacking Lighthouse - 0B9F1E9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Production Begin (0A4300D0)](#trigger-0a4300d0).

Attached scope: Civilian (CIVSF), owner Civilian House, cell (117, 48), tag 0B9F196C, persistence mode 0; Light House (CAFARM06), owner Civilian House, cell (116, 46), tag 0B9F196C, persistence mode 0.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 37 (cell 115, 46).
2. Create radar-event marker type 5 at waypoint 37 (cell 115, 46).
3. Play sound CivSovFemFear.
4. Create/recruit team [Lighthouse Lady (0DB377DC)](sov04s-teams.md#team-0db377dc).
5. Play sound AirRaidSiren.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5187, Events line 5227, Actions line 5267.

<a id="trigger-08ba2dc0"></a>

### 20. BG1 All to Hunt - 08BA2DC0

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Production Begin (0A4300D0)](#trigger-0a4300d0).

Attached scope: tag definitions 08BA2A10 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. All to Hunt: owner selector 15 (country/type BADGUY1; placed owner BadGuy1 House).
2. Reveal the whole map.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5188, Events line 5228, Actions line 5268.

<a id="trigger-09ac1880"></a>

### 21. Invasion ParaTeams a - 09AC1880

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Invasion Para 1 (0BFFF48C)](sov04s-teams.md#team-0bfff48c).
2. Supply reinforcement team [Invasion Para 2 (0BFFEDEC)](sov04s-teams.md#team-0bffedec).
3. Supply reinforcement team [Invasion Para 3 (0BFFE48C)](sov04s-teams.md#team-0bffe48c).
4. Supply reinforcement team [Invasion Para 4 (0BFFA59C)](sov04s-teams.md#team-0bffa59c).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5189, Events line 5229, Actions line 5269.

<a id="trigger-09a2a7f0"></a>

### 22. Stupid Harvester Spawn - 09A2A7F0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09A2A560 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 1 (global list position: Allied Ore Refinery (GAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Stupid Harvester 1 (09A280B0)](sov04s-teams.md#team-09a280b0).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5190, Events line 5230, Actions line 5270.

<a id="trigger-0b14bbb0"></a>

### 23. GI2 Ashore - 0B14BBB0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B14B680 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (GI2 ashore) is set.

**Then perform these actions in order:**

1. Create/recruit team [GI2 Landed (0A3CB920)](sov04s-teams.md#team-0a3cb920).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5191, Events line 5231, Actions line 5271.

<a id="trigger-095078b0"></a>

### 24. Loss - 095078B0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09507510 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 14 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Declare owner selector 14 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5192, Events line 5232, Actions line 5272.

<a id="trigger-0ab06870"></a>

### 25. End Intruder Harrassing - 0AB06870

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09508B00 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Aircraft Type: type index 1 (global list position: Harrier (ORCA)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Disable [Intruder Harrass Attk 1 (09AF4700)](#trigger-09af4700).
2. Disable [Intruder Harrass Attk 2a (09A1FF40)](#trigger-09a1ff40).
3. Disable [Intruder Harrass Attk 2b (0ABF11B0)](#trigger-0abf11b0).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5193, Events line 5233, Actions line 5273.

<a id="trigger-0abf11b0"></a>

### 26. Intruder Harrass Attk 2b - 0ABF11B0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Intruder Harrass Attk 2a (09A1FF40)](#trigger-09a1ff40).

Attached scope: tag definitions 09A1F9A0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 400 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Intruder Harrassment 2 (0D9E5DEC)](sov04s-teams.md#team-0d9e5dec).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5194, Events line 5234, Actions line 5274.

<a id="trigger-079036a0"></a>

### 27. Invasion ParaTeams b - 079036A0

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: [Invasion ParaTeams a (09AC1880)](#trigger-09ac1880).

Attached scope: tag definitions 09AC1330 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Invasion Para 3 (0BFFE48C)](sov04s-teams.md#team-0bffe48c).
2. Supply reinforcement team [Invasion Para 4 (0BFFA59C)](sov04s-teams.md#team-0bffa59c).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5195, Events line 5235, Actions line 5275.

<a id="trigger-0a66103c"></a>

### 28. Zofia RE Scorpion - 0A66103C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A6660BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Unit Type: type index 36 (global list position: Sea Scorpion (HYD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_SeaScorpion.
2. Switch the sidebar to tab 3.
3. Flash cameo/type 336; additional configured duration/location argument 120.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5196, Events line 5236, Actions line 5276.

<a id="trigger-0cb1903c"></a>

### 29. _Reveal Start Point - 0CB1903C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CB2004C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 27 (cell 57, 146).
2. Reveal terrain around waypoint 28 (cell 63, 137).
3. Reveal terrain around waypoint 29 (cell 66, 147).
4. Reveal terrain around waypoint 30 (cell 55, 137).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5197, Events line 5237, Actions line 5277.

<a id="trigger-09e5e25c"></a>

### 30. _Allied Feint Attack - 09E5E25C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09E5CD1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The visible mission countdown has expired.

**Then perform these actions in order:**

1. Play voice notification Mis_S4_SofiaFleetHere.
2. Display message “Objective 2: Drive the Allied invaders back into the sea” (MISSION:Sov04e).
3. Enable and reset applicable timers for [Allied Fleet Arrival (0B3FB820)](#trigger-0b3fb820).
4. Supply reinforcement team [Allied Landing Feint Attack_AF (047374DC)](sov04s-teams.md#team-047374dc).
5. Supply reinforcement team [Allied Landing Feint Attack_AG (047373AC)](sov04s-teams.md#team-047373ac).
6. Supply reinforcement team [Allied Landing Feint Attack_AH (04732A1C)](sov04s-teams.md#team-04732a1c).
7. Supply reinforcement team [Allied Landing Feint Attack_AI (0473256C)](sov04s-teams.md#team-0473256c).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5198, Events line 5238, Actions line 5278.

<a id="trigger-0a073f3c"></a>

### 31. Feint GI Landing 1 - 0A073F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A073A2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (Feint GI Landing 1) is set.

**Then perform these actions in order:**

1. Create/recruit team [GI Feint Attack 1 (0BFFBA4C)](sov04s-teams.md#team-0bffba4c).
2. Reveal terrain around waypoint 31 (cell 91, 135).
3. Create radar-event marker type 5 at waypoint 31 (cell 91, 135).
4. Enable and reset applicable timers for [Attacking Huts (0B9E195C)](#trigger-0b9e195c).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5199, Events line 5239, Actions line 5279.

<a id="trigger-0b9e195c"></a>

### 32. Attacking Huts - 0B9E195C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Feint GI Landing 1 (0A073F3C)](#trigger-0a073f3c).

Attached scope: Civilian (CIVSFM), owner Civilian House, cell (79, 128), tag 0B9E12CC, persistence mode 0; Civilian (CIVSF), owner Civilian House, cell (80, 123), tag 0B9E12CC, persistence mode 0; Civilian (CIVSTM), owner Civilian House, cell (83, 127), tag 0B9E12CC, persistence mode 0; Cottage (CAEUR1), owner Civilian House, cell (79, 124), tag 0B9E12CC, persistence mode 0; House (CAHSE01), owner Civilian House, cell (82, 129), tag 0B9E12CC, persistence mode 0.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 36 (cell 81, 127).
2. Create radar-event marker type 0 at waypoint 36 (cell 81, 127).
3. Play sound CivSovFear.
4. Play sound CivSovFemFear.
5. Create/recruit team [Fishing Village People (0DB3732C)](sov04s-teams.md#team-0db3732c).
6. Play sound AirRaidSiren.

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5200, Events line 5240, Actions line 5280.

<a id="trigger-0a07393c"></a>

### 33. Feint GI Landing 2 - 0A07393C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A07373C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 8 (Feint GI Landing 2) is set.

**Then perform these actions in order:**

1. Create/recruit team [GI Feint Atttack 2 (0BFFB6AC)](sov04s-teams.md#team-0bffb6ac).
2. Reveal terrain around waypoint 32 (cell 93, 132).
3. Create radar-event marker type 5 at waypoint 32 (cell 93, 132).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5201, Events line 5241, Actions line 5281.

<a id="trigger-0a07364c"></a>

### 34. Feint Tank 1 - 0A07364C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A07344C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 12 (Feint Tank 1) is set.

**Then perform these actions in order:**

1. Create/recruit team [Tank Feint Attack 1 (0BFA7EFC)](sov04s-teams.md#team-0bfa7efc).
2. Reveal terrain around waypoint 33 (cell 91, 128).
3. Create radar-event marker type 5 at waypoint 33 (cell 91, 128).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5202, Events line 5242, Actions line 5282.

<a id="trigger-0a076f3c"></a>

### 35. Feint Tank 2 - 0A076F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A076E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 13 (Feint Tank 2) is set.

**Then perform these actions in order:**

1. Create/recruit team [Tank Feint Attack 2 (0BFA2EFC)](sov04s-teams.md#team-0bfa2efc).
2. Reveal terrain around waypoint 34 (cell 84, 118).
3. Create radar-event marker type 5 at waypoint 34 (cell 84, 118).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5203, Events line 5243, Actions line 5283.

<a id="trigger-0abbf69c"></a>

### 36. _Ambient Wind 1 - 0ABBF69C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ABBF21C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 30 (cell 55, 137).
2. Play sound _Amb_WindCold at waypoint 39 (cell 44, 127).
3. Play sound _Amb_WindCold at waypoint 38 (cell 29, 110).
4. Play sound _Amb_WindCold at waypoint 17 (cell 60, 111).
5. Play sound _Amb_WindCold at waypoint 26 (cell 71, 119).
6. Play sound _Amb_WindCold at waypoint 99 (cell 81, 105).
7. Play sound _Amb_WindCold at waypoint 36 (cell 81, 127).
8. Play sound _Amb_WindCold at waypoint 40 (cell 54, 87).
9. Play sound _Amb_WindCold at waypoint 41 (cell 68, 93).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5204, Events line 5244, Actions line 5284.

<a id="trigger-0abc517c"></a>

### 37. _Ambient Wind 2 - 0ABC517C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ABC687C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 42 (cell 84, 92).
2. Play sound _Amb_WindCold at waypoint 43 (cell 73, 73).
3. Play sound _Amb_WindCold at waypoint 44 (cell 82, 62).
4. Play sound _Amb_WindCold at waypoint 21 (cell 94, 49).
5. Play sound _Amb_WindCold at waypoint 22 (cell 87, 41).
6. Play sound _Amb_WindCold at waypoint 20 (cell 112, 50).
7. Play sound _Amb_WindCold at waypoint 19 (cell 105, 27).
8. Play sound _Amb_WindCold at waypoint 24 (cell 92, 77).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5205, Events line 5245, Actions line 5285.

<a id="trigger-0abc678c"></a>

### 38. _Ambient Ocean - 0ABC678C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ABC7DEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 45 (cell 72, 149).
2. Play sound _Amb_OceanHeavy at waypoint 46 (cell 86, 142).
3. Play sound _Amb_OceanHeavy at waypoint 47 (cell 100, 134).
4. Play sound _Amb_OceanHeavy at waypoint 5 (cell 99, 116).
5. Play sound _Amb_OceanHeavy at waypoint 48 (cell 97, 97).
6. Play sound _Amb_OceanHeavy at waypoint 49 (cell 101, 76).
7. Play sound _Amb_OceanHeavy at waypoint 50 (cell 115, 68).
8. Play sound _Amb_OceanHeavy at waypoint 7 (cell 125, 52).
9. Play sound _Amb_OceanHeavy at waypoint 8 (cell 129, 40).
10. Play sound _Amb_OceanHeavy at waypoint 51 (cell 116, 26).

Source locator: MAPS02.MIX/sov04s.map; Triggers line 5206, Events line 5246, Actions line 5286.

[All team rosters and ordered plans](sov04s-teams.md) | [All mission overrides](sov04s-overrides.md)
