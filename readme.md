# 게시판 작성
## mysql DB 사용
## pom.xml 변경 및 추가(API)
  - java 버전 1.6 -> 1.8
  - springframework-version 3.1.1.RELEASE -> 4.3.8.RELEASE 
  - groudId : mysql, org.apache.commons 추가

## servlet-context.xml 
 - mysql DB 연동 정보 추가

## src/main/java - board package 생성
 - Board.java
  -> 순수한 데이터 java 파일 (게시판 DB 정보 : getter, setter)
 - BoardDAO.java
  -> DataBase 의 data에 접근하기 위한 java 파일
 - BoardController.java
  -> board의 controller 를 사용할 java 파일

## views 안에 board 폴더 생성
 - boardInfo.jsp
  -> 게시글 클릭시 나타날 화면
 - boardList.jsp
  -> 게시글 전체 리스트 화면
 - boardWriteForm.jsp
  -> 게시글 글쓰기 클릭시 화면
 - reWriteForm.jsp
  -> 댓글 입력 화면
 - board_mysql.sql
  -> Table 생성할 SQL문 쿼리문 파일

## 1. 오류 및 조치내용
 - 오류 : java.sql.SQLSyntaxErrorException: Table 'com.board' doesn't exist 에러 발생
 - 원인 : DB table 생성을 안해서 오류 발생
 - 해결방안 : DB table 생성

## 2. 오류 및 조치내용
 - 오류 : DB 한글깨짐 발생
 - 원인 : 한글인코딩 설정 안해줌(이클립스 UTF-8 설정만 완료)
 - 해결방안 :  Spring 한글인코딩 설정

## 작업시 오류 내용 정리
## 용어정리(각 API의 기능 추가중)
## 진행시 이해 안되는 용어 정리
