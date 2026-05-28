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

**Full Adder:**

<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/5ba5971f-b9b7-4c1f-b7ab-96f7a5e79dc8" />

**Full Subtractor:**

<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/a69d078e-9a7b-45ce-af45-28b2826fb60d" />

**Procedure:**
1. Create a new project in Quartus II software.
2. Type the Verilog program for Full Adder and Full Subtractor.
3. Compile the program and view the RTL schematic.
4. Create nodes for inputs and outputs to generate the timing waveform.
5. For different input combinations generate the timing waveform and verify the outputs with the truth table.


**Program:**
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: RAAGHAVI S  RegisterNumber: 212225040321
*/

**Full Adder:**
```
module DE1Exp3(sum, carry, a, b, cin);

input a,b,cin;
output sum,carry;

wire w1,w2,w3;

assign w1 = a ^ b;
assign w2 = a & b;
assign w3 = w1 & cin;

assign sum = w1 ^ cin;
assign carry = w2 | w3;

endmodule
```
**Full Subtractor:**
```
module DE2Exp3(diff,bout,a,b,bin);

input a,b,bin;
output diff,bout;

wire w1,w2,w3;

assign w1 = a ^ b;
assign w2 = ~a & b;
assign w3 = ~w1 & bin;

assign diff = w1 ^ bin;
assign bout = w2 | w3;

endmodule
```

**RTL Schematic**

**Full Adder:**
<img width="1919" height="1027" alt="Screenshot 2026-05-25 205150" src="https://github.com/user-attachments/assets/7312e39c-ca6f-4272-abf1-c17fe6929491" />

**Full Subtractor:**
<img width="1919" height="1028" alt="Screenshot 2026-05-25 220232" src="https://github.com/user-attachments/assets/d91d35fd-9a03-4dd5-93b6-c8728ffc7eba" />

**Output Timing Waveform**

**Full Adder:**
<img width="1919" height="1021" alt="Screenshot 2026-05-25 213502" src="https://github.com/user-attachments/assets/ffbb9932-6da1-4f4a-bcb9-83023fe2fce0" />

**Full Subtractor:**
<img width="1919" height="1025" alt="Screenshot 2026-05-25 224500" src="https://github.com/user-attachments/assets/47e3cea7-ddf4-45fe-b057-c2b2b727e08c" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



