# Creating GKE Cluster

Create a `3 node` Kubernetes cluster on GKE using:

```bash
CLUSTER_NAME=wordpress-project
gcloud container clusters create $CLUSTER_NAME \
    --num-nodes=3 --enable-autoupgrade --no-enable-basic-auth \
    --no-issue-client-certificate --enable-ip-alias --metadata \
    disable-legacy-endpoints=true
```
