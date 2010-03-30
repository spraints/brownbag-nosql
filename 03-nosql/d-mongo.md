!SLIDE commandline incremental

# Mongo

	$ db.streets.save({"name": "116th", "traffic": "bad"})

	$ db.streets.find({"name": "116th"})
	{"_id" :  ObjectId( "4bb120d37e2b5a6e0477dd7b")  ,
	 "name" : "116th" ,
	 "traffic" : "bad"}

!SLIDE commandline incremental

# Mongo

	$ db.streets.save({"name": "116th", "traffic": "bad", "_id": ObjectId( "4bb120d37e2b5a6e0477dd7b"), "cities": ["Carmel", "Fishers"]})

	$ db.streets.save({"name": "96th", "traffic": "bad",  "cities": ["Carmel", "Fishers", "Indianapolis"]})

	$ db.streets.find({"cities": "Fishers"})
	{"_id" :  ObjectId( "4bb120d37e2b5a6e0477dd7b")  ,
	 "name" : "116th" ,
	 "traffic" : "bad" ,
	 "cities" : ["Carmel","Fishers"]}
	{"_id" :  ObjectId( "4bb1218f7e2b5a6e0477dd7c")  ,
	 "name" : "96th" ,
	 "traffic" : "bad" ,
	 "cities" : ["Carmel","Fishers","Indianapolis"]}

	$ db.streets.find({"cities": "Indianapolis"})
	{"_id" :  ObjectId( "4bb1218f7e2b5a6e0477dd7c")  ,
	 "name" : "96th" ,
	 "traffic" : "bad" ,
	 "cities" : ["Carmel","Fishers","Indianapolis"]}
