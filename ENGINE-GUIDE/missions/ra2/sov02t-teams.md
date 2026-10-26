# Operation: Hostile Shore - team rosters and plans

[Trigger ledger](sov02t.md) | [Mission overrides](sov02t-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov02t.map; each team/script ID identifies its section.

<a id="team-09f15c8c"></a>

### Wave 2.2 - 09F15C8C

Owner: Confederation. Roster: 1 × Amphibious Transport (SAPC); 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 3; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Beach Assault X (09F15A1C).

1. Move to waypoint: waypoint 23 (cell 81, 60).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Set local flag: local flag 2 (Transports Unloaded).
4. Change country ownership; configured argument 5.

<a id="team-0c4b427c"></a>

### PC Landers 1 - 0C4B427C

Owner: Confederation. Roster: 1 × Soviet Construction Vehicle (SMCV); 1 × Amphibious Transport (SAPC); 3 × Engineer (SENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Player Transports (0992C860).

1. Move to waypoint: waypoint 24 (cell 89, 56).

<a id="team-0c4b403c"></a>

### PC Landers 2 - 0C4B403C

Owner: Confederation. Roster: 1 × Amphibious Transport (SAPC); 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Beach Assualt (090F8A40).

1. Move to waypoint: waypoint 0 (cell 80, 55).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Change country ownership; configured argument 5.

<a id="team-0c4b190c"></a>

### PC Landers 3 - 0C4B190C

Owner: Confederation. Roster: 2 × Rhino Heavy Tank (HTNK); 1 × Amphibious Transport (SAPC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: E.

Ordered plan: Beach Assault W (090F85C0).

1. Move to waypoint: waypoint 22 (cell 82, 52).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Change country ownership; configured argument 5.

<a id="team-0a9de7dc"></a>

### Vlad's Charge Team - 0A9DE7DC

Owner: Russians. Roster: 1 × Vladimir's Command Ship (VLAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Vladmir's Crazy Attack (0A9E7C8C).

1. Move to waypoint: waypoint 7 (cell 105, 71).
2. Move to waypoint: waypoint 8 (cell 108, 86).
3. Move to waypoint: waypoint 9 (cell 113, 94).
4. Move to waypoint: waypoint 8 (cell 108, 86).
5. Move to waypoint: waypoint 7 (cell 105, 71).
6. Move to waypoint: waypoint 10 (cell 91, 59).
7. Move to waypoint: waypoint 55 (cell 102, 37).
8. Delete team objects.

<a id="team-09ec293c"></a>

### 3 Destroyers - 09EC293C

Owner: Americans. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 3; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: L.

Ordered plan: Kill Vlad (0A1AE90C).

1. Guard for interval; configured argument 20.
2. Attack-move toward waypoint: waypoint 5 (cell 84, 56).
3. Attack selected enemy-building category; configured argument 61.
4. Attack selected enemy-building category; configured argument 25.
5. Seek/attack target category; configured argument 5.
6. Move to waypoint: waypoint 5 (cell 84, 56).
7. Adopt object mission: area guard.

<a id="team-0a2e2bb0"></a>

### Fleet Guard - 0A2E2BB0

Owner: Americans. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 3; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: G.

Ordered plan: Move out the Fleet (07F66980).

1. Move to waypoint: waypoint 15 (cell 111, 100).
2. Move to waypoint: waypoint 11 (cell 109, 102).
3. Move to waypoint: waypoint 9 (cell 113, 94).
4. Move to waypoint: waypoint 16 (cell 106, 66).
5. Move to waypoint: waypoint 17 (cell 94, 95).

<a id="team-0a2e2840"></a>

### Fleet 1 - 0A2E2840

Owner: Americans. Roster: 2 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 3; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: M.

Ordered plan: Move out the Fleet (07F66980).

1. Move to waypoint: waypoint 15 (cell 111, 100).
2. Move to waypoint: waypoint 11 (cell 109, 102).
3. Move to waypoint: waypoint 9 (cell 113, 94).
4. Move to waypoint: waypoint 16 (cell 106, 66).
5. Move to waypoint: waypoint 17 (cell 94, 95).

<a id="team-0a2e2630"></a>

### Fleet 2 - 0A2E2630

Owner: Americans. Roster: 2 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 3; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: N.

Ordered plan: Move out the Fleet (07F66980).

1. Move to waypoint: waypoint 15 (cell 111, 100).
2. Move to waypoint: waypoint 11 (cell 109, 102).
3. Move to waypoint: waypoint 9 (cell 113, 94).
4. Move to waypoint: waypoint 16 (cell 106, 66).
5. Move to waypoint: waypoint 17 (cell 94, 95).

<a id="team-0a2e2520"></a>

### Fleet 3 - 0A2E2520

Owner: Americans. Roster: 2 × Amphibious Transport (LCRF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 3; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: O.

Ordered plan: Move out the Fleet (07F66980).

1. Move to waypoint: waypoint 15 (cell 111, 100).
2. Move to waypoint: waypoint 11 (cell 109, 102).
3. Move to waypoint: waypoint 9 (cell 113, 94).
4. Move to waypoint: waypoint 16 (cell 106, 66).
5. Move to waypoint: waypoint 17 (cell 94, 95).

<a id="team-0c4b3c4c"></a>

### Wave 2.1 - 0C4B3C4C

Owner: Confederation. Roster: 1 × Amphibious Transport (SAPC); 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: T.

Ordered plan: Beach Assault AQ (090FBCA0).

1. Move to waypoint: waypoint 42 (cell 80, 58).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Change country ownership; configured argument 5.

<a id="team-0abbab5c"></a>

### America Defense - 0ABBAB5C

Owner: Americans. Roster: 4 × GI (E1)

Explicit team settings: Autocreate: yes; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 5; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: General Base Defense (09F01CBC).

1. Adopt object mission: area guard.

<a id="team-09faf7ec"></a>

### America GI Attack - 09FAF7EC

Owner: Americans. Roster: 6 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 10; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: American Attack (09E6E20C).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 6.
3. Seek/attack target category; configured argument 9.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 5.

<a id="team-0ad12a4c"></a>

### America Armor Attack - 0AD12A4C

Owner: Americans. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 10; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: American Attack (09E6E20C).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 6.
3. Seek/attack target category; configured argument 9.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 5.

<a id="team-0c4b308c"></a>

### wave 2.3 - 0C4B308C

Owner: Confederation. Roster: 1 × Amphibious Transport (SAPC); 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: E.

Ordered plan: Beach Assault AT (090FB3C0).

1. Move to waypoint: waypoint 45 (cell 81, 54).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Change country ownership; configured argument 5.

<a id="team-0c4b0c8c"></a>

### wave 2.4 - 0C4B0C8C

Owner: Confederation. Roster: 1 × Amphibious Transport (SAPC); 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Z.

Ordered plan: Beach Assault AR (090FDDC0).

1. Move to waypoint: waypoint 43 (cell 82, 49).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Change country ownership; configured argument 5.

<a id="team-0c4b08ec"></a>

### wave 2.5 - 0C4B08EC

Owner: Confederation. Roster: 2 × Rhino Heavy Tank (HTNK); 1 × Amphibious Transport (SAPC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AA.

Ordered plan: Beach Assault AE (090FDA40).

1. Move to waypoint: waypoint 30 (cell 82, 46).
2. Unload with continuation mode: transport continues; passengers leave team.
3. Change country ownership; configured argument 5.

<a id="team-0afd1b5c"></a>

### Vlad Attack Team - 0AFD1B5C

Owner: Russians. Roster: 1 × Vladimir's Command Ship (VLAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Fire Missile Barrage (0AFD18EC).

1. Attack waypoint: waypoint 28 (cell 78, 55).
2. Attack waypoint: waypoint 58 (cell 78, 57).
3. Set facing; configured argument 6.
4. Guard for interval; configured argument 30.
5. Attack waypoint: waypoint 46 (cell 71, 43).
6. Guard for interval; configured argument 30.
7. Attack waypoint: waypoint 48 (cell 76, 34).
8. Guard for interval; configured argument 30.
9. Attack waypoint: waypoint 47 (cell 70, 35).
10. Guard for interval; configured argument 30.
11. Attack waypoint: waypoint 49 (cell 73, 28).
12. Adopt object mission: stop.

<a id="team-0a081a1c"></a>

### Vlad is Sleepy - 0A081A1C

Owner: Russians. Roster: 1 × Vladimir's Command Ship (VLAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Sleep (0A0817AC).

1. Adopt object mission: stop.

<a id="team-0ad69c8c"></a>

### USA first attack - 0AD69C8C

Owner: Americans. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 2; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: AF.

Ordered plan: USA 1st Attack (0A008DBC).

1. Move to waypoint: waypoint 64 (cell 63, 81).
2. Seek/attack target category; configured argument 5.
3. Seek/attack target category; configured argument 4.
4. Seek/attack target category; configured argument 2.

<a id="team-0a550dcc"></a>

### Land the MCV - 0A550DCC

Owner: Africans. Roster: 1 × Amphibious Transport (SAPC); 1 × Soviet Construction Vehicle (SMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 1; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Q.

Ordered plan: Land MCV (0A550B5C).

1. Move to waypoint: waypoint 57 (cell 73, 56).
2. Unload with continuation mode: transport and passengers continue.
3. Guard for interval; configured argument 1.
4. Set local flag: local flag 0 (MCV Landed).

<a id="team-08cd1cdc"></a>

### Destroyer Patrols - 08CD1CDC

Owner: Americans. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: G.

Ordered plan: Patrol (09F4FCB0).

1. Attack-move toward waypoint: waypoint 15 (cell 111, 100).
2. Attack-move toward waypoint: waypoint 6 (cell 99, 117).
3. Jump to script line; configured argument 1.

<a id="team-09ea248c"></a>

### American Navy - 09EA248C

Owner: Americans. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Destrpoyer Behavior (0AE6FC8C).

1. Attack-move toward waypoint: waypoint 10 (cell 91, 59).
2. Attack selected enemy-building category; configured argument 131133.
3. Report team success.
4. Attack selected enemy-building category; configured argument 25.
5. Attack selected enemy-building category; configured argument 15.
6. Attack selected enemy-building category; configured argument 11.
7. Adopt object mission: area guard.

<a id="team-0cf1832c"></a>

### Destroyer Attack - 0CF1832C

Owner: Americans. Roster: 1 × Destroyer (DEST)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: G.

Ordered plan: Destrpoyer Behavior (0AE6FC8C).

1. Attack-move toward waypoint: waypoint 10 (cell 91, 59).
2. Attack selected enemy-building category; configured argument 131133.
3. Report team success.
4. Attack selected enemy-building category; configured argument 25.
5. Attack selected enemy-building category; configured argument 15.
6. Attack selected enemy-building category; configured argument 11.
7. Adopt object mission: area guard.

<a id="team-09ea176c"></a>

### American Hard Attack - 09EA176C

Owner: Americans. Roster: 4 × Grizzly Battle Tank (MTNK); 6 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 15; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Anything (09F2BDC0).

1. Seek/attack target category; configured argument 1.

<a id="team-090edce0"></a>

### 7 Transports - 090EDCE0

Owner: Africans. Roster: 7 × Amphibious Transport (SAPC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: Get off map (0A30E43C).

1. Move to waypoint: waypoint 55 (cell 102, 37).
2. Delete team objects.

<a id="team-0a30e1fc"></a>

### Make Boat Go Away - 0A30E1FC

Owner: Africans. Roster: 1 × Amphibious Transport (SAPC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BF.

Ordered plan: Get off map (0A30E43C).

1. Move to waypoint: waypoint 55 (cell 102, 37).
2. Delete team objects.

<a id="team-0a1db35c"></a>

### MCV ON the Beach - 0A1DB35C

Owner: Africans. Roster: 1 × Soviet Construction Vehicle (SMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BF.

Ordered plan: Change House (09A20DBC).

1. Change country ownership; configured argument 7.

<a id="team-094236fc"></a>

### 3 Soviet Engineers - 094236FC

Owner: Confederation. Roster: 3 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 50; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BF.

Ordered plan: Scatter Engineers (0952C90C).

1. Move to waypoint: waypoint 54 (cell 69, 58).

<a id="team-0be41a9c"></a>

### American Big Attack - 0BE41A9C

Owner: Americans. Roster: 6 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: American Attack (09E6E20C).

1. Gather near enemy base; configured argument 0.
2. Seek/attack target category; configured argument 6.
3. Seek/attack target category; configured argument 9.
4. Seek/attack target category; configured argument 2.
5. Seek/attack target category; configured argument 5.

<a id="team-09e73bac"></a>

### American Mixed Team - 09E73BAC

Owner: Americans. Roster: 1 × Grizzly Battle Tank (MTNK); 4 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Clever American Attack (09E7393C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 37 (cell 51, 69).
3. Seek/attack target category; configured argument 1.

<a id="team-09f1c80c"></a>

### American Engineer Attack - 09F1C80C

Owner: Americans. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Engineer Attack (09F1C59C).

1. Approach selected enemy-building category; configured argument 9.
2. Attack selected enemy-building category; configured argument 9.

<a id="team-0a22fdec"></a>

### 9 Civilians - 0A22FDEC

Owner: Neutral. Roster: 3 × Civilian (CIVBFM); 3 × Civilian (CIVBF); 3 × Civilian (CIVBTM)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 10; Veteran Level: 1; Technology level: 0; Waypoint: AM.

Ordered plan: panic! (093E9B4C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-09e2a1fc"></a>

### 6 Free Subs - 09E2A1FC

Owner: Confederation. Roster: 4 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BD.

Ordered plan: Subs Reinforce (09E28DBC).

1. Move to waypoint: waypoint 10 (cell 91, 59).

<a id="team-0a2b50dc"></a>

### Conscript Reinforcements - 0A2B50DC

Owner: Confederation. Roster: 10 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 15; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: AO.

Ordered plan: Guard Area (09CA58CC).

1. Adopt object mission: area guard.

<a id="team-0a2271fc"></a>

### 9 Civies North - 0A2271FC

Owner: Neutral. Roster: 3 × Civilian (CIVBFM); 3 × Civilian (CIVBF); 3 × Civilian (CIVBTM)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: AP.

Ordered plan: panic! (093E9B4C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-09f136ac"></a>

### 6 Civies South - 09F136AC

Owner: Neutral. Roster: 2 × Civilian (CIVBFM); 2 × Civilian (CIVBF); 2 × Civilian (CIVBTM)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 5; Veteran Level: 1; Technology level: 0; Waypoint: AS.

Ordered plan: panic! (093E9B4C).

1. Panic.
2. Jump to script line; configured argument 1.

<a id="team-09dff26c"></a>

### 4 Transports - Hard - 09DFF26C

Owner: Africans. Roster: 4 × Amphibious Transport (SAPC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: Get off map (0A30E43C).

1. Move to waypoint: waypoint 55 (cell 102, 37).
2. Delete team objects.

<a id="team-0afb538c"></a>

### 2 Chrono Harvesters - 0AFB538C

Owner: Americans. Roster: 2 × Chrono Miner (CMIN)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 50; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Chrono Miner Attack (09CA3DBC).

1. Move to waypoint: waypoint 64 (cell 63, 81).

<a id="team-0ab8380c"></a>

### Vlad Sneaks Back On - 0AB8380C

Owner: Russians. Roster: 1 × Vladimir's Command Ship (VLAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BD.

Ordered plan: Vlad Sneaks back on. (0AB8097C).

1. Move to waypoint: waypoint 98 (cell 93, 50).
2. Move to waypoint: waypoint 9 (cell 113, 94).
3. Attack waypoint: waypoint 93 (cell 124, 128).
4. Attack waypoint: waypoint 94 (cell 117, 124).
5. Attack waypoint: waypoint 95 (cell 65, 58).
6. Attack waypoint: waypoint 99 (cell 66, 61).
7. Attack waypoint: waypoint 100 (cell 88, 93).
8. Move to waypoint: waypoint 10 (cell 91, 59).
9. Adopt object mission: area guard.

<a id="team-0af55b5c"></a>

### vlad runs again - 0AF55B5C

Owner: Russians. Roster: 1 × Vladimir's Command Ship (VLAD)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: J.

Ordered plan: Vlad runs away (0AAA4C8C).

1. Move to waypoint: waypoint 10 (cell 91, 59).
2. Move to waypoint: waypoint 55 (cell 102, 37).
3. Clear local flag: local flag 3 (Vlad is Hit).
4. Delete team objects.

<a id="team-08608aec"></a>

### 10 Free Subs - 08608AEC

Owner: Confederation. Roster: 10 × Typhoon Attack Sub (SUB)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 5; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: BD.

Ordered plan: Subs Reinforce (09E28DBC).

1. Move to waypoint: waypoint 10 (cell 91, 59).
