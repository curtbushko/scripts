#!/bin/sh

# Cleanup failed pods

kubectl get pods --field-selector 'status.phase=Failed' -o name | xargs kubectl delete
