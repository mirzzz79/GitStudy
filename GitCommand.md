# github command

## github chapter 1
'''sh
- git init
- git log [-g]                      : 로그 보기 (자세히)
- git reflog                        : 작업한 로그만 보기
- git add [./filename]              : 관리 목록에 추가 [Stage]
- git commit -m "msg"               : 로컬 워크 커밋
- git checkout [commit hash key]    : 커밋 이동
- git checkout -                    : 가장 최근 커밋으로 이동
- git remote add origin https://github.com/mirzzz79/GitStudy.git        : 원격 연결 "origin"이라는 이름으로 원격저장소를 추가함.
- git clone https://github.com/mirzzz79/GitStudy.git .                  : 현재 폴더에 clone 받기 (로컬 저장소 생성)
- git push origin master : 원격으로 커밋 내용 전달
- git pull origin master : 원격에서 커밋 내용 받기
'''

## github chapter 2
'''sh
[master]            : 로컬 저장소 버전의 커밋 위치
[origin/master]     : 원격 저장소 버전의 커밋 위치
    origin - 연결한 GitHub 원격저장소의 닉네임
    master - 커밋을 올리기위한 Branch의 닉네임
'''

## github chapter 3
- 협업을 통한 파일 관리
[branch]            : 브런치 만들기
[checkout]          : 이동하기
[merge]             : 병합히기
[pull request]      : 풀 리퀘스트
[release]           : 릴리즈
[fetch]             : 원격 수정 내용을 로컬저장소로 가져온다. (작업 공간으로 가져 온건 아님)

[HEAD],[origin/HEAD]    
 - 브랜치 혹은 커밋을 가리키는 포인터로 서로 다른 브랜치 사이을 넘나들수 있다. (타임머신)

### Branch 생성기준
1. [master] 브랜치에는 직접 커밋을 올리지 않는다. (동시 작업시 꼬일수 있음)
2. 기능 개발을 하기 전에 [master] 브랜치를 기준으로 새로운 브랜치를 만든다.
3. 브랜치 이름은 [feature/기능이름] 형식으로 하고 한명만 커밋을 올린다.
4. [feature/기능이름] 브랜치에서 기능 개발이 끝나면 [master] 브랜치에 이름 합친다.

- People1 Summary 
 branch 생성 

 
