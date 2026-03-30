Install kubectl on Linux (Ubuntu) - Direct Binary Install

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
