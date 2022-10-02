# 📚 Javascript 클래스
---
## 생성자 함수 (Prototype)
생성자 함수는 여러개의 동일한 프로퍼티를 가지는 객체를 생성하기위해서 사용됩니다.
같은 객체 데이터를 반복해서 사용할 경우 많은 메모리를 차지하기 때문에 생성자 함수를 사용하는 것이 유용합니다.

### `new`
`new` 키워드를 사용하면 객체데이터가 생성 됩니다. 생성자 함수의 첫 글자는 대문자로 작성하는 Pascal case 표기를 해야합니다.(컨벤션)

인스턴스 : new 키워드를 통해 실행된 결과를 반환해 할당되는 변수를 인스턴스라고 합니다.

### `this`
`this`는 객체 자신의 프로퍼티나 메서드를 참조하기 위한 자기 참조 변수입니다.

#### `this` 바인딩 알아보기!

1. 기본 바인딩
전역 객체에 바인딩됩니다.

2. 암시적 바인딩
해당 함수를 호출한 객체에 바인딩됩니다.

3. 명시적 바인딩
`call()`, `apply()`, `bind()` 메소드로 호출합니다.

4. `new` 바인딩
새로 생성된 객체의 프로퍼티로 바인딩됩니다.

5. 화살표 함수
화살표 함수를 정의하는 시점의 컨텍스트 객체가 바인딩됩니다.

### `prototype`
`prototype`을 사용해서 메소드를 생성합니다.

```js
function User (first, last) {
  this.firstName = first
  this.lastName = last
}

User.prototype.getFullName = function () {
  return `${this.firstName} ${this.lastName}`
}

const mudi = new User('mudi', 'woo') // new	키워드로 'mudi' 인스턴스 생성
```

> 참고자료
[this 바인딩](https://seungtaek-overflow.tistory.com/21)
