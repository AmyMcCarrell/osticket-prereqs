
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Setting Up for Success: Prerequisites and Installation Guide</h1>

Hello and welcome! I'm Amy, an IT professional passionate about empowering teams with effective communication tools. I'm thrilled to present my first GitHub project and tutorial on setting up osTicket, a powerful open-source help desk ticketing system. If you’re looking to streamline your support communications, you’ve come to the right place!

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
- **osTicket Installation files**
  - [PHP Manager for IIS](https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link)
  - [Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link)
  - [PHP 7.3.8](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link)
  - [Microsoft Visual C++ 2009 Redistributable Package](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)
  - [MySQL 5.5.62](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link)


<h2>Installation Steps</h2>

<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/49fb9c9c-5da0-4fbf-a0ff-f52b8a70543e">

Let's begin by creating a resource group in Microsoft Azure. Open the Azure portal and navigate to the Resource Group section. 
Click on "Create Resource Group" or type "resource" in the search bar to find the option. 

</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/40eada66-b9cc-4014-a6d4-035ec64f8128">
Choose a unique name and select a region for your resource group.
1. Create a RG name 
2. Choose a Region  (I chose RG-osTicket and (US) East US)
3. Click Review + Create
After that has been done, we will next create a Virtual Machine in the rescource group. 
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/287fbdc3-829d-4e5c-b840-c71cc36f6a1a">


</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/854652a9-28de-4e92-9a44-e899d01e8a38">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/79716214-af1b-4466-b99c-5c86301351bf">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/ec27d128-bbb1-4734-a641-25b2ae750c7c">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/e5e2871f-09b2-435a-856b-9aa9f7bc1bf5">


</p>

<br><br> 
<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/c366ea49-519f-429b-ba67-aff6c51d70a3">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/4eaacf69-3b41-4957-a3d1-ad6f3f1bfe29">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/635475b9-20a2-4c70-8070-aca7b21abc11">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/a9bb65e0-a49c-4ed4-b6c6-b9bca1d7eed2">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/bf5ea8fc-e474-421f-9fe5-225c67cceeab">
</p>


<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/9451808c-1fe9-47ee-9074-c6aa65000dea">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/74eaa0a9-629b-418a-87ac-a91f3263b2c9">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/4f826472-abc4-4b20-b2cd-44d21f28a239">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/d3f88923-5bd6-4c63-a9ea-62893e38a341">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/31ba8ad5-2132-4b51-9a13-4b5177aa69c4">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/d9308db4-d1ae-4538-9e13-f8ef36a1223e">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/6c319441-9d6a-4205-9141-3b20908fd7ec">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/067353f1-6dcd-4539-95a7-92640edab5cb">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/0a1604be-642d-4cd9-93e0-09f334683164">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/25afab08-141b-4db0-90e7-a2921496e137">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/72650f92-2f1a-4314-a540-023449e6efcc">
</p>

<br><br>


<p align="center">
  <img src="https://github.com/AmyMcCarrell/osticket-prereqs/assets/137266179/b91e8eb1-9981-465b-9115-6f4e4716529e">
</p>

<br><br>


