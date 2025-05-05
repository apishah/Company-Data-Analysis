# Company-Data-Analysis


Conversation opened. 1 unread message.


Skip to content
Using Gmail with screen readers

1 of 42,672
(no subject)
Inbox

prachi shah <pbshah1326@gmail.com>
Attachments
10:44 PM (6 minutes ago)
to me


 One attachment
  •  Scanned by Gmail
# Company Data Profiling and Enrichment

This notebook processes and enriches company data by fetching details (like address, incorporation date, account status, etc.) from a Company Data API, performing data cleaning, formatting, and profiling.

## 📌 Features

### 1. Data Collection
- Loads company data from CSV.
### 2. Profiling
- unique() values and basic statistics are checked.
- Finding Records which doesn't have company_number or incorrect formatted data.

### 3. Cleansing
- Cleans and formats date columns (e.g., handles invalid dates like `33/10/3035`, Formating date like `22/10/2023` into format `2023-10-22`).
- Standardizes country names and removes invalid entries.

### 4. Matching & Enrichment
- Extracting Company_number from URI 
- For missing Company_number fetching Company details using 
 `https://api.company-information.service.gov.uk/advanced-search/companies`
- Fills missing data by calling an external company information API
`https://api.company-information.service.gov.uk/company/{company_number}`

### 5. Deduplication
- Handles duplicate records (retains the row with more populated fields).

### 6.reporting 
- Groups and summarizes data by country and account category.
- Finding number of records avaialble for each country.
- Number of Records per Country and Account Category.
- Finding out how many companies in each country has Partially Paid Mortgage, Outstanding Mortgage and Paid Mortgage.
- Finding how many companies has confirmation_statement overdue.
- Generates charts and profiling reports for data understanding.

## Requirements

Install required packages using:

```bash
pip install pandas numpy matplotlib
```

## 🚀 How to Run

1. Open the notebook `CompanyData.ipynb` in Jupyter or VSCode or Google Colab.
2. Ensure your data file (CSV) is correctly loaded.
3. Run all cells in order.


## 📁 Output

- Final cleaned DataFrame saved as CSV.
README.md
Displaying README.md.
