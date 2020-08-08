
> Description kubectl

- Description Help

kubectl xxx


- See events of what happening

kubectl get events


- Monitor

kubectl export HTTPS_PROXY=:5000


- exposing services

kubectl expose rc nginx --port=80 --target-port=8000


- Exposed

kubectl expose rc kubia --type=LoadBalancer --name kubia-http service kubia-http exposed


- Create a secret based docker credentials // registry docker on kubernetes

kubectl


- a

kubectl create secret generic regcred --from-file=.dockerconfigjson=/home/agalan/.docker/config.json --type=kubernetes.io/dockerconfigjson


- List of resources type

kubectl api-resources


- Deployment

kubectl apply -f https://k8s.io/examples/application/nginx-with-request.yaml


