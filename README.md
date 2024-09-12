<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable IIS with CGI
- Install PHP Manager
- Install Rewrite Module 
- Install VC_redist
-  Install MySQL/ set up username & password
-  Install osTicket
-  HeidiSQL

<h2>Installation Steps</h2>


<p>

<h2>Enable IIS with CGI</h2>


![Screenshot 2024-09-10 220133](https://github.com/user-attachments/assets/1f3e1ef2-2c05-4c39-908d-1f6da9bf57d0)


</p>
<p>
Once your VM is created you will log onto the remote desktop using the public IP address of the VM and also the creditials you created. Once you get connected you will enable IIS with CGI. To do this you will click the start menu and type in control panel and open it, next you will select "programs" and then select "turn windows features on or off". Once you are here you will expand and navigate to Internet Information Services, then you will expand and navigate to Application Development Features and select CGI and press ok to apply changes. 
</p>
<br />

<p>
 
<h2>Install PHP Manager for IIS</h2>

![image](https://github.com/user-attachments/assets/f4d8732b-44bc-43d2-918d-939f86ede54a) 

</p>
<p>
From the “osTicket-Installation-Files” folder, install PHP Manager for IIS. You will do this by navigating to the (PHPManagerForIIS_V1.5.0.msi) file in the folder and double clicking the file.
</p>
<br />

<p>

<h2>Install the Rewrite Module</h2>

![image](https://github.com/user-attachments/assets/0f57bd4e-4309-4dc6-a793-a8a7d04ea9b0)

</p>
<p>
From the “osTicket-Installation-Files” folder install the Rewrite Module
</p>
<br />

<p>

<h2>Create the directory C:\PHP.</h2>

![image](https://github.com/user-attachments/assets/3913231e-d203-4774-8466-9f8b1dc60040)

</p>
<p>
Create the directory C:\PHP.
You will do this by opening a new file explorer, navigating to "This PC" selecting the windows C drive and then right clicking and navigating to "new" and select folder and name the folder "PHP" 
</p>
<br />

<p>

<h2>unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder</h2>

![image](https://github.com/user-attachments/assets/3a125d88-3289-4311-875c-eb529f62ccca)

</p>
<p>
From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
You will do this by navigating to the to the osTicket-Installation-Files and right clicking the php-7.3.8-nts-Win32-VC15-x86.zip file and selcting "Extract All". from there you will select browse and navigate to the “C:\PHP” folder and select it and extract.
</p>
<br />

<p>

<h2>Install VC_redist.x86.exe.</h2>

![image](https://github.com/user-attachments/assets/d91d441a-f9d5-414b-befa-bd482b68d2bc)

</p>
<p>
From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
You will do this by nagigating to the osTicket installation files folder and double clicking the file.
</p>
<br />

<p>

<h2>Install MySQL</h2>

![image](https://github.com/user-attachments/assets/3a04d86c-a592-4635-9646-97b354100822)

</p>
<p>
From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
After doublicking the file to install here is what you will need to select 
Typical Setup -
  
![image](https://github.com/user-attachments/assets/f1f1678e-c989-403f-91ad-d568decd8cbb)

Launch Configuration Wizard (after install) ->
![image](https://github.com/user-attachments/assets/b32c6977-f901-4b71-9c63-b1fa5a92560a)

Standard Configuration ->
![image](https://github.com/user-attachments/assets/558efa58-6370-42e4-b6bf-4ba699b04a7a)


Username: root
Password: root
![image](https://github.com/user-attachments/assets/c18a8b65-d8ee-4800-a774-3a67f0d37f56)


</p>
<br />

<h2>Open IIS as an Admin</h2>

<p>

  ![image](https://github.com/user-attachments/assets/9f1faa45-4861-45c6-a5a9-bd85f3267137)

</p>
<p>
You will do this by selecting the start menu and typing "IIS" and then right clicking the application and select "Run as administrator"
</p>
<br />

<h2>Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)</h2>

<p>

</p>
<p>
You will do this by
Selecting "php manager" in IIS
  
  ![image](https://github.com/user-attachments/assets/658bae9d-7f66-4201-ba2d-330bdb8b022c)
  
Then selecting "Register new PHP version" 
  ![image](https://github.com/user-attachments/assets/064da2d9-1a4d-430a-918f-6347e063cc7d)

Then you browse to C:\PHP\php-cgi.exe and select open and press ok.

![image](https://github.com/user-attachments/assets/2b0eae3b-53d6-480b-bb30-33aa15f45e5b)

You will then go back to the "VM-osticket" connection in IIS (top left corner) and restart the server by selecting restart in the top right corner  

![image](https://github.com/user-attachments/assets/5fbe05da-ffce-45fe-bc8b-40dcdb1cc4ed)

![image](https://github.com/user-attachments/assets/33caab60-adfb-46a3-9e1c-2b1b696e2888)



</p>
<br />

<h2>Install osTicket</h2>

<p>

</p>
<p>
You will do this by navigating back to the installation files folder and right clicking the file " osTicket v1.15.8" and selecting "Extract all", select extract and wait for the files to copy/extract into the selcted folder

  ![image](https://github.com/user-attachments/assets/4dcdb991-a453-4720-a740-3776b0e90032)

From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”

![image](https://github.com/user-attachments/assets/b828e666-d86a-4f56-9427-47cdd22c34e6)
![image](https://github.com/user-attachments/assets/b0ccde50-5800-433d-897e-6b15e20ae180)
![image](https://github.com/user-attachments/assets/335ff659-9e0a-494b-8d07-0c01264d7f52)


![image](https://github.com/user-attachments/assets/4eb17c5a-148b-4c18-9f8e-97a553b24488)
![image](https://github.com/user-attachments/assets/06c6d1ea-fe82-48b4-9c8e-c21293f88a8c)


</p>
<br />

<h2>Reload IIS (Open IIS, Restart the server)</h2>
<p>

![image](https://github.com/user-attachments/assets/5ed67ddb-f39c-4b0b-b915-a324f109d9ed)

</p>
<p>
After you restart the serever you will need to 
Go to sites -> Default -> osTicket

![image](https://github.com/user-attachments/assets/a875970d-e0f8-40aa-8b21-442c2f77df04)

  On the right, click “Browse *:80”

![image](https://github.com/user-attachments/assets/12b0526f-f378-47cb-8b97-10bcf0f69be6)

This will open up the osTicket Installer 

![image](https://github.com/user-attachments/assets/3f6dac9d-d700-41b2-b8c4-b32a4d4acdc6)

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket

![image](https://github.com/user-attachments/assets/a875970d-e0f8-40aa-8b21-442c2f77df04)
Double-click PHP Manager

![image](https://github.com/user-attachments/assets/4499c774-b015-4c96-8c81-779721611cf7)

Click “Enable or disable an extension”

![image](https://github.com/user-attachments/assets/ad3ec503-7492-4378-8912-098e0a012f06)

Enable: php_imap.dll

![image](https://github.com/user-attachments/assets/93438311-e590-4861-9bbc-ad74c8911a71)

Enable: php_intl.dll

![image](https://github.com/user-attachments/assets/935742d6-cff5-430e-9f10-198b8a1cee55)

Enable: php_opcache.dll

![image](https://github.com/user-attachments/assets/29ec08c9-ca3c-40bb-864a-62fbc9213ce3)

Refresh the osTicket site in your browser, observe the changes

![image](https://github.com/user-attachments/assets/a64fbd6b-c689-4c4d-b3e9-382cca7daf9f)
![image](https://github.com/user-attachments/assets/3cc92dce-01be-4a8d-b1f3-75a8e1a06032)


</p>
<br />

<h2>Rename: ost-config.php</h2>

<p>

</p>
<p>
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

![image](https://github.com/user-attachments/assets/f6fe2459-1521-4037-994d-c54a65351706)

To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

![image](https://github.com/user-attachments/assets/c64e1ddd-bcaa-4e08-ba28-9313c21e62b8)



</p>
<br />

<h2>Assign Permissions: ost-config.php</h2>
<p>

</p>
<p>
Disable inheritance -> Remove All

You will do this by right clicking ost-config.php and selecting properties, then security, advanced, and then "disable inheritance" 
Then you will select 
  
  ![image](https://github.com/user-attachments/assets/067ad2c2-383b-4420-a756-8a572dfb5d3c)

  
New Permissions -> Everyone -> All

Now to select new permissions you need to select 

Add, Select a principal, then type "everyone" and click check names, press ok
now select: Full Control and press ok, apply, and the ok
![image](https://github.com/user-attachments/assets/fa330658-c4a1-4f0e-9f52-46717373bb7f)


</p>
<br />
<h2>Continue Setting up osTicket in the browser (click Continue)</h2>
<p>

![image](https://github.com/user-attachments/assets/a845016a-1ebd-437b-a414-33f3c257306a)

</p>
<p>
Name Helpdesk
Default email (receives email from customers)

</p>
<br />

![image](https://github.com/user-attachments/assets/5d65e1a0-3e6c-4251-816c-7e40117254a1)


<h2>Install HeidiSQLp</h2>
<p>

![image](https://github.com/user-attachments/assets/3b4e9f78-b1e4-47fe-8289-536bd75a7d27)

</p>
<p>
Open Heidi SQL

Create a new session, root/root

![image](https://github.com/user-attachments/assets/81a6eab8-2af1-407c-9f11-87ea89be121f)

Connect to the session

![image](https://github.com/user-attachments/assets/a68c7d06-1e03-4fa1-932e-becd7df9e7ae)

Create a database called “osTicket”

![image](https://github.com/user-attachments/assets/3ce7457b-d3b9-4443-a5c7-44a0b67a9513)

![image](https://github.com/user-attachments/assets/61ed7a35-0bb0-4014-8777-f49e39069782)

</p>
<br />

<h2>Continue Setting up osTicket in the browser</h2>
<p>

</p>
<p>
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”

![image](https://github.com/user-attachments/assets/a137f206-d917-4e97-9f31-1acb290ac0f5)

</p>
<br />

<h2>Congratulations, hopefully it is installed with no errors!</h2>
<p>

![image](https://github.com/user-attachments/assets/05d686fc-7351-419a-9819-b79da968e792)

</p>
<p>


