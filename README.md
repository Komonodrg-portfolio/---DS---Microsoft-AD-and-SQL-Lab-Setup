### [Cybersecurity](https://github.com/Komonodrg-portfolio/Cybersecurity) | [Networking](https://github.com/Komonodrg-portfolio/Networking) | [Data Science (AI)](https://github.com/Komonodrg-portfolio/AI) | [Media Creation](https://github.com/Komonodrg-portfolio/MediaCreation) | [Mission](https://github.com/Komonodrg-portfolio/Mission/)

---
---

# 🪟 Microsoft Active Directory Lab

This project demonstrates how to build a scaled enterprise-like Windows based System Administration lab built using opensource resource offerings from Microsoft. It's designed to emulate a small business in order to practice and gain incite on how these systems operate both independently & in conjunction with one another - bridging the knowledge base gap.  It contains Windows Servers, Windows Hosts, with an aim later on to incorporate Microsoft SQL Server, and the administration of all components.  With a labtop of 16GB  (recommended) of ram, this lab setup should allow for training from anywhere in the world.  8GB of ram should allow most components to run, if not concurrently, but still offer the ability to learn successfully.

---

## 📌 Goals
To illustrate a cost effective platform to allow for the practice and self study in both System Administration using prodominately Industry Standard tech, providing the ability to gain skills in:

- Virtualization & Hypervisor Management
- Operating System Deployment (Windows 10/11 + Server)
- Active Directory Domain Services (AD DS)
- Windows Networking Fundamentals
- Systems Management & Automation
- **Can even be expanded to allow for cyber security training via addition of Penetration Testing VM (Kali) and Logging triage**

---

## 🧰 Tools & Technologies

| Tool       | Purpose           |  VM Requirements                     |
|------------|--------------------------------------|-------------------|
| VMware Workstation / Player    | Hypervisor providing Host Emulation  | N/A 
| Windows 10/11  | Host Systems        |  2CPUs / 2-4GB Ram / 25-50GB HD|
| Windows Server 2022    | Host & SQL Server Administration (later)       | 2CPUs / 4GB Ram / 50-100GB HD |
| SQL Server 2025  | Database Administration Software                      |
| Wireshark  | Packet Capture and Analysis          |

---



---

## 🔧 Setup Instructions

### Prerequisites

A Windows or Linux host system with VMware Workstation installed.

<details>
 <summary><h4>a) System Requirements</h4></summary>
  <br> 
Before lab setup, ensure your PC/Laptop meets minimum requirements for successful operation:<br> 
 <br>

**Windows:**  Click on Start > in search box type: `msinfo` > press Enter

**Linux (Mint):** Click on LM button (bottom left) > type: `System Info` > press Enter


 <p align="center">
  <img src="images/MSInfo.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>
  <img src="images/MintSystemInfo.png" alt="Image 2" width="40%" />
</p>

Check your system specifications vs what the [official EVE-NG installation guide](https://www.eve-ng.net/index.php/documentation/) recommends.  As of the date of this repo creation, current recommended specs:


 <p align="center">
  <img src="images/SystemReqs.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>

</details>
<details>
 <summary><h4>b) Download Hypervisor (VMWare)</h4></summary>
  <br> 
  For this lab, we will run EVE-NG as a virtual machine from within a <a href="https://chatgpt.com/share/68cb87a6-3580-800b-a816-6c42bfab1272/">hypervisor</a> (type 2).  Both Linux and Windows versions are free, but require <a href="https://support.broadcom.com/">signing up for a broadcom account</a> first:<br>
  <br>
<p align="center">
 <img src="images/VMWareInstall1.png" alt="Image 1" width="43%" style="margin-right: 10px;"/>
 <img src="images/VMWareInstall2.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>
 <img src="images/VMWareInstall3.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>
 <img src="images/VMWareInstall4.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>
 <img src="images/VMWareInstall5.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>
</p>  
<br>
Once the installation file downlods successfully, proceed with installation of VMWare:</br><br>

</details> 
<details>
 <summary><h4>c) Install VMWare Workstation</h4></summary>
  <br> 
  
**Windows:**  Navigate to where the file downloaded, and double click it to start the installer...

**Linux:** A few extra steps are needed prior in order to get this installation completed:
<br>
Open up **Terminal** to install VMWare:
<br>
<br>

| Step    | Command |
|---------|---------|
| 1) Install required dependencies | `sudo apt install build-essential linux-headers-$(uname -r)` |
| 2) Navigate to download location  | `cd ~/Downloads` |
| 3) List files in Downlaods folder  | `ls` |
| 4) Make installation file executable  | `chmod +x VMWare...bundle` |
| 5) Run installation file  | `sudo ./VMWare...bundle` |
<br>
<p align="left">
 <img src="images/VMWareInstall6.png" alt="Image 1" width="60%" style="margin-right: 10px;"/>
 <br>
 <p align="left">
 <img src="images/VMWareInstall7.png" alt="Image 1" width="60%" style="margin-right: 10px;"/>

 ---

 <p align="center">
 <img src="images/VMWareInstall8.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>
 <img src="images/VMWareInstall9.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>
 <img src="images/VMWareInstall10.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>
 <img src="images/VMWareInstall11.png" alt="Image 1" width="45%" style="margin-right: 10px;"/>
</p>  

 
</details> 

<details>
 <summary><h3><em><b>🪂  "One Man's Thoughts..."</b></em></h3></summary>
  <br> 
<em>This lab premise was inspired by my Mission for it's origin.  The basis is to have a business with headquarters in both Kisii (located in the mountains of west Kenya) and Nyali (located on the east coast of Kenya).  Both these places are special locales I enjoyed during my time in Kenya.  More important than the locations, are the people I met on my journey who continue to provide and exemplify inspiration, courage and love which serves as the driving force behind this tutorial repo.  The name of this company is Shujaa, a Swahili term that translates to "warrior" or "hero".<br>
<br>
To all, may the pursuit of your hopes and dreams never waver as we all continue to meander through this lifelong journey called "Life".<br>
<br>
 Colleagues,<br>
<br>
 Onward.
</em><br>
<br>
<b>My Vision:</b><br>
    
- <b>To partner or create a foundation that will provide repurposed/decommissioned cellphones / laptops to individuals in remote area</b>
- <b>Provide scholarships to cover the costs for IT Certifications to individuals showing deep aptitude, skill, and readiness</b><br>

<em>Enjoy these pictures from the trip.

Colleagues,Onward.<br></em>

  

![Alt text](images/Kenya/ChurchKids.png)

<p float="center">
  <img src="images/Kenya/SceneryMountainsTea.png" width="200" />
  <img src="images/Kenya/Flower4.png" width="200" />
  <img src="images/Kenya/ScenerySafari22.png" width="200" />
  <img src="images/Kenya/Flowers.png" width="200" />
  <img src="images/Kenya/Giraffe.png" width="200" />
  <img src="images/Kenya/rhinos.png" width="200" />  
  <img src="images/Kenya/SafariCroc.png" width="200" />
  <img src="images/Kenya/ScenerySafariHole.png" width="200" />

![Alt text](images/Kenya/Safari17.png)

  

</details>

## 🌐 Topology





<h2> 🤳 Connect with me:</h2>

[<img align="left" alt="JoshMadakor | YouTube" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/youtube.svg" />][youtube]
[<img align="left" alt="JoshMadakor | Tik Tok" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/tiktok.svg" />][tiktok]
[<img align="left" alt="JoshMadakor | LinkedIn" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />][linkedin]
[<img align="left" alt="JoshMadakor | Instagram" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/instagram.svg" />][instagram]
