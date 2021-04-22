# TIL-Today-I-Learned-
오늘 무얼 했는지 기록하는 공간

Since 2021.04.22

## 2021년 4월 22일

### 인공지능

- 머신러닝에 대해 정리 (머신러닝은 인공지능을 실현하는 기법으로 분류, 딥러닝, 확률, 유전 등 종류가 다양하다.)
- 딥러닝에 대해 정리 (딥러닝은 인간의 뇌를 모방한 심층 신경망 기법을 통해서 결과를 만들어 내는 것이다. 매우 유연하고 확장성 있는 모델을 구성할 수 있다.)

### 네트워크

- 프로토콜, OSI 7 계층 모델, 데이터 단위, DNS 개념
  - 프로토콜은 데이터를 교환할 때 따르는 통신 규격이다.
  - OSI 7 계층 - 물리, 데이터 링크, 네트워크, 전송, 세션, 표현, 응용 계층 순
  - 데이터 단위 - 데이터 링크(프레임), 네트워크(패킷), 전송(TCP - 세그먼트 / UDP - 데이터그램)
    - OSI 계층마다 다르다.
  - DNS란 주소와 이름 정보를 자동으로 유지하고 관리하는 분산 데이터베이스 시스템
    - 숫자로 된 IP 주소는 기억하기 힘드므로 의미 파악이 쉬운 문자로 된 호스트 이름을 사용하는 것이 일반적임.

- OSI 7계층 모델의 각 계층에서도 목적에 따라 여러 형태의 주소가 사용됨.
  - MAC 주소: 데이터링크 계층에서 사용. 네트워크 계층에서 테이터 링크 계층으로 데이터를 전송할 때는 IP 주소를 MAC 주소로 변환해야 한다.
  - IP 주소: 네트워크 계층의 기능을 수행하는 IP 프로토콜에서 사용. IP 패킷이 지나가는 경로를 결정하는 라우팅의 기준.
  - 포트 주소: 전송 계층에서 사용. TCP와 UDP가 독립적으로 관리
  - 메일 주소: 응용 계층의 메일 시스템에서 사용자를 구분하려고 사용

### 알고리즘

#### 브루트 포스

- BOJ 10972번 다음 순열
- BOJ 10973번 이전 순열
- BOJ 10819번 차이를 최대로

#### 백트래킹

- BOJ 10971번 외판원 순회 2



