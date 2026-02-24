<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- osTicket Installation
- VC_redist.x86.exe.
- MySQL 5.5.62
- PHP Manager
- Rewrite Module 

<h2>Installation Steps</h2>

<p>
<img width="623" height="462" alt="Screenshot 2026-02-24 at 5 29 34 PM" src="https://github.com/user-attachments/assets/95a77de6-5bf4-4d75-9ff0-b2dfd4ecefc2" />


</p>
<p>
Once you download the osTicket installation files, extract them to the desktop
<br />

<p>
<img width="416" height="371" alt="Screenshot 2026-02-24 at 5 35 40 PM" src="https://github.com/user-attachments/assets/cd8771be-8463-403b-a810-124a2294dfda" />

</p>
<p>
Next, install/enable IIS in Windows WITH CGI. On a Windows computer, open the Control Panel, go to Programs → Programs and Features, then click Turn Windows features on or off. In the Windows Features window, expand Internet Information Services (IIS), then expand World Wide Web Services, followed by Application Development Features. Check the box for CGI, click OK, and let Windows install the required components. Once it finishes, IIS will be enabled with CGI support, allowing web applications and scripts to run through the IIS web server.
</p>
<br />

<p>
<img width="500" height="411" alt="Screenshot 2026-02-24 at 5 38 23 PM" src="https://github.com/user-attachments/assets/77b4aebd-fae6-463d-9615-537b723afb56" />

</p>
<p>
Next, install PHP manager located in the osTicket installation files folder. 
</p>
<br />

<p>
  <img width="500" height="411" alt="Screenshot 2026-02-24 at 5 38 23 PM" src="https://github.com/user-attachments/assets/60578639-818f-4b38-bbb3-ae5d2bc8559e" />

</p>
<p>
Next, install the Rewrite Module located in the osTicket installation files folder.
</p>
<br />

<p>
  
</p>
<p>
  From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

</p>
