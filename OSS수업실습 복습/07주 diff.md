# 07주 수업 실습

### 모듈 1
##### SA와 WD의 파일 차이 보기(diff)
>__SA와 WD의 파일 비교해보기__  
> ` git init gdiff ` -> 저장소 gdiff생성  
> <br>
> ` cd gdiff ` -> gdiff로 이동  
> <br>
> ` touch dtype.py ` -> 빈 파일 생성  
> <br>
> ` git status ` -> WD에만 파일 있음  
> <br>
> ` git diff ` -> SA와 WD 비교 (SA가 비어있으면 출력없음)  
> <br> 
> ` echo "print('python')" >> dtype.py ` -> print('python')추가  
> <br>
> ` git add . ` -> add  
> <br>
> ` git status ` -> SA에 dtype.py있음  
> <br>
> ` git diff ` -> SA와 WD의 파일의 차이가 없으면 출력하지않음  
> <br>
> ` echo "print(list('python'))" >> dtype.py ` -> print(list('python'))추가  
> <br>
> ` git diff ` -> SA와 WD파일의 차이가 있기 떄문에 로그뜸  
<br>

### 모듈 2
##### git diff --cached
> ` git diff --cached ` -> HEAD와 SA를 비교 (현재 SA에 1줄 작성돼있기 때문에 로그뜸)  
> <br>
> ` git commit -m 'add string type' ` -> commit   
> <br>
> ` git diff --cached ` -> HEAD랑 SA차이가 없기때문에 로그 안뜸  
> <br>
> ` git diff head ` -> HEAD랑 WD는 차이가 있기 떄문에 로그 뜸  
> <br>
> ` git add . ` -> add (현재 WD(2줄) = WA(2줄) =! HEAD(1줄))  
> <br>
> ` echo "print({i:ord(i) for i in 'python'})" >> dtype.py ` -> WD, SA, HEAD 각각 다르게 만들기  
> <br>
> ` git diff ` -> SA와 WD비교 (SA와 WD는 한줄 차이나기때문에 로그뜸)  
> <br>
> ` git diff --cached ` -> HEAD와 SA비교 (한줄 차이나기 때문에 로그뜸)  
> <br>
> ` git diff head ` -> HEAD와 WD비교 (두줄 차이나기 때문에 로그뜸)  
<br>

