# Operation: Eagle Dawn

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for all02s.map.](../../images/map-all02s.svg)

*Initial placement schematic for all02s.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** all02s.map. **Effective extracted member:** MAPS01.MIX/all02s.map. **Trigger definitions:** 84.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all02s-teams.md) | [All mission overrides](all02s-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Americans |
| Theater | SNOW |
| Map size | 0,0,104,75 |
| Visible local rectangle | 5,4,94,63 |
| Placed vehicles | 25 |
| Placed infantry | 36 |
| Placed structures | 60 |
| Placed aircraft | 0 |
| Team templates | 44 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 100 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | Brits | 0 | British |
| 5 | Africans | 0 | Africans |
| 6 | Arabs | 0 | Arabs |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 300 | Russians |
| 9 | GDI | 0 | GDI |
| 10 | Nod | 0 | Nod |
| 11 | Neutral | 0 | Neutral |
| 12 | Special | 0 | Special |
| 13 | Neutral2 | 0 | NeutralA |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Flak Cannons Spotte,0 |
| 1 | Intruders Scout Don,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Player Wins - End (0874619C)](#trigger-0874619c) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner. |
| [Tanya Dead (0A3876DC)](#trigger-0a3876dc) | Destroyed,  All: owner selector 3 (country/type GERMANS; placed owner Germans). | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |
| [Chapel Destroyed (0BF0490C)](#trigger-0bf0490c) | Building does not exist: type index 186 (global list position: Air Force Academy Chapel (CACOLO01)). A map-local type-list change can affect index interpretation. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |
| [Game Over (076A1C5C)](#trigger-076a1c5c) | The unconditional/any-event condition is satisfied. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |

## Every trigger, in file order

<a id="trigger-097274cc"></a>

### 1. Start Base Building - 097274CC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0972094C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Production Begins: owner selector 8 (country/type RUSSIANS; placed owner Russians).
2. Make enemy: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4838, Events line 4924, Actions line 5010.

<a id="trigger-078a169c"></a>

### 2. Text - GO North - 078A169C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Crosses Horizontal Line: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Display message “Head NORTH and make contact with American forces” (MISSION:ALL02a).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4839, Events line 4925, Actions line 5011.

<a id="trigger-0a3a654c"></a>

### 3. Attack Here - 0A3A654C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Attack Here - first time (0B8FBDDC)](#trigger-0b8fbddc).

Attached scope: tag definitions 0A3A340C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 75 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Use ENGINEERS to re-capture our base to the NORTH WEST” (MISSION:ALL02b).
2. Create radar-event marker type 5 at waypoint 21 (cell 73, 87).
3. Play sound MessageText.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4840, Events line 4926, Actions line 5012.

<a id="trigger-0913be4c"></a>

### 4. Player Wins - 0913BE4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chapel Captured (0A1A33BC)](#trigger-0a1a33bc); enable from [American Captures 1st (0926B97C)](#trigger-0926b97c).

Attached scope: tag definitions 0913B95C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Player Wins - End (0874619C)](#trigger-0874619c).
2. Enable and reset applicable timers for [All Cheer (0D53711C)](#trigger-0d53711c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4841, Events line 4927, Actions line 5013.

<a id="trigger-0874619c"></a>

### 5. Player Wins - End - 0874619C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Wins (0913BE4C)](#trigger-0913be4c).

Attached scope: tag definitions 08747ABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4842, Events line 4928, Actions line 5014.

<a id="trigger-0d53711c"></a>

### 6. All Cheer - 0D53711C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Wins (0913BE4C)](#trigger-0913be4c).

Attached scope: tag definitions 0D5364AC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Make side cheer: owner selector 3 (country/type GERMANS; placed owner Germans).
3. Make side cheer: owner selector 1 (country/type ALLIANCE; placed owner Alliance).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4843, Events line 4929, Actions line 5015.

<a id="trigger-0913b86c"></a>

### 7. Pill Box check - 0913B86C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Building Type: type index 66 (global list position: Pill Box (GAPILL)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4844, Events line 4930, Actions line 5016.

<a id="trigger-09bbff3c"></a>

### 8. Confed road - 09BBFF3C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09BBFA5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Confed Road Patrol (09842EFC)](all02s-teams.md#team-09842efc) at waypoint 0 (cell 131, 107).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4845, Events line 4931, Actions line 5017.

<a id="trigger-09bbf96c"></a>

### 9. Confed Base patrol - 09BBF96C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09BBF76C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Confed Base Patrol (0BB0F43C)](all02s-teams.md#team-0bb0f43c) at waypoint 5 (cell 64, 87).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4846, Events line 4932, Actions line 5018.

<a id="trigger-07cd42ac"></a>

### 10. Open Reveal Shroud - 07CD42AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07CD066C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 98 (cell 119, 112).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4847, Events line 4933, Actions line 5019.

<a id="trigger-0904f61c"></a>

### 11. Confed Road Team 2 - 0904F61C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0904F0DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Confed Road Team 2 (09842A7C)](all02s-teams.md#team-09842a7c) at waypoint 23 (cell 90, 106).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4848, Events line 4934, Actions line 5020.

<a id="trigger-09b5298c"></a>

### 12. Drop More Engies - 09B5298C

Owner reference: Nod. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09B524DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  #: 2.

**Then perform these actions in order:**

1. Supply reinforcement team [6 Engineers (0C5E612C)](all02s-teams.md#team-0c5e612c) at waypoint 5 (cell 64, 87).
2. Destroy current instances of [Attack Here (0A3A654C)](#trigger-0a3a654c).
3. Enable and reset applicable timers for [Create French Team (09B6844C)](#trigger-09b6844c).
4. Enable and reset applicable timers for [Text - Engineer Hint (03EBEAFC)](#trigger-03ebeafc).
5. Remove instances of the team organization (not automatically its surviving objects) [6 Engineers (0C5E612C)](all02s-teams.md#team-0c5e612c).
6. Enable and reset applicable timers for [Engies Sound (0C555F3C)](#trigger-0c555f3c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4849, Events line 4935, Actions line 5021.

<a id="trigger-09b6844c"></a>

### 13. Create French Team - 09B6844C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drop More Engies (09B5298C)](#trigger-09b5298c).

Attached scope: tag definitions 09B6CE6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 80 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Change Engineer to France (09C6620C)](all02s-teams.md#team-09c6620c).
2. Create/recruit team [Change Engineer to France (09C6620C)](all02s-teams.md#team-09c6620c).
3. Enable and reset applicable timers for [Create Capture Teams (092C4ABC)](#trigger-092c4abc).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4850, Events line 4936, Actions line 5022.

<a id="trigger-03ebeafc"></a>

### 14. Text - Engineer Hint - 03EBEAFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drop More Engies (09B5298C)](#trigger-09b5298c).

Attached scope: tag definitions 03EBA19C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “HINT: Order an ENGINEER into any HOSTILE BUILDING to capture the building” (MISSION:ALL02d).
2. Play sound MessageText.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4851, Events line 4937, Actions line 5023.

<a id="trigger-0c555f3c"></a>

### 15. Engies Sound - 0C555F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Drop More Engies (09B5298C)](#trigger-09b5298c).

Attached scope: tag definitions 0C55566C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4852, Events line 4938, Actions line 5024.

<a id="trigger-092c4abc"></a>

### 16. Create Capture Teams - 092C4ABC

Owner reference: French. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create French Team (09B6844C)](#trigger-09b6844c).

Attached scope: tag definitions 092C795C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [Capture Conyard (0A9C5B7C)](all02s-teams.md#team-0a9c5b7c).
2. Create/recruit team [Capture Chapel (0A9C57DC)](all02s-teams.md#team-0a9c57dc).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4853, Events line 4939, Actions line 5025.

<a id="trigger-07b1f0ac"></a>

### 17. Soviet 1st Strike - 07B1F0AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Unit Type: type index 33 (global list position: Chrono Miner (CMIN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Create/recruit team [Soviet 1st Strike Team (09E58EFC)](all02s-teams.md#team-09e58efc).
2. Play music theme InDeep.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4854, Events line 4940, Actions line 5026.

<a id="trigger-07b136ec"></a>

### 18. Corner Crate - 07B136EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B15D6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 36 (cell 19, 110).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4855, Events line 4941, Actions line 5027.

<a id="trigger-03ec308c"></a>

### 19. Confed Base Pentrated - 03EC308C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Sentry Gun (NALASR), owner Confederation, cell (72, 98), tag 03EC495C, persistence mode 0; Sentry Gun (NALASR), owner Confederation, cell (68, 99), tag 03EC495C, persistence mode 0; Sentry Gun (NALASR), owner Confederation, cell (61, 99), tag 03EC495C, persistence mode 0; Sentry Gun (NALASR), owner Confederation, cell (72, 78), tag 03EC495C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. All to Hunt: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4856, Events line 4942, Actions line 5028.

<a id="trigger-08eee43c"></a>

### 20. Chrono Miner Check - 08EEE43C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Pill Box check (0913B86C)](#trigger-0913b86c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Unit Type: type index 33 (global list position: Chrono Miner (CMIN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4857, Events line 4943, Actions line 5029.

<a id="trigger-08eefedc"></a>

### 21. MTank check - 08EEFEDC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Chrono Miner Check (08EEE43C)](#trigger-08eee43c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Unit Type: type index 9 (global list position: Grizzly Battle Tank (MTNK)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4858, Events line 4944, Actions line 5030.

<a id="trigger-08eefbec"></a>

### 22. GI Check - 08EEFBEC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [MTank check (08EEFEDC)](#trigger-08eefedc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Infantry Type: type index 0 (global list position: GI (E1)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4859, Events line 4945, Actions line 5031.

<a id="trigger-08eef92c"></a>

### 23. Rocketeer Check - 08EEF92C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [GI Check (08EEFBEC)](#trigger-08eefbec).

Attached scope: tag definitions 0913B66C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Infantry Type: type index 4 (global list position: Rocketeer (JUMPJET)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4860, Events line 4946, Actions line 5032.

<a id="trigger-03f2d45c"></a>

### 24. Tanya Can Swim - 03F2D45C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: 82 tagged map cells: (74, 75), (75, 75), (76, 75), (77, 75), (78, 75), (74, 76), (78, 76), (79, 76), (80, 76), (81, 76), (72, 77), (73, 77), (74, 77), (81, 77), (82, 77), (83, 77), (84, 77), (85, 77), (73, 78), (85, 78), (85, 79), (86, 79), (87, 79), (88, 79), (89, 79), (90, 79), (91, 79), (85, 80), (85, 81), (85, 82), (85, 83), (86, 84), (87, 85), (88, 85), (88, 86), (88, 88), (88, 89), (88, 90), (88, 91), (88, 92), (88, 93), (88, 94), (88, 95), (88, 96), (74, 97), (87, 97), (88, 97), (73, 98), (74, 99), (87, 99), (88, 99), (74, 100), (85, 100), (74, 101), (85, 101), (87, 101), (88, 101), (74, 102), (86, 102), (87, 102), (74, 103), (85, 103), (86, 103), (74, 104), (84, 104), (85, 104), (74, 105), (83, 105), (84, 105), (74, 106), (75, 106), (76, 106), (77, 106), (78, 106), (79, 106), (80, 106), (81, 106), (82, 106), (83, 106), (83, 107), (83, 108), (83, 109); tag 03F2A25C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 3 (country/type GERMANS; placed owner Germans).

**Then perform these actions in order:**

1. Display message “HINT: TANYA can swim” (MISSION:ALL02f).
2. Play sound MessageText.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4861, Events line 4947, Actions line 5033.

<a id="trigger-09790f3c"></a>

### 25. 1st Patrol has been shot - 09790F3C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0979078C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 6 (country/type ARABS; placed owner Arabs).
2. All to Hunt: owner selector 6 (country/type ARABS; placed owner Arabs).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4862, Events line 4948, Actions line 5034.

<a id="trigger-08d3d8ac"></a>

### 26. 2nd Patrol is Shot - 08D3D8AC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D3D61C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 5 (country/type AFRICANS; placed owner Africans).
2. All to Hunt: owner selector 5 (country/type AFRICANS; placed owner Africans).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4863, Events line 4949, Actions line 5035.

<a id="trigger-07b2cc6c"></a>

### 27. Free Crate! - 07B2CC6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: House (CAHSE03), owner Neutral, cell (85, 117), tag 07B2C82C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 9 at waypoint 39 (cell 84, 116).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4864, Events line 4950, Actions line 5036.

<a id="trigger-07b2c5ec"></a>

### 28. Free Crate - 07B2C5EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: House (CAHSE03), owner Neutral, cell (56, 116), tag 07B2C50C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 40 (cell 55, 115).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4865, Events line 4951, Actions line 5037.

<a id="trigger-07b2c41c"></a>

### 29. Free Crate - 07B2C41C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: House (CAHSE03), owner Neutral, cell (66, 132), tag 07B2C33C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 9 at waypoint 41 (cell 65, 131).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4866, Events line 4952, Actions line 5038.

<a id="trigger-07b2c24c"></a>

### 30. Free Crate - 07B2C24C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: House (CAHSE03), owner Neutral, cell (107, 100), tag 07B2C16C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 42 (cell 106, 99).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4867, Events line 4953, Actions line 5039.

<a id="trigger-0abc9eac"></a>

### 31. Create Harrier Team - 0ABC9EAC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Airplanes are US (09E23D7C)](#trigger-09e23d7c).

Attached scope: tag definitions 0ABC967C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [4 Intruders (09D4059C)](all02s-teams.md#team-09d4059c).
2. Enable and reset applicable timers for [Destroy Airpatrol (09D8D03C)](#trigger-09d8d03c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4868, Events line 4954, Actions line 5040.

<a id="trigger-09d8d03c"></a>

### 32. Destroy Airpatrol - 09D8D03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Create Harrier Team (0ABC9EAC)](#trigger-0abc9eac).

Attached scope: tag definitions 08037C6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [4 Intruders (09D4059C)](all02s-teams.md#team-09d4059c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4869, Events line 4955, Actions line 5041.

<a id="trigger-0b936d4c"></a>

### 33. Play Tanya Air-Movie - 0B936D4C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Airplanes are US (09E23D7C)](#trigger-09e23d7c).

Attached scope: tag definitions 0B9363DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play in-game movie 82.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4870, Events line 4956, Actions line 5042.

<a id="trigger-07e8985c"></a>

### 34. Tanya Can Swim Text - 07E8985C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 31 tagged map cells: (68, 65), (68, 66), (68, 67), (68, 68), (68, 69), (68, 70), (68, 71), (68, 72), (68, 73), (68, 74), (68, 75), (68, 76), (60, 99), (70, 99), (60, 100), (70, 100), (60, 101), (70, 101), (60, 102), (69, 102), (70, 102), (60, 103), (61, 103), (62, 103), (63, 103), (64, 103), (65, 103), (66, 103), (67, 103), (68, 103), (69, 103); tag 07E893DC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 3 (country/type GERMANS; placed owner Germans).

**Then perform these actions in order:**

1. Display message “HINT: TANYA can swim” (MISSION:ALL02f).
2. Play sound MessageText.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4871, Events line 4957, Actions line 5043.

<a id="trigger-07e9654c"></a>

### 35. Disable Tanya Text - 07E9654C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Disable [Tanya Can Swim Text (07E8985C)](#trigger-07e8985c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4872, Events line 4958, Actions line 5044.

<a id="trigger-080097ac"></a>

### 36. Diable Tanya 2 - 080097AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Conscript (E2), owner Confederation, cell (70, 87), tag 0800AEAC, persistence mode 0; Allied War Factory (GAWEAP), owner Neutral2, cell (58, 89), tag 0800AEAC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Tanya Can Swim Text (07E8985C)](#trigger-07e8985c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4873, Events line 4959, Actions line 5045.

<a id="trigger-07ff8f3c"></a>

### 37. Txt Flak Cannons - 07FF8F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FF89FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “HINT: Order TANYA to destroy the FLAK CANNONS” (MISSION:ALL02e).
2. Enable and reset applicable timers for [txt Flak Reminder (096A7BEC)](#trigger-096a7bec).
3. Play sound MessageText.
4. Display message “so the ROCKETEERS can destroy the SENTRY GUNS” (MISSION:ALL02i).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4874, Events line 4960, Actions line 5046.

<a id="trigger-096a7bec"></a>

### 38. txt Flak Reminder - 096A7BEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Txt Flak Cannons (07FF8F3C)](#trigger-07ff8f3c).

Attached scope: tag definitions 096A770C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “HINT: Order TANYA to destroy the FLAK CANNONS” (MISSION:ALl02e).
2. Play sound MessageText.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4875, Events line 4961, Actions line 5047.

<a id="trigger-03e3a95c"></a>

### 39. Hard Patrol Team - 03E3A95C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03E3A2CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Hard Patrol Team (03E3669C)](all02s-teams.md#team-03e3669c) at waypoint 26 (cell 101, 64).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4876, Events line 4962, Actions line 5048.

<a id="trigger-083e90dc"></a>

### 40. TXT Objecitve 2 1st - 083E90DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chapel Captured (0A1A33BC)](#trigger-0a1a33bc); enable from [American Captures 1st (0926B97C)](#trigger-0926b97c).

Attached scope: tag definitions 083EF94C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Txt Objective 2 (0B94D03C)](#trigger-0b94d03c).
2. Display message “Objective 2: Destroy all hostile forces” (MISSION:ALL02c).
3. Play voice notification EVA_NewMissionObjective.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4877, Events line 4963, Actions line 5049.

<a id="trigger-0b94d03c"></a>

### 41. Txt Objective 2 - 0B94D03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [TXT Objecitve 2 1st (083E90DC)](#trigger-083e90dc).

Attached scope: tag definitions 0B94804C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy all hostile forces” (MISSION:ALL02c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4878, Events line 4964, Actions line 5050.

<a id="trigger-07f3448c"></a>

### 42. All to Hunt - 07F3448C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Soviet Construction Yard (NACNST), owner Russians, cell (116, 43), tag 080BA7AC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. All to Hunt: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4879, Events line 4965, Actions line 5051.

<a id="trigger-080a207c"></a>

### 43. Barrels Destroyed - 080A207C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Barrels (CAMISC01), owner Nod, cell (124, 41), tag 080ADE6C, persistence mode 0; Barrels (CAMISC01), owner Nod, cell (123, 43), tag 080ADE6C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [Barrel Defense Team (08060CBC)](all02s-teams.md#team-08060cbc).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4880, Events line 4966, Actions line 5052.

<a id="trigger-0a30803c"></a>

### 44. Tanya Shot - 0A30803C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Tanya (TANY), owner Germans, cell (121, 117), tag 0971A83C, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “Keep TANYA alive!” (MISSION:ALL02g).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4881, Events line 4967, Actions line 5053.

<a id="trigger-0a3876dc"></a>

### 45. Tanya Dead - 0A3876DC

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A3870FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 3 (country/type GERMANS; placed owner Germans).

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.
2. Display message “TANYA has been KILLED!” (MISSION:ALL02h).
3. Play voice notification Mis_A1_EvaTanyaDeath.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4882, Events line 4968, Actions line 5054.

<a id="trigger-0ba7b6cc"></a>

### 46. Opening AX Crate - 0BA7B6CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BA7B18C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create crate type 9 at waypoint 49 (cell 114, 105).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4883, Events line 4969, Actions line 5055.

<a id="trigger-0c4b0c6c"></a>

### 47. Ambient Effects - 0C4B0C6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C4B2E9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_WindPlains at waypoint 98 (cell 119, 112).
2. Play sound _Amb_WindCold at waypoint 1 (cell 91, 107).
3. Play sound _Amb_WindPlains at waypoint 7 (cell 90, 75).
4. Play sound _Amb_WindPlains at waypoint 15 (cell 40, 91).
5. Play sound _Amb_WindPlains at waypoint 17 (cell 47, 113).
6. Play sound _Amb_BirdsNightOwl at waypoint 38 (cell 109, 98).
7. Play sound _Amb_WindCold at waypoint 64 (cell 75, 164).
8. Play sound _Amb_BirdsNightOwl at waypoint 66 (cell 117, 93).
9. Play sound _Amb_WindPlains at waypoint 0 (cell 131, 107).
10. Play sound _Amb_WindPlains at waypoint 67 (cell 131, 94).
11. Play sound _Amb_WindPlains at waypoint 68 (cell 135, 82).
12. Play sound _Amb_WindPlains at waypoint 69 (cell 139, 62).
13. Play sound _Amb_WindPlains at waypoint 70 (cell 136, 52).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4884, Events line 4970, Actions line 5056.

<a id="trigger-0b423a2c"></a>

### 48. Secret Crate AY - 0B423A2C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pickup Truck (PICK), owner Nod, cell (148, 66), tag 0B42318C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 50 (cell 148, 65).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4885, Events line 4971, Actions line 5057.

<a id="trigger-0b427a9c"></a>

### 49. Secret Crate AZ - 0B427A9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pickup Truck (PICK), owner Nod, cell (150, 66), tag 0B42789C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 14 at waypoint 51 (cell 150, 65).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4886, Events line 4972, Actions line 5058.

<a id="trigger-0b4276bc"></a>

### 50. Secret Crate BA - 0B4276BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pickup Truck (PICK), owner Nod, cell (152, 66), tag 0B4273DC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 9 at waypoint 52 (cell 152, 65).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4887, Events line 4973, Actions line 5059.

<a id="trigger-07f83f3c"></a>

### 51. 2 extra Rocketeers - 07F83F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Rocketeer (JUMPJET), owner Neutral, cell (74, 164), tag 07F81F4C, persistence mode 0; Rocketeer (JUMPJET), owner Neutral, cell (76, 166), tag 07F81F4C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Play voice notification Mis_A5_AllSoldier2.
3. Play sound Bonus at waypoint 64 (cell 75, 164).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4888, Events line 4974, Actions line 5060.

<a id="trigger-077a775c"></a>

### 52. Harvester Found - 077A775C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 077409AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Play voice notification EVA_UnitReady.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4889, Events line 4975, Actions line 5061.

<a id="trigger-0896d65c"></a>

### 53. Reveal Second Base - 0896D65C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0896D57C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Intruders Scout Don) is set.
2. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 54 (cell 108, 45).
2. Reveal terrain around waypoint 56 (cell 115, 52).
3. Reveal terrain around waypoint 57 (cell 109, 54).
4. Reveal terrain around waypoint 55 (cell 123, 59).
5. Reveal terrain around waypoint 29 (cell 118, 47).
6. Reveal terrain around waypoint 30 (cell 113, 59).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4890, Events line 4976, Actions line 5062.

<a id="trigger-0a1a33bc"></a>

### 54. Chapel Captured - 0A1A33BC

Owner reference: French. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 186 (global list position: Air Force Academy Chapel (CACOLO01)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Destroy current instances of [Chapel Destroyed (0BF0490C)](#trigger-0bf0490c).
3. Enable and reset applicable timers for [txt objective 1 complete (084B52DC)](#trigger-084b52dc).
4. Enable and reset applicable timers for [TXT Objecitve 2 1st (083E90DC)](#trigger-083e90dc).
5. Destroy current instances of [Attack Here (0A3A654C)](#trigger-0a3a654c).
6. Enable and reset applicable timers for [Player Wins (0913BE4C)](#trigger-0913be4c).
7. Enable and reset applicable timers for [1 French Change House (0D7E70EC)](#trigger-0d7e70ec).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4891, Events line 4977, Actions line 5063.

<a id="trigger-0bf0490c"></a>

### 55. Chapel Destroyed - 0BF0490C

Owner reference: NeutralA. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BF0436C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 186 (global list position: Air Force Academy Chapel (CACOLO01)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.
2. Play voice notification EVA_CriticalStrucureLost.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4892, Events line 4978, Actions line 5064.

<a id="trigger-084b52dc"></a>

### 56. txt objective 1 complete - 084B52DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chapel Captured (0A1A33BC)](#trigger-0a1a33bc); enable from [American Captures 1st (0926B97C)](#trigger-0926b97c).

Attached scope: tag definitions 084B01CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Display message “Objective 1 Complete” (MISSION:Objective1).
2. Play voice notification EVA_PrimaryObjectiveAchieved.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4893, Events line 4979, Actions line 5065.

<a id="trigger-0d7e70ec"></a>

### 57. 1 French Change House - 0D7E70EC

Owner reference: French. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chapel Captured (0A1A33BC)](#trigger-0a1a33bc); enable from [American Captures 1st (0926B97C)](#trigger-0926b97c).

Attached scope: tag definitions 0D7ED19C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. All change house: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4894, Events line 4980, Actions line 5066.

<a id="trigger-0926b97c"></a>

### 58. American Captures 1st - 0926B97C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Chapel Captured (0A1A33BC)](#trigger-0a1a33bc).

Attached scope: Air Force Academy Chapel (CACOLO01), owner Neutral2, cell (57, 81), tag 0A1A669C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Destroy current instances of [Create French Team (09B6844C)](#trigger-09b6844c).
2. Destroy current instances of [Chapel Destroyed (0BF0490C)](#trigger-0bf0490c).
3. Enable and reset applicable timers for [txt objective 1 complete (084B52DC)](#trigger-084b52dc).
4. Enable and reset applicable timers for [TXT Objecitve 2 1st (083E90DC)](#trigger-083e90dc).
5. Destroy current instances of [Attack Here (0A3A654C)](#trigger-0a3a654c).
6. Enable and reset applicable timers for [Player Wins (0913BE4C)](#trigger-0913be4c).
7. Enable and reset applicable timers for [1 French Change House (0D7E70EC)](#trigger-0d7e70ec).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4895, Events line 4981, Actions line 5067.

<a id="trigger-0a660c9c"></a>

### 59. Give French Back - 0A660C9C

Owner reference: French. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A66173C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. All change house: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4896, Events line 4982, Actions line 5068.

<a id="trigger-0977489c"></a>

### 60. Rocketeers Have Arrived - 0977489C

Owner reference: French. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09773B9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [8 Rocketeers (0D691EFC)](all02s-teams.md#team-0d691efc) at waypoint 44 (cell 119, 127).
2. Enable and reset applicable timers for [Rocketeers Become USA (09BFFBEC)](#trigger-09bffbec).
3. Enable and reset applicable timers for [Attack Here - first time (0B8FBDDC)](#trigger-0b8fbddc).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4897, Events line 4983, Actions line 5069.

<a id="trigger-09bffbec"></a>

### 61. Rocketeers Become USA - 09BFFBEC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Rocketeers Have Arrived (0977489C)](#trigger-0977489c).

Attached scope: tag definitions 09BFFADC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [8 Rocketeers (0D691EFC)](all02s-teams.md#team-0d691efc).
2. Create/recruit team [8 Rocketeers - USA (0D691A4C)](all02s-teams.md#team-0d691a4c).
3. Enable and reset applicable timers for [Rocketeers Move (08312AFC)](#trigger-08312afc).
4. Create radar-event marker type 2 at waypoint 58 (cell 116, 125).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4898, Events line 4984, Actions line 5070.

<a id="trigger-0b8fbddc"></a>

### 62. Attack Here - first time - 0B8FBDDC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Rocketeers Have Arrived (0977489C)](#trigger-0977489c); enable from [Play Rocketeer Movie (0A84F66C)](#trigger-0a84f66c).

Attached scope: tag definitions 0B8FB91C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 25 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 21 (cell 73, 87).
2. Create radar-event marker type 5 at waypoint 21 (cell 73, 87).
3. Play sound MessageText.
4. Display message “Objective 1: Use ENGINEERS to re-capture our base to the NORTH WEST” (MISSION:ALL02b).
5. Enable and reset applicable timers for [Attack Here (0A3A654C)](#trigger-0a3a654c).
6. Play voice notification EVA_NewMissionObjective.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4899, Events line 4985, Actions line 5071.

<a id="trigger-08312afc"></a>

### 63. Rocketeers Move - 08312AFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Rocketeers Become USA (09BFFBEC)](#trigger-09bffbec); enable from [Play Rocketeer Movie (0A84F66C)](#trigger-0a84f66c).

Attached scope: tag definitions 08325F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [8 Rocketeer Move Team (0B12B7DC)](all02s-teams.md#team-0b12b7dc).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4900, Events line 4986, Actions line 5072.

<a id="trigger-09d9075c"></a>

### 64. Rocketeers Destroyed - 09D9075C

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Rocketeer Destroyed Enable (0BB7E6DC)](#trigger-0bb7e6dc).

Attached scope: tag definitions 09D9271C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 4.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Rocketeers - 2nd Wave (08408A8C)](#trigger-08408a8c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4901, Events line 4987, Actions line 5073.

<a id="trigger-08408a8c"></a>

### 65. Rocketeers - 2nd Wave - 08408A8C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Rocketeers Destroyed (09D9075C)](#trigger-09d9075c).

Attached scope: tag definitions 0840861C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Rocketeers 2nd Wave (0840EEFC)](all02s-teams.md#team-0840eefc) at waypoint 62 (cell 128, 122).
2. Create radar-event marker type 2 at waypoint 98 (cell 119, 112).
3. Play voice notification EVA_ReinforcementsHaveArrived.
4. Display message “HINT: Order TANYA to destroy the FLAK CANNONS” (MISSION:ALL02e).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4902, Events line 4988, Actions line 5074.

<a id="trigger-0a84f66c"></a>

### 66. Play Rocketeer Movie - 0A84F66C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A84F12C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 70.
2. Enable and reset applicable timers for [Attack Here - first time (0B8FBDDC)](#trigger-0b8fbddc).
3. Enable and reset applicable timers for [Rocketeers Move (08312AFC)](#trigger-08312afc).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4903, Events line 4989, Actions line 5075.

<a id="trigger-07a3ef3c"></a>

### 67. Kill Objective 1 Text - 07A3EF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A3AA4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Destroy current instances of [Attack Here (0A3A654C)](#trigger-0a3a654c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4904, Events line 4990, Actions line 5076.

<a id="trigger-0a7150ac"></a>

### 68. 1 Extra Chrono Miner - 0A7150AC

Owner reference: French. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A710B5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Play sound GenAllVehicleSelect at waypoint 63 (cell 51, 139).
3. Play sound Bonus at waypoint 63 (cell 51, 139).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4905, Events line 4991, Actions line 5077.

<a id="trigger-09d4903c"></a>

### 69. Hard Road Patrol 1 - 09D4903C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09D4B19C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Hard Confed Road Patrol (09D4317C)](all02s-teams.md#team-09d4317c) at waypoint 0 (cell 131, 107).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4906, Events line 4992, Actions line 5078.

<a id="trigger-09d4b0ac"></a>

### 70. Hard Road Patrol 2 - 09D4B0AC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09D4811C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Hard Confed Road Patrol 2 (09D470BC)](all02s-teams.md#team-09d470bc) at waypoint 23 (cell 90, 106).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4907, Events line 4993, Actions line 5079.

<a id="trigger-076a1c5c"></a>

### 71. Game Over - 076A1C5C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 076A140C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4908, Events line 4994, Actions line 5080.

<a id="trigger-0b0af2ac"></a>

### 72. End Paradrop - 0B0AF2AC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B0B504C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 67 (global list position: Flak Cannon (NAFLAK)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [10 Paratroopers BE (09FF2A4C)](all02s-teams.md#team-09ff2a4c) at waypoint 56 (cell 115, 52).
2. Supply reinforcement team [10 Paratroopers BI (09FF259C)](all02s-teams.md#team-09ff259c) at waypoint 60 (cell 115, 56).
3. Supply reinforcement team [10 Paratroopers BJ (09FF246C)](all02s-teams.md#team-09ff246c) at waypoint 61 (cell 114, 48).
4. Enable and reset applicable timers for [EndGame Para Sound (088772EC)](#trigger-088772ec).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4909, Events line 4995, Actions line 5081.

<a id="trigger-088772ec"></a>

### 73. EndGame Para Sound - 088772EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [End Paradrop (0B0AF2AC)](#trigger-0b0af2ac).

Attached scope: tag definitions 08878B3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4910, Events line 4996, Actions line 5082.

<a id="trigger-0bb7e6dc"></a>

### 74. Rocketeer Destroyed Enable - 0BB7E6DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BB7CF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Rocketeers Destroyed (09D9075C)](#trigger-09d9075c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4911, Events line 4997, Actions line 5083.

<a id="trigger-0be8571c"></a>

### 75. ConYard Captured - 0BE8571C

Owner reference: French. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Construction Yard (GACNST), owner Neutral2, cell (65, 80), tag 0BE853CC, persistence mode 0.

**Wait for the recorded events:**

1. Building exists: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4912, Events line 4998, Actions line 5084.

<a id="trigger-04184dac"></a>

### 76. Airplanes Create - 04184DAC

Owner reference: British. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0418229C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [4 Intruders - Start (0A54E20C)](all02s-teams.md#team-0a54e20c) at waypoint 5 (cell 64, 87).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4913, Events line 4999, Actions line 5085.

<a id="trigger-092731ec"></a>

### 77. Destroy Airplane Team - 092731EC

Owner reference: British. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09274C5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [4 Intruders - Start (0A54E20C)](all02s-teams.md#team-0a54e20c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4914, Events line 5000, Actions line 5086.

<a id="trigger-09e23d7c"></a>

### 78. Airplanes are US - 09E23D7C

Owner reference: Nod. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Air Force Command Headquarters (GAAIRC), owner Brits, cell (58, 86), tag 09E2378C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  #: 2.
2. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create Harrier Team (0ABC9EAC)](#trigger-0abc9eac).
2. Enable and reset applicable timers for [Play Tanya Air-Movie (0B936D4C)](#trigger-0b936d4c).
3. Destroy current instances of [Airplanes Destroyed (07AFE48C)](#trigger-07afe48c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4915, Events line 5001, Actions line 5087.

<a id="trigger-07afe48c"></a>

### 79. Airplanes Destroyed - 07AFE48C

Owner reference: British. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07AFBE6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 1.
2. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy current instances of [Create Harrier Team (0ABC9EAC)](#trigger-0abc9eac).
2. Destroy current instances of [Play Tanya Air-Movie (0B936D4C)](#trigger-0b936d4c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4916, Events line 5002, Actions line 5088.

<a id="trigger-0b22f0cc"></a>

### 80. Ambients 2 - 0B22F0CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B2290EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsNightOwl at waypoint 26 (cell 101, 64).
2. Play sound _Amb_WindPlains at waypoint 71 (cell 59, 68).
3. Play sound _Amb_WindCold at waypoint 72 (cell 66, 62).
4. Play sound _Amb_WindCold at waypoint 73 (cell 47, 85).
5. Play sound _Amb_WavesLake at waypoint 74 (cell 80, 88).
6. Play sound _Amb_BirdsNightOwl at waypoint 75 (cell 67, 117).
7. Play sound _Amb_WindPlains at waypoint 75 (cell 67, 117).
8. Play sound _Amb_WindCold at waypoint 77 (cell 70, 150).
9. Play sound _Amb_WindPlains at waypoint 78 (cell 73, 144).
10. Play sound _Amb_BirdsNightOwl at waypoint 79 (cell 77, 137).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4917, Events line 5003, Actions line 5089.

<a id="trigger-0b29af3c"></a>

### 81. Russian Harv Hit - 0B29AF3C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: War Miner (HARV), owner Russians, cell (113, 54), tag 0B29958C, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 8 (country/type RUSSIANS; placed owner Russians).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4918, Events line 5004, Actions line 5090.

<a id="trigger-0a27876c"></a>

### 82. Grizzly Check - 0A27876C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [Soviet 1st Strike (07B1F0AC)](#trigger-07b1f0ac).

Attached scope: tag definitions 07B18F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Unit Type: type index 9 (global list position: Grizzly Battle Tank (MTNK)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Create/recruit team [Soviet 1st Strike Team (09E58EFC)](all02s-teams.md#team-09e58efc).
2. Play music theme InDeep.

Source locator: MAPS01.MIX/all02s.map; Triggers line 4919, Events line 5005, Actions line 5091.

<a id="trigger-0d8bb57c"></a>

### 83. Chrono Miner Changes - 0D8BB57C

Owner reference: Nod. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Chrono Miner  (0CA2B03C)](#trigger-0ca2b03c).

Attached scope: Chrono Miner (CMIN), owner Nod, cell (62, 94), tag 0D8D260C, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4920, Events line 5006, Actions line 5092.

<a id="trigger-0ca2b03c"></a>

### 84. Enable Chrono Miner  - 0CA2B03C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Ore Refinery (GAREFN), owner Neutral2, cell (58, 93), tag 0CA5605C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Miner Changes (0D8BB57C)](#trigger-0d8bb57c).

Source locator: MAPS01.MIX/all02s.map; Triggers line 4921, Events line 5007, Actions line 5093.

[All team rosters and ordered plans](all02s-teams.md) | [All mission overrides](all02s-overrides.md)
