# triplejump

Leverless (Hitbox-style) fighting game controller with ~~three~~ two jump options.

`TODO: One or more images`

## About

This controller is distinguished by its split-hand configuration and angled keyclusters, mitigating the RSI-potential of the standard "hands-together-but-parallel" layout popularized by the Hitbox. The goal is to keep the entire device relatively small while still providing a meaningful ergonomic benefit.

Another notable aspect of the layout is the 10 button right hand cluster. The closeness of the keys in this keyboard-like format makes multi-key inputs (e.g., `LP+LK`) harder than usual to press. Promoting `R3` and `L3` into "first class" buttons mitigates this drawback by providing more locations for macros (the legal kind you can map in-game).

Lastly are the titular ~~three~~ two up buttons. This allows the same handed-preference for jumping (and ability to double-tap using both thumbs) from the normal layout.

Powering this device is OpenStick's excellent [GP2040-CE](https://github.com/OpenStickCommunity/GP2040-CE) gamepad firmware. Please see that repository for information about configuration, console compatibility, and all the rest.

## Creation

If you want to produce one, you will need some parts.

### PCB

- 1x triplejump PCB, created using the [gerbers.zip](./prod/gerbers.zip) files with an online PCB prototyping service. (e.g., [JLCPCB](https://jlcpcb.com/).)
- 1x [RP2040-Zero](https://www.waveshare.com/rp2040-zero.htm).
- 5x 6x6mm Panel PCB Momentary Tactile Mini Push Button Switch DIP 4pin.
- 15x Kailh Choc v1 Hotswap Sockets (PG1350).

### Keys

- 15x Kailh Choc v1 Switches (recommended: linear switches with low actuation force).
- 13x Kailh Choc-compatible 1u Keycaps.
- 2x Kailh Choc-compatible 1.5u Keycaps.

### Case

This case was designed with MBK profile Choc keycaps in mind and may or may not be compatible with other keycaps.

- Laser Cut Acrylic Layers: [Bottom](<./prod/case_layer0_1.5mm.dxf>), [Lower-Middle](<./prod/case_layer1_3mm.dxf>), [Upper-Middle](<./prod/case_layer2_4.5mm.dxf), [Top](<./prod/case_layer3_1.5mm.dxf>)
  - The filenames include how thick each layer should be.
  - The PCB goes between the two middle layers.
- 6x M3 x 12mm Bolts.
- 6x M3 Threaded Heat Set Inserts.
  - Affixed in the top acrylic layer, screwed into from the bottom.
  - I used [these](https://www.amazon.com/gp/product/B077CL322T).
- OPTIONAL: Non-slip Feet or Pads.

### Assembly

- Soldering Equipment.
- Screwdriver.

### Firmware

- The [Latest GP2040-CE Release](https://github.com/OpenStickCommunity/GP2040-CE/releases), flashed accoridng to the documentation.
- Pin (Button) Mapping using GP2040-CE's [Web Configurator](https://gp2040-ce.info/#/web-configurator)
  - There is a catch: the firmware assumes a default pin mapping that the triplejump does not use. Until you've remapped the pins, you must hold down L1 instead of S2 (Start) when plugging in the controller to enter the configurator.
  - You could also short pin 1 to ground manually if you haven't installed the switches yet when setting up the firmware.
  - The correct mapping for the triplejump is shown below.

![](./images/pin-mapping.png)

## Acknowledgments

- [GrooveBob](https://github.com/GroooveBob)'s [Stress](https://github.com/GroooveBob/Stress), which helped inspire this design.
- [jfedor2](https://github.com/jfedor2)'s [Flatbox](https://github.com/jfedor2/flatbox), which helped inspire this design.
- [Afternoon Labs](https://github.com/afternoonlabs)' [Breeze](https://github.com/afternoonlabs/BreezeKeyboard), which helped inspire this design and whose switch layout it mimics.
- [ruiqimao](https://github.com/ruiqimao)'s [Keyboard PCB Guide](https://github.com/ruiqimao/keyboard-pcb-guide), which led me through the entire PCB creation process.
- [crides](https://github.com/crides)'s [Kleeb](https://github.com/crides/kleeb) Kicad library, whose symbols and footprints are present in the PCB schematic and design.
- [daprice](https://github.com/daprice)'s [keyswitches.pretty](https://github.com/daprice/keyswitches.pretty) Kicad library, whose footprints are present in the PCB design. [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- [Sadek Baroudi](https://github.com/sadekbaroudi)'s [Keyboard Case Design](https://kbd.news/Keyboard-Case-Design-1764.html) article, which showed the process for exporting the PCB into a form usable during case design.
- [OpenStickCommunity](https://github.com/OpenStickCommunity)'s [GP2040-CE](https://github.com/OpenStickCommunity/GP2040-CE), whose firmware makes the silicon useful and whose Discord community was extremely helpful.

