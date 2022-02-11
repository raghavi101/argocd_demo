# ArgoCD Demo
This is a demo repo to test argocd with a simple main.go application using [net/http](https://pkg.go.dev/net/http) package.
#### Steps 
1. Clone this repository 
```git clone https://github.com/raghavi101/argocd_demo```

2. Start your minikube ```minikube start```

3. Create a namespace "argocd" 
```kubectl create namespace argocd```
4. Refer to [argocd getting started](https://argo-cd.readthedocs.io/en/stable/getting_started/) doc for this step and get your argocd inststance up and running.

5. Apply the application object created for this deployment in argocd namespace ```kubectl apply -n argocd -f application.yaml ```

6. Check and Synchronise your deployment using argocd UI in your localhost.

7. Check your deployment on a different tab ```minikube service my-go-app-service --url``` 

8. Done and Deployed! Now every change you make in your yaml files and apply it to git, argocd will sync your deployment.
