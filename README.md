# Building-kuberents-cluster
Building Kuberents cluster using kubeadm by Ansible.
- The purpose of this project is to build a kuberents cluster consists of 1 Master node and an (X) number of Worker-Nodes.

![alt text](https://github.com/Ahmed90-DevOps/installing-kuberents/blob/master/README_images/kubernetes_architecture.jpg)

# Prerequisites:
1. Multiple Linux servers running CentOS 7 (1 Master Node, Multiple Worker Nodes)
2. A user account on every system with sudo or root privileges
3. Set the hostname of each machine >>> hostnamectl set-hostname <Node_name>
4. Make a host entry or DNS record to resolve the hostname for all nodes >>> edit in /etc/hosts or /etc/resolve.conf if you have a DNS server
5. Configure Kubernetes Repository on all nodes:-
   vim /etc/yum.repos.d/kubernetes.repo
   
   [kubernetes]
   
   name=Kubernetes
   
   baseurl=https://packages.cloud.google.com/yum/repos/kubernetes-el7-x86_64
   
   enabled=1
   
   gpgcheck=1
   
   repo_gpgcheck=1
   
   gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg


# Installation:
Use the below command on your Ansible server.
- Linux OS (Centos7):
- update hosts file with your desired IPs and Worker-Nodes numbers
- Editing the apiserver-advertise-address to be the same as your Master node IP before running the playbook as below:

![alt text](https://github.com/Ahmed90-DevOps/installing-kuberents/blob/master/README_images/Capture.PNG)

- From the same directory you store the playbook Run >>> ansible-playbook installing_K8s.yml
- After running the playbook successfully check nodes state on Master node by >>> kubectl get nodes

# Contributing:
- Fork it (https://github.com/yourname/yourproject/fork)
- Create your feature branch (git checkout -b feature/fooBar)
- Commit your changes (git commit -am 'Add some fooBar')
- Push to the branch (git push origin feature/fooBar)
- Create a new Pull Request
