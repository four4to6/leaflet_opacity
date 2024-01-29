# 複数の地図の切替と透過表示 (Leaflet)

## Description

「複数の地図の切替と透過表示 (Leaflet)」という記事で紹介しているJavaScript。

使用についての詳細は以下のURL(記事)を**必ずお読みください**。

「複数の地図の切替と透過表示 (Leaflet)」
http://loca.ash.jp/leaflet/leaflet_maps_opacity.htm

## 注意事項

### 前提として

- **ご使用にあたり「全ては自己責任で行う」これが前提です。当方は一切の責任を負いかねます。**

## プログラムの概要

以下、「複数の地図の切替と透過表示 (Leaflet)」より**引用**。

> 標準のマップ切替コントローラを透過度設定付きのコントローラにカスタマイズしてみました。 プラグインを読込み、コントローラのクラス名を変えるだけで、透過度設定が可能になります。 透過度設定は、オーバーレイマップ切替のチェックボックスをチェックすると、透過度設定のスライダが表示され、透過度の変更が可能となります。このサンプルでは、自作プラグインを利用しています。 このページのプラグインをダウンロードすることで、すぐに利用できます。 ただ、Leaflet Ver1.7.1で動作確認を行っています。 Leaflet本体を拡張して作成し、非公開の内部変数も参照しているため、Leafletのバージョンが変わると動作しない可能性があります。 その点だけは、ご注意ください。

## ソースの説明

以下、「複数の地図の切替と透過表示 (Leaflet)」より**引用**。

> JavaScriptのソースの「L.control.layers」を「L.control.opacityLayers」に変えるだけです。

```JavaScript:JavaScript
L.control.opacityLayers(baseCtl, overCtl, {collapsed:true}).addTo(map); // 透過付マップ切替
```

## 処理概要

以下、「複数の地図の切替と透過表示 (Leaflet)」より**引用**。

> leaflet_opacityプラグインは、Control.layersを拡張して作成しました。 Control.layersは、地図切替ボタンを表示するときに、オーバーレイマップに対してチェックボックスを作成しています。 その作成時の処理をオーバーライドして、デフォルト処理を実行後、透過度変更用のスライダを追加する処理を追加しています。 スライダの属性にレイヤIDを格納することにより、スライダ変更時に、どのスライダが変更されたかを調べて、透過度の変更を行っています。leaflet_opacityプラグインに変更すると、Leafletの地図切替コントローラが生成するソースに、`<input type="range">`タグが追加されるようになります。

## Example

### CDN
```html:JavaScript
https://cdn.jsdelivr.net/gh/four4to6/leaflet_opacity@latest/data/leaflet_opacity.js
```

```html:CSS
https://cdn.jsdelivr.net/gh/four4to6/leaflet_opacity@latest/data/leaflet_opacity.css
```

### JSFiddle
https://jsfiddle.net/sfk7p4jw/


## 著作・出典 等

### 複数の地図の切替と透過表示 (Leaflet)
http://loca.ash.jp/leaflet/leaflet_maps_opacity.htm

### Leaflet - a JavaScript library for interactive maps:
https://leafletjs.com/

### 地理院タイル一覧:
https://maps.gsi.go.jp/development/ichiran.html

