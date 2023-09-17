# gcloud CLI commands Cheatsheet

---

This Article consists of gcloud commands which can be handy when working on google cloud shell to manage/automate the infrastructure components. 
Official documentation can be found at <a target="_blank" href=https://cloud.google.com/sdk/docs/cheatsheet>gcloud official doc</a>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

---

 {!inpage-ads.md!}

## Get going with the gcloud

* Initialize, authorize, and configure gcloud

        gcloud init

* Display version + installed components

        gcloud version

* Install specific components

        gcloud components install COMPONENT_NAME

* Update your Cloud SDK to the latest version

        gcloud components update 

* Set a default Google Cloud project to work on

        gcloud config set project

* Display current gcloud environment details

        gcloud info

        * For apt-get and yum, see https://cloud.google.com/sdk/install



## Google Compute Engine commands

* List zones in Region:  

          gcloud  compute zones list | grep us-central1

* Set default zone for new vm:   

          gcloud  config set compute/zone us-central1-c

* To create a new VM: 

          gcloud  compute instances create "my-vm-2" \
            --machine-type "n1-standard-1" \
            --image-project "debian-cloud" \
            --image-family "debian-10" \
            --subnet "default"

* To create a  Cloud Storage Bucket: 

          gsutil mb -l US gs://$PROJECT_ID

* To list the items in Cloud Storage Bucket:  

          gsutil ls gs://$PROJECT_ID

* To list the set project property in the core section:

		gcloud config list $PROJECT_ID

* To list gcloud named configurations: 

		gcloud config configurations list

* To create a new named configuration:

		gcloud config configurations create my-second-config

* To activate sepcific named configuration: 

		gcloud config configurations activate my-default-configuration

* To list the properties of the specified section using the active configuration:

		gcloud config list

* To see your currently available accounts used for `gcloud` authentication: 

		gcloud config list account

* To describe a named configuration by listing its properties: 

		gcloud config configurations describe my-second-configuration

* To display all Compute Engine instances in a project: 

		gcloud compute instances list

* To create Compute Engine virtual machine instances:

		gcloud compute instances create

* To display all data associated with a Compute Engine virtual machine instance: 

		gcloud compute instances describe my-first-instance-from-gcloud

* To delete Compute Engine virtual machine instances: 

		gcloud compute instances delete my-first-instance-from-gcloud

* To display all Google Compute Engine zones in a project: 

		gcloud compute zones list

* To display all Google Compute Engine regions in a project:

		gcloud compute regions list

* To display all Google Compute Engine machine types in a project: 

		gcloud compute machine-types list

* To display all Google Compute Engine machine types in Zone `asia-southeast2-b`:

		gcloud compute machine-types list --filter zone:asia-southeast2-b

* To filter the Google Compute Engine machine types in multiple zones: 

		gcloud compute machine-types list --filter "zone:(asia-southeast2-b asia-southeast2-c)"

* To display all data associated with a Compute Engine region: 

		gcloud compute regions describe $REGION

* To list Google Compute Engine instance templates: 

		gcloud compute instance-templates list

* To create a Compute Engine virtual machine instance template: 

		gcloud compute instance-templates create instance-template-from-command-line

* To delete one or more Compute Engine virtual machine instance templates: 

		gcloud compute instance-templates delete instance-template-from-command-line

* To  display all data associated with a Google Compute Engine virtual machine instance template:

		gcloud compute instance-templates describe my-instance-template-with-custom-image

* To list Google Compute Engine managed instance groups: 

		gcloud compute instance-groups managed list

* To delete Compute Engine managed instance groups:  

		gcloud compute instance-groups managed delete my-managed-instance-group

* To create a Compute Engine managed instance group:

		gcloud compute instance-groups managed create my-mig --zone us-central1-a --template my-instance-template \ 
		--size 1

* To set autoscaling parameters of a managed instance group:

		gcloud compute instance-groups managed set-autoscaling my-mig --max-num-replicas=2 --zone us-central1-a

* To stop autoscaling a managed instance group: 

		gcloud compute instance-groups managed stop-autoscaling my-mig --zone us-central1-a

* To set managed instance group size:

		gcloud compute instance-groups managed resize my-mig --size=1 --zone=us-central1-a

* To recreate instances managed by a managed instance group:

		gcloud compute instance-groups managed recreate-instances my-mig --instances=my-mig-85fb --zone us-central1-a

* To delete Compute Engine managed instance groups: 

		gcloud compute instance-groups managed delete my-managed-instance-group --region=us-central1


## Troubleshooting instance ssh issue

        recommendations, rerun the ssh command with the --troubleshoot option.

        gcloud compute ssh instance-1 --project=smitis-dev --zone=us-central1-a --troubleshoot

        Or, to investigate an IAP tunneling issue:

        gcloud compute ssh instance-1 --project=smitis-dev --zone=us-central1-a --troubleshoot --tunnel-through-iap



## Google App Engine commands

* cd default-service
* gcloud app deploy
* gcloud app services list
* gcloud app versions list
* gcloud app instances list
* gcloud app deploy --version=v2
* gcloud app versions list
* gcloud app versions list --hide-no-traffic ==> DO not show version receiving no traffic.
* gcloud app browse
* gcloud app browse --version 20210215t072907
* gcloud app deploy --version=v3 --no-promote
* gcloud app browse --version v3
* gcloud app services set-traffic split=v3=.5,v2=.5
* gcloud app services set-traffic splits=v3=.5,v2=.5
* watch curl https://melodic-furnace-304906.uc.r.appspot.com/
* gcloud app services set-traffic --splits=v3=.5,v2=.5 --split-by=random
* cd ../my-first-service/
* gcloud app deploy
* gcloud app browse --service=my-first-service
* gcloud app services list
* gcloud app regions list
* gcloud app browse --service=my-first-service --version=20210215t075851
* gcloud app browse --version=v2
* gcloud app open-console --version=v2
* gcloud app versions list --hide-no-traffic



