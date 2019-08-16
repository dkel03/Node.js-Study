### ECMAScript2015 문법
---

#### 1. var와 const, let의 차이
- var는 함수 scope
- const, let은 블럭 scope
- const는 한번 선언 이후 변경 x
- let은 선언이후에도 변경 가능
- const는 선언 시에 초기화 해야함.
- const에 객체가 할당된 경우 객체 내부 속성은 변경가능

#### 2. 백틱(템플릿 문자열)

>  ` ` ` 기호

- 변수는 ${변수}로 사용하고 나머지는 문자열을 만들면됨.
- template string은 백틱이라서 이스케이핑 구문이 필요하지 않다!
- 따옴표, 작은 따옴표 등을 내부에 그대로 삽입가능

- ex) const e = \`${a}의 값은 ${b}이고 ${c}는 몰라요`


#### 3. 객체리터럴의 변화

#### 4. 화살표 함수
```
function add1(x,y){
	return x+y;
};
```
```
const add2 = (x,y) => {
	return x+y;
};
```
- 화살표 함수는 function과 살짝 다르다
- 리턴 값이 없는 경우에는 아래처럼 쓸 수도 있다.
```
const add3 = (x,y) => x + y;
```
- ES6에서는 가독성을 높이기 위한 문법이 추가 되었다.
- function과 화살표 함수는 `this`의 사용법이 다르다.
- 화살표 함수는 함수 내부의 `this`를 외부의 `this`와 같게 만들어 줌.