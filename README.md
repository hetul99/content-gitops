![la logo](https://user-images.githubusercontent.com/42839573/67322755-818e9400-f4df-11e9-97c1-388bf357353d.png)

### Linux Academy Course Repository
### Hands-On GitOps

This repository is a resource provided for Linux Academy students taking the hands-on GitIOps course.

Mode 1:
Linking Flux with our Github repo

export GHUSER=hetul99
cloud_user@ip-10-0-1-101:~$ env | grep GH
GHUSER=hetul99

fluxctl install \
--git-user=${GHUSER} \
--git-email=${GHUSER}@users.noreply.github.com \
--git-url=git@github.com:${GHUSER}/content-gitops \
--git-path=namespaces,workloads \
--namespace=flux | kubectl apply -f -

**Flux v1 is deprecated, please upgrade to v2 as soon as possible!**

New users of Flux can Get Started here:
https://fluxcd.io/docs/get-started/

Existing users can upgrade using the Migration Guide:
https://fluxcd.io/docs/migration/

deployment.apps/memcached created
service/memcached created
serviceaccount/flux created
clusterrole.rbac.authorization.k8s.io/flux created
clusterrolebinding.rbac.authorization.k8s.io/flux created
deployment.apps/flux created
secret/flux-git-deploy created


