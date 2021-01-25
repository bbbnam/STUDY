## HTTP 기본
### 모든 것이 HTTP
- HTTP 메시지에 모든 것을 전송
- 이미지, 텍스트, 영상, 파일, json/xml 등

### 기반 프로토콜
> - TCP : HTTP/1.1, HTTP/2
> - UDP : HTTP/3

### 클라이언트 서버 구조
- Request <-> Response 구조

### 무상태 프로토콜(Stateless)
- 서버가 client 의 상태를 보존하지 않음
- 스케일아웃 유리 (수평확장)
- 한계 : 상태 유지가 필요한 경우(로그인) - 쿠키, 세션 활용
- 상태 유지는 최소한만 사용해야 함

### 비 연결성(connectionless)
- 서버 연결 유지 x -> 최소한의 자원 사용
- 한계 : TCP/IP 연결을 새로 맺어야 함 -> 3way handshake 시간 추가

### HTTP 메시지
- 위에서부터 시작라인, 헤더, 공백라인(CRLF), message body 로 구성
- HTTP 메서드 
> - GET  : 리소스 조회
> - POST : 요청 내역 처리
- HTTP 상태코드
> - 200 : 성공
> - 400 : 클라이언트 요청 오류
> - 500 : 서버 내부 오류


