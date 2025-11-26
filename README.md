# Full_adder_subtractor
Implementation-of-Full-Adder-and-Full-subtractor-circuit

# AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

# Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

# Full Adder and Full Subtractor

# Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin

Carry = AB + ACin + BCin

![full-adder-block-diagram](https://github.com/user-attachments/assets/8625f5b8-8723-4cc7-a32d-8bbc736eca1d)

Figure -1 FULL ADDER

# Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![full-subtractor-logic-circuit-diagram](https://github.com/user-attachments/assets/be89ee50-d660-4740-8767-bb8bbfe62e52)


Diff = A ⊕ B ⊕ Bin

Borrow out = A'Bin + A'B + BBin

# Truthtable

# Full adder
<img width="358" height="234" alt="full adder truth table" src="https://github.com/user-attachments/assets/b3c1a4d3-3dd0-4049-8998-e0596bc711a2" />

# Full subtractor
<img width="209" height="148" alt="full subtractor truth table" src="https://github.com/user-attachments/assets/684b4aa7-29d7-4a26-b77f-3e3228133f9d" />

# Procedure

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram

# Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Harini G
RegisterNumber: 25015377

# Full adder

module Full_adder(

    input  wire a, b, cin,  
    
    output wire sum, carry   
    
);

    assign sum   = a ^ b ^ cin;   
    
    assign carry = (a & b) | (b & cin) | (a & cin); 
    
endmodule

# Full subtractor

module full_subtractor (

    input  wire a, b, bin,      
    
    output wire diff, borrow    
    
);

    assign diff   = a ^ b ^ bin;                  
    
    assign borrow = (~a & b) | (~(a ^ b) & bin);  

endmodule

# RTL Schematic

# Full adder

<img width="976" height="568" alt="Screenshot 2025-11-26 140750" src="https://github.com/user-attachments/assets/ece835b4-18f8-4e45-ad34-ea0be5f9523f" />

# Full subtractor

<img width="963" height="403" alt="Screenshot 2025-11-26 143137" src="https://github.com/user-attachments/assets/2017855d-0e54-4637-9d7e-ee9cb0b426db" />

# Output Timing Waveform

# Full adder

<img width="1854" height="990" alt="Screenshot 2025-11-26 143717" src="https://github.com/user-attachments/assets/c4f8148b-9c70-474c-a0dc-ed72de8f419f" />

# Full subtractor

<img width="1731" height="959" alt="Screenshot 2025-11-26 144142" src="https://github.com/user-attachments/assets/eb656afc-20ae-4d26-9971-e0d4f6340e83" />

# Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.

