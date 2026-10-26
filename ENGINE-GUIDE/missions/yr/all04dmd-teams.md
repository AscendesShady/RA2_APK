# Operation: Tomb Raided - team rosters and plans

[Trigger ledger](all04dmd.md) | [Mission overrides](all04dmd-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: mapsmd03.mix/all04dmd.map; each team/script ID identifies its section.

<a id="team-0ba0ea9c"></a>

### Yuri Foot Attack - 0BA0EA9C

Owner: YuriCountry. Roster: 4 × Initiate (INIT); 1 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 110; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri Foot Attack (0C1DC82C).

1. Gather near own base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131072.
3. Report team success.
4. Seek/attack target category; configured argument 9.
5. Report team success.
6. Seek/attack target category; configured argument 1.

<a id="team-0c1dc5ec"></a>

### Yuri 2nd Foot Attack - 0C1DC5EC

Owner: YuriCountry. Roster: 3 × Initiate (INIT); 4 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri Second Foot Attack (0C1DC37C).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131075.
3. Report team success.
4. Seek/attack target category; configured argument 1.

<a id="team-0b642a4c"></a>

### Yuri Base Defense - 0B642A4C

Owner: YuriCountry. Roster: 1 × Yuri Clone (YURI); 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri Base Defense (0C8F390C).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0c1ddb7c"></a>

### Yuri Tank Attack - 0C1DDB7C

Owner: YuriCountry. Roster: 4 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 120; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri Tank Attack (0BCCF0BC).

1. Seek/attack target category; configured argument 5.
2. Report team success.

<a id="team-0c1dd59c"></a>

### Yuri Hover Attack - 0C1DD59C

Owner: YuriCountry. Roster: 2 × Initiate (INIT); 1 × Yuri Clone (YURI); 2 × Lasher Light Tank (LTNK); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 120; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Q.

Ordered plan: Yuri Hover Attack (0C1DD32C).

1. Move to waypoint: waypoint 2 (cell 58, 133).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 0 (HoverDeliver).
4. Seek/attack target category; configured argument 6.
5. Report team success.
6. Seek/attack target category; configured argument 1.

<a id="team-0c1dd0ec"></a>

### Engineer Repair Task - 0C1DD0EC

Owner: YuriCountry. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 200; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Engineer Repair Unit (0AFB790C).

1. Attack waypoint: waypoint 1 (cell 154, 66).

<a id="team-0c1deb7c"></a>

### Engineer Unit 2 - 0C1DEB7C

Owner: YuriCountry. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 200; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Fixing Second Bridge (0B19F54C).

1. Attack waypoint: waypoint 4 (cell 154, 112).

<a id="team-0b3aaa4c"></a>

### Oil Derreck 1 - 0B3AAA4C

Owner: Russians. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: Oil Derreck 1 (0B09990C).

1. Attack-move toward waypoint: waypoint 6 (cell 167, 99).
2. Attack-move toward waypoint: waypoint 5 (cell 163, 99).
3. Attack-move toward waypoint: waypoint 6 (cell 167, 99).
4. Attack-move toward waypoint: waypoint 5 (cell 163, 99).
5. Attack-move toward waypoint: waypoint 6 (cell 167, 99).
6. Guard for interval; configured argument 5.
7. Jump to script line; configured argument 1.

<a id="team-0b3aa59c"></a>

### Oil Derreck 2 - 0B3AA59C

Owner: Russians. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: G.

Ordered plan: Oil Derreck 2 (0B09945C).

1. Attack-move toward waypoint: waypoint 5 (cell 163, 99).
2. Attack-move toward waypoint: waypoint 6 (cell 167, 99).
3. Attack-move toward waypoint: waypoint 5 (cell 163, 99).
4. Attack-move toward waypoint: waypoint 6 (cell 167, 99).
5. Attack-move toward waypoint: waypoint 5 (cell 163, 99).
6. Attack-move toward waypoint: waypoint 6 (cell 167, 99).
7. Attack-move toward waypoint: waypoint 5 (cell 163, 99).
8. Guard for interval; configured argument 3.
9. Jump to script line; configured argument 1.

<a id="team-0b3afefc"></a>

### Oil Derreck 3 - 0B3AFEFC

Owner: Russians. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: H.

Ordered plan: Oil Derreck 3 (0B5B7DBC).

1. Attack-move toward waypoint: waypoint 8 (cell 177, 85).
2. Attack-move toward waypoint: waypoint 7 (cell 173, 85).
3. Attack-move toward waypoint: waypoint 8 (cell 177, 85).
4. Attack-move toward waypoint: waypoint 7 (cell 173, 85).
5. Attack-move toward waypoint: waypoint 8 (cell 177, 85).
6. Attack-move toward waypoint: waypoint 7 (cell 173, 85).
7. Guard for interval; configured argument 4.
8. Jump to script line; configured argument 1.

<a id="team-0b3afa4c"></a>

### Oil Derreck 4 - 0B3AFA4C

Owner: Russians. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: I.

Ordered plan: Oil Derreck 4 (0B5B6DBC).

1. Attack-move toward waypoint: waypoint 7 (cell 173, 85).
2. Attack-move toward waypoint: waypoint 8 (cell 177, 85).
3. Attack-move toward waypoint: waypoint 7 (cell 173, 85).
4. Attack-move toward waypoint: waypoint 8 (cell 177, 85).
5. Guard for interval; configured argument 6.
6. Jump to script line; configured argument 1.

<a id="team-0b3af59c"></a>

### Oil Derreck Tank 1 - 0B3AF59C

Owner: Russians. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: Oil Derreck Tank 1 (0B130DBC).

1. Attack-move toward waypoint: waypoint 10 (cell 165, 86).
2. Guard for interval; configured argument 3.
3. Attack-move toward waypoint: waypoint 11 (cell 171, 85).
4. Guard for interval; configured argument 6.
5. Attack-move toward waypoint: waypoint 9 (cell 164, 95).
6. Guard for interval; configured argument 4.
7. Attack-move toward waypoint: waypoint 10 (cell 165, 86).
8. Guard for interval; configured argument 6.
9. Attack-move toward waypoint: waypoint 9 (cell 164, 95).
10. Guard for interval; configured argument 3.
11. Attack-move toward waypoint: waypoint 11 (cell 171, 85).
12. Guard for interval; configured argument 2.
13. Jump to script line; configured argument 1.

<a id="team-0b3adefc"></a>

### Oil Derreck Tank 2 - 0B3ADEFC

Owner: Russians. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: L.

Ordered plan: Oil Derreck Tank 2 (0A31030C).

1. Attack-move toward waypoint: waypoint 9 (cell 164, 95).
2. Guard for interval; configured argument 2.
3. Attack-move toward waypoint: waypoint 11 (cell 171, 85).
4. Guard for interval; configured argument 5.
5. Attack-move toward waypoint: waypoint 10 (cell 165, 86).
6. Guard for interval; configured argument 2.
7. Attack-move toward waypoint: waypoint 9 (cell 164, 95).
8. Guard for interval; configured argument 4.
9. Attack-move toward waypoint: waypoint 10 (cell 165, 86).
10. Guard for interval; configured argument 3.
11. Jump to script line; configured argument 1.

<a id="team-0b3ada4c"></a>

### Oil Derreck Tank 3 - 0B3ADA4C

Owner: Russians. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: M.

Ordered plan: Oil Derreck Tank 3 (0A311DBC).

1. Attack-move toward waypoint: waypoint 13 (cell 177, 96).
2. Guard for interval; configured argument 3.
3. Attack-move toward waypoint: waypoint 14 (cell 180, 89).
4. Guard for interval; configured argument 5.
5. Attack-move toward waypoint: waypoint 12 (cell 173, 99).
6. Guard for interval; configured argument 3.
7. Attack-move toward waypoint: waypoint 14 (cell 180, 89).
8. Guard for interval; configured argument 4.
9. Jump to script line; configured argument 1.

<a id="team-0b3ad59c"></a>

### Oil Derreck Tank 4 - 0B3AD59C

Owner: Russians. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: O.

Ordered plan: Oil Derreck Tank 4 (0A31190C).

1. Attack-move toward waypoint: waypoint 12 (cell 173, 99).
2. Guard for interval; configured argument 4.
3. Attack-move toward waypoint: waypoint 13 (cell 177, 96).
4. Guard for interval; configured argument 2.
5. Attack-move toward waypoint: waypoint 14 (cell 180, 89).
6. Guard for interval; configured argument 5.
7. Attack-move toward waypoint: waypoint 12 (cell 173, 99).
8. Guard for interval; configured argument 3.
9. Attack-move toward waypoint: waypoint 13 (cell 177, 96).
10. Guard for interval; configured argument 2.
11. Jump to script line; configured argument 1.

<a id="team-0c1e1b7c"></a>

### Hover Return - 0C1E1B7C

Owner: YuriCountry. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 200; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: C.

Ordered plan: Hover Return (08EE1DBC).

1. Move to waypoint: waypoint 15 (cell 135, 50).
2. Clear local flag: local flag 0 (HoverDeliver).

<a id="team-0c1e16cc"></a>

### No Bridge Hover Attack - 0C1E16CC

Owner: YuriCountry. Roster: 3 × Yuri Clone (YURI); 2 × Engineer (YENGINEER); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 190; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: P.

Ordered plan: No Bridge Hover Attack (0AEAAB7C).

1. Move to waypoint: waypoint 15 (cell 135, 50).
2. Load transport.
3. Move to waypoint: waypoint 26 (cell 82, 135).
4. Unload with continuation mode: passengers continue; transport leaves team.
5. Seek/attack target category; configured argument 4.
6. Seek/attack target category; configured argument 6.
7. Seek/attack target category; configured argument 1.
8. Report team success.

<a id="team-0ba14efc"></a>

### Y Ground Attack - 0BA14EFC

Owner: YuriCountry. Roster: 5 × Initiate (INIT); 1 × Engineer (YENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 75; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Y Ground Attack (0AFA690C).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 3.
4. Seek/attack target category; configured argument 2.

<a id="team-089795dc"></a>

### Y MB Guard 1 - 089795DC

Owner: YuriCountry. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Y MB Guard 1 (0897BAEC).

1. Attack-move toward waypoint: waypoint 18 (cell 129, 42).
2. Attack-move toward waypoint: waypoint 17 (cell 129, 46).
3. Attack-move toward waypoint: waypoint 18 (cell 129, 42).
4. Guard for interval; configured argument 4.
5. Attack-move toward waypoint: waypoint 17 (cell 129, 46).
6. Attack-move toward waypoint: waypoint 18 (cell 129, 42).
7. Attack-move toward waypoint: waypoint 17 (cell 129, 46).
8. Attack-move toward waypoint: waypoint 18 (cell 129, 42).
9. Attack-move toward waypoint: waypoint 17 (cell 129, 46).
10. Guard for interval; configured argument 5.
11. Jump to script line; configured argument 1.

<a id="team-0897b4cc"></a>

### Y MB Guard 2 - 0897B4CC

Owner: YuriCountry. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Y MB Guard 2 (0897B14C).

1. Attack-move toward waypoint: waypoint 20 (cell 139, 54).
2. Attack-move toward waypoint: waypoint 19 (cell 135, 54).
3. Guard for interval; configured argument 3.
4. Attack-move toward waypoint: waypoint 20 (cell 139, 54).
5. Attack-move toward waypoint: waypoint 19 (cell 135, 54).
6. Attack-move toward waypoint: waypoint 20 (cell 139, 54).
7. Attack-move toward waypoint: waypoint 19 (cell 135, 54).
8. Attack-move toward waypoint: waypoint 20 (cell 139, 54).
9. Guard for interval; configured argument 5.
10. Attack-move toward waypoint: waypoint 19 (cell 135, 54).
11. Attack-move toward waypoint: waypoint 20 (cell 139, 54).
12. Attack-move toward waypoint: waypoint 19 (cell 135, 54).
13. Jump to script line; configured argument 1.

<a id="team-0897cefc"></a>

### Y MB Guard 3 - 0897CEFC

Owner: YuriCountry. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 70; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Y MB Guard 3 (0897CC8C).

1. Attack-move toward waypoint: waypoint 22 (cell 149, 54).
2. Attack-move toward waypoint: waypoint 21 (cell 145, 54).
3. Attack-move toward waypoint: waypoint 22 (cell 149, 54).
4. Guard for interval; configured argument 4.
5. Attack-move toward waypoint: waypoint 21 (cell 145, 54).
6. Attack-move toward waypoint: waypoint 22 (cell 149, 54).
7. Attack-move toward waypoint: waypoint 21 (cell 145, 54).
8. Attack-move toward waypoint: waypoint 22 (cell 149, 54).
9. Attack-move toward waypoint: waypoint 21 (cell 145, 54).
10. Guard for interval; configured argument 6.
11. Attack-move toward waypoint: waypoint 22 (cell 149, 54).
12. Attack-move toward waypoint: waypoint 21 (cell 145, 54).
13. Jump to script line; configured argument 1.

<a id="team-0b25259c"></a>

### Y SB Guard 1 - 0B25259C

Owner: YuriCountry2. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Y SB Guard 1 (068ECAEC).

1. Attack-move toward waypoint: waypoint 24 (cell 86, 90).
2. Guard for interval; configured argument 12.
3. Attack-move toward waypoint: waypoint 23 (cell 81, 90).
4. Guard for interval; configured argument 5.
5. Attack-move toward waypoint: waypoint 24 (cell 86, 90).
6. Attack-move toward waypoint: waypoint 23 (cell 81, 90).
7. Jump to script line; configured argument 1.

<a id="team-0b253efc"></a>

### Y SB Guard 2 - 0B253EFC

Owner: YuriCountry2. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Y SB Guard 2 (068EC3CC).

1. Attack-move toward waypoint: waypoint 23 (cell 81, 90).
2. Guard for interval; configured argument 10.
3. Attack-move toward waypoint: waypoint 24 (cell 86, 90).
4. Guard for interval; configured argument 4.
5. Attack-move toward waypoint: waypoint 23 (cell 81, 90).
6. Attack-move toward waypoint: waypoint 24 (cell 86, 90).
7. Guard for interval; configured argument 7.
8. Jump to script line; configured argument 1.

<a id="team-0bce121c"></a>

### No Bridge Hover Attack 2 - 0BCE121C

Owner: YuriCountry. Roster: 2 × Yuri Clone (YURI); 3 × Engineer (YENGINEER); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 50; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: No Bridge Hover Attack 2 (0AEAC6CC).

1. Move to waypoint: waypoint 15 (cell 135, 50).
2. Load transport.
3. Move to waypoint: waypoint 26 (cell 82, 135).
4. Unload with continuation mode: passengers continue; transport leaves team.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-0c1e4b0c"></a>

### Y Hover Team - 0C1E4B0C

Owner: YuriCountry. Roster: 2 × Engineer (YENGINEER); 3 × Initiate (INIT); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 95; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AB.

Ordered plan: Y Hover Team (0BADA90C).

1. Move to waypoint: waypoint 27 (cell 122, 46).
2. Load transport.
3. Move to waypoint: waypoint 26 (cell 82, 135).
4. Unload with continuation mode: passengers continue; transport leaves team.
5. Attack selected enemy-building category; configured argument 131072.
6. Seek/attack target category; configured argument 4.
7. Seek/attack target category; configured argument 1.

<a id="team-094146cc"></a>

### Y Auto Hover 1 - 094146CC

Owner: YuriCountry2. Roster: 2 × Engineer (YENGINEER); 2 × Gattling Tank (YTNK); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AI.

Ordered plan: Y Auto Hover 1 (0941445C).

1. Move to waypoint: waypoint 25 (cell 50, 153).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 0 (HoverDeliver).
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 1.

<a id="team-0c1e41ac"></a>

### Y Auto Hover 1b - 0C1E41AC

Owner: YuriCountry2. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 85; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Z.

Ordered plan: Y Auto Hover 1b (0A37B4AC).

1. Move to waypoint: waypoint 34 (cell 43, 160).
2. Delete team objects.

<a id="team-0b251dec"></a>

### Y SB Back Guard - 0B251DEC

Owner: YuriCountry2. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Y SB Back Guard (0AD46DBC).

1. Attack-move toward waypoint: waypoint 31 (cell 94, 106).
2. Guard for interval; configured argument 6.
3. Attack-move toward waypoint: waypoint 30 (cell 73, 106).
4. Guard for interval; configured argument 8.
5. Attack-move toward waypoint: waypoint 31 (cell 94, 106).
6. Guard for interval; configured argument 4.
7. Attack-move toward waypoint: waypoint 30 (cell 73, 106).
8. Guard for interval; configured argument 7.
9. Jump to script line; configured argument 1.

<a id="team-0b25412c"></a>

### Y SB Top Left Guard - 0B25412C

Owner: YuriCountry2. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Y SB Top Left Guard (0B47EDBC).

1. Attack-move toward waypoint: waypoint 30 (cell 73, 106).
2. Guard for interval; configured argument 10.
3. Attack-move toward waypoint: waypoint 33 (cell 73, 88).
4. Guard for interval; configured argument 4.
5. Attack-move toward waypoint: waypoint 30 (cell 73, 106).
6. Guard for interval; configured argument 8.
7. Attack-move toward waypoint: waypoint 33 (cell 73, 88).
8. Guard for interval; configured argument 10.
9. Jump to script line; configured argument 1.

<a id="team-0b255b7c"></a>

### Y SB Botm Rigt Guard - 0B255B7C

Owner: YuriCountry2. Roster: 1 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Y Botm Rigt Guard (0ACC590C).

1. Attack-move toward waypoint: waypoint 32 (cell 94, 88).
2. Guard for interval; configured argument 10.
3. Attack-move toward waypoint: waypoint 31 (cell 94, 106).
4. Guard for interval; configured argument 8.
5. Attack-move toward waypoint: waypoint 32 (cell 94, 88).
6. Guard for interval; configured argument 7.
7. Attack-move toward waypoint: waypoint 31 (cell 94, 106).
8. Guard for interval; configured argument 11.
9. Jump to script line; configured argument 1.

<a id="team-0c1e6c8c"></a>

### Y Auto Hover 2 - 0C1E6C8C

Owner: Alliance. Roster: 2 × Initiate (INIT); 1 × Yuri Clone (YURI); 2 × Gattling Tank (YTNK); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AJ.

Ordered plan: Auto Hover 2 (0A37B21C).

1. Move to waypoint: waypoint 36 (cell 137, 107).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 4 (HoverDeliver2).
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 1.

<a id="team-0c1e67dc"></a>

### Y Auto Hover 2b - 0C1E67DC

Owner: Alliance. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 85; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: Y Auto Hover 2b (0A37C74C).

1. Move to waypoint: waypoint 35 (cell 165, 48).
2. Delete team objects.

<a id="team-0bb0d7dc"></a>

### Einstein - 0BB0D7DC

Owner: Germans. Roster: 1 × Einstein (EINS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 200; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AL.

Ordered plan: Einstein (0BB0D56C).

1. Move to waypoint: waypoint 29 (cell 90, 103).

<a id="team-09417b7c"></a>

### Y Auto Hover 1 Alt - 09417B7C

Owner: Africans. Roster: 2 × Yuri Clone (YURI); 1 × Lasher Light Tank (LTNK); 1 × Gattling Tank (YTNK); 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AM.

Ordered plan: Y Auto Hover 1 Alt (0941790C).

1. Move to waypoint: waypoint 25 (cell 50, 153).
2. Unload with continuation mode: passengers continue; transport leaves team.
3. Set local flag: local flag 0 (HoverDeliver).
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 7.
6. Seek/attack target category; configured argument 1.

<a id="team-0c1e78ac"></a>

### Y Auto Hover 1b Alt - 0C1E78AC

Owner: Africans. Roster: 1 × Amphibious Transport (YHVR)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Z.

Ordered plan: Y Auto Hover 1b Alt (068B0DBC).

1. Move to waypoint: waypoint 38 (cell 34, 152).
2. Delete team objects.

<a id="team-0bb0e7dc"></a>

### Einstein Helicopter Rescue - 0BB0E7DC

Owner: Germans. Roster: 1 × NightHawk Transport (SHAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 200; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AA.

Ordered plan: Einstein Helicopter Rescue (0BB0E56C).

1. Move to waypoint: waypoint 39 (cell 84, 106).

<a id="team-0b0637dc"></a>

### Einstein 3 - 0B0637DC

Owner: Germans. Roster: 1 × Einstein (EINS); 1 × NightHawk Transport (SHAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AN.

Ordered plan: Einstein 3 (0B06356C).

1. Load transport.
2. Set local flag: local flag 12 (EinsteinIn).
3. Delete team objects.

<a id="team-08e77efc"></a>

### Y Team Kick Ass - 08E77EFC

Owner: YuriCountry. Roster: 3 × Gattling Tank (YTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 110; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Y Team Kick Ass (08E77C8C).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 4.
5. Report team success.
6. Seek/attack target category; configured argument 1.

<a id="team-08e77a4c"></a>

### Y Team Kick Ass 2 - 08E77A4C

Owner: YuriCountry. Roster: 3 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 125; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Y Team Kick Ass 2 (08E777DC).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 1.

<a id="team-0b3c604c"></a>

### _Dummy Team 1 - 0B3C604C

Owner: YuriCountry. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AQ.

Ordered plan: Dummy Team 1 (0B3C15CC).

1. Move to waypoint: waypoint 41 (cell 82, 157).

<a id="team-0b3c129c"></a>

### _Dummy Team 2 - 0B3C129C

Owner: YuriCountry. Roster: 1 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AR.

Ordered plan: Dummy Team 2 (0B3C3DBC).

1. Move to waypoint: waypoint 41 (cell 82, 157).

<a id="team-0c1eac8c"></a>

### _Tank Des 1 - 0C1EAC8C

Owner: Americans. Roster: 1 × Tank Destroyer (TNKD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BO.

Ordered plan: Tank Des 1 (0BC5090C).

1. Move to waypoint: waypoint 44 (cell 78, 162).
2. Set facing; configured argument 0.
3. Guard for interval; configured argument 100.

<a id="team-0c1ea7dc"></a>

### _Tank Des 2 - 0C1EA7DC

Owner: Americans. Roster: 1 × Tank Destroyer (TNKD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BN.

Ordered plan: Tank Des 2 (0BCFF21C).

1. Move to waypoint: waypoint 45 (cell 79, 159).
2. Set facing; configured argument 0.
3. Guard for interval; configured argument 100.

<a id="team-0c1ea15c"></a>

### _Tank Des 3 - 0C1EA15C

Owner: Americans. Roster: 1 × Tank Destroyer (TNKD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BT.

Ordered plan: Tank Des 3 (0BD5A42C).

1. Move to waypoint: waypoint 46 (cell 86, 162).
2. Set facing; configured argument 0.
3. Guard for interval; configured argument 100.

<a id="team-0c1ebc8c"></a>

### _Tank Des 4 - 0C1EBC8C

Owner: Americans. Roster: 1 × Tank Destroyer (TNKD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BU.

Ordered plan: Tank Des 4 (0BD5CC8C).

1. Move to waypoint: waypoint 47 (cell 85, 159).
2. Set facing; configured argument 0.
3. Guard for interval; configured argument 100.

<a id="team-0ba1da4c"></a>

### Yuri Clone Fun - 0BA1DA4C

Owner: YuriCountry. Roster: 5 × Yuri Clone (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 106; Max: 5; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri Clone Fun (043836FC).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 5.
6. Report team success.
7. Seek/attack target category; configured argument 1.

<a id="team-0ba1d59c"></a>

### Even More Fun! - 0BA1D59C

Owner: YuriCountry. Roster: 5 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 90; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Even More Fun! (0922ADBC).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 1.

<a id="team-0d89c48c"></a>

### Yuri Harvester 1 - 0D89C48C

Owner: YuriCountry. Roster: 1 × Slave Miner (SMIN)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: -1; Veteran Level: 1; Technology level: 0; Waypoint: BF.

Ordered plan: Yuri Harvester 1 (0D8A629C).

1. Deploy.

<a id="team-0d8a3ebc"></a>

### Yuri Harvester 2 - 0D8A3EBC

Owner: YuriCountry. Roster: 1 × Slave Miner (SMIN)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BG.

Ordered plan: Yuri Harvester 2 (0D8A781C).

1. Deploy.

<a id="team-0933db7c"></a>

### MVC Move - 0933DB7C

Owner: Americans. Roster: 1 × Allied Construction Vehicle (AMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AW.

Ordered plan: MCV Move (0933D90C).

1. Move to waypoint: waypoint 0 (cell 82, 162).
2. Guard for interval; configured argument 55.
3. Deploy.

<a id="team-0ba1e1ac"></a>

### Engin1Move - 0BA1E1AC

Owner: Americans. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BP.

Ordered plan: Engin1Move (092835EC).

1. Move to waypoint: waypoint 59 (cell 78, 164).

<a id="team-0ba260ec"></a>

### GI1Move - 0BA260EC

Owner: Americans. Roster: 1 × GI (E1); 1 × Attack Dog (ADOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BQ.

Ordered plan: GI1Move (09284DBC).

1. Move to waypoint: waypoint 60 (cell 79, 166).

<a id="team-0ba275ec"></a>

### GI2Move - 0BA275EC

Owner: Americans. Roster: 1 × GI (E1); 1 × Attack Dog (ADOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BR.

Ordered plan: GI2Move (0928412C).

1. Move to waypoint: waypoint 62 (cell 85, 166).

<a id="team-0ba176cc"></a>

### Engin2Move - 0BA176CC

Owner: Americans. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BS.

Ordered plan: Engin2Move (0928589C).

1. Move to waypoint: waypoint 63 (cell 86, 164).

<a id="team-093a031c"></a>

### _FriendlyDinos - 093A031C

Owner: Americans. Roster: 3 × T-Rex (DNOA)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BV.

Ordered plan: FriendlyDinos (093A507C).

1. Adopt object mission: area guard.

<a id="team-08d12c8c"></a>

### _New Gattling Team! - 08D12C8C

Owner: YuriCountry. Roster: 2 × Gattling Tank (YTNK); 2 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 110; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: New Gattling Tank Attack (08D12A1C).

1. Attack-move toward waypoint: waypoint 74 (cell 106, 170).
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Adopt object mission: hunt.
5. Report team success.
6. Seek/attack target category; configured argument 1.

<a id="team-08d127dc"></a>

### _New Evil Lashers! - 08D127DC

Owner: YuriCountry. Roster: 3 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 110; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Lasher Attack Harvesters (08D1256C).

1. Attack-move toward waypoint: waypoint 2 (cell 58, 133).
2. Attack-move toward waypoint: waypoint 25 (cell 50, 153).
3. Seek/attack target category; configured argument 3.
4. Report team success.
5. Seek/attack target category; configured argument 5.
6. Report team success.
7. Seek/attack target category; configured argument 1.

<a id="team-0c1ef60c"></a>

### _Oil Derrickers! - 0C1EF60C

Owner: YuriCountry. Roster: 5 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 150; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Engineer Attack Tech (043E96CC).

1. Seek/attack target category; configured argument 11.
2. Report team success.

<a id="team-0997621c"></a>

### _Easy Reinforcements - 0997621C

Owner: Americans. Roster: 4 × Guardian GI (GGI); 2 × Tank Destroyer (TNKD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CA.

Ordered plan: _Easy Reinforcement 1 (09975DBC).

1. Scatter.
2. Move to waypoint: waypoint 108 (cell 93, 166).

<a id="team-09975b7c"></a>

### _Easy Reinforcment 2 - 09975B7C

Owner: Americans. Roster: 2 × Sniper (SNIPE); 4 × Rocketeer (JUMPJET); 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CB.

Ordered plan: _Easy Reinforcement 2 (0997590C).

1. Scatter.
2. Move to waypoint: waypoint 109 (cell 70, 159).

<a id="team-08d1d32c"></a>

### _Easy Reinforcment 3 - 08D1D32C

Owner: Americans. Roster: 5 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BX.

Ordered plan: _Easy Reinforcement 3 (0997545C).

1. Scatter.
2. Move to waypoint: waypoint 108 (cell 93, 166).

<a id="team-08619c8c"></a>

### Medium Power CR - 08619C8C

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BB.

Ordered plan: Power Building CR (0BA2221C).

1. Enter Bio Reactor.

<a id="team-086197dc"></a>

### Medium Power CF - 086197DC

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Medium Power CF (0BA23A6C).

1. Enter Bio Reactor.

<a id="team-0861943c"></a>

### Medium Power CI - 0861943C

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: Meduim Power CI (0BA236CC).

1. Enter Bio Reactor.

<a id="team-0861a9fc"></a>

### Medium Power CN - 0861A9FC

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: V.

Ordered plan: Medium Power CN (0BA2332C).

1. Enter Bio Reactor.

<a id="team-0861a65c"></a>

### Medium Power CL - 0861A65C

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AZ.

Ordered plan: Medium Power CL (0BA24DBC).

1. Enter Bio Reactor.

<a id="team-0ba230cc"></a>

### Hard Power CK - 0BA230CC

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: P.

Ordered plan: Hard Power CK (0BA21C8C).

1. Enter Bio Reactor.

<a id="team-0ba2497c"></a>

### Hard Power CM - 0BA2497C

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: P.

Ordered plan: Hard Power CM (0BA2470C).

1. Enter Bio Reactor.

<a id="team-0ba245dc"></a>

### Hard Power CH - 0BA245DC

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: P.

Ordered plan: Hard Power CH (0BA2436C).

1. Enter Bio Reactor.

<a id="team-0ba2423c"></a>

### Hard Power CG - 0BA2423C

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: P.

Ordered plan: Hard Power CG (0BA25DBC).

1. Enter Bio Reactor.

<a id="team-0ba2410c"></a>

### Hard Power CP - 0BA2410C

Owner: YuriCountry. Roster: 3 × Initiate (INIT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: P.

Ordered plan: Hard Power CP (0BA25B4C).

1. Enter Bio Reactor.

<a id="team-0c8608ec"></a>

### Bonus Team - 0C8608EC

Owner: Americans. Roster: 1 × Sniper (SNIPE); 1 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CU.

Ordered plan: Bonus Team (0C86067C).

1. Move to waypoint: waypoint 73 (cell 19, 129).

<a id="team-092b87dc"></a>

### _A04_Camels Z - 092B87DC

Owner: Neutral. Roster: 2 × Camel (CAML)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 100; Veteran Level: 1; Technology level: 0; Waypoint: Z.

Ordered plan: Wander (07A33DBC).

1. Move to waypoint: waypoint 42 (cell 70, 148).
2. Guard for interval; configured argument 30.
3. Move to waypoint: waypoint 43 (cell 89, 149).
4. Guard for interval; configured argument 21.
5. Move to waypoint: waypoint 99 (cell 99, 132).
6. Guard for interval; configured argument 25.
7. Move to waypoint: waypoint 25 (cell 50, 153).
8. Guard for interval; configured argument 23.
9. Jump to script line; configured argument 1.

<a id="team-079af23c"></a>

### _A04_Camels AK - 079AF23C

Owner: Neutral. Roster: 2 × Camel (CAML)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AK.

Ordered plan: Wanderers (079B0DBC).

1. Move to waypoint: waypoint 36 (cell 137, 107).
2. Guard for interval; configured argument 20.
3. Move to waypoint: waypoint 100 (cell 132, 141).
4. Guard for interval; configured argument 26.
5. Move to waypoint: waypoint 101 (cell 98, 153).
6. Guard for interval; configured argument 32.
7. Move to waypoint: waypoint 36 (cell 137, 107).
8. Guard for interval; configured argument 25.
9. Jump to script line; configured argument 1.

<a id="team-079b093c"></a>

### _A04_Camels CY - 079B093C

Owner: Neutral. Roster: 3 × Camel (CAML)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CY.

Ordered plan: Wandering Camels 3 (079B2DBC).

1. Move to waypoint: waypoint 103 (cell 91, 47).
2. Guard for interval; configured argument 19.
3. Move to waypoint: waypoint 104 (cell 18, 117).
4. Guard for interval; configured argument 25.
5. Move to waypoint: waypoint 105 (cell 41, 118).
6. Guard for interval; configured argument 31.
7. Move to waypoint: waypoint 106 (cell 62, 77).
8. Guard for interval; configured argument 23.
9. Move to waypoint: waypoint 102 (cell 124, 13).
10. Guard for interval; configured argument 21.
11. Jump to script line; configured argument 1.

<a id="team-09070b7c"></a>

### _A04_Mummy 1 - 09070B7C

Owner: Africans. Roster: 1 × Mummy (MUMY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: DD.

Ordered plan: Mummy Attacks! (0907090C).

1. Seek/attack target category; configured argument 1.

<a id="team-090706cc"></a>

### _A04_Mummy 2 - 090706CC

Owner: Africans. Roster: 1 × Mummy (MUMY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CK.

Ordered plan: Area Guard (0907045C).

1. Seek/attack target category; configured argument 1.

<a id="team-0907032c"></a>

### _A04_Mummy 3 - 0907032C

Owner: Africans. Roster: 1 × Mummy (MUMY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: DG.

Ordered plan: Area Guard (0907045C).

1. Seek/attack target category; configured argument 1.

<a id="team-090701fc"></a>

### _A04_Mummy 4 - 090701FC

Owner: Africans. Roster: 1 × Mummy (MUMY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: DH.

Ordered plan: Area Guard (0907045C).

1. Seek/attack target category; configured argument 1.

<a id="team-094fe68c"></a>

### _A04_Tanya Intro - 094FE68C

Owner: British. Roster: 1 × NightHawk Transport (SHAD); 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 200; Max: 1; Veteran Level: 3; Technology level: 0; Waypoint: DJ.

Ordered plan: Fly in (094FE41C).

1. Move to waypoint: waypoint 41 (cell 82, 157).
2. Unload with continuation mode: transport and passengers continue.
3. Set local flag: local flag 9 (TanyaOut).
4. Change country ownership; configured argument 0.

<a id="team-0780644c"></a>

### Einstein 3a - 0780644C

Owner: Germans. Roster: 1 × NightHawk Transport (SHAD); 1 × Einstein (EINS)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 100; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AN.

Ordered plan: Fly Away! (078061DC).

1. Load transport.
2. Delete team objects.

<a id="team-0817f38c"></a>

### _A04_Too Many Tanks - 0817F38C

Owner: YuriCountry. Roster: 4 × Lasher Light Tank (LTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 110; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Cut Down The Tanks (0817F11C).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 5.
4. Seek/attack target category; configured argument 5.
5. Seek/attack target category; configured argument 5.
6. Seek/attack target category; configured argument 5.
7. Seek/attack target category; configured argument 5.
8. Seek/attack target category; configured argument 5.
9. Seek/attack target category; configured argument 5.
10. Seek/attack target category; configured argument 1.
11. Adopt object mission: area guard.
