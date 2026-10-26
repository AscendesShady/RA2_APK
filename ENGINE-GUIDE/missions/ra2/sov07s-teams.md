# Operation: Chrono Defense - team rosters and plans

[Trigger ledger](sov07s.md) | [Mission overrides](sov07s-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov07s.map; each team/script ID identifies its section.

<a id="team-0b12f93c"></a>

### Propaganda Truck - 0B12F93C

Owner: Other1. Roster: 1 × Propaganda Truck (PROPA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: A.

Ordered plan: PropTruckRoute (092201AC).

1. Move to waypoint: waypoint 0 (cell 137, 84).
2. Move to waypoint: waypoint 1 (cell 128, 91).
3. Move to waypoint: waypoint 2 (cell 112, 75).
4. Move to waypoint: waypoint 3 (cell 106, 84).
5. Move to waypoint: waypoint 4 (cell 106, 92).
6. Move to waypoint: waypoint 5 (cell 105, 98).
7. Move to waypoint: waypoint 6 (cell 95, 105).
8. Move to waypoint: waypoint 7 (cell 94, 111).
9. Move to waypoint: waypoint 8 (cell 89, 116).
10. Move to waypoint: waypoint 9 (cell 83, 117).
11. Move to waypoint: waypoint 10 (cell 79, 114).
12. Move to waypoint: waypoint 11 (cell 69, 125).
13. Move to waypoint: waypoint 12 (cell 47, 124).
14. Move to waypoint: waypoint 13 (cell 45, 126).
15. Move to waypoint: waypoint 14 (cell 39, 121).
16. Set local flag: local flag 0 (PropTruckArrived).
17. Move to waypoint: waypoint 78 (cell 38, 97).
18. Move to waypoint: waypoint 79 (cell 38, 91).
19. Move to waypoint: waypoint 80 (cell 32, 85).
20. Move to waypoint: waypoint 81 (cell 25, 85).
21. Move to waypoint: waypoint 82 (cell 20, 89).
22. Move to waypoint: waypoint 83 (cell 22, 95).
23. Move to waypoint: waypoint 84 (cell 28, 99).
24. Move to waypoint: waypoint 85 (cell 33, 97).
25. Jump to script line; configured argument 17.

<a id="team-0c13f1fc"></a>

### ConvertedSoviets1 - 0C13F1FC

Owner: Civilian1. Roster: 3 × Civilian (CIVSFM); 3 × Civilian (CIVSF); 3 × Civilian (CIVSTM)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CA.

Ordered plan: ChangeHouse (0C178DBC).

1. Change country ownership; configured argument 14.

<a id="team-0ef6bb7c"></a>

### !Sniper - Inf - 0EF6BB7C

Owner: BadGuy1. Roster: 1 × Sniper (SNIPE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: SnipeInfantry (0EF6B90C).

1. Guard for interval; configured argument 80.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 1.

<a id="team-0ef6b6cc"></a>

### !Sniper/GI Squad - Inf - 0EF6B6CC

Owner: BadGuy1. Roster: 1 × Sniper (SNIPE); 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: AntiPersonnelSquad (0EF6B45C).

1. Guard for interval; configured argument 80.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 1.

<a id="team-0c32e21c"></a>

### !Tank Team (4) - Def,Any - 0C32E21C

Owner: BadGuy1. Roster: 4 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: AttackBaseDef,Any (0EF6CDBC).

1. Attack selected enemy-building category; configured argument 67.
2. Seek/attack target category; configured argument 7.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0b299b7c"></a>

### !GI/IFV Combo - Factory, ConYard - 0B299B7C

Owner: BadGuy1. Roster: 1 × IFV (FV); 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 8; Veteran Level: 1; Technology level: 0.

Ordered plan: Factory/ConYard Attack (0B29990C).

1. Unload with continuation mode: transport and passengers continue.
2. Load transport.
3. Seek/attack target category; configured argument 6.
4. Attack selected enemy-building category; configured argument 25.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-09f724e0"></a>

### !Rocketeer (3) - Vehicles - 09F724E0

Owner: BadGuy1. Roster: 3 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: VehicleAttack (0A6C1DE0).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 1.

<a id="team-0ef6c21c"></a>

### !GI Rush (10) - Power - 0EF6C21C

Owner: BadGuy1. Roster: 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: GI Rush1 (0EF6DDBC).

1. Guard for interval; configured argument 80.
2. Seek/attack target category; configured argument 9.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0ef6db7c"></a>

### !Rocketeer (2) - BattleLab - 0EF6DB7C

Owner: BadGuy1. Roster: 2 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: RktAttackBattleLab1 (0B2F3A5C).

1. Attack selected enemy-building category; configured argument 131082.
2. Seek/attack target category; configured argument 9.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0ef6d6cc"></a>

### !Spy (1) - Power - 0EF6D6CC

Owner: BadGuy2. Roster: 1 × Spy (SPY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 8; Veteran Level: 1; Technology level: 0.

Ordered plan: SpyOnPower (0EF6D45C).

1. Guard for interval; configured argument 80.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 9.
4. Attack selected enemy-building category; configured argument 13.
5. Attack selected enemy-building category; configured argument 15.
6. Seek/attack target category; configured argument 2.

<a id="team-0ef6d21c"></a>

### !GI Rush (5) - Power - 0EF6D21C

Owner: BadGuy1. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: GI Rush1 (0EF6DDBC).

1. Guard for interval; configured argument 80.
2. Seek/attack target category; configured argument 9.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0ef6edec"></a>

### !Rocketeer (3) - BaseDef,BatLab - 0EF6EDEC

Owner: BadGuy1. Roster: 3 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: RktBaseDef,BattleLab (0B2F37EC).

1. Seek/attack target category; configured argument 7.
2. Attack selected enemy-building category; configured argument 131082.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0a0a4420"></a>

### !Harriers (2) - Factories - 0A0A4420

Owner: BadGuy1. Roster: 2 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: HarrierAttackFact (0A0A41C0).

1. Seek/attack target category; configured argument 6.
2. Seek/attack target category; configured argument 7.
3. Seek/attack target category; configured argument 1.
4. Move to waypoint: waypoint 15 (cell 96, 139).
5. Delete team objects.

<a id="team-0ef6e59c"></a>

### !Tank Team (4) - Def,Refinery - 0EF6E59C

Owner: BadGuy1. Roster: 4 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackDef,Refine (0EF6E32C).

1. Seek/attack target category; configured argument 7.
2. Attack selected enemy-building category; configured argument 15.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-08df411c"></a>

### !Rocketeer (8) - Vehicles,ConYard,Power - 08DF411C

Owner: BadGuy1. Roster: 8 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackVehicles2 (08DF5DBC).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131097.
4. Seek/attack target category; configured argument 9.
5. Attack selected enemy-building category; configured argument 131082.
6. Seek/attack target category; configured argument 1.

<a id="team-0ef6fb7c"></a>

### !Spy (1) - Radar - 0EF6FB7C

Owner: BadGuy2. Roster: 1 × Spy (SPY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackRadar/Power (0EF6F90C).

1. Guard for interval; configured argument 80.
2. Seek/attack target category; configured argument 4.
3. Attack selected enemy-building category; configured argument 13.
4. Seek/attack target category; configured argument 9.
5. Attack selected enemy-building category; configured argument 15.
6. Seek/attack target category; configured argument 2.

<a id="team-0f99b1fc"></a>

### !Rocketeer (3) - Buildings, Any - 0F99B1FC

Owner: BadGuy1. Roster: 3 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: RktAttackBuildings, Any (0F99CDBC).

1. Scatter.
2. Seek/attack target category; configured argument 2.
3. Seek/attack target category; configured argument 1.

<a id="team-0ef6f43c"></a>

### !Tank Team (4) - Def,Power - 0EF6F43C

Owner: BadGuy1. Roster: 4 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackDef,Power (0EF6F1CC).

1. Seek/attack target category; configured argument 7.
2. Seek/attack target category; configured argument 9.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-0ef671fc"></a>

### !Spy (1) - Radar - 0EF671FC

Owner: BadGuy2. Roster: 1 × Spy (SPY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackRadar/Power (0EF6F90C).

1. Guard for interval; configured argument 80.
2. Seek/attack target category; configured argument 4.
3. Attack selected enemy-building category; configured argument 13.
4. Seek/attack target category; configured argument 9.
5. Attack selected enemy-building category; configured argument 15.
6. Seek/attack target category; configured argument 2.

<a id="team-0922b1fc"></a>

### !Harriers (5) - Refinery - 0922B1FC

Owner: BadGuy1. Roster: 5 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: HarrierRefineryAttack1 (0922DB7C).

1. Attack selected enemy-building category; configured argument 15.
2. Seek/attack target category; configured argument 2.
3. Seek/attack target category; configured argument 1.
4. Move to waypoint: waypoint 15 (cell 96, 139).
5. Delete team objects.

<a id="team-0ef7093c"></a>

### !GI Rush (10) - Buildings, Any - 0EF7093C

Owner: BadGuy1. Roster: 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: InfAttackBuildgs,Any (0EF706CC).

1. Guard for interval; configured argument 80.
2. Seek/attack target category; configured argument 2.
3. Seek/attack target category; configured argument 1.

<a id="team-0b2a580c"></a>

### !GI/IFV Combo - Inf, Buildings Any - 0B2A580C

Owner: BadGuy1. Roster: 1 × IFV (FV); 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Infantry, Buildings Any (0B2A559C).

1. Unload with continuation mode: transport and passengers continue.
2. Load transport.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-0de5f1dc"></a>

### !Engineer (3), GI (10) - Battle Lab - 0DE5F1DC

Owner: BadGuy1. Roster: 3 × Engineer (ENGINEER); 10 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBattleLab1 (0DE5EB4C).

1. Guard for interval; configured argument 80.
2. Attack selected enemy-building category; configured argument 9.
3. Attack selected enemy-building category; configured argument 10.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-0ef71dec"></a>

### !Snipers (3) - Inf - 0EF71DEC

Owner: BadGuy1. Roster: 3 × Sniper (SNIPE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Infantry, BaseDef (0EF71B7C).

1. Guard for interval; configured argument 80.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 1.

<a id="team-09f7e100"></a>

### !Rocketeer (5) - Vehicles - 09F7E100

Owner: BadGuy1. Roster: 5 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: VehicleAttack (0A6C1DE0).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 1.

<a id="team-0de5defc"></a>

### !Engineer (4), GIs (10) - Battle Lab - 0DE5DEFC

Owner: BadGuy1. Roster: 10 × GI (E1); 4 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBattleLab2 (0DE5DC8C).

1. Guard for interval; configured argument 80.
2. Attack selected enemy-building category; configured argument 15.
3. Attack selected enemy-building category; configured argument 10.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-0ef7124c"></a>

### !Tank Team (6) - Def, Battle Lab - 0EF7124C

Owner: BadGuy1. Roster: 6 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: BaseDef, Battle Lab (0EF6EB7C).

1. Seek/attack target category; configured argument 7.
2. Attack selected enemy-building category; configured argument 10.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0922f6fc"></a>

### !Rocketeer (5) - Vehicles, BatLab - 0922F6FC

Owner: BadGuy1. Roster: 5 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Vehicles, Battle Lab (0922F48C).

1. Seek/attack target category; configured argument 5.
2. Attack selected enemy-building category; configured argument 10.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0922f35c"></a>

### !Harriers (6) - Battle Lab - 0922F35C

Owner: BadGuy1. Roster: 6 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: HarrierAttackBattleLab (0925753C).

1. Attack selected enemy-building category; configured argument 10.
2. Seek/attack target category; configured argument 2.
3. Seek/attack target category; configured argument 1.

<a id="team-0b2a38ec"></a>

### !GI/IFV Combo - Inf, Battle Lab - 0B2A38EC

Owner: BadGuy1. Roster: 1 × IFV (FV); 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Infantry, Battle Lab (0B2A367C).

1. Unload with continuation mode: transport and passengers continue.
2. Load transport.
3. Seek/attack target category; configured argument 4.
4. Attack selected enemy-building category; configured argument 10.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-0ae23310"></a>

### SupplyTrucks - 0AE23310

Owner: Other1. Roster: 3 × Truck (loaded) (TRUCKB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: SuppliesToCamp (0955417C).

1. Move to waypoint: waypoint 52 (cell 84, 26).
2. Move to waypoint: waypoint 53 (cell 88, 31).
3. Move to waypoint: waypoint 54 (cell 90, 39).
4. Move to waypoint: waypoint 55 (cell 92, 40).
5. Move to waypoint: waypoint 56 (cell 94, 55).
6. Move to waypoint: waypoint 57 (cell 97, 56).
7. Move to waypoint: waypoint 58 (cell 101, 60).
8. Move to waypoint: waypoint 59 (cell 104, 67).
9. Move to waypoint: waypoint 60 (cell 116, 79).
10. Move to waypoint: waypoint 61 (cell 121, 82).
11. Move to waypoint: waypoint 62 (cell 124, 87).
12. Move to waypoint: waypoint 1 (cell 128, 91).
13. Move to waypoint: waypoint 0 (cell 137, 84).
14. Move to waypoint: waypoint 77 (cell 136, 69).
15. Scatter.
16. Set facing; configured argument 2.
17. Set local flag: local flag 2 (SuppliesArrived).

<a id="team-0e003efc"></a>

### TraitorousSoviets - 0E003EFC

Owner: BadGuy2. Roster: 6 × Technician (CTECH); 5 × GI (E1); 2 × Civilian (CIVSFM); 1 × Civilian (CIVSTM); 1 × Civilian (CIVSF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: TraitorInfantry (0E003C8C).

1. Scatter.
2. Move to waypoint: waypoint 3 (cell 106, 84).
3. Seek/attack target category; configured argument 3.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-0b135dec"></a>

### !Harriers (4) - Power - 0B135DEC

Owner: BadGuy1. Roster: 4 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: HarriersPower (095882DC).

1. Seek/attack target category; configured argument 9.
2. Seek/attack target category; configured argument 5.
3. Move to waypoint: waypoint 15 (cell 96, 139).
4. Delete team objects.

<a id="team-0c2af7dc"></a>

### !Solar (4) - Veh,Def,Fact,Any - 0C2AF7DC

Owner: BadGuy1. Roster: 4 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Vehicles,Def,Fact,Any (0EF74DBC).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 7.
3. Seek/attack target category; configured argument 6.
4. Seek/attack target category; configured argument 1.

<a id="team-0ef74c8c"></a>

### !Solar (6) - Fact,Ref,BattleLab - 0EF74C8C

Owner: BadGuy1. Roster: 6 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Fact,Ref,BattleLab (0EF74A1C).

1. Seek/attack target category; configured argument 6.
2. Attack selected enemy-building category; configured argument 15.
3. Attack selected enemy-building category; configured argument 10.
4. Seek/attack target category; configured argument 1.

<a id="team-0c48218c"></a>

### !Rocketeer (4) - Flak,BaseDef - 0C48218C

Owner: BadGuy1. Roster: 4 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackFlak,BaseDef,Vehicles,Any (0C4873DC).

1. Attack selected enemy-building category; configured argument 67.
2. Attack selected enemy-building category; configured argument 67.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-0ef7432c"></a>

### !Engineer/IFV 1 - 0EF7432C

Owner: BadGuy1. Roster: 1 × Engineer (ENGINEER); 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 2; Technology level: 0.

Ordered plan: EngineerWarFactory (0B2A132C).

1. Unload with continuation mode: transport and passengers continue.
2. Load transport.
3. Approach selected enemy-building category; configured argument 14.
4. Unload with continuation mode: passengers continue; transport leaves team.
5. Attack selected enemy-building category; configured argument 14.
6. Seek/attack target category; configured argument 6.
7. Seek/attack target category; configured argument 2.

<a id="team-0ef75c8c"></a>

### !Engineer/IFV 2 - 0EF75C8C

Owner: BadGuy1. Roster: 1 × Engineer (ENGINEER); 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 2; Technology level: 0.

Ordered plan: EngineerBarracks (0EF75A1C).

1. Unload with continuation mode: transport and passengers continue.
2. Load transport.
3. Approach selected enemy-building category; configured argument 11.
4. Unload with continuation mode: passengers continue; transport leaves team.
5. Attack selected enemy-building category; configured argument 11.
6. Seek/attack target category; configured argument 6.
7. Seek/attack target category; configured argument 2.

<a id="team-0b4352bc"></a>

### OutpostGuards - 0B4352BC

Owner: Player. Roster: 1 × Flak Trooper (FLAKT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GuardOutpost (0B4377DC).

1. Adopt object mission: area guard.

<a id="team-0ef7543c"></a>

### !Tank Team (2) - Def,Any - 0EF7543C

Owner: BadGuy1. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBaseDef,Any (0EF6CDBC).

1. Attack selected enemy-building category; configured argument 67.
2. Seek/attack target category; configured argument 7.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0ef751fc"></a>

### !Solar (3) - Veh,Def,Fact,Any - 0EF751FC

Owner: BadGuy1. Roster: 3 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Vehicles,Def,Fact,Any (0EF74DBC).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 7.
3. Seek/attack target category; configured argument 6.
4. Seek/attack target category; configured argument 1.

<a id="team-0c1c046c"></a>

### !Solar Hint (3) - Veh,Def,Fact,Any - 0C1C046C

Owner: BadGuy1. Roster: 3 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Vehicles,Def,Fact,Any (0EF74DBC).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 7.
3. Seek/attack target category; configured argument 6.
4. Seek/attack target category; configured argument 1.

<a id="team-0884b39c"></a>

### TownRefill - 0884B39C

Owner: Civilian1. Roster: 3 × Civilian (CIVSFM); 3 × Civilian (CIVSF); 3 × Civilian (CIVSTM)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BW.

Ordered plan: GoToTown (0884B12C).

1. Move to waypoint: waypoint 19 (cell 28, 91).
2. Scatter.
3. Adopt object mission: area guard.

<a id="team-0c24c7ec"></a>

### ConvertedSoviets2 - 0C24C7EC

Owner: BadGuy1. Roster: 3 × Civilian (CIVSFM); 3 × Civilian (CIVSF); 3 × Civilian (CIVSTM)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CA.

Ordered plan: AngryMobAttack (086C40AC).

1. Seek/attack target category; configured argument 4.
2. Seek/attack target category; configured argument 9.
3. Seek/attack target category; configured argument 1.

<a id="team-0f8ba20c"></a>

### !IFV (2) -  Veh,Any - 0F8BA20C

Owner: BadGuy1. Roster: 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackVeh,BuildAny,Any (0D55EDBC).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 2.
3. Seek/attack target category; configured argument 1.
