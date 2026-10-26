# Operation: Home Front - team rosters and plans

[Trigger ledger](sov04s.md) | [Mission overrides](sov04s-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov04s.map; each team/script ID identifies its section.

<a id="team-0d9e646c"></a>

### Intruder Harrassment 1 - 0D9E646C

Owner: BadGuy2. Roster: 2 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Intruder Harrassment 1 SCR (0D9E61FC).

1. Attack selected enemy-building category; configured argument 131081.
2. Attack selected enemy-building category; configured argument 11.
3. Attack selected enemy-building category; configured argument 15.
4. Move to waypoint: waypoint 3 (cell 144, 116).
5. Delete team objects.

<a id="team-0d9e5dec"></a>

### Intruder Harrassment 2 - 0D9E5DEC

Owner: BadGuy2. Roster: 2 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: E.

Ordered plan: Intruder Harrassment 2 SCR (0D9E5B7C).

1. Attack selected enemy-building category; configured argument 131087.
2. Attack selected enemy-building category; configured argument 131097.
3. Attack selected enemy-building category; configured argument 131081.
4. Move to waypoint: waypoint 4 (cell 161, 60).
5. Delete team objects.

<a id="team-0befcb5c"></a>

### Allied Assault Fleet a - 0BEFCB5C

Owner: BadGuy1. Roster: 2 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Allied Assault Fleet a SCR (08D35A40).

1. Attack-move toward waypoint: waypoint 5 (cell 99, 116).
2. Attack selected enemy-building category; configured argument 131133.
3. Attack selected enemy-building category; configured argument 131097.
4. Attack selected enemy-building category; configured argument 131139.
5. Seek/attack target category; configured argument 1.
6. Adopt object mission: hunt.

<a id="team-0befc6ac"></a>

### Allied Assault Fleet b - 0BEFC6AC

Owner: BadGuy1. Roster: 2 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: E.

Ordered plan: Allied Assault Fleet b SCR (08D355C0).

1. Attack-move toward waypoint: waypoint 6 (cell 140, 57).
2. Attack-move toward waypoint: waypoint 7 (cell 125, 52).
3. Attack-move toward waypoint: waypoint 8 (cell 129, 40).
4. Attack-move toward waypoint: waypoint 9 (cell 131, 68).
5. Jump to script line; configured argument 1.

<a id="team-0434c1fc"></a>

### Allied Landing Fleet LZ@A a - 0434C1FC

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: Allied Landing Fleet GI@A SCR (08C17820).

1. Move to waypoint: waypoint 6 (cell 140, 57).
2. Set local flag: local flag 6 (Allied Fleet Here).
3. Move to waypoint: waypoint 0 (cell 121, 46).
4. Unload with continuation mode: transport continues; passengers leave team.
5. Set local flag: local flag 1 (GIs ashore).
6. Move to waypoint: waypoint 1 (cell 148, 50).
7. Delete team objects.

<a id="team-0434db7c"></a>

### Allied Landing Fleet LZ@K a - 0434DB7C

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: Allied Landing Fleet Grizz@K SCR (0B3FC7D0).

1. Move to waypoint: waypoint 11 (cell 137, 48).
2. Move to waypoint: waypoint 10 (cell 121, 40).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Set local flag: local flag 2 (Grizzly ashore).
5. Move to waypoint: waypoint 1 (cell 148, 50).
6. Delete team objects.

<a id="team-0434d6cc"></a>

### Allied Landing Fleet LZ@M a - 0434D6CC

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: Allied Landing Fleet Grizz@M SCR (0B3F8890).

1. Move to waypoint: waypoint 6 (cell 140, 57).
2. Move to waypoint: waypoint 12 (cell 123, 56).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Set local flag: local flag 4 (Grizzly2 ashore).
5. Move to waypoint: waypoint 1 (cell 148, 50).
6. Delete team objects.

<a id="team-0434d32c"></a>

### Allied Landing MCV@K - 0434D32C

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 1 × Allied Construction Vehicle (AMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: Allied Landing MCV@A SCR (0B3FBC10).

1. Move to waypoint: waypoint 11 (cell 137, 48).
2. Move to waypoint: waypoint 10 (cell 121, 40).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Set local flag: local flag 3 (MCV ashore).
5. Move to waypoint: waypoint 1 (cell 148, 50).
6. Delete team objects.

<a id="team-0b135360"></a>

### GIs Landed - 0B135360

Owner: BadGuy1. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: GIs Landed SCR (0AC536E0).

1. Attack-move toward waypoint: waypoint 16 (cell 99, 50).
2. Deploy.
3. Adopt object mission: area guard.

<a id="team-09987040"></a>

### Grizz Landed @K - 09987040

Owner: BadGuy1. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: K.

Ordered plan: Grizzly Landed @K SCR (0999FC00).

1. Attack-move toward waypoint: waypoint 15 (cell 98, 47).
2. Adopt object mission: area guard.

<a id="team-099b1610"></a>

### Grizz Landed @M - 099B1610

Owner: BadGuy1. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: M.

Ordered plan: Grizzly Landed @M SCR (099B13B0).

1. Attack-move toward waypoint: waypoint 14 (cell 100, 53).
2. Adopt object mission: area guard.

<a id="team-099b3350"></a>

### MCV Landed - 099B3350

Owner: BadGuy1. Roster: 1 × Allied Construction Vehicle (AMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: K.

Ordered plan: MCV Landed SCR (099D6DC0).

1. Move to waypoint: waypoint 2 (cell 110, 40).
2. Deploy.

<a id="team-0434f90c"></a>

### Allied Landing Fleet LZ@A b - 0434F90C

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: Allied Landing Fleet LZ@A b SCR (08DDAB7C).

1. Move to waypoint: waypoint 6 (cell 140, 57).
2. Move to waypoint: waypoint 0 (cell 121, 46).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Set local flag: local flag 5 (GI2 ashore).
5. Move to waypoint: waypoint 1 (cell 148, 50).
6. Delete team objects.

<a id="team-0a3cb920"></a>

### GI2 Landed - 0A3CB920

Owner: BadGuy1. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: GI2 Landed SCR (0AC52120).

1. Attack-move toward waypoint: waypoint 13 (cell 101, 50).
2. Deploy.
3. Adopt object mission: area guard.

<a id="team-0aa7d920"></a>

### Attk_Grizzly x3 - 0AA7D920

Owner: BadGuy1. Roster: 3 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Grizzly x3 SCR (08DDA43C).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 1.

<a id="team-0a49bf0c"></a>

### Attk_IFV/Rocketeer x4 - 0A49BF0C

Owner: BadGuy1. Roster: 4 × IFV (FV); 4 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_IFV/Rocketeer x4 SCR (08DD9DBC).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 1.

<a id="team-0a713a80"></a>

### Def_Infantry - 0A713A80

Owner: BadGuy1. Roster: 8 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: _Base Defense SCR (08DD990C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a713600"></a>

### Def_V3 - 0A713600

Owner: BadGuy1. Roster: 5 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: _Base Defense SCR (08DD990C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a49b39c"></a>

### Def_Armor - 0A49B39C

Owner: BadGuy1. Roster: 5 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: _Base Defense SCR (08DD990C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a49b16c"></a>

### Def_Terror - 0A49B16C

Owner: BadGuy1. Roster: 4 × IFV (FV); 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 14; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Terror SCR (08DD8DBC).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a49cb8c"></a>

### Def_Combo 1 - 0A49CB8C

Owner: BadGuy1. Roster: 4 × IFV (FV); 4 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 14; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Combo 1 SCR (08DD8A1C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a711820"></a>

### Def_Combo 2 - 0A711820

Owner: BadGuy1. Roster: 2 × IFV (FV); 2 × Grizzly Battle Tank (MTNK); 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: _Base Defense SCR (08DD990C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bfff48c"></a>

### Invasion Para 1 - 0BFFF48C

Owner: BadGuy1. Roster: 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: R.

Ordered plan: Invasion Para 1 SCR (097537DC).

1. Move to waypoint: waypoint 21 (cell 94, 49).
2. Attack selected enemy-building category; configured argument 131087.
3. Seek/attack target category; configured argument 1.

<a id="team-0bffedec"></a>

### Invasion Para 2 - 0BFFEDEC

Owner: BadGuy1. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Invasion Para 2 SCR (0975332C).

1. Move to waypoint: waypoint 21 (cell 94, 49).
2. Attack selected enemy-building category; configured argument 131139.
3. Attack selected enemy-building category; configured argument 131092.
4. Seek/attack target category; configured argument 7.
5. Seek/attack target category; configured argument 1.

<a id="team-09a280b0"></a>

### Stupid Harvester 1 - 09A280B0

Owner: BadGuy1. Roster: 1 × Chrono Miner (CMIN)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: T.

Ordered plan: Stupid Harvester SCR (0ADFB3A0).

1. Move to waypoint: waypoint 23 (cell 102, 20).

<a id="team-0bffe48c"></a>

### Invasion Para 3 - 0BFFE48C

Owner: BadGuy1. Roster: 2 × GI (E1); 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: U.

Ordered plan: Invasion Para 3 SCR (097527DC).

1. Move to waypoint: waypoint 21 (cell 94, 49).
2. Attack selected enemy-building category; configured argument 131139.
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 1.

<a id="team-0aa80720"></a>

### Attk_GI x5 - 0AA80720

Owner: BadGuy1. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_GI x5 SCR (08DE6C8C).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-0c2292e0"></a>

### Attk_Rocketeer x4 - 0C2292E0

Owner: BadGuy1. Roster: 4 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Rocketeer x4 SCR (08DE67DC).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 9.
4. Seek/attack target category; configured argument 1.

<a id="team-0994759c"></a>

### Attk_Intruder x3a - 0994759C

Owner: BadGuy1. Roster: 2 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Intruder x4a SCR (08DE632C).

1. Attack selected enemy-building category; configured argument 131081.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131087.
4. Seek/attack target category; configured argument 1.

<a id="team-09946efc"></a>

### Attk_Intruder x3b - 09946EFC

Owner: BadGuy1. Roster: 2 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Intruder x4a SCR (08DE632C).

1. Attack selected enemy-building category; configured argument 131081.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131087.
4. Seek/attack target category; configured argument 1.

<a id="team-0a6256fc"></a>

### Attk_Combined a - 0A6256FC

Owner: BadGuy1. Roster: 3 × Grizzly Battle Tank (MTNK); 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Combined b SCR (09072A40).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-0a62524c"></a>

### Attk_Combined b - 0A62524C

Owner: BadGuy1. Roster: 8 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Combined b SCR (09072A40).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-08fd87dc"></a>

### Attk_Engineer x2a - 08FD87DC

Owner: BadGuy1. Roster: 2 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Engineer x2a SCR (08DE4C8C).

1. Attack selected enemy-building category; configured argument 131087.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131086.
4. Seek/attack target category; configured argument 2.

<a id="team-08fd832c"></a>

### Attk_Engineer x2b - 08FD832C

Owner: BadGuy1. Roster: 2 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Engineer x2b SCR (08DE47DC).

1. Attack selected enemy-building category; configured argument 196619.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131097.
4. Seek/attack target category; configured argument 2.

<a id="team-0a71d800"></a>

### Def_Engineer x2c - 0A71D800

Owner: BadGuy1. Roster: 2 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: yes; Priority: 10; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: _Base Defense SCR (08DD990C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a4a0b7c"></a>

### Attk_Hard Grp a - 0A4A0B7C

Owner: BadGuy1. Roster: 5 × IFV (FV); 5 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 16; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Hard Grp a SCR (08DE430C).

1. Attack selected enemy-building category; configured argument 131097.
2. Report team success.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-102aeb20"></a>

### Attk_Hard Grp b - 102AEB20

Owner: BadGuy1. Roster: 5 × Grizzly Battle Tank (MTNK); 8 × GI (E1); 5 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 16; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Hard Grp b SCR (08DE3C8C).

1. Attack selected enemy-building category; configured argument 131092.
2. Report team success.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 1.

<a id="team-03d85d70"></a>

### Attk_Destroyer x3 - 03D85D70

Owner: BadGuy1. Roster: 3 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Destroyer x3 SCR (08DE37DC).

1. Attack selected enemy-building category; configured argument 131133.
2. Report team success.
3. Adopt object mission: hunt.

<a id="team-0a719940"></a>

### Def_Navy - 0A719940

Owner: BadGuy1. Roster: 3 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: _Base Defense SCR (08DD990C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bffa59c"></a>

### Invasion Para 4 - 0BFFA59C

Owner: BadGuy1. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: W.

Ordered plan: Invasion Para 4 SCR (0975E6CC).

1. Move to waypoint: waypoint 21 (cell 94, 49).
2. Attack selected enemy-building category; configured argument 131086.
3. Seek/attack target category; configured argument 3.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 1.

<a id="team-08b3b99c"></a>

### Attk_GI Bldg Occupy x8 - 08B3B99C

Owner: BadGuy1. Roster: 8 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 18; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_GI Bldg Occupy x8 SCR (08DE2A1C).

1. Attack selected enemy-building category; configured argument 131178.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-047374dc"></a>

### Allied Landing Feint Attack_AF - 047374DC

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: Landing@AF (04732DBC).

1. Move to waypoint: waypoint 31 (cell 91, 135).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Set local flag: local flag 7 (Feint GI Landing 1).
4. Move to waypoint: waypoint 35 (cell 129, 131).
5. Delete team objects.

<a id="team-047373ac"></a>

### Allied Landing Feint Attack_AG - 047373AC

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: Landing@AG (04732B4C).

1. Move to waypoint: waypoint 32 (cell 93, 132).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Set local flag: local flag 8 (Feint GI Landing 2).
4. Move to waypoint: waypoint 35 (cell 129, 131).
5. Delete team objects.

<a id="team-04732a1c"></a>

### Allied Landing Feint Attack_AH - 04732A1C

Owner: BadGuy1. Roster: 1 × Grizzly Battle Tank (MTNK); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: Landing@AH (0B7FDDBC).

1. Move to waypoint: waypoint 33 (cell 91, 128).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Set local flag: local flag 12 (Feint Tank 1).
4. Move to waypoint: waypoint 35 (cell 129, 131).
5. Delete team objects.

<a id="team-0473256c"></a>

### Allied Landing Feint Attack_AI - 0473256C

Owner: BadGuy1. Roster: 1 × Grizzly Battle Tank (MTNK); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: Landing@AI (0B7FD90C).

1. Move to waypoint: waypoint 34 (cell 84, 118).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Set local flag: local flag 13 (Feint Tank 2).
4. Move to waypoint: waypoint 35 (cell 129, 131).
5. Delete team objects.

<a id="team-0bffba4c"></a>

### GI Feint Attack 1 - 0BFFBA4C

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: GI Feint Attack (0B01A54C).

1. Seek/attack target category; configured argument 7.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 1.

<a id="team-0bffb6ac"></a>

### GI Feint Atttack 2 - 0BFFB6AC

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AG.

Ordered plan: GI Feint Attack (0B01A54C).

1. Seek/attack target category; configured argument 7.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 1.

<a id="team-0bfa7efc"></a>

### Tank Feint Attack 1 - 0BFA7EFC

Owner: BadGuy1. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AH.

Ordered plan: Tank Feint Attack (0BFA204C).

1. Move to waypoint: waypoint 36 (cell 81, 127).
2. Seek/attack target category; configured argument 9.
3. Seek/attack target category; configured argument 1.

<a id="team-0bfa2efc"></a>

### Tank Feint Attack 2 - 0BFA2EFC

Owner: BadGuy1. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AI.

Ordered plan: Tank Feint Attack 2 (0BFA54FC).

1. Move to waypoint: waypoint 36 (cell 81, 127).
2. Seek/attack target category; configured argument 1.

<a id="team-0db377dc"></a>

### Lighthouse Lady - 0DB377DC

Owner: Neutral. Roster: 1 × Civilian (CIVSF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AL.

Ordered plan: Civilian Panic (0C16511C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-0db3732c"></a>

### Fishing Village People - 0DB3732C

Owner: Neutral. Roster: 1 × Civilian (CIVSFM); 1 × Civilian (CIVSF); 1 × Civilian (CIVSTM)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: Civilian Panic (0C16511C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-0ba0eebc"></a>

### Engineer_IFV Rush - 0BA0EEBC

Owner: BadGuy1. Roster: 1 × Engineer (ENGINEER); 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Engineer_IFV Attack (0BA0F48C).

1. Load transport.
2. Move to waypoint: waypoint 38 (cell 29, 110).
3. Move to waypoint: waypoint 39 (cell 44, 127).
4. Unload with continuation mode: passengers continue; transport leaves team.
5. Attack selected enemy-building category; configured argument 131072.

<a id="team-09e6cbfc"></a>

### 1 Intruder (Attacks Navy) - 09E6CBFC

Owner: BadGuy1. Roster: 1 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: Intruder vs Naval Yard (09E6DD0C).

1. Attack selected enemy-building category; configured argument 131133.
