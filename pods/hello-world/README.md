```
docker build -t hello-kubernetes .
docker images
docker run -p 8080:8080 hello-kubernetes

docker login
docker tag hello-kubernetes <your-docker-username>/hello-kubernetes:latest
docker push <your-docker-username>/hello-kubernetes:latest
```
