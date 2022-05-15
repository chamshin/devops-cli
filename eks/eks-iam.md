init


$ aws sts get-caller-identity

$ aws eks update-kubeconfig --name eks-cluster-name --region aws-region

$ aws eks update-kubeconfig --name eks-cluster-name --region aws-region --role-arn arn:aws:iam::XXXXXXXXXXXX:role/testrole

$ kubectl get pods --kubeconfig ./.kube/config

$ kubectl get svc
