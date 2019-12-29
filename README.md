This project contains the Kubernetes manifests you can use to deploy Flashbacker to a cluster.
The secrets to access DynamoDB and GitLab registry have to be created the following way:

```
kubectl create secret generic dynamodb --from-literal=FLASHBACKER_DYNAMODB_ACCESS_KEY=<access_key> --from-literal=FLASHBACKER_DYNAMODB_SECRET_KEY=<secret_key>  --from-literal=FLASHBACKER_DYNAMODB_REGION=<region>
```
```
kubectl create secret docker-registry regcred --docker-server=registry.gitlab.com --docker-username=vasas --docker-password=<token>
```
