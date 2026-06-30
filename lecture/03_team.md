# 3. 팀 단위 작업하기
- 핵심개념: Git Flow와 GitHub Flow 전략
- 명령어: git fetch, git pull
- 포인트: PR(Pull Request) 및 코드 리뷰

## local과 remote
- local repository: 내 컴퓨터 안의 작업 공간
- remote repository: 인터넷 서버에 있는 작업 공간

## remote와 push 명령어
1) 목적지 주소 지정 및 확인하기
```cli
git remote add <별칭> <remote_repository_url>
git remote add origin https://github.com/아이디/저장소.git
git remote -v
```
2) 코드 밀어 올리기
```cli
git push <별칭> <브랜치명>
git push origin main
```
3) 저장소 가져오기
```cli
git clone <remote_repository_url>
```

## 변경된 코드 받아오기
1) 강제 다운로드후 강제 병합
```cli
git pull origin main
```
2) 다운로드만 하기
- 확인후 `git merge`로 병합
```cli
git fetch <별칭>
git fetch origin
```


