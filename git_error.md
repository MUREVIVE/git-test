- modified content, untracked content 문제로 1시간 넘게 헤맨 것을 해결

https://secjong.tistory.com/2

<br>

- git status할 시 한글 깨짐 현상 발생 (ex : 123/45/335...)

: git config --global core.quotepath false

<br>

- programmers 폴더를 push한 후 git에 여전히 programmers/sql/...sql 와 같이 untracked file이 존재하는 경우

: git clean -f 를 사용하여 해결. (더 자세한건 구글에 쳐볼 것.)

<br>

- github에 repository 새로 만들고자 할 때 (원하는 폴더만 저장하는게 아니라 자꾸 git내 전체 폴더들이 저장돼서 적는다.)

: github에 repository를 만든 후, local repository에서 해당 repository의 이름을 가진 폴더가 git폴더에 있어야 한다.

(예를 들어 programmers 폴더라고 하면, 이 폴더는 empty 상태여서는 안된다.)

: 처음으로 push하고자 하는 파일이 programmers/sql/asdf.sql이라고 한다면, git bash에서 경로가 ~/git/programmers에 와서

: git init / git add sql / git commit ~ / git remote ~ / git push -u origin master 

: 위 과정을 거치는 것이다.

<br>

- 약 2일간의 git 문제 해결

    - 겪었던 대표적 git error 

    - fatal: The current branch master has no upstream branch.  
    To push the current branch and set the remote as upstream, use  
    git push --set-upstream origin master

    - git push origin master -> error: failed to push some refs to

    - fatal: The current branch master has no upstream branch.

    이 세가지 문제들에서 자꾸 돌고 돌아가지고 결국 git을 초기화하는 것으로 해결했다. (마치 컴퓨터 초기화한다는 느낌이랄까?)  
    덕분에(?) codeit repository의 commit들이 다 날아갔다.. ㅅㅂ  

    https://blog.itpaper.co.kr/git-%EC%A0%80%EC%9E%A5%EC%86%8C%EC%B4%88%EA%B8%B0%ED%99%94/  

<br>

- ![image](https://user-images.githubusercontent.com/51858239/94357270-660a1100-00d2-11eb-8e56-aae4baae8290.png)

(repository명이 바뀌어 며칠동안 commit 흔적이 보이지가 않았음.)

- ![image](https://user-images.githubusercontent.com/51858239/94357291-a073ae00-00d2-11eb-8624-f5a9fabaac7d.png)

(https://qastack.kr/programming/30443333/error-with-renamed-repo-in-github-remote-this-repository-moved-please-use-th

위 사이트의 도움으로 해결)

- commit을 했음에도 contribution 그래프가 안채워지는 경우

: 나의 경우 user.email이 다른 email이었음.

    - git config user.email : 자신의 이메일 주소 확인 방법
    
    - git config --global user.email 바꿀@이메일주소.com

<br>

- git rm -r . 복구하기 : git reset --hard HEAD

- GH001: Large files detected.

-> 이 후 과정에서 막혔음. db_project 살려내 
