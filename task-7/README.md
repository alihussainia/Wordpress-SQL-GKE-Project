# Deploy WordPress

In task-6, we are going to follow these steps:

1. Prepare the wordpress_cloudsql.yaml file using:
```bash
cat $WORKING_DIR/task-6/wordpress_cloudsql.yaml.template | envsubst > \
    $WORKING_DIR/wordpress_cloudsql.yaml
```
2. Deploy the wordpress_cloudsql.yaml manifest file using:
```bash
kubectl create -f $WORKING_DIR/wordpress_cloudsql.yaml
```
3. Watch the deployment status using:
```bash
kubectl get pod -l app=wordpress --watch
```
