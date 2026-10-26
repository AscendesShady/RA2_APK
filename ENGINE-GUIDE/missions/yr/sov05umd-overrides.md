# Operation: Escape Velocity - mission overrides and local definitions

[Trigger ledger](sov05umd.md) | [Team plans](sov05umd-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: mapsmd03.mix/sov05umd.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Spy Money Steal Percent | 0.05 | 2 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 5000 | 3 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -2500 | 4 |
| Yuri's Revenge -- Official Rules of Engagement (GENERAL) | Total AI Team Cap | 75,75,75 | 5 |
| Rhino Heavy Tank (HTNK) | Production-time multiplier | 1.0 | 8 |
| Grizzly Battle Tank (MTNK) | Production-time multiplier | 1.0 | 11 |
| Lasher Light Tank (LTNK) | Production-time multiplier | 1.0 | 14 |
| Kirov Airship (ZEP) | Name | Kirov Airship | 17 |
| Kirov Airship (ZEP) | Technology level | 9 | 18 |
| Tesla Tank (TTNK) | Name | Tesla Tank | 21 |
| Tesla Tank (TTNK) | Technology level | 9 | 22 |
| Demolition Truck (DTRUCK) | Name | Demolitions Truck | 25 |
| Demolition Truck (DTRUCK) | Permitted country list | Russians,Confederation,Africans,Arabs | 26 |
| Demolition Truck (DTRUCK) | Required countries | Russians | 27 |
| Demolition Truck (DTRUCK) | Technology level | 9 | 28 |
| Terrorist (TERROR) | Name | Terrorist | 31 |
| Terrorist (TERROR) | Permitted country list | Russians,Confederation,Africans,Arabs | 32 |
| Terrorist (TERROR) | Required countries | Russians | 33 |
| Boris (BORIS) | Name | Boris | 36 |
| Boris (BORIS) | Technology level | 10 | 37 |
| Soviet Construction Vehicle (SMCV) | Name | Soviet Construction Vehicle | 40 |
| Soviet Construction Vehicle (SMCV) | Technology level | 9 | 41 |
| Iron Curtain Device (NAIRON) | Name | Soviet Iron Curtain Device | 44 |
| Iron Curtain Device (NAIRON) | Technology level | 9 | 45 |
| Industrial Plant (NAINDP) | Name | Soviet Industrial Plant | 48 |
| Industrial Plant (NAINDP) | Technology level | 9 | 49 |
| Tech Secret Lab (CASLAB) | Name | Tech Secret Lab | 52 |
| Tech Secret Lab (CASLAB) | Secret infantry requirement | DESO | 53 |
| Yuri Battle Lab (YATECH) | Name | Yuri Battle Lab | 56 |
| Yuri Battle Lab (YATECH) | Technology level | 10 | 57 |
| Unknown Building (YAROCK) | Name | Rocket Launch Pad | 60 |
| Unknown Building (YAROCK) | General immunity flag | yes | 61 |
| Unknown Building (YAROCK) | Depends on power | yes | 62 |
| Unknown Building (YAROCK) | Signed power contribution | -150 | 63 |
| Moai (CAEAST01) | Name | Easter Island Statue | 66 |
| Moai (CAEAST01) | Signed power contribution | -1000 | 67 |
| Moai (CAEAST01) | Depends on power | yes | 68 |
| Moai (CAEAST01) | Overpowerable | false | 69 |
| Moai (CAEAST01) | Engineer-capture permission | false | 70 |
| Moai (CAEAST01) | Primary | none | 71 |
| Yuri Statue (CAEAST02) | Name | Yuri Bust | 74 |
| Yuri Statue (CAEAST02) | Signed power contribution | -100 | 75 |
| Yuri Statue (CAEAST02) | Depends on power | Yes | 76 |
| Yuri Statue (CAEAST02) | Overpowerable | true | 77 |
| Yuri Statue (CAEAST02) | Engineer-capture permission | true | 78 |
| SPECIALFLAGS | Tiberium Grows | no | 97 |
| SPECIALFLAGS | Tiberium Spreads | yes | 98 |
| SPECIALFLAGS | Tiberium Explosive | no | 99 |
| SPECIALFLAGS | Destroyable Bridges | yes | 100 |
| SPECIALFLAGS | MCV Deploy | no | 101 |
| SPECIALFLAGS | Initial Veteran | no | 102 |
| SPECIALFLAGS | Fixed Alliance | no | 103 |
| SPECIALFLAGS | Harvester Immune | no | 104 |
| SPECIALFLAGS | Fog Of War | no | 105 |
| SPECIALFLAGS | Inert | no | 106 |
| SPECIALFLAGS | Ion Storms | no | 107 |
| SPECIALFLAGS | Meteorites | no | 108 |
| SPECIALFLAGS | Visceroids | no | 109 |
| COUNTRIES (COUNTRIES) | 0 | Yuri2 | 121 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Sub Pen Destroyed,0 | 172 |
| VARIABLENAMES (VARIABLENAMES) | 1 | MCV @ AI,0 | 173 |
| America (AMERICANS) | Country | Americans | 214 |
| America (AMERICANS) | Technology level | 0 | 215 |
| America (AMERICANS) | Credits | 0 | 216 |
| America (AMERICANS) | IQ | 0 | 217 |
| America (AMERICANS) | Edge | East | 218 |
| America (AMERICANS) | Player Control | no | 219 |
| America (AMERICANS) | Color | Gold | 220 |
| America (AMERICANS) | Allies | Americans | 221 |
| America (AMERICANS) | Percent Built | 0 | 222 |
| America (AMERICANS) | Node Count | 0 | 223 |
| Korea (ALLIANCE) | Country | Alliance | 226 |
| Korea (ALLIANCE) | Technology level | 1 | 227 |
| Korea (ALLIANCE) | Credits | 0 | 228 |
| Korea (ALLIANCE) | IQ | 0 | 229 |
| Korea (ALLIANCE) | Edge | East | 230 |
| Korea (ALLIANCE) | Player Control | no | 231 |
| Korea (ALLIANCE) | Color | Purple | 232 |
| Korea (ALLIANCE) | Allies | Alliance | 233 |
| Korea (ALLIANCE) | Percent Built | 0 | 234 |
| Korea (ALLIANCE) | Node Count | 0 | 235 |
| France (FRENCH) | Country | French | 238 |
| France (FRENCH) | Technology level | 1 | 239 |
| France (FRENCH) | Credits | 0 | 240 |
| France (FRENCH) | IQ | 0 | 241 |
| France (FRENCH) | Edge | East | 242 |
| France (FRENCH) | Player Control | no | 243 |
| France (FRENCH) | Color | Purple | 244 |
| France (FRENCH) | Allies | French,Arabs,YuriCountry,Yuri2Country | 245 |
| France (FRENCH) | Percent Built | 0 | 246 |
| France (FRENCH) | Node Count | 0 | 247 |
| Germany (GERMANS) | Country | Germans | 250 |
| Germany (GERMANS) | Technology level | 10 | 251 |
| Germany (GERMANS) | Credits | 500 | 252 |
| Germany (GERMANS) | IQ | 4 | 253 |
| Germany (GERMANS) | Edge | West | 254 |
| Germany (GERMANS) | Player Control | no | 255 |
| Germany (GERMANS) | Color | Purple | 256 |
| Germany (GERMANS) | Allies | Germans | 257 |
| Germany (GERMANS) | Percent Built | 0 | 258 |
| Germany (GERMANS) | Node Count | 0 | 259 |
| Great Britain (BRITISH) | Country | British | 262 |
| Great Britain (BRITISH) | Technology level | 1 | 263 |
| Great Britain (BRITISH) | Credits | 0 | 264 |
| Great Britain (BRITISH) | IQ | 0 | 265 |
| Great Britain (BRITISH) | Edge | East | 266 |
| Great Britain (BRITISH) | Player Control | no | 267 |
| Great Britain (BRITISH) | Color | Purple | 268 |
| Great Britain (BRITISH) | Allies | British | 269 |
| Great Britain (BRITISH) | Percent Built | 0 | 270 |
| Great Britain (BRITISH) | Node Count | 0 | 271 |
| Libya (AFRICANS) | Country | Africans | 274 |
| Libya (AFRICANS) | Technology level | 1 | 275 |
| Libya (AFRICANS) | Credits | 0 | 276 |
| Libya (AFRICANS) | IQ | 0 | 277 |
| Libya (AFRICANS) | Edge | East | 278 |
| Libya (AFRICANS) | Player Control | no | 279 |
| Libya (AFRICANS) | Color | DarkRed | 280 |
| Libya (AFRICANS) | Allies | Africans | 281 |
| Libya (AFRICANS) | Percent Built | 0 | 282 |
| Libya (AFRICANS) | Node Count | 0 | 283 |
| Iraq (ARABS) | Country | Arabs | 286 |
| Iraq (ARABS) | Technology level | 1 | 287 |
| Iraq (ARABS) | Credits | 0 | 288 |
| Iraq (ARABS) | IQ | 0 | 289 |
| Iraq (ARABS) | Edge | East | 290 |
| Iraq (ARABS) | Player Control | no | 291 |
| Iraq (ARABS) | Color | Purple | 292 |
| Iraq (ARABS) | Allies | French,Arabs,YuriCountry,Yuri2Country | 293 |
| Iraq (ARABS) | Percent Built | 0 | 294 |
| Iraq (ARABS) | Node Count | 0 | 295 |
| Cuba (CONFEDERATION) | Country | Confederation | 298 |
| Cuba (CONFEDERATION) | Technology level | 1 | 299 |
| Cuba (CONFEDERATION) | Credits | 0 | 300 |
| Cuba (CONFEDERATION) | IQ | 0 | 301 |
| Cuba (CONFEDERATION) | Edge | East | 302 |
| Cuba (CONFEDERATION) | Player Control | no | 303 |
| Cuba (CONFEDERATION) | Color | DarkRed | 304 |
| Cuba (CONFEDERATION) | Allies | Confederation | 305 |
| Cuba (CONFEDERATION) | Percent Built | 0 | 306 |
| Cuba (CONFEDERATION) | Node Count | 0 | 307 |
| Russia (RUSSIANS) | Country | Russians | 310 |
| Russia (RUSSIANS) | Technology level | 9 | 311 |
| Russia (RUSSIANS) | Credits | 100 | 312 |
| Russia (RUSSIANS) | IQ | 0 | 313 |
| Russia (RUSSIANS) | Edge | North | 314 |
| Russia (RUSSIANS) | Player Control | yes | 315 |
| Russia (RUSSIANS) | Color | DarkRed | 316 |
| Russia (RUSSIANS) | Allies | Russians | 317 |
| Russia (RUSSIANS) | Percent Built | 0 | 318 |
| Russia (RUSSIANS) | Node Count | 0 | 319 |
| Yuri (YURICOUNTRY) | Country | YuriCountry | 322 |
| Yuri (YURICOUNTRY) | Technology level | 10 | 323 |
| Yuri (YURICOUNTRY) | Credits | 500 | 324 |
| Yuri (YURICOUNTRY) | IQ | 4 | 325 |
| Yuri (YURICOUNTRY) | Edge | West | 326 |
| Yuri (YURICOUNTRY) | Player Control | no | 327 |
| Yuri (YURICOUNTRY) | Color | Purple | 328 |
| Yuri (YURICOUNTRY) | Allies | French,Arabs,YuriCountry,Neutral,Yuri2Country | 329 |
| Yuri (YURICOUNTRY) | Percent Built | 0 | 330 |
| Yuri (YURICOUNTRY) | Node Count | 0 | 331 |
| GDI (GDI) | Country | GDI | 334 |
| GDI (GDI) | Technology level | 1 | 335 |
| GDI (GDI) | Credits | 0 | 336 |
| GDI (GDI) | IQ | 0 | 337 |
| GDI (GDI) | Edge | East | 338 |
| GDI (GDI) | Player Control | no | 339 |
| GDI (GDI) | Color | Gold | 340 |
| GDI (GDI) | Allies | GDI | 341 |
| GDI (GDI) | Percent Built | 0 | 342 |
| GDI (GDI) | Node Count | 0 | 343 |
| Nod (NOD) | Country | Nod | 346 |
| Nod (NOD) | Technology level | 1 | 347 |
| Nod (NOD) | Credits | 0 | 348 |
| Nod (NOD) | IQ | 0 | 349 |
| Nod (NOD) | Edge | East | 350 |
| Nod (NOD) | Player Control | no | 351 |
| Nod (NOD) | Color | Gold | 352 |
| Nod (NOD) | Allies | Nod | 353 |
| Nod (NOD) | Percent Built | 0 | 354 |
| Nod (NOD) | Node Count | 0 | 355 |
| Civilian (NEUTRAL) | Country | Neutral | 358 |
| Civilian (NEUTRAL) | Technology level | 1 | 359 |
| Civilian (NEUTRAL) | Credits | 0 | 360 |
| Civilian (NEUTRAL) | IQ | 0 | 361 |
| Civilian (NEUTRAL) | Edge | East | 362 |
| Civilian (NEUTRAL) | Player Control | no | 363 |
| Civilian (NEUTRAL) | Color | Grey | 364 |
| Civilian (NEUTRAL) | Allies | Neutral | 365 |
| Civilian (NEUTRAL) | Percent Built | 0 | 366 |
| Civilian (NEUTRAL) | Node Count | 0 | 367 |
| JP (SPECIAL) | Country | Special | 370 |
| JP (SPECIAL) | Technology level | 1 | 371 |
| JP (SPECIAL) | Credits | 0 | 372 |
| JP (SPECIAL) | IQ | 0 | 373 |
| JP (SPECIAL) | Edge | East | 374 |
| JP (SPECIAL) | Player Control | no | 375 |
| JP (SPECIAL) | Color | Grey | 376 |
| JP (SPECIAL) | Allies | Special | 377 |
| JP (SPECIAL) | Percent Built | 0 | 378 |
| JP (SPECIAL) | Node Count | 0 | 379 |
