# Weapon paths: firing record, projectile and warhead

[Guide index](../README.md) | [Combat explanation](../03-COMBAT-ECONOMY.md)

Every explicit normal, secondary, elite, occupant, numbered-stage and death weapon on the registered object cards is represented. Additional weapon references reached through projectile/warhead effects are followed recursively. A special weapon's damage field must not automatically be interpreted as ordinary health damage.

Each card is read in order: choose weapon; check range/reload; create its effect/projectile; apply its warhead to the target. Percentages use the armor order explained in Combat. Unspecified fields are not invented defaults.

<a id="ra2-105mm"></a>

## Red Alert 2 - 105MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 105MM |
| Firing - base effect magnitude | 65 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | AP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 105MM, first property line 16693. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-105mme"></a>

## Red Alert 2 - 105MME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 105MME |
| Firing - base effect magnitude | 55 |
| Firing - reload interval | 75 |
| Firing - maximum range setting | 5 |
| Firing - Burst | 2 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | GRIZAPE |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | GRIZAPE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | VTEXPLOD |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 105MME, first property line 17736. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-120mm"></a>

## Red Alert 2 - 120MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 120MM |
| Firing - base effect magnitude | 90 |
| Firing - reload interval | 65 |
| Firing - maximum range setting | 5.75 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | AP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 120MM, first property line 16718. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-120mme"></a>

## Red Alert 2 - 120MME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 120MME |
| Firing - base effect magnitude | 85 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 5.75 |
| Firing - Burst | 2 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | RHINAPE |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RHINAPE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | VTEXPLOD |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 120MME, first property line 17762. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-120mmx"></a>

## Red Alert 2 - 120MMX

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 120MMX |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 5.75 |
| Firing - Burst | 2 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | ApocAP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ApocAP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,100%,100%,70%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | APOCEXP |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 120MMX, first property line 16705. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-120mmxe"></a>

## Red Alert 2 - 120MMXE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 120MMXE |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 5.75 |
| Firing - Burst | 4 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | ApocAPE |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ApocAPE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,100%,100%,100%,100%,70%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | VTEXPLOD |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 120MMXE, first property line 17749. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-155mm"></a>

## Red Alert 2 - 155MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 155MM |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 110 |
| Firing - maximum range setting | 8 |
| Firing - minimum range setting | 0 |
| Firing - Speed | 10 |
| Firing - Projectile | Ballistic |
| Firing - Warhead | ARTYHE |
| Projectile record | Ballistic |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ARTYHE |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,60%,100%,60%,60%,100%,80%,60%,100%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .25 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG |
| Warhead - Pronedamage | 50% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section 155MM, first property line 16797. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-155mme"></a>

## Red Alert 2 - 155MME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 155MME |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 110 |
| Firing - maximum range setting | 8 |
| Firing - minimum range setting | 0 |
| Firing - Burst | 2 |
| Firing - Speed | 10 |
| Firing - Projectile | Ballistic |
| Firing - Warhead | ARTYHE |
| Projectile record | Ballistic |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ARTYHE |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,60%,100%,60%,60%,100%,80%,60%,100%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .25 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG |
| Warhead - Pronedamage | 50% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section 155MME, first property line 17784. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-20mm"></a>

## Red Alert 2 - 20MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 20MM |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible3 |
| Firing - Warhead | SSA |
| Projectile record | Invisible3 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,70%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 20MM, first property line 16459. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-20mme"></a>

## Red Alert 2 - 20MME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 20MME |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 5 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible3 |
| Firing - Warhead | SSA |
| Projectile record | Invisible3 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,70%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 20MME, first property line 17774. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-20mmrapid"></a>

## Red Alert 2 - 20MMRAPID

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 20MMRAPID |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 5.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HARVWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HARVWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,20%,20%,20%,15%,10%,200%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 20MMRAPID, first property line 16449. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-20mmrapide"></a>

## Red Alert 2 - 20MMRAPIDE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 20MMRAPIDE |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 5.75 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | HowitzerWH |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HowitzerWH |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,60%,40%,40%,50%,40%,25%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 20MMRAPIDE, first property line 18056. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-90mm"></a>

## Red Alert 2 - 90MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 90MM |
| Firing - base effect magnitude | 36 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 5.75 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | AP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section 90MM, first property line 16681. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-alliedoccupyw"></a>

## Red Alert 2 - ALLIEDOCCUPYW

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ALLIEDOCCUPYW |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | SSAB |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSAB |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,30%,20%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section ALLIEDOCCUPYW, first property line 16112. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-alligatorbite"></a>

## Red Alert 2 - ALLIGATORBITE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ALLIGATORBITE |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section ALLIGATORBITE, first property line 16871. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-assaultbolt"></a>

## Red Alert 2 - ASSAULTBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ASSAULTBOLT |
| Firing - base effect magnitude | 10 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 1.83 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | ElectricAssault |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ElectricAssault |
| Warhead - armor effectiveness, ordered percentages | 0%,0,0%,0%,0%,0%,100%,100%,100%,50%,100% |
| Warhead - Infdeath | 5 |

Source: ra2.mix/local.mix/rules.ini, section ASSAULTBOLT, first property line 17111. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-aswbomb"></a>

## Red Alert 2 - ASWBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ASWBOMB |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 3 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 30 |
| Firing - Projectile | DepthCharge |
| Firing - Warhead | APSplash |
| Projectile record | DepthCharge |
| Projectile - Arm | 2 |
| Projectile - Rot | 1 |
| Warhead record | APSplash |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,65%,60%,25%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .8 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section ASWBOMB, first property line 16611. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-aswcollision"></a>

## Red Alert 2 - ASWCOLLISION

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ASWCOLLISION |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 30 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | AP |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section ASWCOLLISION, first property line 16647. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-aswlauncher"></a>

## Red Alert 2 - ASWLAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ASWLAUNCHER |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 150 |
| Firing - maximum range setting | -2 |
| Firing - Speed | 10 |
| Firing - Projectile | ASWVirt |
| Firing - Warhead | Special |
| Firing - Omnifire | yes |
| Firing - Spawner | yes |
| Projectile record | ASWVirt |
| Projectile - air targeting | no |
| Projectile - ground targeting | no |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | Special |

Source: ra2.mix/local.mix/rules.ini, section ASWLAUNCHER, first property line 16948. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-awp"></a>

## Red Alert 2 - AWP

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AWP |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 150 |
| Firing - maximum range setting | 14 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section AWP, first property line 16508. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-awpe"></a>

## Red Alert 2 - AWPE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AWPE |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 14 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section AWPE, first property line 18015. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-badteeth"></a>

## Red Alert 2 - BADTEETH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BADTEETH |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 30 |
| Firing - Projectile | DOGJUMP |
| Firing - Warhead | ParasiteDog |
| Projectile record | DOGJUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | ParasiteDog |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,0%,0% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: ra2.mix/local.mix/rules.ini, section BADTEETH, first property line 16848. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-barrelexplosion"></a>

## Red Alert 2 - BARRELEXPLOSION

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BARRELEXPLOSION |
| Firing - base effect magnitude | 200 |
| Firing - Projectile | Invisible |
| Firing - Warhead | OilExplosionWH |
| Projectile record | Invisible |
| Warhead record | OilExplosionWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,100%,90%,70%,50%,200%,90%,50%,100%,100% |
| Warhead - area spread | 4 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 4 |

Source: ra2.mix/local.mix/rules.ini, section BARRELEXPLOSION, first property line 16097. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-bearbite"></a>

## Red Alert 2 - BEARBITE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BEARBITE |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section BEARBITE, first property line 16881. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-blackhawkcannon"></a>

## Red Alert 2 - BLACKHAWKCANNON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BLACKHAWKCANNON |
| Firing - base effect magnitude | 35 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | QuadShell |
| Firing - Warhead | SA |
| Firing - Omnifire | yes |
| Projectile record | QuadShell |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: ra2.mix/local.mix/rules.ini, section BLACKHAWKCANNON, first property line 16530. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-blackhawkcannone"></a>

## Red Alert 2 - BLACKHAWKCANNONE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BLACKHAWKCANNONE |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | QuadShell |
| Firing - Warhead | SSA |
| Firing - Omnifire | yes |
| Projectile record | QuadShell |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,70%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section BLACKHAWKCANNONE, first property line 17932. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-blimpbomb"></a>

## Red Alert 2 - BLIMPBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BLIMPBOMB |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Burst | 1 |
| Firing - Speed | 20 |
| Firing - Projectile | BlimpBombP |
| Firing - Warhead | BlimpHE |
| Firing - Omnifire | yes |
| Projectile record | BlimpBombP |
| Projectile - Arm | 10 |
| Warhead record | BlimpHE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,35%,35%,85%,75%,50%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section BLIMPBOMB, first property line 16164. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-blimpbombe"></a>

## Red Alert 2 - BLIMPBOMBE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BLIMPBOMBE |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Burst | 1 |
| Firing - Speed | 20 |
| Firing - Projectile | BlimpBombP |
| Firing - Warhead | KTSTLEXP |
| Firing - Omnifire | yes |
| Projectile record | BlimpBombP |
| Projectile - Arm | 10 |
| Warhead record | KTSTLEXP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,35%,35%,85%,75%,50%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | KTSTLEXP |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section BLIMPBOMBE, first property line 17876. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-chimpbite"></a>

## Red Alert 2 - CHIMPBITE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CHIMPBITE |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section CHIMPBITE, first property line 16891. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-chronomp5"></a>

## Red Alert 2 - CHRONOMP5

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CHRONOMP5 |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPointNoBuilding |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPointNoBuilding |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,75%,1%,1%,1%,0%,0%,0%,75%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section CHRONOMP5, first property line 16488. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-chronomp5e"></a>

## Red Alert 2 - CHRONOMP5E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CHRONOMP5E |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPointNoBuilding |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPointNoBuilding |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,75%,1%,1%,1%,0%,0%,0%,75%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section CHRONOMP5E, first property line 18035. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-coilbolt"></a>

## Red Alert 2 - COILBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | COILBOLT |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible |
| Firing - Warhead | Electric |
| Projectile record | Invisible |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: ra2.mix/local.mix/rules.ini, section COILBOLT, first property line 17123. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-comet"></a>

## Red Alert 2 - COMET

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | COMET |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 10 |
| Firing - Speed | 40 |
| Firing - Projectile | LargeCometP |
| Firing - Warhead | CometWH |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | LargeCometP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | CometFragment |
| Warhead record | CometWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,50%,50%,200%,200%,200%,100%,100% |
| Warhead - Wall | no |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |

Source: ra2.mix/local.mix/rules.ini, section COMET, first property line 17434. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-cometfragment"></a>

## Red Alert 2 - COMETFRAGMENT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | COMETFRAGMENT |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 10 |
| Firing - Projectile | SmallCometP |
| Firing - Warhead | CometWH |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | SmallCometP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | CometWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,50%,50%,200%,200%,200%,100%,100% |
| Warhead - Wall | no |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |

Source: ra2.mix/local.mix/rules.ini, section COMETFRAGMENT, first property line 17452. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-cowshot"></a>

## Red Alert 2 - COWSHOT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | COWSHOT |
| Firing - base effect magnitude | 300 |
| Firing - reload interval | 75 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | PrismWarhead |
| Firing - Islaser | true |
| Firing - Isbiglaser | true |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | PrismWarhead |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,100%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Infdeath | 5 |

Source: ra2.mix/local.mix/rules.ini, section COWSHOT, first property line 17631. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-crelectricbolt"></a>

## Red Alert 2 - CRELECTRICBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRELECTRICBOLT |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 45 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Shock |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Shock |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: ra2.mix/local.mix/rules.ini, section CRELECTRICBOLT, first property line 17491. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-crflakguygun"></a>

## Red Alert 2 - CRFLAKGUYGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRFLAKGUYGUN |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,50%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .2 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: ra2.mix/local.mix/rules.ini, section CRFLAKGUYGUN, first property line 17656. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-crm60"></a>

## Red Alert 2 - CRM60

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRM60 |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SSA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,70%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section CRM60, first property line 17480. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-crmindcontrol"></a>

## Red Alert 2 - CRMINDCONTROL

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRMINDCONTROL |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 1 |
| Firing - Projectile | Psychic |
| Firing - Warhead | PsiPulse |
| Projectile record | Psychic |
| Warhead record | PsiPulse |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,0%,0% |
| Warhead - area spread | 3 |
| Warhead - Percentatmax | .85 |
| Warhead - Psychicdamage | yes |
| Warhead - Infdeath | 6 |

Source: ra2.mix/local.mix/rules.ini, section CRMINDCONTROL, first property line 17607. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-crmp5"></a>

## Red Alert 2 - CRMP5

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRMP5 |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint3 |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint3 |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,2%,2%,2%,2%,2%,2%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section CRMP5, first property line 17512. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-crneutronrifle"></a>

## Red Alert 2 - CRNEUTRONRIFLE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRNEUTRONRIFLE |
| Firing - base effect magnitude | 10 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | ChronoBeam |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ChronoBeam |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Temporal | yes |

Source: ra2.mix/local.mix/rules.ini, section CRNEUTRONRIFLE, first property line 17536. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-crnuke"></a>

## Red Alert 2 - CRNUKE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRNUKE |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 35 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | CRNUKEWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | CRNUKEWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,90%,50%,50%,60%,150%,20%,100%,100% |
| Warhead - area spread | 5 |
| Warhead - Percentatmax | .25 |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | MININUKE - added 11/30 |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section CRNUKE, first property line 17557. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-crradbeamweapon"></a>

## Red Alert 2 - CRRADBEAMWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRRADBEAMWEAPON |
| Firing - base effect magnitude | 175 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | RadBeamWarhead |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RadBeamWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,20%,15%,10%,0%,0%,0%,100%,100% |
| Warhead - Radiation | yes |
| Warhead - Infdeath | 7 |

Source: ra2.mix/local.mix/rules.ini, section CRRADBEAMWEAPON, first property line 17589. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-crterrorbomb"></a>

## Red Alert 2 - CRTERRORBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRTERRORBOMB |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible |
| Firing - Warhead | TerrorBombWH |
| Projectile record | Invisible |
| Warhead record | TerrorBombWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,100%,90%,50%,50%,100%,150%,30%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .5 |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | MININUKE |

Source: ra2.mix/local.mix/rules.ini, section CRTERRORBOMB, first property line 17568. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-defaultdeathweapon"></a>

## Red Alert 2 - DEFAULTDEATHWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DEFAULTDEATHWEAPON |
| Firing - Projectile | Invisible |
| Firing - Warhead | DeathWH |
| Projectile record | Invisible |
| Warhead record | DeathWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - area spread | 1.5 |
| Warhead - Percentatmax | .5 |
| Warhead - Infdeath | 3 |

Source: ra2.mix/local.mix/rules.ini, section DEFAULTDEATHWEAPON, first property line 16087. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-defusekit"></a>

## Red Alert 2 - DEFUSEKIT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DEFUSEKIT |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | BombDisarm |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | BombDisarm |

Source: ra2.mix/local.mix/rules.ini, section DEFUSEKIT, first property line 17237. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-demobomb"></a>

## Red Alert 2 - DEMOBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DEMOBOMB |
| Firing - base effect magnitude | 300 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 35 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | DemobombWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | DemobombWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,50%,50%,80%,150%,10%,100%,100% |
| Warhead - area spread | 8 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | DEMTEXP |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section DEMOBOMB, first property line 17577. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-doublepistols"></a>

