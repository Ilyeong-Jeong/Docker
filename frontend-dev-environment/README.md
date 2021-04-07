# Frontend Develop Environment Docker
**프론트 개발 환경 셋업 Docker 설정**

프론트 개발 환경을 구성한 도커 컨테이너에서 개발을 진행하기 위함.

## Docker로 개발 환경 셋업
1. 초기 실행시
Dockerfile을 build 또는 Docker image를 pull 받아 해당 image로 컨테이너 생성 및 실행.

```
docker run -it —name <컨테이너 이름> -p <호스트 포트>:<컨테이너 포트> -v <마운트시킬 경로>:<마운트되는 경로> <이미지 이름> <실행 명령어> 
```
로컬 호스트의 Workspace와 컨테이너의 Workspace를 맞추기 위해 이미지 실행시(docker run) Bind mount 방식 사용.

2. 생성된 컨테이너 접속시
```
docker start <컨테이너 이름>

docker exec -it <컨테이너 이름> <실행 명령어>
```

---

**Docker Compose로 구성**

1. 작성된 Dockerfile을 이용한 docker-compose.yml 작성.

2. 생성된 서비스 실행.
```
docker-compose up

docker-compose run <서비스 이름> <실행 명령어>
```

---

- 배포 환경 구성 추가 고려.
- 공통된 작업 환경 셋팅을 위해 더 필요한 라이브러리나 프레임워크는 설치 명령어를 Dockerfile에 추가하거나 추가된 이미지를 풀 받아 컨테이너를 실행.
