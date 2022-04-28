For phase three, I would utilize Terraform and EKS to build out and scale workloads in AWS. I would have a primary cluster and a secondary cluster that is managed 
by a load balancer to route to the proper cluster. These clusters can be changed to be different clusters for different teams or just multiple copies of clusters
for the load balancer to route to for scaling in that way. I would also have a monitoring cluster that has Prometheus installed on it in conjunction with 
Grafana, Alert Manager, and all the different components for monitoring. Grafana can be used to display metrics with dashboards. The EKS clusters will have 
Prometheus, the Prometheus Adapter, the Customer Metrics API, the actual deployment, the Kubernetes horizontal autoscaler, and AWS Fargate. The autoscaler will 
send the custom metrics API its data which will utilize the Prometheus adapter to send data to Prometheus which will in turn send metrics back letting the autoscaler
know to increase or decrease the pod count. AWS Fargate will take care of provisioning these containers without us having to provision clusters of VMs. We can use 
Terraform to write out our deployment standards for EKS and Prometheus.

![Screenshot_1](https://user-images.githubusercontent.com/55933082/165837030-0d4fd1c1-dbb0-4fe3-b69c-a5f6e36ce7fc.png)


Resources:

https://www.metricfire.com/blog/prometheus-metrics-based-autoscaling-in-kubernetes/

https://medium.com/@shacharaj/kubernetes-multi-cluster-monitoring-using-prometheus-thanos-on-eks-using-helm-7279d8b42213


