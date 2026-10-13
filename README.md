# Privacy-Conscious Patient Data Processor

**AI Internship | Week 1 Milestone**

A Python-based data processing pipeline that validates synthetic patient records, masks personally identifiable information (PII), and exports cleaned data to a CSV file.

Built using core Python to demonstrate data handling, validation, and basic privacy-conscious programming practices.

## Features

- **CSV Processing:** Reads and writes patient records using Python's built-in `csv` module.
- **Data Validation:** Identifies missing fields, invalid ages, and incorrectly formatted patient IDs and phone numbers.
- **PII Masking:** Redacts patient names and partially masks phone numbers.
- **Error Handling:** Uses exception handling to identify invalid data.
- **Data Integrity:** Preserves the original dataset while generating a separate processed CSV.
- **Output Verification:** Uses assertions to check exported records.

## Technologies Used

- Python
- CSV Module
- Regular Expressions (`re`)
- Google Colab

No external data-processing libraries are required.

## Processing Workflow

```text
Synthetic Patient Dataset
          |
          v
     Read CSV Data
          |
          v
    Validate Records
          |
          v
 Separate Valid / Invalid
          |
          v
    Mask Sensitive PII
          |
          v
   Export Cleaned CSV
          |
          v
     Verify Output
```

## Sample Results

The pipeline was tested using 30 fictional patient records.

| Metric | Result |
|---|---|
| Total records | 30 |
| Valid records | 21 |
| Invalid records | 9 |
| Exported records | 21 |

### Example PII Masking

| Field | Original | Processed |
|---|---|---|
| Name | John Doe | [REDACTED] |
| Phone | 555-0198 | XXX-0198 |
| Age | 45 | 45 |
| Diagnosis | Diabetes | Diabetes |

## How to Run

1. Open the `.ipynb` notebook in Google Colab or Jupyter Notebook.
2. Run the cells sequentially.
3. The notebook generates the synthetic patient dataset.
4. Records are validated and sensitive fields are masked.
5. The processed records are exported to `clean_patients.csv`.

The notebook uses relative file paths for portability.

## What I Learned

- Applied Python fundamentals, including loops, dictionaries, and conditionals.
- Processed CSV files using core Python.
- Used regular expressions and exception handling for validation.
- Implemented basic PII masking.
- Separated invalid records from valid records.
- Verified output using assertions.
- Understood the distinction between data masking and anonymization.

## Limitations

- Designed for synthetic data and educational use only.
- Supports a simplified patient-data schema and phone number format.
- Masking does not guarantee anonymization.
- Patient IDs and medical attributes remain in the exported data.
- Not designed or validated for handling real patient data or meeting healthcare regulatory requirements.

## Conclusion

This milestone demonstrates a foundational understanding of Python data processing, input validation, and privacy-conscious handling of structured records.

It establishes a base for building more advanced data engineering and AI applications.

---

**Project Type:** AI Internship Milestone 01  
**Focus:** Python Fundamentals, Data Validation, PII Masking
