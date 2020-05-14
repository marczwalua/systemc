# systemc on Docker
This repository contains an a dockerfile in order to run systemc. It contains systemc 2.3.3 and systemc 2.3 ams. The only thing you need for this is this repository and a working installation of docker.

On default, the docker command in run_docker.sh mounts a volume with the folder srcfiles. This is not a necessary step, but can make life easier.

# How to install docker?
[install](https://docs.docker.com/engine/install/)

# How to build the docker container
```
docker build . -t systemc
```

# How to run docker with all the fun?
```
docker run \
  -ti \
  --rm \
  -v "$(pwd)"/srcfiles/:/usr/srcfile/ \
  systemc
```

# Important locations
Systemc is installed in:      /usr/local/systemc-2.3.3
Systemc ams is installed in:  /usr/local/systemc-ams-2.3
Mounted volume:               /usr/srcfile/
