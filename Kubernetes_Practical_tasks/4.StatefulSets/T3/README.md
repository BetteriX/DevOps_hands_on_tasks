1. changed image version to :2
2. Used command:
``` bash
kubectl apply -f random_generator.yaml
kubectl describe sts random-generator
```

``` bash
  Normal  SuccessfulDelete  87s                  statefulset-controller  Delete Pod random-generator-2 in StatefulSet random-generator successful
  Normal  SuccessfulCreate  86s (x2 over 9m7s)   statefulset-controller  Create Pod random-generator-2 in StatefulSet random-generator successful
  Normal  SuccessfulDelete  82s                  statefulset-controller  Delete Pod random-generator-1 in StatefulSet random-generator successful
  Normal  SuccessfulCreate  81s (x2 over 9m9s)   statefulset-controller  Create Pod random-generator-1 in StatefulSet random-generator successful
  Normal  SuccessfulDelete  79s                  statefulset-controller  Delete Pod random-generator-0 in StatefulSet random-generator successful
  Normal  SuccessfulCreate  78s (x2 over 9m12s)  statefulset-controller  Create Pod random-generator-0 in StatefulSet random-generator successful
```