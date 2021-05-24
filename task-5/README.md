# Create a Cloud SQL instance

In task-5, we will follow these steps:

1. Set the INSTANCE_NAME environment variable using:
```bash
export INSTANCE_NAME=mysql-wordpress-instance
```
2. Create a sql instance using:
```bash
gcloud sql instances create $INSTANCE_NAME
```
3. Add the instance connection name as an environment variable:
```bash
export INSTANCE_CONNECTION_NAME=$(gcloud sql instances describe $INSTANCE_NAME \
    --format='value(connectionName)')
```
4. Create a database for WordPress to store its data:
```bash
gcloud sql databases create wordpress --instance $INSTANCE_NAME
```
5. Create a database password for WordPress to authenticate to the instance:
```bash
export CLOUD_SQL_PASSWORD=$(openssl rand -base64 18)
```
6. Create a database user called `wordpress`.
```bash
gcloud sql users create wordpress --host=% --instance $INSTANCE_NAME \
    --password $CLOUD_SQL_PASSWORD
```
7. Let's see the `password` using:
```bash
echo $CLOUD_SQL_PASSWORD
```
**Note**:
If you close your Cloud Shell session, you lose the password. Make a note of the password because you will need it later.
