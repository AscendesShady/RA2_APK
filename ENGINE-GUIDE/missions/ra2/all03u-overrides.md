# Operation: Hail to the Chief - mission overrides and local definitions

[Trigger ledger](all03u.md) | [Team plans](all03u-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS01.MIX/all03u.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 2900,1600,1000 | 11 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 5000 | 12 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -5000 | 13 |
| CRATERULES (CRATERULES) | Solo Crate Money | 2000 | 16 |
| War Miner (HARV) | Resource cargo capacity | 20 | 19 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 22 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 25 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 26 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 27 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 28 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 31 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 34 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 37 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 40 |
| SPECIALFLAGS | Tiberium Grows | yes | 43 |
| SPECIALFLAGS | Tiberium Spreads | yes | 44 |
| SPECIALFLAGS | Tiberium Explosive | no | 45 |
| SPECIALFLAGS | Destroyable Bridges | yes | 46 |
| SPECIALFLAGS | MCV Deploy | yes | 47 |
| SPECIALFLAGS | Initial Veteran | no | 48 |
| SPECIALFLAGS | Fixed Alliance | no | 49 |
| SPECIALFLAGS | Harvester Immune | no | 50 |
| SPECIALFLAGS | Fog Of War | no | 51 |
| SPECIALFLAGS | Inert | no | 52 |
| SPECIALFLAGS | Ion Storms | no | 53 |
| SPECIALFLAGS | Meteorites | no | 54 |
| SPECIALFLAGS | Visceroids | no | 55 |
| COUNTRIES (COUNTRIES) | 0 | Player | 58 |
| COUNTRIES (COUNTRIES) | 1 | Russian1 | 59 |
| COUNTRIES (COUNTRIES) | 2 | Russian2 | 60 |
| COUNTRIES (COUNTRIES) | 3 | CivilianArmy | 61 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 62 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 63 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 64 |
| COUNTRIES (COUNTRIES) | 7 | Civilian2 | 65 |
| Engineer (SENGINEER) | Technology level | -1 | 145 |
| Attack Dog (DOG) | Technology level | -1 | 148 |
| Technician (CTECH) | Primary | Pistola | 151 |
| Technician (CTECH) | Insignificant-object flag | no | 152 |
| Technician (CTECH) | Ammo | 50 | 153 |
| Technician (CTECH) | Reload | 80 | 154 |
| Tesla Trooper (SHK) | Name | Shock Trooper | 157 |
| Tesla Trooper (SHK) | Technology level | 3 | 158 |
| Civilian (CIVA) | Name | Civilian Texan A | 161 |
| Civilian (CIVA) | Insignificant-object flag | no | 162 |
| Civilian (CIVB) | Name | Civilian Texan B | 165 |
| Civilian (CIVB) | Insignificant-object flag | no | 166 |
| Civilian (CIVC) | Name | Civilian Texan C | 169 |
| Civilian (CIVC) | Insignificant-object flag | no | 170 |
| Civilian (CIVSFM) | Name | Civilian Snow Fat Male | 173 |
| Civilian (CIVSFM) | Insignificant-object flag | no | 174 |
| Civilian (CIVSF) | Name | Civilian Snow Female | 177 |
| Civilian (CIVSF) | Insignificant-object flag | no | 178 |
| Civilian (CIVSTM) | Name | Civilian Snow Thin Male | 181 |
| Civilian (CIVSTM) | Insignificant-object flag | no | 182 |
| Secret Service (SSRV) | Name | Secret Service | 185 |
| Secret Service (SSRV) | Fraidycat | no | 186 |
| President (PRES) | Name | President | 189 |
| President (PRES) | Fraidycat | no | 190 |
| PISTOLA (PISTOLA) | Damage | 7 | 193 |
| PISTOLA (PISTOLA) | ROF | 25 | 194 |
| PISTOLA (PISTOLA) | Range | 3 | 195 |
| PISTOLA (PISTOLA) | Projectile | InvisibleLow | 196 |
| PISTOLA (PISTOLA) | Movement rating | 100 | 197 |
| PISTOLA (PISTOLA) | Warhead | SA | 198 |
| PISTOLA (PISTOLA) | Report | CivAttack | 199 |
| Psychic Beacon (NAPSYB) | Name | RA2 Psychic Beacon | 202 |
| Psychic Beacon (NAPSYB) | Starting health capacity | 1000 | 203 |
| Psychic Beacon (NAPSYB) | Armor class | wood | 204 |
| Psychic Beacon (NAPSYB) | Engineer-capture permission | false | 205 |
| Psychic Beacon (NAPSYB) | Crewed | no | 206 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 2400 | 209 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 210 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.40 | 211 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.40 | 212 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.15 | 213 |
| Invisible Red Light Post (INREDLMP) | Local light reach | 2400 | 216 |
| Invisible Red Light Post (INREDLMP) | Local light intensity | 0.02 | 217 |
| Invisible Red Light Post (INREDLMP) | Light Red Tint | 1.0 | 218 |
| Invisible Red Light Post (INREDLMP) | Light Green Tint | 0.40 | 219 |
| Invisible Red Light Post (INREDLMP) | Light Blue Tint | 0.20 | 220 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 1700 | 223 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.001 | 224 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 0.3 | 225 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.05 | 226 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 0.5 | 227 |
| InvisibleSnowNightLamp (SNONITLAMP) | Name | InvisibleSnowNightLamp | 230 |
| InvisibleSnowNightLamp (SNONITLAMP) | Local light reach | 1700 | 231 |
| InvisibleSnowNightLamp (SNONITLAMP) | Local light intensity | 0.01 | 232 |
| InvisibleSnowNightLamp (SNONITLAMP) | Light Red Tint | 0.15 | 233 |
| InvisibleSnowNightLamp (SNONITLAMP) | Light Green Tint | 0.25 | 234 |
| InvisibleSnowNightLamp (SNONITLAMP) | Light Blue Tint | 0.05 | 235 |
| White House (CAWASH01) | Name | RA2 White House | 238 |
| White House (CAWASH01) | Crate Beneath | false | 239 |
| White House (CAWASH01) | Infantry garrison permitted | no | 240 |
| Washington Monument (CAWSH12) | Name | RA2 Washington Monument | 243 |
| Washington Monument (CAWSH12) | Crate Beneath | false | 244 |
| Jefferson Memorial (CAWASH14) | Crate Beneath | false | 247 |
| Lincoln Memorial (CAWASH15) | Crate Beneath | false | 250 |
| Smithsonian Castle (CAWASH16) | Crate Beneath | false | 253 |
| Smithsonian Natural History Museum (CAWASH17) | Name | RA2 Smithsonian Natural History Museum | 256 |
| Smithsonian Natural History Museum (CAWASH17) | Crate Beneath | false | 257 |
| Smithsonian Natural History Museum (CAWASH17) | Crate Beneath Is Money | true | 258 |
| Smithsonian Natural History Museum (CAWASH17) | Infantry garrison permitted | no | 259 |
| Smithsonian Natural History Museum (CAWASH17) | Primary | none | 260 |
| Smithsonian Natural History Museum (CAWASH17) | Secondary | none | 261 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Bridge1Open,1 | 302 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Bridge2Open,1 | 303 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Bridge3Open,1 | 304 |
| VARIABLENAMES (VARIABLENAMES) | 3 | BackBridgeOpen,1 | 305 |
| VARIABLENAMES (VARIABLENAMES) | 4 | IFVRepaired,0 | 306 |
