# kubernetes--tips

## start a pod 
kubectl run mypod --image nginx

## operations on pod
kubectl exec --stdin --tty mypod -- sh

kubectl exec --stdin --tty mypod -- ls

kubectl exec  mypod -- ps 

https://reviewnprep.com/blog/cheat-sheet-kubernetes-and-linux-commands/#Creating_and_Updating_a_Resource

kubectl get component status


# Wait for pod to start 
kubectl get pods -w --namespace default

NAME                 READY   STATUS    RESTARTS   AGE
mysql-1685213458-0   0/1     Pending   0          105s


# Getting certificates from cluster 

kubectl config view --minify --flatten --context kind-terraform


# affinity and labeles 

affinity:
    nodeAffinity:
      requiredDuringSchedulingIgnoredDuringExecution:
        nodeSelectorTerms:
          - matchExpressions:
              - key: special
                operator: Exists
                
                
# Label the node 
kubectl label nodes kind-cluster-control-plane  special=true

#Unlabeling 
kubectl label node kind-cluster-control-plane special-

# Troubleshoot deployment issues full guide
https://learnk8s.io/troubleshooting-deployments

Cluster auto-scaler 
https://aws.github.io/aws-eks-best-practices/cluster-autoscaling/

https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler/FAQ.md

https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler/FAQ.md#what-types-of-pods-can-prevent-ca-from-removing-a-node





