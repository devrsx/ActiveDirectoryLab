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

### Step 1: Download VirtualBox
<p align="center">
<em>Official VirtualBox download page showing version selection</em><br/>
<img src="images/1.png" width="80%" alt="Download VirtualBox"/>
</p>

• **Action**  
   ‣ Visit virtualbox.org  
   ‣ Download installer  
• **Settings**  
   ‣ Version: 6.1.38  
   ‣ Include Extension Pack  
• **Explanation**  
   ‣ Foundation for virtualization environment  
• **Common Mistake**  
   ‣ Downloading only base package  

---

### Step 2: Install VirtualBox
<p align="center">
<em>VirtualBox installation wizard with progress bar</em><br/>
<img src="images/2.png" width="80%" alt="Install VirtualBox"/>
</p>

• **Action**  
   ‣ Run installer as Administrator  
   ‣ Complete setup wizard  
• **Settings**  
   ‣ Accept all defaults  
   ‣ Install both components  
• **Explanation**  
   ‣ Core virtualization platform setup  
• **Common Mistake**  
   ‣ Skipping Extension Pack installation  

---

### Step 3: VirtualBox Interface
<p align="center">
<em>Main VirtualBox console showing empty machine list</em><br/>
<img src="images/3.png" width="80%" alt="VirtualBox Interface"/>
</p>

• **Action**  
   ‣ Launch VirtualBox application  
   ‣ Explore interface components  
• **Settings**  
   ‣ Machine list (left panel)  
   ‣ Toolbar buttons (top)  
• **Explanation**  
   ‣ Primary VM management dashboard  
• **Common Mistake**  
   ‣ Not exploring File > Preferences  

---

### Step 4: Create New VM
<p align="center">
<em>'Create Virtual Machine' dialog with name/type fields</em><br/>
<img src="images/4.png" width="80%" alt="Create VM"/>
</p>

• **Action**  
   ‣ Click "New" button  
   ‣ Enter basic configuration  
• **Settings**  
   ‣ Name: "DC1"  
   ‣ Type: Windows Server 2019  
• **Explanation**  
   ‣ Initial Domain Controller setup  
• **Common Mistake**  
   ‣ Selecting wrong OS version  

---

### Step 5: Allocate Memory
<p align="center">
<em>Memory allocation slider with recommended value</em><br/>
<img src="images/5.png" width="80%" alt="VM Memory"/>
</p>

• **Action**  
   ‣ Set RAM allocation size  
• **Settings**  
   ‣ 2048MB minimum  
   ‣ Maximum 50% host RAM  
• **Explanation**  
   ‣ Critical for server performance  
• **Common Mistake**  
   ‣ Allocating too much host memory  

---

### Step 6: Create Virtual Disk
<p align="center">
<em>Virtual disk creation options with selection buttons</em><br/>
<img src="images/6.png" width="80%" alt="Virtual Disk"/>
</p>

• **Action**  
   ‣ Create new virtual disk  
• **Settings**  
   ‣ Select "Create virtual disk now"  
   ‣ Choose dynamically allocated  
• **Explanation**  
   ‣ Flexible storage management  
• **Common Mistake**  
   ‣ Selecting fixed size unnecessarily  

---

### Step 7: Disk File Type
<p align="center">
<em>Disk format selection with VDI/VMDK/VHD options</em><br/>
<img src="images/7.png" width="80%" alt="Disk Format"/>
</p>

• **Action**  
   ‣ Select virtual disk format  
• **Settings**  
   ‣ VDI (VirtualBox Disk Image)  
   ‣ Avoid VMDK/VHD unless needed  
• **Explanation**  
   ‣ Native format for best performance  
• **Common Mistake**  
   ‣ Choosing incompatible format  

---

### Step 8: Disk Size
<p align="center">
<em>Storage capacity slider with size field</em><br/>
<img src="images/8.png" width="80%" alt="Disk Size"/>
</p>

• **Action**  
   ‣ Set virtual disk capacity  
• **Settings**  
   ‣ Minimum 30GB recommended  
   ‣ Additional space for growth  
