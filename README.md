# ibm-festival-app-deployment
This repository contains all the important YAML resources needed to run the application on an OpenShift cluster.



## Application deployment over multiple "stages"
For simplicity, the various stages are implemented here in a cluster and over multiple namespaces. Of course, the namespaces can also be located on other OpenShift clusters, but for this they must be set up. ArgoCD then also requires not insignificant changes in its configuration.


### Create Namespaces
```bash
$ oc new-project ibm-festival-dev-java-example --description="Our app in dev stage" --display-name="ibm-festival-dev-java-example"
```
