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
module jkff(j,k,clk,q,qbar);
input j,k,clk;
output reg q,qbar;
initial 
begin
q=1'b0;
q=1'b1;
end 

always @(posedge clk)
begin 
q<=(j&~q)|(~k&q);
qbar<=~q;
end
endmodule


**RTL Schematic**
<img width="1334" height="667" alt="Screenshot 2025-12-05 081747" src="https://github.com/user-attachments/assets/f6ec4479-c977-45ce-b7d4-6a69aa20e824" />
<img width="1505" height="802" alt="image" src="https://github.com/user-attachments/assets/87853fce-3011-4c44-a8c2-d59b4043283c" />


**Output Timing Waveform**
TIMING DIAGRAM FOR FLIP FLOP:
<img width="1072" height="563" alt="image" src="https://github.com/user-attachments/assets/9ed242f5-14e6-4658-8e33-b98fca88170e" />
<img width="1541" height="816" alt="image" src="https://github.com/user-attachments/assets/83c6c5e8-89f7-4eff-82c9-5d53de417175" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



