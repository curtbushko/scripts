#!/bin/sh

# Watches pods in your current namespace and refreshes once in a while

BBLUE='\033[1;34m' # Bold blue
BLUE='\033[0;34m'  # Blue
watch -t -n 3 -c "echo \"${BBLUE}   POD WATCHER${BLUE}\" && kubectl get pods -o wide --field-selector=status.phase!=Succeeded --selector=app!=jobqueues"
