# Operation: Deja Vu - mission overrides and local definitions

[Trigger ledger](sov02smd.md) | [Team plans](sov02smd-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: mapsmd03.mix/sov02smd.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Rhino Heavy Tank (HTNK) | Production-time multiplier | 1.0 | 11 |
| Grizzly Battle Tank (MTNK) | Production-time multiplier | 1.0 | 14 |
| Lasher Light Tank (LTNK) | Production-time multiplier | 1.0 | 17 |
| Iron Curtain Device (NAIRON) | Technology level | 12 | 20 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | AI Safe Distance | 20 | 23 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Default Mirage Disguises | TREE26,TREE27,TREE28,TREE25 | 24 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Spy Money Steal Percent | .05 | 25 |
| War Miner (HARV) | Resource cargo capacity | 20 | 28 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 31 |
| Engineer (ENGINEER) | Name | Engineer | 34 |
| Engineer (ENGINEER) | Excluded countries | Russians,Confederation,Africans,Arabs,YuriCountry,Player | 35 |
| Engineer (YENGINEER) | Excluded countries | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,Player | 38 |
| Attack Dog (ADOG) | Name | Allied Attack Dog | 41 |
| Attack Dog (ADOG) | Excluded countries | Russians,Confederation,Africans,Arabs,YuriCountry,Player | 42 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 45 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 46 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 47 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 48 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 51 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 54 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 57 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 60 |
| CRATERULES (CRATERULES) | Solo Crate Money | 1500 | 63 |
| CRATERULES (CRATERULES) | Unit Crate Type | CMIN | 64 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Wall behavior | Yes | 67 |
| Nuclear Missile Silo (NAMISL) | Technology level | 12 | 70 |
| Chronosphere (CHRONOSPHERESPECIAL) | Recharge Time | 10 | 73 |
| Chrono Sphere (GACSPH) | Name | Allied Chrono Sphere | 76 |
| Chrono Sphere (GACSPH) | Reveal To All | no | 77 |
| Yuri Clone (YURI) | Technology level | 12 | 80 |
| Chrono Legionnaire (CLEG) | Technology level | 12 | 83 |
| Siege Chopper (SCHP) | Technology level | 12 | 86 |
| Soviet Shipyard (NAYARD) | Technology level | 12 | 89 |
| Allied Shipyard (GAYARD) | Technology level | 12 | 92 |
| Weather Controller (GAWEAT) | Technology level | 12 | 95 |
| Cloning Vats (NACLON) | Technology level | 12 | 98 |
| Psychic Radar (NAPSIS) | Technology level | 12 | 101 |
| Kirov Airship (ZEP) | Technology level | 9 | 104 |
| Industrial Plant (NAINDP) | Technology level | 9 | 107 |
| Boris (BORIS) | Technology level | 12 | 110 |
| Air Force Command Headquarters (AMRADR) | Name | Airforce Command Headquarters | 113 |
| Air Force Command Headquarters (AMRADR) | Primary granted special weapon | none | 114 |
| Tanya (TANY) | Technology level | 12 | 117 |
| SEAL (GHOST) | Name | SEAL | 120 |
| SEAL (GHOST) | Technology level | 3 | 121 |
| Technician (CTECH) | Name | Technician | 124 |
| Technician (CTECH) | Insignificant-object flag | no | 125 |
| Technician (CTECH) | Threat contribution | 10 | 126 |
| Technician (CTECH) | Primary | M1Carbine | 127 |
| Barrels (CAMISC01) | Name | RA2 Barrels | 130 |
| Barrels (CAMISC01) | Insignificant-object flag | no | 131 |
| Barrels (CAMISC01) | Hidden from radar | no | 132 |
| Barrel (CAMISC02) | Name | RA2 Barrel | 135 |
| Barrel (CAMISC02) | Insignificant-object flag | no | 136 |
| Barrel (CAMISC02) | Hidden from radar | no | 137 |
| Einstein's Laboratory (CALAB) | Name | RA2 Einstein's Lab | 140 |
| Einstein's Laboratory (CALAB) | Technology level | -1 | 141 |
| Einstein's Laboratory (CALAB) | Insignificant-object flag | no | 142 |
| Einstein's Laboratory (CALAB) | Engineer-capture permission | true | 143 |
| Einstein's Laboratory (CALAB) | Hidden from radar | no | 144 |
| Einstein's Laboratory (CALAB) | Repair-tool permission | yes | 145 |
| Einstein's Laboratory (CALAB) | Infantry garrison permitted | no | 146 |
| Einstein's Laboratory (CALAB) | Garrison capacity | 0 | 147 |
| Einstein's Laboratory (CALAB) | Distributed Fire | no | 148 |
| Einstein's Laboratory (CALAB) | Primary | none | 149 |
| Einstein's Laboratory (CALAB) | Secondary | none | 150 |
| SPECIALFLAGS | Tiberium Grows | yes | 153 |
| SPECIALFLAGS | Tiberium Spreads | yes | 154 |
| SPECIALFLAGS | Tiberium Explosive | no | 155 |
| SPECIALFLAGS | Destroyable Bridges | yes | 156 |
| SPECIALFLAGS | MCV Deploy | no | 157 |
| SPECIALFLAGS | Initial Veteran | no | 158 |
| SPECIALFLAGS | Fixed Alliance | no | 159 |
| SPECIALFLAGS | Harvester Immune | no | 160 |
| SPECIALFLAGS | Fog Of War | no | 161 |
| SPECIALFLAGS | Inert | no | 162 |
| SPECIALFLAGS | Ion Storms | no | 163 |
| SPECIALFLAGS | Meteorites | no | 164 |
| SPECIALFLAGS | Visceroids | no | 165 |
| COUNTRIES (COUNTRIES) | 0 | Einstein | 168 |
| COUNTRIES (COUNTRIES) | 1 | Player | 169 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy1 | 170 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy2 | 171 |
| COUNTRIES (COUNTRIES) | 4 | BadGuy3 | 172 |
| COUNTRIES (COUNTRIES) | 5 | Germany1 | 173 |
| COUNTRIES (COUNTRIES) | 6 | Germany2 | 174 |
| COUNTRIES (COUNTRIES) | 7 | Germany3 | 175 |
| COUNTRIES (COUNTRIES) | 8 | Temp | 176 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Refinery Owned,0 | 319 |
| VARIABLENAMES (VARIABLENAMES) | 1 | BG1s Refinery,0 | 320 |
| VARIABLENAMES (VARIABLENAMES) | 2 | BG2s Refinery,0 | 321 |
| VARIABLENAMES (VARIABLENAMES) | 3 | BG2 ConYard Up,0 | 322 |
| VARIABLENAMES (VARIABLENAMES) | 4 | Briefing Complete,0 | 323 |
| VARIABLENAMES (VARIABLENAMES) | 5 | Chrono Prisons Go,0 | 324 |
| VARIABLENAMES (VARIABLENAMES) | 6 | Transfer Chronosphe,0 | 325 |
| VARIABLENAMES (VARIABLENAMES) | 7 | Einstein Lab KIA,0 | 326 |
| VARIABLENAMES (VARIABLENAMES) | 8 | Chronosphere KIA,0 | 327 |
| VARIABLENAMES (VARIABLENAMES) | 9 | Einstein Chrono Off,0 | 328 |
| VARIABLENAMES (VARIABLENAMES) | 10 | Early Air Attks,0 | 329 |
| VARIABLENAMES (VARIABLENAMES) | 11 | G1_Barracks_Gone,0 | 330 |
| VARIABLENAMES (VARIABLENAMES) | 12 | G2_Barracks_Gone,0 | 331 |
| VARIABLENAMES (VARIABLENAMES) | 13 | G3_Barracks_Gone,0 | 332 |
| VARIABLENAMES (VARIABLENAMES) | 14 | Troops2_Arrived,0 | 333 |
| VARIABLENAMES (VARIABLENAMES) | 15 | Troops1_Arrived,0 | 334 |
| VARIABLENAMES (VARIABLENAMES) | 16 | Troops3_Arrived,0 | 335 |
