# EKScluster
A module that provisions an EKS cluster using terraform

- To provision an EKS cluster, make sure certain permissions like iam:GetRole, iam:GetPolicy, and iam:CreateRole are activated

- Assume roles on your account

- To create an EKS cluster, you can either use an existing VPC or create a new one, in my case, I created a new one

- Create an open ID connect provider to be able to assign role to Kubernetes cluster

- Create a provider specifying the region you want the cluster to be assigned

- Create an internet gateway access and attached the VPC to it

- To meet EKS requirement, you need to have 2 public subnet and 2 private subnets in different availability zone

- Run terraform init; terraform plan; and terraform apply

- To export Kubernetes context, Use: aws eks --region us-east-1 update-kubeconfig --name david-eks-cluster

- To check connection to EKS cluster run the following command:  kubectl get svc

- Use kubectl commands to verify your cluster configuration
