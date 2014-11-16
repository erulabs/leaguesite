leaguesite
==========

A League site by the MumbleSchool!

How to develop on Linux/OSX
=======
    cd repoDir/
    docker build -t leaguesite .
    docker run -p 8080:80 -v `pwd`:/var/www/site -d leaguesite

Keep in mind you only need to run "build" once, or when the Dockerfile changes.

How to develop on windows!
=======
Read: http://docs.docker.com/installation/windows/
Install boot2docker for windows

To start and connect to the Docker manager:

    boot2docker up
    boot2docker ssh

To Remember the IP of the docker server:

    boot2docker ip

Once you're connected - you can use docker normally - to start the app, enter your user's directory:

    cd /c/Users/WHEREEVER/leaguesite
    docker build -t leaguesite .
    docker run -p 8080:80 -v /c/Users/USER/Documents/leaguesite/:/var/www/site -d leaguesite

Keep in mind you only need to run "build" once, or when the Dockerfile changes.
Finally, browse to the server!

    http://DOCKER_SERVER_IP:8080