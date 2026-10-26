# Operation: Chrono Defense - mission overrides and local definitions

[Trigger ledger](sov07s.md) | [Team plans](sov07s-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov07s.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Chrono Reinf Delay | 140 | 11 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 5000 | 12 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -10000 | 13 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Total AI Team Cap | 50,50,50 | 14 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | AI Safe Distance | 32 | 15 |
| War Miner (HARV) | Resource cargo capacity | 20 | 18 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 21 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 24 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 25 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 26 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 27 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 30 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 33 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 36 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 39 |
| SPECIALFLAGS | Tiberium Grows | yes | 42 |
| SPECIALFLAGS | Tiberium Spreads | yes | 43 |
| SPECIALFLAGS | Tiberium Explosive | no | 44 |
| SPECIALFLAGS | Destroyable Bridges | no | 45 |
| SPECIALFLAGS | MCV Deploy | no | 46 |
| SPECIALFLAGS | Initial Veteran | no | 47 |
| SPECIALFLAGS | Fixed Alliance | no | 48 |
| SPECIALFLAGS | Harvester Immune | no | 49 |
| SPECIALFLAGS | Fog Of War | no | 50 |
| SPECIALFLAGS | Inert | no | 51 |
| SPECIALFLAGS | Ion Storms | no | 52 |
| SPECIALFLAGS | Meteorites | no | 53 |
| SPECIALFLAGS | Visceroids | no | 54 |
| COUNTRIES (COUNTRIES) | 0 | Player | 57 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 58 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 59 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 60 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 61 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 62 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 63 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 64 |
| PISTOLA (PISTOLA) | Damage | 8 | 144 |
| PISTOLA (PISTOLA) | ROF | 20 | 145 |
| PISTOLA (PISTOLA) | Range | 3 | 146 |
| PISTOLA (PISTOLA) | Projectile | InvisibleLow | 147 |
| PISTOLA (PISTOLA) | Movement rating | 100 | 148 |
| PISTOLA (PISTOLA) | Warhead | SA | 149 |
| PISTOLA (PISTOLA) | Report | CivAttack | 150 |
| CRATERULES (CRATERULES) | Solo Crate Money | 5000 | 153 |
| CRATERULES (CRATERULES) | Wood Crate | Money | 154 |
| POWERUPS (POWERUPS) | Armor class | 20,ARMOR,yes,1.5 | 167 |
| POWERUPS (POWERUPS) | Firepower | 20,FIREPOWR,yes,2.0 | 168 |
| POWERUPS (POWERUPS) | Heal Base | 0,HEALALL,yes | 169 |
| POWERUPS (POWERUPS) | Money | 100,MONEY,yes,2000 | 170 |
| POWERUPS (POWERUPS) | Reveal | 0,REVEAL,yes | 171 |
| POWERUPS (POWERUPS) | Movement rating | 20,SPEED,yes,1.2 | 172 |
| POWERUPS (POWERUPS) | Veteran | 10,VETERAN,yes,1 | 173 |
| POWERUPS (POWERUPS) | Unit | 0,<none>,no | 174 |
| POWERUPS (POWERUPS) | Invulnerability | 0,ARMOR,yes,1.0 | 176 |
| POWERUPS (POWERUPS) | Ion Storm | 0,<none>,yes | 177 |
| POWERUPS (POWERUPS) | Gas | 0,<none>,yes,100 | 178 |
| POWERUPS (POWERUPS) | Tiberium | 0,<none>,no | 179 |
| POWERUPS (POWERUPS) | Pod | 0,<none>,no | 180 |
| POWERUPS (POWERUPS) | Cloak | 0,CLOAK,yes | 181 |
| POWERUPS (POWERUPS) | Darkness | 0,SHROUDX,yes | 182 |
| POWERUPS (POWERUPS) | Explosion | 0,<none>,yes,500 | 183 |
| POWERUPS (POWERUPS) | ICBM | 0,CHEMISLE,yes | 184 |
| POWERUPS (POWERUPS) | Napalm | 0,<none>,no,600 | 185 |
| POWERUPS (POWERUPS) | Squad | 0,<none>,no | 186 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 2200 | 193 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 194 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.25 | 195 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.25 | 196 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.00 | 197 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 1800 | 200 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.001 | 201 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 0.3 | 202 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.05 | 203 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 0.5 | 204 |
| Soviet Battle Lab (NATECH) | Technology level | -1 | 207 |
| Soviet Battle Lab (NATECH) | Selling forbidden | true | 208 |
| Soviet Battle Lab (NATECH) | Name | Soviet Battle Lab | 209 |
| Soviet Battle Lab (NATECH) | Starting health capacity | 750 | 210 |
| Soviet Battle Lab (NATECH) | Armor class | concrete | 211 |
| Soviet Shipyard (NAYARD) | Technology level | -1 | 214 |
| Technician (CTECH) | Primary | Pistola | 217 |
| Technician (CTECH) | Insignificant-object flag | no | 218 |
| Technician (CTECH) | Ammo | 100 | 219 |
| Technician (CTECH) | Reload | 80 | 220 |
| Civilian (CIVSFM) | Name | Civilian Snow Fat Male | 223 |
| Civilian (CIVSFM) | Armor class | none | 224 |
| Civilian (CIVSFM) | Primary | Pistola | 225 |
| Civilian (CIVSFM) | Insignificant-object flag | no | 226 |
| Civilian (CIVSFM) | Ammo | 100 | 227 |
| Civilian (CIVSFM) | Sight radius setting | 2 | 228 |
| Civilian (CIVSFM) | Movement rating | 4 | 229 |
| Civilian (CIVSFM) | Fraidycat | yes | 230 |
| Civilian (CIVSFM) | Civilian | yes | 231 |
| Civilian (CIVSFM) | Nominal | yes | 232 |
| Civilian (CIVSF) | Name | Civilian Snow Female | 235 |
| Civilian (CIVSF) | Armor class | none | 236 |
| Civilian (CIVSF) | Primary | Pistola | 237 |
| Civilian (CIVSF) | Insignificant-object flag | no | 238 |
| Civilian (CIVSF) | Ammo | 100 | 239 |
| Civilian (CIVSF) | Sight radius setting | 2 | 240 |
| Civilian (CIVSF) | Movement rating | 4 | 241 |
| Civilian (CIVSF) | Fraidycat | yes | 242 |
| Civilian (CIVSF) | Civilian | yes | 243 |
| Civilian (CIVSF) | Nominal | yes | 244 |
| Civilian (CIVSTM) | Name | Civilian Snow Thin Male | 247 |
| Civilian (CIVSTM) | Armor class | none | 248 |
| Civilian (CIVSTM) | Primary | Pistola | 249 |
| Civilian (CIVSTM) | Insignificant-object flag | no | 250 |
| Civilian (CIVSTM) | Ammo | 100 | 251 |
| Civilian (CIVSTM) | Sight radius setting | 2 | 252 |
| Civilian (CIVSTM) | Movement rating | 4 | 253 |
| Civilian (CIVSTM) | Fraidycat | yes | 254 |
| Civilian (CIVSTM) | Civilian | yes | 255 |
| Civilian (CIVSTM) | Nominal | yes | 256 |
| Engineer (ENGINEER) | Technology level | -1 | 259 |
| Attack Dog (ADOG) | Technology level | -1 | 262 |
| Yuri (YURI) | Technology level | -1 | 265 |
| Propaganda Truck (PROPA) | Name | RA2 Propaganda Truck | 268 |
| Propaganda Truck (PROPA) | Carries Crate | yes | 269 |
| Truck (loaded) (TRUCKB) | Name | Truck (loaded) | 272 |
| Truck (loaded) (TRUCKB) | Carries Crate | yes | 273 |
| VARIABLENAMES (VARIABLENAMES) | 0 | PropTruckArrived,0 | 314 |
| VARIABLENAMES (VARIABLENAMES) | 1 | CitizensArrived,0 | 315 |
| VARIABLENAMES (VARIABLENAMES) | 2 | SuppliesArrived,0 | 316 |
| VARIABLENAMES (VARIABLENAMES) | 3 | CitizensGathered,0 | 317 |
