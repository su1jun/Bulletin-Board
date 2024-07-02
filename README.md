# :paperclip: Basic board Project
> 전반적인 웹의 기본 소양이 되는 게시판 프로젝트입니다.

![메인 화면](https://user-images.githubusercontent.com/59757689/149616313-dbeace05-67dc-4d70-b6a1-630d601b6455.PNG)

## 목차
- [들어가며](#들어가며)
  - [프로젝트 소개](#1-프로젝트-소개)    
  - [프로젝트 기능](#2-프로젝트-기능)    
  - [사용 기술](#3-사용-기술)   
     - [백엔드](#3-1-백엔드)
     - [프론트엔드](#3-2-프론트엔드)
  - [실행 화면](#4-실행-화면)   

- [구조 및 설계](#구조-및-설계)
  - [패키지 구조](#1-패키지-구조)
  - [DB 설계](#2-db-설계)
  - [API 설계](#3-api-설계)

- [마치며](#마치며)
  - [프로젝트 보완사항](#1-프로젝트-보완사항)

## 들어가며
### 1. 프로젝트 소개

### 2. 프로젝트 기능

프로젝트의 주요 기능은 다음과 같습니다.
- **게시판 -** CRUD 기능, 조회수, 페이징 및 검색 처리
- **사용자 -** Security 회원가입 및 로그인, OAuth 2.0 구글, 네이버 로그인, 회원정보 수정, 회원가입시 유효성 검사 및 중복 검사
- **댓글 -** CRUD 기능

### 3. 사용 기술

#### 3-1 백엔드

##### 주요 프레임워크 / 라이브러리
- Java 11
- SpringBoot 2.5.6
- JPA(Spring Data JPA)
- Spring Security
- OAuth 2.0

##### Build Tool
- Gradle 7.2

##### DataBase
- MySQL 8.0.19 ~> PostgreSQL

#### 3-2 프론트엔드
- Html/Css
- JavaScript
- Mustache ~> Thymeleaf
- Bootstrap 4.3.1

### 4. 실행 화면
  <details>
    <summary>게시글 관련</summary>   
       
    
  **1. 게시글 전체 목록**   
  ![image](https://user-images.githubusercontent.com/59757689/156975336-c37c9866-bba2-4c69-9a3f-230339a80d5a.png)   
  전체 목록을 페이징 처리하여 조회할 수 있다.   
     
  **2. 게시글 등록**   
  ![image](https://user-images.githubusercontent.com/59757689/156975408-413151f1-3bd8-4788-bc8e-77a2ffbd6eea.png)   
  로그인 한 사용자만 새로운 글을 작성할 수 있고, 작성 후 목록 화면으로 redirect한다.   
     
  **3. 게시글 상세보기**   
  ![image](https://user-images.githubusercontent.com/59757689/156975794-9d7ef3fd-7e03-4a24-99de-d3f7a99c8167.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156975849-f3e02f34-47ed-4b7a-92f5-83ee66bed2bb.png)   
  본인이 작성한 글만 수정 및 삭제가 가능하다.   
     
   **4. 게시글 수정 화면**   
  ![image](https://user-images.githubusercontent.com/59757689/156975898-2f17bc37-df52-418e-8a84-dc17cec37070.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156975948-954960c8-987e-4364-a036-3c58cb66bbdd.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156975965-da3681c1-1a0d-4159-865a-b5c202b1f7ee.png)   
  제목과 내용만 수정할 수 있게 하고, Confirm으로 수정 여부를 확인 후 상세보기 화면으로 redirect 한다.   
  목록 버튼을 누를 시 상세보기 화면으로 돌아간다.   
  
  **5. 게시글 삭제 화면**   
  ![image](https://user-images.githubusercontent.com/59757689/156976055-d6e8f6bd-9bda-4fc8-bb5f-3ea60d9f2f5d.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156976074-c27f90c8-c8e0-45b9-9d04-e3541a14b8c2.png)   
  Confirm으로 삭제할지 확인하고, 삭제 후 전체 목록 리스트 화면으로 redirect 한다.   
  
  **6. 게시글 검색 화면**   
  ![image](https://user-images.githubusercontent.com/59757689/156976190-1dac1678-3cf4-4d21-9f3b-d5228b7d50ef.png)   
  검색 키워드에 포함된 글을 모두 보여준다.   
     
  **6-1. 게시글 검색 후 페이징 화면**   
  ![image](https://user-images.githubusercontent.com/59757689/156976258-c4b28ef3-fd6e-4ebe-834c-d5c6bce4c02c.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156976314-c6733cb8-7aac-4502-88d4-02730f88021b.png)   
  검색된 게시글이 많을 경우 다음과 같이 페이징 처리되어 조회할 수 있다.   
     
  </details>
  <br/>   
  
  <details>
    <summary>회원 관련</summary>   
     
  **1. 회원가입 화면**   
  ![image](https://user-images.githubusercontent.com/59757689/156976413-78b9e0e9-2ab1-47e0-a0cd-699ebacddb79.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156976436-fafec47f-3df3-4356-83d5-eb80e1aa2276.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156976548-3a440a6c-49d0-4e5c-9eb3-d5e3524c11b6.png)   
  회원가입 시 유효성 검사 및 중복확인을 진행하며 완료시 회원 정보를 저장하고 로그인 화면으로 이동한다.   
     
  **2. 로그인 화면**   
  ![image](https://user-images.githubusercontent.com/59757689/156976619-6988837d-0dfe-4600-a63c-2e287db9c88e.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156976909-51b0d06c-502f-4e42-b0dd-516834e43efe.png)   
  로그인 실패시 어떤 이유로 실패 했는지 메시지가 나오고, 로그인에 성공하면 게시글 전체 리스트 화면으로 redirect 한다.   
     
  **2-1. OAuth 2.0 소셜 로그인 화면**   
  ![image](https://user-images.githubusercontent.com/59757689/156976991-c517d254-b4b8-4a34-99fd-2684856f2a2d.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156977007-7b44d157-f29c-4a43-9fd3-aa6b743a8fb8.png)   
  구글과 네이버 로그인이 가능하다.   
     
  **3. 회원정보 수정 화면**   
  ![image](https://user-images.githubusercontent.com/59757689/156977253-d1a4de93-da30-4adf-8634-dfe10d0635a8.png)   
  닉네임과 비밀번호만 변경할 수 있고, 변경된 닉네임이 이미 사용중일 경우 alert으로 현재 사용 중임을 알려주고,   
  완료시 게시글 전체 리스트 화면으로 redirect 한다.      
           
  </details>
  <br/>   
  
  <details>
    <summary>댓글 관련</summary>   
       
  **1. 댓글 작성 화면**   
  미로그인 사용자 화면   
  ![image](https://user-images.githubusercontent.com/59757689/156977476-37db357a-ac44-4b24-ad8c-a062d4fe99cf.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156977497-cc7fc2a7-e688-4733-b4c7-8aef4fba93e3.png)   
  댓글은 로그인 한 사용자만 달 수 있으며, 댓글 작성시 현재 페이지를 reload 한다.   
  
  **2. 댓글 수정**   
  ![image](https://user-images.githubusercontent.com/59757689/156977557-8a3dae77-9a8d-4fd3-824e-8ff22606609e.png)   
  다른 사용자는 다른 사람의 댓글을 수정/삭제할 수 없다.   
  ![image](https://user-images.githubusercontent.com/59757689/156977567-fd983777-5b04-4f57-a815-c89a59697377.png)   
  수정은 댓글 작성자만이 할 수 있다. 수정 완료 후 현재 페이지를 reload 한다.   
  
  **3. 댓글 삭제**   
  ![image](https://user-images.githubusercontent.com/59757689/156977655-8125a317-344e-4721-a836-46b36df3a3b5.png)   
  ![image](https://user-images.githubusercontent.com/59757689/156977661-5008733b-2932-4bfc-be01-60a33a093dc9.png)   
  삭제 또한 댓글 작성자만이 할 수 있다. 삭제 후 현재 페이지를 reload 한다.   
           
  </details>
  <br/>   
 
   
## 구조 및 설계   
   
### 1. 패키지 구조
   
<details>
  
<summary>패키지 구조 보기</summary>   
 

```
📦src
 ┣ 📂main
 ┃ ┣ 📂java
 ┃ ┃ ┗ 📂com
 ┃ ┃ ┃ ┗ 📂coco
 ┃ ┃ ┃ ┃ ┗ 📂board
 ┃ ┃ ┃ ┃ ┃ ┣ 📂application
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂dto
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostsDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UserDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂security
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂auth
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CustomAuthFailureHandler.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CustomUserDetails.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CustomUserDetailsService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜LoginUser.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜LoginUserArgumentResolver.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂oauth
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CustomOAuth2UserService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜OAuthAttributes.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂validator
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜AbstractValidator.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CustomValidators.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostsService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UserService.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂domain
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜BaseTimeEntity.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜Comment.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜Posts.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜Role.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜User.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂infrastructure
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂config
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜SecurityConfig.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜WebConfig.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂persistence
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostsRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UserRepository.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂presentation
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentApiController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostsApiController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostsIndexController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserApiController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UserController.java
 ┃ ┃ ┃ ┃ ┃ ┗ 📜BoardApplication.java
 ┃ ┗ 📂resources
 ┃ ┃ ┣ 📂static
 ┃ ┃ ┃ ┣ 📂css
 ┃ ┃ ┃ ┃ ┗ 📜app.css
 ┃ ┃ ┃ ┣ 📂img
 ┃ ┃ ┃ ┃ ┗ 📜naver.ico
 ┃ ┃ ┃ ┗ 📂js
 ┃ ┃ ┃ ┃ ┗ 📜app.js
 ┃ ┃ ┣ 📂templates
 ┃ ┃ ┃ ┣ 📂comment
 ┃ ┃ ┃ ┃ ┣ 📜form.mustache
 ┃ ┃ ┃ ┃ ┗ 📜list.mustache
 ┃ ┃ ┃ ┣ 📂layout
 ┃ ┃ ┃ ┃ ┣ 📜footer.mustache
 ┃ ┃ ┃ ┃ ┗ 📜header.mustache
 ┃ ┃ ┃ ┣ 📂posts
 ┃ ┃ ┃ ┃ ┣ 📜posts-page.mustache
 ┃ ┃ ┃ ┃ ┣ 📜posts-read.mustache
 ┃ ┃ ┃ ┃ ┣ 📜posts-search.mustache
 ┃ ┃ ┃ ┃ ┣ 📜posts-update.mustache
 ┃ ┃ ┃ ┃ ┗ 📜posts-write.mustache
 ┃ ┃ ┃ ┣ 📂user
 ┃ ┃ ┃ ┃ ┣ 📜user-join.mustache
 ┃ ┃ ┃ ┃ ┣ 📜user-login.mustache
 ┃ ┃ ┃ ┃ ┗ 📜user-modify.mustache
 ┃ ┃ ┃ ┗ 📜index.mustache
 ┃ ┃ ┣ 📜application-oauth.properties
 ┃ ┃ ┗ 📜application.properties
 ┗ 📂test
 ┃ ┗ 📂java
 ┃ ┃ ┗ 📂com
 ┃ ┃ ┃ ┗ 📂coco
 ┃ ┃ ┃ ┃ ┗ 📂board
 ┃ ┃ ┃ ┃ ┃ ┣ 📂controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜PostsApiControllerTest.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂domain
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentRepositoryTest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostsRepositoryTest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UserRepositoryTest.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂infrastructure
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂config
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜SecurityConfigTest.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂service
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜PostsServiceTest.java
 ┃ ┃ ┃ ┃ ┃ ┗ 📜BoardApplicationTests.java
 ```
  
 </details>   
 <br/>    
   
     
 ### 2. DB 설계

![erd 3차 2022-01-03](https://user-images.githubusercontent.com/59757689/148910882-2ac9ec57-c339-4bef-a6d5-13025a8d9ac9.PNG)   
![posts 테이블 db 설계](https://user-images.githubusercontent.com/59757689/148910938-c6a99c8e-fefc-467b-a2af-a68a00e01a11.PNG)   
![user 테이블 db 설계](https://user-images.githubusercontent.com/59757689/149279956-b0a184da-9b19-4bcf-9ce8-6c001ef81f1d.PNG) 
![comment 테이블 db 설계](https://user-images.githubusercontent.com/59757689/148910946-02280553-97ce-4d82-bbda-9c911ea89bd4.PNG)   
created_date와 modified_date는 날짜 포맷을 적용해주기 위해 datetime > varchar로 변경했습니다.   
   
<br/>

### 3. API 설계

![게시글 관련 API 설계](https://user-images.githubusercontent.com/59757689/156749365-5e4cee67-1431-4e3a-9140-7b58b6e1fd53.PNG)    
![회원 관련 API 설계 (2)](https://user-images.githubusercontent.com/59757689/148911411-0cfb65ee-5782-4f04-a7c9-7dcc84abfed8.PNG)   
![댓글 관련 API 설계v2](https://github.com/hojunnnnn/board/assets/59757689/fa9032f0-3ce1-4ec4-9dbd-f420fb4e6152)  

## 마치며   
### 1. 프로젝트 보완사항   

<details>
  <summary>보완사항</summary>
     
- 페이징 처리 및 검색 페이징에서 페이지 번호 활성화
- 페이지 번호는 10페이지 단위로 보여주기
- 페이지 처음, 끝으로 이동하는 버튼
- 생성, 수정시간 format 설정 varchar > datetime
- 다른 사용자와 자신의 댓글이 댓글란에 있을때 자신의 댓글만 수정,삭제 버튼 보이기
  
</details>   

추후에 브랜치를 나눠 Mustache에서 Thymeleaf로 조금씩 바꾸며 프로젝트 완성도를 높이고, 고도화 할 계획에 있습니다.   
   
   <details>
  <summary>추가할 기능 </summary>
     
- 댓글 페이징 처리
- 쿠키나 세션을 이용해 조회수 중복 카운트 방지
- 파일 업로드 기능 추가
- 좋아요 기능 추가
  
</details>  
