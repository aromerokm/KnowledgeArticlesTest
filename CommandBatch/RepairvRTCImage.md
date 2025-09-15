# Repair vRTC Image — Versions 2.4 and Later

Use the following procedure to repair the vRTC image if COMMANDbatch cannot connect to the vRTC. Use this procedure only if you are running eVM version 2.4 or later.

This problem may present itself in one of the following ways:

- The eVM software is running (as indicated by the green eVM icon `image.png` in the lower right corner of the Windows desktop), but the RTC Status indicator at the top of the COMMANDbatch screen is displayed in red.  
  ![eVM icon](image.png)  
  ![RTC Status indicator](image.png)
- Or, an eVM General Protection fault error occurs when the PC boots up.

## Procedure

To repair a vRTC Image for a version of eVM 2.4 or later:

1. Stop eVM by right-clicking on the eVM icon and selecting **Stop eVM**.
2. Right-click on the **CB Central** icon.
3. Select **Repair Tools > Repair vRTC Image**.  
   The vRTC setup window is displayed and shows the repair progress.  
   ![vRTC setup window](image.png)
4. When the repair is complete, select **Close** from the setup window.
5. Restart eVM by right-clicking the eVM icon and selecting **Restart eVM**.

---

# Repair vRTC Image — Versions Older Than 2.4

Use the following procedure to repair the vRTC image if COMMANDbatch cannot connect to the vRTC. Use this procedure only if you are running eVM version of eVM that is older than 2.4.

This problem may present itself in one of the following ways:

- The eVM software is running (as indicated by the green eVM icon `image.png` in the lower right corner of the Windows desktop), but the RTC Status indicator at the top of the COMMANDbatch screen is displayed in red.  
  ![eVM icon](image.png)  
  ![RTC Status indicator](image.png)
- Or, an eVM General Protection fault error occurs when the PC boots up.

## Procedure

To repair a vRTC image for versions of eVM that are older than 2.4:

1. Stop eVM by right-clicking on the eVM icon and selecting **Stop eVM**.  
   ![Stop eVM](image.png)
2. Insert the **vRTC Install/Recovery USB** device into the COMMANDbatch PC.
3. From the **vRTC Recovery Menu**, select **Repair vRTC Image**.  
   ![vRTC Recovery Menu](image.png)
4. When the repair is complete, select **Close** from the setup window.
5. Restart eVM.

> **Note:** Depending on the version of COMMANDbatch currently in use, you may be prompted to upgrade the RTC the next time COMMANDbatch is opened.

---

# What the Repair Buttons Do

## Repair vRTC Installation Button

When the **“Repair vRTC Installation”** button is clicked, the installer program performs the following actions:

1. Extracts the `eVM100.ini` file.
2. Extracts the `eVM100.msi` file.
3. Runs the `eVM100.msi` and installs files to `C:\Program Files (x86)\EVM`.
4. Extracts the eVM configuration file (`eVMvRTCconfig.ecf`).
5. Imports the configuration into the eVM software.
6. Installs all network adapters listed in the `vRTC_Installer.ini` file.
7. Renames the **TenAsys Virtual Ethernet Adapter** to **“CBControlNet”**.
8. Sets the **CBControlNet** IP address to `192.168.78.3` and the subnet to `255.255.255.0`.
9. Reboots the PC.

## Repair vRTC Image Button

When the **“Repair vRTC Image”** button is clicked, the installer program extracts a new `eVMvRTC.img` to the `C:\ProgramData\TenAsys\eVM` directory.
