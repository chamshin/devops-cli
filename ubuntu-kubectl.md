## 우분투에 kubectl 설치하기


#### 1. 패키지 최신 버전 확인
```
$ sudo apt-get update
```
```
$ sudo apt-get upgrade
```

#### 2. kubectl 설치
```
sudo curl -o /usr/local/bin/kubectl  \
   https://amazon-eks.s3.us-west-2.amazonaws.com/1.21.2/2021-07-05/bin/linux/amd64/kubectl
```

#### 2. kubectl 실행 허용
```
sudo chmod +x /usr/local/bin/kubectl
```

#### 2. kubectl 설치 확인
```
kubectl version --client=true --short=true
```
