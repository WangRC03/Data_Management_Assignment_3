# MovieLens 100K Data Analysis with PySpark and Zeppelin

**Author:** WANG RONGCHENG  
**Metric Number:** P150280

---

## Project Introduction

This project provides a comprehensive, end-to-end solution for analyzing the [MovieLens 100K dataset](https://grouplens.org/datasets/movielens/100k/) using PySpark and Apache Zeppelin.  
All stages of the workflow are carried out interactively within Zeppelin notebooks, leveraging Spark's distributed data processing capabilities and rich SQL support.

### Objectives

- **Data Engineering Practice:** To simulate a real-world data science workflow, starting from raw data ingestion through to structured analysis and reporting. To illustrate best practices for loading, parsing, and managing structured data in a big data environment.
- **Distributed Computing:** To take advantage of Apache Spark’s distributed processing power for scalable data manipulation and aggregation.
- **Reproducible Analytics:** To showcase powerful SQL and DataFrame-based analysis, such as movie popularity, user segmentation, and genre preferences. To provide a transparent and reproducible notebook that details every step, making it easy for others to learn from or extend the work.
- **Educational Value:** To provide reproducible, step-by-step code and explanations, making the project an effective study reference or course assignment example. To offer a practical learning resource for students and professionals interested in data engineering, big data analytics, and Spark SQL.

This notebook is designed to be highly educational and practical, suitable for coursework, tutorials, or independent study.  
All code blocks are annotated with detailed comments, and typical troubleshooting advice is included for common Spark/HDFS/Zeppelin issues.

---

## Project Overview

This project presents a comprehensive case study on big data analytics using the MovieLens 100K dataset, which is a widely-used benchmark for recommender systems and data mining research.  
The main goal is to demonstrate the complete pipeline for distributed data processing, SQL-based analytics, and result interpretation using the PySpark framework and Apache Zeppelin notebooks.

### Dataset

The project uses the following files from the MovieLens 100K dataset:

- `u.user`  – User information (user ID, age, gender, occupation, zip)
- `u.item`  – Movie information (movie ID, title, release date, 19 genre flags, etc.)
- `u.data`  – User ratings (user ID, movie ID, rating, timestamp)

### Environment

- Apache Zeppelin (with PySpark interpreter)
- Apache Spark 2.3 (with Hive support enabled)
- HDFS or local file system for data storage
- Python 3.2

### Technical Workflow

The project covers the following stages in detail:

1. **Spark Session Initialization:**  
   A SparkSession is created with Hive support enabled, making it possible to persist processed data as tables and perform powerful SQL analytics.

2. **Data Upload and Management:**  
   The raw MovieLens data files (`u.user`, `u.item`, `u.data`) are uploaded from the local environment to HDFS, ensuring they are accessible to Spark across all nodes.

3. **Data Parsing and Cleaning:**  
   Each file is read as a Resilient Distributed Dataset (RDD). The records are parsed, fields are converted to the correct types, and special handling is applied to fields like the genre indicators in `u.item`.

4. **DataFrame Construction and Schema Definition:**  
   The parsed data is transformed into structured Spark DataFrames using explicit schemas. This step enables fast, flexible, and SQL-compliant querying for all later analysis.

5. **Persistence to Hive Tables:**  
   The DataFrames are saved as permanent tables in the Hive metastore. This ensures data is not only available for SQL queries but also persists across sessions and can be used by other tools.

6. **Exploratory Data Analysis and SQL Analytics:**  
   A variety of analytical questions are addressed, including:
   - Calculating average movie ratings and popularity statistics.
   - Ranking movies by average rating and number of ratings.
   - Identifying active users and their genre preferences.
   - Segmenting users by demographic information such as age and occupation.
   - Performing advanced queries for specific user groups or movie genres.

7. **Result Visualization and Interpretation:**  
   Query results are displayed directly within Zeppelin cells, making it easy to visualize, interpret, and discuss findings.  
   Additional markdown explanations are provided to clarify each step, choice, and result.

### Key Features and Highlights

- **End-to-End Workflow:**  
  The project covers every stage from data acquisition to result interpretation, providing a holistic example of big data analytics with Spark.

- **Modular and Extensible Design:**  
  Each step is implemented in a modular fashion, allowing easy modification or reuse for similar projects or larger datasets.

- **Practical Troubleshooting:**  
  The notebook documents common errors (e.g., file path issues, schema mismatches, interpreter problems) and provides tested solutions.

- **Rich Educational Annotation:**  
  Detailed markdown explanations, comments, and code documentation are provided throughout to support learning and reproducibility.

- **Best Practices Demonstration:**  
  The project models industry-standard techniques for data ingestion, schema management, SQL analytics, and scalable ETL workflows.

### Significance

By walking through this workflow, I gain hands-on experience in modern data engineering and analytics using state-of-the-art open-source tools.  
The project not only delivers actionable insights into movie preferences and user behaviors, but also builds a solid foundation for future work in machine learning, data warehousing, or recommender systems development.

---




