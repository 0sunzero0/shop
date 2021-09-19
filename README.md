# shop
## API 설계하기
- 주문하기(POST): 정보 입력 후 '주문하기' 버튼클릭 시 주문목록에 추가
  - **A. 요청 정보**
   - 요청 URL= `/order` , 요청 방식 = `POST`
   - 요청 데이터 : 주문자 이름(name), 수량(order_num), 주소(address), 연락처(phone_num)
  - **B. 서버가 제공할 기능**
    - 클라이언트에게 보낸 요청 데이터를 데이터베이스에 생성하고, 저장이 성공했다고 응답 데이터를 보냄
  - **C. 응답 데이터**
    - (JSON 형식) 'result'= 'success',  'msg'= '주문이 성공적으로 완료되었습니다.
- 주문내역보기(GET): 페이지 로딩 후 하단 주문 목록이 자동으로 보이기
  - **A. 요청 정보**
    - 요청 URL= `/order` , 요청 방식 = `GET`
    - 요청 데이터 : 없음
  - **B. 서버가 제공할 기능**
    - DB에 주문 정보를 읽고, 성공메세지와 주문 정보를 응답 데이터에 보냄.
  - **C. 응답 데이터**
    - (JSON 형식) 'result'= 'success',  'orders'= 주문리스트
