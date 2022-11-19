# 06주 수업 실습


![image](https://user-images.githubusercontent.com/115628899/202843590-2ff06ebd-a3f8-461d-8254-0de218ecffd0.png)
<br>  
### 모듈 1
##### 저장소 bpr생성, 브랜치 main에서 1개의 커밋 
> __저장소 생성 후 커밋__  
> ` git init brp `  
><br>
> ` code login.py `  -> print('login') 추가  
><br>
> ` git add . `  
> <br>
> ` git commit -m 'Create login' `  
<br>  

### 모듈 2
##### 브랜치 hotfix/login 생성 후 파일 login.py 수정 편집, 1개 커밋 
> ` git switch -c hotfix/login `  -> hotfix/login 브랜치 생성 후 이동  
> <br>
> ` echo "print('hotfix login')" >> login.py `  -> login.py에 print('hotfix login') 추가  
> <br>
> ` git commit -am 'Add hotfix login' `  
<br>

### 모듈 3
##### 다시 main브랜치에서 나머지 2개 커밋
> ` git switch - `  -> main브랜치로 이동  
> <br>
> ` echo "print('func1')" >> login.py `  -> print('func1') 추가  
> <br>
> ` git commit -am 'Add func1' `   
> <br>
> ` echo "print('func2')" >> login.py `  -> print('func2') 추가  
> <br>
> `git commit -am 'Add func2' `  
> <br>

### 모듈 4
##### 브랜치 main에서 바로 이전커밋 (head^) 에서 새로운 브랜치 feat/edit를 생성 #edit.py 생성 후 커밋
> ` git switch -c feat/edit HEAD^ `  -> feat/edit브랜치 생성 후 이동 (HEAD^는 이전 커밋)  
> <br>
> ` echo "print('edit')" >> edit.py `  
> <br>
> ` git add . `  
> <br>
> ` git create -m 'create edit' `  
<br><br>

##### 결과화면

![image](https://user-images.githubusercontent.com/115628899/202844246-bfb62ea4-43a8-4387-b0cc-f7776beb9402.png)









