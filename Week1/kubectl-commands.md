# `kubectl` commands for week 1

```bash
# create a pod from a pod definition file (YAML) named 'pod-definition.yml'
kubectl create -f pod-definition.yml

# list the pods in the default namespace
kubectl get pods

# create a job from a job definition file (YAML) named 'job-definition.yaml'
kubectl create -f job-definition.yaml

# list the jobs in the default namespace
kubectl get jobs

# view the output of the pod logs (from pod named 'math-add-job-ld87pn')
kubectl logs math-add-job-ld87pn

# delete the job named 'math-add-job'
kubectl delete job math-add-job

# create a cronjob from a cronjob definition file (YAML) named 'cron-job-definition.yaml'
kubectl create -f cron-job-definition.yaml

# list the cronjobs in the default namespace
kubectl get cronjob

# describe the pod named 'myapp-pod' to get more information about the pod
kubectl describe pod myapp-pod
```