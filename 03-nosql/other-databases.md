!SLIDE
	@@@ sql
	select d.database_name
	from databases d
	  join database_types t
	  on t.id = d.database_type_id
	where t.database_type <> 'Relational'

!SLIDE
	@@@ sql
	select database_type
	from database_types

!SLIDE bullets incremental

# Database types #

* Key-value
* Column-oriented
* Document-oriented

!SLIDE

![Visual guide to nosql systems](visual-guide-to-nosql-systems.png)

!SLIDE

# TODO: key-value store examples
* redis
* memcached
* ???

!SLIDE

# TODO: document database
* couchdb
* mongodb
* riak
