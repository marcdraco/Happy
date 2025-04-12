Break out one of multiple JFETs from the 2N4416 to the 2SK208 and LSK170.

Production gerbers and KiCAD 8.x (or later) files attached. 

![image](https://github.com/user-attachments/assets/6ca5398a-6c80-417e-936c-5a5df1fa58a4)
![image](https://github.com/user-attachments/assets/837431be-d6cc-4f81-910f-0d1f8e1b941b)

Quick update to the readme - Happy can also be pressed into service as a conventional "electret with FET" by shorting the source pin to the ground - there's a ground where the Gate terminal might have an 0805 resistor which makes a conveninet point to solder a small piece of wire (the end of an 1/8W resistor for example) causing the board to behave like --- well one of those "out of a cornflake packet" electrets you get on eBay for under £1 but with performance far exceeding that even the best; for weample the Pandasonic WM61A capsules because youu can mount JLI2555 on there.

You'd wire it exactly per existing drawings. Normally 2-10V is applied to the FET via a 2K2 resistor (to the drain) and the signal is tapped off from a capacitor attached at the Drain terminal.

This is "common source mode" as described by Mr. Linkwitz here: https://www.linkwitzlab.com/images/graphics/microph1.gif (before the modification).

Linkwitz suggests putting the capsule into common drain (power direct to the drain tap) and putting resistor from source to ground. If you're doing this mod, it's worthwhile using a higher gain JFET (2N4416, LSK170a, 2SK209 and so on) as  FET switches, which will work, won't give a much signal in either combination. The Vgs (off) pinch-off is important too. JFETs like the 2N3819 require a fair amount of negative voltage to operate and won't perform well in this board.
