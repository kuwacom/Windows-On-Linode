# windows-on-linode
 install windows on linode<br>

# How to install

## 1. Create node
First create a node without an image.<br>
![image](https://user-images.githubusercontent.com/83022348/194110266-76c87d91-ca29-4c82-bfc5-50d9f254b46d.png)<br>
**Click the red circle.*

## 2. Add storage
After creating the node, go to the storage tab and create a disk for windows.<br>
![image](https://user-images.githubusercontent.com/83022348/194113740-b3d4dd0a-02de-4146-ab22-7526e7e395e7.png)<br>
Enter as shown in the image.<br>
![image](https://user-images.githubusercontent.com/83022348/194112763-17040db5-e09f-44e6-a132-88ab27d0b444.png)<br>

## 3. Launch configuration
Next Go to configuration tab and add configuration.<br>
![image](https://user-images.githubusercontent.com/83022348/194113313-1df57d52-55c0-412a-84e0-aa75bf93de24.png)<br>
Change VMmode to "Full virtualization"<br>
![image](https://user-images.githubusercontent.com/83022348/194114538-7b377ccc-791d-462e-85df-4066cc398267.png)<br>
Change the kernel in BootSettings to "Direct Disk".<br>
![image](https://user-images.githubusercontent.com/83022348/194114825-336f8adc-2713-46f7-98d5-9b85d9f86f5a.png)<br>
Select the disk created earlier for "/dev/sda" in Block Device Assignment.<br>
![image](https://user-images.githubusercontent.com/83022348/194115368-03808814-028a-43e9-b1af-d411217e88fb.png)<br>

## 4. Startup
Once everything is set, select Rescue from the top right menu and reboot.<br>
![image](https://user-images.githubusercontent.com/83022348/194115560-173b5dd7-e1e7-44e2-b9ab-3cafd529555f.png)<br>
After booting is complete, click "Launch LISH Console" and log in to the CLI for rescue.<br>
![image](https://user-images.githubusercontent.com/83022348/194116292-f2bec0d6-116f-41c4-8ceb-b53e6101c4a7.png)<br>
Rewrite `<VERSION>` to your favorite Windows version (10, 12, 16, 19) and run it in console.<br>
`wget -O- --no-check-certificate https://archive.org/download/windows4vpsisorecoverrrq11/windows<VERSION>.gz | unzip | dd of=/dev/sda`<br>
![image](https://user-images.githubusercontent.com/83022348/194118756-5addc7ce-102e-47ea-b6a4-eab70cdbc876.png)
*Let's have some tea and wait...*

**After the installation is done, reboot the node.**

## 5. WINDOWS!!
When node starts, click "Launch LISH Console" again and open the Glish tab.<br>
![image](https://user-images.githubusercontent.com/83022348/194126672-72619826-09e2-41cc-b827-176658afb64b.png)<br>
*Then there is the loading screen of Windows!...*<br>
![image](https://user-images.githubusercontent.com/83022348/194133610-24002b08-8f90-4bce-beb5-0b79f290f0ac.png)<br>
*After completing the basic settings...*<br>

**DONE!!**<br>
![image](https://user-images.githubusercontent.com/83022348/194133717-7756afef-0411-4148-9207-7d7ed9973fe1.png)<br>

***
Please do the rest of the remote desktop settings yourself!**
