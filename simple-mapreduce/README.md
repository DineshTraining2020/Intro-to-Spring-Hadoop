simple-mapreduce
================

Simple MapReduce example.

**Note:** This example depends on the `tweets-mapreduce` project, so you must first build and install that.

Requires that a tweets-hadoop*.txt file is available in HDFS under /twets/input/data dir.

From the XD shell run this:

```
xd:>hadoop config fs --namenode hdfs://borneo:8020
xd:>hadoop fs mkdir /tweets/input
xd:>hadoop fs mkdir /tweets/input/data
xd:>hadoop fs copyFromLocal --from /Users/trisberg/SpringOne/data/hadoop-tweets_2014-08-11.txt --to /tweets/input/data
```

**Note:** Adjust the `--from` path to what you are using.

Build with:

    $ mvn clean package

Run with:

    $ java -jar ./target/simple-mapreduce-0.1.0.jar
