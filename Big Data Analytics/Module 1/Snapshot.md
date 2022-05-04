# HDFS Snapshots
## Questions
- By whom are the snapshots created?
- What command is used to create snapshots?
- What are HDFS snapshots?
- What features do snapshots offer?
	- How long does it take to create a snapshot?
	- What do the snapshots record
	- Do they affect HDFS operations?
	- What are the uses of Snapshots?
	- Which section does the Snapshot record?

## Answers
- HDFS Snapshots are created by **Administrators**
- HDFS Snapshots are created using `hdfs dfs -snapshot` command
- HDFS Snapshots are _read-only, point-in-time_ copies of the file system

- Featues of HDFS Snapshots:
	- Snapshots can be taken of a _sub-tree_ of the file system or the _entire_ file system
	- Snapshots can be used for data backup, protection against user errors, and disaster recovery.
	- Snapshot creation is instantaneous
	- Snapshot files record the _blocklist_ and the _file size_
	- Snapshot do not adversely affect regular HDFS operations