
kubectl get nodes.
/# to display list of nodes #/

kubectl get nodes -o wide
/# iit will shode detailed info like os.docker version. ip address...#/

kubectl get pods
/# to display pods#/

kubectl get rc
/# display list of replication controllers#/

kubectl apply -f hellowworldpod.yml
/# to create pod using pod.yml file #/

kubectl delete -f <hellowworldpod.yml>
/# to delete pod using pod.yml file#/
	or
kubectl delete pod <pod name>
/# to delete specific pod #/

kubectl get pods --all-namespaces
/# to display pods including k8s pods also(etcd, apiserver, flannel, proxy, sheduler, controller...) #/

service commands:
kubectl get svc
kubectl descrive service <servicename>

Deploy commands:
kubectl create -f <deploy file>
kubectl get deploy
kubectl describe deploy <deployment name>
kubectl get rs (replication set which is usefull for rollout deployments)


update deployment:

kubectl apply -f <deploy file> --record
kubectl rollout status deployments <deployment name>
kubectl get deploy <deployment name>
kubectl get rs

rolback deployment:

kubectl rollout undo deployment <deployment name> --to-revision=1
kubectl get deploy


