## Cerebrate

# Quick Links

Website: [cerebrate.online](http://cerebrate.online)  
Presentation: [bit.ly/cerebrateOnline](http://bit.ly/cerebrateOnline)  

# Background

Cerebrate was the project that I created during my time as a Data Engineering Fellow with Insight Data Science in early 2017.  The purpose of this three-week project was to build a pipeline that could ingest, process, and visualize large amounts of data.  

# Pipeline

Most of this project is centered around Flink, which processes the streaming data.  Data is generated by a pair of Python scripts (one script to make requests to nodes, the other to supply them) and ingested by Kafka.  After reading and processing the stream, Flink sends the transformed data streams back to Kafka.  Kafka then hands the data to RethinkDB, which coordinates with Flask to form a front-end.  

![alt tag][pipeline.png]