# Operation: Desecration - team rosters and plans

[Trigger ledger](sov08u.md) | [Mission overrides](sov08u-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov08u.map; each team/script ID identifies its section.

<a id="team-0bf1cb5c"></a>

### Scouts1 - 0BF1CB5C

Owner: Vlad2. Roster: 5 × Conscript (E2); 5 × Flak Trooper (FLAKT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Scouts - Find Con, Attack Inf (0BF1C8EC).

1. Move to waypoint: waypoint 13 (cell 91, 24).
2. Approach selected enemy-building category; configured argument 131097.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 1.

<a id="team-0a0cea4c"></a>

### HarassmentTm1 - 0A0CEA4C

Owner: Vlad1. Roster: 5 × Conscript (E2); 2 × Attack Dog (DOG); 2 × Tesla Trooper (SHK); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Harassment1 (08C6A40C).

1. Attack selected enemy-building category; configured argument 131081.
2. Seek/attack target category; configured argument 6.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 1.

<a id="team-0a02448c"></a>

### BaseDef1 - 0A02448C

Owner: Vlad1. Roster: 5 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: GuardBase (0A02421C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bf0193c"></a>

### BaseDef2 - 0BF0193C

Owner: Vlad1. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GuardBase (0A02421C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0ac896fc"></a>

### !WHAttack06 - 0AC896FC

Owner: Vlad2. Roster: 2 × Flak Track (HTK); 10 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBuildings,Any (09FD2A4C).

1. Gather near own base; configured argument 0.
2. Load transport.
3. Attack-move toward waypoint: waypoint 11 (cell 68, 94).
4. Report team success.
5. Approach selected enemy-building category; configured argument 25.
6. Unload with continuation mode: passengers continue; transport leaves team.
7. Seek/attack target category; configured argument 2.
8. Seek/attack target category; configured argument 1.

<a id="team-0a0ca80c"></a>

### !Attack01 - 0A0CA80C

Owner: Vlad1. Roster: 4 × Rhino Heavy Tank (HTNK); 2 × V3 Launcher (V3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBaseDef,ConYard,Any (0AC88DBC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Report team success.
4. Seek/attack target category; configured argument 5.
5. Attack selected enemy-building category; configured argument 25.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-09fd235c"></a>

### !WHAttack03 - 09FD235C

Owner: Vlad2. Roster: 6 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Power,Any,Anything (09FD1DBC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 0.
4. Report team success.
5. Seek/attack target category; configured argument 9.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-0fbb359c"></a>

### ConscriptPatrol - 0FBB359C

Owner: Vlad2. Roster: 5 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: C.

Ordered plan: Patrol (0AC654A0).

1. Move to waypoint: waypoint 78 (cell 80, 30).
2. Move to waypoint: waypoint 79 (cell 80, 48).
3. Move to waypoint: waypoint 80 (cell 120, 48).
4. Move to waypoint: waypoint 81 (cell 120, 31).
5. Move to waypoint: waypoint 80 (cell 120, 48).
6. Move to waypoint: waypoint 79 (cell 80, 48).
7. Move to waypoint: waypoint 78 (cell 80, 30).
8. Jump to script line; configured argument 2.

<a id="team-0a0c943c"></a>

### !Attack02 - 0A0C943C

Owner: Vlad1. Roster: 6 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Power,Any (09FD11CC).

1. Gather near own base; configured argument 0.
2. Attack selected enemy-building category; configured argument 0.
3. Report team success.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-0b1a932c"></a>

### !WHBaseDef1 - 0B1A932C

Owner: Vlad2. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: WhiteHouseBD1 (0B1A8DBC).

1. Move to waypoint: waypoint 28 (cell 102, 51).
2. Adopt object mission: area guard.
3. Report team success.

<a id="team-0b1a8c8c"></a>

### !WHBaseDef2 - 0B1A8C8C

Owner: Vlad2. Roster: 3 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: WhiteHouseBD2 (0B1B032C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-09fd048c"></a>

### !WHBaseDef3 - 09FD048C

Owner: Vlad2. Roster: 5 × Conscript (E2); 3 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: WhiteHouseBD3 (0B1A856C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a02148c"></a>

### !WHAttack07 - 0A02148C

Owner: Vlad2. Roster: 3 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Vehicles, Fact, ConYard (09FDF9DC).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 6.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-0ac96b7c"></a>

### !WHAttack08 - 0AC96B7C

Owner: Vlad2. Roster: 10 × Conscript (E2); 5 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 2; Technology level: 0.

Ordered plan: AttackBaseDef,ConYard,Any (0AC88DBC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Report team success.
4. Seek/attack target category; configured argument 5.
5. Attack selected enemy-building category; configured argument 25.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-0a11c93c"></a>

### HarrassInfantry - 0A11C93C

Owner: Vlad2. Roster: 4 × Desolator (DESO)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: P.

Ordered plan: Hunt (09FDF2EC).

1. Adopt object mission: hunt.
2. Report team success.

<a id="team-0a0d635c"></a>

### !Attack04 - 0A0D635C

Owner: Vlad1. Roster: 3 × V3 Launcher (V3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: BaseDef, Fact, Power, etc (09FDEC8C).

1. Seek/attack target category; configured argument 7.
2. Report team success.
3. Seek/attack target category; configured argument 6.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-0a11bdec"></a>

### !WHAttack09 - 0A11BDEC

Owner: Vlad2. Roster: 2 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Vehicles, Inf (09FDE7DC).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 3.
6. Seek/attack target category; configured argument 1.

<a id="team-0a11b93c"></a>

### !WHAttack10 - 0A11B93C

Owner: Vlad2. Roster: 7 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Vehicles, Fact, Power, etc (09FDE32C).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 6.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 1.

<a id="team-0c3f393c"></a>

### Vladimir - 0C3F393C

Owner: Vlad2. Roster: 1 × Civilian (VLADIMIR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: StandThere (0C3F36CC).

1. Set facing; configured argument 4.
2. Adopt object mission: guard.

<a id="team-0a11adec"></a>

### !WHAttack11 - 0A11ADEC

Owner: Vlad2. Roster: 2 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackHarv,Vehicles (0A80C940).

1. Attack-move toward waypoint: waypoint 11 (cell 68, 94).
2. Seek/attack target category; configured argument 3.
3. Report team success.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-0a11aa4c"></a>

### !WHAttack12 - 0A11AA4C

Owner: Vlad2. Roster: 4 × Desolator (DESO)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Deso Harass (0B31B7DC).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Adopt object mission: hunt.

<a id="team-0fbcd32c"></a>

### Garrison1 - 0FBCD32C

Owner: Vlad2. Roster: 8 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY12 (0A02E43C).

1. Attack selected enemy-building category; configured argument 131235.

<a id="team-0fbcedec"></a>

### Garrison2 - 0FBCEDEC

Owner: Vlad2. Roster: 8 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash7 (07EE574C).

1. Attack selected enemy-building category; configured argument 131183.

<a id="team-0b60354c"></a>

### Garrison3 - 0B60354C

Owner: Vlad1. Roster: 8 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash5 (07F7A5FC).

1. Attack selected enemy-building category; configured argument 131180.

<a id="team-09fdbb5c"></a>

### Paratroopers - 09FDBB5C

Owner: Vlad1. Roster: 15 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 2; Technology level: 0; Transport Waypoint: T.

Ordered plan: AttackAnything (09F34A3C).

1. Seek/attack target category; configured argument 1.

<a id="team-0b103b7c"></a>

### !Attack03 - 0B103B7C

Owner: Vlad1. Roster: 2 × Apocalypse (APOC); 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackRefine,Any (0B1037FC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 15.
4. Report team success.
5. Attack selected enemy-building category; configured argument 131087.
6. Seek/attack target category; configured argument 7.
7. Seek/attack target category; configured argument 2.
8. Seek/attack target category; configured argument 1.

<a id="team-0853b3bc"></a>

### !WHAttack01 - 0853B3BC

Owner: Vlad2. Roster: 3 × Attack Dog (DOG); 2 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: WHAttackInf,Any (0853D40C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0853ecfc"></a>

### !WHAttack02 - 0853ECFC

Owner: Vlad2. Roster: 2 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Power,Any,Anything (09FD1DBC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 0.
4. Report team success.
5. Seek/attack target category; configured argument 9.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-0a11859c"></a>

### !Attack05 - 0A11859C

Owner: Vlad1. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: BaseDefProbe (0853E36C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0a1181fc"></a>

### !Attack06 - 0A1181FC

Owner: Vlad1. Roster: 4 × Engineer (SENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: EngineerBuildings (085623FC).

1. Seek/attack target category; configured argument 6.
2. Report team success.
3. Attack selected enemy-building category; configured argument 15.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 6.
6. Attack selected enemy-building category; configured argument 10.
7. Seek/attack target category; configured argument 2.

<a id="team-08563d3c"></a>

### !WHAttack04 - 08563D3C

Owner: Vlad2. Roster: 3 × Engineer (ENGINEER); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Engineer/TransAttack (085639BC).

1. Gather near own base; configured argument 0.
2. Load transport.
3. Approach selected enemy-building category; configured argument 11.
4. Report team success.
5. Unload with continuation mode: passengers continue; transport leaves team.
6. Seek/attack target category; configured argument 6.
7. Seek/attack target category; configured argument 2.

<a id="team-085810ec"></a>

### !WHAttack05 - 085810EC

Owner: Vlad2. Roster: 5 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackInfantry (0858331C).

1. Seek/attack target category; configured argument 4.
2. Report team success.

<a id="team-0890e2ec"></a>

### !WHAttack13 - 0890E2EC

Owner: Vlad2. Roster: 4 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackVeh,Def,Veh,Any (0AA6DB1C).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-0880e39c"></a>

### !WHAttack14 - 0880E39C

Owner: Vlad2. Roster: 1 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackVeh,Def,Veh,Any (0AA6DB1C).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-08837efc"></a>

### ShockPatrol - 08837EFC

Owner: Vlad1. Roster: 2 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: ShockPatrol (0882ADBC).

1. Attack-move toward waypoint: waypoint 4 (cell 111, 136).
2. Attack-move toward waypoint: waypoint 0 (cell 111, 121).
3. Jump to script line; configured argument 1.

<a id="team-087d21ec"></a>

### EliteApocGuard - 087D21EC

Owner: Vlad2. Roster: 2 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 3; Technology level: 0.

Ordered plan: GuardBase (0A02421C).

1. Adopt object mission: area guard.
2. Report team success.
