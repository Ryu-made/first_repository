# 설치과정
1. git 프로그램을 Download하고 설치(default)
2. git을 설정하기 위한 workspace 폴더 생성.
3. GitHub 사이트에 접속하여 회원가입 및 로그인 진행.
4. 우측 상단 "new Repository" 클릭
   * 내용을 입력하고 생성 > 생성된 주소를 복사
5. workspace 폴더 내에서"git Bash" 실행
6. 초기설정

   : git config --list(내용확인)

   : git config --global user.name

   : git config --global user.email 
   * Git을 설치하고 나서 제일 먼저 해야하는 것은 "계정정보" 설정입니다.
   * Git은 commit할 때마다, 이 정보를 사용합니다. (한 번 커밋한 정보는 변경이 불가능합니다.)
7. 초기화
   : git init #기본 브랜치 생성
   * ".git" 폴더 생성
      - 저장소의 환경설정 정보, 히스토리 정보 등을 가지는 폴더
8. 원격 저장소 설정
   * git remote add [저장소 별칭] [URL]

# 파일 Push
1. workspace 폴더 내 README.md 파일 생성 및 내용 작성
2. 상태 확인
   - git status
3. 저장소에 변경된 파일을 관리할 수 있도록 추가
   - git add .
   - git add README.md
4. Local Repository에 저장
   - git commit -m "커밋 메시지"
   - 커밋 메시지는 해당 작업에서 변경된 사항을 간략히 작성함
   - 다른 작업자를 위한 설명, 되도록 영어로 작성
5. Remote Repository에 저장
   - git push first_remote_repo main

## README.md 파일
   - README.md 파일은 주로 프로필 혹은 Repository에 대한 설명을 나타내기 위해 작성
   - 소스를 정리하는 데 큰 도움
   - 마크다운(MarkDown) 문법
   : 사용이 쉽고, 마크업 언어인 HTML 태그에 비해 간단하기 때문에 문서작성이 편리
   : 마크다운을 지원하는 프로그램이나 사이트에서만 사용가능(HTML은 어떤 브라우저든 사용 가능)
## Header
   * #... h{n} : #과 글자 사이에는 띄어쓰기로 구분
   > ## 제목2
   > ### 제목3
   > #### 제목4
## 줄바꿈 : 엔터 2번
## 순서가 있는 목록(ol : ordered-list) : 1,2,3,.. 숫자 나열
1. first statement
2. second statement
3. third statement
## 구분선(Division Line) : - 혹은 * 3개 이상 사용
---
***
- - -
* * *
--------
********
## 코드블럭(Code Block) : 코드를 기준으로 위아래 빈 한줄씩 추가 && 코드를 기준으로 4칸 들여쓰기
+ ex) <pre><code> 태그를 이용해서 작성
<pre>
<code>
   public class Class01 {
      private String str;
      private int count;
      public static void method() {
         System.out.println(str);
         System.out.println(count);
      }
   }
</code>
</pre>
+ ex) `\`\`\java {코드블럭} \`\`\` 으로 작성 (java를 입력하면 구문강조표시 가능)
```java
   public class Class02 {
      private String str;
      private int count;
      public static void method() {
         System.out.println(str);
         System.out.println(count);
      }
   }
```
## 하이퍼링크(HyperLink) : <>(앵글브라켓) 안에 http(s)를 포함하는 주소 입력
<https://github.com>   <https://www.naver.com>
---
##### {2024.09.20}
### 깃 플로우(Git Flow, Branch)
* 기본적으로 master라는 하나의 branch를 가진다.
   - 새로운 브랜치를 만들면 master 브랜치와 독립적인 작업이 가능하다
   - checkout하지 않으면 모든 작업은 master 브랜치에서 커밋(저장)한다.
