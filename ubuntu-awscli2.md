## 우분투에 aws cli 2 설치하기

#### 1. zip을 풀기 위해서 unzip 설치
```
$ sudo apt install unzip
```

#### 2. awscli2 zip파일 설치
```
$ curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
```

#### 3. 압축 풀기
```
$ unzip awscliv2.zip
```

#### 4. 설치 진행
```
$ sudo ./aws/install
./aws/install -i /usr/local/aws-cli -b /usr/local/bin
```

#### 현재 자격증명 확인
```
$ aws sts get-caller-identity
```
```
# 출력 값
ubuntu@ip-123-123-123-123:~$ aws sts get-caller-identity
{
    "UserId": "XXXXXXXXXXXXXX",
    "Account": "123456XXXXXXXXX",
    "Arn": "arn:aws:iam::XXXXXXXXXXXXX:user/Iam-User"
}
```
