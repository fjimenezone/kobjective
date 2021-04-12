# Running pods
What happens if a running pod, managed by the job controller, gets deleted?

Here's your chance of finding out.

```
kubectl create -f sleeping-beauty-job.yaml
```
```
kubectl delete pod sleeping-beauty-xxxxx
```
Observe the behavior using `watch`