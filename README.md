# EVALUATION-OF-RADAR-RANGE-USING-PYTHON-

# __Aim__:

To calculate the maximum range of a radar system using the Radar Range Equation and verify the results 
through Python programming.

# __Theory__:

The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum 
range at which a radar can detect a target. It is given by:

<img width="573" height="442" alt="image" src="https://github.com/user-attachments/assets/ba374d30-d11f-41e5-a4fc-a42dde71d8e7" />

# __Procedure__:

1. Set Up the Python Environment: Ensure that Python is installed on your system. You can use 
Anaconda for managing Python packages and environments, or any other Python IDE of your choice. 
2. Import Necessary Libraries: Import the math library in Python. 
3. Define the Radar Range Equation Function: Create a function to calculate the maximum range using 
the Radar Range Equation. 
4. Input Parameters for the Radar System: Define the input parameters such as transmitted power, 
transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power. 
5. Calculate the Maximum Range: Use the function to calculate the maximum range of the radar. 
6. Execute the Program: Run the Python script to calculate and display the maximum range of the radar.


# __Algorithm__:
   
Start the program.

Import the required Python libraries (Example: math or numpy for calculations).

Define all the radar input parameters, such as:

Transmitted power

Transmitter gain

Receiver gain

Radar frequency

Radar cross-section

Minimum detectable power

Calculate the wavelength from the given radar frequency.

Create a function that implements the radar range calculation using the input parameters.

Call the function with the defined parameter values.

Compute the maximum radar range inside the function.

Display the final calculated maximum range as output.

End the program.

# __program__:
```
clc
clear;
close;

Pt = 1000;
G = 40;
lambda = 0.05;
sigma = 10;
pi4 = (4*%pi)^3;

R = linspace(1e3, 200e3, 500);
Pr_R = (Pt .* G^2 .* lambda^2 .* sigma) ./ (pi4 .* R.^4);
figure(1);
Pr_R_dB = 10 .* log10(Pr_R);
plot(R/1000, Pr_R_dB);
xlabel("Power Received");
ylabel("Range");

Pt_values = linspace(100, 10000, 500);
R_fixed = 50e3;
Pr_Pt = (Pt_values .* G^2 .* lambda^2 .* sigma) ./ (pi4 .* R_fixed.^4);
figure(2);
plot(Pt_values, Pr_Pt);
xlabel("Power Received");
ylabel("Power Transmitted");

G_values = linspace(5, 60, 500);
Pt_fixed = 3000;
Pr_G = (Pt_fixed .* G_values.^2 .* lambda^2 .* sigma) ./ (pi4 .* R_fixed.^4);
figure(3);
plot(G_values, Pr_G);
xlabel("Power Received");
ylabel("Gain");
```



  # __Output__:
   
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/2dd5b3d2-7c2d-4e91-8cf3-8e65821a3052" />


# __Tabulation__:

![WhatsApp Image 2025-11-29 at 14 11 29_7d05ffc4](https://github.com/user-attachments/assets/d7304251-f500-4ed6-82fb-f13c6b4fa42b)



 # __Result__:
   
The maximum range of the radar system was successfully calculated using Python. By providing the required radar parameters and executing the radar range function, the program produced the correct maximum detectable range value. Thus, the radar range evaluation using Python was completed and verified.



