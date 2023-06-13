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

- Install / Enable Internet Information Services (IIS) in Windows
- Install PHP Manager for IIS
- Install C++ redistributable
- Install MySQL and set up the username and password
- Configure Permissions and Install os-Ticket

<h2>Installation Steps</h2>

<h3>Step 1: Install / Enable IIS in Windows</h3>
<p>
<br> 
<img src="https://i.imgur.com/JWqloc3.png)" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Access the "Control Panel", "Programs", then "Programs and Features". Then select "Turn Windows features on or off" on the left. On the pop up window, select the box for "Internet Information Services."
</p>
<br />

<h3>Step 2: Install PHP Manager for IIS</h3>
<p>
<img src="https://i.imgur.com/wHPt2N9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install PHP Manager for IIS  (obtain link from Google) and open the file. This allows you to run PHP on IIS
</p>
<br />

<h3>Step 3: Install C++ redistributable</h3>
<p>
<br>  
<img src="https://i.imgur.com/waMtTT6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Step 4: Install MySQL and set up the username and password</h3>
<p>
<br> 
<img src="https://i.imgur.com/Yk27n7b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
MySQL is the database where osTicket will store the application data, such as users and tickets.
</p>
<br />

<h3>Step 5: Configure Permissions and Install os-Ticket
</h3>
<br>

<p>
<img src="https://i.imgur.com/QYIdzRy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Download osTicket (osTicket.com) and open the file. Open IIS (run as an administrator. Click PHP Manager, under "PHP setup," click register New PHP version, create a PHP folder in the  C:drive, select "php-cgi.exe," and click OK. 
</p>
<br>

<h3>Step 6: Rename ost-config.php
</h3>
<br>

<p>
<img src="https://i.imgur.com/UwaADR3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p> 

<p>
  Extract the ost-config.php folder. It will bring up an "upload folder." Copy and paste "upload folder" to "wwwroot" folder within the "inetpub" folder. 
  Rename the "upload" folder to "osTicket."
</p>
<br>
 
 <h3>Step 7: Enable Extensions in IIS
 </h3>
 <br>
 <p>
 <img src="https://i.imgur.com/s2N6Om8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
 </p> 

<p>
 Open IIS, refresh the page, "osTicket" will appear under "sites." Click on "osTicket, then click, "Browse 80(http).  "Localhost/osTicket/setup/" will load on the webpage. You will notice that some of the extensions on the page will be disabled. To enable them, open PHP Manager in IIS, click, "enable or disable an extensions," enable, "imap," "intl," and "opcache." Refresh the osTicket page and click "continue."
</p>

<h3>Step 8: Configure Permissions 
</h3>
<br>

<p>
<img src="https://i.imgur.com/QYIdzRy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
 Create the "ost-config.php" file. Go back to wwwrootfolder, go to osTicket, click include, go to "ost-config," right click it and click  properties, then click "security,"click "users," click "edit," to change permission, click "users" again, then under "Permission for Users," click "Full Control," then click apply, then click ok. This will allow you to have full Access to osTicket. Go back to osTicket and click Continue. You should now see osTicket Basic Installation. Fill out the information for your help desk and admin user. 
</p>  
 
<p>
 When you get to the Database settings page, you must create a database. Download "Heidisql" (from heidisql.com), click "installer 32/64 bit combined." Once it installs, your VM may restart. Open Heidisql, click "New." The username and password will be the same as for MySQL. This will open a connection to the database. Right click and hit "create new," and select "database," name it osTicket.
</p>

<p>
 Go back to osTicket and fill in the database information. MySQL will be "osticket," username will be "root," password will be the same password you entered previously for MySQL. Click Install and osTickt should now be installed successfully.
</p> 
<br />
