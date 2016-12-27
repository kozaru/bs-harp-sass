
```
foundation/
├── base/
├── mixin/
├── variable/
└── vender/
```

---

## baseレイヤー
Foundationレイヤー・baseレイヤーでは、htmlやbodyのような広範囲にわたるベーススタイル、h2やulのような基本的なタイプセレクタのデフォルトスタイルを定義。

### [Bootstrap](/bootstrap.html)・[`css/component`](http://getbootstrap.com/css/)

- normalize
- scaffolding

---

## mixinレイヤー
mixinデータを保存します。

ファイルを追加した場合は、[`/assets/css/_mixin.scss`](/mixin.html)に追加します。

新規に追加する場合は、object内の各scssファイルをベースにファイルを作成

```
├── _layout.scss  // レイアウト用
├── _list.scss    // リスト用
└── _ratio.scss   // ratio（伸縮box）用
```

mixinの引数は、原則、`$_`にしない。通常のvariableとの差別化。
mixin名は、[ファイル名]-[バリエーション名]など
```
// [filename]
// 引数名：$padding-bottom
@mixin ratio($padding-bottom: 100%) {
  display: block;
  overflow: hidden;
  position: relative;
  &:before {
    content: "";
    display: block;
    width: 100%;
    padding-bottom: unquote($padding-bottom);
  }
}

// [filename]-[name]
@mixin ratio_content() {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
```

### _layout.scss：レイアウト用

`variable/_breakpoint.scss`で設定した xs/sm/md/lgのパターンを使用

上記ファイルを変更しない場合は、Bootstrapベース
```
// xs（スマフォ最小幅）のmax以下
@include layout-max('xs'){
   // style
};

// lg（pc最大幅）のmin以上
@include layout-min('lg'){
   // style
};

// sm（タブレット）サイズ（max/minを設定）
@include layout-maxmin('sm') {
   // style
}
```

pxを設定
```
// 400px以下
@include layout-max-px('400px'){
   // style
};

//　800px以下
@include layout-min-px('800px'){
   // style
};

// 600px以上、800px以下
@include layout-maxmin-px('600px','800px') {
   // style
}
```

### _list.scss：リスト用
[cssObject/component](/cssObject/component.html)を参照

### _ratio.scss：ratio（伸縮box）用
[cssObject/utility](/cssObject/utility.html)を参照


---

## variableレイヤー

variableデータを保存します。

ファイルを追加した場合は、[`/assets/css/_variable.scss`](/variable.html)に追加します。

### variableネーミングルール
- general / prefix `$_`
  - column
  - font-size
  - radius
  - line-height-base
  - duration
- general以外 / prefix `$_[filename]-`
- prefix以降のつなぎ目は `-`


### ファイル構成

必要に応じて順次追加、追加時には [`assets/css/_variable.scss`](/variable.html) からimportする

```
├── _global.scss               //グローバル（Bootstrap上書あり）
├── _breakpoint.scss           //メディアクエリー（Bootstrap上書あり）
├── _font-family.scss          //フォントファミリー（Bootstrap上書あり）
├── _color.scss                //色（Bootstrap上書あり）
└── _bootstrap_override.scss   //Bootstrap上書用・上記に設定がないもの
```

### foundation/variable/global

#### A.Bootstrap：variableを上書き用
- $_column
- $_font-size
- $_radius
- $_line-height-base

#### Other（随時追加）
- $_duration

### foundation/variable/breakpoint

#### B.Bootstrap：variableを上書き用
- $_breakpoint-min
- $_breakpoint-max
- $_breakpoint-gutter-width
- $_breakpoint-container-base

#### Other
随時追加

### foundation/variable/font-family

#### C.Bootstrap：variableを上書き用
- $_font-family-base

#### Other（随時追加）
- $_font-family-maru
- $_font-family-kaku
- $_font-family-min

### foundation/variable/color

#### D.Bootstrap：variableを上書き用
- $_color-text
- $_color-bg
- $_color-link
- $_color-link-hover

#### Other
随時追加

### foundation/variable/bootstrap_override

A〜Dは設定済み

その他修正があれば、コメントをはずして、上書きする


---

## venderレイヤー
外部のライブラリやフレームワークを保存します。

ファイルを追加した場合は、`/assets/css/style.scss` 等に追加します。

### Bootstrap

Bootstrapファイル群：[`/assets/css/_bootstrap.scss`](/bootstrap.html)にて読込

2016.12：v3.3.7
