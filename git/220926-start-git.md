# git process

git에는 크게 세 가지의 작업 영역이 있습니다.

1. working directory
2. staging area
3. local repo

![](https://res.cloudinary.com/practicaldev/image/fetch/s--M_fHUEqA--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/128hsgntnsu9bww0y8sz.png)

### 1. working directory
이 공간에서 파일을 생성하고 수정합니다.
이 공간에서의 파일은 크게 두 가지로 나뉩니다.
- Untracked : 워킹 디렉토리에 추가되었지만 git에서 관리하지 않은 상태입니다.
- Tracked : git이 이미 알고있는 파일을 가리킵니다. 이 안의 파일들은 세가지 상태중 하나입니다.
	- Unmodified : 마지막  저장이후 수정 없이 저장된 상태를 의미합니다.
	- Modified : 수정한 파일을 아직 로컬 저장소에 Commit하지 않은 것을 의미합니다.
	- Staged : 현재 수정한 파일을 곧 Commit할 것이라고 표시한 상태를 의미합니다. 

 수정이 완료된 파일은 git add 명령어를 통해서 staging area로 옮겨갈 수 있습니다.

### 2. staging area
git에 있는 파일의 상태를 확인하고 싶을 땐 git status 명령어를 사용하면 됩니다.

git commit 명령어로 스냅샷을 남길 수 있습니다.

> 스냅샷이란 특정 시점에 어떤 파일에 어떤 내용이 기록되어 있었는지, 폴더 구조와 어떤 파일이 존재했는지 확인 할 수 있는 정보입니다.

### 3. local repo
git이 프로젝트의 메타 데이터와 객체 오브젝트를 저장하는 곳을 말합니다.
staging area에 있던 파일들이  git commit 명령어를 통해 이 공간에 저장 됩니다.

## 원격 저장소로 이동시키기
local repo 에 저장된 프로젝트를 'git push 저장소명 브랜치명'명령어로 이동시킬 수 있습니다.
