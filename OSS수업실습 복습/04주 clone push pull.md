# 04주 실습내용 복습

### 모듈 1
##### 자신의 깃허브 저장소(rpsync)생성
> 깃허브 홈페이지에서 깃허브 저장소 생성  
<br>  

### 모듈 2
##### 원격저장소 rpsync를 동일한 이름으로 복제(clone)
> ` git clone 저장소주소 `  
<br>  

### 모듈 3
##### 원격저장소 rpsync를 다른이름인 rpsync-cp로 복제(clone)
> ` git clone 저장소주소 원하는이름`  
<br>   

### 모듈 4
##### 다시 지역저장소 rpsync에서 파일 hello.py룰 코딩해서 커밋반영한 후, 원격저장소 rpsync에 반영(push)
> __코드 추가후 커밋__  
> ` cd rpsync `  
>   
> ` code hello.py `  -> 5자이상 추가  
>   
> ` git add hello.py `  
>   
> ` git commit -m 'create hello.py' `  
> <br>  
> __remote push__  
> ` git remote `  -> 저장소 확인  
>   
> ` git remote -v `  -> 주소까지 자세히 확인  
>   
> ` git push `   
<br>  

### 모듈 5
##### 다시 지역저장소 rpsync-cp에서 원격저장소 rpsync를 지역저장소에 반영 (pull)
> ` cd ../rpsync-cp `  -> rpsync-cp로 이동  
>   
> ` git remote `  
>   
> ` git remote -v `  
>   
> ` ls `  ->현재 존재하는 파일 확인 (readme.md밖에없음)  
>   
> ` git pull `  
>   
> ` ls `  ->현재 존재하는 파일 확인 (hello.py 추가됨)  
<br>   



