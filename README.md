# Helm Charts

A set of helm charts I've created that have proven useful to me, and hopefully
you may find useful also.

So far there are two required values:
- pvcStorage
- dnsName

There is also a prerequisite for you to have a PVC provisioner that can create
PersistentVolumes for the `standard` storage class.

```bash
helm install --set pvcStorage=100G --set dnsName=logs.astuart.co -n elk elk-cluster-addon
```
