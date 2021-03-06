## RJ45 Breakout board ##

This is a break out board to be mounted onto the print head to be able to use a standard ethernet cable to connect low power parts, namely:

![](https://github.com/RURon/Vcore-Mods/blob/main/RJ45%20Breakout/RJ45_Adapter.png)

- Thermistor
- 3 wire probe (I use a VINDA that needs 5V, GND and Signal)
- Hotend and Coldend fans (I use 12 V variants here)
- 12V LED strip (I created a special fang that has space for a little 12V LED strip to illuminate the nozzle area)

If you use this mod, make sure to check the connection of the wires thru your cable - there are crossover cables or maybe even non standard RJ45 jacks. I would advise to check the connection from start to end using a multimeter before you power up! Of course you could connect your wires differently than I do, but this is my connection:
RJ45
P1	GND
P2	5V
P3	LED GND
P4	Probe Signal
P5	Thermistor
P6	12V
P7	Partfan GND
P8	Coldend GND

The LED and the fans share the +12V line so you could connect the 12V to 24V and leave out the LED connection in order to stick to 24V fans.
The probe I use uses 5V - the 5V line in the adapter is only connected to the probe so you could provide your probe with anything else as well.

This makes is easy to replace eventually broken cables with a simple patch cable that you can buy anywhere. Currently, I use a 70cm long cable.
On the printer side you will either need another of the pcb or for example the Adafruit RJ45 Magjack breakout board (which I use, but I had to remove the magjack and replace it with a standard RJ45 jack) or your own solution (like you could cut a cable and simply connect the wires to your board). I included the two 3030 mounts for the first 2 mentioned variants.

My strain relief replacement features side ways cable management "wings" that might be helpful but you could do without them probably.

On my VCore-3 300 I found out a 65cm long Ethernet cable works best. Patch cables vary in actual length compared to nominated length - this 65cm cable that I use is sold as 50cm length! Here is the link to my specific model: [Amazon link, no affiliate](https://www.amazon.de/gp/product/B07S9SZB9L)

In case you want to fabricate your own pcbs, you could try using the included zip file with all Gerber files, which is compatible with Aisler and also Jlcpcb

My own produced PCBs had a design flaw: The Fusion360 Eagle connector library has mistakes in the XH connectors. This leads to too small holes for the connector pins. I fixed this in the provided Gerber and Eagle files but in case you got the same problem, you can sand/file down the XH pins a little (to make their crosssection round instead of square) so that they fit more easily.
