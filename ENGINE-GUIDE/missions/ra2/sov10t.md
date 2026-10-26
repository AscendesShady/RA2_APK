# Operation: Weathered Alliance

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for sov10t.map.](../../images/map-sov10t.svg)

*Initial placement schematic for sov10t.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** sov10t.map. **Effective extracted member:** MAPS02.MIX/sov10t.map. **Trigger definitions:** 59.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov10t-teams.md) | [All mission overrides](sov10t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | TEMPERATE |
| Map size | 0,0,87,144 |
| Visible local rectangle | 10,41,75,97 |
| Placed vehicles | 26 |
| Placed infantry | 35 |
| Placed structures | 200 |
| Placed aircraft | 0 |
| Team templates | 35 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 150 | Player |
| 1 | BadGuy1 House | 1000 | BadGuy1 |
| 2 | BadGuy2 House | 1000 | BadGuy2 |
| 3 | BadGuy3 House | 1000 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 20 | Other1 |
| 6 | Other2 House | 20 | Other2 |
| 7 | Other3 House | 20 | Other3 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Gen1 Destroyed,0 |
| 1 | Gen2 Destroyed,0 |
| 2 | Gen3 Destroyed,0 |
| 3 | Generator Advice,0 |
| 4 | WCD Power On,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Winner (09AB6CC0)](#trigger-09ab6cc0) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [Loser (09AB6F60)](#trigger-09ab6f60) | 3 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-07facf60"></a>

### 1. West Trans Arrives - 07FACF60

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FAFB50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [West Trans (0AF67A4C)](sov10t-teams.md#team-0af67a4c).
2. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5639, Events line 5700, Actions line 5761.

<a id="trigger-07b72cc0"></a>

### 2. East Trans Arrives - 07B72CC0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B72C10 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [East Trans (09ED3A4C)](sov10t-teams.md#team-09ed3a4c).
2. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Reveal terrain around waypoint 36 (cell 179, 176).
4. Reveal terrain around waypoint 37 (cell 141, 170).
5. Reveal terrain around waypoint 18 (cell 140, 123).
6. Reveal terrain around waypoint 17 (cell 157, 123).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5640, Events line 5701, Actions line 5762.

<a id="trigger-07237530"></a>

### 3. Unlock Input - 07237530

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07237270 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Disable [Unlock Input (07237530)](#trigger-07237530).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5641, Events line 5702, Actions line 5763.

<a id="trigger-07237120"></a>

### 4. Lock Input - 07237120

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07231C50 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable player input.
2. Disable [Lock Input (07237120)](#trigger-07237120).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5642, Events line 5703, Actions line 5764.

<a id="trigger-09f40250"></a>

### 5. Allied 1 Counter Attack - 09F40250

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG3 Attacked (09DE1140)](#trigger-09de1140).

Attached scope: Aegis Cruiser (AEGIS), owner BadGuy1 House, cell (153, 130), tag 09F42D90, persistence mode 0; Destroyer (DEST), owner BadGuy1 House, cell (155, 131), tag 09F42D90, persistence mode 0; Dolphin (DLPH), owner BadGuy1 House, cell (150, 127), tag 09F42D90, persistence mode 0; Destroyer (DEST), owner BadGuy1 House, cell (158, 132), tag 09F42D90, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (156, 116), tag 09F42D90, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (154, 116), tag 09F42D90, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (154, 117), tag 09F42D90, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy1 House, cell (153, 118), tag 09F42D90, persistence mode 0; Aircraft Carrier (CARRIER), owner BadGuy1 House, cell (160, 130), tag 09F42D90, persistence mode 0; Chrono Miner (CMIN), owner BadGuy1 House, cell (161, 121), tag 09F42D90, persistence mode 0; GI (E1), owner BadGuy1 House, cell (145, 121), tag 09F42D90, persistence mode 0; GI (E1), owner BadGuy1 House, cell (147, 122), tag 09F42D90, persistence mode 0; GI (E1), owner BadGuy1 House, cell (147, 124), tag 09F42D90, persistence mode 0; GI (E1), owner BadGuy1 House, cell (146, 122), tag 09F42D90, persistence mode 0; GI (E1), owner BadGuy1 House, cell (153, 122), tag 09F42D90, persistence mode 0; Allied Ore Refinery (GAREFN), owner BadGuy1 House, cell (160, 118), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (184, 111), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (188, 116), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (182, 107), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (178, 112), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (178, 108), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (173, 123), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (176, 123), tag 09F42D90, persistence mode 0; Prism Tower (ATESLA), owner BadGuy1 House, cell (177, 110), tag 09F42D90, persistence mode 0; Prism Tower (ATESLA), owner BadGuy1 House, cell (188, 112), tag 09F42D90, persistence mode 0; Patriot Missile (NASAM), owner BadGuy1 House, cell (175, 139), tag 09F42D90, persistence mode 0; Patriot Missile (NASAM), owner BadGuy1 House, cell (179, 127), tag 09F42D90, persistence mode 0; Patriot Missile (NASAM), owner BadGuy1 House, cell (176, 103), tag 09F42D90, persistence mode 0; Patriot Missile (NASAM), owner BadGuy1 House, cell (167, 97), tag 09F42D90, persistence mode 0; Patriot Missile (NASAM), owner BadGuy1 House, cell (161, 97), tag 09F42D90, persistence mode 0; Patriot Missile (NASAM), owner BadGuy1 House, cell (167, 129), tag 09F42D90, persistence mode 0; Patriot Missile (NASAM), owner BadGuy1 House, cell (140, 124), tag 09F42D90, persistence mode 0; Patriot Missile (NASAM), owner BadGuy1 House, cell (151, 101), tag 09F42D90, persistence mode 0; Prism Tower (ATESLA), owner BadGuy1 House, cell (142, 120), tag 09F42D90, persistence mode 0; Prism Tower (ATESLA), owner BadGuy1 House, cell (156, 122), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (160, 111), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (163, 111), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (160, 115), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (163, 115), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (170, 109), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (170, 113), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (167, 101), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (167, 104), tag 09F42D90, persistence mode 0; Allied Barracks (GAPILE), owner BadGuy1 House, cell (159, 107), tag 09F42D90, persistence mode 0; Prism Tower (ATESLA), owner BadGuy1 House, cell (159, 105), tag 09F42D90, persistence mode 0; Prism Tower (ATESLA), owner BadGuy1 House, cell (163, 101), tag 09F42D90, persistence mode 0; Prism Tower (ATESLA), owner BadGuy1 House, cell (178, 119), tag 09F42D90, persistence mode 0; Patriot Missile (NASAM), owner BadGuy1 House, cell (175, 115), tag 09F42D90, persistence mode 0; Allied Construction Yard (GACNST), owner BadGuy1 House, cell (171, 116), tag 09F42D90, persistence mode 0; Allied Barracks (GAPILE), owner BadGuy1 House, cell (172, 102), tag 09F42D90, persistence mode 0; Allied Shipyard (GAYARD), owner BadGuy1 House, cell (156, 127), tag 09F42D90, persistence mode 0; Allied Shipyard (GAYARD), owner BadGuy1 House, cell (183, 127), tag 09F42D90, persistence mode 0; Air Force Command Headquarters (GAAIRC), owner BadGuy1 House, cell (160, 102), tag 09F42D90, persistence mode 0; Allied War Factory (GAWEAP), owner BadGuy1 House, cell (146, 104), tag 09F42D90, persistence mode 0; Power Plant (GAPOWR), owner BadGuy1 House, cell (155, 106), tag 09F42D90, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (158, 112), tag 09F42D90, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (157, 107), tag 09F42D90, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (164, 107), tag 09F42D90, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (170, 104), tag 09F42D90, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (168, 114), tag 09F42D90, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (145, 123), tag 09F42D90, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (149, 123), tag 09F42D90, persistence mode 0; Pill Box (GAPILL), owner BadGuy1 House, cell (151, 122), tag 09F42D90, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. Create/recruit team [Grizzly 4 Tank Defense (07A6EF0C)](sov10t-teams.md#team-07a6ef0c).
3. Create/recruit team [BG 1 Naval Team (07A6EA6C)](sov10t-teams.md#team-07a6ea6c).
4. Ratio of team infantry; main setting 50.
5. Enable and reset applicable timers for [BG2 Delayed Startup (04371B8C)](#trigger-04371b8c).
6. Create/recruit team [BG 1 Naval Team (07A6EA6C)](sov10t-teams.md#team-07a6ea6c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5643, Events line 5704, Actions line 5765.

<a id="trigger-04371b8c"></a>

### 6. BG2 Delayed Startup - 04371B8C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Allied 1 Counter Attack (09F40250)](#trigger-09f40250).

Attached scope: tag definitions 043713BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
2. AI triggers begin: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5644, Events line 5705, Actions line 5766.

<a id="trigger-08970880"></a>

### 7. Allied 2 Counter Attack - 08970880

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG3 Attacked (09DE1140)](#trigger-09de1140).

Attached scope: Chrono Miner (CMIN), owner BadGuy2 House, cell (94, 145), tag 08970390, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy2 House, cell (95, 129), tag 08970390, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy2 House, cell (99, 131), tag 08970390, persistence mode 0; Grizzly Battle Tank (MTNK), owner BadGuy2 House, cell (96, 127), tag 08970390, persistence mode 0; GI (E1), owner BadGuy2 House, cell (101, 137), tag 08970390, persistence mode 0; GI (E1), owner BadGuy2 House, cell (101, 136), tag 08970390, persistence mode 0; GI (E1), owner BadGuy2 House, cell (102, 137), tag 08970390, persistence mode 0; GI (E1), owner BadGuy2 House, cell (92, 137), tag 08970390, persistence mode 0; Allied Construction Yard (GACNST), owner BadGuy2 House, cell (87, 135), tag 08970390, persistence mode 0; Allied Barracks (GAPILE), owner BadGuy2 House, cell (96, 136), tag 08970390, persistence mode 0; Allied Ore Refinery (GAREFN), owner BadGuy2 House, cell (91, 144), tag 08970390, persistence mode 0; Allied War Factory (GAWEAP), owner BadGuy2 House, cell (87, 129), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (106, 154), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (104, 158), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (100, 159), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (96, 161), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (105, 140), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (104, 144), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (88, 151), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (92, 151), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (81, 140), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (85, 132), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (94, 123), tag 08970390, persistence mode 0; Patriot Missile (NASAM), owner BadGuy2 House, cell (110, 119), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (92, 140), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (86, 140), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (92, 134), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (92, 126), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (99, 136), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (104, 136), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (98, 121), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (106, 121), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (81, 136), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (125, 136), tag 08970390, persistence mode 0; Prism Tower (ATESLA), owner BadGuy2 House, cell (100, 147), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (104, 155), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (107, 152), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (103, 146), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (103, 141), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (101, 157), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (97, 159), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (89, 150), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (89, 143), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (83, 141), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (83, 132), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (89, 146), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (94, 162), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (93, 158), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (104, 149), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (91, 124), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (85, 130), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (104, 137), tag 08970390, persistence mode 0; Power Plant (GAPOWR), owner BadGuy2 House, cell (91, 154), tag 08970390, persistence mode 0; Air Force Command Headquarters (GAAIRC), owner BadGuy2 House, cell (82, 135), tag 08970390, persistence mode 0; Air Force Command Headquarters (GAAIRC), owner BadGuy2 House, cell (80, 137), tag 08970390, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
2. Production Begins: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
3. Ratio of team aircraft; main setting 50.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5645, Events line 5706, Actions line 5767.

<a id="trigger-0b7bea70"></a>

### 8. Zofia 5 - 0B7BEA70

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WCD_Attack_fake (0B16B91C)](#trigger-0b16b91c).

Attached scope: tag definitions 0B7BE890 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 45 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).
2. Production Begins: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).
3. Set local flag 4 (WCD Power On).
4. Create/recruit team [BG3 Aegis Attack Team (09E8068C)](sov10t-teams.md#team-09e8068c).
5. Create/recruit team [BG3 Carrier Attack Team (09E80B5C)](sov10t-teams.md#team-09e80b5c).
6. Create/recruit team [BG3 Destroyer Attack Team (09914EFC)](sov10t-teams.md#team-09914efc).
7. Create/recruit team [BG3 Dolphin Attack Team (0AF0DC8C)](sov10t-teams.md#team-0af0dc8c).
8. Create/recruit team [BG3 Intruder Defense (0A93F57C)](sov10t-teams.md#team-0a93f57c).
9. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5646, Events line 5707, Actions line 5768.

<a id="trigger-0b7bd050"></a>

### 9. Zofia 4 - 0B7BD050

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BL Captured (07C0419C)](#trigger-07c0419c).

Attached scope: tag definitions 0B7BEB30 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S10_Sofia4.
2. Enable and reset applicable timers for [Camera to WCD (0C6043EC)](#trigger-0c6043ec).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5647, Events line 5708, Actions line 5769.

<a id="trigger-0c6043ec"></a>

### 10. Camera to WCD - 0C6043EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Zofia 4 (0B7BD050)](#trigger-0b7bd050); enable from [BL Captured (07C0419C)](#trigger-07c0419c).

Attached scope: tag definitions 0C604F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 15 (cell 18, 96).
2. Play sound CameraSwitch.
3. Enable and reset applicable timers for [WCD_Timer_fake (0B16933C)](#trigger-0b16933c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5648, Events line 5709, Actions line 5770.

<a id="trigger-0b16933c"></a>

### 11. WCD_Timer_fake - 0B16933C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Camera to WCD (0C6043EC)](#trigger-0c6043ec).

Attached scope: tag definitions 0B16BA0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set the mission timer to 300 configured time units.
2. Use countdown label “Weather Storm” (Name:Storm).
3. Enable and reset applicable timers for [Weather Control Device (087F44BC)](#trigger-087f44bc).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5649, Events line 5710, Actions line 5771.

<a id="trigger-087f44bc"></a>

### 12. Weather Control Device - 087F44BC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WCD_Timer_fake (0B16933C)](#trigger-0b16933c).

Attached scope: tag definitions 087F799C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 275 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 117.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5650, Events line 5711, Actions line 5772.

<a id="trigger-0b7bd7a0"></a>

### 13. Zofia 3 - 0B7BD7A0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Zofia 2 (089668E0)](#trigger-089668e0).

Attached scope: tag definitions 0B7BD110 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 9 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S10_Sofia3.
2. Enable and reset applicable timers for [Zofia 3 Online (081FCDBC)](#trigger-081fcdbc).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5651, Events line 5712, Actions line 5773.

<a id="trigger-081fcdbc"></a>

### 14. Zofia 3 Online - 081FCDBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Zofia 3 (0B7BD7A0)](#trigger-0b7bd7a0).

Attached scope: tag definitions 081F9F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 18 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5652, Events line 5713, Actions line 5774.

<a id="trigger-0ab36980"></a>

### 15. 1 Landing Craft_5 GIs - 0AB36980

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AB37BD0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Harassment Team (0AA33A3C)](sov10t-teams.md#team-0aa33a3c).
2. Enable and reset applicable timers for [Landing Craft_5 GIs Again (0A7961EC)](#trigger-0a7961ec).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5653, Events line 5714, Actions line 5775.

<a id="trigger-0a7961ec"></a>

### 16. Landing Craft_5 GIs Again - 0A7961EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1 Landing Craft_5 GIs (0AB36980)](#trigger-0ab36980).

Attached scope: tag definitions 0A791BFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Harassment Team_2 (0DCFF25C)](sov10t-teams.md#team-0dcff25c).
2. Enable and reset applicable timers for [2 Landing Craft_2 Tanks (0A791B0C)](#trigger-0a791b0c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5654, Events line 5715, Actions line 5776.

<a id="trigger-0a791b0c"></a>

### 17. 2 Landing Craft_2 Tanks - 0A791B0C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Landing Craft_5 GIs Again (0A7961EC)](#trigger-0a7961ec).

Attached scope: tag definitions 0A791A2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Harassment Team_3 (0CEEC74C)](sov10t-teams.md#team-0ceec74c).
2. Supply reinforcement team [Harassment Team_3a (0CEEC29C)](sov10t-teams.md#team-0ceec29c).
3. Enable and reset applicable timers for [4 Rocketeers (0A79193C)](#trigger-0a79193c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5655, Events line 5716, Actions line 5777.

<a id="trigger-0a79193c"></a>

### 18. 4 Rocketeers - 0A79193C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [2 Landing Craft_2 Tanks (0A791B0C)](#trigger-0a791b0c).

Attached scope: tag definitions 0A79185C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Harassment Team_4 (0863D33C)](sov10t-teams.md#team-0863d33c).
2. Enable and reset applicable timers for [4 Intruders (0A79163C)](#trigger-0a79163c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5656, Events line 5717, Actions line 5778.

<a id="trigger-0a79163c"></a>

### 19. 4 Intruders - 0A79163C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [4 Rocketeers (0A79193C)](#trigger-0a79193c).

Attached scope: tag definitions 0A79155C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Harassment Team_5 (0A796E3C)](sov10t-teams.md#team-0a796e3c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5657, Events line 5718, Actions line 5779.

<a id="trigger-0961d700"></a>

### 20. Bonus Ship - 0961D700

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Dreadnought (DRED), owner Civie1 House, cell (150, 205), tag 0961D290, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Reveal terrain around waypoint 11 (cell 149, 205).
3. Play sound Bonus.
4. Create radar-event marker type 0 at waypoint 11 (cell 149, 205).
5. Play sound GenSovWaterSelect.
6. Create/recruit team [Beach Panic People (0B7CA57C)](sov10t-teams.md#team-0b7ca57c).
7. Play sound CivAllFear.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5658, Events line 5719, Actions line 5780.

<a id="trigger-09ab4d30"></a>

### 21. WCD Destroyed - 09AB4D30

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [WCD Captured (09AB47E0)](#trigger-09ab47e0).

Attached scope: Weather Controller (GAWEAT), owner Other3 House, cell (17, 95), tag 09030F4C, persistence mode 2.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Winner (09AB6CC0)](#trigger-09ab6cc0).
2. Disable [Reminder2_Nuke BL (0A9F7180)](#trigger-0a9f7180).
3. Display message “Objective 2 Complete” (MISSION:Objective2).
4. Disable [WCD Destroyed (09AB4D30)](#trigger-09ab4d30).
5. Enable and reset applicable timers for [Cheer (0A5DD21C)](#trigger-0a5dd21c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5659, Events line 5720, Actions line 5781.

<a id="trigger-09ab47e0"></a>

### 22. WCD Captured - 09AB47E0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Turn On (07537BBC)](#trigger-07537bbc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Winner Bonus (09B23E90)](#trigger-09b23e90).
2. Disable [Reminder2_Nuke BL (0A9F7180)](#trigger-0a9f7180).
3. Display message “Objective 2 Complete” (MISSION:Objective2).
4. Disable [WCD Captured (09AB47E0)](#trigger-09ab47e0).
5. Enable and reset applicable timers for [Cheer (0A5DD21C)](#trigger-0a5dd21c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5660, Events line 5721, Actions line 5782.

<a id="trigger-09ab6cc0"></a>

### 23. Winner - 09AB6CC0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WCD Destroyed (09AB4D30)](#trigger-09ab4d30); enable from [Winner Bonus (09B23E90)](#trigger-09b23e90).

Attached scope: tag definitions 09B21420 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5661, Events line 5722, Actions line 5783.

<a id="trigger-0a9f7180"></a>

### 24. Reminder2_Nuke BL - 0A9F7180

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BL Captured (07C0419C)](#trigger-07c0419c).

Attached scope: tag definitions 0AA060D0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy the Weather Control Device” (MISSION:Sov10c).
2. Create radar-event marker type 5 at waypoint 15 (cell 18, 96).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5662, Events line 5723, Actions line 5784.

<a id="trigger-0a5dd21c"></a>

### 25. Cheer - 0A5DD21C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WCD Destroyed (09AB4D30)](#trigger-09ab4d30); enable from [WCD Captured (09AB47E0)](#trigger-09ab47e0).

Attached scope: tag definitions 0A5DD13C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5663, Events line 5724, Actions line 5785.

<a id="trigger-07537bbc"></a>

### 26. Turn On - 07537BBC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 4 (WCD Power On) is set.

Flag writers in this mission: set local flag 4 (WCD Power On) at [Zofia 5 (0B7BEA70)](#trigger-0b7bea70); set local flag 4 (WCD Power On) at [WCD_Enabled_real (0B17417C)](#trigger-0b17417c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Change House: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).
2. Disable [Turn On (07537BBC)](#trigger-07537bbc).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5664, Events line 5725, Actions line 5786.

<a id="trigger-09b23e90"></a>

### 27. Winner Bonus - 09B23E90

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WCD Captured (09AB47E0)](#trigger-09ab47e0).

Attached scope: tag definitions 09B211A0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set global flag 7.
2. Enable and reset applicable timers for [Winner (09AB6CC0)](#trigger-09ab6cc0).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5665, Events line 5726, Actions line 5787.

<a id="trigger-09ab41e0"></a>

### 28. Player Dead - 09AB41E0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09AB4050 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Loser (09AB6F60)](#trigger-09ab6f60).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5666, Events line 5727, Actions line 5788.

<a id="trigger-09ab6f60"></a>

### 29. Loser - 09AB6F60

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Dead (09AB41E0)](#trigger-09ab41e0); enable from [BL Destroyed (07C053EC)](#trigger-07c053ec); enable from [_Lose Condition (0B3FB3FC)](#trigger-0b3fb3fc).

Attached scope: tag definitions 09AB6D80 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5667, Events line 5728, Actions line 5789.

<a id="trigger-08991690"></a>

### 30. Bad Guy 3 Startup - 08991690

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089900C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. House Discovered; configured argument 16.

**Then perform these actions in order:**

1. Production Begins: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).
2. AI triggers begin: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).
3. Create/recruit team [BG3 Aegis Attack Team (09E8068C)](sov10t-teams.md#team-09e8068c).
4. Create/recruit team [BG3 Carrier Attack Team (09E80B5C)](sov10t-teams.md#team-09e80b5c).
5. Create/recruit team [BG3 Destroyer Attack Team (09914EFC)](sov10t-teams.md#team-09914efc).
6. Create/recruit team [BG3 Dolphin Attack Team (0AF0DC8C)](sov10t-teams.md#team-0af0dc8c).
7. Create/recruit team [BG3 GI Defense (08E366DC)](sov10t-teams.md#team-08e366dc).
8. Create/recruit team [BG3 Grizzly Tank Def (08E367FC)](sov10t-teams.md#team-08e367fc).
9. Create/recruit team [BG3 Intruder Defense (0A93F57C)](sov10t-teams.md#team-0a93f57c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5668, Events line 5729, Actions line 5790.

<a id="trigger-07ef4200"></a>

### 31. Reveal LZ - 07EF4200

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07EF57D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 0 (cell 155, 161).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5669, Events line 5730, Actions line 5791.

<a id="trigger-07490670"></a>

### 32. Faster Unlock Input - 07490670

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Landed (09CC8F3C)](#trigger-09cc8f3c).

Attached scope: tag definitions 074951F0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable player input.
2. Disable [Faster Unlock Input (07490670)](#trigger-07490670).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5670, Events line 5731, Actions line 5792.

<a id="trigger-09de1140"></a>

### 33. BG3 Attacked - 09DE1140

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09DE2D70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Allied 1 Counter Attack (09F40250)](#trigger-09f40250).
2. Enable and reset applicable timers for [Allied 2 Counter Attack (08970880)](#trigger-08970880).
3. AI triggers begin: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).
4. Production Begins: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5671, Events line 5732, Actions line 5793.

<a id="trigger-08964a60"></a>

### 34. Zofia 1 - 08964A60

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089669A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play voice notification Mis_S10_Sofia1.
2. Enable and reset applicable timers for [Zofia 2 (089668E0)](#trigger-089668e0).
3. Enable and reset applicable timers for [Zofia 1 Map (0AFE7F3C)](#trigger-0afe7f3c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5672, Events line 5733, Actions line 5794.

<a id="trigger-089668e0"></a>

### 35. Zofia 2 - 089668E0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Zofia 1 (08964A60)](#trigger-08964a60).

Attached scope: tag definitions 089667A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 22 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S10_Sofia2.
2. Create radar-event marker type 5 at waypoint 2 (cell 148, 128).
3. Reveal terrain around waypoint 2 (cell 148, 128).
4. Enable and reset applicable timers for [Zofia 3 (0B7BD7A0)](#trigger-0b7bd7a0).
5. Enable and reset applicable timers for [Zofia 2 Map (0AFE751C)](#trigger-0afe751c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5673, Events line 5734, Actions line 5795.

<a id="trigger-0afe7f3c"></a>

### 36. Zofia 1 Map - 0AFE7F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Zofia 1 (08964A60)](#trigger-08964a60).

Attached scope: tag definitions 0AFE7E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Zofia 1 Map Return (0AFE734C)](#trigger-0afe734c).
2. Jump the camera to waypoint 40 (cell 164, 98).
3. Reveal terrain around waypoint 40 (cell 164, 98).
4. Create radar-event marker type 5 at waypoint 40 (cell 164, 98).
5. Play sound CameraSwitch.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5674, Events line 5735, Actions line 5796.

<a id="trigger-0afe751c"></a>

### 37. Zofia 2 Map - 0AFE751C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Zofia 2 (089668E0)](#trigger-089668e0).

Attached scope: tag definitions 0AFE743C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Zofia 2 Map Return (0AFE717C)](#trigger-0afe717c).
2. Jump the camera to waypoint 2 (cell 148, 128).
3. Play sound CameraSwitch.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5675, Events line 5736, Actions line 5797.

<a id="trigger-0afe734c"></a>

### 38. Zofia 1 Map Return - 0AFE734C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Zofia 1 Map (0AFE7F3C)](#trigger-0afe7f3c).

Attached scope: tag definitions 0AFE726C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 42 (cell 158, 175).
2. Play sound CameraSwitch.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5676, Events line 5737, Actions line 5798.

<a id="trigger-0afe717c"></a>

### 39. Zofia 2 Map Return - 0AFE717C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Zofia 2 Map (0AFE751C)](#trigger-0afe751c).

Attached scope: tag definitions 0AFE709C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 17 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 4 (cell 148, 176).
2. Play sound CameraSwitch.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5677, Events line 5738, Actions line 5799.

<a id="trigger-07c0471c"></a>

### 40. BL Damaged - 07C0471C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “MISSION CRITICAL STRUCTURE - Do not destroy!” (MISSION:Sov10d).
2. Disable [BL Damaged (07C0471C)](#trigger-07c0471c).
3. Play sound NukeSiren.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5678, Events line 5739, Actions line 5800.

<a id="trigger-07c053ec"></a>

### 41. BL Destroyed - 07C053EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BL Damaged (07C0471C)](#trigger-07c0471c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [BL Destroyed (07C053EC)](#trigger-07c053ec).
2. Enable and reset applicable timers for [Loser (09AB6F60)](#trigger-09ab6f60).
3. Disable [BL Captured (07C0419C)](#trigger-07c0419c).
4. Disable [BL Damaged (07C0471C)](#trigger-07c0471c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5679, Events line 5740, Actions line 5801.

<a id="trigger-07c0419c"></a>

### 42. BL Captured - 07C0419C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [BL Destroyed (07C053EC)](#trigger-07c053ec).

Attached scope: Allied Battle Lab (GATECH), owner BadGuy1 House, cell (163, 97), tag 07C0463C, persistence mode 2.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 15 (cell 18, 96).
2. Enable and reset applicable timers for [Zofia 4 (0B7BD050)](#trigger-0b7bd050).
3. Resize Player View; main setting 0; parameter 1: 1, parameter 2: 7, parameter 3: 84, parameter 4: 131.
4. Reveal terrain around waypoint 15 (cell 18, 96).
5. Disable [BL Captured (07C0419C)](#trigger-07c0419c).
6. Disable [BL Destroyed (07C053EC)](#trigger-07c053ec).
7. Disable [BL Damaged (07C0471C)](#trigger-07c0471c).
8. Disable [Reminder1_Capture BL (0B58F3DC)](#trigger-0b58f3dc).
9. Display message “Objective 1 Complete” (MISSION:Objective1).
10. Enable and reset applicable timers for [Camera to WCD (0C6043EC)](#trigger-0c6043ec).
11. Enable and reset applicable timers for [Reminder2_Nuke BL (0A9F7180)](#trigger-0a9f7180).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5680, Events line 5741, Actions line 5802.

<a id="trigger-0b58f3dc"></a>

### 43. Reminder1_Capture BL - 0B58F3DC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Landed (09CC8F3C)](#trigger-09cc8f3c).

Attached scope: tag definitions 0A66455C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Capture the BATTLE LAB with an ENGINEER” (MISSION:Sov10a).
2. Create radar-event marker type 5 at waypoint 40 (cell 164, 98).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5681, Events line 5742, Actions line 5803.

<a id="trigger-09cc8f3c"></a>

### 44. Landed - 09CC8F3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 13 tagged map cells: (144, 174), (145, 174), (146, 174), (144, 175), (145, 175), (146, 175), (147, 175), (144, 176), (145, 176), (146, 176), (147, 176), (145, 177), (146, 177); tag 09CC83EC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Faster Unlock Input (07490670)](#trigger-07490670).
2. Enable and reset applicable timers for [Reminder1_Capture BL (0B58F3DC)](#trigger-0b58f3dc).
3. Enable and reset applicable timers for [Objective 1 (0830720C)](#trigger-0830720c).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5682, Events line 5743, Actions line 5804.

<a id="trigger-0830720c"></a>

### 45. Objective 1 - 0830720C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Landed (09CC8F3C)](#trigger-09cc8f3c).

Attached scope: tag definitions 0830F05C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Capture the BATTLE LAB with an ENGINEER” (MISSION:Sov10a).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5683, Events line 5744, Actions line 5805.

<a id="trigger-07d50bcc"></a>

### 46. BG1 Delayed Startup - 07D50BCC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07D5060C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5684, Events line 5745, Actions line 5806.

<a id="trigger-098b815c"></a>

### 47. Camera Move 1 - 098B815C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 098BCCFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Move the camera to waypoint 41 (cell 172, 179) with speed setting 2.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5685, Events line 5746, Actions line 5807.

<a id="trigger-0bce5aac"></a>

### 48. Ocean Heavy - 0BCE5AAC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 51 (cell 137, 202).
2. Play sound _Amb_OceanHeavy at waypoint 11 (cell 149, 205).
3. Play sound _Amb_OceanHeavy at waypoint 44 (cell 125, 177).
4. Play sound _Amb_OceanHeavy at waypoint 43 (cell 148, 183).
5. Play sound _Amb_OceanHeavy at waypoint 42 (cell 158, 175).
6. Play sound _Amb_OceanHeavy at waypoint 29 (cell 165, 180).
7. Play sound _Amb_OceanHeavy at waypoint 36 (cell 179, 176).
8. Play sound _Amb_OceanHeavy at waypoint 45 (cell 121, 160).
9. Play sound _Amb_OceanHeavy at waypoint 46 (cell 128, 151).
10. Play sound _Amb_OceanHeavy at waypoint 35 (cell 136, 159).
11. Play sound _Amb_OceanHeavy at waypoint 62 (cell 184, 154).
12. Play sound _Amb_OceanHeavy at waypoint 61 (cell 198, 159).
13. Play sound _Amb_OceanHeavy at waypoint 60 (cell 201, 145).
14. Play sound _Amb_OceanHeavy at waypoint 10 (cell 149, 131).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5686, Events line 5747, Actions line 5808.

<a id="trigger-0bce57ac"></a>

### 49. Ambient Birds - 0BCE57AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ocean Heavy (0BCE5AAC)](#trigger-0bce5aac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsBeach at waypoint 11 (cell 149, 205).
2. Play sound _Amb_BirdsBeach at waypoint 43 (cell 148, 183).
3. Play sound _Amb_BirdsBeach at waypoint 42 (cell 158, 175).
4. Play sound _Amb_BirdsBeach at waypoint 29 (cell 165, 180).
5. Play sound _Amb_BirdsBeach at waypoint 36 (cell 179, 176).
6. Play sound _Amb_BirdsBeach at waypoint 62 (cell 184, 154).
7. Play sound _Amb_BirdsBeach at waypoint 61 (cell 198, 159).
8. Play sound _Amb_BirdsBeach at waypoint 60 (cell 201, 145).
9. Play sound _Amb_BirdsBeach at waypoint 59 (cell 201, 126).
10. Play sound _Amb_BirdsBeach at waypoint 76 (cell 181, 108).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5687, Events line 5748, Actions line 5809.

<a id="trigger-0b7b8c9c"></a>

### 50. Ambient Birds 2 - 0B7B8C9C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ambient Birds (0BCE57AC)](#trigger-0bce57ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsBeach at waypoint 73 (cell 153, 89).
2. Play sound _Amb_BirdsBeach at waypoint 77 (cell 152, 71).
3. Play sound _Amb_BirdsBeach at waypoint 79 (cell 109, 61).
4. Play sound _Amb_BirdsBeach at waypoint 81 (cell 113, 88).
5. Play sound _Amb_BirdsBeach at waypoint 71 (cell 120, 109).
6. Play sound _Amb_BirdsBeach at waypoint 69 (cell 97, 114).
7. Play sound _Amb_BirdsBeach at waypoint 86 (cell 53, 109).
8. Play sound _Amb_BirdsBeach at waypoint 84 (cell 69, 86).
9. Play sound _Amb_BirdsBeach at waypoint 83 (cell 64, 68).
10. Play sound _Amb_BirdsBeach at waypoint 82 (cell 64, 54).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5688, Events line 5749, Actions line 5810.

<a id="trigger-0b79972c"></a>

### 51. Ocean Lite - 0B79972C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ambient Birds 2 (0B7B8C9C)](#trigger-0b7b8c9c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 50 (cell 178, 164).
2. Play sound _Amb_OceanLight at waypoint 14 (cell 131, 48).
3. Play sound _Amb_OceanLight at waypoint 49 (cell 166, 150).
4. Play sound _Amb_OceanLight at waypoint 48 (cell 154, 145).
5. Play sound _Amb_OceanLight at waypoint 47 (cell 144, 149).
6. Play sound _Amb_OceanLight at waypoint 56 (cell 177, 144).
7. Play sound _Amb_OceanLight at waypoint 57 (cell 185, 135).
8. Play sound _Amb_OceanLight at waypoint 58 (cell 185, 123).
9. Play sound _Amb_OceanLight at waypoint 55 (cell 163, 132).
10. Play sound _Amb_OceanLight at waypoint 54 (cell 134, 135).
11. Play sound _Amb_OceanLight at waypoint 53 (cell 120, 138).
12. Play sound _Amb_OceanLight at waypoint 52 (cell 109, 145).
13. Play sound _Amb_OceanLight at waypoint 63 (cell 110, 157).
14. Play sound _Amb_OceanLight at waypoint 65 (cell 81, 153).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5689, Events line 5750, Actions line 5811.

<a id="trigger-0b7d827c"></a>

### 52. Ocean Lite 2 - 0B7D827C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ocean Lite (0B79972C)](#trigger-0b79972c).

Attached scope: tag definitions 0BCE589C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 67 (cell 77, 127).
2. Play sound _Amb_OceanLight at waypoint 68 (cell 85, 119).
3. Play sound _Amb_OceanLight at waypoint 70 (cell 111, 114).
4. Play sound _Amb_OceanLight at waypoint 72 (cell 136, 95).
5. Play sound _Amb_OceanLight at waypoint 75 (cell 171, 94).
6. Play sound _Amb_OceanLight at waypoint 74 (cell 162, 85).
7. Play sound _Amb_OceanLight at waypoint 78 (cell 121, 55).
8. Play sound _Amb_OceanLight at waypoint 80 (cell 106, 79).
9. Play sound _Amb_OceanLight at waypoint 89 (cell 42, 117).
10. Play sound _Amb_OceanLight at waypoint 87 (cell 39, 99).
11. Play sound _Amb_OceanLight at waypoint 85 (cell 63, 101).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5690, Events line 5751, Actions line 5812.

<a id="trigger-087f2c4c"></a>

### 53. Squid Intro - 087F2C4C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 087F2B6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Unit Type: type index 24 (global list position: Giant Squid (SQD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play in-game movie 118.
2. Switch the sidebar to tab 3.
3. Flash cameo/type 324; additional configured duration/location argument 120.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5691, Events line 5752, Actions line 5813.

<a id="trigger-0b16b91c"></a>

### 54. WCD_Attack_fake - 0B16B91C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B1712DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The visible mission countdown has expired.

**Then perform these actions in order:**

1. Lightning Storm strike at waypoint 93 (cell 167, 172).
2. Enable and reset applicable timers for [WCD_Enabled_real (0B17417C)](#trigger-0b17417c).
3. Enable and reset applicable timers for [Zofia 5 (0B7BEA70)](#trigger-0b7bea70).
4. Lightning strike at; main setting 32; location/duration field AG.
5. Lightning strike at; main setting 16; location/duration field Q.
6. Lightning strike at; main setting 60; location/duration field BI.
7. Lightning strike at; main setting 81; location/duration field CD.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5692, Events line 5753, Actions line 5814.

<a id="trigger-0b17417c"></a>

### 55. WCD_Enabled_real - 0B17417C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [WCD_Attack_fake (0B16B91C)](#trigger-0b16b91c).

Attached scope: tag definitions 0B1771AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 4 (WCD Power On).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5693, Events line 5754, Actions line 5815.

<a id="trigger-08c8503c"></a>

### 56. Kill the Nuke! - 08C8503C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AF2878C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 54 (global list position: Nuclear Missile Silo (NAMISL)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Nuke Buster Team (08CC8B0C)](sov10t-teams.md#team-08cc8b0c) at waypoint 95 (cell 34, 109).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5694, Events line 5755, Actions line 5816.

<a id="trigger-0847c3ec"></a>

### 57. Beach Hotel Bonus - 0847C3EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM06), owner Civie1 House, cell (140, 215), tag 0847DD2C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 96 (cell 144, 217).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5695, Events line 5756, Actions line 5817.

<a id="trigger-0cc538ac"></a>

### 58. Bonus Psy Corps - 0CC538AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Psi Commando (PTROOP), owner Civie1 House, cell (125, 68), tag 0CC54A8C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Reveal terrain around waypoint 97 (cell 124, 69).
3. Create radar-event marker type 1 at waypoint 97 (cell 124, 69).
4. Play sound Bonus.
5. Play voice notification Mis_S10_Yuri.

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5696, Events line 5757, Actions line 5818.

<a id="trigger-0b3fb3fc"></a>

### 59. _Lose Condition - 0B3FB3FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B3F87FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Loser (09AB6F60)](#trigger-09ab6f60).

Source locator: MAPS02.MIX/sov10t.map; Triggers line 5697, Events line 5758, Actions line 5819.

[All team rosters and ordered plans](sov10t-teams.md) | [All mission overrides](sov10t-overrides.md)
