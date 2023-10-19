# CSSで横並び

* floatで横並びにする方法  
* flexboxで横並びにする方法  
* inline-blockで横並びにする方法

## floatで横並びにする方法

追加予定

## flexboxで横並びにする方法

折り返し方の指定(flex-wrap)  
nowrap: flexアイテムを折り返さない（デフォルト）  
wrap: flexアイテムを折り返す（左から右）  
wrap-reverse: flexアイテムを折り返す（右から左）

```css
.contents {
    display: flex; /* 横並び */
    flex-wrap: wrap;
    width: 100%;
    background-color: bisque;
    height: 85vh
}

.item {
    width: calc(100% / 5);
    padding: 2vh;
    text-align: center;
}
```

flex-flowは「flex-direction」と「flex-wrap」の2つのプロパティを一括にまとめることができる  
flex-directionの値: 「row（初期値）」「row-reverse」「column」「column-reverse」  
flex-wrapの値: 「nowrap（初期値）」「wrap」「wrap-reverse」

```css
.sample{
    flex-direction: row;
    flex-wrap: wrap;
}
```

↓

```css
.sample{
    flex-flow: row wrap;
}
```

## inline-blockで横並びにする方法

追加予定
