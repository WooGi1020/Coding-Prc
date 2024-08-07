### HTTP 요청 메소드

---

🔖HTTP는 원하는 행동을 수행하는 각각의 메소드를 가지고 있다. (HTTP 동사라고 부르기도 함)

```
1. GET
- 특정 리소스의 조회를 요청한다. 데이터 조회만 가능하다.
- 멱등성의 개념을 가지고 여러번 조회 요청을 해도 변함이 없다.
- 쿼리스트링을 통해 서버에 데이터를 전달하지만 무방비 상태로 노출되어 주의가 필요하다.
```

```
2. POST
- 새로운 리소스의 생성을 요청한다.
- 데이터를 메세지 바디에 파라미터 형식으로 전달한다. (key, value 형식)
- 멱등성이 보장되지 않아 여러번 요청하면 동일하지 않은 결과값이 나올 수 있다.
```

```
3. PUT
- 리소스를 덮어쓰기 형식으로 대체한다.
- 클라이언트가 리소스를 식별할 수 있어 URI를 지정한다.
- 멱등성을 지니며 부분적인 수정이 불가능하다.
```

```
4. PATCH
- 리소스를 부분적으로 변경한다.
- 요청한 데이터와 서버의 데이터의 비교가 가능하며 부분적인 대체가 가능하다.
- 멱등성을 지니지 않으며, 지원하지 않는 서버에선 POST를 사용한다.
```

```
5. DELETE
- 데이터를 제거한다.
- 멱등성을 지닌다.
```

```
6. HEAD
- GET과 마찬가지로 데이터의 조회를 요청한다.
- body 부분을 제외하고 상태줄과 헤더만 반환한다. (일종의 검사 용도)
- 대용량 파일 등의 정보를 간단하고 빠르게 받아오는 것에 용이하며, 리소스의 수정 등의 확인이 가능하다.
```
