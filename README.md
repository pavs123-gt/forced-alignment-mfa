# forced-alignment-mfa
Forced Alignment Using Montreal Forced Aligner(MFA)
# Forced Alignment using Montreal Forced Aligner (MFA)

A complete pipeline for aligning speech audio with text transcripts using **Montreal Forced Aligner (MFA)**.  
The system takes `.wav` audio files and their transcript files, performs forced alignment, and generates **TextGrid files** with word and phoneme-level timestamps.  
These TextGrid files can be opened and analyzed in **Praat** for visualization.

---

## 📌 Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Setup & Installation](#setup--installation)
- [Dataset Format](#dataset-format)
- [Usage – Running Alignment](#usage--running-alignment)
- [Inspecting Output](#inspecting-output)
- [Key Observations](#key-observations)
- [Tools Used](#tools-used)
- [Author](#author)

---

## ✅ Features

- Aligns audio with transcripts at **word and phoneme** level
- Generates **TextGrid** output compatible with Praat
- Works with built-in MFA dictionary (english_us_arpa)
- Can be extended to custom dictionaries or acoustic models
- Simple folder-based input, no coding required for basic use

---
## 📂 Project Structure

```
forced-alignment-mfa/
│
├── wav/                 # Input audio (.wav)
│   └── audio1.wav
│   └── audio2.wav
│
├── transcripts/         # Text transcripts (.txt)
│   └── audio1.txt
│   └── audio2.txt
│
├── output/              # Generated TextGrid alignment files
│   └── audio1.TextGrid
│   └── audio2.TextGrid
│
├── README.md            # This guide
└── scripts/             # (optional) helper scripts
```
## ✅ Features

- Performs word-level and phoneme-level forced alignment
- Works with Montreal Forced Aligner (MFA)
- Generates TextGrid files compatible with Praat
- Simple folder-based dataset structure
- Can use built-in or custom pronunciation dictionaries
## ⚙️ Setup & Installation

### 1. Download and install MFA
```bash
wget https://github.com/MontrealCorpusTools/Montreal-Forced-Aligner/releases/download/v2.2.17/mfa_linux_x86_64.zip
unzip mfa_linux_x86_64.zip
cd mfa








