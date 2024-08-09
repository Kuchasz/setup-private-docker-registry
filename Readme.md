# Setup private docker container registry (easily)

### What's included
1. Docker registry ([distribution](https://github.com/distribution/distribution/))
2. Web UI ([docker-registry-browser](https://github.com/klausmeyer/docker-registry-browser))
3. Security certificates auto-generation
4. Nginx reverse proxy
5. HTTP => HTTPS redirection

### How to run
1. [Prepare .env file](#env-file) in root folder, next to docker-compose.yml
2. Run `docker-compose up`

### .env file
```
USER_NAME=... //user name used to browse registry and push/pull images
USER_PASSWORD=... //password
SECRET_KEY_BASE=... //used for web ui encryption, generate that value with: `openssl rand -hex 64`
```