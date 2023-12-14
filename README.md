# Experiment--03-Half-Subtractor-and-Full-subtractor
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
*Connect the supply (+5V) to the circuit.
*Switch ON the main switch.
*If the output is 1, then the led glows.
## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: MANIKUMAR D.K
RegisterNumber:  23013588
1. Program to design a half subtractor:
module ex4(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=((~a)&b);
endmodule 
2. Program to design a full subtractor:
module ex41(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=a^b^bin;
assign borr=((~a)&b)|(b&bin)|((~a)&bin);
endmodule
```
Logic symbol & Truthtable
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: MANIKUMAR D.K
RegisterNumber:  23013588

## Output:

## TruthtableTRUTH TABLE:HALF ADDER
![image](https://github.com/MANIKUMARDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147215581/67416341-220a-4e4d-8539-b592dc965bc2)
## FULL ADDER
![image](https://github.com/MANIKUMARDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147215581/a3c5e0ec-d956-4d29-b2a9-ca421526ec23)





##  RTL realization 
## HALF ADDER
![image](https://github.com/MANIKUMARDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147215581/79c1423c-64a7-487a-bed0-1384dfcf87ab)
## FULL ADDER
![image](https://github.com/MANIKUMARDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147215581/5056a610-7dc3-426c-8b99-53c53031c7ac)


## Timing diagram 
## HALF ADDER 
![image](https://github.com/MANIKUMARDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147215581/253bbc43-9b71-48cf-85d5-973b67dca54d)
## FULL SUBTRACTOR
:![image](https://github.com/MANIKUMARDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147215581/af082215-cd24-47cf-bf6f-20a314ef7ca4)
RESULT :
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
