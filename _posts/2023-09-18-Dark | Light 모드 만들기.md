---
tags: [html,javascript]
---
```jsx
var count = 0;
      document.getElementById('DarkMode').addEventListener('click', function(){
        count += 1;
        if (count % 2 == 1){
          document.getElementById('DarkMode').innerHTML='light';
        }
        else {
          document.getElementById('DarkMode').innerHTML='Dark';
        }
      });
```

var 변수로 홀수로 눌렀을 때 light 버튼으로, 그외 (짝수 클릭)을 Dark 버튼으로 바꾸는 코드이다.

어느정도 적응이 된것같은데, 자꾸 사소한 부분에서 실수를 한다.

count 를 0으로 할당하고 `count += 1;` 로 버튼을 누를때마다 **1씩 증가**시킨다. 

```jsx
var count = 0;
      $('#DarkMode').on('click', function(){
        count += 1;
        if (count % 2 == 1){
          $('#DarkMode').html('light');
        } else {
          $('#DarkMode').html('Dark');
        }
      });
```

**제이쿼리**로 바꿔서 적었다.

## 변수의 선언과 할당

| `var` | Function-scoped | 재선언 O | 재할당 O |
| `let` | {Block-scoped} | 재선언 X | 재할당 O |
| `const` | {Block-scoped} | 재선언 X | 재할당 X |
