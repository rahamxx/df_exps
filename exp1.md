# 🔍 Evidence Acquisition Using AccessData FTK Imager

## 📌 Experiment No. 1

### 🎯 Aim

To acquire and analyze digital forensic evidence using **AccessData FTK Imager**.

---

## 📖 Description

**FTK (Forensic Toolkit)** is a computer forensics software product developed by AccessData. FTK Imager is capable of acquiring and analyzing computer forensic evidence.

The evidence acquired using FTK Imager can be divided into two main categories:

* 💾 **Volatile Memory Acquisition**
* 💿 **Non-Volatile Memory Acquisition (Hard Disk)**

---

# 🛠️ Methods of Using FTK Imager

There are two main methods for using FTK Imager during forensic acquisition.

## 1️⃣ Portable Version

FTK Imager can be stored on a:

* USB Pen Drive
* External HDD

It can be opened directly from the evidence machine.

This method is commonly used for **live data acquisition** when the evidence computer is switched on.

## 2️⃣ Investigator's Laptop

FTK Imager can also be installed on the investigator's laptop.

The source disk should be connected using a **write blocker**.

### 🔒 Write Blocker

A write blocker:

* Prevents modification of data on the evidence disk.
* Provides read-only access.
* Helps maintain the integrity of the original evidence.

---

# 🧠 Acquiring Volatile Memory

Volatile memory refers to the **RAM (Random Access Memory)** of a computer.

FTK Imager can collect the complete volatile memory of a system.

## Steps

### Step 1: Open FTK Imager

Open the **FTK Imager** application.

### Step 2: Capture Memory

Navigate to the **Capture Memory** option.

### Step 3: Select Additional Options

FTK Imager provides options to include:

* Pagefile
* AD1 File

---

## 📄 Pagefile

The **pagefile (`pagefile.sys`)** is used by Windows when the available physical RAM is insufficient.

It can contain valuable information and may be useful during forensic investigations.

Therefore, it is recommended to capture the pagefile during memory acquisition.

---

## 📦 AD1 File

**AD1** is an FTK Imager image file format.

The investigator can create an AD1 file for later forensic analysis.

---

## ▶️ Start Memory Acquisition

Click the **Capture Memory** button to start acquiring volatile memory.

After acquisition is completed, the destination folder will contain the acquired memory file.

```text
File Extension: .mem
```
<img width="1917" height="1011" alt="Screenshot 2026-08-08 203953" src="https://github.com/user-attachments/assets/f45870ac-a963-4226-a2bf-0bc11af9ca0d" />

---

# 💿 Acquiring Non-Volatile Memory (Disk Image)

FTK Imager can also be used to acquire disk images.

## Steps

### Step 1: Create Disk Image

Open FTK Imager and select:

```text
Create Disk Image
```

### Step 2: Select the Source

Choose the source that needs to be acquired.

FTK Imager can acquire:

* Physical Drives
* Logical Drives
* Image Files
* Folder Contents
* CDs/DVDs

---
<img width="1917" height="1015" alt="Screenshot 2026-08-08 204439" src="https://github.com/user-attachments/assets/ed48fc36-8c5b-4115-a7c6-22af41a354ca" />

# 💽 Collecting Physical Drives

To acquire a physical drive:

1. Select **Physical Drive**.
2. Select the drive that needs to be acquired.
3. Click **Finish**.
<img width="1917" height="987" alt="Screenshot 2026-08-08 204556" src="https://github.com/user-attachments/assets/17763691-3a28-4d98-b7a6-4d38081b8ce9" />

---

# 📂 Disk Image Formats

FTK Imager supports different forensic image formats.

## 🔹 Raw (dd)

The **Raw (dd)** format is commonly used by modern forensic analysis tools.

Features:

* Does not contain headers.
* Does not contain metadata.
* Does not contain magic values.
* Helps maintain spatial integrity.

---

## 🔹 SMART

The **SMART** format is designed for Linux file systems.

Features:

* Stores disk images as pure bitstreams.
* Supports optional compression.
* Contains a standard header.
* Includes sections containing data and comments.

---

