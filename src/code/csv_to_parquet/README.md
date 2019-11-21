Converting CSV to PARQUET usecase
In this usecase, we are just taking the csv file from the local and by using the schema of the csv and convert the csv file into parquet file, change the name of the file .csv to .parquet

InferAvroSchema to get the schema of the csv file

ConvertCSVToAvro it convert the csv to avro by using the schema

UpdateAttribute it remove the .csv in the file name 

ConvertAvroToParquet it change the avrop into parquet and add .parquet to the filename
