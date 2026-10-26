# Operation: Chrono Storm - mission overrides and local definitions

[Trigger ledger](all12s.md) | [Team plans](all12s-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS01.MIX/all12s.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| SEAL (GHOST) | Technology level | 5 | 2 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Cell Spread | 1 | 5 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Percent At Max | .5 | 6 |
| Tesla Coil (TESLA) | Signed power contribution | -10 | 9 |
| War Miner (HARV) | Resource cargo capacity | 20 | 12 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 15 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 18 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 19 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 20 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 21 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 24 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 27 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 30 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 33 |
| Iron Curtain (IRONCURTAINSPECIAL) | Recharge Time | 10 | 36 |
| Nuclear Missile (MULTISPECIAL) | Recharge Time | 20 | 39 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 1000,750,500 | 42 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 4000 | 43 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -4000 | 44 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Line Trail Color | 80,80,90 | 45 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Parachute Max Fall Rate | -10 | 46 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Total AI Team Cap | 60,40,30 | 47 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Chrono Reinf Delay | 60 | 48 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Spy Money Steal Percent | .03 | 49 |
| Engineer (SENGINEER) | Technology level | -1 | 52 |
| Tanya (TANY) | Name | Tanya | 64 |
| Tanya (TANY) | Primary | MP5 | 65 |
| Tanya (TANY) | Assaulter | yes | 66 |
| Tanya (TANY) | Starting health capacity | 250 | 67 |
| Tanya (TANY) | Armor class | flak | 68 |
| Tanya (TANY) | Sight radius setting | 8 | 69 |
| Tanya (TANY) | Movement rating | 6 | 70 |
| Tanya (TANY) | Technology level | -1 | 71 |
| MP5 (MP5) | Damage | 125 | 74 |
| MP5 (MP5) | ROF | 10 | 75 |
| MP5 (MP5) | Range | 8 | 76 |
| Attack Dog (DOG) | UI Name | Name:DOG | 79 |
| Attack Dog (DOG) | Name | Attack Dog | 80 |
| Attack Dog (DOG) | Technology level | -1 | 81 |
| Negative Light Post (NEGLAMP) | Name | Negative Light Post | 84 |
| Negative Light Post (NEGLAMP) | Image | GALITE | 85 |
| Negative Light Post (NEGLAMP) | Local light reach | 5000 | 86 |
| Negative Light Post (NEGLAMP) | Local light intensity | -0.15 | 87 |
| Negative Light Post (NEGLAMP) | Light Red Tint | 0.03 | 88 |
| Negative Light Post (NEGLAMP) | Light Green Tint | 0.04 | 89 |
| Negative Light Post (NEGLAMP) | Light Blue Tint | 0.04 | 90 |
| Invisible Purple Light Post (INPURPLAMP) | Name | Invisible Purple Light Post | 93 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 4000 | 94 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.01 | 95 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 0.67059 | 96 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.19608 | 97 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 0.67059 | 98 |
| Invisible Yellow Light Post (INYELWLAMP) | Name | Invisible Yellow Light Post | 101 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 4000 | 102 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 103 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.2 | 104 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.2 | 105 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.0 | 106 |
| SPECIALFLAGS | Tiberium Grows | no | 109 |
| SPECIALFLAGS | Tiberium Spreads | yes | 110 |
| SPECIALFLAGS | Tiberium Explosive | no | 111 |
| SPECIALFLAGS | Destroyable Bridges | no | 112 |
| SPECIALFLAGS | MCV Deploy | no | 113 |
| SPECIALFLAGS | Initial Veteran | no | 114 |
| SPECIALFLAGS | Fixed Alliance | no | 115 |
| SPECIALFLAGS | Harvester Immune | no | 116 |
| SPECIALFLAGS | Fog Of War | no | 117 |
| SPECIALFLAGS | Inert | no | 118 |
| SPECIALFLAGS | Ion Storms | no | 119 |
| SPECIALFLAGS | Meteorites | no | 120 |
| SPECIALFLAGS | Visceroids | no | 121 |
| COUNTRIES (COUNTRIES) | 0 | Player | 124 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 125 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 126 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 127 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 128 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 129 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 130 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 131 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Play Final Movie,0 | 249 |
| VARIABLENAMES (VARIABLENAMES) | 1 | MammothDead1,0 | 250 |
| VARIABLENAMES (VARIABLENAMES) | 2 | MammothDead2,0 | 251 |
| VARIABLENAMES (VARIABLENAMES) | 3 | MammothDead3,0 | 252 |
| VARIABLENAMES (VARIABLENAMES) | 4 | MammothDead4,0 | 253 |
| VARIABLENAMES (VARIABLENAMES) | 5 | TanyaLaugh,0 | 254 |
