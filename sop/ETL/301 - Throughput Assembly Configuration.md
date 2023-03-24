# ETL:301 - Throughput Assembly Configuration

Author: Caleb Fangmeier and Hayden Swanson

Last Edited: March 24, 2023

## Abstract
This document is to provide instructions to get the correct positions and other site specific information for the script that does the pick and place of the ETROC/LGAD sub-assemblies on the Module PCB for the throughput demonstration. The site specifc information is held in a configuration file called "Throughput_Assy_Configuration.txt" (NOT TP_Config.txt this holds non-site specific information like the geometries of the pieces). I will provide instructions on how to get the following configurations and measurements:

1. Chuck Numbers
2. Module PCB positions and rotations
3. ETROC/LGAD sub-assembly positions and rotations

## Required Materials

You will need the following equipment:
- Staging plate for the ETROC/LGAD sub-assemblies
- Assembly Plate for the Module PCBs 
<img src="https://user-images.githubusercontent.com/70072888/227585331-58b6eded-a7b2-43ae-8e3f-092bacba310b.png"  width=50% height=50%>
- Throughput ETROC/LGAD sub-assemblies <img src="https://user-images.githubusercontent.com/70072888/227582484-cb1e6671-7a6b-4155-ae2f-4b942da2c486.jpg"  width=25% height=25%>
- Throughput Module PCB <img src="https://user-images.githubusercontent.com/70072888/227586341-417144b4-194f-44b7-b187-433f3ce7b04f.png"  width=25% height=25%>

## 1. Chuck Numbers
In the Throughput_Assy_Configuration file there is a section like so:
#chuck numbers
#Bottom is the chuck that holds the assembly plate
chuck_number.bottom: 3
#Top is the 16-pocket chuck that stages the ETROC+LGAD subassemblies as well as the baseplates
chuck_number.top: 4

"chuck_number.bottom" is the chuck that holds the Assembly Plate for the Module PCBs. And the "chuck_number.top" is the chuck that holds the ETROC/LGAD sub-assemblies. Note, chuck numbers for the positions of your chuck should already specified in your main configuration file at your gantry site. In your file there should be a section like, "graph_motion.pos.etl_chuck_1: {726,700,0}" and the chuck number is one in this case. 

##2. Module PCB Positions and Rotations

To get the positions and rotations of the Module PCB you need to go to measure its 4 fiducials using your gantry camera (while it is of course staged on the chuck, according to chuck_number.bottom). You then use the FIT function in gScript. I will now explain which 4 fiducials to call the top left (TL), top right (TR), bottom left (BL) and (BR); as well as the needed geometry for the FIT. 

The convention for TL, TR, BR, and BL is shown here in this picture.
<img src=https://user-images.githubusercontent.com/70072888/227590837-eb1dd635-d767-4cf2-a3f4-d75b6fa10ea1.png width=25% height=25%>

1. Using this convention you take you move your gantry to the fiducials (activating the micro controller with the MPGON command is the easiest). 
2. Turn on the camera with the VIDEO command to look for the fiducials. 
3. Once you are at the fiducial note if its the TL, TR, BR, or BL fiducial as governed by the convention above. Then save it as variable with COPY $TL or COPY $TR etc... depending on the fiducial.
4. Get the geometry of the Module PCB from the TP_Config.txt file, for the FIT command, by runnign the commmand: LOADCONFIG "" Scripts\ETLModules\ThroughPut\TP_Config.txt        OR whaever path it is for you to the TP_Config.txt file
5. Run the command: FIT $pos $rot Module_PCB $TR $BR $BL $TL
6. Print out the $pos and $rot with: PRINT %v $pos and PRINT %q $rot
7. Copy paste these values into the Throughput_Assy_Configuration file where you replace the {} with your position vector and rot quaternion: 
default.Module_PCB.3.1.pos: {649.703701,298.164172,63.961246}
default.Module_PCB.3.1.rot: {-0.000069,0.001439,0.000857,-0.999999}

IMPORTANT: The 3 corresponds to the chuck_number.bottom and the 1 is just a position number on the plate. There are 4 positions on the Assembly Plate for Module PCBs so you have 4 of these numbers: 1, 2, 3, and 4.

##2. ETROC/LGAD sub assembly Positions and Rotations

### Step 2
