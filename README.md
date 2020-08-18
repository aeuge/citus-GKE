# citus-GKE
manifests for Citus in Google Kubernetes Engine

change password in secrets:
echo -n 'otus321$' | base64
kubectl create -f secrets.yaml
kubectl create -f master.yaml
kubectl create -f workers.yaml
psql -h <load balancer ip> -U postgres --password -p 5432
