# Kubernetes cluster bootstrap with ansible and kubeadm

this repo is an opinionated holistic aproach for a k8s cluster install.

the debian-singleNode-playbook.yml will install a kubeadm based
kubernetes cluster version 1.14 on a single node

the multinode playbook will follow eventually

## components

- kubernetes 1.14
- traefik
- prometheus
- grafana
- elasticsearch
- kibana
- filebeat or fluentd
- openebs
- minio
- keycloak
- vault

## getting started

change your ip in the inventory

Then run the playbook:

`ansible-playbook -i inventory debian-singleNode-playbook.yml`

## limitations

right now it only runs on debian
