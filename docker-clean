#!/bin/sh
BPURPLE='\033[1;35m' # Bold purple
GREEN='\033[0;32m'   # Green

echo "${BPURPLE}[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] Removing running containers..${GREEN}"
docker rm -f $(docker ps -a -q)

echo "${BPURPLE}[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] Removing docker images..${GREEN}"
docker image ls -q | xargs -I {} docker image rm -f {}

echo "${BPURPLE}[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] Removing volumes..${GREEN}"
docker volume rm $(docker volume ls -q)
