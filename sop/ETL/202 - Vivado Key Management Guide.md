# ETL:202 - Vivado Key Management Guide
Author: Ian Reed
Last Edited: March 06, 2023

## Abstract
   This SOP covers step-by-step the procedure of installing a software key for Vivado


### WARNING: WE ONLY HAVE ONE KEY FOR NOW. CONTACT THE LAB MANAGER TO DETERMINE IF A NEW KEY IS NEEDED. IF YOU USE THE EXISTING KEY, THE PREVIOUS INSTALL OF VIVADO WILL BREAK

Start by oppening Vivado. Once it is running, open the Help tab at the top, and navigate to Manage License. This will open the Vivado License Manager program.

Navigate to the ```View System Information->View Host Infromation``` page. You will need this info modify the key.
Open the license managment website through the ```Get License->Obtain License``` tabs. Click Connect Now to be taken to the webpage.

From the webpage, navigate to the ```Manage Licenses``` tab. Scroll down and click ```Modify License```. Enter the information from the ```View Host``` metioned earlier. Click through the prompts until a window appears telling you a new key has been sent to the lab manager.

Get this file and move it to the ```$HOME/.Xilinx``` directory.

Back in the Vivado License Manager, navigate to ```Manage License->View License Status```. Click refresh and the keys should appear.
