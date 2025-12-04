# FULL_ADDER_SUBTRACTOR
**Date:04/12/2025**

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

**Procedure**

Write the detailed procedure here

**Program:**
Full Adder
-------------------------------------
// Full Adder in Verilog
```
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
```
Full Sub
-------------------------------------
// Full Subtractor in Verilog
```
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule
```


/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: SANJAI K
RegisterNumber: 25018325
*/

**RTL Schematic**

**Output Timing Waveform**
**Full Adder**
<img width="837" height="524" alt="Screenshot 2025-12-04 161921" src="https://github.com/user-attachments/assets/8b0eee31-0772-40f1-bd93-d1dcf556573d" />

<img width="1294" height="358" alt="Screenshot 2025-12-04 161936" src="https://github.com/user-attachments/assets/edbef774-feca-440b-874f-ac3e6983f731" />


**Full Subtractor**
<img width="910" height="403" alt="Screenshot 2025-12-04 162002" src="https://github.com/user-attachments/assets/4f52154c-a979-46e5-979f-29f88012ac91" />

<img width="1231" height="393" alt="Screenshot 2025-12-04 162029" src="https://github.com/user-attachments/assets/25a1acf2-f00b-4782-aacf-ffaea1615558" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
.
.
.

.
.
.

.
.

.
.
.

.
.
.
.
.

.
.
.
.
.
.

.
..
.

..
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.

..

.
.
.
...
.


