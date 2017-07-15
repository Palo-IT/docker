DOCKER
======

This project give you the possibility to create base image for your application.
You can build and push on the paloIT 's docker registry.
The idea is to create template from each system and shared with the paloIT community. You can version each image.

**FUNCTIONALITY**

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

**COMMAND IN SHELL TO TEST CONTAINER**

RUNNING_CONTAINER=$(docker inspect --format="{{.State.Running}}" YOUR_CONTAINER_NAME 2> /dev/null)
if [ "$RUNNING_CONTAINER" == "true" ]; then
  .....
fi

**COMMAND CLEAN RAM**

- use memory in real time
  - watch -n 1 free -m
  - watch -n 1 cat /proc/meminfo

- clean memory not used
  - sudo sysctl -w vm.drop_caches=3
  - sudo sync && echo 3 | sudo tee /proc/sys/vm/drop_caches
  
**DOCKER BASH COMPLETION**

See page https://docs.docker.com/compose/completion/

  - **on linux:** 
  
        curl -L https://raw.githubusercontent.com/docker/docker-ce/master/components/cli/contrib/completion/bash/docker > /etc/bash_completion.d/docker
        curl -L https://raw.githubusercontent.com/docker/compose/master/contrib/completion/bash/docker-compose > /etc/bash_completion.d/docker-compose
      
  - **on mac:**
  
    **BREW**
    
    brew install bash-completion
    
    edit ~/.bash_profile or ~/.profile:
       
        if [ -f $(brew --prefix)/etc/bash_completion ]; then
        . $(brew --prefix)/etc/bash_completion
        fi
        
    **MACPORTS**
        
     sudo port install bash-completion
        
     edit ~/.bash_profile or ~/.profile:
     
        if [ -f /opt/local/etc/profile.d/bash_completion.sh ]; then
            . /opt/local/etc/profile.d/bash_completion.sh
        fi
    
    **ADD COMPLETION FILE**
    
        curl -L https://raw.githubusercontent.com/docker/docker-ce/master/components/cli/contrib/completion/bash/docker > `brew --prefix`/etc/bash_completion.d/docker   
        curl -L https://raw.githubusercontent.com/docker/compose/master/contrib/completion/bash/docker-compose >`brew --prefix`/etc/bash_completion.d/docker-compose
     
     Open a new terminal or make source ~/.bash_profile or ~/.profile
  
**SED COMMAND ON MAC**
  
Use GNU SED from brew
  
  - install brew: /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  - install gsed: brew install gnu-sed --with-default-names
  - uninstall gsed: brew uninstall gnu-sed
  