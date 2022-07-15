## git 명령어 모음
----
#### git 설치
* <code>sudo apt install git</code>
#### 신원 정보 설정
1. <code>git config --global user.email "you@example.com"</code>
2. <code>git config --global user.name "내 이름"</code>

#### 기본 명령어
* <code>git init</code> : git 저장소 생성 (초기화)
* <code>git clone {url}</code> : 원격 저장소로부터 복제
* <code>git status {경로명}</code> : 변경 사항 체크
* <code>git remote add {등록명?/origin} {원격서버주소}</code> : 원격 저장소 추가

#### 스테이징: 커밋 할 내용 추가

* <code>git add {파일명}</code> : 특정 파일 스테이징
* <code>git add *</code> : 전체 파일 스테이징 (<code>.gitignore</code> 변경 사항 있을 시 경고)
* <code>git add .</code> : 전체 파일 스테이징 (<code>.gitignore</code> 내 파일 제외)
* <code>git reset HEAD {파일명}</code> : 특정 파일 스테이징 취소
  * <code>HEAD</code> : 해당 브랜치의 마지막 커밋

#### 커밋: git에 변경사항 반영
* <code>git commit -m "요약"</code> : 변경사항 반영
* <code>git log</code> : 기록 확인
* <code>git reset {커밋번호 첫 여섯자리} --hard</code> : 해당 커밋 및 이후 커밋 되돌리기 및 기록 삭제
* <code>git revert {커밋번호 첫 여섯자리}</code> : 해당 커밋 되돌리기 및 revert 기록 남음
* 정리 링크 : https://gmlwjd9405.github.io/2018/05/25/git-add-cancle.html

#### 변경사항 가져오기
* <code>git fetch {원격 저장소 명}</code> : 
* <code>git pull {원격 저장소 명} {브랜치 명}</code> : fetch + merge
* <code>git config pull.rebase false</code> : merge
* <code>git config pull.rebase true</code> : rebase
* <code>git config pull.ff only</code> : fast-forward only

#### git 복구 (reset, rebase)
* <code>git reflog</code> : 삭제된 커밋 id 확인
* <code>git reset --hard {커밋번호 첫 여섯자리}</code> : 커밋 복구
* <code>git reflog |grep {브랜치 명}</code> : 삭제된 브랜치 확인
* <code>git checkout -b {브랜치 명} {커밋번호 첫 여섯자리}</code> : 브랜치 복구

#### branch 관리
* checkout : branch 사용 선언
* stash : 파일의 변경 내용 일시적으로 기록
* <code>git branch {브랜치 명}</code> : {브랜치 명}으로 브랜치 생성
* <code>git checkout {브랜치 명}</code> : {브랜치 명} 브랜치를 체크아웃
* 병합 (<code>merge</code>)
  * <code>HEAD</code> 위치 변경 (<code>checkout</code>)
  * <code>git merge {브랜치 명}</code>
* <code>git branch -d {브랜치 명}</code> : {브랜치 명} 브랜치를 삭제
* <code>git rebase {new base}</code> : {new base} 로 베이스 재지정
* [Git - Rebase란?](https://velog.io/@kwonh/Git-Rebase%EB%9E%80)

----
#### 커밋 메시지 작성 방식
<pre>
Type: Subject

Body

Footer (optional)
</pre>
* Type: <code>feat</code>, <code>fix</code>, <code>docs</code>, <code>style</code>, <code>refactor</code>, <code>test</code>, <code>chore</code>
* Subject: 50자 이내, 개조식 구문
* Body: 한 줄 당 72자, 무엇을, 왜
* Footer: <code>유형: #이슈 번호</code> (<code>Fixes</code>, <code>Resolves</code>, <code>Ref</code>, <code>Related to</code>)
* 참고 자료: [Git | git 커밋컨벤션 설정하기](https://velog.io/@shin6403/Git-git-%EC%BB%A4%EB%B0%8B-%EC%BB%A8%EB%B2%A4%EC%85%98-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0)

----
#### push 시 정보 입력 (Github)
1. [Creating a personal access token 도움말](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)에 따라 토큰 생성
2. Username에 Github ID 입력
3. Password에 토큰 입력

----
#### 참고 링크
- https://github.com/jeonghwan-kim/git-usage
- https://hyeo-noo.tistory.com/184
- https://www.lainyzine.com/ko/article/git-init-how-to-initialize-git-repository/
- https://chancoding.tistory.com/76
- https://ebbnflow.tistory.com/196
- https://youngest-programming.tistory.com/220
- https://gmlwjd9405.github.io/2018/05/25/git-add-cancle.html
- https://sabarada.tistory.com/75
- https://kotlinworld.com/272
- https://suwoni-codelab.com/git/2018/04/07/Git-reflog/
- https://backlog.com/git-tutorial/kr/stepup/stepup1_1.html
- https://backlog.com/git-tutorial/kr/stepup/stepup2_1.html
