1. check the pod: kubectl get pods web -n trouble
2. find the error: kubectl describe pods web -n trouble (found the error was a typo)

 Warning  Failed     94s (x3 over 2m12s)  kubelet            spec.containers{web}: Failed to pull image "nginxxx": Error response from daemon: pull access denied for nginxxx, repository does not exist or may require 'docker login': denied: requested access to the resource is denied
3. edit the pod: kubectl edit pod web -n trouble