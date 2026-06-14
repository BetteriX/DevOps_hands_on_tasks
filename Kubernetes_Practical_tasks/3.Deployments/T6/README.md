1. viewed with this commands:
kubectl get deployments.apps -n trouble (I have seen there are 0 pods running)
kubectl describe deployments.apps lemon -n trouble (Checked with this too)
kubectl edit deploy lemon -n trouble (Then added 1 replica and now works)