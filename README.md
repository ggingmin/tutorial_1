# Rails와 CRUD

이 소스 코드는 CRUD를 활용한 간단한 게시판 제작을 다루고 있습니다.

## CRUD란?
- Create(생성)
- Read(열람)
- Update(변경)
- Delete(삭제)

## HTTP 메소드와 라우팅
| URL             | 액션    | HTTP 메소드 | 역할                      |
|-----------------|---------|-------------|---------------------------|
| /posts          | index   | GET         | 목록 페이지               |
| /posts/:id      | show    | GET         | 개별 콘텐츠 페이지        |
| /posts/new      | new     | GET         | 새로운 콘텐츠 입력 페이지 |
| /posts          | create  | POST        | 입력 받은 콘텐츠 등록     |
| /posts/:id/edit | edit    | GET         | 기존의 콘텐츠 수정 페이지 |
| /posts/:id      | update  | PATCH       | 수정한 콘텐츠 내용 등록   |
| /posts/:id      | destroy | DELETE      | 선택한 콘텐츠 제거        |
  
- GET(추출)
- POST(생성)
- PATCH(변경)
- DELETE(제거)
  
Q. 굳이 `method: :delete`, `method: :patch` 코드를 추가한 이유는?
  
A. 내부적으로는 HTTP POST로 접근하지만 추가로 'DELETE'나 'PATCH'를 언급함으로써 이 기능을 사용할 수 있게된다.
  
그 이유는 웹 브라우저 호환성 때문.
  
구 버전의 웹 브라우저는 DELETE/PATCH 등을 지원하지 않아서 일단은 POST로 접근해야 한다.
