# Operation: Big Apple - team rosters and plans

[Trigger ledger](sov03u.md) | [Mission overrides](sov03u-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov03u.map; each team/script ID identifies its section.

<a id="team-08d1f920"></a>

### 4GI Team - 08D1F920

Owner: BadGuy1. Roster: 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: Any Attack (0A0E2B7C).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-08d1f4a0"></a>

### Base D - 08D1F4A0

Owner: BadGuy1. Roster: 4 × GI (E1)

Explicit team settings: Autocreate: yes; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Base Defense (0A4FD460).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a0e259c"></a>

### 2Grizzly Team - 0A0E259C

Owner: BadGuy1. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Any Attack (0A0E2B7C).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-0c199c8c"></a>

### 4Rocket Team - 0C199C8C

Owner: BadGuy1. Roster: 4 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack V3 then Any (08CE2820).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-08d1e980"></a>

### GI Attack Power - 08D1E980

Owner: BadGuy1. Roster: 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Player Base (0B94359C).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131072.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-099fb8ec"></a>

### 2 IFV 2 GI Team - 099FB8EC

Owner: BadGuy1. Roster: 2 × IFV (FV); 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 20; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: IFV Vehicle Attack (099FB67C).

1. Seek/attack target category; configured argument 5.
2. Report team success.

<a id="team-08d1e180"></a>

### Re_Tank - 08D1E180

Owner: BadGuy1. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: Sov03 Lab/Beacon Attack (09693DB4).

1. Attack selected enemy-building category; configured argument 131255.
2. Seek/attack target category; configured argument 1.

<a id="team-08d1dca0"></a>

### Outpost B - 08D1DCA0

Owner: BadGuy1. Roster: 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: Guard Outpost B (08CE16C0).

1. Adopt object mission: guard.

<a id="team-099fdb5c"></a>

### 4IFV Patrol - 099FDB5C

Owner: BadGuy1. Roster: 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0; Waypoint: C.

Ordered plan: IFV Patrol (0976E800).

1. Attack-move toward waypoint: waypoint 3 (cell 77, 78).
2. Attack-move toward waypoint: waypoint 2 (cell 130, 78).
3. Jump to script line; configured argument 1.

<a id="team-099fd6ac"></a>

### 4aIFV Patrol - 099FD6AC

Owner: BadGuy1. Roster: 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: E.

Ordered plan: IFV Patrol (E, F) (0BE3F650).

1. Attack-move toward waypoint: waypoint 5 (cell 130, 92).
2. Attack-move toward waypoint: waypoint 4 (cell 130, 38).
3. Jump to script line; configured argument 1.

<a id="team-099fd30c"></a>

### 4bIFV Patrol - 099FD30C

Owner: BadGuy1. Roster: 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: G.

Ordered plan: IFV Patrol (G, H) (0BE3F180).

1. Attack-move toward waypoint: waypoint 7 (cell 108, 51).
2. Attack-move toward waypoint: waypoint 6 (cell 109, 112).
3. Jump to script line; configured argument 1.

<a id="team-0d33d8ec"></a>

### 4cIFV Patrol - 0D33D8EC

Owner: BadGuy1. Roster: 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: IFV Patrol (I, J) (0ADEF1CC).

1. Attack-move toward waypoint: waypoint 8 (cell 75, 94).
2. Attack-move toward waypoint: waypoint 9 (cell 81, 36).
3. Jump to script line; configured argument 1.

<a id="team-096948d4"></a>

### Re_GI - 096948D4

Owner: BadGuy1. Roster: 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Sov03 Lab/Beacon Attack (09693DB4).

1. Attack selected enemy-building category; configured argument 131255.
2. Seek/attack target category; configured argument 1.

<a id="team-099fe8ec"></a>

### Re_IFV - 099FE8EC

Owner: BadGuy1. Roster: 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Sov03 Lab/Beacon Attack (09693DB4).

1. Attack selected enemy-building category; configured argument 131255.
2. Seek/attack target category; configured argument 1.

<a id="team-08d1c6e0"></a>

### Re_Rocket - 08D1C6E0

Owner: BadGuy1. Roster: 6 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Sov03 Lab/Beacon Attack (09693DB4).

1. Attack selected enemy-building category; configured argument 131255.
2. Seek/attack target category; configured argument 1.

<a id="team-0c19f1bc"></a>

### Final_Tank2 - 0C19F1BC

Owner: BadGuy1. Roster: 6 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 2; Technology level: 0.

Ordered plan: Final Attack (09F2855C).

1. Adopt object mission: hunt.

<a id="team-0c19eb7c"></a>

### Final_IFV - 0C19EB7C

Owner: BadGuy1. Roster: 6 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 2; Technology level: 0.

Ordered plan: Final Attack (09F2855C).

1. Adopt object mission: hunt.

<a id="team-0c19e93c"></a>

### Final_Tank - 0C19E93C

Owner: BadGuy1. Roster: 6 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 2; Technology level: 0.

Ordered plan: Final Attack (09F2855C).

1. Adopt object mission: hunt.

<a id="team-0c19e80c"></a>

### Final_Rocket - 0C19E80C

Owner: BadGuy1. Roster: 6 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 2; Technology level: 0; Waypoint: J.

Ordered plan: Final Attack (09F2855C).

1. Adopt object mission: hunt.

<a id="team-0c19e6dc"></a>

### 10 GIs - 0C19E6DC

Owner: BadGuy1. Roster: 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Player Base (0B94359C).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131072.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0c19e49c"></a>

### 6 Grizzly Team - 0C19E49C

Owner: BadGuy1. Roster: 6 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Player Base (0B94359C).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131072.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0c19e36c"></a>

### Final IFV 2 - 0C19E36C

Owner: BadGuy1. Roster: 6 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 2; Technology level: 0.

Ordered plan: Final Attack (09F2855C).

1. Adopt object mission: hunt.

<a id="team-0c19e23c"></a>

### 6 Rocket Team - 0C19E23C

Owner: BadGuy1. Roster: 6 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack from Sea (0BBE1C8C).

1. Move to waypoint: waypoint 16 (cell 34, 114).
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 2.

<a id="team-0c1df0cc"></a>

### Death Tanks - 0C1DF0CC

Owner: BadGuy1. Roster: 6 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Final Attack (09F2855C).

1. Adopt object mission: hunt.

<a id="team-0c1d8efc"></a>

### Death IFVs - 0C1D8EFC

Owner: BadGuy1. Roster: 6 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Final Attack (09F2855C).

1. Adopt object mission: hunt.

<a id="team-0c1d88ec"></a>

### Death GIs - 0C1D88EC

Owner: BadGuy1. Roster: 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Final Attack (09F2855C).

1. Adopt object mission: hunt.

<a id="team-0c1d87bc"></a>

### Death Rocketeers - 0C1D87BC

Owner: BadGuy1. Roster: 6 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Final Attack (09F2855C).

1. Adopt object mission: hunt.

<a id="team-0ade8a3c"></a>

### 4 Psi-Corp Team - 0ADE8A3C

Owner: Player. Roster: 4 × Yuri (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AI; Transport Waypoint: AJ.

Ordered plan: Do Nothing (0836C9EC).

1. Adopt object mission: stop.

<a id="team-0ae6f1ec"></a>

### 6 Psi-Corp Team - 0AE6F1EC

Owner: Player. Roster: 6 × Yuri (YURI); 5 × Flak Trooper (FLAKT); 5 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AC.

Ordered plan: Do Nothing (0836C9EC).

1. Adopt object mission: stop.

<a id="team-0c1d959c"></a>

### Garrison AF Team - 0C1D959C

Owner: BadGuy1. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: Garrison AF (09BA756C).

1. Attack waypoint: waypoint 31 (cell 91, 96).

<a id="team-0c1d91fc"></a>

### Garrison AG Team - 0C1D91FC

Owner: BadGuy1. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AG.

Ordered plan: Garrison AG (09BA71CC).

1. Attack waypoint: waypoint 32 (cell 119, 82).

<a id="team-0af10b5c"></a>

### 2 Grizzly RE Team - 0AF10B5C

Owner: Player. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: Move to Psy Beacon (086261DC).

1. Move to waypoint: waypoint 10 (cell 105, 17).
2. Move to waypoint: waypoint 28 (cell 103, 31).
