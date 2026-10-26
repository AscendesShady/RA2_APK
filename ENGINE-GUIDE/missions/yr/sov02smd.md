# Operation: Deja Vu

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for sov02smd.map.](../../images/map-sov02smd.svg)

*Initial placement schematic for sov02smd.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** sov02smd.map. **Effective extracted member:** mapsmd03.mix/sov02smd.map. **Trigger definitions:** 86.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov02smd-teams.md) | [All mission overrides](sov02smd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | SNOW |
| Map size | 0,0,105,105 |
| Visible local rectangle | 5,5,95,94 |
| Placed vehicles | 32 |
| Placed infantry | 41 |
| Placed structures | 139 |
| Placed aircraft | 0 |
| Team templates | 103 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 400 | BadGuy1 |
| 2 | BadGuy2 House | 400 | BadGuy2 |
| 3 | German1 House | 50 | Germany1 |
| 4 | Civilian House | 0 | Neutral |
| 5 | Einstein House | 100 | Einstein |
| 6 | BadGuy3 House | 400 | BadGuy3 |
| 7 | German2 House | 50 | Germany2 |
| 8 | German3 House | 50 | Germany3 |
| 9 | Temp House | 0 | Temp |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Refinery Owned,0 |
| 1 | BG1s Refinery,0 |
| 2 | BG2s Refinery,0 |
| 3 | BG2 ConYard Up,0 |
| 4 | Briefing Complete,0 |
| 5 | Chrono Prisons Go,0 |
| 6 | Transfer Chronosphe,0 |
| 7 | Einstein Lab KIA,0 |
| 8 | Chronosphere KIA,0 |
| 9 | Einstein Chrono Off,0 |
| 10 | Early Air Attks,0 |
| 11 | G1_Barracks_Gone,0 |
| 12 | G2_Barracks_Gone,0 |
| 13 | G3_Barracks_Gone,0 |
| 14 | Troops2_Arrived,0 |
| 15 | Troops1_Arrived,0 |
| 16 | Troops3_Arrived,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [_Lose (07D4D4AC)](#trigger-07d4d4ac) | Destroyed,  All: owner selector 15 (country/type PLAYER; placed owner Player House). | Declare owner selector 15 (country/type PLAYER; placed owner Player House) the loser. |
| [_Win (Mission Over) (0A3C3B8C)](#trigger-0a3c3b8c) | 10 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 15 (country/type PLAYER; placed owner Player House) the winner. |

## Every trigger, in file order

<a id="trigger-06b76d8c"></a>

### 1. Reclaimed Refinery (Player) - 06B76D8C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 15 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Refinery_Is_Players (0915344C)](#trigger-0915344c).
2. Create crate type 1 at waypoint 63 (cell 181, 126).
3. Play sound Bonus at waypoint 63 (cell 181, 126).
4. Set local flag 0 (Refinery Owned).
5. Enable and reset applicable timers for [Kill_Me (08E3167C)](#trigger-08e3167c).
6. Disable [Reclaimed Refinery (BG1) (06B755BC)](#trigger-06b755bc).
7. Disable [Reclaimed Refinery (BG2) (06B70CEC)](#trigger-06b70cec).
8. Disable [Refinery_Gone (08E3176C)](#trigger-08e3176c).
9. Disable [Reclaimed Refinery (Player) (06B76D8C)](#trigger-06b76d8c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9094, Events line 9182, Actions line 9270.

<a id="trigger-0915344c"></a>

### 2. Refinery_Is_Players - 0915344C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reclaimed Refinery (Player) (06B76D8C)](#trigger-06b76d8c).

Attached scope: tag definitions 09151CAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Change House: owner selector 15 (country/type PLAYER; placed owner Player House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9095, Events line 9183, Actions line 9271.

<a id="trigger-08e3167c"></a>

### 3. Kill_Me - 08E3167C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BG3 ConYard Killer (08D2B3BC)](#trigger-08d2b3bc).

Incoming activation links: enable from [Reclaimed Refinery (Player) (06B76D8C)](#trigger-06b76d8c); enable from [Refinery_Gone (08E3176C)](#trigger-08e3176c).

Attached scope: Allied Construction Yard (GACNST), owner BadGuy3 House, cell (59, 159), tag 08D2ACAC, persistence mode 2.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Disable [Kill_Me (08E3167C)](#trigger-08e3167c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9096, Events line 9184, Actions line 9272.

<a id="trigger-06b755bc"></a>

### 4. Reclaimed Refinery (BG1) - 06B755BC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Refinery (Player) (06B76D8C)](#trigger-06b76d8c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Change House: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).
2. Supply reinforcement team [Reclaimed Harvester BG1 (06B72DCC)](sov02smd-teams.md#team-06b72dcc).
3. Set local flag 0 (Refinery Owned).
4. Set local flag 1 (BG1s Refinery).
5. Disable [Reclaimed Refinery (BG2) (06B70CEC)](#trigger-06b70cec).
6. Disable [Reclaimed Refinery (BG1) (06B755BC)](#trigger-06b755bc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9097, Events line 9185, Actions line 9273.

<a id="trigger-06b70cec"></a>

### 5. Reclaimed Refinery (BG2) - 06B70CEC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Refinery (BG1) (06B755BC)](#trigger-06b755bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).

**Then perform these actions in order:**

1. Change House: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).
2. Supply reinforcement team [Reclaimed Harvester BG1 (06B72DCC)](sov02smd-teams.md#team-06b72dcc).
3. Set local flag 0 (Refinery Owned).
4. Set local flag 2 (BG2s Refinery).
5. Disable [Reclaimed Refinery (BG1) (06B755BC)](#trigger-06b755bc).
6. Disable [Reclaimed Refinery (BG2) (06B70CEC)](#trigger-06b70cec).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9098, Events line 9186, Actions line 9274.

<a id="trigger-08e3176c"></a>

### 6. Refinery_Gone - 08E3176C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Reclaimed Refinery (BG2) (06B70CEC)](#trigger-06b70cec).

Attached scope: Allied Ore Refinery (GAREFN), owner Civilian House, cell (178, 128), tag 06B7570C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Kill_Me (08E3167C)](#trigger-08e3167c).
2. Disable [Reclaimed Refinery (BG1) (06B755BC)](#trigger-06b755bc).
3. Disable [Reclaimed Refinery (BG2) (06B70CEC)](#trigger-06b70cec).
4. Disable [Reclaimed Refinery (Player) (06B76D8C)](#trigger-06b76d8c).
5. Disable [Refinery_Gone (08E3176C)](#trigger-08e3176c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9099, Events line 9187, Actions line 9275.

<a id="trigger-08d2b3bc"></a>

### 7. BG3 ConYard Killer - 08D2B3BC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.
2. Disable [BG3 ConYard Killer (08D2B3BC)](#trigger-08d2b3bc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9100, Events line 9188, Actions line 9276.

<a id="trigger-0b5ed59c"></a>

### 8. Refinery Owned - 0B5ED59C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B5EFB5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Refinery Owned) is set.

Flag writers in this mission: set local flag 0 (Refinery Owned) at [Reclaimed Refinery (Player) (06B76D8C)](#trigger-06b76d8c); set local flag 0 (Refinery Owned) at [Reclaimed Refinery (BG1) (06B755BC)](#trigger-06b755bc); set local flag 0 (Refinery Owned) at [Reclaimed Refinery (BG2) (06B70CEC)](#trigger-06b70cec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Stop location sound 63 at waypoint 63 (cell 181, 126).
2. Disable [Refinery Grabber BG1 (Easy) (0882EBAC)](#trigger-0882ebac).
3. Disable [Refinery Grabber BG1 (Hrd) (0882E27C)](#trigger-0882e27c).
4. Disable [Refinery Grabber BG1 (Med) (0882E58C)](#trigger-0882e58c).
5. Remove instances of the team organization (not automatically its surviving objects) [Refinery Grabber BG1 (0437EE9C)](sov02smd-teams.md#team-0437ee9c).
6. Disable [Refinery Grabber BG2 (Easy) (0881FD3C)](#trigger-0881fd3c).
7. Disable [Refinery Grabber BG2 (Hrd) (0881F32C)](#trigger-0881f32c).
8. Disable [Refinery Grabber BG2 (Med) (0881F6EC)](#trigger-0881f6ec).
9. Remove instances of the team organization (not automatically its surviving objects) [Refinery Grabber BG2 (0437CD8C)](sov02smd-teams.md#team-0437cd8c).
10. Disable [BG2 Refinery Grabber On (0437C61C)](#trigger-0437c61c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9101, Events line 9189, Actions line 9277.

<a id="trigger-0882ebac"></a>

### 9. Refinery Grabber BG1 (Easy) - 0882EBAC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 720 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Refinery Grabber BG1 (0437EE9C)](sov02smd-teams.md#team-0437ee9c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9102, Events line 9190, Actions line 9278.

<a id="trigger-0882e27c"></a>

### 10. Refinery Grabber BG1 (Hrd) - 0882E27C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Refinery Grabber BG1 (Med) (0882E58C)](#trigger-0882e58c).

Attached scope: tag definitions 0882E67C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Refinery Grabber BG1 (0437EE9C)](sov02smd-teams.md#team-0437ee9c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9103, Events line 9191, Actions line 9279.

<a id="trigger-0882e58c"></a>

### 11. Refinery Grabber BG1 (Med) - 0882E58C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Refinery Grabber BG1 (Easy) (0882EBAC)](#trigger-0882ebac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Refinery Grabber BG1 (0437EE9C)](sov02smd-teams.md#team-0437ee9c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9104, Events line 9192, Actions line 9280.

<a id="trigger-0881fd3c"></a>

### 12. Refinery Grabber BG2 (Easy) - 0881FD3C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG2 Refinery Grabber On (0437C61C)](#trigger-0437c61c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 720 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Refinery Grabber BG2 (0437CD8C)](sov02smd-teams.md#team-0437cd8c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9105, Events line 9193, Actions line 9281.

<a id="trigger-0881f32c"></a>

### 13. Refinery Grabber BG2 (Hrd) - 0881F32C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Refinery Grabber BG2 (Med) (0881F6EC)](#trigger-0881f6ec).

Incoming activation links: enable from [BG2 Refinery Grabber On (0437C61C)](#trigger-0437c61c).

Attached scope: tag definitions 0881F7DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Refinery Grabber BG2 (0437CD8C)](sov02smd-teams.md#team-0437cd8c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9106, Events line 9194, Actions line 9282.

<a id="trigger-0881f6ec"></a>

### 14. Refinery Grabber BG2 (Med) - 0881F6EC

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Refinery Grabber BG2 (Easy) (0881FD3C)](#trigger-0881fd3c).

Incoming activation links: enable from [BG2 Refinery Grabber On (0437C61C)](#trigger-0437c61c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Refinery Grabber BG2 (0437CD8C)](sov02smd-teams.md#team-0437cd8c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9107, Events line 9195, Actions line 9283.

<a id="trigger-0437c61c"></a>

### 15. BG2 Refinery Grabber On - 0437C61C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0437D90C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (BG2 ConYard Up) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Refinery Grabber BG2 (Easy) (0881FD3C)](#trigger-0881fd3c).
2. Enable and reset applicable timers for [Refinery Grabber BG2 (Hrd) (0881F32C)](#trigger-0881f32c).
3. Enable and reset applicable timers for [Refinery Grabber BG2 (Med) (0881F6EC)](#trigger-0881f6ec).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9108, Events line 9196, Actions line 9284.

<a id="trigger-0b5ee99c"></a>

### 16. Crate at BM - 0B5EE99C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (54, 148); tag 043710AC, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 64 (cell 54, 148).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9109, Events line 9197, Actions line 9285.

<a id="trigger-0c2af54c"></a>

### 17. BG2 MCV Deployment (Easy) - 0C2AF54C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [BG2 MCV Deployement (0A011CBC)](sov02smd-teams.md#team-0a011cbc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9110, Events line 9198, Actions line 9286.

<a id="trigger-0c2a649c"></a>

### 18. BG2 MCV Deployment (M_H) - 0C2A649C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [BG2 MCV Deployment (Easy) (0C2AF54C)](#trigger-0c2af54c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [BG2 MCV Deployement (0A011CBC)](sov02smd-teams.md#team-0a011cbc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9111, Events line 9199, Actions line 9287.

<a id="trigger-0c2c797c"></a>

### 19. BG2 MCV Deployment (attkd) - 0C2C797C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BG2 MCV Deployment (M_H) (0C2A649C)](#trigger-0c2a649c).

Attached scope: Allied Construction Vehicle (AMCV), owner BadGuy2 House, cell (115, 130), tag 0C2AF46C, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [BG2 MCV Deployement (0A011CBC)](sov02smd-teams.md#team-0a011cbc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9112, Events line 9200, Actions line 9288.

<a id="trigger-0aa91b1c"></a>

### 20. BG2 Production Start - 0AA91B1C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AA916AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 2 (global list position: Allied Construction Yard (GACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Production Begins: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).
2. AI triggers begin: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).
3. Make enemy: owner selector 15 (country/type PLAYER; placed owner Player House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9113, Events line 9201, Actions line 9289.

<a id="trigger-0aa915bc"></a>

### 21. BG1 Production Start - 0AA915BC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1st Battle Fort Attk Go (0437882C)](#trigger-0437882c).

Attached scope: tag definitions 0AA9672C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9114, Events line 9202, Actions line 9290.

<a id="trigger-0882e07c"></a>

### 22. BG3 Production Start (BG1) - 0882E07C

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [BG3 Power Supply (Off) (06B0A1BC)](#trigger-06b0a1bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 1 (BG1s Refinery) is set.

Flag writers in this mission: set local flag 1 (BG1s Refinery) at [Reclaimed Refinery (BG1) (06B755BC)](#trigger-06b755bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 18 (country/type BADGUY3; placed owner BadGuy3 House).
2. Production Begins: owner selector 18 (country/type BADGUY3; placed owner BadGuy3 House).
3. Disable [BG3 Production Start (BG1) (0882E07C)](#trigger-0882e07c).
4. Disable [BG3 Production Start (BG2) (0AF468CC)](#trigger-0af468cc).
5. Enable and reset applicable timers for [BG3 Power Supply (Off) (06B0A1BC)](#trigger-06b0a1bc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9115, Events line 9203, Actions line 9291.

<a id="trigger-06b0a1bc"></a>

### 23. BG3 Power Supply (Off) - 06B0A1BC

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG3 Production Start (BG1) (0882E07C)](#trigger-0882e07c); enable from [BG3 Production Start (BG2) (0AF468CC)](#trigger-0af468cc); enable from [BG3 Power Supply (On) (08C5D25C)](#trigger-08c5d25c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Low Power: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Change House: owner selector 22 (country/type TEMP; placed owner Temp House).
2. Disable [BG3 Power Supply (Off) (06B0A1BC)](#trigger-06b0a1bc).
3. Enable and reset applicable timers for [BG3 Power Supply (On) (08C5D25C)](#trigger-08c5d25c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9116, Events line 9204, Actions line 9292.

<a id="trigger-0af468cc"></a>

### 24. BG3 Production Start (BG2) - 0AF468CC

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: [BG3 Production Start (BG1) (0882E07C)](#trigger-0882e07c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 2 (BG2s Refinery) is set.

Flag writers in this mission: set local flag 2 (BG2s Refinery) at [Reclaimed Refinery (BG2) (06B70CEC)](#trigger-06b70cec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 18 (country/type BADGUY3; placed owner BadGuy3 House).
2. Production Begins: owner selector 18 (country/type BADGUY3; placed owner BadGuy3 House).
3. Disable [BG3 Production Start (BG2) (0AF468CC)](#trigger-0af468cc).
4. Disable [BG3 Production Start (BG1) (0882E07C)](#trigger-0882e07c).
5. Enable and reset applicable timers for [BG3 Power Supply (Off) (06B0A1BC)](#trigger-06b0a1bc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9117, Events line 9205, Actions line 9293.

<a id="trigger-08c5d25c"></a>

### 25. BG3 Power Supply (On) - 08C5D25C

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BG3 Production Start (BG2) (0AF468CC)](#trigger-0af468cc).

Incoming activation links: enable from [BG3 Power Supply (Off) (06B0A1BC)](#trigger-06b0a1bc).

Attached scope: Power Plant (GAPOWR), owner Temp House, cell (57, 159), tag 06B0CBFC, persistence mode 2; Power Plant (GAPOWR), owner Temp House, cell (57, 157), tag 06B0CBFC, persistence mode 2; Power Plant (GAPOWR), owner Temp House, cell (59, 157), tag 06B0CBFC, persistence mode 2; Power Plant (GAPOWR), owner Temp House, cell (61, 163), tag 06B0CBFC, persistence mode 2; Power Plant (GAPOWR), owner Temp House, cell (63, 163), tag 06B0CBFC, persistence mode 2; Power Plant (GAPOWR), owner Temp House, cell (63, 161), tag 06B0CBFC, persistence mode 2.

**Wait for the recorded events:**

1. Power Full: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Change House: owner selector 18 (country/type BADGUY3; placed owner BadGuy3 House).
2. Disable [BG3 Power Supply (On) (08C5D25C)](#trigger-08c5d25c).
3. Enable and reset applicable timers for [BG3 Power Supply (Off) (06B0A1BC)](#trigger-06b0a1bc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9118, Events line 9206, Actions line 9294.

<a id="trigger-0d4ed32c"></a>

### 26. _Briefing 0 - 0D4ED32C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (118, 131); tag 0D4EAA7C, persistence mode 0.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Disable player input.
2. Reveal terrain around waypoint 98 (cell 109, 20).
3. Supply reinforcement team [Player Starters 2Armor (0437C33C)](sov02smd-teams.md#team-0437c33c).
4. Supply reinforcement team [Player Starters 1Armor (0AD50DEC)](sov02smd-teams.md#team-0ad50dec).
5. Supply reinforcement team [Player Starters 3Armor (0437A6BC)](sov02smd-teams.md#team-0437a6bc).
6. Create/recruit team [Rocketeer_Guard_CK (07909EFC)](sov02smd-teams.md#team-07909efc).
7. Create/recruit team [Rocketeer_Guard_CL (0BEF16CC)](sov02smd-teams.md#team-0bef16cc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9119, Events line 9207, Actions line 9295.

<a id="trigger-06bce16c"></a>

### 27. _Briefing 1 - 06BCE16C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 088B789C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Jump the camera to waypoint 1 (cell 80, 58).
2. Play sound CameraSwitch.
3. Create radar-event marker type 5 at waypoint 1 (cell 80, 58).
4. Play voice notification Mis_xS2_ZofiaBriefing01.
5. Reveal terrain around waypoint 1 (cell 80, 58).
6. Create/recruit team [Rocketeer_Guard_CK (07909EFC)](sov02smd-teams.md#team-07909efc).
7. Create/recruit team [Rocketeer_Guard_CL (0BEF16CC)](sov02smd-teams.md#team-0bef16cc).
8. Display message “Objective 1: Destroy the outposts guarding the German border.” (MISSION:Sov2Obj1).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9120, Events line 9208, Actions line 9296.

<a id="trigger-088b897c"></a>

### 28. _Briefing 2 - 088B897C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 088B808C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Jump the camera to waypoint 2 (cell 110, 41).
2. Play sound CameraSwitch.
3. Create radar-event marker type 5 at waypoint 2 (cell 110, 41).
4. Reveal terrain around waypoint 2 (cell 110, 41).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9121, Events line 9209, Actions line 9297.

<a id="trigger-088aff3c"></a>

### 29. _Briefing 3 - 088AFF3C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 088B52DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Jump the camera to waypoint 3 (cell 145, 72).
2. Play sound CameraSwitch.
3. Create radar-event marker type 5 at waypoint 3 (cell 145, 72).
4. Reveal terrain around waypoint 3 (cell 145, 72).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9122, Events line 9210, Actions line 9298.

<a id="trigger-0883e72c"></a>

### 30. _Briefing 4 - 0883E72C

Owner reference: Einstein. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0883E43C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 26 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 5 (cell 100, 174).
2. Play sound CameraSwitch.
3. Create radar-event marker type 5 at waypoint 5 (cell 100, 174).
4. Reveal terrain around waypoint 19 (cell 102, 176).
5. Play voice notification Mis_xS2_ZofiaBriefing03.
6. Flash buildings of type CALAB; duration argument 60.
7. Flash buildings of type GACSPH; duration argument 60.
8. Display message “Objective 2: Destroy Einstein's Lab and Chronosphere.” (MISSION:Sov2Obj2).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9123, Events line 9211, Actions line 9299.

<a id="trigger-0883fbac"></a>

### 31. _Briefing 6 (Send in Troops Again) - 0883FBAC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0883F7EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 65 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Jump the camera to waypoint 98 (cell 109, 20).
2. Play sound CameraSwitch.
3. Supply reinforcement team [Player Starters 1Troops (078BB93C)](sov02smd-teams.md#team-078bb93c).
4. Supply reinforcement team [Player Starters 2Troops (078BCEFC)](sov02smd-teams.md#team-078bcefc).
5. Supply reinforcement team [Player Starters 3Troops (078BC7BC)](sov02smd-teams.md#team-078bc7bc).
6. Set local flag 4 (Briefing Complete).
7. Play voice notification Mis_xS2_ZofiaBriefing02.
8. Play sound BeaconPlaced.
9. Create radar-event marker type 0 at waypoint 10 (cell 82, 41).
10. Create radar-event marker type 0 at waypoint 14 (cell 161, 69).
11. Create radar-event marker type 0 at waypoint 98 (cell 109, 20).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9124, Events line 9212, Actions line 9300.

<a id="trigger-0883f17c"></a>

### 32. _Briefing 5 (Send in Troops) - 0883F17C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A82B89C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Jump the camera to waypoint 4 (cell 114, 126).
2. Play sound CameraSwitch.
3. Create radar-event marker type 5 at waypoint 4 (cell 114, 126).
4. Supply reinforcement team [Player Starters 1Troops (078BB93C)](sov02smd-teams.md#team-078bb93c).
5. Supply reinforcement team [Player Starters 2Troops (078BCEFC)](sov02smd-teams.md#team-078bcefc).
6. Supply reinforcement team [Player Starters 3Troops (078BC7BC)](sov02smd-teams.md#team-078bc7bc).
7. Reveal terrain around waypoint 4 (cell 114, 126).
8. Reveal terrain around waypoint 15 (cell 112, 128).
9. Reveal terrain around waypoint 16 (cell 118, 128).
10. Reveal terrain around waypoint 17 (cell 112, 124).
11. Reveal terrain around waypoint 18 (cell 118, 124).
12. Play voice notification Mis_xS2_ZofiaBriefing04.

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9125, Events line 9213, Actions line 9301.

<a id="trigger-0883e27c"></a>

### 33. _Briefing 7 (Enable Game) - 0883E27C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0884085C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (Briefing Complete) is set.

Flag writers in this mission: set local flag 4 (Briefing Complete) at [_Briefing 6 (Send in Troops Again) (0883FBAC)](#trigger-0883fbac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Briefing 8 (Briefing Over) (0884076C)](#trigger-0884076c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9126, Events line 9214, Actions line 9302.

<a id="trigger-0884076c"></a>

### 34. _Briefing 8 (Briefing Over) - 0884076C

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Briefing 7 (Enable Game) (0883E27C)](#trigger-0883e27c).

Attached scope: tag definitions 0884046C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Germany3 Tank Destroyers Go (H) (0437980C)](#trigger-0437980c).
2. Enable and reset applicable timers for [Germany3 Tank Destroyers Go (M) (0B6830CC)](#trigger-0b6830cc).
3. Enable and reset applicable timers for [Germany1 Production Start (0A4B6D9C)](#trigger-0a4b6d9c).
4. Enable and reset applicable timers for [Germany2 Production Start (0A4B69BC)](#trigger-0a4b69bc).
5. Enable and reset applicable timers for [Germany3 Production Start (0A4B62AC)](#trigger-0a4b62ac).
6. Create/recruit team [BG1 Base Patrol (08D2D7EC)](sov02smd-teams.md#team-08d2d7ec).
7. Play voice notification EVA_BattlefieldControlOnline.
8. Enable player input.
9. Enable and reset applicable timers for [_Lose (07D4D4AC)](#trigger-07d4d4ac).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9127, Events line 9215, Actions line 9303.

<a id="trigger-0437980c"></a>

### 35. Germany3 Tank Destroyers Go (H) - 0437980C

Owner reference: Germany3. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Briefing 8 (Briefing Over) (0884076C)](#trigger-0884076c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [German3 Tank Destroyers (0437B71C)](sov02smd-teams.md#team-0437b71c).
2. Make enemy: owner selector 15 (country/type PLAYER; placed owner Player House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9128, Events line 9216, Actions line 9304.

<a id="trigger-0b6830cc"></a>

### 36. Germany3 Tank Destroyers Go (M) - 0B6830CC

Owner reference: Germany3. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Germany3 Tank Destroyers Go (H) (0437980C)](#trigger-0437980c).

Incoming activation links: enable from [_Briefing 8 (Briefing Over) (0884076C)](#trigger-0884076c).

Attached scope: tag definitions 0437925C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [German3 Tank Destroyers (0437B71C)](sov02smd-teams.md#team-0437b71c).
2. Make enemy: owner selector 15 (country/type PLAYER; placed owner Player House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9129, Events line 9217, Actions line 9305.

<a id="trigger-0a4b6d9c"></a>

### 37. Germany1 Production Start - 0A4B6D9C

Owner reference: Germany1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Briefing 8 (Briefing Over) (0884076C)](#trigger-0884076c).

Attached scope: tag definitions 0A4B6AAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 11 (G1_Barracks_Gone) is clear.

Flag writers in this mission: set local flag 11 (G1_Barracks_Gone) at [G1_Barracks_Gone (078C61EC)](#trigger-078c61ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Make enemy: owner selector 15 (country/type PLAYER; placed owner Player House).
2. Production Begins: owner selector 19 (country/type GERMANY1; placed owner German1 House).
3. AI triggers begin: owner selector 19 (country/type GERMANY1; placed owner German1 House).
4. Create/recruit team [German1 Infantry Defenders (0A4B243C)](sov02smd-teams.md#team-0a4b243c).
5. Supply reinforcement team [German1 Infantry Attackers (0AE83EFC)](sov02smd-teams.md#team-0ae83efc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9130, Events line 9218, Actions line 9306.

<a id="trigger-0a4b69bc"></a>

### 38. Germany2 Production Start - 0A4B69BC

Owner reference: Germany2. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Briefing 8 (Briefing Over) (0884076C)](#trigger-0884076c).

Attached scope: tag definitions 0A4B639C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 12 (G2_Barracks_Gone) is clear.

Flag writers in this mission: set local flag 12 (G2_Barracks_Gone) at [G2_Barracks_Gone (078C6D8C)](#trigger-078c6d8c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Make enemy: owner selector 15 (country/type PLAYER; placed owner Player House).
2. Production Begins: owner selector 20 (country/type GERMANY2; placed owner German2 House).
3. AI triggers begin: owner selector 20 (country/type GERMANY2; placed owner German2 House).
4. Create/recruit team [German2 Infantry Defenders (0A4B5DEC)](sov02smd-teams.md#team-0a4b5dec).
5. Supply reinforcement team [German2 Infantry Attackers (0AE83A4C)](sov02smd-teams.md#team-0ae83a4c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9131, Events line 9219, Actions line 9307.

<a id="trigger-0a4b62ac"></a>

### 39. Germany3 Production Start - 0A4B62AC

Owner reference: Germany3. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Briefing 8 (Briefing Over) (0884076C)](#trigger-0884076c).

Attached scope: tag definitions 0A4B5D2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 13 (G3_Barracks_Gone) is clear.

Flag writers in this mission: set local flag 13 (G3_Barracks_Gone) at [G3_Barracks_Gone (078C6A5C)](#trigger-078c6a5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Make enemy: owner selector 15 (country/type PLAYER; placed owner Player House).
2. Production Begins: owner selector 21 (country/type GERMANY3; placed owner German3 House).
3. AI triggers begin: owner selector 21 (country/type GERMANY3; placed owner German3 House).
4. Create/recruit team [German3 Infantry Defenders (0A4B5CBC)](sov02smd-teams.md#team-0a4b5cbc).
5. Supply reinforcement team [German3 Infantry Attackers (0AE8391C)](sov02smd-teams.md#team-0ae8391c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9132, Events line 9220, Actions line 9308.

<a id="trigger-07d4d4ac"></a>

### 40. _Lose - 07D4D4AC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Briefing 8 (Briefing Over) (0884076C)](#trigger-0884076c).

Attached scope: tag definitions 07D5428C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 15 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Declare owner selector 15 (country/type PLAYER; placed owner Player House) the loser.

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9133, Events line 9221, Actions line 9309.

<a id="trigger-08d2f8bc"></a>

### 41. Player MCV Reinforcment_E - 08D2F8BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Delay_Reinforcement (095031DC)](#trigger-095031dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 21 (country/type GERMANY3; placed owner German3 House).
2. Destroyed,  All: owner selector 19 (country/type GERMANY1; placed owner German1 House).
3. Destroyed,  All: owner selector 20 (country/type GERMANY2; placed owner German2 House).

**Then perform these actions in order:**

1. Supply reinforcement team [Player MCV Reinforcments (0A0E17BC)](sov02smd-teams.md#team-0a0e17bc).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Create radar-event marker type 1 at waypoint 98 (cell 109, 20).
4. Create crate type 0 at waypoint 2 (cell 110, 41).
5. Create crate type 0 at waypoint 85 (cell 111, 41).
6. Create crate type 0 at waypoint 86 (cell 110, 40).
7. Create crate type 0 at waypoint 87 (cell 111, 40).
8. Play sound Bonus at waypoint 2 (cell 110, 41).
9. Enable and reset applicable timers for [Objective2_Text (07A3EA2C)](#trigger-07a3ea2c).
10. Enable and reset applicable timers for [Center_On_MCV (077FF39C)](#trigger-077ff39c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9134, Events line 9222, Actions line 9310.

<a id="trigger-07a3ea2c"></a>

### 42. Objective2_Text - 07A3EA2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player MCV Reinforcment_E (08D2F8BC)](#trigger-08d2f8bc); enable from [Player MCV Reinforcment_M (094B91CC)](#trigger-094b91cc); enable from [Player MCV Reinforcment_H (094BA1DC)](#trigger-094ba1dc).

Attached scope: tag definitions 07A3E50C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy Einstein's Lab and Chronosphere.” (MISSION:Sov2Obj2).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9135, Events line 9223, Actions line 9311.

<a id="trigger-077ff39c"></a>

### 43. Center_On_MCV - 077FF39C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player MCV Reinforcment_E (08D2F8BC)](#trigger-08d2f8bc); enable from [Player MCV Reinforcment_M (094B91CC)](#trigger-094b91cc); enable from [Player MCV Reinforcment_H (094BA1DC)](#trigger-094ba1dc).

Attached scope: tag definitions 077F8D4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 98 (cell 109, 20).
2. Play sound CameraSwitch.

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9136, Events line 9224, Actions line 9312.

<a id="trigger-08d2c96c"></a>

### 44. BG1 Check on Germans - 08D2C96C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08D2C0AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 19 (country/type GERMANY1; placed owner German1 House).
2. Destroyed,  All: owner selector 20 (country/type GERMANY2; placed owner German2 House).
3. Destroyed,  All: owner selector 21 (country/type GERMANY3; placed owner German3 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 German Check Team (079504DC)](#trigger-079504dc).
2. Enable and reset applicable timers for [BG1 Hill Holders Go (08D2AC9C)](#trigger-08d2ac9c).
3. Enable and reset applicable timers for [1st Battle Fort Attk Go (0437882C)](#trigger-0437882c).
4. Supply reinforcement team [Ptrl_Einstein01 (0B518B7C)](sov02smd-teams.md#team-0b518b7c).
5. Supply reinforcement team [Ptrl_LFlank01 (0B51987C)](sov02smd-teams.md#team-0b51987c).
6. Supply reinforcement team [Ptrl_RFlank01 (0B51848C)](sov02smd-teams.md#team-0b51848c).
7. Supply reinforcement team [BG1 Check on G1 (09479E6C)](sov02smd-teams.md#team-09479e6c).
8. Supply reinforcement team [BG1 Check on G3 (0947BD7C)](sov02smd-teams.md#team-0947bd7c).
9. Enable and reset applicable timers for [BG1 Early Attks (094558EC)](#trigger-094558ec).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9137, Events line 9225, Actions line 9313.

<a id="trigger-079504dc"></a>

### 45. BG1 German Check Team - 079504DC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Check on Germans (08D2C96C)](#trigger-08d2c96c).

Attached scope: tag definitions 09A4F7EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 Check on Germans (0B517A4C)](sov02smd-teams.md#team-0b517a4c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9138, Events line 9226, Actions line 9314.

<a id="trigger-08d2ac9c"></a>

### 46. BG1 Hill Holders Go - 08D2AC9C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Check on Germans (08D2C96C)](#trigger-08d2c96c).

Attached scope: tag definitions 08D2AA7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Hill Holders (0B41AEFC)](sov02smd-teams.md#team-0b41aefc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9139, Events line 9227, Actions line 9315.

<a id="trigger-0437882c"></a>

### 47. 1st Battle Fort Attk Go - 0437882C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Check on Germans (08D2C96C)](#trigger-08d2c96c); enable from [Battlefortress_Found (078370FC)](#trigger-078370fc).

Attached scope: tag definitions 0437CABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [1st Battle Fort Attk (098F40EC)](sov02smd-teams.md#team-098f40ec).
2. Create/recruit team [1st Battle Fort Attk 02 (0990A93C)](sov02smd-teams.md#team-0990a93c).
3. Reveal terrain around waypoint 40 (cell 112, 82).
4. Perform no action.
5. Create radar-event marker type 5 at waypoint 40 (cell 112, 82).
6. Play voice notification Unit_Sofia_BattleFortress.
7. Enable and reset applicable timers for [Mirage Warning Audio (0AC7C6EC)](#trigger-0ac7c6ec).
8. Enable and reset applicable timers for [BG1 Production Start (0AA915BC)](#trigger-0aa915bc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9140, Events line 9228, Actions line 9316.

<a id="trigger-094558ec"></a>

### 48. BG1 Early Attks - 094558EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Check on Germans (08D2C96C)](#trigger-08d2c96c).

Attached scope: tag definitions 09453BCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 Early Attks 01 (08CF47CC)](#trigger-08cf47cc).
2. Enable and reset applicable timers for [BG1 Early Attks 02 (08CF3B4C)](#trigger-08cf3b4c).
3. Supply reinforcement team [BG1 Early Attk Air (0B831B7C)](sov02smd-teams.md#team-0b831b7c).
4. Set local flag 10 (Early Air Attks).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9141, Events line 9229, Actions line 9317.

<a id="trigger-0ac7c6ec"></a>

### 49. Mirage Warning Audio - 0AC7C6EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1st Battle Fort Attk Go (0437882C)](#trigger-0437882c).

Attached scope: tag definitions 0AC7C0DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 26 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Unit_Sofia_MirageTank.
2. Enable and reset applicable timers for [Mirage Warning Go (0B5F81EC)](#trigger-0b5f81ec).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9142, Events line 9230, Actions line 9318.

<a id="trigger-08cf47cc"></a>

### 50. BG1 Early Attks 01 - 08CF47CC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Early Attks (094558EC)](#trigger-094558ec).

Attached scope: tag definitions 08CF46EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 Early Attk 01 (0909945C)](sov02smd-teams.md#team-0909945c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9143, Events line 9231, Actions line 9319.

<a id="trigger-08cf3b4c"></a>

### 51. BG1 Early Attks 02 - 08CF3B4C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Early Attks (094558EC)](#trigger-094558ec).

Attached scope: tag definitions 08CF376C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 Early Attk 02 (094579DC)](sov02smd-teams.md#team-094579dc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9144, Events line 9232, Actions line 9320.

<a id="trigger-0b5f81ec"></a>

### 52. Mirage Warning Go - 0B5F81EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Mirage Warning Audio (0AC7C6EC)](#trigger-0ac7c6ec).

Attached scope: tag definitions 0B5FC80C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Mirage Warning (08F91C8C)](sov02smd-teams.md#team-08f91c8c).
2. Enable and reset applicable timers for [Delay_Reinforcement (095031DC)](#trigger-095031dc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9145, Events line 9233, Actions line 9321.

<a id="trigger-095031dc"></a>

### 53. Delay_Reinforcement - 095031DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Mirage Warning Go (0B5F81EC)](#trigger-0b5f81ec).

Attached scope: tag definitions 0950016C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Player MCV Reinforcment_M (094B91CC)](#trigger-094b91cc).
2. Enable and reset applicable timers for [Player MCV Reinforcment_E (08D2F8BC)](#trigger-08d2f8bc).
3. Enable and reset applicable timers for [Player MCV Reinforcment_H (094BA1DC)](#trigger-094ba1dc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9146, Events line 9234, Actions line 9322.

<a id="trigger-094b91cc"></a>

### 54. Player MCV Reinforcment_M - 094B91CC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Player MCV Reinforcment_E (08D2F8BC)](#trigger-08d2f8bc).

Incoming activation links: enable from [Delay_Reinforcement (095031DC)](#trigger-095031dc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 21 (country/type GERMANY3; placed owner German3 House).
2. Destroyed,  All: owner selector 20 (country/type GERMANY2; placed owner German2 House).
3. Destroyed,  All: owner selector 19 (country/type GERMANY1; placed owner German1 House).

**Then perform these actions in order:**

1. Supply reinforcement team [Player MCV Reinforcments (0A0E17BC)](sov02smd-teams.md#team-0a0e17bc).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Create radar-event marker type 1 at waypoint 98 (cell 109, 20).
4. Create crate type 0 at waypoint 2 (cell 110, 41).
5. Create crate type 0 at waypoint 85 (cell 111, 41).
6. Play sound Bonus at waypoint 2 (cell 110, 41).
7. Enable and reset applicable timers for [Objective2_Text (07A3EA2C)](#trigger-07a3ea2c).
8. Enable and reset applicable timers for [Center_On_MCV (077FF39C)](#trigger-077ff39c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9147, Events line 9235, Actions line 9323.

<a id="trigger-094ba1dc"></a>

### 55. Player MCV Reinforcment_H - 094BA1DC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Player MCV Reinforcment_M (094B91CC)](#trigger-094b91cc).

Incoming activation links: enable from [Delay_Reinforcement (095031DC)](#trigger-095031dc).

Attached scope: tag definitions 08D2F27C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 21 (country/type GERMANY3; placed owner German3 House).
2. Destroyed,  All: owner selector 20 (country/type GERMANY2; placed owner German2 House).
3. Destroyed,  All: owner selector 19 (country/type GERMANY1; placed owner German1 House).

**Then perform these actions in order:**

1. Supply reinforcement team [Player MCV Reinforcments (0A0E17BC)](sov02smd-teams.md#team-0a0e17bc).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Create radar-event marker type 1 at waypoint 98 (cell 109, 20).
4. Enable and reset applicable timers for [Objective2_Text (07A3EA2C)](#trigger-07a3ea2c).
5. Enable and reset applicable timers for [Center_On_MCV (077FF39C)](#trigger-077ff39c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9148, Events line 9236, Actions line 9324.

<a id="trigger-0a0c3e5c"></a>

### 56. Chronosphere Transfer - 0A0C3E5C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Power Plant (GAPOWR), owner Einstein House, cell (103, 176), tag 0A0C3CAC, persistence mode 0; Power Plant (GAPOWR), owner Einstein House, cell (96, 176), tag 0A0C3CAC, persistence mode 0; Chrono Sphere (GACSPH), owner Einstein House, cell (98, 177), tag 0A0C3CAC, persistence mode 0.

**Wait for the recorded events:**

1. local flag 6 (Transfer Chronosphe) is set.

**Then perform these actions in order:**

1. Change House: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).
2. Play voice notification Mis_xS2_ZofiaChronosphere.
3. Enable and reset applicable timers for [_Win (BG2 Chronosphere KIA) (0439E1BC)](#trigger-0439e1bc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9149, Events line 9237, Actions line 9325.

<a id="trigger-0439e1bc"></a>

### 57. _Win (BG2 Chronosphere KIA) - 0439E1BC

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chronosphere Transfer (0A0C3E5C)](#trigger-0a0c3e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building does not exist: type index 27 (global list position: Chrono Sphere (GACSPH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 8 (Chronosphere KIA).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9150, Events line 9238, Actions line 9326.

<a id="trigger-0a0c334c"></a>

### 58. Chronosphere Timer Hack - 0A0C334C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A0C312C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Chronosphere Timer Hack (0B8486FC)](sov02smd-teams.md#team-0b8486fc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9151, Events line 9239, Actions line 9327.

<a id="trigger-0439777c"></a>

### 59. _Win (Einstein Lab KIA) - 0439777C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Einstein's Laboratory (CALAB), owner Einstein House, cell (99, 173), tag 0439B62C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 7 (Einstein Lab KIA).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9152, Events line 9240, Actions line 9328.

<a id="trigger-0439c2cc"></a>

### 60. _Win (Cheer) - 0439C2CC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Win (Check) (07B14C3C)](#trigger-07b14c3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 15 (country/type PLAYER; placed owner Player House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9153, Events line 9241, Actions line 9329.

<a id="trigger-0a3c3b8c"></a>

### 61. _Win (Mission Over) - 0A3C3B8C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Win (Check) (07B14C3C)](#trigger-07b14c3c).

Attached scope: tag definitions 0A3C365C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 15 (country/type PLAYER; placed owner Player House) the winner.

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9154, Events line 9242, Actions line 9330.

<a id="trigger-08bc0c2c"></a>

### 62. _Win (Einstein Chronosphere KIA) - 08BC0C2C

Owner reference: Einstein. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [_Win (BG2 Chronosphere KIA) (0439E1BC)](#trigger-0439e1bc).

Attached scope: tag definitions 0439ECBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 27 (global list position: Chrono Sphere (GACSPH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 8 (Chronosphere KIA).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9155, Events line 9243, Actions line 9331.

<a id="trigger-08c5eb3c"></a>

### 63. Chrono Transfer Win Switch - 08C5EB3C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08C5E20C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (Einstein Chrono Off) is set.

**Then perform these actions in order:**

1. Disable [_Win (Einstein Chronosphere KIA) (08BC0C2C)](#trigger-08bc0c2c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9156, Events line 9244, Actions line 9332.

<a id="trigger-0c26610c"></a>

### 64. BG2 Garrison Barn - 0C26610C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C26C8DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 3 (global list position: Allied Barracks (GAPILE)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 Barn Garrison (0B75521C)](sov02smd-teams.md#team-0b75521c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9157, Events line 9245, Actions line 9333.

<a id="trigger-0944643c"></a>

### 65. BG1 Early Air Assault - 0944643C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Early Air Asslt Go (094563DC)](#trigger-094563dc).

Attached scope: tag definitions 094567EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [BG1 Early Attk Air (0B831B7C)](sov02smd-teams.md#team-0b831b7c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9158, Events line 9246, Actions line 9334.

<a id="trigger-094566fc"></a>

### 66. BG1 Early Air Assault Off - 094566FC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Early Air Asslt Go (094563DC)](#trigger-094563dc).

Attached scope: tag definitions 094564CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 360 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [BG1 Early Air Assault (0944643C)](#trigger-0944643c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9159, Events line 9247, Actions line 9335.

<a id="trigger-094563dc"></a>

### 67. BG1 Early Air Asslt Go - 094563DC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09451ACC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Early Air Attks) is set.

Flag writers in this mission: set local flag 10 (Early Air Attks) at [BG1 Early Attks (094558EC)](#trigger-094558ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 Early Air Assault (0944643C)](#trigger-0944643c).
2. Enable and reset applicable timers for [BG1 Early Air Assault Off (094566FC)](#trigger-094566fc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9160, Events line 9248, Actions line 9336.

<a id="trigger-043b06cc"></a>

### 68. Germany1 Sell KIA_01 - 043B06CC

Owner reference: Germany1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043A9CAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Germany1 Sell KIA_02 (043A9BBC)](#trigger-043a9bbc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9161, Events line 9249, Actions line 9337.

<a id="trigger-043a9bbc"></a>

### 69. Germany1 Sell KIA_02 - 043A9BBC

Owner reference: Germany1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Germany1 Sell KIA_01 (043B06CC)](#trigger-043b06cc).

Attached scope: tag definitions 043A999C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 19 (country/type GERMANY1; placed owner German1 House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9162, Events line 9250, Actions line 9338.

<a id="trigger-043a98ac"></a>

### 70. Germany2 Sell KIA_02 - 043A98AC

Owner reference: Germany2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Germany2 Sell KIA_01 (0950D82C)](#trigger-0950d82c).

Attached scope: tag definitions 06B6647C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 20 (country/type GERMANY2; placed owner German2 House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9163, Events line 9251, Actions line 9339.

<a id="trigger-0950d82c"></a>

### 71. Germany2 Sell KIA_01 - 0950D82C

Owner reference: Germany2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0951720C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Germany2 Sell KIA_02 (043A98AC)](#trigger-043a98ac).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9164, Events line 9252, Actions line 9340.

<a id="trigger-0951711c"></a>

### 72. Germany3 Sell KIA_02 - 0951711C

Owner reference: Germany3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Germany3 Sell KIA_01 (09517C1C)](#trigger-09517c1c).

Attached scope: tag definitions 09517D0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Fire Sale: owner selector 21 (country/type GERMANY3; placed owner German3 House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9165, Events line 9253, Actions line 9341.

<a id="trigger-09517c1c"></a>

### 73. Germany3 Sell KIA_01 - 09517C1C

Owner reference: Germany3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0951757C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Germany3 Sell KIA_02 (0951711C)](#trigger-0951711c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9166, Events line 9254, Actions line 9342.

<a id="trigger-079e4b7c"></a>

### 74. Industrial_Plant_Brief - 079E4B7C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079E448C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 10 (global list position: Soviet Battle Lab (NATECH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Switch the sidebar to tab 0.
2. Flash cameo/type NAINDP; additional configured duration/location argument 120.
3. Play voice notification Unit_Sofia_IndustrialPlant.

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9167, Events line 9255, Actions line 9343.

<a id="trigger-07b14c3c"></a>

### 75. _Win (Check) - 07B14C3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [_Win (Cheer) (0439C2CC)](#trigger-0439c2cc).

Attached scope: tag definitions 0439B7FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 8 (Chronosphere KIA) is set.
2. local flag 7 (Einstein Lab KIA) is set.

Flag writers in this mission: set local flag 8 (Chronosphere KIA) at [_Win (BG2 Chronosphere KIA) (0439E1BC)](#trigger-0439e1bc); set local flag 8 (Chronosphere KIA) at [_Win (Einstein Chronosphere KIA) (08BC0C2C)](#trigger-08bc0c2c); set local flag 7 (Einstein Lab KIA) at [_Win (Einstein Lab KIA) (0439777C)](#trigger-0439777c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [_Lose (07D4D4AC)](#trigger-07d4d4ac).
2. Enable and reset applicable timers for [_Win (Cheer) (0439C2CC)](#trigger-0439c2cc).
3. Enable and reset applicable timers for [_Win (Mission Over) (0A3C3B8C)](#trigger-0a3c3b8c).
4. Disable [_Win (Check) (07B14C3C)](#trigger-07b14c3c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9168, Events line 9256, Actions line 9344.

<a id="trigger-078c61ec"></a>

### 76. G1_Barracks_Gone - 078C61EC

Owner reference: Germany1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Barracks (GAPILE), owner German1 House, cell (76, 56), tag 078C6E7C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 11 (G1_Barracks_Gone).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9169, Events line 9257, Actions line 9345.

<a id="trigger-078c6d8c"></a>

### 77. G2_Barracks_Gone - 078C6D8C

Owner reference: Germany2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Barracks (GAPILE), owner German2 House, cell (106, 41), tag 078C6B4C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 12 (G2_Barracks_Gone).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9170, Events line 9258, Actions line 9346.

<a id="trigger-078c6a5c"></a>

### 78. G3_Barracks_Gone - 078C6A5C

Owner reference: Germany3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Barracks (GAPILE), owner German3 House, cell (143, 73), tag 078C681C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 13 (G3_Barracks_Gone).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9171, Events line 9259, Actions line 9347.

<a id="trigger-04f5d48c"></a>

### 79. All_Hunt_Player - 04F5D48C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player_Deployed_MCV (04F58D5C)](#trigger-04f58d5c).

Attached scope: tag definitions 04F58E4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 15 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. All to Hunt: owner selector 16 (country/type BADGUY1; placed owner BadGuy1 House).
2. All to Hunt: owner selector 17 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9172, Events line 9260, Actions line 9348.

<a id="trigger-04f58d5c"></a>

### 80. Player_Deployed_MCV - 04F58D5C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 04F58B1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [All_Hunt_Player (04F5D48C)](#trigger-04f5d48c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9173, Events line 9261, Actions line 9349.

<a id="trigger-078370fc"></a>

### 81. Battlefortress_Found - 078370FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Mirage Tank (MGTK), owner BadGuy1 House, cell (114, 83), tag 07831C2C, persistence mode 0; Mirage Tank (MGTK), owner BadGuy1 House, cell (110, 82), tag 07831C2C, persistence mode 0; Battle Fortress (BFRT), owner BadGuy1 House, cell (111, 81), tag 07831C2C, persistence mode 0; Battle Fortress (BFRT), owner BadGuy1 House, cell (113, 81), tag 07831C2C, persistence mode 0; GI (E1), owner BadGuy1 House, cell (111, 79), tag 07831C2C, persistence mode 0; GI (E1), owner BadGuy1 House, cell (113, 79), tag 07831C2C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [1st Battle Fort Attk Go (0437882C)](#trigger-0437882c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9174, Events line 9262, Actions line 9350.

<a id="trigger-09025b6c"></a>

### 82. Troops1_Arrived - 09025B6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 090255EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 15 (Troops1_Arrived) is set.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Player Starters 1Troops (078BB93C)](sov02smd-teams.md#team-078bb93c).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9175, Events line 9263, Actions line 9351.

<a id="trigger-090254fc"></a>

### 83. Troops2_Arrived - 090254FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 090252BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 14 (Troops2_Arrived) is set.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Player Starters 2Troops (078BCEFC)](sov02smd-teams.md#team-078bcefc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9176, Events line 9264, Actions line 9352.

<a id="trigger-090251cc"></a>

### 84. Troops3_Arrived - 090251CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0902179C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 16 (Troops3_Arrived) is set.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Player Starters 3Troops (078BC7BC)](sov02smd-teams.md#team-078bc7bc).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9177, Events line 9265, Actions line 9353.

<a id="trigger-0790c9cc"></a>

### 85. _BG1_Hates_Player - 0790C9CC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0790C44C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 15 (country/type PLAYER; placed owner Player House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9178, Events line 9266, Actions line 9354.

<a id="trigger-0790c35c"></a>

### 86. _BG2_Hates_Player - 0790C35C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0790FF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 15 (country/type PLAYER; placed owner Player House).

Source locator: mapsmd03.mix/sov02smd.map; Triggers line 9179, Events line 9267, Actions line 9355.

[All team rosters and ordered plans](sov02smd-teams.md) | [All mission overrides](sov02smd-overrides.md)
