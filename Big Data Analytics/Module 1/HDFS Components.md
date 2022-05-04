# HDFS Components
#HDFS #namenode #datanode #architecture
## Questions
- Types of nodes?

## Answers
- There are two types of nodes
	1. **[[NameNode]]**: Manages all the metadata needed to store and retrieve the actual data from the [[DataNode]]s. No data is stored on this node.
	2. **[[DataNode]]**: A single **[[DataNode]]** daemon will be running on at least one machine.
- Design is **Master/Slave** architecture:
	- Master(**[[NameNode]]**) manages the file system namespace and regulates access to files by clients.
	- File system namespace operations managed by **[[NameNode]]**:
		- Opening
		- Closing
		- Renaming files and directories
	- Slave(**[[DataNode]]**) are responsible for serving read and write requests from the file system to the clients.
	- **Master/Slave Architecture** ![[HDFS Architecture.png]]
		- When client writes data, it communicates with [[NameNode]] to create a file
		- NameNode then determines number of nodes needed to store the data
		- Data blocks are replicated after they are written to the assigned node
		- **Reading Data**:
			- The client request for a file. [[NameNode]] returns [[DataNode]] to read the data.
			- Conversation between the client and the [[DataNode]] begins.
			- NameNode keeps track of [[DataNode]] by listening to heartbeats sent from [[DataNode]]
			- Lack of heartbeat indicates node failure.
			- Thus [[NameNode]] may redidrect client to other [[DataNode]] consisting of replicated data.
			- Client can now continue reading missing data.
		- Secondary NameNode:
			- Performs periodic checkpoints that evaluate the status of the [[NameNode]].
			- It also has two disk files that track changes to the metadata:
				- An image of the file system state when the [[NameNode]] was started. This file begins with `fsimage_*`.
				- A series of modifications done to the file system indicated by the `edit_*`.