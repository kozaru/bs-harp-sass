## css構成
ファイルの構成は主に[FLOCSS](https://github.com/hiloki/flocss)がベース

FLOCSSはFoundation、Layout、Objectの3つのレイヤーとComponent、Project、Utilityの3つの子レイヤーから構成

```
root
└── assets/
    └── css/
        ├── style.scss
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
