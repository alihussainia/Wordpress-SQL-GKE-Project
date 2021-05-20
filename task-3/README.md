# Creating a PV and PVC

In task-3, we will follow these steps:

1. Deploy the `PVC` manifest for Wordpress using:
```bash
kubectl apply -f $WORKING_DIR/task-3/wordpress-volumeclaim.yaml
```
2. Check the status:
```bash
kubectl get persistentvolumeclaim
```