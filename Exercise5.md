# Exercise 5: Local Deployment

## Objective
Deploy your packaged application locally using either a Vagrant cluster or a Minikube cluster, setting up one database server and one application server.

## Prerequisites
- Completed Exercise 4 (Packaging and Versioning)
- Vagrant or Minikube installed on your local machine
- Basic understanding of Kubernetes (if using Minikube)

## Instructions

1. **Retrieve Your Package**
   - Download the package (Docker image or Vagrant box) you created in Exercise 4 from your chosen artifactory.

2. **Choose Your Deployment Method**
   Select either Vagrant or Minikube for your local deployment:

   ### Option A: Vagrant Cluster
   
   a. Create a Vagrantfile that defines two VMs:
      - One for the database server
      - One for the application server

   b. Configure the Vagrantfile to:
      - Set up networking between the VMs
      - Install necessary software (e.g., Docker, database software)
      - Pull and run your application package

   c. Use `vagrant up` to start your cluster

   ### Option B: Minikube Cluster

   a. Start Minikube:
      ```
      minikube start
      ```

   b. Create Kubernetes manifests for:
      - A deployment for your application
      - A service to expose your application
      - A deployment for your database
      - A service for your database
      - (Optional) A persistent volume for database data

   c. Apply your Kubernetes manifests:
      ```
      kubectl apply -f your-manifests.yaml
      ```

3. **Configure Your Application**
   - Ensure your application is configured to connect to the database server
   - Set any necessary environment variables or configuration files

4. **Verify Deployment**
   - Access your application (via browser or API calls)
   - Confirm that it's connected to the database and functioning correctly

5. **Test Scaling (Optional)**
   - For Vagrant: Create additional application server VMs
   - For Minikube: Scale your application deployment
     ```
     kubectl scale deployment your-app-deployment --replicas=3
     ```

6. **Clean Up**
   - For Vagrant: Run `vagrant destroy`
   - For Minikube: Delete your resources or run `minikube delete`

## Bonus Tasks
1. Implement a load balancer for your application servers
2. Set up monitoring for your local cluster (e.g., Prometheus and Grafana)
3. Implement a simple CI/CD pipeline that deploys to your local cluster on code changes

## Deliverables
1. Vagrantfile or Kubernetes manifests used for deployment
2. Screenshots or terminal output showing:
   - Successful deployment
   - Application running and connected to the database
   - (If attempted) Scaled deployment
3. Brief documentation of your deployment process and any challenges faced

Remember, the goal is to create a local environment that mimics a production setup. This exercise will help you understand the complexities of deploying and managing multi-service applications.
