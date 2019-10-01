Topic: Why do you have a pause container for every pod?

Community Answer: 
1: To set up a network namespace for the pod, as all containers in the same pod have the same IP
2:  garbage collector for the containers in pod.
3: Pause container is a collection of system resources that containers running inside will share. These include ip, port range, routing table, hostname, domain sockets etc.

