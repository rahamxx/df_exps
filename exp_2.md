# EXPERIMENT NO. 2 — RECOVER DELETED OR DAMAGED FILES USING TESTDISK

## AIM

To recover a deleted partition and restore the files stored on it using TestDisk.

## DESCRIPTION

TestDisk is an open-source data recovery utility used to recover lost partitions and restore access to data from deleted or damaged partitions.

## REQUIREMENTS

- Windows 10/11
- TestDisk 7.2
- Windows Disk Management
- Command Prompt
- File Explorer
- 5 GB Virtual Hard Disk (VHD)

## SAFETY PRECAUTION

This experiment was performed using a 5 GB Virtual Hard Disk (VHD) instead of the real Windows disk.

Disk identification:

Disk 0 = Real Windows SSD (~512 GB) — DO NOT MODIFY
Disk 1 = 5 GB VHD — Used for the experiment

VHD path:

C:\TestDisk_Experiment.vhd


10. Assign a drive letter.

The VHD was successfully created and prepared for the recovery experiment.


###  — DELETE THE TEST PARTITION

1. Open Disk Management.
2. Locate Disk 1, which is the 5 GB VHD.
3. Right-click the Test_recovery partition.
4. Select Delete Volume.
5. Confirm the deletion.

After deletion, the VHD appeared as:

5.00 GB Unallocated

### STEP  — START TESTDISK

Open Command Prompt and navigate to the TestDisk directory:

cd "C:\Users\moham\Downloads\testdisk-7.2-20250721T144550Z-1-001 (1)\testdisk-7.2"

Start TestDisk:

testdisk_win.exe

### STEP — CREATE TESTDISK LOG

At the TestDisk startup screen, select:

[ Create ]
<img width="1092" height="642" alt="Screenshot 2026-09-23 202822" src="https://github.com/user-attachments/assets/1337570a-3153-40e8-a8ac-07d0660bb09f" />

Press Enter to create the TestDisk log.

### STEP 7 — SELECT THE VHD

TestDisk displayed the available disks.

The following disk was selected:

Disk \\.\PhysicalDrive1 - 5368 MB / 5120 MiB - Msft Virtual Disk
<img width="1097" height="638" alt="Screenshot 2026-09-23 203944" src="https://github.com/user-attachments/assets/35aa9e7c-205d-4090-ace9-22d0b1f0f211" />


### STEP 8 — SELECT PARTITION TABLE TYPE

The VHD was initialized using MBR.

Therefore, the following partition table type was selected:

[Intel] Intel/PC partition
<img width="951" height="1012" alt="Screenshot 2026-09-23 204218" src="https://github.com/user-attachments/assets/5e60069c-c977-40e9-8349-6b9926c455cc" />

Press Enter.

### STEP 9 — ANALYSE THE DISK

From the TestDisk main menu, select:

[ Analyse ]

Press Enter.

TestDisk displayed the current partition structure.

Because the partition had been deleted, it was no longer visible to Windows.

<img width="947" height="1013" alt="Screenshot 2026-09-23 204257" src="https://github.com/user-attachments/assets/c9e00a6b-141a-4839-8a37-88b14886dc6b" />



### STEP  — WRITE THE RECOVERED PARTITION TABLE

Press Enter to continue.
<img width="943" height="1012" alt="Screenshot 2026-09-23 205348" src="https://github.com/user-attachments/assets/d71f0340-8f93-4a9d-9166-6bcf7f9d4161" />

Select:

[ Write ]

Press Enter.

TestDisk displayed:

Write partition table, confirm ? (Y/N)
<img width="956" height="1021" alt="Screenshot 2026-09-23 210205" src="https://github.com/user-attachments/assets/b5ccdaca-a314-42f3-8785-c6d746f018e5" />


### STEP  — VERIFY THE RECOVERED PARTITION

After reattaching the VHD, Disk Management displayed:
<img width="933" height="737" alt="Screenshot 2026-09-23 210657" src="https://github.com/user-attachments/assets/ac2c59d2-8648-4984-90c0-19673a825cc6" />


### STEP 18 — VERIFY THE RECOVERED FILES

Open:

D:\Evidence

The following files were successfully recovered:

document1.txt
document2.txt
important.txt
sample_data.txt

The files were opened and their contents were verified.
<img width="1915" height="1013" alt="Screenshot 2026-09-23 210724" src="https://github.com/user-attachments/assets/4c441a2f-e935-4855-be80-ed7586808c45" />



## RESULT

The deleted NTFS partition was successfully recovered using TestDisk.
