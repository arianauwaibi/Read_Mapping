# How to access Nautilus

[Nautilus Home Page](https://portal.nrp-nautilus.io)

Once logged in create a pod in the namespce `molecular-aquatic-microbial-ecology`

Check to make sure you are in the correct namespace with 

```
kubectl config get-contexts
```
* If in the wrong namespace check the config file you downloaded and change the namespace to the correct namespace`*

## Excuting a Pod 

Create a YAML file for the desired pod [Example](docs/coverm.yaml)
