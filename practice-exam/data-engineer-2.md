Data Engineer Practice Exam
===========================

> Q. Storage of JSON files with occasionally changing schema, for ANSI SQL queries.

A. Store in BigQuery. Provide format files for data load and update them as needed.

B. Store in BigQuery. Select "Automatically detect" in the Schema section.

C. Store in Cloud Storage. Link data as temporary tables in BigQuery and turn on the "Automatically detect" option in the Schema section of BigQuery.

D. Store in Cloud Storage. Link data as permanent tables in BigQuery and turn on the "Automatically detect" option in the Schema section of BigQuery.

---
**Correct. B.** This is correct because of the requirement to support occasionally (schema) changing JSON files and aggregate ANSI SQL queries: you need to use BigQuery, and it is quickest to use 'Automatically detect' for schema changes.

---
> Q. Low-cost one-way one-time migration of two 100-TB file servers to Google Cloud; data will be frequently accessed and only from Germany.

**Possible A.** Use Transfer Appliance. Transfer to a Cloud Storage Standard bucket.

**Possible B.** Use Transfer Appliance. Transfer to a Cloud Storage Nearline bucket.

**Not C.** Use Storage Transfer Service. Transfer to a Cloud Storage Standard bucket.

**Not D.** Use Storage Transfer Service. Transfer to a Cloud Storage Coldline bucket.

---
**C-D.** This is not correct because you should only use Transfer Service for a one-time one-way transfer. Also, Storage Transfer Service does not work for data stored on-premises.

---
> Q. Cost-effective backup to Google Cloud of multi-TB databases from another cloud including monthly DR drills.

A. Use Transfer Appliance. Transfer to Cloud Storage Nearline bucket.

B. Use Transfer Appliance. Transfer to Cloud Storage Coldline bucket.

**Possible C.** Use Storage Transfer Service. Transfer to Cloud Storage Nearline bucket.

**Not D.** Use Storage Transfer Service. Transfer to Cloud Storage Coldline bucket.

---
**D**. This is not correct because you should not use Coldline if you want to access the files monthly.

---
