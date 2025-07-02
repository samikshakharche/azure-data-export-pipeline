Azure Data Export Pipeline

This mini-project showcases how to export data from an Azure SQL Database into three commonly used file formats — CSV, Parquet, and Avro — using Azure Data Factory. It’s designed to help understand how data can be transformed and saved in multiple formats for various use cases like analytics, reporting, and storage.
________________________________________
What This Project Does

Using Azure’s powerful data tools, this pipeline takes data from a SQL table and saves it in:

•	CSV – widely supported and easy to read

•	Parquet – efficient for analytics

•	Avro – useful for storing data with evolving schemas
________________________________________
Tools and Services Used

•	Azure SQL Database – where the data (e.g., a 'Students' table) is stored

•	Azure Blob Storage – used to store the exported files

•	Azure Data Factory (V2) – manages the movement and conversion of the data

•	File Formats – CSV, Parquet, Avro
________________________________________
How the Pipeline Works

The pipeline, named ExportToAllFormats, is set up to perform these steps:

1.	Connects to a SQL Database and reads the Students table
  
2.	Creates three parallel “Copy Data” activities that:
   
o	Export the data to a .csv file

o	Export the data to a .parquet file

o	Export the data to a .avro file

3.	All three files are saved into separate folders inside Azure Blob Storage.
________________________________________
Key Components Explained

•	Linked Services – Connect ADF with SQL and Blob

•	Datasets – Represent source (SQL_Students) and sinks (CSV_Students, Parquet_Students, Avro_Students)

•	Pipeline Activities – Copy data to all three formats in parallel from a dummy start activity
________________________________________
Where the Files Are Saved

export-data-task-1 
which is the container saved in the storage account
_______________________________________
How the Pipeline Runs

•	Triggered manually using the "Trigger Now" option in ADF

•	Can be extended with schedule or event-based triggers
________________________________________
Screenshot Folder

Screenshots included in the GitHub repo:

•	datasets.png

•	pipeline-structure.png

•	monitor-results.png
________________________________________
Author

Samiksha Kharche

This project helped me explore cloud-based data pipelines and real-world data integration using Azure tools.
