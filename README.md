Probably a bug in nginx's default.conf or likely in postgres
Fix that and docker-compose should run.

Update:
The problem is with the redis setup.

client, server, and redis services are
working fine, the routing thus with docker-compose is working.

Update 2:
After _actually_ debugging attempt(reading logs) it appears the env variables
passed to worker service were not set.
That's fixed, but postgres is down, probably same problem of env variables.
