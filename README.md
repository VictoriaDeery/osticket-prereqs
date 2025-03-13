<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. This includes setting up a Virtual Machie, installing the osTicket requirements, Installing osTicket, after-installation configurating of osTicket, and exploring osTicket as a Help Desk Professional by creating, interacting with, and closing tickets.<br />


<h2>Video Demonstration to Come</h2>

- ### [YouTube: How To Install osTicket with Prerequisites Coming Soon](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p> 
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/e4ca9b8e-61e7-44bd-9105-1e3eed437394"

</p>
<p>
1. First create a VM in Azure, then log into remote desktop (for detailed steps for this, go to my repository [Azure Compute and Networking](https://github.com/victoriadeery/azure-computing-and-networking). Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and move it to your desktop, and then unzip it. The folder should be called “osTicket-Installation-Files” As a test, open a browser and search 127.0.0.1 and you should see that it refused to connect. So in the next step we will enable IIS in Windows with CGI and with this installed webserver, this page will change. And we will use the files in this folder to install osTicket and some of the dependencies.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/e82fd2dc-abcf-4fbc-ab88-5bc7b57a559f>

</p>
<p>
2. Go to the start menu, go to the control panel, where there is programs, select "uninstall a program" in the blue below it (although we will not be uninstalling a program). On the left, select "turn Windows features on or off." Select "internet information services" (IIS) and also expand it by clicking the small "+" to its left. Now to install CGI, an osTicket dependency for the webserver. Select within the IIS drop down "world wide web services" then "Application Development Features" then find CGI and select it too. Select "ok" and when it is finished click "close." Then if you refresh that webpage you will see the default web page for IIS which looks like blue squares.

</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/ae22fc55-04af-446b-b187-8608575467cf" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  ![image](https://github.com/user-attachments/assets/ae22fc55-04af-446b-b187-8608575467cf)

</p>
<p>
3. From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) which is a backend webserver language that osTicket runs on. So double click the folder on the desktop to open it. double click it again then double click "PHP manager" and install it saying yes and I agree. Then within the same folder, install the rewrite file and finish. Next create a directory on the c drive called php, C:\PHP by right clicking the manila folder on the bottom and opening a new file explorer, select the Windows (C:) on the left,then right click in the white space to the right to create and name a new folder "PHP". Now unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the previos windows explorer into the new “C:\PHP” folder by right clicking this php-7.3.8 file of binary language files and selecting "extract all" and browse to the C:\PHP folder to select it, and extract it into. 
</p>
<br />
