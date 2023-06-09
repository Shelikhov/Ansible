Playbook to install K8s with kubeadm.

Hosts:
- bastion instance - with public IP throught which we can access k8s nodes;
- master_nodes - k8s master nodes with control plane;
- worker_nodes - k8s worker nodes.
 
Roles:
- containerd - to prepare net modules (overlay, br_netfilter) and install containerd as ContainerRuntime;
- kube_tools - to install kubelet, kubeadm, kubectl;
- init_primary_master - to initialize primary master node with kubeadm;
- join_master_nodes - to join rest master nodes to the primary master node;
- join_worker_nodes - to join worker nodes to the primary master node.

Prerequesites:
- to replace variables in inventory and vars files.
