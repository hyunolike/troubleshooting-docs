## 문제
- 젠킨스 일반 유저계정으로 실행 시 아래와 같이 권한 이슈 발생


```
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post http://%2Fvar%2Frun%2Fdocker.sock/v1.38/build?buildargs=%7B%7D&cachefrom=%5B%5D&cgroupparent=&cpuperiod=0&cpuquota=0&cpusetcpus=&cpusetmems=&cpushares=0&dockerfile=Dockerfile&labels=%7B%7D&memory=0&memswap=0&networkmode=default&rm=1&session=klv1s7gcvua6o8j7srtt572zk&target=&ulimits=null&version=1: dial unix /var/run/docker.sock: connect: permission denied
```

## 해결
> [참고자료](https://lifeplan-b.tistory.com/172)
[조치방안]

2가지 해결방법이 있다.

 

방법1. Docker.sock 권한 변경

Chmod 666 /var/run/docker.sock

 

특이사항 : 권한을 변경한 경우, 일시적인 조치 입니다.

docker 서비스를 재시작하면 권한이 660으로 돌아옵니다.

해당 방법은 권장하지 않습니다.

 

방법2. Docker 그룹을 만들어서. 사용자 추가하기

$ Sudo groupadd docker

$ sudo usermod -aG docker $USER

$ newgrp

 
