# Data Warehouse
## Business Perspective
Business is about a set of processes, including *Operational Processes* and *Analytical Processes*
> Eg. A retail's data infrastructure
> ##### Operational Process
> - customers should be able to find goods & make orders
> - Inventory staff should be able to stock, retrieve & re-order goods
> - Delivery staff should be able to pick up & deliver goods
> ##### Analytical Process
> - HR should be able to access the performance of sales staff
> - Marketing should be able to see the effect of different sales channels
> - Management should be able to monitor sales growth
##### A database could not satisfy the demand of both kind of processes. Data Warehouse is a system which includes the processes and technologies and data representations that enable the support to analytical process.
### OLAP vs OLTP
#### OLAP: Online Analytical Processing
#### OLTP: Online Transactional Processing
## Technical Perspective
- Data warehouse is a copy of transaction data specifically stuctured for query and analysis
- A data warehouse is a **subject-oriented**, **integrated**,**nonvolatile** and **time-variant** collection of data in support of management's decisions
  - **subject-oriented** means there is no one-size-fits-all and needs to be categorized by topic
  - **integrated** means the information comes from several resources
  - **nonvolatile** means it has to be persisitant rather than transient
  - **time-variant** means the answer to the same question could change over time
- A data warehouse is a system than retrieves and consolidates data periodically from the source systems into a dimensional or normalized data store.It usually keeps years of history and is queried for business intelligence or other analytical activities. It is typically updated in batches, not everytime a trsaction happens in the source system
### Dimensional Model
The dimensional model is designed to 
+ Make it easy for business users to work with the data
+ Improve analytical queries performance
#### Fact vs. Dimension table

## Data Warehouse Architecture
__some of the most famous design__
### Kimball's Bus Architecture
![image](https://user-images.githubusercontent.com/59595363/142093265-b3fb7d58-aaa4-4d4a-8a32-5ca8be7f0b7d.png)

### Independent Data Marts
### Inmon's Corporate Information Factory (CIF)
### Hybrid Bus & CIF
