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
