---
permalink: /kali-linux-on-windows
---

# How to install Kali Linux on Windows
So most people know what Kali Linux is.
Its a command console thingy for Linux computers and is great for hacking.

This is a tutorial to get it on Windows

---

### Step 1: (Very annoying) Enable Visualization in BIOS
On your computer theres this secret little thingy with settings where you cant type, or use mouse, and 
its to enable some dumb ass settings like virtualization. Its called *BIOS*.

Open it by restarting your computer and rapidly press either *Esc, F10, F9,* or something else depending 
on the brand of computer. 

Another thing thats dumb about this, is the fact that where you enable virtualization also varies by 
brand of computers WITH THE SAME OS.

**Links to directions for each brand:**
- [For HP brand](https://support.hp.com/us-en/document/ish_5637142-5637191-16)
- [For Dell brand](https://www.dell.com/support/kbdoc/en-us/000195978/how-to-enable-or-disable-hardware-virtualization-on-dell-systems)

---

### Step 2: Download WSL2 Linux Kernal Package
Download the [WSL2 Linux Kernal Package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

---

### Step 3: Run some long commands
Open Powershell as an administrator.
Run this command to enable the Windows Linux Subsystem.
`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`

Run this command to enable the Virtual Machine Platform.
`dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`

Set the default WSL version
`wsl --set-default-version 2`

---

### Step 4: Install the Kali Linux Distribution for WSL
Get Kali Linux in the Microsoft Store app or [here](https://www.microsoft.com/store/apps/9PKR34TNCV07)