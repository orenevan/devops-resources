# kubernetes--tips

## start a pod 
kubectl run mypod --image nginx

## operations on pod
kubectl exec --stdin --tty mypod -- sh

kubectl exec --stdin --tty mypod -- ls

kubectl exec  mypod -- ps 

https://reviewnprep.com/blog/cheat-sheet-kubernetes-and-linux-commands/#Creating_and_Updating_a_Resource

kubectl get component status

## get context 

kubectl config current-context


kubectl config get-contexts


kubectl config use-context arn:aws:eks:us-east-1:250364183413:cluster/DG-STAGE-EKS




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

#  Deploy & troubleshoot pods 
execute nslookup on pod
kubectl run -n orenevan -it --rm --image=tutum/dnsutils --restart=Never nslookup nslookup dg1.tlv.datagen.tech
Testing Network Connectivity — kuryr-kubernetes 8.1.0.dev11 documentation
 
find my egress ip
kubectl run -n ci-runners -it --rm --image=curlimages/curl:7.85.0  --restart=Never curl https://www.showmyip.com/
 
run kubectl aws cli with AWS_ACCESS_KEY_ID + aws s3 command
kubectl run -n services -it --rm --image=amazon/aws-cli --restart=Never export AWS_ACCESS_KEY_ID="YOUR_KEY"; export AWS_SECRET_ACCESS_KEY="YOURSECRET" ; aws s3 ls
 


# Troubleshoot deployment issues full guide
https://learnk8s.io/troubleshooting-deployments

Cluster auto-scaler 
https://aws.github.io/aws-eks-best-practices/cluster-autoscaling/

https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler/FAQ.md

https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler/FAQ.md#what-types-of-pods-can-prevent-ca-from-removing-a-node

## k8 commands & tips 

kubectl get --raw '/healthz?verbose





