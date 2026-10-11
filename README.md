# Fishy8
PCB with vintage camera looking footage. A microphone and a fisheye lens.

Okay, name explained first
FISHeYe lens + hi8 = FISHY8!
Original name was FISH8 but FISHY8 sounds more jolly.

Why have i made it? Those old sony handycams are increndibly hard to get. Except if you live near the old camera market in barcelona (I still hate that it wasnt open when i was there.), so, why not make one that costs a one time payment of max 120 bucks, and doesnt require extra additions like those 100 dollar converters. but has a 15 dollar converter inside of it!

I got a fpv camera with fisheye built in, for easyness: footage looks like this:
<img width="1920" height="7863" alt="image" src="https://github.com/user-attachments/assets/74478870-7d0e-4082-aef5-84f7790e329f" />

so, allat of yap. what does it look like?

PCB
<img width="636" height="632" alt="image" src="https://github.com/user-attachments/assets/a4449cad-d76e-4f96-bfef-897f562eb91d" />

SCHEMATIC
<img width="585" height="535" alt="image" src="https://github.com/user-attachments/assets/db2e0249-a78b-42dc-9065-9c5d9ce463bd" />

3D
<img width="833" height="617" alt="image" src="https://github.com/user-attachments/assets/d011945b-770d-41d5-91ce-cfdaecef1cb7" />
ehh not the pretties, but gets the job done LOL!



I am planning to make a 3d print later on, zo the additional components can snap on!
It doesnt need any firmware, since android supports the gracetop cvbs to usb c natively.


BOM:

# FISHY8 — Bill of Materials

Power delivery, audio capture and module mounting have not yet been tested with physical hardware. Items marked “to be determined” are not final purchase selections.

## Complete modules

