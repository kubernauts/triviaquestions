Topic:  Which all api's are depricated and will stop working from kubernetes  1.16 onwards.

Answer: Network policy resources from extensions/v1beta1 
Use networking.k8s.io/vi
Podsecuritypolicy from extensions/v1beta1 
Use policy/v1beta1
Daemonset,replicaset,deployment from extensions/v1beta1, apps/v1beta1, apps/v1beta2 wont work 
Use apps/v1 
