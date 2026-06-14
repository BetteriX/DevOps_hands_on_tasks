1. made the pod.yaml with my name in a env variables
2. started yaml: kubectl apply -f pod.yaml
3. checked logs: kubectl logs envtest
4. pasted logs: kubectl logs envtest > $HOME/k8s_pods/default-envtest.log