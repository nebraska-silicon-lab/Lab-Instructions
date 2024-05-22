# TFPX:201 - TFPX Module Testing

Author: Jahid Hossain

Last Edited: May 22, 2024

## Abstract

This SOP covers step-by-step the procedure of electrical testing on assembled TFPX modules using the FC7 test setup.

## Additional Information

- [SCC Configuration](https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/RD53A_SCC_Configuration.pdf)
- [SCC Schematics](https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/RD53A_SCC_Rev1.0.pdf)
- [RD53A TWiki](https://twiki.cern.ch/twiki/bin/viewauth/RD53/RD53ATesting)
- [SOP at production site](https://docs.google.com/document/d/1fTHaYf8PxtNhBlqVFKXlMlH5xZvBGXrcpEw__MC7PI8/edit#heading=h.w4xt7cwcb3fq)

## Required Materials

- Chiller
- UIC Cold box
- Peltier
- FC7 board
- KSU FMC card
- Keithley 2260B-80-13 Low Voltage Power Supply
- Keithley 2410 High Voltage Power Supply
- Multimeters
- Probe Card
## Required Training

## Procedure

### Turn on the Chiller:

- Set the internal temperature to 15˚C using the button on the chiller display.
- Ensure water is flowing through the cold box.
- Monitor water flow and check for any unexpected water leaks inside the cold box for safety.

### Login to the FC7 Computer:

- Password: huskershuskers

### Open the GUI:

- Open the terminal and navigate to the “Ph2_ACF_GUI” folder.
- Run "source portfinder.sh" to find the corresponding ports for LV, HV, and Peltier.
- Update the device ports in “GUI/siteConfig.py”.
- Run bash run_docker.sh to open the GUI.
- No password is currently set for the username "localexpert".

### Read Humidity:

- This feature is currently not working. ( will be updated soon on GUI )
- If the dew point is above the operating temperature, turn on the dry air blower.

### Plug in the Peltier power cable.
- In the GUI:
              . Start the Peltier.
              . Set the temperature.
              . Monitor the temperature reading.
              . Once the temperature reading is close to the set temperature, turn on the Peltier.
              . Check the polarity. (optional)
              . Continuously monitor the temperature throughout the operation, ensuring it stays within +/- 0.5˚C of the set temperature.

### Mount the Module:

- Mount the module on the aluminum base plate and tighten the screws properly.
- Wear a static wristband.
- Plug in the LV, HV, and DP cables carefully.

### Powering the Module

- Turn on the LV and operate manually at constant current. Ensure the current is at zero before connecting the LV plug to the module.
- Click on the output button.
- Gradually increase the constant current to the optimal value and read the voltage:
 	          . For 1x2 CROC: 4.5 A
 	          . For 2x2 CROC: 7.5 A
- Turn off the LV (output).

### SLDO Scans

- Perform SLDO scans using a multimeter and the probe card.
- Use a black cover with holes for the probe card to protect the module.
- Operate the LV PS manually.
- No HV connection is required for SLDO scan.
- Measure VDDD and VDDA for all ROCs using a multimeter.
- Measure the input voltage at the power adapter board using a multimeter. The input voltage shouldn't exceed 2 V at 7.5 A for a 2x2 CROC module.
- VDDA & VDDD should reach 1.2 V.
- Plot the IV characteristics curve.

### Electrical Tests:

- Turn on FC7 and connect it to the GUI.
- Turn on the LV and HV and connect the devices using the GUI.

## Bias Scan:

- Follow the instructions in the GUI to perform the Bias Scan.

## Pixel Alive Scan:

- Follow the instructions in the GUI to perform the Pixel Alive Scan.

## Noise Scan (for troubleshooting purposes only):
	
- Perform this scan only if troubleshooting is required.

### Update the Purdue Database:
    
- Log the results and updates in the Purdue database.

### Report the Results:

- Document the results on the lab log or worksheet.

### Turning Off All Devices:
	
- Turn off the Peltier.
- Turn off the LV, HV, and FC7.
- Close the GUI.
- Unplug the Peltier power cable.
- Turn off the chiller.
- Turn off the dry air flow if it is on.

### Unmount the Module:

- Unmount the module and return it to the dry cabinet in the clean room.
- If the job is not finished, keep the module inside the cold box with the lid closed.



              





