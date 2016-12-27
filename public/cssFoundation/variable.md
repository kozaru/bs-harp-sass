
```
├── _global.scss               //グローバル（Bootstrap上書あり）
├── _breakpoint.scss           //メディアクエリー（Bootstrap上書あり）
├── _font-family.scss          //フォントファミリー（Bootstrap上書あり）
├── _color.scss                //色（Bootstrap上書あり）
└── _bootstrap_override.scss   //Bootstrap上書用・上記に設定がないもの
```

## foundation/variable/global
@import "foundation/variable/breakpoint";
@import "foundation/variable/font-family";
@import "foundation/variable/color";

// Bootstrap variables + override (Foundation variables)
@import "foundation/variable/bootstrap_override";
