# triplejump

Leverless (box-style) fighting game controller with three jump options.

> TODO: One or more images

## About

This controller is distinguished by its split-hand configuration and angled keyclusters, mitigating the RSI-potential of the standard "hands-together-but-parallel" layout popularized by the Hitbox. The goal is to keep the entire device relatively small while still providing a meaningful ergonomic benefit.

> [TODO] Dimensions of the assembled device are LxWxHmm, approximately the size of a [FIXME].

Another unusual aspect of the layout is the 10 button right hand cluster. The closeness of the keys in this keyboard-like format makes multi-key inputs (e.g., `LP+LK`) harder than usual to press. Promoting `R3` and `L3` into "first class" buttons mitigates this drawback by providing more locations for macros.

Lastly are the titular three up buttons. Really, this is just for player comfort. Some prefer a `WASD` jump and others prefer a thumb jump. If concerned about being DQ'd for having more than one (i.e., under CPT rules), just remove remove the two switches you don't personally use.

Powering this device is OpenStick's excellent [GP2040-CE](https://github.com/OpenStickCommunity/GP2040-CE) gamepad firmware. Please see that repository for information about console compatibility, configuration, and all the rest.

## Creation

If you want to produce one, you will need some parts. Note that anywhere a quantity of `14-16x` is listed, the number you need will depend on how many `Up` buttons you intend on installing.

### PCB

- 1x triplejump PCB, created using the [gerber.zip](./prod/gerber.zip) files with an online PCB prototyping service. I \[intend to have\] used [JLCPCB](https://jlcpcb.com/).
- 1x [RP2040-Zero](https://www.waveshare.com/rp2040-zero.htm).
- 6x 6x6mm Panel PCB Momentary Tactile Mini Push Button Switch DIP 4pin.
- 14-16x Kailh Choc v1 Hotswap Sockets (PG1350).

### Keys

- 14-16x Kailh Choc v1 Switches (recommended: linear switches with low actuation force).
- 14-16x Kailh Choc-compatible Keycaps.

### Case [NYI]

- > [TODO] 3D Printed Case [Top](./prod/NYI) and [Bottom](./prod/NYI).
- > [TODO] Nx M3x? Screws.
- > [TODO] Anything else? Brass inserts? Nuts? Magnets? TBD.
- OPTIONAL: Non-slip Feet or Pads.

### Assembly

- Soldering Equipment.
- Screwdriver.

### Firmware [NYI]

- The [Latest GP2040-CE Release](https://github.com/OpenStickCommunity/GP2040-CE/releases).
- > [TODO: Can I just provide a config file?] Button Mapping using GP2040-CE's Web Interface.

## Hacking

Here are some ideas for mods that should be fairly straightfoward, if you want to fork this project:

- Changing from Choc keyswitches to standard MX-style switches "should" be a simple operation, because I used MX-standard 19.05mm switch spacing everywhere.
- Case could surely use some improvement, this was my first time designing or 3D printing anything.

## Acknowledgments

- [GrooveBob](https://github.com/GroooveBob)'s [Stress](https://github.com/GroooveBob/Stress), which helped inspire this design.
- [jfedor2](https://github.com/jfedor2)'s [Flatbox](https://github.com/jfedor2/flatbox), which helped inspire this design.
- [Afternoon Labs](https://github.com/afternoonlabs)' [Breeze], which helped inspire this design and whose switch layout it mimics.
- [ruiqimao](https://github.com/ruiqimao)'s [Keyboard PCB Guide](https://github.com/ruiqimao/keyboard-pcb-guide), which led me through the entire PCB creation process.
- [crides](https://github.com/crides)'s [Kleeb](https://github.com/crides/kleeb) Kicad library, whose symbols and footprints are present in the PCB schematic and design.
- [daprice](https://github.com/daprice)'s [keyswitches.pretty](https://github.com/daprice/keyswitches.pretty) Kicad library, whose footprints are present in the PCB design. [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- [OpenStickCommunity](https://github.com/OpenStickCommunity/GP2040-CE)'s [GP2040-CE](https://github.com/OpenStickCommunity/GP2040-CE), whose firmware makes the silicon useful and whose Discord community was extremely helpful.
