# Operation: Time Lapse - team rosters and plans

[Trigger ledger](all01umd.md) | [Mission overrides](all01umd-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: mapsmd03.mix/all01umd.map; each team/script ID identifies its section.

<a id="team-0a2bc12c"></a>

### Paradrop@I - 0A2BC12C

Owner: Russians. Roster: 8 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Transport Waypoint: J.

Ordered plan: Paradrop@I_AttackBase (08133DBC).

1. Seek/attack target category; configured argument 2.
2. Seek/attack target category; configured argument 1.
3. Report team success.

<a id="team-0a2bd90c"></a>

### Hover_Team_1 - 0A2BD90C

Owner: Nod. Roster: 1 × Lasher Light Tank (LTNK); 3 × Initiate (INIT); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: K.

Ordered plan: Hover_One_Attack (0A9F8B7C).

1. Move to waypoint: waypoint 11 (cell 89, 79).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 0 (Hover1_Unloaded).
4. Move to waypoint: waypoint 39 (cell 98, 87).
5. Move to waypoint: waypoint 40 (cell 92, 93).
6. Seek/attack target category; configured argument 4.
7. Seek/attack target category; configured argument 5.
8. Seek/attack target category; configured argument 2.
9. Seek/attack target category; configured argument 1.
10. Report team success.

<a id="team-0b7d664c"></a>

### Hover1_Home_Team - 0B7D664C

Owner: Nod. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: L.

Ordered plan: Hover1_Home_Script (0B7D63DC).

1. Move to waypoint: waypoint 10 (cell 50, 21).
2. Delete team objects.

<a id="team-089b3a4c"></a>

### TEAM_NW_Attack - 089B3A4C

Owner: Russians. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: NW_Team_Script (0A9F821C).

1. Move to waypoint: waypoint 80 (cell 76, 124).
2. Move to waypoint: waypoint 81 (cell 80, 120).
3. Move to waypoint: waypoint 8 (cell 84, 119).
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 4.
6. Seek/attack target category; configured argument 5.
7. Seek/attack target category; configured argument 7.
8. Seek/attack target category; configured argument 2.
9. Seek/attack target category; configured argument 1.
10. Report team success.

<a id="team-0b03e84c"></a>

### TEAM_Starting_GI - 0B03E84C

Owner: Americans. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: Deploy_Starting_GI (0B03E5DC).

1. Deploy.

<a id="team-08b03a4c"></a>

### TEAM_Starting_GGI - 08B03A4C

Owner: Americans. Roster: 5 × Guardian GI (GGI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: N.

Ordered plan: Deploy_Starting_GGI (0A2BFB7C).

1. Deploy.

<a id="team-043998ec"></a>

### TEAM_UT_Garrison - 043998EC

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: U.

Ordered plan: Garrsion_UT (0A797DBC).

1. Attack waypoint: waypoint 19 (cell 128, 97).

<a id="team-0aa79a4c"></a>

### AA_AB_Patrol - 0AA79A4C

Owner: YuriCountry. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AA.

Ordered plan: AA_AB_Patrol (0BB87DBC).

1. Attack-move toward waypoint: waypoint 27 (cell 139, 125).
2. Attack-move toward waypoint: waypoint 28 (cell 135, 126).
3. Attack-move toward waypoint: waypoint 29 (cell 134, 134).
4. Attack-move toward waypoint: waypoint 30 (cell 129, 135).
5. Attack-move toward waypoint: waypoint 29 (cell 134, 134).
6. Attack-move toward waypoint: waypoint 28 (cell 135, 126).
7. Attack-move toward waypoint: waypoint 26 (cell 127, 125).
8. Jump to script line; configured argument 1.

<a id="team-0bf1048c"></a>

### TEAM_GGI_GuineaPig - 0BF1048C

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: V.

Ordered plan: GGI_GuineaPig (0AB470CC).

1. Move to waypoint: waypoint 22 (cell 89, 97).

<a id="team-08b066cc"></a>

### TEAM_GGI_Flash - 08B066CC

Owner: Americans. Roster: 5 × Guardian GI (GGI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: N.

Ordered plan: Flash_GGI (08B0645C).

1. Flash team; configured argument 120.

<a id="team-0437f1ec"></a>

### TEAM_ZAI_Garrison - 0437F1EC

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: Z.

Ordered plan: Garrison_AI_Building (0437FCDC).

1. Attack waypoint: waypoint 34 (cell 118, 122).

<a id="team-089ce49c"></a>

### TEAM_AJ_AK_Garrison - 089CE49C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: AJ_AK_Garrison (089CE22C).

1. Attack waypoint: waypoint 36 (cell 145, 98).

<a id="team-0a80332c"></a>

### TEAM_Water_Two - 0A80332C

Owner: Confederation. Roster: 4 × Lasher Light Tank (LTNK); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: Y.

Ordered plan: Water_Two_Unload (0AA0521C).

1. Move to waypoint: waypoint 23 (cell 104, 65).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 1 (Hover_2_Unloaded).
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.
8. Report team success.

<a id="team-0ab4ab7c"></a>

### Hover2_Home_Team - 0AB4AB7C

Owner: Confederation. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: X.

Ordered plan: Hover2_Home_Script (0AB4A90C).

1. Move to waypoint: waypoint 24 (cell 56, 14).
2. Delete team objects.

<a id="team-08a006ac"></a>

### TEAM_AF_AG_Patrol - 08A006AC

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AG.

Ordered plan: AF_AH_Patrol (08A0043C).

1. Attack-move toward waypoint: waypoint 31 (cell 150, 101).
2. Attack-move toward waypoint: waypoint 33 (cell 150, 111).
3. Attack-move toward waypoint: waypoint 31 (cell 150, 101).
4. Attack-move toward waypoint: waypoint 32 (cell 138, 101).
5. Jump to script line; configured argument 1.

<a id="team-0a7f16ac"></a>

### TEAM_Water3 - 0A7F16AC

Owner: Germans. Roster: 3 × Lasher Light Tank (LTNK); 2 × Initiate (INIT); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AL.

Ordered plan: Water3_Land (0AA0421C).

1. Move to waypoint: waypoint 38 (cell 81, 86).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 2 (Hover_3_Unloaded).
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.
8. Report team success.

<a id="team-0b16493c"></a>

### Hover3_Home_Team - 0B16493C

Owner: Germans. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AM.

Ordered plan: Hover3_Go_Home (0B1646CC).

1. Move to waypoint: waypoint 37 (cell 42, 29).
2. Delete team objects.

<a id="team-09f3bc1c"></a>

### TEAM_Attack_Tanya - 09F3BC1C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AP.

Ordered plan: Attack_Tanya (09F3B76C).

1. Move to waypoint: waypoint 14 (cell 100, 110).
2. Seek/attack target category; configured argument 4.
3. Report team success.

<a id="team-09f3a3cc"></a>

### TEAM_Apocs - 09F3A3CC

Owner: Russians. Roster: 4 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CB.

Ordered plan: Apoc_Attack (0927132C).

1. Attack/garrison waypoint building: waypoint 78 (cell 75, 100).
2. Seek/attack target category; configured argument 1.

<a id="team-093ddc8c"></a>

### TEAM_Apoc1 - 093DDC8C

Owner: Special. Roster: 1 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CE.

Ordered plan: Apoc1_Script (09270C8C).

1. Set facing; configured argument 6.
2. Attack/garrison waypoint building: waypoint 78 (cell 75, 100).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 10.

<a id="team-093dd7dc"></a>

### TEAM_Apoc2 - 093DD7DC

Owner: Special. Roster: 1 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CF.

Ordered plan: Apoc2_Script (092707DC).

1. Set facing; configured argument 6.
2. Attack/garrison waypoint building: waypoint 78 (cell 75, 100).
3. Seek/attack target category; configured argument 1.

<a id="team-093dd32c"></a>

### TEAM_Apoc3 - 093DD32C

Owner: Special. Roster: 1 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CG.

Ordered plan: Apoc3_Script (0927032C).

1. Set facing; configured argument 6.
2. Attack/garrison waypoint building: waypoint 78 (cell 75, 100).
3. Seek/attack target category; configured argument 1.

<a id="team-093dfdec"></a>

### TEAM_Apoc4 - 093DFDEC

Owner: Special. Roster: 1 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CH.

Ordered plan: Apoc4_Script (0930529C).

1. Set facing; configured argument 6.
2. Attack/garrison waypoint building: waypoint 78 (cell 75, 100).
3. Seek/attack target category; configured argument 1.

<a id="team-0d2af91c"></a>

### TEAM_AP_Paradrop - 0D2AF91C

Owner: Africans. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AP; Transport Waypoint: CI.

Ordered plan: AP_Paradrop_Script (0D2AF6AC).

1. Move to waypoint: waypoint 42 (cell 101, 111).
2. Seek/attack target category; configured argument 2.
3. Seek/attack target category; configured argument 1.
4. Report team success.

<a id="team-0955bb7c"></a>

### TEAM_Dred1 - 0955BB7C

Owner: French. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: DX.

Ordered plan: Dred1_Script (0C32290C).

1. Set facing; configured argument 2.
2. Attack selected enemy-building category; configured argument 131138.

<a id="team-0955b6cc"></a>

### TEAM_Dred2 - 0955B6CC

Owner: French. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: DY.

Ordered plan: Dred2_Script (0B4F0DBC).

1. Set facing; configured argument 2.
2. Attack/garrison waypoint building: waypoint 70 (cell 73, 102).
3. Attack waypoint: waypoint 286 (cell 78, 85).
4. Attack waypoint: waypoint 441 (cell 87, 90).

<a id="team-0955b21c"></a>

### TEAM_Dred3 - 0955B21C

Owner: French. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: DZ.

Ordered plan: Dred3_Script (0C360A1C).

1. Set facing; configured argument 3.
2. Attack waypoint: waypoint 291 (cell 99, 65).
3. Attack waypoint: waypoint 125 (cell 102, 72).
4. Attack waypoint: waypoint 440 (cell 108, 75).

<a id="team-09645efc"></a>

### TEAM_Scorp1 - 09645EFC

Owner: French. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: ST.

Ordered plan: Scorp1_Script (09645C8C).

1. Move to waypoint: waypoint 63 (cell 66, 64).
2. Move to waypoint: waypoint 64 (cell 61, 50).
3. Move to waypoint: waypoint 65 (cell 46, 45).
4. Move to waypoint: waypoint 66 (cell 35, 53).
5. Move to waypoint: waypoint 67 (cell 31, 70).
6. Move to waypoint: waypoint 68 (cell 49, 88).
7. Move to waypoint: waypoint 69 (cell 62, 85).
8. Move to waypoint: waypoint 513 (cell 69, 79).
9. Jump to script line; configured argument 1.

<a id="team-09645a4c"></a>

### TEAM_Scorp2 - 09645A4C

Owner: French. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: BO.

Ordered plan: Scorp2_Script (091F7C8C).

1. Move to waypoint: waypoint 67 (cell 31, 70).
2. Move to waypoint: waypoint 68 (cell 49, 88).
3. Move to waypoint: waypoint 69 (cell 62, 85).
4. Move to waypoint: waypoint 513 (cell 69, 79).
5. Move to waypoint: waypoint 63 (cell 66, 64).
6. Move to waypoint: waypoint 64 (cell 61, 50).
7. Move to waypoint: waypoint 65 (cell 46, 45).
8. Move to waypoint: waypoint 66 (cell 35, 53).
9. Jump to script line; configured argument 1.

<a id="team-0964580c"></a>

### TEAM_Scorp3 - 0964580C

Owner: French. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: BM.

Ordered plan: Scorp3_Script (091F730C).

1. Move to waypoint: waypoint 65 (cell 46, 45).
2. Move to waypoint: waypoint 66 (cell 35, 53).
3. Move to waypoint: waypoint 67 (cell 31, 70).
4. Move to waypoint: waypoint 68 (cell 49, 88).
5. Move to waypoint: waypoint 69 (cell 62, 85).
6. Move to waypoint: waypoint 513 (cell 69, 79).
7. Move to waypoint: waypoint 63 (cell 66, 64).
8. Move to waypoint: waypoint 64 (cell 61, 50).
9. Jump to script line; configured argument 1.

<a id="team-096455cc"></a>

### TEAM_Scorp4 - 096455CC

Owner: French. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: BQ.

Ordered plan: Scorp4_Script (091F5ABC).

1. Move to waypoint: waypoint 69 (cell 62, 85).
2. Move to waypoint: waypoint 513 (cell 69, 79).
3. Move to waypoint: waypoint 63 (cell 66, 64).
4. Move to waypoint: waypoint 64 (cell 61, 50).
5. Move to waypoint: waypoint 65 (cell 46, 45).
6. Move to waypoint: waypoint 66 (cell 35, 53).
7. Move to waypoint: waypoint 67 (cell 31, 70).
8. Move to waypoint: waypoint 68 (cell 49, 88).
9. Jump to script line; configured argument 1.

<a id="team-08071c8c"></a>

### TEAM_Carriers - 08071C8C

Owner: Americans. Roster: 3 × Aircraft Carrier (CARRIER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: CQ.

Ordered plan: Carrier_Script (089B0DBC).

1. Move to waypoint: waypoint 417 (cell 56, 89).

<a id="team-0aa2aefc"></a>

### TEAM_RA_Tanks - 0AA2AEFC

Owner: Russians. Roster: 4 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: RA.

Ordered plan: RA_Tanks_Script (0E5B3A1C).

1. Move to waypoint: waypoint 469 (cell 101, 119).
2. Move to waypoint: waypoint 470 (cell 88, 118).
3. Seek/attack target category; configured argument 1.

<a id="team-0bb37c5c"></a>

### TEAM_RDU_Patrol - 0BB37C5C

Owner: YuriCountry. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: RD.

Ordered plan: RDU_Patrol_Script (0BB379EC).

1. Attack-move toward waypoint: waypoint 472 (cell 128, 79).
2. Attack-move toward waypoint: waypoint 473 (cell 130, 81).
3. Attack-move toward waypoint: waypoint 474 (cell 129, 91).
4. Attack-move toward waypoint: waypoint 20 (cell 129, 101).
5. Attack-move toward waypoint: waypoint 474 (cell 129, 91).
6. Attack-move toward waypoint: waypoint 473 (cell 130, 81).
7. Attack-move toward waypoint: waypoint 472 (cell 128, 79).
8. Attack-move toward waypoint: waypoint 471 (cell 120, 79).
9. Jump to script line; configured argument 1.

<a id="team-0bb4625c"></a>

### TEAM_RHRL_Patrol - 0BB4625C

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: RH.

Ordered plan: RHRL_Patrol_Script (0BB47DBC).

1. Attack-move toward waypoint: waypoint 476 (cell 128, 150).
2. Attack-move toward waypoint: waypoint 477 (cell 117, 150).
3. Attack-move toward waypoint: waypoint 478 (cell 117, 143).
4. Attack-move toward waypoint: waypoint 479 (cell 112, 142).
5. Attack-move toward waypoint: waypoint 478 (cell 117, 143).
6. Attack-move toward waypoint: waypoint 477 (cell 117, 150).
7. Attack-move toward waypoint: waypoint 476 (cell 128, 150).
8. Attack-move toward waypoint: waypoint 475 (cell 128, 141).
9. Jump to script line; configured argument 1.

<a id="team-0c36e6ac"></a>

### TEAM_RM_RN_Attack - 0C36E6AC

Owner: Russians. Roster: 4 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: RM.

Ordered plan: RM_RN_Script (0C36E43C).

1. Move to waypoint: waypoint 481 (cell 102, 100).
2. Attack selected enemy-building category; configured argument 314.
3. Seek/attack target category; configured argument 2.
4. Seek/attack target category; configured argument 1.
5. Report team success.

<a id="team-0a7ab79c"></a>

### TEAM_Taxi1 - 0A7AB79C

Owner: Neutral. Roster: 1 × Taxi (TAXI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: DA.

Ordered plan: Taxi1_Script (0A9467DC).

1. Move to waypoint: waypoint 679 (cell 109, 77).
2. Move to waypoint: waypoint 108 (cell 87, 83).
3. Move to waypoint: waypoint 111 (cell 80, 95).
4. Move to waypoint: waypoint 112 (cell 84, 96).
5. Move to waypoint: waypoint 111 (cell 80, 95).
6. Move to waypoint: waypoint 108 (cell 87, 83).
7. Move to waypoint: waypoint 679 (cell 109, 77).
8. Move to waypoint: waypoint 104 (cell 114, 68).
9. Jump to script line; configured argument 1.

<a id="team-0a7ab0cc"></a>

### TEAM_Truck1 - 0A7AB0CC

Owner: Neutral. Roster: 1 × Pickup Truck (PTRUCK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: DL.

Ordered plan: Truck1_Script (0A91721C).

1. Move to waypoint: waypoint 116 (cell 105, 65).
2. Move to waypoint: waypoint 117 (cell 105, 77).
3. Move to waypoint: waypoint 118 (cell 115, 79).
4. Move to waypoint: waypoint 119 (cell 129, 79).
5. Move to waypoint: waypoint 20 (cell 129, 101).
6. Move to waypoint: waypoint 35 (cell 150, 102).
7. Move to waypoint: waypoint 120 (cell 149, 112).
8. Move to waypoint: waypoint 121 (cell 152, 112).
9. Move to waypoint: waypoint 122 (cell 152, 115).
10. Move to waypoint: waypoint 130 (cell 156, 115).
11. Move to waypoint: waypoint 122 (cell 152, 115).
12. Move to waypoint: waypoint 121 (cell 152, 112).
13. Move to waypoint: waypoint 120 (cell 149, 112).
14. Move to waypoint: waypoint 35 (cell 150, 102).
15. Move to waypoint: waypoint 20 (cell 129, 101).
16. Move to waypoint: waypoint 119 (cell 129, 79).
17. Move to waypoint: waypoint 118 (cell 115, 79).
18. Move to waypoint: waypoint 117 (cell 105, 77).
19. Move to waypoint: waypoint 116 (cell 105, 65).
20. Move to waypoint: waypoint 115 (cell 103, 65).
21. Jump to script line; configured argument 1.

<a id="team-0a7acc6c"></a>

### TEAM_Cop1 - 0A7ACC6C

Owner: Neutral. Roster: 1 × Police Car (COP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: U.

Ordered plan: Cop1_Script (0A90532C).

1. Move to waypoint: waypoint 481 (cell 102, 100).
2. Move to waypoint: waypoint 13 (cell 88, 100).
3. Move to waypoint: waypoint 481 (cell 102, 100).
4. Move to waypoint: waypoint 20 (cell 129, 101).
5. Jump to script line; configured argument 1.

<a id="team-0a7ac7bc"></a>

### TEAM_ConVehicle1 - 0A7AC7BC

Owner: Neutral. Roster: 1 × Excavator (CONA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: EB.

Ordered plan: ConVehicle1_Script (08A06C2C).

1. Guard for interval; configured argument 120.
2. Jump to script line; configured argument 1.

<a id="team-0a7ac30c"></a>

### TEAM_ConVehicle2 - 0A7AC30C

Owner: Neutral. Roster: 1 × Excavator (CONA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: EC.

Ordered plan: ConVehicle2_Script (08A0664C).

1. Guard for interval; configured argument 120.
2. Jump to script line; configured argument 1.

<a id="team-0a7addec"></a>

### TEAM_Cop2 - 0A7ADDEC

Owner: Neutral. Roster: 1 × Police Car (COP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: ED.

Ordered plan: Cop2_Script (0A90632C).

1. Move to waypoint: waypoint 134 (cell 113, 118).
2. Move to waypoint: waypoint 135 (cell 115, 118).
3. Move to waypoint: waypoint 136 (cell 115, 110).
4. Move to waypoint: waypoint 137 (cell 111, 110).
5. Move to waypoint: waypoint 138 (cell 111, 100).
6. Move to waypoint: waypoint 13 (cell 88, 100).
7. Move to waypoint: waypoint 138 (cell 111, 100).
8. Move to waypoint: waypoint 137 (cell 111, 110).
9. Move to waypoint: waypoint 136 (cell 115, 110).
10. Move to waypoint: waypoint 135 (cell 115, 118).
11. Move to waypoint: waypoint 134 (cell 113, 118).
12. Move to waypoint: waypoint 133 (cell 113, 149).
13. Jump to script line; configured argument 1.

<a id="team-06a1c95c"></a>

### TEAM_Civ1 - 06A1C95C

Owner: Neutral. Roster: 1 × Civilian (CIV1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Civ1_Script (06A1C6EC).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-06a1c37c"></a>

### TEAM_Civ2 - 06A1C37C

Owner: Neutral. Roster: 1 × Civilian (CIV2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Civ2_Script (06A1C10C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-06a1debc"></a>

### TEAM_Civ3 - 06A1DEBC

Owner: Neutral. Roster: 1 × Civilian (CIV3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Civ3_Script (06A1DC4C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-068fe26c"></a>

### TEAM_Calm_Civ1 - 068FE26C

Owner: Neutral. Roster: 1 × Civilian (CIV1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Calm_Civ1_Script (068FFDBC).

1. Guard for interval; configured argument 120.
2. Jump to script line; configured argument 1.

<a id="team-068ffc5c"></a>

### TEAM_Calm_Civ2 - 068FFC5C

Owner: Neutral. Roster: 1 × Civilian (CIV2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Calm_Civ1_Script (068FFDBC).

1. Guard for interval; configured argument 120.
2. Jump to script line; configured argument 1.

<a id="team-068ffb2c"></a>

### TEAM_Calm_Civ3 - 068FFB2C

Owner: Neutral. Roster: 1 × Civilian (CIV3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Calm_Civ1_Script (068FFDBC).

1. Guard for interval; configured argument 120.
2. Jump to script line; configured argument 1.

<a id="team-068fc13c"></a>

### TEAM_Stat_Stang - 068FC13C

Owner: Neutral. Roster: 1 × Automobile (STANG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Stat_Stang_UL_Script (0A91BC8C).

1. Set facing; configured argument 6.

<a id="team-068fdefc"></a>

### TEAM_Stat_SUVW - 068FDEFC

Owner: Neutral. Roster: 1 × Automobile (SUVW)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Stat_SUVW_LR_Script (0A91B7DC).

1. Set facing; configured argument 2.

<a id="team-0692d74c"></a>

### TEAM_SUVW1 - 0692D74C

Owner: Neutral. Roster: 1 × Automobile (SUVW)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0; Waypoint: GC.

Ordered plan: SUVW1_Script (0692D4DC).

1. Move to waypoint: waypoint 28 (cell 135, 126).
2. Move to waypoint: waypoint 185 (cell 135, 125).
3. Move to waypoint: waypoint 186 (cell 86, 125).
4. Move to waypoint: waypoint 184 (cell 86, 126).
5. Jump to script line; configured argument 1.

<a id="team-0692ab8c"></a>

### TEAM_Cop3 - 0692AB8C

Owner: Neutral. Roster: 1 × Police Car (COP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: GD.

Ordered plan: Cop3_Script (0692A91C).

1. Move to waypoint: waypoint 186 (cell 86, 125).
2. Move to waypoint: waypoint 184 (cell 86, 126).
3. Move to waypoint: waypoint 28 (cell 135, 126).
4. Move to waypoint: waypoint 185 (cell 135, 125).
5. Jump to script line; configured argument 1.

<a id="team-069226cc"></a>

### TEAM_Cop4 - 069226CC

Owner: Neutral. Roster: 1 × Police Car (COP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: GF.

Ordered plan: Cop4_Script (0692245C).

1. Move to waypoint: waypoint 114 (cell 153, 102).
2. Move to waypoint: waypoint 187 (cell 87, 102).
3. Move to waypoint: waypoint 188 (cell 151, 100).
4. Move to waypoint: waypoint 13 (cell 88, 100).
5. Move to waypoint: waypoint 187 (cell 87, 102).
6. Jump to script line; configured argument 1.

<a id="team-0c92859c"></a>

### TEAM_Alcatraz1 - 0C92859C

Owner: French. Roster: 1 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 50; Veteran Level: 1; Technology level: 0.

Ordered plan: Alcatraz_1_Script (0692849C).

1. Set facing; configured argument 6.
2. Guard for interval; configured argument 120.
3. Jump to script line; configured argument 2.

<a id="team-0c95aa7c"></a>

### TEAM_Alcatraz_2 - 0C95AA7C

Owner: French. Roster: 1 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 50; Veteran Level: 1; Technology level: 0.

Ordered plan: Alcatraz_2_Script (0692C79C).

1. Set facing; configured argument 1.
2. Guard for interval; configured argument 120.
3. Jump to script line; configured argument 2.

<a id="team-0c39aefc"></a>

### TEAM_SUVB_LL - 0C39AEFC

Owner: Neutral. Roster: 1 × Automobile (SUVB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: Stat_SUVB_LL (0C39AC8C).

1. Set facing; configured argument 4.
2. Guard for interval; configured argument 120.
3. Jump to script line; configured argument 2.

<a id="team-0c39803c"></a>

### TEAM_WINI_UR - 0C39803C

Owner: Neutral. Roster: 1 × Recreational Vehicle (WINI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 10; Veteran Level: 1; Technology level: 0.

Ordered plan: Wini_UR_Script (0C39879C).

1. Set facing; configured argument 1.
2. Guard for interval; configured argument 120.
3. Jump to script line; configured argument 2.

<a id="team-0c8992cc"></a>

### TEAM_Stang2 - 0C8992CC

Owner: Neutral. Roster: 1 × Automobile (STANG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Stang2_Script (0C89905C).

1. Move to waypoint: waypoint 191 (cell 115, 102).
2. Move to waypoint: waypoint 192 (cell 114, 83).
3. Move to waypoint: waypoint 193 (cell 103, 83).
4. Move to waypoint: waypoint 194 (cell 104, 78).
5. Move to waypoint: waypoint 107 (cell 101, 78).
6. Move to waypoint: waypoint 195 (cell 96, 82).
7. Move to waypoint: waypoint 196 (cell 86, 82).
8. Move to waypoint: waypoint 197 (cell 86, 84).
9. Move to waypoint: waypoint 198 (cell 80, 84).
10. Move to waypoint: waypoint 111 (cell 80, 95).
11. Move to waypoint: waypoint 112 (cell 84, 96).
12. Move to waypoint: waypoint 114 (cell 153, 102).
13. Jump to script line; configured argument 1.

<a id="team-08bf127c"></a>

### TEAM_Bus1 - 08BF127C

Owner: Neutral. Roster: 1 × Cable Car (CBLC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Bus1_Script (08BF2DBC).

1. Move to waypoint: waypoint 46 (cell 85, 101).
2. Move to waypoint: waypoint 55 (cell 127, 100).
3. Jump to script line; configured argument 1.

<a id="team-0a7c0a8c"></a>

### TEAM_SUVB_2 - 0A7C0A8C

Owner: Neutral. Roster: 1 × Automobile (SUVB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: SUVB2_Script (0A7C081C).

1. Move to waypoint: waypoint 199 (cell 135, 119).
2. Move to waypoint: waypoint 200 (cell 134, 119).
3. Move to waypoint: waypoint 201 (cell 133, 114).
4. Move to waypoint: waypoint 202 (cell 132, 114).
5. Move to waypoint: waypoint 203 (cell 131, 106).
6. Move to waypoint: waypoint 204 (cell 130, 106).
7. Move to waypoint: waypoint 20 (cell 129, 101).
8. Move to waypoint: waypoint 35 (cell 150, 102).
9. Move to waypoint: waypoint 120 (cell 149, 112).
10. Move to waypoint: waypoint 121 (cell 152, 112).
11. Move to waypoint: waypoint 122 (cell 152, 115).
12. Move to waypoint: waypoint 205 (cell 152, 125).
13. Move to waypoint: waypoint 27 (cell 139, 125).
14. Move to waypoint: waypoint 28 (cell 135, 126).
15. Jump to script line; configured argument 1.

<a id="team-0780f21c"></a>

### TEAM_Harriers - 0780F21C

Owner: Alliance. Roster: 1 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: PG.

Ordered plan: Harrier1_Script (0C69990C).

1. Move to waypoint: waypoint 214 (cell 60, 69).

<a id="team-0780bc8c"></a>

### TEAM_Harrier2 - 0780BC8C

Owner: Alliance. Roster: 1 × Harrier (ORCA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: PC.

Ordered plan: Harrier2_Script (0C69945C).

1. Move to waypoint: waypoint 214 (cell 60, 69).

<a id="team-088c1a4c"></a>

### TEAM_Tanya - 088C1A4C

Owner: Americans. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 3; Technology level: 0; Waypoint: PE.

Ordered plan: TEAM_Tanya (0926745C).

1. Move to waypoint: waypoint 93 (cell 96, 106).
2. Adopt object mission: area guard.

<a id="team-0aeb2efc"></a>

### TEAM_CityP1 - 0AEB2EFC

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: ZC.

Ordered plan: CityP1_Script (0AEB2C8C).

1. Move to waypoint: waypoint 134 (cell 113, 118).
2. Move to waypoint: waypoint 678 (cell 112, 135).
3. Jump to script line; configured argument 1.

<a id="team-089305fc"></a>

### TEAM_City2 - 089305FC

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: GJ.

Ordered plan: CityP2_Script (0893038C).

1. Move to waypoint: waypoint 313 (cell 137, 101).
2. Move to waypoint: waypoint 191 (cell 115, 102).
3. Jump to script line; configured argument 1.

<a id="team-0aeb68dc"></a>

### TEAM_CityP3 - 0AEB68DC

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BB.

Ordered plan: CityP3_Script (0AEB666C).

1. Move to waypoint: waypoint 54 (cell 129, 89).
2. Move to waypoint: waypoint 53 (cell 114, 89).
3. Jump to script line; configured argument 1.

<a id="team-08934b5c"></a>

### TEAM_CityP4 - 08934B5C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: CityP4_Script (089348EC).

1. Move to waypoint: waypoint 204 (cell 130, 106).
2. Move to waypoint: waypoint 54 (cell 129, 89).
3. Jump to script line; configured argument 1.

<a id="team-0aeb564c"></a>

### TEAM_CityP5 - 0AEB564C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: CityP5_Script (0AEB50CC).

1. Move to waypoint: waypoint 205 (cell 152, 125).
2. Move to waypoint: waypoint 27 (cell 139, 125).
3. Jump to script line; configured argument 1.

<a id="team-096c680c"></a>

### TEAM_CityP6 - 096C680C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: ZF.

Ordered plan: CityP6_Script (096C659C).

1. Move to waypoint: waypoint 205 (cell 152, 125).
2. Move to waypoint: waypoint 681 (cell 153, 114).
3. Jump to script line; configured argument 1.

<a id="team-09569a4c"></a>

### TEAM_Dred4 - 09569A4C

Owner: French. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KC.

Ordered plan: DredKC_Script (0C372DBC).

1. Set facing; configured argument 2.
2. Attack waypoint: waypoint 287 (cell 83, 83).
3. Attack waypoint: waypoint 294 (cell 86, 80).
4. Attack waypoint: waypoint 109 (cell 88, 87).

<a id="team-0956959c"></a>

### TEAM_Dred5 - 0956959C

Owner: French. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KD.

Ordered plan: DredKD_Script (094DB7DC).

1. Set facing; configured argument 2.
2. Attack/garrison waypoint building: waypoint 194 (cell 104, 78).
3. Move to waypoint: waypoint 127 (cell 64, 90).
4. Move to waypoint: waypoint 289 (cell 90, 52).
5. Jump to script line; configured argument 3.

<a id="team-0956aefc"></a>

### TEAM_Dred6 - 0956AEFC

Owner: French. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KE.

Ordered plan: DredKE_Script (0956AC8C).

1. Set facing; configured argument 2.
2. Attack/garrison waypoint building: waypoint 292 (cell 112, 64).
3. Move to waypoint: waypoint 127 (cell 64, 90).
4. Move to waypoint: waypoint 290 (cell 98, 51).
5. Jump to script line; configured argument 3.

<a id="team-0b4ffc8c"></a>

### TEAM_Dred7 - 0B4FFC8C

Owner: French. Roster: 1 × Dreadnought (DRED)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KH.

Ordered plan: DredKH_Script (0956A7DC).

1. Set facing; configured argument 2.
2. Attack waypoint: waypoint 109 (cell 88, 87).
3. Move to waypoint: waypoint 513 (cell 69, 79).
4. Move to waypoint: waypoint 127 (cell 64, 90).
5. Jump to script line; configured argument 3.

<a id="team-0973710c"></a>

### TEAM_CruiseShip1 - 0973710C

Owner: Neutral. Roster: 1 × Cruise Ship (CRUISE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KJ.

Ordered plan: CruiseShip1_Script (06B482DC).

1. Set facing; configured argument 0.
2. Adopt object mission: sleep.

<a id="team-0973241c"></a>

### TEAM_CruiseShip2 - 0973241C

Owner: Neutral. Roster: 1 × Cruise Ship (CRUISE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KK.

Ordered plan: CruiseShip2_Script (06B4AC8C).

1. Set facing; configured argument 6.
2. Adopt object mission: sleep.

<a id="team-09339c8c"></a>

### TEAM_ScorpPatrol1 - 09339C8C

Owner: French. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KL.

Ordered plan: ScorpPatrol1 (0798D54C).

1. Move to waypoint: waypoint 299 (cell 61, 65).
2. Move to waypoint: waypoint 297 (cell 61, 58).
3. Jump to script line; configured argument 1.

<a id="team-09735b1c"></a>

### TEAM_TugBoat2 - 09735B1C

Owner: Neutral. Roster: 1 × Tug Boat (TUG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KM.

Ordered plan: TugBoat2_Script (06B4A43C).

1. Set facing; configured argument 6.
2. Adopt object mission: sleep.

<a id="team-0925e45c"></a>

### TEAM_SovArmor1 - 0925E45C

Owner: Soviet2 Country. Roster: 2 × Rhino Heavy Tank (HTNK); 1 × Tesla Tank (TTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RM.

Ordered plan: SovArmor1_Script (0973352C).

1. Move to waypoint: waypoint 14 (cell 100, 110).
2. Seek/attack target category; configured argument 1.

<a id="team-0925fdec"></a>

### TEAM_SovArmor2 - 0925FDEC

Owner: Soviet2 Country. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RM.

Ordered plan: SovArmor2_Script (0973D72C).

1. Move to waypoint: waypoint 421 (cell 98, 101).
2. Seek/attack target category; configured argument 1.

<a id="team-096fcb5c"></a>

### TEAM_CityP7 - 096FCB5C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: ZB.

Ordered plan: CityP7_Script (096FC8EC).

1. Move to waypoint: waypoint 680 (cell 134, 110).
2. Move to waypoint: waypoint 677 (cell 122, 110).
3. Jump to script line; configured argument 1.

<a id="team-0c96fb7c"></a>

### TEAM_CW_Garrison - 0C96FB7C

Owner: French. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CX.

Ordered plan: NA_Garrison_Script (0C819ABC).

1. Attack waypoint: waypoint 100 (cell 41, 71).

<a id="team-0b7feecc"></a>

### TEAM_Lame_Tanks - 0B7FEECC

Owner: French. Roster: 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: NC.

Ordered plan: LameTank_Script (0B7FEC5C).

1. Move to waypoint: waypoint 367 (cell 42, 59).
2. Move to waypoint: waypoint 366 (cell 46, 54).
3. Jump to script line; configured argument 1.

<a id="team-0941632c"></a>

### TEAM_Kirov_HT - 0941632C

Owner: Soviet2 Country. Roster: 1 × Kirov Airship (ZEP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: HT.

Ordered plan: Kirov_Script (0962056C).

1. Move to waypoint: waypoint 304 (cell 70, 106).
2. Attack selected enemy-building category; configured argument 131136.
3. Move to waypoint: waypoint 146 (cell 107, 80).
4. Attack/garrison waypoint building: waypoint 146 (cell 107, 80).
5. Move to waypoint: waypoint 147 (cell 124, 76).
6. Attack/garrison waypoint building: waypoint 147 (cell 124, 76).
7. Move to waypoint: waypoint 148 (cell 126, 71).
8. Delete team objects.

<a id="team-0e0f469c"></a>

### TEAM_GGI_Group2 - 0E0F469C

Owner: Americans. Roster: 5 × Guardian GI (GGI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RN.

Ordered plan: GGI_Group2_Script (0E0F442C).

1. Deploy.

<a id="team-0d3fa93c"></a>

### TEAM_Start_Engineer - 0D3FA93C

Owner: Americans. Roster: 1 × Engineer (ENGINEER); 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: O.

Ordered plan: Start_Engineer_Script (06C9B07C).

1. Load transport.

<a id="team-0c8e7a8c"></a>

### TEAM_PP1_Group_PatrolA - 0C8E7A8C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AA.

Ordered plan: PP1_Group_Patrol_Script (0C8E8DBC).

1. Move to waypoint: waypoint 27 (cell 139, 125).
2. Move to waypoint: waypoint 26 (cell 127, 125).
3. Jump to script line; configured argument 1.

<a id="team-06b9cd4c"></a>

### TEAM_PP1_Group_PatrolB - 06B9CD4C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: PP1_Group_PatrolB (06B9CADC).

1. Move to waypoint: waypoint 185 (cell 135, 125).
2. Move to waypoint: waypoint 29 (cell 134, 134).
3. Jump to script line; configured argument 1.

<a id="team-0dc53efc"></a>

### TEAM_Nuke_Repair - 0DC53EFC

Owner: Confederation. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BG.

Ordered plan: Nuke_Repair (0DCD703C).

1. Attack waypoint: waypoint 364 (cell 55, 72).

<a id="team-060fb74c"></a>

### TEAM_CableCar2 - 060FB74C

Owner: Neutral. Roster: 1 × Cable Car (CBLC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AH.

Ordered plan: CableCar_Script (060FDC5C).

1. Move to waypoint: waypoint 137 (cell 111, 110).
2. Move to waypoint: waypoint 33 (cell 150, 111).
3. Jump to script line; configured argument 1.

<a id="team-096d287c"></a>

### TEAM_BYgarrison - 096D287C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BY.

Ordered plan: BY_Garrision (096D260C).

1. Attack/garrison waypoint building: waypoint 77 (cell 119, 124).

<a id="team-0796497c"></a>

### ScorpPatrol2 - 0796497C

Owner: French. Roster: 1 × Sea Scorpion (HYD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KO.

Ordered plan: ScorpPatrol2 (0796470C).

1. Move to waypoint: waypoint 301 (cell 63, 58).
2. Move to waypoint: waypoint 300 (cell 63, 65).
3. Jump to script line; configured argument 1.

<a id="team-098a9b5c"></a>

### Alcatraz_Patrol - 098A9B5C

Owner: Confederation. Roster: 4 × Conscript (E2); 2 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BT.

Ordered plan: Alcatraz_Patrol (098A833C).

1. Move to waypoint: waypoint 72 (cell 53, 61).
2. Move to waypoint: waypoint 71 (cell 52, 73).
3. Jump to script line; configured argument 1.

<a id="team-0788e0ec"></a>

### SovGar_BV - 0788E0EC

Owner: French. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BV.

Ordered plan: Sov_Garrison (0788BDBC).

1. Enter neutral occupiable building.

<a id="team-0788f21c"></a>

### SovGarrision_BW - 0788F21C

Owner: French. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BW.

Ordered plan: Sov_Garrison (0788BDBC).

1. Enter neutral occupiable building.

<a id="team-0788bc4c"></a>

### SovGarrision_BX - 0788BC4C

Owner: French. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BX.

Ordered plan: Sov_Garrison (0788BDBC).

1. Enter neutral occupiable building.

<a id="team-077d3bac"></a>

### SovGar_CK - 077D3BAC

Owner: French. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CK.

Ordered plan: Sov_Garrison (0788BDBC).

1. Enter neutral occupiable building.

<a id="team-077d3a7c"></a>

### SovGarr_CL - 077D3A7C

Owner: French. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CL.

Ordered plan: Sov_Garrison (0788BDBC).

1. Enter neutral occupiable building.

<a id="team-077d394c"></a>

### SovGarr_CM - 077D394C

Owner: French. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CM.

Ordered plan: Sov_Garrison (0788BDBC).

1. Enter neutral occupiable building.

<a id="team-077d381c"></a>

### SovGarr_CN - 077D381C

Owner: French. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CN.

Ordered plan: Sov_Garrison (0788BDBC).

1. Enter neutral occupiable building.

<a id="team-077d36ec"></a>

### SovGar_CO - 077D36EC

Owner: French. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CO.

Ordered plan: Sov_Garrison (0788BDBC).

1. Enter neutral occupiable building.

<a id="team-0908b07c"></a>

### Engineers - 0908B07C

Owner: Americans. Roster: 4 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: EM; Transport Waypoint: EN.

Ordered plan: Engineers (0AE30DBC).

1. Set local flag: local flag 54 (Engineers_Landed).
2. Adopt object mission: area guard.

<a id="team-0915293c"></a>

### Leftover_Guy - 0915293C

Owner: Confederation. Roster: 1 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: HA.

Ordered plan: Leftover_Guy (091526CC).

1. Delete team objects.
