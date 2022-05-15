init


$ aws sts get-caller-identity

$ aws eks update-kubeconfig --name eks-cluster-name --region aws-region

$ kubectl get pods --kubeconfig ./.kube/config

$ aws eks update-kubeconfig --name eks-demo --region ap-northeast-2 --role-arn arn:aws:iam::12121212121212:role/aws-service-role/eks.amazonaws.com/AWSServiceRoleForAmazonEKS

$ kubectl config view --minify

$ kubectl get svc
