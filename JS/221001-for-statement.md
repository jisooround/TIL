# ๐ ๋ฐ๋ณต๋ฌธ (For Statement)
๋ฐ๋ณต๋ฌธ์ ๋ช๋ น์ ๋ฐ๋ณตํด์ ์ํํ๋๋ก ํ๋ ์ ์ด๋ฌธ์๋๋ค.

**์คํ ์์**
1. ์์ ์กฐ๊ฑด์ ๋ง๊ฒ ์์๋ฉ๋๋ค.
2. ์กฐ๊ฑด์ด true์ด๋ฉด ๋ฐ๋ณต๋ฌธ ๋ณธ๋ฌธ์ ์คํํฉ๋๋ค.
3. ๊ทธ ์ดํ ๋ณํ ์กฐ๊ฑด์ ๋ง๊ฒ ์คํ๋ฉ๋๋ค.
4. ๋ณํ ์กฐ๊ฑด์ ๋ง๊ฒ ์คํ๋ ๊ฐ์ผ๋ก ๋ค์ ์์..
5. ์กฐ๊ฑด์ด true์ด๋ฉด ๋ฐ๋ณต๋ฌธ ๋ณธ๋ฌธ ์คํ... (์ด ๊ฐ์ด false์ผ ๋ ๊น์ง ์คํํฉ๋๋ค.)

```js
for (์์์กฐ๊ฑด; false๊ฐ ๋๋ฉด ์ข๋ฃ; ๋ณํ์กฐ๊ฑด) {
	๋ฐ๋ณต๋ฌธ ๋ณธ๋ฌธ
 }
 ```
๐ **1๋ถํฐ 10๊น์ง์ ์ซ์ ์ค ์ง์๋ง ์ถ๋ ฅํ๊ธฐ**

```js
for (i = 2; i < 11 ; i++) {
  if (i % 2 == 0) {
    alert(i)
  }
} // 2,4,6,8,10
```
