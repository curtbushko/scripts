#!/bin/sh

# Watches the nodes in your kubernetes cluster and refreshes once in a while

BPURPLE='\033[1;35m'      # Bold purple
PURPLE='\033[0;35m'       # Purple
watch -t -n 10 -c "echo \"${BPURPLE}   NODE WATCHER${PURPLE}\" && kubectl get nodes"
