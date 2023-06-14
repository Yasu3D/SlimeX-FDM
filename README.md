### !! This case was designed for specific parts, check [Guides](/#-guides) for more info. !!
 
 It *may* fit other parts, but those setups are neither tested nor supported.

# 🦈 SlimeX-FDM
![woa cool animation](/Docs/explodeView.gif)
> woa cool animation

An easy to print, clean and very compact case design for SlimeVR.
Based on GniloAloe's SlimeX case, which is based on StonX.

Gniloe's design was intended for SLA printers. SlimeX-FDM is an adjusted version designed to be easier to print on FDM machines.

# ⚠️ Battery Safety Warning
- ***ALWAYS** separate the battery from the circuit boards to protect the battery from being poked by solder joints. Use a piece of craft foam or the provided 3d-printable battery-protector plastic card.*

- *Don't use V1 if you have battery tolerance issues!*

- *This case design is a **very** tight fit and may put a considerable amount of pressure on the battery if assembled incorrectly.*

- *Always ensure that your battery is safe and not a bomb please. I do not want to be held accountable for exploding trackers.*

# 📄 Changelog
| Version | Changes |
| - | - |
| V1 | Base Design |
| V2 | More space for battery, slightly larger I2C port |
| V3 | Complete remodel in Fusion360, .step file now available |
| V3.1 | Improved the clips, cases should stay together better now. |

# 📝 Guides
Always refer to the [SlimeVR Docs](https://docs.slimevr.dev/index.html) for the most up-to-date information. If you have any questions, ask in the [SlimeVR Discord](https://discord.gg/SlimeVR), DM me on Discord [Yasu#4645] or send me an [E-Mail](mailto:contact@yasu3d.art)

## Parts
SlimeX-FDM was designed around these parts. Resistors and Diodes obviously fit as well.
 - Wemos D1 Mini V4 Wifi Board // [Aliexpress](https://www.aliexpress.com/item/1005004605967379.html)
 - TP4056 USB-C Charger Board// [Aliexpress](https://www.aliexpress.com/item/1005004427739715.html)
 - SS22F32 Switch // [Aliexpress](https://www.aliexpress.com/item/1005003660190950.html)
 - BMI160 IMUs // [Aliexpress](https://www.aliexpress.com/item/4000084874141.html)
 - 804040 Li-Po Batteries // [Aliexpress](https://www.aliexpress.com/item/4000036291424.html)
 - 28AWG stranded silicone wire
 - [JST 1mm 4-pin / JST SH 4-pin connectors](https://jst.de/product-family/show/65/sh) for auxillary trackers // [Aliexpress](https://www.aliexpress.com/item/1005004350939786.html)

> please note that the Aliexpress pages are only for reference. It's recommended to look for other offers yourself.

> if any page is unavailable, the part name should be enough to find them.

> 1mm JST connector cables rarely come in lengths longer than 15cm. The linked page offers up to 30cm.

## 3D Printing
### Config
***TL;DR** 0.4mm nozzle, 0.15mm layers, 15% gyroid infill, arachne.*

Full config (that's been successful for me) can be found [here.](/Docs/SLICERCONFIG.md)

### Orientation/Arrangement
All STL files are exported in their correct orientation. The hollow inside of each case piece should point up:
![print orientation](/Docs/print_orientation.png)
> This allows the case to be printed with minimal supports.

### Supports
If possible, use support-painting and organic supports with a slicer like PrusaSlicer 2.6.0.
This makes support material less wasteful and makes removing supports an absolute breeze.

![supports1](/Docs/support_paint_top.png)
> supports under the I2C interface for auxillary trackers

![supports2](/Docs/support_paint_bottom.png)
> supports for bridges around strap slots + support for bridge around switch.

> support painting on bottom shell is symmetrical.

## Soldering
//TBD, check smeltieVR's guide "Soldering for dummies" to learn the basics.

## Assembly
### Closing an empty case
- Line up pegs with switch slot
- Hook one clip into a slot
- Push halves together, slowly increasing pressure until it snaps shut.

![its as shrimple as that](/Docs/assemblyIRL.gif)

### Assembling a full tracker (refer to animation for visual guide)
**Battery:** (bottom case)
- Place battery in bottom case. May require a little pushing to move the circuit board at the top of the battery. That's fine.
- Route the battery cable in a way that it pokes out on the right side of the switch slot.

**Boards:** (top case)
- Place the BMI160 in the top right corner, make sure that it is laying flat or as flat as possible. Bend wiring if necessary.
- Push TP4056 and Wemos D1 Mini into the bottom half of the case. They're a very tight fit and assembly might be tricky because of the clips, wiring and pegs. Patience and some pressure is key to get them in their spot.
- Make sure the TP4056 lies flat and that the USB-C port is almost flush with the port on the case. If necessary, bend some wiring.
- Make sure the D1 Mini's I2C interface lines up with the port on the case. (the small cutout on one of the corners)
> - The D1 Mini's USB-C port does not poke out as much as the TP4056. That's normal, you'll still be able to access it.
> - The D1 Mini's I2C interface should line up, even if the tracker won't be used with an auxillary tracker. That's because the USB-C port may be too far in to properly access and because the pegs the D1 Mini sits on may not align.
> - It sometimes takes a considerable amount of force to get the D1 Mini in place. It feels a little scary, but it's normal.

**Switch:**
- Place the switch on the pegs, not in the slot. This is to ensure alignment when closing the case.
- If your wiring is too long the switch may become temperamental and will jump off the pegs. Press it down and optionally tape it to show it who's boss and put it in it's place.

**Closing:**
- Same process as an empty case, but this time you have to do it with a bunch of components in the way.
- Make sure nothing's poking the battery
- Make sure nothing's in the way of the switch and clips.
- Conglaturations! You did it :3

[May your trackers be many and your drifters few.](https://www.youtube.com/watch?v=CgHS1fa69aU)

![woo other cool animation](/Docs/assembly.gif)


## Disassembly
If you need to troubleshoot or maintain your trackers, they're easily opened with the flat end of tweezers or a butter knife. Be slow to ensure you don't break anything.
- Hold case gentle like hamster
- Gently push against one of the clips inside the strap slots
- Apply a little force upwards with your fingers until case pops free.
 
Mind the cables and battery. You can carefully open the tracker like a book along the top edge (where the switch is).

![disassembly IRL](/Docs/disassemblyIRL.gif)


## Durability
Standard PLA(+) is recommended. ***Don't use silk PLA.***
If your filament is brittle, the clips *may* break. 

I durability-tested with silk and non-silk PLA+ and the clips on silk cases snapped with minor force applied. I couldn't even break a non-silk clip so far. (I've tried about 5 times with all my strength. It just doesn't want to break.)

If you repeatedly open and close a case (20+ times), you ***will*** shave off the small hooks that make the clips work properly. Once worn down, the case will still stay together but can easily be opened by pulling the two halves apart. This may be fixed in a design revision, but it's hard to find a balance between ease of use and durability for the clips. Just press against the clips and open them slowly, then you'll be ok.

I've also stood on top of a case (~85kg) and it didn't even buckle much lol. You'll be fine laying on one if your bed isn't made of concrete.
