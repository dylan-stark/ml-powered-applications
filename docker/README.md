# Docker

Build a new image with

```
cd ml-powered-applications
docker build -t mlpowered/tensorflow:latest-py3-jupyter -f docker/Dockerfile .
```

This will take some time to pull the base image, install all of the dependencies, and download the required data sets.

Start up an instance of Jupyter to work with

```
docker run -u $(id -u):$(id -g) -it -p 8888:8888 -v ${PWD}:/ml-powered-applications mlpowered/tensorflow:latest-py3-jupyter
```

You should now be able to run all of the notebooks
