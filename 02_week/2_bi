# Business Intelligence

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
