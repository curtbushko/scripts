#!/bin/bash

# Watches a directory for changes in files and runs go test with a clear cache
# Requires watchexec program

export BBLUE='\033[1;34m' # Blue
watchexec -e go -- 'echo "${BBLUE}[$(date -u +'%Y-%m-%dT%H:%M:%SZ')]   RUNNING BUILD ${BBLUE}" && go build .'
