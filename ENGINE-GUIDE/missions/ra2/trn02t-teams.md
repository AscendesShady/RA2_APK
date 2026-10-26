# Boot Camp - Day 2 - team rosters and plans

[Trigger ledger](trn02t.md) | [Mission overrides](trn02t-overrides.md) | [Campaign guide](../../05-CAMPAIGNS.md)

These are declared possibilities. A create/reinforcement action, AI selection, recruitment path or another mechanism must make a live team before its plan runs. Script arguments for encoded building selection remain identified numeric settings; an unproved index-to-target interpretation is not invented. Source: MAPS01.MIX/trn02t.map; each team/script ID identifies its section.

<a id="team-09ab3c8c"></a>

### RedAttackTeamA - 09AB3C8C

Owner: RedTeam. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 10; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: AttackBlueInfantry (09E7CB7C).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 10.
4. Seek/attack target category; configured argument 4.
5. Set local flag: local flag 0 (1stRedTeamWon).

<a id="team-07fb10f4"></a>

### RedTeamRegroup - 07FB10F4

Owner: RedTeam. Roster: 5 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: ReturnToBase (0A562854).

1. Move to waypoint: waypoint 0 (cell 47, 60).
2. Adopt object mission: area guard.

<a id="team-07fb0284"></a>

### BaseDef1 - 07FB0284

Owner: RedTeam. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BA.

Ordered plan: GuardBase (07FB21D4).

1. Adopt object mission: area guard.

<a id="team-08f9b580"></a>

### BaseDef2 - 08F9B580

Owner: RedTeam. Roster: 1 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BB.

Ordered plan: GuardBase (07FB21D4).

1. Adopt object mission: area guard.

<a id="team-08f9b360"></a>

### BaseDef3 - 08F9B360

Owner: RedTeam. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: yes; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BC.

Ordered plan: GuardBase (07FB21D4).

1. Adopt object mission: area guard.

<a id="team-0973c33c"></a>

### RedAttackTeamB - 0973C33C

Owner: RedTeam. Roster: 8 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 40; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: A.

Ordered plan: AttackBlueBase (0973BDBC).

1. Gather near own base; configured argument 0.
2. Seek/attack target category; configured argument 4.
3. Seek/attack target category; configured argument 9.
4. Attack selected enemy-building category; configured argument 1.
5. Attack selected enemy-building category; configured argument 2.
6. Attack selected enemy-building category; configured argument 3.
7. Seek/attack target category; configured argument 2.
8. Seek/attack target category; configured argument 1.

<a id="team-0beb05fc"></a>

### Player_MCV - 0BEB05FC

Owner: Player. Roster: 1 × Allied Construction Vehicle (AMCV)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 30; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: CM.

Ordered plan: DriveOn (0BEB038C).

1. Move to waypoint: waypoint 18 (cell 23, 38).
2. Guard for interval; configured argument 200.

<a id="team-088ce6ec"></a>

### BarnHaters - 088CE6EC

Owner: RedTeam. Roster: 2 × GI (E1)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: no; Aggressive: yes; Base-defense role: no; Avoid Threats: no; Priority: 50; Max: 1; Veteran Level: 1; Technology level: 0; Waypoint: BH.

Ordered plan: BarnMustDie (09FF245C).

1. Move to waypoint: waypoint 13 (cell 57, 51).
2. Attack selected enemy-building category; configured argument 131158.
3. Adopt object mission: area guard.

<a id="team-0868eefc"></a>

### EngineerBridge - 0868EEFC

Owner: RedTeam. Roster: 1 × Engineer (ENGINEER)

Explicit team settings: Autocreate: no; Prebuild: no; Reinforce: no; Recruiter: no; Full: no; Loadable: no; Suicide: yes; Aggressive: no; Base-defense role: no; Avoid Threats: no; Priority: 7; Max: 1; Veteran Level: 1; Technology level: 0.

Ordered plan: RepairBridge (0868BC9C).

1. Attack selected enemy-building category; configured argument 131102.
