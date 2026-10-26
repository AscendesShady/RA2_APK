# Every mobile piece: infantry, vehicles, ships and aircraft

[Guide index](README.md) | [Engine workflow](01-ENGINE-WORKFLOW.md)

A catalogue entry is not a promise that you can construct it. This book covers every distinct registered type in either effective ruleset, including scenery, hidden/dormant records and weapon-managed objects. The same ID can change role between RA2 and Yuri. Campaign-only additions are listed at the end. Missing properties stay unspecified; a missing permission is not silently treated as yes or no.

Each card gives an ordinary-language workflow, then explicit rule settings. Workflows apply when the object is active and the relevant orders are legal; special map scripts can intervene. Numeric movement/sight/range settings are game units; delays are not automatically wall-clock seconds. For the shared firing procedure see [Combat](03-COMBAT-ECONOMY.md).

## Reading an IFV

1. Start empty: the IFV uses its default weapon.
2. Load an infantry passenger.
3. Read that passenger's IFV mode, which chooses the configured vehicle role.
4. Use that mode's vehicle weapon rather than assuming the passenger fires the ordinary hand-held weapon.
5. Unload to return to the default configuration.

A Battle Fortress uses a different open-topped mechanism: eligible passengers contribute their own fire while carried. Neither mechanism makes all transport slots interchangeable.

## Type index

