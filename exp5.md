# 🔍 Digital Forensics Using Autopsy

## 📌 Experiment No. 5

### 🎯 Aim

To use **Autopsy** to create a forensic case, import digital evidence, analyze artifacts, and generate a forensic report.

---

## 📖 Description

**Autopsy** is an open-source digital forensics platform used for analyzing and extracting data from digital devices.

It helps investigators examine digital evidence such as:

* 💾 Disk Images
* 📁 Files and Directories
* 🌐 Web History
* 📧 Email Records
* 🗂️ File System Metadata
* 🔑 Keywords
* 🔐 File Hashes

---

# 🛠️ Requirements

* Autopsy
* Digital Evidence File
* Disk Image File

### Sample Evidence Files

```text
4Dell Latitude CPi.E01
4Dell Latitude CPi.E02
```

---

# ⚙️ 1. Installation

### Step 1: Download Autopsy

Download and install **Autopsy** on your computer.

Autopsy supports different operating systems, including:

* Windows
* Linux
* macOS

### Step 2: Install the Application

Follow the installation instructions for your operating system and complete the setup.

---

# 📂 2. Starting a New Case

### Step 1: Open Autopsy

Launch the **Autopsy** application.

### Step 2: Create a New Case

Click:
<img width="1702" height="903" alt="Screenshot 2026-09-04 150904" src="https://github.com/user-attachments/assets/ba4fb6f7-b714-4b59-88af-5e007de2ffa6" />

```text
New Case
```

### Step 3: Enter Case Details

Enter the following information:

* Case Name
* Case Number
* Case Location
* Examiner Name

Click **Next** to continue.
<img width="1692" height="906" alt="Screenshot 2026-09-04 151008" src="https://github.com/user-attachments/assets/b28eaccf-dcf6-48d9-97df-67077290f710" />

---

# 💾 3. Adding a Data Source

After creating the case, add the digital evidence.

## Select the Type of Data Source

Autopsy allows different types of data sources:

* 💿 Disk Images
* 📁 Directories
* 📄 Logical Files
* 💻 Local Disks

---

## Select the Evidence File

Browse and select the evidence file you want to analyze.

Supported examples include:

```text
.E01
.dd
.raw
```

---

# ⚙️ Configure Ingest Modules

Autopsy provides different modules for analyzing digital evidence.

Examples include:

* 🔍 File Type Identification
* 🔑 Keyword Search
* 🔐 Hash Lookup

Enable or disable the modules based on the requirements of the investigation.

Click **Next** to start the analysis.
<img width="1697" height="887" alt="Screenshot 2026-09-04 151507" src="https://github.com/user-attachments/assets/5cf4a346-3011-4dca-8f91-d9ea9b714e27" />

---

# 📊 4. Initial Analysis and Overview

## Ingest Progress

As Autopsy processes the data source, the progress can be monitored from the application interface.
<img width="1698" height="900" alt="Screenshot 2026-09-04 153007" src="https://github.com/user-attachments/assets/e3a97033-d6b5-4aee-82cc-bf47c9bb1e01" />

---

## Explore Artifacts

Autopsy automatically categorizes important findings such as:

* 🌐 Web Artifacts
* 🗂️ File System Metadata
* 💬 Communication Records
<img width="1707" height="882" alt="Screenshot 2026-09-04 152753" src="https://github.com/user-attachments/assets/d98d1ff3-692f-45e9-8435-2b568991d410" />

---

## 🌳 Use the Tree Viewer

The left-side panel provides a tree structure for exploring evidence.

Examples include:

```text
📁 File System
🌐 Web History
📧 Email
📂 Other Artifacts
```
<img width="1711" height="903" alt="Screenshot 2026-09-04 153814" src="https://github.com/user-attachments/assets/e31afe85-1038-4ba6-83cc-224c9cb5fb99" />

---

# 🔎 5. Detailed Analysis

## 🔑 Keyword Search

Use the **Keyword Search** module to search for specific words or phrases.

You can:

* Use pre-configured keyword lists.
* Add custom keywords.
* Search for important evidence.

---

## 📁 File Analysis

Navigate through files and folders using:

* File Types
* File System

You can:

* Open files
* View files
* Export files


---

## 🔐 Hash Analysis

Hash analysis compares file hashes with known databases.

This helps identify:

* Known good files
* Known bad files
* Suspicious files

---

# 📄 6. Reporting

## Generate a Report

After completing the analysis:

1. Click **Generate Report**.
2. Select the report format.
3. Choose the information to include.

Supported report formats may include:

* HTML
* CSV
* Excel
<img width="1195" height="741" alt="Screenshot 2026-09-04 154106" src="https://github.com/user-attachments/assets/22056e65-0176-4f80-9aa1-2e1a34ba6e75" />

---

## 📤 Export Findings

Export important files or artifacts for:

* Further investigation
* Documentation
* Evidence reporting
<img width="1898" height="977" alt="Screenshot 2026-09-04 154143" src="https://github.com/user-attachments/assets/4374b1c3-2931-47ce-9f0b-b51c52b4316e" />

---

## ✅ Final Review

Before completing the case:

* Review the report.
* Ensure all important findings are included.
* Save or print the report.

---

# 🔒 7. Case Closure

## Close the Case

Once the investigation is completed, close the case in Autopsy.

---

## 🗄️ Archiving

Ensure that:

* Evidence is properly stored.
* Reports are archived.
* Investigation data is preserved according to organizational policies.

---

# 🚀 8. Advanced Features

## ⚙️ Custom Ingest Modules

Autopsy allows custom modules to be added when additional analysis tools are required.

This helps investigators perform specialized forensic analysis.

---

## 👥 Collaboration

Autopsy can be configured for multi-user cases.

This allows multiple investigators to work together during a forensic investigation.

---

# 🧪 Workflow

```text
Start Autopsy
      │
      ▼
Create New Case
      │
      ▼
Enter Case Details
      │
      ▼
Add Data Source
      │
      ▼
Configure Ingest Modules
      │
      ▼
Start Analysis
      │
      ▼
Analyze Artifacts
      │
      ▼
Keyword / File / Timeline / Hash Analysis
      │
      ▼
Generate Report
      │
      ▼
Review Findings
      │
      ▼
Close & Archive Case
```

---

# 🛡️ Key Features of Autopsy

| Feature                 | Description                                        |
| ----------------------- | -------------------------------------------------- |
| 📁 Data Source Analysis | Analyze disk images, files, directories, and disks |
| 🔍 Keyword Search       | Search for important keywords                      |
| 🌐 Web Artifacts        | Analyze web-related evidence                       |
| 📧 Email Analysis       | Examine email-related records                      |
| ⏱️ Timeline             | Analyze events based on timestamps                 |
| 🔐 Hash Lookup          | Identify known good or bad files                   |
| 📊 Reporting            | Generate forensic investigation reports            |

---

# 👨‍💻 Tool Used

* **Autopsy**

---

# 📋 Result

A forensic case was successfully created using **Autopsy**, and digital evidence was imported for analysis.

The evidence was processed using ingest modules, and artifacts such as files, metadata, web history, communication records, keywords, timelines, and hashes could be examined. A forensic report can then be generated and the case properly archived.

---

# 🏁 Conclusion

Autopsy provides an organized platform for conducting digital forensic investigations. It allows investigators to create cases, import evidence, analyze artifacts, perform keyword and hash analysis, examine timelines, and generate investigation reports.
