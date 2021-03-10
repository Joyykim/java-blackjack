# java-blackjack
블랙잭 게임 미션 저장소

# 🚀 블랙잭 1단계
## 기능 요구사항
- 블랙잭 게임을 변형한 프로그램을 구현한다. 블랙잭 게임은 딜러와 플레이어 중 카드의 합이 21 또는 21에 가장 가까운 숫자를 가지는 쪽이 이기는 게임이다.
- 플레이어는 게임을 시작할 때 배팅 금액을 정해야 한다. 카드의 숫자 계산은 카드 숫자를 기본으로 하며, 예외로 Ace는 1 또는 11로 계산할 수 있으며, King, Queen, Jack은 각각 10으로 계산한다.
- 게임을 시작하면 플레이어는 두 장의 카드를 지급 받으며, 두 장의 카드 숫자를 합쳐 21을 초과하지 않으면서 21에 가깝게 만들면 이긴다. 21을 넘지 않을 경우 원한다면 얼마든지 카드를 계속 뽑을 수 있다. 단, 카드를 추가로 뽑아 21을 초과할 경우 배팅 금액을 모두 잃게 된다.
- 딜러는 처음에 받은 2장의 합계가 16이하이면 반드시 1장의 카드를 추가로 받아야 하고, 17점 이상이면 추가로 받을 수 없다.
- 게임을 완료한 후 각 플레이어별로 승패를 출력한다.

### 기본 룰
- 카드 클래스 정의
  - [x] 카드 한장은 수트와 숫자로 이루어짐
  - [x] 하나의 덱은 1 부터 10, J, Q, K의 값을 가진 카드들을 가짐
  - [x] 10, J, Q, K는 숫자 10으로 취급
- [x] 카드 덱은 모든 Suit, Rank 조합의 카드들을 가진다

### 플레이어
- [x] 이름을 가짐
  - [x] 이름의 길이는 1~5자
- [x] 카드 패를 가짐
- [x] 시작하면 카드 두 장을 받는다
- [x] 자신의 턴 동안 원하는 만큼 카드를 계속 뽑을 수 있다
- [x] 카드의 합이 21 이상이 되면 더 이상 뽑을 수 없다

### 딜러
- [x] 이름을 가짐
  - [x] 이름의 길이는 1~5자
- [x] 카드 패를 가짐
- [x] 시작하면 카드 두 장을 받고 한 장만 공개한다
- [x] 모든 플레이어의 턴이 끝나고 딜러의 턴이 진행된다
- [x] 딜러는 패의 합계가 16 이하면 계속해서 뽑는다
- [x] 플레이어와 딜러에게 카드를 전달

### 승패
- [x] 21을 초과하지 않으면서 21에 가까운 플레이어가 이김
- 카드 합을 계산하여 승패를 정한다
  - [x] 21을 넘으면 버스트, 패배
  - [x] 딜러의 합산한 수보다 낮은 플레이어는 패배
  - [x] 딜러와 합산한 수가 같다면 무승부
  - 딜러가 버스트되었다면
    - [x] 버스트한 플레이어를 제외하고 모두 승리
- [x] 게임을 완료한 후 각 플레이어별로 승패를 출력한다.

### 입력
- [x] 참가할 플레이어들의 이름을 `,` 단위로 나눠서 입력
- [x] 각 플레이어의 턴 - 카드 한 장을 더 받을지 말지 `y`(예), `n`(아니오)를 입력

## 출력 예시
```
게임에 참여할 사람의 이름을 입력하세요.(쉼표 기준으로 분리)
pobi,jason

딜러와 pobi, jason에게 2장의 카드를 나누었습니다.
딜러 카드: 3다이아몬드
pobi 카드: 2하트, 8스페이드
jason 카드: 7클로버, K스페이드

pobi는 한장의 카드를 더 받겠습니까?(예는 y, 아니오는 n)
y
pobi 카드: 2하트, 8스페이드, A클로버
pobi는 한장의 카드를 더 받겠습니까?(예는 y, 아니오는 n)
n
jason은 한장의 카드를 더 받겠습니까?(예는 y, 아니오는 n)
n
jason 카드: 7클로버, K스페이드

딜러는 16이하라 한장의 카드를 더 받았습니다.

딜러 카드: 3다이아몬드, 9클로버, 8다이아몬드 - 결과: 20
pobi 카드: 2하트, 8스페이드, A클로버 - 결과: 21
jason 카드: 7클로버, K스페이드 - 결과: 17

## 최종 승패
딜러: 1승 1패
pobi: 승 
jason: 패
```
## 프로그래밍 요구사항
딜러와 플레이어에서 발생하는 중복 코드를 제거해야 한다.

## 우아한테크코스 코드리뷰
* [온라인 코드 리뷰 과정](https://github.com/woowacourse/woowacourse-docs/blob/master/maincourse/README.md)