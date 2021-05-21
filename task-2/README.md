# Creating GKE Cluster

1. Set the CLUSTER_NAME environment variable using:
```bash
export CLUSTER_NAME=wordpress-project
```

2. Create a `3 node` Kubernetes cluster on GKE using:

```bash
gcloud container clusters create $CLUSTER_NAME \
    --num-nodes=3 --enable-autoupgrade --no-enable-basic-auth \
    --no-issue-client-certificate --enable-ip-alias --metadata \
    disable-legacy-endpoints=true
```

Reference: https://cloud.google.com/sdk/gcloud/reference/container/clusters/create#
