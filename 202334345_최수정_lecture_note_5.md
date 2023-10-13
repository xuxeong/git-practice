# Lab 5:Lecutre Note on Shell Commands
***Author:*** 202334345 최수정
### Standard Ouput
---
어떤 명령을 내릴 때 그 출력의 기반이 되는 것 ex. screen
\> : 특정 내용을 어떤 파일에 저장할 때 사용
cat : 파일의 내용을 그대로 출력해줌
\>\> : 예전의 내용에 새로운 내용을 추가할 수 있게 함
```
$ ls -lh > 내용을 저장할 파일 이름
$ cat 파일 이름
$ ls -lh >> 파일 이름
```
### Standard Input
---
\< : 파일의 내용을 읽어와 전달해줌
sort : 정렬 명령어
\< \> : 함께 사용하면 특정 파일에 특정 파일의 내용을 불러와 넣어주는 등의 기능을 할 수 있음
```
$ sort < 불러올 파일 이름 > 저장할 파일이름
```
### Pipelines "|"
---
앞서 있는 커맨드의 출력을 그대로 다음 커맨드에 입력으로 가져감
```
$ ls -lh | less
$ ls | wc-l
```

### Expansion
---
특수한 캐릭터들이 쉘 커맨드에 들어가기 전에 확장 되는 것을 말함
echo : 뒤에 오는 텍스트를 출력
\* : echo 뒤에 넣으면 ls 와 같은 기능을 하게 됨
\~ : echo 뒤에 넣으면 현재 사용자의 홈 디렉토리를 expansion하게 됨 결과적으로 현재 사용자의 홈 디렉토리를 출력하게 됨
```
$ echo 출력내용
$ echo *
$ echo ~
$ echo ~유저이름
```
***Tip.*** *backslash + enter*
### Permissions
---
Linux는 파일과 디렉토리에 3단계의 권한을 부여하고 있음
-> owner / group / others
chmod: 권한 변경 명령어
```
$ ls -l /bin/bash
-rwxr-xr-x 1 (owner) (group) (others)
$ chmod (권한을 나타내는 세자리 숫자) (권한을 변경할 파일이나 디렉토리 이름)
```
***rwx :*** *read, write, execute*
***-*** : *그 위치에 해당하는 권한이 없다는 의미*

권한을 나타내는 세자리 숫자는 2진수를 생각하면 됨
### Superuser
---
시스템 관리자를 생각하면 됨
sudo : superuser 권한으로 설정할 수 있음
-i : sudo뒤에 붙이면 한동안 그 뒤에도 sudo를 계속 쓰지 않아도 superuser권한으로 실행 가능 *(권장하지않음)*
exit : sudo setion에 들어갔다가 다시 본인 계정으로 돌아올 때 사용
```
$ sudo (명령어)
```
### Shell Script
---
텍스트 파일로 작성하며 여러가지 shell command가 순차대로 실행됨
```
$ sh 파일
```
***tip :*** *history 과거의 모든 명령들을 보여줌*