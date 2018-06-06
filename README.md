# vue-autokana-sample

vue.jsで自動でふりがなを入力するためのサンプルになります。

利用ライブラリは、「terrierscript/historykana」になります。

https://github.com/terrierscript/historykana

``` bash
npm i historykana
```
で導入します。

サンプルでは、v-on:inputで文字入力イベントを拾っていますが、
IMEが確定するまでは、v-modelで紐づけた値(サンプル内では、this.name)には値が入りません。
このため取得したeventオブジェクトから、
実際に入力されている値を取得しています。

# デモ画面

https://idani.github.io/vue-autokana/

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
