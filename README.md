# Minified CMet GTFS

Lisbon's Carris Metropolitana GTFS, minified and compatibility-enhanced, per the following process:

* Removed commas from long route names to avoid compatibility issues with legacy CSV parsers
* Minified using `gtfs-tidy`: 
  * `gtfstidy -neOzscmACSPIW --fix --standard-route-types --explicit-calendar`
  * Contains -50% shape points, -76% calendar_date entries (converted to calendar.txt), -99.5% services (duplicates)
* Compressed with zip level 9
* Total size is approx. -40% of original after compression
