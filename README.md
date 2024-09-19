# 설치과정
1. git 프로그램을 Download하고 설치(default)
2. git을 설정하기 위한 workspace 폴더 생성.
3. GitHub 사이트에 접속하여 회원가입 및 로그인 진행.
4. 우측 상단 "new Repository" 클릭
   - 내용을 입력하고 생성 > 생성된 주소를 복사
5. workspace 폴더 내에서"git Bash" 실행
6. 초기설정
   : git config --list(내용확인)
   : git config --global user.name 
   : git config --global user.email 
   - Git을 설치하고 나서 제일 먼저 해야하는 것은 "계정정보" 설정입니다.
   - Git은 commit할 때마다, 이 정보를 사용합니다. (한 번 커밋한 정보는 변경이 불가능합니다.)
7. 초기화
   : git init
8. 원격 저장소 설정
   - git remote add [저장소 별칭] [URL]
9. workspace 폴더 내 README.md 파일 생성 및 내용 작성
10. 상태 확인
   - git status
11. 저장소에 변경된 파일을 관리할 수 있도록 추가
   - git add .
   - git add README.md
12. Local Repository에 저장
   - git commit -m "커밋 메시지"
   - 커밋 메시지는 해당 작업에서 변경된 사항을 간략히 작성함
   - 다른 작업자를 위한 설명, 되도록 영어로 작성
13. Remote Repository에 저장
   - git push first_remote_repo main
