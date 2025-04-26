
 Package Sorting - Data Cleaning and Classification
Overview
This script processes a raw dataset of package dimensions and mass, simulating real-world inconsistencies, to classify packages according to sorting criteria used in a robotic automation factory.

The script:

Parses a manually provided CSV string with various data errors.

Cleans the data by handling missing values, invalid types, negative numbers, and malformed rows.

Classifies each valid package into STANDARD, SPECIAL, or REJECTED categories based on volume and mass.

Logs both successful classifications and errors found during ingestion.

Sorting Criteria
The sorting function applies the following logic:

A package is considered bulky if its volume (Width × Height × Length) is ≥ 1,000,000 cm³ or any dimension is ≥ 150 cm.

A package is considered heavy if its mass is ≥ 20 kg.

Classification:

If both heavy and bulky → REJECTED

If either heavy or bulky → SPECIAL

Otherwise → STANDARD

Data Cleaning
During ingestion, the script handles:

Repeated headers.

Rows with missing fields or "None" values.

Rows with non-numeric or corrupted fields (e.g., "abc", "23ab").

Negative dimension or mass values.

Rows with an incorrect number of columns.

Invalid entries are logged separately for internal reporting.

Output
The script generates:

A list of valid packages and their classification.

A list of discarded rows with the reason for rejection (e.g., missing fields, invalid types).

Potential Improvements
Replace manual parsing with pandas.read_csv() and enhanced error handling.

Calculate and display summary statistics (counts, percentages, average mass and volume per classification).

Export a clean CSV report summarizing results.

Extend support for very large datasets with efficient streaming or chunk processing.

