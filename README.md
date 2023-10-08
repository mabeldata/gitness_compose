# gitness_compose
Unofficial gitness docker compose

[![Maintained_By Mabel Data](https://img.shields.io/badge/Maintained_By-MabelData-purple)](https://github.com/mabeldata/mojo_docker/blob/main/LICENSE)

The official project -> [GITNESS](https://github.com/harness/gitness)

### Requirements
- Docker, Docker-Compose

### Running
Clone the repository and then go to gitness_compose folder 

Rename the .env.example file to .env, change or add the environment variables as you need.

Then run:
```
docker compose up -d
```
After running, access [localhost](http://localhost)

The default user is Admin and the password is the one set in the .env file

### Production
I have add inside the nginx folder a default-ssl-example.conf file with the minimal configurations
to use with nginx, as in my servers I don't use the nginx container as I have another service for reverse proxy,
if you are going to use nginx you will need to modify the docker-compose.yml to add a share volume
between your server and the nginx container with the certibot files or modify the nginx container image
to create the certibot/let's encrypt files within it.
