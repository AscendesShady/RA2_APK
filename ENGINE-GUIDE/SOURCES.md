# Sources, verification and limits

[Guide index](README.md)

Prepared from the local game install and port workspace on 26 October 2026. This is a plain-language analysis, not the original source code and not a claim of a completed playthrough of every mission.

## Evidence labels

- **Data-confirmed:** present in extracted rules, campaign tables, maps or strings.
- **Binary-supported:** backed by local class/function recovery or inspected lifted procedures.
- **Manual-described:** player-visible behavior described by the supplied English manuals.
- **Conceptual reconstruction:** an explanatory decision sequence consistent with these sources, without a claim that every original instruction/order has been recovered.
- **Unverified in play:** a prediction or branch not exercised in a recorded playthrough.

## Extraction and precedence

1. Read the original MIX archive index, decrypting its header where required.
2. Resolve member names with the game-compatible filename hash.
3. Check every member span stays within the declared archive body.
4. Extract the known rules, AI, campaign tables, localization tables and campaign maps.
5. Validate the complete CSF string-table structure and decode its text.
6. Apply the patch archive's rulesmd.ini and all02umd.map in preference to the base members.
7. Keep RA2 and Yuri rules separate.
8. Merge a mission's explicit overrides only for its scenario; missing values are not invented.
9. Translate every recovered event/action record, retaining action order, identifiers and source line locators.

The tools and raw extracted resources remain in the local build-cache/engine-guide-research folder. The reading folder contains derived explanations and factual reference tables, not a new dump of the original rule/map files.

## Coverage

| Item | Count |
| --- | --- |
| Distinct registered mobile types across both games | 157 |
| Distinct registered building types across both games | 408 |
| Story missions | 38 |
| Training missions | 2 |
| Additional legacy/alternate map | 1 |
| Documented scenario maps | 41 |
| Translated trigger definitions | 4274 |
| Translated event records | 4787 |
| Translated ordered action records | 13724 |
| Weapon/effect cards (game-specific) | 341 |
| RA2 global AI team templates | 103 |
| Yuri global AI team templates | 163 |

## Local binary evidence

- native-ra2/game/game.exe: 5,077,312 bytes; SHA-256 73288c03b58d370be268ca6d156b4e33bfdb2066dc980359467d8852ff3b00df.
- native-ra2/game/gamemd.exe: 5,286,208 bytes; SHA-256 3e81a61775d2745d1dabe397325ef663cd994ffc194da4e998e3bf5d2d308600.

The local recovered class catalogue contains the expected live-object/type, house, cell, trigger, team, factory, projectile and movement-controller responsibilities. The guide does not equate class names with a complete recovery of their algorithms. The Yuri function catalogue and lifted action runner were checked together. The action-runner trace at original address 0x007265C0 checks enabled/destroyed state, walks the action list and invokes the executor at 0x006DD8B0. Those addresses are version-specific evidence locators, not mobile gameplay instructions.

Local source locators: native-ra2/work/rtti.json; native-ra2/work/game/rtti.json; native-ra2/work/functions.json; native-ra2/src/recomp/gen/recomp_0049.c; native-ra2/docs/voxels.md; native-android/PORTING.md; native-android/src/android_entry.c; native-android/app/src/main/java; Native-APK/qa/save-0.1.4/report.md. Relative paths here describe the original workspace and are not required to read the published guide.

## Supplied manuals

The accompanying English RA2 manual explains units, structures, garrisons, Engineers, economy, powers and controls. The English Yuri manual explains expansion changes and the added units/structures. They were text-extracted locally for this analysis; the reading guide paraphrases their gameplay explanations and cross-checks explicit rule fields. Manuals can describe intended behavior that differs from a particular patch or scenario.

Local files: Command.&.Conquer.Red.Alert.II/game/Manuals/Red Alert 2 - English 2 - Manual.pdf; Command.&.Conquer.Red.Alert.II/game/Manuals/Yuri_s Revenge - English - Manual.pdf.

## Primary technical cross-checks

