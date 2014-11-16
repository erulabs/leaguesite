leaguesite
==========

A League site by the MumbleSchool!

How to develop on windows!
=======
Install boot2docker for windows

In Git Shell:

To start and connect to the Docker manager:

    boot2docker.exe up

    boot2docker.exe ssh


To Remember the IP of the docker server:

    boot2docker.exe ip


Once you're connected - you can use docker normally - to start the app:

    cd /Users/WHEREEVER/leaguesite
    docker run -p 8080:80 -v /Users/Documents/leaguesite/:/var/www/site -d leaguesite


You'll need to built the image "leaguesite" at least once, but the error from above will tell you that. To build the image, just:

   docker build -t leaguesite .

Then run the "docker run" above - Make sure to connect the proper path (User/Documents...) so that docker can read your local files!

Finally, browse to the server!

    http://DOCKER_SERVER_IP:8080