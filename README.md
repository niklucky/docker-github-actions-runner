# Running Github actions on self-hosted server
Github actions runner in Docker for **Organizations**
Source:
https://testdriven.io/blog/github-actions-docker/

## Ubuntu

### Docker build

```
docker build --platform linux/amd64 -t syndicatedb/github-runner .
```

### Docker run

```
docker run -it --name my-runner \
    -e ACCESS_TOKEN=... \
    -e ORGANIZATION=Orgname \
    -v /var/run/docker.sock:/var/run/docker.sock \
    syndicatedb/github-runner
```
### Set your variables in docker-compose

### Run on runner machine

```sh
cd ubuntu && docker-compose up -d
```

