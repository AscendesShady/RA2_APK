# Operation: Sub-Divide - team rosters and plans

[Trigger ledger](sov06t.md) | [Mission overrides](sov06t-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov06t.map; each team/script ID identifies its section.

<a id="team-0e4fe57c"></a>

### Scouts1 - 0E4FE57C

Owner: BadGuy1. Roster: 5 × GI (E1); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AT.

Ordered plan: ScoutTroops (0E4FE30C).

1. Move to waypoint: waypoint 45 (cell 54, 118).
2. Load transport.
3. Move to waypoint: waypoint 9 (cell 176, 85).
4. Report team success.
5. Unload with continuation mode: passengers continue; transport leaves team.
6. Guard for interval; configured argument 10.
7. Adopt object mission: hunt.

<a id="team-0e4fdefc"></a>

### Scouts2 - 0E4FDEFC

Owner: BadGuy1. Roster: 5 × GI (E1); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AU.

Ordered plan: Scouts2 (0E4FDC8C).

1. Move to waypoint: waypoint 46 (cell 78, 96).
2. Load transport.
3. Move to waypoint: waypoint 48 (cell 168, 47).
4. Report team success.
5. Unload with continuation mode: passengers continue; transport leaves team.
6. Guard for interval; configured argument 10.
7. Adopt object mission: hunt.

<a id="team-0fca056c"></a>

### AsianFleet1 - 0FCA056C

Owner: KoreanFleet. Roster: 4 × Destroyer (DEST); 1 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: ReinforceAllies1 (0FCA02FC).

1. Attack-move toward waypoint: waypoint 5 (cell 118, 137).
2. Scatter.
3. Set facing; configured argument 2.
4. Guard for interval; configured argument 20.
5. Gather near enemy base; configured argument 0.
6. Seek/attack target category; configured argument 7.
7. Seek/attack target category; configured argument 9.
8. Seek/attack target category; configured argument 4.
9. Seek/attack target category; configured argument 10.
10. Seek/attack target category; configured argument 9.
11. Seek/attack target category; configured argument 8.
12. Jump to script line; configured argument 6.

<a id="team-0fcafefc"></a>

### AsianFleet2 - 0FCAFEFC

Owner: KoreanFleet. Roster: 1 × Aegis Cruiser (AEGIS); 1 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: ReinforceAllies3 (0FCAFC8C).

1. Move to waypoint: waypoint 7 (cell 125, 132).
2. Scatter.
3. Set facing; configured argument 2.
4. Guard for interval; configured argument 20.
5. Gather near enemy base; configured argument 0.
6. Attack selected enemy-building category; configured argument 131087.
7. Attack selected enemy-building category; configured argument 131097.
8. Seek/attack target category; configured argument 6.
9. Seek/attack target category; configured argument 7.
10. Seek/attack target category; configured argument 9.
11. Seek/attack target category; configured argument 5.
12. Jump to script line; configured argument 6.

<a id="team-0b0dc7dc"></a>

### AsianFleet3 - 0B0DC7DC

Owner: KoreanFleet. Roster: 1 × Aegis Cruiser (AEGIS); 3 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: ReinforceAllies3 (0FCAFC8C).

1. Move to waypoint: waypoint 7 (cell 125, 132).
2. Scatter.
3. Set facing; configured argument 2.
4. Guard for interval; configured argument 20.
5. Gather near enemy base; configured argument 0.
6. Attack selected enemy-building category; configured argument 131087.
7. Attack selected enemy-building category; configured argument 131097.
8. Seek/attack target category; configured argument 6.
9. Seek/attack target category; configured argument 7.
10. Seek/attack target category; configured argument 9.
11. Seek/attack target category; configured argument 5.
12. Jump to script line; configured argument 6.

<a id="team-0fcaf80c"></a>

### AsianFleet4 - 0FCAF80C

Owner: KoreanFleet. Roster: 2 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: ReinforceAllies4 (0FCAF59C).

1. Attack-move toward waypoint: waypoint 8 (cell 129, 142).
2. Scatter.
3. Set facing; configured argument 2.
4. Guard for interval; configured argument 50.
5. Gather near enemy base; configured argument 0.
6. Seek/attack target category; configured argument 6.
7. Seek/attack target category; configured argument 7.
8. Seek/attack target category; configured argument 5.
9. Seek/attack target category; configured argument 9.
10. Seek/attack target category; configured argument 8.
11. Jump to script line; configured argument 6.

<a id="team-0c10432c"></a>

### Naval1 - 0C10432C

Owner: BadGuy1. Roster: 3 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 40; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackPower,Def,Fact,Any (0C105DBC).

1. Seek/attack target category; configured argument 9.
2. Report team success.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 6.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 5.
7. Seek/attack target category; configured argument 1.

<a id="team-0e4fc48c"></a>

### Harrass1 - 0E4FC48C

Owner: BadGuy1. Roster: 2 × Grizzly Battle Tank (MTNK); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AR.

Ordered plan: Harrass1 (0E4FC21C).

1. Move to waypoint: waypoint 43 (cell 103, 138).
2. Load transport.
3. Move to waypoint: waypoint 10 (cell 169, 71).
4. Report team success.
5. Unload with continuation mode: passengers continue; transport leaves team.
6. Guard for interval; configured argument 5.
7. Seek/attack target category; configured argument 7.
8. Seek/attack target category; configured argument 1.

<a id="team-0e4fbdec"></a>

### Harrass2 - 0E4FBDEC

Owner: BadGuy1. Roster: 1 × Amphibious Transport (LCRF); 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AS.

Ordered plan: Harrass2 (0E4FBB7C).

1. Move to waypoint: waypoint 44 (cell 60, 105).
2. Load transport.
3. Move to waypoint: waypoint 10 (cell 169, 71).
4. Report team success.
5. Unload with continuation mode: passengers continue; transport leaves team.
6. Guard for interval; configured argument 5.
7. Seek/attack target category; configured argument 4.
8. Seek/attack target category; configured argument 9.
9. Seek/attack target category; configured argument 1.

<a id="team-0bf9232c"></a>

### CoastGuard1 - 0BF9232C

Owner: Other1. Roster: 1 × Coast Guard Boat (CDEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CA.

Ordered plan: CoastGuard1 (0AA5A534).

1. Guard for interval; configured argument 10.
2. Attack-move toward waypoint: waypoint 79 (cell 90, 179).
3. Guard for interval; configured argument 10.
4. Attack-move toward waypoint: waypoint 80 (cell 75, 180).
5. Guard for interval; configured argument 10.
6. Attack-move toward waypoint: waypoint 78 (cell 86, 197).
7. Jump to script line; configured argument 1.

<a id="team-0bf91b7c"></a>

### CoastGuard2 - 0BF91B7C

Owner: Other1. Roster: 1 × Coast Guard Boat (CDEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CD.

Ordered plan: CoastGuard2 (0948DDB4).

1. Guard for interval; configured argument 10.
2. Attack-move toward waypoint: waypoint 82 (cell 69, 162).
3. Guard for interval; configured argument 10.
4. Attack-move toward waypoint: waypoint 83 (cell 56, 164).
5. Guard for interval; configured argument 10.
6. Attack-move toward waypoint: waypoint 84 (cell 68, 177).
7. Guard for interval; configured argument 10.
8. Attack-move toward waypoint: waypoint 81 (cell 82, 179).
9. Jump to script line; configured argument 1.

<a id="team-0bf917dc"></a>

### CoastGuard3 - 0BF917DC

Owner: Other1. Roster: 1 × Coast Guard Boat (CDEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CH.

Ordered plan: CoastGuard3 (0948DB34).

1. Guard for interval; configured argument 10.
2. Attack-move toward waypoint: waypoint 86 (cell 52, 151).
3. Guard for interval; configured argument 10.
4. Attack-move toward waypoint: waypoint 87 (cell 47, 161).
5. Guard for interval; configured argument 10.
6. Attack-move toward waypoint: waypoint 85 (cell 63, 164).
7. Jump to script line; configured argument 1.

<a id="team-0bf9143c"></a>

### CoastGuard4 - 0BF9143C

Owner: Other1. Roster: 1 × Coast Guard Boat (CDEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CK.

Ordered plan: CoastGuard4 (0948D8B4).

1. Guard for interval; configured argument 10.
2. Attack-move toward waypoint: waypoint 89 (cell 17, 155).
3. Guard for interval; configured argument 10.
4. Attack-move toward waypoint: waypoint 88 (cell 45, 155).
5. Jump to script line; configured argument 1.

<a id="team-0adceb54"></a>

### AirportHarass - 0ADCEB54

Owner: BadGuy1. Roster: 2 × Grizzly Battle Tank (MTNK); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 29; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AQ.

Ordered plan: AirportHarrass (0AE5FB04).

1. Move to waypoint: waypoint 42 (cell 73, 131).
2. Load transport.
3. Move to waypoint: waypoint 33 (cell 40, 172).
4. Unload with continuation mode: transport and passengers continue.
5. Seek/attack target category; configured argument 11.
6. Seek/attack target category; configured argument 1.

<a id="team-0c16a1ac"></a>

### 2Rocketeers - 0C16A1AC

Owner: BadGuy1. Roster: 2 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Rocketeers (09FABDB4).

1. Seek/attack target category; configured argument 9.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131087.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-0c169b7c"></a>

### 3Rocketeers - 0C169B7C

Owner: BadGuy1. Roster: 3 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Rocketeers (09FABDB4).

1. Seek/attack target category; configured argument 9.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131087.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-0b0d91fc"></a>

### Naval2 - 0B0D91FC

Owner: BadGuy1. Roster: 1 × Aegis Cruiser (AEGIS); 1 × Aircraft Carrier (CARRIER); 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 40; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackAny (08B8621C).

1. Gather near enemy base; configured argument 0.
2. Report team success.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0bfa22cc"></a>

### Naval3 - 0BFA22CC

Owner: BadGuy1. Roster: 1 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 40; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBAny,Power,Any (0BFA205C).

1. Gather near enemy base; configured argument 0.
2. Report team success.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 1.

<a id="team-0bfa7dec"></a>

### Naval4 - 0BFA7DEC

Owner: BadGuy1. Roster: 2 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 40; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackRefine,Fact,Con,Radar (0BFA7B7C).

1. Gather near enemy base; configured argument 0.
2. Report team success.
3. Attack selected enemy-building category; configured argument 15.
4. Seek/attack target category; configured argument 6.
5. Attack selected enemy-building category; configured argument 25.
6. Attack selected enemy-building category; configured argument 13.
7. Seek/attack target category; configured argument 2.
8. Seek/attack target category; configured argument 1.

<a id="team-0af5c0d4"></a>

### BaseDef1 - 0AF5C0D4

Owner: BadGuy1. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AL.

Ordered plan: Guard Area (09FAA064).

1. Scatter.
2. Adopt object mission: area guard.
3. Report team success.

<a id="team-0b0a3efc"></a>

### BaseDef2 - 0B0A3EFC

Owner: BadGuy1. Roster: 3 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AN.

Ordered plan: Guard Area (09FAA064).

1. Scatter.
2. Adopt object mission: area guard.
3. Report team success.

<a id="team-0af5d9e4"></a>

### BaseDef3 - 0AF5D9E4

Owner: BadGuy1. Roster: 3 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AM.

Ordered plan: Guard Area (09FAA064).

1. Scatter.
2. Adopt object mission: area guard.
3. Report team success.

<a id="team-0bfa0dcc"></a>

### BaseDef4(Navy) - 0BFA0DCC

Owner: BadGuy1. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Area 2 (0947A620).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-09ad6520"></a>

### StartForce1a - 09AD6520

Owner: Player. Roster: 1 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: PlayerSubLand_a (09AD62C0).

1. Move to waypoint: waypoint 21 (cell 201, 79).
2. Set facing; configured argument 4.

<a id="team-08d49cb0"></a>

### StartForce2 - 08D49CB0

Owner: Player. Roster: 1 × Amphibious Transport (SAPC); 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: PlayerTrans1Land (0A8A6120).

1. Move to waypoint: waypoint 4 (cell 196, 70).
2. Unload with continuation mode: passengers continue; transport leaves team.

<a id="team-08d49840"></a>

### StartForce3 - 08D49840

Owner: Player. Roster: 1 × Amphibious Transport (SAPC); 1 × Soviet Construction Vehicle (SMCV); 2 × Tesla Trooper (SHK); 2 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: PlayerTrans2Land (0A2B6DE0).

1. Move to waypoint: waypoint 25 (cell 200, 70).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Scatter.

<a id="team-09adfe00"></a>

### StartForce1c - 09ADFE00

Owner: Player. Roster: 1 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: PlayerSubLand_b (09ADFBA0).

1. Move to waypoint: waypoint 22 (cell 203, 79).
2. Set facing; configured argument 4.

<a id="team-09adfa80"></a>

### StartForce1b - 09ADFA80

Owner: Player. Roster: 1 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: PlayerSubLand_c (09ADF820).

1. Move to waypoint: waypoint 23 (cell 205, 79).
2. Set facing; configured argument 4.

<a id="team-09adf700"></a>

### StartForce1d - 09ADF700

Owner: Player. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: PlayerSeaScorpLand_d (09ADF4A0).

1. Move to waypoint: waypoint 24 (cell 204, 82).
2. Set facing; configured argument 4.

<a id="team-09adf280"></a>

### StartForce1e - 09ADF280

Owner: Player. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: PlayerSeaScorpLand_e (09ADBDC0).

1. Move to waypoint: waypoint 20 (cell 202, 82).
2. Set facing; configured argument 4.

<a id="team-0c1bf43c"></a>

### BaseDef5(Harriers) - 0C1BF43C

Owner: BadGuy1. Roster: 4 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CR.

Ordered plan: HarrierDefend (0D93E43C).

1. Approach friendly building category; configured argument 131177.

<a id="team-0b0a532c"></a>

### BaseDefInfantry - 0B0A532C

Owner: BadGuy1. Roster: 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Area 3 (07F8FDC0).

1. Guard for interval; configured argument 50.
2. Report team success.
3. Adopt object mission: patrol.

<a id="team-0bfadb7c"></a>

### Naval6 - 0BFADB7C

Owner: BadGuy1. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 50; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack NavalYard (0948E9A0).

1. Attack selected enemy-building category; configured argument 131133.
2. Report team success.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0ab9932c"></a>

### 3Carriers - 0AB9932C

Owner: BadGuy1. Roster: 3 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: CarrierAttack (0AB98DBC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 2.
3. Seek/attack target category; configured argument 1.

<a id="team-0ab991fc"></a>

### GiftDread1 - 0AB991FC

Owner: Player. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Q.

Ordered plan: DreadToBase1 (0BB3667C).

1. Move to waypoint: waypoint 75 (cell 192, 89).
2. Scatter.
3. Set facing; configured argument 4.
4. Set local flag: local flag 6 (DreadsHome).

<a id="team-0ab9890c"></a>

### GiftDread2 - 0AB9890C

Owner: Player. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Q.

Ordered plan: DreadToBase2 (0AB9869C).

1. Move to waypoint: waypoint 11 (cell 195, 86).
2. Set facing; configured argument 4.
3. Set local flag: local flag 6 (DreadsHome).

<a id="team-0ab9856c"></a>

### GiftDread3 - 0AB9856C

Owner: Player. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Q.

Ordered plan: DreadToBase3 (0AB982FC).

1. Move to waypoint: waypoint 12 (cell 197, 86).
2. Set facing; configured argument 4.
3. Set local flag: local flag 6 (DreadsHome).

<a id="team-0c10d30c"></a>

### GiftScorp1 - 0C10D30C

Owner: Player. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: ScorpToBase4 (0C10EDBC).

1. Follow friendly objects.
2. Set facing; configured argument 4.
3. Set local flag: local flag 6 (DreadsHome).

<a id="team-0c10d1dc"></a>

### GiftScorp2 - 0C10D1DC

Owner: Player. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: B.

Ordered plan: ScorpToBase5 (0C10EB4C).

1. Follow friendly objects.
2. Set facing; configured argument 4.
3. Set local flag: local flag 6 (DreadsHome).

<a id="team-0e50354c"></a>

### Harrass3 - 0E50354C

Owner: BadGuy1. Roster: 2 × Grizzly Battle Tank (MTNK); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AX.

Ordered plan: Harrass3 (0E5032DC).

1. Move to waypoint: waypoint 49 (cell 60, 123).
2. Load transport.
3. Move to waypoint: waypoint 48 (cell 168, 47).
4. Report team success.
5. Unload with continuation mode: passengers continue; transport leaves team.
6. Guard for interval; configured argument 5.
7. Seek/attack target category; configured argument 9.
8. Attack selected enemy-building category; configured argument 131097.
9. Seek/attack target category; configured argument 2.
10. Seek/attack target category; configured argument 1.

<a id="team-097393a4"></a>

### HarrierAnnoyance1 - 097393A4

Owner: BadGuy1. Roster: 2 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: HarrierAttack1 (09743074).

1. Seek/attack target category; configured argument 10.
2. Report team success.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 1.

<a id="team-097422d4"></a>

### HarrierAnnoyance2 - 097422D4

Owner: BadGuy1. Roster: 2 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: HarrierAttack2 (0B2A5654).

1. Seek/attack target category; configured argument 7.
2. Report team success.
3. Seek/attack target category; configured argument 11.
4. Seek/attack target category; configured argument 10.
5. Seek/attack target category; configured argument 1.

<a id="team-09520324"></a>

### Rocketeer VS Airport - 09520324

Owner: BadGuy1. Roster: 3 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: RocketeerAirportAttack (09521DB4).

1. Seek/attack target category; configured argument 11.
2. Report team success.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0c00503c"></a>

### Naval5 - 0C00503C

Owner: BadGuy1. Roster: 1 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 50; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackVeh,Con,Garr,Power,Def (0C00A0EC).

1. Gather near enemy base; configured argument 0.
2. Report team success.
3. Seek/attack target category; configured argument 5.
4. Attack selected enemy-building category; configured argument 131097.
5. Seek/attack target category; configured argument 10.
6. Seek/attack target category; configured argument 9.
7. Seek/attack target category; configured argument 7.
8. Seek/attack target category; configured argument 2.
9. Seek/attack target category; configured argument 1.

<a id="team-0868f29c"></a>

### GiftFleet - 0868F29C

Owner: Player. Roster: 3 × Dreadnought (DRED); 2 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Q.

Ordered plan: DreadToBase1 (0BB3667C).

1. Move to waypoint: waypoint 75 (cell 192, 89).
2. Scatter.
3. Set facing; configured argument 4.
4. Set local flag: local flag 6 (DreadsHome).
