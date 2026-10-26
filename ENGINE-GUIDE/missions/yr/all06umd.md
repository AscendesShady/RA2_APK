# Operation: Trick or Treaty

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all06umd.map. **Effective extracted member:** mapsmd03.mix/all06umd.map. **Trigger definitions:** 75.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all06umd-teams.md) | [All mission overrides](all06umd-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Americans |
| Theater | NEWURBAN |
| Map size | 0,0,60,85 |
| Visible local rectangle | 2,41,56,38 |
| Placed vehicles | 18 |
| Placed infantry | 14 |
| Placed structures | 233 |
| Placed aircraft | 0 |
| Team templates | 68 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 250 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 0 | Africans |
| 6 | Arabs | 0 | Arabs |
| 7 | Confederation | 0 | Confederation |
| 8 | Russians | 0 | Russians |
| 9 | YuriCountry | 450 | YuriCountry |
| 10 | GDI | 0 | GDI |
| 11 | Nod | 0 | Nod |
| 12 | Neutral | 0 | Neutral |
| 13 | Special | 0 | Special |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Unloaded Limo 1,0 |
| 1 | Unloaded Limo 2,0 |
| 2 | Unloaded Limo 3,0 |
| 3 | Setpiece1_Unlock,0 |
| 4 | Unloaded Heli 1,0 |
| 5 | Unloaded Heli 2,0 |
| 6 | Unloaded Bridge Lef,0 |
| 7 | Unloaded Bridge Mid,0 |
| 8 | Unloaded Bridge Rig,0 |
| 9 | Unloaded BK Team,0 |
| 10 | Unloaded BL Team,0 |
| 11 | Left Broken,0 |
| 12 | Middle Broken,0 |
| 13 | Right Broken,0 |
| 14 | Master Mind Intro,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Player Loses (0BD7FB3C)](#trigger-0bd7fb3c) | 2 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser. |
| [Player Wins (0BD7E82C)](#trigger-0bd7e82c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner. |

## Every trigger, in file order

<a id="trigger-09ad534c"></a>

### 1. Movie1_Briefing - 09AD534C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09AD51AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play in-game movie 24.
2. Enable and reset applicable timers for [Setpiece1_Limo1Arrive (09AD6A2C)](#trigger-09ad6a2c).
3. Enable and reset applicable timers for [Movie1_Audio Portion (0F35541C)](#trigger-0f35541c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6137, Events line 6214, Actions line 6291.

<a id="trigger-09ad6a2c"></a>

### 2. Setpiece1_Limo1Arrive - 09AD6A2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Movie1_Briefing (09AD534C)](#trigger-09ad534c).

Attached scope: tag definitions 09AD694C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Limo 1 Team (08EEB7DC)](all06umd-teams.md#team-08eeb7dc).
2. Enable and reset applicable timers for [Setpiece1_Limo2Arrive (048E961C)](#trigger-048e961c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6138, Events line 6215, Actions line 6292.

<a id="trigger-0f35541c"></a>

### 3. Movie1_Audio Portion - 0F35541C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Movie1_Briefing (09AD534C)](#trigger-09ad534c).

Attached scope: tag definitions 0F35303C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification A06_p01.
2. Enable and reset applicable timers for [Movie1_Radar Ping (0C5B195C)](#trigger-0c5b195c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6139, Events line 6216, Actions line 6293.

<a id="trigger-048e961c"></a>

### 4. Setpiece1_Limo2Arrive - 048E961C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Limo1Arrive (09AD6A2C)](#trigger-09ad6a2c).

Attached scope: tag definitions 048E953C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 11 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Limo 2 Team (08EEADEC)](all06umd-teams.md#team-08eeadec).
2. Enable and reset applicable timers for [Setpiece1_Limo3Arrive (070A410C)](#trigger-070a410c).
3. Move the camera to waypoint 23 (cell 92, 115) with speed setting 0.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6140, Events line 6217, Actions line 6294.

<a id="trigger-0c5b195c"></a>

### 5. Movie1_Radar Ping - 0C5B195C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Movie1_Audio Portion (0F35541C)](#trigger-0f35541c).

Attached scope: tag definitions 0C5B187C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 14 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 11 at waypoint 23 (cell 92, 115).
2. Play sound BeaconPlaced.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6141, Events line 6218, Actions line 6295.

<a id="trigger-070a410c"></a>

### 6. Setpiece1_Limo3Arrive - 070A410C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Limo2Arrive (048E961C)](#trigger-048e961c).

Attached scope: tag definitions 070A1F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Limo 3 Team (08EEA80C)](all06umd-teams.md#team-08eea80c).
2. Enable and reset applicable timers for [Setpiece1_Heli1Arrive (09A5D20C)](#trigger-09a5d20c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6142, Events line 6219, Actions line 6296.

<a id="trigger-09a5d20c"></a>

### 7. Setpiece1_Heli1Arrive - 09A5D20C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Limo3Arrive (070A410C)](#trigger-070a410c).

Attached scope: tag definitions 09A5D09C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 28 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Heli  1 Team (08EEA33C)](all06umd-teams.md#team-08eea33c).
2. Enable and reset applicable timers for [Setpiece1_Heli2Arrive (09A5D3DC)](#trigger-09a5d3dc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6143, Events line 6220, Actions line 6297.

<a id="trigger-09a5d3dc"></a>

### 8. Setpiece1_Heli2Arrive - 09A5D3DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Heli1Arrive (09A5D20C)](#trigger-09a5d20c).

Attached scope: tag definitions 09A5D2FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Heli  2 Team (08EE9DEC)](all06umd-teams.md#team-08ee9dec).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6144, Events line 6221, Actions line 6298.

<a id="trigger-09ada12c"></a>

### 9. Setpiece1_Limo1Leave - 09ADA12C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09ADA04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Unloaded Limo 1) is set.

**Then perform these actions in order:**

1. Create/recruit team [TM_Unloaded Limo 1 Team (0712A3AC)](all06umd-teams.md#team-0712a3ac).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6145, Events line 6222, Actions line 6299.

<a id="trigger-048d972c"></a>

### 10. Setpiece1_Limo2Leave - 048D972C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 048DB10C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Unloaded Limo 2) is set.

**Then perform these actions in order:**

1. Create/recruit team [TM_Unloaded Limo 2 Team (0712B91C)](all06umd-teams.md#team-0712b91c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6146, Events line 6223, Actions line 6300.

<a id="trigger-070a1e5c"></a>

### 11. Setpiece1_Limo3Leave - 070A1E5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 070A1D7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Unloaded Limo 3) is set.

**Then perform these actions in order:**

1. Create/recruit team [TM_Unloaded Limo 3 Team (0712B44C)](all06umd-teams.md#team-0712b44c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6147, Events line 6224, Actions line 6301.

<a id="trigger-09a5d77c"></a>

### 12. Setpiece1_Heli2Leave - 09A5D77C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09A5D69C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (Unloaded Heli 2) is set.

**Then perform these actions in order:**

1. Create/recruit team [TM_Unloaded Heli  2 Team (0712C37C)](all06umd-teams.md#team-0712c37c).
2. Play sound RomanovSelect.
3. Create/recruit team [TM_Unloaded Heli_1 Romanov (0E2EB04C)](all06umd-teams.md#team-0e2eb04c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6148, Events line 6225, Actions line 6302.

<a id="trigger-09a5d5ac"></a>

### 13. Setpiece1_Heli1Leave - 09A5D5AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09A5D4CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 4 (Unloaded Heli 1) is set.

**Then perform these actions in order:**

1. Create/recruit team [TM_Unloaded Heli  1 Team (0712C82C)](all06umd-teams.md#team-0712c82c).
2. Play voice notification Mis_S9_President4.
3. Create/recruit team [TM_Unloaded Heli_1 Pres (0E34745C)](all06umd-teams.md#team-0e34745c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6149, Events line 6226, Actions line 6303.

<a id="trigger-09b5d40c"></a>

### 14. Allied Mission 6_Setup - 09B5D40C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09ADAA7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable player input.
2. Resize Player View; main setting 0; parameter 1: 2, parameter 2: 41, parameter 3: 56, parameter 4: 38.
3. Reveal terrain around waypoint 26 (cell 65, 109).
4. Reveal terrain around waypoint 27 (cell 84, 109).
5. Reveal terrain around waypoint 28 (cell 111, 109).
6. Reveal terrain around waypoint 29 (cell 103, 110).
7. Reveal terrain around waypoint 30 (cell 93, 110).
8. Reveal terrain around waypoint 31 (cell 75, 111).
9. Reveal terrain around waypoint 32 (cell 65, 116).
10. Reveal terrain around waypoint 33 (cell 75, 118).
11. Reveal terrain around waypoint 34 (cell 89, 119).
12. Reveal terrain around waypoint 35 (cell 102, 118).
13. Reveal terrain around waypoint 36 (cell 74, 126).
14. Reveal terrain around waypoint 37 (cell 83, 134).
15. Reveal terrain around waypoint 38 (cell 97, 125).
16. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6150, Events line 6227, Actions line 6304.

<a id="trigger-0bf31efc"></a>

### 15. Yuri Wave Attack 1 - 0BF31EFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Warning_REYuri_Med (0BF330EC)](#trigger-0bf330ec); enable from [Warning_RE Yuri_Easy (091F3D6C)](#trigger-091f3d6c); enable from [Warning_RE Yuri_Hard (091F3F3C)](#trigger-091f3f3c).

Attached scope: tag definitions 0BF31CCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_6 Initiates (middle) (0B2CE0EC)](all06umd-teams.md#team-0b2ce0ec).
2. Supply reinforcement team [TM_Yuri_6 Initiates (right) (0B2CFB7C)](all06umd-teams.md#team-0b2cfb7c).
3. Supply reinforcement team [TM_Yuri_6 Lashers (Right) (0B2CF7DC)](all06umd-teams.md#team-0b2cf7dc).
4. Supply reinforcement team [TM_Yuri_6 Initiates (left) (0B2CB6FC)](all06umd-teams.md#team-0b2cb6fc).
5. Supply reinforcement team [TM_Yuri_6 Lashers (Left) (0B2CF18C)](all06umd-teams.md#team-0b2cf18c).
6. Enable and reset applicable timers for [Yuri Wave Attack 2 (06C160CC)](#trigger-06c160cc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6151, Events line 6228, Actions line 6305.

<a id="trigger-06c160cc"></a>

### 16. Yuri Wave Attack 2 - 06C160CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Wave Attack 1 (0BF31EFC)](#trigger-0bf31efc).

Attached scope: tag definitions 06C14E3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 160 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_3 Gattling (left) (06C0E3DC)](all06umd-teams.md#team-06c0e3dc).
2. Supply reinforcement team [TM_Yuri_3 Gattling (middle) (06C6120C)](all06umd-teams.md#team-06c6120c).
3. Supply reinforcement team [TM_Yuri_3 Gattling (right) (06C6235C)](all06umd-teams.md#team-06c6235c).
4. Supply reinforcement team [TM_Yuri_6 Initiates (left) (0B2CB6FC)](all06umd-teams.md#team-0b2cb6fc).
5. Supply reinforcement team [TM_Yuri_6 Initiates (middle) (0B2CE0EC)](all06umd-teams.md#team-0b2ce0ec).
6. Supply reinforcement team [TM_Yuri_6 Initiates (right) (0B2CFB7C)](all06umd-teams.md#team-0b2cfb7c).
7. Enable and reset applicable timers for [Yuri Wave Attack 3 (095ECF3C)](#trigger-095ecf3c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6152, Events line 6229, Actions line 6306.

<a id="trigger-095ecf3c"></a>

### 17. Yuri Wave Attack 3 - 095ECF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Wave Attack 2 (06C160CC)](#trigger-06c160cc).

Attached scope: tag definitions 095ECB4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_2 Master Mind (intro) (077E8BAC)](all06umd-teams.md#team-077e8bac).
2. Supply reinforcement team [TM_Yuri_4 Brute (right) (095EBBEC)](all06umd-teams.md#team-095ebbec).
3. Supply reinforcement team [TM_Yuri_5 Virus 3 Clone (left) (0C5DC94C)](all06umd-teams.md#team-0c5dc94c).
4. Enable and reset applicable timers for [Yuri Wave Attack 4 (095EB2AC)](#trigger-095eb2ac).
5. Supply reinforcement team [TM_Yuri_1 Hov_1 Gatt_5 Init (0B7F57DC)](all06umd-teams.md#team-0b7f57dc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6153, Events line 6230, Actions line 6307.

<a id="trigger-095eb2ac"></a>

### 18. Yuri Wave Attack 4 - 095EB2AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Wave Attack 3 (095ECF3C)](#trigger-095ecf3c).

Attached scope: tag definitions 095EB1CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Yuri Wave Attack 5 (095EB0DC)](#trigger-095eb0dc).
2. Supply reinforcement team [TM_Yuri_3 Gattling (left) (06C0E3DC)](all06umd-teams.md#team-06c0e3dc).
3. Supply reinforcement team [TM_Yuri_3 Gattling (middle) (06C6120C)](all06umd-teams.md#team-06c6120c).
4. Supply reinforcement team [TM_Yuri_3 Gattling (right) (06C6235C)](all06umd-teams.md#team-06c6235c).
5. Supply reinforcement team [TM_Yuri_2 Floating Discs (0879E90C)](all06umd-teams.md#team-0879e90c).
6. Supply reinforcement team [TM_Yuri_2 Master Mind (left) (0C5DC12C)](all06umd-teams.md#team-0c5dc12c).
7. Supply reinforcement team [TM_Yuri_2 Master Mind (right) (0C5DC25C)](all06umd-teams.md#team-0c5dc25c).
8. Supply reinforcement team [TM_Yuri_3 Gattling (far left) (0C5DDEFC)](all06umd-teams.md#team-0c5ddefc).
9. Supply reinforcement team [TM_Yuri_1 Hov_2 Gatt (0B7F050C)](all06umd-teams.md#team-0b7f050c).
10. Enable and reset applicable timers for [Yuri Wave Attack 4a (086D334C)](#trigger-086d334c).
11. Enable and reset applicable timers for [Yuri Wave Attack 4b (05C6450C)](#trigger-05c6450c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6154, Events line 6231, Actions line 6308.

<a id="trigger-095eb0dc"></a>

### 19. Yuri Wave Attack 5 - 095EB0DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Wave Attack 4 (095EB2AC)](#trigger-095eb2ac).

Attached scope: tag definitions 095F2F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_3 Gattling (far left) (0C5DDEFC)](all06umd-teams.md#team-0c5ddefc).
2. Supply reinforcement team [TM_Yuri_2 Floating Discs (0879E90C)](all06umd-teams.md#team-0879e90c).
3. Supply reinforcement team [TM_Yuri_2 Master Mind (left) (0C5DC12C)](all06umd-teams.md#team-0c5dc12c).
4. Supply reinforcement team [TM_Yuri_2 Master Mind (Mid) (08EFD34C)](all06umd-teams.md#team-08efd34c).
5. Supply reinforcement team [TM_Yuri_2 Master Mind (right) (0C5DC25C)](all06umd-teams.md#team-0c5dc25c).
6. Supply reinforcement team [TM_Yuri_3 Gattling (left) (06C0E3DC)](all06umd-teams.md#team-06c0e3dc).
7. Supply reinforcement team [TM_Yuri_3 Gattling (middle) (06C6120C)](all06umd-teams.md#team-06c6120c).
8. Supply reinforcement team [TM_Yuri_3 Gattling (right) (06C6235C)](all06umd-teams.md#team-06c6235c).
9. Supply reinforcement team [TM_Yuri_4 Brute (right) (095EBBEC)](all06umd-teams.md#team-095ebbec).
10. Supply reinforcement team [TM_Yuri_5 Virus 3 Clone (left) (0C5DC94C)](all06umd-teams.md#team-0c5dc94c).
11. Supply reinforcement team [TM_Yuri_6 Initiates (left) (0B2CB6FC)](all06umd-teams.md#team-0b2cb6fc).
12. Supply reinforcement team [TM_Yuri_6 Initiates (middle) (0B2CE0EC)](all06umd-teams.md#team-0b2ce0ec).
13. Supply reinforcement team [TM_Yuri_6 Initiates (right) (0B2CFB7C)](all06umd-teams.md#team-0b2cfb7c).
14. Supply reinforcement team [TM_Yuri_6 Lashers (Left) (0B2CF18C)](all06umd-teams.md#team-0b2cf18c).
15. Supply reinforcement team [TM_Yuri_6 Lashers (middle) (06C6222C)](all06umd-teams.md#team-06c6222c).
16. Supply reinforcement team [TM_Yuri_6 Lashers (Right) (0B2CF7DC)](all06umd-teams.md#team-0b2cf7dc).
17. Enable and reset applicable timers for [Yuri Wave Attack 5 Dead (0CD2E62C)](#trigger-0cd2e62c).
18. Supply reinforcement team [TM_Yuri_1 Hov_1 Gatt_5 Init (0B7F57DC)](all06umd-teams.md#team-0b7f57dc).
19. Supply reinforcement team [TM_Yuri_1 Hov_2 Gatt (0B7F050C)](all06umd-teams.md#team-0b7f050c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6155, Events line 6232, Actions line 6309.

<a id="trigger-086d334c"></a>

### 20. Yuri Wave Attack 4a - 086D334C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Wave Attack 4 (095EB2AC)](#trigger-095eb2ac).

Attached scope: tag definitions 086D6CBC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA6_CarvilleFloatingDisc.
2. Reveal terrain around waypoint 71 (cell 84, 69).
3. Create radar-event marker type 0 at waypoint 71 (cell 84, 69).
4. Play sound BeaconPlaced.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6156, Events line 6233, Actions line 6310.

<a id="trigger-0cd2e62c"></a>

### 21. Yuri Wave Attack 5 Dead - 0CD2E62C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Wave Attack 5 (095EB0DC)](#trigger-095eb0dc).

Attached scope: tag definitions 0CD2F95C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  All: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Setpiece 2_Treaty Movie (0CD2F42C)](#trigger-0cd2f42c).
2. Disable [Wave Attack Prod (05C6397C)](#trigger-05c6397c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6157, Events line 6234, Actions line 6311.

<a id="trigger-0cd2f42c"></a>

### 22. Setpiece 2_Treaty Movie - 0CD2F42C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Wave Attack 5 Dead (0CD2E62C)](#trigger-0cd2e62c).

Attached scope: tag definitions 0CD2F34C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 26.
2. Disable player input.
3. Jump the camera to waypoint 23 (cell 92, 115).
4. Enable and reset applicable timers for [Setpiece2_Treaty Audio (0E2F6B1C)](#trigger-0e2f6b1c).
5. Play voice notification EVA_BattleControlOnline.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6158, Events line 6235, Actions line 6312.

<a id="trigger-0e2f6b1c"></a>

### 23. Setpiece2_Treaty Audio - 0E2F6B1C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece 2_Treaty Movie (0CD2F42C)](#trigger-0cd2f42c).

Attached scope: tag definitions 0E2F6A3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification A06_p04.
2. Enable and reset applicable timers for [Setpiece2_SovietsArrive (0B913B6C)](#trigger-0b913b6c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6159, Events line 6236, Actions line 6313.

<a id="trigger-0b913b6c"></a>

### 24. Setpiece2_SovietsArrive - 0B913B6C

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece2_Treaty Audio (0E2F6B1C)](#trigger-0e2f6b1c).

Attached scope: tag definitions 0B913A8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 27 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 60 (cell 102, 104) with speed setting 2.
2. Supply reinforcement team [TM_Sov_1 Armor_2 Flak Trak (09513C2C)](all06umd-teams.md#team-09513c2c).
3. Supply reinforcement team [TM_Sov_1 Armor_8 Tesla_2 TDrone (095776AC)](all06umd-teams.md#team-095776ac).
4. Supply reinforcement team [TM_Sov_1 Armored_2 Rhino (0957513C)](all06umd-teams.md#team-0957513c).
5. Supply reinforcement team [TM_Sov_2 Dread_3 Scorp_3 Sub (091F259C)](all06umd-teams.md#team-091f259c).
6. Enable and reset applicable timers for [Setpiece2_Unlock Ready (0957813C)](#trigger-0957813c).
7. Play voice notification EVA_ReinforcementsHaveArrived.
8. All change house: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6160, Events line 6237, Actions line 6314.

<a id="trigger-0957813c"></a>

### 25. Setpiece2_Unlock Ready - 0957813C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece2_SovietsArrive (0B913B6C)](#trigger-0b913b6c).

Attached scope: tag definitions 095138DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Resize Player View; main setting 0; parameter 1: 2, parameter 2: 7, parameter 3: 56, parameter 4: 72.
3. Enable and reset applicable timers for [Setpiece2_End (06C2AAFC)](#trigger-06c2aafc).
4. All change house: owner selector 0 (country/type AMERICANS; placed owner Americans).
5. Make side cheer: owner selector 0 (country/type AMERICANS; placed owner Americans).
6. Display message “Objective 2: Destroy Yuri's Base.” (MISSION:All6Obj2).
7. Enable and reset applicable timers for [Setpiece2_Obj2 Restate (0A13E03C)](#trigger-0a13e03c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6161, Events line 6238, Actions line 6315.

<a id="trigger-06c2aafc"></a>

### 26. Setpiece2_End - 06C2AAFC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece2_Unlock Ready (0957813C)](#trigger-0957813c).

Attached scope: tag definitions 06C2AA1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_1 Slave Miner @ BN (091FFA4C)](all06umd-teams.md#team-091ffa4c).
2. Supply reinforcement team [TM_Yuri_1 Slave Miner @ BO (0CCCEEFC)](all06umd-teams.md#team-0ccceefc).
3. Supply reinforcement team [TM_Yuri_6 Init Def @ BP (091FF46C)](all06umd-teams.md#team-091ff46c).
4. Supply reinforcement team [TM_Yuri_6 Init Def @ BQ (091F8EFC)](all06umd-teams.md#team-091f8efc).
5. Supply reinforcement team [TM_Yuri_6 Init Def @ BR (091F8DCC)](all06umd-teams.md#team-091f8dcc).
6. Supply reinforcement team [TM_Yuri_3 Gatt Def @ BS (090020CC)](all06umd-teams.md#team-090020cc).
7. Production Begins: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
8. AI triggers begin: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
9. Enable and reset applicable timers for [Conditions_Lose (06C364EC)](#trigger-06c364ec).
10. Enable and reset applicable timers for [Detect_Yuri Facts Dead (07A07B8C)](#trigger-07a07b8c).
11. Supply reinforcement team [TM_Yuri_2 Boomer (0C5CF6AC)](all06umd-teams.md#team-0c5cf6ac).
12. Play voice notification EVA_BattlefieldControlOnline.
13. Enable and reset applicable timers for [_Setup_All06_Bio Load (0A23BA9C)](#trigger-0a23ba9c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6162, Events line 6239, Actions line 6316.

<a id="trigger-0a13e03c"></a>

### 27. Setpiece2_Obj2 Restate - 0A13E03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece2_Unlock Ready (0957813C)](#trigger-0957813c).

Attached scope: tag definitions 0A13D04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Destroy all of Yuri's structures” (MISSION:KillYuri).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6163, Events line 6240, Actions line 6317.

<a id="trigger-06c364ec"></a>

### 28. Conditions_Lose - 06C364EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece2_End (06C2AAFC)](#trigger-06c2aafc).

Attached scope: tag definitions 06C3640C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Player Loses (0BD7FB3C)](#trigger-0bd7fb3c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6164, Events line 6241, Actions line 6318.

<a id="trigger-07a07b8c"></a>

### 29. Detect_Yuri Facts Dead - 07A07B8C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece2_End (06C2AAFC)](#trigger-06c2aafc).

Attached scope: tag definitions 07A07AAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Enable and reset applicable timers for [All to Hunt_Yuri (07A0745C)](#trigger-07a0745c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6165, Events line 6242, Actions line 6319.

<a id="trigger-0a23ba9c"></a>

### 30. _Setup_All06_Bio Load - 0A23BA9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece2_End (06C2AAFC)](#trigger-06c2aafc).

Attached scope: tag definitions 0A23B9BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [TM_Yuri_Bio Load @ BO (0A23B29C)](all06umd-teams.md#team-0a23b29c).
2. Supply reinforcement team [TM_Yuri_Bio Load @ BP (07ABD1BC)](all06umd-teams.md#team-07abd1bc).
3. Supply reinforcement team [TM_Yuri_Bio Load @ BQ (0A23B16C)](all06umd-teams.md#team-0a23b16c).
4. Supply reinforcement team [TM_Yuri_Bio Load @ BR (0A23B03C)](all06umd-teams.md#team-0a23b03c).
5. Supply reinforcement team [TM_Yuri_Bio Load @ BR (0A23B03C)](all06umd-teams.md#team-0a23b03c).
6. Supply reinforcement team [TM_Yuri_Bio Load @ BS (0A23CB2C)](all06umd-teams.md#team-0a23cb2c).
7. Supply reinforcement team [TM_Yuri_1 Boomer Defense (09310EFC)](all06umd-teams.md#team-09310efc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6166, Events line 6243, Actions line 6320.

<a id="trigger-0bd7fb3c"></a>

### 31. Player Loses - 0BD7FB3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Conditions_Lose (06C364EC)](#trigger-06c364ec); enable from [Parliament Destroyed (048BB6BC)](#trigger-048bb6bc); enable from [Detect_Leader Dead (0883F63C)](#trigger-0883f63c).

Attached scope: tag definitions 0BD7E91C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the loser.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6167, Events line 6244, Actions line 6321.

<a id="trigger-07a0745c"></a>

### 32. All to Hunt_Yuri - 07A0745C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Detect_Yuri Facts Dead (07A07B8C)](#trigger-07a07b8c).

Attached scope: tag definitions 07A0737C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).
2. Enable and reset applicable timers for [Conditions_Win (06C3694C)](#trigger-06c3694c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6168, Events line 6245, Actions line 6322.

<a id="trigger-06c3694c"></a>

### 33. Conditions_Win - 06C3694C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [All to Hunt_Yuri (07A0745C)](#trigger-07a0745c).

Attached scope: tag definitions 06C365DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  Land: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Player Wins (0BD7E82C)](#trigger-0bd7e82c).
2. Make side cheer: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6169, Events line 6246, Actions line 6323.

<a id="trigger-0bd7e82c"></a>

### 34. Player Wins - 0BD7E82C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Conditions_Win (06C3694C)](#trigger-06c3694c).

Attached scope: tag definitions 0BD7E74C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 0 (country/type AMERICANS; placed owner Americans) the winner.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6170, Events line 6247, Actions line 6324.

<a id="trigger-09addb1c"></a>

### 35. Setpiece1_Unlock Ready - 09ADDB1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09ADA5EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Setpiece1_Unlock) is set.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Setpiece1_End (0BDAF1CC)](#trigger-0bdaf1cc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6171, Events line 6248, Actions line 6325.

<a id="trigger-0bdaf1cc"></a>

### 36. Setpiece1_End - 0BDAF1CC

Owner reference: Neutral. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Unlock Ready (09ADDB1C)](#trigger-09addb1c).

Attached scope: tag definitions 0BDABF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Defend Parliament from Assault.” (MISSION:All6Obj1).
2. Enable and reset applicable timers for [Yuri Taunt_Med (09B412EC)](#trigger-09b412ec).
3. Enable and reset applicable timers for [Warning_REYuri_Med (0BF330EC)](#trigger-0bf330ec).
4. Flash buildings of type CALOND04; duration argument 80.
5. Enable and reset applicable timers for [Setpiece1_Camera to Y (0713041C)](#trigger-0713041c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6172, Events line 6249, Actions line 6326.

<a id="trigger-09b412ec"></a>

### 37. Yuri Taunt_Med - 09B412EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_End (0BDAF1CC)](#trigger-0bdaf1cc); enable from [Setpiece1_Timer Med (08F6F03C)](#trigger-08f6f03c).

Attached scope: tag definitions 09B42D0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 860 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 25.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6173, Events line 6250, Actions line 6327.

<a id="trigger-0bf330ec"></a>

### 38. Warning_REYuri_Med - 0BF330EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_End (0BDAF1CC)](#trigger-0bdaf1cc); enable from [Setpiece1_Timer Med (08F6F03C)](#trigger-08f6f03c).

Attached scope: tag definitions 0BF3788C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1130 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA6_CarvilleGetReady.
2. Enable and reset applicable timers for [Yuri Wave Attack 1 (0BF31EFC)](#trigger-0bf31efc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6174, Events line 6251, Actions line 6328.

<a id="trigger-0713041c"></a>

### 39. Setpiece1_Camera to Y - 0713041C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_End (0BDAF1CC)](#trigger-0bdaf1cc).

Attached scope: tag definitions 0713033C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 24 (cell 90, 126) with speed setting 3.
2. Enable player input.
3. Play voice notification EVA_BattlefieldControlOnline.
4. Enable and reset applicable timers for [Setpiece1_Timer Easy (08F6803C)](#trigger-08f6803c).
5. Enable and reset applicable timers for [Setpiece1_Timer Med (08F6F03C)](#trigger-08f6f03c).
6. Enable and reset applicable timers for [Setpiece1_Timer Hard (08F6907C)](#trigger-08f6907c).
7. Enable and reset applicable timers for [For whom the bell tolls (091F07BC)](#trigger-091f07bc).
8. Enable and reset applicable timers for [5 Minute Tolls (091F283C)](#trigger-091f283c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6175, Events line 6252, Actions line 6329.

<a id="trigger-08f6803c"></a>

### 40. Setpiece1_Timer Easy - 08F6803C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Camera to Y (0713041C)](#trigger-0713041c).

Attached scope: tag definitions 08F6D04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 1500 configured time units.
2. Use countdown label “Yuri Forces Arriving In:” (MISSION:YuriTimer).
3. Start the visible mission timer.
4. Enable and reset applicable timers for [Yuri Taunt_Easy (091F220C)](#trigger-091f220c).
5. Enable and reset applicable timers for [Warning_RE Yuri_Easy (091F3D6C)](#trigger-091f3d6c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6176, Events line 6253, Actions line 6330.

<a id="trigger-08f6f03c"></a>

### 41. Setpiece1_Timer Med - 08F6F03C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Camera to Y (0713041C)](#trigger-0713041c).

Attached scope: tag definitions 08F6A04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 1200 configured time units.
2. Use countdown label “Yuri Forces Arriving In:” (MISSION:YuriTimer).
3. Start the visible mission timer.
4. Enable and reset applicable timers for [Yuri Taunt_Med (09B412EC)](#trigger-09b412ec).
5. Enable and reset applicable timers for [Warning_REYuri_Med (0BF330EC)](#trigger-0bf330ec).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6177, Events line 6254, Actions line 6331.

<a id="trigger-08f6907c"></a>

### 42. Setpiece1_Timer Hard - 08F6907C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Camera to Y (0713041C)](#trigger-0713041c).

Attached scope: tag definitions 08F6B08C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 900 configured time units.
2. Use countdown label “Yuri Forces Arriving In:” (MISSION:YuriTimer).
3. Start the visible mission timer.
4. Enable and reset applicable timers for [Yuri Taunt_Hard (091F3B9C)](#trigger-091f3b9c).
5. Enable and reset applicable timers for [Warning_RE Yuri_Hard (091F3F3C)](#trigger-091f3f3c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6178, Events line 6255, Actions line 6332.

<a id="trigger-091f07bc"></a>

### 43. For whom the bell tolls - 091F07BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Camera to Y (0713041C)](#trigger-0713041c); enable from [5 Minute Tolls (091F283C)](#trigger-091f283c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [For whom the bell tolls (091F07BC)](#trigger-091f07bc).
2. Play sound BigBenBell.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6179, Events line 6256, Actions line 6333.

<a id="trigger-091f283c"></a>

### 44. 5 Minute Tolls - 091F283C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [It tolls for thee (091F1E6C)](#trigger-091f1e6c).

Incoming activation links: enable from [Setpiece1_Camera to Y (0713041C)](#trigger-0713041c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [For whom the bell tolls (091F07BC)](#trigger-091f07bc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6180, Events line 6257, Actions line 6334.

<a id="trigger-091f220c"></a>

### 45. Yuri Taunt_Easy - 091F220C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Timer Easy (08F6803C)](#trigger-08f6803c).

Attached scope: tag definitions 091F212C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1260 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 25.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6181, Events line 6258, Actions line 6335.

<a id="trigger-091f3d6c"></a>

### 46. Warning_RE Yuri_Easy - 091F3D6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Timer Easy (08F6803C)](#trigger-08f6803c).

Attached scope: tag definitions 091F3C8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1430 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA6_CarvilleGetReady.
2. Enable and reset applicable timers for [Yuri Wave Attack 1 (0BF31EFC)](#trigger-0bf31efc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6182, Events line 6259, Actions line 6336.

<a id="trigger-091f3b9c"></a>

### 47. Yuri Taunt_Hard - 091F3B9C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Timer Hard (08F6907C)](#trigger-08f6907c).

Attached scope: tag definitions 091F3ABC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 560 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 25.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6183, Events line 6260, Actions line 6337.

<a id="trigger-091f3f3c"></a>

### 48. Warning_RE Yuri_Hard - 091F3F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Setpiece1_Timer Hard (08F6907C)](#trigger-08f6907c).

Attached scope: tag definitions 091F3E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 830 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_xA6_CarvilleGetReady.
2. Enable and reset applicable timers for [Yuri Wave Attack 1 (0BF31EFC)](#trigger-0bf31efc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6184, Events line 6261, Actions line 6338.

<a id="trigger-091f1e6c"></a>

### 49. It tolls for thee - 091F1E6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [For whom the bell tolls (091F07BC)](#trigger-091f07bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Disable [It tolls for thee (091F1E6C)](#trigger-091f1e6c).
2. Play sound BigBenBell.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6185, Events line 6262, Actions line 6339.

<a id="trigger-048bc46c"></a>

### 50. Parliament Attacked 1 - 048BC46C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Parliament Attacked 1 Delay (048BBB6C)](#trigger-048bbb6c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Play voice notification Mis_xA6_CarvilleBuildDefense.
2. Disable [Parliament Attacked 1 (048BC46C)](#trigger-048bc46c).
3. Enable and reset applicable timers for [Parliament Attacked 2 Delay (048BB98C)](#trigger-048bb98c).
4. Display message “Hint: Repair Parliament with an Engineer” (MISSION:ParlHint).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6186, Events line 6263, Actions line 6340.

<a id="trigger-048bb98c"></a>

### 51. Parliament Attacked 2 Delay - 048BB98C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Parliament Attacked 2 (048BBA7C)](#trigger-048bba7c).

Incoming activation links: enable from [Parliament Attacked 1 (048BC46C)](#trigger-048bc46c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Parliament Attacked 2 Delay (048BB98C)](#trigger-048bb98c).
2. Enable and reset applicable timers for [Parliament Attacked 2 (048BBA7C)](#trigger-048bba7c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6187, Events line 6264, Actions line 6341.

<a id="trigger-048bba7c"></a>

### 52. Parliament Attacked 2 - 048BBA7C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Parliament Attacked 1 Delay (048BBB6C)](#trigger-048bbb6c).

Incoming activation links: enable from [Parliament Attacked 2 Delay (048BB98C)](#trigger-048bb98c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Play voice notification Mis_xA6_CarvilleUnderAttack.
2. Disable [Parliament Attacked 2 (048BBA7C)](#trigger-048bba7c).
3. Enable and reset applicable timers for [Parliament Attacked 3 Delay (048BB7AC)](#trigger-048bb7ac).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6188, Events line 6265, Actions line 6342.

<a id="trigger-048bbb6c"></a>

### 53. Parliament Attacked 1 Delay - 048BBB6C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Parliament Attacked 1 (048BC46C)](#trigger-048bc46c).

Incoming activation links: enable from [Parliament Attacked 3 (048BB89C)](#trigger-048bb89c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Parliament Attacked 1 Delay (048BBB6C)](#trigger-048bbb6c).
2. Enable and reset applicable timers for [Parliament Attacked 1 (048BC46C)](#trigger-048bc46c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6189, Events line 6266, Actions line 6343.

<a id="trigger-048bb7ac"></a>

### 54. Parliament Attacked 3 Delay - 048BB7AC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Parliament Attacked 3 (048BB89C)](#trigger-048bb89c).

Incoming activation links: enable from [Parliament Attacked 2 (048BBA7C)](#trigger-048bba7c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Parliament Attacked 3 Delay (048BB7AC)](#trigger-048bb7ac).
2. Enable and reset applicable timers for [Parliament Attacked 3 (048BB89C)](#trigger-048bb89c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6190, Events line 6267, Actions line 6344.

<a id="trigger-048bb89c"></a>

### 55. Parliament Attacked 3 - 048BB89C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Parliament Attacked 2 Delay (048BB98C)](#trigger-048bb98c).

Incoming activation links: enable from [Parliament Attacked 3 Delay (048BB7AC)](#trigger-048bb7ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

**Then perform these actions in order:**

1. Disable [Parliament Attacked 3 (048BB89C)](#trigger-048bb89c).
2. Enable and reset applicable timers for [Parliament Attacked 1 Delay (048BBB6C)](#trigger-048bbb6c).
3. Play voice notification Mis_xA6_CarvilleProtectParl.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6191, Events line 6268, Actions line 6345.

<a id="trigger-048bb6bc"></a>

### 56. Parliament Destroyed - 048BB6BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Parliament Attacked 3 Delay (048BB7AC)](#trigger-048bb7ac).

Incoming activation links: enable from [Parliament @ 25% Health (077B8E1C)](#trigger-077b8e1c); enable from [Really Destroyed (08F91C4C)](#trigger-08f91c4c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Parliament Destroyed (048BB6BC)](#trigger-048bb6bc).
2. Disable [Parliament Attacked 1 (048BC46C)](#trigger-048bc46c).
3. Disable [Parliament Attacked 1 Delay (048BBB6C)](#trigger-048bbb6c).
4. Disable [Parliament Attacked 2 (048BBA7C)](#trigger-048bba7c).
5. Disable [Parliament Attacked 2 Delay (048BB98C)](#trigger-048bb98c).
6. Disable [Parliament Attacked 3 (048BB89C)](#trigger-048bb89c).
7. Disable [Parliament Attacked 3 Delay (048BB7AC)](#trigger-048bb7ac).
8. Play voice notification EVA_TechBuildingLost.
9. Display message “Critical Structure Lost” (MISSION:LostStct).
10. Enable and reset applicable timers for [Player Loses (0BD7FB3C)](#trigger-0bd7fb3c).
11. Do Explosion At; main setting 13; location/duration field W.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6192, Events line 6269, Actions line 6346.

<a id="trigger-07e4a1cc"></a>

### 57. _Amb_Birds Morning - 07E4A1CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E4CF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsMorning at waypoint 17 (cell 107, 120).
2. Play sound _Amb_BirdsMorning at waypoint 38 (cell 97, 125).
3. Play sound _Amb_BirdsMorning at waypoint 37 (cell 83, 134).
4. Play sound _Amb_BirdsMorning at waypoint 50 (cell 42, 96).
5. Play sound _Amb_BirdsMorning at waypoint 43 (cell 35, 89).
6. Play sound _Amb_BirdsMorning at waypoint 71 (cell 84, 69).
7. Play sound _Amb_BirdsMorning at waypoint 516 (cell 130, 78).
8. Play sound _Amb_BirdsMorning at waypoint 517 (cell 71, 78).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6193, Events line 6270, Actions line 6347.

<a id="trigger-07e4ce5c"></a>

### 58. _Amb_Cricket Chirps - 07E4CE5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E4CD7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_CricketChirps at waypoint 699 (cell 82, 124).
2. Play sound _Amb_CricketChirps at waypoint 36 (cell 74, 126).
3. Play sound _Amb_CricketChirps at waypoint 35 (cell 102, 118).
4. Play sound _Amb_CricketChirps at waypoint 20 (cell 111, 113).
5. Play sound _Amb_CricketChirps at waypoint 50 (cell 42, 96).
6. Play sound _Amb_CricketChirps at waypoint 508 (cell 26, 69).
7. Play sound _Amb_CricketBed at waypoint 509 (cell 19, 66).
8. Play sound _Amb_CricketChirps at waypoint 507 (cell 12, 61).
9. Play sound _Amb_CricketChirps at waypoint 505 (cell 29, 45).
10. Play sound _Amb_CricketChirps at waypoint 515 (cell 106, 73).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6194, Events line 6271, Actions line 6348.

<a id="trigger-07e4cc8c"></a>

### 59. _Amb_Wind Cold - 07E4CC8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E4CBAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 508 (cell 26, 69).
2. Play sound _Amb_WindCold at waypoint 509 (cell 19, 66).
3. Play sound _Amb_WindCold at waypoint 510 (cell 41, 43).
4. Play sound _Amb_WindCold at waypoint 511 (cell 91, 47).
5. Play sound _Amb_WindCold at waypoint 512 (cell 74, 55).
6. Play sound _Amb_WindCold at waypoint 513 (cell 54, 51).
7. Play sound _Amb_WindCold at waypoint 36 (cell 74, 126).
8. Play sound _Amb_WindCold at waypoint 24 (cell 90, 126).
9. Play sound _Amb_WindCold at waypoint 514 (cell 118, 62).
10. Play sound _Amb_WindCold at waypoint 515 (cell 106, 73).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6195, Events line 6272, Actions line 6349.

<a id="trigger-07e4cabc"></a>

### 60. _Amb_Urban Murmur 2b - 07E4CABC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E4C9DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur2 at waypoint 500 (cell 124, 83).
2. Play sound _Amb_UrbanMurmur2 at waypoint 501 (cell 118, 71).
3. Play sound _Amb_UrbanMurmur2 at waypoint 502 (cell 108, 59).
4. Play sound _Amb_UrbanMurmur2 at waypoint 503 (cell 102, 67).
5. Play sound _Amb_UrbanMurmur2 at waypoint 504 (cell 53, 58).
6. Play sound _Amb_UrbanMurmur2 at waypoint 505 (cell 29, 45).
7. Play sound _Amb_UrbanMurmur2 at waypoint 506 (cell 19, 54).
8. Play sound _Amb_UrbanMurmur2 at waypoint 507 (cell 12, 61).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6196, Events line 6273, Actions line 6350.

<a id="trigger-07e4c8ec"></a>

### 61. _Amb_Urban Murmur 2a - 07E4C8EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E4C80C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur2 at waypoint 48 (cell 111, 91).
2. Play sound _Amb_UrbanMurmur2 at waypoint 57 (cell 110, 84).
3. Play sound _Amb_UrbanMurmur2 at waypoint 47 (cell 85, 93).
4. Play sound _Amb_UrbanMurmur2 at waypoint 56 (cell 83, 86).
5. Play sound _Amb_UrbanMurmur2 at waypoint 52 (cell 65, 95).
6. Play sound _Amb_UrbanMurmur2 at waypoint 55 (cell 64, 86).
7. Play sound _Amb_UrbanMurmur2 at waypoint 44 (cell 61, 74).
8. Play sound _Amb_UrbanMurmur2 at waypoint 42 (cell 72, 67).
9. Play sound _Amb_UrbanMurmur2 at waypoint 71 (cell 84, 69).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6197, Events line 6274, Actions line 6351.

<a id="trigger-07e4c71c"></a>

### 62. _Amb_Waves Lake - 07E4C71C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E4C63C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WavesLake at waypoint 58 (cell 120, 103).
2. Play sound _Amb_WavesLake at waypoint 60 (cell 102, 104).
3. Play sound _Amb_WavesLake at waypoint 494 (cell 88, 101).
4. Play sound _Amb_WavesLake at waypoint 495 (cell 69, 100).
5. Play sound _Amb_WavesLake at waypoint 496 (cell 53, 96).
6. Play sound _Amb_WavesLake at waypoint 497 (cell 41, 71).
7. Play sound _Amb_WavesLake at waypoint 498 (cell 41, 57).
8. Play sound _Amb_WavesLake at waypoint 499 (cell 58, 21).
9. Play sound _Amb_WavesLake at waypoint 64 (cell 40, 30).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6198, Events line 6275, Actions line 6352.

<a id="trigger-07e4c54c"></a>

### 63. _Amb_Birds Harbor - 07E4C54C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07E4C46C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsHarbor at waypoint 58 (cell 120, 103).
2. Play sound _Amb_BirdsHarbor at waypoint 51 (cell 103, 100).
3. Play sound _Amb_BirdsHarbor at waypoint 45 (cell 43, 87).
4. Play sound _Amb_BirdsHarbor at waypoint 64 (cell 40, 30).
5. Play sound _Amb_BirdsHarbor at waypoint 494 (cell 88, 101).
6. Play sound _Amb_BirdsHarbor at waypoint 495 (cell 69, 100).
7. Play sound _Amb_BirdsHarbor at waypoint 496 (cell 53, 96).
8. Play sound _Amb_BirdsHarbor at waypoint 497 (cell 41, 71).
9. Play sound _Amb_BirdsHarbor at waypoint 498 (cell 41, 57).
10. Play sound _Amb_BirdsHarbor at waypoint 499 (cell 58, 21).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6199, Events line 6276, Actions line 6353.

<a id="trigger-0945978c"></a>

### 64. Parliament Attacked by Player - 0945978C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Parliament Destroyed (048BB6BC)](#trigger-048bb6bc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Disable [Parliament Attacked by Player (0945978C)](#trigger-0945978c).
2. Display message “WARNING - Critical structure. Do not destroy!!!” (MISSION:WarnStct).
3. Play sound WarningAlarm.
4. Flash buildings of type CALOND04; duration argument 100.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6200, Events line 6277, Actions line 6354.

<a id="trigger-0883f63c"></a>

### 65. Detect_Leader Dead - 0883F63C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0883F55C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “Critical Unit Lost” (MISSION:LostUnit).
2. Enable and reset applicable timers for [Player Loses (0BD7FB3C)](#trigger-0bd7fb3c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6201, Events line 6278, Actions line 6355.

<a id="trigger-0917f4bc"></a>

### 66. Amb_Lightning  - 0917F4BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0917EF1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 200 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Play sound WeatherStrike.

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6202, Events line 6279, Actions line 6356.

<a id="trigger-077b8e1c"></a>

### 67. Parliament @ 25% Health - 077B8E1C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Parliament Attacked by Player (0945978C)](#trigger-0945978c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Quarter health (any source). See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Parliament @ 25% Health (077B8E1C)](#trigger-077b8e1c).
2. Destroy the attached object through the scripted destruction action.
3. Enable and reset applicable timers for [Parliament Destroyed (048BB6BC)](#trigger-048bb6bc).
4. Jump the camera to waypoint 23 (cell 92, 115).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6203, Events line 6280, Actions line 6357.

<a id="trigger-077ec7ec"></a>

### 68. Intro_Master Mind - 077EC7EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 077EC70C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 14 (Master Mind Intro) is set.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 72 (cell 86, 74).
2. Jump the camera to waypoint 72 (cell 86, 74).
3. Play voice notification Unit_Eva_MasterMind.
4. Enable and reset applicable timers for [Intro_Master Mind_Ends (077E82CC)](#trigger-077e82cc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6204, Events line 6281, Actions line 6358.

<a id="trigger-077e82cc"></a>

### 69. Intro_Master Mind_Ends - 077E82CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Intro_Master Mind (077EC7EC)](#trigger-077ec7ec).

Attached scope: tag definitions 077E81EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [TM_Yuri_Master Mind (post intro) (077E857C)](all06umd-teams.md#team-077e857c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6205, Events line 6282, Actions line 6359.

<a id="trigger-08f91c4c"></a>

### 70. Really Destroyed - 08F91C4C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Parliament @ 25% Health (077B8E1C)](#trigger-077b8e1c).

Attached scope: British Parliament (CALOND04), owner Neutral, cell (91, 114), tag 048BC38C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Really Destroyed (08F91C4C)](#trigger-08f91c4c).
2. Enable and reset applicable timers for [Parliament Destroyed (048BB6BC)](#trigger-048bb6bc).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6206, Events line 6283, Actions line 6360.

<a id="trigger-091faf3c"></a>

### 71. Ben's Dead - 091FAF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [5 Minute Tolls (091F283C)](#trigger-091f283c).

Attached scope: Big Ben (CALOND05), owner Neutral, cell (88, 116), tag 091F06DC, persistence mode 2.

**Wait for the recorded events:**

1. No instances of Big Ben (CALOND05) exist on the map, under this event's ownership scope.

**Then perform these actions in order:**

1. Disable [For whom the bell tolls (091F07BC)](#trigger-091f07bc).
2. Disable [It tolls for thee (091F1E6C)](#trigger-091f1e6c).
3. Disable [5 Minute Tolls (091F283C)](#trigger-091f283c).
4. Disable [Ben's Dead (091FAF3C)](#trigger-091faf3c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6207, Events line 6284, Actions line 6361.

<a id="trigger-090f833c"></a>

### 72. Clean up_BK Trans TM - 090F833C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 090F825C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (Unloaded BK Team) is set.

Flag writers in this mission: clear local flag 9 (Unloaded BK Team) at [Clean up_BK Trans TM (090F833C)](#trigger-090f833c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 9 (Unloaded BK Team).
2. Create/recruit team [TM_Yuri_1 Hov @ BK (090FC12C)](all06umd-teams.md#team-090fc12c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6208, Events line 6285, Actions line 6362.

<a id="trigger-090f816c"></a>

### 73. Clean up_BL Trans TM - 090F816C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 090FC35C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 10 (Unloaded BL Team) is set.

Flag writers in this mission: clear local flag 10 (Unloaded BL Team) at [Clean up_BL Trans TM (090F816C)](#trigger-090f816c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 10 (Unloaded BL Team).
2. Create/recruit team [TM_Yuri_1 Hov @ BL (0910455C)](all06umd-teams.md#team-0910455c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6209, Events line 6286, Actions line 6363.

<a id="trigger-05c6397c"></a>

### 74. Wave Attack Prod - 05C6397C

Owner reference: YuriCountry. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Wave Attack 4b (05C6450C)](#trigger-05c6450c).

Attached scope: tag definitions 05C6389C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. All to Hunt: owner selector 9 (country/type YURICOUNTRY; placed owner YuriCountry).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6210, Events line 6287, Actions line 6364.

<a id="trigger-05c6450c"></a>

### 75. Yuri Wave Attack 4b - 05C6450C

Owner reference: <none>. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Yuri Wave Attack 4 (095EB2AC)](#trigger-095eb2ac).

Attached scope: tag definitions 05C6442C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Wave Attack Prod (05C6397C)](#trigger-05c6397c).

Source locator: mapsmd03.mix/all06umd.map; Triggers line 6211, Events line 6288, Actions line 6365.

[All team rosters and ordered plans](all06umd-teams.md) | [All mission overrides](all06umd-overrides.md)
