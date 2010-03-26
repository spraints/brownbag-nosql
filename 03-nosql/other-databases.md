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

# should this be used in place of the other slides?

!SLIDE
# how to use some of these

!SLIDE
# (redis commands)

!SLIDE
# (couch documents)

!SLIDE
# (couch design documents)

!SLIDE
# (mongo documents)

!SLIDE
# (mongo map-reduce)

!SLIDE
# (bigtable stuff)
