# Business Intelligence


## five types of analysis
### descriptive
- often called data mining
- this form is the oldest and most common. This method involves aggregating or comparing historic values to answer the question “What happened?” or “What is happening?”
- provides insights and requires a large amount of human judgment to turn those insights into actionable information.

### diagnostic
- involves comparing historic data, often gathered in descriptive analysis, to other data sets to answer the question “Why did it happen?” 

### predictive
- involves predicting what might happen in the future based on what happened in the past.
- this form of analysis provides insights called predictions. These predictions also require human judgment to evaluate the validity, ensuring they are realistic.

### prescriptive
- involves looking at historic data and predictions to answer the question “What should be done?”
- this form of analysis deviates from the three previous in that it requires applications to incorporate rules and constraints to make intelligent recommendations
- greatest advantage of this form of analysis is that it can be automated
- Machine learning makes this method of analysis possible. 

### cognitive
- This form of analysis uses a type of artificial intelligence called deep learning.
- Deep learning, along with prescriptive analysis, is used to make decisions and take action based upon visual, auditory, or even natural language inputs.
- With each analysis, the results feed back into a knowledge database to inform future decisions.
- Self learning feedback loop

_______________________

- Ingest/Collect
- Store
- Process/Analyze
- Consume/Visualize
- Answers and Insights

Volume: amount of data the solution must handle
Velocity: the speed at which data enters and flows through your solution
Variety: ingesting data of many types from many sources
Veracity: trust worthiness of your data, you know the chain of custody for your data, accurate and consistent
Value: creating value

- Three data source:
  - Structured
    - Transactional database (heavy write and update)
    - Analytical database (heavy read) 
  - Semi-structured
  - Unstructured
    -  stored as files
    -  no pre defined schema
    -  pdfs
    -  maybe, little to no text
    -  preprocessing is necessary (maybe add tags, or catalog the data)
    
- Batch processing vs Streaming
- Scheduled vs periodic

## Introduction to structured data stores
- relational database (ACID)
- A process known as normalization helps a business take flat-file data and turn it into a relational database. Normalization is a set of rules that work together to reduce redundancy, increase reliability, and improve the consistency of data storage.
- OLTP vs OLAP
- why two different systems?
- comes down to how the resources supporting the db, is being used?
- write operation vs read operation
- use same resources but different 
- you can optimize for one, one is usually sacrified
- OLTP -> scheduled transformed ETL -> OLAP

### OLTP
Online transaction processing (OLTP) databases, often called operational databases, logically organize data into tables with the primary focus being on the speed of data entry. These databases are characterized by a large number of insert, update, and delete operations.
All decisions about the organization of data and storage of attributes is based on ensuring rapid data entry and updates. The effectiveness of an OLTP system is often measured by the number of transactions per second.

### OLAP
Online analytical processing (OLAP) databases, often called data warehouses, logically organize data into tables with the primary focus being the speed of data retrieval through queries. These databases are characterized by a relatively low number of write operations and the lack of update and delete operations.

All decisions about the organization of data and storage of attributes are based on the types of queries and other analytics that will be performed using the data. The effectiveness of an OLAP system is often measured by the response time of query results.


| Characteristic | OLTP                                                 | OLAP                                    |
| -------------- | ---------------------------------------------------- | --------------------------------------- |
| Nature         | Constant transactions (queries/updates)              | Periodic large updates, complex queries |
| Examples       | Accounting database, online retail transactions      | Reporting, decision support             |
| Type           | Operational data                                     | Consolidated data                       |
| Data retention | Short-term (2-6 months)                              | Long-term (2-5 years)                   |
| Storage        | Gigabytes (GB)                                       | Terabytes (TB)/petabytes (PB)           |
| Users          | Many                                                 | Few                                     |
| Protection     | Robust, constant data protection and fault tolerance | Periodic protection                     |

