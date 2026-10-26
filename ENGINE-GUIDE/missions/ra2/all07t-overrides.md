# Operation: Deep Sea - mission overrides and local definitions

[Trigger ledger](all07t.md) | [Team plans](all07t-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS01.MIX/all07t.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 1500,1000,750 | 11 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Spy Money Steal Percent | .05 | 12 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Total AI Team Cap | 30,30,30 | 13 |
| War Miner (HARV) | Resource cargo capacity | 20 | 16 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 19 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 22 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 23 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 24 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 25 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 28 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 31 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 34 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 37 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Wall behavior | Yes | 40 |
| Soviet Construction Vehicle (SMCV) | Name | Soviet Construction Vehicle | 43 |
| Soviet Construction Vehicle (SMCV) | Required structures/groups | NAWEAP | 44 |
| Soviet Construction Vehicle (SMCV) | Technology level | 8 | 45 |
| SEAL (GHOST) | Technology level | 12 | 48 |
| Apocalypse (APOC) | Name | Apocalypse | 51 |
| Apocalypse (APOC) | Technology level | 12 | 52 |
| Engineer (SENGINEER) | Technology level | 10 | 55 |
| Attack Dog (DOG) | Technology level | 10 | 58 |
| Tanya (TANY) | Technology level | 12 | 61 |
| Allied Construction Vehicle (AMCV) | Technology level | 5 | 64 |
| Yuri (YURI) | Technology level | 12 | 67 |
| Crazy Ivan (IVAN) | Technology level | 12 | 70 |
| Desolator (DESO) | Technology level | 12 | 73 |
| Chrono Legionnaire (CLEG) | Technology level | 12 | 76 |
| Dolphin (DLPH) | Technology level | 12 | 79 |
| Giant Squid (SQD) | Technology level | 12 | 82 |
| Mirage Tank (MGTK) | Technology level | 12 | 85 |
| Tesla Tank (TTNK) | Technology level | 12 | 88 |
| Prism Tank (SREF) | Technology level | 12 | 91 |
| Kirov Airship (ZEP) | Technology level | 12 | 94 |
| Ore Purifier (GAOREP) | Technology level | 12 | 97 |
| SpySat Uplink (GASPYSAT) | Technology level | 12 | 100 |
| Cloning Vats (NACLON) | Technology level | 12 | 103 |
| Iron Curtain Device (NAIRON) | Technology level | 12 | 106 |
| Weather Controller (GAWEAT) | Technology level | 12 | 109 |
| Chrono Sphere (GACSPH) | Technology level | 12 | 112 |
| Gap Generator (GAGAP) | Name | Gap Generator | 115 |
| Gap Generator (GAGAP) | Technology level | 12 | 116 |
| Psychic Sensor (NAPSIS) | Technology level | 12 | 119 |
| Nuclear Reactor (NANRCT) | Technology level | 12 | 122 |
| Police Car (COP) | Name | RA2 Pig | 125 |
| Police Car (COP) | Ambient Sound | Dummy | 126 |
| Air Force Command Headquarters (AMRADR) | Name | Airforce Command Headquarters | 129 |
| Air Force Command Headquarters (AMRADR) | Primary granted special weapon | none | 130 |
| Negative Light Post (NEGLAMP) | Name | Negative Light Post | 133 |
| Negative Light Post (NEGLAMP) | Image | GALITE | 134 |
| Negative Light Post (NEGLAMP) | Local light reach | 5000 | 135 |
| Negative Light Post (NEGLAMP) | Local light intensity | -0.15 | 136 |
| Negative Light Post (NEGLAMP) | Light Red Tint | 0.03 | 137 |
| Negative Light Post (NEGLAMP) | Light Green Tint | 0.04 | 138 |
| Negative Light Post (NEGLAMP) | Light Blue Tint | 0.04 | 139 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 3500 | 142 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.30 | 143 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.25 | 144 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.10 | 145 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.01 | 146 |
| SPECIALFLAGS | Tiberium Grows | yes | 149 |
| SPECIALFLAGS | Tiberium Spreads | yes | 150 |
| SPECIALFLAGS | Tiberium Explosive | no | 151 |
| SPECIALFLAGS | Destroyable Bridges | yes | 152 |
| SPECIALFLAGS | MCV Deploy | no | 153 |
| SPECIALFLAGS | Initial Veteran | no | 154 |
| SPECIALFLAGS | Fixed Alliance | no | 155 |
| SPECIALFLAGS | Harvester Immune | no | 156 |
| SPECIALFLAGS | Fog Of War | no | 157 |
| SPECIALFLAGS | Inert | no | 158 |
| SPECIALFLAGS | Ion Storms | no | 159 |
| SPECIALFLAGS | Meteorites | no | 160 |
| SPECIALFLAGS | Visceroids | no | 161 |
| COUNTRIES (COUNTRIES) | 0 | Player | 164 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 165 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 166 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 167 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 168 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 169 |
| COUNTRIES (COUNTRIES) | 6 | Civilian3 | 170 |
| COUNTRIES (COUNTRIES) | 7 | Balabos | 171 |
| COUNTRIES (COUNTRIES) | 8 | Civilian2 | 172 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Niihau Invaders 1,0 | 302 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Niihau Invaders 2,0 | 303 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Niihau Invaders 3,0 | 304 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Niihau Invaders MCV,0 | 305 |
