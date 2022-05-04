# HDFS Block Replication
## Questions

## Answers
- HDFS writes a file, it is replicated across the cluster.
- The amount of replication is based on the value of `dfs.replication` in the `hdfs_site.xml` file
- Default value can be changed with `hdfs dfs -setrep` command.
- HDFS default block size is often 64MB. If file of 80MB is written to HDFS, a 64MB block iand 16MB block will be created.
- The HDFS block are based on size, while the splits are based on logical partitions of the data.