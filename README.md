# docker-git

## How to use this image
### Docker Run ###

```
docker run --rm \
	-v /some/absoult/path:/git-workdir \
	-v ~/.ssh:/root/.ssh \
	plocek/git \
	git status
```

### Docker-Compose ###

Use a **docker-compose.yml** file similar to this...

```yml
version: '3'

services:
  git:
    image: plocek/git
    volumes:
      - ./:/git-workdir
      - ~/.ssh:/root/.ssh
```

... and start it via

```
docker-compose run --rm git git status
``