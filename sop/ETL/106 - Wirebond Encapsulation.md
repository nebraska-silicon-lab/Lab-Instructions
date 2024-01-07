# ETL:106 - Wirebond Encapsulation

Author: **Jahid Hossain**, Caleb Fangmeier

Last Edited: January 05, 2024

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
   - Lindberg/Blue-M Laboratory Vacuum Oven
  

<table>
  <tr>
    <td><img src="https://github.com/jhosain/Lab-Instructions/blob/adc72fadc96f47e0cd351dcefd4421fe60658971/sop/ETL/106_materials/images/Mixing_tools.pmg.png" alt="Alt Text" height="500"></td>
    <td><img src="https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/4ebc7bd9b4cc317091ead333f8c5d22cf70e17fb/sop/ETL/106_materials/images/Screen%20Shot%202023-02-28%20at%205.26.35%20PM.png" alt="Alt Text" height="500"></td>
  </tr>
</table>

## Required Software

- Nordoson Dispense Motion
- Windows based Operating System


## Required Training

Users must complete a short training program with either Caleb or another trained person to conduct this activity.

## Procedure

### Preparation of Encapsulant Cartridge (Sylgard 186 Base & Cure Mixing Procedure)

 - Don gloves and use Kimwipes to cover the workbench.
 - Use a stand to hold the 2-Part Cartridge barrel.
 - Fill the smaller ratio section of the 2-part cartridge with the Sylgard curing agent using a 1cc syringe, and seal it with the piston.
 - Fill the larger ratio section of the 2-part cartridge with the elastomer base using a 10cc syringe or spatula, and seal it with the piston.
 - Set up the cartridge barrel on the dispenser gun.
                                                                                                        
### Encapsulation Procedure

  ### Step 1: Encapsulation Preparation
  
 - Activate the vacuum system.
 - Place the weight instrument inside the oven and set the temperature to 100˚C for heating.
 - Turn on the compressed air at 100 psi.
 - Activate the Gantry.
 - Position the wirebonded module carrier on the mini gantry.
 - Launch the program on the PC.
 - Perform the Needle Z detect procedure.
 - Verify the z height and make necessary adjustments in the program.
  
  
  ### Step 2: Preapring and Moungint the Dispenser Syringe 
  
  - Connect the spiral mixer to the cartridge barrel.
  - Securely fasten the blue cap onto the syringe.
  - Pour mixed encapsulant into the 5cc syringe to about half of its capacity using the mixer and by pressing the dispenser gun.
  - Utilize the centrifuge machine to eliminate air bubbles from the dispensing syringe barrel.
  - Arrange the filled syringe and a similarly weighted syringe in opposing positions within the centrifuge rotor. Degas by running the centrifuge at 5000 RPM for a minimum of 10 minutes.
  - Once the encapsulant has undergone sufficient centrifugation, remove it and inspect for any significant air pockets.
  - Replace the blue cap with a tightly screwed precision dispense needle (23GA).
  - Insert a white syringe barrel piston into the syringe, pushing it all the way in to ensure there are no visible trapped air pockets.
  - Securely attach the syringe to the adapter and mount it on the robot stand.


  ### Step 3: Starting the Program

  - Open a saved program or create a new program.
  - Program should have included the Needle Z detect calibration and fiducial mark adjustment
   
  ### Step 5: Despensing (Potting)
  
  - Once everything is set the user may go with the saved program or modify the program, allowing the mini-gantry to pot the wire bonds
  - Place the assembled module carrier on the robot base plate
  - Start potting by running the program
  - Make sure to monitor the sylgarde deposition by watching the needle. Should it veer off path, or dislocated in any way, STOP. 
  
  <table>
  <tr>
    <td><img src="https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/34b568780d223a462ff5e476d205c3dd24d595a4/sop/ETL/106_materials/images/0%2058.jpeg" alt="Alt Text" height="500"></td>
  </tr>
</table>
  
  ### Step 6: Removing Syringe from Holder
  
  - Once the working life of encapsulant is over dump the syringe and replace it by new one if needed
  
  ### Step 7: Saving and Ending the Program
  
  - If the program is modifed don't forget to save the program
  
  ### Step 8: Survey of the Encapsulation using the Gantry Machine

  - Load the script for the encapsulant survey.
  - Position the module carrier on chunk 3 on the gantry table.
  - Run the encasulant survay script 

  ### Step 8: Base Plate Placement using the Gantry Machine
      
   - Place the base plate.
   - Remove the film from the base plate and place it on the carrier.
   - Run the base plate script.
  
  ### Step 9: Encapsulating Bias Wirebonds

   - Right after the installation of the base plate, place the module carrier on the mini-Gantry.
   - Execute the program for bias wirebonds encapsulation on the mini-Gantry.

  ### Step 10: Curing the Encapsulation

   - Once the modules are completely encapsulated place them inside the weight.
   - Insert the weight with the module carrier into the vacuum oven at 100˚C for 15 minutes without activating the vacuum.
   - Allow the module carrier to remain in the oven for an additional 15 minutes with the vacuum activated.
    
  ### Step 11: Transfering Modules to the Dry Cabinet

  - Once the encapsulated module are cured transfer them to a designated dry area
  
  ### Step 12: Creating and Publishing Report on the Lablog
  
  - Report should contain the batch number and some of the results information from the result section below
  
  ### Step 13: Wrapping up

  - Turn off the equipments and make sure the scripts are saved
  
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
  
  - Filling cartidg barrel: ~ 30 mins
  - Mixing, filling syringe ~ 15 mins
  - Degassing (removing air bubbles), mounting syringe on robot ~ 10 mins
  - Dispenseing and Potting ~ 25 mins [Setup: Pressure 100 psi, Needle tip 23GA, Pass no 2]
  - Encapsulation Survey time ~ 15 mins
  - Base Plate installatioon ~ 5 mins
  - Bias Wirebonds Enacapsulation dispense time ~ 15 mins [Setup: Pressure 100 psi. 23 GA needle tip used.]
  - Useful Pot life from time of mix ~ 90 mins
  - Curing time at room temperuture ~ 8 hrs
  - Curing time in oven at 100˚C ~ 15 mins and at 50˚C ~ 60 mins
  

  ## Height Sensor Mounting and Programming
  
  https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/10c3c8147399fd2c56cc56ffa02cdff5624fff0c/sop/ETL/106_materials/Height%20Sensor%20Instructions%2006_06_2022.pdf
  
  https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/10c3c8147399fd2c56cc56ffa02cdff5624fff0c/sop/ETL/106_materials/Scripts/ht%20sensor.SRC
  
  ## Example Scripts
  
  https://github.com/nebraska-silicon-lab/Lab-Instructions/blob/64b2fda4bc70a23b71700733215d9b36aa51efb0/sop/ETL/106_materials/Scripts/Dispanse_allline.SRC
  
  ## Dispenser Manuals and Documentations
  
  https://github.com/jhosain/Lab-Instructions/blob/768eb1cc1a815b52ed1e035f0b792decac89b61e/sop/ETL/106_materials/Nordson-EFD-Ultimus-I-II-Operating-Manual.pdf
