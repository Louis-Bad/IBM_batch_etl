# IBM_batch_etl
The below script will extract data from multiple sources and file types (csv, json, xml) before performing simple cleaning tasks and finally outputting a single csv file. The csv output file will be a collation of all the data ingested, post the simple cleaning transformation. <br>
Of course, this was just a fun evening project and the code has not been designed for any kind of commercial application.
<br><br>
The data is a very simple dataset comprising of a handful of people and a log of their names, height and weight. In the data file holding each of the datasets exists three duplicates of the same data. Again, the data itself is not important, more so that I had a simple collection of multiple sources of data to play around with. 
<br><br>
I have also taken a very 'functional programming' approach here, where all of the operations have been broken down into smaller modularised functions that will then be called within other functions representing the extract, transform and load operations of an automated ETL pipeline. This can (or will be) further generalised into a final single function that will take an arguement of one file path, directing the script to the directory containing the many differing sources of data. This final function will then output a single collation of these data sources as one .csv file and an accompanying etl_process_log.text file containing the details of each stage of the etl process and that stage's corresponding timestamp.
<br><br>
For the sake of true automation, the below code can easily be copied into a script text file and executed via an OS's automated task command.
