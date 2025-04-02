# TFPX:201 - TFPX Module Testing

Author: Jahid Hossain

Last Edited: Apr 2, 2025

## Abstract

This SOP describes step-by-step assembly quality control (QC) testing procedures of fully assembled TFPX CROC v2 double and quad modules, with focus on electrical lab testing and FCy test setups.


## Additional Information

- [SCC Configuration](https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/RD53A_SCC_Configuration.pdf)
- [SCC Schematics](https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/RD53A_SCC_Rev1.0.pdf)
- [RD53A TWiki](https://twiki.cern.ch/twiki/bin/viewauth/RD53/RD53ATesting)
- [RD53B](https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/RD53B_CMS_Main.pdf)
- [SOP at production site](https://docs.google.com/document/d/1fTHaYf8PxtNhBlqVFKXlMlH5xZvBGXrcpEw__MC7PI8/edit#heading=h.w4xt7cwcb3fq)
- [Ph2_ACF User guide](https://ph2acf.docs.cern.ch/innerTracker/calibrations/)
  
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
- ADC Board
  
## Required Training

Users must complete a short training program with either Aman or another trained person to conduct this activity.

## Procedure

### Turn on the Chiller:

- Set the internal temperature to 5˚C using the circular button on the chiller display.
<table>
  <tr>
    <td><img src="https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/images/Chiller_Setup.jpeg" alt="Alt Text" height="250"></td>
  </tr>
</table>
- Adjust chiller controller at internal control if it is not adjusted before. 
<table>
  <tr>
    <td><img src="https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/images/Chiller_03.jpeg" alt="Alt Text" height="250"></td>
    <td><img src="https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/images/Chiller_01.jpeg" alt="Alt Text" height="250"></td>
    <td><img src="https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/images/Chiller_02.jpeg" alt="Alt Text" height="250"></td>
  </tr>
</table>
- Ensure water is flowing through the cold box.
- Monitor water flow and check for any unexpected water leaks inside the cold box for safety.
- There is a sensor inside the cold box that can also detect any water leaks, make sure the sensor is functional.

### Login to the FC7 Computer:

- Password: huskershuskers

### Open the GUI:

- Open the terminal and navigate to the “Ph2_ACF_GUI” folder.
- Run "source portfinder.sh" to find the corresponding ports for LV, HV, and Peltier.
- Update the device ports in “GUI/siteConfig.py”.
- Run bash run_docker.sh to open the GUI.
- On the login screen you can use either of the following usernames to log in locally (bypassing connection to the database).
  For non-expert mode: username = local (in development) For expert mode: username = localexpert
  To connect with database: username = *your Panthera username*  password = *your Panthera password*
  Note. it will only work in the expert mode if you have panthera admin access (https://panthera.fit.edu/) 

### Read Humidity:

- If the dew point is above the operating temperature, turn on the dry air blower.
<table>
  <tr>
    <td><img src="https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/master/sop/TFPX/201_materials/images/humidity.jpg" alt="Alt Text" height="250"></td>
 </tr>
</table>	  

### Plug in the Peltier power cable.
- In the GUI:
              . Start the Peltier.
              . Set the temperature at 10˚C.
              . Monitor the temperature reading.
              . Once the temperature reading is close to the set temperature, turn on the Peltier.
              . Check the polarity. (Should be set at HEAT WP2+ and WP1-)
              . Continuously monitor the temperature throughout the operation, ensuring it stays within +/- 0.5˚C of the set temperature.


### Module Handling

The front-end chip (FE) chip is an electrostatic sensitive device and must be handled properly to avoid damage from electrostatic discharge (ESD). The working environment, including tools, materials and containers for handling and transport of modules should provide for ESD protection. All operators dealing with the items must be grounded to same potential as the equipment with at least the use of grounding wrist straps. To avoid damage from particulates bare modules, module PCBs and assembled modules must always be handled in a clean room environment with a particle count corresponding to at least class 10000 (ISO 7), or better, using properly designed tools and materials to prevent touching with bare hands and applying excessive pressure. If modules are to be transported between cleanrooms, a suitable carrier should be used, and the container should remain closed during transportation. The container should be externally cleaned on re-entering the cleanroom. 

- Use ESD protected module carrier shipping box to transport module from clean room to testing station.


### Mount the Module:

- Wear surgical gloves and a static wristband before mounting module.
- Mount the module on the aluminum base plate and tighten the screws properly.
- Plug in the LV connector first, then HV and DP cables carefully.

### Powering the Module

- Turn on the LV and operate manually at constant current. Ensure the current is at zero before connecting the LV plug to the module.
- Click on the output button.
- Gradually increase the constant current to the optimal value and read the voltage:
 	          . For 1x2 CROC: 4.5 A
 	          . For 2x2 CROC: 7.5 A
- Turn off the LV (output).

### Manual SLDO Scans using multimeter

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

### Assembly Quality Control (QC) Tests:

TFPX Assembly QC tests contains,

- SLDOScan (currently not supported by GUI)
- IVCurve (Bias scan)
- CommunicationTest
- PixelAlive_Digital
- PixelAlive_Analog

### Upload the test on Panthera:

Once the scans are done, check the results. If you are satisfied, upload the results on Panthera by clicking the tab "Upload Results." This feature will only work if you log in using your Panthera credentials. 

## Additional Tests (for troubleshooting purposes only):

- Noise Scan
- BER (FMC) Test (more details, https://unl.nebraskadetectorlab.com/submission/6584)

### Update the results on the Purdue Database:
    
- Upload the results in the Purdue database (https://www.physics.purdue.edu/cmsfpix/Phase2_Test/edit.php)

### Store the results:

- Save the log of the test sequences
- Collect all the results into a single folder
- If possible, store the results on the cloud

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





              





