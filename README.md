# Student-Academic-Performance-Monitoring-System

## Overview
In many primary schools, tracking student progress and identifying struggling learners can be challenging when relying solely on manual record-keeping. This project leverages **Python** and data analysis libraries (`Pandas`, `Matplotlib`) to automate the cleaning, organisation, and analysis of academic records for **74 pupils** across **Primary 4, Primary 5, and Primary 6** in a selected primary school in Ibadan, Oyo State.

The goal is to demonstrate how data-driven insights can help teachers and administrators monitor academic performance, compare class trends, and identify pupils who may require additional academic support.

## Tech Stack and Libraries
* **Language:** Python
* **Environment:** Jupyter Notebook / Google Colab
* **Core Libraries:**
  * `Pandas` (Data loading, cleaning, manipulation, and aggregation)
  * `Matplotlib` / `Seaborn` (Data visualisation and performance charting)

## Methodology and Workflow
1. **Data Collection and Loading:** Imported raw academic records from Excel into a Pandas DataFrame (`df`).
2. **Data Cleaning:**
   * Handled missing values (`dropna`) and checked for duplicate student IDs.
   * Standardised inconsistent class name labels (e.g., mapping `"P4"`, `"PRI 4"` to `"PRIMARY 4"`) using `.str.strip()`, `.str.upper()`, and `.replace()`.
   * Converted 12 subject score columns to numeric data types using `pd.to_numeric(..., errors='coerce')`.
3. **Performance Analysis:**
   * Calculated individual total scores and average scores across 12 subjects (`axis=1`, `min_count=1`).
   * Aggregated data by class to compare pupil counts, average performance, and highest/lowest individual averages.
4. **Intervention Flagging:** Identified pupils falling below performance thresholds to highlight who might need targeted academic assistance.
5. **Data Visualisation:** Generated graphs to illustrate score distributions, subject averages, and class comparisons.

## Key Findings and Insights
* **Overall Performance:** Across all 74 pupils, the overall mean student average was approximately **60.85**.
* **Class-Level Breakdown:**
  * **Primary 5:** Recorded the highest class average (**72.15**) and the highest individual average (**84.08**).
  * **Primary 6:** Had the largest cohort (28 pupils) with a class average of **55.67** and contained the lowest individual average (**41.17**).
  * **Primary 4:** Recorded the lowest class average (**55.12**).
* **Takeaway:** The class with the lowest average is distinct from the class containing the single lowest-performing pupil, highlighting the necessity of granular, pupil-level tracking.

## Future Enhancements
* Expand the dataset to include multiple schools for broader regional benchmarking.
* Track longitudinal performance across different terms and academic sessions.
* Build an interactive dashboard (e.g., using Streamlit) for teachers to easily view student and subject summaries.

## Project Contributors
* **Chimamaka Victor Daniel**
* **Umeizudike Franklyn Chukwuemeka**

