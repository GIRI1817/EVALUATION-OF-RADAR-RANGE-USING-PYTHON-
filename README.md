# EVALUATION-OF-RADAR-RANGE-USING-PYTHON-

## Aim:

To calculate the maximum range of a radar system using the Radar Range Equation and verify the results 
through Python programming.

## Theory:

The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum 
range at which a radar can detect a target. It is given by:

<img width="573" height="442" alt="image" src="https://github.com/user-attachments/assets/ba374d30-d11f-41e5-a4fc-a42dde71d8e7" />

## Procedure:

1. Set Up the Python Environment: Ensure that Python is installed on your system. You can use 
Anaconda for managing Python packages and environments, or any other Python IDE of your choice. 
2. Import Necessary Libraries: Import the math library in Python. 
3. Define the Radar Range Equation Function: Create a function to calculate the maximum range using 
the Radar Range Equation. 
4. Input Parameters for the Radar System: Define the input parameters such as transmitted power, 
transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power. 
5. Calculate the Maximum Range: Use the function to calculate the maximum range of the radar. 
6. Execute the Program: Run the Python script to calculate and display the maximum range of the radar.


## Algorithm:

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

## Program:
```
import matplotlib.pyplot as plt

# Given values
Pt = 1000
G = 40
lambda_ = 0.05
sigma = 10
pi4 = (4 * np.pi) ** 3

R = np.linspace(1e3, 200e3, 500)     # Range
Pr_R = (Pt * G**2 * lambda_**2 * sigma) / (pi4 * R**4)
Pr_R_dB = 10 * np.log10(Pr_R)

plt.figure(1)
plt.plot(R / 1000, Pr_R_dB)
plt.xlabel("Range (km)")
plt.ylabel("Power Received (dB)")
plt.title("Received Power vs Range (Radar Equation)")
plt.grid(True)

Pt_values = np.linspace(100, 10000, 500)
R_fixed = 50e3
Pr_Pt = (Pt_values * G**2 * lambda_**2 * sigma) / (pi4 * R_fixed**4)

plt.figure(2)
plt.plot(Pt_values, Pr_Pt)
plt.xlabel("Power Transmitted")
plt.ylabel("Power Received")
plt.title("Received Power vs Transmitted Power")
plt.grid(True)

G_values = np.linspace(5, 60, 500)
Pt_fixed = 3000
Pr_G = (Pt_fixed * G_values**2 * lambda_**2 * sigma) / (pi4 * R_fixed**4)

plt.figure(3)
plt.plot(G_values, Pr_G)
plt.xlabel("Gain")
plt.ylabel("Power Received")
plt.title("Received Power vs Antenna Gain")
plt.grid(True)

plt.show()
```
## Output:
   
<img width="1158" height="835" alt="512533058-d0d8553b-6236-4f66-bd9d-90399ac977a0" src="https://github.com/user-attachments/assets/dd6a3d6e-fb00-4e49-8b26-852d1cdc6917" />
<img width="1094" height="828" alt="512532978-a7261c1d-0a30-44f7-89a8-288c6356782b" src="https://github.com/user-attachments/assets/e26633d8-f72d-41a7-93e4-e5d74c02e892" />
<img width="1082" height="840" alt="512533363-89a8d24f-bb1a-434c-b8bc-a96e64341cbc" src="https://github.com/user-attachments/assets/502944b7-5fda-4d75-b0c8-2be2e5635bc0" />







## Result:
   
The maximum range of the radar system was successfully calculated using Python. By providing the required radar parameters and executing the radar range function, the program produced the correct maximum detectable range value. Thus, the radar range evaluation using Python was completed and verified.



