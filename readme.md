# Bs-Harp-Sass

Harp + browser-sync + Bootstrap-Sass

## Install（インストール）

### 1. Node.js and npm（Node.jsをインストール）

[Node.js](http://nodejs.org/)

### 2. Harp（Harpをインストール）

[Harp](http://harpjs.com/) - the static web server with built-in preprocessing

```
$ sudo npm install -g harp
```

### 3. bs-harp-sass repository（Download or git clone）（bs-harp-sass リポジトリをダウンロード、または git clone）


### 4. Install some node-module（node-moduleをインストール）

```
$ cd bs-harp-sass
$ npm install
```

## Usage（使い方）

### Start using LiveReload（LiveReloadの使い方）

Start harp server（harp server を起動）

```
$ harp server
```

and open a new tab（新しいタブを開く）

command + t


Start proxy of harp server using browsersync Livereload on that tab（そのタブでbrowsersync Livereloadを使って harp server のプロキシを開始）

```
$ gulp server
```

### Write the code to jade files or the content to markdown files（jadeファイルにコードを書く または、マークダウンするコンテンツを書く）

When you write the code to jade files , there is a need to write root path.（jadeファイルにコードを書くときには、ルートパスを書く必要がある）

```_layout.jade
img(src="/assets/images/demo.png", alt="demo")
```

#### Finish LiveReload and harp server（LiveReloadとハープサーバーを終了する）

On the corresponding tab（該当タブで）

control + c

### Compile source（コンパイル方法）

Compile source non-minify-html in /dist（コンパイルされたHTMLは  /distディレクトリ内に保存され　non-minify-html になる）

If you don't need to convert relative path to the dist directory, you change config.relativePath to false in gulpfile.js.（相対パスを`dist`ディレクトリに変換する必要がない場合は、gulpfile.jsでconfig.relativePathをfalseに変更）

```
$ gulp dist
```

## The Structure of Css（Css構造）

Coding rules are based on the following links.（コーディング規則は、以下のリンクをベースに作成）

- [styleguide](https://github.com/manabuyasuda/styleguide)
- [equip](https://github.com/manabuyasuda/equip)

## Change Log

### v.1.0.3 (2016.12)
Add Japanese to Readme

### v.1.0.2 (2016.12)
Change the structure of css
Change all indent_style to 2space
Change Compile source

### v.1.0.1 (2016.6)
Fix bugs

### v.1.0.0 (2016.5)


## Change Log [Bs-Harp](https://github.com/kozaru/bs-harp)

### v.1.4 (2016.1)
Use Bootstrap Sass

### v.1.3.2 (2016.1)
Install gulp-autoprefixer
Use browser-sync with gulp

### v.1.3.1 (2016.1)

Use gulp-cssnano instead of gulp-minify-css
Install gulp-sourcemaps

### v.1.3.0 (2016.1)

Install JS and css libraries from npm

### v.1.2.0 (2015.7)

It is possible to convert relative path, even if there are lower directories.

### v.1.1.0 (2015.4)

#### add
- gulp-csscomb
- gulp-minify-css
- gulp-uglify
- .editorconfig
- .jsbeautifyrc
- .jshintrc
- .tern-project

#### fix or update
- gulp-html-prettify
