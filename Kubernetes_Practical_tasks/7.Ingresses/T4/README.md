1. check the ingress:
``` bash
kubectl describe trouble-1-ingress
```
and its was on the default namespace and the services were in the trouble-1 namespace
2. Move the ingress to the trouble-1 namespace:
``` bash
kubectl get ingress trouble-1-ingress -o yaml > ingress.yaml
kubectl apply -f ingress.yaml
```
3. Now its works:
``` bash
ubuntu@epam:~/Kubernetes_Practical_tasks/7.Ingresses/T4$ kubectl describe ingress trouble-1-ingress -n trouble-1
Name:             trouble-1-ingress
Labels:           <none>
Namespace:        trouble-1
Address:          192.168.39.181
Ingress Class:    nginx
Default backend:  <default>
Rules:
  Host                  Path  Backends
  ----                  ----  --------
  trouble-1.k8slab.net
                        /lime     lime-svc:80 (10.244.0.136:80,10.244.0.143:80,10.244.0.141:80)
                        /purple   purple-svc:80 (10.244.0.137:80,10.244.0.144:80)
Annotations:            <none>
Events:
  Type    Reason  Age                From                      Message
  ----    ------  ----               ----                      -------
  Normal  Sync    33s (x2 over 38s)  nginx-ingress-controller  Scheduled for sync
```