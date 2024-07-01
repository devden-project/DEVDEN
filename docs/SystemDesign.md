# 시스템 설계 문서
**프로젝트 주제** : 블로그와 커뮤니티 결합 사이트 개발  
**프로젝트 관리자** : 고진혁  
**작성일** : 2024년 6월 23일  
**버전** : 1.0
## 문서 개요
### 목적
이 문서는 커뮤니티 사이트 개발을 위한 시스템 설계를 명확히 정의하고, 개발자들이 이를 구현할 수 있도록 가이드라인을 제공
## 아키텍처 개요
### 시스템 아키텍처
* 클라이언트-서버 아키텍처 기반, 프론트와 백엔드로 구성
* **프론트** : React
* **백엔드** : Spring
## 데이터베이스 설계
### 데이터베이스 개요
MySQL을 사용하여 사용자 정보, 게시글, 댓글 등의 데이터 저장
### ER 다이어그램

### 테이블 정의
#### 사용자
* **이름** : USER
* **컬럼** :
  * id(PK)
  * username
  * password
  * email
  * create_dt
#### 사용자 프로필
* **이름** : USER_PROFILE
* **컬럼** :
  * user_id(fk)
  * profile_image
  * address_work
  * univ
  * 전공
  * 직책
  * 경력
  * 관심분야
  * 보유 기술
  * 자격증/수료증
  * 수상경력
  * 프로젝트 등록
  * 전화번호
#### 게시글
* **이름** : POST
* **컬럼** :
* id(pk)
* user_id(fk)
* title
* content
* major_category
* minor_category
* like
* post_visible
* community_visible
* create_dt
* update_dt
#### 댓글
* **이름** : Comment
* **컬럼** : 
* id(pk)
* post_id(fk)
* user_id(fk)
* comment
* parent_id(comment_id 대댓글 용)
* create_dt
* update_dt
## API 설계
### API 개요
백엔드는 RESTful API를 제공하여 프론트엔드와 데이터베이스 간의 상호작용을 처리
### 엔드포인트 정의
#### 로그인
* **경로** : ("/login")
* **메서드** : POST
* **요청** : 
* **응답** :
#### 회원가입
## UI/UX 설계
### UI 개요
### 화면 설계
#### 메인페이지
* **설명** : 
* **와이어프레임** :  
![main page](./design/Logo.jpg)
* **사용자 플로우** :
  1. 123
  2. 123
  3. 123
#### 로그인페이지
#### 회원가입 페이지