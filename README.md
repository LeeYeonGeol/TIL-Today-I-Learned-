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

## 2021년 4월 23일

### 인공지능

- 퍼셉트론: 퍼셉트론은 가장 단순한 형태의 신경망
  - 예측 값과 실제 값의 최소가 되는 weight 값을 찾는 과정이 퍼셉트론을 학습하는 과정이다.
  - 예측 값과 실제 값의 차이를 줄일 수 있도록 weight 값을 변경하는 방법이 경사하강법이다.

- 회귀 개요: 회귀는 여러 개의 독립변수와 한 개의 종속변수 간의 상관관계를 모델링하는 기법
  - RSS: 오류 값의 제곱을 구해서 더하는 방식, RSS를 최소로 하는 W(회귀 계수)를 찾는 것이 목표
  - MSE: RSS를 학습 데이터의 건수로 나눈 것이며 비용 함수, 손실함수가 된다.
- 경사 하강법: '점진적으로' 반복적인 계산을 통해 W 파라미터 값을 업데이트하면서 오류 값이 최소가 되는 W 파라미터를 구하는 방식
  - 예측값과 실제값의 차이가 작아지는 방향성을 가지고 W 파라미터를 보정한다.
  - 오류 값이 더 이상 커지지 않으면 그 오류 값을 최소 비용으로 판단하고 그때의 W 값을 최적 파라미터로 반환한다.
  - 이 과정에서 편미분을 사용하고 Update는 기존 W값에 손실 함수 편미분 값을 감소시키는 방식을 적용하되 편미분 값을 그냥 감소 시키지 않고 일정한 계수를 곱해서 감소 시키며, 이를 **학습률**이라고 한다.
  - 기본적으로 $w_{new} = w_{old} + 이동 거리 * 부호$가 된다.
    - 기울기가 양수인 경우 음의 방향으로 움직여야 최소가 나오고 음수인 경우는 양의 방향으로 움직여야 최소가 나오기 때문에 **부호는 기울기의 부호**가 된다.
    - 한편, 최솟값에 가까울 수록 조심히 움직여야 발산하지 않는데, 최솟값에 가까워질 수록 기울기의 크기는 작아지므로 **기울기를 이동거리로 사용한다.**

### 데이터 분석

- 넘파이 개요
  - shape, ndim, dtype으로 형태, 차원, 타입을 구할 수 있다.
  - axis = 0은 행 방향, axis = 1은 열 방향
  - ndarray 초기화 방법들
    - np.arange(10)
    - np.zeros((3, 2), dtype='int32')
    - np.ones((3, 2))
  - ndarray 차원과 크기 변경: reshape() 
  - 인덱싱, 슬라이싱, 팬시 인덱싱, 불링 인덱싱
  - sort(), argsort()
  - 행렬 내적: np.dot(A, B) / 전치 행렬: np.transpose(A)

### 알고리즘

- 비트마스크 개요