# HTML
## Hyper Text Matkup Language
### HTML은 웹문서의 구조를 담당하는 언어이다.
* HTML에서 구조는 <> 로 묶인 태그로 작성한다.
* <시작태그></닫기태그>
* <빈태그> 
* 시작과 닫기태그는 한쌍의 요소로 불린다.
### HTML 구조태그
* HTML5 버전 선언하는 <!doctype html>
* HTML 웹브라우저 구조 처리하는 태그들
1. < html >< /html >
2. < head >< /head >
3. < body >< /body >
----
# git&gitHub
* 버전관리 프로그램 git
* 버전 파일, 폴더들을 저장하는 저장소 gitHub
## git 용어와 뜻
* 작업 디렉터리 : 실제 작업하는 로컬 저장소(윈도우 탐색기 개념)
* 스테이징 :깃허브에 작업 업로드 전 파일을 대기시키는 대기소
* repository : 대기소(stage)에 파일 대기 후 최종 github 업로드 저장소
## 주의사항
* 당일 작업 기준 github 저장소와 로컬저장소의 파일, 폴더 상태가 같아야한다.
* 동일한 저장소를 관리하는 사람을 경우 작업컴퓨터가 달라도 gitconfig에 등록된 이름, 이메일이 동일해야 한다.
----
# 주요 단축기 모음
* ctrl+ / 한줄 주석
* shift + alt + a선택한 영역만 주석
# 처음 git을 이용한 github 저장소 업로드 시 해야하는 순서
1. 현재 사용중 로컬 저장소를 git 저장소로 등록 git init
2. 위 1번 정상 등록 시 경로에 (master) 표시 출력
3. master -> main으로 최상위 경로명칭을 변경하기 위해 git branch -m main 작성
4. github 저장소 생성 후 저장소 주소 복사
5. 현재 로컬 저장소 github 저장소 연결 git remote add origin 주소붙여넣기
6. git status 현재 상태확인 (스테이징, 작업디렉터리, 저장소)
7. 위 6번 결과 파일이 빨강색으로 출력될 경우 git add 파일명 스테이지에 올리기
8. git status 위 7번에서 올린 파일이 초록색으로 변경된 걸 확인
9. git commit -m '기록메세지' 스테이징 파일을 저장소에 올리기 위한 기록설정
10. git push origin main github 저장소에 최종 파일, 폴더 업로드
11. 위 10번 처음 진행 시 github 계정 안증 화면나오니 인증 진행 후 저장소 들어가서 F5
## 다른 환경에서 이어서 작업해야 하는 경우
1. 폴더 생성하기 (영어,날짜) -> vs code 폴더 연결
2. github 저장소 주소 복사
3. vs code 돌아와서 ctrl + j 터미널 실행 후 bash 환경 변경
4. git clone 저장소 주소 붙여넣기
5. 터미널 경로 오른쪽에 main 또는 master 표시가 있는지 확인
6. 위 5번에서 표시가 없다면 cd 복제한폴더명
7. 자유롭게 수정 후 파일 저장
8. 터미널에 git status업로드 안된 파일 빨강색 색 확인
9. git add 파일명 수정한 파일 스테이지에 업로드하기
10. git status위 9번 업로드 됐는지 확인 (초록색 변경)
11. git commit -m '메세지' 수정 파일에 대한 기록 메세지 작성
12. git push origin main github 저장소에 업로드
----
# HTML과 meta의 속성
## HTML
* 여기서 html의 속성은 lang 언어이고, ko는 값이며 코리아를 뜻한다.
* 컴퓨터의 화면 낭독 소프트웨어 "스크린 리더"라고 부른다.
## meta
* < meta charset="utf-8" >
* 언어를 다국어로 설정하고 head에 입력한다.
* <meta name="description"content=""> 검색어 제목 밑에 요약, 설명을 덧붙일때 사용한다.
* <meta name="keywords"content=""> 키워드로 사용자가 검색했을 때 관련되어 내 사이트가 나오게 설정하는 것이다.
----
# day2 HTML
* HTML 작성 시 항상 구조태그 먼저 작성하기
* HTML 작성하면서 유효성검사 자주 이용하기 (반드시 저장 후)
* https://validator.w3.org/#validate_by_upload
### 유효성 검사 오류잡기 TIP
* 유효성 검사 시 전체 오류 개수를 보지말고 가장 윗 줄 에러부터 확인 후 고치기
* 고친 후 vs code에서 바로 파일 저장 후 다시 유효성 검사하면서 에러잡기
## HTML TREE
* HTML 작성 시 줄 바꿈, 들여쓰기를 주의하며 태그를 작성한다.
* 관계구조는 부모-자식-자손-형제로 구분된다.
* 형제 관계는 첫째 자식과 마지막 자식으로도 따로 구분한다.
* 형제가 없을 시 외동으로 구분한다.
----
## HTML title 웹접근성
* 사용자가 웹브라우저를 여러 탭으로 놓고 봤을 때 페이지 구분을 쉽게 할 수 있는가?
* 페이지명 | 사이트명
* 페이지명에 들어가는 후보 : 상품명, 페이지경햐로, 상품 관련 부가정보 등등..
* 사이트명에는 광고문구가 같이 들어갈 수 있다. : 깊이 빠져들다 CGV
* 잘못된 예) 네이버 블로그, 네이버 카페
* 잘된 예) 책제목 | 저자 | 출판사 | 교보문고 , 쇼핑몰 상품 | 쿠팡
----
# 다앙한 문거 태그 종류
## block & inline
* body
* 존재하는 모든 HTML태그의 두 분류 = 블록과 인라인 (block tag & inline tag)
* 블록 (b) : 큰 레이아웃 개념, 폭 100%, 새로운 행 배치 (→ 줄바꿈) → 코끼리, 옆으로 자리가 없어서 밑으로 배치된다.
* 인라인 (i) : 작은 요소 개념, 폭 자기 자신만큼 인식, 옆으로 배치 → 뱀, 기본적으로 옆으로 가다가 자동 줄바꿈으로 밑으로 떨어진다.
1. 블록은 인라인을 담을 수 있다. → 블록은 부모가 될 수 있다. 블록 안에 블록 가능
2. 인라인은 블록을 담을 수 없다. → 인라인은 부모가 될 수 없다. 인라인 안에 인라인은 가능
* 태그 사용 시 그 태그가 인라인 인지 볼록인지 먼저 확인하고 사용하기!
* 블록-블록-블록 O
* 인라인-인라인-인라인 O
* 블록(인라인) O
* 인라인(블록) X
* 블록(블록) O
* 인라인(인라인) O
* -=형제, ()=자식
----
## (b)h태그(heading)
* 제목태그 h태그는 1~6 레벨을 가진다. 1이 가장 중요하다.
* 메인페이지, 서브페이지에 따라서 h1이 어디 들어가는지부터 확인하고 나머지 레벨을 순차적으로 결정한다.
* 대표적으로 사이트 로고(h1)와 서브페이지의 페이지제목(h1)이 주로 사용된다.
* 숫자 처리할 때 건너뛰면 X, 무조건 순서대로 처리!
* 제목은 사용자가 사이트에 접속하기 위한 검색키워드로의 목적도 되므로 신중하게 결정한다.
## (b)p 단락 (paragragh)
* 제목의 내용 용도로 주로 사용
* 블록 → 줄바꿈 ⇒ 옆에 공간이 남았는데 줄바꿈이 되어 있으면 블록으로 새로운 행을 만든것이다.
* h 랑 p 형제 → 제목이 끝나고 내용
## (i)br
* 블록 내에서 강제 줄바꿈이 필요한 경우 사용
* 자식으로 br이 들어간다. → h / p 태그
* 오류 가능성이 많아 신중하게 사용해야한다. → 많이 사용하는 편은 아님.
* 글자수가 많지 않은 곳에 사용
* 내용보다는 제목에 사용하는 경우가 많다
* 블록 옆에 쓰면 X → 블록 옆에는 블록만 가능
* 빈태그
## (i)strong
* 블록 안에만 사용
* 중요성, 심각성 또는 긴급성
* 경고성 문구
* 주로 내용안에서 강조할 때 사용
* 제목이 이미 강조라는 뜻을 가지고 있으니까 제목안에는 잘 사용하지 않음
## (i)em
* 문장 내에서 특정 문맥을 강조할 때 사용
* 단순 강조
* 대부분 많이 사용
* 이미 글자를 썼을 경우 : ctrl + x 로 글자 잘라내고 em 태그 쓰고 붙여넣기
## (i)s, del 교체 or 삭제 텍스트
* 블록안에
* 가격교체 or 삭제
* 주로 del 태그를 사용
## (i)sub, sup 아래첨자, 위첨자
* 수학기호같은 처리할 때 사용
* 블록안에
* 많이 사용하지 않음
----
## 태그 작성 시 주의사항
* 부모 요소의 기능 및 디자인은 자식, 자손까지 전달된다.
* 메뉴들이 옆으로 생성되어 있어도 개별 태그로 줘야 한다.
* enter, tab, space는 기본적으로 작용하지 않음.  space는 여러 번 찍어도 한번만 적용된다. → CSS로 해결
* H태그와 P태그를 사용 시 H태그 안에 P태그를 작성하면 H태그의 '제목'이란 의미가 전달되기 때문에 P는 반드시 H 밖에 형제 위치로 작성해야 한다.
* br태그는 인라인태그로 블록 태그안에만 작성할 수 있다.
* br태그는 강제 줄바꿈으로 모바일 ~ 태블릿 ~ PC까지 반응하는 반응형웹에 적합하지 않기 때문에 사용시에는 글자 수가 적은 제목이나 내용 위주로 꼭 필요한 경우에만 사용한다.
----
# day3 HTML
## (b) blockquote 긴 인용문
* p태그 밖에
* cite : 사이트 출처 주소를 넣는 속성
* ex) < blockquote cite=… >< /blockquote >
## (i) q 짧은 인용문
* p태그 안에
* 내용중에 일부만 처리할때
* ex) < q cite=… >< /q >
## (i) code 
* 컴퓨터가 지원하는 다양한 명령어를 화면 표시할 경우
* 강의사이트 등..
## (b) address 연락처, 회사소개, 고객센터 등
* 웹 사이트의 관련 연락처, 소개, 고객센터 정보들을 담을 때
* 다른 블록을 자식 또는 자손으로 배치할 수 없다
* footer 영역에 주로 사용 → 헤더랑 정반대, 맨 밑에, 무조건 존재
* 내 회사에 대한 정보만 작성해야 한다 → 혐력 업체여도 작성하면 안됨,  < p > 태그로 처리
* 인라인만 가능 (em, strong, s, del, sub, sup, br, q, code)
## (b) hr 수평선
* 사이트 각 영역을 구분할 때 사용
* 경계구분용
* CSS에서는 표현하지 않고 숨기는 경우가 대부분
* 주석과 같이 태그 구조 이해에 주 용도로 사용
* 블록과 형제로 → p, addrees …
* 대부분의 선은 디자인으로 표현
* h p em addrees
----
# 레이아웃 태그
## (b) 그룹 div
: 2개 이상의 인라인 or 블록 요소를 묶어주는 그룹 태그
## (i) 인라인 그룹 span
: 개 이상의 인라인 요소를 묶을 때 사용
* 가까이 있는 레이아웃 묶기
* 의미도 같고 디자인도 같은 요소들
# 태그+이름 속성 Class, id
* .Class: 반복 유형 분류 시 사용, 반복지정가능 → 설문조사, 글꼴이나 색
* #id : 전체 페이지 중 단 하나의 요소에만 지정 시 사용 → header, footer, 하나의 큰 덩어리를 명칭할 때
* Class, id는 태그 관계없이 모든 태그에 적용 할 수 있다.
* id의 이름을 중복해서 사용하려면 class로 변경 후 사용.
* 이름작성시 주의사항 : 반드시 용도에 맞는 의미있는 영단어 사용!
* 다른 단어는 구분해서 작성 -> title_g
* 길게 쓰더라도 의미있게 작성하는게 중요
# 하이퍼링크 태그 < a >
### (b)(i) 링크태그 < a > 
* 원래는 인라인이었으나 버전5부터 필요에 따라 블록으로도 처리가능하다.
* 형제로 블록/ 인라인 결정
* 인라인 특성으로 옆으로 배치
* HTML < a > 요소 (앵커요소)는 href 속성을 통해 다른 페이지나 같은 페이지의 어느 위치, 파일, 이메일 주소와 그 외 다른 URL로 연결할 수 있는 하리퍼링크를 만든다.
* 2개의 요소 image - span
* < a > - < a > 형제관계 
1. 절대경로
* 절대경로는 변하지 않는 주소로 쉽게 말해 흔히 알고 있는 웹 주소를 떠올리면 된다.
* http://naver.com  → 네이버가 망하지 않는 한 사라지거나 변경되지 않는 주소
* 절대경로는 http:// 웹 프로토콜로 시작  /  https:// → 안전한 웹 프로토콜
### < a href=””> 링크 주소 속성
* 속성 안 값은 링크 목적지 주소를 정확히 입력해야 한다.
* 일반적으로 절대경로, 상대경로로 나뉜다.
* 링크영역은 넓게
* 필수
* 링크는 존재하는 링크가 아닌 내가 만든 링크를 넣어야함 → 안만들었을 때는 임시링크로 ‘#’을 사용한다
    -> < a href="#">
* 링크를 만들게 되면 #을 지우고 링크를 넣기
### < a href=”” target=”” > 링크 위치 속성
* _blank: URL을 새로운 창에 표시합니다.
* 내 사이트가 아닌 목적이 다른 사이트를 연결 → 새로운 탭으로
* 선택
2. 상대경로 (./파일명.확장자)
: 경로를 작성하는 파일((ex)html, css등) 기준으로 연결하는 파일의 위치를 작성하는 것
* 같은 위치 : ./파일명명.확장자
* 하위 위치 : ./폴더명/파일명.확장자, 현재 위치에서
* 상위 위치 : ../폴더명/파일명.확장자, 한번위로
* 같은 파일안에서 링크 → id 태그 걸어주기
    * 이동하고 싶은 내용을 id 태그안에 적기 -> 눌러서 이동할 링크태그로 가서 id 태그 적어주기