- [YRpp TriggerClass](https://github.com/Ares-Developers/YRpp/blob/master/TriggerClass.h): event state and trigger-action responsibilities.
- [YRpp TActionClass](https://github.com/Ares-Developers/YRpp/blob/master/TActionClass.h): action executor and identified operation entry points.
- [YRpp ScriptClass](https://github.com/Ares-Developers/YRpp/blob/master/ScriptClass.h): ordered script state.
- [YRpp GeneralDefinitions](https://github.com/Ares-Developers/YRpp/blob/master/GeneralDefinitions.h): event identifiers and object-mission identifiers.
- [FinalAlert extension documentation](https://github.com/secsome/FA2sp/blob/master/DOCUMENT.md): editor labels for script instruction numbers. Only vanilla instructions used by these maps are described; extension-only features are not assigned to this APK.
- The supplied FinalAlert2/FAData.ini event/action descriptions supply the main translation vocabulary. Its modification date is newer than the retail game, so descriptions are cross-checking aids, not proof that later extension behavior is present.
- [Static recompilation project](https://github.com/sp00nznet/redalert2-recomp): background for the local runtime and renderer research. Android behavior here is established from the local port, not inferred from desktop feature claims.

## What remains open

The guide does not claim exact pathfinder search/tie-breaking, every target-score formula, complete save serialization internals, exhaustive numeric hardcoded defaults, or proof that every declared trigger is reachable. Special editor parameters not independently established remain named configured values. No new complete campaign playthrough, physical Samsung S Pen/OTG qualification, performance measurement or long-session stability trial was performed while writing this guide.

The legacy sov09t.map is documented separately from the campaign-selected sov09u.map. Both tutorial maps are included. Multiplayer/co-op/skirmish maps are not each treated as a new story mission, and multiplayer is disabled in the delivered APK. Global rules/AI still explain their shared mechanisms.

## Extracted member fingerprints

These identify the exact local source bytes used. Duplicated maps in multiple archives remain listed so provenance is not lost.

| Archive/member | Bytes | SHA-256 |
| --- | --- | --- |
| ra2.mix/local.mix/rules.ini | 541915 | fd1e95cea0306ea78049dc81c8cd816e18c28c496872a1ff02edd50bd082062f |
| ra2.mix/local.mix/art.ini | 245825 | b477f861063a9509e87b7836b78190204c73bea5ea5595a842c456f5920ea223 |
| ra2.mix/local.mix/ai.ini | 84972 | 1feac6ddea6886b177ddf7e5f8580b7a99a63f12684f2cbb42831671bb7a8a79 |
| ra2.mix/local.mix/battle.ini | 4054 | a5752a8d49e1c3823fe01a55e0057f91f2996d8b4a78804f197251a79b552a1d |
| ra2.mix/local.mix/mission.ini | 9756 | 49eb674e46058d67a08e0cf4ba31c99b1948d3d2072b10beced873f62226c54e |
| ra2.mix/local.mix/mapsel.ini | 7875 | f4bcbb678d182c35a4331d69c92150a719d73fc0c95fae36cc52e65d74923982 |
| ra2.mix/local.mix/tutorial.ini | 14762 | 59b44499e1720c275e78cb5397e19fb94dbac46e22ea54c220e01e9e1a1d0492 |
| ra2md.mix/localmd.mix/rulesmd.ini | 742958 | 06761dd7f714e7d9400216ec3c06109ec5c1461f6a0727be7401eb9d8b0f6d05 |
| ra2md.mix/localmd.mix/artmd.ini | 336535 | e1f0378394313c04ebbd5073f47785ee3e46f1b3c62d65724e8f3c310ee7ba31 |
| ra2md.mix/localmd.mix/aimd.ini | 138538 | 5df41eaec00a78d0760ef5eecdf27d65ae1cd537309c7eac973318266986f89d |
| ra2md.mix/localmd.mix/battlemd.ini | 2733 | 7e40691a3480b1e5ffe6d1cdfccb83f67da4447157607ec3ecb5d2278acf0791 |
| ra2md.mix/localmd.mix/missionmd.ini | 5034 | ce170ec97fc28589ee971792a31d135e0f0510f878acde3fd0d79a7b7896a775 |
| ra2md.mix/localmd.mix/mapselmd.ini | 5573 | 074ccccd9e156d586d0ed099ceab78b3d72384c808725d8b5bee2c9799691d52 |
| expandmd01.mix/rulesmd.ini | 743215 | 3d341ef8a13a4b5ab24af2eef48ac94931ac2bb87d950fe3330a07e2d25672ef |
| expandmd01.mix/all02umd.map | 465788 | e761d28ce43401308ca4532d65479b1cf4a309d74fd4f996fafa92a0a06f8b65 |
| language.mix/ra2.csf | 485776 | e46715fcdf038c4c3231a457873fc711174110d721a0a5390a508dbadcf4ff72 |
| langmd.mix/ra2md.csf | 573269 | f3382231d7eb3bd713bf3908ecdba175a1b2e20d9d80fa2702e9ab84c3a79deb |
| MAPS01.MIX/all01t.map | 146240 | ad64c9293a8bccb85c38f5871a974ed9c09b8b5da11bb346e990423bf625c79c |
| MAPS01.MIX/all02s.map | 191242 | 5ebd7a3aaa60215a6da1f63e87a53c4ebf8cb28378b09f7128953ab05e6425fc |
| MAPS01.MIX/all03u.map | 202576 | 186e317d4be77eaeec8e0b09e5c813f6ff95aa01e4e206f4b4c82178bf679a61 |
| MAPS01.MIX/all04u.map | 222831 | 09e52db16946a330c032e988679ef61ff7745670ddad5e9bfcf96f916d18d093 |
| MAPS01.MIX/all05s.map | 214744 | d09cebddc1f4009098dfa48b18bf4022e6e4d00801f1ca8efd99917f185bb225 |
| MAPS01.MIX/all06u.map | 260458 | 9e02b8fa4c570000c2bb34c9b0e702b143e2e93ae529faa36556e1f43af0f922 |
| MAPS01.MIX/all07t.map | 471258 | 3925c1211d86938a7137ff0df11cba85c59d3ae75742221d5e2d4d502d33c103 |
| MAPS01.MIX/all08u.map | 199442 | 71a119187bd8f78a1c7677636e20a18a258f24dc94add2ac2b108a3dae9df8ea |
| MAPS01.MIX/all09t.map | 190682 | 89a243ea0d9ccc802bd6e1d7da4d271d0077f86c3883802e27be7840364ac279 |
| MAPS01.MIX/all10s.map | 289946 | ac0ea14ec650256a014626db7c78135bb74168ba86d4eb863d987f04b07d1593 |
| MAPS01.MIX/all11t.map | 369324 | 08456515dd5e258f5a9ff73b8961491883eccaa3635a8f008dcb1f9369d43887 |
| MAPS01.MIX/all12s.map | 185688 | e6d31134742f8566a425a252113fa6b8e3f3eb178b00e34124deec4f7e11250b |
| MAPS01.MIX/sov01t.map | 184260 | 7f4492961d30b5799367aa840ba007932057b19a22a77f95475a18ca1407b99f |
| MAPS01.MIX/trn01t.map | 98389 | 4dcec9e12f2541e4c15bf1e7da78c6ff74932c794837c35029a02de5bf43cd71 |
| MAPS01.MIX/trn02t.map | 57795 | 35f7b531a8d0312ca7e44fa1da33f88dde1af48ac3781841bc74d3122c498445 |
| MAPS02.MIX/all01t.map | 146240 | ad64c9293a8bccb85c38f5871a974ed9c09b8b5da11bb346e990423bf625c79c |
| MAPS02.MIX/sov01t.map | 184260 | 7f4492961d30b5799367aa840ba007932057b19a22a77f95475a18ca1407b99f |
| MAPS02.MIX/sov02t.map | 186385 | ea3aff6876f7e81e76284a2c9b41ee693c71f0f27e1ae45542e8f5ea95c96ae7 |
| MAPS02.MIX/sov03u.map | 173904 | a0ec1cd648f2b1f5cd122713d405b514634941977289080e22990021f8719c05 |
| MAPS02.MIX/sov04s.map | 201817 | a0a95b26639cc1d4d916dea3a264a18e409bef3d2b84c245e67cd250defc2100 |
| MAPS02.MIX/sov05u.map | 85694 | 31c6883ce678c0bcede293c571a610d355319a7cd729d45560183ced152a5629 |
| MAPS02.MIX/sov06t.map | 262145 | bea4548cca589aa1caf6fbc4e69700f8b408d650b700b71c65242f0df9eeeb83 |
| MAPS02.MIX/sov07s.map | 178521 | 0ad2fde5c76f17085065f7b43cb76045935774092b2498badc44fe91e7793171 |
| MAPS02.MIX/sov08u.map | 197257 | 91817fa1585e631cd929b6356ccc29c99f1dfb8144c52cd225e3eeb924370b7e |
| MAPS02.MIX/sov09t.map | 110638 | e444665c9afec8ffa2528d4e10641739f8a7c16921522b91dba3520cacd71041 |
| MAPS02.MIX/sov09u.map | 105691 | ef2dd5c5280d20f5759c02cebf860111280dc0f091c322f21b42eeae6b53c8b6 |
| MAPS02.MIX/sov10t.map | 276498 | 5c3d8b26e05a0a73530630db8353637fa9ed7072144d5360e1ab994869428449 |
| MAPS02.MIX/sov11s.map | 187412 | 2f51c08a063f3c4d648bd486672eacc50d3f32903aa14e9566bfd2030464fc7f |
| MAPS02.MIX/sov12s.map | 231726 | f69c18a54ce5915c9cdc08c2f10113853bc8656cf3e5f1392a64818a700d2720 |
| mapsmd03.mix/all01umd.map | 301077 | dee38769f2247a85908705486c175ef14a4cf90437899defe7c8b4c0d1c51fb0 |
| mapsmd03.mix/all02umd.map | 465825 | 168ed42024991b6c2af4de0e5a667e9c2bf15767741efe99dac975721460b303 |
| mapsmd03.mix/all03umd.map | 418628 | b84a2e689cc00f0be064ecbfcd385635ac037f28bf8f72c02b426a0e52ff1547 |
| mapsmd03.mix/all04dmd.map | 282057 | f1621a21e7221c1e475a52dccd4a04bb3125f8a095377c917e2122019f2157b2 |
| mapsmd03.mix/all05umd.map | 274279 | 7ee8148ad4b0092b7970588d9b064ddd6b753fc7bfb352bcc043affeb72c6aed |
| mapsmd03.mix/all06umd.map | 192301 | cfd2b50c5448fd84ab3647ff3a95f96b45e8dccd6a72b2601c0bb603cddeeb63 |
| mapsmd03.mix/all07smd.map | 434373 | 0ec687c320382e4c02cf66eec0153b713e56c4449fab7d29b5a19b61bf10e4f3 |
| mapsmd03.mix/sov01umd.map | 329188 | 498b989a4b6f579dee0904a77f1fabf982c14786db21a46c41900fc8344ec72b |
| mapsmd03.mix/sov02smd.map | 327808 | 139a7f17a17cefc20d12c21e9221d94ff6e1e8894ac09ab716fc9f6975d5a665 |
| mapsmd03.mix/sov03umd.map | 189836 | df69d0f63f982823bb5818d3d49776028a719a2c20ced2526fab8f5cecb49fe6 |
| mapsmd03.mix/sov04dmd.map | 228003 | 702bd788efbd08ae5b7591a1dfc240684e73faedace2ffaac68baefdfd0fb12a |
| mapsmd03.mix/sov05umd.map | 467636 | 22518e8b4a86331a9172048e10de13b45c2826ea4fdf4d2203b58994b897761b |
| mapsmd03.mix/sov06lmd.map | 141376 | f55b65fd33a53dd03f61b48259d7732d260a4f97170e6dcf0767a61af82403a4 |
| mapsmd03.mix/sov07tmd.map | 367021 | eacf89952cb6e8eacd762f97895a062e0b6bfa16c8f916b901c1e667def266d4 |
