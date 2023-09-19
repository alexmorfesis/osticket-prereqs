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
  </ol>


<h3>Step 3: Download and Install PHP Manager for IIS</h3>
  <ol>
    <li>From the installation files, download "PHP Manager for IIS" (PHPManagerForIIS_V1.5.0.msi).</li>
    <li>Install it.</li>
  </ol>


<h3>Step 4: Download and Install the Rewrite Module</h3>
  <ol>
    <li>From the installation files, download "URL Rewrite Module" (rewrite_amd64_en-US.msi).</li>
    <li>Install it.</li>
  </ol>
  

<h3>Step 5: Download and Configure PHP</h3>
  <ol>
    <li>Create a directory, e.g., C:\PHP.</li>
    <li>From the installation files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip).</li>
    <li>Extract the contents into C:\PHP.</li>
  </ol>
<p>


<h3>Step 6: Install VC Redistributable</h3>
  <ol>
    <li>From the installation files, download and install VC_redist.x86.exe.</li>
  </ol>


<h3>Step 7: Install MySQL</h3>
  <ol>
    <li>From the installation files, download MySQL 5.5.62 (mysql-5.5.62-win32.msi).</li>
    <li>Choose a "Typical Setup."</li>
    <li>Launch the MySQL Configuration Wizard after installation and select "Standard Configuration." Set the root password (e.g., Password1).</li>
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


<h3></h3>
  <ol>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
  </ol>


<h3></h3>
  <ol>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
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
