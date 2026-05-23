# myHome

STS 기반 Spring MVC 웹 애플리케이션 프로젝트입니다.  
회원 관리, 상품 조회, 장바구니, 주문, 게시판, 공지사항, 이미지 게시판 기능을 포함한 쇼핑몰 형태의 웹 프로젝트입니다.

## 프로젝트 소개

myHome은 Spring MVC 구조를 기반으로 제작한 웹 애플리케이션입니다.  
사용자는 회원가입 및 로그인을 통해 상품을 조회하고 장바구니에 상품을 담을 수 있으며, 주문 기능과 게시판 기능을 이용할 수 있습니다.

관리자는 회원 조회, 상품 등록, 상품 관리, 공지사항 작성, 주문 및 배송 상태 관리 등 쇼핑몰 운영에 필요한 관리 기능을 수행할 수 있습니다.

이 프로젝트는 MVC 패턴을 기반으로 Controller, DAO, Model, Mapper 구조를 분리하여 구현했으며, JSP 화면과 MyBatis 기반 데이터베이스 연동을 통해 웹 서비스의 전체 흐름을 학습하고 구현하는 것을 목표로 했습니다.

## 주요 기능

### 사용자 기능

- 회원가입
- 로그인 / 로그아웃
- 마이페이지
- 상품 목록 조회
- 상품 상세 조회
- 장바구니 담기
- 장바구니 목록 조회
- 주문 및 결제 흐름 처리
- 주문 내역 확인
- 게시글 조회 및 작성
- 공지사항 조회
- 이미지 게시판 조회 및 작성

### 관리자 기능

- 회원 목록 조회
- 회원 상세 정보 확인
- 상품 등록
- 상품 정보 관리
- 상품 원산지 정보 등록
- 주문 목록 조회
- 배송 상태 변경
- 매출 내역 확인
- 공지사항 작성 및 관리

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

### Server / Tool

- Apache Tomcat
- STS / Eclipse
- Maven WAR Packaging

## 프로젝트 구조

```bash
myHome
└── myHome
    ├── src
    │   └── main
    │       ├── java
    │       │   ├── admin
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
    │           └── index.jsp
    │
    └── pom.xml
```

## 주요 기능 상세

### 1. 회원 기능

사용자는 회원가입을 통해 계정을 생성할 수 있으며, 로그인 후 마이페이지와 장바구니, 주문 기능을 이용할 수 있습니다.  
세션을 활용하여 로그인 상태를 유지하고 사용자별 기능을 구분합니다.

### 2. 상품 기능

상품 목록과 상세 정보를 조회할 수 있습니다.  
관리자는 상품을 등록하고 상품 정보를 관리할 수 있으며, 상품의 원산지 정보도 함께 관리할 수 있습니다.

### 3. 장바구니 기능

로그인한 사용자는 원하는 상품을 장바구니에 담을 수 있습니다.  
장바구니 화면에서 담긴 상품을 확인하고 주문 단계로 이동할 수 있습니다.

### 4. 주문 및 배송 관리

사용자는 장바구니에 담긴 상품을 기반으로 주문을 진행할 수 있습니다.  
관리자는 전체 주문 목록과 배송 상태를 확인하고 수정할 수 있습니다.

### 5. 게시판 기능

일반 게시판을 통해 게시글을 작성하고 조회할 수 있습니다.  
사용자 간 정보 공유를 위한 기본 게시판 기능을 구현했습니다.

### 6. 공지사항 기능

관리자는 공지사항을 작성하고 관리할 수 있습니다.  
사용자는 등록된 공지사항을 조회할 수 있습니다.

### 7. 이미지 게시판 기능

이미지 게시글 작성, 목록 조회, 상세 조회, 수정, 삭제 기능을 제공합니다.  
파일 업로드 기능을 통해 이미지가 포함된 게시글을 관리할 수 있습니다.

## 주요 Controller

