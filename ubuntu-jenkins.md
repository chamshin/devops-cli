## 우분투에 Jenkins 설치하기


#### 1. 패키지 최신 버전 확인
```
$ sudo apt-get update
```
```
$ sudo apt-get upgrade
```
#### 2. Jenkins 설치를 위해 Repository Key 추가
```
$ wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
```

#### 3. 서버의 sources.list에 Jenkins 패키지 저장소를 추가
```
$ sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
    /etc/apt/sources.list.d/jenkins.list'
```
#### 4. Java openjdk11 설치
```
$ sudo apt-get install openjdk-11-jdk
```
#### 5. 패키지 최신 버전 확인
```
$ sudo apt-get update
```

#### 6. Jenkins 패키지 설치
```
$ sudo apt-get install jenkins
```

#### 7. Jenkins 실행하기
```
$ sudo systemctl start jenkins
```

#### 8. Jenkins 상태체크
```
$ sudo systemctl status jenkins
```

#### 젠킨스 초기 비밀번호 설정
```
$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
