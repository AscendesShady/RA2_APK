# Operation: Home Front - mission overrides and local definitions

[Trigger ledger](sov04s.md) | [Team plans](sov04s-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov04s.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
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
| AI (AI) | Attack Interval | 0.01 | 35 |
| AI (AI) | Attack Delay | 0.10 | 36 |
| 155MM (155MM) | Range | 10 | 39 |
| Destroyer (DEST) | Name | Destroyer | 42 |
| Destroyer (DEST) | Technology level | 5 | 43 |
| Allied Repair Depot (GADEPT) | Name | Service Depot | 46 |
| Allied Repair Depot (GADEPT) | Technology level | 6 | 47 |
| Tesla Coil (TESLA) | Name | Tesla Coil | 50 |
| Tesla Coil (TESLA) | Technology level | 12 | 51 |
| Prism Tower (ATESLA) | Name | Prism Cannon | 54 |
| Prism Tower (ATESLA) | Technology level | 12 | 55 |
| Aircraft Carrier (CARRIER) | Name | Aircraft Carrier | 58 |
| Aircraft Carrier (CARRIER) | Technology level | 12 | 59 |
| Engineer (ENGINEER) | Name | Engineer | 62 |
| Engineer (ENGINEER) | Technology level | 12 | 63 |
| Attack Dog (ADOG) | Name | Allied Attack Dog | 66 |
| Attack Dog (ADOG) | Technology level | 12 | 67 |
| Spy (SPY) | Name | Spy | 70 |
| Spy (SPY) | Technology level | 12 | 71 |
| Dolphin (DLPH) | Name | Dolphin | 74 |
| Dolphin (DLPH) | Technology level | 12 | 75 |
| Allied Battle Lab (GATECH) | Name | Allied Battle Lab | 78 |
| Allied Battle Lab (GATECH) | Technology level | 12 | 79 |
| Soviet Battle Lab (NATECH) | Name | Soviet Battle Lab | 82 |
| Soviet Battle Lab (NATECH) | Technology level | 12 | 83 |
| Crazy Ivan (IVAN) | Name | Crazy Ivan | 86 |
| Crazy Ivan (IVAN) | Technology level | 12 | 87 |
| Tesla Trooper (SHK) | Name | Shock Trooper | 90 |
| Tesla Trooper (SHK) | Technology level | 5 | 91 |
| Dreadnought (DRED) | Name | Dreadnought | 94 |
| Dreadnought (DRED) | Technology level | 12 | 95 |
| Yuri (YURI) | Name | Yuri | 98 |
| Yuri (YURI) | Technology level | 12 | 99 |
| Gap Generator (GAGAP) | Name | Gap Generator | 102 |
| Gap Generator (GAGAP) | Technology level | 12 | 103 |
| Patriot Missile (NASAM) | Name | Patriot Missile | 106 |
| Patriot Missile (NASAM) | Technology level | 12 | 107 |
| Light House (CAFARM06) | Name | RA2 Lighthouse | 110 |
| Light House (CAFARM06) | Insignificant-object flag | no | 111 |
| Soviet Construction Vehicle (SMCV) | Name | Soviet Construction Vehicle | 114 |
| Soviet Construction Vehicle (SMCV) | Technology level | 6 | 115 |
| Negative Light Post (NEGLAMP) | Name | Negative Light Post | 118 |
| Negative Light Post (NEGLAMP) | Image | GALITE | 119 |
| Negative Light Post (NEGLAMP) | Local light reach | 4000 | 120 |
| Negative Light Post (NEGLAMP) | Local light intensity | -0.15 | 121 |
| Negative Light Post (NEGLAMP) | Light Red Tint | 0.03 | 122 |
| Negative Light Post (NEGLAMP) | Light Green Tint | 0.04 | 123 |
| Negative Light Post (NEGLAMP) | Light Blue Tint | 0.04 | 124 |
| Invisible Purple Light Post (INPURPLAMP) | Name | Invisible Purple Light Post | 127 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 4000 | 128 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.01 | 129 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 0.4000 | 130 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.0000 | 131 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 0.4000 | 132 |
| Invisible Yellow Light Post (INYELWLAMP) | Name | Invisible Yellow Light Post | 135 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 4000 | 136 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 137 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.2 | 138 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.2 | 139 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | -0.1 | 140 |
| SPECIALFLAGS | Tiberium Grows | no | 143 |
| SPECIALFLAGS | Tiberium Spreads | yes | 144 |
| SPECIALFLAGS | Tiberium Explosive | no | 145 |
| SPECIALFLAGS | Destroyable Bridges | yes | 146 |
| SPECIALFLAGS | MCV Deploy | no | 147 |
| SPECIALFLAGS | Initial Veteran | no | 148 |
| SPECIALFLAGS | Fixed Alliance | no | 149 |
| SPECIALFLAGS | Harvester Immune | no | 150 |
| SPECIALFLAGS | Fog Of War | no | 151 |
| SPECIALFLAGS | Inert | no | 152 |
| SPECIALFLAGS | Ion Storms | no | 153 |
| SPECIALFLAGS | Meteorites | no | 154 |
| SPECIALFLAGS | Visceroids | no | 155 |
| COUNTRIES (COUNTRIES) | 0 | Other1 | 158 |
| COUNTRIES (COUNTRIES) | 1 | Player | 159 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy1 | 160 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy2 | 161 |
| COUNTRIES (COUNTRIES) | 4 | BadGuy3 | 162 |
| COUNTRIES (COUNTRIES) | 5 | Germany1 | 163 |
| COUNTRIES (COUNTRIES) | 6 | Germany2 | 164 |
| COUNTRIES (COUNTRIES) | 7 | Germany3 | 165 |
| COUNTRIES (COUNTRIES) | 8 | Temp | 166 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Flak Cannons Up,0 | 297 |
| VARIABLENAMES (VARIABLENAMES) | 1 | GIs ashore,0 | 298 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Grizzly ashore,0 | 299 |
| VARIABLENAMES (VARIABLENAMES) | 3 | MCV ashore,0 | 300 |
| VARIABLENAMES (VARIABLENAMES) | 4 | Grizzly2 ashore,0 | 301 |
| VARIABLENAMES (VARIABLENAMES) | 5 | GI2 ashore,0 | 302 |
| VARIABLENAMES (VARIABLENAMES) | 6 | Allied Fleet Here,0 | 303 |
| VARIABLENAMES (VARIABLENAMES) | 7 | Feint GI Landing 1,0 | 304 |
| VARIABLENAMES (VARIABLENAMES) | 8 | Feint GI Landing 2,0 | 305 |
| VARIABLENAMES (VARIABLENAMES) | 9 | Feint Tank Landing ,0 | 306 |
| VARIABLENAMES (VARIABLENAMES) | 10 | Feint Tank Landing ,0 | 307 |
| VARIABLENAMES (VARIABLENAMES) | 11 | Feint Tank Landing ,0 | 308 |
| VARIABLENAMES (VARIABLENAMES) | 12 | Feint Tank 1,0 | 309 |
| VARIABLENAMES (VARIABLENAMES) | 13 | Feint Tank 2,0 | 310 |
