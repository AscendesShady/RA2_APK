# Operation: Eagle Dawn - team rosters and plans

[Trigger ledger](all02s.md) | [Mission overrides](all02s-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS01.MIX/all02s.map; each team/script ID identifies its section.

<a id="team-09d3248c"></a>

### 2 HTank - North - 09D3248C

Owner: Russians. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 15; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: North Attack Anything (092502CC).

1. Attack-move toward waypoint: waypoint 37 (cell 97, 62).
2. Attack-move toward waypoint: waypoint 18 (cell 74, 70).
3. Seek/attack target category; configured argument 1.

<a id="team-09d31dec"></a>

### 2 HTank - South - 09D31DEC

Owner: Russians. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: South Attack (09251DBC).

1. Attack-move toward waypoint: waypoint 1 (cell 91, 107).
2. Attack-move toward waypoint: waypoint 20 (cell 71, 110).
3. Attack-move toward waypoint: waypoint 4 (cell 64, 97).
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-07c9c6bc"></a>

### West Field Guard Team - 07C9C6BC

Owner: Russians. Roster: 2 × Rhino Heavy Tank (HTNK); 2 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Field Guard - West (07C8B66C).

1. Move to waypoint: waypoint 12 (cell 78, 67).
2. Adopt object mission: area guard.

<a id="team-096fbb7c"></a>

### Base Field Guard Team - 096FBB7C

Owner: Russians. Roster: 1 × Rhino Heavy Tank (HTNK); 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Harvester Radiers South (07C8BB4C).

1. Move to waypoint: waypoint 0 (cell 131, 107).
2. Move to waypoint: waypoint 16 (cell 84, 126).
3. Move to waypoint: waypoint 17 (cell 47, 113).
4. Seek/attack target category; configured argument 3.

<a id="team-09e4bb7c"></a>

### Mixed Base Defense - 09E4BB7C

Owner: Russians. Roster: 2 × Rhino Heavy Tank (HTNK); 2 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Outer Base Patrol (0A5D2C0C).

1. Attack-move toward waypoint: waypoint 26 (cell 101, 64).
2. Guard for interval; configured argument 10.
3. Attack-move toward waypoint: waypoint 27 (cell 123, 65).
4. Guard for interval; configured argument 10.
5. Attack-move toward waypoint: waypoint 26 (cell 101, 64).
6. Guard for interval; configured argument 10.
7. Attack-move toward waypoint: waypoint 28 (cell 103, 49).
8. Guard for interval; configured argument 10.
9. Jump to script line; configured argument 1.

<a id="team-0ad26c8c"></a>

### 6 Conscript Defense - 0AD26C8C

Owner: Russians. Roster: 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: general base defense (0AE762AC).

1. Adopt object mission: area guard.

<a id="team-08dc191c"></a>

### 10 Conscrits North - 08DC191C

Owner: Russians. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 15; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: North Attack Anything (092502CC).

1. Attack-move toward waypoint: waypoint 37 (cell 97, 62).
2. Attack-move toward waypoint: waypoint 18 (cell 74, 70).
3. Seek/attack target category; configured argument 1.

<a id="team-08dc16dc"></a>

### 10 Conscripts South - 08DC16DC

Owner: Russians. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: South Attack Buildings (098217DC).

1. Attack-move toward waypoint: waypoint 1 (cell 91, 107).
2. Attack-move toward waypoint: waypoint 20 (cell 71, 110).
3. Attack-move toward waypoint: waypoint 4 (cell 64, 97).
4. Seek/attack target category; configured argument 2.

<a id="team-08dc15ac"></a>

### Harv Hunt North - 08DC15AC

Owner: Russians. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Harvester Raiders North (07C8BDBC).

1. Move to waypoint: waypoint 14 (cell 79, 47).
2. Move to waypoint: waypoint 10 (cell 52, 73).
3. Move to waypoint: waypoint 15 (cell 40, 91).
4. Seek/attack target category; configured argument 3.

<a id="team-08dc10fc"></a>

### Harv Hunt South - 08DC10FC

Owner: Russians. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Harvester Radiers South (07C8BB4C).

1. Move to waypoint: waypoint 0 (cell 131, 107).
2. Move to waypoint: waypoint 16 (cell 84, 126).
3. Move to waypoint: waypoint 17 (cell 47, 113).
4. Seek/attack target category; configured argument 3.

<a id="team-0a9ba6ac"></a>

### 2 Dog Raiders - 0A9BA6AC

Owner: Russians. Roster: 2 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: General Infantry Attack (0AE7655C).

1. Seek/attack target category; configured argument 4.
2. Seek/attack target category; configured argument 1.

<a id="team-0976b78c"></a>

### Mixed North - 0976B78C

Owner: Russians. Roster: 2 × Rhino Heavy Tank (HTNK); 2 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: North Attack Troops (0982425C).

1. Attack-move toward waypoint: waypoint 37 (cell 97, 62).
2. Attack-move toward waypoint: waypoint 18 (cell 74, 70).
3. Seek/attack target category; configured argument 5.

<a id="team-07ca419c"></a>

### Mixed South - 07CA419C

Owner: Russians. Roster: 2 × Rhino Heavy Tank (HTNK); 2 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: South Attack Buildings (098217DC).

1. Attack-move toward waypoint: waypoint 1 (cell 91, 107).
2. Attack-move toward waypoint: waypoint 20 (cell 71, 110).
3. Attack-move toward waypoint: waypoint 4 (cell 64, 97).
4. Seek/attack target category; configured argument 2.

<a id="team-09820a7c"></a>

### North Capture Team - 09820A7C

Owner: Russians. Roster: 1 × Flak Track (HTK); 2 × Engineer (ENGINEER); 3 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 15; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: North Attack - Capture (0982080C).

1. Load transport.
2. Wait for loading completion.
3. Move to waypoint: waypoint 37 (cell 97, 62).
4. Move to waypoint: waypoint 18 (cell 74, 70).
5. Move to waypoint: waypoint 19 (cell 71, 87).
6. Approach selected enemy-building category; configured argument 131074.
7. Unload with continuation mode: transport and passengers continue.
8. Report team success.
9. Attack selected enemy-building category; configured argument 131074.
10. Attack selected enemy-building category; configured argument 186.
11. Attack selected enemy-building category; configured argument 7.
12. Seek/attack target category; configured argument 2.

<a id="team-098205cc"></a>

### South Capture Team - 098205CC

Owner: Russians. Roster: 1 × Flak Track (HTK); 2 × Engineer (ENGINEER); 3 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: South Attack Building Capture (08DC3DBC).

1. Load transport.
2. Wait for loading completion.
3. Move to waypoint: waypoint 1 (cell 91, 107).
4. Move to waypoint: waypoint 20 (cell 71, 110).
5. Move to waypoint: waypoint 4 (cell 64, 97).
6. Approach selected enemy-building category; configured argument 1.
7. Report team success.
8. Unload with continuation mode: transport and passengers continue.
9. Attack selected enemy-building category; configured argument 1.
10. Seek/attack target category; configured argument 2.

<a id="team-0bb0f43c"></a>

### Confed Base Patrol - 0BB0F43C

Owner: Confederation. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: Confed Base Patrol (0985030C).

1. Attack-move toward waypoint: waypoint 3 (cell 67, 96).
2. Attack-move toward waypoint: waypoint 4 (cell 64, 97).
3. Attack-move toward waypoint: waypoint 5 (cell 64, 87).
4. Attack-move toward waypoint: waypoint 19 (cell 71, 87).
5. Attack-move toward waypoint: waypoint 5 (cell 64, 87).
6. Attack-move toward waypoint: waypoint 4 (cell 64, 97).
7. Jump to script line; configured argument 1.

<a id="team-09842efc"></a>

### Confed Road Patrol - 09842EFC

Owner: Confederation. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: Confed Road Patrol (0976FA1C).

1. Attack-move toward waypoint: waypoint 35 (cell 109, 109).
2. Attack-move toward waypoint: waypoint 22 (cell 104, 107).
3. Attack-move toward waypoint: waypoint 34 (cell 98, 107).
4. Attack-move toward waypoint: waypoint 33 (cell 95, 107).
5. Attack-move toward waypoint: waypoint 1 (cell 91, 107).
6. Guard for interval; configured argument 20.
7. Attack-move toward waypoint: waypoint 11 (cell 65, 108).
8. Attack-move toward waypoint: waypoint 9 (cell 53, 108).
9. Guard for interval; configured argument 20.
10. Attack-move toward waypoint: waypoint 11 (cell 65, 108).
11. Attack-move toward waypoint: waypoint 1 (cell 91, 107).
12. Attack-move toward waypoint: waypoint 33 (cell 95, 107).
13. Attack-move toward waypoint: waypoint 34 (cell 98, 107).
14. Attack-move toward waypoint: waypoint 22 (cell 104, 107).
15. Attack-move toward waypoint: waypoint 35 (cell 109, 109).
16. Attack-move toward waypoint: waypoint 0 (cell 131, 107).
17. Guard for interval; configured argument 20.
18. Jump to script line; configured argument 1.

<a id="team-09842a7c"></a>

### Confed Road Team 2 - 09842A7C

Owner: Confederation. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AG.

Ordered plan: Confed Road 2 (0983761C).

1. Attack-move toward waypoint: waypoint 23 (cell 90, 106).
2. Guard for interval; configured argument 20.
3. Attack-move toward waypoint: waypoint 32 (cell 89, 103).
4. Attack-move toward waypoint: waypoint 31 (cell 89, 100).
5. Attack-move toward waypoint: waypoint 24 (cell 89, 95).
6. Attack-move toward waypoint: waypoint 7 (cell 90, 75).
7. Guard for interval; configured argument 20.
8. Attack-move toward waypoint: waypoint 24 (cell 89, 95).
9. Attack-move toward waypoint: waypoint 31 (cell 89, 100).
10. Attack-move toward waypoint: waypoint 32 (cell 89, 103).
11. Jump to script line; configured argument 1.

<a id="team-0c5e612c"></a>

### 6 Engineers - 0C5E612C

Owner: Americans. Roster: 6 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: Guard for 1 (0B62878C).

1. Guard for interval; configured argument 1.

<a id="team-09e58efc"></a>

### Soviet 1st Strike Team - 09E58EFC

Owner: Russians. Roster: 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Z.

Ordered plan: North Attack Troops (0982425C).

1. Attack-move toward waypoint: waypoint 37 (cell 97, 62).
2. Attack-move toward waypoint: waypoint 18 (cell 74, 70).
3. Seek/attack target category; configured argument 5.

<a id="team-08dc4b8c"></a>

### Inner Base Defense - 08DC4B8C

Owner: Russians. Roster: 2 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Confed Base Patrol (0985030C).

1. Attack-move toward waypoint: waypoint 3 (cell 67, 96).
2. Attack-move toward waypoint: waypoint 4 (cell 64, 97).
3. Attack-move toward waypoint: waypoint 5 (cell 64, 87).
4. Attack-move toward waypoint: waypoint 19 (cell 71, 87).
5. Attack-move toward waypoint: waypoint 5 (cell 64, 87).
6. Attack-move toward waypoint: waypoint 4 (cell 64, 97).
7. Jump to script line; configured argument 1.

<a id="team-03e3f6fc"></a>

### 2 H-Tank - 03E3F6FC

Owner: Russians. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: North Attack Troops (0982425C).

1. Attack-move toward waypoint: waypoint 37 (cell 97, 62).
2. Attack-move toward waypoint: waypoint 18 (cell 74, 70).
3. Seek/attack target category; configured argument 5.

<a id="team-03e3669c"></a>

### Hard Patrol Team - 03E3669C

Owner: Confederation. Roster: 5 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 3; Technology level: 0; Waypoint: AT.

Ordered plan: Hard Inside Base Patrol (03E36DBC).

1. Attack-move toward waypoint: waypoint 45 (cell 66, 84).
2. Guard for interval; configured argument 5.
3. Attack-move toward waypoint: waypoint 46 (cell 68, 90).
4. Guard for interval; configured argument 5.
5. Jump to script line; configured argument 1.

<a id="team-08060cbc"></a>

### Barrel Defense Team - 08060CBC

Owner: Russians. Roster: 5 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: Attack Anything (080A2C3C).

1. Seek/attack target category; configured argument 1.

<a id="team-09d4059c"></a>

### 4 Intruders - 09D4059C

Owner: Americans. Roster: 4 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AV.

Ordered plan: air patrol (09E5EDBC).

1. Set local flag: local flag 1 (Intruders Scout Don).
2. Move to waypoint: waypoint 26 (cell 101, 64).
3. Adopt object mission: stop.

<a id="team-0b8ce08c"></a>

### 2 Half Tracks - 0B8CE08C

Owner: Russians. Roster: 2 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Z.

Ordered plan: Attack Anything (080A2C3C).

1. Seek/attack target category; configured argument 1.

<a id="team-0a3473ac"></a>

### Hard 4 Tank North - 0A3473AC

Owner: Russians. Roster: 4 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: North Attack Anything (092502CC).

1. Attack-move toward waypoint: waypoint 37 (cell 97, 62).
2. Attack-move toward waypoint: waypoint 18 (cell 74, 70).
3. Seek/attack target category; configured argument 1.

<a id="team-0a34716c"></a>

### Hard 4 Tank South - 0A34716C

Owner: Russians. Roster: 4 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: South Attack Buildings (098217DC).

1. Attack-move toward waypoint: waypoint 1 (cell 91, 107).
2. Attack-move toward waypoint: waypoint 20 (cell 71, 110).
3. Attack-move toward waypoint: waypoint 4 (cell 64, 97).
4. Seek/attack target category; configured argument 2.

<a id="team-0b6129ec"></a>

### 2 Engineers, 6 Conscripts - 0B6129EC

Owner: Russians. Roster: 2 × Engineer (SENGINEER); 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: North Engineer Rush (0B61490C).

1. Move to waypoint: waypoint 37 (cell 97, 62).
2. Move to waypoint: waypoint 19 (cell 71, 87).
3. Attack selected enemy-building category; configured argument 0.

<a id="team-09baddcc"></a>

### 1 H-Tank - 09BADDCC

Owner: Russians. Roster: 1 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: North Attack Troops (0982425C).

1. Attack-move toward waypoint: waypoint 37 (cell 97, 62).
2. Attack-move toward waypoint: waypoint 18 (cell 74, 70).
3. Seek/attack target category; configured argument 5.

<a id="team-09c6620c"></a>

### Change Engineer to France - 09C6620C

Owner: Americans. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: Change to France (09C67DBC).

1. Change country ownership; configured argument 2.

<a id="team-0a9c5b7c"></a>

### Capture Conyard - 0A9C5B7C

Owner: French. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: Capture Conyard (0924C5FC).

1. Move to waypoint: waypoint 45 (cell 66, 84).
2. Attack selected enemy-building category; configured argument 2.

<a id="team-0a9c57dc"></a>

### Capture Chapel - 0A9C57DC

Owner: French. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: Capture Chapel (0A3B18EC).

1. Move to waypoint: waypoint 53 (cell 62, 83).
2. Attack selected enemy-building category; configured argument 131258.

<a id="team-0d691efc"></a>

### 8 Rocketeers - 0D691EFC

Owner: Neutral. Roster: 8 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AS.

Ordered plan: Rocketeer Behavior (0BD2E59C).

1. Move to waypoint: waypoint 58 (cell 116, 125).

<a id="team-0d691a4c"></a>

### 8 Rocketeers - USA - 0D691A4C

Owner: Neutral. Roster: 8 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BG.

Ordered plan: Change House (0BB35C8C).

1. Change country ownership; configured argument 1.

<a id="team-0b12b7dc"></a>

### 8 Rocketeer Move Team - 0B12B7DC

Owner: Alliance. Roster: 8 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BG.

Ordered plan: Move to BH (09BAE5BC).

1. Move to waypoint: waypoint 59 (cell 114, 109).

<a id="team-09d4317c"></a>

### Hard Confed Road Patrol - 09D4317C

Owner: Confederation. Roster: 1 × Rhino Heavy Tank (HTNK); 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Confed Road Patrol (0976FA1C).

1. Attack-move toward waypoint: waypoint 35 (cell 109, 109).
2. Attack-move toward waypoint: waypoint 22 (cell 104, 107).
3. Attack-move toward waypoint: waypoint 34 (cell 98, 107).
4. Attack-move toward waypoint: waypoint 33 (cell 95, 107).
5. Attack-move toward waypoint: waypoint 1 (cell 91, 107).
6. Guard for interval; configured argument 20.
7. Attack-move toward waypoint: waypoint 11 (cell 65, 108).
8. Attack-move toward waypoint: waypoint 9 (cell 53, 108).
9. Guard for interval; configured argument 20.
10. Attack-move toward waypoint: waypoint 11 (cell 65, 108).
11. Attack-move toward waypoint: waypoint 1 (cell 91, 107).
12. Attack-move toward waypoint: waypoint 33 (cell 95, 107).
13. Attack-move toward waypoint: waypoint 34 (cell 98, 107).
14. Attack-move toward waypoint: waypoint 22 (cell 104, 107).
15. Attack-move toward waypoint: waypoint 35 (cell 109, 109).
16. Attack-move toward waypoint: waypoint 0 (cell 131, 107).
17. Guard for interval; configured argument 20.
18. Jump to script line; configured argument 1.

<a id="team-09d470bc"></a>

### Hard Confed Road Patrol 2 - 09D470BC

Owner: Confederation. Roster: 1 × Rhino Heavy Tank (HTNK); 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Confed Road 2 (0983761C).

1. Attack-move toward waypoint: waypoint 23 (cell 90, 106).
2. Guard for interval; configured argument 20.
3. Attack-move toward waypoint: waypoint 32 (cell 89, 103).
4. Attack-move toward waypoint: waypoint 31 (cell 89, 100).
5. Attack-move toward waypoint: waypoint 24 (cell 89, 95).
6. Attack-move toward waypoint: waypoint 7 (cell 90, 75).
7. Guard for interval; configured argument 20.
8. Attack-move toward waypoint: waypoint 24 (cell 89, 95).
9. Attack-move toward waypoint: waypoint 31 (cell 89, 100).
10. Attack-move toward waypoint: waypoint 32 (cell 89, 103).
11. Jump to script line; configured argument 1.

<a id="team-09ff2a4c"></a>

### 10 Paratroopers BE - 09FF2A4C

Owner: Alliance. Roster: 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: BE.

Ordered plan: attack soviets (0B0AADBC).

1. Seek/attack target category; configured argument 1.

<a id="team-09ff259c"></a>

### 10 Paratroopers BI - 09FF259C

Owner: Alliance. Roster: 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: BI.

Ordered plan: Attack Anything (080A2C3C).

1. Seek/attack target category; configured argument 1.

<a id="team-09ff246c"></a>

### 10 Paratroopers BJ - 09FF246C

Owner: Alliance. Roster: 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: BJ.

Ordered plan: Attack Anything (080A2C3C).

1. Seek/attack target category; configured argument 1.

<a id="team-0840eefc"></a>

### Rocketeers 2nd Wave - 0840EEFC

Owner: Americans. Roster: 8 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BK.

Ordered plan: 2nd Wave Rocketeers (0840EC8C).

1. Move to waypoint: waypoint 98 (cell 119, 112).

<a id="team-0a54e20c"></a>

### 4 Intruders - Start - 0A54E20C

Owner: British. Roster: 4 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: intruder start-up (09CFF30C).

1. Move to waypoint: waypoint 53 (cell 62, 83).

<a id="team-0ad3e68c"></a>

### 1 Harvester - 0AD3E68C

Owner: Russians. Roster: 1 × War Miner (HARV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CC.

Ordered plan: Harvest (0AD3E41C).

1. Move to waypoint: waypoint 81 (cell 113, 56).
