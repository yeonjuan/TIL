# 자바 스크립트 동적 로딩

브라우저 환경에서 자바스크립트를 동적으로 로딩해야 할 때 다음과 같은 방법을 쓸 수 있다.
```js
var script = document.createElement('script');
script.type = 'text/javascript';
script.url = '...'; // script url.
document.body.appendChild(script);
```

스크립트 로딩 완료에 대한 콜백과, 구 IE 에서도 동작을 원하면 다음과 같이 사용하면 된다.

```js
function loadScript (url, callback) {
  var script = document.createElement('script');
  script.type = 'text/javascript';

  if (script.readyState) { // IE < 11
    script.onreadystatechange = function() {
      if (script.readyState === 'loaded' || script.readyState === 'complete') {
          script.onreadystatechange = null;
          callback();
        }
    }
  } else { // Others
    script.onload = function () {
      callback();
    }
  }

  script.src = url;
  document.body.appendChild(script);
}
```
* 모던 브라우저와, IE 11 이후는 script 의 readyState 를 지원하지 않는다. - [참고](http://help.dottoro.com/ljcecmhr.php)

### 참고
* [The best way to load external JavaScript](https://humanwhocodes.com/blog/2009/07/28/the-best-way-to-load-external-javascript/)



