# Docker

Docker is a virtualisation software that allows you to define and run virtual machines with pre-loaded user code.

*Images* are the specification and data associated with a virtual machine.

*Containers* are running instances of virtual machines


## How To

In order to build, run and push docker images follow the instructions below. Start by opening a terminal (with admin privileges in Windows) and ensuring docker is running.

### Create a new docker image

Create a projec folder and create a `Dockerfile`.

Inside the docker project folder, execute the following command.

```
docker build -t <tag> -f <docker file> .
```

**-t** tags the image with a name. **-f** lets you specify the path to the Dockerfile, which is handy if the file is not called Dockerfile (e.g. with version names) or not in the root folder of the project folder.

**For Example** navigate to this file's folder and execute the command below to build a docker image.

```
docker build -t mujoco -f mujoco_dockerfile .
```

### Run a docker image inside a container in interactive mode

```
docker run --interactive --rm sstein2/lighton_idi:1.0.3
```

You may want to run a jupyter server inside a docker container and connect to it from the host machine.

```
docker run --gpu all -it -p 8888:8888 --rm octopus
```
Inside the container:
```
jupyter-lab --ip 0.0.0.0 --no-browser
```
In the host browser
[http://localhost:8888/lab]()

### upload a new docker image
docker push sstein2/lighton_idi:1.0.3
