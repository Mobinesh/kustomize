# kustomize
Kustomize lets you customize raw, template-free YAML files for multiple purposes, leaving the original YAML untouched and usable as is.
Install kustomize for Linux:
```
curl --silent --location --remote-name \
"https://github.com/kubernetes-sigs/kustomize/releases/download/kustomize/v3.2.3/kustomize_kustomize.v3.2.3_linux_amd64" && \
chmod a+x kustomize_kustomize.v3.2.3_linux_amd64 && \
sudo mv kustomize_kustomize.v3.2.3_linux_amd64 /usr/local/bin/kustomize```
you can also install it by snap
```
```
sudo apt update
sudo apt install snapd
sudo snap install kustomize
```
for deploying with kubectl use `kubectl apply -k /overlays/dev/`
to use argocd application file `kubectl apply -f application.yaml`

> Note that in the application.yaml file argocd-image-updater is activated8 and to use it you need to install argocd image updater firs, create secret for write-back method and then apply the application
