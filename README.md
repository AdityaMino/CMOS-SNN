# CMOS-SNN
Spiking neural networks (SNNs) have emerged as a  promising candidate for the next generation of neural  networks, mainly due to their alignment with biological neuron function, which may help to uncover brain mechanisms. This subthreshold CMOS implementation of the 
Izhikevich neuron model using Xschem and Skywater 
130nm pdk, demonstrates a significant step towards 
biologically accurate neuromorphic hardware. Due to the 
extremely low energy consumption and supply voltage 
requirements, the circuit is suitable for use in large-scale 
spiking neural networks, neuromorphic processors and in 
embedded applications 

## Schematic Of the Circiuit
![Screenshot from 2024-11-08 23-15-15](https://github.com/user-attachments/assets/e48f4e25-19fd-4f8e-ab67-213a934c1423)

The spike generation and communication functions are 
performed by the digital circuitry shown on the right in Fig. 
2. When the membrane potential reaches the threshold of 
the inverter (M9, M10), the output of that inverter goes 
low. The ACK signal is normally low and hence the second 
inverter (M11, M12) remains activated, and its output goes 
high. This then turns on M14, and M15, which sends out an 
activelow request (REQ) signal to indicate that a spike has 
been generated to the following digital arbitration circuitry. 
The resistor R1 and capacitor C1 are used to emulate the 
load that M15 will have to drive. When the ACK pulse 
ends, the circuit has been reset to its original state and the 
temporal evolutions of state variables resume.
## Output Plots
![image](https://github.com/user-attachments/assets/5538dd67-ef1a-4f61-b509-19b09ba8834b)

**Regular Spiking Behaviour**

Regular spiking (RS) was
obtained by setting Vc to 140mV and Vd to 140mV. Chattering
(CH) was obtained by setting Vc to 20mV and Vd to 150mV.
Low threshold spiking (LTS) was obtained by setting Vc to
20mV and Vd to 20mV. An input current of 2pA was used
for all three cases. For all these simulations, a 1µs delay was
used between the time the REQ signal is sent out and the ACK
signal is received to emulate the delay in the digital circuitry.
![image](https://github.com/user-attachments/assets/a0413865-b65d-41e5-8838-7a14c96380dd)

**Low Threshold Spiking, with the final periodic behavior**
