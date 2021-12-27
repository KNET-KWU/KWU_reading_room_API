# KWU_reading_room_API

API 문서는 완성 후 작성 예정입니다.

---

광운대학교 중앙도서관 오픈열람실 API 입니다

![api structure](./assets/img/api-structure-1.png)

구조는 위와 같이 API 백엔드에서 오픈열람실 HTML을 광운대학교 도서관 사이트에서 가져온 뒤 파싱하여 데이터를 지속적으로 저장하는 형태를 갖추고 있습니다.

1분마다 갱신되는 열람실 정보를 1분 주기로 Amazon EventBridge가 HTML을 가져와서 파싱하는 람다함수를 작동시켜 좌석 번호 데이터를 DynamoDB에 저장합니다.

엔드 유저가 API를 호출할 때 직접 광운대 도서관 홈페이지가 아닌 DynamoDB로부터 데이터를 반환합니다.

---

API 개발 블로그 :

[KWU 도서관 오픈열람실 API 만들기 - 1](https://ccppoo.github.io/2021/12/26/KWU-%EC%98%A4%ED%94%88%EC%97%B4%EB%9E%8C%EC%8B%A4-API-%EB%A7%8C%EB%93%A4%EA%B8%B0-1.html)