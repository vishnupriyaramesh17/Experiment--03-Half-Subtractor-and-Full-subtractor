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



Write the detailed procedure here 


## Program:

/*

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: Vishnupriya R

RegisterNumber:  212222110054

*/

module halfsubtractor(A,B,Diff,Borrow);

input A,B;

output Diff,Borrow;

wire x;

xor(Diff,Borrow);

not(x,A);

and(Borrow,X,B);

endmodule

module fullsubtractor(A,B,C,Diff,Borrow);

input A,B,C;

output Diff,Borrow;

wire p;

assign Diff=((A^B)^C);

not(p,A);

assign Borrow=((p&B)|(p&C)|(p&C));

endmodule


## Truthtable

![tt](https://user-images.githubusercontent.com/119393589/229293420-6936c9c9-52b6-4f88-a057-773821c903c6.png)


![tt full](https://user-images.githubusercontent.com/119393589/229293555-97abfd9b-4500-440a-bbd2-3cc8402ab436.png)

## RTL Realization

![full outt](https://user-images.githubusercontent.com/119393589/229293661-86327fb8-c1de-427f-974e-7869d8637b4e.png)

![half outt](https://user-images.githubusercontent.com/119393589/229293644-5da78448-26fe-43fe-9114-bb450969b480.png)

## Timing diagram 

![half timm](https://user-images.githubusercontent.com/119393589/229293687-ec7e179b-faa6-4ba4-8630-996a4358fbdc.png)
![full timm](https://user-images.githubusercontent.com/119393589/229293736-2e7ef60a-25e6-4511-843f-ad5a9b85a287.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
