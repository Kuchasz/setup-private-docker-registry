# Setup private docker container registry (easily)

![Project logo](https://github.com/Kuchasz/setup-private-docker-registry/raw/main/src/images/logo.jpeg "Project logo")


### What's included

1. Docker registry ([distribution](https://github.com/distribution/distribution/))
2. Web UI ([docker-registry-browser](https://github.com/klausmeyer/docker-registry-browser))
3. HTTPS protocol configuration
4. Basic credentials authentication
5. Basic config customizations

### How to run

1. Pull this repository code
2. [Prepare .env file](#env-file) in root folder, next to docker-compose.yml
3. Run `docker-compose up`

### Required .env file variables

| Variable               | Description                                                                  | Example Value             |
| ---------------------- | ---------------------------------------------------------------------------- | ------------------------- |
| `USER_NAME`            | User name used to browse registry and push/pull images                       | `admin`                   |
| `USER_PASSWORD`        | Password                                                                     | `extremely_hard_password` |
| `SECRET_KEY_BASE`      | Used for web UI encryption, generate this value with: `openssl rand -hex 64` | `your_secret_key_base`    |
| `PORT`                 | Port to listen on                                                            | `443`                     |
| `DOMAIN`               | Domain name to listen on                                                     | `localhost`               |
| `CONTAINER_SIZE_LIMIT` | Maximum container size, e.g., `100M` or `1GB`                                | `250M`                    |

### Todo's

1. Support for let's encrypt
2. Make let's encrypt cert optional
3. ~~Add container size limit to .env~~
4. Add pull/push usage examples
5. ~~Support for domain names~~
