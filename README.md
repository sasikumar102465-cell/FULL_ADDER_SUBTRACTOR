# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
FULL ADDER
<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/6b126d07-0dae-45b9-8f26-8f0becf23cec" />

FULL SUBTRACTOR
<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/b1910d76-df6d-465d-bf94-9a09cb8ccd6b" />

**Procedure**
Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:SASIKUMAR S
RegisterNumber:25015350
FULL ADDER
module exp4(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule

FULL SUBTRACTOR
module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (~a & b) | (~(a ^ b) & bin);
endmodule

**RTL Schematic**
FULL ADDER
<img width="1177" height="744" alt="image" src="https://github.com/user-attachments/assets/a4fcbc73-4a56-4e65-9bfd-9c8c7b830826" />


FULL SUBTRACTOR
<img width="1351" height="542" alt="image" src="https://github.com/user-attachments/assets/3159aaf5-5e15-47f7-a048-25bd181d63f8" />

**Output Timing Waveform**
FULL ADDER

<img width="1920" height="1201" alt="image" src="https://github.com/user-attachments/assets/a35008db-5ff8-4882-ae23-07ddd84347ca" />

FULL SUBTRACTOR
<img width="1921" height="1201" alt="image" src="https://github.com/user-attachments/assets/36627636-be76-489d-9c3e-fc7b1af2d498" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



