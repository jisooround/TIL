# π Javascript ν΄λμ€
---
## μμ±μ ν¨μ (Prototype)
μμ±μ ν¨μλ μ¬λ¬κ°μ λμΌν νλ‘νΌν°λ₯Ό κ°μ§λ κ°μ²΄λ₯Ό μμ±νκΈ°μν΄μ μ¬μ©λ©λλ€.
κ°μ κ°μ²΄ λ°μ΄ν°λ₯Ό λ°λ³΅ν΄μ μ¬μ©ν  κ²½μ° λ§μ λ©λͺ¨λ¦¬λ₯Ό μ°¨μ§νκΈ° λλ¬Έμ μμ±μ ν¨μλ₯Ό μ¬μ©νλ κ²μ΄ μ μ©ν©λλ€.

### `new`
`new` ν€μλλ₯Ό μ¬μ©νλ©΄ κ°μ²΄λ°μ΄ν°κ° μμ± λ©λλ€. μμ±μ ν¨μμ μ²« κΈμλ λλ¬Έμλ‘ μμ±νλ Pascal case νκΈ°λ₯Ό ν΄μΌν©λλ€.(μ»¨λ²€μ)

μΈμ€ν΄μ€ : new ν€μλλ₯Ό ν΅ν΄ μ€νλ κ²°κ³Όλ₯Ό λ°νν΄ ν λΉλλ λ³μλ₯Ό μΈμ€ν΄μ€λΌκ³  ν©λλ€.

### `this`
`this`λ κ°μ²΄ μμ μ νλ‘νΌν°λ λ©μλλ₯Ό μ°Έμ‘°νκΈ° μν μκΈ° μ°Έμ‘° λ³μμλλ€.

#### `this` λ°μΈλ© μμλ³΄κΈ°!

1. κΈ°λ³Έ λ°μΈλ©
μ μ­ κ°μ²΄μ λ°μΈλ©λ©λλ€.

2. μμμ  λ°μΈλ©
ν΄λΉ ν¨μλ₯Ό νΈμΆν κ°μ²΄μ λ°μΈλ©λ©λλ€.

3. λͺμμ  λ°μΈλ©
`call()`, `apply()`, `bind()` λ©μλλ‘ νΈμΆν©λλ€.

4. `new` λ°μΈλ©
μλ‘ μμ±λ κ°μ²΄μ νλ‘νΌν°λ‘ λ°μΈλ©λ©λλ€.

5. νμ΄ν ν¨μ
νμ΄ν ν¨μλ₯Ό μ μνλ μμ μ μ»¨νμ€νΈ κ°μ²΄κ° λ°μΈλ©λ©λλ€.

### `prototype`
`prototype`μ μ¬μ©ν΄μ λ©μλλ₯Ό μμ±ν©λλ€.

```js
function User (first, last) {
  this.firstName = first
  this.lastName = last
}

User.prototype.getFullName = function () {
  return `${this.firstName} ${this.lastName}`
}

const mudi = new User('mudi', 'woo') // new	ν€μλλ‘ 'mudi' μΈμ€ν΄μ€ μμ±
```

> μ°Έκ³ μλ£
[this λ°μΈλ©](https://seungtaek-overflow.tistory.com/21)
