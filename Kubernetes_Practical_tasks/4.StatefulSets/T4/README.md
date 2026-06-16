1. Entered this command:
``` bash
kubectl run dns-test --rm -i --image=busybox --restart=Never -- sh -c \
"nslookup random-generator-0.random-generator.default.svc.cluster.local && 
nslookup random-generator-1.random-generator.default.svc.cluster.local && 
nslookup random-generator-2.random-generator.default.svc.cluster.local" | tee $HOME/k8s_sts.txt
```