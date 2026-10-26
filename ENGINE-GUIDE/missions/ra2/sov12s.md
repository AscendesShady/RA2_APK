# Operation: Polar Storm

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov12s.map. **Effective extracted member:** MAPS02.MIX/sov12s.map. **Trigger definitions:** 54.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov12s-teams.md) | [All mission overrides](sov12s-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | SNOW |
| Map size | 0,0,78,120 |
| Visible local rectangle | 2,5,74,109 |
| Placed vehicles | 21 |
| Placed infantry | 23 |
| Placed structures | 192 |
| Placed aircraft | 0 |
| Team templates | 37 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 500 | BadGuy1 |
| 2 | BadGuy2 House | 150 | BadGuy2 |
| 3 | BadGuy3 House | 600 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | BG_Naval House | 200 | BG_Naval |
| 6 | Other2 House | 20 | Other2 |
| 7 | Other3 House | 20 | Other3 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | BG1 Chrono,0 |
| 1 | BG2 Chrono,0 |
| 2 | BG3 Chrono,0 |
| 3 | BG1 Entered,0 |
| 4 | BG2 Entered,0 |
| 5 | BG3 Entered,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Win (0CDA750C)](#trigger-0cda750c) | 7 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [Lose Condition (0AC7BD50)](#trigger-0ac7bd50) | Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House). | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-08a01b20"></a>

### 1. First Contact - 08A01B20

Owner reference: BG_Naval. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Aegis Cruiser (AEGIS), owner BadGuy1 House, cell (136, 149), tag 08A014E0, persistence mode 0; Aegis Cruiser (AEGIS), owner BadGuy1 House, cell (135, 130), tag 08A014E0, persistence mode 0; Aegis Cruiser (AEGIS), owner BadGuy1 House, cell (135, 138), tag 08A014E0, persistence mode 0; Destroyer (DEST), owner BadGuy1 House, cell (130, 122), tag 08A014E0, persistence mode 0; Destroyer (DEST), owner BadGuy1 House, cell (130, 116), tag 08A014E0, persistence mode 0; Destroyer (DEST), owner BadGuy1 House, cell (133, 125), tag 08A014E0, persistence mode 0; Destroyer (DEST), owner BadGuy1 House, cell (134, 141), tag 08A014E0, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Play sound NukeSiren.
2. Reveal terrain around waypoint 0 (cell 136, 153).
3. Reveal terrain around waypoint 1 (cell 135, 149).
4. Reveal terrain around waypoint 2 (cell 132, 144).
5. Reveal terrain around waypoint 3 (cell 133, 140).
6. Reveal terrain around waypoint 4 (cell 134, 137).
7. Reveal terrain around waypoint 5 (cell 134, 129).
8. Reveal terrain around waypoint 6 (cell 133, 126).
9. Reveal terrain around waypoint 7 (cell 129, 123).
10. Reveal terrain around waypoint 8 (cell 131, 120).
11. Reveal terrain around waypoint 9 (cell 130, 116).
12. Reveal terrain around waypoint 10 (cell 128, 108).
13. Create/recruit team [Destroyer (1) Team (087D680C)](sov12s-teams.md#team-087d680c).
14. Production Begins: owner selector 18 (country/type BG_NAVAL; placed owner BG_Naval House).
15. AI triggers begin: owner selector 18 (country/type BG_NAVAL; placed owner BG_Naval House).
16. Enable and reset applicable timers for [Ship_Radar_Event (0D0203D0)](#trigger-0d0203d0).
17. Enable and reset applicable timers for [BG1 Startup (09FA8F40)](#trigger-09fa8f40).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5385, Events line 5441, Actions line 5497.

<a id="trigger-0d0203d0"></a>

### 2. Ship_Radar_Event - 0D0203D0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [First Contact (08A01B20)](#trigger-08a01b20).

Attached scope: tag definitions 0D025DC0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Carrier (1) Team (087D6EFC)](sov12s-teams.md#team-087d6efc) at waypoint 12 (cell 132, 112).
2. Supply reinforcement team [Destroyer (1) Team (087D680C)](sov12s-teams.md#team-087d680c) at waypoint 13 (cell 132, 150).
3. Create radar-event marker type 5 at waypoint 0 (cell 136, 153).
4. Create radar-event marker type 5 at waypoint 1 (cell 135, 149).
5. Create radar-event marker type 5 at waypoint 2 (cell 132, 144).
6. Create radar-event marker type 5 at waypoint 3 (cell 133, 140).
7. Create radar-event marker type 5 at waypoint 4 (cell 134, 137).
8. Create radar-event marker type 5 at waypoint 5 (cell 134, 129).
9. Create radar-event marker type 5 at waypoint 6 (cell 133, 126).
10. Create radar-event marker type 5 at waypoint 7 (cell 129, 123).
11. Create radar-event marker type 5 at waypoint 8 (cell 131, 120).
12. Create radar-event marker type 5 at waypoint 9 (cell 130, 116).
13. Create radar-event marker type 5 at waypoint 10 (cell 128, 108).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5386, Events line 5442, Actions line 5498.

<a id="trigger-09fa8f40"></a>

### 3. BG1 Startup - 09FA8F40

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [First Contact (08A01B20)](#trigger-08a01b20); enable from [Default Enable BG1 (0812ADBC)](#trigger-0812adbc).

Attached scope: tag definitions 09FA8E70 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Create/recruit team [Rocketeer (4) Team (0AD57F10)](sov12s-teams.md#team-0ad57f10).
4. Enable and reset applicable timers for [BG2 Startup (09F06970)](#trigger-09f06970).
5. Enable and reset applicable timers for [Chrono at Island Gold (07F510FC)](#trigger-07f510fc).
6. Enable and reset applicable timers for [Sofia Re Chrono (08F6D0C0)](#trigger-08f6d0c0).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5387, Events line 5443, Actions line 5499.

<a id="trigger-09f06970"></a>

### 4. BG2 Startup - 09F06970

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Startup (09FA8F40)](#trigger-09fa8f40).

Attached scope: tag definitions 00000008 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. AI triggers begin: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
2. Production Begins: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
3. Enable and reset applicable timers for [BG3 Startup (0B6558A0)](#trigger-0b6558a0).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5388, Events line 5444, Actions line 5500.

<a id="trigger-07f510fc"></a>

### 5. Chrono at Island Gold - 07F510FC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Startup (09FA8F40)](#trigger-09fa8f40); enable from [Harass Enable (0805556C)](#trigger-0805556c).

Attached scope: tag definitions 0BC6694C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono Harass 6 IFV (0D1F022C)](sov12s-teams.md#team-0d1f022c) at waypoint 29 (cell 170, 100).
2. Enable and reset applicable timers for [Chrono at Island Front (08055CBC)](#trigger-08055cbc).
3. Play sound ChronosphereMove at waypoint 29 (cell 170, 100).
4. Play Anim At; main setting 253; location/duration field CI.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5389, Events line 5445, Actions line 5501.

<a id="trigger-08f6d0c0"></a>

### 6. Sofia Re Chrono - 08F6D0C0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Startup (09FA8F40)](#trigger-09fa8f40).

Attached scope: tag definitions 08F68190 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 50 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification Mis_S12_Sofia2.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5390, Events line 5446, Actions line 5502.

<a id="trigger-0b6558a0"></a>

### 7. BG3 Startup - 0B6558A0

Owner reference: BadGuy3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG2 Startup (09F06970)](#trigger-09f06970).

Attached scope: tag definitions 0B655470 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).
2. AI triggers begin: owner selector 16 (country/type BADGUY3; placed owner BadGuy3 House).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5391, Events line 5447, Actions line 5503.

<a id="trigger-08055cbc"></a>

### 8. Chrono at Island Front - 08055CBC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono at Island Gold (07F510FC)](#trigger-07f510fc).

Attached scope: tag definitions 0BC6686C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono Harass 6 Grizzly (0D1F1EFC)](sov12s-teams.md#team-0d1f1efc) at waypoint 17 (cell 168, 112).
2. Enable and reset applicable timers for [Chrono Seals (0BC66A2C)](#trigger-0bc66a2c).
3. Play sound ChronosphereMove at waypoint 17 (cell 168, 112).
4. Play Anim At; main setting 253; location/duration field CK.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5392, Events line 5448, Actions line 5504.

<a id="trigger-0bc66a2c"></a>

### 9. Chrono Seals - 0BC66A2C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono at Island Front (08055CBC)](#trigger-08055cbc).

Attached scope: tag definitions 0BC6678C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono Seals (0BB03DEC)](sov12s-teams.md#team-0bb03dec) at waypoint 34 (cell 174, 133).
2. Enable and reset applicable timers for [Chrono Carriers Attack (0BC380EC)](#trigger-0bc380ec).
3. Reveal terrain around waypoint 34 (cell 174, 133).
4. Create radar-event marker type 5 at waypoint 34 (cell 174, 133).
5. Play voice notification EVA_EnemyFleetDetected.
6. Play sound ChronosphereMove at waypoint 34 (cell 174, 133).
7. Play Anim At; main setting 253; location/duration field CM.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5393, Events line 5449, Actions line 5505.

<a id="trigger-0bc380ec"></a>

### 10. Chrono Carriers Attack - 0BC380EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono Seals (0BC66A2C)](#trigger-0bc66a2c).

Attached scope: tag definitions 0BC3B1CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono Carriers (0CFB393C)](sov12s-teams.md#team-0cfb393c) at waypoint 36 (cell 150, 93).
2. Enable and reset applicable timers for [Chrono Tank Attack (0BC3E10C)](#trigger-0bc3e10c).
3. Reveal terrain around waypoint 36 (cell 150, 93).
4. Create radar-event marker type 5 at waypoint 36 (cell 150, 93).
5. Play voice notification EVA_EnemyFleetDetected.
6. Play sound ChronosphereMove at waypoint 36 (cell 150, 93).
7. Play Anim At; main setting 253; location/duration field CJ.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5394, Events line 5450, Actions line 5506.

<a id="trigger-0bc3e10c"></a>

### 11. Chrono Tank Attack - 0BC3E10C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono Carriers Attack (0BC380EC)](#trigger-0bc380ec).

Attached scope: tag definitions 0BC3D1CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono Harass 6 Grizzly (0D1F1EFC)](sov12s-teams.md#team-0d1f1efc) at waypoint 37 (cell 176, 120).
2. Reveal terrain around waypoint 37 (cell 176, 120).
3. Create radar-event marker type 5 at waypoint 37 (cell 176, 120).
4. Play voice notification EVA_ArmorBattallianDetected.
5. Play sound ChronosphereMove at waypoint 37 (cell 176, 120).
6. Play Anim At; main setting 253; location/duration field CL.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5395, Events line 5451, Actions line 5507.

<a id="trigger-093c78b0"></a>

### 12. Create Team - 093C78B0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 093C73D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [(2)Destroyer Team (087D44BC)](sov12s-teams.md#team-087d44bc).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5396, Events line 5452, Actions line 5508.

<a id="trigger-0ac68f60"></a>

### 13. Win Condition_Timer - 0AC68F60

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Chrono Sphere (GACSPH), owner BadGuy3 House, cell (68, 129), tag 0AC689E0, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “Objective 1 Complete” (MISSION:Objective1).
2. Enable and reset applicable timers for [Ending Movie 1 (0D10EF3C)](#trigger-0d10ef3c).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5397, Events line 5453, Actions line 5509.

<a id="trigger-0d10ef3c"></a>

### 14. Ending Movie 1 - 0D10EF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win Condition_Timer (0AC68F60)](#trigger-0ac68f60).

Attached scope: tag definitions 0D10EE5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play full-screen movie 141.
2. Enable and reset applicable timers for [Cheer (0CDA6F3C)](#trigger-0cda6f3c).
3. Enable and reset applicable timers for [Win (0CDA750C)](#trigger-0cda750c).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5398, Events line 5454, Actions line 5510.

<a id="trigger-0cda6f3c"></a>

### 15. Cheer - 0CDA6F3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Ending Movie 1 (0D10EF3C)](#trigger-0d10ef3c).

Attached scope: tag definitions 0CDA6E5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5399, Events line 5455, Actions line 5511.

<a id="trigger-0cda750c"></a>

### 16. Win - 0CDA750C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Ending Movie 1 (0D10EF3C)](#trigger-0d10ef3c).

Attached scope: tag definitions 0CDA742C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 7 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5400, Events line 5456, Actions line 5512.

<a id="trigger-0ac77da0"></a>

### 17. Kirovs Gained - 0AC77DA0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Kirov Airship (ZEP), owner Civie1 House, cell (73, 38), tag 083A1D3C, persistence mode 0; Kirov Airship (ZEP), owner Civie1 House, cell (77, 33), tag 083A1D3C, persistence mode 0; Kirov Airship (ZEP), owner Civie1 House, cell (81, 35), tag 083A1D3C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Change House: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Reveal terrain around waypoint 14 (cell 77, 36).
3. Play sound Bonus.
4. Display message “Objective 2 Complete” (MISSION:Objective2).
5. Display message “Objective 1: Destroy the Allied CHRONOSPHERE” (MISSION:Sov12c).
6. Create/recruit team [Kirovs Rise (088F5CEC)](sov12s-teams.md#team-088f5cec).
7. Disable [Text Trigger 2 (0805B27C)](#trigger-0805b27c).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5401, Events line 5457, Actions line 5513.

<a id="trigger-0805b27c"></a>

### 18. Text Trigger 2 - 0805B27C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 69 tagged map cells: (106, 106), (107, 106), (108, 106), (106, 107), (107, 107), (108, 107), (109, 107), (105, 108), (106, 108), (107, 108), (108, 108), (109, 108), (110, 108), (105, 109), (106, 109), (107, 109), (108, 109), (109, 109), (110, 109), (111, 109), (105, 110), (106, 110), (107, 110), (108, 110), (109, 110), (110, 110), (111, 110), (112, 110), (105, 111), (106, 111), (107, 111), (108, 111), (109, 111), (110, 111), (111, 111), (112, 111), (113, 111), (106, 112), (107, 112), (108, 112), (109, 112), (110, 112), (111, 112), (112, 112), (113, 112), (114, 112), (108, 113), (109, 113), (110, 113), (111, 113), (112, 113), (113, 113), (114, 113), (109, 114), (110, 114), (111, 114), (112, 114), (113, 114), (114, 114), (110, 115), (111, 115), (112, 115), (113, 115), (111, 116), (112, 116), (113, 116), (112, 117), (113, 117), (113, 118); tag 0805CC2C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Display message “Objective 1 Complete” (MISSION:Objective1).
2. Play voice notification Mis_S12_Sofia1.
3. Display message “Move north and reclaim our captured Kirov airships” (MISSION:Sov12b).
4. Enable and reset applicable timers for [Disable Chrono at BG1 (07F5230C)](#trigger-07f5230c).
5. Enable and reset applicable timers for [Disable Chrono Harass (07F528CC)](#trigger-07f528cc).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5402, Events line 5458, Actions line 5514.

<a id="trigger-07f5230c"></a>

### 19. Disable Chrono at BG1 - 07F5230C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Text Trigger 2 (0805B27C)](#trigger-0805b27c); enable from [Chrono Attack at BG2 (080DE8EC)](#trigger-080de8ec).

Attached scope: tag definitions 07F5210C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Chrono Attack at BG1 (08066F3C)](#trigger-08066f3c).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5403, Events line 5459, Actions line 5515.

<a id="trigger-07f528cc"></a>

### 20. Disable Chrono Harass - 07F528CC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Text Trigger 2 (0805B27C)](#trigger-0805b27c); enable from [Chrono Attack at BG1 (08066F3C)](#trigger-08066f3c).

Attached scope: tag definitions 07F524AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Chrono at Island Gold (07F510FC)](#trigger-07f510fc).
2. Disable [Chrono at Island Front (08055CBC)](#trigger-08055cbc).
3. Disable 0 (not a defined local trigger).
4. Disable 0 (not a defined local trigger).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5404, Events line 5460, Actions line 5516.

<a id="trigger-08066f3c"></a>

### 21. Chrono Attack at BG1 - 08066F3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player at BG1 Gold  (08062BFC)](#trigger-08062bfc); enable from [Start BG1 BG2 (07AAAF40)](#trigger-07aaaf40); enable from [Start BG1 BG2 BG3 (07AAACA0)](#trigger-07aaaca0); enable from [Start BG1 BG3 (07AAAE60)](#trigger-07aaae60); enable from [Start BG1 Chrono (07AA9450)](#trigger-07aa9450).

Attached scope: tag definitions 08066A0C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono Attack 6 IFV (07BC9F00)](sov12s-teams.md#team-07bc9f00) at waypoint 28 (cell 98, 125).
2. Enable and reset applicable timers for [Disable Chrono Harass (07F528CC)](#trigger-07f528cc).
3. Enable and reset applicable timers for [Stop Mainland Chrono (07AA99E0)](#trigger-07aa99e0).
4. Disable [Chrono Attack at BG1 (08066F3C)](#trigger-08066f3c).
5. Play sound ChronosphereMove at waypoint 28 (cell 98, 125).
6. Play Anim At; main setting 253; location/duration field CN.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5405, Events line 5461, Actions line 5517.

<a id="trigger-07aa99e0"></a>

### 22. Stop Mainland Chrono - 07AA99E0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chrono Attack at BG1 (08066F3C)](#trigger-08066f3c); enable from [Chrono Attack at BG2 (080DE8EC)](#trigger-080de8ec); enable from [Chrono Attack at BG3 (080EE57C)](#trigger-080ee57c).

Attached scope: tag definitions 07AA9530 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Stop Mainland Chrono (07AA99E0)](#trigger-07aa99e0).
2. Enable and reset applicable timers for [Check Mainland Chrono (07A95EA0)](#trigger-07a95ea0).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5406, Events line 5462, Actions line 5518.

<a id="trigger-07a95ea0"></a>

### 23. Check Mainland Chrono - 07A95EA0

Owner reference: Other3. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Stop Mainland Chrono (07AA99E0)](#trigger-07aa99e0).

Attached scope: tag definitions 07A95CD0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  All: owner selector 20 (country/type OTHER3; placed owner Other3 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Start BG1 BG2 (07AAAF40)](#trigger-07aaaf40).
2. Enable and reset applicable timers for [Start BG1 BG2 BG3 (07AAACA0)](#trigger-07aaaca0).
3. Enable and reset applicable timers for [Start BG1 BG3 (07AAAE60)](#trigger-07aaae60).
4. Enable and reset applicable timers for [Start BG2 BG3 (07AAAD80)](#trigger-07aaad80).
5. Enable and reset applicable timers for [Start BG1 Chrono (07AA9450)](#trigger-07aa9450).
6. Enable and reset applicable timers for [Start BG2 Chrono (07AA91A0)](#trigger-07aa91a0).
7. Enable and reset applicable timers for [Start BG3 Chrono (07AA90C0)](#trigger-07aa90c0).
8. Disable [Check Mainland Chrono (07A95EA0)](#trigger-07a95ea0).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5407, Events line 5463, Actions line 5519.

<a id="trigger-0ac7bd50"></a>

### 24. Lose Condition - 0AC7BD50

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AC7B760 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5408, Events line 5464, Actions line 5520.

<a id="trigger-096740f0"></a>

### 25. Reveal StartPoint - 096740F0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09674620 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 98 (cell 176, 114).
2. Reveal terrain around waypoint 15 (cell 171, 119).
3. Reveal terrain around waypoint 16 (cell 166, 122).
4. Reveal terrain around waypoint 17 (cell 168, 112).
5. Reveal terrain around waypoint 18 (cell 158, 102).
6. Reveal terrain around waypoint 19 (cell 159, 93).
7. Reveal terrain around waypoint 20 (cell 168, 105).
8. Reveal terrain around waypoint 46 (cell 150, 104).
9. Reveal terrain around waypoint 29 (cell 170, 100).
10. Reveal terrain around waypoint 34 (cell 174, 133).
11. Reveal terrain around waypoint 89 (cell 177, 122).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5409, Events line 5465, Actions line 5521.

<a id="trigger-0967dd00"></a>

### 26. Reveal BG3 Gold - 0967DD00

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 32 tagged map cells: (95, 159), (95, 160), (96, 160), (97, 160), (96, 161), (97, 161), (98, 161), (99, 161), (97, 162), (98, 162), (99, 162), (100, 162), (99, 163), (100, 163), (101, 163), (100, 164), (101, 164), (102, 164), (101, 165), (102, 165), (103, 165), (102, 166), (103, 166), (103, 167), (104, 167), (104, 168), (105, 168), (106, 168), (106, 169), (107, 169), (108, 169), (108, 170); tag 0967CE20, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 23 (cell 110, 166).
2. Reveal terrain around waypoint 24 (cell 103, 160).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5410, Events line 5466, Actions line 5522.

<a id="trigger-096783f0"></a>

### 27. Reveal BG3 Base - 096783F0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0967FD10 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 25 (cell 89, 150).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5411, Events line 5467, Actions line 5523.

<a id="trigger-0d1019e0"></a>

### 28. Reveal BG_Naval - 0D1019E0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 33 tagged map cells: (127, 101), (128, 101), (128, 102), (129, 102), (128, 103), (129, 103), (130, 103), (127, 104), (128, 104), (129, 104), (130, 104), (131, 104), (130, 105), (131, 105), (126, 106), (127, 106), (128, 106), (129, 106), (130, 106), (131, 106), (126, 107), (127, 107), (128, 107), (129, 107), (130, 107), (131, 107), (125, 108), (126, 108), (126, 109), (126, 110), (127, 110), (126, 111), (127, 111); tag 0D104420, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 22 (cell 125, 104).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5412, Events line 5468, Actions line 5524.

<a id="trigger-0d104340"></a>

### 29. Reveal BG1 - 0D104340

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 50 tagged map cells: (116, 70), (117, 70), (118, 70), (116, 71), (117, 71), (118, 71), (119, 71), (116, 72), (117, 72), (118, 72), (119, 72), (120, 72), (116, 73), (117, 73), (118, 73), (119, 73), (120, 73), (121, 73), (116, 74), (117, 74), (118, 74), (119, 74), (120, 74), (121, 74), (122, 74), (116, 75), (117, 75), (118, 75), (119, 75), (120, 75), (121, 75), (122, 75), (117, 76), (118, 76), (119, 76), (120, 76), (121, 76), (122, 76), (119, 77), (120, 77), (121, 77), (122, 77), (120, 78), (121, 78), (122, 78), (120, 79), (121, 79), (122, 79), (121, 80), (122, 80); tag 0D104230, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Reveal terrain around waypoint 21 (cell 116, 77).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5413, Events line 5469, Actions line 5525.

<a id="trigger-08062bfc"></a>

### 30. Player at BG1 Gold  - 08062BFC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 50 tagged map cells: (97, 117), (96, 118), (98, 118), (96, 119), (97, 119), (99, 119), (100, 119), (95, 120), (96, 120), (100, 120), (94, 121), (95, 121), (99, 121), (100, 121), (94, 122), (100, 122), (102, 122), (94, 123), (100, 123), (102, 123), (94, 124), (101, 124), (103, 124), (94, 125), (102, 125), (103, 125), (94, 126), (95, 126), (102, 126), (95, 127), (102, 127), (95, 128), (102, 128), (95, 129), (96, 129), (101, 129), (102, 129), (96, 130), (101, 130), (96, 131), (100, 131), (101, 131), (95, 132), (96, 132), (99, 132), (100, 132), (96, 133), (97, 133), (98, 133), (99, 133); tag 080650FC, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG1 (08066F3C)](#trigger-08066f3c).
2. Set local flag 3 (BG1 Entered).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5414, Events line 5470, Actions line 5526.

<a id="trigger-07aaaf40"></a>

### 31. Start BG1 BG2 - 07AAAF40

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start BG3 Chrono (07AA90C0)](#trigger-07aa90c0).

Incoming activation links: enable from [Check Mainland Chrono (07A95EA0)](#trigger-07a95ea0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (BG1 Entered) is set.
2. local flag 4 (BG2 Entered) is set.

Flag writers in this mission: set local flag 3 (BG1 Entered) at [Player at BG1 Gold  (08062BFC)](#trigger-08062bfc); set local flag 4 (BG2 Entered) at [Player at BG2 Gold (080DE0EC)](#trigger-080de0ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG1 (08066F3C)](#trigger-08066f3c).
2. Enable and reset applicable timers for [Chrono Attack at BG2 (080DE8EC)](#trigger-080de8ec).
3. Disable [Start BG1 BG2 (07AAAF40)](#trigger-07aaaf40).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5415, Events line 5471, Actions line 5527.

<a id="trigger-07aaaca0"></a>

### 32. Start BG1 BG2 BG3 - 07AAACA0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start BG2 BG3 (07AAAD80)](#trigger-07aaad80).

Incoming activation links: enable from [Check Mainland Chrono (07A95EA0)](#trigger-07a95ea0).

Attached scope: tag definitions 07AA9280 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (BG1 Entered) is set.
2. local flag 4 (BG2 Entered) is set.
3. local flag 5 (BG3 Entered) is set.

Flag writers in this mission: set local flag 3 (BG1 Entered) at [Player at BG1 Gold  (08062BFC)](#trigger-08062bfc); set local flag 4 (BG2 Entered) at [Player at BG2 Gold (080DE0EC)](#trigger-080de0ec); set local flag 5 (BG3 Entered) at [Player at BG3 Gold (080EFD2C)](#trigger-080efd2c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG1 (08066F3C)](#trigger-08066f3c).
2. Enable and reset applicable timers for [Chrono Attack at BG2 (080DE8EC)](#trigger-080de8ec).
3. Enable and reset applicable timers for [Chrono Attack at BG3 (080EE57C)](#trigger-080ee57c).
4. Disable [Start BG1 BG2 BG3 (07AAACA0)](#trigger-07aaaca0).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5416, Events line 5472, Actions line 5528.

<a id="trigger-07aaae60"></a>

### 33. Start BG1 BG3 - 07AAAE60

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start BG1 BG2 (07AAAF40)](#trigger-07aaaf40).

Incoming activation links: enable from [Check Mainland Chrono (07A95EA0)](#trigger-07a95ea0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (BG1 Entered) is set.
2. local flag 5 (BG3 Entered) is clear.

Flag writers in this mission: set local flag 3 (BG1 Entered) at [Player at BG1 Gold  (08062BFC)](#trigger-08062bfc); set local flag 5 (BG3 Entered) at [Player at BG3 Gold (080EFD2C)](#trigger-080efd2c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG1 (08066F3C)](#trigger-08066f3c).
2. Enable and reset applicable timers for [Chrono Attack at BG3 (080EE57C)](#trigger-080ee57c).
3. Disable [Start BG1 BG3 (07AAAE60)](#trigger-07aaae60).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5417, Events line 5473, Actions line 5529.

<a id="trigger-07aaad80"></a>

### 34. Start BG2 BG3 - 07AAAD80

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start BG1 BG3 (07AAAE60)](#trigger-07aaae60).

Incoming activation links: enable from [Check Mainland Chrono (07A95EA0)](#trigger-07a95ea0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 4 (BG2 Entered) is set.
2. local flag 5 (BG3 Entered) is set.

Flag writers in this mission: set local flag 4 (BG2 Entered) at [Player at BG2 Gold (080DE0EC)](#trigger-080de0ec); set local flag 5 (BG3 Entered) at [Player at BG3 Gold (080EFD2C)](#trigger-080efd2c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG2 (080DE8EC)](#trigger-080de8ec).
2. Enable and reset applicable timers for [Chrono Attack at BG3 (080EE57C)](#trigger-080ee57c).
3. Disable [Start BG2 BG3 (07AAAD80)](#trigger-07aaad80).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5418, Events line 5474, Actions line 5530.

<a id="trigger-07aa9450"></a>

### 35. Start BG1 Chrono - 07AA9450

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Check Mainland Chrono (07A95EA0)](#trigger-07a95ea0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 3 (BG1 Entered) is set.

Flag writers in this mission: set local flag 3 (BG1 Entered) at [Player at BG1 Gold  (08062BFC)](#trigger-08062bfc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG1 (08066F3C)](#trigger-08066f3c).
2. Disable [Start BG1 Chrono (07AA9450)](#trigger-07aa9450).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5419, Events line 5475, Actions line 5531.

<a id="trigger-07aa91a0"></a>

### 36. Start BG2 Chrono - 07AA91A0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start BG1 Chrono (07AA9450)](#trigger-07aa9450).

Incoming activation links: enable from [Check Mainland Chrono (07A95EA0)](#trigger-07a95ea0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 4 (BG2 Entered) is set.

Flag writers in this mission: set local flag 4 (BG2 Entered) at [Player at BG2 Gold (080DE0EC)](#trigger-080de0ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG2 (080DE8EC)](#trigger-080de8ec).
2. Disable [Start BG2 Chrono (07AA91A0)](#trigger-07aa91a0).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5420, Events line 5476, Actions line 5532.

<a id="trigger-07aa90c0"></a>

### 37. Start BG3 Chrono - 07AA90C0

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Start BG2 Chrono (07AA91A0)](#trigger-07aa91a0).

Incoming activation links: enable from [Check Mainland Chrono (07A95EA0)](#trigger-07a95ea0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 5 (BG3 Entered) is set.

Flag writers in this mission: set local flag 5 (BG3 Entered) at [Player at BG3 Gold (080EFD2C)](#trigger-080efd2c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG3 (080EE57C)](#trigger-080ee57c).
2. Disable [Start BG3 Chrono (07AA90C0)](#trigger-07aa90c0).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5421, Events line 5477, Actions line 5533.

<a id="trigger-080de8ec"></a>

### 38. Chrono Attack at BG2 - 080DE8EC

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start BG1 BG2 (07AAAF40)](#trigger-07aaaf40); enable from [Start BG1 BG2 BG3 (07AAACA0)](#trigger-07aaaca0); enable from [Start BG2 BG3 (07AAAD80)](#trigger-07aaad80); enable from [Start BG2 Chrono (07AA91A0)](#trigger-07aa91a0); enable from [Player at BG2 Gold (080DE0EC)](#trigger-080de0ec).

Attached scope: tag definitions 080DE2BC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono Attack 6 Grizzly (07BC8130)](sov12s-teams.md#team-07bc8130) at waypoint 26 (cell 72, 29).
2. Enable and reset applicable timers for [Disable Chrono at BG1 (07F5230C)](#trigger-07f5230c).
3. Enable and reset applicable timers for [Stop Mainland Chrono (07AA99E0)](#trigger-07aa99e0).
4. Disable [Chrono Attack at BG2 (080DE8EC)](#trigger-080de8ec).
5. Play sound ChronosphereMove at waypoint 26 (cell 72, 29).
6. Play Anim At; main setting 253; location/duration field CO.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5422, Events line 5478, Actions line 5534.

<a id="trigger-080ee57c"></a>

### 39. Chrono Attack at BG3 - 080EE57C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Start BG1 BG2 BG3 (07AAACA0)](#trigger-07aaaca0); enable from [Start BG1 BG3 (07AAAE60)](#trigger-07aaae60); enable from [Start BG2 BG3 (07AAAD80)](#trigger-07aaad80); enable from [Start BG3 Chrono (07AA90C0)](#trigger-07aa90c0); enable from [Player at BG3 Gold (080EFD2C)](#trigger-080efd2c).

Attached scope: tag definitions 080EFE1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply chrono reinforcement team [Chrono Attack 4 Prism (07BC9DE0)](sov12s-teams.md#team-07bc9de0) at waypoint 27 (cell 40, 87).
2. Enable and reset applicable timers for [Stop Mainland Chrono (07AA99E0)](#trigger-07aa99e0).
3. Disable [Chrono Attack at BG3 (080EE57C)](#trigger-080ee57c).
4. Play sound ChronosphereMove at waypoint 27 (cell 40, 87).
5. Play Anim At; main setting 253; location/duration field CP.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5423, Events line 5479, Actions line 5535.

<a id="trigger-07ab4b20"></a>

### 40. Disable Start Mainland - 07AB4B20

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07AB37F0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Start BG1 BG2 (07AAAF40)](#trigger-07aaaf40).
2. Disable [Start BG1 BG2 BG3 (07AAACA0)](#trigger-07aaaca0).
3. Disable [Start BG1 BG3 (07AAAE60)](#trigger-07aaae60).
4. Disable [Start BG2 BG3 (07AAAD80)](#trigger-07aaad80).
5. Disable [Start BG1 Chrono (07AA9450)](#trigger-07aa9450).
6. Disable [Start BG2 Chrono (07AA91A0)](#trigger-07aa91a0).
7. Disable [Start BG3 Chrono (07AA90C0)](#trigger-07aa90c0).
8. Disable [Disable Start Mainland (07AB4B20)](#trigger-07ab4b20).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5424, Events line 5480, Actions line 5536.

<a id="trigger-080de0ec"></a>

### 41. Player at BG2 Gold - 080DE0EC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 41 tagged map cells: (71, 23), (72, 23), (72, 24), (72, 25), (73, 25), (74, 25), (74, 26), (75, 26), (75, 27), (75, 28), (76, 28), (77, 28), (77, 29), (77, 30), (76, 31), (77, 31), (61, 32), (62, 32), (75, 32), (76, 32), (61, 33), (62, 33), (63, 33), (64, 33), (65, 33), (66, 33), (73, 33), (74, 33), (75, 33), (60, 34), (61, 34), (66, 34), (67, 34), (68, 34), (69, 34), (72, 34), (73, 34), (69, 35), (70, 35), (71, 35), (72, 35); tag 080DFF4C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG2 (080DE8EC)](#trigger-080de8ec).
2. Set local flag 4 (BG2 Entered).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5425, Events line 5481, Actions line 5537.

<a id="trigger-080efd2c"></a>

### 42. Player at BG3 Gold - 080EFD2C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 92 tagged map cells: (31, 75), (32, 75), (33, 75), (34, 75), (35, 75), (30, 76), (31, 76), (35, 76), (36, 76), (37, 76), (29, 77), (30, 77), (37, 77), (38, 77), (29, 78), (38, 78), (29, 79), (38, 79), (29, 80), (38, 80), (39, 80), (29, 81), (39, 81), (40, 81), (29, 82), (30, 82), (40, 82), (30, 83), (40, 83), (41, 83), (30, 84), (31, 84), (41, 84), (42, 84), (31, 85), (42, 85), (43, 85), (31, 86), (32, 86), (43, 86), (44, 86), (32, 87), (44, 87), (32, 88), (44, 88), (45, 88), (46, 88), (32, 89), (33, 89), (46, 89), (47, 89), (48, 89), (33, 90), (34, 90), (48, 90), (49, 90), (50, 90), (34, 91), (35, 91), (50, 91), (51, 91), (52, 91), (35, 92), (36, 92), (52, 92), (36, 93), (37, 93), (38, 93), (39, 93), (40, 93), (41, 93), (52, 93), (41, 94), (42, 94), (52, 94), (42, 95), (43, 95), (52, 95), (43, 96), (48, 96), (49, 96), (50, 96), (51, 96), (52, 96), (43, 97), (44, 97), (45, 97), (46, 97), (48, 97), (46, 98), (47, 98), (48, 98); tag 080EFA7C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono Attack at BG3 (080EE57C)](#trigger-080ee57c).
2. Set local flag 5 (BG3 Entered).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5426, Events line 5482, Actions line 5538.

<a id="trigger-0805556c"></a>

### 43. Harass Enable - 0805556C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0805447C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Chrono at Island Gold (07F510FC)](#trigger-07f510fc).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5427, Events line 5483, Actions line 5539.

<a id="trigger-0805bc6c"></a>

### 44. Text Trigger 1 - 0805BC6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0805B77C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “Build naval forces and invade the Allied base” (MISSION:Sov12a).
2. Play in-game movie 121.

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5428, Events line 5484, Actions line 5540.

<a id="trigger-0812adbc"></a>

### 45. Default Enable BG1 - 0812ADBC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0812A78C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 Startup (09FA8F40)](#trigger-09fa8f40).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5429, Events line 5485, Actions line 5541.

<a id="trigger-07ff3f3c"></a>

### 46. Nuke Buster Jump Start - 07FF3F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FF45FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 54 (global list position: Nuclear Missile Silo (NAMISL)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Create/recruit team [Nuke Breaker Team (0B3B15FC)](sov12s-teams.md#team-0b3b15fc).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5430, Events line 5486, Actions line 5542.

<a id="trigger-07ff31cc"></a>

### 47. Kirov Breaker  - 07FF31CC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FF7E5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Unit Type: type index 15 (global list position: Kirov Airship (ZEP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Create/recruit team [Kirov Breaker Team (0886890C)](sov12s-teams.md#team-0886890c).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5431, Events line 5487, Actions line 5543.

<a id="trigger-0c111e5c"></a>

### 48. Ambient Ocean 1 - 0C111E5C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 38 (cell 90, 159).
2. Play sound _Amb_OceanHeavy at waypoint 39 (cell 100, 168).
3. Play sound _Amb_OceanHeavy at waypoint 40 (cell 111, 178).
4. Play sound _Amb_OceanHeavy at waypoint 41 (cell 124, 177).
5. Play sound _Amb_OceanHeavy at waypoint 42 (cell 134, 170).
6. Play sound _Amb_OceanHeavy at waypoint 43 (cell 148, 153).
7. Play sound _Amb_OceanHeavy at waypoint 44 (cell 150, 139).
8. Play sound _Amb_OceanHeavy at waypoint 45 (cell 162, 135).
9. Play sound _Amb_OceanHeavy at waypoint 46 (cell 150, 104).
10. Play sound _Amb_OceanHeavy at waypoint 47 (cell 150, 80).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5432, Events line 5488, Actions line 5544.

<a id="trigger-0c11131c"></a>

### 49. Ambient Ocean 2 - 0C11131C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ambient Ocean 1 (0C111E5C)](#trigger-0c111e5c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 48 (cell 158, 86).
2. Play sound _Amb_OceanHeavy at waypoint 36 (cell 150, 93).
3. Play sound _Amb_OceanHeavy at waypoint 49 (cell 156, 117).
4. Play sound _Amb_OceanHeavy at waypoint 50 (cell 147, 123).
5. Play sound _Amb_OceanHeavy at waypoint 51 (cell 142, 107).
6. Play sound _Amb_OceanHeavy at waypoint 52 (cell 137, 92).
7. Play sound _Amb_OceanHeavy at waypoint 53 (cell 143, 82).
8. Play sound _Amb_OceanHeavy at waypoint 54 (cell 125, 73).
9. Play sound _Amb_OceanHeavy at waypoint 55 (cell 133, 66).
10. Play sound _Amb_OceanHeavy at waypoint 56 (cell 113, 60).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5433, Events line 5489, Actions line 5545.

<a id="trigger-0c11469c"></a>

### 50. Ambient Ocean 3 - 0C11469C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ambient Ocean 2 (0C11131C)](#trigger-0c11131c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 56 (cell 113, 60).
2. Play sound _Amb_OceanHeavy at waypoint 57 (cell 106, 44).
3. Play sound _Amb_OceanHeavy at waypoint 58 (cell 93, 29).
4. Play sound _Amb_OceanHeavy at waypoint 59 (cell 82, 17).
5. Play sound _Amb_OceanHeavy at waypoint 0 (cell 136, 153).
6. Play sound _Amb_OceanHeavy at waypoint 3 (cell 133, 140).
7. Play sound _Amb_OceanHeavy at waypoint 5 (cell 134, 129).
8. Play sound _Amb_OceanHeavy at waypoint 12 (cell 132, 112).
9. Play sound _Amb_OceanHeavy at waypoint 8 (cell 131, 120).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5434, Events line 5490, Actions line 5546.

<a id="trigger-0a2aaa7c"></a>

### 51. Ambient Wind 1 - 0A2AAA7C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ambient Ocean 3 (0C11469C)](#trigger-0c11469c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 11 (cell 128, 132).
2. Play sound _Amb_WindCold at waypoint 98 (cell 176, 114).
3. Play sound _Amb_WindCold at waypoint 16 (cell 166, 122).
4. Play sound _Amb_WindCold at waypoint 17 (cell 168, 112).
5. Play sound _Amb_WindCold at waypoint 29 (cell 170, 100).
6. Play sound _Amb_WindCold at waypoint 60 (cell 115, 131).
7. Play sound _Amb_WindCold at waypoint 28 (cell 98, 125).
8. Play sound _Amb_WindCold at waypoint 61 (cell 107, 121).
9. Play sound _Amb_WindCold at waypoint 62 (cell 112, 106).
10. Play sound _Amb_WindCold at waypoint 63 (cell 114, 96).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5435, Events line 5491, Actions line 5547.

<a id="trigger-0644420c"></a>

### 52. Ambient Wind 2 - 0644420C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ambient Wind 1 (0A2AAA7C)](#trigger-0a2aaa7c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 64 (cell 113, 82).
2. Play sound _Amb_WindCold at waypoint 65 (cell 106, 69).
3. Play sound _Amb_WindCold at waypoint 66 (cell 96, 56).
4. Play sound _Amb_WindCold at waypoint 67 (cell 82, 43).
5. Play sound _Amb_WindCold at waypoint 26 (cell 72, 29).
6. Play sound _Amb_WindCold at waypoint 68 (cell 71, 43).
7. Play sound _Amb_WindCold at waypoint 69 (cell 61, 43).
8. Play sound _Amb_WindCold at waypoint 70 (cell 55, 49).
9. Play sound _Amb_WindCold at waypoint 71 (cell 60, 59).
10. Play sound _Amb_WindCold at waypoint 72 (cell 47, 54).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5436, Events line 5492, Actions line 5548.

<a id="trigger-064454fc"></a>

### 53. Ambient Wind 3 - 064454FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ambient Wind 2 (0644420C)](#trigger-0644420c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 30 (cell 67, 68).
2. Play sound _Amb_WindCold at waypoint 73 (cell 79, 67).
3. Play sound _Amb_WindCold at waypoint 74 (cell 63, 82).
4. Play sound _Amb_WindCold at waypoint 75 (cell 38, 60).
5. Play sound _Amb_WindCold at waypoint 76 (cell 30, 69).
6. Play sound _Amb_WindCold at waypoint 77 (cell 26, 83).
7. Play sound _Amb_WindCold at waypoint 27 (cell 40, 87).
8. Play sound _Amb_WindCold at waypoint 78 (cell 39, 106).
9. Play sound _Amb_WindCold at waypoint 31 (cell 60, 121).
10. Play sound _Amb_WindCold at waypoint 79 (cell 123, 163).
11. Play sound _Amb_WindCold at waypoint 24 (cell 103, 160).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5437, Events line 5493, Actions line 5549.

<a id="trigger-064466bc"></a>

### 54. Ambient Wind 4 - 064466BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Ambient Wind 3 (064454FC)](#trigger-064454fc).

Attached scope: tag definitions 0C11140C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play sound _Amb_WindCold at waypoint 25 (cell 89, 150).
2. Play sound _Amb_WindCold at waypoint 32 (cell 84, 139).
3. Play sound _Amb_WindCold at waypoint 99 (cell 77, 122).
4. Play sound _Amb_WindCold at waypoint 80 (cell 76, 108).
5. Play sound _Amb_WindCold at waypoint 81 (cell 74, 91).
6. Play sound _Amb_WindCold at waypoint 82 (cell 84, 83).
7. Play sound _Amb_WindCold at waypoint 83 (cell 45, 73).
8. Play sound _Amb_WindCold at waypoint 84 (cell 98, 75).
9. Play sound _Amb_WindCold at waypoint 85 (cell 97, 92).

Source locator: MAPS02.MIX/sov12s.map; Triggers line 5438, Events line 5494, Actions line 5550.

[All team rosters and ordered plans](sov12s-teams.md) | [All mission overrides](sov12s-overrides.md)
