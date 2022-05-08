# Experiment 04 Implementation of combinational logic using universal gates

# Implementation of Half subtractor and Full subtractor circuit

## AIM:

To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

## EQUIPMENT'S REQUIRED:

 1.Hardware – PCs, Cyclone II , USB flasher
 
 2.Software – Quartus prime

## THEORY:

A universal gate is a logic gate which can implement any Boolean function without the need to use any other type of logic gate. The NOR gate and NAND gate are universal gates. This means that you can create any logical Boolean expression using only NOR gates or only NAND gates. In practice, this is advantageous since NOR and NAND gates are economical and easier to fabricate than other logic gates. Similarly, an OR gate is typically realised as a NOR gate followed by an inverter.

## PROCEDURE:

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## PROGRAM:

```
/*
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.
Developed by:Paarkavy B
RegisterNumber:212221230072
*/

## F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

module Combination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule


## F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

module norcombination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
not(F,S);
endmodule
```

## OUTPUT:

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

### TRUTH TABLE:

![output](TT-1.png)

### RTL REALIZATION:

![output](rtl-1.png)

### TIMING DIAGRAM:

![output](Td-1.png)


F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

### TRUTH TABLE:

![output](TT-2.png)

### RTL REALIZATION:

![output](rtl-2.png)

### TIMING DIAGRAM:

![output](Td-2.png)

## RESULT:

Thus implementation of logic functions using NAND and NOR gates is done and its operation is verified in Quartus using Verilog programming.
 
