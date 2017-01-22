# coredns-docker
A minimalistic Docker image for CoreDNS (https://coredns.io/).

This image is packaged with a sample configuration file (`Corefile`) which forwards all queries to `8.8.8.8` and logs them to stdout.

## Run a Container

**Sample Corefile**
```
$ docker run -p 53:53 -p 53:53/udp blachniet/coredns
```

**Custom Corefile**
```
$ docker run -p 53:53 -p 53:53/udp \
    -v $HOME/coredns/Corefile:/etc/coredns/Corefile
    blachniet/coredns
```