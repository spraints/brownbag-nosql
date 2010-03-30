!SLIDE
	@@@ sql
	select d.database_name
	from dbms d
	  join database_types t
	  on t.id = d.database_type_id
	where t.database_type <> 'Relational'

!SLIDE
	@@@ sql
	select database_type
	from database_types

!SLIDE bullets

# Database types #

* Key-value
* Column-oriented <!-- common for OLAP or data warehouses, stores columns first instead of rows -->
* Document-oriented
* Graph

!SLIDE
	@@@ sql
	select database_type, database_name
	from database_types t
	  join dbms d
	  on d.database_type_id = t.id

!SLIDE full-page

![Visual guide to nosql systems](visual-guide-to-nosql-systems.png)

<!--
 RDBMS
 Aster Data - map reduce
 Greenplum
 Vertica - data warehousing

 Dynamo - amazon
 Voldemort - open source version of Dynamo
 Tokyo Cabinet
 KAI
 Cassandra - facebook
 SimpleDB
 CouchDB
 Riak - Basho, highly scalable

 BigTable - Google AppEngine data store
 Hypertable - OSS clone of BigTable
 Hbase - hadoop data store
 MongoDB - from 10gen
 Terrastore - based on Terracotta
 Scalaris - from Zuse Institute Berlin and onScale solutions in Europe
 Berkeley DB - 1990ish
 MemcacheDB - persistence for memcache
 Redis - open source
-->
