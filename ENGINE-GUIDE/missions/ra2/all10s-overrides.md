# Operation: Mirage - mission overrides and local definitions

[Trigger ledger](all10s.md) | [Team plans](all10s-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS01.MIX/all10s.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 1500,750,500 | 11 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | AI Safe Distance | 20 | 12 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Default Mirage Disguises | TREE26,TREE27,TREE28,TREE25 | 13 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Spy Money Steal Percent | .05 | 14 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Total AI Team Cap | 30,30,30 | 15 |
| War Miner (HARV) | Resource cargo capacity | 20 | 18 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 21 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 24 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 25 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 26 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 27 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 30 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 33 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 36 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 39 |
| CRATERULES (CRATERULES) | Solo Crate Money | 1500 | 42 |
| CRATERULES (CRATERULES) | Unit Crate Type | CMIN | 43 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Wall behavior | Yes | 46 |
| COLORS (COLORS) | Neo Red | 0,140,205 | 49 |
| Chrono Sphere (GACSPH) | Name | Chrono Sphere | 52 |
| Chrono Sphere (GACSPH) | Technology level | 12 | 53 |
| Allied Construction Vehicle (AMCV) | Technology level | 5 | 56 |
| Chronosphere (CHRONOSPHERESPECIAL) | Recharge Time | 120 | 59 |
| Chronosphere (CHRONOSPHERESPECIAL) | Show Timer | no | 60 |
| Engineer (SENGINEER) | Technology level | 10 | 63 |
| Attack Dog (DOG) | Technology level | 10 | 66 |
| Nuclear Missile Silo (NAMISL) | Technology level | 12 | 69 |
| Iron Curtain Device (NAIRON) | Technology level | 12 | 72 |
| Yuri (YURI) | Technology level | 12 | 75 |
| Chrono Legionnaire (CLEG) | Technology level | 12 | 78 |
| Soviet Shipyard (NAYARD) | Technology level | 12 | 81 |
| Kirov Airship (ZEP) | Technology level | 12 | 84 |
| Allied Shipyard (GAYARD) | Technology level | 12 | 87 |
| Weather Controller (GAWEAT) | Technology level | 12 | 90 |
| Gap Generator (GAGAP) | Name | Gap Generator | 93 |
| Gap Generator (GAGAP) | Technology level | 12 | 94 |
| Cloning Vats (NACLON) | Technology level | 12 | 97 |
| Psychic Sensor (NAPSIS) | Technology level | 12 | 100 |
| Tanya (TANY) | Technology level | 12 | 103 |
| Ore Purifier (GAOREP) | Name | Allied Ore Processor | 106 |
| Ore Purifier (GAOREP) | Technology level | 9 | 107 |
| SEAL (GHOST) | Name | SEAL | 110 |
| SEAL (GHOST) | Technology level | 3 | 111 |
| Technician (CTECH) | Name | Technician | 114 |
| Technician (CTECH) | Insignificant-object flag | no | 115 |
| Technician (CTECH) | Threat contribution | 10 | 116 |
| Negative Light Post (NEGLAMP) | Name | Negative Light Post | 119 |
| Negative Light Post (NEGLAMP) | Image | GALITE | 120 |
| Negative Light Post (NEGLAMP) | Local light reach | 4000 | 121 |
| Negative Light Post (NEGLAMP) | Local light intensity | -0.15 | 122 |
| Negative Light Post (NEGLAMP) | Light Red Tint | 0.03 | 123 |
| Negative Light Post (NEGLAMP) | Light Green Tint | 0.04 | 124 |
| Negative Light Post (NEGLAMP) | Light Blue Tint | 0.04 | 125 |
| Invisible Purple Light Post (INPURPLAMP) | Name | Invisible Purple Light Post | 128 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 4000 | 129 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.01 | 130 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 0.4000 | 131 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.0000 | 132 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 0.4000 | 133 |
| Invisible Yellow Light Post (INYELWLAMP) | Name | Invisible Yellow Light Post | 136 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 4000 | 137 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 138 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.2 | 139 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.2 | 140 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | -0.1 | 141 |
| Barrels (CAMISC01) | Name | RA2 Barrels | 144 |
| Barrels (CAMISC01) | Insignificant-object flag | no | 145 |
| Barrels (CAMISC01) | Hidden from radar | no | 146 |
| Barrel (CAMISC02) | Name | RA2 Barrel | 149 |
| Barrel (CAMISC02) | Insignificant-object flag | no | 150 |
| Barrel (CAMISC02) | Hidden from radar | no | 151 |
| Einstein's Laboratory (CALAB) | Name | RA2 Einstein's Lab | 154 |
| Einstein's Laboratory (CALAB) | Technology level | -1 | 155 |
| Einstein's Laboratory (CALAB) | Insignificant-object flag | no | 156 |
| Einstein's Laboratory (CALAB) | Hidden from radar | no | 157 |
| Einstein's Laboratory (CALAB) | Repair-tool permission | yes | 158 |
| Einstein's Laboratory (CALAB) | Infantry garrison permitted | no | 159 |
| Einstein's Laboratory (CALAB) | Garrison capacity | 0 | 160 |
| Einstein's Laboratory (CALAB) | Distributed Fire | no | 161 |
| Einstein's Laboratory (CALAB) | Primary | none | 162 |
| Einstein's Laboratory (CALAB) | Secondary | none | 163 |
| SPECIALFLAGS | Tiberium Grows | no | 166 |
| SPECIALFLAGS | Tiberium Spreads | yes | 167 |
| SPECIALFLAGS | Tiberium Explosive | no | 168 |
| SPECIALFLAGS | Destroyable Bridges | yes | 169 |
| SPECIALFLAGS | MCV Deploy | no | 170 |
| SPECIALFLAGS | Initial Veteran | no | 171 |
| SPECIALFLAGS | Fixed Alliance | no | 172 |
| SPECIALFLAGS | Harvester Immune | no | 173 |
| SPECIALFLAGS | Fog Of War | no | 174 |
| SPECIALFLAGS | Inert | no | 175 |
| SPECIALFLAGS | Ion Storms | no | 176 |
| SPECIALFLAGS | Meteorites | no | 177 |
| SPECIALFLAGS | Visceroids | no | 178 |
| COUNTRIES (COUNTRIES) | 0 | Einstein | 181 |
| COUNTRIES (COUNTRIES) | 1 | Player | 182 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy1 | 183 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy2 | 184 |
| COUNTRIES (COUNTRIES) | 4 | BadGuy3 | 185 |
| COUNTRIES (COUNTRIES) | 5 | Germany1 | 186 |
| COUNTRIES (COUNTRIES) | 6 | Germany2 | 187 |
| COUNTRIES (COUNTRIES) | 7 | Germany3 | 188 |
| COUNTRIES (COUNTRIES) | 8 | Temp | 189 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Einsteins Gift FLG,0 | 325 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Einstein Audio1,0 | 326 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Einstein Audio2,0 | 327 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Einstein Audio3,0 | 328 |
| VARIABLENAMES (VARIABLENAMES) | 4 | SpySat Audio Played,0 | 329 |
| VARIABLENAMES (VARIABLENAMES) | 5 | Polar Bears Gone,0 | 330 |
| VARIABLENAMES (VARIABLENAMES) | 6 | Woman in Car,0 | 331 |
| VARIABLENAMES (VARIABLENAMES) | 7 | Spawn Crate,0 | 332 |
| VARIABLENAMES (VARIABLENAMES) | 8 | Spawn Crate2,0 | 333 |
| VARIABLENAMES (VARIABLENAMES) | 9 | Spawn Crate3,0 | 334 |
| VARIABLENAMES (VARIABLENAMES) | 10 | Spawn Crate4,0 | 335 |
| VARIABLENAMES (VARIABLENAMES) | 11 | Spawn Crate5,0 | 336 |
| VARIABLENAMES (VARIABLENAMES) | 12 | Spawn Crate6,0 | 337 |
| VARIABLENAMES (VARIABLENAMES) | 13 | Spawn Crate7,0 | 338 |
| VARIABLENAMES (VARIABLENAMES) | 14 | Purifier Exists,0 | 339 |
