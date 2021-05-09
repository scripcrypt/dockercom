Stops all processes in the docker container, deletes all images, and deletes all objects.<br>
A script that prepares you to stop the all docker container, delete the image, delete the object and start over　'docker compose'　from scratch.<br>
straightforwardly this script doesn't do much at all.<br><br>

This script uses PHP, so it is assumed that PHP is included in your environment.<br>
Make sure the PHP path on the first line of this script matches your environment.<br>
You can check if PHP is included in your environment and what the path is with the following command.<br><br>

xxx$ <b>which php</b><br>
xxx$ /bin/php

You see '#!/usr/bin/php' on first line.<br>
Replace the path on this first line with the path shown in'which php'.<br><br>

The main usage is as follows.<br><br>

[all processes in the docker container, deletes all images]<br>
xxx$ <b>dockercom remove</b><br><br>

[Show all running docker processes instead of "docker ps"]<br>
xxx$ <b>dockercom process</b><br>
...'process' can be 'proc','ps'<br><br>

[Show all running docker container images instead of "docker images"]<br>
xxx$ <b>dockercom images</b><br><br>

[Show all running docker processes and docker container instead of "docker ps" and "docker images"]<br>
xxx$ <b>dockercom show</b><br><br>

[Stop all running docker processes instead of "docker stop 08787c23235f cf5a85818448 727a67ae4d69 a30d898a3704"]<br>
xxx$ <b>dockercom stop</b><br><br>

[Stop all running docker processes,remove all container images,and all docker images]<br>
xxx$ <b>dockercom remove</b><br><br>

I tried to display how to use and simple usage of <b>docker</b> command with 'dockercom help'.<br><br>
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
