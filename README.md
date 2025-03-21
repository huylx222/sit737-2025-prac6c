### 1. Modify Node.js application
First, change the calculator app, adding Factorial and Logarithm function
### 2. Build and push a new Docker image
* docker build -t lehuy222/calculator-app:6.2c .
* docker push lehuy222/calculator-app:6.2c
  
### 3. Update Kubernetes deployment
* bashCopykubectl set image deployment/calculator-app-deployment calculator-app=lehuy222/calculator-app:5.2p

### 4. Verify the update
* bashCopykubectl rollout status deployment/calculator-app-deployment
* kubectl get pods

### 5. Check the code running
* minikube service calculator-app-service
