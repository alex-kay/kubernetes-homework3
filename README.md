# kubernetes-homework3

## Task 3: application with persistance

* Find an app wich requires some type of persistance: Suggestions:Blog, Task Manager, Address database... Deploy this on the cluster using persisntant storage
* Specify the PV/PVC size to be 10 Gi or less
* Useful links: [Persistent Volumes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/)

## Task steps

1. First idea was to deploy a simple wordpress app. Used the following tutorial: [Example: Deploying WordPress and MySQL with Persistent Volumes](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)

2. Deployed all using `kubectl apply -k ./` (example was using Kustomize).

3. ![wp](img/CleanShot%202021-10-28%20at%2000.14.56@2x.png)

4. Deployed successfully, using same ingress from second task. Changed the tutorial code just a bit, changing storage class and resource requests. [Deployed app link here](https://alex-wp.kubelab.spainip.es)

5. Checked volumes, like uploading pictures to wordpress, recreating pods and checking for persistance.

## Task update

* Exercise:Deploy a stateful app which requires a DB of some sort (or persistent file storage) like a Blog, a Wiki, a Guestbook, Forum.... with storage that will SURVIVE deleting and re-deploying the app
* Tip if you want to use Helm Charts: [Artifact Hub Find, install and publish Kubernetes packages](https://artifacthub.io/)
* And after the app is deployed, convert it into a helm chart
