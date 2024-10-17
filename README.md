# java-calculator-precourse

## 기능 요구사항
입력한 문자열에서 숫자를 추출하여 더하는 계산기를 구현한다.

쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환한다. <br>
예: "" => 0, "1,2" => 3, "1,2,3" => 6, "1,2:3" => 6 <br>
앞의 기본 구분자(쉼표, 콜론) 외에 커스텀 구분자를 지정할 수 있다. <br>
커스텀 구분자는 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다. <br>

예를 들어 `"//;\n1;2;3"`과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 `6`이 반환되어야 한다. <br>
사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`을 발생시킨 후 애플리케이션은 종료되어야 한다.

- 입력 : 구분자와 양수로 구성된 문자열 <br>
- 출력 : 덧셈 결과

### 라이브러리 <br>
`camp.nextstep.edu.missionutils`에서 제공하는 Console API를 사용하여 구현해야 한다. <br>
사용자가 입력하는 값은 `camp.nextstep.edu.missionutils.Console`의 `readLine()`을 활용한다.
## 기능 목록

- [x] 문자열 입력받기
  - [x] 입력 클래스 분리  
  - [x] 문자열 입력 문구 출력 
  - [x] 라이브러리를 이용한 문자열 입력
- [x] 문자열 쉼표 및 세미콜론, 커스텀 구분자로 나누기
  - [x] 문자열 분석 클래스 분리
  - [x] 구분자 분리
    - [x] 커스텀 구분자 분리
    - [x] 입력값에서 쉼표 및 세미콜론 또는 커스텀 구분자만 사용되었는지 검증
  - [x] 구분 인덱스 enum으로 관리
  - [x] 커스텀 구분자 구문 삭제 로직 구현
  - [x] 구분자를 이용하여 문자열을 숫자만 있는 배열로 추출
- [ ] 숫자 덧셈
  - [x] 계산 클래스 분리
  - [ ] 구분자를 비교하여 숫자 덧셈 구현
- [ ] 예외 처리
  - [ ] 예외 클래스 분리
- [ ] 결과 반환