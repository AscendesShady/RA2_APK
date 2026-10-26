# Operation: Big Apple - mission overrides and local definitions

[Trigger ledger](sov03u.md) | [Team plans](sov03u-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov03u.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Deferment | 1 | 11 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Damage | 1 | 12 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Storm Duration | 200 | 13 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Warhead | IonWH | 14 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Hit Delay | 40000 | 15 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Scatter Delay | 40000 | 16 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Cell Spread | 1 | 17 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Lightning Print Text | no | 18 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Ion Storms | no | 19 |
| AUDIOVISUAL (AUDIOVISUAL) | Storm Sound | ChronoLegionAttack | 22 |
| AUDIOVISUAL (AUDIOVISUAL) | Lightning Sounds | ChronoLegionAttack | 23 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | UI Name | Name:Storm | 26 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Name | Lightning Storm | 27 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Is Powered | true | 28 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Recharge Time | 10 | 29 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Type | LightningStorm | 30 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Action | LightningStorm | 31 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Sidebar Image | BOLTICON | 32 |
| Weather Storm (LIGHTNINGSTORMSPECIAL) | Show Timer | no | 33 |
| Truck (loaded) (TRUCKB) | Immune to ordinary psychic control | yes | 36 |
| Truck (loaded) (TRUCKB) | Insignificant-object flag | yes | 37 |
| Pickup Truck (PTRUCK) | Immune to ordinary psychic control | yes | 40 |
| Pickup Truck (PTRUCK) | Insignificant-object flag | yes | 41 |
| Taxi (TAXI) | Immune to ordinary psychic control | yes | 44 |
| Taxi (TAXI) | Insignificant-object flag | yes | 45 |
| Automobile (SUVW) | Immune to ordinary psychic control | yes | 48 |
| Automobile (SUVW) | Insignificant-object flag | yes | 49 |
| Automobile (SUVB) | Immune to ordinary psychic control | yes | 52 |
| Automobile (SUVB) | Insignificant-object flag | yes | 53 |
| Automobile (STANG) | Immune to ordinary psychic control | yes | 56 |
| Automobile (STANG) | Insignificant-object flag | yes | 57 |
| Automobile (EUROC) | Immune to ordinary psychic control | yes | 60 |
| Automobile (EUROC) | Insignificant-object flag | yes | 61 |
| Excavator (CONA) | Immune to ordinary psychic control | yes | 64 |
| Excavator (CONA) | Insignificant-object flag | yes | 65 |
| Automobile (CAR) | Immune to ordinary psychic control | yes | 68 |
| Automobile (CAR) | Insignificant-object flag | yes | 69 |
| War Miner (HARV) | Resource cargo capacity | 20 | 72 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 75 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 78 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 79 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 80 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 81 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 84 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 87 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 90 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 93 |
| Tesla Coil (TESLA) | Technology level | 6 | 96 |
| Flak Cannon (NAFLAK) | Technology level | 6 | 99 |
| Terror Drone (DRON) | Technology level | 6 | 102 |
| Amphibious Transport (SAPC) | Technology level | 5 | 105 |
| Crazy Ivan (IVAN) | Name | Crazy Ivan | 108 |
| Crazy Ivan (IVAN) | Technology level | 6 | 109 |
| Yuri (YURI) | UI Name | Name:PTROOP | 112 |
| Engineer (ENGINEER) | Name | Engineer | 115 |
| Engineer (ENGINEER) | Technology level | -1 | 116 |
| Attack Dog (ADOG) | Name | Allied Attack Dog | 119 |
| Attack Dog (ADOG) | Technology level | -1 | 120 |
| Rocketeer (JUMPJET) | Name | Rocketeer | 123 |
| Rocketeer (JUMPJET) | Technology level | -1 | 124 |
| Harrier (ORCA) | Name | Intruder | 127 |
| Harrier (ORCA) | Technology level | -1 | 128 |
| Patriot Missile (NASAM) | Name | Patriot Missile | 131 |
| Patriot Missile (NASAM) | Technology level | -1 | 132 |
| Air Force Command Headquarters (GAAIRC) | Name | Airforce Command Headquarters | 135 |
| Air Force Command Headquarters (GAAIRC) | Technology level | -1 | 136 |
| Psychic Sensor (NAPSIS) | Name | Psychic Sensor | 139 |
| Psychic Sensor (NAPSIS) | Technology level | -1 | 140 |
| Allied Battle Lab (GATECH) | UI Name | Name:GATECH | 143 |
| Allied Battle Lab (GATECH) | Name | Allied Battle Lab | 144 |
| Allied Battle Lab (GATECH) | Construction category | Tech | 145 |
| Allied Battle Lab (GATECH) | Required structures/groups | GAWEAP,RADAR | 146 |
| Allied Battle Lab (GATECH) | Starting health capacity | 500 | 147 |
| Allied Battle Lab (GATECH) | Armor class | wood | 148 |
| Allied Battle Lab (GATECH) | Technology level | 8 | 149 |
| Allied Battle Lab (GATECH) | Placement adjacency setting | 2 | 150 |
| Allied Battle Lab (GATECH) | Sight radius setting | 6 | 151 |
| Allied Battle Lab (GATECH) | Permitted country list | British,French,Germans,Americans,Alliance | 152 |
| Allied Battle Lab (GATECH) | Price in credits | 2000 | 153 |
| Allied Battle Lab (GATECH) | Points | 85 | 154 |
| Allied Battle Lab (GATECH) | Signed power contribution | -100 | 155 |
| Allied Battle Lab (GATECH) | Engineer-capture permission | true | 156 |
| Allied Battle Lab (GATECH) | Crewed | no | 157 |
| Allied Battle Lab (GATECH) | Explosion | TWLT070,S_BANG48,S_BRNL58,S_CLSN58,S_TUMU60 | 158 |
| Allied Battle Lab (GATECH) | Max Debris | 5 | 159 |
| Allied Battle Lab (GATECH) | Threat contribution | 0 | 160 |
| Allied Battle Lab (GATECH) | Damage Particle Systems | SparkSys,SmallGreySSys,BigGreySmokeSys | 161 |
| Allied Battle Lab (GATECH) | Damage Smoke Offset | 1500, 1055, 815 | 162 |
| Allied Battle Lab (GATECH) | AI Build This | yes | 163 |
| Allied Battle Lab (GATECH) | Player power toggle allowed | no | 164 |
| Allied Battle Lab (GATECH) | Spy-infiltration permission | yes | 165 |
| Allied Battle Lab (GATECH) | Protect With Wall | yes | 166 |
| Psychic Beacon (NAPSYB) | Name | RA2 Psychic Beacon | 169 |
| Psychic Beacon (NAPSYB) | Construction category | Combat | 170 |
| Psychic Beacon (NAPSYB) | Required structures/groups | NATECH | 171 |
| Psychic Beacon (NAPSYB) | Starting health capacity | 2500 | 172 |
| Psychic Beacon (NAPSYB) | Armor class | wood | 173 |
| Psychic Beacon (NAPSYB) | Technology level | 10 | 174 |
| Psychic Beacon (NAPSYB) | Placement adjacency setting | 2 | 175 |
| Psychic Beacon (NAPSYB) | Sight radius setting | 10 | 176 |
| Psychic Beacon (NAPSYB) | Permitted country list | Russians,Confederation,Africans,Arabs | 177 |
| Psychic Beacon (NAPSYB) | Price in credits | 50 | 178 |
| Psychic Beacon (NAPSYB) | Points | 50 | 179 |
| Psychic Beacon (NAPSYB) | Signed power contribution | 100 | 180 |
| Psychic Beacon (NAPSYB) | Depends on power | true | 181 |
| Psychic Beacon (NAPSYB) | Engineer-capture permission | true | 182 |
| Psychic Beacon (NAPSYB) | Crewed | no | 183 |
| Psychic Beacon (NAPSYB) | Explosion | TWLT070,S_BANG48,S_BRNL58,S_CLSN58,S_TUMU60 | 184 |
| Psychic Beacon (NAPSYB) | Max Debris | 3 | 185 |
| Psychic Beacon (NAPSYB) | Threat contribution | 0 | 186 |
| Psychic Beacon (NAPSYB) | Damage Particle Systems | SparkSys,SmallGreySSys,BigGreySmokeSys | 187 |
| Psychic Beacon (NAPSYB) | Damage Smoke Offset | 220, 390, 150 | 188 |
| Psychic Beacon (NAPSYB) | AI Build This | no | 189 |
| Psychic Beacon (NAPSYB) | Has Radial Indicator | true | 190 |
| Psychic Beacon (NAPSYB) | Detect Disguise | yes | 191 |
| Tech Outpost (CAOUTP) | Name | Tech Outpost | 194 |
| Tech Outpost (CAOUTP) | Insignificant-object flag | yes | 195 |
| Tech Oil Derrick (CAOILD) | Name | Tech Oil Derrick | 198 |
| Tech Oil Derrick (CAOILD) | Explosive destruction flag | no | 199 |
| Soviet Shipyard (NAYARD) | Name | Soviet Shipyard | 202 |
| Soviet Shipyard (NAYARD) | Technology level | -1 | 203 |
| Allied Shipyard (GAYARD) | Name | Soviet Shipyard | 206 |
| Allied Shipyard (GAYARD) | Technology level | -1 | 207 |
| World Trade Center (CANEWY05) | Name | RA2 World Trade Center | 210 |
| World Trade Center (CANEWY05) | Whole-map reveal service | no | 211 |
| SPECIALFLAGS | Tiberium Grows | no | 214 |
| SPECIALFLAGS | Tiberium Spreads | yes | 215 |
| SPECIALFLAGS | Tiberium Explosive | no | 216 |
| SPECIALFLAGS | Destroyable Bridges | no | 217 |
| SPECIALFLAGS | MCV Deploy | no | 218 |
| SPECIALFLAGS | Initial Veteran | no | 219 |
| SPECIALFLAGS | Fixed Alliance | no | 220 |
| SPECIALFLAGS | Harvester Immune | no | 221 |
| SPECIALFLAGS | Fog Of War | no | 222 |
| SPECIALFLAGS | Inert | no | 223 |
| SPECIALFLAGS | Ion Storms | no | 224 |
| SPECIALFLAGS | Meteorites | no | 225 |
| SPECIALFLAGS | Visceroids | no | 226 |
| COUNTRIES (COUNTRIES) | 0 | Player | 229 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 230 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 231 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 232 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 233 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 234 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 235 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 236 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Stop_Looping,0 | 356 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Play Yuri Movie,0 | 357 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Play Yuri Audio,0 | 358 |
