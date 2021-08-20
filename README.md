# Course_EKS-Basics

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

unzip awscliv2.zip

which aws

sudo ./aws/install --bin-dir /usr/bin --install-dir /usr/bin/aws-cli --update

aws --version

aws configure


https://dl.k8s.io/release/v1.22.0/bin/windows/amd64/kubectl.exe


curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.16.8/2020-04-16/bin/linux/amd64/kubectl


chmod +x ./kubectl

mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:$HOME/bin


kubectl version --short --client

curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp

sudo mv /tmp/eksctl /usr/bin

eksctl version

eksctl create cluster --name dev --version 1.16 --region us-east-1 --nodegroup-name standard-workers --node-type t3.micro --nodes 3 --nodes-min 1 --nodes-max 4 --managed

eksctl get cluster

aws eks update-kubeconfig --name dev --region us-east-1

sudo yum install -y git

git clone https://github.com/shk2123/Course_EKS-Basics.git -b develop

