# HDFS NFS Gateway
## Questions
- Which version of NFS does it support?
	- What does the supported version offer?
- What other features does it offer?

## Answers
- Supports **NFSv3**, enables HDFS to be mounted as part of the client's local file system.
- HDFS NFS Gateway offers users the following capabilities:
	- Users can easily download/upload files from/to the HDFS file system to/from their local file system
	- Users can stream data directly to HDFS through the mount point. Appending to a file is supported, but random write capabilities is not supported.