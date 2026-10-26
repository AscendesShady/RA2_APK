# Operation: Head Games - mission overrides and local definitions

[Trigger ledger](sov07tmd.md) | [Team plans](sov07tmd-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: mapsmd03.mix/sov07tmd.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | AI Safe Distance | 20 | 2 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Spy Money Steal Percent | .05 | 3 |
| CRATERULES (CRATERULES) | Solo Crate Money | 2500 | 6 |
| Tech Secret Lab (CASLAB) | Name | Tech Secret Lab | 9 |
| Tech Secret Lab (CASLAB) | Secret Building | GTGCAN | 10 |
| Rhino Heavy Tank (HTNK) | Production-time multiplier | 1.0 | 13 |
| Grizzly Battle Tank (MTNK) | Production-time multiplier | 1.0 | 16 |
| Lasher Light Tank (LTNK) | Production-time multiplier | 1.0 | 19 |
| Tesla Tank (TTNK) | Name | Tesla Tank | 22 |
| Tesla Tank (TTNK) | Technology level | 2 | 23 |
| Tesla Tank (TTNK) | Required countries | Player,BadGuy2 | 24 |
| Engineer (ENGINEER) | Name | Engineer | 27 |
| Engineer (ENGINEER) | Excluded countries | Russians,Confederation,Africans,Arabs,YuriCountry,Player | 28 |
| Engineer (YENGINEER) | Excluded countries | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,Player | 31 |
| Attack Dog (ADOG) | Name | Allied Attack Dog | 34 |
| Attack Dog (ADOG) | Excluded countries | Russians,Confederation,Africans,Arabs,YuriCountry,Player | 35 |
| Desolator (DESO) | Name | Desolater | 38 |
| Desolator (DESO) | Required countries | Arabs,BadGuy2,Player | 39 |
| Yuri's Fortress (CATRAN03) | Name | TRANS FORTRESS | 42 |
| Yuri's Fortress (CATRAN03) | Starting health capacity | 5000 | 43 |
| Yuri's Fortress (CATRAN03) | Armor class | concrete | 44 |
| Yuri's Fortress (CATRAN03) | Repair-tool permission | yes | 45 |
| Yuri's Fortress (CATRAN03) | Engineer-capture permission | false | 46 |
| Yuri's Fortress (CATRAN03) | To Protect | yes | 47 |
| Grinder (YAGRND) | Name | Yuri Grinder | 50 |
| Grinder (YAGRND) | Crewed | no | 51 |
| Building (CAPARS04) | Name | Paris Building 4 | 54 |
| Building (CAPARS04) | Starting health capacity | 1000 | 55 |
| Building (CAPARS06) | Name | Paris Building 6 | 58 |
| Building (CAPARS06) | Starting health capacity | 1000 | 59 |
| Allied Shipyard (GAYARD) | Technology level | 12 | 62 |
| Soviet Shipyard (NAYARD) | Technology level | 12 | 65 |
| Yuri Naval Yard (YAYARD) | Technology level | 12 | 68 |
| Boris (BORIS) | Name | Boris | 71 |
| Boris (BORIS) | Technology level | 12 | 72 |
| Tanya (TANY) | Name | Tanya | 75 |
| Tanya (TANY) | Technology level | 12 | 76 |
| Yuri Prime (YURIPR) | Name | Yuri Prime | 79 |
| Yuri Prime (YURIPR) | Technology level | 12 | 80 |
| Chrono Sphere (GACSPH) | Name | Allied Chrono Sphere | 83 |
| Chrono Sphere (GACSPH) | Technology level | 12 | 84 |
| Terrorist (TERROR) | Name | Terrorist | 87 |
| Terrorist (TERROR) | Required structures/groups | NAHAND,RADAR | 88 |
| Terrorist (TERROR) | Technology level | 12 | 89 |
| Terrorist (TERROR) | Required countries | Player | 90 |
| Demolition Truck (DTRUCK) | Name | Demolitions Truck | 93 |
| Demolition Truck (DTRUCK) | Required structures/groups | NAWEAP,RADAR | 94 |
| Demolition Truck (DTRUCK) | Technology level | 12 | 95 |
| Demolition Truck (DTRUCK) | Required countries | Player | 96 |
| Orange Light Post (INORANLAMP) | Local light reach | 3000 | 99 |
| Orange Light Post (INORANLAMP) | Local light intensity | 0.005 | 100 |
| Orange Light Post (INORANLAMP) | Light Red Tint | 1.00 | 101 |
| Orange Light Post (INORANLAMP) | Light Green Tint | 0.15 | 102 |
| Orange Light Post (INORANLAMP) | Light Blue Tint | 0.02 | 103 |
| Negative Light Post (NEGLAMP) | Name | Negative Light Post | 106 |
| Negative Light Post (NEGLAMP) | Local light reach | 5000 | 107 |
| Negative Light Post (NEGLAMP) | Local light intensity | -0.10 | 108 |
| Negative Light Post (NEGLAMP) | Light Red Tint | 0.03 | 109 |
| Negative Light Post (NEGLAMP) | Light Green Tint | 0.04 | 110 |
| Negative Light Post (NEGLAMP) | Light Blue Tint | 0.04 | 111 |
| Invisible Yellow Light Post (INYELWLAMP) | Name | Invisible Yellow Light Post | 114 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 2500 | 115 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | .01 | 116 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.4392 | 117 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.4471 | 118 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.1138 | 119 |
| COUNTRIES (COUNTRIES) | 0 | Einstein | 122 |
| COUNTRIES (COUNTRIES) | 1 | Player | 123 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy1 | 124 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy2 | 125 |
| COUNTRIES (COUNTRIES) | 4 | BadGuy3 | 126 |
| COUNTRIES (COUNTRIES) | 5 | Germany1 | 127 |
| COUNTRIES (COUNTRIES) | 6 | Germany2 | 128 |
| COUNTRIES (COUNTRIES) | 7 | Germany3 | 129 |
| COUNTRIES (COUNTRIES) | 8 | Temp | 130 |
| SPECIALFLAGS | Tiberium Grows | yes | 238 |
| SPECIALFLAGS | Tiberium Spreads | yes | 239 |
| SPECIALFLAGS | Tiberium Explosive | no | 240 |
| SPECIALFLAGS | Destroyable Bridges | yes | 241 |
| SPECIALFLAGS | MCV Deploy | no | 242 |
| SPECIALFLAGS | Initial Veteran | no | 243 |
| SPECIALFLAGS | Fixed Alliance | no | 244 |
| SPECIALFLAGS | Harvester Immune | no | 245 |
| SPECIALFLAGS | Fog Of War | no | 246 |
| SPECIALFLAGS | Inert | no | 247 |
| SPECIALFLAGS | Ion Storms | no | 248 |
| SPECIALFLAGS | Meteorites | no | 249 |
| SPECIALFLAGS | Visceroids | no | 250 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Minions Build,0 | 300 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Demo Driver L In,0 | 301 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Demo Driver R In,0 | 302 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Player MCV on map,0 | 303 |
| VARIABLENAMES (VARIABLENAMES) | 4 | Deployed MCV,0 | 304 |
| VARIABLENAMES (VARIABLENAMES) | 5 | Soviets Freed,0 | 305 |
| VARIABLENAMES (VARIABLENAMES) | 6 | Allies Freed,0 | 306 |
| VARIABLENAMES (VARIABLENAMES) | 7 | IFV for Combine 1,0 | 307 |
| VARIABLENAMES (VARIABLENAMES) | 8 | Shock for Combine 1,0 | 308 |
| VARIABLENAMES (VARIABLENAMES) | 9 | Combine 01,0 | 309 |
| VARIABLENAMES (VARIABLENAMES) | 10 | Combine 02,0 | 310 |
| VARIABLENAMES (VARIABLENAMES) | 11 | IFV for Combine 2,0 | 311 |
| VARIABLENAMES (VARIABLENAMES) | 12 | Shock for Combine 2,0 | 312 |
| VARIABLENAMES (VARIABLENAMES) | 13 | IFV for Combine 3,0 | 313 |
| VARIABLENAMES (VARIABLENAMES) | 14 | Troops for Combine ,0 | 314 |
| VARIABLENAMES (VARIABLENAMES) | 15 | Combine 03a,0 | 315 |
| VARIABLENAMES (VARIABLENAMES) | 16 | Combine 03b,0 | 316 |
| VARIABLENAMES (VARIABLENAMES) | 17 | Combine 03c,0 | 317 |
| VARIABLENAMES (VARIABLENAMES) | 18 | Combine 03d,0 | 318 |
| VARIABLENAMES (VARIABLENAMES) | 19 | Combine 03e,0 | 319 |
| VARIABLENAMES (VARIABLENAMES) | 20 | WCryptKIA,0 | 320 |
| VARIABLENAMES (VARIABLENAMES) | 21 | ECryptKIA,0 | 321 |
| VARIABLENAMES (VARIABLENAMES) | 22 | SW Grinder KIA,0 | 322 |
| VARIABLENAMES (VARIABLENAMES) | 23 | NE Grinder KIA,0 | 323 |
