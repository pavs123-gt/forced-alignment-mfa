# Forced Alignment using Montreal Forced Aligner (MFA)

A complete pipeline for aligning speech audio with text transcripts using **Montreal Forced Aligner (MFA)**.  
The system takes `.wav` audio files and their transcript files, performs forced alignment, and generates **TextGrid files**  
with word and phoneme-level timestamps.  
These TextGrid files can be opened and analyzed in **Praat** for visualization.

---

## ✅ Table of Contents
- [Setup & Installation](#setup--installation)
- [Dataset Format](#dataset-format)
- [Running Forced Alignment](#running-forced-alignment)
- [Inspecting Output in Praat](#inspecting-output-in-praat)
- [Final Alignment Output](#final-alignment-output)
- [Custom Dictionary Output](#custom-dictionary-output)
- [Final Report](#final-report)
- [Tools Used](#tools-used)
- [Author](#author)

---

##  Setup & Installation
```bash
conda create -n mfa python=3.8 -y
conda activate mfa
pip install montreal-forced-aligner
mfa version

### 2. Verify Installation

Run the following command to confirm MFA is installed correctly:

```bash
./mfa_align --help
```
## Dataset Format
This project contains:
1. Wav/                → speech audio files
2. Transcripts/         → matching transcript text files
3. output_custom/       → TextGrid alignment results
4. custom.dict          → pronunciation dictionary

## Features
- Uses Montreal Forced Aligner for word & phoneme alignment
- Generates TextGrid files
- Visualizable in Praat
- Custom dictionary support
- Final alignment output (.txt) included in final_alignment.zip

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
output/

```

## Inspecting Output in Praat

1. Open Praat
2. Go to: File → Open → Read from file
3. Select the `.wav` and `.TextGrid` file
4. View the waveform with phoneme and word boundaries


### Sample Alignment Output

After running the Montreal Forced Aligner, TextGrid files are generated.  
The screenshot below shows how phoneme and word boundaries are aligned in Praat:

![Praat Output](https://github.com/pavs123-gt/forced-alignment-mfa/blob/main/praat.png?raw=true)

## Final Alignment Output:
```
Complete alignment results are provided in:
✅ final_alignment_output.zip

This ZIP contains:
- Words time-aligned
- Phones time-aligned
- Individual alignment text files for all audio

```
##  Custom Dictionary Output:
```
The `output_custom.zip` contains:
- custom.dict
- alignment_analysis.csv
- TextGrid files generated using my custom lexicon
```


## Tools Used
```
- Montreal Forced Aligner (MFA)
- Praat
- Linux Terminal
```

### 📄 Final Report
```
👉 [Download Report.pdf](https://github.com/pavs123-gt/forced-alignment-mfa/raw/main/Report.pdf)

(The preview may not load on GitHub, but the file downloads and opens correctly.)
```

## Author
````
Linguberi Pavani
```
# Forced Alignment using Montreal Forced Aligner (MFA)

This project performs forced alignment on speech audio (.wav) and transcripts using Montreal Forced Aligner (MFA). It generates timestamped TextGrid files with word and phoneme boundaries, which can be visualized in Praat.

## Table of Contents
- Setup & Installation
- Dataset Format
- Features
- Running Forced Alignment
- Inspecting Output in Praat
- Sample Alignment Output
- Final Alignment Output
- Custom Dictionary Output
- Final Report
- Tools Used
- Author

## Setup & Installation
conda create -n mfa python=3.8 -y
conda activate mfa
pip install montreal-forced-aligner
mfa version

To verify installation:
mfa_align --help

## Dataset Format
Wav/                → speech audio files (.wav)
Transcripts/        → transcript files (.txt)
output_custom/      → TextGrid alignment results
custom.dict         → custom dictionary

## Features
- Performs word and phoneme alignment on speech audio
- Generates TextGrid files for every sample
- TextGrid files can be opened in Praat to see word and phone boundaries
- Supports custom dictionary alignment
- Creates readable alignment output text files in final_alignment_output.zip

## Running Forced Alignment
1. Download dictionary:
mfa download dictionary english_us_arpa

2. Align audio and transcript:
mfa align Wav/ Transcripts/ english_us_arpa output/

Aligned TextGrid files will appear inside:
output/

## Inspecting Output in Praat
1. Open Praat
2. File → Open → Read from File
3. Select .wav and .TextGrid
4. View waveform with word and phoneme timestamps

## Sample Alignment Output
Praat visualization screenshot:
(Your praat.png image link)

## Final Alignment Output
Complete alignment results are provided in:
final_alignment_output.zip

This ZIP contains:
- Word-level timestamps
- Phone-level timestamps
- One alignment text file per audio

## Custom Dictionary Output
output_custom.zip contains:
- custom.dict
- alignment_analysis.csv
- TextGrid generated using custom dictionary

## Final Report
Download Report.pdf from repository:
(Your Repo Link)

## Tools Used
Montreal Forced Aligner (MFA)
Praat
Linux Terminal
Python

## Author
Linguberi Pavani



