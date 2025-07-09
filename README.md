# Active Directory Home Lab

### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

## Description  
Learn Active Directory by building a home lab with Oracle VirtualBox.

## Tools
- PowerShell
- Diskpart

## Environment
- Windows 10 (21H2)

---

## Lab Guide

### Step 1: Download VirtualBox
<p align="center">
<em>VirtualBox download page</em><br/>
<img src="images/1.png" width="80%" alt="Download VirtualBox"/>
</p>
- **Action:** 
  - Download VirtualBox installer
- **Settings:** 
  - Version 6.1.x or newer
  - Include Extension Pack
- **Explanation:** 
  - Base virtualization software
- **Common Mistake:** 
  - Getting only base package

---

### Step 2: Install VirtualBox  
<p align="center">
<em>Installation wizard</em><br/>
<img src="images/2.png" width="80%" alt="Install VirtualBox"/>
</p>
- **Action:** 
  - Run installer as admin
- **Settings:** 
  - Accept defaults
  - Install both components
- **Explanation:** 
  - Sets up virtualization platform
- **Common Mistake:** 
  - Skipping Extension Pack

---

### Step 3: VirtualBox Interface  
<p align="center">
<em>Main console view</em><br/>
<img src="images/3.png" width="80%" alt="VirtualBox Interface"/>
</p>
- **Action:** 
  - Launch VirtualBox
- **Settings:** 
  - Note machine list
  - Check toolbar buttons
- **Explanation:** 
  - VM management center
- **Common Mistake:** 
  - Not exploring menus

---

### Step 4: Create New VM  
<p align="center">
<em>New VM dialog</em><br/>
<img src="images/4.png" width="80%" alt="Create VM"/>
</p>
- **Action:** 
  - Click "New"
- **Settings:** 
  - Name: "DC1"
  - Type: Windows Server
- **Explanation:** 
  - Domain Controller setup
- **Common Mistake:** 
  - Wrong version selection

---

### Step 5: Allocate Memory  
<p align="center">
<em>RAM allocation</em><br/>
<img src="images/5.png" width="80%" alt="VM Memory"/>
</p>
- **Action:** 
  - Set RAM size
- **Settings:** 
  - 2048MB minimum
  - Don't exceed 50% host RAM
- **Explanation:** 
  - Critical for performance
- **Common Mistake:** 
  - Too much/little RAM

---

### Step 6: Create Virtual Disk  
<p align="center">
<em>Disk creation</em><br/>
<img src="images/6.png" width="80%" alt="Virtual Disk"/>
</p>
- **Action:** 
  - Create new disk
- **Settings:** 
  - Dynamically allocated
  - VDI format
- **Explanation:** 
  - VM storage space
- **Common Mistake:** 
  - Fixed size allocation

---

### Step 7: Disk File Type  
<p align="center">
<em>Format selection</em><br/>
<img src="images/7.png" width="80%" alt="Disk Format"/>
</p>
- **Action:** 
  - Select disk type
- **Settings:** 
  - Choose VDI
  - Avoid VMDK/VHD
- **Explanation:** 
  - Native VirtualBox format
- **Common Mistake:** 
  - Wrong format selection

---

### Step 8: Disk Size  
<p align="center">
<em>Capacity setting</em><br/>
<img src="images/8.png" width="80%" alt="Disk Size"/>
</p>
- **Action:** 
  - Set storage size
- **Settings:** 
  - Minimum 30GB
  - More for future needs
- **Explanation:** 
  - OS + AD requirements
- **Common Mistake:** 
  - Under-allocation

---

### Step 9: VM Settings  
<p align="center">
<em>Final review</em><br/>
<img src="images/9.png" width="80%" alt="VM Settings"/>
</p>
- **Action:** 
  - Verify configuration
- **Settings:** 
  - Check name
  - Verify resources
- **Explanation:** 
  - Pre-creation validation
- **Common Mistake:** 
  - Skipping review

---

### Step 10: Start VM  
<p align="center">
<em>Startup screen</em><br/>
<img src="images/10.png" width="80%" alt="Start VM"/>
</p>
- **Action:** 
  - Power on VM
- **Settings:** 
  - Attach Windows ISO
  - Select boot media
- **Explanation:** 
  - Begin OS installation
- **Common Mistake:** 
  - No ISO attached

---

### Step 11: Windows Installation  
<p align="center">
<em>OS setup</em><br/>
<img src="images/11.png" width="80%" alt="Windows Install"/>
</p>
- **Action:** 
  - Install Windows Server
- **Settings:** 
  - Standard/Datacenter
  - GUI mode
- **Explanation:** 
  - Base for AD services
- **Common Mistake:** 
  - Core installation
---

### Step 12: Disk Partition
<p align="center">
<img src="images/12.png" width="80%" alt="Step 12"/>
</p>
- **Action:** Create OS partition
- **Settings:** Use entire disk space
- **Explanation:** Prepare for installation
- **Common Mistake:** Multiple partitions unnecessarily

---

### Step 13: Install Progress
<p align="center">
<img src="images/13.png" width="80%" alt="Step 13"/>
</p>
- **Action:** Wait for installation
- **Settings:** Automatic reboots expected
- **Explanation:** System files being deployed
- **Common Mistake:** Interrupting process

---

