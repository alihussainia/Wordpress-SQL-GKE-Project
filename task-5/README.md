# Configure a `Service Account` and Create `Secrets`

In task-5, we will follow these steps:

1. Create a service account using:
```bash
SA_NAME=cloudsql-proxy
gcloud iam service-accounts create $SA_NAME --display-name $SA_NAME
```
2. Add the service account email address as an environment variable using:
```bash
SA_EMAIL=$(gcloud iam service-accounts list \
    --filter=displayName:$SA_NAME \
    --format='value(email)')
```
3. Add the cloudsql.client role to your service account using:
```bash
gcloud projects add-iam-policy-binding $PROJECT_ID \
    --role roles/cloudsql.client \
    --member serviceAccount:$SA_EMAIL
```
4. Create a key for the service account using:
```bash
gcloud iam service-accounts keys create $WORKING_DIR/key.json \
    --iam-account $SA_EMAIL
```
5. Create a Kubernetes secret for the MySQL credentials using:
```bash
kubectl create secret generic cloudsql-db-credentials \
    --from-literal username=wordpress \
    --from-literal password=$CLOUD_SQL_PASSWORD
```
6. Create a Kubernetes secret for the service account credentials using:
```bash
kubectl create secret generic cloudsql-instance-credentials \
    --from-file $WORKING_DIR/key.json
```
