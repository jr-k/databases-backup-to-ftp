# dumprotate2
Simple database dump rotate system

# help
Usage: dumprotate2 [-options]
where options include:
	-r | --rotate		rotate counter (e.g: -r=10, default: 10)
	-c | --crondir		cron directory, useful when you want to store dump in many ways  (e.g: -c=hourly, default: default)
	-o | --output		output directory, location where all dumps will be stored (e.g: -o=/home/dumps, default: /home/dbdumps)
	-u | --dbuser		database username
	-p | --dbpwd		database password
	-d | --database		dumps only a specific database
	-h | --help		shows this help
