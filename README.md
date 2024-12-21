# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

/* write all the steps invloved */
ALGORITM: 
Step1: Define the specifications and initialize the design. 
Step2: Declare the name of the entity and architecture by using VHDL source code. 
Step3: Write the source code in VERILOG. 
Step4: Check the syntax and debug the errors if found, obtain the synthesis report. 
Step5: Verify the output by simulating the source code. 
Step6: Write all possible combinations of input using the test bench. 
Step7: Obtain the place and route report. 

**PROGRAM**
module exp6(din, clk, rst, dout); 
    input din; 
    input clk; 
    input rst; 
    output dout; 
  reg dout; 
  reg [7:0]x; 
  always @ (posedge(clk) or posedge(rst)) begin 
  if (rst==1'b1) 
  begin 
  dout=8'hzz; 
  end 
  else 
  begin 
  x={x[6:0],din}; 
  dout=x[7]; 
  end 
  end 
  endmodule

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2024-12-21 083718](https://github.com/user-attachments/assets/0d68c49e-6274-4452-8b5b-9792eb55f026)


**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-12-21 084246](https://github.com/user-attachments/assets/08056b92-684f-408d-8fd4-cc6930b5ef6a)


**RESULTS**
Thus the OUTPUT’s of 8-bit shift register are verified by synthesizing and simulating the 
VERILOG code.
