# plotter

DIY LY Drawbot Pen Drawing Robot Lettering Corexy Normal Version A4 A3 Engraving Frame Plotter Robot Kit for Drawing Writing

This has Nema 17 steppers

https://components101.com/motors/nema17-stepper-motor

Specifically in idraw_conf.py I use the following

```
SL42STH34-1334A
NEMA 17 : Steps per inch = (200 * 16) / (1.8 degrees per step) = 1777.78
DPI_16X = 2489

```

3555  # ~= 1777 *2 was way too big.  I settled out at about 88.8/cm 

----

In ddraw (inkscape extention), I use 
* Pen Height Up: 25
* Pen Height Down: 65
* Laser Power: 100

----

No instructions were not in the box. This seems to be a FAQ for the sellers, and they advise that customs often does not allow the USB device that is part of the shipment

Contacting the seller via Aliexpress got me a link to a google drive with instructions including Inkscape setup for the most part.

The instructions were clean when scanned via Virus Total

The PDF's had mostly chinese text in them. Not too bad. The pictures were more than enough to get things set.

I did have a few things that I assembled, disassembled, and reassembled. No big deal, just dont tighten everything a ton until you are done.

----

The instructions are pretty good overall.

----

Alignment was challenging and took a bit of time. Here are some tips based on my experience.

First, do initial assembly and testing to make sure things are working.

To do alignment
* move carriage to the center, all axis
* loosen the bolts that hold the carriage to the rail, yes all of them
* Mark a location on the y-axis, I used blue masking tape and 23 cm from the rail end.
* Use zip tie to hold that location
* Tighten belts making sure they are properly on the bearings/rollers at each step
* Do final belt tightening
* Do final carriage bolt tightening
* remove the zip ties (or whatever you need to to to release the carriage)
* Do micro adjustments as necessary
* Test, repeat as necessary

----

I wasnt able to get it to work with any software other than what was provided.

I was able to export svg from Drawbotv3 and use that in inkscape (import).

I have since collaborated with Github Copilot to create a few scripts that have been helpful for me.

The first is https://github.com/furryalien/EggBot/tree/master/other/jog-control which is very helpful for moving the carriage around when testing stuff.

The second is the collection in here https://github.com/furryalien/EggBot/tree/master/other/gcode-plotter 
* The calibration script was very helpful for adjusting and learnings what was going on.
* The gcode script makes it so I can use gcode from just about anything with the plotter. It mostly uses the gcode for the path since there is only up and down for the z-axis. This is very useful since then I can use Drawbotv3 to generate the gcode and then just run it here. It suits my workflow nicely.

----

The board is a clone of EiBotBoard https://www.schmalzhaus.com/EBB/ 

The board was able to be flashed with the latest EBB firmware via https://wiki.evilmadscientist.com/Installing_software

----

clamps for the belt

I didnt like that it wanted me to use zip ties so I used binder clips to start with. Even after tweaking I still didnt like it. I looked at a few different 3d printed options, but didnt want to mess with that. So I kept thinkging about it. I wanted something that could work like a hinge so that it would pinch and release as necessary. There are a few 3d printed models that were close to this but not exactly what I wanted. After ruminating for a bit I remembered that I had a number of old bicycle chains, and that when disassembled, the links could be connected with M3 bolts and nuts to create a pinch point so thats what I did. They work well.

----

belt tensioning

I was watching the plotter the other day and I was noticing that the belts were bounding around quite a bit. So I thought that they needed retentioning, so I did that. Then plotting again I noticed the same belt bouncing. I ordered some of the spring tensioners and was impatient and not convinced that I thought those would be best since they are designed to go in the working areas of the belt. Thinking a bit more, the pen carrier has the belt ends nicely aligned end to end. So potentially something that can tension the belt, end to end could work. I intitially thought about having a spring between the ends and I think that would work. I didnt have any springs, so Im initally trying rubber bands and zip ties to connect the ends across the carrier. The initial setup of this works and I can see that the belts are more tensioned. Functional test looks good. 

Here is an image of these two belt related mods.
<img width="1086" height="683" alt="image" src="https://github.com/user-attachments/assets/5ad4cc84-5cf1-4043-b897-d59654be493c" />