## Red Alert 2 - DOUBLEPISTOLS

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DOUBLEPISTOLS |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section DOUBLEPISTOLS, first property line 16478. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-doublepistolse"></a>

## Red Alert 2 - DOUBLEPISTOLSE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DOUBLEPISTOLSE |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section DOUBLEPISTOLSE, first property line 18092. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-dredlauncher"></a>

## Red Alert 2 - DREDLAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DREDLAUNCHER |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 25 |
| Firing - minimum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 15 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | Special |
| Firing - Omnifire | yes |
| Firing - Spawner | yes |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Special |

Source: ra2.mix/local.mix/rules.ini, section DREDLAUNCHER, first property line 16823. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-dronejump"></a>

## Red Alert 2 - DRONEJUMP

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DRONEJUMP |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 1.83 |
| Firing - Speed | 30 |
| Firing - Projectile | JUMP |
| Firing - Warhead | Parasite |
| Projectile record | JUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | Parasite |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,0%,0% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: ra2.mix/local.mix/rules.ini, section DRONEJUMP, first property line 16837. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-eiffelbolt"></a>

## Red Alert 2 - EIFFELBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | EIFFELBOLT |
| Firing - base effect magnitude | 2000 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 20 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | Electric |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: ra2.mix/local.mix/rules.ini, section EIFFELBOLT, first property line 17148. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-electricbolt"></a>

## Red Alert 2 - ELECTRICBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ELECTRICBOLT |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Shock |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Shock |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: ra2.mix/local.mix/rules.ini, section ELECTRICBOLT, first property line 17088. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-electricbolte"></a>

## Red Alert 2 - ELECTRICBOLTE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ELECTRICBOLTE |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | Electricbounce |
| Firing - Warhead | Shock |
| Projectile record | Electricbounce |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | TeslaFragment |
| Warhead record | Shock |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: ra2.mix/local.mix/rules.ini, section ELECTRICBOLTE, first property line 17808. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-fakec4"></a>

## Red Alert 2 - FAKEC4

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FAKEC4 |
| Firing - base effect magnitude | 5000 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | FakeC4WH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FakeC4WH |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,0%,0%,0%,100%,100%,100%,0%,100% |
| Warhead - area spread | 0 |

Source: ra2.mix/local.mix/rules.ini, section FAKEC4, first property line 16497. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flakguyaagun"></a>

## Red Alert 2 - FLAKGUYAAGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKGUYAAGUN |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakGuyWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakGuyWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,50%,80%,20%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .2 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKGUYAAGUN, first property line 17404. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flakguyaagune"></a>

## Red Alert 2 - FLAKGUYAAGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKGUYAAGUNE |
| Firing - base effect magnitude | 8 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakGuyWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakGuyWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,50%,80%,20%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .2 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKGUYAAGUNE, first property line 17724. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flakguygun"></a>

## Red Alert 2 - FLAKGUYGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKGUYGUN |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,50%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .2 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKGUYGUN, first property line 17424. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flakguygune"></a>

## Red Alert 2 - FLAKGUYGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKGUYGUNE |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 5 |
| Firing - Burst | 2 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,50%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .2 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKGUYGUNE, first property line 17713. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flaktrackaagun"></a>

## Red Alert 2 - FLAKTRACKAAGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKTRACKAAGUN |
| Firing - base effect magnitude | 35 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 10 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakWH |
| Warhead - armor effectiveness, ordered percentages | 150%,80%,50%,100%,20%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKTRACKAAGUN, first property line 17394. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flaktrackaagune"></a>

## Red Alert 2 - FLAKTRACKAAGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKTRACKAAGUNE |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakWH |
| Warhead - armor effectiveness, ordered percentages | 150%,80%,50%,100%,20%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKTRACKAAGUNE, first property line 17691. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flaktrackgun"></a>

## Red Alert 2 - FLAKTRACKGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKTRACKGUN |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,50%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .2 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKTRACKGUN, first property line 17414. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flaktrackgune"></a>

## Red Alert 2 - FLAKTRACKGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKTRACKGUNE |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 5 |
| Firing - Burst | 2 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,50%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .2 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKTRACKGUNE, first property line 17702. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flakweapon"></a>

## Red Alert 2 - FLAKWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKWEAPON |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakWH |
| Warhead - armor effectiveness, ordered percentages | 150%,80%,50%,100%,20%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKWEAPON, first property line 17384. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-flakweapone"></a>

## Red Alert 2 - FLAKWEAPONE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKWEAPONE |
| Firing - base effect magnitude | 35 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 10 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakWH |
| Warhead - armor effectiveness, ordered percentages | 150%,80%,50%,100%,20%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: ra2.mix/local.mix/rules.ini, section FLAKWEAPONE, first property line 17680. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-goodteeth"></a>

## Red Alert 2 - GOODTEETH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | GOODTEETH |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 30 |
| Firing - Projectile | ADOGJUMP |
| Firing - Warhead | ParasiteDog |
| Projectile record | ADOGJUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | ParasiteDog |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,0%,0% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: ra2.mix/local.mix/rules.ini, section GOODTEETH, first property line 16860. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-grandcannonweapon"></a>

## Red Alert 2 - GRANDCANNONWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | GRANDCANNONWEAPON |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 15 |
| Firing - minimum range setting | 3 |
| Firing - Speed | 1 |
| Firing - Projectile | GrandCannonBall |
| Firing - Warhead | GrandCannonWH |
| Projectile record | GrandCannonBall |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | GrandCannonWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,50%,100%,50%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .2 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 30% |

Source: ra2.mix/local.mix/rules.ini, section GRANDCANNONWEAPON, first property line 17372. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-hornetbomb"></a>

## Red Alert 2 - HORNETBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HORNETBOMB |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 3 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 30 |
| Firing - Projectile | NormalBomb |
| Firing - Warhead | ORCAAP |
| Projectile record | NormalBomb |
| Projectile - Arm | 2 |
| Projectile - Rot | 1 |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section HORNETBOMB, first property line 16602. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-hornetbombe"></a>

## Red Alert 2 - HORNETBOMBE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HORNETBOMBE |
| Firing - base effect magnitude | 80 |
| Firing - reload interval | 3 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 30 |
| Firing - Projectile | NormalBomb |
| Firing - Warhead | ARTYHE |
| Projectile record | NormalBomb |
| Projectile - Arm | 2 |
| Projectile - Rot | 1 |
| Warhead record | ARTYHE |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,60%,100%,60%,60%,100%,80%,60%,100%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .25 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG |
| Warhead - Pronedamage | 50% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section HORNETBOMBE, first property line 17920. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-hornetcollision"></a>

## Red Alert 2 - HORNETCOLLISION

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HORNETCOLLISION |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 30 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | AP |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section HORNETCOLLISION, first property line 16626. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-hornetlauncher"></a>

## Red Alert 2 - HORNETLAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HORNETLAUNCHER |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 150 |
| Firing - maximum range setting | 25 |
| Firing - Speed | 10 |
| Firing - Projectile | Invisible |
| Firing - Warhead | Special |
| Firing - Omnifire | yes |
| Firing - Spawner | yes |
| Projectile record | Invisible |
| Warhead record | Special |

Source: ra2.mix/local.mix/rules.ini, section HORNETLAUNCHER, first property line 16936. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-hovermissile"></a>

## Red Alert 2 - HOVERMISSILE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HOVERMISSILE |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 6 |
| Firing - minimum range setting | 1 |
| Firing - Burst | 2 |
| Firing - Speed | 40 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | HE |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,70%,35%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section HOVERMISSILE, first property line 16285. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-hovermissilee"></a>

## Red Alert 2 - HOVERMISSILEE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HOVERMISSILEE |
| Firing - base effect magnitude | 80 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 6 |
| Firing - minimum range setting | 1 |
| Firing - Burst | 4 |
| Firing - Speed | 40 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | HE |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,70%,35%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section HOVERMISSILEE, first property line 17992. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-howitzergun"></a>

## Red Alert 2 - HOWITZERGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HOWITZERGUN |
| Firing - base effect magnitude | 75 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 12 |
| Firing - minimum range setting | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Ballistic |
| Firing - Warhead | HowitzerWH |
| Projectile record | Ballistic |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HowitzerWH |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,60%,40%,40%,50%,40%,25%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section HOWITZERGUN, first property line 16754. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-ivanbomber"></a>

## Red Alert 2 - IVANBOMBER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | IVANBOMBER |
| Firing - base effect magnitude | 400 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible |
| Firing - Warhead | IvanBomb |
| Projectile record | Invisible |
| Warhead record | IvanBomb |
| Warhead - Ivanbomb | yes |

Source: ra2.mix/local.mix/rules.ini, section IVANBOMBER, first property line 17306. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-ivanbombere"></a>

## Red Alert 2 - IVANBOMBERE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | IVANBOMBERE |
| Firing - base effect magnitude | 600 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible |
| Firing - Warhead | IvanBomb |
| Projectile record | Invisible |
| Warhead record | IvanBomb |
| Warhead - Ivanbomb | yes |

Source: ra2.mix/local.mix/rules.ini, section IVANBOMBERE, first property line 17943. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-m1carbine"></a>

## Red Alert 2 - M1CARBINE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | M1CARBINE |
| Firing - base effect magnitude | 15 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: ra2.mix/local.mix/rules.ini, section M1CARBINE, first property line 16421. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-m1carbinee"></a>

## Red Alert 2 - M1CARBINEE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | M1CARBINEE |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: ra2.mix/local.mix/rules.ini, section M1CARBINEE, first property line 17671. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-m60"></a>

## Red Alert 2 - M60

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | M60 |
| Firing - base effect magnitude | 15 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: ra2.mix/local.mix/rules.ini, section M60, first property line 16430. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-m60e"></a>

## Red Alert 2 - M60E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | M60E |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: ra2.mix/local.mix/rules.ini, section M60E, first property line 18128. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-makeupkit"></a>

## Red Alert 2 - MAKEUPKIT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAKEUPKIT |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | -2 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | Snapshot |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | Snapshot |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,100%,100% |

Source: ra2.mix/local.mix/rules.ini, section MAKEUPKIT, first property line 17335. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-mammothtusk"></a>

## Red Alert 2 - MAMMOTHTUSK

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAMMOTHTUSK |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 20 |
| Firing - Projectile | AAHeatSeeker |
| Firing - Warhead | HE |
| Projectile record | AAHeatSeeker |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 80 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,70%,35%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section MAMMOTHTUSK, first property line 16786. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-maverick"></a>

## Red Alert 2 - MAVERICK

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICK |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | ORCAAP |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section MAVERICK, first property line 16564. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-maverick2"></a>

## Red Alert 2 - MAVERICK2

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICK2 |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | ORCAAP |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section MAVERICK2, first property line 16574. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-maverick2e"></a>

## Red Alert 2 - MAVERICK2E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICK2E |
| Firing - base effect magnitude | 400 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 9 |
| Firing - Burst | 2 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | ORCAAP |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section MAVERICK2E, first property line 17910. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-mavericke"></a>

## Red Alert 2 - MAVERICKE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICKE |
| Firing - base effect magnitude | 300 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 9 |
| Firing - Burst | 4 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | ORCAAP |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section MAVERICKE, first property line 17900. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-mayanprism"></a>

## Red Alert 2 - MAYANPRISM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAYANPRISM |
| Firing - base effect magnitude | 1000 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 25 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | PrismWarhead |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | PrismWarhead |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,100%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Infdeath | 5 |

Source: ra2.mix/local.mix/rules.ini, section MAYANPRISM, first property line 17056. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-medusa"></a>

## Red Alert 2 - MEDUSA

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MEDUSA |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 120 |
| Firing - Projectile | MedusaProjectile |
| Firing - Warhead | SAMWH |
| Firing - Omnifire | yes |
| Projectile record | MedusaProjectile |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Arm | 1 |
| Projectile - Rot | 20 |
| Projectile - High | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SAMWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | 1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section MEDUSA, first property line 16310. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-medusae"></a>

## Red Alert 2 - MEDUSAE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MEDUSAE |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 5 |
| Firing - maximum range setting | 14 |
| Firing - Burst | 2 |
| Firing - Speed | 150 |
| Firing - Projectile | MedusaProjectile |
| Firing - Warhead | SAMWH |
| Firing - Omnifire | yes |
| Projectile record | MedusaProjectile |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Arm | 1 |
| Projectile - Rot | 20 |
| Projectile - High | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SAMWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | 1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section MEDUSAE, first property line 18080. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-mindcontrol"></a>

## Red Alert 2 - MINDCONTROL

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MINDCONTROL |
| Firing - base effect magnitude | 10 |
| Firing - reload interval | 200 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | PsychicControl |
| Firing - Warhead | Controller |
| Projectile record | PsychicControl |
| Warhead record | Controller |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - Mindcontrol | yes |
| Warhead - Animlist | YURICNTL |

Source: ra2.mix/local.mix/rules.ini, section MINDCONTROL, first property line 17271. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-mindcontrole"></a>

## Red Alert 2 - MINDCONTROLE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MINDCONTROLE |
| Firing - base effect magnitude | 10 |
| Firing - reload interval | 200 |
| Firing - maximum range setting | 14 |
| Firing - Speed | 100 |
| Firing - Projectile | PsychicControl |
| Firing - Warhead | Controller |
| Projectile record | PsychicControl |
| Warhead record | Controller |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - Mindcontrol | yes |
| Warhead - Animlist | YURICNTL |

Source: ra2.mix/local.mix/rules.ini, section MINDCONTROLE, first property line 18067. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-miragegun"></a>

## Red Alert 2 - MIRAGEGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MIRAGEGUN |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 70 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | MirageWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | MirageWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,80%,100%,100%,100%,30%,20%,20%,100%,100% |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | IRONFX |

Source: ra2.mix/local.mix/rules.ini, section MIRAGEGUN, first property line 17358. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-miragegune"></a>

## Red Alert 2 - MIRAGEGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MIRAGEGUNE |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 9 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | MirageWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | MirageWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,80%,100%,100%,100%,30%,20%,20%,100%,100% |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | IRONFX |

Source: ra2.mix/local.mix/rules.ini, section MIRAGEGUNE, first property line 17863. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-mp5"></a>

## Red Alert 2 - MP5

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MP5 |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section MP5, first property line 16468. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-mp5e"></a>

## Red Alert 2 - MP5E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MP5E |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section MP5E, first property line 18025. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-neutronrifle"></a>

## Red Alert 2 - NEUTRONRIFLE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | NEUTRONRIFLE |
| Firing - base effect magnitude | 8 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | ChronoBeam |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ChronoBeam |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Temporal | yes |

Source: ra2.mix/local.mix/rules.ini, section NEUTRONRIFLE, first property line 17003. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-neutronriflee"></a>

## Red Alert 2 - NEUTRONRIFLEE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | NEUTRONRIFLEE |
| Firing - base effect magnitude | 16 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | ChronoBeam |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ChronoBeam |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Temporal | yes |

Source: ra2.mix/local.mix/rules.ini, section NEUTRONRIFLEE, first property line 17890. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-nukecarrier"></a>

## Red Alert 2 - NUKECARRIER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | NUKECARRIER |
| Firing - Speed | 100 |
| Firing - Projectile | GiantNukeUp |
| Firing - Warhead | NukeMaker |
| Projectile record | GiantNukeUp |
| Projectile - Arm | 2 |
| Warhead record | NukeMaker |

