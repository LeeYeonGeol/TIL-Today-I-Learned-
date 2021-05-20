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

## 2021년 4월 24일

### 네트워크

- 모듈화: 오류발생시 오류가 발생한 모듈만 교체하면 된다. 대부분의 모듈 구조에서는 계층 구조를 이룬다.
- 프로토콜 설계 시 고려 사항
  - 주소 표현: 시스템을 구분하여 지칭하기 위해서 이름을 부여
    - 브로드캐스팅: 네트워크에 연결된 모든 호스트에 데이터 전송가능
    - 멀티태스킹: 특정 사용자를 그룹으로 묶어서 지칭
  - 오류 제어
    - 데이터 변형 오류: 데이터가 깨져서 도착
    - 데이터 분실 오류: 데이터가 도착하지 못함
    - 오류 해결 방법: 재전송
  - 흐름 제어: 송신 호스트의 전송 속도를 조정
- OSI 7계층 모델
  - 물리 계층: 전송 매체의 물리적 인터페이스에 관한 사항 기술
  - 데이터 링크 계층: 물리 계층을 통해 전송되는 데이터의 물리적 전송 오류를 해결
  - 네트워크 계층: 어떤 경로를 통해 수신 호스트에 전달되는지를 결정하는 라우팅 문제 처리
  - 전송 계층: 컴퓨터 내부에서 논리적으로 구축되는 통신 당사자인 프로세스 사이의 문제 처리
  - 세션 계층: 전송 계층과 유사하지만 상위적 연결 개념인 세션 기능 제공
  - 표현 계층: 데이터의 의미와 표현 방법 처리
  - 응용 계층: 다양하게 존재하는 응용 환경에서 공통으로 필요한 기능을 다룬다.

## 2021년 4월 25일

### 데이터 분석

- pandas 개요
  - Series와 DataFrame 차이
    - Series는 1개의 Column값으로만 구성된 1차원 데이터셋
    - DataFrame은 Column X Rows로 구성된 2차원 데이터셋
    - 시리즈는 Column명이 없다.
  - 기본 API
    - read_csv, head 등
    - DataFrame에서 Series, DataFrame 추출 방법
    - shape, info, describe 등을 통해 정보를 얻을 수 있다.
    - value_counts() - 데이터값의 분포 확인
    - sort_values - 정렬
  - 데이터 삭제
    - drop() 활용
  - loc, iloc를 통한 인덱싱
  - Aggregation 함수 와 Group By
  - 결손 데이터 처리하기
    - isna()
    - fillna()
  - apply 함수에 lambda식을 결합해서 데이터 가공하기

### 알고리즘

#### 비트마스크

- BOJ 11723번 집합

## 2021년 4월 26일

### 딥러닝

- 경사하강법을 이용하여 선형회귀 구현 (sklearn 보스턴 집값 예측)

- 확률적 경사하강법과 미니배치 경사하강법
  - Keras의 경우 미니배치 경사하강법을 사용. 배치크기 32가 디폴트.

## 2021년 4월 27일

### 딥러닝

- 역전파 알고리즘의 등장 배경
  - 심층신경망에서는 많은 은닉층이 있고 경사하강법으로 가중치를 일일이 업데이트하는데 제한이 생긴다.
  - 따라서 출력층에서 역순으로 미분의 연쇄법칙(Chain Rule)을 활용하여 Gradient를 전달하여 전체 Layer의 가중치를 업데이트할 수 있다.

### 알고리즘

#### 브루트포스

- BOJ 14391번 종이 조각 

#### 다이나믹 프로그래밍

- 개요 복습
  - 큰 문제를 작은 문제로 나눠서 푸는 알고리즘
  - Overlapping Subproblem (겹치는 작은 문제)
  - Optimal Substructure (최적 부분 구조)

- 파이썬 알고리즘 문제풀이 / 섹션 8 / 4. 최대 부분 증가수열 

## 2021년 4월 28일

### 알고리즘

#### 다이나믹 프로그래밍

- 개요 복습
  - 모든 문제를 풀어야 함
  - 모든 문제는 1번만 풀어야 함
  - 시간복잡도 = 문제의 개수 x 문제 1개를 푸는 시간
  - 2가지 방식
    - Top-down (재귀)
    - Bottom-up (반복문)
  - 문제풀이 방식
    - 점화식
    - 문제를 작게 만들 수 있는 방법 찾기

#### 문제 풀이

- 프로그래머스 / 로또의 최고 순위와 최저 순위

##### 다이나믹 프로그래밍

- BOJ 1463번 1로 만들기

### 딥러닝

- 활성화 함수
  - 목적: 딥러닝 네트워크에 비선형성을 적용하기 위함
  - Sigmoid: 은닉층에서는 그래디언트 소실 문제로 사용 X. 이진 분류 최종 아웃풋에서 사용
  - Hyperbolic Tangent: Tanh는 시그모이드와 달리 -1과 1사이의 값을 출력하여 평균이 0이 될 수 있지만 여전히 그래디언트 소실 문제.
  - ReLU: 대표적인 은닉층의 활성함수
  - 소프트맥스 함수: Multi Classification의 최종 활성화 함수로 사용

