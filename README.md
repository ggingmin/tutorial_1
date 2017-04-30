# Rails와 CRUD

이 소스 코드는 CRUD를 활용한 간단한 게시판 제작을 다루고 있습니다.

## CRUD란?
- Create(생성)
- Read(열람)
- Update(변경)
- Delete(삭제)

## HTTP 와 라우팅
| URL             | 액션    | HTTP 메소드 | 역할                      |
|-----------------|---------|-------------|---------------------------|
| /posts          | index   | GET         | 목록 페이지               |
| /posts/:id      | show    | GET         | 개별 콘텐츠 페이지        |
| /posts/new      | new     | GET         | 새로운 콘텐츠 입력 페이지 |
| /posts          | create  | POST        | 입력 받은 콘텐츠 등록     |
| /posts/:id/edit | edit    | GET         | 기존의 콘텐츠 수정 페이지 |
| /posts/:id      | update  | PATCH       | 수정한 콘텐츠 내용 등록   |
| /posts/:id      | destroy | DELETE      | 선택한 콘텐츠 제거        |