Source: ra2.mix/local.mix/rules.ini, section NUKECARRIER, first property line 17257. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-nukepayload"></a>

## Red Alert 2 - NUKEPAYLOAD

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | NUKEPAYLOAD |
| Firing - base effect magnitude | 600 |
| Firing - maximum range setting | 30 |
| Firing - Speed | 10 |
| Firing - Projectile | GiantNukeDown |
| Firing - Warhead | NUKE |
| Projectile record | GiantNukeDown |
| Projectile - Arm | 2 |
| Warhead record | NUKE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,200%,100%,100%,60%,100%,8%,100%,100% |
| Warhead - area spread | 10 |
| Warhead - Percentatmax | .02 |
| Warhead - Wood | yes |
| Warhead - Infdeath | 7 |
| Warhead - Animlist | NUKEANIM |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section NUKEPAYLOAD, first property line 17248. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-oilexplosion"></a>

## Red Alert 2 - OILEXPLOSION

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | OILEXPLOSION |
| Firing - base effect magnitude | 600 |
| Firing - Projectile | Invisible |
| Firing - Warhead | OilExplosionWH |
| Projectile record | Invisible |
| Warhead record | OilExplosionWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,100%,90%,70%,50%,200%,90%,50%,100%,100% |
| Warhead - area spread | 4 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 4 |

Source: ra2.mix/local.mix/rules.ini, section OILEXPLOSION, first property line 16091. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-opcoilbolt"></a>

## Red Alert 2 - OPCOILBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | OPCOILBOLT |
| Firing - base effect magnitude | 300 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | Electric |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: ra2.mix/local.mix/rules.ini, section OPCOILBOLT, first property line 17136. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-para"></a>

## Red Alert 2 - PARA

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PARA |
| Firing - base effect magnitude | 15 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SSA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,70%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section PARA, first property line 16440. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-paradropweapon"></a>

## Red Alert 2 - PARADROPWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PARADROPWEAPON |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 130 |
| Firing - maximum range setting | 4 |
| Firing - Burst | 1 |
| Firing - Speed | 30 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | MaverickHE |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | MaverickHE |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,100%,50%,50%,100%,75%,50%,25%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section PARADROPWEAPON, first property line 16584. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-parae"></a>

## Red Alert 2 - PARAE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PARAE |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 5 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SSA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,70%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section PARAE, first property line 18138. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-pistola"></a>

## Red Alert 2 - PISTOLA

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PISTOLA |
| Firing - base effect magnitude | 2 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: ra2.mix/local.mix/rules.ini, section PISTOLA, first property line 17262. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-prismshot"></a>

## Red Alert 2 - PRISMSHOT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PRISMSHOT |
| Firing - base effect magnitude | 120 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | PrismWarhead |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | PrismWarhead |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,100%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Infdeath | 5 |

Source: ra2.mix/local.mix/rules.ini, section PRISMSHOT, first property line 17039. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-prismsupport"></a>

## Red Alert 2 - PRISMSUPPORT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PRISMSUPPORT |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | DummyWarhead |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | DummyWarhead |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,0%,0%,0%,0%,0%,0%,0%,0% |

Source: ra2.mix/local.mix/rules.ini, section PRISMSUPPORT, first property line 17072. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-psiwave"></a>

## Red Alert 2 - PSIWAVE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PSIWAVE |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 1 |
| Firing - Projectile | Psychic |
| Firing - Warhead | PsiPulse |
| Projectile record | Psychic |
| Warhead record | PsiPulse |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,0%,0% |
| Warhead - area spread | 3 |
| Warhead - Percentatmax | .85 |
| Warhead - Psychicdamage | yes |
| Warhead - Infdeath | 6 |

Source: ra2.mix/local.mix/rules.ini, section PSIWAVE, first property line 17294. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-radbeamweapon"></a>

## Red Alert 2 - RADBEAMWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | RADBEAMWEAPON |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | RadBeamWarhead |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RadBeamWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,20%,15%,10%,0%,0%,0%,100%,100% |
| Warhead - Radiation | yes |
| Warhead - Infdeath | 7 |

Source: ra2.mix/local.mix/rules.ini, section RADBEAMWEAPON, first property line 17014. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-radbeamweapone"></a>

## Red Alert 2 - RADBEAMWEAPONE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | RADBEAMWEAPONE |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | RadBeamWarhead |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RadBeamWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,20%,15%,10%,0%,0%,0%,100%,100% |
| Warhead - Radiation | yes |
| Warhead - Infdeath | 7 |

Source: ra2.mix/local.mix/rules.ini, section RADBEAMWEAPONE, first property line 17954. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-raderuptionweapon"></a>

## Red Alert 2 - RADERUPTIONWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | RADERUPTIONWEAPON |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 1 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | RadEruptionWarhead |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RadEruptionWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,20%,10%,10%,0%,0%,0%,100%,100% |
| Warhead - area spread | 10 |
| Warhead - Radiation | yes |
| Warhead - Infdeath | 7 |

Source: ra2.mix/local.mix/rules.ini, section RADERUPTIONWEAPON, first property line 17025. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-redeye2"></a>

## Red Alert 2 - REDEYE2

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | REDEYE2 |
| Firing - base effect magnitude | 75 |
| Firing - reload interval | 55 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 100 |
| Firing - Projectile | AAHeatSeeker |
| Firing - Warhead | SAMWH |
| Projectile record | AAHeatSeeker |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 80 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SAMWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | 1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML |
| Warhead - Pronedamage | 100% |

Source: ra2.mix/local.mix/rules.ini, section REDEYE2, first property line 16274. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-repairbullet"></a>

## Red Alert 2 - REPAIRBULLET

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | REPAIRBULLET |
| Firing - base effect magnitude | -50 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 1.8 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible |
| Firing - Warhead | Mechanical |
| Projectile record | Invisible |
| Warhead record | Mechanical |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Infdeath | 0 |

Source: ra2.mix/local.mix/rules.ini, section REPAIRBULLET, first property line 16979. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-sabot"></a>

## Red Alert 2 - SABOT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SABOT |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 70 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 60 |
| Firing - Projectile | Cannon |
| Firing - Warhead | UltraAP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | UltraAP |
| Warhead - armor effectiveness, ordered percentages | 2%,2%,2%,100%,40%,100%,2%,2%,2%,2%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN30 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section SABOT, first property line 16742. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-sabote"></a>

## Red Alert 2 - SABOTE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SABOTE |
| Firing - base effect magnitude | 175 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 6.75 |
| Firing - Burst | 2 |
| Firing - Speed | 60 |
| Firing - Projectile | Cannon |
| Firing - Warhead | UltraAPE |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | UltraAPE |
| Warhead - armor effectiveness, ordered percentages | 2%,2%,2%,100%,50%,100%,2%,2%,2%,100%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | VTEXPLOD |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section SABOTE, first property line 18044. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-sapper"></a>

## Red Alert 2 - SAPPER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SAPPER |
| Firing - base effect magnitude | 2500 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible5 |
| Firing - Warhead | Super |
| Projectile record | Invisible5 |
| Projectile - air targeting | no |
| Projectile - ground targeting | no |
| Warhead record | Super |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 100% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section SAPPER, first property line 16407. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-soniczap"></a>

## Red Alert 2 - SONICZAP

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SONICZAP |
| Firing - base effect magnitude | 4 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | Sonic |
| Firing - Warhead | SonicWarhead |
| Firing - Issonic | Yes |
| Projectile record | Sonic |
| Warhead record | SonicWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,80%,80%,100%,60%,60%,100%,100% |
| Warhead - area spread | .1 |
| Warhead - Percentatmax | 1 |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Pronedamage | 50% |
| Warhead - Sonic | yes |

Source: ra2.mix/local.mix/rules.ini, section SONICZAP, first property line 16963. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-soniczape"></a>

## Red Alert 2 - SONICZAPE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SONICZAPE |
| Firing - base effect magnitude | 8 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Sonic |
| Firing - Warhead | SonicWarhead |
| Firing - Issonic | Yes |
| Projectile record | Sonic |
| Warhead record | SonicWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,80%,80%,100%,60%,60%,100%,100% |
| Warhead - area spread | .1 |
| Warhead - Percentatmax | 1 |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Pronedamage | 50% |
| Warhead - Sonic | yes |

Source: ra2.mix/local.mix/rules.ini, section SONICZAPE, first property line 17977. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-sovietoccupyw"></a>

## Red Alert 2 - SOVIETOCCUPYW

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SOVIETOCCUPYW |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | SSAB |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSAB |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,30%,20%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section SOVIETOCCUPYW, first property line 16122. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-squidgrab"></a>

## Red Alert 2 - SQUIDGRAB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SQUIDGRAB |
| Firing - base effect magnitude | 15 |
| Firing - reload interval | 99 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 30 |
| Firing - Projectile | SQDJUMP |
| Firing - Warhead | ParasitePlus |
| Projectile record | SQDJUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | ParasitePlus |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: ra2.mix/local.mix/rules.ini, section SQUIDGRAB, first property line 16910. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-squidgrabe"></a>

## Red Alert 2 - SQUIDGRABE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SQUIDGRABE |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 99 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 30 |
| Firing - Projectile | SQDJUMP |
| Firing - Warhead | ParasitePlus |
| Projectile record | SQDJUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | ParasitePlus |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: ra2.mix/local.mix/rules.ini, section SQUIDGRABE, first property line 18103. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-squidpunch"></a>

## Red Alert 2 - SQUIDPUNCH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SQUIDPUNCH |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 32 |
| Firing - maximum range setting | 1.83 |
| Firing - Speed | 30 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HE |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,70%,35%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section SQUIDPUNCH, first property line 16924. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-squidpunche"></a>

## Red Alert 2 - SQUIDPUNCHE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SQUIDPUNCHE |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 32 |
| Firing - maximum range setting | 1.83 |
| Firing - Speed | 30 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | HE |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,70%,35%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section SQUIDPUNCHE, first property line 18118. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-subtorpedo"></a>

## Red Alert 2 - SUBTORPEDO

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUBTORPEDO |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 25 |
| Firing - Projectile | Torpedo |
| Firing - Warhead | APSplash |
| Projectile record | Torpedo |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 12 |
| Warhead record | APSplash |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,65%,60%,25%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .8 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section SUBTORPEDO, first property line 16253. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-subtorpedoe"></a>

## Red Alert 2 - SUBTORPEDOE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUBTORPEDOE |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 7 |
| Firing - Burst | 2 |
| Firing - Speed | 18 |
| Firing - Projectile | Torpedo |
| Firing - Warhead | APSplash |
| Projectile record | Torpedo |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 12 |
| Warhead record | APSplash |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,65%,60%,25%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .8 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: ra2.mix/local.mix/rules.ini, section SUBTORPEDOE, first property line 17966. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-supercomet"></a>

## Red Alert 2 - SUPERCOMET

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUPERCOMET |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 10 |
| Firing - Speed | 10 |
| Firing - Projectile | SuperCometP |
| Firing - Warhead | CometWH |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | SuperCometP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | SuperCometFragment |
| Warhead record | CometWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,50%,50%,200%,200%,200%,100%,100% |
| Warhead - Wall | no |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |

Source: ra2.mix/local.mix/rules.ini, section SUPERCOMET, first property line 17831. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-supercometfragment"></a>

## Red Alert 2 - SUPERCOMETFRAGMENT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUPERCOMETFRAGMENT |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 10 |
| Firing - Projectile | SuperSmallCometP |
| Firing - Warhead | CometWH |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | SuperSmallCometP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | CometFragment |
| Warhead record | CometWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,50%,50%,200%,200%,200%,100%,100% |
| Warhead - Wall | no |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |

Source: ra2.mix/local.mix/rules.ini, section SUPERCOMETFRAGMENT, first property line 17847. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-supermindcontrol"></a>

## Red Alert 2 - SUPERMINDCONTROL

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUPERMINDCONTROL |
| Firing - base effect magnitude | 10 |
| Firing - reload interval | 200 |
| Firing - maximum range setting | 30 |
| Firing - Speed | 100 |
| Firing - Projectile | PsychicControl |
| Firing - Warhead | Controller |
| Projectile record | PsychicControl |
| Warhead record | Controller |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - Mindcontrol | yes |
| Warhead - Animlist | YURICNTL |

Source: ra2.mix/local.mix/rules.ini, section SUPERMINDCONTROL, first property line 17282. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-tankbolt"></a>

## Red Alert 2 - TANKBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TANKBOLT |
| Firing - base effect magnitude | 135 |
| Firing - reload interval | 75 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Electric |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: ra2.mix/local.mix/rules.ini, section TANKBOLT, first property line 17100. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-tankbolte"></a>

## Red Alert 2 - TANKBOLTE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TANKBOLTE |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | Electricbounce |
| Firing - Warhead | Electric |
| Projectile record | Electricbounce |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | TeslaFragment |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: ra2.mix/local.mix/rules.ini, section TANKBOLTE, first property line 17797. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-terrorbomb"></a>

## Red Alert 2 - TERRORBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TERRORBOMB |
| Firing - base effect magnitude | 225 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible |
| Firing - Warhead | TerrorBombWH |
| Projectile record | Invisible |
| Warhead record | TerrorBombWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,100%,90%,50%,50%,100%,150%,30%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .5 |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | MININUKE |

Source: ra2.mix/local.mix/rules.ini, section TERRORBOMB, first property line 16103. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-teslafragment"></a>

## Red Alert 2 - TESLAFRAGMENT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TESLAFRAGMENT |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 10 |
| Firing - Projectile | SmallTeslaP |
| Firing - Warhead | Electric |
| Projectile record | SmallTeslaP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: ra2.mix/local.mix/rules.ini, section TESLAFRAGMENT, first property line 17467. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-v3cluster"></a>

## Red Alert 2 - V3CLUSTER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | V3CLUSTER |
| Firing - base effect magnitude | 80 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 20 |
| Firing - Projectile | ClusterBits |
| Firing - Warhead | V3HE |
| Projectile record | ClusterBits |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Warhead record | V3HE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,30%,5%,5%,85%,50%,30%,100%,0% |
| Warhead - area spread | .9 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Tiberium | yes |

Source: ra2.mix/local.mix/rules.ini, section V3CLUSTER, first property line 17315. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-v3launcher"></a>

## Red Alert 2 - V3LAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | V3LAUNCHER |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 150 |
| Firing - maximum range setting | 18 |
| Firing - minimum range setting | 5 |
| Firing - Speed | 10 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | Special |
| Firing - Spawner | yes |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Special |

Source: ra2.mix/local.mix/rules.ini, section V3LAUNCHER, first property line 16812. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-virtualscanner"></a>

## Red Alert 2 - VIRTUALSCANNER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | VIRTUALSCANNER |
| Firing - base effect magnitude | 1 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | SA |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: ra2.mix/local.mix/rules.ini, section VIRTUALSCANNER, first property line 16901. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-vulcan"></a>

## Red Alert 2 - VULCAN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | VULCAN |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 26 |
| Firing - maximum range setting | 5.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: ra2.mix/local.mix/rules.ini, section VULCAN, first property line 16350. Projectile/warhead rows use the named sections in that same rules source.

<a id="ra2-vulcan2"></a>

## Red Alert 2 - VULCAN2

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | VULCAN2 |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 26 |
| Firing - maximum range setting | 5.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: ra2.mix/local.mix/rules.ini, section VULCAN2, first property line 16230. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-105mm"></a>

