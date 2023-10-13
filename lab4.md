# Lab 4:Lecutre Note on Shell Commands
***Author:*** 202334345 최수정
### pwd
---
현재의 경로 또는 디렉토리의 정보를 보여줌
```
$ pwd
/C/Users/최 수 정
```
### cd
---
디렉토리를 변경

**여러가지 arguments를 줄 수 있다**
- [directory name]
- **/** 최상위 디렉토리로 이동
- **.** 현재 디렉토리로 이동
- **.\.** 한단계 상위레벨의 디렉토리로 이동
- **~** home of current user
- **/[direcotry name]**
- **./[direcotry name]**
- **.\./[direcotry name]**
```
$ cd oss
$ pwd
/c/Users/최수정/oss
$ cd ..
$ pwd
/c/Users/최수정
$ cd /
$ pwd
/
$ cd ~
$ pwd
/c/Users/최수정
```
### ls
---
파일이나 디렉토리를 출력

**option을 선택할 수 있다(대부분의 sheel command는 option 선택 가능하다고 함)**
- **-l** 추가적인 상세한 정보를 볼 수 있다 long format
- **-lh** 파일 사이즈를 사람이 읽기 쉽게 바꿔줌
```
$ ls
 AppData/
'Application Data'@
 Contacts/
 Cookies@
 Desktop/
 Documents/
 Downloads/
 Favorites/
 Intel/
 oss/
 $ ls -l
 (파일에 대한 권한 정보) (소유 정보) (용량) (생성날짜) (파일명)
```

**이 외에도 ls는 굉장히 다양한 옵션과 사용방법이 있음**
- ls /bin 현재 디렉토리를 유지한 상태에서 다른 디렉토리를 출력
- ls -l /etc /bin 
- ls -la .\. 모든 파일을 다 보여줌

### clear
---
화면에 출력된 모든 내용을 지워줌
```
$ clear
```
### cp
---
파일과 디렉토리를 복사함
```
$ cp (복사할 원본 파일) (어떤 이름이나 경로로 저장할 지에 대한 것)
```
### mv
---
파일과 디렉토리를 이동하거나 이름을 바꿀 때 사용
```
$ mv (바꿀 원본 파일) (바꿀 이름명)
$ mv (이동할 원본 파일) (경로)
```
### rm
---
파일이나 디렉토리를 지울 수 있음 *(주의해서 사용해야함)*
```
$ rm (파일명)
$ rm -i (파일명)
$ rm -r (디렉토리명)
```
### mkdir
---
새로운 디렉토리를 만드는 명령어
```
$ mkdir (디렉토리명)
```