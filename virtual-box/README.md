# VirtualBox Installation For Virtual Labs

## Introduction
Virtual Labs is a Ministry of Education initiative, Govt of India,  which aims at making the  experiments done in Engineering Colleges available in a Virtual form, to all the college students as an adjunct facility to the physical labs. These labs provide an opportunity to the students to perform these simulated experiments, read the theory and improve their understanding of the subject.

There are 1800+ Virtual Experiments bundled in 180 + labs spread across 9 domains available for  the users of Virtual Labs. Some of these labs have software dependencies such as Java, Icedtea plugin, Adobe Flash and Java3D to run the simulations. For the convenience of the users,  Virtual Labs offers a free download of a customized VirtualBox with all software dependencies  installed. 


##  Motivation and Audience
The motivation of this document is to detail  the steps to download and  run the simulated experiments of Virtual Labs  on VirtualBox. VirtualBox is a Virtualization Software. It means that you can create and run multiple Virtual Machines, running different operating systems, on the same computer at the same time. For example, you can run Windows and Linux on your Mac, or run Windows on your Linux systems. This document is for the consumption of all the users of Virtual Labs. 

## System requirement
1. Operating Systems ( OS ) - Any OS that supports Oracle VirtualBox. The machine should have [provision to support virtualization](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/virtualization_administration_guide/sect-virtualization-troubleshooting-enabling_intel_vt_and_amd_v_virtualization_hardware_extensions_in_bios) technology.

2. Memory : 4 GB RAM.

3. Processor : Any recent Intel or AMD processor.
## Downloading and Installing VirtualBox in your OS
The following subsections list the steps to download and install VirtualBoxbased on the operating system of your machine - 
  1. [Installation steps for Windows](#installation-steps-for-windows).

  2. [Installation steps for CentOS](#installation-steps-for-centos).

  3. [Installation steps for Ubuntu](#installation-steps-for-ubuntu).

  4. [Installation steps for Mac OS](#installation-steps-for-mac-os).

### Installation steps for Windows
 1. Download VirtualBox from the [link](https://www.virtualbox.org/wiki/Downloads). 

 2. Click on Windows hosts and click on ok to download the file. .exe file is downloaded.

 3. Double click on the .exe file and run the setup of VirtualBox.

 4. Click on the Run button

 <center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img1.png"> <br> </center>
 <center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img2.png"> <br> </center>

 5. Click on Next button and follow the instructions to complete the installation.

 6. After the installation, Click on Finish to complete the installation.

 7. After installation, ensure that a VirtualBox icon is created on the desktop.

 8. [Steps to import custom Ubuntu Image](#importing-virtual-labs-os-image-to-virtualbox).
### Installation steps for CentOS
1. Open Terminal (ctrl+alt+t).

2. Download RPM package with the below command:

   Wget http://download.virtualbox.org/virtualbox/5.1.6/VirtualBox-5.1-5.1.6_110634_el6-1.x86_64.rpm

3. Install VirtualBox with the below command:

   sudo rpm -i VirtualBox-5.1-5.1.6_110634_el6-1.x86_64.rpm

4. To ensure VirtualBox installation Type the below command: in the terminal:

   Virtualbox -V

5. [Steps to import custom Ubuntu Image](#importing-virtual-labs-os-image-to-virtualbox).
### Installation steps for Ubuntu
1. Open Terminal (ctrl+alt+t).

2. Type below command to download VirtualBox:

   wget http://download.virtualbox.org/virtualbox/5.2.0/virtualbox-5.2_5.2.0-118431~Ubuntu~trusty_amd64.deb

3. Install VirtualBox with the below command:

   sudo dpkg -i 

   virtualbox-5.2_5.2.0-1a18431~Ubuntu~trusty_amd64.deb

4. To ensure VirtualBox installation Type the below command: in the terminal:

   Virtualbox -V

5. [Steps to import custom Ubuntu Image](#importing-virtual-labs-os-image-to-virtualbox).
### Installation steps for Mac OS
1. Download VirtualBox from the [link](https://www.virtualbox.org/wiki/Downloads) and click on OS X hosts and save the file.

2. Double click on downloaded file .dmg.

3. Follow the instructions and install it.

4. [Steps to import custom Ubuntu Image](#importing-virtual-labs-os-image-to-virtualbox).

## Importing Virtual Labs OS Image to VirtualBox
Steps to import Ubuntu ( .ova file )in VirtualBox :

**Note :** The import steps need to be done only once.

1. Click on the [link](https://drive.google.com/file/d/1sFWId8LPAUK0YTkTEizLQ-cJF1jYShuf/view) to download the Ubuntu OS image file and save the **ubuntu-14.04-college-cloud.ova** in your machine.

2. Click on the **VirtualBox** Icon to open.

3. Click on **File** on the top left corner of the screen and select **Import Appliances**.

4. **Application to import** window will pop up.

<center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img3.png"> <br> </center>
<center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img4.png"> <br> </center>

5. Browse the downloaded file by clicking on the **browse** button.

6. Click on the selected file and click on **Open**.

<center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img5.png"> <br> </center>
<center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img6.png"> <br> </center>

7. Click on import to start the import setup.

8. Click on next to start importing the downloaded file.

<center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img7.png"> <br> </center>

9. The importing process looks as below:

<center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img8.png"> <br> </center>

10. This may take 5 to 10 minutes to complete the import process.

11. After the completion of importing, you can find the ubuntu-virtualbox in the   VirtualBox window on the left side menu.

12. Double click on the Ubuntu-14.04-college-cloud.

13. You can find the Ubuntu OS, it prompts to enter a password.

14. Password for the OS is “cc”.

**NOTE:**
Select the **ubuntu-14.04-college-cloud** from the VirtualBox window and allocate the Processor and Memory/RAM size from the Settings menu appropriately based on the system configuration of the user machine.

## Recommended Settings for the Imported VirtualBox
* Processor --> Single.

* Memory/RAM size --> 2GB or 4GB according to your RAM Size.

<center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img9.png"> <br> </center>

* Please change the network setting in your Virtualization software for the imported image from **Bridge adapter** to **Nat**.

<center><img src="https://raw.githubusercontent.com/virtual-labs/ph3-exp-dev-process/main/virtual-box/images/img10.png"> <br> </center>

* **Do not update or upgrade any application in it.**

## Running Virtual Labs Simulation in VirtualBox

1. Open Virtualbox.

2. Click on Ubuntu-14.04-college-cloud from the left menu bar.

3. Enter password *cc*.

4. Open Firefox (web browser) and type [http://vlab.co.in/](https://www.vlab.co.in/). 

5. Scroll the page down to Participating Institutes and click on IIITH logo or click on the [link](https://www.vlab.co.in/participating-institute-iiit-hyderabad).

6. Choose any lab that you would  like to perform.

7. Introduction page is loaded. Now click on List of Experiments.

8. Click on any of the Experiment.

9. Select any Experiment and click on Simulation/Experiment in the side menu bar to perform the experiment.

10. Once you are done performing the experiment you can test your learnings in the Quizzes section.

11. Following the above steps, you can explore any number of labs and experiments of Virtual Labs.
 
## Conclusion 
This document has captured the steps for the download, installation and use of Virtual Box (with all software dependencies installed ) to facilitate easy use of Virtual Labs. Any queries regarding the use of this document can be addressed to support@vlabs.ac.in. 






