**Containers and Microservices
**
**Divide an application into microservices :**/feed and /user backends are separated into
independent projects.

**Build and run a container image using Docker:** Project includes Dockerfiles to successfully create Docker images for /feed, /user backends, project frontend, and reverse proxy. Screenshot of DockerHub shows the images.

**Independent Releases and Deployments
**
**Use Travis to build a CI/CD pipeline**: Screenshot of the Travis CI interface shows a successful build and deploy job.

**Service Orchestration with Kubernetes
**
Deploy microservices using a Kubernetes cluster on AWS: A screenshots of kubectl commands show the Frontend and API projects deployed in Kubernetes.The output of kubectl get pods indicates that the pods are running successfully with the STATUS value Running.

The output of kubectl describe services does not expose any sensitive strings such as database passwords.

**Use a reverse proxy to direct requests to the appropriate backend:** Screenshot of Kubernetes services shows a reverse proxy

**Configure scaling and self-healing for each service**: Kubernetes services are replicated. At least one of the Kubernetes services has replicas: defined with a value greater than 1 in itsdeployment.yml file. Screenshot of Kubernetes cluster of command kubectl describe hpa has autoscaling configured with CPU metrics.

**Use logs to capture metrics for debugging a microservices deployment:** Screenshot of one of the backend API pod logs indicates user activity that is logged when an API call is made.

