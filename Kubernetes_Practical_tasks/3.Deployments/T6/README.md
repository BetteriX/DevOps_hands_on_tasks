1. viewed with this commands:
``` bash
kubectl get deployments.apps -n trouble 
```
Seen there are 0 pods running

``` bash
kubectl describe deployments.apps lemon -n trouble
```

``` bash
kubectl edit deploy lemon -n trouble
```
Then added 1 replica and now works