# sr-flipflop
AIM:

To implement SR flipflop using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED:

Quartus prime

THEORY

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied.
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state,
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

Procedure:
1.Type the program in Quartus software. 2.Compile and run the program. 3.Generate the RTL schematic and save the logic diagram. 4.Create nodes for inputs and outputs to generate the timing diagram. 5.For different input combinations generate the timing diagram.


PROGRAM:
module exp6(S,R,clk,Q,Qbar);
input S,R,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=S|((~R)&Q);
Qbar=~Q;
end
endmodule

Name: MINHAJ AHAMED J
Reg No: 25006694

**RTL LOGIC FOR FLIPFLOPS:
[rtl.pdf](https://github.com/user-attachments/files/24150242/rtl.pdf)


TIMING DIGRAMS FOR FLIP FLOPS 


[wave2.bmp](https://github.com/user-attachments/files/24158068/wave2.bmp)


RESULTS Thus the SR flipflop is implemented successfully and truth table has verified
