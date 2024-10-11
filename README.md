# COMP90051 Report - Predicting Postoperative Cardiovascular Risks with MOVER Data

## Project Overview
This project aims to predict cardiovascular complications in patients following general anesthesia using the MOVER dataset. The data, collected over five years from the University of California, Irvine Medical Center, contains comprehensive patient records. Cardiovascular complications pose significant risks to patient recovery and overall health. Therefore, developing a classification model to accurately predict these complications can greatly aid in improving patient care and outcomes.

## Dataset Overview
The MOVER dataset contains various tables with detailed information about patients, their medical history, procedures, and outcomes. Here is a summary of the key tables used in this project:

| **EPIC Dataset Table**              | **Description**                                                                                                                                             |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Patient Information**             | Demographic data (e.g., age, sex, height, weight) and surgery details (e.g., surgery type, start and end times, ASA status, discharge disposition).           |
| **Patient History**                 | Patient health history, including all diagnoses available in the Electronic Health Record (EHR).                                                             |
| **Patient Visit**                   | Records of diagnoses and diagnosis codes for each patient visit.                                                                                             |
| **Patient Medications**             | Information on prescribed medications, including dosage, administration time, prescription time, and route of medication.                                    |
| **Patient LDA**                     | Descriptions of lines, drains, and airway devices used on patients, including placement time, removal time, and location of placement.                        |
| **Patient Labs**                    | Lab orders for patients, corresponding observed measurements, and reference values for each lab test.                                                        |
| **Patient Measurements**            | All preoperative and postoperative measurements, including vital signs, intake and output, pain levels, complications, and disposition.                       |
| **Patient Postoperative Complications** | Type of complications and detailed notes describing them.                                                                                                 |
| **Patient Procedure Events**        | Preoperative, perioperative, and postoperative events, along with their corresponding timestamps.                                                            |
| **Patient Coding**                  | Billing codes for patient procedures and treatments.                                                                                                         |

### ECG Waveform Data
The dataset also includes ECG waveform data, which provides vital insights into patient heart activity. These waveforms are encoded in alphanumeric format and need to be decoded before analysis.

## Data Decoding
To decode the ECG waveform data, a Python script named `waveform_decode.ipynb` is provided in the `code` folder. This script decodes the waveforms, preparing them for feature extraction and model training.

### How to Decode EPIC_wave_form Data
1. Clone or download this project.
2. Place the `waveform_decode.ipynb` script in the `code` folder.
3. Navigate to the `code` folder in your terminal or command line, then run:
   ```bash
   python waveform_decode.py
   ```
4. The decoded data will be saved in the `processedData` folder, ready for further analysis.

## Project Structure
```
- code
  - feature_extraction_part1.ipynb  # First part of feature extraction process, focusing on initial data processing.
  - feature_extraction_part2.ipynb  # Second part of feature extraction, including advanced feature engineering.
  - waveFeature_extraction.ipynb  # Extracting features specifically from waveform data.
  - waveform_decode.ipynb         # Script to decode alphanumeric-encoded ECG waveform data.
  - EDA.ipynb                     # Exploratory Data Analysis to understand dataset patterns and trends.
  - LogicRegression.ipynb         # Implementation of Logistic Regression model for prediction.
  - patient_label.ipynb           # Script for labeling patient data for training and testing.
  - SVM.ipynb                     # Support Vector Machine (SVM) model for classification.
  - Tabnet.ipynb                  # TabNet model for deep learning-based classification.
- data
  - rawData/                      # Raw data files, including patient information, history, labs, etc.
  - processedData/                # Processed data files, including extracted features and decoded waveform data.
- README.md                       # This file

```

## How to Run
1. Download or clone this repository.
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Decode the waveform data:
   ```bash
   python code/waveform_decode.ipynb
   ```
4. Open and run the Jupyter Notebooks for data analysis and model training (e.g., `EDA.ipynb`, `feature_extraction_part1.ipynb`, etc.).

## Results Analysis
The classification model predicts the likelihood of cardiovascular complications in patients after general anesthesia. Detailed analysis and model performance metrics are available in the notebooks `LogicRegression.ipynb`, `SVM.ipynb`, and `Tabnet.ipynb`.


## License
This project is for academic research and educational purposes only. Commercial use is not permitted.


