# dbtf
Simple database dump rotate system

# help
Usage: `dbtf [-options]`<br />
where options include:
-	`-r | --rotate`		rotate counter (e.g: -r=10, default: 10)
-	`-c | --crondir`		cron directory, useful to store dump in different cron (e.g: -c=hourly, default: default)
-	`-o | --output`		output directory, location where dumps will be stored (e.g: -o=/home/dumps)
-	`-n | --dbuser`		database username
-	`-p | --dbpwd`		database password
-	`-d | --database`		dumps only a specific database
-	`-u | --ftpuser`		ftp username
-	`-w | --ftppwd`		ftp password
-	`-s | --ftphost`		ftp host
-	`-t | --ftpport`		ftp port
-	`-h | --help`		shows this help

Crontab entries
- `* * * * * /usr/local/sbin/dbtf -r=60 -c="minutely1"`
- `*/5 * * * * /usr/local/sbin/dbtf -r=12 -c="minutely5"`
- `0 * * * * /usr/local/sbin/dbtf -r=24 -c="hourly"`
- `0 1 * * * /usr/local/sbin/dbtf -r=30 -c="daily"`
- `0 0 * * 0 /usr/local/sbin/dbtf -r=52 -c="weekly"`
- `0 0 1 * * /usr/local/sbin/dbtf -r=12 -c="monthly"`
