# GIT 정리

* `git init`
  * 현재 폴더에서 git 명령어를 쓸 수 있게 해준다.
  * `.git` 파일이 생기고 이 파일에 지금부터 쓰는 git 명령어들과 history가 저장된다.
* `git log`
  * 현재 repository의 history를 보여준다.
  * option: `git log -p`는 변경된 history의 내용을 보여준다.
* `git diff`
  * 마지막 버전과 변경된 파일의 차이점을 보여준다.
* `git status`
  * working tree의 상태를 보여준다.
* `git add .`
  * 현재 폴더의 모든 파일을 staging area로 올려준다.
  * `.` 대신 각각의 파일을 지정해줘도 된다.
  * 예를 들면, `git add hello.txt`
* `git commit`
  * 버전을 만든다.
  * repository에 저장된다. 
    * 저장된다고 해서 원격과 동기화가 되는 것은 아니다.
    * repository에 저장된 데이터는 `push`로 원격 git과 동기화 시켜줘야 한다.
  * `git commit -m "message"` 는 우리가 커밋할 때, 쓸 메세지를 쓸 수 있게 만든다.
* `git push`
  * 원격 git과 동기화 시킨다.
  * 현재 로컬 git에서 수정한 파일들을 원격 git으로 올리는 것이다.
  * `git push origin master` 이렇게 하면 master 브랜치로 올릴 수 있다.
  * `git push -u origin master` 
    * 이렇게 하면 다음부터 `git push`만 써도 `git push origin master`가 실행된다.
* `git reset --hard`
  * 마지막 버전으로 working tree를 돌린다.
  * add나 commit을 하지 않았을 때, 사용 가능
  * 했을 때도 사용가능한지 모르겠음 -- 다음에 알아볼 예정
* `git log -p`
  * 이 명령어를 통해 각 커밋의 해시 값을 알 수 있다.
  * 그 해시 값을 통해 각 커밋 버전으로 돌아갈 수 있다.



* untracked files
  * git에서 관리하지 않고 있는 파일
* tracked files
  * git에서 관리하고 있는 파일