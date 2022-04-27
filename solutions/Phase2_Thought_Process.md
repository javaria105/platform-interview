For phase 2, I chose Kubernetes as the container orechestration tool. I chose Kubernetes because it's a popular
open-source system that helps automate containerized appplications. Some of its features include automated 
rollouts and rollbacks, service discovery and loadbalancing, horizontal scaling, self-healing, and secret and
configuration management. Kubenetes can be deployed anywhere (on-prem, cloud, or hybrid). 
There are many lightweight versions of Kubernetes such as K3s and minikube, but since I am to implement
a local single node version, I chose minikube.

For this I visited their website and followed the steps to download it for my particular platform. I simply ran
the following two commands to install minikube:
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-latest.x86_64.rpm
sudo rpm -Uvh minikube-latest.x86_64.rpm
```

After it was installed, I ran `minikube start`. After that, I had to install kubectl so I ran 
`minikube kubectl -- get po -A`. With 4 simple commands, I was able to start deploying to minikube.

I deployed the hello-minikube application in the tutorial and below is a screenshot of some commands I ran to 
see the pods, services, and namespaces. Developers can use similar commands to explore minikube 
and create their deployments.

<img width="585" alt="Screen Shot 2022-04-27 at 12 14 43 PM" src="https://user-images.githubusercontent.com/55933082/165582625-bf7bbc45-ba00-421c-b895-b1805f825f58.png">



Resources:

https://kubernetes.io/

https://k3s.io/

https://minikube.sigs.k8s.io/docs/start/
