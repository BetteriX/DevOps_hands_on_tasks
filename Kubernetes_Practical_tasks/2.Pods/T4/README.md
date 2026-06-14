1. check the pod: kubectl get pods redis-db -n trouble
2. find the error: kubectl describe pods web -n trouble (found the error was in args)
They are immutable so we have to delete the pod:
3. kubectl delete pod redis-db -n trouble
4. kubectl apply -f redis-db.yaml