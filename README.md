# Vector2humio

Vector log shipper for Docker

Instructions for deploying Vector as a docker container and shipping container applications logs , docker events and docker stats to a humio endpoint.

1.) Run vector in docker using attached vector.toml configuration file. This will listen to any incoming logs on standard out as long as your using json file logging driver for all your containers.

docker run -d -v /path/to/vector/vector.toml:/etc/vector/vector.toml:ro -v /var/run/docker.sock:/var/run/docker.sock  -p 8383:8383 timberio/vector:0.11.X-debian

2.) Follow instructions to deploy docker events sidecar for vector https://github.com/Reevzee/docker_events2Stdout

3.) Follow instructions to deploy docker stats sidecar for vector https://github.com/Reevzee/Docker_stats2stdout







Reference:
https://vector.dev/docs/setup/installation/platforms/docker/
