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
 <img width="496" height="386" alt="Screenshot 2026-02-24 at 5 39 21 PM" src="https://github.com/user-attachments/assets/2d44775e-c2c8-4cfa-9030-259325fb787a" />

</p>
<p>
Next, install the Rewrite Module located in the osTicket installation files folder.
</p>
<br />

<p>
 <img width="599" height="461" alt="Screenshot 2026-02-24 at 5 41 35 PM" src="https://github.com/user-attachments/assets/d373e030-591c-4f5f-afee-c5dc42c65f41" />
 
</p>
<p>
 Navigate to the C: Drive and create a new folder and name it "PHP". Then, from the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

<p>
  <img width="474" height="292" alt="Screenshot 2026-02-24 at 5 44 37 PM" src="https://github.com/user-attachments/assets/33467d41-146b-423c-943f-cd0325d7da5b" />

</p>
<p>
  From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
</p>

<p>
  <img width="488" height="378" alt="Screenshot 2026-02-24 at 5 44 58 PM" src="https://github.com/user-attachments/assets/8b708adb-2731-4acb-a697-8c6abc75f928" />

</p>
<p>
  From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi). During installation select, "Typical Setup" and then after the install, launch "Configuration Wizard" and select "Standard Configuration".
</p>

<p>
  <img width="518" height="314" alt="Screenshot 2026-02-24 at 5 49 38 PM" src="https://github.com/user-attachments/assets/26a479c4-5d95-4e47-82f3-bfc20f1de555" />

</p>
<p>
  Next, open IIS as an administrator and register PHP from within (PHP Manager -> C:\PHP\php-cgi.exe). After reload IIS by right clicking the server and selecting stop, waiting a moment, then selecting start.
</p>

<p>
<img width="778" height="557" alt="Screenshot 2026-02-24 at 5 55 19 PM" src="https://github.com/user-attachments/assets/4af23f9b-2666-4e37-a6a2-874a5689d11a" />


</p>
<p>
  Next, intall os Ticket v1.15.8 from the osTicket Installation files folder,Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
</p>


<p>
<img width="823" height="740" alt="Screenshot 2026-02-24 at 5 56 59 PM" src="https://github.com/user-attachments/assets/ab42a25a-4d2f-471f-87d6-fa2ec37bc29e" />

<p>
<img width="275" height="502" alt="Screenshot 2026-02-24 at 8 31 07 PM" src="https://github.com/user-attachments/assets/9ce04260-1e21-441a-b54a-154a4d0b30e2" />


</p>
<p>
At this stage, note that some required PHP extensions may not yet be enabled. Return to IIS, navigate to Sites → Default Web Site → osTicket, and then double-click PHP Manager. From there, select “Enable or disable an extension” and enable the following extensions: php_imap.dll, php_intl.dll, and php_opcache.dll. Once these extensions are enabled, refresh the osTicket site in your web browser and observe the changes to confirm that the updates have taken effect.
</p>

<p>
<img width="535" height="24" alt="Screenshot 2026-02-24 at 6 08 26 PM" src="https://github.com/user-attachments/assets/dfb7c13b-306d-4b40-99b3-801c6f886413" />


</p>
<p>
 Next, navigate to C:\inetpub\wwwroot\osTicket\include\ and locate the file named ost-sampleconfig.php. Rename this file to ost-config.php, ensuring the filename matches exactly. This step creates the required configuration file that osTicket uses to store system settings during the installation process. Continue the installion process from the browser.
</p>

<p>
 <img width="759" height="511" alt="Screenshot 2026-02-24 at 6 08 58 PM" src="https://github.com/user-attachments/assets/97e566dd-7753-49dd-b7d9-530038d88efe" />

</p>
<p>
 From the osTicket-Installation-Files folder, install HeidiSQL and then launch the application. Once open, create a new session using the username root and password root, and connect to the session. After successfully connecting, create a new database named osTicket, which will be used during the osTicket installation process to store ticket data and system information.
</p>

<p>
 <img width="822" height="641" alt="Screenshot 2026-02-24 at 6 16 23 PM" src="https://github.com/user-attachments/assets/fd47d2fa-a080-4d4f-9744-a023d1baa851" />

</p>
