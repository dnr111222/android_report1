# android 과제
2017261037 민사욱
=================


## github 명령어
> ### **설정과 초기화.**
---


1. 전역 사용자명/이메일 구성하기

> * git config - -global user.name “Your name”                    //사용자명을 등록합니다 (필수)

> * git config - -global user.email “Your email address”         //이메일 주소를 등록합니다. (필수)

2. 저장소별 사용자명/이메일 구성하기 (해당 저장소 디렉터리로 이동후)

> * git config user.name “Your name”

> * git config user.email “Your email address”

3. 전역 설정 정보 조회

> * git config - -global - -list

4. 저장소별 설정 정보 조회

> * git config - -list

5. Git의 출력결과 색상 활성화하기

> * git config - -global color.ui “auto”       //터미널에 표시되는 메시지에 칼라를 표시해줌


> **### 사용 문법**

version
* git --version  : 현재 git의 버전을 확인합니다.

add
* git add [파일] : stage area에 파일을 추가하여 commit 할 수 있도록 한다.
 //작업내용을 반영하는 작업
