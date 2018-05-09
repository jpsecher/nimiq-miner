# Docker container for stand-alone Nimiq miner

## Plan

- [x] Get a Nimiq miner up and running locally.
- [ ] Make the Nimiq account configurable.
- [x] Get the miner to connect to a mining pool.
- [ ] Make a HTTP endpoint that reports the status of the miner.

## Notes

    $ cd src/miner
    $ docker build -t jpsecher/nimiq-miner .
    $ docker docker run  jpsecher/nimiq-miner
