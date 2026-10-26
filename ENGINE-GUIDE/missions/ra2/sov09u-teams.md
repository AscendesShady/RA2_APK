# Operation: The Fox and the Hound - team rosters and plans

[Trigger ledger](sov09u.md) | [Mission overrides](sov09u-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov09u.map; each team/script ID identifies its section.

<a id="team-07a58aac"></a>

### Northern Car - 07A58AAC

Owner: Neutral. Roster: 1 × Automobile (CAR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Car Patrol - North (087144BC).

1. Move to waypoint: waypoint 18 (cell 52, 39).
2. Move to waypoint: waypoint 7 (cell 52, 55).
3. Move to waypoint: waypoint 20 (cell 44, 55).
4. Move to waypoint: waypoint 7 (cell 52, 55).
5. Move to waypoint: waypoint 8 (cell 52, 69).
6. Jump to script line; configured argument 1.

<a id="team-08ba5a6c"></a>

### Southern Car - 08BA5A6C

Owner: Neutral. Roster: 1 × Automobile (CAR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Car Patrol - South (07A527BC).

1. Move to waypoint: waypoint 10 (cell 79, 92).
2. Move to waypoint: waypoint 11 (cell 79, 25).
3. Move to waypoint: waypoint 12 (cell 77, 25).
4. Move to waypoint: waypoint 13 (cell 77, 93).
5. Jump to script line; configured argument 1.

<a id="team-0871bc9c"></a>

### Northern Patrol - 0871BC9C

Owner: Americans. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Patrol - North (086EB23C).

1. Attack-move toward waypoint: waypoint 18 (cell 52, 39).
2. Attack-move toward waypoint: waypoint 7 (cell 52, 55).
3. Attack-move toward waypoint: waypoint 8 (cell 52, 69).
4. Attack-move toward waypoint: waypoint 7 (cell 52, 55).
5. Attack-move toward waypoint: waypoint 20 (cell 44, 55).
6. Attack-move toward waypoint: waypoint 7 (cell 52, 55).
7. Jump to script line; configured argument 1.

<a id="team-08ba2ccc"></a>

### Southern Patrol - 08BA2CCC

Owner: Americans. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Patrol - South (08C7646C).

1. Attack-move toward waypoint: waypoint 14 (cell 78, 58).
2. Attack-move toward waypoint: waypoint 15 (cell 78, 52).
3. Attack-move toward waypoint: waypoint 14 (cell 78, 58).
4. Attack-move toward waypoint: waypoint 17 (cell 90, 59).
5. Attack-move toward waypoint: waypoint 14 (cell 78, 58).
6. Attack-move toward waypoint: waypoint 16 (cell 78, 76).
7. Jump to script line; configured argument 1.

<a id="team-0872f6dc"></a>

### Northern Defenders - 0872F6DC

Owner: Americans. Roster: 4 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: W.

Ordered plan: Northern Team moves south (0872F46C).

1. Attack-move toward waypoint: waypoint 14 (cell 78, 58).
2. Adopt object mission: area guard.

<a id="team-090b3a4c"></a>

### ifv patrol - 090B3A4C

Owner: Americans. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Y.

Ordered plan: IFV Patrol (08E0931C).

1. Move to waypoint: waypoint 24 (cell 37, 52).
2. Move to waypoint: waypoint 25 (cell 37, 75).
3. Jump to script line; configured argument 1.

<a id="team-08d9846c"></a>

### upper right patrol - 08D9846C

Owner: Americans. Roster: 2 × Attack Dog (DOG); 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AC.

Ordered plan: upper right perimiter (0932C54C).

1. Attack-move toward waypoint: waypoint 28 (cell 56, 48).
2. Attack-move toward waypoint: waypoint 29 (cell 75, 48).
3. Jump to script line; configured argument 1.

<a id="team-0cbefa4c"></a>

### lower left patrol - 0CBEFA4C

Owner: Americans. Roster: 2 × Attack Dog (DOG); 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AA.

Ordered plan: lower left perimiter (0932C7BC).

1. Attack-move toward waypoint: waypoint 26 (cell 57, 73).
2. Attack-move toward waypoint: waypoint 27 (cell 75, 73).
3. Jump to script line; configured argument 1.

<a id="team-08f03b4c"></a>

### Seal Power Plant - 08F03B4C

Owner: Americans. Roster: 1 × SEAL (GHOST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AE.

Ordered plan: Power Plant Patrol (08CB7DBC).

1. Attack-move toward waypoint: waypoint 30 (cell 62, 50).
2. Attack-move toward waypoint: waypoint 31 (cell 68, 50).
3. Jump to script line; configured argument 1.

<a id="team-08f74c8c"></a>

### Drop Group 1 - 08F74C8C

Owner: Russians. Roster: 15 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AI; Transport Waypoint: AN.

Ordered plan: patrol to A (07BD691C).

1. Attack-move toward waypoint: waypoint 0 (cell 64, 59).
2. Adopt object mission: hunt.

<a id="team-0a41e93c"></a>

### Drop Group 2 - 0A41E93C

Owner: Russians. Roster: 5 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AK; Transport Waypoint: AO.

Ordered plan: patrol to A (07BD691C).

1. Attack-move toward waypoint: waypoint 0 (cell 64, 59).
2. Adopt object mission: hunt.

<a id="team-08f7459c"></a>

### Drop Group 3 - 08F7459C

Owner: Russians. Roster: 15 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AJ; Transport Waypoint: AP.

Ordered plan: patrol to A (07BD691C).

1. Attack-move toward waypoint: waypoint 0 (cell 64, 59).
2. Adopt object mission: hunt.

<a id="team-0ac22efc"></a>

### spy team - 0AC22EFC

Owner: Germans. Roster: 1 × Spy (SPY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AM.

Ordered plan: spy behavior (07B08DBC).

1. Seek/attack target category; configured argument 4.
2. Report team success.

<a id="team-0a4656dc"></a>

### Yuri Drop - 0A4656DC

Owner: Africans. Roster: 2 × Yuri (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AL; Transport Waypoint: AQ.

Ordered plan: vehicle attack (0A76F5EC).

1. Seek/attack target category; configured argument 5.

<a id="team-07f36d6c"></a>

### Spot Radar Team (hack) - 07F36D6C

Owner: Confederation. Roster: 1 × SEAL (GHOST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AR.

Ordered plan: Delete Yourself (07F36AFC).

1. Guard for interval; configured argument 2.
2. Delete team objects.

<a id="team-0ad0f7dc"></a>

### Presidente - 0AD0F7DC

Owner: French. Roster: 1 × President (PRES)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BJ.

Ordered plan: President Script (0AD0F48C).

1. Move to waypoint: waypoint 62 (cell 63, 60).
2. Flash team; configured argument 20.
3. Guard for interval; configured argument 30.
4. Move to waypoint: waypoint 71 (cell 64, 61).
5. Guard for interval; configured argument 30.
6. Move to waypoint: waypoint 62 (cell 63, 60).
7. Guard for interval; configured argument 30.
8. Jump to script line; configured argument 4.

<a id="team-0c0f3a9c"></a>

### IFV Is Un-Mind Controled - 0C0F3A9C

Owner: Americans. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: 2nd Patrol (0C0F382C).

1. Unload with continuation mode: transport continues; passengers leave team.
2. Move to waypoint: waypoint 49 (cell 53, 74).
3. Guard for interval; configured argument 15.
4. Move to waypoint: waypoint 50 (cell 53, 47).
5. Guard for interval; configured argument 15.
6. Move to waypoint: waypoint 51 (cell 78, 48).
7. Guard for interval; configured argument 15.
8. Move to waypoint: waypoint 52 (cell 77, 74).
9. Guard for interval; configured argument 15.
10. Jump to script line; configured argument 1.

<a id="team-0839ca9c"></a>

### 1 Extra Engineer - 0839CA9C

Owner: British. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BB.

Ordered plan: Wait (0839ED4C).

1. Adopt object mission: wait.

<a id="team-0a4751fc"></a>

### Yuri Drop Easy - 0A4751FC

Owner: Africans. Roster: 3 × Yuri (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: AL; Transport Waypoint: AQ.

Ordered plan: vehicle attack (0A76F5EC).

1. Seek/attack target category; configured argument 5.

<a id="team-0a474dec"></a>

### Yuri Drop Hard - 0A474DEC

Owner: Africans. Roster: 1 × Yuri (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AL; Transport Waypoint: AQ.

Ordered plan: vehicle attack (0A76F5EC).

1. Seek/attack target category; configured argument 5.

<a id="team-0abe496c"></a>

### Presidente Guards - 0ABE496C

Owner: GDI. Roster: 2 × Secret Service (SSRV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BJ.

Ordered plan: Secret Service Move (083B4DBC).

1. Move to waypoint: waypoint 62 (cell 63, 60).
2. Adopt object mission: guard.

<a id="team-0abb535c"></a>

### Civilian 1 - 0ABB535C

Owner: Germans. Roster: 1 × Civilian (CIVA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BU.

Ordered plan: Civilian Patrol 1 (0ABBD03C).

1. Move to waypoint: waypoint 74 (cell 49, 39).
2. Guard for interval; configured argument 5.
3. Move to waypoint: waypoint 75 (cell 76, 40).
4. Guard for interval; configured argument 5.
5. Jump to script line; configured argument 1.

<a id="team-0abbfefc"></a>

### Civilian 2 - 0ABBFEFC

Owner: Germans. Roster: 1 × Civilian (CIVB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: BW.

Ordered plan: Civilian 2 (0ABBFA0C).

1. Move to waypoint: waypoint 74 (cell 49, 39).
2. Guard for interval; configured argument 5.
3. Move to waypoint: waypoint 75 (cell 76, 40).
4. Guard for interval; configured argument 5.
5. Jump to script line; configured argument 1.

<a id="team-0af4d6cc"></a>

### Civilian 3 - 0AF4D6CC

Owner: Germans. Roster: 1 × Civilian (CIVC); 1 × Civilian (CIV1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AY.

Ordered plan: Civilian 3 (0ABBF34C).

1. Move to waypoint: waypoint 50 (cell 53, 47).
2. Guard for interval; configured argument 4.
3. Move to waypoint: waypoint 76 (cell 44, 50).
4. Guard for interval; configured argument 6.
5. Move to waypoint: waypoint 77 (cell 44, 67).
6. Guard for interval; configured argument 6.
7. Jump to script line; configured argument 1.

<a id="team-0af51efc"></a>

### Civilian 4 - 0AF51EFC

Owner: Germans. Roster: 1 × Civilian (CIVA); 1 × Civilian (CIV1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CA.

Ordered plan: Civilian 4 (083EF96C).

1. Move to waypoint: waypoint 78 (cell 28, 75).
2. Guard for interval; configured argument 2.
3. Move to waypoint: waypoint 19 (cell 50, 76).
4. Guard for interval; configured argument 2.
5. Jump to script line; configured argument 1.

<a id="team-0d37ad0c"></a>

### 6 SEALs - 0D37AD0C

Owner: Americans. Roster: 6 × SEAL (GHOST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: W.

Ordered plan: Attack Infantry (0D37E98C).

1. Seek/attack target category; configured argument 4.
2. Seek/attack target category; configured argument 1.
