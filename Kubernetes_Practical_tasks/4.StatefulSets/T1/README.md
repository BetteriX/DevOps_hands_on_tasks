1. Made random_generator.yaml (Made some mistakes when i wont applied the label in the statefulset)
2. Run with this commands:
``` bash
kubectl create -f random_generator.yaml
kubectl get services random-generator
kubectl get sts random-generator
kubectl get sts random-generator --show-labels
```