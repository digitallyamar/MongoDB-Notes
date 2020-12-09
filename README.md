# MongoDB-Notes
Commands related to MongoDB

## Export MongoDB query to a CSV file
mongoexport --db DBName --collection CollectionName --fields Field1,Field2 --type=csv -q '{YOUR_QUERY}' --out Output.csv

Eg: mongoexport --db Namekarna --collection dom_dom --fields id,name --type=csv -q '{"available":true}'  --out filtered_output.csv
