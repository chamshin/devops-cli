## 우분투에 docker 설치하기


#### 1. 패키지 최신 버전 확인
```
$ sudo apt-get update
```

```
$ sudo apt-get upgrade
```
#### 2. HTTPS를 통해 repository를 이용하는 것을 허용할 수 있도록 해주는 패키지 설치
```
$ sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```

#### 3. docker 공식 GPG key 추가
```
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

#### 4. docker repository 등록
```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

#### 5. docker 설치
```
$ sudo apt-get update
```
```
$ sudo apt-get install docker-ce docker-ce-cli containerd.io
```

#### 6. docker 설치 확인
```
$ sudo docker version
```

#### 7. sudo 없이 docker 명령어 사용하기
```
sudo usermod -aG docker $Ubuntu
```
+ 사용자 이름에 따라 $Ubuntu 이곳을 변경해주면 된다.
