# Operation: Power Play - team rosters and plans

[Trigger ledger](all03umd.md) | [Mission overrides](all03umd-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: mapsmd03.mix/all03umd.map; each team/script ID identifies its section.

<a id="team-0b50a68c"></a>

### TEAM_Yuri_PP1 - 0B50A68C

Owner: Russians. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 4 × Initiate (INIT); 2 × Yuri Clone (YURI); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: TA_Guard_Gatt1 (0C767DBC).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 471 (cell 103, 57).
3. Adopt object mission: guard.

<a id="team-093c248c"></a>

### TEAM_Yuri_PP2 - 093C248C

Owner: Nod. Roster: 4 × Initiate (INIT); 2 × Yuri Clone (YURI); 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TB.

Ordered plan: Yuri_PP2_Start (0BA1DDBC).

1. Adopt object mission: area guard.

<a id="team-093df0bc"></a>

### TEAM_Yuri_PP3 - 093DF0BC

Owner: Confederation. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 4 × Initiate (INIT); 2 × Yuri Clone (YURI); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: TC.

Ordered plan: Yuri_PP3_Start (09418DBC).

1. Adopt object mission: area guard.

<a id="team-0be791bc"></a>

### TEAM_AB_GI - 0BE791BC

Owner: Americans. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_GI_Script (0BE79B7C).

1. Deploy.

<a id="team-0b3e926c"></a>

### TEAM_Yuri_TA_Attack - 0B3E926C

Owner: Russians. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 4 × Initiate (INIT); 2 × Yuri Clone (YURI); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba3c0ec"></a>

### TEAM_AA_Engineer - 0BA3C0EC

Owner: Russians. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: EA; Transport Waypoint: PA.

Ordered plan: AA_Engineer_Script (0CCEB6CC).

1. Attack waypoint: waypoint 26 (cell 116, 73).
2. Seek/attack target category; configured argument 9.

<a id="team-0b3736cc"></a>

### TEAM_TB_Reinforce - 0B3736CC

Owner: Russians. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 4 × Initiate (INIT); 2 × Yuri Clone (YURI); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RB.

Ordered plan: TB_Reinforce_Script (06B3B36C).

1. Attack-move toward waypoint: waypoint 183 (cell 94, 73).
2. Adopt object mission: area guard.

<a id="team-0d3c66fc"></a>

### TEAM_TB_Become_TA - 0D3C66FC

Owner: Russians. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 4 × Initiate (INIT); 2 × Yuri Clone (YURI); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: GB.

Ordered plan: TB_Become_TA_Script (06B3BDBC).

1. Attack-move toward waypoint: waypoint 182 (cell 103, 62).
2. Adopt object mission: area guard.
3. Set local flag: local flag 10 (Nuked_PPTA).

<a id="team-094c815c"></a>

### TEAM_Yuri_TC_Attack - 094C815C

Owner: Confederation. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 4 × Initiate (INIT); 2 × Yuri Clone (YURI); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TC.

Ordered plan: TB_Attack_Script (094C9DBC).

1. Seek/attack target category; configured argument 0.

<a id="team-094cab1c"></a>

### TEAM_Yuri_TD_Attack - 094CAB1C

Owner: Arabs. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TD.

Ordered plan: Yuri_TD_Attack_Script (094CA8AC).

1. Attack-move toward waypoint: waypoint 133 (cell 120, 122).
2. Adopt object mission: area guard.
3. Clear local flag: local flag 13 (Nuked_MA).

<a id="team-094cb1ac"></a>

### TEAM_Yuri_PP4 - 094CB1AC

Owner: Arabs. Roster: 3 × Lasher Light Tank (LTNK); 2 × Gattling Tank (YTNK); 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TD.

Ordered plan: Yuri_PP4_Defend (0B1F6B4C).

1. Adopt object mission: guard.

<a id="team-06af927c"></a>

### TEAM_Dog1 - 06AF927C

Owner: Americans. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: HE.

Ordered plan: Dog1_Script (0953956C).

1. Move to waypoint: waypoint 208 (cell 167, 110).
2. Set local flag: local flag 19 (Kill_GI).

<a id="team-0954011c"></a>

### TEAM_Dog2 - 0954011C

Owner: Americans. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: HF.

Ordered plan: Dog2_Script (0A95845C).

1. Move to waypoint: waypoint 209 (cell 164, 107).
2. Set local flag: local flag 20 (Kill_GI_HF).

<a id="team-06afe7dc"></a>

### TEAM_Dog3 - 06AFE7DC

Owner: Americans. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: HG.

Ordered plan: Dog3_Script (0A959DBC).

1. Move to waypoint: waypoint 210 (cell 157, 101).
2. Set local flag: local flag 21 (Kill_GI_HG).

<a id="team-0b24c21c"></a>

### TEAM_Dog4 - 0B24C21C

Owner: Americans. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: HH.

Ordered plan: Dog4_Script (0A95990C).

1. Move to waypoint: waypoint 211 (cell 152, 96).
2. Set local flag: local flag 22 (Kill_GI_HH).

<a id="team-04e50efc"></a>

### TEAM_Dog5 - 04E50EFC

Owner: Americans. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: HI.

Ordered plan: Dog5_Script (04E5408C).

1. Move to waypoint: waypoint 218 (cell 147, 90).
2. Set local flag: local flag 23 (Kill_GI_HI).

<a id="team-0948fefc"></a>

### TEAM_Dog6 - 0948FEFC

Owner: Americans. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: HJ.

Ordered plan: Dog6_Script (0949393C).

1. Move to waypoint: waypoint 219 (cell 140, 84).
2. Set local flag: local flag 24 (Kill_GI_HJ).

<a id="team-0da0f32c"></a>

### TEAM_TA_Lasher1 - 0DA0F32C

Owner: Russians. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RA.

Ordered plan: TA_Guard_Lasher1 (0C7600AC).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 468 (cell 103, 61).
3. Adopt object mission: area guard.

<a id="team-0da10efc"></a>

### TEAM_TA_Lasher2 - 0DA10EFC

Owner: Russians. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RC.

Ordered plan: TA_Guard_Lasher2 (0C77599C).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 470 (cell 104, 59).
3. Adopt object mission: area guard.

<a id="team-0da10cbc"></a>

### TEAM_TA_Lasher3 - 0DA10CBC

Owner: Russians. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RH.

Ordered plan: TA_Guard_Lasher3 (0C7754BC).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 475 (cell 101, 61).
3. Adopt object mission: area guard.

<a id="team-0da10a7c"></a>

### TEAM_TA_Gatt1 - 0DA10A7C

Owner: Russians. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RD.

Ordered plan: TA_Guard_Gatt1 (0C767DBC).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 471 (cell 103, 57).
3. Adopt object mission: guard.

<a id="team-0da1083c"></a>

### TEAM_TA_Gatt2 - 0DA1083C

Owner: Russians. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RG.

Ordered plan: TA_Guard_Gatt2 (0C77315C).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 474 (cell 101, 56).
3. Adopt object mission: area guard.

<a id="team-0da105fc"></a>

### TEAM_TA_Init1 - 0DA105FC

Owner: Russians. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RI.

Ordered plan: TA_Guard_Init1 (0C770DBC).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 476 (cell 99, 61).
3. Adopt object mission: area guard.

<a id="team-0da103bc"></a>

### TEAM_TA_Init2 - 0DA103BC

Owner: Russians. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RJ.

Ordered plan: TA_Guard_Init2 (0C770A1C).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 477 (cell 99, 60).
3. Adopt object mission: area guard.

<a id="team-0da1017c"></a>

### TEAM_TA_Init3 - 0DA1017C

Owner: Russians. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RK.

Ordered plan: TA_Guard_Init3 (0C77067C).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 478 (cell 99, 59).
3. Adopt object mission: area guard.

<a id="team-0da11dec"></a>

### TEAM_TA_Init4 - 0DA11DEC

Owner: Russians. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RL.

Ordered plan: TA_Guard_Init4 (0C7701CC).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 479 (cell 99, 58).
3. Adopt object mission: area guard.

<a id="team-0da11bac"></a>

### TEAM_TA_Yuri1 - 0DA11BAC

Owner: Russians. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RE.

Ordered plan: TA_Guard_Yuri1 (0C777C8C).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 472 (cell 102, 55).
3. Adopt object mission: area guard.

<a id="team-0da1196c"></a>

### TEAM_TA_Yuri2 - 0DA1196C

Owner: Russians. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RF.

Ordered plan: TA_Guard_Yuri2 (0C7777DC).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 473 (cell 100, 55).
3. Adopt object mission: area guard.

<a id="team-0da1172c"></a>

### TEAM_TA_Virus1 - 0DA1172C

Owner: Russians. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RB.

Ordered plan: TA_Guard_Virus (0C77732C).

1. Clear local flag: local flag 46 (Russia_Gone).
2. Move to waypoint: waypoint 469 (cell 104, 60).
3. Adopt object mission: guard.

<a id="team-0ba253bc"></a>

### TEAM_AA_Gatt1 - 0BA253BC

Owner: Africans. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba2528c"></a>

### TEAM_AA_Gatt2 - 0BA2528C

Owner: Africans. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba2515c"></a>

### TEAM_AA_Init1 - 0BA2515C

Owner: Africans. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba26efc"></a>

### TEAM_AA_Init2 - 0BA26EFC

Owner: Africans. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba26dcc"></a>

### TEAM_AA_Init3 - 0BA26DCC

Owner: Africans. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba26c9c"></a>

### TEAM_AA_Init4 - 0BA26C9C

Owner: Africans. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba26b6c"></a>

### TEAM_AA_Lasher1 - 0BA26B6C

Owner: Africans. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba26a3c"></a>

### TEAM_AA_Lasher2 - 0BA26A3C

Owner: Africans. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba2690c"></a>

### TEAM_AA_Lasher3 - 0BA2690C

Owner: Africans. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba267dc"></a>

### TEAM_AA_Yuri1 - 0BA267DC

Owner: Africans. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba266ac"></a>

### TEAM_AA_Yuri2 - 0BA266AC

Owner: Africans. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0ba2657c"></a>

### TEAM_AA_Virus - 0BA2657C

Owner: Africans. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA.

Ordered plan: Yuri_TA_AA_Attack (0C1FB21C).

1. Set local flag: local flag 7 (Engineer_AA).
2. Move to waypoint: waypoint 130 (cell 112, 69).
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Adopt object mission: area guard.

<a id="team-0afc2dcc"></a>

### TEAM_TB_Gatt1 - 0AFC2DCC

Owner: Nod. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SD.

Ordered plan: TB_Guard_Gatt1 (0C772DBC).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 497 (cell 93, 74).
3. Adopt object mission: area guard.

<a id="team-0afc322c"></a>

### TEAM_TB_Gatt2 - 0AFC322C

Owner: Nod. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SE.

Ordered plan: TB_Guard_Gatt2 (0C772A1C).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 498 (cell 93, 72).
3. Adopt object mission: area guard.

<a id="team-0afc4efc"></a>

### TEAM_TB_Init1 - 0AFC4EFC

Owner: Nod. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SI.

Ordered plan: TB_Guard_Init1 (0C77256C).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 502 (cell 91, 70).
3. Adopt object mission: area guard.

<a id="team-0afc4cbc"></a>

### TEAM_TB_Init2 - 0AFC4CBC

Owner: Nod. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: SJ.

Ordered plan: TB_Guard_Init2 (0C7720BC).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 503 (cell 91, 69).
3. Adopt object mission: area guard.

<a id="team-0afc4a7c"></a>

### TEAM_TB_Init3 - 0AFC4A7C

Owner: Nod. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SK.

Ordered plan: TB_Guard_Init3 (0C78BC8C).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 504 (cell 93, 71).
3. Adopt object mission: area guard.

<a id="team-0afc483c"></a>

### TEAM_TB_Init4 - 0AFC483C

Owner: Nod. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SL.

Ordered plan: TB_Guard_Init4 (0C78B7DC).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 505 (cell 93, 68).
3. Adopt object mission: area guard.

<a id="team-0afc45fc"></a>

### TEAM_TB_Lasher1 - 0AFC45FC

Owner: Nod. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SA.

Ordered plan: TB_Guard_Lasher1 (0C78DC8C).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 494 (cell 95, 75).
3. Adopt object mission: area guard.

<a id="team-0afc43bc"></a>

### TEAM_TB_Lasher2 - 0AFC43BC

Owner: Nod. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SB.

Ordered plan: TB_Guard_Lasher2 (0C78D7DC).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 495 (cell 95, 73).
3. Adopt object mission: area guard.

<a id="team-0afc417c"></a>

### TEAM_TB_Lasher3 - 0AFC417C

Owner: Nod. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SC.

Ordered plan: TB_Guard_Lasher3 (0C78D32C).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 496 (cell 95, 71).
3. Adopt object mission: area guard.

<a id="team-0afc372c"></a>

### TEAM_TB_Virus - 0AFC372C

Owner: Nod. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SF.

Ordered plan: TB_Guard_Virus (0C78C93C).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 499 (cell 89, 70).
3. Adopt object mission: area guard.

<a id="team-0afc34ec"></a>

### TEAM_TB_Yuri1 - 0AFC34EC

Owner: Nod. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SG.

Ordered plan: TB_Guard_Yuri1 (0C78C48C).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 500 (cell 89, 69).
3. Adopt object mission: area guard.

<a id="team-0afc59ac"></a>

### TEAM_TB_Yuri2 - 0AFC59AC

Owner: Nod. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SH.

Ordered plan: TB_Guard_Yuri2 (0C78EDBC).

1. Clear local flag: local flag 45 (Nod_Gone).
2. Move to waypoint: waypoint 501 (cell 89, 68).
3. Adopt object mission: area guard.

<a id="team-0950e09c"></a>

### TEAM_French_Gatt1 - 0950E09C

Owner: French. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095a805c"></a>

### TEAM_French_Gatt2 - 095A805C

Owner: French. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095aa06c"></a>

### TEAM_French_Init1 - 095AA06C

Owner: French. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095ad13c"></a>

### TEAM_French_Init2 - 095AD13C

Owner: French. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095af13c"></a>

### TEAM_French_Init3 - 095AF13C

Owner: French. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095ab13c"></a>

### TEAM_French_Init4 - 095AB13C

Owner: French. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-0951303c"></a>

### TEAM_French_Lasher1 - 0951303C

Owner: French. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095cf8ec"></a>

### TEAM_French_Lasher2 - 095CF8EC

Owner: French. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095cb13c"></a>

### TEAM_French_Lasher3 - 095CB13C

Owner: French. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095c813c"></a>

### TEAM_French_Virus - 095C813C

Owner: French. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095c913c"></a>

### TEAM_French_Yuri1 - 095C913C

Owner: French. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-095ca1ac"></a>

### TEAM_French_Yuri2 - 095CA1AC

Owner: French. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA.

Ordered plan: French_Guard (0CC4C90C).

1. Clear local flag: local flag 44 (French_Gone).
2. Adopt object mission: area guard.

<a id="team-0967471c"></a>

### TEAM_TC_Gatt1 - 0967471C

Owner: Confederation. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VD.

Ordered plan: TC_Guard_Gatt1 (0C789B7C).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 575 (cell 88, 108).
3. Adopt object mission: area guard.

<a id="team-09675efc"></a>

### TEAM_TC_Gatt2 - 09675EFC

Owner: Confederation. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VE.

Ordered plan: TC_Guard_Gatt2 (0C7896CC).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 576 (cell 88, 106).
3. Adopt object mission: area guard.

<a id="team-09675b1c"></a>

### TEAM_TC_Init1 - 09675B1C

Owner: Confederation. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VI.

Ordered plan: TC_Guard_Init1 (0C78921C).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 580 (cell 88, 109).
3. Adopt object mission: area guard.

<a id="team-096756fc"></a>

### TEAM_TC_Init2 - 096756FC

Owner: Confederation. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VJ.

Ordered plan: TC_Guard_Init2 (0C788C8C).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 581 (cell 88, 110).
3. Adopt object mission: area guard.

<a id="team-0be0d2bc"></a>

### TEAM_TC_Init3 - 0BE0D2BC

Owner: Confederation. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VK.

Ordered plan: TC_Guard_Init3 (0C7887DC).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 582 (cell 91, 109).
3. Adopt object mission: area guard.

<a id="team-06c6fefc"></a>

### TEAM_TC_Init4 - 06C6FEFC

Owner: Confederation. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VL.

Ordered plan: TC_Guard_Init4 (0C78832C).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 583 (cell 91, 110).
3. Adopt object mission: area guard.

<a id="team-06c6f82c"></a>

### TEAM_TC_Lasher1 - 06C6F82C

Owner: Confederation. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VA.

Ordered plan: TC_Guard_Lasher1 (0C78FDBC).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 572 (cell 86, 109).
3. Adopt object mission: area guard.

<a id="team-06c6f21c"></a>

### TEAM_TC_Lasher2 - 06C6F21C

Owner: Confederation. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VB.

Ordered plan: TC_Guard_Lasher2 (0C78F90C).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 573 (cell 86, 107).
3. Adopt object mission: area guard.

<a id="team-06c6e0fc"></a>

### TEAM_TC_Lasher3 - 06C6E0FC

Owner: Confederation. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VC.

Ordered plan: TC_Guard_Lasher3 (0C78F45C).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 574 (cell 86, 105).
3. Adopt object mission: area guard.

<a id="team-06c6b95c"></a>

### TEAM_TC_Virus - 06C6B95C

Owner: Confederation. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VH.

Ordered plan: TC_Guard_Virus (0C7941AC).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 579 (cell 88, 104).
3. Adopt object mission: area guard.

<a id="team-06c6b53c"></a>

### TEAM_TC_Yuri1 - 06C6B53C

Owner: Confederation. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VF.

Ordered plan: TC_Guard_Yuri1 (0C794C8C).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 577 (cell 90, 105).
3. Adopt object mission: area guard.

<a id="team-06c6b11c"></a>

### TEAM_TC_Yuri2 - 06C6B11C

Owner: Confederation. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VG.

Ordered plan: TC_Guard_Yuri2 (0C7947DC).

1. Clear local flag: local flag 48 (Confed_Gone).
2. Move to waypoint: waypoint 578 (cell 90, 104).
3. Adopt object mission: area guard.

<a id="team-096586bc"></a>

### TEAM_TD_Gatt1 - 096586BC

Owner: Arabs. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UD.

Ordered plan: TD_Guard_Gatt1 (0E10CDBC).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 549 (cell 107, 109).
3. Adopt object mission: guard.

<a id="team-09650b4c"></a>

### TEAM_TD_Gatt2 - 09650B4C

Owner: Arabs. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UE.

Ordered plan: TD_Guard_Gatt2 (0E10CA1C).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 550 (cell 109, 107).
3. Adopt object mission: guard.

<a id="team-09663e5c"></a>

### TEAM_TD_Lasher1 - 09663E5C

Owner: Arabs. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UA.

Ordered plan: TD_Guard_Lasher1 (0E10C56C).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 546 (cell 110, 113).
3. Adopt object mission: guard.

<a id="team-096639ac"></a>

### TEAM_TD_Lasher2 - 096639AC

Owner: Arabs. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UB.

Ordered plan: TD_Guard_Lasher2 (0E10C0BC).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 547 (cell 111, 112).
3. Adopt object mission: guard.

<a id="team-09661cdc"></a>

### TEAM_TD_Lasher3 - 09661CDC

Owner: Arabs. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UC.

Ordered plan: TD_Guard_Lasher3 (0E10D09C).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 548 (cell 112, 111).
3. Adopt object mission: guard.

<a id="team-09668e2c"></a>

### TEAM_TD_Yuri1 - 09668E2C

Owner: Arabs. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UF.

Ordered plan: TD_Guard_Yuri1 (0E10FB7C).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 551 (cell 112, 109).
3. Adopt object mission: guard.

<a id="team-0966897c"></a>

### TEAM_TD_Yuri2 - 0966897C

Owner: Arabs. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UG.

Ordered plan: TD_Guard_Yuri2 (0E10F6CC).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 552 (cell 108, 111).
3. Adopt object mission: guard.

<a id="team-0967732c"></a>

### TEAM_TD_Init1 - 0967732C

Owner: Arabs. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UI.

Ordered plan: TD_Guard_Init1 (0E10F21C).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 554 (cell 106, 107).
3. Adopt object mission: guard.

<a id="team-0967092c"></a>

### TEAM_TD_Init2 - 0967092C

Owner: Arabs. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UJ.

Ordered plan: TD_Guard_Init2 (0E10EC8C).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 555 (cell 106, 106).
3. Adopt object mission: guard.

<a id="team-0967047c"></a>

### TEAM_TD_Init3 - 0967047C

Owner: Arabs. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UK.

Ordered plan: TD_Guard_Init3 (0E10E7DC).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 556 (cell 107, 105).
3. Adopt object mission: guard.

<a id="team-0967028c"></a>

### TEAM_TD_Init4 - 0967028C

Owner: Arabs. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UL.

Ordered plan: TD_Guard_Init4 (0E10E32C).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 557 (cell 108, 105).
3. Adopt object mission: guard.

<a id="team-0967699c"></a>

### TEAM_TD_Virus - 0967699C

Owner: Arabs. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: UH.

Ordered plan: TD_Guard_Virus (0E10ADBC).

1. Clear local flag: local flag 47 (Arabs_Gone).
2. Move to waypoint: waypoint 553 (cell 105, 109).
3. Adopt object mission: guard.

<a id="team-0967b39c"></a>

### TEAM_AB_Gatt1 - 0967B39C

Owner: Germans. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Gatt1 (0967E87C).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-0967e61c"></a>

### TEAM_AB_Gatt2 - 0967E61C

Owner: Germans. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Gatt2 (0967FDBC).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-0967fb7c"></a>

### TEAM_AB_Init1 - 0967FB7C

Owner: Germans. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Init1 (0967F90C).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-0967f51c"></a>

### TEAM_AB_Init2 - 0967F51C

Owner: Germans. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Init2 (0967F2AC).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-0966041c"></a>

### TEAM_AB_Init3 - 0966041C

Owner: Germans. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Init3 (09677DBC).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-0966954c"></a>

### TEAM_AB_Init4 - 0966954C

Owner: Germans. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Init4 (09683DBC).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-09683a4c"></a>

### TEAM_AB_Lasher1 - 09683A4C

Owner: Germans. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Lasher1 (096837DC).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-0968359c"></a>

### TEAM_AB_Lasher2 - 0968359C

Owner: Germans. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Lasher2 (0968332C).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-09685efc"></a>

### TEAM_AB_Lasher3 - 09685EFC

Owner: Germans. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Lasher3 (09685C8C).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-09685adc"></a>

### TEAM_AB_Virus - 09685ADC

Owner: Germans. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Virus (0968586C).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-096856bc"></a>

### TEAM_AB_Yuri1 - 096856BC

Owner: Germans. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Yuri1 (0968544C).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-0968529c"></a>

### TEAM_AB_Yuri2 - 0968529C

Owner: Germans. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: AB_Guard_Yuri2 (09686A0C).

1. Move to waypoint: waypoint 27 (cell 127, 96).
2. Adopt object mission: area guard.

<a id="team-0c0b821c"></a>

### TEAM_TE_Gatt1 - 0C0B821C

Owner: GDI. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WH.

Ordered plan: TE_Guard_Gatt1 (0E11F90C).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 605 (cell 84, 132).
3. Adopt object mission: area guard.

<a id="team-09502e2c"></a>

### TEAM_TE_Gatt2 - 09502E2C

Owner: GDI. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WI.

Ordered plan: TE_Guard_Gatt2 (0E11F45C).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 606 (cell 84, 130).
3. Adopt object mission: area guard.

<a id="team-0950297c"></a>

### TEAM_TE_Init1 - 0950297C

Owner: GDI. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WA.

Ordered plan: TE_Guard_Init1 (0E11EDBC).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 598 (cell 89, 133).
3. Adopt object mission: area guard.

<a id="team-0950251c"></a>

### TEAM_TE_Init2 - 0950251C

Owner: GDI. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WB.

Ordered plan: TE_Guard_Init2 (0E11EA1C).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 599 (cell 89, 132).
3. Adopt object mission: area guard.

<a id="team-095020bc"></a>

### TEAM_TE_Init3 - 095020BC

Owner: GDI. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WC.

Ordered plan: TE_Guard_Init3 (0E11E56C).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 600 (cell 89, 131).
3. Adopt object mission: area guard.

<a id="team-0950d50c"></a>

### TEAM_TE_Init4 - 0950D50C

Owner: GDI. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WD.

Ordered plan: TE_Guard_Init4 (0E11E0BC).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 601 (cell 89, 130).
3. Adopt object mission: area guard.

<a id="team-0950d16c"></a>

### TEAM_TE_Lasher1 - 0950D16C

Owner: GDI. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WH.

Ordered plan: TE_Guard_Lasher1 (0E11DB7C).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 602 (cell 86, 133).
3. Adopt object mission: area guard.

<a id="team-0950d03c"></a>

### TEAM_TE_Lasher2 - 0950D03C

Owner: GDI. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WF.

Ordered plan: TE_Guard_Lasher2 (0E11D6CC).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 603 (cell 86, 131).
3. Adopt object mission: area guard.

<a id="team-0950f66c"></a>

### TEAM_TE_Lasher3 - 0950F66C

Owner: GDI. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WG.

Ordered plan: TE_Guard_Lasher3 (0E11D21C).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 604 (cell 86, 129).
3. Adopt object mission: area guard.

<a id="team-0950f20c"></a>

### TEAM_TE_Virus - 0950F20C

Owner: GDI. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WJ.

Ordered plan: TE_Guard_Virus (0E11BC8C).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 607 (cell 84, 129).
3. Adopt object mission: area guard.

<a id="team-0950ec8c"></a>

### TEAM_TE_Yuri1 - 0950EC8C

Owner: GDI. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WK.

Ordered plan: TE_Guard_Yuri1 (0E11B7DC).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 608 (cell 81, 130).
3. Adopt object mission: area guard.

<a id="team-0950e65c"></a>

### TEAM_TE_Yuri2 - 0950E65C

Owner: GDI. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WL.

Ordered plan: TE_Guard_Yuri2 (0E11B32C).

1. Clear local flag: local flag 49 (GDI_Gone).
2. Move to waypoint: waypoint 609 (cell 81, 131).
3. Adopt object mission: area guard.

<a id="team-096aaefc"></a>

### TEAM_AD_Gatt1 - 096AAEFC

Owner: PPAD Country. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Gatt1 (096AAC8C).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096aa94c"></a>

### TEAM_AD_Gatt2 - 096AA94C

Owner: PPAD Country. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Gatt2 (096AA6DC).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096aa3fc"></a>

### TEAM_AD_Init1 - 096AA3FC

Owner: PPAD Country. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Init1 (096AEDBC).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096aec8c"></a>

### TEAM_AD_Init2 - 096AEC8C

Owner: PPAD Country. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Init2 (096AEA1C).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096ae8ec"></a>

### TEAM_AD_Init3 - 096AE8EC

Owner: PPAD Country. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Init3 (096AE2AC).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096a9bdc"></a>

### TEAM_AD_Init4 - 096A9BDC

Owner: PPAD Country. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Init4 (096A996C).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096a97bc"></a>

### TEAM_AD_Lasher1 - 096A97BC

Owner: PPAD Country. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Lasher1 (096A954C).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096a939c"></a>

### TEAM_AD_Lasher2 - 096A939C

Owner: PPAD Country. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Lasher2 (096A5DBC).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096a926c"></a>

### TEAM_AD_Lasher3 - 096A926C

Owner: PPAD Country. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Lasher3 (096B6DBC).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096b678c"></a>

### TEAM_AD_Virus - 096B678C

Owner: PPAD Country. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Virus (096B651C).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096b62dc"></a>

### TEAM_AD_Yuri2 - 096B62DC

Owner: PPAD Country. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Yuri2 (096B1DBC).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-096b1c0c"></a>

### TEAM_AD_Yuri1 - 096B1C0C

Owner: PPAD Country. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: AD_Guard_Yuri1 (096B199C).

1. Move to waypoint: waypoint 29 (cell 125, 124).
2. Adopt object mission: area guard.

<a id="team-095b536c"></a>

### TEAM_TF_Gatt1 - 095B536C

Owner: PPTF Country. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XD.

Ordered plan: TF_Guard_Gatt1 (0C3DCA1C).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 627 (cell 66, 117).
3. Adopt object mission: area guard.

<a id="team-095b6d7c"></a>

### TEAM_TF_Gatt2 - 095B6D7C

Owner: PPTF Country. Roster: 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XE.

Ordered plan: TF_Guard_Gatt2 (0C3DBDBC).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 628 (cell 64, 110).
3. Adopt object mission: area guard.

<a id="team-095b68cc"></a>

### TEAM_TF_Init1 - 095B68CC

Owner: PPTF Country. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XI.

Ordered plan: TF_Guard_Init1 (0C3DBB4C).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 632 (cell 70, 117).
3. Adopt object mission: area guard.

<a id="team-095b606c"></a>

### TEAM_TF_Init2 - 095B606C

Owner: PPTF Country. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XJ.

Ordered plan: TF_Guard_Init2 (0C3DB69C).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 633 (cell 71, 116).
3. Adopt object mission: area guard.

<a id="team-095b7c0c"></a>

### TEAM_TF_Init3 - 095B7C0C

Owner: PPTF Country. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XK.

Ordered plan: TF_Guard_Init3 (0C3DB1EC).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 634 (cell 71, 115).
3. Adopt object mission: area guard.

<a id="team-095b782c"></a>

### TEAM_TF_Init4 - 095B782C

Owner: PPTF Country. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XL.

Ordered plan: TF_Guard_Init4 (0C3DAC8C).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 635 (cell 71, 114).
3. Adopt object mission: area guard.

<a id="team-095b740c"></a>

### TEAM_TF_Lasher1 - 095B740C

Owner: PPTF Country. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XA.

Ordered plan: TF_Guard_Lasher1 (0C3DA7DC).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 624 (cell 68, 117).
3. Adopt object mission: area guard.

<a id="team-0ba5fc1c"></a>

### TEAM_TF_Lasher2 - 0BA5FC1C

Owner: PPTF Country. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XB.

Ordered plan: TF_Guard_Lasher2 (0C3DA32C).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 625 (cell 68, 119).
3. Adopt object mission: area guard.

<a id="team-095b706c"></a>

### TEAM_TF_Lasher3 - 095B706C

Owner: PPTF Country. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XC.

Ordered plan: TF_Guard_Lasher3 (0C3D9DBC).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 626 (cell 69, 112).
3. Adopt object mission: area guard.

<a id="team-095b8a4c"></a>

### TEAM_TF_Virus - 095B8A4C

Owner: PPTF Country. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XH.

Ordered plan: TF_Guard_Virus (0C3D990C).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 631 (cell 67, 110).
3. Adopt object mission: area guard.

<a id="team-095b859c"></a>

### TEAM_TF_Yuri1 - 095B859C

Owner: PPTF Country. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XF.

Ordered plan: TF_Guard_Yuri1 (0C3D945C).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 629 (cell 65, 117).
3. Adopt object mission: area guard.

<a id="team-095b813c"></a>

### TEAM_TF_Yuri2 - 095B813C

Owner: PPTF Country. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XG.

Ordered plan: TF_Guard_Yuri2 (0C3D8DBC).

1. Clear local flag: local flag 43 (PPTF_Gone).
2. Move to waypoint: waypoint 630 (cell 66, 110).
3. Adopt object mission: area guard.

<a id="team-095c2e1c"></a>

### TEAM_AB_Engineer - 095C2E1C

Owner: YuriCountry. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: EB; Transport Waypoint: PB.

Ordered plan: Engineer_AB_Script (095C2BAC).

1. Attack waypoint: waypoint 27 (cell 127, 96).

<a id="team-04646b6c"></a>

### TEAM_YuriBD1 - 04646B6C

Owner: YuriCountry. Roster: 3 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: DA.

Ordered plan: YuriBD1_Script (046468FC).

1. Adopt object mission: area guard.

<a id="team-046465fc"></a>

### TEAM_YuriBD2 - 046465FC

Owner: YuriCountry. Roster: 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: DB.

Ordered plan: YuriBD2_Script (0464638C).

1. Adopt object mission: area guard.

<a id="team-0464781c"></a>

### TEAM_YuriBD3 - 0464781C

Owner: YuriCountry. Roster: 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: DC.

Ordered plan: YuriBD_Script (046475AC).

1. Adopt object mission: area guard.

<a id="team-096173cc"></a>

### TEAM_Virus_Attack - 096173CC

Owner: YuriCountry. Roster: 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Virus_Attack (0961715C).

1. Seek/attack target category; configured argument 4.
2. Report team success.

<a id="team-0961797c"></a>

### TEAM_Tank_Attack1 - 0961797C

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Tank_Attack1_Script (0961770C).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 2.
4. Report team success.

<a id="team-096462ec"></a>

### TEAM_Tank_Attack2 - 096462EC

Owner: YuriCountry. Roster: 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Tank_Attack2_Script (06BF73AC).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 2.
3. Report team success.

<a id="team-0956f76c"></a>

### Team_Clone_Attack - 0956F76C

Owner: YuriCountry. Roster: 2 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Clone_World_Script (09578DBC).

1. Seek/attack target category; configured argument 4.
2. Seek/attack target category; configured argument 5.
3. Report team success.

<a id="team-095b932c"></a>

### TEAM_BD_Clones - 095B932C

Owner: YuriCountry. Roster: 3 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: DA.

Ordered plan: BD_Clones_Script (0464AA3C).

1. Move to waypoint: waypoint 104 (cell 49, 87).
2. Adopt object mission: area guard.

<a id="team-0464a7dc"></a>

### TEAM_BD_Tanks - 0464A7DC

Owner: YuriCountry. Roster: 3 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: DB.

Ordered plan: BD_Tanks_Script (0464A56C).

1. Move to waypoint: waypoint 105 (cell 56, 87).
2. Adopt object mission: area guard.

<a id="team-095b87dc"></a>

### TEAM_BD_Virus - 095B87DC

Owner: YuriCountry. Roster: 2 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: DC.

Ordered plan: BD_Virus_Script (0464A0BC).

1. Move to waypoint: waypoint 106 (cell 53, 91).
2. Adopt object mission: area guard.

<a id="team-0d8a4bbc"></a>

### TEAM_Gattling_Attack - 0D8A4BBC

Owner: YuriCountry. Roster: 2 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Gattling_Attack_Script (0D8A494C).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 2.
4. Report team success.

<a id="team-0d8a455c"></a>

### TEAM_Initiate_Attack - 0D8A455C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Initiate_Attack_Script (0D8A42EC).

1. Seek/attack target category; configured argument 4.
2. Seek/attack target category; configured argument 5.
3. Seek/attack target category; configured argument 2.
4. Report team success.

<a id="team-0d8a5efc"></a>

### TEAM_VirusClone_Attack - 0D8A5EFC

Owner: YuriCountry. Roster: 1 × Yuri Clone (YURI); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: VirusClone_Attack_Script (0D8A5C8C).

1. Seek/attack target category; configured argument 4.
2. Report team success.

<a id="team-08d650ec"></a>

### TEAM_Alliance_Reinforce - 08D650EC

Owner: Americans. Roster: 3 × Grizzly Battle Tank (MTNK); 1 × Mirage Tank (MGTK); 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BA.

Ordered plan: British_Reinforce_Script (0EA2980C).

1. Move to waypoint: waypoint 341 (cell 131, 132).
2. Move to waypoint: waypoint 306 (cell 114, 132).

<a id="team-0c11c0ec"></a>

### TEAM_AD_Engineer - 0C11C0EC

Owner: YuriCountry. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: ED; Transport Waypoint: PD.

Ordered plan: AD_Engineer_Script (0C11123C).

1. Attack waypoint: waypoint 29 (cell 125, 124).

<a id="team-0b6d745c"></a>

### TEAM_Grizzly_BD - 0B6D745C

Owner: Americans. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: GrizzlyBD_Script (0B6D6DBC).

1. Move to waypoint: waypoint 55 (cell 153, 120).

<a id="team-0b6d6b5c"></a>

### TEAM_Grizzly_BE - 0B6D6B5C

Owner: Americans. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: GrizzlyBE_Script (0B6D68EC).

1. Move to waypoint: waypoint 56 (cell 153, 118).

<a id="team-0b6d66ec"></a>

### TEAM_Grizzly_BF - 0B6D66EC

Owner: Americans. Roster: 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: GrizzlyBF_Script (0B6D647C).

1. Move to waypoint: waypoint 57 (cell 153, 116).

<a id="team-0b6d62cc"></a>

### TEAM_Mirage_BG - 0B6D62CC

Owner: Americans. Roster: 1 × Mirage Tank (MGTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: MirageBG_Script (0B6D605C).

1. Move to waypoint: waypoint 58 (cell 155, 120).

<a id="team-0b6d3ebc"></a>

### TEAM_Mirage_BH - 0B6D3EBC

Owner: Americans. Roster: 1 × Mirage Tank (MGTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: MirageBH_Script (0B6D3C4C).

1. Move to waypoint: waypoint 59 (cell 155, 118).

<a id="team-0b6d3adc"></a>

### TEAM_Mirage_BI - 0B6D3ADC

Owner: Americans. Roster: 1 × Mirage Tank (MGTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: MirageBI_Script (0B6D386C).

1. Move to waypoint: waypoint 60 (cell 155, 116).

<a id="team-04f3226c"></a>

### TEAM_IFV_BG - 04F3226C

Owner: Americans. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: IFVBJ_Script (04F33DBC).

1. Move to waypoint: waypoint 58 (cell 155, 120).

<a id="team-04f33c8c"></a>

### TEAM_IFV_BI - 04F33C8C

Owner: Americans. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: IFVBK_Script (04F33A1C).

1. Move to waypoint: waypoint 60 (cell 155, 116).

<a id="team-0b6d1efc"></a>

### TEAM_IFV_BL - 0B6D1EFC

Owner: Americans. Roster: 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: IFVBL_Script (0B6D1C8C).

1. Move to waypoint: waypoint 63 (cell 157, 116).

<a id="team-0b6ef9bc"></a>

### TEAM_TD_Snipers - 0B6EF9BC

Owner: Americans. Roster: 3 × Sniper (SNIPE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 12; Veteran Level: 1; Technology level: 0; Waypoint: TD; Transport Waypoint: BA.

Ordered plan: TD_Snipers (0B6EF74C).

1. Adopt object mission: area guard.

<a id="team-0b8df08c"></a>

### TEAM_Yuri_TC_TD_Engineers - 0B8DF08C

Owner: YuriCountry. Roster: 5 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VB; Transport Waypoint: AC.

Ordered plan: TC_TD_Engineers (0B69439C).

1. Attack waypoint: waypoint 523 (cell 109, 109).

<a id="team-0954544c"></a>

### TEAM_TC_Snipers - 0954544C

Owner: Americans. Roster: 3 × Sniper (SNIPE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TC; Transport Waypoint: BA.

Ordered plan: TC_Snipers (095451DC).

1. Adopt object mission: area guard.

<a id="team-0b8d57dc"></a>

### TEAM_Yuri_TF_TC_Engineer - 0B8D57DC

Owner: YuriCountry. Roster: 5 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XJ; Transport Waypoint: AF.

Ordered plan: TF_TC_Engineers (095D1DBC).

1. Attack waypoint: waypoint 522 (cell 90, 107).

<a id="team-0c88543c"></a>

### TEAM_TA_Engineer - 0C88543C

Owner: YuriCountry. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: RF; Transport Waypoint: PA.

Ordered plan: Yuri_TA_Engineer (0C775C0C).

1. Attack waypoint: waypoint 520 (cell 101, 58).

<a id="team-0c886efc"></a>

### TEAM_TB_Engineer - 0C886EFC

Owner: YuriCountry. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SL; Transport Waypoint: PA.

Ordered plan: Yuri_TB_Engineer (0BCA56BC).

1. Attack waypoint: waypoint 521 (cell 90, 72).

<a id="team-0c94e2dc"></a>

### TEAM_TC_Engineer - 0C94E2DC

Owner: YuriCountry. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: VC; Transport Waypoint: PZ.

Ordered plan: Yuri_TC_Engineer (0BCA663C).

1. Attack waypoint: waypoint 521 (cell 90, 72).

<a id="team-0c2e054c"></a>

### TEAM_TD_Engineer - 0C2E054C

Owner: YuriCountry. Roster: 1 × Engineer (YENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: EC; Transport Waypoint: KW.

Ordered plan: Yuri_TD_Engineer (0BCA61CC).

1. Attack waypoint: waypoint 523 (cell 109, 109).

<a id="team-0c94f90c"></a>

### TEAM_TE_Engineer - 0C94F90C

Owner: YuriCountry. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: WG; Transport Waypoint: PZ.

Ordered plan: Yuri_TE_Engineer (0BC41DBC).

1. Attack waypoint: waypoint 524 (cell 84, 134).

<a id="team-0c85e1fc"></a>

### TEAM_TF_Engineer - 0C85E1FC

Owner: YuriCountry. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: EF; Transport Waypoint: PZ.

Ordered plan: Yuri_TF_Engineer (0BC418DC).

1. Attack waypoint: waypoint 525 (cell 65, 113).

<a id="team-0bcb4a1c"></a>

### TEAM_TE_Snipers - 0BCB4A1C

Owner: Americans. Roster: 3 × Sniper (SNIPE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TE; Transport Waypoint: BA.

Ordered plan: TC_Snipers (095451DC).

1. Adopt object mission: area guard.

<a id="team-0bc4edac"></a>

### TEAM_TF_Snipers - 0BC4EDAC

Owner: Americans. Roster: 3 × Sniper (SNIPE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TF; Transport Waypoint: BA.

Ordered plan: TC_Snipers (095451DC).

1. Adopt object mission: area guard.

<a id="team-0bc6d60c"></a>

### TEAM_TA_Snipers - 0BC6D60C

Owner: Americans. Roster: 3 × Sniper (SNIPE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TA; Transport Waypoint: PA.

Ordered plan: TC_Snipers (095451DC).

1. Adopt object mission: area guard.

<a id="team-0bc6ac4c"></a>

### TEAM_TB_Snipers - 0BC6AC4C

Owner: Americans. Roster: 3 × Sniper (SNIPE)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: TB; Transport Waypoint: PA.

Ordered plan: TC_Snipers (095451DC).

1. Adopt object mission: area guard.

<a id="team-0b8e2dcc"></a>

### TEAM_Yuri_TB_TA_Engineer - 0B8E2DCC

Owner: YuriCountry. Roster: 5 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: SC; Transport Waypoint: PA.

Ordered plan: Yuri_TB_TA_Engineers (0BC06BFC).

1. Attack waypoint: waypoint 520 (cell 101, 58).

<a id="team-0bbfb72c"></a>

### TEAM_Yuri_FA_TB_Engineer - 0BBFB72C

Owner: YuriCountry. Roster: 5 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FA; Transport Waypoint: PZ.

Ordered plan: Yuri_FA_TB_Engineers (0BBFB4BC).

1. Attack waypoint: waypoint 521 (cell 90, 72).

<a id="team-0b8e268c"></a>

### TEAM_Yuri_TF_TE_Engineer - 0B8E268C

Owner: YuriCountry. Roster: 5 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: XJ; Transport Waypoint: PZ.

Ordered plan: Yuri_TF_TE_Engineers (0BC2216C).

1. Attack waypoint: waypoint 524 (cell 84, 134).

<a id="team-0b8e22ec"></a>

### TEAM_Yuri_FB_TF_Engineer - 0B8E22EC

Owner: YuriCountry. Roster: 5 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: FB; Transport Waypoint: PZ.

Ordered plan: Yuri_FB_TF_Engineer (0929B86C).

1. Attack waypoint: waypoint 525 (cell 65, 113).

<a id="team-0988192c"></a>

### TEAM_Nuke_Guard - 0988192C

Owner: YuriCountry. Roster: 5 × Virus (VIRUS); 3 × Yuri Clone (YURI); 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: NY; Transport Waypoint: PZ.

Ordered plan: Nuke_Guard_Script (0988EDBC).

1. Scatter.
2. Adopt object mission: area guard.

<a id="team-045ea05c"></a>

### TEAM_Paradrop_WC1 - 045EA05C

Owner: YuriCountry. Roster: 5 × Initiate (INIT); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: DC; Transport Waypoint: AC.

Ordered plan: Paradrop_WC1_Script (045EDDBC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 131101.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 4.
6. Seek/attack target category; configured argument 9.
7. Seek/attack target category; configured argument 10.

<a id="team-0968684c"></a>

### TEAM_Paradrop_WC2 - 0968684C

Owner: YuriCountry. Roster: 6 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: DC; Transport Waypoint: AF.

Ordered plan: Paradrop_WC2_Script (096865DC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 131101.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 9.
7. Seek/attack target category; configured argument 10.

<a id="team-06be73dc"></a>

### TEAM_Paradrop_WC3 - 06BE73DC

Owner: YuriCountry. Roster: 5 × Initiate (INIT); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: DC; Transport Waypoint: PZ.

Ordered plan: Paradrop_WC3_Script (06BE716C).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Attack selected enemy-building category; configured argument 131101.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 9.
6. Seek/attack target category; configured argument 10.

<a id="team-045e812c"></a>

### TEAM_Infantry_Hunter_1 - 045E812C

Owner: YuriCountry. Roster: 2 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: DC; Transport Waypoint: AC.

Ordered plan: Infantry_Hunter1_Script (045EA66C).

1. Seek/attack target category; configured argument 4.
2. Attack selected enemy-building category; configured argument 131101.

<a id="team-045ea43c"></a>

### TEAM_Infantry_Hunter2 - 045EA43C

Owner: YuriCountry. Roster: 1 × Virus (VIRUS); 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: DC; Transport Waypoint: AF.

Ordered plan: Infantry_Hunter2_Script (045EA1CC).

1. Seek/attack target category; configured argument 4.
2. Seek/attack target category; configured argument 9.
3. Seek/attack target category; configured argument 10.
4. Attack selected enemy-building category; configured argument 131101.

<a id="team-096f77ac"></a>

### TEAM_Vehicle_Hunter1 - 096F77AC

Owner: YuriCountry. Roster: 4 × Initiate (INIT); 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: DC; Transport Waypoint: PZ.

Ordered plan: Vehicle_Hunter1 (096F753C).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 9.
4. Attack selected enemy-building category; configured argument 131101.

<a id="team-09718efc"></a>

### TEAM_Vehicle_Hunter2 - 09718EFC

Owner: YuriCountry. Roster: 4 × Initiate (INIT); 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: DC; Transport Waypoint: AC.

Ordered plan: Vehicle_Hunter2_Script (09718C8C).

1. Seek/attack target category; configured argument 5.
2. Seek/attack target category; configured argument 4.
3. Attack selected enemy-building category; configured argument 131101.
4. Seek/attack target category; configured argument 9.
5. Seek/attack target category; configured argument 10.

<a id="team-089b368c"></a>

### Patrol_AH_JS - 089B368C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AH.

Ordered plan: AH_JS_Patrol (089B341C).

1. Move to waypoint: waypoint 278 (cell 83, 102).
2. Move to waypoint: waypoint 33 (cell 84, 112).
3. Jump to script line; configured argument 1.

<a id="team-089bec9c"></a>

### Patrol_AI_AJ - 089BEC9C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AI.

Ordered plan: AI_AJ_Patrol (089BEA2C).

1. Move to waypoint: waypoint 35 (cell 79, 113).
2. Move to waypoint: waypoint 34 (cell 80, 130).
3. Jump to script line; configured argument 1.

<a id="team-089b8a3c"></a>

### Patrol_AK_AL_AM - 089B8A3C

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: AK_AL_AM_Patrol (089B87CC).

1. Move to waypoint: waypoint 37 (cell 64, 103).
2. Move to waypoint: waypoint 38 (cell 71, 110).
3. Move to waypoint: waypoint 37 (cell 64, 103).
4. Move to waypoint: waypoint 36 (cell 59, 108).
5. Jump to script line; configured argument 1.

<a id="team-089b83ec"></a>

### Patrol_KK_KO - 089B83EC

Owner: YuriCountry. Roster: 4 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KK.

Ordered plan: KK_KO_Patrol (089B817C).

1. Move to waypoint: waypoint 39 (cell 99, 64).
2. Move to waypoint: waypoint 300 (cell 109, 64).
3. Move to waypoint: waypoint 39 (cell 99, 64).
4. Move to waypoint: waypoint 296 (cell 97, 66).
5. Jump to script line; configured argument 1.

<a id="team-0affd42c"></a>

### Patrol_AO_AQ - 0AFFD42C

Owner: YuriCountry. Roster: 2 × Yuri Clone (YURI); 2 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AO.

Ordered plan: AO_AQ_Patrol (0B00193C).

1. Move to waypoint: waypoint 41 (cell 103, 82).
2. Move to waypoint: waypoint 42 (cell 115, 94).
3. Move to waypoint: waypoint 41 (cell 103, 82).
4. Move to waypoint: waypoint 40 (cell 102, 79).
5. Jump to script line; configured argument 1.

<a id="team-0b0061ac"></a>

### Patrol_JT_AH - 0B0061AC

Owner: YuriCountry. Roster: 2 × Yuri Clone (YURI); 2 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: JT.

Ordered plan: JT_AH_Patrol (0B0016CC).

1. Move to waypoint: waypoint 33 (cell 84, 112).
2. Move to waypoint: waypoint 279 (cell 99, 112).
3. Jump to script line; configured argument 1.

<a id="team-0b00159c"></a>

### Patrol_JN_AT - 0B00159C

Owner: YuriCountry. Roster: 2 × Yuri Clone (YURI); 2 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: JN.

Ordered plan: JN_AT_Patrol (0B00132C).

1. Move to waypoint: waypoint 43 (cell 82, 118).
2. Move to waypoint: waypoint 44 (cell 92, 128).
3. Move to waypoint: waypoint 45 (cell 93, 131).
4. Move to waypoint: waypoint 44 (cell 92, 128).
5. Move to waypoint: waypoint 43 (cell 82, 118).
6. Move to waypoint: waypoint 273 (cell 80, 118).
7. Jump to script line; configured argument 1.

<a id="team-0b007dbc"></a>

### Patrol_KL_AO - 0B007DBC

Owner: YuriCountry. Roster: 2 × Yuri Clone (YURI); 2 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: KL.

Ordered plan: KL_AO_Patrol (0B007B4C).

1. Move to waypoint: waypoint 46 (cell 102, 74).
2. Move to waypoint: waypoint 40 (cell 102, 79).
3. Move to waypoint: waypoint 46 (cell 102, 74).
4. Move to waypoint: waypoint 297 (cell 86, 58).
5. Jump to script line; configured argument 1.

<a id="team-0462b5ac"></a>

### Garrision_AJ - 0462B5AC

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: Garrison_Script (0462B33C).

1. Enter neutral occupiable building.

<a id="team-0462cefc"></a>

### Garrison_AN - 0462CEFC

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AN.

Ordered plan: Garrison_Script (0462B33C).

1. Enter neutral occupiable building.

<a id="team-061a379c"></a>

### Garrison_AV - 061A379C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AV.

Ordered plan: Garrison_Script (0462B33C).

1. Enter neutral occupiable building.

<a id="team-061a366c"></a>

### Garrison_AW - 061A366C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AW.

Ordered plan: Garrison_Script (0462B33C).

1. Enter neutral occupiable building.

<a id="team-061a353c"></a>

### Garrison_EF - 061A353C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: EF.

Ordered plan: Garrison_Script (0462B33C).

1. Enter neutral occupiable building.

<a id="team-061e6e5c"></a>

### Backdoor1 - 061E6E5C

Owner: YuriCountry. Roster: 8 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AX; Transport Waypoint: AC.

Ordered plan: Backdoor1_Script (061E6BEC).

1. Move to waypoint: waypoint 286 (cell 92, 78).
2. Move to waypoint: waypoint 41 (cell 103, 82).
3. Move to waypoint: waypoint 50 (cell 131, 110).
4. Move to waypoint: waypoint 309 (cell 124, 130).
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-0619684c"></a>

### Backdoor2 - 0619684C

Owner: YuriCountry. Roster: 6 × Initiate (INIT); 1 × Virus (VIRUS); 1 × Engineer (YENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AX; Transport Waypoint: AC.

Ordered plan: Backdoor1_Script (061E6BEC).

1. Move to waypoint: waypoint 286 (cell 92, 78).
2. Move to waypoint: waypoint 41 (cell 103, 82).
3. Move to waypoint: waypoint 50 (cell 131, 110).
4. Move to waypoint: waypoint 309 (cell 124, 130).
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.

<a id="team-0619e1bc"></a>

### Backdoor3 - 0619E1BC

Owner: YuriCountry. Roster: 4 × Initiate (INIT); 2 × Yuri Clone (YURI); 1 × Engineer (YENGINEER); 1 × Virus (VIRUS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AX; Transport Waypoint: AC.

Ordered plan: Backdoor1_Script (061E6BEC).

1. Move to waypoint: waypoint 286 (cell 92, 78).
2. Move to waypoint: waypoint 41 (cell 103, 82).
3. Move to waypoint: waypoint 50 (cell 131, 110).
4. Move to waypoint: waypoint 309 (cell 124, 130).
5. Seek/attack target category; configured argument 2.
6. Seek/attack target category; configured argument 1.
