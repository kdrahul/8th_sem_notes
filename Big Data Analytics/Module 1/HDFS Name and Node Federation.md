# HDFS Name and Node Federation
#namenode 
## Questions
- What are the benefits of this?
- Provide an example

## Answers
- Key benefits are as follows:
	1. **Namespace Scalability**: HDFS cluster storage scale horizontally without placing burden on the [[NameNode]]
	2. **Better Performance**: Adding more [[NameNode]]s to the cluster scales the file system read/write operation throughput
	3. **System Isolation**: Multiple [[NameNode]]s enable different categories of applications to be distinguished.
- Example:
	-  -- Draw the diagram here 
	- [[NameNode]] 1 manages the _research_ and _marketting_
	- [[NameNode]] 2 manages the _data_ and _project_
	- NameNodes do not communicate with each other and [[DataNode]]s just store data blocks as directed by either [[NameNode]]