# docker-iperf3

## Introduction

The repository contains a simple docker container that runs IPerf3.

## How to run

By default, the container listens on port 5201.

```shell
docker run -p 5201:5201 ghcr.io/l13t/iperf3:latest
```

If you want to enable authorization on your in your setup, you need to perform the following steps:

1. generate a file that contains credentials
1. run container and mount credentials file into it

    ```shell
    docker run -p 5201:5201 -v <path_to_auth_file>:/auth_file ghcr.io/l13t/iperf3:latest --authorized-users-path file /auth_file
    ```
