# docker-helpers
Usefull docker helpers

Remove all containers
```bash
docker rm $(docker ps -a -q)
```

Remove all containers with filter
```bash
docker ps --all | grep '<some_name>' | awk '{print $1}' | xargs --no-run-if-empty docker rm
```
