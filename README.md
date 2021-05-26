# Deploying `WordPress` with `MySQL` on GKE

This project shows how to set up a single-replica WordPress deployment on Google Kubernetes Engine (GKE) using a MySQL database. Instead of installing MySQL, we will use Cloud SQL, which provides a managed version of MySQL.

# Pre-requisite:

1. Google Cloud Account.
2. Enabled Billing.

# Tasks
1. Project Creation.
2. Set-up environment.
3. Create a 3 node GKE cluster.
4. Create a PV and a PVC.
5. Create a Cloud SQL instance.
6. Configure a Service Account & Create Secrets.
7. Deploy WordPress.
8. Expose the WordPress service.
9. Set-up your WordPress blog.
10. Wind up the Project. 
