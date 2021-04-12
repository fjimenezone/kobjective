# Default Job

Run

```kubectl create -f italian-job.yaml```

The watch pane shows a job.batch/italian resource. This job would have created a pod.

```
$ kubectl get all
NAME                READY   STATUS      RESTARTS   AGE
pod/italian-pgtjr   0/1     Completed   0          12s

NAME                COMPLETIONS   DURATION   AGE
job.batch/italian   1/1           3s         12s
```

Observe

```kubectl describe job italian```

Lines of interest:
- Parallelism
- Completions
- Start Time
- Completed At
- Duration
- Pods Statuses
- Events

Check the output of the pod

```kubectl logs italian-pgtjr```

The `STATUS` of the pod is `Completed`

`COMPLETIONS` is `1/1` in the job


Clear the job

```kubectl delete -f italian-job.yaml```

Documentation
https://kubernetes.io/docs/concepts/workloads/controllers/job/

