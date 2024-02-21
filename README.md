# Extracting Diagnoses from Medical Transcription by Fine-Tuning Longformer Model

## Overview
In the realm of healthcare, accurately capturing comorbidities in chronically ill patients remains a significant challenge due to limitations in traditional medical transcription. This project introduces an innovative approach using the Longformer model, fine-tuned to predict six types of diagnoses—namely, anemia, atrial fibrillation, hyperlipidemia, hypertension, pneumonia, and a category encompassing other conditions—from the MIMIC-IV Notes discharge summaries. Utilising the BioCreative V CDR corpus, diagnoses were identified within the discharge diagnosis sections. The model, trained on texts averaging over 1,312 words post-processing, demonstrated high accuracy, with an F1-Score of 0.9555, Precision of 0.9580, and Recall of 0.9531. Despite computational constraints leading to a reduced dataset (6,000 from an available 110,000) and a shift to multiclass rather than multilabel classification, the project highlights the potential of NLP in enhancing diagnostic precision and streamlining medical documentation, ultimately contributing to improved patient care.

## Repository Contents
This repository contains the following Jupyter Notebook files:

1. **MIMIC_IV_Preprocessing.ipynb**:
   - Describes label encoding and data cleaning processes for the discharge summaries.
   - Utilizes NLP tools such as ScispaCy and NLTK libraries.

2. **MIMIC_IV_Longformer_Tokenizer.ipynb**:
   - Details the implementation of tokenization for the free-text data using the Longformer model.

3. **MIMIC_IV_Longformer_Multiclass_Classification.ipynb**:
   - Documents the application of the Longformer model in classifying the diagnoses.

4. **MIMIC_IV_BART_Model.ipynb**:
   - Presents an initial attempt using the BART transformer model, highlighting its limitations in processing long documents and the consequent inaccuracies in prediction.

## Accessing the MIMIC-IV Notes Dataset
Note: The MIMIC-IV Notes dataset is not included in this repository.

To access the dataset, please visit the [PhysioNet website](https://physionet.org/) or refer to their [documentation on MIMIC-IV data access](https://physionet.org/content/mimiciv/2.2/).
