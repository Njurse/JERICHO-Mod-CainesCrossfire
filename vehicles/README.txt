CROSSFIRE - one-car Driver 2 car-data bank
================================

Source: VEGAS model 3
Destination model slot: 1

This bank carries ONE car: clean, damaged and low. Every other model
slot is -1.

Files:
  bank.json          the declaration (slot order, cars)
  CROSSFIRE.LEV / .LCF      installed copies of build/ (loadable pair)
  cars/              the car's editable OBJ/MTL, page PNGs and sounds
  build/             the bake output, never edited (safe to delete)

Install:
  Shipped as a mod (JERICHO/MODS/<id>/banks/<dir>/), carhacks 0.2.7+
  registers it on its own when the mod is enabled. By hand:
  1. Put this folder where cities.ini can reach it.
  2. Add the line from cities.ini under [cities] in
     JERICHO/CONFIG/cities.ini.
  3. Import it with import = <resident slot>:<city index>:<model>.
     city_N has city index 11 (11 + N).

Stage scripts (written beside this file):
  wizard.bat    hub for every stage below
  rebake.bat    bake + install + register, then preview / ride
  preview.bat   pick a slot, endless preview until you quit
  playtest.bat  Take a Ride with a car, no bake

Rebuild after editing the car's OBJ or bank.json:
  rebake.bat
