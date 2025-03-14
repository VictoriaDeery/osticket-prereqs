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

- osTicket docuentation and gather all the files

<h2>Installation Steps</h2>

<p> 
<img src="https://github.com/user-attachments/assets/e4ca9b8e-61e7-44bd-9105-1e3eed437394" height="80%" width="80%" />

</p>
<p>
1. First create a VM in Azure, then log into remote desktop (for detailed steps for this, go to my repository
  
  [Azure Compute and Networking](https://github.com/victoriadeery/azure-computing-and-networking)  
Then within the VM (osticket-vm), download the osTicket-Installation-Files.zip and move it to your desktop, and then unzip it. The folder should be called “osTicket-Installation-Files” As a test, open a browser and search 127.0.0.1 and you should see that it refused to connect. So in the next step we will enable IIS in Windows with CGI and with this installed webserver, this page will change. And we will use the files in this folder to install osTicket and some of the dependencies.

</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/e82fd2dc-abcf-4fbc-ab88-5bc7b57a559f" height="80%" width="80%" />

</p>
<p>
2. Go to the start menu, go to the control panel, where there is programs, select "uninstall a program" in the blue below it (although we will not be uninstalling a program). On the left, select "turn Windows features on or off." Select "internet information services" (IIS) and also expand it by clicking the small "+" to its left. Now to install CGI, an osTicket dependency for the webserver. Select within the IIS drop down "world wide web services" then "Application Development Features" then find CGI and select it too. Select "ok" and when it is finished click "close." Then if you refresh that webpage you will see the default web page for IIS which looks like blue squares.

</p>
<br />
<img src="https://github.com/user-attachments/assets/cebbd618-aacf-44b2-8162-ea382f8b33ec" height="80%" width="80%" />

<p>
<img src="https://github.com/user-attachments/assets/ae22fc55-04af-446b-b187-8608575467cf" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/ae22fc55-04af-446b-b187-8608575467cf" height="80%" width="80%" />

</p>
<p>
3. From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) which is a backend webserver language that osTicket runs on. So double click the folder on the desktop to open it. double click it again then double click "PHP manager" and install it saying yes and I agree. Then within the same folder, install the rewrite file and finish. Next create a directory on the c drive called php, C:\PHP by right clicking the manila folder on the bottom and opening a new file explorer, select the Windows (C:) on the left,then right click in the white space to the right to create and name a new folder "PHP". Now unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the previos windows explorer into the new “C:\PHP” folder by right clicking this php-7.3.8 file of binary language files and selecting "extract all" and browse to the C:\PHP folder to select it, and extract it into. So the PHP folder should have many files now. Now PHP files that the osTicket is going to use, is on the C drive.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/ae22fc55-04af-446b-b187-8608575467cf" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/ae22fc55-04af-446b-b187-8608575467cf" height="80%" width="80%" />

</p>
<p>
4.From the “osTicket-Installation-Files” folder, double click to install VC_redist.x86.exe. And from the “osTicket-Installation-Files” folder. Also install MySQL 5.5.62 (mysql-5.5.62-win32.msi) (database to store all info) select Typical Setup ->Finish-> Launch Configuration Wizard (after install) ->select next and select Standard Configuration -> create a username and password carefully. Select "next" and "execute" and "finish." Now the 
database is installed, but it is empty, not configured...yet. Now we will configure it in our webserver using the IIS as an admin.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/bfbb75b5-5511-4278-8209-9e8a7d75c6f7" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<img src="https://github.com/user-attachments/assets/3cbbc61e-c9da-430b-a465-c832c88a182e" height="80%" width="80%" />

<p>
5. click start, search IIS, run as admin, and a new window will pop up. Now register PHP from within IIS to make the web server aware of and locate PHP on the computer. We installed PHP manager earlier, so now double click it in this new window. select "register a new PHP version" and browse for the one saved in the PHP folder, specifically doule clicking this folder and selecting the "php-cgi" application file and "ok". Now reload IIS (Open IIS, Stop and Start the server) by clicking "osTicket-VM (osTicket-VM\username) on the top left of the IIS manager window, right click there again and select stop, right click it again and select start. Then Install osTicket from within the folder stored on the desktop by right clicking the "osTicket-v1.15.8" compressed folder and extracting all there. Then open this unipped copy of this folder and copy the "upload" folder to a new location. first open this new location by opening a new Windows explorer-> Windows (C:) -> inetpub -> wwwroot -> now select the "upload" folder and then drag and drop the upload folder into the wwwroot folder to move it here. Right click it to rename the upload folder "osTicket" then Restart the IIS server again (stop and start). 


</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/a5e9946e-f1f6-4c69-9153-172c7a4ea29e" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  

</p>
<p>
6. Now load the OS ticket site in the server. In the IIS manager in the top left near where we restarted it, click on arrow to the right of "Sites", then the arrow to the right of "Default web site," then actually select "osTicket." Now on the right of the screen, select "browse *.80 (http) and a new browser tab will open, shown in the picture above. Since some features are not yet available, indicated with a red 'x' next I'll walk you through the steps to enable all features. Go back to IIS manager and again click on the arrow to the right of "Sites", then the arrow to the right of "Default web site," then actually select "osTicket." This time now, double click on the PHP manager icon, then at the bottom of the new page click "enable to disable an extension." The grayed oout ones are disabled. Within the gray list of extensions, Enable: php_imap.dll, Enable: php_intl.dll, and Enable: php_opcache.dll by finding and right clicking on and selecting enable. Now go back to the last browser tab that popped up with the checkmarks and x's and refresh by clicking the circle with an arrow in it, between the back button and URL and all except the last two should have checkmarks.

</p>
<br />


<img src="https://github.com/user-attachments/assets/33a2b155-26cd-4154-af9c-77e2f9bd6bbb" height="80%" width="80%" />

7. now rename the ost-sampleconfig.php file within the osTicket to ost-config.php and then change the permissions to make sure osTicket has access to make changes to it in the back end. In file explorer search "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" then rightclick it to rename it to ost-sampleconfig so C:\inetpub\wwwroot\osTicket\include\ost-config.php now right click the file ->properties -> security -> advanced ->disable inheritance ->remove all inherited permissions from this host.
 Now add permissions by clicking "add" select "select a principal" then in the bottom box "enter the object name to select" and consider the user that osTicket represents and who you want to give access to it then select ok. and select the controls you want these users to have. For the sake of this non-secure demo, I wrote "everyone" and selected to give them full access selecting apply, ok, and ok.


<p>
</p>
<img src="https://github.com/user-attachments/assets/60ba9e15-c41e-4a5c-b126-a390bf0a0ad2" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/7020ddf7-77d9-49df-aded-03fe1b8a9d01" height="80%" width="80%" />

<p>
  8. go back to the browser tab that opened for you with te checkmarks and 'x's' and cllick "continue" at the bottom. name the helpdesk and give an email, fill out the admin section making this second email unique from the first. Make a new user and password. Scroll down, and now log into the database appllication that we created on the backend and then create a database specific to osTicket, and then provide the credentials here on this browser tab. Locate the osTicket-Installation-files folder on the desktop, and open it, then install Heidi SQL (an app that allows connection and configuration of the database) selecting next until you can select install, and then open it by selecting finish with "Launch Heidi sql" checked on then select skip. Now to use heidi sql to make a connection to the database and set up a database for osTicket to use. So select "+New" in the bottom left and input the username and password we made towards the beginning when we created the SQL server to create a new session. Then select "open" which opens the connection to the database so now we are connected to the session.Now to create the database, rightclick "Unnamed" select "create new" select "database" and name it "osTicket" and then "osTicket" will show on the left side below Unnamed. The installation that we are doing in the browser tab will make use of this database and put information in there.
</p>
<p>

<img src="https://github.com/user-attachments/assets/08688415-079f-450a-98f1-29f11d4518ae" height="80%" width="80%" />

<p>
  9.In the browser tab under "database settings" under "MySQL Database:" type "osTicket" which is the new database we just created inside of heidi. And enter the username and password you used when we first created the MySQL. then click "install now." You may look inside the database inside heidi by right clicking the osTicket databas on the left and selecting refresh and notice this is no longer empty. You may close Heidi. in the browser tab, below "you'll find some useful links regarding your installation." are useful URLs to log in as an admin or user:
<p>
</p>
Your osTicket URL: http://localhost/osTicket/	    Your Staff Control Panel: http://localhost/osTicket/scp
<p>
  osTicket Forums: https://forum.osticket.com/	  osTicket Documentation: https://docs.osticket.com/
</p>
<img src="https://github.com/user-attachments/assets/44fe6dff-773a-498e-87fc-c033036df9c6" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/a25d301f-4edb-4e0a-9970-bfb44ae7e98a" height="80%" width="80%" />

<p>
10. Try going to http://localhost/osTicket/scp/login.php now input the username and password created for osTicket Admin and you will see the ticketing system.
<p>
<img src="https://github.com/user-attachments/assets/03d6d399-7e77-4284-afc8-d031e06a71e4" height="80%" width="80%" />

  <p>
11. Go to http://localhost/osTicket/ to use the ticketing system as an end user.
</p>
in my next repository I will show you how to configure SLAs and departments
</p>
