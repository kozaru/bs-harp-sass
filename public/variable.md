読み込むVariableファイルをまとめたscssファイル。  
variableファイルを追加した際は、ここに追記します。  
追加するvariableファイルは[`/assets/css/foundation/variable/`](/cssFoundation/variable.html)内に作成します。

```
// Bootstrap variables
@import "foundation/vendor/bootstrap/bootstrap/variables";

// Foundation variables
@import "foundation/variable/[filename]";

// Bootstrap variables + override (Foundation variables)
@import "foundation/variable/bootstrap_override";
```
