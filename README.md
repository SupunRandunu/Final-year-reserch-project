# Final-year-reserch-project
Home automation system with autonomous device identification 

#Introduction

Nowadays home automation is tending all over the world. Home automation system represent automation sensation and electronic control of devices to leads to ease and comfort lifestyle for each member at home. 
Home automation market rapid growth in the past decade. In 2023, there have 85 billion markets in the industry. But there are few solutions available in the market. But there are few solutions available in the market. The home automation industry has a good market opportunity to succeed.
 
In-home automation, electronic and electrical environments with respect to this context is an environment that consists of apparatuses such as Tv, HVAC system, radios, motors, AC systems, lighting systems, etc. A remotely accessible environment can assess appliances and can easily control appliances using a web interface.
The main issues of the home automation system are we can't directly identify devices using system. always need human interaction to assign devices to the system. the system cannot identify a frequent pattern of the user, user need to do same thing, again and again, every day. and also, the system should communicate with user friendly way, button click in not a good way.
Using artificial intelligence, need to address those issues that are happening in the home automation system. The target of the project is to embed artificial intelligence into home automation systems. The initial usage of the product is to act as an assistant of the users, control surrounding devices, understanding human speech, etc. The uses of this product will be home automation or industry automation. This home automation system can identify the devices from the voltage and current patterns. Users can switch on and off the devices from commanding to the computer using voice. 
The motivation of the project is that currently there are no such solutions available in the market and therefore need to build the product ourselves. In the long run, the product can potentially also can be commercialized and sell to the other service business in Sri Lanka or internationally. This project will give me an excellent view of how a software product implementation starting and how is the idea became to the actual productization.
The special component of this system is that, the system can identify which devices are connected to the system. To do that system collect device current and voltage consumption and cluster the data using different clustering algorithms. Smart plug develops to send current and voltage consumption of the device to the system. The controlling part of the System is mainly develop using a web interface.  Any person who is able to connect system can easily control home devices.


#Theoretical framework

This research consists with three sub parts

•	Device identification

•	Voice recognition system

•	Control devices

In this research, the most important part is identifying electrical devices form their power consumption. According to (BACURAU, 2015) , to identify the devices, power signature needs to calculate. Power signature can calculate using
•	Active power

•	Reactive power

•	Vrms

•	Irms

•	Phase Shift

##Power signature 

###Power factor

Power Factor used to measure, how effectively approaching power is used in electrical devices, it is defined as the ratio of Active power to Apparent power. Real Power (kW) is the actual powers the equipment performs useful, productive work. Figure 2.1.1 display how calculate   power factor using real and total powers.

###Active power 

Active power, True power or real power is the power that is actually absorbed or utilized in an AC Circuit. It is measured in kilowatt (kW) or megawatt (MW). It is the actual achievements of the electrical system which runs the electric devices.

###Reactive power
Reactive power is also called "phantom power", that occurs when the voltage waveform is out of phase (usually by 90 degrees if the load is purely reactive) with the current waveform of the voltage and is the result of either capacitive or inductive loads. Only when current is in phase with voltage is there actual work is done, such as in resistive loads
Reactive power is additionally "phantom power" because it isn't clear where it goes. The reactive loads such as capacitors and inductors don't scatter power in a sense that it is not utilized to power them but measuring the voltage and current around them shows the fact that they drop voltage and draw current. The power disseminated through this voltage drop and current draw is in the form of heat or waste energy and is not done as genuine work; hence engineers have locked for ways to reduce this. Because of this phantom power, conductors and generators must be rated and sized accordingly to carry the total current including the waste and not just the current that does the actual work.
Capacitors are considered to create reactive power, while inductors consume it. So when both are placed in the parallel association, the current flowing through them cancels out. This is essential when controlling the power factor of a circuit and has become a fundamental mechanism in electric power transmission. Including both capacitors and inductors in a circuit makes a difference in part compensate for the reactive power expended by the load.

###Apparent power 
The product of root means square (RMS) value of voltage and current is known as Apparent Power. This power is calculated in kVA or MVA.
It has been seen that power is utilized only in resistance. An immaculate inductor and an immaculate capacitor do not utilize any power since in a half cycle whatever power is received from the source by these segments, the corresponding power is returned to the source. This power that returns and flows in both the way in the device is named as Reactive power. This reactive power does not produce any useful work in the device.
In the immaculate resistive devices, the current is in phase with the used voltage, whereas in the pure inductive and capacitive circuit the current is 90 degrees out of phase. 
Hence, from the above all discussion, it is concluded that the current in phase with the voltage originates true or active power, whereas, the current 90 degrees out of phase with the voltage provides to reactive power in the circuit.               

