# fluxcd-intro

```
kubectl create ns flux

$GHUSER = "yossicohn"
fluxctl install \
--git-user=${GHUSER} \
--git-email=${GHUSER}@users.noreply.github.com \
--git-url=git@github.com:${GHUSER}/fluxcd-intro \
--git-path=kubernetes/configmaps,kubernetes/secrets,kubernetes/deployments \
--git-branch=flux-test \
--namespace=flux | kubectl apply -f -

kubectl -n flux rollout status deployment/flux

$env:FLUX_FORWARD_NAMESPACE = "flux"
fluxctl list-workloads
fluxctl identity


https://github.com/marcel-dempers/docker-development-youtube-series/settings/keys/new

fluxctl sync

  annotations:
    fluxcd.io/tag.example-app: semver:~1.0
    fluxcd.io/automated: 'true'

fluxctl policy -w default:deployment/example-deploy --tag "example-app=1.0.*"
```
