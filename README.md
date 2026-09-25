# 🔐 Digital Forensics Experiments

A collection of **10 Digital Forensics and Cybersecurity laboratory experiments** covering evidence acquisition, file recovery, network analysis, email investigation, disk forensics, Android extraction, steganalysis, process investigation, and malware analysis.

## 📚 Experiments

| No. | Experiment                                                   | File                     |
| --- | ------------------------------------------------------------ | ------------------------ |
| 1   | Evidence Acquisition Using AccessData FTK Imager             | [`exp1.md`](exp1.md)     |
| 2   | Recover Deleted or Damaged Files Using TestDisk              | [`exp2.md`](exp2.md)     |
| 3   | Password Capturing Using Wireshark                           | [`exp3.md`](exp3.md)     |
| 4   | Email Header Analysis and Email Spoofing Detection Using MHA | [`exp4.md`](exp4.md)     |
| 5   | Digital Forensics Using Autopsy                              | [`exp5.md`](exp5.md)     |
| 6   | Sleuth Kit Digital Evidence Analysis                         | [`exp6.md`](exp6.md)     |
| 7   | Android Data Extraction Using AFLogical OSE                  | [`exp7.md`](exp7.md)     |
| 8   | Detect Hidden Data in Images Using StegExpose                | [`exp8.md`](exp8.md)     |
| 9   | Identify Suspicious Processes Using Process Explorer         | [`exp9.md`](exp9.md)     |
| 10  | Malware Analysis Using Ghidra                                | [`exp_10.md`](exp_10.md) |

---

## 🛠️ Tools Covered

The experiments demonstrate the use of several digital forensics and security tools:

* **AccessData FTK Imager**
* **TestDisk**
* **Wireshark**
* **Mail Header Analyzer (MHA)**
* **Autopsy**
* **The Sleuth Kit (TSK)**
* **AFLogical OSE**
* **Android Debug Bridge (ADB)**
* **StegExpose**
* **Microsoft Sysinternals Process Explorer**
* **Ghidra**
* **Java**
* **GCC / MinGW**
* **Perl**
* **Windows Command Prompt**

---

## 📁 Repository Structure

```text
df_exps/
│
├── README.md
├── exp1.md
├── exp2.md
├── exp3.md
├── exp4.md
├── exp5.md
├── exp6.md
├── exp7.md
├── exp8.md
├── exp9.md
└── exp_10.md
```

Each Markdown file contains the corresponding experiment, including its objective, requirements, procedure, commands, explanations, and practical evidence/screenshots where applicable.

---

## 🎯 Topics Covered

### 1. Digital Evidence Acquisition

Using **FTK Imager** to acquire and work with forensic evidence.

### 2. File Recovery

Using **TestDisk** to recover deleted or damaged files.

### 3. Network Forensics

Using **Wireshark** to capture and analyze network traffic in an authorized laboratory environment.

### 4. Email Forensics

Analyzing email headers and authentication information to identify indicators of possible spoofing.

### 5. Computer Forensics

Using **Autopsy** to create forensic cases, examine evidence, analyze artifacts, and generate reports.

### 6. Disk Image Analysis

Using **The Sleuth Kit** for partition analysis, filesystem analysis, deleted-file identification, metadata analysis, recovery, and timeline generation.

### 7. Android Forensics

Using **AFLogical OSE** and **ADB** for logical extraction of supported data from an Android device.

### 8. Steganalysis

Using **StegExpose** to detect possible hidden information in PNG images and analyze Fusion scores.

### 9. Process Investigation

Using **Process Explorer** to examine Windows processes, process relationships, executable paths, digital signatures, and other indicators.

### 10. Malware Analysis

Using **Ghidra** for static analysis of a self-created benign executable, including functions, strings, API calls, cross-references, and control flow.

---

## ⚙️ General Requirements

Requirements vary by experiment, but may include:

* Windows / Linux / macOS
* Java JDK
* Wireshark
* FTK Imager
* TestDisk
* Autopsy
* The Sleuth Kit
* AFLogical OSE
* Android Debug Bridge
* StegExpose
* Process Explorer
* Ghidra
* GCC / MinGW
* Perl

Refer to the individual experiment file for the complete requirements and installation instructions.

---

## ⚠️ Safety and Ethical Use

These experiments are intended for **educational and authorized laboratory environments**.

* Only analyze devices, networks, accounts, files, and digital evidence that you are authorized to examine.
* Do not capture or inspect other people's credentials or private communications.
* Use intentionally vulnerable applications and test data for security demonstrations.
* Preserve the integrity of forensic evidence when performing investigations.
* Do not use the techniques demonstrated in these experiments for unauthorized access or surveillance.
* The malware-analysis experiment uses a **self-created benign executable** for educational purposes rather than real malware.

---

## 📖 How to Use This Repository

1. Clone or download this repository.

```bash
git clone <your-repository-url>
```

2. Open the repository folder.

3. Select the experiment you want to study.

4. Open the corresponding `.md` file.

5. Follow the requirements and procedure provided in that experiment.

Example:

```text
exp1.md  → Experiment 1
exp2.md  → Experiment 2
exp3.md  → Experiment 3
...
exp_10.md → Experiment 10
```

---

## 🎓 Purpose

This repository is intended as a **Digital Forensics laboratory record and learning resource**. It documents practical experiments involving digital evidence acquisition, recovery, analysis, network forensics, mobile forensics, steganalysis, process investigation, and reverse engineering.

---

## 👨‍💻 Author

**rahamxx**

---

## 📜 Disclaimer

This repository is created for **educational and cybersecurity laboratory purposes only**.

The author does not encourage unauthorized access, credential interception, privacy violations, malware deployment, or any other illegal activity. Always obtain appropriate authorization before performing security or forensic testing.
