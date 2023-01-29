## Kubernetes Bootcamp

Wer die Details aus dieser Woche nacharbeiten möchte kann recht gut hier einsteigen:

https://kubernetes.io/de/docs/tutorials/hello-minikube/

Für den Helm Part geht es hier los:

https://helm.sh/docs/intro/using_helm/




### Anleitung für ssh findet sich unter

https://docs.github.com/de/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent




## Setup kind instead of minikube
```
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.17.0/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/kind
```
Add Autocompletion for kind to bash with  
```
echo 'source <(kind completion bash)' >> /etc/bash.bashrc
```
Start a cluster with
```
kind create [CLUSTERNAME, default= kind]
```
Use the provided kindMultiNodeCluster.yml with option '--config' to automatically create a 3 node cluster, 1 control-plane and two worker nodes

![out](https://user-images.githubusercontent.com/123601944/215346448-a9f5d26f-7110-4d7b-a77c-a0a2053fa426.gif)


## Add helm repos
```
helm repo add bitnami https://charts.bitnami.com/bitnami                
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
```
