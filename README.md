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