• **Explanation**  
   ‣ Accommodates OS + AD + updates  
• **Common Mistake**  
   ‣ Underestimating future needs  

---

### Step 9: VM Settings
<p align="center">
<em>Final configuration summary before creation</em><br/>
<img src="images/9.png" width="80%" alt="VM Settings"/>
</p>

• **Action**  
   ‣ Review all settings  
• **Settings**  
   ‣ Verify name: "DC1"  
   ‣ Check RAM/disk allocations  
• **Explanation**  
   ‣ Last chance to correct mistakes  
• **Common Mistake**  
   ‣ Rushing through verification  

---

### Step 10: Start VM
<p align="center">
<em>Virtual Machine start screen with media selection</em><br/>
<img src="images/10.png" width="80%" alt="Start VM"/>
</p>

• **Action**  
   ‣ Power on virtual machine  
• **Settings**  
   ‣ Attach Windows Server ISO  
   ‣ Select correct boot media  
• **Explanation**  
   ‣ Begins operating system installation  
• **Common Mistake**  
   ‣ Forgetting to mount ISO file  

---

---

### Step 11: Windows Installation (Recap)
<p align="center">
<em>Windows Server setup screen with edition selection</em><br/>
<img src="images/11.png" width="80%" alt="Windows Install"/>
</p>

• **Action**  
   ‣ Complete OS installation  
   ‣ Wait for automatic reboots  
• **Settings**  
   ‣ Standard/Datacenter edition  
   ‣ GUI mode required  
• **Explanation**  
   ‣ Prepares base for AD services  
• **Common Mistake**  
   ‣ Choosing Core installation  

---

### Step 12: Initial Server Configuration
<p align="center">
<em>Windows Server desktop after first login</em><br/>
<img src="images/12.png" width="80%" alt="Server Desktop"/>
</p>

• **Action**  
   ‣ Set computer name  
   ‣ Configure network  
• **Settings**  
   ‣ Static IP recommended  
   ‣ Disable IE Enhanced Security  
• **Explanation**  
   ‣ Prepares server for AD role  
• **Common Mistake**  
   ‣ Using DHCP for DC  

---

### Step 13: Server Manager Dashboard
<p align="center">
<em>Server Manager main console view</em><br/>
<img src="images/13.png" width="80%" alt="Server Manager"/>
</p>

• **Action**  
   ‣ Open Server Manager  
   ‣ Review dashboard alerts  
• **Settings**  
   ‣ Note "Add roles" option  
   ‣ Check network configuration  
• **Explanation**  
   ‣ Central management console  
• **Common Mistake**  
   ‣ Ignoring warnings  

---

### Step 14: Add Roles Wizard
<p align="center">
<em>'Add Roles and Features' wizard start screen</em><br/>
<img src="images/14.png" width="80%" alt="Add Roles"/>
</p>

• **Action**  
   ‣ Launch role installation  
• **Settings**  
   ‣ Select "Role-based installation"  
   ‣ Choose current server  
• **Explanation**  
   ‣ First step to install AD  
• **Common Mistake**  
   ‣ Wrong installation type  

---

### Step 15: Select AD DS Role
<p align="center">
<em>Role selection screen with checkboxes</em><br/>
<img src="images/15.png" width="80%" alt="AD DS Role"/>
</p>

• **Action**  
   ‣ Check "Active Directory Domain Services"  
• **Settings**  
   ‣ Include management tools  
   ‣ Accept dependency additions  
• **Explanation**  
   ‣ Core AD components  
• **Common Mistake**  
   ‣ Skipping management tools  

---

### Step 16: Installation Progress
<p align="center">
<em>Installation progress bar screen</em><br/>
<img src="images/16.png" width="80%" alt="Install Progress"/>
</p>

• **Action**  
   ‣ Wait for completion  
   ‣ Don't interrupt process  
• **Settings**  
   ‣ Automatic restart if needed  
   ‣ Verify success message  
• **Explanation**  
   ‣ Installing AD binaries  
• **Common Mistake**  
   ‣ Closing window prematurely  

---

