# Kubernetes Quality of Service (QoS) Classes for Pods (Guaranteed, Burstable, BestEffort)

## Links

- [stress-ng](https://unix.stackexchange.com/questions/99334/how-to-fill-90-of-the-free-memory)


```
ssh ec2-user@3.16.128.62
sudo amazon-linux-extras install epel -y
sudo yum install stress -y

stress --vm-bytes 2G --vm-keep -m 1
```