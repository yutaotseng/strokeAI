# StrokeAI: Using Electrocardiogram to Classify Stroke by Artificial Neural Networks

## Overview

This repository contains the code and resources for an AI-driven system designed to classify different type of strokes, including ischemic stroke and intracranial hemorrhage (ICH), using electrocardiogram (ECG) data. The project integrates deep learning models, data preprocessing pipelines, and interpretability tools to enhance early stroke detection and support clinical decision-making. The current implementation supports binary classifications, such as distinguishing normal vs. ICH or normal vs. ischemic stroke.


## Key Features

- **Deep Learning Model**: A DenseNet-based architecture optimized for classifying stroke from ECG data.
- **Data Cleaning & Annotation**: Comprehensive preprocessing pipeline to handle raw ECG data, including filtering, normalization, and artifact removal.
- **Model Interpretability**: Saliency maps implementation to visualize key ECG segments influencing predictions, fostering clinical trust in the model.
- **Performance**: Achieves high accuracy with an AUROC of 0.98, demonstrating robust classification capabilities.
- **End-to-End Pipeline**: Seamlessly processes raw data through preprocessing, model training, evaluation, and visualization.

## Motivation

Stroke is a leading cause of mortality and morbidity worldwide, with early diagnosis playing a critical role in improving patient outcomes. ECG data, often collected during triage at the emergency department, may hold subtle clues indicative of stroke. This project seeks to unlock the potential of ECG data in stroke diagnostics using AI.


## Repository Structure

Repository Structure

The repository is organized into the following components:

---

### 1. Preprocessing
Contains scripts for cleaning and annotating raw ECG data to create a well-structured and labeled dataset, ensuring readiness for model training and evaluation.

- **`CopyPasteFilesForSaliencyMaps_V01.ipynb`**: Handles file management for saliency map generation.
- **`GetECGSeverityInfo_V01.ipynb`**: Extracts severity information from ECG data.
- **`GetOutlier_V01.ipynb`**: Identifies and processes outliers in the dataset.
- **`parseSVG_V01.ipynb`**: Parses and preprocesses SVG-based ECG data.
- **`patientCharacteristicAnalysis_V01.ipynb`**: Analyzes patient characteristics for data preparation.

### 2. Model
Implements the deep learning model based on the ResNet architecture, optimized for classifying intracranial hemorrhage (ICH) or ischemic stroke from ECG data.

- **`ClassifierModel_V06.ipynb`**: Core model architecture and training pipeline.

### 3. Saliency Map
Includes tools for enhancing model interpretability by visualizing critical ECG segments influencing classification decisions.

- **`modelVisualization_V04.ipynb`**: Generates saliency maps to highlight key ECG features used by the model.
- **`modelWeightAnalysis_V02.ipynb`**: Analyzes and visualizes the model’s weight contributions.

---

These components collectively enable efficient preprocessing, robust model training, and enhanced transparency in AI-driven stroke detection.


## Usage
### 1. Clone the repository:
```bash
git clone https://github.com/your-repo-name.git
cd your-repo-name
```

### 2.	Prepare your environment:
Ensure you have Python 3.x installed along with the required libraries such as numpy, pandas, torch, and matplotlib. Install additional dependencies as needed for your specific setup.

### 3.	Preprocess the data:
Use the scripts in the Preprocessing folder to clean and annotate raw ECG data. Depending on your dataset, you may need to run multiple scripts in sequence. For example:
- Start with parseSVG_V01.ipynb to extract ECG features.
- Use GetOutlier_V01.ipynb to identify and handle outliers.
- Further refine data using patientCharacteristicAnalysis_V01.ipynb.

### 4.	Train the model:
Load and configure the deep learning model in ClassifierModel_V06.ipynb for training and evaluation.

### 5.	Visualize model interpretability:
After training, run modelVisualization_V04.ipynb and modelWeightAnalysis_V02.ipynb to generate saliency maps and analyze model weights, enhancing interpretability.

## Results
- **Performance**: The model achieves high classification accuracy, with an AUROC of 0.98 for distinguishing between normal and intracranial hemorrhage (ICH) cases.
- **Supported Classifications**:
  - Normal vs. ICH
  - Normal vs. Ischemic Stroke
- **Interpretability**: Saliency maps reveal critical ECG segments influencing predictions, fostering clinical trust in the AI model.

## Contributing
We welcome contributions! Feel free to open issues or submit pull requests for enhancements or bug fixes.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contact
For questions or collaboration inquiries, contact Yu-Tao (Danny) Tseng at yutaotseng@gmail.com.