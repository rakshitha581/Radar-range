# Radar-range
**Aim:**
 To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.
 ** Theory:**
 The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:
 ![WhatsApp Image 2025-11-26 at 09 32 51_6939cc8c](https://github.com/user-attachments/assets/3eb70800-e6cc-4db5-af00-4b8ca3062bea)
 
**Procedure:**
1.Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.
2.Import Necessary Libraries: Import the math library in Python.
3.Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.
4.Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.
5.Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.
6.Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

**Program:**
```
Pt = 500;
G = 500;
sigma = 1;
Ae = 10;

Smin = logspace(-12, -6, 100);
Rmax = ((Pt * G * sigma * Ae) ./ (16 * %pi^2 .* Smin)).^(1/4);
subplot(3,1,1);
plot(Smin, Rmax);

Ppeak = linspace(100, 10000, 100);
Rmax2 = ((Ppeak * G * sigma * Ae) ./ (16 * %pi^2 * 1e-5)).^(1/4);
subplot(3,1,2);
plot(Ppeak, Rmax2);

Gt = linspace(100, 2000, 100);
Rmax3 = ((Pt * Gt * sigma * Ae) ./ (16 * %pi^2 * 1e-5)).^(1/4);
subplot(3,1,3);
plot(Gt, Rmax3);
```
**Output:**
![WhatsApp Image 2025-11-26 at 09 33 31_041ac4d2](https://github.com/user-attachments/assets/28a0ddd3-80d9-4750-94e7-2d1e02da6645)
Manual calculation:
![WhatsApp Image 2025-11-26 at 11 52 05_1cf99164](https://github.com/user-attachments/assets/0e34974f-7375-4d36-ae9f-8b8fda9a42e4)
**Result:**
 The evaluation of radar range using python is verified


