<div align="center">
    <h1> VISIT US </h1>
</div>

![배너](https://github.com/Access-projcet/.github/blob/main/banner.png)

<br>
<br>

## 👩‍👧‍👧 프로젝트 소개
<br>

- **VISIT US 는 어떠한 서비스 인가요?**
    - 저희 서비스는 QR코드 출입과 간편한 방문예약, 출입관리와 보안까지 아우르는
    회사 출입방문 시스템 VISIT US 입니다.

- **VISIT US 의 핵심기능은 뭔가요?**
    - QR 코드로 편리하게 출입이 가능합니다.
    - 간편하게 방문 예약을 할 수 있습니다.
    - 관리자페이지에서 출입내역을 효율적으로 관리할 수 있습니다.

##### 👉🏻 [프론트 바로가기](https://github.com/Access-projcet/FrontEnd)
##### 👉🏻 [백엔드 바로가기](https://github.com/Access-projcet/BackEnd)
<br>

---

## 📒 개발기간

### 2023.03.10 ~ 2023.04.13
<br>

---

<h2>🏡팀원 소개</h2>

|이름|github |역할|
|------|---|---|
|이승렬|https://github.com/LEESEUNGRYEOL|BackEnd(팀장)|
|조민성|https://github.com/Ganpyeon|BackEnd|
|김진원|https://github.com/skwwnl|BackEnd|
|첨기범|https://github.com/Gnar-dev|FrontEnd(부팀장)|
|이신행|https://github.com/akfangus|FrontEnd|
|전찬열|https://github.com/chanyeol123|FrontEnd|
|한송이||Designer|


#### 1. 방문 시간이 DB에 잘못된 값으로 저장되는 오류

| 요구 사항 | 사유 및 근거 |
| -------- | ----------- |
| 문제 상황 | 방문 신청을 하였을때 방문 시간을 입력하면 post요청으로 DB에 저장을 할때 입력한 시간에서 +9시간이 추가 되는 오류가 발생 |
| 원인 | 방문 시간을 작성해서 요청을 보낼때 서버의 시간을 거쳐서 DB에 저장을 하다보니 현재 시간에서 9시간이 추가되는 상황 |
| 시도 | 1. 서버끼리의 시간은 동일할거라 생각하여 백엔드, 프론트엔드 둘다 서버를 올려서 확인 해보았지만 실패. </br> 2. Docker에 타임존을 추가하여 Docker자체에 시간을 한국 표준시로 지정 |
| 해결 방법 | Docker에 타임존을 추가하여 Docker의 시간을 한국 표준시로 지정하여 데이터가 정확히 들어오는걸 확인 및 해결 </br> Fix → /etc/localtime:/etc/localtime:ro -e TZ=Asiz/Seoul |
