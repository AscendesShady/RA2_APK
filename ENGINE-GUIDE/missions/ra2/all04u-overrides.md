# Operation: Last Chance - mission overrides and local definitions

[Trigger ledger](all04u.md) | [Team plans](all04u-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS01.MIX/all04u.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 3000,2000,1000 | 11 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 5000 | 12 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -5000 | 13 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Deferment | 1 | 14 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Damage | 1 | 15 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Storm Duration | 200 | 16 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Warhead | IonWH | 17 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Hit Delay | 40000 | 18 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Scatter Delay | 40000 | 19 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Cell Spread | 1 | 20 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Print Text | no | 21 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Ion Storms | no | 22 |
| AUDIOVISUAL (AUDIOVISUAL) | Storm Sound | ChronoLegionAttack | 25 |
| AUDIOVISUAL (AUDIOVISUAL) | Lightning Sounds | ChronoLegionAttack | 26 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | UI Name | Name:Storm | 29 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Name | Lightning Storm | 30 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Is Powered | true | 31 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Recharge Time | 10 | 32 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Type | LightningStorm | 33 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Action | LightningStorm | 34 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Sidebar Image | BOLTICON | 35 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Show Timer | no | 36 |
| War Miner (HARV) | Resource cargo capacity | 20 | 39 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 42 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 45 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 46 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 47 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 48 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 51 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 54 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 57 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 60 |
| SPECIALFLAGS | Tiberium Grows | no | 63 |
| SPECIALFLAGS | Tiberium Spreads | yes | 64 |
| SPECIALFLAGS | Tiberium Explosive | no | 65 |
| SPECIALFLAGS | Destroyable Bridges | yes | 66 |
| SPECIALFLAGS | MCV Deploy | no | 67 |
| SPECIALFLAGS | Initial Veteran | no | 68 |
| SPECIALFLAGS | Fixed Alliance | no | 69 |
| SPECIALFLAGS | Harvester Immune | no | 70 |
| SPECIALFLAGS | Fog Of War | no | 71 |
| SPECIALFLAGS | Inert | no | 72 |
| SPECIALFLAGS | Ion Storms | no | 73 |
| SPECIALFLAGS | Meteorites | no | 74 |
| SPECIALFLAGS | Visceroids | no | 75 |
| COUNTRIES (COUNTRIES) | 0 | Player | 78 |
| COUNTRIES (COUNTRIES) | 1 | Russian1 | 79 |
| COUNTRIES (COUNTRIES) | 2 | Russian2 | 80 |
| COUNTRIES (COUNTRIES) | 3 | Cops | 81 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 82 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 83 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 84 |
| COUNTRIES (COUNTRIES) | 7 | Russian3 | 85 |
| COUNTRIES (COUNTRIES) | 8 | CivilianTech | 86 |
| COUNTRIES (COUNTRIES) | 9 | PlayerAlt | 87 |
| COUNTRIES (COUNTRIES) | 10 | PlayerAlt2 | 88 |
| Psychic Amplifier (NAPSYA) | Name | RA2 Psychic Amplifier | 198 |
| Psychic Amplifier (NAPSYA) | Engineer-capture permission | false | 199 |
| Psychic Amplifier (NAPSYA) | Working Sound | PsychicAmplifierLoop | 200 |
| Psychic Amplifier (NAPSYA) | Ambient Sound | Dummy | 201 |
| Grand Cannon (GTGCAN) | Name | Grand Cannon | 204 |
| Grand Cannon (GTGCAN) | Starting health capacity | 1200 | 205 |
| Grand Cannon (GTGCAN) | Armor class | wood | 206 |
| Grand Cannon (GTGCAN) | Sight radius setting | 9 | 207 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | Damage | 100 | 210 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | ROF | 150 | 211 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | Range | 15 | 212 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | Minimum Range | 3 | 213 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | Projectile | GrandCannonBall | 214 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | Movement rating | 1 | 215 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | Report | GrandCannonAttack | 216 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | Bright | yes | 217 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | Warhead | GrandCannonWH | 218 |
| GRANDCANNONWEAPON (GRANDCANNONWEAPON) | Anim | GCMUZZLE | 219 |
| Nuclear Missile Silo (NAMISL) | Charged Anim Time | 9.7 | 222 |
| Nuclear Missile Silo (NAMISL) | Signed power contribution | 0 | 223 |
| Nuclear Missile Silo (NAMISL) | Price in credits | 5 | 224 |
| Nuclear Missile (MULTISPECIAL) | Name | N U K E !!! | 227 |
| Nuclear Missile (MULTISPECIAL) | Show Timer | no | 228 |
| Sears Tower (CACHIG05) | Name | RA2 Chicago Sears Tower | 231 |
| Sears Tower (CACHIG05) | Whole-map reveal service | no | 232 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 3000 | 235 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 236 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.40 | 237 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.40 | 238 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.15 | 239 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 1800 | 242 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.001 | 243 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 0.3 | 244 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.05 | 245 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 0.5 | 246 |
| Allied Repair Depot (GADEPT) | Name | Allied Service Depot | 249 |
| Allied Repair Depot (GADEPT) | Technology level | -1 | 250 |
| Police Car (COP) | Name | RA2 Pig | 253 |
| Police Car (COP) | Starting health capacity | 20 | 254 |
| Police Car (COP) | Primary | Pistola | 255 |
| Police Car (COP) | Movement rating | 10 | 256 |
| Police Car (COP) | Can crush through ordinary crushing logic | no | 257 |
| Police Car (COP) | Turret | no | 258 |
| Police Car (COP) | Insignificant-object flag | no | 259 |
| Police Car (COP) | Ambient Sound | PoliceSirenLoop | 260 |
| PISTOLA (PISTOLA) | Damage | 5 | 263 |
| PISTOLA (PISTOLA) | ROF | 20 | 264 |
| PISTOLA (PISTOLA) | Range | 4 | 265 |
| PISTOLA (PISTOLA) | Projectile | InvisibleLow | 266 |
| PISTOLA (PISTOLA) | Movement rating | 100 | 267 |
| PISTOLA (PISTOLA) | Warhead | SA | 268 |
| PISTOLA (PISTOLA) | Report | CivAttack | 269 |
| Engineer (SENGINEER) | Technology level | -1 | 272 |
| Attack Dog (DOG) | Technology level | -1 | 275 |
| Tesla Trooper (SHK) | Name | Shock Trooper | 278 |
| Tesla Trooper (SHK) | Technology level | 4 | 279 |
| Civilian (CIVBFM) | Name | Civilian Beach Fat Male | 282 |
| Civilian (CIVBFM) | Insignificant-object flag | no | 283 |
| Civilian (CIVBFM) | Image | BeInvisibleHack | 284 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Reactor1Taken,0 | 325 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Reactor2Taken,0 | 326 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Reactor3Taken,0 | 327 |
| VARIABLENAMES (VARIABLENAMES) | 3 | BridgeOpen,1 | 328 |
| VARIABLENAMES (VARIABLENAMES) | 4 | CopsArrived,0 | 329 |
| VARIABLENAMES (VARIABLENAMES) | 5 | mcvUnloaded,0 | 330 |
