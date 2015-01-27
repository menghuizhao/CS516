#CompSci 516 
#Data-intensive Computing Systems - Project Part 0

Mengzhe Zhao

mz69@duke.edu

##Apache Storm
__Strengths__

* Do not require custom code.
* Failures, fault tolerance, threads and tuple distribution are all handled by Storm.

__Weaknesses__

* Tick tuples are topology specific.Cannot use them for managing different batch schedules for different components within topologies.

__References__

* http://zh.hortonworks.com/blog/apache-storm-design-pattern-micro-batching/

##Accumulo
__Strengths__

* Accumulo supports very large rows with very large numbers of columns. Its rows do not need to fit in memory and its columns do not need to be specified in advance.
* An off-heap in-memory map (where recently written data goes) which makes it less susceptible to Java garbage collection issues.

__Weaknesses__

* Comparing with HBase,Accumulo’s read caching is not currently as good as HBase's.

__References__

* http://accumulo.apache.org/notable_features.html

##Apache Hive

__Strengths__

* Hive is good at querying.

__Weaknesses__

* Hive's security support still has some gotchas on the operational side.

__References__

* http://www.quora.com/What-are-the-pros-and-cons-between-Pig-and-Hive

##AWS EMR

__Strengths__

* Dynamic MapReduce cluster sizing.
* Ease of use for simple jobs via their proprietary web console.
* Great documentation.
* Integrates nicely with other Amazon Web Services.

__References__

* http://www.quora.com/What-are-the-advantages-disadvantages-running-Clouderas-distribution-for-Hadoop-on-EC2-instances-rather-than-using-Amazons-Elastic-Map-Reduce-Service

##CouchDB
__Strengths__

* Simplicity. CouchDB can store any JSON data. Each document can have any number of binary attachments.
* Due to map/reduce, querying is separated from data itself.

__Weaknesses__

* Arbitrary queries are expensive. In order to do a query that haven't been created a view for, users need to create a temporary view.
* There's a bit of extra space overhead with CouchDB compared to most alternatives.

__References__

* http://www.quora.com/What-are-the-pros-and-cons-of-CouchDB

##Cloudera's Distribution for Hadoop
__Strengths__

* CDH is open source. CDH packages a number of open source projects that are not included with EMR. Users have access to the complete platform composed of data collection, storage, and processing tools.
* A stable and feature-rich product. CDH packages a number of critical bug fixes and features and the most recent stable releases.
* CDH includes a number of integrations with other software components of the data management stack. It's easy to integrate CDH with an existing analytics infrastructure.
* CDH has been designed and deployed in common Linux environments.

__References__

* http://www.quora.com/What-are-the-advantages-disadvantages-running-Clouderas-distribution-for-Hadoop-on-EC2-instances-rather-than-using-Amazons-Elastic-Map-Reduce-Service

##Cassandra
__Strengths__

* Can be running on multiple platforms: e.g. CentOS, Red Hat, Debian, Ubuntu, Mac OS X, Windows.
* Symmetric architecture, which makes Cassandra relatively easy to create and scale large clusters.
* SQL-like Cassandra Query Language eases developers' transition from RDBMS.
* Balance performance and consistency well.
* Free product. Open source under Apache License version 2.0.

__Weaknesses__

* Configuration is relatively complicated.
* The management GUI is difficult to get up and running.

__References__

* http://www.infoworld.com/article/2610676/database/review--cassandra-lowers-the-barriers-to-big-data.html

##AWS DynamoDB

__Strengths__

* DynamoDB has a pretty simple flat key-value store.
* Support for conditional writes and sets.
* AWSDynamoDB Split up users' datasheet uniformly across enough database nodes to meet users' demands.
* Almost guarantee single-digit latencies.

__Weaknesses__

* Transactions are not supported.

__References__

*http://stackoverflow.com/questions/19750404/what-are-the-pros-and-cons-of-dynamodb-with-respect-to-google-cloud-datastore 

##DeepDB
__Strengths__

* Quick and easy installation.
* Gives MySQL DBAs the ability to improve ACID transaction throughput by 5~10 times, dramatically reduce query latencies, reduce data storage to half of the current size.
* Support very large tables (> 1 billion rows).
* Use cloud disk storage systems highly efficiently.
* Good Scalability.

__References__

* http://bigdata.sys-con.com/node/3080848

##DB2
__Strengths__

* Can be running on most major platforms, including Windows. Compatible with large data set.
* Good scalability with multi-nodes environment.
* High performance. Suitable for data warehouse and online transaction processing.
* Easy operations. DB provides both GUI and command lines and have same operations on Windows and Linux.

