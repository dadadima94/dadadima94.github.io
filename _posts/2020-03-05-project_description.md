---
title: "Master Thesis: Log Analytics"
layout: post
date: 2020-03-04 21:00
picture: /assets/images/timeline.jpg
headerImage: false
tag:
- Master Thesis
- Data Science
- Log Anlytics
- Anomaly Detection
- Elastic Stack
projects: false
category: blog
author: dima
description: General Information and Current Status of my Master Thesis Project
---

## Summary:

- [Introduction](#introduction)
- [Background](#background)
- [Project Descriotion](#project-description)
- [Research Question](#research-question)
- [Current Status](#current-status)
- [Future Steps](#future-steps)
- [Timeline](#timeline)

---

## Introduction
An important part of a Master Degree at KTH is the final thesis and I am working on it under the academic supervision of [Sina Sheikholeslami](https://www.kth.se/profile/sinash). My work is conducted in close cooperation with the Data Science Team of Electrolux, which interned me as a Master Thesis Student in Data Science and Engineerig. Here, I am supervised by [Martin Neumann](https://se.linkedin.com/in/consultmartinneumann) throughout my research. The final examiner is [Amir Payberah](https://www.kth.se/profile/payberah). I want also to thank [Stephanie Nissen](https://www.linkedin.com/in/stephanie-nissen-9a8a5928/), who is helping me by providing me useful information and a free student license of the Elastic Stack.

## Background
With the introduction of microservices and cloud-based technologies, we have been able to find solutions for lots of problems which allow us to make stable distributed applications around the world, but this comes at a cost!
These distributed systems are maintained by different teams, different release cycles and so on. So to maintain the system in a healthier way we need to analyze full transaction and system activities. According to that, we can identify whether the systems or applications have malfunctions or anomalies. 
The main problem is that the microservices are isolated among themselves and do not share a common database or log files. 
So how to analyze all the transactions happened in a distributed system effectively?
This is the place where distributed log management envirornments, like the [Elastic Stack](https://www.elastic.co/what-is/elk-stack), come into play. Log management platforms can monitor all the issues just mentioned as well as process operating system logs, application logs, server logs, and many more.

## Project Description
The main scope of my project is to collect logs from different Internet of Things (IoT) environments in Elasticsearch and apply the anomaly detection algorithm included in the elastic stack to perform log analytics. Therefore, below there is a list of what my engineering tasks look like:

1. setup Elasticsearch, Kibana, and Logstash on Azure
2. gather IoT logs most likely using Azure logging service and Logstash/Beats from the Elastic Stack
3. cleaning and preprocessing of that data (to be done in Logstash)
4. building service dashboard in Kibana
5. run real-time anomaly detection built-in Elasticsearch and present the result in the dashboard from the previous point
6. creation of a labeled dataset of anomalies in the system (this will be achieved only if time permits)

## Research Question
This Master Thesis will address the problem of finding an Anomaly Detection solution on IoT logs better (or good enough) compared to the one integrated Elastic Stack. The other approaches will tried on Spark, by implementing a few different simple real-time anomaly detection algorithms. After that, the quality and the responsiveness of the prediction(s) of all of them will be assessed using the [Numenta benchmark (NAB)](https://numenta.com/machine-intelligence-technology/numenta-anomaly-benchmark/) as a reference. More specifically, this study will focus on comparing the two approaches (Elastic Stack and Spark) as a whole for the specific task of Anomaly Detection.

## Current Status
At the moment, I have set up the Elastic Stack on the cluster and I am collecting, processing and ingesting system logs for testing purposes. I played around and explored Kibana and the Elasticsearch APIs. I have started to write a script to process the IoT logs I will use in my research and I am looking at possible anomalies in the data in order to understand what I  should look for. In parallel, I am conducting literature research on the topic of Log Analytics and Anomaly Detection.

## Future Steps
Once the logs are ingested correctly, I will perform anomaly detection on them using the Elastic Stack, trying different aggregation and approaches. After that, I will try a couple of implementation in Spark and I will benchmark them using the NAB.

## Timeline 
![Here's a draft of what my timeline will look like.]({{ site.url }}/{{ page.picture }}){: .center-image }



