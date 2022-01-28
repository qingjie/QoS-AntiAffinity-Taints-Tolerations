### nodeAffinity就是节点亲和性，相对应的是Anti-Affinity，就是反亲和性，这种方法比上面的nodeSelector更加灵活，它可以进行一些简单的逻辑组合了，不只是简单的相等匹配。 调度可以分成软策略和硬策略两种方式，软策略就是如果你没有满足调度要求的节点的话，POD 就会忽略这条规则，继续完成调度过程，说白了就是满足条件最好了，没有的话也无所谓了的策略；而硬策略就比较强硬了，如果没有满足条件的节点的话，就不断重试直到满足条件为止，简单说就是你必须满足我的要求，不然我就不干的策略。 nodeAffinity就有两上面两种策略：preferredDuringSchedulingIgnoredDuringExecution和requiredDuringSchedulingIgnoredDuringExecution，前面的就是软策略，后面的就是硬策略。


```
 kubectl get nodes 
 kubectl get nodes --show-labels
 kubectl label nodes ip-192-168-22-221.us-east-2.compute.internal role=spot
 kubectl get nodes --show-labels
 kubectl apply -f examples/0-node-selector.yaml
 kubectl get po -o wide
```

---
* https://www.qikqiak.com/post/understand-kubernetes-affinity/


