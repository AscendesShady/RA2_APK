# Operation: Clones Down Under - mission overrides and local definitions

[Trigger ledger](all05umd.md) | [Team plans](all05umd-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: mapsmd03.mix/all05umd.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | AI Safe Distance | 20 | 2 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Spy Money Steal Percent | .05 | 3 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 3000 | 4 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -2000 | 5 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Total AI Team Cap | 40,40,40 | 6 |
| Rhino Heavy Tank (HTNK) | Production-time multiplier | 1.0 | 9 |
| Grizzly Battle Tank (MTNK) | Production-time multiplier | 1.0 | 12 |
| Lasher Light Tank (LTNK) | Technology level | 11 | 15 |
| Lasher Light Tank (LTNK) | Production-time multiplier | 1.0 | 16 |
| Gattling Tank (YTNK) | Production-time multiplier | 1.0 | 19 |
| Chaos Drone (CAOS) | Production-time multiplier | 1.0 | 22 |
| IFV (FV) | Production-time multiplier | 1.0 | 25 |
| Mirage Tank (MGTK) | Production-time multiplier | 1.0 | 28 |
| Prism Tank (SREF) | Production-time multiplier | 1.0 | 31 |
| Tanya (TANY) | Technology level | 11 | 34 |
| Psychic Dominator (YAPPET) | Name | Yuri Puppet Master | 37 |
| Psychic Dominator (YAPPET) | Technology level | 11 | 38 |
| Weather Controller (GAWEAT) | Name | Allied Weather Controller | 41 |
| Weather Controller (GAWEAT) | Technology level | 11 | 42 |
| Genetic Mutator (YAGNTC) | Name | Yuri Genetic Mutator Device | 45 |
| Genetic Mutator (YAGNTC) | Technology level | 11 | 46 |
| Floating Disc (DISK) | Name | Floating Disk | 49 |
| Floating Disc (DISK) | Technology level | 11 | 50 |
| Master Mind (MIND) | Name | Master Mind | 53 |
| Master Mind (MIND) | Technology level | 11 | 54 |
| Yuri Prime (YURIPR) | Technology level | 11 | 57 |
| Yuri MCV (PCV) | Name | Yuri Construction Vehicle | 60 |
| Yuri MCV (PCV) | Technology level | 11 | 61 |
| Engineer (SENGINEER) | Required countries | Russians | 64 |
| Engineer (YENGINEER) | Required countries | BadGuy1,BadGuy2,BadGuy3 | 67 |
| Attack Dog (DOG) | Name | Attack Dog | 70 |
| Attack Dog (DOG) | Required countries | Russians | 71 |
| Black Eagle (BEAG) | Technology level | 11 | 74 |
| Black Eagle (BEAG) | Required countries | Player | 75 |
| COUNTRIES (COUNTRIES) | 0 | Einstein | 78 |
| COUNTRIES (COUNTRIES) | 1 | Player | 79 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy1 | 80 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy2 | 81 |
| COUNTRIES (COUNTRIES) | 4 | BadGuy3 | 82 |
| COUNTRIES (COUNTRIES) | 5 | Germany1 | 83 |
| COUNTRIES (COUNTRIES) | 6 | Germany2 | 84 |
| COUNTRIES (COUNTRIES) | 7 | Germany3 | 85 |
| COUNTRIES (COUNTRIES) | 8 | Temp | 86 |
| SPECIALFLAGS | Tiberium Grows | yes | 192 |
| SPECIALFLAGS | Tiberium Spreads | yes | 193 |
| SPECIALFLAGS | Tiberium Explosive | no | 194 |
| SPECIALFLAGS | Destroyable Bridges | yes | 195 |
| SPECIALFLAGS | MCV Deploy | no | 196 |
| SPECIALFLAGS | Initial Veteran | no | 197 |
| SPECIALFLAGS | Fixed Alliance | no | 198 |
| SPECIALFLAGS | Harvester Immune | no | 199 |
| SPECIALFLAGS | Fog Of War | no | 200 |
| SPECIALFLAGS | Inert | no | 201 |
| SPECIALFLAGS | Ion Storms | no | 202 |
| SPECIALFLAGS | Meteorites | no | 203 |
| SPECIALFLAGS | Visceroids | no | 204 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Black Eagle 1,0 | 253 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Black Eagle 2,0 | 254 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Black Eagle 3,0 | 255 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Garrison Time,0 | 256 |
| VARIABLENAMES (VARIABLENAMES) | 4 | Building 1 Fallen,0 | 257 |
| VARIABLENAMES (VARIABLENAMES) | 5 | Building 2 Fallen,0 | 258 |
| VARIABLENAMES (VARIABLENAMES) | 6 | Building 3 Fallen,0 | 259 |
| VARIABLENAMES (VARIABLENAMES) | 7 | Building 4 Fallen,0 | 260 |
| VARIABLENAMES (VARIABLENAMES) | 8 | Building 5 Fallen,0 | 261 |
| VARIABLENAMES (VARIABLENAMES) | 9 | Building 6 Fallen,0 | 262 |
| VARIABLENAMES (VARIABLENAMES) | 10 | Building 7 Fallen,0 | 263 |
| VARIABLENAMES (VARIABLENAMES) | 11 | Building 8 Fallen,0 | 264 |
| VARIABLENAMES (VARIABLENAMES) | 12 | BadGuy1 Dead,0 | 265 |
| VARIABLENAMES (VARIABLENAMES) | 13 | BadGuy2 Dead,0 | 266 |
| VARIABLENAMES (VARIABLENAMES) | 14 | Virus Dropped Off,0 | 267 |
| VARIABLENAMES (VARIABLENAMES) | 15 | Boomers There?,0 | 268 |
| VARIABLENAMES (VARIABLENAMES) | 16 | Chaos Revealed?,0 | 269 |
| VARIABLENAMES (VARIABLENAMES) | 17 | Obj 1 Complete,0 | 270 |
