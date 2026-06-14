1. Used this commands:
``` bash
kubectl get deployments.apps -n trouble 
```
There are a crashed pod because it had 1 pod but unavailable
``` bash
kubectl describe deploy orange -n trouble 
```
For more information and i have seen there a typo in the command:
``` bash
    Command:
      sh
      c
      sleeep infinity
```
``` bash
kubectl edit deploy orange -n trouble
```

into this:
``` bash
    Command:
      sh
      -c
      sleep infinity
```