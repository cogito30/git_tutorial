# 실무 중심 Git 튜토리얼 블로그 연재 로드맵 🚀

**기획 의도**: "Git 명령어는 아는데, 실무에서 어떻게 쓰는지 모르겠어요"라고 말하는 주니어 개발자 및 취업 준비생을 위한 실전형 튜토리얼

## 🟢 Part 1. Git과 친해지기 (Local 기초)

가장 기본적인 내 PC에서의 버전 관리 흐름을 익히는 단계입니다.

$$1편$$

Git, 넌 누구냐? (그리고 초기 세팅)

- 주제: Git의 필요성과 기본 개념, 그리고 초기 설정
- 핵심 내용:
  - Git과 GitHub의 차이점
  - CLI(터미널) vs GUI(소스트리, GitKraken) 무엇을 써야 할까? (실무에서는 둘 다 씁니다)
  - 초기 환경 설정: `git config` (이름, 이메일, 기본 에디터 설정)

$$2편$$

실무자의 하루 1: 변경사항 저장하기

- 주제: 파일을 수정하고 기록을 남기는 기본 사이클
- 핵심 내용:
  - Working Directory, Staging Area, Repository의 개념 (이해하기 쉽게 비유)
  - `git add`, `git commit`, `git status`, `git log`
  - ⭐ 실무 팁: 좋은 커밋 메시지 작성법 (커밋 컨벤션 소개: feat, fix, docs 등)

## 🟡 Part 2. 평행우주 만들기 (브랜치와 병합)

여러 작업이 동시에 진행되는 실무 환경을 이해하는 단계입니다.

$$3편$$

브랜치(Branch): 내 작업 공간 분리하기
- 주제: 안전하게 새로운 기능을 개발하기 위한 브랜치 기초
- 핵심 내용:
  - 브랜치란 무엇인가? (HEAD의 개념)
  - `git branch`, `git switch` (구 `checkout`), `git branch -d`
  - ⭐ 실무 팁: 실무에서 브랜치 이름 짓는 룰 (예: `feature/login`, `hotfix/typo`)

$$4편$$

두 세계의 만남: Merge와 충돌(Conflict) 해결
- 주제: 작업한 내용을 하나로 합치고, 충돌에 대처하는 법
- 핵심 내용:
  - `git merge` 기초 (Fast-forward vs 3-way merge)
  - ⭐ 실무 팁: 가장 두려워하는 'Merge Conflict(충돌)' 발생 이유와 해결 방법 (VS Code 등 에디터를 활용한 충돌 해결)

## 🟠 Part 3. 진짜 협업의 시작 (원격 저장소와 GitHub)

팀원들과 코드를 공유하고 리뷰하는 방법을 배웁니다.

$$5편$$

내 코드를 세상으로: Remote Repository
- 주제: GitHub을 활용한 코드 백업 및 공유
- 핵심 내용:
  - `git remote`, `git push`, `git clone`
  - `git pull` 과 `git fetch`의 차이점 완벽 이해하기

$$6편$$

$$핵심$$

실무 협업의 꽃, Pull Request (PR)
- 주제: 팀 개발의 표준, PR과 코드 리뷰 문화
- 핵심 내용:
  - 협업 워크플로우: Issue 생성 -> Branch 작업 -> Push -> PR -> Review -> Merge
  - 좋은 PR 설명(Description) 작성하는 법
  - Fork를 활용한 오픈소스 기여 방식 (간략히)

## 🔴 Part 4. 실무 레벨업 (고급 기능)

이 기능들을 쓸 줄 알면 "Git 좀 다루네?" 라는 소리를 듣습니다.

$$7편$$

"앗, 지금 다른 브랜치로 가야해!": Stash

- 주제: 작업 중이던 코드를 임시로 저장해두는 방법
- 핵심 내용:
  - `git stash`, `git stash pop`, `git stash list`
  - ⭐ 실무 팁: 급하게 핫픽스(Hotfix)를 처리해야 할 때 Stash 활용법

$$8편$$

코드 히스토리를 아름답게: Rebase
- 주제: Merge와는 다른 브랜치 병합 방식, Rebase
- 핵심 내용:
  - `git rebase`의 개념과 Merge와의 차이점
  - ⭐ 실무 팁: Interactive Rebase (`git rebase -i`)를 활용해 지저분한 커밋 하나로 묶기(Squash), 커밋 메시지 수정하기
  - 🚨 주의: 이미 Push된 커밋은 Rebase 하지 말아야 하는 이유

$$9편$$

저 커밋만 쏙 빼올래: Cherry-pick
- 주제: 다른 브랜치의 특정 커밋만 가져오는 방법
- 핵심 내용:
  - `git cherry-pick` 사용법
  - ⭐ 실무 팁: 릴리즈 브랜치에 누락된 버그 픽스 커밋만 긴급하게 가져올 때

## 🟣 Part 5. 멘붕 탈출 (위기 극복 가이드)

실무에서 무조건 겪게 되는 실수들을 안전하게 복구하는 방법입니다.

$$10편$$

 "방금 커밋 잘못했어요!": 취소의 미학

주제: 상황별 커밋 되돌리기

핵심 내용:

방금 한 커밋 메시지 수정: git commit --amend

아예 과거로 돌아가기: git reset (soft, mixed, hard 차이점)

이미 Push 해버렸을 때 안전하게 되돌리기: git revert

$$11편$$

$$비기$$

 지워진 커밋도 살려내는 마법: Reflog

주제: Git 최후의 보루

핵심 내용:

git reflog를 이용해 실수로 삭제한 브랜치나 reset --hard로 날아간 코드 복구하기

🟤 Part 6. 실무 적용 및 자동화 (에필로그)

단순한 명령어 툴을 넘어 팀 문화를 만드는 과정입니다.

$$12편$$

 우리 팀은 어떻게 일할까? (Git Branching Strategies)

주제: 실무에서 사용하는 대표적인 브랜치 전략들

핵심 내용:

Git Flow (전통적이고 무거운 방식)

GitHub Flow (가볍고 빠른 CI/CD에 적합한 방식)

Trunk-based Development (최신 트렌드)

$$13편$$

 휴먼 에러를 막아라: Git Hooks (Husky)

주제: 커밋이나 푸시 전에 자동으로 검사 실행하기

핵심 내용:

Git Hooks의 개념

프론트엔드/백엔드 실무 팁: Husky를 설정하여 Linter(ESLint 등), Code formatter(Prettier), 테스트 코드를 통과해야만 커밋되게 만들기
