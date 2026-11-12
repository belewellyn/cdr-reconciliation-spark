# CDR Reconciliation in Telecom — PySpark Capstone

A data engineering capstone completed as part of the Purdue University / Simplilearn Post Graduate Program in Data Engineering (2026).

## Project overview

Telecommunications systems generate call detail records (CDRs) that need to be validated before downstream billing and reporting. This project uses **Apache Spark (PySpark)** to reconcile expected record counts against actual CDR data and flag discrepancies.

## Technologies

- Python
- Apache Spark / PySpark
- Spark DataFrames
- CSV/text file ingestion and output

## Workflow

1. Load a pipe-delimited reconciliation file containing expected file names and record counts.
2. Load a tab-delimited CDR dataset.
3. Group the CDR records by `CDR_FILENAME` to calculate actual counts.
4. Left-join actual counts to expected counts using the file name.
5. Label each file as `Match` or `Mismatch`.
6. Export the reconciliation results to CSV.

## Repository contents

- `CDR_Reconciliation_Capstone.ipynb` — notebook reconstructed from the original capstone PySpark source code.
- `requirements.txt` — Python dependency.

## How to run

1. Install Python and a Java runtime compatible with your Spark version.
2. Install the dependencies with `pip install -r requirements.txt`.
3. Open the notebook in JupyterLab, Jupyter Notebook, or VS Code.
4. Obtain the original input files: `file_count_reconciliation.txt` and `rec_cdr_1.txt` (not included).
5. Update the notebook's `/home/labuser/` input and output paths to your local paths.
6. Run the notebook cells.

**Note:** This repository contains the project code, not the original input datasets or an independently verified execution. The notebook preserves the original capstone logic.

## Skills demonstrated

Data ingestion, Spark DataFrame transformations, aggregation, joins, data-quality validation, and batch output generation.
