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

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:25017728
*/

**Program: Full Adder

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
Full Sub // Full Subtractor in Verilog
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
**RTL Schematic**
full adder
<img width="1038" height="562" alt="Screenshot 2025-12-06 135641" src="https://github.com/user-attachments/assets/b7628306-73ab-413c-9f32-917c6827c8df" />

full subtractor
<img width="1038" height="452" alt="Screenshot 2025-12-06 135944" src="https://github.com/user-attachments/assets/acfdcc60-1a88-48f3-8dcd-20756f6cd333" />


**Output Timing Waveform**
full adder
<img width="1051" height="191" alt="Screenshot 2025-12-06 140038" src="https://github.com/user-attachments/assets/43ad166d-527b-4b2b-86d7-c8623702f3e8" />

full subtracter
<img width="1047" height="166" alt="Screenshot 2025-12-06 140129" src="https://github.com/user-attachments/assets/c3e35597-de25-4599-8089-3b466cd33bde" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
.................................... ............................................ ....................... .............. ............................................ ........................ ................................................................................................................................................ ................. ...................... ..........................................................

.......................... ......................................

. ..... . . .... . . . . . . . . . . . . . . . . . ..... . . . . . . . . . . . . .. . . . . . . . . . . .. . . . ..... . . . . . . . ...... . . . . . .... . . . .... . . . ... . .. . . . . . . . . . . .... .. .. .. . . . . . . . . . .... . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

.. . . . . . . . . . . . . . . . . . . . . . .


