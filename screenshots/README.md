# Screenshots

To help review your infrastructure, please include the following screenshots in this directory::

## Deployment Pipeline

- DockerHub showing containers that you have pushed
  ![images](https://raw.githubusercontent.com/alkaj/monolith2microservices/master/screenshots/images.png)
- GitHub repository’s settings showing your Travis webhook (can be found in Settings - Webhook)
  ![settings](https://raw.githubusercontent.com/alkaj/monolith2microservices/master/screenshots/travis_integration.png)
- Travis CI showing a successful build and deploy job  
  Builds will triggered everytime a push request is made to the master branch, and a docker image will be generated using the dockerfile in the directory relative to the branch and will be pushed to DockerHub.

  ![travis](https://raw.githubusercontent.com/alkaj/monolith2microservices/master/screenshots/travis-ci_passing.png)

## Kubernetes

- To verify Kubernetes pods are deployed properly

```bash
kubectl get pods
```

![k8s](https://raw.githubusercontent.com/alkaj/monolith2microservices/master/screenshots/pods_running.png)

- To verify Kubernetes services are properly set up

```bash
kubectl describe services
```

![k8s](https://raw.githubusercontent.com/alkaj/monolith2microservices/master/screenshots/describe_services_1_2.png)  
![k8s](https://raw.githubusercontent.com/alkaj/monolith2microservices/master/screenshots/describe_services_2_2.png)

- To verify that you have horizontal scaling set against CPU usage

```bash
kubectl describe hpa
```

![k8s](https://raw.githubusercontent.com/alkaj/monolith2microservices/master/screenshots/autoscaled_deployment.png)

- To verify that you have set up logging with a backend application

```bash
kubectl logs {pod_name}
```

![feed log](https://raw.githubusercontent.com/alkaj/monolith2microservices/master/screenshots/feed_api_log.png)
