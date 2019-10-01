Topic: What is the difference between managed kubernetes and self managed kubernetes and what all components you do not have control in managed kubernetes, how good it is for large scale?

Community Answers:
1: Managed services eg EKS AKS GKE platform - no control over master, etcd
Self managed k8s like rancher kubeadm kops
2:In Managed K8s you don't have control over your Master Nodes (Etcd/API/Controller Manager/Scheduler), and you don't have to worry about scaling as its managed by your cloud provider.
3:For scaling purpose the cloud provider Will optimise your ressource comsumption and consistency via machine type/autoscaling.
4:Here is also an option of self-hosted and self-driving, or an autonomous kubernetes with AI / ML support,
There are also managed kubernetes services via cloudless technology, where you don’t need to deal with worker nodes either.
5:Managed kubernetes is a service offering from various cloud providers like GKE, OKE, AKS, EKS etc. where you do not have control over the control plane. You can interact with the cluster but you do not manage the master.
Self managed cluster are the cluster that you have created on baremetal, cloud VM's etc and you have full control over all the components of the cluster.
for large scale self managed clusters have more advantages over the managed as you would need full control over the master, etcd servers, autoscaler for spanning across zones(current autoscaling apabilities for managed kubernetes is limited and you do not get control and you dont know how many cluster autoscalers would be running as well). Another point is the Ip ranges in a private network it makes sense to manage your own cluster otherwise creating multiple clusters with set of ip ranges would create a mess at the end.
the pre pull of images is another example that you can control for self managed but not the managed ones.
so for an org that do not want overhead of managing k8s should definitely go for managed kubernetes while large scale orgs still prefer the self managed due to different reasons.
