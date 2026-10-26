# Operation: Eagle Dawn - mission overrides and local definitions

[Trigger ledger](all02s.md) | [Team plans](all02s-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS01.MIX/all02s.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| War Miner (HARV) | Resource cargo capacity | 20 | 2 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 5 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 8 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 9 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 10 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 11 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 14 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 17 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 20 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 23 |
| FLAKWEAPON (FLAKWEAPON) | Damage | 20 | 26 |
| FLAKWEAPON (FLAKWEAPON) | Range | 9 | 27 |
| FLAKWH (FLAKWH) | Cell Spread | 1.0 | 30 |
| FLAKWH (FLAKWH) | Percent At Max | .2 | 31 |
| FLAKWH (FLAKWH) | Verses | 125%,80%,50%,100%,100%,20%,0%,0%,0%,100%,100% | 32 |
| FLAKWH (FLAKWH) | Anim List | SMKPUFF | 33 |
| FLAKWH (FLAKWH) | Inf Death | 3 | 34 |
| COUNTRIES (COUNTRIES) | 0 | Americans | 46 |
| COUNTRIES (COUNTRIES) | 1 | Alliance | 47 |
| COUNTRIES (COUNTRIES) | 2 | French | 48 |
| COUNTRIES (COUNTRIES) | 3 | Germans | 49 |
| COUNTRIES (COUNTRIES) | 4 | British | 50 |
| COUNTRIES (COUNTRIES) | 5 | Africans | 51 |
| COUNTRIES (COUNTRIES) | 6 | Arabs | 52 |
| COUNTRIES (COUNTRIES) | 7 | Confederation | 53 |
| COUNTRIES (COUNTRIES) | 8 | Russians | 54 |
| COUNTRIES (COUNTRIES) | 9 | GDI | 55 |
| COUNTRIES (COUNTRIES) | 10 | Nod | 56 |
| COUNTRIES (COUNTRIES) | 12 | NeutralA | 57 |
| COUNTRIES (COUNTRIES) | 13 | Neutral | 58 |
| COUNTRIES (COUNTRIES) | 14 | Special | 59 |
| Great Britain (BRITISH) | UI Name | Name:British | 72 |
| Great Britain (BRITISH) | Name | Great Britain | 73 |
| Great Britain (BRITISH) | Suffix | Allied | 74 |
| Great Britain (BRITISH) | Prefix | G | 75 |
| Great Britain (BRITISH) | Color | Gold | 76 |
| Great Britain (BRITISH) | Multiplay Passive | true | 77 |
| Great Britain (BRITISH) | Side | GDI | 78 |
| Great Britain (BRITISH) | Smart AI | yes | 79 |
| Harrier (ORCA) | Technology level | -1 | 82 |
| BARRELEXPLOSION (BARRELEXPLOSION) | Projectile | Invisible | 85 |
| BARRELEXPLOSION (BARRELEXPLOSION) | Damage | 200 | 86 |
| BARRELEXPLOSION (BARRELEXPLOSION) | Warhead | OilExplosionWH | 87 |
| BARRELEXPLOSION (BARRELEXPLOSION) | Anim | RING1 | 88 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Verses | 150%,100%,100%,90%,70%,50%,200%,90%,50%,100%,100% | 91 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Sparky | no | 92 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Fire | yes | 93 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Inf Death | 4 | 94 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Cell Spread | 2 | 95 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Percent At Max | .25 | 96 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Wall Absolute Destroyer | Yes | 97 |
| Air Force Command Headquarters (AMRADR) | Technology level | -1 | 100 |
| V3 Launcher (V3) | Technology level | -1 | 103 |
| Radar Tower (NARADR) | Technology level | -1 | 106 |
| Tanya (TANY) | Sight radius setting | 10 | 109 |
| Air Force Command Headquarters (GAAIRC) | Technology level | -1 | 112 |
| Attack Dog (DOG) | Double Owned | No | 115 |
| Attack Dog (DOG) | Permitted country list | Russians | 116 |
| Attack Dog (DOG) | Excluded countries | Americans,Confederation | 117 |
| IFV (FV) | Technology level | -1 | 120 |
| Air Force Academy Chapel (CACOLO01) | Name | RA2 Air Force Academy Chapel Colorado | 123 |
| Air Force Academy Chapel (CACOLO01) | UI Name | Name:CACOLO01 | 124 |
| Air Force Academy Chapel (CACOLO01) | Technology level | -1 | 125 |
| Air Force Academy Chapel (CACOLO01) | Starting health capacity | 1000 | 126 |
| Air Force Academy Chapel (CACOLO01) | Insignificant-object flag | yes | 127 |
| Air Force Academy Chapel (CACOLO01) | Nominal | yes | 128 |
| Air Force Academy Chapel (CACOLO01) | Hidden from radar | no | 129 |
| Air Force Academy Chapel (CACOLO01) | Points | 5 | 130 |
| Air Force Academy Chapel (CACOLO01) | Armor class | concrete | 131 |
| Air Force Academy Chapel (CACOLO01) | Normal base-adjacency role | no | 132 |
| Air Force Academy Chapel (CACOLO01) | Sight radius setting | 6 | 133 |
| Air Force Academy Chapel (CACOLO01) | Repair-tool permission | yes | 134 |
| Air Force Academy Chapel (CACOLO01) | Infantry garrison permitted | no | 135 |
| Air Force Academy Chapel (CACOLO01) | Garrison capacity | 0 | 136 |
| Air Force Academy Chapel (CACOLO01) | Distributed Fire | no | 137 |
| Air Force Academy Chapel (CACOLO01) | Engineer-capture permission | true | 138 |
| Air Force Academy Chapel (CACOLO01) | Crate Beneath | false | 139 |
| Air Force Academy Chapel (CACOLO01) | Crate Beneath Is Money | false | 140 |
| Rocketeer (JUMPJET) | Required structures/groups | GAPILE,CACOLO01 | 143 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 4000 | 146 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 147 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.40 | 148 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.40 | 149 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.15 | 150 |
| Invisible Light Post (INGALITE) | Local light reach | 5000 | 153 |
| Invisible Light Post (INGALITE) | Local light intensity | 0.2 | 154 |
| Invisible Light Post (INGALITE) | Light Red Tint | 0.05 | 155 |
| Invisible Light Post (INGALITE) | Light Green Tint | 0.05 | 156 |
| Invisible Light Post (INGALITE) | Light Blue Tint | 0.03 | 157 |
| Soviet Shipyard (NAYARD) | Technology level | -1 | 163 |
| SPECIALFLAGS | Tiberium Grows | yes | 166 |
| SPECIALFLAGS | Tiberium Spreads | yes | 167 |
| SPECIALFLAGS | Tiberium Explosive | no | 168 |
| SPECIALFLAGS | Destroyable Bridges | no | 169 |
| SPECIALFLAGS | MCV Deploy | no | 170 |
| SPECIALFLAGS | Initial Veteran | no | 171 |
| SPECIALFLAGS | Fixed Alliance | no | 172 |
| SPECIALFLAGS | Harvester Immune | no | 173 |
| SPECIALFLAGS | Fog Of War | no | 174 |
| SPECIALFLAGS | Inert | no | 175 |
| SPECIALFLAGS | Ion Storms | no | 176 |
| SPECIALFLAGS | Meteorites | no | 177 |
| SPECIALFLAGS | Visceroids | no | 178 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Flak Cannons Spotte,0 | 219 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Intruders Scout Don,0 | 220 |
| America (AMERICANS) | Country | Americans | 253 |
| America (AMERICANS) | Technology level | 3 | 254 |
| America (AMERICANS) | Credits | 100 | 255 |
| America (AMERICANS) | IQ | 0 | 256 |
| America (AMERICANS) | Edge | West | 257 |
| America (AMERICANS) | Player Control | yes | 258 |
| America (AMERICANS) | Color | DarkBlue | 259 |
| America (AMERICANS) | Allies | Americans,Alliance,French,Germans,GDI,Neutral | 260 |
| America (AMERICANS) | Percent Built | 0 | 261 |
| America (AMERICANS) | Node Count | 0 | 262 |
| Korea (ALLIANCE) | Country | Alliance | 265 |
| Korea (ALLIANCE) | Technology level | 1 | 266 |
| Korea (ALLIANCE) | Credits | 0 | 267 |
| Korea (ALLIANCE) | IQ | 0 | 268 |
| Korea (ALLIANCE) | Edge | East | 269 |
| Korea (ALLIANCE) | Player Control | yes | 270 |
| Korea (ALLIANCE) | Color | DarkBlue | 271 |
| Korea (ALLIANCE) | Allies | Americans,Alliance,French,Germans,Brits,GDI,Neutral | 272 |
| Korea (ALLIANCE) | Percent Built | 0 | 273 |
| Korea (ALLIANCE) | Node Count | 0 | 274 |
| France (FRENCH) | Country | French | 277 |
| France (FRENCH) | Technology level | 1 | 278 |
| France (FRENCH) | Credits | 0 | 279 |
| France (FRENCH) | IQ | 0 | 280 |
| France (FRENCH) | Edge | North | 281 |
| France (FRENCH) | Player Control | no | 282 |
| France (FRENCH) | Color | DarkBlue | 283 |
| France (FRENCH) | Allies | Americans,French,Germans,Africans,Arabs,Confederation,Russians,GDI,Neutral | 284 |
| France (FRENCH) | Percent Built | 0 | 285 |
| France (FRENCH) | Node Count | 0 | 286 |
| Germany (GERMANS) | Country | Germans | 289 |
| Germany (GERMANS) | Technology level | 1 | 290 |
| Germany (GERMANS) | Credits | 0 | 291 |
| Germany (GERMANS) | IQ | 0 | 292 |
| Germany (GERMANS) | Edge | North | 293 |
| Germany (GERMANS) | Player Control | yes | 294 |
| Germany (GERMANS) | Color | DarkBlue | 295 |
| Germany (GERMANS) | Allies | Americans,Alliance,French,Germans,Brits,GDI,Neutral,Neutral2 | 296 |
| Germany (GERMANS) | Percent Built | 0 | 297 |
| Germany (GERMANS) | Node Count | 0 | 298 |
| Libya (AFRICANS) | Country | Africans | 313 |
| Libya (AFRICANS) | Technology level | 1 | 314 |
| Libya (AFRICANS) | Credits | 0 | 315 |
| Libya (AFRICANS) | IQ | 0 | 316 |
| Libya (AFRICANS) | Edge | North | 317 |
| Libya (AFRICANS) | Player Control | no | 318 |
| Libya (AFRICANS) | Color | DarkRed | 319 |
| Libya (AFRICANS) | Allies | French,Brits,Africans,Arabs,Confederation,Russians,Nod,Neutral,Neutral2 | 320 |
| Libya (AFRICANS) | Percent Built | 0 | 321 |
| Libya (AFRICANS) | Node Count | 0 | 322 |
| Iraq (ARABS) | Country | Arabs | 325 |
| Iraq (ARABS) | Technology level | 1 | 326 |
| Iraq (ARABS) | Credits | 0 | 327 |
| Iraq (ARABS) | IQ | 0 | 328 |
| Iraq (ARABS) | Edge | North | 329 |
| Iraq (ARABS) | Player Control | no | 330 |
| Iraq (ARABS) | Color | DarkRed | 331 |
| Iraq (ARABS) | Allies | French,Brits,Africans,Arabs,Confederation,Russians,Nod,Neutral,Neutral2 | 332 |
| Iraq (ARABS) | Percent Built | 0 | 333 |
| Iraq (ARABS) | Node Count | 0 | 334 |
| Cuba (CONFEDERATION) | Country | Confederation | 337 |
| Cuba (CONFEDERATION) | Technology level | 1 | 338 |
| Cuba (CONFEDERATION) | Credits | 0 | 339 |
| Cuba (CONFEDERATION) | IQ | 0 | 340 |
| Cuba (CONFEDERATION) | Edge | North | 341 |
| Cuba (CONFEDERATION) | Player Control | no | 342 |
| Cuba (CONFEDERATION) | Color | DarkRed | 343 |
| Cuba (CONFEDERATION) | Allies | Alliance,French,Brits,Africans,Arabs,Confederation,Russians,Nod,Neutral,Neutral2 | 344 |
| Cuba (CONFEDERATION) | Percent Built | 0 | 345 |
| Cuba (CONFEDERATION) | Node Count | 0 | 346 |
| Russia (RUSSIANS) | Country | Russians | 349 |
| Russia (RUSSIANS) | Technology level | 10 | 350 |
| Russia (RUSSIANS) | Credits | 300 | 351 |
| Russia (RUSSIANS) | IQ | 5 | 352 |
| Russia (RUSSIANS) | Edge | North | 353 |
| Russia (RUSSIANS) | Player Control | no | 354 |
| Russia (RUSSIANS) | Color | DarkRed | 355 |
| Russia (RUSSIANS) | Allies | French,Brits,Africans,Arabs,Confederation,Russians,Nod,Neutral,Neutral2 | 356 |
| Russia (RUSSIANS) | Percent Built | 60 | 357 |
| Russia (RUSSIANS) | Node Count | 6 | 358 |
| Russia (RUSSIANS) | 000 | NAPOWR,120,48 | 359 |
| Russia (RUSSIANS) | 001 | NAPOWR,120,50 | 360 |
| Russia (RUSSIANS) | 002 | NAHAND,118,53 | 361 |
| Russia (RUSSIANS) | 003 | NAREFN,109,54 | 362 |
| Russia (RUSSIANS) | 004 | NAWEAP,109,50 | 363 |
| Russia (RUSSIANS) | 005 | NAREFN,109,46 | 364 |
| GDI (GDI) | Country | GDI | 367 |
| GDI (GDI) | Technology level | 1 | 368 |
| GDI (GDI) | Credits | 0 | 369 |
| GDI (GDI) | IQ | 0 | 370 |
| GDI (GDI) | Edge | North | 371 |
| GDI (GDI) | Player Control | yes | 372 |
| GDI (GDI) | Color | DarkGreen | 373 |
| GDI (GDI) | Allies | Americans,Alliance,French,Germans,GDI | 374 |
| GDI (GDI) | Percent Built | 0 | 375 |
| GDI (GDI) | Node Count | 0 | 376 |
| Nod (NOD) | Country | Nod | 379 |
| Nod (NOD) | Technology level | 1 | 380 |
| Nod (NOD) | Credits | 0 | 381 |
| Nod (NOD) | IQ | 0 | 382 |
| Nod (NOD) | Edge | North | 383 |
| Nod (NOD) | Player Control | no | 384 |
| Nod (NOD) | Color | DarkRed | 385 |
| Nod (NOD) | Allies | Brits,Africans,Arabs,Confederation,Russians,Nod | 386 |
| Nod (NOD) | Percent Built | 0 | 387 |
| Nod (NOD) | Node Count | 0 | 388 |
| Civilian (NEUTRAL) | Country | Neutral | 391 |
| Civilian (NEUTRAL) | Technology level | 1 | 392 |
| Civilian (NEUTRAL) | Credits | 0 | 393 |
| Civilian (NEUTRAL) | IQ | 0 | 394 |
| Civilian (NEUTRAL) | Edge | North | 395 |
| Civilian (NEUTRAL) | Player Control | no | 396 |
| Civilian (NEUTRAL) | Color | Grey | 397 |
| Civilian (NEUTRAL) | Allies | Americans,Alliance,Germans,Arabs,Russians,Neutral | 398 |
| Civilian (NEUTRAL) | Percent Built | 0 | 399 |
| Civilian (NEUTRAL) | Node Count | 0 | 400 |
| JP (SPECIAL) | Country | Special | 403 |
| JP (SPECIAL) | Technology level | 1 | 404 |
| JP (SPECIAL) | Credits | 0 | 405 |
| JP (SPECIAL) | IQ | 0 | 406 |
| JP (SPECIAL) | Edge | North | 407 |
| JP (SPECIAL) | Player Control | no | 408 |
| JP (SPECIAL) | Color | Grey | 409 |
| JP (SPECIAL) | Allies | Special | 410 |
| JP (SPECIAL) | Percent Built | 0 | 411 |
| JP (SPECIAL) | Node Count | 0 | 412 |
