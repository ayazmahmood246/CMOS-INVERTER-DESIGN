# CMOS-INVERTER-DESIGN
#### APPROACH:

We have to design a circuit which inverts the input like a not gate which is a basic gate or which inverts the output. 


| INPUT  |   OUTPUT  |
|--------|-----------|
|   O    |    1      | 
|   1    |    0      |

For designing this type of circuit we neeed a device which gives high output at low input and low input at high output you can think of bjt could work as an inverter



## NMOS INVERTER DESIGNING

First we need to understand the characteristics of an nmos transistor so we design a circuit in which we vary Vgs and Vds to get suitable characteristics
so i design a circuit in this using nmos BSBO17N03LX3 which is available in lt spice we can use any nmos model present there

<img width="607" height="535" alt="Screenshot 2025-08-17 at 3 02 53 PM" src="https://github.com/user-attachments/assets/3b35e25b-9244-41db-99be-3e73db0fbc35" />
Fig (1)

In this circuit we fixed the Vd at 3 volt and vary the Vg from 0 to 10 and plot the current negative of I(Vd) which entering in the Vd voltage source  we get the following characteristics:
<img width="1470" height="956" alt="Screenshot 2025-08-17 at 3 03 25 PM" src="https://github.com/user-attachments/assets/131ddc95-5a99-4c72-9e86-3eb9cfd6b6d3" />
Fig(2)
Now we zoom into the part where current start to increase:
<img width="2940" height="1912" alt="Screenshot 2025-08-17 at 3 04 50 PM" src="https://github.com/user-attachments/assets/cc4456d4-b725-4d9b-ba3b-006ae6502bc9" />
Fig(3)

Now this shows that if Vd is greater than 2.6 volt the Id start to increase and when it is less the current is zero so the threshold voltage is 2.6V.

Now we see that if we take input as Vg then when Vg is less than Vth(threshold voltage) There is no current flowing, but as the input Vg goes high the current also increases.
so can these charasteristics be helpful in making a inverter yes i think because if the input is low we get no current so we can connect a resistor in between Vd and drain and take the output from drain in this case when input is less than 2.6 volt we get no current and Vo will be equal to Vd as no voltage drop occurs at resistor and if the input is high voltage drop across resistor and ve get a low output.

## CIRCUIT DIAGRAM NMOS INVERTER
Now i have placed a 10k resistor between Vd and drain and set the value of Vd equals to 3v.

Now i dc sweep the value of Vg from 0 to 5 volts and simulate the circuit to see the characteristics between Vo and Vg 

As we can see when the input is in between 0 to 2 v the output is 3v and when the input is in between 2.4 to 5 v the output is 0v.
So it is showing the prediction of ours is somewhat true we get high output at low voltage and low output at high voltage.
<img width="959" height="654" alt="Screenshot 2025-08-29 at 7 44 25 PM" src="https://github.com/user-attachments/assets/4d4c5ecf-5dc1-4e62-a829-8f518bd5397f" />


Now we apply a square pulse and see what are the results
<img width="1470" height="956" alt="Screenshot 2025-08-29 at 7 46 29 PM" src="https://github.com/user-attachments/assets/f1591300-c053-4e62-b32a-955a212acd60" />
so, as we can see the results are as expexted we get low ouptut at high input and vice versa. We have successfully constucted an inverter by using nmos transistor. 

We can similary do it for pmos and we get inverse of this.



















