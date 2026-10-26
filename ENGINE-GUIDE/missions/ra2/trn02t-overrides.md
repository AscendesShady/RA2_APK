# Boot Camp - Day 2 - mission overrides and local definitions

[Trigger ledger](trn02t.md) | [Team plans](trn02t-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS01.MIX/trn02t.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| SPECIALFLAGS | Tiberium Grows | no | 2 |
| SPECIALFLAGS | Tiberium Spreads | yes | 3 |
| SPECIALFLAGS | Tiberium Explosive | no | 4 |
| SPECIALFLAGS | Destroyable Bridges | yes | 5 |
| SPECIALFLAGS | MCV Deploy | no | 6 |
| SPECIALFLAGS | Initial Veteran | no | 7 |
| SPECIALFLAGS | Fixed Alliance | no | 8 |
| SPECIALFLAGS | Harvester Immune | no | 9 |
| SPECIALFLAGS | Fog Of War | no | 10 |
| SPECIALFLAGS | Inert | no | 11 |
| SPECIALFLAGS | Ion Storms | no | 12 |
| SPECIALFLAGS | Meteorites | no | 13 |
| SPECIALFLAGS | Visceroids | no | 14 |
| War Miner (HARV) | Resource cargo capacity | 20 | 17 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 20 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 23 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 24 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 25 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 26 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 29 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 32 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 35 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 38 |
| COUNTRIES (COUNTRIES) | 0 | Player | 41 |
| COUNTRIES (COUNTRIES) | 1 | RedTeam | 42 |
| COUNTRIES (COUNTRIES) | 2 | Civilian | 43 |
| COUNTRIES (COUNTRIES) | 3 | Other1 | 44 |
| COUNTRIES (COUNTRIES) | 4 | Other2 | 45 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 3300 | 96 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 97 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.40 | 98 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.40 | 99 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.15 | 100 |
| Engineer (ENGINEER) | Technology level | -1 | 103 |
| Engineer (SENGINEER) | Technology level | -1 | 106 |
| Attack Dog (ADOG) | Technology level | -1 | 109 |
| Attack Dog (DOG) | Technology level | -1 | 112 |
| Allied War Factory (GAWEAP) | Technology level | -1 | 115 |
| Pill Box (GAPILL) | Technology level | -1 | 118 |
| Allied Wall (GAWALL) | Technology level | -1 | 121 |
| Allied Construction Yard (GACNST) | Name | Allied Construction Yard | 124 |
| Allied Construction Yard (GACNST) | Selling forbidden | true | 125 |
| Allied Ore Refinery (GAREFN) | Name | Allied Ore Refinery | 128 |
| Allied Ore Refinery (GAREFN) | Selling forbidden | true | 129 |
| Power Plant (GAPOWR) | Name | Power Plant | 132 |
| Power Plant (GAPOWR) | Selling forbidden | true | 133 |
| Allied Barracks (GAPILE) | Name | Allied Barracks | 136 |
| Allied Barracks (GAPILE) | Required structures/groups | GAPOWR | 137 |
| Allied Barracks (GAPILE) | Selling forbidden | true | 138 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | AI Safe Distance | 8 | 141 |
| VARIABLENAMES (VARIABLENAMES) | 0 | 1stRedTeamWon,0 | 191 |
