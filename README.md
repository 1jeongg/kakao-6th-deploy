## 6주차 과제 - 카카오 클라우드 배포

### 과제 설명

```
1. 통합테스트를 구현하시오.
2. API문서를 구현하시오. (swagger, restdoc, word로 직접 작성, 공책에 적어서 제출 등 모든 방법이 다 가능합니다)
3. 프론트앤드에 입장을 생각해본뒤 어떤 문서를 가장 원할지 생각해본뒤 API문서를 작성하시오.
4. 카카오 클라우드에 배포하시오.
```

## Todo-List

---

- [x] 5주차 과제 옮기기(장바구니 관련 예외처리, 주문하기)
- [x] 통합테스트(성공, 실패) 구현
  - [x] user - 로그인, 로그아웃, 이메일 중복 체크
  - [x] cart - 장바구니 추가하기, 조회하기, 업데이트하기
  - [x] order - 결제하기, 주문결과 확인하기
  - [x] product - 전체 상품 조회, 개별 상품 상세 조회
- [x] API 문서 구현
- [x] 카카오 클라우드에 배포

## 통합테스트 구현 상세

---

### User

- 회원가입
  - 성공
  - 실패 - 중복된 이메일, 잘못된 형식의 패스워드, 잘못된 형식의 이메일, 길이가 잘못된 사용자이름, 길이가 잘못된 패스워드
- 로그인
  - 성공
  - 실패 - 존재하지 않는 사용자, 잘못된 형식의 패스워드, 잘못된 형식의 이메일, 길이가 잘못된 패스워드

---

### Product

- 전체 상품 조회 (성공)
- 개별 상품 조회 (성공)
---

### Cart

- 추가하기
  - 성공 - 이미 존재하는 장바구니일 경우 업데이트, 아닌 경우 추가
  - 실패 - 중복된 장바구니, 수량이 0개, 비어있는 요청리스트, 존재하지 않는 optionId
- 조회하기
  - 성공
- 업데이트하기
  - 성공
  - 실패 - 중복된 장바구니, 수량이 0개, 존재하지 않는 cartId, 비어있는 요청리스트

---

### Order

- 결제하기
  - 성공
  - 실패 - 장바구니가 비어있을 경우
- 주문 결과 확인하기
  - 성공
  - 실패 - 잘못된 orderId일 경우

---
