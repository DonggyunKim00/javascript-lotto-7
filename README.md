# javascript-lotto-precourse

### 🔥 학습 목표

- **공통**
  - 관련 함수를 묶어 클래스를 만들고, 객체들이 협력하여 하나의 큰 기능을 수행하도록 한다.
  - 클래스와 함수에 대한 단위 테스트를 통해 의도한 대로 정확하게 작동하는 영역을 확보한다.
  - 2주 차 공통 피드백을 최대한 반영한다.
    - README.md 를 상세히 작성하기
    - 기능 목록을 재검토 하기
    - 살아있는 기능 명세서를 만들기
    - 값을 하드코딩 하지 않기
    - 메서드가 한가지 일만 하도록 하기
    - 테스트를 작성하는 이유에 대해 생각하기
    - 처음부터 큰 단위의 테스트를 만들지말고, 작은단위의 테스트를 만들기
- **개인**
  - 변수, 메서드 네이밍 신경쓰기
  - 고민이 생기면 미루지 말고 기록하기
    - 상황 → 고민 → 해결 순으로 기록하기
  - 디자인 패턴 공부하기
    - 퍼사드 패턴

---

### ✅ 요구 사항 체크리스트

- [ ] Git의 커밋 단위를 기능명세서에 정리한 기능 목록 단위로 추가하였는가?
- [ ] Airbnb 코드 컨벤션을 지켰는가?
- [ ] indent depth 3을 넘지 않았는가?
- [ ] 3항 연산자를 쓰지 않았는가?
- [ ] 함수(메서드)가 한 가지 일만 하도록 최대한 작게 만들었는가?
- [ ] Jest를 사용하여 정리한 기능 목록이 정상적으로 작동하는지 테스트 하였는가?
- [ ] 함수(메서드)의 길이가 15라인을 넘어가지 않았는가?
- [ ] else를 지양 하였는가?
- [ ] 구현한 기능에 대해서 단위 테스트를 작성하였는가? (UI 로직 제외)
- [ ] Lotto 클래스를 사용하여 구현하였는가?
- [ ] Lotto에 numbers 이외의 필드(인스턴스 변수)를 추가하지 않았는가?
- [ ] numbers의 접근 제어자인 #을 변경하지 않았는가?

---

### 🎯 기능 명세서

- [x] 사용자에게 구입 금액을 입력 받을 수 있다.
  - [x] 입력이 공백이라면 `[ERROR]`
  - [x] 입력이 숫자가 아니라면 `[ERROR]`
  - [x] 로또 금액으로 나누어 떨어지지 않으면 `[ERROR]`
  - [x] 예외 발생 시 에러 메시지 출력 후, 해당 위치부터 다시 입력 받을 수 있다.
- [x] 로또를 구입할 수 있다.
  - [x] 로또 1장의 가격은 1,000원이다.
  - [x] 구입 개수 만큼 로또를 발행할 수 있다.
  - [x] 로또 번호의 숫자 범위는 1~45까지이다.
  - [x] 1개의 로또를 발행할 때 중복되지 않는 6개의 숫자를 뽑는다.
  - [x] 로또 생성 시 구성된 번호가 6개가 아니면 `[ERROR]`
  - [x] 로또 생성 시 구성된 번호가 중복이면 `[ERROR]`
  - [x] 로또 생성 시 숫자로만 구성되지 않았다면 `[ERROR]`
  - [x] 로또의 각 번호들이 1~45 사이의 숫자가 아니라면 `[ERROR]`
  - [x] 로또의 각 번호들이 정수가 아니라면 `[ERROR]`
  - [x] 로또의 각 번호에 숫자만 들어가있지 않다면 `[ERROR]`
- [x] 발행된 로또를 출력할 수 있다.
  - [x] 발행한 로또 수량을 `8개를 구매했습니다.` 형식으로 출력한다.
  - [x] N개의 로또를 `[8, 21, 23, 41, 42, 43]` 형식으로 출력한다. (오름차순 정렬)
- [ ] 사용자에게 당첨 번호를 입력 받을 수 있다.
  - [ ] 번호는 쉼표(,)를 기준으로 구분한다.
  - [ ] 구분된 번호가 숫자가 아니라면 `[ERROR]`
  - [ ] 구분된 번호가 1~45 사이의 숫자가 아니라면 `[ERROR]`
  - [ ] 구분된 번호중 중복된 숫자가 있다면 `[ERROR]`
  - [ ] 예외 발생 시 에러 메시지 출력 후, 해당 위치부터 다시 입력 받을 수 있다.
- [ ] 사용자에게 보너스 번호를 입력 받을 수 있다.
  - [ ] 입력이 숫자가 아니라면 `[ERROR]`
  - [ ] 입력이 1~45 사이의 숫자가 아니라면 `[ERROR]`
  - [ ] 입력이 당첨 번호와 중복된다면 `[ERROR]`
  - [ ] 예외 발생 시 에러 메시지 출력 후, 해당 위치부터 다시 입력 받을 수 있다.
- [ ] 발행된 로또와 당첨 번호를 비교할 수 있다.
  ```
  1등: 6개 번호 일치 / 2,000,000,000원
  2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
  3등: 5개 번호 일치 / 1,500,000원
  4등: 4개 번호 일치 / 50,000원
  5등: 3개 번호 일치 / 5,000원
  ```
- [ ] 당첨 내역을 출력할 수 있다.
  ```
  3개 일치 (5,000원) - 1개
  4개 일치 (50,000원) - 0개
  5개 일치 (1,500,000원) - 0개
  5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
  6개 일치 (2,000,000,000원) - 0개
  ```
- [ ] 수익률을 계산할 수 있다.
  - [ ] 수익률은 (수익률) / (구입금액) \* 100 으로 계산한다.
  - [ ] `총 수익률은 (수익률)%입니다.` 형식으로 출력한다.
