# Kubernetes cluster bootstrap with ansible and kubeadm

## Work in Progress! Do not use this in production until it reaches a stable version/tag

## if you need the old version of this repo checkout the 1.0 release

https://github.com/ben-st/ansible-kubeadm/releases

## this repo is an opinionated holistic aproach for a k8s cluster install.

the debian-singleNode-playbook.yml will install a kubeadm based
kubernetes cluster version 1.14 on a single node

the multinode playbook will follow some time soon

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
