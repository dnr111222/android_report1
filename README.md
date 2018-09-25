# android 과제
2017261037 민사욱
=================


 ## 1. github 명령어
> + ## **설정과 초기화.**
---


1. 전역 사용자명/이메일 구성하기
 > * git config - -global user.name “Your name”                    //사용자명을 등록합니다 (필수)
>  * git config - -global user.email “Your email address”         //이메일 주소를 등록합니다. (필수)

2. 저장소별 사용자명/이메일 구성하기 (해당 저장소 디렉터리로 이동후)
>  * git config user.name “Your name”
>  * git config user.email “Your email address”

3. 전역 설정 정보 조회
> * git config - -global - -list

4. 저장소별 설정 정보 조회
>  * git config - -list

5. Git의 출력결과 색상 활성화하기
>  * git config - -global color.ui “auto”       //터미널에 표시되는 메시지에 칼라를 표시해줌

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

**tag**
+ git tag : 만들어진 태그 목록을 보여준다.
+ git tag [태그] : 태그를 만든다.
+ git tag -l ‘v1.0′ : 1.0버전의 태그들만 검색하여 보여준다.

**diff**
* git diff : 파일 변경사항들을 보여준다.
* git diff [파일] : 해당 파일의 변경사항을 보여준다.

**branch**
* git branch : 브랜치 목록을 보여준다.
* git branch [브랜치] : 브랜치를 생성한다.
* git branch -d [브랜치명] : 브렌치를 삭제한다.
//로컬의 branch 목록을 표시. 초기에는 *master 만 표기됨.
  * 은 현재 활성화 된 branch. 
  
**checkout**
* git checkout [브랜치] : 해당 브랜치로 이동한다.                                 //해당 branch 를 활성화 .
* git checkout -b [브랜치] : 브랜치가 없으면 브랜치를 생성하고 이동한다.           // branch 생성. 

**merge**
* git merge [브랜치] : 현재 브랜치에서 입력한 브랜치와 합친다.<br>
//merge 시에 충돌이 발생하면 : "fix conflicts and then commit the result" 라는 문구가 나옴. 
해당 파일을 열면 >>>>>> 이나 ====== 또는 <<<<<< 등으로 문제 부분이 나옴. 적절히 수정 후 다시 add 와 commit 을 진행 함. 

**reset**
* git reset [커밋] [파일] : stage area에 있는 파일들을 모두 특정 커밋으로 되돌린다.
* git reset --soft 커밋 : 수정사항을 유지하고 특정 커밋으로 되돌린다.
* git reset --hard 커밋 : 수정사항을 무시하고 특정 커밋으로 되돌린다.
//이전 단계로 되돌리는 방법. 로그를 확인해서 commit 된 상태의 키값을 확인 한다.

**rog**
* git rog : master 에 변경된 내용이 log 됨. 
* git rog --graph 옵션 : 시각적으로 확인. 
* git log -20 -p   :  6개월 동안의 커밋 로그 보기

**status**
* git status : 변경되고 commit 되지 않은 파일 목록을 보여 줌. 

**init**
* git init :  git 초기화 인데 git clone 을 하게 되면 자동 수행 됨

**commit**
* git commit -m "커밋메시지" : 스테이징 영역에 올라가 있는 파일들을 커밋합니다 특정파일만 커밋하려면 마지막에 파일명을 추가해주면 됩니다.

**rebase**
* git rebase [브랜치명] : 브랜치명의 변경사항을 현재 브랜치에 적용합니다.

**blame**
* git blame [파일명] : 갈 줄 앞에 커밋명과 커밋한 사람등의 정보를 볼 수 있습니다
* git blame -L [숫자],[숫자] [파일명] : 범위를 지정해서 볼 수 있다.

**fetch**
* git fetch : 원격저장소의 변경사항 가져와서 원격브랜치를 갱신합니다.

---

## 2. markdown 문법
---
<br></br>
### 1.1. 마크다운이란?

Markdown은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다.


### 1.2. 마크다운의 장-단점

#### 1.2.1. 장점
* 간결하다.
* 별도의 도구없이 작성가능하다.
* 다양한 형태로 변환이 가능하다.
* 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
* 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있다.
* 지원하는 프로그램과 플랫폼이 다양하다.


#### 1.2.2. 단점
* 표준이 없다.
* 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
* 모든 HTML 마크업을 대신하지 못한다.

<br>

## 2. markdown문법

* 문서제목
이것은 문서제목이다.
==================

* 소제목
이것은 소제목이다
---------------
