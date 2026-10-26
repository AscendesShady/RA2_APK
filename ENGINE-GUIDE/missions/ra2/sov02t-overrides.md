# Operation: Hostile Shore - mission overrides and local definitions

[Trigger ledger](sov02t.md) | [Team plans](sov02t-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov02t.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Civilian (CIV1) | Insignificant-object flag | no | 2 |
| Civilian (CIV1) | Threat contribution | 15 | 3 |
| Civilian (CIV2) | Insignificant-object flag | no | 6 |
| Civilian (CIV2) | Threat contribution | 15 | 7 |
| Civilian (CIV3) | Insignificant-object flag | no | 10 |
| Civilian (CIV3) | Threat contribution | 15 | 11 |
| Civilian (CIVBFM) | Insignificant-object flag | no | 14 |
| Civilian (CIVBFM) | Threat contribution | 15 | 15 |
| Civilian (CIVBF) | Insignificant-object flag | no | 18 |
| Civilian (CIVBF) | Threat contribution | 15 | 19 |
| Civilian (CIVBTM) | Insignificant-object flag | no | 22 |
| Civilian (CIVBTM) | Threat contribution | 15 | 23 |
| IFV (FV) | Technology level | -1 | 26 |
| War Miner (HARV) | Resource cargo capacity | 20 | 29 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 32 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 35 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 36 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 37 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 38 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 41 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 44 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 47 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 50 |
| Soviet Shipyard (NAYARD) | Starting health capacity | 1200 | 53 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 1000,750,500 | 56 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | AI Hate Delays | 2000,1500,1000 | 57 |
| Hotel (CAMIAM02) | Armor class | Wood | 60 |
| Hotel (CAMIAM03) | Armor class | Wood | 63 |
| Hotel (CAMIAM01) | Armor class | Wood | 66 |
| Hut (CAMSC07) | UI Name | Name:CABANA | 69 |
| Hut (CAMSC08) | UI Name | Name:CABANA | 72 |
| Hotel (CAMIAM05) | Armor class | Wood | 78 |
| Hotel (CAMIAM06) | Armor class | Wood | 81 |
| Hotel (CAMIAM07) | Armor class | Wood | 84 |
| DREDLAUNCHER (DREDLAUNCHER) | Range | 35 | 87 |
| DMISLWH (DMISLWH) | Verses | 100%,90%,80%,100%,90%,80%,10%,65%,10%,80%,0% | 90 |
| Building (CAPARS10) | UI Name | Name:CANWY09 | 93 |
| Building (CAPARS13) | UI Name | Name:CANWY09 | 96 |
| Building (CAPARS14) | UI Name | Name:CANWY09 | 99 |
| Flak Trooper (FLAKT) | Technology level | -1 | 111 |
| Air Force Command Headquarters (GAAIRC) | Technology level | -1 | 114 |
| Air Force Command Headquarters (AMRADR) | Technology level | -1 | 117 |
| Rocketeer (JUMPJET) | Technology level | -1 | 120 |
| V3 Launcher (V3) | Technology level | -1 | 123 |
| Radar Tower (NARADR) | Signed power contribution | 1 | 126 |
| Radar Tower (NARADR) | Technology level | 4 | 127 |
| Radar Tower (NARADR) | Insignificant-object flag | yes | 128 |
| Radar Tower (NARADR) | Hidden from radar | yes | 129 |
| Allied Ore Refinery (GAREFN) | Signed power contribution | 0 | 132 |
| Destroyer (DEST) | Technology level | 3 | 135 |
| Communications Center (CATECH01) | Name | Command Center | 138 |
| Communications Center (CATECH01) | Technology level | -1 | 139 |
| Communications Center (CATECH01) | Starting health capacity | 400 | 140 |
| Communications Center (CATECH01) | Insignificant-object flag | no | 141 |
| Communications Center (CATECH01) | Nominal | yes | 142 |
| Communications Center (CATECH01) | Hidden from radar | no | 143 |
| Communications Center (CATECH01) | Infantry garrison permitted | no | 144 |
| INVISIBLELOW (INVISIBLELOW) | Subject To Walls | no | 147 |
| Grand Cannon (GTGCAN) | Starting health capacity | 200 | 150 |
| Grand Cannon (GTGCAN) | Signed power contribution | 0 | 151 |
| Grand Cannon (GTGCAN) | Depends on power | no | 152 |
| CANNON (CANNON) | Image | 120MM | 155 |
| CANNON (CANNON) | Arcing | true | 156 |
| CANNON (CANNON) | Subject To Cliffs | no | 157 |
| CANNON (CANNON) | Subject To Elevation | yes | 158 |
| CANNON (CANNON) | Subject To Walls | no | 159 |
| Sandbags (GASAND) | Name | Sandbags | 162 |
| Sandbags (GASAND) | Construction category | Combat | 163 |
| Sandbags (GASAND) | Starting health capacity | 50 | 164 |
| Sandbags (GASAND) | Armor class | wood | 165 |
| Sandbags (GASAND) | Can be crushed | yes | 166 |
| Sandbags (GASAND) | Wall behavior | yes | 167 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 2500 | 170 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 171 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.50 | 172 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.20 | 173 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.02 | 174 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 2500 | 177 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.01 | 178 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 1.0 | 179 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.005 | 180 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 1.0 | 181 |
| 155MM (155MM) | Minimum Range | 0 | 184 |
| Dreadnought (DRED) | Name | Vladimir's Command Ship | 187 |
| Dreadnought (DRED) | Starting health capacity | 10000 | 188 |
| Dreadnought (DRED) | Attacker replacement delay | 120 | 189 |
| Dreadnought (DRED) | Movement rating | 9 | 190 |
| Vladimir's Command Ship (VLAD) | Movement rating | 9 | 193 |
| Vladimir's Command Ship (VLAD) | Starting health capacity | 10000 | 194 |
| Vladimir's Command Ship (VLAD) | Attacker replacement delay | 120 | 195 |
| ASWBOMB (ASWBOMB) | Damage | 100 | 198 |
| Attack Dog (DOG) | Technology level | 1 | 201 |
| Typhoon Attack Sub (SUB) | Technology level | 3 | 204 |
| Amphibious Transport (SAPC) | Technology level | 11 | 207 |
| Amphibious Transport (SAPC) | Starting health capacity | 800 | 208 |
| SPECIALFLAGS | Tiberium Grows | yes | 211 |
| SPECIALFLAGS | Tiberium Spreads | yes | 212 |
| SPECIALFLAGS | Tiberium Explosive | no | 213 |
| SPECIALFLAGS | Destroyable Bridges | no | 214 |
| SPECIALFLAGS | MCV Deploy | no | 215 |
| SPECIALFLAGS | Initial Veteran | no | 216 |
| SPECIALFLAGS | Fixed Alliance | no | 217 |
| SPECIALFLAGS | Harvester Immune | no | 218 |
| SPECIALFLAGS | Fog Of War | no | 219 |
| SPECIALFLAGS | Inert | no | 220 |
| SPECIALFLAGS | Ion Storms | no | 221 |
| SPECIALFLAGS | Meteorites | no | 222 |
| SPECIALFLAGS | Visceroids | no | 223 |
| VARIABLENAMES (VARIABLENAMES) | 0 | MCV Landed,0 | 264 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Hotels Destroyed,0 | 265 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Transports Unloaded,0 | 266 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Vlad is Hit,0 | 267 |
| America (AMERICANS) | Country | Americans | 299 |
| America (AMERICANS) | Technology level | 10 | 300 |
| America (AMERICANS) | Credits | 500 | 301 |
| America (AMERICANS) | IQ | 5 | 302 |
| America (AMERICANS) | Edge | South | 303 |
| America (AMERICANS) | Player Control | no | 304 |
| America (AMERICANS) | Color | DarkBlue | 305 |
| America (AMERICANS) | Allies | Americans,Alliance,French,Germans,British,Arabs,GDI,Nod,Neutral,Special | 306 |
| America (AMERICANS) | Percent Built | 0 | 307 |
| America (AMERICANS) | Node Count | 0 | 308 |
| Korea (ALLIANCE) | Country | Alliance | 311 |
| Korea (ALLIANCE) | Technology level | 1 | 312 |
| Korea (ALLIANCE) | Credits | 0 | 313 |
| Korea (ALLIANCE) | IQ | 0 | 314 |
| Korea (ALLIANCE) | Edge | North | 315 |
| Korea (ALLIANCE) | Player Control | no | 316 |
| Korea (ALLIANCE) | Color | DarkBlue | 317 |
| Korea (ALLIANCE) | Allies | Americans,Alliance,French,Germans,British,Arabs,GDI | 318 |
| Korea (ALLIANCE) | Percent Built | 0 | 319 |
| Korea (ALLIANCE) | Node Count | 0 | 320 |
| France (FRENCH) | Country | French | 323 |
| France (FRENCH) | Technology level | 1 | 324 |
| France (FRENCH) | Credits | 0 | 325 |
| France (FRENCH) | IQ | 0 | 326 |
| France (FRENCH) | Edge | North | 327 |
| France (FRENCH) | Player Control | no | 328 |
| France (FRENCH) | Color | DarkBlue | 329 |
| France (FRENCH) | Allies | Americans,Alliance,French,Germans,British,Arabs,GDI,Neutral | 330 |
| France (FRENCH) | Percent Built | 0 | 331 |
| France (FRENCH) | Node Count | 0 | 332 |
| Germany (GERMANS) | Country | Germans | 335 |
| Germany (GERMANS) | Technology level | 1 | 336 |
| Germany (GERMANS) | Credits | 0 | 337 |
| Germany (GERMANS) | IQ | 0 | 338 |
| Germany (GERMANS) | Edge | North | 339 |
| Germany (GERMANS) | Player Control | no | 340 |
| Germany (GERMANS) | Color | DarkBlue | 341 |
| Germany (GERMANS) | Allies | Americans,Alliance,French,Germans,British,Arabs,GDI,Neutral | 342 |
| Germany (GERMANS) | Percent Built | 0 | 343 |
| Germany (GERMANS) | Node Count | 0 | 344 |
| Great Britain (BRITISH) | Country | British | 347 |
| Great Britain (BRITISH) | Technology level | 1 | 348 |
| Great Britain (BRITISH) | Credits | 500 | 349 |
| Great Britain (BRITISH) | IQ | 0 | 350 |
| Great Britain (BRITISH) | Edge | North | 351 |
| Great Britain (BRITISH) | Player Control | no | 352 |
| Great Britain (BRITISH) | Color | DarkGreen | 353 |
| Great Britain (BRITISH) | Allies | Americans,Alliance,French,Germans,British,Arabs,GDI,Neutral | 354 |
| Great Britain (BRITISH) | Percent Built | 0 | 355 |
| Great Britain (BRITISH) | Node Count | 0 | 356 |
| Libya (AFRICANS) | Country | Africans | 359 |
| Libya (AFRICANS) | Technology level | 1 | 360 |
| Libya (AFRICANS) | Credits | 10 | 361 |
| Libya (AFRICANS) | IQ | 0 | 362 |
| Libya (AFRICANS) | Edge | North | 363 |
| Libya (AFRICANS) | Player Control | no | 364 |
| Libya (AFRICANS) | Color | DarkRed | 365 |
| Libya (AFRICANS) | Allies | Americans,Africans,Russians | 366 |
| Libya (AFRICANS) | Percent Built | 0 | 367 |
| Libya (AFRICANS) | Node Count | 0 | 368 |
| Iraq (ARABS) | Country | Arabs | 371 |
| Iraq (ARABS) | Technology level | 1 | 372 |
| Iraq (ARABS) | Credits | 0 | 373 |
| Iraq (ARABS) | IQ | 0 | 374 |
| Iraq (ARABS) | Edge | North | 375 |
| Iraq (ARABS) | Player Control | no | 376 |
| Iraq (ARABS) | Color | DarkGreen | 377 |
| Iraq (ARABS) | Allies | Americans,Alliance,French,Germans,British,Arabs,GDI | 378 |
| Iraq (ARABS) | Percent Built | 0 | 379 |
| Iraq (ARABS) | Node Count | 0 | 380 |
| Cuba (CONFEDERATION) | Country | Confederation | 383 |
| Cuba (CONFEDERATION) | Technology level | 3 | 384 |
| Cuba (CONFEDERATION) | Credits | 50 | 385 |
| Cuba (CONFEDERATION) | IQ | 0 | 386 |
| Cuba (CONFEDERATION) | Edge | East | 387 |
| Cuba (CONFEDERATION) | Player Control | yes | 388 |
| Cuba (CONFEDERATION) | Color | DarkRed | 389 |
| Cuba (CONFEDERATION) | Allies | Africans,Confederation,Russians,Special | 390 |
| Cuba (CONFEDERATION) | Percent Built | 0 | 391 |
| Cuba (CONFEDERATION) | Node Count | 0 | 392 |
| Russia (RUSSIANS) | Country | Russians | 395 |
| Russia (RUSSIANS) | Technology level | 1 | 396 |
| Russia (RUSSIANS) | Credits | 0 | 397 |
| Russia (RUSSIANS) | IQ | 0 | 398 |
| Russia (RUSSIANS) | Edge | North | 399 |
| Russia (RUSSIANS) | Player Control | no | 400 |
| Russia (RUSSIANS) | Color | NeonBlue | 401 |
| Russia (RUSSIANS) | Allies | Africans,Confederation,Russians | 402 |
| Russia (RUSSIANS) | Percent Built | 0 | 403 |
| Russia (RUSSIANS) | Node Count | 0 | 404 |
| GDI (GDI) | Country | GDI | 407 |
| GDI (GDI) | Technology level | 1 | 408 |
| GDI (GDI) | Credits | 0 | 409 |
| GDI (GDI) | IQ | 0 | 410 |
| GDI (GDI) | Edge | North | 411 |
| GDI (GDI) | Player Control | no | 412 |
| GDI (GDI) | Color | DarkGreen | 413 |
| GDI (GDI) | Allies | Americans,Alliance,French,Germans,British,Arabs,GDI,Neutral | 414 |
| GDI (GDI) | Percent Built | 0 | 415 |
| GDI (GDI) | Node Count | 0 | 416 |
| Nod (NOD) | Country | Nod | 419 |
| Nod (NOD) | Technology level | 1 | 420 |
| Nod (NOD) | Credits | 0 | 421 |
| Nod (NOD) | IQ | 0 | 422 |
| Nod (NOD) | Edge | North | 423 |
| Nod (NOD) | Player Control | no | 424 |
| Nod (NOD) | Color | Grey | 425 |
| Nod (NOD) | Allies | Americans,Nod,Neutral | 426 |
| Nod (NOD) | Percent Built | 0 | 427 |
| Nod (NOD) | Node Count | 0 | 428 |
| Civilian (NEUTRAL) | Country | Neutral | 431 |
| Civilian (NEUTRAL) | Technology level | 1 | 432 |
| Civilian (NEUTRAL) | Credits | 0 | 433 |
| Civilian (NEUTRAL) | IQ | 0 | 434 |
| Civilian (NEUTRAL) | Edge | North | 435 |
| Civilian (NEUTRAL) | Player Control | no | 436 |
| Civilian (NEUTRAL) | Color | Grey | 437 |
| Civilian (NEUTRAL) | Allies | Neutral | 438 |
| Civilian (NEUTRAL) | Percent Built | 0 | 439 |
| Civilian (NEUTRAL) | Node Count | 0 | 440 |
| JP (SPECIAL) | Country | Special | 443 |
| JP (SPECIAL) | Technology level | 1 | 444 |
| JP (SPECIAL) | Credits | 0 | 445 |
| JP (SPECIAL) | IQ | 0 | 446 |
| JP (SPECIAL) | Edge | North | 447 |
| JP (SPECIAL) | Player Control | no | 448 |
| JP (SPECIAL) | Color | Grey | 449 |
| JP (SPECIAL) | Allies | Special | 450 |
| JP (SPECIAL) | Percent Built | 0 | 451 |
| JP (SPECIAL) | Node Count | 0 | 452 |
