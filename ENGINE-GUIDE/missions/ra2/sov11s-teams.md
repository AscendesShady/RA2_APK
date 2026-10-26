# Operation: Red Revolution - team rosters and plans

[Trigger ledger](sov11s.md) | [Mission overrides](sov11s-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS02.MIX/sov11s.map; each team/script ID identifies its section.

<a id="team-0ab8657c"></a>

### Reinforcements - 0AB8657C

Owner: Player. Roster: 2 × V3 Launcher (V3); 1 × Apocalypse (APOC); 4 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: F.

Ordered plan: Reinforce Base (07855DBC).

1. Move to waypoint: waypoint 6 (cell 113, 161).

<a id="team-08fd5b7c"></a>

### BG2 - Yuri1 - 08FD5B7C

Owner: BadGuy2. Roster: 2 × Yuri (YURI); 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 30; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri 1 (083F8DBC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 1.
4. Report team success.

<a id="team-08fd56cc"></a>

### BG1 - Tank1D - 08FD56CC

Owner: BadGuy1. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Area (0AC3756C).

1. Report team success.
2. Adopt object mission: area guard.

<a id="team-0a481b5c"></a>

### BG1 - Drones1D - 0A481B5C

Owner: BadGuy1. Roster: 4 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Area (0AC3756C).

1. Report team success.
2. Adopt object mission: area guard.

<a id="team-0927095c"></a>

### BG1 - Conscripts1D - 0927095C

Owner: BadGuy1. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Test3 (08AE27FC).

1. Adopt object mission: area guard.
2. Report team success.

<a id="team-0a48146c"></a>

### BG1 - Drones3 - 0A48146C

Owner: BadGuy1. Roster: 3 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: ARMOR - Attack Vehicles (08FDA56C).

1. Gather near enemy base; configured argument 0.
2. Request special-weapon support; configured argument 0.
3. Seek/attack target category; configured argument 5.
4. Report team success.
5. Seek/attack target category; configured argument 1.
6. Jump to script line; configured argument 4.

<a id="team-07a0b91c"></a>

### BG1 - Conscripts4 - 07A0B91C

Owner: BadGuy1. Roster: 4 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Occupy Structures (078CB7DC).

1. Move to waypoint: waypoint 0 (cell 129, 127).
2. Attack selected enemy-building category; configured argument 131158.
3. Attack selected enemy-building category; configured argument 131178.

<a id="team-08fd82dc"></a>

### BG1 - Conscripts8 - 08FD82DC

Owner: BadGuy1. Roster: 8 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Infantry (0ADB403C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 1.
5. Report team success.
6. Jump to script line; configured argument 4.

<a id="team-0a668a0c"></a>

### BG1 - Engineer Rush - 0A668A0C

Owner: BadGuy1. Roster: 1 × Flak Track (HTK); 4 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: yes; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: ARMOR - Engineer Rush (0A66BDBC).

1. Load transport.
2. Gather near enemy base; configured argument 0.
3. Request special-weapon support; configured argument 0.
4. Approach selected enemy-building category; configured argument 131097.
5. Unload with continuation mode: transport and passengers continue.
6. Scatter.
7. Seek/attack target category; configured argument 2.
8. Report team success.
9. Seek/attack target category; configured argument 1.
10. Jump to script line; configured argument 8.

<a id="team-0a66c8ac"></a>

### BG1 - FlakTrack3 - 0A66C8AC

Owner: BadGuy1. Roster: 3 × Flak Track (HTK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: ARMOR - Attack Infantry (0A66CBEC).

1. Gather near own base; configured argument 0.
2. Request special-weapon support; configured argument 0.
3. Seek/attack target category; configured argument 4.
4. Report team success.
5. Request special-weapon support; configured argument 0.
6. Seek/attack target category; configured argument 1.
7. Report team success.
8. Jump to script line; configured argument 5.

<a id="team-0a66bb7c"></a>

### BG1 - V32 - 0A66BB7C

Owner: BadGuy1. Roster: 2 × V3 Launcher (V3); 1 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: ARMOR - Attack Buildings (0A66B90C).

1. Gather near own base; configured argument 0.
2. Request special-weapon support; configured argument 0.
3. Seek/attack target category; configured argument 2.
4. Report team success.
5. Request special-weapon support; configured argument 0.
6. Seek/attack target category; configured argument 1.
7. Report team success.
8. Jump to script line; configured argument 5.

<a id="team-0a66b6cc"></a>

### BG1 - MixedInfanty6 - 0A66B6CC

Owner: BadGuy1. Roster: 2 × Tesla Trooper (SHK); 4 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Infantry (0ADB403C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 1.
5. Report team success.
6. Jump to script line; configured argument 4.

<a id="team-0a66adec"></a>

### BG1 - MixedInfantry4 - 0A66ADEC

Owner: BadGuy1. Roster: 3 × Tesla Trooper (SHK); 1 × Yuri (YURI); 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: -1; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Vehicles (0ADB603C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 5.
3. Report team success.
4. Seek/attack target category; configured argument 1.
5. Report team success.
6. Jump to script line; configured argument 4.

<a id="team-0a66abac"></a>

### BG2 - Yuris4D - 0A66ABAC

Owner: BadGuy2. Roster: 4 × Yuri (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 30; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Area (0AC3756C).

1. Report team success.
2. Adopt object mission: area guard.

<a id="team-0791d75c"></a>

### BG2 - ShockTroopers5D - 0791D75C

Owner: BadGuy2. Roster: 5 × Tesla Trooper (SHK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: yes; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Area (0AC3756C).

1. Report team success.
2. Adopt object mission: area guard.

<a id="team-0a669efc"></a>

### BG2 - Yuris3 - 0A669EFC

Owner: BadGuy2. Roster: 3 × Yuri (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 30; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri 1 (083F8DBC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 1.
4. Report team success.

<a id="team-0a669cbc"></a>

### Conscripts6 - 0A669CBC

Owner: BadGuy1. Roster: 6 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Infantry (0ADB403C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 1.
5. Report team success.
6. Jump to script line; configured argument 4.

<a id="team-0796857c"></a>

### BG2 - Tanks3 - 0796857C

Owner: BadGuy2. Roster: 1 × Apocalypse (APOC); 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: ARMOR - Attack Buildings (0A66B90C).

1. Gather near own base; configured argument 0.
2. Request special-weapon support; configured argument 0.
3. Seek/attack target category; configured argument 2.
4. Report team success.
5. Request special-weapon support; configured argument 0.
6. Seek/attack target category; configured argument 1.
7. Report team success.
8. Jump to script line; configured argument 5.

<a id="team-0a66983c"></a>

### BG2 - Conscripts14 - 0A66983C

Owner: BadGuy2. Roster: 20 × Conscript (E2)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Attack Infantry (0ADB403C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Report team success.
4. Seek/attack target category; configured argument 1.
5. Report team success.
6. Jump to script line; configured argument 4.

<a id="team-0a486dec"></a>

### BG2 - Drones 3 - 0A486DEC

Owner: BadGuy2. Roster: 3 × Terror Drone (DRON)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Backdoor IC 1 (0A66D67C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 2 (cell 114, 89).
3. Move to waypoint: waypoint 3 (cell 115, 104).
4. Move to waypoint: waypoint 4 (cell 91, 118).
5. Request special-weapon support; configured argument 0.
6. Seek/attack target category; configured argument 1.
7. Report team success.
8. Jump to script line; configured argument 5.

<a id="team-0a66dc8c"></a>

### BG2 - Conscripts20 - 0A66DC8C

Owner: BadGuy2. Roster: 2 × Tesla Trooper (SHK); 4 × Attack Dog (DOG)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 2; Veteran Level: 1; Technology level: 0.

Ordered plan: Backdoor Attack 2 (0A66DA1C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 2 (cell 114, 89).
3. Move to waypoint: waypoint 3 (cell 115, 104).
4. Move to waypoint: waypoint 4 (cell 91, 118).
5. Seek/attack target category; configured argument 1.
6. Report team success.
7. Seek/attack target category; configured argument 1.

<a id="team-0a66d8ec"></a>

### BG2 - 3Tanks - 0A66D8EC

Owner: BadGuy2. Roster: 1 × V3 Launcher (V3); 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Backdoor IC 1 (0A66D67C).

1. Gather near own base; configured argument 0.
2. Move to waypoint: waypoint 2 (cell 114, 89).
3. Move to waypoint: waypoint 3 (cell 115, 104).
4. Move to waypoint: waypoint 4 (cell 91, 118).
5. Request special-weapon support; configured argument 0.
6. Seek/attack target category; configured argument 1.
7. Report team success.
8. Jump to script line; configured argument 5.

<a id="team-0ac0a57c"></a>

### BG3 - Yuri 1 - 0AC0A57C

Owner: BadGuy3. Roster: 1 × Yuri (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: yes; Priority: 8; Max: 20; Veteran Level: 1; Technology level: 0.

Ordered plan: Yuri 1 (083F8DBC).

1. Gather near own base; configured argument 0.
2. Gather near enemy base; configured argument 0.
3. Seek/attack target category; configured argument 1.
4. Report team success.

<a id="team-07a4966c"></a>

### BG3 - Kirovs 1 - 07A4966C

Owner: BadGuy3. Roster: 1 × Kirov Airship (ZEP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Kirov (07A4BDBC).

1. Attack selected enemy-building category; configured argument 131126.
2. Report team success.
3. Seek/attack target category; configured argument 2.
4. Report team success.
5. Seek/attack target category; configured argument 1.
6. Report team success.
7. Jump to script line; configured argument 3.

<a id="team-096acefc"></a>

### Player Kirov 1 - 096ACEFC

Owner: Player. Roster: 1 × Kirov Airship (ZEP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AT.

Ordered plan: Player Kirov 1 (096AC9FC).

1. Move to waypoint: waypoint 45 (cell 107, 152).

<a id="team-096a857c"></a>

### Player Kirov 2 - 096A857C

Owner: Player. Roster: 1 × Kirov Airship (ZEP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: AS.

Ordered plan: Player Kirov 2 (096A830C).

1. Move to waypoint: waypoint 44 (cell 115, 152).

<a id="team-096a167c"></a>

### Player MCV - 096A167C

Owner: Player. Roster: 1 × Soviet Construction Vehicle (SMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: Player MCV (096A9DBC).

1. Move to waypoint: waypoint 46 (cell 111, 153).
2. Deploy.

<a id="team-0ad1d90c"></a>

### Iron Curtain 1e - 0AD1D90C

Owner: BadGuy2. Roster: 3 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Iron Curtain Buildings (0A5797DC).

1. Report team success.
2. Gather near own base; configured argument 0.
3. Request special-weapon support; configured argument 0.
4. Seek/attack target category; configured argument 2.
5. Report team success.
6. Seek/attack target category; configured argument 1.
7. Report team success.
8. Jump to script line; configured argument 3.

<a id="team-0ca97efc"></a>

### Iron Curtain 1m - 0CA97EFC

Owner: BadGuy2. Roster: 1 × Apocalypse (APOC); 2 × Rhino Heavy Tank (HTNK)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Iron Curtain Buildings (0A5797DC).

1. Report team success.
2. Gather near own base; configured argument 0.
3. Request special-weapon support; configured argument 0.
4. Seek/attack target category; configured argument 2.
5. Report team success.
6. Seek/attack target category; configured argument 1.
7. Report team success.
8. Jump to script line; configured argument 3.

<a id="team-0ca97cbc"></a>

### Iron Curtain 1h - 0CA97CBC

Owner: BadGuy2. Roster: 3 × Apocalypse (APOC)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 3; Veteran Level: 1; Technology level: 0.

Ordered plan: Iron Curtain Buildings (0A5797DC).

1. Report team success.
2. Gather near own base; configured argument 0.
3. Request special-weapon support; configured argument 0.
4. Seek/attack target category; configured argument 2.
5. Report team success.
6. Seek/attack target category; configured argument 1.
7. Report team success.
8. Jump to script line; configured argument 3.

<a id="team-0ad6396c"></a>

### BG3 - Yuri 1d - 0AD6396C

Owner: BadGuy3. Roster: 10 × Yuri (YURI)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 30; Veteran Level: 1; Technology level: 0.

Ordered plan: Guard Area (0AC3756C).

1. Report team success.
2. Adopt object mission: area guard.

<a id="team-0a52e3dc"></a>

### BG3 - Kirovs2 (Left) - 0A52E3DC

Owner: BadGuy3. Roster: 1 × Kirov Airship (ZEP)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 4; Veteran Level: 1; Technology level: 0.

Ordered plan: Kirov (Left) (0B1076BC).

1. Move to waypoint: waypoint 20 (cell 72, 111).
2. Attack selected enemy-building category; configured argument 131126.
3. Report team success.
4. Seek/attack target category; configured argument 2.
5. Report team success.
6. Seek/attack target category; configured argument 1.
7. Report team success.
8. Jump to script line; configured argument 4.
