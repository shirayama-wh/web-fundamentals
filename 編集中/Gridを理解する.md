# Gridを理解する

## Gridとは
Gridは、親要素(コンテナ)を縦横の2次元のグリッドに分割し、その中に子要素(アイテム)を配置することができます。

## Gridの基本
Gridは親(コンテナ)と子(アイテム)の2つの要素から構成されています。

```<div class="gr-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
</div>
```

Gridを使用する場合は、CSSファイルで親要素（コンテナ）にdisplay:gridを指定します。
細かいレイアウトの調整は、コンテナとアイテムにそれぞれプロパティを指定して調整を行います。

```.wrapper {
    display: grid;
}
```

##　Gridのプロパティ一覧
コンテナ(親要素)に使用できるプロパティ一覧
|プロパティ|説明|
|---|---|
|grid-template-columns|行の数と幅を定義を指定|
|grid-template-rows|列の数と高さを定義を指定|
|grid-template-areas|要素の配置を指定|
|column-gap|要素の横のスペースを指定|
|row-gap|要素の縦のスペースを指定|
|justify-items|主軸の要素の配置を指定|
|align-items|交差軸の要素の配置を指定|
|justify-content|コンテナ内の主軸のグリッドの配置を指定|
|align-content|コンテナ内の交差軸のグリッドの配置を指定|

アイテム(子要素)に使用できるプロパティ一覧
|プロパティ|説明|
|---|---|
|grid-column-start/end、grid-row-start/end|複数の行・列を結合|
|grid-area|grid-template-areasの名前を定義|
|justify-self|コンテナ内の主軸のアイテムの配置を指定|
|align-self|コンテナ内の交差軸のアイテムの配置を指定|









