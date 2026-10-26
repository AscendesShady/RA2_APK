# Boot Camp - Day 1 - mission overrides and local definitions

[Trigger ledger](trn01t.md) | [Team plans](trn01t-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS01.MIX/trn01t.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | AI Auto Deploy Frame Delay | 10000,10000,10000 | 2 |
| War Miner (HARV) | Resource cargo capacity | 20 | 5 |
| Chrono Miner (CMIN) | Resource cargo capacity | 10 | 8 |
| TIBERIUMS (TIBERIUMS) | 0 | Riparius | 11 |
| TIBERIUMS (TIBERIUMS) | 1 | Cruentus | 12 |
| TIBERIUMS (TIBERIUMS) | 2 | Vinifera | 13 |
| TIBERIUMS (TIBERIUMS) | 3 | Aboreus | 14 |
| Tiberium Riparius (RIPARIUS) | Value | 50 | 17 |
| Tiberium Cruentus (CRUENTUS) | Value | 100 | 20 |
| Tiberium Vinifera (VINIFERA) | Value | 50 | 23 |
| Tiberium Aboreus (ABOREUS) | Value | 50 | 26 |
| Patriot Missile (NASAM) | Name | Patriot Missile | 29 |
| Patriot Missile (NASAM) | Sight radius setting | 7 | 30 |
| Allied War Factory (GAWEAP) | Name | Allied War Factory | 33 |
| Allied War Factory (GAWEAP) | Sight radius setting | 15 | 34 |
| Outhouse (CAFRMB) | Name | RA2 Outhouse | 37 |
| Outhouse (CAFRMB) | Infantry garrison permitted | yes | 38 |
| Outhouse (CAFRMB) | Garrison capacity | 1 | 39 |
| Allied Construction Yard (GACNST) | Name | Allied Construction Yard | 42 |
| Allied Construction Yard (GACNST) | Points | 0 | 43 |
| Allied Construction Yard (GACNST) | Engineer-capture permission | false | 44 |
| Allied Construction Yard (GACNST) | Crewed | no | 45 |
| M60 (M60) | Damage | 25 | 48 |
| M60 (M60) | ROF | 20 | 49 |
| M60 (M60) | Range | 6 | 50 |
| PARA (PARA) | Damage | 15 | 53 |
| PARA (PARA) | ROF | 10 | 54 |
| PARA (PARA) | Range | 8 | 55 |
| PARA (PARA) | Projectile | InvisibleLow | 56 |
| PARA (PARA) | Movement rating | 100 | 57 |
| PARA (PARA) | Warhead | SSA | 58 |
| PARA (PARA) | Report | GIAttackDeployed | 59 |
| Cow (COW) | UI Name | Name:COW | 62 |
| Cow (COW) | Name | Cow | 63 |
| Cow (COW) | Category | Soldier | 64 |
| Cow (COW) | Starting health capacity | 150 | 65 |
| Cow (COW) | Armor class | none | 66 |
| Cow (COW) | Technology level | -1 | 67 |
| Cow (COW) | Can be crushed | no | 68 |
| Cow (COW) | Insignificant-object flag | no | 69 |
| Cow (COW) | Can garrison buildings | yes | 70 |
| Cow (COW) | Sight radius setting | 4 | 71 |
| Cow (COW) | Movement rating | 4 | 72 |
| Cow (COW) | Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | 73 |
| Cow (COW) | Allowed To Start In Multiplayer | yes | 74 |
| Cow (COW) | Price in credits | 10 | 75 |
| Cow (COW) | Recycling value setting | 2000 | 76 |
| Cow (COW) | Points | 1 | 77 |
| Cow (COW) | Fraidycat | yes | 78 |
| Cow (COW) | Civilian | no | 79 |
| Cow (COW) | Nominal | no | 80 |
| Cow (COW) | Pip | green | 81 |
| Cow (COW) | Voice Select | CowSelect | 82 |
| Cow (COW) | Voice Move | CowMove | 83 |
| Cow (COW) | Voice Attack | CowMove | 84 |
| Cow (COW) | Voice Feedback | CowFear | 85 |
| Cow (COW) | Voice Die | CowDie | 86 |
| Cow (COW) | Locomotor | {4A582744-9839-11d1-B709-00A024DDAFD1} | 87 |
| Cow (COW) | Physical Size | 1 | 88 |
| Cow (COW) | Permitted movement zone | Infantry | 89 |
| Cow (COW) | Threat contribution | 0 | 90 |
| Cow (COW) | Immune To Veins | yes | 91 |
| Cow (COW) | Transport size usage | 1 | 92 |
| SPECIALFLAGS | Tiberium Grows | no | 95 |
| SPECIALFLAGS | Tiberium Spreads | yes | 96 |
| SPECIALFLAGS | Tiberium Explosive | no | 97 |
| SPECIALFLAGS | Destroyable Bridges | yes | 98 |
| SPECIALFLAGS | MCV Deploy | no | 99 |
| SPECIALFLAGS | Initial Veteran | no | 100 |
| SPECIALFLAGS | Fixed Alliance | no | 101 |
| SPECIALFLAGS | Harvester Immune | no | 102 |
| SPECIALFLAGS | Fog Of War | no | 103 |
| SPECIALFLAGS | Inert | no | 104 |
| SPECIALFLAGS | Ion Storms | no | 105 |
| SPECIALFLAGS | Meteorites | no | 106 |
| SPECIALFLAGS | Visceroids | no | 107 |
| COUNTRIES (COUNTRIES) | 0 | Player | 110 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 111 |
| COUNTRIES (COUNTRIES) | 2 | BadGuy2 | 112 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 113 |
| COUNTRIES (COUNTRIES) | 4 | Civilian1 | 114 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 115 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 116 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 117 |
| VARIABLENAMES (VARIABLENAMES) | 0 | Engineer Landed,0 | 246 |
| VARIABLENAMES (VARIABLENAMES) | 1 | Helicopter Leaves,0 | 247 |
| VARIABLENAMES (VARIABLENAMES) | 2 | Annoyed,0 | 248 |
| VARIABLENAMES (VARIABLENAMES) | 3 | Annoyed_Again,0 | 249 |
| VARIABLENAMES (VARIABLENAMES) | 4 | Near Target,0 | 250 |
| VARIABLENAMES (VARIABLENAMES) | 5 | Far Target,0 | 251 |
