#!/bin/sh

# Description: Deletes a GKE node 

if [ "$1" = "" ]; then
        echo "Error: Missing node name"
        exit 1
fi

echo "Deleting GKE node: $1"


NODE="$1"
set -e
echo "Cordoning ${NODE}"
kubectl cordon "${NODE}"
echo "Draining ${NODE}"
kubectl drain "${NODE}" --force --ignore-daemonsets --delete-emptydir-data
ZONE="$(kubectl get node "${NODE}" -o jsonpath='{.metadata.labels.topology\.gke\.io/zone}')"
INSTANCE_GROUP=$(gcloud compute instances describe --zone="${ZONE}" --format='value[](metadata.items.created-by)' "${NODE}")
INSTANCE_GROUP="${INSTANCE_GROUP##*/}"

echo "Deleting instance for node '${NODE}' in zone '${ZONE}' instance group '${INSTANCE_GROUP}'"
gcloud compute instance-groups managed delete-instances --instances="${NODE}" --zone="${ZONE}" "${INSTANCE_GROUP}"
echo "Deleting instance for node '${NODE}' completed."
