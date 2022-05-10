## 1. 최신 OSS 릴리스 설치
```
$ sudo apt-get install -y apt-transport-https
```
```
$ sudo apt-get install -y software-properties-common wget
```
```
$ wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
```

## 2. 안정적인 릴리스를 위해 레포지토리 추가
```
$ echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
```

## 3. 저장소 추가후 그라파나 설치
```
$ sudo apt-get update
```
```
$ sudo apt-get install grafana
```

#### systemd로 서버 시작, 확인
```
sudo systemctl daemon-reload
```
```
sudo systemctl start grafana-server
```
```
sudo systemctl status grafana-server
```

#### 부팅시 grafana 서버 시작 구성
```
sudo systemctl enable grafana-server.service
```

#### [Grafana Labs 에서 사용자 환경에 따라 설치하는 방법 참고](https://grafana.com/docs/grafana/latest/installation/)