## Yuri's Revenge - 105MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 105MM |
| Firing - base effect magnitude | 65 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | AP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,15%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section 105MM, first property line 23326. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-105mme"></a>

## Yuri's Revenge - 105MME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 105MME |
| Firing - base effect magnitude | 65 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 5 |
| Firing - Burst | 2 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | GRIZAPE |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | GRIZAPE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | VTEXPLOD |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section 105MME, first property line 24787. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-120mm"></a>

## Yuri's Revenge - 120MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 120MM |
| Firing - base effect magnitude | 90 |
| Firing - reload interval | 65 |
| Firing - maximum range setting | 5.75 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | AP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,15%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section 120MM, first property line 23351. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-120mme"></a>

## Yuri's Revenge - 120MME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 120MME |
| Firing - base effect magnitude | 90 |
| Firing - reload interval | 65 |
| Firing - maximum range setting | 5.75 |
| Firing - Burst | 2 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | RHINAPE |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RHINAPE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | VTEXPLOD |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section 120MME, first property line 24813. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-120mmx"></a>

## Yuri's Revenge - 120MMX

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 120MMX |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 5.75 |
| Firing - Burst | 2 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | ApocAP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ApocAP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,100%,100%,70%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | APOCEXP |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section 120MMX, first property line 23338. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-120mmxe"></a>

## Yuri's Revenge - 120MMXE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 120MMXE |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 5.75 |
| Firing - Burst | 4 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | ApocAPE |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ApocAPE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,100%,100%,100%,100%,70%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | VTEXPLOD |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section 120MMXE, first property line 24800. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-155mm"></a>

## Yuri's Revenge - 155MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 155MM |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 110 |
| Firing - maximum range setting | 8 |
| Firing - minimum range setting | 0 |
| Firing - Speed | 10 |
| Firing - Projectile | Ballistic |
| Firing - Warhead | ARTYHE |
| Projectile record | Ballistic |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ARTYHE |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,60%,100%,60%,60%,100%,100%,60%,100%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .25 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG |
| Warhead - Pronedamage | 50% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section 155MM, first property line 23453. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-155mme"></a>

## Yuri's Revenge - 155MME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 155MME |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 110 |
| Firing - maximum range setting | 8 |
| Firing - minimum range setting | 0 |
| Firing - Burst | 2 |
| Firing - Speed | 10 |
| Firing - Projectile | Ballistic |
| Firing - Warhead | ARTYHE |
| Projectile record | Ballistic |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ARTYHE |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,60%,100%,60%,60%,100%,100%,60%,100%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .25 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG |
| Warhead - Pronedamage | 50% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section 155MME, first property line 24835. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-160mm"></a>

## Yuri's Revenge - 160MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 160MM |
| Firing - base effect magnitude | 90 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 12 |
| Firing - minimum range setting | 0 |
| Firing - Speed | 10 |
| Firing - Projectile | Ballistic |
| Firing - Warhead | SCHOPWH |
| Projectile record | Ballistic |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SCHOPWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,60%,80%,50%,50%,100%,100%,60%,100%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .25 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG |
| Warhead - Pronedamage | 50% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section 160MM, first property line 23467. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-160mme"></a>

## Yuri's Revenge - 160MME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 160MME |
| Firing - base effect magnitude | 90 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 12 |
| Firing - minimum range setting | 0 |
| Firing - Burst | 2 |
| Firing - Speed | 10 |
| Firing - Projectile | Ballistic |
| Firing - Warhead | SCHOPWH |
| Projectile record | Ballistic |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SCHOPWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,60%,80%,50%,50%,100%,100%,60%,100%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .25 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG |
| Warhead - Pronedamage | 50% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section 160MME, first property line 24849. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-20mm"></a>

## Yuri's Revenge - 20MM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 20MM |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible3 |
| Firing - Warhead | SSA |
| Projectile record | Invisible3 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 80% |

Source: expandmd01.mix/rulesmd.ini, section 20MM, first property line 22977. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-20mme"></a>

## Yuri's Revenge - 20MME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 20MME |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 5 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible3 |
| Firing - Warhead | SSA |
| Projectile record | Invisible3 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 80% |

Source: expandmd01.mix/rulesmd.ini, section 20MME, first property line 24825. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-20mmrapid"></a>

## Yuri's Revenge - 20MMRAPID

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 20MMRAPID |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 5.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HARVWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HARVWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,20%,20%,20%,15%,10%,400%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section 20MMRAPID, first property line 22967. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-20mmrapide"></a>

## Yuri's Revenge - 20MMRAPIDE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | 20MMRAPIDE |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 5.75 |
| Firing - Speed | 40 |
| Firing - Projectile | Cannon |
| Firing - Warhead | HowitzerWH |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HowitzerWH |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,60%,40%,40%,50%,40%,25%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section 20MMRAPIDE, first property line 25200. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aagattcann"></a>

## Yuri's Revenge - AAGATTCANN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AAGATTCANN |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 16 |
| Firing - maximum range setting | 12 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible4 |
| Firing - Warhead | GattWH |
| Projectile record | Invisible4 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AAGATTCANN, first property line 22762. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aagattcann2"></a>

## Yuri's Revenge - AAGATTCANN2

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AAGATTCANN2 |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 8 |
| Firing - maximum range setting | 12 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible4 |
| Firing - Warhead | GattWH |
| Projectile record | Invisible4 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AAGATTCANN2, first property line 22775. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aagattcann3"></a>

## Yuri's Revenge - AAGATTCANN3

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AAGATTCANN3 |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 4 |
| Firing - maximum range setting | 12 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible4 |
| Firing - Warhead | GattWH |
| Projectile record | Invisible4 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AAGATTCANN3, first property line 22788. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aagattling"></a>

## Yuri's Revenge - AAGATTLING

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AAGATTLING |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 16 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible4 |
| Firing - Warhead | GattWH |
| Projectile record | Invisible4 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AAGATTLING, first property line 22696. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aagattling2"></a>

## Yuri's Revenge - AAGATTLING2

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AAGATTLING2 |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 8 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible4 |
| Firing - Warhead | GattWH |
| Projectile record | Invisible4 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AAGATTLING2, first property line 22722. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aagattling2e"></a>

## Yuri's Revenge - AAGATTLING2E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AAGATTLING2E |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 8 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible4 |
| Firing - Warhead | GattWH |
| Projectile record | Invisible4 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AAGATTLING2E, first property line 24641. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aagattling3"></a>

## Yuri's Revenge - AAGATTLING3

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AAGATTLING3 |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 4 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible4 |
| Firing - Warhead | GattWH |
| Projectile record | Invisible4 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AAGATTLING3, first property line 22748. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aagattling3e"></a>

## Yuri's Revenge - AAGATTLING3E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AAGATTLING3E |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 4 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible4 |
| Firing - Warhead | GattWH |
| Projectile record | Invisible4 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AAGATTLING3E, first property line 24667. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aagattlinge"></a>

## Yuri's Revenge - AAGATTLINGE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AAGATTLINGE |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 16 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible4 |
| Firing - Warhead | GattWH |
| Projectile record | Invisible4 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AAGATTLINGE, first property line 24615. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aggattling"></a>

## Yuri's Revenge - AGGATTLING

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AGGATTLING |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 16 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisiblelow |
| Firing - Warhead | GattWH |
| Projectile record | Invisiblelow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AGGATTLING, first property line 22683. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aggattling2"></a>

## Yuri's Revenge - AGGATTLING2

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AGGATTLING2 |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 16 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisiblelow |
| Firing - Warhead | SA |
| Projectile record | Invisiblelow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AGGATTLING2, first property line 22709. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aggattling2e"></a>

## Yuri's Revenge - AGGATTLING2E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AGGATTLING2E |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 16 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisiblelow |
| Firing - Warhead | SA |
| Projectile record | Invisiblelow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AGGATTLING2E, first property line 24628. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aggattling3"></a>

## Yuri's Revenge - AGGATTLING3

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AGGATTLING3 |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 16 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisiblelow |
| Firing - Warhead | SSA |
| Projectile record | Invisiblelow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 80% |

Source: expandmd01.mix/rulesmd.ini, section AGGATTLING3, first property line 22735. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aggattling3e"></a>

## Yuri's Revenge - AGGATTLING3E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AGGATTLING3E |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 16 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisiblelow |
| Firing - Warhead | SSA |
| Projectile record | Invisiblelow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 80% |

Source: expandmd01.mix/rulesmd.ini, section AGGATTLING3E, first property line 24654. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aggattlinge"></a>

## Yuri's Revenge - AGGATTLINGE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AGGATTLINGE |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 16 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisiblelow |
| Firing - Warhead | GattWH |
| Projectile record | Invisiblelow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | GattWH |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,70%,50%,30%,10%,10%,5%,3%,200%,50% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AGGATTLINGE, first property line 24602. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-akm"></a>

## Yuri's Revenge - AKM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AKM |
| Firing - base effect magnitude | 65 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | BORISWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | BORISWH |
| Warhead - armor effectiveness, ordered percentages | 200%,200%,100%,50%,50%,50%,1%,1%,1%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AKM, first property line 23006. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-akme"></a>

## Yuri's Revenge - AKME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AKME |
| Firing - base effect magnitude | 90 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 9 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | BORISWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | BORISWH |
| Warhead - armor effectiveness, ordered percentages | 200%,200%,100%,50%,50%,50%,1%,1%,1%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section AKME, first property line 25246. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-alligatorbite"></a>

## Yuri's Revenge - ALLIGATORBITE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ALLIGATORBITE |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section ALLIGATORBITE, first property line 23560. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-assaultbolt"></a>

## Yuri's Revenge - ASSAULTBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ASSAULTBOLT |
| Firing - base effect magnitude | 10 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 1.83 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | ElectricAssault |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ElectricAssault |
| Warhead - armor effectiveness, ordered percentages | 0%,0,0%,0%,0%,0%,100%,100%,100%,50%,100% |
| Warhead - Infdeath | 5 |

Source: expandmd01.mix/rulesmd.ini, section ASSAULTBOLT, first property line 23880. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aswbomb"></a>

## Yuri's Revenge - ASWBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ASWBOMB |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 3 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 30 |
| Firing - Projectile | DepthCharge |
| Firing - Warhead | APSplash |
| Projectile record | DepthCharge |
| Projectile - Arm | 2 |
| Projectile - Rot | 1 |
| Warhead record | APSplash |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,65%,60%,25%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .8 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section ASWBOMB, first property line 23220. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aswcollision"></a>

## Yuri's Revenge - ASWCOLLISION

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ASWCOLLISION |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 30 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | AP |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,15%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section ASWCOLLISION, first property line 23256. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-aswlauncher"></a>

## Yuri's Revenge - ASWLAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ASWLAUNCHER |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 150 |
| Firing - maximum range setting | -2 |
| Firing - Speed | 10 |
| Firing - Projectile | ASWVirt |
| Firing - Warhead | Special |
| Firing - Omnifire | yes |
| Firing - Spawner | yes |
| Projectile record | ASWVirt |
| Projectile - air targeting | no |
| Projectile - ground targeting | no |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | Special |

Source: expandmd01.mix/rulesmd.ini, section ASWLAUNCHER, first property line 23667. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-atgun"></a>

## Yuri's Revenge - ATGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ATGUN |
| Firing - base effect magnitude | 65 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 60 |
| Firing - Projectile | Cannon |
| Firing - Warhead | AP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,15%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section ATGUN, first property line 23375. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-atgune"></a>

## Yuri's Revenge - ATGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ATGUNE |
| Firing - base effect magnitude | 65 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 5 |
| Firing - Burst | 2 |
| Firing - Speed | 60 |
| Firing - Projectile | Cannon |
| Firing - Warhead | RHINAPE |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RHINAPE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | VTEXPLOD |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section ATGUNE, first property line 25176. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-awp"></a>

## Yuri's Revenge - AWP

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AWP |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 150 |
| Firing - maximum range setting | 14 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section AWP, first property line 23077. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-awpe"></a>

## Yuri's Revenge - AWPE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | AWPE |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 14 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section AWPE, first property line 25147. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-badteeth"></a>

## Yuri's Revenge - BADTEETH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BADTEETH |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 30 |
| Firing - Projectile | DOGJUMP |
| Firing - Warhead | ParasiteDog |
| Firing - Fireintransport | no |
| Projectile record | DOGJUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | ParasiteDog |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,0%,0% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: expandmd01.mix/rulesmd.ini, section BADTEETH, first property line 23535. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-barrelexplosion"></a>

## Yuri's Revenge - BARRELEXPLOSION

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BARRELEXPLOSION |
| Firing - base effect magnitude | 200 |
| Firing - Projectile | Invisible |
| Firing - Warhead | OilExplosionWH |
| Projectile record | Invisible |
| Warhead record | OilExplosionWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,100%,90%,70%,50%,200%,200%,200%,100%,100% |
| Warhead - area spread | 4 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 4 |

Source: expandmd01.mix/rulesmd.ini, section BARRELEXPLOSION, first property line 22365. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-bearbite"></a>

## Yuri's Revenge - BEARBITE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BEARBITE |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section BEARBITE, first property line 23570. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-blackhawkcannon"></a>

## Yuri's Revenge - BLACKHAWKCANNON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BLACKHAWKCANNON |
| Firing - base effect magnitude | 35 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | QuadShell |
| Firing - Warhead | SA |
| Firing - Omnifire | yes |
| Projectile record | QuadShell |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section BLACKHAWKCANNON, first property line 23121. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-blackhawkcannone"></a>

## Yuri's Revenge - BLACKHAWKCANNONE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BLACKHAWKCANNONE |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | QuadShell |
| Firing - Warhead | SSA |
| Firing - Omnifire | yes |
| Projectile record | QuadShell |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 80% |

Source: expandmd01.mix/rulesmd.ini, section BLACKHAWKCANNONE, first property line 25042. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-blimpbomb"></a>

## Yuri's Revenge - BLIMPBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BLIMPBOMB |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Burst | 1 |
| Firing - Speed | 20 |
| Firing - Projectile | BlimpBombP |
| Firing - Warhead | BlimpHE |
| Firing - Omnifire | yes |
| Projectile record | BlimpBombP |
| Projectile - Arm | 10 |
| Warhead record | BlimpHE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,35%,35%,85%,75%,50%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section BLIMPBOMB, first property line 22413. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-blimpbombe"></a>

## Yuri's Revenge - BLIMPBOMBE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BLIMPBOMBE |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Burst | 1 |
| Firing - Speed | 20 |
| Firing - Projectile | BlimpBombP |
| Firing - Warhead | KTSTLEXP |
| Firing - Omnifire | yes |
| Projectile record | BlimpBombP |
| Projectile - Arm | 10 |
| Warhead record | KTSTLEXP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,35%,35%,85%,75%,50%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | KTSTLEXP |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section BLIMPBOMBE, first property line 24941. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-blimpbombeffect"></a>

## Yuri's Revenge - BLIMPBOMBEFFECT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BLIMPBOMBEFFECT |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Burst | 1 |
| Firing - Speed | 20 |
| Firing - Projectile | BlimpBombP |
| Firing - Warhead | BlimpHEEffect |
| Firing - Omnifire | yes |
| Projectile record | BlimpBombP |
| Projectile - Arm | 10 |
| Warhead record | BlimpHEEffect |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,35%,35%,85%,75%,50%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | EXPLOMED |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section BLIMPBOMBEFFECT, first property line 22425. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-boomertorpedo"></a>

