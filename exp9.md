# Experiment No. 9 — Use Process Explorer to Identify Suspicious Processes

## Aim

To use **Process Explorer** to examine running processes in a Windows system and identify potentially suspicious processes by analyzing process information, executable paths, digital signatures, resource usage, and network activity.


## Description

**Process Explorer** is a Windows system-monitoring tool developed by Microsoft Sysinternals. It provides detailed information about running processes and their relationships.

It can be used by security and forensic investigators to examine:

* Running processes
* Process IDs (PID)
* Parent-child process relationships
* CPU and memory usage
* Executable file paths
* Command-line arguments
* Company and description information
* Digital signatures
* Network activity
* VirusTotal detection information

A combination of these indicators can help identify processes that require further investigation.

---

## Requirements

* Windows operating system
* Internet connection
* Microsoft Sysinternals Process Explorer
* Administrator privileges

---

## Tool Used

**Process Explorer**

Official Microsoft Sysinternals page:

https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer

---

# Procedure

## Step 1 — Download Process Explorer

1. Open a web browser.
2. Visit the official Microsoft Sysinternals Process Explorer page.
3. Download the Process Explorer ZIP file.
4. Extract the downloaded ZIP file.

The extracted folder contains executables such as:

```text
procexp.exe
procexp64.exe
procexp64a.exe
```

For a 64-bit Windows system, `procexp64.exe` can be used.

<img width="1917" height="1030" alt="Screenshot 2026-09-22 113541" src="https://github.com/user-attachments/assets/8df9659f-50d4-474e-848f-527466c67ef4" />


## Step 2 — Run Process Explorer

1. Open the extracted Process Explorer folder.
2. Right-click `procexp64.exe`.
3. Select **Run as administrator**.
4. Click **Yes** when Windows displays the User Account Control prompt.

The Process Explorer main window displays the currently running processes.



## Step 3 — Examine the Process Tree

The main window displays processes in a hierarchical tree structure.

The process tree shows:

* Parent processes
* Child processes
* Process names
* Process IDs
* CPU usage
* Memory usage

The process hierarchy can help investigators understand how a process was started.

Example:

```text
services.exe
 ├── svchost.exe
 ├── svchost.exe
 └── svchost.exe
```

---

## Step 4 — Select a Process for Investigation

A process can be selected for detailed analysis.

For the practical demonstration, a Windows process such as:

```text
svchost.exe
```

can be examined.

**Important:** A process should not be considered malicious simply because its name is unfamiliar or because it uses system resources.

---

## Step 5 — Check Process Properties

1. Right-click the selected process.
2. Select **Properties**.
3. Open the **Image** tab.

Important information includes:

* Process name
* Process ID
* Executable path
* Command line
* Company name
* Description
* CPU usage
* Memory usage
<img width="1915" height="1015" alt="Screenshot 2026-09-22 115455" src="https://github.com/user-attachments/assets/2c9738e8-a7e9-4de8-9613-2f91ae28f62f" />



## Step 6 — Verify the Executable Path

The executable path should be examined carefully.

For example, a legitimate Windows system executable may be located under:

```text
C:\Windows\System32\
```

A process with a misleading name running from an unexpected location such as a temporary or user-download directory may require additional investigation.

The location alone is not sufficient to classify a process as malware.

---

## Step 7 — Check the Digital Signature

The executable's digital signature can be checked to determine whether it has been signed by its claimed publisher.

Process Explorer can also verify image signatures through its options.

A valid Microsoft signature can provide evidence that the executable was published by Microsoft, although a valid signature by itself does not guarantee that the process is harmless.

<img width="1917" height="1012" alt="Screenshot 2026-09-22 115523" src="https://github.com/user-attachments/assets/45adf80e-d2ab-46c4-9e43-3b6cba6701f5" />


## Step 8 — Check CPU and Memory Usage

The CPU and memory columns were observed in Process Explorer.

Processes consuming unusually high resources should be investigated in context.

The following information can be recorded:
<img width="1917" height="1020" alt="Screenshot 2026-09-22 121131" src="https://github.com/user-attachments/assets/0d3fdd60-27da-4e83-be21-3d2cb4754ae3" />


---

## Step 9 — Check Network Activity

Process Explorer can provide information about network activity associated with a process.

The TCP/IP information can be examined where available.

Important information includes:

* Local address
* Local port
* Remote address
* Remote port

Unexpected network connections may be investigated further.

<img width="1915" height="1020" alt="Screenshot 2026-09-22 121522" src="https://github.com/user-attachments/assets/29d354cf-c31f-47b7-b28a-6c9de7a13afe" />




## Step 10 — Check VirusTotal Information

Process Explorer can integrate with VirusTotal.

The VirusTotal information can be used as an additional indicator when investigating an executable.

A result such as:
<img width="1910" height="1022" alt="Screenshot 2026-09-22 120836" src="https://github.com/user-attachments/assets/859a47d4-a3c3-476e-a9f8-553b27dfabd7" />

```text
0/70
```

means that no detections were reported by the engines represented in that result at that time.

VirusTotal results should be treated as supporting evidence rather than absolute proof that a file is safe or malicious.

---

## Step 12 — Process Termination

Process Explorer provides options such as:

* Kill Process
* Suspend Process

However, processes should **not** be terminated simply because they appear unfamiliar.

Terminating important Windows processes can cause system instability or data loss.

For this experiment, process termination was not performed on critical Windows processes.

If a process is confirmed to be malicious, appropriate evidence should first be preserved and the system should be handled according to the organization's incident-response or forensic procedure.



# Result

Process Explorer was successfully used to monitor and analyze Windows processes. Various process attributes such as executable location, process hierarchy, digital signatures, resource usage, and network activity were examined to identify indicators of potentially suspicious behavior.





