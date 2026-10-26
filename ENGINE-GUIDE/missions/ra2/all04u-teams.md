# Operation: Last Chance - team rosters and plans

[Trigger ledger](all04u.md) | [Mission overrides](all04u-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS01.MIX/all04u.map; each team/script ID identifies its section.

<a id="team-0a6a8b3c"></a>

### StartingForce1 - 0A6A8B3C

Owner: Player. Roster: 1 × Allied Construction Vehicle (AMCV); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: C.

Ordered plan: LC1EnterMap (03FCD2DC).

1. Move to waypoint: waypoint 0 (cell 142, 88).
2. Set facing; configured argument 6.

<a id="team-0b1b559c"></a>

### StartingDest1 - 0B1B559C

Owner: Player. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BV.

Ordered plan: Dest1EnterMap (0FB64B7C).

1. Move to waypoint: waypoint 16 (cell 138, 92).
2. Set facing; configured argument 6.
3. Guard for interval; configured argument 160.

<a id="team-0d592a4c"></a>

### StartingForce2 - 0D592A4C

Owner: PlayerAlt2. Roster: 1 × Grizzly Battle Tank (MTNK); 5 × GI (E1); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: C.

Ordered plan: LC2EnterMap (07FB8A1C).

1. Move to waypoint: waypoint 21 (cell 142, 90).
2. Set facing; configured argument 6.

<a id="team-0d59259c"></a>

### StartingForce3 - 0D59259C

Owner: PlayerAlt2. Roster: 1 × Grizzly Battle Tank (MTNK); 5 × GI (E1); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: C.

Ordered plan: LC3EnterMap (07FB86AC).

1. Move to waypoint: waypoint 22 (cell 142, 92).
2. Set facing; configured argument 6.

<a id="team-0c51ec8c"></a>

### Patrol1 - 0C51EC8C

Owner: Russian1. Roster: 3 × Conscript (E2); 2 × Tesla Trooper (SHK); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: Patrol1 (0A6E13BC).

1. Move to waypoint: waypoint 78 (cell 25, 112).
2. Move to waypoint: waypoint 79 (cell 53, 112).
3. Guard for interval; configured argument 50.
4. Move to waypoint: waypoint 80 (cell 53, 97).
5. Move to waypoint: waypoint 81 (cell 36, 97).
6. Move to waypoint: waypoint 82 (cell 36, 125).
7. Move to waypoint: waypoint 83 (cell 25, 125).
8. Jump to script line; configured argument 1.

<a id="team-0c51e7dc"></a>

### Patrol2 - 0C51E7DC

Owner: Russian1. Roster: 3 × Conscript (E2); 2 × Tesla Trooper (SHK); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: G.

Ordered plan: Patrol2 (0A6EF21C).

1. Move to waypoint: waypoint 84 (cell 77, 97).
2. Guard for interval; configured argument 30.
3. Move to waypoint: waypoint 80 (cell 53, 97).
4. Move to waypoint: waypoint 85 (cell 53, 138).
5. Set facing; configured argument 2.
6. Guard for interval; configured argument 30.
7. Move to waypoint: waypoint 86 (cell 36, 138).
8. Move to waypoint: waypoint 81 (cell 36, 97).
9. Jump to script line; configured argument 3.

<a id="team-0c51e43c"></a>

### Patrol3 - 0C51E43C

Owner: Russian1. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: H.

Ordered plan: Patrol3 (0993412C).

1. Move to waypoint: waypoint 78 (cell 25, 112).
2. Move to waypoint: waypoint 79 (cell 53, 112).
3. Move to waypoint: waypoint 80 (cell 53, 97).
4. Move to waypoint: waypoint 84 (cell 77, 97).
5. Move to waypoint: waypoint 87 (cell 77, 138).
6. Move to waypoint: waypoint 86 (cell 36, 138).
7. Move to waypoint: waypoint 82 (cell 36, 125).
8. Move to waypoint: waypoint 83 (cell 25, 125).
9. Jump to script line; configured argument 1.

<a id="team-095657dc"></a>

### BaseDef1 - 095657DC

Owner: Russian1. Roster: 3 × Conscript (E2); 1 × Tesla Trooper (SHK); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 40; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BA.

Ordered plan: GuardBase (09056DBC).

1. Adopt object mission: area guard.

<a id="team-0956532c"></a>

### BaseDef2 - 0956532C

Owner: Russian1. Roster: 3 × Conscript (E2); 1 × Tesla Trooper (SHK); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 40; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BB.

Ordered plan: GuardBase (09056DBC).

1. Adopt object mission: area guard.

<a id="team-095651fc"></a>

### BaseDef3 - 095651FC

Owner: Russian1. Roster: 2 × Rhino Heavy Tank (HTNK); 2 × Conscript (E2); 2 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 40; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: GuardBase (09056DBC).

1. Adopt object mission: area guard.

<a id="team-0c6a76dc"></a>

### EngineerBridge - 0C6A76DC

Owner: Russian1. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 40; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: RepairBridge (0995370C).

1. Attack selected enemy-building category; configured argument 131102.

<a id="team-0c6a733c"></a>

### !Attack01 - 0C6A733C

Owner: Russian1. Roster: 6 × Conscript (E2); 4 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackRefine,Harv,Any (07FC64FC).

1. Attack selected enemy-building category; configured argument 1.
2. Report team success.
3. Seek/attack target category; configured argument 3.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-087f632c"></a>

### !Attack02 - 087F632C

Owner: Russian1. Roster: 3 × Flak Track (HTK); 6 × Conscript (E2); 4 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackInf,Any (07FC78AC).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 1.

<a id="team-093b990c"></a>

### !Attack03 - 093B990C

Owner: Russian1. Roster: 4 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBaseDef,Veh,ConYard (07FCFDBC).

1. Seek/attack target category; configured argument 7.
2. Report team success.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 5.
5. Attack selected enemy-building category; configured argument 131074.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-0c6a821c"></a>

### !Attack04 - 0C6A821C

Owner: Russian1. Roster: 2 × V3 Launcher (V3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackPower,BaseDef,Fact,Any (0C6A9DBC).

1. Seek/attack target category; configured argument 9.
2. Report team success.
3. Seek/attack target category; configured argument 9.
4. Seek/attack target category; configured argument 7.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-0800769c"></a>

### !V3Escort - 0800769C

Owner: Russian1. Roster: 4 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: GuardV3s (0800514C).

1. Follow friendly objects.
2. Report team success.

<a id="team-0c1c0b7c"></a>

### !SubAttack - 0C1C0B7C

Owner: Russian1. Roster: 2 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackNavyYard,Veh,Any (0800030C).

1. Attack selected enemy-building category; configured argument 23.
2. Report team success.
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 1.

<a id="team-0b21321c"></a>

### !Attack05 - 0B21321C

Owner: Russian1. Roster: 7 × Conscript (E2); 2 × V3 Launcher (V3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackPower,BaseDef,Fact,Any (0C6A9DBC).

1. Seek/attack target category; configured argument 9.
2. Report team success.
3. Seek/attack target category; configured argument 9.
4. Seek/attack target category; configured argument 7.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-0b215dec"></a>

### !Attack06 - 0B215DEC

Owner: Russian1. Roster: 4 × Rhino Heavy Tank (HTNK); 2 × V3 Launcher (V3); 2 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBaseDef,Fact,Any (07DD071C).

1. Seek/attack target category; configured argument 7.
2. Report team success.
3. Seek/attack target category; configured argument 6.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 1.

<a id="team-080070bc"></a>

### !Attack07 - 080070BC

Owner: Russian1. Roster: 4 × Rhino Heavy Tank (HTNK); 2 × V3 Launcher (V3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBaseDef,Any (08005DBC).

1. Seek/attack target category; configured argument 7.
2. Report team success.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-087f2a4c"></a>

### !DestroyAirport - 087F2A4C

Owner: Russian1. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: DestroyAirport (087F4DBC).

1. Gather near own base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131142.
3. Attack selected enemy-building category; configured argument 131141.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-09868efc"></a>

### Garrison1 - 09868EFC

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY18 (09868ABC).

1. Attack selected enemy-building category; configured argument 131241.

<a id="team-07f3b68c"></a>

### Garrison2 - 07F3B68C

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY11 (07F3CDBC).

1. Attack selected enemy-building category; configured argument 131234.

<a id="team-098685ec"></a>

### Garrison3 - 098685EC

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY23 (0986837C).

1. Attack selected enemy-building category; configured argument 131261.

<a id="team-0b1be6ac"></a>

### StartingDest2 - 0B1BE6AC

Owner: Player. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BW.

Ordered plan: Dest2EnterMap (0FBDEB4C).

1. Move to waypoint: waypoint 1 (cell 138, 90).
2. Set facing; configured argument 6.
3. Guard for interval; configured argument 160.

<a id="team-0b1be30c"></a>

### StartingDest3 - 0B1BE30C

Owner: Player. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BX.

Ordered plan: Dest3EnterMap (0FBDE7AC).

1. Move to waypoint: waypoint 17 (cell 138, 88).
2. Set facing; configured argument 6.
3. Guard for interval; configured argument 160.

<a id="team-0b1bdc8c"></a>

### StartingDest4 - 0B1BDC8C

Owner: Player. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BY.

Ordered plan: Dest4EnterMap (0FBDE40C).

1. Move to waypoint: waypoint 19 (cell 138, 86).
2. Set facing; configured argument 6.
3. Guard for interval; configured argument 160.

<a id="team-0b1bd8ec"></a>

### StartingDest5 - 0B1BD8EC

Owner: Player. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BZ.

Ordered plan: Dest5EnterMap (0FBDADBC).

1. Move to waypoint: waypoint 20 (cell 138, 84).
2. Set facing; configured argument 6.
3. Guard for interval; configured argument 160.

<a id="team-094b207c"></a>

### Garrison4 - 094B207C

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY10 (094B55BC).

1. Attack selected enemy-building category; configured argument 131233.

<a id="team-094b53ac"></a>

### Garrison5 - 094B53AC

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY26 (094B683C).

1. Attack selected enemy-building category; configured argument 131264.

<a id="team-094b663c"></a>

### Garrison6 - 094B663C

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrChicagoBrick(S) (094B36FC).

1. Attack selected enemy-building category; configured argument 131275.

<a id="team-094b59ec"></a>

### Garrison7 - 094B59EC

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrAssociatesCtr (094B7DBC).

1. Attack selected enemy-building category; configured argument 131269.

<a id="team-0c1cc67c"></a>

### EnemySubs - 0C1CC67C

Owner: Russian1. Roster: 1 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AA.

Ordered plan: SubHunt (0B082DBC).

1. Attack-move toward waypoint: waypoint 8 (cell 117, 111).
2. Guard for interval; configured argument 20.
3. Adopt object mission: hunt.

<a id="team-0949d97c"></a>

### Garrison8 - 0949D97C

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY22 (0949D70C).

1. Attack selected enemy-building category; configured argument 131260.

<a id="team-07f3887c"></a>

### !Attack08 - 07F3887C

Owner: Russian1. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackAnything (07F3D8FC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 1.
3. Report team success.

<a id="team-07f3d58c"></a>

### !Attack09 - 07F3D58C

Owner: Russian1. Roster: 2 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackAnything (07F3D8FC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 1.
3. Report team success.

<a id="team-0d59946c"></a>

### StartingForce4 - 0D59946C

Owner: PlayerAlt2. Roster: 1 × Grizzly Battle Tank (MTNK); 5 × GI (E1); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: C.

Ordered plan: LC4EnterMap (0B08F18C).

1. Move to waypoint: waypoint 46 (cell 142, 86).
2. Set facing; configured argument 6.

<a id="team-0b1be1dc"></a>

### StartingDest6 - 0B1BE1DC

Owner: Player. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BU.

Ordered plan: Dest6EnterMap (0FBDD6AC).

1. Move to waypoint: waypoint 47 (cell 138, 94).
2. Set facing; configured argument 6.
3. Guard for interval; configured argument 160.

<a id="team-0c1a3c8c"></a>

### Reinforce1-Trans - 0C1A3C8C

Owner: Player. Roster: 1 × Amphibious Transport (LCRF); 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforce1 (0A3D4A1C).

1. Move to waypoint: waypoint 1 (cell 138, 90).
2. Move to waypoint: waypoint 56 (cell 90, 127).
3. Set facing; configured argument 6.

<a id="team-0c1a37dc"></a>

### Reinforce2-Trans - 0C1A37DC

Owner: Player. Roster: 1 × Grizzly Battle Tank (MTNK); 5 × GI (E1); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforce2 (09B5043C).

1. Move to waypoint: waypoint 16 (cell 138, 92).
2. Move to waypoint: waypoint 57 (cell 90, 129).
3. Set facing; configured argument 6.

<a id="team-0c1a343c"></a>

### Reinforce3-Trans - 0C1A343C

Owner: Player. Roster: 1 × Amphibious Transport (LCRF); 4 × GI (E1); 1 × Grizzly Battle Tank (MTNK); 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforce3 (09B54C8C).

1. Move to waypoint: waypoint 47 (cell 138, 94).
2. Move to waypoint: waypoint 58 (cell 90, 131).
3. Set facing; configured argument 6.

<a id="team-0c1a4c8c"></a>

### Reinforce4-Trans - 0C1A4C8C

Owner: Player. Roster: 1 × Grizzly Battle Tank (MTNK); 5 × GI (E1); 1 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforce4 (0A3D3B7C).

1. Move to waypoint: waypoint 22 (cell 142, 92).
2. Move to waypoint: waypoint 59 (cell 90, 133).
3. Set facing; configured argument 6.

<a id="team-0c1a48ec"></a>

### MonkeyForce5 - 0C1A48EC

Owner: Player. Roster: 5 × Monkey (JOSH)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GuardBase (09056DBC).

1. Adopt object mission: area guard.

<a id="team-086abbfc"></a>

### SubReinforcments - 086ABBFC

Owner: Russian1. Roster: 1 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: E.

Ordered plan: SubReinforce (086AB98C).

1. Move to waypoint: waypoint 26 (cell 140, 48).
2. Adopt object mission: area guard.

<a id="team-086068ec"></a>

### V3HintTeam - 086068EC

Owner: Russian1. Roster: 1 × V3 Launcher (V3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: GuardBase (09056DBC).

1. Adopt object mission: area guard.

<a id="team-0f99246c"></a>

### !Attack10 - 0F99246C

Owner: Russian1. Roster: 1 × Rhino Heavy Tank (HTNK); 1 × V3 Launcher (V3); 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBaseDef,Fact,Any (07DD071C).

1. Seek/attack target category; configured argument 7.
2. Report team success.
3. Seek/attack target category; configured argument 6.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 1.

<a id="team-0ba2739c"></a>

### !SubAttack(Easy) - 0BA2739C

Owner: Russian1. Roster: 1 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackNavyYard,Veh,Any (0800030C).

1. Attack selected enemy-building category; configured argument 23.
2. Report team success.
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 1.

<a id="team-0ba2712c"></a>

### !Engineers4SovConYard - 0BA2712C

Owner: Russian1. Roster: 1 × Engineer (SENGINEER); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 15; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: RetakeConYard (0428ABBC).

1. Move to waypoint: waypoint 78 (cell 25, 112).
2. Load transport.
3. Approach selected enemy-building category; configured argument 131097.
4. Unload with continuation mode: passengers continue; transport leaves team.
5. Attack selected enemy-building category; configured argument 131097.

<a id="team-086d29bc"></a>

### GarrNY18Easy - 086D29BC

Owner: Russian1. Roster: 2 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY18 (09868ABC).

1. Attack selected enemy-building category; configured argument 131241.

<a id="team-08762efc"></a>

### GarrNY18Medium - 08762EFC

Owner: Russian1. Roster: 5 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY18 (09868ABC).

1. Attack selected enemy-building category; configured argument 131241.

<a id="team-086e876c"></a>

### GarrNY18Hard - 086E876C

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY18 (09868ABC).

1. Attack selected enemy-building category; configured argument 131241.

<a id="team-0d57225c"></a>

### Reinforce5-Dest - 0D57225C

Owner: PlayerAlt2. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforce1 (0A3D4A1C).

1. Move to waypoint: waypoint 1 (cell 138, 90).
2. Move to waypoint: waypoint 56 (cell 90, 127).
3. Set facing; configured argument 6.

<a id="team-0d57212c"></a>

### Reinforce6-Dest - 0D57212C

Owner: PlayerAlt2. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforce2 (09B5043C).

1. Move to waypoint: waypoint 16 (cell 138, 92).
2. Move to waypoint: waypoint 57 (cell 90, 129).
3. Set facing; configured argument 6.

<a id="team-0d571efc"></a>

### Reinforce7-Dest - 0D571EFC

Owner: PlayerAlt2. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforce3 (09B54C8C).

1. Move to waypoint: waypoint 47 (cell 138, 94).
2. Move to waypoint: waypoint 58 (cell 90, 131).
3. Set facing; configured argument 6.

<a id="team-0d571dcc"></a>

### Reinforce8-Dest - 0D571DCC

Owner: PlayerAlt2. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforce4 (0A3D3B7C).

1. Move to waypoint: waypoint 22 (cell 142, 92).
2. Move to waypoint: waypoint 59 (cell 90, 133).
3. Set facing; configured argument 6.

<a id="team-0d571c9c"></a>

### Reinforce9-Rocketeers - 0D571C9C

Owner: PlayerAlt2. Roster: 10 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AZ.

Ordered plan: ReinforceRocketeers (0A147DBC).

1. Move to waypoint: waypoint 28 (cell 87, 53).
2. Adopt object mission: guard.

<a id="team-0ba2932c"></a>

### ShockBridgeGuards - 0BA2932C

Owner: Russian1. Roster: 5 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BI.

Ordered plan: MoveToBridge (0A56CDBC).

1. Move to waypoint: waypoint 55 (cell 53, 90).
2. Seek/attack target category; configured argument 5.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 1.

<a id="team-0446f20c"></a>

### CopCar1 - 0446F20C

Owner: Cops. Roster: 1 × Police Car (COP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BJ.

Ordered plan: Cop1 (0446C27C).

1. Move to waypoint: waypoint 62 (cell 62, 126).
2. Set local flag: local flag 4 (CopsArrived).
3. Seek/attack target category; configured argument 4.

<a id="team-08cd6efc"></a>

### CopKillers - 08CD6EFC

Owner: Russian3. Roster: 3 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BK.

Ordered plan: KillCopCars (0DDC1A1C).

1. Seek/attack target category; configured argument 5.
2. Adopt object mission: guard.

<a id="team-0bc2a80c"></a>

### TankAttackWSO - 0BC2A80C

Owner: Russian1. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BI.

Ordered plan: AttackWallStrOffice (0BC2A59C).

1. Move to waypoint: waypoint 80 (cell 53, 97).
2. Move to waypoint: waypoint 63 (cell 54, 123).
3. Attack selected enemy-building category; configured argument 131226.

<a id="team-0bc2a11c"></a>

### TankAttackSAO - 0BC2A11C

Owner: Russian1. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BI.

Ordered plan: AttackSanAntOffice (0BC2CDBC).

1. Move to waypoint: waypoint 80 (cell 53, 97).
2. Move to waypoint: waypoint 64 (cell 54, 120).
3. Attack selected enemy-building category; configured argument 131265.

<a id="team-0bc2ca5c"></a>

### TankAttackNY23 - 0BC2CA5C

Owner: Russian1. Roster: 1 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BI.

Ordered plan: TankAttackNY23 (0BC2F73C).

1. Move to waypoint: waypoint 80 (cell 53, 97).
2. Move to waypoint: waypoint 64 (cell 54, 120).
3. Attack selected enemy-building category; configured argument 131261.

<a id="team-0bc2f4fc"></a>

### TankAttackChigoBrick2 - 0BC2F4FC

Owner: Russian1. Roster: 1 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BI.

Ordered plan: AttackChigoBrickVar2 (0BC2BDBC).

1. Move to waypoint: waypoint 80 (cell 53, 97).
2. Move to waypoint: waypoint 65 (cell 54, 116).
3. Attack selected enemy-building category; configured argument 131276.

<a id="team-0867773c"></a>

### HackCivilianForEnding - 0867773C

Owner: Other2. Roster: 1 × Civilian (CIVBFM)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: BeAsleep (0867D49C).

1. Adopt object mission: sleep.

<a id="team-08cd76ac"></a>

### CopCar2 - 08CD76AC

Owner: Cops. Roster: 1 × Police Car (COP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BJ.

Ordered plan: Cop2 (08CD743C).

1. Move to waypoint: waypoint 62 (cell 62, 126).
2. Seek/attack target category; configured argument 4.

<a id="team-08cd730c"></a>

### CopCar3 - 08CD730C

Owner: Cops. Roster: 1 × Police Car (COP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BJ.

Ordered plan: Cop3 (08CD709C).

1. Move to waypoint: waypoint 62 (cell 62, 126).
2. Seek/attack target category; configured argument 4.

<a id="team-08821d2c"></a>

### SpawnedSubs - 08821D2C

Owner: Russian1. Roster: 1 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: SpawnAndGuard (08821ABC).

1. Set facing; configured argument 6.
2. Adopt object mission: area guard.

<a id="team-0d57e67c"></a>

### StartingRocket(R) - EASY - 0D57E67C

Owner: PlayerAlt2. Roster: 3 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: StartRktRightEasy (0D4E0A1C).

1. Move to waypoint: waypoint 19 (cell 138, 86).
2. Guard for interval; configured argument 10.
3. Move to waypoint: waypoint 94 (cell 124, 102).
4. Attack selected enemy-building category; configured argument 131136.

<a id="team-044699cc"></a>

### StartingRocket(L) - EASY - 044699CC

Owner: PlayerAlt2. Roster: 3 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: StartRktLeftEasy (0446975C).

1. Move to waypoint: waypoint 16 (cell 138, 92).
2. Guard for interval; configured argument 10.
3. Move to waypoint: waypoint 95 (cell 124, 114).
4. Move to waypoint: waypoint 24 (cell 118, 116).
5. Attack selected enemy-building category; configured argument 131136.

<a id="team-0d57dc8c"></a>

### StartingRocket(L) - MED - 0D57DC8C

Owner: PlayerAlt2. Roster: 2 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: StartRktLeftMed (087D87CC).

1. Move to waypoint: waypoint 16 (cell 138, 92).
2. Move to waypoint: waypoint 95 (cell 124, 114).

<a id="team-0d57d7dc"></a>

### StartingRocket(R) - MED - 0D57D7DC

Owner: PlayerAlt2. Roster: 2 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: StartRktRightMed (087DFDBC).

1. Move to waypoint: waypoint 19 (cell 138, 86).
2. Move to waypoint: waypoint 94 (cell 124, 102).

<a id="team-0d57d43c"></a>

### StartingRocket - HARD - 0D57D43C

Owner: PlayerAlt2. Roster: 2 × Rocketeer (JUMPJET)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: StartRktHard (087DBDBC).

1. Move to waypoint: waypoint 17 (cell 138, 88).

<a id="team-0b1c230c"></a>

### PlayerMCV - 0B1C230C

Owner: Player. Roster: 1 × Allied Construction Vehicle (AMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CK.

Ordered plan: MCVUnloaded (0E323B4C).

1. Set local flag: local flag 5 (mcvUnloaded).
2. Guard for interval; configured argument 5.
