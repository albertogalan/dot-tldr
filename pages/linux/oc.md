
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

`oc patch limitrange myapp-limitrange '{"spec":{"limits"....}}`

- Output patch when edit

`oc edit dc hello-openshift --output-patch`



- installed operators

`oc get packagemanifests -n openshift-marketplace`


- troubleshooting

`https://www.openshift.com/blog/troubleshooting-openshift-internal-networking`


- Build strategies

`https://docs.openshift.com/container-platform/4.2/builds/build-strategies.html`


- rollout

oc rollout history


- rollout cancel so rollback

oc rollout cancel dc/jenkins


- get nodes

`oc get pod -o custom-columns=POD:.metadata.name,NODE:.spec.nodeName`


- Operators

`Create a operator groups`
`Create a subcription`
`Verify operator is installed`
`oc get pod -n namespace`
`Most of cases Create an instance`

`oc describe packagemanifests.packages.operators.coreos.com cluster-logging -n openshift-marketplace`



- Get last configuration applied

`oc apply view-last-applied -f simple3-dc.yaml`


- Config of a namespace

`oc config view`


- Resource Manifest

`oc explain resource`



> Description oc

- Description Help

oc xxx


- Debuging pods

`oc debug nexus4-554b56875b-t8lqx  --image=registry.access.redhat.com/rhel7/rhel-tools`


- Info Image -- ports etc

`oc image info sonatype/nexus3:latest`


