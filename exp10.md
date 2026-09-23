# Experiment No. 10 — Malware Analysis Using Ghidra

## Aim

To use Ghidra to disassemble and analyze an executable file and identify its functions, strings, API calls, cross-references, control flow, file operations, and behavioral indicators.

## Tools Used

- Ghidra
- Java JDK 21+
- GCC / MinGW
- Windows
- Command Prompt

## Safety Note

A self-created benign executable was used for this experiment instead of real malware. The sample does not contain malicious functionality and was created only for demonstrating static analysis using Ghidra.

---

# Step 2 — Create the Sample Directory

Open Command Prompt and run:

    mkdir C:\Users\moham\Ghidra_Sample
    cd C:\Users\moham\Ghidra_Sample

---

# Step 3 — Create the C Source File

Create a file named:

    malware_lab.c

<img width="920" height="815" alt="Screenshot 2026-09-23 093353" src="https://github.com/user-attachments/assets/70be2495-b46f-4b07-b98a-c06166b68bf8" />


# Step 4 — Verify GCC

Run:

    gcc --version

GCC should display its installed version.

Example:

    gcc (MinGW-W64 x86_64-ucrt-posix-seh, built by Brecht Sanders, r8) 13.2.0

---

# Step 5 — Compile the Program

Run:

    gcc malware_lab.c -o malware_lab.exe

Then verify the generated files:

    dir

Expected files:

    malware_lab.c
    malware_lab.exe

---

# Step 6 — Verify the Sample

The executable is a benign laboratory sample.

The program contains:

    main()
    file_operation()
    suspicious_function()

The program creates:

    analysis_test.txt

The file contains:

    Ghidra malware analysis laboratory

---

# Step 7 — Open Ghidra

Launch Ghidra.

Select:

    File → New Project

Choose:

    Non-Shared Project

Project location:

    C:\Users\moham\Ex9_Ghidra_Malware_Analysis
<img width="1091" height="651" alt="Screenshot 2026-09-23 081411" src="https://github.com/user-attachments/assets/8bc4baf4-9b59-45dd-90bb-c842512b93f8" />


# Step 8 — Import the Executable

In Ghidra select:

    File → Import File

Select:

    C:\Users\moham\Ghidra_Sample\malware_lab.exe

Click Import.

Open the imported program in CodeBrowser.

When Ghidra asks whether to perform analysis:

    Select Yes
<img width="1917" height="1022" alt="Screenshot 2026-09-23 083051" src="https://github.com/user-attachments/assets/2a47954f-f10e-4037-8532-d5a031641486" />


# Step 9 — Analyze main()

Open:

    Symbol Tree → Functions → main
<img width="1917" height="1020" alt="Screenshot 2026-09-23 083245" src="https://github.com/user-attachments/assets/f3150da1-428f-4621-a8f4-8abefecbf5da" />

Double-click main.


### Observation

The main() function controls the execution of the program and calls the other functions.

---

# Step 10 — Analyze file_operation()

Open:

    Symbol Tree → Functions → file_operation

Double-click file_operation.


The function opens analysis_test.txt in write mode, writes data to it, and closes the file.

### Observation

The file_operation() function performs a simple file creation and write operation.

---

# Step 11 — String Analysis

Open:

    Window → Defined Strings


The reference should lead to the code where the string is used.



# Step 13 — Analyze Imports / APIs

Open:

    Symbol Tree → Imports

Look for functions such as:

    fopen()
    fprintf()
    fclose()
    printf()

### Observation

API analysis helped identify the file and console operations performed by the executable.

---

# Step 14 — Cross-Reference Analysis

Open:

    main()

### Observation

Cross-reference analysis was used to understand the relationships between functions.

---

# Step 15 — Function Graph Analysis

Open:

    Window → Function Graph

The Function Graph displays the control flow of the selected function.

It shows:

- Function entry
- Instructions
- Conditional branches
- Function calls
- Return paths

### Observation

The Function Graph provided a visual representation of the program's control flow.

---

# Step 16 — Analyze suspicious_function()

Go to:

    Symbol Tree → Functions → suspicious_function

# Step 17 — Behavioral Analysis

## File Activity

The program uses:

    fopen()
    fprintf()
    fclose()

and creates/writes:

    analysis_test.txt

<img width="826" height="916" alt="Screenshot 2026-09-23 085957" src="https://github.com/user-attachments/assets/814a6fcb-72fa-4a6b-bd80-d812516ba397" />
<img width="1251" height="938" alt="Screenshot 2026-09-23 085809" src="https://github.com/user-attachments/assets/b76e9419-c7ef-4ec3-8486-447355fddc4d" />
<img width="1917" height="440" alt="Screenshot 2026-09-23 085152" src="https://github.com/user-attachments/assets/07a462dc-a7d4-4052-85a9-320c835fb150" />
<img width="1917" height="1017" alt="Screenshot 2026-09-23 084808" src="https://github.com/user-attachments/assets/594dc935-ae89-4185-a3b1-39fa1c531ad7" />
<img width="1915" height="1000" alt="Screenshot 2026-09-23 084210" src="https://github.com/user-attachments/assets/396f609d-7149-46a4-92e2-62cd06949ac4" />


# Step 18 — Display File Content

The program creates:

    analysis_test.txt

Display its contents:

    cd C:\Users\moham\Ghidra_Sample
    type analysis_test.txt

Expected output:

    Ghidra malware analysis laboratory

---

# Step 19 — Calculate File Hashes

Hashing provides a unique fingerprint for a file.

## MD5

    certutil -hashfile malware_lab.exe MD5

## SHA-1

    certutil -hashfile malware_lab.exe SHA1

## SHA-256

    certutil -hashfile malware_lab.exe SHA256


# Step 21 — Hash Results

<img width="926" height="116" alt="Screenshot 2026-09-23 090807" src="https://github.com/user-attachments/assets/98441be1-1996-49f1-85dc-6e56952ab8dc" />
<img width="852" height="112" alt="Screenshot 2026-09-23 090703" src="https://github.com/user-attachments/assets/7e1e7f81-a4d9-4eff-a78b-2abc3c25c3fd" />

# Step 24 — Result

The executable was successfully imported into Ghidra and analyzed using static-analysis techniques.

The following Ghidra features were used:

- CodeBrowser
- Disassembly
- Decompiler
- Symbol Tree
- Functions
- Defined Strings
- Imports
- Cross-References
- Function Graph

The executable's functions, strings, APIs, file operations, and control flow were identified and analyzed.

The file hashes were calculated to provide unique identifiers for the analyzed files.

