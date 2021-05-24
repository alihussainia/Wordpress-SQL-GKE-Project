
# Setting up `Environment`:
In this task-2, we are going to set up a working environment for our project using the following steps:

1. Enable the GKE and Cloud SQL Admin APIs using:
```bash
gcloud services enable container.googleapis.com sqladmin.googleapis.com
```
2. Set the default region/zone using:
```bash
gcloud config set compute/region us-central1
gcloud config set compute/zone us-central1-a 
```
3. Set the PROJECT_ID environment variable using:
```bash
export PROJECT_ID=wordpress-demo-01
```
4. Clone the GitHub repository using:
```bash
git clone https://github.com/alihussainia/Wordpress-SQL-GKE-Project.git
```
5. Change to the Wordpress-SQL-GKE-Project directory using:
```bash
cd Wordpress-SQL-GKE-Project
```
6. Set the WORKING_DIR environment variable using:
```bash
WORKING_DIR=$(pwd)
```
