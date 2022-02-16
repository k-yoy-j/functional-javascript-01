# ES6
## 정리
- 이터러블/이터레이터 프로토콜   
. 이터러블: 이터레이터를 리턴하는 [Symbol.iterator]() 를 가진 값   
. 이터레이터: {value,done} 객체를 리턴하는 next()를 가진 값   
. 이터러블/이터레이터 프로토콜: 이터러블을 for...of, 전개 연산자 등과 함께 동작하도록한 규약   
* for .. of   
for (const a of arr) log(a);   
iterator 개념으로 순회
* map   
const map = new Map(['a,', 1], ['b', 2]);   
for (const a of map.keys()) log(a);   
map.values(), map.entries()
* 전개연산자   
log([...a, ...arr]);   
const [head, a, ...tail] = odds(5);   
log(head); log(a); log(tail);   
* 제너레이터   
: 이터레이터이자 이터러블을 생성하는 함수   
function *gen(){   
   yield 1;   
   yield 2;   
   return 100; (done true 일때 사용)   
}   
let iter = gen();   
iter.next();   
for (const a of gen())   

## 강의 목록
1. 함수형 자바스크립트 기본기
    1. 평가와 일급
    2. 일급 함수
    3. 고차 함수
    4. 부수효과와 순수 함수
2. ES6에서의 순회와 이터러블/이터레이터 프로토콜
    1. 기존과 달라진 ES6에서의 리스트 순회
    2. Array, Set, Map을 통해 알아보는 이터러블/이터레이터 프로토콜
    3. 사용자 정의 이터러블
    4. 전개 연산자
3. 제너레이터와 이터레이터
    1. 제너레이터와 이터레이터
    2. odds
    3. for...of, 전개 연산자, 구조 분해, 나머지 연산자
4. map, filter, reduce
    1. map
    2. 이터러블 프로토콜을 따른 map의 다형성 1
    3. 이터러블 프로토콜을 따른 map의 다형성 2
    4. filter
    5. reduce
    6. reduce 2
    7. map+filter+reduce 중첩 사용과 함수형 사고
5. 코드를 값으로 다루어 표현력 높이기
    1. go
    2. pipe
    3. go를 사용하여 읽기 좋은 코드로 만들기
    4. go+curry를 사용하여 더 읽기 좋은 코드로 만들기
    5. 함수 조합으로 함수 만들기
6. 장바구니 예제
    1. 총 수량, 총 가격
    2. HTML로 출력하기
7. 지연성 1
    1. range와 느긋한 L.range
    2. range와 느긋한 L.range 테스트
    3. take
    4. 제너레이터/이터레이터 프로토콜로 구현하는 지연 평가
    5. L.map
    6. L. filter
    7. range, map, filter, take, reduce 중첩 사용
    8. L.range, L.map, L.filter, take 의 평가 순서
    9. 엄격한 계산과 느긋한 계산의 효율성 비교
    10. map, filter 계열 함수들이 가지는 결합 법칙
    11. ES6의 기본 규악을 통해 구현하는 지연 평가의 장점
8. 지연성 2
    1. 결과를 만드는 함수 reduce, take
    2. queryStr 함수 만들기
    3. Array.prototype.join 보다 다형성이 높은 join 함수
    4. take, find
    5. L.map, L.filter로 map과 filter 만들기
    6. L.flatten, flatten
    7. L.flatMap, flatMap
    8. 2차원 배열 다루기
    9. 지연성 / 이터러블 중심 프로그래밍 실무적인 코드
9. 비동기/동시성 프로그래밍 1
    1. callback과 Promise
    2. 비동기를 값으로 만드는 Promise
    3. 값으로서의 Promise 활용
    4. 합성 관점에서의 Promise와 모나드
    5. Kleisli Composition 관점에서의 Promise
    6. go, pipe, reduce에서 비동기 제어
    7. promise.then의 중요한 규칙
10. 비동기/동시성 프로그래밍 2
    1. 지연 평가 + Promise - L.map, map, take
    2. Kleisli Composition - L.filter, filter, nop, take
    3. reduce에서 nop 지원
    4. 지연 평가 + Promise의 효율성
    5. 지연된 함수열을 병렬적으로 평가하기 - C.reduce, C.take 1
    6. 지연된 함수열을 병렬적으로 평가하기 - C.reduce, C.take 2
    7. 즉시 병렬적으로 평가하기 - C.map, C.filter
    8. 즉시, 지연, Promise, 병렬적 조합하기
    9. 코드 간단히 정리
    10. Node.js에서 SQL 병렬 평가로 얻은 효율
11. 비동기/동시성 프로그래밍 3
    1. async/await
    2. Q&A) Array.prototype.map이 있는데 왜 FxJS의 map 함수가 필요한지?
    3. Q&A) 이제 비동기는 async/await로 제어할 수 있는데 왜 파이프라인이 필요한지?
    4. Q&A) async/await와 파이프라인을 같이 사용하기도 하는지?
    5. Q&A) 동기 상황에서 에러 핸들링은 어떻게 해야하는지?
    6. Q&A) 비동기 상황에서 에러 핸들링은 어떻게 해야하는지?
    7. Q&A) 동기/비동기 에러 핸들링에서의 파이프라인의 이점은?
