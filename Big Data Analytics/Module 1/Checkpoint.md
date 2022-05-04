# HDFS Checkpoints
#checkpoint #namenode #fsimage
## Questions
- What do checkpoints do?

## Answers
- NameNode stores the metadata of the HDFS in a file called `fsimage`
- File systems modification are written to a *log file*
- At startup the NameNode merges the edits into a new `fsimage`
- **CheckpointNode** periodically fetches edits form the NameNode, merges them, and returns an updated `fsimage` to the NameNode