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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
