# Vine-Reviews
Use ETL, Amazon Web Services, and Spark to analyze big data on an Amazon dataset.

---

# Project Summary
This two-part project uses big data and Amazon Web Services to gather and analyze a dataset on Amazon reviews for video games. In the first part of the project, I performed ETL process in Google Colaboratory. I extracted the video games dataset from an S3 bucket using Spark into a PySpark dataframe, transformed the raw data so that it fits the tables according to the ERD diagram, and loaded the transformed raw data into an Amazon RDS instance once connected to Postgress. In the second part of the project, I continued to use PySpark to perform statistical analysis and determine if the vine reviews were biased. 

# Findings
For the analysis, I filtered my data frames that had at least 20+ votes and at least 50% of helpful votes, then filtered by those that have and did not have a vine review. Summary statistics showed that there could be biased among "Star Ratings" given the quantities of "viner" and "non-viner" reviews. There were about 41,000 records that did not have vine reviews, and only 94 records that did have vine reviews. Next, I calculated the percentage of 5-star ratings for both groups. 51% of Amazon reviews that were part of the vine program gave a 5-star rating. In comparison, 38% of Amazon reviews that were not part of the vine program also gave a 5-star rating. Given the fact that there were significantly less Amazon reviews that had "viners" than those Amazon reviews that did not have "viners", there is the possibility of biased in the "Star Ratings".
