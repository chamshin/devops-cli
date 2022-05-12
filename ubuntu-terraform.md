## 우분투에 terraform 설치하기

#### 릴리스 설치
```
$ curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
```

#### 레포 추가
```
$ sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
```

#### 테라폼 설치
```
$ sudo apt-get update && sudo apt-get install terraform
```

#### 테라폼 버전확인
```
$ terraform version
```
