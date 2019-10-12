#  ECMA2018(ES9) Regex flag s

ECMA2018(ES9)에서 정규식에 `s flag` 가 추가되었다.  
`s flag` 의 기능은 정규식에서 `.`이 개행문자(`\n`)도 매칭시키도록 한다.

```js
// without s falg
console.log(/./.test('\n')); // false;

// with s flag
onsole.log(/./s.test('\n')); // true;
```
