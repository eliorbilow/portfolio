---
title: Sound Effect Button
draft: false
tags:
  - ESD
  - pcb-design
  - product-design
  - 3D-printing
  - projects
---
YouTube: [https://www.youtube.com/watch?v=fGJMsBuuvgI](https://www.youtube.com/watch?v=fGJMsBuuvgI)  
Thingiverse: https://www.thingiverse.com/thing:7169223

# Overview
There's a meme where someone is smashing a button with some kind of annotation on it. I wanted to make that meme in real life. In particular, I wanted to make the button make the "bonk" sound effect so my D&D group could use it when someone got hit in the campaign. I did not find any videos on how to do this in a simple project, so I had to design my own solution.
![[Sound Effect Button-1781704399027.webp|400]]
![[Sound Effect Button-1781704445146.webp|200]]![[Sound Effect Button-1781704449850.webp|200]]

# Component Selection
I wanted this to be a simple project that anyone could do and that didn't take much skill to put together. Therefore, I tried to minimize the number and cost of the components. In the end, the Bill of Materials consists of only a handful of parts:
- DFPlayer Mini and SD card
- Pushbutton
- Speaker
- 9V battery and connector
- Voltage regulator
- Wire/Dotterboard
The heart of the project is the DFPlayer Mini, which is essentially the computer and amplifier for an MP3 player. It also only costs $2-4.

![[Sound Effect Button-1781705390903.webp|200]]![[Sound Effect Button-1781705415379.webp|200]]
# Schematic and breadboard
Using the datasheet for the DFPlayer Mini, I found that I needed to use a voltage regulator in the final product because it only accepts 3.2-5VDC as input voltage. I also learned that by grounding the ADKEY_1 pin, I could play the first (and only) track that would be stored on the SD card, which would contain our sound effect.
![[Sound Effect Button-1781705737266.webp]]
![[Sound Effect Button-1781705754173.webp|400]]

# PCB
I designed the circuit using KiCad and designed a PCB, which I ordered 5 of from PCBway. To my surprise, the boards worked on the first try!

![[Sound Effect Button-1781705816337.webp|400]]

# Skeleton assembly
With the PCBs made, I assembled a clean version for the internals of the Bonk Button.

![[Sound Effect Button-1781705863790.webp|200]]![[Sound Effect Button-1781705856630.webp|200]]

# Housing
I wasn't happy with just having a skeleton of a button. I wanted something I could smash with my fist! So I made a 4-part housing assembly using Fusion 360 and a 3D printer. The features that I'm most proud of are the compliant mechanisms built into the housing like the spring and the snap-fit. I am also proud of the integration with how the switch can be screwed in.

Some things I learned were how to design for the button not being centered (creating a circular extrusion to contact the button, Image 1), how to let the speaker not be muffled by putting in the box (adding holes and feet to the base, Image 2), designing snap-in-place parts (Images 3 and 4), designing so that the parts can be assembled and disassembled easily (by adding notches to the outer housing to be able to pull apart the snap-fit parts easily, Image 5), and tolerancing to achieve a satisfying fit.​

In the images, you can see how the design progressed from the first version on the left to the final version on the right.
> [!info]- Click to see images of the housing
> ![[Sound Effect Button-1781705992150.webp]] ![[Sound Effect Button-1781705992155.webp]]![[Sound Effect Button-1781705992154.webp]]![[Sound Effect Button-1781705992152.webp]]![[Sound Effect Button-1781705992153.webp]]

# Circuit Board Upgrades
Based on feedback from a tester, I modified the circuit board to allow jumper pins to be soldered onto the board in place of the wires that would go to the speaker, battery, and on/off switch (oh yeah, that was also something that the tester thought of). The pins allow the components to be taken apart easily for situations like charging the battery.

In the first update, I didn't account for the width of the battery properly, so the assembly didn't fit and I had to shift the pin locations on the third board.

![[Sound Effect Button-1781706094490.webp|300]]![[Sound Effect Button-1781706108168.webp|300]]

  

# Assembly, current state, next steps
With the new board and the finished housing, I have a minimum viable product. It is fun to press, loud, and user-friendly.

If I were to upgrade this, I would remove the DFPlayer Mini and add bluetooth and flash capabilities to allow the user to upload MP3 files to the board instead of needing to pop out the SD card.
![[Sound Effect Button-1781706153655.webp|500]]![[Sound Effect Button-1781706173984.webp|500]]![[Sound Effect Button-1781706215655.webp|500]]


If the draft box is checked, it will not be shown on the site.
The "Title" property is what will be displayed on the website, not the name of the note.

Using this information, I created a schematic and tested the circuit on a breadboard (though I used a power supply instead of a 9V battery with a voltage regulator). To my pleasure, the circuit worked!