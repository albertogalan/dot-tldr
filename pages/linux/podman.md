
> Description podman

- Accessing registry directly from cluster

```
oc login -u kubeadmin -p <password_from_install_log>
podman login -u kubeadmin -p $(oc whoami -t) image-registry.openshift-image-registry.svc:5000
```


