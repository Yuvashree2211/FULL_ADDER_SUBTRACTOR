NAME: YUVASHREE R

REG NO: 212224040378

# FULL ADDER SUBTRACTOR



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

![Screenshot 2025-04-21 221754](https://github.com/user-attachments/assets/07efece1-6e81-4c16-b5a1-8c85e4368e36)

![Screenshot 2025-04-21 221808](https://github.com/user-attachments/assets/b50ea26d-2d9c-428a-bcb0-914e8d88fa0f)


**Program:**
```
module exp4(a,b,cin,c,d,bin,sum,cout,difference,bout); 
input a,b,cin,c,d,bin;
output sum, cout, difference, bout;
assign sum=a^b^cin;
assign cout=(a&b) | (b&cin) | (cin&a);
assign difference=a^b^bin;
assign bout=(~a&b) | (bin&(~a))| (bin&~b);
endmodule
```

**RTL Schematic**

![Screenshot 2025-04-21 231437](https://github.com/user-attachments/assets/e7ad695c-dd8d-4556-a352-4ee72f3e1972)


**Output Timing Waveform**

![Screenshot 2025-04-21 231506](https://github.com/user-attachments/assets/217471e4-3d14-43c5-99e2-78ed65df0167)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



