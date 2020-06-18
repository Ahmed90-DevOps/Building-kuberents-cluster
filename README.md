# Building-kuberents-cluster
Building Kuberents cluster using kubeadm by Ansible.
- The purpose of this project is to build a kuberents cluster consists of 1 Master node and an (X) number of Worker-Nodes.

![alt text](https://github.com/Ahmed90-DevOps/installing-kuberents/blob/master/kubernetes_architecture.jpg)

# Prerequisites:
1. Multiple Linux servers running CentOS 7 (1 Master Node, Multiple Worker Nodes)
2. A user account on every system with sudo or root privileges
3. set the hostname of each machine

# Installation:
Use the below command on your Ansible server after you edit the hosts file to suit your physical setup.
- Linux OS:
- ansible-playbook installing_K8s.yml
