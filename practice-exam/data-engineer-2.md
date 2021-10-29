Data Engineer Practice Exam
===========================

> **Q. Storage of JSON files with occasionally changing schema, for ANSI SQL queries.**

A. Store in BigQuery. Provide format files for data load and update them as needed.

B. Store in BigQuery. Select "Automatically detect" in the Schema section.

C. Store in Cloud Storage. Link data as temporary tables in BigQuery and turn on the "Automatically detect" option in the Schema section of BigQuery.

D. Store in Cloud Storage. Link data as permanent tables in BigQuery and turn on the "Automatically detect" option in the Schema section of BigQuery.

---
**Correct. B.** This is correct because of the requirement to support occasionally (schema) changing JSON files and aggregate ANSI SQL queries: you need to use BigQuery, and it is quickest to use 'Automatically detect' for schema changes.

---
> **Q. Low-cost one-way one-time migration of two 100-TB file servers to Google Cloud; data will be frequently accessed and only from Germany.**

**Possible A.** Use Transfer Appliance. Transfer to a Cloud Storage Standard bucket.

**Possible B.** Use Transfer Appliance. Transfer to a Cloud Storage Nearline bucket.

**Not C.** Use Storage Transfer Service. Transfer to a Cloud Storage Standard bucket.

**Not D.** Use Storage Transfer Service. Transfer to a Cloud Storage Coldline bucket.

---
**C-D.** This is not correct because you should only use Transfer Service for a one-time one-way transfer. Also, Storage Transfer Service does not work for data stored on-premises.

---
> **Q. Cost-effective backup to Google Cloud of multi-TB databases from another cloud including monthly DR drills.**

A. Use Transfer Appliance. Transfer to Cloud Storage Nearline bucket.

B. Use Transfer Appliance. Transfer to Cloud Storage Coldline bucket.

**Possible C.** Use Storage Transfer Service. Transfer to Cloud Storage Nearline bucket.

**Not D.** Use Storage Transfer Service. Transfer to Cloud Storage Coldline bucket.

---
**D**. This is not correct because you should not use Coldline if you want to access the files monthly.

---
> **Q. 250,000 devices produce a JSON device status every 10 seconds. How do you capture event data for outlier time series analysis?**

A. Capture data in BigQuery. Develop a BigQuery API custom application to query the dataset and display device outlier data.

B.Capture data in BigQuery. Use the BigQuery console to query the dataset and display device outlier data.

C. Capture data in Cloud Bigtable. Use the Cloud Bigtable cbt tool to display device outlier data.

D. Capture data in Cloud Bigtable. Install and use the HBase shell for Cloud Bigtable to query the table for device outlier data.

---
**Correct. C.** This is correct because the data type, volume, and query pattern best fit Cloud Bigtable capabilities.

---
> **Q. Event data in CSV format to be queried for individual values over time windows. Which storage and schema to minimize query costs?**

A. Use Cloud Storage. Join the raw file data with a BigQuery log table.

B. Use Cloud Bigtable. Design tall and narrow tables, and use a new row for each single event version.

C. Use Cloud Storage. Write a Dataprep job to split the data into partitioned tables.

D. Use Cloud Bigtable. Design short and wide tables, and use a new column for each single event version.

---
**Correct. B.** This is correct because it is a recommended best practice. Use Cloud Bigtable and this schema for this scenario. Cloud Storage would have cheaper STORAGE costs than Cloud Bigtable, but we want to minimize QUERY costs.

---
> **Q. Customer wants to maintain investment in an existing Apache Spark code data pipeline.**

A. BigQuery

B. Dataflow

C. Dataproc

D. Dataprep

---
**Correct. C.** This is correct because Dataproc is a managed Hadoop service and runs Apache Spark applications.

---
> **Q. Host a deep neural network machine learning model on Google Cloud. Run and monitor jobs that could occasionally fail.**

**Not A.** Use AI Platform to host your model. Monitor the status of the Operation object for 'error' results.

B. Use AI Platform to host your model. Monitor the status of the Jobs object for 'failed' job states.

C. Use a Google Kubernetes Engine cluster to host your model. Monitor the status of the Jobs object for 'failed' job states.

D. Use a Google Kubernetes Engine cluster to host your model. Monitor the status of the Operation object for 'error' results.

---
**A.**  This is not correct because you should not use the Operation object to monitor failures.

---

> **Q. Cost-effective way to run non-critical Apache Spark jobs on Dataproc?**

A. Set up a cluster in high availability mode with high-memory machine types. Add 10 additional local SSDs.

B. Set up a cluster in high availability mode with default machine types. Add 10 additional preemptible worker nodes.

**C.** Set up a cluster in standard mode with high-memory machine types. Add 10 additional preemptible worker nodes.

D. Set up a cluster in standard mode with the default machine types. Add 10 additional local SSDs.

---
**Correct. C.** This is correct because Spark and high-memory machines only need the standard mode. Also, use preemptible nodes because you want to save money and this is not mission-critical.

---
