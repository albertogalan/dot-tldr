
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


