https://homeproject.tistory.com/9 참고

git upload 핵심 순서

1. 원하는 디렉토리로 간 다음 (나의 경우 git이라고 적힌 파일로 지정) 

2. git clone 원격저장소 주소 입력.
-> 깃허브에 readme파일이 존재하는 경우 로컬 저장소 역시 readme파일이 생길 것임.

3. git_test.txt를 만든 후

4. txt를 저장하고자 하는 파일로 cd한 후

5. git status
-> 이 때 빨간색으로 git_test.txt가 뜰텐데 이걸 git add명령어로 이용해야 함.

6. git add git_text.txt

7. git status
-> 이 때 초록색으로 git_text.txt가 뜨면 commit할 수 있는 상태가 된 것임.

8. git commit -m "test"

9. git remote add origin https://github.com/MUREVIVE/os_project.git
(로컬저장소와 깃허브 원격저장소를 연결.
- git remote -v : 연결 확인

10. git push
-> 로컬저장소의 파일이 원격저장소(깃허브)로 올라간다.