| Quantity | Part | Selected product / supplier link | Notes |
| --- | --- | --- | --- |
| 1 | Analog camera | [CADDX Ratel 2 Micro, original 2.1 mm lens](https://www.caddxfpv.com/products/ratel-2-1-1-8inch-starlight-sensor-freestyle-fpv-camera) | Complete camera; published dimensions: 19 × 19 × 20 mm. Select the Micro version. |
| 1 | USB-C video grabber | [GRACETOP rqrr322t CVBS to Type-C](https://www.gracetop.com/products/rqrr322t) | Use the selected module and its original four-wire harness. Available current from its 5 V camera supply is still unconfirmed. |
| 1 | Microphone and amplifier | [Adafruit 1063, MAX4466 Electret Microphone Amplifier](https://www.adafruit.com/product/1063) | Complete microphone module. The J3 pin assignment is specific to this board. |
| 1, included if supplied | OSD joystick | Original Ratel 2 menu board supplied with the camera | Confirm that the selected camera package includes it. Its original cable connects directly to the camera. |

## Components on the carrier PCB

| Reference | Quantity used | Part | Selected part / supplier link | Dimensions and electrical specification |
| --- | --- | --- | --- | --- |
| F1 | 1 | Resettable PTC fuse | [Bourns MF-R050](https://www.tme.eu/nl/details/mf-r050/tht-polimeer-zekeringen/bourns/) | 0.50 A hold current at 23 °C; 5.10 mm lead pitch. [Datasheet](https://www.bourns.com/docs/product-datasheets/mf-r.pdf). |
| R1 | 1 | Resistor | [SR PASSIVES CF1/4W-1K](https://www.tme.eu/nl/details/cf1_4w-1k/tht-weerstanden/sr-passives/) | 1 kΩ, 0.25 W, axial. The horizontal footprint uses 10.16 mm lead spacing. Check the supplier's minimum order quantity. |
| C1 | 1 | Ceramic capacitor | [Vishay K104K15X7RF5TH5](https://www.tme.eu/en/details/k104k15x7rf5th5/mlcc-tht-capacitors/vishay/) | 100 nF, 50 V, X7R; 5.00 mm lead pitch. |
| D1 | 1 | Red LED | [Kingbright L-934ID-TNB2.54](https://www.tme.eu/en/details/l-934id-tnb2.54/tht-leds-round/kingbright-electronic/) | 3 mm LED, 2.54 mm lead pitch. PCB pad 1 = cathode/GND; pad 2 = anode. |
| RV1 | 1 | Trimmer potentiometer | [Bourns 3296W-1-103LF](https://nl.mouser.com/nl/ProductDetail/Bourns/3296W-1-103LF?qs=CL3xLxiry19Id6AEaxYcng%3D%3D) | 10 kΩ, vertical 3296W version; pin 2 is the wiper. [Datasheet](https://www.bourns.com/docs/product-datasheets/3296.pdf). |
| C2 | 1 | Bipolar electrolytic capacitor | [Nichicon UES1C101MPM](https://www.tme.eu/en/details/ues1c101mpm/tht-audio-electrolytic-capacitors/nichicon/) | 100 µF, 16 V, diameter 10 mm, height 12.5 mm, lead pitch 5 mm. Use the **bipolar** part. |
| J3 | 1 | Straight female header | 1 × 3 contacts, 2.54 mm pitch, through-hole; supplier to be selected | Socket for the microphone module. Confirm header height and clearance beneath the module. |
| J4 | 1 | Straight male header | 1 × 2 contacts, 2.54 mm pitch, through-hole; supplier to be selected | Connection to the grabber's audio input. May be cut from a longer strip. |
| J1, J2 | 0 purchased components | Wire pads | Included in the copper of the custom PCB | Solder the original module wires to these pads. |

The microphone module also needs one straight **1 × 3 male header, 2.54 mm pitch**. Use three pins from the supplied strip if included. Add a separate header to the order only if needed.

## PCB, cables and mounting

| Quantity used | Item | Selection / status |
| --- | --- | --- |
| 1 PCB | Custom carrier PCB, two-layer FR4, 100 × 100 mm | Fabrication supplier and order quantity to be selected. Mounting is still unresolved; the board is not yet released for fabrication. |
| 1 | USB-C to USB-C data cable | Connects the grabber to the Pixel 9. Must support at least USB 2.0 data. Supplier to be selected. |
| 1 | Camera power/video harness | Use the original Ratel 2 harness; confirm that it is included. |
| 1 | OSD cable | Original cable between the menu board and camera; confirm that it is included. |
| 1 | Four-wire grabber harness | Must fit the grabber's original 1.25 mm connector. Confirm inclusion with the rqrr322t package and the exact pin assignment. |
| 1 | Female cable connector for J4 | 1 × 2 contacts, 2.54 mm pitch, with two wires for AUDIO_IN and GND. Connect these to the grabber harness. Supplier to be selected. |
| 1 set | Nonconductive 3D-printed module holders | For the camera, grabber and joystick, plus microphone support if required. Final designs and material quantities are still to be determined. |
| To be determined | Screws, nuts/inserts and spacers | Select after the holders and mounting method are defined. The Ratel uses M2 side screws; confirm safe screw length. |
| Small amount | Insulated wire, heat-shrink tubing and solder | Assembly materials. Keep the analog video connection short, with a nearby GND connection. Supplier and pack quantities to be selected if not already available. |

M1, M2 and M3 in KiCad are module reservation drawings. They are not additional purchased components.

The current design contains no battery, USB hub or additional test points. These are not included in the base BOM.

## Footprints used in the current schematic

| Reference | Footprint |
| --- | --- |
| F1 | `FISH8:MF_R050_P5.10` |
| R1 | `Resistor_THT:R_Axial_DIN0207_L6.3mm_D2.5mm_P10.16mm_Horizontal` |
| C1 | `FISH8:C_Vishay_K104K15X7RF5TH5_P5.00` |
| D1 | `FISH8:LED_Kingbright_L934ID_TNB2.54_P2.54_Drill1.20` |
| RV1 | `Potentiometer_THT:Potentiometer_Bourns_3296W_Vertical` |
| C2 | `Capacitor_THT:C_Radial_D10.0mm_H12.5mm_P5.00mm` |
| J3 | `Connector_PinSocket_2.54mm:PinSocket_1x03_P2.54mm_Vertical` |
| J4 | `Connector_PinHeader_2.54mm:PinHeader_1x02_P2.54mm_Vertical` |
| J1, J2 | `FISH8:WirePads_1x03_P2.54` |

The complete camera, grabber and joystick retain their own small PCBs. They are mechanically attached to the carrier PCB, with their external signals connected through wires.


