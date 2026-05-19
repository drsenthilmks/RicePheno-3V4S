# RicePheno-3V4S Dataset Metadata Generator

## Overview

The **RicePheno-3V4S Dataset Metadata Generator** is a comprehensive Python-based utility for:

- Automatic metadata extraction
- EXIF parsing
- Dataset validation
- Metadata CSV/Excel generation
- Rice phenotyping dataset organization

This tool was specifically designed for the **RicePheno-3V4S multi-sensor rice phenotyping dataset**, but can also be adapted for similar agricultural imaging datasets.

---

# Features

## Dataset Structure Discovery

Automatically scans and validates dataset folder structure.

Supported structure:

```text
Dataset/
│
├── ActiveTillering/
│   ├── CO51/
│   │   ├── UAV/
│   │   ├── DSLR/
│   │   └── Mobile/
│   ├── CR1009/
│   └── IWPonni/
│
├── PanicleInitiation/
├── Flowering/
└── Harvesting/
```

---

# Metadata Extraction

The script automatically extracts:

## Agricultural Metadata

- Rice variety
- Growth stage
- Sensor type
- Plot ID
- Collection date

## Technical Metadata

- Image resolution
- File size
- Bit depth
- Image format
- Aspect ratio
- Megapixels

## Camera EXIF Metadata

- Camera model
- Aperture (F-number)
- ISO
- Exposure time
- Focal length
- Capture timestamp

---


# Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/RicePheno-3V4S-MetadataGenerator.git

cd RicePheno-3V4S-MetadataGenerator
```

---

# Create Virtual Environment (Recommended)

## Windows

```bash
python -m venv venv

venv\Scripts\activate
```

## Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

---

# Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Required Python Packages

```text
pandas
numpy
Pillow
exifread
openpyxl
pyyaml
```

---

# Usage

## Run Metadata Generator

```bash
python metadata_generator.py
```

---

# Configuration

Inside the script:

```python
dataset_root_directory = (
    "../dataset/RicePheno-3V4S-Dataset_Ver.1.0.0/"
)
```

Update this path according to your dataset location.

---

# Generated Outputs

The script generates:

## metadata.csv

Structured metadata table.

## metadata.xlsx

Excel-compatible metadata file with formatting fixes.

---

# Output Metadata Columns

| Column | Description |
|---|---|
| image_id | Unique image identifier |
| filename | Relative image path |
| file_hash | MD5 file checksum |
| collection_date | Dataset collection date |
| variety | Rice variety |
| growth_stage | Rice growth stage |
| sensor_type | Sensor category |
| plot_id | Plot identifier |
| image_width | Width in pixels |
| image_height | Height in pixels |
| image_channels | Number of image channels |
| megapixels | Image megapixels |
| aspect_ratio | Image aspect ratio |
| file_size_mb | File size |
| image_format | Image format |
| bit_depth | Image bit depth |
| camera_model | Camera model |
| focal_length_mm | Focal length |
| aperture_f_number | Aperture value |
| iso | ISO value |
| exposure_time | Exposure time |
| capture_datetime | Original capture timestamp |

---

# Supported Sensors

- UAV
- DSLR
- Mobile

---

# Supported Rice Varieties

- CO-51
- CR1009
- IW-Ponni

---

# Supported Growth Stages

- Active Tillering
- Panicle Initiation
- Flowering
- Harvesting

---

# Example Output

```text
image_id: IMG_img001_8f2ab31c
variety: CR1009
growth_stage: Active_Tillering
sensor_type: uav
aperture_f_number: f/2.8
iso: 100
exposure_time: 1/1250 sec
```

---

# Advantages of This Version

## Cleaner Codebase

- Improved readability
- Meaningful variable names
- Modular functions

## Robust EXIF Handling

- Safe rational number parsing
- Prevents corrupted metadata

## Excel Compatibility

- Prevents date conversion bugs
- UTF-8 compatible export

## Dataset Scalability

Efficiently handles:

- Thousands of images
- Multi-sensor datasets
- Large-scale phenotyping projects

---

# Recommended Python Version

```text
Python 3.9+
```

---

# Citation

If you use this project in your research, please cite:

```text
RicePheno-3V4S: A Multi-Sensor Multi-Variety Rice Phenotyping Dataset
```

---

# License

This project is released under the MIT License.

---

# Author

Developed by: Senthilkumar. M.K.S.

## RicePheno-3V4S Dataset Project

Multi-Sensor Rice Phenotyping and Deep Learning Research.

---

# Contact

For issues, suggestions, or collaborations:

Create an issue on GitHub or contact the repository maintainer.
