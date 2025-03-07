# FLUX sample

### Prerequisites
- [Brew](https://gist.github.com/fardjad/2e38d4dbdd42b28ec8bbe0b725e67f37)
- [Docker](https://docs.docker.com/engine/install/debian/)
  - Add user on docker group (see command bellow)
- [Kubernetes](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/)
  - [Kind](https://kind.sigs.k8s.io/docs/user/quick-start/)
- [Flux cli](https://fluxcd.io/flux/get-started/)
- Export GitHub credentials (see command bellow)

``` bash
sudo usermod -aG docker ${USER}
```

``` bash
export GITHUB_TOKEN=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
export GITHUB_USER=julien-juncker
```

``` bash
flux bootstrap github \
  --owner=julien-juncker \
  --repository=flux-sample \
  --branch=main \
  --path=./clusters/my-cluster \
  --personal
```

Connect to VM on ssh in PC pro:
``` bash
ssh -i /Users/JULIEN/.ssh/julien-juncker-perso-gcp junckerjulien9@34.38.221.175
```