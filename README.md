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

![Screenshot 2025-04-23 230714](https://github.com/user-attachments/assets/50af18be-826c-4d3c-9f53-db2798696f33)

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

![Screenshot 2025-04-23 230729](https://github.com/user-attachments/assets/07a0ce64-df08-4b69-b182-5e93ece76dbb)

**Procedure**

Full Adder:
       1.Open Quartus II and create a new project.
       2.Use schematic design entry to draw the full adder circuit. 
       3.The circuit consists of XOR, AND, and OR gates.
       4.Compile the design, verify its functionality through simulation.
       5.Implement the design on the target device and program it.
 
 Full Subtractor:
       1.Follow the same steps as for the full adder.
       2.Draw the full subtractor circuit using schematic design.
       3.The circuit includes XOR, AND, OR gates to perform subtraction.
       4.Compile, simulate, implement, and program the design similarly to the full adder.
       
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:Divya Dharshini S RegisterNumber:212224240039
```
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```
*/

**RTL Schematic**

![Screenshot 2025-04-23 230838](https://github.com/user-attachments/assets/7397ab69-2e71-4f06-aab6-25b8b739eb36)
![Screenshot 2025-04-23 230855](https://github.com/user-attachments/assets/08db9ea1-3a85-491a-b7eb-9a79c0109ad8)

**Output Timing Waveform**

![Screenshot 2025-04-23 230948](https://github.com/user-attachments/assets/0f001bb4-4cb1-40c2-8130-4da701c53660)
![Screenshot 2025-04-23 231010](https://github.com/user-attachments/assets/11bb764d-58f2-44b9-9426-e54f9e09c331)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



