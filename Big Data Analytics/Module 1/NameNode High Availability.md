# NameNode High Availability
#namenode 

## Questions
- Why is it used?
- How many clusters does HA Hadoop have?
- What are those clusters? Explain them.

## Answers
- [[NameNode High Availability]] is used to provide _failover service_.
- HA Hadoop cluster has two separate [[NameNode]] machines configured with same software:
	- **Active State**: Responsible for all client HDFS operation in the cluster.
	- **Standby State**: Maintain enough state to provide a fast failover.
- Both active and standby [[NameNode]] receive block reports from the [[DataNode]].
- Three JournalNodes are required to maintain the updated file, so that they can tolerate failure of a single JournalNode machine.
- StandbyNode continuously reads data from ActiveNode. In the event of active Node failure, the StandbyNode can promote itself to Active State.
- To prevent confusion between [[NameNode]]s, the JournalNodes allow only one [[NameNode]] to be a writer at a time.
- [Apache Zookeper](https://zookeeper.apache.org/) is used to monitor the [[NameNode]] health