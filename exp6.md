# 🔍 Sleuth Kit Digital Evidence Analysis

## 📌 Overview

This project demonstrates the use of **The Sleuth Kit (TSK)** to analyze a forensic disk image and perform basic digital forensic investigation.

The investigation covers:

- Partition analysis
- Filesystem analysis
- File and directory analysis
- Deleted file identification
- Metadata analysis
- Deleted file recovery
- Forensic timeline generation
- Evidence preservation

---

## 🎯 Objective

To analyze a digital forensic disk image using **The Sleuth Kit** and extract useful forensic information while preserving the integrity of the original evidence.

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| `mmls` | Partition analysis |
| `fsstat` | Filesystem analysis |
| `fls` | File and directory listing |
| `fls -d` | Deleted file identification |
| `istat` | File metadata analysis |
| `icat` | Deleted file recovery |
| `mactime` | Forensic timeline generation |
| `Perl` | Execute `mactime.pl` on Windows |
| `certutil` | SHA-256 hashing |

---

## 💾 Evidence Image

The forensic image consisted of image files:

4Dell Latitude CPi.E01
output screenshots
<img width="1836" height="907" alt="Screenshot 2026-09-18 162527" src="https://github.com/user-attachments/assets/853d006d-f46f-40bd-8bf2-18454a8de0d4" />
<img width="912" height="265" alt="Screenshot 2026-09-18 163316" src="https://github.com/user-attachments/assets/b6d390d2-e046-488b-b256-c2d82b3f2d9e" />

<img width="915" height="555" alt="Screenshot 2026-09-18 165947" src="https://github.com/user-attachments/assets/157ed95f-f1bc-4ad0-a344-279374259c40" />
<img width="1917" height="1018" alt="Screenshot 2026-09-18 165717" src="https://github.com/user-attachments/assets/11fe9571-316c-406d-86f9-5bd0c118229c" />
<img width="1846" height="987" alt="Screenshot 2026-09-18 165424" src="https://github.com/user-attachments/assets/09ddf944-9a63-447d-935f-b7c287eab2f3" />
<img width="922" height="755" alt="Screenshot 2026-09-18 165244" src="https://github.com/user-attachments/assets/86b3466e-222b-45c5-937a-dbc3c92c8cf9" />
<img width="1766" height="830" alt="Screenshot 2026-09-18 165037" src="https://github.com/user-attachments/assets/f94f8b89-295b-47ef-8b9b-acb039ad7b97" />
<img width="1917" height="996" alt="Screenshot 2026-09-18 164151" src="https://github.com/user-attachments/assets/28dafd17-d37a-4ba3-874a-d366fcf86169" />
<img width="1725" height="948" alt="Screenshot 2026-09-18 164016" src="https://github.com/user-attachments/assets/2a742ffd-2fda-4008-a949-f4b7adea8803" />
<img width="920" height="642" alt="Screenshot 2026-09-18 203830" src="https://github.com/user-attachments/assets/a2bf3e08-3018-4c04-b4e6-b136a4200037" />
<img width="885" height="467" alt="Screenshot 2026-09-18 173807" src="https://github.com/user-attachments/assets/3550e09f-e0ee-4a81-bb50-e34a4a9bf68a" />
<img width="1915" height="1022" alt="Screenshot 2026-09-18 172947" src="https://github.com/user-attachments/assets/b5a89102-43c1-4cd7-9fbc-16300bd08605" />
<img width="920" height="300" alt="Screenshot 2026-09-18 170407" src="https://github.com/user-attachments/assets/c4ffac98-2bce-420d-839e-d87bef3419fa" />
<img width="933" height="291" alt="Screenshot 2026-09-18 170149" src="https://github.com/user-attachments/assets/98a853f2-f74a-4919-b085-c7eb04140514" />
