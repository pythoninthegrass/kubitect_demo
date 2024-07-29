# kubitect_demo

## Minimum Requirements

* [dl-gh](https://github.com/pythoninthegrass/dl_gh)
* [devbox](https://www.jetify.com/devbox/docs/quickstart/)

## Install

```bash
cd ~/Downloads/
dl-gh -u musicdin -r kubitect -t tar.gz
tar -xzf kubitect-v3.4.0-darwin-arm64.tar.gz
sudo mv kubitect /usr/local/bin/
kubitect completion bash > $(brew --prefix)/etc/bash_completion.d/kubitect
```

## Quickstart

```bash
# export preset
kubitect export preset --name getting-started > cluster.yaml

# edit cluster.yaml

# apply preset
kubitect apply --config cluster.yaml

# list clusters
kubitect list clusters

# display nodes
kubectl --context k8s-cluster get nodes

# print config
kubitect export config          # --cluster <string>

# export kubeconfig
kubitect export kubeconfig      # --cluster <string>

# destroy cluster
kubitect destroy --auto-approve --cluster <string>
```

## TODO

* POC
* Docs
  * Description
  * Minimum Requirements
  * Usage
