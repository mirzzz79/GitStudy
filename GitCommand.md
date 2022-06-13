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
[branch]                : 브런치 만들기
[checkout]              : 이동하기
[merge]                 : 병합히기
[pull request]          : 풀 리퀘스트 (병합을 외부에 알리고 github에서 진행할수 있도록 지원)
[release]               : 릴리즈
[fetch]                 : 그래프만 내려 받아 상태를 업데이트 한다.
[pull]                  : 실제 코드를 내려 받아, 프로젝트를 업데이트 한다.
[fork]                  : 원본저장소를 복사해서, 원격저장소를 생성 한다.

[HEAD],[origin/HEAD]    : 브랜치 혹은 커밋을 가리키는 포인터로 서로 다른 브랜치 사이을 넘나들수 있다. (타임머신)

### Branch 생성기준
1. [master] 브랜치에는 직접 커밋을 올리지 않는다. (동시 작업시 꼬일수 있음)
2. 기능 개발을 하기 전에 [master] 브랜치를 기준으로 새로운 브랜치를 만든다.
3. 브랜치 이름은 [feature/기능이름] 형식으로 하고 한명만 커밋을 올린다.
4. [feature/기능이름] 브랜치에서 기능 개발이 끝나면 [master] 브랜치에 이름 합친다.

- 브랜치는 작업물 별로 진행 하며, 작업자 간 하나의 브랜치를 관리하는 것이 좋다.
- 추후 작업이 완료되면, 마무리된 작업을 Master 브랜치로 병합한다.
    1. Master 브랜치로 병합 진행시, 우선 작업 브랜치[feature/기능]에 Master 브랜치를 병합하여, 충돌등을 해결하여, 안정성을 확보한다.
    2. [feature/기능]에 병합이 완료된 내용을 Master 브랜치에 다시 머지 시켜준다.

## github chapter4 
 - 협업을 통한 파일 관리 (원본저장소 > 원격 저장소 : fork)


git 원격 주소 확인
    - git remote -v         
        origin  https://github.com/mirzzz79/GitStudy.git (fetch)
        origin  https://github.com/mirzzz79/GitStudy.git (push)

git 원격 주소 재설정
    - git remote set-url origin https://github.com/mirzzz79/GitStudy.git


push 진행시 아래와 같이 거부되면 set-url를 통해 아이디를 다시 설정해준다.
   remote: Permission to mirzzz79/GitStudy.git denied to mirzzz.

git remote set-url origin https://mirzzz79@github.com/mirzzz79/GitStudy.git/