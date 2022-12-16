# Overview

Would you like more basic districts for your colonies?  Perhaps you're tired of being limited by building slots?  Then this mods is for you!  Adds a Research District, Trade District, Leisure District, Administrative District, and Military District for construction on normal colonies.  Also adds an Administrative District and Military District for construction on habitats.  All gestalt empires can use Research Districts and Military Districts, but Leisure Districts are only available for Rogue Servitors.  Hive Minds, Machines, and Spiritualists have their own versions of the Administrative District.

Due to the addition of Research Districts, this mod adds a new research support building similar to the Alloy Foundries or Civilian Industries buildings.

Requested by [Mad Cow](https://steamcommunity.com/profiles/76561197969740903).

# Changes

Research, Trade, Leisure, Administrative/Ecclesiastical/Synapse/Data Warehouse, and Military Districts are now available for regular colonies.  Administrative (_et al_) and Military Districts are now also available for construction on habitats.  These new districts are considered "city" districts similar to Industrial Districts.  In addition, this mod adds a new research support building which functions similarly to how Industrial Districts are enhanced (the jobs provided by the district, really) by the Alloy Foundries or Civilian Industries buildings:

* maximum one per planet
* all tiers provide 1 head researcher or 2 gestalt researcher jobs
* tier 2 increases research output by 1 point (per field) and increases researcher upkeep
* tier 3 increases research output by a total of 2 points (per field) and further increases researcher upkeep

Along with the new district types, this mod adds new colony designations for Commercial Worlds (focuses on Trade Districts) and Leisure Worlds (focuses on Leisure Districts) as well as updates the Tech-World designation to understand the new research district type and to offer a Research District build speed increase. Trade planet, unity planet, and fortress planet automation plans are also updated to understand the new district types.  Each of the new colony designations features a build automation plan (including Rogue Servitors for Leisure Worlds).

All districts respond to changes in civics that alter jobs.  For example, Leisure Districts swap Entertainers for a Duelists with Warrior Culture and Ecclesiastical Districts trade a Priest for a Manager for spiritualist MegaCorps.

## Localisation

* English by corsairmarks (author)
* German (Deutsch) by [Lucanoria](https://steamcommunity.com/id/Lucanoria)
* Polish (Polskie) by [Gatzek](https://steamcommunity.com/profiles/76561198440146604)
* Russian (Русский) by [Dimonius](https://steamcommunity.com/profiles/76561198011628045)
* Simplified Chinese by [megumin](https://steamcommunity.com/profiles/76561199071646261)

## Compatibility

Although the districts added by this mod seem similar to existing districts, they are created as new districts so as to not present a compatibility challenge by overwriting many of the district files.  The district changes should work with other mods that add or alter districts.

To implement the new research support building (Planetary Archives) job bonuses, this mod overwrites the economic category for researchers (`planet_researchers`) in order to generate the `_add` modifiers for research production (previously only `_mult` was available).

Also overwrites research world build automation to use the new Research Districts and include the new research support building.  Trade planet, unity planet, and fortress planet build automation is similarly overwritten.  Thus this mod is incompatible with other mods that also update these four build plans.  Whichever mod loads _last_ will use its version of these files.

This mod adds a Commercial District which also has been built with compatibility for my mod [Enhanced Trade Districts and Designations](https://steamcommunity.com/workshop/filedetails/?id=2641081470).  Enjoy building commercial enterprises on practically any world.

Built for Stellaris version 3.6 "Orion."  Not compatible with achievements.  Compatible with Planetary Diversity and follows its exclusions for some colony types.  Compatible with Gigastructural Engineering and follows its exclusions for some colony types.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/workshop/filedetails/?id=2522974089); however is fully compatible.

### Required Dependency Mods

In order to see and interact with the new district types, it is necessary to use a UI mod that allows more districts to be visible.  [UI Overhaul Dynamic](https://steamcommunity.com/workshop/filedetails/?id=1623423360) and [Bigger Planet View](https://steamcommunity.com/workshop/filedetails/?id=1587178040) are two possible options.  If you play Stellaris on a lower resolution (such as 1366x768 or 1600x900) there are not many mod offerings that show many districts without making the planetview too large, so I created [Basic Planetview: More Districts](https://steamcommunity.com/workshop/filedetails/?id=2654043078) to address that challenge.

## Known Issues

Overriding a game object causes the game to write a line to its error.log file, expect to see fourteen errors like these:

```
[00:09:59][game_singleobjectdatabase.h:165]: Object with key: planet_researchers already exists, using the one at  file: common/economic_categories/01_more_standard_districts_economic_category_overrides.txt line: 1
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_research already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 6
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_bureau already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 50
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_bureau_spiritualist already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 120
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_bureau_hive already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 190
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_bureau_machine already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 242
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_trophy_machine already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 297
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_habitat_bureau already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 385
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_habitat_bureau_spiritualist already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 434
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_habitat_bureau_hive already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 483
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_habitat_bureau_machine already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 522
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_fortress already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 562
[00:10:01][game_singleobjectdatabase.h:165]: Object with key: col_habitat_fortress already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 601
[00:10:02][game_singleobjectdatabase.h:165]: Object with key: has_trade_designation already exists, using the one at  file: common/scripted_triggers/10_more_standard_districts_scripted_triggers_ai_overrides.txt line: 2
```

## Changelog

* 1.0.0 Initial version
* 1.1.0 Add new districts:
    * Military Districts
    * Administrative Districts (Hives get Synapse Districts and Machines get Data Warehouse Districts instead)
    * Adjust colony automation plans for Bureaucratic Center and Fortress World
* 1.1.1 Add missing localisation
* 1.2.0 Add Simplified Chinese localisation by megumin
* 2.0.0 Update for compatibility with Stellaris version 3.2 "Herbert"
    * Adjust economic category overwrite
    * Apply base game colony automation and designation changes
    * Apply base game research building changes
* 2.1.0 Exclude the basic More Standard Districts from Planetary Diversity's Planetary Habitats
    * Special thanks to Gatzek for help with the correct special `district_set`s
    * Add Polish localisation by Gatzek
* 2.2.0 Add German localisation by Lucanoria
* 2.3.0 Add administrative and military districts for habitats (including for Hives and Machines) with designations and automation plans
    * Update German localisation by Lucanoria
    * Update Polish localisation by Gatzek
    * Could use assistance with Russian and Simplified Chinese
* 3.0.0 Update for Stellaris version 3.3.0 "Libra" - integrate underlying changes from the base game
    * Buildings are no longer full-file overwrites!
    * Only the relevant `building_research_lab_X` buildings are overridden instead of all research buildings
    * Add Ecclesiastical Districts for Spiritualists -these districts replace Administrative Districts and offer a mix of Priests, Death Priests and Mortal Initiates, and/or Managers based on your civics
    * Leisure Districts provide Entertainers or Duelists only
    * Administrative Districts replace Bureaucrats with Managers for megacorps
    * Switched the color on all the flavors of admin districts to light blue to match the new arcology unity districts
    * Update icons for all flavors of admin district to use the unity symbol instead of the administrative capacity symbol
    * Add bureau colony automation plans for Hive and Machine Intelligence empires
    * All colony automation overwritten by this mod now prioritizes the Posthumous Employment Center over Robot Assembly Plants
    * Use the new `script_values` feature to dynamically weight the bureau (unity) colony type based on how many unity jobs, buildings, and districts are present
    * Add compatibility for Gigastructural Engineering: districts from this mod are prohibited on gigastructures, habitat-specific districts from this mod are allowed on Interstellar habitats and Gas Giant Habitats
* 3.1.0 Allow an uncapped amount of Research Labs to be built
    * Previous "per researcher" bonus from Research Labs is now part of a new building series (Planetary Archives)
    * All research-related automation plans are now overwritten to account for this new building
* 4.0.0 Update for Stellaris version 3.4 "Cepheus"
    * Use memory optimization feature for triggers
    * Integrate underlying colony type changes
    * Remove existing automation plans, replace with simplified versions (similar to how the base game simplified and refined its automation plans)
    * Update overridden colony types to respect sector automation settings
    * Commercial World colony designation now indicates that it improves the relevant trade district type
* 4.1.0 Balance update - reduce the overwhelming **Trade Power™** generated for minimal effort and also simplify triggered job swaps
    * Update support for Planetary Diversity and Gigastructural Engineering
    * Reduce the amount of free MegaCorp job swaps; post-unity-rework they are much more powerful than in the past
    * Simplify the Merchant/Executive/Manager jobs swaps for commercial districts - things got a little out of hand
    * Add custom description to the trade district, describing the job shifts
* 4.2.0 Better colony designation compatibility
    * The Tech-World and Fortress World colony designations requirements more accurately reflect the base game: they can be used on any planet which is not an ecumenopolis, habitat, or ringworld - the bonus district build speed modifiers will only appear on planets supported by the districts
    * Fix the broken weight-related script_value for the Commercial World colony designation
    * Improve weighting for Fortress Worlds and Fortress Stations
* 5.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Bonus clerk jobs are now tied to the tradition Trickle Up Economics instead of Interstellar Franchising (from underlying game changes)
    * Add override of new built-in trigger `has_trade_designation`, consume it for trade colony automation
    * Trade planet automation is now an override and cooperates with my other trade-related district mods
    * No longer destroy the archive advanced buildings when out of exotic gas (mirrors similar changes in the underlying game)
    * Integrate underlying automation plan and colony designation changes
    * Apply changes from the game's district types to my similar types (e.g. the new perks for the spiritualist federation affecting unity districts)
    * Support the megalopolis from Guilli's Planet Modifiers and Features

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/more_standard_districts)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.