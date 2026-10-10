# DeadAir Economy Overhaul adopted by Chem O`Dun. Version without DeadAir wares

## Message from the DeadAir

I have decided to completely retire from X4 Modding. I have added licenses to Eco, Scripts, and DeadTater if any persons are interested in using, modifying, or continuing my works. Thank you for all the support and interest in my work over these years

## Message from Chem O`Dun

There is adoption the original mod to the **game version 9.0**.
Take into account that the mod is not compatible with older versions of X4. If you want to use it on older version, please use the original mod.
Additionally, please be informed that some ideas from the original mod now is implemented in a vanilla version of the game.

## Version without DeadAir wares

- This package, `deadair_eco_wo_da_w-<version>.zip` on Nexus Mods, is the mod without the three DeadAir wares (Advanced Schematics, Military Schematics, Labor Union Contracts), their production modules and factories, and the secondary-resource recipes that use them. Prices, production cycles, workforce effects, module and storage counts, baskets, jobs and faction logic are the same as in the full version.
- It shows up in the game as "DeadAir Eco. W/o DeadAir Wares". The full version comes in two packages, `deadair_eco_<version>.zip` and `deadair_eco_saved-<version>.zip` (recorded in savegames). Install only one of the three packages, into the same "deadair_eco" folder.

## Dynamic Universe (another DeadAir mod)

Status: unchanged

Minimalized diff mod for economy changes in X4. Readme is often out of date on features or numbers so feel free to contact me on the Egosoft Discord or check patch notes on pushes.

## AiScripts\Build.Shiptrader.xml

Status: unchanged

- Added chance for player to get rookies or veterans on hiring.
- Increased amount of ships assigned to trade for NPC shipyards and wharves.
- Added logic for traders to be assigned to Xenon shipyards.

## Structure Macro Changes

Status: unchanged

- Doubled capacity of drones for build modules to prevent AI from having too few drones to build ships at full speed.
- Increased Terran habitation modules to have same worker capacity as other factions.
- Updated threatscore for several xenon modules.

## Map Changes

Status: adopted to 9.0

- Added asteroid fields to cluster 403, 406
- Added gas field to cluster 403, 406

## Libraries\Baskets.xml

Status: adopted to 9.0

- Adjusted wares in baskets used by AI.

## Libraries\Constructionplans.xml

Status: adopted to 9.0

- Replaced 1M6S dock modules at important stations with 3M6S modules to improve ship docking capacity.

## Libraries\Defaults.xml

Status: unchanged

- Adjusted threatscore for different ships and increased station threatscore.

## Libraries\God.xml

Status: adopted to 9.0

- Increases allowed stations per zone to accomodate higher density.
- Removes Argon and Paranid stations from Split DLC sectors so they stop wasting resources and CPU cycles.
- Removes several quotas that cause smaller stations but does not change total production module count.

## Libraries\Jobs.xml

Status: adopted to 9.0

- Adjusted baskets used by traders to improve trader efficien (partly done by 9.0 vanilla).
- Adjusted trade ships to use traderoutine instead of distributewares aiscript so they will actually respond to trade imbalances on demand side instead of supply side (mostly done by 9.0 vanilla).
- Added jobs for silicon mining and ore mining for Xenon.
- Added missing water trader jobs for Antigone.

## Libraries\Loadoutrules.xml

Status: unchanged

- Increased weighting values for imprortant drones (transport drones for traders and build drones for construction ships).
- Attempted to reduce NPC ships loading up on deployables that serve no purpose other than to tank the economy.

## Libraries\mapdefaults.xml

Status: adopted to 9.0

- Adjusts sector economy ratings to remove undocumented effect on station size generation.
- For version 9.0, increased resource yields and "recovery" speed of several areas that are vital to the factions economic stability.

## Libraries\Modulegroups.xml

Status: adopted to 9.0

- Adjusted the dock module groups used for NPC station generation, in line with the Constructionplans.xml dock change.

## Libraries\Modules.xml

Status: unchanged

- Increased amount of modules that NPC are allowed to build on a single station. This greatly reduces the number of stations required for a functional economy.

## Libraries\Parameters.xml

Status: unchanged

- Increased amount of modules that NPC are allowed to build on a single station.
- Increased default level of drone loadout to prevent ships without enough drones to function effectively.

## Libraries\People.xml

Status: unchanged

- Increased fill percentage of certain NPC crews.
- Ships with Regular crews will have 50%+ of the ships capacity.
- Ships with Veteran crews will have 75%+ of the ships capacity.
- Ships with Elite crews will have 90%+ of the ships capacity.
- The higher importance the ship is to the faction, the higher the amount and ability of the crew.

## Libraries\Region_Definitions.xml

Status: adopted to 9.0

- Increased resource yields of several areas that are vital to the factions economic stability.

## Libraries\Ships.xml

Status: unchanged

- Adjusted the crews used by different ships.

## Libraries\Wares.xml

Status: adopted to 9.0

