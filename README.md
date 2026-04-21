# Final-Project---Battery-Monitoring-Report-and-Demo-
GitHub Repo for Hybrid Electric Vehicles

The BMS-I2C-LCD code will take the ADC value from SARADC_VIN2 (PIN 37 on Rock5C) and print the current battery voltage, percentage, and low voltage warning when battery is less than 30%.

Due to the high value of the resistors, R1 = 46400 Ohms and R2 = 6400 Ohms, the internal capacitor in the Rock5C's ADC never fully charges, thus outputing a lower than expected value into the program. The voltage divider works as intended, because of that capacitance, a manual correction was added into the code. 
