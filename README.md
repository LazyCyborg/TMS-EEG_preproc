# TMS-EEG Analysis Pipeline Setup

This repository contains a pipeline for analyzing TMS-EEG data using MNE-Python.

## Prerequisites

- Python 3.8 or higher
- FreeSurfer (for MRI processing)
- Git
- ~20GB free disk space for sample data and FreeSurfer processing

## Sample Data

The sample TMS-EEG data and preprocessed FreeSurfer MRI can be downloaded from:
[TMS-EEG Sample Data](https://drive.google.com/drive/folders/116Qc1Ko-Y8wgshy8g4YLTpxOdp1cgOQW?usp=drive_link)

Download the contents and extract them to the following structure:

TMS-EEG_preproc/
  data/                     # Place TMS1 folder here
  freesurfer_subjects/      # Place Freesurfer subject folder here

## Quick Start

```bash
# Clone the repository
git clone https://github.com/YourUsername/TMS-EEG_preproc.git
cd TMS-EEG_preproc

# Create and activate conda environment
conda create -n tms_eeg python=3.8
conda activate tms_eeg

# Install requirements
pip install -r requirements.txt
