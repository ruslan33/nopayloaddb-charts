# nopayloaddb_charts
Helm-charts for NoPayloadDB deployments

# Checkout
git clone https://github.com/BNLNPPS/nopayloaddb-charts.git

# Copy values
#sPHENIX:
cp /path/to/your/values/values.yaml nopayloaddb-charts/npdbchart_sphenix
#Belle2 Java
cp /path/to/your/values/values.yaml nopayloaddb-charts/npdbchart_belle2_java

# oc and heml commands
#cd to your directory where oc and helm are installed
#Login
oc login --token='YOUR_TOKEN'
#Enter to your project
oc project <project-name>
#List helm release in current namespace
helm list
#Upgrade helm release
helm upgrade <helm-release-name> /path/to/your/helm-charts/nopayloaddb-charts/npdbchart_YOUR_EXPERIMENT
#Uninstall
helm uninstall RELEASE
#Install
helm install <helm-release-name> /path/to/your/helm-charts/nopayloaddb-charts/npdbchart_YOUR_EXPERIMENT
#Get pods
oc get pods
#Get pod logs
oc logs <pod-name>
#Get pod events
oc describe pod <pod-name>
#Get image streams
oc get imagestreams
#Get image stream events
oc describe imagestream <image-stream-name>
#In most cases deleting the pod fixes all issues. New pod will be automatically spawned
oc delete pod <pod-name>
