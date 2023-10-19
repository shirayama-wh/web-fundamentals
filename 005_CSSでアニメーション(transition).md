# CSSでアニメーション(transition)

## transitionプロパティの使い方

transitionプロパティを使えば簡単にアニメーションを実現できます。  
transitionは:hoverや:activeなどのトリガー必要になります。

```css
.button a {
    display: inline-block;
    text-decoration: none;
    font-size: 20px;
    padding: 15px;
    color: #ffffff;
    background-color: #1A60BF;
    transition: all 0.5s 0s ease;/*transitionの記述を追加*/
}
.button a:hover {
    color: #1A60BF;
    background-color: #D0E2FB;
}
```

プロパティ名: 説明  
transition-property: 指定要素の度のプロパティにアニメーションを適用するかを定義する  
transition-duration: アニメーションの時間を定義する  
transition-delay: アニメーションを開始するタイミングを定義する  
transition-timing-function: アニメーション変化の度合を定義する  

transition-timing-functionの種類  
値: 説明  
ease: 開始時と終了時にはゆっくり変化（初期値）  
ease-in: 開始時はゆっくり変化し、終了時は早く変化  
ease-out: 開始時に早く、終了時にゆっくり変化  
ease-in-out: easeよりさらに、開始時と終了時はゆっくり変化  
linear: 速度が変わることなく一定に変化  
cubic-bezier(x軸の値, y軸の値, x軸の値, y軸の値): 変化の度合いをベジェ曲線により任意で指定
