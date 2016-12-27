[Bootstrap](http://getbootstrap.com/)から読み込むスタイルをまとめたscssファイル。  
navbar は 説明用に読み込んでいるので、不要な場合はコメントアウトする。  
その他のComponentsで必要なものは、コメントをはずす。

```
// Reset and dependencies
@import "foundation/vendor/bootstrap/bootstrap/normalize";

// Core CSS
@import "foundation/vendor/bootstrap/bootstrap/scaffolding";
@import "foundation/vendor/bootstrap/bootstrap/type";
@import "foundation/vendor/bootstrap/bootstrap/code";
@import "foundation/vendor/bootstrap/bootstrap/grid";
@import "foundation/vendor/bootstrap/bootstrap/tables";
@import "foundation/vendor/bootstrap/bootstrap/forms";
@import "foundation/vendor/bootstrap/bootstrap/buttons";

// Components
@import "foundation/vendor/bootstrap/bootstrap/component-animations";

// Bootstrapのnavbarを使用しない場合は、コメントアウトする
@import "foundation/vendor/bootstrap/bootstrap/dropdowns";

// Bootstrapのnavbarを使用しない場合は、コメントアウトする
@import "foundation/vendor/bootstrap/bootstrap/navs";

// Bootstrapのnavbarを使用しない場合は、コメントアウトする
@import "foundation/vendor/bootstrap/bootstrap/navbar";


// Utility classes
@import "foundation/vendor/bootstrap/bootstrap/utilities";
@import "foundation/vendor/bootstrap/bootstrap/responsive-utilities";
```
