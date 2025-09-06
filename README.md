# 🧹 Data Cleaning and Preprocessing  

## 📌 Overview  
This repository contains work on **data cleaning and preprocessing**.  
The main focus is on preparing raw data into a **clean, analysis-ready format** by fixing **dirty data** (invalid, inconsistent) and **messy data** (untidy structure).  

Currently, it includes cleaning of the **Audible Dataset (Audiobooks metadata)**.  
More datasets may be added in the future.  

---

## 📂 Dataset  

- **Raw file:** `audible_uncleaned.csv`  
- **Cleaning notebook:** `data_cleaning.ipynb`  
- **Cleaned output:** `cleaned_audible.csv`  

---

## ⚠️ Data Issues Identified  

- **Dirty Data (Validity Problems):**  
  - Wrong data types (`release_date` as string instead of datetime, price as string with commas)  
  - Invalid formatting (duration in `"x hrs y mins"` string format)  
  - Combined info in one column (`stars` = rating + review count)  

- **Messy Data (Tidiness Problems):**  
  - Author and narrator prefixed with `"Writtenby:"` / `"Narratedby:"`  
  - Rating stored as text instead of separate numeric values  
  - Wide-format columns needing restructuring  

---

## 🛠️ Cleaning Steps  

1. **Standardize Strings** (remove prefixes, trim spaces)  
2. **Convert Data Types** (strings → datetime, strings → floats/integers)  
3. **Split Columns** (stars into rating + rating count)  
4. **Format Durations** (`"x hrs y mins"` → `timedelta`)  
5. **Reshape Data** into tidy format where needed  

---

## ✅ Example of Cleaned Output  

| name              | author         | narrator        | time            | releasedate | language | price | star | rating_count  |
|-------------------|----------------|-----------------|-----------------|-------------|----------|-------|------|---------------|
| The Burning Maze  | Rick Riordan   | Robbie Daymond  | 0 days 13:08:00 | 2018-05-01  | English  | 820.0 | 4.5  | 41            |

---

## 🚀 Usage  

Clone the repo:  
```bash
git clone https://github.com/yashthakur-01/Data-cleaning.git
cd Data-cleaning
