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

![image](https://github.com/user-attachments/assets/b09e7332-958e-4e84-9f53-7affd2357d9c)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/user-attachments/assets/ca8e58aa-8470-42ed-8d58-e2f5effe7f02)

**Figure -1 FULL SUBTRACTOR**

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
FULL ADDER

![image](https://github.com/user-attachments/assets/4d112be1-6902-42f6-a80f-d6ffa1814c34)

FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/affd2a74-295b-48dc-b7c5-3e2de75db7d3)




**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.


**Program:**
```
Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: KABELAN G K
RegisterNumber: 24900985
```
```
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
```

**RTL Schematic**
![image](https://github.com/user-attachments/assets/1d2b3085-ade9-4211-bba1-ae7ccfe625b3)


**Output Timing Waveform**
![image](https://github.com/user-attachments/assets/6b3631f9-4f94-417d-89f4-ab72d3f0fb7f)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



