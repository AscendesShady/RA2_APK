# Operation: Red Dawn - mission overrides and local definitions

[Trigger ledger](sov01t.md) | [Team plans](sov01t-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov01t.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 2 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 5 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 6 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 7 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 8 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 11 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 14 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 17 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 20 |
| Automobile (CAR) | Insignificant-object flag | no | 23 |
| Automobile (CAR) | Threat contribution | 15 | 24 |
| Cruise Ship (CRUISE) | Insignificant-object flag | no | 27 |
| Cruise Ship (CRUISE) | Threat contribution | 15 | 28 |
| Pickup Truck (PTRUCK) | Insignificant-object flag | no | 31 |
| Pickup Truck (PTRUCK) | Threat contribution | 15 | 32 |
| Taxi (TAXI) | Insignificant-object flag | no | 35 |
| Taxi (TAXI) | Threat contribution | 15 | 36 |
| Automobile (SUVW) | Insignificant-object flag | no | 39 |
| Automobile (SUVW) | Threat contribution | 15 | 40 |
| Excavator (CONA) | Insignificant-object flag | no | 43 |
| Excavator (CONA) | Threat contribution | 15 | 44 |
| Police Car (COP) | Insignificant-object flag | no | 47 |
| Police Car (COP) | Threat contribution | 15 | 48 |
| Police Car (COP) | Ambient Sound | Dummy | 49 |
| Automobile (EUROC) | Insignificant-object flag | no | 52 |
| Automobile (EUROC) | Threat contribution | 15 | 53 |
| Limousine (LIMO) | Insignificant-object flag | no | 56 |
| Limousine (LIMO) | Threat contribution | 15 | 57 |
| Automobile (STANG) | Insignificant-object flag | no | 60 |
| Automobile (STANG) | Threat contribution | 15 | 61 |
| Automobile (SUVB) | Insignificant-object flag | no | 64 |
| Automobile (SUVB) | Threat contribution | 15 | 65 |
| Civilian (CIV1) | Insignificant-object flag | no | 68 |
| Civilian (CIV1) | Threat contribution | 15 | 69 |
| Civilian (CIV2) | Insignificant-object flag | no | 72 |
| Civilian (CIV2) | Threat contribution | 15 | 73 |
| Civilian (CIV3) | Insignificant-object flag | no | 76 |
| Civilian (CIV3) | Threat contribution | 15 | 77 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 1500 | 80 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -1500 | 81 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 1000,750,500 | 82 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Parachute Max Fall Rate | -5 | 83 |
| Engineer (ENGINEER) | Technology level | -1 | 86 |
| Attack Dog (ADOG) | Technology level | -1 | 89 |
| Soviet Construction Yard (NACNST) | UI Name | Name:NACNST | 92 |
| Soviet Construction Yard (NACNST) | Selling forbidden | Yes | 93 |
| Soviet Construction Vehicle (SMCV) | UI Name | Name:SMCV | 96 |
| Soviet Construction Vehicle (SMCV) | Name | Soviet Construction Vehicle | 97 |
| Soviet Construction Vehicle (SMCV) | Sight radius setting | 5 | 98 |
| Iwo Jima Victory Monument (CAWASH19) | Name | RA2 Iwo Jima Memorial | 101 |
| Iwo Jima Victory Monument (CAWASH19) | UI Name | Name:CAWASH19 | 102 |
| Iwo Jima Victory Monument (CAWASH19) | Infantry garrison permitted | yes | 103 |
| Iwo Jima Victory Monument (CAWASH19) | Garrison capacity | 1 | 104 |
| Iwo Jima Victory Monument (CAWASH19) | Clear All Weapons | yes | 105 |
| Iwo Jima Victory Monument (CAWASH19) | General immunity flag | Yes | 106 |
| Iwo Jima Victory Monument (CAWASH19) | Show Occupant Pips | false | 107 |
| Soviet Wall (NAWALL) | UI Name | Name:NAWALL | 110 |
| Soviet Wall (NAWALL) | Name | Soviet Wall | 111 |
| Soviet Wall (NAWALL) | Technology level | -1 | 112 |
| Allied Wall (GAWALL) | UI Name | Name:GAWALL | 115 |
| Allied Wall (GAWALL) | Name | Allied Wall | 116 |
| Allied Wall (GAWALL) | Technology level | -1 | 117 |
| Paradrop (PARADROPSPECIAL) | UI Name | Name:Para | 120 |
| Paradrop (PARADROPSPECIAL) | Name | Paratrooper Drop | 121 |
| Paradrop (PARADROPSPECIAL) | Recharge Time | 3 | 122 |
| Pentagon (CAWA2A) | UI Name | Name:CAWA2A | 125 |
| Pentagon (CAWA2A) | Name | RA2 Wash Pent A | 126 |
| Pentagon (CAWA2A) | Engineer-capture permission | false | 127 |
| Pentagon (CAWA2A) | Starting health capacity | 180 | 128 |
| Pentagon (CAWA2A) | Infantry garrison permitted | no | 129 |
| Pentagon (CAWA2A) | Garrison capacity | 0 | 130 |
| Pentagon (CAWA2A) | Clear All Weapons | yes | 131 |
| Pentagon (CAWA2B) | UI Name | Name:CAWA2A | 134 |
| Pentagon (CAWA2B) | Name | RA2 Wash Pent B | 135 |
| Pentagon (CAWA2B) | Engineer-capture permission | false | 136 |
| Pentagon (CAWA2B) | Starting health capacity | 180 | 137 |
| Pentagon (CAWA2B) | Infantry garrison permitted | no | 138 |
| Pentagon (CAWA2B) | Garrison capacity | 0 | 139 |
| Pentagon (CAWA2B) | Clear All Weapons | yes | 140 |
| Pentagon (CAWA2C) | UI Name | Name:CAWA2A | 143 |
| Pentagon (CAWA2C) | Name | RA2 Wash Pent C | 144 |
| Pentagon (CAWA2C) | Engineer-capture permission | false | 145 |
| Pentagon (CAWA2C) | Starting health capacity | 180 | 146 |
| Pentagon (CAWA2C) | Infantry garrison permitted | no | 147 |
| Pentagon (CAWA2C) | Garrison capacity | 0 | 148 |
| Pentagon (CAWA2C) | Clear All Weapons | yes | 149 |
| Pentagon (CAWA2D) | UI Name | Name:CAWA2A | 152 |
| Pentagon (CAWA2D) | Name | RA2 Wash Pent D | 153 |
| Pentagon (CAWA2D) | Engineer-capture permission | false | 154 |
| Pentagon (CAWA2D) | Starting health capacity | 180 | 155 |
| Pentagon (CAWA2D) | Infantry garrison permitted | no | 156 |
| Pentagon (CAWA2D) | Garrison capacity | 0 | 157 |
| Pentagon (CAWA2D) | Clear All Weapons | yes | 158 |
| Flak Trooper (FLAKT) | UI Name | Name:FLAKT | 170 |
| Flak Trooper (FLAKT) | Name | Flak Trooper | 171 |
| Flak Trooper (FLAKT) | Technology level | -1 | 172 |
| Soviet War Factory (NAWEAP) | UI Name | Name:NAWEAP | 175 |
| Soviet War Factory (NAWEAP) | Name | Soviet War Factory | 176 |
| Soviet War Factory (NAWEAP) | Technology level | -1 | 177 |
| Allied War Factory (GAWEAP) | UI Name | Name:GAWEAP | 180 |
| Allied War Factory (GAWEAP) | Name | Allied War Factory | 181 |
| Allied War Factory (GAWEAP) | Technology level | -1 | 182 |
| Soviet Barracks (NAHAND) | UI Name | Name:NAHAND | 185 |
| Soviet Barracks (NAHAND) | Name | Soviet Barracks | 186 |
| Soviet Barracks (NAHAND) | Technology level | 1 | 187 |
| Soviet Shipyard (NAYARD) | UI Name | Name:NAYARD | 190 |
| Soviet Shipyard (NAYARD) | Name | Soviet Shipyard | 191 |
| Soviet Shipyard (NAYARD) | Technology level | -1 | 192 |
| SOVIETOCCUPYW (SOVIETOCCUPYW) | Range | 8 | 195 |
| VULCANTOWER (VULCANTOWER) | Range | 5 | 198 |
| War Miner (HARV) | Name | War Miner | 201 |
| War Miner (HARV) | Starting health capacity | 1000 | 202 |
| War Miner (HARV) | Armor class | medium | 203 |
| War Miner (HARV) | Sight radius setting | 4 | 204 |
| War Miner (HARV) | Movement rating | 6 | 205 |
| War Miner (HARV) | Resource cargo capacity | 20 | 206 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Cell Spread | 1.5 | 209 |
| OILEXPLOSIONWH (OILEXPLOSIONWH) | Percent At Max | .25 | 210 |
| Engineer (SENGINEER) | Sight radius setting | 9 | 213 |
| Engineer (SENGINEER) | Movement rating | 7 | 214 |
| Conscript (E2) | Name | Conscript | 217 |
| Conscript (E2) | Primary | M1Carbine | 218 |
| Conscript (E2) | Starting health capacity | 100 | 219 |
| Conscript (E2) | Armor class | none | 220 |
| Conscript (E2) | Sight radius setting | 9 | 221 |
| Conscript (E2) | Movement rating | 7 | 222 |
| Invisible Green Light Post (INGRNLMP) | Name | Invisible Green Light Post | 225 |
| Invisible Green Light Post (INGRNLMP) | Local light reach | 4000 | 226 |
| Invisible Green Light Post (INGRNLMP) | Local light intensity | 0.01 | 227 |
| Invisible Green Light Post (INGRNLMP) | Light Red Tint | 0.01 | 228 |
| Invisible Green Light Post (INGRNLMP) | Light Green Tint | 1.00 | 229 |
| Invisible Green Light Post (INGRNLMP) | Light Blue Tint | 1.00 | 230 |
| Invisible Red Light Post (INREDLMP) | Name | Invisible Red Light Post | 233 |
| Invisible Red Light Post (INREDLMP) | Local light reach | 4000 | 234 |
| Invisible Red Light Post (INREDLMP) | Local light intensity | 0.07 | 235 |
| Invisible Red Light Post (INREDLMP) | Light Red Tint | 0.30 | 236 |
| Invisible Red Light Post (INREDLMP) | Light Green Tint | 0.30 | 237 |
| Invisible Red Light Post (INREDLMP) | Light Blue Tint | 0.01 | 238 |
| Invisible Blue Light Post (INBLULMP) | Name | Invisible Blue Light Post | 241 |
| Invisible Blue Light Post (INBLULMP) | Local light reach | 4000 | 242 |
| Invisible Blue Light Post (INBLULMP) | Local light intensity | 0.01 | 243 |
| Invisible Blue Light Post (INBLULMP) | Light Red Tint | 0.01 | 244 |
| Invisible Blue Light Post (INBLULMP) | Light Green Tint | 0,01 | 245 |
| Invisible Blue Light Post (INBLULMP) | Light Blue Tint | 0.6 | 246 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 2500 | 249 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 250 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.25 | 251 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.10 | 252 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.01 | 253 |
| SPECIALFLAGS | Tiberium Grows | no | 256 |
| SPECIALFLAGS | Tiberium Spreads | yes | 257 |
| SPECIALFLAGS | Tiberium Explosive | no | 258 |
| SPECIALFLAGS | Destroyable Bridges | no | 259 |
| SPECIALFLAGS | MCV Deploy | no | 260 |
| SPECIALFLAGS | Initial Veteran | no | 261 |
| SPECIALFLAGS | Fixed Alliance | no | 262 |
| SPECIALFLAGS | Harvester Immune | no | 263 |
| SPECIALFLAGS | Fog Of War | no | 264 |
| SPECIALFLAGS | Inert | no | 265 |
| SPECIALFLAGS | Ion Storms | no | 266 |
| SPECIALFLAGS | Meteorites | no | 267 |
| SPECIALFLAGS | Visceroids | no | 268 |
| COUNTRIES (COUNTRIES) | 0 | Player | 271 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 272 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 273 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 274 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 275 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 276 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 277 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 278 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Need Reinforcements,0 | 403 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Win 1,1 | 404 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Win 2,0 | 405 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Win 3,0 | 406 |
| VARIABLENAMES (VARIABLENAMES) | 4 | Win 4,0 | 407 |
| VARIABLENAMES (VARIABLENAMES) | 5 | Baseball Panic,0 | 408 |
| VARIABLENAMES (VARIABLENAMES) | 6 | Bridge Discovered,0 | 409 |
| VARIABLENAMES (VARIABLENAMES) | 7 | Engineer Built,0 | 410 |
