---
title: GPIO
---

The Arduino allows you to connect your kit to your own electronics. It has 14 digital I/O pins, and 6 analogue. The analogue pins can read an analogue signal from 0 to 5V. The board also has a couple of ground pins, as well as some pins fixed at 3.3V and 5V output.

The pin layout of the servo assembly is the same as an Arduino uno.

![Pin Map](https://raw.githubusercontent.com/Bouni/Arduino-Pinout/master/Arduino%20Uno%20R3%20Pinout.png?width=50pc)


{{% notice note %}}
The servo hat communicates with the Arduino using two of the analogue input pins (4 and 5) and it communicates with the Pi using 2 of the digital IO pins (0 and 1), so these four pins are reserved. Using these pins will cause the servo hat to behave unusually.
{{% /notice %}}