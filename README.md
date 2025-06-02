
# 📊 Task 1: Data Cleaning and Preprocessing

## 🗂 Dataset
**Medical Appointment No Shows**  
This dataset contains information about medical appointments in Brazil and whether patients showed up.

## 🛠 Tools Used
- Python
- Pandas
- Jupyter Notebook

## ✅ Cleaning Steps Performed

1. **Loaded Dataset**
   - Used `pandas.read_csv()` to load the data.

2. **Checked Basic Info**
   - Used `.shape`, `.info()`, and `.describe()` for initial exploration.

3. **Renamed Columns**
   - Converted all column names to Pascal case(first letter of each word is capitalized) for consistency.

4. **Checked for Duplicates**
   - Verified with `df.duplicated().sum()` — no duplicates found.

5. **Checked and Handled Missing Values**
   - Confirmed that there were no missing values.

6. **Converted Date Columns**
   - `ScheduledDay` and `AppointmentDay` converted to datetime format.

7. **Filtered Invalid Date Differences**
   - Removed rows where `day_diff` was negative (appointment before scheduled).
  
8. **Changed Data Type**
   - Changed data type of PatientID from float to int for memory efficiency.

9. **Validated and Cleaned Age Column**
   - Removed rows with negative ages or ages > 120 (unrealistic).

## 📁 Output Files
- `data/cleaned_healthcare_noshows.csv` – final cleaned dataset 
- `preprocessing.ipynb` – Jupyter Notebook with all steps

## 💡 Notes
This task focused on essential data cleaning tasks including:
- Standardizing formats
- Ensuring logical consistency
- Handling outliers and potential data entry errors
