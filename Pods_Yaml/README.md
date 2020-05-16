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

Please not that pod name is unique so you can't have two pods with the same name inside the same namespace

#POD File notes:-
    the labels section inside metadata , can contain any key value .
    containers is list as the pod can contain multiple Containers ( images )
    so the first item start with - name .
    
spec:
  containers:
  - name: myapp_nginx
    image: nginx
    resources:
      limits:
        memory: "128Mi"
        cpu: "500m"
    ports:
      - containerPort: 80


kubectl create -f pod-nginx.yaml 
kubectl create -f pod-nginx.yaml 
# Create empty file pod.yaml 
touch pod.yaml

# to delete pod 
kubectl delete pod demoapp ( Pod Name)
kubectl delete pod nginx1234-5f686c77fc-26sr8


#to delete any resouce just type 
kubectl delete resouceName 
kubectl delete service/azure-vote-front 
kubectl delete deployment/azure-vote-front


