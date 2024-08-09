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
```
USER_NAME=... //user name used to browse registry and push/pull images
USER_PASSWORD=... //password
SECRET_KEY_BASE=... //used for web ui encryption, generate that value with: `openssl rand -hex 64`
```

### Todo's
1. Support for let's encrypt
2. Optional let's encrypt
3. Container size limit to .env