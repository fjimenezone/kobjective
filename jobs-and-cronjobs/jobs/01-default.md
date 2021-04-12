# Default Job

Run

`kubectl create -f italian-job.yaml`

The watch pane shows a job.batch/italian resource. This job would have created a pod.

```
$ kubectl get all
NAME                READY   STATUS      RESTARTS   AGE
pod/italian-pgtjr   0/1     Completed   0          12s

NAME                COMPLETIONS   DURATION   AGE
job.batch/italian   1/1           3s         12s
```

Observe

`kubectl describe job italian`

Check the output of the pod

`kubectl logs italian-xxxxx`


The `STATUS` of the pod is `Completed`

`COMPLETIONS` is `1/1` in the job


Clear the job

`kubectl delete -f italian-job.yaml`

