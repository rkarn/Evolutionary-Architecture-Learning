Kubernetes cluster is deployed from:

    https://github.com/kubernetes/minikube

Useful descriptions on Kubernetes cluster and compute resource:

    https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/#resource-types

Details on Kubernetes resource QoS: 
    
    https://github.com/kubernetes/community/blob/master/contributors/design-proposals/node/resource-qos.md

Details of Kubernetes cloud metrics: 

    https://docs.datadoghq.com/agent/kubernetes/metrics/
    
Some of these metrics can be directly obtained from dashboard. Steps to open dash board is given at 

    https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/. 
    Run the command ‘kubectl proxy’ and open the bowser with the link 
    http://localhost:8001/api/v1/namespaces/kube-system/services/kubernetes-dashboard/proxy.  
    All the details are available from command “kubectl get nodes” and “kubectl describe nodes <nodename>”.
    
Vertical Scaling: Change the running container resources. Performed by docker update.
    
    https://docs.docker.com/engine/reference/commandline/update/#options
    
An automated way of vertical pod scaler is also available that uses some of the above features. Sample is given at:

    https://banzaicloud.com/blog/k8s-vertical-pod-autoscaler/ 
    
Horizontal Scaling: Change the number of replicated pods. Kubernetes horizontal pod autoscaler is available to use only CPU usage variable. But any custom metric can be used. An example of such implementation is given at: 
    
    https://docs.bitnami.com/kubernetes/how-to/configure-autoscaling-custom-metrics/ .  
    Another is https://medium.com/uptime-99/kubernetes-hpa-autoscaling-with-custom-and-external-metricsda7f41ff7846
    
    
Restart Policy: A way for automatic restart is performed by setting the restart policy given at: 

    https://blog.codeship.com/ensuring-containers-are-always-running-with-dockers-restartpolicy/. 
    Docker currently has four restart policies as no, on-failure, unless-stopped, always.
