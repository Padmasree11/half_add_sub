# half_add_sub

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

<img width="1920" height="1080" alt="Screenshot (103)" src="https://github.com/user-attachments/assets/27c84482-c562-4f7f-a22b-4e49fafeda89" />




Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B


<img width="1920" height="1080" alt="Screenshot (104)" src="https://github.com/user-attachments/assets/8f17b83c-c827-470d-8548-cb587979b45a" />



Figure -02 HALF Subtractor

**Truthtable**
HALF ADDER

![image](https://github.com/user-attachments/assets/5ddc52ef-d125-4442-8265-139c2bb7c6e7)


HALF SUBTRACTOR

![image](https://github.com/user-attachments/assets/83ec047b-4a5b-42ea-ac00-af7c49740ea2)



**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**


Program to design a half adder and half subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:padmasree.p
RegisterNumber:25008840


**Half Adder**

module half_adder (
    input  wire a, b,     // Inputs
    output wire sum,      // Sum output
    output wire carry     // Carry output
);

    // Logic equations
    assign sum   = a ^ b;   // XOR for sum
    assign carry = a & b;   // AND for carry

endmodule


**Half Subtractor**

module half_subtractor (
    input  wire a, b,         // Inputs
    output wire diff, borrow  // Outputs
);
    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = ~a & b;    // Borrow when a < b

endmodule

**RTL Schematic**
**Half Adder**
<img width="1920" height="1080" alt="Screenshot (103)" src="https://github.com/user-attachments/assets/41554039-d0b5-4b6f-b86f-19322c83fb10" />


**Half Subtractor**
<img width="1920" height="1080" alt="Screenshot (104)" src="https://github.com/user-attachments/assets/3a034fb9-9a40-4d86-945e-ba73e6216e3e" />

**Output/TIMING Waveform**
**Half Adder**
<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/5f9877ea-82a1-4064-94fa-ba9c1c82ece0" />


**Half Subtractor**
<img width="1920" height="1080" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/d8d361dd-c901-461a-9e0d-d56b49c49154" />

**Result:**

Thus the Half Adder and Half Subtractor are studied and the truth tables are verified
