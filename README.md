# Cross-Platform Data Ingestion Pipeline: MySQL to HDFS using Sqoop

## Project Overview

This project demonstrates the implementation of a cross-platform data ingestion pipeline that transfers data from a MySQL database running on a Windows 10 host machine into Hadoop Distributed File System (HDFS) running on a CentOS 6 virtual machine using Apache Sqoop.

The objective was not only to perform a successful data import but also to understand and troubleshoot the infrastructure, networking, compatibility, and Hadoop ecosystem challenges commonly encountered in real-world Big Data environments.

---

## Architecture

Source System:

* MySQL 8.0 running on Windows 10

Data Transfer Tool:

* Apache Sqoop 1.4.7

Big Data Platform:

* Hadoop 2.7.3
* HDFS
* YARN

Operating Systems:

* Windows 10 Host Machine
* CentOS 6 Virtual Machine (VMware NAT Network)

---

## Data Flow

MySQL Database (Windows Host)
↓
JDBC Connection
↓
Apache Sqoop
↓
MapReduce Execution
↓
HDFS Storage (CentOS VM)

---

## Key Engineering Challenges Solved

### Network Connectivity

* Identified Windows host IP address.
* Enabled MySQL remote access.
* Configured MySQL to listen on external interfaces.
* Opened Windows Firewall for MySQL traffic.
* Verified connectivity from Linux VM.

### JDBC Compatibility

* Identified compatibility issues between Sqoop 1.4.7 and MySQL Connector versions.
* Selected and deployed a compatible JDBC driver.
* Integrated the driver into the Sqoop runtime environment.

### Linux Environment Configuration

* Diagnosed PATH-related execution failures.
* Configured SQOOP_HOME and PATH variables.
* Persisted environment variables through shell profile configuration.

### Hadoop Ecosystem Troubleshooting

* Investigated MapReduce execution failures.
* Diagnosed YARN ResourceManager misconfiguration.
* Corrected invalid ResourceManager endpoint configuration.
* Validated successful Hadoop service communication.

### End-to-End Data Validation

* Listed remote MySQL databases through Sqoop.
* Accessed source tables successfully.
* Imported relational data into HDFS.
* Verified successful storage within Hadoop.

---

## Skills Demonstrated

* Apache Hadoop
* HDFS
* YARN
* Apache Sqoop
* MySQL
* Linux Administration
* JDBC Connectivity
* Distributed Systems Troubleshooting
* Network Configuration
* VMware Networking
* Data Ingestion Pipelines
* Big Data Platform Operations

---

## Business Relevance

Organizations often need to ingest operational data from relational databases into data lakes for analytics, reporting, machine learning, and downstream processing.

This project simulates a common enterprise ingestion scenario where data must be moved from transactional systems into a Hadoop-based storage layer while resolving infrastructure and integration challenges along the way.

---

## Outcome

Successfully established a reliable pipeline between a Windows-hosted MySQL database and a Linux-based Hadoop environment, enabling relational data ingestion into HDFS through Apache Sqoop.

