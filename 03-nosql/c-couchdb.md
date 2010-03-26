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
