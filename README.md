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
    <li>Right-click the Windows icon and select "Run."</li>
    <li>Type "control" to open the Control Panel, and then click on "Programs."
</li>
    <li>Next, click on "Turn Windows features on or off." This action opens the "Windows Features" dialog.</li>
    <li>In the "Windows Features" dialog, scroll down or search for "Internet Information Services." </li>
    <li>Add the IIS Management Console by following this path: Internet Information Services -> Web Management Tools -> IIS Management Console [X] IIS Management Console</li>
    <li>Additionally, ensure that you add the required features: CGI and Common HTTP Features.</li>
    <br />
<p>
<img src="https://i.imgur.com/1Xx2vhl.png" height="80%" width="80%" alt="CGI path and seletion"/>
</p>
<p>
   <br />
<p>
<img src="https://i.imgur.com/4CuRFyZ.png" height="80%" width="80%" alt="Common HTTP Features"/>
</p>
<p>
  <li>Open a web browser and visit http://127.0.0.1/. If the installation was successful you will see a site like the one depicted below.</li>
     <br />
<p>
<img src="https://i.imgur.com/vV12vmo.png" height="80%" width="80%" alt="Visit Webpage to Confirm Installation"/>
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
    <li>Open IIS Manager and run an Administrator.</li>
      <br />
<p>
<img src="https://i.imgur.com/YG6FD1b.png" height="80%" width="80%" alt="IIS Run as Admin"/>
</p>
    <li>Register PHP: In IIS Manager
       <ul>
        <li>Double click PHP Manager</li>
        <li>Select "register new PHP version"</li>
        <li>Provide the path "C:\PHP\php-cgi.exe"</li>
         <br />

<p>
<img src="https://i.imgur.com/U6ci6Bc.png" height="80%" width="80%" alt="Register PHP"/>
</p>
      </ul>
    </li>
    <li>In IIS Manager, select your server, and click "Restart" from the right-hand side.</li>
       <br />

<p>
<img src="https://i.imgur.com/Zk1AzMz.png" height="80%" width="80%" alt="Restart Webserver"/>
</p>
  </ol>


<h3>Step 9: Download and Install osTicket</h3>
  <ol>
    <li>Download osTicket from the provided installation files.</li>
    <li>Extract the contents and copy the "upload" folder to C:\inetpub\wwwroot. Make a note of the folder pathway. You can simply drag and drop the "upload" folder.</li>
    <li>Rename the "upload" folder to "osTicket."</li>
    <br />

<p>
<img src="https://i.imgur.com/qVP0ghE.png" height="80%" width="80%" alt="upload to osTicket"/>
</p>
    <li>In IIS Manager, select your server, and then click "Restart" from the right-hand side.</li>
  <li>Navigate to Sites -&gt; Default -&gt; osTicket. On the right, click “Browse *:80”. If the osTicket installation was successful, you will see a site that resembles the one depicted below.</li>
         <br />

<p>
<img src="https://i.imgur.com/k6ygW7d.png" height="80%" width="80%" alt="Successful osTicket Install"/>
</p>
  </ol>


<h3>Step 10: Configure PHP Extensions</h3>
  <ol>
    <li>In IIS Manager, double-click "PHP Manager."</li>
    <li>Click "Enable or disable an extension."</li>
    <br />

<p>
<img src="https://i.imgur.com/BQ2JsNP.png" height="80%" width="80%" alt="Enable Extensions PHP"/>
</p>
    <li>Enable the following extensions: 
      <ul>
        <li>php_imap.dll</li>
        <li>php_intl.dll</li>
        <li>php_opcache.dll</li>
      </ul>
    </li>
    <li>Refresh the osTicket site in your browser and observe the changes below.</li>
      <br />

<p>
<img src="https://i.imgur.com/6jE98lE.png" height="80%" width="80%" alt="Enable Extensions PHP"/>
</p>
  </ol>

<h3>Step 11: Rename Configuration File</h3>
  <ol>
    <li>Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php.</li>
  </ol>

<h3>Step 12: Set Permissions</h3>
  <ol>
    <li>Right-click ost-config.php, go to "Properties," and under the "Security" tab, assign appropriate permissions.</li>
    <li>Disable inheritance and give "Everyone" read and execute permissions.</li>
    <br />
<p>
<img src="https://i.imgur.com/eRcDe4b.png" height="80%" width="80%" alt="Extract PHP"/>
</p>
  </ol>

<h3>Step 13: Begin osTicket Setup</h3>
  <ol>
    <li>Open a web browser and navigate to http://localhost/osTicket/scp/.</li>
    <li>Name the Helpdesk and assign a default email to receive emails from customers.</li>
  </ol>

<h3>Step 14: Install HeidiSQL</h3>
  <ol>
    <li>From the Installation Files, download and install HeidiSQL.</li>
    <li>When installation is complete, create a new session, root/[password from MySQL credentials creation]</li>
         </br>
<p>
<img src="https://i.imgur.com/xqI7LmN.png" height="80%" width="80%" alt="Launch New Session HeidiSQL"/>
</p>
<p>
    <li>Connect to the session and create a database called “osTicket”</li>
    </br>
<p>
<img src="https://i.imgur.com/xuYtLsN.png" height="80%" width="80%" alt="create osTicket Database"/>
</p>
<p>
  </ol>


<h3>Step 15: Continue Setting Up osTicket in the Browser</h3>
  <ol>
    <li>After installing HeidiSQL, complete the bottom of the setup form under the heading "Database Settings":
      <ul>
        <li>MySQL Database: osTicket</li>
        <li>MySQL Username: root</li>
        <li>MySQL Password: (use the password you created when setting up the MySQL Credentials)</li>
      </ul></li>
     </br>
<p>
<img src="https://i.imgur.com/HV4Vslk.png" height="80%" width="80%" alt="Database Settings"/>
</p>
<p>
    <li>Click “Install Now!”</li>
     </br>
<p>
<img src="https://i.imgur.com/iq2gigu.png" height="80%" width="80%" alt="Success osTicket Install"/>
</p>
  </ol>
 

<h3>Step 16: Cleanup</h3>
  <ol>
    <li>Delete the C:\inetpub\wwwroot\osTicket\setup directory.</li>
    </br>
<p>
<img src="https://i.imgur.com/3XzCuI6.png" height="80%" width="80%" alt="Delete Set-up Folder"/>
</p>
<p>
    <li>Set permissions for ost-config.php to "Read" only.</li>
    </br>
<p>
<img src="https://i.imgur.com/J3GI9u0.png" height="80%" width="80%" alt="Read Only"/>
</p>
<p>
  </ol>

<h3>Step 17: Access osTicket</h3>
  <ol>
    <li>You can access the osTicket admin panel at http://localhost/osTicket/scp/login.php.</li>
    <p>
      <br />
<img src="https://i.imgur.com/vvitx3c.png" height="80%" width="80%" alt="osTicket Installed"/>
</p>
<p>
    <li>The end-user portal is available at http://localhost/osTicket/.</li>
  </ol>
  

