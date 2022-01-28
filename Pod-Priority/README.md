```
kubectl get PriorityClass
kubectl get pods -A
kubectl get pods -A \
    -o jsonpath='{range .items[*]}{.metadata.name}{" - "}{.spec.priorityClassName}{"\n"}{end}'
```


