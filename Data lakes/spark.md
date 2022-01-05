### Four key machine components

>CPU handles every process on computers. 
>Data that waits to be processed stores in memory temporarily. When computer shuts down, the data in the memory is lost.
>So data is kept in *Storage* over long periods of time and is loaded to memory teporarily when program runs.

+ *CPU-Central Processing Unit-handle every process on computer*
  + 2.5 Gigahertz CPU means that CPU processes 2.5 billion operations per second,Computer operate 8 bytes data per operation
  + 200 times faster than memory
+ *Memory-Main Memory/RAM-store data before it goes to CPU*
  + "efficient, expensive, ephemeral"
  + 15 times faster than SSD
+ *Storage-SSD/Magnetic Disk-keep data over long periods of time*
  + slow when deal with gigabyte or terabyte data
  + Magnetic disk is 200 times slower than memory and SSD is 15 times slower then memory.
  + 20 times faster than network
+ *Network-LAN/Internet-access to outside of computer*
  + The bottlenect when working with big data

Memory is efficient when load data into CPU, however, it's ephemeral and expensive. One of strategies that set GOOGLE apart is bypassing the expense of memory by building distributed systems using commodity hardware. Google leveraged long-term storage on cheap pre-used hardware.
A distributed system is a bunch of connected machines that called nodes and the commodity hardware is common to be purchased under tight budget. These early systems at google are the foundation of technology of *spark*
