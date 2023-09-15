# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
1. Use module projname(input,output) to start the Verilog programmming.
2. Assign inputs and outputs using the word input and output respectively.
3. Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
4. Use each output to represnt onre for differnce and the other for borrow.
5. End the verilog program using keyword endmodule.





## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Jerushlin Jose JB
RegisterNumber:  212222240039
```
```
Half Subtractor

module halfsub(a,b,diff,borrow);
input a,b;
output diff,borrow;
assign diff=a^b;
assign borrow=(~a)&b;
endmodule
```
```
Full Subtractor

module fullsub(a,b,bin,diff,borrow);
input a,b,bin;
output diff,borrow;
assign diff=a^b^bin;
assign borrow=((~a)&b)+(~(a^b))&bin;
endmodule
```

## RTL Diagram:
### Half Subtractor

![RTL Halfsub](https://github.com/Aswinth21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120236638/1405b5b6-d889-4747-be8a-e636fc78e6b9)

### Full Subtractor

![RTL Fullsub](https://github.com/Aswinth21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120236638/53f2d536-129c-4e7d-9a78-02338826337a)


## Truthtable
### Half Subtractor

![WhatsApp Image 2023-09-08 at 09 23 55](https://github.com/Aswinth21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120236638/8417db91-3f21-4678-8304-8fffa9b37486)

### Full Subtractor

![TT Fullsub](https://github.com/Aswinth21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120236638/263a6edf-9b46-41e0-a827-e78a5975d9b8)


## OUTPUT WAVEFORM:
### Half Subtractor

![Waveform halfsub](https://github.com/Aswinth21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120236638/a2e82798-fb8b-4c9b-8afd-80868d75742f)

### Full Subtractor

![Waveform Fullsub](https://github.com/Aswinth21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120236638/8b8780e8-8821-44e8-bcb6-0f4e6f705981)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
