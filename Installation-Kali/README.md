# 🐉 Installing Kali Linux in VirtualBox (Guest VM)

This guide walks through setting up **Kali Linux** inside **VirtualBox** as a guest VM. Running Kali in a VM provides isolation, easy interaction with other VMs and your network, and snapshot support for safe rollbacks.

---

## 1. Create a new virtual machine
1. Open **VirtualBox** and click **New**.
2. Name the VM (e.g., `kali-linux-2025.3-vbox-amd64`).
3. Set:
   - **Type**: Linux
   - **Version**: Debian (64‑bit).

![New VM wizard](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-01.png)

---

## 2. Configure memory and CPU
- **Memory size**: 2048 MB (2 GB) minimum; increase if your host has spare RAM.
- **Processors**: Set to at least 2.
- Enable **PAE/NX** under System → Processor.

![Memory size](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-02.png)
![Hard disk](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-03.png)

---

## 3. Create a virtual hard disk
1. Choose **Create a virtual hard disk now**.
2. **Hard disk file type**: VDI (VirtualBox Disk Image).
3. **Storage on physical hard disk**: Dynamically allocated.
4. **File location and size**: 80 GB recommended.

![Disk file type](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-04.png)
![Storage type](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-05.png)
![Disk size](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-06.png)

---

## 4. Adjust VM settings
- General → Advanced:
  - **Shared Clipboard**: Bidirectional
  - **Drag’n’Drop**: Bidirectional
- System → Motherboard:
  - **Boot Order**: Hard Disk first, Optical second
- System → Processor:
  - **Processor(s)**: 2
  - **Enable PAE/NX**: On
- Display → Screen:
  - **Video Memory**: 128 MB
  - **Accelerated 3D Graphics**: Disabled.

![General → Advanced](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-07.png)
![System → Motherboard](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-08.png)
![System → Processor](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-09.png)
![Display → Screen](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-10.png)
![Final settings view](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-11.png)

---

## 5. Mount the Kali ISO and start
1. Click **Start** on the VM.
2. In the startup disk prompt, click the disk icon to open **Optical Disk Selector**.
3. Click **Add**, select your Kali ISO, then **Choose**, and **Start**.

![Startup disk prompt](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-12.png)
![Optical Disk Selector](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-13.png)
![ISO added](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-14.png)

---

## 6. Install Kali Linux
Proceed with the standard installer. During setup, Kali detects it’s inside a VM and automatically installs guest additions (e.g., `virtualbox-guest-x11`) for a better experience.

![Kali installer](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-15.png)

---

## 7. Expanding storage (optional)
1. Power off the VM.
2. Go to **File → Tools → Virtual Media Manager**.
3. Select the VM’s `.vdi`, adjust its size, and click **Apply**.
4. Boot Kali and use `gparted` (or similar) to extend the partition and filesystem.

![Virtual Media Manager](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-16.png)
![Adjust size](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-17.png)
![Apply size](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/vb-18.png)

---

## ✅ Summary
You now have a fully functional **Kali Linux VM inside VirtualBox** with guest additions enabled—ideal for penetration testing, infosec experiments, and AI‑driven workflows.

---

> Source: Kali Linux Documentation — “Kali inside VirtualBox (Guest VM)”