__References__

* http://www.360doc.com/content/13/1217/14/14919052_337866679.shtml

##FoundationDB
__Strengths__

* All features are free outside production. Production licensing terms essentially means it is currently free for user to use.
* Full ACID compliance.
* Has both consistency and availability during partitioning.
* Built in transaction retries.
* Excellent read performance on single reads. And range reads are only marginally slower.
* Transaction isolation level is serializable.
* Simple to scale horizontally.

__Weaknesses__  

* Weak .NET support. Little .NET documentation and support. .NET is not considered first class citizen of FoundationDB.
* Constraints on deployment - cannot be deployed in IIS, must be self-hosted - loss of IIS specific features such as graceful request handling, automatic app pool recycles/mem management.
* Cannot run in multiple AppDomains on same process.
* No nice 'management' interface - you need to roll your own admin tool.

__References__
* http://pauldevenney.blogspot.com/2014/07/pros-and-cons-comparing-ravendb-and.html

##Google App Engine
__Strengths__
* Handle irregular traffic load.
* Quick to get started.
* Free quota.
* Automatic CDN.
* Lot of Google services.
* No server maintenance.
* Use Google high speed network.
* SDK and languages.

__Weaknesses__

* No multithreading.
* 30 second per request.
* Expensive for constant load.
* Free quota is tricky.
* Not task intensive.
* Locked to App Engine.
* It’s not a “standard” server (PaaS).

__References__

* http://doduck.com/gae-pros-and-cons/

##Google Cloud Datastore
__Strengths__

* Automatically scales to data size and access patterns.
* Users cannot specify for a read to be consistent but can force consistency by structuring the entities in a certain way.

__Weaknesses__

* Documentation and language support is not very uniform.

__References__

* http://stackoverflow.com/questions/19750404/what-are-the-pros-and-cons-of-dynamodb-with-respect-to-google-cloud-datastore

##Hadoop

__Strengths__

* High reliability.
* High Scalability.
* High efficiency.
* Excellent fault-tolerant performance. 

__Weaknesses__

* Not suitable for data access with low latency requirement.
* Can not efficiently store a large amount of small-size files.
* Does not support multi-user write operation.
* Does not support modifying files randomly.

__References__

* http://zhidao.baidu.com/link?url=zhWI9P0RNe21-mq-rlbgtCyFj2SEZdW8qMWFIDMR46ZKEHBdQTBqLwePT3Kbrh3bHWFaQl_t2n1Y1vHR5CRoDKys2TeA8fPNWr022cxQLCW

##HBase

__Strengths__

* Built-in versioning.
* Strong consistency at the record level.
* Provides RDBMS-like triggers and stored procedures through coprocessors.
* Built on tried-and-true Hadoop technologies.
* Active development community.
* Free, open source under the Apache License version 2.0.

__Weaknesses__

* Lacks a friendly, SQL-like query language.
* Lots of moving parts.
* Setup beyond a single-node development cluster can be difficult.
* Requires Java SE version 6

__References__

* http://www.infoworld.com/article/2610709/database/review--hbase-is-massively-scalable----and-hugely-complex.html

##HPCC
__Strengths__

* Highly optimized language and compiler.
* Easy to develop data-centric language.
* Highly productive integrated development environment (IDE).
* Enterprise-class support.
* Runs on commodity hardware.
* Inbuilt auditing, monitoring and workflow.
* Battle tested.

__References__

* http://blog.163.com/li_hx/blog/static/1839914132011645120424/

##Hyperdex
__Strengths__

* HyperDex's replication and fault-tolerance guarantees have deep roots in the distributed systems literature.
* This solid foundation makes it much easier to converge to a solid implementation than ad-hoc solutions.
* HyperDex Warp provides cross-object transactions (even for documents).
* Users can atomically and safely modify multiple objects, as if they are the only thread accessing the database.

__Weaknesses__

* HyperDex's document storage is relatively new.

__References__

* http://www.reddit.com/r/programming/comments/2byle1/hyperdex_the_next_generation_keyvaluedocument/

##Hypertable
__Strengths__

* Quick 
* Handles heterogeneous data well.Different rows can have different columns.
* Can manage distributed data by Map/Reduce.
* Scales nicely.
* Easy to Install.

__Weaknesses__

* GPL License.
* Documents are weak.
* HQL works for simple queries only.
* Limit of 255 column families.

__References__

