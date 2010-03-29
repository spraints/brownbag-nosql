!SLIDE commandline incremental

## CouchDB

	$ curl -X PUT http://localhost:5984/test/
	{"ok":true}

	$ curl -X PUT -d '{"name": "Matt"}' http://localhost:5984/test/maburke
	{"ok":true,"id":"maburke",
	"rev":"1-47804390369d435cb116403da935bdd5"}

	$ curl http://localhost:5984/test/maburke
	{"_id":"maburke","_rev":"1-47804390369d435cb116403da935bdd5",
	"name":"Matt"}

!SLIDE

## CouchDB

	@@@ javascript
	{
	  "first_name": "Matt",
	  "employer": "SEP",
	  "hobbies": [
	    "programming",
	    "farming"
	  ]
	}

!SLIDE

## CouchDB

# _design/count

	@@@ javascript
	{
	  "language": "javascript",
	  "views": {
	    "by_hobby": {
	      "map":    //...
	      "reduce": //...
	    },
	    "by_name": {
	      // ...
	    },
	  }
	}

!SLIDE

## CouchDB
## _design/count
# by_hobby

	@@@ javascript
	"map": "function(doc) {
	  if(doc.hobbies) {
	    for(var i = 0; i < doc.hobbies.length; i++) {
	      emit(doc.hobbies[i], 1);
	    }
	  }
	}"

!SLIDE

## CouchDB
## _design/count
# by_hobby

	@@@ javascript
	"reduce": "function(keys, values) {
	  return sum(values);
	}"

!SLIDE

## CouchDB
# Cached map output

!SLIDE

## CouchDB
# Replication

!SLIDE

## CouchDB
# CouchApps

