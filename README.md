# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy


## Developed by: 
Nandakesore J

## RegisterNumber: 
23009689  
 
## Equipments Required:

Hardware PC Cyclone II, USB flasher Software - Quartus prime

## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory:

A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.
 
## Logic Diagram:

## Procedure:

Create a New Project:

1.Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
Create a New Design File:

2.Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.
Write the Combinational Logic Code:

3.Open the newly created Verilog or VHDL file and write the code for your combinational logic.
Compile the Project:

4.To compile the project, click on "Processing" > "Start Compilation" in the menu.
Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
Analyze and Fix Errors:*

5.If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary.
View the RTL diagram.
6.Verification:

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
Give the Input Combinations according to the Truth Table amd then simulate the Output waveform

## Program:

module ex_02(a,b,c,d,f1);
input a,b,c,d;
output f1;
wire x1,x2,x3,x4,x5;
assign x1=(~a)&(~b)&(~c)&(~d);
assign x2=(a) &(~c)&(~d);
assign x3=(~b)& (c) &(~d);
assign x4=(~a)& (b) & (c) & (d);
assign x5=(b) & (~c)&(d);
assign f1=x1|x2|x3|x4|x5;
endmodule

## Code :

![image](https://github.com/Nandakesore0210/Experiment--02-Implementation-of-combinational-logic-/assets/149365088/4c961eef-da72-4419-8cbe-1afb677fc44e)

## RTL realization : 

![image](https://github.com/Nandakesore0210/Experiment--02-Implementation-of-combinational-logic-/assets/149365088/399ea6c3-a645-445b-96c6-8ce02a70ad70)

## Timing Diagram :

![image](https://github.com/Nandakesore0210/Experiment--02-Implementation-of-combinational-logic-/assets/149365088/39e56e43-8018-4168-97a1-fae7dfa6144b)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
