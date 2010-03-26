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
* Document-oriented
* Column-oriented

!SLIDE
	@@@ sql
	select database_type, database_name
	from database_types t
	  join databases d
	  on d.database_type_id = t.id

!SLIDE full-page

![Visual guide to nosql systems](visual-guide-to-nosql-systems.png)

!SLIDE
# how to use some of these

!SLIDE commandline incremental

# Redis

	$ SET presentation:name "NOSQL Brown Bag"
	"OK"

	$ GET presentation:name
	"NOSQL Brown Bag"

!SLIDE commandline incremental

# Redis

	$ SET presentation:slides 1
	"OK"

	$ INCR presentation:slides
	2

!SLIDE commandline incremental

# Redis

	$ SET presentation:interesting true
	"OK"

	$ EXPIRE presentation:interesting 45
	"OK"

	$ TTL presentation:interesting
	37

!SLIDE bullets

# Redis

* List
* Set
* Sorted set
* <http://try.redis-db.com/>

!SLIDE

# CouchDB

	@@@ javascript
	{
	  "first_name": "Matt",
	  "employer": "SEP",
	  "hobbies": [
	    "programming",
	    "farming"
	  ]
	}

!SLIDE commandline incremental

# CouchDB

	$ curl -X PUT http://localhost:5984/test/
	{"ok":true}

	$ curl -X PUT -d '{"name": "Matt"}' http://localhost:5984/test/maburke
	{"ok":true,"id":"maburke",
	"rev":"1-47804390369d435cb116403da935bdd5"}

	$ curl http://localhost:5984/test/maburke
	{"_id":"maburke","_rev":"1-47804390369d435cb116403da935bdd5",
	"name":"Matt"}
	

!SLIDE

# CouchDB

	@@@ javascript

!SLIDE
# (mongo documents)

!SLIDE
# (mongo map-reduce)

!SLIDE
# (bigtable stuff)
