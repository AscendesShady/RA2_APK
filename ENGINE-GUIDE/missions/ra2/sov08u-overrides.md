# Operation: Desecration - mission overrides and local definitions

[Trigger ledger](sov08u.md) | [Team plans](sov08u-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov08u.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 2000,1750,1500 | 11 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 5000 | 12 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -5000 | 13 |
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
| RADBEAMWEAPON (RADBEAMWEAPON) | Damage | 200 | 40 |
| CRATERULES (CRATERULES) | Solo Crate Money | 8000 | 43 |
| SPECIALFLAGS | Tiberium Grows | yes | 46 |
| SPECIALFLAGS | Tiberium Spreads | yes | 47 |
| SPECIALFLAGS | Tiberium Explosive | no | 48 |
| SPECIALFLAGS | Destroyable Bridges | yes | 49 |
| SPECIALFLAGS | MCV Deploy | yes | 50 |
| SPECIALFLAGS | Initial Veteran | no | 51 |
| SPECIALFLAGS | Fixed Alliance | no | 52 |
| SPECIALFLAGS | Harvester Immune | no | 53 |
| SPECIALFLAGS | Fog Of War | no | 54 |
| SPECIALFLAGS | Inert | no | 55 |
| SPECIALFLAGS | Ion Storms | no | 56 |
| SPECIALFLAGS | Meteorites | no | 57 |
| SPECIALFLAGS | Visceroids | no | 58 |
| COUNTRIES (COUNTRIES) | 0 | Player | 61 |
| COUNTRIES (COUNTRIES) | 1 | Vlad1 | 62 |
| COUNTRIES (COUNTRIES) | 2 | Vlad2 | 63 |
| COUNTRIES (COUNTRIES) | 3 | CivilianArmy | 64 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 65 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 66 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 67 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 68 |
| POWERUPS (POWERUPS) | Armor class | 20,ARMOR,yes,1.5 | 159 |
| POWERUPS (POWERUPS) | Firepower | 20,FIREPOWR,yes,2.0 | 160 |
| POWERUPS (POWERUPS) | Heal Base | 0,HEALALL,yes | 161 |
| POWERUPS (POWERUPS) | Money | 100,MONEY,yes,2000 | 162 |
| POWERUPS (POWERUPS) | Reveal | 5,REVEAL,yes | 163 |
| POWERUPS (POWERUPS) | Movement rating | 20,SPEED,yes,1.2 | 164 |
| POWERUPS (POWERUPS) | Veteran | 30,VETERAN,yes,1 | 165 |
| POWERUPS (POWERUPS) | Unit | 0,<none>,no | 166 |
| POWERUPS (POWERUPS) | Invulnerability | 0,ARMOR,yes,1.0 | 168 |
| POWERUPS (POWERUPS) | Ion Storm | 0,<none>,yes | 169 |
| POWERUPS (POWERUPS) | Gas | 0,<none>,yes,100 | 170 |
| POWERUPS (POWERUPS) | Tiberium | 0,<none>,no | 171 |
| POWERUPS (POWERUPS) | Pod | 0,<none>,no | 172 |
| POWERUPS (POWERUPS) | Cloak | 0,CLOAK,yes | 173 |
| POWERUPS (POWERUPS) | Darkness | 0,SHROUDX,yes | 174 |
| POWERUPS (POWERUPS) | Explosion | 0,<none>,yes,500 | 175 |
| POWERUPS (POWERUPS) | ICBM | 0,CHEMISLE,yes | 176 |
| POWERUPS (POWERUPS) | Napalm | 0,<none>,no,600 | 177 |
| POWERUPS (POWERUPS) | Squad | 0,<none>,no | 178 |
| Psychic Beacon (NAPSYB) | Name | RA2 Psychic Beacon | 185 |
| Psychic Beacon (NAPSYB) | Engineer-capture permission | false | 186 |
| White House (CAWASH01) | Name | RA2 White House | 189 |
| White House (CAWASH01) | Starting health capacity | 1000 | 190 |
| White House (CAWASH01) | Infantry garrison permitted | no | 191 |
| White House (CAWASH01) | Primary | none | 192 |
| White House (CAWASH01) | Secondary | none | 193 |
| White House (CAWASH01) | Engineer-capture permission | true | 194 |
| White House (CAWASH01) | Crate Beneath | false | 195 |
| White House (CAWASH01) | Crate Beneath Is Money | true | 196 |
| Washington Monument (CAWSH12) | Name | RA2 Washington Monument | 199 |
| Washington Monument (CAWSH12) | Crate Beneath | false | 200 |
| Washington Monument (CAWSH12) | Crate Beneath Is Money | true | 201 |
| Jefferson Memorial (CAWASH14) | Name | Jefferson Memorial | 204 |
| Jefferson Memorial (CAWASH14) | Crate Beneath | false | 205 |
| Jefferson Memorial (CAWASH14) | Crate Beneath Is Money | true | 206 |
| Jefferson Memorial (CAWASH14) | Infantry garrison permitted | no | 207 |
| Lincoln Memorial (CAWASH15) | Name | RA2 Lincoln Memorial | 210 |
| Lincoln Memorial (CAWASH15) | Crate Beneath | false | 211 |
| Lincoln Memorial (CAWASH15) | Crate Beneath Is Money | true | 212 |
| Smithsonian Castle (CAWASH16) | Name | RA2 Smithsonian Castle | 215 |
| Smithsonian Castle (CAWASH16) | Crate Beneath | false | 216 |
| Smithsonian Castle (CAWASH16) | Crate Beneath Is Money | true | 217 |
| Smithsonian Natural History Museum (CAWASH17) | Name | RA2 Smithsonian Natural History Museum | 220 |
| Smithsonian Natural History Museum (CAWASH17) | Crate Beneath | false | 221 |
| Smithsonian Natural History Museum (CAWASH17) | Crate Beneath Is Money | true | 222 |
| Smithsonian Natural History Museum (CAWASH17) | Infantry garrison permitted | no | 223 |
| Smithsonian Natural History Museum (CAWASH17) | Primary | none | 224 |
| Smithsonian Natural History Museum (CAWASH17) | Secondary | none | 225 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 3300 | 228 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 229 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.40 | 230 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.40 | 231 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.15 | 232 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 1800 | 235 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.001 | 236 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 0.3 | 237 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.05 | 238 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 0.5 | 239 |
| Soviet Shipyard (NAYARD) | Name | Soviet Shipyard | 242 |
| Soviet Shipyard (NAYARD) | Technology level | -1 | 243 |
| Nuclear Reactor (NANRCT) | Technology level | -1 | 246 |
| Desolator (DESO) | Permitted country list | Russians,Confederation,Africans,Arabs | 249 |
| Desolator (DESO) | Required countries | Player | 250 |
| Engineer (ENGINEER) | Technology level | -1 | 253 |
| Attack Dog (ADOG) | Technology level | -1 | 256 |
| Yuri (YURI) | Technology level | -1 | 259 |
| Giant Squid (SQD) | Technology level | -1 | 262 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Bridge1Open,0 | 303 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Bridge2Open,1 | 304 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Bridge3Open,0 | 305 |
| VARIABLENAMES (VARIABLENAMES) | 3 | VladSoldBase,0 | 306 |