## Yuri's Revenge - BOOMERTORPEDO

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BOOMERTORPEDO |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 7 |
| Firing - Burst | 2 |
| Firing - Speed | 25 |
| Firing - Projectile | Torpedo |
| Firing - Warhead | APSplash2 |
| Projectile record | Torpedo |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 12 |
| Warhead record | APSplash2 |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,100%,100%,65%,65%,60%,25%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .8 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section BOOMERTORPEDO, first property line 22525. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-boomertorpedoe"></a>

## Yuri's Revenge - BOOMERTORPEDOE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | BOOMERTORPEDOE |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 7 |
| Firing - Burst | 4 |
| Firing - Speed | 18 |
| Firing - Projectile | Torpedo |
| Firing - Warhead | APSplash2 |
| Projectile record | Torpedo |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 12 |
| Warhead record | APSplash2 |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,100%,100%,65%,65%,60%,25%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .8 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section BOOMERTORPEDOE, first property line 25086. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-chaosattack"></a>

## Yuri's Revenge - CHAOSATTACK

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CHAOSATTACK |
| Firing - base effect magnitude | 600 |
| Firing - reload interval | 45 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 30 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | PsychGasCreate |
| Firing - Omnifire | yes |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | PsychGasCreate |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,50%,50%,50%,0%,0%,0%,100%,100% |
| Warhead - area spread | 3 |
| Warhead - Percentatmax | 1 |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | CDGAS |

Source: expandmd01.mix/rulesmd.ini, section CHAOSATTACK, first property line 23507. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-chimpbite"></a>

## Yuri's Revenge - CHIMPBITE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CHIMPBITE |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section CHIMPBITE, first property line 23580. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-chronomp5"></a>

## Yuri's Revenge - CHRONOMP5

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CHRONOMP5 |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPointNoBuilding |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPointNoBuilding |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,75%,1%,1%,1%,0%,0%,0%,75%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section CHRONOMP5, first property line 23057. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-chronomp5e"></a>

## Yuri's Revenge - CHRONOMP5E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CHRONOMP5E |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPointNoBuilding |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPointNoBuilding |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,75%,1%,1%,1%,0%,0%,0%,75%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section CHRONOMP5E, first property line 25167. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-clintgun"></a>

## Yuri's Revenge - CLINTGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CLINTGUN |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section CLINTGUN, first property line 23046. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-coilbolt"></a>

## Yuri's Revenge - COILBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | COILBOLT |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible |
| Firing - Warhead | Electric |
| Projectile record | Invisible |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: expandmd01.mix/rulesmd.ini, section COILBOLT, first property line 23892. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-comet"></a>

## Yuri's Revenge - COMET

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | COMET |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 10 |
| Firing - Speed | 40 |
| Firing - Projectile | LargeCometP |
| Firing - Warhead | CometWH |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | LargeCometP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | CometFragment |
| Warhead record | CometWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,50%,50%,200%,200%,200%,100%,100% |
| Warhead - Wall | no |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |

Source: expandmd01.mix/rulesmd.ini, section COMET, first property line 24289. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-cometfragment"></a>

## Yuri's Revenge - COMETFRAGMENT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | COMETFRAGMENT |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 10 |
| Firing - Projectile | SmallCometP |
| Firing - Warhead | CometWH |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | SmallCometP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | CometWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,50%,50%,200%,200%,200%,100%,100% |
| Warhead - Wall | no |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |

Source: expandmd01.mix/rulesmd.ini, section COMETFRAGMENT, first property line 24307. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-cowshot"></a>

## Yuri's Revenge - COWSHOT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | COWSHOT |
| Firing - base effect magnitude | 300 |
| Firing - reload interval | 75 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | PrismWarhead |
| Firing - Islaser | true |
| Firing - Isbiglaser | true |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | PrismWarhead |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,100%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Infdeath | 5 |

Source: expandmd01.mix/rulesmd.ini, section COWSHOT, first property line 24561. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crelectricbolt"></a>

## Yuri's Revenge - CRELECTRICBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRELECTRICBOLT |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 45 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Shock |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Shock |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: expandmd01.mix/rulesmd.ini, section CRELECTRICBOLT, first property line 24378. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crflakguygun"></a>

## Yuri's Revenge - CRFLAKGUYGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRFLAKGUYGUN |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,125%,100%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | 1.0 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: expandmd01.mix/rulesmd.ini, section CRFLAKGUYGUN, first property line 24586. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crm60"></a>

## Yuri's Revenge - CRM60

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRM60 |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SSA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 80% |

Source: expandmd01.mix/rulesmd.ini, section CRM60, first property line 24367. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crmindcontrol"></a>

## Yuri's Revenge - CRMINDCONTROL

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRMINDCONTROL |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 1 |
| Firing - Projectile | Psychic |
| Firing - Warhead | PsiPulse |
| Projectile record | Psychic |
| Warhead record | PsiPulse |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,0%,0% |
| Warhead - area spread | 3 |
| Warhead - Percentatmax | .85 |
| Warhead - Psychicdamage | yes |
| Warhead - Infdeath | 6 |
| Warhead - Affectsallies | no |

Source: expandmd01.mix/rulesmd.ini, section CRMINDCONTROL, first property line 24537. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crmissilelauncher"></a>

## Yuri's Revenge - CRMISSILELAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRMISSILELAUNCHER |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 8 |
| Firing - minimum range setting | 1 |
| Firing - Burst | 2 |
| Firing - Speed | 30 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | GUARDWH |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | GUARDWH |
| Warhead - armor effectiveness, ordered percentages | 20%,20%,20%,100%,50%,100%,10%,10%,10%,100%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section CRMISSILELAUNCHER, first property line 24496. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crmp5"></a>

## Yuri's Revenge - CRMP5

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRMP5 |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint3 |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint3 |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,2%,2%,2%,2%,2%,2%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section CRMP5, first property line 24399. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crneutronrifle"></a>

## Yuri's Revenge - CRNEUTRONRIFLE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRNEUTRONRIFLE |
| Firing - base effect magnitude | 5 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | ChronoBeam |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ChronoBeam |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,0% |
| Warhead - Temporal | yes |

Source: expandmd01.mix/rulesmd.ini, section CRNEUTRONRIFLE, first property line 24423. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crnuke"></a>

## Yuri's Revenge - CRNUKE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRNUKE |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 35 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | CRNUKEWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | CRNUKEWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,90%,50%,50%,60%,150%,20%,100%,100% |
| Warhead - area spread | 5 |
| Warhead - Percentatmax | .25 |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | MININUKE - added 11/30 |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section CRNUKE, first property line 24444. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crpsychicjab"></a>

## Yuri's Revenge - CRPSYCHICJAB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRPSYCHICJAB |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 6.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SAFlame |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SAFlame |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | INITFIRE |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section CRPSYCHICJAB, first property line 24464. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crradbeamweapon"></a>

## Yuri's Revenge - CRRADBEAMWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRRADBEAMWEAPON |
| Firing - base effect magnitude | 175 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | RadBeamWarhead |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RadBeamWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,20%,15%,10%,0%,0%,0%,100%,100% |
| Warhead - Radiation | yes |
| Warhead - Infdeath | 7 |

Source: expandmd01.mix/rulesmd.ini, section CRRADBEAMWEAPON, first property line 24519. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crsupermindblast"></a>

## Yuri's Revenge - CRSUPERMINDBLAST

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRSUPERMINDBLAST |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 1 |
| Firing - Projectile | Psychic |
| Firing - Warhead | SuperPsiPulse |
| Projectile record | Psychic |
| Warhead record | SuperPsiPulse |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,50%,50%,50%,0%,0%,0%,0%,0% |
| Warhead - area spread | 5 |
| Warhead - Percentatmax | .85 |
| Warhead - Psychicdamage | yes |
| Warhead - Infdeath | 6 |
| Warhead - Affectsallies | no |

Source: expandmd01.mix/rulesmd.ini, section CRSUPERMINDBLAST, first property line 24483. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crterrorbomb"></a>

## Yuri's Revenge - CRTERRORBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRTERRORBOMB |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible |
| Firing - Warhead | TerrorBombWH |
| Projectile record | Invisible |
| Warhead record | TerrorBombWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,100%,90%,50%,50%,100%,150%,30%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .5 |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | MININUKE |

Source: expandmd01.mix/rulesmd.ini, section CRTERRORBOMB, first property line 24455. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-cruiselauncher"></a>

## Yuri's Revenge - CRUISELAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRUISELAUNCHER |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 20 |
| Firing - minimum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 15 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | Special |
| Firing - Omnifire | yes |
| Firing - Spawner | yes |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Special |

Source: expandmd01.mix/rulesmd.ini, section CRUISELAUNCHER, first property line 22594. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-crvirusgun"></a>

## Yuri's Revenge - CRVIRUSGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | CRVIRUSGUN |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Virus |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Virus |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 8 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section CRVIRUSGUN, first property line 24473. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-defaultdeathweapon"></a>

## Yuri's Revenge - DEFAULTDEATHWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DEFAULTDEATHWEAPON |
| Firing - Projectile | Invisible |
| Firing - Warhead | DeathWH |
| Projectile record | Invisible |
| Warhead record | DeathWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - area spread | 1.5 |
| Warhead - Percentatmax | .5 |
| Warhead - Infdeath | 3 |

Source: expandmd01.mix/rulesmd.ini, section DEFAULTDEATHWEAPON, first property line 22355. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-defusekit"></a>

## Yuri's Revenge - DEFUSEKIT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DEFUSEKIT |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | BombDisarm |
| Firing - Fireintransport | no |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | BombDisarm |

Source: expandmd01.mix/rulesmd.ini, section DEFUSEKIT, first property line 24006. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-demobomb"></a>

## Yuri's Revenge - DEMOBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DEMOBOMB |
| Firing - base effect magnitude | 300 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 35 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | DemobombWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | DemobombWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,50%,50%,80%,150%,10%,100%,100% |
| Warhead - area spread | 8 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | DEMTEXP |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section DEMOBOMB, first property line 24507. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-diskdrain"></a>

## Yuri's Revenge - DISKDRAIN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DISKDRAIN |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Burst | 1 |
| Firing - Speed | 20 |
| Firing - Projectile | InvisibleVertical |
| Firing - Warhead | AntiB |
| Firing - Omnifire | yes |
| Projectile record | InvisibleVertical |
| Warhead record | AntiB |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,0%,0%,0%,100%,100%,100%,0%,0% |

Source: expandmd01.mix/rulesmd.ini, section DISKDRAIN, first property line 24274. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-disklaser"></a>

## Yuri's Revenge - DISKLASER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DISKLASER |
| Firing - base effect magnitude | 90 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 40 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | DiskWH |
| Firing - Omnifire | yes |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | DiskWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,50%,50%,50%,100%,100%,100%,100%,100% |
| Warhead - Wall | no |
| Warhead - Infdeath | 7 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Penetratesbunker | yes |

Source: expandmd01.mix/rulesmd.ini, section DISKLASER, first property line 24256. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-disklasere"></a>

## Yuri's Revenge - DISKLASERE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DISKLASERE |
| Firing - base effect magnitude | 90 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 40 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | DiskWH |
| Firing - Omnifire | yes |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | DiskWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,50%,50%,50%,100%,100%,100%,100%,100% |
| Warhead - Wall | no |
| Warhead - Infdeath | 7 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Penetratesbunker | yes |

Source: expandmd01.mix/rulesmd.ini, section DISKLASERE, first property line 24755. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-doublepistols"></a>

## Yuri's Revenge - DOUBLEPISTOLS

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DOUBLEPISTOLS |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 5 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint2 |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint2 |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section DOUBLEPISTOLS, first property line 22996. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-doublepistolse"></a>

## Yuri's Revenge - DOUBLEPISTOLSE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DOUBLEPISTOLSE |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint2 |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint2 |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section DOUBLEPISTOLSE, first property line 25236. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-dredlauncher"></a>

## Yuri's Revenge - DREDLAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DREDLAUNCHER |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 25 |
| Firing - minimum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 15 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | Special |
| Firing - Omnifire | yes |
| Firing - Spawner | yes |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Special |

Source: expandmd01.mix/rulesmd.ini, section DREDLAUNCHER, first property line 23493. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-dronejump"></a>

## Yuri's Revenge - DRONEJUMP

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | DRONEJUMP |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 1.83 |
| Firing - Speed | 30 |
| Firing - Projectile | JUMP |
| Firing - Warhead | Parasite |
| Firing - Fireintransport | no |
| Projectile record | JUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | Parasite |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,0%,0% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: expandmd01.mix/rulesmd.ini, section DRONEJUMP, first property line 23521. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-eiffelbolt"></a>

## Yuri's Revenge - EIFFELBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | EIFFELBOLT |
| Firing - base effect magnitude | 2000 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 20 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | Electric |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: expandmd01.mix/rulesmd.ini, section EIFFELBOLT, first property line 23917. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-electricbolt"></a>

## Yuri's Revenge - ELECTRICBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ELECTRICBOLT |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Shock |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Shock |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: expandmd01.mix/rulesmd.ini, section ELECTRICBOLT, first property line 23857. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-electricbolte"></a>

## Yuri's Revenge - ELECTRICBOLTE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ELECTRICBOLTE |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | Electricbounce |
| Firing - Warhead | Shock |
| Projectile record | Electricbounce |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | TeslaFragment |
| Warhead record | Shock |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: expandmd01.mix/rulesmd.ini, section ELECTRICBOLTE, first property line 24873. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-fakec4"></a>

## Yuri's Revenge - FAKEC4

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FAKEC4 |
| Firing - base effect magnitude | 5000 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | FakeC4WH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FakeC4WH |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,0%,0%,0%,100%,100%,100%,0%,100% |
| Warhead - area spread | 0 |

Source: expandmd01.mix/rulesmd.ini, section FAKEC4, first property line 23066. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flakguyaagun"></a>

## Yuri's Revenge - FLAKGUYAAGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKGUYAAGUN |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakGuyWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakGuyWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,50%,80%,80%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .2 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKGUYAAGUN, first property line 24211. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flakguyaagune"></a>

## Yuri's Revenge - FLAKGUYAAGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKGUYAAGUNE |
| Firing - base effect magnitude | 8 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakGuyWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakGuyWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,50%,80%,80%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .2 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKGUYAAGUNE, first property line 24744. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flakguygun"></a>

## Yuri's Revenge - FLAKGUYGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKGUYGUN |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,125%,100%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | 1.0 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKGUYGUN, first property line 24231. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flakguygune"></a>

## Yuri's Revenge - FLAKGUYGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKGUYGUNE |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 5 |
| Firing - Burst | 2 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,125%,100%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | 1.0 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKGUYGUNE, first property line 24733. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flaktrackaagun"></a>

## Yuri's Revenge - FLAKTRACKAAGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKTRACKAAGUN |
| Firing - base effect magnitude | 35 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 10 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakWH |
| Warhead - armor effectiveness, ordered percentages | 150%,80%,50%,100%,100%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKTRACKAAGUN, first property line 24201. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flaktrackaagune"></a>

## Yuri's Revenge - FLAKTRACKAAGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKTRACKAAGUNE |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakWH |
| Warhead - armor effectiveness, ordered percentages | 150%,80%,50%,100%,100%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKTRACKAAGUNE, first property line 24711. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flaktrackgun"></a>

