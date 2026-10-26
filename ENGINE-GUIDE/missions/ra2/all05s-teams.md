# Operation: Dark Night - team rosters and plans

[Trigger ledger](all05s.md) | [Mission overrides](all05s-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS01.MIX/all05s.map; each team/script ID identifies its section.

<a id="team-082aba4c"></a>

### Red Patrol 1 - 082ABA4C

Owner: RedTeam. Roster: 1 × Conscript (E2); 2 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Patrol B to I Script (0A92CB7C).

1. Attack-move toward waypoint: waypoint 2 (cell 127, 141).
2. Attack-move toward waypoint: waypoint 3 (cell 124, 139).
3. Attack-move toward waypoint: waypoint 4 (cell 120, 133).
4. Attack-move toward waypoint: waypoint 5 (cell 120, 129).
5. Attack-move toward waypoint: waypoint 6 (cell 109, 128).
6. Attack-move toward waypoint: waypoint 8 (cell 103, 114).
7. Guard for interval; configured argument 15.
8. Attack-move toward waypoint: waypoint 6 (cell 109, 128).
9. Attack-move toward waypoint: waypoint 5 (cell 120, 129).
10. Attack-move toward waypoint: waypoint 4 (cell 120, 133).
11. Attack-move toward waypoint: waypoint 3 (cell 124, 139).
12. Attack-move toward waypoint: waypoint 2 (cell 127, 141).
13. Attack-move toward waypoint: waypoint 1 (cell 123, 147).
14. Guard for interval; configured argument 15.
15. Jump to script line; configured argument 4.

<a id="team-0a55348c"></a>

### Red Patrol 2 - 0A55348C

Owner: RedTeam. Roster: 1 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Patrol Border (07E3CDE0).

1. Guard for interval; configured argument 30.
2. Attack-move toward waypoint: waypoint 15 (cell 95, 83).
3. Attack-move toward waypoint: waypoint 14 (cell 106, 83).
4. Jump to script line; configured argument 2.

<a id="team-0a15e69c"></a>

### Reinforcement Spies 1 - 0A15E69C

Owner: Reinforcements. Roster: 3 × Spy (SPY); 1 × NightHawk Transport (SHAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: Spy Reinforcement Script (0A15ADBC).

1. Attack-move toward waypoint: waypoint 0 (cell 112, 141).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Attack-move toward waypoint: waypoint 13 (cell 116, 163).
4. Delete team objects.

<a id="team-08533a2c"></a>

### Reinforcements 1 - 08533A2C

Owner: Reinforcements. Roster: 3 × Spy (SPY); 1 × NightHawk Transport (SHAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: N.

Ordered plan: Unload Helicopter (08536DBC).

1. Move to waypoint: waypoint 12 (cell 112, 140).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Move to waypoint: waypoint 13 (cell 116, 163).
4. Delete team objects.

<a id="team-088be7dc"></a>

### Spies - 088BE7DC

Owner: Reinforcements. Roster: 1 × Spy (SPY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Change Spies House (088BE56C).

1. Change country ownership; configured argument 14.
2. Flash team; configured argument 90.

<a id="team-07f21c10"></a>

### Tanya (1) - 07F21C10

Owner: Reinforcements. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Tanya Script (07F21920).

1. Change country ownership; configured argument 13.

<a id="team-08ae2380"></a>

### Helicopter - 08AE2380

Owner: Reinforcements. Roster: 1 × NightHawk Transport (SHAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Delete Helicopter (098CB0A0).

1. Change country ownership; configured argument 13.
2. Attack-move toward waypoint: waypoint 13 (cell 116, 163).
3. Delete team objects.

<a id="team-0a552efc"></a>

### 3 Dogs - 0A552EFC

Owner: RedTeam. Roster: 2 × Attack Dog (DOG)

Explicit team settings: Autocreate: yes; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Patrol for Spies (07D875C0).

1. Attack-move toward waypoint: waypoint 8 (cell 103, 114).
2. Seek/attack target category; configured argument 4.
3. Report team success.

<a id="team-03d48870"></a>

### Red Patrol 3 - 03D48870

Owner: RedTeam. Roster: 2 × Attack Dog (DOG); 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 40; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Red Patrol 3 (0A92E21C).

1. Attack-move toward waypoint: waypoint 31 (cell 87, 77).
2. Attack-move toward waypoint: waypoint 32 (cell 91, 77).
3. Attack-move toward waypoint: waypoint 33 (cell 100, 77).
4. Attack-move toward waypoint: waypoint 34 (cell 102, 75).
5. Attack-move toward waypoint: waypoint 35 (cell 101, 72).
6. Guard for interval; configured argument 8.
7. Attack-move toward waypoint: waypoint 34 (cell 102, 75).
8. Attack-move toward waypoint: waypoint 33 (cell 100, 77).
9. Attack-move toward waypoint: waypoint 32 (cell 91, 77).
10. Attack-move toward waypoint: waypoint 31 (cell 87, 77).
11. Attack-move toward waypoint: waypoint 30 (cell 87, 72).
12. Guard for interval; configured argument 8.
13. Jump to script line; configured argument 1.

<a id="team-03d4b940"></a>

### Red Patrol 4 - 03D4B940

Owner: RedTeam. Roster: 2 × Attack Dog (DOG); 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Red Patrol 4 (0A92FB7C).

1. Attack-move toward waypoint: waypoint 27 (cell 97, 92).
2. Attack-move toward waypoint: waypoint 28 (cell 97, 100).
3. Attack-move toward waypoint: waypoint 29 (cell 105, 100).
4. Attack-move toward waypoint: waypoint 26 (cell 105, 92).
5. Jump to script line; configured argument 1.

<a id="team-0a555efc"></a>

### Red Patrol 6 - 0A555EFC

Owner: RedTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: yes; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Patrol for Spies (07D875C0).

1. Attack-move toward waypoint: waypoint 8 (cell 103, 114).
2. Seek/attack target category; configured argument 4.
3. Report team success.

<a id="team-08af15e0"></a>

### Red Patrol 5 - 08AF15E0

Owner: RedTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Red Patrol 5 (0A92F59C).

1. Attack-move toward waypoint: waypoint 24 (cell 109, 106).
2. Guard for interval; configured argument 4.
3. Attack-move toward waypoint: waypoint 23 (cell 95, 106).
4. Guard for interval; configured argument 4.
5. Jump to script line; configured argument 1.

<a id="team-0a55580c"></a>

### Red Patrol 7 - 0A55580C

Owner: RedTeam. Roster: 2 × Attack Dog (DOG); 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Red Patrol 6 (0A930DBC).

1. Attack-move toward waypoint: waypoint 39 (cell 95, 113).
2. Guard for interval; configured argument 4.
3. Attack-move toward waypoint: waypoint 38 (cell 109, 113).
4. Guard for interval; configured argument 4.
5. Jump to script line; configured argument 1.

<a id="team-08a81c00"></a>

### 3 Rebels - 08A81C00

Owner: Civilians. Roster: 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: AL.

Ordered plan: Change to Rebels House (08A819C0).

1. Change country ownership; configured argument 20.

<a id="team-0b0bc420"></a>

### Border Guard 1 - 0B0BC420

Owner: RedTeam. Roster: 1 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: Border Guard 1 (0B0B9DC0).

1. Guard for interval; configured argument 4.
2. Attack-move toward waypoint: waypoint 42 (cell 66, 98).
3. Guard for interval; configured argument 10.
4. Attack-move toward waypoint: waypoint 36 (cell 76, 114).
5. Guard for interval; configured argument 10.
6. Jump to script line; configured argument 2.

<a id="team-08ab2210"></a>

### Tanya (2) - 08AB2210

Owner: Tanya. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 8; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: Tanya 2 Script (08AB9D20).

1. Play idle behavior.

<a id="team-09b3fa00"></a>

### Rebels 2 - 09B3FA00

Owner: Rebels. Roster: 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: AR.

Ordered plan: Rebels 2 (09B3F7C0).

1. Attack-move toward waypoint: waypoint 44 (cell 126, 117).

<a id="team-070290c0"></a>

### Yellow Patrol 1 - 070290C0

Owner: YellowTeam. Roster: 1 × Conscript (E2); 2 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Yellow Patrol 1 (0A93169C).

1. Attack-move toward waypoint: waypoint 46 (cell 69, 37).
2. Attack-move toward waypoint: waypoint 47 (cell 62, 37).
3. Attack-move toward waypoint: waypoint 48 (cell 62, 44).
4. Attack-move toward waypoint: waypoint 45 (cell 69, 44).
5. Jump to script line; configured argument 1.

<a id="team-07cecf30"></a>

### Yellow Patrol 2 - 07CECF30

Owner: YellowTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Yellow Patrol 2 (0A9312FC).

1. Attack-move toward waypoint: waypoint 55 (cell 67, 36).
2. Guard for interval; configured argument 3.
3. Attack-move toward waypoint: waypoint 56 (cell 62, 36).
4. Guard for interval; configured argument 3.
5. Jump to script line; configured argument 1.

<a id="team-07cefc70"></a>

### Yellow Patrol 3 - 07CEFC70

Owner: YellowTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Yellow Patrol 3 (0A932DBC).

1. Attack-move toward waypoint: waypoint 50 (cell 62, 31).
2. Guard for interval; configured argument 3.
3. Attack-move toward waypoint: waypoint 49 (cell 66, 31).
4. Guard for interval; configured argument 3.
5. Jump to script line; configured argument 1.

<a id="team-07ce9e80"></a>

### Yellow Patrol 4 - 07CE9E80

Owner: YellowTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Yellow Patrol 4 (0A932A1C).

1. Attack-move toward waypoint: waypoint 51 (cell 75, 46).
2. Guard for interval; configured argument 3.
3. Attack-move toward waypoint: waypoint 52 (cell 75, 35).
4. Guard for interval; configured argument 3.
5. Jump to script line; configured argument 1.

<a id="team-07cea3c0"></a>

### Yellow Patrol 5 - 07CEA3C0

Owner: YellowTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Yellow Patrol 5 (0A93267C).

1. Attack-move toward waypoint: waypoint 54 (cell 72, 38).
2. Guard for interval; configured argument 3.
3. Attack-move toward waypoint: waypoint 53 (cell 72, 43).
4. Guard for interval; configured argument 3.
5. Jump to script line; configured argument 1.

<a id="team-06f85f30"></a>

### Yellow Patrol 6 - 06F85F30

Owner: YellowTeam. Roster: 1 × Attack Dog (DOG); 3 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yellow Patrol 6 (0A9322DC).

1. Attack-move toward waypoint: waypoint 57 (cell 79, 59).
2. Attack-move toward waypoint: waypoint 58 (cell 79, 64).
3. Attack-move toward waypoint: waypoint 59 (cell 84, 64).
4. Attack-move toward waypoint: waypoint 60 (cell 84, 59).
5. Jump to script line; configured argument 1.

<a id="team-07cd22e0"></a>

### Yellow Patrol 7 - 07CD22E0

Owner: YellowTeam. Roster: 1 × Attack Dog (DOG); 3 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Yellow Patrol 7 (0A933C8C).

1. Attack-move toward waypoint: waypoint 59 (cell 84, 64).
2. Attack-move toward waypoint: waypoint 60 (cell 84, 59).
3. Attack-move toward waypoint: waypoint 57 (cell 79, 59).
4. Attack-move toward waypoint: waypoint 58 (cell 79, 64).
5. Jump to script line; configured argument 1.

<a id="team-0a2d2700"></a>

### Engineers (3) - 0A2D2700

Owner: Rebels. Roster: 3 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Rebels 2 (09B3F7C0).

1. Attack-move toward waypoint: waypoint 44 (cell 126, 117).

<a id="team-087d8f30"></a>

### Orange Patrol 1 - 087D8F30

Owner: OrangeTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Orange Patrol 1 (0A9336AC).

1. Attack-move toward waypoint: waypoint 74 (cell 59, 66).
2. Attack-move toward waypoint: waypoint 75 (cell 59, 61).
3. Attack-move toward waypoint: waypoint 76 (cell 55, 61).
4. Attack-move toward waypoint: waypoint 73 (cell 55, 66).
5. Jump to script line; configured argument 1.

<a id="team-087dfb40"></a>

### Orange Patrol 2 - 087DFB40

Owner: OrangeTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Orange Patrol 2 (0A93330C).

1. Attack-move toward waypoint: waypoint 76 (cell 55, 61).
2. Attack-move toward waypoint: waypoint 73 (cell 55, 66).
3. Attack-move toward waypoint: waypoint 74 (cell 59, 66).
4. Attack-move toward waypoint: waypoint 75 (cell 59, 61).
5. Jump to script line; configured argument 1.

<a id="team-087dfa50"></a>

### Orange Patrol 3 - 087DFA50

Owner: OrangeTeam. Roster: 1 × Attack Dog (DOG); 3 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Orange Patrol 3 (0A934DBC).

1. Attack-move toward waypoint: waypoint 78 (cell 47, 57).
2. Attack-move toward waypoint: waypoint 77 (cell 47, 69).
3. Jump to script line; configured argument 1.

<a id="team-087df960"></a>

### Orange Patrol 4 - 087DF960

Owner: OrangeTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Orange Patrol 4 (0A934B4C).

1. Attack-move toward waypoint: waypoint 80 (cell 42, 61).
2. Attack-move toward waypoint: waypoint 79 (cell 42, 65).
3. Jump to script line; configured argument 1.

<a id="team-087d9ce0"></a>

### Orange Patrol 5 - 087D9CE0

Owner: OrangeTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Orange Patrol 5 (0A9347AC).

1. Attack-move toward waypoint: waypoint 82 (cell 40, 48).
2. Attack-move toward waypoint: waypoint 81 (cell 29, 48).
3. Jump to script line; configured argument 1.

<a id="team-087d9bf0"></a>

### Orange Patrol 6 - 087D9BF0

Owner: OrangeTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Orange Patrol 6 (0A93440C).

1. Attack-move toward waypoint: waypoint 84 (cell 33, 69).
2. Attack-move toward waypoint: waypoint 83 (cell 36, 69).
3. Jump to script line; configured argument 1.

<a id="team-087d9b00"></a>

### Orange Patrol 7 - 087D9B00

Owner: OrangeTeam. Roster: 1 × Conscript (E2); 2 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Orange Patrol 7 (0A935DBC).

1. Attack-move toward waypoint: waypoint 86 (cell 41, 80).
2. Attack-move toward waypoint: waypoint 87 (cell 41, 86).
3. Attack-move toward waypoint: waypoint 88 (cell 47, 86).
4. Attack-move toward waypoint: waypoint 85 (cell 47, 80).
5. Jump to script line; configured argument 1.

<a id="team-087d9f30"></a>

### Orange Patrol 8 - 087D9F30

Owner: OrangeTeam. Roster: 1 × Attack Dog (DOG); 3 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Orange Patrol 8 (0A935B4C).

1. Attack-move toward waypoint: waypoint 90 (cell 31, 61).
2. Attack-move toward waypoint: waypoint 91 (cell 31, 67).
3. Attack-move toward waypoint: waypoint 92 (cell 38, 67).
4. Attack-move toward waypoint: waypoint 89 (cell 38, 61).
5. Jump to script line; configured argument 1.

<a id="team-087d9e40"></a>

### Orange Patrol 9 - 087D9E40

Owner: OrangeTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Orange Patrol 9 (0A9357AC).

1. Attack-move toward waypoint: waypoint 94 (cell 24, 59).
2. Attack-move toward waypoint: waypoint 95 (cell 44, 59).
3. Attack-move toward waypoint: waypoint 96 (cell 44, 50).
4. Attack-move toward waypoint: waypoint 93 (cell 24, 50).
5. Jump to script line; configured argument 1.

<a id="team-0a55d54c"></a>

### Red Patrol 8 - 0A55D54C

Owner: RedTeam. Roster: 1 × Conscript (E2); 1 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0; Waypoint: X.

Ordered plan: Red Patrol 7 (0A2C1DC0).

1. Attack-move toward waypoint: waypoint 24 (cell 109, 106).
2. Guard for interval; configured argument 4.
3. Attack-move toward waypoint: waypoint 23 (cell 95, 106).
4. Guard for interval; configured argument 4.
5. Jump to script line; configured argument 1.

<a id="team-0907359c"></a>

### Truck - 0907359C

Owner: RedTeam. Roster: 1 × Propaganda Truck (PROPA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AP.

Ordered plan: Truck (0907072C).

1. Attack-move toward waypoint: waypoint 1 (cell 123, 147).
2. Attack-move toward waypoint: waypoint 2 (cell 127, 141).
3. Attack-move toward waypoint: waypoint 3 (cell 124, 139).
4. Attack-move toward waypoint: waypoint 4 (cell 120, 133).
5. Attack-move toward waypoint: waypoint 5 (cell 120, 129).
6. Attack-move toward waypoint: waypoint 6 (cell 109, 128).
7. Attack-move toward waypoint: waypoint 7 (cell 110, 141).
8. Attack-move toward waypoint: waypoint 8 (cell 103, 114).
9. Attack-move toward waypoint: waypoint 17 (cell 102, 106).
10. Attack-move toward waypoint: waypoint 24 (cell 109, 106).
11. Adopt object mission: sleep.

<a id="team-0f1097dc"></a>

### Elite GI's - 0F1097DC

Owner: Player. Roster: 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: H.

Ordered plan: Seals (0CDC493C).

1. Scatter.
2. Set facing; configured argument 4.

<a id="team-0a7cfdbc"></a>

### Hint: Spies - 0A7CFDBC

Owner: Spies. Roster: 1 × Spy (SPY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Hint:Spies (0A71503C).

1. Flash team; configured argument 70.

<a id="team-0becec1c"></a>

### Flash Conscript - 0BECEC1C

Owner: RedTeam. Roster: 1 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 8; Veteran Level: 1; Technology level: 0.

Ordered plan: Hint:Spies (0A71503C).

1. Flash team; configured argument 70.

<a id="team-0a62eefc"></a>

### Shock Trooper 1 - 0A62EEFC

Owner: RedTeam. Roster: 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Shock Trooper 1 (0A62F2EC).

1. Set facing; configured argument 6.
2. Flash team; configured argument 120.
3. Guard for interval; configured argument 120.
4. Set facing; configured argument 4.
5. Guard for interval; configured argument 0.

<a id="team-0a62bbcc"></a>

### Shock Trooper 2 - 0A62BBCC

Owner: RedTeam. Roster: 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Shock Trooper 2 (0A62B95C).

1. Set facing; configured argument 2.
2. Guard for interval; configured argument 120.
3. Flash team; configured argument 120.
4. Set facing; configured argument 4.
5. Guard for interval; configured argument 0.

<a id="team-0e584efc"></a>

### Cows1 - 0E584EFC

Owner: Rebels. Roster: 3 × Cow (COW)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: V.

Ordered plan: Cows (0E584C8C).

1. Flash team; configured argument 90.
