## docker 명령어 모음
----
#### docker 설치
* <code>curl -fsSL https://get.docker.com/ | sudo sh</code>
#### 권한 설정 및 설치 확인
* <code>sudo usermod -aG docker $USER</code>
* <code>sudo usermod -aG docker {사용자명}</code>
* <code>docker version</code>

#### docker 실행 명령어 구조
<code>docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]</code>

##### 옵션 목록
| 옵션 | 설명 |
|---|---|
| <code>-d</code> | 백그라운드에서 실행 및 컨테이너 ID 출력 |
| <code>-p</code> | 호스트와 컨테이너의 포트를 연결 |
| <code>-v</code> | 호스트와 컨테이너의 디렉토리를 연결 |
| <code>-e</code> | 환경 변수 설정 |
| <code>-name</code> | 컨테이너 이름 설정 |
| <code>-rm</code> | 프로세스 종료 시 컨테이너 자동 삭제 |
| <code>-it</code> | <code>-i</code> + <code>-t</code>; 터미널 입력 지원 |
| <code>-link {컨테이너명}:{별칭}</code> | 컨테이너 연결 |


#### 참고 링크
- https://subicura.com/2017/01/19/docker-guide-for-beginners-2.html
