# API 설계 문서
**프로젝트 주제** : 블로그와 커뮤니티 결합 사이트 개발  
**프로젝트 관리자** : 고진혁  
**작성일** : 2024년 6월 23일  
**버전** : 1.0
## 문서 개요
### 목적
이 문서는 커뮤니티 사이트의 RESTful API를 정의하고, 클라이언트는 이 API를 사용하여 서버와 상호작용
## 기본 URL
* **개발** : `'http://oci이용 예정.포트번호`
* **프로덕션** : `https://devden.dev`
## 인증
JWT 및 XSRF-TOKEN 이용, 사용자는 로그인 시 발급된 토큰을 사용하여 인증
### 요청 헤더
```http request
Authorization: Bearer <JWT TOKEN>
X-XSRF-TOKEN: <XSRF-TOKEN>
```
## 엔드포인트
### 사용자 API
#### 회원가입
* **경로** : `/login/register`
* **메서드** : POST
* **요청 헤더** : Content-Type: application/json
* **요청 본문** :
```json
{
  "username" : "",
  "password" : ""
}
```
* **응답** : 
  * 성공(201 Created)
  ```json
  {
    "username" : ""
  }
  ```
  * 실패(400 Bad Request)
  ```json
  {
    
  }
   ```
### 게시판 API
#### 게시글 포스팅