## Yuri's Revenge - FLAKTRACKGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKTRACKGUN |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,125%,100%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | 1.0 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKTRACKGUN, first property line 24221. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flaktrackgune"></a>

## Yuri's Revenge - FLAKTRACKGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKTRACKGUNE |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 5 |
| Firing - Burst | 2 |
| Firing - Speed | 50 |
| Firing - Projectile | FlakTProj |
| Firing - Warhead | FlakTWH |
| Projectile record | FlakTProj |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakTWH |
| Warhead - armor effectiveness, ordered percentages | 150%,125%,100%,60%,10%,10%,30%,20%,10%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | 1.0 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | HTRKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKTRACKGUNE, first property line 24722. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flakweapon"></a>

## Yuri's Revenge - FLAKWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKWEAPON |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakWH |
| Warhead - armor effectiveness, ordered percentages | 150%,80%,50%,100%,100%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKWEAPON, first property line 24191. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flakweapone"></a>

## Yuri's Revenge - FLAKWEAPONE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLAKWEAPONE |
| Firing - base effect magnitude | 35 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 10 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | FlakProj |
| Firing - Warhead | FlakWH |
| Projectile record | FlakProj |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Inaccurate | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | FlakWH |
| Warhead - armor effectiveness, ordered percentages | 150%,80%,50%,100%,100%,20%,0%,0%,0%,100%,100% |
| Warhead - area spread | 1.0 |
| Warhead - Percentatmax | .1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | SMKPUFF |

Source: expandmd01.mix/rulesmd.ini, section FLAKWEAPONE, first property line 24700. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-flare"></a>

## Yuri's Revenge - FLARE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | FLARE |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 12 |
| Firing - Projectile | Invisible |
| Firing - Warhead | AirstrikeFlare |
| Firing - Ishousecolor | true |
| Projectile record | Invisible |
| Warhead record | AirstrikeFlare |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,0%,0%,0%,1%,1%,1%,0%,0% |

Source: expandmd01.mix/rulesmd.ini, section FLARE, first property line 23279. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-goodteeth"></a>

## Yuri's Revenge - GOODTEETH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | GOODTEETH |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 30 |
| Firing - Projectile | ADOGJUMP |
| Firing - Warhead | ParasiteDog |
| Firing - Fireintransport | no |
| Projectile record | ADOGJUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | ParasiteDog |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,0%,0% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: expandmd01.mix/rulesmd.ini, section GOODTEETH, first property line 23548. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-grandcannonweapon"></a>

## Yuri's Revenge - GRANDCANNONWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | GRANDCANNONWEAPON |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 15 |
| Firing - minimum range setting | 3 |
| Firing - Speed | 1 |
| Firing - Projectile | GrandCannonBall |
| Firing - Warhead | GrandCannonWH |
| Projectile record | GrandCannonBall |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | GrandCannonWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,50%,100%,50%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .2 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 30% |

Source: expandmd01.mix/rulesmd.ini, section GRANDCANNONWEAPON, first property line 24179. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-hornetbomb"></a>

## Yuri's Revenge - HORNETBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HORNETBOMB |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 3 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 30 |
| Firing - Projectile | NormalBomb |
| Firing - Warhead | ORCAAP |
| Projectile record | NormalBomb |
| Projectile - Arm | 2 |
| Projectile - Rot | 1 |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |
| Warhead - Penetratesbunker | yes |

Source: expandmd01.mix/rulesmd.ini, section HORNETBOMB, first property line 23211. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-hornetbombe"></a>

## Yuri's Revenge - HORNETBOMBE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HORNETBOMBE |
| Firing - base effect magnitude | 80 |
| Firing - reload interval | 3 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 30 |
| Firing - Projectile | NormalBomb |
| Firing - Warhead | ARTYHE |
| Projectile record | NormalBomb |
| Projectile - Arm | 2 |
| Projectile - Rot | 1 |
| Warhead record | ARTYHE |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,60%,100%,60%,60%,100%,100%,60%,100%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .25 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG |
| Warhead - Pronedamage | 50% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section HORNETBOMBE, first property line 25032. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-hornetcollision"></a>

## Yuri's Revenge - HORNETCOLLISION

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HORNETCOLLISION |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 30 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | AP |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,15%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section HORNETCOLLISION, first property line 23235. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-hornetlauncher"></a>

## Yuri's Revenge - HORNETLAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HORNETLAUNCHER |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 150 |
| Firing - maximum range setting | 25 |
| Firing - Speed | 10 |
| Firing - Projectile | Invisible |
| Firing - Warhead | Special |
| Firing - Omnifire | yes |
| Firing - Spawner | yes |
| Projectile record | Invisible |
| Warhead record | Special |

Source: expandmd01.mix/rulesmd.ini, section HORNETLAUNCHER, first property line 23655. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-hovermissile"></a>

## Yuri's Revenge - HOVERMISSILE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HOVERMISSILE |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 6 |
| Firing - minimum range setting | 1 |
| Firing - Burst | 2 |
| Firing - Speed | 40 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | HE |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,70%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section HOVERMISSILE, first property line 22558. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-hovermissilee"></a>

## Yuri's Revenge - HOVERMISSILEE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HOVERMISSILEE |
| Firing - base effect magnitude | 80 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 6 |
| Firing - minimum range setting | 1 |
| Firing - Burst | 4 |
| Firing - Speed | 40 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | HE |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,70%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section HOVERMISSILEE, first property line 25113. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-howitzergun"></a>

## Yuri's Revenge - HOWITZERGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | HOWITZERGUN |
| Firing - base effect magnitude | 75 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 12 |
| Firing - minimum range setting | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Ballistic |
| Firing - Warhead | HowitzerWH |
| Projectile record | Ballistic |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HowitzerWH |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,60%,40%,40%,50%,40%,25%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section HOWITZERGUN, first property line 23410. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-ivanbomber"></a>

## Yuri's Revenge - IVANBOMBER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | IVANBOMBER |
| Firing - base effect magnitude | 400 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible |
| Firing - Warhead | IvanBomb |
| Firing - Fireintransport | no |
| Projectile record | Invisible |
| Warhead record | IvanBomb |
| Warhead - Ivanbomb | yes |

Source: expandmd01.mix/rulesmd.ini, section IVANBOMBER, first property line 24111. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-ivanbombere"></a>

## Yuri's Revenge - IVANBOMBERE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | IVANBOMBERE |
| Firing - base effect magnitude | 600 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible |
| Firing - Warhead | IvanBomb |
| Firing - Fireintransport | no |
| Projectile record | Invisible |
| Warhead record | IvanBomb |
| Warhead - Ivanbomb | yes |

Source: expandmd01.mix/rulesmd.ini, section IVANBOMBERE, first property line 25053. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-lunarlaser"></a>

## Yuri's Revenge - LUNARLASER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | LUNARLASER |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 40 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | LUNARWH |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | LUNARWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,50%,50%,100%,100%,100%,100%,100% |
| Warhead - Wall | no |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |

Source: expandmd01.mix/rulesmd.ini, section LUNARLASER, first property line 24242. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-m1carbine"></a>

## Yuri's Revenge - M1CARBINE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | M1CARBINE |
| Firing - base effect magnitude | 15 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Firing - Occupantanim | UCCONS |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section M1CARBINE, first property line 22861. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-m1carbinee"></a>

## Yuri's Revenge - M1CARBINEE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | M1CARBINEE |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 25 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Firing - Occupantanim | UCCONS |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section M1CARBINEE, first property line 24679. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-m60"></a>

## Yuri's Revenge - M60

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | M60 |
| Firing - base effect magnitude | 15 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Firing - Occupantanim | UCFLASH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section M60, first property line 22923. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-m60e"></a>

## Yuri's Revenge - M60E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | M60E |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Firing - Occupantanim | UCFLASH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section M60E, first property line 25282. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-magneshake"></a>

## Yuri's Revenge - MAGNESHAKE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAGNESHAKE |
| Firing - base effect magnitude | 80 |
| Firing - reload interval | 110 |
| Firing - maximum range setting | 10 |
| Firing - Speed | 40 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | MagneShakeWH |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | MagneShakeWH |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,0%,100%,0%,100%,100%,100%,0%,0% |

Source: expandmd01.mix/rulesmd.ini, section MAGNESHAKE, first property line 24347. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-magneticbeam"></a>

## Yuri's Revenge - MAGNETICBEAM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAGNETICBEAM |
| Firing - base effect magnitude | 5000 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 12 |
| Firing - minimum range setting | 3 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | LocomotorBeam |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | LocomotorBeam |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,100%,100%,100%,0%,0%,0%,100%,0% |

Source: expandmd01.mix/rulesmd.ini, section MAGNETICBEAM, first property line 24334. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-magneticbeame"></a>

## Yuri's Revenge - MAGNETICBEAME

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAGNETICBEAME |
| Firing - base effect magnitude | 10000 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 12 |
| Firing - minimum range setting | 3 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | LocomotorBeam |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | LocomotorBeam |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,100%,100%,100%,0%,0%,0%,100%,0% |

Source: expandmd01.mix/rulesmd.ini, section MAGNETICBEAME, first property line 24991. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-makeupkit"></a>

## Yuri's Revenge - MAKEUPKIT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAKEUPKIT |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | -2 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | Snapshot |
| Firing - Fireintransport | no |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | Snapshot |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,100%,100% |

Source: expandmd01.mix/rulesmd.ini, section MAKEUPKIT, first property line 24141. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-mammothtusk"></a>

## Yuri's Revenge - MAMMOTHTUSK

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAMMOTHTUSK |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 8 |
| Firing - Burst | 2 |
| Firing - Speed | 20 |
| Firing - Projectile | AAHeatSeeker |
| Firing - Warhead | HE |
| Projectile record | AAHeatSeeker |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 80 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,70%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section MAMMOTHTUSK, first property line 23442. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-maverick"></a>

## Yuri's Revenge - MAVERICK

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICK |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 1 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | ORCAAP |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |
| Warhead - Penetratesbunker | yes |

Source: expandmd01.mix/rulesmd.ini, section MAVERICK, first property line 23155. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-maverick2"></a>

## Yuri's Revenge - MAVERICK2

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICK2 |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 1 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | ORCAAP |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |
| Warhead - Penetratesbunker | yes |

Source: expandmd01.mix/rulesmd.ini, section MAVERICK2, first property line 23165. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-maverick2e"></a>

## Yuri's Revenge - MAVERICK2E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICK2E |
| Firing - base effect magnitude | 400 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 9 |
| Firing - Burst | 1 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | ORCAAP |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |
| Warhead - Penetratesbunker | yes |

Source: expandmd01.mix/rulesmd.ini, section MAVERICK2E, first property line 25012. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-maverick3"></a>

## Yuri's Revenge - MAVERICK3

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICK3 |
| Firing - base effect magnitude | 750 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 4 |
| Firing - Burst | 2 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | MIGWH |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | MIGWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,50%,100%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section MAVERICK3, first property line 23175. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-maverick3e"></a>

## Yuri's Revenge - MAVERICK3E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICK3E |
| Firing - base effect magnitude | 400 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 9 |
| Firing - Burst | 2 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | ORCAAP |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |
| Warhead - Penetratesbunker | yes |

Source: expandmd01.mix/rulesmd.ini, section MAVERICK3E, first property line 25022. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-mavericke"></a>

## Yuri's Revenge - MAVERICKE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAVERICKE |
| Firing - base effect magnitude | 300 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 9 |
| Firing - Burst | 1 |
| Firing - Speed | 70 |
| Firing - Projectile | AirToGroundMissile |
| Firing - Warhead | ORCAAP |
| Projectile record | AirToGroundMissile |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 100 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | ORCAAP |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,75%,100%,100% |
| Warhead - area spread | .4 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |
| Warhead - Penetratesbunker | yes |

Source: expandmd01.mix/rulesmd.ini, section MAVERICKE, first property line 25002. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-mayanprism"></a>

## Yuri's Revenge - MAYANPRISM

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MAYANPRISM |
| Firing - base effect magnitude | 1000 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 25 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | PrismWarhead |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | PrismWarhead |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,100%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Infdeath | 5 |

Source: expandmd01.mix/rulesmd.ini, section MAYANPRISM, first property line 23826. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-medusa"></a>

## Yuri's Revenge - MEDUSA

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MEDUSA |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 120 |
| Firing - Projectile | MedusaProjectile |
| Firing - Warhead | SAMWH |
| Firing - Omnifire | yes |
| Projectile record | MedusaProjectile |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Arm | 1 |
| Projectile - Rot | 20 |
| Projectile - High | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SAMWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | 1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section MEDUSA, first property line 22620. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-medusae"></a>

## Yuri's Revenge - MEDUSAE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MEDUSAE |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 5 |
| Firing - maximum range setting | 14 |
| Firing - Burst | 2 |
| Firing - Speed | 150 |
| Firing - Projectile | MedusaProjectile |
| Firing - Warhead | SAMWH |
| Firing - Omnifire | yes |
| Projectile record | MedusaProjectile |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Arm | 1 |
| Projectile - Rot | 20 |
| Projectile - High | yes |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SAMWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | 1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section MEDUSAE, first property line 25224. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-mindcontrol"></a>

## Yuri's Revenge - MINDCONTROL

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MINDCONTROL |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 200 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | PsychicControl |
| Firing - Warhead | Controller |
| Projectile record | PsychicControl |
| Warhead record | Controller |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - Mindcontrol | yes |
| Warhead - Animlist | YURICNTL |

Source: expandmd01.mix/rulesmd.ini, section MINDCONTROL, first property line 24041. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-mindcontrole"></a>

## Yuri's Revenge - MINDCONTROLE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MINDCONTROLE |
| Firing - base effect magnitude | 10 |
| Firing - reload interval | 200 |
| Firing - maximum range setting | 14 |
| Firing - Speed | 100 |
| Firing - Projectile | PsychicControl |
| Firing - Warhead | Controller |
| Projectile record | PsychicControl |
| Warhead record | Controller |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - Mindcontrol | yes |
| Warhead - Animlist | YURICNTL |

Source: expandmd01.mix/rulesmd.ini, section MINDCONTROLE, first property line 25211. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-miragegun"></a>

## Yuri's Revenge - MIRAGEGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MIRAGEGUN |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 70 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | MirageWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | MirageWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,80%,100%,100%,100%,30%,20%,20%,100%,100% |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | IRONFX |

Source: expandmd01.mix/rulesmd.ini, section MIRAGEGUN, first property line 24165. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-miragegune"></a>

## Yuri's Revenge - MIRAGEGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MIRAGEGUNE |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 9 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | MirageWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | MirageWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,80%,100%,100%,100%,30%,20%,20%,100%,100% |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | IRONFX |

Source: expandmd01.mix/rulesmd.ini, section MIRAGEGUNE, first property line 24928. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-missilelauncher"></a>

## Yuri's Revenge - MISSILELAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MISSILELAUNCHER |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 40 |
| Firing - maximum range setting | 8 |
| Firing - minimum range setting | 1 |
| Firing - Burst | 1 |
| Firing - Speed | 30 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | GUARDWH |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | GUARDWH |
| Warhead - armor effectiveness, ordered percentages | 20%,20%,20%,100%,50%,100%,10%,10%,10%,100%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section MISSILELAUNCHER, first property line 22570. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-missilelaunchere"></a>

