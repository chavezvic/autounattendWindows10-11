# autounattendWindows10-11
# Generate autounattend installation for Windows 10/11


This repository provides instructions for creating an unattended installation file (`autounattend.xml`) for Windows 10/11 using the [Schneegans Unattended Generator](https://schneegans.de/windows/unattend-generator/).

### Steps to Generate autounattend.xml

#### Step 1: Open the Website
Go to [Schneegans Unattended Generator](https://schneegans.de/windows/unattend-generator/).

#### Step 2: Configure Region and Language Settings
- **Display Language**: Select the desired language.
- **Locale**: Choose the locale for formatting dates, times, and currency.
- **Keyboard Layout**: Select the desired keyboard layout.
- **Home Location**: Choose the country or region.

#### Step 3: Select Processor Architecture
Choose the processor architecture(s) you need (e.g., Intel/AMD 64-bit).

#### Step 4: Setup Settings
- **Bypass Windows 11 Requirements Check**: Check this box if needed.
- **Allow Windows 11 Installation Without Internet**: Check this if no internet access during setup.

#### Step 5: Configure Computer Name
Choose whether to let Windows generate a random computer name or specify a custom name.

#### Step 6: Set Time Zone
Set the time zone explicitly or let Windows determine it.

#### Step 7: Partitioning and Formatting
- **Partition the disk interactively**: Manual partitioning during setup.
- **Let Windows Setup wipe, partition, and format**: Automated process.

##### Partition Layout
- **GPT (GUID Partition Table)**: Use for UEFI-based systems.
- **MBR (Master Boot Record)**: Use for legacy BIOS systems.

##### Windows RE (Recovery Environment) Installation
- **Install on recovery partition**
- **Install on Windows partition**
- **Remove Windows RE**

##### Custom Diskpart Script
See the [custom_diskpart_script.txt](resources/custom_diskpart_script.txt) file in this repository for an example script.

#### Step 8: Choose Windows Edition
Select the edition of Windows you want to install.

#### Step 9: Create User Accounts
- **Account Name**: Username for the local account.
- **Password**: Password for the local account.
- **Group**: Group membership (e.g., Administrators, Users).

#### Step 10: Set Password and Account Policies
Configure password expiration settings and account lockout policies.

#### Step 11: Optimization Settings
- **Disable Windows Defender**
- **Disable System Protection/System Restore**
- **Enable long paths**
- **Enable Remote Desktop services (RDP)**
- **Harden ACLs**
- **Allow execution of PowerShell script files**
- **Do not update Last Access Time stamp**
- **Do not reboot with users signed in**
- **Turn off system sounds**
- **Disable app suggestions**
- **Disable widgets**
- **Prevent device encryption**
- **Audit process creation events**

#### Step 12: Virtual Machine Support
Choose to install VirtualBox Guest Additions, VMware Tools, or VirtIO Guest Tools.

#### Step 13: Wi-Fi Setup
Configure Wi-Fi settings or skip Wi-Fi configuration.

#### Step 14: Express Settings
Choose to disable or enable all express settings or configure them interactively.

#### Step 15: Remove Bloatware
Select pre-installed apps to remove.

#### Step 16: Run Custom Scripts
Configure custom scripts to run at various stages of the setup process.

#### Step 17: Configure WDAC Policy
Configure Windows Defender Application Control (WDAC) policy.

#### Step 18: Generate the autounattend.xml File
Click the button to generate the autounattend.xml file and download it.

#### Step 19: Use the autounattend.xml File
Place the `autounattend.xml` file on the root of your installation media (USB drive). Boot from the installation media to start the unattended Windows setup.

## Resources
- [Custom Diskpart Script](resources/custom_diskpart_script.txt)
- [Autounattend Template](resources/autounattend_template.xml)

Reference
This guide is based on instructions from schneegans.de.

Contact
For any questions or issues, please contact Christoph Schneegans.
