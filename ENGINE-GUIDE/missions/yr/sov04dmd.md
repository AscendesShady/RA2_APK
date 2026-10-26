# Operation: Romanov on the Run

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov04dmd.map. **Effective extracted member:** mapsmd03.mix/sov04dmd.map. **Trigger definitions:** 132.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov04dmd-teams.md) | [All mission overrides](sov04dmd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Russians |
| Theater | DESERT |
| Map size | 0,0,100,71 |
| Visible local rectangle | 12,5,86,60 |
| Placed vehicles | 22 |
| Placed infantry | 69 |
| Placed structures | 98 |
| Placed aircraft | 0 |
| Team templates | 90 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 0 | Americans |
| 1 | Alliance | 100 | YuriCountry2 |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 150 | Africans |
| 6 | Arabs | 1500 | Arabs |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 80 | Russians |
| 9 | YuriCountry | 1500 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 0 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 500 | Special |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Romaov In!,0 |
| 1 | Romanov Captured,0 |
| 2 | It Dead,0 |
| 3 | Romanov Changed Bri,0 |
| 4 | Romanov Changed Ger,0 |
| 5 | Low Power,0 |
| 6 | Romanov Found,0 |
| 7 | It House Destroyed,0 |
| 8 | Stop Respawn,0 |
| 9 | Romanov Killed,0 |
| 10 | PsychicSmash1,0 |
| 11 | PsychicSmash2,0 |
| 12 | PsychicSmash3,0 |
| 13 | Set1,0 |
| 14 | Set2,0 |
| 15 | Set3,0 |
| 16 | Set4,0 |
| 17 | Set5,0 |
| 18 | It's Safe,0 |
| 19 | Rom Change Brit Bac,0 |
| 20 | Rom In Yuri Base,0 |
| 21 | Gattling 1,0 |
| 22 | Gattling 2,0 |
| 23 | Gattling 3,0 |
| 24 | Gattling 4,0 |
| 25 | Gattling 5,0 |
| 26 | Gattling 6,0 |
| 27 | Light 2,0 |
| 28 | Light 1,0 |
| 29 | Landed,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Romanov Flies Away 2 (0CA0ABDC)](#trigger-0ca0abdc) | local flag 29 (Landed) is set. | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner. |
| [Congrats! (0CA09E0C)](#trigger-0ca09e0c) | 17 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner. |
| [It's Over : ( (0921D45C)](#trigger-0921d45c) | Destroyed,  All: owner selector 3 (country/type GERMANS; placed owner Germans).<br>Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians). | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser. |
| [Romanov Killed (043915FC)](#trigger-043915fc) | No instances of Premier Romanov (RMNV) exist on the map, under this event's ownership scope. | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser. |
| [Dumb Player (097304AC)](#trigger-097304ac) | Destroyed by anything. See attached-object/cell scope below. | Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser. |

## Every trigger, in file order

<a id="trigger-0921dedc"></a>

### 1. It's Over! - 0921DEDC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 40 tagged map cells: (100, 15), (101, 15), (102, 15), (103, 15), (104, 15), (105, 15), (106, 15), (100, 16), (101, 16), (105, 16), (106, 16), (100, 17), (101, 17), (105, 17), (106, 17), (100, 18), (101, 18), (105, 18), (106, 18), (100, 19), (101, 19), (102, 19), (103, 19), (104, 19), (105, 19), (106, 19), (100, 20), (101, 20), (102, 20), (103, 20), (104, 20), (105, 20), (106, 20), (100, 21), (101, 21), (102, 21), (103, 21), (104, 21), (105, 21), (106, 21); tag 0921D5AC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 3 (country/type GERMANS; placed owner Germans).

**Then perform these actions in order:**

1. Disable player input.
2. Play voice notification EVA_BattleControlOnline.
3. Enable and reset applicable timers for [Romanov Flies Away! (0CA00ABC)](#trigger-0ca00abc).
4. Remove instances of the team organization (not automatically its surviving objects) [_IT! (090B26FC)](sov04dmd-teams.md#team-090b26fc).
5. Disable [Obj 2 Speech (091FF36C)](#trigger-091ff36c).
6. Disable [Obj 2 Kill Base (0438410C)](#trigger-0438410c).
7. Create/recruit team [ITX (092C469C)](sov04dmd-teams.md#team-092c469c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7125, Events line 7259, Actions line 7393.

<a id="trigger-0ca00abc"></a>

### 2. Romanov Flies Away! - 0CA00ABC

Owner reference: Germans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [It's Over! (0921DEDC)](#trigger-0921dedc).

Attached scope: tag definitions 0CA006CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Romanov! (0B3BBA4C)](sov04dmd-teams.md#team-0b3bba4c).
2. Supply reinforcement team [Romanov Rescue! (089D5EFC)](sov04dmd-teams.md#team-089d5efc).
3. Move the camera to waypoint 3 (cell 103, 20) with speed setting 4.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7126, Events line 7260, Actions line 7394.

<a id="trigger-091ff36c"></a>

### 3. Obj 2 Speech - 091FF36C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Rescue Movie (0C9E79EC)](#trigger-0c9e79ec); enable from [Romanov Free (091357DC)](#trigger-091357dc).

Attached scope: tag definitions 043843CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 18 (It's Safe) is clear.

Flag writers in this mission: set local flag 18 (It's Safe) at [It's Safe! V1 (0682762C)](#trigger-0682762c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_ZofiaGetRomanovToAirport.
2. Disable [Obj 2 Speech (091FF36C)](#trigger-091ff36c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7127, Events line 7261, Actions line 7395.

<a id="trigger-0438410c"></a>

### 4. Obj 2 Kill Base - 0438410C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Rescue Movie (0C9E79EC)](#trigger-0c9e79ec); enable from [Romanov Free (091357DC)](#trigger-091357dc).

Attached scope: tag definitions 091EEBBC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 18 (It's Safe) is clear.

Flag writers in this mission: set local flag 18 (It's Safe) at [It's Safe! V1 (0682762C)](#trigger-0682762c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Display message “Objective: Destroy Yuri's base around the airport so Romanov can be safely evacuated” (MISSION:DestroyYuri04S).
2. Create radar-event marker type 1 at waypoint 32 (cell 103, 19).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7128, Events line 7262, Actions line 7396.

<a id="trigger-0ca0abdc"></a>

### 5. Romanov Flies Away 2 - 0CA0ABDC

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CA0BE4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 29 (Landed) is set.

**Then perform these actions in order:**

1. Play sound Cheer.
2. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7129, Events line 7263, Actions line 7397.

<a id="trigger-0ca09e0c"></a>

### 6. Congrats! - 0CA09E0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov In! (0438156C)](#trigger-0438156c).

Attached scope: tag definitions 0CA0F22C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 17 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound Cheer.
2. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the winner.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7130, Events line 7264, Actions line 7398.

<a id="trigger-0921d45c"></a>

### 7. It's Over : ( - 0921D45C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0921D22C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 3 (country/type GERMANS; placed owner Germans).
2. Destroyed,  All: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7131, Events line 7265, Actions line 7399.

<a id="trigger-0921e84c"></a>

### 8. Romanov Found! - 0921E84C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 36 tagged map cells: (136, 64), (137, 64), (138, 64), (139, 64), (140, 64), (136, 65), (137, 65), (138, 65), (139, 65), (140, 65), (141, 65), (136, 66), (137, 66), (141, 66), (142, 66), (136, 67), (137, 67), (141, 67), (142, 67), (136, 68), (137, 68), (141, 68), (142, 68), (136, 69), (137, 69), (138, 69), (139, 69), (140, 69), (141, 69), (142, 69), (137, 70), (138, 70), (139, 70), (140, 70), (141, 70), (142, 70); tag 0921E58C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 1 (cell 139, 69).
2. Enable and reset applicable timers for [Romanov Rescue Movie (0C9E79EC)](#trigger-0c9e79ec).
3. Disable [Bar Fired On (092D297C)](#trigger-092d297c).
4. Play voice notification Mis_xS4_ZofiaFoundRomanov.
5. Disable [Obj 1 Find Romanov! (091FF64C)](#trigger-091ff64c).
6. Disable [Obj 1 Speech (0438493C)](#trigger-0438493c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7132, Events line 7266, Actions line 7400.

<a id="trigger-0c9e79ec"></a>

### 9. Romanov Rescue Movie - 0C9E79EC

Owner reference: Germans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Found! (0921E84C)](#trigger-0921e84c); enable from [Bar Fired On (092D297C)](#trigger-092d297c).

Attached scope: tag definitions 0C9E25EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 4 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 1 (cell 139, 69).
2. Play in-game movie 47.
3. Enable and reset applicable timers for [Obj 2 Kill Base (0438410C)](#trigger-0438410c).
4. Enable and reset applicable timers for [Obj 2 Speech (091FF36C)](#trigger-091ff36c).
5. Remove instances of the team organization (not automatically its surviving objects) [_Rom Search 1 (08FF2B7C)](sov04dmd-teams.md#team-08ff2b7c).
6. Remove instances of the team organization (not automatically its surviving objects) [_Rom Search 2 (08FF221C)](sov04dmd-teams.md#team-08ff221c).
7. Remove instances of the team organization (not automatically its surviving objects) [_Rom Search 3 (08FF1B7C)](sov04dmd-teams.md#team-08ff1b7c).
8. Remove instances of the team organization (not automatically its surviving objects) [_Rom Search 4 (08FF113C)](sov04dmd-teams.md#team-08ff113c).
9. Remove instances of the team organization (not automatically its surviving objects) [_Rom Search 5 (08FF0A9C)](sov04dmd-teams.md#team-08ff0a9c).
10. Remove instances of the team organization (not automatically its surviving objects) [_Rom Search 6 (08FF050C)](sov04dmd-teams.md#team-08ff050c).
11. Create/recruit team [_ROM DESTROY 2 (08FFF96C)](sov04dmd-teams.md#team-08fff96c).
12. Create/recruit team [_ROM DESTROY 3 (08FFF3DC)](sov04dmd-teams.md#team-08fff3dc).
13. Create/recruit team [_ROM DESTROY 4 (08FFEC8C)](sov04dmd-teams.md#team-08ffec8c).
14. Create/recruit team [_ROM DESTROY 5 (08FFE6FC)](sov04dmd-teams.md#team-08ffe6fc).
15. Create/recruit team [_ROM DESTROY 6 (08FFE16C)](sov04dmd-teams.md#team-08ffe16c).
16. Enable and reset applicable timers for [Romanov Rescue Movie 2 (0524289C)](#trigger-0524289c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7133, Events line 7267, Actions line 7401.

<a id="trigger-092d297c"></a>

### 10. Bar Fired On - 092D297C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Rick's Place (CAMORR06), owner Neutral, cell (138, 66), tag 09311EDC, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Romanov Found! (0921E84C)](#trigger-0921e84c).
2. Reveal terrain around waypoint 1 (cell 139, 69).
3. Enable and reset applicable timers for [Romanov Rescue Movie (0C9E79EC)](#trigger-0c9e79ec).
4. Play voice notification Mis_xS4_ZofiaFoundRomanov.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7134, Events line 7268, Actions line 7402.

<a id="trigger-091ff64c"></a>

### 11. Obj 1 Find Romanov! - 091FF64C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hey! Intro UNLOCK (0CCC3B6C)](#trigger-0ccc3b6c).

Attached scope: tag definitions 091FF56C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Locate Premier Romanov before Yuri's troops do” (MISSION:FindRomanov).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7135, Events line 7269, Actions line 7403.

<a id="trigger-0438493c"></a>

### 12. Obj 1 Speech - 0438493C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hey! Intro UNLOCK (0CCC3B6C)](#trigger-0ccc3b6c).

Attached scope: tag definitions 0438428C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_ZofiaRomanovInEast.
2. Disable [Obj 1 Speech (0438493C)](#trigger-0438493c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7136, Events line 7270, Actions line 7404.

<a id="trigger-0524289c"></a>

### 13. Romanov Rescue Movie 2 - 0524289C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Rescue Movie (0C9E79EC)](#trigger-0c9e79ec).

Attached scope: tag definitions 052421EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 49 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Romanov! (0B3BBA4C)](sov04dmd-teams.md#team-0b3bba4c) at waypoint 1 (cell 139, 69).
2. Create radar-event marker type 1 at waypoint 32 (cell 103, 19).
3. Play voice notification Mis_xS4_RomanovAirportHint.
4. Supply reinforcement team [_It #1 (084EE51C)](sov04dmd-teams.md#team-084ee51c).
5. Set local flag 6 (Romanov Found).
6. Enable and reset applicable timers for [Romanov Killed (043915FC)](#trigger-043915fc).
7. Enable and reset applicable timers for [_Rom's Iron Curtain (068A958C)](#trigger-068a958c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7137, Events line 7271, Actions line 7405.

<a id="trigger-043915fc"></a>

### 14. Romanov Killed - 043915FC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Rescue Movie 2 (0524289C)](#trigger-0524289c).

Attached scope: tag definitions 04390F1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Premier Romanov (RMNV) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Disable [Romanov Captured (0915E18C)](#trigger-0915e18c).
2. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7138, Events line 7272, Actions line 7406.

<a id="trigger-068a958c"></a>

### 15. _Rom's Iron Curtain - 068A958C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Rescue Movie 2 (0524289C)](#trigger-0524289c); enable from [Iron Curtain (09327F3C)](#trigger-09327f3c).

Attached scope: tag definitions 067F811C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set Tech Level (Techno)[Level]; main setting NAIRON; location/duration field 1.
2. Play voice notification Mis_xS4_RomanovIronCurtain.
3. Enable and reset applicable timers for [Flash! (0DC26F3C)](#trigger-0dc26f3c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7139, Events line 7273, Actions line 7407.

<a id="trigger-0915e18c"></a>

### 16. Romanov Captured - 0915E18C

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0921EE7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 1 (Romanov Captured).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7140, Events line 7274, Actions line 7408.

<a id="trigger-0dc26f3c"></a>

### 17. Flash! - 0DC26F3C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Rom's Iron Curtain (068A958C)](#trigger-068a958c).

Attached scope: tag definitions 0DC2663C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash cameo/type NAIRON; additional configured duration/location argument 45.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7141, Events line 7275, Actions line 7409.

<a id="trigger-0b3dea1c"></a>

### 18. Create It! - 0B3DEA1C

Owner reference: Special. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Timed IT Respawn (0B43633C)](#trigger-0b43633c).

Attached scope: tag definitions 0B3DE3FC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (It House Destroyed) is clear.

Flag writers in this mission: set local flag 7 (It House Destroyed) at [End IT! Respawn (0437F64C)](#trigger-0437f64c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_IT! (090B26FC)](sov04dmd-teams.md#team-090b26fc).
2. Disable [Create It! (0B3DEA1C)](#trigger-0b3dea1c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7142, Events line 7276, Actions line 7410.

<a id="trigger-0438156c"></a>

### 19. Romanov In! - 0438156C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0438167C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Romaov In!) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Congrats! (0CA09E0C)](#trigger-0ca09e0c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7143, Events line 7277, Actions line 7411.

<a id="trigger-0b3f507c"></a>

### 20. Get It On! - 0B3F507C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hey! Intro UNLOCK (0CCC3B6C)](#trigger-0ccc3b6c).

Attached scope: tag definitions 0B40404C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_Cap Base Defense 1 (0B3CEDEC)](sov04dmd-teams.md#team-0b3cedec).
2. Create/recruit team [_Cap Base Defense 2 (0B3CFDEC)](sov04dmd-teams.md#team-0b3cfdec).
3. Production Begins: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
4. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).
5. Production Begins: owner selector 6 (country/type ARABS; placed owner Arabs).
6. Create/recruit team [Y Base Defense 1 (0B602A4C)](sov04dmd-teams.md#team-0b602a4c).
7. Create/recruit team [Y Base Defense 2 (0B60259C)](sov04dmd-teams.md#team-0b60259c).
8. AI triggers begin: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
9. Create/recruit team [_Moving Guards (0CD0F93C)](sov04dmd-teams.md#team-0cd0f93c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7144, Events line 7278, Actions line 7412.

<a id="trigger-0925e44c"></a>

### 21. _REGEN IT! - 0925E44C

Owner reference: Special. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Timed IT Respawn (0B43633C)](#trigger-0b43633c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7145, Events line 7279, Actions line 7413.

<a id="trigger-0b43633c"></a>

### 22. Timed IT Respawn - 0B43633C

Owner reference: Special. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_REGEN IT! (0925E44C)](#trigger-0925e44c).

Attached scope: tag definitions 0B437A9C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Create It! (0B3DEA1C)](#trigger-0b3dea1c).
2. Disable [Timed IT Respawn (0B43633C)](#trigger-0b43633c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7146, Events line 7280, Actions line 7414.

<a id="trigger-0925d82c"></a>

### 23. REGEN _ROM SEARCH 1 - 0925D82C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0925D5FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_Rom Search 1 (08FF2B7C)](sov04dmd-teams.md#team-08ff2b7c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7147, Events line 7281, Actions line 7415.

<a id="trigger-0925d50c"></a>

### 24. REGEN _ROM SEARCH 2 - 0925D50C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0925D2DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_Rom Search 2 (08FF221C)](sov04dmd-teams.md#team-08ff221c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7148, Events line 7282, Actions line 7416.

<a id="trigger-0925d1ec"></a>

### 25. REGEN _ROM SEARCH 3 - 0925D1EC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0925C8CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_Rom Search 3 (08FF1B7C)](sov04dmd-teams.md#team-08ff1b7c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7149, Events line 7283, Actions line 7417.

<a id="trigger-0925c7dc"></a>

### 26. REGEN _ROM SEARCH 4 - 0925C7DC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0925C55C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_Rom Search 4 (08FF113C)](sov04dmd-teams.md#team-08ff113c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7150, Events line 7284, Actions line 7418.

<a id="trigger-0925c46c"></a>

### 27. REGEN _ROM SEARCH 5 - 0925C46C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0925542C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_Rom Search 5 (08FF0A9C)](sov04dmd-teams.md#team-08ff0a9c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7151, Events line 7285, Actions line 7419.

<a id="trigger-0925533c"></a>

### 28. REGEN _ROM SEARCH 6 - 0925533C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0930506C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_Rom Search 6 (08FF050C)](sov04dmd-teams.md#team-08ff050c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7152, Events line 7286, Actions line 7420.

<a id="trigger-092fa5fc"></a>

### 29. REGEN _ROM DESTROY 2 - 092FA5FC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 092FFEAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Regen _Rom ok (0B3CC8DC)](#trigger-0b3cc8dc).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7153, Events line 7287, Actions line 7421.

<a id="trigger-0b3cc8dc"></a>

### 30. Regen _Rom ok - 0B3CC8DC

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [REGEN _ROM DESTROY 2 (092FA5FC)](#trigger-092fa5fc).

Attached scope: tag definitions 0B3C846C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 8 (Stop Respawn) is clear.

Flag writers in this mission: set local flag 8 (Stop Respawn) at [Disable Destroy Respawn (093DAB5C)](#trigger-093dab5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_ROM DESTROY 2 (08FFF96C)](sov04dmd-teams.md#team-08fff96c) at waypoint 29 (cell 93, 30).
2. Disable [Regen _Rom ok (0B3CC8DC)](#trigger-0b3cc8dc).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7154, Events line 7288, Actions line 7422.

<a id="trigger-092ffdbc"></a>

### 31. REGEN _ROM DESTROY 3 - 092FFDBC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 092FFB8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_ROM DESTROY 3 (08FFF3DC)](sov04dmd-teams.md#team-08fff3dc).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7155, Events line 7289, Actions line 7423.

<a id="trigger-092ffa9c"></a>

### 32. REGEN _ROM DESTROY 4 - 092FFA9C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 092FF86C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [_ROM DESTROY 4 (08FFEC8C)](sov04dmd-teams.md#team-08ffec8c) at waypoint 29 (cell 93, 30).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7156, Events line 7290, Actions line 7424.

<a id="trigger-092ff77c"></a>

### 33. REGEN _ROM DESTROY 5 - 092FF77C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 092FA49C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [_ROM DESTROY 5 (08FFE6FC)](sov04dmd-teams.md#team-08ffe6fc).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7157, Events line 7291, Actions line 7425.

<a id="trigger-092fa3ac"></a>

### 34. REGEN _ROM DESTROY 6 - 092FA3AC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 092FCB3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [_ROM DESTROY 6 (08FFE16C)](sov04dmd-teams.md#team-08ffe16c) at waypoint 29 (cell 93, 30).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7158, Events line 7292, Actions line 7426.

<a id="trigger-09135c9c"></a>

### 35. Romanov Slave - 09135C9C

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Free (091357DC)](#trigger-091357dc).

Attached scope: tag definitions 091358CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Romanov Captured) is set.

Flag writers in this mission: set local flag 1 (Romanov Captured) at [Romanov Captured (0915E18C)](#trigger-0915e18c); clear local flag 1 (Romanov Captured) at [Free Romanov (06859E1C)](#trigger-06859e1c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Romanov! (0B3BBA4C)](sov04dmd-teams.md#team-0b3bba4c).
2. Create/recruit team [_Captured Romanov (05B84B7C)](sov04dmd-teams.md#team-05b84b7c).
3. Disable [Romanov Slave (09135C9C)](#trigger-09135c9c).
4. Enable and reset applicable timers for [Romanov Free (091357DC)](#trigger-091357dc).
5. Disable [Obj 2 Speech (091FF36C)](#trigger-091ff36c).
6. Disable [Obj 2 Kill Base (0438410C)](#trigger-0438410c).
7. Enable and reset applicable timers for [Obj 3 Rescue Romanov (043844EC)](#trigger-043844ec).
8. Enable and reset applicable timers for [Obj 3 Speech (04382BEC)](#trigger-04382bec).
9. Play voice notification Mis_xS4_RomanovIAmCaptured.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7159, Events line 7293, Actions line 7427.

<a id="trigger-091357dc"></a>

### 36. Romanov Free - 091357DC

Owner reference: British. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Slave (09135C9C)](#trigger-09135c9c).

Attached scope: tag definitions 0913528C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Romanov Captured) is clear.

Flag writers in this mission: set local flag 1 (Romanov Captured) at [Romanov Captured (0915E18C)](#trigger-0915e18c); clear local flag 1 (Romanov Captured) at [Free Romanov (06859E1C)](#trigger-06859e1c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [_Captured Romanov 2 (05B8421C)](sov04dmd-teams.md#team-05b8421c).
2. Create/recruit team [_Freed Romanov 2 (05B87C8C)](sov04dmd-teams.md#team-05b87c8c).
3. Disable [Romanov Free (091357DC)](#trigger-091357dc).
4. Enable and reset applicable timers for [Romanov Slave (09135C9C)](#trigger-09135c9c).
5. Disable [Obj 3 Rescue Romanov (043844EC)](#trigger-043844ec).
6. Disable [Obj 3 Speech (04382BEC)](#trigger-04382bec).
7. Enable and reset applicable timers for [Obj 2 Speech (091FF36C)](#trigger-091ff36c).
8. Enable and reset applicable timers for [Obj 2 Kill Base (0438410C)](#trigger-0438410c).
9. Play voice notification Mis_xS4_RomanovCured.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7160, Events line 7294, Actions line 7428.

<a id="trigger-043844ec"></a>

### 37. Obj 3 Rescue Romanov - 043844EC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Slave (09135C9C)](#trigger-09135c9c).

Attached scope: tag definitions 04382CDC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Rescue Romanov from Yuri's control” (MISSION:RecoverRomanov).
2. Create radar-event marker type 1 at waypoint 27 (cell 118, 33).
3. Reveal terrain around waypoint 27 (cell 118, 33).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7161, Events line 7295, Actions line 7429.

<a id="trigger-04382bec"></a>

### 38. Obj 3 Speech - 04382BEC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Slave (09135C9C)](#trigger-09135c9c).

Attached scope: tag definitions 0438262C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_RomanovHelpMe.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7162, Events line 7296, Actions line 7430.

<a id="trigger-093435ec"></a>

### 39. Romanov Slave 2 - 093435EC

Owner reference: British. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 093432EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Romanov Changed Bri) is set.

Flag writers in this mission: clear local flag 3 (Romanov Changed Bri) at [Romanov Slave 2 (093435EC)](#trigger-093435ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [_Captured Romanov (05B84B7C)](sov04dmd-teams.md#team-05b84b7c).
2. Create/recruit team [_Captured Romanov 2 (05B8421C)](sov04dmd-teams.md#team-05b8421c).
3. Clear local flag 3 (Romanov Changed Bri).
4. Enable and reset applicable timers for [Zofia Rom Captured (0438F09C)](#trigger-0438f09c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7163, Events line 7297, Actions line 7431.

<a id="trigger-0438f09c"></a>

### 40. Zofia Rom Captured - 0438F09C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Romanov Slave 2 (093435EC)](#trigger-093435ec).

Attached scope: tag definitions 0438EB8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_ZofiaRomanovCaptured.
2. Disable [Zofia Rom Captured (0438F09C)](#trigger-0438f09c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7164, Events line 7298, Actions line 7432.

<a id="trigger-0cea333c"></a>

### 41. Power Low - 0CEA333C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Power Up (0CEA4E5C)](#trigger-0cea4e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Low Power: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Change House: owner selector 12 (country/type NEUTRAL; placed owner Neutral).
2. Disable [Power Low (0CEA333C)](#trigger-0cea333c).
3. Enable and reset applicable timers for [Power Up (0CEA4E5C)](#trigger-0cea4e5c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7165, Events line 7299, Actions line 7433.

<a id="trigger-0cea4e5c"></a>

### 42. Power Up - 0CEA4E5C

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Power Low (0CEA333C)](#trigger-0cea333c).

Incoming activation links: enable from [Power Low (0CEA333C)](#trigger-0cea333c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Power Full: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Change House: owner selector 5 (country/type AFRICANS; placed owner Africans).
2. Disable [Power Up (0CEA4E5C)](#trigger-0cea4e5c).
3. Enable and reset applicable timers for [Power Low (0CEA333C)](#trigger-0cea333c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7166, Events line 7300, Actions line 7434.

<a id="trigger-043b96bc"></a>

### 43. Arab Enemy - 043B96BC

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043B914C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 3 (country/type GERMANS; placed owner Germans).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7167, Events line 7301, Actions line 7435.

<a id="trigger-0b4d344c"></a>

### 44. Hate Germany! - 0B4D344C

Owner reference: Special. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B4D49AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 3 (country/type GERMANS; placed owner Germans).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7168, Events line 7302, Actions line 7436.

<a id="trigger-0437f64c"></a>

### 45. End IT! Respawn - 0437F64C

Owner reference: Special. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Barracks (YABRCK), owner Alliance, cell (35, 92), tag 04384B3C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 7 (It House Destroyed).
2. Set local flag 27 (Light 2).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7169, Events line 7303, Actions line 7437.

<a id="trigger-093dab5c"></a>

### 46. Disable Destroy Respawn - 093DAB5C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Barracks (YABRCK), owner YuriCountry, cell (92, 27), tag 093D8ADC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 8 (Stop Respawn).
2. Disable [REGEN _ROM DESTROY 4 (092FFA9C)](#trigger-092ffa9c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7170, Events line 7304, Actions line 7438.

<a id="trigger-0682762c"></a>

### 47. It's Safe! V1 - 0682762C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0682473C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building does not exist: type index 301 (global list position: Yuri Construction Yard (YACNST)). A map-local type-list change can affect index interpretation.
2. Building does not exist: type index 300 (global list position: Bus Stop (CASTRT05)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_ZofiaSafeToEvac.
2. Disable [Obj 2 Kill Base (0438410C)](#trigger-0438410c).
3. Disable [Obj 2 Speech (091FF36C)](#trigger-091ff36c).
4. Enable and reset applicable timers for [Obj 4 To the Airport (09965F3C)](#trigger-09965f3c).
5. Set local flag 18 (It's Safe).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7171, Events line 7305, Actions line 7439.

<a id="trigger-09965f3c"></a>

### 48. Obj 4 To the Airport - 09965F3C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [It's Safe! V1 (0682762C)](#trigger-0682762c).

Attached scope: tag definitions 099659BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective: Take Romanov to the airport where he can be transported away safely” (MISSION:TakeRomanov).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7172, Events line 7306, Actions line 7440.

<a id="trigger-0bcdc0fc"></a>

### 49. Turn Off Power - 0BCDC0FC

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BD0744C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Disable [Power Up (0CEA4E5C)](#trigger-0cea4e5c).
2. Set local flag 5 (Low Power).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7173, Events line 7307, Actions line 7441.

<a id="trigger-0924a18c"></a>

### 50. Power Down For Good - 0924A18C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Power Up (0CEA4E5C)](#trigger-0cea4e5c).

Attached scope: Nuclear Reactor (NANRCT), owner Africans, cell (4, 100), tag 0CEA4F4C, persistence mode 2.

**Wait for the recorded events:**

1. local flag 5 (Low Power) is set.

Flag writers in this mission: set local flag 5 (Low Power) at [Turn Off Power (0BCDC0FC)](#trigger-0bcdc0fc); set local flag 5 (Low Power) at [Power Off For Good (089F57BC)](#trigger-089f57bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 12 (country/type NEUTRAL; placed owner Neutral).
2. Disable [Power Down For Good (0924A18C)](#trigger-0924a18c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7174, Events line 7308, Actions line 7442.

<a id="trigger-09327f3c"></a>

### 51. Iron Curtain - 09327F3C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 093278CC (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.
2. Building exists: type index 10 (global list position: Soviet Battle Lab (NATECH)). A map-local type-list change can affect index interpretation.
3. local flag 1 (Romanov Captured) is clear.

Flag writers in this mission: set local flag 1 (Romanov Captured) at [Romanov Captured (0915E18C)](#trigger-0915e18c); clear local flag 1 (Romanov Captured) at [Free Romanov (06859E1C)](#trigger-06859e1c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Rom's Iron Curtain (068A958C)](#trigger-068a958c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7175, Events line 7309, Actions line 7443.

<a id="trigger-06859e1c"></a>

### 52. Free Romanov - 06859E1C

Owner reference: Special. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [_REGEN IT! (0925E44C)](#trigger-0925e44c).

Attached scope: tag definitions 0925DD2C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Clear local flag 1 (Romanov Captured).
2. Disable [Zofia Rom Captured (0438F09C)](#trigger-0438f09c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7176, Events line 7310, Actions line 7444.

<a id="trigger-092de21c"></a>

### 53. Psychic Smash 1 - 092DE21C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner Africans, cell (94, 33), tag 092DC1FC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 10 (PsychicSmash1).
2. Disable [Introduce Psychic Towers (077FF3EC)](#trigger-077ff3ec).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7177, Events line 7311, Actions line 7445.

<a id="trigger-077ff3ec"></a>

### 54. Introduce Psychic Towers - 077FF3EC

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 9 tagged map cells: (94, 45), (95, 45), (96, 45), (97, 45), (98, 45), (94, 46), (98, 46), (94, 47), (98, 47); tag 094A406C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 110 (cell 96, 34).
2. Play voice notification Unit_Sofia_PsychTower.
3. Flash buildings of type YAPSYT; duration argument 90.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7178, Events line 7312, Actions line 7446.

<a id="trigger-0c06ff3c"></a>

### 55. Psychic Smash 2 - 0C06FF3C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner Africans, cell (98, 33), tag 0C06E2CC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 11 (PsychicSmash2).
2. Disable [Introduce Psychic Towers (077FF3EC)](#trigger-077ff3ec).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7179, Events line 7313, Actions line 7447.

<a id="trigger-0cc7567c"></a>

### 56. Psychic Smash 3 - 0CC7567C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner Africans, cell (112, 29), tag 0CC77D1C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 12 (PsychicSmash3).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7180, Events line 7314, Actions line 7448.

<a id="trigger-0cc73c4c"></a>

### 57. Psychic Smash 1b - 0CC73C4C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner YuriCountry, cell (10, 107), tag 0CC7230C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 10 (PsychicSmash1) is set.

Flag writers in this mission: set local flag 10 (PsychicSmash1) at [Psychic Smash 1 (092DE21C)](#trigger-092de21c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7181, Events line 7315, Actions line 7449.

<a id="trigger-0cc7131c"></a>

### 58. Psychic Smash 2b - 0CC7131C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner YuriCountry, cell (14, 111), tag 0CC7116C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 11 (PsychicSmash2) is set.

Flag writers in this mission: set local flag 11 (PsychicSmash2) at [Psychic Smash 2 (0C06FF3C)](#trigger-0c06ff3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7182, Events line 7316, Actions line 7450.

<a id="trigger-0cc706ec"></a>

### 59. Psychic Smash 3b - 0CC706EC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psychic Tower (YAPSYT), owner YuriCountry, cell (18, 115), tag 0CC7C43C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 12 (PsychicSmash3) is set.

Flag writers in this mission: set local flag 12 (PsychicSmash3) at [Psychic Smash 3 (0CC7567C)](#trigger-0cc7567c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7183, Events line 7317, Actions line 7451.

<a id="trigger-0bbb692c"></a>

### 60. Break Moving Guards - 0BBB692C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Yuri Barracks (YABRCK), owner YuriCountry, cell (96, 63), tag 0BBB63AC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [_Moving Guards (0CD0F93C)](sov04dmd-teams.md#team-0cd0f93c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7184, Events line 7318, Actions line 7452.

<a id="trigger-0b587c2c"></a>

### 61. Evil-Go-Round 1 - 0B587C2C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil-Go-Round 5 (0B583A5C)](#trigger-0b583a5c).

Attached scope: tag definitions 0B58755C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 300 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Yuri Attack! (08DFE0EC)](sov04dmd-teams.md#team-08dfe0ec).
2. Enable and reset applicable timers for [Evil-Go-Round 2 (0B58746C)](#trigger-0b58746c).
3. Disable [Evil-Go-Round 1 (0B587C2C)](#trigger-0b587c2c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7185, Events line 7319, Actions line 7453.

<a id="trigger-0b58746c"></a>

### 62. Evil-Go-Round 2 - 0B58746C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil-Go-Round 1 (0B587C2C)](#trigger-0b587c2c).

Attached scope: tag definitions 0B58722C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 200 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Y Brute Force (0C5096CC)](sov04dmd-teams.md#team-0c5096cc).
2. Enable and reset applicable timers for [Evil-Go-Round 3 (0B58713C)](#trigger-0b58713c).
3. Disable [Evil-Go-Round 2 (0B58746C)](#trigger-0b58746c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7186, Events line 7320, Actions line 7454.

<a id="trigger-0b58713c"></a>

### 63. Evil-Go-Round 3 - 0B58713C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil-Go-Round 2 (0B58746C)](#trigger-0b58746c).

Attached scope: tag definitions 0B583E7C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 400 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Lots O Initiates (0C5146CC)](sov04dmd-teams.md#team-0c5146cc).
2. Enable and reset applicable timers for [Evil-Go-Round 4 (0B583D8C)](#trigger-0b583d8c).
3. Disable [Evil-Go-Round 3 (0B58713C)](#trigger-0b58713c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7187, Events line 7321, Actions line 7455.

<a id="trigger-0b583d8c"></a>

### 64. Evil-Go-Round 4 - 0B583D8C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil-Go-Round 3 (0B58713C)](#trigger-0b58713c).

Attached scope: tag definitions 0B583B4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 350 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Harvester Attack (0C71293C)](sov04dmd-teams.md#team-0c71293c).
2. Enable and reset applicable timers for [Evil-Go-Round 5 (0B583A5C)](#trigger-0b583a5c).
3. Disable [Evil-Go-Round 4 (0B583D8C)](#trigger-0b583d8c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7188, Events line 7322, Actions line 7456.

<a id="trigger-0b583a5c"></a>

### 65. Evil-Go-Round 5 - 0B583A5C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Evil-Go-Round 4 (0B583D8C)](#trigger-0b583d8c).

Attached scope: tag definitions 0B58353C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 350 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Create/recruit team [Lots O Initiates (0C5146CC)](sov04dmd-teams.md#team-0c5146cc).
2. Enable and reset applicable timers for [Evil-Go-Round 1 (0B587C2C)](#trigger-0b587c2c).
3. Disable [Evil-Go-Round 5 (0B583A5C)](#trigger-0b583a5c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7189, Events line 7323, Actions line 7457.

<a id="trigger-0931cafc"></a>

### 66. Hey! Intro here! - 0931CAFC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0931C36C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_Conscript1Move (0690DEFC)](sov04dmd-teams.md#team-0690defc).
2. Create/recruit team [_Conscript2Move (0690F22C)](sov04dmd-teams.md#team-0690f22c).
3. Create/recruit team [_Conscript3Move (0690BC0C)](sov04dmd-teams.md#team-0690bc0c).
4. Create/recruit team [_Conscript4Move (0690B71C)](sov04dmd-teams.md#team-0690b71c).
5. Create/recruit team [_Conscript5Move (092EC2EC)](sov04dmd-teams.md#team-092ec2ec).
6. Create/recruit team [_Conscript6Move (092EA90C)](sov04dmd-teams.md#team-092ea90c).
7. Create/recruit team [_Conscript7Move (092EA6CC)](sov04dmd-teams.md#team-092ea6cc).
8. Create/recruit team [_Conscript8Move (092E990C)](sov04dmd-teams.md#team-092e990c).
9. Supply reinforcement team [_Rhino1Move (08F4893C)](sov04dmd-teams.md#team-08f4893c).
10. Supply reinforcement team [_Rhino2Move (08F4848C)](sov04dmd-teams.md#team-08f4848c).
11. Create/recruit team [_Rhino3Move (08F4DDEC)](sov04dmd-teams.md#team-08f4ddec).
12. Supply reinforcement team [_Rhino4Move (08F4D93C)](sov04dmd-teams.md#team-08f4d93c).
13. Supply reinforcement team [_MCVMove (0D2AC93C)](sov04dmd-teams.md#team-0d2ac93c).
14. Disable player input.
15. Play voice notification EVA_EstablishBattlefieldControl.
16. Enable and reset applicable timers for [Hey! Intro here! 1b (0972D7DC)](#trigger-0972d7dc).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7190, Events line 7324, Actions line 7458.

<a id="trigger-0972d7dc"></a>

### 67. Hey! Intro here! 1b - 0972D7DC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hey! Intro here! (0931CAFC)](#trigger-0931cafc).

Attached scope: tag definitions 0973010C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 45.
2. Enable and reset applicable timers for [Hey! Intro UNLOCK (0CCC3B6C)](#trigger-0ccc3b6c).
3. Enable and reset applicable timers for [UnnecessaryExtraTrigger (0C6D3A7C)](#trigger-0c6d3a7c).
4. Enable and reset applicable timers for [MV Yuri Calling Rom (09258CFC)](#trigger-09258cfc).
5. Supply reinforcement team [_S04_ Power Troops (0910AB7C)](sov04dmd-teams.md#team-0910ab7c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7191, Events line 7325, Actions line 7459.

<a id="trigger-0ccc3b6c"></a>

### 68. Hey! Intro UNLOCK - 0CCC3B6C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hey! Intro here! 1b (0972D7DC)](#trigger-0972d7dc).

Attached scope: tag definitions 0CCC32FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 137 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Enable and reset applicable timers for [Get It On! (0B3F507C)](#trigger-0b3f507c).
3. Play voice notification EVA_BattlefieldControlOnline.
4. Enable and reset applicable timers for [Obj 1 Find Romanov! (091FF64C)](#trigger-091ff64c).
5. Enable and reset applicable timers for [Obj 1 Speech (0438493C)](#trigger-0438493c).
6. Enable and reset applicable timers for [Ping Rom Easy 1 (0B14C8AC)](#trigger-0b14c8ac).
7. Enable and reset applicable timers for [Ping Rom Easy 2 (0B14C23C)](#trigger-0b14c23c).
8. Create/recruit team [_S04_Brute Demo (093B0EFC)](sov04dmd-teams.md#team-093b0efc).
9. Create/recruit team [_S04_Brute Patrol 1 (08F16D7C)](sov04dmd-teams.md#team-08f16d7c).
10. Create/recruit team [_S04_Brute Patrol 2 (08F1632C)](sov04dmd-teams.md#team-08f1632c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7192, Events line 7326, Actions line 7460.

<a id="trigger-0c6d3a7c"></a>

### 69. UnnecessaryExtraTrigger - 0C6D3A7C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hey! Intro here! 1b (0972D7DC)](#trigger-0972d7dc).

Attached scope: tag definitions 0C6D327C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification S04_p01.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7193, Events line 7327, Actions line 7461.

<a id="trigger-09258cfc"></a>

### 70. MV Yuri Calling Rom - 09258CFC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hey! Intro here! 1b (0972D7DC)](#trigger-0972d7dc).

Attached scope: tag definitions 092585FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 46.
2. Enable and reset applicable timers for [SP Yuri - Can't Hide (0D1B563C)](#trigger-0d1b563c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7194, Events line 7328, Actions line 7462.

<a id="trigger-0b14c8ac"></a>

### 71. Ping Rom Easy 1 - 0B14C8AC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hey! Intro UNLOCK (0CCC3B6C)](#trigger-0ccc3b6c).

Attached scope: tag definitions 0B14C32C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Romanov Found) is clear.
2. 300 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 6 (Romanov Found) at [Romanov Rescue Movie 2 (0524289C)](#trigger-0524289c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 1 (cell 139, 69).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7195, Events line 7329, Actions line 7463.

<a id="trigger-0b14c23c"></a>

### 72. Ping Rom Easy 2 - 0B14C23C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Hey! Intro UNLOCK (0CCC3B6C)](#trigger-0ccc3b6c).

Attached scope: tag definitions 0B14FCDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Romanov Found) is clear.
2. 900 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 6 (Romanov Found) at [Romanov Rescue Movie 2 (0524289C)](#trigger-0524289c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 1 (cell 139, 69).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7196, Events line 7330, Actions line 7464.

<a id="trigger-0d1b563c"></a>

### 73. SP Yuri - Can't Hide - 0D1B563C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [MV Yuri Calling Rom (09258CFC)](#trigger-09258cfc).

Attached scope: tag definitions 0D1B53FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Romanov Found) is clear.
2. 240 configured time units have elapsed since the trigger timer was initialized/reset.

Flag writers in this mission: set local flag 6 (Romanov Found) at [Romanov Rescue Movie 2 (0524289C)](#trigger-0524289c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_YuriOnlyHideSoLong.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7197, Events line 7331, Actions line 7465.

<a id="trigger-093f822c"></a>

### 74. _Introduce the Demo Truck - 093F822C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C0B1F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 14 (global list position: Soviet War Factory (NAWEAP)). A map-local type-list change can affect index interpretation.
2. Building exists: type index 13 (global list position: Radar Tower (NARADR)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Disable [_Introduce the Demo Truck (093F822C)](#trigger-093f822c).
2. Enable and reset applicable timers for [_Introduce Again! (0BCFCA8C)](#trigger-0bcfca8c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7198, Events line 7332, Actions line 7466.

<a id="trigger-0bcfca8c"></a>

### 75. _Introduce Again! - 0BCFCA8C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Introduce the Demo Truck (093F822C)](#trigger-093f822c).

Attached scope: tag definitions 0BCFC5CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Switch the sidebar to tab 3.
2. Enable and reset applicable timers for [_Introduce DT 2 (0C0B0F3C)](#trigger-0c0b0f3c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7199, Events line 7333, Actions line 7467.

<a id="trigger-0c0b0f3c"></a>

### 76. _Introduce DT 2 - 0C0B0F3C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Introduce Again! (0BCFCA8C)](#trigger-0bcfca8c).

Attached scope: tag definitions 0C0B003C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Flash cameo/type DTRUCK; additional configured duration/location argument 90.
2. Play voice notification Unit_Sofia_DemoTruck.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7200, Events line 7334, Actions line 7468.

<a id="trigger-0923ebac"></a>

### 77. Set1 - 0923EBAC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Set local flag 13 (Set1).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7201, Events line 7335, Actions line 7469.

<a id="trigger-0923e24c"></a>

### 78. Set1Undo - 0923E24C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Set1 (0923EBAC)](#trigger-0923ebac).

Attached scope: Tech Oil Derrick (CAOILD), owner Neutral, cell (51, 67), tag 0923E4BC, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 13 (Set1).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7202, Events line 7336, Actions line 7470.

<a id="trigger-0923fbbc"></a>

### 79. Set4 - 0923FBBC

Owner reference: YuriCountry2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner Alliance, cell (45, 82), tag 0923FADC, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 16 (Set4).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7203, Events line 7337, Actions line 7471.

<a id="trigger-0923724c"></a>

### 80. Set2 - 0923724C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Set local flag 14 (Set2).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7204, Events line 7338, Actions line 7472.

<a id="trigger-0b210dec"></a>

### 81. Set2Undo - 0B210DEC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Set2 (0923724C)](#trigger-0923724c).

Attached scope: Tech Oil Derrick (CAOILD), owner Neutral, cell (41, 113), tag 0B210EDC, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 14 (Set2).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7205, Events line 7339, Actions line 7473.

<a id="trigger-068c8e4c"></a>

### 82. Set3 - 068C8E4C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Set local flag 15 (Set3).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7206, Events line 7340, Actions line 7474.

<a id="trigger-0923f45c"></a>

### 83. Set3Undo - 0923F45C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Set3 (068C8E4C)](#trigger-068c8e4c).

Attached scope: Tech Oil Derrick (CAOILD), owner Neutral, cell (160, 68), tag 0923F54C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Clear local flag 15 (Set3).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7207, Events line 7341, Actions line 7475.

<a id="trigger-0923f9ec"></a>

### 84. Set5 - 0923F9EC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Set5 (0682068C)](#trigger-0682068c).

Attached scope: 1 tagged map cells: (57, 85); tag 068CA46C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Set5b (06820F3C)](#trigger-06820f3c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7208, Events line 7342, Actions line 7476.

<a id="trigger-06820f3c"></a>

### 85. Set5b - 06820F3C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Set5 (0923F9EC)](#trigger-0923f9ec).

Attached scope: tag definitions 06820C2C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [PB1 (0BE696CC)](sov04dmd-teams.md#team-0be696cc).
2. Supply reinforcement team [PB2 (06823A1C)](sov04dmd-teams.md#team-06823a1c).
3. Supply reinforcement team [PB3 (0682349C)](sov04dmd-teams.md#team-0682349c).
4. Supply reinforcement team [PB4 (06824A6C)](sov04dmd-teams.md#team-06824a6c).
5. Supply reinforcement team [PB5 (0682457C)](sov04dmd-teams.md#team-0682457c).
6. Supply reinforcement team [PB6 (06825B0C)](sov04dmd-teams.md#team-06825b0c).
7. Supply reinforcement team [PB7 (0682559C)](sov04dmd-teams.md#team-0682559c).
8. Supply reinforcement team [PB8 (0682506C)](sov04dmd-teams.md#team-0682506c).
9. Supply reinforcement team [PB9 (06826B3C)](sov04dmd-teams.md#team-06826b3c).
10. Supply reinforcement team [PB10 (068265CC)](sov04dmd-teams.md#team-068265cc).
11. Supply reinforcement team [PB11 (0682609C)](sov04dmd-teams.md#team-0682609c).
12. Supply reinforcement team [PB12 (06827B7C)](sov04dmd-teams.md#team-06827b7c).
13. Supply reinforcement team [PB13 (0682760C)](sov04dmd-teams.md#team-0682760c).
14. Supply reinforcement team [PB14 (0B1FD1FC)](sov04dmd-teams.md#team-0b1fd1fc).
15. Supply reinforcement team [PB15 (0439F88C)](sov04dmd-teams.md#team-0439f88c).
16. Supply reinforcement team [PB16 (0682111C)](sov04dmd-teams.md#team-0682111c).
17. Supply reinforcement team [PB17 (0682124C)](sov04dmd-teams.md#team-0682124c).
18. Supply reinforcement team [PB18 (0C0B672C)](sov04dmd-teams.md#team-0c0b672c).
19. Supply reinforcement team [PB19 (0682211C)](sov04dmd-teams.md#team-0682211c).
20. Supply reinforcement team [PB20 (0439F64C)](sov04dmd-teams.md#team-0439f64c).
21. Enable and reset applicable timers for [Part2 (0BAD7F3C)](#trigger-0bad7f3c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7209, Events line 7343, Actions line 7477.

<a id="trigger-0bad7f3c"></a>

### 86. Part2 - 0BAD7F3C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Set5b (06820F3C)](#trigger-06820f3c).

Attached scope: tag definitions 0BAD77AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Set5 (0923F9EC)](#trigger-0923f9ec).
2. Disable [Set5b (06820F3C)](#trigger-06820f3c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7210, Events line 7344, Actions line 7478.

<a id="trigger-0682068c"></a>

### 87. Enable Set5 - 0682068C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 068200CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 13 (Set1) is set.
2. local flag 14 (Set2) is set.
3. local flag 15 (Set3) is set.
4. local flag 16 (Set4) is set.

Flag writers in this mission: set local flag 13 (Set1) at [Set1 (0923EBAC)](#trigger-0923ebac); clear local flag 13 (Set1) at [Set1Undo (0923E24C)](#trigger-0923e24c); set local flag 14 (Set2) at [Set2 (0923724C)](#trigger-0923724c); clear local flag 14 (Set2) at [Set2Undo (0B210DEC)](#trigger-0b210dec); set local flag 15 (Set3) at [Set3 (068C8E4C)](#trigger-068c8e4c); clear local flag 15 (Set3) at [Set3Undo (0923F45C)](#trigger-0923f45c); set local flag 16 (Set4) at [Set4 (0923FBBC)](#trigger-0923fbbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Set5 (0923F9EC)](#trigger-0923f9ec).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7211, Events line 7345, Actions line 7479.

<a id="trigger-06821f3c"></a>

### 88. Set5bUndo - 06821F3C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 8 tagged map cells: (56, 84), (57, 84), (58, 84), (56, 85), (58, 85), (56, 86), (57, 86), (58, 86); tag 06821D8C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Disable [Set5b (06820F3C)](#trigger-06820f3c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7212, Events line 7346, Actions line 7480.

<a id="trigger-09412afc"></a>

### 89. _Reinforcements 1 - 09412AFC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0941091C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 6.

**Then perform these actions in order:**

1. Supply reinforcement team [_Easy Reinforcements 1 (075D3C8C)](sov04dmd-teams.md#team-075d3c8c).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Enable and reset applicable timers for [_Reinforcements 1a (078356AC)](#trigger-078356ac).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7213, Events line 7347, Actions line 7481.

<a id="trigger-078356ac"></a>

### 90. _Reinforcements 1a - 078356AC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Reinforcements 1 (09412AFC)](#trigger-09412afc).

Attached scope: tag definitions 078352CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound ApocalypseSelect.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7214, Events line 7348, Actions line 7482.

<a id="trigger-094132bc"></a>

### 91. _Reinforcements 2 - 094132BC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0943F94C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 15.

**Then perform these actions in order:**

1. Supply reinforcement team [_Easy Reinforcements 2 (0789FEFC)](sov04dmd-teams.md#team-0789fefc).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Enable and reset applicable timers for [_Reinforcements 2a (078312EC)](#trigger-078312ec).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7215, Events line 7349, Actions line 7483.

<a id="trigger-078312ec"></a>

### 92. _Reinforcements 2a - 078312EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Reinforcements 2 (094132BC)](#trigger-094132bc).

Attached scope: tag definitions 07832CDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound DesolatorSelect.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7216, Events line 7350, Actions line 7484.

<a id="trigger-0943ef3c"></a>

### 93. _Reinforcements 3 - 0943EF3C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0943AACC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  #: 3.

**Then perform these actions in order:**

1. Supply reinforcement team [_Easy Reinforcements 3 (075D332C)](sov04dmd-teams.md#team-075d332c).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Enable and reset applicable timers for [_Reinforcements 3a (0783424C)](#trigger-0783424c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7217, Events line 7351, Actions line 7485.

<a id="trigger-0783424c"></a>

### 94. _Reinforcements 3a - 0783424C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Reinforcements 3 (0943EF3C)](#trigger-0943ef3c).

Attached scope: tag definitions 0783164C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound ApocalypseSelect.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7218, Events line 7352, Actions line 7486.

<a id="trigger-043c590c"></a>

### 95. Our Engine is Fun! - 043C590C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 043C568C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [_Rom Search 1 (08FF2B7C)](sov04dmd-teams.md#team-08ff2b7c).
2. Create/recruit team [_Rom Search 2 (08FF221C)](sov04dmd-teams.md#team-08ff221c).
3. Create/recruit team [_Rom Search 3 (08FF1B7C)](sov04dmd-teams.md#team-08ff1b7c).
4. Create/recruit team [_Rom Search 4 (08FF113C)](sov04dmd-teams.md#team-08ff113c).
5. Create/recruit team [_Rom Search 5 (08FF0A9C)](sov04dmd-teams.md#team-08ff0a9c).
6. Create/recruit team [_Rom Search 6 (08FF050C)](sov04dmd-teams.md#team-08ff050c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7219, Events line 7353, Actions line 7487.

<a id="trigger-0972c2fc"></a>

### 96. Garrison Teams Easy - 0972C2FC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0972D8CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_Garrison Team 1 (08DFAB5C)](sov04dmd-teams.md#team-08dfab5c).
2. Supply reinforcement team [_Garrison Team 2 (08DFA6AC)](sov04dmd-teams.md#team-08dfa6ac).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7220, Events line 7354, Actions line 7488.

<a id="trigger-0fc311dc"></a>

### 97. Moving Cam - 0FC311DC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0FB4104C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 52 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 32 (cell 103, 19).
2. Move the camera to waypoint 32 (cell 103, 19) with speed setting 3.
3. Enable and reset applicable timers for [Moving Cam 2 (097A004C)](#trigger-097a004c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7221, Events line 7355, Actions line 7489.

<a id="trigger-097a004c"></a>

### 98. Moving Cam 2 - 097A004C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Moving Cam (0FC311DC)](#trigger-0fc311dc).

Attached scope: tag definitions 097A14CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 700 (cell 92, 81).
2. Reveal terrain around waypoint 38 (cell 102, 81).
3. Reveal terrain around waypoint 33 (cell 93, 60).
4. Reveal terrain around waypoint 34 (cell 99, 60).
5. Reveal terrain around waypoint 91 (cell 97, 72).
6. Move the camera to waypoint 91 (cell 97, 72) with speed setting 3.
7. Enable and reset applicable timers for [Moving Cam 3 (0FB4003C)](#trigger-0fb4003c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7222, Events line 7356, Actions line 7490.

<a id="trigger-0fb4003c"></a>

### 99. Moving Cam 3 - 0FB4003C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Moving Cam 2 (097A004C)](#trigger-097a004c).

Attached scope: tag definitions 0FB4B04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 13 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 0 (cell 81, 139) with speed setting 3.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7223, Events line 7357, Actions line 7491.

<a id="trigger-0984d66c"></a>

### 100. @Sounds - Crickets - 0984D66C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09853F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_CricketDesert at waypoint 0 (cell 81, 139).
2. Play sound _Amb_CricketDesert at waypoint 92 (cell 64, 135).
3. Play sound _Amb_CricketDesert at waypoint 93 (cell 96, 131).
4. Play sound _Amb_CricketDesert at waypoint 94 (cell 73, 117).
5. Play sound _Amb_CricketDesert at waypoint 95 (cell 53, 112).
6. Play sound _Amb_CricketDesert at waypoint 96 (cell 62, 94).
7. Play sound _Amb_CricketChirps at waypoint 97 (cell 88, 107).
8. Play sound _Amb_CricketDesert at waypoint 98 (cell 110, 116).
9. Play sound _Amb_CricketDesert at waypoint 99 (cell 69, 83).
10. Play sound _Amb_CricketDesert at waypoint 21 (cell 96, 98).
11. Play sound _Amb_CricketDesert at waypoint 100 (cell 48, 86).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7224, Events line 7358, Actions line 7492.

<a id="trigger-0cd0712c"></a>

### 101. @Sounds - Crickets 2 - 0CD0712C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CD0704C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_CricketDesert at waypoint 67 (cell 49, 74).
2. Play sound _Amb_CricketDesert at waypoint 40 (cell 66, 70).
3. Play sound _Amb_CricketDesert at waypoint 101 (cell 71, 56).
4. Play sound _Amb_CricketDesert at waypoint 13 (cell 89, 70).
5. Play sound _Amb_CricketChirps at waypoint 15 (cell 107, 70).
6. Play sound _Amb_CricketDesert at waypoint 23 (cell 115, 101).
7. Play sound _Amb_CricketDesert at waypoint 24 (cell 132, 101).
8. Play sound _Amb_CricketDesert at waypoint 25 (cell 134, 86).
9. Play sound _Amb_CricketDesert at waypoint 102 (cell 115, 58).
10. Play sound _Amb_CricketChirps at waypoint 17 (cell 133, 59).
11. Play sound _Amb_CricketDesert at waypoint 19 (cell 148, 69).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7225, Events line 7359, Actions line 7493.

<a id="trigger-0cd1e3ac"></a>

### 102. @Sounds - Crickets 3 - 0CD1E3AC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0CD1FDAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound _Amb_CricketDesert at waypoint 103 (cell 116, 39).
2. Play sound _Amb_CricketChirps at waypoint 104 (cell 99, 43).
3. Play sound _Amb_CricketDesert at waypoint 105 (cell 84, 40).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7226, Events line 7360, Actions line 7494.

<a id="trigger-097ad9ac"></a>

### 103. It's Safe? - 097AD9AC

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 4 tagged map cells: (94, 53), (95, 53), (96, 53), (97, 53); tag 097AD0FC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 3 (country/type GERMANS; placed owner Germans).
2. local flag 18 (It's Safe) is clear.

Flag writers in this mission: set local flag 18 (It's Safe) at [It's Safe! V1 (0682762C)](#trigger-0682762c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_ZofiaStopRomanov.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7227, Events line 7361, Actions line 7495.

<a id="trigger-0d0d4cac"></a>

### 104. Wandering Camels - 0D0D4CAC

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D10077C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Wandering Camel (0690F06C)](sov04dmd-teams.md#team-0690f06c).
2. Create/recruit team [Wandering Camel 2 (069DEADC)](sov04dmd-teams.md#team-069deadc).
3. Create/recruit team [Wandering Camel 3 (097B147C)](sov04dmd-teams.md#team-097b147c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7228, Events line 7362, Actions line 7496.

<a id="trigger-0d10005c"></a>

### 105. Brute Set - 0D10005C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Brute (BRUTE), owner YuriCountry, cell (79, 103), tag 0D101DEC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Flash team [_S04_Brute Demo (093B0EFC)](sov04dmd-teams.md#team-093b0efc) with duration setting 90.
2. Play voice notification Unit_Sofia_Brute.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7229, Events line 7363, Actions line 7497.

<a id="trigger-07a5981c"></a>

### 106. Rom in Yuri Base - 07A5981C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A590EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 20 (Rom In Yuri Base) is set.

**Then perform these actions in order:**

1. Play voice notification Mis_xS4_RomanovHelpMe.
2. Disable [Rom in Yuri Base (07A5981C)](#trigger-07a5981c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7230, Events line 7364, Actions line 7498.

<a id="trigger-089f57bc"></a>

### 107. Power Off For Good - 089F57BC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089F9E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Bio Reactor (YAPOWR) exist on the map, under this event's ownership scope.
2. No instances of Yuri Construction Yard (YACNST) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 5 (Low Power).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7231, Events line 7365, Actions line 7499.

<a id="trigger-075e947c"></a>

### 108. Med - Xtra Power - 075E947C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 075EAEEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_S04_Xtra Power (08A47EFC)](sov04dmd-teams.md#team-08a47efc) at waypoint 111 (cell 89, 28).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7232, Events line 7366, Actions line 7500.

<a id="trigger-075eac0c"></a>

### 109. Hard - Xtra Power - 075EAC0C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 075EA9CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_S04_Xtra Power (08A47EFC)](sov04dmd-teams.md#team-08a47efc) at waypoint 112 (cell 108, 16).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7233, Events line 7367, Actions line 7501.

<a id="trigger-097304ac"></a>

### 110. Dumb Player - 097304AC

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0973358C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Declare owner selector 8 (country/type RUSSIANS; placed owner Russians) the loser.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7234, Events line 7368, Actions line 7502.

<a id="trigger-078276ec"></a>

### 111. Gattling Killed 1 - 078276EC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner Arabs, cell (92, 34), tag 07825A2C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 21 (Gattling 1).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7235, Events line 7369, Actions line 7503.

<a id="trigger-0782593c"></a>

### 112. Gattling Killed 1b - 0782593C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (20, 117), tag 078256FC, persistence mode 0.

**Wait for the recorded events:**

1. local flag 21 (Gattling 1) is set.

Flag writers in this mission: set local flag 21 (Gattling 1) at [Gattling Killed 1 (078276EC)](#trigger-078276ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7236, Events line 7370, Actions line 7504.

<a id="trigger-078250cc"></a>

### 113. Gattling Killed 2 - 078250CC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner Arabs, cell (100, 34), tag 07824E7C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 22 (Gattling 2).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7237, Events line 7371, Actions line 7505.

<a id="trigger-07824b0c"></a>

### 114. Gattling Killed 3 - 07824B0C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner Arabs, cell (100, 21), tag 078248CC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 23 (Gattling 3).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7238, Events line 7372, Actions line 7506.

<a id="trigger-078247dc"></a>

### 115. Gattling Killed 4 - 078247DC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner Arabs, cell (106, 21), tag 0782459C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 24 (Gattling 4).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7239, Events line 7373, Actions line 7507.

<a id="trigger-078244ac"></a>

### 116. Gattling Killed 5 - 078244AC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07823EAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 25 (Gattling 5).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7240, Events line 7374, Actions line 7508.

<a id="trigger-07823dbc"></a>

### 117. Gattling Killed 6 - 07823DBC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner Arabs, cell (106, 15), tag 07823CDC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 26 (Gattling 6).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7241, Events line 7375, Actions line 7509.

<a id="trigger-078230cc"></a>

### 118. Gattling Killed 2b - 078230CC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (22, 119), tag 0782536C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 22 (Gattling 2) is set.

Flag writers in this mission: set local flag 22 (Gattling 2) at [Gattling Killed 2 (078250CC)](#trigger-078250cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7242, Events line 7376, Actions line 7510.

<a id="trigger-07829d1c"></a>

### 119. Gattling Killed 3b - 07829D1C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (24, 121), tag 07828C6C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 23 (Gattling 3) is set.

Flag writers in this mission: set local flag 23 (Gattling 3) at [Gattling Killed 3 (07824B0C)](#trigger-07824b0c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7243, Events line 7377, Actions line 7511.

<a id="trigger-07828b7c"></a>

### 120. Gattling Killed 4b - 07828B7C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (26, 123), tag 0782893C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 24 (Gattling 4) is set.

Flag writers in this mission: set local flag 24 (Gattling 4) at [Gattling Killed 4 (078247DC)](#trigger-078247dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7244, Events line 7378, Actions line 7512.

<a id="trigger-05e0d9ac"></a>

### 121. Gattling Killed 5b - 05E0D9AC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05E0D42C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 25 (Gattling 5) is set.

Flag writers in this mission: set local flag 25 (Gattling 5) at [Gattling Killed 5 (078244AC)](#trigger-078244ac). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7245, Events line 7379, Actions line 7513.

<a id="trigger-05e0d33c"></a>

### 122. Gattling Killed 6b - 05E0D33C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Gattling Cannon (YAGGUN), owner YuriCountry, cell (30, 127), tag 05E0EE7C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 26 (Gattling 6) is set.

Flag writers in this mission: set local flag 26 (Gattling 6) at [Gattling Killed 6 (07823DBC)](#trigger-07823dbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7246, Events line 7380, Actions line 7514.

<a id="trigger-0778fbcc"></a>

### 123. Power Down For Good 2 - 0778FBCC

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 5 (Low Power) is set.

Flag writers in this mission: set local flag 5 (Low Power) at [Turn Off Power (0BCDC0FC)](#trigger-0bcdc0fc); set local flag 5 (Low Power) at [Power Off For Good (089F57BC)](#trigger-089f57bc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 12 (country/type NEUTRAL; placed owner Neutral).
2. Disable [Power Down For Good 2 (0778FBCC)](#trigger-0778fbcc).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7247, Events line 7381, Actions line 7515.

<a id="trigger-07788f3c"></a>

### 124. Power Up 2 - 07788F3C

Owner reference: Arabs. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Power Down For Good 2 (0778FBCC)](#trigger-0778fbcc).

Incoming activation links: enable from [Power Low 2 (07789F3C)](#trigger-07789f3c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Power Full: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Change House: owner selector 6 (country/type ARABS; placed owner Arabs).
2. Disable [Power Up 2 (07788F3C)](#trigger-07788f3c).
3. Enable and reset applicable timers for [Power Low 2 (07789F3C)](#trigger-07789f3c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7248, Events line 7382, Actions line 7516.

<a id="trigger-07789f3c"></a>

### 125. Power Low 2 - 07789F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Power Up 2 (07788F3C)](#trigger-07788f3c).

Incoming activation links: enable from [Power Up 2 (07788F3C)](#trigger-07788f3c).

Attached scope: Nuclear Reactor (NANRCT), owner Arabs, cell (33, 129), tag 0778FAEC, persistence mode 2.

**Wait for the recorded events:**

1. Low Power: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Change House: owner selector 12 (country/type NEUTRAL; placed owner Neutral).
2. Disable [Power Low 2 (07789F3C)](#trigger-07789f3c).
3. Enable and reset applicable timers for [Power Up 2 (07788F3C)](#trigger-07788f3c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7249, Events line 7383, Actions line 7517.

<a id="trigger-05b545fc"></a>

### 126. Kill Base 2 Light - 05B545FC

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Blue Light Post (INBLULMP), owner Neutral, cell (32, 93), tag 05B52DDC, persistence mode 0.

**Wait for the recorded events:**

1. local flag 27 (Light 2) is set.

Flag writers in this mission: set local flag 27 (Light 2) at [End IT! Respawn (0437F64C)](#trigger-0437f64c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7250, Events line 7384, Actions line 7518.

<a id="trigger-05b523fc"></a>

### 127. Kill Base 1 Light - 05B523FC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Invisible Blue Light Post (INBLULMP), owner Neutral, cell (92, 23), tag 05B521BC, persistence mode 0.

**Wait for the recorded events:**

1. local flag 28 (Light 1) is set.

Flag writers in this mission: set local flag 28 (Light 1) at [Blow Up Light 1 (05B7F1CC)](#trigger-05b7f1cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7251, Events line 7385, Actions line 7519.

<a id="trigger-05b7f1cc"></a>

### 128. Blow Up Light 1 - 05B7F1CC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 05B7B98C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No instances of Yuri Construction Yard (YACNST) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Set local flag 28 (Light 1).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7252, Events line 7386, Actions line 7520.

<a id="trigger-078347bc"></a>

### 129. Easy Reinforcments 2a - 078347BC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0783457C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play sound CrazyIvanAttackCommand.

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7253, Events line 7387, Actions line 7521.

<a id="trigger-0762a5ac"></a>

### 130. Garrison Team Normal - 0762A5AC

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0762BF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_Garrison Team 5 (08DFB7DC)](sov04dmd-teams.md#team-08dfb7dc).
2. Supply reinforcement team [_Garrison Team 6 (08DFB32C)](sov04dmd-teams.md#team-08dfb32c).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7254, Events line 7388, Actions line 7522.

<a id="trigger-0762be5c"></a>

### 131. Garrison Team Hard - 0762BE5C

Owner reference: YuriCountry. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0762BA7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [_Garrison Team 3 (08DFA1FC)](sov04dmd-teams.md#team-08dfa1fc).
2. Supply reinforcement team [_Garrison Team 4 (08DFBC8C)](sov04dmd-teams.md#team-08dfbc8c).
3. Supply reinforcement team [_Garrison Team 7 (08DFCDEC)](sov04dmd-teams.md#team-08dfcdec).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7255, Events line 7389, Actions line 7523.

<a id="trigger-0852486c"></a>

### 132. Break Base Defense - 0852486C

Owner reference: Alliance. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Bio Reactor (YAPOWR), owner Alliance, cell (32, 101), tag 0852421C, persistence mode 0; Bio Reactor (YAPOWR), owner Alliance, cell (40, 102), tag 0852421C, persistence mode 0; Bio Reactor (YAPOWR), owner Alliance, cell (40, 98), tag 0852421C, persistence mode 0; Bio Reactor (YAPOWR), owner Alliance, cell (40, 86), tag 0852421C, persistence mode 0; Bio Reactor (YAPOWR), owner Alliance, cell (36, 86), tag 0852421C, persistence mode 0; Yuri War Factory (YAWEAP), owner Alliance, cell (24, 91), tag 0852421C, persistence mode 0; Yuri Battle Lab (YATECH), owner Alliance, cell (24, 97), tag 0852421C, persistence mode 0; Bio Reactor (YAPOWR), owner Alliance, cell (35, 98), tag 0852421C, persistence mode 0; Bio Reactor (YAPOWR), owner Alliance, cell (29, 96), tag 0852421C, persistence mode 0; Bio Reactor (YAPOWR), owner Alliance, cell (32, 86), tag 0852421C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [_Cap Base Defense 1 (0B3CEDEC)](sov04dmd-teams.md#team-0b3cedec).
2. Remove instances of the team organization (not automatically its surviving objects) [_Cap Base Defense 2 (0B3CFDEC)](sov04dmd-teams.md#team-0b3cfdec).

Source locator: mapsmd03.mix/sov04dmd.map; Triggers line 7256, Events line 7390, Actions line 7524.

[All team rosters and ordered plans](sov04dmd-teams.md) | [All mission overrides](sov04dmd-overrides.md)
