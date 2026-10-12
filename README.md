# EU_OUKITEL_WP5_Pro_V15_stock_zip
oukitel_wp5pro_eea_v15_20210918
write able with tsm-tool pro
can also be use for rooting OUKITEL WP5 Pro EU ver. oukitel_wp5pro_eea_v15_20210918

download here since the files too bige for my github page

https://drive.google.com/drive/folders/1_uOPVxfhcvwQrw3NbvMnj0JIfnu_5G78?usp=sharing
link will be valid at 10 pm mountain standard time GTM 10/11/2026





Here is the complete, step-by-step walkthrough to flash your universal stock backup onto the target Oukitel WP5 Pro. This process will completely wipe custom software, remove root, and restore the device to 100% factory state without damaging the target phone's unique IMEI info.
## 📋 Prerequisites

* Ensure the target phone is charged to at least 50%.
* Use a high-quality USB data cable.
* Make sure TSM-TOOL PRO (or Pro Edition) is open and your MediaTek drivers are working as they did during the backup.
* Ensure your universal backup files (scatter.txt, boot.img, system.img, vendor.img, vbmeta.img, etc.) are organized in a single folder on your PC.

------------------------------
## Step 1: Load the Universal Backup into TSM Tool

   1. Launch TSM-TOOL PRO and select the MediaTek (MTK) module tab.
   2. Look for the Flashing / Write Firmware workspace.
   3. Click on the folder icon next to Scatter File or Load Firmware.
   4. Browse to your universal backup folder, select your generated scatter text file (usually named something like MT6761_Android_scatter.txt or similar depending on the chipset), and click Open.
   5. TSM Tool will automatically scan the folder and checkmark the corresponding image files (boot, system, vendor, etc.) in the partition grid.

## Step 2: Double-Check Partition Exclusions (Safety Check)
Before clicking anything else, look closely at the list of checked boxes in the partition grid. To ensure you don't corrupt the target phone's network capabilities:

* Make sure nvram, nvdata, nvcfg, protect, and proinfo are UNCHECKED / EMPTY in the flashing queue. (Since you omitted them during backup, they should either not appear or be blank).
* This ensures the target phone keeps its own unique physical IMEI and calibration settings.

## Step 3: Set the Flashing Mode to "Download Only"

   1. Locate the drop-down menu in TSM Tool that determines the flashing method.
   2. Set it strictly to Download Only (sometimes labeled as Write Firmware or Flash Checked).
   3. ⚠️ WARNING: Absolutely NEVER select "Format All + Download" or "Firmware Upgrade". Choosing these modes will wipe the target device's motherboard raw, permanently deleting its original IMEI and bricking the cellular radio.

## Step 4: Initiate the Flash Connection

   1. Click the Flash, Write, or Start button in TSM Tool. The software status bar will shift to "Waiting for device..." or "Searching for MTK Port...".
   2. Turn off the target Oukitel WP5 Pro completely. Wait roughly 10 seconds for the hardware to cycle down.
   3. Press and hold both the Volume Up (+) and Volume Down (-) keys at the exact same time. Do not press the Power button.
   4. While holding both volume keys, plug the USB cable into the target phone.
   5. Watch the TSM Tool interface. The moment the status bar changes color (usually red or purple) and begins displaying text like "BROM Connection Achieved", release both volume buttons immediately.

## Step 5: Wait for Completion and Reboot

   1. TSM Tool will begin flashing the partitions sequentially (preloader ➡️ boot ➡️ vbmeta ➡️ system ➡️ vendor). This takes a few minutes as large system images move over the connection.
   2. Ensure the USB cable remains undisturbed during this window.
   3. Once finished, TSM Tool will display a green success notification or read out "Flash Operation Completed successfully".
   4. Unplug the USB cable from the phone.
   5. Press and hold the Power Button for about 10 seconds until the Oukitel logo appears.

Note: The very first boot after a clean stock flash takes significantly longer (around 3 to 7 minutes) because Android is rebuilding its system cache. Once it boots up, you will be greeted by the original factory setup wizard.
Did the tool successfully establish the handshake connection and pass the preloader check on the target phone, or are you running into any partition mismatch errors? Let me know if you run into any blocks!

