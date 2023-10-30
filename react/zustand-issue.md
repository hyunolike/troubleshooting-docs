## 문제 
1. 라이브러리 가져오는 방법
2. `auto-zustand-selectors-hook` 사용 시 변수로 선언해서 사용

## 해결
1. 아래 처럼 중괄호 넣어주자


```js
import { createSelectorHooks } from 'auto-zustand-selectors-hook';
import { create } from 'zustand'; // 상태관리 라이브러리
import { produce } from 'immer'; // 불변성 라이브러리
```


2. 위와 동일


```js
  //#region  //*=========== Store ===========
  const open = useDialogStore.useOpen();
  const state = useDialogStore.useState();
  const handleClose = useDialogStore.useHandleClose();
  const handleSubmit = useDialogStore.useHandleSubmit();
  //#endregion  //*======== Store ===========

```
