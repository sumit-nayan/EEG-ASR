# EEG-ASR Experiment Platform

A Streamlit-based platform for EEG Artifact Subspace Reconstruction (ASR), focused on eye blink artifact removal, calibration efficiency, and subject generalization.

---

## 🚀 Features

- **Interactive Web App**: Upload EEG CSV files and perform ASR experiments in your browser.
- **Supported Experiments**:
  - **Intra-Subject Calibration**: Analyze blink removal vs. calibration length.
  - **Eyeblink Classification**: Detect robust, partial, and missed blinks.
  - **Standardized Cleaning**: Visualize raw vs. cleaned signals (time & frequency domains).
  - **Inter-Subject Generalization (LOSO)**: Train on all but one subject.
  - **Generalization Trends**: Visualize trends in RRMSE, bandpower, and blink metrics.

---

## 📦 Installation

```bash
git clone https://github.com/sumit-nayan/EEG-ASR.git
cd EEG-ASR
pip install -r requirements.txt
```

---

## 📁 Usage

1. **Prepare Your Data**  
   - Format: CSV, one file per subject.  
   - Each column = one channel (`Ch_1`, `Ch_2`, ..., `Ch_24`)  
   - Each row = one time sample.

2. **Launch the App**
    
    ```bash
    streamlit run main.py
    ```

3. **Interact with the UI**  
   - Upload subject CSV files via sidebar.  
   - Set sampling rate (e.g., 500 Hz).  
   - Choose an experiment and view plots & metrics.

---

## 📂 Project Structure

| File/Folder        | Description                          |
|--------------------|--------------------------------------|
| `main.py`          | Streamlit application                |
| `requirements.txt` | Python dependencies                  |
| `*.csv`            | EEG subject files (user-provided)    |

---

## 📊 Example CSV Format

| Ch_1 | Ch_2 | Ch_3 | ... | Ch_24 |
|------|------|------|-----|-------|
|  ... | ...  | ...  | ... |  ...  |

---

## 🧪 Experiments Summary

| Experiment                          | Description                                      |
|------------------------------------|--------------------------------------------------|
| Intra-Subject Calibration          | Blink removal vs. calibration duration           |
| Eyeblink Classification            | Classify robust/partial/missed blinks            |
| Standardized Cleaning              | Compare raw vs. cleaned (plots, bandpower, etc.) |
| Inter-Subject Generalization (LOSO)| Leave-one-subject-out validation                 |
| Generalization Trend Analysis      | Metric trends across all subjects                |

---

## 📝 Notes

- Use raw (unfiltered) EEG data for best results.
- Performance may vary with file size and system specs.
- Fully modular: add your own experiments easily.

---

## 📄 License

MIT License

---

## 👨‍💻 Author

Developed by [sumit-nayan](https://github.com/sumit-nayan)
