# Operation: Hail to the Chief - team rosters and plans

[Trigger ledger](all03u.md) | [Mission overrides](all03u-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS01.MIX/all03u.map; each team/script ID identifies its section.

<a id="team-0b76ea4c"></a>

### ArmedHordes1 - 0B76EA4C

Owner: CivilianArmy. Roster: 5 × Technician (CTECH); 2 × Conscript (E2); 1 × Civilian (CIVC); 1 × Civilian (CIVSFM); 1 × Civilian (CIVSTM); 2 × Civilian (CIVA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: CA.

Ordered plan: Civs1AttackPlayer (0A14932C).

1. Move to waypoint: waypoint 55 (cell 125, 134).
2. Seek/attack target category; configured argument 1.

<a id="team-0b76e59c"></a>

### ArmedHordes2 - 0B76E59C

Owner: CivilianArmy. Roster: 5 × Technician (CTECH); 2 × Conscript (E2); 1 × Civilian (CIVC); 1 × Civilian (CIVSFM); 1 × Civilian (CIVSTM); 2 × Civilian (CIVA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: CB.

Ordered plan: Civs2AttackPlayer (0A1B0B7C).

1. Move to waypoint: waypoint 54 (cell 153, 101).
2. Seek/attack target category; configured argument 1.

<a id="team-0a148dcc"></a>

### ArmedHordes3 - 0A148DCC

Owner: CivilianArmy. Roster: 5 × Technician (CTECH); 2 × Conscript (E2); 1 × Civilian (CIVC); 1 × Civilian (CIVSFM); 1 × Civilian (CIVSTM); 2 × Civilian (CIVA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: CC.

Ordered plan: Civs3AttackPlayer (0A1BA57C).

1. Move to waypoint: waypoint 56 (cell 44, 103).
2. Seek/attack target category; configured argument 1.

<a id="team-0c4e57bc"></a>

### *President - 0C4E57BC

Owner: Other1. Roster: 1 × President (PRES)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: ExitWhiteHouse (0C4E554C).

1. Move to waypoint: waypoint 27 (cell 76, 19).
2. Set facing; configured argument 4.
3. Adopt object mission: guard.

<a id="team-0ecab6ac"></a>

### *PresidentialHelicopter - 0ECAB6AC

Owner: Other1. Roster: 1 × NightHawk Transport (SHAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: HelicopterLand (0ECAB43C).

1. Move to waypoint: waypoint 7 (cell 75, 19).
2. Adopt object mission: stop.

<a id="team-0b2a832c"></a>

### EngineerBridgeRepair - 0B2A832C

Owner: Russian1. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 40; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: RepairBridge (0B2B7DBC).

1. Move to waypoint: waypoint 53 (cell 96, 108).
2. Attack selected enemy-building category; configured argument 131102.

<a id="team-0b63732c"></a>

### Hunters(Shock&Flak) - 0B63732C

Owner: Russian2. Roster: 6 × Tesla Trooper (SHK); 2 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackPartyHunt (0B72367C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 1.

<a id="team-0b2b743c"></a>

### !Shock-TanksVS AirCommand - 0B2B743C

Owner: Russian1. Roster: 3 × Tesla Trooper (SHK); 4 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackAirCom,Power (0B2B71CC).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131177.
3. Report team success.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 1.

<a id="team-09f826cc"></a>

### !RhinoVSAny, BaseDef - 09F826CC

Owner: Russian1. Roster: 3 × Rhino Heavy Tank (HTNK); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Any,BaseDef (0988E6CC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 2.
3. Report team success.
4. Seek/attack target category; configured argument 7.
5. Seek/attack target category; configured argument 1.

<a id="team-0b2b693c"></a>

### !Shock-TanksVS Barracks - 0B2B693C

Owner: Russian1. Roster: 2 × Rhino Heavy Tank (HTNK); 4 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBarracks,Fact,Any (0B2B66CC).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131075.
3. Report team success.
4. Seek/attack target category; configured argument 6.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-0b2b648c"></a>

### !SmallShockAttack - 0B2B648C

Owner: Russian1. Roster: 3 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Shock vs Anything (0B2B621C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 1.
3. Report team success.

<a id="team-0a950b7c"></a>

### !BaseDef1 - 0A950B7C

Owner: Russian1. Roster: 3 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Base (0965C9DC).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a9506cc"></a>

### !BaseDef2 - 0A9506CC

Owner: Russian1. Roster: 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Base (0965C9DC).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a95048c"></a>

### !BaseDef3 - 0A95048C

Owner: Russian1. Roster: 1 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Base (0965C9DC).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0b0c380c"></a>

### !TanksVSBase - 0B0C380C

Owner: Russian1. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackBaseDef,ConYard (0C4D648C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 36 (cell 109, 102).
3. Move to waypoint: waypoint 45 (cell 109, 121).
4. Seek/attack target category; configured argument 7.
5. Report team success.
6. Attack selected enemy-building category; configured argument 131074.
7. Seek/attack target category; configured argument 2.
8. Seek/attack target category; configured argument 1.

<a id="team-0b0c335c"></a>

### !FlakAttack1 - 0B0C335C

Owner: Russian1. Roster: 3 × Conscript (E2); 2 × Tesla Trooper (SHK); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackAnything(Trans) (0B2B4B7C).

1. Gather near own base; configured argument 0.
2. Load transport.
3. Gather near enemy base; configured argument 0.
4. Approach selected enemy-building category; configured argument 131074.
5. Report team success.
6. Unload with continuation mode: transport and passengers continue.
7. Seek/attack target category; configured argument 1.

<a id="team-09f8fefc"></a>

### !TankAttack(SML) - 09F8FEFC

Owner: Russian1. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Garr, Any (0B2B46CC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 10.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-095f8a4c"></a>

### GarrisonWash10 - 095F8A4C

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash10 (095F87DC).

1. Attack selected enemy-building category; configured argument 131188.

<a id="team-0b740efc"></a>

### GarrisonWash11 - 0B740EFC

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash11 (0B761DBC).

1. Attack selected enemy-building category; configured argument 131184.

<a id="team-0b7618dc"></a>

### GarrisonWash03 - 0B7618DC

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash3 (0B76166C).

1. Attack selected enemy-building category; configured argument 131182.

<a id="team-0b7614bc"></a>

### GarrisonWash04 - 0B7614BC

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash4 (0B76099C).

1. Attack selected enemy-building category; configured argument 131181.

<a id="team-0b76074c"></a>

### GarrisonWash05 - 0B76074C

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash5 (0B76030C).

1. Attack selected enemy-building category; configured argument 131180.

<a id="team-0b76019c"></a>

### GarrisonWash07 - 0B76019C

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash7 (0B76DC6C).

1. Attack selected enemy-building category; configured argument 131183.

<a id="team-0b76d96c"></a>

### GarrisonWash08 - 0B76D96C

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash8 (0B76D6FC).

1. Attack selected enemy-building category; configured argument 131192.

<a id="team-0b76d4fc"></a>

### GarrisonWash09 - 0B76D4FC

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWash9 (0B76D28C).

1. Attack selected enemy-building category; configured argument 131187.

<a id="team-0b77c6bc"></a>

### GarrisonNY26 - 0B77C6BC

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrNY26 (0B77B8DC).

1. Attack selected enemy-building category; configured argument 131264.

<a id="team-0b77ebfc"></a>

### GarrisonMiamiHotel3 - 0B77EBFC

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrMiamiHotel3 (0B7789FC).

1. Attack selected enemy-building category; configured argument 131270.

<a id="team-0bf3e7bc"></a>

### GarrisonWashMon - 0BF3E7BC

Owner: Russian1. Roster: 1 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrWashMon (07F037BC).

1. Attack selected enemy-building category; configured argument 131185.

<a id="team-07f06bdc"></a>

### GarrisonLincolnMem - 07F06BDC

Owner: Russian1. Roster: 7 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GarrLincolnMem (07F0696C).

1. Attack selected enemy-building category; configured argument 131246.

<a id="team-0b88567c"></a>

### *PresDuganAndHeli - 0B88567C

Owner: Other1. Roster: 1 × NightHawk Transport (SHAD); 1 × President (PRES); 2 × Secret Service (SSRV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 50; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: W.

Ordered plan: BoardHeli (07E6F42C).

1. Load transport.

<a id="team-0b0ce69c"></a>

### TanksVSHosp&Garr - 0B0CE69C

Owner: Russian1. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackHosp-Garrisoned (0C4D0C8C).

1. Move to waypoint: waypoint 36 (cell 109, 102).
2. Move to waypoint: waypoint 45 (cell 109, 121).
3. Seek/attack target category; configured argument 11.
4. Report team success.
5. Seek/attack target category; configured argument 10.
6. Seek/attack target category; configured argument 1.

<a id="team-0a9558ec"></a>

### !BaseDef4 - 0A9558EC

Owner: Russian1. Roster: 5 × Flak Trooper (FLAKT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Base (0965C9DC).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0b0cbdec"></a>

### AirDropSquad1 - 0B0CBDEC

Owner: Russian1. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: AirDropAttackAny (0B7FF7BC).

1. Seek/attack target category; configured argument 1.

<a id="team-09f8b6cc"></a>

### !TankAttack(MED) - 09F8B6CC

Owner: Russian1. Roster: 4 × Rhino Heavy Tank (HTNK); 3 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 40; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackAny (0829239C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 2.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-09f8defc"></a>

### !TankAttack(LRG) - 09F8DEFC

Owner: Russian1. Roster: 6 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 50; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackAny (0829239C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 2.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-09f8adec"></a>

### !Engineer/FlakAttack - 09F8ADEC

Owner: Russian1. Roster: 3 × Engineer (ENGINEER); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: EngAttackPower,Fact,Con,Any (09F8AB7C).

1. Gather near own base; configured argument 0.
2. Load transport.
3. Move to waypoint: waypoint 36 (cell 109, 102).
4. Move to waypoint: waypoint 45 (cell 109, 121).
5. Approach selected enemy-building category; configured argument 2.
6. Report team success.
7. Unload with continuation mode: passengers continue; transport leaves team.
8. Seek/attack target category; configured argument 9.
9. Attack selected enemy-building category; configured argument 7.
10. Attack selected enemy-building category; configured argument 2.
11. Seek/attack target category; configured argument 2.

<a id="team-08206efc"></a>

### !FlakAttack2 - 08206EFC

Owner: Russian1. Roster: 4 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: FlakAttackInfantry (08206B7C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.

<a id="team-09f8a30c"></a>

### !AttackWash7Garr - 09F8A30C

Owner: Russian1. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: AttackWash7Garr (0B318C8C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 131183.
4. Report team success.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 5.
7. Seek/attack target category; configured argument 1.

<a id="team-0c0b56ac"></a>

### AirDropSquad2 - 0C0B56AC

Owner: Russian1. Roster: 3 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: ShockAttackBaseDef (0C0B543C).

1. Move to waypoint: waypoint 25 (cell 104, 137).
2. Seek/attack target category; configured argument 5.
3. Seek/attack target category; configured argument 1.

<a id="team-09dddc3c"></a>

### AirDropSquad3 - 09DDDC3C

Owner: Russian1. Roster: 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: AirDropAttackAny (0B7FF7BC).

1. Seek/attack target category; configured argument 1.

<a id="team-0b90ba4c"></a>

### ReinforcementsWest1 - 0B90BA4C

Owner: Player. Roster: 2 × Grizzly Battle Tank (MTNK); 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AV.

Ordered plan: DriveOnWest (0B90B32C).

1. Move to waypoint: waypoint 48 (cell 47, 90).
2. Adopt object mission: area guard.

<a id="team-0b90b59c"></a>

### ReinforcementsEast - 0B90B59C

Owner: Player. Roster: 4 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AU.

Ordered plan: DriveOnEast (0B90B7DC).

1. Move to waypoint: waypoint 49 (cell 147, 90).
2. Adopt object mission: area guard.

<a id="team-0c4ea7dc"></a>

### *SecretService1 - 0C4EA7DC

Owner: Other1. Roster: 1 × Secret Service (SSRV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: MoveToBM (0C4EA56C).

1. Move to waypoint: waypoint 27 (cell 76, 19).
2. Set facing; configured argument 4.
3. Adopt object mission: guard.

<a id="team-0c4ea32c"></a>

### *SecretService2 - 0C4EA32C

Owner: Other1. Roster: 1 × Secret Service (SSRV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: MoveToBL (0C4E9DBC).

1. Move to waypoint: waypoint 27 (cell 76, 19).
2. Set facing; configured argument 4.
3. Adopt object mission: guard.

<a id="team-0a2c624c"></a>

### !EngineerAttack - 0A2C624C

Owner: Russian2. Roster: 2 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: EngineersAttack (085CFDBC).

1. Seek/attack target category; configured argument 9.
2. Report team success.
3. Seek/attack target category; configured argument 6.
4. Seek/attack target category; configured argument 2.

<a id="team-087606ac"></a>

### ReinforcementsWest2 - 087606AC

Owner: Player. Roster: 1 × Engineer (ENGINEER); 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AV.

Ordered plan: DriveOnWestTransport (0C18E1BC).

1. Move to waypoint: waypoint 44 (cell 31, 90).
2. Load transport.
3. Move to waypoint: waypoint 48 (cell 47, 90).
4. Adopt object mission: area guard.

<a id="team-087e855c"></a>

### !R2BaseDef1 - 087E855C

Owner: Russian2. Roster: 1 × Attack Dog (DOG); 2 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 20; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Base (0965C9DC).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-087ede9c"></a>

### !R2BaseDef2 - 087EDE9C

Owner: Russian2. Roster: 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Base (0965C9DC).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0c33adcc"></a>

### ShockAttack-Intro - 0C33ADCC

Owner: Russian2. Roster: 2 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: ShockIntro (086BC2CC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Seek/attack target category; configured argument 9.
4. Seek/attack target category; configured argument 1.

<a id="team-0862a03c"></a>

### !TankAttack(XTRA-SML) - 0862A03C

Owner: Russian2. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Russ2-AttackBaseDef,Any (0862BDBC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-08633b7c"></a>

### !ShockAttack - 08633B7C

Owner: Russian2. Roster: 3 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Russ2-AttackBaseDef,Any (0862BDBC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.

<a id="team-0863390c"></a>

### !ConAttack - 0863390C

Owner: Russian2. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: R2ConAttack (0863369C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 36 (cell 109, 102).
3. Move to waypoint: waypoint 45 (cell 109, 121).
4. Seek/attack target category; configured argument 1.

<a id="team-086330cc"></a>

### !DogAttack - 086330CC

Owner: Russian2. Roster: 3 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: DogAttack (08634DBC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Adopt object mission: hunt.
4. Seek/attack target category; configured argument 4.

<a id="team-0c15d3dc"></a>

### Hint(IFV/Engineer) - 0C15D3DC

Owner: Player. Roster: 1 × Engineer (ENGINEER); 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BQ.

Ordered plan: Hint(Engineer/IFV) (088868EC).

1. Load transport.
2. Attack waypoint: waypoint 69 (cell 85, 128).

<a id="team-0c15d2ac"></a>

### Hint(IFV/GI) - 0C15D2AC

Owner: Player. Roster: 1 × IFV (FV); 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BP.

Ordered plan: Hint(IFV/GI) (0C1AF5AC).

1. Load transport.

<a id="team-0af2dafc"></a>

### FlashIFV1 - 0AF2DAFC

Owner: Player. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BR.

Ordered plan: StayPut (0AF2963C).

1. Guard for interval; configured argument 10.

<a id="team-0af2930c"></a>

### FlashIFV2 - 0AF2930C

Owner: Player. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BQ.

Ordered plan: StayPut (0AF2963C).

1. Guard for interval; configured argument 10.

<a id="team-0af2aefc"></a>

### FlashIFV3 - 0AF2AEFC

Owner: Player. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BP.

Ordered plan: StayPut (0AF2963C).

1. Guard for interval; configured argument 10.
