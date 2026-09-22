# Experiment No. 8 – Detect Hidden Data in Images Using StegExpose

## Aim

To detect hidden data in images using the StegExpose steganalysis tool.

---

## Objective

The objectives of this experiment are:

- To understand image steganography and steganalysis.
- To install and configure Java.
- To install and run StegExpose.
- To analyze PNG images for possible hidden data.
- To understand the Fusion score and detection threshold.
- To generate and analyze a CSV report.
- To test an image containing LSB-based hidden data.

---

## Requirements

### Software

- Windows Operating System
- Java JDK 17
- StegExpose
- Command Prompt (CMD)

### Input

PNG image files.

---

# 1. Introduction

Steganography is the technique of hiding secret information inside another file such as an image, audio file, video, or document.

Steganalysis is the process of detecting whether an image or other media may contain hidden information.

StegExpose is a steganalysis tool that can detect possible LSB-based steganography in lossless image formats such as PNG and BMP.

The tool calculates a Fusion score between 0 and 1.

### Detection Threshold

| Fusion Score | Interpretation |
|--------------|----------------|
| < 0.2 | Generally clean |
| 0.2 – 0.3 | Possible hidden data |
| > 0.3 | More likely to contain hidden data |

The default threshold used in this experiment is:0.2


<img width="946" height="1077" alt="Screenshot 2026-09-22 083547" src="https://github.com/user-attachments/assets/12d2ee37-be45-43e8-bdeb-a4bd31ea155f" />


<img width="1901" height="1015" alt="Screenshot 2026-09-22 090614" src="https://github.com/user-attachments/assets/9b6a6b26-5e52-4715-980e-60e3fcf47815" />
<img width="1832" height="270" alt="Screenshot 2026-09-22 090546" src="https://github.com/user-attachments/assets/91f764ce-c018-41fc-8cd1-aa3a0ec58d83" />
<img width="1917" height="1067" alt="Screenshot 2026-09-22 085428" src="https://github.com/user-attachments/assets/0690537f-d196-4e45-941b-8a6117723195" />
<img width="1890" height="322" alt="Screenshot 2026-09-22 091500" src="https://github.com/user-attachments/assets/ec1a4913-650a-4ceb-b409-3b28b5d160d9" />


<img width="1865" height="395" alt="Screenshot 2026-09-22 091526" src="https://github.com/user-attachments/assets/8e8c6bae-606f-4715-95d5-66e95378c275" />
<img width="1872" height="622" alt="Screenshot 2026-09-22 090643" src="https://github.com/user-attachments/assets/a3b364ce-83f7-4abf-aa3c-79ff60139c3f" />


