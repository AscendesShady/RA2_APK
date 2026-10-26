# Operation: Weathered Alliance - team rosters and plans

[Trigger ledger](sov10t.md) | [Mission overrides](sov10t-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov10t.map; each team/script ID identifies its section.

<a id="team-0af67a4c"></a>

### West Trans - 0AF67A4C

Owner: Player. Roster: 1 × Amphibious Transport (SAPC); 1 × Soviet Construction Vehicle (SMCV); 4 × Conscript (E2); 1 × Engineer (SENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 7; Veteran Level: 1; Technology level: 0; Waypoint: G.

Ordered plan: West Trans Lands (0C1CAA1C).

1. Move to waypoint: waypoint 1 (cell 163, 181).
2. Move to waypoint: waypoint 24 (cell 158, 178).
3. Move to waypoint: waypoint 25 (cell 154, 177).
4. Move to waypoint: waypoint 26 (cell 149, 179).
5. Move to waypoint: waypoint 5 (cell 145, 176).
6. Unload with continuation mode: passengers continue; transport leaves team.

<a id="team-09ed3a4c"></a>

### East Trans - 09ED3A4C

Owner: Player. Roster: 1 × Amphibious Transport (SAPC); 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: H.

Ordered plan: East Trans Lands (09ED37DC).

1. Move to waypoint: waypoint 23 (cell 175, 180).
2. Move to waypoint: waypoint 27 (cell 173, 180).
3. Move to waypoint: waypoint 28 (cell 171, 180).
4. Move to waypoint: waypoint 29 (cell 165, 180).
5. Move to waypoint: waypoint 8 (cell 147, 174).
6. Unload with continuation mode: passengers continue; transport leaves team.

<a id="team-08e2a39c"></a>

### Team Ivan - 08E2A39C

Owner: Player. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: Ivan Moves (08E2A12C).

1. Move to waypoint: waypoint 4 (cell 148, 176).

<a id="team-08e2924c"></a>

### One Intruder - 08E2924C

Owner: BadGuy2. Roster: 1 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: BG2 Intruder Attack (099096CC).

1. Seek/attack target category; configured argument 2.
2. Report team success.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-093881cc"></a>

### Base Team - 093881CC

Owner: BadGuy1. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Base Defense (08E28C9C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0938d1cc"></a>

### Beach Team - 0938D1CC

Owner: BadGuy1. Roster: 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Beach Defense (07A6B7FC).

1. Attack-move toward waypoint: waypoint 32 (cell 148, 117).
2. Report team success.

<a id="team-07a6b5cc"></a>

### Seal Team - 07A6B5CC

Owner: BadGuy1. Roster: 2 × SEAL (GHOST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0.

Ordered plan: Seal Attack (092A549C).

1. Seek/attack target category; configured argument 9.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-07a6b12c"></a>

### Rocket Team - 07A6B12C

Owner: BadGuy1. Roster: 4 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Vehicle and Building Attack (09E8445C).

1. Move to waypoint: waypoint 39 (cell 110, 168).
2. Seek/attack target category; configured argument 2.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-07f9d710"></a>

### Timer Team - 07F9D710

Owner: <none>. Roster: 1 × Chrono Legionnaire (CLEG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: no script reference.

No local script steps recovered for this reference; it may be supplied by another loaded source.

<a id="team-08e3782c"></a>

### Grizzly Tank Team - 08E3782C

Owner: BadGuy2. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 20; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: Base Defense (08E28C9C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-08e375fc"></a>

### Mirage Tank Team - 08E375FC

Owner: BadGuy2. Roster: 1 × Mirage Tank (MGTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 15; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Base Defense (08E28C9C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-08e373cc"></a>

### Base Defense BG2 - 08E373CC

Owner: BadGuy2. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: Base Defense (08E28C9C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-07a6ef0c"></a>

### Grizzly 4 Tank Defense - 07A6EF0C

Owner: BadGuy1. Roster: 4 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Beach Tank Defense (09BE6CF0).

1. Attack-move toward waypoint: waypoint 33 (cell 148, 120).
2. Seek/attack target category; configured argument 1.

<a id="team-07a6ea6c"></a>

### BG 1 Naval Team - 07A6EA6C

Owner: BadGuy1. Roster: 1 × Dolphin (DLPH); 1 × Aegis Cruiser (AEGIS); 2 × Destroyer (DEST); 1 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: BG1 Naval Attack (07A757FC).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-08e367fc"></a>

### BG3 Grizzly Tank Def - 08E367FC

Owner: BadGuy3. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: BG3 Base Defense (07C3E95C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-08e366dc"></a>

### BG3 GI Defense - 08E366DC

Owner: BadGuy3. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: BG3 Base Defense (07C3E95C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a93f57c"></a>

### BG3 Intruder Defense - 0A93F57C

Owner: BadGuy3. Roster: 1 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: BG2 Intruder Attack (099096CC).

1. Seek/attack target category; configured argument 2.
2. Report team success.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-07055d80"></a>

### Yuri - 07055D80

Owner: Player. Roster: 1 × Yuri (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Do Nothing (07055B40).

1. Play idle behavior.

<a id="team-07a7503c"></a>

### BG1 Carrier Team - 07A7503C

Owner: BadGuy1. Roster: 1 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: BG1 Naval Attack (07A757FC).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-09e83dec"></a>

### BG1 Destroyer Team - 09E83DEC

Owner: BadGuy1. Roster: 2 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: BG3 Naval Attack (0AF0EDBC).

1. Move to waypoint: waypoint 39 (cell 110, 168).
2. Seek/attack target category; configured argument 1.
3. Report team success.

<a id="team-07a7195c"></a>

### BG1 Aegis Team - 07A7195C

Owner: BadGuy1. Roster: 1 × Aegis Cruiser (AEGIS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Aegis Script (09E836CC).

1. Move to waypoint: waypoint 39 (cell 110, 168).
2. Follow friendly objects.
3. Report team success.

<a id="team-07a6d28c"></a>

### BG1 Dolphin Team - 07A6D28C

Owner: BadGuy1. Roster: 1 × Dolphin (DLPH)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: BG1 Naval Attack (07A757FC).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-09914efc"></a>

### BG3 Destroyer Attack Team - 09914EFC

Owner: BadGuy3. Roster: 2 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: BG3 Naval Attack (0AF0EDBC).

1. Move to waypoint: waypoint 39 (cell 110, 168).
2. Seek/attack target category; configured argument 1.
3. Report team success.

<a id="team-09e80b5c"></a>

### BG3 Carrier Attack Team - 09E80B5C

Owner: BadGuy3. Roster: 1 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 10; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Vehicle and Building Attack (09E8445C).

1. Move to waypoint: waypoint 39 (cell 110, 168).
2. Seek/attack target category; configured argument 2.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0af0dc8c"></a>

### BG3 Dolphin Attack Team - 0AF0DC8C

Owner: BadGuy3. Roster: 1 × Dolphin (DLPH)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 10; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: BG3 Naval Attack (0AF0EDBC).

1. Move to waypoint: waypoint 39 (cell 110, 168).
2. Seek/attack target category; configured argument 1.
3. Report team success.

<a id="team-09e8068c"></a>

### BG3 Aegis Attack Team - 09E8068C

Owner: BadGuy3. Roster: 1 × Aegis Cruiser (AEGIS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 10; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Aegis Script (09E836CC).

1. Move to waypoint: waypoint 39 (cell 110, 168).
2. Follow friendly objects.
3. Report team success.

<a id="team-0aa33a3c"></a>

### Harassment Team - 0AA33A3C

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: Harass Player (0AA337CC).

1. Move to waypoint: waypoint 35 (cell 136, 159).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Seek/attack target category; configured argument 9.
4. Seek/attack target category; configured argument 1.

<a id="team-0b5e773c"></a>

### BG3 Rocketeer Attack - 0B5E773C

Owner: BadGuy3. Roster: 4 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 10; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: BG2 Intruder Attack (099096CC).

1. Seek/attack target category; configured argument 2.
2. Report team success.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-0dcff25c"></a>

### Harassment Team_2 - 0DCFF25C

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: Back-of-Base Attack (084A651C).

1. Move to waypoint: waypoint 90 (cell 170, 175).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0ceec74c"></a>

### Harassment Team_3 - 0CEEC74C

Owner: BadGuy1. Roster: 1 × Grizzly Battle Tank (MTNK); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: CN Attack (0A7944CC).

1. Move to waypoint: waypoint 91 (cell 145, 174).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Seek/attack target category; configured argument 1.

<a id="team-0ceec29c"></a>

### Harassment Team_3a - 0CEEC29C

Owner: BadGuy1. Roster: 1 × Grizzly Battle Tank (MTNK); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: CN Attack (0A7944CC).

1. Move to waypoint: waypoint 91 (cell 145, 174).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Seek/attack target category; configured argument 1.

<a id="team-0863d33c"></a>

### Harassment Team_4 - 0863D33C

Owner: BadGuy1. Roster: 4 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: CQ.

Ordered plan: Any Attack (0A7901DC).

1. Seek/attack target category; configured argument 1.

<a id="team-0a796e3c"></a>

### Harassment Team_5 - 0A796E3C

Owner: BadGuy2. Roster: 4 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: BG2 Intruder Attack (099096CC).

1. Seek/attack target category; configured argument 2.
2. Report team success.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-0b7ca57c"></a>

### Beach Panic People - 0B7CA57C

Owner: Civilian1. Roster: 2 × Civilian (CIVBFM); 2 × Civilian (CIVBF); 1 × Civilian (CIVBTM); 1 × Civilian (CIV3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: L.

Ordered plan: Beach Panic (0B7CA30C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-08cc8b0c"></a>

### Nuke Buster Team - 08CC8B0C

Owner: BadGuy3. Roster: 4 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 40; Max: 4; Veteran Level: 2; Technology level: 0.

Ordered plan: Kill Nuke (0AF1F63C).

1. Attack selected enemy-building category; configured argument 65590.
2. Report team success.
3. Attack selected enemy-building category; configured argument 65601.
4. Seek/attack target category; configured argument 2.
