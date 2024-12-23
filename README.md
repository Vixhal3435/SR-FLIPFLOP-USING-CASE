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
```
1 Type the program in Quartus software.
2 compile and the reun the program.
3 Generate the RTL schematic and save the logic diagram.
4 create nodes for inputs and outputs to generate the timing diagram.
5 For different inuput combinations generate the timing diagram.
```

**PROGRAM**
```
module sr_ff(s,r,clk,q,qbar);
input s,r,clk;
output reg q;
output reg qbar;
initial 
begin
q=0;
qbar=1;
end
always @(posedge clk)
begin
   q=s|(~r&q);
   qbar=r|(~s&~q);
end
endmodule
```

![Screenshot 2024-12-23 082432](https://github.com/user-attachments/assets/9f175f40-e44e-4d0c-9d1d-32d18d9e4fb7)

 Developed by: VISHAL V
 
 RegisterNumber:24900179


**RTL LOGIC FOR FLIPFLOPS**

![Screenshot 2024-12-23 082631](https://github.com/user-attachments/assets/4dbcd1cc-270d-4473-9c73-b746b5576537)


**TIMING DIGRAMS FOR FLIP FLOPS**

![Screenshot 2024-12-23 082646](https://github.com/user-attachments/assets/f526139d-edd8-43f8-880a-38f848ef7f55)


**RESULTS**
Thus the given SR Flip Flop expression is verified using Quartus software.
