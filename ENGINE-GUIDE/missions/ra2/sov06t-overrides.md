# Operation: Sub-Divide - mission overrides and local definitions

[Trigger ledger](sov06t.md) | [Team plans](sov06t-teams.md) | [Campaign guide](../../05-CAMPAIGNS.md)

Each row is explicitly written in this map. It replaces/adds that property for the scenario; properties absent here continue to come from the effective rules/defaults. This table includes matching common-rule/weapon/terrain sections and new registered type definitions, but excludes map-placement data, packed art/terrain blocks and trigger/team sections translated in the companions. It is a property reference, not a claim to have decoded every packed map field. Source: MAPS02.MIX/sov06t.map.

| Object/system | Property | Mission value | Source line |
| --- | --- | --- | --- |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Team Delays | 3500,1800,900 | 11 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Easy | 5000 | 12 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Campaign Money Delta Hard | -5000 | 13 |
| Red Alert 2 -- Official Rules of Engagement (GENERAL) | Total AI Team Cap | 20,20,20 | 14 |
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
| SPECIALFLAGS | Tiberium Grows | yes | 41 |
| SPECIALFLAGS | Tiberium Spreads | yes | 42 |
| SPECIALFLAGS | Tiberium Explosive | no | 43 |
| SPECIALFLAGS | Destroyable Bridges | no | 44 |
| SPECIALFLAGS | MCV Deploy | no | 45 |
| SPECIALFLAGS | Initial Veteran | no | 46 |
| SPECIALFLAGS | Fixed Alliance | no | 47 |
| SPECIALFLAGS | Harvester Immune | no | 48 |
| SPECIALFLAGS | Fog Of War | no | 49 |
| SPECIALFLAGS | Inert | no | 50 |
| SPECIALFLAGS | Ion Storms | no | 51 |
| SPECIALFLAGS | Meteorites | no | 52 |
| SPECIALFLAGS | Visceroids | no | 53 |
| COUNTRIES (COUNTRIES) | 0 | Player | 56 |
| COUNTRIES (COUNTRIES) | 1 | BadGuy1 | 57 |
| COUNTRIES (COUNTRIES) | 2 | KoreanFleet | 58 |
| COUNTRIES (COUNTRIES) | 3 | BadGuy3 | 59 |
| COUNTRIES (COUNTRIES) | 4 | Neutral | 60 |
| COUNTRIES (COUNTRIES) | 5 | Other1 | 61 |
| COUNTRIES (COUNTRIES) | 6 | Other2 | 62 |
| COUNTRIES (COUNTRIES) | 7 | Other3 | 63 |
| Civilian (NEUTRAL) | Parent Country | Neutral | 106 |
| Civilian (NEUTRAL) | Name | Neutral | 107 |
| Civilian (NEUTRAL) | Suffix | CIV | 108 |
| Civilian (NEUTRAL) | Prefix | C | 109 |
| Civilian (NEUTRAL) | Color | Grey | 110 |
| Civilian (NEUTRAL) | Multiplay Passive | true | 111 |
| Civilian (NEUTRAL) | Smart AI | yes | 112 |
| Civilian (NEUTRAL) | Side | Civilian | 113 |
| CRATERULES (CRATERULES) | Solo Crate Money | 5000 | 143 |
| CRATERULES (CRATERULES) | Wood Crate | Money | 144 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light reach | 1500 | 147 |
| Invisible Yellow Light Post (INYELWLAMP) | Local light intensity | 0.01 | 148 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Red Tint | 0.50 | 149 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Green Tint | 0.20 | 150 |
| Invisible Yellow Light Post (INYELWLAMP) | Light Blue Tint | 0.02 | 151 |
| Invisible Purple Light Post (INPURPLAMP) | Local light reach | 1500 | 154 |
| Invisible Purple Light Post (INPURPLAMP) | Local light intensity | 0.01 | 155 |
| Invisible Purple Light Post (INPURPLAMP) | Light Red Tint | 1.0 | 156 |
| Invisible Purple Light Post (INPURPLAMP) | Light Green Tint | 0.005 | 157 |
| Invisible Purple Light Post (INPURPLAMP) | Light Blue Tint | 1.0 | 158 |
| Soviet Battle Lab (NATECH) | Technology level | -1 | 161 |
| Amphibious Transport (LCRF) | Name | Landing Craft | 164 |
| Amphibious Transport (LCRF) | Deploy Time | .022 | 165 |
| Amphibious Transport (LCRF) | Leadership Rating | 10 | 166 |
| Crazy Ivan (IVAN) | Technology level | -1 | 169 |
| Engineer (ENGINEER) | Technology level | -1 | 172 |
| Attack Dog (ADOG) | Technology level | -1 | 175 |
| Soviet Construction Vehicle (SMCV) | Name | Soviet Construction Vehicle | 178 |
| Soviet Construction Vehicle (SMCV) | Technology level | 6 | 179 |
| Harrier (ORCA) | Name | Intruder | 182 |
| Harrier (ORCA) | Can Passive Aquire | no | 183 |
| Harrier (ORCA) | Can Retaliate | no | 184 |
| Harrier (ORCA) | Sight radius setting | 8 | 185 |
| Harrier (ORCA) | Guard Range | 0 | 186 |
| VARIABLENAMES (VARIABLENAMES) | 0 | TransportArrived,0 | 227 |
| VARIABLENAMES (VARIABLENAMES) | 1 | TransportsUnloaded,0 | 228 |
| VARIABLENAMES (VARIABLENAMES) | 2 | TransportArrived2,0 | 229 |
| VARIABLENAMES (VARIABLENAMES) | 3 | TransportUnloaded2,0 | 230 |
| VARIABLENAMES (VARIABLENAMES) | 4 | AirHarrassArrived,0 | 231 |
| VARIABLENAMES (VARIABLENAMES) | 5 | TransportArrived1,0 | 232 |
| VARIABLENAMES (VARIABLENAMES) | 6 | DreadsHome,0 | 233 |
