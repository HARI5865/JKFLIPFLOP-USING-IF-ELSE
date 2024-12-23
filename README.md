# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

/* write all the steps invloved */

**PROGRAM**<br>
module exp7(J,K,clk,q,qbar);<br>
input J,K,clk;<br>
output reg q;<br>
output reg qbar;<br>
initial q=0;<br>
initial qbar=1;<br>
always @(posedge clk)<br>
begin<br>
q=((J&(~q))|((~K)&q));<br>
qbar=~q;<br>
end<br>
endmodule<br>

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL LOGIC FOR FLIPFLOPS**<br>
![390972706-c9220406-83d4-432b-a4c7-538fb7bcbddc](https://github.com/user-attachments/assets/85ef689a-5145-4667-91c1-1b6503c23487)

**TIMING DIGRAMS FOR FLIP FLOPS**<br>
![390972662-c1da8a4e-6032-4773-8b9e-188826706d47](https://github.com/user-attachments/assets/af3714ab-deb4-4ebe-8a1b-acc53ea9d6b5)


**RESULTS**<br>
To implement JK flipflop using verilog and validating their functionality using their functional tables are verified.
