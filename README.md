# Kubernetes cluster bootstrap with ansible and kubeadm

## Work in Progress! Do not use this in production until it reaches a stable 2.X version/tag

https://github.com/utf18/ansible-kubeadm/releases

the install-all.yml will install a kubernetes 1.17 cluster with kubeadm and flannel
Right now it is only tested on ubuntu 18.04

## components

- kubernetes 1.17
- flannel

## Minimum Requirements

1 Master
- 2 cpu
- 4gb ram

at least 1 Node, better 3 with more ram and cpu
- 2 cpu
- 4gb ram

## getting started

create your inventory from the example-inventory or edit the values directly

generate yourself a new cluster join token and insert it in the inventory with

`kubeadm token generate`

Then run the playbook:

`ansible-playbook -i inventories/<example-inventory>/ install-all.yml`

you can give your newly added Nodes the "worker" label with
`kubectl label node <nodeName> node-role.kubernetes.io/worker=worker`