<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"  alt="osTicket logo"/>
</p>

<h1>Installation of osTicket and prerequisites</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.
All of the following steps were done on a  VM (Virtual Machine) created using the Microsoft Azure cloud services.
The VM was set up and connected to using Microsoft remote Desktop beforehand. The VM is running the Windows 10 operating system.


<br/>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Microsoft Remote Desktop
- Internet Information Services (IIS)
- osTicket (Open Source Ticketing System)

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
<img src="https://i.imgur.com/fSjSQno.png" height="80%" width="80%" alt="Install / Enable IIS"/>
</p>
<p>
 <h2>Install / Enable IIS </h2>
Install / Enable IIS in Windows with CGI and common HTTP features and IIS Management Console. <br> 
 This can be found after going to the control panel in windows and selecting programs -> Then select "turn windows features on or off".


</p>
<br />

<P>
<img src="https://i.imgur.com/Q9gvV0C.png" height="80%" width="80%" alt="create PHP directory"/>

<p> 
 <h2>Create Directory C:\PHP</h2>
Go to "This PC" in File Explorer and Create the directory C:\PHP and extract PHP 7.3.8 into it.

</p>

<br/>

<p>
<img src="https://i.imgur.com/YCDGNKb.png" height="80%" width="80%" alt="osTIcket Prerequisites"/>
</p>
<p>
 <h2>osTicket Prerequisites</h2>
Download rest of prerequisite applications in order to run osTicket 
<ul> 
 <li>PHP Manager for IIS </li>
 <li>Rewrite Module </li>
<li>VC_redist.x86.exe.</li>
<li>MySQL 5.5.62</li>
<li>osTicket v1.15.8 </li> 
<li>HeidiSQL </li>
 </ul>
</p>
<br />

<p>
<img src="https://i.imgur.com/U27xXmo.png" height="80%" width="80%" alt="regiser PHP"/>
</p>
<p>
 <h2>Register PHP and Enable Extensions</h2>
Open IIS as an Admin and Register PHP from within IIS. Then Reload IIS or (Open IIS, Stop and Start the server). After registering PHP make sure to Click “Enable or disable an extension”.
<ul> 
  <li>Enable: php_imap.dll</li>
 <li>Enable: php_intl.dll</li>
   <li>Enable: php_opcache.dll</li>
</ul>
 Finally refresh the osTicket site in your browser.

</p>
<br />
<p>
  <ol> 
  <li><img src="https://i.imgur.com/e2D6MRl.png" height="80%" width="80%" alt="renaming ost file"/>  </li> 
<li> <img src="https://i.imgur.com/vhE3Jpm.png" height="80%" width="80%" alt="ost-config permission"/> </li>
   </ol>
</p>
<p>
 <h2>Rename: ost-sampleconfig.php </h2> 
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php <br>
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php <br>
right click on ost-config.php and select properties then the tab named "security" <br>
Assign Permissions: ost-config.php <br>
Disable inheritance and select Remove All <br>
Add new permissions "Everyone", then select All

</p>
<br/>

<p> <img src="https://i.imgur.com/A9tadBu.png" height="80%" width="80%" alt="set up heidi SQL"> </p>
 <p>
  <h2> Creating a New Session In HeidiSQL</h2>
Open Heidi SQL which was installed earlier and create a new session. After making a password Connect to the session.
Then Create a database called “osTicket”; which will be the database that is entered later.
</P>
<br/>
 <p> <img src="https://i.imgur.com/HPqn4fv.png" height="80%" width="80%" alt="osTicket setup"> </P>

   <p>
    <h2> Finish Setting up osTicket In Browser</h2>
   Fill in all the required fields (helpdesk name, admin username and password, etc.)
    The last step should be connecting to the SQL database that was just created.
    The following are what I used to fill in these fields.

<ul>
<li style="list-style-type:square"> MySQL Database: osTicket  </li>
<li style="list-style-type:square">  MySQL Username: root </li> 
<li style="list-style-type:square"> MySQL Password: Password1 </li>
<li style="list-style-type:square"> Finish by clicking “Install Now" </li>
</ul>
</p> 
<br/>
<p>
 
</p>
<br/>

<p> <img src="https://i.imgur.com/u2PMI5J.png" height="80%" width="80%" alt="osTicket Login"/> </p>
<p> 

<h2>osTicket Installed</h2></p>
<p>
 Now using the URL http://localhost/osTicket/scp/login.php you should be taken to login screen osTicket.
Hopefully if everything was done correctly osTicket should now be installed and ready to start creating tickets.
</p>


