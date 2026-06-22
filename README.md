# 📋 JSP 게시판 웹 사이트

> Bootstrap을 활용한 JSP 기반 게시판 웹 사이트

<br>

## 👨‍💻 개발자
| 이름 | GitHub |
|------|--------|
| kddong991121 | [@kddong991121](https://github.com/kddong991121) |

<br>

## 📌 프로젝트 소개
Bootstrap과 JSP를 활용하여 제작한 게시판 웹 사이트입니다.
회원가입, 로그인, 게시글 작성/수정/삭제 등 게시판의 핵심 기능을 구현하였습니다.

<br>

## ⚙️ 사용 기술
| 분류 | 기술 |
|------|------|
| Frontend | HTML, CSS, Bootstrap |
| Backend | Java, JSP, Servlet |
| Database | MySQL |
| Server | Apache Tomcat 9.0 |
| IDE | Eclipse |

<br>

## 🔧 주요 기능

### 👤 회원 관리
- 회원가입 (아이디 중복 확인, 비밀번호 확인)
- 로그인 / 로그아웃
- 세션 기반 로그인 유지
- 비밀번호 보기/숨기기 토글 기능

### 📝 게시판
- 게시글 목록 조회 (페이징 처리)
- 게시글 작성
- 게시글 상세보기
- 게시글 수정 (작성자 본인만 가능)
- 게시글 삭제 (작성자 본인만 가능)
- XSS 공격 방지

<br>

## 🗂️ 프로젝트 구조
```
JSPBook
├── src/main/java
│   ├── bbs
│   │   ├── Bbs.java
│   │   └── BbsDAO.java
│   └── user
│       ├── User.java
│       └── UserDAO.java
└── src/main/webapp
    ├── css/
    ├── js/
    ├── images/
    ├── index.jsp
    ├── main.jsp
    ├── bbs.jsp
    ├── view.jsp
    ├── write.jsp
    ├── writeAction.jsp
    ├── update.jsp
    ├── updateAction.jsp
    ├── deleteAction.jsp
    ├── login.jsp
    ├── loginAction.jsp
    ├── join.jsp
    ├── joinAction.jsp
    └── logoutAction.jsp
```

<br>

## 🗄️ DB 테이블 구조

### user 테이블
| 컬럼 | 타입 | 설명 |
|------|------|------|
| userID | VARCHAR(20) | 아이디 (PK) |
| userPassword | VARCHAR(20) | 비밀번호 |
| userName | VARCHAR(20) | 이름 |
| userGender | VARCHAR(10) | 성별 |
| userEmail | VARCHAR(20) | 이메일 |

### bbs 테이블
| 컬럼 | 타입 | 설명 |
|------|------|------|
| bbsID | INT | 게시글 번호 (PK) |
| bbsTitle | VARCHAR(50) | 제목 |
| userID | VARCHAR(20) | 작성자 |
| bbsDate | DATETIME | 작성일 |
| bbsContent | VARCHAR(2048) | 내용 |
| bbsAvailable | INT | 게시글 상태 (1: 정상) |

<br>

## 🚀 실행 방법

1. MySQL에서 데이터베이스 및 테이블 생성
2. `UserDAO.java`, `BbsDAO.java`에서 DB 접속 정보 설정
```java
String dbURL = "jdbc:mysql://localhost:3306/bbs";
String dbID = "root";
String dbPassword = "본인 비밀번호";
```
3. Eclipse에서 Tomcat 서버 실행
4. 브라우저에서 접속
```
http://localhost:8080/JSPBook/main.jsp
```
## 📚 참고 자료
- [나동빈 JSP 게시판 웹 사이트 만들기](https://www.youtube.com/watch?v=wEIBDHfoMBg&list=PLRx0vPvlEmdAZv_okJzox5wj2gG_fNh_6)

## 🎯 프로젝트 목적
- 코딩 감각 회복 및 JSP 기초 복습
- Bootstrap을 활용한 웹 개발 실습
- Java, JSP, MySQL 연동 복습