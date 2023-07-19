#!/bin/sh

# Watches a directory for changes in files and runs go test with a clear cache
BPURPLE='\033[1;35m' # Purple
echo "${BPURPLE}[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] ﭧ RUNNING TESTS"
gotestsum --format=testname --watch -- -failfast -count=1
