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


 <h2>Installation Steps: osTicket Installation</h2>


<p>
Now that we have all our prerequisite configuration, we can start installing osTicket.
</p>

<p>
- Step 1: Download osTicket, and extract and copy the "upload" folder to c:\inetpub\wwwroot. Rename "upload" folder, "osTicket".
</p>

<p>
 <img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/72c3c89d-6776-4c5f-99d1-398494d51529)"/>
</p>
<br />
 
<p>
- Step 2: Open IIS, and Stop and Start the server. Then, go to Sites → Default → osTicket
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
- Step 3: Rename the "ost-sampleconfig.php" file inside the osTicket folder in your hard drive to "ost/config".
</p>
<p>
C:\inetpub\wwwroot\osTicket\include\ost/sampleconfig.php
</p>
<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/23db55ca-4381-4659-bbd1-f9ebd754aa87)"/>
</p>
<br />
<p>
Now, assign permissions to this "ost-config" file. Right-click on the file, Properties → Security → Advanced → Disable Inheritance
<p>
"Remove All Permissions"

<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/611b8d54-3049-4396-bd42-08c33e08e3df)"/>
</p>

<p>
Now, click on "Add..." → Select Principal. Enter subject name by typying "Everyone". Then assign Full Control. 
  
<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/5bcb1412-798d-454f-8d2b-e212c9fde572)"/>
</p>

<p>
Now, if we go back to the Web browser where we were setting up the osTicket installation, and click Continue. It should look like this>
</p>
<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/1b2b0209-f119-4a51-8f4d-01e8939bbb5e)"/>
</p>

<p>
- Step 4: download and install HeidiSQL to connect to a SQL server and install a Database.
</p>

<p>
Now, let's create a new session on Heidi SQL. Click on New.  
</p>

<p>
User name: root
</p>
<p>
Password: Password1
</p>
<p>
Note: for the purposes of this demonstration, I picked a very generic Password and Username.
</p>

<p>
Click Open to start the SQL session. Then right click to Create a New Database. In this example, I named it osTicket.
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_prerequisites/assets/139581822/30e25736-61ca-49fb-92a6-c550f6076448)"/>
</p>
<br />

<p>
- Step 5: Let's go back to the Browser where we are setting up osTicket, and we're going to enter all the information, including Name of the ticketing system, email address to receive requests from customers, etc. 
</p>
<p>
In the MySQL Database field, I entered the name osTicket, as it is the Database that I created in Heidi SQL on the previous step. In the same way, I used the same Username and Password selected in Heidi SQL (username: root; password: Password1).
</p>

<p>
Now, we can FINALLY click "Install Now!"
</p>
</p>
</p>
</p>
</p>
</p>
</p>







<br />
