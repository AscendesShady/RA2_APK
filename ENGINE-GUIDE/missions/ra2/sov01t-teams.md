# Operation: Red Dawn - team rosters and plans

[Trigger ledger](sov01t.md) | [Mission overrides](sov01t-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov01t.map; each team/script ID identifies its section.

<a id="team-09ccdc8c"></a>

### Paratroopers 1 - 09CCDC8C

Owner: Player. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: Paratroopers 1 (03D7B0A0).

1. Scatter.

<a id="team-08608f00"></a>

### Defense 1 - 08608F00

Owner: BadGuy1. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: 0AC98490-G (0AC98490-G).

No local script steps recovered for this reference; it may be supplied by another loaded source.

<a id="team-08c774e0"></a>

### Bridge Rush 1 - 08C774E0

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Player Base 1 (08C77280).

1. Seek/attack target category; configured argument 4.
2. Seek/attack target category; configured argument 2.

<a id="team-0a0a0b40"></a>

### Harvester - 0A0A0B40

Owner: Player. Roster: 1 × War Miner (HARV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0; Waypoint: CV.

Ordered plan: Harvester 1 (0A0A8630).

1. Move to waypoint: waypoint 5 (cell 101, 52).
2. Adopt object mission: harvest.

<a id="team-07abe1c0"></a>

### Initial Attack Team - 07ABE1C0

Owner: BadGuy1. Roster: 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Con Yard (08BD9DC0).

1. Unload with continuation mode: transport and passengers continue.
2. Attack selected enemy-building category; configured argument 131097.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-08bd9ca0"></a>

### Flak Trak (3) - 08BD9CA0

Owner: Civilian1. Roster: 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: Flak Trak (08BD9A40).

1. Change country ownership; configured argument 13.

<a id="team-09c1defc"></a>

### Civilian 1 (3) - 09C1DEFC

Owner: Civilian1. Roster: 1 × Civilian (CIVSFM); 1 × Civilian (CIVSF); 1 × Civilian (CIVSTM)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0.

Ordered plan: Civilian 1 (09C0467C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-086d6e10"></a>

### Civilian 1 (1) - 086D6E10

Owner: Civilian1. Roster: 1 × Civilian (CIV1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0.

Ordered plan: Civilian 1 (09C0467C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-085e9d10"></a>

### Base Rush 1 - 085E9D10

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Con Yard (085E9AB0).

1. Seek/attack target category; configured argument 6.

<a id="team-09cf00ec"></a>

### Flak Trak (3) 2 - 09CF00EC

Owner: Player. Roster: 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: Flak Trak 2 (09CFFDBC).

1. Move to waypoint: waypoint 6 (cell 35, 70).
2. Guard for interval; configured argument 60.

<a id="team-0bdae1fc"></a>

### Initial Paratroopers - 0BDAE1FC

Owner: Player. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: V; Transport Waypoint: AN.

Ordered plan: Initial Paratroopers (093DADBC).

1. Guard for interval; configured argument 34.
2. Move to waypoint: waypoint 31 (cell 105, 131).

<a id="team-08e14f00"></a>

### Initial Paratroopers 2 - 08E14F00

Owner: Player. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: T; Transport Waypoint: AO.

Ordered plan: Initial Paratroopers (093DADBC).

1. Guard for interval; configured argument 34.
2. Move to waypoint: waypoint 31 (cell 105, 131).

<a id="team-08e14d10"></a>

### Initial Paratroopers 3 - 08E14D10

Owner: Player. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: U; Transport Waypoint: AP.

Ordered plan: Initial Paratroopers (093DADBC).

1. Guard for interval; configured argument 34.
2. Move to waypoint: waypoint 31 (cell 105, 131).

<a id="team-09c0e2ec"></a>

### Baseball Players1 - 09C0E2EC

Owner: Civilian1. Roster: 4 × Civilian (CIVBBP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Civilian 1 (09C0467C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-079b6624"></a>

### Baseball Players2 - 079B6624

Owner: Other3. Roster: 4 × Civilian (CIV3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Civilian 1 (09C0467C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-07adc0ac"></a>

### Starting Civilians - 07ADC0AC

Owner: Other3. Roster: 1 × Civilian (CIV1); 1 × Civilian (CIV2); 1 × Civilian (CIV3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Civilian 1 (09C0467C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-093da36c"></a>

### IFVs (2) - 093DA36C

Owner: BadGuy1. Roster: 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: IFVs (2) (093CEA4C).

1. Attack selected enemy-building category; configured argument 131081.

<a id="team-08e7da4c"></a>

### IFVs (2)b - 08E7DA4C

Owner: BadGuy1. Roster: 3 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: IFVs (2) (093CEA4C).

1. Attack selected enemy-building category; configured argument 131081.

<a id="team-09bdd6fc"></a>

### Angry GI's - 09BDD6FC

Owner: BadGuy1. Roster: 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Area (07A9FA4C).

1. Scatter.
2. Guard for interval; configured argument 0.

<a id="team-0a7a16fc"></a>

### GI's Flash - 0A7A16FC

Owner: BadGuy2. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: GI's Flash (09CC8C8C).

1. Flash team; configured argument 90.

<a id="team-0815eb2c"></a>

### Soviet MCV - 0815EB2C

Owner: Player. Roster: 1 × Soviet Construction Vehicle (SMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Soviet MCV (0815B04C).

1. Move to waypoint: waypoint 33 (cell 108, 134).
2. Deploy.

<a id="team-0a0e182c"></a>

### BG1 - GI - 0A0E182C

Owner: BadGuy1. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: BG1 - GI (0A0E15BC).

1. Seek/attack target category; configured argument 1.
2. Report team success.
3. Jump to script line; configured argument 1.

<a id="team-0a0e112c"></a>

### BG1 - GI d - 0A0E112C

Owner: BadGuy1. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: BG1 - GI d (0A0E2BEC).

1. Guard for interval; configured argument 0.

<a id="team-0807bc2c"></a>

### BG1 - GI 2 - 0807BC2C

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: BG1 - GI (0A0E15BC).

1. Seek/attack target category; configured argument 1.
2. Report team success.
3. Jump to script line; configured argument 1.

<a id="team-0a0fd23c"></a>

### Engineer 1 - 0A0FD23C

Owner: Player. Roster: 1 × Engineer (SENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GI's Flash (09CC8C8C).

1. Flash team; configured argument 90.

<a id="team-080bb0bc"></a>

### Patrol 1 - 080BB0BC

Owner: BadGuy1. Roster: 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CT.

Ordered plan: Patrol 1 (080C20CC).

1. Move to waypoint: waypoint 100 (cell 50, 30).
2. Move to waypoint: waypoint 30 (cell 70, 30).
3. Move to waypoint: waypoint 29 (cell 70, 49).
4. Move to waypoint: waypoint 97 (cell 50, 49).
5. Jump to script line; configured argument 1.

<a id="team-080c747c"></a>

### Patrol 2 - 080C747C

Owner: BadGuy1. Roster: 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AE.

Ordered plan: Patrol 2 (080C40DC).

1. Move to waypoint: waypoint 29 (cell 70, 49).
2. Move to waypoint: waypoint 97 (cell 50, 49).
3. Move to waypoint: waypoint 100 (cell 50, 30).
4. Move to waypoint: waypoint 30 (cell 70, 30).
5. Jump to script line; configured argument 1.

<a id="team-079df5fc"></a>

### Initial GI Attack - 079DF5FC

Owner: BadGuy1. Roster: 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Attack Player Base 1 (08C77280).

1. Seek/attack target category; configured argument 4.
2. Seek/attack target category; configured argument 2.

<a id="team-0a0c1a7c"></a>

### Occupy Memorial - 0A0C1A7C

Owner: Other3. Roster: 1 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: T; Transport Waypoint: AO.

Ordered plan: Occupy Memorial (0A0C6DBC).

1. Move to waypoint: waypoint 46 (cell 94, 120).
2. Attack selected enemy-building category; configured argument 131281.

<a id="team-09d3357c"></a>

### Flak 1 - 09D3357C

Owner: Other2. Roster: 1 × Flak Track (HTK); 4 × Engineer (SENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AA.

Ordered plan: Flak 1 (07902DBC).

1. Change country ownership; configured argument 13.
2. Move to waypoint: waypoint 6 (cell 35, 70).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Seek/attack target category; configured argument 1.

<a id="team-09d32efc"></a>

### Flak 2 - 09D32EFC

Owner: Other2. Roster: 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BZ.

Ordered plan: Flak 2 (0790439C).

1. Change country ownership; configured argument 13.
2. Move to waypoint: waypoint 23 (cell 64, 108).
3. Seek/attack target category; configured argument 1.

<a id="team-09d32a4c"></a>

### Flak 3 - 09D32A4C

Owner: Other2. Roster: 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: Flak 3 (07900C3C).

1. Change country ownership; configured argument 13.
2. Move to waypoint: waypoint 25 (cell 137, 101).
3. Seek/attack target category; configured argument 1.

<a id="team-09d326ac"></a>

### Flak 4 - 09D326AC

Owner: Other2. Roster: 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: Flak 4 (079063AC).

1. Change country ownership; configured argument 13.
2. Move to waypoint: waypoint 22 (cell 139, 90).
3. Seek/attack target category; configured argument 1.

<a id="team-09d3230c"></a>

### Flak 5 - 09D3230C

Owner: Other2. Roster: 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AC.

Ordered plan: Flak 5 (07903DBC).

1. Change country ownership; configured argument 13.
2. Move to waypoint: waypoint 5 (cell 101, 52).
3. Seek/attack target category; configured argument 1.

<a id="team-08aad22c"></a>

### Panic Female - 08AAD22C

Owner: Civilian1. Roster: 1 × Civilian (CIV2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 30; Veteran Level: 1; Technology level: 0.

Ordered plan: Panic (08AB50FC).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-08ab5e3c"></a>

### Panic Thin - 08AB5E3C

Owner: Civilian1. Roster: 1 × Civilian (CIV3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 30; Veteran Level: 1; Technology level: 0.

Ordered plan: Panic (08AB50FC).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-08ab2bfc"></a>

### Panic Fat - 08AB2BFC

Owner: Civilian1. Roster: 1 × Civilian (CIV1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 30; Veteran Level: 1; Technology level: 0.

Ordered plan: Panic (08AB50FC).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-0aa795cc"></a>

### Secret Transport - 0AA795CC

Owner: Other3. Roster: 1 × Amphibious Transport (SAPC); 4 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CA.

Ordered plan: Secret Transport (08545DBC).

1. Move to waypoint: waypoint 79 (cell 25, 69).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Change country ownership; configured argument 13.
4. Flash team; configured argument 90.

<a id="team-08263efc"></a>

### Paratroopers 1b - 08263EFC

Owner: Player. Roster: 6 × Conscript (E2); 3 × Engineer (SENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: Guard Area (07A9FA4C).

1. Scatter.
2. Guard for interval; configured argument 0.

<a id="team-0836f59c"></a>

### Secret Tanks - 0836F59C

Owner: Player. Roster: 4 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: Secret Tanks 1 (07A47C5C).

1. Move to waypoint: waypoint 95 (cell 50, 40).
2. Seek/attack target category; configured argument 1.

<a id="team-0826d22c"></a>

### Secret Tanks 2 - 0826D22C

Owner: Player. Roster: 4 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: K.

Ordered plan: Secret Tanks 2 (08208DBC).

1. Move to waypoint: waypoint 90 (cell 70, 40).
2. Seek/attack target category; configured argument 1.

<a id="team-084311cc"></a>

### ByeByeTransport - 084311CC

Owner: Other3. Roster: 1 × Amphibious Transport (SAPC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: ByeByeTransport (08430B8C).

1. Move to waypoint: waypoint 78 (cell 15, 69).
2. Delete team objects.

<a id="team-0aee832c"></a>

### Initial Guys - 0AEE832C

Owner: Player. Roster: 18 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0; Waypoint: AG.

Ordered plan: DO NOTHING (0831E90C).

1. Adopt object mission: stop.
2. Adopt object mission: sleep.

<a id="team-0a94465c"></a>

### Emergency Reinforcements - 0A94465C

Owner: Player. Roster: 3 × Engineer (SENGINEER); 3 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AH.

Ordered plan: Guard Area (07A9FA4C).

1. Scatter.
2. Guard for interval; configured argument 0.
