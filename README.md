# eks-3-frontend-microservices

# create cluster using eksctl
```
eksctl create cluster -f /Users/ranjiniganeshan/udemy/Argocd/dev-cluster.yaml
```
# Argo CD Installation 
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl -n argocd patch svc argocd-server -p '{"spec": {"type": "LoadBalancer"}}'
kubectl -n argocd get svc argocd-server
```
```
git clone https://github.com/udemykcloud/eks-3-frontend-microservices.git
kubectl apply -f /Users/ranjiniganeshan/udemy/Argocd/guestbook-ui-workflow/eks-3-frontend-microservices/app-frontend-1.yaml
application.argoproj.io/frontend-1 created
ranjiniganeshan@Ranjinis-MacBook-Pro eks-3-frontend-microservices % kubectl apply -f /Users/ranjiniganeshan/udemy/Argocd/guestbook-ui-workflow/eks-3-frontend-microservices/app-frontend-2.yaml

application.argoproj.io/frontend-2 created
ranjiniganeshan@Ranjinis-MacBook-Pro eks-3-frontend-microservices % kubectl apply -f /Users/ranjiniganeshan/udemy/Argocd/guestbook-ui-workflow/eks-3-frontend-microservices/app-frontend-3.yaml 
application.argoproj.io/frontend-3 created
```

<img width="1509" height="779" alt="Screenshot 2025-09-18 at 8 16 14 PM" src="https://github.com/user-attachments/assets/f1b943aa-8dd3-4fdc-a167-6d06aa70751c" />

