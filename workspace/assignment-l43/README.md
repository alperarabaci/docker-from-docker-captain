# Dockerizing Sample Node JS App
# Create image using Dockerfile
docker build -t sample-node-app  .
# Run (used with --rm, it deletes container when container stop)
docker container run --rm -p 80:3000 --name nodeapp sample-node-app
# Send to repo: (https://hub.docker.com/u/alperarabaci)
docker image tag sample-node-app  alperarabaci/sample-node-app
docker image push alperarabaci/sample-node-app
# Find image id and delete local image
docker image ls
docker image rm -f 9db59ea37d
# Download and run app from docker hub
docker container run --rm -p 80:3000 --name node-app alperarabaci/sample-node-app
# It Worked! We All Deserve The Captain's Applause