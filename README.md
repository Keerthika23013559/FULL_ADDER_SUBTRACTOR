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
![image](https://github.com/23004513/FULL_ADDER_SUBTRACTOR/assets/138973069/73fd7b9e-ba95-4d5d-a22c-57d26c2b98eb)


![image](https://github.com/23004513/FULL_ADDER_SUBTRACTOR/assets/138973069/2d6d58dc-2b3a-40dc-a3b9-6fabb513cfed)


**Procedure**

Write the detailed procedure here
FULL ADDER

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

FULL SUBTRACTOR
1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
FULL ADDER:
```
module fulladd_top(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);
endmodule
```
FULL SUBTRACTOR:
```
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```

**RTL Schematic**
### FULL ADDER:
![318210459-fbb0551a-202f-4aae-a0de-d22f24506755](https://github.com/Keerthana-VJ/FULL_ADDER_SUBTRACTOR/assets/149347704/c2d5f25c-abc0-4243-b529-06309e5c32d5)
### FULL SUBTRACTOR:
![318210531-522a1f25-8b70-4139-bd45-47f235d74331](https://github.com/Keerthana-VJ/FULL_ADDER_SUBTRACTOR/assets/149347704/ef901cf2-aed3-4906-8efa-b51dc61e1d0b)

**Output Timing Waveform**
### FULL ADDER:
![318210582-4a30573e-0766-4f04-8596-c4718b5d8241](https://github.com/Keerthana-VJ/FULL_ADDER_SUBTRACTOR/assets/149347704/6ad6f1b1-c4c0-4a83-b8ea-468ecd65adc0)
### FULL SUBTRACTOR:
![318210618-9f1e8407-b18d-4ba7-a52f-9c653098bc7a](https://github.com/Keerthana-VJ/FULL_ADDER_SUBTRACTOR/assets/149347704/28995fa5-c6d5-47a6-8ce5-576ccf187dc0)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



