# Install-Ubuntu-22.04-LTS-on-MacBook-
To install Ubuntu 22.04 LTS (long-term support) on Apple Silicon MacBooks.

Apple Silicon chips are M1, M2…. M5.

Follow the below steps for installation process

#### Step 1:
Install UTM (UTM employs Apple's Hypervisor virtualization framework to run ARM64 operating systems on Apple Silicon)
```
https://mac.getutm.app/
```
#### Step 2:
Download the ISO of Ubuntu Server 22.04 LTS (long-term support) ARM64 
```
https://cdimage.ubuntu.com/releases/22.04/release/ubuntu-22.04.5-live-server-arm64.iso
```
**Note:** Apple uses ARM architecture and hence, you will need to download ARM64 Ubuntu server. Also note, ARM64 doesn’t desktop version. So, you will first have to download the server and once it is installed, you will have install Ubuntu Desktop from the terminal (which you will see the below steps)

#### Step 3:
Open UTM and Click + icon <br>
<img width="246" height="169" alt="image" src="https://github.com/user-attachments/assets/bd49a01e-a8df-45ab-a8df-216d9cb29bd2" /><br>

#### Step 4:
Select Virtualize<br>
<img width="218" height="250" alt="image" src="https://github.com/user-attachments/assets/cf906245-35c8-4fa2-86a8-169f8ba99266" /><br>

#### Step 5:
Select Linux under Operation System<br>
<img width="218" height="252" alt="image" src="https://github.com/user-attachments/assets/ca316c95-66f9-46cf-86a7-46c01426e52c" /><br>

#### Step 6: 
Configure the required hardware for Ubuntu OS. Enable the option – _Enable Display output_ and click Continue<br>
<img width="216" height="249" alt="image" src="https://github.com/user-attachments/assets/40a1b023-30e5-45f7-8444-c813e4d188d9" /><br>

#### Step 7:
Enable the options - _Use Apple Virtualization_ and _Boot from ISO Image_ and click Continue<br>
<img width="217" height="282" alt="image" src="https://github.com/user-attachments/assets/c12e4766-1ea0-41e3-a4b7-e916370ffa68" /><br>

#### Step 8:
Speficy the storage for Ubuntu OS<br>
<img width="217" height="250" alt="image" src="https://github.com/user-attachments/assets/f9aa6b1a-5d17-4f81-a3c9-a5690ed8f88a" /><br>

#### Step 9:
In case you need Shared Directory between Mac and Ubuntu OS, select a specific directly here<br>
<img width="217" height="249" alt="image" src="https://github.com/user-attachments/assets/a97d9de8-0373-4291-97a8-16842f20ed4d" /><br>

#### Step 10:
You will the complete summary of the settings and click on Save<br>
<img width="215" height="330" alt="image" src="https://github.com/user-attachments/assets/12730e30-14ea-4b11-9dd7-9bacdd7146b5" /><br>

#### Step 11: 
You will see the image and click on Play button<br>
<img width="355" height="254" alt="image" src="https://github.com/user-attachments/assets/f5a91a3c-01c7-4b16-b30c-88631f3d35fa" /><br>

#### Step 12:
You will see terminal from here. Follow the steps below to install Ubuntu server and later Ubuntu Desktop version
- Select Try or Install Ubuntu Server
- And after sometime, select your preferred language (use tab key from your keyboard to navigate)
- When asked for type of installation – choose Ubuntu Server (using space key)
- Keep next 2 pages as default and proceed
- Ubuntu will perform the mirror location test wait until you see test passed and continue
- Leave the next page (storage configuration) as it is and continue
- Now, you will see the summary of the hard drive, click on continue
- Enter your name, server name, password (remember the password) and continue
- Skip the next page and continue (for Ubuntu Pro)
- Ignore the SSH setup and continue (you can install it later)
- Now the installation process will begin and it will ask for a reboot after the installation
- After reboot, it will ask for username and password, give your credentials. <br>
 ** Note:** Since we installed server edition, we will see the terminal only
- Run the below commands to install Desktop version one after other
```
sudo apt update && apt upgrade -y
sudo apt install tasksel
sudo apt install ubuntu-desktop
```
Note: Ubuntu Desktop will take at least 45 mins or more to install. Once the installation is completed, reboot the machine
```
sudo reboot now
```
- Once it is rebooted, you will see the Graphical User Interface and login with your password.
- Your installation is complete

> [!NOTE]  
> To install Kubernetes on Ubuntu 22.04 LTS, refer the repository: https://github.com/vikramhemchandar/Kubernetes-and-Docker-Installation
