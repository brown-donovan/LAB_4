# LAB 4

This lab serves as an introduction to utilizing PWM and Timers on the MSP430FR2355 Microcontroller.

# Question 1

In the first part of this lab, we will follow the WDT timer interrupt process to toggle the an LED on the MSP430 board. For this part, we will toggle the green LED with a 250msec interval. The following figure shows the code used for this to achieve this:

![Lab4p1](https://user-images.githubusercontent.com/85361948/200364637-aa6fcca6-f80a-4ea1-919b-eef7aa2e79a6.PNG)

Referencing the figure above, lines 6 and 7 assign the output and select used for the green LED on the board. The following line configures our board to a low power mode used for the WDT Timer Process. The next snippet of code, lines 11-16 configure the PWM period and duty cycle for this question. The last part of the code uses a while loop to continue the blinking LED.

# Question 2
In part 2, a PWM signal with a 10% duty cycle and a 500ms period using the polling process. The duty cycle can be calculated by finding the ratio of TB0CCR1 / TB0CCR0. TB0CCR0 can be calculated by multiplying the clock frequency chosen by the period. The clock that was chosen was the auxilary clock which has a frequency of 32.768 kHz. When multiplying this frequency by the 500 ms period, TB0CCR0 will contain a value of 16,384 Hz. TB0CCR1 can now be calculated by multiplying 16,384 Hz by the 10% duty cycle, which will result in a value of 1638.4 Hz.When visulaizing this PWM signal on the oscilloscope, the duty cycle was at 10% and the period was at 500.6 ms. 

<img width="376" alt="Q2 CHART" src="https://user-images.githubusercontent.com/98994111/200406540-491f6b27-6d3a-432b-85b5-0263feaf3726.png">

![LAB 4 Q2 - POLLING](https://user-images.githubusercontent.com/98994111/200405999-01542d7d-7e78-4bf3-a0a4-2bbd8939e4cf.png)

![IMG_1494](https://user-images.githubusercontent.com/98994111/200368912-0060acf2-1000-4ae3-bf50-a5eaddc772e8.jpg)


# Question 3
