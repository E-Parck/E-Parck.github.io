# [고량주] 1주차 Git

**GIT WORKFLOW**
=

**LOCAL REPOSITORY**
-

> **WORKING DIRECTOROY**: 파일을 작업하는 공간
* **untracked**: Git이 traking하지 못하는 파일
* **tracked**: Git이 traking 하고 있는 파일 (*unmodified* or *modified*)

> **STAGING AREA**: 버전 히스토리에 저장할 준비가 되어있는 파일을 옮겨놓는 공간
* **git add**: working directory -> staging area

> **.GIT DIRECTORY**: 버전 히스토리를 가지고 있는 공간
* **git commit**: staging area -> .git directory
* **git checkout**: .git directory -> working directory

**REMOTE REPOSITORY**
-

> **.GIT DIRECTORY**
* **git push**: (local).git directory -> (remote).git directory
* **git pull**: (remote).git directory -> (local).git directory

---

|용어|Description|
|--|--|
|**repository** / **repo** (저장소)|Git으로 버전 관리하는 디렉토리|
|**local repository** (로컬 저장소)|작업자의 개발 환경(PC)에 설정된 Git 저장소|
|**remote repository** (원격 저장소)|GitHub 등 외부 서버에 설정된 Git 저장소|
|**commit** (커밋)|특정 상태를 기록한 것 = 버전|
|**branch** (브랜치)|또 다른 작업공간|
|**merge** (머지)|병합/합치기, 특정 브랜치에서 작업한 내용을 또 다른 브랜치에 적용하는 것|

|terminal commands|Description|
|--|--|
|**mkdir**|디렉토리 생성|
|**cd**|디렉토리로 이동|
|**touch**|빈 파일 생성|
|**echo "[글자]" >> [파일]**|파일에 글자 추가|
|**echo [글자] > [파일].txt**|파일 생성 + 글자 추가|
|**cd ..**|상위 디렉토리로 이동|

|Git commands|Description|
|--|--|
|**git init**|저장소 만들기|
|**git status**|현재 상태 확인|
|**git add**|현재 상태 추적|
|**git commit**|현재 상태 저장|
|**git log**|이력 확인|
|**git reset**|이력 제거|
|**git revert**|이력 유지|
|**git branch -M main**|기본 브랜치 master -> main|
|**git branch -m master**|기본 브랜치 main -> master|

*참고 [Git command refernece](https://git-scm.com/docs)

---

**BRANCH**
=

|Git commands|Description|
|--|--|
|**git switch -c [new branch]**|브랜치를 생성하면서 이동|
|= **git branch [new branch]** & **git switch [new branch]**|브랜치 생성 & 브랜치 변경|
|**git merge**|브랜치 합치기|


**conflict 해결**
-
* 머지 작업 취소: **git merge --abort**
* 충돌 해결

1. **충돌이 발생한 파일 열기**

<img src="https://ifh.cc/g/HozZgR.png" width="170" height="120"></img>

2. **맞는 내용만 남기고 전부 삭제**
3. **commit** (git add & git commit)

---

**GitHub**
=
Git 기본 저장소: origin

|Git commands|Description|
|--|--|
|**git push**|local -> remote|
|**git clone [address] [directory** or (**blank**)**]**|(복제) remote -> local|
|**git pull**|(추가) remote -> local|

*원격 저장소와 로컬 저장소의 차이가 커지면 나중에 충돌이 많이 발생하기 때문에 Git Pull은 자주 수행하는 것이 좋다.

---

**우당당탕**
=

[Windows에서 명령어 code 등록하기](https://www.lainyzine.com/ko/article/how-to-execute-visual-studio-code-from-terminal/#%EC%9C%88%EB%8F%84%EC%9A%B0%EC%97%90%EC%84%9C-visual-studio-code%EC%9D%98-path%EB%A5%BC-%EC%84%A4%EC%A0%95%ED%95%98%EB%8A%94-%EB%B0%A9%EB%B2%95)

--

|*단축키*|저장소 진입|터미널 초기화|
|--|--|--|
|Windows|**start .git**|**ctrl + K**|
|mac|**open .git**|**command + K**|

--

1. git log 명령어 실행

2. 다음 로그 메세지 or (end) 메세지

3. Q키를 눌러 로그 화면 나가기

--

1. 오류 발생: *'npm' is not recognized as an internal or external command, operable program or batch file.*

2.  node.js 설치

3. Git bash에서 node -v와 npm -v 명령어 실행

4. 오류 발생: *bash: node: command not found*

5. node.js 삭제 후 재설치

6. Git bash에서 node -v와 npm -v 명령어 실행, 각각 버전 확인이 되는지 확인