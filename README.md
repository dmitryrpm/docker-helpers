# docker-helpers
Usefull docker helpers

Stop and Remove all containers
```bash
// stop all containers
docker stop $(docker ps -a -q)
// delete all containers
docker rm $(docker ps -a -q)
// delete all volumes
docker rmi $(docker images -a -q)
```

Remove all containers with filter
```bash
docker ps -a | grep '<some_name>' | awk '{print $1}' | xargs --no-run-if-empty docker rm

docker volume ls | grep '<some_name>' | awk '{print $2}' | xargs --no-run-if-empty docker volume rm
```
