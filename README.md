# Replicating Fama-French Factors (HML & SMB)

This project replicates the **Fama-French three-factor model**, specifically focusing on the construction and validation of the **HML (High Minus Low)** and **SMB (Small Minus Big)** factors using public stock data. The replication is then compared to the official Fama-French factors to evaluate accuracy.

---

## 📁 File Structure

### Main Notebook
- `replicating_fama_french_factor.ipynb`: Core notebook where HML and SMB are computed and compared.

### 📊 Data & Output
- `stock classification.csv`: Used to classify stocks into size and value portfolios.
- `Fama-French factors.csv`: Final output file containing:
  - `my_HML`, `my_SMB`: Replicated factors
  - `FF_HML`, `FF_SMB`: Official Fama-French factors (for comparison)

### 📁 fama-french data/
- `F-F_Research_Data_Factors.CSV`: Raw Fama-French factor data from the Kenneth French data library.
- `F-F_Research_Data_Factors.txt`: Documentation that explains the structure of the above CSV file.

### 📄 Reference & Output
- `Fama-French three factor calculation.pdf`: Official methodology used by Fama and French.
- `hml_comparison.png`: Visualization comparing your HML with the official one.

### ⚙️ Environment
- `requirements.txt`: Python packages required to run the notebook.

---

## ✅ Key Features

- Constructs **HML** and **SMB** using book-to-market and size-based portfolio sorting.
- Compares replicated factors with official Fama-French values.
- Computes correlation between the two sets across multiple time periods.
- Visual output (PNG) to demonstrate how closely the replication matches.

---

## 📈 Sample Correlation Results

| Period        | HML Correlation | SMB Correlation |
|---------------|------------------|------------------|
| 2022–2024     | 0.9977           | 0.9976           |
| 2016–2024     | 0.9978           | 0.9974           |
| 2001–2024     | 0.9968           | 0.9972           |
| 1962–2024     | 0.9778           | 0.9878           |

These results indicate the replication closely follows the official factors, especially in more recent years.

---

## ▶️ How to Run

### 1. Install Dependencies

```bash
pip install -r requirements.txt

### 2. Launch the Notebook
jupyter notebook replicating_fama_french_factor.ipynb

