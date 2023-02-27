#!/bin/sh

# Watches the kube-system namespace and refreshes every 10 seconds 

BGREEN='\033[1;32m'       # Bold green
GREEN='\033[0;32m'        # Green
watch -t -n 10 -c "echo \"${BGREEN}  ⎈  KUBE-SYSTEM WATCHER${GREEN}\" && kubectl get pods -n kube-system"