## 🔹 E01

**E01** is a proprietary forensic image format developed by EnCase.

Features:

* Supports compression.
* Contains case information.
* Includes acquisition details.
* Contains an MD5 hash.
* Can store examiner information.
* Can include special notes.

---

## 🔹 AFF

**AFF (Advanced Forensic Format)** was developed to provide a forensic disk image format that does not lock users into a proprietary format.

The latest implementation mentioned is:

```text
AFF4
```
<img width="1917" height="1015" alt="Screenshot 2026-08-08 204650" src="https://github.com/user-attachments/assets/39b88599-e74a-4b95-bbbb-49d05b57e994" />

---

# 📝 Enter Case Details

Enter the required case information before creating the forensic image.

Example details may include:

* Case Number
* Evidence Number
* Examiner Name
* Notes
* Description

---
<img width="1915" height="1013" alt="Screenshot 2026-08-08 204757" src="https://github.com/user-attachments/assets/7611beac-bbb4-4764-a458-7cd441c1560c" />

# 📁 Select Image Destination

Select:

* Image destination folder
* Image file name
* Image fragment size

---

# 📦 Image Fragment Size

The **Image Fragment Size (MB)** option separates a large image into multiple files.

### To create multiple fragments:

Set the required fragment size.

### To create a single image file:

```text
Image Fragment Size = 0
```
<img width="505" height="390" alt="SS 2" src="https://github.com/user-attachments/assets/027e0baf-58a3-4950-afe5-8cc6319ae457" />

---

# 🔐 Verify Image Integrity

Select:

```text
Verify images after they are created
```

This option verifies the hash values after the image is created.

### Advantages

* Ensures evidence integrity.
* Verifies the acquired forensic image.
* Helps confirm that the evidence was acquired correctly.

> ⚠️ Note: Verification can increase the acquisition time, especially for large disk images.

---

# ▶️ Start Acquisition

Click:

```text
Start
```
<img width="470" height="355" alt="SS 9" src="https://github.com/user-attachments/assets/bdeee37f-a7ae-415b-aa89-173b9c698e4d" />

FTK Imager will begin acquiring the forensic evidence.

After the acquisition is completed:

* The forensic image will be created.
* A text file containing acquisition information will also be generated.
* Hash values can be checked to verify the integrity of the evidence.

---

# 🔒 Importance of Hash Verification

Hash verification is important in digital forensics because it helps confirm that the acquired evidence has not been modified.

```text
Original Evidence Hash
        │
        ▼
Forensic Image Acquisition
        │
        ▼
Generated Image Hash
        │
        ▼
Compare Hash Values
        │
        ▼
   ✅ Hash Values Match
```

---

# 🧪 Result

The digital evidence was successfully acquired using **AccessData FTK Imager**.

Both volatile memory and non-volatile disk evidence can be acquired using the tool. Hash verification helps ensure the integrity of the acquired forensic evidence.

---
<img width="1173" height="1341" alt="ChatGPT Image Aug 22, 2026, 05_54_21 PM" src="https://github.com/user-attachments/assets/c42bdacd-0623-4b59-ad95-2c3313bc3bf7" />

# 🛡️ Key Concepts

| Concept                 | Description                                              |
| ----------------------- | -------------------------------------------------------- |
| **FTK Imager**          | Tool used for forensic evidence acquisition and analysis |
| **Volatile Memory**     | Temporary memory such as RAM                             |
| **Non-Volatile Memory** | Permanent storage such as hard disks                     |
| **Write Blocker**       | Prevents modification of the evidence disk               |
| **Disk Image**          | A forensic copy of a storage device                      |
| **Hash Value**          | Used to verify data integrity                            |
| **Pagefile**            | Windows file that may contain valuable memory data       |

---

## 👨‍💻 Tools Used

* **AccessData FTK Imager**
* **Write Blocker**
* **Storage Device / Evidence Disk**

---

### ✅ Conclusion

FTK Imager is a useful digital forensic tool for acquiring volatile and non-volatile evidence. Proper acquisition procedures and hash verification help maintain the integrity of digital evidence.
