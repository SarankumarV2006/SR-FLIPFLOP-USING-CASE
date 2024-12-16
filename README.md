# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.


![Screenshot 2024-12-16 091349](https://github.com/user-attachments/assets/0509ce1c-46f4-43c7-84ff-a0933f157bc6)


 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![Screenshot 2024-12-10 144335](https://github.com/user-attachments/assets/b4afd217-4c02-4c79-9edc-c37fe760a71e)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![Screenshot 2024-12-10 144315](https://github.com/user-attachments/assets/42f17af4-1870-47ef-a010-42c95d43d202)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![Screenshot 2024-12-16 093438](https://github.com/user-attachments/assets/52a17602-6b40-4ba8-92f6-397e7d22e053)


 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

Step 1: Create a New Project

1. Open Quartus Prime.
2. Click "File" > "New Project Wizard".
3. Choose "Verilog" as the design language.
4. Select a project name and location.

Step 2: Write the Verilog Code

1. Create a new file (sr_flipflop.v) in the project directory.
2. Copy and paste the Verilog code for the SR flip-flop (provided earlier).
3. Save the file.

Step 3: Create a Testbench

1. Create a new file (tb_sr_flipflop.v) in the project directory.
2. Copy and paste the testbench code (provided earlier).
3. Save the file.

Step 4: Compile and Simulate
1. Add both files (sr_flipflop.v and tb_sr_flipflop.v) to the project.
2. Click "Compile" to compile the design.
3. Click "Simulate" to run the simulation.
4. Observe the waveform outputs.

Step 5: Verify Functionality

1. Verify the output waveforms match the expected behavior based on the state table.
2. Check for hold, set, and reset conditions.

Step 6: Implement on FPGA (Optional)

1. If desired, program the FPGA board with the compiled design.
2. Verify the hardware implementation using external inputs and outputs.


**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by:Sarankumar.V RegisterNumber:24010668
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

**RTL LOGIC FOR FLIPFLOPS**

**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-12-10 143130](https://github.com/user-attachments/assets/bc7aeacd-d556-4581-ae31-0ce8d48bdac6)

**RESULTS**
Thus the truth table of sr flipflop in Quartus|| using verilog programming are studied,verify and executed successfully.
