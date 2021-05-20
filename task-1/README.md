
# Task#1: Setting up `Environment`:

1. Create a new Google Cloud project with the name `wordpress-demo-01`.
2. Activate Cloud Shell.
3. Enable the GKE and Cloud SQL Admin APIs using:
```bash
gcloud services enable container.googleapis.com sqladmin.googleapis.com
```
4. Set the default region/zone using:
```bash
gcloud config set compute/region us-central1
gcloud config set compute/zone us-central1-a 
```
5. Set the PROJECT_ID environment variable using:
```bash
export PROJECT_ID=wordpress-demo-01
```
6. Clone the GitHub repository using:
```bash
git clone https://github.com/alihussainia/Wordpress-SQL-GKE-Project.git
```
7. Change to the Wordpress-SQL-GKE-Project directory using:
```bash
cd Wordpress-SQL-GKE-Project
```
8. Set the WORKING_DIR environment variable using:
```bash
WORKING_DIR=$(pwd)
```
