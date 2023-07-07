
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Setting Up for Success: Prerequisites and Installation Guide</h1>

Hello and welcome! I'm Amy, an IT professional passionate about empowering teams with effective communication tools. I'm thrilled to present my first GitHub project and tutorial on setting up osTicket. If you’re looking to streamline your support communications, you’ve come to the right place!

<h2>🛠 What is osTicket?</h2>
osTicket is a highly regarded open-source ticketing system. Imagine having a centralized command center for all your customer support communications. Whether it’s emails, phone calls, or web-based forms, osTicket effortlessly aggregates these inquiries and provides an intuitive multi-user web interface. The end game? A structured and efficient way to manage, organize, and archive support requests and responses, ensuring your customers receive the exceptional service they deserve.
</p>

<br>


In this walkthrough, we’ll tackle the essentials – from prerequisites to a step-by-step installation guide. Ready to upgrade your customer support experience? Let’s get started!


<h2>Tools and Technologies We Will Employ:</h2>

- **Microsoft Azure Virtual Machine** (a virtualized computing resource over the cloud)
- **Remote Desktop** (enabling remote access to the virtual machine)
- **Internet Information Services (IIS)** - A robust web server solution from Microsoft
- **Heidi SQL** (an intuitive database management system for streamlined data handling)

<h2>Operating Systems Used </h2>

- **Windows 10**</b> (21H2)

<h2>List of Prerequisites</h2>

