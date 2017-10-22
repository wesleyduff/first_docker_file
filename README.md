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

### Docker file 
Examples: 
- From : antoher image : usually node
    - from : node
- maintainer : name
- Run : Like apt-get or something like that
    - npm install 
- copy : when ready for prod. put sorce code in container
    - copy: ./var/www : example 
- entrypoint : main entrypoint to kick off a cointainer : Like : npm start
- workdir : working dir
    - /var/www
- expose : port
    - expose: 8080
- env : variables
- volum : volum of code


### Docker Build
- contains build instructions

```javaScript
docker build -t <your username>/node .

or if you have a diff. name for docker file
docker build -f <name of file> -t wesduff/node .

```

### Communicate between containers
Container linking
- legacy linking
    - link one container to another container
- Contaienr Linking

_Bridge Network (Container Network)_
- node 
- mongo



