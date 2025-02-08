# Docker Image Creation and Run docker container to expose outside world

## Build docker image

docker build --network host -t "dockerhubreponame/image_name:tag" .

## Push docker image to docker hub ( We can use ECR also )

docker push "dockerhubreponame/image_name:tag"

## Create simple container and expose it on port 80

docker -it -d --name="container-name" -p "localhost-port:container-port" "image_name"

EX:

docker run -it -d --name simple-py-con -p 80:80 gowtham904/simple-python-app:v1

