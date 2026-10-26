# Operation: Brain Wash - team rosters and plans

[Trigger ledger](sov03umd.md) | [Mission overrides](sov03umd-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: mapsmd03.mix/sov03umd.map; each team/script ID identifies its section.

<a id="team-093ad32c"></a>

### TM_Seal - 093AD32C

Owner: BadGuy1Country. Roster: 1 × SEAL (GHOST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: I.

Ordered plan: Blow Bridge (093AEDBC).

1. Flash team; configured argument 100.
2. Move to waypoint: waypoint 10 (cell 70, 121).
3. Attack/garrison waypoint building: waypoint 9 (cell 69, 120).

<a id="team-0bc5c90c"></a>

### TM_South Bridge Guard - 0BC5C90C

Owner: BadGuy1Country. Roster: 2 × Grizzly Battle Tank (MTNK); 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: I.

Ordered plan: Guard South Bridge (0D6BE40C).

1. Move to waypoint: waypoint 8 (cell 69, 117).
2. Adopt object mission: area guard.

<a id="team-0879e52c"></a>

### TM_Tanya_IFV - 0879E52C

Owner: AlliesCountry. Roster: 1 × Tanya (TANY); 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 3; Technology level: 0; Waypoint: R.

Ordered plan: Tanya Rolls On (0902E90C).

1. Move to waypoint: waypoint 18 (cell 50, 97).
2. Set local flag: local flag 0 (YuriSeesTanya).
3. Flash team; configured argument 100.
4. Unload with continuation mode: passengers continue; transport leaves team.
5. Flash team; configured argument 100.

<a id="team-0bcf01bc"></a>

### TM_SMiddle Backup - 0BCF01BC

Owner: BadGuy1Country. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: N.

Ordered plan: Defend SMiddle Bridge (0BD08DBC).

1. Move to waypoint: waypoint 13 (cell 71, 88).
2. Adopt object mission: area guard.

<a id="team-0bd262ec"></a>

### TM_3 Initiates Defense - 0BD262EC

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 10; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri Initiate Base Defense (0BD222DC).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-099ce37c"></a>

### TM_2 Lashers Attack - 099CE37C

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Lasher Attack (099CE10C).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-099d133c"></a>

### TM_3 Initiates Attack - 099D133C

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 10; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Initiate Attack (099D10CC).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-0c4297bc"></a>

### TM_5 GIs Attack - 0C4297BC

Owner: BadGuy1Country. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 10; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: X.

Ordered plan: GI Attack (0D444DBC).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-0d44492c"></a>

### TM_2 Guardian GI Attack - 0D44492C

Owner: BadGuy1Country. Roster: 2 × Guardian GI (GGI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: 2 Guardian GI Attack (0D4446BC).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-08e1245c"></a>

### TM_2 IFVs - 08E1245C

Owner: BadGuy1Country. Roster: 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: TB.

Ordered plan: 2 IFV Attack (0D4455CC).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-087a1efc"></a>

### TM_Tanya (Allied)_100 Flash - 087A1EFC

Owner: AlliesCountry. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 3; Technology level: 0; Waypoint: S.

Ordered plan: Flash 100-->Move to Z-->Delete (08B0407C).

1. Flash team; configured argument 100.
2. Move to waypoint: waypoint 25 (cell 44, 98).
3. Delete team objects.

<a id="team-087a1a4c"></a>

### TM_Tanya (Soviet)_100 Flash - 087A1A4C

Owner: SovietsCountry. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 3; Technology level: 0; Waypoint: Z.

Ordered plan: Flash 100 (0F77AC8C).

1. Flash team; configured argument 100.

<a id="team-087a16ac"></a>

### TM_Tanya (Allied)_250 Flash - 087A16AC

Owner: AlliesCountry. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 3; Technology level: 0; Waypoint: S.

Ordered plan: Flash 250 (0F6D212C).

1. Flash team; configured argument 250.

<a id="team-087a130c"></a>

### TM_Tanya (Soviet)_250 Flash - 087A130C

Owner: SovietsCountry. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 3; Technology level: 0; Waypoint: Y.

Ordered plan: Flash 250 (0F6D212C).

1. Flash team; configured argument 250.

<a id="team-087a10fc"></a>

### TM_Tanya (Allied)_350 Flash - 087A10FC

Owner: AlliesCountry. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 3; Technology level: 0; Waypoint: S.

Ordered plan: Flash 350 (0EF3C7BC).

1. Flash team; configured argument 350.

<a id="team-0c6261dc"></a>

### TM_Seal Leaves - 0C6261DC

Owner: AlliesCountry. Roster: 1 × SEAL (GHOST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: Seal Leaves the Map (043C1BEC).

1. Move to waypoint: waypoint 21 (cell 65, 123).
2. Delete team objects.

<a id="team-091f77bc"></a>

### TM_Allies_4 GIs to Tent - 091F77BC

Owner: AlliesCountry. Roster: 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: R.

Ordered plan: Go to Z-->Enter Tent (091F754C).

1. Scatter.
2. Move to waypoint: waypoint 25 (cell 44, 98).
3. Enter neutral occupiable building.
4. Change script: 96 (reference 96).

<a id="team-0b0d66ac"></a>

### TM_CIV1 (female) - 0B0D66AC

Owner: Civie3Country. Roster: 1 × Civilian (CIV1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Go To Grinder (08F461DC).

1. Enter Grinder.

<a id="team-0b0d61fc"></a>

### TM_CIV2 - 0B0D61FC

Owner: Civie3Country. Roster: 1 × Civilian (CIV2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Go To Grinder (08F461DC).

1. Enter Grinder.

<a id="team-0b0d7dec"></a>

### TM_CIV3 - 0B0D7DEC

Owner: Civie3Country. Roster: 1 × Civilian (CIV3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Go To Grinder (08F461DC).

1. Enter Grinder.

<a id="team-0b0d7bac"></a>

### TM_Civ Snow Female - 0B0D7BAC

Owner: Civie3Country. Roster: 1 × Civilian (CIVSF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 6; Veteran Level: 1; Technology level: 0.

Ordered plan: Go To Grinder (08F461DC).

1. Enter Grinder.

<a id="team-08fffefc"></a>

### TM_Allies_Chrono Arrives - 08FFFEFC

Owner: AlliesCountry. Roster: 1 × Chrono Miner (CMIN)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: R.

Ordered plan: Chrono Arrives (08FFFC8C).

1. Move to waypoint: waypoint 521 (cell 59, 101).
2. Adopt object mission: area guard.

<a id="team-08fc8b7c"></a>

### TM_BG2_6 Initiates into Bio - 08FC8B7C

Owner: BadGuy2Country. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Into Bio Reactor (08FFF7DC).

1. Panic.
2. Guard for interval; configured argument 10.
3. End panic.
4. Enter Bio Reactor.

<a id="team-07f33a4c"></a>

### TM_Yuri_3 Inits 2 Grinder Bio - 07F33A4C

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Into Bio Reactor (08FFF7DC).

1. Panic.
2. Guard for interval; configured argument 10.
3. End panic.
4. Enter Bio Reactor.

<a id="team-0440db8c"></a>

### TM_Yuri_"Everyone Attack" - 0440DB8C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AU.

Ordered plan: Move to AV-->All to Hunt (0440D91C).

1. Move to waypoint: waypoint 47 (cell 49, 30).
2. Adopt object mission: hunt.

<a id="team-07dc367c"></a>

### TM_Yuri_4 Init_2 Lash Attack - 07DC367C

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK); 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri Basic Attack (07DC340C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Report team success.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 4.
7. Seek/attack target category; configured argument 1.

<a id="team-086d763c"></a>

### TM_BG1_1 Grizzly - 086D763C

Owner: BadGuy1Country. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: TB.

Ordered plan: GI Attack (0D444DBC).

1. Seek/attack target category; configured argument 1.
2. Report team success.

<a id="team-0908b5ac"></a>

### TM_Seal Stop - 0908B5AC

Owner: BadGuy1Country. Roster: 1 × SEAL (GHOST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 100; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: K.

Ordered plan: Move to I (0908B33C).

1. Move to waypoint: waypoint 8 (cell 69, 117).
2. Adopt object mission: area guard.
