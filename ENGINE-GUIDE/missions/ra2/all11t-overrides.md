# Operation: Fallout - mission overrides and local definitions

[Trigger ledger](all11t.md) | [Team plans](all11t-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS01.MIX/all11t.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Wall behavior | Yes | 11 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | AI Safe Distance | 12 | 14 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Total AI Team Cap | 30,30,30 | 15 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Spy Money Steal Percent | .05 | 16 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Default Mirage Disguises | TREE20,TREE21,TREE22,TREE23 | 17 |
| War Miner (HARV) | Resource cargo capacity | 20 | 20 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 23 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 26 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 27 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 28 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 29 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 32 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 35 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 38 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 41 |
| Gap Generator (GAGAP) | Name | Gap Generator | 44 |
| Gap Generator (GAGAP) | Technology level | 12 | 45 |
| V3 Launcher (V3) | Default To Guard Area | yes | 48 |
| Tesla Trooper (SHK) | Default To Guard Area | yes | 51 |
| Apocalypse (APOC) | Default To Guard Area | yes | 54 |
| Flak Track (HTK) | Default To Guard Area | yes | 57 |
| Flak Trooper (FLAKT) | Default To Guard Area | yes | 60 |
| Conscript (E2) | Default To Guard Area | yes | 63 |
| Rhino Heavy Tank (HTNK) | Default To Guard Area | yes | 66 |
| Allied War Factory (GAWEAP) | Name | Allied War Factory | 69 |
| Allied War Factory (GAWEAP) | Armor class | concrete | 70 |
| Nuclear Missile (MULTISPECIAL) | Name | N U K E !!! | 73 |
| Nuclear Missile (MULTISPECIAL) | Recharge Time | 20 | 74 |
| Nuclear Missile (MULTISPECIAL) | Show Timer | yes | 75 |
| Chronosphere (CHRONOSPHERESPECIAL) | Name | Chrono Sphere | 78 |
| Chronosphere (CHRONOSPHERESPECIAL) | Recharge Time | 5 | 79 |
| Cruise Ship (CRUISE) | Name | RA2 Cruise Ship | 82 |
| Cruise Ship (CRUISE) | Crate Goodie | no | 83 |
| Cruise Ship (CRUISE) | Permitted country list | Russians,Confederation,Africans,Arabs,British,French,Germans,Americans,Alliance | 84 |
| Cruise Ship (CRUISE) | Insignificant-object flag | no | 85 |
| Cruise Ship (CRUISE) | Starting health capacity | 600 | 86 |
| Police Car (COP) | Ambient Sound | Dummy | 89 |
| Chrono Legionnaire (CLEG) | Name | Chrono Legionnaire | 92 |
| Chrono Legionnaire (CLEG) | Technology level | 12 | 93 |
| Tanya (TANY) | Name | Tanya | 96 |
| Tanya (TANY) | Technology level | 12 | 97 |
| Yuri (YURI) | Name | Yuri | 100 |
| Yuri (YURI) | Technology level | 12 | 101 |
| Kirov Airship (ZEP) | Name | Kirov Airship | 104 |
| Kirov Airship (ZEP) | Technology level | 12 | 105 |
| Iron Curtain Device (NAIRON) | Name | Iron Curtain Device | 108 |
| Iron Curtain Device (NAIRON) | Technology level | 12 | 109 |
| Weather Controller (GAWEAT) | Name | Weather Controller | 112 |
| Weather Controller (GAWEAT) | Technology level | 12 | 113 |
| Chrono Sphere (GACSPH) | Name | Chrono Sphere | 116 |
| Chrono Sphere (GACSPH) | Charged Anim Time | 1 | 117 |
| Chrono Sphere (GACSPH) | Armor class | concrete | 118 |
| Engineer (SENGINEER) | Technology level | -1 | 121 |
| SEAL (GHOST) | Technology level | 9 | 124 |
| Attack Dog (DOG) | Technology level | -1 | 127 |
| Negative Light Post (NEGLAMP) | Name | Negative Light Post | 130 |
| Negative Light Post (NEGLAMP) | Image | GALITE | 131 |
| Negative Light Post (NEGLAMP) | Local light reach | 5000 | 132 |
| Negative Light Post (NEGLAMP) | Local light intensity | -0.30 | 133 |
| Negative Light Post (NEGLAMP) | Light Red Tint | 0.03 | 134 |
| Negative Light Post (NEGLAMP) | Light Green Tint | 0.04 | 135 |
| Negative Light Post (NEGLAMP) | Light Blue Tint | 0.04 | 136 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 2500 | 139 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 140 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.25 | 141 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.10 | 142 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.01 | 143 |
| SPECIALFLAGS | Tiberium Grows | yes | 146 |
| SPECIALFLAGS | Tiberium Spreads | yes | 147 |
| SPECIALFLAGS | Tiberium Explosive | no | 148 |
| SPECIALFLAGS | Destroyable Bridges | yes | 149 |
| SPECIALFLAGS | MCV Deploy | no | 150 |
| SPECIALFLAGS | Initial Veteran | no | 151 |
| SPECIALFLAGS | Fixed Alliance | no | 152 |
| SPECIALFLAGS | Harvester Immune | no | 153 |
| SPECIALFLAGS | Fog Of War | no | 154 |
| SPECIALFLAGS | Inert | no | 155 |
| SPECIALFLAGS | Ion Storms | no | 156 |
| SPECIALFLAGS | Meteorites | no | 157 |
| SPECIALFLAGS | Visceroids | no | 158 |
| COUNTRIES (COUNTRIES) | 0 | Player | 161 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 162 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 163 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 164 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 165 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 166 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 167 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 168 |
| COUNTRIES (COUNTRIES) | 8 | Elania | 169 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Chronosphere Built,0 | 297 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Team Landed,0 | 298 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Team 2 Landed,0 | 299 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Anti-Oil Landed,0 | 300 |
| VARIABLENAMES (VARIABLENAMES) | 4 | Oil Captured,0 | 301 |
| VARIABLENAMES (VARIABLENAMES) | 5 | Team 3 Landed,0 | 302 |
| VARIABLENAMES (VARIABLENAMES) | 6 | Team 2b Landed,0 | 303 |
| VARIABLENAMES (VARIABLENAMES) | 7 | Team 3b Landed,0 | 304 |
| VARIABLENAMES (VARIABLENAMES) | 8 | Team 3c Landed,0 | 305 |
| VARIABLENAMES (VARIABLENAMES) | 9 | Anti-Oil 2 Landed,0 | 306 |
| VARIABLENAMES (VARIABLENAMES) | 10 | Para 1 Landed,0 | 307 |
| VARIABLENAMES (VARIABLENAMES) | 11 | Recur Invader 1a La,0 | 308 |
| VARIABLENAMES (VARIABLENAMES) | 12 | Nuke Ready,0 | 309 |
| VARIABLENAMES (VARIABLENAMES) | 13 | Got Gap,0 | 310 |
| VARIABLENAMES (VARIABLENAMES) | 14 | Nuke2 Ready,0 | 311 |
| VARIABLENAMES (VARIABLENAMES) | 15 | Civ Boat offscreen,0 | 312 |
| VARIABLENAMES (VARIABLENAMES) | 16 | Recur 2a landed,0 | 313 |
| VARIABLENAMES (VARIABLENAMES) | 17 | Recur 2b landed,0 | 314 |
| VARIABLENAMES (VARIABLENAMES) | 18 | Low Power,0 | 315 |
| VARIABLENAMES (VARIABLENAMES) | 19 | Mainland Bridge,0 | 316 |
| VARIABLENAMES (VARIABLENAMES) | 20 | Base Island Bridge,0 | 317 |
| VARIABLENAMES (VARIABLENAMES) | 21 | 1 CO Landed,0 | 318 |
| VARIABLENAMES (VARIABLENAMES) | 22 | 2 CO Landed,0 | 319 |
| VARIABLENAMES (VARIABLENAMES) | 23 | 3 CO Landed,0 | 320 |
| VARIABLENAMES (VARIABLENAMES) | 24 | 4 CO Landed,0 | 321 |
| VARIABLENAMES (VARIABLENAMES) | 25 | 5 CO Landed,0 | 322 |
| VARIABLENAMES (VARIABLENAMES) | 26 | 6 CO Landed,0 | 323 |
| VARIABLENAMES (VARIABLENAMES) | 27 | 1 CN Landed,0 | 324 |
| VARIABLENAMES (VARIABLENAMES) | 28 | 2 CN Landed,0 | 325 |
| VARIABLENAMES (VARIABLENAMES) | 29 | 3 CN Landed,0 | 326 |
| VARIABLENAMES (VARIABLENAMES) | 30 | 4 CN Landed,0 | 327 |
| VARIABLENAMES (VARIABLENAMES) | 31 | 5 CN Landed,0 | 328 |
| VARIABLENAMES (VARIABLENAMES) | 32 | 6 CN Landed,0 | 329 |
| VARIABLENAMES (VARIABLENAMES) | 33 | Chronosphere Up,0 | 330 |
| VARIABLENAMES (VARIABLENAMES) | 34 | Nuke Win Go,0 | 331 |
| VARIABLENAMES (VARIABLENAMES) | 35 | Dead Squid,0 | 332 |
