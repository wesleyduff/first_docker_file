# First docker file 
This will load a create-react-app on a docker image to load and the container will run the react application on start.

## Volume
```javaScript
/var/www
```

### Commands
```javaScript

//https://app.pluralsight.com/player?course=docker-web-development&author=dan-wahlin&name=docker-web-development-m4&clip=7&mode=live

docker run -p 8080:3000 -v /var/www node

Customizing Volumes
- docker host
    - volum : /var/www
        - /src

docker run -p 8080:3000 -v $(pwd):/var/www -w "/var/www" node npm start

docker inspect <container-id>

Mounts ....

//remove container and its volum
docker rm -v <container-id first 3 or 4 characters>
```

