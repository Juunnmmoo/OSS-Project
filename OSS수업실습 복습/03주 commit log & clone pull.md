# 03주 실습내용 복습 

### 모듈실습 1
> __사용자 환경설정__  
> ` $ git config --global user.name Junmo  `  -> userName 설정  
> ` $ git config --global user.email Juunnmmoo@gmail.com `  -> userEmail 설정  
><br>      
> __저장소 생성__  
> ` $ git init adv `  -> 저장소 adv 생성  
> ` $ cd adv ` -> 저장소 adv로 이동  
> <br>  
> __Python 파일 생성__  
> ` $ code hello.py `  -> vs코드열리면 수정후 (Ctrl + s)하면 저장됨  
> ` $ python hello.py ` -> 코드 확인하기  
> <br>  
> __별칭 생성후 상태 확인하기__  
> ` $ git config --global alias.st 'status' `  -> status를 st로 별칭설정  
> ` $ git st ` -> add하지 않은 파일은 untracked file로 나옴   
> <br>  
>  __python 파일 삭제__  
>  ` $ rm hello.py `  
>  ` $ ls ` -> 현재 디렉토리에 존재하는 파일이나 디렉토리를 확인하는 코드  
>  ` $ git st ` -> 저장소에 커밋할 것이 없다고 나옴  
>  <br>  

### 모듈실습 2
##### 파일을 생성해 추가한 후 stage에서 삭제, 복구 후 커밋
> __저장소 basic생성및 코드입력후 status확인__  
> ` code basic.py `  -> print(list(range(10)))추가  
> ` python basic.py `  
> ` git status `  -> 빨간색 untracktfile로 나옴  
> <br>  
> __git add후 status확인__  
> ` git add basic.py `   
> ` git status `  -> 초록색 newfile basic.py (add성공)  
> <br>  
> __파일 수정 후 status확인__  
> ` code basic.py `  -> print(list(range(1, 20, 3)))추가  
> ` python basic.py `  
> ` git status `  -> 
> <br><br>  
> ![image](https://user-images.githubusercontent.com/115628899/202840862-ee4422e3-a200-4828-8215-aedaf53d7807.png)  
> <br>  
> ` git rm --cached basic.py `  -> WD에는 남겨두고 SA부분만 삭제 (WD와 SA의 파일내용이 다르기 떄문에 오류남)  
> ` gir rm --cached -f basic.py `  -> -f붙이면 오류 해결  
> ` git status `  ->  SA의 파일이 삭제됐기 때문에 빨간색 untrackfile 나옴  
> <br>  
> __STAGE에서 취소 (STAGE -> UNTRACK FILE)__  
> ` git add basic.py `  -> SA에 올리기  
> ` git status `  -> 초록색 new file확인   
> ` git rm --cached basic.py `   -> SA삭제   
> ` git status `   -> 다시 untrack file 확인  
> <br>  
> __SA 원래대로 되돌리기__  
> ` git restore --staged basic.py    
> ` git status `  -> 초록색 new file 확인가능  
> <br>  
> 

