# TMS-EEG Analysis Pipeline Setup

This repository contains some code which is an attempt at analyzing TMS-EEG data using MNE-Python.

Note that it contains a modified version of the neurone_loader which is used to load the sample data provided in the link bellow

## Prerequisites

- Python 3.8 or higher
- FreeSurfer (for MRI processing)
- Git
- ~20GB free disk space for sample data and FreeSurfer processing

## Sample Data

The sample TMS-EEG data and preprocessed FreeSurfer MRI can be downloaded from:
[TMS-EEG Sample Data](https://drive.google.com/drive/folders/116Qc1Ko-Y8wgshy8g4YLTpxOdp1cgOQW?usp=sharing)

Download the contents and extract them to the following structure:

TMS-EEG_preproc/data/    # Place TMS1 folder here
TMS-EEG_preproc/freesurfer_subject/    # Place Freesurfer subject folder here

## Quick Start

```bash
# Clone the repository
git clone https://github.com/LazyCyborg/TMS-EEG_preproc.git
cd TMS-EEG_preproc

# Create and activate conda environment
conda create -n tms_eeg python=3.8
conda activate tms_eeg

# Install requirements
pip install -r requirements.txt
```

### Setting Up File Paths

1. The notebook begins with a configuration cell where you can verify/modify these paths:
   ```python
   BASE_DIR = os.path.abspath(os.path.dirname('__file__'))
   DATA_DIR = os.path.join(BASE_DIR, 'data')
   FREESURFER_DIR = os.path.join(BASE_DIR, 'freesurfer_subjects')
