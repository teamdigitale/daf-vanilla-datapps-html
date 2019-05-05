This is the skeleton for build and deploy static html application inside PDND project

You can integrate your code editing index.html component. After modyfing index.html you 
can follow the steps below. 

**Remember: ASK to the ifrastructure administration to change manually the kubernetes ingress
for going live on the internet

### Prerequisites
You can read the necessary setup for test and prod [here](https://github.com/teamdigitale/daf-operational/blob/master/docs/readme.md)


- PDND VPN access for test or prod
- kubectl configured
- docker

### Steps for deploying
Follow this steps in order to deploy the app inside the Daf environment: 

1. change <daf-skeleton-html> with your app name YOUR-APP-NAME inside daf-skeleton.yml file
2. sudo docker build --no-cache -t nexus.teamdigitale.test/YOUR-APP-NAME:1.0.0 .
3. sudo docker push nexus.teamdigitale.test/YOUR-APP-NAME:1.0.0
4. kubectl delete -f kubernetes/test/daf-skeleton.yml (not the first time!!!)
5. kubectl create -f kubernetes/test/daf-skeleton.yml
