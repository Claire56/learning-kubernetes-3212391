minikube start: Start Cluster<br>
minikube stop: stop Cluster<br>
minikube minikube update-check #Compare with latest version<br>
minikube delete #delete cluster<br>
kubectl cluster-info #info about where the cluster is running <br>
kubectl get nodes: Nodes from namespace<br>
kubectl get nodes -A: List nodes from all namespaces<br>
kubectl get namespacesor ns<br>
kubectl get services -A<br>
yamlchecker.com: validate yaml files<br>
kubectl apply -f namespace.yaml: create namespaces using yaml file<br>
kubectl delete -f namespace.yaml:delete namespaces using yaml file<br>
kubectl get pods -n development: get pods in development namespace<br>
kubectl delete  pod pod-info-deployment-68c8476764-dx98b  -n development<br>
kubectl describe  pod pod-info-deployment-68c8476764-dx98b  -n development: look at pod's event log<br>
kubectl get pods -n development -o wide: pods with IP addresses<br>
kubectl exec -it busybox-6c747767dd-gcwqf -- /bin/sh: connect to busybox pod interactively<br>
use busybox to interact with pods using their ip addresses for example #wget 10.244.0.6:3000<br>
kubectl logs pod-info-deployment-68c8476764-blpnd -n development: check if working.<br>
<h1> Create k8s Load Balance service</h1>

The service will send traffic to pods with pod-info app, to create the service first run 
bash
```
minikube tunnel
```

in another terminal deploy the service , you will go back to enter the PW in the tunnel window
<h3>resource management </h3>

* set CPU and Memory values
* https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/ 


<h3>Clean up</h3>
You can delete resources

* using the yaml files
* by deleting the namespaces


