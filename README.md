# LAB 4

This lab serves as an introduction to utilizing PWM and Timers on the MSP430FR2355 Microcontroller. In this lab, we will explore the WDT timer interrupt process, as well as implementing PWM signals at various duty cycles and periods.

# Question 1

In the first part of this lab, we will follow the WDT timer interrupt process to toggle the an LED on the MSP430 board. For this part, we will toggle the green LED with a 250msec interval. The following figure shows the code used for this to achieve this:

![image](https://user-images.githubusercontent.com/85361948/206021495-2e7b0023-3e4c-4c22-881c-7b14482310ca.png)

Referencing the code above, the first line in main established the WDT to 250ms. We then assign Pin 6.6 on the MSP430FR2355 as an output. In the last part of the code, we enable an interrupt and performed the XOR bitwise operator on Pin 6.6.

# Question 2
In part 2, a PWM signal with a 10% duty cycle and a 500ms period using the polling process. The duty cycle can be calculated by finding the ratio of TB0CCR1 / TB0CCR0. TB0CCR0 can be calculated by multiplying the clock frequency chosen by the period. The clock that was chosen was the auxilary clock which has a frequency of 32.768 kHz. When multiplying this frequency by the 500 ms period, TB0CCR0 will contain a value of 16,384 Hz. TB0CCR1 can now be calculated by multiplying 16,384 Hz by the 10% duty cycle, which will result in a value of 1638.4 Hz.When visualizing this PWM signal on the oscilloscope, the duty cycle was at 10% and the period was at 500.6 ms. 

<img width="376" alt="Q2 CHART" src="https://user-images.githubusercontent.com/98994111/200406540-491f6b27-6d3a-432b-85b5-0263feaf3726.png">

![001](https://user-images.githubusercontent.com/98994111/200408272-de1623a4-6c35-4c68-847a-537064c6e161.jpg)

![LAB 4 Q2 - POLLING](https://user-images.githubusercontent.com/98994111/200405999-01542d7d-7e78-4bf3-a0a4-2bbd8939e4cf.png)

![IMG_1494](https://user-images.githubusercontent.com/98994111/200368912-0060acf2-1000-4ae3-bf50-a5eaddc772e8.jpg)


# Question 3
In the third part of this lab, we are tasked with generating another PWM signal but this time with a 20% duty cycle and a 250ms period. Similar to part 2, we use the same auxilary clock frequency of 32.768 will be used. When following the same approach of calculating TB0CCR0 and TB0CCR1, we get values of 8192 and 1638.4 respectively. The following figure shows the hand calculation used for this test:
![002](https://user-images.githubusercontent.com/98994111/200408518-a6219216-74bb-42cf-a7b3-ed462ec80b21.jpg)

The following figure shows when analyzing the PWM signal on an oscilloscope. When reading the oscilloscope, we can see a duty cycle of 20.01% and a period of 250.3ms:

![LAB 4 Q3 - POLLING](https://user-images.githubusercontent.com/98994111/200408652-72a16f32-1228-4351-be7c-aed5e1b8570b.png)
