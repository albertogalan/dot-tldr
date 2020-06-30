# kubectl

> Command line interface for running commands against Kubernetes clusters.

- List all pods in all namespaces:

`kubectl get pods --all-namespaces`

- List all pods with more information (such as node name):

`kubectl get pods -o wide`

- Update specified pod with the label 'unhealthy' and the value 'true':

`kubectl label pods {{name}} unhealthy=true`

- List all resources with different types:

`kubectl get all`

- Show metrics for all nodes:

`kubectl top node`

- Show metrics for all pods in the default namespace:

`kubectl top pod`

- Print the address of the master and cluster services:

`kubectl cluster-info`
- resources type

`https://kubernetes.io/docs/reference/kubectl/overview/#resource-types`


- quickly create single-container deployment and service

`kubectl run;kubetcl expose`
- Create a registry secret

`kubectl create secret generic myregistry --from-file=.dockerconfigjson=/home/agalan/.docker/config.json`


- create a pod from image and access to console

`kubectl run postgres-rhel4 --image=registry.redhat.io/rhel8/nginx-114 -it bash`


- Run a Pod

`kubectl run --generator=run-pod/v1 {name} --image={imagename}`


- see previous logs , when pod is crash



- access to shell

`kubectl exec -it {pod-name} -- /bin/bash`


- getting information as env variables and open ports
```
kubectl logs pod/{name}
kubectl logs --previous pod/{name}
kubectl describe deployment/{name}
kubectl describe template openshift/{name}
kubectl exec -it <pod_name> -- env  # get env variables
kubectl get events
```



- Monitor kubetl api requests
`need to trus CA of mitmproxy`
`mitmproxy -p 5000 --ssl; export HTTPS_PROXY=:5000; kubectl get deployment`


- exposing services

`kubectl expose rc nginx --port=80 --target-port=8000`
`kubectl expose rc kubia --type=LoadBalancer --name kubia-http service kubia-http exposed`


- Create a secret based docker credentials // registry docker on kubernetes

`https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/`
`kubectl create secret generic regcred --from-file=.dockerconfigjson=/home/agalan/.docker/config.json --type=kubernetes.io/dockerconfigjson`


- List of resources type

`kubectl api-resources`


