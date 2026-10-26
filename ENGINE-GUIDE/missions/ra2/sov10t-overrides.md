# Operation: Weathered Alliance - mission overrides and local definitions

[Trigger ledger](sov10t.md) | [Team plans](sov10t-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov10t.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 5000 | 2 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -5000 | 3 |
| War Miner (HARV) | Resource cargo capacity | 20 | 15 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 18 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 21 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 22 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 23 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 24 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 27 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 30 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 33 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 36 |
| Yuri (YURI) | Technology level | -1 | 39 |
| Iron Curtain Device (NAIRON) | Technology level | -1 | 42 |
| Psychic Sensor (NAPSIS) | Technology level | -1 | 45 |
| Cloning Vats (NACLON) | Technology level | -1 | 48 |
| Kirov Airship (ZEP) | Technology level | -1 | 51 |
| Engineer (ENGINEER) | Name | Engineer | 54 |
| Engineer (ENGINEER) | Technology level | -1 | 55 |
| Attack Dog (ADOG) | Name | Allied Attack Dog | 58 |
| Attack Dog (ADOG) | Technology level | -1 | 59 |
| SEAL (GHOST) | Name | SEAL | 62 |
| SEAL (GHOST) | Technology level | 9 | 63 |
| Tanya (TANY) | Name | Tanya | 66 |
| Tanya (TANY) | Technology level | -1 | 67 |
| Spy (SPY) | Name | Spy | 70 |
| Spy (SPY) | Technology level | -1 | 71 |
| Giant Squid (SQD) | UI Name | Name:SQD | 74 |
| Giant Squid (SQD) | Name | Giant Squid | 75 |
| Giant Squid (SQD) | No Shadow | yes | 76 |
| Giant Squid (SQD) | Category | AFV | 77 |
| Giant Squid (SQD) | Required structures/groups | NAYARD,NATECH | 78 |
| Giant Squid (SQD) | Primary | SquidGrab | 79 |
| Giant Squid (SQD) | Secondary | SquidPunch | 80 |
| Giant Squid (SQD) | Naval-target selection mode | 3 | 81 |
| Giant Squid (SQD) | Ground-target selection mode | 1 | 82 |
| Giant Squid (SQD) | Walk Rate | 2 | 83 |
| Giant Squid (SQD) | Idle Rate | 4 | 84 |
| Giant Squid (SQD) | Starting health capacity | 200 | 85 |
| Giant Squid (SQD) | Suppression Threshold | 250 | 86 |
| Giant Squid (SQD) | Organic | yes | 87 |
| Giant Squid (SQD) | Armor class | light | 88 |
| Giant Squid (SQD) | Technology level | 8 | 89 |
| Giant Squid (SQD) | Underwater | yes | 90 |
| Giant Squid (SQD) | Naval role | yes | 91 |
| Giant Squid (SQD) | Turret | no | 92 |
| Giant Squid (SQD) | Is Tilter | no | 93 |
| Giant Squid (SQD) | Self-healing | yes | 94 |
| Giant Squid (SQD) | Crate Goodie | no | 95 |
| Giant Squid (SQD) | Sight radius setting | 5 | 96 |
| Giant Squid (SQD) | Detector service | yes | 97 |
| Giant Squid (SQD) | Detection range setting | 4 | 98 |
| Giant Squid (SQD) | Guard Range | 5 | 99 |
| Giant Squid (SQD) | Movement rating | 8 | 100 |
| Giant Squid (SQD) | Permitted country list | Russians,Confederation,Africans,Arabs | 101 |
| Giant Squid (SQD) | Price in credits | 1000 | 102 |
| Giant Squid (SQD) | Points | 20 | 103 |
| Giant Squid (SQD) | ROT | 40 | 104 |
| Giant Squid (SQD) | Allowed To Start In Multiplayer | no | 105 |
| Giant Squid (SQD) | Can crush through ordinary crushing logic | no | 106 |
| Giant Squid (SQD) | Crewed | no | 107 |
| Giant Squid (SQD) | Is Selectable Combatant | yes | 108 |
| Giant Squid (SQD) | Voice Select | SquidSelect | 109 |
| Giant Squid (SQD) | Voice Move | SquidMove | 110 |
| Giant Squid (SQD) | Voice Attack | SquidAttackCommand | 111 |
| Giant Squid (SQD) | Voice Feedback | SquidFear | 112 |
| Giant Squid (SQD) | Die Sound | SquidDie | 113 |
| Giant Squid (SQD) | Locomotor | {2BEA74E1-7CCA-11d3-BE14-00104B62A16C} | 114 |
| Giant Squid (SQD) | Movement speed category | Float | 115 |
| Giant Squid (SQD) | Permitted movement zone | Water | 116 |
| Giant Squid (SQD) | Threat contribution | 25 | 117 |
| Giant Squid (SQD) | Weight | .5 | 118 |
| Giant Squid (SQD) | Immune to ordinary psychic control | yes | 119 |
| Giant Squid (SQD) | Parasiteable | no | 120 |
| Giant Squid (SQD) | Can gain rank | yes | 121 |
| Giant Squid (SQD) | Explosive destruction flag | no | 122 |
| Giant Squid (SQD) | Acceleration Factor | 0.01 | 123 |
| Giant Squid (SQD) | Z Fudge Column | 8 | 124 |
| Giant Squid (SQD) | Z Fudge Tunnel | 13 | 125 |
| Giant Squid (SQD) | Attached bombs permitted | yes | 126 |
| Giant Squid (SQD) | Transport size usage | 30 | 127 |
| Giant Squid (SQD) | Can cloak | yes | 128 |
| Giant Squid (SQD) | Cloaking Speed | 5 | 129 |
| Giant Squid (SQD) | Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | 130 |
| Giant Squid (SQD) | Elite improvements | STRONGER,FIREPOWER,ROF | 131 |
| Giant Squid (SQD) | Movement Restricted To | Water | 132 |
| Giant Squid (SQD) | Elite Primary | SquidGrabE | 133 |
| Giant Squid (SQD) | Elite Secondary | SquidPunchE | 134 |
| Giant Squid (SQD) | Too Big To Fit Under Bridge | true | 135 |
| Soviet Construction Vehicle (SMCV) | Name | Soviet Construction Vehicle | 138 |
| Soviet Construction Vehicle (SMCV) | Technology level | 8 | 139 |
| Nuclear Missile Silo (NAMISL) | Name | Nuclear Missile Silo | 142 |
| Nuclear Missile Silo (NAMISL) | Technology level | 8 | 143 |
| Weather Controller (GAWEAT) | Name | Weather Controller | 146 |
| Weather Controller (GAWEAT) | Starting health capacity | 200 | 147 |
| Weather Controller (GAWEAT) | Armor class | wood | 148 |
| Allied Battle Lab (GATECH) | Name | Allied Battle Lab | 151 |
| Allied Battle Lab (GATECH) | Signed power contribution | 0 | 152 |
| SPECIALFLAGS | Tiberium Grows | yes | 155 |
| SPECIALFLAGS | Tiberium Spreads | yes | 156 |
| SPECIALFLAGS | Tiberium Explosive | no | 157 |
| SPECIALFLAGS | Destroyable Bridges | no | 158 |
| SPECIALFLAGS | MCV Deploy | no | 159 |
| SPECIALFLAGS | Initial Veteran | no | 160 |
| SPECIALFLAGS | Fixed Alliance | no | 161 |
| SPECIALFLAGS | Harvester Immune | no | 162 |
| SPECIALFLAGS | Fog Of War | no | 163 |
| SPECIALFLAGS | Inert | no | 164 |
| SPECIALFLAGS | Ion Storms | no | 165 |
| SPECIALFLAGS | Meteorites | no | 166 |
| SPECIALFLAGS | Visceroids | no | 167 |
| COUNTRIES (COUNTRIES) | 0 | Player | 170 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 171 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 172 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 173 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 174 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 175 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 176 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 177 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Gen1 Destroyed,0 | 295 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Gen2 Destroyed,0 | 296 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Gen3 Destroyed,0 | 297 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Generator Advice,0 | 298 |
| VARIABLENAMES (VARIABLENAMES) | 4 | WCD Power On,0 | 299 |
