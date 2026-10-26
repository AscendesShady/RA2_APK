# Operation: City of Lights - mission overrides and local definitions

[Trigger ledger](sov05u.md) | [Team plans](sov05u-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov05u.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| War Miner (HARV) | Resource cargo capacity | 20 | 11 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 14 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 17 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 18 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 19 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 20 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 23 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 26 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 29 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 32 |
| Invisible Light Post (INGALITE) | Name | Invisible Light Post | 35 |
| Invisible Light Post (INGALITE) | Local light reach | 4000 | 36 |
| Invisible Light Post (INGALITE) | Local light intensity | 0.01 | 37 |
| Invisible Light Post (INGALITE) | Light Red Tint | 0.5 | 38 |
| Invisible Light Post (INGALITE) | Light Green Tint | 0.5 | 39 |
| Invisible Light Post (INGALITE) | Light Blue Tint | 0.5 | 40 |
| Invisible Yellow Light Post (INYELWLAMP) | Name | Invisible Yellow Light Post | 43 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 4000 | 44 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 45 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.5 | 46 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.5 | 47 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.0 | 48 |
| Invisible Purple Light Post (INPURPLAMP) | Name | Invisible Purple Light Post | 51 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 4000 | 52 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.01 | 53 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 1.5 | 54 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.01 | 55 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 0.01 | 56 |
| Invisible Green Light Post (INGRNLMP) | Name | Invisible Green Light Post | 59 |
| Invisible Green Light Post (INGRNLMP) | Local light reach | 4000 | 60 |
| Invisible Green Light Post (INGRNLMP) | Local light intensity | 0.01 | 61 |
| Invisible Green Light Post (INGRNLMP) | Light Red Tint | 1.5 | 62 |
| Invisible Green Light Post (INGRNLMP) | Light Green Tint | 0.01 | 63 |
| Invisible Green Light Post (INGRNLMP) | Light Blue Tint | 0.01 | 64 |
| Invisible Red Light Post (INREDLMP) | Name | Invisible Red Light Post | 67 |
| Invisible Red Light Post (INREDLMP) | Local light reach | 2000 | 68 |
| Invisible Red Light Post (INREDLMP) | Local light intensity | 0.01 | 69 |
| Invisible Red Light Post (INREDLMP) | Light Red Tint | 0.4 | 70 |
| Invisible Red Light Post (INREDLMP) | Light Green Tint | 0.2 | 71 |
| Invisible Red Light Post (INREDLMP) | Light Blue Tint | 0.01 | 72 |
| Invisible Blue Light Post (INBLULMP) | Name | Invisible Blue Light Post | 75 |
| Invisible Blue Light Post (INBLULMP) | Local light reach | 3000 | 76 |
| Invisible Blue Light Post (INBLULMP) | Local light intensity | 0.01 | 77 |
| Invisible Blue Light Post (INBLULMP) | Light Red Tint | 0.01 | 78 |
| Invisible Blue Light Post (INBLULMP) | Light Green Tint | 0,01 | 79 |
| Invisible Blue Light Post (INBLULMP) | Light Blue Tint | 0.7 | 80 |
| Crazy Ivan (IVAN) | Name | Crazy Ivan | 83 |
| Crazy Ivan (IVAN) | Required structures/groups | NAHAND | 84 |
| Engineer (ENGINEER) | Name | Engineer | 87 |
| Engineer (ENGINEER) | Technology level | -1 | 88 |
| Attack Dog (ADOG) | Name | Allied Attack Dog | 91 |
| Attack Dog (ADOG) | Technology level | -1 | 92 |
| Barrels (CAMISC01) | Name | RA2 Barrels | 95 |
| Barrels (CAMISC01) | Starting health capacity | 2 | 96 |
| Barrel (CAMISC02) | Name | RA2 Barrel | 99 |
| Barrel (CAMISC02) | Starting health capacity | 1 | 100 |
| BARRELEXPLOSION (BARRELEXPLOSION) | Projectile | Invisible | 103 |
| BARRELEXPLOSION (BARRELEXPLOSION) | Damage | 50 | 104 |
| BARRELEXPLOSION (BARRELEXPLOSION) | Warhead | OilExplosionWH | 105 |
| BARRELEXPLOSION (BARRELEXPLOSION) | Anim | RING1 | 106 |
| Pickup Truck (PICK) | Name | Pickup Truck | 109 |
| Pickup Truck (PICK) | Category | Support | 110 |
| Pickup Truck (PICK) | Passenger slot capacity | 0 | 111 |
| Pickup Truck (PICK) | Can crush through ordinary crushing logic | no | 112 |
| Soviet Barracks (NAHAND) | Name | Soviet Barracks | 115 |
| Soviet Barracks (NAHAND) | Signed power contribution | 0 | 116 |
| Tesla Coil (TESLA) | Name | Tesla Coil | 119 |
| Tesla Coil (TESLA) | Signed power contribution | 0 | 120 |
| Paris Tower (CAPARS01) | UI Name | Name:CAPARS01 | 123 |
| Paris Tower (CAPARS01) | Name | RA2 Paris Tower | 124 |
| Paris Tower (CAPARS01) | Technology level | -1 | 125 |
| Paris Tower (CAPARS01) | Starting health capacity | 30000 | 126 |
| Paris Tower (CAPARS01) | Insignificant-object flag | yes | 127 |
| Paris Tower (CAPARS01) | Nominal | yes | 128 |
| Paris Tower (CAPARS01) | Hidden from radar | no | 129 |
| Paris Tower (CAPARS01) | Points | 5 | 130 |
| Paris Tower (CAPARS01) | Armor class | concrete | 131 |
| Paris Tower (CAPARS01) | Explosion | TWLT070,S_BANG48,S_BRNL58,S_CLSN58,S_TUMU60 | 132 |
| Paris Tower (CAPARS01) | Max Debris | 0 | 133 |
| Paris Tower (CAPARS01) | Normal base-adjacency role | no | 134 |
| Paris Tower (CAPARS01) | Primary | EiffelBolt | 135 |
| Paris Tower (CAPARS01) | Signed power contribution | -100 | 136 |
| Paris Tower (CAPARS01) | Depends on power | Yes | 137 |
| Paris Tower (CAPARS01) | Overpowerable | true | 138 |
| Paris Tower (CAPARS01) | Attached bombs permitted | no | 139 |
| SPECIALFLAGS | Tiberium Grows | no | 142 |
| SPECIALFLAGS | Tiberium Spreads | yes | 143 |
| SPECIALFLAGS | Tiberium Explosive | no | 144 |
| SPECIALFLAGS | Destroyable Bridges | no | 145 |
| SPECIALFLAGS | MCV Deploy | no | 146 |
| SPECIALFLAGS | Initial Veteran | no | 147 |
| SPECIALFLAGS | Fixed Alliance | no | 148 |
| SPECIALFLAGS | Harvester Immune | no | 149 |
| SPECIALFLAGS | Fog Of War | no | 150 |
| SPECIALFLAGS | Inert | no | 151 |
| SPECIALFLAGS | Ion Storms | no | 152 |
| SPECIALFLAGS | Meteorites | no | 153 |
| SPECIALFLAGS | Visceroids | no | 154 |
| COUNTRIES (COUNTRIES) | 0 | Player | 157 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 158 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 159 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 160 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 161 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 162 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 163 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 164 |
