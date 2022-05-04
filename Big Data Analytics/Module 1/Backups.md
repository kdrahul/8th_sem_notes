# HDFS Backups
#checkpoint #backup #namenode 

- **BackupNode** maintains an up-to-date copy of the file system namespce both in _memory_ and _on disk_
- NameNode supports one **BackupNode** at a time.
- No **CheckpointNode** may be registered if a **BackupNode** is in use.