# dumprotate2
Simple database dump rotate system

# help
Usage: `dumprotate2 [-options]`<br />
where options include:
-	`-r | --rotate`		rotate counter (e.g: -r=10, default: 10)
-	`-c | --crondir`		cron directory, useful to store dump in different cron (e.g: -c=hourly, default: default)
-	`-o | --output`		output directory, location where dumps will be stored (e.g: -o=/home/dumps)
-	`-u | --dbuser`		database username
-	`-p | --dbpwd`		database password
-	`-d | --database`		dumps only a specific database
-	`-h | --help`		shows this help
