# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

Open Quartus software and create a new Verilog file. Paste the code and save it.
Compile the program to check for errors.
Generate the RTL schematic via the RTL Viewer and save the logic diagram.
Use the Waveform Editor to assign nodes for clk, rstn, and out.
Simulate the design with different clk and rstn combinations to generate the timing diagram, and save the results.
**PROGRAM**
```
Developed by: RISHI M
RegisterNumber: 212222230119
```

```
module exp11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin
	if(!rstn)
		out<=0;
	else
		out <= out+1;
end
endmodule
```
**RTL LOGIC FOR 4 Bit Ripple Counter**

![image](https://github.com/user-attachments/assets/bbebe33f-f7db-414b-be35-b98f674d1699)


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![image](https://github.com/user-attachments/assets/031f541f-55e4-472a-ad46-4b6b547a0543)

TRUTH TABLE

![image](https://github.com/user-attachments/assets/b3faf794-9025-4e91-a3e7-0f6cec9b805f)


**RESULTS**
Thus the Synchronous 3 bit Up counter is implemeted and verified.
