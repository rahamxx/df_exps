# EXPERIMENT NO. 7 — USE AFLOGICAL OSE TO EXTRACT DATA FROM AN ANDROID DEVICE

## AIM

To perform logical extraction of data from an Android device using AFLogical OSE and Android Debug Bridge (ADB).

## DESCRIPTION

AFLogical OSE (Open Source Edition) is an Android forensic acquisition tool designed to perform logical extraction of selected data from Android devices. It can be used to collect information such as contacts, SMS messages, MMS messages, and call logs without performing a full physical file-system acquisition.

## REQUIREMENTS

- Android device
- Windows/Linux/macOS computer
- USB cable
- AFLogical OSE
- Java
- Android Debug Bridge (ADB)
- USB drivers, if required
- USB Debugging enabled on the Android device

## STEP 1 — PREPARE THE ENVIRONMENT

### 1. Download AFLogical OSE

Download AFLogical OSE from its official project repository:

https://github.com/den4uk/AFLogical-OSE

Extract the downloaded files to a suitable directory.

### 2. Install Java

Install Java if it is not already installed.

Verify Java using:

java -version
<img width="937" height="147" alt="Screenshot 2026-09-23 232158" src="https://github.com/user-attachments/assets/4523bf4f-7989-4ee7-8da8-eb013637a91a" />

### 3. Install Android Debug Bridge

Download Android SDK Platform Tools from:

https://developer.android.com/tools/releases/platform-tools

Extract the Platform Tools package.

Verify ADB using:

adb version



## STEP 2 — CONNECT THE ANDROID DEVICE

Connect the Android device to the computer using a USB cable.

Open Command Prompt or Terminal and execute:

adb devices
<img width="937" height="418" alt="Screenshot 2026-09-23 234914" src="https://github.com/user-attachments/assets/495a3bfc-9066-47cf-b224-8d183f89a6da" />


## STEP 3 — INSTALL AFLOGICAL OSE

Navigate to the directory containing the AFLogical OSE APK.

Install the APK using:

adb install aflogical.apk

If the installation is successful, AFLogical OSE will be installed on the Android device.
<img width="1285" height="125" alt="Screenshot 2026-09-24 002319" src="https://github.com/user-attachments/assets/f4565709-7511-44ff-a451-0da3c671352e" />

## STEP 4 — LAUNCH AFLOGICAL OSE

Open the AFLogical application on the Android device.

Select the available data categories that need to be extracted.

Typical categories may include:

- Contacts
- Call Logs
- SMS
- MMS
- Other supported logical data

Start the extraction process from the application.

The application collects the selected logical data and stores the extracted information on the device.

## STEP 5 — LOCATE THE EXTRACTED DATA

AFLogical OSE may store the extracted results in a directory such as:

/sdcard/aflogical/

The extracted information may be stored in CSV or other supported output files.

## STEP 6 — TRANSFER THE EXTRACTED DATA TO THE COMPUTER

Create a destination directory on the computer for the forensic output.

Use ADB to copy the extracted data:

adb pull /sdcard/aflogical <destination_directory>
<img width="1268" height="75" alt="Screenshot 2026-09-24 002307" src="https://github.com/user-attachments/assets/2368d1fd-7c8a-4ce3-ace2-0af9c4309db1" />


## STEP 8 — ANALYZE THE EXTRACTED DATA

Open the extracted CSV files using an appropriate application such as:

- Microsoft Excel
- LibreOffice Calc
- Google Sheets
- Text editor

Review the extracted records and document relevant forensic findings.
<img width="1262" height="640" alt="Screenshot 2026-09-24 002404" src="https://github.com/user-attachments/assets/6b9824d0-eae2-4c14-8ad5-878786387f10" />
<img width="1245" height="602" alt="Screenshot 2026-09-24 002344" src="https://github.com/user-attachments/assets/82fa1b89-16b7-4b69-995d-ad58cba9d6ea" />

Important information should be recorded without modifying the original evidence files.

## STEP 9 — DOCUMENT THE RESULTS

Record the following information:

- Device identification information
- Date and time of acquisition
- ADB connection status
- AFLogical OSE version, if available
- Data categories selected
- Extracted files
- Number of records, where applicable
- Relevant observations
- Evidence storage location

## STEP 10 — CLEAN UP

After completing the forensic acquisition and verifying the evidence, the AFLogical application can be removed if required.

Use:

adb uninstall com.viaforensics.android.aflogical

Disconnect the Android device safely from the computer.


## RESULT

AFLogical OSE was used to perform a logical extraction of supported data from an Android device. The extracted data was transferred to the computer using ADB and verified for further forensic analysis.
