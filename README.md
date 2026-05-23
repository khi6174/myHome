# myHome

STS 기반 Spring MVC 웹 애플리케이션 프로젝트입니다.  
회원 관리, 상품 조회, 장바구니, 주문, 게시판, 공지사항, 이미지 게시판 기능을 포함한 쇼핑몰 형태의 웹 프로젝트입니다.

## 프로젝트 소개

myHome은 Spring MVC 구조를 기반으로 제작한 웹 애플리케이션입니다.  
사용자는 회원가입 및 로그인을 통해 상품을 조회하고 장바구니에 담을 수 있으며, 게시글 작성, 공지사항 확인, 이미지 게시판 이용 등의 기능을 사용할 수 있습니다.

관리자는 회원 조회, 상품 등록, 공지사항 작성, 배송 상태 변경 등 운영 관리 기능을 수행할 수 있습니다.

## 주요 기능

### 사용자 기능

- 회원가입
- 로그인 / 로그아웃
- 마이페이지
- 상품 목록 조회
- 상품 상세 조회
- 장바구니 추가
- 장바구니 수량 수정 및 삭제
- 주문 및 결제 흐름 처리
- 게시글 조회 및 작성
- 공지사항 조회
- 이미지 게시판 조회 및 작성
- 댓글형 이미지 게시판 기능

### 관리자 기능

- 가입자 조회
- 상품 등록
- 상품 원산지 등록
- 배송 상태 변경
- 공지사항 작성
- 상품 관리
- 주문 내역 및 판매 내역 확인

## 기술 스택

### Backend

- Java 1.8
- Spring MVC
- MyBatis
- JDBC
- Oracle DB
- Maven

### Frontend

- JSP
- JSTL
- HTML
- CSS
- JavaScript

### Server / Build

- Apache Tomcat
- Maven WAR Packaging
- STS / Eclipse 기반 개발 환경

## 프로젝트 구조

```bash
myHome
└── myHome
    ├── src
    │   └── main
    │       ├── java
    │       │   ├── controller
    │       │   ├── dao
    │       │   ├── logic
    │       │   ├── mapper
    │       │   ├── model
    │       │   ├── utils
    │       │   └── mybatisConfig.xml
    │       │
    │       └── webapp
    │           ├── home
    │           ├── imgs
    │           ├── WEB-INF
    │           │   ├── view
    │           │   ├── mvc-config.xml
    │           │   └── web.xml
    │           └── index.jsp
    │
    └── pom.xml
