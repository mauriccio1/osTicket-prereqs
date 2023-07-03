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

- PHP Manager for IIS 
-  Rewrite Module 
-  PHP 7.3.8
- VC_redist.x86.exe.
- MySQL 5.5.62
- osTicket v1.15.8
- HeidiSQL



<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/fSjSQno.png" alt="Install / Enable IIS"/>
</p>
<p>
Install / Enable IIS in Windows with CGI and common HTTP features and IIS Management Console. This can be found after going to the control panel in windows and selecting programs. Then select "turn windows features on or off".


</p>
<br />

<P>
<img src="https://i.imgur.com/Q9gvV0C.png" alt="create PHP directory"/>

<p>
Create the directory C:\PHP and extract PHP 7.3.8 into it

</p>

<br/>

<p>
<img src="https://i.imgur.com/YCDGNKb.png" height="80%" width="80%" alt="osTIcket Prerequisites"/>
</p>
<p>
Download the other prerequisite applications in order to run osTicket 
 - PHP Manager for IIS 
-  Rewrite Module 
- VC_redist.x86.exe.
- MySQL 5.5.62
- osTicket v1.15.8
- HeidiSQL
</p>
<br />

<p>
<img src="https://i.imgur.com/U27xXmo.png" height="80%" width="80%" alt="regiser PHP"/>
</p>
<p>
Open IIS as an Admin and Register PHP from within IIS. Then Reload IIS or (Open IIS, Stop and Start the server). After registering PHP make sure to Click “Enable or disable an extension”.
<ul> 
  <li>Enable: php_imap.dll</li>
 <li>Enable: php_intl.dll</li>
   <li>Enable: php_opcache.dll</li>
</ul>
  Refresh the osTicket site in your browseand observe the changes.

</p>
<br />
<p>
  <img src="https://i.imgur.com/e2D6MRl.png" height="80%" width="80%" alt="renaming ost file"/>
</p>
<p>
  Rename: ost-sampleconfig.php 
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
right click on ost-config.php and select properties -> security 
Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

</p>
<br/>

<p> <img src="https://i.imgur.com/A9tadBu.png" height="80%" width="80%" alt="set up heidi SQL"  </p>
 <p>
Open Heidi SQL which was installed earlier and create a new session. After making a password Connect to the session.
then Create a database called “osTicket”.
</P>
