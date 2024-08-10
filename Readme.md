# Setup private docker container registry (easily)

### What's included

1. Docker registry ([distribution](https://github.com/distribution/distribution/))
2. Web UI ([docker-registry-browser](https://github.com/klausmeyer/docker-registry-browser))
3. Security certificates auto-generation
4. Nginx reverse proxy
5. HTTP => HTTPS redirection
6. Container size limit is set to 1GB

### How to run

0. Pull this repository code
1. [Prepare .env file](#env-file) in root folder, next to docker-compose.yml
2. Run `docker-compose up`

### .env file

Here's the markdown rewritten as a pretty table:

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