- Adjusts ware pricing to balance credits / m3 so traders will be rewarded for prioritizing shipping needed resources.
- Adjusts ware production cycles to standard increments. Scales required resources to match ratio from vanilla (Station calculator will still be accurate for ratio of modules not including workforce).
- Adjusts workforce effects to be more pronounced. This allows fewer stations for increased performance and increases the importance of food and medical supplies to a healthy economy.
- Adds a separate production method of energy cells for Xenon with values balanced for lack of workforce.
- Reduces construction time of modules so that the majority of the wait is for resources.
- Removes hullparts from station construction resources. This reduces the chance of a hull part shortage from building ships causing an entire economy to seize. Amount of claytronics and energy cells increased to match pre-change average credit cost.

## Md\Factionlogic_economy.xml

Status: adopted to 9.0

- Stations built after game start by NPC will have more modules.
- Early expansion of staged (prefab) stations: when a faction has a production shortage of a ware in a sector that stays below the level for a new production module, and an idle prefab there has a next stage producing that ware, the shortage counts as reaching that level with a 1-in-3 chance per evaluation, so the prefab grows by that stage instead of waiting for the regular prefab check hours later.
- Idle staged stations are offered as candidates whenever a faction looks for a station to extend with a production module. Vanilla rules them all out, because every vanilla prefab plan is fixed; a prefab whose next stage produces the ware is preferred over adding a module to an ordinary station.
- Fixes the vanilla check of a prefab's next stage, which skipped the stage's last module, so a stage holding only a production module could never be chosen or built.

## Md\Factionlogic_stations.xml

Status: unchanged

- Reduced desired wharves for Argon, Paranid, and Split to 1.

## Md\Finalisestations.xml

Status: adopted to 9.0

- Nudges station generation to use more horizontal connections than vertical.
- Increases station desired storage capacity to at least 2Mil M3 container and/or 1Mil M3 solid/liquid.

## Md\Inituniverse.xml

Status: unchanged

- Added several ship production wares to Trade Stations.
- Reduces rng for station initial fill.

## Dependencies

- From version 1.23 this mod requires the [Print Extension List](https://www.nexusmods.com/x4foundations/mods/2191) mod to record the game version and the enabled extensions in the debug log. Version `1.00` and upper is required.
- Requires Split, Terran, Pirate, and Boron DLC.

## Installation Info

- This mod is not compatible and must not be used with the older versions of Jobs, Gate, and Ware.
- Folder must be named "deadair_eco" or filepath's for added assets will fail and cause issues.
- Do not install a full version alongside this one; they all use the same folder.

## Save state

- **No** (removing the extension does not break saves). This version is not recorded in savegames (`save="false"`). Loading an existing game with it for the first time applies the new prices at once and adds the mod's ships (Antigone water traders, Xenon miners and traders). Stations that already exist keep their layout: the larger module and storage counts apply to stations built after the install. Removing the mod later returns the game to vanilla without a warning.

## Requesting Help

- It is very helpful to have a debug log with the debug options enabled.
- Include your mod list in any bug reports. There are a lot of poorly written mods out there.
- Best place to contact me is via @ on Egosoft Discord modding channel.

## Download

- Available on [Nexus Mods](https://www.nexusmods.com/x4foundations/mods/2139)

## Credits

- **Author**: Chem O`Dun, on [Nexus Mods](https://next.nexusmods.com/profile/ChemODun/mods?gameId=2659) and [Steam Workshop](https://steamcommunity.com/id/chemodun/myworkshopfiles/?appid=392160)
- *"X4: Foundations"* is a trademark of [Egosoft](https://www.egosoft.com).

## Acknowledgements

- [EGOSOFT](https://www.egosoft.com) - for the X series.
- [DeadAir](https://www.nexusmods.com/profile/DeaDAir) - for the original mod and permission to update it.

## Changelog

### [1.24] - 2026-10-10

- Early expansion of staged (prefab) stations on a production shortage works now; the previous logic could never trigger.
- Fixed a vanilla check that skipped the last module of a prefab's next stage.
- This version shows its own name in the game.

### [1.23] - 2026-08-21

- Restored the game-start creation of the defence stations and wharves in the Split DLC sectors, whose absence broke the Split-related game starts. Thanks to `ninchuka` and `Sentenza` for reporting it.
- Added the `Print Extension List` mod as a dependency, to help with debugging.

### [1.22] - 2026-07-12

- Removed hullparts from the Argon connector pieces added in game version 8.0 (Arc, Cross 02/03, and the T/L junction pieces) that were missed by the original hullparts-removal pass; costs now match their pre-8.0 sibling connectors.
- Removed hullparts from three dock "Showroom" modules and two Khaak scrap-processing modules (Scrapworks Khaak, Scrap Recycler Khaak) added in game version 9.0 that were likewise missed; costs now match their existing sibling modules.

### [1.21] - 2026-07-07

- Restored some accidentally removed god entries.
- Added version with no DA wares for those who want to use the mod but not the wares.

### [1.20] - 2026-05-31

- Initial public version for X4: Foundations version 9.0.