| Controller | 설명 |
|---|---|
| HomeController | 메인 화면 이동 처리 |
| LoginController | 로그인 처리 |
| LogoutController | 로그아웃 처리 |
| EntryController | 회원가입 처리 |
| MypageController | 마이페이지 처리 |
| ItemController | 상품 조회 및 관리 |
| CartController | 장바구니 처리 |
| CheckoutController | 주문 및 결제 처리 |
| EndController | 주문 완료 처리 |
| AdminController | 관리자 기능 처리 |
| NoticeController | 공지사항 처리 |
| WriteController | 게시판 처리 |
| ImageController | 이미지 게시판 처리 |
| NationController | 상품 원산지 관리 |
| BeerController | 상품 카테고리 관련 처리 |

## 주요 Model

| Model | 설명 |
|---|---|
| User | 사용자 정보 |
| LoginUser | 로그인 사용자 정보 |
| Item | 상품 정보 |
| Cart | 장바구니 정보 |
| CartItem | 장바구니 상품 정보 |
| Sale | 주문 정보 |
| SaleDetail | 주문 상세 정보 |
| Board | 게시판 정보 |
| Notice | 공지사항 정보 |
| Imagebbs | 이미지 게시판 정보 |
| Nation | 원산지 정보 |

## 실행 방법

### 1. 저장소 클론

```bash
git clone https://github.com/khi6174/myHome.git
```

### 2. STS 또는 Eclipse에서 프로젝트 Import

1. STS 또는 Eclipse 실행
2. `File` → `Import`
3. `Existing Maven Projects` 선택
4. `myHome/myHome` 폴더 선택
5. Maven 프로젝트로 Import

### 3. Maven 업데이트

프로젝트 우클릭 후 아래 메뉴를 실행합니다.

```bash
Maven > Update Project
```

### 4. DB 설정

Oracle DB 사용을 기준으로 구성되어 있으므로 실행 전 DB 연결 정보를 본인 환경에 맞게 수정해야 합니다.

확인 대상 예시:

```bash
src/main/java/mybatisConfig.xml
src/main/webapp/WEB-INF/
```

### 5. Tomcat 서버 실행

1. Tomcat 서버 등록
2. 프로젝트를 서버에 추가
3. 서버 실행
4. 브라우저 접속

```bash
http://localhost:8080/myHome/
```

## 구현 포인트

- Spring MVC 기반 웹 애플리케이션 구조 구현
- Controller, DAO, Model, Mapper 역할 분리
- MyBatis를 활용한 SQL Mapper 방식의 데이터베이스 연동
- JSP와 JSTL을 활용한 동적 화면 구성
- 세션 기반 로그인 처리
- 사용자와 관리자 기능 분리
- 장바구니, 주문, 게시판, 공지사항 등 쇼핑몰 핵심 기능 구현
- 이미지 게시판을 통한 파일 업로드 기능 구현

## 개발 환경

| 항목 | 내용 |
|---|---|
| IDE | STS / Eclipse |
| Language | Java 1.8 |
| Framework | Spring MVC |
| View | JSP, JSTL |
| Database | Oracle DB |
| Persistence | MyBatis, JDBC |
| Build Tool | Maven |
| Server | Apache Tomcat |
| Packaging | WAR |

## 프로젝트를 통해 배운 점

- Spring MVC의 전체 요청 처리 흐름을 이해하고 구현했습니다.
- Controller, DAO, Model, Mapper를 분리하여 MVC 패턴 기반의 구조를 학습했습니다.
- MyBatis를 활용하여 SQL과 Java 객체를 연결하는 방식을 익혔습니다.
- JSP와 JSTL을 활용하여 서버 사이드 렌더링 기반 화면을 구성했습니다.
- 로그인, 장바구니, 주문, 게시판 등 웹 서비스에서 자주 사용되는 핵심 기능을 직접 구현했습니다.
- 관리자 기능을 분리하여 사용자 기능과 운영자 기능의 차이를 이해했습니다.

## 향후 개선 방향

- Spring Boot 기반 프로젝트로 마이그레이션
- 비밀번호 암호화 적용
- DB 접속 정보 외부 설정 파일 분리
- 관리자 / 사용자 권한 관리 강화
- 입력값 검증 및 예외 처리 보완
- UI 디자인 개선
- REST API 구조 도입
- 프로젝트 실행 화면 이미지 추가

## 작성자

김용우