### Step 14: Admin Password
<p align="center">
<img src="images/14.png" width="80%" alt="Step 14"/>
</p>
- **Action:** Set administrator password
- **Settings:** Complex password required
- **Explanation:** Critical security step
- **Common Mistake:** Weak credentials

---

### Step 15: Server Desktop
<p align="center">
<img src="images/15.png" width="80%" alt="Step 15"/>
</p>
- **Action:** Login to server
- **Settings:** Initial configuration
- **Explanation:** Ready for AD installation
- **Common Mistake:** Skipping updates

---

### Step 16: Server Manager
<p align="center">
<img src="images/16.png" width="80%" alt="Step 16"/>
</p>
- **Action:** Open Server Manager
- **Settings:** Review dashboard
- **Explanation:** Central management console
- **Common Mistake:** Ignoring warnings

---

### Step 17: Add Roles
<p align="center">
<img src="images/17.png" width="80%" alt="Step 17"/>
</p>
- **Action:** Add AD Domain Services
- **Settings:** Include management tools
- **Explanation:** Core AD components
- **Common Mistake:** Missing dependencies

---

### Step 18: Promote to DC
<p align="center">
<img src="images/18.png" width="80%" alt="Step 18"/>
</p>
- **Action:** Promote server to DC
- **Settings:** Create new forest
- **Explanation:** Establish domain foundation
- **Common Mistake:** Wrong domain name

---

### Step 19: DCPromo
<p align="center">
<img src="images/19.png" width="80%" alt="Step 19"/>
</p>
- **Action:** Run DCPromo wizard
- **Settings:** Set forest/domain levels
- **Explanation:** AD installation process
- **Common Mistake:** Incorrect levels

---

### Step 20: DNS Options
<p align="center">
<img src="images/20.png" width="80%" alt="Step 20"/>
</p>
- **Action:** Configure DNS
- **Settings:** Install DNS server
- **Explanation:** Required for AD
- **Common Mistake:** Skipping DNS

---

### Step 21: Directory Services
<p align="center">
<img src="images/21.png" width="80%" alt="Step 21"/>
</p>
- **Action:** Restore mode password
- **Settings:** Secure password
- **Explanation:** Disaster recovery
- **Common Mistake:** Simple password

---

### Step 22: Prerequisites Check
<p align="center">
<img src="images/22.png" width="80%" alt="Step 22"/>
</p>
- **Action:** Review warnings
- **Settings:** Address any issues
- **Explanation:** Pre-installation verification
- **Common Mistake:** Ignoring warnings

---

### Step 23: Installation
<p align="center">
<img src="images/23.png" width="80%" alt="Step 23"/>
</p>
- **Action:** Begin installation
- **Settings:** Automatic reboot
- **Explanation:** AD components installing
- **Common Mistake:** Interrupting

---

### Step 24: Post-Install
<p align="center">
<img src="images/24.png" width="80%" alt="Step 24"/>
</p>
- **Action:** Verify AD installation
- **Settings:** Check DNS and AD tools
- **Explanation:** Confirm successful setup
- **Common Mistake:** Not verifying

---

### Step 25: AD Users
<p align="center">
<img src="images/25.png" width="80%" alt="Step 25"/>
</p>
- **Action:** Open AD Users and Computers
- **Settings:** Create organizational units
- **Explanation:** User management
- **Common Mistake:** Flat structure

---

### Step 26: Create Users
<p align="center">
<img src="images/26.png" width="80%" alt="Step 26"/>
</p>
- **Action:** New user accounts
- **Settings:** Follow naming conventions
- **Explanation:** Populate directory
- **Common Mistake:** Weak passwords

---

### Step 27: PowerShell
<p align="center">
<img src="images/27.png" width="80%" alt="Step 27"/>
</p>
- **Action:** Bulk user creation
- **Settings:** Import CSV data
- **Explanation:** Automation advantage
- **Common Mistake:** Format errors

---

### Step 28: Group Policy
<p align="center">
<img src="images/28.png" width="80%" alt="Step 28"/>
</p>
- **Action:** Configure GPOs
- **Settings:** Password policies
- **Explanation:** Security enforcement
- **Common Mistake:** Overly restrictive

---

### Step 29: Client Join
<p align="center">
<img src="images/29.png" width="80%" alt="Step 29"/>
</p>
- **Action:** Join client to domain
- **Settings:** Proper credentials
- **Explanation:** Test domain functionality
- **Common Mistake:** DNS misconfiguration

---

### Step 30: Authentication
<p align="center">
<img src="images/30.png" width="80%" alt="Step 30"/>
</p>
- **Action:** Test domain login
- **Settings:** User credentials
- **Explanation:** Verify AD authentication
- **Common Mistake:** Wrong credentials

---

### Step 31: Shared Resources
<p align="center">
<img src="images/31.png" width="80%" alt="Step 31"/>
</p>
- **Action:** Create shared folder
- **Settings:** Proper permissions
- **Explanation:** Test resource access
- **Common Mistake:** Everyone permission

---

### Step 32: Lab Complete
<p align="center">
<img src="images/32.png" width="80%" alt="Step 32"/>
</p>
- **Action:** Document configuration
- **Settings:** Backup VM
- **Explanation:** Preserve lab work
- **Common Mistake:** No backups