## Yuri's Revenge - MISSILELAUNCHERE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MISSILELAUNCHERE |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 8 |
| Firing - minimum range setting | 1 |
| Firing - Burst | 1 |
| Firing - Speed | 40 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | GUARDWH |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | GUARDWH |
| Warhead - armor effectiveness, ordered percentages | 20%,20%,20%,100%,50%,100%,10%,10%,10%,100%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section MISSILELAUNCHERE, first property line 25124. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-mp5"></a>

## Yuri's Revenge - MP5

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MP5 |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section MP5, first property line 22986. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-mp5e"></a>

## Yuri's Revenge - MP5E

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MP5E |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section MP5E, first property line 25157. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-multiplemindcontroltank"></a>

## Yuri's Revenge - MULTIPLEMINDCONTROLTANK

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MULTIPLEMINDCONTROLTANK |
| Firing - base effect magnitude | 3 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | PsychicControl |
| Firing - Warhead | Controller |
| Firing - Omnifire | yes |
| Projectile record | PsychicControl |
| Warhead record | Controller |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - Mindcontrol | yes |
| Warhead - Animlist | YURICNTL |

Source: expandmd01.mix/rulesmd.ini, section MULTIPLEMINDCONTROLTANK, first property line 24063. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-multiplemindcontroltower"></a>

## Yuri's Revenge - MULTIPLEMINDCONTROLTOWER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MULTIPLEMINDCONTROLTOWER |
| Firing - base effect magnitude | 3 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | PsychicControl |
| Firing - Warhead | Controller |
| Projectile record | PsychicControl |
| Warhead record | Controller |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - Mindcontrol | yes |
| Warhead - Animlist | YURICNTL |

Source: expandmd01.mix/rulesmd.ini, section MULTIPLEMINDCONTROLTOWER, first property line 24076. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-mummypunch"></a>

## Yuri's Revenge - MUMMYPUNCH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MUMMYPUNCH |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 1.4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Battering |
| Firing - Fireintransport | no |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Battering |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,30%,30%,20%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 10 |

Source: expandmd01.mix/rulesmd.ini, section MUMMYPUNCH, first property line 23738. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-mummysmash"></a>

## Yuri's Revenge - MUMMYSMASH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | MUMMYSMASH |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 1.1 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Smashing |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Smashing |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,100%,20%,100%,0%,0%,0%,0%,0% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 10 |

Source: expandmd01.mix/rulesmd.ini, section MUMMYSMASH, first property line 23749. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-neutronrifle"></a>

## Yuri's Revenge - NEUTRONRIFLE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | NEUTRONRIFLE |
| Firing - base effect magnitude | 8 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleMedium |
| Firing - Warhead | ChronoBeam |
| Projectile record | InvisibleMedium |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ChronoBeam |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,0% |
| Warhead - Temporal | yes |

Source: expandmd01.mix/rulesmd.ini, section NEUTRONRIFLE, first property line 23759. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-neutronriflee"></a>

## Yuri's Revenge - NEUTRONRIFLEE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | NEUTRONRIFLEE |
| Firing - base effect magnitude | 16 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | ChronoBeam |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | ChronoBeam |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,0% |
| Warhead - Temporal | yes |

Source: expandmd01.mix/rulesmd.ini, section NEUTRONRIFLEE, first property line 24980. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-nukecarrier"></a>

## Yuri's Revenge - NUKECARRIER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | NUKECARRIER |
| Firing - Speed | 100 |
| Firing - Projectile | GiantNukeUp |
| Firing - Warhead | NukeMaker |
| Projectile record | GiantNukeUp |
| Projectile - Arm | 2 |
| Warhead record | NukeMaker |

Source: expandmd01.mix/rulesmd.ini, section NUKECARRIER, first property line 24027. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-nukepayload"></a>

## Yuri's Revenge - NUKEPAYLOAD

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | NUKEPAYLOAD |
| Firing - base effect magnitude | 600 |
| Firing - maximum range setting | 30 |
| Firing - Speed | 10 |
| Firing - Projectile | GiantNukeDown |
| Firing - Warhead | NUKE |
| Projectile record | GiantNukeDown |
| Projectile - Arm | 2 |
| Warhead record | NUKE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,200%,100%,100%,60%,100%,8%,100%,100% |
| Warhead - area spread | 10 |
| Warhead - Percentatmax | .02 |
| Warhead - Wood | yes |
| Warhead - Infdeath | 7 |
| Warhead - Animlist | NUKEANIM |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section NUKEPAYLOAD, first property line 24018. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-oilexplosion"></a>

## Yuri's Revenge - OILEXPLOSION

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | OILEXPLOSION |
| Firing - base effect magnitude | 600 |
| Firing - Projectile | Invisible |
| Firing - Warhead | OilExplosionWH |
| Projectile record | Invisible |
| Warhead record | OilExplosionWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,100%,90%,70%,50%,200%,200%,200%,100%,100% |
| Warhead - area spread | 4 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 4 |

Source: expandmd01.mix/rulesmd.ini, section OILEXPLOSION, first property line 22359. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-opcoilbolt"></a>

## Yuri's Revenge - OPCOILBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | OPCOILBOLT |
| Firing - base effect magnitude | 300 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | Electric |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: expandmd01.mix/rulesmd.ini, section OPCOILBOLT, first property line 23905. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-para"></a>

## Yuri's Revenge - PARA

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PARA |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SSA |
| Firing - Occupantanim | UCFLASH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 80% |

Source: expandmd01.mix/rulesmd.ini, section PARA, first property line 22934. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-paradropweapon"></a>

## Yuri's Revenge - PARADROPWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PARADROPWEAPON |
| Firing - base effect magnitude | 60 |
| Firing - reload interval | 130 |
| Firing - maximum range setting | 4 |
| Firing - Burst | 1 |
| Firing - Speed | 30 |
| Firing - Projectile | AAHeatSeeker2 |
| Firing - Warhead | MaverickHE |
| Projectile record | AAHeatSeeker2 |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | MaverickHE |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,100%,50%,50%,100%,75%,50%,25%,100% |
| Warhead - area spread | 1 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section PARADROPWEAPON, first property line 23185. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-parae"></a>

## Yuri's Revenge - PARAE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PARAE |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SSA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSA |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,60%,40%,40%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 80% |

Source: expandmd01.mix/rulesmd.ini, section PARAE, first property line 25294. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-pistola"></a>

## Yuri's Revenge - PISTOLA

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PISTOLA |
| Firing - base effect magnitude | 2 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section PISTOLA, first property line 24032. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-prismshot"></a>

## Yuri's Revenge - PRISMSHOT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PRISMSHOT |
| Firing - base effect magnitude | 120 |
| Firing - reload interval | 45 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | PrismWarhead |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | PrismWarhead |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,100%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Infdeath | 5 |

Source: expandmd01.mix/rulesmd.ini, section PRISMSHOT, first property line 23795. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-prismsupport"></a>

## Yuri's Revenge - PRISMSUPPORT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PRISMSUPPORT |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 45 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | DummyWarhead |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | DummyWarhead |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,0%,0%,0%,0%,0%,0%,0%,0% |

Source: expandmd01.mix/rulesmd.ini, section PRISMSUPPORT, first property line 23842. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-psiwave"></a>

## Yuri's Revenge - PSIWAVE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PSIWAVE |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 1 |
| Firing - Projectile | Psychic |
| Firing - Warhead | PsiPulse |
| Projectile record | Psychic |
| Warhead record | PsiPulse |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,0%,0% |
| Warhead - area spread | 3 |
| Warhead - Percentatmax | .85 |
| Warhead - Psychicdamage | yes |
| Warhead - Infdeath | 6 |
| Warhead - Affectsallies | no |

Source: expandmd01.mix/rulesmd.ini, section PSIWAVE, first property line 24087. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-psychicjab"></a>

## Yuri's Revenge - PSYCHICJAB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PSYCHICJAB |
| Firing - base effect magnitude | 25 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 4.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SAFlame |
| Firing - Occupantanim | UCINIT |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SAFlame |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | INITFIRE |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section PSYCHICJAB, first property line 22891. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-psychicjabe"></a>

## Yuri's Revenge - PSYCHICJABE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PSYCHICJABE |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SAFlame |
| Firing - Occupantanim | UCINIT |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SAFlame |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | INITFIRE |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section PSYCHICJABE, first property line 24689. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-punch"></a>

## Yuri's Revenge - PUNCH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PUNCH |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 1.4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Battering |
| Firing - Fireintransport | no |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Battering |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,30%,30%,20%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 10 |

Source: expandmd01.mix/rulesmd.ini, section PUNCH, first property line 23716. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-punche"></a>

## Yuri's Revenge - PUNCHE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | PUNCHE |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 1.4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Battering |
| Firing - Fireintransport | no |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Battering |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,30%,30%,20%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 10 |

Source: expandmd01.mix/rulesmd.ini, section PUNCHE, first property line 24954. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-radbeamweapon"></a>

## Yuri's Revenge - RADBEAMWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | RADBEAMWEAPON |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | RadBeamWarhead |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RadBeamWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,20%,15%,10%,0%,0%,0%,100%,100% |
| Warhead - Radiation | yes |
| Warhead - Infdeath | 7 |

Source: expandmd01.mix/rulesmd.ini, section RADBEAMWEAPON, first property line 23770. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-radbeamweapone"></a>

## Yuri's Revenge - RADBEAMWEAPONE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | RADBEAMWEAPONE |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 8 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | RadBeamWarhead |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RadBeamWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,20%,15%,10%,0%,0%,0%,100%,100% |
| Warhead - Radiation | yes |
| Warhead - Infdeath | 7 |

Source: expandmd01.mix/rulesmd.ini, section RADBEAMWEAPONE, first property line 25065. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-raderuptionweapon"></a>

## Yuri's Revenge - RADERUPTIONWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | RADERUPTIONWEAPON |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 1 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | RadEruptionWarhead |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | RadEruptionWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,20%,10%,10%,0%,0%,0%,100%,100% |
| Warhead - area spread | 10 |
| Warhead - Radiation | yes |
| Warhead - Infdeath | 7 |

Source: expandmd01.mix/rulesmd.ini, section RADERUPTIONWEAPON, first property line 23781. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-redeye2"></a>

## Yuri's Revenge - REDEYE2

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | REDEYE2 |
| Firing - base effect magnitude | 75 |
| Firing - reload interval | 55 |
| Firing - maximum range setting | 12 |
| Firing - Speed | 100 |
| Firing - Projectile | AAHeatSeeker |
| Firing - Warhead | SAMWH |
| Projectile record | AAHeatSeeker |
| Projectile - air targeting | yes |
| Projectile - ground targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 80 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Warhead record | SAMWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | 1 |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section REDEYE2, first property line 22547. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-repairbullet"></a>

## Yuri's Revenge - REPAIRBULLET

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | REPAIRBULLET |
| Firing - base effect magnitude | -50 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 1.8 |
| Firing - Speed | 100 |
| Firing - Projectile | Invisible |
| Firing - Warhead | Mechanical |
| Projectile record | Invisible |
| Warhead record | Mechanical |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - Infdeath | 0 |

Source: expandmd01.mix/rulesmd.ini, section REPAIRBULLET, first property line 23694. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-robogun"></a>

## Yuri's Revenge - ROBOGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | ROBOGUN |
| Firing - base effect magnitude | 65 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 60 |
| Firing - Projectile | Cannon |
| Firing - Warhead | AP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | AP |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,15%,75%,100%,100%,65%,45%,60%,60%,100% |
| Warhead - area spread | .3 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section ROBOGUN, first property line 23386. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-sabot"></a>

## Yuri's Revenge - SABOT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SABOT |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 70 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 60 |
| Firing - Projectile | Cannon |
| Firing - Warhead | UltraAP |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | UltraAP |
| Warhead - armor effectiveness, ordered percentages | 2%,2%,2%,100%,40%,100%,2%,2%,2%,2%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN30 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section SABOT, first property line 23398. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-sabote"></a>

## Yuri's Revenge - SABOTE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SABOTE |
| Firing - base effect magnitude | 175 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 6.75 |
| Firing - Burst | 2 |
| Firing - Speed | 60 |
| Firing - Projectile | Cannon |
| Firing - Warhead | UltraAPE |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | UltraAPE |
| Warhead - armor effectiveness, ordered percentages | 2%,2%,2%,100%,50%,100%,2%,2%,2%,100%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | VTEXPLOD |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section SABOTE, first property line 25188. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-sapper"></a>

## Yuri's Revenge - SAPPER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SAPPER |
| Firing - base effect magnitude | 2500 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible |
| Firing - Warhead | Mechanical |
| Projectile record | Invisible |
| Warhead record | Mechanical |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,100%,100%,100%,0%,0%,0%,100%,100% |
| Warhead - Infdeath | 0 |

Source: expandmd01.mix/rulesmd.ini, section SAPPER, first property line 22847. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-shovel"></a>

## Yuri's Revenge - SHOVEL

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SHOVEL |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section SHOVEL, first property line 23610. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-smash"></a>

## Yuri's Revenge - SMASH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SMASH |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 1.1 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Smashing |
| Firing - Fireintransport | no |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Smashing |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,100%,20%,100%,0%,0%,0%,0%,0% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 10 |

Source: expandmd01.mix/rulesmd.ini, section SMASH, first property line 23727. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-smashe"></a>

## Yuri's Revenge - SMASHE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SMASHE |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 1.1 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Smashing |
| Firing - Fireintransport | no |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Smashing |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,100%,20%,100%,0%,0%,0%,0%,0% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 10 |

Source: expandmd01.mix/rulesmd.ini, section SMASHE, first property line 24967. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-soniczap"></a>

## Yuri's Revenge - SONICZAP

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SONICZAP |
| Firing - base effect magnitude | 4 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | Sonic |
| Firing - Warhead | SonicWarhead |
| Firing - Issonic | Yes |
| Projectile record | Sonic |
| Warhead record | SonicWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,80%,80%,100%,60%,60%,100%,100% |
| Warhead - area spread | .1 |
| Warhead - Percentatmax | 1 |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Pronedamage | 50% |
| Warhead - Sonic | yes |

Source: expandmd01.mix/rulesmd.ini, section SONICZAP, first property line 23679. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-soniczape"></a>

## Yuri's Revenge - SONICZAPE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SONICZAPE |
| Firing - base effect magnitude | 8 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 6 |
| Firing - Burst | 2 |
| Firing - Speed | 100 |
| Firing - Projectile | Sonic |
| Firing - Warhead | SonicWarhead |
| Firing - Issonic | Yes |
| Projectile record | Sonic |
| Warhead record | SonicWarhead |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,80%,80%,100%,60%,60%,100%,100% |
| Warhead - area spread | .1 |
| Warhead - Percentatmax | 1 |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Pronedamage | 50% |
| Warhead - Sonic | yes |

Source: expandmd01.mix/rulesmd.ini, section SONICZAPE, first property line 25098. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-spycameraweapon"></a>

## Yuri's Revenge - SPYCAMERAWEAPON

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SPYCAMERAWEAPON |
| Firing - base effect magnitude | 6 |
| Firing - maximum range setting | 20 |
| Firing - Burst | 1 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | DummyWarhead |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | DummyWarhead |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,0%,0%,0%,0%,0%,0%,0%,0% |

Source: expandmd01.mix/rulesmd.ini, section SPYCAMERAWEAPON, first property line 23194. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-squidgrab"></a>

