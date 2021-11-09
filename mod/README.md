# Overview

Would you like more basic districts for your colonies?  Perhaps you're tired of being limited by building slots?  Then this mods is for you!  Adds a Research District, Commercial District, and Leisure District for construction on normal colonies.  All gestalt empires can use Research Districts, but Leisure Districts are only available for Rogue Servitors.

Due to the addition of Research Districts, Research Labs have been adjusted to function similarly to the Alloy Foundries or Civilian Industries buildings.

Requested by [Mad Cow](https://steamcommunity.com/profiles/76561197969740903).

# Changes

Research, Commercial, and Leisure districts are now available for regular colonies.

Because Research Districts are now available, this mod updates Research Labs to function similarly to the Alloy Foundries or Civilian Industries buildings:

* maximum one per planet
* all tiers provide exactly 2 jobs
* tier 2 increases research output by 1 point (per field) and increases researcher upkeep
* tier 3 increases research output by a total of 2 points (per field) and further increases researcher upkeep

## Compatibility

Although the districts added by this mod seem similar to existing districts, they are created as new districts so as to not present a compatibility challenge by overwriting many of the district files.  The district changes should work with other mods that add or alter districts.

Overwrites `common/buildings/05_research_buildings.txt` to alter the Research Labs, and thus is not compatible with other mods that want to make changes to Research Labs, the Research Institute, or the Planetary Supercomputer.

This mod adds a Commercial District which also has been build with compatibility for my mod [Enhanced Trade Districts and Designations](https://steamcommunity.com/sharedfiles/filedetails/?id=2641081470).  Enjoy building commercial enterprises on practically any world.

Built for Stellaris version 3.1.\* "Lem."  Not compatible with achievements.

### Required Dependency Mods

In order to see and interact with the new district types, it is necessary to use a UI mod that allows more districts to be available.  [UI Overhaul Dynamic](), [](), or []() are a few of the available options.

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub]()

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.



---------------------------


In short, I'd like to port the habitat trade, research, and leisure districts for use on regular worlds. I think if the exact designations are used the AI will understand their function (or it may simply be needed to be included in the district code, you'd know better than I would). Gestalts can be excluded from trade districts are discretion. And yes, I use the Bigger Planets mod which has a scrollbar for districts. My personal mod uses the "more than 1 district" uses 3/14 display and allows up to 20 buildings. Once those districts are standardized, it opens up more options for world customization.



colony automation for new designations
override science automation