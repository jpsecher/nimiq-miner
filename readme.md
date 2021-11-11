# Docker container for stand-alone Nimiq miner

This is a [Nimiq](https://nimiq.com) cryptocurrency miner.  Run it like

    $ docker run -d \
        --name nimiq-miner \
        --mount 'type=volume,source=nimiq-miner,destination=/home/nimiq' \
        jpsecher/nimiq-miner \
        --pool=pool.acemining.co:8443 \
        --wallet-address=NQ6272GHCS6H3XL5L09SFGAM34MK7CU11JFE

Or start it with `docker-compose up -d`:

    version: "3"
    services:
      nimiq-miner:
        image: jpsecher/nimiq-miner
        command: --wallet-address=NQ6272GHCS6H3XL5L09SFGAM34MK7CU11JFE
        volumes:
          - nimiq-miner:/home/nimiq
        restart: on-failure
    volumes:
      nimiq-miner:

Of course, you need to replace the wallet with your own (but you are welcome to use mine ;-), and maybe change the pool if you fancy a different one, or simply go solo and leave out the pool argument.

You will then have a running Nimiq miner that uses all the available resources for mining.

To see the output from the miner, run one of:

    $ docker logs -t -f nimiq-miner
    $ docker-compose logs

To update the miner:

    $ docker stop nimiq-miner
    $ docker rm nimiq-miner
    $ docker pull jpsecher/nimiq-miner
    $ docker run -d --mount ... (like above) ...

or

    $ docker-compose stop
    $ docker-compose pull
    $ docker-compose up -d

## Build container

    $ cd src/miner
    $ docker build -t jpsecher/nimiq-miner .

----

[![Docker build status](https://img.shields.io/docker/cloud/build/jpsecher/nimiq-miner.svg)](https://hub.docker.com/r/jpsecher/nimiq-miner/builds/)
