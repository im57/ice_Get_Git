- 깃 초기 설정

  - 사용자 정보 설정

    - git config --global user.name "im57"
    - git config --global user.email eovhehd1986@gmail.com

  - 설정 정보 확인

    - git config --list

      

- 깃 저장소 생성

  - 깃 리포지토리 생성
    - git init



- 깃 파일 생성
  - working directory -> staging area
    - git add (파일 .. 전체 - . )
  - staging area -> Git repository
    - git commit -m "메세지"
    - 저장소 반영 내용 변경  - 텍스트 편집기 실행
      - git commit --amend



- 깃 관리 상태 확인

  - staging area 파일 상태 확인
    - git status

  - git repository에 존재하는 history 확인 (저장소 반영 내역 확인)
    - git log
  - add 명령 취소
    - git reset 파일이름
  - commit 된 파일 중 변경 사항 비교
    - git diff

  - untracked - add로 staging 되지 않은 파일들
  - modified - commit 된 파일 중 수정된 파일들



- 브랜치
  - 브랜치 생성
    - git branch 브랜치이름
  - 현재 브랜치 확인
    - git branch
  - 브랜치 전환
    - git checkout 브랜치이름
  - 브랜치 삭제
    - git branch -d  브랜치이름



- 원격 저장소
  - 원격 저장소 받아오기
    - git clone 원격저장소주소
  - 원격 저장소 연결
    - git remote add 원격저장소이름 원격저장소주소
  - 연결된 원격 저장소 확인
    - git remote -v
  - 원격 저장소 이름 변경
    - git remote rename 원래이름 바꿀이름
  - 원격 저장소 삭제
    - git remote rm 원격저장소이름
  - 원격 저장소에서 데이터 가져오기 + 병합l
    - git pull origin master
  - 원격 저장소에서 데이터 가져오기 
    - git fetch
    - git merge origin/master   (병합 필요)
  - 작업 내용 원격 저장소에 반영
    - git push origin master
  - 브랜치 추적
    - --set-upstream



- rebase

  - 그래프를 선형으로 만듦

  - 공통된 부모까지의 commit을 가져와 원하는 브랜치 옆에 이어붙임

    c1-c2-c6-c7Master		->		c1-c2-c6-c7Master-c3'-c4'-c5'Cat

    ​          \c3-c4-c5Cat

  - git rebase master

  - rebase conflict

    - git status로 파일 상태 확인
    - 파일에서 충돌 해결 후 git add로 파일을 staging
    - git rebase --continue로 rebase 마무리



- Head pointer
  - Index
    - git add로 staging 되어있는 데이터들
  - Head
    - 마지막 커밋을 가리키는 snapshot
  - snapshot
    - staging 되어진 데이터들을(index) commit 명령으로 영구히 저장한 것
  - 예전 버전으로 돌아가 commit 수정
    - git reset --soft HEAD~
  - working directory에 존재하는 파일도 사라짐
    - git reset --hard HEAD~









//app/src/main에서 git init 했음

//DID_Student_Card에도 git init 했음 (ls하면 front랑 DID_STudent나옴)