## Introduction to semistructured and unstructured data stores
- Semistructured and unstructured data are often stored in non-relational database systems, sometimes called NoSQL databases.
- Non-relational or NoSQL does not mean the data stored cannot be queried using SQL. A better way to think of it is not only SQL.
- rapid collection and retrival
- several broad category
  - document store: in the form of files, you can navigate the file using python, node-js or anything else
  - key-value database: semi structure data being stored as key value (schema less
- NoSql also has graph databases:
  - finding patterns in relationships


| Characteristics | Relational                                           | Non-relational                                               | Graph                                  |
| --------------- | ---------------------------------------------------- | ------------------------------------------------------------ | -------------------------------------- |
| Representation  | Multiple tables, each containing columns and rows    | Collection of documents<br>Single table with keys and values | Collections of nodes and relationships |
| Data design     | Normalized relational or dimensional data warehouse. | Denormalized document, wide column or key value              | Denormalized entity relationship       |
| Optimized       | Optimized for storage                                | Optimized for compute                                        | Optimized for relationships            |
| Query style     | Language: SQL                                        | Language: many<br>Uses object querying                       | Language: many<br>Uses object querying |
| Scaling         | Scale vertically                                     | Scale horizontally                                           | Hybrid                                 |
| Implementation  | OLTP business systems, OLAP data warehouse           | OLTP web/mobile apps                                         | OLTP web/mobile apps                   |



- data integrity
  - creation: ensuring data accuracy when data is created, regular audits might be necessary
  - aggregation: key phase for many systems, loss of integrity in this phase might due to planning
  - storage: maintaining data in secure form, some data is subject to frequent change, and some are stable
  - access: your data is visible to users, data's integrity cannot change, here it is mostly read only
  - sharing: once report has been created they are shared with businesses, read only here too.

**Data cleansing** is the process of detecting and correcting corruptions within data.
**Referential integrity** is the process of ensuring that the constraints of table relationships are enforced.
**Domain integrity** is the process of ensuring that the data being entered into a field matches the data type defined for that field..
**Entity integrity** is the process of ensuring that the values stored within a field match the constraints defined for that field.


ETL—Extract, Transform, Load—is the process of collecting data from raw data sources and transforming that data into a common type. This new data is loaded into a final location to be available for analytical analysis and inspection. In modern cloud-based environments, we often refer to this process as ELT (Extract, Load, Transform) instead. The steps are simply performed in a different order, but the result is the same.

## Introduction to data lakes

- A data lake is an architectural concept that helps you manage multiple data types from multiple sources, both structured and unstructured, through a single set of tools.
- A data lake takes Amazon S3 buckets and organizes them by categorizing the data inside the buckets. It doesn’t matter how the data got there or what kind it is. You can store both structured and unstructured data effectively in an Amazon S3 data lake.
- Out of the dire need for organizing the ever increasing volume of data, data lakes were born.
- Data lakes promise the ability to store all data for a business in a single repository. You can leverage data lakes to store large volumes of data instead of persisting that data in data warehouses.
- Data lakes, such as those built in Amazon S3, are generally less expensive than specialized big data storage solutions.
- That way, you only pay for the specialized solutions when using them for processing and analytics and not for long-term storage.
- Your extract, transform, and load (ETL) and analytic process can still access this data for analytics. 

## Benefits
- Single source of truth
- Store any type of data, regardless of structure
- can be used later for other purposes (AI etc)

## Data Warehouses
- central repository of structured data 
- usually transformed before put in the warehouse
- AWS -> Amazon Redshift
- build to store and query up to petabytes of data
- Amazon Redshift Specturm allows you to query both datalakes and data warehouse
- Amazon EMR: managed hadoop framework
- Whether you use Hadoop on-premises or Amazon EMR, you will use the same tools, with one major exception: Amazon EMR uses its own file system. And that means you can use your Amazon S3 data lake as the data store. So there’s no need to copy data into the cluster, as you would with Hadoop on-premises.
- Amazon EMR File System can catalog data within an Amazon S3 data lake and from an on-premises Hadoop File System at the same time
- The first principle of data analysis is to separate storage from processing. Amazon EMR is a perfect example of this principle.
- A data warehouse is a central repository of structured data from many data sources. This data is transformed, aggregated, and prepared for business reporting and analysis.
- Data flows into a data warehouse from transactional systems, relational databases, and other sources. These data sources can include structured, semistructured, and unstructured data. These data sources are transformed into structured data before they are stored in the data warehouse.
- Data is stored within the data warehouse using a schema. A schema defines how data is stored within tables, columns, and rows.
- Business analysts, data scientists, and decision makers access the data through business intelligence (BI) tools, SQL clients, and other analytics applications. 

## Data marts
- subset of data warehouse
- Data marts only focus on one subject or functional area
- A warehouse might contain all relevant sources for an enterprise, but a data mart might store only a single department’s sources.
- because data marts are generally a copy of data already contained in a data warehouse, they are often fast and simple to implement

| Characteristics       | Data warehouse                                                                                  | Data lake                                                                                                       |
| --------------------- | ----------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Data                  | Relational from transactional systems, operational databases, and line of business applications | Non-relational and relational from IoT devices, websites, mobile apps, social media, and corporate applications |
| Schema                | Designed prior to implementation (schema-on-write)                                              | Written at the time of analysis<br>(schema-on-read)                                                             |
| Price/<br>performance | Fastest query results using higher cost storage                                                 | Query results getting faster using<br>low-cost storage                                                          |
| Data quality          | Highly curated data that serves as the central version of the truth                             | Any data, which may or may not be curated (e.g., raw data)                                                      |
| Users                 | Business analysts                                                                               | Data scientists, data developers, and business analysts (using curated data)                                    |
| Analytics             | Batch reporting, BI, and visualizations                                                         | Machine learning, predictive analytics, data discovery, and profiling.                                          |
