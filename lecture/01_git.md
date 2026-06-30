# 1. Git 생존 필수기

- 핵심개념: 버전관리의 필요성, Working Directory, Staging Area, Repository
- 명령어: git init, git clone, git add, git commit
- 포인트: .gitignore의 필요성, commit message 작성법


## 버전관리의 필요성
- 개발할 때 파일이 수백개가 되고 코드를 수정하다보면 잘못된 부분을 찾기 어렵다.
- 이런 상황에 변경사항을 기록해두고 잘못된 부분을 찾기 위해 버전관리 도구가 필요히다.

## Git과 GitHub
- Git: Local에서 코드의 변경점(버전)을 기록하고 관리하는 프로그램. 오프라인 상태에서도 작동
- GitHub: Git으로 기록한 코드를 온라인에 올려 다른 사람과 공유하고 협업할 수 있는 웹 서비스

## CLI와 GUI
- CLI(Command Line Interface): 터미널에 직접 명령어를 입력하는 방식
- GUI(Graphical User Interface): 마우스 클릭으로 조작하는 시각적인 방식

## GitHub 초기 설정
1) GitHub 계정 생성
2) 이름과 이메일 설정
- GitHub에 가입시 사용한 이메일 주소와 동일
```cli
git config --global user.name "여러분의 영문 이름"
git config --global user.email "여러분의 이메일 주소"
```
3) 설정 확인
```cli
git config --list
```
4) 기본 브랜치 변경하기
```cli
git config --global init.defaultBranch main
```

## Git의 3가지 공간
- Working Directory: 실제 작업하는 폴더. Git에 올리지 않은 상태
- Staging Area: 수정한 파일 중 기록할 파일들만 골라서 담아두는 임시 공간
- Repository: 버전으로 기록한 상태

## 주요 명령어
1) 상태 확인하기
- staging area에 담겨 있는 파일 확인
```cli
git status
```
2) staging area에 파일 담기
- \[파일명\]에 .을 사용할 경우 전체 파알을 의미
```cli
git add [파일명]
```
3) 설명 기록하기
- commmit message: 무엇을 업로드했는지 기록
```cli
git commit -m "기록할 내용"
```
4) 기록 확인하기
```cli
git log
```

## commit message 양식
```
# <type>: <subject>
- 제목행은 50자로 제한
- 제목행의 첫글자는 대문자로 시작
- 제목행은 명령문 사용
# body message
- 본문은 72자마다 끊어서 줄바꿈
- 본문은 변경 내용과 이유 설명
# issue: number/url
```
(type)
- feat: 새로운 기능 추가
- fix: 버그 수정
- docs: 문서 수정
- style: 코드 포맷팅, 세미콜론 누락 수정(코드 로직 변경 없음)
- test: 테스트 코드, 리팩토링 테스트 코드 추가
- refactor: 코드 리팩토링
- chore: 빌드 업무 수정, 패키지 매니저 수정
- remove: 파일만 삭제

(issue)
- 해결: Closes(종료), Fixes(수정), Resolves(해결)
- 참고: Ref(참고), Related to(관련), See also(참고)
