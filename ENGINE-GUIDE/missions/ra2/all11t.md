# Operation: Fallout

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** all11t.map. **Effective extracted member:** MAPS01.MIX/all11t.map. **Trigger definitions:** 102.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all11t-teams.md) | [All mission overrides](all11t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | TEMPERATE |
| Map size | 0,0,90,170 |
| Visible local rectangle | 10,5,75,95 |
| Placed vehicles | 35 |
| Placed infantry | 49 |
| Placed structures | 145 |
| Placed aircraft | 0 |
| Team templates | 95 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 100 | BadGuy1 |
| 2 | BadGuy2 House | 600 | BadGuy2 |
| 3 | BadGuy3 House | 100 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 0 | Other1 |
| 6 | Other2 House | 0 | Other2 |
| 7 | Other3 House | 0 | Other3 |
| 8 | House Elania | 0 | Elania |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Chronosphere Built,0 |
| 1 | Team Landed,0 |
| 2 | Team 2 Landed,0 |
| 3 | Anti-Oil Landed,0 |
| 4 | Oil Captured,0 |
| 5 | Team 3 Landed,0 |
| 6 | Team 2b Landed,0 |
| 7 | Team 3b Landed,0 |
| 8 | Team 3c Landed,0 |
| 9 | Anti-Oil 2 Landed,0 |
| 10 | Para 1 Landed,0 |
| 11 | Recur Invader 1a La,0 |
| 12 | Nuke Ready,0 |
| 13 | Got Gap,0 |
| 14 | Nuke2 Ready,0 |
| 15 | Civ Boat offscreen,0 |
| 16 | Recur 2a landed,0 |
| 17 | Recur 2b landed,0 |
| 18 | Low Power,0 |
| 19 | Mainland Bridge,0 |
| 20 | Base Island Bridge,0 |
| 21 | 1 CO Landed,0 |
| 22 | 2 CO Landed,0 |
| 23 | 3 CO Landed,0 |
| 24 | 4 CO Landed,0 |
| 25 | 5 CO Landed,0 |
| 26 | 6 CO Landed,0 |
| 27 | 1 CN Landed,0 |
| 28 | 2 CN Landed,0 |
| 29 | 3 CN Landed,0 |
| 30 | 4 CN Landed,0 |
| 31 | 5 CN Landed,0 |
| 32 | 6 CN Landed,0 |
| 33 | Chronosphere Up,0 |
| 34 | Nuke Win Go,0 |
| 35 | Dead Squid,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Win (Game Over) (0CD424DC)](#trigger-0cd424dc) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [_Loss (Game Over) (0A06B1BC)](#trigger-0a06b1bc) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-08a048f0"></a>

### 1. Reveal BG Base - 08A048F0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08A00E90 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Chronosphere Built) is set.

Flag writers in this mission: set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Easy) (09EDD83C)](#trigger-09edd83c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Med) (09EDD46C)](#trigger-09edd46c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Hard) (09EE6F3C)](#trigger-09ee6f3c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (CSphere Up) (09EE6A5C)](#trigger-09ee6a5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Resize Player View; main setting 0; parameter 1: 10, parameter 2: 5, parameter 3: 75, parameter 4: 155.
2. Supply reinforcement team [Sov Right Flank Patrol (0BCC8AD0)](all11t-teams.md#team-0bcc8ad0).
3. Supply reinforcement team [Sov Left Flank Patrol (0BCD1810)](all11t-teams.md#team-0bcd1810).
4. Supply reinforcement team [BG2 Harvesters a (04186C8C)](all11t-teams.md#team-04186c8c).
5. Supply reinforcement team [BG2 Harvesters b (0BA595AC)](all11t-teams.md#team-0ba595ac).
6. Enable and reset applicable timers for [BG2 AITrig & Prod Start (0BCDB040)](#trigger-0bcdb040).
7. Enable and reset applicable timers for [Win (Nukes KIA) Enabler (07A1260C)](#trigger-07a1260c).
8. Enable and reset applicable timers for [Play 1st Romanov Movie (0A9CD77C)](#trigger-0a9cd77c).
9. Supply reinforcement team [BG2 ParaTeam 6 (0877B26C)](all11t-teams.md#team-0877b26c).
10. Enable and reset applicable timers for [1st Teams Go (0ADC130C)](#trigger-0adc130c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9409, Events line 9513, Actions line 9617.

<a id="trigger-0bcdb040"></a>

### 2. BG2 AITrig & Prod Start - 0BCDB040

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reveal BG Base (08A048F0)](#trigger-08a048f0).

Attached scope: tag definitions 0BCDBD20 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Production Begins: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
2. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
3. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9410, Events line 9514, Actions line 9618.

<a id="trigger-07a1260c"></a>

### 3. Win (Nukes KIA) Enabler - 07A1260C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reveal BG Base (08A048F0)](#trigger-08a048f0).

Attached scope: tag definitions 079FF99C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Win (Nukes KIA) (0BA9F670)](#trigger-0ba9f670).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9411, Events line 9515, Actions line 9619.

<a id="trigger-0a9cd77c"></a>

### 4. Play 1st Romanov Movie - 0A9CD77C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reveal BG Base (08A048F0)](#trigger-08a048f0).

Attached scope: tag definitions 0A9CD3DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 63 (cell 189, 199).
2. Play sound CameraSwitch.
3. Play in-game movie with game pause 73.
4. Enable and reset applicable timers for [Return Camera to CU (0C9771AC)](#trigger-0c9771ac).
5. Disable player input.

Source locator: MAPS01.MIX/all11t.map; Triggers line 9412, Events line 9516, Actions line 9620.

<a id="trigger-0adc130c"></a>

### 5. 1st Teams Go - 0ADC130C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reveal BG Base (08A048F0)](#trigger-08a048f0); enable from [3rd Teams Go (0A77D05C)](#trigger-0a77d05c).

Attached scope: tag definitions 0ADC0B6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [300CN Team (0B0A448C)](all11t-teams.md#team-0b0a448c).
2. Supply reinforcement team [300CO Team (0B0A493C)](all11t-teams.md#team-0b0a493c).
3. Enable and reset applicable timers for [2nd Teams Go (0B65103C)](#trigger-0b65103c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9413, Events line 9517, Actions line 9621.

<a id="trigger-0ba9f670"></a>

### 6. Win (Nukes KIA) - 0BA9F670

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win (Nukes KIA) Enabler (07A1260C)](#trigger-07a1260c).

Attached scope: Nuclear Missile Silo (NAMISL), owner BadGuy1 House, cell (184, 202), tag 0BA99E80, persistence mode 1; Nuclear Missile Silo (NAMISL), owner BadGuy1 House, cell (186, 196), tag 0BA99E80, persistence mode 1; Nuclear Missile Silo (NAMISL), owner BadGuy1 House, cell (192, 194), tag 0BA99E80, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Win (Play Movie) (0AD6F94C)](#trigger-0ad6f94c).
2. Disable [Objective 1 Statement (0A9513BC)](#trigger-0a9513bc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9414, Events line 9518, Actions line 9622.

<a id="trigger-0c9771ac"></a>

### 7. Return Camera to CU - 0C9771AC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Play 1st Romanov Movie (0A9CD77C)](#trigger-0a9cd77c).

Attached scope: tag definitions 0C977E9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Jump the camera to waypoint 98 (cell 110, 102).
2. Play sound CameraSwitch.
3. Enable player input.

Source locator: MAPS01.MIX/all11t.map; Triggers line 9415, Events line 9519, Actions line 9623.

<a id="trigger-0b65103c"></a>

### 8. 2nd Teams Go - 0B65103C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [1st Teams Go (0ADC130C)](#trigger-0adc130c).

Attached scope: tag definitions 0B65C04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [600CO Team (0B0A559C)](all11t-teams.md#team-0b0a559c).
2. Supply reinforcement team [600CN Team (0B0A67BC)](all11t-teams.md#team-0b0a67bc).
3. Enable and reset applicable timers for [3rd Teams Go (0A77D05C)](#trigger-0a77d05c).
4. Supply reinforcement team [BG2 ParaTeam 5 (087AF6AC)](all11t-teams.md#team-087af6ac).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9416, Events line 9520, Actions line 9624.

<a id="trigger-0ad6f94c"></a>

### 9. Win (Play Movie) - 0AD6F94C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win (Nukes KIA) (0BA9F670)](#trigger-0ba9f670).

Attached scope: tag definitions 0AD709BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 2 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie with game pause 74.
2. Enable and reset applicable timers for [Win (Nukes All Finished) (0B3EA4FC)](#trigger-0b3ea4fc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9417, Events line 9521, Actions line 9625.

<a id="trigger-0a9513bc"></a>

### 10. Objective 1 Statement - 0A9513BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 1 Statement Enable (0A9519EC)](#trigger-0a9519ec).

Attached scope: tag definitions 0A957F4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 120 configured time units have elapsed since the trigger timer was initialized/reset.
2. local flag 33 (Chronosphere Up) is clear.

Flag writers in this mission: set local flag 33 (Chronosphere Up) at [Chronosphere is Built (0B5E803C)](#trigger-0b5e803c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Display message “Objective 1: Construct a Chronosphere” (MISSION:All11d).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9418, Events line 9522, Actions line 9626.

<a id="trigger-0a77d05c"></a>

### 11. 3rd Teams Go - 0A77D05C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [2nd Teams Go (0B65103C)](#trigger-0b65103c).

Attached scope: tag definitions 0A77EB8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [900CN Team (0B0A630C)](all11t-teams.md#team-0b0a630c).
2. Supply reinforcement team [900CO Team (0B0A7C8C)](all11t-teams.md#team-0b0a7c8c).
3. Enable and reset applicable timers for [1st Teams Go (0ADC130C)](#trigger-0adc130c).
4. Supply reinforcement team [BG2 ParaTeam 6 (0877B26C)](all11t-teams.md#team-0877b26c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9419, Events line 9523, Actions line 9627.

<a id="trigger-0b3ea4fc"></a>

### 12. Win (Nukes All Finished) - 0B3EA4FC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win (Play Movie) (0AD6F94C)](#trigger-0ad6f94c).

Attached scope: tag definitions 0B3E9EAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 8 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Set local flag 34 (Nuke Win Go).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9420, Events line 9524, Actions line 9628.

<a id="trigger-0ad71f3c"></a>

### 13. Win (Cheer) - 0AD71F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AD721BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 34 (Nuke Win Go) is set.

Flag writers in this mission: set local flag 34 (Nuke Win Go) at [Win (Nukes All Finished) (0B3EA4FC)](#trigger-0b3ea4fc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).
2. Enable and reset applicable timers for [Win (Game Over) (0CD424DC)](#trigger-0cd424dc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9421, Events line 9525, Actions line 9629.

<a id="trigger-0cd424dc"></a>

### 14. Win (Game Over) - 0CD424DC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Win (Cheer) (0AD71F3C)](#trigger-0ad71f3c).

Attached scope: tag definitions 0CD43EEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all11t.map; Triggers line 9422, Events line 9526, Actions line 9630.

<a id="trigger-0bcd1030"></a>

### 15. Create BG Defense Teams - 0BCD1030

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BCD0C80 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Chronosphere Built) is set.

Flag writers in this mission: set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Easy) (09EDD83C)](#trigger-09edd83c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Med) (09EDD46C)](#trigger-09edd46c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Hard) (09EE6F3C)](#trigger-09ee6f3c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (CSphere Up) (09EE6A5C)](#trigger-09ee6a5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [_WDefense Dolphin (0418E94C)](all11t-teams.md#team-0418e94c).
2. Supply reinforcement team [_WDefense Destroyer (0418E4CC)](all11t-teams.md#team-0418e4cc).
3. Create/recruit team [_Defense Spy (0D1516AC)](all11t-teams.md#team-0d1516ac).
4. Create/recruit team [_Defense Infantry (0D150DEC)](all11t-teams.md#team-0d150dec).
5. Create/recruit team [_Defense Lt Armor (0D1511FC)](all11t-teams.md#team-0d1511fc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9423, Events line 9527, Actions line 9631.

<a id="trigger-0bcceb50"></a>

### 16. Nuke Silos to BG2 - 0BCCEB50

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BCCE950 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Chronosphere Built) is set.

Flag writers in this mission: set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Easy) (09EDD83C)](#trigger-09edd83c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Med) (09EDD46C)](#trigger-09edd46c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Hard) (09EE6F3C)](#trigger-09ee6f3c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (CSphere Up) (09EE6A5C)](#trigger-09ee6a5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).
2. Display message “WARNING: Soviet Nuclear Missiles are now” (MISSION:All11c1).
3. Display message “being armed” (MISSION:All11c2).
4. Enable and reset applicable timers for [Objective 2 Statement (0A0C951C)](#trigger-0a0c951c).
5. Play voice notification EVA_NewObjectiveReceived.

Source locator: MAPS01.MIX/all11t.map; Triggers line 9424, Events line 9528, Actions line 9632.

<a id="trigger-0a0c951c"></a>

### 17. Objective 2 Statement - 0A0C951C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Nuke Silos to BG2 (0BCCEB50)](#trigger-0bcceb50).

Attached scope: tag definitions 0A0CDDEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Neutralize the Soviet Nuclear” (MISSION:All11e1).
2. Display message “Missile Silos” (MISSION:All11e2).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9425, Events line 9529, Actions line 9633.

<a id="trigger-09d97560"></a>

### 18. BG2 Initial Patrols - 09D97560

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09D93D10 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 62 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Squid Patrol (0BA6672C)](all11t-teams.md#team-0ba6672c).
2. Create/recruit team [BG2 Sub Patrol (0BA6627C)](all11t-teams.md#team-0ba6627c).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9426, Events line 9530, Actions line 9634.

<a id="trigger-09e5a2a0"></a>

### 19. BG2 Invader 1 Go t=90 - 09E5A2A0

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09E5BCD0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 Invader 1 (09EF548C)](all11t-teams.md#team-09ef548c).
2. Supply reinforcement team [BG2 Invader 1 Escort (0B07348C)](all11t-teams.md#team-0b07348c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9427, Events line 9531, Actions line 9635.

<a id="trigger-09e5bbf0"></a>

### 20. BG2 Invader 1a Go - 09E5BBF0

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09E5B850 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Team Landed) is set.

Flag writers in this mission: clear local flag 1 (Team Landed) at [BG2 Invader 1a Go (09E5BBF0)](#trigger-09e5bbf0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Invader 1a (0879D48C)](all11t-teams.md#team-0879d48c).
2. Clear local flag 1 (Team Landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9428, Events line 9532, Actions line 9636.

<a id="trigger-09fce390"></a>

### 21. BG2 Para 1 Go (t=150) - 09FCE390

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09FCFE30 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 150 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 ParaTeam 1 (0879C3EC)](all11t-teams.md#team-0879c3ec).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9429, Events line 9533, Actions line 9637.

<a id="trigger-0999c740"></a>

### 22.  BG2 Invader 2 Go t=240 - 0999C740

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0999E600 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 240 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 Invader 2-1 (0AE7CAA0)](all11t-teams.md#team-0ae7caa0).
2. Supply reinforcement team [BG2 Invader 2-2 (0AE78630)](all11t-teams.md#team-0ae78630).
3. Supply reinforcement team [BG2 Invader 2 Escort (0AEA72D0)](all11t-teams.md#team-0aea72d0).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9430, Events line 9534, Actions line 9638.

<a id="trigger-0999e450"></a>

### 23.  BG2 Invader 2a Go - 0999E450

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0999E2E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Team 2 Landed) is set.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Invader 2a (0879B7DC)](all11t-teams.md#team-0879b7dc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9431, Events line 9535, Actions line 9639.

<a id="trigger-0999aab0"></a>

### 24. BG2 Anti-Oil Team Enable 1 - 0999AAB0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 71 (global list position: Tech Oil Derrick (CAOILD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 4 (Oil Captured).
2. Enable and reset applicable timers for [BG2 Anti-Oil Team Go (0999A680)](#trigger-0999a680).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9432, Events line 9536, Actions line 9640.

<a id="trigger-0999a680"></a>

### 25. BG2 Anti-Oil Team Go - 0999A680

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG2 Anti-Oil Team Enable 1 (0999AAB0)](#trigger-0999aab0); enable from [BG2 Anti-Oil Team Enable 2 (time) (089FD960)](#trigger-089fd960).

Attached scope: tag definitions 0999A360 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. A random delay centered on 60 configured time units expires (the editor describes a 50%-150% range).

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 Anti-Oil Team-1 (08C802A0)](all11t-teams.md#team-08c802a0).
2. Supply reinforcement team [BG2 Anti-Oil Team-2 (0BBFA43C)](all11t-teams.md#team-0bbfa43c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9433, Events line 9537, Actions line 9641.

<a id="trigger-0999a1e0"></a>

### 26. BG2 Anti-Oil Team a Go - 0999A1E0

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 099A0F50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Anti-Oil Landed) is set.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Anti-Oil Team a (0879995C)](all11t-teams.md#team-0879995c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9434, Events line 9538, Actions line 9642.

<a id="trigger-099baf40"></a>

### 27.  BG2 Invader 3 Go (battlelab up) - 099BAF40

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 099C20C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 6 (global list position: Allied Battle Lab (GATECH)). A map-local type-list change can affect index interpretation.
2. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 Invader 3-2 (0D15A1FC)](all11t-teams.md#team-0d15a1fc).
2. Supply reinforcement team [BG2 Invader 3 Escorts (093BE580)](all11t-teams.md#team-093be580).
3. Supply reinforcement team [BG2 Invader 3-1 (0D15BA4C)](all11t-teams.md#team-0d15ba4c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9435, Events line 9539, Actions line 9643.

<a id="trigger-099c32c0"></a>

### 28.  BG2 Invader 3a - 099C32C0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. local flag 5 (Team 3 Landed) is set.

Flag writers in this mission: clear local flag 5 (Team 3 Landed) at [BG2 Invader 3c Go (09EC92C0)](#trigger-09ec92c0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Invader 3a (0D15B59C)](all11t-teams.md#team-0d15b59c).
2. Create/recruit team [BG2 Invader 3b (0D15AEFC)](all11t-teams.md#team-0d15aefc).
3. Create/recruit team [BG2 Invader 3c (0D15AA4C)](all11t-teams.md#team-0d15aa4c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9436, Events line 9540, Actions line 9644.

<a id="trigger-b"></a>

### 29. BG2 Invader 3a Go - B

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 099C89A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 5 (Team 3 Landed) is set.

Flag writers in this mission: clear local flag 5 (Team 3 Landed) at [BG2 Invader 3c Go (09EC92C0)](#trigger-09ec92c0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Invader 3a (0D15B59C)](all11t-teams.md#team-0d15b59c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9437, Events line 9541, Actions line 9645.

<a id="trigger-09ecabd0"></a>

### 30. BG2 Invader 2b Go - 09ECABD0

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09ECAA20 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 6 (Team 2b Landed) is set.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Invader 2b (0879B32C)](all11t-teams.md#team-0879b32c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9438, Events line 9542, Actions line 9646.

<a id="trigger-09ec95b0"></a>

### 31. BG2 Invader 3b Go - 09EC95B0

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09EC9430 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (Team 3b Landed) is set.

Flag writers in this mission: clear local flag 7 (Team 3b Landed) at [BG2 Invader 3c Go (09EC92C0)](#trigger-09ec92c0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Invader 3b (0D15AEFC)](all11t-teams.md#team-0d15aefc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9439, Events line 9543, Actions line 9647.

<a id="trigger-09ec92c0"></a>

### 32. BG2 Invader 3c Go - 09EC92C0

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09EC91F0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 7 (Team 3b Landed) is set.
2. local flag 5 (Team 3 Landed) is set.

Flag writers in this mission: clear local flag 7 (Team 3b Landed) at [BG2 Invader 3c Go (09EC92C0)](#trigger-09ec92c0); clear local flag 5 (Team 3 Landed) at [BG2 Invader 3c Go (09EC92C0)](#trigger-09ec92c0). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Invader 3c (0D15AA4C)](all11t-teams.md#team-0d15aa4c).
2. Clear local flag 5 (Team 3 Landed).
3. Clear local flag 7 (Team 3b Landed).
4. Clear local flag 8 (Team 3c Landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9440, Events line 9544, Actions line 9648.

<a id="trigger-09ec9880"></a>

### 33. BG2 Anti-Oil Team b GO - 09EC9880

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09ECBD90 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 9 (Anti-Oil 2 Landed) is set.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Anti-Oil Team b (0879EEFC)](all11t-teams.md#team-0879eefc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9441, Events line 9545, Actions line 9649.

<a id="trigger-09edabb0"></a>

### 34. BG2 Seaborn Attk Go (warfactory up) - 09EDABB0

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09EDA920 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 7 (global list position: Allied War Factory (GAWEAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 Seaborn Attack (09C011FC)](all11t-teams.md#team-09c011fc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9442, Events line 9546, Actions line 9650.

<a id="trigger-093a04f0"></a>

### 35.  BG2 ParaTeam 2 - 093A04F0

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 ParaTeam 2 (087A247C)](all11t-teams.md#team-087a247c).
2. Supply reinforcement team [BG2 ParaTeam 3 (087A223C)](all11t-teams.md#team-087a223c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9443, Events line 9547, Actions line 9651.

<a id="trigger-3-go"></a>

### 36. BG2 Para 2&3 Go (t=360) Hard - 3 GO

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 360 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 ParaTeam 2 (087A247C)](all11t-teams.md#team-087a247c).
2. Supply reinforcement team [BG2 ParaTeam 3 (087A223C)](all11t-teams.md#team-087a223c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9444, Events line 9548, Actions line 9652.

<a id="trigger-089fd960"></a>

### 37. BG2 Anti-Oil Team Enable 2 (time) - 089FD960

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [BG2 Anti-Oil Team Enable 1 (0999AAB0)](#trigger-0999aab0).

Attached scope: tag definitions 0999A760 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG2 Anti-Oil Team Go (0999A680)](#trigger-0999a680).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9445, Events line 9549, Actions line 9653.

<a id="trigger-0ae6c0d0"></a>

### 38. First Squid Attack (t=5) - 0AE6C0D0

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AE620E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Civ Boat (0C54E59C)](all11t-teams.md#team-0c54e59c).
2. Create/recruit team [First Squid Attk (0BCAF21C)](all11t-teams.md#team-0bcaf21c).
3. Make enemy: owner selector 18 (country/type OTHER1; placed owner Other1 House).
4. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
5. Move the camera to waypoint 94 (cell 97, 119) with speed setting 2.

Source locator: MAPS01.MIX/all11t.map; Triggers line 9446, Events line 9550, Actions line 9654.

<a id="trigger-0ae750e0"></a>

### 39. Civ Call for Help - 0AE750E0

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Cruise Ship (CRUISE), owner Other1 House, cell (88, 115), tag 0AE73770, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.
2. local flag 35 (Dead Squid) is clear.

Flag writers in this mission: set local flag 35 (Dead Squid) at [Dead Squid (0DC801EC)](#trigger-0dc801ec). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 50 (cell 103, 129).
2. Enable and reset applicable timers for [Squid Explanation (0AE9139C)](#trigger-0ae9139c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9447, Events line 9551, Actions line 9655.

<a id="trigger-0ae9139c"></a>

### 40. Squid Explanation - 0AE9139C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Civ Call for Help (0AE750E0)](#trigger-0ae750e0).

Attached scope: tag definitions 0AE90B6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play in-game movie 104.
2. Enable and reset applicable timers for [Dolphin Explanation (0AE8F44C)](#trigger-0ae8f44c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9448, Events line 9552, Actions line 9656.

<a id="trigger-0ae8f44c"></a>

### 41. Dolphin Explanation - 0AE8F44C

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Squid Explanation (0AE9139C)](#trigger-0ae9139c).

Attached scope: tag definitions 0AE8B72C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 21 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “HINT: To make SQUID release a ship, you” (MISSION:All11a1).
2. Create/recruit team [Dolphin Flashers! (0B3612CC)](all11t-teams.md#team-0b3612cc).
3. Display message “must force your DOLPHINS to fire on the” (MISSION:All11a2).
4. Display message “AFFECTED SHIP” (MISSION:All11a3).
5. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).
6. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9449, Events line 9553, Actions line 9657.

<a id="trigger-0ba99910"></a>

### 42. _Loss (Occurs) - 0BA99910

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BA995A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss (Game Over) (0A06B1BC)](#trigger-0a06b1bc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9450, Events line 9554, Actions line 9658.

<a id="trigger-0a06b1bc"></a>

### 43. _Loss (Game Over) - 0A06B1BC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Loss (Occurs) (0BA99910)](#trigger-0ba99910).

Attached scope: tag definitions 09F866CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all11t.map; Triggers line 9451, Events line 9555, Actions line 9659.

<a id="trigger-0d5f4220"></a>

### 44. ParaTeam 4 (t=t+420) - 0D5F4220

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Persistent Teams (0DB6A7EC)](#trigger-0db6a7ec).

Attached scope: tag definitions 0D5F19D0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 420 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 ParaTeam 4 (087AA6AC)](all11t-teams.md#team-087aa6ac).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9452, Events line 9556, Actions line 9660.

<a id="trigger-0d5f1860"></a>

### 45. _AAA Disable Recursives - 0D5F1860

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D5F7920 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Chronosphere Built) is set.

Flag writers in this mission: set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Easy) (09EDD83C)](#trigger-09edd83c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Med) (09EDD46C)](#trigger-09edd46c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Hard) (09EE6F3C)](#trigger-09ee6f3c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (CSphere Up) (09EE6A5C)](#trigger-09ee6a5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Disable [Recur Invader 2a (t=300) (0A3B0160)](#trigger-0a3b0160).
2. Disable [ Invader 2b (t=t+450) (0A390C80)](#trigger-0a390c80).
3. Disable [Recur Invader 1 (t=t+300) (0BB1A4D0)](#trigger-0bb1a4d0).
4. Disable [Sea Attk (t=t+625) (0BB1C5E0)](#trigger-0bb1c5e0).
5. Disable [ParaTeam 5 (t=t+500) (09B465EC)](#trigger-09b465ec).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9453, Events line 9557, Actions line 9661.

<a id="trigger-0a3b0160"></a>

### 46. Recur Invader 2a (t=300) - 0A3B0160

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Persistent Teams (0DB6A7EC)](#trigger-0db6a7ec).

Attached scope: tag definitions 0A3B6520 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Recur Invader 2a (0A391780)](all11t-teams.md#team-0a391780).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9454, Events line 9558, Actions line 9662.

<a id="trigger-0a390c80"></a>

### 47.  Invader 2b (t=t+450) - 0A390C80

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Persistent Teams (0DB6A7EC)](#trigger-0db6a7ec).

Attached scope: tag definitions 0A39A030 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 450 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Recur Invader 2b (0A3B1C10)](all11t-teams.md#team-0a3b1c10).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9455, Events line 9559, Actions line 9663.

<a id="trigger-0bb1a4d0"></a>

### 48. Recur Invader 1 (t=t+300) - 0BB1A4D0

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Persistent Teams (0DB6A7EC)](#trigger-0db6a7ec).

Attached scope: tag definitions 0BB1DCA0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Recur Invader 1a (0AEE07DC)](all11t-teams.md#team-0aee07dc).
2. Supply reinforcement team [Recur Invader 1 escort (0A41CEFC)](all11t-teams.md#team-0a41cefc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9456, Events line 9560, Actions line 9664.

<a id="trigger-0bb1c5e0"></a>

### 49. Sea Attk (t=t+625) - 0BB1C5E0

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Persistent Teams (0DB6A7EC)](#trigger-0db6a7ec).

Attached scope: tag definitions 0BB18850 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 625 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Sea Attk (09C167DC)](all11t-teams.md#team-09c167dc).
2. Supply reinforcement team [BG2 Squid Patrol (0BA6672C)](all11t-teams.md#team-0ba6672c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9457, Events line 9561, Actions line 9665.

<a id="trigger-09b465ec"></a>

### 50. ParaTeam 5 (t=t+500) - 09B465EC

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Persistent Teams (0DB6A7EC)](#trigger-0db6a7ec).

Attached scope: tag definitions 09B43BEC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 500 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 ParaTeam 5 (087AF6AC)](all11t-teams.md#team-087af6ac).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9458, Events line 9562, Actions line 9666.

<a id="trigger-0a067260"></a>

### 51. Invader 1 Onshore - 0A067260

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A067F50 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 11 (Recur Invader 1a La) is set.

Flag writers in this mission: clear local flag 11 (Recur Invader 1a La) at [Invader 1 Onshore (0A067260)](#trigger-0a067260). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Recur Invader 1a-Landed (0AEE6EFC)](all11t-teams.md#team-0aee6efc).
2. Clear local flag 11 (Recur Invader 1a La).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9459, Events line 9563, Actions line 9667.

<a id="trigger-0bae9210"></a>

### 52. Got Gap Generator? - 0BAE9210

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BAE3070 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 63 (global list position: Gap Generator (GAGAP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 13 (Got Gap).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9460, Events line 9564, Actions line 9668.

<a id="trigger-0baf16f0"></a>

### 53. NUKE Targeting 1 - 0BAF16F0

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Reveal Nukes (0A3C7E40)](#trigger-0a3c7e40).

Attached scope: tag definitions 0BAF71D0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 710 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Preferred target; main setting 7.
2. Enable and reset applicable timers for [NUKE Targeting 2 (0BAF6240)](#trigger-0baf6240).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9461, Events line 9565, Actions line 9669.

<a id="trigger-0baf6240"></a>

### 54. NUKE Targeting 2 - 0BAF6240

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [NUKE Targeting 1 (0BAF16F0)](#trigger-0baf16f0).

Attached scope: tag definitions 0BAF1080 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 720 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Preferred target; main setting 9.
2. Enable and reset applicable timers for [NUKE Targeting 3+ (0BAEB340)](#trigger-0baeb340).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9462, Events line 9566, Actions line 9670.

<a id="trigger-0baeb340"></a>

### 55. NUKE Targeting 3+ - 0BAEB340

Owner reference: BadGuy2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [NUKE Targeting 2 (0BAF6240)](#trigger-0baf6240).

Attached scope: tag definitions 0BAF76A0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 720 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Preferred target; main setting 6; location/duration field BI.

Source locator: MAPS01.MIX/all11t.map; Triggers line 9463, Events line 9567, Actions line 9671.

<a id="trigger-0a353800"></a>

### 56. Make sure Civ Boat is gone - 0A353800

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A36E190 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 15 (Civ Boat offscreen) is clear.
2. 60 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Civ Boat (0C54E59C)](all11t-teams.md#team-0c54e59c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9464, Events line 9568, Actions line 9672.

<a id="trigger-0a3c7e40"></a>

### 57. Reveal Nukes - 0A3C7E40

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A3C6720 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Chronosphere Built) is set.

Flag writers in this mission: set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Easy) (09EDD83C)](#trigger-09edd83c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Med) (09EDD46C)](#trigger-09edd46c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Hard) (09EE6F3C)](#trigger-09ee6f3c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (CSphere Up) (09EE6A5C)](#trigger-09ee6a5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 48 (cell 197, 207).
2. Reveal terrain around waypoint 15 (cell 181, 207).
3. Reveal terrain around waypoint 14 (cell 183, 193).
4. Reveal terrain around waypoint 16 (cell 197, 191).
5. Reveal terrain around waypoint 63 (cell 189, 199).
6. Create radar-event marker type 5 at waypoint 63 (cell 189, 199).
7. Enable and reset applicable timers for [NUKE Targeting 1 (0BAF16F0)](#trigger-0baf16f0).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9465, Events line 9569, Actions line 9673.

<a id="trigger-0a95e08c"></a>

### 58. Chronosphere Hint - 0A95E08C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Chronosphere is Built (0B5E803C)](#trigger-0b5e803c).

Attached scope: tag definitions 0A95FE0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 290 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “HINT: The CHRONOSPHERE will teleport all” (MISSION:All11b1).
2. Display message “VEHICLES within a small area across any distance” (MISSION:All11b2).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9466, Events line 9570, Actions line 9674.

<a id="trigger-0a3b3c10"></a>

### 59. Invader 2a Landed - 0A3B3C10

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A3B3B00 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 16 (Recur 2a landed) is set.

Flag writers in this mission: clear local flag 16 (Recur 2a landed) at [Invader 2a Landed (0A3B3C10)](#trigger-0a3b3c10). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Recur Invader 2a Landed (0A3AD940)](all11t-teams.md#team-0a3ad940).
2. Clear local flag 16 (Recur 2a landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9467, Events line 9571, Actions line 9675.

<a id="trigger-0a2e7b30"></a>

### 60.  Invader 2b Landed - 0A2E7B30

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A36E4A0 (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 17 (Recur 2b landed) is set.

Flag writers in this mission: clear local flag 17 (Recur 2b landed) at [ Invader 2b Landed (0A2E7B30)](#trigger-0a2e7b30). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Recur Invader 2b Landed (08C8E2A0)](all11t-teams.md#team-08c8e2a0).
2. Clear local flag 17 (Recur 2b landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9468, Events line 9572, Actions line 9676.

<a id="trigger-0a3cef40"></a>

### 61. Reveal Known Areas - 0A3CEF40

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A3CAC30 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 32 (cell 124, 83).
2. Reveal terrain around waypoint 67 (cell 74, 62).
3. Reveal terrain around waypoint 66 (cell 110, 85).
4. Reveal terrain around waypoint 52 (cell 132, 87).
5. Reveal terrain around waypoint 53 (cell 123, 113).
6. Reveal terrain around waypoint 42 (cell 64, 62).
7. Reveal terrain around waypoint 60 (cell 72, 76).
8. Reveal terrain around waypoint 68 (cell 118, 92).
9. Reveal terrain around waypoint 69 (cell 126, 99).
10. Reveal terrain around waypoint 70 (cell 83, 54).
11. Reveal terrain around waypoint 71 (cell 75, 32).
12. Reveal terrain around waypoint 72 (cell 49, 60).
13. Reveal terrain around waypoint 73 (cell 75, 43).
14. Reveal terrain around waypoint 74 (cell 68, 50).
15. Reveal terrain around waypoint 75 (cell 58, 49).
16. Reveal terrain around waypoint 76 (cell 66, 43).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9469, Events line 9573, Actions line 9677.

<a id="trigger-0a9519ec"></a>

### 62. Objective 1 Statement Enable - 0A9519EC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A9514AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Objective 1 Statement (0A9513BC)](#trigger-0a9513bc).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9470, Events line 9574, Actions line 9678.

<a id="trigger-0a952a2c"></a>

### 63. Play Crickets Sounds - 0A952A2C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A95094C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_CricketBed at waypoint 85 (cell 65, 82).
2. Play sound _Amb_CricketBed at waypoint 86 (cell 44, 77).
3. Play sound _Amb_CricketBed at waypoint 56 (cell 50, 101).
4. Play sound _Amb_CricketBed at waypoint 47 (cell 64, 123).
5. Play sound _Amb_CricketBed at waypoint 55 (cell 67, 102).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9471, Events line 9575, Actions line 9679.

<a id="trigger-0a95072c"></a>

### 64. Play Beach Birds Sounds - 0A95072C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A9503CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsBeach at waypoint 51 (cell 80, 60).
2. Play sound _Amb_BirdsBeach at waypoint 71 (cell 75, 32).
3. Play sound _Amb_BirdsBeach at waypoint 52 (cell 132, 87).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9472, Events line 9576, Actions line 9680.

<a id="trigger-0a9502dc"></a>

### 65. Play Harbor Birds Sounds - 0A9502DC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A9500DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsHarbor at waypoint 82 (cell 103, 108).
2. Play sound _Amb_BirdsHarbor at waypoint 83 (cell 170, 186).
3. Play sound _Amb_BirdsHarbor at waypoint 84 (cell 183, 178).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9473, Events line 9577, Actions line 9681.

<a id="trigger-0a94e12c"></a>

### 66. Play Urban Murmur Sounds - 0A94E12C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A95544C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur2 at waypoint 76 (cell 66, 43).
2. Play sound _Amb_UrbanMurmur2 at waypoint 59 (cell 61, 57).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9474, Events line 9578, Actions line 9682.

<a id="trigger-0a95fbbc"></a>

### 67. Play Light Surf Sounds - 0A95FBBC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A95EF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 61 (cell 93, 46).
2. Play sound _Amb_OceanLight at waypoint 64 (cell 78, 35).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9475, Events line 9579, Actions line 9683.

<a id="trigger-0a95ed7c"></a>

### 68. Play Hvy Surf Sounds 1 - 0A95ED7C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A95F9AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 79 (cell 148, 203).
2. Play sound _Amb_OceanHeavy at waypoint 17 (cell 147, 179).
3. Play sound _Amb_OceanHeavy at waypoint 19 (cell 162, 166).
4. Play sound _Amb_OceanHeavy at waypoint 18 (cell 183, 153).
5. Play sound _Amb_OceanHeavy at waypoint 80 (cell 210, 141).
6. Play sound _Amb_OceanHeavy at waypoint 81 (cell 200, 148).
7. Play sound _Amb_OceanHeavy at waypoint 22 (cell 143, 96).
8. Play sound _Amb_OceanHeavy at waypoint 53 (cell 123, 113).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9476, Events line 9580, Actions line 9684.

<a id="trigger-0a95f8bc"></a>

### 69. Play Hvy Surf Sounds 2 - 0A95F8BC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A95E96C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 21 (cell 123, 128).
2. Play sound _Amb_OceanHeavy at waypoint 44 (cell 82, 89).
3. Play sound _Amb_OceanHeavy at waypoint 27 (cell 91, 81).
4. Play sound _Amb_OceanHeavy at waypoint 28 (cell 101, 65).
5. Play sound _Amb_OceanHeavy at waypoint 46 (cell 123, 65).
6. Play sound _Amb_OceanHeavy at waypoint 23 (cell 135, 71).
7. Play sound _Amb_OceanHeavy at waypoint 41 (cell 72, 122).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9477, Events line 9581, Actions line 9685.

<a id="trigger-08193f3c"></a>

### 70. Power transfer to Nuke - 08193F3C

Owner reference: BadGuy3. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08193C5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Chronosphere Built) is set.

Flag writers in this mission: set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Easy) (09EDD83C)](#trigger-09edd83c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Med) (09EDD46C)](#trigger-09edd46c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Hard) (09EE6F3C)](#trigger-09ee6f3c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (CSphere Up) (09EE6A5C)](#trigger-09ee6a5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. All change house: owner selector 15 (country/type BADGUY2; placed owner BadGuy2 House).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9478, Events line 9582, Actions line 9686.

<a id="trigger-0ad7fbac"></a>

### 71. Ack! They see us...Get'em! - 0AD7FBAC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AD7F45C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Chronosphere Built) is set.

Flag writers in this mission: set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Easy) (09EDD83C)](#trigger-09edd83c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Med) (09EDD46C)](#trigger-09edd46c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Hard) (09EE6F3C)](#trigger-09ee6f3c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (CSphere Up) (09EE6A5C)](#trigger-09ee6a5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 ParaTeam 1 (0879C3EC)](all11t-teams.md#team-0879c3ec).
2. Supply reinforcement team [BG2 ParaTeam 2 (087A247C)](all11t-teams.md#team-087a247c).
3. Supply reinforcement team [BG2 ParaTeam 3 (087A223C)](all11t-teams.md#team-087a223c).
4. Supply reinforcement team [BG2 ParaTeam 4 (087AA6AC)](all11t-teams.md#team-087aa6ac).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9479, Events line 9583, Actions line 9687.

<a id="trigger-0ad61b0c"></a>

### 72. Mainland Brdg Fixers 1 - 0AD61B0C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (91, 43); tag 0AD66F4C, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 19 (Mainland Bridge).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9480, Events line 9584, Actions line 9688.

<a id="trigger-0b09f59c"></a>

### 73. Mainland Brdg Fixers 2 - 0B09F59C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B09F16C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 19 (Mainland Bridge) is set.

Flag writers in this mission: set local flag 19 (Mainland Bridge) at [Mainland Brdg Fixers 1 (0AD61B0C)](#trigger-0ad61b0c); clear local flag 19 (Mainland Bridge) at [Mainland Brdg Fixers 2 (0B09F59C)](#trigger-0b09f59c); set local flag 19 (Mainland Bridge) at [Mainland Brdg Fixers 3 (0B0A0F3C)](#trigger-0b0a0f3c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Supply reinforcement team [Bridge to Mainland Up (0AF3DDEC)](all11t-teams.md#team-0af3ddec).
2. Clear local flag 19 (Mainland Bridge).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9481, Events line 9585, Actions line 9689.

<a id="trigger-0b0a0f3c"></a>

### 74. Mainland Brdg Fixers 3 - 0B0A0F3C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B0A09DC (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 19 (Mainland Bridge).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9482, Events line 9586, Actions line 9690.

<a id="trigger-0b93071c"></a>

### 75. Base Isle Brdg Fixers1 - 0B93071C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (110, 66); tag 0B93036C, persistence mode 2.

**Wait for the recorded events:**

1. Bridge destroyed. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 20 (Base Island Bridge).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9483, Events line 9587, Actions line 9691.

<a id="trigger-0b93027c"></a>

### 76. Base Isle Brdg Fixers2 - 0B93027C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B93EB8C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 20 (Base Island Bridge) is set.

Flag writers in this mission: set local flag 20 (Base Island Bridge) at [Base Isle Brdg Fixers1 (0B93071C)](#trigger-0b93071c); clear local flag 20 (Base Island Bridge) at [Base Isle Brdg Fixers2 (0B93027C)](#trigger-0b93027c); set local flag 20 (Base Island Bridge) at [Base Isle Brdg Fixers3 (0B93E94C)](#trigger-0b93e94c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Clear local flag 20 (Base Island Bridge).
2. Supply reinforcement team [Bridge to Base Isle Up (0AF3D93C)](all11t-teams.md#team-0af3d93c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9484, Events line 9588, Actions line 9692.

<a id="trigger-0b93e94c"></a>

### 77. Base Isle Brdg Fixers3 - 0B93E94C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B93E74C (persistence 1); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed by anything [not infiltrate]. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 20 (Base Island Bridge).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9485, Events line 9589, Actions line 9693.

<a id="trigger-081dd84c"></a>

### 78. Zone Defenders Go 1 - 081DD84C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Entered by: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Create/recruit team [Zone Defender 1 (081D57EC)](all11t-teams.md#team-081d57ec).
2. Create/recruit team [Zone Defender 2 (081DA76C)](all11t-teams.md#team-081da76c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9486, Events line 9590, Actions line 9694.

<a id="trigger-099aec2c"></a>

### 79. BG2 Base Response (M) - 099AEC2C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Base Response 1 (0B41CDEC)](all11t-teams.md#team-0b41cdec).
2. Create/recruit team [BG2 Base Response 2 (0B41C93C)](all11t-teams.md#team-0b41c93c).
3. Create/recruit team [BG2 Base Response 3 (0B41C48C)](all11t-teams.md#team-0b41c48c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9487, Events line 9591, Actions line 9695.

<a id="trigger-07f6786c"></a>

### 80. Zone Defenders Go 2 - 07F6786C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Zone Defenders Go 1 (081DD84C)](#trigger-081dd84c).

Attached scope: 221 tagged map cells: (208, 148), (209, 148), (206, 149), (207, 149), (208, 149), (209, 149), (210, 149), (211, 149), (212, 149), (213, 149), (214, 149), (215, 149), (223, 149), (224, 149), (234, 149), (206, 150), (215, 150), (216, 150), (217, 150), (218, 150), (219, 150), (220, 150), (221, 150), (222, 150), (223, 150), (224, 150), (225, 150), (226, 150), (227, 150), (228, 150), (229, 150), (230, 150), (231, 150), (232, 150), (233, 150), (234, 150), (205, 151), (206, 151), (205, 152), (198, 153), (199, 153), (200, 153), (201, 153), (202, 153), (203, 153), (204, 153), (205, 153), (196, 154), (197, 154), (198, 154), (196, 155), (197, 155), (197, 156), (197, 157), (196, 158), (197, 158), (196, 159), (197, 159), (198, 159), (198, 160), (198, 161), (191, 162), (192, 162), (198, 162), (191, 163), (192, 163), (193, 163), (194, 163), (197, 163), (198, 163), (191, 164), (192, 164), (194, 164), (197, 164), (192, 165), (194, 165), (195, 165), (196, 165), (197, 165), (192, 166), (192, 167), (192, 168), (192, 169), (192, 170), (192, 171), (192, 172), (192, 173), (193, 173), (193, 174), (193, 175), (188, 176), (189, 176), (190, 176), (191, 176), (192, 176), (193, 176), (186, 177), (187, 177), (188, 177), (186, 178), (174, 179), (175, 179), (176, 179), (177, 179), (178, 179), (179, 179), (180, 179), (186, 179), (187, 179), (172, 180), (173, 180), (174, 180), (180, 180), (187, 180), (172, 181), (180, 181), (181, 181), (182, 181), (187, 181), (172, 182), (182, 182), (185, 182), (186, 182), (187, 182), (172, 183), (182, 183), (183, 183), (184, 183), (185, 183), (172, 184), (172, 185), (172, 186), (171, 187), (172, 187), (159, 188), (160, 188), (161, 188), (162, 188), (163, 188), (164, 188), (171, 188), (157, 189), (158, 189), (159, 189), (164, 189), (165, 189), (166, 189), (167, 189), (168, 189), (169, 189), (170, 189), (171, 189), (157, 190), (157, 191), (157, 192), (157, 193), (157, 194), (157, 195), (156, 196), (157, 196), (156, 197), (157, 197), (158, 197), (158, 198), (158, 199), (156, 200), (157, 200), (158, 200), (156, 201), (154, 202), (155, 202), (156, 202), (154, 203), (154, 204), (154, 205), (154, 206), (154, 207), (153, 208), (154, 208), (153, 209), (154, 209), (155, 209), (155, 210), (141, 211), (142, 211), (143, 211), (144, 211), (145, 211), (146, 211), (147, 211), (155, 211), (141, 212), (147, 212), (155, 212), (141, 213), (147, 213), (148, 213), (149, 213), (155, 213), (141, 214), (149, 214), (150, 214), (151, 214), (152, 214), (153, 214), (154, 214), (155, 214), (141, 215), (141, 216), (141, 217), (142, 217), (142, 218), (142, 219), (141, 220), (142, 220), (141, 221), (141, 222), (141, 223), (139, 224), (140, 224), (141, 224); tag 081D9D0C, persistence mode 0.

**Wait for the recorded events:**

1. local flag 0 (Chronosphere Built) is set.
2. Build Unit Type: type index 0 (global list position: Allied Construction Vehicle (AMCV)). A map-local type-list change can affect index interpretation.

Flag writers in this mission: set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Easy) (09EDD83C)](#trigger-09edd83c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Med) (09EDD46C)](#trigger-09edd46c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (Hard) (09EE6F3C)](#trigger-09ee6f3c); set local flag 0 (Chronosphere Built) at [Heeeere's Cuuuba (CSphere Up) (09EE6A5C)](#trigger-09ee6a5c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [Zone Defender 1 (081D57EC)](all11t-teams.md#team-081d57ec).
2. Create/recruit team [Zone Defender 2 (081DA76C)](all11t-teams.md#team-081da76c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9488, Events line 9592, Actions line 9696.

<a id="trigger-09edd83c"></a>

### 81. Heeeere's Cuuuba (Easy) - 09EDD83C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1860 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set local flag 0 (Chronosphere Built).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9489, Events line 9593, Actions line 9697.

<a id="trigger-09edd46c"></a>

### 82. Heeeere's Cuuuba (Med) - 09EDD46C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Heeeere's Cuuuba (Easy) (09EDD83C)](#trigger-09edd83c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1260 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set local flag 0 (Chronosphere Built).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9490, Events line 9594, Actions line 9698.

<a id="trigger-09ee6f3c"></a>

### 83. Heeeere's Cuuuba (Hard) - 09EE6F3C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Heeeere's Cuuuba (Med) (09EDD46C)](#trigger-09edd46c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 960 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Set local flag 0 (Chronosphere Built).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9491, Events line 9595, Actions line 9699.

<a id="trigger-09ee6a5c"></a>

### 84. Heeeere's Cuuuba (CSphere Up) - 09EE6A5C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Heeeere's Cuuuba (Hard) (09EE6F3C)](#trigger-09ee6f3c).

Attached scope: tag definitions 09EDD55C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 27 (global list position: Chrono Sphere (GACSPH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 0 (Chronosphere Built).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9492, Events line 9596, Actions line 9700.

<a id="trigger-09f0874c"></a>

### 85. Reveal Known Areas Mk II - 09F0874C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09F0815C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 38 (cell 108, 156).
2. Reveal terrain around waypoint 34 (cell 113, 156).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9493, Events line 9597, Actions line 9701.

<a id="trigger-0c7cf10c"></a>

### 86. Stop CK Attackers - 0C7CF10C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM07), owner Civie1 House, cell (127, 89), tag 0C7D004C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [Recur Invader 1 (t=t+300) (0BB1A4D0)](#trigger-0bb1a4d0).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9494, Events line 9598, Actions line 9702.

<a id="trigger-07ee33fc"></a>

### 87. BG2 Para 2 Go (t=360) Easy - 07EE33FC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [BG2 Para 2&3 Go (t=360) Hard (3 Go)](#trigger-3-go).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 360 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 ParaTeam 2 (087A247C)](all11t-teams.md#team-087a247c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9495, Events line 9599, Actions line 9703.

<a id="trigger-07ee677c"></a>

### 88. BG2 Para 3 Go (t=360) Med - 07EE677C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [BG2 Para 2 Go (t=360) Easy (07EE33FC)](#trigger-07ee33fc).

Attached scope: tag definitions 093A4F50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 360 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [BG2 ParaTeam 3 (087A223C)](all11t-teams.md#team-087a223c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9496, Events line 9600, Actions line 9704.

<a id="trigger-0adc09cc"></a>

### 89. 300CO SAPC exit - 0ADC09CC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ADC07CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 21 (1 CO Landed) is set.

Flag writers in this mission: clear local flag 21 (1 CO Landed) at [300CO SAPC exit (0ADC09CC)](#trigger-0adc09cc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [300CO SAPC exit (0ADC069C)](all11t-teams.md#team-0adc069c).
2. Clear local flag 21 (1 CO Landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9497, Events line 9601, Actions line 9705.

<a id="trigger-0adc2c7c"></a>

### 90. 300CN SAPC exit - 0ADC2C7C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0ADC274C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 27 (1 CN Landed) is set.

Flag writers in this mission: clear local flag 27 (1 CN Landed) at [300CN SAPC exit (0ADC2C7C)](#trigger-0adc2c7c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [300CN SAPC exit (0ADB6A3C)](all11t-teams.md#team-0adb6a3c).
2. Clear local flag 27 (1 CN Landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9498, Events line 9602, Actions line 9706.

<a id="trigger-086c374c"></a>

### 91.  600CN SAPC exit - 086C374C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A858D6C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 28 (2 CN Landed) is set.

Flag writers in this mission: clear local flag 28 (2 CN Landed) at [ 600CN SAPC exit (086C374C)](#trigger-086c374c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [600CN SAPC exit (0A859B1C)](all11t-teams.md#team-0a859b1c).
2. Clear local flag 28 (2 CN Landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9499, Events line 9603, Actions line 9707.

<a id="trigger-0a858c7c"></a>

### 92.  600CO SAPC exit - 0A858C7C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A7789DC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 22 (2 CO Landed) is set.

Flag writers in this mission: clear local flag 22 (2 CO Landed) at [ 600CO SAPC exit (0A858C7C)](#trigger-0a858c7c). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [600CO SAPC exit (0A859EFC)](all11t-teams.md#team-0a859efc).
2. Clear local flag 22 (2 CO Landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9500, Events line 9604, Actions line 9708.

<a id="trigger-0b25fdbc"></a>

### 93. 900CO SAPC exit - 0B25FDBC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B25F7CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 23 (3 CO Landed) is set.

Flag writers in this mission: clear local flag 23 (3 CO Landed) at [900CO SAPC exit (0B25FDBC)](#trigger-0b25fdbc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [900CO SAPC exit (0A77BA3C)](all11t-teams.md#team-0a77ba3c).
2. Clear local flag 23 (3 CO Landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9501, Events line 9605, Actions line 9709.

<a id="trigger-0b25f6dc"></a>

### 94. 900CN SAPC exit - 0B25F6DC

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B25F23C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 29 (3 CN Landed) is set.

Flag writers in this mission: clear local flag 29 (3 CN Landed) at [900CN SAPC exit (0B25F6DC)](#trigger-0b25f6dc). Script steps can also change flags; see teams below.

**Then perform these actions in order:**

1. Create/recruit team [900CN SAPC exit (0A77D83C)](all11t-teams.md#team-0a77d83c).
2. Clear local flag 29 (3 CN Landed).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9502, Events line 9606, Actions line 9710.

<a id="trigger-0907f09c"></a>

### 95. BG2 Base Response (E) - 0907F09C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [BG2 Base Response (M) (099AEC2C)](#trigger-099aec2c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Base Response 1 (0B41CDEC)](all11t-teams.md#team-0b41cdec).
2. Create/recruit team [BG2 Base Response 2 (0B41C93C)](all11t-teams.md#team-0b41c93c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9503, Events line 9607, Actions line 9711.

<a id="trigger-0907b33c"></a>

### 96. BG2 Base Response (H) - 0907B33C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [BG2 Base Response (E) (0907F09C)](#trigger-0907f09c).

Attached scope: Tesla Coil (TESLA), owner BadGuy2 House, cell (181, 203), tag 099AEA2C, persistence mode 0; Tesla Coil (TESLA), owner BadGuy2 House, cell (193, 191), tag 099AEA2C, persistence mode 0; Tesla Coil (TESLA), owner BadGuy2 House, cell (193, 207), tag 099AEA2C, persistence mode 0; Tesla Coil (TESLA), owner BadGuy2 House, cell (197, 203), tag 099AEA2C, persistence mode 0; Soviet Construction Yard (NACNST), owner BadGuy2 House, cell (192, 202), tag 099AEA2C, persistence mode 0; Soviet Ore Refinery (NAREFN), owner BadGuy2 House, cell (200, 178), tag 099AEA2C, persistence mode 0; Sentry Gun (NALASR), owner BadGuy2 House, cell (201, 186), tag 099AEA2C, persistence mode 0; Sentry Gun (NALASR), owner BadGuy2 House, cell (201, 182), tag 099AEA2C, persistence mode 0; Sentry Gun (NALASR), owner BadGuy2 House, cell (176, 195), tag 099AEA2C, persistence mode 0; Sentry Gun (NALASR), owner BadGuy2 House, cell (173, 194), tag 099AEA2C, persistence mode 0; Flak Cannon (NAFLAK), owner BadGuy2 House, cell (185, 207), tag 099AEA2C, persistence mode 0; Flak Cannon (NAFLAK), owner BadGuy2 House, cell (197, 196), tag 099AEA2C, persistence mode 0; Soviet Ore Refinery (NAREFN), owner BadGuy2 House, cell (166, 201), tag 099AEA2C, persistence mode 0; Tesla Reactor (NAPOWR), owner BadGuy2 House, cell (176, 207), tag 099AEA2C, persistence mode 0; Tesla Reactor (NAPOWR), owner BadGuy2 House, cell (189, 205), tag 099AEA2C, persistence mode 0; Nuclear Reactor (NANRCT), owner BadGuy2 House, cell (172, 203), tag 099AEA2C, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [BG2 Base Response 4 (0907C51C)](all11t-teams.md#team-0907c51c).
2. Create/recruit team [BG2 Base Response 3 (0B41C48C)](all11t-teams.md#team-0b41c48c).
3. Create/recruit team [BG2 Base Response 2 (0B41C93C)](all11t-teams.md#team-0b41c93c).
4. Create/recruit team [BG2 Base Response 1 (0B41CDEC)](all11t-teams.md#team-0b41cdec).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9504, Events line 9608, Actions line 9712.

<a id="trigger-0b5e803c"></a>

### 97. Chronosphere is Built - 0B5E803C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B5F604C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 27 (global list position: Chrono Sphere (GACSPH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Set local flag 33 (Chronosphere Up).
2. Enable and reset applicable timers for [Chronosphere Hint (0A95E08C)](#trigger-0a95e08c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9505, Events line 9609, Actions line 9713.

<a id="trigger-0afa6f3c"></a>

### 98. Disable Cuba Invasion Teams - 0AFA6F3C

Owner reference: BadGuy2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Soviet Shipyard (NAYARD), owner BadGuy2 House, cell (180, 173), tag 0AFA660C, persistence mode 1; Soviet Shipyard (NAYARD), owner BadGuy2 House, cell (166, 182), tag 0AFA660C, persistence mode 1.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Disable [1st Teams Go (0ADC130C)](#trigger-0adc130c).
2. Disable [2nd Teams Go (0B65103C)](#trigger-0b65103c).
3. Disable [3rd Teams Go (0A77D05C)](#trigger-0a77d05c).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9506, Events line 9610, Actions line 9714.

<a id="trigger-0b148f3c"></a>

### 99. Battlefield Control Online - 0B148F3C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B148A2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 62 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play voice notification EVA_BattlefieldControlOnline.
2. Display message “--Battle Control Online--” (MISSION:All01q).
3. Enable player input.

Source locator: MAPS01.MIX/all11t.map; Triggers line 9507, Events line 9611, Actions line 9715.

<a id="trigger-0dc801ec"></a>

### 100. Dead Squid - 0DC801EC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Giant Squid (SQD), owner BadGuy2 House, cell (93, 128), tag 0DC8618C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Set local flag 35 (Dead Squid).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9508, Events line 9612, Actions line 9716.

<a id="trigger-0e01140c"></a>

### 101. Battlefield Control Hold - 0E01140C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0E0135AC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Disable player input.
2. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS01.MIX/all11t.map; Triggers line 9509, Events line 9613, Actions line 9717.

<a id="trigger-0db6a7ec"></a>

### 102. Enable Persistent Teams - 0DB6A7EC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0DB6BD3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 62 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Recur Invader 1 (t=t+300) (0BB1A4D0)](#trigger-0bb1a4d0).
2. Enable and reset applicable timers for [Recur Invader 2a (t=300) (0A3B0160)](#trigger-0a3b0160).
3. Enable and reset applicable timers for [Sea Attk (t=t+625) (0BB1C5E0)](#trigger-0bb1c5e0).
4. Enable and reset applicable timers for [ParaTeam 4 (t=t+420) (0D5F4220)](#trigger-0d5f4220).
5. Enable and reset applicable timers for [ParaTeam 5 (t=t+500) (09B465EC)](#trigger-09b465ec).
6. Enable and reset applicable timers for [ Invader 2b (t=t+450) (0A390C80)](#trigger-0a390c80).

Source locator: MAPS01.MIX/all11t.map; Triggers line 9510, Events line 9614, Actions line 9718.

[All team rosters and ordered plans](all11t-teams.md) | [All mission overrides](all11t-overrides.md)
