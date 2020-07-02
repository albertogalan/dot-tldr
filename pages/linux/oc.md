
> Description oc


- load oc environment

`minishift oc-env`


- see status of the namespace

`oc status`


- Search resources

`oc api-resources`


- Gives permission to user  to deploy on those projects

`oc policy add-role-to-user edit system:serviceaccount:{{logon-cicd:jenkins}} -n {{project}}`

- Create secrets 

`oc create secret generic {{name}} -n {{project}} --from-literal=username=ulgn02 --from-literal=pwd=XXXXXXXXXXX`
- Create secret for keystores and keytabs

`oc create secret generic {{namesecrets}}-secret -n logon-eu-dev \
  --from-file=javax.net.ssl.trustStore=openshift/logon-eu-dev/security/keystore/truststore.jks `

- Parametrize Quotas

    `oc patch quota logon-eu-dev-quota -p '{"spec":{"hard":{"persistentvolumeclaims": "15", "pods": "20", "requests.cpu": "32", "requests.memory": "256Gi", "requests.storage": "50Gi"}}}' -n logon-eu-dev`

- Applying patching

`oc patch deployment myapp-deployment '{"service":"ddd ...."}`
`oc patch quota myapp-quota '{"spec":"hard....."}`
`oc patch limitrange myapp-limitrange '{"spec":{"limits"....}}`



- installed operators

`oc get packagemanifests -n openshift-marketplace`


- troubleshooting

`https://www.openshift.com/blog/troubleshooting-openshift-internal-networking`


- Build strategies

`https://docs.openshift.com/container-platform/4.2/builds/build-strategies.html`


