## 우분투에 helm 설치하기

#### 1. 최신 helm 릴리스 설치
```
$ curl https://baltocdn.com/helm/signing.asc | sudo apt-key add -
```
```
$ sudo apt-get install apt-transport-https --yes
```

#### 2. 안정적인 릴리스를 위해 레포지토리 추가
```
$ echo "deb https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
```

#### 3. 패키지 최신 버전 확인
```
$ sudo apt-get update
```

#### 4. helm 설치
```
$ sudo apt-get install helm
```

#### 4. helm 설치 확인
```
$ helm version
```
