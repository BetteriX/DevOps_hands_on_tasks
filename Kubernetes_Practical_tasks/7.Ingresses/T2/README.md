1. added colors.k8slab.net to /etc/hosts
2. viewed with:
``` bash
ubuntu@epam:~/Kubernetes_Practical_tasks/7.Ingresses/T2$ curl -s http://colors.k8slab.net/aqua && echo
curl -s http://colors.k8slab.net/maroon && echo
curl -s http://colors.k8slab.net/ && echo
curl -s http://colors.k8slab.net/blah-blah-blah && echo
{"color": "aqua", "hostname": "aqua-b9967f989-tgbpd", "address": "10.244.0.58", "version": "1.0.1"}
{"color": "maroon", "hostname": "maroon-6d78dfcf7c-n75b4", "address": "10.244.0.69", "version": "1.0.1"}
{"color": "olive", "hostname": "olive-756fd9f577-7tnvj", "address": "10.244.0.66", "version": "1.0.1"}
{"color": "olive", "hostname": "olive-756fd9f577-szdxc", "address": "10.244.0.63", "version": "1.0.1"}
```