###Vrms
The term “RMS” stands for “Root-Mean-Squared”. Most publications describe this as the “amount of AC power that generate the same heating effect as a similar DC power”, or something similar along these lines, but an RMS value is more than just that. The RMS value is the square root of the mean value of the squared function of the instantaneous values.
Another way, the effective value is an equivalent DC value which tells how many volts or amps of DC that a time-varying sinusoidal waveform is equal to in terms of its capacity to create the same power.

###Irms
RMS Current is the effective value in the sense of the value of the direct current that would produce the same power dissipation in a resistive load. Figure 2.1.6.1 displays calculations of Irms.

###Phase shift
When capacitors or inductors are involved in an AC circuit, the current and voltage do not peak at the same time. The fraction of a period distinction between the peaks displayed in degrees is said to be the phase difference (Figure 2.1.7.1). The phase difference is less or equal to 90 degrees. It is common to use the angle by which the voltage leads the current. This leads to a positive phase for inductive circuits since the current lags the voltage in an inductive circuit. The phase is negative for a capacitive circuit since the current leads the voltage.  

#Device identification system (DIS)

Device identification is a core component of this system. The system should need to identify which devices are connected to the system correctly. There is a step by step process to identify devices. Basically, a smart plug and neural network used to identify the devices. This system based on pattern recognition therefore pattern recognition design cycle and system explanation added to further explanation. The step by step process explained below

##Design Cycle

Pattern recognition is the process of recognizing patterns by using a machine learning algorithm. Pattern recognition can be defined as the classification of data based on knowledge already gained or on statistical information extracted from patterns and their representation (Ansari, 2018) Pattern recognition is a classification technique that decomposes into three components, supervised learning, unsupervised learning and semi supervise. In this research supervised learning used to develop the system. Device recognition based on pattern recognition is a complex process that involves several steps to identify devices.

###Data collection

Data collection is a collection of data that can collect from the problem domain. There are usable and unusable data available. In this stage, discriminative features and irrelevant features are not considered. Sensors and other sources are used to collect data. In this research, the smart plug with different sensors used to collect data.

###Choose features

Depending on the characteristic of the problem domain, need to extract discriminative, invariant and irrelevant data to reduce transformation insensitive to noise. Data convert, transform, load and refresh according to the classification to get accurate result.

###Choose model

Used different algorithms to check the performance. if the data is not satisfied with predict the result, want to move another classification technic. Likewise continuously do this process to get accurate results.

###Train classifier

Use previously collected test data from choosing features to determine the classifier. Create a model file to reduce the time that takes to create classification boundaries and increase performance.

###Evaluate classifire

Use actual data to measure error rate or performance. If performance is not satisfied with the expected outcome, need to move one set from one feature to another. When if happen continuously need to switch from one classifier to another.

###Pattern recognition system

Device identification is the most important step in this system. This system enables the user to predict which devices are connected to the system. The device identification system brake into five steps. Each step describes step by step process of the system such as how data collected, how to segment data, how chose data, how classification happens, and the evaluation part. Those steps are more important to the system (all are tightly coupling). If one step gets corrupted, the overall system will collapse.

###Sensing

The sensors in a system are what receives the data input, and they may vary depending on the purpose of the system. They are usually some form of transducers such as a camera or a microphone. In this system we used smart plug to receive the inputs.

##Smart plug

Device called smart plug is created to detect the power consumption from each device. And the smart plug identifies each device using machine learning techniques and classifies data for further analysis. There are many researches done to detect electrical devices in real-time and some different researches were done to optimize and predict power consumption.
Smart plug consists of the voltage sensor, current sensor WIFI sensor, and the Arduino board. Voltage sensor and current sensor capture the changes in power. Arduino board process data and send it to API using the WIFI model.

![alt text](https://github.com/SupunRandunu/Final-year-reserch-project/blob/master/img/IMG_20201109_132046.jpg)

![alt text](https://github.com/SupunRandunu/Final-year-reserch-project/blob/master/img/Circuit%20Diagram.png)

#Voice recognition system

The Voice recognition system is an essential subsystem of this home automation system. This system enables the user to execute commands through the voice. 
Proprietary approach enable user to use closed source software to develop the system. User could experience high performance and accurate system because of the advance algorithm and powerful servers. There are some advantages and disadvantages also. 

![alt text](https://github.com/SupunRandunu/Final-year-reserch-project/blob/master/img/mobile%20ui.png)
