```Install kubectl on Linux (Ubuntu) - Direct Binary Install

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
kubectl version --client
-------------------------------------------------------------------------------------------

Install eksctl on Linux (Ubuntu)
Step 1: Download latest binary
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" -o eksctl.tar.gz
Step 2: Extract file
tar -xzf eksctl.tar.gz
Step 3: Move to system path
sudo mv eksctl /usr/local/bin
Step 4: Verify installation
eksctl version
--------------------------------------------------------------------------------------------

Step 1: Download AWS CLI package
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
Step 2: Install unzip (if not installed)
sudo apt install unzip -y
Step 3: Unzip the package
unzip awscliv2.zip
Step 4: Run installer
sudo ./aws/install
Step 5: Verify installation
aws --version
aws configure
-------------------------------------------------------------------------------------------

eksctl create cluster --name demo-cluster --region us-east-1 --fargate

aws eks update-kubeconfig \
  --region us-east-1 \
  --name demo-cluster



kubectl config current-context


kubectl get nodes

## Create Fargate profile

eksctl create fargateprofile \
    --cluster demo-cluster \
    --region us-east-1 \
```
    --name alb-sample-app \
    --namespace game-2048

kubectl get pods -n game-2048
kubectl get svc -n game-2048
kubectl get ingress -n game-2048
-------------------------------------------------------------------------------------------

-
