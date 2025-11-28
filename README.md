# Mean-and-Variance
Aim

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

Equipments Needed

1.Computer with i3 Processor

2.SCI LAB

Algorithm

Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
Evaluate the Function: Compute the function values at each of these sample points.
Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
Display Results: Output the computed mean variance and Cross Correlation.
Procedure

Refer Algorithms and write code for the experiment.
Open SCILAB in System
Type your code in New Editor
Save the file
Execute the code
If any Error, correct it in code and execute again
Verify the generated results

Program
~~~~
Mean

function y = f(x)
    z = 3.7 * (1 - x)^2;
    y = x * z;
endfunction
function y = c(y_input)
    z = 3.7 * (1 - y_input)^2;
    y = y_input * z;
endfunction
a = 0;
b = 1;
EX = intg(a, b, f);
EY = intg(a, b, c);
disp(EX, "i) Mean of X = ");
disp(EY, "Mean of Y = ");
Varaince

function y=g(x)
    z= 3.7*(1-x).^2;
    y=x.^2 .*z;
endfunction
a=0;
b=1;
[EX2, errX2]= intg(a,b,g);
function y=h(yv)
    z= 3.7*(1-yv).^2;
    y=yv.^2 .*z;
endfunction
[EY2, errY2]=intg(a,b,h)
vX2=EX2-EX^2;
vY2=EY2-EY^2;
disp(vX2, "ii)Variance of X=");
disp(vY2, " Variance of Y=");
Cross Correlation

x=input("type in the referance sequence=");
y=input("type in the second sequence=");
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
~~~~~
Output Waveform
<img width="1920" height="1200" alt="Screenshot (121)" src="https://github.com/user-attachments/assets/3dc9c8af-2f87-43fe-a90a-72cc5286659c" />

Calculation

![WhatsApp Image 2025-11-28 at 18 22 43_010aa0be](https://github.com/user-attachments/assets/2370fe80-d5a7-47c7-88a6-fa50e19e9fbb)
![WhatsApp Image 2025-11-28 at 18 22 53_5ed1f589](https://github.com/user-attachments/assets/3ac90a70-3682-4a97-afe7-9f48d23ce4bb)


Result 

Thus the mean , variance and cross correlation are executed in Scilab and output is verified.


