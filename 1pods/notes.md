# if we use kubectl create -f filename.yaml we can't use kubectl apply 

kubectl apply with the same file many time if we run the yaml file with apply command or kubectl create -save-config 

# what's the differnce we write the following two command 

1- kubectl run nginxapp --image=nginx 
2- kubectl create -f pod.yaml ( pod.yaml contain pod for nginx image)
3- kubectl create --save-config -f pod-nginx.yaml ( pod.yaml contain pod for nginx image)
4- kubectl apply -f pod.yaml ( pod.yaml contain pod for nginx image)

#1- kubectl run nginxapp --image=nginx 
this command create deployment , replicaset and pod so it's shortcut to run deployment based on nginx image . 
Q : how to write command like this that run with 3 replicas 
  kubectl run nginxdeployment --image=nginx --replicas=5
nginxdeployment   : is the deployment name. 
  to remove this deployment that created from the above command use the below command
  kubectl run nginxdeployment --image=nginx --replicas=5

  there's a very good shortcut to get list of all just type
  <b> kubectl run </b>  and u will get this list . 
  