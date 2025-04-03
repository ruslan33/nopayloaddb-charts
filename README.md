# nopayloaddb_charts
Helm-charts for NoPayloadDB deployments

## Checkout
To clone the repository, use the following command:

```bash
git clone https://github.com/BNLNPPS/nopayloaddb-charts.git
```

## Copy values
You need to copy your configuration values into the appropriate charts.

### sPHENIX:
```bash
cp /path/to/your/values/values.yaml nopayloaddb-charts/npdbchart_sphenix
```

### Belle2 Java:
```bash
cp /path/to/your/values/values.yaml nopayloaddb-charts/npdbchart_belle2_java
```

## oc and helm commands

Make sure you are in the directory where `oc` and `helm` are installed.

### Login
```bash
oc login --token='YOUR_TOKEN'
```

### Enter your project
```bash
oc project <project-name>
```

### List helm releases in the current namespace
```bash
helm list
```

### Upgrade a helm release
```bash
helm upgrade <helm-release-name> /path/to/your/helm-charts/nopayloaddb-charts/npdbchart_YOUR_EXPERIMENT
```

### Uninstall a helm release
```bash
helm uninstall RELEASE
```
### Install a helm release
```bash
helm install <helm-release-name> /path/to/your/helm-charts/nopayloaddb-charts/npdbchart_YOUR_EXPERIMENT
```

### Get pods
```bash
oc get pods
```

### Get pod logs
```bash
oc logs <pod-name>
```

### Get pod events
```bash
oc describe pod <pod-name>
```

### Get image streams
```bash
oc get imagestreams
```

### Get image stream events
```bash
oc describe imagestream <image-stream-name>
```

### Deleting the pod
In most cases, deleting the pod fixes all issues. A new pod will be automatically spawned.

```bash
oc delete pod <pod-name>
```

## Creator and Contact
- **Creator:** Ruslan Mashinistov (BNL)
