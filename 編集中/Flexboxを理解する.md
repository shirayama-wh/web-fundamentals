# Flexboxを理解する

## Flexboxとは
Flexboxの正式名称は「Flexible Box Layout Module」と言い、CSS3から導入されたレイアウトモジュールです。
以前までは要素を横並びで配置したいときはfloatなどを使うことが一般的でしたが、最近ではFlexboxを使って要素を横並びに配置するようになりました。

## Flexboxの基本
Flexboxは親(コンテナ)と子(アイテム)の2つの要素から構成されています。

```<div class="fb-container">
  <div class="fb-item"></div>
  <div class="fb-item"></div>
  <div class="fb-item"></div>
  <div class="fb-item"></div>
</div>
```

Flexboxを使用する場合は、CSSファイルで親要素（コンテナ）にdisplay:flexを指定します。
細かいレイアウトの調整は、コンテナとアイテムにそれぞれプロパティを指定して調整を行います。

```.fb-container{
  display: flex;
}
```

##　Flexboxのプロパティ一覧
コンテナ(親要素)に使用できるプロパティ一覧
|プロパティ|説明|
|---|---|
|flex-direction|アイテムの並び順を指定|
|flex-wrap|アイテムの折り返しを指定|
|flex-flow|アイテムの並び順と折り返しを一括で指定|
|justify-content|アイテムの水平方向の配置を指定|
|align-items|アイテムの垂直方向の配置を指定|
|align-content|アイテムの行の垂直方向の配置を指定|

アイテム(子要素)に使用できるプロパティ一覧
|プロパティ|説明|
|---|---|
|order|アイテムの並び順を指定|
|flex-grow|アイテムの伸び率を指定|
|flex-shrink|アイテムの縮み率を指定|
|flex-basis|アイテムのベースの幅を指定|
|flex|アイテムの伸び率、縮み率、ベースの幅を一括指定|
|align-self|アイテムの垂直方向の位置を指定|

## コンテナ(親要素)のプロパティ(1) | flex-direction(アイテムの並び順)
flex-directionはアイテムを配置する向きを指定できます。
デフォルトは横並びでcolumnを指定すると縦並びになります。

|値|説明|
|---|---|
|row（デフォルト）|アイテムを水平方向に左から右へと配置|
|row-reverse|アイテムを水平方向に右から左へと配置|
|column|アイテムを垂直方向に上から下へと配置|
|colmn-reverse|アイテムを垂直方向に下から上へと配置|

## コンテナ(親要素)のプロパティ(2) | flex-wrap(アイテムの折り返し)
flex-wrapはアイテムの折り返しを指定できます。
デフォルトは折り返しさずに一列になっており、折り返す場合はwrapを指定します。
|値|説明|
|---|---|
|nowrap（デフォルト）|アイテムを折り返さずに一列に配置|
|wrap|複数行のアイテムを上から下へと配置|
|wrap-reverse|複数行のアイテムを下から上へと配置|

## コンテナ(親要素)のプロパティ(3) | flex-flow(アイテムの並び順と折り返しを一括指定)
flex-flowは、flex-directionとflex-wrapを一括で設定できます。

```.fb-container{
  flex-flow: [flex-directionの値] [flex-wrapの値];
}
```

## コンテナ(親要素)のプロパティ(4) | justify-content(水平方向の配置)
justify-contentは、水平方向の配置を指定します。

|値|説明|
|---|---|
|flex-start（デフォルト）|アイテムを左揃えで配置
|flex-end|アイテムを右揃えで配置|
|center|アイテムを左右中央揃えで配置|
|space-between|両端のアイテムを余白を空けずに配置し、他の要素は均等に間隔を空けて配置|
|space-around|両端のアイテムも含めて、均等な間隔を空けて配置|

## コンテナ(親要素)のプロパティ(5) | align-items(垂直方向の配置)
align-itemsは、垂直方向の配置を指定します。

|値|説明|
|---|---|
|stretch（デフォルト）|アイテムを上下の余白を埋めるように配置|
|flex-start|アイテムを上揃えで配置|
|flex-end|アイテムを下揃えで配置|
|center|アイテムを上下中央揃えで配置|
|baseline|アイテムをベースラインに合わせて配置|

## コンテナ(親要素)のプロパティ(6) | align-content(複数行の時の垂直方向の配置)
align-contentは、複数行の時の垂直方向の配置を指定します。

|値|説明|
|---|---|
|stretch（デフォルト）|アイテムの行を余白を埋めるように配置|
|flex-start|アイテムの行を上揃えで配置|
|flex-end|アイテムの行を下揃えで配置|
|center|アイテムの行を上下中央揃えで配置|
|space-between|最上行と最下行のアイテムを余白を空けずに配置し、他のアイテム行は均等に間隔を空けて配置|
|space-around|最上行と最下行のアイテムを余白を空けずに配置し、他のアイテム行は均等に間隔を空けて配置|

## アイテム(子要素)のプロパティ(1) | order(並び順)
デフォルトはHTMLの記述順ですが、orderを指定することで要素の並び順を指定できます。

```.fb-item01 {order: 3;}
.fb-item02 {order: 1;}
.fb-item03 {order: 4;}
.fb-item04 {order: 2;}
```

## アイテム(子要素)のプロパティ(2) | flex-grow(伸び率)
子要素を配置して余白ができたときに幅を広げて余白を埋める時の伸び率を指定します。

```.fb-item01 {flex-grow:3;}
.fb-item02 {flex-grow:1;}
.fb-item03 {flex-grow:4;}
.fb-item04 {flex-grow:2;}
```

## アイテム(子要素)のプロパティ(3) | flex-shrink(縮み率)
flexboxは子要素が親要素からはみ出す場合、子要素を縮めて収めようとします。その時の縮み率を指定します。

```.fb-item01 {flex-shrink:1;}
.fb-item02 {flex-shrink:2;}
.fb-item03 {flex-shrink:1.5;}
.fb-item04 {flex-shrink:1;}
```

## アイテム(子要素)のプロパティ(4) | flex-basis(ベースの幅)
flex-basisは、アイテムの基本幅を指定します。

```.fb-item01 {flex-basis:50%;}
.fb-item02 {flex-basis:20%;}
.fb-item03 {flex-basis:30%;}
.fb-item04 {flex-basis:40%;}
```


## アイテム(子要素)のプロパティ(5) | flex(伸び率、縮み率、ベースの幅を一括指定)
flexは、flex-grow、flex-shrink、flex-basisの3つの値をまとめて指定できます。

```.fb-item {
  flex: [flex-growの値] [flex-shrinkの値] [flex-basisの値];
}
```

## アイテム(子要素)のプロパティ(6) | align-self(垂直方向の配置)
align-selfは、アイテムの垂直方向の配置を指定します。
align-itemsは全体の縦の配置でしたが、align-selfは個々の配置になります。
align-selfは親要素のalign-itemsよりも優先されます。

|値|説明|
|---|---|
|auto（デフォルト）|親要素のalign-itemsの値を使用|
|flex-start|アイテムを上揃えで配置|
|flex-end|アイテムを下揃えで配置|
|center|アイテムを中央揃えで配置|
|baselne|アイテムをベースラインに合わせて配置|
|stretch|アイテムを上下の余白を埋めるように配置
