# Cassandra-Learning


Apache Cassandra:

1). Open source,
2). NoSQL database
3). A Distributed database technology.
4). A big data technology which provides massive scalability.
5). Commonly used to create a database that is spread across nodes in more than one data center for high
    availability.
6). Based on Amazon Dynamo and Google Big table.
7). Cassandra is high performance and its for crating realtime applications.
8). Cassandra is used by netflix, accenture, hulu, ebay, instagram and many more big giants.
9). We can store massive amount of data.

https://cassandra.apache.org/ -> Read what is cassandra db
https://planetcassandra.org/  -> Read usage of cassandra db

System Requirement for Cassandra:

1). 64Bit OS System
2). 8gb Ram
3). 30gb HDD
4). VmWare


1). Cassandra is distributed database - Multiple servers allowing for massive horizontal skill
    ability in cassandra. In Cluster there is a master slave and many more nodes. Cassandra cluster can easily spread
    across more than one data center allowing for data visibility even if 1 or more data centers goes down.

    https://docs.datastax.com/en/home/index.html -> providing professional Services

2). SNITCH:- Snitch is how the nodes in a cluster know about the topology of the cluster.
    Ways to define snitch

    a). Dynamix Snitching
    b). Simple Snitch
    c). Rack Inferring Snitch
    d). Property File Snitch
    e). Gossiping Property File Snitch
    f). EC2Snitch
    g). EC2 Multi Region Snitch

    Property Snitch:
        130.77.100.147 =DC1:RAC1
        130.77.100.148 =DC1:RAC1
        130.77.100.151 =DC1:RAC2

        130.77.100.128 =DC2:RAC1
        130.77.100.129 =DC2:RAC2

3). GOSSIP: Gossip is how the nodes in a cluster communicate with each other.
    Every one second, each node communicates with up to three other nodes,
    exchanging information about itself and the other nodes that has information about.

    Gossip is the internal communication method for nodes in a cluster to talk to each other.

    For external communication, such as form an application to a cassandra database,
    CQL or Thrift are used.

4). DATA DISTRIBUTION:- Data distribution is done through consistent hashing, to strive for even
    distribution of data across the nodes in a cluster.

    The rows are distributed across the nodes in the cluster.

5). REPLICATION:- Replication factor must be specified whenever a database is defined,
                  The replication factor specified how many instances of the data there
                  will be within a given database.
                  Like if we have 3 instances, if 1 or 2 goes down, there is at least
                  1 more replica of the data is available.

6). VIRTUAL NODES:- Virtual nodes are an alternative way to assign token ranges to nodes
    and are now the default in cassandra.

    With virtual nodes, instead of a node being responsible for just one token range, it
    is instead responsible for many small token ranges.

    Virtual nodes were created to make it easier to add new nodes to a cluster while
    keeping the cluster balanced.
