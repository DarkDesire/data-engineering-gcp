Data Engineer Practice Exam
===========================

> Storage of JSON files with occasionally changing schema, for ANSI SQL queries.

A. Store in BigQuery. Provide format files for data load and update them as needed.

B. Store in BigQuery. Select "Automatically detect" in the Schema section.

C. Store in Cloud Storage. Link data as temporary tables in BigQuery and turn on the "Automatically detect" option in the Schema section of BigQuery.

D. Store in Cloud Storage. Link data as permanent tables in BigQuery and turn on the "Automatically detect" option in the Schema section of BigQuery.

------

Correct
B. This is correct because of the requirement to support occasionally (schema) changing JSON files and aggregate ANSI SQL queries: you need to use BigQuery, and it is quickest to use 'Automatically detect' for schema changes.
