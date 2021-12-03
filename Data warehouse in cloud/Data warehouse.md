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
_some of the most famous design_
### Kimball's Bus Architecture
![image](https://user-images.githubusercontent.com/59595363/142093265-b3fb7d58-aaa4-4d4a-8a32-5ca8be7f0b7d.png)
+ ETL
  + Extracting
    + Get the data from its source
    + Possibly deleting old state
  + Transforming
    + Integrate many sources together
    + Possibly cleansing: inconsistencies, duplication, missing values
    + Possibly producing diagnostic metadata
  + Loading
    + Structuring and loading the data into the dimensional data model
### Independent Data Marts
![image](https://user-images.githubusercontent.com/59595363/142094387-e705e475-522a-41f6-b1e5-95f066854dfb.png)
+ Departments have independent ETL processes & dimensional models
+ These **separate & smaller** dimensional models are called "Data Marts"
+ Different fact tables for the same events, **no conformed dimensions**
+ Uncoordinated efforts can lead to inconsistent views
+ Despite awareness of the emergence of this architecture from departmental autonomy, it is generally discouraged
### Inmon's Corporate Information Factory (CIF)
![image](https://user-images.githubusercontent.com/59595363/142095181-bc36d72c-fda5-4958-b7b6-dbd5260fc35f.png)
+ 2 ETL Processes
  + Source systems &rarr; 3 NF DB
  + 3 NF DB &rarr; Departmental Data Marts
+ The 3NF DB acts an enterprise wide data store
  + Single integrated source of truth for data-marts
  + Accessable for end-users
+ Data marts dimensionally modelled & mostly aggregated
### Hybrid Bus & CIF
![image](https://user-images.githubusercontent.com/59595363/142095867-da7a25aa-0a42-48f3-a86c-d74efa51b3b9.png)
Combine of Kimball and Inmon
## OLAP Cubes
>An OLAP cube is an aggregation of a fact metric on a number of dimensions, which is easy to cummunicate to business users.
### Approaches
+ *MOLAP*: Pre-aggregate the OLAP cubes and saves them on a special purpose non-relational database
+ *ROLAP*: Compute the OLAP cubes on the fly from the existing relational databases where the dimensional model resides

**Roll up** 
- Sum up a branch by a higher hierarchy of category(eg. sum up sales of all the cities by countried)

**Drill down** 
- Decompose a branch to a lower hierarchy of category.(eg. decompose sales of each city into districts)

**Slice & Dice** 
- Slice: Reducing N dimensions to N-1 dimensions by restricting one dimension to a single value 
- Dice: Same dimensions but computing a sub-cube by restricting some of the value of the dimensions

>OLAP cubes technology
>
>Pre-aggregate the OLAP cubes and saves them on a special purpose non-relational database(MOLAP)
> 
> Compute the OLAP cubes on the fly from the existing relational databases where the dimensional model resides(ROLAP)
