# 📊 Ad Group Structure & Status Analysis Tool

## 🚀 Overview
This is a **Streamlit-based automation tool** designed for **digital marketers and ad account managers** to analyze ad campaign activity across multiple accounts. It processes structured Excel files containing account info, ad reports, and keyword data to:

- Identify **ad groups matching custom naming patterns**
- Evaluate **ad and keyword status**
- Provide **summary metrics and insights** via an interactive UI

---

## 🧠 Key Features

- 🔍 **Pattern-Based Ad Group Detection**  
  Automatically finds ad groups based on naming rules using regular expressions (e.g., `New - Lease - 2024`, `Finance Other 2023`).

- 📂 **Multiple File Input Support with Validation**  
  Accepts three input files:
  - `accounts_list.xlsx`
  - `ad_report.xlsx`
  - `keyword_report.xlsx`

- ✅ **Ad & Keyword Status Checker**  
  Checks activation status of ads and keywords within each ad group.

- 🎛️ **Account-Wise Analysis with Dropdown**  
  Allows account-specific filtering — select any account to view its valid ad groups, ad/keyword activity, and group-level summaries.

- 📊 **Campaign-Level Metrics & Summary Stats**  
  Displays:
  - Total records processed
  - Active/inactive ad groups
  - Ad/keyword counts
  - Processing time

- 📥 **Export to CSV**  
  Final filtered output can be downloaded in `.csv` format.

---

## 📁 Input File Requirements

| File Name              | Required Columns                            |
|------------------------|---------------------------------------------|
| `accounts_list.xlsx`   | `Customer ID`, `Account name`               |
| `ad_report.xlsx`       | `Campaign`, `Ad group`, `Ad group ID`, headlines, descriptions, `Ad state`, etc. |
| `keyword_report.xlsx`  | `Ad group ID`, keyword status-related data  |

---

## 🛠️ Technologies Used

- `Streamlit` – UI rendering and interaction  
- `Pandas` – Excel parsing and data filtering  
- `Regex` – Pattern matching for ad group names  
- `OpenPyXL` – Excel file handling  
- `Python` – Core application logic

---

## 📦 How to Run Locally

1. **Clone the repo**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Create a virtual environment (optional but recommended)**:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the app**:
   ```bash
   streamlit run check.py
   ```

---

## 🧪 Example Use Case

> A marketing agency managing 50+ client accounts wants to quickly:
> - Identify which ad groups follow a standardized naming convention
> - Check if their ads and keywords are active
> - Export status reports and take action  
>  
> This tool handles all of that — instantly.

---

## 📸 Sample Output (Summary Table)

| Account Name | Campaign   | Ad Group               | Ads Status  | Keywords Status |
|--------------|------------|------------------------|-------------|-----------------|
| ABC Motors   | Lease2024  | New - Lease - 2024     | ✅ Active    | ❌ Not Active    |
| XYZ Finance  | Promo2023  | Finance Other 2023     | ❌ Not Active| ✅ Active         |

---

## 📄 License

This project is for educational and portfolio purposes. All data shown in examples is fictional.

---

## 🙌 Acknowledgements

Built with ❤️ using Streamlit and Pandas to simplify ad account auditing for digital marketers.
