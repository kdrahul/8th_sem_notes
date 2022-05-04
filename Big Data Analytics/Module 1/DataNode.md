# DataNode
#datanode 
A [[DataNode]] is a HDFS process that manage storage attached to the [nodes](https://datacadamia.com/db/hadoop/node) that they run on.

The [[DataNode]] are responsible for serving [read and write requests from the file system’s clients](https://datacadamia.com/db/hadoop/hdfs/client#operation "A client establishes a connection to a configurable TCP port on the NameNode machine. It talks the ClientProtocol with the NameNode.  A Remote Procedure Call (RPC) abstraction wraps both the Client Protocol and the DataNode Protocol.  Articles Relateddata integrityMemory Storage Support in HDFSFileSystem Java The Hadoop FileSystem DefinitionC language wNFS gateway"). The [[DataNode]] also perform block creation, deletion, and replication upon instruction from the NameNode.