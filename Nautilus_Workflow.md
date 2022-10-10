# How to access Nautilus

[Nautilus Home Page](https://portal.nrp-nautilus.io)

Once logged in create a pod in the namespce `molecular-aquatic-microbial-ecology`

Check to make sure you are in the correct namespace with 

```
kubectl config get-contexts
```
*If in the wrong namespace check the config file you downloaded and change the namespace to the correct namespace*

## Excuting a Pod 

Create a YAML file for the desired pod [Example](coverm.yaml)

Create the pod
```
kubectl create -f coverm.yaml
```

Verify the status of the pod 
```
kubectl get pods
```

Oncce the pod is create it should say Running

Then input 
```
kubectl exec -it coverm -- /bin/bash
```
*the coverm section directly relates to the name of the pod*

Open a Terminal and input
```
kubectl port-forward coverm 8888:8888
```

In the orginal terminal this will appear`(base) jovyan@coverm:~$`

Then input: 
```
jupyter notebook --ip='0.0.0.0'
```

I often use the third link and put it in browser's address bar. 


**Once you are done with the pod it was be deleted**

```
kubectl delete pod coverm
```

Ensure the pod was deleted
