# Explainable-AI-Cardio-Risk
## 📉 Reproducibility & Data Privacy

Due to the **Data Use Agreement (DUA)** of PhysioNet, we cannot share the raw MIMIC-III patient data used in this study.

### Demo Mode (Default)
The notebook includes a **dummy data generator**. If you run the code directly (e.g., in Colab), it will detect missing data and automatically generate synthetic text.
* **Purpose:** To verify code functionality and pipeline logic.
* **Note:** The performance metrics (Accuracy/AUC) obtained on dummy data are **meaningless** and will not match the paper.

### Reproduction Mode (For Credentialed Users)
To reproduce the exact results reported in the paper:
1. Obtain access to MIMIC-III via [PhysioNet](https://physionet.org/content/mimiciii/).
2. Extract discharge summaries for patients with ICD-9 codes `410-414` and `428`.
3. Save the data as `data/cardio_notes.csv` with columns: `subject_id`, `hadm_id`, `text`, `target`.
4. Run the notebook. The script will detect the file and switch to **Real Data Mode**.

[![Open In Colab](https://colab.research.google.com/drive/1GEuMTW7qVDEEJExIqVy2gyL0ZXSVNCgZ?usp=drive_link)
