1. kubectl get pod -A (view all)
found: find-me       save-me                            1/1     Running            1 (10m ago)      57m
kubectl get pod (Only checks default ns)
find-me -> namespace
save-me -> pod_name

2. kubectl get pod save-me -n find-me -o yaml > $HOME/k8s_pods/save-me_pod.yml
