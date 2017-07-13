DOCKER
======

**Functionality**

- docker images
- docker rmi {id or image name}
- docker rm {id or container name} 
- docker ps -a (show all container)
- docker ps (show alive container)
- docker network ls (show all network)
- docker network rm {network name} (remove a network)
- docker stats $(docker ps --format={{.Names}}) (show stats by container name)
- docker inspect --format="{{.State.Running}}" YOUR_CONTAINER_NAME (test if container running)
- docker volume ls -f dangling=true -f driver=local -q | xargs -r docker volume rm (rm all useless volume, be carefull with flocker driver)
- docker rmi $(docker images | grep "^<none>" | awk "{print $3}") (rm all untagged images)
- docker rmi $(docker images -a --filter=dangling=true -q) (clean all dangling images)

COMMAND IN SHELL TO TEST CONTAINER
==================================
RUNNING_CONTAINER=$(docker inspect --format="{{.State.Running}}" YOUR_CONTAINER_NAME 2> /dev/null)
if [ "$RUNNING_CONTAINER" == "true" ]; then
  .....
fi

COMMAND CLEAN RAM
=================

- use memory in real time
  - watch -n 1 free -m
  - watch -n 1 cat /proc/meminfo

- clean memory not used
  - sudo sysctl -w vm.drop_caches=3
  - sudo sync && echo 3 | sudo tee /proc/sys/vm/drop_caches