# docker-helpers
Usefull docker helpers

Stop and Remove all containers
```bash
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

Remove all containers with filter
```bash
docker ps -a | grep '<some_name>' | awk '{print $1}' | xargs --no-run-if-empty docker rm
```
