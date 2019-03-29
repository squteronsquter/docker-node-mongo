# ERRORS WHICH MIGHT ARISE

for local port 80 you might get an error while running

docker-compose up

or

docker-compose up -d

eg. valet is running nginx on that port or ngnx is running inside another docker container which is still running

than just change the port to 8080 or 8081 or 8083

whichever is free!

Inside docker-compose.yml
...

    ports:
      - '8083:3000'

...

http://localhost:8083/

This code comes from a YouTube tutorial by Brad Traversy:

https://www.youtube.com/watch?v=hP77Rua1E0c

and his Github:

https://github.com/bradtraversy/docker-node-mongo

Stop the container

docker-compose down
