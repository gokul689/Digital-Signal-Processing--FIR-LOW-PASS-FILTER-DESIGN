# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
 clear all; % clear screen
 close all; % close all figure windows
wc=input('enter the value of cut off frequency');
N=input('enter the value of filter');
alpha=(N-1)/2;
eps=0.001;
%high Pass Filter Coefficient
n=0:1:N-1;
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps))
%hanning Window Sequence
n=0:1:N-1 
wh=0.5-0.5*cos((2*pi*n)/(N-1))
hn=hd.*wh
%plot the high pass filter with hamming window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
title('High Pass FIR filter using Hamming Window')
```

## OUTPUT:
<img width="697" height="620" alt="Screenshot 2026-03-18 125555" src="https://github.com/user-attachments/assets/dadf56d3-87ed-45d2-ba56-84682dd7fa81" />

## RESULT:
<img width="1396" height="710" alt="image" src="https://github.com/user-attachments/assets/2c6cc55c-6010-4a3b-922f-ae2557ca1612" />

