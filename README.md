# SCSpringMVC
My spring MVC project.
1. 개발환경
- java 1.8
- tomcat 9.0.48
- oracle 18c
- spring sts3 4.3.5
- mybatis
<img width="934" alt="KakaoTalk_20220218_123021686" src="https://user-images.githubusercontent.com/85739056/154613763-c3e9b42e-39fd-4d72-becd-7587bc724e30.png">

2. 개발 일정
- 2022-01.15 ~ 2022.01.20
- Srping MVC 기본 개발환경 설정 (set java version 1.8, poom.xml, root-context, web.xml, mybatis)
- 오라클 데이터 베이스 table 생성

3. 프로젝트 구조
- 스샷 첨부
<img width="324" alt="스크린샷 2022-02-18 오후 12 20 20" src="https://user-images.githubusercontent.com/85739056/154611462-1ff67e5a-b480-45ba-85e8-7fcad6725575.png">
<img width="308" alt="스크린샷 2022-02-18 오후 12 20 06" src="https://user-images.githubusercontent.com/85739056/154611478-ea76bdca-b5b8-4aca-9619-eb98a21c498e.png">

4. 주요 기능 로직
![ajaxReplyModify](https://user-images.githubusercontent.com/85739056/154622386-3c730c51-4e29-451c-ba7c-76a8fe4b1120.png)
- read.jsp에서 댓글 수정하기를 실시간 댓글 수정으로 사용하기 위해서 ajax로 구현하였음. 클라이언트가 id값이 replyModBtn 인 버튼을 클릭하면 댓글 수정을 할 수 있으며 replytext에 기재된 html 내용과 modal-title에 있는 글제목 값을 변수로 담아 url:'/ex/replies/'+rno 의 경로에 있는 컨트롤러로 보내는 MVC 구조.


