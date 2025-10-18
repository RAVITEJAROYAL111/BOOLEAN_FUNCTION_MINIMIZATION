# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**
Logic function is implemented using Verilog, a hardware description language used to model electronic systems. Verilog enables the design and simulation of digital circuits efficiently. Quartus software is utilized to compile, synthesize, and verify the logic function through simulation. This process ensures the functionality aligns with the expected behavior of the logic design.

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
module DE2(A, B, C, D, W, X, Y, Z, F1,F2);

input A, B, C, D, W, X, Y, Z;

wire x1, x2, x3, x4, x5, x6, x7, x8, x9, x10;

output F1, F2;

assign x1=(~A) & (~B) & (~C) & (~D);

assign x2=(A)&(~C)&(~D);

assign x3=(~B)&(C)&(~D);

assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);

assign x6=(X)&(~Y)&(Z);

assign x7=(~X)&(~Y)&(Z);

assign x8=(~W)&(X)&(Y);
assign x9=(W)&(~X)&(Y);

assign x10=(W)&(X)&(Y);

assign F1=x1|x2|x3|x4|x5;

assign F2=x6|x7|x8|x9|x10;

endmodule 

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:ravi teja royal
RegisterNumber:25011599


**RTL realization**
<img width="851" height="512" alt="image" src="https://github.com/user-attachments/assets/62ff47b1-e870-4390-a84d-1d76eed0cef9" />

**Output:**
<img width="844" height="437" alt="image" src="https://github.com/user-attachments/assets/f2417aba-237e-4229-8514-c2b64f2efb0d" />

**RTL**

**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

