<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/7t7CynK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open the Start menu.
Type features and select Turn Windows features on or off.
Tick the Internet Information Services checkbox and hit OK.
Wait for the installation to complete and hit Close
</p>
<br />

<p>
<img src="https://i.imgur.com/ymKh4vE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Web Platform Installer (download from within lab files: <a href="https://drive.google.com/file/d/1nJbiPfZSC3PNpP3r7jvoujaxRj_nCYup/view?usp=sharing"> link)

Open after installation
Add MySQL 5.5 (it will ask for credentials to be created later)
Name: root
Password: Password1
Add All simple versions of x86 PHP up until 7.3
Fix any failures if required ( <a href="https://drive.google.com/file/d/1eiO0nqSzieyhhBmIGxy-x2iToHGNLb7s/view?usp=sharing"> link)

Install PHP Version 7.3.8 (or any other version if necessary, <a href="https://windows.php.net/downloads/releases/archives/"> archives)

Install PHP Manager 1.5.0 for IIS 10 (folder you unzipped on the desktop)

Install Microsoft Visual C++ 2009 Redistributable Package

</p>
<br />

<p>
<img src="https://i.imgur.com/GapucqI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download osTicket (<a href="https://drive.google.com/file/d/16x7qQVFZ_edrrG53J3mvugDdtDLgwZjI/view?usp=sharing"> link )

Extract and copy the “upload” folder INTO c:\inetpub\wwwroot

Within c:\inetpub\wwwroot
Rename “upload” to “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/DMNyAxM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Reload IIS (Open IIS, Stop and Start the server)

  Go to sites -> Default -> osTicket

  On the right, click “Browse *:80”
  
</p>
<br />

<p>
<img src="https://i.imgur.com/ZCH9AIT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable Extensions in IIS: Note that some extensions are not enabled
  
Go back to IIS, sites -> Default -> osTicket

Double-click PHP Manager

Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
  
</p>
<br />

<p>
<img src="https://i.imgur.com/CnqDhMP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Refresh the osTicket site in your browser
  
Observe the changes

Rename: From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
  
</p>
<br />

<p>
<img src="https://i.imgur.com/ERQfN62.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
