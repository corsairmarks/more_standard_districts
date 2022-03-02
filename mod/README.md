# Overview

Would you like more basic districts for your colonies?  Perhaps you're tired of being limited by building slots?  Then this mods is for you!  Adds a Research District, Trade District, Leisure District, Administrative District, and Military District for construction on normal colonies.  Also adds an Administrative District and Military District for construction on habitats.  All gestalt empires can use Research Districts and Military Districts, but Leisure Districts are only available for Rogue Servitors.  Hive Minds, Machines, and Spiritualists have their own versions of the Administrative District.

Due to the addition of Research Districts, Research Labs have been adjusted to function similarly to the Alloy Foundries or Civilian Industries buildings.

Requested by [Mad Cow](https://steamcommunity.com/profiles/76561197969740903).

# Changes

Research, Trade, Leisure, Administrative/Ecclesiastical/Synapse/Data Warehouse, and Military districts are now available for regular colonies.  Administrative and Military districts are now also available for construction on habitats.  These new districts are considered "city" districts similar to Industrial Districts.  In addition, this mod updates Research Labs to function similarly to how Industrial Districts (the jobs provided by the district, really) are enhanced by the Alloy Foundries or Civilian Industries buildings:

* maximum one per planet
* all tiers provide exactly 2 jobs
* tier 2 increases research output by 1 point (per field) and increases researcher upkeep
* tier 3 increases research output by a total of 2 points (per field) and further increases researcher upkeep

Along with the new district types, this mod adds new colony designations for Commercial Worlds (focuses on Trade Districts) and Leisure Worlds (focuses on Leisure Districts) as well as updates the Tech-World designation to offer Research District build speed in addition to its existing benefits.  Unification Center and Fortress World automation plans are also updated to understand the new district types.  Each of the new colony designations features a build automation plan (including Rogue Servitors for Leisure Worlds).  The automation plan for Unification Centers, Fortress Worlds, and Tech-Worlds are also adjusted to use the new districts.

All districts respond to changes in civics that alter jobs.  For example, Leisure Districts trade Entertainers for a Duelists with Warrior Culture and Ecclesiastical Districts trade a Priest for a Manager for spiritualists megacorps.

## Localisation

* English by corsairmarks (author)
* German (Deutsch) by [Lucanoria](https://steamcommunity.com/id/Lucanoria)
* Polish (Polskie) by [Gatzek](https://steamcommunity.com/profiles/76561198440146604)
* Russian (Русский) by [Dimonius](https://steamcommunity.com/profiles/76561198011628045)
* Simplified Chinese by [megumin](https://steamcommunity.com/profiles/76561199071646261)

## Compatibility

Although the districts added by this mod seem similar to existing districts, they are created as new districts so as to not present a compatibility challenge by overwriting many of the district files.  The district changes should work with other mods that add or alter districts.

Overwrites `common/buildings/05_research_buildings.txt` to alter the Research Labs, and thus is not compatible with other mods that want to make changes to Research Labs, the Research Institute, or the Planetary Supercomputer.  To implement the desired effect from the new Research Lab, this mod overwrites the economic category for researchers (`planet_researchers`) in order to generate the `_add` modifiers for research production (previously only `_mult` was available).

Also overwrites all three flavors of Tech-World build automation (`common/colony_types/00_research_automation.txt`, `common/colony_types/00_research_hive_automation.txt`, `common/colony_types/00_research_machine_automation.txt`) to use the new Research Districts and enabling the AI to understand the Research Lab building changes.  Unification Center (`common/colony_types/00_bureau_automation.txt`) and Fortress World (`common/colony_types/00_fortress_automation.txt`, `common/colony_types/00_fortress_hive_automation.txt`, `common/colony_types/00_fortress_machine_automation.txt`) build automation is similarly overwritten.  Thus this mod is incompatible with other mods that also update these build plans.  Commonly this is AI mods - whichever mod loads _last_ will use its version of these files.

This mod adds a Commercial District which also has been built with compatibility for my mod [Enhanced Trade Districts and Designations](https://steamcommunity.com/workshop/filedetails/?id=2641081470).  Enjoy building commercial enterprises on practically any world.  Compatible with Planetary Diversity and follows its exclusions for some colony types.  Compatible with Gigastructural Engineering and follows its exclusions for some colony types.

Built for Stellaris version 3.3 "Libra."  Not compatible with achievements.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/workshop/filedetails/?id=2522974089); however is fully compatible.

### Required Dependency Mods

In order to see and interact with the new district types, it is necessary to use a UI mod that allows more districts to be visible.  [UI Overhaul Dynamic](https://steamcommunity.com/workshop/filedetails/?id=1623423360) and [Bigger Planet View](https://steamcommunity.com/workshop/filedetails/?id=1587178040) are two possible options.  If you play Stellaris on a lower resolution (such as 1366x768 or 1600x900) there are not many mod offerings that show many districts without making the planetview too large, so I created [Basic Planetview: More Districts](https://steamcommunity.com/workshop/filedetails/?id=2654043078) to solve that issue.

## Known Issues

Overriding an economic category and colony designations causes the game to log 12 errors like these:

```
[01:10:26][game_singleobjectdatabase.h:147]: Object with key: planet_researchers already exists, using the one at  file: common/economic_categories/01_more_standard_districts_economic_category_overrides.txt line: 1
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_research already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 6
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_bureau already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 29
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_bureau_spiritualist already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 70
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_bureau_hive already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 111
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_bureau_machine already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 141
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_habitat_bureau already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 172
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_habitat_bureau_spiritualist already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 198
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_habitat_bureau_hive already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 224
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_habitat_bureau_machine already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 247
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_fortress already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 271
[01:10:28][game_singleobjectdatabase.h:147]: Object with key: col_habitat_fortress already exists, using the one at  file: common/colony_types/01_more_standard_districts_colony_type_overrides.txt line: 358
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
    * Add Ecclesiastical Districts for Spiritualists -these districts replace Administrative Districts and offer a mix of Priests, Death Priests and Mortal Initiates, and/or Managers based on your civics
    * Leisure Districts are for Entertainers and Duelists only
    * Administrative Districts replace Bureaucrats with Managers for megacorps
    * Switched the color on all the flavors of admin districts to light blue to match the new arcology unity districts
    * Update icons for all flavors of admin district to use the unity symbol instead of the administrative capacity symbol
    * Add bureau colony automation plans for Hive and Machine Intelligence empires
    * All colony automation already overwritten by this mod now prioritizes the Posthumous Employment Center over Robot Assembly Plants
    * Use the new `script_values` feature to dynamically weight the bureau (unity) colony type based on how many unity jobs and buildings are present
    * Add compatibility for Gigastructural Engineering: districts from this mod are prohibited on gigastructures, habitat-specific districts from this mod are allowed on Interstellar habitats and Gas Giant Habitats

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/more_standard_districts)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.