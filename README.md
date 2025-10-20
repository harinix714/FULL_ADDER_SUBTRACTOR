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


<img width="754" height="563" alt="Screenshot 2025-10-20 180757" src="https://github.com/user-attachments/assets/2b2c5039-22a6-4a93-8d6c-ad000265d3e9" />
<img width="507" height="350" alt="Screenshot 2025-10-20 180618" src="https://github.com/user-attachments/assets/ddb95d6c-af46-4f51-932f-76ec0871fbe3" />





**Procedure**

Write the detailed procedure here

**Program:**
module fulladder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule

module fafs (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Harini S K 
RegisterNumber:25018849


**RTL Schematic


<img width="1920" height="1080" alt="Screenshot 2025-10-20 172350" src="https://github.com/user-attachments/assets/ce57a79b-8ef4-4f15-966d-acf7f05d358c" />

<img width="1920" height="1080" alt="Screenshot 2025-10-20 175731" src="https://github.com/user-attachments/assets/177e7718-ae23-4fce-ac6f-b0014f55f925" />



**Output Timing Waveform**

<img width="1920" height="1080" alt="Screenshot 2025-10-20 172359" src="https://github.com/user-attachments/assets/1dfdd499-6a17-402b-9207-4178881bf264" />

<img width="1920" height="1080" alt="Screenshot 2025-10-20 175903" src="https://github.com/user-attachments/assets/304a747f-860f-4bd3-b9d1-1d74acea8287" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



