```
kubectl describe pdb/nginx-pdb

kubectl drain ip-192-168-42-45.us-east-2.compute.internal
kubectl drain ip-192-168-42-45.us-east-2.compute.internal --delete-emptydir-data --ignore-daemonsets

kubectl uncordon ip-192-168-42-45.us-east-2.compute.internal
```