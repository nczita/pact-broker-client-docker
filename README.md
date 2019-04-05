# Pact Broker Client Docker

Docker image running the pact broker client.
You can pull the latest image from Dockerhub [nczita/pact-broker-client](https://hub.docker.com/r/nczita/pact-broker-client).

## Usage

```sh
# Get the latest version
$ docker pull nczita/pact-broker-client

# Publish pacts
$ docker run \
    --rm \
    -v $(pwd):/app/pacts \
    -e PACT_BROKER_BASE_URL=http://pact-broker.example.net \
    nczita/pact-broker-client \
    publish --consumer-app-version=1.0.0 pacts

# Use can-i-deploy
$ docker run \
    --rm \
    -e PACT_BROKER_BASE_URL=http://pact-broker.example.net \
    nczita/pact-broker-client \
    can-i-deploy --pacticipant "Animal Service" --latest
```

For examples of the other commands, please refer to https://github.com/pact-foundation/pact_broker-client.

Dockerhub: [nczita/pact-broker-client](https://hub.docker.com/r/nczita/pact-broker-client).
