# Clean Installation Walkthrough: Windows 11

A step-by-step procedure for performing a clean OS deployment on a target machine using a bootable USB drive.

---

## Requirements
* Bootable USB drive (minimum 8GB, created via Media Creation Tool or Rufus).
* Target computer with storage device initialized.

---

## Setup Execution

### 1. Boot from Installation Media
1. Insert the bootable USB into the target machine.
2. Power on the PC and repeatedly tap your vendor's Boot Menu key (\F12\ for Dell, \F9\ for HP, \F12\ for Lenovo, \F8\ for Asus).
3. Select the USB flash drive from the boot list and press **Enter**.

*Verification:* The blue **Windows Setup** dialog box appears with Language, Time, and Keyboard options.

### 2. Initial Setup Selection
1. Select your preferred **Language to install**, **Time and currency format**, and **Keyboard method**.
2. Click **Next**.
3. Click **Install Now**.

*Verification:* The screen displays "Setup is starting".

### 3. Product Key & Edition Selection
1. Enter your 25-character product key, or click **"I don't have a product key"** to activate later.
2. Select your Windows Edition (e.g., *Windows 11 Pro*) and click **Next**.
3. Check **"I accept the Microsoft Software License Terms"** and click **Next**.

### 4. Select Installation Type
On the prompt "Which type of installation do you want?":
* Select **Custom: Install Windows only (advanced)**.

*Verification:* The partition management table ("Where do you want to install Windows?") appears.

### 5. Partition Management & Disk Formatting
*(Warning: The following step erases all existing data on target partitions)*

1. Identify the target disk drive (e.g., \Drive 0\).
2. Select each partition on the target drive and click **Delete** until only **Drive 0 Unallocated Space** remains.
3. Select **Drive 0 Unallocated Space** and click **Next**.

*Verification:* Setup creates necessary system partitions automatically and begins copying files (*Installing Windows* screen showing percentage progress).

### 6. Out-of-Box Experience (OOBE)
Once installation files copy and the system automatically reboots:
1. Select your **Region/Country** -> Click **Yes**.
2. Select your **Keyboard Layout** -> Click **Yes**.
3. Choose to add a second layout or click **Skip**.
4. Set computer name -> Click **Next**.
5. Connect to network (or follow the \OOBE\\BYPASSNRO\ runbook if no network is present).
6. Complete user account setup and privacy preference toggles.
7. Click **Accept** on the final screen.

---

## Outcome
The system completes initial desktop provisioning and logs into the Windows desktop environment.