- **Microsoft Azure Virtual Machine**
  - [Active subscription in Azure](https://portal.azure.com)
- **osTicket Installation Files**
  - [PHP Manager for IIS](https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link)
  - [Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link)
  - [PHP 7.3.8](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link)
  - [Microsoft Visual C++ 2009 Redistributable Package](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)
  - [MySQL 5.5.62](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link)


<h2>Installation Steps</h2>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/49fb9c9c-5da0-4fbf-a0ff-f52b8a70543e">

Let's begin by creating a resource group in Microsoft Azure. Open the Azure portal and navigate to the Resource Group section.<br>
Click on "Create Resource Group" or type "resource" in the search bar to find the option. 
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/40eada66-b9cc-4014-a6d4-035ec64f8128">
  
Create a resource group by giving it a unique name and selecting a region.<br>
1. Enter a unique name for your Resource Group.<br>
2. Select a Region for your resource group (e.g., I chose "US East").<br>
3. Click 'Review + Create'.<br>
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/287fbdc3-829d-4e5c-b840-c71cc36f6a1a">
  
In the search bar, start typing "Virtual". Once the option labeled "Virtual Machine" appears, click on it.
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/854652a9-28de-4e92-9a44-e899d01e8a38">

1. Now click "Create" and
2. Select "Azure virtual machine" from the drop down menu
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/79716214-af1b-4466-b99c-5c86301351bf">

</p>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/ec27d128-bbb1-4734-a641-25b2ae750c7c">

Next, let's generate a name for our virtual machine within the Resource Group (RG). Please refer to the visual instructions provided above for guidance.<br>

Create a username and password for your virtual machine, similar to how you would set them up for your personal computer. It's important to jot down your username and passwords as we will need them later.
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/e5e2871f-09b2-435a-856b-9aa9f7bc1bf5">

Once our machine is ready, please click the 'Copy' option located to the right of the Public IP Address displayed above. Make sure to copy this IP address.
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/c366ea49-519f-429b-ba67-aff6c51d70a3">

Next, open the Remote Desktop Connection application on your computer. Paste the copied IP address into the "Computer:" field.
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/5f50f7da-615e-4946-b83c-a4f02291494a">
  
Now we need to enable CGI within Internet Information Services (IIS) after establishing the connection, please follow these steps:

1. Click on the Start Menu.
2. Open the Windows Features.
3. Locate and select 'Internet Information Services.'
4. Expand 'World Wide Web Services.'
5. Select 'Application Development Features.'
6. Check the box for 'CGI.'

 You can also use the following pathway to navigate to the desired setting: <br>
 **Start Menu > Windows Feature > Internet Information Services > World Wide Web Services > Application Development Features > CGI.**  
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/635475b9-20a2-4c70-8070-aca7b21abc11">

Great! Now that we have enabled IIS, the next step is to install Web Platform Installer. To access all the necessary installation files, you can follow this link:  [https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6].
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/a9bb65e0-a49c-4ed4-b6c6-b9bca1d7eed2">

To complete the installation process, please follow these steps:

1. Install PHP Manager for IIS:
   - Download and run the installation file named "PHPManagerForIIS_V1.5.0.msi" from the installation files.

2. Install the Rewrite Module:
   - Download and run the installation file named "rewrite_amd64_en-US.msi" from the installation files.

3. Create a new directory named "C:\PHP" on your system.

4. Download PHP 7.3.8:
   - Download the file named "php-7.3.8-nts-Win32-VC15-x86.zip" from the provided files.
   - Once the download is complete, extract the contents of the zip file into the previously created "C:\PHP" directory.

5. Install the Visual C++ Redistributable Package:
   - Download and install "VC_redist.x86.exe" from the installation files.

6. Install MySQL 5.5.62:
   - Download and run the installation file named "mysql-5.5.62-win32.msi" from the installation files.
   -  Follow the prompts for a typical setup.
   - Launch the Configuration Wizard after the installation is complete.
   - Choose the "Standard Configuration" option.
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/9451808c-1fe9-47ee-9074-c6aa65000dea">
</p>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/74eaa0a9-629b-418a-87ac-a91f3263b2c9">
</p>

<br>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/4f826472-abc4-4b20-b2cd-44d21f28a239">

After installing all the necessary files:

1. Open IIS and run it as an Administrator.
2. Register PHP in IIS:
    - Double-click on PHP in IIS.
    - Click on "Register new PHP version"
</p>
<br>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/d3f88923-5bd6-4c63-a9ea-62893e38a341">

 - Follow the sequence in the C:\ directory: PHP -> php.cgi.exe. ⬆️
 - Once PHP has been registered, Open IIS and restart the server by clicking on "Restart Server."   
</p>

<br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/31ba8ad5-2132-4b51-9a13-4b5177aa69c4">

1. Install osTicket v1.15.8:
   - Download osTicket from the Installation Files Folder
   - Extract & copy "upload" folder to "c:\inetpub\wwwroot"
   - Rename the pasted "upload" folder to "osTicket"

2. Again, Restart the server by clicking on "Restart Server" in IIS
</p>
<br>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/d9308db4-d1ae-4538-9e13-f8ef36a1223e">
- Access osTicket:
   - Go to "Sites" > "Default" > "osTicket"
   - On the right side, click "Browse *:80"
</p>

<br>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/6c319441-9d6a-4205-9141-3b20908fd7ec">
To enable these ⬆️ necessary extensions:

1. Go back to IIS and navigate to "Sites" > "Default" > "osTicket"

2. Double-click PHP Manager

3. Click on "Enable or disable an extension"

4. Enable the following extensions:
   - php_imap.dll
   - php_intl.dll
   - php_opcache.dll

After these extentions are enabled it should look like this ⬇️
</p>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/067353f1-6dcd-4539-95a7-92640edab5cb">
</p>

<br>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/0a1604be-642d-4cd9-93e0-09f334683164">

- Go to file explorer:  This PC > Windows (C:) > inetpub > wwwroot > osTicket > include
- Look for the file named "ost-sampleconfig.php" 
- Rename it to "ost-config.php"

- Now right click the file, Click "Properties" > "Security" > "Advanced" > "Disable Inheritance" 
Select "Remove all new permissions", and give "everyone" permissions.
</p>

<br>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/25afab08-141b-4db0-90e7-a2921496e137">
</p>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/72650f92-2f1a-4314-a540-023449e6efcc">

Finally we will download and install [HeidiSQL](https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe) 
- Open Heidi SQL
- Create a new session, root/Password1
- Connect to the session
- Create a database called “osTicket”<br>
    
Now, let's continue setting up osTicket in the browser. Jot down your login credentials.
- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: Password1
- Click "Install Now!"</p>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/b91e8eb1-9981-465b-9115-6f4e4716529e">
</p>
Congratulations!