## Yuri's Revenge - SQUIDGRAB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SQUIDGRAB |
| Firing - base effect magnitude | 15 |
| Firing - reload interval | 99 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 30 |
| Firing - Projectile | SQDJUMP |
| Firing - Warhead | ParasitePlus |
| Projectile record | SQDJUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | ParasitePlus |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: expandmd01.mix/rulesmd.ini, section SQUIDGRAB, first property line 23629. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-squidgrabe"></a>

## Yuri's Revenge - SQUIDGRABE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SQUIDGRABE |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 99 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 30 |
| Firing - Projectile | SQDJUMP |
| Firing - Warhead | ParasitePlus |
| Projectile record | SQDJUMP |
| Projectile - air targeting | no |
| Projectile - Arm | 2 |
| Projectile - Rot | 8 |
| Projectile - Subjecttocliffs | no |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | no |
| Warhead record | ParasitePlus |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Parasite | yes |
| Warhead - Infdeath | 1 |

Source: expandmd01.mix/rulesmd.ini, section SQUIDGRABE, first property line 25257. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-squidpunch"></a>

## Yuri's Revenge - SQUIDPUNCH

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SQUIDPUNCH |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 32 |
| Firing - maximum range setting | 1.83 |
| Firing - Speed | 30 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HE |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,70%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section SQUIDPUNCH, first property line 23643. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-squidpunche"></a>

## Yuri's Revenge - SQUIDPUNCHE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SQUIDPUNCHE |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 32 |
| Firing - maximum range setting | 1.83 |
| Firing - Speed | 30 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | HE |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | HE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,70%,70%,35%,75%,40%,20%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Pronedamage | 70% |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section SQUIDPUNCHE, first property line 25272. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-stalgren"></a>

## Yuri's Revenge - STALGREN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | STALGREN |
| Firing - base effect magnitude | 10000 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | Cannon |
| Firing - Warhead | NukeB |
| Projectile record | Cannon |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | NukeB |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,0%,0%,0%,100%,100%,100%,0%,0% |
| Warhead - Animlist | MININUKE |

Source: expandmd01.mix/rulesmd.ini, section STALGREN, first property line 23036. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-stalgun"></a>

## Yuri's Revenge - STALGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | STALGUN |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint4 |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint4 |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,0%,0%,0%,0%,0%,0%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section STALGUN, first property line 23026. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-subtorpedo"></a>

## Yuri's Revenge - SUBTORPEDO

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUBTORPEDO |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 25 |
| Firing - Projectile | Torpedo |
| Firing - Warhead | APSplash |
| Projectile record | Torpedo |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 12 |
| Warhead record | APSplash |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,65%,60%,25%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .8 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section SUBTORPEDO, first property line 22514. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-subtorpedoe"></a>

## Yuri's Revenge - SUBTORPEDOE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUBTORPEDOE |
| Firing - base effect magnitude | 100 |
| Firing - reload interval | 120 |
| Firing - maximum range setting | 7 |
| Firing - Burst | 2 |
| Firing - Speed | 18 |
| Firing - Projectile | Torpedo |
| Firing - Warhead | APSplash |
| Projectile record | Torpedo |
| Projectile - air targeting | no |
| Projectile - ground targeting | yes |
| Projectile - Arm | 2 |
| Projectile - Rot | 12 |
| Warhead record | APSplash |
| Warhead - armor effectiveness, ordered percentages | 25%,25%,25%,75%,100%,100%,65%,65%,60%,25%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .8 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 3 |
| Warhead - Animlist | S_CLSN16,S_CLSN22,S_CLSN30,S_CLSN42,S_CLSN58 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section SUBTORPEDOE, first property line 25075. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-supercomet"></a>

## Yuri's Revenge - SUPERCOMET

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUPERCOMET |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 10 |
| Firing - Speed | 10 |
| Firing - Projectile | SuperCometP |
| Firing - Warhead | CometWH |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | SuperCometP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | SuperCometFragment |
| Warhead record | CometWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,50%,50%,200%,200%,200%,100%,100% |
| Warhead - Wall | no |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |

Source: expandmd01.mix/rulesmd.ini, section SUPERCOMET, first property line 24896. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-supercometfragment"></a>

## Yuri's Revenge - SUPERCOMETFRAGMENT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUPERCOMETFRAGMENT |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 10 |
| Firing - Projectile | SuperSmallCometP |
| Firing - Warhead | CometWH |
| Firing - Ishousecolor | true |
| Firing - Islaser | true |
| Projectile record | SuperSmallCometP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | CometFragment |
| Warhead record | CometWH |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,75%,50%,50%,200%,200%,200%,100%,100% |
| Warhead - Wall | no |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |

Source: expandmd01.mix/rulesmd.ini, section SUPERCOMETFRAGMENT, first property line 24912. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-supermindcontrol"></a>

## Yuri's Revenge - SUPERMINDCONTROL

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUPERMINDCONTROL |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 200 |
| Firing - maximum range setting | 7 |
| Firing - Speed | 100 |
| Firing - Projectile | PsychicControl |
| Firing - Warhead | ControllerBuilding |
| Projectile record | PsychicControl |
| Warhead record | ControllerBuilding |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,100%,100%,100%,100%,100%,100%,100%,100% |
| Warhead - Mindcontrol | yes |
| Warhead - Animlist | YURICNTL |

Source: expandmd01.mix/rulesmd.ini, section SUPERMINDCONTROL, first property line 24052. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-superpsiwave"></a>

## Yuri's Revenge - SUPERPSIWAVE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | SUPERPSIWAVE |
| Firing - base effect magnitude | 250 |
| Firing - reload interval | 50 |
| Firing - maximum range setting | 1 |
| Firing - Speed | 1 |
| Firing - Projectile | Psychic |
| Firing - Warhead | SuperPsiPulse |
| Projectile record | Psychic |
| Warhead record | SuperPsiPulse |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,50%,50%,50%,0%,0%,0%,0%,0% |
| Warhead - area spread | 5 |
| Warhead - Percentatmax | .85 |
| Warhead - Psychicdamage | yes |
| Warhead - Infdeath | 6 |
| Warhead - Affectsallies | no |

Source: expandmd01.mix/rulesmd.ini, section SUPERPSIWAVE, first property line 24099. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-tankbolt"></a>

## Yuri's Revenge - TANKBOLT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TANKBOLT |
| Firing - base effect magnitude | 135 |
| Firing - reload interval | 75 |
| Firing - maximum range setting | 4 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Electric |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: expandmd01.mix/rulesmd.ini, section TANKBOLT, first property line 23869. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-tankbolte"></a>

## Yuri's Revenge - TANKBOLTE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TANKBOLTE |
| Firing - base effect magnitude | 150 |
| Firing - reload interval | 60 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | Electricbounce |
| Firing - Warhead | Electric |
| Projectile record | Electricbounce |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | no |
| Projectile - Subjecttoelevation | no |
| Projectile - Shrapnelweapon | TeslaFragment |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: expandmd01.mix/rulesmd.ini, section TANKBOLTE, first property line 24862. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-termigun"></a>

## Yuri's Revenge - TERMIGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TERMIGUN |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 5 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | HollowPoint |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | HollowPoint |
| Warhead - armor effectiveness, ordered percentages | 200%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section TERMIGUN, first property line 23016. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-terrorbomb"></a>

## Yuri's Revenge - TERRORBOMB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TERRORBOMB |
| Firing - base effect magnitude | 225 |
| Firing - reload interval | 10 |
| Firing - maximum range setting | 1.5 |
| Firing - Projectile | Invisible |
| Firing - Warhead | TerrorBombWH |
| Firing - Fireintransport | no |
| Projectile record | Invisible |
| Warhead record | TerrorBombWH |
| Warhead - armor effectiveness, ordered percentages | 150%,100%,100%,90%,50%,50%,100%,150%,30%,100%,100% |
| Warhead - area spread | 2 |
| Warhead - Percentatmax | .5 |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | MININUKE |

Source: expandmd01.mix/rulesmd.ini, section TERRORBOMB, first property line 22371. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-teslafragment"></a>

## Yuri's Revenge - TESLAFRAGMENT

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TESLAFRAGMENT |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 3 |
| Firing - Speed | 10 |
| Firing - Projectile | SmallTeslaP |
| Firing - Warhead | Electric |
| Projectile record | SmallTeslaP |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Electric |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,85%,100%,100%,50%,50%,50%,200%,100% |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 5 |
| Warhead - Animlist | TSTIMPCT |

Source: expandmd01.mix/rulesmd.ini, section TESLAFRAGMENT, first property line 24322. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-trexbite"></a>

## Yuri's Revenge - TREXBITE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TREXBITE |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | TRexWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | TRexWH |
| Warhead - armor effectiveness, ordered percentages | 0%,0%,0%,60%,40%,40%,50%,40%,25%,80%,100% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 10 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section TREXBITE, first property line 23590. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-trexinfbite"></a>

## Yuri's Revenge - TREXINFBITE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | TREXINFBITE |
| Firing - base effect magnitude | 200 |
| Firing - reload interval | 30 |
| Firing - maximum range setting | 1.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | TRexInfWH |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | TRexInfWH |
| Warhead - armor effectiveness, ordered percentages | 100%,90%,80%,0%,0%,0%,0%,0%,0%,0%,0% |
| Warhead - area spread | .5 |
| Warhead - Percentatmax | .5 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 10 |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section TREXINFBITE, first property line 23600. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-ucelitem1carbine"></a>

## Yuri's Revenge - UCELITEM1CARBINE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | UCELITEM1CARBINE |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | SSAB |
| Firing - Occupantanim | UCCONS |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSAB |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,30%,20%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section UCELITEM1CARBINE, first property line 22881. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-ucelitepara"></a>

## Yuri's Revenge - UCELITEPARA

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | UCELITEPARA |
| Firing - base effect magnitude | 40 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | SSAB |
| Firing - Occupantanim | UCFLASH |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSAB |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,30%,20%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section UCELITEPARA, first property line 22956. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-ucelitepsychicjab"></a>

## Yuri's Revenge - UCELITEPSYCHICJAB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | UCELITEPSYCHICJAB |
| Firing - base effect magnitude | 73 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | SSABFlame |
| Firing - Occupantanim | UCINIT |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSABFlame |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,30%,20%,100%,100% |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | INITFIRE |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section UCELITEPSYCHICJAB, first property line 22913. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-ucm1carbine"></a>

## Yuri's Revenge - UCM1CARBINE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | UCM1CARBINE |
| Firing - base effect magnitude | 20 |
| Firing - reload interval | 20 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | SSAB |
| Firing - Occupantanim | UCCONS |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSAB |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,30%,20%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section UCM1CARBINE, first property line 22871. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-ucpara"></a>

## Yuri's Revenge - UCPARA

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | UCPARA |
| Firing - base effect magnitude | 30 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | SSAB |
| Firing - Occupantanim | UCFLASH |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSAB |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,30%,20%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section UCPARA, first property line 22945. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-ucpsychicjab"></a>

## Yuri's Revenge - UCPSYCHICJAB

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | UCPSYCHICJAB |
| Firing - base effect magnitude | 63 |
| Firing - reload interval | 15 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | SSABFlame |
| Firing - Occupantanim | UCINIT |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SSABFlame |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,30%,20%,100%,100% |
| Warhead - Infdeath | 4 |
| Warhead - Animlist | INITFIRE |
| Warhead - Pronedamage | 50% |

Source: expandmd01.mix/rulesmd.ini, section UCPSYCHICJAB, first property line 22903. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-v3cluster"></a>

## Yuri's Revenge - V3CLUSTER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | V3CLUSTER |
| Firing - base effect magnitude | 80 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 6 |
| Firing - Speed | 20 |
| Firing - Projectile | ClusterBits |
| Firing - Warhead | V3HE |
| Projectile record | ClusterBits |
| Projectile - Arm | 2 |
| Projectile - Rot | 60 |
| Warhead record | V3HE |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,30%,5%,5%,85%,50%,30%,100%,0% |
| Warhead - area spread | .9 |
| Warhead - Percentatmax | 1 |
| Warhead - Wall | yes |
| Warhead - Wood | yes |
| Warhead - Infdeath | 2 |
| Warhead - Animlist | XGRYSML1,XGRYSML2,EXPLOSML,XGRYMED1,XGRYMED2,EXPLOMED,EXPLOLRG,TWLT070 |
| Warhead - Tiberium | yes |

Source: expandmd01.mix/rulesmd.ini, section V3CLUSTER, first property line 24121. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-v3launcher"></a>

## Yuri's Revenge - V3LAUNCHER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | V3LAUNCHER |
| Firing - base effect magnitude | 1 |
| Firing - reload interval | 150 |
| Firing - maximum range setting | 18 |
| Firing - minimum range setting | 5 |
| Firing - Speed | 10 |
| Firing - Projectile | InvisibleHigh |
| Firing - Warhead | Special |
| Firing - Spawner | yes |
| Projectile record | InvisibleHigh |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Special |

Source: expandmd01.mix/rulesmd.ini, section V3LAUNCHER, first property line 23482. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-virtualscanner"></a>

## Yuri's Revenge - VIRTUALSCANNER

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | VIRTUALSCANNER |
| Firing - base effect magnitude | 1 |
| Firing - maximum range setting | 5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleAll |
| Firing - Warhead | SA |
| Projectile record | InvisibleAll |
| Projectile - air targeting | yes |
| Projectile - ground targeting | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section VIRTUALSCANNER, first property line 23620. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-virusgun"></a>

## Yuri's Revenge - VIRUSGUN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | VIRUSGUN |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 100 |
| Firing - maximum range setting | 10 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Virus |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Virus |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 8 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section VIRUSGUN, first property line 23087. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-virusgune"></a>

## Yuri's Revenge - VIRUSGUNE

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | VIRUSGUNE |
| Firing - base effect magnitude | 125 |
| Firing - reload interval | 80 |
| Firing - maximum range setting | 16 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | Virus |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | Virus |
| Warhead - armor effectiveness, ordered percentages | 100%,100%,100%,1%,1%,1%,1%,1%,1%,1%,100% |
| Warhead - Infdeath | 8 |
| Warhead - Animlist | PIFF |
| Warhead - Pronedamage | 100% |

Source: expandmd01.mix/rulesmd.ini, section VIRUSGUNE, first property line 23098. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-vulcan"></a>

## Yuri's Revenge - VULCAN

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | VULCAN |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 26 |
| Firing - maximum range setting | 5.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section VULCAN, first property line 22660. Projectile/warhead rows use the named sections in that same rules source.

<a id="yr-vulcan2"></a>

## Yuri's Revenge - VULCAN2

| Part of attack | Explicit setting/value |
| --- | --- |
| Firing record | VULCAN2 |
| Firing - base effect magnitude | 50 |
| Firing - reload interval | 26 |
| Firing - maximum range setting | 5.5 |
| Firing - Speed | 100 |
| Firing - Projectile | InvisibleLow |
| Firing - Warhead | SA |
| Projectile record | InvisibleLow |
| Projectile - Subjecttocliffs | yes |
| Projectile - Subjecttowalls | yes |
| Projectile - Subjecttoelevation | yes |
| Warhead record | SA |
| Warhead - armor effectiveness, ordered percentages | 100%,80%,80%,50%,25%,25%,75%,50%,25%,100%,100% |
| Warhead - Infdeath | 1 |
| Warhead - Animlist | PIFFPIFF,PIFFPIFF |
| Warhead - Pronedamage | 70% |

Source: expandmd01.mix/rulesmd.ini, section VULCAN2, first property line 22491. Projectile/warhead rows use the named sections in that same rules source.
