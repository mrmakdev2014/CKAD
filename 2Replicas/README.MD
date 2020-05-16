# Repllicas 
the target of the replicas is to ensure high availability for the pods , so if one of the pods down for any reason , the repica controller will start anew pod
anther reason is to scale and load balance request between multipe pods . 

There's two similar terms ( Repication Controller , replicaset)
the first is the old way and the second in the new way to implement repliation

# How Create Repication Controller 
the below link 
https://raw.githubusercontent.com/kubernetes/website/master/content/en/examples/controllers/replication.yaml

<img src="replicationcontroller.png />