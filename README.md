# GADS_Learning_Phase_2_Practice_Project_Submission
This is the project submission GADS Learning Phase 2 by **Ayman Ahmed**
## Part 1: Completed Qwiklabs:

### 1. GCP Fundamentals: Getting Started with Cloud Marketplace
![](/Qwiklabs_screenshots/1-%20GCP%20Fundamentals:%20Getting%20Started%20with%20Cloud%20Marketplace.png)



### 2. GCP Fundamentals: Getting Started with Compute Engine
![](/Qwiklabs_screenshots/2-%20%20GCP%20Fundamentals:%20Getting%20Started%20with%20Compute%20Engine.png)



### 3. Google Cloud Fundamentals: Getting Started with GKE
![](/Qwiklabs_screenshots/3%20-%20Google%20Cloud%20Fundamentals:%20Getting%20Started%20with%20GKE.png)



### 4. Google Cloud Fundamentals: Getting Started with App Engine
![](/Qwiklabs_screenshots/4-%20Google%20Cloud%20Fundamentals:%20Getting%20Started%20with%20App%20Engine.png)



### 5. Google Cloud Fundamentals: Getting Started with Deployment Manager and Cloud Monitoring
![](/Qwiklabs_screenshots/5.%20Google%20Cloud%20Fundamentals:%20Getting%20Started%20with%20Deployment%20Manager%20and%20Cloud%20Monitoring.png)



### 6. Console and Cloud Shell
![](/Qwiklabs_screenshots/6.%20Console%20and%20Cloud%20Shell%20.png)



### 7. Infrastructure Preview
![](/Qwiklabs_screenshots/7.%20Infrastructure%20Preview%20.png)



### 8. Creating Virtual Machines
![](/Qwiklabs_screenshots/8.Creating%20Virtual%20Machines.png)



### 9. Classify Images with Pre-built ML Models using Cloud Vision API and AutoML
![](/Qwiklabs_screenshots/9.%20Classify%20Images%20with%20Pre-built%20ML%20Models%20using%20Cloud%20Vision%20API%20and%20AutoML.png)



### 10. Automating the Deployment of Infrastructure Using Deployment Manager
![](/Qwiklabs_screenshots/10.%20Automating%20the%20Deployment%20of%20Infrastructure%20Using%20Deployment%20Manager.png)



### 11. Automating the Deployment of Infrastructure Using Terraform
![](/Qwiklabs_screenshots/11.%20Automating%20the%20Deployment%20of%20Infrastructure%20Using%20Terraform.png)



### 12. Introduction to Containers and Docker v1.6
![](/Qwiklabs_screenshots/12.%20Introduction%20to%20Containers%20and%20Docker%20v1.6.png)

## Part 2: Translation projects from Console instructions command line instructions

### 1. GCP Fundamentals: Getting Started with Compute Engine

```
# Create a virtual machine using the GCP Console

gcloud compute zones list | grep us-central1

gcloud config set compute/zone us-central1-a

gcloud compute instances create "my-vm-1" --machine-type "n1-standard-1" --image-project "debian-cloud" --image "debian-9-stretch-v20190213" --subnet "default"


# Create second virtual machine using the GCP Console

gcloud config set compute/zone us-central1-b

gcloud compute instances create "my-vm-2" --machine-type "n1-standard-1" --image-project "debian-cloud" --image "debian-9-stretch-v20190213" --subnet "default"

# To open a command prompt on the my-vm-2 instance, click SSH in its row in the VM instances list.

ping my-vm-1

ssh my-vm-1

sudo apt-get install nginx-light -y

sudo nano /var/www/html/index.nginx-debian.html

# below the h1 header place Hi from YOUR_NAME

curl http://localhost/

exit

# To open a command prompt on the my-vm-1 instance, click SSH in its row in the VM instances list.

curl http://my-vm-1/

```


### 2. Google Cloud Fundamentals: Getting Started with App Engine

```
gcloud auth list

gcloud config list project

gcloud app create --project=$DEVSHELL_PROJECT_ID

git clone https://github.com/GoogleCloudPlatform/python-docs-samples

cd python-docs-samples/appengine/standard_python3/hello_world

sudo apt-get update

sudo apt-get install virtualenv

virtualenv -p python3 venv

source venv/bin/activate

pip install  -r requirements.txt

python main.py

cd ~/python-docs-samples/appengine/standard_python3/hello_world

gcloud app deploy

gcloud app browse
```



### 3. Google Cloud Fundamentals: Getting Started with GKE

```
export MY_ZONE=us-central1-a

gcloud container clusters create webfrontend --zone $MY_ZONE --num-nodes 2

kubectl version

kubectl create deploy nginx --image=nginx:1.17.10

kubectl get pods

kubectl expose deployment nginx --port 80 --type LoadBalancer

kubectl get services

kubectl scale deployment nginx --replicas 3

kubectl get pods

kubectl get services
```



