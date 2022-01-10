# genie-dry-contact-adapter
Push-Button Adapter for Series III Compatible Genie Garage Door Openers

KiCAD project for a clone of the [Genie Series III Dry Contact Adapter](https://store.geniecompany.com/products/series-iii-dry-contact-adapter-switch)

# Background
After purchasing a Wifi controller for my garage door opener, I realized that my opener did not have a standard push-button ("dry contact") input.
I investigated how my existing [wall console](https://store.geniecompany.com/products/copy-of-wall-console-for-series-ii-product) operated and discovered that it provided three different signals depending on the button that was pushed (DOOR, LIGHT, or LOCK).
The opener provides a soft ~15V to the wall console, and the wall console shorts this signal at a low duty cycle (~10%).  The approximate frequency for each button is as follows:
* DOOR: 16kHz
* LIGHT: 8kHz
* LOCK: 4kHz

The opener detects the frequency of the short and is able to determine which button is pressed.
I was only interested in the DOOR signal, so I simplified the circuit, but a full schematic of the wall console is provided for convenience.
I also discovered that the wall console itself was a dry contact adapter, as it had two-through hole pads in the circuit board that were in parallel with the DOOR button.

# Fabrication
While I initially breadboarded the circuit, I wanted a PCB.
Using [JLCPCB](https://jlcpcb.com), I was able to get five populated/assembled boards delivered for less than $20, not including the [screw terminals](https://www.amazon.com/gp/product/B07H5G7GC6), which I installed myself.
That is much less than a single ~$50 adapter (or ~$30 wall console) sold by Genie, especially given that I have two garage doors.
