## 문제
- Uncaught TypeError: Failed to execute "appendChild" on "Node"

## 해결
- `appendChild` 노드만 받음!


```js
var todo = `<div >${text}</div>`; // -> string
document.querySelector('#todo-list').appendChild(todo);

var $div = document.createElement('div'); // -> node
$div.innerHTML = text;
document.querySelector('#todo-list').appendChild($div);
```
