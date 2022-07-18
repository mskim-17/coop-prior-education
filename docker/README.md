## docker 명령어 모음
#### docker 설치
* <code>curl -fsSL https://get.docker.com/ | sudo sh</code>
#### 권한 설정 및 설치 확인
* <code>sudo usermod -aG docker $USER</code>
* <code>sudo usermod -aG docker {사용자명}</code>
* <code>docker version</code>

#### docker 실행 명령어 구조
* <code>docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]</code> : 컨테이너 생성 및 실행
  * <code>-d</code> : 백그라운드에서 실행 및 컨테이너 ID 출력
  * <code>-p</code> : 호스트와 컨테이너의 포트를 연결
  * <code>-v</code> : 호스트와 컨테이너의 디렉토리를 연결
  * <code>-e</code> : 환경 변수 설정
  * <code>-name</code> : 컨테이너 이름 설정
  * <code>-rm</code> : 프로세스 종료 시 컨테이너 자동 삭제
  * <code>-it</code> : <code>-i</code> + <code>-t</code>; 터미널 입력 지원
  * <code>-link {컨테이너명}:{별칭}</code> : 컨테이너 연결


#### 컨테이너 관리
* <code>docker ps [OPTIONS]</code> : 컨테이너 목록 확인하기 (기본값: 실행 중)
* <code>docker ps -all</code> : 모든 컨테이너 목록 확인하기
* <code>docker stop [OPTIONS] CONTAINER [CONTAINER...]</code> : 실행 중인 컨테이너 중지
* <code>docker rm [OPTIONS] CONTAINER [CONTAINER...]</code> : 컨테이너 삭제
* <code>docker logs [OPTIONS] CONTAINER</code> : 로그 확인
  * <code>--tail {숫자}</code>: 가장 최근 {숫자} 개의 로그 출력
  * <code>-f</code>: 로그 실시간 갱신
* <code>docker exec [OPTIONS] CONTAINER COMMAND [ARG...]</code> : 실행 중인 컨테이너에 명령


#### 이미지 관리
* <code>docker images [OPTIONS] [REPOSITORY[:TAG]]</code> : 이미지 목록 확인하기
* <code>docker pull [OPTIONS] NAME[:TAG|@DIGEST]</code> : 이미지 다운로드하기
* <code>docker rmi [OPTIONS] IMAGE [IMAGE...]</code> : 이미지 삭제하기 (실행 중일 경우 삭제 불가)


## Docker Compose
#### docker-compose 설치
<pre>
curl -L "https://github.com/docker/compose/releases/download/1.9.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
# test
docker-compose version
</pre>

----
#### 참고 링크
- https://subicura.com/2017/01/19/docker-guide-for-beginners-2.html
- https://subicura.com/2017/02/10/docker-guide-for-beginners-create-image-and-deploy.html

