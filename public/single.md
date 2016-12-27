スタイルは基本的に/assets/css/style.scssで出力しますが、ページ特有のスタイルが多く出る場合は/assets/css/[pagename].scssのようにページ専用のスタイルシートを作ります。

上記のベース用のscssです。

```
root
└── assets/
    └── css/
        ├── style.scss
        ├── [pagename].scss
        ├── foundation/
        │   ├── base/
        │   ├── mixin/
        │   ├── variable/
        │   └── vender/
        ├── layout/
        └── object/
        　   ├── component/
        　   ├── project/
        　   ├── scope/
        　   └── utility/
```
