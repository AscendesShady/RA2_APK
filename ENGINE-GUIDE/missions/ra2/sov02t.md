# Operation: Hostile Shore

[Campaign reading guide](../../05-CAMPAIGNS.md) | [Engine](../../01-ENGINE-WORKFLOW.md)

**Map:** sov02t.map. **Effective extracted member:** MAPS02.MIX/sov02t.map. **Trigger definitions:** 76.

This is a translated static ledger, not a recorded playthrough. Trigger numbering below is browsing order, not chronological execution. Each trigger still requires eligibility, enabling, relevant attachments and its event logic. Values called time units remain in the source scale; no unverified wall-clock conversion is applied.

Read an event as applying to the trigger's attached scope when it is object/cell-specific. Multiple event entries are recorded conditions for the trigger, not alternative objectives unless the runtime's event logic makes them so. Tag persistence modes: 0 consumes on the relevant first occurrence; 1 waits for the applicable attached-object completion; 2 permits repeating. Not all definitions have a live attached instance.


[All team rosters and ordered plans](sov02t-teams.md) | [All mission overrides](sov02t-overrides.md)

## Starting world

| Part | Recorded value |
| --- | --- |
| Player house | Confederation |
| Theater | TEMPERATE |
| Map size | 0,0,71,103 |
| Visible local rectangle | 2,5,64,89 |
| Placed vehicles | 46 |
| Placed infantry | 42 |
| Placed structures | 136 |
| Placed aircraft | 0 |
| Team templates | 42 |

### Houses

| Map house slot | Owner name | Starting credits setting | Country |
| --- | --- | --- | --- |
| 0 | Americans | 500 | Americans |
| 1 | Alliance | 0 | Alliance |
| 2 | French | 0 | French |
| 3 | Germans | 0 | Germans |
| 4 | British | 500 | British |
| 5 | Africans | 10 | Africans |
| 6 | Arabs | 0 | Arabs |
| 7 | Confederation | 50 | Confederation |
| 8 | Russians | 0 | Russians |
| 9 | GDI | 0 | GDI |
| 10 | Nod | 0 | Nod |
| 11 | Neutral | 0 | Neutral |
| 12 | Special | 0 | Special |

### Local state flags at initialization

| Flag | Meaning label and initial value |
| --- | --- |
| 0 | MCV Landed,0 |
| 1 | Hotels Destroyed,0 |
| 2 | Transports Unloaded,0 |
| 3 | Vlad is Hit,0 |

## Terminal gates: victory, defeat or forced end

These records can issue an outcome or its announcement. An announcement is distinguished from the actual winner/loser action. Follow the linked trigger for all guards and action order.

