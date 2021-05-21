# Deploying `WordPress` with `MySQL` on GKE

This project shows how to set up a single-replica WordPress deployment on Google Kubernetes Engine (GKE) using a MySQL database. Instead of installing MySQL, we will use Cloud SQL, which provides a managed version of MySQL.

# Pre-requisite:

1. Google Cloud Account.
2. Enabled Billing.

# Tasks
1. Set-up environment.
2. Create a 3 node GKE cluster.
3. Create a PV and a PVC.
4. Create a Cloud SQL instance.
5. Configure a Service Account & Create Secrets.
6. Deploy WordPress.
7. Expose the WordPress service.
8. Set-up your WordPress blog.
9. Wind up the Project. 
