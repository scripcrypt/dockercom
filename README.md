Stops all processes in the docker container, deletes all images, and deletes all objects.<br>
A script that prepares you to stop the all docker container, delete the image, delete the object and start over　'dockre compose' from scratch.<br>
This script doesn't do much at all.<br>
The main usage is as follows.<br><br>

[all processes in the docker container, deletes all images]<br>
xxx$ dockercom remove<br><br>

[Show all running docker processes instead of "docker ps"]<br>
xxx$ dockercom process<br>
...'process' can be 'proc','ps'<br><br>

[Show all running docker container images instead of "docker images"]<br>
xxx$ dockercom images<br><br>

[Show all running docker processes and docker container instead of "docker ps" and "docker images"]<br>
xxx$ dockercom show<br><br>

[Stop all running docker processes instead of "docker stop 08787c23235f cf5a85818448 727a67ae4d69 a30d898a3704"]<br>
xxx$ dockercom stop<br><br>

[Stop all running docker processes,remove all container images,and all docker images]<br>
xxx$ dockercom remove<br><br>

You can also use this script and commands to stop or delete the docker container without using this script.<br>
'dockercom help'<br>
I made it so that you can see it at.<br><br>

'dockercom help'<br>
The displayed contents of are as follows.<br>
<pre>Usage:	dockercom [ACTIONS] TARGET<br>
  ACTIONS:
    process     show running docker process list. [ailias] proc,ps
    images      show docker container images.
    show        show process and container images.
    stop        stop docker container process.
    remove      stop docker images and or docker object.
                TARGET:<br>
                  images        remove docker container images.
                  object        remove docker container object.
                  all or none   remove both container images and container object.

  Run 'dockercom help' for this.

  docker command usages...
       run docker process      docker compose up -d  [docker-compose up -d --build]
       show docker process     docker ps
       login docker container  docker exec -it docker_web_1 bash
       stop docker process     docker stop 08787c23235f cf5a85818448
       show docker images      docker images
       remove docker images    docker image rm -f 727a67ae4d69 a30d898a3704
       remove docker objects   docker system prune -a</pre>

All licenses are waived, so feel free to use them.