| Gate | Conditions recorded | Terminal-related actions |
| --- | --- | --- |
| [Player Win - Final (0CBCDB0C)](#trigger-0cbcdb0c) | 5 configured time units have elapsed since the trigger timer was initialized/reset. | Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the winner. |
| [Player Loses (089D1680)](#trigger-089d1680) | Destroyed,  All: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).<br>20 configured time units have elapsed since scenario start. | Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the loser. |

## Every trigger, in file order

<a id="trigger-06a94550"></a>

### 1. Open Start - 06A94550

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 98 (cell 93, 50).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4783, Events line 4861, Actions line 4939.

<a id="trigger-09388f60"></a>

### 2. Reveal at Start - 09388F60

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09388AD0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 98 (cell 93, 50).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4784, Events line 4862, Actions line 4940.

<a id="trigger-06da18d0"></a>

### 3. wave 2.1 - 06DA18D0

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Wave 2.1 (0C4B3C4C)](sov02t-teams.md#team-0c4b3c4c) at waypoint 19 (cell 98, 41).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4785, Events line 4863, Actions line 4941.

<a id="trigger-07fd8060"></a>

### 4. PC Tank 1 - 07FD8060

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08097D10 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [PC Landers 2 (0C4B403C)](sov02t-teams.md#team-0c4b403c) at waypoint 3 (cell 99, 42).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4786, Events line 4864, Actions line 4942.

<a id="trigger-08097080"></a>

### 5. PC Tank 2 - 08097080

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0809F4C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [PC Landers 3 (0C4B190C)](sov02t-teams.md#team-0c4b190c) at waypoint 4 (cell 101, 44).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4787, Events line 4865, Actions line 4943.

<a id="trigger-09819300"></a>

### 6. Vladimir's Attack - 09819300

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player has built sub (08E056AC)](#trigger-08e056ac); enable from [Player has attacked (08E0042C)](#trigger-08e0042c); enable from [Player's Time has Run Out (08E32B9C)](#trigger-08e32b9c).

Attached scope: tag definitions 0981ABF0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Vlad Attack Team (0AFD1B5C)](sov02t-teams.md#team-0afd1b5c).
2. Create/recruit team [Vlad's Charge Team (0A9DE7DC)](sov02t-teams.md#team-0a9de7dc).
3. Play in-game movie 77.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4788, Events line 4866, Actions line 4944.

<a id="trigger-096fcea0"></a>

### 7. Destroyer Attack - 096FCEA0

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: 1 tagged map cells: (113, 94); tag 09704F70, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 8 (country/type RUSSIANS; placed owner Russians).

**Then perform these actions in order:**

1. Make enemy: owner selector 8 (country/type RUSSIANS; placed owner Russians).
2. Enable and reset applicable timers for [Kill Vlad! (08743820)](#trigger-08743820).
3. Play in-game movie 78.
4. Reveal terrain around waypoint 69 (cell 120, 116).
5. Reveal terrain around waypoint 60 (cell 123, 125).
6. Reveal terrain around waypoint 94 (cell 117, 124).
7. Reveal terrain around waypoint 96 (cell 118, 109).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4789, Events line 4867, Actions line 4945.

<a id="trigger-08743820"></a>

### 8. Kill Vlad! - 08743820

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroyer Attack (096FCEA0)](#trigger-096fcea0).

Attached scope: tag definitions 08743350 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [3 Destroyers (09EC293C)](sov02t-teams.md#team-09ec293c).
2. Enable and reset applicable timers for [Free Subs have Arrived (0A4EAA2C)](#trigger-0a4eaa2c).
3. Enable and reset applicable timers for [Free Subs Easy (0860A3EC)](#trigger-0860a3ec).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4790, Events line 4868, Actions line 4946.

<a id="trigger-0a4eaa2c"></a>

### 9. Free Subs have Arrived - 0A4EAA2C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 0, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Kill Vlad! (08743820)](#trigger-08743820).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [6 Free Subs (09E2A1FC)](sov02t-teams.md#team-09e2a1fc) at waypoint 55 (cell 102, 37).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Create radar-event marker type 0 at waypoint 36 (cell 98, 48).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4791, Events line 4869, Actions line 4947.

<a id="trigger-0860a3ec"></a>

### 10. Free Subs Easy - 0860A3EC

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 0, Hard 0 (1 means included). Linked trigger: [Free Subs have Arrived (0A4EAA2C)](#trigger-0a4eaa2c).

Incoming activation links: enable from [Kill Vlad! (08743820)](#trigger-08743820).

Attached scope: tag definitions 0A4EA72C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Supply reinforcement team [10 Free Subs (08608AEC)](sov02t-teams.md#team-08608aec) at waypoint 55 (cell 102, 37).
2. Play voice notification EVA_ReinforcementsHaveArrived.
3. Create radar-event marker type 2 at waypoint 36 (cell 98, 48).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4792, Events line 4870, Actions line 4948.

<a id="trigger-0aaa576c"></a>

### 11. Vlad's Return - 0AAA576C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Vlad runs again (0AAA52DC)](#trigger-0aaa52dc).

Attached scope: tag definitions 0AAA53CC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 200 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Vlad has been hit (0AC5B14C)](#trigger-0ac5b14c).
2. Supply reinforcement team [Vlad Sneaks Back On (0AB8380C)](sov02t-teams.md#team-0ab8380c) at waypoint 55 (cell 102, 37).
3. Disable [Vlad's Return (0AAA576C)](#trigger-0aaa576c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4793, Events line 4871, Actions line 4949.

<a id="trigger-0ac5b14c"></a>

### 12. Vlad has been hit - 0AC5B14C

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Vlad's Return (0AAA576C)](#trigger-0aaa576c).

Attached scope: tag definitions 0AC5BF4C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Attacked by (house): owner selector 0 (country/type AMERICANS; placed owner Americans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Vlad runs again (0AAA52DC)](#trigger-0aaa52dc).
2. Enable and reset applicable timers for [2 Destroyer Attack (0BA2C61C)](#trigger-0ba2c61c).
3. Disable [Vlad has been hit (0AC5B14C)](#trigger-0ac5b14c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4794, Events line 4872, Actions line 4950.

<a id="trigger-0aaa52dc"></a>

### 13. Vlad runs again - 0AAA52DC

Owner reference: Russians. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Vlad has been hit (0AC5B14C)](#trigger-0ac5b14c).

Attached scope: tag definitions 0AAA6CBC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Vlad Sneaks Back On (0AB8380C)](sov02t-teams.md#team-0ab8380c).
2. Create/recruit team [vlad runs again (0AF55B5C)](sov02t-teams.md#team-0af55b5c).
3. Enable and reset applicable timers for [Vlad's Return (0AAA576C)](#trigger-0aaa576c).
4. Disable [Vlad runs again (0AAA52DC)](#trigger-0aaa52dc).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4795, Events line 4873, Actions line 4951.

<a id="trigger-0ba2c61c"></a>

### 14. 2 Destroyer Attack - 0BA2C61C

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Vlad has been hit (0AC5B14C)](#trigger-0ac5b14c).

Attached scope: tag definitions 0BA2C31C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Create/recruit team [Destroyer Attack (0CF1832C)](sov02t-teams.md#team-0cf1832c).
2. Disable [2 Destroyer Attack (0BA2C61C)](#trigger-0ba2c61c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4796, Events line 4874, Actions line 4952.

<a id="trigger-07b11750"></a>

### 15. American Troops Build - 07B11750

Owner reference: Americans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [USA 1st Attack (0A26E840)](#trigger-0a26e840); enable from [Player has Built (089F5CE0)](#trigger-089f5ce0).

Attached scope: tag definitions 07B11210 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Production Begins: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. AI triggers begin: owner selector 0 (country/type AMERICANS; placed owner Americans).
3. Make enemy: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4797, Events line 4875, Actions line 4953.

<a id="trigger-07b18f60"></a>

### 16. wave 2.2 - 07B18F60

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [wave 2.1 (06DA18D0)](#trigger-06da18d0).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [Wave 2.2 (09F15C8C)](sov02t-teams.md#team-09f15c8c) at waypoint 3 (cell 99, 42).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4798, Events line 4876, Actions line 4954.

<a id="trigger-07b18c70"></a>

### 17. wave 2.3 - 07B18C70

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [wave 2.2 (07B18F60)](#trigger-07b18f60).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [wave 2.3 (0C4B308C)](sov02t-teams.md#team-0c4b308c) at waypoint 4 (cell 101, 44).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4799, Events line 4877, Actions line 4955.

<a id="trigger-0719ea80"></a>

### 18. Player Wins - 0719EA80

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0719B030 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. Destroyed,  All: owner selector 3 (country/type GERMANS; placed owner Germans).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [All to Cheer (0CBCE79C)](#trigger-0cbce79c).
2. Enable and reset applicable timers for [Player Win - Final (0CBCDB0C)](#trigger-0cbcdb0c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4800, Events line 4878, Actions line 4956.

<a id="trigger-0cbce79c"></a>

### 19. All to Cheer - 0CBCE79C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Wins (0719EA80)](#trigger-0719ea80).

Attached scope: tag definitions 0CBCDBFC (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 3 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Make side cheer: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4801, Events line 4879, Actions line 4957.

<a id="trigger-0cbcdb0c"></a>

### 20. Player Win - Final - 0CBCDB0C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player Wins (0719EA80)](#trigger-0719ea80).

Attached scope: tag definitions 0CBCD90C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the winner.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4802, Events line 4880, Actions line 4958.

<a id="trigger-0a248f60"></a>

### 21. Wave 2.4 - 0A248F60

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: [wave 2.3 (07B18C70)](#trigger-07b18c70).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [wave 2.4 (0C4B0C8C)](sov02t-teams.md#team-0c4b0c8c) at waypoint 25 (cell 100, 43).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4803, Events line 4881, Actions line 4959.

<a id="trigger-0a249990"></a>

### 22. Wave 2.5 - 0A249990

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: [Wave 2.4 (0A248F60)](#trigger-0a248f60).

Attached scope: tag definitions 09386EB0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Supply reinforcement team [wave 2.5 (0C4B08EC)](sov02t-teams.md#team-0c4b08ec) at waypoint 26 (cell 99, 41).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4804, Events line 4882, Actions line 4960.

<a id="trigger-0a225f60"></a>

### 23. Vlad Shoots - 0A225F60

Owner reference: Russians. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A225920 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 1 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Vlad Attack Team (0AFD1B5C)](sov02t-teams.md#team-0afd1b5c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4805, Events line 4883, Actions line 4961.

<a id="trigger-0b8b5680"></a>

### 24. Reveal Beach - 0B8B5680

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B8B51C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 24 (cell 89, 56).
2. Reveal terrain around waypoint 23 (cell 81, 60).
3. Reveal terrain around waypoint 0 (cell 80, 55).
4. Reveal terrain around waypoint 29 (cell 95, 52).
5. Reveal terrain around waypoint 30 (cell 82, 46).
6. Reveal terrain around waypoint 1 (cell 97, 40).
7. Reveal terrain around waypoint 21 (cell 102, 46).
8. Reveal terrain around waypoint 20 (cell 94, 38).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4806, Events line 4884, Actions line 4962.

<a id="trigger-0a26e840"></a>

### 25. USA 1st Attack - 0A26E840

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Player has Built (089F5CE0)](#trigger-089f5ce0).

Attached scope: 1 tagged map cells: (72, 58); tag 0A26E380, persistence mode 0.

**Wait for the recorded events:**

1. Crosses Vertical Line: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

**Then perform these actions in order:**

1. Create/recruit team [USA first attack (0AD69C8C)](sov02t-teams.md#team-0ad69c8c).
2. Reveal terrain around waypoint 54 (cell 69, 58).
3. Enable and reset applicable timers for [American Troops Build (07B11750)](#trigger-07b11750).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4807, Events line 4885, Actions line 4963.

<a id="trigger-089d1680"></a>

### 26. Player Loses - 089D1680

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089D3AB0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  All: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. 20 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Declare owner selector 7 (country/type CONFEDERATION; placed owner Confederation) the loser.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4808, Events line 4886, Actions line 4964.

<a id="trigger-089f5ce0"></a>

### 27. Player has Built - 089F5CE0

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 089F59E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [USA 1st Attack (0A26E840)](#trigger-0a26e840).
2. Enable and reset applicable timers for [American Troops Build (07B11750)](#trigger-07b11750).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4809, Events line 4887, Actions line 4965.

<a id="trigger-0ac91480"></a>

### 28. Lock Input - 0AC91480

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AC92D90 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Disable player input.
2. Move the camera to waypoint 0 (cell 80, 55) with speed setting 1.
3. Play voice notification EVA_EstablishBattlefieldControl.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4810, Events line 4888, Actions line 4966.

<a id="trigger-0ac92cb0"></a>

### 29. Unlock - 0AC92CB0

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0AC92870 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Transports Unloaded) is set.

**Then perform these actions in order:**

1. Enable player input.
2. Play voice notification EVA_BattlefieldControlOnline.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4811, Events line 4889, Actions line 4967.

<a id="trigger-09e6b790"></a>

### 30. Boat Patrol - 09E6B790

Owner reference: British. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09E6B2C0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 0 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Destroyer Patrols (08CD1CDC)](sov02t-teams.md#team-08cd1cdc).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4812, Events line 4890, Actions line 4968.

<a id="trigger-09ef6f40"></a>

### 31. American Destroyer Attack - 09EF6F40

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09EF6A00 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Create/recruit team [Destroyer Attack (0CF1832C)](sov02t-teams.md#team-0cf1832c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4813, Events line 4891, Actions line 4969.

<a id="trigger-07c9e0e0"></a>

### 32. Objective 1 - 07C9E0E0

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C9EF50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Display message “Objective 1: Force a beach landing and build a base” (MISSION:Sov02a).
2. Play voice notification EVA_NewMissionObjective.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4814, Events line 4892, Actions line 4970.

<a id="trigger-07c9ee70"></a>

### 33. Objective 2 - 07C9EE70

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07C99C90 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 25 (global list position: Soviet Construction Yard (NACNST)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Display message “Objective 1 Complete” (MISSION:Objective1).
2. Enable and reset applicable timers for [Remind Player of Object (03E9A47C)](#trigger-03e9a47c).
3. Enable and reset applicable timers for [Objective 2 Sounds (0AABD06C)](#trigger-0aabd06c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4815, Events line 4893, Actions line 4971.

<a id="trigger-03e9a47c"></a>

### 34. Remind Player of Object - 03E9A47C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 2 (07C9EE70)](#trigger-07c9ee70).

Attached scope: tag definitions 03E9819C (persistence 2); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 75 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy all enemy forces” (MISSION:Sov02b).
2. Play sound MessageText.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4816, Events line 4894, Actions line 4972.

<a id="trigger-0aabd06c"></a>

### 35. Objective 2 Sounds - 0AABD06C

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Objective 2 (07C9EE70)](#trigger-07c9ee70).

Attached scope: tag definitions 0AAD318C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Display message “Objective 2: Destroy all enemy forces” (MISSION:Sov02b).
2. Play voice notification EVA_NewMissionObjective.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4817, Events line 4895, Actions line 4973.

<a id="trigger-08e056ac"></a>

### 36. Player has built sub - 08E056AC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Build Unit Type: type index 19 (global list position: Typhoon Attack Sub (SUB)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Vladimir's Attack (09819300)](#trigger-09819300).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4818, Events line 4896, Actions line 4974.

<a id="trigger-08e0042c"></a>

### 37. Player has attacked - 08E0042C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player has built sub (08E056AC)](#trigger-08e056ac).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Crosses Horizontal Line: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Vladimir's Attack (09819300)](#trigger-09819300).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4819, Events line 4897, Actions line 4975.

<a id="trigger-08e32b9c"></a>

### 38. Player's Time has Run Out - 08E32B9C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Player has attacked (08E0042C)](#trigger-08e0042c).

Attached scope: 1 tagged map cells: (75, 100); tag 08E00B3C, persistence mode 0.

**Wait for the recorded events:**

1. 600 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Vladimir's Attack (09819300)](#trigger-09819300).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4820, Events line 4898, Actions line 4976.

<a id="trigger-07b27b40"></a>

### 39. create crate ba - 07B27B40

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM05), owner Neutral, cell (81, 93), tag 07B27520, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 52 (cell 81, 92).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4821, Events line 4899, Actions line 4977.

<a id="trigger-07b27440"></a>

### 40. AZ Crate - 07B27440

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM06), owner Neutral, cell (84, 74), tag 07B27270, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 14 at waypoint 51 (cell 84, 73).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4822, Events line 4900, Actions line 4978.

<a id="trigger-07b27190"></a>

### 41. BB Crate - 07B27190

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM07), owner Neutral, cell (87, 100), tag 07B28B70, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 14 at waypoint 53 (cell 88, 99).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4823, Events line 4901, Actions line 4979.

<a id="trigger-07af4970"></a>

### 42. End Mission - 07AF4970

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Construction Yard (GACNST), owner Americans, cell (79, 129), tag 07AF3F50, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Fire Sale: owner selector 0 (country/type AMERICANS; placed owner Americans).
2. All to Hunt: owner selector 0 (country/type AMERICANS; placed owner Americans).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4824, Events line 4902, Actions line 4980.

<a id="trigger-0a9c07e0"></a>

### 43. MCV Landed Hint - 0A9C07E0

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A9C0270 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (MCV Landed) is set.

**Then perform these actions in order:**

1. Create radar-event marker type 1 at waypoint 42 (cell 80, 58).
2. Display message “Your Mobile Construction Vehicle has landed. Double-click on it to create a Construction Yard” (MISSION:Sov02g).
3. Play voice notification EVA_ReinforcementsReady.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4825, Events line 4903, Actions line 4981.

<a id="trigger-03e2bb40"></a>

### 44. Fleet Detected - 03E2BB40

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 03E2CF50 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 11 (global list position: Soviet Barracks (NAHAND)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 9 (cell 113, 94).
2. Create radar-event marker type 5 at waypoint 9 (cell 113, 94).
3. Play voice notification EVA_EnemyFleetDetected.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4826, Events line 4904, Actions line 4982.

<a id="trigger-0add00e0"></a>

### 45. Give PC Radar - 0ADD00E0

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Radar Tower (NARADR), owner Neutral, cell (82, 13), tag 0ADD1BE0, persistence mode 0.

**Wait for the recorded events:**

1. local flag 2 (Transports Unloaded) is set.

**Then perform these actions in order:**

1. Change House: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).
2. Display message “--Battle Control Online--” (MISSION:ALL01q).
3. Reveal terrain around waypoint 50 (cell 83, 15).
4. Reshroud Map At; main setting 50; location/duration field AY.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4827, Events line 4905, Actions line 4983.

<a id="trigger-07f36c80"></a>

### 46. Transports Off - 07F36C80

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 07F352E0 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Transports Unloaded) is set.

**Then perform these actions in order:**

1. Create/recruit team [7 Transports (090EDCE0)](sov02t-teams.md#team-090edce0).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4828, Events line 4906, Actions line 4984.

<a id="trigger-07edc7b0"></a>

### 47. Send MCV Boat Away - 07EDC7B0

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroy MCV Team (0B0EE1BC)](#trigger-0b0ee1bc).

Attached scope: tag definitions 07EDFF20 (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [Make Boat Go Away (0A30E1FC)](sov02t-teams.md#team-0a30e1fc).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4829, Events line 4907, Actions line 4985.

<a id="trigger-0a39993c"></a>

### 48. Txt - MCV Selected - 0A39993C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A39959C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Selected by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Display message “Your Mobile Construction Vehicle has landed. Double-click on it to create a Construction Yard” (MISSION:Sov02g).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4830, Events line 4908, Actions line 4986.

<a id="trigger-0b10aa2c"></a>

### 49. Land the MCV - 0B10AA2C

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pill Box (GAPILL), owner Americans, cell (72, 53), tag 0B10A4EC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Supply reinforcement team [Land the MCV (0A550DCC)](sov02t-teams.md#team-0a550dcc) at waypoint 16 (cell 106, 66).
2. Enable and reset applicable timers for [1 MCV Reinforce Voice (0A99E5AC)](#trigger-0a99e5ac).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4831, Events line 4909, Actions line 4987.

<a id="trigger-0a99e5ac"></a>

### 50. 1 MCV Reinforce Voice - 0A99E5AC

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Land the MCV (0B10AA2C)](#trigger-0b10aa2c).

Attached scope: tag definitions 0A99DE9C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 10 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4832, Events line 4910, Actions line 4988.

<a id="trigger-09b9703c"></a>

### 51. Play Build Fleet Movie - 09B9703C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 15 (global list position: Soviet Ore Refinery (NAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play in-game movie 76.
2. Destroy current instances of [Play Fleet if A Refine (0871968C)](#trigger-0871968c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4833, Events line 4911, Actions line 4989.

<a id="trigger-0871968c"></a>

### 52. Play Fleet if A Refine - 0871968C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Play Build Fleet Movie (09B9703C)](#trigger-09b9703c).

Attached scope: no direct placed object/cell tag found; can be scenario-wide, linked or dynamically attached.

**Wait for the recorded events:**

1. Building exists: type index 1 (global list position: Allied Ore Refinery (GAREFN)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Play in-game movie 76.
2. Destroy current instances of [Play Build Fleet Movie (09B9703C)](#trigger-09b9703c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4834, Events line 4912, Actions line 4990.

<a id="trigger-0b0ee1bc"></a>

### 53. Destroy MCV Team - 0B0EE1BC

Owner reference: Africans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0B0EAB1C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 0 (MCV Landed) is set.

**Then perform these actions in order:**

1. Remove instances of the team organization (not automatically its surviving objects) [Land the MCV (0A550DCC)](sov02t-teams.md#team-0a550dcc).
2. Enable and reset applicable timers for [Send MCV Boat Away (07EDC7B0)](#trigger-07edc7b0).
3. Enable and reset applicable timers for [Change MCV House (0B0EAA2C)](#trigger-0b0eaa2c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4835, Events line 4913, Actions line 4991.

<a id="trigger-0b0eaa2c"></a>

### 54. Change MCV House - 0B0EAA2C

Owner reference: Africans. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Destroy MCV Team (0B0EE1BC)](#trigger-0b0ee1bc).

Attached scope: tag definitions 0B0EA82C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Create/recruit team [MCV ON the Beach (0A1DB35C)](sov02t-teams.md#team-0a1db35c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4836, Events line 4914, Actions line 4992.

<a id="trigger-0ab4fdbc"></a>

### 55. Flip Tab for Sub - 0AB4FDBC

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Enable Tab Flip (083F72EC)](#trigger-083f72ec).

Attached scope: tag definitions 0AB4F3DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 5 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Switch the sidebar to tab 3.
2. Play voice notification Unit_Sofia_Sub.
3. Flash cameo/type 319; additional configured duration/location argument 40.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4837, Events line 4915, Actions line 4993.

<a id="trigger-083f72ec"></a>

### 56. Enable Tab Flip - 083F72EC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 083F52DC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Building exists: type index 61 (global list position: Soviet Shipyard (NAYARD)). A map-local type-list change can affect index interpretation.

**Then perform these actions in order:**

1. Enable and reset applicable timers for [Flip Tab for Sub (0AB4FDBC)](#trigger-0ab4fdbc).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4838, Events line 4916, Actions line 4994.

<a id="trigger-08324a9c"></a>

### 57. Make Civlians Freak - 08324A9C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Civilian (CIVBFM), owner Neutral, cell (102, 95), tag 0832461C, persistence mode 0; Civilian (CIVBTM), owner Neutral, cell (100, 102), tag 0832461C, persistence mode 0; Civilian (CIVBF), owner Neutral, cell (103, 92), tag 0832461C, persistence mode 0; Civilian (CIVBF), owner Neutral, cell (99, 102), tag 0832461C, persistence mode 0; Civilian (CIVBF), owner Neutral, cell (93, 102), tag 0832461C, persistence mode 0; Civilian (CIVBTM), owner Neutral, cell (95, 102), tag 0832461C, persistence mode 0; Civilian (CIVBFM), owner Neutral, cell (92, 103), tag 0832461C, persistence mode 0; Civilian (CIVBTM), owner Neutral, cell (99, 92), tag 0832461C, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [9 Civilians (0A22FDEC)](sov02t-teams.md#team-0a22fdec).
2. Play sound CivAllFear.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4839, Events line 4917, Actions line 4995.

<a id="trigger-09ca6f3c"></a>

### 58. Send in More Troops! - 09CA6F3C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 0 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09CA6DEC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. Destroyed,  Units,  #: 14.

**Then perform these actions in order:**

1. Supply reinforcement team [Conscript Reinforcements (0A2B50DC)](sov02t-teams.md#team-0a2b50dc) at waypoint 40 (cell 74, 73).
2. Enable and reset applicable timers for [Para Reinforcement Audio (089608AC)](#trigger-089608ac).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4840, Events line 4918, Actions line 4996.

<a id="trigger-089608ac"></a>

### 59. Para Reinforcement Audio - 089608AC

Owner reference: Confederation. Initially disabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Incoming activation links: enable from [Send in More Troops! (09CA6F3C)](#trigger-09ca6f3c).

Attached scope: tag definitions 089604CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 20 configured time units have elapsed since the trigger timer was initialized/reset.

**Then perform these actions in order:**

1. Play voice notification EVA_ReinforcementsHaveArrived.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4841, Events line 4919, Actions line 4997.

<a id="trigger-07a4da5c"></a>

### 60. North Civis - 07A4DA5C

Owner reference: Neutral. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Civilian (CIVBFM), owner Neutral, cell (78, 37), tag 07A4D97C, persistence mode 0; Civilian (CIVBFM), owner Neutral, cell (79, 31), tag 07A4D97C, persistence mode 0; Civilian (CIVBF), owner Neutral, cell (78, 33), tag 07A4D97C, persistence mode 0; Civilian (CIVBF), owner Neutral, cell (81, 37), tag 07A4D97C, persistence mode 0; Civilian (CIVBTM), owner Neutral, cell (80, 38), tag 07A4D97C, persistence mode 0; Civilian (CIVBTM), owner Neutral, cell (79, 31), tag 07A4D97C, persistence mode 0; Civilian (CIVBF), owner Neutral, cell (73, 40), tag 07A4D97C, persistence mode 0; Civilian (CIVBTM), owner Neutral, cell (72, 38), tag 07A4D97C, persistence mode 0; Civilian (CIVBFM), owner Neutral, cell (73, 35), tag 07A4D97C, persistence mode 0.

**Wait for the recorded events:**

1. 30 configured time units have elapsed since scenario start.
2. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [9 Civies North (0A2271FC)](sov02t-teams.md#team-0a2271fc).
2. Play sound CivAllFear.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4842, Events line 4920, Actions line 4998.

<a id="trigger-07a489ac"></a>

### 61. Freak 3 - 07A489AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Civilian (CIVBFM), owner Neutral, cell (114, 112), tag 07A488CC, persistence mode 0; Civilian (CIVBFM), owner Neutral, cell (123, 113), tag 07A488CC, persistence mode 0; Civilian (CIVBF), owner Neutral, cell (126, 117), tag 07A488CC, persistence mode 0; Civilian (CIVBF), owner Neutral, cell (116, 111), tag 07A488CC, persistence mode 0; Civilian (CIVBTM), owner Neutral, cell (117, 109), tag 07A488CC, persistence mode 0; Civilian (CIVBTM), owner Neutral, cell (126, 119), tag 07A488CC, persistence mode 0.

**Wait for the recorded events:**

1. Discovered by player. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create/recruit team [6 Civies South (09F136AC)](sov02t-teams.md#team-09f136ac).
2. Play sound CivAllFear.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4843, Events line 4921, Actions line 4999.

<a id="trigger-0a10509c"></a>

### 62. Reveal Vlad Targets - 0A10509C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A104B3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 60 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Reveal terrain around waypoint 46 (cell 71, 43).
2. Reveal terrain around waypoint 47 (cell 70, 35).
3. Reveal terrain around waypoint 49 (cell 73, 28).
4. Reveal terrain around waypoint 48 (cell 76, 34).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4844, Events line 4922, Actions line 5000.

<a id="trigger-09fd0cbc"></a>

### 63. Transports Get Off Hard - 09FD0CBC

Owner reference: Arabs. Initially enabled. Difficulty eligibility: Easy 0, Normal 0, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 09FD09CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. local flag 2 (Transports Unloaded) is set.

**Then perform these actions in order:**

1. Create/recruit team [4 Transports - Hard (09DFF26C)](sov02t-teams.md#team-09dff26c).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4845, Events line 4923, Actions line 5001.

<a id="trigger-09cbe0dc"></a>

### 64. Secret Crate Truck BH - 09CBE0DC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Pickup Truck (PICK), owner Neutral, cell (45, 59), tag 09CB882C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 11 at waypoint 59 (cell 44, 59).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4846, Events line 4924, Actions line 5002.

<a id="trigger-09cde5dc"></a>

### 65. Secret Crate BI - 09CDE5DC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM07), owner Neutral, cell (123, 126), tag 09CDF07C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 60 (cell 123, 125).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4847, Events line 4925, Actions line 5003.

<a id="trigger-09cd939c"></a>

### 66. Secret Crate BJ - 09CD939C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM06), owner Neutral, cell (114, 130), tag 09CD916C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 61 (cell 115, 129).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4848, Events line 4926, Actions line 5004.

<a id="trigger-09cdfb5c"></a>

### 67. Secret Crate BK - 09CDFB5C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: McBurger Kong (CAMSC10), owner Neutral, cell (68, 91), tag 09CDF95C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 62 (cell 68, 90).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4849, Events line 4927, Actions line 5005.

<a id="trigger-09d9b4ac"></a>

### 68. Secret Crate BL - 09D9B4AC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Hotel (CAMIAM07), owner Neutral, cell (69, 33), tag 09D9B10C, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 63 (cell 70, 32).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4850, Events line 4928, Actions line 5006.

<a id="trigger-0a25472c"></a>

### 69. Ambient Crickets - 0A25472C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A25464C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_CricketChirps at waypoint 76 (cell 23, 78).
2. Play sound _Amb_CricketChirps at waypoint 77 (cell 38, 96).
3. Play sound _Amb_CricketBed at waypoint 78 (cell 48, 105).
4. Play sound _Amb_CricketBed at waypoint 79 (cell 61, 118).
5. Play sound _Amb_CricketBed at waypoint 80 (cell 71, 129).
6. Play sound _Amb_CricketBed at waypoint 81 (cell 87, 146).
7. Play sound _Amb_CricketChirps at waypoint 82 (cell 95, 157).
8. Play sound _Amb_CricketBed at waypoint 90 (cell 42, 87).
9. Play sound _Amb_CricketChirps at waypoint 91 (cell 43, 49).
10. Play sound _Amb_CricketChirps at waypoint 92 (cell 29, 69).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4851, Events line 4929, Actions line 5007.

<a id="trigger-0a25455c"></a>

### 70. Ambient Birds - 0A25455C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A25447C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_BirdsBeach at waypoint 65 (cell 77, 68).
2. Play sound _Amb_BirdsJungle1 at waypoint 66 (cell 81, 66).
3. Play sound _Amb_BirdsBeach at waypoint 67 (cell 96, 90).
4. Play sound _Amb_BirdsJungle2 at waypoint 68 (cell 80, 101).
5. Play sound _Amb_BirdsTemperate1 at waypoint 69 (cell 120, 116).
6. Play sound _Amb_BirdsTemperate2 at waypoint 70 (cell 77, 42).
7. Play sound _Amb_BirdsJungle1 at waypoint 71 (cell 61, 59).
8. Play sound _Amb_BirdsBeach at waypoint 72 (cell 61, 89).
9. Play sound _Amb_BirdsJungle1 at waypoint 73 (cell 55, 89).
10. Play sound _Amb_BirdsHarbor at waypoint 6 (cell 99, 117).
11. Play sound _Amb_BirdsHarbor at waypoint 12 (cell 97, 122).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4852, Events line 4930, Actions line 5008.

<a id="trigger-0a2542ac"></a>

### 71. Ambient Ocean - 0A2542AC

Owner reference: Americans. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 0A2541CC (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_OceanHeavy at waypoint 97 (cell 88, 37).
2. Play sound _Amb_OceanHeavy at waypoint 43 (cell 82, 49).
3. Play sound _Amb_OceanHeavy at waypoint 42 (cell 80, 58).
4. Play sound _Amb_OceanHeavy at waypoint 23 (cell 81, 60).
5. Play sound _Amb_OceanHeavy at waypoint 83 (cell 98, 70).
6. Play sound _Amb_OceanHeavy at waypoint 84 (cell 101, 79).
7. Play sound _Amb_OceanHeavy at waypoint 38 (cell 102, 89).
8. Play sound _Amb_OceanHeavy at waypoint 11 (cell 109, 102).
9. Play sound _Amb_OceanLight at waypoint 85 (cell 99, 105).
10. Play sound _Amb_OceanLight at waypoint 86 (cell 88, 112).
11. Play sound _Amb_OceanLight at waypoint 13 (cell 94, 126).
12. Play sound _Amb_OceanLight at waypoint 14 (cell 100, 127).
13. Play sound _Amb_OceanLight at waypoint 87 (cell 109, 118).
14. Play sound _Amb_OceanHeavy at waypoint 88 (cell 124, 107).
15. Play sound _Amb_OceanHeavy at waypoint 89 (cell 131, 119).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4853, Events line 4931, Actions line 5009.

<a id="trigger-08c1524c"></a>

### 72. Ambient Urban - 08C1524C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: tag definitions 08C15D3C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. The unconditional/any-event condition is satisfied.

**Then perform these actions in order:**

1. Play sound _Amb_UrbanMurmur1 at waypoint 74 (cell 73, 96).
2. Play sound _Amb_UrbanMurmur2 at waypoint 75 (cell 65, 32).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4854, Events line 4932, Actions line 5010.

<a id="trigger-088fbacc"></a>

### 73. Fleet Destroyed - 088FBACC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Destroyer (DEST), owner Americans, cell (117, 90), tag 088FB1DC, persistence mode 0; Destroyer (DEST), owner Americans, cell (121, 96), tag 088FB1DC, persistence mode 0; Destroyer (DEST), owner Americans, cell (120, 93), tag 088FB1DC, persistence mode 0.

**Wait for the recorded events:**

1. Destroyed by anything. See attached-object/cell scope below.

**Then perform these actions in order:**

1. Destroy current instances of [Fleet Detected (03E2BB40)](#trigger-03e2bb40).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4855, Events line 4933, Actions line 5011.

<a id="trigger-086f1b2c"></a>

### 74. Secret Crate CV - 086F1B2C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Ore Refinery (GAREFN), owner Germans, cell (63, 62), tag 086F138C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 99 (cell 66, 61).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4856, Events line 4934, Actions line 5012.

<a id="trigger-086f129c"></a>

### 75. Secret Crate CR - 086F129C

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: none.

Attached scope: Allied Ore Refinery (GAREFN), owner Germans, cell (61, 55), tag 086F109C, persistence mode 0.

**Wait for the recorded events:**

1. Entered by: owner selector 7 (country/type CONFEDERATION; placed owner Confederation).

**Then perform these actions in order:**

1. Create crate type 0 at waypoint 95 (cell 65, 58).

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4857, Events line 4935, Actions line 5013.

<a id="trigger-085f72cc"></a>

### 76. Build a Fleet - Catch All - 085F72CC

Owner reference: Confederation. Initially enabled. Difficulty eligibility: Easy 1, Normal 1, Hard 1 (1 means included). Linked trigger: [Play Fleet if A Refine (0871968C)](#trigger-0871968c).

Attached scope: tag definitions 09B9004C (persistence 0); no placed object/cell attachment found by this extraction.

**Wait for the recorded events:**

1. 300 configured time units have elapsed since scenario start.

**Then perform these actions in order:**

1. Play in-game movie 76.

Source locator: MAPS02.MIX/sov02t.map; Triggers line 4858, Events line 4936, Actions line 5014.

[All team rosters and ordered plans](sov02t-teams.md) | [All mission overrides](sov02t-overrides.md)
