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

<ul>
  <li>Azure Account: Ensure you have an active Azure account.</li>
  <li>Azure Virtual Machine: Create a Windows 10 Virtual Machine on Azure if you haven't already.</li>
  <li>Remote Desktop: Make sure you can access your VM using Remote Desktop.</li>
  <li>Access to the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank" >Installation Files</a> on Google Drive</li>
</ul>

<h2>Installation Steps</h2>

<h3>Step 1: Connect to Your VM</h3>
  <ol>
    <li>Use Remote Desktop to connect to your Azure Windows 10 VM.</li>
  </ol>

<h3>Step 2: Enable IIS</h3>
  <ol>
    <li>In the Start menu, type "Turn Windows features on or off" and press Enter. This will open the "Windows Features" dialog.</li>
    <li>In the "Windows Features" dialog, scroll down or look for "Internet Information Services." </li>
    <li>Add the IIS Management Console by following this path: Internet Information Services -> Web Management Tools -> IIS Management Console [X] IIS Management Console</li>
    <li>Add required features: CGI and Common HTTP Features.</li>
    <br />
<p>
<img src="https://i.imgur.com/1Xx2vhl.png" height="80%" width="80%" alt="CGI path and seletion"/>
</p>
<p>
   <br />
<p>
<img src="https://i.imgur.com/TDyu27P.png" height="80%" width="80%" alt="Common HTTP Features"/>
</p>
<p>
  <li>Open a webrowser and visit http://127.0.0.1/. If the installation was successful you will see a site like the one below.</li>
     <br />
<p>
<img src="https://i.imgur.com/vV12vmo.png" height="80%" width="80%" alt="Common HTTP Features"/>
</p>
<p>
  </ol>


<h3>Step 3: Download and Install PHP Manager for IIS</h3>
  <ol>
    <li>From the installation files, download and install "PHP Manager for IIS" (PHPManagerForIIS_V1.5.0.msi).</li>
  </ol>


<h3>Step 4: Download and Install the Rewrite Module</h3>
  <ol>
    <li>From the installation files, download and install "URL Rewrite Module" (rewrite_amd64_en-US.msi).</li>
  </ol>
  

<h3>Step 5: Download and Configure PHP</h3>
  <ol>
    <li>Create a directory, e.g., C:\PHP.</li>
       <br />
<p>
<img src="https://i.imgur.com/oaT10VC.png" height="80%" width="80%" alt="Create PHP directory"/>
</p>
<p>
    <li>From the installation files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip).</li>
    <li>Extract the contents into C:\PHP.</li>
     <br />
<p>
<img src="https://i.imgur.com/eEaQOy4.png" height="80%" width="80%" alt="Extract PHP"/>
</p>
  </ol>


<h3>Step 6: Install VC Redistributable</h3>
  <ol>
    <li>From the installation files, download and install VC_redist.x86.exe.</li>
  </ol>


<h3>Step 7: Install MySQL</h3>
  <ol>
    <li>From the installation files, download MySQL 5.5.62 (mysql-5.5.62-win32.msi).</li>
    <li>Choose a "Typical Setup."</li>
    <li>Launch the MySQL Configuration Wizard after installation and select "Standard Configuration." Set the root password (e.g., Password1).</li>
    <br />

<p>
<img src="https://i.imgur.com/lTt04Uq.png" height="80%" width="80%" alt="MySQL Credentials"/>
</p>
  </ol>


<h3>Step 8: Configure IIS</h3>
  <ol>
    <li>Open IIS Manager.</li>
    <li>Register PHP: In IIS Manager, select your server, then double-click on "Handler Mappings."</li>
    <li>Click "Add Module Mapping" and configure it to handle .php files with the PHP executable.</li>
  </ol>


<h3>Step 9: Download and Install osTicket:</h3>
  <ol>
    <li>Download osTicket from the provided installation files.</li>
    <li>Extract the contents and copy the "upload" folder to C:\inetpub\wwwroot.</li>
    <li>Rename the "upload" folder to "osTicket.</li>
  </ol>


<h3>Step 10: Restart IIS</h3>
  <ol>
    <li>In IIS Manager, select your server, and click "Restart" from the right-hand side.</li>
  </ol>

<h3>Step 11: Configure PHP Extensions:</h3>
  <ol>
    <li>In IIS Manager, double-click "PHP Manager."</li>
    <li>Click "Enable or disable an extension."</li>
    <li>Enable the following extensions: php_imap.dll, php_intl.dll, php_opcache.dll.</li>
  </ol>

<h3>Step 12: Rename Configuration File:</h3>
  <ol>
    <li>Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php.</li>
  </ol>

<h3>Step 13: Set Permissions</h3>
  <ol>
    <li>Right-click ost-config.php, go to "Properties," and under the "Security" tab, assign appropriate permissions.</li>
    <li>Remove inheritance and give "Everyone" read and execute permissions.</li>
  </ol>

<h3>Step 14: Complete osTicket Setup</h3>
  <ol>
    <li>Open a web browser and navigate to http://localhost/osTicket/scp/. Follow the on-screen instructions to set up osTicket, including database configuration</li>
  </ol>

<h3>Step 15: Cleanup</h3>
  <ol>
    <li>Delete the C:\inetpub\wwwroot\osTicket\setup directory.</li>
    <li>Set permissions for ost-config.php to "Read" only.</li>
  </ol>

<h3>Access osTicket</h3>
  <ol>
    <li>You can access the osTicket admin panel at http://localhost/osTicket/scp/login.php.</li>
    <li>The end-user portal is available at http://localhost/osTicket/.</li>
  </ol>
  
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
