# Bs-Harp-Sass

Harp + browser-sync + Bootstrap-Sass

## Install

### 1. Node.js

[Node.js](http://nodejs.org/)

### 2. Harp

[Harp](http://harpjs.com/) - the static web server with built-in preprocessing
```
$ sudo npm install -g harp
```

### 3. Download Bs-Harp or git clone Bs-Harp

### 4. Install some node-module
```
$ npm install
```

## Usage

### Start using LiveReload

Start http://localhost:9000

```
$ harp server
```

and start proxying: http://localhost:9000 and http://localhost:3000

```
$ gulp server
```

### Write the code to jade files

When you write the code to jade files , there is a need to write root path.

```index.jade
img(src="/images/demo.png", alt="demo")
```

#### Finish using LiveReload

control + c

### Compile source

Compile source non-minify-html in /dist

If you don't need to convert relative path to the dist directory, you change config.relativePath to false in gulpfile.js.

```
$ gulp dist
```

## The Structure of Css

Coding rules are based on the following links.

- [styleguide](https://github.com/manabuyasuda/styleguide)
- [equip](https://github.com/manabuyasuda/equip)

## Change Log
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
