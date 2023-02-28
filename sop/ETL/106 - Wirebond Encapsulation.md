# ETL:106 - Wirebond Encapsulation

Author: **Jahid Hossain**, Caleb Fangmeier

Last Edited: February 14, 2023

## Abstract
   This SOP covers step-by-step the procedure of encapsulating the wire bonds on assembled modules.


## Required Tools and Materials

  ### Instruments for the Encapsulation
  
   - Nordson EFD 3-Axis EV Series Automated Fluid Dispensing Robot
   - Nordson EFD's Ultimus I dispensers
   - Height Sensor 
   - Fully assembled module on carrier
 <table>
  <tr>
    <td><img src="https://github.com/jhosain/Lab-Instructions/blob/5c053aab6d16644239808934567de8e67dd6179b/sop/ETL/106_materials/images/Mini_Gantry.png" alt="Alt Text" height="500"></td>
    <td><img src="https://github.com/jhosain/Lab-Instructions/blob/49ff5233f0ebae66c431dc95049ced5a41a420ab/sop/ETL/106_materials/images/Height_Sensor.png" alt="Alt Text" height="500"></td>
  </tr>
</table>
  
  ### Tools and Materials to Prepare the Encapsulant
  
   - Centrifugal Machine
   - Sylgard 186 Silicon Elastomer Kit (Base & Curing Agent)
   - Nordson EFD 2K 50ml Manual Cartidges Dispenser Gun, 10:1 ratio
   - Nordson EFD 2-Part Cartidegs with Sealing Cap, 10:1 ratio
   - Nordson EFD 2K, 10:1 S & L 50ML Pistons
   - Nordson EFD Precison Tips: 23GA (Orrange) 30GA (Pink) 32GA (Yellow)
   - Electronic Balance
   - Disposable Spiral Mixer and 1cc & 10cc Syringe, and Spatula
   - Optimum Syringe Barrel (5cc), Syringe Barrel Adapters, Piston and Tip Caps 
   - Stand 
   - Vacuum Oven

<table>
  <tr>
    <td><img src="https://github.com/jhosain/Lab-Instructions/blob/adc72fadc96f47e0cd351dcefd4421fe60658971/sop/ETL/106_materials/images/Mixing_tools.pmg.png" alt="Alt Text" height="500"></td>
  </tr>
</table>

## Required Software

- Nordoson Dispense Motion
- Windows based Operating System


## Required Training

Users must complete a short training program with either Caleb or another trained person to conduct this activity.

## Procedure

### Encapsulant (Sylgard 186) Mixing Procedure

 - Wear the gloves and cover the work bench with the Kimwipes
 - Place the 2-Part Cartidge barrale on a stand to hold 
 - Fill up the smaller ratio part of the 2 part cartidge by the sylgard curing agent using a 1cc syring, seal it up by the piston 
 - Fill up the large part of the 2 part cartidge by the elastomer base using a 10cc syringe or using an spatula, seal it up by the piston 
 - Setup the cartidge barrel on the dispenser gun                                                                                                           
 
 

### Encapsulation Procedure

  ### Step 1: Preapring and Moungint the Dispenser Syringe 
  
  - Attach the spiral mixer to the cartidge barrel 
  - Screw the blue cap onto the syringe
  - Pour mixed encapsulant into the 5cc syringe by pressing the dispenser gun
  - Use the centrifuge machine to remove the air bubbles from the dispensing syrige barrel
  - Put the filled syringe and an empty syringe into opposite positions in the centrifuge rotor. Degas by running the centrifuge at 5000 RPM for at least 8 minutes.
  - Once the encapsulant has been sufficiently centrifuged, then the user should take the encapsulant out, look for any major air pockets, and replace the blue cap with a precision dispanse needle.
  - Screw the syringe to the adapter and mount the syringe on the robot stand
  
  ### Step 2: Purging the Dispenser Syring 
  
  - Turn on the computer and open the nordoson dispense motion software 
  - Purging can be done via hand by pressing the dispensing button on the EFD Ultimus
  - Click on the system settings and click on open tab
  - Clink on the Purge button
  - Once the user sees encapsulant coming out slightly then stop and gently touch a kimwipe to the needle tip
  
  ### Step 3: Starting the Program
  
  - Open a saved program or create a new program
  
  ### Step 4: Calibrating the Needle Tip 
  
  - Hit the "Needle Z Detect" button to calibrate the z height. 
  - Hit the "Needle XY Adjust" button to calibrate the X & Y position. 
  
  ### Step 5: Despensing (Potting)
  
  - Once everything is set the user may go with the saved program or modify the program, allowing the mini-gantry to pot the wire bonds
  - Place the assembled module carrier on the robot base plate
  - Start potting by running the program
  
  ### Step 6: Removing Syringe from Holder
  
  - Once the working life of encapsulant is over dump the syringe and replace it by new one if needed
  
  ### Step 7: Saving and Ending the Program
  
  - If the program is modifed don't forget to save the program
  
  ### Step 8: Creating and Publishing Report
  
  - Report should contain the batch number and some of the results information from the result section below
  
  ### Step 9: Transfering Plates to the Curing Vacuum Oven
  
  - Once the potting is finished put the encapsulated module into the vacumm oven to cure at 60˚C for 30 mins
    
  ### Step 10: Transfering Modules to the Carrier
  
  - Once the encapsulated module are cured transfer them to a designated dry area
  
  ## Results 
  

  - Needle tip size
  - Air Pressure
  - Encapsulant Bead Dimensions (Width, lenght, Height)
  - Tip and Bond Pad Gap
  - Rate of motion of the Syringe ( Flow Rate)
  - Number of Passes
  - Line Dispense Setup
  - Backtrack Setup
  - Z Clearance Setup
  - Timming
  - Curing Time
  - Bead Dimension after Curing
  - Bead Dimension on PCB w/wo wirebonds
  - Bead Dimension on Glass Plate
  - Bead Dimension vs Speed/Air_Pressure/Tip_Gap/Pass_No/Time/Cure_Time/Tip_Size/Surface


  ## Timming
   
  - Mixing sylgard and filling cartidg barrel: ~ 30 mins
  - Mixing, filling syringe ~ 10 mins
  - Degassing (removing air bubbles), mounting syringe on robot ~ 10 mins
  - Calibration and pruging time: ~ 10 mins
  - Potting Time 
  * 1 pass ~ 3.5 mins and Total time for a single module ~ 15 mins
  * 2 passes ~ 7 mins on a pad. Total time for four pads ~ 30 mins
  
  - Useful Pot life from time of mix ~ 90 mins
  - Curing time at room temperuture ~ 8 hrs
  - Curing time in oven at 60˚C ~ 30 mins and at 50˚C ~ ?
  

  ## Height Sensor Mounting and Programming
  
  ## Example Scripts
  
  ## Dispenser Manuals and Documentations
  
  https://github.com/jhosain/Lab-Instructions/blob/768eb1cc1a815b52ed1e035f0b792decac89b61e/sop/ETL/106_materials/Nordson-EFD-Ultimus-I-II-Operating-Manual.pdf
