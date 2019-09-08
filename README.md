# Kubernetes cluster bootstrap with ansible and kubeadm

## Work in Progress! Do not use this in production until it reaches a stable version/tag

## if you need the old version of this repo checkout the 1.0 release

https://github.com/ben-st/ansible-kubeadm/releases

## this repo is an opinionated holistic aproach for a k8s cluster install.

the install-all.yml will install a kubernetes 1.15 cluster with kubeadm and the components below.
Right now it is only tested on ubuntu 18.04

## components

- kubernetes 1.15
- flannel
- metallb
- traefik
- prometheus
- grafana
- elasticsearch
- filebeat
- kibana

## Requirements

an nfs server to use for persistence
You can install one on the k8s-master with the playbook

`ansible-playbook -i inventories/<example-inventory>/ install-nfs-on-master.yml`


## getting started

create your inventory from the example-inventory or edit the values directly

generate yourself a new cluster join token and insert it in the inventory with

`kubeadm token generate`

Then run the playbook:

`ansible-playbook -i inventories/<example-inventory>/ install-all.yml`

if you want to just deploy and not run all the other tasks run

`ansible-playbook -i inventories/<example-inventory>/ deploy-all.yml`
