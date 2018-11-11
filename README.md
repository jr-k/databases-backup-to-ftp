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

Crontab entries
#* * * * * /usr/local/sbin/dumprotate2 -r=3 -c="minutely1"
*/5 * * * * /usr/local/sbin/dumprotate2 -r=12 -c="minutely5"
0 * * * * /usr/local/sbin/dumprotate2 -r=24 -c="hourly"
0 1 * * * /usr/local/sbin/dumprotate2 -r=30 -c="daily"
0 0 * * 0 /usr/local/sbin/dumprotate2 -r=52 -c="weekly"
0 0 1 * * /usr/local/sbin/dumprotate2 -r=12 -c="monthly"
