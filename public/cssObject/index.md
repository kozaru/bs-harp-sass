Objectレイヤーはプロジェクトにおけるビジュアルパターン。

4つのレイヤーにわけます

```
object
├── component/
├── project/
├── scope/
└── utility/
```

---

## component レイヤー
多くのプロジェクトで横断的に再利用できるような小さな単位のモジュール

### [Bootstrap](/bootstrap.html)
大半を[Bootstrap](/bootstrap.html)の以下の[`css/component`](http://getbootstrap.com/css/)で補います。

- Typography
- Code
- Tables
- Forms
- Buttons
- Images

### Other

プレフィックス（接頭辞）:`c-[filename]`

ファイルを追加した場合は、`/assets/css/style.scss` に追加します。

#### list
プレフィックス（接頭辞）:`c-list`


---

## project レイヤー

プロジェクト固有のスタイル（各ブロックやテーマに埋めこむパーツごとにファイルを作成）

プレフィックス（接頭辞）:`p-[filename]`

ファイルを追加した場合は、`/assets/css/style.scss` に追加します。


```
├── _box.scss
└── _btn.scss
````

### _box.scss
画像やテキストなどを並べるコンポーネントです。

プレフィックス（接頭辞）:`p-box`

### _btn.scss
a/button用のコンポーネントです。

プレフィックス（接頭辞）:`p-btn`

---

## scope レイヤー

classセレクタと要素セレクタの子孫セレクタでスタイルを指定する（記事ブロック/HTMLブロック用）

プレフィックス（接頭辞）:`s-[filename]`

ファイルを追加した場合は、`/assets/css/style.scss` に追加します。

---

## utility レイヤー

汎用クラス

### Bootstrap
[Bootstrap](/bootstrap.html)/[`css/component`](http://getbootstrap.com/css/)にて代用

- Grid system
- Helper classes
- Responsive utilities


### Other
プレフィックス（接頭辞）:`u-[filename]`

ファイルを追加した場合は、`/assets/css/style.scss` に追加します。

```
├── _margin.scss
├── _text.scss
└── _ratio.scss
```

### _mb.scss

マージンで余白の管理をします。常に下方向にだけ余白をとります。
`<section>`要素を使うようなセクションの余白はlayout/_section.scssで管理します。

プレフィックス（接頭辞）:`u-mb`

### _text.scss

プレフィックス（接頭辞）:`u-text`


### _ratio.scss

レスポンシブ用伸縮Box

プレフィックス（接頭辞）:`u-ratio`