## Google Kubernetes Engine commands

* gcloud config set project my-kubernetes-project-304910
* gcloud container clusters get-credentials my-cluster --zone us-central1-c --project my-kubernetes-project-304910
* kubectl create deployment hello-world-rest-api --image=in28min/hello-world-rest-api:0.0.1.RELEASE
* kubectl get deployment
* kubectl expose deployment hello-world-rest-api --type=LoadBalancer --port=8080
* kubectl get services
* kubectl get services --watch
* curl 35.184.204.214:8080/hello-world
* kubectl scale deployment hello-world-rest-api --replicas=3
* gcloud container clusters resize my-cluster --node-pool default-pool --num-nodes=2 --zone=us-central1-c
* kubectl autoscale deployment hello-world-rest-api --max=4 --cpu-percent=70
* kubectl get hpa
* kubectl create configmap hello-world-config --from-literal=RDS_DB_NAME=todos
* kubectl get configmap
* kubectl describe configmap hello-world-config
* kubectl create secret generic hello-world-secrets-1 --from-literal=RDS_PASSWORD=dummytodos
* kubectl get secret
* kubectl describe secret hello-world-secrets-1
* kubectl apply -f deployment.yaml
* gcloud container node-pools list --zone=us-central1-c --cluster=my-cluster
* kubectl get pods -o wide
* kubectl set image deployment hello-world-rest-api hello-world-rest-api=in28min/hello-world-rest-api:0.0.2.RELEASE
* kubectl get services
* kubectl get replicasets
* kubectl get pods
* kubectl delete pod hello-world-rest-api-58dc9d7fcc-8pv7r
* kubectl scale deployment hello-world-rest-api --replicas=1
* kubectl get replicasets
* gcloud projects list
* kubectl delete service hello-world-rest-api
* kubectl delete deployment hello-world-rest-api
* gcloud container clusters delete my-cluster --zone us-central1-c
* kubectl create deployment hello-world-rest-api --image=in28min/hello-world-rest-api:0.0.1.RELEASE


*  Create GKE cluster using below gcloud command:

          gcloud beta container clusters create test-cluster-1 \
           --zone=us-central1-a \
           --num-nodes=3 \
           --machine-type=n1-standard-1 \
           --disk-size=100 \
           --disk-type=pd-standard \
           --image-type=COS \
           --enable-autorepair \
           --enable-autoupgrade \
           --enable-autoscaling \
           --max-nodes=3 \
           --min-nodes=0

## Google IAM commands

* 		gcloud compute project-info describe
* 		gcloud auth list
* 		gcloud projects get-iam-policy glowing-furnace-304608
* 		gcloud projects add-iam-policy-binding glowing-furnace-304608 --member=user:in28minutes@gmail.com --role=roles/storage.objectAdmin
* 		gcloud projects remove-iam-policy-binding glowing-furnace-304608 --member=user:in28minutes@gmail.com --role=roles/storage.objectAdmin
* 		gcloud iam roles describe roles/storage.objectAdmin
* 		gcloud iam roles copy --source=roles/storage.objectAdmin --destination=my.custom.role --dest-project=glowing-furnace-304608


## Cloud SQL

* 		gcloud sql connect my-first-cloud-sql-instance --user=root --quiet
* 		gcloud config set project glowing-furnace-304608
* 		gcloud sql connect my-first-cloud-sql-instance --user=root --quiet
       *  		use todos
      * 		create table user (id integer, username varchar(30) );
      * 		describe user;
      * 		insert into user values (1, 'Ranga');
      * 		select * from user


## Cloud BigTable

* 		bq show bigquery-public-data:samples.shakespeare
* 		gcloud --version
* 		cbt listinstances -project=glowing-furnace-304608
* 		echo project = glowing-furnace-304608 > ~/.cbtrc
* 		cat ~/.cbtrc
* 		cbt listinstances


## Pub/Sub

* 		gcloud config set project glowing-furnace-304608
* 		gcloud pubsub topics create topic-from-gcloud
* 		gcloud pubsub subscriptions create subscription-gcloud-1 --topic=topic-from-gcloud
* 		gcloud pubsub subscriptions create subscription-gcloud-2 --topic=topic-from-gcloud
* 		gcloud pubsub subscriptions pull subscription-gcloud-2
* 		gcloud pubsub subscriptions pull subscription-gcloud-1
* 		gcloud pubsub topics publish topic-from-gcloud --message="My First Message"
* 		gcloud pubsub topics publish topic-from-gcloud --message="My Second Message"
* 		gcloud pubsub topics publish topic-from-gcloud --message="My Third Message"
* 		gcloud pubsub subscriptions pull subscription-gcloud-1 --auto-ack
* 		gcloud pubsub subscriptions pull subscription-gcloud-2 --auto-ack
* 		gcloud pubsub topics list
* 		gcloud pubsub topics delete topic-from-gcloud
* 		gcloud pubsub topics list-subscriptions my-first-topic

---

<br>

{!footer.md!}
