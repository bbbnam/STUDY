## HTTP 메서드 활용
### 클라이언트에서 서버로 데이터 전송

- 데이터 전달 방식 크게 2가지
> - 쿼리 파라미터를 통한 데이터 전송 : GET
> - 메시지 바디를 통한 데이터 전송 : POST, PUT, PATCH

- 4가지 경우
> - 정적 데이터 조회 (GET)
> - 동적 데이터 조회 (GET)
> - HTML Form을 통한 데이터 전송 (POST, GET)
> - HTTP API를 통한 데이터 전송 (GET, POST, PUT, PATCH)

### HTTP API 설계 예시
#### - HTTP API - 컬렉션
- POST 기반 등록 - `클라이언트가 리소스 URI를 모른다.`
> - 회원목록 /members -> GET
> - 회원등록 /members -> POST
> - 회원조회 /members/{id} -> GET
> - 회원수정 /members/{id} -> PATCH, PUT, POST (우선순위 순)
> - 회원삭제 /members/{id} -> DELETE

#### - HTTP API - 스토어
- PUT 기반 등록 - `클라이언트가 리소스 URI를 알고 있다.`
> - 파일목록 /files -> GET
> - 파일조회 /files/{filename} -> GET
> - 파일등록 /files/{filename} -> PUT (기존 것 지우고 대체)
> - 파일삭제 /files/{filename} -> DELETE
> - 파일 대량 등록 /files -> POST

#### - HTML Form 사용
- GET, POST만 지원
- GET, POST만 쓰기에 제약이 있음 -> 컨트롤 URI 사용으로 극복
- POST로 쓰되 URI에 /new(등록) /edit(수정) /delete(삭제) 를 나타내줌
* 참고 : `컨트롤 URI는 동사로 써줌`

#### 참고하면 좋은 URI 설계 개념
- https://restfulapi.net/resource-naming 참고