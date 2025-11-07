# Forced Alignment using Montreal Forced Aligner (MFA)

A complete pipeline for aligning speech audio with text transcripts using **Montreal Forced Aligner (MFA)**.  
The system takes `.wav` audio files and their transcript files, performs forced alignment, and generates **TextGrid files**  
with word and phoneme-level timestamps.  
These TextGrid files can be opened and analyzed in **Praat** for visualization.

---
## ✅ Table of Contents
- [Setup & Installation](#setup--installation)
- [Dataset Format](#dataset-format)
- [Features](#features)
- [Running Forced Alignment](#running-forced-alignment)
- [Inspecting Output in Praat](#inspecting-output-in-praat)
- [Sample praat Output](#sample-alignment-output)
- [Final Alignment Output](#final-alignment-output)
- [Custom Dictionary Output](#custom-dictionary-output)
- [Final Report](#final-report)
- [Tools Used](#tools-used)
- [Author](#author)
---
##  Setup & Installation


##  Create and Activate Conda Environment
```bash
conda create -n mfa python=3.8 -y
conda activate mfa
```

## Install Montreal Forced Aligner
```bash
pip install montreal-forced-aligner
```
## Verfiy Installation
```bash
mfa version
mfa align --help
```
---
## Features
- Performs forced alignment on speech audio and transcripts
- Generates TextGrid files with word-level and phoneme-level timestamps
- TextGrid files can be visualized in Praat
- Supports custom pronunciation dictionaries (`custom.dict`)
- Produces readable alignment output (.txt) inside `final_alignment_output.zip`
- Works for multiple audio files automatically
---
##  Running Forced Alignment:
To perform forced alignment, we first download a pronunciation dictionary and then run the aligner on our audio and transcript folders.
##  Download dictionary
```bash
mfa download dictionary english_us_arpa
```
## Run Forced Alignment
```bash
mfa align wav/ transcripts/ english_us_arpa output/
```
---
##  Inspecting Output in Praat

Once alignment is complete, each audio file will have a matching `.TextGrid` file in the output folder.

You can visualize word and phoneme boundaries in **Praat** using these steps:

###  How to View Alignment in Praat
1. Open **Praat**
2. Go to **File → Open → Read from file**
3. Select both:
    the `.wav` audio file  
    the `.TextGrid` alignment file
4. Click **View & Edit**

Praat will display:
-  Waveform
-  Spectrogram
-  Word boundaries
-  Phoneme boundaries
-  Time-stamped alignment for each speech unit

This helps verify whether the alignment correctly matches the speech signal.

###  Sample Praat Visualization
The screenshot below shows aligned words and phonemes from my dataset:

![Praat Output](https://github.com/pavs123-gt/forced-alignment-mfa/blob/main/praat.png?raw=true)

---

##  Final Alignment Output

After processing all audio files, the system generates time-aligned transcripts.  
The complete alignment results are provided in:
 **final_alignment_output.zip**

This ZIP contains:
- Word-level timestamps
- Phoneme-level timestamps
- Individual `.txt` alignment files for every audio
- Easy-to-read format for report submission or evaluation
---

##  Custom Dictionary Output
The `output_custom.zip` contains:
- custom.dict
- alignment_analysis.csv
- TextGrid files generated using my custom lexicon

## 📄 Final Report

The project report explains the full workflow, methodology, errors, observations, and results.

📌 **Download the final report here:**  
👉 [Report.pdf](https://github.com/pavs123-gt/forced-alignment-mfa/raw/main/Report.pdf)

*If the preview does not load on GitHub, click “Download” to view the PDF.*

## 🔧 Tools Used
- Montreal Forced Aligner
- Praat
- Python

## 👩‍💻 Author

**Linguberi Pavani**  
B.Tech Student  
Speech Processing | Forced Alignment using MFA  
GitHub: https://github.com/pavs123-gt

