---
title: Temperature comparer
draft: false
tags:
  - ESD
  - projects
---
# Purpose
I do not like paying for air conditioning. Instead, I try my best to open the windows when it's cooler outside than it is inside, and I close the windows when it's hotter outside than it is inside. Currently, the best way I have to compare the outdoor and indoor temperatures is by using a heat gun to measure the indoor temperature and checking a weather app to get the outdoor temperature. This project uses a simple circuit to notify me if the temperature outside is hotter than it is inside, thereby letting me know when to close the windows.

# Project complexity
Normally, a sensor's reading is measured by putting it in series with a resistor and measuring the voltage at the midpoint. One of the issues I with thermistors though is that they are not all that accurate, requiring tuning to get accurate temperature readings. This is complicated, and I looked up ways to circumvent this. A [video by Texas Instruments](https://www.youtube.com/watch?v=i4a9RkVUgIw) suggests replacing the resistors in the voltage divider with a constant current source to reduce error, but I am unfamiliar with creating constant current sources and I would have to make a current mirror to keep the current matched for the indoor and outdoor thermistor. Furthermore this doesn't "tune" the thermistors at all. Another idea that I thought of is using a resistor with one thermistor, and using a potentiometer on the other. Since I am not looking for accuracy but instead just a comparison, I could turn the potentiometer until the voltage dividers see the same voltage at room temperature.

# Circuit diagram for testing
I designed a dead simple circuit using NTC thermistors (see the circuit diagram to the right). I then tested this circuit on a breadboard and found that it works. The bill of materials is as follows:
- 1x LM393P comparator
- 1x LED
- 1x 1.5kΩ resistor
- 2x 10kΩ resistor
- 2x 10kΩ NTC thermistor
- Power supply (5-9V)
- Wires
![[Temperature Comparer-1781839364404.webp]]
![[Temperature Comparer-1781839374206.webp|200]]![[Temperature Comparer-1781839385029.webp|200]]![[Temperature Comparer-1781839394501.webp|200]]

# Perfboard and installation
With the circuit verified, I transferred the circuit onto a perfboard for a more permanent solution. I then mounted it to a wall with a pushpin and ran the outside temperature sensor through the brushes between the sliding windows to mount it outside.
![[Temperature Comparer-1781839450379.webp|200]]![[Temperature Comparer-1781839470682.webp|200]]![[Temperature Comparer-1781839430397.webp|200]]

​

The problem with all these solutions though is that they add complexity. Furthermore, I'm lazy, so I went with the simplest solution of using a thermistor in series with a resistor for both sides. Improving the accuracy of these sensing circuits is one way that this project can be improved in the future.