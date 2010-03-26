!SLIDE
	@@@ sql
	select *
	from dbms

!SLIDE

<object data="image/02-relational/relational_database_terms.svg" type="text/svg+xml" width="984" height="460"></iframe>

!SLIDE
	@@@ sql
	select database_name
	from dbms
	where is_relational = 1

!SLIDE
	@@@ sql
	select d.database_name
	from dbms d
	  join database_types t
	  on t.id = d.database_type_id
	where t.database_type = 'Relational'