- 손실 함수
  - Cross Entropy vs Squared Error
    - Squared Error의 2가지 문제점: 일반적인 잘못된 예측에 대해서 CE보다 높은 비율의 페널티, 아주 잘못된 예측에 대해서는 CE보다 낮은 비율의 페널티 부과
- 옵티마이저
  - 역할: 보다 최적으로 GD를 적용, 최소 Loss로 보다 빠르고 안정적으로 수렴할 수 있는 기법 적용
  - Momentum: 가중치 Update 수행 시마다 이전의 Gradient들의 값을 일정 수준 반영 시키면서 신규 가중치로 Update 적용. (지그재그 형태의 Update 개선)
  - Adagrad (Adaptive Gradient): 가중치 별로 서로 다른 Learning Rate를 동적으로 적용한다. 처음에는 큰 Learning Rate가 적용되지만 최저점에 가까울 수록 Learning Rate가 작아진다. 하지만 iteration이 커질 때 Learning Rate가 아주 작게 변환되는 문제 발생.
  - RMSProp: Adagrad의 문제를 해결하기 위해 지수 가중 평균법을 사용. (오랜 과거의 Gradient값의 영향을 줄일 수 있도록 한다.)
  - Adam: RMSProp과 같이 개별 Weight에 서로 다른 Learning Rate를 적용함과 동시에 Gradient에 Momentum 효과를 부여

## 2021년 4월 29일

### 딥러닝

- Dense Layer를 활용한 Fashion MNIST 연습
- Keras Callback
  - ModelCheckpoint
  - ReduceLROnPlateau
  - EarlyStopping

## 2021년 4월 30일

### 딥러닝

- CNN 알고리즘
  - 합성곱 연산
  - 스트라이드, 패딩, 풀링
    - 요즘은 풀링을 안하는 추세
  - Fashion_MNIST 연습
  - Dropout 활용(오버피팅 방지)
- KNN 알고리즘 연습 (붓꽃 데이터, 유방암 데이터 등)

### 알고리즘

#### 다이나믹 프로그래밍

- BOJ 1463번 1로 만들기

## 2021년 5월 1일

### 코딩테스트

- 라인 채용연계형 코딩테스트 (2시간, 3문제)

### 머신러닝

- 선형 모델
  - LinearRegression
  - Ridge
  - Lasso

## 2021년 5월 2일

### CNN 알고리즘

- CNN 알고리즘 과정 이해
- CIFAR10 데이터세트를 활용한 구현 연습

## 2021년 5월 3일

### 알고리즘

#### 다이나믹 프로그래밍

- BOJ 11726번 2xn 타일링
- BOJ 11727번 2xn 타일링 2

- BOJ 1, 2, 3 더하기

### CNN 알고리즘

- 배치 정규화
  - 아웃풋의 분포가 밀리는 현상 방지
- 가중치 초기화 
  - 입력 노드와 출력노드 수 등을 감안하여 초기화
- Global Average Pooling
  - 피처맵의 채널별로 평균 값을 추출
- 가중치 규제
  - 가중치 값이 지나치게 학습데이터에만 정교화되는 현상을 방지하기 위함.

- 데이터 증강

## 2021년 5월 4일

### CNN 알고리즘

- CIFAR10 데이터셋에 Augmentation 적용

## 2021년 5월 5일

### 알고리즘

#### DFS

- BOJ 13023번 ABCDE

## 2021년 5월 6일

### CNN 알고리즘

- 사전 훈련 모델 활용하여 CIFAR10 학습 모델 구현 연습
  - VGG16
  - Xception
- 개와 고양이 분류 연습

※ 아픈 관계로 당분간은 쉬엄쉬엄 해야될듯 함.

## 2021년 5월 7일

### CNN 알고리즘

- Keras Generator 기반의 전처리 및 데이터 로딩 

## 2021년 5월 8일

### 코딩테스트

- 카카오 인턴쉽

## 2021년 5월 9일

### 코딩테스트

- 프로그래머스 서머인턴 

## 2021년 5월 10일

### CNN 알고리즘

- Albumentation 여러가지 기능 

## 2021년 5월 11일

### 알고리즘

- BOJ 11052번 카드 구매하기
- BOJ 16194번 카드 구매하기 2

### CNN 알고리즘

- Keras의 Sequence기반의 Dataset 활용하여 이미지 분류 연습

## 2021년 5월 12일

### CNN 알고리즘

#### CNN 모델 공부

- AlexNet
- VGGNet

## 2021년 5월 12일

### CNN 알고리즘

#### CNN 모델 공부

- GoogLeNet(Inception)

## 2021년 5월 14일

### CNN 알고리즘

#### CNN 모델 공부

- ResNet

## 2021년 5월 15일

- 카카오 인턴 설명회

## 2021년 5월 16일

### CNN 알고리즘

- 감정 분류 모델 

### 기타

- 카카오 자소서

## 2021년 5월 17일

### 기타

- 카카오 자소서 (반나절 이상 걸림)

### 머신 러닝

- 피처 엔지니어링

## 2021년 5월 20일

### CNN 알고리즘

- EfficientNet
- Pretrained 모델의 Fine Tuning