#!/bin/sh

# Description: Delete all helm things

helm ls --all --short | xargs -L1 helm delete
kubectl delete --all jobs
kubectl delete --all statefulsets
kubectl delete --all daemonsets
kubectl delete --all replicasets
kubectl delete --all deployments
kubectl delete --all services
kubectl delete --all pvc
kubectl delete --all secrets
kubectl delete ns ns1
kubectl delete ns ns2
kubectl delete ns vault
kubectl patch crd/servicedefaults.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/serviceintentions.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/ingressgateways.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/meshes.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/proxydefaults.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/serviceresolvers.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/servicerouters.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/servicesplitters.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/terminatinggateways.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/controlplanerequestlimits.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/exportedservices.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/gatewayclassconfigs.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/jwtproviders.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/meshservices.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl patch crd/samenessgroups.consul.hashicorp.com -p '{"metadata":{"finalizers":[]}}' --type=merge
kubectl delete crd/servicedefaults.consul.hashicorp.com
kubectl delete crd/serviceintentions.consul.hashicorp.com
kubectl delete crd/ingressgateways.consul.hashicorp.com
kubectl delete crd/meshes.consul.hashicorp.com
kubectl delete crd/proxydefaults.consul.hashicorp.com
kubectl delete crd/serviceresolvers.consul.hashicorp.com
kubectl delete crd/servicerouters.consul.hashicorp.com
kubectl delete crd/servicesplitters.consul.hashicorp.com
kubectl delete crd/terminatinggateways.consul.hashicorp.com
kubectl delete crd/controlplanerequestlimits.consul.hashicorp.com
kubectl delete crd/exportedservices.consul.hashicorp.com
kubectl delete crd/gatewayclassconfigs.consul.hashicorp.com
kubectl delete crd/jwtproviders.consul.hashicorp.com
kubectl delete crd/meshservices.consul.hashicorp.com
kubectl delete crd/samenessgroups.consul.hashicorp.com
