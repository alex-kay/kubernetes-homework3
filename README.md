# kubernetes-homework3

## Task 3: application with persistance

* Find an app wich requires some type of persistance: Suggestions:Blog, Task Manager, Address database... Deploy this on the cluster using persisntant storage
* Specify the PV/PVC size to be 10 Gi or less
* Useful links: [Persistent Volumes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/)

## Task steps

1. First idea is to deploy a simple wordpress app. Read the following tutorial: [Example: Deploying WordPress and MySQL with Persistent Volumes](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)

2. Deployed all using `kubectl apply -k ./` (example was using Kustomize).

3. Deployed successfully, using same ingress from second task. Changed the tutorial code just a bit, changing storage class and resource requests. [Deployed app link](alex-wp.kubelab.spainip.es)

4. Added nodeSelector for pod templates on deployments for only storage_database:true nodes.

5. *Todo: check volumes, like uploading pictures to wordpress and checking files on the mounts.*