* https://trac.openmicroscopy.org.uk/ome/raw-attachment/wiki/WorkPlan/AlternativeStorageMongoDB/AlternativeStorage.pptx

##Impala
__Strengths__

* Support two kinds of JOIN: broadcast join and partition join.
* Data transmission between tasks is realized by PUSH method, which can reduce the pressure of the network and improve the efficiency.
* Support slow query function in version later than Cloudera Manager 4.6.
* Impala can use data on disks directly without HDFS.

__Weaknesses__

* Impala does not support sorting by column like GROUP BY.
* Currently does not support UDF.
* Does not support Serializer/Deserializer such as Hive.
* Does not support fault tolerance. If any node in the query has mistake, Impala will discard this query.
* Security issue. The data transmitted on Impala is not be encrypted.

__References__

* http://yanbohappy.sinaapp.com/?tag=tez

##Informix

__Strengths__

* Relatoinal database supporting SQL.
* A major commercial database product in Unix environment.

__References__

* http://wenku.baidu.com/link?url=jviP4jxXEWqGvQLGCDp4EfE-SHTzInzXuR30HMStePvlhAdlUTdWX9_4A0vjU7NB2O95lif2h2az0QzXmPKO_LS1KILzqBiLGvp3e2m1FT_

##Infinite Graph

__Strengths__

* Support a tool set to realize data visualization.
* Support node with multiple classes.
* The key-value struct can be mapped to member variables in InfiniteGraph.

__Weaknesses__

* Configuration is complex.
* Since objects can be either vertex or edge, when processing a hugh graphical structure, the performance may be influenced.

__References__

* http://tech.it168.com/a2012/0112/1302/000001302117_all.shtml

##IBM Big SQL
__Strengths__

* Provide a standard query interface: InfoSphere BigInsights.
* Provide SQL users a familiar method to use the big data storage environment.

__Weaknesses__

* Since the concurrency is realized by Hadoop's Map/Reduce structure, for specific queries, the cost of Map/Reduce may exceed the benefit of concurrency.

__References__

* http://www.ibm.com/developerworks/cn/data/library/bd-bigsql/index.html

##Microsoft HDInsight
__Strengths__

* Easy to get started.
* Windows-based.
* .NET code MapReduce functions.
* Awesome SDK.
* Pretty UI.

__Weaknesses__

* Slow, especially on the default 3 nodes.
* UI obscures Hadoop and HDFS functionality.
* Incomplete documentation.
* Still in preview stage.

__References__

* http://picnicerror.net/data-and-analysis/hands-on-hadoop-hdinsight-2013-03-07/

##Microsoft SQL Server
__Strengths__

* Easy query by SQL.
* Easy operation method.
* Provide a GUI.

__Weaknesses__

* Only run on Windows OS.
* Reliability, scalability and security are limited due to the limitation of runnable OS.
* Limited performance in multiple users situation.

__References__

* http://www.360doc.com/content/13/1217/14/14919052_337866679.shtml

##MapReduce

__Strengths__

* Simple and easy to use.
* Flexible.
* Independent of the storage.
* Fault tolerance.
* High scalability

__Weaknesses__

* No high-level language.
* No schema and no index.
* A Single ﬁxed dataﬂow.
* Low efficiency.

__References__

* Parallel Data Processing with MapReduce: A Survey. Kyong-Ha Lee, Hyunsik Choi, Bongki Moon.
* http://www.cs.arizona.edu/~bkmoon/papers/sigmodrec11.pdf


##Memcached
__Strengths__

* Low complexity.
* Simple to configure.
* Few command macros means simple to master.
* Atomic increment and decrement.
* Simple to cluster - uses a hashing algorithm at the client to find keys in a cluster.
* Memcached requires a nuclear strike to fall over.
* Can withstand a member dying.
* Many years in production.
* Every programming language has a memcached library.

__Weaknesses__

* Doesn't do anything besides be an in-memory key/value store.
* Caches sharded by client do not scale across AWS zones.
* Unbalanced memcached clusters require a full system restart.
* Adding a member to the pool requires reconfiguring and rebooting the client.

__References__

* http://www.bigdatalittlegeek.com/blog/2014/3/25/memcached-vs-redis

##MongoDB
__Strengths__

