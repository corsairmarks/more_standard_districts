# Overview

Would you like more basic districts for your colonies?  Perhaps you're tired of being limited by building slots?  Then this mods is for you!  Adds a Research District, Trade District, Leisure District, Administrative District, and Military District for construction on normal colonies.  All gestalt empires can use Research Districts and Military Districts, but Leisure Districts are only available for Rogue Servitors.  Hive Minds and Machines have their own versions of the Administrative District.

Due to the addition of Research Districts, Research Labs have been adjusted to function similarly to the Alloy Foundries or Civilian Industries buildings.

Requested by [Mad Cow](https://steamcommunity.com/profiles/76561197969740903).

# Changes

Research, Trade, Leisure, Administrative/Synapse/Data Warehouse, and Military districts are now available for regular colonies.  These new districts are considered "city" districts similar to Industrial Districts.  In addition, this mod updates Research Labs to function similarly to how Industrial Districts (the jobs provided by the district, really) are enhanced by the Alloy Foundries or Civilian Industries buildings:

* maximum one per planet
* all tiers provide exactly 2 jobs
* tier 2 increases research output by 1 point (per field) and increases researcher upkeep
* tier 3 increases research output by a total of 2 points (per field) and further increases researcher upkeep

Along with the new district types, this mod adds new colony designations for Commercial Worlds (focuses on Trade Districts) and Leisure Worlds (focuses on Leisure Districts) as well as updates the Tech-World designation to offer Research District build speed in addition to its existing benefits.  Bureaucratic Center and Fortress World automation plans are also updated to understand the new district types.  Each of the new colony designations features a build automation plan (including Rogue Servitors for Leisure Worlds).  The automation plan for Bureaucratic Centers, Fortress Worlds, and Tech-Worlds is also adjusted to use the new Research District and updated Research Lab.

## Localisation

* English by corsairmarks (author)
* Simplified Chinese by [megumin](https://steamcommunity.com/profiles/76561199071646261)

## Compatibility

Although the districts added by this mod seem similar to existing districts, they are created as new districts so as to not present a compatibility challenge by overwriting many of the district files.  The district changes should work with other mods that add or alter districts.

Overwrites `common/buildings/05_research_buildings.txt` to alter the Research Labs, and thus is not compatible with other mods that want to make changes to Research Labs, the Research Institute, or the Planetary Supercomputer.  To implement the desired effect from the new Research Lab, this mod overwrites the economic category for researchers (`planet_researchers`) in order to generate the `_add` modifiers for research production (previously only `_mult` was available).

Also overwrites all three flavors of Tech-World build automation (`common/colony_types/00_research_automation.txt`, `common/colony_types/00_research_hive_automation.txt`, `common/colony_types/00_research_machine_automation.txt`) to use the new Research Districts and enabling the AI to understand the Research Lab building changes.  Bureaucratic Center (`common/colony_types/00_bureau_automation.txt`) and Fortress World (`common/colony_types/00_fortress_automation.txt`, `common/colony_types/00_fortress_hive_automation.txt`, `common/colony_types/00_fortress_machine_automation.txt`) build automation is similarly overwritten.  Thus this mod is incompatible with other mods that also update these build plans.  Commonly this is AI mods - whichever mod loads _last_ will use its version of these files.

This mod adds a Commercial District which also has been built with compatibility for my mod [Enhanced Trade Districts and Designations](https://steamcommunity.com/sharedfiles/filedetails/?id=2641081470).  Enjoy building commercial enterprises on practically any world.

Built for Stellaris version 3.1.\* "Lem."  Not compatible with achievements.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) because it would require users to add a UI mod in order to see the expanded districts.  It it otherwise fully compatible.

### Required Dependency Mods

In order to see and interact with the new district types, it is necessary to use a UI mod that allows more districts to be visible.  [UI Overhaul Dynamic](https://steamcommunity.com/sharedfiles/filedetails/?id=1623423360) and [Bigger Planet View](https://steamcommunity.com/sharedfiles/filedetails/?id=1587178040) are two possible options.  If you play Stellaris on a lower resolution (such as 1366x768 or 1600x900) there are not many mod offerings that show many districts without making the planetview too large, so I created [Basic Planetview: More Districts](https://steamcommunity.com/sharedfiles/filedetails/?id=2654043078) to solve that issue.

## Known Issues

Overriding an economic category and colony designations causes the game to log four errors like these:

```
[20:58:16][game_singleobjectdatabase.h:147]: Object with key: planet_researchers already exists
[20:58:17][game_singleobjectdatabase.h:147]: Object with key: col_research already exists
[20:58:17][game_singleobjectdatabase.h:147]: Object with key: col_bureau already exists
[20:58:17][game_singleobjectdatabase.h:147]: Object with key: col_fortress already exists
```

## Changelog

* 1.0.0 Initial version
* 1.1.0 Add new districts:
    * Military Districts
    * Administrative Districts (Hives get Synapse Districts and Machines get Data Warehouse Districts instead)
    * Adjust colony automation plans for Bureaucratic Center and Fortress World
* 1.1.1 Add missing localisation
* 1.2.0 Add Simplified Chinese localisation by megumin

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/more_standard_districts)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.