# k8s-mongo-express-demo

## Prerequisite

* [Minikube](https://v1-18.docs.kubernetes.io/docs/tasks/tools/install-minikube/)
* [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

## Getting started

1. Enable Ingress Controller addon:
    ```bash
    $ minikube addon enable ingress
    ```
2. Setup ConfigMap & Secret:
    ```bash
    $ kubectl apply -f mongo-secrets.yml -f mongo-configmap.yml
    ````
3. Deploy MongoDB:
    ```bash
    $ kubectl apply -f mongodb.yml
    ````
4. Deploy Mongo Express:
    ```bash
    $ kubectl apply -f mongodb-express.yml
    ````
5. Apply Ingress config:
    ```bash
    $ kubectl apply -f mongodb-ingress.yml
    ```
