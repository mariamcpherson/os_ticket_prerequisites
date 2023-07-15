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

- Create a Windows 10 Virtual Machine
- Install/Enable IIS in Windows
- Install PHP Manager for IIS
- Install Rewrite Module
- Download and copy PHP files
- Install Microsoft Visual C++
- Install MySQL Server

<h2>Installation Steps: Prerequisites</h2>

<p>
First, we'll start by setting up all the prerequisites needed for the osTicket installation.
</p>
<br />

<p>
- Step 1:
  Create a Windows 10 Virtual Machine in Azure, preferably choose a minimum of 2 Virtual CPUs.
</p> 

<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/17b98cc6-4023-4772-8341-c227113ace16)"/>
</p>
<br />

<p>
- Step 2: Enable IIS in Windows with CGI and Common HTTP Features and IIS Management Console.
  Control Panel → Programs → Turn Windows Features on or off → Internet Information Services → World Wide Services → Apllication Development Features 
</p>
<p>
  X CGI
</p>
 <p>
  X Common HTTP Features
</p>
  
<p>
 <img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/0ae1c3fc-6545-4c83-a121-bc7a1e7e2776)"/>
</p>

<p>
 Control Panel → Programs → Turn Windows Features on or off → Internet Information Services → Web Management Tools → IIS Management Console
 </p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/787613cc-1011-415a-98de-6cef95fc966b)"/>
</p>
<br />

<p>
  - Step 3: Install PHP Manager for IIS.
</p>
<br />

<p>
- Step 4: Install Rewrite module.
</p>

<p>
 <img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/08ff6fbc-2b02-46d1-ab75-6b8ba3681a98"/>
</p>
<br />

<p>
  - Step 5: Download PHP and copy the "upload" folder into a New Folder named PHP in your VM's hard drive.
</p>
<br />

<p>
- Step 6: Install Microsoft Visual CC++
</p>
<br />
  
<p>
- Step 7: Install MySQL Server, Standard Configuration.
</p>
<br />

<p>
- Step 8: Download osTicket, and extract and copy the "upload" folder to c:\inetpub\wwwroot
</p>

<p>
 <img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/08ff6fbc-2b02-46d1-ab75-6b8ba3681a98"/>
</p>
<br />

 <h2>Installation Steps: osTicket Installation</h2>


<p>
Now that we have all our prerequisite configuration, we can start installing osTicket.
</p>
 
<p>
-Steo 1: Open IIS, and Stop and Start the server. Then, go to Sites → Default → osTicket
</p>
On the right, click "Browse *:80 
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/f43d358a-188f-424c-9406-bd4bb2a29abc)"/>
</p>
  
<p>
This will take you to the osTicket installer on your web browser, and you'll notice that some of the extensions are not enables. We will need to enable extensions php_impap.dll, php_intl-dll, and php_opcache.dll.
</p>

<p>
Go back to IIS → Sites  → Default  → osTicket
</p>
<p>
Double-click PHP Manager on the right, then "Enable or disable an extension", and right-click to enable the three extensions we need: 
</p>
<p>
php_impap.dll
</p>
<p>
php_intl-dll
</p>
<p>
php_opcache.dll
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/36d7856e-9697-4617-a9ad-7455924073d8)"/>
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/94b99468-1421-4668-a5c3-6615b245ef0f)"/>
</p>
<br />


<p>
Step 2: Rename the "ost-sampleconfig.php" file inside the osTicket folder in your hard drive to "ost/config".
</p>
<p>
C:\inetpub\wwwroot\osTicket\include\ost/sampleconfig.php
</p>
<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/94b99468-1421-4668-a5c3-6615b245ef0f)"/>
</p>
<br />
<
  p>
</p>



<br />