### Step 17: Post-Installation Notification
<p align="center">
<em>Yellow warning bar prompting promotion</em><br/>
<img src="images/17.png" width="80%" alt="Promote Notification"/>
</p>

• **Action**  
   ‣ Click "Promote this server"  
• **Settings**  
   ‣ Note task details  
   ‣ Prepare admin credentials  
• **Explanation**  
   ‣ Next step to make it a DC  
• **Common Mistake**  
   ‣ Missing this notification  

---

### Step 18: Deployment Configuration
<p align="center">
<em>'Add a new forest' option selection</em><br/>
<img src="images/18.png" width="80%" alt="New Forest"/>
</p>

• **Action**  
   ‣ Select "Add new forest"  
   ‣ Enter root domain name  
• **Settings**  
   ‣ Example: corp.contoso.com  
   ‣ Set Forest functional level  
• **Explanation**  
   ‣ Creates domain foundation  
• **Common Mistake**  
   ‣ Overly complex domain name  

---

### Step 19: Domain Controller Options
<p align="center">
<em>DNS and GC options configuration</em><br/>
<img src="images/19.png" width="80%" alt="DC Options"/>
</p>

• **Action**  
   ‣ Set DSRM password  
   ‣ Select DNS server option  
• **Settings**  
   ‣ 8+ character DSRM password  
   ‣ Install DNS (recommended)  
• **Explanation**  
   ‣ Critical for AD functionality  
• **Common Mistake**  
   ‣ Weak DSRM password  

---

### Step 20: DNS Delegation Warning
<p align="center">
<em>Yellow warning about DNS delegation</em><br/>
<img src="images/20.png" width="80%" alt="DNS Warning"/>
</p>

• **Action**  
   ‣ Acknowledge warning  
   ‣ Click "Next" to continue  
• **Settings**  
   ‣ No action required  
   ‣ Note warning text  
• **Explanation**  
   ‣ Normal for first DC  
• **Common Mistake**  
   ‣ Aborting setup unnecessarily  

---

### Step 21: Paths Configuration
<p align="center">
<em>Database/log file/SYSVOL paths screen</em><br/>
<img src="images/21.png" width="80%" alt="AD Paths"/>
</p>

• **Action**  
   ‣ Review default paths  
   ‣ Modify if needed  
• **Settings**  
   ‣ Default locations recommended  
   ‣ Ensure sufficient space  
• **Explanation**  
   ‣ AD database storage  
• **Common Mistake**  
   ‣ Putting on system drive  

---

### Step 22: Prerequisites Check
<p align="center">
<em>Green success checkmark screen</em><br/>
<img src="images/22.png" width="80%" alt="Prerequisites"/>
</p>

• **Action**  
   ‣ Review all checks  
   ‣ Resolve any failures  
• **Settings**  
   ‣ All items should pass  
   ‣ Note warnings if any  
• **Explanation**  
   ‣ Final verification  
• **Common Mistake**  
   ‣ Ignoring failed checks  

---

---

### Step 23: Installation Confirmation
<p align="center">
<em>Final review screen before AD installation</em><br/>
<img src="images/23.png" width="80%" alt="Install Confirmation"/>
</p>

• **Action**  
   ‣ Review configuration  
   ‣ Export settings (optional)  
• **Settings**  
   ‣ Verify domain name  
   ‣ Check paths  
• **Explanation**  
   ‣ Last chance to cancel  
• **Common Mistake**  
   ‣ Not backing up settings  

---

### Step 24: AD Installation Progress
<p align="center">
<em>Progress bar during AD installation</em><br/>
<img src="images/24.png" width="80%" alt="AD Install Progress"/>
</p>

• **Action**  
   ‣ Wait for completion  
   ‣ Don't interrupt process  
• **Settings**  
   ‣ Automatic reboots expected  
   ‣ 10-30 minute duration  
• **Explanation**  
   ‣ Critical configuration phase  
• **Common Mistake**  
   ‣ Force-restarting server  

---

