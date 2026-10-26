# Operation: Brain Dead - team rosters and plans

[Trigger ledger](all07smd.md) | [Mission overrides](all07smd-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: mapsmd03.mix/all07smd.map; each team/script ID identifies its section.

<a id="team-0b1df85c"></a>

### TEAM_Player_Engineer1 - 0B1DF85C

Owner: Americans. Roster: 5 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: DD; Transport Waypoint: DA.

Ordered plan: Engineer1_Script (0DE1003C).

1. Adopt object mission: area guard.

<a id="team-0955cefc"></a>

### TEAM_Start_GIs - 0955CEFC

Owner: Americans. Roster: 2 × Guardian GI (GGI); 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: DC; Transport Waypoint: DB.

Ordered plan: StartGI_Script (0955CC8C).

1. Adopt object mission: area guard.

<a id="team-08d5d5fc"></a>

### TEAM_YuriBarracks_1 - 08D5D5FC

Owner: Arabs. Roster: 1 × Amphibious Transport (YHVR); 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: YuriBarracks_Script (07F7E8EC).

1. Move to waypoint: waypoint 521 (cell 93, 98).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 2 (Make_Hover1).
4. Clear local flag: local flag 4 (Send_Barracks1).
5. Set local flag: local flag 5 (Send_Barracks2).
6. Move to waypoint: waypoint 106 (cell 85, 120).
7. Seek/attack target category; configured argument 1.

<a id="team-08d68b7c"></a>

### TEAM_Hover_TA - 08D68B7C

Owner: Arabs. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TB.

Ordered plan: Hover_TA_Script (0960C2FC).

1. Move to waypoint: waypoint 520 (cell 78, 71).
2. Delete team objects.

<a id="team-08d686cc"></a>

### TEAM_YuriBarracks_2 - 08D686CC

Owner: Arabs. Roster: 5 × Initiate (INIT); 1 × Yuri Clone (YURI); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TC.

Ordered plan: YuriBarracks2_Script (07F7DDBC).

1. Move to waypoint: waypoint 523 (cell 81, 157).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 3 (Make_HoverTD).
4. Clear local flag: local flag 5 (Send_Barracks2).
5. Set local flag: local flag 6 (Send_Barracks3).
6. Move to waypoint: waypoint 107 (cell 87, 127).
7. Seek/attack target category; configured argument 1.

<a id="team-08d6821c"></a>

### TEAM_Hover_TD - 08D6821C

Owner: Arabs. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TD.

Ordered plan: HoverTD_Script (046483DC).

1. Move to waypoint: waypoint 522 (cell 68, 174).
2. Delete team objects.

<a id="team-08d680ec"></a>

### TEAM_YuriBarracks_3 - 08D680EC

Owner: Arabs. Roster: 1 × Lasher Light Tank (LTNK); 2 × Initiate (INIT); 1 × Yuri Clone (YURI); 1 × Brute (BRUTE); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TM.

Ordered plan: YuriBarracks3_Script (07F7D56C).

1. Move to waypoint: waypoint 525 (cell 105, 107).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 7 (Make_HoverTF).
4. Clear local flag: local flag 6 (Send_Barracks3).
5. Set local flag: local flag 8 (Send_Barracks4).
6. Move to waypoint: waypoint 106 (cell 85, 120).
7. Seek/attack target category; configured argument 1.

<a id="team-08d6990c"></a>

### TEAM_HoverTF - 08D6990C

Owner: Arabs. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TF.

Ordered plan: HoverTF_Script (097C5A1C).

1. Move to waypoint: waypoint 532 (cell 171, 67).
2. Delete team objects.

<a id="team-08d6945c"></a>

### TEAM_YuriBarracks_4 - 08D6945C

Owner: Arabs. Roster: 2 × Lasher Light Tank (LTNK); 3 × Initiate (INIT); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TM.

Ordered plan: YuriBarracks4_Script (07F7CA1C).

1. Move to waypoint: waypoint 527 (cell 95, 141).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Clear local flag: local flag 6 (Send_Barracks3).
4. Set local flag: local flag 9 (Make_HoverTH).
5. Set local flag: local flag 22 (Send_Barracks5).
6. Move to waypoint: waypoint 107 (cell 87, 127).
7. Seek/attack target category; configured argument 1.

<a id="team-08d6ad2c"></a>

### TEAM_HoverTH - 08D6AD2C

Owner: Arabs. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TH.

Ordered plan: HoverTH_Script (097C4DBC).

1. Move to waypoint: waypoint 532 (cell 171, 67).
2. Delete team objects.

<a id="team-08d57b5c"></a>

### TEAM_YuriWarFac1 - 08D57B5C

Owner: Confederation. Roster: 2 × Lasher Light Tank (LTNK); 1 × Brute (BRUTE); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TI.

Ordered plan: YuriWarFac1_Script (07F7C1CC).

1. Move to waypoint: waypoint 521 (cell 93, 98).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 16 (Make_HoverTJ).
4. Clear local flag: local flag 10 (Send_WarFac1).
5. Set local flag: local flag 11 (Send_WarFac2).
6. Move to waypoint: waypoint 106 (cell 85, 120).
7. Seek/attack target category; configured argument 1.

<a id="team-08d68c8c"></a>

### TEAM_HoverTJ - 08D68C8C

Owner: Confederation. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TJ.

Ordered plan: HoverTJ_Script (096A2B5C).

1. Move to waypoint: waypoint 528 (cell 83, 66).
2. Delete team objects.

<a id="team-08d6ba4c"></a>

### TEAM_YuriWarFac2 - 08D6BA4C

Owner: Arabs. Roster: 2 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TK.

Ordered plan: YuriWarFac2_Script (07F7B6CC).

1. Move to waypoint: waypoint 531 (cell 85, 158).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 18 (Make_HoverTL).
4. Clear local flag: local flag 11 (Send_WarFac2).
5. Set local flag: local flag 12 (Send_WarFac3).
6. Move to waypoint: waypoint 107 (cell 87, 127).
7. Seek/attack target category; configured argument 1.

<a id="team-08d6b59c"></a>

### TEAM_HoverTL - 08D6B59C

Owner: Arabs. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TL.

Ordered plan: HoverTL_Script (09652DBC).

1. Move to waypoint: waypoint 530 (cell 77, 183).
2. Delete team objects.

<a id="team-0964c97c"></a>

### TEAM_Chrono_MCV - 0964C97C

Owner: Americans. Roster: 1 × Allied Construction Vehicle (AMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AA.

Ordered plan: Chrono_MCV_Script (0964C70C).

1. Adopt object mission: sleep.

<a id="team-08d6cb7c"></a>

### TEAM_YuriWarFac3 - 08D6CB7C

Owner: Arabs. Roster: 2 × Brute (BRUTE); 1 × Yuri Clone (YURI); 1 × Virus (VIRUS); 1 × Gattling Tank (YTNK); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TM.

Ordered plan: YuriWarFac3_Script (07F7A6CC).

1. Move to waypoint: waypoint 533 (cell 103, 102).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 19 (Make_HoverTN).
4. Clear local flag: local flag 12 (Send_WarFac3).
5. Set local flag: local flag 13 (Send_WarFac4).
6. Move to waypoint: waypoint 106 (cell 85, 120).
7. Seek/attack target category; configured argument 1.

<a id="team-08d6c6cc"></a>

### TEAM_HoverTN - 08D6C6CC

Owner: Arabs. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TN.

Ordered plan: HoverTN_Script (0B81213C).

1. Move to waypoint: waypoint 520 (cell 78, 71).
2. Delete team objects.

<a id="team-08d6c21c"></a>

### TEAM_HoverTP - 08D6C21C

Owner: Arabs. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TP.

Ordered plan: HoverTP_Script (0B80918C).

1. Move to waypoint: waypoint 534 (cell 81, 185).
2. Delete team objects.

<a id="team-08d6dc8c"></a>

### TEAM_YuriWarFac4 - 08D6DC8C

Owner: Arabs. Roster: 1 × Gattling Tank (YTNK); 1 × Lasher Light Tank (LTNK); 2 × Brute (BRUTE); 1 × Yuri Clone (YURI); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TO.

Ordered plan: YuriWarFac4_Script (07F796CC).

1. Move to waypoint: waypoint 535 (cell 89, 156).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 20 (Make_HoverTP).
4. Clear local flag: local flag 13 (Send_WarFac4).
5. Set local flag: local flag 14 (Send_WarFac5).
6. Move to waypoint: waypoint 107 (cell 87, 127).
7. Seek/attack target category; configured argument 1.

<a id="team-08d6d6fc"></a>

### TEAM_HoverTR - 08D6D6FC

Owner: Arabs. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TR.

Ordered plan: HoverTR_Script (0B805AFC).

1. Move to waypoint: waypoint 536 (cell 91, 58).
2. Delete team objects.

<a id="team-08d6d18c"></a>

### TEAM_YuriWarFac5 - 08D6D18C

Owner: Arabs. Roster: 2 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TQ.

Ordered plan: YuriWarFac5_Script (07F78B7C).

1. Move to waypoint: waypoint 537 (cell 108, 107).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 21 (Make_HoverTR).
4. Clear local flag: local flag 14 (Send_WarFac5).
5. Set local flag: local flag 10 (Send_WarFac1).
6. Move to waypoint: waypoint 106 (cell 85, 120).
7. Seek/attack target category; configured argument 1.

<a id="team-08d6a1cc"></a>

### TEAM_YuriBarracks5 - 08D6A1CC

Owner: Arabs. Roster: 4 × Initiate (INIT); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TZ; Transport Waypoint: DA.

Ordered plan: YuriBarracks5_Script (07F786CC).

1. Move to waypoint: waypoint 521 (cell 93, 98).
2. Clear local flag: local flag 22 (Send_Barracks5).
3. Set local flag: local flag 4 (Send_Barracks1).
4. Move to waypoint: waypoint 106 (cell 85, 120).
5. Seek/attack target category; configured argument 1.

<a id="team-0b5dda4c"></a>

### Yuri_BA1_8I - 0B5DDA4C

Owner: YuriCountry. Roster: 8 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: YA.

Ordered plan: BA1_8I_Script (095A673C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 1.

<a id="team-0e3297dc"></a>

### Yuri_AntiTank_1 - 0E3297DC

Owner: YuriCountry. Roster: 6 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiTank_1 (0E32956C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 6.
5. Seek/attack target category; configured argument 1.

<a id="team-0e32aefc"></a>

### Yuri_AntiGuardian_1 - 0E32AEFC

Owner: YuriCountry. Roster: 2 × Virus (VIRUS); 2 × Yuri Clone (YURI); 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiGuardian_1 (0E32AC8C).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-092c3efc"></a>

### Yuri_AntiHarvester_1 - 092C3EFC

Owner: YuriCountry. Roster: 3 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK); 2 × Brute (BRUTE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiHarvester_1 (092C3C8C).

1. Seek/attack target category; configured argument 3.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-045cc43c"></a>

### Yuri_AntiHarvester_2 - 045CC43C

Owner: YuriCountry. Roster: 4 × Brute (BRUTE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiHarvester_2 (045CC1CC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 3.
3. Report team success.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-045ca87c"></a>

### Yuri_AntiTank_2 - 045CA87C

Owner: YuriCountry. Roster: 3 × Lasher Light Tank (LTNK); 1 × Master Mind (MIND); 2 × Gattling Tank (YTNK); 2 × Brute (BRUTE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiTank_2 (0CA8C90C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0ca2eb7c"></a>

### Yuri_BD_1 - 0CA2EB7C

Owner: YuriCountry. Roster: 2 × Gattling Tank (YTNK); 3 × Lasher Light Tank (LTNK); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: YA.

Ordered plan: Yuri_BD_1 (0E5EEA1C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-096276ac"></a>

### Yuri_AntiGI_1 - 096276AC

Owner: YuriCountry. Roster: 2 × Virus (VIRUS); 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiGI_1 (095C7DBC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 2.

<a id="team-095c7a7c"></a>

### Yuri_AntiGI_2 - 095C7A7C

Owner: YuriCountry. Roster: 5 × Initiate (INIT); 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiGI_2 (095C780C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-095c750c"></a>

### Yuri_AntiGI_3 - 095C750C

Owner: YuriCountry. Roster: 2 × Gattling Tank (YTNK); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiGI_2 (095C780C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 1.

<a id="team-0ca2da4c"></a>

### Yuri_BD_2 - 0CA2DA4C

Owner: YuriCountry. Roster: 1 × Magnetron (TELE); 2 × Gattling Tank (YTNK); 1 × Virus (VIRUS); 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: YB.

Ordered plan: Yuri_BD_1 (0E5EEA1C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0ca2d80c"></a>

### Yuri_BD_3 - 0CA2D80C

Owner: YuriCountry. Roster: 2 × Gattling Tank (YTNK); 4 × Brute (BRUTE); 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: YC.

Ordered plan: Yuri_BD_1 (0E5EEA1C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0963594c"></a>

### Yuri_BA_2 - 0963594C

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_BA_2 (0965BC8C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 35 (cell 177, 192).
3. Move to waypoint: waypoint 36 (cell 160, 205).
4. Move to waypoint: waypoint 37 (cell 131, 196).
5. Move to waypoint: waypoint 38 (cell 121, 208).
6. Seek/attack target category; configured argument 6.
7. Report team success.
8. Seek/attack target category; configured argument 2.
9. Seek/attack target category; configured argument 1.

<a id="team-0958594c"></a>

### Yuri_BA_Soviet_1 - 0958594C

Owner: YuriCountry. Roster: 3 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK); 1 × Master Mind (MIND); 1 × Magnetron (TELE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_BA_2 (0965BC8C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 35 (cell 177, 192).
3. Move to waypoint: waypoint 36 (cell 160, 205).
4. Move to waypoint: waypoint 37 (cell 131, 196).
5. Move to waypoint: waypoint 38 (cell 121, 208).
6. Seek/attack target category; configured argument 6.
7. Report team success.
8. Seek/attack target category; configured argument 2.
9. Seek/attack target category; configured argument 1.

<a id="team-095cd19c"></a>

### Yuri_AntiSW_Allied_1 - 095CD19C

Owner: YuriCountry. Roster: 1 × Master Mind (MIND); 3 × Gattling Tank (YTNK); 3 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiSW_Allied_1 (08C446CC).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 35 (cell 177, 192).
3. Move to waypoint: waypoint 36 (cell 160, 205).
4. Move to waypoint: waypoint 37 (cell 131, 196).
5. Move to waypoint: waypoint 38 (cell 121, 208).
6. Attack selected enemy-building category; configured argument 131099.
7. Attack selected enemy-building category; configured argument 131101.
8. Report team success.
9. Seek/attack target category; configured argument 1.

<a id="team-095f68ec"></a>

### Yuri_AntiTank_Allied_2 - 095F68EC

Owner: YuriCountry. Roster: 5 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiTank_1 (0E32956C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 6.
5. Seek/attack target category; configured argument 1.

<a id="team-0e60477c"></a>

### Yuri_AntiGuardian_2 - 0E60477C

Owner: YuriCountry. Roster: 3 × Gattling Tank (YTNK); 2 × Virus (VIRUS); 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiGuardian_1 (0E32AC8C).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-09590b8c"></a>

### Yuri_AntiPrism_1 - 09590B8C

Owner: YuriCountry. Roster: 4 × Lasher Light Tank (LTNK); 1 × Chaos Drone (CAOS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiPrism_1 (0959091C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-06c71efc"></a>

### Yuri_AntiTank_Soviet_2 - 06C71EFC

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK); 3 × Brute (BRUTE); 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiTank_2 (0CA8C90C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-06c2694c"></a>

### Yuri_BA_3 - 06C2694C

Owner: YuriCountry. Roster: 3 × Initiate (INIT); 1 × Yuri Clone (YURI); 2 × Gattling Tank (YTNK); 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_BA_2 (0965BC8C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 35 (cell 177, 192).
3. Move to waypoint: waypoint 36 (cell 160, 205).
4. Move to waypoint: waypoint 37 (cell 131, 196).
5. Move to waypoint: waypoint 38 (cell 121, 208).
6. Seek/attack target category; configured argument 6.
7. Report team success.
8. Seek/attack target category; configured argument 2.
9. Seek/attack target category; configured argument 1.

<a id="team-0e67c21c"></a>

### Yuri_Allied_Barracks_1 - 0E67C21C

Owner: YuriCountry. Roster: 5 × Initiate (INIT); 1 × Yuri Clone (YURI); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RA.

Ordered plan: Engineer1_Script (0DE1003C).

1. Adopt object mission: area guard.

<a id="team-0d29367c"></a>

### Yuri_EngineerRush_1 - 0D29367C

Owner: YuriCountry. Roster: 1 × Yuri Clone (YURI); 1 × Virus (VIRUS); 2 × Engineer (YENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: EngineerRush_1 (0D29340C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 131072.
4. Report team success.
5. Attack selected enemy-building category; configured argument 131075.
6. Attack selected enemy-building category; configured argument 131079.

<a id="team-04e3aa8c"></a>

### TEAM_Chrono_Grizzly1 - 04E3AA8C

Owner: Americans. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: Chrono_MCV_Script (0964C70C).

1. Adopt object mission: sleep.

<a id="team-04e3a75c"></a>

### TEAM_Chrono_Grizzly2 - 04E3A75C

Owner: Americans. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AC.

Ordered plan: Chrono_MCV_Script (0964C70C).

1. Adopt object mission: sleep.

<a id="team-04e39a4c"></a>

### TEAM_Chrono_Mirage1 - 04E39A4C

Owner: Americans. Roster: 1 × Mirage Tank (MGTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: Chrono_MCV_Script (0964C70C).

1. Adopt object mission: sleep.

<a id="team-04e403bc"></a>

### TEAM_Chrono_IFV1 - 04E403BC

Owner: Americans. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AE.

Ordered plan: Chrono_MCV_Script (0964C70C).

1. Adopt object mission: sleep.

<a id="team-04e4028c"></a>

### TEAM_Chrono_Prism1 - 04E4028C

Owner: Americans. Roster: 1 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: Chrono_MCV_Script (0964C70C).

1. Adopt object mission: sleep.

<a id="team-04e4077c"></a>

### TEAM_Chrono_IFV2 - 04E4077C

Owner: Americans. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AG.

Ordered plan: Chrono_MCV_Script (0964C70C).

1. Adopt object mission: sleep.

<a id="team-04e4064c"></a>

### TEAM_Chrono_Mirage2 - 04E4064C

Owner: Americans. Roster: 1 × Mirage Tank (MGTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AH.

Ordered plan: Chrono_MCV_Script (0964C70C).

1. Adopt object mission: sleep.

<a id="team-04e40b3c"></a>

### TEAM_Chrono_Grizzly3 - 04E40B3C

Owner: Americans. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AI.

Ordered plan: Chrono_MCV_Script (0964C70C).

1. Adopt object mission: sleep.

<a id="team-0bc207dc"></a>

### Yuri_Floater1 - 0BC207DC

Owner: YuriCountry. Roster: 2 × Floating Disc (DISK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Floater1 (08D6ADBC).

1. Seek/attack target category; configured argument 7.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-0ca2993c"></a>

### Yuri_Mastermind1 - 0CA2993C

Owner: YuriCountry. Roster: 1 × Master Mind (MIND); 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Mastermind1 (06BCF49C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0ca2948c"></a>

### Yuri_Mastermind2 - 0CA2948C

Owner: YuriCountry. Roster: 2 × Master Mind (MIND); 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Mastermind2 (095E725C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 1.

<a id="team-045e7d5c"></a>

### Yuri_Floater2 - 045E7D5C

Owner: YuriCountry. Roster: 1 × Floating Disc (DISK); 2 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Floater2 (08D6BDBC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-045e579c"></a>

### Yuri_Infantry1 - 045E579C

Owner: YuriCountry. Roster: 5 × Initiate (INIT); 1 × Virus (VIRUS); 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Infantry1 (045E6DBC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 1.
3. Report team success.

<a id="team-09321c8c"></a>

### Africa_BD1 - 09321C8C

Owner: Yuri2Country. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 1 × Magnetron (TELE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: EA.

Ordered plan: Africa_BD1 (098AA6CC).

1. Adopt object mission: area guard.

<a id="team-093217dc"></a>

### Africa_BD2 - 093217DC

Owner: Yuri2Country. Roster: 2 × Lasher Light Tank (LTNK); 1 × Magnetron (TELE); 1 × Master Mind (MIND); 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: EB.

Ordered plan: Africa_BD2 (098A6B0C).

1. Adopt object mission: area guard.

<a id="team-0932132c"></a>

### Africa_BD3 - 0932132C

Owner: Yuri2Country. Roster: 2 × Yuri Clone (YURI); 1 × Magnetron (TELE); 1 × Master Mind (MIND); 3 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: EC.

Ordered plan: Africa_BD3 (04F3034C).

1. Adopt object mission: area guard.

<a id="team-09327b7c"></a>

### Africa_AntiInfantry1 - 09327B7C

Owner: Yuri2Country. Roster: 2 × Virus (VIRUS); 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_AntiInfantry1 (04F2211C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-093276cc"></a>

### Africa_AntiInfantry2 - 093276CC

Owner: Yuri2Country. Roster: 2 × Gattling Tank (YTNK); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_AntiInfantry2 (04F1833C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-09324efc"></a>

### Africa_AntiInfantry3 - 09324EFC

Owner: Yuri2Country. Roster: 1 × Virus (VIRUS); 1 × Yuri Clone (YURI); 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_AntiInfantry3 (04F1F56C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-09324a4c"></a>

### Africa_AntiTank1 - 09324A4C

Owner: Yuri2Country. Roster: 4 × Lasher Light Tank (LTNK); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_AntiTank1 (04F27DBC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 8.
5. Seek/attack target category; configured argument 1.

<a id="team-0932459c"></a>

### Africa_AntiTank2 - 0932459C

Owner: Yuri2Country. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 1 × Magnetron (TELE); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_AntiTank2 (04F2771C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-09322dec"></a>

### Africa_AntiTank3 - 09322DEC

Owner: Yuri2Country. Roster: 5 × Lasher Light Tank (LTNK); 1 × Magnetron (TELE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_AntiTank3 (04F271EC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 6.
5. Seek/attack target category; configured argument 1.

<a id="team-0932293c"></a>

### Africa_AntiTank4 - 0932293C

Owner: Yuri2Country. Roster: 3 × Brute (BRUTE); 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_AntiTank4 (04F25A9C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0932248c"></a>

### Africa_BA1 - 0932248C

Owner: Yuri2Country. Roster: 3 × Lasher Light Tank (LTNK); 1 × Magnetron (TELE); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_BA1 (04F255FC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Report team success.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 1.

<a id="team-09325c8c"></a>

### Africa_BA2 - 09325C8C

Owner: Yuri2Country. Roster: 2 × Yuri Clone (YURI); 3 × Gattling Tank (YTNK); 3 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_BA2 (04F2299C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 2.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-093257dc"></a>

### Africa_BA3 - 093257DC

Owner: Yuri2Country. Roster: 1 × Master Mind (MIND); 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 1 × Magnetron (TELE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Africa_BA3 (04F2253C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 6.
3. Report team success.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-0965042c"></a>

### BioReactor_Men1 - 0965042C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BA.

Ordered plan: BioReactor_Men1 (09655DBC).

1. Enter Bio Reactor.

<a id="team-09654d7c"></a>

### BioReactor_Men2 - 09654D7C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BB.

Ordered plan: BioReactor_Men1 (09655DBC).

1. Enter Bio Reactor.

<a id="team-09654c4c"></a>

### BioReactor_Men3 - 09654C4C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: BioReactor_Men1 (09655DBC).

1. Enter Bio Reactor.

<a id="team-09654b1c"></a>

### BioReactor_Men4 - 09654B1C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BD.

Ordered plan: BioReactor_Men1 (09655DBC).

1. Enter Bio Reactor.

<a id="team-08e9634c"></a>

### Yuri_Floater3 - 08E9634C

Owner: YuriCountry. Roster: 2 × Floating Disc (DISK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Floater2 (08D6BDBC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-09f9967c"></a>

### Yuri_AntiIFV1 - 09F9967C

Owner: YuriCountry. Roster: 4 × Lasher Light Tank (LTNK); 1 × Master Mind (MIND); 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiIFV1 (09F9CDBC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 1.

<a id="team-092e55ac"></a>

### Africa_AntiIFV1 - 092E55AC

Owner: Yuri2Country. Roster: 4 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiIFV1 (09F9CDBC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 1.

<a id="team-090af55c"></a>

### Yuri_PrismCheese_Team - 090AF55C

Owner: YuriCountry. Roster: 2 × Master Mind (MIND); 2 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AN.

Ordered plan: PrismCheese_Script (090AD6DC).

1. Move to waypoint: waypoint 40 (cell 195, 121).
2. Move to waypoint: waypoint 41 (cell 170, 110).
3. Move to waypoint: waypoint 40 (cell 195, 121).
4. Move to waypoint: waypoint 39 (cell 210, 144).
5. Jump to script line; configured argument 1.

<a id="team-0905becc"></a>

### Africa_AntiPCannon - 0905BECC

Owner: Yuri2Country. Roster: 3 × Magnetron (TELE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Anti_PCannon (0905BC5C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Report team success.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-079cc70c"></a>

### Yuri_BA_4 - 079CC70C

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK); 2 × Magnetron (TELE); 2 × Gattling Tank (YTNK); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_BA_2 (0965BC8C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 35 (cell 177, 192).
3. Move to waypoint: waypoint 36 (cell 160, 205).
4. Move to waypoint: waypoint 37 (cell 131, 196).
5. Move to waypoint: waypoint 38 (cell 121, 208).
6. Seek/attack target category; configured argument 6.
7. Report team success.
8. Seek/attack target category; configured argument 2.
9. Seek/attack target category; configured argument 1.

<a id="team-079ce8ec"></a>

### Yuri_SovietBA_2 - 079CE8EC

Owner: YuriCountry. Roster: 1 × Floating Disc (DISK); 1 × Magnetron (TELE); 1 × Gattling Tank (YTNK); 3 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_BA_2 (0965BC8C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 35 (cell 177, 192).
3. Move to waypoint: waypoint 36 (cell 160, 205).
4. Move to waypoint: waypoint 37 (cell 131, 196).
5. Move to waypoint: waypoint 38 (cell 121, 208).
6. Seek/attack target category; configured argument 6.
7. Report team success.
8. Seek/attack target category; configured argument 2.
9. Seek/attack target category; configured argument 1.

<a id="team-08d7135c"></a>

### Yuri3_BA_1 - 08D7135C

Owner: Yuri3Country. Roster: 2 × Magnetron (TELE); 2 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_BA_1 (0A3D611C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 7.
4. Report team success.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-08d72dec"></a>

### Yuri3_BA_2 - 08D72DEC

Owner: Yuri3Country. Roster: 4 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_BA_2 (09732C2C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 9.
4. Report team success.
5. Seek/attack target category; configured argument 1.

<a id="team-08d7293c"></a>

### Yuri3_BA_3 - 08D7293C

Owner: Yuri3Country. Roster: 1 × Floating Disc (DISK); 1 × Magnetron (TELE); 1 × Master Mind (MIND); 2 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_BA_1 (0A3D611C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 7.
4. Report team success.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-08d726fc"></a>

### Yuri3_BA_4 - 08D726FC

Owner: Yuri3Country. Roster: 3 × Magnetron (TELE); 1 × Master Mind (MIND); 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_BA_2 (09732C2C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 9.
4. Report team success.
5. Seek/attack target category; configured argument 1.

<a id="team-0973262c"></a>

### Yuri3_Irritate_1 - 0973262C

Owner: Yuri3Country. Roster: 8 × Initiate (INIT); 2 × Yuri Clone (YURI); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_Irritate_1 (097323BC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 6.
4. Report team success.
5. Seek/attack target category; configured argument 1.

<a id="team-09731e7c"></a>

### Yuri3_Irritate_2 - 09731E7C

Owner: Yuri3Country. Roster: 5 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_Irritate_2 (09731C0C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 2.
4. Report team success.
5. Seek/attack target category; configured argument 1.

<a id="team-097314ec"></a>

### Yuri3_Irritate_3 - 097314EC

Owner: Yuri3Country. Roster: 4 × Brute (BRUTE); 1 × Virus (VIRUS); 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_BA_1 (0A3D611C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 7.
4. Report team success.
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-09736efc"></a>

### Yuri3_Irritate_4 - 09736EFC

Owner: Yuri3Country. Roster: 4 × Initiate (INIT); 2 × Yuri Clone (YURI); 1 × Virus (VIRUS); 2 × Brute (BRUTE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_Irritate_2 (09731C0C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 2.
4. Report team success.
5. Seek/attack target category; configured argument 1.

<a id="team-09736dcc"></a>

### Yuri3_AntiChrono_1 - 09736DCC

Owner: Yuri3Country. Roster: 3 × Magnetron (TELE); 2 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_AntiSW_1 (09736B5C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 131099.
4. Report team success.
5. Seek/attack target category; configured argument 1.

<a id="team-09735e1c"></a>

### Yuri3_AntiIron_1 - 09735E1C

Owner: Yuri3Country. Roster: 4 × Lasher Light Tank (LTNK); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_AntiIron_1 (09735BAC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 131096.
4. Report team success.
5. Seek/attack target category; configured argument 1.

<a id="team-097358ac"></a>

### Yuri3_AntiChrono_2 - 097358AC

Owner: Yuri3Country. Roster: 4 × Lasher Light Tank (LTNK); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_AntiSW_1 (09736B5C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 131099.
4. Report team success.
5. Seek/attack target category; configured argument 1.

<a id="team-0973577c"></a>

### Yuri3_AntiIron_2 - 0973577C

Owner: Yuri3Country. Roster: 3 × Magnetron (TELE); 2 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_AntiIron_1 (09735BAC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 131096.
4. Report team success.
5. Seek/attack target category; configured argument 1.

<a id="team-092f5efc"></a>

### Yuri3_AQ_Engineer - 092F5EFC

Owner: Yuri3Country. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AQ.

Ordered plan: Yuri3_AQ_Engineer (092F5C8C).

1. Attack/garrison waypoint building: waypoint 43 (cell 142, 228).

<a id="team-092f59dc"></a>

### Yuri3_AT_Engineer - 092F59DC

Owner: Yuri3Country. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AT.

Ordered plan: Yuri3_AT_Engineer (092F576C).

1. Attack/garrison waypoint building: waypoint 44 (cell 142, 232).

<a id="team-095042ec"></a>

### Yuri3_BD_1 - 095042EC

Owner: Yuri3Country. Roster: 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_BD_Script (04613DBC).

1. Gather near own base; configured argument 0.
2. Adopt object mission: area guard.

<a id="team-09509b7c"></a>

### Yuri3_BD_2 - 09509B7C

Owner: Yuri3Country. Roster: 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_BD_Script (04613DBC).

1. Gather near own base; configured argument 0.
2. Adopt object mission: area guard.

<a id="team-0950993c"></a>

### Yuri3_BD_3 - 0950993C

Owner: Yuri3Country. Roster: 1 × Magnetron (TELE); 1 × Master Mind (MIND)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri3_BD_Script (04613DBC).

1. Gather near own base; configured argument 0.
2. Adopt object mission: area guard.

<a id="team-050fee1c"></a>

### Yuri_AntiTank3 - 050FEE1C

Owner: YuriCountry. Roster: 3 × Brute (BRUTE); 2 × Gattling Tank (YTNK); 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiTank3 (050FEBAC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 6.
5. Seek/attack target category; configured argument 1.

<a id="team-094e907c"></a>

### Yuri_AntiRT_1 - 094E907C

Owner: YuriCountry. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiRT_Script (0951603C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0951318c"></a>

### Yuri_AntiRT_2 - 0951318C

Owner: YuriCountry. Roster: 6 × Initiate (INIT); 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiRT_Script (0951603C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0951305c"></a>

### Yuri_AntiRT_3 - 0951305C

Owner: YuriCountry. Roster: 4 × Initiate (INIT); 4 × Brute (BRUTE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiRT_Script (0951603C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0951809c"></a>

### Yuri2_AntiRT_1 - 0951809C

Owner: Yuri2Country. Roster: 4 × Initiate (INIT); 4 × Brute (BRUTE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiRT_Script (0951603C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0951ec5c"></a>

### Yuri3_AntiRT_1 - 0951EC5C

Owner: Yuri3Country. Roster: 4 × Initiate (INIT); 4 × Brute (BRUTE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_AntiRT_Script (0951603C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0900e65c"></a>

### Yuri2_Garrison1 - 0900E65C

Owner: Yuri2Country. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BE.

Ordered plan: Yuri2_Garrison (0900EDBC).

1. Enter Bio Reactor.

<a id="team-0900b27c"></a>

### Yuri2_Garrison2 - 0900B27C

Owner: Yuri2Country. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BF.

Ordered plan: Yuri2_Garrison (0900EDBC).

1. Enter Bio Reactor.

<a id="team-08ffe99c"></a>

### BioReactor_Men5 - 08FFE99C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BG.

Ordered plan: BioReactor_Men1 (09655DBC).

1. Enter Bio Reactor.

<a id="team-08ffec1c"></a>

### BioReactor_Men6 - 08FFEC1C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BH.

Ordered plan: BioReactor_Men1 (09655DBC).

1. Enter Bio Reactor.

<a id="team-07ab65cc"></a>

### Yuri_Boomer_Solo - 07AB65CC

Owner: YuriCountry. Roster: 1 × Boomer (BSUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TG.

Ordered plan: Boomer_Solo (07AB0DBC).

1. Attack selected enemy-building category; configured argument 131095.
2. Seek/attack target category; configured argument 1.

<a id="team-08ffb35c"></a>

### Africa_Floater1 - 08FFB35C

Owner: Yuri2Country. Roster: 2 × Floating Disc (DISK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Floater1 (08D6ADBC).

1. Seek/attack target category; configured argument 7.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-05ed7efc"></a>

### Africa_AntiTesla01 - 05ED7EFC

Owner: Yuri2Country. Roster: 3 × Magnetron (TELE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Anti_PCannon (0905BC5C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Report team success.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-05ed248c"></a>

### Yuri_AntiTesla01 - 05ED248C

Owner: YuriCountry. Roster: 3 × Magnetron (TELE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Anti_PCannon (0905BC5C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 7.
3. Report team success.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-05e12d5c"></a>

### Yuri_TierraFloater01 - 05E12D5C

Owner: Yuri2Country. Roster: 2 × Floating Disc (DISK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: TierraFloater_SCR (08D771EC).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 106 (cell 85, 120).
3. Seek/attack target category; configured argument 7.
4. Report team success.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 1.

<a id="team-05e1257c"></a>

### Africa_TierraFloater01 - 05E1257C

Owner: Yuri2Country. Roster: 2 × Floating Disc (DISK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: TierraFloater_SCR (08D771EC).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 106 (cell 85, 120).
3. Seek/attack target category; configured argument 7.
4. Report team success.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 1.

<a id="team-08d9b58c"></a>

### Yuri_Prime_Grizzly - 08D9B58C

Owner: Yuri2Country. Roster: 2 × Master Mind (MIND); 1 × Yuri Prime (YURIPR); 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Prime_Grizzly (0941A5AC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 5.
7. Seek/attack target category; configured argument 4.

<a id="team-08d9b0dc"></a>

### Yuri_Prime_Rhino - 08D9B0DC

Owner: Yuri2Country. Roster: 2 × Master Mind (MIND); 1 × Yuri Prime (YURIPR); 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Prime_Grizzly (0941A5AC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 5.
7. Seek/attack target category; configured argument 4.

<a id="team-04f46bbc"></a>

### Africa_TierraFloater_Easy - 04F46BBC

Owner: Yuri3Country. Roster: 1 × Floating Disc (DISK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: TierraFloater_SCR (08D771EC).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 106 (cell 85, 120).
3. Seek/attack target category; configured argument 7.
4. Report team success.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 1.

<a id="team-04f46a8c"></a>

### Yuri_Floater_Easy - 04F46A8C

Owner: YuriCountry. Roster: 1 × Floating Disc (DISK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri_Floater1 (08D6ADBC).

1. Seek/attack target category; configured argument 7.
2. Report team success.
3. Seek/attack target category; configured argument 1.
