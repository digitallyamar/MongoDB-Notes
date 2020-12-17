# MongoDB-Notes
Commands related to MongoDB

## Export MongoDB query to a CSV file
mongoexport --db DBName --collection CollectionName --fields Field1,Field2 --type=csv -q '{YOUR_QUERY}' --out Output.csv

Eg: mongoexport --db Namekarna --collection dom_dom --fields id,name --type=csv -q '{"available":true}'  --out filtered_output.csv

## Query to check MongoDB collection by date range in Robo3T
Eg: db.getCollection('domains_domain').find({'expiry_date':{ "$gte" : ISODate("2020-12-16T00:00:00Z"), "$lt" : ISODate("2020-12-31T00:00:00Z") }})

## Query MongoDB to check for string containing pattern
Eg: db.getCollection('domains').find({'expiry_date':{$regex:'2020-12-15T*'}})

## Query to find total no. of documents in a collection
Eg: db.getCollection('domains_domain').find({}).count()