[GI (E1)](#e1), [Conscript (E2)](#e2), [Tesla Trooper (SHK)](#shk), [Engineer (ENGINEER)](#engineer), [Rocketeer (JUMPJET)](#jumpjet), [SEAL (GHOST)](#ghost), [Yuri Clone (YURI)](#yuri), [Crazy Ivan (IVAN)](#ivan), [Desolator (DESO)](#deso), [Attack Dog (DOG)](#dog), [Civilian (CIV1)](#civ1), [Civilian (CIV2)](#civ2), [Civilian (CIV3)](#civ3), [Technician (CTECH)](#ctech), [Chem Spray Infantry (WEEDGUY)](#weedguy), [Chrono Legionnaire (CLEG)](#cleg), [Spy (SPY)](#spy), [Chrono Commando (CCOMAND)](#ccomand), [Psi Commando (PTROOP)](#ptroop), [Chrono Ivan (CIVAN)](#civan), [Yuri Prime (YURIPR)](#yuripr), [Sniper (SNIPE)](#snipe), [Cow (COW)](#cow), [Alligator (ALL)](#all), [Tanya (TANY)](#tany), [Flak Trooper (FLAKT)](#flakt), [Terrorist (TERROR)](#terror), [Engineer (SENGINEER)](#sengineer), [Attack Dog (ADOG)](#adog), [Civilian (VLADIMIR)](#vladimir), [Civilian (PENTGEN)](#pentgen), [President (PRES)](#pres), [Secret Service (SSRV)](#ssrv), [Civilian (CIVA)](#civa), [Civilian (CIVB)](#civb), [Civilian (CIVC)](#civc), [Civilian (CIVBBP)](#civbbp), [Civilian (CIVBFM)](#civbfm), [Civilian (CIVBF)](#civbf), [Civilian (CIVBTM)](#civbtm), [Civilian (CIVSFM)](#civsfm), [Civilian (CIVSF)](#civsf), [Civilian (CIVSTM)](#civstm), [Polar Bear (POLARB)](#polarb), [Monkey (JOSH)](#josh), [Allied Construction Vehicle (AMCV)](#amcv), [War Miner (HARV)](#harv), [Apocalypse (APOC)](#apoc), [Rhino Heavy Tank (HTNK)](#htnk), [Amphibious Transport (SAPC)](#sapc), [Automobile (CAR)](#car), [School Bus (BUS)](#bus), [Recreational Vehicle (WINI)](#wini), [Pickup Truck (PICK)](#pick), [Grizzly Battle Tank (MTNK)](#mtnk), [War Miner (HORV)](#horv), [Truck (TRUCKA)](#trucka), [Truck (loaded) (TRUCKB)](#truckb), [Aircraft Carrier (CARRIER)](#carrier), [V3 Launcher (V3)](#v3), [Kirov Airship (ZEP)](#zep), [Terror Drone (DRON)](#dron), [Flak Track (HTK)](#htk), [Destroyer (DEST)](#dest), [Typhoon Attack Sub (SUB)](#sub), [Aegis Cruiser (AEGIS)](#aegis), [Amphibious Transport (LCRF)](#lcrf), [Dreadnought (DRED)](#dred), [NightHawk Transport (SHAD)](#shad), [Giant Squid (SQD)](#sqd), [Dolphin (DLPH)](#dlph), [Soviet Construction Vehicle (SMCV)](#smcv), [Tank Destroyer (TNKD)](#tnkd), [Howitzer (HOWI)](#howi), [Tesla Tank (TTNK)](#ttnk), [Hind Transport (HIND)](#hind), [Lasher Light Tank (LTNK)](#ltnk), [Chrono Miner (CMON)](#cmon), [Chrono Miner (CMIN)](#cmin), [Prism Tank (SREF)](#sref), [Placeholder (XCOMET)](#xcomet), [Sea Scorpion (HYD)](#hyd), [Mirage Tank (MGTK)](#mgtk), [IFV (FV)](#fv), [DEATHDUMMY (DEATHDUMMY)](#deathdummy), [Vladimir's Command Ship (VLAD)](#vlad), [Demolition Truck (DTRUCK)](#dtruck), [Propaganda Truck (PROPA)](#propa), [Excavator (CONA)](#cona), [Police Car (COP)](#cop), [Automobile (EUROC)](#euroc), [Limousine (LIMO)](#limo), [Automobile (STANG)](#stang), [Automobile (SUVB)](#suvb), [Automobile (SUVW)](#suvw), [Taxi (TAXI)](#taxi), [Pickup Truck (PTRUCK)](#ptruck), [Cruise Ship (CRUISE)](#cruise), [Tug Boat (TUG)](#tug), [Coast Guard Boat (CDEST)](#cdest), [APACHE (APACHE)](#apache), [Harrier (ORCA)](#orca), [Hornet (HORNET)](#hornet), [V3 Rocket (V3ROCKET)](#v3rocket), [Osprey (ASW)](#asw), [Missile (DMISL)](#dmisl), [Cargo Plane (PDPLANE)](#pdplane), [Black Eagle (BEAG)](#beag), [Cargo Plane (CARGOPLANE)](#cargoplane), [Engineer (YENGINEER)](#yengineer), [Guardian GI (GGI)](#ggi), [Initiate (INIT)](#init), [Boris (BORIS)](#boris), [Brute (BRUTE)](#brute), [Virus (VIRUS)](#virus), [Cowboy (CLNT)](#clnt), [Hero (ARND)](#arnd), [Bodybuilder (STLN)](#stln), [Camel (CAML)](#caml), [Einstein (EINS)](#eins), [Mummy (MUMY)](#mumy), [Premier Romanov (RMNV)](#rmnv), [Cosmonaut (LUNR)](#lunr), [T-Rex (DNOA)](#dnoa), [Brachiosaurus (DNOB)](#dnob), [Slave (SLAV)](#slav), [Mummy (WWLF)](#wwlf), [Attack Dog (YDOG)](#ydog), [Attack Dog (YADOG)](#yadog), [Amphibious Transport (YHVR)](#yhvr), [Yuri MCV (PCV)](#pcv), [Slave Miner (SMIN)](#smin), [Chrono Miner(noback) (SMON)](#smon), [Yellow Cab (YCAB)](#ycab), [Gattling Tank (YTNK)](#ytnk), [Battle Fortress (BFRT)](#bfrt), [Magnetron (TELE)](#tele), [Chaos Drone (CAOS)](#caos), [Bus (DDBX)](#ddbx), [Black Cab (BCAB)](#bcab), [Boomer (BSUB)](#bsub), [Siege Chopper (SCHP)](#schp), [Truck (JEEP)](#jeep), [Master Mind (MIND)](#mind), [Floating Disc (DISK)](#disk), [ZZZ Not Used (UTNK)](#utnk), [Robot Tank (ROBO)](#robo), [YDUM (YDUM)](#ydum), [Siege Chopper (SCHD)](#schd), [Camera Dolly (DOLY)](#doly), [Cable Car (CBLC)](#cblc), [Fire Truck (FTRK)](#ftrk), [Ambulance (AMBU)](#ambu), [Passenger Plane (CIVP)](#civp), [MiG (BPLN)](#bpln), [Spy Plane (SPYP)](#spyp), [Missile (CMISL)](#cmisl)

<a id="e1"></a>

## GI - E1

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Walk and fire using the standing infantry weapon.
2. Deploy to stop movement and use the deployed attack state; undeploy before moving again.
3. Where permitted, enter an occupiable building and contribute the configured garrison weapon.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 200 | 200 |
| Starting health capacity | 125 | 125 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 5 | 5 |
| Technology level | 1 | 1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAPILE | GAPILE |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Immune to ordinary psychic control | no | no |
| Can be crushed | yes | yes |
| Fires on deployment | yes | yes |
| Passenger IFV mode | 2 | 2 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 10 | 10 |
| Recycling value setting | 150 | 100 |
| Can garrison buildings | yes | yes |
| Attached bombs permitted | yes | yes |

**Red Alert 2 weapon paths:** Primary: [M60](reference/WEAPONS.md#ra2-m60); Secondary: [Para](reference/WEAPONS.md#ra2-para); Elite Primary: [M60E](reference/WEAPONS.md#ra2-m60e); Elite Secondary: [ParaE](reference/WEAPONS.md#ra2-parae).

**Data source:** ra2.mix/local.mix/rules.ini, section E1, first property line 3131.

**Yuri's Revenge weapon paths:** Primary: [M60](reference/WEAPONS.md#yr-m60); Secondary: [Para](reference/WEAPONS.md#yr-para); Occupy Weapon: [UCPara](reference/WEAPONS.md#yr-ucpara); Elite Occupy Weapon: [UCElitePara](reference/WEAPONS.md#yr-ucelitepara); Elite Primary: [M60E](reference/WEAPONS.md#yr-m60e); Elite Secondary: [ParaE](reference/WEAPONS.md#yr-parae).

**Data source:** expandmd01.mix/rulesmd.ini, section E1, first property line 3714.

<a id="e2"></a>

## Conscript - E2

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move as basic Soviet infantry and engage eligible targets.
2. Enter a permitted civilian building or bunker to contribute its configured garrison fire.
3. Leave the building through its unload/deploy interaction when ordered.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 100 | 100 |
| Starting health capacity | 125 | 125 |
| Armor class | flak | flak |
| Movement rating | 4 | 4 |
| Sight radius setting | 5 | 5 |
| Technology level | 1 | 1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAHAND | NAHAND |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Passenger IFV mode | 2 | 2 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 5 | 5 |
| Recycling value setting | 20 | 50 |
| Can garrison buildings | yes | yes |

**Red Alert 2 weapon paths:** Primary: [M1Carbine](reference/WEAPONS.md#ra2-m1carbine); Elite Primary: [M1CarbineE](reference/WEAPONS.md#ra2-m1carbinee).

**Data source:** ra2.mix/local.mix/rules.ini, section E2, first property line 3222.

**Yuri's Revenge weapon paths:** Primary: [M1Carbine](reference/WEAPONS.md#yr-m1carbine); Occupy Weapon: [UCM1Carbine](reference/WEAPONS.md#yr-ucm1carbine); Elite Occupy Weapon: [UCEliteM1Carbine](reference/WEAPONS.md#yr-ucelitem1carbine); Elite Primary: [M1CarbineE](reference/WEAPONS.md#yr-m1carbinee).

**Data source:** expandmd01.mix/rulesmd.ini, section E2, first property line 4328.

<a id="shk"></a>

## Tesla Trooper - SHK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use its Tesla weapon against eligible targets.
2. Approach a friendly Tesla Coil through the supported power-up interaction.
3. Contribute to that coil while attached instead of acting as an independent firing soldier.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 500 |
| Starting health capacity | 130 | 130 |
| Armor class | Plate | Plate |
| Movement rating | 4 | 4 |
| Sight radius setting | 6 | 6 |
| Technology level | 5 | 5 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAHAND | NAHAND |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can be crushed | no | no |
| Passenger IFV mode | 6 | 6 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 20 | 20 |
| Recycling value setting | 125 | 250 |

**Red Alert 2 weapon paths:** Primary: [ElectricBolt](reference/WEAPONS.md#ra2-electricbolt); Secondary: [AssaultBolt](reference/WEAPONS.md#ra2-assaultbolt); Elite Primary: [ElectricBoltE](reference/WEAPONS.md#ra2-electricbolte).

**Data source:** ra2.mix/local.mix/rules.ini, section SHK, first property line 3302.

**Yuri's Revenge weapon paths:** Primary: [ElectricBolt](reference/WEAPONS.md#yr-electricbolt); Secondary: [AssaultBolt](reference/WEAPONS.md#yr-assaultbolt); Elite Primary: [ElectricBoltE](reference/WEAPONS.md#yr-electricbolte).

**Data source:** expandmd01.mix/rulesmd.ini, section SHK, first property line 4508.

<a id="engineer"></a>

## Engineer - ENGINEER

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Travel to a legal building or repair-hut entry.
2. Enter to capture an eligible enemy/neutral structure, repair a suitable friendly structure, or invoke bridge repair.
3. The mission can react to the entry/capture separately from destruction.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 500 |
| Starting health capacity | 75 | 75 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 4 | 4 |
| Technology level | 1 | 1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,British,French,Germans,Americans,Alliance | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Excluded countries | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | Barracks | Barracks |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Passenger IFV mode | 1 | 1 |
| Threat contribution | 0 | 0 |
| Recycling value setting | 100 | 250 |

**Red Alert 2 weapon paths:** Primary: [DefuseKit](reference/WEAPONS.md#ra2-defusekit); Secondary: [VirtualScanner](reference/WEAPONS.md#ra2-virtualscanner).

**Data source:** ra2.mix/local.mix/rules.ini, section ENGINEER, first property line 3343.

**Yuri's Revenge weapon paths:** Primary: [DefuseKit](reference/WEAPONS.md#yr-defusekit); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section ENGINEER, first property line 3818.

<a id="jumpjet"></a>

## Rocketeer - JUMPJET

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Take off and use the jumpjet movement controller.
2. Move over ground obstacles while airborne and fire at supported targets.
3. Remain subject to anti-air targeting and landing/state rules; flying is not invulnerability.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 600 | 600 |
| Starting health capacity | 125 | 125 |
| Armor class | none | none |
| Movement rating | 9 | 9 |
| Sight radius setting | 8 | 8 |
| Technology level | 3 | 3 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAPILE,RADAR | GAPILE,RADAR |
| Permitted movement zone | Fly | Fly |
| Movement speed category | Hover | Hover |
| Transport size usage | 1 | 1 |
| Can be crushed | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 15 | 15 |
| Recycling value setting | 500 | 300 |

**Red Alert 2 weapon paths:** Primary: [20mm](reference/WEAPONS.md#ra2-20mm); Elite Primary: [20mmE](reference/WEAPONS.md#ra2-20mme).

**Data source:** ra2.mix/local.mix/rules.ini, section JUMPJET, first property line 3434.

**Yuri's Revenge weapon paths:** Primary: [20mm](reference/WEAPONS.md#yr-20mm); Elite Primary: [20mmE](reference/WEAPONS.md#yr-20mme).

**Data source:** expandmd01.mix/rulesmd.ini, section JUMPJET, first property line 3917.

<a id="ghost"></a>

## SEAL - GHOST

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move on supported land/water routes.
2. Use its gun against eligible targets.
3. Reach a legal demolition target and apply its C4 interaction.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 125 | 125 |
| Armor class | flak | flak |
| Movement rating | 5 | 5 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | 9 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAPILE,RADAR | GAPILE,RADAR |
| Permitted movement zone | AmphibiousDestroyer | AmphibiousDestroyer |
| Movement speed category | Amphibious | Amphibious |
| Transport size usage | 1 | 1 |
| Can be crushed | yes | yes |
| Passenger IFV mode | 4 | 4 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,SCATTER,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,SCATTER,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF,FASTER | SELF_HEAL,STRONGER,FIREPOWER,ROF,FASTER |
| Naval-target selection mode | 4 | 4 |
| Threat contribution | 25 | 25 |
| Recycling value setting | 1000 | 500 |
| C4 capability | yes | yes |

**Red Alert 2 weapon paths:** Primary: [MP5](reference/WEAPONS.md#ra2-mp5); Secondary: [Sapper](reference/WEAPONS.md#ra2-sapper); Elite Primary: [MP5E](reference/WEAPONS.md#ra2-mp5e).

**Data source:** ra2.mix/local.mix/rules.ini, section GHOST, first property line 3490.

**Yuri's Revenge weapon paths:** Primary: [MP5](reference/WEAPONS.md#yr-mp5); Secondary: [Sapper](reference/WEAPONS.md#yr-sapper); Elite Primary: [MP5E](reference/WEAPONS.md#yr-mp5e).

**Data source:** expandmd01.mix/rulesmd.ini, section GHOST, first property line 4015.

<a id="yuri"></a>

## Yuri Clone - YURI

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Acquire a susceptible target through mind control.
2. Maintain its control relationship rather than dealing ordinary gun damage.
3. Deploy to invoke its close-area psychic attack; immunity and affected-side behavior depend on this version and weapon data.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1200 | 800 |
| Starting health capacity | 100 | 100 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 12 | 12 |
| Technology level | 10 | 10 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Required structures/groups | NAHAND,NATECH | YABRCK,NAPSIS |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Immune to ordinary psychic control | yes | yes |
| Fires on deployment | yes | yes |
| Passenger IFV mode | 8 | 8 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 15 | 15 |
| Insignificant-object flag | no | no |
| Recycling value setting | 200 | 400 |

**Red Alert 2 weapon paths:** Primary: [MindControl](reference/WEAPONS.md#ra2-mindcontrol); Secondary: [PsiWave](reference/WEAPONS.md#ra2-psiwave).

**Data source:** ra2.mix/local.mix/rules.ini, section YURI, first property line 3591.

**Yuri's Revenge weapon paths:** Primary: [MindControl](reference/WEAPONS.md#yr-mindcontrol); Secondary: [PsiWave](reference/WEAPONS.md#yr-psiwave).

**Data source:** expandmd01.mix/rulesmd.ini, section YURI, first property line 5198.

<a id="ivan"></a>

## Crazy Ivan - IVAN

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Reach a target permitted by the bomb-placement interaction.
2. Attach a timed explosive.
3. Let its fuse/detonation/disarm rules resolve; the placement click is not an ordinary instant cannon shot.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 600 | 600 |
| Starting health capacity | 125 | 125 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 6 | 6 |
| Technology level | 5 | 5 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAHAND,NARADR | NAHAND,NARADR |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Passenger IFV mode | 7 | 7 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 15 | 15 |
| Insignificant-object flag | no | no |
| Explosive destruction flag | yes | yes |
| Recycling value setting | 150 | 300 |

**Red Alert 2 weapon paths:** Primary: [IvanBomber](reference/WEAPONS.md#ra2-ivanbomber); Elite Primary: [IvanBomberE](reference/WEAPONS.md#ra2-ivanbombere).

**Data source:** ra2.mix/local.mix/rules.ini, section IVAN, first property line 3637.

**Yuri's Revenge weapon paths:** Primary: [IvanBomber](reference/WEAPONS.md#yr-ivanbomber); Elite Primary: [IvanBomberE](reference/WEAPONS.md#yr-ivanbombere).

**Data source:** expandmd01.mix/rulesmd.ini, section IVAN, first property line 4548.

<a id="deso"></a>

## Desolator - DESO

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use its mobile radiation weapon against supported targets.
2. Deploy to produce the configured radiation-area effect.
3. Handle exposure over time and undeploy before relocating.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 600 | 600 |
| Starting health capacity | 150 | 150 |
| Armor class | plate | plate |
| Movement rating | 4 | 4 |
| Sight radius setting | 6 | 6 |
| Technology level | 8 | 8 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required countries | Arabs | Arabs |
| Required structures/groups | NAHAND,RADAR | NAHAND,RADAR |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Self-healing | yes | yes |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | yes | yes |
| Can be crushed | no | no |
| Fires on deployment | yes | yes |
| Passenger IFV mode | 9 | 9 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 20 | 20 |
| Recycling value setting | 300 | 300 |
| Attached bombs permitted | yes | yes |

**Red Alert 2 weapon paths:** Primary: [RadBeamWeapon](reference/WEAPONS.md#ra2-radbeamweapon); Secondary: [RadEruptionWeapon](reference/WEAPONS.md#ra2-raderuptionweapon); Elite Primary: [RadBeamWeaponE](reference/WEAPONS.md#ra2-radbeamweapone).

**Data source:** ra2.mix/local.mix/rules.ini, section DESO, first property line 3685.

**Yuri's Revenge weapon paths:** Primary: [RadBeamWeapon](reference/WEAPONS.md#yr-radbeamweapon); Secondary: [RadEruptionWeapon](reference/WEAPONS.md#yr-raderuptionweapon); Elite Primary: [RadBeamWeaponE](reference/WEAPONS.md#yr-radbeamweapone).

**Data source:** expandmd01.mix/rulesmd.ini, section DESO, first property line 4817.

<a id="dog"></a>

## Attack Dog - DOG

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Acquire an eligible infantry target or help expose disguised infiltrators.
2. Close to the target and perform its lethal close attack.
3. Do not treat this as a general anti-vehicle weapon.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 200 | 200 |
| Starting health capacity | 100 | 100 |
| Armor class | none | none |
| Movement rating | 8 | 8 |
| Sight radius setting | 9 | 9 |
| Technology level | 2 | 2 |
| Permitted country list | Russians,Confederation,Africans,Arabs,British,French,Germans,Americans,Alliance | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Excluded countries | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance,YuriCountry |
| Required structures/groups | Barracks | Barracks |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | yes | yes |
| Radiation immunity | no | no |
| Passenger IFV mode | 0 | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER,SCATTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER,SCATTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval-target selection mode | 6 | 6 |
| Threat contribution | 20 | 20 |
| Recycling value setting | 50 | 100 |
| Attached bombs permitted | yes | yes |

**Red Alert 2 weapon paths:** Primary: [BadTeeth](reference/WEAPONS.md#ra2-badteeth); Secondary: [VirtualScanner](reference/WEAPONS.md#ra2-virtualscanner).

**Data source:** ra2.mix/local.mix/rules.ini, section DOG, first property line 3784.

**Yuri's Revenge weapon paths:** Primary: [BadTeeth](reference/WEAPONS.md#yr-badteeth); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section DOG, first property line 4370.

<a id="civ1"></a>

## Civilian - CIV1

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIV1, first property line 3884.

**Data source:** expandmd01.mix/rulesmd.ini, section CIV1, first property line 5619.

<a id="civ2"></a>

## Civilian - CIV2

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIV2, first property line 3920.

**Data source:** expandmd01.mix/rulesmd.ini, section CIV2, first property line 5655.

<a id="civ3"></a>

## Civilian - CIV3

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIV3, first property line 3956.

**Data source:** expandmd01.mix/rulesmd.ini, section CIV3, first property line 5691.

<a id="ctech"></a>

## Technician - CTECH

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Red Alert 2 weapon paths:** Primary: [Pistola](reference/WEAPONS.md#ra2-pistola).

**Data source:** ra2.mix/local.mix/rules.ini, section CTECH, first property line 4648.

**Yuri's Revenge weapon paths:** Primary: [Pistola](reference/WEAPONS.md#yr-pistola).

**Data source:** expandmd01.mix/rulesmd.ini, section CTECH, first property line 6517.

<a id="weedguy"></a>

## Chem Spray Infantry - WEEDGUY

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 300 | 300 |
| Starting health capacity | 130 | 130 |
| Armor class | none | none |
| Movement rating | 6 | 6 |
| Sight radius setting | 4 | 4 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | BARRACKS | BARRACKS |
| Permitted movement zone | Infantry | Infantry |
| Resource cargo capacity | 7 | 7 |
| Threat contribution | 0 | 0 |

**Red Alert 2 weapon paths:** Primary: [NukeCarrier](reference/WEAPONS.md#ra2-nukecarrier); Secondary: [V3Cluster](reference/WEAPONS.md#ra2-v3cluster).

**Data source:** ra2.mix/local.mix/rules.ini, section WEEDGUY, first property line 4688.

**Yuri's Revenge weapon paths:** Primary: [NukeCarrier](reference/WEAPONS.md#yr-nukecarrier); Secondary: [V3Cluster](reference/WEAPONS.md#yr-v3cluster).

**Data source:** expandmd01.mix/rulesmd.ini, section WEEDGUY, first property line 6557.

<a id="cleg"></a>

## Chrono Legionnaire - CLEG

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Teleport to the chosen location and wait out the applicable arrival recovery.
2. Attach its temporal weapon to a legal target and accumulate erasure progress.
3. If interrupted, handle release of the partially erased target; erasure is different from normal shell damage.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1500 | 1500 |
| Starting health capacity | 125 | 125 |
| Armor class | none | none |
| Movement rating | 5 | 5 |
| Sight radius setting | 8 | 8 |
| Technology level | 10 | 10 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAPILE,TECH | GAPILE,TECH |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can be crushed | no | no |
| Passenger IFV mode | 10 | 10 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 20 | 20 |
| Recycling value setting | 1200 | 750 |
| Attached bombs permitted | yes | yes |

**Red Alert 2 weapon paths:** Primary: [NeutronRifle](reference/WEAPONS.md#ra2-neutronrifle); Elite Primary: [NeutronRifleE](reference/WEAPONS.md#ra2-neutronriflee).

**Data source:** ra2.mix/local.mix/rules.ini, section CLEG, first property line 3734.

**Yuri's Revenge weapon paths:** Primary: [NeutronRifle](reference/WEAPONS.md#yr-neutronrifle); Elite Primary: [NeutronRifleE](reference/WEAPONS.md#yr-neutronriflee).

**Data source:** expandmd01.mix/rulesmd.ini, section CLEG, first property line 4126.

<a id="spy"></a>

## Spy - SPY

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Adopt an allowed enemy-infantry disguise.
2. Avoid detection and reach an eligible enemy building.
3. Apply that building type's infiltration result; the mission can also listen for the infiltration event.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 100 | 100 |
| Armor class | flak | flak |
| Movement rating | 4 | 4 |
| Sight radius setting | 9 | 9 |
| Technology level | 5 | 5 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAPILE,GATECH | GAPILE,GATECH |
| Permitted movement zone | Infantry | Infantry |
| Can gain rank | no | no |
| Passenger IFV mode | 2 | 2 |
| Threat contribution | 0 | 0 |
| Recycling value setting | 900 | 500 |

**Red Alert 2 weapon paths:** Primary: [MakeupKit](reference/WEAPONS.md#ra2-makeupkit).

**Data source:** ra2.mix/local.mix/rules.ini, section SPY, first property line 4720.

**Yuri's Revenge weapon paths:** Primary: [MakeupKit](reference/WEAPONS.md#yr-makeupkit).

**Data source:** expandmd01.mix/rulesmd.ini, section SPY, first property line 3974.

<a id="ccomand"></a>

## Chrono Commando - CCOMAND

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use the special chrono movement/arrival procedure where this record is available.
2. Use its infantry combat and demolition capabilities on supported targets.
3. Availability depends on the appropriate infiltration/special prerequisite or mission provision.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 2000 | 2000 |
| Starting health capacity | 100 | 100 |
| Armor class | none | none |
| Movement rating | 5 | 5 |
| Sight radius setting | 8 | 8 |
| Technology level | 9 | 9 |
| Permitted country list | British,French,Germans,Americans,Alliance | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Required structures/groups | GAPILE | BARRACKS |
| Needs stolen Allied technology | yes | yes |
| Permitted movement zone | Infantry | Infantry |
| Can be crushed | no | no |
| Passenger IFV mode | 4 | 4 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 25 | 25 |
| Recycling value setting | 1000 | 1000 |

**Red Alert 2 weapon paths:** Primary: [ChronoMP5](reference/WEAPONS.md#ra2-chronomp5); Secondary: [FakeC4](reference/WEAPONS.md#ra2-fakec4); Elite Primary: [ChronoMP5E](reference/WEAPONS.md#ra2-chronomp5e).

**Data source:** ra2.mix/local.mix/rules.ini, section CCOMAND, first property line 4809.

**Yuri's Revenge weapon paths:** Primary: [ChronoMP5](reference/WEAPONS.md#yr-chronomp5); Secondary: [FakeC4](reference/WEAPONS.md#yr-fakec4); Elite Primary: [ChronoMP5E](reference/WEAPONS.md#yr-chronomp5e).

**Data source:** expandmd01.mix/rulesmd.ini, section CCOMAND, first property line 4175.

<a id="ptroop"></a>

## Psi Commando - PTROOP

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use the special commando record rather than the ordinary Yuri Clone.
2. Mind-control eligible enemies and use supported demolition interactions.
3. Check special prerequisite/infiltration availability before expecting it in a normal queue.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 100 | 100 |
| Armor class | none | none |
| Movement rating | 5 | 5 |
| Sight radius setting | 8 | 8 |
| Technology level | 9 | 9 |
| Permitted country list | British,French,Germans,Americans,Alliance | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Required structures/groups | GAPILE | BARRACKS |
| Needs stolen Soviet technology | yes | Not explicitly set |
| Permitted movement zone | Infantry | Infantry |
| Immune to ordinary psychic control | yes | yes |
| Can be crushed | no | no |
| Passenger IFV mode | 4 | 4 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 25 | 25 |
| Recycling value setting | 1000 | 500 |
| C4 capability | yes | yes |
| Needs stolen Yuri technology | Not explicitly set | yes |

**Red Alert 2 weapon paths:** Primary: [MindControl](reference/WEAPONS.md#ra2-mindcontrol); Elite Primary: [MindControlE](reference/WEAPONS.md#ra2-mindcontrole).

**Data source:** ra2.mix/local.mix/rules.ini, section PTROOP, first property line 4860.

**Yuri's Revenge weapon paths:** Primary: [MindControl](reference/WEAPONS.md#yr-mindcontrol); Elite Primary: [MindControlE](reference/WEAPONS.md#yr-mindcontrole).

**Data source:** expandmd01.mix/rulesmd.ini, section PTROOP, first property line 4227.

<a id="civan"></a>

## Chrono Ivan - CIVAN

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use the chrono movement procedure and its arrival delay.
2. Reach a target eligible for an Ivan-style attached bomb.
3. Resolve the bomb separately; special production prerequisites govern access to this unit.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1750 |
| Starting health capacity | 100 | 100 |
| Armor class | none | none |
| Movement rating | 6 | 6 |
| Sight radius setting | 8 | 8 |
| Technology level | 9 | 9 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Required structures/groups | NAHAND | BARRACKS |
| Needs stolen Allied technology | yes | Not explicitly set |
| Permitted movement zone | Infantry | Infantry |
| Can gain rank | no | no |
| Can be crushed | no | no |
| Passenger IFV mode | 7 | 7 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 25 | 25 |
| Recycling value setting | 250 | 500 |
| Needs stolen Soviet technology | Not explicitly set | yes |

**Red Alert 2 weapon paths:** Primary: [IvanBomber](reference/WEAPONS.md#ra2-ivanbomber).

**Data source:** ra2.mix/local.mix/rules.ini, section CIVAN, first property line 4909.

**Yuri's Revenge weapon paths:** Primary: [IvanBomber](reference/WEAPONS.md#yr-ivanbomber).

**Data source:** expandmd01.mix/rulesmd.ini, section CIVAN, first property line 4662.

<a id="yuripr"></a>

## Yuri Prime - YURIPR

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use this specific hero record: RA2 and Yuri do not assign it identical availability or behavior.
2. Acquire eligible targets through its mind-control weapon; the Yuri version can also control suitable structures.
3. Use its deployment psychic effect and hover movement according to the selected rules.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 2000 | 1500 |
| Starting health capacity | 200 | 150 |
| Armor class | flak | flak |
| Movement rating | 6 | 6 |
| Sight radius setting | 8 | 9 |
| Technology level | 9 | 10 |
| Permitted country list | Russians,Confederation,Africans,Arabs | YuriCountry |
| Required structures/groups | NAHAND | YABRCK,YATECH |
| Needs stolen Soviet technology | yes | Not explicitly set |
| Build limit | 1 | 1 |
| Permitted movement zone | Infantry | AmphibiousDestroyer |
| Transport size usage | 1 | 1 |
| Immune to ordinary psychic control | yes | yes |
| Can be crushed | no | no |
| Fires on deployment | yes | yes |
| Passenger IFV mode | 8 | 15 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 25 | 25 |
| Recycling value setting | 250 | 750 |
| Movement speed category | Not explicitly set | Amphibious |
| Self-healing | Not explicitly set | yes |
| Psychic-weapon immunity | Not explicitly set | yes |

**Red Alert 2 weapon paths:** Primary: [SuperMindControl](reference/WEAPONS.md#ra2-supermindcontrol); Secondary: [PsiWave](reference/WEAPONS.md#ra2-psiwave).

**Data source:** ra2.mix/local.mix/rules.ini, section YURIPR, first property line 4958.

**Yuri's Revenge weapon paths:** Primary: [SuperMindControl](reference/WEAPONS.md#yr-supermindcontrol); Secondary: [SuperPsiWave](reference/WEAPONS.md#yr-superpsiwave).

**Data source:** expandmd01.mix/rulesmd.ini, section YURIPR, first property line 5247.

<a id="snipe"></a>

## Sniper - SNIPE

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Seek an infantry target within supported range.
2. Aim/fire its anti-infantry weapon.
3. Use the owner/country restrictions on the card; range does not grant an anti-tank role.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 600 | 600 |
| Starting health capacity | 125 | 125 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 8 | 8 |
| Technology level | 1 | 1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required countries | British | British |
| Required structures/groups | GAPILE,RADAR | GAPILE,RADAR |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Immune to ordinary psychic control | no | no |
| Passenger IFV mode | 5 | 5 |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 10 | 10 |
| Recycling value setting | 600 | 300 |
| Attached bombs permitted | yes | yes |

**Red Alert 2 weapon paths:** Primary: [AWP](reference/WEAPONS.md#ra2-awp); Elite Primary: [AWPE](reference/WEAPONS.md#ra2-awpe).

**Data source:** ra2.mix/local.mix/rules.ini, section SNIPE, first property line 3180.

**Yuri's Revenge weapon paths:** Primary: [AWP](reference/WEAPONS.md#yr-awp); Elite Primary: [AWPE](reference/WEAPONS.md#yr-awpe).

**Data source:** expandmd01.mix/rulesmd.ini, section SNIPE, first property line 4279.

<a id="cow"></a>

## Cow - COW

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 150 | 150 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 4 | 4 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 2 | 2 |
| Can be crushed | no | no |
| Passenger IFV mode | 12 | 12 |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 2000 | 200 |

**Data source:** ra2.mix/local.mix/rules.ini, section COW, first property line 4504.

**Data source:** expandmd01.mix/rulesmd.ini, section COW, first property line 5315.

<a id="all"></a>

## Alligator - ALL

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 200 | 200 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 2 | 2 |
| Can gain rank | no | no |
| Can be crushed | no | no |
| Passenger IFV mode | 12 | 12 |
| Threat contribution | 2 | 2 |
| Insignificant-object flag | no | no |
| Recycling value setting | 2000 | 200 |

**Red Alert 2 weapon paths:** Primary: [AlligatorBite](reference/WEAPONS.md#ra2-alligatorbite); Secondary: [VirtualScanner](reference/WEAPONS.md#ra2-virtualscanner).

**Data source:** ra2.mix/local.mix/rules.ini, section ALL, first property line 4541.

**Yuri's Revenge weapon paths:** Primary: [AlligatorBite](reference/WEAPONS.md#yr-alligatorbite); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section ALL, first property line 5354.

<a id="tany"></a>

## Tanya - TANY

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move or swim toward the ordered target.
2. Use her infantry weapon against eligible enemies and C4 against supported close demolition targets.
3. Check the mission ledger: her death is a failure event in several scenarios, independently of the remaining army.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1500 |
| Starting health capacity | 125 | 200 |
| Armor class | flak | flak |
| Movement rating | 5 | 6 |
| Sight radius setting | 8 | 8 |
| Technology level | 9 | 9 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAPILE,GATECH | GAPILE,GATECH |
| Permitted movement zone | AmphibiousDestroyer | AmphibiousDestroyer |
| Movement speed category | Amphibious | Amphibious |
| Transport size usage | 1 | 1 |
| Can be crushed | yes | no |
| Passenger IFV mode | 4 | 4 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,SCATTER | STRONGER,FIREPOWER,ROF,SIGHT,SCATTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval-target selection mode | 4 | 4 |
| Threat contribution | 25 | 25 |
| Recycling value setting | 1000 | 750 |
| C4 capability | yes | yes |
| Build limit | Not explicitly set | 1 |
| Self-healing | Not explicitly set | yes |
| Immune to ordinary psychic control | Not explicitly set | yes |

**Red Alert 2 weapon paths:** Primary: [DoublePistols](reference/WEAPONS.md#ra2-doublepistols); Secondary: [Sapper](reference/WEAPONS.md#ra2-sapper); Elite Primary: [DoublePistolsE](reference/WEAPONS.md#ra2-doublepistolse).

**Data source:** ra2.mix/local.mix/rules.ini, section TANY, first property line 3541.

**Yuri's Revenge weapon paths:** Primary: [DoublePistols](reference/WEAPONS.md#yr-doublepistols); Secondary: [Sapper](reference/WEAPONS.md#yr-sapper); Elite Primary: [DoublePistolsE](reference/WEAPONS.md#yr-doublepistolse); Elite Secondary: [Sapper](reference/WEAPONS.md#yr-sapper).

**Data source:** expandmd01.mix/rulesmd.ini, section TANY, first property line 4069.

<a id="flakt"></a>

## Flak Trooper - FLAKT

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Choose the ground or air weapon appropriate to the target.
2. Move into range and fire flak.
3. Resolve the projectile/warhead rather than assuming one shot always damages every nearby target equally.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 300 | 300 |
| Starting health capacity | 100 | 100 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 5 | 5 |
| Technology level | 1 | 1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAHAND,NARADR | NAHAND,NARADR |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Passenger IFV mode | 3 | 3 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 5 | 5 |
| Recycling value setting | 50 | 150 |

**Red Alert 2 weapon paths:** Primary: [FlakGuyGun](reference/WEAPONS.md#ra2-flakguygun); Secondary: [FlakGuyAAGun](reference/WEAPONS.md#ra2-flakguyaagun); Elite Primary: [FlakGuyGunE](reference/WEAPONS.md#ra2-flakguygune); Elite Secondary: [FlakGuyAAGunE](reference/WEAPONS.md#ra2-flakguyaagune).

**Data source:** ra2.mix/local.mix/rules.ini, section FLAKT, first property line 3261.

**Yuri's Revenge weapon paths:** Primary: [FlakGuyGun](reference/WEAPONS.md#yr-flakguygun); Secondary: [FlakGuyAAGun](reference/WEAPONS.md#yr-flakguyaagun); Elite Primary: [FlakGuyGunE](reference/WEAPONS.md#yr-flakguygune); Elite Secondary: [FlakGuyAAGunE](reference/WEAPONS.md#yr-flakguyaagune).

**Data source:** expandmd01.mix/rulesmd.ini, section FLAKT, first property line 4421.

<a id="terror"></a>

## Terrorist - TERROR

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Approach the requested target.
2. Trigger its suicide explosive effect when the supported attack/detonation condition occurs.
3. Remove the attacker and resolve the explosion against nearby eligible objects.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 200 | 200 |
| Starting health capacity | 75 | 75 |
| Armor class | flak | flak |
| Movement rating | 6 | 6 |
| Sight radius setting | 9 | 9 |
| Technology level | 5 | 5 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required countries | Confederation | Confederation |
| Required structures/groups | NAHAND,RADAR | NAHAND,RADAR |
| Permitted movement zone | Infantry | Infantry |
| Can gain rank | no | no |
| Passenger IFV mode | 11 | 11 |
| Threat contribution | 0 | 0 |
| Explosive destruction flag | yes | yes |
| Recycling value setting | 25 | 100 |

**Red Alert 2 weapon paths:** Primary: [TerrorBomb](reference/WEAPONS.md#ra2-terrorbomb); Death Weapon: [TerrorBomb](reference/WEAPONS.md#ra2-terrorbomb).

**Data source:** ra2.mix/local.mix/rules.ini, section TERROR, first property line 4762.

**Yuri's Revenge weapon paths:** Primary: [TerrorBomb](reference/WEAPONS.md#yr-terrorbomb); Death Weapon: [TerrorBomb](reference/WEAPONS.md#yr-terrorbomb).

**Data source:** expandmd01.mix/rulesmd.ini, section TERROR, first property line 4769.

<a id="sengineer"></a>

## Engineer - SENGINEER

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use the Soviet Engineer type with its own art, owner and production restrictions.
2. Reach and enter a legal building or bridge-repair hut.
3. Apply capture/repair and notify attached mission logic.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 500 |
| Starting health capacity | 75 | 75 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 4 | 4 |
| Technology level | 1 | 1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,British,French,Germans,Americans,Alliance | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Excluded countries | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance,YuriCountry |
| Required structures/groups | Barracks | Barracks |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Passenger IFV mode | 1 | 1 |
| Threat contribution | 0 | 0 |
| Recycling value setting | 100 | 250 |

**Red Alert 2 weapon paths:** Primary: [DefuseKit](reference/WEAPONS.md#ra2-defusekit); Secondary: [VirtualScanner](reference/WEAPONS.md#ra2-virtualscanner).

**Data source:** ra2.mix/local.mix/rules.ini, section SENGINEER, first property line 3388.

**Yuri's Revenge weapon paths:** Primary: [DefuseKit](reference/WEAPONS.md#yr-defusekit); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section SENGINEER, first property line 4462.

<a id="adog"></a>

## Attack Dog - ADOG

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use the Allied dog record with its own appearance/owner rules.
2. Approach an eligible infantry target and perform the close attack.
3. Its detection role matters against spies even when other defenders accept a disguise.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 200 | 200 |
| Starting health capacity | 100 | 100 |
| Armor class | none | none |
| Movement rating | 8 | 8 |
| Sight radius setting | 9 | 9 |
| Technology level | 2 | 2 |
| Permitted country list | Russians,Confederation,Africans,Arabs,British,French,Germans,Americans,Alliance | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Excluded countries | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | Barracks | Barracks |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | yes | yes |
| Radiation immunity | no | no |
| Passenger IFV mode | 0 | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER,SCATTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER,SCATTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval-target selection mode | 6 | 6 |
| Threat contribution | 20 | 20 |
| Recycling value setting | 50 | 100 |
| Attached bombs permitted | yes | yes |

**Red Alert 2 weapon paths:** Primary: [GoodTeeth](reference/WEAPONS.md#ra2-goodteeth); Secondary: [VirtualScanner](reference/WEAPONS.md#ra2-virtualscanner).

**Data source:** ra2.mix/local.mix/rules.ini, section ADOG, first property line 3835.

**Yuri's Revenge weapon paths:** Primary: [GoodTeeth](reference/WEAPONS.md#yr-goodteeth); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section ADOG, first property line 3768.

<a id="vladimir"></a>

## Civilian - VLADIMIR

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Passenger IFV mode | 0 | 0 |
| Threat contribution | 0 | 0 |
| Recycling value setting | 100 | 200 |

**Red Alert 2 weapon paths:** Primary: [Pistola](reference/WEAPONS.md#ra2-pistola).

**Data source:** ra2.mix/local.mix/rules.ini, section VLADIMIR, first property line 4360.

**Yuri's Revenge weapon paths:** Primary: [Pistola](reference/WEAPONS.md#yr-pistola).

**Data source:** expandmd01.mix/rulesmd.ini, section VLADIMIR, first property line 6370.

<a id="pentgen"></a>

## Civilian - PENTGEN

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Passenger IFV mode | 0 | 0 |
| Threat contribution | 0 | 0 |
| Recycling value setting | 100 | 200 |

**Red Alert 2 weapon paths:** Primary: [Pistola](reference/WEAPONS.md#ra2-pistola).

**Data source:** ra2.mix/local.mix/rules.ini, section PENTGEN, first property line 4396.

**Yuri's Revenge weapon paths:** Primary: [Pistola](reference/WEAPONS.md#yr-pistola).

**Data source:** expandmd01.mix/rulesmd.ini, section PENTGEN, first property line 6407.

<a id="pres"></a>

## President - PRES

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Passenger IFV mode | 12 | 12 |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 2000 |

**Data source:** ra2.mix/local.mix/rules.ini, section PRES, first property line 4469.

**Data source:** expandmd01.mix/rulesmd.ini, section PRES, first property line 6480.

<a id="ssrv"></a>

## Secret Service - SSRV

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Passenger IFV mode | 0 | 0 |
| Threat contribution | 0 | 0 |
| Recycling value setting | 100 | 100 |

**Red Alert 2 weapon paths:** Primary: [Pistola](reference/WEAPONS.md#ra2-pistola).

**Data source:** ra2.mix/local.mix/rules.ini, section SSRV, first property line 4433.

**Yuri's Revenge weapon paths:** Primary: [Pistola](reference/WEAPONS.md#yr-pistola).

**Data source:** expandmd01.mix/rulesmd.ini, section SSRV, first property line 6444.

<a id="civa"></a>

## Civilian - CIVA

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Red Alert 2 weapon paths:** Primary: [Pistola](reference/WEAPONS.md#ra2-pistola).

**Data source:** ra2.mix/local.mix/rules.ini, section CIVA, first property line 3993.

**Yuri's Revenge weapon paths:** Primary: [Pistola](reference/WEAPONS.md#yr-pistola).

**Data source:** expandmd01.mix/rulesmd.ini, section CIVA, first property line 5728.

<a id="civb"></a>

## Civilian - CIVB

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Red Alert 2 weapon paths:** Primary: [Pistola](reference/WEAPONS.md#ra2-pistola).

**Data source:** ra2.mix/local.mix/rules.ini, section CIVB, first property line 4030.

**Yuri's Revenge weapon paths:** Primary: [Pistola](reference/WEAPONS.md#yr-pistola).

**Data source:** expandmd01.mix/rulesmd.ini, section CIVB, first property line 5765.

<a id="civc"></a>

## Civilian - CIVC

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Red Alert 2 weapon paths:** Primary: [Pistola](reference/WEAPONS.md#ra2-pistola).

**Data source:** ra2.mix/local.mix/rules.ini, section CIVC, first property line 4067.

**Yuri's Revenge weapon paths:** Primary: [Pistola](reference/WEAPONS.md#yr-pistola).

**Data source:** expandmd01.mix/rulesmd.ini, section CIVC, first property line 5802.

<a id="civbbp"></a>

## Civilian - CIVBBP

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIVBBP, first property line 4105.

**Data source:** expandmd01.mix/rulesmd.ini, section CIVBBP, first property line 5840.

<a id="civbfm"></a>

## Civilian - CIVBFM

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIVBFM, first property line 4142.

**Data source:** expandmd01.mix/rulesmd.ini, section CIVBFM, first property line 5877.

<a id="civbf"></a>

## Civilian - CIVBF

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIVBF, first property line 4178.

**Data source:** expandmd01.mix/rulesmd.ini, section CIVBF, first property line 5913.

<a id="civbtm"></a>

## Civilian - CIVBTM

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIVBTM, first property line 4214.

**Data source:** expandmd01.mix/rulesmd.ini, section CIVBTM, first property line 5949.

<a id="civsfm"></a>

## Civilian - CIVSFM

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIVSFM, first property line 4251.

**Data source:** expandmd01.mix/rulesmd.ini, section CIVSFM, first property line 5986.

<a id="civsf"></a>

## Civilian - CIVSF

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIVSF, first property line 4287.

**Data source:** expandmd01.mix/rulesmd.ini, section CIVSF, first property line 6022.

<a id="civstm"></a>

## Civilian - CIVSTM

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 50 | 50 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 1 | 1 |
| Can gain rank | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | 100 | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CIVSTM, first property line 4323.

**Data source:** expandmd01.mix/rulesmd.ini, section CIVSTM, first property line 6058.

<a id="polarb"></a>

## Polar Bear - POLARB

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 200 | 200 |
| Armor class | none | none |
| Movement rating | 4 | 4 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 2 | 2 |
| Can gain rank | no | no |
| Can be crushed | no | no |
| Passenger IFV mode | 12 | 12 |
| Threat contribution | 2 | 2 |
| Insignificant-object flag | no | no |
| Recycling value setting | 2000 | 200 |

**Red Alert 2 weapon paths:** Primary: [BearBite](reference/WEAPONS.md#ra2-bearbite); Secondary: [VirtualScanner](reference/WEAPONS.md#ra2-virtualscanner).

**Data source:** ra2.mix/local.mix/rules.ini, section POLARB, first property line 4577.

**Yuri's Revenge weapon paths:** Primary: [BearBite](reference/WEAPONS.md#yr-bearbite); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section POLARB, first property line 5391.

<a id="josh"></a>

## Monkey - JOSH

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 10 | 10 |
| Starting health capacity | 200 | 200 |
| Armor class | none | none |
| Movement rating | 6 | 6 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry | Infantry |
| Transport size usage | 2 | 2 |
| Can gain rank | no | no |
| Can be crushed | no | no |
| Passenger IFV mode | 12 | 12 |
| Threat contribution | 2 | 2 |
| Insignificant-object flag | no | no |
| Recycling value setting | 2000 | 200 |

**Red Alert 2 weapon paths:** Primary: [ChimpBite](reference/WEAPONS.md#ra2-chimpbite); Secondary: [VirtualScanner](reference/WEAPONS.md#ra2-virtualscanner).

**Data source:** ra2.mix/local.mix/rules.ini, section JOSH, first property line 4612.

**Yuri's Revenge weapon paths:** Primary: [ChimpBite](reference/WEAPONS.md#yr-chimpbite); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section JOSH, first property line 5428.

<a id="amcv"></a>

## Allied Construction Vehicle - AMCV

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move to a clear legal foundation.
2. Deploy into the Allied Construction Yard.
3. Use the resulting building's construction workflow; blocked foundations prevent deployment.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 3000 | 3000 |
| Starting health capacity | 1000 | 1000 |
| Armor class | heavy | heavy |
| Movement rating | 4 | 4 |
| Sight radius setting | 6 | 6 |
| Technology level | 10 | 10 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP,GADEPT | GAWEAP,GADEPT |
| Permitted movement zone | Normal | Normal |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Can crush through ordinary crushing logic | yes | yes |
| Deploys into | GACNST | GACNST |
| Threat contribution | 0 | 0 |
| Recycling value setting | Not explicitly set | 3000 |
| Can enter tank bunkers | Not explicitly set | no |

**Data source:** ra2.mix/local.mix/rules.ini, section AMCV, first property line 6091.

**Data source:** expandmd01.mix/rulesmd.ini, section AMCV, first property line 6970.

<a id="harv"></a>

## War Miner - HARV

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Collect resources into its cargo.
2. Drive back to a usable Soviet refinery, dock and unload.
3. Repeat the cycle; use its gun only against supported targets.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1400 | 1400 |
| Starting health capacity | 1000 | 1000 |
| Armor class | medium | medium |
| Movement rating | 4 | 4 |
| Sight radius setting | 4 | 4 |
| Technology level | 1 | 1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP,PROC | NAWEAP,PROC |
| Permitted movement zone | Crusher | Crusher |
| Transport size usage | 3 | 3 |
| Resource cargo capacity | 40 | 40 |
| Self-healing | yes | yes |
| Immune to ordinary psychic control | yes | yes |
| Radiation immunity | yes | yes |
| Can crush through ordinary crushing logic | yes | yes |
| Conventional harvester behavior | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 0 | 0 |
| Compatible aircraft docks | NAREFN,GAREFN | NAREFN,GAREFN |
| Resource-gathering role | Not explicitly set | yes |
| Recycling value setting | Not explicitly set | 1400 |
| Can enter tank bunkers | Not explicitly set | no |

**Red Alert 2 weapon paths:** Primary: [20mmRapid](reference/WEAPONS.md#ra2-20mmrapid); Elite Primary: [20mmRapidE](reference/WEAPONS.md#ra2-20mmrapide).

**Data source:** ra2.mix/local.mix/rules.ini, section HARV, first property line 5925.

**Yuri's Revenge weapon paths:** Primary: [20mmRapid](reference/WEAPONS.md#yr-20mmrapid); Elite Primary: [20mmRapidE](reference/WEAPONS.md#yr-20mmrapide).

**Data source:** expandmd01.mix/rulesmd.ini, section HARV, first property line 8216.

<a id="apoc"></a>

## Apocalypse - APOC

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Advance as a heavy tank and choose the ground cannon or anti-air weapon for the target.
2. Wait for the relevant reload/burst and resolve the shot.
3. Use its self-healing and rank properties as defined; it is not immune to all special effects.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1750 | 1750 |
| Starting health capacity | 800 | 800 |
| Armor class | heavy | heavy |
| Movement rating | 4 | 4 |
| Sight radius setting | 6 | 6 |
| Technology level | 7 | 7 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP,NATECH | NAWEAP,NATECH |
| Permitted movement zone | Destroyer | Destroyer |
| Transport size usage | 6 | 6 |
| Self-healing | yes | yes |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 40 | 40 |
| Explosive destruction flag | yes | yes |
| Production-time multiplier | Not explicitly set | 1.0 |
| Recycling value setting | Not explicitly set | 1750 |

**Red Alert 2 weapon paths:** Primary: [120mmx](reference/WEAPONS.md#ra2-120mmx); Secondary: [MammothTusk](reference/WEAPONS.md#ra2-mammothtusk); Elite Primary: [120mmxE](reference/WEAPONS.md#ra2-120mmxe).

**Data source:** ra2.mix/local.mix/rules.ini, section APOC, first property line 5012.

**Yuri's Revenge weapon paths:** Primary: [120mmx](reference/WEAPONS.md#yr-120mmx); Secondary: [MammothTusk](reference/WEAPONS.md#yr-mammothtusk); Elite Primary: [120mmxE](reference/WEAPONS.md#yr-120mmxe).

**Data source:** expandmd01.mix/rulesmd.ini, section APOC, first property line 7789.

<a id="htnk"></a>

## Rhino Heavy Tank - HTNK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move into range using the tracked ground controller.
2. Fire the Rhino's cannon at eligible targets.
3. Repeat or accept a new order; crushing and target armor affect its practical role.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 900 | 900 |
| Starting health capacity | 400 | 400 |
| Armor class | heavy | heavy |
| Movement rating | 6 | 6 |
| Sight radius setting | 8 | 8 |
| Technology level | 2 | 2 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Destroyer | Destroyer |
| Transport size usage | 3 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 40 | 40 |
| Production-time multiplier | Not explicitly set | 1.3 |
| Recycling value setting | Not explicitly set | 900 |

**Red Alert 2 weapon paths:** Primary: [120mm](reference/WEAPONS.md#ra2-120mm); Elite Primary: [120mmE](reference/WEAPONS.md#ra2-120mme).

**Data source:** ra2.mix/local.mix/rules.ini, section HTNK, first property line 6476.

**Yuri's Revenge weapon paths:** Primary: [120mm](reference/WEAPONS.md#yr-120mm); Elite Primary: [120mmE](reference/WEAPONS.md#yr-120mme).

**Data source:** expandmd01.mix/rulesmd.ini, section HTNK, first property line 7684.

<a id="sapc"></a>

## Amphibious Transport - SAPC

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Load infantry or vehicles permitted by passenger-size/capacity rules.
2. Travel over legal land/water to a usable unloading shore or location.
3. Unload into available cells; do not assume a full transport can unload onto blocked terrain.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 900 | 900 |
| Starting health capacity | 300 | 300 |
| Armor class | heavy | heavy |
| Movement rating | 6 | 6 |
| Sight radius setting | 6 | 6 |
| Technology level | 2 | 2 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAYARD | NAYARD |
| Permitted movement zone | Amphibious | Amphibious |
| Movement speed category | Hover | Hover |
| Passenger slot capacity | 12 | 12 |
| Largest passenger-size setting | 6 | 6 |
| Transport size usage | 15 | 15 |
| Can gain rank | no | no |
| Can crush through ordinary crushing logic | yes | yes |
| Naval role | yes | yes |
| Threat contribution | 10 | 10 |
| Recycling value setting | Not explicitly set | 900 |
| Can enter tank bunkers | Not explicitly set | no |

**Data source:** ra2.mix/local.mix/rules.ini, section SAPC, first property line 6947.

**Data source:** expandmd01.mix/rulesmd.ini, section SAPC, first property line 7882.

<a id="car"></a>

## Automobile - CAR

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CAR, first property line 6382.

**Data source:** expandmd01.mix/rulesmd.ini, section CAR, first property line 9556.

<a id="bus"></a>

## School Bus - BUS

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Passenger slot capacity | 5 | 5 |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section BUS, first property line 6287.

**Data source:** expandmd01.mix/rulesmd.ini, section BUS, first property line 9359.

<a id="wini"></a>

## Recreational Vehicle - WINI

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section WINI, first property line 6429.

**Data source:** expandmd01.mix/rulesmd.ini, section WINI, first property line 9605.

<a id="pick"></a>

## Pickup Truck - PICK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section PICK, first property line 6334.

**Data source:** expandmd01.mix/rulesmd.ini, section PICK, first property line 9506.

<a id="mtnk"></a>

## Grizzly Battle Tank - MTNK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move into a usable ground firing position.
2. Fire its Grizzly cannon at an eligible target.
3. Recheck range and reload as the target moves.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 700 | 700 |
| Starting health capacity | 300 | 300 |
| Armor class | heavy | heavy |
| Movement rating | 7 | 7 |
| Sight radius setting | 8 | 8 |
| Technology level | 2 | 2 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP | GAWEAP |
| Permitted movement zone | Normal | Normal |
| Transport size usage | 3 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 15 | 15 |
| Production-time multiplier | Not explicitly set | 1.5 |
| Recycling value setting | Not explicitly set | 700 |

**Red Alert 2 weapon paths:** Primary: [105mm](reference/WEAPONS.md#ra2-105mm); Elite Primary: [105mmE](reference/WEAPONS.md#ra2-105mme).

**Data source:** ra2.mix/local.mix/rules.ini, section MTNK, first property line 6570.

**Yuri's Revenge weapon paths:** Primary: [105mm](reference/WEAPONS.md#yr-105mm); Elite Primary: [105mmE](reference/WEAPONS.md#yr-105mme).

**Data source:** expandmd01.mix/rulesmd.ini, section MTNK, first property line 6604.

<a id="horv"></a>

## War Miner - HORV

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1400 | 1400 |
| Starting health capacity | 1000 | 1000 |
| Armor class | medium | medium |
| Movement rating | 4 | 4 |
| Sight radius setting | 4 | 4 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Permitted movement zone | Crusher | Crusher |
| Self-healing | yes | yes |
| Radiation immunity | yes | yes |
| Can crush through ordinary crushing logic | yes | yes |
| Conventional harvester behavior | yes | yes |
| Threat contribution | 0 | 0 |
| Compatible aircraft docks | NAREFN,GAREFN | NAREFN,GAREFN |

**Data source:** ra2.mix/local.mix/rules.ini, section HORV, first property line 5885.

**Data source:** expandmd01.mix/rulesmd.ini, section HORV, first property line 8175.

<a id="trucka"></a>

## Truck - TRUCKA

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 0 |
| Starting health capacity | 200 | 200 |
| Armor class | light | light |
| Movement rating | 4 | 4 |
| Sight radius setting | 5 | 5 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Normal | Normal |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Self-healing | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section TRUCKA, first property line 5105.

**Data source:** expandmd01.mix/rulesmd.ini, section TRUCKA, first property line 9176.

<a id="truckb"></a>

## Truck (loaded) - TRUCKB

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 0 |
| Starting health capacity | 200 | 200 |
| Armor class | light | light |
| Movement rating | 4 | 4 |
| Sight radius setting | 5 | 5 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Normal | Normal |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Self-healing | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section TRUCKB, first property line 5143.

**Data source:** expandmd01.mix/rulesmd.ini, section TRUCKB, first property line 9216.

<a id="carrier"></a>

## Aircraft Carrier - CARRIER

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Acquire a supported strike target.
2. Launch its managed Hornet aircraft, which fly and attack separately.
3. Recover/rearm or replace attackers according to the spawn-manager settings.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 2000 | 2000 |
| Starting health capacity | 800 | 800 |
| Armor class | heavy | heavy |
| Movement rating | 4 | 4 |
| Sight radius setting | 7 | 7 |
| Technology level | 7 | 7 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAYARD,TECH | GAYARD,TECH |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Transport size usage | 50 | 50 |
| Can crush through ordinary crushing logic | no | no |
| Spawned attacker type | HORNET | HORNET |
| Managed attacker count | 3 | 3 |
| Attacker replacement delay | 600 | 600 |
| Attacker reload delay | 150 | 150 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Threat contribution | 25 | 25 |
| Recycling value setting | Not explicitly set | 2000 |

**Red Alert 2 weapon paths:** Primary: [HornetLauncher](reference/WEAPONS.md#ra2-hornetlauncher).

**Data source:** ra2.mix/local.mix/rules.ini, section CARRIER, first property line 5348.

**Yuri's Revenge weapon paths:** Primary: [HornetLauncher](reference/WEAPONS.md#yr-hornetlauncher).

**Data source:** expandmd01.mix/rulesmd.ini, section CARRIER, first property line 7250.

<a id="v3"></a>

## V3 Launcher - V3

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Select a valid bombardment target.
2. Raise/launch its spawned rocket under its missile-manager rules.
3. Resolve the rocket's flight and impact separately, then prepare another attack.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 800 | 800 |
| Starting health capacity | 150 | 150 |
| Armor class | light | light |
| Movement rating | 4 | 4 |
| Sight radius setting | 7 | 7 |
| Technology level | 3 | 3 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP,NARADR | NAWEAP,NARADR |
| Permitted movement zone | Destroyer | Destroyer |
| Transport size usage | 3 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Spawned attacker type | V3ROCKET | V3ROCKET |
| Managed attacker count | 1 | 1 |
| Attacker replacement delay | 400 | 400 |
| Attacker reload delay | 0 | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 25 | 25 |
| Recycling value setting | Not explicitly set | 800 |
| Can enter tank bunkers | Not explicitly set | no |

**Red Alert 2 weapon paths:** Primary: [V3Launcher](reference/WEAPONS.md#ra2-v3launcher).

**Data source:** ra2.mix/local.mix/rules.ini, section V3, first property line 5712.

**Yuri's Revenge weapon paths:** Primary: [V3Launcher](reference/WEAPONS.md#yr-v3launcher).

**Data source:** expandmd01.mix/rulesmd.ini, section V3, first property line 7734.

<a id="zep"></a>

## Kirov Airship - ZEP

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Fly slowly toward a usable bombing position.
2. Release bombs on eligible targets.
3. Remain exposed to anti-air and use its configured crash/death effects if destroyed.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 2000 | 2000 |
| Starting health capacity | 2000 | 2000 |
| Armor class | light | medium |
| Movement rating | 5 | 5 |
| Sight radius setting | 8 | 8 |
| Technology level | 10 | 10 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP,NATECH | NAWEAP,NATECH |
| Permitted movement zone | Fly | Fly |
| Movement speed category | Hover | Hover |
| Transport size usage | 50 | 50 |
| Self-healing | Yes | Yes |
| Hidden from radar | no | no |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 30 | 30 |
| Recycling value setting | Not explicitly set | 2000 |
| Can enter tank bunkers | Not explicitly set | no |

**Red Alert 2 weapon paths:** Primary: [BlimpBomb](reference/WEAPONS.md#ra2-blimpbomb); Elite Primary: [BlimpBombE](reference/WEAPONS.md#ra2-blimpbombe).

**Data source:** ra2.mix/local.mix/rules.ini, section ZEP, first property line 7982.

**Yuri's Revenge weapon paths:** Primary: [BlimpBomb](reference/WEAPONS.md#yr-blimpbomb); Elite Primary: [BlimpBombE](reference/WEAPONS.md#yr-blimpbombe).

**Data source:** expandmd01.mix/rulesmd.ini, section ZEP, first property line 11213.

<a id="dron"></a>

## Terror Drone - DRON

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Reach a valid ground victim.
2. Enter its parasite interaction and cause internal damage.
3. Handle victim destruction or supported repair/removal; the drone does not keep acting as an ordinary visible tank.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 500 |
| Starting health capacity | 100 | 100 |
| Armor class | special_1 | special_1 |
| Movement rating | 10 | 10 |
| Sight radius setting | 4 | 4 |
| Technology level | 4 | 4 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Destroyer | Destroyer |
| Transport size usage | 2 | 2 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | yes | yes |
| Radiation immunity | yes | yes |
| Can crush through ordinary crushing logic | no | no |
| Naval-target selection mode | 6 | 6 |
| Threat contribution | 25 | 25 |
| Explosive destruction flag | no | no |
| Recycling value setting | Not explicitly set | 500 |
| Can enter tank bunkers | Not explicitly set | no |

**Red Alert 2 weapon paths:** Primary: [DroneJump](reference/WEAPONS.md#ra2-dronejump); Secondary: [VirtualScanner](reference/WEAPONS.md#ra2-virtualscanner).

**Data source:** ra2.mix/local.mix/rules.ini, section DRON, first property line 5763.

**Yuri's Revenge weapon paths:** Primary: [DroneJump](reference/WEAPONS.md#yr-dronejump); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section DRON, first property line 7570.

<a id="htk"></a>

## Flak Track - HTK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Choose flak fire for an eligible target or load infantry as ordered.
2. Carry passengers to a reachable destination.
3. Unload through the supported transport interaction; cargo and weapon roles coexist.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 500 |
| Starting health capacity | 180 | 180 |
| Armor class | heavy | heavy |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | 3 | 3 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Passenger slot capacity | 5 | 5 |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 3 | 3 |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 10 | 10 |
| Recycling value setting | Not explicitly set | 500 |

**Red Alert 2 weapon paths:** Primary: [FlakTrackGun](reference/WEAPONS.md#ra2-flaktrackgun); Secondary: [FlakTrackAAGun](reference/WEAPONS.md#ra2-flaktrackaagun); Elite Primary: [FlakTrackGunE](reference/WEAPONS.md#ra2-flaktrackgune); Elite Secondary: [FlakTrackAAGunE](reference/WEAPONS.md#ra2-flaktrackaagune).

**Data source:** ra2.mix/local.mix/rules.ini, section HTK, first property line 6232.

**Yuri's Revenge weapon paths:** Primary: [FlakTrackGun](reference/WEAPONS.md#yr-flaktrackgun); Secondary: [FlakTrackAAGun](reference/WEAPONS.md#yr-flaktrackaagun); Elite Primary: [FlakTrackGunE](reference/WEAPONS.md#yr-flaktrackgune); Elite Secondary: [FlakTrackAAGunE](reference/WEAPONS.md#yr-flaktrackaagune).

**Data source:** expandmd01.mix/rulesmd.ini, section HTK, first property line 7627.

<a id="dest"></a>

## Destroyer - DEST

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Engage supported surface/shore targets with its gun.
2. Use its spawned anti-submarine aircraft for supported submerged targets.
3. Manage that aircraft separately from the ship's own gun/reload.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 600 | 600 |
| Armor class | heavy | heavy |
| Movement rating | 6 | 6 |
| Sight radius setting | 7 | 7 |
| Technology level | 4 | 4 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAYARD | GAYARD |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Transport size usage | 30 | 30 |
| Can crush through ordinary crushing logic | no | no |
| Detector service | yes | yes |
| Detection range setting | 8 | 8 |
| Spawned attacker type | ASW | ASW |
| Managed attacker count | 1 | 1 |
| Attacker replacement delay | 400 | 400 |
| Attacker reload delay | 150 | 150 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Naval-target selection mode | 1 | 1 |
| Threat contribution | 15 | 15 |
| Recycling value setting | Not explicitly set | 1000 |

**Red Alert 2 weapon paths:** Primary: [155mm](reference/WEAPONS.md#ra2-155mm); Secondary: [ASWLauncher](reference/WEAPONS.md#ra2-aswlauncher); Elite Primary: [155mmE](reference/WEAPONS.md#ra2-155mme).

**Data source:** ra2.mix/local.mix/rules.ini, section DEST, first property line 5657.

**Yuri's Revenge weapon paths:** Primary: [155mm](reference/WEAPONS.md#yr-155mm); Secondary: [ASWLauncher](reference/WEAPONS.md#yr-aswlauncher); Elite Primary: [155mmE](reference/WEAPONS.md#yr-155mme).

**Data source:** expandmd01.mix/rulesmd.ini, section DEST, first property line 7076.

<a id="sub"></a>

## Typhoon Attack Sub - SUB

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move through legal water using its submerged/cloak state.
2. Reveal/engage as required to fire at eligible naval targets.
3. Remain subject to detection and anti-submarine weapons.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 600 | 600 |
| Armor class | heavy | heavy |
| Movement rating | 4 | 4 |
| Sight radius setting | 4 | 4 |
| Technology level | 2 | 2 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAYARD | NAYARD |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Transport size usage | 20 | 20 |
| Can crush through ordinary crushing logic | no | no |
| Can cloak | yes | yes |
| Detector service | yes | yes |
| Detection range setting | 4 | 7 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Ground-target selection mode | 1 | 1 |
| Naval-target selection mode | 5 | 5 |
| Threat contribution | 20 | 20 |
| Recycling value setting | Not explicitly set | 1000 |

**Red Alert 2 weapon paths:** Primary: [SubTorpedo](reference/WEAPONS.md#ra2-subtorpedo); Elite Primary: [SubTorpedoE](reference/WEAPONS.md#ra2-subtorpedoe).

**Data source:** ra2.mix/local.mix/rules.ini, section SUB, first property line 5183.

**Yuri's Revenge weapon paths:** Primary: [SubTorpedo](reference/WEAPONS.md#yr-subtorpedo); Elite Primary: [SubTorpedoE](reference/WEAPONS.md#yr-subtorpedoe).

**Data source:** expandmd01.mix/rulesmd.ini, section SUB, first property line 8002.

<a id="aegis"></a>

## Aegis Cruiser - AEGIS

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Scan for eligible air or missile targets.
2. Choose and fire its anti-air weapon.
3. Use reload/weapon-selection rules; its anti-air role does not imply a shore cannon.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1200 | 1200 |
| Starting health capacity | 800 | 800 |
| Armor class | light | light |
| Movement rating | 4 | 4 |
| Sight radius setting | 8 | 8 |
| Technology level | 7 | 7 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAYARD,RADAR | GAYARD,RADAR |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Transport size usage | 30 | 30 |
| Can crush through ordinary crushing logic | no | no |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Ground-target selection mode | 1 | 1 |
| Naval-target selection mode | 6 | 6 |
| Threat contribution | 25 | 25 |
| Recycling value setting | Not explicitly set | 1200 |

**Red Alert 2 weapon paths:** Primary: [Medusa](reference/WEAPONS.md#ra2-medusa); Elite Primary: [MedusaE](reference/WEAPONS.md#ra2-medusae).

**Data source:** ra2.mix/local.mix/rules.ini, section AEGIS, first property line 5286.

**Yuri's Revenge weapon paths:** Primary: [Medusa](reference/WEAPONS.md#yr-medusa); Elite Primary: [MedusaE](reference/WEAPONS.md#yr-medusae).

**Data source:** expandmd01.mix/rulesmd.ini, section AEGIS, first property line 7187.

<a id="lcrf"></a>

## Amphibious Transport - LCRF

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Load infantry or vehicles permitted by passenger-size/capacity rules.
2. Travel over legal land/water to a usable unloading shore or location.
3. Unload into available cells; do not assume a full transport can unload onto blocked terrain.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 900 | 900 |
| Starting health capacity | 300 | 300 |
| Armor class | light | light |
| Movement rating | 6 | 6 |
| Sight radius setting | 6 | 6 |
| Technology level | 4 | 4 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAYARD | GAYARD |
| Permitted movement zone | Amphibious | Amphibious |
| Movement speed category | Hover | Hover |
| Passenger slot capacity | 12 | 12 |
| Largest passenger-size setting | 6 | 6 |
| Transport size usage | 16 | 16 |
| Can gain rank | no | no |
| Can crush through ordinary crushing logic | no | no |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Threat contribution | 3 | 3 |
| Recycling value setting | Not explicitly set | 900 |
| Can enter tank bunkers | Not explicitly set | no |

**Data source:** ra2.mix/local.mix/rules.ini, section LCRF, first property line 6168.

**Data source:** expandmd01.mix/rulesmd.ini, section LCRF, first property line 7013.

<a id="dred"></a>

## Dreadnought - DRED

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Acquire a supported bombardment target.
2. Launch its managed missile attackers.
3. Resolve independent missile travel/impact and prepare subsequent launches.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 2000 | 2000 |
| Starting health capacity | 800 | 800 |
| Armor class | heavy | heavy |
| Movement rating | 4 | 4 |
| Sight radius setting | 7 | 7 |
| Technology level | 6 | 6 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAYARD,NATECH | NAYARD,NATECH |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Transport size usage | 50 | 50 |
| Can crush through ordinary crushing logic | no | no |
| Spawned attacker type | DMISL | DMISL |
| Managed attacker count | 2 | 2 |
| Attacker replacement delay | 80 | 80 |
| Attacker reload delay | 0 | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Threat contribution | 25 | 25 |
| Recycling value setting | Not explicitly set | 2000 |

**Red Alert 2 weapon paths:** Primary: [DredLauncher](reference/WEAPONS.md#ra2-dredlauncher).

**Data source:** ra2.mix/local.mix/rules.ini, section DRED, first property line 5451.

**Yuri's Revenge weapon paths:** Primary: [DredLauncher](reference/WEAPONS.md#yr-dredlauncher).

**Data source:** expandmd01.mix/rulesmd.ini, section DRED, first property line 8120.

<a id="shad"></a>

## NightHawk Transport - SHAD

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Load eligible infantry.
2. Fly to a legal destination and unload.
3. Use its gun where supported; radar invisibility does not mean immunity to visual detection or anti-air.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 175 | 175 |
| Armor class | light | light |
| Movement rating | 14 | 14 |
| Sight radius setting | 7 | 7 |
| Technology level | 7 | 7 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP | GAWEAP |
| Permitted movement zone | Fly | Fly |
| Movement speed category | Hover | Hover |
| Passenger slot capacity | 5 | 5 |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 15 | 15 |
| Can gain rank | yes | yes |
| Hidden from radar | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 0 | 0 |
| Can enter tank bunkers | Not explicitly set | no |

**Red Alert 2 weapon paths:** Primary: [BlackHawkCannon](reference/WEAPONS.md#ra2-blackhawkcannon); Elite Primary: [BlackHawkCannonE](reference/WEAPONS.md#ra2-blackhawkcannone).

**Data source:** ra2.mix/local.mix/rules.ini, section SHAD, first property line 7913.

**Yuri's Revenge weapon paths:** Primary: [BlackHawkCannon](reference/WEAPONS.md#yr-blackhawkcannon); Elite Primary: [BlackHawkCannonE](reference/WEAPONS.md#yr-blackhawkcannone).

**Data source:** expandmd01.mix/rulesmd.ini, section SHAD, first property line 10512.

<a id="sqd"></a>

## Giant Squid - SQD

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Approach a legal naval victim.
2. Attach through the squid/parasite-like special interaction and damage it.
3. Handle release/interruption; Dolphin counterplay does not make every weapon a release tool.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 200 | 200 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 5 | 5 |
| Technology level | 9 | 9 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAYARD,NATECH | NAYARD,NATECH |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Transport size usage | 30 | 30 |
| Can gain rank | yes | yes |
| Self-healing | yes | yes |
| Immune to ordinary psychic control | yes | yes |
| Can crush through ordinary crushing logic | no | no |
| Can cloak | yes | yes |
| Detector service | yes | yes |
| Detection range setting | 4 | 8 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | STRONGER,FIREPOWER,ROF | STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Ground-target selection mode | 1 | 1 |
| Naval-target selection mode | 3 | 3 |
| Threat contribution | 25 | 25 |
| Explosive destruction flag | no | no |
| Attached bombs permitted | yes | yes |
| Recycling value setting | Not explicitly set | 1000 |

**Red Alert 2 weapon paths:** Primary: [SquidGrab](reference/WEAPONS.md#ra2-squidgrab); Secondary: [SquidPunch](reference/WEAPONS.md#ra2-squidpunch); Elite Primary: [SquidGrabE](reference/WEAPONS.md#ra2-squidgrabe); Elite Secondary: [SquidPunchE](reference/WEAPONS.md#ra2-squidpunche).

**Data source:** ra2.mix/local.mix/rules.ini, section SQD, first property line 5819.

**Yuri's Revenge weapon paths:** Primary: [SquidGrab](reference/WEAPONS.md#yr-squidgrab); Secondary: [SquidPunch](reference/WEAPONS.md#yr-squidpunch); Elite Primary: [SquidGrabE](reference/WEAPONS.md#yr-squidgrabe); Elite Secondary: [SquidPunchE](reference/WEAPONS.md#yr-squidpunche).

**Data source:** expandmd01.mix/rulesmd.ini, section SQD, first property line 8052.

<a id="dlph"></a>

## Dolphin - DLPH

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move through valid water and use its cloak/detection-related state.
2. Fire its sonic weapon at supported naval targets.
3. Its supported interaction can help free squid-held ships; check actual target/effect eligibility.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 500 |
| Starting health capacity | 200 | 200 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 4 | 4 |
| Technology level | 5 | 5 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAYARD,GATECH | GAYARD,GATECH |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Transport size usage | 15 | 15 |
| Can cloak | yes | yes |
| Detector service | yes | yes |
| Detection range setting | 4 | 8 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Ground-target selection mode | 1 | 1 |
| Naval-target selection mode | 5 | 5 |
| Threat contribution | 20 | 20 |
| Recycling value setting | Not explicitly set | 500 |

**Red Alert 2 weapon paths:** Primary: [SonicZap](reference/WEAPONS.md#ra2-soniczap); Elite Primary: [SonicZapE](reference/WEAPONS.md#ra2-soniczape).

**Data source:** ra2.mix/local.mix/rules.ini, section DLPH, first property line 5231.

**Yuri's Revenge weapon paths:** Primary: [SonicZap](reference/WEAPONS.md#yr-soniczap); Elite Primary: [SonicZapE](reference/WEAPONS.md#yr-soniczape).

**Data source:** expandmd01.mix/rulesmd.ini, section DLPH, first property line 7131.

<a id="smcv"></a>

## Soviet Construction Vehicle - SMCV

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Find a legal foundation and deploy into the Soviet Construction Yard.
2. Update the owner's building availability.
3. Use the yard's building queue until sold, destroyed or undeployed where allowed.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 3000 | 3000 |
| Starting health capacity | 1000 | 1000 |
| Armor class | heavy | heavy |
| Movement rating | 4 | 4 |
| Sight radius setting | 6 | 6 |
| Technology level | 10 | 10 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP,NADEPT | NAWEAP,NADEPT |
| Permitted movement zone | Normal | Normal |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Can crush through ordinary crushing logic | yes | yes |
| Deploys into | NACNST | NACNST |
| Threat contribution | 0 | 0 |
| Recycling value setting | Not explicitly set | 3000 |
| Can enter tank bunkers | Not explicitly set | no |

**Data source:** ra2.mix/local.mix/rules.ini, section SMCV, first property line 6130.

**Data source:** expandmd01.mix/rulesmd.ini, section SMCV, first property line 7839.

<a id="tnkd"></a>

## Tank Destroyer - TNKD

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use the country-restricted tank-destroyer record when available.
2. Engage armored ground targets with its specialized weapon.
3. Check effectiveness against other armor classes instead of assuming universal superiority.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 900 | 900 |
| Starting health capacity | 400 | 400 |
| Armor class | heavy | heavy |
| Movement rating | 5 | 5 |
| Sight radius setting | 8 | 8 |
| Technology level | 2 | 2 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required countries | Germans | Germans |
| Required structures/groups | GAWEAP,RADAR | GAWEAP,RADAR |
| Permitted movement zone | Normal | Normal |
| Transport size usage | 3 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 15 | 15 |
| Recycling value setting | Not explicitly set | 900 |

**Red Alert 2 weapon paths:** Primary: [SABOT](reference/WEAPONS.md#ra2-sabot); Elite Primary: [SABOTE](reference/WEAPONS.md#ra2-sabote).

**Data source:** ra2.mix/local.mix/rules.ini, section TNKD, first property line 6863.

**Yuri's Revenge weapon paths:** Primary: [SABOT](reference/WEAPONS.md#yr-sabot); Elite Primary: [SABOTE](reference/WEAPONS.md#yr-sabote).

**Data source:** expandmd01.mix/rulesmd.ini, section TNKD, first property line 7477.

<a id="howi"></a>

## Howitzer - HOWI

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 750 | 750 |
| Starting health capacity | 200 | 200 |
| Armor class | light | light |
| Movement rating | 5 | 5 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required countries | Alliance | Alliance |
| Required structures/groups | GAWEAP | GAWEAP |
| Permitted movement zone | Normal | Normal |
| Transport size usage | 3 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 15 | 15 |
| Recycling value setting | Not explicitly set | 750 |

**Red Alert 2 weapon paths:** Primary: [HowitzerGun](reference/WEAPONS.md#ra2-howitzergun).

**Data source:** ra2.mix/local.mix/rules.ini, section HOWI, first property line 6906.

**Yuri's Revenge weapon paths:** Primary: [HowitzerGun](reference/WEAPONS.md#yr-howitzergun).

**Data source:** expandmd01.mix/rulesmd.ini, section HOWI, first property line 7522.

<a id="ttnk"></a>

## Tesla Tank - TTNK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use the country-restricted Tesla Tank when available.
2. Move into range and fire its electric weapon.
3. Apply the actual warhead effectiveness and recharge rules.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1200 | 1200 |
| Starting health capacity | 300 | 300 |
| Armor class | heavy | heavy |
| Movement rating | 6 | 6 |
| Sight radius setting | 8 | 8 |
| Technology level | 10 | 10 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required countries | Russians | Russians |
| Required structures/groups | NAWEAP,NARADR | NAWEAP,NARADR |
| Permitted movement zone | Destroyer | Destroyer |
| Transport size usage | 3 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 40 | 40 |
| Production-time multiplier | Not explicitly set | 1.2 |
| Recycling value setting | Not explicitly set | 1200 |

**Red Alert 2 weapon paths:** Primary: [TankBolt](reference/WEAPONS.md#ra2-tankbolt); Elite Primary: [TankBoltE](reference/WEAPONS.md#ra2-tankbolte).

**Data source:** ra2.mix/local.mix/rules.ini, section TTNK, first property line 7016.

**Yuri's Revenge weapon paths:** Primary: [TankBolt](reference/WEAPONS.md#yr-tankbolt); Elite Primary: [TankBoltE](reference/WEAPONS.md#yr-tankbolte).

**Data source:** expandmd01.mix/rulesmd.ini, section TTNK, first property line 8331.

<a id="hind"></a>

## Hind Transport - HIND

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 300 | 300 |
| Armor class | light | light |
| Movement rating | 15 | 15 |
| Sight radius setting | 7 | 7 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required countries | Confederation | Confederation |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Fly | Fly |
| Movement speed category | Hover | Hover |
| Passenger slot capacity | 10 | 10 |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 15 | 15 |
| Hidden from radar | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 0 | 0 |

**Red Alert 2 weapon paths:** Primary: [BlackHawkCannon](reference/WEAPONS.md#ra2-blackhawkcannon).

**Data source:** ra2.mix/local.mix/rules.ini, section HIND, first property line 7851.

**Yuri's Revenge weapon paths:** Primary: [BlackHawkCannon](reference/WEAPONS.md#yr-blackhawkcannon).

**Data source:** expandmd01.mix/rulesmd.ini, section HIND, first property line 10811.

<a id="ltnk"></a>

## Lasher Light Tank - LTNK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Compare versions: this ID is a legacy Light Tank in RA2 and Yuri's Lasher in the expansion.
2. Use the selected version's eligibility, weapon and health.
3. Move and fire as that version's ground tank; do not import the expansion's availability into RA2.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 600 | 700 |
| Starting health capacity | 200 | 300 |
| Armor class | heavy | heavy |
| Movement rating | 8 | 7 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | 2 |
| Permitted country list | Russians,Confederation,Africans,Arabs | YuriCountry |
| Required countries | Arabs | Not explicitly set |
| Required structures/groups | NAWEAP | YAWEAP |
| Permitted movement zone | Destroyer | Destroyer |
| Transport size usage | 6 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 40 | 40 |
| Production-time multiplier | Not explicitly set | 1.5 |
| Recycling value setting | Not explicitly set | 700 |

**Red Alert 2 weapon paths:** Primary: [90mm](reference/WEAPONS.md#ra2-90mm).

**Data source:** ra2.mix/local.mix/rules.ini, section LTNK, first property line 6523.

**Yuri's Revenge weapon paths:** Primary: [ATGUN](reference/WEAPONS.md#yr-atgun); Elite Primary: [ATGUNE](reference/WEAPONS.md#yr-atgune).

**Data source:** expandmd01.mix/rulesmd.ini, section LTNK, first property line 8435.

<a id="cmon"></a>

## Chrono Miner - CMON

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1400 | 1400 |
| Starting health capacity | 1000 | 1000 |
| Armor class | medium | medium |
| Movement rating | 4 | 4 |
| Sight radius setting | 4 | 4 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Permitted movement zone | Crusher | Crusher |
| Can gain rank | no | no |
| Self-healing | yes | yes |
| Radiation immunity | yes | yes |
| Can crush through ordinary crushing logic | yes | yes |
| Conventional harvester behavior | yes | yes |
| Threat contribution | 0 | 0 |
| Compatible aircraft docks | NAREFN,GAREFN | NAREFN,GAREFN |

**Data source:** ra2.mix/local.mix/rules.ini, section CMON, first property line 5983.

**Data source:** expandmd01.mix/rulesmd.ini, section CMON, first property line 7304.

<a id="cmin"></a>

## Chrono Miner - CMIN

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Drive outward to a resource field.
2. Collect cargo and invoke its chrono return toward a usable refinery.
3. Unload and repeat; valid destination/placement constraints still apply.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1400 | 1400 |
| Starting health capacity | 1000 | 1000 |
| Armor class | medium | medium |
| Movement rating | 4 | 4 |
| Sight radius setting | 4 | 4 |
| Technology level | 1 | 1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP,PROC | GAWEAP,PROC |
| Permitted movement zone | Crusher | Crusher |
| Transport size usage | 3 | 3 |
| Resource cargo capacity | 20 | 20 |
| Can gain rank | no | no |
| Self-healing | yes | yes |
| Immune to ordinary psychic control | yes | yes |
| Radiation immunity | yes | yes |
| Can crush through ordinary crushing logic | yes | yes |
| Conventional harvester behavior | yes | yes |
| Threat contribution | 0 | 0 |
| Compatible aircraft docks | NAREFN,GAREFN | NAREFN,GAREFN |
| Resource-gathering role | Not explicitly set | yes |
| Recycling value setting | Not explicitly set | 1400 |
| Can enter tank bunkers | Not explicitly set | no |

**Data source:** ra2.mix/local.mix/rules.ini, section CMIN, first property line 6029.

**Data source:** expandmd01.mix/rulesmd.ini, section CMIN, first property line 7352.

<a id="sref"></a>

## Prism Tank - SREF

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Position within its prism weapon range.
2. Fire the primary beam.
3. Resolve its configured follow-on/splitting effects through the weapon/warhead chain.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1200 | 1200 |
| Starting health capacity | 150 | 150 |
| Armor class | light | light |
| Movement rating | 4 | 4 |
| Sight radius setting | 8 | 8 |
| Technology level | 8 | 8 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP,GATECH | GAWEAP,GATECH |
| Permitted movement zone | Destroyer | Destroyer |
| Transport size usage | 3 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 40 | 40 |
| Recycling value setting | Not explicitly set | 1200 |

**Red Alert 2 weapon paths:** Weapon1: [Comet](reference/WEAPONS.md#ra2-comet); Elite Weapon1: [SuperComet](reference/WEAPONS.md#ra2-supercomet).

**Data source:** ra2.mix/local.mix/rules.ini, section SREF, first property line 7062.

**Yuri's Revenge weapon paths:** Weapon1: [Comet](reference/WEAPONS.md#yr-comet); Elite Weapon1: [SuperComet](reference/WEAPONS.md#yr-supercomet).

**Data source:** expandmd01.mix/rulesmd.ini, section SREF, first property line 6862.

<a id="xcomet"></a>

## Placeholder - XCOMET

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 2000 | 2000 |
| Starting health capacity | 300 | 300 |
| Armor class | heavy | heavy |
| Movement rating | 4 | 4 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP,GATECH | GAWEAP,GATECH |
| Permitted movement zone | Destroyer | Destroyer |
| Transport size usage | 3 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Threat contribution | 40 | 40 |

**Red Alert 2 weapon paths:** Primary: [CometFragment](reference/WEAPONS.md#ra2-cometfragment); Secondary: [TeslaFragment](reference/WEAPONS.md#ra2-teslafragment); Elite Primary: [SuperCometFragment](reference/WEAPONS.md#ra2-supercometfragment).

**Data source:** ra2.mix/local.mix/rules.ini, section XCOMET, first property line 7114.

**Yuri's Revenge weapon paths:** Primary: [CometFragment](reference/WEAPONS.md#yr-cometfragment); Secondary: [TeslaFragment](reference/WEAPONS.md#yr-teslafragment); Elite Primary: [SuperCometFragment](reference/WEAPONS.md#yr-supercometfragment).

**Data source:** expandmd01.mix/rulesmd.ini, section XCOMET, first property line 9657.

<a id="hyd"></a>

## Sea Scorpion - HYD

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move on legal water.
2. Choose supported air/ground flak targeting.
3. Resolve flak attacks while protecting more specialized naval attackers.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 600 | 600 |
| Starting health capacity | 400 | 400 |
| Armor class | heavy | heavy |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | 6 | 6 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAYARD,NARADR | NAYARD,NARADR |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Transport size usage | 20 | 20 |
| Can crush through ordinary crushing logic | no | no |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Threat contribution | 25 | 25 |
| Recycling value setting | Not explicitly set | 600 |

**Red Alert 2 weapon paths:** Primary: [FlakTrackGun](reference/WEAPONS.md#ra2-flaktrackgun); Secondary: [FlakWeapon](reference/WEAPONS.md#ra2-flakweapon); Elite Primary: [FlakTrackGunE](reference/WEAPONS.md#ra2-flaktrackgune); Elite Secondary: [FlakWeaponE](reference/WEAPONS.md#ra2-flakweapone).

**Data source:** ra2.mix/local.mix/rules.ini, section HYD, first property line 5609.

**Yuri's Revenge weapon paths:** Primary: [FlakTrackGun](reference/WEAPONS.md#yr-flaktrackgun); Secondary: [FlakWeapon](reference/WEAPONS.md#yr-flakweapon); Elite Primary: [FlakTrackGunE](reference/WEAPONS.md#yr-flaktrackgune); Elite Secondary: [FlakWeaponE](reference/WEAPONS.md#yr-flakweapone).

**Data source:** expandmd01.mix/rulesmd.ini, section HYD, first property line 7954.

<a id="mgtk"></a>

## Mirage Tank - MGTK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Move visibly to position.
2. When stationary, use its configured disguise behavior.
3. Fire at eligible enemies, briefly exposing the attack state; disguise does not add armor.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 200 | 200 |
| Armor class | light | light |
| Movement rating | 7 | 7 |
| Sight radius setting | 9 | 9 |
| Technology level | 9 | 9 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP,GATECH | GAWEAP,GATECH |
| Permitted movement zone | Normal | Normal |
| Transport size usage | 3 | 3 |
| Can crush through ordinary crushing logic | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 15 | 15 |
| Recycling value setting | Not explicitly set | 1000 |

**Red Alert 2 weapon paths:** Primary: [MirageGun](reference/WEAPONS.md#ra2-miragegun); Elite Secondary: [MirageGunE](reference/WEAPONS.md#ra2-miragegune).

**Data source:** ra2.mix/local.mix/rules.ini, section MGTK, first property line 6615.

**Yuri's Revenge weapon paths:** Primary: [MirageGun](reference/WEAPONS.md#yr-miragegun); Elite Secondary: [MirageGunE](reference/WEAPONS.md#yr-miragegune).

**Data source:** expandmd01.mix/rulesmd.ini, section MGTK, first property line 6808.

<a id="fv"></a>

## IFV - FV

**Registered in:** Red Alert 2, Yuri's Revenge.

1. With no passenger, use the IFV's default weapon.
2. Load one eligible infantry passenger and read its IFV mode.
3. Switch the vehicle's weapon/turret role accordingly; an Engineer produces a repair role, not an offensive machine gun.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 600 | 600 |
| Starting health capacity | 200 | 200 |
| Armor class | light | light |
| Movement rating | 10 | 10 |
| Sight radius setting | 8 | 8 |
| Technology level | 3 | 3 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP | GAWEAP |
| Permitted movement zone | Normal | Normal |
| Passenger slot capacity | 1 | 1 |
| Largest passenger-size setting | 1 | 1 |
| Transport size usage | 3 | 3 |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 10 | 10 |
| Recycling value setting | Not explicitly set | 600 |

**Red Alert 2 weapon paths:** Primary: [HoverMissile](reference/WEAPONS.md#ra2-hovermissile); Weapon1: [HoverMissile](reference/WEAPONS.md#ra2-hovermissile); Elite Weapon1: [HoverMissileE](reference/WEAPONS.md#ra2-hovermissilee); Weapon2: [RepairBullet](reference/WEAPONS.md#ra2-repairbullet); Elite Weapon2: [RepairBullet](reference/WEAPONS.md#ra2-repairbullet); Weapon3: [CRM60](reference/WEAPONS.md#ra2-crm60); Elite Weapon3: [CRM60](reference/WEAPONS.md#ra2-crm60); Weapon4: [CRFlakGuyGun](reference/WEAPONS.md#ra2-crflakguygun); Elite Weapon4: [CRFlakGuyGun](reference/WEAPONS.md#ra2-crflakguygun); Weapon5: [CRMP5](reference/WEAPONS.md#ra2-crmp5); Elite Weapon5: [CRMP5](reference/WEAPONS.md#ra2-crmp5); Weapon6: [AWPE](reference/WEAPONS.md#ra2-awpe); Elite Weapon6: [AWPE](reference/WEAPONS.md#ra2-awpe); Weapon7: [CRElectricBolt](reference/WEAPONS.md#ra2-crelectricbolt); Elite Weapon7: [CRElectricBolt](reference/WEAPONS.md#ra2-crelectricbolt); Weapon8: [CRNuke](reference/WEAPONS.md#ra2-crnuke); Elite Weapon8: [CRNuke](reference/WEAPONS.md#ra2-crnuke); Weapon9: [CRMindControl](reference/WEAPONS.md#ra2-crmindcontrol); Elite Weapon9: [CRMindControl](reference/WEAPONS.md#ra2-crmindcontrol); Weapon10: [CRRadBeamWeapon](reference/WEAPONS.md#ra2-crradbeamweapon); Elite Weapon10: [CRRadBeamWeapon](reference/WEAPONS.md#ra2-crradbeamweapon); Weapon11: [CRNeutronRifle](reference/WEAPONS.md#ra2-crneutronrifle); Elite Weapon11: [CRNeutronRifle](reference/WEAPONS.md#ra2-crneutronrifle); Weapon12: [CRTerrorBomb](reference/WEAPONS.md#ra2-crterrorbomb); Elite Weapon12: [CRTerrorBomb](reference/WEAPONS.md#ra2-crterrorbomb); Weapon13: [CowShot](reference/WEAPONS.md#ra2-cowshot); Elite Weapon13: [CowShot](reference/WEAPONS.md#ra2-cowshot); Death Weapon: [CRNuke](reference/WEAPONS.md#ra2-crnuke); Elite Primary: [HoverMissileE](reference/WEAPONS.md#ra2-hovermissilee).

**Data source:** ra2.mix/local.mix/rules.ini, section FV, first property line 6667.

**Yuri's Revenge weapon paths:** Primary: [HoverMissile](reference/WEAPONS.md#yr-hovermissile); Weapon1: [HoverMissile](reference/WEAPONS.md#yr-hovermissile); Elite Weapon1: [HoverMissileE](reference/WEAPONS.md#yr-hovermissilee); Weapon2: [RepairBullet](reference/WEAPONS.md#yr-repairbullet); Elite Weapon2: [RepairBullet](reference/WEAPONS.md#yr-repairbullet); Weapon3: [CRM60](reference/WEAPONS.md#yr-crm60); Elite Weapon3: [CRM60](reference/WEAPONS.md#yr-crm60); Weapon4: [CRFlakGuyGun](reference/WEAPONS.md#yr-crflakguygun); Elite Weapon4: [CRFlakGuyGun](reference/WEAPONS.md#yr-crflakguygun); Weapon5: [CRMP5](reference/WEAPONS.md#yr-crmp5); Elite Weapon5: [CRMP5](reference/WEAPONS.md#yr-crmp5); Weapon6: [AWPE](reference/WEAPONS.md#yr-awpe); Elite Weapon6: [AWPE](reference/WEAPONS.md#yr-awpe); Weapon7: [CRElectricBolt](reference/WEAPONS.md#yr-crelectricbolt); Elite Weapon7: [CRElectricBolt](reference/WEAPONS.md#yr-crelectricbolt); Weapon8: [CRNuke](reference/WEAPONS.md#yr-crnuke); Elite Weapon8: [CRNuke](reference/WEAPONS.md#yr-crnuke); Weapon9: [CRMindControl](reference/WEAPONS.md#yr-crmindcontrol); Elite Weapon9: [CRMindControl](reference/WEAPONS.md#yr-crmindcontrol); Weapon10: [CRRadBeamWeapon](reference/WEAPONS.md#yr-crradbeamweapon); Elite Weapon10: [CRRadBeamWeapon](reference/WEAPONS.md#yr-crradbeamweapon); Weapon11: [CRNeutronRifle](reference/WEAPONS.md#yr-crneutronrifle); Elite Weapon11: [CRNeutronRifle](reference/WEAPONS.md#yr-crneutronrifle); Weapon12: [CRTerrorBomb](reference/WEAPONS.md#yr-crterrorbomb); Elite Weapon12: [CRTerrorBomb](reference/WEAPONS.md#yr-crterrorbomb); Weapon13: [CowShot](reference/WEAPONS.md#yr-cowshot); Elite Weapon13: [CowShot](reference/WEAPONS.md#yr-cowshot); Weapon14: [CRPsychicJab](reference/WEAPONS.md#yr-crpsychicjab); Elite Weapon14: [CRPsychicJab](reference/WEAPONS.md#yr-crpsychicjab); Weapon15: [CRVirusGun](reference/WEAPONS.md#yr-crvirusgun); Elite Weapon15: [CRVirusGun](reference/WEAPONS.md#yr-crvirusgun); Weapon16: [CRSuperMindBlast](reference/WEAPONS.md#yr-crsupermindblast); Elite Weapon16: [CRSuperMindBlast](reference/WEAPONS.md#yr-crsupermindblast); Weapon17: [CRMissileLauncher](reference/WEAPONS.md#yr-crmissilelauncher); Elite Weapon17: [CRMissileLauncher](reference/WEAPONS.md#yr-crmissilelauncher); Death Weapon: [CRNuke](reference/WEAPONS.md#yr-crnuke); Elite Primary: [HoverMissileE](reference/WEAPONS.md#yr-hovermissilee).

**Data source:** expandmd01.mix/rulesmd.ini, section FV, first property line 6655.

<a id="deathdummy"></a>

## DEATHDUMMY - DEATHDUMMY

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |

**Red Alert 2 weapon paths:** Primary: [DefaultDeathWeapon](reference/WEAPONS.md#ra2-defaultdeathweapon).

**Data source:** ra2.mix/local.mix/rules.ini, section DEATHDUMMY, first property line 6859.

**Yuri's Revenge weapon paths:** Primary: [DefaultDeathWeapon](reference/WEAPONS.md#yr-defaultdeathweapon).

**Data source:** expandmd01.mix/rulesmd.ini, section DEATHDUMMY, first property line 9654.

<a id="vlad"></a>

## Vladimir's Command Ship - VLAD

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 2500 | 2500 |
| Starting health capacity | 1500 | 1500 |
| Armor class | heavy | heavy |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Excluded countries | Russians | Russians |
| Required structures/groups | NAYARD,NATECH | NAYARD,NATECH |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Transport size usage | 50 | 50 |
| Can crush through ordinary crushing logic | no | no |
| Spawned attacker type | DMISL | DMISL |
| Managed attacker count | 2 | 2 |
| Attacker replacement delay | 80 | 80 |
| Attacker reload delay | 0 | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Threat contribution | 25 | 25 |
| Recycling value setting | Not explicitly set | 2500 |

**Red Alert 2 weapon paths:** Primary: [DredLauncher](reference/WEAPONS.md#ra2-dredlauncher).

**Data source:** ra2.mix/local.mix/rules.ini, section VLAD, first property line 5556.

**Yuri's Revenge weapon paths:** Primary: [DredLauncher](reference/WEAPONS.md#yr-dredlauncher).

**Data source:** expandmd01.mix/rulesmd.ini, section VLAD, first property line 9121.

<a id="dtruck"></a>

## Demolition Truck - DTRUCK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Drive toward its intended detonation position.
2. Trigger its configured death/suicide explosion.
3. Resolve the explosive/radiation effects, including danger to friendly objects.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1500 | 1500 |
| Starting health capacity | 150 | 150 |
| Armor class | light | light |
| Movement rating | 5 | 5 |
| Sight radius setting | 5 | 5 |
| Technology level | 10 | 10 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Required countries | Africans | Africans |
| Required structures/groups | NAWEAP,RADAR | NAWEAP,RADAR |
| Permitted movement zone | Normal | Normal |
| Transport size usage | 3 | 3 |
| Can gain rank | no | no |
| Self-healing | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 50 | 50 |
| Explosive destruction flag | yes | yes |
| Recycling value setting | Not explicitly set | 1500 |

**Red Alert 2 weapon paths:** Primary: [Demobomb](reference/WEAPONS.md#ra2-demobomb); Death Weapon: [Demobomb](reference/WEAPONS.md#ra2-demobomb).

**Data source:** ra2.mix/local.mix/rules.ini, section DTRUCK, first property line 5059.

**Yuri's Revenge weapon paths:** Primary: [Demobomb](reference/WEAPONS.md#yr-demobomb); Death Weapon: [Demobomb](reference/WEAPONS.md#yr-demobomb).

**Data source:** expandmd01.mix/rulesmd.ini, section DTRUCK, first property line 8381.

<a id="propa"></a>

## Propaganda Truck - PROPA

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Passenger slot capacity | 5 | 5 |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 3 | 3 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |

**Data source:** ra2.mix/local.mix/rules.ini, section PROPA, first property line 7158.

**Data source:** expandmd01.mix/rulesmd.ini, section PROPA, first property line 9701.

<a id="cona"></a>

## Excavator - CONA

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 3 | 3 |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CONA, first property line 7205.

**Data source:** expandmd01.mix/rulesmd.ini, section CONA, first property line 9749.

<a id="cop"></a>

## Police Car - COP

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section COP, first property line 7253.

**Data source:** expandmd01.mix/rulesmd.ini, section COP, first property line 9799.

<a id="euroc"></a>

## Automobile - EUROC

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section EUROC, first property line 7301.

**Data source:** expandmd01.mix/rulesmd.ini, section EUROC, first property line 9849.

<a id="limo"></a>

## Limousine - LIMO

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section LIMO, first property line 7348.

**Data source:** expandmd01.mix/rulesmd.ini, section LIMO, first property line 9898.

<a id="stang"></a>

## Automobile - STANG

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section STANG, first property line 7395.

**Data source:** expandmd01.mix/rulesmd.ini, section STANG, first property line 9947.

<a id="suvb"></a>

## Automobile - SUVB

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section SUVB, first property line 7442.

**Data source:** expandmd01.mix/rulesmd.ini, section SUVB, first property line 9996.

<a id="suvw"></a>

## Automobile - SUVW

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section SUVW, first property line 7489.

**Data source:** expandmd01.mix/rulesmd.ini, section SUVW, first property line 10045.

<a id="taxi"></a>

## Taxi - TAXI

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section TAXI, first property line 7536.

**Data source:** expandmd01.mix/rulesmd.ini, section TAXI, first property line 10094.

<a id="ptruck"></a>

## Pickup Truck - PTRUCK

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 0 | 0 |
| Starting health capacity | 100 | 100 |
| Armor class | light | light |
| Movement rating | 8 | 8 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Normal | Normal |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | no | no |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section PTRUCK, first property line 7583.

**Data source:** expandmd01.mix/rulesmd.ini, section PTRUCK, first property line 10293.

<a id="cruise"></a>

## Cruise Ship - CRUISE

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 0 |
| Starting health capacity | 300 | 300 |
| Armor class | light | light |
| Movement rating | 4 | 4 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | yes | yes |
| Naval role | yes | yes |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section CRUISE, first property line 7630.

**Data source:** expandmd01.mix/rulesmd.ini, section CRUISE, first property line 10342.

<a id="tug"></a>

## Tug Boat - TUG

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 500 | 0 |
| Starting health capacity | 200 | 200 |
| Armor class | light | light |
| Movement rating | 4 | 4 |
| Sight radius setting | 8 | 8 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP | NAWEAP |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Largest passenger-size setting | 2 | 2 |
| Transport size usage | 6 | 6 |
| Can gain rank | no | no |
| Immune to ordinary psychic control | no | no |
| Radiation immunity | no | no |
| Can crush through ordinary crushing logic | yes | yes |
| Naval role | yes | yes |
| Threat contribution | 0 | 0 |
| Insignificant-object flag | yes | yes |
| Recycling value setting | Not explicitly set | 100 |

**Data source:** ra2.mix/local.mix/rules.ini, section TUG, first property line 7682.

**Data source:** expandmd01.mix/rulesmd.ini, section TUG, first property line 10396.

<a id="cdest"></a>

## Coast Guard Boat - CDEST

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1000 | 1000 |
| Starting health capacity | 600 | 600 |
| Armor class | light | light |
| Movement rating | 6 | 6 |
| Sight radius setting | 7 | 7 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Permitted movement zone | Water | Water |
| Movement speed category | Float | Float |
| Can crush through ordinary crushing logic | yes | yes |
| Detector service | yes | yes |
| Detection range setting | 8 | 8 |
| Spawned attacker type | ASW | ASW |
| Managed attacker count | 1 | 1 |
| Attacker replacement delay | 400 | 400 |
| Attacker reload delay | 150 | 150 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes | yes |
| Naval-target selection mode | 1 | 1 |
| Threat contribution | 15 | 15 |

**Red Alert 2 weapon paths:** Primary: [155mm](reference/WEAPONS.md#ra2-155mm); Secondary: [ASWLauncher](reference/WEAPONS.md#ra2-aswlauncher); Elite Primary: [155mmE](reference/WEAPONS.md#ra2-155mme).

**Data source:** ra2.mix/local.mix/rules.ini, section CDEST, first property line 7733.

**Yuri's Revenge weapon paths:** Primary: [155mm](reference/WEAPONS.md#yr-155mm); Secondary: [ASWLauncher](reference/WEAPONS.md#yr-aswlauncher); Elite Primary: [155mmE](reference/WEAPONS.md#yr-155mme).

**Data source:** expandmd01.mix/rulesmd.ini, section CDEST, first property line 10449.

<a id="apache"></a>

## APACHE - APACHE

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |

**Data source:** ra2.mix/local.mix/rules.ini, section APACHE, first property line 0.

**Data source:** expandmd01.mix/rulesmd.ini, section APACHE, first property line 0.

<a id="orca"></a>

## Harrier - ORCA

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Launch from a usable airfield slot with ammunition.
2. Fly to the target, perform its allowed attack and expend ammunition.
3. Return to a compatible pad to reload and repeat as ordered.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1200 | 1200 |
| Starting health capacity | 150 | 150 |
| Armor class | light | light |
| Movement rating | 14 | 14 |
| Sight radius setting | 8 | 8 |
| Technology level | 3 | 3 |
| Permitted country list | British,French,Germans,Americans | British,French,Germans,Americans |
| Excluded countries | Alliance | Alliance |
| Required structures/groups | RADAR | RADAR |
| Permitted movement zone | Fly | Fly |
| Immune to ordinary psychic control | yes | yes |
| Hidden from radar | no | no |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | STRONGER,FIREPOWER,ROF | STRONGER,FIREPOWER,ROF |
| Threat contribution | 20 | 20 |
| Compatible aircraft docks | GAAIRC,AMRADR | GAAIRC,AMRADR |

**Red Alert 2 weapon paths:** Primary: [Maverick](reference/WEAPONS.md#ra2-maverick); Elite Primary: [MaverickE](reference/WEAPONS.md#ra2-mavericke).

**Data source:** ra2.mix/local.mix/rules.ini, section ORCA, first property line 7786.

**Yuri's Revenge weapon paths:** Primary: [Maverick](reference/WEAPONS.md#yr-maverick); Elite Primary: [MaverickE](reference/WEAPONS.md#yr-mavericke).

**Data source:** expandmd01.mix/rulesmd.ini, section ORCA, first property line 10583.

<a id="hornet"></a>

## Hornet - HORNET

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Be managed by a carrier rather than bought as an ordinary standalone queue item.
2. Fly to the carrier's selected target and attack.
3. Return or be replaced through the carrier's spawn manager.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 50 | 50 |
| Starting health capacity | 75 | 75 |
| Armor class | light | light |
| Movement rating | 12 | 12 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Permitted movement zone | Fly | Fly |
| Immune to ordinary psychic control | yes | yes |
| Hidden from radar | no | no |
| Managed spawned object | yes | yes |
| Veteran improvements | STRONGER,FIREPOWER | STRONGER,FIREPOWER |
| Elite improvements | STRONGER,FIREPOWER | STRONGER,FIREPOWER |
| Threat contribution | 10 | 10 |

**Red Alert 2 weapon paths:** Primary: [HornetBomb](reference/WEAPONS.md#ra2-hornetbomb); Secondary: [HornetCollision](reference/WEAPONS.md#ra2-hornetcollision); Elite Primary: [HornetBombE](reference/WEAPONS.md#ra2-hornetbombe).

**Data source:** ra2.mix/local.mix/rules.ini, section HORNET, first property line 8044.

**Yuri's Revenge weapon paths:** Primary: [HornetBomb](reference/WEAPONS.md#yr-hornetbomb); Secondary: [HornetCollision](reference/WEAPONS.md#yr-hornetcollision); Elite Primary: [HornetBombE](reference/WEAPONS.md#yr-hornetbombe).

**Data source:** expandmd01.mix/rulesmd.ini, section HORNET, first property line 10695.

<a id="v3rocket"></a>

## V3 Rocket - V3ROCKET

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Be spawned by the V3 launch procedure.
2. Follow its missile movement toward the designated impact.
3. Apply its impact/death weapon rather than recruiting it as a reusable tank.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 50 | 50 |
| Starting health capacity | 50 | 50 |
| Armor class | special_2 | special_2 |
| Movement rating | 15 | 15 |
| Sight radius setting | 1 | 1 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Permitted movement zone | Fly | Fly |
| Can gain rank | no | no |
| Immune to ordinary psychic control | yes | yes |
| Hidden from radar | no | no |
| Managed spawned object | yes | yes |
| Threat contribution | 10 | 10 |
| Explosive destruction flag | no | no |

**Data source:** ra2.mix/local.mix/rules.ini, section V3ROCKET, first property line 8181.

**Data source:** expandmd01.mix/rulesmd.ini, section V3ROCKET, first property line 11365.

<a id="asw"></a>

## Osprey - ASW

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Be supplied/managed by the Destroyer's spawn mechanism.
2. Approach a supported submarine target and attack.
3. Return/reload or be replaced through that mechanism.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 50 | 50 |
| Starting health capacity | 30 | 30 |
| Armor class | light | light |
| Movement rating | 12 | 12 |
| Sight radius setting | 2 | 2 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Permitted movement zone | Fly | Fly |
| Immune to ordinary psychic control | yes | yes |
| Hidden from radar | no | no |
| Managed spawned object | yes | yes |
| Ground-target selection mode | 1 | 1 |
| Naval-target selection mode | 2 | 2 |
| Threat contribution | 10 | 10 |

**Red Alert 2 weapon paths:** Primary: [ASWBomb](reference/WEAPONS.md#ra2-aswbomb); Secondary: [ASWCollision](reference/WEAPONS.md#ra2-aswcollision).

**Data source:** ra2.mix/local.mix/rules.ini, section ASW, first property line 8133.

**Yuri's Revenge weapon paths:** Primary: [ASWBomb](reference/WEAPONS.md#yr-aswbomb); Secondary: [ASWCollision](reference/WEAPONS.md#yr-aswcollision).

**Data source:** expandmd01.mix/rulesmd.ini, section ASW, first property line 10647.

<a id="dmisl"></a>

## Missile - DMISL

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Be supplied through the Dreadnought missile mechanism.
2. Travel toward its assigned target.
3. Resolve its weapon/impact and be consumed by that attack.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 50 | 50 |
| Starting health capacity | 50 | 50 |
| Armor class | special_2 | special_2 |
| Movement rating | 20 | 18 |
| Sight radius setting | 0 | 0 |
| Technology level | -1 | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs | Russians,Confederation,Africans,Arabs |
| Permitted movement zone | Fly | Fly |
| Can gain rank | no | no |
| Immune to ordinary psychic control | yes | yes |
| Hidden from radar | no | no |
| Managed spawned object | yes | yes |
| Threat contribution | 10 | 10 |
| Explosive destruction flag | no | no |

**Data source:** ra2.mix/local.mix/rules.ini, section DMISL, first property line 8094.

**Data source:** expandmd01.mix/rulesmd.ini, section DMISL, first property line 11405.

<a id="pdplane"></a>

## Cargo Plane - PDPLANE

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Enter as a scripted/special-weapon delivery aircraft.
2. Carry the configured payload to the drop area.
3. Release its parachuting cargo and complete the delivery path.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Starting health capacity | 400 | 400 |
| Armor class | light | light |
| Movement rating | 15 | 15 |
| Sight radius setting | 0 | 0 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Fly | Fly |
| Immune to ordinary psychic control | yes | yes |
| Hidden from radar | no | no |
| Managed spawned object | yes | yes |
| Threat contribution | 0 | 0 |

**Red Alert 2 weapon paths:** Primary: [ParaDropWeapon](reference/WEAPONS.md#ra2-paradropweapon).

**Data source:** ra2.mix/local.mix/rules.ini, section PDPLANE, first property line 8257.

**Yuri's Revenge weapon paths:** Primary: [ParaDropWeapon](reference/WEAPONS.md#yr-paradropweapon).

**Data source:** expandmd01.mix/rulesmd.ini, section PDPLANE, first property line 11537.

<a id="beag"></a>

## Black Eagle - BEAG

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use the Korean aircraft's own weapon and availability.
2. Launch, approach and attack a supported target.
3. Return to a usable aircraft pad for rearming.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Price in credits | 1200 | 1200 |
| Starting health capacity | 200 | 200 |
| Armor class | light | light |
| Movement rating | 14 | 14 |
| Sight radius setting | 8 | 8 |
| Technology level | 3 | 3 |
| Permitted country list | British,French,Germans,Americans,Alliance | British,French,Germans,Americans,Alliance |
| Required countries | Alliance | Alliance |
| Required structures/groups | RADAR | RADAR |
| Permitted movement zone | Fly | Fly |
| Immune to ordinary psychic control | yes | yes |
| Hidden from radar | no | no |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | STRONGER,FIREPOWER,ROF | STRONGER,FIREPOWER,ROF |
| Threat contribution | 20 | 20 |
| Compatible aircraft docks | GAAIRC,AMRADR | GAAIRC,AMRADR |

**Red Alert 2 weapon paths:** Primary: [Maverick2](reference/WEAPONS.md#ra2-maverick2); Elite Primary: [Maverick2E](reference/WEAPONS.md#ra2-maverick2e).

**Data source:** ra2.mix/local.mix/rules.ini, section BEAG, first property line 8329.

**Yuri's Revenge weapon paths:** Primary: [Maverick2](reference/WEAPONS.md#yr-maverick2); Elite Primary: [Maverick2E](reference/WEAPONS.md#yr-maverick2e).

**Data source:** expandmd01.mix/rulesmd.ini, section BEAG, first property line 10748.

<a id="cargoplane"></a>

## Cargo Plane - CARGOPLANE

**Registered in:** Red Alert 2, Yuri's Revenge.

1. Use this separate transport-aircraft record when a script/ability supplies it.
2. Move to its delivery destination with the prescribed cargo.
3. Complete unloading/drop and departure through that mission/ability.

| Setting | Red Alert 2 | Yuri's Revenge |
| --- | --- | --- |
| Starting health capacity | 400 | 400 |
| Armor class | light | light |
| Movement rating | 15 | 15 |
| Sight radius setting | 0 | 0 |
| Technology level | -1 | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Fly | Fly |
| Immune to ordinary psychic control | yes | yes |
| Hidden from radar | no | no |
| Threat contribution | 0 | 0 |

**Data source:** ra2.mix/local.mix/rules.ini, section CARGOPLANE, first property line 8293.

**Data source:** expandmd01.mix/rulesmd.ini, section CARGOPLANE, first property line 11573.

<a id="yengineer"></a>

## Engineer - YENGINEER

**Registered in:** Yuri's Revenge.

1. Use the Yuri Engineer type and its production restrictions.
2. Reach a legal building or repair-hut entry.
3. Apply the supported capture or repair operation.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 500 |
| Starting health capacity | 75 |
| Armor class | none |
| Movement rating | 4 |
| Sight radius setting | 4 |
| Technology level | 1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Excluded countries | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs |
| Required structures/groups | Barracks |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Passenger IFV mode | 1 |
| Threat contribution | 0 |
| Recycling value setting | 250 |

**Yuri's Revenge weapon paths:** Primary: [DefuseKit](reference/WEAPONS.md#yr-defusekit); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section YENGINEER, first property line 5059.

<a id="ggi"></a>

## Guardian GI - GGI

**Registered in:** Yuri's Revenge.

1. Fight with the standing weapon while mobile.
2. Deploy to switch into the guarded anti-vehicle/anti-air role.
3. Undeploy to move; the deployed and mobile states have different combat restrictions.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 400 |
| Starting health capacity | 100 |
| Armor class | none |
| Movement rating | 3 |
| Sight radius setting | 6 |
| Technology level | 2 |
| Permitted country list | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAPILE |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Immune to ordinary psychic control | no |
| Can be crushed | yes |
| Fires on deployment | yes |
| Crushable while deployed | no |
| Passenger IFV mode | 16 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 10 |
| Recycling value setting | 150 |
| Can garrison buildings | no |
| Attached bombs permitted | yes |

**Yuri's Revenge weapon paths:** Primary: [M60](reference/WEAPONS.md#yr-m60); Secondary: [MissileLauncher](reference/WEAPONS.md#yr-missilelauncher); Elite Primary: [M60E](reference/WEAPONS.md#yr-m60e); Elite Secondary: [MissileLauncherE](reference/WEAPONS.md#yr-missilelaunchere).

**Data source:** expandmd01.mix/rulesmd.ini, section GGI, first property line 3864.

<a id="init"></a>

## Initiate - INIT

**Registered in:** Yuri's Revenge.

1. Use its psychic attack as ordinary damage against supported targets.
2. Enter permitted civilian buildings to contribute garrison fire.
3. Do not confuse the Initiate's visual psychic attack with ownership-changing mind control.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 200 |
| Starting health capacity | 100 |
| Armor class | none |
| Movement rating | 4 |
| Sight radius setting | 9 |
| Technology level | 1 |
| Permitted country list | YuriCountry |
| Required structures/groups | YABRCK |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Passenger IFV mode | 13 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 5 |
| Recycling value setting | 100 |
| Can garrison buildings | yes |

**Yuri's Revenge weapon paths:** Primary: [PsychicJab](reference/WEAPONS.md#yr-psychicjab); Occupy Weapon: [UCPsychicJab](reference/WEAPONS.md#yr-ucpsychicjab); Elite Occupy Weapon: [UCElitePsychicJab](reference/WEAPONS.md#yr-ucelitepsychicjab); Elite Primary: [PsychicJabE](reference/WEAPONS.md#yr-psychicjabe).

**Data source:** expandmd01.mix/rulesmd.ini, section INIT, first property line 4871.

<a id="boris"></a>

## Boris - BORIS

**Registered in:** Yuri's Revenge.

1. Fire his personal weapon at supported combat targets.
2. Designate a supported structure for a MiG airstrike.
3. Let the aircraft arrival/attack procedure resolve while preserving Boris if the mission requires him.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1500 |
| Starting health capacity | 200 |
| Armor class | flak |
| Movement rating | 5 |
| Sight radius setting | 9 |
| Technology level | 9 |
| Permitted country list | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAHAND,NATECH |
| Build limit | 1 |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Self-healing | yes |
| Immune to ordinary psychic control | yes |
| Can be crushed | no |
| Passenger IFV mode | 4 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,SCATTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval-target selection mode | 4 |
| Threat contribution | 25 |
| Recycling value setting | 750 |
| Psychic-weapon immunity | no |

**Yuri's Revenge weapon paths:** Primary: [AKM](reference/WEAPONS.md#yr-akm); Secondary: [Flare](reference/WEAPONS.md#yr-flare); Elite Primary: [AKME](reference/WEAPONS.md#yr-akme).

**Data source:** expandmd01.mix/rulesmd.ini, section BORIS, first property line 4594.

<a id="brute"></a>

## Brute - BRUTE

**Registered in:** Yuri's Revenge.

1. Close on an eligible ground target.
2. Apply its close anti-vehicle/infantry combat according to its weapons.
3. Use its immunity and crushing restrictions; appearance alone does not define target eligibility.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 500 |
| Starting health capacity | 200 |
| Armor class | plate |
| Movement rating | 6 |
| Sight radius setting | 8 |
| Technology level | 5 |
| Permitted country list | YuriCountry |
| Required structures/groups | YABRCK |
| Permitted movement zone | InfantryDestroyer |
| Transport size usage | 2 |
| Self-healing | yes |
| Immune to ordinary psychic control | yes |
| Can be crushed | no |
| Passenger IFV mode | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 20 |
| Recycling value setting | 250 |

**Yuri's Revenge weapon paths:** Primary: [Punch](reference/WEAPONS.md#yr-punch); Secondary: [Smash](reference/WEAPONS.md#yr-smash); Elite Primary: [PunchE](reference/WEAPONS.md#yr-punche); Elite Secondary: [SmashE](reference/WEAPONS.md#yr-smashe).

**Data source:** expandmd01.mix/rulesmd.ini, section BRUTE, first property line 5105.

<a id="virus"></a>

## Virus - VIRUS

**Registered in:** Yuri's Revenge.

1. Aim at eligible infantry at long range.
2. Apply the configured toxic kill/effect.
3. The resulting poison cloud can affect other nearby susceptible infantry over time.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 700 |
| Starting health capacity | 100 |
| Armor class | none |
| Movement rating | 4 |
| Sight radius setting | 9 |
| Technology level | 1 |
| Permitted country list | YuriCountry |
| Required structures/groups | YABRCK,RADAR |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Immune to ordinary psychic control | no |
| Passenger IFV mode | 14 |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 10 |
| Recycling value setting | 350 |
| Poison immunity | yes |
| Attached bombs permitted | yes |

**Yuri's Revenge weapon paths:** Primary: [Virusgun](reference/WEAPONS.md#yr-virusgun); Elite Primary: [VirusgunE](reference/WEAPONS.md#yr-virusgune).

**Data source:** expandmd01.mix/rulesmd.ini, section VIRUS, first property line 5156.

<a id="clnt"></a>

## Cowboy - CLNT

**Registered in:** Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 10 |
| Starting health capacity | 200 |
| Armor class | plate |
| Movement rating | 6 |
| Sight radius setting | 2 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Passenger IFV mode | 4 |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 200 |

**Yuri's Revenge weapon paths:** Primary: [CLINTGUN](reference/WEAPONS.md#yr-clintgun).

**Data source:** expandmd01.mix/rulesmd.ini, section CLNT, first property line 6093.

<a id="arnd"></a>

## Hero - ARND

**Registered in:** Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 10 |
| Starting health capacity | 200 |
| Armor class | plate |
| Movement rating | 6 |
| Sight radius setting | 2 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Passenger IFV mode | 4 |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Yuri's Revenge weapon paths:** Primary: [TERMIGUN](reference/WEAPONS.md#yr-termigun).

**Data source:** expandmd01.mix/rulesmd.ini, section ARND, first property line 6134.

<a id="stln"></a>

## Bodybuilder - STLN

**Registered in:** Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 10 |
| Starting health capacity | 200 |
| Armor class | plate |
| Movement rating | 6 |
| Sight radius setting | 2 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Passenger IFV mode | 4 |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 200 |

**Yuri's Revenge weapon paths:** Primary: [STALGUN](reference/WEAPONS.md#yr-stalgun); Secondary: [STALGREN](reference/WEAPONS.md#yr-stalgren).

**Data source:** expandmd01.mix/rulesmd.ini, section STLN, first property line 6175.

<a id="caml"></a>

## Camel - CAML

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 10 |
| Starting health capacity | 200 |
| Armor class | none |
| Movement rating | 6 |
| Sight radius setting | 2 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 2 |
| Can gain rank | no |
| Can be crushed | no |
| Passenger IFV mode | 12 |
| Threat contribution | 2 |
| Insignificant-object flag | no |
| Recycling value setting | 200 |

**Data source:** expandmd01.mix/rulesmd.ini, section CAML, first property line 5466.

<a id="eins"></a>

## Einstein - EINS

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 10 |
| Starting health capacity | 50 |
| Armor class | none |
| Movement rating | 4 |
| Sight radius setting | 2 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 200 |

**Data source:** expandmd01.mix/rulesmd.ini, section EINS, first property line 6217.

<a id="mumy"></a>

## Mummy - MUMY

**Registered in:** Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 100 |
| Starting health capacity | 400 |
| Armor class | plate |
| Movement rating | 3 |
| Sight radius setting | 6 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Self-healing | yes |
| Immune to ordinary psychic control | yes |
| Threat contribution | 0 |
| Recycling value setting | 200 |

**Yuri's Revenge weapon paths:** Primary: [Mummypunch](reference/WEAPONS.md#yr-mummypunch); Secondary: [Mummysmash](reference/WEAPONS.md#yr-mummysmash).

**Data source:** expandmd01.mix/rulesmd.ini, section MUMY, first property line 6253.

<a id="rmnv"></a>

## Premier Romanov - RMNV

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 10 |
| Starting health capacity | 50 |
| Armor class | none |
| Movement rating | 4 |
| Sight radius setting | 2 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Data source:** expandmd01.mix/rulesmd.ini, section RMNV, first property line 6331.

<a id="lunr"></a>

## Cosmonaut - LUNR

**Registered in:** Yuri's Revenge.

1. Use the lunar infantry record and its flight/movement properties.
2. Engage supported targets with its laser weapon.
3. Its campaign availability and lunar rules are distinct from an ordinary Rocketeer.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 600 |
| Starting health capacity | 125 |
| Armor class | none |
| Movement rating | 9 |
| Sight radius setting | 8 |
| Technology level | 11 |
| Permitted country list | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAPILE,RADAR |
| Permitted movement zone | Fly |
| Movement speed category | Hover |
| Transport size usage | 1 |
| Can be crushed | yes |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 15 |
| Recycling value setting | 250 |

**Yuri's Revenge weapon paths:** Primary: [Lunarlaser](reference/WEAPONS.md#yr-lunarlaser); Elite Primary: [Lunarlaser](reference/WEAPONS.md#yr-lunarlaser).

**Data source:** expandmd01.mix/rulesmd.ini, section LUNR, first property line 4711.

<a id="dnoa"></a>

## T-Rex - DNOA

**Registered in:** Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 2700 |
| Starting health capacity | 300 |
| Armor class | Plate |
| Movement rating | 8 |
| Sight radius setting | 5 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 30 |
| Can gain rank | no |
| Self-healing | yes |
| Immune to ordinary psychic control | yes |
| Can be crushed | no |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | STRONGER,FIREPOWER,ROF |
| Threat contribution | 25 |
| Explosive destruction flag | no |
| Attached bombs permitted | yes |

**Yuri's Revenge weapon paths:** Primary: [TRexInfBite](reference/WEAPONS.md#yr-trexinfbite); Secondary: [TRexBite](reference/WEAPONS.md#yr-trexbite).

**Data source:** expandmd01.mix/rulesmd.ini, section DNOA, first property line 5505.

<a id="dnob"></a>

## Brachiosaurus - DNOB

**Registered in:** Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1000 |
| Starting health capacity | 200 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 5 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Water |
| Movement speed category | Float |
| Transport size usage | 30 |
| Can gain rank | no |
| Self-healing | yes |
| Immune to ordinary psychic control | yes |
| Can be crushed | no |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | STRONGER,FIREPOWER,ROF |
| Threat contribution | 25 |
| Explosive destruction flag | no |
| Recycling value setting | 200 |
| Attached bombs permitted | yes |

**Yuri's Revenge weapon paths:** Primary: [ChimpBite](reference/WEAPONS.md#yr-chimpbite); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section DNOB, first property line 5559.

<a id="slav"></a>

## Slave - SLAV

**Registered in:** Yuri's Revenge.

1. Belong to a Slave Miner's worker-management relationship while assigned.
2. Travel to ore, collect and return it to the deployed miner.
3. Handle death/replacement or release through that manager and the scenario, rather than treating the worker as a second refinery.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 10 |
| Starting health capacity | 125 |
| Armor class | none |
| Movement rating | 3 |
| Sight radius setting | 5 |
| Technology level | -1 |
| Permitted country list | YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Resource cargo capacity | 4 |
| Immune to ordinary psychic control | yes |
| Passenger IFV mode | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 2 |
| Recycling value setting | 0 |

**Yuri's Revenge weapon paths:** Primary: [SHOVEL](reference/WEAPONS.md#yr-shovel); Elite Primary: [SHOVEL](reference/WEAPONS.md#yr-shovel).

**Data source:** expandmd01.mix/rulesmd.ini, section SLAV, first property line 5016.

<a id="wwlf"></a>

## Mummy - WWLF

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 10 |
| Starting health capacity | 50 |
| Armor class | none |
| Movement rating | 4 |
| Sight radius setting | 2 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 200 |

**Data source:** expandmd01.mix/rulesmd.ini, section WWLF, first property line 6294.

<a id="ydog"></a>

## Attack Dog - YDOG

**Registered in:** Yuri's Revenge.

1. Use this registered dog variant only where placed or made available.
2. Follow its own weapon and movement record.
3. Do not infer normal buildability from the dog name.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 200 |
| Starting health capacity | 100 |
| Armor class | none |
| Movement rating | 8 |
| Sight radius setting | 9 |
| Technology level | 2 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Required countries | YuriCountry |
| Required structures/groups | NAHAND |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Immune to ordinary psychic control | yes |
| Radiation immunity | no |
| Passenger IFV mode | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER,SCATTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval-target selection mode | 6 |
| Threat contribution | 20 |
| Recycling value setting | 50 |
| Attached bombs permitted | yes |

**Yuri's Revenge weapon paths:** Primary: [BadTeeth](reference/WEAPONS.md#yr-badteeth); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section YDOG, first property line 4965.

<a id="yadog"></a>

## Attack Dog - YADOG

**Registered in:** Yuri's Revenge.

1. Use this separate registered dog variant only where supplied.
2. Follow its own attack and movement record.
3. Compare its actual availability with the ordinary Allied dog.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 200 |
| Starting health capacity | 100 |
| Armor class | none |
| Movement rating | 8 |
| Sight radius setting | 9 |
| Technology level | 2 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry,British,French,Germans,Americans,Alliance |
| Required countries | YuriCountry |
| Required structures/groups | GAPILE |
| Permitted movement zone | Infantry |
| Transport size usage | 1 |
| Can gain rank | no |
| Immune to ordinary psychic control | yes |
| Radiation immunity | no |
| Passenger IFV mode | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER,SCATTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval-target selection mode | 6 |
| Threat contribution | 20 |
| Recycling value setting | 50 |
| Attached bombs permitted | yes |

**Yuri's Revenge weapon paths:** Primary: [GoodTeeth](reference/WEAPONS.md#yr-goodteeth); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section YADOG, first property line 4914.

<a id="yhvr"></a>

## Amphibious Transport - YHVR

**Registered in:** Yuri's Revenge.

1. Load infantry or vehicles permitted by passenger-size/capacity rules.
2. Travel over legal land/water to a usable unloading shore or location.
3. Unload into available cells; do not assume a full transport can unload onto blocked terrain.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 900 |
| Starting health capacity | 300 |
| Armor class | heavy |
| Movement rating | 6 |
| Sight radius setting | 6 |
| Technology level | 2 |
| Permitted country list | YuriCountry |
| Required structures/groups | YAYARD |
| Permitted movement zone | Amphibious |
| Movement speed category | Hover |
| Passenger slot capacity | 12 |
| Largest passenger-size setting | 6 |
| Transport size usage | 15 |
| Can gain rank | no |
| Can crush through ordinary crushing logic | yes |
| Naval role | yes |
| Threat contribution | 10 |
| Recycling value setting | 900 |
| Can enter tank bunkers | no |

**Data source:** expandmd01.mix/rulesmd.ini, section YHVR, first property line 8871.

<a id="pcv"></a>

## Yuri MCV - PCV

**Registered in:** Yuri's Revenge.

1. Move to a legal deployment position.
2. Become Yuri's Construction Yard.
3. Use its distinct faction prerequisites and production list.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 3000 |
| Starting health capacity | 1000 |
| Armor class | heavy |
| Movement rating | 4 |
| Sight radius setting | 8 |
| Technology level | 10 |
| Permitted country list | YuriCountry |
| Required structures/groups | YAWEAP,YAGRND |
| Permitted movement zone | Normal |
| Transport size usage | 6 |
| Can gain rank | no |
| Can crush through ordinary crushing logic | yes |
| Deploys into | YACNST |
| Threat contribution | 0 |
| Recycling value setting | 3000 |
| Can enter tank bunkers | no |

**Data source:** expandmd01.mix/rulesmd.ini, section PCV, first property line 8827.

<a id="smin"></a>

## Slave Miner - SMIN

**Registered in:** Yuri's Revenge.

1. Move next to an accessible deposit and deploy into the linked refinery form.
2. Supply and manage slave workers gathering into that deployed miner.
3. Undeploy to relocate; worker replacement has a configured delay.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1750 |
| Starting health capacity | 2000 |
| Armor class | medium |
| Movement rating | 3 |
| Sight radius setting | 4 |
| Technology level | 1 |
| Permitted country list | YuriCountry |
| Required structures/groups | YAWEAP |
| Permitted movement zone | Crusher |
| Transport size usage | 3 |
| Resource cargo capacity | 20 |
| Selling forbidden | yes |
| Can gain rank | yes |
| Self-healing | yes |
| Immune to ordinary psychic control | yes |
| Radiation immunity | yes |
| Can crush through ordinary crushing logic | yes |
| Deploys into | YAREFN |
| Resource-gathering role | yes |
| Resource-delivery destination | yes |
| Managed worker type | SLAV |
| Worker count | 5 |
| Worker replacement delay | 500 |
| Worker delivery delay | 25 |
| Threat contribution | 0 |
| Production-time multiplier | 0.8 |
| Recycling value setting | 1750 |
| Can enter tank bunkers | no |

**Yuri's Revenge weapon paths:** Primary: [20mmRapid](reference/WEAPONS.md#yr-20mmrapid); Elite Primary: [20mmRapidE](reference/WEAPONS.md#yr-20mmrapide).

**Data source:** expandmd01.mix/rulesmd.ini, section SMIN, first property line 9043.

<a id="smon"></a>

## Chrono Miner(noback) - SMON

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1400 |
| Starting health capacity | 1000 |
| Armor class | medium |
| Movement rating | 4 |
| Sight radius setting | 4 |
| Technology level | -1 |
| Permitted country list | YuriCountry |
| Permitted movement zone | Crusher |
| Selling forbidden | yes |
| Can gain rank | no |
| Self-healing | yes |
| Radiation immunity | yes |
| Can crush through ordinary crushing logic | yes |
| Conventional harvester behavior | yes |
| Threat contribution | 0 |
| Compatible aircraft docks | NAREFN,GAREFN |

**Data source:** expandmd01.mix/rulesmd.ini, section SMON, first property line 8996.

<a id="ycab"></a>

## Yellow Cab - YCAB

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 0 |
| Starting health capacity | 100 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Normal |
| Largest passenger-size setting | 2 |
| Transport size usage | 4 |
| Can gain rank | no |
| Immune to ordinary psychic control | no |
| Radiation immunity | no |
| Can crush through ordinary crushing logic | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Data source:** expandmd01.mix/rulesmd.ini, section YCAB, first property line 10143.

<a id="ytnk"></a>

## Gattling Tank - YTNK

**Registered in:** Yuri's Revenge.

1. Begin firing the appropriate ground/air weapon.
2. Accumulate firing-stage progress and select the corresponding Gattling stage weapons.
3. Lose stage progress when the rules call for cooldown; a short engagement does not start at peak sustained output.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 600 |
| Starting health capacity | 210 |
| Armor class | light |
| Movement rating | 6 |
| Sight radius setting | 10 |
| Technology level | 4 |
| Permitted country list | YuriCountry |
| Required structures/groups | YAWEAP |
| Permitted movement zone | Destroyer |
| Transport size usage | 3 |
| Can crush through ordinary crushing logic | no |
| Gattling stage behavior | yes |
| Firing-stage count | 3 |
| First stage threshold | 200 |
| Second stage threshold | 400 |
| Third stage threshold | 600 |
| Stage accumulation setting | 1 |
| Stage cooldown setting | 50 |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 40 |
| Recycling value setting | 600 |

**Yuri's Revenge weapon paths:** Primary: [AGGattling](reference/WEAPONS.md#yr-aggattling); Secondary: [AAGattling](reference/WEAPONS.md#yr-aagattling); Weapon1: [AGGattling](reference/WEAPONS.md#yr-aggattling); Elite Weapon1: [AGGattlingE](reference/WEAPONS.md#yr-aggattlinge); Weapon2: [AAGattling](reference/WEAPONS.md#yr-aagattling); Elite Weapon2: [AAGattlingE](reference/WEAPONS.md#yr-aagattlinge); Weapon3: [AGGattling2](reference/WEAPONS.md#yr-aggattling2); Elite Weapon3: [AGGattling2E](reference/WEAPONS.md#yr-aggattling2e); Weapon4: [AAGattling2](reference/WEAPONS.md#yr-aagattling2); Elite Weapon4: [AAGattling2E](reference/WEAPONS.md#yr-aagattling2e); Weapon5: [AGGattling3](reference/WEAPONS.md#yr-aggattling3); Elite Weapon5: [AGGattling3E](reference/WEAPONS.md#yr-aggattling3e); Weapon6: [AAGattling3](reference/WEAPONS.md#yr-aagattling3); Elite Weapon6: [AAGattling3E](reference/WEAPONS.md#yr-aagattling3e); Elite Primary: [AGGattlingE](reference/WEAPONS.md#yr-aggattlinge); Elite Secondary: [AAGattlingE](reference/WEAPONS.md#yr-aagattlinge).

**Data source:** expandmd01.mix/rulesmd.ini, section YTNK, first property line 8485.

<a id="bfrt"></a>

## Battle Fortress - BFRT

**Registered in:** Yuri's Revenge.

1. Load eligible infantry into its passenger slots.
2. Move the heavy transport while allowing supported passenger fire through its open-topped rules.
3. Apply its special crushing permissions when moving over eligible victims/obstacles.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 2000 |
| Starting health capacity | 600 |
| Armor class | heavy |
| Movement rating | 4 |
| Sight radius setting | 6 |
| Technology level | 10 |
| Permitted country list | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP,GATECH |
| Permitted movement zone | CrusherAll |
| Passenger slot capacity | 5 |
| Largest passenger-size setting | 2 |
| Transport size usage | 6 |
| Can crush through ordinary crushing logic | yes |
| Special all-crushing behavior | yes |
| Passengers can use open-topped fire | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 40 |
| Recycling value setting | 2000 |

**Yuri's Revenge weapon paths:** Primary: [20mmRapid](reference/WEAPONS.md#yr-20mmrapid).

**Data source:** expandmd01.mix/rulesmd.ini, section BFRT, first property line 6918.

<a id="tele"></a>

## Magnetron - TELE

**Registered in:** Yuri's Revenge.

1. Choose the magnetic interaction appropriate to a vehicle or structure.
2. Lift/pull an eligible vehicle, or apply the supported structure attack.
3. Release/place the victim through the special logic; ordinary infantry is not a valid substitute target for its lift.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1000 |
| Starting health capacity | 150 |
| Armor class | light |
| Movement rating | 5 |
| Sight radius setting | 10 |
| Technology level | 2 |
| Permitted country list | YuriCountry |
| Required structures/groups | YAWEAP,NAPSIS |
| Permitted movement zone | Destroyer |
| Transport size usage | 6 |
| Can crush through ordinary crushing logic | no |
| Veteran improvements | STRONGER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,ROF |
| Threat contribution | 40 |
| Recycling value setting | 1000 |
| Can enter tank bunkers | no |

**Yuri's Revenge weapon paths:** Primary: [MagneticBeam](reference/WEAPONS.md#yr-magneticbeam); Secondary: [MagneShake](reference/WEAPONS.md#yr-magneshake); Elite Primary: [MagneticBeamE](reference/WEAPONS.md#yr-magneticbeame).

**Data source:** expandmd01.mix/rulesmd.ini, section TELE, first property line 8587.

<a id="caos"></a>

## Chaos Drone - CAOS

**Registered in:** Yuri's Revenge.

1. Move into a useful close-area position.
2. Release its configured chaos effect.
3. Affected eligible units enter berserk behavior temporarily instead of becoming conventionally owned units.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1000 |
| Starting health capacity | 130 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 6 |
| Technology level | 4 |
| Permitted country list | YuriCountry |
| Required structures/groups | YAWEAP |
| Permitted movement zone | Destroyer |
| Transport size usage | 2 |
| Can gain rank | no |
| Immune to ordinary psychic control | yes |
| Radiation immunity | yes |
| Can crush through ordinary crushing logic | no |
| Fires on deployment | yes |
| Naval-target selection mode | 6 |
| Threat contribution | 25 |
| Explosive destruction flag | no |
| Production-time multiplier | 1.1 |
| Recycling value setting | 1000 |
| Can enter tank bunkers | no |

**Yuri's Revenge weapon paths:** Primary: [ChaosAttack](reference/WEAPONS.md#yr-chaosattack); Secondary: [VirtualScanner](reference/WEAPONS.md#yr-virtualscanner).

**Data source:** expandmd01.mix/rulesmd.ini, section CAOS, first property line 8762.

<a id="ddbx"></a>

## Bus - DDBX

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 0 |
| Starting health capacity | 100 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Normal |
| Passenger slot capacity | 5 |
| Largest passenger-size setting | 2 |
| Transport size usage | 6 |
| Can gain rank | no |
| Immune to ordinary psychic control | no |
| Radiation immunity | no |
| Can crush through ordinary crushing logic | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Data source:** expandmd01.mix/rulesmd.ini, section DDBX, first property line 9456.

<a id="bcab"></a>

## Black Cab - BCAB

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 0 |
| Starting health capacity | 100 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Normal |
| Largest passenger-size setting | 2 |
| Transport size usage | 4 |
| Can gain rank | no |
| Immune to ordinary psychic control | no |
| Radiation immunity | no |
| Can crush through ordinary crushing logic | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Data source:** expandmd01.mix/rulesmd.ini, section BCAB, first property line 10243.

<a id="bsub"></a>

## Boomer - BSUB

**Registered in:** Yuri's Revenge.

1. Move submerged on legal water.
2. Use torpedoes against eligible naval targets or its missile attack against supported land targets.
3. Resolve its independently managed missiles and detection state.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 2000 |
| Starting health capacity | 1200 |
| Armor class | heavy |
| Movement rating | 5 |
| Sight radius setting | 8 |
| Technology level | 2 |
| Permitted country list | YuriCountry |
| Required structures/groups | YAYARD,RADAR |
| Permitted movement zone | Water |
| Movement speed category | Float |
| Transport size usage | 20 |
| Can crush through ordinary crushing logic | no |
| Can cloak | yes |
| Detector service | yes |
| Detection range setting | 8 |
| Spawned attacker type | CMISL |
| Managed attacker count | 2 |
| Attacker replacement delay | 80 |
| Attacker reload delay | 0 |
| Veteran improvements | STRONGER,FIREPOWER,ROF,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Naval role | yes |
| Ground-target selection mode | 2 |
| Naval-target selection mode | 7 |
| Threat contribution | 20 |
| Recycling value setting | 2000 |

**Yuri's Revenge weapon paths:** Primary: [BoomerTorpedo](reference/WEAPONS.md#yr-boomertorpedo); Secondary: [CruiseLauncher](reference/WEAPONS.md#yr-cruiselauncher); Elite Primary: [BoomerTorpedoE](reference/WEAPONS.md#yr-boomertorpedoe).

**Data source:** expandmd01.mix/rulesmd.ini, section BSUB, first property line 8937.

<a id="schp"></a>

## Siege Chopper - SCHP

**Registered in:** Yuri's Revenge.

1. Fly and use its airborne weapon.
2. Deploy/land into its siege state at a legal position.
3. Use the deployed siege weapon until ordered to return to mobile flight.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1100 |
| Starting health capacity | 300 |
| Armor class | light |
| Movement rating | 12 |
| Sight radius setting | 7 |
| Technology level | 7 |
| Permitted country list | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP,TECH |
| Permitted movement zone | Fly |
| Movement speed category | Hover |
| Largest passenger-size setting | 2 |
| Transport size usage | 15 |
| Can gain rank | yes |
| Fires on deployment | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 0 |
| Recycling value setting | 1100 |
| Can enter tank bunkers | no |

**Yuri's Revenge weapon paths:** Primary: [BlackHawkCannon](reference/WEAPONS.md#yr-blackhawkcannon); Secondary: [160mm](reference/WEAPONS.md#yr-160mm); Elite Primary: [BlackHawkCannonE](reference/WEAPONS.md#yr-blackhawkcannone); Elite Secondary: [160mmE](reference/WEAPONS.md#yr-160mme).

**Data source:** expandmd01.mix/rulesmd.ini, section SCHP, first property line 10873.

<a id="jeep"></a>

## Truck - JEEP

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 0 |
| Starting health capacity | 100 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Normal |
| Largest passenger-size setting | 2 |
| Transport size usage | 6 |
| Can gain rank | no |
| Immune to ordinary psychic control | no |
| Radiation immunity | no |
| Can crush through ordinary crushing logic | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Data source:** expandmd01.mix/rulesmd.ini, section JEEP, first property line 10193.

<a id="mind"></a>

## Master Mind - MIND

**Registered in:** Yuri's Revenge.

1. Acquire eligible enemies into multiple control relationships.
2. Track the number under control.
3. Exceeding safe capacity invokes overload/self-damage behavior; it is not unlimited free capacity.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1750 |
| Starting health capacity | 500 |
| Armor class | heavy |
| Movement rating | 4 |
| Sight radius setting | 9 |
| Technology level | 2 |
| Permitted country list | YuriCountry |
| Required structures/groups | YAWEAP,YATECH |
| Permitted movement zone | Destroyer |
| Transport size usage | 6 |
| Can gain rank | no |
| Self-healing | yes |
| Immune to ordinary psychic control | yes |
| Can crush through ordinary crushing logic | no |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 40 |
| Recycling value setting | 1750 |

**Yuri's Revenge weapon paths:** Primary: [MultipleMindControlTank](reference/WEAPONS.md#yr-multiplemindcontroltank).

**Data source:** expandmd01.mix/rulesmd.ini, section MIND, first property line 8640.

<a id="disk"></a>

## Floating Disc - DISK

**Registered in:** Yuri's Revenge.

1. Fly to a combat or drain position.
2. Use its laser against supported targets or attach its drain effect to an eligible structure.
3. Power-drain and refinery-money effects follow the structure-specific drain procedure.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1750 |
| Starting health capacity | 600 |
| Armor class | light |
| Movement rating | 15 |
| Sight radius setting | 9 |
| Technology level | 2 |
| Permitted country list | YuriCountry |
| Required structures/groups | YAWEAP,YATECH |
| Permitted movement zone | Fly |
| Movement speed category | Hover |
| Transport size usage | 6 |
| Self-healing | yes |
| Can crush through ordinary crushing logic | no |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 20 |
| Recycling value setting | 1750 |

**Yuri's Revenge weapon paths:** Primary: [DiskLaser](reference/WEAPONS.md#yr-disklaser); Secondary: [DiskDrain](reference/WEAPONS.md#yr-diskdrain); Elite Primary: [DiskLaserE](reference/WEAPONS.md#yr-disklasere); Death Weapon: [BlimpBombEffect](reference/WEAPONS.md#yr-blimpbombeffect).

**Data source:** expandmd01.mix/rulesmd.ini, section DISK, first property line 8692.

<a id="utnk"></a>

## ZZZ Not Used - UTNK

**Registered in:** Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1000 |
| Starting health capacity | 400 |
| Armor class | heavy |
| Movement rating | 6 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Destroyer |
| Transport size usage | 3 |
| Can crush through ordinary crushing logic | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 40 |

**Yuri's Revenge weapon paths:** Primary: [Comet](reference/WEAPONS.md#yr-comet); Elite Primary: [120mmE](reference/WEAPONS.md#yr-120mme).

**Data source:** expandmd01.mix/rulesmd.ini, section UTNK, first property line 8278.

<a id="robo"></a>

## Robot Tank - ROBO

**Registered in:** Yuri's Revenge.

1. Require the appropriate Robot Control Center and power conditions.
2. Move as a hovering tank across supported land/water and fire at eligible ground targets.
3. Enter the powered-down state when its control conditions fail; mind-control immunity is a separate property.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 600 |
| Starting health capacity | 180 |
| Armor class | heavy |
| Movement rating | 10 |
| Sight radius setting | 6 |
| Technology level | 2 |
| Permitted country list | British,French,Germans,Americans,Alliance |
| Required structures/groups | GAWEAP,GAROBO |
| Permitted movement zone | AmphibiousDestroyer |
| Movement speed category | Hover |
| Transport size usage | 3 |
| Can gain rank | no |
| Immune to ordinary psychic control | yes |
| Radiation immunity | yes |
| Can crush through ordinary crushing logic | yes |
| Requires powered-unit control | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 15 |
| Production-time multiplier | 1.3 |
| Recycling value setting | 600 |

**Yuri's Revenge weapon paths:** Primary: [Robogun](reference/WEAPONS.md#yr-robogun).

**Data source:** expandmd01.mix/rulesmd.ini, section ROBO, first property line 7418.

<a id="ydum"></a>

## YDUM - YDUM

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |

**Data source:** expandmd01.mix/rulesmd.ini, section YDUM, first property line 0.

<a id="schd"></a>

## Siege Chopper - SCHD

**Registered in:** Yuri's Revenge.

1. Receive its initial order from the map, production queue, manager or player.
2. Move through its permitted movement controller and use the listed weapon links for supported attacks.
3. Recheck target/order validity and resolve damage, death or script transitions through the normal object workflow.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 1000 |
| Starting health capacity | 200 |
| Armor class | light |
| Movement rating | 12 |
| Sight radius setting | 7 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Fly |
| Movement speed category | Hover |
| Largest passenger-size setting | 2 |
| Transport size usage | 15 |
| Can gain rank | yes |
| Fires on deployment | yes |
| Veteran improvements | STRONGER,FIREPOWER,SIGHT,FASTER |
| Elite improvements | SELF_HEAL,STRONGER,FIREPOWER,ROF |
| Threat contribution | 0 |
| Can enter tank bunkers | no |

**Yuri's Revenge weapon paths:** Primary: [BlackHawkCannon](reference/WEAPONS.md#yr-blackhawkcannon); Elite Primary: [BlackHawkCannonE](reference/WEAPONS.md#yr-blackhawkcannone).

**Data source:** expandmd01.mix/rulesmd.ini, section SCHD, first property line 11145.

<a id="doly"></a>

## Camera Dolly - DOLY

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 0 |
| Starting health capacity | 100 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Normal |
| Largest passenger-size setting | 2 |
| Transport size usage | 4 |
| Can gain rank | no |
| Immune to ordinary psychic control | no |
| Radiation immunity | no |
| Can crush through ordinary crushing logic | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Data source:** expandmd01.mix/rulesmd.ini, section DOLY, first property line 10948.

<a id="cblc"></a>

## Cable Car - CBLC

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 0 |
| Starting health capacity | 100 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Normal |
| Largest passenger-size setting | 2 |
| Transport size usage | 4 |
| Can gain rank | no |
| Immune to ordinary psychic control | no |
| Radiation immunity | no |
| Can crush through ordinary crushing logic | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Data source:** expandmd01.mix/rulesmd.ini, section CBLC, first property line 10997.

<a id="ftrk"></a>

## Fire Truck - FTRK

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 0 |
| Starting health capacity | 100 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Normal |
| Largest passenger-size setting | 2 |
| Transport size usage | 4 |
| Can gain rank | no |
| Immune to ordinary psychic control | no |
| Radiation immunity | no |
| Can crush through ordinary crushing logic | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Data source:** expandmd01.mix/rulesmd.ini, section FTRK, first property line 11046.

<a id="ambu"></a>

## Ambulance - AMBU

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 0 |
| Starting health capacity | 100 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Normal |
| Largest passenger-size setting | 2 |
| Transport size usage | 4 |
| Can gain rank | no |
| Immune to ordinary psychic control | no |
| Radiation immunity | no |
| Can crush through ordinary crushing logic | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |
| Recycling value setting | 100 |

**Data source:** expandmd01.mix/rulesmd.ini, section AMBU, first property line 11095.

<a id="civp"></a>

## Passenger Plane - CIVP

**Registered in:** Yuri's Revenge.

1. Receive the movement/idle/transport order supplied by its map or manager.
2. Follow legal movement and explicit passenger/service settings on this card.
3. Respond to damage or mission tags as configured; no hidden combat weapon or normal build availability is inferred.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 0 |
| Starting health capacity | 100 |
| Armor class | light |
| Movement rating | 8 |
| Sight radius setting | 8 |
| Technology level | -1 |
| Permitted country list | Russians,Confederation,Africans,Arabs,YuriCountry |
| Required structures/groups | NAWEAP |
| Permitted movement zone | Normal |
| Largest passenger-size setting | 2 |
| Transport size usage | 4 |
| Can gain rank | no |
| Immune to ordinary psychic control | yes |
| Radiation immunity | no |
| Can crush through ordinary crushing logic | no |
| Threat contribution | 0 |
| Insignificant-object flag | yes |

**Data source:** expandmd01.mix/rulesmd.ini, section CIVP, first property line 9408.

<a id="bpln"></a>

## MiG - BPLN

**Registered in:** Yuri's Revenge.

1. Be called through Boris's supported airstrike interaction.
2. Fly in and attack the designated structure.
3. Leave/complete the strike under the airstrike manager rather than becoming an ordinary player airfield unit.

| Setting | Yuri's Revenge |
| --- | --- |
| Starting health capacity | 200 |
| Armor class | light |
| Movement rating | 16 |
| Sight radius setting | 0 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Fly |
| Can gain rank | no |
| Immune to ordinary psychic control | yes |
| Hidden from radar | no |
| Managed spawned object | yes |
| Threat contribution | 0 |

**Yuri's Revenge weapon paths:** Primary: [Maverick3](reference/WEAPONS.md#yr-maverick3); Elite Primary: [Maverick3E](reference/WEAPONS.md#yr-maverick3e); Death Weapon: [BlimpBomb](reference/WEAPONS.md#yr-blimpbomb).

**Data source:** expandmd01.mix/rulesmd.ini, section BPLN, first property line 11277.

<a id="spyp"></a>

## Spy Plane - SPYP

**Registered in:** Yuri's Revenge.

1. Be dispatched by a reconnaissance ability.
2. Fly over the relevant area to reveal terrain.
3. Leave/complete the pass; it is not a normal fighter queue item.

| Setting | Yuri's Revenge |
| --- | --- |
| Starting health capacity | 600 |
| Armor class | light |
| Movement rating | 15 |
| Sight radius setting | 0 |
| Technology level | -1 |
| Permitted country list | British,French,Germans,Americans,Alliance,Russians,Confederation,Africans,Arabs,YuriCountry |
| Permitted movement zone | Fly |
| Immune to ordinary psychic control | yes |
| Hidden from radar | no |
| Managed spawned object | yes |
| Threat contribution | 0 |

**Yuri's Revenge weapon paths:** Primary: [SpyCameraWeapon](reference/WEAPONS.md#yr-spycameraweapon); Death Weapon: [BlimpBomb](reference/WEAPONS.md#yr-blimpbomb).

**Data source:** expandmd01.mix/rulesmd.ini, section SPYP, first property line 11324.

<a id="cmisl"></a>

## Missile - CMISL

**Registered in:** Yuri's Revenge.

1. Be supplied through the expansion's missile-launching mechanism.
2. Travel toward the selected impact target.
3. Resolve its impact and the parent launcher's replacement/reload cycle.

| Setting | Yuri's Revenge |
| --- | --- |
| Price in credits | 50 |
| Starting health capacity | 50 |
| Armor class | special_2 |
| Movement rating | 20 |
| Sight radius setting | 0 |
| Technology level | -1 |
| Permitted country list | YuriCountry |
| Permitted movement zone | Fly |
| Can gain rank | no |
| Immune to ordinary psychic control | yes |
| Hidden from radar | no |
| Managed spawned object | yes |
| Threat contribution | 10 |
| Explosive destruction flag | no |

**Data source:** expandmd01.mix/rulesmd.ini, section CMISL, first property line 11447.

## Campaign-only additions and other placed references

These are not silently added to the skirmish build menu. An explicit mission definition is reported below. A placed name without a local definition remains unresolved rather than being assigned invented statistics.

### DNOAA

- [sov01umd.map](missions/yr/sov01umd.md): explicit mission definition; Transport size usage: 1, Starting health capacity: 3500, Movement rating: 10, Armor class: Plate, Technology level: -1, Self-healing: yes, Sight radius setting: 5, Permitted country list: Russians,Confederation,Africans,Arabs,YuriCountry, Price in credits: 2700, Permitted movement zone: Infantry, Threat contribution: 25, Immune to ordinary psychic control: yes, Explosive destruction flag: no, Attached bombs permitted: yes, Veteran improvements: STRONGER,FIREPOWER,ROF,SIGHT,FASTER, Elite improvements: STRONGER,FIREPOWER,ROF, Can be crushed: no, Can gain rank: no.
