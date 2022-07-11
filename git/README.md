## git 초기 설정
----
#### git 설치
* <code>sudo apt install git</code>
#### 신원 정보 설정
1. <code>git config --global user.email "you@example.com"</code>
2. <code>git config --global user.name "내 이름"</code>
----
#### 기본 명령어
- 초기화?
  - <code>git init</code>
- 원격 저장소로부터 복제
  - <code>git clone {url}</code>
- 변경 사항 체크
  - <code>git status {경로명}</code>
----
#### push 시 정보 입력
1. [Creating a personal access token 도움말](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)에 따라 토큰 생성
2. Username에 Github ID 입력
3. Password에 토큰 입력
