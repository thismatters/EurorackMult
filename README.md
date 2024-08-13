# Signal Multiplier

The signal mulitplier, as the name implies, multiplies signals. This module is an active mult, meaning that the input signal is buffered and the output duplicate signals are also individually buffered to ensure the signal is faithfully duplicated.

This is an original design featuring a three-layer stackup with a front face, a layer for all the jacks, and a power/processing layer where all the SMD components are layed out.

As with other modules in this line, this mult features:
* Polarity protection so that a backward power header doesn't fry anything (twin series schotty diodes: BAT54SL),
* Full surface mount design.

The KiCAD project here uses the library/footprints [found in my companion repo](https://github.com/thismatters/EurorackKiCAD).

## Width

11hp on an [Intellijel 1U rack](https://intellijel.com/support/1u-technical-specifications/).

## Inputs

There are two signal jacks, the lower one normals to the upper.

## Outputs

There are six output jacks with the top set being fed by the top input, and the bottom set being fed by the bottom input. If there is no jack plugged into the bottom input socket then the bottom outputs will output the upper input's signal.

## Adjustment

No adjustment required.


## Vendors

There are part numbers in the [BOM](mult.csv) for many of the parts (not for basic passives though) at the following vendors:

* [Mouser](https://www.mouser.com): Needs no introduction. Get your ICs from here (or [digikey](https://www.digikey.com)).
* [Tayda Electronics](https://www.taydaelectronics.com/): Good supplier for passive components; audio jacks, and potentiometers. Their audio jacks are slightly smaller than the thonkiconn from thonk.
* [Love My Switches](https://lovemyswitches.com/): Has [really good knobs](https://lovemyswitches.com/anodized-aluminum-knob-the-lo-fi-1-4-smooth-shaft-12-5mm-od/) to go on those potentiometers!
* [OSHPark](https://oshpark.com/): Fast and (relatively) cheap PCB manufacturer. I haven't done a prototype run yet... stay tuned.


## Versions

### V0

#### Bugs
* This version was kind of a mess. To fix, remove first three pins from both TL074 ICs. Omit R3, R4, R8, and R9. Bridge pad 1 of U1 with the pad of R3 closes to the center of the module. Bridge pad 1 of U2 with the pad of R8 closest to the board edge.