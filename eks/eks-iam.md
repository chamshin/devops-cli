init


$ aws sts get-caller-identity

$ aws eks update-kubeconfig --name eks-cluster-name --region aws-region

$ aws eks update-kubeconfig --name eks-cluster-name --region aws-region --role-arn arn:aws:iam::XXXXXXXXXXXX:role/testrole

$ kubectl get pods --kubeconfig ./.kube/config

$ kubectl get svc

$ aws eks update-kubeconfig --name eks-demo --region ap-northeast-2 --role-arn arn:aws:iam::12121212121212:role/aws-service-role/eks.amazonaws.com/AWSServiceRoleForAmazonEKS
