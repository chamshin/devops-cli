## 우분투에 eksctl 설치하기

## 1. awscli2 설치

##### 1-1. zip을 풀기 위해서 unzip 설치
```
sudo apt install unzip
```

##### 1-2. awscli2 zip파일 설치
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
```

##### 1-3. 압축 풀기
```
unzip awscliv2.zip
```

##### 1-4. 설치 진행
```
sudo ./aws/install
./aws/install -i /usr/local/aws-cli -b /usr/local/bin
```

## 2. aws configure 설정
```
$ aws configure
AWS Access Key ID [None] : [발급받은 IAM의 Access Key ID]
AWS Secret Access Key [None] : [발급받은 IAM의 Secret Access Key]
Default region name [None] : ap-northeast-2[서울 리전]
Default output format [None] : 
```

- Default output format(기본 출력 포맷)은 API를 호출한 결과를 출력할 포맷을 지정합니다. text, json, table 중에 하나를 사용할 수 있다.
- AWS Access Key ID, AWS Secret Access Key가 깃에 올라가 해킹당하는 경우가 많으니 절대주의.

## 3. eksctl 설치
```
$ curl --silent --location "https://github.com/weaveworks/eksctl/releases/download/latest_release/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
```
```
$ sudo mv /tmp/eksctl /usr/local/bin
```
```
$ eksctl version
```

## 클러스터 설정 예시
```
$ eksctl create cluster \
> --name prod \
> --version 1.12 \
> --nodegroup-name example-workers \
> --node-type t2.micro \
> --nodes 1 \
> --nodes-min 1 \
> --nodes-max 5 \
> --node-ami auto
```

- EKS 클러스터 배포시 권한 문제 이슈가 많다. 
- EKS admin 권한을 주는 IAM 정책은 AmazonEKSAdminPolicy

## 클러스터 확인
```
$ kubectl get svc
```

## 클러스터 노드수 늘리기
```
$ eksctl get nodegroup --cluster=prod
$ eksctl scale nodegroup --cluster=prod --nodes=3 --name=standard-workers
$ eksctl get nodegroup --cluster=prod
```

