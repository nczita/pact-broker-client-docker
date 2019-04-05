# Releasing

```
docker build -t nczita/pact-broker-client .
docker push nczita/pact-broker-client
```


# Update gems

Actually this is work in progress, right now:

* remove `Gemfile.lock`
* remove `COPY Gemfile.lock /app/` in `Dockerfile:9`
* build image
* start container
* copy `Gemfile.lock` to host
* stop (and remove) container
* commit updated `Gemfile.lock` only (reset other changes!)
