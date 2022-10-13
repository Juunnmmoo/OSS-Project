# 02주 실습내용 복습 

### 모듈실습 1
>__전체 설정 파일 위치__<br>
> ` $ pwd ` <br>
> /c/OSS/Git/02W 
> <br><br>
>
>__전체 설정 위치__<br>
> ` $ ~ `<br> 
>bash: /c/Users/samsung: Is a directory
> <br><br>
> 
> __전체 설정 파일__<br>
> ` $ cat ~/.gitconfig ` ->  이것저것 각종 정보들 나옴 
> <br><br>
> 
>  __userName 바꾸기__<br>
> ` $ git config --global user.name ` -> _ex_ $ git config --global user.name Junmo
> <br><br>
> 
> __userEmail 바꾸기__ <br>
> ` $ git config --global user.email ` -> _ex_ $ git config --global user.email Juunnmmoo@gmail,com
> <br><br>
> 
> __맥,윈도우 간의 자동변환 true/false__ <br>
> ` $ git config --global core.autocrlf ture/false ` 
> <br><br>
> 
> __뉴라인 경고발생 true/false__ <br>
> ` $ git config --global core.safecrlf true/false `
> <br><br>
> 
> __기본 브랜치 지정 (main)으로__ <br>
> ` $ git config --global init.defaultBranch main ` 
> <br><br>
> 
> __각종 추가된 정보, 수정된 정보 보기__ <br>
> ` $ $ git config --global init.defaultBranch main ` <br>
> user.name=Junmo<br>
>user.email=Juunnmmoo@gmail,com<br>
>~~
> <br><br>

### 모듈실습 2
##### 지역저장소 basic생성 후 환경 설정과 해제, 저장소 삭제
>__저장소 생성__<br>
> ` $ git init  ` ->  _ex)_ $ git init basic
> <br><br>
> 
>__지역 환경 설정__<br>
> ` $ git config user.name ~ ` ->  _ex)_ $ git config user.name Junmo <br>
> ` $ git config user.email ~ ` ->  _ex)_ $ git config user.email Juunnmmoo@gmail,com
> <br><br>
> 
>__저장소 하부폴더 .git삭제 (저장소 기능 상실)__<br>
> ` $ rm -rf .git ` 
> <br><br>
> 
>__저장소 폴더 삭제__<br>
> ` $ rm -rf ~ ` ->  _ex)_ $ rm -rf basic
> <br><br>

### 모듈실습 3
##### 지역저장소 mid생성 후, 파일 hello를 생성 후 1회 커밋, 이력정보 확인
>__저장소 생성__<br>
> ` $ git init mid ` 
> <br><br>
> 
>__생성한 저장소로 이동__<br>
> ` $ cd mid ` ->  
> <br><br>
> 
>__퍼알 수정__<br>
> ` $ echo 'A' > hello ` ->  _기존에 있던 파일이면 내용 모두 제거 후 삽입, 기존 없던 파일이면 새로운 파일 생성해 삽입_
> <br><br>
> 
> __파일 보기__<br>
> ` $ cat hello ` <br>
> A
> <br><br>
> 
>__상태보기__<br>
> ` $ git status `
> <br><br>
> 
>__스테이지(stage)에 저장(tracked file)하기__<br>
> ` $ git add hello ` 
> <br><br>
> 
>__커밋하기__<br>
> ` $ git commit -m 'create hello' `
> <br><br>
> 
>__커밋 이력 보기__<br>
> ` $ log `  
> ` $ log --oneline ` -> 한줄로 보기
> <br><br>
> 
>__HEAD 포인터가 가르키는 커밋 정보를 확인__<br>
> ` $ git show ` ->  브랜치마다 HEAD포인터 위치가 다르기 때문에 확인해 줘야함  
> <br><br>
> 
>__깃 명령 별칭 저장하기__<br>
> ` $ git config --global alias.~1 '~2'` ->  ~2 를 ~1으로 줄임<br>
> ` $ git config --global alias.log1 'log --oneline' ` -> log --oneline을 log1으로 바꿔줌<br>
> ` $ git log1 ` ==> `$ git log --oneline`
> <br><br>
> 
>__깃 명령 별칭 조회하기__<br>
> ` $ git config --global alias.log1 ` ->  log1에 저장한 별칭을 조회
> <br><br>

### 모듈실습 4
##### 원격저장소 mid에 파일 hello 2연속 커밋, add와 commit을 나누어 상태를 파악
>__파일이 add되지 않았을 때 git status__<br>
> ` 파일 상태 : modified(빨간색)  ` -> add해야하는 것을 의미
> <br><br>
>
>__파일이 commit되지 않았을 때 git status__<br>
> ` 파일 상태 : modified(초록색)  ` -> 커밋준비가 됐음을 의미
> <br><br>
> 
>__commit까지 완료했을 때 git status__<br>
> ` noting to commit, working tree clean  ` -> 모든것을 완료했음을 의미
> <br><br>


