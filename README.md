# Welcome to Flashbacker

Flashbacker is a minimalist app which helps you to save the precious memories of your life in a form
of tiny written stories. It's not a tool for writing a journal, it's more like a space for the "tweets"
you send to your future self to be able to relive the moments which were special for you.

## Introduction
This branch contains the Kubernetes manifests for the QA environment only.

For the project code please refer to:
  * [https://gitlab.com/flashbacker/backend](https://gitlab.com/flashbacker/backend)
  * [https://gitlab.com/flashbacker/frontend](https://gitlab.com/flashbacker/frontend)

## Create DynamoDB secret

```
kubectl create secret generic dynamodb-secret --from-literal=FLASHBACKER_DYNAMODB_ENDPOINT=http://dynamodb-local-service:8000 --from-literal=FLASHBACKER_DYNAMODB_REGION=
```

## Create Cognito secret

```
kubectl create secret generic cognito-secret --from-literal=FLASHBACKER_COGNITO_REGION=<value> --from-literal=FLASHBACKER_COGNITO_USER_POOLS_ID=<value> --from-literal=FLASHBACKER_COGNITO_USER_POOLS_WEB_CLIENT_ID=<value> --from-literal=FLASHBACKER_COGNITO_DOMAIN=<value> --from-literal=FLASHBACKER_COGNITO_REDIRECT_SIGN_IN=<value> --from-literal=FLASHBACKER_COGNITO_REDIRECT_SIGN_OUT=<value>
```

## Create GitLab registry secret

```
kubectl create secret docker-registry gitlab-registry-secret --docker-server=registry.gitlab.com --docker-username=vasas --docker-password=<token>
```
