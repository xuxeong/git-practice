# Lab 6:Lecutre Note on Git
***Author:*** 202334345 최수정
### Git이 중요한 이유(Version Control & Collaboration)
---
Git: version control와 collaboration 기능을 가진 소프트웨어
**version control**: branch에 새로운 version의 내용을 써놓고 필요한 경우에 따라 version을 선택해서 사용할 수 있음
**collaboration**: 누가 언제 어떻게 수정했는지 등 규칙과 필요한 내용을 제공 
### Version Control 방법1
---
Changes
-한 파일에 대한 변화를 기록하는 것
-한 파일의 변화 과정에 따른 버전을 각각 선택하기 어려움
Snapshosts
-Git이 채택한 방식
-한 파일에 대한 변화를 기록하는 것이 아니라 각각의 버전에서 원본 파일 전부 가지고 있음
### Version Control 방법2
---
Local
-잘 사용하지 않음
Centralized
-version control을 관리하는 중앙서버가 각 컴퓨터의 요청을 받아 version을 보내주는 형식
-단점: 중앙서버가 다운될 경우, 어떤 파일이 손상을 입었을 경우 사용하기 어려움
Distributed
-Git이 채택한 방식
-version database를 중앙컴퓨터 뿐 아니라 각 컴퓨터에도 통째로 복사해와서 사용
-centralized와 달리 바로 복구하기 쉬움
### Three Staes in Git
---
1 Stage Fixes (Working Directory -> Staging Area)
2 commit(Staging Area -> git directory)
3 Checkout the project
### Git config
---
Three Levels
1 System level: --system option. 모든 사용자들과 저장소에 영향을 줌(관리자 권한이 있어야 사용 가능)
file: /etc/gitconfig
2 Global(user) level: --global option. 현재 명령어를 실행한 유저의 모든 저장소에 영향을 줌
file: ~/.config/git/config
3 Local level: --local option. 그 저장소 안에서만 영향을 줌
file: .git/gitconfig
$git config --list 현재 쓰여지고 있는 config 확인
git config --list --show-origin :어떤 레벨에서 작성된 건지 확인할 수 있음
```
$ git config --global user.name "Sujeong Choi"
$ git config --global user.emial your-email-address(이메일 주소)
$ git config --global init.defaultBranch main

$ git config --list
$ git config --list --show-origin
$ git config user.name
```
### git Command
---
**git init**: Initializinga Repository in an Existing Directory
**git status**: Checking repository status
**git add[file_name]**: 파일을 스테이지에 올리는 명령어
***이미 stage에 올린 파일을 수정하면 수정한 파일은 changes not staged for comit에 저장됨 
즉, 무언가 수정했다면 다시 git add 명령어를 이용해야 함***
**git add .**: 현재 레파지토리의 모든 파일을 스테이지에 올림
**git ram --cashed[file_name]**: 스테이지에 올렸던 파일을 다시 스테이지에서 내리는 명령어
**git commit -m "commit message"**: commit 명령어. -m "commit message"는 필수입력사항은 아니나 대부분의 경우 권장하고 있음
**git log**: 지금까지 git을 수정한 내용들을 볼 수 있음
**git branch**: 현재 branch확인
**git branch -m 바꿀 브랜치**
```
$ git init
$ git status
$ git add [file_name]
$ git add .
$ git rm --cashed [file_name]
$ git commit
$ git log
$ git branch
$ git brach -m [branch_name]
```
### .gitignore
---
위와 같은 이름을 가진 파일을 만들고 그 파일에 무시하고 싶은 파일 이름을 적고 저장하면 git add . 명령어를 사용해도 이름이 적힌 파일들은 올라가지 않음
*ppt 예제 참고*