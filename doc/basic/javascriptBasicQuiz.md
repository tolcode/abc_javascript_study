# javascript basic quiz

- What are the five primitive values in JavaScript? (There are six if you consider ES6).
```
자바스크립트의 기본값 5가지
(Boolean, Null, Undefined, Number, String) + ES6를 고려한다고 하면 Symbol
```

- How do you declare and assign variables in JavaScript?
```
* 변수 선언
[var 변수명;]

* 변수 할당
[변수명= 데이터;]
```

- What’s the difference between const, let and var?
```
● const, let은 ES6 문법
● var, let은 변수를 선언하는 키워드이고 const는 상수를 선언하는 키워드 이다.
● var, let은 변수선언 키워드 이므로 리터럴 값의 재할당 가능하지만, const는 리터럴 값의 재할당이 불가능하다. 그러므로 더욱더 const 키워드는 선언과 동시에 리터럴 값을 할당해 줘야 함

* let
변수의 재선언을 막아주고 호이스팅 되지 않으므로, 변수 사용전에 반드시 먼저 선언 해야한다.

* const
let 키워드와 유사하나, 상수선언용 이기때문에 리터럴 값을 재할당하는것이 불가능하므로 선언과 동시에 값 할당을 해야한다
사용하는이유는 const 식별자로 선언된 배열이나 객체 같은경우, 일종의 객체 타입이라는 자료형을 유지하기 위한 수단으로 사용 된다.

출처 - https://blog.hanumoka.net/2018/09/21/javascript-20180921-javascript-var-let-const/

```

- How do you use the following conditionals?
  - if
  - if else
  - else
  ```
  1. if 문 
  => 조건식이 참이면 실행되는 형태
  if(expression) {
  조건이 참이면 실행
  }
  
  2. if... else 문
  => 모든 조건을 실행할수 있는 문법, 조건에서 참이든 거짓이든 하나를 실행함
  if (expression){
  조건이 참이면 실행
  } else {
  조건이 거짓이면 실행
  }
  
  3. if..else..if.. 문
  =>조건문을 여러개 중복해서 넣을수 있는 문법, 경우의 수를 여러개 만들어 조건들에서 맞지 않는다면 마지막 else 영역이 실행됨
  ```
  
- How do you use a for loop?
```
* while 반복문
while(조건) {
반복
}


* do while 반복문
do {
// 우선 실행
} while (조건) // 조건이 맞으면다 시반복



* for 반복문
var array = ['수박', '딸기', '바나나'];

for (var i=0; i <array.length; i++) { //배열 크기까지 반복후
alert(array[i]); //출력
}

```

```
ES6 - for문

* For-in
=> 객체의 속성 또는 배열의 요소에 대해 반복하는 기능 수행. 즉, 객체의 속성들을 순회하기 위한 구문이다.
=> 단점1. 인덱스가 문자로반환,
   단점2 : 루프구문이 요솓르만 순회하는것이 아니라 프로토타입 체인도 순회
   단점3 : 루프 순회 순서가 무작외

* For-of
=> 반복가능한 객체(Array, Map, Type Array, arguments 객체 등)을 반복하는 기능 수행 즉 객체의 요소들(Data)를 순회하기 위한 구문
=> 장점1 : 배열 순회를 지우너하는 문법 중에서 가장 간결하고 직접적으로 접근 가능
   장점2 : for-in 구문의 단점을 보완
   장점3 : forEach문에서 지워하지 않는 break, continue, return 구문 사용 가능
   

ex 배열)

let list = ['사과', '딸기', '배'];

for(let i in list) {
  console.log(i); //결과 : "0", "1", "2"
}

for(let i of list) {
  console.log(i); //결과 : "사과", "딸기", "배"
}



ex 객체)

let objhome = {
color = "orange",
width = "5",
heith = "1.7"
}

for(let i in objhome) {
  console.log(i); //결과 : "color", "width", "heith"
}

for(let i of objhome) {
  console.log(i); //결과 : "orange", "5", "1.7"
}


```


- What is an array?
  - How do you put values into arrays?
  ```
  배열 참고 출처 : https://kssong.tistory.com/26
  
  1. 직접할당 (인덱스를 지정하여 할당)
  2. push()메서드 사용
  3. unshift()메서드 사용 (배열의 맨앞에 원소를 추가하여 기존 운솓르의 인덱스 값이 1씩 커짐)
  ```
  - How to you get values out of arrays?
  ```
  1. 배열의 각 원소에 접근시 [] 연산자를 사용
  2. 사용자가 명시한 숫자 배열 인덱스를 문자열 형태로 바꿔서 속성 이름으로 사용
  ```
  - How do you remove a value from an array?
  ```
  1. delete는 배열의 길이가 변경되지 않으며 값만 삭제함
  2. length 속성 이용 -> 배열의 끝에서부터 원소 삭제가능
  3. pop() 메서드 사용 -> 배열의 length를 하나 줄이고 삭제된 값을 반환
  4. shift() 메서드 사용 -> 배열의 맨앞 원소를 삭제, 모둔 우너소의 인덱스 값을 하나씩 감소
  5. splice() 메서드는 추가, 삭제, 대치하는 범용 메서드
  ```
  - How do you loop through every value of an array?
  ```
  for문을 사용하여 순회시키는데, 사용전 null, undifined, 빈원소가 있는지 확인하고 제외시켜줘야 함
  ```
  
  
  
  
  
- What is an object?
  ```js
  <sciprt>
    var product = {
      제품명: '건조 딸기',
      성분: '딸기',
      원산지: '대한민국
      };
  </sciprt>
  ```
  - How do you put values into objects?
  ```
  객체.속성명 = 속성값
  ```

  - How do you get values out from objects?
  ```
  *첫번째 방법
  product['제품명']
  product['성분']
  prodduct['원산지']
  
  * 두번재방법
  product.제품명
  product.성분
  product.원산지
  ```
  - How do you remove a property from an object?
  ```
  delete(속성명)
  ```
  - How do you loop through every value of an object?
  ```
  for (변수 in 객체) {
  구문
  }
  
  
  ex)
  for (let props in product) {
    console.log("name :" + props + " value : " + product[props]);
   }
  ```
  - What is a method on an object?
  - How do you define methods?
  - How do you call/invoke a method?
  
  
  
- What is a function?
  - How do you define functions?
  ```
  * 방법1 (방법 1로 함수를 선언한 경우, 함수 호출은 함수 선언 전 또는 함수 선언 후에 할 수 있음
  function example1 (argument1, argument2, ...) {
  
  }
  
  * 방법2 (방법 2로 함수를 선언한 경우, 함수 호출은 함수 선언 후에 해야 함)
  var example2 = function(argument1, argument2, ...) {
  
  }
  ```
  - How do you call/invoke/execute functions?
  ```
  함수이름(value1, value2,..);
  
   방법1 ex1)
  example1(value1, value2, ...);
  function example1 (argument1, argument2, ...) {
  
  }
  
  방법1 ex2)
 ```
 function example1 (argument1, argument2, ...) {
  
  }
 example1(value1, value2, ...);
 
 
 
 방법2 ex)
 var example2 = function(argument1, argument2, ...) {
  
 };
 example(value1, value2, ...);

  ```
  - How do you pass arguments into a function?  
  - What does the return keyword do in a function?
  ```
  1. 반환값을 반환하는데 사용
  2. 지역변수를 알수있는데 사용
  3. 현재 진행중인 함수를 중지(탈출)할 수 있음
  ```

---
## Reference
[ Learning Javascript from Scratch (The Baby Phase)](https://zellwk.com/)
