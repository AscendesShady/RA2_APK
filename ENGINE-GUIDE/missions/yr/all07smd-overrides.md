# Operation: Brain Dead - mission overrides and local definitions

[Trigger ledger](all07smd.md) | [Team plans](all07smd-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: mapsmd03.mix/all07smd.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | AI Slave Miner Number | 2,2,2 | 2 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 5000 | 3 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -5000 | 4 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Spy Money Steal Percent | 0.05 | 5 |
| Rhino Heavy Tank (HTNK) | Production-time multiplier | 1.0 | 8 |
| Grizzly Battle Tank (MTNK) | Production-time multiplier | 1.0 | 11 |
| Lasher Light Tank (LTNK) | Production-time multiplier | 1.0 | 14 |
| Genetic Mutator (GENETICCONVERTERSPECIAL) | Recharge Time | 10 | 17 |
| Yuri Prime (YURIPR) | Technology level | 11 | 20 |
| Tanya (TANY) | Technology level | 12 | 23 |
| Boris (BORIS) | Technology level | 12 | 26 |
| Grand Cannon (GTGCAN) | UI Name | Name:GTGCAN | 29 |
| Grand Cannon (GTGCAN) | Name | Allied Grand Cannon | 30 |
| Grand Cannon (GTGCAN) | Construction category | Combat | 31 |
| Grand Cannon (GTGCAN) | Starting health capacity | 900 | 32 |
| Grand Cannon (GTGCAN) | Armor class | steel | 33 |
| Grand Cannon (GTGCAN) | Technology level | 7 | 34 |
| Grand Cannon (GTGCAN) | Required structures/groups | RADAR,GACNST | 35 |
| Grand Cannon (GTGCAN) | Placement adjacency setting | 2 | 36 |
| Grand Cannon (GTGCAN) | Sight radius setting | 10 | 37 |
| Grand Cannon (GTGCAN) | Permitted country list | British,French,Germans,Americans,Alliance | 38 |
| Grand Cannon (GTGCAN) | Price in credits | 2000 | 39 |
| Grand Cannon (GTGCAN) | Required countries | Americans | 40 |
| Grand Cannon (GTGCAN) | Points | 30 | 41 |
| Grand Cannon (GTGCAN) | Signed power contribution | -100 | 42 |
| Grand Cannon (GTGCAN) | Crewed | no | 43 |
| Grand Cannon (GTGCAN) | ROT | 1 | 44 |
| COUNTRIES (COUNTRIES) | 0 | Yuri2Country | 47 |
| COUNTRIES (COUNTRIES) | 1 | Yuri3Country | 48 |
| SPECIALFLAGS | Tiberium Grows | no | 87 |
| SPECIALFLAGS | Tiberium Spreads | yes | 88 |
| SPECIALFLAGS | Tiberium Explosive | no | 89 |
| SPECIALFLAGS | Destroyable Bridges | yes | 90 |
| SPECIALFLAGS | MCV Deploy | no | 91 |
| SPECIALFLAGS | Initial Veteran | no | 92 |
| SPECIALFLAGS | Fixed Alliance | no | 93 |
| SPECIALFLAGS | Harvester Immune | no | 94 |
| SPECIALFLAGS | Fog Of War | no | 95 |
| SPECIALFLAGS | Inert | no | 96 |
| SPECIALFLAGS | Ion Storms | no | 97 |
| SPECIALFLAGS | Meteorites | no | 98 |
| SPECIALFLAGS | Visceroids | no | 99 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Has_Soviet_Barrack,0 | 149 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Has_Soviet_WarFac,0 | 150 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Make_Hover1,0 | 151 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Make_HoverTD,0 | 152 |
| VARIABLENAMES (VARIABLENAMES) | 4 | Send_Barracks1,0 | 153 |
| VARIABLENAMES (VARIABLENAMES) | 5 | Send_Barracks2,0 | 154 |
| VARIABLENAMES (VARIABLENAMES) | 6 | Send_Barracks3,0 | 155 |
| VARIABLENAMES (VARIABLENAMES) | 7 | Make_HoverTF,0 | 156 |
| VARIABLENAMES (VARIABLENAMES) | 8 | Send_Barracks4,0 | 157 |
| VARIABLENAMES (VARIABLENAMES) | 9 | Make_HoverTH,0 | 158 |
| VARIABLENAMES (VARIABLENAMES) | 10 | Send_WarFac1,0 | 159 |
| VARIABLENAMES (VARIABLENAMES) | 11 | Send_WarFac2,0 | 160 |
| VARIABLENAMES (VARIABLENAMES) | 12 | Send_WarFac3,0 | 161 |
| VARIABLENAMES (VARIABLENAMES) | 13 | Send_WarFac4,0 | 162 |
| VARIABLENAMES (VARIABLENAMES) | 14 | Send_WarFac5,0 | 163 |
| VARIABLENAMES (VARIABLENAMES) | 15 | Has_Soviet_Radar,1 | 164 |
| VARIABLENAMES (VARIABLENAMES) | 16 | Make_HoverTJ,0 | 165 |
| VARIABLENAMES (VARIABLENAMES) | 17 | Has_Naval_Yard,0 | 166 |
| VARIABLENAMES (VARIABLENAMES) | 18 | Make_HoverTL,0 | 167 |
| VARIABLENAMES (VARIABLENAMES) | 19 | Make_HoverTN,0 | 168 |
| VARIABLENAMES (VARIABLENAMES) | 20 | Make_HoverTP,0 | 169 |
| VARIABLENAMES (VARIABLENAMES) | 21 | Make_HoverTR,0 | 170 |
| VARIABLENAMES (VARIABLENAMES) | 22 | Send_Barracks5,0 | 171 |
| VARIABLENAMES (VARIABLENAMES) | 23 | MCV_Arrived,0 | 172 |
| VARIABLENAMES (VARIABLENAMES) | 24 | Main_ConYards_Gone,0 | 173 |
| VARIABLENAMES (VARIABLENAMES) | 25 | Yuri_ConYard_Gone,0 | 174 |
| VARIABLENAMES (VARIABLENAMES) | 26 | Yuri2_ConYard_Gone,0 | 175 |
| VARIABLENAMES (VARIABLENAMES) | 27 | WarTeam1_Gone,1 | 176 |
| VARIABLENAMES (VARIABLENAMES) | 28 | Yuri_Prime_Built,0 | 177 |
| VARIABLENAMES (VARIABLENAMES) | 29 | Has_Allied_BLab,0 | 178 |
| VARIABLENAMES (VARIABLENAMES) | 30 | Has_Allied_WarF,0 | 179 |
| America (AMERICANS) | Country | Americans | 221 |
| America (AMERICANS) | Technology level | 10 | 222 |
| America (AMERICANS) | Credits | 150 | 223 |
| America (AMERICANS) | IQ | 0 | 224 |
| America (AMERICANS) | Edge | North | 225 |
| America (AMERICANS) | Player Control | yes | 226 |
| America (AMERICANS) | Color | DarkBlue | 227 |
| America (AMERICANS) | Allies | Americans,Special | 228 |
| America (AMERICANS) | Percent Built | 0 | 229 |
| America (AMERICANS) | Node Count | 0 | 230 |
| Korea (ALLIANCE) | Country | Alliance | 233 |
| Korea (ALLIANCE) | Technology level | 1 | 234 |
| Korea (ALLIANCE) | Credits | 0 | 235 |
| Korea (ALLIANCE) | IQ | 0 | 236 |
| Korea (ALLIANCE) | Edge | North | 237 |
| Korea (ALLIANCE) | Player Control | no | 238 |
| Korea (ALLIANCE) | Color | Gold | 239 |
| Korea (ALLIANCE) | Allies | Alliance | 240 |
| Korea (ALLIANCE) | Percent Built | 0 | 241 |
| Korea (ALLIANCE) | Node Count | 0 | 242 |
| France (FRENCH) | Country | French | 245 |
| France (FRENCH) | Technology level | 1 | 246 |
| France (FRENCH) | Credits | 0 | 247 |
| France (FRENCH) | IQ | 0 | 248 |
| France (FRENCH) | Edge | North | 249 |
| France (FRENCH) | Player Control | no | 250 |
| France (FRENCH) | Color | Gold | 251 |
| France (FRENCH) | Allies | French | 252 |
| France (FRENCH) | Percent Built | 0 | 253 |
| France (FRENCH) | Node Count | 0 | 254 |
| Germany (GERMANS) | Country | Germans | 257 |
| Germany (GERMANS) | Technology level | 1 | 258 |
| Germany (GERMANS) | Credits | 0 | 259 |
| Germany (GERMANS) | IQ | 0 | 260 |
| Germany (GERMANS) | Edge | North | 261 |
| Germany (GERMANS) | Player Control | no | 262 |
| Germany (GERMANS) | Color | Gold | 263 |
| Germany (GERMANS) | Allies | Germans | 264 |
| Germany (GERMANS) | Percent Built | 0 | 265 |
| Germany (GERMANS) | Node Count | 0 | 266 |
| Great Britain (BRITISH) | Country | British | 269 |
| Great Britain (BRITISH) | Technology level | 1 | 270 |
| Great Britain (BRITISH) | Credits | 0 | 271 |
| Great Britain (BRITISH) | IQ | 0 | 272 |
| Great Britain (BRITISH) | Edge | North | 273 |
| Great Britain (BRITISH) | Player Control | no | 274 |
| Great Britain (BRITISH) | Color | Gold | 275 |
| Great Britain (BRITISH) | Allies | British | 276 |
| Great Britain (BRITISH) | Percent Built | 0 | 277 |
| Great Britain (BRITISH) | Node Count | 0 | 278 |
| Libya (AFRICANS) | Country | Africans | 281 |
| Libya (AFRICANS) | Technology level | 10 | 282 |
| Libya (AFRICANS) | Credits | 1000 | 283 |
| Libya (AFRICANS) | IQ | 4 | 284 |
| Libya (AFRICANS) | Edge | North | 285 |
| Libya (AFRICANS) | Player Control | no | 286 |
| Libya (AFRICANS) | Color | DarkRed | 287 |
| Libya (AFRICANS) | Allies | Africans,Arabs,Confederation,Russians,YuriCountry,Nod,Yuri2,Yuri3 | 288 |
| Libya (AFRICANS) | Percent Built | 0 | 289 |
| Libya (AFRICANS) | Node Count | 0 | 290 |
| Iraq (ARABS) | Country | Arabs | 293 |
| Iraq (ARABS) | Technology level | 10 | 294 |
| Iraq (ARABS) | Credits | 100 | 295 |
| Iraq (ARABS) | IQ | 3 | 296 |
| Iraq (ARABS) | Edge | North | 297 |
| Iraq (ARABS) | Player Control | no | 298 |
| Iraq (ARABS) | Color | Purple | 299 |
| Iraq (ARABS) | Allies | Africans,Arabs,Confederation,Russians,YuriCountry,Nod,Neutral,Yuri2,Yuri3 | 300 |
| Iraq (ARABS) | Percent Built | 0 | 301 |
| Iraq (ARABS) | Node Count | 0 | 302 |
| Cuba (CONFEDERATION) | Country | Confederation | 305 |
| Cuba (CONFEDERATION) | Technology level | 1 | 306 |
| Cuba (CONFEDERATION) | Credits | 0 | 307 |
| Cuba (CONFEDERATION) | IQ | 0 | 308 |
| Cuba (CONFEDERATION) | Edge | North | 309 |
| Cuba (CONFEDERATION) | Player Control | no | 310 |
| Cuba (CONFEDERATION) | Color | Purple | 311 |
| Cuba (CONFEDERATION) | Allies | Africans,Arabs,Confederation,Russians,YuriCountry,Nod,Neutral,Yuri2,Yuri3 | 312 |
| Cuba (CONFEDERATION) | Percent Built | 0 | 313 |
| Cuba (CONFEDERATION) | Node Count | 0 | 314 |
| Russia (RUSSIANS) | Country | Russians | 317 |
| Russia (RUSSIANS) | Technology level | 1 | 318 |
| Russia (RUSSIANS) | Credits | 0 | 319 |
| Russia (RUSSIANS) | IQ | 0 | 320 |
| Russia (RUSSIANS) | Edge | North | 321 |
| Russia (RUSSIANS) | Player Control | no | 322 |
| Russia (RUSSIANS) | Color | DarkRed | 323 |
| Russia (RUSSIANS) | Allies | Africans,Arabs,Confederation,Russians,YuriCountry,Nod,Neutral,Yuri2,Yuri3 | 324 |
| Russia (RUSSIANS) | Percent Built | 0 | 325 |
| Russia (RUSSIANS) | Node Count | 0 | 326 |
| Yuri (YURICOUNTRY) | Country | YuriCountry | 329 |
| Yuri (YURICOUNTRY) | Technology level | 10 | 330 |
| Yuri (YURICOUNTRY) | Credits | 1000 | 331 |
| Yuri (YURICOUNTRY) | IQ | 5 | 332 |
| Yuri (YURICOUNTRY) | Edge | North | 333 |
| Yuri (YURICOUNTRY) | Player Control | no | 334 |
| Yuri (YURICOUNTRY) | Color | Purple2 | 335 |
| Yuri (YURICOUNTRY) | Allies | Africans,Arabs,Confederation,Russians,YuriCountry,Nod,Neutral,Yuri2,Yuri3 | 336 |
| Yuri (YURICOUNTRY) | Percent Built | 100 | 337 |
| Yuri (YURICOUNTRY) | Node Count | 13 | 338 |
| Yuri (YURICOUNTRY) | 000 | YAWEAP,176,157 | 339 |
| Yuri (YURICOUNTRY) | 001 | YAPOWR,175,153 | 340 |
| Yuri (YURICOUNTRY) | 002 | YABRCK,169,155 | 341 |
| Yuri (YURICOUNTRY) | 003 | YAPOWR,187,154 | 342 |
| Yuri (YURICOUNTRY) | 004 | YAPOWR,193,154 | 343 |
| Yuri (YURICOUNTRY) | 005 | YAPOWR,197,158 | 344 |
| Yuri (YURICOUNTRY) | 006 | YAPOWR,183,144 | 345 |
| Yuri (YURICOUNTRY) | 007 | NACLON,180,146 | 346 |
| Yuri (YURICOUNTRY) | 008 | NAPSIS,179,140 | 347 |
| Yuri (YURICOUNTRY) | 009 | YAGRND,188,149 | 348 |
| Yuri (YURICOUNTRY) | 010 | YAPSYT,177,151 | 349 |
| Yuri (YURICOUNTRY) | 011 | YAPSYT,184,148 | 350 |
| Yuri (YURICOUNTRY) | 012 | YAPSYT,191,157 | 351 |
| GDI (GDI) | Country | GDI | 354 |
| GDI (GDI) | Technology level | 1 | 355 |
| GDI (GDI) | Credits | 0 | 356 |
| GDI (GDI) | IQ | 0 | 357 |
| GDI (GDI) | Edge | North | 358 |
| GDI (GDI) | Player Control | no | 359 |
| GDI (GDI) | Color | Gold | 360 |
| GDI (GDI) | Allies | GDI | 361 |
| GDI (GDI) | Percent Built | 0 | 362 |
| GDI (GDI) | Node Count | 0 | 363 |
| Nod (NOD) | Country | Nod | 366 |
| Nod (NOD) | Technology level | 1 | 367 |
| Nod (NOD) | Credits | 0 | 368 |
| Nod (NOD) | IQ | 0 | 369 |
| Nod (NOD) | Edge | North | 370 |
| Nod (NOD) | Player Control | no | 371 |
| Nod (NOD) | Color | Purple | 372 |
| Nod (NOD) | Allies | Africans,Arabs,Confederation,Russians,YuriCountry,Nod,Neutral,Yuri2,Yuri3 | 373 |
| Nod (NOD) | Percent Built | 0 | 374 |
| Nod (NOD) | Node Count | 0 | 375 |
| Civilian (NEUTRAL) | Country | Neutral | 378 |
| Civilian (NEUTRAL) | Technology level | 1 | 379 |
| Civilian (NEUTRAL) | Credits | 0 | 380 |
| Civilian (NEUTRAL) | IQ | 0 | 381 |
| Civilian (NEUTRAL) | Edge | North | 382 |
| Civilian (NEUTRAL) | Player Control | no | 383 |
| Civilian (NEUTRAL) | Color | Grey | 384 |
| Civilian (NEUTRAL) | Allies | Americans,Confederation,Russians,YuriCountry,Nod,Neutral,Yuri2 | 385 |
| Civilian (NEUTRAL) | Percent Built | 0 | 386 |
| Civilian (NEUTRAL) | Node Count | 0 | 387 |
| JP (SPECIAL) | Country | Special | 390 |
| JP (SPECIAL) | Technology level | 1 | 391 |
| JP (SPECIAL) | Credits | 0 | 392 |
| JP (SPECIAL) | IQ | 0 | 393 |
| JP (SPECIAL) | Edge | North | 394 |
| JP (SPECIAL) | Player Control | no | 395 |
| JP (SPECIAL) | Color | DarkRed | 396 |
| JP (SPECIAL) | Allies | Americans,Special | 397 |
| JP (SPECIAL) | Percent Built | 0 | 398 |
| JP (SPECIAL) | Node Count | 0 | 399 |
