# AWS EMR

* cloud based big data platform
* open source tools
    * Apache Spark
    * Apache Hive
    * Apache HBase
    * Apache Flink
    * Apache Hudi
    * Presto
> analysis Petabyte`s of data at less than half of the cost of traditional on-premises solutions and over 3x faster than standard Apache Spark.

# Benefits

* Easy to use 
    * [EMR Notebooks](https://pages.awscloud.com/EMR_Notebooks.html)
* Low cost
* Elastic
    * Auto Scaling (which manages cluster sizes based on utilization)
* Reliable
    * retrying failed tasks and automatically replacing poorly performing instances
    * don’t have to manage updates and bug fixes
    * less effort to maintain the environment
* Secure
    * EC2 firewall settings
    * launches clusters in an Amazon Virtual Private Cloud (VPC)
    * S[erver-side encryption](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingServerSideEncryption.html) or [client-side encryption](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingClientSideEncryption.html)
    * other [encryption options](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-data-encryption-options.html) and [Kerberos](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-kerberos-configure.html)
* Flexible
    * dependencies in Docker containers
---

# Use cases

* Machine learning
    * Tools
        1. Apache Spark MLlib
        2. TensorFlow
        3. Apache MXNet
    * use custom AMIs and bootstrap actions
    * create your own predictive analytics toolset.
* Extract transform load (ETL)
    * data transformation workloads
    * Case Study [REDFIN](https://aws.amazon.com/solutions/case-studies/redfin/)
* Clickstream analysis
    * understand user preferences, and deliver more effective ads.
* Real-time streaming
    * [Kafka, Kinesis] -> [S3, HDFS]  using [Spark, Flink]
* Interactive analytics
* Genomics

### Amazon EMRMigration Guide


## KAFKA -> HDFS

* [Gobblin](https://github.com/apache/incubator-gobblin).
* [Kafka Connect framework](https://github.com/confluentinc/kafka-connect-hdfs).
