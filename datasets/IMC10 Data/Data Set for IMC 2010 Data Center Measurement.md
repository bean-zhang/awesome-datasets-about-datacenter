## Data Set for IMC 2010 Data Center Measurement

This page contains data from three of the data centers studied in the IMC 2010 paper titled [Network Traffic Characteristics of Data Centers in the Wild](http://pages.cs.wisc.edu/~tbenson/papers/imc192.pdf). The data centers are: UNI1, UNI2, and PRV1. For each of these data centers, this page contains links for topology and SNMP data. Packet traces form the university data centers (UNI1 and UNI2) are available; however, due to space constraints you should directly contact me at tbenson@cs.wisc.edu for access.

|   Data Center Name    |   Topology Data   |   SNMP Data   |   Packet Traces   |
|   ----------------    |   -------------   |   ---------   |   -------------   |
|   UNI1                |   [Topology](http://pages.cs.wisc.edu/~tbenson/IMC_DATA/unv1.cdp.txt)        |   [SNMP](http://pages.cs.wisc.edu/~tbenson/IMC_DATA/unv1.sql.tgz)        |   [Packet Trace](http://pages.cs.wisc.edu/~tbenson/IMC_DATA/univ1_trace.tgz)    |
|   UNI2                |   [Topology](http://pages.cs.wisc.edu/~tbenson/IMC_DATA/unv2.cdp.txt)        |   [SNMP](http://pages.cs.wisc.edu/~tbenson/IMC_DATA/univ2.sql.tgz)        |   [Packet Trace](http://pages.cs.wisc.edu/~tbenson/IMC_DATA/univ2_trace.tgz)    |
|   PRV1                |   [Topology](http://pages.cs.wisc.edu/~tbenson/IMC_DATA/prv1.cdp.txt)        |   [SNMP](http://pages.cs.wisc.edu/~tbenson/IMC_DATA/prv1.sql.tgz)        |   Unavailable    |

### Naming Conventions

cr[0-9]+ Core devices
rc[0-9]+ Core devices
es[0-9]+ Edge/ToR devices
b[0-9]+ An external border device that peers with the core routers (Not included)

### Data Formats

#### Topology

The topology files are plain text files. Each line in the file contains the following 4 columns: `source_device` `source_interface` `destination_device` `destination_interface`

#### SNMP

The SNMP files are compressed text files. They can be uncompressed using the following commands "tar -xzf ". The each line in the uncompressed text files contains an SQL insert query for populating a MySQL database. The following [sql file](http://pages.cs.wisc.edu/~tbenson/IMC_DATA/routerinterfacedata.sql) will create the appropriate table.

#### Packet Trace

The packet trace files are compressed pcap files. They can be uncompressed using the following commands "tar -xzf ". In anonymizing the data, the payload have been nulled out and the IP addresses have been anonymized using SHA1 hash. The traces are a snippet of the total data used in our evaluation. They contain the snippet that we are allowed to publish.
