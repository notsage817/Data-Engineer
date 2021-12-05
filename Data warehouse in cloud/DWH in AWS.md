![image](https://user-images.githubusercontent.com/59595363/144727860-40c121bc-5533-4bd0-aeca-99a93aad4bba.png)
![image](https://user-images.githubusercontent.com/59595363/144727899-0398e3b7-bead-49fe-ac98-3cd6c73dd8a4.png)
![image](https://user-images.githubusercontent.com/59595363/144727904-3a604aad-960a-4b9f-afea-d461fb5efbf9.png)
![image](https://user-images.githubusercontent.com/59595363/144727940-cf722d19-d89e-41c4-b36b-75014caf1984.png)
![image](https://user-images.githubusercontent.com/59595363/144727961-81af0f08-3089-4cf8-8cbd-6f458c4427e9.png)
 #### Amazon Redshift Technology
 + Column-oriented
   + Best suited for storing OLAP workloads
   + Modified postgresql internally
 + Massively Parallel Processing (MPP) databases parallelize the execution of one query on multiples CPUs/machines
   + A table is partitioned and partitions are processed in parallel
 + cloud-managed
##### Architecture
Redshift architecture is the cluster of one leader node and more than one compute nodes
![image](https://user-images.githubusercontent.com/59595363/144728314-6af9b01c-7381-4841-9df5-f691b9d0a183.png)
Leader node 
+ communicate with outside client applications
+ coordinate compute nodes
+ optimize query execution
Compute node
