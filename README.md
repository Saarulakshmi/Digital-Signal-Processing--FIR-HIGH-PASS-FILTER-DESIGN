# Digital-Signal-Processing--FIR-HIGH-PASS-FILTER-DESIGN
## AIM:
To generate design of High pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the hIGH Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
 clear all; % clear screen
 close all; % close all figure windows
wc=input('enter the value of cut off frequency');
M=input('enter the value of filter');
alpha=(M-1)/2;
eps=0.001;
%High Pass Filter Coefficient
n=0:1:M-1;
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps))
%Bartlett Window Sequence
n=0:1:M-1;
wh=1-(2*abs(n-((M-1)/2))/(M-1))
hn=hd.*wh
% Plot the High Pass Filter with Bartlett Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```
## OUTPUT:
![WhatsApp Image 2026-03-31 at 8 45 52 PM](https://github.com/user-attachments/assets/eb866890-f9d5-489f-b67b-3360fb738f46)

## RESULT:
Thus the design of high pass FIR digital filter using bartlett waveforms were 
plotted and output was verified
