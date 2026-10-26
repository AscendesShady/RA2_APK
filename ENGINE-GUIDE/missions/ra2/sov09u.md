# Operation: The Fox and the Hound

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov09u.map. **Effective extracted member:** MAPS02.MIX/sov09u.map. **Trigger definitions:** 55.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov09u-teams.md) | [All mission overrides](sov09u-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Confederation |
| Theater | URBAN |
| Map size | 0,0,60,60 |
| Visible local rectangle | 2,4,56,50 |
| Placed vehicles | 53 |
| Placed infantry | 56 |
| Placed structures | 101 |
| Placed aircraft | 0 |
| Team templates | 26 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 0 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | British | 0 | British |
| 5 | Africans | 100 | Africans |
| 6 | Arabs | 0 | Arabs |
| 7 | Confederation | 40 | Confederation |
| 8 | Russians | 0 | Russians |
| 9 | GDI | 0 | GDI |
| 10 | Nod | 0 | Nod |
| 11 | Neutral | 0 | Neutral |
| 12 | Special | 0 | Special |

### Local state flags at initialization

No named local flags were found.

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Pres is Captured (0873BB5C)](#trigger-0873bb5c) | Attacked by (house): owner selector 5 (country/type AFRICANS; placed owner Africans). | Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the winner. |
| [Pres is Dead (086A4CCC)](#trigger-086a4ccc) | First damaged (any source). See attached-object/cell scope below. | Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the loser. |
| [Yuri's are Dead (07A7507C)](#trigger-07a7507c) | Destroyed,  Units,  All: owner selector 5 (country/type AFRICANS; placed owner Africans). | Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the loser. |

## Every trigger, in file order

<a id="trigger-03e3836c"></a>

### 1. Clear Starting Shroud - 03E3836C

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03E3991C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 0 (cell 64, 59).
2. Reveal terrain around waypoint 1 (cell 57, 58).
3. Reveal terrain around waypoint 2 (cell 77, 59).
4. Reveal terrain around waypoint 3 (cell 66, 70).
5. Reveal terrain around waypoint 4 (cell 64, 51).
6. Reveal terrain around waypoint 23 (cell 32, 49).
7. Reveal terrain around waypoint 33 (cell 85, 35).
8. Reveal terrain around waypoint 34 (cell 50, 54).
9. Reveal terrain around waypoint 35 (cell 50, 58).
10. Reveal terrain around waypoint 37 (cell 35, 70).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3096, Events line 3153, Actions line 3210.

<a id="trigger-0873bb5c"></a>

### 2. Pres is Captured - 0873BB5C

Owner reference: French. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 5 (country/type AFRICANS; placed owner Africans).

**Then perform these actions in order:**

1. Display message “Objective 1 Complete” (MISSION:Objective1).
2. Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the winner.
3. Enable and reset applicable timers for [Ally Americans (0878DF3C)](#trigger-0878df3c).
4. Enable and reset applicable timers for [Allly Latin (0CC0044C)](#trigger-0cc0044c).
5. Enable and reset applicable timers for [Ally British (0CC00E5C)](#trigger-0cc00e5c).
6. Enable and reset applicable timers for [Ally Germans (0CBFF28C)](#trigger-0cbff28c).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3097, Events line 3154, Actions line 3211.

<a id="trigger-0878df3c"></a>

### 3. Ally Americans - 0878DF3C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Pres is Captured (0873BB5C)](#trigger-0873bb5c).

Attached scope: tag definitions 0878DCAC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Make ally: owner selector 5 (country/type AFRICANS; placed owner Africans).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3098, Events line 3155, Actions line 3212.

<a id="trigger-0cc0044c"></a>

### 4. Allly Latin - 0CC0044C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Pres is Captured (0873BB5C)](#trigger-0873bb5c).

Attached scope: tag definitions 0CC0024C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Make ally: owner selector 5 (country/type AFRICANS; placed owner Africans).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3099, Events line 3156, Actions line 3213.

<a id="trigger-0cc00e5c"></a>

### 5. Ally British - 0CC00E5C

Owner reference: British. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Pres is Captured (0873BB5C)](#trigger-0873bb5c).

Attached scope: tag definitions 0CC0094C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Make ally: owner selector 5 (country/type AFRICANS; placed owner Africans).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3100, Events line 3157, Actions line 3214.

<a id="trigger-0cbff28c"></a>

### 6. Ally Germans - 0CBFF28C

Owner reference: Germans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Pres is Captured (0873BB5C)](#trigger-0873bb5c).

Attached scope: tag definitions 0CC00F4C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Make ally: owner selector 5 (country/type AFRICANS; placed owner Africans).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3101, Events line 3158, Actions line 3215.

<a id="trigger-086a4ccc"></a>

### 7. Pres is Dead - 086A4CCC

Owner reference: French. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Pres is Captured (0873BB5C)](#trigger-0873bb5c).

Attached scope: tag definitions 07A4F52C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. First damaged (any source). See attached-object/cell scope below.

**Then perform these actions in order:**

1. Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the loser.
2. Play voice notification EVA_CriticalUnitLost.

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3102, Events line 3159, Actions line 3216.

<a id="trigger-07a59a6c"></a>

### 8. Southern Patrol - 07A59A6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07A5986C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [Southern Patrol (08BA2CCC)](sov09u-teams.md#team-08ba2ccc).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3103, Events line 3160, Actions line 3217.

<a id="trigger-0a53a1dc"></a>

### 9. Reactive Defense - 0A53A1DC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A53B94C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 5 (country/type AFRICANS; placed owner Africans).

**Then perform these actions in order:**

1. Create/recruit team [Northern Defenders (0872F6DC)](sov09u-teams.md#team-0872f6dc).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3104, Events line 3161, Actions line 3218.

<a id="trigger-0757067c"></a>

### 10. Player in Base - 0757067C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 35 tagged map cells: (58, 53), (60, 53), (61, 53), (62, 53), (66, 53), (67, 53), (71, 54), (72, 54), (73, 54), (73, 55), (74, 55), (56, 57), (73, 57), (56, 58), (72, 58), (73, 58), (56, 59), (73, 59), (56, 60), (74, 60), (59, 61), (73, 61), (74, 61), (58, 62), (59, 62), (60, 62), (60, 63), (74, 63), (60, 64), (61, 64), (74, 64), (66, 66), (67, 66), (72, 67), (73, 67); tag 0757013C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 5 (country/type AFRICANS; placed owner Africans).

**Then perform these actions in order:**

1. All to Hunt: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3105, Events line 3162, Actions line 3219.

<a id="trigger-07a7507c"></a>

### 11. Yuri's are Dead - 07A7507C

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Yuri Dead (03EAB030)](#trigger-03eab030).

Attached scope: tag definitions 07A7692C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  All: owner selector 5 (country/type AFRICANS; placed owner Africans).

**Then perform these actions in order:**

1. Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the loser.

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3106, Events line 3163, Actions line 3220.

<a id="trigger-08e6d1bc"></a>

### 12. ifv patrol - 08E6D1BC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08E6D62C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [ifv patrol (090B3A4C)](sov09u-teams.md#team-090b3a4c) at waypoint 24 (cell 37, 52).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3107, Events line 3164, Actions line 3221.

<a id="trigger-03e6df3c"></a>

### 13. Text - Obj1 - 03E6DF3C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03E6CE6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 105 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “Objective 1: Use Mind-Control to capture the President” (MISSION:Sov09a).
2. Create radar-event marker type 5 at waypoint 0 (cell 64, 59).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3108, Events line 3165, Actions line 3222.

<a id="trigger-03e6827c"></a>

### 14. Text - Hint1 - 03E6827C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03E680EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 93 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “Use America's own soldiers against them” (MISSION:Sov09b).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3109, Events line 3166, Actions line 3223.

<a id="trigger-08f4286c"></a>

### 15. Reveal All - 08F4286C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08F4232C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal the whole map.

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3110, Events line 3167, Actions line 3224.

<a id="trigger-0933136c"></a>

### 16. Wall Patrol Teams - 0933136C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0933774C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [lower left patrol (0CBEFA4C)](sov09u-teams.md#team-0cbefa4c) at waypoint 26 (cell 57, 73).
2. Supply reinforcement team [upper right patrol (08D9846C)](sov09u-teams.md#team-08d9846c) at waypoint 28 (cell 56, 48).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3111, Events line 3168, Actions line 3225.

<a id="trigger-08f00efc"></a>

### 17. SEAL Power Plant - 08F00EFC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08F009BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Seal Power Plant (08F03B4C)](sov09u-teams.md#team-08f03b4c) at waypoint 30 (cell 62, 50).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3112, Events line 3169, Actions line 3226.

<a id="trigger-07b7c7bc"></a>

### 18. Reminder - 07B7C7BC

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B7951C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 360 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “Objective 1: Use Mind-Control to capture the President” (MISSION:Sov09a).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3113, Events line 3170, Actions line 3227.

<a id="trigger-07b7942c"></a>

### 19. Ping Bases - 07B7942C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B7A13C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 150 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 23 (cell 32, 49).
2. Create radar-event marker type 5 at waypoint 33 (cell 85, 35).
3. Display message “Enemy bases detected” (MISSION:Sov09c).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3114, Events line 3171, Actions line 3228.

<a id="trigger-07b7bbac"></a>

### 20. Ping Again - 07B7BBAC

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B7B69C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 180 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create radar-event marker type 5 at waypoint 23 (cell 32, 49).
2. Create radar-event marker type 5 at waypoint 33 (cell 85, 35).
3. Display message “Enemy bases detected” (MISSION:Sov09c).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3115, Events line 3172, Actions line 3229.

<a id="trigger-08eee03c"></a>

### 21. Initial Drop - 08EEE03C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08EDF03C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [Drop Group 1 (08F74C8C)](sov09u-teams.md#team-08f74c8c) at waypoint 34 (cell 50, 54).
2. Supply reinforcement team [Drop Group 2 (0A41E93C)](sov09u-teams.md#team-0a41e93c) at waypoint 36 (cell 47, 55).
3. Supply reinforcement team [Drop Group 3 (08F7459C)](sov09u-teams.md#team-08f7459c) at waypoint 35 (cell 50, 58).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3116, Events line 3173, Actions line 3230.

<a id="trigger-08ec703c"></a>

### 22. create patrol IFV - 08EC703C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08EF304C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 75 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Northern Patrol (0871BC9C)](sov09u-teams.md#team-0871bc9c) at waypoint 7 (cell 52, 55).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3117, Events line 3174, Actions line 3231.

<a id="trigger-07b8036c"></a>

### 23. Lock Input - 07B8036C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B835DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable player input.
2. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3118, Events line 3175, Actions line 3232.

<a id="trigger-07b834ec"></a>

### 24. Scroll Camera - 07B834EC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B84F0C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Move the camera to waypoint 37 (cell 35, 70) with speed setting 2.

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3119, Events line 3176, Actions line 3233.

<a id="trigger-07b79b4c"></a>

### 25. Unlock Input - 07B79B4C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B7FCCC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 65 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable player input.
2. Enable and reset applicable timers for [Text - Use US Remind (092CCD8C)](#trigger-092ccd8c).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3120, Events line 3177, Actions line 3234.

<a id="trigger-092ccd8c"></a>

### 26. Text - Use US Remind - 092CCD8C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Unlock Input (07B79B4C)](#trigger-07b79b4c).

Attached scope: tag definitions 092CC44C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 140 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Use America's own soldiers against them” (MISSION:Sov09b).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3121, Events line 3178, Actions line 3235.

<a id="trigger-07b080cc"></a>

### 27. Make Spy Team - 07B080CC

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07B0983C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [spy team (0AC22EFC)](sov09u-teams.md#team-0ac22efc).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3122, Events line 3179, Actions line 3236.

<a id="trigger-07c7badc"></a>

### 28. Yuri Drop - 07C7BADC

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Yuri Drop (0A4656DC)](sov09u-teams.md#team-0a4656dc) at waypoint 37 (cell 35, 70).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3123, Events line 3180, Actions line 3237.

<a id="trigger-0a73f88c"></a>

### 29. Text Object 1 Remind - 0A73F88C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A73FC2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “Objective 1: Use Mind-Control to capture the President” (MISSION:Sov09a).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3124, Events line 3181, Actions line 3238.

<a id="trigger-07cd2c6c"></a>

### 30. Switch Power House - 07CD2C6C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07CD272C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Change House: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3125, Events line 3182, Actions line 3239.

<a id="trigger-08fd2cdc"></a>

### 31. Battle Lab Captured - 08FD2CDC

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Battle Lab (GATECH), owner Alliance, cell (31, 44), tag 08FD794C, persistence mode 0.

**Wait for the recorded events:**

1. Building exists: type index 6 (global list position: Allied Battle Lab (GATECH)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3126, Events line 3183, Actions line 3240.

<a id="trigger-09c480c0"></a>

### 32. Captured Barracks - 09C480C0

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Barracks (GAPILE), owner Alliance, cell (33, 48), tag 09B510D0, persistence mode 0.

**Wait for the recorded events:**

1. Building exists: type index 3 (global list position: Allied Barracks (GAPILE)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Change House: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. Enable and reset applicable timers for [Flip Tab (07B35C6C)](#trigger-07b35c6c).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3127, Events line 3184, Actions line 3241.

<a id="trigger-07b35c6c"></a>

### 33. Flip Tab - 07B35C6C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Captured Barracks (09C480C0)](#trigger-09c480c0).

Attached scope: tag definitions 07B3561C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Switch the sidebar to tab 2.

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3128, Events line 3185, Actions line 3242.

<a id="trigger-03eab030"></a>

### 34. Enable Yuri Dead - 03EAB030

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03EABF50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 100 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Yuri's are Dead (07A7507C)](#trigger-07a7507c).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3129, Events line 3186, Actions line 3243.

<a id="trigger-07f3773c"></a>

### 35. Spot Radar - 07F3773C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Radar Tower (NARADR), owner Neutral, cell (59, 117), tag 07F32EEC, persistence mode 0.

**Wait for the recorded events:**

1. 65 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Change House: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. Display message “--Battle Control Online--” (MISSION:ALL01q).
3. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3130, Events line 3187, Actions line 3244.

<a id="trigger-092cbf3c"></a>

### 36. Txt Disable US Remind - 092CBF3C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: NightHawk Transport (SHAD), owner Alliance, cell (87, 35), tag 092CBBEC, persistence mode 0; Grizzly Battle Tank (MTNK), owner Alliance, cell (84, 36), tag 092CBBEC, persistence mode 0; Engineer (ENGINEER), owner British, cell (30, 46), tag 092CBBEC, persistence mode 0; Sniper (SNIPE), owner British, cell (83, 31), tag 092CBBEC, persistence mode 0.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 5 (country/type AFRICANS; placed owner Africans).

**Then perform these actions in order:**

1. Disable [Text - Use US Remind (092CCD8C)](#trigger-092ccd8c).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3131, Events line 3188, Actions line 3245.

<a id="trigger-082c788c"></a>

### 37. Ambient Sounds - 082C788C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 082C470C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_Traffic at waypoint 44 (cell 64, 23).
2. Play sound _Amb_UrbanMurmur1 at waypoint 45 (cell 100, 58).
3. Play sound _Amb_UrbanMurmur2 at waypoint 46 (cell 50, 88).
4. Play sound _Amb_Traffic at waypoint 47 (cell 23, 63).
5. Play sound _Amb_Traffic at waypoint 28 (cell 56, 48).
6. Play sound _Amb_UrbanMurmur2 at waypoint 68 (cell 26, 53).
7. Play sound _Amb_UrbanMurmur2 at waypoint 18 (cell 52, 39).
8. Play sound _Amb_UrbanMurmur2 at waypoint 12 (cell 77, 25).
9. Play sound _Amb_UrbanMurmur2 at waypoint 17 (cell 90, 59).
10. Play sound _Amb_UrbanMurmur2 at waypoint 16 (cell 78, 76).
11. Play sound _Amb_UrbanMurmur1 at waypoint 69 (cell 26, 77).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3132, Events line 3189, Actions line 3246.

<a id="trigger-0a3ccf3c"></a>

### 38. President Movie - 0A3CCF3C

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A3CC3BC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play in-game movie 115.

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3133, Events line 3190, Actions line 3247.

<a id="trigger-09e41dcc"></a>

### 39. Create IFV Free Teams - 09E41DCC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09E4173C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [IFV Is Un-Mind Controled (0C0F3A9C)](sov09u-teams.md#team-0c0f3a9c).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3134, Events line 3191, Actions line 3248.

<a id="trigger-0839ff3c"></a>

### 40. Easy - Extra Engineer - 0839FF3C

Owner reference: British. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0839FA6C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Supply reinforcement team [1 Extra Engineer (0839CA9C)](sov09u-teams.md#team-0839ca9c) at waypoint 53 (cell 31, 46).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3135, Events line 3192, Actions line 3249.

<a id="trigger-0a41304c"></a>

### 41. Yuri Drop - Easy - 0A41304C

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Yuri Drop (07C7BADC)](#trigger-07c7badc).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Yuri Drop Easy (0A4751FC)](sov09u-teams.md#team-0a4751fc) at waypoint 37 (cell 35, 70).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3136, Events line 3193, Actions line 3250.

<a id="trigger-0a41405c"></a>

### 42. Yuri Drop Hard - 0A41405C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: [Yuri Drop - Easy (0A41304C)](#trigger-0a41304c).

Attached scope: tag definitions 07C7CD2C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [Yuri Drop Hard (0A474DEC)](sov09u-teams.md#team-0a474dec) at waypoint 37 (cell 35, 70).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3137, Events line 3194, Actions line 3251.

<a id="trigger-0417477c"></a>

### 43. Crate BD - 0417477C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Truck (loaded) (TRUCKB), owner Neutral, cell (101, 66), tag 0417469C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 55 (cell 102, 66).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3138, Events line 3195, Actions line 3252.

<a id="trigger-041745ac"></a>

### 44. Crate BE - 041745AC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Truck (loaded) (TRUCKB), owner Neutral, cell (101, 67), tag 041743CC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 56 (cell 102, 67).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3139, Events line 3196, Actions line 3253.

<a id="trigger-041742dc"></a>

### 45. Crate BF - 041742DC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Truck (loaded) (TRUCKB), owner Neutral, cell (101, 68), tag 0416735C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 57 (cell 102, 68).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3140, Events line 3197, Actions line 3254.

<a id="trigger-04164c1c"></a>

### 46. Crate BG - 04164C1C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Truck (loaded) (TRUCKB), owner Neutral, cell (96, 66), tag 041654BC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 9 at waypoint 58 (cell 95, 66).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3141, Events line 3198, Actions line 3255.

<a id="trigger-04162f3c"></a>

### 47. Crate BH - 04162F3C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Truck (loaded) (TRUCKB), owner Neutral, cell (96, 67), tag 041620AC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 11 at waypoint 59 (cell 95, 67).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3142, Events line 3199, Actions line 3256.

<a id="trigger-041636ac"></a>

### 48. Crate BI - 041636AC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Truck (loaded) (TRUCKB), owner Neutral, cell (96, 68), tag 041635CC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 14 at waypoint 60 (cell 95, 68).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3143, Events line 3200, Actions line 3257.

<a id="trigger-083ba9cc"></a>

### 49. create Pres Guards - 083BA9CC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 083BA30C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 35 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Presidente Guards (0ABE496C)](sov09u-teams.md#team-0abe496c) at waypoint 61 (cell 61, 65).
2. Supply reinforcement team [Presidente (0AD0F7DC)](sov09u-teams.md#team-0ad0f7dc) at waypoint 61 (cell 61, 65).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3144, Events line 3201, Actions line 3258.

<a id="trigger-08c7d24c"></a>

### 50. Ambient Birds - 08C7D24C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A5A99CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsPark at waypoint 26 (cell 57, 73).
2. Play sound _Amb_BirdsTemperate1 at waypoint 63 (cell 68, 98).
3. Play sound _Amb_BirdsPark at waypoint 64 (cell 67, 88).
4. Play sound _Amb_BirdsTemperate1 at waypoint 65 (cell 58, 35).
5. Play sound _Amb_BirdsPark at waypoint 66 (cell 101, 51).
6. Play sound _Amb_BirdsPark at waypoint 67 (cell 84, 82).
7. Play sound _Amb_BirdsTemperate1 at waypoint 70 (cell 11, 64).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3145, Events line 3202, Actions line 3259.

<a id="trigger-0a27f75c"></a>

### 51. text hint - 2 - 0A27F75C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A27F2EC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 6 (global list position: Allied Battle Lab (GATECH)). A map-local type-list change can affect index interpretation.
2. Building exists: type index 3 (global list position: Allied Barracks (GAPILE)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Display message “Order spies to enter power plants to sabotage base power” (MISSION:SOV09d).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3146, Events line 3203, Actions line 3260.

<a id="trigger-0c1c9d8c"></a>

### 52. Alamo Destroyed - 0C1C9D8C

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Alamo (CATEXS02), owner Neutral, cell (62, 64), tag 0C1C933C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by any house. See attached-object/cell scope below.

**Then perform these actions in order:**

1. All to Hunt: owner selector 3 (country/type GERMANS; placed owner Germans).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3147, Events line 3204, Actions line 3261.

<a id="trigger-084ffc6c"></a>

### 53. Airport Captured - 084FFC6C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 084FF70C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 70 (global list position: Tech Airport (CAAIRP)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play voice notification EVA_NewConstructionOptions.

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3148, Events line 3205, Actions line 3262.

<a id="trigger-0abbe1dc"></a>

### 54. Create Civies - 0ABBE1DC

Owner reference: Germans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AD2A04C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 90 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Civilian 1 (0ABB535C)](sov09u-teams.md#team-0abb535c).
2. Create/recruit team [Civilian 2 (0ABBFEFC)](sov09u-teams.md#team-0abbfefc).
3. Create/recruit team [Civilian 3 (0AF4D6CC)](sov09u-teams.md#team-0af4d6cc).
4. Create/recruit team [Civilian 4 (0AF51EFC)](sov09u-teams.md#team-0af51efc).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3149, Events line 3206, Actions line 3263.

<a id="trigger-0d36a0fc"></a>

### 55. SEALs Killed - 0D36A0FC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0D37006C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. First damaged (any source). See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [6 SEALs (0D37AD0C)](sov09u-teams.md#team-0d37ad0c).

Source locator: MAPS02.MIX/sov09u.map; Triggers line 3150, Events line 3207, Actions line 3264.

[All team rosters and ordered plans](sov09u-teams.md) | [All mission overrides](sov09u-overrides.md)
