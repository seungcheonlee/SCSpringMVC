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
<img width="509" alt="스크린샷 2022-02-18 오후 2 31 22" src="https://user-images.githubusercontent.com/85739056/154624662-77902235-33ec-445c-b7de-205e1abd1133.png">
- read.jsp에서 댓글 수정하기를 실시간 댓글 수정으로 사용하기 위해서 ajax로 구현하였음. 클라이언트가 id값이 replyModBtn 인 버튼을 클릭하면 댓글 수정을 할 수 있으며 replytext에 기재된 html 내용과 modal-title에 있는 글제목 값을 변수로 담아 url:'/ex/replies/'+rno 의 경로에 있는 컨트롤러로 보내는 MVC 구조.

<img width="875" alt="스크린샷 2022-02-18 오후 2 32 31" src="https://user-images.githubusercontent.com/85739056/154625172-b310a2c5-12d6-4e13-873d-2eb2a2d92146.png">
- html option 태그와 jstl의 <c:out> 태그를 이용하여 pagemaker의 searchtype에 맞추어 title, content, writer, title or content 등을 이용하여 검색 옵션을 추가함.

<img width="671" alt="스크린샷 2022-02-18 오후 2 33 05" src="https://user-images.githubusercontent.com/85739056/154626375-d7ffa289-be88-4f69-94d4-535670af6723.png">
<img width="721" alt="스크린샷 2022-02-18 오후 2 33 12" src="https://user-images.githubusercontent.com/85739056/154626378-b8a572a5-6047-4d5b-8cfa-8303c030b3ea.png">
- pring에서는 body와 헤더 정보, 상태 코드 등을 담을 수 있는 ResponseEntity가 제공된다. ResponseEntity로 추가적인 정보를 설정할 수 있다. 예를 들면 존재하지 않는 id를 가진 user를 조회하면 404 상태 코드를 return 하도록 작성하였다. 사진에 있는 HttpStatus.BAD_REQUEST의 404에러와 같은 상태 코드를 return 할 수 있다. view 로 전달할 때에는 e.getMessage() 내장 함수를 사용한다. ResponseEntity는 일반적인 객체 뿐만 아니라 List와 Map 등 다양한 객체들을 담아서 전달이 가능하기에 게시판 작업에서 매우 용이하다. 단 한번의 HashMap이나 객체를 전달할 때에는 List Map이 유용하지만 이번 게시판 작업에서는 Rest API를 사용하였다.

5. 결과 화면
