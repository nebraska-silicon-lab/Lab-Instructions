# TFPX:300 - Updating Module Tracking Database

Author: Caleb Fangmeier

Last Edited: October 1, 2021

## Abstract

This SOP covers how to update the HL-LHC TFPX Module Database (aka the Purdue database).

## Additional Information

  - The database URL can be found [here](https://www.physics.purdue.edu/cmsfpix/Phase2_Test/main.php)
  - If you require an account, you can request one from Matthew Jones (<mjones@physics.purdue.edu>).

## Required Materials

N/A

## Required Training

N/A

## Updating module location and status

First, navigate to the database using the url in [Additional Information](#Additional-Information).

![Login Page](https://user-images.githubusercontent.com/2569566/135650073-df9f98ac-1b34-408f-a95b-0d85a08c6c36.png)

Enter your login credentials and submit. This will bring you to the main page.

![image](https://user-images.githubusercontent.com/2569566/135650195-b02ef521-6686-4eb1-a6ac-31ff22ebaa52.png)

Here, you can modify your user information, add or change information associated with "parts", submit feedback, and generate reports. Our goal here is to find a specific part and update its status. Let's take part "MJ150" and update its status from "Glued" to "Wirebonded". 

First, we need to locate this part. Click on "Part annotation".

![image](https://user-images.githubusercontent.com/2569566/135651173-2898fd9e-2a51-4b18-943e-36418a986f33.png)

Here, we can specify which parts we want to search for. In this case, we happen to know that this part is located at Nebraska - so select that using the Location drop-down. Let's also specify the status as "Glued" using the Status drop-down. Now click "Search".

![image](https://user-images.githubusercontent.com/2569566/135651457-e3a95070-713f-4ad8-894c-341995a6c103.png)

There's the part we need, `MJ150`. Click the "Edit" button next to it.

![image](https://user-images.githubusercontent.com/2569566/135651656-67c6fe31-1b33-4325-afea-8f15f5a0c7cb.png)

Now all that remains is to use the Status drop-down to change the status to "Wire bonded" and click "Update". 

Now we are finished. But just to make sure that the changes went through let's go back to the part list. To get there, click the "Back to main" button at the foot of the page, then "Part annotation" again. This time, select Nebraska as the location and "Wire bonded" as the status.

![image](https://user-images.githubusercontent.com/2569566/135652246-ae8bc4fa-ede1-4b78-831f-956d29673a72.png)

And here we see that the module status has been updated successfully.
