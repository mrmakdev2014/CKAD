# this file contain some instruction for creating pod 
1- files key values :  must consist of lower case alphanumeric characters, '-' or '.', and must start and end with an alphanumeric character (e.g. 'example.com', regex used for validation is '[a-z0-9]([-a-z0-9]*[a-z0-9])?(\.[a-z0-9]([-a-z0-9]*[a-z0-9])?)*')

so we our name must be like this myapp-frontend-123 . 
2- the key words in the yaml files is lower but we have only apiVersion with capital V


# running the Pod 
##to run pod from yaml file just type
kubectl apply -f filename.yaml

## to show the pods running inside the Cluster just type
kubectl get pods

## to create pod int the fly  , type the command
kubectl run my-nginxpod --image nginx

## Please not that pod name is unique so you can't have two pods with the same name inside the same namespace
