# Exposing the WordPress service

In task-8, we will expose WordPress service using these steps:

1. Create a Service of type:LoadBalancer using:
```bash
kubectl create -f $WORKING_DIR/task-8/wordpress-service.yaml
```
2. Watch the `service` deployment status:
```bash
kubectl get svc -l app=wordpress --watch
```
Note: Make a note of the EXTERNAL_IP address to use later.
