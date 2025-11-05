# forced-alignment-mfa
Forced Alignment Using Montreal Forced Aligner(MFA)
# Forced Alignment using Montreal Forced Aligner (MFA)

A complete pipeline for aligning speech audio with text transcripts using **Montreal Forced Aligner (MFA)**.  
The system takes `.wav` audio files and their transcript files, performs forced alignment, and generates **TextGrid files** with word and phoneme-level timestamps.  
These TextGrid files can be opened and analyzed in **Praat** for visualization.

---

## Table of Contents
- [Setup & Installation](#setup--installation)
- [Dataset Format](#dataset-format)
- [Running Forced Alignment](#running-forced-alignment)
- [Inspecting Output in Praat](#inspecting-output-in-praat)
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
├── wav/                ✅ audio + transcript pairs
│   ├── audio1.wav
│   ├── audio1.txt
│   ├── audio2.wav
│   ├── audio2.txt
│   └── ...
│
├── output/             ✅ final results
│   ├── audio1.TextGrid
│   └── results.csv
│
└── README.md

```


## Setup & Installation

### 1. Download the Montreal Forced Aligner

Download the official MFA release and extract it:

```bash
wget https://github.com/MontrealCorpusTools/Montreal-Forced-Aligner/releases/download/v2.2.17/mfa_linux_x86_64.zip
unzip mfa_linux_x86_64.zip
cd mfa
```

---

### 2. Verify Installation

Run the following command to confirm MFA is installed correctly:

```bash
./mfa_align --help
```

If a help/help menu appears, MFA is successfully installed ✅

## Dataset Format

Your project directory must contain:

```
wav/          → audio files (.wav)
transcripts/  → text files (.txt)
output/       → alignment results (.TextGrid)
```

Example:

```
wav/audio1.wav
transcripts/audio1.txt
```

⚠ Each transcript must match the audio filename.
## Running Forced Alignment

### 1. Download Dictionary

```bash
mfa download dictionary english_us_arpa
```

### 2. Run Alignment

```bash
mfa align wav/ transcripts/ english_us_arpa output/
```

After completion, alignment TextGrid files will appear inside:

```
output/
```
## Inspecting Output in Praat

1. Open Praat
2. Go to: File → Open → Read from file
3. Select the `.wav` and `.TextGrid` file
4. View the waveform with phoneme and word boundaries

### Sample Alignment Output

The following screenshot shows the word-level and phoneme-level alignment viewed in Praat:

![Praat Output]()

## Tools Used

- Montreal Forced Aligner (MFA)
- Praat
- Linux Terminal

## Author

Linguberi Pavani
