# Operation: Deep Sea

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

<!-- ILLUSTRATIONS:START -->
![Initial placement schematic for all07t.map.](../../images/map-all07t.svg)

*Initial placement schematic for all07t.map. Explanatory diagram derived from the guide and local data; not a screenshot.*
<!-- ILLUSTRATIONS:END -->

**Map:** all07t.map. **Effective extracted member:** MAPS01.MIX/all07t.map. **Trigger definitions:** 57.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](all07t-teams.md) | [All mission overrides](all07t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Player House |
| Theater | TEMPERATE |
| Map size | 0,0,175,125 |
| Visible local rectangle | 5,5,165,114 |
| Placed vehicles | 35 |
| Placed infantry | 47 |
| Placed structures | 128 |
| Placed aircraft | 0 |
| Team templates | 87 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Player House | 100 | Player |
| 1 | BadGuy1 House | 600 | BadGuy1 |
| 2 | BadGuy2 House | 0 | BadGuy2 |
| 3 | BadGuy3 House | 0 | BadGuy3 |
| 4 | Civie1 House | 0 | Civilian1 |
| 5 | Other1 House | 10 | Other1 |
| 6 | Civie3 House | 0 | Civilian3 |
| 7 | House Balabos | 0 | Balabos |
| 8 | Civie2 House | 0 | Civilian2 |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | Niihau Invaders 1,0 |
| 1 | Niihau Invaders 2,0 |
| 2 | Niihau Invaders 3,0 |
| 3 | Niihau Invaders MCV,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [_Win Game Over (09C9877C)](#trigger-09c9877c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner. |
| [_Loss Game Over (09C98F3C)](#trigger-09c98f3c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser. |

## Every trigger, in file order

<a id="trigger-0a991f3c"></a>

### 1. Reveal Hawaii - 0A991F3C

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A991A2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 1 (cell 186, 161).
2. Reveal terrain around waypoint 2 (cell 196, 171).
3. Reveal terrain around waypoint 3 (cell 205, 168).
4. Reveal terrain around waypoint 4 (cell 216, 166).
5. Reveal terrain around waypoint 5 (cell 211, 147).
6. Reveal terrain around waypoint 95 (cell 204, 123).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10368, Events line 10427, Actions line 10486.

<a id="trigger-0ba51e1c"></a>

### 2. Zone Reveal Hawaii - 0BA51E1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BA51A1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal the zone associated with waypoint 6 (cell 172, 113).
2. Reveal the zone associated with waypoint 7 (cell 87, 114).
3. Reveal the zone associated with waypoint 9 (cell 65, 131).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10369, Events line 10428, Actions line 10487.

<a id="trigger-07c3c06c"></a>

### 3. Niihau Neutralizers Go1 (Easy) - 07C3C06C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Intro Step 5 (0899009C)](#trigger-0899009c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 40 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 18 (country/type OTHER1; placed owner Other1 House).
2. Supply reinforcement team [Niihau Softener 1a (09D4AA4C)](all07t-teams.md#team-09d4aa4c).
3. Supply reinforcement team [Niihau Softener 1b (09D496AC)](all07t-teams.md#team-09d496ac).
4. Supply reinforcement team [Niihau Softener 1c (0AF92A1C)](all07t-teams.md#team-0af92a1c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10370, Events line 10429, Actions line 10488.

<a id="trigger-0c43798c"></a>

### 4. Niihau Neutralizers Go2 - 0C43798C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0C435B8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 6 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Niihau Softener 2 (0913C28C)](all07t-teams.md#team-0913c28c).
2. Enable and reset applicable timers for [Niihau Neutralizers Go3 (0C435A9C)](#trigger-0c435a9c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10371, Events line 10430, Actions line 10489.

<a id="trigger-0c435a9c"></a>

### 5. Niihau Neutralizers Go3 - 0C435A9C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Niihau Neutralizers Go2 (0C43798C)](#trigger-0c43798c); enable from [Niihau Defenders (0AAC521C)](#trigger-0aac521c).

Attached scope: tag definitions 0C4357EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Niihau Softener 3a (0A0F832C)](all07t-teams.md#team-0a0f832c).
2. Supply reinforcement team [Niihau Softener 3b (08D1174C)](all07t-teams.md#team-08d1174c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10372, Events line 10431, Actions line 10490.

<a id="trigger-0aac521c"></a>

### 6. Niihau Defenders - 0AAC521C

Owner reference: Other1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Patriot Missile (NASAM), owner Other1 House, cell (63, 188), tag 0AAC1A0C, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (50, 188), tag 0AAC1A0C, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (54, 195), tag 0AAC1A0C, persistence mode 0; Patriot Missile (NASAM), owner Other1 House, cell (59, 195), tag 0AAC1A0C, persistence mode 0.

**Wait for the recorded events:**

1. First damaged (any source). See attached-object/cell scope below.

**Then perform these actions in order:**

1. Make enemy: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. Create/recruit team [Niihau Choppers (0AAB5ABC)](all07t-teams.md#team-0aab5abc).
3. Create/recruit team [Niihau GIs (08C4935C)](all07t-teams.md#team-08c4935c).
4. Play in-game movie 89.
5. Enable and reset applicable timers for [Niihau - Just Die Already (03EE525C)](#trigger-03ee525c).
6. Create/recruit team [Niihau Grizzlies (09DEDEFC)](all07t-teams.md#team-09dedefc).
7. Supply reinforcement team [Niihau Softener 2 (0913C28C)](all07t-teams.md#team-0913c28c).
8. Enable and reset applicable timers for [Niihau Neutralizers Go3 (0C435A9C)](#trigger-0c435a9c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10373, Events line 10432, Actions line 10491.

<a id="trigger-03ee525c"></a>

### 7. Niihau - Just Die Already - 03EE525C

Owner reference: Other1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Niihau Defenders (0AAC521C)](#trigger-0aac521c).

Attached scope: GI (E1), owner Other1 House, cell (63, 193), tag 03EE33CC, persistence mode 0; GI (E1), owner Other1 House, cell (63, 191), tag 03EE33CC, persistence mode 0; GI (E1), owner Other1 House, cell (50, 193), tag 03EE33CC, persistence mode 0; GI (E1), owner Other1 House, cell (50, 191), tag 03EE33CC, persistence mode 0; GI (E1), owner Other1 House, cell (55, 197), tag 03EE33CC, persistence mode 0; GI (E1), owner Other1 House, cell (58, 197), tag 03EE33CC, persistence mode 0; GI (E1), owner Other1 House, cell (55, 197), tag 03EE33CC, persistence mode 0; GI (E1), owner Other1 House, cell (59, 197), tag 03EE33CC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (52, 193), tag 03EE33CC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (61, 193), tag 03EE33CC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (50, 190), tag 03EE33CC, persistence mode 0; Pill Box (GAPILL), owner Other1 House, cell (63, 190), tag 03EE33CC, persistence mode 0.

**Wait for the recorded events:**

1. 135 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Destroy the attached object through the scripted destruction action.

Source locator: MAPS01.MIX/all07t.map; Triggers line 10374, Events line 10433, Actions line 10492.

<a id="trigger-07a173ac"></a>

### 8. _Win Occurred - 07A173AC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A170FC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Win Game Over (09C9877C)](#trigger-09c9877c).
2. Make side cheer: owner selector 13 (country/type PLAYER; placed owner Player House).
3. Make side cheer: owner selector 17 (country/type CIVILIAN1; placed owner Civie1 House).
4. Make side cheer: owner selector 21 (country/type CIVILIAN2; placed owner Civie2 House).
5. Make side cheer: owner selector 19 (country/type CIVILIAN3; placed owner Civie3 House).
6. Disable [Objective Statement (0A949BE4)](#trigger-0a949be4).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10375, Events line 10434, Actions line 10493.

<a id="trigger-09c9877c"></a>

### 9. _Win Game Over - 09C9877C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Win Occurred (07A173AC)](#trigger-07a173ac).

Attached scope: tag definitions 09C984CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the winner.

Source locator: MAPS01.MIX/all07t.map; Triggers line 10376, Events line 10435, Actions line 10494.

<a id="trigger-07a17a6c"></a>

### 10. _Loss Occured - 07A17A6C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A1749C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 13 (country/type PLAYER; placed owner Player House).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [_Loss Game Over (09C98F3C)](#trigger-09c98f3c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10377, Events line 10436, Actions line 10495.

<a id="trigger-09c98f3c"></a>

### 11. _Loss Game Over - 09C98F3C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Loss Occured (07A17A6C)](#trigger-07a17a6c).

Attached scope: tag definitions 09C9894C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 13 (country/type PLAYER; placed owner Player House) the loser.

Source locator: MAPS01.MIX/all07t.map; Triggers line 10378, Events line 10437, Actions line 10496.

<a id="trigger-08da9e3c"></a>

### 12. Niihau Lost - 08DA9E3C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08DA981C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 18 (country/type OTHER1; placed owner Other1 House).

**Then perform these actions in order:**

1. Supply reinforcement team [Niihau Invaders 1 (0B0EBEFC)](all07t-teams.md#team-0b0ebefc).
2. Supply reinforcement team [Niihau Invaders 2 (0B0EBA4C)](all07t-teams.md#team-0b0eba4c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10379, Events line 10438, Actions line 10497.

<a id="trigger-07c2b23c"></a>

### 13. Niihau Invaders 1a Go - 07C2B23C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C28DFC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (Niihau Invaders 1) is set.

**Then perform these actions in order:**

1. Create/recruit team [Niihau Invaders 1a (09D7B59C)](all07t-teams.md#team-09d7b59c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10380, Events line 10439, Actions line 10498.

<a id="trigger-07c28d0c"></a>

### 14. Niihau Invaders 2a Go - 07C28D0C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C28B0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 1 (Niihau Invaders 2) is set.

**Then perform these actions in order:**

1. Create/recruit team [Niihau Invaders 2a (08D6495C)](all07t-teams.md#team-08d6495c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10381, Events line 10440, Actions line 10499.

<a id="trigger-07a3a6bc"></a>

### 15. Niihau Captured - 07A3A6BC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A3C7CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 18 (country/type OTHER1; placed owner Other1 House).

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Niihau Softener 1a (09D4AA4C)](all07t-teams.md#team-09d4aa4c).
2. Remove instances of the team organization (not automatically its surviving objects) [Niihau Softener 1b (09D496AC)](all07t-teams.md#team-09d496ac).
3. Remove instances of the team organization (not automatically its surviving objects) [Niihau Softener 1c (0AF92A1C)](all07t-teams.md#team-0af92a1c).
4. Remove instances of the team organization (not automatically its surviving objects) [Niihau Softener 3a (0A0F832C)](all07t-teams.md#team-0a0f832c).
5. Remove instances of the team organization (not automatically its surviving objects) [Niihau Softener 3b (08D1174C)](all07t-teams.md#team-08d1174c).
6. Remove instances of the team organization (not automatically its surviving objects) [Niihau Softener 2 (0913C28C)](all07t-teams.md#team-0913c28c).
7. Supply reinforcement team [Niihau Invaders MCV (0B0ECA4C)](all07t-teams.md#team-0b0eca4c).
8. Create/recruit team [Niihau Softener 1a2 (08DF920C)](all07t-teams.md#team-08df920c).
9. Create/recruit team [Niihau Softener 1b2 (08C232DC)](all07t-teams.md#team-08c232dc).
10. Create/recruit team [Niihau Softener 1c2 (08C21DFC)](all07t-teams.md#team-08c21dfc).
11. Create/recruit team [Niihau Softener 3a2 (08BFA80C)](all07t-teams.md#team-08bfa80c).
12. Create/recruit team [Niihau Softener 3b2 (08BFEF0C)](all07t-teams.md#team-08bfef0c).
13. Create/recruit team [Niihau Softener 22 (0AA1D1EC)](all07t-teams.md#team-0aa1d1ec).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10382, Events line 10441, Actions line 10500.

<a id="trigger-07a3d71c"></a>

### 16. Niihau Invaders MCV Go - 07A3D71C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A3A56C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 3 (Niihau Invaders MCV) is set.

**Then perform these actions in order:**

1. Create/recruit team [Niihau Invaders MCVa (08F867FC)](all07t-teams.md#team-08f867fc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10383, Events line 10442, Actions line 10501.

<a id="trigger-07c38abc"></a>

### 17. BG1 Production Start - 07C38ABC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C3849C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Production Begins: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. AI triggers begin: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).
4. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10384, Events line 10443, Actions line 10502.

<a id="trigger-08bfcc2c"></a>

### 18. Can't See BG1 - 08BFCC2C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08BFC87C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 18 (country/type OTHER1; placed owner Other1 House).

**Then perform these actions in order:**

1. Reshroud Map At; main setting 0.
2. Reshroud Map At; main setting 18; location/duration field S.
3. Reshroud Map At; main setting 17; location/duration field R.
4. Reshroud Map At; main setting 25; location/duration field Z.
5. Reshroud Map At; main setting 23; location/duration field X.
6. Reshroud Map At; main setting 36; location/duration field AK.
7. Reshroud Map At; main setting 46; location/duration field AU.
8. Reshroud Map At; main setting 47; location/duration field AV.
9. Reshroud Map At; main setting 21; location/duration field V.
10. Enable and reset applicable timers for [Objective Statement (0A949BE4)](#trigger-0a949be4).
11. Reshroud Map At; main setting 49; location/duration field AX.

Source locator: MAPS01.MIX/all07t.map; Triggers line 10385, Events line 10444, Actions line 10503.

<a id="trigger-0a949be4"></a>

### 19. Objective Statement - 0A949BE4

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Can't See BG1 (08BFCC2C)](#trigger-08bfcc2c).

Attached scope: tag definitions 0A949764 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 1: Destroy all Soviet forces” (MISSION:All07a1).
2. Display message “on or around the Hawaiian Islands” (MISSION:All07a2).
3. Create radar-event marker type 5 at waypoint 18 (cell 57, 192).
4. Play voice notification Mis_A7_EvaNiihauFallen.
5. Enable and reset applicable timers for [Restate Objective (07F3E94C)](#trigger-07f3e94c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10386, Events line 10445, Actions line 10504.

<a id="trigger-07f3e94c"></a>

### 20. Restate Objective - 07F3E94C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective Statement (0A949BE4)](#trigger-0a949be4).

Attached scope: tag definitions 07F3E5EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 18 (cell 57, 192).
2. Display message “Objective 1: Destroy all Soviet forces” (MISSION:All07a1).
3. Display message “on or around the Hawaiian Islands” (MISSION:All07a2).
4. Enable and reset applicable timers for [Enough with the Objective (07F3E44C)](#trigger-07f3e44c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10387, Events line 10446, Actions line 10505.

<a id="trigger-07f3e44c"></a>

### 21. Enough with the Objective - 07F3E44C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Restate Objective (07F3E94C)](#trigger-07f3e94c).

Attached scope: tag definitions 07F3E24C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 540 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Restate Objective (07F3E94C)](#trigger-07f3e94c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10388, Events line 10447, Actions line 10506.

<a id="trigger-07be3ccc"></a>

### 22. Pearl Neutralization 1 (Easy) - 07BE3CCC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Intro Step 5 (0899009C)](#trigger-0899009c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 40 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Pearl Attack Fleet 1a (0A102C8C)](all07t-teams.md#team-0a102c8c).
2. Supply reinforcement team [Pearl Attack Fleet 1b (0A1027DC)](all07t-teams.md#team-0a1027dc).
3. Supply reinforcement team [Pearl Attack Fleet 1c (0A101A4C)](all07t-teams.md#team-0a101a4c).
4. Display message “WARNING - SOVIET ATTACK IMMINENT” (MISSION:All07b).
5. Enable and reset applicable timers for [Pearl Neutralization 2 (09A5098C)](#trigger-09a5098c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10389, Events line 10448, Actions line 10507.

<a id="trigger-09a5098c"></a>

### 23. Pearl Neutralization 2 - 09A5098C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Pearl Neutralization 1 (Easy) (07BE3CCC)](#trigger-07be3ccc); enable from [Pearl Neutralization 1 (Med) (041788DC)](#trigger-041788dc); enable from [Pearl Neutralization 1 (Hard) (0417812C)](#trigger-0417812c).

Attached scope: tag definitions 09A5057C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 12 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Pearl Attack Fleet 3a (0A1016AC)](all07t-teams.md#team-0a1016ac).
2. Supply reinforcement team [Pearl Attack Fleet 3b (0A1011FC)](all07t-teams.md#team-0a1011fc).
3. Supply reinforcement team [Pearl Attack Fleet 3c (0A100C8C)](all07t-teams.md#team-0a100c8c).
4. Enable and reset applicable timers for [Pearl Neutralization 3 (09A50F3C)](#trigger-09a50f3c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10390, Events line 10449, Actions line 10508.

<a id="trigger-09a50f3c"></a>

### 24. Pearl Neutralization 3 - 09A50F3C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Pearl Neutralization 2 (09A5098C)](#trigger-09a5098c).

Attached scope: tag definitions 09A50A7C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Pearl Attack Fleet 2a (09366444)](all07t-teams.md#team-09366444).
2. Supply reinforcement team [Pearl Attack Fleet 2b (08F077FC)](all07t-teams.md#team-08f077fc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10391, Events line 10450, Actions line 10509.

<a id="trigger-0bd9631c"></a>

### 25. PAttk_Infantry2 Trig - 0BD9631C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PAttk_Infantrys Enable (Easy) (07A1628C)](#trigger-07a1628c); enable from [PAttk_Infantrys Enable (Med) (0834D25C)](#trigger-0834d25c); enable from [PAttk_Infantrys Enable (Hard) (0835372C)](#trigger-0835372c).

Attached scope: tag definitions 0BD97E1C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [PAttk_Infantry2 (0AFC51FC)](all07t-teams.md#team-0afc51fc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10392, Events line 10451, Actions line 10510.

<a id="trigger-07a1628c"></a>

### 26. PAttk_Infantrys Enable (Easy) - 07A1628C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Building Type: type index 15 (global list position: Soviet Ore Refinery (NAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PAttk_Infantry2 Trig (0BD9631C)](#trigger-0bd9631c).
2. Enable and reset applicable timers for [PAttk_Infantry1 Trig (08EB692C)](#trigger-08eb692c).
3. Enable and reset applicable timers for [PAttk_Infantry3 Trig (08EB60BC)](#trigger-08eb60bc).
4. Supply reinforcement team [PAttk_Infantry1 (0AFC56AC)](all07t-teams.md#team-0afc56ac).
5. Supply reinforcement team [PAttk_Infantry2 (0AFC51FC)](all07t-teams.md#team-0afc51fc).
6. Enable and reset applicable timers for [End PAttk Trigs (07B775BC)](#trigger-07b775bc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10393, Events line 10452, Actions line 10511.

<a id="trigger-08eb692c"></a>

### 27. PAttk_Infantry1 Trig - 08EB692C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PAttk_Infantrys Enable (Easy) (07A1628C)](#trigger-07a1628c); enable from [PAttk_Infantrys Enable (Med) (0834D25C)](#trigger-0834d25c); enable from [PAttk_Infantrys Enable (Hard) (0835372C)](#trigger-0835372c).

Attached scope: tag definitions 08EB644C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 420 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [PAttk_Infantry1 (0AFC56AC)](all07t-teams.md#team-0afc56ac).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10394, Events line 10453, Actions line 10512.

<a id="trigger-08eb60bc"></a>

### 28. PAttk_Infantry3 Trig - 08EB60BC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PAttk_Infantrys Enable (Easy) (07A1628C)](#trigger-07a1628c); enable from [PAttk_Infantrys Enable (Med) (0834D25C)](#trigger-0834d25c); enable from [PAttk_Infantrys Enable (Hard) (0835372C)](#trigger-0835372c).

Attached scope: tag definitions 08EB7C5C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 720 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [PAttk_Infantry3 (0AFC4B7C)](all07t-teams.md#team-0afc4b7c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10395, Events line 10454, Actions line 10513.

<a id="trigger-07b775bc"></a>

### 29. End PAttk Trigs - 07B775BC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [PAttk_Infantrys Enable (Easy) (07A1628C)](#trigger-07a1628c); enable from [PAttk_Infantrys Enable (Med) (0834D25C)](#trigger-0834d25c); enable from [PAttk_Infantrys Enable (Hard) (0835372C)](#trigger-0835372c).

Attached scope: tag definitions 07B7171C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Buildings,  All: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Disable [PAttk_Infantry1 Trig (08EB692C)](#trigger-08eb692c).
2. Disable [PAttk_Infantry2 Trig (0BD9631C)](#trigger-0bd9631c).
3. Disable [PAttk_Infantry3 Trig (08EB60BC)](#trigger-08eb60bc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10396, Events line 10455, Actions line 10514.

<a id="trigger-0a8f13d4"></a>

### 30. Player Harvesters Start - 0A8F13D4

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A8F6C44 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [Player Harvesters (0A8F2F04)](all07t-teams.md#team-0a8f2f04).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10397, Events line 10456, Actions line 10515.

<a id="trigger-07fed65c"></a>

### 31. Play Heavy Surf - 07FED65C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FED15C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 69 (cell 223, 155).
2. Play sound _Amb_OceanHeavy at waypoint 70 (cell 197, 180).
3. Play sound _Amb_OceanHeavy at waypoint 71 (cell 175, 165).
4. Play sound _Amb_OceanHeavy at waypoint 72 (cell 148, 168).
5. Play sound _Amb_OceanHeavy at waypoint 73 (cell 122, 169).
6. Play sound _Amb_OceanHeavy at waypoint 76 (cell 120, 122).
7. Play sound _Amb_OceanHeavy at waypoint 77 (cell 135, 106).
8. Play sound _Amb_OceanHeavy at waypoint 78 (cell 129, 81).
9. Play sound _Amb_OceanHeavy at waypoint 79 (cell 141, 72).
10. Play sound _Amb_OceanHeavy at waypoint 81 (cell 174, 77).
11. Play sound _Amb_OceanHeavy at waypoint 82 (cell 196, 80).
12. Play sound _Amb_OceanHeavy at waypoint 83 (cell 226, 83).
13. Play sound _Amb_OceanHeavy at waypoint 84 (cell 252, 121).
14. Play sound _Amb_OceanHeavy at waypoint 28 (cell 78, 182).
15. Play sound _Amb_OceanHeavy at waypoint 30 (cell 40, 166).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10398, Events line 10457, Actions line 10516.

<a id="trigger-07fee3ec"></a>

### 32. Play Light Surf - 07FEE3EC

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FEFC0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_OceanLight at waypoint 37 (cell 209, 136).
2. Play sound _Amb_OceanLight at waypoint 74 (cell 101, 150).
3. Play sound _Amb_OceanLight at waypoint 75 (cell 106, 132).
4. Play sound _Amb_OceanLight at waypoint 80 (cell 157, 82).
5. Play sound _Amb_OceanLight at waypoint 85 (cell 245, 139).
6. Play sound _Amb_OceanLight at waypoint 15 (cell 47, 202).
7. Play sound _Amb_OceanLight at waypoint 16 (cell 64, 204).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10399, Events line 10458, Actions line 10517.

<a id="trigger-07fefb1c"></a>

### 33. Play Harbor Birds - 07FEFB1C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FEF98C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsHarbor at waypoint 38 (cell 194, 139).
2. Play sound _Amb_BirdsHarbor at waypoint 39 (cell 196, 126).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10400, Events line 10459, Actions line 10518.

<a id="trigger-07fef89c"></a>

### 34. Play Urban Murmur - 07FEF89C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FEFF4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur2 at waypoint 65 (cell 230, 125).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10401, Events line 10460, Actions line 10519.

<a id="trigger-07fefe5c"></a>

### 35. Play Birdsongs - 07FEFE5C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07FEE5CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsTemperate2 at waypoint 86 (cell 163, 95).
2. Play sound _Amb_BirdsTemperate2 at waypoint 58 (cell 154, 132).
3. Play sound _Amb_BirdsTemperate1 at waypoint 9 (cell 65, 131).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10402, Events line 10461, Actions line 10520.

<a id="trigger-0b33703c"></a>

### 36. BG1 Firesale - 0B33703C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Firesale Enabler 2 (0BF482EC)](#trigger-0bf482ec).

Attached scope: tag definitions 0BF48B8C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. No Factories left. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
2. All to Hunt: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).
3. Enable and reset applicable timers for [Transports Must Die (0B445EDC)](#trigger-0b445edc).
4. Enable and reset applicable timers for [End Transport Team Creation (0B4458FC)](#trigger-0b4458fc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10403, Events line 10462, Actions line 10521.

<a id="trigger-0b445edc"></a>

### 37. Transports Must Die - 0B445EDC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Firesale (0B33703C)](#trigger-0b33703c).

Attached scope: tag definitions 0B4459EC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Stupid Transports Must Die (083346CC)](all07t-teams.md#team-083346cc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10404, Events line 10463, Actions line 10522.

<a id="trigger-0b4458fc"></a>

### 38. End Transport Team Creation - 0B4458FC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Firesale (0B33703C)](#trigger-0b33703c).

Attached scope: tag definitions 0B44149C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 51 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Disable [Transports Must Die (0B445EDC)](#trigger-0b445edc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10405, Events line 10464, Actions line 10523.

<a id="trigger-0bf48a9c"></a>

### 39. BG1 Firesale Enabler 1 - 0BF48A9C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BF484BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 Firesale Enabler 2 (0BF482EC)](#trigger-0bf482ec).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10406, Events line 10465, Actions line 10524.

<a id="trigger-0bf482ec"></a>

### 40. BG1 Firesale Enabler 2 - 0BF482EC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [BG1 Firesale Enabler 1 (0BF48A9C)](#trigger-0bf48a9c).

Attached scope: tag definitions 0BF49C3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [BG1 Firesale (0B33703C)](#trigger-0b33703c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10407, Events line 10466, Actions line 10525.

<a id="trigger-0bf4ccfc"></a>

### 41. BG1 Hates Player - 0BF4CCFC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0BF4C96C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 18 (country/type OTHER1; placed owner Other1 House).

**Then perform these actions in order:**

1. Make ally: owner selector 18 (country/type OTHER1; placed owner Other1 House).
2. Make enemy: owner selector 13 (country/type PLAYER; placed owner Player House).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10408, Events line 10467, Actions line 10526.

<a id="trigger-079ed7ec"></a>

### 42. Couple Extra Transports - 079ED7EC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 079ED17C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [Extra Transport 1 (079ED04C)](all07t-teams.md#team-079ed04c).
2. Supply reinforcement team [Extra Transport 2 (079EE79C)](all07t-teams.md#team-079ee79c).
3. Supply reinforcement team [Extra Transport 3 (081B8EFC)](all07t-teams.md#team-081b8efc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10409, Events line 10468, Actions line 10527.

<a id="trigger-0834d25c"></a>

### 43. PAttk_Infantrys Enable (Med) - 0834D25C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [PAttk_Infantrys Enable (Easy) (07A1628C)](#trigger-07a1628c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Building Type: type index 11 (global list position: Soviet Barracks (NAHAND)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PAttk_Infantry1 Trig (08EB692C)](#trigger-08eb692c).
2. Enable and reset applicable timers for [PAttk_Infantry2 Trig (0BD9631C)](#trigger-0bd9631c).
3. Enable and reset applicable timers for [PAttk_Infantry3 Trig (08EB60BC)](#trigger-08eb60bc).
4. Supply reinforcement team [PAttk_Infantry1 (0AFC56AC)](all07t-teams.md#team-0afc56ac).
5. Supply reinforcement team [PAttk_Infantry2 (0AFC51FC)](all07t-teams.md#team-0afc51fc).
6. Enable and reset applicable timers for [End PAttk Trigs (07B775BC)](#trigger-07b775bc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10410, Events line 10469, Actions line 10528.

<a id="trigger-0835372c"></a>

### 44. PAttk_Infantrys Enable (Hard) - 0835372C

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [PAttk_Infantrys Enable (Med) (0834D25C)](#trigger-0834d25c).

Attached scope: tag definitions 07A17B5C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [PAttk_Infantry1 Trig (08EB692C)](#trigger-08eb692c).
2. Enable and reset applicable timers for [PAttk_Infantry2 Trig (0BD9631C)](#trigger-0bd9631c).
3. Enable and reset applicable timers for [PAttk_Infantry3 Trig (08EB60BC)](#trigger-08eb60bc).
4. Supply reinforcement team [PAttk_Infantry1 (0AFC56AC)](all07t-teams.md#team-0afc56ac).
5. Supply reinforcement team [PAttk_Infantry2 (0AFC51FC)](all07t-teams.md#team-0afc51fc).
6. Enable and reset applicable timers for [End PAttk Trigs (07B775BC)](#trigger-07b775bc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10411, Events line 10470, Actions line 10529.

<a id="trigger-0cea003c"></a>

### 45. Niihau Neutralizers Go1 (Med) - 0CEA003C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Niihau Neutralizers Go1 (Easy) (07C3C06C)](#trigger-07c3c06c).

Incoming activation links: enable from [_Intro Step 5 (0899009C)](#trigger-0899009c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 18 (country/type OTHER1; placed owner Other1 House).
2. Supply reinforcement team [Niihau Softener 1a (09D4AA4C)](all07t-teams.md#team-09d4aa4c).
3. Supply reinforcement team [Niihau Softener 1b (09D496AC)](all07t-teams.md#team-09d496ac).
4. Supply reinforcement team [Niihau Softener 1c (0AF92A1C)](all07t-teams.md#team-0af92a1c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10412, Events line 10471, Actions line 10530.

<a id="trigger-04178e9c"></a>

### 46. Niihau Neutralizers Go1 (Hard) - 04178E9C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Niihau Neutralizers Go1 (Med) (0CEA003C)](#trigger-0cea003c).

Incoming activation links: enable from [_Intro Step 5 (0899009C)](#trigger-0899009c).

Attached scope: tag definitions 07C3E94C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make enemy: owner selector 18 (country/type OTHER1; placed owner Other1 House).
2. Supply reinforcement team [Niihau Softener 1a (09D4AA4C)](all07t-teams.md#team-09d4aa4c).
3. Supply reinforcement team [Niihau Softener 1b (09D496AC)](all07t-teams.md#team-09d496ac).
4. Supply reinforcement team [Niihau Softener 1c (0AF92A1C)](all07t-teams.md#team-0af92a1c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10413, Events line 10472, Actions line 10531.

<a id="trigger-041788dc"></a>

### 47. Pearl Neutralization 1 (Med) - 041788DC

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 0 (1 means included). Linked trigger: [Pearl Neutralization 1 (Easy) (07BE3CCC)](#trigger-07be3ccc).

Incoming activation links: enable from [_Intro Step 5 (0899009C)](#trigger-0899009c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Pearl Attack Fleet 1a (0A102C8C)](all07t-teams.md#team-0a102c8c).
2. Supply reinforcement team [Pearl Attack Fleet 1b (0A1027DC)](all07t-teams.md#team-0a1027dc).
3. Supply reinforcement team [Pearl Attack Fleet 1c (0A101A4C)](all07t-teams.md#team-0a101a4c).
4. Display message “WARNING - SOVIET ATTACK IMMINENT” (MISSION:All07b).
5. Enable and reset applicable timers for [Pearl Neutralization 2 (09A5098C)](#trigger-09a5098c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10414, Events line 10473, Actions line 10532.

<a id="trigger-0417812c"></a>

### 48. Pearl Neutralization 1 (Hard) - 0417812C

Owner reference: BadGuy1. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Pearl Neutralization 1 (Med) (041788DC)](#trigger-041788dc).

Incoming activation links: enable from [_Intro Step 5 (0899009C)](#trigger-0899009c).

Attached scope: tag definitions 07BE0C0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Pearl Attack Fleet 1a (0A102C8C)](all07t-teams.md#team-0a102c8c).
2. Supply reinforcement team [Pearl Attack Fleet 1b (0A1027DC)](all07t-teams.md#team-0a1027dc).
3. Supply reinforcement team [Pearl Attack Fleet 1c (0A101A4C)](all07t-teams.md#team-0a101a4c).
4. Display message “WARNING - SOVIET ATTACK IMMINENT” (MISSION:All07b).
5. Enable and reset applicable timers for [Pearl Neutralization 2 (09A5098C)](#trigger-09a5098c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10415, Events line 10474, Actions line 10533.

<a id="trigger-08b45e0c"></a>

### 49. _Intro Step 1 - 08B45E0C

Owner reference: Player. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08B458CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Disable player input.
2. Enable and reset applicable timers for [_Intro Step 2 (08B457DC)](#trigger-08b457dc).
3. Play voice notification EVA_EstablishBattlefieldControl.
4. Create/recruit team [Forward Team (064DCC9C)](all07t-teams.md#team-064dcc9c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10416, Events line 10475, Actions line 10534.

<a id="trigger-08b457dc"></a>

### 50. _Intro Step 2 - 08B457DC

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Intro Step 1 (08B45E0C)](#trigger-08b45e0c).

Attached scope: tag definitions 08B455DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 100 (cell 200, 132) with speed setting 4.
2. Create/recruit team [Aegis Flashers (0AFE51FC)](all07t-teams.md#team-0afe51fc).
3. Enable and reset applicable timers for [_Intro Step 3 (07EC505C)](#trigger-07ec505c).
4. Play voice notification Unit_Eva_Aegis.
5. Switch the sidebar to tab 3.
6. Flash cameo/type 320; additional configured duration/location argument 200.

Source locator: MAPS01.MIX/all07t.map; Triggers line 10417, Events line 10476, Actions line 10535.

<a id="trigger-07ec505c"></a>

### 51. _Intro Step 3 - 07EC505C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Intro Step 2 (08B457DC)](#trigger-08b457dc).

Attached scope: tag definitions 07EC2EDC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 15 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 38 (cell 194, 139) with speed setting 4.
2. Create/recruit team [Aircraft Carrier Flashers (0AFE6B7C)](all07t-teams.md#team-0afe6b7c).
3. Enable and reset applicable timers for [_Intro Step 5 (0899009C)](#trigger-0899009c).
4. Play voice notification Unit_Eva_AircraftCarrier.

Source locator: MAPS01.MIX/all07t.map; Triggers line 10418, Events line 10477, Actions line 10536.

<a id="trigger-0899009c"></a>

### 52. _Intro Step 5 - 0899009C

Owner reference: Player. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [_Intro Step 3 (07EC505C)](#trigger-07ec505c).

Attached scope: tag definitions 0899105C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 23 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Move the camera to waypoint 98 (cell 195, 155) with speed setting 3.
2. Play voice notification EVA_BattlefieldControlOnline.
3. Display message “--Battle Control Online--” (MISSION:ALL01q).
4. Enable player input.
5. Enable and reset applicable timers for [Niihau Neutralizers Go1 (Easy) (07C3C06C)](#trigger-07c3c06c).
6. Enable and reset applicable timers for [Niihau Neutralizers Go1 (Hard) (04178E9C)](#trigger-04178e9c).
7. Enable and reset applicable timers for [Niihau Neutralizers Go1 (Med) (0CEA003C)](#trigger-0cea003c).
8. Enable and reset applicable timers for [Pearl Neutralization 1 (Easy) (07BE3CCC)](#trigger-07be3ccc).
9. Enable and reset applicable timers for [Pearl Neutralization 1 (Hard) (0417812C)](#trigger-0417812c).
10. Enable and reset applicable timers for [Pearl Neutralization 1 (Med) (041788DC)](#trigger-041788dc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10419, Events line 10478, Actions line 10537.

<a id="trigger-0ab356bc"></a>

### 53. BG1 Niihau Patrol Start - 0AB356BC

Owner reference: BadGuy1. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AB353CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Build Building Type: type index 15 (global list position: Soviet Ore Refinery (NAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Supply reinforcement team [BG1 Niihau Patrol (090F489C)](all07t-teams.md#team-090f489c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10420, Events line 10479, Actions line 10538.

<a id="trigger-0ce3b93c"></a>

### 54. Honolulu Area Panic - 0CE3B93C

Owner reference: Civilian2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 37 tagged map cells: (244, 115), (246, 115), (244, 116), (245, 116), (244, 117), (245, 117), (246, 117), (244, 118), (245, 118), (246, 118), (244, 119), (245, 119), (246, 119), (245, 120), (222, 122), (218, 123), (219, 123), (220, 123), (221, 123), (222, 123), (223, 123), (218, 124), (219, 124), (220, 124), (223, 124), (230, 124), (218, 125), (219, 125), (220, 125), (230, 125), (230, 126), (231, 126), (232, 126), (233, 126), (232, 127), (233, 127), (233, 128); tag 0CE3B85C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Create/recruit team [Waikiki Panic (0CE3BEFC)](all07t-teams.md#team-0ce3befc).
2. Create/recruit team [Honolulu Panic (0CE3583C)](all07t-teams.md#team-0ce3583c).
3. Enable and reset applicable timers for [Stop Honolulu Panic (0CE3A79C)](#trigger-0ce3a79c).
4. Play sound CivAllFear at waypoint 8 (cell 219, 124).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10421, Events line 10480, Actions line 10539.

<a id="trigger-0ce3a79c"></a>

### 55. Stop Honolulu Panic - 0CE3A79C

Owner reference: Civilian2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Honolulu Area Panic (0CE3B93C)](#trigger-0ce3b93c).

Attached scope: tag definitions 0CE3A16C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Honolulu Panic (0CE3583C)](all07t-teams.md#team-0ce3583c).
2. Remove instances of the team organization (not automatically its surviving objects) [Waikiki Panic (0CE3BEFC)](all07t-teams.md#team-0ce3befc).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10422, Events line 10481, Actions line 10540.

<a id="trigger-0ce3f44c"></a>

### 56. Cultural Cntr Panic - 0CE3F44C

Owner reference: Civilian2. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 26 tagged map cells: (164, 99), (165, 99), (166, 99), (164, 100), (165, 100), (166, 100), (164, 101), (165, 101), (166, 101), (164, 102), (165, 102), (166, 102), (164, 103), (165, 103), (166, 103), (143, 104), (141, 105), (142, 105), (143, 105), (141, 106), (142, 106), (143, 106), (141, 107), (142, 107), (143, 107), (142, 108); tag 0CE3F24C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 14 (country/type BADGUY1; placed owner BadGuy1 House).

**Then perform these actions in order:**

1. Create/recruit team [Cultural Center Panic (0CE3FC6C)](all07t-teams.md#team-0ce3fc6c).
2. Enable and reset applicable timers for [Stop Cntr Panic (0CE3AF3C)](#trigger-0ce3af3c).
3. Play sound CivAllFear.

Source locator: MAPS01.MIX/all07t.map; Triggers line 10423, Events line 10482, Actions line 10541.

<a id="trigger-0ce3af3c"></a>

### 57. Stop Cntr Panic - 0CE3AF3C

Owner reference: Civilian2. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Cultural Cntr Panic (0CE3F44C)](#trigger-0ce3f44c).

Attached scope: tag definitions 0CE3B4EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Cultural Center Panic (0CE3FC6C)](all07t-teams.md#team-0ce3fc6c).

Source locator: MAPS01.MIX/all07t.map; Triggers line 10424, Events line 10483, Actions line 10542.

[All team rosters and ordered plans](all07t-teams.md) | [All mission overrides](all07t-overrides.md)
