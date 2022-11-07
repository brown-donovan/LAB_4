# LAB 4

This lab serves as an introduction to utilizing PWM and Timers on the MSP430FR2355 Microcontroller.

# Question 1

In the first part of this lab, we will follow the WDT timer interrupt process to toggle the an LED on the MSP430 board. For this part, we will toggle the green LED with a 250msec interval. The following figure shows the code used for this to achieve this:

![Lab4p1](https://user-images.githubusercontent.com/85361948/200364637-aa6fcca6-f80a-4ea1-919b-eef7aa2e79a6.PNG)

Referencing the figure above, lines 6 and 7 assign the output and select used for the green LED on the board. The following line configures our board to a low power mode used for the WDT Timer Process. The next snippet of code, lines 11-16 configure the PWM period and duty cycle for this question. The last part of the code uses a while loop to continue the blinking LED.

# Question 2

![IMG_1494](https://user-images.githubusercontent.com/98994111/200368912-0060acf2-1000-4ae3-bf50-a5eaddc772e8.jpg)


# Question 3
