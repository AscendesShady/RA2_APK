# Operation: Red Revolution - mission overrides and local definitions

[Trigger ledger](sov11s.md) | [Team plans](sov11s-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov11s.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Soviet Construction Vehicle (SMCV) | Technology level | 9 | 2 |
| Psychic Sensor (NAPSIS) | Technology level | 9 | 5 |
| Kirov Airship (ZEP) | Technology level | 9 | 8 |
| War Miner (HARV) | Resource cargo capacity | 20 | 11 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 14 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 17 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 18 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 19 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 20 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 23 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 26 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 29 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 32 |
| NUKEPAYLOAD (NUKEPAYLOAD) | Damage | 600 | 35 |
| Kremlin (CARUS03) | Starting health capacity | 800 | 38 |
| Kremlin (CARUS03) | Infantry garrison permitted | no | 39 |
| Kremlin (CARUS03) | Garrison capacity | 0 | 40 |
| Nuclear Missile Silo (NAMISL) | Technology level | 9 | 43 |
| Iron Curtain (IRONCURTAINSPECIAL) | Recharge Time | 10 | 46 |
| Engineer (ENGINEER) | Technology level | -1 | 49 |
| Attack Dog (ADOG) | Technology level | -1 | 52 |
| BARRELEXPLOSION (BARRELEXPLOSION) | Damage | 200 | 55 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Cell Spread | 2 | 58 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Percent At Max | .25 | 59 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Wall Absolute Destroyer | Yes | 60 |
| Yuri (YURI) | UI Name | Name:PTROOP | 63 |
| Yuri (YURI) | Name | Yuri | 64 |
| Yuri (YURI) | Technology level | 10 | 65 |
| Cloning Vats (NACLON) | UI Name | Name:NACLON | 77 |
| Cloning Vats (NACLON) | Name | Cloning Vats | 78 |
| Cloning Vats (NACLON) | Technology level | -1 | 79 |
| Soviet Shipyard (NAYARD) | UI Name | Name:NAYARD | 82 |
| Soviet Shipyard (NAYARD) | Name | Soviet Shipyard | 83 |
| Soviet Shipyard (NAYARD) | Technology level | -1 | 84 |
| Iron Curtain Device (NAIRON) | UI Name | Name:NAIRON | 87 |
| Iron Curtain Device (NAIRON) | Name | Iron Curtain Device | 88 |
| Iron Curtain Device (NAIRON) | Technology level | -1 | 89 |
| AI (AI) | Attack Interval | 0.40 | 92 |
| AI (AI) | Attack Delay | 0.40 | 93 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 1000,750,500 | 96 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 2500 | 97 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -2000 | 98 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Total AI Team Cap | 60,45,30 | 99 |
| Invisible Yellow Light Post (INYELWLAMP) | Name | Invisible Yellow Light Post | 102 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 4000 | 103 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 104 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.2 | 105 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.2 | 106 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.0 | 107 |
| Negative Light Post (NEGLAMP) | Name | Negative Light Post | 110 |
| Negative Light Post (NEGLAMP) | Image | GALITE | 111 |
| Negative Light Post (NEGLAMP) | Local light reach | 5000 | 112 |
| Negative Light Post (NEGLAMP) | Local light intensity | -0.15 | 113 |
| Negative Light Post (NEGLAMP) | Light Red Tint | 0.03 | 114 |
| Negative Light Post (NEGLAMP) | Light Green Tint | 0.04 | 115 |
| Negative Light Post (NEGLAMP) | Light Blue Tint | 0.04 | 116 |
| Invisible Purple Light Post (INPURPLAMP) | Name | Invisible Purple Light Post | 119 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 4000 | 120 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.01 | 121 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 0.67059 | 122 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.19608 | 123 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 0.67059 | 124 |
| SPECIALFLAGS | Tiberium Grows | no | 127 |
| SPECIALFLAGS | Tiberium Spreads | yes | 128 |
| SPECIALFLAGS | Tiberium Explosive | no | 129 |
| SPECIALFLAGS | Destroyable Bridges | yes | 130 |
| SPECIALFLAGS | MCV Deploy | no | 131 |
| SPECIALFLAGS | Initial Veteran | no | 132 |
| SPECIALFLAGS | Fixed Alliance | no | 133 |
| SPECIALFLAGS | Harvester Immune | no | 134 |
| SPECIALFLAGS | Fog Of War | no | 135 |
| SPECIALFLAGS | Inert | no | 136 |
| SPECIALFLAGS | Ion Storms | no | 137 |
| SPECIALFLAGS | Meteorites | no | 138 |
| SPECIALFLAGS | Visceroids | no | 139 |
| COUNTRIES (COUNTRIES) | 0 | Player | 142 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 143 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 144 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 145 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 146 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 147 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 148 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 149 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Play IC Movie,0 | 267 |
