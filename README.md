# big-data-crime-and-weather
A big data system to handle weather and crime data | Final Project MPCS 53013 Big Data

### Summary
This repo implements a [lambda architecture](https://en.wikipedia.org/wiki/Lambda_architecture) for a large-scale application that takes realtime weather and crime data, ingests it, then automatically running views of the data for users. I'm working on recovering the full implementation from the servers and will have the all the files, including raw Java files, here soon.

You can see the Speed layer interface [here](http://104.197.248.161/agolab-crime-reports.html). Fair warning, it's not very pretty because of the time constraints placed on this project -- the effort was, necessarily, on the back end functionality.

### Tools Implemented

- Assumes a Hadoop HDFS file system hosted on Google Cloud
- Apache Kakfa for Serving Layer data collection
- Apache Storm topology for Serving Layer ingestion
- Apache Thrift data structure for fact-based, schema-on read data storage
- Apache Pig for Batch Layer pre-computed view construction
- Apache HBase for pre-computed view storage, Serving Layer data storage, and data access in Speed Layer
- Super basic HTML with Python back-end for Speed Layer data access

### What's Here

- ingestFiles contains the jars for ingestion
- javaFiles will contain the java files that are the core functionality of the ingestFiles jars (retrieving)
- set-up contains the necessary shell code for running various aspects of the system
- pigFiles contain all the Pig code for batch layer runs
- mvn and pig contain necessary jars for implementation
