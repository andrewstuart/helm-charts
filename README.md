# Helm Charts

A set of helm charts I've created that have proven useful to me, and hopefully
you may find useful also.

## Elk

Set up ELK logging with automatic fluentd log aggregation for all stdout logs in
your kubernetes cluster. Log events will be tagged automatically with helpful
metadata such as pod name, container name, namespace, and some other k8s
metadata.

So far there are two required values:
- pvcStorage
- dnsName

There is also a prerequisite for you to have a PVC provisioner that can create
PersistentVolumes for the `standard` storage class.


```bash
helm install --set pvcStorage=100G --set dnsName=logs.astuart.co -n elk elk-cluster-addon
```
