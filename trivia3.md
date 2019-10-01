Topic3: What are different set of usecases for multicontainer pod?? 
Lets list all that community has used.

Community Answers:
1: The simplest is log gathering as a side car container.
2: Ambassador container to proxy a database connection or adapter container to pass/simplify monitoring output to an external monitoring service.
3: TLS sidecar container to force tls communication from other clients to some other containers in the pod: jmx prometheus java exporter as sidecar, sidecars used by a service mesh, e.g. envoy or proxy sidecar for istio.
4: Git synchornizer,have a nginx in the sidecar to view stuff from a shared volume.
