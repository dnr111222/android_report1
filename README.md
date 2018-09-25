# android 과제
2017261037 민사욱
=================


1. ## github 명령어
> + ## **설정과 초기화.**
---


1. 전역 사용자명/이메일 구성하기
 * git config - -global user.name “Your name”                    //사용자명을 등록합니다 (필수)
 * git config - -global user.email “Your email address”         //이메일 주소를 등록합니다. (필수)

2. 저장소별 사용자명/이메일 구성하기 (해당 저장소 디렉터리로 이동후)
 * git config user.name “Your name”
 * git config user.email “Your email address”

3. 전역 설정 정보 조회
 * git config - -global - -list

4. 저장소별 설정 정보 조회
 * git config - -list

5. Git의 출력결과 색상 활성화하기
 * git config - -global color.ui “auto”       //터미널에 표시되는 메시지에 칼라를 표시해줌

<br></br>
> + ## **사용 문법**

**version**
* git --version  : 현재 git의 버전을 확인합니다.

**add**
* git add [파일] : stage area에 파일을 추가하여 commit 할 수 있도록 한다.
 //작업내용을 반영하는 작업
 
**commit**
* git commit -m”mention” : stage area에 있는 파일들을 commit 한다.
* git commit -a -m”mention” : 이미 추가된 파일이 수정 중인 상황에서 stage area에 올리지 않아도 stage area에 올리고 바로 commit 한다.
//변경 내용 or 신규 추가 파일이 master 에 추가 됨.

**remote**
* git remote add [저장소] [저장소주소] : 원격 저장소를 추가한다.
* git remote -v : 원격 저장소 목록을 보여준다.
* git remote rm 이름 : 원격저장소를 제거합니다.

**clone**
* git clone [주소] [저장될 폴더] : git 원격 저장소에 있는 프로젝트를 내려받는다.
* git clone –depth [숫자] [주소] : 프로젝트가 많은 커밋들을 가지고 있을 경우 내려받는데 오래 걸리므로 depth 옵션을 사용하면 해당 숫자만큼의 최신 커밋들만 가지고 프로젝트를 내려받는다.
//origin 에 있는 repository 를 로컬로 가져오는 명령어.  이렇게 해서 가져온 git 이 master 임. 

**push**
* git push origin master : origin 원격 저장소에 master 브랜치에 추가된 스냅샷들을 올린다.
* git push origin +master : origin 원격 저장소에 master 브랜치에 추가된 스냅샷들을 강제로 올린다.
//master 의 수정 사항이 GitHub 의 origin repository 에 등록.

**stash**
* git stash : 변경된 내역들을 스택에 만들고 워킹디렉토리는 깨끗하게 비운다.
* git stash list : 스택에 저장된 내역들을 확인할 수 있다.
* git stash apply : 스택에 저장된 최신의 stash를 적용한다.
* git stash apply stash이름(ex.stash@{0}) : 스택에 저장된 stash중 이름이 같은 stash를 적용한다.
* git stash apply –index : Stage 상태로 스택에 저장된 stash를 Stage 상태까지 복원한다.

