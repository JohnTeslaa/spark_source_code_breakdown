Structured Streaming 如何实现exactly_once语义？

技术上：the system ensures end-to-end exactly-once fault-tolerance guarantees through checkpointing and Write-Ahead Logs. 
要配置：checkpointLocation
WAL怎么开启？



外部条件：
The engine uses checkpointing and write-ahead logs to record the offset range of the data being processed in each trigger. 
The streaming sinks are designed to be idempotent for handling reprocessing. 
Together, using **replayable sources and idempotent sinks**, Structured Streaming can ensure end-to-end exactly-once semantics under any failure.
