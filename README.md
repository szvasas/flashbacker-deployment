This project contains the Kubernetes manifests you can use to deploy Flashbacker to a cluster.
The secrets to access DynamoDB, Cognito and GitLab registry have to be created the following way:

```
kubectl create secret generic dynamodb-secret --from-literal=FLASHBACKER_DYNAMODB_ENDPOINT=http://dynamodb-local-service:8000 --from-literal=FLASHBACKER_DYNAMODB_REGION=
```

```
kubectl create secret generic cognito-secret --from-literal=FLASHBACKER_COGNITO_REGION=<value> --from-literal=FLASHBACKER_COGNITO_USER_POOLS_ID=<value> --from-literal=FLASHBACKER_COGNITO_USER_POOLS_WEB_CLIENT_ID=<value> --from-literal=FLASHBACKER_COGNITO_DOMAIN=<value> --from-literal=FLASHBACKER_COGNITO_REDIRECT_SIGN_IN=<value> --from-literal=FLASHBACKER_COGNITO_REDIRECT_SIGN_OUT=<value>
```

```
kubectl create secret docker-registry regcred --docker-server=registry.gitlab.com --docker-username=vasas --docker-password=<token>
```
