Модальное окно может быть реализовано с помощью полупрозрачного `<div id="cover-div">`, который полностью перекрывает всё окно:

```css
#cover-div {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 9000;
  width: 100%;
  height: 100%;
  background-color: gray;
  opacity: 0.3;
}
```

Так как он перекрывает вообще всё, все клики будут именно по этому `<div>`.

Также возможно предотвратить прокрутку страницы, установив `body.style.overflowY='hidden'`.

Форма должна быть не внутри `<div>`, а после него, чтобы она не унаследовала полупрозрачность (`opacity`).
