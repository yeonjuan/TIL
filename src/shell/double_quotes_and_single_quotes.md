# 쉘에서 작은 따옴표 (`'`), 큰 따옴표 (`"`) 차이

작은 따옴표로 감싸진 문자열은 그대로 출력된다.

```bash
echo '$((1+1))' # $((1+1)) 출력
```

- 큰 따옴표로 감싸진 문자열은 `$` 과같은 문자를 특별 취급해 값, 커맨드, 계산 결과등으로 치환한다.

```bash
echo "$((1+1))" # 2 출력
```
