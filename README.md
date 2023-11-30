# create container inside pod
kubectl create -f `file/pod.yaml`

# list all pod
kubectl get pods

# list all pod with label
kubectl get pods --show-labels

# list with more detail
kubectl get pods -o wide

# get detail pod
kubectl describe pod `pod-name`

# port forwarding
kubectl port-forward `pod-name` `port-host`:`port-guest`

# add label
kubectl label pod `pod-name` `key`=`value`

# update label
kubectl label pod `pod-name` `key`=`value` --overwrite

# searching pod by label
## show all pod containt with key
kubectl get pods -l `key`

## show all pod !containt with key
kubectl get pods -l `!key`

## show all pod with spesific param
kubectl get pods -l '`key`=`value`'

## show all pod with multiple param
kubectl get pods -l '`key`=`value`,`key1`=`value1`'

# add annotation to pod
kubectl annotate pod `pod-name` `key`=`value`

# update annotation to pod
kubectl annotate pod `pod-name` `key`=`value` --overwrite

# show all namespace
kubectl get namespace

# show all pod with namespace
kubectl get pods --namespace `namespace`

# create pod with namespace
kubectl create -f `file/pod.yaml` --namespace `namespace`

# delete namespace
kubectl delete namespace `namespace`

# delete pod
kubectl delete pod `pod-name`

kubectl delete pod `pod-name1,pod-name2`

# delete pod by label
kubectl delete pod -l '`key`=`value`'

# delete all pod
kubectl delete pod --all

# delete all pod on with namespace
kubectl delete pod --all --namespace `namespace`

# show replication controller
kubectl get replicationcontrollers

# delete replication controller with all pods inside of it
kubectl delete replicationcontrollers `nama-replication-controller` --cascade=true

# delete replication controller only
kubectl delete replicationcontrollers `nama-replication-controller` --cascade=false

# show replica set
kubectl get replicaset

# delete replica set with all pods inside of it
kubectl delete replicaset `nama-replica-set` --cascade=true

# delete replica set only
kubectl delete replicaset `nama-replica-set` --cascade=false

# show daemon set
kubectl get daemonsets

# show daemon set detail
kubectl describe daemonsets `nama-daemonsets`

# delete daemon set
kubectl delete daemonsets `nama-daemonset`

# show all jobs
kubectl get jobs

# show detail jobs
kubectl describe jobs `nama-jobs`

# delete jobs
kubectl delete jobs `nama-jobs`

# show all cron jobs
kubectl get cronjobs

# delete cron jobs
kubectl delete cronjobs `nama-cron-jobs`

# show log on pod
kubectl logs `nama-pod`

# add label to node
kubectl label node `nama-node` `key`=`value`

# show all resources
kubectl get all

# show all resources on spesific namespace
kubectl get all --namespace `nama-namespace`

# delete all resources
kubectl delete all

# delete all resources on spesific namespace
kubectl delete all --namespace `nama-namespace`

# show services
kubectl get services

# delete services
kubectl delete services `nama-service`

# access shell on pods
kubectl exec `nama-pod` -it -- /bin/bash

# get env on pod
kubectl exec `nama-pod` -it -- env

# access service through DNS 
`nama-service.nama-namespace.svc.cluster.local`

# show all endpoints
kubectl get endpoints

# Continue
https://www.youtube.com/watch?v=IOX2stxBw7k&list=PL-CtdCApEFH8XrWyQAyRd6d_CKwxD8Ime&index=28