### Step 25: Post-Installation Reboot
<p align="center">
<em>Server login screen after promotion</em><br/>
<img src="images/25.png" width="80%" alt="Post-Install Reboot"/>
</p>

• **Action**  
   ‣ Log in with domain admin  
   ‣ Verify DNS records  
• **Settings**  
   ‣ DOMAIN\Administrator  
   ‣ Check _msdcs zone  
• **Explanation**  
   ‣ Successful DC promotion  
• **Common Mistake**  
   ‣ Using local admin account  

---

### Step 26: AD Administrative Tools
<p align="center">
<em>Start menu showing AD management tools</em><br/>
<img src="images/26.png" width="80%" alt="AD Tools"/>
</p>

• **Action**  
   ‣ Open "Active Directory Users and Computers"  
   ‣ Explore default containers  
• **Settings**  
   ‣ Check Builtin/Users containers  
   ‣ Verify Domain Controllers OU  
• **Explanation**  
   ‣ Primary AD management console  
• **Common Mistake**  
   ‣ Modifying default containers  

---

### Step 27: Create Organizational Units
<p align="center">
<em>OU creation dialog in ADUC</em><br/>
<img src="images/27.png" width="80%" alt="Create OUs"/>
</p>

• **Action**  
   ‣ Right-click domain > New > OU  
   ‣ Create logical structure  
• **Settings**  
   ‣ Example: "Employees"  
   ‣ Enable protection  
• **Explanation**  
   ‣ Organizational hierarchy  
• **Common Mistake**  
   ‣ Overly complex OU design  

---

### Step 28: Create User Accounts
<p align="center">
<em>New user dialog in ADUC</em><br/>
<img src="images/28.png" width="80%" alt="Create Users"/>
</p>

• **Action**  
   ‣ Right-click OU > New > User  
   ‣ Fill mandatory fields  
• **Settings**  
   ‣ UserPrincipalName format  
   ‣ Complex password  
• **Explanation**  
   ‣ Basic AD object creation  
• **Common Mistake**  
   ‣ Weak password policies  

---

### Step 29: PowerShell User Creation
<p align="center">
<em>PowerShell window with New-ADUser command</em><br/>
<img src="images/29.png" width="80%" alt="PS User Creation"/>
</p>

• **Action**  
   ‣ Open PowerShell as Admin  
   ‣ Run New-ADUser cmdlet  
• **Settings**  
   ‣ Import ActiveDirectory module  
   ‣ Use -Path parameter for OU  
• **Explanation**  
   ‣ Bulk account creation  
• **Common Mistake**  
   ‣ Missing required parameters  

---

### Step 30: Group Policy Management
<p align="center">
<em>GPMC showing Default Domain Policy</em><br/>
<img src="images/30.png" width="80%" alt="GPMC"/>
</p>

• **Action**  
   ‣ Open Group Policy Management  
   ‣ Edit Default Domain Policy  
• **Settings**  
   ‣ Password/Account policies  
   ‣ Security settings  
• **Explanation**  
   ‣ Central policy enforcement  
• **Common Mistake**  
   ‣ Over-modifying default GPOs  

---

### Step 31: Join Client to Domain
<p align="center">
<em>Windows 10 System Properties dialog</em><br/>
<img src="images/31.png" width="80%" alt="Join Domain"/>
</p>

• **Action**  
   ‣ Change client computer name  
   ‣ Click "Domain" option  
• **Settings**  
   ‣ Enter full domain name  
   ‣ Provide domain admin creds  
• **Explanation**  
   ‣ Tests domain functionality  
• **Common Mistake**  
   ‣ Incorrect DNS settings  

---

### Step 32: Verify Domain Login
<p align="center">
<em>Windows 10 login screen with domain dropdown</em><br/>
<img src="images/32.png" width="80%" alt="Domain Login"/>
</p>

• **Action**  
   ‣ Select domain in dropdown  
   ‣ Log in with test user  
• **Settings**  
   ‣ DOMAIN\username format  
   ‣ Check mapped drives  
• **Explanation**  
   ‣ Validates AD authentication  
• **Common Mistake**  
   ‣ Forgetting to switch from local login  
