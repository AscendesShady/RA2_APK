# Operation: City of Lights - team rosters and plans

[Trigger ledger](sov05u.md) | [Mission overrides](sov05u-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov05u.map; each team/script ID identifies its section.

<a id="team-07701760"></a>

### Suicide GI - 07701760

Owner: BadGuy1. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: Suicide Run (089DADC0).

1. Move to waypoint: waypoint 3 (cell 74, 76).
2. Seek/attack target category; configured argument 1.

<a id="team-08ab64e0"></a>

### CivCar1Team - 08AB64E0

Owner: Other1. Roster: 1 × Pickup Truck (PICK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AA.

Ordered plan: CivCar1Path (089311C0).

1. Move to waypoint: waypoint 26 (cell 50, 50).
2. Move to waypoint: waypoint 27 (cell 64, 50).
3. Move to waypoint: waypoint 28 (cell 64, 57).
4. Move to waypoint: waypoint 29 (cell 83, 57).
5. Move to waypoint: waypoint 30 (cell 83, 68).
6. Move to waypoint: waypoint 31 (cell 75, 68).
7. Move to waypoint: waypoint 32 (cell 73, 69).
8. Move to waypoint: waypoint 33 (cell 69, 65).
9. Move to waypoint: waypoint 34 (cell 67, 67).
10. Move to waypoint: waypoint 35 (cell 50, 67).
11. Jump to script line; configured argument 1.

<a id="team-076e4560"></a>

### CivCar2Team - 076E4560

Owner: Other1. Roster: 1 × Pickup Truck (PICK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BF.

Ordered plan: CivCar2Path (0844E980).

1. Move to waypoint: waypoint 52 (cell 38, 29).
2. Move to waypoint: waypoint 53 (cell 40, 29).
3. Move to waypoint: waypoint 54 (cell 40, 50).
4. Move to waypoint: waypoint 55 (cell 51, 50).
5. Move to waypoint: waypoint 56 (cell 51, 58).
6. Move to waypoint: waypoint 57 (cell 38, 58).
7. Jump to script line; configured argument 1.

<a id="team-076e41e0"></a>

### CivCar3Team - 076E41E0

Owner: Other1. Roster: 1 × Pickup Truck (PICK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CA.

Ordered plan: CivCar3Path (076E35A0).

1. Move to waypoint: waypoint 78 (cell 51, 67).
2. Move to waypoint: waypoint 79 (cell 51, 75).
3. Move to waypoint: waypoint 80 (cell 71, 75).
4. Move to waypoint: waypoint 81 (cell 71, 85).
5. Move to waypoint: waypoint 82 (cell 60, 85).
6. Move to waypoint: waypoint 83 (cell 60, 67).
7. Jump to script line; configured argument 1.

<a id="team-0ebf61cc"></a>

### Full Transport Team - 0EBF61CC

Owner: Other3. Roster: 1 × Amphibious Transport (SAPC); 6 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Just Sit There (0EBF5DBC).

1. Move to waypoint: waypoint 61 (cell 32, 53).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Change country ownership; configured argument 13.

<a id="team-088b124c"></a>

### Full Trak Team - 088B124C

Owner: Other3. Roster: 2 × Conscript (E2); 3 × Tesla Trooper (SHK); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Just Sit There Really (0A99854C).

1. Adopt object mission: stop.

<a id="team-0b458e1c"></a>

### GI Patrol 1 - 0B458E1C

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AL.

Ordered plan: AM AN AO AL Patrol (0B458BAC).

1. Attack-move toward waypoint: waypoint 38 (cell 61, 76).
2. Attack-move toward waypoint: waypoint 39 (cell 70, 76).
3. Attack-move toward waypoint: waypoint 40 (cell 70, 84).
4. Attack-move toward waypoint: waypoint 37 (cell 61, 84).
5. Jump to script line; configured argument 1.

<a id="team-0b45856c"></a>

### GI Patrol 2 - 0B45856C

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CA.

Ordered plan: CF AP CB CA Patrol (0B4582FC).

1. Attack-move toward waypoint: waypoint 83 (cell 60, 67).
2. Attack-move toward waypoint: waypoint 41 (cell 60, 75).
3. Attack-move toward waypoint: waypoint 79 (cell 51, 75).
4. Attack-move toward waypoint: waypoint 78 (cell 51, 67).
5. Jump to script line; configured argument 1.

<a id="team-0b4586bc"></a>

### GI Patrol 3 - 0B4586BC

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AU.

Ordered plan: AX AW AV AU Patrol (0B459C1C).

1. Attack-move toward waypoint: waypoint 49 (cell 50, 57).
2. Attack-move toward waypoint: waypoint 48 (cell 50, 51).
3. Attack-move toward waypoint: waypoint 47 (cell 40, 51).
4. Attack-move toward waypoint: waypoint 46 (cell 40, 57).
5. Jump to script line; configured argument 1.

<a id="team-0b45991c"></a>

### GI Patrol 4 - 0B45991C

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AS.

Ordered plan: AR AQ AT AS Patrol (0B4596AC).

1. Attack-move toward waypoint: waypoint 43 (cell 63, 57).
2. Attack-move toward waypoint: waypoint 42 (cell 51, 57).
3. Attack-move toward waypoint: waypoint 45 (cell 51, 51).
4. Attack-move toward waypoint: waypoint 44 (cell 63, 51).
5. Jump to script line; configured argument 1.

<a id="team-09ff31ac"></a>

### GI Patrol 5 - 09FF31AC

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AV.

Ordered plan: AZ AY Patrol (09FF1DBC).

1. Attack-move toward waypoint: waypoint 51 (cell 64, 58).
2. Attack-move toward waypoint: waypoint 50 (cell 82, 58).
3. Jump to script line; configured argument 1.

<a id="team-0a0912dc"></a>

### GI Patrol 6 - 0A0912DC

Owner: BadGuy1. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: BG.

Ordered plan: BH BG Patrol (0A090DBC).

1. Attack-move toward waypoint: waypoint 59 (cell 27, 33).
2. Attack-move toward waypoint: waypoint 58 (cell 39, 33).
3. Jump to script line; configured argument 1.

<a id="team-083d089c"></a>

### 1 Tesla Trooper Team - 083D089C

Owner: Player. Roster: 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BI.

Ordered plan: Change to Other3 (084C3DBC).

1. Change country ownership; configured argument 20.

<a id="team-0a0ec38c"></a>

### 1 Flak Trak Team - 0A0EC38C

Owner: Other3. Roster: 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: R.

Ordered plan: Change to Player (0A1C903C).

1. Change country ownership; configured argument 13.

<a id="team-084413fc"></a>

### Re_6 GIs_2 Tanks Team - 084413FC

Owner: BadGuy1. Roster: 6 × GI (E1); 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0; Waypoint: G.

Ordered plan: Guard Area (08444DBC).

1. Adopt object mission: area guard.

<a id="team-08444a1c"></a>

### Re_3 IFV Team - 08444A1C

Owner: BadGuy1. Roster: 3 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0; Waypoint: BG.

Ordered plan: Guard Area (08444DBC).

1. Adopt object mission: area guard.
