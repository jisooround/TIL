# 📚 조건문 (If Statement)
조건문은 조건에 따라 명령을 실행할지 말지 판단합니다.

---
## If문
조건이 참일 때 명령을 실행하고 싶다면 if문을 사용하시면 됩니다.

예를 들어 시험 점수가 80점 이상일 때 '합격입니다.'라는 문자가 나오게 실행하려고 합니다.
```js
function pass(name, score) {
  if (score >= 80) { 
    alert(name + '님은 합격입니다.')
  }
}

pass('경민',90) // 경민님은 합격입니다.
```


### If...Else문
불합격을 알리는 명령을 하고싶다면 else 뒤에 명령을 추가하면 됩니다.

```js
function pass(name, score) {
  if (score >= 80) { 
    alert(name + '님은 합격입니다.')
  } else { 
    alert(name + '님은 불합격입니다.')
  }
}

pass('윤찬',65) // 윤찬님은 불합격입니다.
pass('경민',90) // 경민님은 합격입니다.
```

### Else if문
이번에는 아래 조건에 따라 등급을 알려줘보겠습니다.

95점 이상은 A
85점 이상은 B
75점 이상은 C
그 이하는 '재수강입니다.'
```js
function pass(name, score) {
  if (score >= 95) { 
    alert(name + '님의 등급은 A입니다.')
  } else if (score >= 85) { 
    alert(name + '님의 등급은 B입니다.')
  } else if (score >= 75) { 
    alert(name + '님의 등급은 C입니다.')
  } else { 
    alert(name + '님은 재수강입니다.')
  }
}

pass('연우',78) // 연우님의 등급은 C입니다.
pass('경민',100) // 경민님의 등급은 A입니다.
pass('지수',74) // 지수님은 재수강입니다.
```

else if문에도 if문과 비슷한 맥락으로 조건을 걸고, 조건에 모두 부합하지 않으면 else 명령을 실행하게 됩니다.

---
## Switch문
Switch문에서는 일치, 불일치 여부만을 확인하여 명령을 실행합니다.
If문 보다 간결한 작성이 가능합니다.

**case 작성법**
`case 확인할 일치 대상을 작성 : 일치하면 실행할 명령문을 작성`
`break`

**모든 case가 불일치일 경우**
마지막에 `default`에 출력할 명령을 작성합니다. if문의 else와 비슷한 역할입니다.

```js
function mbti (a) {
  switch(a) {
    case 'ENFP': console.log('당신은 재기발랄한 활동가입니다.')
    break
    case 'ISFJ': console.log('당신은 용감한 수호자!')
    break
    case 'ISTP': console.log('당신은 만능 재주꾼이군요')
    break
    default : console.log('대문자로 다시 작성해주세요!')
  }
}

mbti('ENFP') // 당신은 재기발랄한 활동가입니다.
mbti('CUTE') // 대문자로 다시 작성해주세요!

```
<br>

