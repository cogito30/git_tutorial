# 1. 협업의 기본, 브랜치와 병합

- 핵심개념: 왜 main(master) 브랜치에서 직접 작업하면 안되는지
- 명령어: git branch, git switch, git merge
- 포인트: conflict 해결하기

## Branch가 필요한 이유
- 기존의 서비스를 건드리지 않고 새로운 기능을 추가하기 위해

## Branch란?
- 독립적인 공간을 만드는 기능

## HEAD란?
- 현재 머물고 있는 Branch를 가리키는 화살표

## Branch 관련 명령어
1) 브랜치 확인 및 만들기
- `*` 표시가 있는 branch가 HEAD
```cli
git branch
git branch <브랜치명>
```
2) branch 변경하기
- `-c` 옵션을 추가할 경우 브랜치 생성과 변경을 동시에 진행
```cli
git switch <브랜치명>
git switch -c <브랜치명>
```
3) branch 제거하기
- branch 제거시 해당 branch 밖으로 나와야 함
```cli
git branch -d <브랜치명>
```

## Branch 명명법
- `/`를 사용해 폴더처럼 구조화
- `feature/이름`: 새로운 기능 개발
- `bugfix/이름`: 일반적인 버그 수정
- `hotfix/이름`: 긴급 버그 수정
- `release/이름`: 다음 버전을 배포하기 위한 준비

## Branch 합치기
- 코드를 가져올 목적지 브랜치로 이동 후 병합
- 해당 브랜치에서 가져올 브랜치를 `git merge`로 병합
```cli
git merge <브랜치명>
```

## Merge Conflict 해결하기
- 동시 작업시 같은 줄을 수정했을 경우 충돌 발생
- `<<<< HEAD`와 `=====` 사이: 현재 있는 branch의 코드
- `=====`와 `>>>> 브랜치명` 사이: 합치려고 가져온 branch의 코드
- 수정후 `git add`와 `git commit` 진행