* It has bindings to numerous languages (C++, C#, Java, Python, ...). 
* Allows storage, indexing, linking of any user data.
* Annotations are now very easy, efficient.
* Has mechanisms for schema upgrade.
* Dynamic Queries.
* Replication.
* Sharding.
* Map-Reduce framework.
* Fast.
* GridFS is a distributed file storage mechanism within Mongo.
* Easy to install.

__Weaknesses__

* Schemaless, data integrity will need to be worked on.
* Graph structures not inherently supported.

__References__

* https://trac.openmicroscopy.org.uk/ome/raw-attachment/wiki/WorkPlan/AlternativeStorageMongoDB/AlternativeStorage.pptx

##MySQL
__Strengths__

* Free of cost.
* Light weight, easy installation and configuration.
* Open source C/S structure.
* Support multi-threading.
* Support many APIs.
* Support connection between different database platforms.
* Internationalization.

__Weaknesses__

* Got a few stability issues.
* Suffers from relatively poor performance scaling.
* Development is not community driven, and hence has lagged.
* Its functionality tends to be heavily dependant on add-ons.

__References__

* http://wenku.baidu.com/link?url=jviP4jxXEWqGvQLGCDp4EfE-SHTzInzXuR30HMStePvlhAdlUTdWX9_4A0vjU7NB2O95lif2h2az0QzXmPKO_LS1KILzqBiLGvp3e2m1FT_
* https://www.datarealm.com/blog/five-advantages-disadvantages-of-mysql/

##MapR
__Strengths__

* Easy installation and configuration.
* Dependable. Good stability.
* Fast speed.

__References__

* http://answers.mapr.com/questions/2854/what-are-the-pros-and-cons-of-using-mapr.html

##MemSQL
__Strengths__

* Blazing fast speed.
* Users can use all the MySQL client tools out there. Also because it uses MySQL, troubleshooting might not be an issue because it isn’t a new product.

__Weaknesses__

* Huge cache folder.
* After restoring the database (15Mb) MemSQL creates a folder in the plan cache folder which is.5GB. So performance comes with a price.
* Unable to create users in Developer Edition.

__References__

* http://manuel.manuelles.nl/blog/2012/06/20/taking-memsql-for-a-spin/

##Neo4j

__Strengths__

* Can be used as either built-in database or individual server.
* Provide widely REST interface.
* Can be integrated into environment based on PHP\.NET\JavaScript.
* Data structure is not necessary, which can simplify mode changing and data migration.
* Good scalability.

__Weaknesses__

* It is complex to creat index for new edges.
* Vertex can have multiple objects, which make the data structure more complicated.

__References__

* http://www.infoq.com/cn/articles/graph-nosql-neo4j
* http://tech.it168.com/a2012/0112/1302/000001302117_all.shtml

##Oracle
__Strengths__

* Can be running on most major platforms, including Windows.
* Completely support all industry standards.
* Adopt an open strategy. Allow clients to choose best technical solution.
* Suuport solutions with high availability and high scalability.
* Highest Performance. Keep the TPC-D and TPC-C world record on open source platforms.
* Support both GUI and commandline tool.
* Complete downward compatibility.
* Good security.

__References__

* http://www.360doc.com/content/13/1217/14/14919052_337866679.shtml

##Oracle TimesTen
__Strengths__

* Fast, consistent response time.
* High transaction throughput.
* Standard SQL, no application rewrite.
* Persistent and recoverable.
* High availability and no data loss.

__Weaknesses__

* Priced out of the reach of most people ($41,500.00 / Processor).

__References__

* http://stackoverflow.com/questions/1593987/alternative-to-the-timesten-in-memory-database

##Oracle Coherence

__Strengths__

* Coherence is ideal for scaling out read/write workloads.
* Coherence provides an object view of data (e.g. Java or .Net objects).

__Weaknesses__

* Coherence did not provide cross-partition atomicity before 3.6.
* Even starting with that, that functionality is severely limited compared to the non-transactional case.
* Coherence dynamically rebalances partitions upon nodes coming and going. 

__References__

* https://community.oracle.com/thread/2447944

##Oracle NoSQL
__Strengths__

* Ability to scale out compute and storage capacity horizontally over a wide range of hardware resources.
* Simple and fast queries.
* A flexible and simple approach to schema management.

__Weaknesses__

* Lack of support for complex queries.
* Lack of support for multitable joins.
* Limited transaction support.

__References__

* http://www.oracle.com/technetwork/issue-archive/2012/12-mar/o22interview-1512298.html

##PostgreSQL

__Strengths__

* Support a large amount of dat structures.
* Support transaction.
* Support sub query.
* Multiple version concurrency control.
* Data integrity check.

__References__

* http://wenku.baidu.com/link?url=jviP4jxXEWqGvQLGCDp4EfE-SHTzInzXuR30HMStePvlhAdlUTdWX9_4A0vjU7NB2O95lif2h2az0QzXmPKO_LS1KILzqBiLGvp3e2m1FT_

##RavenDB
__Strengths__

* Excellent .NET client API with extensibility points, providing easy developer learning curve.
* Designed as Document Store.
* Provides Index/Map/Reduce.
* Stores natively as JSON.
* Good Read Performance.
* Fits excellently into integration testing, due to in memory db option designed for testing.
* Automatically generates IDs for records.
* Well presented web based management studio.
* Provide a good console where users can see requests/response times and what indexes are used to resolve queries.

__Weaknesses__

* Cannot test replication, sharding or authenticated access functions without purchasing licenses and licenses are needed for anything other than development (UAT would need licenses).
* Some concerns over the dependence of the RavenDB project on one key developer.
* Some concerns about the robustness of the testing of the product and its unproven track record in enterprise solutions.
* Need to understand the “eventually consistent” model well when designing solutions.

__References__

* http://pauldevenney.blogspot.com/2014/07/pros-and-cons-comparing-ravendb-and.html

##Redis
__Strengths__

* Stores data in a variety of formats: list, array, sets and sorted sets.
* Pipelining multiple commands at once.
* Blocking reads - will sit and wait until another process writes data to the cache.
* Mass insertion of data to prime a cache.
* Partitions data across multiple redis instances.
* Can back data to disk.

__Weaknesses__

* Super complex to configure - requires consideration of data size to configure well.
* Master-slave architecture means if the master wipes out, and SENTINEL doesn't work, the system is sad.
* Lots of server administration for monitoring and partitioning and balancing.

__References__

* http://www.bigdatalittlegeek.com/blog/2014/3/25/memcached-vs-redis

##RethinkDB

__Strengths__

* RethinkDB really embraces the schema-less storage, and it shows throughout their API.

__Weaknesses__

* RethinkDB doesn't seem to have any support for cross-document transactions.

__References__

* http://www.reddit.com/r/programming/comments/2byle1/hyperdex_the_next_generation_keyvaluedocument/

##SAP Sybase ASE
__Strengths__

* Runnable on most major platforms, including Windows.
* Use DB Switch to support parallel servers.
* Good performances as SQL Server, better concurrency performance on Unix.
* Client/Server structure. Able to connect with network client using ODBC\Jconnect\Ct-library.
* Support both GUI and command line.
* Downward compatibility.

__Weaknesses__

* Since early version Sybase did not highly integrates with OS, there may be issues when running on multi-platform environment.
* DB Switch needs a server to be SWITCH, which may take in some hardware issues.
* CT-library is difficult to transplant.

__References__

* http://www.360doc.com/content/13/1217/14/14919052_337866679.shtml

##Spark

__Strengths__

* Fast speed and rich features.
* Exists within a popular programming environment.
* Works on Hadoop.

__Weaknesses__

* Still Kind of Hard to Run.

__References__

* http://zh.hortonworks.com/blog/spark-data-science-case-study/

##SQLite
__Strengths__

* Free for any purpose.
* Does not rely on a server process to run.
* Easy installation and configuration.
* No client-server negotiation, accesses to the database are much faster (2-3 times faster than a MySQL database).
* SQLite is small.
* SQLite can handle files up to 2 terabytes in size.
* SQLite implements most of the SQL 92 standard. This means you can usually use standard and well known queries to access it.
* SQLite does not enforce datatype constraints.

__Weaknesses__

* Not all SQL queries and syntax are supported.
* SQLite is not suitable for projects which requires a lot of semi-simultaneous writing operations.
* Not suitable for big databases.
* Cannot handle heavy website traffic, hence only suitable for small or medium size websites.

__References__

* https://h3rald.com/articles/quick-overview-of-sqlite/

##XtremeData

__Strengths__

* XtremeData provides a massively parallel database engine for Big Data analytics.
* Designed to be data model and data placement agnostic, dbX enables rapid on-demand and self-service of Big Data analytics.

__References__

* http://sdn.sys-con.com/node/2877513

##Zettaset
__Strengths__

* Standards-based and designed to easily fit within existing enterprise security frameworks.
* Compatible with Apache-based Hadoop distributions including those from Hortonworks, Cloudera, MapR, Pivotal, Teradata, and IBM.
* Compatible with NoSQL distributions such as Cassandra and Couchbase.
* Optimized to minimize impact on database performance.
* Optimized for on-premises as well as cloud deployments.

__References__

* http://ibm.ulitzer.com/node/3127259
