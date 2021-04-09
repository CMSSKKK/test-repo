# git CLI - 버전 관리

## 1. 버전관리의 시작

> * `pwd` 현재 위치 
> * `cd` (주소) 디렉터리 이동
> * `mkdir`(파일명) 디렉터리 생성
> * `ls -al` 
> * `git init` repository 시작

 	

## 2.  버전 생성

#### 기본 이론

> * Working tree :  버전으로 수정하는 곳, 수정한 파일들
> * Staging Area :   버전을 만드려고 하는 파일들
> * Repository : 만들어진 버전



#### 생성 및 확인

> * `nano (파일명) `: 파일 생성
> * `cat (파일명)` : 파일 내용 확인
> * `git status` : Working tree 상태 확인
> * `git add (파일명)` :  파일을 Staging Area로 보냄
> * `git commit -m [message]` Staging Area의 파일을 repository로 보내기  **버전 생성** 
> * `git log` 버전을 보여주는 기능
> * `git log --stat` 버전에 대해 변경 사항 설명
> * `git diff` 전 버전과 현재 작업한 내용의 변경 사항 확인
> * `git log -p` 각 버전의 자세한 변경사항 확인
> * `git commit` 버전 생성 // 내용 따로 추가 



* `q` 나가기_

* _`ctrl + l` 줄 청소_ 



#### 시간 여행

- `git checkout (commit ID)` 버전을 만든 시점으로 이동
- `git checkout master` 현재 시점으로 이동



#### 보충 수업

* `git add .` 현재 디렉터리 밑에 있는 모든 파일 Add  

- `git commit -am [message]` :  add 와 commit을 동시에 수행(*add가 한번도 안된 `untracked` 파일은 불가)*

- git 에디터 변경하기 

  ```bash
  git config --global core.editor "(에디터 이름)"
  ```

  

#### 버전 삭제

```bash
git reset --hard (commit ID)
```

**commit ID버전으로 리셋하겠다.(되겠다.)**  수정하는 것까지 지운다(가장 강력함)*

*`--soft` `--mixed` 등의 모드가 있지만 나중에 찾아보기* 

*협업시 공유되기 전 단계의 버전만 리셋하기*



#### 버전 되돌리기(삭제X)

- ```
  git revert (commit ID)
  ```

  commit ID 버전에서 진행된 사항을 되돌린다.

  - `R3`로 돌아가기 위해서 `R4`를 Revert!

  - 충돌을 방지하려면 역순으로 모두 Revert 해야함!

    

