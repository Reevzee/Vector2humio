# Vector2humio

Vector Collector for Docker

This is tested instructions for deploying Vector as a docker container and shipping container applications logs , docker events and docker stats to humio endpoint.

Run vector in docker using attacked vector.toml configuration file

docker run -d -v /path/to/vector/vector.toml:/etc/vector/vector.toml:ro -v /var/run/docker.sock:/var/run/docker.sock  -p 8383:8383 timberio/vector:0.11.X-debian


Reference:
https://vector.dev/docs/setup/installation/platforms/docker/
