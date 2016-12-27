足りないものは適宜追加。
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

## _layout.scss：レイアウト用

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

## _list.scss：リスト用
[cssObject/component](/cssObject/component.html)を参照

## _ratio.scss：ratio（伸縮box）用
[cssObject/component](/cssObject/component.html)を参照
