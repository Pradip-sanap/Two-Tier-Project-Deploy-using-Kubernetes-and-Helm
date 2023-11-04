create template for flaskapp and mysql using below command:
helm create flaskapp-chart
helm create mysql-chart

Do changes in values file in both chart according to project.
Install mysql-chart on kubernetes:
helm install mysql mysql-chart

copy service ip of mysql  and paste it into values file for mysqlhost.

Install flaskapp-chart:
helm install flaskapp flaskapp-chart

-------------------------------------------------------
Check deployment:
kubectl get all

For minikube users, below command use for exposing service to outside.
minikube service flask-app-flaskapp-chart

Use get output in browser.
ThankYou.
