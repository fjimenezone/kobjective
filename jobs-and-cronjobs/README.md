# Kubernetes Jobs and Cronjobs basics
The material presented here will help demonstrating the behavior jobs and cronjobs.

## Requirements
* A k8s cluster access via kubectl client.
* The ability to create a new namespace, pods, jobs and cronjobs utilizing kubectl.

## Intended workflow for demonstration
Create a fresh namespace and set the context to use that namespace.
```
kubectl create ns tenet

kubectl config set-context --current --namespace=tenet
```

It is best if a tmux session is established in a window with two panes opened.
```
tmux new-session -s tenet -d -- watch -n1 'kubectl get all'
tmux split-window -v -t tenet
tmux -2 attach-session -t tenet
```