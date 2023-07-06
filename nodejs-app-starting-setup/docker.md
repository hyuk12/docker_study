# 도커 명령은 --help를 통해서 알 수 있다.

docker --help 를 치게 되면 docker의 여러가지 명령어를 알 수 있다.

자주 쓰게 되는 명령어들
```docker
docker ps -> 실행중인 도커 컨테이너를 나타낸다
docker ps -a -> 모든 도커 컨테이너를 나타낸다.
docker run -> 도커 컨테이너를 실행 시킨다. 디폴트 값이 attached모드
docker start -> 도커 컨테이너를 실행 시킨다. 디폴트 값이 detached모드

docker logs {{컨테이너 이름}}-> 해당 컨테이너의 로그를 모두 보여줍니다. , f를 붙이게 되면 계속 볼 수 있습니다.

```

attached모드와 detached모드 :
detached모드는 백그라운드에서 움직입니다.
attached모드는 실행하게 되면 더 이상 
명령어를 칠 수가 없습니다.

백그라운드로 실행되는 detached모드 같은경우는 
console로 만약 받는 등의 일련의 행동들이 백그라운드에서 
실행되는 구조기 때문에 나타나지 않는다.

attached모드가 기본인 run 같은경우도 따로 설정 할 수 있는데
docker run -p 8080:80 -d {{컨테이너 이름및 id}}

실행중인 컨테이너의 상태를 보고 싶다면
attach를 사용해서
docker attach {{컨테이너 이름및 아이디}}

stop으로 중지된 컨테이너를 재실행 하고싶으면
docker start -a {{컨테이너 이름}} 해주게 되면 attached모드로 실행 됩니다.