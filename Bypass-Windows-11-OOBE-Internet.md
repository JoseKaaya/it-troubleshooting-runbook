# How to Bypass Internet Requirement During Windows 11 Setup (OOBE)

During a clean installation of Windows 11, the Out-of-Box Experience (OOBE) setup screen enforces an active internet connection to proceed past the "Let's connect you to a network" step. If no Ethernet or Wi-Fi network is available (or missing network drivers), setup cannot proceed normally.

This runbook outlines the steps to bypass this enforcement using the built-in \OOBE\\BYPASSNRO\ command to create a local user account.

---

## Prerequisites
* Booted into the Windows 11 initial setup screen (Out-of-Box Experience / OOBE).
* A physical keyboard connected to the device.

---

## Step-by-Step Procedure

### 1. Reach the Network Selection Screen
Proceed through the initial setup language, keyboard layout, and region selection until you arrive at the screen titled **"Let's connect you to a network"**.

*Verification:* The "Next" button on screen will be grayed out if no active network connection is detected.

### 2. Open the Command Prompt
On your keyboard, press the key combination:
\\\cmd
Shift + F10
\\\
*(Note: On some laptop keyboards, you may need to press \Shift + Fn + F10\)*.

*Verification:* A black Command Prompt (\cmd.exe\) window opens on top of the setup interface with the prompt \C:\\Windows\\System32>\.

### 3. Execute the Bypass Command
In the Command Prompt window, type the following command exactly as shown and press **Enter**:

\\\cmd
oobe\\bypassnro
\\\

*Verification:* The computer will immediately initiate a soft reboot and restart the OOBE setup process.

---

## Post-Reboot Execution

### 4. Navigate Setup Again
Select your region and keyboard layout once more until you arrive back at the **"Let's connect you to a network"** screen.

### 5. Select Local Account Option
Look at the bottom right corner of the network screen. You will now see a new option:
* Click **"I don't have internet"**.

*Verification:* The setup screen advances to a secondary prompt.

### 6. Confirm Limited Setup
On the next screen, click **"Continue with limited setup"**.

*Verification:* The interface shifts to the local user account creation wizard ("Who's going to use this PC?").

### 7. Create Local User Account
1. Enter your preferred local username and click **Next**.
2. Enter a password (or leave it blank for no password) and click **Next**.
3. Set your 3 security questions if a password was entered.
4. Accept or customize your Privacy Settings.
5. Click **Accept** on the final screen.

---

## Outcome
Windows finishes setting up your desktop environment without requiring a Microsoft account or active internet connection. Driver updates and internet-dependent services can be configured later once connectivity is restored.
