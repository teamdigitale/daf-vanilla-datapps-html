This is the skeleton for build html application inside Daf project

You can integrate you code editing index.html component.

Follow this steps in order to deploy the app inside the Daf environment: 

1. change <daf-skeleton-html> with your app name (<your-app-name>) inside daf-skeleton.yml file
2. sudo docker build --no-cache -t nexus.teamdigitale.test/<your-app-name>:1.0.0 .
3. sudo docker push nexus.teamdigitale.test/<your-app-name>:1.0.0
4. kubectl delete -f kubernetes/test/daf-skeleton.yml (not the first time!!!)
5. kubectl create -f kubernetes/test/daf-skeleton.yml
