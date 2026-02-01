# CSRF(Cross-site request forgery)란?
> 서버가 실제 서비스 페이지를 통한 정상요청인지 확인하지 않고 처리하는 경우 악의적인 스크립트를 이용하여 다른 사용자의 권한으로 게시판 자동 글쓰기, 자동 회원가입, 중요기능 실행 등의 공격을 할 수 있는 취약점
출처: https://mokpo.tistory.com/245 [MSS:티스토리]
--- 

<img width="694" height="420" alt="image" src="https://github.com/user-attachments/assets/470627ac-5208-4618-ae7c-069a805644b8" />


|  	| XSS 	| CSRF 	|
|---	|---	|---	|
| 공격대상 	| Client 	| Server 	|
| 목적 	| 스크립트 실행이 목적 	| 특정 행동을 유도 	|
| 공격방법 	| 인증된 세션 없이 공격<br>ex)악성코드 사이트로 리다이렉트, <br>인증(로그인)없이 피해를 입힐 수 있음 	| 인증된 세션을 악용하여 공격<br>ex)반드시 인증된 사용자를 공격 	|
