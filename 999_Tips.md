# Tips

## %とvwの違い
%は親が基準  
vwはブラウザの横幅が基準

## user agent stylesheetとは
「user agent stylesheet」とは、ブラウザ毎に定義されているデフォルトのCSS設定  
無効化するにはリセットCSSを適用

## input(type=checkbox)とlabelの連動
or属性の値は単一のidでなければいけない

```
<div class="preference">
    <label for="cheese">Do you like cheese?</label>
    <input type="checkbox" name="cheese" id="cheese">
</div>
```

labelの内側に入れると関連付けが明確なのでforおよびidが不要

```
<label>Do you like peas?
  <input type="checkbox" name="peas">
</label>
```


