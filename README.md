DevOps Project Setup with Terraform, MicroK8s, and ArgoCD
# GitOps project
MicroK8s & ArgoCD Deployment on Kali WSL



🔧 **Project Structure**
![image](https://github.com/user-attachments/assets/8d3a8d8e-cbe5-401a-a768-a7da872bff35)

Prerequisites :
- Kali Linux WSL2

- Terraform installed (sudo apt install terraform)

- Docker enabled (sudo systemctl enable docker)

**1. Infrastructure Deployment**

> cd terraform
> terraform init
> terraform apply -auto-approve

**2. Verify Installation**
# Check MicroK8s status
> microk8s status

# Verify ArgoCD pods
> kubectl get pods -n argocd

**3. Access ArgoCD**
> kubectl port-forward svc/argocd-server -n argocd 8080:443
