# 🐉 Installing Kali Linux in VirtualBox (Guest VM)

This guide walks through setting up **Kali Linux** inside **VirtualBox** as a guest VM.  
Running Kali in a VM provides isolation from your host system, snapshot support, and easy interaction with other VMs or networked machines.

---

## 1. Create a New Virtual Machine
1. Open **VirtualBox** and click **New**.
2. Enter a name (e.g., `kali-linux-2025.3-vbox-amd64`).
3. Set:
   - **Type**: Linux  
   - **Version**: Debian (64‑bit)

![New VM Wizard](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/new-vm.png)

---

## 2. Configure Memory and CPU
- **Memory size**: Minimum 2 GB (2048 MB). Increase if your host has spare RAM.  
- **Processors**: Set to at least 2.  
- Enable **PAE/NX** under *System → Processor*.

![Memory Settings](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/memory.png)  
![CPU Settings](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/cpu.png)

---

## 3. Create a Virtual Hard Disk
1. Choose **Create a virtual hard disk now**.
2. Select **VDI (VirtualBox Disk Image)**.
3. Storage type: **Dynamically allocated**.
4. Size: **80 GB** recommended.

![Disk Settings](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/disk.png)

---

## 4. Adjust VM Settings
- **General → Advanced**:  
  - Shared Clipboard: *Bidirectional*  
  - Drag’n’Drop: *Bidirectional*
- **System → Motherboard**:  
  - Boot Order: Hard Disk first, Optical second  
- **Display → Screen**:  
  - Video Memory: 128 MB  
  - Disable *Accelerated 3D Graphics*

![General Settings](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/general.png)  
![Display Settings](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/display.png)

---

## 5. Mount Kali ISO
1. Click **Start** on the VM.  
2. When prompted for a startup disk, select your Kali ISO.  
3. Use the **Optical Disk Selector** → **Add** → choose ISO → **Open** → **Choose**.

![ISO Selector](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/iso.png)

---

## 6. Install Kali Linux
- Proceed with the standard Kali installation wizard.  
- The installer will detect VirtualBox and automatically install **guest additions** (e.g., `virtualbox-guest-x11`) for better integration.

![Kali Installer](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/installer.png)

---

## 7. Expanding Storage (Optional)
1. Power off the VM.  
2. Go to **File → Tools → Virtual Media Manager**.  
3. Select your VM’s `.vdi` file and adjust its size.  
4. Boot Kali and use `gparted` to extend the partition and filesystem.

![Virtual Media Manager](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/media-manager.png)

---

## ✅ Summary
You now have a fully functional **Kali Linux VM inside VirtualBox** with guest additions enabled.  
This setup provides a safe, isolated environment for penetration testing, infosec experiments, and AI‑driven workflows.

---

*Based on [Kali Linux Documentation](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/).*
