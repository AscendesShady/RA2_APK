# Operation: Free Gateway - team rosters and plans

[Trigger ledger](all08u.md) | [Mission overrides](all08u-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS01.MIX/all08u.map; each team/script ID identifies its section.

<a id="team-0a99211c"></a>

### Player Start Force - 0A99211C

Owner: Player. Roster: 5 × GI (E1); 2 × Engineer (ENGINEER); 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 3; Technology level: 0; Waypoint: B; Transport Waypoint: C.

Ordered plan: Player Start Force SCR (0740F56C).

1. Adopt object mission: guard.
2. Report team success.

<a id="team-09b81684"></a>

### GILanders - 09B81684

Owner: Player. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: GILanders SCR (07A9CB4C).

1. Change country ownership; configured argument 19.

<a id="team-0ac59b7c"></a>

### EngineerLanders - 0AC59B7C

Owner: Player. Roster: 2 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: EngineerLanders SCR (0AC5990C).

1. Set local flag: local flag 12 (Engineer Fix).
2. Change country ownership; configured argument 20.

<a id="team-09b80694"></a>

### TanyaLanders - 09B80694

Owner: Player. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: TanyaLanders SCR (079C0A1C).

1. Change country ownership; configured argument 18.

<a id="team-0ce11dec"></a>

### Player Reinforcements 1 - 0CE11DEC

Owner: Reinforcers. Roster: 1 × Amphibious Transport (LCRF); 1 × Prism Tank (SREF); 1 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Player Reinforcements SCR (0CE11B7C).

1. Move to waypoint: waypoint 5 (cell 148, 81).
2. Set local flag: local flag 1 (Reinforcments Arriv).
3. Move to waypoint: waypoint 18 (cell 115, 84).
4. Unload with continuation mode: transport continues; passengers leave team.
5. Set local flag: local flag 10 (Prism 1 Unloaded).
6. Move to waypoint: waypoint 45 (cell 115, 88).
7. Change country ownership; configured argument 13.
8. Adopt object mission: guard.

<a id="team-081104f4"></a>

### Beacon Perimeter Patrol - 081104F4

Owner: BadGuy2. Roster: 5 × Conscript (E2); 2 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 9; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: G.

Ordered plan: Beacon Perimeter Patrol SCR (08F897B4).

1. Attack-move toward waypoint: waypoint 7 (cell 39, 88).
2. Guard for interval; configured argument 10.
3. Attack-move toward waypoint: waypoint 8 (cell 56, 88).
4. Guard for interval; configured argument 10.
5. Attack-move toward waypoint: waypoint 9 (cell 56, 100).
6. Guard for interval; configured argument 10.
7. Attack-move toward waypoint: waypoint 10 (cell 56, 113).
8. Guard for interval; configured argument 10.
9. Attack-move toward waypoint: waypoint 11 (cell 48, 113).
10. Guard for interval; configured argument 10.
11. Attack-move toward waypoint: waypoint 10 (cell 56, 113).
12. Guard for interval; configured argument 10.
13. Attack-move toward waypoint: waypoint 9 (cell 56, 100).
14. Guard for interval; configured argument 10.
15. Attack-move toward waypoint: waypoint 8 (cell 56, 88).
16. Guard for interval; configured argument 10.
17. Attack-move toward waypoint: waypoint 7 (cell 39, 88).
18. Guard for interval; configured argument 10.
19. Attack-move toward waypoint: waypoint 6 (cell 39, 106).
20. Guard for interval; configured argument 10.
21. Jump to script line; configured argument 1.

<a id="team-0b996384"></a>

### Evil Patrol 1 - 0B996384

Owner: BadGuy1. Roster: 1 × Technician (CTECH); 4 × GI (E1); 1 × Attack Dog (ADOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 3; Veteran Level: 1; Technology level: 0; Waypoint: M.

Ordered plan: Evil Patrol 1 SCR (09721DB4).

1. Scatter.
2. Attack-move toward waypoint: waypoint 4 (cell 114, 80).
3. Guard for interval; configured argument 12.
4. Attack-move toward waypoint: waypoint 13 (cell 114, 113).
5. Guard for interval; configured argument 12.
6. Attack-move toward waypoint: waypoint 14 (cell 96, 113).
7. Guard for interval; configured argument 12.
8. Attack-move toward waypoint: waypoint 15 (cell 89, 80).
9. Guard for interval; configured argument 12.
10. Attack-move toward waypoint: waypoint 16 (cell 95, 47).
11. Guard for interval; configured argument 12.
12. Attack-move toward waypoint: waypoint 12 (cell 114, 47).
13. Guard for interval; configured argument 12.
14. Jump to script line; configured argument 2.

<a id="team-0ce10dec"></a>

### Player Reinforcements 2 - 0CE10DEC

Owner: Reinforcers. Roster: 1 × Amphibious Transport (LCRF); 1 × Grizzly Battle Tank (MTNK); 1 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Player Reinforcements 2 SCR (0CE10B7C).

1. Move to waypoint: waypoint 5 (cell 148, 81).
2. Move to waypoint: waypoint 19 (cell 115, 76).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Set local flag: local flag 11 (Prism 2 Unloaded).
5. Move to waypoint: waypoint 46 (cell 115, 72).
6. Change country ownership; configured argument 13.
7. Adopt object mission: guard.

<a id="team-0ce1093c"></a>

### Player Reinforcements 3 - 0CE1093C

Owner: Reinforcers. Roster: 1 × Amphibious Transport (LCRF); 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Player Reinforcements 3 SCR (0CE106CC).

1. Move to waypoint: waypoint 5 (cell 148, 81).
2. Move to waypoint: waypoint 17 (cell 111, 80).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Set local flag: local flag 15 (3 Unloaded).
5. Move to waypoint: waypoint 45 (cell 115, 88).
6. Change country ownership; configured argument 13.
7. Adopt object mission: guard.

<a id="team-0ce1048c"></a>

### Player Reinforcements 4 - 0CE1048C

Owner: Reinforcers. Roster: 1 × Amphibious Transport (LCRF); 1 × Allied Construction Vehicle (AMCV); 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Player Reinforcements 4 SCR (0CE1021C).

1. Move to waypoint: waypoint 5 (cell 148, 81).
2. Move to waypoint: waypoint 4 (cell 114, 80).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Set local flag: local flag 16 (4 Unloaded).
5. Move to waypoint: waypoint 46 (cell 115, 72).
6. Change country ownership; configured argument 13.
7. Adopt object mission: guard.

<a id="team-08f73af4"></a>

### Evil Patrol 2 - 08F73AF4

Owner: BadGuy1. Roster: 2 × Technician (CTECH); 3 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: Y.

Ordered plan: Evil Patrol 2 SCR (0972FA04).

1. Scatter.
2. Attack-move toward waypoint: waypoint 22 (cell 66, 72).
3. Guard for interval; configured argument 28.
4. Attack-move toward waypoint: waypoint 23 (cell 66, 88).
5. Guard for interval; configured argument 6.
6. Attack-move toward waypoint: waypoint 7 (cell 39, 88).
7. Guard for interval; configured argument 12.
8. Attack-move toward waypoint: waypoint 24 (cell 39, 72).
9. Guard for interval; configured argument 24.
10. Jump to script line; configured argument 2.

<a id="team-07a458c4"></a>

### Evil Patrol 3 - 07A458C4

Owner: BadGuy1. Roster: 2 × Technician (CTECH); 2 × Attack Dog (DOG); 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AC.

Ordered plan: Evil Patrol 3 SCR (0972F534).

1. Scatter.
2. Attack-move toward waypoint: waypoint 25 (cell 66, 27).
3. Guard for interval; configured argument 27.
4. Attack-move toward waypoint: waypoint 26 (cell 78, 26).
5. Guard for interval; configured argument 15.
6. Attack-move toward waypoint: waypoint 27 (cell 77, 47).
7. Guard for interval; configured argument 21.
8. Attack-move toward waypoint: waypoint 28 (cell 66, 47).
9. Guard for interval; configured argument 15.
10. Jump to script line; configured argument 2.

<a id="team-08da8f04"></a>

### Evil Armor 1 - 08DA8F04

Owner: BadGuy1. Roster: 3 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AD.

Ordered plan: Evil Armor 1 SCR (0972EDB4).

1. Scatter.
2. Attack-move toward waypoint: waypoint 27 (cell 77, 47).
3. Guard for interval; configured argument 6.
4. Attack-move toward waypoint: waypoint 30 (cell 77, 57).
5. Guard for interval; configured argument 20.
6. Attack-move toward waypoint: waypoint 32 (cell 86, 72).
7. Guard for interval; configured argument 9.
8. Attack-move toward waypoint: waypoint 22 (cell 66, 72).
9. Guard for interval; configured argument 15.
10. Attack-move toward waypoint: waypoint 24 (cell 39, 72).
11. Guard for interval; configured argument 12.
12. Attack-move toward waypoint: waypoint 33 (cell 39, 57).
13. Guard for interval; configured argument 17.
14. Attack-move toward waypoint: waypoint 29 (cell 48, 47).
15. Guard for interval; configured argument 10.
16. Jump to script line; configured argument 2.

<a id="team-0a632efc"></a>

### Evil Armor 2 - 0A632EFC

Owner: BadGuy2. Roster: 2 × IFV (FV); 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: N.

Ordered plan: Evil Armor 2 SCR (0A63244C).

1. Scatter.
2. Unload with continuation mode: transport and passengers continue.
3. Load transport.
4. Attack-move toward waypoint: waypoint 14 (cell 96, 113).
5. Guard for interval; configured argument 25.
6. Attack-move toward waypoint: waypoint 11 (cell 48, 113).
7. Guard for interval; configured argument 25.
8. Attack-move toward waypoint: waypoint 34 (cell 66, 113).
9. Guard for interval; configured argument 25.
10. Attack-move toward waypoint: waypoint 23 (cell 66, 88).
11. Attack-move toward waypoint: waypoint 22 (cell 66, 72).
12. Attack-move toward waypoint: waypoint 28 (cell 66, 47).
13. Guard for interval; configured argument 25.
14. Attack-move toward waypoint: waypoint 12 (cell 114, 47).
15. Guard for interval; configured argument 25.
16. Attack-move toward waypoint: waypoint 13 (cell 114, 113).
17. Guard for interval; configured argument 25.
18. Jump to script line; configured argument 4.

<a id="team-0c1b17b4"></a>

### Terror On Patrol - 0C1B17B4

Owner: BadGuy1. Roster: 3 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: E.

Ordered plan: Terror On Patrol SCR (0C1B1534).

1. Scatter.
2. Attack-move toward waypoint: waypoint 14 (cell 96, 113).
3. Guard for interval; configured argument 25.
4. Attack-move toward waypoint: waypoint 34 (cell 66, 113).
5. Guard for interval; configured argument 25.
6. Attack-move toward waypoint: waypoint 23 (cell 66, 88).
7. Guard for interval; configured argument 25.
8. Attack-move toward waypoint: waypoint 36 (cell 22, 88).
9. Guard for interval; configured argument 25.
10. Attack-move toward waypoint: waypoint 35 (cell 22, 72).
11. Guard for interval; configured argument 25.
12. Attack-move toward waypoint: waypoint 32 (cell 86, 72).
13. Guard for interval; configured argument 25.
14. Attack-move toward waypoint: waypoint 16 (cell 95, 47).
15. Guard for interval; configured argument 25.
16. Attack-move toward waypoint: waypoint 4 (cell 114, 80).
17. Guard for interval; configured argument 25.
18. Jump to script line; configured argument 2.

<a id="team-0c48359c"></a>

### 1st Desolator Usage - 0C48359C

Owner: BadGuy1. Roster: 3 × Desolator (DESO)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 16; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: 1st Desolator Usage SCR (0DA7432C).

1. Guard for interval; configured argument 45.
2. Move to waypoint: waypoint 20 (cell 71, 80).
3. Set local flag: local flag 9 (Desolator Gooing).
4. Deploy.
5. Flash team; configured argument 90.
6. Guard for interval; configured argument 15.
7. Deploy.
8. Approach selected enemy-building category; configured argument 131074.
9. Deploy.

<a id="team-0be84804"></a>

### Def_Spy - 0BE84804

Owner: BadGuy1. Roster: 3 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0be86a74"></a>

### Def_Engineer - 0BE86A74

Owner: BadGuy1. Roster: 1 × Attack Dog (DOG); 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0be86524"></a>

### Def_Rocketeer - 0BE86524

Owner: BadGuy1. Roster: 3 × Flak Trooper (FLAKT); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bdef684"></a>

### Def_GI - 0BDEF684

Owner: BadGuy1. Roster: 3 × Conscript (E2); 1 × Attack Dog (DOG); 1 × Desolator (DESO)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bdee994"></a>

### Def_Grizzly - 0BDEE994

Owner: BadGuy1. Roster: 2 × Terror Drone (DRON); 1 × Rhino Heavy Tank (HTNK); 2 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bdeda74"></a>

### Def_IFV - 0BDEDA74

Owner: BadGuy1. Roster: 1 × Rhino Heavy Tank (HTNK); 1 × V3 Launcher (V3); 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bded6d4"></a>

### Def_Intruder - 0BDED6D4

Owner: BadGuy1. Roster: 2 × Flak Track (HTK); 2 × Flak Trooper (FLAKT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bde7234"></a>

### Def_Blackhawk - 0BDE7234

Owner: BadGuy1. Roster: 1 × Flak Track (HTK); 1 × Flak Trooper (FLAKT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bdef8e4"></a>

### Def_Hard1 - 0BDEF8E4

Owner: BadGuy1. Roster: 3 × Terror Drone (DRON); 3 × Tesla Trooper (SHK); 2 × Desolator (DESO)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0bde6614"></a>

### Def_Hard2 - 0BDE6614

Owner: BadGuy1. Roster: 2 × V3 Launcher (V3); 2 × Rhino Heavy Tank (HTNK); 1 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: yes; Avoid Threats: no; Priority: 9; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Def_Base SCR (0BDE2924).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-092fccbc"></a>

### Attk_Rhino1 - 092FCCBC

Owner: BadGuy1. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Rhino1 SCR (092FCA4C).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131127.
4. Seek/attack target category; configured argument 7.
5. Attack selected enemy-building category; configured argument 131079.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-092fc80c"></a>

### Attk_Rhino2 - 092FC80C

Owner: BadGuy1. Roster: 2 × Rhino Heavy Tank (HTNK); 1 × Flak Track (HTK); 3 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Rhino2 SCR (092FC59C).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131072.
4. Seek/attack target category; configured argument 9.
5. Attack selected enemy-building category; configured argument 131075.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-09362f04"></a>

### Attk_V3 1 - 09362F04

Owner: BadGuy1. Roster: 2 × V3 Launcher (V3); 2 × Terror Drone (DRON); 2 × Flak Trooper (FLAKT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_V3 1 SCR (093634C4).

1. Attack selected enemy-building category; configured argument 131127.
2. Report team success.
3. Seek/attack target category; configured argument 7.
4. Seek/attack target category; configured argument 9.
5. Attack selected enemy-building category; configured argument 131079.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-09365d64"></a>

### Attk_V3 2 - 09365D64

Owner: BadGuy1. Roster: 2 × V3 Launcher (V3); 2 × Flak Trooper (FLAKT); 2 × Conscript (E2); 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_V3 2 SCR (093657E4).

1. Attack selected enemy-building category; configured argument 131072.
2. Report team success.
3. Seek/attack target category; configured argument 9.
4. Attack selected enemy-building category; configured argument 131177.
5. Attack selected enemy-building category; configured argument 131074.
6. Seek/attack target category; configured argument 2.
7. Seek/attack target category; configured argument 1.

<a id="team-09343ae4"></a>

### Attk_FlakTrack - 09343AE4

Owner: BadGuy1. Roster: 2 × Flak Track (HTK); 3 × Flak Trooper (FLAKT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_FlakTrack SCR (09345DB4).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131177.
4. Attack selected enemy-building category; configured argument 131074.
5. Seek/attack target category; configured argument 1.

<a id="team-09345924"></a>

### Attk_Terror 1 - 09345924

Owner: BadGuy1. Roster: 2 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Terror 1 SCR (09345584).

1. Seek/attack target category; configured argument 3.
2. Report team success.
3. Seek/attack target category; configured argument 5.
4. Adopt object mission: hunt.

<a id="team-093450e4"></a>

### Attk_Terror 2 - 093450E4

Owner: BadGuy1. Roster: 2 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Terror 2 SCR (09346C94).

1. Seek/attack target category; configured argument 5.
2. Report team success.
3. Seek/attack target category; configured argument 4.
4. Adopt object mission: hunt.

<a id="team-08114dec"></a>

### Attk Infantry 1 - 08114DEC

Owner: BadGuy1. Roster: 6 × Conscript (E2); 2 × Flak Trooper (FLAKT); 2 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk Infantry 1 SCR (08114B7C).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131072.
4. Seek/attack target category; configured argument 9.
5. Attack selected enemy-building category; configured argument 131075.
6. Seek/attack target category; configured argument 1.

<a id="team-0811493c"></a>

### Attk Infantry 2 - 0811493C

Owner: BadGuy1. Roster: 2 × Attack Dog (DOG); 2 × Desolator (DESO); 4 × Conscript (E2); 2 × Flak Trooper (FLAKT)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk Infantry 2 SCR (081146CC).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Adopt object mission: hunt.

<a id="team-0811448c"></a>

### Attk Infantry 3 - 0811448C

Owner: BadGuy1. Roster: 5 × Flak Trooper (FLAKT); 5 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk Infantry 3 SCR (0811421C).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131075.
3. Report team success.
4. Seek/attack target category; configured argument 4.
5. Seek/attack target category; configured argument 1.

<a id="team-08113dec"></a>

### Attk Infantry 4 - 08113DEC

Owner: BadGuy1. Roster: 8 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk Infantry 4 SCR (08113B7C).

1. Seek/attack target category; configured argument 10.
2. Report team success.
3. Seek/attack target category; configured argument 1.

<a id="team-09301b7c"></a>

### Attk_Hard1 - 09301B7C

Owner: BadGuy1. Roster: 3 × V3 Launcher (V3); 2 × Rhino Heavy Tank (HTNK); 2 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 14; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Hard1 SCR (0930190C).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131079.
3. Report team success.
4. Attack selected enemy-building category; configured argument 131074.
5. Seek/attack target category; configured argument 2.

<a id="team-093016cc"></a>

### Attk_Hard2 - 093016CC

Owner: BadGuy1. Roster: 4 × Desolator (DESO); 3 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 14; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Hard2 SCR (0C1B7064).

1. Seek/attack target category; configured argument 4.
2. Report team success.
3. Seek/attack target category; configured argument 5.
4. Adopt object mission: hunt.

<a id="team-0930121c"></a>

### Attk_Hard3 - 0930121C

Owner: BadGuy1. Roster: 5 × Rhino Heavy Tank (HTNK); 1 × Flak Track (HTK); 2 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 14; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Hard3 SCR (09300DBC).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131177.
3. Report team success.
4. Attack selected enemy-building category; configured argument 131079.
5. Attack selected enemy-building category; configured argument 131073.
6. Seek/attack target category; configured argument 6.
7. Seek/attack target category; configured argument 1.

<a id="team-09300b7c"></a>

### Attk_Engineer1 - 09300B7C

Owner: BadGuy1. Roster: 2 × Engineer (SENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Engineer1 SCR (0930090C).

1. Attack selected enemy-building category; configured argument 131177.
2. Report team success.
3. Attack selected enemy-building category; configured argument 131075.
4. Attack selected enemy-building category; configured argument 131074.
5. Seek/attack target category; configured argument 6.
6. Seek/attack target category; configured argument 2.

<a id="team-093006cc"></a>

### Attk_Engineer2 - 093006CC

Owner: BadGuy1. Roster: 3 × Conscript (E2); 2 × Engineer (SENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Engineer2 SCR (0930045C).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131072.
3. Report team success.
4. Attack selected enemy-building category; configured argument 131072.
5. Seek/attack target category; configured argument 9.
6. Seek/attack target category; configured argument 2.

<a id="team-0930021c"></a>

### Attk_Engineer3 - 0930021C

Owner: BadGuy1. Roster: 2 × Terror Drone (DRON); 2 × Engineer (SENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Engineer3 SCR (09302DBC).

1. Gather near enemy base; configured argument 0.
2. Attack selected enemy-building category; configured argument 131073.
3. Report team success.
4. Attack selected enemy-building category; configured argument 131073.
5. Attack selected enemy-building category; configured argument 131074.
6. Seek/attack target category; configured argument 9.
7. Seek/attack target category; configured argument 2.

<a id="team-07e4d754"></a>

### Attk_Patrol1 - 07E4D754

Owner: BadGuy2. Roster: 3 × Conscript (E2); 2 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Patrol1 SCR (0ABD60E4).

1. Attack-move toward waypoint: waypoint 22 (cell 66, 72).
2. Guard for interval; configured argument 17.
3. Attack-move toward waypoint: waypoint 28 (cell 66, 47).
4. Guard for interval; configured argument 10.
5. Attack-move toward waypoint: waypoint 16 (cell 95, 47).
6. Guard for interval; configured argument 15.
7. Attack-move toward waypoint: waypoint 31 (cell 86, 57).
8. Guard for interval; configured argument 8.
9. Attack-move toward waypoint: waypoint 32 (cell 86, 72).
10. Guard for interval; configured argument 24.
11. Attack-move toward waypoint: waypoint 14 (cell 96, 113).
12. Guard for interval; configured argument 3.
13. Attack-move toward waypoint: waypoint 10 (cell 56, 113).
14. Guard for interval; configured argument 18.
15. Attack-move toward waypoint: waypoint 8 (cell 56, 88).
16. Guard for interval; configured argument 10.
17. Jump to script line; configured argument 1.

<a id="team-0a287514"></a>

### 2x Check on BG2 - 0A287514

Owner: BadGuy1. Roster: 6 × Conscript (E2); 2 × Attack Dog (DOG); 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: 2x Check on BG2 SCR (0A289554).

1. Attack-move toward waypoint: waypoint 8 (cell 56, 88).
2. Guard for interval; configured argument 12.
3. Attack-move toward waypoint: waypoint 7 (cell 39, 88).
4. Guard for interval; configured argument 12.
5. Attack-move toward waypoint: waypoint 24 (cell 39, 72).
6. Guard for interval; configured argument 12.
7. Attack-move toward waypoint: waypoint 22 (cell 66, 72).
8. Guard for interval; configured argument 12.
9. Attack-move toward waypoint: waypoint 23 (cell 66, 88).
10. Guard for interval; configured argument 12.
11. Jump to script line; configured argument 1.

<a id="team-0930221c"></a>

### Attk_Desolators - 0930221C

Owner: BadGuy1. Roster: 3 × Desolator (DESO)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 14; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attk_Desolators SCR (09306DBC).

1. Gather near enemy base; configured argument 0.
2. Approach selected enemy-building category; configured argument 131075.
3. Report team success.
4. Deploy.

<a id="team-09d7f8d4"></a>

### Harrassment Team - 09D7F8D4

Owner: BadGuy1. Roster: 1 × Attack Dog (DOG); 4 × Conscript (E2); 1 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 12; Max: 2; Veteran Level: 1; Technology level: 0; Waypoint: Y.

Ordered plan: Harrassment Team SCR (093489D4).

1. Adopt object mission: hunt.
2. Report team success.
3. Seek/attack target category; configured argument 4.

<a id="team-0be8b86c"></a>

### Techs Goto Arch - 0BE8B86C

Owner: Player. Roster: 1 × Technician (CTECH)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Techs Goto Arch SCR (0BE8DDBC).

1. Move to waypoint: waypoint 17 (cell 111, 80).
2. Adopt object mission: guard.

<a id="team-0a2bd7dc"></a>

### Prism Flashers! - 0A2BD7DC

Owner: Player. Roster: 2 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: E.

Ordered plan: Prism Flashers! SCR (0A2BD56C).

1. Flash team; configured argument 180.
2. Report team success.

<a id="team-08352e1c"></a>

### Tanya Converted - 08352E1C

Owner: TanyaLand. Roster: 1 × Tanya (TANY)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 20; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Tanya Converted SCR (083508EC).

1. Center view on team; configured argument 4.
2. Flash team; configured argument 15.
3. Play voice notification; configured argument 154.
4. Change country ownership; configured argument 16.

<a id="team-0ce2448c"></a>

### Player Reinforcements 5E_1 - 0CE2448C

Owner: Reinforcers. Roster: 1 × Amphibious Transport (LCRF); 2 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Player Reinforcements 5E_1 SCR (0CE2421C).

1. Move to waypoint: waypoint 5 (cell 148, 81).
2. Move to waypoint: waypoint 18 (cell 115, 84).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Set local flag: local flag 17 (5e1 Unloaded).
5. Move to waypoint: waypoint 45 (cell 115, 88).
6. Change country ownership; configured argument 13.
7. Adopt object mission: guard.

<a id="team-0ce23dec"></a>

### Player Reinforcements 5E_2 - 0CE23DEC

Owner: Reinforcers. Roster: 1 × Amphibious Transport (LCRF); 2 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: D.

Ordered plan: Player Reinforcements 5E_2 SCR (0CE23B7C).

1. Move to waypoint: waypoint 5 (cell 148, 81).
2. Move to waypoint: waypoint 19 (cell 115, 76).
3. Unload with continuation mode: transport continues; passengers leave team.
4. Set local flag: local flag 18 (5e2 Unloaded).
5. Move to waypoint: waypoint 46 (cell 115, 72).
6. Change country ownership; configured argument 13.
7. Adopt object mission: guard.

<a id="team-0a300cbc"></a>

### POW Patrol 1 - 0A300CBC

Owner: BadGuy1. Roster: 2 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: AP.

Ordered plan: POW Patrol 1 SCR (0A30EDBC).

1. Attack-move toward waypoint: waypoint 42 (cell 67, 86).
2. Guard for interval; configured argument 10.
3. Attack-move toward waypoint: waypoint 44 (cell 67, 73).
4. Guard for interval; configured argument 10.
5. Attack-move toward waypoint: waypoint 43 (cell 79, 73).
6. Guard for interval; configured argument 10.
7. Attack-move toward waypoint: waypoint 41 (cell 79, 87).
8. Guard for interval; configured argument 10.
9. Jump to script line; configured argument 1.

<a id="team-0af7132c"></a>

### POW Patrol 2 - 0AF7132C

Owner: BadGuy1. Roster: 2 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 2; Technology level: 0; Waypoint: AS.

Ordered plan: POW Patrol 2 SCR (0AF73DBC).

1. Attack-move toward waypoint: waypoint 43 (cell 79, 73).
2. Guard for interval; configured argument 10.
3. Attack-move toward waypoint: waypoint 41 (cell 79, 87).
4. Guard for interval; configured argument 10.
5. Attack-move toward waypoint: waypoint 42 (cell 67, 86).
6. Guard for interval; configured argument 10.
7. Attack-move toward waypoint: waypoint 44 (cell 67, 73).
8. Guard for interval; configured argument 10.
9. Jump to script line; configured argument 1.

<a id="team-0d1a928c"></a>

### POW Panic - 0D1A928C

Owner: Civilian1. Roster: 5 × Civilian (CIV1); 7 × Civilian (CIV2); 7 × Civilian (CIV3)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 12; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: U.

Ordered plan: POW Panic SCR (0D1AABFC).

1. Panic.
2. Scatter.
3. Jump to script line; configured argument 1.

<a id="team-0cf25a4c"></a>

### Evil Armor 2 Redemption - 0CF25A4C

Owner: BadGuy2. Roster: 2 × IFV (FV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: yes; Priority: 40; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: N.

Ordered plan: Evil Armor 2 Redemption SCR (0CF257DC).

1. Move to waypoint: waypoint 32 (cell 86, 72).
2. Unload with continuation mode: transport and passengers continue.
3. Set local flag: local flag 13 (Evil Armor Redempti).
4. Change country ownership; configured argument 13.

<a id="team-0a5c531c"></a>

### Evil Armor Redemption MkII - 0A5C531C

Owner: BadGuy2. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 40; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AG.

Ordered plan: Evil Armor Redemption MkII SCR (0A5C469C).

1. Set local flag: local flag 14 (Goto AW).
2. Change country ownership; configured argument 13.

<a id="team-0a5c321c"></a>

### Get thee to the Arch - 0A5C321C

Owner: Player. Roster: 2 × IFV (FV); 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 41; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AG.

Ordered plan: Get thee to the Arch SCR (0A5C5CAC).

1. Move to waypoint: waypoint 48 (cell 107, 81).
2. Report team success.

<a id="team-0cdaaefc"></a>

### Player Reinforcers 1a - 0CDAAEFC

Owner: Reinforcers. Roster: 1 × Grizzly Battle Tank (MTNK); 1 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforcers Change House SCR (0D14204C).

1. Change country ownership; configured argument 13.

<a id="team-0cdaab5c"></a>

### Player Reinforcers 2a - 0CDAAB5C

Owner: Reinforcers. Roster: 1 × Grizzly Battle Tank (MTNK); 1 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: T.

Ordered plan: Reinforcers Change House SCR (0D14204C).

1. Change country ownership; configured argument 13.

<a id="team-0cdaa91c"></a>

### Player Reinforcers 3a - 0CDAA91C

Owner: Reinforcers. Roster: 2 × Grizzly Battle Tank (MTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: R.

Ordered plan: Reinforcers Change House SCR (0D14204C).

1. Change country ownership; configured argument 13.

<a id="team-0cdaa6dc"></a>

### Player Reinforcers 4a - 0CDAA6DC

Owner: Reinforcers. Roster: 1 × Allied Construction Vehicle (AMCV); 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: E.

Ordered plan: Reinforcers Change House SCR (0D14204C).

1. Change country ownership; configured argument 13.

<a id="team-0cdaa49c"></a>

### Player Reinforcers 5e1a - 0CDAA49C

Owner: Reinforcers. Roster: 2 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: S.

Ordered plan: Reinforcers Change House SCR (0D14204C).

1. Change country ownership; configured argument 13.

<a id="team-0cdaa25c"></a>

### Player Reinforcers 5e2a - 0CDAA25C

Owner: Reinforcers. Roster: 2 × Prism Tank (SREF)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: yes; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: T.

Ordered plan: Reinforcers Change House SCR (0D14204C).

1. Change country ownership; configured argument 13.
