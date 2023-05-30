In order to build, run and push docker images follow the instructions below. Start by opening a terminal (with admin privileges in Windows) and ensuring docker is running.

# build a new docker image

docker build -t sstein2/lighton_idi:<version>-<tag> -f <Dockerfile> .

example:
docker build -t sstein2/lighton_idi:1.0.3 -f Dockerfile_1.0.3 .

# run a docker image in interactive mode
docker run --interactive --rm sstein2/lighton_idi:1.0.3

# upload a new docker image
docker push sstein2/lighton_idi:1.0.3
