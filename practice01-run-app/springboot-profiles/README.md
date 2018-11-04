# Start my first app on kubernetes

### Build the project
```
gradle clean build
```

### Build docker image
```
docker build -t springboot-profiles:1.0 .
```

By default, Docker will create images and store them in your local machine’s Docker registry.
In this tutorial, we will not use your local machine’s Docker registry; we will use the Docker registry of the Docker daemon running inside Minikube’s vm instance. To point the ‘docker’ command to your Minikube’s Docker daemon, type (unix shells):

```
eval $(minikube docker-env)
```

Note: Later, when you no longer wish to use the Minikube host, you can undo this change by running eval ```$(minikube docker-env -u)```.

Build your Docker image, using the Minikube Docker daemon (mind the trailing dot):
```
docker build -t springboot-profiles:1.0 .
```
check that the image is in Minikube’s Docker registry:
```
minikube ssh docker images
```

### Create a deployment



