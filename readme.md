# Docker container for stand-alone Nimiq miner

This is a [Nimiq](https://nimiq.com) cryptocurrency miner.  Run it like

    $ docker run -d \
        --name nimiq-miner-1.5.0 \
        --mount 'type=volume,source=nimiq-miner,destination=/home/nimiq' \
        jpsecher/nimiq-miner \
        --pool=eu.nimpool.io:8444 \
        --wallet-address=NQ6272GHCS6H3XL5L09SFGAM34MK7CU11JFE

Of course, you need to replace the wallet with your own (but you are welcome to use mine ;-), and maybe change the pool if you fancy a different one, or simply go solo and leave out the pool argument.

You will then have a running Nimiq miner that uses all the available resources for mining.

To see the output from the miner, run

    $ docker logs -t -f myminer

To stop the miner:

    $ docker stop myminer

To restart the miner:

    $ docker restart myminer

## Build

    $ cd src/miner
    $ docker build -t jpsecher/nimiq-miner .

----

[![Docker build status](https://img.shields.io/docker/build/jpsecher/nimiq-miner.svg)](https://hub.docker.com/r/jpsecher/nimiq-miner/builds/)
