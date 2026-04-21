# Final-Project---Battery-Monitoring-Report-and-Demo-
GitHub Repo for Hybrid Electric Vehicles

The BMS-I2C-LCD code will take the ADC value from SARADC_VIN2 (PIN 37 on Rock5C) and print the current battery voltage, percentage, and low voltage warning when battery is less than 30%.

Due to the high value of the resistors, R1 = 46400 Ohms and R2 = 6400 Ohms, the internal capacitor in the Rock5C's ADC never fully charges, thus outputing a lower than expected value into the program. The voltage divider works as intended, because of that capacitance, a manual correction was added into the code. 

Line 26: voltage2 = voltage * (8.75) * 1.91

The additional multiplication of 1.91 is to correct the value of the ADC. This is not the correct way to fix the issue, a better solution would be to use resistance values that are 10x less than the current ones and to add a capacitor to help stabilize the voltage. However, due to time constrants, this was not a feasible option. 

---------------------------------------------------------------------------
The BMS Video shows the battery voltage and percentage being displayed on the LCD along with the Detect.py file running for the camera. This shows that both files can be running at the same time without any issues. 
